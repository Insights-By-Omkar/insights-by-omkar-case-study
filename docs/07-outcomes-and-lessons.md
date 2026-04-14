# 07 · Outcomes & Lessons

## What I shipped

In **~6 weeks, solo**, I delivered:

- A **live, production-grade AI SaaS** at [insightsbyomkar.com](https://www.insightsbyomkar.com)
- **12+ product modules** spanning structured AI outputs, each with its own schema + cost model
- **Dual payment rails** (Stripe + PayPal) with webhook reconciliation and chargeback-case modeling
- **Multi-tier AI support system** (6 rotating Tier-1 + Anthropic-powered Tier-2 escalation)
- **30+ DB migrations** with Row-Level Security on every user-scoped table
- **5 scheduled cron jobs** for content, intelligence, reports, re-engagement
- **8 branded email templates** with evidence-stamping for chargeback defense
- **20+ admin panels** for ops, content intelligence, support, observability
- A full **pre-launch checklist** (13 sections) and **versioned CHANGELOG** discipline

## What this evidences

I don't just manage shipping — I do the shipping when needed. I can:

- **Strategize like a PM** — segment users, price the product, decide what to cut
- **Execute like a TPM** — sequence releases, track dependencies, gate launches
- **Build like an engineer** — ship production-ready code across the stack
- **Think like legal/finance** — chargeback defense, unit economics, compliance posture

That combination is what makes this case study worth reading: most senior PM/TPM candidates can do one or two of these. I did all four, concurrently, on a commercial deadline.

---

## What worked

### 1. Ruthless scoping

I wrote a "not doing at launch" list on day one and held to it:
- No mobile app
- No social features
- No custom ML models
- No more than 5 modules at v1.0

Every "no" freed up the "yes" list to actually ship. The 12-module product today exists only because the v1.0 product was 5 modules.

### 2. Compliance as a product decision, not a legal one

Chargeback defense, consent logging, RLS, refund policy enforcement — I treated these as **product requirements**, designed into the data model and UX, not bolted on after legal review. Result: the product is audit-ready on day 1 without blocking velocity.

### 3. Versioned releases, always

Every change got a version. Every version got a changelog entry. 6 weeks in, I can still answer "when did we ship X?" in 10 seconds. That's operational leverage.

### 4. AI-native operating model

I used AI coding tools aggressively — not as a shortcut, but as an amplifier. The `update-ai-context.sh` + `repomix-output.xml` pattern kept the full codebase compressible and queryable. A solo dev with AI can legitimately outpace a 5-person team *if* they keep the context tight.

---

## What I'd do differently

### 1. Define payment-provider abstraction at v1.0

I added Stripe at v1.2 and PayPal at v2.0, which meant retrofitting rail-aware logic into a bunch of handlers. Cleaner would've been a `PaymentProvider` interface from day one — even if PayPal didn't exist yet, Stripe-only code would've been provider-agnostic.

### 2. Add a staging smoke-test suite earlier

The support-agent escalation bug (v2.0.7) would've been caught by a 2-message staging test. I was doing manual smoke tests against production — works at this scale, doesn't scale to a team. Building the test harness at v1.4 (pre-launch) rather than post-incident would've been better practice.

### 3. Instrument the dispute dashboard on day 1

I have `chargeback_cases` modeled, but no live dashboard showing dispute rate, refund rate, per-product trendlines, or threshold alerts. The data's there — the surfacing isn't. That's the first thing I'd build in week 7.

### 4. Pre-dispute "save" flow

The amber "Questions about this charge?" callout in receipts currently links to email support. Better: route it into an in-product support conversation with full purchase context preloaded, so the user hits a warm resolution path *before* calling their bank. Industry data suggests this converts 30%+ of would-be chargebacks.

---

## What this project unlocks next

This repo is a capability proof. The applications from here:

- **Founding PM / Founding TPM at an AI startup** — I've shown I can own a product end-to-end at startup speed
- **Senior TPM at a consumer AI org** — scale the same discipline across multiple teams
- **Senior PM for AI monetization / payments / compliance surfaces** — the law + accounting + engineering combo is rare and valuable in regulated consumer AI

I'm not looking for "a PM role." I'm looking for a role where the combination of operator, builder, and governance-thinker all get used. If that sounds like your org, **[let's talk](mailto:Jaliparthiomkar03@gmail.com)**.

---

<p align="center"><i>End of case study.</i></p>

<p align="center">
  ← <a href="./06-operating-rhythm.md">Operating Rhythm</a> · <a href="../README.md">Back to overview</a>
</p>
