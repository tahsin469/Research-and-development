
---

# **Comprehensive Backend Engineering Curriculum (বাংলা)**

---

## **1. HTTP Protocol**

**সাব-টপিক:**

* HTTP Methods: GET, POST, PUT, DELETE, PATCH
* Status Codes: 1xx, 2xx, 3xx, 4xx, 5xx
* Headers: Content-Type, Authorization, Cache-Control
* Cookies & Sessions
* HTTPS & TLS basics

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Postman, Curl, Browser Dev Tools, Network analyzers

**ইন্টারভিউ প্রশ্ন:**

* GET এবং POST এর মধ্যে পার্থক্য কী?
* Statelessness মানে কী HTTP-এ?
* HTTPS কিভাবে কাজ করে?

---

## **2. Routing**

**সাব-টপিক:**

* RESTful routing
* Dynamic vs static routes
* Route parameters & query parameters
* Route grouping & versioning

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Route mapping principles, API gateway concepts

**ইন্টারভিউ প্রশ্ন:**

* Route parameter এবং query parameter এর পার্থক্য কী?
* API versioning কিভাবে করবেন?

---

## **3. Serialization & Deserialization**

**সাব-টপিক:**

* Object ↔ JSON/XML/YAML conversion
* Schema validation & data mapping
* Streaming & large payload handling

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* DTO patterns, schema validation techniques

**ইন্টারভিউ প্রশ্ন:**

* Serialization এবং deserialization এর পার্থক্য কী?
* Large payload হ্যান্ডেল করার সেরা পদ্ধতি কী?

---

## **4. Authentication & Authorization**

**সাব-টপিক:**

* Identity management
* Session, Token, Key-based authentication
* Role-based vs Permission-based access control
* Multi-factor authentication

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* JWT principles, OAuth/OpenID concepts, Security design principles

**ইন্টারভিউ প্রশ্ন:**

* JWT এবং session authentication পার্থক্য কী?
* RBAC এবং ABAC পার্থক্য কী?

---

## **5. Validation & Transformation**

**সাব-টপিক:**

* Input validation: type, format, regex
* Data sanitization & normalization
* Transformation pipelines (DTOs)
* Backward-compatible schema handling

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Validation pipelines, schema mapping patterns

**ইন্টারভিউ প্রশ্ন:**

* Validation এবং transformation এর পার্থক্য কী?
* Input sanitization কেন গুরুত্বপূর্ণ?

---

## **6. Middlewares**

**সাব-টপিক:**

* Request/response interception
* Logging, auditing, monitoring hooks
* Security, validation, error handling middleware

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Middleware chain principles, Interceptor patterns

**ইন্টারভিউ প্রশ্ন:**

* Middleware lifecycle কিভাবে কাজ করে?
* Global vs route-specific middleware পার্থক্য কী?

---

## **7. Request Context**

**সাব-টপিক:**

* Request-scoped variables
* Context propagation
* Correlation IDs for tracing

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Request context patterns, logging correlation

**ইন্টারভিউ প্রশ্ন:**

* Request context কি এবং কেন গুরুত্বপূর্ণ?

---

## **8. Handlers, Controllers & Services**

**সাব-টপিক:**

* Separation of concerns
* Controllers: route handling
* Services: business logic
* Idempotency & safe operations

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Layered architecture, SRP principle

**ইন্টারভিউ প্রশ্ন:**

* Controller এবং Service পার্থক্য কী?
* Idempotency কেন গুরুত্বপূর্ণ?

---

## **9. CRUD Deep Dive**

**সাব-টপিক:**

* Create, Read, Update, Delete
* Soft vs Hard delete
* Bulk operations
* Concurrency: optimistic vs pessimistic

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Transaction patterns, consistency models

**ইন্টারভিউ প্রশ্ন:**

* Soft delete কী এবং কখন ব্যবহার করবেন?
* Concurrency control কিভাবে করবেন?

---

## **10. RESTful Architecture & Best Practices**

**সাব-টপিক:**

