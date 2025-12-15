
---

# 🚀 Frontend System Design Curriculum

### (Interview Perspective – Topic + Question Based )

---

## 🟦 Module 1: How Web Works (Web Fundamentals)

### Topics Covered

* Browser Architecture (UI, JS Engine, Rendering Engine)
* DNS Resolution
* TCP 3-way Handshake
* TLS / HTTPS
* HTTP Request → Response Lifecycle
* Browser Rendering Pipeline

### Interview Questions

* Browser-এ URL লিখলে end-to-end কী ঘটে?
* DNS lookup কোথায় হয়?
* HTTPS কেন HTTP থেকে secure?
* Rendering blocking resource কী?

---

## 🟦 Module 2: Communication Protocols

---

### 🔹 REST APIs

#### Topics Covered

* REST Architecture Principles
* HTTP Request / Response Structure
* HTTP Headers (Auth, Cache, CORS)
* HTTP Methods (GET, POST, PUT, PATCH, DELETE)
* HTTP Status Codes (2xx, 3xx, 4xx, 5xx)
* REST Best Practices
* Idempotency
* Real-world API examples

#### Interview Questions

* PUT vs PATCH পার্থক্য কী?
* GET request body রাখা উচিত?
* 401 vs 403 difference?
* REST API scalable কেন?
* Idempotent API কী?

---

### 🔹 GraphQL

#### Topics Covered

* REST limitations
* GraphQL Overview
* Schema & Types
* Query vs Mutation
* Resolver
* Single Endpoint Concept
* Overfetching / Underfetching
* Caching Challenges
* Working Examples

#### Interview Questions

* REST vs GraphQL—কখন কোনটা?
* GraphQL এ caching কঠিন কেন?
* Resolver কী?

---

### 🔹 gRPC

#### Topics Covered

* gRPC Overview
* Protocol Buffers
* Service Definition
* RPC Methods
* IDL (Interface Definition Language)
* Code Generation
* Working Examples

#### Interview Questions

* gRPC vs REST
* JSON vs Binary protocol
* Frontend-এ gRPC কম কেন?

---

## 🟦 Module 3: Networking & Realtime Communication

### Topics Covered

* Short Polling
* Long Polling
* WebSockets
* Server-Sent Events (SSE)
* WebHooks
* Pros & Cons of each
* Real-world examples (Chat, Notification, Live Feed)

### Interview Questions

* WebSocket vs SSE
* Long polling inefficient কেন?
* Chat app বানাতে কী use করবে?

---

## 🟦 Module 4: Security 

### Topics Covered

* Cross Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* iFrame / Clickjacking Protection
* Authentication vs Authorization
* Security Headers
* Client-side Security
* HTTPS & TLS
* Dependency Security
* Compliance & Regulation
* Input Validation & Sanitization
* SSRF
* Server-side JS Injection
* Permissions-Policy
* Subresource Integrity (SRI)
* CORS

### Interview Questions

* XSS কী এবং prevent কিভাবে?
* CSRF token কীভাবে কাজ করে?
* Cookie vs LocalStorage security
* CORS error কেন হয়?

---

## 🟦 Module 5: Performance Optimization

### Topics Covered

* Asset Optimization (Images, Fonts)
* Network Optimization
* Build Optimization (Tree Shaking, Minification)
* React Optimization
* JavaScript Optimization
* Performance Monitoring
* Performance Tools
* Rendering Patterns (CSR, SSR, ISR)

### Interview Questions

* Page slow হলে debugging কিভাবে?
* Debounce vs Throttle
* Lazy loading কীভাবে কাজ করে?
* LCP, CLS কী?

---

## 🟦 Module 6: Database, Storage & Caching

### Topics Covered

* Local Storage
* Session Storage
* Cookie Storage
* IndexedDB
* Data Normalization
* HTTP Caching
* Service Worker Caching
* API Caching
* State Management Caching

### Interview Questions

* LocalStorage vs Cookie
* IndexedDB কখন ব্যবহার করবে?
* Cache invalidation কী?

---

## 🟦 Module 7: Testing Strategy

### Topics Covered

* Unit Testing
* Component Testing
* Integration Testing
* End-to-End (e2e) Testing
* A/B Testing
* Test Driven Development (TDD)
* Automation Testing
* Testing Tools & Libraries

### Interview Questions

* Unit vs Integration testing
* Flaky test কী?
* Frontend-এ e2e দরকার কেন?

---

## 🟦 Module 8: Low Level Design (LLD)

### Topics Covered

* Design Patterns
* Component Design
* State Management
* Routing
* SOLID Principles

### LLD Problems

* Infinite Scroll
* Nested Comments
* Pagination
* Image Carousel
* Live Streaming Chat UI
* Autocomplete / Search Bar

### Interview Questions

* Component breakup কিভাবে করো?
* State কোথায় রাখবে?
* Pagination vs Infinite Scroll trade-off

---

## 🟦 Module 9: High Level Design (HLD)

### Design Problems

* Social Media Feed (Facebook, Twitter)
* Photo Sharing App (Instagram)
* E-commerce App (Amazon, Flipkart)
* Video Streaming (Netflix, Hotstar)
* Google Docs / Sheets
* Diagram Tools (Excalidraw)
* Music Streaming (Spotify)
* Live Commentary (CricInfo, Cricbuzz)
* Cab Services (Uber, Ola)
* Analytics Dashboard (Google Analytics)

### Interview Questions

* Realtime update কিভাবে handle করবে?
* Scalability frontend-এ কীভাবে?
* Feed ranking কোথায় হবে?

---

## 🟦 Module 10: Offline Support

### Topics Covered

* Progressive Web Applications (PWA)
* Service Workers
* Offline Caching
* Background Sync

### Interview Questions

* Offline-first app কী?
* Service worker lifecycle

---

## 🟦 Module 11: Accessibility (A11y)

### Topics Covered

* Keyboard Accessibility
* Screen Readers
* ARIA attributes
* Color Contrast

### Interview Questions

* ARIA-label কী?
* Accessibility কেন গুরুত্বপূর্ণ?

---

## 🟦 Module 12: Logging & Monitoring

### Topics Covered

* Telemetry
* Error Logging
* Feature Usage Tracking
* User Tracking
* Monitoring Tools
* Alerting
* Performance Metrics
* Infra Capacity
* Error Threshold
* API Failure Handling
* Debugging
* Mitigation & Prevention

### Interview Questions

* Production error কিভাবে track করো?
* Sentry / Datadog কী?
* Alert threshold কীভাবে সেট করো?

---

