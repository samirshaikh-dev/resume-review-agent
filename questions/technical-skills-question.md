# Technical Skills — Probing Questions

This file contains targeted questions probing the candidate's core **Technical Skills**.

## Tech Stack Depth & Frameworks
1. **Frontend Architecture**: You listed both Next.js and React.js (Hooks, Component Architecture, State Management). How do you approach Server Components vs. Client Components in Next.js, and when do you reach for Redux versus the Context API?
2. **Databases & Data Modeling**: You list PostgreSQL, MongoDB, MySQL, and Redis. How do you decide when to choose a relational database (PostgreSQL/MySQL) versus NoSQL (MongoDB)? Compare their transaction isolation models, indexing strategies, and migration complexities.
3. **Caching & Low Latency**: You list Redis and Caching under concepts. What caching strategies (e.g., Cache-Aside, Write-Through, Write-Behind) have you implemented in production, and how do you handle cache invalidation and distributed locking?

## Backend, APIs & Payment Integration
1. **Payment Gateways & Webhooks**: You listed Payment Gateways & Webhooks under Backend & APIs. How do you design an idempotent webhook receiver in Express.js/Node.js to handle network timeouts, duplicated events, and signature verification?
2. **RESTful API Design & Profiling**: How do you profile Node.js REST APIs under load, and what specific tools or techniques do you use to identify event loop lag, memory leaks, or unindexed database queries?

## Security, Auth & RBAC
1. **RBAC Implementation**: How do you model and enforce Role-Based Access Control (RBAC) across both the database layer and API middleware? How do you defend against privilege escalation and IDOR attacks?
2. **API Security Standards**: Beyond JWT and bcrypt, how do you protect production REST/GraphQL APIs against common vulnerabilities (e.g., CSRF, rate limit exhaustion, SQL injection, NoSQL injection)?

## Messaging & Observability
1. **Messaging Queues**: What are the operational differences between BullMQ (Redis-backed) and Apache Kafka, and when is each appropriate for asynchronous task handling versus event stream processing?
2. **Metrics & Monitoring**: How do you configure Prometheus metrics and Grafana dashboards to monitor Node.js application health (p95/p99 latency, error rates, throughput)?