* Resource-oriented design
* Stateless API
* HATEOAS & hypermedia principles
* Response codes & error handling
* API versioning strategies

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* REST design patterns, hypermedia principles

**ইন্টারভিউ প্রশ্ন:**

* REST vs RPC পার্থক্য কী?
* Statelessness কেন গুরুত্বপূর্ণ?

---

## **11. Databases**

**সাব-টপিক:**

* Relational vs NoSQL modeling
* Indexing & query optimization
* Transactions & ACID principles
* Sharding, replication, partitioning
* Normalization & denormalization

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* ER modeling, query optimization principles

**ইন্টারভিউ প্রশ্ন:**

* ACID vs BASE পার্থক্য কী?
* Normalization এবং denormalization কেন গুরুত্বপূর্ণ?

---

## **12. Business Logic Layer (BLL)**

**সাব-টপিক:**

* Domain-driven design
* Service orchestration
* Error handling & validation
* Testable & maintainable design

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Layered architecture, separation of concerns

**ইন্টারভিউ প্রশ্ন:**

* BLL vs DAL পার্থক্য কী?
* Domain logic কেন service layer এ রাখা উচিত?

---

## **13. Caching**

**সাব-টপিক:**

* Cache strategies: read-through, write-through, write-back
* Expiration & invalidation
* Hot vs cold data handling
* Performance profiling

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Cache design patterns, latency measurement

**ইন্টারভিউ প্রশ্ন:**

* Cache aside vs write-through vs write-back?
* Cache consistency কিভাবে নিশ্চিত করবেন?

---

## **14. Transactional Emails**

**সাব-টপিক:**

* SMTP vs API-based sending
* Template design & personalization
* Queued vs synchronous sending

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Email sending patterns, queueing concepts

**ইন্টারভিউ প্রশ্ন:**

* Transactional email vs marketing email পার্থক্য কী?
* Queued email কেন গুরুত্বপূর্ণ?

---

## **15. Task Queuing & Scheduling**

**সাব-টপিক:**

* Background jobs
* Message queues & prioritization
* Retry & dead-letter handling
* Cron vs event-based scheduling

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Job orchestration principles, idempotency

**ইন্টারভিউ প্রশ্ন:**

* Background jobs vs synchronous tasks পার্থক্য?
* Retry strategies কীভাবে implement করবেন?

---

## **16. Elasticsearch**

**সাব-টপিক:**

* Full-text search concepts
* Indexing & query optimization
* Aggregations & filtering
* Real-time analytics basics

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Search indexing patterns, aggregation principles

**ইন্টারভিউ প্রশ্ন:**

* Full-text search কেন প্রয়োজন?
* Indexing ও query optimization কিভাবে করবেন?

---

## **17. Error Handling**

**সাব-টপিক:**

* Exception vs error handling
* Global error handling strategies
* Retry policies & circuit breakers
* Graceful degradation

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Error propagation, fault isolation patterns

**ইন্টারভিউ প্রশ্ন:**

* Graceful degradation কী?
* Circuit breaker pattern কবে ব্যবহার করবেন?

---

## **18. Config Management**

**সাব-টপিক:**

* Environment-specific configs
* Secrets management & encryption
* Dynamic reload & feature flags

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Secure config principles, feature toggle patterns

**ইন্টারভিউ প্রশ্ন:**

* Environment-specific configuration কেন গুরুত্বপূর্ণ?
* Secrets management কিভাবে করবেন?

---

## **19. Logging, Monitoring & Observability**

**সাব-টপিক:**

* Structured logging & correlation IDs
* Metrics & health checks
* Distributed tracing
* Alerting & incident response

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Logging & tracing patterns, observability design

**ইন্টারভিউ প্রশ্ন:**

* Logging vs monitoring vs tracing পার্থক্য কী?
* Observability কেন গুরুত্বপূর্ণ?

---

## **20. Graceful Shutdown**

**সাব-টপিক:**

* Signal handling
* Cleanup tasks
* Connection draining
* Resource release

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Lifecycle hooks, shutdown handlers

**ইন্টারভিউ প্রশ্ন:**

