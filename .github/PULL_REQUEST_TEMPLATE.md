## What does this PR change?

<!-- One paragraph. What is being added, modified, or removed? -->

## Why

<!-- The reason for the change. Reference any internal decision or discussion. -->

## Reviewer checklist – press-release-grade gate

Reviewer, before approving this PR, verify ALL of the following:

- [ ] **No internal methodology IP** – nothing in this diff exposes scoring formulas, algorithms, internal frameworks, training pipeline details, or proprietary methodology mechanics. If a reader could reproduce the methodology from this content, REJECT.
- [ ] **No internal terminology** – the product is **Creative Engines**. Internal shorthand (e.g. "CREN") MUST NOT appear in any public-facing file. Use the full product name everywhere.
- [ ] **No customer or partner data** – no real client names, real campaigns, real numbers, real conversations.
- [ ] **No pricing or commercial terms** – pricing details, contracts, and commercial terms do not live in this repo. If this PR adds any, treat as a deliberate exception and require both founders' approval.
- [ ] **No internal personal information** – no founder personal contact details beyond what is already public.
- [ ] **No hallucinated content** – every claim is verifiable. Numbers, dates, and named entities have been cross-checked against the canonical sources.
- [ ] **Voice and style** – active voice, no marketing buzzwords (no "seamlessly", "intuitive", "robust", "leverage", "unlock", "empower", "game-changing"), no "X isn't Y; it's Z" pivot constructions, no em-dashes without spaces.
- [ ] **English only** – no Russian or other-language prose. Verbatim quotations from non-English sources are acceptable when clearly demarcated.
- [ ] **Markdown discipline** – clean H1 → H2 → H3 hierarchy; one H1 per file; YAML frontmatter present where used; no large binaries.
- [ ] **Public-safe** – if this content appeared on the home page of TechCrunch tomorrow, would it embarrass us? If yes, REJECT.

## Reviewer

<!-- Approval requires a founder who is NOT the PR author. Self-approval is blocked by GitHub. -->
