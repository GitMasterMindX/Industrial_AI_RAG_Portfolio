> **Portfolio note:** Commands and modules mentioned below refer to the restricted internal project; they are not executable from this documentation-only repository. Historical results are not a public CI claim.

# GH.07B — Negative-case audit

Run `python benchmarks/run_gh07b.py`. This tests routing against 30 synthetic cases and six isolated structural-evidence cases. It reports mismatches without changing production policy. Audit success does not mean release approval. Current pipeline does not integrate the answerability gate; no semantic entailment or LLM answer safety is tested. Public release remains HOLD.
