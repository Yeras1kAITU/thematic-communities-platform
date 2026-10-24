# Project Risk Register

## 1. Purpose

This document identifies major risks that could affect the quality, schedule, scope, or technical reliability of the Thematic Communities Platform.

Risk levels use the following qualitative scale:
- Low;
- Medium;
- High.

## 2. Risk Register

| ID | Risk | Likelihood | Impact | Mitigation / Response |
|---|---|---:|---:|---|
| R1 | Scope grows beyond what can be implemented and verified within the diploma schedule | High | High | Keep Must requirements as the baseline; treat additional prototype ideas as optional until formally approved |
| R2 | Excessive architecture complexity delays implementation | Medium | High | Retain the modular-monolith baseline; introduce additional infrastructure only when justified by a verified requirement |
| R3 | Requirements change after implementation begins | Medium | Medium | Maintain traceability and requirement change management; evaluate effects on architecture, implementation, and verification before accepting major changes |
| R4 | Real-time community chat is more complex than expected | Medium | High | Implement chat incrementally; test authentication, connection lifecycle, persistence, and failure handling separately |
| R5 | Authorization defects allow users to perform operations outside their role | Medium | High | Centralize permission checks where practical and include negative authorization tests for Member, Moderator, and Owner roles |
| R6 | Persistent data becomes inconsistent because of incorrect application or database behavior | Medium | High | Use relational constraints, transactions where required, integration tests, and controlled migrations |
| R7 | Application performance does not meet the planned NFR target | Medium | Medium | Establish a reproducible performance baseline, profile bottlenecks, review queries and indexes, and optimize based on measurements |
| R8 | UX design is difficult for users despite technically correct functionality | Medium | Medium | Execute planned usability evaluation and revise screens based on observed user difficulties |
| R9 | Security-sensitive configuration or credentials are accidentally committed | Low–Medium | High | Use `.gitignore`, placeholder configuration, environment variables, repository inspection, and later secret scanning where practical |
| R10 | Limited project time prevents implementation of all Should requirements | Medium | Medium | Prioritize Must requirements first and document incomplete Should requirements transparently |
| R11 | Supervisor feedback requires late rework | Medium | Medium | Request review at meaningful intermediate milestones instead of waiting until final delivery |
| R12 | Single-developer workload creates a project bottleneck | High | Medium | Keep tasks small, maintain clear priorities, avoid unnecessary parallel scope, and preserve reproducible documentation |
| R13 | SRE or infrastructure work becomes larger than the application itself | Medium | Medium | Add monitoring, CI/CD, deployment automation, and reliability mechanisms incrementally; avoid infrastructure without a concrete operational purpose |
| R14 | Prototype functionality silently expands approved scope | Medium | Medium | Mark exploratory UI features explicitly and add new mandatory functionality only through requirement change management |
| R15 | Verification evidence cannot be reproduced | Low–Medium | High | Record tested Git revision, environment, dataset, procedure, and retained test output for important evaluations |

## 3. Priority Risks

The most important current risks are:

### R1 - Scope Growth

The platform can easily expand into:
- recommendation systems;
- complex social-network functionality;
- advanced moderation;
- extensive infrastructure;
- multiple communication modes.

The primary mitigation is strict prioritization of the approved requirements.

### R4 - Real-Time Communication Complexity

WebSocket-based communication introduces:
- connection lifecycle;
- authentication;
- concurrent clients;
- disconnection;
- persistence;
- resource management.

The chat should therefore be developed and verified incrementally rather than treated as a single final-stage feature.

### R5 - Authorization Errors

Community roles create security-sensitive behavior.

A visually hidden button is not sufficient authorization.

Protected operations must be checked on the backend and tested using unauthorized scenarios.

### R12 - Single-Developer Bottleneck

Because the project is developed primarily by one student, implementation, research, documentation, testing, and deployment compete for the same development time.

The response is to:
- prioritize Must requirements;
- avoid unnecessary architectural complexity;
- keep YouTrack tasks small and traceable;
- maintain a reviewed baseline throughout development.

## 4. Risk Review

The risk register should be reviewed when:
- requirements materially change;
- a major implementation milestone is completed;
- performance or usability testing identifies significant issues;
- supervisor feedback affects project scope;
- a new infrastructure dependency is proposed.
