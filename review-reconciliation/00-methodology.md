# Reconciliation Methodology

## Purpose

This reconciliation compares the findings of three independent LLM reviews of Scotland's AI Strategy 2026-2031 to identify:

1. **Consensus** -- where all three reviewers agree (strongest signal)
2. **Unique findings** -- points raised by only one or two reviewers
3. **Disagreements** -- areas where reviewers contradict each other
4. **Meta-gaps** -- themes or issues none of them covered
5. **Section-level patterns** -- how assessments compare across the document's structure

## Reviewers

| Reviewer | Model | Review approach |
|----------|-------|-----------------|
| Claude | Claude (Anthropic) | Section-by-section analysis using a structured checklist covering clarity, measurability, gaps, feasibility, and internal consistency. Produced 21 section reviews + summary. |
| GPT | GPT (OpenAI) | Section-by-section analysis using the same methodology and checklist. Produced 21 section reviews + findings summary. |
| Gemini | Gemini (Google) | Section-by-section analysis using the same methodology and checklist. Produced 21 section reviews + summary. |

## Shared methodology

All three reviewers used the same:
- **Source material**: 21 markdown files extracted from the PDF in `source/markdown/`
- **Review checklist**: `review-checklist.md` (clarity, measurability, gaps, feasibility, consistency)
- **Review methodology**: `review-methodology.md`

## Reconciliation process

The reconciliation was conducted by Claude (Opus 4.6) reading all 63 section-level reviews and 3 summaries to identify patterns of agreement, divergence, and omission across reviewers.

### What counts as consensus
A finding is treated as consensus when all three reviewers independently identified the same concern or strength, even if they framed it differently. The threshold is substantive agreement on the point, not identical wording.

### What counts as a unique finding
A finding is unique when only one or two reviewers raised it. This includes both genuinely missed points and cases where a reviewer went deeper on a topic others only touched on.

### What counts as a disagreement
A disagreement requires reviewers to reach opposing or meaningfully different conclusions about the same aspect of the strategy. Different emphasis alone does not qualify -- the assessments must be in tension.

## Output files

| File | Contents |
|------|----------|
| `01-consensus-findings.md` | Points where all 3 reviewers agree |
| `02-unique-findings.md` | Points raised by only 1 or 2 reviewers |
| `03-disagreements.md` | Areas of contradiction between reviewers |
| `04-gap-analysis.md` | Themes none of the reviewers covered |
| `05-section-matrix.md` | Section-by-section comparison table |
| `summary.md` | Overall reconciliation summary |
