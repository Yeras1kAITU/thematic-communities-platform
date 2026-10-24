# Verification and Evaluation Plan

## 1. Purpose

This document defines the planned verification and evaluation approach for the Thematic Communities Platform.

The purpose is to establish, before implementation is evaluated, how the project will determine whether the approved requirements and intended user experience have been satisfied.

The plan is derived from:
- the approved requirements specification;
- the system context diagram;
- the use case diagram;
- the proposed component architecture;
- the visual UX prototype.

This document defines planned procedures and acceptance conditions.

## 2. Verification Objectives

The verification process should answer the following questions:
1. Do the required user-facing functions behave as specified?
2. Are authentication and authorization restrictions enforced correctly?
3. Is persistent data stored consistently?
4. Does the system provide acceptable response times under the defined diploma evaluation load?
5. Does community chat provide sufficiently responsive communication?
6. Does the application handle invalid input and expected failures without uncontrolled termination?
7. Can representative users complete the main interaction scenarios?
8. Does the interface operate correctly in the selected supported browsers?
9. Are application secrets and configuration handled safely?
10. Does the system expose sufficient operational information for basic service monitoring?

## 3. Verification Levels

The project will use several complementary verification levels.

### 3.1 Unit Verification

Unit tests should verify isolated business behavior where practical.

Examples include:
- validation rules;
- role and permission decisions;
- domain-level state transitions;
- content-ownership rules.

### 3.2 Integration Verification

Integration tests should verify interaction between application modules and infrastructure boundaries.

Examples include:
- persistence operations;
- PostgreSQL constraints;
- authentication flows;
- community membership;
- publication creation;
- comments and replies.

### 3.3 API Verification

API-level tests should verify request/response behavior without depending on manual browser interaction.

These tests should cover:
- successful requests;
- validation failures;
- authentication failures;
- authorization failures;
- nonexistent resources;
- conflicting input.

### 3.4 End-to-End Verification

Selected core scenarios should be verified through the complete application path.

Examples include:
- account creation;
- joining a community;
- publishing content;
- participating in a discussion;
- sending a chat message.

### 3.5 Inspection

Some requirements are better verified through repository or architecture inspection rather than runtime testing.

Examples include:
- secret handling;
- modular structure;
- configuration;
- existence of automated tests;
- observability interfaces.

### 3.6 Evaluation

Usability and performance requirements require measured evaluation rather than only pass/fail functional testing.

---

# 4. Functional Requirements Verification

## FR-01 - User Registration

**Method:** API test + end-to-end scenario.

### Verify
- valid account creation;
- duplicate nickname rejection;
- required-field validation;
- invalid-input handling;
- single account creation per successful request.

### Evidence
- automated test output;
- API response evidence;
- persistent-state verification.

---

## FR-02 - User Authentication

**Method:** API and authorization tests.

### Verify
- valid credentials authenticate;
- invalid credentials fail;
- protected requests reject unauthenticated users;
- authenticated identity corresponds to the correct user.

### Evidence
- automated test output;
- HTTP responses;
- authorization test cases.

---

## FR-03 - Community Creation

**Method:** API + persistence integration test.

### Verify
- authenticated user can create a community;
- creator becomes initial owner;
- required information is persisted;
- invalid or conflicting identifiers are rejected;
- unauthenticated creation is rejected.

---

## FR-04 - Community Membership

**Method:** Integration and authorization tests.

### Verify
- user can join a community;
- duplicate membership is prevented;
- membership is persisted;
- user can leave where ownership constraints allow;
- access checks correctly distinguish members and non-members.

---

## FR-05 - Community Discovery

**Method:** API test + UI scenario.

### Verify
- discoverable communities are returned;
- search can locate matching communities;
- no-result state is handled;
- selected community can be opened.

---

## FR-06 - Publication Creation

**Method:** API + persistence test.

### Verify
- authorized member can create a publication;
- publication is associated with the correct author;
- publication is associated with the correct community;
- invalid content is rejected;
- unauthorized creation is rejected.

---

## FR-07 - Community Publication Feed

**Method:** Integration test + UI scenario.

### Verify
- community feed returns relevant publications;
- publications from unrelated communities are excluded;
- authorship is displayed;
- newly created publications become available.

---

## FR-08 - Comments

**Method:** API + persistence test.

### Verify
- member can comment;
- comment references correct publication;
- comment references correct author;
- comments persist;
- unauthorized comment creation is rejected.

---

## FR-09 - Replies

**Method:** API + persistence test.

### Verify
- reply can be created for an existing comment;
- parent relationship is preserved;
- invalid parent references are rejected;
- reply author is preserved;
- replies are retrievable with discussion content.

---

## FR-10 - Publication Author Identification

**Method:** service/UI verification.

