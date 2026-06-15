# Cheng-Wei Paperwriting Style

English | [中文说明](README.zh-CN.md)

`cheng-wei-paperwriting-style` is a Codex skill for conservative English scientific manuscript polishing. It helps revise biomedical and translational research text into a calm, precise, evidence-forward scientific register while preserving the original meaning, claims, citations, data, model systems, and uncertainty.

The skill is based on high-level prose patterns summarized from legally accessible pre-2025 papers associated with Qiang Cheng and Tuo Wei. It focuses on sentence shape, diction, transitions, hedging, paragraph rhythm, and anti-AI phrasing. It does not copy source sentences and should not be used to fabricate results, mechanisms, novelty claims, or references.

## What It Is For

Use this skill when you want to polish:

- English manuscript paragraphs
- Abstracts, introductions, results, and discussion sections
- Cover letters and response-to-reviewer text
- Biomedical delivery, oncology, immunology, nanomedicine, or translational research prose
- AI-like scientific text that needs to sound more natural, restrained, and publication-oriented

The skill is especially useful when the input already contains the correct scientific meaning but the language feels generic, promotional, overly smooth, or machine-written.

## What It Does Not Do

This skill does not:

- Invent new mechanisms, data, citations, controls, endpoints, or clinical implications
- Strengthen claims beyond the original evidence
- Replace expert scientific judgment or journal-specific editing
- Copy distinctive sentences from the reference papers
- Use paywalled full text unless lawful access is provided by the user
- Force mRNA-LNP terminology into unrelated manuscripts

## Core Behavior

The skill applies three linked principles.

### 1. Meaning preservation

It preserves:

- Numerical values, units, sample sizes, time points, doses, percentages, and statistics
- Citation placement and claim-citation pairing
- Gene, protein, disease, tissue, organ, cell-type, animal-model, and assay names
- Whether evidence is in vitro, ex vivo, in vivo, preclinical, clinical, computational, or review-based
- Hedging strength, including `may`, `could`, `suggest`, `demonstrate`, `significantly`, and similar terms

### 2. Cheng-Wei-like scientific register

The style profile favors:

- Concrete sentence subjects such as `The results`, `This strategy`, `These findings`, `We`, `LNPs`, `The formulation`, or the studied object
- Exact research verbs such as `developed`, `designed`, `engineered`, `evaluated`, `enabled`, `enhanced`, `revealed`, `confirmed`, and `suggested`
- Sentences that usually stay near 18-30 words
- Balanced active and passive voice
- Restrained transitions such as `However`, `Here`, `Notably`, `Together`, and `Overall`
- Bounded implications instead of promotional conclusions

### 3. Anti-AI polish

The skill reduces common AI-like patterns by:

- Removing generic openings such as `In recent years` or `With the rapid development of`
- Replacing vague praise with specific biological or experimental meaning
- Avoiding overbroad phrases such as `shows great promise` unless the application boundary is specified
- Reducing stacked adjectives and unsupported intensifiers
- Splitting sentences that carry too many claims at once

## Modes

### `polish`

Use when the user wants a publication-oriented rewrite with visible improvement in flow, precision, and rhythm.

Example prompt:

```text
Use cheng-wei-paperwriting-style in polish mode to revise this paragraph:

[paste paragraph]
```

### `conservative`

Use when the text is already close to final and meaning preservation is the top priority. This mode makes minimal edits and avoids strong stylistic transformation.

Example prompt:

```text
Use cheng-wei-paperwriting-style in conservative mode. Keep all claims and citations unchanged:

[paste paragraph]
```

### `diagnose`

Use when the user wants to understand why a paragraph feels AI-like before rewriting.

Example prompt:

```text
Use cheng-wei-paperwriting-style in diagnose mode. Explain what makes this paragraph sound AI-generated and suggest fixes:

[paste paragraph]
```

## Recommended Output Format

For `polish` and `conservative`, the skill should return:

1. Revised text.
2. A brief note listing meaning-sensitive choices, only when the input contains claims, citations, numbers, or uncertainty.

For `diagnose`, the skill should return:

1. Main AI-like issues.
2. Suggested fixes.
3. Optional revised version if requested.

## Installation

For local Codex use, place this folder under the Codex skills directory:

```text
~/.codex/skills/cheng-wei-paperwriting-style/
```

The required entry point is:

```text
~/.codex/skills/cheng-wei-paperwriting-style/SKILL.md
```

After installation, start a new Codex conversation or refresh the skills list. Then invoke the skill by name:

```text
Use cheng-wei-paperwriting-style to polish this manuscript paragraph...
```

## Repository Structure

```text
cheng-wei-paperwriting-style/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── corpus_inventory.md
    ├── rewrite_checklist.md
    └── style_profile.md
```

### File roles

- `SKILL.md`: Main Codex skill instructions and guardrails.
- `agents/openai.yaml`: Optional UI metadata.
- `references/corpus_inventory.md`: Paper inventory, eligibility rules, and access status.
- `references/style_profile.md`: High-level prose style profile derived from the analyzed corpus.
- `references/rewrite_checklist.md`: Meaning-preservation and anti-AI revision checklist.

## Corpus Basis

The current profile is based mainly on user-provided, legally accessible pre-2025 materials, including:

- Luo et al., 2024, `ACS Nano`
- Fei et al., 2024, `Advanced Materials`
- Lin et al., 2023, `Biophysics Reports`
- Wei et al., 2022, `Life Medicine`
- Dilliard et al., 2021, `PNAS`
- Cheng et al., 2020, `Nature Nanotechnology` author manuscript
- A 2024 Chinese Science Bulletin review used mainly for conceptual structure rather than English syntax

See `references/corpus_inventory.md` for the full record list, access notes, and inclusion rules.

## Writing Principles

When rewriting, the skill should:

- Keep one main claim per sentence where possible
- Make the sentence subject concrete
- Replace vague verbs with exact study or result verbs
- Preserve hedging at the same strength
- Shorten overlong sentences into readable scientific units
- Add transitions only when they clarify logic
- End paragraphs with bounded implications rather than broad claims

## Safety and Integrity

This skill is designed for language-level polishing. It must not change scientific content unless the user explicitly asks for scientific revision. If the input contains ambiguous, unsupported, or potentially overstated claims, the skill should flag them rather than silently rewriting them as facts.

The safest use pattern is:

1. Provide the paragraph with its citations.
2. Specify `polish`, `conservative`, or `diagnose`.
3. Ask for preservation of all claims, citations, model systems, and uncertainty.
4. Review the output against the original before manuscript submission.

## Example Prompt

```text
Use cheng-wei-paperwriting-style in polish mode. Preserve all claims, citations, cell types, animal models, and uncertainty levels. Do not add new mechanisms or references.

[paste manuscript paragraph]
```

## License and Source Text Note

This repository contains instructions, summaries, and derived high-level writing guidelines. It does not include full-text PDFs or extracted copyrighted article text. Any future corpus expansion should use open-access sources, publisher-permitted manuscripts, PMC versions, or user-provided lawful copies.
