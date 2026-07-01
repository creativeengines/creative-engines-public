---
title: "Brand Knowledge"
status: Current
last_updated: 2026-07-01
audience: [buyers, users, agencies, ai-assistants]
tags: [product, brand-knowledge, source-grounding, hybrid-search, creative-engines]
---

# Brand Knowledge

Brand Knowledge is the product area for organizing approved brand context so every strategy and content task can start from the brand's real material instead of generic web knowledge.

Creative Engines should not behave like an empty chat window. It should know which brand it is working for, which source material is approved, and which context should constrain the work.

## How it works

1. **Upload** – add source files to a brand (text, Markdown, PDF, Word, HTML, CSV): decks, docs, transcripts, exports.
2. **Ingest** – each document is processed into many small, coherent, searchable pieces, each assessed for quality, so retrieval surfaces the strongest material and avoids redundancy. The brand's knowledge becomes retrievable at the paragraph level.
3. **Ground** – when a content session runs its research step, the most relevant pieces are pulled into the draft, and gaps in the brand's knowledge are flagged.

Retrieval uses hybrid search – combining semantic relevance (conceptually related material) with keyword relevance (the exact words) – so the product finds the right context even when brand knowledge is scattered across decks, notes, interviews, and prior work.

## What it does today

- **Document upload** across common file types, so the brand's real material becomes the foundation content is written from.
- **Ingestion into searchable pieces**, quality-assessed, retrievable at the paragraph level.
- **Grounded retrieval during content research** – relevant brand material pulled into a draft, with thin spots flagged. This is the difference between brand-specific content and generic AI output.
- **Document management** with active and archived views, bulk actions, and status badges; archiving a document removes its content from all downstream retrieval.
- **A knowledge explorer** to view, search, filter, and preview individual pieces of brand knowledge with their quality assessments.
- **Multiple retrieval modes and filtering** – balanced, wide, or deep retrieval, plus filtering by source type, quality, recency, and topic.

## On the roadmap

- **More source connectors** – pulling brand knowledge automatically from cloud sources beyond manual upload (existing blog or CMS content, a connected document store, a knowledge repository) and keeping it in sync as the source changes.

## What it helps decide

- Which source material should guide a task.
- Whether content has enough grounding to proceed.
- Which claims need support from approved knowledge.
- Which brand facts, examples, or explanations should be reused.
- Where a draft risks becoming generic because it lacks source context.

## How it connects to other product areas

Brand Knowledge supports [Brand Strategy](./brand-strategy.md) by giving strategy work a reliable base of context. It supports [Creative Studio](./creative-studio.md) by grounding drafts and reviews in approved source material. It supports [Editorial Governance](../concepts/editorial-governance.md) by helping reviewers ask where a claim or decision came from.

## Public boundary

This page explains source grounding at a client level. It can name hybrid search as a concept, but does not publish retrieval settings, source-processing rules, quality-evaluation details, storage design, or protected knowledge-organization methods.

## See also

- [Product](./README.md)
- [Brand Strategy](./brand-strategy.md)
- [Creative Studio](./creative-studio.md)
- [Editorial governance](../concepts/editorial-governance.md)
- [Brand voice](../concepts/brand-voice.md)
