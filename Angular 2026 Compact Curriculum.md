
---

# 🏆 **Angular 2026 Compact Curriculum**

---

## **Phase 0 — Environment Setup & Angular Overview (1 Week)**

**শিখবেন:**

* Angular & SPA (Single Page Application) কি এবং কেন
* Node.js, npm, Angular CLI, VS Code setup
* Angular project structure (`ng new`, `ng serve`, `ng generate component`)
* Version differences overview (Angular 2 → Angular 18)

**Interview Q:**

1. Angular কি? SPA কেন ব্যবহার করা হয়?
2. Angular CLI কী? সুবিধা কি?
3. Angular 2 থেকে Angular 16 পর্যন্ত major changes কি কি?

**Real-world tip:**
প্রথমে simple dashboard বানান যেখানে Home, About page আছে এবং Routing + API calls integration করা আছে।

---

## **Phase 1 — TypeScript Deep Dive (1 Week)**

**শিখবেন:**

* Basic Types, Union, Enum, Interface
* Classes, Decorators (`@Component`, `@Injectable`)
* Modules & Imports

**Interview Q:**

1. Interface vs Class পার্থক্য?
2. Decorators কেন ব্যবহার হয় Angular-এ?

**Real-world tip:**
Login/Register module বানাতে TypeScript classes + interfaces ব্যবহার করুন।

---

## **Phase 2 — Components & Templates (2 Weeks)**

**শিখবেন:**

* Component creation & template syntax
* Data binding: Property, Event, Two-way
* Lifecycle hooks (`ngOnInit`, `ngOnChanges`, `ngOnDestroy`)
* Component Styling & Encapsulation

**Interview Q:**

1. `ngOnInit` vs Constructor?
2. Lifecycle hooks performance-critical কি?

**Real-world tip:**
Navbar, Dropdown, Modal UI তৈরি করুন। Component encapsulation ব্যবহার করে CSS conflict কমান।

---

## **Phase 3 — Services, Dependency Injection & HTTP (2 Weeks)**

**শিখবেন:**

* Angular Services creation & DI
* HttpClient, Observables, RxJS basics
* Interceptors, Error handling
* Routing, Route Guards, Lazy Loading

**Interview Q:**

1. Lazy Loading vs Eager Loading?
2. Route Guards কেন ব্যবহার হয়?
3. HTTP Interceptor কী?

**Real-world tip:**
JWT token authentication দিয়ে API integration করুন। Lazy load Dashboard module।

---

## **Phase 4 — Forms & Validation (2 Weeks)**

**শিখবেন:**

* Template-driven Forms
* Reactive Forms (`FormGroup`, `FormControl`, `FormBuilder`)
* Custom & Async Validators
* Dynamic forms

**Interview Q:**

1. Reactive vs Template-driven forms?
2. Custom validator কিভাবে করবেন?

**Real-world tip:**
Login/Register + Profile Update ফর্ম বানান। Validation + Submit logic integrate করুন।

---

## **Phase 5 — RxJS & Signals (2–3 Weeks)**

**শিখবেন:**

* Observables, Subjects, BehaviorSubjects
* Operators: `map`, `switchMap`, `mergeMap`
* Signals (v16+), Computed signals, Effects
* Combining RxJS with Signals

**Interview Q:**

1. Observable vs Promise
2. switchMap vs mergeMap
3. Signals vs RxJS পার্থক্য

**Real-world tip:**
Live search feature বানান: API call debounce + Signal based state।

---

## **Phase 6 — Change Detection & Performance (2 Weeks)**

**শিখবেন:**

* Change Detection (Default vs OnPush)
* trackBy in `*ngFor`, Web Workers
* Partial hydration & SSR (v16+)

**Interview Q:**

1. OnPush কেন ব্যবহার করবেন?
2. trackBy কেন দরকার?

**Real-world tip:**
লম্বা লিস্ট UI তৈরি করুন এবং performance optimization দেখান।

---

## **Phase 7 — State Management (2–3 Weeks)**

**শিখবেন:**

* Service + BehaviorSubject State
* NgRx (Store, Actions, Reducers, Effects)
* Signals state approach

**Interview Q:**

1. NgRx core parts?
2. Local vs Global State?
3. Signals advantages?

**Real-world tip:**
Shopping Cart: Add/Remove, Persist state, Observable + Signal integration।

---

## **Phase 8 — Security (1 Week)**

**শিখবেন:**

* JWT Authentication, OAuth2 basics
* Route protection
* XSS & CSRF prevention

**Interview Q:**

1. Angular-এ CSRF কিভাবে প্রতিরোধ করবেন?
2. Route protection কিভাবে করবেন?

**Real-world tip:**
Secure Dashboard module বানান। Protected routes + token verification।

---

## **Phase 9 — Testing (1–2 Weeks)**

**শিখবেন:**

* Jasmine / Karma basics
* Unit Testing, Integration Testing
* Testing HTTP, Router, Component

**Interview Q:**

1. Unit vs Integration test পার্থক্য?
2. Async test কিভাবে করবেন?

**Real-world tip:**
Login/Register module + HTTP service test লিখুন।

---

## **Phase 10 — Deployment & Optimization (1–2 Weeks)**

**শিখবেন:**

* Production Build (`ng build --prod`)
* AWS S3 Hosting, CloudFront CDN
* Route53 + SSL
* AOT, Tree-shaking, Bundle Optimization

**Interview Q:**

1. Angular Production build optimization কিভাবে হয়?
2. AOT এবং Tree-shaking কি?

**Real-world tip:**
Production-ready SPA deploy করুন AWS S3 + CloudFront + Custom domain + HTTPS।

---

## **Phase 11 — Angular Versions & Differences**

| Version       | Key Features                     | Real-world Use                             |
| ------------- | -------------------------------- | ------------------------------------------ |
| Angular 2     | TS-based, Components, Modules    | SPA structure                              |
| Angular 4–5   | Animations, HttpClient           | Smaller bundles, API integration           |
| Angular 6–7   | Elements, Drag&Drop, ng update   | Web components, better UI                  |
| Angular 8     | Differential loading, Ivy opt-in | Faster runtime                             |
| Angular 9     | Ivy default                      | Faster rendering, smaller bundle           |
| Angular 14    | Standalone Components            | Module-less feature modules                |
| Angular 16    | Signals, Partial hydration       | Fine-grained reactive UI, SSR optimization |
| Angular 17–18 | Micro-frontends, optimized SSR   | Large enterprise apps, modular deployment  |

**Interview Q:**

1. Ivy Renderer কী এবং কেন Angular 9+ default হলো?
2. Standalone Components vs Module Components?
3. Signals vs RxJS?
4. Partial Hydration কী?
5. Micro-frontends (Angular 18 preview) কীভাবে কাজ করে?

---

## **Phase 12 — Real-world Mini Projects**

1. Simple Dashboard (CRUD + Auth)
2. E-commerce UI (Cart + Wishlist + State)
3. Live Search + Signal/RxJS Integration
4. Feature Flags + Lazy Modules

**Tip:** Projects করার সময় সব নতুন Angular ফিচার (Signals, Standalone Components, Lazy Loading, State Management) integrate করুন।

---

