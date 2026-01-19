# Trusted AI Agents Working Group (WG) — Use Case Clusters & Architectural Components

This document groups the use cases into clusters and maps them to key architectural components.  
It supports the definition of DIF work items and shared architectural building blocks.

---

## Use Case Clusters

| PR | Author | Use Case | Merge | Cluster | Cluster Name |
|----|---------|-----------|--------|----------|---------------|
| 15 | @andorsk | Book a Calendar with Agents |  | 1 | Multi-Agent Negotiation & Discovery |
| 17 | @douglascrice | Finding and Booking a Hotel | TO BE MERGED | 1 | Multi-Agent Negotiation & Discovery |
| 14 | @alanhkarp | Using Multiple AI Agents for a Corporate Purchase | TO BE MERGED | 1 | Multi-Agent Negotiation & Discovery |
| 19 | @ngallo | Dynamic Policy Bundles and Federated Machine Identity for Asynchronous Industrial Meshes |  | 2 | Policy, Delegation & Compliance |
| 3 | @ngallo | Adaptive Error Handling in Multi-Step API Workflows |  | 2 | Policy, Delegation & Compliance |
| 12 | @alanhkarp | Buy a Gift for a Tween |  | 3 | Personal AI Agents |

Below is a summary of the use case clusters, their focus areas, and typical components involved.

| Cluster | Focus | Typical Components |
|----------|--------|--------------------|
| **1 – Multi-Agent Negotiation & Discovery** | Transactional coordination, scheduling, procurement | Agentic Negotiation, Discovery, Identity, Decision Trail |
| **2 – Policy, Delegation & Compliance** | Policy enforcement, attestation, resilience, federation | Trust Fabric, Workflow Orchestration, Decision Trail |
| **3 – Personal AI Agents** | Consent, privacy, delegated autonomy | Agentic Identity, Policy, Decision Trail |

## Architectural Components Mapping

| Use Case | Agentic Identity & Control Authority | Trust Fabric, Attestation & Policy | Decentralized Discovery & Trust Registry | Adaptive Workflow Orchestration | Agentic Negotiation, Commerce & Value Exchange | Verifiable Decision Trail |
|-----------|--------------------------------------|-----------------------------------|------------------------------------------|---------------------------------|------------------------------------------------|---------------------------|
| Book a Calendar with Agents | X | X | X | X | X | X |
| Finding and Booking a Hotel | X | X | X | X | X | X |
| Using Multiple AI Agents for a Corporate Purchase | X | X | X | X | X | X |
| Dynamic Policy Bundles and Federated Machine Identity for Asynchronous Industrial Meshes | X | X | X | X |  | X |
| Adaptive Error Handling in Multi-Step API Workflows | X | X | X | X |  | X |
| Buy a Gift for a Tween | X | X | X |  | X | X |

---

### Architectural Component Summary

#### Agentic Identity & Control Authority

The scope of the **Agentic Identity & Control Authority** includes defining and managing identities for AI agents — both human and non-human.  
This includes highlighting the limitations of centralized identity providers and the need for decentralized, verifiable identity solutions.

This work explores how **DIDs (Decentralized Identifiers)** are involved and how **delegation of authority** can be achieved through **Verifiable Credentials**, **ZCAP-LD**, and similar mechanisms.  
It also aims to identify potential extensions or new protocols required to support *agentic identity* and autonomous control.

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| O1 | Define Agent Identity Model | Establish a model for representing human and non-human agent identities using DIDs and VCs. | Common DID-based schema for AI and software agents. |
| O2 | Explore Delegation Mechanisms | Evaluate ZCAP-LD and other decentralized delegation models to enable verifiable control and consent. | Proposal or reference implementation of delegation patterns. |
| O3 | Identify Gaps in Existing Standards | Analyze current DIF and W3C specs to identify missing primitives for agentic identity. | Input for new work item or extension proposal. |
| O4 | Develop Reference Architecture | Map agent identity, control authority, and delegation into the broader Trusted AI Agent architecture. | Draft diagram and narrative for DIF deliverable. |

#### Trust Fabric, Attestation & Policy

The **Trust Fabric** is the glue and core enabler for secure and compliant interactions between AI agents.  
It defines **trust boundaries**, **attestation mechanisms**, **policy enforcement points**, and **compliance frameworks** that support zero-trust and verifiable collaboration.

