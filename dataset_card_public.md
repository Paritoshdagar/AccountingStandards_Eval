# Public Evaluation Dataset Card

Release date: **2026-02-17**

## Overview
This package contains a public gold evaluation dataset for ambiguous accounting and audit questions, with expected outcomes for grounding and clarification behaviour.

## Included Files
- `evaluation_dataset_public.json`
- `evaluation_dataset_public.csv`
- `evaluation_summary_public.json`
- `dataset_card_public.md`
- `linkedin_post_template.txt`

## Dataset Composition
| Metric | Value |
|---|---:|
| Total cases | 5,680 |
| Expected READY | 2,840 |
| Expected NEEDS_CLARIFICATION | 2,840 |
| Distinct standard labels | 90 |

Top standard labels by count:

| Standard | Cases | Share |
|---|---:|---:|
| Professional Auditing Standards (General) | 2,910 | 51.2% |
| FRS 102 | 340 | 6.0% |
| FRS 101 | 250 | 4.4% |
| FRS 105 | 120 | 2.1% |
| FRS 100 | 80 | 1.4% |
| FRS 103 | 80 | 1.4% |
| FRS 104 | 60 | 1.1% |
| ISA 220 | 60 | 1.1% |
| ISA 240 | 60 | 1.1% |
| ISA 260 | 50 | 0.9% |
| ISA 500 | 50 | 0.9% |
| ISA 505 | 50 | 0.9% |
| ISA 600 | 50 | 0.9% |
| ISA 200 | 40 | 0.7% |
| ISA 210 | 40 | 0.7% |
| ISA 230 | 40 | 0.7% |
| ISA 330 | 40 | 0.7% |
| ISA 450 | 40 | 0.7% |
| ISA 540 | 40 | 0.7% |
| ISA 570 | 40 | 0.7% |

## Schema
| Field | Description |
|---|---|
| `case_id` | Stable identifier for each evaluation case. |
| `standard_name` | Standard label associated with the question. |
| `question` | Ambiguous or edge-case audit/accounting question. |
| `expected_outcome` | Expected behavior (`READY` or `NEEDS_CLARIFICATION`). |
| `question_type` | Prompt pattern (`ready` or `clarification`). |
| `scenario` | Edge-case scenario tag. |

## NeuroSymbolicAI - Headline Evaluation Metrics
| Metric | Value |
|---|---:|
| Pass cases | 5,561 / 5,680 |
| Pass rate | 0.9790 |
| Soft pass rate | 0.9790 |
| Status match rate | 0.9790 |
| Clarification hit rate | 1.0000 |
| Citation validity rate | 1.0000 |
| Remaining failures | 119 |

Residual failure pattern:
- Expected READY, but the model requested clarification.

## Sample Questions
- `v3_edge_0001_01_ready_8a4c669fdb` | `Professional Auditing Standards (General)` | Under Professional Auditing Standards (General), management says the transaction is partly in scope and partly out of scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0001_11_clarification_e11a21b144` | `Professional Auditing Standards (General)` | In a cross-border restructuring, how should it apply when one contract is partly in scope, and what are its dependencies on other standards?
- `v3_edge_0006_01_ready_20a135e9a4` | `IFRS 4` | Under IFRS 4, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0007_01_ready_4494940e9c` | `IFRS 1` | Under IFRS 1, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0008_01_ready_f855912c6c` | `IFRS 10` | Under IFRS 10, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0009_01_ready_93493341fc` | `IFRS 11` | Under IFRS 11, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0010_01_ready_1164cd9ad9` | `IFRS 12` | Under IFRS 12, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0011_01_ready_79edccdb8c` | `IFRS 13` | Under IFRS 13, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0012_01_ready_1f8d214fcb` | `IFRS 14` | Under IFRS 14, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0013_01_ready_e66f4e4fff` | `IFRS 15` | Under IFRS 15, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0014_01_ready_04aba690ab` | `IFRS 16` | Under IFRS 16, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0015_01_ready_387546c194` | `IFRS 17` | Under IFRS 17, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0016_01_ready_edd30162e5` | `IFRS 2` | Under IFRS 2, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?
- `v3_edge_0017_01_ready_91eb3a01f6` | `IFRS 3` | Under IFRS 3, a transaction appears partially inside and partially outside scope. How should the boundary be determined, and what facts would change the conclusion?

## Privacy and Sanitisation
- Internal implementation details are intentionally excluded.
- Source-document identifiers are intentionally excluded.
- Internal storage paths are intentionally excluded.