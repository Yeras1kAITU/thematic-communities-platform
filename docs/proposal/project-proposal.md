# Project Proposal

## 1. Project Title

**Thematic Communities Platform: Design and Development of a Web Platform for Interest-Based Online Communities**

## 2. Team Members

**Student:** Yerassyl Ibrayev
**Program:** Software Engineering  
**Supervisor:** Altynbek Dana

## 3. Project Overview

The Thematic Communities Platform is a web application designed to support the creation and management of online communities centered around shared interests. The platform combines structured community publications, threaded discussions, community membership, moderation, and community-based chat within a single system.

Users can register using a unique nickname, discover and join communities, create their own communities, publish posts, comment on publications, reply to other comments, and communicate with other members through a dedicated community chat.

Community creators receive ownership privileges and can manage community content. The system also supports moderation roles to provide communities with mechanisms for managing discussions and maintaining appropriate interaction.

The project focuses not only on implementation but also on investigating how structured asynchronous communication, such as posts and comments, can coexist with faster community chat within one platform.

## 4. Problem Statement

Online interest-based communities commonly rely on social networks, forums, and messaging applications for communication. These platforms support different interaction models. Forum-oriented systems emphasize persistent and structured discussions, while messaging systems emphasize rapid communication. Social platforms may additionally provide feeds, groups, and content discovery.

As a result, organizers and members of interest-based communities may use multiple communication mechanisms to support different activities such as announcements, structured discussions, casual communication, and moderation.

The project investigates whether these interaction patterns can be supported within a unified community-oriented web application while maintaining clear separation between persistent publication-based discussions and real-time or near-real-time community communication.

At the proposal stage, this problem statement represents a working hypothesis. Interviews with potential users, analysis of existing systems, and a literature review will be used to determine which parts of the problem are supported by evidence and which assumptions need to be revised.

## 5. Target Users

The primary target users are people who participate in online communities based on shared interests.

The initial target group includes:

- university students participating in student communities and clubs;
- members of hobby and interest-based communities;
- community organizers;
- community moderators;
- users who want to create and manage their own online communities.

The project particularly considers small and medium-sized communities in which members need both structured content publication and less formal communication.

## 6. Project Aim

The aim of the project is to design, implement, and evaluate a web platform that supports structured interaction within thematic online communities by integrating community management, publications, threaded discussions, community communication, and role-based moderation.

## 7. Project Objectives

The project has the following objectives:

1. Identify the communication and community-management needs of potential users through interviews and analysis of relevant user processes.

2. Conduct a critical review of scientific and professional literature related to online communities, user participation, social presence, moderation, community governance, and online discussions.

3. Analyze existing community-oriented platforms using a consistent set of comparison criteria.

4. Compare reasonable technology alternatives and select technologies based on the functional and non-functional requirements of the project.

5. Define a structured set of functional and non-functional requirements with priorities and measurable acceptance criteria.

6. Design an architecture that separates user interface, application logic, domain logic, and data persistence responsibilities.

7. Develop a working web application prototype supporting the principal community interaction scenarios.

8. Implement mechanisms for community membership, content creation, discussions, community communication, and moderation.

9. Define and execute a verification and evaluation strategy for determining whether the implemented solution satisfies its requirements.

10. Maintain traceability between requirements, project-management tasks, implementation changes, tests, and evaluation results.

## 8. Expected Outcomes

The expected project outcomes are:

- a documented analysis of potential users and their needs;
- a structured literature review;
- a comparison of existing community platforms;
- justified technology decisions;
- a functional and non-functional requirements specification;
- system architecture documentation and diagrams;
- a working web application prototype;
- community creation and membership functionality;
- structured community publications;
- comments and replies;
- dedicated community chat;
- community ownership and moderation mechanisms;
- automated tests for critical application functionality;
- a verification and evaluation plan;
- project-management documentation and development history.

## 9. Project Scope

### 9.1 In Scope

The planned system includes:

- user registration;
- user authentication;
- unique user nicknames;
- community discovery;
- community creation;
- joining communities;
- community membership management;
- community ownership;
- moderator roles;
- creation of community posts;
- community publication feeds;
- comments on posts;
- replies to comments;
- identification of the post author in discussions;
- dedicated community chat;
- content deletion where authorized;
- moderation of community content;
- persistent storage of application data;
- web-based user interface;
- backend HTTP API;
- automated testing of critical functionality.

### 9.2 Out of Scope

The following functionality is outside the initial project scope:

- native Android or iOS applications;
- voice calls;
- video calls;
- live video streaming;
- advertising systems;
- monetization;
- marketplace functionality;
- complex recommendation algorithms;
- machine-learning-based content moderation;
- end-to-end encrypted private messaging;
- large-scale distributed deployment across multiple geographical regions.

These limitations are intended to keep the project achievable within the available diploma-project timeframe while preserving sufficient software-engineering complexity.

## 10. Key User Roles

### Guest

A guest is an unauthenticated visitor. A guest can access publicly available parts of the application and create an account.

### Member

A member is an authenticated user who can join communities and participate in community activities according to the permissions provided by the system.

### Community Owner

The user who creates a community becomes its owner. The owner has additional community-management and moderation permissions.

### Community Moderator

A moderator assists with managing discussions and community content according to the permissions assigned by the system.

## 11. Preliminary Technology Stack

The current prototype uses the following technologies:

- **Go** — backend application development;
- **HTTP/REST-style API** — communication between the web client and backend;
- **PostgreSQL** — persistent relational data storage;
- **HTML, CSS and JavaScript** — web user interface;
- **Git** — version control;
- **GitHub/GitLab** — source-code repository and review workflow;
- **YouTrack** — project and task management;
- **PlantUML** — editable architecture and UML diagrams.

The final technology decisions will be justified through a separate technology comparison rather than solely by the technologies already used in the prototype.

## 12. Engineering Complexity

The project involves multiple software-engineering concerns rather than only implementing a collection of web pages.

These include:

- authentication and authorization;
- role-based access control;
- relational data modelling;
- community ownership and membership;
- hierarchical discussion structures;
- content moderation;
- community communication;
- separation of application layers;
- API design;
- persistence abstraction;
- frontend/backend interaction;
- testing;
- security considerations;
- maintainability;
- deployment and configuration.

The project therefore provides sufficient scope for applying software-engineering practices involving requirements engineering, architecture, implementation, verification, and evaluation.

## 13. Current Project Status

The project is currently in the initial research, requirements engineering, and system design stage.

The project repository has been initialized, while the application implementation has not yet been introduced into the main project repository.

The current work focuses on validating the problem, defining the project scope, investigating related research and existing systems, specifying requirements, and designing the proposed system architecture.

## 14. Success Criteria

The project will be considered successful if:

1. mandatory functional requirements are implemented and pass their acceptance tests;
2. critical authorization rules prevent unauthorized operations;
3. users can complete the principal community interaction scenarios;
4. the system provides both persistent publication-based discussions and community chat;
5. application architecture and technical decisions are documented and traceable to project requirements;
6. evaluation results provide measurable evidence about whether the project aim has been achieved.