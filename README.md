# Sentiment Annotation Pilot

A small annotation pilot project demonstrating end-to-end annotation work: task setup, guideline writing, execution, and documentation.

30 short texts annotated for sentiment (positive / negative / neutral) using a structured spreadsheet workflow, with a documented annotation guideline including label definitions, decision rules, and edge cases encountered during the pass.

---

## Project Summary

| Field | Value |
|-------|-------|
| Task | Single-label sentiment classification |
| Labels | positive, negative, neutral |
| Sample size | 30 examples |
| Tool | Google Sheets with validated label dropdowns |
| Annotator | Single annotator |

---

## Repository Contents

- `README.md` - This file
- `annotation_guidelines.md` - Full annotation guideline document with label definitions, decision rules, and 5 documented edge cases
- `sentiment_annotations.csv` - 30 annotated examples with labels and annotator notes

---

## Methodology

1. **Task definition:** Defined a 3-class sentiment classification task (positive, negative, neutral) appropriate for a small pilot.
2. **Guideline development:** Drafted the annotation guideline before starting, then refined the edge case section based on patterns seen during annotation.
3. **Execution:** Annotated 30 examples in a single pass, logging borderline cases inline in a notes column.
4. **Review:** Single end-to-end review pass to catch label drift and inconsistencies.

---

## Reproducibility

To reproduce this work:

1. Create a Google Sheet with columns: `id`, `text`, `label`, `notes`
2. Add data validation on the `label` column with three options: `positive`, `negative`, `neutral`
3. Paste in your source examples
4. Annotate each row, using the `notes` column for borderline cases
5. Follow the rules in `annotation_guidelines.md` for label decisions
6. Export the sheet as CSV when complete

---

## What This Project Demonstrates

- End-to-end annotation task design at small scale
- Writing decision-ready annotation guidelines with documented edge cases
- Application of rubric-based labeling with consistent rule application
- Quality process discipline (single-pass annotation with consistency review)

---

## Contact

[Your Name] | [Email] | [LinkedIn]