This work identifies where **centralized trust models** (e.g., traditional IAM or SSO) break down and explores how **decentralized trust frameworks** can provide stronger, federated, and more adaptable alternatives.

The analysis includes **microsegmentation**, **service meshes**, and **federated architectures** across both **synchronous communication** (HTTPS, gRPC) and **asynchronous channels** (message queues, event streams).

Recognizing that enterprise adoption cannot be a "big bang" shift, the Trust Fabric must be **interoperable** — capable of bridging **existing enterprise security stacks** (e.g., SPIFFE/SPIRE, SSO, OIDC) with **decentralized identity and trust models** (DID, Verifiable Credentials, Attestations).  
This enables the seamless integration of **verifiable proofs** and **agent attestations** into modern cloud-native and zero-trust infrastructures.

Additionally, the Trust Fabric must support **trust continuity at the point of consumption**, ensuring that verifiable trust is maintained as data and actions propagate across domains and services.  
This implies modeling a **Trust Chain** that links identity, attestation, and policy decisions across each hop of an interaction — from the originating agent to downstream consumers — preserving verifiability and accountability end-to-end.

To support secure, interoperable agent communication, the Trust Fabric should adopt also messaging as a **trusted transport protocol**.  

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| TF-1 | Define the Trust Fabric Architecture | Establish the core trust boundary and policy enforcement model for secure multi-agent interactions. | Architectural blueprint for decentralized trust interoperability. |
| TF-2 | Bridge Centralized and Decentralized Trust Models | Design interoperability between SPIFFE/SSO and DID-based identity and attestation systems. | Protocol or adapter specification enabling hybrid trust. |
| TF-3 | Integrate Attestation and Verifiable Credentials | Define how agents use verifiable credentials and attestations to prove compliance and trustworthiness. | Reference implementation for verifiable agent trust. |
| TF-4 | Analyze Cloud-Native & Federated Environments | Study trust enforcement across microsegmentation, service meshes, and event-driven architectures. | Guidelines for implementing trust in real-world enterprise meshes. |
| TF-5 | Support Gradual Enterprise Adoption | Ensure the Trust Fabric can be deployed incrementally, coexisting with current enterprise perimeter security. | Migration path and integration roadmap for enterprises. |
| TF-6 | Enable Trust Continuity at Consumption | Ensure that trust remains verifiable when data or actions move across domains and are consumed by different agents. | Specification for end-to-end trust propagation and validation. |
| TF-7 | Model the End-to-End Trust Chain | Define a model that connects identity, attestation, and policy decisions across the full interaction path. | Trust chain framework linking actors, attestations, and enforcement points. |
| TF-8 | Integrate Messaging for Secure Agent Communication | Leverage messaging as a trusted, end-to-end encrypted messaging layer for exchanging trust evidence and policy artifacts between agents. | Reference pattern for verifiable, interoperable agent-to-agent messaging. |

#### Verifiable Decision Trail

Agents operate very fast and can make deep autonomous decisions.  
Monitoring alone is not enough — agents need to produce a **decision log** for auditing, accountability, and compliance.  

The goal is to define a **decentralized standard** for verifiable decision logs that extends traditional observability with cryptographic trust and provenance.  
Each decision entry should form part of a **trust chain**, maintaining **trust continuity** as information and actions move across agents, domains, and systems.  

Beyond compliance, verifiable decision trails enable **risk and anomaly detection** — allowing organizations to detect abnormal, biased, or unsafe agent behaviors while preserving privacy and accountability.

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| VD-1 | Define Verifiable Decision Log Model | Specify a common, minimal schema for recording agent decisions and outcomes. | Draft specification for decision log structure. |
| VD-2 | Ensure Integrity and Verifiability | Define how each log entry is signed, hashed, and linked to the agent’s DID. | Standard for tamper-evident and DID-bound logs. |
| VD-3 | Support Trust Continuity | Maintain verifiability when logs move or are shared across domains. | Model for chained proofs and end-to-end trust. |
| VD-4 | Enable Secure Exchange via messaging | Use messaging for transmitting logs and proofs between agents securely. | Messaging profile for trusted log exchange. |
| VD-5 | Address Privacy and Selective Disclosure | Allow redacted or scoped sharing of decision data using VC/SD-JWT patterns. | Privacy-preserving mechanism for verifiable logs. |
| VD-6 | Enable Risk and Anomaly Detection | Use decision trails to identify abnormal or non-compliant agent behaviors in real time. | Framework for verifiable risk and anomaly signals. |

