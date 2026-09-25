# Global Ride — Product & Engineering Showcase

> **What if a ride-hailing marketplace could create a more predictable economic relationship with the people supplying the rides?**

Global Ride is a **working ride-hailing prototype in pre-validation**. It combines a Flutter mobile experience with a Python/FastAPI backend and Google Maps services to demonstrate a connected passenger ↔ driver journey.

This repository is intentionally a **showcase, not a source-code mirror**.

[View the demo walkthrough](DEMO.md) · [Read the business thesis](BUSINESS_THESIS.md) · [See the pilot framework](PILOT_VALIDATION.md)

---

## The story

Ride-hailing looks simple from the passenger seat: choose a destination, request a car and arrive. The difficult part is the marketplace behind that interaction — aligning passengers, drivers, operators and the platform while maintaining availability, reliability and sustainable economics.

Global Ride began with a business question rather than a UI exercise:

**Can that relationship be designed differently while preserving the experience passengers expect?**

The first milestone was execution. Instead of stopping at a pitch deck, the idea became a working prototype with separate passenger and driver flows.

The next milestone is evidence: validate supply, demand, local marketplace liquidity, economics and regulatory feasibility under real conditions.

## Working product journey

**Passenger**

Destination search → route calculation → Economy / Comfort / XL → ride request → driver matching → pickup → active ride → completion → rating & tip → demo payment → receipt

**Driver**

Online → incoming request → accept → drive to pickup → passenger pickup → start ride → active ride → complete

### Running Android demo

<p align="center">
  <img src="assets/destination-search.jpg" width="320" alt="Global Ride destination search showing Vienna Airport autocomplete" />
</p>

The screenshot is from the running Android prototype, not a design mockup.

## What the prototype demonstrates

- Passenger and driver application modes
- Destination search and place autocomplete
- Google Maps integration and location-aware routing
- Economy, Comfort and XL ride categories
- Ride request and driver acceptance workflow
- Pickup, active-trip and completion states
- Passenger rating, comments and tipping
- Demo payment and receipt flow
- Flutter ↔ FastAPI HTTP integration
- Persistent ride/domain data architecture
- Separated user, driver, operator and vehicle concepts
- Modular backend structure across API, schema, service, model and database layers

## Architecture

```text
┌──────────────────────────┐
│      Flutter Client      │
│ Passenger / Driver flows │
└─────────────┬────────────┘
              │ HTTP
              ▼
┌──────────────────────────┐
│     Python / FastAPI     │
│ API · Services · Schemas │
└───────┬─────────┬────────┘
        │         │
        ▼         ▼
  Domain/Data   Maps/Places
    Layer       Route Services
```

| Area | Technology |
| --- | --- |
| Mobile | Flutter / Dart |
| Backend | Python / FastAPI |
| Mapping | Google Maps Platform |
| Data architecture | SQLAlchemy / PostgreSQL-oriented |
| Development | Git / GitHub |

## Investor snapshot

**Stage:** working prototype / pre-validation  
**Product proof:** connected passenger and driver ride lifecycle demonstrated end to end  
**Business question:** can a different platform-cost relationship improve alignment while still supporting sustainable marketplace economics?  
**Validation focus:** local liquidity, active supply, repeat passenger demand, contribution economics and regulatory feasibility

### De-risked so far

- The core passenger and driver journeys can be implemented and demonstrated.
- Mobile, backend, maps/location and ride-state components work as a connected prototype.
- The commercial hypothesis is concrete enough to model and test.

### Still unproven

- driver/operator willingness to adopt the proposed commercial relationship;
- ability to create dense local supply and repeat passenger demand;
- sustainable acquisition, support and operating economics;
- regulatory structure for a live commercial launch;
- retention, utilization and contribution economics under real usage.

**The prototype is evidence of execution. It is not presented as evidence of market traction.**

## Product thesis

Global Ride is exploring whether an alternative platform-cost structure can create stronger alignment for active supply while still funding a sustainable marketplace.

That is a **hypothesis to validate**, not a claim of superiority.

The detailed pricing formula, thresholds, unit-economics assumptions and commercialization mechanics are deliberately not published here.

## Validation philosophy

A marketplace is not successful because it has registrations. The meaningful signals are active supply, completed rides, passenger repeat behavior, acceptance/completion rates, service availability and contribution economics.

The planned validation sequence is:

1. **Product reliability** — ensure software defects do not distort the test.
2. **Local liquidity** — concentrate supply and demand rather than pretending to launch everywhere.
3. **Behavioral evidence** — measure actual usage and repeat behavior.
4. **Economic evidence** — test realistic revenue against acquisition, support and operating costs.
5. **Expansion** — widen geography only if the earlier gates survive.

## What stays private

To make the project visible without giving away the implementation, this public repository deliberately excludes:

- complete application source code;
- credentials, API keys and environment configuration;
- internal endpoint implementations;
- detailed pricing thresholds and charging formula;
- private unit-economics assumptions and contribution targets;
- commercially sensitive rollout and partner mechanics.

## Two reasons to start a conversation

### Engineering teams

Global Ride demonstrates product-oriented engineering across mobile UI, backend APIs, maps/location services, domain modelling and end-to-end workflow validation.

The complete source is maintained privately and can be considered for **controlled technical review** when appropriate.

### Investors & strategic partners

The larger question is whether the product thesis can become a sustainable marketplace. Detailed economics, pilot assumptions and commercialization mechanics are reserved for private discussion.

## Public communication standard

Global Ride describes its own product and hypotheses. It does not make claims about the quality, motives or conduct of identifiable competitors. Illustrative economics are labelled as scenarios, and unvalidated assumptions are presented as hypotheses rather than facts.

---

### About the developer

Global Ride is a hands-on portfolio and product project by **Bogdan Dulgheru**, covering product thinking, architecture, implementation, validation, debugging and testing.

**Status:** active development · working prototype · pre-validation