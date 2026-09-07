# Mission Zero Radar — Evaluation Rubric

A useful radar is judged by decisions, not by how many signals it retains.

## Primary metrics

1. **Verdict agreement** — exact match against a founder/operator-reviewed contrast set.
2. **False-action rate** — percentage of `BUILD_NOW` / `TEST_NOW` verdicts that lack a verified current fit.
3. **Noise suppression** — percentage of clearly irrelevant/duplicated/no-trigger signals correctly sent to `IGNORE`.
4. **Commercial discipline** — unconfirmed business ideas must be `COMMERCIAL_VALIDATE`, never treated as proven demand.
5. **Bounded-test quality** — every `TEST_NOW` includes a measurable metric and stop condition.

## Secondary metrics

- Route correctness
- Evidence honesty
- Opportunity-cost awareness
- Revisit-trigger specificity
- Brand-asset precision

## Release gate for a public v0.1

Suggested initial gate:
- >=80% verdict agreement on a reviewed contrast set;
- zero high-risk direct-action recommendations from radar-only evidence;
- zero commercial ideas mislabeled as validated demand;
- >=90% of `TEST_NOW` cases include both metric and stop condition;
- manual review of all `BUILD_NOW` and `PRODUCTIZE` outputs.

The dataset should contain positive, negative, ambiguous, commercial, technical, and brand cases. Do not optimize only for exciting signals.