### Verify
- system can identify the original publication author;
- author indicator is displayed when appropriate;
- unrelated users do not receive the indicator.

---

## FR-11 - Community Chat

**Method:** integration + real-time end-to-end test.

### Verify
- authorized member can send a message;
- another active client receives the message;
- message is associated with the correct user;
- message is associated with the correct community;
- message is persisted;
- unauthorized users cannot send messages.

---

## FR-12 - Dedicated Community Chat Interface

**Method:** UX inspection + UI scenario.

### Verify
- community chat is clearly accessible;
- chat is visually distinguishable from publications;
- users can return between community content and chat.

---

## FR-13 - Community Ownership and Roles

**Method:** authorization tests.

### Verify
- community has one initial owner;
- owner privileges are recognized;
- moderator privileges differ from normal membership;
- ordinary members cannot perform protected management operations.

---

## FR-14 - Content Moderation

**Method:** authorization + API tests.

### Verify
- authorized Moderator or Owner can perform permitted moderation;
- ordinary member cannot perform moderator-only actions;
- backend validates moderation permission;
- insufficient permissions receive a controlled rejection.

---

## FR-15 - User Content Deletion

**Method:** API + authorization + persistence test.

### Verify
- user can delete supported own content;
- user cannot delete another user's content without permission;
- moderated deletion respects authorization;
- deletion does not leave invalid relationships.

---

## FR-16 - Consistent User Identity

**Method:** integration + UI inspection.

### Verify
the same user nickname is consistently associated with:
- publications;
- comments;
- replies;
- chat messages.

---

# 5. Non-Functional Requirements Verification

## NFR-01 - Authentication Security

**Method:** negative API/security testing.

### Verify
- protected routes reject unauthenticated requests;
- invalid authentication data is rejected;
- expired authentication data is rejected where applicable;
- sensitive authentication information is not exposed in responses.

---

## NFR-02 - Password Protection

**Method:** implementation and persistence inspection.

### Verify
- plaintext passwords are not stored;
- plaintext passwords are not written to logs;
- password verification uses the protected stored representation.

No production or real user credentials should be used during verification.

---

## NFR-03 - Authorization and Access Control

**Method:** permission matrix testing.

Test combinations should include:
- Guest;
- Registered User;
- Community Member;
- Moderator;
- Community Owner.

Protected operations should be executed both with valid and invalid roles.

### Success Condition

No tested client-side request modification should bypass backend authorization rules.

---

## NFR-04 - Data Integrity

**Method:** database integration tests.

### Verify
- invalid references are prevented;
- prohibited duplicates are prevented;
- relevant multi-step operations remain consistent;
- failed operations do not knowingly leave invalid persistent state.

---

# 6. Performance Evaluation

## 6.1 Purpose

The performance evaluation will determine whether core operations satisfy the initial NFR-05 target under a documented reference workload.

The evaluation will not attempt to represent internet-scale production traffic.

## 6.2 API Performance Metric

Primary metric:

**95th percentile response latency (p95).**

Initial NFR target:

> p95 ≤ 1 second for selected normal core REST operations under the defined reference load.

Additional values to report:
- median latency;
- p95 latency;
- request count;
- successful request count;
- error count;
- throughput.

## 6.3 Operations to Measure

At minimum:
- authentication;
- community listing/search;
- opening community data;
- retrieving publication feed;
- creating a publication;
- retrieving a publication discussion;
- creating a comment.

Write operations should use isolated test data where necessary.

## 6.4 Reference Load

Initial diploma evaluation load:
- **20 concurrent virtual users**;
- **10-minute measured interval**;
- at least one warm-up period before measurement.

The test should be repeated at least **three times** where practical.

## 6.5 Reference Dataset

Before performance evaluation, the database should contain a repeatable seeded dataset.

The exact dataset generator may be implemented later.

The evaluation report must record at least:
- number of users;
- number of communities;
- number of memberships;
- number of publications;
- number of comments/replies;
- number of chat messages.

The dataset should not be silently changed between comparative runs.

## 6.6 Reference Environment

Before reporting performance results, the following must be recorded:
- tested Git commit/tag;
- operating system;
- CPU;
- available RAM;
- database version;
- application configuration relevant to performance;
- whether client, application, and database run on the same machine or separately.

Performance results without the corresponding environment description should not be treated as reproducible evidence.

## 6.7 Result Interpretation

A result should only be considered compliant with NFR-05 if:
- the specified workload was used;
- the environment was documented;
- the relevant operation remained within the defined p95 target;
- excessive functional errors did not occur during the measurement.

---

# 7. Community Chat Evaluation

## 7.1 Functional Verification

At minimum two authenticated clients should join the same community chat.

Verify:
1. Client A sends a message.
2. Client B receives it without manual page refresh.
3. Author identity is correct.
4. Community association is correct.
5. The message remains available after reconnection/reload where persistence is expected.

