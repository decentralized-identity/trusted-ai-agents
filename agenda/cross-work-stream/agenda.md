# Trusted AI Agents WG - Meeting Notes

[![hackmd-github-sync-badge](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw/badge)](https://hackmd.io/I2BRY1EOSH-BzZ8a2SQvHw)

## 📅 2026-09-14 Agenda - Longer Session (ITU AI-for-Good Summit Hot Takes Before w/Damian and Ward Churchill (Thales))

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 30min | ITU AI for Good Summit "Hot Takes" (Podcast) recording | Damian ||
| 5min | Announcements, routine business | Juan |
| 5min | KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| ?min | Demo Update? (see last week's minutes) | Erik Passoja |

## 📅 2026-09-07 Agenda - US Holiday! 

async updates on Slack!

## 📅 2026-08-31 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min | KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| ?min | Demo Update? (see last week's minutes) | Erik Passoja |

## 📅 2026-08-31 Minutes

- Delegated Authority updates
    - https://identity.foundation/delegated-authority-evaluations/ live
        - [X] BF will fix TOC and relink Alan's affil SitePassword (link to [github](https://github.com/alanhkarp/SitePassword/))
    - VC chapter
    - Sachio's WIMSE/OIDC federation chapter
- KYA-OS - builder's registry, MCP update,,,
- Other Announcements and Topics
    - Alan: Working on a different approach in an essay called "Assigning Responsibility" to work through some framing disagreements that came out of editing the report
    - Identity Salon (H Flanagan) - Delegation focus this issue of the newsletter and this week's [event](https://luma.com/kkhsik9z)!
    - Alan: lots of podcasts bemoaning the Huggingface Apocalypse these days

## 📅 2026-08-24 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min | KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| ?min | Product Presi (see last week's minutes) | Erik Passoja |

## 📅 2026-08-24 Minutes

- Intros
    - Alan: Huggingface attack éxposé from NYT on Slack - 
        - Tom: Prompts didn't tell the model to show restraint or where to look-- it just found vulns that would've impressed most cybersec experts; the models find weaknesses quite well
        - Alan: At stanford agentic security conf, "stop on fail"
        - Alan: Zeynep Tayfecki: agents fail differently than humans do
- TF updates
    - Delegated Authority - editing, v1 soon
    - KYA-OS
        - SemVer
        - BF: Going to MCPCon/AGNTCON
        - Grace: Repping KYAOS at KuppCole Agentic and nonhuman id conference 
- Erik's Presi - different kinds of trust (CAWG Spec chapt 9)
    - backstory: likeness rights is personal for me
    - deepfake scams (post-Turing Test reality :grimacing: ); insurance fraud (adversarial AI can't detect, will never reliably enough detect; watermark debates)
    - legislative backdrop: laws specifying outcomes but no certain way to deliver
        - ![image](https://hackmd.io/_uploads/Hka-IxcDfe.png)
    - Eric: "the new sheriff in town is going to be the ACTUARY"
    - Q&A
        - redteam me!

## 📅 2026-08-17 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min | KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| ?min | Update on NIST responses? (see last week's minutes) | Erik Passoja |

## 📅 2026-08-17 Minutes

- KYA-OS updates
    - builder registry
    - SEP and extension registry, navigating AAIF
    - Version 1.1/1.2 
        - DEFCON demo
- Delegated Authority TF
    - Editorial update
    - Big decision: Reworking the scorecard about "byzantine deputy" vulnerability; degree of authentication-based/identity-bindedness hard to find language for but crucial
    - Janssen "moving towards capabilities" document --> 
        - Erik P: I just wrote [something analogous](https://www.researchgate.net/publication/412302275_Self-Sovereign_Identity_and_Governed_Action_The_PersonAsset_Distinction_and_an_Arithmetic_Authorization_Layer) - combining more kinds of provenance and just-in-time evaluation over authentication/identifier-based trust
- Update on open-letter 
    - Tom: Got feedback from NIST that the narrow scope and omissions were deliberate - NIST is focused only on closed-weight frontier models, they are keeping open-weight out of scope, and B2B/enterprise only for the time being
    - Erik P: terrifying that they are not thinking about many other kinds of risk 
- Upcoming Confs
    - MCPCon/AGNTCon AMS (MidSept)
    - KC Munich Agentic Trust (MidOct)
        - KC is open to guest blog posts for BOTH TFs --> free press! get on podcasts!
        - sent questions for Grace's interview, can discuss at tomorrow's KYA-OS

## 📅 2026-08-10 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||

- Updates from the TFs
    - KYA-OS <> MCP new major version
    - Delegated Authority report
        - editing review sections now (zcap/ucan last week, oauth/aauth/cedar this week, VC next?)
        - ZCap meetings now on the calendar (CCG-hosted)
        - timeline: sections of the report stay in google doc until they're in github
            - Grace: GDC (2ish Sept) - will the whole report be ready for [early?] feedback 
- Announcements:
            - Grace: Agentic ID KuppCole mini-congress in Munich (5ish Oct) - will the whole report be cleanly v1 published on spec-up by then? 
        - Erik interested in responding - test boundaries for measurement
        - 
    - Tom (in chat): i read [NIST AI 200-2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.200-2.ipd.pdf) (an RFI from a few days ago with 60day response time) with some concern that it does not consider open-weight models or policy generated by the user - i already sent in [my personal response](https://docs.google.com/document/d/1TNf3wlHSYg9-hzVbzdtcz8z3edlp_A8SMFKNlmhOoxE/edit?tab=t.0#heading=h.w17yrrmau8wb) but i think they should hear from us too as an org -
        - Erik will start a TAAWG response, we can all join in via [google doc blotter]( https://docs.google.com/document/d/1TNf3wlHSYg9-hzVbzdtcz8z3edlp_A8SMFKNlmhOoxE/edit?tab=t.0#heading=h.w17yrrmau8wb) ; will also follow up with Tom on his already-submitted one
- Alan: (minutes left on the clock) let's talk about my "resource reference" rule of thumb Thursday on the DA call!


## 📅 2026-08-03 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||

## 📅 2026-08-03 Minutes

- KYA-OS task force activities last week: the TF discussed updates to the MCP spec, discussions with AAIF / Advanced AI Society & timings of KYA-OS MCP extensions 
- Implications of the new MCP release for DIF: the identity pieces were unspecified in the original version which people have been using for a year now. Some of the pieces which were missing / dependent on external custom code (such as KYA-OS) are now becoming standard APIs, e.g. Authentication extensions are being added to the MCP spec 
- This is good news for KYA-OS, as the problems which KYA-OS is designed to addresss are being highlighted to MCP users / normalised 
    - Grace: Would be great to publish a blog post highlighting the fact that Vouched / KYA-OS TF correctly guessed that this would be the direction MCP would need to go in  
    - Juan: may be best to finish the registration piece before we do so 
- Draft of the Decentralized Authority extension (drafted by KYA-oS TF) is WIP 
    - DA Report TF - people are working on the different parts of the doc in parallel, most sections have been read by at least 3 people. The doc is pinned in the slack channel. 
    - Alan: Debs' section on A Auth is the best available intro to this topic
    - Grace: Is this a book? Can we print out drafts at GDC?
        - Alan: It would take a lot of work to turn that into a formal piece of literature
        - Alan: Being more comprehensive in the "other systems not analyzed in detail" would take a lot of research and legwork, including reviewing all other delegation specs (Macaroons, Biscuits etc) & writing a para on each (or at least why we decided not to cover it)
            - Good first issue! Jump into the google doc pinned in the task force channel
        - BF: other work too-- not sure it can be done before GDC
            - Grace: Munich KuppingerCole [agentic conf](https://www.kuppingercole.com/events/nhiid2026)?
- Juan: CCG is working on the ZCAP spec plus other interrelated specs inc capability-based storage; hard to jump in because multiple work items are being worked on together
    - recommended starting points: [Wallet.storage overview](https://wallet.storage/#example) or the more technical [CCG W-A-S spec](https://wallet.storage/spec#goals-and-requirements)
- Last call for other business?
    - Alan: Delegation often thought of as delegation "to keys", particularly long-lived (rotating?) keys, but that makes for messy chains and hard-to-verify chains, so how delegate to short-lived keys but keep the audit logs clear and stable? A running thought I'm thinking of as relevant to both TFs

## 📅 2026-07-27 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| Remaining Time | Read-out from Agentic BoFs/I-Ds at IETF Vienna | Bumble (and Grace?) ||

## 📅 2026-07-27 Minutes

- [registration of agents like companies](https://www.linkedin.com/pulse/mandatory-agent-registration-agents-who-transact-bourn-collier-rj5mc/?trackingId=nzPmdh6cR9q%2FHlgaDwSzIQ%3D%3D)
    - Juan - A lot of people are rushing to be the authoritative registry, inc NANDA. A lot depends on what context you give it, which skills you let it use etc.
        - Alan: App store great example of a registry that collapses 50 trust decisions into 1. The danger is control - Apple can put you out of business by removing you from the registry. Alan: what if UL or EFF published policies endusers could opt into (for filtering out the more-dangerous 90% of their options)
    - Erik - The new sheriff is gonna be the actuary crunching all those receipts
        - damian: public? erik: nah, e2e txn reqs SOMEONE see e2e receipts (ex of SAG-AFTA: public identifiers versus authNd identities)
    - Alan - Using the evidence to seek redress is going to be challenging
    - WG updates: KYA-OS are talking to the advanced AI society about a prototype that maps the AAIS requirements to the KYA-OS spec.
    - KYA-OS group is also considering putting forward an SEP (MCP Extension Protocol) once the new MCP spec goes live
    - DA task force is trying to edit together the different chapters (Alan: the new AAuth chapter is good!)
        - sidebar on AAuth - stick a policy EP on a proxy and call it a person server - Alan: 
        - Alan: Sarah Cepetti (sp?) - Carapace - what happens when two people run those harnesses that cooperate? 
        - Erik: Are OpenAi and Anthropic creating moral frameworks instead of ethical protocols?
- Damian: Data Transfer Initiative has a [registry](https://dt-reg.org/registry/?vertical=Documents) who might come to a future KYA-OS meeting 
- IETF update: Grace & Juan went to many side meetings e.g. DAWN?, many of which got majorly heckled. Universal objection to agentic proposals was "scope is not sufficiently narrow". The one that seemed to have the best buy in was Agent Protocol (proposed as a coordination point for all IETF WGs that need extension points for agents). WebBot Auth had their 3rd WG meeting. Agentic-aware networking was another topic (Dirk's BoF sidemeeting on Thursday).
- Grace: Agent Protocol got [soft] approved (still needs to iterate charter but might happen over list without an interim). barely touched discovery and "session layer"/"context container" across IETF layers, defers to WIMSE for ephemeral and OAuth for long-lived identifiers. Seem to have won the prize for "who gets to write the framework"
    - good i-d [IETF-wide overview](https://github.com/nomoticai/ietf-agent-landscape/blob/main/agent-standards-landscape.md) ; see also [this overview from the WIMSE wg](https://www.ietf.org/archive/id/draft-klrc-aiagent-auth-03.html)
    - the dissenters: why are DIDs and gateways out of scope?
    - extremely hyperscaler-shaped framework; IETF does engineering, not business strategy, after all
- closing meditations: trust at scale? Alan: non-technical trust is v squishy and contextual, 

## 📅 2026-07-20 Agenda 

| Time | Agenda Item | Lead | Notes Alan|
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| Remaining Time | Read-out from ITU AI-for-Good | Damian ||

## 📅 2026-07-20 Minutes

Tom - has anyone defined what an agent is? 
Alan - a piece of software dependent on an LLM. Given a task by a user. It can then autonomously decide how to carry out that task. 
Tom - I don't see why an agent needs an identity. Alan - I agree.
Erik - we should def have an identity, so it can be tied to a responsible party. 
Alan - the agent acts on the legal person's behalf. Tracking the agent only needs an identifier visible to the operator.
Erik - I would use the word semi autonomous. 
Alan - I wrote a paper called "AI Agent identity is useless". https://docs.google.com/document/d/1N4Y2adf4LQs3tZGJm1hJ2VLqikRptr0Rd6dPCUGNJSA/edit?tab=t.8jy77r4bo2dg ALso https://www.linkedin.com/feed/update/urn:li:activity:7391222507598643202/
https://www.linkedin.com/feed/update/urn:li:activity:7394426845611540480/ (Alan's definition of the 4 properties of identity)
Because we use identity for 2 things: establish trust and track responsibility. 
Dmitri - the id is useful for accountability
Erik - disagree. I think the agent needs an identity not an identifier. Agents need Provenance, consent, authorisation, liability. For these to be true, we need a human to be resposible. 
Tom - I run my own agent on my own computer. From time to time it needs to do something offsite. If you are the owner of the agent that starts the process, you may not be the owner of the agent that finishes the process. We need something more abstract
Alan - if I have a program on my machine that uses your web service, isn't that analagous? 
Erik - the big issue with identity is, how easy is it to redact information / track someone using their identity? 
Alan - agree, however we're looking from the other side, assigning responsibility. 
Alan - put together a chapter on different capability systems. Would be nice to have a sentence or two on each of them. E.g. mararoons and biscuits are both bearer tokens, we decided to discount them. Bearer token - whoever holds it can use it, v hard to keep them secret on the open internet, therefore we wanted proof of posession, e.g. zcaps - only someone with the private key can use the capability. 
Alan - KYA-OS has addressed the problems with using VCs for this. I believe they are doing a decent job. 
Tom - what did method are people using with KYA-OS? I didn't find the ones in the spec acceptable. Are they in production? 
Damian - suggested that Dylan joins an upcoming WG call to answer this. 


## 📅 2026-07-13 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| 10min | Integrating AAuth permissioning into my running prototype for auditable agentic delegations | Deb Bucci || 
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born, maybe a terminology list? | Bumble ||

## 📅 2026-07-13 Minutes

Announcements
- KYA-OS meeting one hour later starting this week/tomorrow! See DIF Calendar

Intros - Cooper Halpern, intern for digital governance institute, joining to get perspective on DIF and how the field is working 
Updates - not too much new on kya-os, mostly discussion about marketing & outreach. Also meeting is moving back to the original time (1 hour later)
DA - please ship without Sachio's section, he is still waiting for clearance to contribute
Alan - did a search for certificate-based capability systems. Won't need a full chapter on each, more like 2-3 sentences. 
Juan - has been hearing about cookie based sandboxing and context limiting approaches, as a stopgap. 
Alan - this approach works fine for your agent, but not if an outside agent needs to communicate with you. 
Juan - agree, in a distributed MAS you need better approaches to delegation.
Mitchell - has implemented a 'cookie jar' solution for a federated research wiki [based on ward c's fedwiki](https://github.com/WardCunningham/Smallest-Federated-Wiki) (using cookies to set boundaries between read and write for agents). Delegation chain becomes vulnerable once you leave your environment. 
    - "quite myterms-y"
Next week is IETF in Vienna - Juan can provide a link dump of anything that might be useful after the event. 
Debb's presentation. What she has been working on for the past year, much of which is informed by the WG's discussions. Idea is to capture intent, looking at protocols that could be used. Components include a Mission Builder, a Stage Gate Engine and a Governance PDP (Deny / Restrict / Allow), Capability Registry. 
Debb shared an example of what the data output looks like. 
The envelope is protocol agnostic and can accept various inputs. 
She is meeting the AAuth group next week. Also just spoke to Dick Hardt. They don't want anything to do with attenuation. 
Person Server (~== wallet?) & Mission will likely use LLM (??). 
Alan - comment on the use of "Governance PDP" as terminology. (Governance is in content/human/legal layer in most systems) ; Deb: but isn't this is a technical decision with governance consequences? is the policy static?W
Alan - uses the term "Validator" for the PDP. 
Juan & Alan - agree that governance is the act of creating policy, PEP is where it gets evaluated at runtime. 
Juan - how to make this deterministic enough to qualify as PEP and PDPs? 
- Debb - the AAuth discussion assumes any person server would have access to a governance decision. should i call that policy?
    - Alan - this is what I've been calling the verifier. Governance is more the creation of the policy. 
    - conventionally, there's a PAP (policy access point) for access policy at runtime
Juan - AAuth refers to a 'person server' vs a personal assistant. They are trying to give it its own PAP, enabling it too to evaluate non-deterministic inputs at runtime. I.e. the agent brings its policy, the server brings its policy and they need to evaluate each other.
Juan - has recently been thinking about DIDComm and its competitors. Original assumption was that everyone controls a cloud agent working on their behalf - now IETF is assuming this will be a reality soon. 
Alan - suggested to add KYA-OS (this was Debb's ask, to flag DIF work items that should be on her chart). AAuth can't do attenuation, so This won't work once I need to give an EXTERNAL agent my query. 
Debb - if a mission is defined well enough, it can drive some of the oversight. 
Nicola - if everyone has their own person server, they also need their own identity. If you keep chaining identity, what problem are they solving? There is already OAuth token exchange. They are inventing a solution that will chain identity, what's different from OAuth? Someone still needs to know everyone on earth, non?
Alan - the big change from OAuth is not needing client registration. 
Nicola - chaining identity but for what? you're chaining identifiERS, and what does that even get you? Feels like patches that don't work around the lack of consistency (in [CAP Theorem sense](https://en.wikipedia.org/wiki/CAP_theorem)), eventual consistency is more realistic for an actually distributed system
    Deb: not chaining identities so much as chaining authorizations/receipts; 
BF (in chat): maybe the Person Server and Attenuation/delegation are out of scope for the same reason-- they want all that to happen at a HIGHER layer, which this layer doesn't get audit/log access to?
like, if PS is opaque to this authZ language, and attenuation/negotiations happen there... it's out of scope to be out of the logs/SLAs/liabilities...
Tom (in chat): Missions are seldom static. They often need to request additional permissions during execution.
Juan - we need to understand WHY the AAuth team thinks it will work / they don't need attenuation. 
Tom - "person server" is a non sequitur. 
Juan - the AAuth spec calls the person server's negotiation with the other server "governace". 
Debb - I'm focused on the 'are you allowed to do this' piece. 
Alan - the person server is a "power box" that has all your permissions (i.e. its very powerful). When you ask it to do something, it's bounded by the permissions in your power box. The agent can ask for more permissions from the power box / person server, based on the mission. The agent has a subset of your permissions - where attenuation comes in. 
Juan - summarising, this is great context for the DA report & understanding Debb's chapter. IETF likes 'thin' layers.

## 📅 2026-07-06 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| 10min | Discuss agentic possibilities for the new HTTP verb (QUERY) [RFC](https://datatracker.ietf.org/doc/html/rfc10008#name-introduction) | Tom Jones || 
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born, maybe a terminology list? | Bumble ||

## 📅 2026-07-06 Minutes

- Banter
    - new members & Vouched exploring OAuth integrations
- KYA-OS update
- RFC10008
    - Tom: nota bene: IETF HTTP BIS WG doesn't define HTTP, that's still W3C jurisdiction
    - Tom: trust registries are a legal hallucination, I think the protocol and connection ceremony is worth thinking about
        - Tom: I think [MyTerms](https://myterms.info/ieee7012-standards/) is going a little crazy
        - "ceremony" from karl ellison
    - BF: Legal relationships are in scope... if you want it
        - Subra: KERI has some cool legal capabilities, non?  BF: totally! worth including
    - Alan: Does IEEE -7012 include some kind of intent?
        - see section b-2 [in the spec](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=11360682)
    - Tom: does it make sense to push down into OSI level 4? is that crazy?
        - BF: idunno conneg is p cool?
        - Tom: I think the issue is more about trust models-- can you really trust an endpoint to REPRESENT the legal entity that own/runs it? can you trust TLS? Did they give the TLS keys to CF? is amazon.com (run by amazon US) trustable to obligate amazon UK to ship me? isn't it even worse to trust an agent based on who runs its domain apex?
            - alan: good point
    - Grace (in chat): therapy usecase might unearth more legal complexity than just "go buy me things, agent!" usecase
        - Tom: Recent german case: LLM model made responsible hallucinations 
        - responsibility and authority get real bad
    - 

## 📅 2026-06-29 Agenda - SPECIAL TIME - starting half an hour early

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 30min | KYA-OS and/or CIMD for agents | Judith (Curity) ||
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born, maybe a terminology list? | Bumble+Damian ||

## 📅 2026-06-29 Minutes  

- Judith Kahrer (Curity) - primary product is a specialized AS
    - CIMD <> KYA-OS?
    - CIMD URL-->doc <> did:web -->doc
    - OAuth WG context at IETF
        - Other CIMD<>Agent stuff in the OAuth WG
            - Core CIMD [internet-draft](https://datatracker.ietf.org/doc/draft-ietf-oauth-client-id-metadata-document/) - up to 5th iteration since July 2024 now
            - [Authlete](https://www.authlete.com/developers/cimd/) [AuthZero](https://auth0.com/blog/cimd-vs-dcr-mcp-registration/) [Takahiko Kawasaki](https://darutk.medium.com/cimd-metadata-policy-c25969b538b6)
        - Judith: i-d for how AS can challenge an MCP client directly ("on behalf of the MCP Server")
            - Context: MCP server (until recently) needed to authZ clients 1 by 1 (for a given scope)
                - scopes hard to decide upfront; long-running task or background/monitoring tasks (i.e. renewing grants)
                - mandate more important than scope - have been thinking in that direction
    - Damian: KYAOS?
        - Dylan:
        - Judith: CIMD borrows lots of the DCR protocol; i see DIDs as key DISCOVERY; delegation [VC] could be a mandate; i see CIMD as a did specifically for running code; there was a [draft in OAuth workload identity<>ClientID merger](https://www.ietf.org/archive/id/draft-ietf-oauth-spiffe-client-auth-02.html) (why did it use SPIFFE but not a DID? could've used either or both)
            - Dylan: Yeah that makes sense
            - Dylan: Revocation and attenuation easier to reason over when each actor is DID-identified; the KYA-OS system has "levels" (for progressively authorizing an agent MORE over time, as more trust signals and attestations accrue to it); see [spec here](https://www.kya-os.org/mcp/docs/concepts/verification-protocol/flows)
            - Nicola: SPIFFEE is very efficiency-focused, so DIDs might be much slowed in many contexts; so maybe it's worth exploring "bootstrapping" to SPIFFEE where possible, DID slow lane? (or some future SPIFFEE or SPIFFEE-like thing that's more flexible on data shape, so that DIDs are easier to integrate)
            - Judith: Yeah, totally, SPIFFEE AND DIDs makes more sense than XOR
                - Nicola: DIDs good way to identify a given model/config/harness, but running it 10 times in parallel can spin up 10 SPIFFEEs for each ephemeral instance
        - Dylan: the
        -  
    - Grace: OAuth systems and DID systems need a bridge, so this is a promising direction for me as ED of DIF
        - Judith: I haven't made up my mind about how to bridge or whether to bridge, but OAuth has its own various key discovery mechanisms
            - Judith: If you want to authN clients that are id'd by a did, you'll need to translate to downstream OAuth APIs anyways (token exchange, etc), whether it's translating the same key into OAuth-native key expressions
            - Dylan: A registration record (pointing to a SPIFFEE id) is an ephemeral token, the authority stops at the AS that gave it the bearer token? downstream servers are just expecting bearer tokens, not DPoP
            - Judith: Yeah but that's not an agent-specific problem, most contexts where downstream servers are handed a bearer token are already secured otherwise? Dylan: probabilistic/nondeterministic software changes the terms a little, i would think... 
            - Alan: OAuth the protocol or OAuth the token?
            - Alan: History of DCR's sybil problem, which they keep adding another layer and another layer of identity docs; 
    - Concluding
        - Dylan: CIMD + mandate is a great onramp to a good e2e provenance layer
        - Damian: What's exciting here is a way for an agent to bring a CIMD or a DID and get treated the same way
        - BF: Join DIF! Or just present an IP-safe version
        - Alan: AI Security conf at Stanford; 
- Regular Business
    - Tom: Presentation [at CCG yesterday](https://github.com/TomCJones/threat-modeling/blob/main/models/Threats%20created%20by%20the%20introduction%20of%20Intelligent%20Agents%20to%20the%20WWW.md)
        - CCG reminded me SSRF isn't here and should be
        - Dylan: Are there levels of trust here, or relative weight/urgency/threat?
            - Tom: I think there are level of infra trust (Apple Wallet most people trust a lot) versus... Dylan: Yeah, a captcha
        - Tom: caveat, cloudflare started this and the major browser vendors are all behind it now
    - 


## 📅 2026-06-22 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born, maybe a terminology list? | Bumble+Damian ||

## 📅 2026-06-22 Minutes

- Updates
    - KYA-OS - waiting on SC, v1.1 design issues up next
    - Delegated Authority
    - [LFDT workshop](https://www.lfdecentralizedtrust.org/privacylondon) - Damian will represent us
        - Damian: Tell me what to ask/yell!
        - DIDs versus CIMD?
            - Dmitri: CIMD was invented in parallel to DIDs (or reinvented it?)
        - DIDs versus OIDC-provisioned identifiers and metadata documents
            - Dmitri: DCC did a report on how to use OIDF registry (URL-to-"metadata statements" mapping) as a VC issuer-registry; 
            - Tom: Federation spec is orthogonal and fairly distinct from the rest of the OIDC structure; it's a generic registry of URLS --> entity statements
    - Sidebar on long-lived identifiers
        - Erik: Not all opaque identifiers are created equal! SAG-AFTA member# is on a need-to-know basis, needed for payroll/licensing, so selective-disclosure is key
            - Consent TF at CAWG - URI that needs to contain (shielded at least) some legally actionably identifiers and TDMAI consent to help platforms gate their content, so that's what we're designing
            - School yearbook photo usecase: narrow licensing + "Take it Down Act" - maybe people will start reading HTTP headers 


## 📅 2026-06-15 Agenda 

| Time | Agenda Item | Lead | Notes |
| :---: | :--- | :--- | :--- |
| 5min | Announcements, routine business | Juan |
| 5min |  KYA-OS (new earlier meeting time!), delegated authority update | Juan ||
| Remaining Time | Keep discussing policy and/or governance work items struggling to be born, maybe a terminology list? | Bumble+Damian ||

## 📅 2026-06-15 Minutes

- Announcements, routine business 
    - Alan attended Identity Salon. Inc IAM & Security leaders at Fortune 50 companies. Attenuated delegation was raised, had to be explained to participants! 
    - Fable (new Anthropic model) / CLI [anecdotes](https://simonwillison.net/2026/Jun/11/fable-is-relentlessly-proactive/)
    - Alan: This reinforces for me that we Need to filter LLM requests through a non LLM policy engine (e.g. Clawdrey Hepburn )
    - Erik: we'll all have AIs tied to our devices, e.g. Siri - how will access be gated? 
- delegated authority update
    - Update from DA group: Dmitri has written up his description of ZCAPs, Alan doing the same for UCAN. Juan working out how to merge in Governance considerations / threat model / protocol assessments (so they are interlinked and function as a suite of related specs)
- KYA-OS (new earlier meeting time!)
    - Update on KYA-OS group - approaching consensus on V1, some are waiting to see how V1.2 looks / how extensible it is, to fully endorse it. 
    - Ran out of time for SC to approve last week, will happen asynch
    - Convos still happening on prototyping KYA-OS
    - Liability for Bearer Tokens: Tom did some thinking on why they suck / whether they are still acceptable. 
    - Alan: agrees with the problem. Bearer tokens are the last resort. Proof of possession - can I prove I'm the designated holder. OAuth RFC to do this is D pop. 
    - Tom: One next step could be to look at the liability model for more complex tokens. 
    - Juan: any time you create a bearer token you're encouraging impersonation by the agent
    - Alan / Juan: you would also need to bolt on extra surveillance to enable bearer tokens to be auditable
    - Tom: liability for bearer tokens is very unclear. Without an AUD you can't assign responsibility 
    - Alan: Token exchange still uses bearer tokens, albeit enabling attenuation and revocation
    - Juan: Agents swallow up bearer tokens like cookies, API keys etc
    - Erik: designed the consent mechanism for CAWG. When the token is transferred, it can include consent declarations. 
    - Juan: Single Sign On also uses a bearer token! 
- future work: policy and/or governance work items, terminology list?
    - BF working on getting the AAIF Taxonomy WG's working draft as a possible starting point or input doc 

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
