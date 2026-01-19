---
name: Use Case
about: Use this template to propose a use case be elaborated collectively.
title: "[UC] Calendaring"
champion: andorsk ( @andorsk )
labels: usecase
tags: [ state management, coordination, distributed transaction ]

---

## Summary

I want to be able to negotiate calendar invites with other users via my agent.

Demo App
<img width="720" height="398" alt="Image" src="https://github.com/user-attachments/assets/d9cc992b-67e3-4919-b511-be355ddf000d" />

Problem To Solve 
<img width="732" height="408" alt="Image" src="https://github.com/user-attachments/assets/4e2b731f-cd5b-46fa-8893-4e7f1af45aaf" />

This is work expanding on a workshop I put together here:  [google doc](https://docs.google.com/presentation/d/1FmHqqIsZOZ3zWnd0SnjR2dEYvYxa8iM0sNkJAl_hG_w/edit?slide=id.g39881ca7abc_0_197#slide=id.g39881ca7abc_0_197)

### Driving User Story

**As a attendee at an event,**
**I want book calendar invites,**
**With other attendees at an event,**
**So that I can easily have follow up calls later*

## Context

This use-case extends prior work on agentic negotiation protocols (A2A, MCP) and authenticated delegation frameworks that let an agent act on behalf of a human with scoped authorization.

It focuses on practical post-event coordination, where multiple independently controlled agents can find mutually acceptable times while preserving privacy, consent, and accountability.

- [x] I have looked for similar use cases and feel this issue is a distinct use-case, rather than best encoded as a variant or "alternate path" to an existing one.

### Related Use Cases  

### Terminology

### Actors

- **User Agent (A)** — negotiates meetings on behalf of a human attendee.
- **Counterparty Agent (B):** representing another attendee.
- **Calendar Service(s):** Google Calendar, Outlook, or decentralized scheduling API.
- **Registry / Discovery Index:** finds agent endpoints and associated DIDs.
- **PEP** : enforces access control, delegation scope, and logging.
- **User(s)**: human participants approving or delegating scheduling authority.

### Other Stakeholders

- Event organizers (who may broker the first discovery handshake)

## Flows

### 0 – Preconditions

- Each attendee has an authenticated **agent**.
- Each agent is authorized to perform scheduling actions within a defined scope.  
- Calendar APIs (e.g., Google, Outlook, or decentralized calendar endpoints) are available and accessible to the agents.  
- A **discovery index or registry** exists for agents to resolve each other’s endpoints and capabilities.  
- A **PDP* enforces delegation, authentication, and audit logging.

### 1 – Trigger

- After an event, a user instructs their agent:  
  > “Find a time to meet with [Person/Organization X].”
- Alternatively, agents may autonomously initiate negotiation when context suggests mutual value (e.g., “We found mutual valuable!”).

### 2A – Happy Path

1. **Discovery**
   - Agent A queries the **Registry / Index** to locate Agent B’s endpoint, DID, and declared capabilities.
2. **Negotiation Initiation**
   - Agent A sends a **meeting proposal** (available slots, duration, medium, context) to Agent B.
3. **Preference & Policy Evaluation**
   - Agent B checks its calendar, user preferences, and policy constraints.
   - If incompatible, Agent B proposes an alternate slot.
4. **Iterative Negotiation**: 
    - Agents exchange proposals until they reach a mutually acceptable time.
6. **Invite Confirmation**   - Both agents create or update the calendar entry through their local **Calendar Service API**.
   - The resulting event includes human participants and delegation credentials.
6. **Audit & Logging**
   - The **Gateway** records the transaction, including timestamps, policy decisions, and digital signatures.

### 2B – Alternative Paths

#### a) Policy Constraint Conflict

- An organization’s policy forbids auto-scheduling without explicit human approval.  
- The agent pauses negotiation and escalates to the user.

#### b) Identity Resolution Failure

- Agent B’s DID cannot be verified or resolved from the registry.  
- Agent A aborts negotiation and notifies the user.

#### c) Manual Fallback

- Negotiation partially completes, but no final slot is agreed upon.  
- Agents generate a **shared scheduling link** or fallback to manual coordination.

### 3A – Challenges and Key Risks

- **Delegation Scope Drift:** Agent exceeds its authorized actions (e.g., recurring or multi-party meetings).  
- **Privacy Leakage:** Calendar metadata reveals sensitive information such as affiliations or intent.  
- **Trust Boundary Mismatch:** Organizational policies differ in allowed scheduling methods.  
- **Malicious or “Bad” Calendar Agents:** Rogue or buggy agents spam or misrepresent identity.  
- **Protocol Interoperability:** Well documented APIs and data models would make this a lot closer to deterministic.

### 3B – Success Criteria

- Meeting successfully appears on both participants’ calendars.  
- Human consent is preserved and verifiable.  
- Delegation credentials validated through cryptographic proof.  
- Negotiation latency under one minute for typical scheduling.  

### 3C – Acceptable Outcomes

Meeting scheduled and confirmed by both agents. Agent is a good actor relative to the user and desired to be met by the user.

## References

### Prior Art

- This is work expanding on a workshop I put together here:  [google docs presentation](https://docs.google.com/presentation/d/1FmHqqIsZOZ3zWnd0SnjR2dEYvYxa8iM0sNkJAl_hG_w/edit?slide=id.g39881ca7abc_0_197#slide=id.g39881ca7abc_0_197)
- Code here: [github link - The-AI-Alliance/ai-agent-workshop](https://github.com/The-AI-Alliance/ai-agent-workshop/tree/main/day2)

### Annotated Bibliography