## 7.2 Delivery-Latency Metric

NFR-05 currently defines an initial target:

> chat message delivery should normally occur within 1 second under the defined baseline load.

The measurement procedure should record:
- send timestamp;
- receive timestamp;
- calculated delivery latency.

## 7.3 Load Context

Chat evaluation should record:
- number of active connections;
- number of communities involved;
- message rate;
- test duration.

---

# 8. Reliability and Failure Evaluation

## 8.1 Invalid Requests

Test:
- malformed JSON;
- missing required fields;
- invalid identifiers;
- invalid resource references;
- unauthorized actions.

Expected behavior:
- controlled error response;
- no uncontrolled process termination.

## 8.2 Database Unavailability

Where practical, temporarily make the database unavailable.

Observe:
- whether requests fail in a controlled manner;
- whether the application remains alive;
- whether readiness correctly reflects inability to serve normal requests;
- whether sensitive internal information is hidden from normal client responses.

## 8.3 Graceful Shutdown

Initiate normal application termination.

Verify:
- the application stops without uncontrolled failure;
- owned resources are released;
- new work is not accepted indefinitely during shutdown;
- persistent connections are handled in a controlled manner.

## 8.4 WebSocket Disconnection

Verify behavior when:
- client closes connection normally;
- connection disappears unexpectedly;
- client later reconnects.

The exact reconnection UX may be refined during implementation.

---

# 9. Usability Evaluation

## 9.1 Objective

Evaluate whether representative users can complete the main scenarios without procedural guidance.

The usability evaluation is intended to test the prototype/application experience, not participants' technical knowledge.

## 9.2 Participants

The evaluation should use several participants representative of the intended audience.

An initial target is:

**at least 5 participants**.

Participants do not need to be the same people who took part in the initial research.

## 9.3 Scenarios

At minimum:

### U1 - Registration

Create an account.

### U2 - Community Discovery

Find a community matching a given topic.

### U3 - Community Membership

Open and join the selected community.

### U4 - Persistent Discussion

Create a publication and locate it afterwards.

### U5 - Discussion Interaction

Open a publication and add a comment or reply.

### U6 - Quick Communication

Open community chat and send a message.

## 9.4 Completion Measurement

For each scenario record:

- completed successfully: yes/no;
- procedural assistance required: yes/no;
- major error encountered: yes/no;
- optional completion time;
- participant comments.

## 9.5 Acceptance Target

The initial NFR-07 target is:

> at least 80% of participants should complete each selected core scenario without direct procedural assistance.

With five participants, this means at least four participants must successfully complete a scenario without direct procedural assistance.

## 9.6 Moderator Behavior

The evaluator should:

- provide the task goal;
- avoid telling the participant exactly which button to press;
- intervene only when necessary;
- record interventions.

## 9.7 Post-Task Feedback

After the scenarios, participants may be asked short questions such as:
- What was difficult to find?
- Was the difference between Publications and Chat clear?
- Was anything unexpected?
- What would you change first?

---

# 10. Browser Compatibility Evaluation

## Target

Verify core scenarios in at least:
- a current Chromium-based browser;
- a current Firefox release.

## Scenarios

At minimum:
- registration/authentication;
- discovery;
- community page;
- publication interaction;
- community chat.

## Evidence

Record:
- browser name;
- browser version;
- scenario result;
- visible compatibility problems.

---

# 11. Configuration and Secret Security Verification

Repository inspection should verify:
- `.env` and equivalent local secret files are ignored;
- real passwords or tokens are not committed;
- example configuration uses placeholders;
- runtime configuration can be provided externally;
- logs do not contain known test passwords or authentication secrets.

If automated secret scanning is introduced later, its output may be retained as additional evidence.

---

# 12. Observability Verification

The planned implementation should expose enough operational information to understand basic service health.

## Verify

### Health

A mechanism exists to indicate that the application process is alive.

### Readiness

Where dependency availability matters, a readiness mechanism can indicate whether normal application traffic can be served.

### Logs

Application logs should provide structured operational information without exposing secrets.

### Metrics

Basic service metrics should be available.

Candidate useful metrics include:
- HTTP request count;
- request duration;
- error count;
- active WebSocket connections.

The final metric set may be refined during implementation.

---

# 13. Maintainability Verification

NFR-08 will primarily be evaluated through architecture and code review.

Verify that:
- major domain responsibilities remain identifiable;
- transport concerns are separated from business behavior;
- persistence concerns are separated from presentation concerns;
- module dependencies remain understandable;
- implementation remains consistent with the approved modular-monolith architecture unless an approved design change exists.

---

# 14. Testability and CI Verification

NFR-09 will be evaluated by repository inspection and execution of automated checks.

