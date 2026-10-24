# Thematic Communities Platform

Thematic Communities Platform is a proposed web platform for interest-based online communities that combines persistent structured discussions with quick community communication.

**Current milestone:** Pre-Defense 1  
**Baseline date:** 24 October 2026  
**Current project stage:** research, requirements, architecture, UX prototype, verification planning, and project-management baseline.

> The current Pre-Defense 1 repository baseline does not claim a completed application implementation or working MVP.

## Problem

Online thematic communities often use different platforms for different interaction needs.

Fast-moving chat is useful for immediate communication but important information can become difficult to retrieve later. More persistent discussion platforms provide better structure but may not provide the same immediacy as chat-oriented systems.

Project-specific user research also identified recurring concerns involving:
- information becoming difficult to retrieve in chat;
- the need for both persistent and quick communication;
- organization of community information;
- use of multiple platforms for related community activity;
- moderation and governance.

The project investigates a community interaction model that combines persistent publication-oriented discussion with dedicated quick communication while maintaining clear community organization and governance.

## Target Users

The initial target users are people participating in interest-based online communities, including communities related to:
- hobbies;
- entertainment;
- technology;
- games;
- education;
- other shared interests.

The platform distinguishes between:
- Guests;
- Registered Users;
- Community Members;
- Moderators;
- Community Owners.

## Aim

The aim of the project is to design, implement, and evaluate a thematic-community platform that supports both persistent structured community content and quick communication within a clear community-centered interaction model.

## Main Objectives

The project aims to:
1. investigate problems experienced by users of existing community platforms;
2. review scientific literature relevant to online-community participation, information organization, communication, governance, and moderation;
3. compare existing community platforms;
4. evaluate alternative implementation technologies;
5. define verifiable functional and non-functional requirements;
6. design the system architecture and main user interactions;
7. develop and refine a visual UX prototype;
8. implement the approved core requirements;
9. verify the implementation using predefined functional and non-functional evaluation procedures;
10. evaluate the resulting system transparently against the approved requirements.

## Current Scope

### In Scope

The current approved baseline includes:
- user registration and authentication;
- thematic communities;
- community membership;
- community discovery;
- persistent publications;
- comments and replies;
- publication-author identification;
- community chat;
- community ownership and roles;
- moderation;
- user-controlled content deletion;
- consistent user identity;
- reliability, security, testability, maintainability, observability, and usability requirements.

### Out of Scope for the Initial Baseline

The following are not mandatory initial requirements:
- native mobile applications;
- voice or video communication;
- advanced recommendation algorithms;
- machine-learning moderation;
- payment functionality;
- advertising systems;
- synchronization with external social platforms;
- mandatory microservice architecture;
- mandatory distributed caching;
- mandatory message-broker infrastructure.

## Proposed Technical Baseline

The technology comparison selected the following proposed baseline:

| Area | Proposed Approach |
|---|---|
| Backend | Go |
| Primary database | PostgreSQL |
| Browser-facing API | REST-style HTTP/JSON |
| Real-time communication | WebSocket |
| Application architecture | Modular monolith |

These are planned implementation decisions.

## Architecture

The architecture is documented at three complementary levels.

### System Context

Shows the system boundary and primary external actors.
- [System Context — Mermaid source](docs/architecture/system-context.mmd)
- [System Context — SVG](docs/architecture/system-context.svg)

### Use Cases

Shows the primary user goals and role relationships.
- [Use Case Diagram — Mermaid source](docs/architecture/use-case.mmd)
- [Use Case Diagram — SVG](docs/architecture/use-case.svg)

### Component Architecture

Defines the proposed modular-monolith structure, communication interfaces, application responsibilities, persistence boundary, and PostgreSQL data store.
- [Component Diagram — Mermaid source](docs/architecture/component-diagram.mmd)
- [Component Diagram — SVG](docs/architecture/component-diagram.svg)
- [Architecture Description](docs/architecture/architecture.md)

## UX Prototype

The project includes a visual UX prototype covering key scenarios such as:
- registration;
- community discovery;
- community creation;
- community membership;
- publication creation;
- persistent discussions;
- comments and replies;
- publication-author identification;
- community chat.

