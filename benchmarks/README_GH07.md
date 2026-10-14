# GH.07 — Expanded Synthetic Benchmark (internal project)

The full internal project defines a retrieval benchmark with 36 questions against 12 fictional manual sections. Its implementation uses BM25Okapi, ChromaDB, SentenceTransformer and reciprocal rank fusion (RRF) with routing/safety checks.

**The GH.07 benchmark runner and the full retrieval engine are not distributed in this public portfolio.** The scenario file `public/gh07_cases.json` is provided for inspection, not as an independently executable test suite. The internal runner's report schema covers Hit@1, Hit@3, MRR, routing coverage and per-question latency; execution success alone is not a retrieval-quality acceptance criterion.

The questions explicitly reference section identifiers, so the dataset is not a realistic blind evaluation. This stage does not itself establish LLM answer quality, industrial safety, or production readiness.

For the distinct GH07H semantic-verification experiment, see `public/gh07h_report.json` and `../docs/VALIDATION_STATUS.md`. GH07H reports 24 challenge cases and must not be confused with the 36-question GH.07 retrieval dataset.
