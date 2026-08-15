# Bachelor Thesis — Cognitive RAG: Bloom's Taxonomy & DSRP Plugins for ComoRAG

## Overview

This project contains my original [thesis defense presentation](presentation.pdf).
*Development of RAG Architecture Based on Bloom's Taxonomy Principles for Context-Sensitive
Information Retrieval* — Danial Baitakov, Astana IT University, 2026.

The project extends [ComoRAG](https://github.com/EternityJune25/ComoRAG), a
cognitive-inspired memory-organized RAG system
([paper](https://arxiv.org/abs/2508.10419)), with two toggleable plugins:

- **Bloom Taxonomy Estimator** — classifies each query into one of six cognitive levels
  (Remember → Create) and scales retrieval parameters accordingly: up to 3× top-k and 5
  metacognitive loop iterations for high-complexity queries, instead of fixed parameters
  for every query.
- **DSRP Decomposer** — during indexing, annotates each memory chunk with four cognitive
  dimensions (Distinctions, Systems, Relationships, Perspectives), creating additional
  retrieval pathways for multi-hop questions.

On DetectiveQA the enhanced system improves accuracy from 18.0% to 24.0% (+6 pp, 50
samples; GPT-4.1-nano, text-embedding-3-large).
The full thesis text is available upon request.

## Datasets used

- [NarrativeQA](https://arxiv.org/abs/1712.07040) — QA over full-length books
- [DetectiveQA](https://arxiv.org/abs/2409.02465) — long-context reasoning over detective novels
- [InfiniteBench](https://arxiv.org/abs/2402.13718) — long-context benchmark (En.MC, En.QA tasks)

## License

[MIT](LICENSE). Built on top of [ComoRAG](https://github.com/EternityJune25/ComoRAG) (MIT).
