# Academic Writing Skill

`academic-writing` is a source-grounded Codex skill for English academic-paper writing. It helps analyze, teach, diagnose, revise, rewrite, outline, compare, and proofread papers while preserving the author's claims, evidence, results, and level of certainty.

## What it covers

- Introduction
- Literature Review
- Methodology / Methods
- Results
- Discussion
- Conclusion(s)
- Abstract
- Academic argumentation
- Cohesion, coherence, and information flow
- Academic stance and hedging
- Academic vocabulary and phraseology
- Figures, tables, captions, and legends
- Revision and proofreading

The skill treats rhetorical function as more important than fixed sentence templates. Its default review order is:

```text
Content → Argumentation → Organization → Academic discourse → Language
```

## Installation

Copy this directory to the Codex skills directory:

```text
$CODEX_HOME/skills/academic-writing
```

On a default Windows Codex installation, this is usually:

```text
C:\Users\<your-user>\.codex\skills\academic-writing
```

Then invoke it explicitly:

```text
Use $academic-writing to revise this Introduction while preserving the claims and evidence.
```

It may also be selected automatically for relevant academic-writing tasks.

## Repository layout

```text
academic-writing/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── section guidance
│   ├── cross-section argumentation and discourse guidance
│   ├── figures/tables guidance
│   ├── revision workflow
│   └── source map and variation protocol
└── examples/validation.md
```

`SKILL.md` contains routing, task-type detection, the five-level workflow, discipline/journal sensitivity, and safeguards against changing authorial meaning. Detailed guidance is loaded from `references/` only when relevant.

## Source basis

The reference files were synthesized from the user's Markdown knowledge base covering Introduction, Literature Review, Methodology, Results, Discussion, Readability, Captions/Legends, and Abstract materials. The source map records overlaps, source-specific rules, unresolved wording, and differences among journals.

No external references or invented journal requirements are included. Source-specific rules remain scoped to their named journal or publication context.

## Validation

The package includes six synthetic validation cases covering:

1. Introduction routing;
2. Literature Review synthesis and research gap;
3. Methods reproducibility;
4. Discussion interpretation and implication;
5. minimal correction of a grammar-only problem; and
6. detection of fluent but unsupported argumentation.

The package has been checked for valid skill metadata, resolved local Markdown links, and the safeguards described above.

## License status

No license is included yet. The package contains guidance synthesized from user-provided materials that may include book- or publisher-derived content. A public license should be added only after the rights holder and intended reuse conditions are confirmed.

