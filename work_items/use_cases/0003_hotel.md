---
name: Use Case
about: Use this template to propose a use case be elaborated collectively.
title: "[UC] Finding and Booking a Hotel"
champion: Douglas Rice ( @douglascrice )
labels: usecase
tags: [ discovery, preferences, distributed transaction ]

---

## Summary

_Finding and Booking a Hotel_

### Driving User Story

Carol, who is planning a long weekend in New York City,
Enlists a set of AI agents to qualify suppliers and intermediaries which, 1.) following her needs and preferences, can 2.) identify multiple options,
can 3.) evaluate, 4.) recommend and 5.) optionally select the best option and 6.) complete the booking,
so that 7.) she gets a room that best meets her needs such as for location, price, or features.

## Context

- [x] I have looked for similar use cases and feel this issue is a distinct use-case, rather than best encoded as a variant or "alternate path" to an existing one.

### Related Use Cases  

- “Using Multiple AI Agents for a Corporate Purchase”:  some common issues, but additional complexities related to (a) complexity of preferences/requirements and the likelihood that iteration may be required to express them adequately, and (b) the presence of multiple intermediaries who may act on behalf of hotels or other intermediaries, or (importantly) pretend to do so fraudulently.

### Terminology

### Actors

- Purchaser: person planning the trip
- Discoverer: AI agent that finds potential Suppliers and Intermediaries and requests accommodation offers.
- Supplier: AI agent or human for a hotel (or other lodging provider) that is capable of proposing and confirming an accommodation product to Purchaser or an Intermediary.
- Intermediary: AI agent or human that does not provide accommodations but that can propose and confirm accommodations on behalf of a Supplier or another Intermediary. Includes most hotel brands, third party reservation services and booking engines, travel agents (online or traditional), bed banks, channel managers, distribution switches, visitor’s bureaus, and the like.
- Qualifier: AI agent that filters out unqualified Suppliers and Intermediaries and ranks qualified offers according to Purchaser’s needs and preferences
- Selector: AI agent or human that makes a selection from among the ranked qualified suppliers, ensuring compliance with policies set by the Purchaser
- Booker: AI agent that completes the booking, fulfilling requirements such as information on the Purchaser, payment, etc.
- Payer: AI agent that makes payment for the booking, if required at the time of booking

### Other Stakeholders

None in this variant.
If the Purchaser is on a business trip, there may be an additional requirement that the booking be made in compliance with corporate travel policy, in which case a Corporate Travel Manager would be a stakeholder.
If payment is to be made by a third party, then that third party would be an additional stakeholder as well.

## Flows

1. The Purchaser starts one or more Discoverers to identify and request proposals from Suppliers and Intermediaries offering accommodations that generally meet the Purchaser’s predefined needs and preferences (see below) and to retrieve product options.
    1. Each time one is found, a Qualifier agent is started to score the response.
1. Once a sufficient number of options have been scored, a Selector (Agent or human) chooses a proposal and instructs the Booking Agent to confirm it and record the contract terms and confirmation details.
1. If the contract terms require prepayment, then the Booking Agent invokes a Payer Agent to complete the payment.

### Example Preferences

- location
- dates
- style
- loyalty program
- features
- contract term

### Example Product Options

- room type
- room features
- price
- contract terms

### 0 - Preconditions

- A registry of hotels, brands, and other intermediaries that can book hotels.
- Access to information about the Supplier and/or Intermediary that may be needed to assess fit with the Purchaser’s needs (e.g., does the hotel have a pool; does the Supplier or Intermediary charge a fee for cancellations or modifications)
- A way to ensure that an Intermediary is authorized by any specific Supplier to accept bookings on its behalf, and conditions under which it can do so (e.g. must confirm with Supplier or another Intermediary prior to confirming to Purchaser)
- A means for matching Purchaser’s needs and preferences with attributes of a particular offering
- An agreed upon library of pricing and contract terms that hotels, brands, intermediaries, and agents all understand.

### 1 - Trigger

The Purchaser initiates the process by creating a set of requirements and preferences and starting one or more Discoverer AI agents.

### 2A - Happy Path

- The Discoverer agents find 200 hotels that meet the Purchaser’s basic requirements, such as within a certain radius of a location.
- The Discover identifies one or more Suppliers or Intermediaries that can sell each hotel, and requests proposals (generic or individualized) from each, using whatever qualifying mechanisms each endpoint supports (e.g. filtering by room or bedding type, refund policies, hotel features, etc.).
- The Qualifier uses these proposals (and possibly other data services) to eliminate options that fail to meet the Purchaser’s most important requirements.
- The Qualifier scores and ranks the proposals against the Purchaser’s detailed requirements and preferences.
- The Selector decides on a particular proposal and instructs the Booker to accept the proposal.
- If required, the Booker instructs the Payer to complete payment.
- The Booker provides confirmation to the Purchaser of the completed transaction.

### 2B - Alternative Paths

#### Discovery failure

There are no Suppliers identified that meet the basic requirements of the Purchaser (e.g. near the specified location).

#### Qualification failure

Suppliers are identified but fail to qualify based on more detailed requirements (e.g. must have a gym).

#### Qualification requires iteration

In some cases there may be further communications with the Supplier to refine a proposal (many hotels and intermediaries use a multi-step process, with a coarse filter used for initial inquiries and more detail provided at later stages).

#### Selection failure

Multiple qualified proposals are identified, but none are acceptable to the Selector.

#### Payment failure

Payer fails to complete a required payment.

#### Booking failure

The booking cannot be confirmed due to issues with the request (e.g. insufficient information), failure to process required payment, quoted product no longer being available, or other processing errors.

### 3A - Challenges and Key Risks

- Discoverer agent fails to find all relevant options because of hotels that are not listed in a trusted registry.
- Qualifier agent is unable to get sufficient information to properly assess the fit of particular Suppliers, Intermediaries, or proposals vs. Purchaser’s requirements and preferences.
- Discoverer agent accepts proposals from fraudulent hotels because of inaccurate registries or inadequate vetting by intermediaries
- Purchaser fails to describe all relevant needs and preferences, leading to Discoverer and Qualifier either identifying poor options, or failing to identify good ones.
- Payer pays an incorrect amount, pays the wrong party, or fails to pay at all.
- An Intermediary accepts a booking on behalf of a Supplier or another Intermediary, but delivery to the other party fails or is incorrect or incomplete.

### 3B - Success Criteria

A valid booking is made with a qualified Supplier or Intermediary and confirmed to the Purchaser.

### 3C - Acceptable Outcomes

A valid booking is made with a qualified Supplier, or is made with an Intermediary and correctly delivered to any upstream Intermediaries and to the Supplier. Purchaser receives a booking confirmation.

## References

### Prior Art

Some material reused from "Using Multiple AI Agents for a Corporate Purchase" use case.

### Annotated Bibliography
