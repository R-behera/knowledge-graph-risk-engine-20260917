# Portfolio and Career Mapping

## Project Pitch

**Knowledge Graph Risk Engine** solves this real-world problem:

Risk teams need relationship-level explanations instead of opaque entity scores.

It combines `token-classification`, `feature-extraction`, `question-answering`, `sentence-similarity` with data ingestion, evaluation, observability, and scalable
service design.

## Why This Is More Than an API Wrapper

- Owns ingestion, validation, model artifacts, and evaluation datasets.
- Exposes evidence and confidence instead of returning opaque text.
- Includes offline evaluation and a CI release gate.
- Defines tracing, rollback, human review, and failure recovery.
- Provides a realistic path from free local baseline to production stack.

## AI Engineering Job Description Mapping

- Entity resolution and relation extraction
- Knowledge-graph modeling and path queries
- Graph-based explainability and provenance
- Streaming ingestion and schema evolution
- Risk-model evaluation and data quality controls

## Resume-Ready Impact Targets

Replace targets with measured results after completing the roadmap:

- Reach entity-resolution precision >= 0.95 on reviewed pairs
- Return evidence paths for 100% of emitted risk flags
- Process 10,000 relationship events per minute in load tests
- Detect schema and orphan-node regressions in CI

Example resume format:

> Built Knowledge Graph Risk Engine, a production-oriented knowledge-graphs system
> using FastAPI for entity and evidence APIs, Neo4j Community or PostgreSQL recursive queries, Sentence Transformers for entity resolution; measured
> relation_accuracy, path_coverage, entity_resolution_precision and
> enforced regression thresholds in CI.

## Interview Discussion Areas

- Why this architecture fits the problem and where it fails
- Retrieval/model choice and baseline comparisons
- Evaluation-set construction and metric trade-offs
- Data privacy, authorization, and human escalation
- Scaling, caching, index tuning, and failure recovery
- Model, prompt, dataset, and deployment lineage
