Sentiment Annotation Pilot
A small annotation pilot project demonstrating end-to-end annotation work: task setup, guideline writing, execution, and documentation.
30 short texts annotated for sentiment (positive / negative / neutral) using Label Studio, with a documented annotation guideline including label definitions, decision rules, and edge cases encountered during the pass.
---
Project Summary
Field	Value
Task	Single-label sentiment classification
Labels	positive, negative, neutral
Sample size	30 examples
Source dataset	dair-ai/emotion (test split sample)
Tool	Label Studio (self-hosted)
Annotator	Single annotator
---
Repository Contents
`annotation_guidelines.md` - Full annotation guideline document
`sentiment_data.csv` - 30 unlabeled source examples
`annotations_export.json` - Exported annotations from Label Studio
`get_data.py` - Script to fetch source data
`screenshots/` - Label Studio interface screenshots
---
Methodology
Task definition: Collapsed the 6-class emotion taxonomy of the source dataset into 3 sentiment classes appropriate for a small pilot.
Guideline development: Drafted the annotation guideline before starting, then refined edge case section based on patterns seen during annotation.
Execution: Annotated 30 examples in a single pass, logging borderline cases inline.
Review: Single end-to-end review pass to catch label drift and inconsistencies.
---
Reproducibility
```bash
pip install label-studio datasets
python get_data.py
label-studio start
```
Then create a Label Studio project, import the CSV, configure text classification with the three labels above, and follow `annotation_guidelines.md`.
---
What This Project Demonstrates
End-to-end annotation task design at small scale
Writing decision-ready annotation guidelines with documented edge cases
Use of a production annotation tool (Label Studio)
Quality process discipline (single-pass annotation with consistency review)
---
Contact
[Abdul Rahman] | [Arikhan1224@gmail.com] | 
