## Overview

This project contains my original [thesis defense presentation](presentation.pdf).
*Development of RAG Architecture Based on Bloom's Taxonomy Principles for Context-Sensitive
Information Retrieval* — Danial Baitakov, Astana IT University, 2026.

The project extends [ComoRAG](https://github.com/EternityJune25/ComoRAG), a
cognitive-inspired memory-organized RAG system
([paper](https://arxiv.org/abs/2508.10419)), with two toggleable plugins:

- **Bloom Taxonomy Estimator** — classifies each query into one of the six cognitive levels
  of [Bloom's Taxonomy](https://en.wikipedia.org/wiki/Bloom%27s_taxonomy)
  (Remember → Create) and scales retrieval parameters accordingly: up to 3× top-k and 5
  metacognitive loop iterations for high-complexity queries, instead of fixed parameters
  for every query.
- **DSRP Decomposer** — during indexing, annotates each memory chunk with the four patterns
  of [DSRP](https://en.wikipedia.org/wiki/DSRP) (Distinctions, Systems, Relationships,
  Perspectives), creating additional retrieval pathways for multi-hop questions.

On DetectiveQA the enhanced system improves accuracy from 18.0% to 24.0% (+6 pp, 50
samples; GPT-4.1-nano, text-embedding-3-large).

## Datasets used

- [NarrativeQA](https://arxiv.org/abs/1712.07040) — QA over full-length books
- [DetectiveQA](https://arxiv.org/abs/2409.02465) — long-context reasoning over detective novels
- [InfiniteBench](https://arxiv.org/abs/2402.13718) — long-context benchmark (En.MC, En.QA tasks)

## License

[MIT](LICENSE). Built on top of [ComoRAG](https://github.com/EternityJune25/ComoRAG) (MIT).

## Afterword

I'm looking to continue this research in a graduate lab working on
retrieval-augmented generation and long-context reasoning — if the work
is relevant to yours, I'd be happy to share the full thesis and discuss
it: [danialxbaitakov@gmail.com](mailto:danialxbaitakov@gmail.com)
