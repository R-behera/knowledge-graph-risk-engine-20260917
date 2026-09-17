---
license: cc-by-4.0
language:
- en
pretty_name: Knowledge Graph Risk Engine Synthetic Evaluation Set
size_categories:
- n<1K
task_categories:
- feature-extraction
tags:
- synthetic
- knowledge-graphs
- evaluation
- token-classification
- feature-extraction
- question-answering
- sentence-similarity
configs:
- config_name: default
  data_files:
  - split: train
    path: data/train.jsonl
  - split: test
    path: data/test.jsonl
---

# Knowledge Graph Risk Engine Synthetic Dataset

## Summary

This dataset contains 14 training examples and 4
held-out examples for **Risk teams need relationship-level explanations instead of opaque entity scores.**

Every record is synthetic and includes:

- `input`: query, event, or feature description
- `label`: expected class, route, relation, or evidence category
- `context`: synthetic supporting context
- `source`: fictional source identifier
- `variant`: generation pattern
- `synthetic`: always `true`

## Uses

- Reproducible unit and integration tests
- Baseline model training
- Evaluation harness development
- Schema and architecture demonstrations

## Limitations

All entities are fictional. Real identity or financial data requires governance, consent, and bias review.

This dataset does not represent real users, patients, customers, production
traffic, or licensed media. It must not be presented as real-world evidence.

## Related Model

[{{HF_NAMESPACE}}/knowledge-graph-risk-engine-20260917-model](https://huggingface.co/{{HF_NAMESPACE}}/knowledge-graph-risk-engine-20260917-model)
