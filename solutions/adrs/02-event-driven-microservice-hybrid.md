# Hybrid of Event Driven and Microservice Architecture

## Status

Accepted

## Context

An event driven architecture promotes the generation, detection, consumption, and reaction based on events.
It would allow the system to be distributed and scalable, while handling asynchronous communication between various services.

The event drivern architecture will be used to used for pushing notifications and real-time updates to ensure that they are delivered quickly and reliably, for a consistent experience across different platforms for the user.

## Decision Drivers

- To reduce performance overhead from the network calls between individual services within the microservices architecture
- To ensure data consistency between services and interfaces

## Decision

We chose to use a hybrid architecture setup of both event driven and microservices styles for the Road Warriors system.
This provides us the best of both worlds, where we can have the speed and robustness from a event driven architecture for communications while maintaining flexibility for other modules of the system.

## Consequences

### Pros

- Improved Performance
  - Services are communicate through an Event Broker, which reacts to events in real-time or near-real-time asynchronously.
  - This is crucial for **Road Warriors** that needs to capture and push travel updates from serveral sources to travelers.
- Support Complex Workflows:
  - The hybrid framework is well-suited for managing complex business workflows that involve multiple steps and asynchronous interactions.
  - This can be useful for **Road Warriors** that has multiple operations to capture, aggregate and analyze the travel reservations.

### Cons

- Additional cost and complexity: Managing events, ensuring reliable delivery, and dealing with eventual consistency can be challenging.
- Event Loss: In cases of system failures or misconfigurations, events can be lost, leading to potential data inconsistency or missed updates.