Verify:
- automated tests exist for critical functionality;
- tests have documented execution commands;
- tests can be executed repeatedly;
- authentication and authorization are included;
- CI executes the required project checks once CI is introduced.

---

# 15. Requirements Verification Matrix

| Requirement | Primary Verification |
|---|---|
| FR-01 | API + E2E |
| FR-02 | API + authorization |
| FR-03 | API + persistence |
| FR-04 | Integration + authorization |
| FR-05 | API + UI |
| FR-06 | API + persistence |
| FR-07 | Integration + UI |
| FR-08 | API + persistence |
| FR-09 | API + persistence |
| FR-10 | Service + UI |
| FR-11 | Real-time integration + E2E |
| FR-12 | UX/UI verification |
| FR-13 | Authorization |
| FR-14 | Authorization + API |
| FR-15 | Authorization + persistence |
| FR-16 | Integration + UI |
| NFR-01 | Security/API |
| NFR-02 | Inspection + authentication test |
| NFR-03 | Permission matrix |
| NFR-04 | Database/integration |
| NFR-05 | Performance measurement |
| NFR-06 | Failure/reliability scenarios |
| NFR-07 | Usability evaluation |
| NFR-08 | Architecture/code review |
| NFR-09 | Automated-test and CI inspection |
| NFR-10 | Repository/configuration inspection |
| NFR-11 | Operational inspection |
| NFR-12 | Cross-browser testing |

---

# 16. Entry Criteria

A verification activity should begin only when the relevant functionality exists.

For full implementation verification, expected entry criteria include:
- target Git commit or tag identified;
- application can be started in the test environment;
- required dependencies are available;
- test database can be initialized;
- test data can be created;
- required configuration is documented;
- critical known blockers are recorded.

---

# 17. Exit Criteria

The implementation can be considered verified against the initial baseline when:
- all Must functional requirements have corresponding executed verification;
- all Must NFRs have corresponding evidence;
- unresolved critical authorization or data-integrity failures are absent;
- performance evaluation has been executed and documented;
- usability evaluation has been executed and documented;
- failed requirements are explicitly reported rather than omitted;
- evidence is linked to the tested commit or tag.

---

# 18. Evidence Retention

Verification evidence should be stored or referenced in a reproducible form.

Possible evidence includes:
- automated test reports;
- CI run references;
- performance-test output;
- screenshots where visual verification is appropriate;
- usability-test tables;
- browser compatibility results;
- relevant application logs;
- monitoring screenshots or exports;
- tested Git commit/tag.

---

# 19. Defect Handling

When verification identifies a defect:
1. record the affected requirement;
2. record the observed behavior;
3. record the expected behavior;
4. fix the defect through the normal Git/YouTrack workflow;
5. repeat the relevant verification;
6. retain the final result.

---

# 20. Baseline Comparison

The first implementation measurement will establish the project's initial technical baseline.

Later optimizations may be compared against this baseline using the same or explicitly documented equivalent test conditions.

Examples include comparing:
- API latency before and after query optimization;
- chat behavior before and after connection-management improvements;
- database query behavior before and after indexing.

---

# 21. Evaluation Limitations

The diploma evaluation environment will not reproduce the scale or geographic distribution of a large commercial social platform.

Expected limitations include:
- relatively small test population;
- limited server infrastructure;
- limited concurrent-user load;
- local or single-region testing;
- short-duration performance tests;
- limited browser/device coverage.

The project should therefore avoid claims such as:
- internet-scale scalability;
- production-grade global availability;
- support for millions of concurrent users;

unless such properties are actually demonstrated.

---

# 22. Planned Evaluation Outputs

Later verification work should produce a result table similar to:

| Requirement | Method | Result | Evidence | Notes |
|---|---|---|---|---|
| FR-01 | API/E2E | Not yet executed | - | Planned |
| FR-02 | API | Not yet executed | - | Planned |
| ... | ... | ... | ... | ... |
| NFR-05 | Performance | Not yet executed | - | Planned |
| NFR-07 | Usability | Not yet executed | - | Planned |

At the current first-pre-defense stage, the expected state is **Not yet executed** where implementation-dependent verification has not occurred.

---

# 23. Summary

The verification and evaluation plan establishes how the Thematic Communities Platform will later be evaluated against its approved requirements.

The plan covers:
- functional verification;
- authentication and authorization;
- persistent data integrity;
- performance;
- real-time chat;
- reliability and failure handling;
- usability;
- browser compatibility;
- configuration security;
- observability;
- maintainability;
- automated testing and CI.

The plan also defines:
- reference performance conditions;
- usability success criteria;
- entry and exit criteria;
- evidence retention;
- defect handling;
- evaluation limitations.

No implementation-dependent results are claimed at the current stage.