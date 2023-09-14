# Road Warrior Architecture Proposal

## Problem

### Context
In today's increasingly complex travel landscape, travelers are faced with the challenge of managing numerous reservations scattered across various platforms and emails. Whether planning business trips or leisure vacations, the lack of a centralized and user-friendly solution for organizing travel itineraries has become a significant pain point.

A new startup dedicated to build the next generation online trip management dashboard, **Road Warrior** which aims to empower travelers by offering a unified platform accessible via web or mobile devices, streamlining the management of all travel reservations and revolutionizing the way individuals and businesses organize their trips.

### Requirements

#### Business Goals

As stated in the given [requirements](problems/requirements.md), below are the primary business goals targeted for the **Road Warrior**:
- Allow travelers to view all their trip related reservations details in a unified dashboard which extract from various sources:
  - Email
  - Self input details
  - Integrated Agency System (Airline, Hotel, Car Rental)
  - Integrated Travel System (SABRE, APOLLO)
- Allow travelers to manage their existing trip related reservations from the dashboard
- Allow travelers to get near real-time updates regarding their trip related reservations
- Provide meaningful insights to travelers and any interested parties by gathering the analytical data derived from travelers' trips details

#### Business Requirements
We proposed to start the implementation with a Minimum Viable Product (MVP) and then iterating over it in later phases, so that we can build a functional system that meets the core requirements and improve incrementally based evolving business needs.

Below is the suggested roadmap for implementing **Road Warrior** from short to long term timelines:

##### Short Term

- basic user authentication for traveler to sign up and login to the system
- allow travelers to manually add, update, or delete travel reservations from the dashboard
- poll and filter travel-related emails (flight details, hotel reservations, and car rentals) from traveler's email inbox
- create a simple dashboard that displays travel information which can be view from both web & mobile applications
- show real-time travel updates to travelers from integrated agency system

##### Mid Term
- enhance the dashboard to group items by trips and remove completed trip items automatically
- integrate 3rd party travel system to capture traveler's reservations
- integrate with prefered travel agency for quick problem resolution
- share trip information on social media or with specific individuals

##### Long Term
- generate more in-depth analytics with the power of AI
- generate end-of-year summary reports for travelers with a wide range of travel metrics
- internationalization support for users across the world

#### Business Constraints

- Initial funding for the project was secured by numerous investors to kickstart the MVP
- The project is expected to sustain mainly with revenue generated from user subcription model in a long run, but not limited to other possible revenue model like providing data insights report

#### Technical Constraints

- This is a build from scratch project

## Solution

### Actors, Actions & Significant Scenarios

Actor/actions approach is used to map the requirements to components which help to understand who do what within the system and ease for further analyzing the architecture characteristics.

#### Actors & Actions
Below are the actors and their corresponding actions invovled in the Road Warrior system

| Actors | Actions |
|---|---|
| Traveler | - sign up & login to the system<br>- add new travel reservation<br>- update & delete the existing travel reservations<br>- view all the captured travel reservations in a unified dashboard<br>- view end-of-year travel usage summary reports<br>- view real-time travel updates<br>- share trip information on social media or other users within the system |
| System | - poll & filter emails to capture travel related reservations<br>- pull travel updates from integrated agency or travel systems<br>- group travel reservations by locations & time<br>- archive completed travel reservations<br>- analyze trip details gathered from travelers |

#### Significant Scenarios

Below are the most architecturally significant scenarios derived from the Actors and Actions above, which will shape the architecture of the Road Warrior system.

>todo: need some simple flow diagram
##### Travel Reservation Capture
- Capture from Email
- Capture from User input

##### Travel Reservation Updates Tracker
- Track from Integrated Agency or Travel System
- Track from Travelers Input

##### Travel Reservation Analyzer
- Group travel reservations by locations & time
- Archive completed travel reservations
- Reporting and metrics analytics

### Architecture Analysis

#### Desired Architecture Characteristics
We consider each of the given requirements and map them to corresponsing architecture characteristics below

>todo: need rationale
- Performance
- Scalability
- Extensibility
- Availability
- Data Consistency
- Data Integrity
- Usability

#### Architecture Styles
With the help of the [worksheet](https://www.developertoarchitect.com/downloads/architecture-styles-worksheet.pdf), we compared against few styles and finalized with the one that will give us the most benefits and least trade-offs with respect to the architecture properties above.

>todo: why choose event driven + microservices

### High Level Architecture

### Detailed Architecture

### ADRs

### References
- [Previous Katas Entries](https://github.com/tekiegirl/SoftwareArchitectureResources/blob/main/Resources/OReillyKata.md)
- [Fundamentals of Software Architecture](https://learning.oreilly.com/library/view/fundamentals-of-software/9781492043447/)
- [Building Event-Driven Microservices](https://learning.oreilly.com/library/view/building-event-driven-microservices/9781492057888/)
