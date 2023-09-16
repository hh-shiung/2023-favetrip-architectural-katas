# Using Eventual Consistency

## Status

Proposed

## Context

To maintain data consistency within the hybrid event-driven and microservices architecture, we need a consistency model.

In a microservices architecture, independent services often maintain individual data stores.
Hence, there is an coordination overhead to maintain immediate consistency between data stores, introducing cost in the form of increased latency and reduced performance.

Eventual consistency helps microservices maintain high scalability and performance without sacrificing data consistency.

## Decision

An eventual consistency model is used to prioritise availability and partition tolerance over immediate consistency, making it perfect for microservices architecture.
It allows microservices to propagate changes across different data stores asynchronously and eventually converge to a consistent state.

## Consequences

### Pros

- Performance is guaranteed while still having the data consistency "eventually" across services

### Cons

- Asynchronous data changes has delays between different services
  - Eventually every services will have the finalised state of data
  - As the main goal of **Fave Trip** is to provide timely travel updates to users, a slight delay can be compromised on as the users eventually got the final updates
