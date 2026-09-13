# Eventify — Probing Questions

This file contains targeted interview questions for the project **Eventify — Full-Stack Event Management Platform**.

## Architecture & Design
1. You mentioned designing data models in MongoDB. How did you design the schema for events, users, and ticket purchases/bookings? What indices did you create to support frequent queries (e.g., searching events by date/location)?
2. How does the role-based access control (RBAC) work within your API? How did you protect routes and ensure that only authorized users can modify or delete events?
3. What design patterns or architectural styles did you use in the React frontend to manage state and components cleanly?

## Tech Stack Depth
1. What was the rationale behind choosing a hybrid REST and GraphQL (Apollo) API? Which parts of the app use GraphQL, and which parts use REST?
2. How did you set up optimized connection pooling in MongoDB/Mongoose? What were the connection settings, and how do you handle scaling connections?
3. How did you structure JWT session management? Where are tokens stored on the client side, and how do you protect against XSS and CSRF?

## System Design & Scalability
1. If the platform experiences a sudden spike in ticket booking requests (e.g., when a popular event goes live), how would you scale the architecture to handle the concurrent write load?
2. What rate limiting strategies did you implement? How do they function under high traffic?
3. How is Nodemailer integrated? How do you ensure emails are sent reliably without blocking the main event loop?

## Fundamentals & Verification
1. Walk me through the security checks in your authentication pipeline. How does bcrypt hashing and SHA-256 OTP verification fit in?
2. How does Zod payload validation help at runtime compared to TypeScript compile-time checks?
