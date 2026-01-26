# 📅 2026-01-26 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | [PR #30](https://github.com/decentralized-identity/trusted-ai-agents/pull/30/changes) | Dmitri | |
| 5min | Doodle poll for delegated Authority: https://doodle.com/group-poll/participate/aOXyzXQb/vote | Dmitri | |
| 10min | Progress reports on work items: 1. Delegated Authority Report 2. Prototyping on AWS: MCP-i | Alan, Juan ||
| 5min | Tom's threat modeling [document](https://docs.google.com/document/d/1I8hJH8QdVps4ISqnfVlLsBecQ28KfXonIApx4Avot_M/edit?usp=sharing)| Tom ||

## Minutes

- PR #30
  - Dima: Let's get some +1s and merge it
  - BF:
- Doodle poll for delegated Authority: https://doodle.com/group-poll/participate/aOXyzXQb/vote
- Progress reports on work items:
  - Delegated Authority Report
    - Dima: Just getting calls together; first meeting next week
    - Alan: i've filled in 80% of Deb's outline, first draft done by end of week; treat it like a rough draft and edit away, everyone!
      - bf: can people read it before the first meeting? dima/alan: please do!
      - alan: kudos to deb for shaping it! dima: and kudos to alan for powering through it before the first meeting
  - Prototyping on AWS: MCP-i?
    - bf: VPS is up, people can reach out if they want to prototype with MCP-i or with anything else
    - Alan: I read the MCP-i doc, I don't find the confused deputy section very convincing; i'm discussing with them on their discord
- Potential future work items
  - Tom's threat modeling [document](https://docs.google.com/document/d/1I8hJH8QdVps4ISqnfVlLsBecQ28KfXonIApx4Avot_M/edit?usp=sharing)?
    - Tom's explanation:
      - 1. (formally) this is a good threat modeling exercise
      - 2. (contentwise) i believe we should start thinking against MCP/server-centric models, the more i wrote this the more i was convinced this usecase is better for A2A
      - instructions for review: read first 2 pages closely, the rest isn't even fully fleshed out;
    - tom will send a use case to bf to PR it into the use-cases folder
- Action Items
  - [ ] EVERYONE - Review Tom's Threat Model for a Personal Agent usecase before next meeting - any feedback welcome
  - [ ] DELEGATION TEAM - Respond to Dmitri's Doodle on the mailing list and in Slack
  - [ ] DELEGATION TEAM - Review of Alan's rough draft before first meeting
  - [ ] PROTOTYPERS - reach out to BF on DIF Slack if you need access to the MCP-i VPS or if you have another usecase/toolchain you want to prototype

# 📅 2026-01-012 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| **5 min** | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group's JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min** | Review of previous action items | Chairs | Quick review of open items and updates from prior meetings. |
| **20 min** | **Main Topic:** Review current status and define next steps | Chairs | Take stock of where we are with agentic identifiers and agentic identity work. Decide on the next steps forward. |
| **5 min** | Review decisions and action items<br>Planning for next meeting | Chairs | Summarize key decisions, confirm action owners, and discuss agenda for next session. |

## Attendees

- Dmitri Zagidulin
- Alan Karp
- Alex Bainbridge
- Alex
- Dylan Hobbs
- Juan C.
- Jim St. Clair
- Debb
- Sachio Iwamoto 
- Victor Lu
- Mitchell Travers
  
## Notes

