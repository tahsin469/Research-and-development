
# 🧠 Backend Architecture – Interview Cheat-Sheet 

## 🧱 Layered Architecture কেন ব্যবহার করো?

**Short Answer:**
👉 Separation of concerns, maintainability, testability

**Key Points বলবে:**

* Controller = HTTP handling
* Service = Business logic
* Repository = Data access
* Change impact limited থাকে

---

## 🧼 Clean Architecture কী?

**Short Answer:**
👉 Business logic কে framework-independent রাখা

**Key Line:**

> “Framework is a detail, business rules are not.”

---

## 🆚 Clean vs Layered Architecture

| বিষয়              | Layered   | Clean            |
| ----------------- | --------- | ---------------- |
| Complexity        | কম        | বেশি             |
| Learning curve    | সহজ       | কঠিন             |
| Scale suitability | Small–Mid | Large–Enterprise |

**Interview Tip:**
👉 “Layered দিয়ে শুরু, Clean-এ evolve”

---

## 🍔 Fat Controller নাকি Fat Service?

✔️ **Fat Service**
❌ Fat Controller

**One-liner:**

> Controller orchestrates, Service decides.

---

## 🔄 API Request Flow (1-liner)

```
Client → Middleware → Controller → Service → Repository → DB → Response
```

---

## 🧾 DTO কেন দরকার?

**Answer:**

* Security (Entity expose না করা)
* API versioning
* Loose coupling

---

## 🔐 Authentication vs Authorization

* Authentication = “তুমি কে?”
* Authorization = “তুমি কী করতে পারো?”

---

## 🔑 Password কীভাবে store করবে?

✔️ bcrypt / PBKDF2 + salt
❌ plain text / simple hash

---

## 🛡️ API Security Checklist

* HTTPS
* Input validation
* JWT expiry
* Rate limiting

---

## ⚡ High Traffic Handle করবে কীভাবে?

**Golden 3:**

1. Caching
2. Load balancing
3. DB optimization

---

## 🧠 Cache Invalidation কেন কঠিন?

**Classic quote:**

> “There are only two hard things in CS: cache invalidation…”

**Strategies বলবে:**

* TTL
* Write-through
* Event-based invalidation

---

## 📈 Vertical vs Horizontal Scaling

* Vertical = RAM/CPU বাড়ানো
* Horizontal = server সংখ্যা বাড়ানো ✔️

---

## 🔁 Race Condition কী?

👉 Multiple process একই resource modify করে

**Solution:**

* Lock
* Transaction
* Optimistic concurrency

---

## 💥 Distributed Transaction Problem?

✔️ Saga Pattern
✔️ Eventual Consistency
❌ 2PC (avoid in microservices)

---

## 🧪 Unit vs Integration Test

* Unit = Fast, isolated
* Integration = Real DB, slower

---

## 🧩 Monolith vs Microservices

**Senior answer:**

> “Start monolith, split when pain appears.”

---

## 🔗 Inter-service Communication

* Sync: REST / gRPC
* Async: Message Queue / Events ✔️

---

## 📊 Observability মানে কী?

**3 pillars:**

* Logs
* Metrics
* Traces

---

## 📴 Graceful Shutdown কেন দরকার?

👉 Ongoing request শেষ করা
👉 Data loss এড়ানো

---

## 🚀 CI/CD Pipeline এ কী থাকে?

* Build
* Test
* Deploy

---

## ⚙️ Config কোথায় রাখবে?

✔️ Environment variables
✔️ Secret manager
❌ Code-এ hardcode না

---

## 🧠 Scalable Login System – Key Ideas

* Stateless auth
* JWT
* Redis for session/blacklist

---

## 🧩 “Change is constant” – Architecture Response

✔️ Interface-driven design
✔️ Loose coupling
✔️ Config-based behavior

---

## 📘 Architecture Documentation কীভাবে?

* Folder structure clear
* README
* OpenAPI / Swagger

---


---

# 🔥 Real Production Incident Discussion 

আমি ৩টি **সবচেয়ে কমন কিন্তু সিরিয়াস production incident** তুলে ধরছি।

প্রতিটা case-এ থাকবে:

* 🔴 Problem
* 🔍 Investigation
* 🛠️ Fix
* 🧠 Learning (সবচেয়ে গুরুত্বপূর্ণ)

