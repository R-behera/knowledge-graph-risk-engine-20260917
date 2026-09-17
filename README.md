# Knowledge Graph Risk Engine

An explainable knowledge-graph pipeline for entity links, relationship paths, and risk evidence.

Generated on 2026-09-17 as an independent production-AI architecture project.

## Real-World Problem

Risk teams need relationship-level explanations instead of opaque entity scores.

## Hugging Face Tasks

- `token-classification`
- `feature-extraction`
- `question-answering`
- `sentence-similarity`

## Recommended Production Stack

- FastAPI for entity and evidence APIs
- Neo4j Community or PostgreSQL recursive queries
- Sentence Transformers for entity resolution
- NetworkX for local graph validation
- Kafka-compatible event ingestion
- OpenTelemetry for lineage and query traces

## Included

- Runnable Python pipeline with no runtime dependencies
- Local JSON HTTP inference service
- Public-data API connector with explicit provenance
- Reproducible training script
- Held-out evaluation command
- Synthetic dataset with explicit provenance
- Trained transparent baseline model
- Architecture and production-boundary documentation
- Unit tests, CI workflow, and Dockerfile
- Hugging Face-ready model and dataset cards

## Architecture

1. Entity normalization
1. Relationship extraction
1. Adjacency graph construction
1. Path-based evidence search
1. Graph quality evaluation

See [ARCHITECTURE.md](ARCHITECTURE.md) for the full flow and production
boundaries.

## Quick Start

```bash
python3 -m unittest discover -s tests
PYTHONPATH=src python3 -m knowledge_graph_risk.cli "Who controls supplier alpha?"
PYTHONPATH=src python3 evaluate.py
PYTHONPATH=src python3 -m knowledge_graph_risk.service
```

The service exposes `GET /health` and `POST /predict`.

Rebuild the model:

```bash
python3 train.py
```

## Baseline Evaluation

- Held-out synthetic examples: 4
- Accuracy: 1
- Target metrics: relation_accuracy, path_coverage, entity_resolution_precision

This score verifies that the code and evaluation contract work. It does not
claim production performance.

## Hugging Face Artifacts

When the controller has a Hugging Face token and namespace configured, it
publishes:

- Dataset: `knowledge-graph-risk-engine-20260917-dataset`
- Model: `knowledge-graph-risk-engine-20260917-model`

## Portfolio Value

This repository maps to production AI engineering work in:

- Entity resolution and relation extraction
- Knowledge-graph modeling and path queries
- Graph-based explainability and provenance
- Streaming ingestion and schema evolution
- Risk-model evaluation and data quality controls

See [PORTFOLIO.md](PORTFOLIO.md) for resume-ready impact targets and interview
discussion areas.

## 1-3 Month Expansion

Follow [ROADMAP.md](ROADMAP.md) to add real-world APIs, a stronger open model,
durable orchestration, evaluation, observability, scalability testing, and a
public deployment.

## Safety

All entities are fictional. Real identity or financial data requires governance, consent, and bias review.

Review [ARCHITECTURE.md](ARCHITECTURE.md),
[PRODUCTION.md](PRODUCTION.md), [SECURITY.md](SECURITY.md),
[MODEL_CARD.md](MODEL_CARD.md), and [DATASET_CARD.md](DATASET_CARD.md) before
adapting this project.
