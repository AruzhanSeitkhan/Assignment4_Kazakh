
# Assignment 4 — Kazakh Question Answering

## Project Overview

This project compares question-answering performance on original Kazakh and machine-translated Kazakh datasets.

The experiments use 200 questions:
- 100 original Kazakh questions
- 100 machine-translated Kazakh questions

## Models

- Qwen/Qwen2.5-1.5B-Instruct
- deepset/xlm-roberta-large-squad2

Additional simple-span and TF-IDF retrieval baselines were evaluated.

## Evaluation Metrics

- Exact Match (EM)
- Token F1
- Exact McNemar test for paired model comparisons
- Paired bootstrap confidence intervals for F1 differences

## Main Results

| Model | Dataset | EM | Token F1 |
|---|---|---:|---:|
| Qwen2.5-1.5B | Original | 0.00 | 0.1187 |
| Qwen2.5-1.5B | Translated | 0.00 | 0.0705 |
| XLM-R-large | Original | 0.40 | 0.5611 |
| XLM-R-large | Translated | 0.30 | 0.4237 |

XLM-R achieved higher scores than Qwen on both evaluation groups.

## Repository Contents

- Assignment4_Kazakh_RMT.ipynb — experiment notebook
- selected.json — selected evaluation questions
- predictions.json — Qwen predictions
- xlmr_predictions.csv — XLM-R predictions
- baseline_predictions.csv — baseline predictions
- final_model_comparison.csv — final results
- final_statistical_comparison.csv — statistical comparisons
- final_qwen_vs_xlmr.png — model comparison figure
- subgroup_analysis.csv — subgroup analysis
- Assignment4_Error_Analysis_Preliminary.csv — preliminary error categorization

## Reproducibility

The experiment used random seed 42 and CPU inference.

Dataset: KazQAD
Dataset commit:
ab8684a667109f2a7345f4f89ab3b123e8d78e1f

The notebook contains the experiment code and analysis.
Some preparation cells depend on qa_compare.py and local input files. These dependencies must be provided before full reproduction.

The preliminary error analysis requires human verification.
