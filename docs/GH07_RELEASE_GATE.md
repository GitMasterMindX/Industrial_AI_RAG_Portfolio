# GH.07 — Internal System Release Gate

This checklist describes **full-system** readiness, not approval to publish the documentation-only portfolio. A checked item denotes the state of the internal project at the time of the original gate and does not establish public reproducibility.

- [x] 36 synthetic retrieval questions and 12 synthetic corpus sections prepared
- [x] Benchmark implementation, report schema and SHA-256 provenance recorded internally
- [ ] Confirm clean-environment real retrieval execution, versions and evidence
- [ ] Independently review safety/routing test coverage and behavior
- [ ] Validate generated answers and abstention separately
- [ ] Add non-ID paraphrases and blind test set
- [ ] Complete third-party rights, provenance and licensing review
- [ ] Complete security review of source and release history
- [ ] Confirm CI and fresh installation on supported Python versions
- [ ] Approve full-system release

**Full-system release: HOLD.** The GH07H experimental execution status `PASS` does not change its `semantic_capability_pass: false` or `release_decision: HOLD`.

## Separate public portfolio gate

This repository candidate contains documentation, synthetic scenarios and selected results only. It excludes the proprietary implementation and is not a runnable full system.

- [x] Separate portfolio package assembled and integrity checked
- [x] Proprietary code excluded by strict package allowlist
- [x] Public README distinguishes internal FAT from public artifacts
- [ ] Complete human review of every public file and third-party rights
- [x] Approve private GitHub commit and verify the RC3 file inventory on GitHub
- [ ] Approve any future switch to PUBLIC explicitly

**Portfolio publication: PENDING APPROVAL.** No open-source license is intended or granted; `NOTICE.md` applies. An open-source LICENSE is not a requirement for this portfolio, but third-party rights still require review.