---

## 🚨 Incident 1: Production suddenly slow / API timeout

### 🔴 Problem

* কিছু API response time হঠাৎ 10–15 সেকেন্ড
* User complaint আসছে
* Server CPU normal, কিন্তু request pile-up

---

### 🔍 Investigation (Senior thinking)

আমি চেক করেছি:

1. **Logs** → কোন endpoint slow?
2. **Metrics** → response time spike
3. **DB query logs** → long-running query

👉发现:

* একটি API loop-এর ভিতরে DB call করছে
* N+1 query problem

---

### 🛠️ Fix

* Query optimize
* JOIN / eager loading ব্যবহার
* Redis cache add করা

---

### 🧠 Learning (Interview gold)

> “Code correct হওয়া মানেই production-ready না।
> Data access pattern ভুল হলে system ধীরে মরে।”

---

## 🚨 Incident 2: Duplicate Order / Double Payment

### 🔴 Problem

* কিছু user-এর order দুইবার create হচ্ছে
* Payment gateway retry করলে issue বেশি

---

### 🔍 Investigation

* API retry হচ্ছে (network failure)
* POST endpoint **idempotent না**
* Same request দুইবার process হচ্ছে

---

### 🛠️ Fix

* Idempotency key introduce করা
* Unique constraint DB-তে
* Business logic level guard

---

### 🧠 Learning

> “Distributed system-এ retry normal,
> Architecture-কে retry-safe বানাতে হয়।”

---

## 🚨 Incident 3: Memory leak → server crash

### 🔴 Problem

* Server কয়েক ঘণ্টা পর পর crash
* Restart দিলে ঠিক, আবার leak

---

### 🔍 Investigation

* Memory graph analysis
  -发现:

  * Static in-memory cache
  * No eviction strategy

---

### 🛠️ Fix

* Redis external cache
* TTL set করা
* Remove static collections

---

### 🧠 Learning

> “In-memory optimization production-এ silent killer হতে পারে।”

---

## 🚨 Incident 4: Production bug but cannot reproduce locally

### 🔴 Problem

* Production-only error
* Local / staging-এ reproduce হচ্ছে না

---

### 🔍 Investigation

* Config difference
* Environment variable mismatch
* Missing feature flag

---

### 🛠️ Fix

* Config centralization
* Env parity ensured
* Better logging added

---

### 🧠 Learning

> “If environments are different, bugs are guaranteed.”

---

## 🚨 Incident 5: Deployment caused downtime

### 🔴 Problem

* New release-এর পর 5 min downtime
* Users logged out

---

### 🔍 Investigation

* Server restart = active request killed
* No graceful shutdown

---

### 🛠️ Fix

* Graceful shutdown implemented
* Load balancer health check
* Rolling deployment

---

### 🧠 Learning

> “Deployment is also part of architecture.”

---

## 🎯 Interview-এ এই প্রশ্ন এলে কীভাবে বলবে?

### Question:

**“Tell me about a production issue you handled.”**

### STAR-style Answer Template:

```
Situation: Production slow / error
Task: Identify root cause quickly
Action: Used logs, metrics, fixed architecture issue
Result: Downtime reduced, system stable
Learning: Improved architecture / monitoring
```

---

## 🧠 Senior Engineer-এর চিন্তার Pattern

| Junior         | Senior              |
| -------------- | ------------------- |
| Bug fix        | Root cause          |
| Restart server | Fix architecture    |
| Code-level     | System-level        |
| Now works      | Works under failure |

---



---

# 🔥 .NET Production Incidents – Deep Dive

---

## 🚨 Incident 1: Thread Pool Exhaustion (ASP.NET)

### 🔴 Incident

* API random time-out দিচ্ছে
* CPU low, Memory OK
* Server alive কিন্তু request hang

---

### 🔍 Root Cause

* `.Result` / `.Wait()` ব্যবহার করা হয়েছে async method-এর উপর
* Thread pool block হয়ে গেছে

```csharp
var data = _service.GetDataAsync().Result; // ❌
```

---

### 🛠️ Fix

* Full async/await chain

```csharp
var data = await _service.GetDataAsync(); // ✅
```

---

### 🧠 Prevention

> “In ASP.NET, blocking calls = silent killer”

---

## 🚨 Incident 2: Memory Leak due to Singleton misuse

