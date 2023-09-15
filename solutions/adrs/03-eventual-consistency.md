# Title

Use of Eventual Consistency to maintain data consistency in the hybrid of event-driven & microservices architecture

## Status

Proposed

## Context

In a microservices architecture, services are independent of each other and often have separate data stores for each microservice. Hence, maintaining immediate consistency between data stores would require a lot of coordination between the services, increasing the latency and reducing performance.

So, we need to have a way to help microservices maintain high scalability and performance without sacrificing data consistency, hence eventual consistency come in place.

## Decision

We decide to ensure eventual consistency to prioritise availability and partition tolerance over immediate consistency, making it perfect for microservices architecture. It allows microservices to propagate changes across different data stores asynchronously and eventually converge to a consistent state.

## Consequences

### Pros
- Performance is gurantee while we still having the data consistency "eventually" across services

### Cons
- Data changes might not be reflected synchronously across every services, might be a bit lag behind for different services, but eventually every services will be having the same finalized state of data. This is still acceptable, as main goals of **Road Warrior** is to provide timely travel updates to travelers, a slight delay can be compromised as the travelers eventually got the final updates.
