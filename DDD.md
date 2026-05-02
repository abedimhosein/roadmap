# Domain-Driven Design (DDD) Concepts

## 1. Strategic Design (Big Picture)

### Core Concepts

* **Domain** – The problem space your software is solving
* **Subdomain**

  * Core Subdomain (competitive advantage)
  * Supporting Subdomain
  * Generic Subdomain
* **Bounded Context** – Explicit boundary where a model is defined and consistent
* **Ubiquitous Language** – Shared language between developers and domain experts

### Context Mapping

* **Context Map** – Diagram of relationships between bounded contexts
* **Relationships**

  * Partnership
  * Shared Kernel
  * Customer–Supplier
  * Conformist
  * Anti-Corruption Layer (ACL)
  * Open Host Service
  * Published Language
  * Separate Ways
  * Big Ball of Mud

---

## 2. Tactical Design (Inside the Boundary)

### Building Blocks

#### Entities

* Objects with **identity**
* Mutable lifecycle
* Example: User, Order

#### Value Objects

* Objects with **no identity**
* Immutable
* Compared by value
* Example: Money, Address

#### Aggregates

* Cluster of domain objects treated as a unit
* Enforces consistency boundaries

##### Aggregate Root

* Entry point to an aggregate
* Only root is accessed externally

---

### Domain Logic

#### Domain Events

* Something meaningful that happened in the domain
* Immutable
* Example: `OrderPlaced`, `PaymentCompleted`

#### Domain Services

* Domain logic that doesn't fit in Entity or Value Object
* Stateless

#### Application Services

* Orchestrate use cases
* Coordinate domain objects
* No business logic

---

### Repositories

* Abstraction over persistence
* Provide access to aggregates
* Mimic in-memory collections

---

### Factories

* Handle complex object creation
* Ensure invariants are satisfied

---

## 3. Architectural Patterns

### Layers (Classic DDD)

* Presentation Layer
* Application Layer
* Domain Layer
* Infrastructure Layer

---

### Hexagonal / Clean Architecture

* Domain at the center
* Ports & Adapters
* Dependency inversion

---

### CQRS (Command Query Responsibility Segregation)

* Separate read and write models
* Commands = mutate state
* Queries = read-only

---

### Event Sourcing

* Store state as a sequence of events
* Rebuild state from events

---

## 4. Supporting Concepts

### Specifications

* Encapsulate business rules
* Reusable predicates

---

### Policies

* Business rules that guide decisions

---

### Invariants

* Rules that must always be true inside an aggregate

---

### Modules

* Group related domain concepts
* Improve structure

---

### Domain Model

* The heart of DDD
* Rich model with behavior (not anemic)

---

## 5. Integration Patterns

* **Anti-Corruption Layer (ACL)** – Protect your domain from external models
* **Domain Events Integration** – Communicate between bounded contexts
* **Messaging / Event Bus** – Async communication

---

## 6. Common Anti-Patterns (You should avoid these)

* **Anemic Domain Model** – No behavior, just data
* **God Object** – One class does everything
* **Leaky Abstractions** – Domain polluted by infrastructure
* **Tight Coupling Between Contexts**
* **Over-Engineering DDD** (yes, this happens a lot)

---

## 7. Optional Advanced Concepts

* **Saga / Process Manager** – Manage long-running workflows
* **Eventual Consistency**
* **Domain Policies vs Application Policies**
* **Temporal Modeling**
* **Aggregate Design Heuristics**

---

## 8. Quick Mental Model

* Strategic = boundaries and communication
* Tactical = how you model inside
* Architecture = how you implement it
