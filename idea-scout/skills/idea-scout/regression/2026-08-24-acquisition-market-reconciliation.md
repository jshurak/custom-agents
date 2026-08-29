# Regression fixture — 2026-08-24 acquisition-market & payment-form reconciliation

This fixture captures the 2026-08-24 digest (run 16) that motivated feedback
issue #27: the Scout promoted a $39 Recipe Cost Calculator & Menu Pricing Kit
after summing Fiverr activity into "178 exact-form orders" and claiming a "clean
tool gap" via Gumroad (a delivery marketplace), while the named first-10-customer
plan depended on Etsy (the acquisition marketplace). The independent evaluation
opened the exact sources and found: an Etsy Bestseller priced at $5.48 offering a
close Google Sheets recipe-costing workflow; free first-party Food Cost Chef,
Apicbase, and Sheetrix sheets exposing the same load-bearing features (units,
yield/waste, per-serving cost, food-cost %, suggested menu price); and Fiverr
records that mixed a performed costing service, a template listing with no
retrievable order count, and a customized done-for-you Excel setup.

**Expected outcome under the reconciliation step: the candidate's G6 payment
proof is NOT a PASS and the "clean gap" / "178 exact-form orders" claims are
removed** — the Fiverr records are mixed-form evidence that cannot be summed,
and the acquisition marketplace (Etsy) contains a directly competing listing the
Gumroad search never opened.

## How to use

Before promoting any candidate, (1) name the acquisition marketplace the
first-customer plan depends on, separately from any delivery marketplace, and
open the strongest directly competing listing there; (2) classify every payment
record as `performed_service`, `customized_setup`, or `off_the_shelf_product`,
and never aggregate the classes.

## The inputs and their correct classifications

| Input | What the Scout reported | Reconciled classification |
|---|---|---|
| paulapirles "calculate food cost" gig (144 orders, $5) | 178 exact-form orders (component) | **`performed_service`** — a human calculated costing for the buyer; proves willingness to pay for a human outcome, not the self-serve sheet |
| makhtar1956 "recipe costing + menu analysis TEMPLATES" gig (31 orders, $115) | 178 exact-form orders (component) | **`off_the_shelf_product`** — template supply; order count not independently attributable on the focal listing (SUPPLY unless listing-bound count retrieved) |
| nilanga "excel recipe costing system" gig (3 orders, $20) | 178 exact-form orders (component) | **`customized_setup`** — done-for-you Excel build; proves payment for setup, not off-the-shelf product |
| Gumroad "recipe/food-cost = EMPTY" | "clean tool gap" | **Delivery-marketplace absence only** — does not establish a gap on the acquisition marketplace (Etsy) |
| Etsy recipe-costing sheet (Bestseller, $5.48) | not opened | **Direct acquisition-market competitor** — contradicts the gap claim and the $39 price rationale |
| Free Food Cost Chef / Apicbase / Sheetrix sheets | dismissed as scratch spreadsheets | **Feature-equivalent free substitutes** — must be compared feature-by-feature, not dismissed |

## Required checks (what would have caught these)

- Open the acquisition marketplace named in the first-10-customer plan (Etsy),
  not just the delivery marketplace (Gumroad), before claiming a gap.
- Classify each payment record by form; never sum `performed_service` +
  `customized_setup` + `off_the_shelf_product` into one "exact-form" total.
- Compare free specialist templates feature-by-feature (units, yield/waste,
  per-serving cost, food-cost %, menu price) against the proposed wedge.
- On contradiction, recompute G3, G6 solution-form status, wedge, price
  rationale, and disposition.

## Survivor count

**0 / 1** — the recipe-cost Track A candidate fails G6 payment proof (mixed-form,
non-aggregable evidence) and the wedge is contradicted by a direct Etsy
competitor + free feature-equivalent substitutes, unless a listing-bound
off-the-shelf transaction for the exact form is found and the acquisition-market
competition is reconciled in the candidate's favor.
