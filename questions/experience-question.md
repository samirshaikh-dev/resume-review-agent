# Experience — Probing Questions

This file contains targeted interview questions based on the candidate's professional experience at **Xira Infotech** and **Logicwind**.

---

## 1. Full Stack Engineer — Xira Infotech (Aug 2026 – Sep 2026)

### Technical Depth & End-to-End Delivery
1. **End-to-End Architecture**: You owned delivery of the dynamic job portal from PostgreSQL schema design through the Next.js UI. Can you walk through your data model for handling job postings, multi-status applications, resume file attachments, and complex search filters?
2. **Search & Filtering Performance**: How did you implement advanced search and filtering in PostgreSQL? Did you leverage Full-Text Search (TSVECTOR/TSQUERY), trigram indices (pg_trgm), or an external search engine? How did you maintain sub-100ms query performance with concurrent filters?
3. **Next.js Rendering Strategy**: Which Next.js rendering paradigm (SSR, SSG, ISR, or Client Components / Server Actions) did you select for the job listings page versus the application tracking dashboard, and what were the SEO vs. real-time latency trade-offs?

### Authentication, Security & RBAC
1. **Role-Based Access Control**: How was RBAC implemented across the API and the Next.js UI to ensure internal teams, recruiters, and applicants have strictly segregated permissions? How did you prevent Insecure Direct Object References (IDOR) on resume downloads and application statuses?
2. **Admin Dashboard Autonomy**: What design patterns or UI components did you build to allow non-engineering internal teams to manage listings, candidate pipelines, and user roles safely without causing schema or data inconsistencies?

### Integrations & Transactions
1. **Payment Gateway Workflows**: Which payment gateway did you integrate (e.g., Razorpay, Stripe), and how did you handle asynchronous webhook events, idempotent charge verification, payment failure retries, and reconciliation?
2. **Real-Time Notifications**: How were real-time notifications implemented (e.g., WebSockets, Server-Sent Events, or push services)? How did you ensure reliable delivery if an applicant or recruiter was temporarily offline?

### Performance & Profiling
1. **Backend Profiling & Low Latency**: You mentioned profiling and refactoring REST APIs to keep response times low as feature surface expanded. What tools (e.g., Node.js clinic, pg_stat_statements, APM) did you use to profile bottlenecks, and what was the most impactful refactor you performed?

---

## 2. Backend Developer Intern — Logicwind (Sep 2025 – May 2026)

### Technical Depth & Optimization
1. **Query & Schema Migrations**: You achieved a ~30% reduction in API response times for real users. Walk me through how you profiled the bottlenecks, and provide a concrete example of a PostgreSQL query or schema migration you executed to achieve this.
2. **Redis Caching Layer**: How was the Redis caching layer designed? What was your cache invalidation strategy (e.g., cache-aside, write-through, TTLs), and how did you mitigate risks like cache stampedes or stale reads?

### Architecture & Microservices
1. **Event-Driven Architecture**: What patterns did you use for asynchronous API endpoints and event-driven communication across microservices in Node.js? How did you manage distributed error handling, message retries, and dead-letter queues?
2. **Scalability & Connection Pooling**: How did you manage database connection pooling (e.g., PgBouncer) across distributed microservices under heavy load?

### Integrations & Automation
1. **Email & Validation Pipeline**: You integrated Dittofeed, Reoon Email Verifier, and Loops. What was the architecture of this pipeline, and how did you handle rate-limiting, backpressure, and third-party downtime?
2. **AI-Assisted Development**: How did you incorporate AI-assisted workflows into architecture planning and debugging without compromising code security or introducing hallucinations into production?

### Collaboration & QA
1. **Edge-Case Resolution**: Can you share a specific edge-case production bug you diagnosed and resolved alongside the QA team?
2. **API Documentation**: How did you document your REST/asynchronous APIs and data contracts to streamline cross-team development in Agile sprints?
