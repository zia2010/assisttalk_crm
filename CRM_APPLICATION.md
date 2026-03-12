# AssistTalk Labs — CRM Application Reference

> Last Updated: March 12, 2026
> This document is a quick reference for what the application does and how it's structured.

---

## What This App Does

An all-in-one system for real estate agents that:
- Answers their phone calls with AI
- Captures and organizes leads
- Sends instant alerts to the agent
- Emails property brochures to prospects automatically
- Reminds prospects about showings
- Sends bulk marketing emails
- Generates weekly performance reports

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Next.js | The app (website + dashboard + API) |
| Supabase | Database, login system, file storage |
| Vapi | AI voice assistant that answers calls |
| Twilio | Phone numbers + SMS messaging |
| Gmail API | Sending emails (notifications + brochures + campaigns) |
| Google Gemini | AI intelligence (call analysis, report writing) |
| Vercel | Hosts the app on the internet |
| Tailwind + shadcn/ui | Makes the UI look good |

---

## Users of the App

| User | What They See |
|---|---|
| **Agent (client)** | Their own leads, pipeline, properties, notifications |
| **Admin (you)** | Everything — all clients, costs, system health |

Agents are invited by admin. They cannot self-register.

---

## 10 Features Overview

### MVP Features (Build First — Day 1-15)

**1. AI Receptionist**
- Answers every call 24/7 with a custom greeting
- Qualifies the caller: budget, timeline, area, bedrooms, pre-approval
- Collects name, phone, email
- Detects spam/robocalls and hangs up
- Transfers existing clients directly to the agent
- Sends all call data to our app when the call ends

**2. CRM Dashboard**
- Pipeline board: New → Contacted → Showing → Offer → Closed/Lost
- Lead cards with name, phone, budget, area, property, date
- Full lead detail page with call transcript and notes
- Add, edit, delete, search, and filter leads
- Stats: total leads, new this week, showings booked, deals closed

**3. SMS + Email Notifications**
- Agent gets an SMS within 10 seconds of a new lead
- Agent gets a detailed email with call summary
- Notification preferences: SMS only, email only, or both
- Daily digest email: yesterday's summary

**4. Auto Brochure Sender**
- AI identifies which property the caller asked about
- System matches it to the brochure PDF
- Sends a branded email to the prospect with the brochure
- Agent gets a copy of what was sent
- Listing management page to add/edit properties and upload PDFs

**5. Auth System**
- Email + password login
- Two roles: Agent and Admin
- Password reset via email
- Admin invites new agents

**6. Multi-Tenant System**
- One app shared by all clients
- Each agent only sees their own data
- Each agent has their own AI assistant configuration
- Each agent has their own phone number
- Emails go out with the agent's branding, not ours

**7. Admin Dashboard**
- See all clients and their status
- Per-client: leads, calls, properties, notifications
- Cost tracking: Vapi minutes, Twilio SMS, estimated cost per client
- System health: errors, failed messages

---

### Post-MVP Features (Build After Client #1 Is Live — Day 16-45)

**8. Reminder System**
- Agent schedules a showing in the CRM
- 24 hours before: prospect gets an SMS reminder
- 2 hours before: prospect gets an automated call confirmation
- Agent also gets a reminder
- Prospect can reply CANCEL or RESCHEDULE

**9. Bulk Email Tool**
- Select leads by status, area, budget, date
- Pick from templates: Just Listed, Open House, Price Reduced, Market Update
- Or write a custom email
- Auto-inserts lead's name and property details
- Includes unsubscribe link
- Send history with dates and recipients

**10. Weekly Report**
- Auto-generates every Monday morning
- Includes: calls answered, leads captured, brochures sent, showings booked
- AI writes a natural language summary
- Compares to previous week (up/down trends)
- Emailed to the agent as a clean formatted email
- All past reports viewable in the dashboard

---

## The Main Flow


Here's the content for CRM_APPLICATION.md:

Buyer calls agent's number
→ Twilio routes call to Vapi
→ AI answers, qualifies, collects info
→ Call ends
→ Vapi sends data to our app
→ App saves lead in database
→ App sends SMS to agent ("New lead: John, $400K, Downtown")
→ App sends email to agent (detailed summary)
→ App sends brochure email to prospect
→ Agent opens dashboard → sees new lead → calls back


Here's the content for CRM_APPLICATION.md:

Buyer calls agent's number
→ Twilio routes call to Vapi
→ AI answers, qualifies, collects info
→ Call ends
→ Vapi sends data to our app
→ App saves lead in database
→ App sends SMS to agent ("New lead: John, $400K, Downtown")
→ App sends email to agent (detailed summary)
→ App sends brochure email to prospect
→ Agent opens dashboard → sees new lead → calls back