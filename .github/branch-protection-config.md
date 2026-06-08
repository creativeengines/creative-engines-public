---
title: "Branch Protection Policy"
status: Current
last_updated: 2026-06-08
audience: [maintainers, reviewers, ai-assistants]
tags: [github, branch-protection, review-governance, creative-engines]
---

# Branch Protection Policy

This file documents the intended protection rules for `main`.

## Required policy

- No direct pushes to `main`.
- No force pushes.
- No branch deletion.
- Pull request review required before merge.
- Code owner review required when CODEOWNERS is active.
- New commits after approval require fresh review.
- All review threads must be resolved before merge.
- Use squash or rebase merge only.
- No bypass actors.

## Ruleset body

Use `.github/branch-protection-config.json` as the ruleset body when applying repository rules.

## Verification

After rules are active:

- Direct push to `main` is rejected.
- Force push is rejected.
- Branch deletion is rejected.
- A pull request cannot merge without required review.
- A new commit after approval invalidates the previous approval.

## See also

- [CODEOWNERS](CODEOWNERS)
- [Pull request template](PULL_REQUEST_TEMPLATE.md)
- [Main push audit workflow](workflows/main-push-audit.yml)
