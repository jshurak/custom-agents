# Regression fixture — 2026-08-27 temporal provenance & negative claims

This fixture captures the 2026-08-27 digest (run 19) that motivated feedback
issue #28: the Scout issued an integrity correction declaring its run-18
"getpinflow.com" nutrition-label citation **fabricated** because the cited path
returned 404 and the root domain marketed Pinterest tooling, and in the same
digest called Supplement-Facts analysis "genuinely uncovered." The independent
evaluation found a current first-party PinFlow nutrition-label page at
`/tools/nutrition-label-generator` exposing the attributed capabilities, and
first-party Food Label Maker and NutriCalcPro pages advertising supplement
formula/ingredient workflows and Supplement Facts output.

**Expected outcome under the temporal-provenance rule: the "fabricated" claim
is replaced with `UNAVAILABLE_AT_CITED_URL` (path disproven, product not), the
historical fabrication claim is UNVERIFIED, and the "genuinely uncovered" claim
is downgraded to "none found in checked sources" and recomputed against the
opened substitutes.**

## How to use

Before correcting a citation or declaring a niche uncovered, distinguish four
states — invalid/stale URL, temporarily unavailable page, product at a different
canonical route, fabricated/nonexistent product — and preserve temporal
provenance for any historical claim.

## The inputs and their correct classifications

| Input | What the Scout reported | Correct classification |
|---|---|---|
| `getpinflow.com` (run-18 cited nutrition-label URL, 404 at cited path) | FABRICATED — "product never existed" | **UNAVAILABLE_AT_CITED_URL** — only the cited path was disproven; product identity is not disproven. Current canonical page at `/tools/nutrition-label-generator` is real. |
| "getpinflow is a Pinterest marketing tool, not a nutrition-label generator" (root-domain description) | load-bearing for the fabricated claim | **INSUFFICIENT** — an unrelated root homepage does not disprove a sibling tool page; recovery checks (site search / canonical paths) were not run. |
| "Supplement-Facts analysis is genuinely uncovered" | uncovered claim | **CONTRADICTED as stated** — Food Label Maker and NutriCalcPro advertise supplement formula/ingredient workflows; downgrade to "none found in checked sources" and recompute the wedge against them. |
| Historical claim that the PinFlow citation never existed at the prior retrieval date | implied by "fabricated" | **UNVERIFIED** — no dated capture/archive/prior extraction establishes absence at the prior time. |

## Required checks (what would have caught these)

- Run site search / search-engine results and plausible canonical paths before
  declaring a product nonexistent; a 404 or unrelated root page is not
  fabrication.
- Record the exact cited URL, retrieval date, HTTP/result state, final canonical
  URL, and whether product identity or only the path was disproven.
- Use bounded language ("none found in checked sources") unless absence is
  independently established.
- Before an uncovered claim, open the strongest current first-party substitutes
  (Food Label Maker, NutriCalcPro) and compare the load-bearing workflow.

## Survivor count

**0 / 1** — the nutrition/supplement-facts Track A candidate's "uncovered
supplement-facts analysis" wedge is contradicted by first-party supplement-software
competitors, so the wedge must be recomputed against them (and still requires the
evaluator's manual paid pilot for the remaining correctness-critical gap); the
run-18 free-saturation conclusion is correspondingly softened from "formatters
plus analyzers are free-saturated" to "formatting is free-saturated; correct
recipe→supplement-facts analysis is bounded-underserved in checked sources."
