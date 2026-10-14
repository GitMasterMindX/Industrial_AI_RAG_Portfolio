# GH.07D E2E scope

Real BM25/Chroma/SentenceTransformer/RRF is exercised through a provenance-bound adapter into `run_guarded_pipeline`.

Registry is built from the **synthetic fixture** in the same process. This demonstrates correct integration but does **not** establish an independent authoritative source of truth. Identifier alignment is a narrow deterministic check, not semantic entailment. `ANSWERABLE` means structural readiness only; semantic_verified remains false. Public release remains HOLD.
