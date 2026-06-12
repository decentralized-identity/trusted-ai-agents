# Trusted AI Agents WG - Meeting Notes

[![hackmd-github-sync-badge](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw/badge)](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw)

## 📅 2026-06-08 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS update | Juan ||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born | Bumble+Damian ||

## 📅 2026-06-08 Minutes

- Updates
    - KYA-OS
        - Alan: 
    - Delegated Authority Reports Proliferating!
        - Reports Family Tree
            - s
        - Dmitri went first for ZCaps - Coworking every Thursday until we have more! 
    - Deb: Prototyping a Delegation-agnostic PEP/PDP
        - Tom: What's the role of intent here? what kind of intent?
        - Deb: stringing together GNAP AAuth and UCAN to compare what each container can do with a common intent identity
            - AAuth has a "governance server" idea ; i've been working on some of these ideas since 2007
        - Alan: Claudry Hepburn, for ex., has a RS PEP applied after agent's post-condition checks
        - Deb: I have this "decision-package" distinct: agent request > normZ > PDP > decision package > PEP > RS
        - Alan: Historically, intent was subject to an ontology problem
        - Tom: Confidential Compute Consortium isn't touching cross-org; very hardware-centric
            - (in chat): the trust problem can be looked at from the bottom up (like CC) or from the top down (multi-agent) - very different views
        - 
    - ITU
        - Juan: try to make intent machine-readable versus context snapshot. Need trust in others' runtimes. 

## 📅 2026-06-01 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Damian ||
| 5min |  KYA-OS update | Damian ||
| 10min | Demo of Flaxscrip/Mitchell two-agent explorations | Mitchel, Christian (DID Methods WG)||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born | Bumble+Damian ||

## 📅 2026-06-01 Minutes

- The group welcomed Adolfo, co-founder of the Trust Layer Foundation (building ARIA protocol)
- Annoucements
    - KYA-OS Task Force meeting brought forward 1 hour to 9am EST (ongoing)
    - Feedback received from Sachio, Alan, Tom & Agne on KYA-OS roadmap to date
    - Dyland is incorporating all edits in one go  
    - Please can others who wish to register their approval of the proposed V1 scope and/or feedback do so by giving a thumbs up on Juan's post (https://difdn.slack.com/archives/C0AK05AKHGV/p1778776535438769) or adding their feedback inline
- Damian to add a note on the KYA-OS slack channel reminding people to register their approval / feedback (done)
- Damian to invite feedback from H&T SIG chair, Creator Assertions chair (done)
- Mitchell demo'd the approach he is developing with Christian to a privacy preserving dual-agent architecture, including a boundary-making agent / expert model plus delegation to an LLM based agent with access to a user's personal info  
- The approach generates a knowledge graph based on trust tasks & verifiable relationship credentials, enabling 2 browsers to talk to each other without revealing any PII  
- Questions from the floor on multiple ledgers using one key (answer is linked to key rotation), how to express trust relationships (answer: using promise theory), how the agent's behaviour is compressed as an observation of the runtime & how to trust the harness (answer: the geometry enables trust to port between ecosystems)

## 📅 2026-05-25 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 10min | Announcements, routine business - KYA-OS update | Damian ||
| 10min | Demo of Flaxscrip/Mitchell two-agent explorations | Mitchel, Christian (DID Methods WG)||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born | Damian ||

## 📅 2026-05-25 Minutes