Prototype documentation:
- [UX Prototype](docs/ux/prototype.md)
- [User Flow — Mermaid source](docs/ux/user-flow.mmd)
- [User Flow — SVG](docs/ux/user-flow.svg)

## Research

### Potential-User Research

The project collected:
- 12 survey responses;
- 4 short semi-structured user discussions.

Artifacts:
- [Survey Design](docs/research/survey-design.md)
- [Survey Results](docs/research/survey-results.md)
- [User Discussions](docs/research/user-discussions.md)
- [User Research Analysis](docs/research/user-research-analysis.md)

### Literature Review

The project includes a critical literature review and structured publication analysis concerning online communities, participation, information organization, communication, moderation, governance, and related topics.

- [Literature Review](docs/research/literature-review.md)
- [Literature Analysis](docs/research/literature-analysis.md)

### Existing Systems

The project compares:
- Reddit;
- Discord;
- Telegram;
- Tumblr.

- [Existing Systems Comparison](docs/comparisons/existing-systems.md)

### Technology Alternatives

The project compares alternatives for:
- backend technology;
- primary database;
- API style;
- real-time communication;
- application architecture.

- [Technology Alternatives Comparison](docs/comparisons/technology-comparison.md)

## Requirements

The approved initial requirements baseline contains:
- 16 functional requirements;
- 12 non-functional requirements;
- 5 technical design constraints.

- [Requirements Specification](docs/requirements/requirements-specification.md)

## Verification and Evaluation

A verification and evaluation plan has been defined before implementation results are reported.

It covers:
- functional verification;
- authentication and authorization;
- data integrity;
- performance;
- community chat;
- reliability;
- usability;
- browser compatibility;
- configuration security;
- observability;
- maintainability;
- automated testing and CI.

- [Verification and Evaluation Plan](docs/verification/verification-plan.md)

## Project Management

The project uses GitHub and YouTrack for traceable development.

The normal workflow is:

`YouTrack issue → task branch → meaningful commits → Pull Request → review → merge → acceptance check → Done`

Project-management artifacts:
- [Project Plan](docs/management/project-plan.md)
- [Risk Register](docs/management/risks.md)
- [Project Dependencies](docs/management/dependencies.md)

## Repository Structure

```text
docs/
├── architecture/
├── comparisons/
├── management/
├── proposal/
├── research/
├── requirements/
├── ux/
└── verification/
```

## Student and Responsibilities

**Student:** Yerassyl Ibrayev  
**Group:** SE-2425

Primary responsibilities:
- research;
- requirements engineering;
- technology evaluation;
- architecture;
- UX prototype;
- implementation;
- verification;
- documentation;
- project management.

**Project Supervisor:** Yespenbetova Dana

## Current Status

### Completed for Pre-Defense 1

- project repository initialization;
- project proposal and scope;
- potential-user research;
- user-research analysis;
- critical literature review;
- structured literature analysis;
- existing-system comparison;
- technology comparison;
- functional and non-functional requirements;
- system context diagram;
- use case diagram;
- component architecture;
- architecture documentation;
- visual UX prototype;
- verification and evaluation plan;
- project risks, milestones, dependencies, and workflow.

### Planned After Pre-Defense 1

- core application implementation;
- automated tests;
- database implementation;
- real-time chat implementation;
- CI/CD;
- operational instrumentation;
- execution of the verification plan;
- usability evaluation;
- performance testing;
- reliability evaluation;
- deployment and later SRE refinement.

## Running and Testing

Application run and test instructions are not provided at the current milestone because the Pre-Defense 1 baseline does not claim a completed application implementation.

## Pre-Defense 1

The exact reviewed first-pre-defense baseline is marked using the Git tag:
`pre-defense-1`

Submission details and known limitations are documented in:
- [Pre-Defense 1 Submission](docs/pre-defense-1.md)

## Project Links

- GitHub Repository: https://github.com/Yeras1kAITU/thematic-communities-platform
- YouTrack: https://thematic-communities.youtrack.cloud/projects/DIP

## License

No project license has been selected at the current Pre-Defense 1 stage.