#### Decentralized Discovery & Trust Registry

In a decentralized and dynamic agentic ecosystem, **discovery** and **trust registries** are essential.  
Agents must be able to discover each other, verify capabilities, and establish trust relationships without relying on centralized directories.  
These registries should be **anchored to DIDs** and leverage **verifiable data** to ensure authenticity, interoperability, and transparency.  
The scope is to define a **new decentralized discovery and trust protocol** aligned with DIF standards.

This layer should build on top of the **Trust Fabric**.

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| DR-1 | Define Decentralized Discovery Protocol | Specify how agents discover other agents and services using DIDs. | Protocol specification for decentralized discovery. |
| DR-2 | Establish Trust Registry Model | Create a registry format for verifying agent credentials, capabilities, and reputations. | Trust registry schema and verification model. |
| DR-3 | Ensure Interoperability | Align with existing DIF, W3C, and ToIP standards for DIDs and VCs. | Compatibility matrix for cross-ecosystem use. |
| DR-4 | Support Dynamic and Federated Environments | Allow trust registries to federate and update in real time. | Model for federated and adaptive trust registries. |
| DR-5 | Integrate with Trust Fabric | Use the Trust Fabric to bridge Centralized and Decentralized Trust Models. | Interoperable layer aligned with decentralized trust. |

#### Adaptive Workflow Orchestration

AI agents operate as **distributed systems** that must coordinate complex, multi-step workflows.  
These workflows can be implemented through **orchestration** (centralized coordination) or **choreography** (decentralized collaboration).  
Orchestration requires persistent state and recovery mechanisms, while choreography depends on asynchronous communication patterns and shared context propagation.

Both models face challenges related to **resilience**, **error handling**, and **token continuity**.  
A key risk is the emergence of an *Internet of Shared Credentials*, where agents persist credentials in long-lived secret stores.  
When credentials are no longer ephemeral, the **trust and security guarantees of zero-trust** systems degrade.

This layer should build on top of the **Trust Fabric**, ensuring verifiable, ephemeral, and policy-governed workflow execution across distributed agent environments.

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| WO-1 | Define Workflow Coordination Patterns | Specify orchestration and choreography models for multi-agent systems. | Common model for distributed agent workflows. |
| WO-2 | Ensure Resilience and Error Handling | Support recovery, retries, and adaptive rollback across steps and domains. | Specification for reliable and self-healing workflows. |
| WO-3 | Enforce Ephemeral Credential Use | Prevent long-lived credentials by integrating token rotation and short TTLs. | Policy for secure, ephemeral authorization. |
| WO-4 | Integrate with Trust Fabric | Use the Trust Fabric for verification, attestation, and policy enforcement. | Interoperable layer aligned with decentralized trust. |

#### Agentic Negotiation, Commerce & Value Exchange

**Agentic systems** introduce a new class of economic actors — autonomous agents capable of negotiation, commerce, and value exchange on behalf of humans or organizations.  
To support this, we need **new primitives and protocols** that enable trusted, verifiable, and privacy-preserving transactions between agents.

The goal is not just digitalization of existing markets, but **true market decentralization** — where agents can interact, negotiate, and exchange value without centralized intermediaries.  
These interactions must preserve privacy, fairness, and enforceable commitments through **capability tokens**, **verifiable agreements**, and **policy-aware negotiation** mechanisms.

Below are the key objectives for this component:

| ID | Objective | Description | Expected Outcome |
|----|------------|--------------|------------------|
| NC-1 | Define Agentic Commerce Primitives | Identify the core protocols and objects for negotiation, contracts, and value exchange. | Foundational spec for agentic transaction models. |
| NC-2 | Support Verifiable and Privacy-Preserving Transactions | Enable agents to exchange offers and commitments using verifiable, privacy-safe proofs. | Mechanism for trusted and confidential transactions. |
| NC-3 | Introduce Capability-Token Based Negotiation | Use capability tokens (ZCAPs) to grant and prove limited negotiation or execution rights. | Token model for controlled and auditable delegation. |
| NC-4 | Enable Decentralized Market Interactions | Allow agents to form and participate in markets without centralized brokers. | Protocol for decentralized, trust-based commerce. |

---