- Announcements
    - Erik Passoja: Led here by CAWG, recently posted a [response to a NIST](https://docs.google.com/document/d/1Mv0yYNkW_LU_uaaSs7VA1ep-0luRfl-NgvfFE0ORA2M/edit?usp=sharing) RFI that might be relevant here
- KYA-OS feedback on [proposed roadmap](https://difdn.slack.com/archives/C0AK05AKHGV/p1778776535438769)
    - Sachio's feedback [on Slack](https://difdn.slack.com/archives/C0AK05AKHGV/p1779652848654009): Cedar --> PaC, REL integration
    - Alan's feedback [on Slack](https://difdn.slack.com/archives/C0AK05AKHGV/p1779209517045449) - points out some subtle assumptions about secret/key management (custodial and/or inside of agents), the scope of reputation, and privacy
    - Tom's feedback and [threat model](https://docs.google.com/document/d/1rqNtqZ60yUF5EsE4-Nqfrih9Hbedyzcor9I1Wn19uHo/edit?tab=t.0) - unlinkability and the risk of "aggregation" of data that was decentralized/private at the time... but gets merged into a behavioral graph by leakage and "third-party sharing" at scale (huge risk to the privacy of principles/wards)
- Restarted KYA-OS prototyping efforts
    - most interest was around eCommerce use case
        - Alan: Shopping cart usecases are kinda simple and have lots of purchase-semantic specifics; something involving collaboration or data-sharing exposes more problems
    - Special Topic calls can start back up again if people want to prototype!
        - Alan: My [transitive usecase](https://www.alanhkarp.com/UseCases.pdf) is always a good one to think through or start with
            - Sachio: I definitely took inspo from Alan's use-case doc, and  "Composable attenuation" is definitely something I want to model; Anil (Rise11) was the one who thought a purchase/shopping would be a good place to start, and we drifted towards something like booking a flight because it had some complexity 
            - Sachio: for legal reasons hard for me to contribute code, just review for now
            - Grace: Aven (Steven) might be interested in helping to prototype on this, with or without KYAOS
- Policy and Governance
            - Alan: My work on "automated negotiation" (#20, 21, and 26 in https://alanhkarp.com/techreports.html)
    - [Tom's document on AI Constrained by Policy](https://docs.google.com/document/d/1uIBuaQw0mrx_brB3krQ7CgHUSCY60jTuV4xjnwHHtkY/edit?tab=t.0#heading=h.mfujiy6fu4iq)
    - Paul Knowles - the ["Legal" problem](https://medium.com/@paul_15561/vocabulary-before-standards-why-the-legal-community-must-move-first-on-autonomous-systems-b7ec705c6f66) is upstream of agentic governance 
        - Tom: Dazza Greenwood would say legal and policy aren't two distinct categories, code is a metaphor for law and vice versa...
        - Erik Passoja: consent + liability VC schemata proposed in CAWG... interested in comparing notes with how this group is thinking about intention and policy enforcement towards some day being able to INSURE these processes

## 📅 2026-05-18 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Bumblefudge ||
| 5min | KYA-OS v1 [roadmap - CFC](https://github.com/decentralized-identity/trusted-ai-agents/blob/main/agenda/agenda-kyaos-tf-2026.md#kya-osmcp--v1-scope) | Bumblefudge ||
| 10min | AI Policy Task Force Kickoff? | Tom & Bumblefudge | See Slack for Tom's Proposal Notes and [Deb's draft report](https://identity.foundation/governance-of-delegated-authority-report/) |
| 10min | Enterprise/runtime Identifier versus intent/distributed-transaction context | Tom | last-minute agenda proposal | 

## 📅 2026-05-18 Minutes

- Banter
    - EIC
        - DIDs in EBSI project
- Please review [roadmap for KYAOS]()
- Policy
    - Tom's identifier question from the chat: "i would like to discuss the identifier for the agent provided by some enterprise versus the identifier of the data context supplied by the user and the service selected by the user."
        - Subra: Yes plz, let's chat about that!
        - BF: Seems like you always need both?
        - Tom: The sticking point is always revocation - Need to distinguish transaction ID, not just agent ID
            - Tom: Not a fan of KYA-OS current version - needs Transaction Revocation
    - Cedar
        - Alan: Sidenote, at IIW i found out formal methods people contributed significantly to the design
    - BF: Who wants to prototype policy, whether in Cedar or REGO or whatever?
        - Wilmer: don't wait for everyone, any 2 people can meet up and start playing with it! doesn't take much with agentic codegen
        - Alan: in Deb's report, INTENT is an important input to any policy enforcement
            - Tom: How express? Seems a pretty thorny category
            - Alan: at AIIW, lots of people experimenting with LLMs modeling policy in natural language and translating (and formally verifying the product); these companies provide a custom, trained LM to do this policy work
            - Tom: should the LLM have less autonomy when authoring policy, or _help_ a user; here a helper LLM or mini-/assistant lang model ("SLM" as it were)
    - Subra: What is "intent" for you guys? intended outcome? 
        - BF: distributed
        - Alan: Agent Payment Protocol has a document called an "intent manifest" (easy to do with payments)
        - Subra: If "it's the intent that matters", we need some semantics there...
        - Alan: "I want you to book a flight that gets me to Boston for this conference" is an example... 
            - slippage between "book me a flight" and "get me to the right city the night before the wedding/conference/etc" (and replan if that date changes)
        - Alan: Deb's threat modeling doc is good at getting us to think through these issues
    - Mitchell: +1 to Tom's approach to two-models with diff goals, I think that approach will catch on quickly
    - Damian: Can a universal/baseline policy affordance be worth defining, or is it too vertical-specific?
        - Tom: My doc proposes that baseline already, I think the CONDITIONS are domain-specific but the CONTAINER/general logic is universal
        - Alan: Ontology problem? Tom: Meh, that's just versioning and DSLs
- Wilmer: Wanna take lead on prototyping, will ping you (BF) on slack

## 📅 2026-05-11 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Bumblefudge ||
| 5min | Deb's video: Delegation<>Guardianship? DIF Youtube? | Bumblefudge ||
| 20min | AI Policy Task Force Kickoff? | Tom & Bumblefudge | See Slack for Tom's Proposal Notes and [Deb's draft report](https://identity.foundation/governance-of-delegated-authority-report/) |

## 📅 2026-05-11 Minutes

- Announcements
    - IAM conf - Damian will be moderating a panel with an Okta Product Owner,  a security architect from a bank, CIAM lead from pharma on agentic security 
    - EIC (Berlin, 19-22 May)- Grace is speaking on content creator assertions, Juan is organising DIF drinks in Berlin during the conference 
- Deb's [video](https://www.youtube.com/watch?v=u-uWl_s0PPM) and how to frame it for a general audience
    - Alan: Delegation !== Guardianship
    - Deb: Intention was more use-case focused, to show how delegation works in this specific medical user story how to wrap a legal/medical situation in software
    - Deb: [Threat model](https://docs.google.com/document/d/1VcsHZ7jOs3jzYOdD_BsVMw0D2Tri-Tb7sQsrbup5JoI/edit?tab=t.0) posted - please feed back 
    - Juan: shared Tom's doc, [AI Constrained by Policy](https://docs.google.com/document/d/1uIBuaQw0mrx_brB3krQ7CgHUSCY60jTuV4xjnwHHtkY/edit?tab=t.0#heading=h.mfujiy6fu4iq). This contains a number of prospective work items, please review and think about if you'd like to collaborate 
    - Mitchell Travers also features a split between generator / solver in his work - the solver is the deterministic part that sets the boundaries for what of the generated information is passed through. 
    - Mitchell also flagged MyTerms - a Cedar flavour of a bilateral agreement between 2 agents. User privacy can be protected via policy or cryptography. He will present the approach to the group 
    - Geun-Hyung Kim - new member said hello 

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
