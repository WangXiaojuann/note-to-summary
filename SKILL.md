---
name: note-to-summary
description: Write or revise an English, topic-level literature review from user-specified academic PDF files, Markdown notes, or both. Use when the task is to synthesize research questions, methods, structural differences, and limitations into one finance-journal-style review saved as a Markdown file.
metadata:
  short-description: Synthesize selected PDFs or Markdown notes into an English literature review
---

# Note To Summary

## Overview

Write a concise English literature review for one topic using the PDF files or Markdown notes specified by the user.
Produce a polished synthesis suitable for an academic introduction or literature review, not a paper-by-paper digest.
When both a note and its underlying PDF are supplied, use the PDF to resolve factual differences. A Markdown note can also serve as the sole source when no PDF is supplied.

## Workflow

### 1. Identify the sources, topic, and output file

- Use the PDF files or Markdown notes specified by the user. Do not assume a particular folder structure or expand the source set without reason.
- Use the topic and output path specified by the user. If no output path is given, save one `<topic>-literature-review.md` file in the working folder.
- If the topic is not named, infer it from the selected sources when clear; otherwise ask for clarification.
- Edit only the output file unless the user explicitly asks for more.

### 2. Build the source map

- Read each supplied Markdown note and PDF to identify paper names, core claims, topic fit, and likely strands of the literature.
- When both a note and its underlying PDF are supplied, compare them and trust the PDF on factual points.
- Do not require a matching PDF for a Markdown input or a matching note for a PDF input.
- If the supplied material is incomplete, proceed conservatively and mention the gap only when it materially affects the review.

### 3. Read the sources with synthesis in mind

- For each PDF, read the introduction and literature review sections first. Use the abstract, data, method, and conclusion sections to verify classification, identification strategy, or economic interpretation when needed.
- For each Markdown input, read the relevant note in full and keep claims within what that note supports.
- Extract only the information needed for synthesis:
  - the core research question
  - the main empirical or modeling approach
  - the paper's positioning within the literature
  - the mechanism or interpretation emphasized by the authors
- Capture relevant outside literature cited in the supplied sources when it materially sharpens the synthesis.
- Prefer outside citations that help explain the genealogy of the literature, a methodological fork, or a contested interpretation.
- Do not fabricate citations, years, or author names. If a citation is not clear enough, omit it.

### 4. Synthesize instead of describing

- When the sources support it, organize the literature around two to four research strands, tensions, or design choices.
- Compare papers systematically by research focus, data and measurement, identification design, and interpretation.
- Emphasize economic intuition and structural differences across papers.
- State what the literature has established, what remains unresolved, and where the main limitations lie.
- Do not write paper-by-paper mini summaries.
- Do not rely on abstract-like descriptions or phrases such as "This paper studies...".

### 5. Write or revise the literature review

- If the output file already exists and the user asks for revision, rewrite it where needed and make it strictly better than the original.
- Preserve useful existing structure when it works, but do not keep weak phrasing or clutter.
- Keep the result concise, readable, and publication-oriented.
- Use clean, portable Markdown formatting.
- Favor short connected paragraphs over heavy bulleting unless the content is inherently list-shaped.

### 6. Verify before finishing

- Confirm that only the target output file was edited.
- Check that citations and factual claims are supported by the supplied PDF or Markdown sources.
- Check that the output is a synthesis rather than a list of paper summaries.

## Output Format

Use a clean, readable layout like this by default. Keep the structure flexible: the headings are scaffolding, not a rigid outline. Combine or omit sections when the supplied sources do not support them.

```md
# Topic Title

One or two sentences that state the central synthesis.

## Core Questions

**First strand.** Explain the first major question or divide in the literature.
**Second strand.** Explain the second major question or divide when supported by the sources.

Short connected paragraphs group the literature into a few central questions.

## Methods and Evidence

Short connected paragraphs explain how different strands identify or model the question.

## Consensus and Disagreement

Short connected paragraphs compare results, interpretations, and mechanisms.

## Assessment and Open Questions

One or two sentences that state the contribution and the remaining gap.

- Compact bullets on established findings.
- Compact bullets on major limitations.
- Compact bullets on promising directions.
```

## Writing Rules

- Write in English.
- Use top-tier finance journal style: concise, precise, structured, and formal.
- Use established technical terms accurately and consistently.
- Avoid informal language, generic filler, and vague expressions.
- Write for academic reuse in introductions or literature review sections.
- Prefer depth and structure over exhaustive coverage.
- Keep the note shorter than a survey article and tighter than a classroom summary.
- Aim for a strong opening thesis, disciplined transitions, and a clear closing assessment.

## Citation Rules

- Use standard author-year citations, such as `(Mayew and Venkatachalam, 2012)`, when the supplied sources identify the authors and year clearly.
- Do not fabricate citations.
- Cite only when reasonably confident.
- Do not force citations into every sentence; cite where they support a structural claim, comparison, or genealogy of the literature.
- If a cited paper cannot be identified clearly from the supplied files, omit the citation. When working from a Markdown note alone, do not imply that its underlying paper was checked.

## Synthesis Rules

- Cover the core research questions by grouping the literature into meaningful categories when the supplied sources support them.
- Integrate methods with the research questions rather than mechanically separating them.
- Explain systematic differences across papers instead of listing them one by one.
- Organize around literature structure rather than source-file order or paper chronology, unless chronology itself is analytically important.
- Focus on structural differences in:
  - research focus
  - data and measurement
  - empirical design or modeling choice
  - interpretation of results
- Summarize both consensus and unresolved issues.
- Propose future directions when appropriate, especially for asset pricing, bond markets, textual analysis, macro-finance, or machine learning applications.
- Do not write one paragraph per paper.
- Do not let the summary become an annotated bibliography.

## Formatting Rules

- Use a `#` title and short `##` sections.
- Make the summary visually clean and publication-ready, with restrained but noticeable hierarchy.
- Open with a short paragraph stating the central synthesis.
- Use short paragraphs and compact flat bullets.
- Use bullets only where comparison is clearer in list form; otherwise prefer compact prose.
- Use bold micro-headings within paragraphs to improve scanability, especially for the main literature strands.
- Leave intentional blank lines between sections, paragraphs, and bullet groups.
- Prefer a small number of well-chosen visual devices over excessive decoration.
- Do not use emoji markers in topic summaries unless the user explicitly asks for them.
- If you use markers, do not output garbled, corrupted, or abnormal symbols. If marker rendering looks broken in the generated file, fix it before finishing.
- Keep spacing clean and visually balanced in Markdown.
- Do not create a long bibliography section unless the user explicitly asks for one.

## Editing Discipline

- Modify only the target output file unless the user explicitly asks for additional edits.
- If the user asks to revise an existing summary, make the revision strictly better than the original on accuracy, logic, and prose quality.
- If a factual point or citation is unclear, return to the supplied files and resolve it before writing. If the sources remain unclear, write conservatively.
- Never invent a literature consensus that is not supported by the source papers.
- When a supplied PDF and note cover the same paper, do not let an imprecise note override a clearer statement from the paper.
