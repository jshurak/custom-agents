# Regression fixture — 2026-08-21 semantic spike correctness

This fixture captures the 2026-08-20-r4 digest (run 12) that motivated feedback
issue #14: the Scout executed every load-bearing spike and reported each as
PASS, yet two promoted ideas shipped artifacts whose *semantic* content was
wrong. It is the regression input for the semantic-correctness requirement on
implementation spikes. **Expected outcome: the two named artifacts FAIL the
spike gate** because they verify file emission, not the claimed outcome.

## How to use

Before marking a load-bearing spike PASS, re-run it against the failure
patterns below. A spike that only proves the file was generated — without an
independently computed test case, a domain invariant, or a named
client/environment matrix — is **PARTIAL/UNVERIFIED** and cannot clear G1/G7 by
itself, exactly as this fixture demotes its two inputs.

## Failure patterns (the rules these artifacts violate)

1. **Wrong metric definition** — a figure labeled NOI is computed after
   subtracting mortgage debt service. NOI is *pre-financing* by definition; a
   workbook that labels a post-debt-service figure "NOI" misstates the metric.
2. **Internally inconsistent fee treatment** — a cleaning fee is labeled
   *revenue* (added to gross) and then also subtracted in full as an *expense*,
   double-counting the same cash flow.
3. **Compatibility asserted, not tested** — an artifact is described as
   "email-client-safe" or "vertical-compliance" without running the actual
   client matrix (Gmail/Outlook/Apple Mail) or implementing the claimed
   compliance field packs.

## The two failing artifacts

| # | Artifact | Claimed | Actual | Semantic verdict |
|---|---|---|---|---|
| 1 | `str_projector.xlsx` (STR Revenue & Expense Projector) | correct NOI / CoC projection | labels a post-debt-service figure "NOI"; labels cleaning fees as revenue *and* subtracts them as expense | **FAIL — metric misdefinition + inconsistent fee treatment** |
| 2 | `signature_sample.html` (Email Signature Generator) | email-client-safe signature with DRE/NMLS/HIPAA packs | table-based HTML only; no vertical packs implemented; no Gmail/Outlook/Apple Mail render test | **FAIL — compatibility asserted, not tested** |

## Required checks (what would have caught these)

- **Spreadsheet/calculator:** an independent hand-computed test case. E.g. a
  property with $0 debt service must yield the same NOI whether or not a
  mortgage line exists; a cleaning fee of $X must change NOI by $0 net of its
  own revenue/expense treatment (or by a single, named, non-double-counted
  effect).
- **Generated artifact:** open the rendered file and confirm the promised
  fields/calculations/delivery appear (not just that the file exists).
- **Compatibility:** name the exact client/environment matrix tested; list any
  untested environment as untested, never as PASS.

## Survivor count

**0 / 2** — both artifacts would be demoted to validation-lead status until a
semantically correct spike (with the above checks passing) is produced.
