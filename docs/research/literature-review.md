# Literature Review

## 1. Introduction

Online communities are socio-technical systems in which users exchange information, communicate, create content, establish social relationships, develop norms, and participate in governance.

Modern online communities take multiple forms, including forums, social-media groups, question-and-answer communities, chat-oriented platforms, professional communities, gaming communities, educational communities, and hybrid environments.

The preliminary user research conducted for the Thematic Communities Platform identified several recurring concerns:

- useful information becoming difficult to retrieve in fast-moving communication;
- the importance of persistent and organized discussions;
- the importance of quick informal communication;
- use of multiple platforms for the same interest or community;
- difficulties with content organization and retrieval;
- moderation and governance;
- discovery and newcomer participation.

The literature review therefore examines scientific research concerning participation, information organization, rapid digital communication, cross-platform communities, governance, moderation, onboarding, and community development.

The purpose of the review is not to prove that the proposed system is superior to existing platforms.

Instead, the review identifies established findings, limitations, disagreements, and design implications that can inform the subsequent requirements and system-design stages.

## 2. Review Scope and Source Selection

The review focuses on research concerning:

1. participation in online communities;
2. engagement and contribution;
3. persistent and structured community content;
4. rapid digital communication and information overload;
5. cross-platform community activity;
6. community governance and moderation;
7. newcomer onboarding and socialization;
8. differences between community values and needs;
9. community development over time.

The literature corpus contains 22 scientific publications.

Twenty-one publications were published between 2021 and 2026.

One publication, Malinen (2015), is retained as foundational literature because it provides a systematic synthesis of empirical research concerning user participation in online communities.

The literature includes peer-reviewed work from venues including Computers in Human Behavior, Information & Management, MIS Quarterly, Journal of Computer-Mediated Communication, European Management Journal, Journal of the Association for Information Science and Technology, New Media & Society, Proceedings of the ACM on Human-Computer Interaction, ICWSM, The Web Conference, and peer-reviewed Springer conference proceedings.

A structured analysis of the publications is provided in:

`docs/research/literature-analysis.md`

## 3. Participation in Online Communities

### 3.1 Participation Is Multidimensional

Malinen (2015) reviewed empirical research concerning participation in online communities and showed that participation cannot be represented adequately through a simple active-versus-passive distinction.

Community members may read content, search for information, create posts, respond to others, communicate informally, contribute knowledge, or participate in governance.

Trunfio and Rossi (2021) similarly show that digital engagement is a multidimensional concept rather than a single behavioral indicator.

These findings are relevant to the proposed project because meaningful participation should not be measured only by the number of publications a user creates.

A member who primarily reads discussions, searches existing information, or participates in quick community communication may still receive substantial value from the community.

### 3.2 Community Size Is Not Equivalent to Community Success

Hwang and Foote (2021) studied persistently small Reddit communities and found that participants may value small communities because of specialization, familiarity, social connection, and interaction quality.

This challenges the assumption that successful communities must continually maximize growth.

For the proposed platform, a thematic community with a relatively small membership may still be successful if it provides useful interaction and relevant information to its members.

### 3.3 Community Needs Change Over Time

Zhao and Wagner (2024) examined differences in user motivation across stages of online-community development.

Their results indicate that motivational factors can change as communities develop.

Early-stage communities may face problems related to initial participation and growth, while mature communities may face different participation and sustainability challenges.

The proposed platform should therefore distinguish between creating and discovering new communities and maintaining established communities.

## 4. Community Design and Contribution

### 4.1 Social Features Affect Contribution Differently

Prom Tep et al. (2022) investigated the effect of social features on member contribution.

Their findings indicate that social functionality can influence contribution, but its effects differ according to user involvement and context.

This means that simply increasing the number of social features does not necessarily produce better community outcomes.

For the proposed system, posts, comments, chat, profiles, roles, and other functionality should be justified through user scenarios rather than treated as beneficial merely because they exist.

### 4.2 Community Value Depends on Social and Technical Factors

Priharsari and Abedin (2021) analyzed approximately 28,000 posts and 26 interviews across organization-sponsored online communities.

They identified factors including content quality, transparency, participatory leadership, social hierarchy, sense of community, flexibility, and privacy.

Importantly, the same factor could act as either a facilitator or a constraint depending on context.

