---
name: Use Case
about: Use this template to propose a use case be elaborated collectively.
title: "[UC] Personal Intelligence Agent"
champion: Tom Jones ( ? )
labels: usecase
tags: [ commerce, research, international ]

---

## Summary

_Creating an intelligent user agent that can handle many simple queries locally._

### Driving User Story

An intelligent agent that is closely-controlled, highly-trusted, and with access to extensive, sensitive memory is powerful, but the control, the trust, and the governance of that memory are paramount here.

### Design Goals

To optimize for these properties, we imagine a user that:

1. Retains local possession of their personal data, and runs inference locally. (See [Alternate Flows](#2b---alternative-paths) for variants)
2. Requires attestations of authenticity and integrity to install or update their inference model and tooling.
3. Writes and maintains nuanced policy for what, if any, data (both personal data inputs and accrued context) is shared when an external agent (or other process) is delegated.
4. _Treasures their privacy and would like as little as possible to be inferable about them from agent<>external system communications or from other processes on their device._
    * added by bumblefudge

## Context

- [x] I have looked for similar use cases and feel this issue is a distinct use-case, rather than best encoded as a variant or "alternate path" to an existing one.

### Related Use Cases  

Similar in shape to [hotel](./0003_hotel.md) or [calendaring](./0002_calendaring.md) use-cases, but with higher stakes for misbehavior and more attention to the policy mechanics and trust boundary issues inherent in delegating from highly-trusted local agent to less-trusted, external agents.

### Terminology

- intelligent agent - an agent that has significant agency, significant access to persisted context (i.e. "memory"), and significant policy
- wallet - distinct interface for getting consent from user, authoring policy changes, and tracking external data sharing
- consent - for the purposes of this usecase, interactive confirmation or additional input to policy from the primary actor, requested by the intelligent agent before proceeding
- memory - context persisted and accrued over time in the intelligent agent
- session context - an asynchronous yet ephemeral interaction that ends and is forgotten unless policy or consent adds to memory

### Actors

1. **Primary Actor**:
    * The user who holds a device and is the initiator of the context for a query.
1. **Secondary Actors**
    * In all cases, the source of the model and tooling that is used locally by primary actor.
    * An external (e.g. web- or API-based) agentic inference engine (as needed).
        * Source of that model and tooling.

### Other Stakeholders

This use-case is simplified to focus on policy and data governance, but other stakeholders could be added to deepen those issues (See [Alternate Flows](#2b---alternative-paths)).

## Flows

### 0 - Preconditions

1. The human is the holder of some digital device that has effective secret management keeping all secrets on-device.
    * For simplicity, we can call that device "the computer" and assume conventional personal computing boundaries.
    * For simplicity, we can assume a secure execution environment, modern keyrings, etc. are responsible for secrets like private keys
    * we also assume that the agent cooperates in keeping these on-device.
2. The human is presumed to have configured a default set of policies that can be changed for each context if time is taken to target specific providers.
3. The human can trust the integrity and authenticity of the software (model and tooling) comprising their agent.
    * For simplicity, we can assume current best practices for software supply chain attestations suffice, i.e. all software signed and sourced by a supplier trusted by the human user, and all signatures checked by package manger, OS, etc.
4. In addition to preconditions 1 and 3, a distinct user interface is used that bridges secrets from 1, the software from 3, and real-time user consent any time policy justifies it or is ambiguous/fails.
    * For simplicity, we can refer to this interface as "the wallet", and we can imagine it as a multi-device, strongly authenticated interface like a DID wallet, google/apple wallet, etc. 
    * In particular, the Wallet controls write access to the local model specifically.
    * The user will have full control of the wallet which is needed to set and control policy as a decision point or PDP.

Negative conditions:

1. This model does not consider a distributed secure execution environment where the human could have the same secrets shared by multiple, otherwise independent, devices. An [alternate flow](#2b---alternative-paths) could be added to this effect if it were desirable to design such an environment with equivalent trust and security guarantees, but such design would be a significant undertaking.
1. The user will NOT necessarily assume an long-lived identifier that is used for any purpose other than maintaining a context with a cloud agent. See [design goal](#design-goals) #4.


### 1 - Trigger

The user has a question to ask which will return data to the user and may instantiate commitments on the user’s behalf.

### 2A - Happy Path

1. The user has instantiated the personal intelligent agent and provided a set of default policies to be used.
2. The user keys a question into the personal intelligent agent.
    * This initiates a session context.
3. If the agent requires access to any resources that are not available by the default policy it may request additional resources accessible only to this session context. 
    * This may include a suggestion to use a cloud agent or other interaction with outside agents or APIs.
4. [Optionally] the local agent accesses the external agents or APIs (e.g. a cloud agent).
    * The cloud agent may request access to resources that it needs to create a response, including a token for a pre-existing or new subscription, or data resources not already provided.
    * This might use OODA logic/logging, or some other policy/authZ structure.
5. The local agent attempts to respond to the user query interactively.
6. The user may continue the context by providing additional queries (recursing this flow) within a timeout window for further interaction.
7. Once user signals success or timeout is reached, wallet logs transaction in audit logs.
8. [Optionally] agent may recommend additions to memory as a result of these interactions, which require user consent and/or policy.
9. Session context is cleared or "garbage collected" via timeout or user input.

### 2B - Alternative Paths

1. **Consent Expired**: If session policy includes a timeout, and this is met before Agent prompts user to renew.
2. **Policy Denied**: If agent actions are denied by policy, notification (which should include reason and alternatives) is presented to user.
3. **Network Failure**: Agent retries or defers request.
4. **Streams Content**: Agent provides content or a lesson that enables user inputs.
5. **Initiates Action**: Agent turns off lights to enable viewing content.
6. **Consenter's Regret**: Human user realizes too late that they authorized too much data-sharing with an external service, or with the wrong external service. Studies logs in wallet, decides to revoke/reverse authorization, and takes some action to request deletion/refund/etc.

### 3A - Challenges and Key Risks

### 3B - Success Criteria

1. Record is securely delivered from local and cloud agents
2. Audit trail is updated - this contains as little user private data as possible, but enough metadata to understand WHAT data was exfiltrated to WHICH services.
3. User retains as much control as possible over data usage internally
    * e.g., session context lifecycle, memory management if applicable. 
4.  User retains as much control as possible over data usage externally 
    * e.g., receive from external counterparties deletion attestations, ephemeral workflow attestations, actionable contracts, escrows/penalties, etc.

### 3C - Acceptable Outcomes

### 3D - Error Cases

1. Invalid delegation - the agent cannot acquire the credentials needed to initiate a session context
2. Revoked or expired credentials
3. API schema or policy mismatch 
    * fail by default if policy not confidently known or processable?

## References

- Threat Modeling Report for Personal Intelligent Agent = Contains data flow diagram (forthcoming attachment)

### Prior Art


### Annotated Bibliography
