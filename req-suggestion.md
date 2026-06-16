# Requirements Gap Analysis

## 1. Metadata

```
Requirements Fit Score: 79/100
Requirements Source: req.txt (project root)
Target Role (inferred): Backend Developer (Node.js / Nest.js) — 0–1 YOE, On Premise
Resume Author: Samir Shaikh
```

## 2. Requirements Coverage Table

| # | Requirement | Category | Priority | Coverage | Risk | Evidence Location |
|---|---|---|---|---|---|---|
| R1 | Node.js experience | Hard Skill | P0 | **Full** | Low | Summary, Experience, Projects 1–3, Technical Skills |
| R2 | Nest.js experience | Hard Skill | P0 | **Partial** | **High** | Technical Skills line (listed but no project evidence) |
| R3 | TypeScript proficiency | Hard Skill | P0 | **Full** | Low | Sahara Tyre (TS), Eventifyy (TS), Technical Skills |
| R4 | RESTful API design & implementation | Hard Skill | P0 | **Full** | Low | Summary, Eventifyy, 2FA, Sahara Tyre, Technical Skills |
| R5 | SQL & NoSQL database + data modeling | Hard Skill | P0 | **Full** | Low | PostgreSQL (Eventifyy), MongoDB (2FA), Firebase, Skills line |
| R6 | Version control (Git) | Hard Skill | P0 | **Full** | Low | GitHub links on all projects, GitHub Actions CI/CD, Skills |
| R7 | JavaScript proficiency | Hard Skill | P0 | **Full** | Low | All projects in JS/TS, Skills line (ES6+) |
| R8 | Async programming & event-driven architecture | Hard Skill | P0 | **Full** | Low | Sahara ("concurrent batch processing", "real-time"), Socket.io in skills |
| R9 | Problem-solving skills | Soft Skill | P0 | **Full** | Low | Experience bullet ("strengthened problem-solving"), Skills line |
| R10 | Communication & collaboration | Soft Skill | P0 | **Full** | Low | Soft skills line, Experience ("multiple products", "diverse patterns") |
| R11 | Bachelor's degree (CS/Engineering/related) | Education | P0 | **Full** | Low | Education section — B.Tech IT, 2022–2026 |
| R12 | Express.js experience | Hard Skill | P1 | **Full** | Low | Sahara, Eventifyy, 2FA — all use Express |
| R13 | Third-party service integration | Hard Skill | P1 | **Full** | Low | Dittofeed, Reoon, Google Sheets API, WhatsApp Web API, Nodemailer |
| R14 | Code review participation | Process | P1 | **Missing** | **High** | No mention anywhere |
| R15 | Agile development familiarity | Process | P1 | **Missing** | **High** | Not mentioned anywhere |
| R16 | Security best practices | Hard Skill | P1 | **Full** | Low | 2FA project (Helmet, bcrypt, rate limiting), Eventifyy (CORS, Zod) |
| R17 | Performance optimization | Hard Skill | P1 | **Partial** | Medium | Sahara ("rate-limit-safe"), Experience ("improved system performance") — no metrics |

## 3. Gap Analysis by Category

### Must-Have Gaps (P0)

- **R2** — **Nest.js listed but zero project evidence.** The job title *is* "Node.js and Nest.js Developer", yet NestJS appears only as a bullet in Technical Skills. No project, no code sample, no deployment uses NestJS. This is the single biggest credibility gap.

### Nice-to-Have Gaps (P1)

- **R14** — **Code review experience is completely absent.** The JD lists "Conduct code reviews and ensure adherence to best practices and coding standards" as a responsibility. Resume says nothing about reviewing peers' code or establishing standards.
- **R15** — **Agile methodology not mentioned.** No reference to sprints, standups, retrospectives, or working in an Agile team despite this being listed under Qualifications.
- **R17** — **Performance optimization claims lack metrics.** "Improved system performance" and "rate-limit-safe randomized delays" are qualitative. No before/after numbers, no throughput/response-time data.

### Evidence Depth Issues

- **NestJS** (R2) — claimed in skills, nowhere else. Credibility risk: may be filtered out at ATS or interview stage.
- **Kafka / BullMQ / Message Queues** listed in skills but never used in any project. Not required by the JD but if included, should be demonstrated.
- **Monitoring stack** (OpenTelemetry, Prometheus, Grafana) — listed but never used in any project description.

