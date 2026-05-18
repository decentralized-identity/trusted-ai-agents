# TAAWG - KYA-OS Task Force

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
    - [ ] BF - announce 14-day review people 
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
