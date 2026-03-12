# AssistTalk Labs — Business TODO List

> Last Updated: March 12, 2026
> Status: Pre-Launch

---

## Legend

- [ ] Not started
- [~] In progress
- [x] Completed

---

## Phase 0: Business Setup

- [ ] **1. Redesign Website**
  - [ ] Design landing page for AssistTalk Labs
  - [ ] Hero section with clear value proposition (AI receptionist for real estate agents)
  - [ ] Features section (7 features with icons/visuals)
  - [ ] Pricing section ($500/mo + free trial CTA)
  - [ ] Testimonials section (placeholder until real ones come in)
  - [ ] "Book a Demo" CTA button
  - [ ] Mobile responsive
  - [ ] Deploy to custom domain

- [ ] **2. Google Workspace Setup**
  - [ ] Register domain (assisttalklabs.com or similar)
  - [ ] Set up Google Workspace ($7/mo)
  - [ ] Create professional email (hello@assisttalklabs.com, support@, etc.)
  - [ ] Set up Google Calendar for demo scheduling
  - [ ] Set up Google Drive for client documents/brochures
  - [ ] Configure email signatures with branding

- [ ] **3. Social Media Setup**
  - [ ] Create LinkedIn company page
  - [ ] Create Instagram business account
  - [ ] Create Twitter/X account
  - [ ] Create Facebook business page (optional — for credibility)
  - [ ] Design profile picture + banner (consistent branding)
  - [ ] Write bio/description (same across all platforms)
  - [ ] Post 3-5 initial content pieces (before outreach begins)
  - [ ] Content ideas: "Why agents miss 40% of leads", "AI vs human receptionist", demo clips

- [ ] **4. Onboarding System**
  - [ ] Create client intake form (Typeform/Google Form)
    - Business name, phone, email, branding, active listings
  - [ ] Create onboarding checklist (internal — per client)
  - [ ] Create welcome email template
  - [ ] Create "how it works" guide for clients (1-pager)
  - [ ] Create Vapi configuration template (clone per client)
  - [ ] Create CRM setup playbook (step-by-step for each new client)
  - [ ] Estimated onboarding time target: <8 hours per client

- [ ] **5. Payment System**
  - [ ] Set up Stripe account
  - [ ] Create $500/mo subscription product in Stripe
  - [ ] Set up payment links (for sending to clients after trial)
  - [ ] Configure auto-invoicing (monthly)
  - [ ] Set up Stripe webhook → Supabase (track payment status)
  - [ ] Create cancellation flow (self-serve or manual)
  - [ ] Handle refund process (30-day money-back on first paid month)

- [ ] **6. Automated Workflow Systems**
  - [ ] Call received → Lead created in CRM (Vapi → Supabase)
  - [ ] Lead created → SMS + Email to agent (Twilio + Gmail)
  - [ ] Lead created → Auto brochure sent to prospect (Gmail)
  - [ ] Showing scheduled → 24hr SMS reminder to prospect (Twilio cron)
  - [ ] Showing scheduled → 2hr call confirmation to prospect (Twilio voice)
  - [ ] Weekly → Auto-generate performance report (Gemini + Supabase)
  - [ ] Weekly → Email report to agent (Gmail)
  - [ ] Referral link clicked → Track + create referral record
  - [ ] Referral converts → Apply discount to referrer's invoice

- [ ] **7. Monitoring System**
  - [ ] Set up uptime monitoring (UptimeRobot / BetterStack — free tier)
  - [ ] Monitor: Website, API endpoints, Vapi webhook, Supabase
  - [ ] Set up error tracking (Sentry — free tier)
  - [ ] Set up Supabase database alerts (storage, connections)
  - [ ] Monitor Twilio balance + usage per client
  - [ ] Monitor Vapi usage per client (minutes, costs)
  - [ ] Create simple internal dashboard: costs per client vs revenue
  - [ ] Set up daily health check (automated ping test)
  - [ ] Alert channel: SMS or email when something breaks

---

## Phase 1: BUILD MVP (Day 1-15)

- [ ] Project scaffolding (Next.js + Supabase + Tailwind + shadcn/ui)
- [ ] Database schema design + migration
- [ ] Authentication (Supabase Auth)
- [ ] Lead management (CRUD)
- [ ] Dashboard UI (pipeline view + stats)
- [ ] Vapi AI receptionist integration
- [ ] Twilio SMS notifications
- [ ] Auto brochure sender (Gmail API)
- [ ] Referral tracking system
- [ ] Reminder system (SMS + outbound call)
- [ ] Bulk email tool
- [ ] Weekly report generator
- [ ] UI polish + responsive design
- [ ] End-to-end testing
- [ ] Deploy to Vercel
- [ ] Record demo video

---

## Phase 2: GET FIRST 2 CLIENTS (Day 16-65)

- [ ] Research 30 real estate agents (Friday session #1)
- [ ] Send first batch of cold emails (30 agents)
- [ ] Book + run demo calls
- [ ] Sign Client #1 (free pilot)
- [ ] Onboard Client #1 (customize system)
- [ ] Go live with Client #1
- [ ] Research 30 more agents (Friday session #2)
- [ ] Send second batch of cold emails
- [ ] Sign Client #2 (free pilot)
- [ ] Onboard Client #2
- [ ] Go live with Client #2
- [ ] Client #1 trial ends → Convert to paid ($500/mo)
- [ ] Client #2 trial ends → Convert to paid ($500/mo)

---

## Phase 3: GET NEXT 2 CLIENTS (Day 55-85)

- [ ] Research 30-40 agents (Friday session)
- [ ] Send outreach emails
- [ ] Book + run demo calls
- [ ] Sign Client #3 + Client #4 together (free pilot)
- [ ] Onboard both clients
- [ ] Go live with both
- [ ] Client #3 trial ends → Convert to paid ($500/mo)
- [ ] Client #4 trial ends → Convert to paid ($500/mo)
- [ ] **STOP ALL OUTREACH** — 4 clients locked in

---

## Phase 4: MAINTAIN (Day 86+)

- [ ] Weekly: Review all 4 client dashboards
- [ ] Weekly: Send/review automated reports
- [ ] Weekly: Check costs vs revenue
- [ ] Monthly: Review client satisfaction (quick check-in call)
- [ ] Monthly: Review and optimize AI receptionist prompts
- [ ] Monthly: System updates + security patches
- [ ] As needed: Bug fixes, minor feature requests

---

## Notes

- Sunday = OFF. Always.
- Max 4 clients. No exceptions until all 4 are stable for 3+ months.
- No outreach after 4 clients are paying.
- If a client churns, replace with 1 new client only.
- Every feature built must answer: "Does this get or keep a client?"

---

*Check off items as you complete them. This is your single tracking document.*
