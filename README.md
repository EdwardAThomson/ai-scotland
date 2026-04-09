# Scotland's AI Strategy 2026-2031 - Review

A multi-LLM review and analysis of **Scotland's AI Strategy 2026-2031**, published by the Scottish Government on 20th March 2026.

Three LLMs (Claude 4.6 Opus, GPT 5.4, and Gemini 3.1 Pro) independently reviewed every section of the strategy using a shared methodology and checklist. The 63 resulting section-level reviews were then reconciled to identify where the reviewers agree, where they diverge, and what none of them caught. The goal was to stress-test the strategy's clarity, measurability, feasibility, and internal consistency.

## About the Strategy

The strategy sets out Scotland's ambition to harness AI responsibly for sustainable growth, stronger public services, and inclusive economic opportunity. It spans eight "AI Stack" layers -- from users and skills through to semiconductors and regulation -- with outcomes targeting 2031.

## Key Findings

The reconciliation identified **17 consensus findings** where all three reviewers independently agreed. The strongest signals:

- The strategy has **no measurable targets** -- outcomes have no baselines, metrics, or success criteria
- **No budgets** are attached to any action across the entire strategy
- Actions predominantly **create structures** (panels, boards, pilots) rather than committing to tangible deliverables
- The **Case for Change** is the strongest, most analytically honest section
- The **Semiconductors** layer has the best strategic thinking, with a realistic niche focus
- **Fair Work** is rhetorically central but operationally absent from governance and delivery

See [review-reconciliation/summary.md](review-reconciliation/summary.md) for the full reconciliation, or dive into the individual files for detail.

## Review Approach

1. **Extract** -- Split the 58-page PDF into 21 markdown files for structured analysis
2. **Review** -- Each section independently reviewed by Claude, Gemini, and GPT using the same methodology and checklist
3. **Reconcile** -- Cross-reference all 63 section reviews to identify consensus, unique findings, disagreements, and meta-gaps
4. **Share** -- Publish findings

![AI Strategy 2026-2031](ai_scotland_banner.png)


## Repository Structure

```
source/
  ai-strategy-scotland.pdf    # Original strategy document
  markdown/                    # Strategy split into markdown sections
    00-contents.md             # Table of contents
    01-foreword.md             # Foreword by Kate Forbes MSP
    02-introduction.md         # Introduction
    03-foundations.md           # Foundations
    04-case-for-change.md      # Case for Change
    05-purpose-and-outcomes.md  # Purpose & Outcomes
    06-actions.md              # Actions
    07-ai-scotland.md          # AI Scotland
    08-ai-action-plan.md       # AI Action Plan
    09-layer1-users.md         # Layer 1 - Users
    10-layer2-adoption-and-skills.md
    11-layer3-companies-and-products.md
    12-layer4-innovation-research-and-development.md
    13-layer5-data-centres-and-infrastructure.md
    14-layer6-semiconductors.md
    15-layer7-data.md
    16-layer8-regulation.md
    17-risks-and-mitigations.md
    18-glossary.md
    19-acknowledgments.md
    20-endnotes.md
review-claude/                 # Claude review (21 section reviews + summary)
review-gemini/                 # Gemini review (21 section reviews + summary)
review-gpt/                    # GPT review (21 section reviews + findings summary)
review-reconciliation/         # Cross-review reconciliation
  00-methodology.md            # How the reconciliation was conducted
  01-consensus-findings.md     # 17 points where all 3 LLMs agree
  02-unique-findings.md        # 26 findings raised by only 1 or 2 reviewers
  03-disagreements.md          # 18 areas where reviewers diverge
  04-gap-analysis.md           # 10 themes none of the reviewers covered
  05-section-matrix.md         # Section-by-section comparison across all 21 sections
  summary.md                   # Overall reconciliation summary
review-checklist.md            # Progress tracker across all LLMs
review-methodology.md          # How each section should be reviewed
process.md                     # How the PDF-to-markdown conversion was done
plan.md                        # Review plan
```
