---
name: idea-scout-feedback
description: "Turn evaluation patterns into actionable Scout issues."
version: 0.1.0
author: jshurak, Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [idea-evaluator, idea-scout, feedback-loop, github-issues, calibration]
    related_skills: [idea-evaluator, github-issues]
---

# Idea Scout Feedback

Convert recurring findings from Idea Evaluator runs into actionable GitHub
issues for the Idea Scout. This is the Evaluator-to-Scout half of the agents'
self-learning loop: it records process improvements without directly rewriting
the Scout or turning every rejected idea into an issue.

## When to Use

Use this skill after an evaluation when:

- the same Scout reasoning error appears across multiple ideas or runs;
- a load-bearing gate was missing, ambiguous, or applied inconsistently;
- independent research contradicts a reusable Scout assumption;
- real validation or launch outcomes reveal a calibration error;
- the user asks to turn evaluation feedback into a Scout improvement issue.

Do not use it for:

- a weakness unique to one otherwise ordinary candidate;
- a disagreement caused only by unavailable evidence;
- speculative preferences with no observed failure mechanism;
- direct edits to the Scout skill unless the user separately requests them;
- duplicate feedback already represented by an open issue.

## Prerequisites

- Work in the canonical `custom-agents` repository.
- Load the `idea-evaluator` skill and finish the evaluation before extracting
  process-level feedback.
- Use `gh` authenticated with Issues read/write access to the repository.
- Apply both labels to every issue created through this workflow:
  - `idea-scout-feedback`
  - `feedback-author-idea-evaluator`

If either label is missing, stop and report the missing repository prerequisite;
do not silently substitute a different label.

## Issue Standard

Each issue must describe one reusable Scout improvement and contain:

1. **Context** — which evaluation run or outcome exposed the problem.
2. **Observed pattern** — the repeated reasoning or gate failure, with concrete
   examples from the evaluation.
3. **Why it matters** — how the pattern can promote weak candidates, kill strong
   ones, or waste operator time.
4. **Requested change** — the behavior the Scout skill should adopt without
   prescribing unnecessary wording or implementation details.
5. **Acceptance criteria** — checkable conditions a future Scout run or skill
   review can verify.
6. **Non-goals** when needed — boundaries that prevent the fix from becoming a
   broad rewrite or a universal numeric threshold.

Write the issue so the Scout maintainer can implement it without reopening the
original evaluation transcript. Separate facts, inferences, and proposed policy.
Do not include private data, secrets, unsupported quotations, or invented
examples.

## Procedure

### 1. Extract the reusable pattern

Review the final evaluation, Scout calibration notes, and any real-world outcome.
State the pattern as:

> When the Scout does **X**, it tends to produce **Y**, because **Z** is not
> adequately checked.

Require at least one concrete example. Prefer multiple ideas or runs. If the
finding cannot be generalized without changing the customer, product, or
business model, keep it in the evaluation report instead of creating an issue.

**Completion criterion:** the proposed feedback identifies a Scout process
failure rather than merely restating an idea's verdict.

### 2. Check for duplicates

Use `terminal` from the repository root:

```text
terminal(command="gh issue list --state all --label idea-scout-feedback --limit 100 --json number,title,body,state,url", timeout=120)
```

Search titles and bodies for the same failure mechanism. If an open issue already
covers it, add a concise comment with the new evidence instead of creating a
second issue. If a closed issue covers it, create a new issue only when the old
fix regressed or materially new evidence changes the required behavior; link the
closed issue and explain what changed.

**Completion criterion:** the new issue is distinct, or the existing issue has
received the incremental evidence.

### 3. Draft the issue

Use a specific, behavior-oriented title such as:

> Tighten solution-form payment proof before promoting Track A ideas

Draft the body under these headings:

```markdown
## Context

## Observed pattern

## Why it matters

## Requested change

## Acceptance criteria

- [ ] ...

## Non-goals
```

Acceptance criteria must be observable in the Scout skill or a future Scout
report. Avoid vague items such as “improve research” or “be more rigorous.” Do
not impose universal sample sizes or conversion thresholds unless outcome data
supports them across the affected niche.

**Completion criterion:** every requested behavior maps to at least one
acceptance criterion, and every example is grounded in the completed evaluation.

### 4. Create and label the issue

Save the body to a temporary Markdown file with `write_file`, then use `terminal`
from the repository root:

```text
terminal(command="gh issue create --title \"<title>\" --body-file <body-file> --label idea-scout-feedback --label feedback-author-idea-evaluator", timeout=120)
```

Do not create an unlabeled issue and promise to label it later. The two labels
encode both the feedback target and its author, which makes the learning loop
queryable.

**Completion criterion:** GitHub returns the issue URL.

### 5. Verify the remote issue

Read the created issue back with:

```text
terminal(command="gh issue view <number> --json number,title,body,state,labels,url", timeout=120)
```

Confirm that:

- the issue is open;
- the title and body describe the intended reusable improvement;
- both required labels are present exactly once;
- the URL belongs to the canonical repository.

If verification fails, repair the issue with `gh issue edit` and verify again.
Never report success based only on the create command's exit code.

**Completion criterion:** the read-back contains the expected issue, state, URL,
and both labels.

### 6. Report and preserve the loop

Return the issue number, title, URL, and labels to the user. The issue—not memory
or an uncommitted local note—is the durable work item for changing the Scout.
Record evaluation outcomes separately according to the Idea Evaluator's memory
rules; do not store issue numbers as long-term memory.

**Completion criterion:** the user can open the verified issue and understand the
proposed Scout improvement without additional context.

## Pitfalls

- **Issue per rejection:** rejected ideas are evaluation outcomes, not necessarily
  Scout process defects. Create feedback only for reusable failures.
- **Duplicate learning requests:** search closed issues as well as open ones.
- **Pain/payment collapse:** “users have pain” and “users pay for this solution
  form” are separate claims; feedback should preserve that distinction.
- **Overfitting:** do not turn one niche's validation threshold into a universal
  gate.
- **Solution disguised as diagnosis:** specify the required Scout behavior and
  acceptance criteria, but leave harmless wording choices to the implementer.
- **Unverified creation:** always read the remote issue back and inspect labels.
- **Direct mutation:** this workflow proposes Scout changes through an issue. It
  does not edit or merge the Scout skill unless the user explicitly requests the
  implementation work.

## Verification Checklist

- [ ] Feedback describes a reusable Scout process improvement.
- [ ] At least one grounded evaluation example supports it.
- [ ] Existing open and closed feedback issues were checked.
- [ ] The issue is self-contained and has checkable acceptance criteria.
- [ ] No private data, invented evidence, or unsupported universal threshold was added.
- [ ] `idea-scout-feedback` is present.
- [ ] `feedback-author-idea-evaluator` is present.
- [ ] The remote issue was read back successfully.
- [ ] The final response includes the verified GitHub URL.
