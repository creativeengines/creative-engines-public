# Branch Protection – pending config

This file documents the branch protection rules that **must** be applied to `main` before this repository is flipped from Private to Public.

## Current state (as of repo creation)

- **Repo is PRIVATE.** Org plan is `free`, which does NOT support branch protection or repository rulesets on private repos. GitHub returns: *"Upgrade to GitHub Pro or make this repository public to enable this feature."*
- **A post-hoc audit workflow is in place** ([`.github/workflows/main-push-audit.yml`](workflows/main-push-audit.yml)) that fires on every push to main and flags non-PR-merge commits. This is a visibility signal, not a block.
- **CODEOWNERS is in place** ([CODEOWNERS](CODEOWNERS)) but is only enforced when branch protection is active. Without protection it auto-requests reviews but does not block merges.

## Action required before going public

Apply the ruleset below. Two paths to unlock it:

1. **Flip the repo to Public.** At that moment all branch protection features become free. Recommended sequence: founder review of full content → flip to public → IMMEDIATELY apply ruleset before the public URL is shared anywhere.
2. **Upgrade org to GitHub Team.** ~$4 per seat per month, ~$24/month at current 6 seats. Unlocks protection on private repos so the protection lives through the pre-launch phase.

## Ruleset to apply

```json
{
  "name": "Protect main – press-release-grade gate",
  "target": "branch",
  "enforcement": "active",
  "conditions": {
    "ref_name": {
      "include": ["refs/heads/main"],
      "exclude": []
    }
  },
  "bypass_actors": [],
  "rules": [
    { "type": "deletion" },
    { "type": "non_fast_forward" },
    { "type": "required_linear_history" },
    {
      "type": "pull_request",
      "parameters": {
        "required_approving_review_count": 1,
        "dismiss_stale_reviews_on_push": true,
        "require_code_owner_review": true,
        "require_last_push_approval": true,
        "required_review_thread_resolution": true,
        "allowed_merge_methods": ["squash", "rebase"]
      }
    }
  ]
}
```

## Apply command

Once the repo is public (or the org is on Team):

```bash
gh api -X POST /repos/creativeengines/creative-engines-public/rulesets \
  --input .github/branch-protection-config.json
```

Where the JSON file holds the ruleset body above. See [GitHub Rulesets API](https://docs.github.com/rest/repos/rules#create-a-repository-ruleset).

## Verification after applying

- Try `git push origin main` directly → must be rejected.
- Open a PR and try to self-approve → GitHub web UI will not allow it.
- Try to force-push → must be rejected.
- Try to delete `main` → must be rejected.

## Why these specific rules

- **`deletion`** – nobody can delete `main`.
- **`non_fast_forward`** – nobody can force-push (history is immutable).
- **`required_linear_history`** – no merge commits; rebase or squash only. Keeps history clean and auditable.
- **`required_approving_review_count: 1`** – at least one human review.
- **`require_code_owner_review: true`** – the reviewer must be a CODEOWNER for the changed paths.
- **`require_last_push_approval: true`** – any new push after approval invalidates the approval. Prevents the "approve, then add a malicious commit" pattern.
- **`dismiss_stale_reviews_on_push: true`** – complements the above. New commits drop old approvals.
- **`required_review_thread_resolution: true`** – every review comment must be resolved before merge.
- **`allowed_merge_methods: ["squash", "rebase"]`** – no merge commits (matches `required_linear_history`).
- **Empty `bypass_actors`** – nobody bypasses, not even admins. Equivalent to "Include administrators" in classic branch protection.
