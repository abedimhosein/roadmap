# Microservices Concepts

## 1. Core Principles

* **Microservices Architecture** – System composed of small, independent services
* **Single Responsibility** – Each service does one thing well
* **Autonomous Services** – Deploy, scale, and develop independently
* **Decentralization**

  * Data
  * Governance
  * Deployment
* **Failure Isolation** – One service failure shouldn’t kill the system
* **Scalability** – Scale services independently

---

## 2. Service Design

* **Service Boundary** – Logical separation of functionality
* **Bounded Context** (from DDD)
* **Loose Coupling** – Minimal dependencies between services
* **High Cohesion** – Related logic grouped together
* **API-First Design** – Define contracts before implementation
* **Backward Compatibility** – Don’t break consumers

---

## 3. Communication Patterns

### Synchronous Communication

* REST (HTTP/JSON)
* gRPC

### Asynchronous Communication

* Message Broker (queue-based)
* Event Streaming

### Interaction Styles

* Request–Response
* Publish–Subscribe
* Event-Driven Architecture

---

## 4. Data Management

* **Database per Service** – No shared DB (ignore this and you’re not doing microservices)
* **Polyglot Persistence** – Different DBs per service
* **Eventual Consistency**
* **Data Replication**
* **CQRS** – Separate read/write models

---

## 5. Distributed System Patterns

* **Saga Pattern**

  * Choreography
  * Orchestration
* **Event Sourcing**
* **API Composition**
* **Command Query Responsibility Segregation (CQRS)**

---

## 6. Resilience & Fault Tolerance

* **Circuit Breaker**
* **Retry Pattern**
* **Timeouts**
* **Bulkhead Isolation**
* **Fallback Mechanisms**
* **Rate Limiting**

---

## 7. Service Discovery

* **Service Registry** – Tracks available services
* **Client-Side Discovery**
* **Server-Side Discovery**

---

## 8. API Gateway

* Single entry point for clients
* Responsibilities:

  * Routing
  * Authentication
  * Rate limiting
  * Aggregation

---

## 9. Security

* **Authentication**

  * JWT
  * OAuth2
* **Authorization**
* **mTLS (Mutual TLS)**
* **Zero Trust Architecture**
* **Secrets Management**

---

## 10. Deployment & Infrastructure

* **Containerization** (e.g., Docker)
* **Orchestration** (e.g., Kubernetes)
* **Immutable Infrastructure**
* **Blue-Green Deployment**
* **Canary Releases**
* **Rolling Updates**

---

## 11. Observability

* **Logging** (centralized)
* **Monitoring** (metrics)
* **Tracing** (distributed tracing)
* **Alerting**

---

## 12. Configuration Management

* **Externalized Configuration**
* **Feature Flags**
* **Dynamic Configuration**

---

## 13. DevOps & CI/CD

* **Continuous Integration (CI)**
* **Continuous Deployment (CD)**
* **Infrastructure as Code (IaC)**
* **Automated Testing**

  * Unit
  * Integration
  * Contract Testing

---

## 14. Data & Consistency Challenges

* **Distributed Transactions Problem**
* **Two-Phase Commit (2PC)** (usually avoid)
* **Eventual Consistency**
* **Idempotency**

---

## 15. Versioning & Compatibility

* **API Versioning**
* **Schema Evolution**
* **Backward/Forward Compatibility**

---

## 16. Anti-Patterns (Common Mistakes)

* **Distributed Monolith** – Services tightly coupled
* **Shared Database** – Breaks independence
* **Chatty Services** – Too many network calls
* **Over-Splitting Services** – Micro ≠ tiny for no reason
* **No Observability** – You’re blind in production
* **Synchronous Everything** – Leads to cascading failures

---

## 17. Advanced Concepts

* **Service Mesh** (e.g., Istio, Linkerd)
* **Sidecar Pattern**
* **Backend for Frontend (BFF)**
* **Strangler Fig Pattern** (for migration)
* **Multi-Region Deployment**
* **Chaos Engineering**

---

## 18. Quick Mental Model

* Design → boundaries + APIs
* Communication → sync vs async
* Data → distributed, eventually consistent
* Infra → containers + orchestration
* Ops → observe everything or suffer
