# Process: PDF to Markdown Conversion

## Overview

This document describes the process used to convert the Scottish Government's AI Strategy PDF (58 pages, 3.8MB) into structured markdown files for review and analysis.

## Source

- **Document**: Scotland's AI Strategy 2026-2031
- **File**: `source/ai-strategy-scotland.pdf`
- **Published**: 20th March 2026 by the Scottish Government
- **Pages**: 58
- **Output**: 21 markdown files in `source/markdown/`

## Method

### Step 1: Read the PDF in batches

The PDF was too large to read in a single pass. The Read tool renders PDF pages as images and has a maximum of 20 pages per request. The document was read in three batches:

| Batch | Pages | Purpose |
|-------|-------|---------|
| 1 | 1-20 | Cover, contents, foreword, introduction, foundations, case for change, purpose, actions, AI Scotland, AI Action Plan |
| 2 | 21-40 | AI Stack layers 1-5 (Users through Data Centres & Infrastructure) with case studies |
| 3 | 41-58 | AI Stack layers 6-8 (Semiconductors, Data, Regulation), risks, glossary, acknowledgments, endnotes |

### Step 2: Identify the document structure

Page 2 contained a table of contents with section titles and page numbers. This provided the natural split points for individual markdown files. The structure follows the PDF's own organisation:

- Front matter (foreword, introduction)
- Foundations (pioneers, research, energy, business, investment, public services, sectors)
- Strategic framing (case for change, purpose & outcomes, actions)
- AI Scotland programme
- AI Action Plan with 8 "layers" of the AI Stack
- Risks and mitigations
- Back matter (glossary, acknowledgments, endnotes)

### Step 3: Transcribe content from page images

Each page was rendered as an image by the Read tool. The content was read visually (as a multimodal LLM) and transcribed into markdown. This included:

- **Body text** -- converted to plain paragraphs
- **Headings** -- mapped to markdown heading levels (`#`, `##`, `###`)
- **Bold/italic text** -- preserved with `**bold**` and `*italic*` syntax
- **Bullet lists** -- converted to markdown list syntax
- **Numbered lists** -- converted to ordered markdown lists
- **Tables** -- converted to markdown table syntax (e.g. the risks/mitigations table, outcomes tables)
- **Callout boxes** -- converted to subsections or block content (e.g. university profiles, key investments)
- **Case studies** -- included inline within their parent layer file
- **Quotes** -- converted to markdown blockquotes (`>`)
- **Page references** -- noted in italics at the top of each file

### Step 4: Write markdown files

Files were written using a numbered naming convention (`00-contents.md` through `20-endnotes.md`) to preserve reading order. Independent files were written in parallel batches to speed up the process.

The contents file (`00-contents.md`) includes relative links to all other files.

## Limitations

| Limitation | Detail |
|------------|--------|
| **No images** | Photographs, logos, and decorative graphics from the PDF are not included in the markdown files. |
| **AI Stack diagrams** | The visual AI Stack diagrams that appear on each layer's page are described in text but not reproduced as images. |
| **Endnote hyperlinks** | The original PDF contained clickable hyperlinks in the endnotes. These are listed as plain text references in the markdown. |
| **Layout nuance** | Two-column layouts in the PDF have been linearised into single-column markdown. The reading order follows left column then right column. |
| **OCR accuracy** | There was no OCR step. Content was read visually from rendered page images by a multimodal LLM. Minor transcription errors are possible, particularly for footnote superscript numbers. |

## Output

21 files in `source/markdown/`:

```
00-contents.md          - Table of contents with links
01-foreword.md          - Foreword (pages 3)
02-introduction.md      - Introduction (pages 4-5)
03-foundations.md       - Foundations (pages 6-13)
04-case-for-change.md   - Case for Change (pages 14-15)
05-purpose-and-outcomes.md - Purpose & Outcomes (page 16)
06-actions.md           - 10 Key Actions (page 17)
07-ai-scotland.md       - AI Scotland programme (pages 18-19)
08-ai-action-plan.md    - AI Action Plan & AI Stack (pages 20-21)
09-layer1-users.md      - Layer 1: Users (pages 22-24)
10-layer2-adoption-and-skills.md - Layer 2: Adoption & Skills (pages 25-29)
11-layer3-companies-and-products.md - Layer 3: Companies & Products (pages 30-32)
12-layer4-innovation-research-and-development.md - Layer 4: Innovation & R&D (pages 33-35)
13-layer5-data-centres-and-infrastructure.md - Layer 5: Data Centres (pages 36-40)
14-layer6-semiconductors.md - Layer 6: Semiconductors (pages 41-43)
15-layer7-data.md       - Layer 7: Data (pages 44-46)
16-layer8-regulation.md - Layer 8: Regulation (pages 47-49)
17-risks-and-mitigations.md - Risks & Mitigations (pages 50-51)
18-glossary.md          - Glossary of Terms (pages 52-53)
19-acknowledgments.md   - Acknowledgments (page 54)
20-endnotes.md          - Endnotes (pages 55-56)
```

## Tools Used

- **Claude Code** (Claude Opus 4.6) -- multimodal LLM used to read page images and transcribe to markdown
- **Read tool** -- rendered PDF pages as images for visual reading
- **Write tool** -- created the markdown files
- **Glob tool** -- verified output files were created correctly
