---
name: academic-writing
description: "Analyze, teach, diagnose, revise, and proofread English academic papers by section, using source-grounded rhetorical, argumentation, coherence, stance, and language guidance."
---

# Academic Writing Skill

Use this skill when the user is working on an English academic paper or research article and asks to draft, outline, explain, diagnose, revise, rewrite, compare, or proofread a title, abstract, Introduction, Literature Review, Methods/Methodology, Results, Discussion, Conclusion, paragraph, argument, citation integration, cohesion, stance, hedging, or academic language.

This is an instruction and workflow skill, not a fixed-template writing manual. Its primary knowledge base is the source-derived material in `references/`. Load only the references needed for the current task.

## Source priority and provenance

Apply guidance in this order:

1. The user's manuscript, target journal instructions, supplied examples, and explicit constraints.
2. The relevant source-derived references in this skill.
3. The workflow and safeguards in this file.
4. General model knowledge, only when the sources and user materials do not decide the issue.

Do not invent references, evidence, results, methods, journal rules, or disciplinary conventions. When the source material is ambiguous or gives competing recommendations, preserve the alternatives and label them as source-specific. Prefer the target journal or supplied exemplar when available. Otherwise explain the choice or present alternatives rather than silently merging them. See [source-map.md](references/source-map.md).

## Routing: task to references

| User task | Read first | Add when relevant |
|---|---|---|
| Write or revise an Introduction | [introduction.md](references/introduction.md) | `academic-argumentation.md`, `cohesion-coherence.md`, `academic-stance.md` |
| Write or revise a Literature Review | [literature-review.md](references/literature-review.md) | `academic-argumentation.md`, `cohesion-coherence.md`, `academic-vocabulary.md` |
| Write or revise Methods/Methodology | [methodology.md](references/methodology.md) | `cohesion-coherence.md`, `revision.md`, `academic-argumentation.md` when a method choice or evaluation claim needs evidence |
| Interpret or write Results | [results.md](references/results.md) | `figures-tables.md`, `academic-stance.md`, `cohesion-coherence.md` |
| Write or revise Discussion | [discussion.md](references/discussion.md) | `academic-argumentation.md`, `academic-stance.md`, `cohesion-coherence.md`; add `results.md` when the passage mixes result reporting and interpretation |
| Write or revise Conclusion(s) | [conclusion.md](references/conclusion.md) | `discussion.md`, `academic-stance.md` |
| Write or revise an Abstract | [abstract.md](references/abstract.md) | `introduction.md`, `results.md`, `conclusion.md` |
| Improve claims, evidence, gaps, contribution, or reasoning | [academic-argumentation.md](references/academic-argumentation.md) | relevant section reference |
| Improve paragraph coherence or information flow | [cohesion-coherence.md](references/cohesion-coherence.md) | relevant section reference |
| Improve stance, certainty, or hedging | [academic-stance.md](references/academic-stance.md) | `discussion.md`, relevant section reference |
| Improve vocabulary, reporting verbs, or phraseology | [academic-vocabulary.md](references/academic-vocabulary.md) | relevant section reference |
| Revise the whole paper or several sections | [revision.md](references/revision.md) | all and only the section references involved |
| Revise figures, tables, captions, or legends | [figures-tables.md](references/figures-tables.md) | `results.md`, target-journal guidance |
| Explain source conflicts or choose between traditions | [source-map.md](references/source-map.md) | relevant section reference |

If a request spans sections, load multiple references. For example, an Abstract based on a paper's findings uses `abstract.md`, `results.md`, and `conclusion.md`; a Discussion that compares prior work uses `discussion.md`, `literature-review.md`, and `academic-argumentation.md`.

## Identify the section and task type

First determine:

- **Section:** use an explicit heading if supplied; otherwise infer from rhetorical purpose and state the assumption briefly. A paragraph can contain moves from more than one section; diagnose the mismatch instead of forcing a label.
- **Task type:** `explain`, `teach`, `diagnose`, `revise`, `rewrite`, `proofread`, `outline`, `generate`, or `compare`.
- **Scope:** sentence, paragraph, subsection, section, whole paper, target journal, discipline, and requested degree of intervention.

Task type controls the response:

