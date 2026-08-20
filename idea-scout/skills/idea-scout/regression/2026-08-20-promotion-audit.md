# Regression fixture — 2026-08-20 promotion audit

This fixture captures the 2026-08-20 digest (run 11) that motivated feedback
issue #12: the Scout printed the required audit sections but promoted five
candidates whose own evidence fails the gates. It is the regression input for
the disposition-controlling promotion audit. **Expected outcome: zero
survivors** unless new, independent payment-form, sharing, or technical
evidence is supplied.

## How to use

Before finalizing a digest, re-run every candidate through the promotion audit
in `idea-scout/skills/idea-scout/SKILL.md` and check it against the failure
patterns below. A candidate that reproduces one of these patterns — without
new, independent, transaction-shaped evidence — is demoted, exactly as this
fixture demotes its five inputs.

## Failure patterns (the rules these candidates violate)

1. **Indirect payment proof** — spend on integrated FSM/estimating/reporting
   software cited as payment proof for a one-time document kit that omits the
   software's load-bearing paid function.
2. **Indirect solution-form proof** — autocomplete volume + marketplace
   emptiness treated as proof buyers pay for the *document-kit form*, when the
   only observed paid form is an integrated app.
3. **"Self-owned layer" reframe** — a non-equivalent product (a documentation
   layer that omits the carrier-mandated estimating/submission function)
   defended as a "self-owned layer" without separate transaction-shaped
   evidence for that layer.
4. **Private hand-off as share loop** — customer/carrier/accountant/authority
   delivery labeled as voluntary public sharing.
5. **Unverified output chain** — a named no-code chain ("Tally → PDF download")
   asserted without an end-to-end working spike of render/export, calculations,
   uploaded-file treatment, gate, and delivery.

## Candidates and audited statuses

| # | Candidate | Track | Pain | Freq. | Payment | Solution-form | Share loop | Output chain | Disposition |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Appliance Repair Documentation OS | A | PASS | PASS | INDIRECT (ServiceMinder/Service Fusion subscription spend, not one-time doc-kit spend) | INDIRECT (paid form is an integrated FSM, not a doc kit) | — | — | **Demote** |
| 2 | Backflow Test Report & Certification OS | A | PASS (single platform) | PASS | INDIRECT (Syncta spend is for a reporting app with device history + authority submission) | INDIRECT (omits device history, reminders, authority-specific forms, e-submission) | — | — | **Demote** |
| 3 | Independent Adjuster Scope-of-Loss Documentation OS | A | PASS | PASS | INDIRECT (Symbility/Xactimate remain carrier-mandated; no layer-level spend) | INDIRECT ("self-owned layer" reframe without layer evidence) | — | — | **Demote** |
| 4 | Appliance Repair Service-Report & Invoice Generator | B | PASS | PASS | — | — | CONTRADICTED (report handed to the customer = private hand-off) | UNVERIFIED ("Tally → PDF download" not spiked) | **Demote** |
| 5 | Backflow Test Report Generator | B | PASS | PASS | — | — | CONTRADICTED (report handed to the customer/water authority = private hand-off) | UNVERIFIED ("Tally → PDF download" not spiked) | **Demote** |

**Survivor count: 0 / 5.**

## Notes

- Candidates 1–3 fail G6 on INDIRECT payment and/or solution-form claims; #3's
  "self-owned layer" reframe does not rescue it because there is no separate
  transaction-shaped evidence for the documentation layer itself.
- Candidates 4–5 fail the Track B share-loop check (private hand-off to the
  customer/authority receives no share-loop credit) and the implementation
  check (the Tally→PDF chain was never rendered end to end).
- The digest's own self-check reported payment-form mismatch 1, share-loop
  mismatch 0, unverified implementation 1 — which does not reconcile to the
  five non-PASS candidates above. A correct self-check counts from these
  statuses and must read: payment-form 3, solution-form 3, share-loop 2,
  unverified implementation 2, survivors 0.
