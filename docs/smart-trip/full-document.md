# Smart Trip – AI-Assisted Airline Booking Simulator

<p align="center">
  <img src="../../assets/images/smarttrip.png" alt="Smart Trip Thumbnail" width="350">
</p>

## 1. Overview
Smart Trip is an AI-assisted travel booking application that simulates a realistic airline booking journey from flight search to booking, payment, and itinerary generation.

The solution combines two modes of interaction:
- **Structured booking flow** through normal application screens
- **AI-assisted conversation flow** through a chat interface

The main idea is simple: the booking engine remains controlled and rule-based, while the AI layer helps the user provide travel details in natural language and then routes the request into the normal application flow.

---

## 2. Objective
The goal of Smart Trip is to demonstrate a full working travel booking simulator that:
- feels like a real airline or travel portal
- supports search, booking, payment, and itinerary flow
- uses simulated API-based provider interaction
- adds an AI assistant without disturbing the core business logic

---

## 3. Scope
### Included
- One-way and round-trip search
- Fare selection
- Traveler selection from saved records
- Booking confirmation
- Payment simulation
- Booking summary and itinerary PDF
- AI chat-based travel request handling
- Audit logging and traceability

### Not Included
- Real airline integration
- Real payment gateway
- Hotel or car booking
- Enterprise-grade production security

---

## 4. Solution Summary
Smart Trip has two main layers.

### 4.1 Core Booking Engine
Handles the structured business process:
- flight search
- result display
- fare selection
- traveler selection
- booking
- payment
- itinerary generation

### 4.2 AI Assistant Layer
Helps the user by:
- capturing travel intent in plain language
- identifying missing details
- confirming unclear dates
- converting conversation into structured search input

The AI layer is an assistant only. It does not replace the booking engine.

---

## 5. High-Level Architecture
The application is built using the following main parts:

- **Frontend:** HTML, CSS, JavaScript, Jinja2 templates
- **Backend:** FastAPI
- **Database:** MySQL
- **AI orchestration:** LangGraph / LangChain style flow
- **Provider simulator:** Search, booking, and payment APIs
- **Output:** Booking summary, itinerary view, PDF download

---

## 6. Main Functional Modules
### Flight Search
Captures route, travel date, cabin, currency, and passenger details, then fetches matching flights.

### Fare Selection
Displays available fare families with details such as baggage, refundability, and change rules.

### Traveler Management
Allows users to select saved travelers instead of typing details again.

### Booking
Builds booking payload, calls booking API, and stores booking reference and details.

### Payment
Simulates payment processing and updates booking payment status.

### Itinerary
Provides final journey details and downloadable PDF output.

### AI Chat
Accepts travel requests in natural language and guides the user into the normal booking process.

### Audit Logging
Captures important user and system events for traceability and debugging.

---

## 7. End-to-End Flow
Typical flow:

1. User starts from search page or AI chat
2. Travel details are captured
3. System validates and normalizes input
4. Search API is called
5. Flight options are shown
6. User selects flight and fare
7. User selects travelers
8. Booking is confirmed
9. Payment is completed
10. Booking summary and itinerary are shown

---

## 8. AI Flow Summary
In chat mode, the system follows these steps:

1. Read user travel request
2. Extract important details
3. Check for missing fields
4. Ask for clarification if needed
5. Confirm ambiguous dates
6. Build structured request
7. Pass it into the normal booking engine

This keeps the AI flow flexible for the user but controlled for the system.

---

## 9. Design Principles
Smart Trip is based on these key principles:

- **Configuration-driven design** to reduce hardcoding
- **AI as helper, not decision-maker**
- **Separation of concerns** between UI, AI, business logic, and provider simulation
- **Auditability** for traceable behavior
- **Professional guided user experience**

---

## 10. Strengths
Smart Trip demonstrates:
- complete travel booking life cycle
- realistic application flow
- AI-assisted conversation with controlled routing
- strong demo value for portfolio and presentation
- extensible architecture for future enhancement

---

## 11. Current Limitations
Current limitations include:
- simulated provider APIs only
- simulated payment flow only
- limited business scope compared to enterprise travel systems
- AI still depends on strong application-side validation

---

## 12. Future Enhancement Options
Possible improvements:
- real airline API integration
- real payment integration
- hotel and car booking modules
- stronger session persistence
- analytics dashboard
- production deployment model
- stronger security and role management

---

## 13. Conclusion
Smart Trip is a practical demonstration of how AI can be added on top of a structured business application without replacing core rules and validations.

It is useful as a portfolio project, technical demo, and discussion piece for AI-assisted software development because it shows a realistic working flow from search to itinerary generation.

---
