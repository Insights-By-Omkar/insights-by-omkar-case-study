# 01 · Problem & Users

## The problem I was solving

Consumer AI apps in the "spiritual guidance" category have two chronic issues:

1. **Wall-of-text outputs.** Most tarot/astrology AI apps paste a prompt into GPT and dump the raw response on the user. No structure, no progressive disclosure, no shareability, no memory.
2. **Trust leakage.** Payment flows feel sketchy, refund terms are hidden, and there's no human escalation path when AI gets it wrong. Users disengage fast — or worse, file chargebacks.

I wanted to build a platform where:
- Every AI output has a **structured shape** (summary → key themes → elements → guidance) users can skim, save, and share
- **Payment and support feel legitimate**, even when automated — because the business runs as a business, not a side project
- Users who come back find their **history preserved** across modules (tarot today, spell tomorrow, dream next week — one coherent thread)

---

## Users

Three primary segments, prioritized by willingness-to-pay × engagement frequency:

| Segment | Need | Monetization |
|---|---|---|
| **Daily-ritual seekers** | Low-friction, high-frequency touchpoints (daily card, mood check) | Subscription (Lucky Pro / Lucky Max) |
| **Depth-readers** | Structured, longer-form readings for life events | Credit packs (pay-per-reading) |
| **Skeptical first-timers** | Free entry point that doesn't feel predatory | Guest flow + email opt-in + first-reading gift |

---

## Why I made this the first product

This isn't a category I entered because I'm a believer — I entered it because it's:

- **Large and under-built.** Massive consumer demand, almost no product thinking in the category
- **AI-native.** Every module benefits from structured LLM outputs; no AI shoehorning required
- **Fast to validate.** Consumer willingness-to-pay for spiritual content is high and measurable
- **High governance surface.** Forces good habits: clear refund terms, chargeback defense, consent, RLS — skills that transfer to any regulated B2C product

The category is the *wrapper* — the real project is building a disciplined 0→1 AI consumer SaaS with strong unit economics and compliance posture.

---

## Non-goals

I explicitly did **not**:

- Build a mobile app (web-first shipped 10× faster)
- Add social features (viral loops would've doubled the scope; can add later)
- Chase every module at launch (shipped 5 modules at v1.0, added 7 more across v1.x–v2.x)
- Build custom AI models (use best-in-class APIs; swap models per module as quality/economics evolve)

Every "no" was a cost reduction that let the "yes" list actually ship.
