# Review Methodology

How each section of Scotland's AI Strategy 2026-2031 should be reviewed. All three LLMs (Claude, Gemini, GPT) follow the same structure so that reviews can be compared and reconciled.

## Review Structure

Each review file should follow this format:

### 1. Summary

A concise summary of the section in 2-3 sentences. What is this section about and what is it trying to achieve?

### 2. Key Points

A bullet list of the concrete commitments, claims, or arguments the section makes. Focus on what the government is committing to, not general scene-setting.

### 3. Observations

Critical analysis, organised under the following lenses as applicable:

- **Clarity** -- Flag anything vague, ambiguous, or that could be read multiple ways. Highlight jargon or language that obscures meaning.
- **Measurability** -- Are outcomes and targets specific enough to assess progress? Could the government claim success without meaningful change?
- **Gaps** -- What is missing? What does the section avoid addressing? Are there obvious questions left unanswered?
- **Feasibility** -- Are the proposed actions realistic given the timelines, resources, or powers available to the Scottish Government?
- **Internal consistency** -- Does this section align with other parts of the strategy? Do actions map to stated outcomes?

Not every lens will apply to every section. Only include those that are relevant.

## Scope

### Full review

Sections 01-17 should receive the full review treatment (summary, key points, observations).

### Light review

The following sections need only a brief note rather than the full structure, since they are reference material:

- `00-contents.md` -- Table of contents
- `18-glossary.md` -- Glossary of terms
- `19-acknowledgments.md` -- Acknowledgments
- `20-endnotes.md` -- Endnotes

For these, a short comment on anything notable (e.g. missing glossary terms, gaps in acknowledgments) is sufficient.

## File Naming

Review files should mirror the source file names and be saved in the corresponding LLM directory:

```
review-claude/01-foreword.md
review-gemini/01-foreword.md
review-gpt/01-foreword.md
```

## Tools

Reviews were conducted using IDE-integrated CLI tools within Windsurf:

- **Claude** (Claude 4.6 Opus) -- via the Claude Code (CC) extension
- **GPT** (GPT 5.4) -- via the Codex extension
- **Gemini** (Gemini 3.1 Pro) -- via the Antigravity extension

Each LLM reviewed the source material independently with no visibility of the other reviews. The reconciliation was performed by Claude Code.

## Tone

Reviews should be analytical and constructive. The goal is to understand the strategy's strengths and weaknesses, not to score political points. Where criticism is warranted, it should be specific and grounded in the text.
