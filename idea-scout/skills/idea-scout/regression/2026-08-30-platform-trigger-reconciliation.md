# Regression fixture — 2026-08-30 platform-trigger reconciliation

This fixture captures the 2026-08-30 digest (run 22) that motivated feedback
issue #31: the Scout ran a bounded named-trigger check and treated third-party
fee-tracker facts as current event inputs, then generalized from one visible
tracker hub to a structural claim that calculator sites auto-emit a free tool
for every fee event. The independent evaluation reconciled the triggers against
live platform-owned pages and found two load-bearing conflicts:

- the digest reported Shopify Basic's third-party-provider surcharge rising from
  2.0% to 2.2% on June 9, 2026, while Shopify's current pricing page shows 2%;
- the digest reported PayPal Pay with Crypto changing from 0.99% to 1.5% on
  August 1, 2026, while PayPal's merchant-fee page says 2026 but its live
  campaign page says the 0.99% promotion lasts through July 31, 2027.

**Expected outcome under the platform-trigger reconciliation rule: the Shopify
2.2% claim is CONTRADICTED by current first-party pricing, the PayPal effective
date is CONFLICTED (first-party pages disagree), both triggers receive no timing
credit, and the "ecosystem auto-emits a tool for every event / structurally
closed" claim is downgraded to bounded, sample-scoped language. The zero-survivor
result is preserved because neither trigger has G6 buyer or payment evidence.**

## How to use

Before a named platform fee/pricing/policy event earns timing credit, produce a
source-reconciliation record (platform, market/region, affected plan/product,
old value, new value, announcement date, effective date, retrieval date,
canonical first-party URL), check the current platform-owned governing page plus
any dated changelog/policy page, and classify agreement among first-party
sources. A third-party tracker, affiliate page, news article, or search snippet
can discover an event but cannot mark it VERIFIED.

## The inputs and their correct classifications

| Input | What the Scout reported | Reconciled classification |
|---|---|---|
| Shopify Basic third-party-provider surcharge 2.0% → 2.2% (2026-06-09) | fresh dated trigger, "immaterial" | **CONTRADICTED** — Shopify's current pricing page shows 2%; the 2.2% figure appears only on third-party tracker/news pages. No first-party changelog supplied. |
| PayPal Pay with Crypto 0.99% → 1.5% (2026-08-01) | fresh dated trigger, "payment-method-niche, no wedge" | **CONFLICTED** — PayPal's merchant-fee page states 2026 while its campaign page says the 0.99% promotion lasts through July 31, 2027. Effective date unresolved; no timing credit. |
| "fee-tracker sites auto-emit a free 'calculate this fee change' tool for every new fee event — the well is structurally closed" | structural market conclusion | **UNVERIFIED / OVERGENERALIZED** — one hub + several calculators prove severe substitution for the *checked* events, not a universal generation mechanism or accuracy claim. Downgrade to bounded, sample-scoped language. |
| "free tools already calculate the Amazon FBA surcharge" | free-saturation support | **availability / claimed scope only** — the tools exist and claim current rates; runtime accuracy was not exercised against a first-party fixture. |

## Required checks (what would have caught these)

- Reconcile each named trigger against the current platform-owned
  pricing/policy/developer page (and dated changelog when available) before
  using it as a timing edge.
- Mark an event CONFLICTED when current first-party pages disagree; report the
  exact disagreement and withhold timing credit until reconciled.
- Do not generalize a region- or plan-specific rate beyond its documented scope.
- Distinguish "a substitute exists and claims current rates" from "the
  substitute was run against a first-party fixture and was correct".
- Use bounded language naming the sampled sites/events; never upgrade a sample
  to "every event" or "structurally closed".

## Survivor count

**0 / 0** — no candidate reached the gates; both triggers are ineligible for
timing credit (one CONTRADICTED, one CONFLICTED), and no G6 pain, urgency,
payment, or solution-form evidence exists, so the zero-survivor result is
preserved. A future trigger survives only when it carries first-party-verified
facts, fresh target-buyer behavior, and a demonstrated substitute gap.
