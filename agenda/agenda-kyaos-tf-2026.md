# TAAWG - KYA-OS Task Force

- future topics
    + statusList2021 - does it need to be public/global? should the spec encourage non-public URL usage of statusList2021, or authN'd/internal-only/RS-side revocation anyways, à la UCAN/ZCap?
        + is this a quick PR or a directional thing? do we need more donations/a pluggable revocation mechanism?

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
