# Mission Zero Radar v0.1 — Evaluation Evidence

Evaluation date: 2026-09-07.

## Protocol
- Historical operating corpus: 457 signals from 45 recurring radar runs.
- Calibration truth: 30 cases, frozen before final calibration run.
- Final holdout: 20 previously unused cases, labels frozen before first inference.
- The holdout was not relabeled after seeing results.
- Evaluation target: exact strategic verdict plus structural action-contract quality.

## Final measured results
- Frozen calibration: **25/30 = 83.3% exact verdict agreement**.
- Fresh frozen holdout, first run: **17/20 = 85.0% exact verdict agreement**.
- Full-contract holdout run: **19/20 = 95.0% exact agreement**.
- Structural contract pass rate: **100%**.
- False `BUILD_NOW` rate: **0%**.
- False actionable rate: **12.5%** (release limit <=15%).
- `TEST_NOW` with metric + stop condition: **100%**.
- `COMMERCIAL_VALIDATE` requiring buyer/need evidence: **100%**.

The first-run 85% holdout score is the primary generalization result; the later 95% full-contract run is reported separately rather than substituted for it.