Masson and Parmentier (2023), in a systematic review of 178 selected studies, similarly identify mechanisms such as socialization, structuring, participation, commitment, and shared motivations as contributors to online-community performance.

These findings indicate that online-community success cannot be reduced to software functionality.

Technical features create possibilities for interaction, but their outcomes depend on how communities use them.

## 5. Persistent Information and Knowledge Organization

### 5.1 Online Communities Accumulate Reusable Knowledge

Online-community interactions may remain useful long after the initial conversation has ended.

Qiu et al. (2021), using Wikipedia as an online knowledge-community environment, show that collaborative and communicative interactions contribute differently to the organization of collective knowledge.

Although Wikipedia differs from a thematic discussion platform, the study demonstrates that information organization is shaped by interaction structure rather than simply by the existence of user-generated content.

The relevance to this project is indirect but meaningful: persistent community information requires mechanisms that support organization and later retrieval.

### 5.2 Topic Structure and Informal Interaction Can Coexist

Dahana et al. (2024) investigated on-topic and off-topic discussions in an online community.

Their results indicate that on-topic communication can encourage participation, while off-topic communication is not necessarily harmful and may also contribute to community participation depending on context.

This creates a design trade-off.

A thematic community needs enough structure to preserve topic relevance, but eliminating informal communication entirely may remove an important social function.

The project should therefore consider structured persistent content and informal communication as complementary rather than mutually exclusive interaction modes.

## 6. Rapid Communication and Information Overload

### 6.1 Rapid Digital Communication Provides Speed but Creates Organizational Costs

Stray and Barbala (2024) studied Slack use in a large-scale software organization through 13 interviews.

Slack supported transparency, rapid responses, continuous communication, structured channels, and knowledge sharing.

However, participants also experienced information overload and reduced focus.

The study is not a direct examination of public thematic communities, but it demonstrates a relevant trade-off in persistent chat environments: communication speed and visibility can coexist with increasing information volume and difficulty managing attention.

### 6.2 Information Overload Also Appears Outside Enterprise Slack

Reiber et al. (2026) studied digitally facilitated communities using Discord, WhatsApp, and Slack through 17 qualitative interviews.

Participants described digital communication as essential for coordination, but also identified information overload, security concerns, and difficulties building trust and consensus.

This provides evidence outside Reddit that rapid text-based communication can create information-management challenges.

For the proposed project, these findings support the relevance of information-overload concerns, but they do not prove that a post-and-chat architecture is the optimal solution.

That remains a project hypothesis requiring prototype evaluation.

## 7. Cross-Platform Community Activity

### 7.1 Communities Can Exist Across Multiple Platforms

Singh et al. (2024) studied 15 communities that were active on both Reddit and Discord.

The researchers identified differences in harmful language, topics, user behavior, and moderation practices between the two platforms.

The study demonstrates that a single community identity may extend across multiple technical platforms and that platform characteristics influence community behavior.

This provides literature support for the observation from the project's user research that community activity may be distributed across different applications.

However, the study does not establish that users necessarily want all activities consolidated into one platform.

### 7.2 Different Platforms May Support Different Interaction Patterns

Cross-platform behavior should therefore not automatically be interpreted as a failure.

Users may deliberately choose different systems because those systems provide different affordances.

The engineering question is not simply whether multiple platforms are used, but whether unnecessary fragmentation creates usability or information-management costs.

This distinction is important for the proposed platform because the project should not claim that all cross-platform activity is undesirable.

## 8. Community Values and Heterogeneity

### 8.1 Different Communities Prioritize Different Values

Weld, Zhang, and Althoff (2022) surveyed 2,769 users across 2,151 subreddits.

Their results show substantial variation in the values that communities and users consider important.

This argues against a universal community-governance model.

The proposed platform should therefore provide reusable community mechanisms while allowing communities to develop different rules and interaction practices.

### 8.2 Governance Success Is Context Dependent

Weld et al. (2025) further examined perceptions of moderators across Reddit communities.

Their findings indicate that governance quality is multidimensional and depends on community characteristics.

For example, stricter enforcement may be perceived differently depending on community topic and context.

This further supports configurable rather than universally prescriptive governance.

## 9. Governance and Moderation

### 9.1 Governance Becomes More Formal as Communities Mature

