# AssistTalk Labs — Complete Business Plan

> Last Updated: March 12, 2026
> Founder: Solo (Full-time employed, building on the side)
> Launch Date: March 12, 2026
> Target MRR: $2,000 by June 5, 2026

---

## Table of Contents

1. [Business Overview](#1-business-overview)
2. [Target Market](#2-target-market)
3. [Product — 7 Features](#3-product--7-features)
4. [Tech Stack](#4-tech-stack)
5. [Pricing Strategy](#5-pricing-strategy)
6. [Revenue Model](#6-revenue-model)
7. [Cost Structure](#7-cost-structure)
8. [Client Acquisition Strategy](#8-client-acquisition-strategy)
9. [Onboarding Process](#9-onboarding-process)
10. [Timeline & Milestones](#10-timeline--milestones)
11. [Weekly Schedule](#11-weekly-schedule)
12. [Financial Projections](#12-financial-projections)
13. [Risk Assessment](#13-risk-assessment)
14. [Competitive Advantage](#14-competitive-advantage)
15. [Scaling Plan (Future)](#15-scaling-plan-future)

---

## 1. Business Overview

| Field | Detail |
|---|---|
| **Business Name** | AssistTalk Labs |
| **Type** | AI Specialist Agency / Vertical SaaS |
| **What We Do** | AI-powered lead capture, CRM, and automation for real estate agents |
| **How We Make Money** | Monthly subscription — $500/client/month |
| **Target Clients** | 4 (capped intentionally) |
| **Target MRR** | $2,000/month |
| **Target Net Profit** | $1,750/month |
| **Founder Commitment** | Part-time (4 hrs/weeknight + weekends) alongside full-time job |

---

## 2. Target Market

### Industry: Real Estate (Phase 1 — sole focus)

| Attribute | Detail |
|---|---|
| **Who** | Independent real estate agents or small teams (2-5 people) |
| **Where** | Any English-speaking market (start local) |
| **Revenue** | Agents doing $3M+/year in transactions |
| **Current spending** | $500-2,000/mo on marketing (Zillow, Facebook ads, etc.) |
| **Key pain points** | Missing calls during showings, slow lead follow-up, no organized system |
| **Decision maker** | The agent themselves (no committees, fast decisions) |

### Why Real Estate First

- **Speed-to-lead is proven** — responding in <5 min = 8x more conversions
- **High commission per deal** — avg $8,000-15,000 per sale
- **Solo operators** — they can't be on the phone 24/7
- **Clear ROI story** — 1 saved deal/month > 10x the subscription cost
- **Budget exists** — they already pay for lead gen tools
- **Low tech expectations** — they want "it just works", not a complex platform

### Future Verticals (NOT now — only after Phase 1 success)

- Wedding Planners
- Interior Designers
- Second-hand Car Dealers

---

## 3. Product — 7 Features

### Feature 1: AI Receptionist (Vapi)
| Aspect | Detail |
|---|---|
| **What** | AI voice assistant that answers calls 24/7 |
| **How it works** | Prospect calls → AI answers → qualifies (budget, timeline, area, property type) → logs lead → sends brochure → notifies agent |
| **Tech** | Vapi (voice AI platform) + Gemini (intelligence) |
| **Value** | Never miss a lead. Instant response. Professional first impression |
| **Real estate specifics** | Asks about budget range, preferred neighborhoods, bedrooms, timeline to buy/sell |

### Feature 2: CRM Dashboard (Next.js + Supabase)
| Aspect | Detail |
|---|---|
| **What** | Central dashboard to view and manage all leads |
| **How it works** | All leads auto-populated from calls/emails/SMS → pipeline view (New → Contacted → Showing → Offer → Closed) |
| **Tech** | Next.js (frontend) + Supabase (database + auth) |
| **Value** | One place to see everything. No spreadsheets. No sticky notes |
| **Real estate specifics** | Property interest tracking, showing scheduler, commission calculator |

### Feature 3: Auto Brochure Sender + Referral Bonus
| Aspect | Detail |
|---|---|
| **What** | Automatically emails property brochure/listing PDF after AI call |
| **How it works** | AI identifies property of interest → system matches to listing → sends branded email with PDF + agent contact |
| **Tech** | Gmail API + Supabase (listing storage) |
| **Value** | Instant follow-up while competitor agents are still checking voicemail |
| **Referral system** | Each client gets a referral link. Referred agent signs up → referrer gets $50/mo discount. Tracked automatically |

### Feature 4: SMS + Email Notifications
| Aspect | Detail |
|---|---|
| **What** | Instant alerts to agent when something happens |
| **How it works** | New lead → SMS + email to agent within 10 seconds |
| **Tech** | Twilio (SMS) + Gmail API (email) |
| **Value** | Agent knows about every lead in real-time, even during a showing |
| **Notification types** | New lead, lead status change, showing reminder, missed follow-up alert |

### Feature 5: Reminder System (SMS + Outbound Call)
| Aspect | Detail |
|---|---|
| **What** | Automated reminders to prospects before showings/appointments |
| **How it works** | Showing scheduled → 24hr before: SMS reminder → 2hr before: automated call confirmation |
| **Tech** | Twilio (SMS + voice) + Supabase (scheduler) + cron jobs |
| **Value** | Reduces no-shows by 60-80%. Agent doesn't waste time on empty showings |

### Feature 6: Bulk Email Tool
| Aspect | Detail |
|---|---|
| **What** | Send marketing emails to lead database |
| **How it works** | Agent selects segment (e.g., "all buyers interested in downtown") → writes or picks template → sends |
| **Tech** | Gmail API / SendGrid (for scale) + Supabase |
| **Value** | "Just Listed", "Open House", "Price Reduced" campaigns in 2 clicks |
| **Templates** | Pre-built for: New listing, Open house invite, Market update, Holiday greeting |

### Feature 7: Weekly Report
| Aspect | Detail |
|---|---|
| **What** | Auto-generated weekly performance summary |
| **How it works** | Every Monday → system analyzes past 7 days → generates report → emails to agent |
| **Tech** | Gemini (AI summary) + Supabase (data) + Gmail (delivery) |
| **Value** | Agent sees ROI clearly: "12 leads captured, 8 brochures sent, 3 showings booked this week" |
| **Includes** | Lead count, response times, conversion rates, top lead sources, upcoming showings |

---

## 4. Tech Stack

| Layer | Technology | Purpose | Cost |
|---|---|---|---|
| **Frontend** | Next.js 14+ (App Router) | CRM dashboard, admin panel | Free |
| **Database** | Supabase (PostgreSQL) | Data storage, auth, real-time | $25/mo (Pro) |
| **Voice AI** | Vapi | AI receptionist, outbound calls | ~$20-40/client/mo |
| **SMS** | Twilio | SMS notifications, reminders | ~$10-20/client/mo |
| **Email** | Gmail API | Brochure sending, notifications, bulk email | Free (within limits) |
| **AI/LLM** | Google Gemini | Call intelligence, report generation, email drafting | ~$5-10/client/mo |
| **Hosting** | Vercel | Frontend deployment | Free tier |
| **Styling** | Tailwind CSS + shadcn/ui | UI components | Free |
| **Cron/Jobs** | Vercel Cron / Supabase Edge Functions | Scheduled tasks (reminders, reports) | Free tier |

---

## 5. Pricing Strategy

### Pricing

| | Detail |
|---|---|
| **Monthly price** | $500/client/month |
| **Trial** | 30 days FREE (no credit card required) |
| **First paid month** | 30-day money-back guarantee |
| **After that** | Standard monthly, cancel anytime |
| **Contracts** | None — month-to-month |

### Why $500/month

- Agent spends $500-2K/mo on marketing already — this is within budget
- 1 saved deal/month = $10,000 commission = **20x ROI** on our fee
- Cheaper than hiring a part-time receptionist ($1,500-2,500/mo)
- Cheaper than competing tools combined (CRM $100 + answering service $200 + SMS tool $50 + email tool $50 = $400 without AI)

### Trial Strategy

```
Days 1-30:    FREE pilot (full access, full setup, full support)
              → Purpose: Prove value with real leads
              
Day 31:       First payment — $500
              → 30-day money-back guarantee still applies
              
Day 61+:      Standard recurring — $500/mo
              → Cancel anytime, no questions asked
```

**Why free trial, not discounted:**
- "$100/month" sounds cheap → positions us as a tool
- "Free pilot program" sounds exclusive → positions us as a partner
- Zero friction to start
- We look confident, not desperate

### Referral Program

| Mechanic | Detail |
|---|---|
| How it works | Client refers another agent → referred agent signs up |
| Reward | Referrer gets $50/mo discount (ongoing while referral stays) |
| Max discount | $200/mo (4 referrals) — agent pays minimum $300/mo |
| Tracking | Automated via referral links in the CRM |

---

## 6. Revenue Model

### Revenue Streams

| Stream | Amount | Notes |
|---|---|---|
| Monthly subscription | $500/client/mo | Primary revenue |
| Setup fee | $0 | Free — remove friction |
| Overage charges | $0 | All-inclusive — keep it simple |

### Revenue Math

| Clients | Gross MRR | Monthly Costs | Net Monthly Profit | Annual Net |
|---|---|---|---|---|
| 1 | $500 | ~$100 | $400 | $4,800 |
| 2 | $1,000 | ~$175 | $825 | $9,900 |
| 3 | $1,500 | ~$250 | $1,250 | $15,000 |
| **4** | **$2,000** | **~$300** | **$1,700** | **$20,400** |

### Effective Hourly Rate (Steady State — 4 Clients)

| Metric | Value |
|---|---|
| Monthly profit | $1,700 |
| Weekly hours | 6-7 hrs |
| Monthly hours | ~28 hrs |
| **Effective hourly rate** | **~$60/hr** |

---

## 7. Cost Structure

### Fixed Costs (Monthly)

| Item | Cost | Notes |
|---|---|---|
| Supabase Pro | $25 | Shared across all clients |
| Vercel hosting | $0 | Free tier sufficient for 4 clients |
| Domain + DNS | ~$1 | Annual domain / 12 |
| **Total fixed** | **~$26/mo** | |

### Variable Costs (Per Client/Month)

| Item | Cost | Notes |
|---|---|---|
| Vapi (voice minutes) | $20-40 | ~100-200 min/month/client |
| Twilio (SMS + calls) | $10-20 | ~100-200 SMS + 10-20 calls |
| Gemini API | $5-10 | Report generation, call analysis |
| Gmail API | $0 | Free within limits |
| **Total per client** | **~$40-70** | |

### Total Monthly Costs by Client Count

| Clients | Fixed | Variable | Total | Gross Margin |
|---|---|---|---|---|
| 1 | $26 | $55 | $81 | 84% |
| 2 | $26 | $110 | $136 | 86% |
| 3 | $26 | $165 | $191 | 87% |
| 4 | $26 | $220 | $246 | 88% |

### Upfront Investment (One-time)

| Item | Cost | Notes |
|---|---|---|
| Domain registration | ~$12/yr | .com or .io |
| Twilio phone number | $1/mo | Per client number |
| Vapi account setup | $0 | Pay-as-you-go |
| Development time | $0 (sweat equity) | 90 hours over 15 days |
| **Total upfront cash** | **~$15** | |

---

## 8. Client Acquisition Strategy

### Method: Targeted Cold Outreach (Warm-ish)

**Step 1: Find prospects (every Friday, until 4 clients locked)**

| Source | How |
|---|---|
| Zillow | Search agents in target area, note phone + email |
| Realtor.com | Same — agent profiles have contact info |
| Google | "Real estate agent [city]" — check their websites |
| LinkedIn | Search "real estate agent" + city, connect + DM |
| Instagram | Many agents post listings — DM them |

**Step 2: Qualify prospects**

Call their listed phone number:
- Goes to voicemail? → **Perfect prospect** (they miss calls)
- Answers quickly? → Still a prospect, but lower urgency

**Step 3: Outreach email**

> **Subject:** I called you today — it went to voicemail
>
> Hi [Name],
>
> I called your number listed on Zillow today at 2pm. Got your voicemail.
>
> I'm not a lead — but your next buyer might be. And they'll call the next agent instead.
>
> I built an AI system that answers your phone 24/7, qualifies leads instantly (budget, timeline, area), and texts you a summary in real-time. It even sends property brochures automatically.
>
> I'm offering 3 agents in [city] a free 30-day pilot. No cost, no commitment.
>
> Want to see a 2-minute demo?
>
> — [Your name], AssistTalk Labs

**Step 4: Demo call (Saturday, 15-20 min)**

| Minute | Do |
|---|---|
| 0-3 | Ask about their current lead flow, pain points |
| 3-8 | Show the CRM dashboard (screen share) |
| 8-12 | Play a sample AI receptionist call |
| 12-15 | Explain the free pilot — "I set it up, you test it, zero risk" |
| 15-18 | Answer questions, handle objections |
| 18-20 | "Can I set this up for you this week?" |

**Step 5: Close**

Get from them:
- Business phone number (to forward or set up secondary)
- 3-5 active listings (for brochure system)
- Logo + branding colors (for emails)
- Preferred notification method (SMS/email/both)

### Outreach Volume Plan

| Milestone | Prospects to Contact | Expected Pilots | Expected Conversions |
|---|---|---|---|
| Client #1 | 30-50 | 2-3 | 1 |
| Client #2 | 30-50 | 2-3 | 1 |
| Clients #3+#4 | 40-60 | 3-4 | 2 |
| **Total** | **~100-150** | **8-10** | **4-5** |

### After 4 Clients: STOP ALL OUTREACH

- No more cold emails
- No more Friday prospecting
- Focus 100% on serving existing 4 clients
- Only add new clients if one churns (replacement only)

---

## 9. Onboarding Process

### Per-Client Onboarding Checklist (5-8 hours total)

| Step | Time | Task |
|---|---|---|
| 1 | 30 min | Collect business info (name, phone, email, branding, listings) |
| 2 | 2 hrs | Configure Vapi assistant with their business script |
| 3 | 1 hr | Add listings to brochure system |
| 4 | 1 hr | Set up CRM dashboard (pipeline stages, custom fields) |
| 5 | 30 min | Configure Twilio number + call forwarding |
| 6 | 30 min | Set up email notifications + templates |
| 7 | 1 hr | End-to-end testing (make test calls, verify everything works) |
| 8 | 1 hr | Walkthrough call with client (show them the dashboard, explain alerts) |
| **Total** | **~8 hrs** | |

---

## 10. Timeline & Milestones

### Master Timeline

| Phase | Days | Dates | Goal |
|---|---|---|---|
| **BUILD** | Day 1-15 | Mar 12 - Mar 27 | MVP complete and deployed |
| **CLIENT #1** | Day 16-50 | Mar 28 - May 1 | First trial → first payment |
| **CLIENT #2** | Day 31-65 | Apr 12 - May 16 | Second trial → second payment |
| **CLIENTS #3+#4** | Day 55-85 | May 6 - Jun 5 | Two trials → two payments |
| **STEADY STATE** | Day 86+ | Jun 6+ | 4 clients, maintenance mode |

### Build Phase Detail (Day 1-15)

| Day | Deliverable |
|---|---|
| 1 | Project setup, Supabase schema, auth |
| 2 | Lead management — CRUD operations |
| 3 | Dashboard UI — pipeline view, stats |
| 4 | Vapi setup — AI receptionist script |
| 5 | Vapi → Supabase — auto-log calls as leads |
| 6 | Twilio SMS — agent notifications |
| 7 | Gmail — auto brochure sender |
| 8 | Referral system — tracking + bonus |
| 9 | Reminder system — SMS + outbound call |
| 10 | Bulk email tool |
| 11 | Weekly report generator |
| 12 | UI polish + responsive design |
| 13 | Testing + bug fixes |
| 14 | Deploy to Vercel + domain setup |
| 15 | Demo video + pitch materials |

---

## 11. Weekly Schedule

### During Build Phase (Day 1-15)

| Day | Time | Hours | Activity |
|---|---|---|---|
| Mon-Thu | 8 PM - 2 AM | 6 hrs | Building the system |
| Fri | 8 PM - 2 AM | 6 hrs | Building the system |
| Sat | Flexible | 6-8 hrs | Building the system |
| Sun | OFF | 0 hrs | REST |
| **Total** | | **~38 hrs/week** | |

### During Sales Phase (Day 16-85)

| Day | Time | Hours | Activity |
|---|---|---|---|
| Mon-Thu | 8 PM - 12 AM | 4 hrs | Client support + outreach + improvements |
| Fri | 8 PM - 12 AM | 4 hrs | Prospect research (find 30 agents) |
| Sat | Flexible | 2-3 hrs | Demo calls |
| Sun | OFF | 0 hrs | REST |
| **Total** | | **~22-23 hrs/week** | |

### Steady State (Day 86+ — 4 clients, no outreach)

| Day | Time | Hours | Activity |
|---|---|---|---|
| Mon-Fri | 8 PM - 9 PM | 1 hr/night | Client support + monitoring |
| Sat | — | 1-2 hrs (if needed) | Improvements |
| Sun | OFF | 0 hrs | REST |
| **Total** | | **~6-7 hrs/week** | |

---

## 12. Financial Projections

### Month-by-Month (6-Month View)

| Month | Paying Clients | Trial Clients | MRR | Costs | Net Profit | Cumulative Profit |
|---|---|---|---|---|---|---|
| Mar 2026 | 0 | 0 | $0 | $50 | -$50 | -$50 |
| Apr 2026 | 0 | 1-2 | $0 | $100 | -$100 | -$150 |
| May 2026 | 1-2 | 1-2 | $500-1,000 | $175 | $325-825 | $175-675 |
| Jun 2026 | 3-4 | 0-1 | $1,500-2,000 | $250 | $1,250-1,750 | $1,425-2,425 |
| Jul 2026 | 4 | 0 | $2,000 | $275 | $1,725 | $3,150-4,150 |
| Aug 2026 | 4 | 0 | $2,000 | $275 | $1,725 | $4,875-5,875 |

### Annual Projection (Steady State)

| Metric | Value |
|---|---|
| Annual Revenue | $24,000 |
| Annual Costs | ~$3,300 |
| **Annual Net Profit** | **~$20,700** |
| Monthly Net Profit | ~$1,725 |
| Weekly Hours (steady state) | 6-7 hrs |
| Effective Hourly Rate | ~$60/hr |

### Break-Even Analysis

| Metric | Value |
|---|---|
| Upfront investment | ~$150 (first 2 months of infra costs during build + trial) |
| Break-even point | **Month 3** (first paying client covers all prior costs) |
| Time to recoup all costs | ~30 days after first payment |

---

## 13. Risk Assessment

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| **AI gives wrong property info** | Medium | High | Strict data validation, only use verified listing data, human fallback option |
| **Client churns after trial** | Medium | Medium | Deliver "wow moment" in week 1, ensure 5+ leads captured before trial ends |
| **Not enough prospects respond** | Medium | Medium | Iterate email copy, try multiple channels (email + LinkedIn + Instagram + cold call) |
| **Vapi/Twilio outage** | Low | High | Monitor uptime alerts, fallback: direct call forwarding to agent's cell |
| **Gmail sending limits hit** | Low | Medium | Use SendGrid/Resend for bulk email if needed ($0-20/mo) |
| **Agent says "I already have a CRM"** | High | Low | Position as ADD-ON (AI receptionist + automation layer), not CRM replacement |
| **Full-time job affected** | Low | Critical | Hard limit: 4 hrs/night weekdays, Sunday always OFF, cap at 4 clients |
| **Scope creep from clients** | Medium | Medium | Define clear feature list upfront, "that's on the roadmap" for extras |
| **Competitor enters market** | Low | Low | First-mover advantage, deep client relationship, switching cost (data in our system) |

---

## 14. Competitive Advantage

### Why Agents Would Choose Us Over Alternatives

| Alternative | Their Cost | Their Weakness | Our Edge |
|---|---|---|---|
| Ruby Receptionists (human) | $300-600/mo | Humans can't qualify leads with AI precision, limited hours | AI works 24/7, qualifies intelligently, costs same or less |
| kvCORE / Follow Up Boss (CRM) | $100-500/mo | No AI receptionist, no voice integration | All-in-one: AI phone + CRM + automation |
| Smith.ai (AI receptionist) | $200-600/mo | Generic, no CRM, no brochure sending | Built specifically for real estate, end-to-end workflow |
| Doing nothing | $0 | Missing 40% of leads | Clear ROI: 1 saved deal > 10x our annual cost |

### Our Moat (Why They Won't Leave)

1. **Data lock-in** — All their leads, history, and analytics live in our CRM
2. **Workflow integration** — AI is answering their phone; switching means downtime
3. **Relationship** — We're not a faceless SaaS; we're their "tech person"
4. **Results** — If they're closing more deals, why change?

---

## 15. Scaling Plan (Future)

> **NOT for now. Only after Phase 1 is stable (4 clients, 3+ months retained).**

### Option A: More Real Estate Clients
- Raise cap from 4 to 8-10 clients
- Hire a part-time VA for support ($500/mo)
- MRR: $4,000-5,000
- Requires: more automation, less manual onboarding

### Option B: New Verticals
- Wedding Planners — event-based lead capture + vendor coordination
- Interior Designers — project-based pipeline + mood board sharing
- Car Dealers — inventory integration + test drive booking
- Each vertical needs ~2 weeks of customization

### Option C: White-Label / Agency Model
- License the platform to other AI agencies
- They resell to their clients at their own price
- We charge $200/mo per sub-client
- Passive revenue, higher volume

### Option D: Quit Full-Time Job
- When MRR > full-time salary × 1.5 (safety buffer)
- If salary = $4,000/mo → quit when MRR hits $6,000 (12 clients)
- Estimated timeline: 12-18 months from launch

---

## Quick Reference Card

```
BUSINESS:        AssistTalk Labs
WHAT:            AI automation for real estate agents
PRICE:           $500/month
TARGET CLIENTS:  4 (capped)
TARGET MRR:      $2,000
NET PROFIT:      $1,750/month ($20,700/year)
GROSS MARGIN:    ~88%
TIME TO 4 CLIENTS: ~85 days
STEADY STATE EFFORT: 6-7 hours/week
TECH:            Next.js + Supabase + Vapi + Twilio + Gmail + Gemini
TRIAL:           30 days free → $500/mo with 30-day money-back
OUTREACH:        Stop after 4 clients
```

---

*This document is the single source of truth for AssistTalk Labs. Refer back to it whenever making decisions about features, pricing, clients, or priorities.*
