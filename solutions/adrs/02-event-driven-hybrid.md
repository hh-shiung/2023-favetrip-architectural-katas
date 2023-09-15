# Title

Use Hybrid of Event Driven and Microservice architecture style

## Status

Proposed

## Context

To reduce performance overhead from the network calls between individual services within the microservices architecture, event driven design is take into consideration in the architecture design.

## Decision

We decide to have hybrid of event driven and microservices architecture for the **Road Warrior** system, so that we can have the performance from the event driven architecture while we still can enjoy the benefits of microservices.

## Consequences

### Pros
- Improved Performance: Services are communicate via Event Broker, which react to events in real-time or near-real-time asynchronously. This is crucial for **Road Warrior** which need to capture and push travel updates from serveral sources to travelers.
- Support Complex Workflows: Well-suited for managing complex business workflows that involve multiple steps and asynchronous interactions. This can be useful for **Road Warrior** which invovled steps to capture, aggregate and analyze the travel reservations.

### Cons
- Additional cost and complexity: Managing events, ensuring reliable delivery, and dealing with eventual consistency can be challenging.
- Event Loss: In cases of system failures or misconfigurations, events can be lost, leading to potential data inconsistency or missed updates.
