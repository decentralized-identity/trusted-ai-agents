---
name: Use Case
about: Use this template to propose a use case be elaborated collectively.
title: "[UC] Supply Chain Research"
champion: Alan Karp ( @alanhkarp )
labels: usecase
tags: [ commerce, research, international ]

---

## Summary

_Finding a Supplier and Completing a Deal_

### Driving User Story

As the person responsible for buying power cords for the rice cookers your company makes,
You enlist a set of specialized AI agents to
1.) qualify suppliers (validate that they meet reputation and licensing thresholds),
2.) negotiate with them on a supplier contract with multiple terms and conditions,
3.) select a supplier and a backup supplier, and
4.) send them the company's default contracts,
5.) which get negotiated, and
6.) when enough negotiated, validated vendors have been identified, some kind of auction selects one,
without limiting potential suppliers based on whether they negotiate manually (human-to-human), digitally (classical APIs), or agentically, so that my company gets the best deal from a reliable supplier.

## Context

- [ x] I have looked for similar use cases and feel this issue is a distinct use-case, rather than best encoded as a variant or "alternate path" to an existing one.

### Related Use Cases  

### Terminology

### Actors

- Purchaser: person responsible for purchasing power cords (primary)
- Discoverer:  AI agent that finds potential suppliers
- Qualifier: AI agent that filters out unqualified suppliers
- Negotiator: AI agent that negotiates terms and conditions
- Auctioneer: AI agent that runs an auction among companies that have agreed to terms and conditions
- Closer: Person or AI agent that completes the contract
- Monitor: AI agent that monitors that the contract is fulfilled according the agreed upon terms
- Payer: AI agent that makes payment according to the terms of the contract if the Monitor approves
- Dispute Handler: Human or AI agent that deals with conflicts

### Other Stakeholders

- CFO: Responsible for determining acceptable financial terms
- Product Owner: Responsible for determining required number of power cords per time period
- Engineering Lead: Set parameters for power cords, e.g., length, rating, plug types
- Legal: Responsible for approving contracts and dealing with disputes

## Flows

1. The buyer starts one or more AI agents to discover suppliers of power cords that meet the engineering requirements.  
   1. Each time one is found, a Qualifier agent is started to review that company's qualifications.  
2. Once a company is qualified, a Negotiator agent interacts with the company (human, software, or AI) to reach a set of terms that the buyer requires and the supplier is willing to provide.
   1. May require manual steps or human-in-the-loop approvals
   2. May be async/parallelized
3. Once a number of suppliers are identified, they are sent to an [agentic] Auctioneer process where they can bid on the business.  
4. The winner is directed to a Closer that finalizes the deal.

This process can be ongoing if the contracts are short term.

### 0 - Preconditions

- A place for companies to advertise that they sell power cords of various types.
- A way to evaluate the reliability of potential suppliers, e.g., BBB or UL.
- An agreed upon negotiation protocol.
- An agreed upon auction protocol.
- A place to bring disputes for resolution.

### 1 - Trigger

The buyer initiates the process by creating one or more Discoverer AI agents.

### 2A - Happy Path

- The Discoverer agents find 10 potential suppliers, 8 of which pass qualification.
- 7 of the qualified suppliers complete negotiation successfully.
- The auction selects a primary and a backup supplier for each type of power cord.
- A contract is signed with the primary supplier.
- Power cords are delivered on time and on budget.

### 2B - Alternative Paths

- Discovery failure: No company sells power cords that meet all the requirements.  
  - Either engineering must redesign the rice cooker or the company will have to make its own power cords.
- Qualification failure: No company that sells power cords meets the requirements.
  - The Product Owner must relax the conditions in consultation with Engineering, or the company will have to make its own power cords.
- Negotiation failure: No agreement is reached with any potential supplier.
  - The Product Owner in collaboration with the CFO and Engineering will have to change the product requirements.
- Auction failure: The auction closes with no acceptable bids.
  - The Product Owner in collaboration with the CFO and Engineering will have to change the product requirements.
- Delivery failure: The power cords are not delivered as agreed to.
  - Invoke Dispute Resolution
  - Use backup supplier

### 3A - Challenges and Key Risks

- Discoverer agent finds inappropriate companies.
- Qualifier misclassifies companies, rejecting ones that should pass or accepting those that don't.
- Negotiator agrees to terms it shouldn't or doesn't agree to terms it should.
- Auctioneer terminates the auction so that the terms are not the best the company can get.
- Closer agrees to a contract other than what was negotiated.
- Monitor fails to detect violations or reports spurious violations.
- Payer pays an incorrect amount, pays the wrong supplier, or fails to pay at all.
- Dispute Handler fails to represent the company's best interests.

### 3B - Success Criteria

A valid contract is signed with a qualified supplier that delivers on time and on budget.

### 3C - Acceptable Outcomes

A valid contract is signed with a qualified supplier that is sometimes late with deliveries by an amount that doesn't affect product delivery.

## References

### Prior Art

Note: this use case comes from the proposer's experience at Hewlett Packard, which saved $170M/year by changing the way it ran auctions for power cords it was buying for its computers.

### Annotated Bibliography
