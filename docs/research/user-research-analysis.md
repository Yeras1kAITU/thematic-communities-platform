# User Research Analysis

## 1. Purpose

This document analyzes the evidence collected during the potential-user research conducted for the Thematic Communities Platform project.

The analysis is based on two evidence sources:
- 12 anonymous structured survey responses;
- 4 anonymized semi-structured user discussions.

The purpose of the analysis is to identify recurring user problems and needs, evaluate the initial project assumptions, preserve contradictory evidence, and identify potential system requirements.

This document distinguishes between reported evidence, interpretation, and assumptions. Potential requirements identified here are research-informed candidates and are not automatically treated as final system requirements.

## 2. Evidence Sources

### 2.1 Survey

The structured survey collected 12 responses from potential users of online thematic communities.

The survey investigated:
- frequency of community usage;
- platforms used;
- community activities;
- satisfaction with existing platforms;
- information retrieval;
- experienced problems;
- use of multiple platforms;
- importance of persistent discussions;
- importance of quick communication;
- preferred platform functionality.

Detailed survey evidence is documented in:

`docs/research/survey-results.md`

### 2.2 User Discussions

Four short semi-structured discussions were conducted with users having experience with different types of online communities.

The discussions explored:
- problems experienced in online communities;
- persistent versus quick communication;
- use of multiple platforms;
- desired improvements.

Detailed qualitative evidence is documented in:

`docs/research/user-discussions.md`

## 3. Analysis Method

Evidence is analyzed using the following structure:

**Reported Finding** - a statement directly supported by collected evidence.

**Interpretation** - a project-level interpretation of what the evidence may mean.

**Assumption** - a hypothesis that is not sufficiently established by the available evidence.

**Potential Requirement** - functionality or a quality attribute that may be justified by the evidence but must still be evaluated during requirements specification.

Confidence is classified as:
- **High** - supported by multiple quantitative and qualitative evidence points;
- **Medium** - supported by recurring evidence, but with limited sample size or mixed evidence;
- **Low** - supported by individual observations or insufficient evidence.

Because the research uses convenience sampling and a small sample, confidence refers to consistency within the collected evidence rather than statistical generalizability.

## 4. Finding F1 - Information Persistence Is a Recurring Problem

### Reported Evidence

In the survey:
- 8 of 12 respondents reported that important information gets lost in chat messages;
- 5 of 12 reported difficulty finding old discussions;
- 6 of 12 reported that discussions become disorganized;
- the mean score for ease of finding useful or previously discussed information was 3.42 out of 5.

The qualitative discussions provide additional evidence.

P1 described useful tutorials and recommendation lists becoming buried under large volumes of Discord messages.

P2 described useful discussions becoming difficult to locate among repeated questions and unrelated communication.

P4 described Telegram as inconvenient for locating important older messages.

### Reported Finding

Loss of useful information and difficulty retrieving previous discussions are recurring problems within the collected evidence.

### Interpretation

Fast chat-based communication is useful for immediate interaction but may provide insufficient persistence and organization for information that users want to access later.

### Confidence

**High within the collected sample.**

The finding is supported by both survey responses and multiple independent user discussions.

### Potential Requirement

The proposed system should support persistent, structured content that remains accessible after the original discussion has ended.

Potential functionality may include:
- persistent publications;
- topic-based discussions;
- comments and replies;
- search or other information-retrieval mechanisms.

The exact implementation is not determined by this finding alone.

## 5. Finding F2 - Users Value Both Persistent and Quick Communication

### Reported Evidence

The survey produced the following mean importance scores:
- organized and persistent discussions: **4.42 / 5**;
- quick informal communication: **4.17 / 5**.

For organized and persistent discussions:
- 11 of 12 respondents selected a rating of 4 or 5.

For quick communication:
- 10 of 12 respondents selected a rating of 4 or 5.

The qualitative discussions also distinguish between these interaction modes.

P1 uses Discord or Telegram for quick communication but prefers Reddit or forums for substantial questions.

