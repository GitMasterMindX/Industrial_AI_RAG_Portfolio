# Validation Status

**Portfolio release candidate:** v0.1.0-portfolio-rc3

## Scope separation

This document distinguishes internal staging validation
from artifacts distributed in the public portfolio.

## Local FAT

- Environment: isolated offline copy of internal staging
- Framework: pytest
- Previously reported result: 216/216 PASS
- Public reproducibility: NO
- Production certification: NO

This result is a historical local test report, not a
fresh test executed by the RC3 portfolio packaging or GitHub publication procedure.

## GH07H experimental NLI

- Model: cross-encoder/nli-MiniLM2-L6-H768
- Dataset: GH07G_FROZEN
- Cases: 24
- Accuracy: 0.75
- Decisive coverage: 0.5385
- Wrong confident count: 0
- Threshold: 0.8
- Margin: 0.2

The report records:
- Stage status: PASS
- Semantic capability pass: false
- Release decision: HOLD

Source: `benchmarks/public/gh07h_report.json`

## Known limitations

1. Confidence scores have not been calibrated.
2. Polish-language performance has not been evaluated.
3. No integration with generated answer verification.
4. No validation using production documentation.
5. Real retrieval FAT remains unconfirmed.
6. Full end-to-end application is not included.

## Interpretation

Passing individual tests or an experimental benchmark
does not demonstrate production safety or readiness.

Publication of documentation and synthetic evaluation
materials is separate from releasing operational code.

## Gate decisions

- Package structural integrity: PASS
- Public/proprietary file separation: PASS by allowlist
- Internal local FAT: HISTORICAL PASS
- GH07H experimental execution: PASS
- GH07H semantic capability: FAIL / NOT ESTABLISHED
- Full-system release: HOLD
- Public portfolio release: PENDING CONTENT APPROVAL
