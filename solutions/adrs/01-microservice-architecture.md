# Title

Use the microservice architecture style

## Status

Proposed

## Context

Microservices is an extremely popular architecture style in recent years especially for large scale application. However, this is not a good enough reason for us to just go with it, there are some consequences need to be consider.

## Decision

We decide to go with Mircoservices architecture style for due to its nature of distributed design which able to maximise with potential of scability, evolvability and availability.

## Consequences

### Pros
- Extensibility / Evolvability: new functions or features can be decoupled into smaller capabiltiy services easily which allow rapid iteration
- Scalability: each services are defined with boundary which allow to scale horizontally for specific services based on the varying load and help to support huge amount of incoming requests simultaneously
- Availability: each defined services are isolated, whereas one of the less important service is down, it won't affect the entire system hence lead to a near 0 downtime


### Cons
- Cost and Complexity: Each services are decoupled into multiple separate boundaries and with their own set of infrastructures included data storage
  > Though additional cost and complexity needed, but given that the larger user base currently had, we will need to have the scaibility in place and extensibility for adapt the fast-paced environment for a startup to survive
- Performance Overhead: Multiple network calls needed between each services to complete the work, there will be extra turnaround time added
  > This can be mitigate by having a hybrid architecture of event driven and microservices which can refer to [ADR-02 Event Driven Hybrid Architecture](/solutions/adrs/02-event-driven-hybrid.md)
- Data Consistency: As each of the services has their own separate data storage, it might be a concern to sync the data across each services which we should be addressed.
  > This can be mitigate by having a eventual consistency design in place which can refer to [ADR-03 Eventual Consistency](/solutions/adrs/02-eventual-consistency.md)

As compare with the trade-offs, the benefits given are much more significant to suit the needs of **Road Warrior**.
