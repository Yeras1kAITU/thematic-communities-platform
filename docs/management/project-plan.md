# Project Plan

## 1. Purpose

This document defines the project-management baseline for the Thematic Communities Platform.

The project is developed as an individual diploma project and uses:
- GitHub for source control and pull-request review;
- YouTrack for work-item tracking;
- documented requirements and architecture as the project baseline;
- supervisor review for significant academic deliverables.

The plan is intended to maintain traceability between research, requirements, design, implementation, verification, and final project delivery.

## 2. Roles and Responsibilities

### Student

The student is responsible for:
- project research;
- requirements analysis;
- architecture and UX design;
- implementation;
- testing and verification;
- documentation;
- Git history;
- YouTrack task maintenance;
- preparation of pre-defense and final-defense deliverables;
- addressing supervisor feedback.

### Project Supervisor

The supervisor is responsible for academic guidance and review.

Supervisor involvement may include:
- reviewing key deliverables;
- identifying required corrections;
- approving appropriate pull requests;
- providing academic and technical feedback;
- helping ensure that project scope remains suitable for the diploma.

## 3. Major Milestones

| Milestone | Main Outcome | Status |
|---|---|---|
| Project Initialization | Repository, proposal, initial scope | Completed |
| Research Baseline | Potential-user research and analysis | Completed |
| Literature and Existing-System Analysis | Literature review and platform comparison | Completed |
| Technology Baseline | Technology and architecture decisions | Completed |
| Requirements Baseline | Functional and non-functional requirements | Completed |
| Architecture Baseline | Context, use-case, and component architecture | Completed |
| UX Prototype | Visual prototype and user flow | Completed |
| Verification Plan | Planned verification and evaluation procedures | Completed |
| Project Management Baseline | Risks, milestones, dependencies, workflow | In progress |
| Pre-Defense 1 | First documented project baseline | Planned for 24 October 2026 |
| Implementation Baseline | Core functional system implementation | Planned after Pre-Defense 1 |
| Verification Execution | Functional and non-functional evaluation | Planned |
| Pre-Defense 2 | Updated implementation and evidence baseline | Planned; date to be confirmed |
| Final Project Baseline | Final implementation, verification, documentation, and defense materials | Planned; date to be confirmed |

## 4. Development Workflow

Meaningful project work follows the workflow:

YouTrack issue  
→ task branch  
→ meaningful commits  
→ GitHub Pull Request  
→ review  
→ merge into `main`  
→ acceptance-criteria check  
→ YouTrack issue marked `Done`.

The `main` branch represents the reviewed project baseline.

## 5. Naming Conventions

### Branches

Format:

`DIP-<number>-<short-description>`

Examples:
- `DIP-8-requirements`
- `DIP-11-component-architecture`
- `DIP-14-project-management`

### Commits

Format: `DIP-<number>: <meaningful change>`

Example: `DIP-14: Add project risk register`

Commits should describe a meaningful unit of work rather than generic messages such as:
- `update`;
- `changes`;
- `fix stuff`.

### Pull Requests

Format: `DIP-<number>: <deliverable description>`

Each pull request should include:
- YouTrack task reference;
- summary of changes;
- affected files;
- verification performed;
- relevant next step.

## 6. YouTrack Usage

A meaningful project task should contain:
- clear objective;
- expected outcome;
- acceptance criteria;
- assignee;
- state;
- appropriate priority;
- links to related Git activity where available.

A task should not be marked `Done` only because a file was created.

The acceptance criteria should first be checked against the completed work.

## 7. Review Process

Key academic deliverables should be submitted through GitHub pull requests.

Where supervisor review is requested:
1. the pull request is created;
2. the supervisor is assigned as reviewer;
3. requested changes are addressed through additional commits;
4. approval is obtained;
5. the pull request is merged.

Review comments and resulting project changes may later be referenced as evidence for supervisor-feedback requirements.

## 8. Definition of Done

A project task is considered complete when all applicable conditions are satisfied:
- the expected deliverable exists;
- acceptance criteria are satisfied;
- relevant documentation is updated;
- editable source artifacts are included where required;
- generated exports are included where required;
- changes are committed using the task ID;
- changes are pushed to the task branch;
- a pull request exists;
- required review has been completed;
- the pull request has been merged into `main`;
- the task has been verified against its acceptance criteria;
- the YouTrack issue is updated to `Done`.

For implementation tasks, Definition of Done additionally includes:
- relevant automated tests;
- no known critical regression in affected functionality;
- configuration and secrets handled safely;
- documentation updated where behavior changed.

## 9. Baseline Tags

Important academic baselines should be marked using Git tags.

Planned tags include:
- `pre-defense-1`;
- `pre-defense-2`;
- `final-pre-defense`.

A baseline tag should point to the exact reviewed commit submitted for the corresponding milestone.

## 10. Traceability

The project uses the following traceability chain:

Research evidence  
→ requirements  
→ architecture / UX  
→ implementation  
→ verification  
→ evaluation results.

Project-management traceability follows:

YouTrack task  
→ branch  
→ commits  
→ pull request  
→ review  
→ merged baseline.

This structure allows a reviewer to trace both why a feature exists and how its implementation entered the project.

## 11. Scope Management

New functionality should not automatically become project scope simply because it appears in:
- a prototype;
- an experimental branch;
- a reference implementation;
- a technical idea.

A significant scope addition should first be checked against:
- project objectives;
- requirements;
- available development time;
- architecture;
- verification cost.

## 12. Current Project Stage

At the first pre-defense stage, the primary deliverables are research, requirements, architecture, prototype, verification planning, and project-management evidence.
