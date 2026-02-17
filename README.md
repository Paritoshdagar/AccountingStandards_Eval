# Public Evaluation Dataset Release

This folder contains a sanitized public release of an evaluation dataset for ambiguous accounting and audit Q&A.

## Objective

The objective of this dataset is to measure whether a Q&A system makes the right decision **before** answering:

- Answer directly when there is enough context (`READY`).
- Ask for clarification when key context is missing (`NEEDS_CLARIFICATION`).

The dataset is designed to benchmark grounded-response quality, compare model or prompt versions, and detect regressions over time.

## What This Evaluates

Each case includes a question and an expected outcome. The core evaluation question is:

- Did the system correctly classify the question as `READY` or `NEEDS_CLARIFICATION`?

This helps evaluate practical reliability for real-world audit/accounting workflows where user questions are often incomplete or ambiguous.

## Intended Use

- Offline benchmark runs during model/prompt updates.
- Regression testing in CI before releasing changes.
- Comparative testing across multiple model configurations.

## Package Contents

- `evaluation_dataset_public.json`: Full dataset in JSON.
- `evaluation_dataset_public.csv`: Spreadsheet-friendly tabular format.
- `evaluation_summary_public.json`: Headline benchmark metrics.
- `dataset_card_public.md`: Human-readable dataset card with methodology and examples.

## Suggested Evaluation Flow

1. Run your system on all questions in `evaluation_dataset_public.json`.
2. Record predicted outcome (`READY` or `NEEDS_CLARIFICATION`) per case.
3. Compare predictions to `expected_outcome`.
4. Track pass rate and error patterns by standard, scenario, and question type.
