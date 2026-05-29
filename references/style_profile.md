# Style Profile

Status: Phase 2 complete for the user-provided PDF corpus. This profile emphasizes English scientific prose style, not research-topic content. Use high-level patterns only; do not copy source sentences.

## Corpus Basis

The English style profile is based mainly on six English PDFs: Fei 2024 Advanced Materials, Luo 2024 ACS Nano, Lin 2023 Biophysics Reports, Wei 2022 Life Medicine, Dilliard 2021 PNAS, and the 2020 SORT author manuscript. The Chinese Science Bulletin PDF is useful for conceptual structure but should not drive English syntax.

The extracted English corpus contained about 59,500 words and 2,053 usable sentences. Average sentence length was about 25 words, median length about 23 words, with passive constructions in roughly one-third of sentences.

## Overall Voice

- Write in a calm, compressed, evidence-forward style.
- Prefer concrete sentence subjects: `The results`, `This strategy`, `These findings`, `We`, `LNPs`, `The formulation`, `The platform`.
- Avoid conversational framing, broad claims, and ornate adjectives.
- Let precision carry authority: use clear nouns, exact verbs, and measured implications.
- Balance active and passive voice. Use active voice for what the authors did; use passive voice for methods, formulations, measurements, and established observations.

## Sentence Shape

- Target 18-30 words for most sentences.
- Use one main claim per sentence; split AI-like compound sentences that contain multiple claims joined by `and`, `while`, or `which`.
- Prefer this shape for contribution sentences:
  - field limitation -> `Here/Herein, we ...`
  - intervention -> measured effect
  - result -> implication
- Prefer this shape for evidence sentences:
  - `These results/This observation` + verb + bounded conclusion.
- Use longer sentences only when the syntax tracks a clear causal chain.

## Common Sentence Openings

Use these naturally, without overloading any one pattern:

- `The ...` for objective statements and results.
- `This ...` for linking a result to the preceding sentence.
- `These results ...` or `These findings ...` for paragraph-level inference.
- `We ...` for study actions: designed, developed, investigated, evaluated, demonstrated.
- `To ...` for purpose-driven experimental logic.
- `In addition`, `Furthermore`, or `Moreover` for additive evidence.
- `However` for a real limitation or contrast.
- `Notably` for an important result, not for routine facts.
- `Overall`, `Together`, or `Collectively` for final synthesis.

Avoid starting paragraphs with generic phrases such as `In recent years`, `With the rapid development of`, `In the current era`, or `It is well known that` unless the sentence quickly becomes specific.

## Verbs

Preferred author-action verbs:

- `developed`, `designed`, `engineered`, `incorporated`, `optimized`, `evaluated`, `investigated`, `validated`.

Preferred result verbs:

- `enabled`, `enhanced`, `improved`, `promoted`, `reduced`, `inhibited`, `induced`, `facilitated`, `revealed`, `confirmed`, `showed`, `demonstrated`.

Use `demonstrated` only for direct experimental evidence. Use `suggested`, `may`, `could`, or `potential` for inferred mechanisms and future applications.

Avoid vague verbs:

- `revolutionized`, `leveraged`, `utilized` when `used` is enough, `impacted`, `highlighted` without a clear object, `underscored` as filler.

## Modality and Hedging

- Keep hedging explicit and conservative.
- Use `may` and `could` for future applications, possible mechanisms, or translational implications.
- Use `suggesting` when the sentence links an observed result to an interpretation.
- Avoid strengthening `may improve` into `improves`, or `suggests` into `demonstrates`.
- Avoid empty certainty phrases such as `undoubtedly`, `clearly proves`, or `without question`.

## Connectors and Flow

Preferred flow markers:

- Contrast: `However`, `In contrast`, `Although`, `While`.
- Addition: `In addition`, `Furthermore`, `Moreover`.
- Purpose: `To address this`, `To further investigate`, `To evaluate`.
- Key observation: `Notably`, `Importantly`.
- Inference: `These results suggest`, `These findings indicate`, `This observation supports`.
- Synthesis: `Together`, `Overall`, `Collectively`.

Use connectors as logical hinges, not decoration. If two adjacent sentences both start with connectors, remove one.

## Noun Phrase Style

- Prefer compact technical noun phrases over explanatory padding.
- Put modifiers before the core noun when readable: `tissue-selective mRNA delivery`, `cell-type-specific expression`, `surface-engineered LNPs`.
- Avoid stacking more than three modifiers before a noun. If needed, split the phrase.
- Use abbreviations after first definition and then keep abbreviation use consistent.

## Paragraph Rhythm

Research paragraphs often work best as:

1. A concise topic or gap sentence.
2. One or two design or method sentences.
3. Two or three evidence sentences.
4. A final bounded inference sentence.

Review paragraphs often work best as:

1. A topic sentence defining the strategy or limitation.
2. A short taxonomy or example sequence.
3. A caveat or translational challenge.
4. A restrained forward-looking sentence.

## Anti-AI Rewriting Rules

- Replace abstract enthusiasm with observable action.
- Replace `plays a vital role in` with a specific verb whenever possible.
- Replace `has attracted increasing attention` with the reason it matters.
- Replace `shows great promise` with the exact application boundary.
- Remove repeated intensifiers such as `highly`, `remarkably`, `greatly`, and `significantly` unless supported by measured data.
- Prefer exact causal wording over decorative transitions.

## Practical Rewrite Template

For a manuscript paragraph, revise in this order:

1. Identify the main claim and keep it unchanged.
2. Make the sentence subject concrete.
3. Replace vague verbs with specific study or result verbs.
4. Keep hedging at the same strength.
5. Shorten overlong sentences into 18-30 word units.
6. Add a connector only where it clarifies logic.
7. End with a bounded implication rather than a broad claim.
