# Trusted AI Agents WG - Meeting Notes

[![hackmd-github-sync-badge](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw/badge)](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw)

## 📅 2026-05-11 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Bumblefudge ||
| 5min | Deb's video: Delegation<>Guardianship? DIF Youtube? | Bumblefudge ||
| 20min | AI Policy Task Force Kickoff? | Tom & Bumblefudge | See Slack for Tom's Proposal Notes and [Deb's draft report](https://identity.foundation/governance-of-delegated-authority-report/) |

## 2026-05-08 Special Meeting - Onboarding for Eastern Hemisphere Time Zones Members

- Intros
    - Anil (Rise11): US Healthcare, clinical trials (data governance, graph DBs → LLM/agentic interactions) - Compliance certs (geographical cloud processing restrictions as well as HIPPA) at risk of agentic mayhem
        * Transition from APIs and third-party integrations/platforms to MCP/Agentic land - urgent data governance issues
    - Goals: governance triage asap
Gareth Fakhry (NZ) - lawyer and creative producer, blockchain law and identity in partic; Agentic <> ZKP convergence - cross-system AuthZ/AuthN requires incorporating lawful status and fiduciary lifecycle/evaluation into the technical system ( https://siltcore.org/ ); DIDs/digital-identity is a semantic layer that can be useful “outside” the system
GaoWei: founded ANP (agent network protocol - allow all agents to communication and coordinate - open nonprofit) and 
Sean (ANP) - went to IIW/AIIW 
Tour of website, Slack, WG’s githubs
How to prototype - post user story, discuss, [optional - present user story and prototyping approach on a call], prototype, share link, [optional - present/demo prototype on a call] 


## 📅 2026-05-04 Agenda - SPECIAL TIME/LONGER MEETING - 9.30am**-10.30am** PST

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Bumblefudge ||
| 25min | Post-IIW decompression | WG members ||
| 30min | ITU and SIA read-out (for Hot Takes podcast) | Damian ||

## 📅 2026-05-04 Meeting Notes

- Intros and announcements
    - Travis (lyfe.ninja)
    - Aaron - gTLD and eCommerce background - registry of agents for accountability
        - ARIA
    - Geun-Hyung (SKorea) - how to make trustworthiness for agentic ecosystems (national initiative here)
        - See you Friday at 6pm 
    - Mitchell Traverse - Agent Privacy / dual-agent architecture ; have been working on a dapp with Christian, traces of the convo on Slack, adding ZK features to archon;
        - there's a large body of work on the subject, lots of transparency and ZKP aspects
- IIW Favorites
    - Alan: Claudry Hepburn - set up a agent who did crowd work, gave her own read-out at the end
    - Alan: Agentic Identity is useless, prove me wrong session: Only Andrew held out and conceded nothing
    - Alan: Only heard the word "blockchain" twice; less than half of sessions (in IIW proper) had anything agentic/LLM in the titles
    - Aaron: First IIW ever, loved the format, looking forward to the notes; UTAH/SETI stuff was a big standout for me; saw KYA-OS
    - Aaron: Verana (general-purpose blockchain-based trust registry) from south america
    - Aaron: [ARIA](https://Aria.bar)
    - Dmitri: 4th day, like a mini-IIW, lots of overlap
    - Sidebar: Expert Systems versus LLMs versus non-LLM AIs
        - "memory" as emergent property of LLMs; 
        - Subra: Rulebased systems get so complex as you layer on enough rules that they become less knowable/reasonable, they can almost approach nondeterminism at 
- ITU Readout from Damian and Ward Duchamps (Thales)
    - Damian: themes
        - agents can't solve new problems created by agents
        - new protocols are hard, but agents change autonomy so much that OAuth won't work ever
        - workloads are composite/multi-dimension; SPIFFEE not designed for cross-domain trust
        - DNS panel
        - OAuth session-based, coarse authZ (hard to constrain enough)
        - Legal perspective (from a GDPR veteran): legal consequences staggering, need more lawyers in the loop if [EU] business is gonna be even able to much less willing to adopt this stuff
            - code as law (governance in protocol layer) 
    - Ward Duchamps: HUman intent is the new trust anchor
        - similar takeaways and highlights
            - need more lawyers fersure 
            - one researcher projected 900 BILLION agents by 2030
        - slides: how applicable/salvageable is OAuth
            - ![image](https://hackmd.io/_uploads/Hk3BSLURWl.png)
            - "Power of attorney"/foundation of dist. txn. needs some kind of additional trust mechanisms (distributed ledger for timestamps? confidential vaults?)
                - OOB human strongly-authN'd to sign the initial intent doc
        - Conclusions
            - user defines what, agent chooses how
            - time delay b/w intent and execution
            - "agent defines data access paths"
        - Q&A
            - Subra: "human" "intent" is doubly vague, and "power of attorney" kicks it down the road a little
                - Ward: We trained an agent to gather "intent" from humans, teasing it out via NL; we still try to translate that at inception into structured data for the intent; BF: Confirmation step? Ward: Reuse UX pattern of MFA, so confirmation can be used to "sign" the intent
            - Alan: How express capabilities and intents? Ward: we're looking at VCs (VP pass from agent to agent); also looking at recent JWT formats cuz they're so cheap/easy to compute
                - Alan: UCan or ZCap may be useful
                - Ward: early days, we're assuming there will be a lot of design into that [DSL?]
            - Matthew Rappard: Promise theory might be a good ontological basis for intents; agents can only promise and that works well for this kind of trust problem
            - Power of attorney revocable at any time: does that apply here as well? I think it should; in a medical case, for example, also good to maybe blind permissions even to person/actor checking them
            - Alan: A2A negotiation needed? Ward: I think so, there will probably be more-trusted agents delegating to less-trusted agents
            - Matthew Rappard: we found experimenting with agents that logging A2A interactions that there were huge legal risks (analogy: my lawyer talking to a specialist lawyer about my case, latter can be liable)
                - Ward: Defined intent versus derived intent; historical interactions of a given agent can be measured against the fvormer
            - BF: Distributed transactions - how unify the runtime? don't agents run on diff OSs, diff environments, diff org boundaries... how be sure they read/understand the intent (however constant/authenticate) the same way everywhere?
                - Nicola: But for me, an agent is still, fundamentally a [distributed] workload, so we just need better transports and async messaging once we leave HTTP behind...; moving beyond the SAGA pattern, we have to rethink the _execution model_ (and secure it) without as much focus on identity; i think we need more delegation and less identity
                - Ward: Intent > identity, which is basically a "nice have" ; anchor to intent, not identity
                - Nicola: DID and SPIFEE will eventually be bridged; 
                - Ward: Are you implicitly differentiating ephemeral agents from [relatively] long-lived, persistent, or memory-using ones? context identifier rather than an agent identifier?
                - Nicola: Sure, but you can't assign permissions to a context
                - Ward: we want to bring this to the ITU; working with Google's office of CTO to prototype this
                - Juan: let's stay in touch on how permission is expressed
                - Ward: agree, we need to converge on a solution through industry collaboration 

## 📅 2026-04-27  Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Logistics and task force updates | Bumblefudge ||
| 5min | Next Week's Presi: ITU Agentic Readout for the Hot Takes podcast | Damian ||
| 5min | Next Week - IIW decompression | Bumblefudge ||

## 📅 2026-04-27 Meeting Notes

- The WG welcomed new DIF member Aaron Grego (president, ARIA AI Agent identity protocol @ Trust Layer Foundation) 
- BF - Longer meeting next week, to do "read outs" about ITU+SIA (Damian) and IIW (everyone else); the former intended for the DIF Hot Takes podcast
- Victor - Recap of Supply Chain security <> Agentic DID rabbithole I've been going down, which I mentioned on the MCP-i call last week
  - [SPDX profile](https://spdx.dev/spdx-3-1-ontology-and-schema-available-for-review/) and [demo](https://spdx.github.io/spdx-spec/v3.1-RC1/)
    - [business processes](https://spdx.github.io/spdx-spec/v3.1-RC1/model/Operations/Operations/)
    - [hardware](https://spdx.github.io/spdx-spec/v3.1-RC1/model/Hardware/Hardware/) - piloted by german car manufacturers
    - AI meeting not up to date
    - [Slack](https://join.slack.com/t/spdx/shared_invite/zt-2fa9pqty9-AcobGadsN_TN1K~sSkUG4w)
    - Threat Control mtg happening... now! Mitre never got around to defining "threat" in its ontologies...
  - [IETF SCITT](https://datatracker.ietf.org/group/scitt/about/)
  - [ODRL demo](https://odrl.dev.codata.org/demo)
    - uses DIDs and wallets for open-data provenance.

## 📅 2026-04-20 Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Logistics and task force updates | Bumblefudge ||
| 5min | Intro New Chair | Alan? ||
| 5min | EU/Asia calls? | Bumblefudge ||

## ??? @dmitrizagudulin

- [Deb's amazing illustrative demo of a medical power-of-attorney delegation user story (YouTube)](https://www.youtube.com/watch?v=u-uWl_s0PPM)

## 📅 2026-03-02 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Logistics and task force updates | Dmitri ||
| 5min | Governance and policy task force? | Alan? ||

# 📅 2026-02-23 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Logistics and task force updates | Dmitri ||
| 10min | MCP-i for dummies? | Alex ||
| 5min | Governance and policy task force? | Alan? ||

## Minutes

- Dima: Updates from Delegated Authority TF-group invited to think about use-case applicability informally or collectively, we'll start doing that on Thursday
  - Alan: Finalizing draft tomorrow
- Alex K: MCP-i presi (slides)
  - Ideally evolves into a general Protocol layer, not just a single platform or product
  - extensibility; subgroup here could make extensions that will get used
  - Nicola's focus on confused deputy has already been helpful iterating on this already
  - looking forward to seeing how diff subgroups and usecase modeling can be applied
- Other topics: how to get policy and governance off the ground? any champions?
  - Debbie: I am more interested in evaluating protocols for the time being but I could try proposing an initial outline for an overview report like I did last time? 
    - the crowd goes wild

# 📅 2026-02-16 Meeting Notes

Canceled for US holidays

# 📅 2026-02-09 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Logistics and task force updates | Dmitri ||
| 5min | Show-and-tell: DIF has a (tiny) MCP-i server :salute: | Juan, Alex ||
| 5min | Tom's [use case](https://github.com/decentralized-identity/trusted-ai-agents/pull/32) and corresponding threat modeling [document](https://docs.google.com/document/d/1I8hJH8QdVps4ISqnfVlLsBecQ28KfXonIApx4Avot_M/edit?usp=sharing)| Tom, BF ||

## Minutes

- Intros and re-intros
  - Christian Saucier - Coming over from DID Methods WG (where I represented the [MDIP did method](https://docs.selfid.com/mdip)) - led here by my agents; clawbot proves DIDs are urgently needed
- Other groups
  - Delegated Authorization updates: google doc needs another pass, next week check it in and start workingon bigger PRs?
    - requirements for any new specs?
    - Dima: gap analysis and review of existing AuthZ specs/languages? Alan: Maybe that's next pass/step for the report, not much in there prior art wise
      - Dima: I have some notes from a prior project (doesn't cover policy languages, just token formats and authZ protocols)
    - Alan: Where does Nico's ZTA fit in? We're still debating in sidechannel about reconciling the PIC approach (policy enforcement across a distributed txn) and the Capability approach
      - Dima: Is this just caveats? Alan: Yes, but Nico is talking about originator imposing conditions across the whole chain- originator expressing something that follows whole chain
  - Governance and Policy TF? Whom lead? Call for lead? Alan: Upstream of policy languages or tokens/AuthZ context per se; Sachio: I'm interested, but uncomfortable leading
  - Prototyping TF
    - BF: not much progress, but hopefully soon we spin up meetings specifically for MCP-i; discussions in the MCP-i discord for now (not IP-protected yet)
  - MCP-i TF
    - Alex: meetings to iterate draft spec and collab on extensions (e.g. additional DID methods)
    - Dima: 10min presi to get the WG up to speed? Two weeks from today?
- Action Items
  - [ ] Everyone - try to close marginalia and comments to check into github end of week?
  - [ ] BF will make progress on the WG's toy MCP/MCP-i server

# 📅 2026-02-02 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Logistics | Dmitri ||
| 10min | Kickoff for Delegation Report, logistics | Dmitri | |
| 5min | Report-outs from other task forces | Juan, Alex | will install on server; MCP-i donation ongoing |
| 10min | Any more task forces? | Dmitri | Policy engines & governance of interest to lots of folks |

## Minutes

- alan: i think we have at least two usecases already that really require some governance thinking: shopping for a tween and enterprise purchasing
  - sachio: how a registry tracks and allocates and gates skills and authZ for a given agent in a given use-case, that's an interesting and novel form of governance to explore new policy mechanisms for
  + deb: my experience with healthcare data, NIST, etc makes me think human governance and tech policy can never interface simply, you need a lot of complexity and dynamic interfaces ; having built out a gateway and PDT/PDP, policy and governance are a huge part of the requirements, it's very complex; how do you automate policy in a dynamic way?
- Action Items
  + [ ] alex and juan will meet about prototyping and donation/spec work item
  + [ ] read report before Thursday's meeting, those thinking about delegation!
  + [ ] share links and thoughts on governance in slack channel, discuss more next week?

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

# 📅 2026-01-19 Meeting Notes

## Agenda

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| **5 min** | Start recording<br>Welcome & antitrust notice<br>Introduction of new members<br>Agenda review | Chairs | **Antitrust Policy Notice:**<br>Attendees are reminded to adhere to the meeting agenda and not participate in activities prohibited under antitrust and competition laws.<br><br>Only members of the **Decentralized Identity Foundation (DIF)** who have signed the necessary agreements are permitted to participate in this activity beyond an observer role.<br><br>To join DIF and sign the charter, please visit: [https://identity.foundation/join/](https://identity.foundation/join/)<br><br>**Code of Conduct:** [https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md](https://github.com/decentralized-identity/org/blob/master/code-of-conduct.md)<br><br>**Licensing Policy Reminder:**<br>In addition to the licensing terms of this Working Group's JDF charter, any Working Group Participant who makes a contribution to a Draft Deliverable shall have a maximum of **45 days** from the date of that contribution to exclude any Essential Claims pertaining to that contribution. |
| **5 min** | Review of previous action items | Chairs | Quick review of open items and updates from prior meetings. |
| **20 min** | **Main Topic:** Review current status and define next steps | Chairs | Take stock of where we are with agentic identifiers and agentic identity work. Decide on the next steps forward. |
| **5 min** | Review decisions and action items<br>Planning for next meeting | Chairs | Summarize key decisions, confirm action owners, and discuss agenda for next session. |

## Attendees

- Nicola Gallo
- Bumblefudge
- Alan Karp
- Debb
- Douglas Rice
- Geun Hyung Kim
- Sachio Iwamoto

## Notes

- Google doc already up and being collaborated on
- Delegation report meetings waiting on Dmitri but work in the gdoc in the meantime 
- One or more prototyping work streams to start soon (BF will provision)

## Action Items

- [ ] Dmitri send doodle for folks to work on the delegation work stream
- [ ] Delegation Report: Everyone Work in the google doc for now
- [ ] Use Cases - review pull #30 and iterate/update any other use-cases to bring them up to speed/shape
- [ ] BF to get a VPS for the prototyping efforts

# 📅 2026-01-12 Meeting Notes
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