| Task type | Default response |
|---|---|
| Explain / teach | Explain the relevant rhetorical function, checks, and source-grounded alternatives; do not silently rewrite the user's text. |
| Diagnose | Identify the problem, why it matters, its level, and a targeted remedy; rewrite only a short example when it clarifies the diagnosis. |
| Revise / rewrite | Give the revised version first, then briefly explain substantive changes and any unresolved evidence or logic issue. |
| Proofread | Correct language only within scope; flag any logic, claim, evidence, or meaning risk instead of silently changing it. |
| Outline | Propose functions, moves, evidence needs, and information order; do not fill gaps with invented content. |
| Generate | Draft only from supplied facts, sources, results, and constraints; mark placeholders where information is missing. |
| Compare | Compare alternatives by rhetorical function, evidence, stance, coherence, discipline, and target-journal fit. |

## Core workflow: diagnose before polishing

Process the text in this order:

```text
Identify section and task
        ↓
Load only the relevant references
        ↓
Level 1: Content — relevance, claim, evidence, missing information
        ↓
Level 2: Argumentation — reasoning, claim–evidence relation, gap, contribution, interpretation
        ↓
Level 3: Organization — paragraph purpose, moves, information order, transitions
        ↓
Level 4: Academic discourse — stance, certainty, hedging, authorial focus, discipline-sensitive style
        ↓
Level 5: Language — grammar, vocabulary, collocation, sentence structure, concision
        ↓
Respond in the mode requested, preserving meaning
```

Do not lead with grammar correction when a content, argumentation, organization, or discourse problem affects the paper's meaning. A language-only request may stay at Level 5, but still flag a change that would alter a claim or implication.

For each important claim, check:

1. What is being claimed?
2. What evidence or cited source supports it?
3. What reasoning connects the evidence to the claim?
4. Is the certainty level warranted?
5. What does the claim do in this section: establish background, synthesize literature, state a gap, report a result, interpret a result, state a contribution, limit, implication, or recommendation?

When a gap, contribution, explanation, or implication is missing, say what information is needed. Do not manufacture it.

## Revision safeguards

- Preserve the author's academic meaning, technical distinctions, uncertainty, and reported results.
- Do not strengthen a tentative claim, broaden a population, add a causal interpretation, or convert association into causation without evidence.
- Do not add citations or references that the user did not provide.
- Do not change methods, numerical results, sample descriptions, or limitations for stylistic reasons.
- If the original logic is defective, show the problem explicitly; do not hide it behind fluent prose.
- Prefer the smallest change that solves the identified problem. Distinguish `grammar`, `style/readability`, `logic/coherence`, and `argumentation/evidence` in the diagnosis.
- Treat rhetorical moves as functions, not compulsory sentences. `Rhetorical function > fixed sentence template`.
- Treat source-derived phrases as optional linguistic realizations, not formulas that every paper must use.

## Discipline and journal sensitivity

Separate general academic-writing principles from discipline- or journal-specific conventions. If the discipline or target journal is missing, avoid making a field-specific rule sound universal. If it is supplied, use its terminology, section structure, reference style, word limits, figure/table rules, and level of accessibility as the controlling constraints, then use this skill to diagnose fit.

When sources disagree, report the disagreement with its scope. For example, a journal-specific rule can override a general source pattern, but it should not be generalized to all journals. Keep unresolved source ambiguities visible.

## Output quality check

Before answering, verify that:

- the response matches the user's task type;
- the section's rhetorical purpose is addressed;
- substantive claims are tied to supplied evidence or explicitly marked as missing;
- the information flow is clear;
- certainty and stance match the evidence;
- the revision does not change authorial meaning;
- journal/discipline rules are not presented as universal;
- language changes are proportionate to the request.

For multi-level revision, report the main issue first, then the revised text or actionable diagnosis, followed by only the explanations needed for the user's goal. Use the source map when a conflict, uncertain attribution, or incomplete source example affects the recommendation.

## Supporting references

- Section guidance: [introduction.md](references/introduction.md), [literature-review.md](references/literature-review.md), [methodology.md](references/methodology.md), [results.md](references/results.md), [discussion.md](references/discussion.md), [conclusion.md](references/conclusion.md), [abstract.md](references/abstract.md)
- Cross-section guidance: [academic-argumentation.md](references/academic-argumentation.md), [cohesion-coherence.md](references/cohesion-coherence.md), [academic-stance.md](references/academic-stance.md), [academic-vocabulary.md](references/academic-vocabulary.md), [revision.md](references/revision.md), [figures-tables.md](references/figures-tables.md)
- Provenance and conflicts: [source-map.md](references/source-map.md)
