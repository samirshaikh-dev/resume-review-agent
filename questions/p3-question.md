# Sahara Tyre — Probing Questions

This file contains targeted interview questions for the project **Sahara Tyre -- WhatsApp Promotional Campaign Platform**.

## Architecture & Design
1. How does the integration with `whatsapp-web.js` work? How do you maintain session persistence (e.g., authentication state, QR code pairing) when the Node.js/Express server restarts?
2. You built a React Native (Expo) mobile client. How did you structure the mobile client to consume the Node.js backend REST APIs? How did you handle user authentication and session tokens on mobile?
3. How did you structure the Socket.io state synchronization to update the React Native app in real time when messages are sent or failed?

## Tech Stack Depth
1. What was the rationale behind choosing Google Sheets API as a backend/data source? What limitations did you hit (e.g., rate limits, concurrent writes, structural changes), and how did you design around them?
2. How is the rate-limited batch processing designed to ensure WhatsApp's third-party guidelines are respected? What happens if a batch partially fails?
3. Walk me through the automated deployment using GitHub Actions and Render. How do you handle continuous integration and zero-downtime deployments while active campaigns might be running?

## System Design & Scalability
1. If the platform needs to scale to support dozens of concurrent campaigns, how would you design session persistence and socket communication to handle the increased load?
2. What precautions did you take on the backend stack to secure API keys for the Google Sheets API and WhatsApp Web API in production?
