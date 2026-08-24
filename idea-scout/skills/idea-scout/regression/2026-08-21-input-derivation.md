# Regression fixture — 2026-08-21 input-derivation boundary

This fixture captures the 2026-08-21 digest (run 13) that motivated feedback
issue #16: the Scout ran `spikes/fba_reimbursement_math.py` and promoted the
Amazon FBA Reimbursement Self-Audit Kit partly because the spike passed, even
though the spike never exercised the product's load-bearing transformation —
deriving `owed` / `kept` / non-claimable states from real Amazon Inventory
Ledger and Reimbursements report rows.

The spike began with tuples **already labeled** `owed` and `received_and_kept`,
manually converted a reversed item to `(0, 0)`, and then proved that
`owed − kept` sums correctly. The proposed product must derive those states from
raw report rows, reason codes, found/reversed events, eligibility windows,
valuation rules, and duplicate conditions — none of which was exercised. The
spike also assumed a 25% commission base without citing GETIDA's current terms.

**Expected outcome: the spike is PARTIAL/UNVERIFIED and cannot clear G1/G7**
until raw Inventory Ledger / Reimbursements-style rows are transformed into
`owed`, `kept`, and non-claimable states and the assumed commission base is
either sourced to first-party terms or removed.

## How to use

Before marking a load-bearing spike PASS, identify the earliest non-trivial
semantic boundary: if the product classifies, reconciles, or derives states from
external reports, the fixture must begin with representative raw rows (or a
documented synthetic facsimile of their exact schema) and assert the derived
classification before testing downstream arithmetic. Business rules embedded in
the fixture must cite a first-party source or be marked unverified.

## Failure patterns (the rules this artifact violates)

1. **Pre-labeled fixture** — input tuples already carry the desired conclusion
   (`owed`, `received_and_kept`), so the "reconciliation" never happens.
2. **Skipped adverse transition** — a found-after-lost, reversal, duplicate,
   missing-field, or out-of-window event is hand-converted instead of derived.
3. **Unverified business rule** — a 25% commission base is asserted without
   tying it to GETIDA's current fee terms (which define the fee against
   reimbursements, payments, and credits obtained through the service).

## Required checks (what would have caught these)

- Name the input schema (Inventory Ledger columns, Reimbursements report
  columns) and the expected derived state before any arithmetic.
- Begin with raw rows; derive `owed` / `kept` / non-claimable; then sum.
- Cover at least one ambiguous/adverse transition (reversal, duplicate, missing
  field, out-of-window, found-after-lost).
- Cite the commission base to current first-party terms or mark it unverified.

## Survivor count

**0 / 1** — the FBA Reimbursement Self-Audit Kit's implementation claim is
PARTIAL/UNVERIFIED and the candidate is demoted until an input-derivation spike
transforms raw report rows into the claimed states with a sourced commission
rule.
