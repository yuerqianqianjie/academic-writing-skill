# Validation Cases and Results

These are synthetic test cases for the Skill workflow. They are not additional source material and must not be treated as facts or citations.

## Case 1 — Introduction routing

**Input**

> Collaborative robots are increasingly used in manufacturing. Previous studies have examined collision avoidance, but few studies have investigated how operators adapt their trust after repeated near-miss events. This study examines whether feedback timing affects trust calibration.

**Expected behavior and observed result**

- Route: `introduction.md` + `academic-argumentation.md`.
- The section is correctly identified as general → prior work/gap → present study.
- The gap is plausible but should be checked against the cited literature; no citation is invented.
- `trust calibration` and `feedback timing` are preserved; the current study's question is not inflated into a causal claim beyond the supplied wording.

## Case 2 — Literature Review synthesis and gap

**Input**

> Smith (2020) studied sensor fusion in mobile robots. Lee (2021) studied sensor fusion in mobile robots. Kumar (2022) studied sensor fusion in mobile robots. These studies are important. Therefore, sensor fusion is well understood.

**Expected behavior and observed result**

- Route: `literature-review.md` + `academic-argumentation.md`.
- The Skill identifies citation listing without comparison, evaluation, or synthesis.
- It flags that “well understood” is unsupported because the studies' findings, methods, limitations, and scope are not stated.
- It requests the missing comparison/gap evidence rather than fabricating a gap or rewriting the paragraph into a stronger claim.

## Case 3 — Methods reproducibility

**Input**

> We tested the system in the laboratory. The data were processed and the results were analyzed. The method was effective.

**Expected behavior and observed result**

- Route: `methodology.md` + `revision.md` + `academic-argumentation.md` for the unsupported evaluation claim.
- The Skill checks the three Methods questions and identifies missing subjects/materials, procedure, analysis method, and criteria for “effective”; it asks for location/context details if they are needed for interpretation or replication.
- It distinguishes a reproducibility/content problem from grammar; the sentences are grammatically acceptable.
- It does not invent instruments, sample sizes, software, statistics, or performance values.

## Case 4 — Discussion: summary versus interpretation and implication

**Input**

> The intervention group had a higher score than the control group. The difference was statistically significant. The intervention group therefore benefits from the intervention in all educational settings.

**Expected behavior and observed result**

- Route: `discussion.md` + `academic-argumentation.md` + `academic-stance.md`.
- The first two sentences are result summary; the final sentence is a broad implication/causal generalization.
- The Skill flags missing interpretation, scope, evidence for transfer to all settings, and possible overclaiming. It may suggest a qualified placeholder such as `[specify the tested setting and evidence for generalization]`.
- It does not convert the result into a universal claim.

## Case 5 — Grammar problem with sound logic

**Input**

> The results indicates that the treatment reduce error rates, although this effect was observed only in the high-noise condition.

**Expected behavior and observed result**

- Route: `revision.md` + `academic-stance.md`.
- The Skill makes minimal grammar corrections: `results indicate` and `treatment reduces` (or preserves a past-tense framing consistently).
- It preserves the important limitation `only in the high-noise condition` and does not add explanation or stronger claims.
- It reports that the logic is otherwise coherent rather than over-rewriting the sentence.

## Case 6 — Fluent language with weak argumentation

**Input**

> The present study provides definitive evidence that the algorithm will improve healthcare outcomes. The conclusion follows from our benchmark accuracy, which exceeded the baseline by 2%.

**Expected behavior and observed result**

- Route: `academic-argumentation.md` + `academic-stance.md` + `revision.md`.
- The Skill detects an argumentation/evidence problem despite fluent grammar: benchmark accuracy does not by itself establish healthcare-outcome improvement or future certainty.
- It recommends narrowing the claim to the tested benchmark or adding the missing clinical evidence, and it preserves the 2% value.
- It does not treat “definitive” or “will improve” as merely stylistic choices.

## Validation summary

All six cases satisfy the intended invariants: section-specific routing occurs before language editing; synthesis, reproducibility, Results–Discussion boundaries, and overclaiming are diagnosed; a grammar-only case receives a restrained edit; and no references, data, methods, or results are invented.