* Graceful shutdown কিভাবে implement করবেন?
* Resource cleanup কেন গুরুত্বপূর্ণ?

---

## **21. Security**

**সাব-টপিক:**

* Threat modeling, OWASP Top 10
* Input/output validation & sanitization
* Data encryption & hashing
* Rate limiting, throttling, DDoS mitigation

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Secure design patterns, encryption principles

**ইন্টারভিউ প্রশ্ন:**

* SQL Injection প্রতিরোধ কিভাবে করবেন?
* JWT security considerations কী?

---

## **22. Scaling & Performance**

**সাব-টপিক:**

* Horizontal vs vertical scaling
* Load balancing & request distribution
* Bottleneck identification
* Database & service scaling strategies

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Performance profiling, scaling principles

**ইন্টারভিউ প্রশ্ন:**

* Horizontal vs vertical scaling পার্থক্য?
* Bottleneck কিভাবে সনাক্ত করবেন?

---

## **23. Concurrency & Parallelism**

**সাব-টপিক:**

* Multithreading & async processing
* Locks, semaphores, mutex
* Event-driven concurrency
* Deadlock & race condition prevention

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Thread-safe patterns, async design principles

**ইন্টারভিউ প্রশ্ন:**

* Deadlock vs race condition পার্থক্য?
* Async vs parallel processing কখন ব্যবহার করবেন?

---

## **24. Object Storage & Large Files**

**সাব-টপিক:**

* Streaming large files
* Object storage fundamentals
* Partitioning & sharding
* Backup & archival strategies

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Storage design patterns, data retention policies

**ইন্টারভিউ প্রশ্ন:**

* Large file streaming কিভাবে করবেন?
* Object storage vs block storage পার্থক্য?

---

## **25. Real-time Backend Systems**

**সাব-টপিক:**

* Event-driven & pub/sub architectures
* Low-latency updates & notifications
* Message ordering & reliability
* Real-time monitoring

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Event-driven system design, low-latency principles

**ইন্টারভিউ প্রশ্ন:**

* Polling vs WebSocket পার্থক্য?
* Event-driven architecture কবে ব্যবহার করবেন?

---

## **26. Testing & Code Quality**

**সাব-টপিক:**

* Unit, Integration, E2E testing
* Mocks, fakes, stubs
* Code coverage & static analysis
* Testable & maintainable design

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Testing pyramid, TDD & BDD principles

**ইন্টারভিউ প্রশ্ন:**

* Unit vs integration vs functional test পার্থক্য?
* Testable design কিভাবে করবেন?

---

## **27. 12 Factor App**

**সাব-টপিক:**

* Codebase, dependencies, config
* Backing services, logs, processes
* Dev/prod parity, statelessness

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* 12-Factor principles, environment parity patterns

**ইন্টারভিউ প্রশ্ন:**

* 12 Factor App principles কী?
* Stateless app design কেন গুরুত্বপূর্ণ?

---

## **28. OpenAPI Standards**

**সাব-টপিক:**

* API documentation & contract
* Specification standards
* API versioning & validation

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* API contract design principles, schema validation

**ইন্টারভিউ প্রশ্ন:**

* OpenAPI vs GraphQL পার্থক্য?
* API contract importance কী?

---

## **29. Webhooks**

**সাব-টপিক:**

* Event-driven communication
* Payload validation
* Retry & idempotency handling

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* Event-driven design, webhook reliability patterns

**ইন্টারভিউ প্রশ্ন:**

* Webhook vs API request পার্থক্য?
* Idempotency handling কিভাবে করবেন?

---

## **30. DevOps for Backend Engineers**

**সাব-টপিক:**

* CI/CD principles
* Containerization & orchestration
* Infrastructure as Code
* Rollback, blue-green, canary deployments

**প্রয়োগযোগ্য টুলস/লাইব্রেরি:**

* CI/CD design principles, immutable deployment

**ইন্টারভিউ প্রশ্ন:**

* CI/CD workflow explain করুন
* Immutable deployment কেন গুরুত্বপূর্ণ?

---


