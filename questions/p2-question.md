# AI Customer Ticket — Probing Questions

This file contains targeted interview questions for the project **AI Customer Ticket -- Microservice-Based Support Automation Platform**.

## Architecture & Design
1. Walk me through the layout of your 6+ Express.js microservice architecture. How are duties divided among them, and how do they coordinate to handle customer tickets?
2. You used PostgreSQL with Sequelize ORM. How did you structure the schema for support tickets, SLAs, and customer feedback? What challenges did you face with database sync or connection pooling across multiple microservices?
3. How did you deploy your DevOps stack? How do Prometheus and Grafana gather metrics from separate Docker containers?

## Tech Stack Depth
1. What was the rationale behind choosing Next.js and React for the frontend dashboard? How did you utilize Context API-driven state management to handle SLA monitoring and dynamic AI scoring?
2. You used HTTP Long Polling for sub-second real-time ticket synchronization. Why did you choose Long Polling over WebSockets or Server-Sent Events (SSE)? What challenges did you encounter regarding connection limits or server resources?
3. How is BullMQ integrated with Redis to manage classification and scoring jobs? What are your job retry, rate limiting, and failure handling policies?

## System Design & Scalability
1. If the rate of incoming support tickets increases by 10x, how does the BullMQ-based background worker pool scale to handle the increased classification traffic?
2. Walk me through the LLM classification pipeline. How did you integrate the LLM API, and how do you handle rate-limits, API downtime, or long response times from the model?
3. How did you handle distributed tracing across all the microservices? How does a request get tracked from the gateway to individual services in Grafana/Prometheus?

## Fundamentals & Verification
1. What were the specific AI-assisted development tools (e.g., OpenCode, Kilocode) used during implementation? How did you verify the accuracy of the classification logic generated with their help?
2. How do you handle database migrations across all microservices using Sequelize ORM in a production deployment?