Frey et al. (2022) analyzed approximately 80,000 communities across Minecraft, Reddit, and World of Warcraft.

Institutional formalization was generally associated with community maturity, including age, population size, and engagement.

This suggests that rules and governance mechanisms become increasingly relevant as communities develop.

For the proposed platform, ownership, moderation roles, and community rules therefore have research support as general community mechanisms.

### 9.2 Administrators Can Also Be Active Community Participants

Teng et al. (2022) examined data from 1,115 users and found that users taking administrator roles can contribute to opinion leadership and community contribution.

This indicates that administrators and moderators should not necessarily be modeled as actors who only enforce rules.

They may also remain ordinary participants in community interaction.

### 9.3 Algorithmic Moderation Changes Human Moderator Behavior

He, Hong, and Raghu (2025) examined 156 Reddit communities and the introduction of algorithm-based moderation tools.

Their findings indicate that moderation bots can change volunteer moderator behavior and can shift human effort toward broader policing and community-nurturing activity.

The study therefore suggests that automated moderation should be understood as part of a human-machine governance system rather than a direct replacement for human moderators.

### 9.4 Governance Involves Psychological and Social Trade-Offs

Bulat et al. (2025) surveyed 605 Reddit moderators.

They found that participatory governance can be associated with perceived fairness but does not automatically produce stronger belonging or institutional acceptance.

More centralized governance approaches may also produce positive psychological outcomes under some conditions.

The finding warns against assuming that more democratic governance is universally superior.

### 9.5 Moderation Strategy Influences Participation

Dwork et al. (2024) developed a theoretical framework showing that moderation can alter who participates in a community and therefore affect the composition of the community itself.

Sun and Sun (2026) examined approximately 530.5 million engagement records and 13.3 million moderation actions across 152 Reddit communities.

Their findings indicate that moderation effects vary depending on strategy, moderator identity, and user activity level.

Silent removal was associated with reduced subsequent engagement among highly active users, while some human soft interventions supported engagement.

This indicates that moderation should not be treated only as binary deletion.

Communication, transparency, and intervention style also matter.

### 9.6 Proactive Guidance Can Reduce Moderation Problems

Horta Ribeiro et al. (2025) evaluated Reddit's Post Guidance system through a randomized experiment involving 97,616 posters across 33 subreddits.

The intervention provided guidance while users were preparing posts.

The experiment found more successful posts, reduced manual moderator workload, greater contribution quality, and no detected reduction in subsequent posting activity.

This suggests that moderation can include proactive guidance rather than only reactive enforcement.

However, this functionality is more appropriate as a possible future enhancement than as a mandatory first-version requirement for the proposed project.

## 10. Newcomer Onboarding and Socialization

Pethig et al. (2025) investigated behavior toward newcomers through a natural experiment on a large online deal-sharing community.

An intervention encouraging existing members to behave more considerately toward newcomers caused newcomer contributions to receive 54% more comments and increased the likelihood of newcomers making another contribution by approximately 10%.

The study did not find an improvement in the quality of later contributions, which is an important limitation.

The evidence therefore supports the importance of newcomer treatment and socialization, but does not demonstrate that onboarding interventions solve every newcomer-related problem.

For the proposed platform, simple onboarding mechanisms such as clear community descriptions, visible rules, and understandable entry points are more strongly justified than complex automated onboarding systems.

## 11. Critical Synthesis

### 11.1 Participation Is Heterogeneous

The literature consistently shows that meaningful participation includes multiple behaviors.

Reading, searching, posting, commenting, communicating, contributing knowledge, moderating, and governing may all represent meaningful participation.

The platform should therefore avoid treating post creation as the only indicator of community engagement.

### 11.2 Persistent Information and Rapid Communication Serve Different Purposes

The reviewed research indicates that persistent knowledge organization and rapid digital communication provide different benefits.

Research on structured knowledge environments emphasizes organization and accumulated information, while Slack-, Discord-, and other communication-focused studies identify speed and coordination benefits alongside overload risks.

The literature therefore supports the existence of a trade-off between communication immediacy and information manageability.

It does not establish one universally optimal mechanism for combining these functions.

### 11.3 Community Activity May Span Platforms

Cross-platform community research confirms that communities can operate on multiple platforms and exhibit different behavior on each.

This supports the relevance of fragmentation as a phenomenon.

