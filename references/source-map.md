# Source Map, Classification, and Variation Protocol

## Source set inspected

The source directory supplied by the user was:

`E:\工作使我快乐\学为人师\2026秋\skill\knowledge`

It contains 62 Markdown files in eight folders. The files were read as a content set rather than classified only by filename. `processing_report.md` files were treated as provenance and quality-control records, not as independent writing rules.

## Content classification

| Source folder | Primary classification | Secondary/general content |
|---|---|---|
| `01_Introduction` (6 files) | Introduction moves, language functions, tense, Abstract distinction | Journal-specific variation |
| `02_Literature_Review` (8 files) | Literature Review purpose, synthesis, citation, tense, reporting verbs | Gap and discipline-sensitive style |
| `03_Methodology` (9 files) | Methods purpose, organization, clarity, tense/voice, research verbs | Reproducibility, equations, journal rules |
| `04_Results` (7 files) | Results organization, reporting/Discussion boundary, tense | Figures/tables and result language |
| `05_Discussion` (9 files) | Discussion, hedges, Conclusions, implications, limitations, future work | Abstract distinction and source variation |
| `06_Readability` (7 files) | General sentence construction, information flow, concision, ambiguity, precision | Language/proofreading support |
| `07_captions_and_legends` (9 files) | Figures, tables, captions, legends, visual conventions | Journal-specific visual rules |
| `08_Abstract` (7 files) | Abstract purpose, five-part structure, opening, tense | Journal limits and graphical Abstract |

The installed references are deliberate conceptual consolidations of these files. They retain source names, page ranges, source-specific examples, and unresolved ambiguities where those affect decisions.

## Overlapping content found

- **Introduction / Literature Review:** background, previous studies, research gap, present-study necessity, citation and tense. Route the rhetorical job: Introduction positions the whole paper; Literature Review synthesizes and evaluates prior work.
- **Introduction / Abstract:** purpose, methods, findings, and tense. The Abstract is self-contained and concise; the Introduction develops territory, literature, gap, and present work.
- **Results / Discussion:** reporting versus interpreting results, section arrangements, tense, and comparison. Keep the boundary visible even when a journal combines sections.
- **Discussion / Conclusion:** contributions, implications, limitations, and future research. Placement is an article-design choice in the supplied source.
- **Methods / Readability:** completeness, concision, clarity, logical order, sentence-step load, and passive/active information focus.
- **Results / Captions and Legends:** figure/table references and the requirement to describe relationships or key messages, not just name a visual.
- **Discussion / Academic stance:** hedges, certainty verbs, possible explanations, interpretations, and implications.
- **All sections / Readability:** word order, sentence length, redundancy, pronoun reference, precision, and grammatical signaling.

## Source differences and how the Skill handles them

| Issue | Difference preserved | Handling rule |
|---|---|---|
| Introduction literature coverage | IEEE includes literature positioning; Chinese Journal of Aeronautics avoids a detailed literature survey; Science Robotics emphasizes broad background and implications. | Follow the target journal; otherwise state the chosen balance. |
| Methods name and placement | `Methods`, `Methods and Materials`, `Experimental`, and other labels/placements are all recorded. | Do not normalize section names or placement without journal context. |
| Methods voice | Passive is presented as suitable, but active subjects are also listed. | Choose by information focus and clarity; no one-voice rule. |
| Methods/equations | Nature Communications, Advanced Materials, JMPS, and Science Advances give different limits and equation rules. | Keep rules attached to the named journal; never universalize. |
| Results/Discussion boundary | A separate Results section should avoid excessive interpretation, but “commenting on results” also appears as an optional move. | Interpret the move in light of separate versus combined sections and flag the source ambiguity. |
| Discussion/Conclusion placement | Contributions, limitations, and future work may be in Conclusions or in Discussion before a later Conclusion. | Follow article structure and journal requirements; avoid purposeless duplication. |
| Abstract rules | Nature allows/requires a referenced summary paragraph in the supplied excerpt; several other sources avoid references. Word limits and paragraph rules differ. | Use target-journal guidance; do not infer a universal limit. |
| Readability thresholds | The source gives around 25 words, avoid over 35, and about 30 as different checks; it also recommends both splitting and sometimes combining sentences. | Treat thresholds as warnings, not hard grammar rules; prioritize logic and clarity. |
| Figures/legends/tables | Science and Nature have different legend limits; table rules differ across named journals. | Keep every rule source-scoped. |
| Citation principle wording | “To cite friendly” appears without explanation. | Preserve the phrase as an unresolved source note; do not turn it into invented advice. |

## Conflict/variation protocol for the model

1. Identify whether the instruction is general, discipline-sensitive, target-journal-specific, or an example.
2. Prefer the user's current journal instructions and supplied examples.
3. If no controlling context exists, present the source-supported alternatives and explain the trade-off.
4. Keep the author's claims and evidence unchanged while choosing a wording or structure.
5. Never delete a conflicting source rule merely to make the Skill appear consistent.

## Processing-report status

The supplied processing reports state that the original PDFs were reviewed, source pages were retained, and no outside rules or unseen visual content were intentionally added. The Skill follows that provenance boundary. The cross-section workflow and safety constraints in `SKILL.md` are operational instructions requested by the user, not claims that they appeared verbatim in the source PDFs.
