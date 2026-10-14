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

This public repository contains documentation, synthetic scenarios and selected results only. It excludes the proprietary implementation and is not a runnable full system.

- [x] Separate portfolio package assembled and integrity checked
- [x] Proprietary code excluded by strict package allowlist
- [x] Public README distinguishes internal FAT from public artifacts
- [x] Portfolio owner approved publication of the selected files and confirmed publication rights (2026-10-14); independent licensing audit not asserted
- [x] Approve private GitHub commit and verify the RC3 file inventory on GitHub
- [x] Portfolio owner approved public visibility (2026-10-14)

**Portfolio publication: PUBLIC — owner approved and verified (2026-10-14).** Full-system release remains HOLD. No open-source license is granted; `NOTICE.md` applies. Independent third-party licensing verification is not asserted.
