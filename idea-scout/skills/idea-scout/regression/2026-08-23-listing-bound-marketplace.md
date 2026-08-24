# Regression fixture — 2026-08-23 marketplace listing-bound attribution

This fixture captures the 2026-08-23 digest (run 15) that motivated feedback
issue #19: the Scout promoted a Rent Roll & Tenant Ledger Spreadsheet after
citing exact Fiverr gigs and reporting review counts of 370 / 113 / 88 / 84 /
80 / 53 / 44 from the live pages' **related-gig shelves**. The independent
evaluation opened the exact gigs: two exposed no completed-order or review
count, and one seller profile showed only one completed order. The large counts
belonged to generic recommended Excel gigs, not to the rent-roll outcome. The
same digest cited Etsy listing 1543461345 (a property-investment ROI/cash-flow
analyzer, not a rent-roll/tenant-ledger tracker) and `rentledger.pro` (a parked
domain) as form-matched corroboration.

**Expected outcome under listing-bound attribution: the candidate's G6 payment
proof is NOT a PASS** — the marketplace signals collapse to *supply* (two
no-count gigs) + *one narrow transaction signal* (one-order seller) + *adjacent
INDIRECT evidence* (Etsy ROI analyzer) + *CONTRADICTED* (parked domain).

## How to use

Before marking a marketplace payment signal PASS, bind every count to the focal
listing: record `canonical_url`, `seller`, `listing_title`, `paid_outcome`,
`solution_form`, `transaction_indicator`, and `retrieval_date`. A count from a
related-gig shelf, a seller-wide profile, a search-result card, or an ad cannot
be attached to the focal listing unless the marketplace identifies it as that
listing's transactions.

## The inputs and their correct classifications

| Input | What the Scout reported | Listing-bound classification |
|---|---|---|
| jesper_krahl "property management spreadsheet, rent roll tracker, maintenance dashboard" gig | form-matched seller with high review count | **SUPPLY** — live page exposes no completed-order/review count attributable to this gig; the 370/113/… counts are related-shelf numbers |
| mike_fea "automated real estate spreadsheet for rent roll property management" gig | form-matched seller with high review count | **SUPPLY** — no attributable completed-order/review count on the focal listing |
| johnson_kemaun "rent roll, tenant ledger, cash flow…" gig | form-matched seller with high review count | **ONE NARROW TRANSACTION SIGNAL** — one completed order visible; does not establish repeated paid work |
| Etsy listing 1543461345 (assetafc) | rent-tracking spreadsheet corroboration | **INDIRECT / ADJACENT** — the listing is a property-investment ROI/cash-flow deal analyzer, not a rent-roll/tenant-ledger tracker; its purchase-gated review proves adjacent spreadsheet payment only |
| `rentledger.pro` | current paid product corroboration | **CONTRADICTED** — domain is parked at Namecheap; no product, price, or transaction evidence |

## Required checks (what would have caught these)

- Open the focal listing and read its *own* transaction indicator (completed
  orders / purchase-gated reviews), not the shelf around it.
- Confirm the listing's delivered outcome matches the candidate's load-bearing
  workflow (rent tracking ≠ deal analysis).
- Re-check any named corroborating URL; a parked/redirected/dead page is
  CONTRADICTED and contributes zero payment credit.
- Recompute the G6 status from the listing-bound records only.

## Survivor count

**0 / 1** — the rent-roll Track A candidate fails G6 payment proof and is
demoted to a validation lead (or killed) unless a listing-bound
transaction-shaped signal for the exact rent-roll/tenant-ledger form is found.