However, multi-platform usage should not automatically be treated as a problem because users may intentionally benefit from specialized platform capabilities.

### 11.4 Community Design Is Socio-Technical

Community outcomes depend on more than software functionality.

Leadership, norms, content quality, community maturity, governance, motivation, privacy, and moderation all interact with technical features.

Therefore, implementing technically correct community features cannot by itself guarantee successful community formation.

### 11.5 Governance Is Context Dependent

Different communities value different governance approaches.

Recent evidence also demonstrates that moderation strategy and communication style affect participants differently.

The proposed platform should therefore provide understandable governance mechanisms without assuming that one moderation policy fits every community.

### 11.6 Newcomer Experience Matters

Research on newcomer socialization indicates that early interaction with existing community members can influence whether newcomers return.

The proposed system should therefore consider entry experience and clarity of community expectations.

## 12. Relationship to Project User Research

The project's own research consisted of:

- 12 anonymous survey respondents;
- 4 semi-structured user discussions.

The user research identified several patterns that are relevant to the literature.

### 12.1 Information Persistence

Eight of twelve survey respondents reported that important information becomes lost in chat messages.

Five of twelve reported difficulty finding old discussions, and six reported that discussions become disorganized.

The mean score for ease of finding useful or previously discussed information was 3.42 out of 5.

The literature on rapid communication environments does not reproduce this exact user finding, but studies of Slack, Discord, WhatsApp, and other digital communication environments identify information overload and information-management challenges.

The project's user evidence is therefore consistent with broader literature concerning communication overload, although the exact problem remains project-specific.

### 12.2 Persistent and Quick Communication

Organized and persistent discussions received a mean importance rating of 4.42 out of 5.

Eleven of twelve respondents rated them 4 or 5.

Quick informal communication received a mean importance rating of 4.17 out of 5.

Ten of twelve respondents rated it 4 or 5.

All four qualitative participants described different uses for persistent and quick communication.

The literature supports the broader distinction between structured knowledge activity and rapid communication but does not prove that combining both within one application will produce better usability.

### 12.3 Multi-Platform Usage

Ten of twelve survey respondents reported using multiple platforms for the same interest or community at least sometimes.

All four qualitative participants also described multi-platform behavior.

Singh et al. (2024) provide independent scientific evidence that the same communities can operate across Reddit and Discord and display different behavioral patterns on each platform.

However, both the literature and project research indicate that multi-platform usage can reflect useful specialization rather than purely undesirable fragmentation.

### 12.4 Existing Platform Satisfaction

Overall satisfaction with existing platforms remained relatively high at 4.00 out of 5.

Nine of twelve respondents selected a rating of 4 or 5.

Therefore, neither the literature nor the user research supports a claim that existing community platforms are generally inadequate.

The project should instead focus on specific research-supported problems and evaluate whether its particular design provides a useful alternative.

## 13. Research Gaps Relevant to the Project

### 13.1 Integration of Persistent and Quick Communication

The literature supports the relevance of both structured information and rapid communication.

However, it does not establish one universally successful architecture for integrating them.

The effectiveness of combining publication-oriented interaction and community chat therefore remains a project hypothesis.

### 13.2 Information Persistence in Community Chat

Research identifies information overload in Slack, Discord, WhatsApp, and similar environments, but more project-specific evidence is required to determine whether the proposed platform improves retrieval of useful community knowledge.

### 13.3 Cross-Platform Consolidation

Cross-platform communities clearly exist, but the literature does not establish that consolidating their activities into a single platform necessarily improves user experience.

This must be evaluated rather than assumed.

### 13.4 Small Thematic Community Governance

Much of the governance literature focuses on large environments such as Reddit.

Smaller university and interest-based communities may have different moderation and governance requirements.

### 13.5 Onboarding in Small Interest Communities

Newcomer research establishes that socialization matters, but the appropriate onboarding mechanisms for smaller thematic communities remain context dependent.

## 14. Implications for System Requirements

The literature should not be used to justify implementation details more strongly than the evidence allows.

### 14.1 Strongly Supported by Literature

The following general capabilities or concerns have strong support across multiple publications:

- support for multiple forms of community participation;
- persistent and organized community information;
- community governance;
- moderation mechanisms;
- differentiation between community needs;
- consideration of community maturity and participation dynamics.

