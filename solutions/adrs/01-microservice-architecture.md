# Using a Microservice Architecture

## Status

Accepted

## Context

Microservices is suited for our application as it provides benefits for evolvability, performance, and scalability.

In the book Microservice Architecture, the definition of microservices includes the architecture element:

> A microservice is an independently deployable component of bounded scope that supports interoperability through message based communications.
> It is a style of engineering highly automated, evolvable software systems made up of capability aligned microservices.

## Decision Drivers

- Which architecture scores highly on the characteristics identified as important in our Architecture Analysis:
  - Performance
  - Scalability
  - Extensibility
- For immediate and medium business needs for Fave Trip, which architecture can deliver the most value with consideration for future functionality additions?

## Decision.

We decided to adopt a microservice architecture style for Fave Trip.
The distributed design of this architecture style will allow us to maximise with potential of scability, evolvability and availability.

## Consequences

### Pros

- Extensibility / Evolvability: New functions or features can be decoupled into smaller contained services to facilitate rapid iterations.
- Scalability: Defining each service with clear boundaries allows for granular horizontal scaling based on load and demand.
- Availability: With isolation each service is a self contained instance, allowing for graceful degradation of the overall service.


### Cons

- Cost and Complexity: Decoupled services with separate boundaries, each maintaining their own infrastructure (included data storage) adds maintenance overhead.
  > To serve the existing large user base, scalability and extensibility is needed to provide critical speed and malleability for Fave Trip as a startup.
- Performance Overhead: Multiple chained network calls would be needed between each services to complete their tasks would add turnaround time.
  > Have a hybrid architecture of event driven and microservices. Refer to [ADR-02 Event Driven Hybrid Architecture](/solutions/adrs/02-event-driven-hybrid.md)
- Data Consistency: As each service maintains their own data storage, there is a need to sync the data across each services.
  > Have an eventual consistency design to ensure data consistency. Refer to [ADR-03 Eventual Consistency](/solutions/adrs/02-eventual-consistency.md)

In summary, the trade-offs are acceptable for the benefits given to suit the needs of **Road Warrior**.