- https://github.com/decentralized-identity/taa-delegatable-authorization-tf
- [Review the ](https://difdn.slack.com/archives/C0A70MT32QL/p1767970277273299 Debbi's strawman TOC)
- 3 leads propose 3 times that work.
- Use this meeting for progress reports.
- MCP-I progression.
- Previous TOC:
    1. Problem Statement: Delegation vs. Agency
    • What breaks when authority must cross heterogeneous systems
    • Why “agent intelligence” is not the core problem
    2. Authority Continuity and Intent
    • Delegation as a continuation property, not a transferable object
    • Mutable intent and bounded authority
    3. Execution Boundaries and Verification
    • Where verification must occur when no single system is authoritative
    • Resource PDPs vs. gateways vs. runtime enforcement
    4. Delegation Chains and Chaining Hazards
    • Confused deputy, covert channels, and authority creep
    • Why blocking delegation fails in practice
    5. Policy as Constraint, Not Prompt
    • Deterministic policy enforcement vs. nondeterministic interpretation
    • Separation of prompts, policies, and execution
    6. Auditability and Provenance
    • What must be observable at runtime
    • What existing systems fail to record
    7. Capability-Based vs. Token-Based vs. Continuity-Based Models
    • Where each model holds
    • Where they break in distributed agent systems
    8. Implications for Agent Interoperability
    • Cross-domain delegation
    • Federated and decentralized environments
    9. Open Questions and Research Gaps
    • What is not yet well understood
    • Areas for prototyping and comparison

## Action Items

- [ ] Debb to push to markdown for Google docs.
- [ ] Dimitri schedule doodle for folks to work on the work stream directly
- [ ] Conveners : Propose time slots in slack channel.
- [ ] This meeting to move to 30 min as a status update.

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| **5 min** | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group's JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min** | Review of previous action items | Chairs | Quick review of open items and updates from prior meetings. |
| **20 min** | **Main Topic:** Review current status and define next steps | Chairs | Take stock of where we are with agentic identifiers and agentic identity work. Decide on the next steps forward. |
| **5 min** | Review decisions and action items<br>Planning for next meeting | Chairs | Summarize key decisions, confirm action owners, and discuss agenda for next session. |

## Attendees

## Notes

- Delegation requirements helpful to document and formalize (Alan)
- Capability authz task force (Dmitri)
- Architecture and Distributed Transactions has to be addressed by a future work stream to extract common patterns and create a reference architecture; much easier once other work streams have already written reports and prototyped (Juan)
- Tom: Should we just use slack to gather opinions and entice people to contribute to work streams? BF: absolutely! 

### Delegation Authz Work Stream (Use Cases)

- First volunteers: Dmitri, Tom, Dylan, Debb, Alan, Alex
- First deliverable: Pick usecases to target and write report on patterns, requirements and gaps
    + Topics: Revocation in particular

### Governance and/of Policy Work Stream

- Tom: we already have policy syntaxes (Cedar, etc), but are they good enough? How can the syntaxes be anchored in semantics good enough for real-world safety and contracts?
- Alan: Hard to talk about policy semantics without clear governance of those semantics, non? Tom: Yes, but you can isolate the policy relative to specific use cases and leave clearer connections to governance questions 

## Action Items

- [X] Bumblefudge - Set up the Slack channel(s)
- [X] BF - get Alex B into Slack
- [ ] Chairs to meet w/Grace/DIF staff re: archiving significant contributions from outside recorded/minuted meetings

# 📅 2025-12-07 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| **5 min** | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min** | Review of previous action items | Chairs | Quick review of open items and updates from prior meetings. |
| **20 min** | **Main Topic:** Identity Working Group Output | @andor | Discuss agentic identifiers and agentic identity. Prepare a set of valid indentifier for identity requirements per the use case. | 
| **5 min** | Review decisions and action items<br>Planning for next meeting | Chairs | Summarize key decisions, confirm action owners, and discuss agenda for next session. |


| | Pattern |
| -----|--- |
| Use Case | |

## Attendees

## Notes

## Call To Action


# 📅 2025-12-01 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| **5 min** | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min** | Review of previous action items | Chairs | Quick review of open items and updates from prior meetings. |
| **20 min** | **Main Topic:** Timeline Alignment | Chairs | Understand how to structure the first work item. Evaluate the UC/ISSUE[#24](https://github.com/decentralized-identity/trusted-ai-agents/issues/24) |
| **5 min** | Review decisions and action items<br>Planning for next meeting | Chairs | Summarize key decisions, confirm action owners, and discuss agenda for next session. |

## Attendees

* Andor Kesselman
* Nicola Gallo 
* Alan Karp
* Neil Thomson 
* Subra
* Makki Elfaith 
* Michael Herman
* Tom Jones
* Dmitri
* Jim St.
* Sachio Iwamoto
* Douglas Rice
* Eric Drury
* Matt Arcblock

## Notes

* https://modelcontextprotocol.io/specification/2025-11-25/changelog
* https://hyperonomy.com/2025/10/14/web-7-0-agentic-os-agent-architecture-reference-model-aarm/#mcp
* https://blog.modelcontextprotocol.io/posts/2025-11-25-first-mcp-anniversary/  
* https://mcp.mintlify.app/specification/draft/basic/authorization#standards-compliance


## Call To Action

- [ ] @andor : issue Decompose and generalize patterns


# 📅 2025-11-24 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **20 min** | **Main Topic:** Timeline Alignment                                | Chairs   |Understand how to structure the first work item. Evaluate the PR [#22](https://github.com/decentralized-identity/trusted-ai-agents/pull/22) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          
## Attendees:                                                                                                                                                                                             

* Nicola Gallo
* Andor Kesselman
* Dmitiri Zagidulin
* Makki Elfaith 
* Sachio Iwamoto
* Subra
* Tom Jones
* Neil Thompson
* Victor Lu
* Iain Henderson
* Matt

## Call To Action

- [ ] Calendar negotation / travel?
- [ ] 

## Notes

* How do agents interact with each-other.
* 

## Call To Action

`TO BE FILLED AFTER THE MEETING`


# 📅 2025-11-17 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **20 min** | **Main Topic:** Timeline Alignment                                | Chairs   | [#20](https://github.com/decentralized-identity/trusted-ai-agents/pull/20) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          ## Attendees:                                                                                                                                                                                             

## Call To Action 

* Agentic Identity & Control Authority : 9
  * Dmitri Zagidulin
  * Jim
  * Alan
  * Makki
  * Subra
  * Geun HK
  * Sachio
  * Andor
  * Nicola
* Trust Fabric, Attestation and Policy : 5
  * Nicola
  * Neil
  * Dmitri
  * Geun
  * Sachio
* Decentralized Discovery and Trust Registry :  4
  * Dmitiry
  * Jim
  * Sachio
  * Nicola
* Adaptive Workflow Orchestration : 2
  * Andor
  * Nicola
* Agentic Negotiation, Commerce, & Value Exchange : 4
  * Dmitri
  * Alan
  * Geun
  * Subra
* Verifiable Decision Trail : 2
  * Nicola
  * Dmitri

## Notes:

* Alan Karp : https://www.computer.org/csdl/magazine/sp/5555/01/11194053/2aB2Rf5nZ0k
* Dmitri Zagidulin
* Neil Thomson
* Alan Karp
* Michael Herman
* Sachio Iwamoto
* Douglas Rice
* Geun Hyung Kim
* Iain Henderson
* Jim St Clair
* Nicola Gallo
* Subra
* Tom Jones
* Victor Lu
* Matt McKinney
* Makki

## Call To Action 

* Send a message about workstream structure. Decided we will focus on identity to start. Swap out existing time. 

# 📅 2025-11-10 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **20 min** | **Main Topic:** Timeline Alignment                                | Chairs   | [PR #14](https://github.com/decentralized-identity/trusted-ai-agents/pull/14) and [PR #15](https://github.com/decentralized-identity/trusted-ai-agents/pull/15) and [PR #17](https://github.com/decentralized-identity/trusted-ai-agents/pull/17) and [PR #19](https://github.com/decentralized-identity/trusted-ai-agents/pull/19)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        

### Attendees :

* Tom Jones
* Alan Karp
* Douglas Rice
* Thierry Thevenet (Talao),
* Andor Kesselman,
* Michael Herman,
* Iain Henderson,
* nicolagallo,
* Mark Lizar,
* Victor Lu,
* Neil Thomson,
* Makki Elfatih,
* Geun-Hyung Kim,
* Agne Caunt,
* Victor Lu,
* Makki Elfatih
 
## Notes

**DISCLAIMER**

*This meeting summary was automatically generated by Zoom’s AI features and has not been reviewed for accuracy or completeness. Refer to Zoom’s Terms of Service regarding AI use: [https://www.zoom.com/en/blog/zooms-term-service-ai/](https://www.zoom.com/en/blog/zooms-term-service-ai/)*

*To request edits or deletion, email: [operations@identity.foundation](mailto:operations@identity.foundation)*

**Overview**

The meeting focused on managing and progressing use cases forward, with discussions about starting meetings on time and the importance of having actual users in use cases. The team explored various AI agent use cases, including supply chain scenarios, calendar booking, and travel-related applications, emphasizing the need for trusted sources of information and multiple levels of intermediaries. The group discussed agent identity and responsibility, technology stack requirements, and the process for managing and refining use cases, with plans to continue discussions in the next meeting.

**Use Case Management and Progression**

The meeting began with a discussion about starting meetings on time and managing participants. Tom presented a use case that he had expanded based on Andrew's work, which will be the seventh submitted use case. The group discussed the need to manage and progress use cases forward, as there are currently seven submissions. They also addressed the importance of having actual users in use cases, which Tom highlighted as a personal concern. The meeting was led by Nicola, who shared the agenda, and Andor took attendance. Mark, a new DIF member, introduced himself to the group.

**AI Use Cases and Trust Boundaries**

The team discussed various use cases for AI agents, with Alan presenting a complex supply chain scenario involving multiple trust boundaries and enterprise workflows. Andor emphasized the importance of identifying stakeholders willing to advance each use case, suggesting this could be a key factor in evaluating their feasibility. Alan highlighted that these use cases help identify necessary features for the architecture, such as trust management and agent interactions, even if specific use cases may not be implemented directly.

**AI Use Cases and Implementation Challenges**

The group discussed various use cases for AI agents, focusing on their practical value and implementation challenges. Andor emphasized the importance of validating that developed use cases would benefit real people, while Makki suggested having a variety of use cases even if their exact stakeholders aren't clear yet. Alan highlighted the potential of the calendar booking use case as a test bed for AI agents, noting its adversarial nature and the need for features like discovery, agent communication, and negotiation. Douglas provided insights into the complexities of the travel use case, including multi-level delegations and authorization chains. The group agreed on the potential for collaboration with other working groups to further develop these use cases.

**Travel Use Cases Discussion**

Douglas noted that while a specific use case might not be on the immediate implementation list, it could be socialized within the community to generate interest and workflows over the coming months. Alan highlighted the overlap between the virtual travel agent and enterprise use cases, emphasizing the need for trusted sources of information and multiple levels of intermediaries. Neil pointed out the unique aspects of the travel use case, such as the exchange of personal information and the need for a micro-sharing mechanism to ensure the secure handling of data. The group discussed the differences in data provenance requirements between the hotel booking agent and the calendar agent, with Andor suggesting that the hotel use cases may require more advanced technical solutions.

**AI Governance Use Case Development**

The Working Group is focused on developing a Use Case for governance, with emphasis on retaining information past transactions and defining the scope of allowed actions and conditions. Nicolagallo discussed an industrial environment scenario where AI agents manage sensor data in an oil company setting, highlighting differences between this approach and traditional human-AI interactions. The discussion touched on service mesh projects and identity management, with Nicolagallo noting interesting parallels between current challenges and historical oil industry problems.

**Agent Identity vs Authorization Debate**

The group discussed agent identity and responsibility, with Alan emphasizing that the agent's identity is secondary to authorization and permissions management. Andor expressed concern about the lack of real-world deployment feedback for testing the use case, while Nicole suggested potential testing opportunities. The discussion explored two approaches: using agent identity with carefully managed permissions, or starting with authorization to minimize identity-related complications.

**Digital Identity and Trust Framework**

The group discussed identity and trust in digital systems, with Tom advocating for relationship-based identity rather than endpoint-based identity. Neil shared insights from a UN project on supply chain trust registration, highlighting the need for verifiable registries and organizational trust across boundaries. The team agreed to track Tom's relationship identity documentation in the issues section, with Andor requesting a write-up for better tracking. Alan and Andor also discussed a PR for a use case, seeking feedback from the group.

**Use Case Management Process Review**

The team discussed the process for managing and refining use cases, focusing on how to track and mature approved use cases. Alan shared his experience with creating a pull request and suggested setting up a GitHub action to streamline the process. The group agreed that once a use case is approved, it should be added to a markdown file, with the possibility of having multiple people contribute to the PR. They also discussed the need to prioritize which use case to anchor to, with Andor suggesting they consider other options beyond the current one.

**Use Case Qualification Strategy Discussion**

The team discussed qualifying requirements for use cases, focusing on unique architectural features and enterprise-specific needs. They agreed that leading by component rather than accepting individual use cases might be more effective. Alan and Tom emphasized the importance of distinguishing between individual and enterprise users in travel-related use cases. The group decided to start with agentic discovery as a requirement and to focus on building functional components before expanding features. They planned to continue the discussion in the next meeting.

**Action Items and Tech Stack Requirements**

The meeting focused on action items and technology stack requirements. Andor requested participants to add leads for their use cases and map out technology stack requirements, noting that help could be sought if unable to do so. The group discussed a plan to meet next Monday, and participants expressed gratitude and farewells as the conversation ended.

**Action Items**
1. Tom: Post the relationship identity write-up as a document linked in a new issue in the issues tracker.  
2. All use case proposers/leads: Add a lead for each use case, either in the issue or in the shared sheet.  
3. All use case proposers/leads: Map out technology stack requirements for each use case in the shared sheet (or indicate if help is needed).  
4. Nicola: Lead discussion on use case prioritization and process at the next meeting.  
5. All: Review and provide feedback on Tom's use case in the doc/issue.  
6. Chairs/Andor: Offload the burden of submitting use cases as PRs by helping proposers copy-paste and submit PRs for approved use cases.  
7. All: Consider and discuss at the next meeting the proposal to start by selecting and building out key components (e.g., agentic discovery/registries) and mapping use cases to those components.

# 📅 2025-11-03 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **20 min** | **Main Topic:** Timeline Alignment                                | Chairs   | [PR #2](https://github.com/decentralized-identity/trusted-ai-agents/pull/2) and [https://github.com/decentralized-identity/trusted-ai-agents/issues/3](https://github.com/decentralized-identity/trusted-ai-agents/issues/3) and [#6](https://github.com/decentralized-identity/trusted-ai-agents/issues/6), [7](https://github.com/decentralized-identity/trusted-ai-agents/issues/7)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        

### Attendees :

* Andor
* Dmitri
* Victor
* Tom
* Matt
* Alan Karp
* Iain
* Thierry
* Michael Herman
* Misha
* Douglas Rice
* Jim St. Clair

## Notes

* Richard Peterson : ERC-8004 Trustless Agents. Wants to make sure the efforts are in sync. 
* Jim : Curious about trusted AI Agents. Co-Lead AI Agents in AGNTCY. LF Data Foundation Trustworthy AI Initative.
* Douglas Rice : Co-Chair of Hospitality Travel Group & DIF. How does AI Agents work with Travel?
* Dimitri : Here to get a minimal set of use cases to work on.
* Jim : Why do we need DID's to solve the use case?
* Juan : Disposition is it requires multiple trust boundaries. 
* Juan : Submit a PR? If you're stepping away, allow chairs write directly to branch?
* Alan : This use case is particular on permissions. Delegation vs. Impersonation. 
* Jim : What the most technically elegant solution is decentralized X?
* Alan : Use cases don't present anything about the solution. The use case is the problem.
* Makki : Governance process describes this.
* Alan : Certain enterprise use cases. Centralized is the answer. So it's context based.
* Andor : How strongly positioned do we focus on a particular set of technology?
* Richard : Hybrid based.
* 

## Action Items: 

- [ ] Douglas : Draft a Use Case For H&T.
- [ ] Alan : To submit PR with the Use Case off `main` branch for feedback.

# 📅 2025-10-27 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **20 min** | **AIW Updates:** Timeline Alignment                                | Chairs   | AIW updates       
| **20 min** | **Main Topic:** Timeline Alignment                                | Chairs   | [PR #2](https://github.com/decentralized-identity/trusted-ai-agents/pull/2) and [https://github.com/decentralized-identity/trusted-ai-agents/issues/3](https://github.com/decentralized-identity/trusted-ai-agents/issues/3) and [#6](https://github.com/decentralized-identity/trusted-ai-agents/issues/6), [7](https://github.com/decentralized-identity/trusted-ai-agents/issues/7)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        

### Attendees :
- Andor Kesselman
- Nicola Gallo
- Dimitry Z.
- Neil Thomson
- Geun Hyung Kim
- Ivan
- Victor Lu
- Savita Farooqui
- Alan Karp
- Tom Jones
- Alex Bainbridge
- Douglas Rice

## Notes

**AIW Concepts**
- Know Your Agent w/ KYAPay 
- MCP Governance Challenges 
- Security and Identity in Agentic Browsers 
- Personal AI w/ Loyal Agents
- Private Inference 
- Agentic DNS (IAS)
- Data Provence For Agentic Digital Media
- Limiting Data Access For Agents
- Open Knowledge Graph Agent Protocol
- ERC-8004 -- Trustless Agents 
- Legal Layer for Agentic Commerce Contracts for Rights Duties, Liability
- Murderbot Metaphor 
- Human in the Loop Messaging Protocol
- Tools for Trusting Agents: Leveraging Existing OpenID Fed 
- Agentic Identity Books Club 
- Building Trust in the Agentic Web Through Accountability
- “Agenthood” How first Person identity can apply to AI Agents 
- PEA - Policy Enforcer in your agent 
- Creating An Agentic Trust Market Capability Map
- Maximally Minimal “ Server User-Agents” 
- Agent Evals
- MyTerms and Agents 
- Agent ID Can Be No Stronger Than the Person/Org Behind it
- Fine Grained AuthZ in OAuth and MCP
- Identity delegation with Agents
- Dumb Agents
- Fastest Path to 1 Billion Authenticated Agents
- Human / Agentic Meta Cognition
- How Would you Design Private AI Glasses
- AP2 & ACP Agentic Commerce Impact 
- Agent Surfaces and Digital Freedom 
- JOINC (Audit Langchain)
- How to Reliably Anchor Agents to Ground Truth
- Privacy is Normal and the path to Value in the Agentic Everything
- MCP-I Extending MCP

Notes on: 
1. https://github.com/decentralized-identity/trusted-ai-agents/issues/7
2. https://github.com/decentralized-identity/trusted-ai-agents/issues/5
3. https://github.com/decentralized-identity/trusted-ai-agents/issues/3
4. https://github.com/decentralized-identity/trusted-ai-agents/issues/6

Created https://github.com/decentralized-identity/trusted-ai-agents/issues/10

Tagged discuss-next-call for issues that will be brought up next call.

## Action Items: 

- [ ] Comment on issues async! 

## Goals For Next Call : 

Set a clear course for work in the Working Item. 

# 📅 2025-10-20 Meeting Notes

Note: This is during the week of IIW. We expect less activity than usual tomorrow. 

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings. Notify about wrong repo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **40 min** | **Main Topic:** Process for Managing and Registering Use Cases                                | Chairs   | [PR #2](https://github.com/decentralized-identity/trusted-ai-agents/pull/2) and [https://github.com/decentralized-identity/trusted-ai-agents/issues/3](https://github.com/decentralized-identity/trusted-ai-agents/issues/3)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |


### Attendees :

- Nicola Gallo
- Andor Kesselman 
- Kim Hamilton Duffy
- Tom Jones
- Agne Caunt
- Alan Karp
- Alex Bainbrige
- Antinio Radesca
- Juan Cabarello
- Dmitry Zagidulin
- Geun Hyung Kim
- Makki Elfaith
- Sachio Iwamoto
- Theirry Thevenet
- Victor Lu

## Notes

- Parallelized work items.
- How soon do we want 1 or more
- Fine to work in a google doc.
- Source of truth for a work item.
- Moving to git is an agreement/consensus mechanism.
- Faster to work in Google Docs.
- How soon can there be consensus on V1.
- Sachio : How flexible on the progress
- Andor :
  - Owners of use case will drive how flex.
  - https://github.com/decentralized-identity/trusted-ai-agents/issues/3
- I do think there’s a role for both
- developers are human, today, kind of ;)
- AI soon!
- I think if we align it to the governance will be great, basically answering those 3 questions:
- Goal/Problem: What is the Agent trying to achieve? (e.g., "Run a multi-step workflow across several APIs operating under different security boundaries, with intelligent failure handling.")
Estimated Value: Why is this important? (e.g., "Enhance workflow reliability by enabling adaptive recovery, reducing downtime in cross-system integrations by 20%.")
Required Autonomy (Simple Tag): Does the Agent suggest (Low), execute simple tasks (Medium), or plan/execute complex workflows (High)?
This is also more of the user story section if you will
- Suggestion : Give people that build use cases time to present!


Note: we might have two audiences.

## Action Items: 

- [ ] Develop a plan around timelines
- [ ] Give feedback and finish off issues Use case: Adaptive error handling in multi-step API workflows #3, Detail Governance Process for Accepting Use Cases #5 Bumblefudge/add-usecase-template #2
- [ ] What is the deliverable?

## Goals For Next Call : 

Set a clear course for work in the Working Item. 

# 📅 2025-10-13 Meeting Notes

## Agenda

| **Time**   | **Agenda Item**                                                                               | **Lead** | **Notes**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------- | --------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **5 min**  | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs   | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group’s JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min**  | Review of previous action items                                                               | Chairs   | Quick review of open items and updates from prior meetings.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **40 min** | **Main Topic:** Process for Managing and Registering Use Cases                                | Chairs   | Discussion on how the Working Group defines, tracks, and publishes use cases.<br>• Review prior emails beforehand.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **5 min**  | Review decisions and action items<br>Planning for next meeting                                | Chairs   | Summarize key decisions, confirm action owners, and discuss agenda for next session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        
## Notes

### Attendees :

  * Dimitry Zagiulin
  * Nicola Gallo
  * Sachio Iwamoto
  * Thierry Thevenet
  * Agne Caunt
  * Tom Jones
  * Alan Karp
  * Alex Bainbridge | WG 
  * Frederic Choudat
  * Geun-Hyung Kim
  * Iain Henderson
  * Savita Farooqui
  * Drummond Reed
  * Makki Elfatih
  * Sultan Mahmud
  * Kim Duffy
  * Juan Caberello 
    
### How Do We Govern Use Cases

* Use Case Template -- Propose A Template
* Alan Karp -- Setup An Issues Page. SOLID does an issue page.
  *  Cons : Group did not interact well with the use cases.
* Alex Bainsbridge:
  * https://dif.notion.site/HOSPITALITY-TRAVEL-SIG-242105321e1747f8bce776bf634a55b3
  * Pros and Cons : Not everyone can update it
* Prior Art from Ben:
  * https://wallet.storage/user-stories/connect-wallet  
  * https://wallet.storage/user-stories/share-vc
  * https://wallet.storage/user-stories/share-vc-undo
  * https://wallet.storage/user-stories/delete
* Updating and Commenting
  * Sachio : How can Alan's document be applied to different industries.
    * General vs. Specific
    * Mechanism Creations
    * Where can be the one pager?
    * General vs. Specific Categories 
* Tom :
  * Excption to building use cases toward industries.
  * Use Cases should test our ideas?
  * Person Oriented not Industry Oriented. By Human Focal Point.
* Dimitri :
  * Push back on industry specific use case.
  * How do we filter / carry them?
  * If a use case is narrow, hold off on them.
  * Care about genearlity.
  * Drummond +1 to Dmitry's ooint
* Alan :
  * Industry use cases useful for adoption.
  * Not too narrowly focuesed.
* Nicola :
  * Goal : Generate some design patterns.
* Makki :
  * Shouldn't expect industry can inform us.
  * How do we build an ecosystem of Trusted AI Agents. 
* Juan :
  * Propose : Consensus Mechanism
  * Rocketing : I'll contribute
  * Parallelized Activity
  * Write the next one
* Dimitry : Should multiple people be required.
* Alan : Anyone should be able to put a use case up.
* Makki : Use this call to short list the use case.
  * Next Call : Get a sample prepare
*  Use Cases:
*    Agentic AI securely mediates HULA agreements using biometric authentication to verify user identity, assurance and intent. This ensures non-repudiation and trust in digital interactions enabling autonomous agents to execute legally binding actions on behalf of users.
*    As a use case, consider an AI agent that runs a multi-step workflow across several APIs operating under different security boundaries. When one step fails, the agent doesn’t just roll back automatically, it analyzes the situation, checks for possible recovery options, and decides whether to retry, undo previous steps, or report the issue based on simple rules.
* Makki : To help with the governance of the use cases.
* Invitation is All You Need.
* Juan Quick sidebar (people can comment on this message in parallel to the main discussion): what should the template include?
1.) all acting/determinant parties (including agents, AuthZ servers, etc), enumerated and named/represented by a Letter/Number/etc.
2.) specific AuthZ/policy language/DSL reqs (i.e. actor C needs logs about what actors A and B did)

## Action Items: 

 - [ ] Template By Next Week That Would Accomodate The Use Case Provided By Nicola <- Nicola 
 - [ ] Governance Process for Use Case Management <- Makki
   - [ ] Shared Glossary / Definition

## Goals For Next Call : 

- [ ] Have 2 Use Cases To Discuss





