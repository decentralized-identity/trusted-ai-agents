# TAAWG - KYA-OS Task Force

[![hackmd-github-sync-badge](https://hackmd.io/q4ooV2G8RLy64ejstykq3g/badge)](https://hackmd.io/q4ooV2G8RLy64ejstykq3g)

## future topics

- statusList2021 - does it need to be public/global? should the spec encourage non-public URL usage of statusList2021, or authN'd/internal-only/RS-side revocation anyways, à la UCAN/ZCap?
    + is this a quick PR or a directional thing? do we need more donations/a pluggable revocation mechanism?

## 11 Nov

- Builder Registry
    - [Bankee.ai](https://www.bankee.ai/blog/protocol-layer/kya-os)
    - Some portion of bandwidth of VouchedID DevRel (hiring ongoing) can take lead on coordinating meetups and discord and all that top of funnel 
- Dylan: A list from IIW of prior art worth looking at: 
    - CyberStrategyInstitute, NEXUS v0.4: ships a Portable Delegation Bridge adapter for KYA-OS identity and delegated-authority evidence. 
    - AINumbers, OpenChainGraph: ships KYA-OS credential-chain attestation checker tools.
    - IDCanopy: their KYARA receipt layer is built on top of KYA-OS as the identity and delegation standard underneath payment protocols.
    - AgentLair: drafted a proposed Level 4 behavioral trust extension on top of MCP-I's L1 to L3. An extension proposal, not an implementation, but it means a third party is building upward from the ladder.
    - OWASP AISVS C09-05 catalogues KYA-OS for requirements 9.5.2 and 9.5.5
    - W3C Agentic Web WG charter draft names DIF TAAWG and KYA-OS in its coordination section
    - Keio University academic survey (arXiv:2604.23280) evaluates MCP-I/KYA-OS in its standards comparison
- Dylan: Other IIW takeaways
    - KERI people everywhere!
        - Sidebar: did:webs and the "bridge between KERI and DIDs/VCs"
- What KYA-OS already has
    - CIMD pretty done, but needs to be written up better
    - A2A part of LF?
    - NANDA AgentCards
    - Policy adapter (generic)
- What KYA-OS needs to prove greater interop
    - more detailed AuthZEN policy adapter and specifically the new 4Sept COAZ draft
        - COAZ has a "yes and" or "no but" syntax for HITL/stepup policies (could be enforced with delegated authority as an onramp)
        - Dylan's change reqs for COAZ extensions: 
            - 1 "no schema for chain-authZ envelope"; 
            - 2 principal always human and agent always agent
            - Dylan has a contact there; possible work item? (BF: Dmytro might be interested here)
    - WIMSE/SPIFFE adapter (contact Curity?); check against 
        - ID-JAG isn't multihop by design (it's token exchange)
        - prior art tends to lose provenance along the hops (confused deputy arises from that isolation)
        - did-binding spec wen
- Dylan: Agentic Web Framework at W3C: TAAWG already a coordination point, but need 
    - ANP, etc - 
    - Spiffe and Spire in CNCF
- Press/namechecks [chart](https://imgur.com/iIwD4gh)
    - ![](https://imgur.com/iIwD4gh)
- TPAC Contacts
    - iShare (NL-based, GLEIF-adjacent) - might
- Rosalyn: Michael Casey, Tricia, AAIS down to coord
    - Big in AAIS: [aqua protocol](https://aqua-protocol.org/)
    - meeting forthcoming
- Action Items
    - [ ] Grace - Get Daniela B on the horn about a KYA-OS specific meeting

## 20 Oct

- Grace: KC event went well. Demo landed, one of the participants is speaking to Juan potentially about membership, works with big Enterprises in Germany & wants something that's implementable on-prem / not tied to any vendor's solution 
- Dylan. Re Fraser's [comment on Request proof binding](https://github.com/decentralized-identity/kya-os-mcp/issues/253), invited Fraser to shape this as a potential contribution
- Dylan submitted a [new PR 15min ago](https://github.com/decentralized-identity/kya-os-mcp/pull/256) for envelopes & schema we went over last week
    -  Doesn't include the execution side (request binding, deterministic algorithm for processing)
    - does include other stuff we covered like payment, intent/manifest, constraints/caveats
    -   doesn't cover idempotency/journal-recovery capability or storage 
-  Does include payment authorisation, caveats, outcomes, evidence references, outline for MCP negotation & mappings to adjacent protocols 
-  alan: what's the rela to e.g. AP2 or other prior art's intent/manifest semantics?
    -  dylan: the payments protocols all have some kind of intent or mandate object, we are trying to be a transport-level/substrate solution that has a lowest-common-denom intent/mandate answer in case no more specific one is provided in the data;
    -  dylan: the mandatory info at this layer is somewhat orthogonal, and more permissions/authZ focused ("evidence-"); but this extension adds a few more mandatory items that can provide minimal answers to multiple protocols' messages on top
    -  Alan: more concretely: do the dictionary terms map 1:1? is a "manifest" here an AP2 manifest?
        -  Dylan: not 1:1 in every case, more of a lowest-common denominator
- Alan: it would be good to docuemnt a comparison of existing authorisation manifests / data models / protocols, and a justification for why a new one is needed (para or two at most)
- Juan: part of the justification is to have a fallback in case the 'happy path' is not available 
- Dylan: Recovacation is tricky because you want to be able to cancel a transaction before it reaches the payment processor
- Working design docs [on member-only Slack](https://difdn.slack.com/archives/C0AK05AKHGV/p1791571106410819?thread_ts=1791383056.947339&cid=C0AK05AKHGV) 
- PRs welcome
    - Execution context protocol
    - double-checking what each commerce protocol would additionally need
    - [8.4.6 algorithm for verification](https://github.com/decentralized-identity/kya-os-mcp/blob/f32bab579be236c5662eb54da26cb09682d8b857/experimental/payment-authority/SPEC-PAYMENT-AUTHORITY.md#846-verification-order) in particular could use close and wide review
        - Alan: like old compilers that stopped (and threw) on first compile error, maybe it's better to keep going and report ALL failures in one response? Could be a MAY instead of a MUST to allow both ways?
        - BF: maybe worth being loose in case some [future] commerce protocols requires verbose error logging or something; i can imagine those tradeoffs might be contextual, not universal
        - Dylan: Actually Ive been benchmarking it for time and compute, I should think about how i'm measuring that and measure 
        - Alan: Third option: do a few quick-exit checks first, and then all-or-nothing the complex-to-evaluate stuff? the more we talk the more i think this should be implementation-specific
        - Dylan: revocation list entails a query (and uncertain latency thereof); so far i've been mostly optimizing for latency and mitigation of expiry/revocation clockskew (partic of intermediary permissions)
    - [Standards mapping section](https://github.com/decentralized-identity/kya-os-mcp/blob/f32bab579be236c5662eb54da26cb09682d8b857/experimental/payment-authority/SPEC-PAYMENT-AUTHORITY.md#12-standards-mappings) in partic could use some love
    - [WG open questions too](https://github.com/decentralized-identity/kya-os-mcp/blob/f32bab579be236c5662eb54da26cb09682d8b857/experimental/payment-authority/SPEC-PAYMENT-AUTHORITY.md#open-working-group-decisions)
        - extension namespacing - can someone use this without using MCP-core?
            - BF: pro of one being extension of the other is it mitigates cornercases around using a new version of one with and old version of the other, etc-- versions lockstop to the parent namespace
            - Dylan: also worried the payments piece could evolve faster and get more outside contribution...
            - no need to decide soon, will think
- dylan: I think it's ready for people to play with please  extensions and hacking --> good tire kicking
    - most urgent feedback on execution/algorithm sections 
- dylan's action items
    - TOC
    - wordsmithing pass on "narrow only" --> "non-escalating"/"non-widening"
- Alan: asked if there is a section on privacy. Dylan confirmed this is the case. 
- Juan: the privacy and security sections will probably need to be re-done before V2; once there are mutiple implementations a lot can change
- Dylan: the only heavy lifing for a verifier wishing to implement KYA-OS is there are multiple considerations / decisions to make within 8.4.6 Verification Order 
- Juan: the spec doesn't need to be tightly coupled to one implementation's goals e.g. speed of response vs reducing round trips is context-dependent; best to start with a bit of leeway, in case someone needs to break a 'rule' as their goal is different to the reference implementation 


## 13 Oct

- Further workshopping of [internal draft](https://h0bb5.dev/v/YF4lcXZBWQp-hgB-NnMjmNnliqLeAcwCursGZIlAchY) of payments profile extension to spec-as-published
    - Fraser: Shopify, Stripe & Google are each in 2 -3 implementations of the protocols compared in his matrix (versus KYA-OS) 
    - Dylan: provided a walk through of the KYA-OS Authority Profile Flows
    - All other protocols phone home to Visa Agent Pay - but what happens before the token exchange is untouched
    - We're trying to stitch together the entire session so the merchant can verify the tx, connecting the protocols into a common authority layer
    - When a payment intent is created KYA-OS hashes this into an IntentDigest, adding protection against confused deputy, man in the middle etc. If the fingerprint changes, the tx can't be processed (barcode)
    - Post verification the system creates a transaction authorisation (not for money / payment
    - Rail Adapters allows KYA-OS to work across different protocols in x402, card, bank, wallet
    - Merchant receives intent digest and requested rail
    - It will get complex once a merchant wants to accept different rails, each rail does things differently 
    - The merchant's verifier will require certain properties to be present and won't accept the transaction without these (mandatory) properties 
- Broader discussion - KYA-OS as not just an MCP extension, but a more general "engine" for identifying and logging agents in any context/gateway
    - Sachio: is KYA-OS still an MCP wrapper, or are you building for additional protocols? 
    - Dylan: we view KYA-OS as like TLS for agents, a supplemental protocol that's hidden; it's about applying the bindings to whatever rails / harness / endpoint / gateway the agent touches. MCP is the reference implementation and a good starting point. 
    - Sachio: maybe i should see this as a proxy for many things, including MCP, A2A based agents, Langchain based workflows, Http endpoints etc. Then users like me can pick and choose which components we use, so if i want to build my own implementation for e.g. agent identity / binding agent ID / workload ID / accountable entity through KYC / KYB. Is that the idea? 
    - Dylan: that's exactly it! 
    - Sachio: very good!!
    - Juan: this is a natural opening for additional contributions 

## 6 October

- webvh

## 29 September

CommerceTalk

- Reviewing Dylan's [explainer](https://h0bb5.dev/v/YF4lcXZBWQp-hgB-NnMjmNnliqLeAcwCursGZIlAchY)
    - caveats (internal) versus payments profile add-on?
    - schema linked from doc but it's 404

## 22 September

- Rosalyn: having announced v1.0.0, the focus is on developing the spec, including integrating payment protocols 
- Dylan: the idea is to add a payments schema. Also paying to add support for did:webvh 
- In UCP it would be part of the mandate / delegation that's constructed. Binding between the user and agent, spend cap etc. The actio 
- The payment protocols don't answer the 'before the card' moment. You're at the mercy of the token provider for any session telemetry. e.g. being tamper evident. 
- Having this before session start until transaction time is what KYA-OS woud provide. 
- You could have an MCP server set up with KYA_oS, choose which token /tool call / delegation it's bound to, we'd still do the delegation minting. 
- A third party verifier would be able to use KYA-Os
- Sachio; what i could image is taking x402 as an example, some client as agent whos intent is based on some approved to make payment, that request is conveyed with consent to pay .e.g. if A2p / x402, that info is conveyed to the MCP server so now KYA-oS can support 
- Please order would have check out intent, 
- I want to standardise a profile for that so that the properties (e.g. currency type) are consistent . Then agent signs the request, 
- We'd still want the attenuation on the delegation e.g. budget. 
- Sachio: if we look at this from an architecture perspective, there are multiple ways of locating the policy enforcement point. E.g. put it in a sidecar. What i'm seeing recently is enterprises putting a proxy / gateway or multiple of them in front of each MCP, versus KYA-OS which is more of a wrapper intercepting ALL inbound on a given MCP. KYA_OS could do this and convey information . 
- KYA-OS may also act as an MCP gateway. How do we provide capability to integrate PDP / PEP? 
- Fraser - don't account-model blockchains solve the budget issue, i.e. via x402?
    - x402 vs AP2 vs ACP UDP (UCP?)?
    - Dylan: [AP2 captures the mandate as a VC](https://ap2-protocol.org/ap2/flows/) referenced by every event. "Budget" is a very hard thing to model in these kinds of things, i haven't seen that in any of the protocols
        - maybe that's merchant-side concern, not really our problem? 
        - are we doing enough if we coarsely distinguish "shopping" agents from agents with some access to a wallet?
        - The objective is fine grained control. what level of human verification is required to enable this? 
        - Decisions about when to step up authz lies with the merchant. Maybe KYA-oS does't need to decide or log every little thing and maybe being aware of the data models/categories/signals used to make that decision (e.g. in FinOS) might be enough?
        - Damian: How can we make KYA-OS useful to merchants deciding how much agentic traffic to allow?
        - Dylan: I think KYA-OS is already there, the merchant can already advertise merch via UCP, accept payments via x402, parse tokens from various payment protocols from out of a delegation and pass it along... our abstracting over the x402 complexity makes it comparable to traditional fiat payments from a merchant's POV; 
    - damian: what's the UX like? is the kya-os step exposed to user?
        - Dylan: ideally, if the consent is already given, the delegation step can be invisible; can't always be hidden, though, for example an x402 wallet binding/selection, or an ACP confirmation; 
    - damian: schema alignment? translating between differences in protocol minutae?
        - dylan: sort of, but usually the protocols don't differ that much; one outlier would be [kya-pay](https://kyapay.org/) by skyfire
        - fraser: can we borrow from AP2's mandate idea, for example? is it just data dictionary work
        - dylan: payment profile could be attached to each txn to fill in any missing inputs 
        - dylan: the hardest things to enforce here are time and budget and revocation; it's unclear what is in our scope
            - skyfire for example just does it as a bearer token; it functions more by expiry than revocation
- power to spend (race condition between multiple parallel agents?)
- Sachio: been playing with did:webvh; agent cards in nanda and a2a are self-signed, but webvh would make these a little more externally-signed/verifiable
    - open issues:
        - witness stuff is unclear
            - dylan: me too
        - performance/resilience concerns around statusList 
            - bf: more writers --> smaller bitstring/file, i would think? no BCP i can think of
            - matthew: statuslist is usually a govtech anonymity/herd-privacy thing; if you don't need anonymity, as small as possible (even just one list per operator or platform); one footgun i've suffered is counterparties caching it every 10sec, so consider a no-cache flag if you need them to get up-to-the-second data
            - sachio: when kill/revoke manifest versus kill spiffe/runtime

## 15 September
- Dylan reported out on a standards-focused workshop on agentic commerce attended by Vouched. 2 day conference hosted by Google. Attended by Huawei, shopify, visa, stripe, openAI. How agentic payments should be handled, which standards are emerging, etc. B2C centric. OpenAI showed how in 1 month their agent browser's action speed doubled. 
- No solution apart from KYA-OS was shown around credential handling, disclosure that it's an AI agent (agents are indistinguishable from regular user session by default - Merchants can verify it's a chatgpt session using the user agent header, however Claude is not playing ball)
- shopify demo'd WebMCP, however apart from KYA-OS there was no demo of an agent presenting user credentials and proof of delegated authz
- Huawei has a framework AP4? (similar ish to KYA-oS) integrated into Wechat, however no demo. 
- A lot of people were calling for auditability from third parties 
- Clear recognition of the gap that KYA-OS addresses, particuarly around need for outside auditability, need to avoid vendor lock-in. Bosch etc are advocating for an open standard around this. 
- Dylan showed the WG the demo he gave at the event (purchasing risotto using claude interacting with the merchant via KYA-OS)
- Juan: Potential to use KYA-OS with on-chain balances - speak to Wilmer from the group if exploring? 
- Alan: is looking for a home for his B2B negotiation protocol 
    - links:
        - https://shiftleft.com/mirrors/www.hpl.hp.com/techreports/2003/HPL-2003-152.html
        - https://shiftleft.com/mirrors/www.hpl.hp.com/techreports/2003/HPL-2003-153.html
        - https://shiftleft.com/mirrors/www.hpl.hp.com/techreports/2004/HPL-2004-77.html
- Rosalyn: we want to ensure KYA-OS continues to evolve; I want to figure out how to bring a little more structure to our conversations. In addition to the spec, we're working on additional use cases, also need to keep up with what else is happening in this space, make it easy for people to implement and adopt KYA-OS. Has 4 workstreams in mind: Spec, Ref Implementation, Industry Intel, Docs
- Rosalyn and Dylan will work on producing a timeline for these and other activities, to share next week 

## 25 August
#### kya-os-schema: 
- Repo is DIF hosted at: https://github.com/decentralized-identity/kya-os-schema
- Creates sha of conformance vectors e.g, sha256:81d537d4574d3f66d651a03ca41c0b18493b67ea6f3e61aba47d1bda4f3cf49b and PR template has been created for community: [conformance submissions](https://github.com/kya-os/kya-os-usergroup/new/main/registry/builders?filename=your-project.json&value=%7B%0A%20%20%22name%22%3A%20%22Your%20Project%22%2C%0A%20%20%22slug%22%3A%20%22your-project%22%2C%0A%20%20%22description%22%3A%20%22One%20or%20two%20sentences%20on%20what%20you%20ship%20on%20KYA-OS.%22%2C%0A%20%20%22homepage%22%3A%20%22https%3A%2F%2Fexample.com%22%2C%0A%20%20%22repo%22%3A%20%22https%3A%2F%2Fgithub.com%2Fyour-org%2Fyour-project%22%2C%0A%20%20%22kind%22%3A%20%22implementation%22%2C%0A%20%20%22buildsOn%22%3A%20%5B%0A%20%20%20%20%22kya-os-mcp%22%0A%20%20%5D%2C%0A%20%20%22contact%22%3A%20%7B%0A%20%20%20%20%22github%22%3A%20%22your-github-username%22%0A%20%20%7D%2C%0A%20%20%22listedAt%22%3A%20%22YYYY-MM-DD%22%0A%7D%0A)
#### kya-os-usergroup
- Community repo for reference implementations and adds a public 'builders' table to showcase services. 
- Builders are able to test their KYA-OS conformance off of test vectors to verify if they are conformant or not and receive a badge they can display on their repo's to show verified conformance.
- Site is hosted via Cloudflare Worker at the [builders.kya-os.org domain](https://builders.kya-os.org).

#### DID:WEBVH
- Juan Caveat: "Late publishing attack" - DID:WEBVH has a loose framework for implementing / mitigation. There is no normative solution, did:webvh could have a rotation event e.g, "jan 1st I rotate my keys" 
- Cool thing about did:webvh you can get the entire history of the method. Adds possibility to download entire thing to check version time rather than web/pre-request. 
- Machine readable 'show your notes' type of feature shown as registry implementation. 
- Create `didWebVHResolver` (similar to `did-web-resolver.ts` in kya-os-mcp). Leverage audit adapter for `trustedObservers[]` to reference witnesses for did:webvh.
- We can't force a controller to publish. Witnessing gives us detect + refuse-to-honor but not prevention. "To make sure your document in your hand isn't one behind, use a witness" (trusted observer).
- Dylan: Need to write separation of duties, when witness is introduced we should clarify the trade between 'trust the controller' to 'trust the witness'
- Outline trust model changes when did:webvh vs did:web.
    - Juan: Without a witness a did:webvh is basically a public key you got from 'some guy'.

## 18 August

Agenda
- Review proposed list of topics for v1.0.1 (Dylan has been collecting feedback from a handful of sources and will briefly review and prioritize each)
Discussion
- Rosalyn: goal today is to align on which items to address in the roadmap
- Dylan and Rosalyn are meeting with SC tomorrow to understand what requires approval (likely to be breaking changes)
- Ankur and Manu have provided feedback on what they would like to see addressed in KYA-OS 
- Top requested items:  Status List to bitstring, did:webvh (highest priority); none of these should probably need approval 
- Juan: some specs have received more SC scrutiny than others, due to e.g. cadence of changes / publication schedules; if we want to seek SC approval for KYA-OS v1.1 we can but that may not be needed. Treat minor changes as updates to editors draft in that case. 
- Juan suggested to create an issue in the repo to keep track of the roadmap, owned by Dylan, which is a URL to a changing document (features roadmap / future changes log in Github)
- Releases of the software / versions of the spec don't need to be in lockstep. E.g. the spec can be at 1.1 while the reference implementation is still 1.0. 
- Dylan: makes sense, good to know. Otherwise it would slow things down a lot. 
- Juan: might be good to concentrate on the versioning of the reference implementation and align the versions of the spec to major announcements
- Being able to point people to the features roadmap is potentially more important than publishing version releases 
- Rosalyn: agrees, the priority is to align the roadmap to what the market is asking for 
- Juan: Issues are not IPR sensitive, PRs are. Juan has been lobbying to treat authorisation / delegation languages e.g. ZCAPs as a pluggable thing - got some pushback from Manu on that 
- Dylan: probably makes sense for us to take a first stab at the roadmap before soliciting the TF's thoughts; items to address off the back include Lars' feedback / resulting small fixes (enable them to rebuild their verifier against the spec and test)  
- Juan: protocol specs are less tidy than software specs, re what constitutes a feature. Think of spec versions as mental models rather than hard and fast boundaries
- Plan for tommorrow: Dylan to put together a list of items (e.g. features in the reference implementation that may be rolled into the spec) for SC to review / ratify
- Juan: Re the User Group, anyone can open PRs (don't need to be a DIF member), Dylan to merge
- Re the builder registry, should be fine to merge changes outside of meeting time and only raise questions during the TF meeting
- The more eyeballs you can get on the roadmap, the more you'll get people raising their hand to open PRs
- Dylan: did:trail is a W3C tracked did method for AI agents. Reciprocal binding of mutual proof (principal + agent; 2 signatures vs just 1)
- Juan: the track to W3C approval for did methods will probably be chaired by me; the track does not yet exist. did:trail uses bitstring status list, which is neat. May well be worth implementing a driver in KYA-OS. We could invite the author of did:trail to present to the WG (e.g. with a view to contributing a driver), though he is based in Japan so may be difficult for him to join 
- EU AI act requires the operator of a service to know which human is the "beneficial owner" / responsible natural or legal person for an AI (hard to do without decentralized ID); KYA-OS will need a lot of drivers / modularity if people bring their own trust chains that terminate in UBOs 
- Dylan: agree, there's no way to do this without DID
- Juan: NIST guidance relates to large scale systems, which may not need DID to have UBO tracking (credit cards will play this role), wheras more complicated identifier schemes will need levels of assurance / auditability 
- Dylan: how can we do a verifiable presentation to reveal e.g. UBO ; may be needed if there's an insurance component or it's a regulated industry e.g. healthcare
- Juan: Being able to audit at UBO level will probably be part of the premium version(s) of KYA-OS
- Dylan: agree, getting a verified assurance level facilitates compliance, is a commercially valuable feature
- Juan: knowing the UBOs of a shell company is something that needs to be done at scale in real time, mostly done via oracles / APIs; extending this to KYA-OS there will probably need to be a similar approach (ARIA also has responsible person binding in their protocol; this might be a v2 thing for KYA-OS, experimenting with multiple routes in the meantime)
Summary - Actions 


- Action Items
    - [ ] - Dylan - prep for SC meeting 
    - [ ] - Dylan - chat with did:trail guy
        - [ ] give him bf's calendly! https://calendly.com/difsupport
    - [ ] Dylan - after SC, start feature backlog/roadmap
        - bf: suggested buckets:
            1. pluggable DID methods
            2. multiple permission/delegation DSLs?
            3. UBO/responsible-party tracking
            4. MCP-specific (or A2A/AP2/etc specific?) features
            5. Onchain/UCP stuff?
            6. miscellaneous
        - specs.md/skills.md? how make builder registry discoverable to agents and crawlers?
        - roadmap/backlog drift is bad; centralize to one place (glossary in each repo pointing to same place for such things)
    - some day - Izuru and did:trail guy both interesting re: UBO... keep thinking about this! (bf: also the did:aria guys!) 

## 11 August

Agenda:
- spec site transfer update - this week ideally!
    - /kya-os-schema/
    - /kya-os/
        - should have spec itself, glossary, etc; README links to all other repos
        - could have IP/WG-governed demos (if separate)
    - /kya-os-usergroup/  
        - builder-registry (render to subdomain) and BUILDER demos (if separate) 
- builder registry update
    - pending spec transfer-- will go live on kya-os.org subdomain or path (sep repo so that it can be publically PRable)
- Def Con - Dylan won 2nd place at their competition for his KYA-OS presentation! :tada: I'd like him to share that with you all
    - ![image](https://hackmd.io/_uploads/By_BenOUfe.png)
    - left pane: Claude (with kya-os connector enabled, and using a DEFCON badge as signer via FIDO2)
        - ![image](https://hackmd.io/_uploads/SJFsg2uIzl.png) - signing events show a confirmation on the badge screen!
    - right pane: revocation server running locally, with realtime event-log updates, and links to cosmos explorer to see CHEQD txns on-chain
    - [loom recording here](loom.com/share/f32b82a292f14a6c952dba3a0a246e45)
    - cheqd's onchain DRL version of statusList! Something like `resolver.cheqd.net/1.0/identifiers/did:cheqd:testnet:17bc59fe-2e93-4e01-8613-c7c4560adcf2?resourceName=kya-statuslist...`)
    - Alan: but if you ask claude to send 11 and the limit is 10, won't it just send as 2 txns?  Dylan: (tries it) well i'll be darned
        - bf: what about swarms? do they have swarm-wide or dist-txn-wide budget? alan: is there a "delegatable quota", so that people can delegate a fraction of their own budget to delegees? Dylan: Not... currently.  will have to think about that.
    - Dylan: What's a sensible default limit for Depth of delegation chain?
        - Alan: antipattern- you never know how many delegations a cross-org txn with multiple swarms might take! 20 or 30 might be normal in some usecases. if you limit delegation length, you're encouraging the guy (or the agent) at the last link to impersonate or share creds to get
        - BF: i'd make it configurable, some people will need lower limits for performance reasons (or needing entire chains to be expressible as a token, or base64 string of less than X length, etc, depending on the delegation DSL, backlinks by ref or by value, etc)
        - Alan: just think of delegation depth as a DOS vector, verifier is going to need to apply heuristics to inbound tokens anyways to protect itself from overruns and slow-downs...
- v1.0.1 - list of topics to cover for the next update and future updates. Note that Dylan and Rosalyn are meeting with DIF SteerCo next week to obtain their guidance on versioning and required ratification
    - sidebar: VC 1.1-->2.0 is breaking change... need to figure out how to manage that
        - bf (in chat): btw, Dylan, re: the breaking changes, one way to manage the VC2.0 thing would be to have a working draft or editor's draft of v2.0 already; it's a little confusing, and no need to link to it from the kya-os.org version of the v1.x spec, but it's a way to pre-design breaking changes now that don't get into effect until all the other breaking changes are decided
- [last-minute, not pre-announced] BF: SEP and MCP Registry entry PR? 

## 4 August

Agenda
- Rosalyn: v.1.0.0 press release impact
    - repo clones and forks up bigly, lots of new issues
    - Dylan shared some numbers: 1055 clones in the past 14 days, huge uptick since the annoucement. 193 unique cloners. 138 unique visitors.  
    - 282 clones the day of the new MCP
- Rosalyn shared a [LinkedIn post](https://lnkd.in/p/e6-iJDkc) to the effect that KYA-OS: Vouched handed it to the Decentralized Identity Foundation in March. 6 contributors, 263 commits in the last 90 days. More than all of AGNTCY (led by Cisco), and AP2 combined. Last push four days ago. AP2: Google handed it to FIDO Alliance on 28 April, the same day v0.2 shipped, zero commits since. I checked FIDO's GitHub org directly: 11 repos but nothing AP2 or payments related.
- spec site transfer
    - will transfer today, then cloudflare stuff
- builder registry
    - included in the transfer
- v1.0.1 - what should be addressed in our next update?
- [IzuruToys' issue on the main repo](https://github.com/decentralized-identity/trusted-ai-agents/issues/42) and Lars' very thoughtful [analysis on DIF Members-only Slack](https://difdn.slack.com/archives/C08NNP7PZ6Y/p1785648060668859)
    - VCDM v1 versus v2
        - v2 should be added later? at time of press, v1 was vast majority in the wild
            - issues [#151](https://github.com/decentralized-identity/kya-os-mcp/issues/151) and [#152](https://github.com/decentralized-identity/kya-os-mcp/issues/152) already merged, address this
        - human use-case -- ask to write up the use-case?
- Grace: [AIdentity & Non-Human Identity Impact Day 2026]()
- MCP extension update: Dylan: Must have an "experimental" WG under the AAIF to post MCP extensions. 2 properties in the spec for extension discovery. extension-discovery governed by the MCP WG there (also separate SemVer).
    - [template to create a WG here](https://modelcontextprotocol.io/community/charter-template) 
    - Dylan: process for extensions =
        1. maintainer or member (?) has to champion from the jump
        2. submit use-case
        3. dedicated interest group or WG create for that use-case w/a Lead with "contributor" status on MCP itself
- Juan: AAIF 'gave' DIF a seat in the AAIF; he was told at the time that the governance of each donated codebase is separate to the cross-org WGs. MCP-specific governance wasn't clear yet
    - Dylan: 
        - I found a fine-grained Auth meeting to join, but it felt more researchy; 
        - [CONTRIBUTING.md](https://github.com/modelcontextprotocol/typescript-sdk/blob/main/CONTRIBUTING.md) got beefed up on the MCP SDK;
        [extension submission process docs]() now uses more IETF MUST/SHD lang; 
            + current process requires ALL NINE core maintainers to approve each extension!
        - Dylan is still navigating the orga (discord and LF-wide calendar a little disjoint)
            - see also [WG listing](https://modelcontextprotocol.io/community/interest-groups/auth)
        - Rosalyn: you need some clout at AAIF to get an extension approved; we are looking into how to navigate this / get the extension sponsored; working with [AAIS](https://advancedaisociety.org/) on a pilot, they're evaling KYA-OS for recommendation/approved status
    - Dylan: WG leads must be on the contributor ladder
    - Grace: could we tap up a DIF friend who is on the ladder, e.g. Huawei are participating in AAIF
- Alan: Delegation to "Juan's Key"; short-lived delegation and short-lived keys
    - Dylan: I think that query is implicit int he entityCard spec; the delegation keys are single-use/single-purpose; agentCard has a CNF prop (fingerprint) for ROOT key, but derived keys used for all the delegation stuff; where no card is present, it treats delegated key as identity for logging purposes
    - Alan: Often an implicit assumption people bring to identity and delegation; being explicit in the spec couldn't hurt
    - BF: isn't this protocol-specific? Alan: AAuth and OAuth give ME the new ephemeral token to give to you, 
    - Dylan: Newest [PR](https://github.com/decentralized-identity/kya-os-mcp/pull/157/changes) cleans this up a bit
        - BF: 
    - Alan: BCP for delegation-specific ephemeral keys is for key to be generated by the delegee and returned to the delegatOR to be registered in logs... but that's not always possible, so that can only be a SHOULD and you gotta manage careful pragmatic exception
- Grace: [KupCole talk in Munich Oct](https://www.kuppingercole.com/events/nhiid2026) - Grace applied copy-pasting from KYA-OS spec and blog posts, I can represent`. Title: Who Approved That? The One Question Your Agent Logs Cannot Answer
- Grace: Will Vouched be at IdentityWeek DC? Rosalyn: Vouched is going, not sure if we specifically will go
    - Grace: If you DO go, meet Will from HAND (CAWG)
- Rosalyn: What's in V1.0.1. 
    - Dylan: Candidates: Did:webvh, bitstring vs StatusList 2021
    - Grace: breaking changes / moving from V1 to V2 will need to go to TSC

## 28 July

- MCP seems to be  ["going stateless"](https://blog.modelcontextprotocol.io/posts/2026-07-28-release-candidate/)
    - that'll break lots of people, but not us, we were early adopters of `_meta` sidecar for metadata
    - one error code will break, lol
    - extensions registry established by [SEP-414](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/seps/414-request-meta.md)
        - the `org.kya-os/mcp` doesn't work for naming the extension, so landed on `/delegation` because our delegation stuff 
        - debate around semantics/devex: what should come after the /
            - alan: delegate is neat, it's on trend these days (delegation > impersonation) 
            - bf: provenance or verification? mroe general, not everyone uses the delegation stuff
            - dylan: maybe lead with the uniq value prop? /consent? /human-on-the-loop? alan: /openworld-auth? dylan: /decentralized-authz? bf: /decent-auth alan: "in an open authorisation world, every participant has it's own authz policy"
- sidebar how to AAIF
    - BF: ask for a presentation-time at identity & trust wg (every other Thursday)
    - Dylan: the PR asap on MCP/auth-ext, would I&T WG help get that PR merged sooner? How do i get the attn of the MCP governers?
        - BF: couldn't hurt, but probably additional measures would help more
            - BF: business case most important for getting a quick merge
        - Dylan: DEFCON proof-of-control framework (Bob Montgomery, Dick Hardt, Midnight, MHuang (sp?), insurers/underwriters) ==> SOC2-like certification
            - [kya-os POC against that framework](https://poc.kya-os.ai/)
            - Juan: when talking about KYA-OS at e.g. DEFCON, reference mapping to e.g. AAIF / Advanced AI Society frameworks to fend off general objections to "decentralized tech" and anchor in real threat modeling and business case

## 21 July 

- agenda
    + v1 standard approval check-in
- Discussion 
- Dylan: delegation will live in the other doc, the KYA-OS doc will focus on the spec. 
- Dylan updated the doc based on 3 comments shared by Matthew
- Advanced AI Society is working on proof of control (enables external audit & determination of compliance status e.g. with EU AI Act, HIPPA), based on 4 levels. Dylan demo'd KYA-OS, mapping to their framework. He is considering doing a reference implementation based on this. 
- Alan: what does control mean? 
- Dylan: probably something that an insurer would require. Aligns to KYA-OS assurance levels.
- Dylan / Damian to send over entity card spec to Judith, get her thoughts on how CIMD mapping will work
- Update to core MCP spec is due late July / August. Consider submitting KYA-OS as an extension under the Identity track. 
- Grace: spec was approved by SC, next step is to announce on the blog (avoid being repetitive).
- Also re IETF, there are lots of side meetings / preliminary discussions, currently unclear what IETF expects its role to be viz a viz AI. Current work items: Small things e.g. workload identifiers for AI. Potential Large items: discovering agents using DNS. ITU is asking to collaborate and divide up scope in a logical way.
- Anthropic has implementations that may move into IETF. From DIF, KYA-OS could be a candidate work item, however DIDs aren't a good fit for IETF & Grace is advocating for a discussion about artitecture. Currently we see ITU as a better collaborator as they are in advanced discussions about what is in scope. DIF is seeking partners willing to have an open discussion. 
- Dylan: China and Singapore have 3x d visits to the KYA-oS page in the past few months. 
- Grace: IETF is not welcoming to non-OAuth approaches. 
- Also if we want to include participation from China, we may need to look at different communications tools (Zoom may be blocked).  ITU uses Meet You, very good & privacy preserving. 
- Alan: being untactful about OAuth generates good discussions, e.g. at IIW. 

## 14 July 

- agenda
    + v1 standard approval check-in
- Discussion 
- Re CIMD / client registration discussion / upcoming MCP release, there is a draft for adding a server JSON file. Nanda uses Agent Facts. Also one that A2A uses. Lots of proposals. 
- Dylan added PR to KYA-OS repo to use the same verifier for all presentations in different formats. See https://github.com/decentralized-identity/kya-os-mcp/blob/main/SPEC-ENTITY-CARD.md - includes a demo
- Alan: how do we deal with the semantics of what the words in the presentation mean.
- Dylan: they are trying to define the terms. 
- Alan: since we're dealing with LLMs,we have the opporutnity to describe the agent properties using natural language.  These could be independently attested in a VC. Example: "My agent understands how to read weather maps and will charge you 5 cents", signed by the National Weather Service. The advantage is you get round the need for everyone to agree on a precise ontology. "My experience is attempts to get precise on these things always fail"
- Dylan: AAuth uses the Governor (an LLM to handle governance). Alan is not a fan!
- Matthew Rappard: I think the eventually the agent will cache the description in some intermediary agent format.I think it’s not an OR but an AND.  I think we can use natural language, but inevitably a TAG or some other more computer version will have utility.
- Alan asked about "Delegation Chain" and "Audience". 
- Dylan: this relates to if there's a multi hop scenario. 
- Alan: it's a claim delegation rather than a permission delegation. Dylan: yes.
- Alan: the whole mess with client registration in OAuth is it breaks cross domain. 
- Dylan: agree. I see CIMD support as an on-ramp into the protocol. 
- Matthew: We might have multiple proof for multiple trust registries so the “audience” would describe which trust registry this proof was for.

- Matthew (in chat): The “Status of This Document” section says the stateless proof coexists with the legacy proof “under the same _meta key.” Section 8.1 then says they deliberately use separate keys:
    + _meta["org.kya-os/proof"] 
    + _meta["org.kya-os/proof@1"]
    + I think the first is a contradiction
- Next steps for the entity card? 
    - Dylan: might demo/PoC something for AAIS with this (their levels map to KYAOS's), 
    - also send to Judith to see if it passes basic OAuth WG sanity-check

## 30 June

- agenda
    + v1 standard approval check-in
    + Presentation yesterday: CIMD vs DCR
        + Dylan: other RFC in play at IETF would provide unidirectional link from a CIMD to a WIMSE? particularly if so, I see CIMD as a good good "level 0" onramp to KYAOS
        + Dylan: in our system, DID is key-bound identity, CIMD would just be a base-level did:web equiv
        + BF: I was curious about the "key discovery"
        + Dylan: I think OAuth still ends up at a bearer token; 
        + Dylan: I'm very curious if she's asking for help authoring or accepting contributions about a section of her i-d/rfc
            + CIMD > DID > Mandate more valuable to KYAOS than DID > CIMD > Mandate
                + bf: what if mandate could take either as a subj? dylan: idunno, slippery slope... 
        +
- push to next week
    + KYA-OS builder community
    + post-approval timeline (blog post, etc)
    + discuss cheqd usecase and PR 
    + developer advocate?

## 23 June

- agenda
    + discuss cheqd usecase and PR next week?
    + post-approval timeline (blog post, etc)
    + developer advocate?

# 16 June

- feedback on v1 draft
    + 1 SC member: DIF-wide deprecation of did:web/recommendation of did:webvh? 
        + bf: I think this is a v1.2 or v2 thing, we should try to get an extension in after did:cheqd
        + rosalyn: talked to verana.io
    + alan: i don't think my point about revocation and claims made it into the edits; i'll leave more comments on slack (see below)
- post-approval?
    + blog post? grace: just posted about the donation, would be redundant, so let's think of a good way to post about it (interview? some other narrative?)
        * rosalyn: v1-1.2 roadmap; action plan? 
- damian: Curity (sp? IAM in Nordics) working on agentic authZ; saw KYA-OS as a bridge from CIMD-identified agents --> OAuth
    + alan: VCs often bound to client identities; so worth asking how to use CIMD without a "client registration" problem; delegation and revocation of permissions != delegation and revocation of claims
    + statusList2021 revocation for example doesn't need to be globally readable/unauthNd; 

## 9 June 2026

- Final feedback
    - alan --> dylan: i think i've reworded everything conceptual
    - kya-os.org migration (and schema migration) all done
        - schemas + spec site repos both will move to decentralized-identity/kya-os-*
- other dev updates
    - more providers (make auth pluggable); fetch provider; storage provider
    - tazos (sp?) from cheqd adding did:cheqd (and onchaining some receipts to cosmos chain); that [PR](https://github.com/decentralized-identity/kya-os-mcp/pull/93) is in progress
    - need an API key for cloudflare Pages, then add it to the github repo
- Steering Committee approval (tomorrow)
    - Grace: Helps me to have an overview of reviewers and incorporated feedback
    - Dylan: [changelog](https://github.com/decentralized-identity/kya-os-mcp/blob/main/CHANGELOG.md) in the MAIN repo is p thorough
        - npm bump will bring this changelog with it
    - Dylan: mostly the delegation-chain and fancy OAuth 2.1 stuff got differed to v1.2, examples 
    - Grace: First pageload "intro" section still sounds like KYA-OS is only for MCP
    - BF: "Community" link --> [WG Webpage](https://identity.foundation/working-groups/trusted-agents.html)? KYA-OS's existing Open Discord?
        - Dylan: IdentiClaw demo was on the discord, but mostly non-commercial
    - [GH Analytics worth a gander](https://github.com/decentralized-identity/kya-os-mcp/graphs/traffic)

## 2 June 2026 

- Adapter to connect to storage for persistence, plus OAuth adatper can be added to demos (one has one server that acts like the OAuth provider)
- For spec site & schema, Juan got access to KYA-OS.org domain and pointed it to the spec site, schemas still need to be ported over (this week) - a second repo that will be transferred to DIF - will be source of truth for deployed schemas 
- Rosalyn: Comment period is closed for KYA-OS
- Dylan showed provider-registry, which will recognise different provider schemas (+ ability to add custom provider). Depends on auth method - credentials by default, also passkey, Google,Github
- New auth methods can be easily added using a template (import default registry, pull in OAuth provider if OAuth)
- Dylan's summary: 2 layers: auth method, registry provider 
- Dylan will update the package this week 
- Schema repo will have plug to deploy the site, deploying the schemas (will be deployed on PR push). E.g. if going over HTTP / using MCP, those implementations can use the specifics from any provider being used. 
- If a provider submits their schema to the repo...
- We could show on the website other orgs / tools which are adjacent to / compliant with / building with KYA-OS (e.g. MCP gateways)
- Could do industry audit on who is aligned with what, which other servies are 
- Value is in aligment, e.g. if all outbound requests have KYA-OS header attached with ID presentation, it tells other businesses there is traction in that pattern / promotes interop 
- Next week Dylan will add more examples / reference implemetnations to the repo, plus show how the Auth adapter works / expand on it
- Including flows e.g. you're a server operator and want both compliant and non-complaint agents to be able to connect, auth & consent flows before delegation credential is minted  
- Repo analytics / insights - 90 unique clones in last 14 days
- Vouched is creating a builder community to support orgs leaning in 
- Damian to check if DIF has benchmarks from other projects 

## 26 May 2026 - discussing roadmap feedback

- migration update
    - spec migration ready to go, will do later today (specs will move to kya-os.ai/mcp)
        - repos will be transfered to DIF
- Feedback (copied from Monday sync notes)
    - KYA-OS feedback on [proposed roadmap](https://difdn.slack.com/archives/C0AK05AKHGV/p1778776535438769)
    - Sachio's feedback [on Slack](https://difdn.slack.com/archives/C0AK05AKHGV/p1779652848654009): Cedar --> PaC; REL integration (as part of pluggable AuthZ); arbitrary .well-known filenames (to align with NANDA, Agncy, etc); OAuth 2.1 adapter interface strongly recommended in later versions
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
- Feedback discussion
    - Sachio's feedback
        - Dylan: Generalizing "just Cedar" to more PAC stuff makes sense; going pluggable there makes sense, as with AuthZ; the OAuth stuff is already pluggable upstream, was already planning on bringing it over; 
            - Sachio: wise to standardize Interface, and let multiple implementations compete for the AS integrations and OAuth methods; I think adoption hinges on smooth integration with many diff kinds of OAuth [2.1] flows and configs
        - Dylan: 
            - will fix terminology in V1;
            - Generalizing Cedar to PoC and pluggable AuthZ we will target spec in 1.1 and support in 1.2 depending on our internal timeline;
            - arbitrary manifest files (//NANDA registries) seems an easy change, was waiting to see how they evolve but can get those in 
        -  Sachio: ZCap folks wanted to use ODRL cuz it integrates cleanly; this is what I meant by beyond Cedar 
    - Tom's feedback
        - Dylan: lots of overlap with Alan's - lots of it is addressed [in the changelog](https://github.com/decentralized-identity/kya-os-mcp/blob/main/CHANGELOG.md)
        - linkability is a bigger problem - if we want unlinkable credentials, that probably couldn't happen any earlier than 1.2, let's call that 1.X; in the meantime, spec can mention this
            - Sachio: did:peer for ephemeral DIDs would work, but spec is ambig, looks like did:webvh is being used in the impl?
            - Sachio: can't remember exactly what, but I think there was a contact7 bug where spec didn't match and messages weren't parsing/verifying right; Dylan: contact7 and brave-mcp were just in there for an example 
    - Alan's feedback on credential formats (VCs vs ZCAP / UCAN)
        - Binding permissions to specific enumerated resources depends on the AuthZ DSL (Tom's "missing context" feels related); 
        - Dylan: Credentials other than delegation are now rejected by default (to avoid confused deputy). Reference issuer.Tightened capability language in the spec. User DID field in schema now reads “whose delegated authority the agent exercises”. Many changes to the spec to reflect Alan’s feedback, including updates to trust model, threat model, revocation. Introduced principal & responsible party as first-class terms.    
    - Alan's feedback on registration flow
        - Dylan: updates made to conformance requirements, language on re-delegation (to ensure agent needs to request this if delegation revoked) 
    - Alan's feedback on Directory of MCP-I endpoints
        - Dylan: we now have the schema, not updated at the time of Alan’s feedback 
    - Alan's feedback on revocation
        - Dylan: Level3 requires strictest conformance re auditability; UCAN handles revocation as an explicit delegatable permission, could be a good flow to use. Language in spec has been updated to state statuslist / bitstring not required for permission revocation 
    - Alan's feedback on reputation management 
        - Dylan: believe his feedback was around the search functionality on KnowthatAI 


## 14 May 2026 - v1 Roadmap

- donation of KYA-OS-core is live! 
    - will figure out npm package pipeline soon (will stay at `kya-os/` npm org)
    - last clean-up of naming stuff will also add [DIF membership requirement](https://identity.foundation/join) for PRs.
        - Optionally, it might help to say DCO is required _FOR ATTRIBUTION IN CHANGELOGS_. that might get more contributions from DIF members who DON'T want to set up DCO on their github accounts but DO want to fix a typo or notice a bad loop or something.
- Workflow?
    - More formal about specs and ref impl, less formal about tutorials, example spec, prototypes, experiments, etc., extensions/optional bits...
    - CONTRIBUTING.md policy for PR review process
- v1 Roadmap
- Next Steps
    - [X] BF - announce 14-day review people 
    - [ ] Dylan - Rename spec website & 301 all links (incl schemata) - donate repos that build those two sites as well
    - [ ] BF - recruit TSC to review as well 
    - [ ] WG to decide after that how and when to present V1 to SC for approval (next SC in 3 weeks!)

### Roadmap Proposal

# `@kya-os/mcp` — V1 Scope

**Spec:** 1.0.0 Stable · **Package:** `@kya-os/mcp@1.2.0` **Status:** Donated to DIF TAAWG for ratification

The MCP binding of the KYA-OS primitives. Adds cryptographic identity, delegation, and signed proofs to MCP servers. Profiles existing W3C and IETF standards into a stable wire format.

---

## What's in V1

| Area              | Capability                 | Standard / mechanism                                                                                                                |
| ----------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Identity**      | Agent DIDs                 | `did:key` (ephemeral) and `did:web` (org-hosted)                                                                                    |
|                   | Signing                    | Ed25519 / EdDSA, 64-byte sigs                                                                                                       |
| **Session**       | Handshake                  | 16-byte nonce, audience, timestamp (±120s skew)                                                                                     |
|                   | Replay prevention          | Nonce cache with TTL retention                                                                                                      |
|                   | Session model              | `mcpi_<uuidv4>`, idle-timeout tracking                                                                                              |
| **Delegation**    | Credential format          | W3C VC v1 with `Ed25519Signature2020`; <br>JSON-LD and **VC-JWT** representations                                                   |
|                   | Constraint envelope        | **CRISP** — Constraints, Resources, Identity, Scope, Policy (exact/prefix/regex scope matchers, budgets, temporal bounds, audience) |
|                   | Chain semantics            | DAG with parent-child links; <br>Child scopes MUST narrow parent                                                                    |
|                   | Revocation                 | StatusList2021 (gzip bitstring) with **cascading revocation**                                                                       |
|                   | Transitive enforcement     | `requireAudienceOnRedelegation`                                                                                                     |
|                   | Migration                  | `allowLegacyUnsafeDelegation` escape hatch (documented as temporary)                                                                |
| **Proof**         | Format                     | Detached JWS over RFC 8785 JCS-canonicalized request/response hashes (`sha256:<hex>`)                                               |
|                   | Attachment                 | Response `_meta.proof` — invisible to the LLM                                                                                       |
| **Outbound**      | Cross-hop chain of custody | `kya-agent-did`, `kya-delegation-chain`, `kya-session-id`, `kya-delegation-proof`, `kya-granted-scopes` HTTP headers                |
| **Authorization** | Hint pattern               | `verifyOrHints` + `needs_authorization` response with consent URL + resume token                                                    |
| **Discovery**     | Service doc                | `.well-known/mcpi` (capabilities, endpoints, algorithms)                                                                            |
| **Integration**   | MCP SDK                    | 2-line adoption: `withMCPI(server, { crypto: new NodeCryptoProvider() })`                                                           |
| **Extensibility** | Provider model             | Pluggable `CryptoProvider` / `StorageProvider` / `NonceCacheProvider` / `IdentityProvider` / `ClockProvider` / `FetchProvider`      |

**Conformance ladder:** L1 Core Crypto (10 reqs) → L2 Full Session (15 reqs) → L3 Full Delegation (25 reqs). Every requirement maps to a named test.

**Quality posture:** 884 tests · 53 files · 88% statement coverage · CI on Ubuntu/macOS/Windows × Node 20/22 · CodeQL · product-contamination CI guard.

**Schemas:** 5 JSON Schemas (Draft 2020-12) shipped in the tarball and exported as `./schemas/*.json`.

**Examples:** 4 main + 3 specialized — including a **2-line migration of Context7** (real third-party MCP server) and a **full revocation lifecycle** demo.

---

## What's not in V1

Cedar scope language · selective disclosure (BBS+ / SD-JWT) · DID methods beyond key/web · pluggable resolver registry · OAuth/OIDC adapter interfaces · reputation hooks · audit-event taxonomy as typed contract · tool-protection type contracts · multi-language SDKs (TypeScript only) · conformance vectors as separable package · selective revocation. 

---

## Proposed V1.1

**Extensibility (so the community can land things without forking the core):**

| Item                                | Why                                                                                                                                                                                                                                       | Source |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| **Pluggable DID resolver registry** | Today `did:key` + `did:web` are hard-coded. Registry pattern lets `did:webvh`, `did:peer`, `did:jwk` land as drop-in modules.                                                                                                             | New    |
| **Signature suite abstraction**     | Orthogonal to `CryptoProvider`. Today Ed25519 is hard-coded through JWS alg, multicodec prefix, key/sig sizes, proof type. <br>A `SignatureSuite` interface unblocks ES256 / ES256K / BBS+ / post-quantum without touching protocol core. | New    |

**Protocol surface (upstream what Vouched already built out):**

| Item                                                                 | Why                                                                          | Source                                     |
| -------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------ |
| `.well-known/agent.json` agent document                              | Discovery for non-DID consumers; already shipping in xmcp-i                  | Upstream from `/contracts/well-known`      |
| **Audit event taxonomy** as typed contract                           | KeyRotation, SessionStart, ToolExecution etc.; privacy-preserving by default | Upstream from `/contracts/audit`           |
| **Tool-protection contracts**                                        | Typed guard format for per-tool authorization                                | Upstream from `/contracts/tool-protection` |
| Conformance vectors as separable package (`@kya-os/mcp-conformance`) | Language-agnostic JSON fixtures so future Python/Go/Rust SDKs self-validate  | Spin out from `src/__tests__/`             |
|                                                                      |                                                                              |                                            |

| Item                          | Why                                                                                                                                                                                                         | Source |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| **JCS conformance + fuzzing** | RFC 8785 buggy-edge cases (Unicode escapes, number representation, key ordering with non-ASCII keys). Property-based tests via `fast-check` + golden vectors cross-checked against a non-TS implementation. | New    |


---

## Proposed V1.2 — "interop adapters + first non-TS SDK"

| Item                                                         | Why                                                                                                |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| **OAuth 2.1 AS adapter interface**                           | Define the contract, not the implementations; lets adopters plug any AS into `needs_authorization` |
| **OIDC bridge interface**                                    | Same pattern: contract upstream, provider definitions stay private                                 |
| **Community DID method packages**                            | `did:webvh` / `did:peer` / `did:jwk` shipped against the v1.1 resolver registry                    |
| **Second `SignatureSuite` implementation** (ES256 or ES256K) | Proves the abstraction in production; opens enterprise HSM adopters                                |
| **Python SDK**                                               | Matches what's already on the public docs site; conformance vectors guarantee parity               |
| **Go SDK skeleton**                                          | Same                                                                                               |

---

**Repo:** github.com/modelcontextprotocol-identity/mcp-i-core · **npm:** [`@kya-os/mcp`](https://www.npmjs.com/package/@kya-os/mcp) · **Spec portal:** modelcontextprotocol-identity.io · **DIF:** TAAWG
