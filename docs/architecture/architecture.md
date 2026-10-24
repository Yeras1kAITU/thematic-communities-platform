# Proposed Application Architecture

## 1. Purpose

The architecture is derived from:

- the approved requirements specification;
- the technology-alternatives comparison;
- the system context diagram;
- the use case diagram.

The architecture represents the planned structure of the system.


## 2. Architecture Style

The proposed backend architecture is a **modular monolith**.

The application is planned to be deployed as one primary backend application while separating major domain responsibilities internally.

The initial domain boundaries are:
- Auth & Users;
- Communities & Membership;
- Content & Discussions;
- Community Chat;
- Moderation.

This approach was selected in DIP-7 because it provides clear internal separation without introducing the operational complexity of a distributed microservice architecture.

## 3. High-Level Components

### 3.1 Web Client

The Web Client provides the user-facing interface.

Its responsibilities include:
- displaying community information;
- presenting publications and discussions;
- sending user actions to the backend;
- presenting community chat;
- maintaining the real-time chat connection.

### 3.2 REST API

The REST API is the primary request-response interface between the Web Client and the backend.

It is intended for operations including:
- registration;
- authentication;
- community discovery;
- community creation;
- membership;
- publications;
- comments;
- replies;
- moderation actions.

The REST layer is responsible for HTTP communication and input/output handling.

Business rules should remain within the appropriate application/domain modules rather than being concentrated in HTTP handlers.

### 3.3 WebSocket Gateway

The WebSocket Gateway provides the real-time communication interface required by community chat.

Its responsibilities include:
- establishing authenticated real-time connections;
- receiving chat-related client messages;
- delivering new chat events to connected clients;
- passing chat operations to the Community Chat module.

## 4. Application and Domain Modules

### 4.1 Auth & Users

The Auth & Users module is responsible for:
- account registration;
- authentication;
- user identity;
- consistent nickname information.

### 4.2 Communities & Membership

The Communities & Membership module is responsible for:

- community creation;
- community information;
- community discovery behavior;
- joining communities;
- leaving communities;
- ownership;
- membership;
- community roles.

Other modules may use community membership and role information when authorization decisions are required.

### 4.3 Content & Discussions

The Content & Discussions module is responsible for persistent community discussion functionality, including:
- publications;
- community publication feeds;
- comments;
- replies;
- user-owned content operations;
- publication-author relationships.

### 4.4 Community Chat

The Community Chat module is responsible for quick community communication.

Its responsibilities include:
- chat message creation;
- association of messages with communities and users;
- persistent chat history;
- chat-related business rules.

The WebSocket Gateway provides transport, while the Community Chat module owns the application behavior.

This module primarily supports FR-11 and FR-12.

### 4.5 Moderation

The Moderation module is responsible for authorized community moderation operations.

It uses community role information when deciding whether an operation is permitted and interacts with the content domain when content is moderated.

This module primarily supports FR-14.

## 5. Persistence

Application modules access persistent data through a defined persistence boundary.

The proposed structure is:
Application Module → Repository Interface / Persistence Adapter → PostgreSQL.

This separation is intended to avoid coupling HTTP transport or application behavior directly to database queries.

The exact repository interfaces and database schema will be defined during implementation.

Persistent data is expected to include:
- users;
- communities;
- memberships;
- roles;
- publications;
- comments;
- replies;
- chat messages;
- moderation-related data where required.

## 6. Main Communication Paths

### 6.1 Standard Application Operations

The planned request path for normal application operations is:

Web Client → REST API → Application Module → Persistence Layer → PostgreSQL.

Responses follow the reverse path.

### 6.2 Real-Time Chat

The planned real-time communication path is:
Web Client ↔ WebSocket Gateway → Community Chat → Persistence Layer → PostgreSQL.

The Community Chat module also uses membership information to determine whether the user is permitted to participate in the target community.

### 6.3 Moderation

A moderation operation follows the conceptual path:

Web Client → REST API → Moderation → Communities & Membership → Content & Discussions.

The moderation module uses:
- role information to verify authority;
- content information to identify and modify the target content.

## 7. Requirements Alignment

| Component | Main Requirement Areas |
|---|---|
| Web Client | User-facing interaction across functional requirements |
| REST API | HTTP access to account, community, content, and moderation operations |
| WebSocket Gateway | FR-11, FR-12 |
| Auth & Users | FR-01, FR-02, FR-16 |
| Communities & Membership | FR-03, FR-04, FR-05, FR-13 |
| Content & Discussions | FR-06, FR-07, FR-08, FR-09, FR-10, FR-15 |
| Community Chat | FR-11, FR-12 |
| Moderation | FR-14 |
| Persistence Layer | NFR-04 and persistent functional requirements |
| PostgreSQL | Persistent relational data |
| Operational Interfaces | NFR-06, NFR-11 |

Non-functional requirements such as security, reliability, maintainability, and testability apply across multiple components rather than belonging to a single module.

## 8. Technology Alignment

The architecture is consistent with DIP-7.

| Technical Decision | Architectural Representation |
|---|---|
| Go | Backend implementation |
| PostgreSQL | Primary persistent data store |
| REST-style HTTP/JSON | Standard browser-backend communication |
| WebSocket | Real-time community chat |
| Modular monolith | Internal backend organization |

## 9. Operational Direction

The architecture should support later reliability and SRE work without introducing unnecessary infrastructure during the first pre-defense stage.

The backend is expected to provide operational capabilities such as:
- health information;
- readiness information where appropriate;
- structured logs;
- basic application metrics.

These concerns are represented as operational interfaces rather than as a complete monitoring platform.

Specific monitoring backends, deployment infrastructure, alerting systems, and production topology are intentionally not selected in this document.

## 10. Architecture Boundaries

The proposed architecture intentionally does not introduce:
- microservices;
- distributed databases;
- mandatory caches;
- message brokers;
- container orchestration platforms.

These technologies may be evaluated later if a verified requirement or measured system behavior demonstrates a need for them.

## 11. Current Limitations

At the first pre-defense stage:

- the architecture is a design baseline;
- detailed Go package structure has not yet been finalized;
- database schema design is not defined by this document;
- deployment topology is not finalized;
- performance characteristics have not yet been measured;
- operational tooling has not yet been selected in detail.

These decisions will be refined during implementation and verification.

## 12. Summary

The proposed architecture uses:

- a browser-based Web Client;
- a Go modular-monolith backend;
- REST-style HTTP/JSON for standard application operations;
- WebSocket for community chat;
- separated domain modules;
- a defined persistence boundary;
- PostgreSQL for persistent relational data.