P2 uses persistent systems such as Stack Overflow, GitHub, and Reddit for substantial questions while using Telegram and Discord for quick communication.

P3 uses Telegram for quick communication and Reddit or forums for more persistent information.

P4 similarly uses Reddit for persistent information and Discord or Telegram for quick communication.

### Reported Finding

Both persistent discussions and quick informal communication are important to participants.

The two interaction modes are not treated by participants as interchangeable.

### Interpretation

A community platform supporting only persistent publications or only transient chat may not address the full range of interaction patterns observed in the research.

### Confidence

**High within the collected sample.**

The finding is supported consistently by both quantitative and qualitative evidence.

### Potential Requirement

The proposed system should consider supporting both:
- persistent publication-oriented interaction;
- quick community communication.

The relationship between these interaction modes should be evaluated during system and UX design.

## 6. Finding F3 - Multi-Platform Usage Is Common

### Reported Evidence

In the survey:
- 4 of 12 respondents reported frequently using multiple platforms for the same interest or community;
- 6 of 12 reported doing so sometimes;
- 2 of 12 reported not doing so.

Therefore, **10 of 12 respondents** reported multi-platform usage at least sometimes.

Reasons selected by respondents included:
- different platforms being better for organized discussions;
- different platforms being better for quick conversations;
- different members using different platforms;
- some content being available only on particular platforms;
- differences in moderation and management functionality.

All four qualitative participants described using multiple platforms for different purposes.

Examples included combinations of:
- Discord and Reddit;
- Telegram and Reddit;
- GitHub, Discord, and Telegram;
- Telegram, Instagram, and shared documents.

### Reported Finding

Using multiple platforms for the same interest or related community activities is common within the collected sample.

### Interpretation

Users may distribute community activities across multiple platforms because individual platforms provide different strengths.

This creates some degree of interaction and information fragmentation.

### Confidence

**High within the collected sample.**

The finding is supported by 10 of 12 survey respondents and all four qualitative discussions.

### Potential Requirement

The proposed system should evaluate whether commonly separated community activities can be supported within a more unified environment.

However, the evidence does not establish that users want every external platform function reproduced in a single application.

## 7. Finding F4 - Organization and Retrieval Are Important

### Reported Evidence

The survey identified several organization-related problems:
- 8 of 12 respondents reported important information becoming lost in chat;
- 6 of 12 reported discussions becoming disorganized;
- 5 of 12 reported difficulty finding old discussions.

Search was also repeatedly selected as an important platform feature.

In the qualitative discussions:
- P1 requested a way to make useful discussions persistent and searchable;
- P2 requested better search and topic organization;
- P3 described difficulty understanding where different types of community information are located;
- P4 requested better topic organization in Telegram.

### Reported Finding

Participants repeatedly identified organization and information retrieval as important aspects of community-platform usability.

### Interpretation

Providing communication functionality alone is insufficient if users cannot understand where information belongs or retrieve it later.

### Confidence

**High within the collected sample.**

### Potential Requirement

The system should provide clear organization of community content.

Potential mechanisms include:
- separate community spaces;
- structured publications;
- topic organization;
- consistent navigation;
- search functionality.

The final mechanisms will be determined during requirements and UX design.

## 8. Finding F5 - Moderation Influences Community Quality

### Reported Evidence

Four of twelve survey respondents reported insufficient or inconsistent moderation as a problem.

Moderation tools and user roles or permissions were also selected as important features by multiple respondents.

P2 specifically described community quality as dependent on moderation and contrasted well-organized communities with poorly managed ones.

Other participants reported problems involving spoilers, noise, repeated questions, and community organization that may also be influenced by moderation practices.

### Reported Finding

Moderation is relevant to community quality for a meaningful subset of participants, although it was not the most frequently reported problem.

### Interpretation

Community-management functionality may be necessary to maintain usable community spaces, particularly as participation grows.

### Confidence

**Medium.**