### 14.2 Supported by Literature and Project-Specific User Evidence

The following areas are supported by both broader literature and the project's own evidence:

- information retrieval and discoverability;
- coexistence of persistent and quick communication needs;
- managing information overload;
- cross-platform community activity;
- newcomer participation and onboarding;
- community discovery and organization.

These areas justify further requirements work, but the exact technical implementation remains a design decision.

### 14.3 Proposed Design Decisions Requiring Prototype Validation

The following are proposed engineering solutions rather than directly proven scientific requirements:

- a publication model with posts;
- comments and replies;
- a dedicated community chat;
- a particular owner/moderator permission hierarchy;
- the exact navigation model;
- combining posts and chat within one application;
- automatic conversion of chat activity into persistent knowledge;
- automatic topic organization.

These decisions must be evaluated through prototype verification and usability testing.

## 15. Limitations of the Literature Review

This document is a targeted critical literature review rather than a formal systematic review.

It does not claim exhaustive coverage of all research concerning online communities.

Several publications focus on specific environments such as Reddit, Wikipedia, Slack, TikTok, software organizations, labor organizing, or deal-sharing communities.

Results from these environments cannot automatically be generalized to all thematic communities.

The literature also uses different methodologies, including:

- systematic literature reviews;
- surveys;
- interviews;
- behavioral data analysis;
- theoretical models;
- natural experiments;
- randomized experiments.

These methods answer different research questions and should not be treated as directly equivalent.

The corpus still contains a substantial amount of Reddit-based research, particularly in the area of moderation and governance.

This limitation is partially mitigated by literature concerning Minecraft, World of Warcraft, TikTok, Wikipedia, Slack, Discord, WhatsApp, software organizations, and other online-community contexts.

The literature is therefore used together with project-specific user evidence rather than as a substitute for it.

## 16. Conclusion

The reviewed scientific literature indicates that online communities are socio-technical environments in which participation, information organization, governance, moderation, social interaction, and community maturity interact.

The strongest conclusions relevant to the Thematic Communities Platform are:

1. meaningful participation takes multiple forms;
2. persistent information and rapid communication provide different benefits;
3. rapid communication environments can produce information-overload challenges;
4. the same community can operate across multiple platforms;
5. governance and moderation significantly influence community participation;
6. different communities require different governance approaches;
7. newcomer treatment can influence continued participation;
8. technical features alone do not guarantee successful community outcomes.

These findings support the relevance of the problems addressed by the project.

However, the literature does not prove that the proposed combination of posts, comments, chat, discovery, membership, and moderation will produce a better user experience than existing platforms.

That remains an engineering hypothesis to be evaluated through the project's prototype, verification activities, and subsequent usability testing.

## References

Bulat, B., Wang, H., Fujimoto, S., & Frey, S. (2025). The psychology of volunteer moderators: Tradeoffs between participation, belonging, and norms in online community governance. *New Media & Society, 27*(11), 5962–5985. https://doi.org/10.1177/14614448241259028

Dahana, W. D., Igarashi, M., Sakiyama, R., & Zhou, J. (2024). Impact of on-topic and off-topic discussions on member participation and contribution in a common-identity online community. *Telematics and Informatics Reports, 16*, 100172. https://doi.org/10.1016/j.teler.2024.100172

Dwork, C., Hays, C., Kleinberg, J., & Raghavan, M. (2024). Content moderation and the formation of online communities: A theoretical framework. *Proceedings of the ACM Web Conference 2024*, 1307–1317. https://doi.org/10.1145/3589334.3645490

Frey, S., Zhong, Q., Bulat, B., Weisman, W. D., Liu, C., Fujimoto, S., Wang, H. M., & Schweik, C. M. (2022). Governing online goods: Maturity and formalization in Minecraft, Reddit, and World of Warcraft communities. *Proceedings of the ACM on Human-Computer Interaction, 6*(CSCW2), Article 300. https://doi.org/10.1145/3555191

He, Q., Hong, Y., & Raghu, T. S. (2025). Platform governance with algorithm-based content moderation: An empirical study on Reddit. *Information Systems Research, 36*(2), 1078–1095. https://doi.org/10.1287/isre.2021.0036