### 🔴 Incident

* Server কয়েক ঘণ্টা পর crash
* GC pressure বেড়ে যাচ্ছে

---

### 🔍 Root Cause

* `Singleton` service-এ DbContext inject করা

```csharp
services.AddSingleton<MyService>(); // ❌
```

DbContext = Scoped

---

### 🛠️ Fix

* Correct DI lifetime

```csharp
services.AddScoped<MyService>(); // ✅
```

---

### 🧠 Prevention

> “Lifetime mismatch is the most common .NET production bug.”

---

## 🚨 Incident 3: EF Core N+1 Query Problem

### 🔴 Incident

* API slow with large dataset
* DB CPU high

---

### 🔍 Root Cause

Lazy loading inside loop

```csharp
foreach (var o in orders)
{
   o.Customer.Name; // DB hit each time
}
```

---

### 🛠️ Fix

* Eager loading

```csharp
_context.Orders.Include(o => o.Customer);
```

---

### 🧠 Prevention

> “ORM hides complexity, not cost.”

---

## 🚨 Incident 4: Connection Pool Exhaustion (SQL Server)

### 🔴 Incident

* Timeout expired
* App restart fixes temporarily

---

### 🔍 Root Cause

* DbConnection not disposed properly
* `using` missing

---

### 🛠️ Fix

* Ensure `using` or DI-managed DbContext

---

### 🧠 Prevention

> “Leaking connections kills scalability.”

---

## 🚨 Incident 5: Configuration Bug (appsettings)

### 🔴 Incident

* Production-only failure
* Staging works fine

---

### 🔍 Root Cause

* `ASPNETCORE_ENVIRONMENT` mismatch
* Missing config value

---

### 🛠️ Fix

* Environment parity
* Startup validation

---

### 🧠 Prevention

> “If config is optional, bug is mandatory.”

---

## 🚨 Incident 6: Unhandled Exception → App Crash

### 🔴 Incident

* App suddenly down
* No clear error

---

### 🔍 Root Cause

* No global exception handling middleware

---

### 🛠️ Fix

```csharp
app.UseExceptionHandler("/error");
```

---

### 🧠 Prevention

> “Unhandled exception = uncontrolled outage.”

---

## 🚨 Incident 7: High GC Pause (Large Object Heap)

### 🔴 Incident

* Random latency spikes
* Memory usage fluctuates

---

### 🔍 Root Cause

* Large byte[] allocations (>85KB)
* LOH fragmentation

---

### 🛠️ Fix

* Stream processing
* Array pooling

---

### 🧠 Prevention

> “Memory patterns matter more than memory size.”

---

## 🚨 Incident 8: JWT Token Bug (Auth Failure)

### 🔴 Incident

* Users auto logout
* Token suddenly invalid

---

### 🔍 Root Cause

* Server restart invalidates in-memory key
* Clock skew issue

---

### 🛠️ Fix

* Centralized key store
* Clock sync
* Refresh token

---

### 🧠 Prevention

> “Auth is state, treat it carefully.”

---

## 🚨 Incident 9: Background Service Crash

### 🔴 Incident

* HostedService stops silently
* No alert

---

### 🔍 Root Cause

* Exception not handled inside `ExecuteAsync`

---

### 🛠️ Fix

* try-catch + retry policy

---

### 🧠 Prevention

> “Background jobs need supervision.”

---

## 🚨 Incident 10: Deployment Caused Downtime

### 🔴 Incident

* IIS recycle → active request lost

---

### 🔍 Root Cause

* No graceful shutdown

---

### 🛠️ Fix

* `IHostApplicationLifetime`
* Health checks
* Load balancer support

---

### 🧠 Prevention

> “Deployment is runtime behavior.”

---

## 🎯 Interview Gold: One Structured Answer

**Question:**

> “Have you handled production issues in .NET?”

**Answer Template:**

```
Yes. One incident was thread pool exhaustion caused by blocking async calls.
I analyzed metrics, found blocked threads, refactored to async/await.
After fix, timeout reduced by 90%.
```

---

## 🧠 Senior-Level Mindset (Remember This)

| Junior  | Senior     |
| ------- | ---------- |
| Fix bug | Fix system |
| Restart | Root cause |
| Guess   | Measure    |
| Panic   | Observe    |

---





