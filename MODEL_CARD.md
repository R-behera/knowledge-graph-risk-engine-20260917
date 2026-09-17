---
license: mit
library_name: custom
pipeline_tag: feature-extraction
datasets:
- {{HF_NAMESPACE}}/knowledge-graph-risk-engine-20260917-dataset
tags:
- synthetic-data
- transparent-baseline
- knowledge-graphs
- token-classification
- feature-extraction
- question-answering
- sentence-similarity
metrics:
- accuracy
---

# Knowledge Graph Risk Engine Baseline Model

## Model Description

This repository contains a small, transparent prototype model for
**Risk teams need relationship-level explanations instead of opaque entity scores.**

The model combines per-label token weights with IDF-weighted evidence
retrieval. It was generated for reproducible architecture demonstrations and
does not call a hosted LLM.

## Evaluation

- Held-out synthetic examples: 4
- Accuracy: 1
- Intended metrics: relation_accuracy, path_coverage, entity_resolution_precision

## Intended Use

- Architecture prototyping
- CI and evaluation examples
- Local baseline comparisons
- Educational experimentation

## Hugging Face Task Coverage

- `token-classification`
- `feature-extraction`
- `question-answering`
- `sentence-similarity`

## Limitations and Risks

All entities are fictional. Real identity or financial data requires governance, consent, and bias review.

The dataset is synthetic and small. Do not use this model for consequential
decisions without representative data, expert review, and production-grade
evaluation.

## Reproducibility

The linked GitHub repository includes `train.py`, the exact dataset split,
evaluation code, and the model JSON format.
