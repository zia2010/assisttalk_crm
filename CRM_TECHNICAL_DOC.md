src/
│
│   Think of it like a building:
│
│   FLOOR 5 — PAGES           (what the user sees — full screens)
│   FLOOR 4 — UI COMPONENTS   (reusable visual pieces)
│   FLOOR 3 — COMMON          (shared components used everywhere)
│   FLOOR 2 — HOOKS/QUERIES   (data fetching + state logic)
│   FLOOR 1 — API LAYER       (talks to backend)
│   BASEMENT — UTILS           (helper functions)
│
│   Each floor ONLY talks to the floor below it. Never skips floors.
│
│   Pages → use UI Components → use Common Components
│   Pages → use Hooks → use API Layer → use Utils

assisttalk-crm/
│
├── app/                              ← PAGES (Floor 5)
│   ├── layout.tsx
│   ├── page.tsx
│   │
│   ├── (auth)/                       ← Auth pages (public — no login needed)
│   │   ├── login/
│   │   │   └── page.tsx
│   │   ├── reset-password/
│   │   │   └── page.tsx
│   │   └── callback/
│   │       └── route.ts
│   │
│   ├── (dashboard)/                  ← Agent pages (protected — login required)
│   │   ├── layout.tsx                ← Dashboard layout with sidebar
│   │   ├── page.tsx                  ← Dashboard home
│   │   ├── leads/
│   │   │   ├── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   ├── properties/
│   │   │   ├── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   ├── notifications/
│   │   │   └── page.tsx
│   │   └── settings/
│   │       └── page.tsx
│   │
│   ├── (admin)/                      ← Admin pages (protected — admin role only)
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── clients/
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   └── system/
│   │       └── page.tsx
│   │
│   └── api/                          ← API Routes (backend)
│       ├── vapi/
│       │   └── webhook/
│       │       └── route.ts
│       ├── leads/
│       │   ├── route.ts
│       │   └── [id]/
│       │       └── route.ts
│       ├── properties/
│       │   ├── route.ts
│       │   └── [id]/
│       │       └── route.ts
│       ├── notifications/
│       │   ├── sms/
│       │   │   └── route.ts
│       │   └── email/
│       │       └── route.ts
│       ├── brochure/
│       │   └── send/
│       │       └── route.ts
│       └── admin/
│           ├── clients/
│           │   └── route.ts
│           └── system/
│               └── route.ts
│
├── api/                              ← API LAYER (Floor 1)
│   ├── endpoints.ts                  ← All API URLs in one place
│   ├── client.ts                     ← Base fetch wrapper with auth headers
│   ├── leads.api.ts                  ← Lead-related API calls
│   ├── properties.api.ts             ← Property-related API calls
│   ├── notifications.api.ts          ← Notification API calls
│   ├── brochure.api.ts               ← Brochure API calls
│   └── admin.api.ts                  ← Admin API calls
│
├── hooks/                            ← REACT QUERY HOOKS (Floor 2)
│   ├── queries/
│   │   ├── useLeads.ts               ← Fetch leads, single lead
│   │   ├── useProperties.ts          ← Fetch properties
│   │   ├── useNotifications.ts       ← Fetch notification history
│   │   ├── useDashboardStats.ts      ← Fetch dashboard numbers
│   │   └── useAdminData.ts           ← Fetch admin panel data
│   ├── mutations/
│   │   ├── useCreateLead.ts          ← Create new lead
│   │   ├── useUpdateLead.ts          ← Update lead status/info
│   │   ├── useDeleteLead.ts          ← Delete lead
│   │   ├── useCreateProperty.ts
│   │   ├── useUpdateProperty.ts
│   │   └── useSendBrochure.ts
│   └── useAuth.ts                    ← Login, logout, current user
│
├── components/                       ← UI COMPONENTS (Floor 4)
│   ├── leads/
│   │   ├── LeadCard.tsx
│   │   ├── LeadCard.test.tsx
│   │   ├── LeadPipeline.tsx
│   │   ├── LeadPipeline.test.tsx
│   │   ├── LeadForm.tsx
│   │   ├── LeadForm.test.tsx
│   │   ├── LeadDetail.tsx
│   │   └── LeadFilters.tsx
│   ├── properties/
│   │   ├── PropertyCard.tsx
│   │   ├── PropertyForm.tsx
│   │   └── PropertyList.tsx
│   ├── dashboard/
│   │   ├── StatsCards.tsx
│   │   ├── RecentActivity.tsx
│   │   └── QuickActions.tsx
│   ├── admin/
│   │   ├── ClientList.tsx
│   │   ├── CostTracker.tsx
│   │   └── SystemHealth.tsx
│   └── layout/
│       ├── Sidebar.tsx
│       ├── Header.tsx
│       └── MobileNav.tsx
│
├── common/                           ← COMMON COMPONENTS (Floor 3)
│   ├── Button.tsx
│   ├── Input.tsx
│   ├── Modal.tsx
│   ├── Table.tsx
│   ├── Badge.tsx
│   ├── Card.tsx
│   ├── Loading.tsx
│   ├── ErrorBoundary.tsx
│   ├── EmptyState.tsx
│   ├── Pagination.tsx
│   ├── SearchBar.tsx
│   ├── Toast.tsx
│   └── ConfirmDialog.tsx
│
├── lib/                              ← SERVICE CONNECTIONS
│   ├── supabase/
│   │   ├── client.ts                 ← Browser-side (uses anon key — safe)
│   │   ├── server.ts                 ← Server-side (uses anon key + cookies)
│   │   └── admin.ts                  ← Admin operations (uses service role key — NEVER on client)
│   ├── twilio/
│   │   └── client.ts                 ← Server-only — Twilio SDK
│   ├── resend/
│   │   └── client.ts                 ← Server-only — Resend SDK
│   ├── vapi/
│   │   └── client.ts                 ← Server-only — Vapi API
│   └── providers/
│       ├── QueryProvider.tsx          ← React Query provider
│       ├── AuthProvider.tsx           ← Auth context provider
│       └── ToastProvider.tsx          ← Toast notification provider
│
├── utils/                            ← UTILITY FUNCTIONS (Basement)
│   ├── format.ts                     ← formatPhone(), formatCurrency(), formatDate()
│   ├── format.test.ts
│   ├── validate.ts                   ← validateEmail(), validatePhone(), sanitizeInput()
│   ├── validate.test.ts
│   ├── constants.ts                  ← Pipeline stages, status options, etc.
│   └── helpers.ts                    ← Generic helpers
│
├── types/                            ← TYPE DEFINITIONS
│   ├── lead.ts
│   ├── property.ts
│   ├── call.ts
│   ├── notification.ts
│   ├── agent.ts
│   └── api.ts                        ← API response/request types
│
├── middleware.ts                      ← Auth + role protection
│
├── .env.local                        ← Secrets (NEVER committed)
├── .env.example                      ← Template (committed — no real values)
├── jest.config.ts
├── jest.setup.ts
├── package.json
├── tailwind.config.ts
├── tsconfig.json
└── next.config.ts

