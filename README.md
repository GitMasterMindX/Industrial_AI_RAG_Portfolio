# Industrial AI RAG Assistant

**Public Portfolio | v0.1.0-portfolio-rc3 | Pre-release**

Industrial AI RAG Assistant is an engineering research and
development project exploring retrieval-augmented assistance
for industrial technical documentation.

The project investigates document retrieval, query routing,
evidence validation, answerability assessment, and
safety-oriented response gating.

## Repository purpose

This repository is a **public portfolio package**, not the
complete implementation of the Industrial AI RAG Assistant.

It contains selected technical documentation, synthetic
demonstration materials, benchmark scenarios, and
experimental validation results.

The full retrieval engine, implementation details,
operational assets, indexes, and proprietary components
are intentionally excluded.

## Architecture overview

Conceptual processing flow:

1. Technical question
2. Query analysis and routing
3. Retrieval of relevant documentation
4. Evidence assessment
5. Answerability and safety checks
6. Evidence-grounded response or abstention

This is an architectural description, not a claim that
the complete pipeline is executable from this repository.

## Public / Proprietary boundary

**Public Portfolio**
- Selected architecture and validation documentation
- Synthetic technical manual and example questions
- Benchmark scenarios and experimental results
- Release and security information

**Proprietary Core — Restricted**
- Full source implementation and internal algorithms
- Retrieval engine and operational integrations
- Models, embeddings, and persistent vector indexes
- Production/customer documentation and credentials
- Backups and internal infrastructure configuration

## Validation summary

### Local FAT — full private staging environment

A previously recorded local offline test run reported
**216/216 pytest tests passing** in an isolated staging copy.

This result relates to the full internal project staging,
not to tests executable from this public portfolio.

The complete test suite and its implementation are not
included in this repository.

### GH07H — experimental semantic verification

The included GH07H report documents an experiment using
`cross-encoder/nli-MiniLM2-L6-H768` on 24 frozen,
synthetic challenge cases.

Reported metrics:

- Overall accuracy: **75%**
- Decisive coverage: **53.85%**
- Wrong confident assertions: **0**
- Decision threshold: **0.8**
- Margin: **0.2**

The experimental stage reported PASS for its own
execution criteria, but **semantic capability did not
pass the release gate**.

The report explicitly records `semantic_capability_pass:
false` and `release_decision: HOLD`.

### Important limitations

- The model confidence scores are not calibrated.
- Polish-language questions were not assessed in GH07H.
- Claim-generation integration was not demonstrated.
- Production documentation was not validated.
- Real retrieval FAT has not been confirmed.
- The public portfolio does not contain an executable
  end-to-end RAG application.

For details, see `docs/VALIDATION_STATUS.md` and
`benchmarks/public/gh07h_report.json`.

## Synthetic demonstration materials

The `demo/synthetic/` directory contains a fictional
industrial drive manual and sample questions.

These files are intended to illustrate the evaluation
context and are not manufacturer instructions.

No executable RAG demo is distributed in this release.

## Repository structure

```text
Industrial_AI_RAG_Assistant/
├── README.md
├── SECURITY.md
├── CHANGELOG.md
├── NOTICE.md
├── docs/
│   └── VALIDATION_STATUS.md
├── demo/
│   └── synthetic/
└── benchmarks/
    └── public/
```

Additional selected documents are located under
`docs/` and `benchmarks/`.

## Safety and release status

This project is experimental engineering software.

It must not be used as the sole basis for decisions
affecting machinery, personnel safety, industrial
operations, or equipment protection.

**Production readiness: NOT ESTABLISHED.**

**Full-system release decision: HOLD.**

Portfolio publication approval is a separate decision
and does not imply production approval.

## Intellectual property and licensing

All rights reserved.

No open-source license is granted by this repository.
Third-party rights remain with their respective owners.

See `NOTICE.md` and `SECURITY.md`.
