# Event Driven Infrastructure
**Author:** Mike Place

 * Automation brought us new toolchains. DevOps brought us new culture.
   - Now what?

## Three Pillars of Distributed Systems
 * The ability for the system to be aware of the existence and capability of its member nodes.
 * The ability to coordinate tasks between these nodes.
 * Inter-process communication which can connect (almost) any node in the system to another.

## What are the properties of a message bus?
 * A data model.
 * A command set.
 * A transport infrastructure.

## Message Buses for Ops
 * Monitoring.
 * Configuration management.
 * ChatOps.
 * Auto-scale.
 * Lambda.
 * Provisioning.
   - Two divisions:
     + Provisioning time configuration.
     + Infrastructure life cycle management.
 * The rest of the presentation will be addressing infrastructure life cycle management.
 * there are also message buses for devs.
 * What can happen when both Dev and Ops message buss-es are shared and interact with eachother?

## Challenges of modern Infrastructure
 * Scaleability.
   - Ability to have effective command and control.
 * Observability.
   - How do we understand what's going on in these systems?
 * Serviceability
   - How do we modify deployed infrastructure?
 * Understandability

## State of Configuration Management
 * Resource provisioning.
 * Remote Execution.
 * Service/application packaging.
 * State management.

# What does (most) automation look like now
 * Packaged workflows.
   - We take a series of steps and we list them out and do these steps.
   - Much of the time, these workflows are initiated by lazy humans.
   - This can still be very brittle.
   - This doesn't feel much like **programming**.

## Event-driven Programming:
 * A program's flow is determined by events and external inputs.
 * Three Principles of Event Driven Programming:
   1. A set of functions which handle events.
   2. A mechanism for binding the registered functions to events.
   3. A main loop which constantly polls for new events and responds to them.
 * Criticisms:
   * Highly difficult to debug.
 * Advantages
   - It's easy to find natural dividing lines for unit testing infrastructure.
   - It's highly composeable.
   - It allows for a very simple and understandable model for both sides of the Dev-Ops bridge.
   - Both purely procedural and imperative approaches get brittle as they grow in complexity.
   - A good way to model.

## Advantages of Event-driven Infrastructure:
 * Gate deploys behind the operational state of the network.
 * React to service degradation behind initiating workflows.
 * Tune the health of the infrastructure.

## Principles of Event-driven Automation
 * Events originate from apps and systems
 * filters exist to sort these events and apply to rule to them.
 * As these events happen, registered actions can happen.

## Events are representations of systems, can be Stateful.
 * File changed
 * System load
 * Service status.
 * etc

## Advantages of Event-driven approach
 * Distributed, salable and loosely coupled between systems.
 * A "DevOps" automation backplane for systems.
 * Does more than just configure/provision systems at their birth. Allows for more complete life cycle management

## Disadvantages of Event-driven approach
 * Possible tight coupling between event schema and consumers of schema.
 * Message loss.
 * Reasoning about "blocking" ops can become more difficult.
 * Reproducing the state of the infrastructure might be difficult with this approach.
 * Testing.

## How to build it?
 * Flow:
   - An event is emitted on the event bus.
   - It flows to a manager.
   - The manager checks to see if the event matches a registered handler.
   - If so, a series of rules are checked.
   - For each matched rule, a series of actions are taking
 * Requirements:
   - Event bus transport.
   - Events
   - Actors: event emitters
   - Reactors: event responders.

## Building event Buses
 * Bus **must** handle:
   - Security
   - Reliability
   - Serialization

## Off the shelf messaging
 * ZeroMQ
 * Many others
   - Commentary: The presenter is going way to fast to keep up with! Going forward, he should consider slowing it down, cutting scope.

## Review
 * To build scalable systems, we need to adopt lessons of distributed computing.
 * We can migrate from human-driven processes to reactive, programmable systems.
 * Configuration management to evolve to continue doing heavy lifting