The finding is supported by multiple survey responses and qualitative evidence, but it is less universal than information-persistence and multi-platform findings.

### Potential Requirement

The system should provide basic community moderation and role-management capabilities.

Potential capabilities include:
- community ownership;
- moderator roles;
- removal of inappropriate content;
- management of community membership or permissions.

Detailed moderation functionality requires further specification.

## 9. Finding F6 - Community Discovery and Onboarding Affect Some Users

### Reported Evidence

Two survey respondents reported difficulty discovering relevant communities.

Community discovery was selected as an important feature by several respondents.

P1 described difficulty joining conversations when an existing group is already socially established.

P3 described uncertainty about community activity and hesitation when joining conversations in large groups.

P3 also suggested introductory information or dedicated spaces for new members.

### Reported Finding

Some participants experience difficulties discovering communities or becoming comfortable participating after joining them.

### Interpretation

Discovery and onboarding may affect whether new users successfully transition from finding a community to actively participating in it.

### Confidence

**Medium to Low.**

The evidence is meaningful but occurs less consistently than the major findings concerning persistence, organization, and communication modes.

### Potential Requirement

The system should consider:
- community discovery;
- clear community descriptions;
- understandable community structure;
- onboarding information for new members.

More evidence would be required before treating advanced onboarding functionality as a core requirement.

## 10. Contradictory and Negative Evidence

The collected evidence does not indicate that existing community platforms are generally unsuccessful or unusable.

### 10.1 Existing Platform Satisfaction

Overall satisfaction with existing community platforms was relatively high:
- mean satisfaction: **4.00 / 5**;
- 9 of 12 respondents selected a satisfaction rating of 4 or 5;
- no respondent selected 1 or 2.

This contradicts any strong assumption that users are broadly dissatisfied with existing platforms.

### Interpretation

The project should not be justified by claiming that existing platforms fail completely.

A more evidence-supported problem statement is that users who are generally satisfied with existing platforms still experience specific problems involving:
- information persistence;
- organization;
- retrieval;
- fragmentation across platforms;
- moderation;
- balancing persistent and quick communication.

### 10.2 Multi-Platform Usage Is Not Universal

Two of twelve survey respondents reported that they do not use multiple platforms for the same interest or community.

Therefore, platform fragmentation should not be presented as a universal user problem.

### 10.3 Information Retrieval Is Not Difficult for Everyone

Two respondents rated information retrieval at 5 out of 5 and three rated it at 4 out of 5.

This indicates that some users are satisfied with existing information-retrieval mechanisms.

### 10.4 Different Users Have Different Priorities

The qualitative discussions show different priorities.

For example:
- some participants emphasized search and persistent information;
- some emphasized moderation;
- some emphasized onboarding and community accessibility;
- some emphasized interface simplicity.

The proposed system should therefore avoid assuming that one feature set will solve every user's community-platform problems.

## 11. Evaluation of Initial Assumptions

### A1. Users experience problems when useful information is communicated primarily through chat.

**Status:** Supported.

Evidence includes 8 of 12 survey respondents reporting lost information and multiple qualitative participants describing difficulty retrieving previous chat content.

### A2. Users value persistent discussions.

**Status:** Supported.

The mean importance score was 4.42 out of 5, with 11 of 12 respondents selecting 4 or 5.

### A3. Users also value quick informal communication.

**Status:** Supported.

The mean importance score was 4.17 out of 5, with 10 of 12 respondents selecting 4 or 5.

### A4. Users frequently use multiple platforms because different systems serve different purposes.

**Status:** Supported within the collected sample.

Ten of twelve survey respondents reported using multiple platforms at least sometimes, and all four qualitative participants described multi-platform behavior.

### A5. Users are dissatisfied with existing community platforms.

**Status:** Not supported.

Mean satisfaction was 4.00 out of 5, and 9 of 12 respondents selected 4 or 5.

The project should therefore focus on specific unresolved problems rather than general dissatisfaction.

