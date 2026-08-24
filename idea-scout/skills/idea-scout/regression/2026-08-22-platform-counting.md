# Regression fixture — 2026-08-22 platform-vs-community/thread counting

This fixture captures the 2026-08-22 digest (run 14) that motivated feedback
issue #18: the Scout promoted an eBay Reseller Fee & Profit Tracker after
reporting pain proof from r/eBaySellerAdvice, r/Ebay, and r/Flipping as a
"multi-platform" evidence vein. All three are Reddit communities, so the
evidence spans three threads but only **one platform** — it does not satisfy
the two-platform G6 pain rule.

**Expected outcome under mechanical independence counting: G6 pain proof is
FAIL** unless a qualifying second-platform source is added. Three Reddit threads
across three Reddit communities = one platform.

## How to use

Before marking a pain claim PASS, record each item's `platform` (normalized
host), `community`, `thread_or_transaction`, `person_or_buyer`, `source_date`,
and `retrieval_date`. Derive the distinct-platform count from normalized
platform identifiers — never from the number of subreddits, threads, or
communities. A recency claim cannot be bridged by a retrieval date or an
autocomplete hit.

## The input and its correct classification

| Field | Value |
|---|---|
| Quotes retrieved | 3 verbatim buyer quotes (eBay seller fee pain) |
| Communities | r/eBaySellerAdvice, r/Ebay, r/Flipping |
| Threads | 3 independent threads |
| Distinct platforms (normalized) | **1** (Reddit) |
| G6 pain PASS/FAIL | **FAIL** — two-platform requirement unmet |
| Two full quotes dated | 2021 (recency gap not bridged by a current second-platform buyer statement) |

## Required checks (what would have caught these)

- Normalize platform = host/service, not subreddit or thread.
- Print both distinct-thread count and distinct-platform count in the G6 audit.
- A two-platform claim cannot be PASS with all evidence on one host.
- Distinguish `source_date` (when the buyer wrote it) from `retrieval_date`
  (when the Scout fetched it); a current retrieval date or an autocomplete hit
  cannot stand in for a current buyer statement.

## Survivor count

**0 / 1** — the eBay tracker's pain claim fails the distinct-platform bar and
the candidate is demoted until a qualifying second-platform buyer statement
(e.g. Trustpilot, app-store review, forum) is added.
