# GH.07C — Answerability Gate integration

`run_guarded_pipeline` is the new **strict entrypoint**. It requires a caller-provided verified chunk registry (SHA-256, section, title, pages, document filename) and fails closed if retrieval returns unsupported or unverified data. It does not infer provenance from retrieval hits. `run_pipeline` remains backward compatible and **does not** enforce answerability unless `enforce_answerability=True` is set.

`ANSWERABLE` means **structurally verified evidence available** only, not semantic support or authorization. `semantic_verified` remains `False`. No LLM generation is present. The registry must itself be trusted and must correspond to the indexed corpus; this is not independently proven by this stage. Mixed-document results require a future per-document verified registry. Safety routing precedes retrieval.

Release remains HOLD until semantic entailment checks, no-ID queries, negative/out-of-domain cases, and end-to-end deployment checks. Original frozen GH.07/GH.07B datasets are unchanged.