## 4. Critical Issues (Priority Order)

1. **NestJS — claimed without proof (R2, P0 blocker).** The entire role is framed around Node.js + Nest.js. The resume must include at minimum one project or a significant code example using NestJS (modules, decorators, dependency injection, guards). Without this, the application looks misaligned.

2. **Code review experience missing (R14, P1).** The JD explicitly requires this. Even a single line like "Reviewed 5+ peer PRs per week, enforcing TypeScript strict-mode compliance and test coverage thresholds" would close this gap.

3. **Agile methodology absent (R15, P1).** The candidate's internship at Logicwind likely used some Agile process. Needs to be surfaced. A single bullet: "Participated in daily standups, sprint planning, and retrospectives within a 4-person backend team using Agile/Scrum."

4. **Performance improvements unquantified (R17, P1 partial).** "Improved system performance" carries no weight. Replace with concrete metrics: "Reduced API p95 latency by 40% by optimizing N+1 queries" (if true) or similar.

5. **On-premise location risk.** The job is "On Premise" with no location stated. The candidate is in Vapi, Gujarat. If the job is in a different city, relocation willingness should be stated explicitly in the resume header or summary.

## 5. Suggested Rewrites (Before → After)

| Before | After |
|---|---|
| *NestJS* (in skills only, no project) | Add a project: "Built a modular NestJS microservice with dependency-injected services, guards for RBAC, and interceptors for structured logging — deployed via Docker Compose." |
| *Contributed to multiple products across microservices, Firebase-based apps, and scalable backend architectures* | "Delivered features across 3+ products (microservices, Firebase, monolithic backends) in a **biweekly Agile sprint cycle with code reviews, standups, and retrospectives**." |
| *Improved system performance across existing applications* | "Optimized API response times by ~30% through query tuning and caching layer implementation." |
| (No code review mention) | "Reviewed 10+ peer pull requests, enforcing TypeScript strict-mode, test coverage, and NestJS best practices." |

## 6. Missing Keywords vs Requirements

| Keyword | Required? | In Resume? |
|---|---|---|
| Nest.js / NestJS | **Yes (P0)** | Listed but no evidence |
| Code review | Yes | **No** |
| Agile / Scrum | Yes | **No** |
| Sprint | Yes | **No** |
| Performance optimization | Yes | Partial (no metrics) |
| Event-driven architecture | Yes | Implicit (Socket.io, batch processing) — should be explicit |
| Data modeling | Yes | Implicit (Sequelize ORM, MongoDB schemas) — should be explicit |
| Scalability | Yes | Mentioned in summary but not quantified |
| Competitive salary | No (Company offer) | N/A |
| Professional development | No (Company offer) | N/A |

## 7. Skills Section — Recommended Changes

| Action | Change |
|---|---|
| **Add** | Agile methodologies / Scrum |
| **Demonstrate NestJS** | Move NestJS out of skills-only — add it to a project OR create a small NestJS project and link it |
| **Keep** | Node.js, Express.js, TypeScript, PostgreSQL, MongoDB, Git — all well-evidenced |
| **Questionable** | Kafka, BullMQ, Prometheus, Grafana, OpenTelemetry — listed without evidence. Either add project proof or remove to avoid credibility loss at interview |

## 8. Interview Questions (Requirements-Gap Driven)

### Technical

1. **R2 (NestJS gap):** "You list NestJS on your resume but none of your projects use it. Can you walk me through how you'd structure a NestJS application — modules, controllers, services, guards, and interceptors — and how that differs from Express?"
2. **R17 (Performance):** "You mention 'improved system performance' at Logicwind. What specific metrics did you track, what tools did you use to measure them, and what was the before/after?"
3. **R8 (Async/event-driven):** "Your Sahara Tyre project uses 'concurrent batch processing with rate-limit-safe randomized delays.' Walk me through the concurrency model — what happens when the rate limit is hit mid-batch?"

### Behavioral

4. **R14 (Code review):** "Have you ever had a pull request rejected or had to reject someone else's? Walk me through how you handled the feedback conversation."
5. **R15 (Agile):** "Tell me about a time you had to reprioritize work mid-sprint due to changing requirements. How did you handle it?"

### System Design

6. **R5 + R8:** "Design a real-time notification system for an event management platform. Walk through your database schema (SQL + NoSQL choices), message queue integration, and how you'd ensure delivery guarantees."
