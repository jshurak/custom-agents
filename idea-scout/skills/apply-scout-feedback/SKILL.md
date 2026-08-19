---
name: apply-scout-feedback
description: "Ingest open idea-scout-feedback issues, judge which changes to accept, apply them to the Idea Scout skill, and ship via branch → pull request → merge → issue closure."
version: 0.1.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [idea-scout, feedback-loop, self-improvement, github-issues, github-pr]
    related_skills: [idea-scout, idea-scout-feedback]
---

# Apply Scout Feedback

Consume the `idea-scout-feedback` issues created by the Idea Evaluator and apply
the accepted improvements to the Idea Scout skill. This is the Scout-side half
of the agents' self-learning loop: the Evaluator files feedback as issues, and
this skill turns the accepted subset of that feedback into a shipped change to
the Scout methodology.

## When to Use

Run this skill:

- periodically, or whenever the user asks the Scout to "check for feedback" or
  "apply your feedback";
- after a batch of `idea-scout-feedback` issues has accumulated;
- when the user explicitly asks to ingest and apply evaluator feedback.

Do not use it to:

- file feedback (that is the `idea-scout-feedback` skill's job, on the Evaluator
  side);
- change the Scout skill on a whim without an underlying issue;
- apply feedback the Scout rejects on the merits — record the rejection instead.

## Prerequisites

- Work in the canonical `custom-agents` repository at
  `/home/hermes/repos/custom-agents`, with a clean working tree on `main`.
- `gh` authenticated with Issues and Pull Requests read/write access.
- The `idea-scout-feedback` label exists on the repository (the Evaluator-side
  skill guarantees it on every feedback issue).

## Judgment rules

Apply your best judgment; do not blindly implement every suggestion.

- **Accept** feedback that fixes a reusable Scout process failure: a missing or
  ambiguous gate, a collapsed distinction (e.g. pain vs. payment vs. solution
  form), or an overclaim about distribution or implementation.
- **Reject or scope down** feedback that overfits one niche into a universal
  threshold, prescribes magic numbers unsupported by outcome data, or asks for a
  broad rewrite with no observed failure mechanism.
- Keep thresholds niche-appropriate. Preserve the kill-rate ethos: a change that
  makes it *easier* to promote weak ideas is wrong by definition.
- One issue per pull request unless two issues are trivially the same change.
  Do not stack unrelated edits.

## Procedure

### 1. Discover open feedback

From the repository root:

```text
gh issue list --repo jshurak/custom-agents --state open --label idea-scout-feedback
```

If none are open, report that and stop.

### 2. Read and analyze each issue

```text
gh issue view <number> --json number,title,body,state,labels,url
```

Extract, for each issue:

- the requested changes (the behavior the Scout skill should adopt);
- the acceptance criteria (checkable conditions);
- the concrete examples that motivated it.

Separate facts, inferences, and proposed policy. Note anything you plan to
reject or scope down, and why.

### 3. Map changes to the skill

For each accepted change, identify the exact section of
`idea-scout/skills/idea-scout/SKILL.md` it touches (gates G1–G8, pipeline,
scoring, promotion tiers, output structure, source priority, memory, anti-slop).
Bump the skill `version` field (patch or minor) on every behavioral change.

### 4. Branch

From a clean `main`:

```text
git switch main
git pull --ff-only
git switch -c feat/apply-scout-feedback-<issue-number>
```

### 5. Edit and verify

Edit the skill (and the `idea-scout/AGENTS.md` pointer only if the change adds
or moves a skill). Then re-read the diff and check each acceptance criterion in
the issue against the new text. Every criterion must be either satisfied by the
edit or explicitly recorded as rejected with a reason.

### 6. Commit and push

```text
git add -A
git commit -m "feat(idea-scout): apply feedback from #<number>"
git push -u origin feat/apply-scout-feedback-<issue-number>
```

### 7. Open, merge, and close

```text
gh pr create --base main --head feat/apply-scout-feedback-<number> \
  --title "feat(idea-scout): apply feedback from #<number>" \
  --body "Closes #<number>"
gh pr merge --squash --delete-branch
gh issue close <number> --comment "Applied in #<pr-number>. <one-line summary>"
```

The PR body lists what changed and what was rejected. If the merge auto-closes
the issue (because the body says "Closes #<number>"), skip the explicit close —
but always verify the issue is actually closed before reporting success.

### 8. Sync the profile and report

Run the profile sync (`scripts/sync-custom-agents.sh`) so the merged skill
reaches the live profile, then report: issue number, PR number, what changed,
what was rejected (if anything), and the final issue state.

## Pitfalls

- **Blind application:** applying a suggestion the Scout should have rejected
  degrades the methodology. Record rejections instead.
- **Overfitting to one niche:** a validation threshold that worked once is not a
  universal gate.
- **Magic numbers:** never encode an unsupported sample size or conversion target.
- **Easing promotion:** a change that lowers the bar for weak ideas is a
  regression, not an improvement.
- **Stacked PRs:** unrelated edits in one branch make review and rollback harder.
- **Unclosed issue:** verify closure on the remote; do not trust the merge exit
  code alone.
- **Forgetting the sync:** the repo is canonical, but the live profile only
  changes after the sync runs.

## Verification Checklist

- [ ] Discovered open `idea-scout-feedback` issues and read each fully.
- [ ] Accepted changes map to specific skill sections; rejections recorded with reasons.
- [ ] Skill `version` bumped.
- [ ] Every acceptance criterion satisfied or explicitly rejected.
- [ ] Branch cut from clean `main`; one issue per PR.
- [ ] PR body links the issue; commit is conventional.
- [ ] PR merged; issue closed on the remote (verified).
- [ ] Profile sync ran; report lists issue, PR, changes, and rejections.