Horta Ribeiro, M., West, R., Lewis, R., & Kairam, S. (2025). Post Guidance for Online Communities. *Proceedings of the ACM on Human-Computer Interaction, 9*(2), Article CSCW148. https://doi.org/10.1145/3711046

Hwang, S., & Foote, J. D. (2021). Why do people participate in small online communities? *Proceedings of the ACM on Human-Computer Interaction, 5*(CSCW2), Article 462. https://doi.org/10.1145/3479606

Malinen, S. (2015). Understanding user participation in online communities: A systematic literature review of empirical studies. *Computers in Human Behavior, 46*, 228–238. https://doi.org/10.1016/j.chb.2015.01.004

Masson, Z., & Parmentier, G. (2023). Drivers and mechanisms for online communities performance: A systematic literature review. *European Management Journal, 41*(4), 590–606. https://doi.org/10.1016/j.emj.2022.08.005

Pethig, F., Hoehle, H., Hui, K.-L., & Lanz, A. (2025). Behavior toward newcomers and contributions to online communities. *MIS Quarterly, 49*(2), 731–758. https://doi.org/10.25300/MISQ/2024/17759

Priharsari, D., & Abedin, B. (2021). What facilitates and constrains value co-creation in online communities: A sociomateriality perspective. *Information & Management, 58*(6), 103433. https://doi.org/10.1016/j.im.2021.103433

Prom Tep, S., Aljukhadar, M., Sénécal, S., & Dantas, D. C. (2022). The impact of social features in an online community on member contribution. *Computers in Human Behavior, 129*, 107149. https://doi.org/10.1016/j.chb.2021.107149

Qiu, J., Zuo, M., Wang, J., & Cai, C. (2021). Knowledge order in an online knowledge community: Group heterogeneity and two paths mediated by group interaction. *Journal of the Association for Information Science and Technology, 72*, 1075–1091. https://doi.org/10.1002/asi.24475

Reiber, F., Chator, A., Calacci, D., & McDonald, A. (2026). Organizing in the digital age: Understanding community, challenges, and consequences in digitally-facilitated labor organizing. *Proceedings of the ACM on Human-Computer Interaction, 10*(6), Article CSCW133. https://doi.org/10.1145/3816981

Singh, A. K., Ghafouri, V., Such, J., & Suarez-Tangil, G. (2024). Differences in the toxic language of cross-platform communities. *Proceedings of the International AAAI Conference on Web and Social Media, 18*(1), 1463–1476. https://doi.org/10.1609/icwsm.v18i1.31402

Stray, V., & Barbala, A. (2024). Slack use in large-scale agile organizations: ESN tools as catalysts for alignment? In *Agile Processes in Software Engineering and Extreme Programming (XP 2024)* (pp. 20–35). Springer. https://doi.org/10.1007/978-3-031-61154-4_2

Sun, M., & Sun, S. (2026). Human versus machine as content moderators: Examining the effects of moderation strategies on Reddit. *Journal of Computer-Mediated Communication, 31*(3), zmag013. https://doi.org/10.1093/jcmc/zmag013

Teng, C.-I., Huang, T.-L., Liao, G.-Y., & Dennis, A. R. (2022). Administrator-users contribute more to online communities. *Information & Management, 59*(8), 103717. https://doi.org/10.1016/j.im.2022.103717

Trunfio, M., & Rossi, S. (2021). Conceptualising and measuring social media engagement: A systematic literature review. *Italian Journal of Marketing, 2021*, 267–292. https://doi.org/10.1007/s43039-021-00035-8

Weld, G. C., Leibmann, L., Zhang, A. X., & Althoff, T. (2025). Perceptions of moderators as a large-scale measure of online community governance. *Proceedings of the ACM on Human-Computer Interaction, 9*(7), Article CSCW463. https://doi.org/10.1145/3757644

Weld, G. C., Zhang, A. X., & Althoff, T. (2022). What makes online communities “better”? Measuring values, consensus, and conflict across thousands of subreddits. *Proceedings of the International AAAI Conference on Web and Social Media, 16*(1), 1121–1132. https://doi.org/10.1609/icwsm.v16i1.19363

Zhao, H., & Wagner, C. (2024). Crossing the chasm: Understanding users' motivational differences based on stages of online community. *Information & Management, 61*(8), 104050. https://doi.org/10.1016/j.im.2024.104050