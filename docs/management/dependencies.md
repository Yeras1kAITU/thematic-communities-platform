# Project Dependencies

## 1. Purpose

This document identifies dependencies between major project activities and deliverables of the Thematic Communities Platform.

The purpose is to prevent later work from being presented independently of the evidence and decisions on which it depends.

## 2. Deliverable Dependencies

### Research - Requirements

Potential-user research and literature analysis provide evidence for identifying user needs and project problems.

Relevant flow:

User research  
- research analysis  
- requirements.

The requirements must not be presented as if every design decision was directly requested by users.

### Existing Systems - Requirements and UX

Existing-platform analysis provides evidence about established approaches to:
- community organization;
- discussion;
- chat;
- moderation;
- discovery.

### Technology Comparison - Architecture

The approved technology baseline provides constraints for the proposed component architecture.

Current dependency:

Go  
+ PostgreSQL  
+ REST-style HTTP/JSON  
+ WebSocket  
+ Modular Monolith  
- Component Architecture.

### Requirements - Use Cases

The use-case model depends on the approved functional requirements.

### Requirements + Technology - Component Architecture

The component architecture depends on:
- functional responsibilities from the requirements;
- non-functional concerns;
- selected technology constraints.

### Requirements + Use Cases - UX Prototype

The UX prototype translates selected user-facing requirements into interface concepts.

Prototype-only features remain exploratory until requirements are formally updated.

### Requirements + Architecture + UX - Verification Plan

Verification procedures depend on:
- what the system is required to do;
- how responsibilities are structured;
- which user scenarios need evaluation.

## 3. Implementation Dependencies

The planned implementation has several logical dependencies.

### Authentication Before Protected Operations

Protected community operations require authenticated user identity.

Therefore:

Authentication  
- membership / content / moderation authorization.

### Community Model Before Community Content

Publications and chat require an existing community context.

Therefore:

Community creation  
- membership  
- publications / discussions / chat.

### Membership and Roles Before Moderation

Moderation permissions depend on community-specific roles.

Therefore:

Community membership and role model  
- moderation behavior.

### Publications Before Comments and Replies

Persistent discussion requires an existing publication.

Therefore:

Publication  
- comment  
- reply.

### Persistence Before Full Integration Verification

Integration tests for:
- membership;
- publications;
- comments;
- chat history;
- moderation

depend on the persistence implementation and test database environment.

## 4. Verification Dependencies

Verification results depend on an identifiable implementation baseline.

A valid result should therefore reference:
- tested Git commit or tag;
- test environment;
- relevant configuration;
- dataset where applicable;
- executed procedure.

### Performance Evaluation

Depends on:
- functioning implementation;
- stable test environment;
- repeatable test dataset;
- load-generation tooling.

### Usability Evaluation

Depends on:
- a sufficiently complete prototype or interface;
- defined user scenarios;
- participant instructions;
- evaluation procedure.

### Reliability Evaluation

Depends on:
- implemented health/failure behavior;
- controllable dependency failures;
- defined expected behavior.

## 5. Project-Management Dependencies

The normal task dependency is:

YouTrack issue  
- task branch  
- commits  
- pull request  
- review  
- merge  
- acceptance check  
- Done.

A task should not normally be marked `Done` while required review or acceptance checks remain incomplete.

## 6. Remaining First Pre-Defense Dependencies

Before the `pre-defense-1` baseline is finalized, the remaining work depends on the approved documentation baseline.

### DIP-15 - Review Prototype Implementation

Depends primarily on:
- DIP-8 requirements;
- DIP-11 architecture;
- DIP-12 visual prototype;
- DIP-13 verification plan.

The review should distinguish between:
- designed;
- visually prototyped;
- implemented;
- not yet implemented.

### DIP-16 - Collect and Address Supervisor Feedback

Depends on actual supervisor review evidence.

Feedback must not be invented.

Existing GitHub approvals and real review comments may be documented where appropriate.

### DIP-17 - Prepare Pre-Defense-1 Submission

Depends on completion of the required first-pre-defense artifacts and reviewed `main` baseline.

It includes:

- final repository inspection;
- README and submission documentation;
- known limitations;
- outstanding work;
- creation of the `pre-defense-1` Git tag.

## 7. External Dependencies

The project also depends on external development tooling and services, including:

- GitHub;
- YouTrack;
- Go toolchain during implementation;
- PostgreSQL during implementation and testing;
- browser environment for UX and compatibility testing;
- Mermaid tooling for editable architecture diagrams.

Availability of these tools is necessary for the corresponding project activity but does not change the functional scope of the platform.

## 8. Dependency Change Management

When a major upstream artifact changes, affected downstream artifacts should be reviewed.

Examples:

A requirement changes  
- review use cases, architecture, UX, implementation, and verification.

A technology decision changes  
- review component architecture and deployment assumptions.

A prototype changes scope  
- verify whether the requirements should also change.

A measured implementation limitation appears  
- review requirements, architecture, risks, and verification assumptions.

This prevents project documents from drifting into mutually inconsistent versions.