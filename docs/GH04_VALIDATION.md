> **Portfolio note:** Commands and modules mentioned below refer to the restricted internal project; they are not executable from this documentation-only repository. Historical results are not a public CI claim.

# GH.04 — Offline integration validation

## Commands (existing Python environment with numpy and pytest)

```bash
PYTHONPATH=src python -m pytest -q
python examples/run_demo.py
```

The demo exercises `run_pipeline` and `HybridRetriever.search` with deterministic, in-memory adapters. The sparse adapter is term overlap, **not BM25**. The dense adapter uses hashed token vectors and an in-memory cosine similarity collection, **not SentenceTransformer or ChromaDB**. It does not generate answers. Two synthetic questions are evaluated; Hit@1 on two examples is not a representative retrieval benchmark.

## Installation limitation

An isolated Python virtual environment was created, but installing build dependencies failed because the execution environment could not resolve the Python package index. A second environment using system site-packages failed to import the `setuptools.build_meta` backend when attempting editable installation. Therefore `pip install -e .` in a clean environment is **not verified**. Existing dependencies were used to run the integration demo and regression tests. No release approval is implied.

## Known issue

The GH.02 English questions were routed to `REVIEW_REQUIRED` and no retrieval occurred. GH.04 uses Polish questions that match the current routing policy. English routing remains an unresolved product limitation.

## Provenance

Original 12 application modules and 6 test modules are unchanged from GH.02. This package adds `examples/run_demo.py`, updates demo questions and documentation. Original recovery checkpoint and GH.02 ZIP are unchanged.