THREE SUPABASE CLIENTS — EACH FOR A DIFFERENT PURPOSE

1. BROWSER CLIENT (lib/supabase/client.ts)
   ├── Uses: NEXT_PUBLIC_SUPABASE_URL + NEXT_PUBLIC_SUPABASE_ANON_KEY
   ├── Where: Runs in the user's browser
   ├── Can do: Read/write data filtered by RLS (agent sees own data only)
   ├── Cannot do: Bypass RLS, access other agents' data, admin operations
   └── Safe to expose: YES — anon key + RLS = restricted access

2. SERVER CLIENT (lib/supabase/server.ts)
   ├── Uses: NEXT_PUBLIC_SUPABASE_URL + NEXT_PUBLIC_SUPABASE_ANON_KEY + cookies
   ├── Where: Runs on your server (API routes, server components)
   ├── Can do: Same as browser but with server-side cookie access
   ├── Cannot do: Bypass RLS
   └── Used for: API routes, server-side rendering

3. ADMIN CLIENT (lib/supabase/admin.ts)
   ├── Uses: NEXT_PUBLIC_SUPABASE_URL + SUPABASE_SERVICE_ROLE_KEY
   ├── Where: ONLY on your server (NEVER in browser)
   ├── Can do: EVERYTHING — bypass RLS, access all data, create users
   ├── Cannot do: Nothing — it has god-mode access
   └── Used for: Webhook processing, admin operations, user creation

                             BROWSER          SERVER
                        (user sees)     (your code only)
                        ───────────     ────────────────
NEXT_PUBLIC_SUPABASE_URL     ✅              ✅
NEXT_PUBLIC_SUPABASE_ANON_KEY ✅             ✅
SUPABASE_SERVICE_ROLE_KEY    ❌ NEVER        ✅
TWILIO_ACCOUNT_SID           ❌ NEVER        ✅
TWILIO_AUTH_TOKEN            ❌ NEVER        ✅
RESEND_API_KEY               ❌ NEVER        ✅
VAPI_API_KEY                 ❌ NEVER        ✅
VAPI_WEBHOOK_SECRET          ❌ NEVER        ✅
GEMINI_API_KEY               ❌ NEVER        ✅


Summary
Layer	Purpose	Knows About Secrets?
Utils	Formatting, validation, helpers	No
API Layer	Fetch wrapper + endpoint URLs	No — only calls your own API
Hooks	React Query — caching + state	No
Common	Generic UI components	No
Components	Business UI (leads, properties)	No
Pages	Compose hooks + components	No
API Routes	Backend logic — auth, database, notifications	YES — server-only
Lib	Service clients (Supabase, Twilio, Resend)	YES — server-only
Middleware	Auth + role checking	Minimal — only Supabase anon key
The browser NEVER touches Twilio, Resend, Vapi keys, or the service role key. Everything sensitive runs on the server through API routes.