### A6. Users would prefer the proposed Thematic Communities Platform over existing alternatives.

**Status:** Unverified.

The research investigated current behavior and problems rather than asking participants to evaluate a complete proposed product.

No claim about adoption preference can currently be made.

### A7. Combining persistent discussions and quick communication in one environment will improve user experience.

**Status:** Partially supported but not verified.

The evidence shows that users value both interaction modes and often use different platforms for them.

However, the research does not yet demonstrate that integrating them into one system will necessarily produce a better user experience.

This assumption should be evaluated through prototype testing and subsequent usability evaluation.

## 12. Research Findings and Potential Requirements

| Finding | Evidence Summary | Confidence | Potential Requirement |
|---|---|---|---|
| F1 - Information persistence | 8/12 report lost chat information; multiple discussion participants report retrieval problems | High | Persistent publications and retrievable discussions |
| F2 - Persistent and quick communication | Persistent discussions 4.42/5; quick communication 4.17/5; all discussions distinguish the two modes | High | Support both publication-oriented interaction and community chat |
| F3 - Multi-platform usage | 10/12 use multiple platforms at least sometimes; all four discussion participants describe multi-platform usage | High | Provide multiple complementary community interaction mechanisms in one environment |
| F4 - Organization and retrieval | Lost information, disorganized discussions, old-discussion retrieval problems, qualitative search requests | High | Structured content organization and search |
| F5 - Moderation | 4/12 report moderation problems; qualitative evidence identifies moderation as affecting quality | Medium | Community roles and basic moderation capabilities |
| F6 - Discovery and onboarding | Survey and qualitative evidence identify discovery and newcomer difficulties | Medium-Low | Community discovery and clear onboarding information |

## 13. Research-Informed Priorities

Based on the collected evidence, the strongest research-supported areas for the proposed system are:

### Higher Priority
1. Persistent and organized community publications.
2. Quick community communication.
3. Clear separation and relationship between persistent and quick interaction.
4. Information retrieval and content organization.
5. Basic community structure and membership.

### Medium Priority
6. Moderation and role-management capabilities.
7. Community discovery.

### Requires Further Validation
8. Advanced onboarding functionality.
9. Automatic conversion of chat discussions into persistent content.
10. Automatic topic organization.
11. Advanced cross-platform integration.

These priorities are research-informed rather than final. Final requirement priorities are defined during requirements specification.

## 14. Limitations

The findings must be interpreted within the limitations of the research.

### Sample Size

The survey contains 12 responses and the qualitative research contains four participants.

This is sufficient for preliminary project validation but not for statistical generalization to the entire population of online-community users.

### Convenience Sampling

Participants were selected through convenience sampling.

The sample may therefore overrepresent university students and users with similar demographic or technological backgrounds.

### Platform Distribution

Discord, Telegram, and Reddit are strongly represented in the collected evidence.

The findings may not represent users whose primary communities exist on other platforms.

### Self-Reported Evidence

The research records what participants report about their behavior rather than observing their behavior directly.

### Prototype Not Evaluated

Participants were not asked to evaluate a complete implementation of the proposed platform.

Therefore, the research supports the relevance of several problems but does not demonstrate that the proposed system will successfully solve them.

## 15. Conclusion

The research provides preliminary evidence that potential users value both persistent discussions and quick communication while experiencing recurring problems involving information loss, organization, retrieval, and fragmentation across platforms.

The strongest findings concern:
- information persistence;
- the importance of both persistent and quick communication;
- multi-platform usage;
- organization and retrieval.

At the same time, respondents generally reported high satisfaction with their existing platforms. The project should therefore not position the proposed system as a replacement for universally inadequate existing platforms.

Instead, the project addresses a narrower research-supported opportunity: providing a thematic community environment in which persistent structured interaction and quick communication can coexist while maintaining clearer organization and retrievability.

The findings provide input to the initial requirements specification. Whether the proposed design actually improves user experience must be evaluated later through prototype verification and usability testing.

