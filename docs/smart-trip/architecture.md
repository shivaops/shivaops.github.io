# Solution & Architecture

## Solution Summary
Smart Trip has two main layers.

### Core Booking Engine
Handles the structured business process:

- flight search
- result display
- fare selection
- traveler selection
- booking
- payment
- itinerary generation

### AI Assistant Layer
Helps the user by:

- capturing travel intent in plain language
- identifying missing details
- confirming unclear dates
- converting conversation into structured search input

The AI layer is an assistant only. It does not replace the booking engine.

## High-Level Architecture
The application is built using the following main parts:

- **Frontend:** HTML, CSS, JavaScript, Jinja2 templates
- **Backend:** FastAPI
- **Database:** MySQL
- **AI orchestration:** LangGraph / LangChain style flow
- **Provider simulator:** Search, booking, and payment APIs
- **Output:** Booking summary, itinerary view, PDF download

## Architectural value
This design keeps AI support on top of a structured system, which makes the whole application easier to explain, validate, and demonstrate.
