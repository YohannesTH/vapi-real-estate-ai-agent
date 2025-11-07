# 🏡 VAPI Smart Real Estate Scheduler

**VAPI Smart Real Estate Scheduler** is an AI-powered voice automation system built for real estate businesses.  
It uses **VAPI**’s voice agent capabilities to handle client qualification, check availability, and book property appointments via **Google Calendar** — all through natural, human-like conversations.

---

## 🚀 Features

- 🎙️ **Voice-Driven Interaction** – Clients can talk naturally to schedule or check appointments.  
- 📅 **Google Calendar Integration** – Automatically checks and updates agent calendars.  
- 🤖 **Lead Qualification** – Identifies and routes potential leads before booking.  
- ⚡ **Real-Time Booking** – Confirms and responds instantly to clients.  
- 🧩 **Webhook & Routing Logic** – Smart routing based on client intent (`CheckAvailability`, `BookAppointment`, `QualifyLead`).

---

## 🗂️ Workflow Overview

```mermaid
graph TD;
    A[VAPI Tool Call Webhook] --> B[Variables];
    B --> C[Route by Tool Name];
    C -->|CheckAvailability| D[Calculate Potential Spots];
    D --> E[Get Google Calendar Events];
    E --> F[Filter for Available Slots];
    F --> G[Respond with Available Times];
    C -->|bookAppointment| H[Book Appointment in Google Calendar];
    H --> I[Respond with Booking Confirmation];
    C -->|qualifyLead| J[Respond with Qualification];

📁 Project Structure
📦 vapi-real-estate-voice-agent
 ┣ 📜 README.md
 ┣ 📜 vapi-real-estate-ai-agent.json

🧠 How It Works

Webhook Trigger: The voice agent receives client input through the VAPI Tool Call Webhook.

Routing Logic: The flow routes requests by intent (availability, booking, or qualification).

Integration: Uses Google Calendar API to read and create events dynamically.

Response: The agent replies instantly with available times, confirmation, or qualification info.

📘 Workflow JSON

Below is the workflow definition file:

File: vapi-real-estate-ai-agent.json

📁 Project Structure
📦 vapi-real-estate-voice-agent
 ┣ 📜 README.md
 ┣ 📜 vapi-real-estate-ai-agent.json

🧠 How It Works

Webhook Trigger: The voice agent receives client input through the VAPI Tool Call Webhook.

Routing Logic: The flow routes requests by intent (availability, booking, or qualification).

Integration: Uses Google Calendar API to read and create events dynamically.

Response: The agent replies instantly with available times, confirmation, or qualification info.

## 📘 Workflow JSON

You can view the full workflow configuration here:  
➡️ [vapi-real-estate-ai-agent.json](./vapi-real-estate-ai-agent.json)

