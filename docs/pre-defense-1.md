# Pre-Defense 1 Submission

## 1. Submission Information

**Project:** Thematic Communities Platform  
**Student:** Yerassyl Ibrayev  
**Group:** SE-2425  
**Submission milestone:** Pre-Defense 1  
**Baseline date:** 24 October 2026  
**Repository:** https://github.com/Yeras1kAITU/thematic-communities-platform  
**Git tag:** `pre-defense-1`

## 2. Purpose of This Baseline

The Pre-Defense 1 baseline presents the research, requirements, design, prototype, verification-planning, and project-management foundation of the diploma project.

The baseline intentionally distinguishes between:
- completed research and design artifacts;
- proposed implementation decisions;
- future implementation work;
- planned verification activities;
- actually executed evidence.

## 3. Completed Work

### Project Definition

Completed:
- project proposal;
- problem definition;
- target users;
- aim and objectives;
- scope boundaries;
- expected outcomes.

### User Evidence

Completed:
- potential-user survey;
- 12 survey responses;
- 4 short semi-structured discussions;
- anonymized research evidence;
- user-research analysis;
- supported findings, contradictions, and assumptions.

### Literature Review

Completed:
- critical scientific literature review;
- structured publication analysis;
- comparison of findings and limitations;
- relationship between scientific evidence and project-specific research.

### Existing Systems

Completed comparison of:
- Reddit;
- Discord;
- Telegram;
- Tumblr.

The comparison identifies strengths, limitations, established functionality, and implications for the proposed system without claiming that the proposed platform is universally superior.

### Technology Alternatives

Completed comparison of alternatives for:
- backend technology;
- primary database;
- client-server API style;
- real-time communication;
- application architecture.

The proposed technical baseline is:
- Go;
- PostgreSQL;
- REST-style HTTP/JSON;
- WebSocket;
- modular monolith.

### Requirements

Completed initial requirements baseline containing:
- 16 functional requirements;
- 12 non-functional requirements;
- priorities;
- acceptance criteria;
- verification methods;
- traceability;
- dependencies;
- scope exclusions.

### Architecture

Completed:
- system context diagram;
- use case diagram;
- proposed component architecture;
- supporting architecture documentation.

Editable Mermaid sources and rendered SVG exports are retained in the repository.

### UX Prototype

Completed visual prototype coverage for:
- registration;
- community discovery;
- community creation;
- community membership;
- publication creation;
- persistent discussion;
- comments and replies;
- publication-author identification;
- community chat.

A visual user-flow diagram is also included.

### Verification Planning

Completed verification and evaluation plan covering:
- functional testing;
- authentication and authorization;
- data integrity;
- performance;
- real-time communication;
- reliability;
- usability;
- browser compatibility;
- configuration security;
- observability;
- maintainability;
- automated testing and CI.

Implementation-dependent verification has not yet been reported as completed.

### Project Management

Completed:
- milestone plan;
- Git/YouTrack workflow;
- Definition of Done;
- risk register;
- project dependencies;
- traceability model;
- scope-management rules.

## 4. Repository Traceability

The project uses the following workflow:

`YouTrack issue → task branch → meaningful commits → Pull Request → review → merge into main → acceptance check → Done`

Meaningful Git activity references the corresponding `DIP-*` task identifier.

The `main` branch represents the reviewed baseline.

## 5. Current Implementation Status

The Pre-Defense 1 baseline focuses on:
- research;
- requirements;
- architecture;
- UX;
- verification planning;
- project management.

A complete application implementation is not claimed in this submission.

## 6. Verification Status

The project has defined how implementation will later be verified.

At this milestone:
- the verification plan exists;
- acceptance conditions are defined;
- performance measurement conditions are defined;
- usability evaluation procedures are defined;
- implementation-dependent results are not yet claimed.

## 7. Known Limitations

Current limitations include:
- core application implementation is not yet part of the reviewed baseline;
- performance measurements have not yet been executed;
- usability evaluation has not yet been executed;
- production deployment has not yet been evaluated;
- final responsive/mobile UX is not finalized;
- moderator and detailed role-management interfaces are not yet fully represented in the visual prototype;
- final SRE and deployment tooling has not yet been selected or implemented;
- scalability beyond the later defined diploma evaluation environment has not been demonstrated.

These limitations are intentional and documented rather than hidden.

## 8. Outstanding Work

Post-Pre-Defense 1 work includes:
1. implement the approved core functional requirements;
2. implement PostgreSQL persistence;
3. implement authentication and authorization;
4. implement community membership and roles;
5. implement persistent publications, comments, and replies;
6. implement community chat using the selected real-time approach;
7. implement moderation behavior;
8. add automated testing;
9. introduce CI/CD;
10. introduce health, logging, metrics, and other justified operational capabilities;
11. execute the verification and evaluation plan;
12. perform usability evaluation;
13. perform performance and reliability evaluation;
14. document measured results;
15. refine the system based on implementation evidence and supervisor feedback.

## 9. Submission Baseline

The final reviewed commit for this milestone is marked by the annotated Git tag:

`pre-defense-1`

The tag should be created only after:
- all required Pre-Defense 1 changes are merged into `main`;
- the working tree is clean;
- the final repository state has been inspected.

The tag should not later be moved to a different commit.

## 10. Baseline Statement

This submission represents the first reviewed project baseline.

It demonstrates that the project problem, evidence, requirements, technology decisions, architecture, UX direction, evaluation approach, and project-management process have been established before full implementation proceeds.

Future project claims will be evaluated against this baseline and updated when evidence or approved requirements change.