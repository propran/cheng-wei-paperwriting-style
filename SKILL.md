---
name: cheng-wei-paperwriting-style
description: Use when polishing English scientific manuscripts, abstracts, introductions, discussions, cover letters, or response-to-reviewer text to reduce AI-like prose while preserving scientific meaning, claims, citations, data, scope, and hedging. The skill applies high-level English paper-writing style patterns derived from legally accessible pre-2025 Cheng Qiang and Tuo Wei corpus materials, focusing on diction, syntax, transitions, paragraph rhythm, and claim strength rather than research-topic content.
---

# Cheng-Wei Paperwriting Style

## Status

This skill includes a Phase 2 English prose profile derived from user-provided pre-2025 Cheng/Wei corpus PDFs. The priority is diction, syntax, transitions, paragraph rhythm, and claim strength rather than research-topic imitation. Use only high-level style patterns; do not copy source sentences.

## Quick Workflow

1. Identify the user's requested mode:
   - `polish`: rewrite in a precise, compressed scientific register.
   - `conservative`: make minimal edits with maximum meaning preservation.
   - `diagnose`: explain why the text feels AI-like and propose edits.
2. Before rewriting, preserve:
   - all citations, gene/protein names, cell types, animal models, dose/time details, statistical claims, and limitations;
   - the original certainty level, including words such as `may`, `could`, `suggest`, `demonstrate`, `significantly`, and `robustly`;
   - the same experimental scope, disease model, and translational distance.
3. Consult `references/rewrite_checklist.md` for mandatory checks.
4. Consult `references/style_profile.md` for the approved high-level Cheng/Wei corpus style profile.
5. Consult `references/corpus_inventory.md` only when the user asks what literature supports the skill, which papers are eligible, or whether a source may be legally analyzed.

## Guardrails

- Never invent mechanisms, study results, novelty claims, journal impact, author roles, citations, or clinical relevance.
- Do not copy distinctive sentences or long phrases from the source papers.
- Do not use paywalled full text for style analysis unless the user provides lawful access.
- Keep terminology specific to the user's field, but do not force mRNA-LNP vocabulary into unrelated text.
- Prioritize concrete subjects, exact verbs, restrained transitions, and preserved hedging over topic-specific imitation.
- For `conservative` mode, prioritize clarity and naturalness over visible stylistic transformation.

## Output Format

For `polish` or `conservative`, return:

1. Revised text.
2. A brief note listing any meaning-sensitive choices, only if the text involved claims, citations, numbers, or uncertainty.

For `diagnose`, return:

1. Main AI-like issues.
2. Suggested fixes.
3. Optional revised version if the user asks for one.
