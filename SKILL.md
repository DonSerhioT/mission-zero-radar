---
name: mission-zero-radar
description: "Signal triage for AI agents — convert an external signal into a context-grounded decision, bounded test, commercial validation, productization path, watch/park trigger, or explicit discard."
version: 0.1.0
category: strategy
status: stable
---

# Mission Zero Radar

Use after research, monitoring, a competitor move, a new model/tool, a market signal, or another external event creates a candidate for attention.

The job is not to summarize the signal. The job is to decide: **does this matter now, why, and what happens next?**

## Required context
Before deciding, identify:
- current goal/mission;
- verified bottleneck, risk, or open decision;
- existing capability affected;
- time/cost/risk constraints;
- facts, claims, and missing evidence.

If context is missing, do not invent strategic relevance.

## Verdicts
- `BUILD_NOW` — exceptional: verified blocker + verified missing capability + proven implementation path.
- `TEST_NOW` — relevant uncertainty can be resolved by a cheap reversible test.
- `COMMERCIAL_VALIDATE` — plausible external value/revenue; real buyer/need evidence required before build.
- `PRODUCTIZE` — internally proven capability with a credible reusable external surface.
- `WATCH` — no action now; a specific external event/date/threshold can change the decision.
- `PARK` — value path exists, but a named internal dependency is not ready and a cheap test cannot resolve it now.
- `IGNORE` — no current value path, no justified test, no precise trigger, or duplicated capability.

## Decision ladder
Apply in order:
1. **Current state first.** If the capability already exists and has no unresolved active-goal measurement, suppress the duplicate.
2. **Commercial gate.** No buyer/need evidence → `COMMERCIAL_VALIDATE`, never a product build.
3. **High-risk gate.** Money movement, destructive actions, credentials, production writes, or authority expansion cannot become `BUILD_NOW` from radar evidence alone.
4. **BUILD is exceptional.** If blocker, missing capability, or proven implementation path is uncertain, do not build.
5. **Prefer TEST over PARK when uncertainty is cheap to resolve.** A <=1-day or small-sample bounded test with metric + stop condition should become `TEST_NOW`.
6. **PARK needs a real dependency.** “Maybe later” is not enough.
7. **WATCH needs an exogenous trigger.** Generic technology maturity is not a trigger.
8. **IGNORE founder-noise.** Hype, stars, funding, generic monetization, and duplicate capabilities do not create work.
9. **PRODUCTIZE only after internal proof.** External demand may still require commercial validation.

## Active-goal measurement rule
If a signal targets an explicitly active goal, related capability already exists, but the outcome is not measured against a current baseline, choose `TEST_NOW` rather than assuming the problem is solved or building another layer.

Examples:
- cost-control signal + routing/limits already exist + spend leakage unmeasured → test current spend/overrun baseline;
- observability signal + logs exist + cost/trace coverage unknown → audit coverage;
- governance signal + approvals exist + false-pass/false-block behavior unmeasured → test representative actions.

## Context and time discipline
- Use only goals/dependencies explicitly present in current project context or verified state; do not invent hypothetical future customers or roadmaps to keep an idea alive.
- PARK requires a real existing dependency. WATCH requires a real external trigger. “If someday X happens” is IGNORE.
- Check temporal validity. Expired deadlines, stale odds/rankings, and past “next week” promises do not justify WATCH without fresh evidence.

## Five decision questions
1. Current fit — what current goal/bottleneck does this affect?
2. Value path — what concrete benefit can occur?
3. Evidence — what is fact, claim, and gap?4. Bounded next step — what is the cheapest reversible way to decide?
5. Opportunity cost — what current work would this displace?

## Required output
```yaml
signal: <normalized signal>
verdict: BUILD_NOW|TEST_NOW|COMMERCIAL_VALIDATE|PRODUCTIZE|WATCH|PARK|IGNORE
relevance_band: HIGH|MEDIUM|LOW
current_fit: <specific fit or NONE>
value_path: <specific benefit or NONE>
evidence_status: <FACTS / CLAIMS / GAPS>
why_now: <why action is justified now or why not>
cheapest_bounded_next_step: <single test/action or NONE>
metric: <measurable success criterion>
stop_condition: <rejection/stop condition>
route_to: <evaluation|backlog|commercial-validation|productization|watch|discard>
revisit_trigger: <specific trigger or NONE>
brand_asset: YES|NO
brand_angle: <only when tied to real work, evidence, experiment, failure, or measured result>
```

## Safety boundary
This skill decides and routes. It does not authorize purchases, financial transactions, deployments, destructive changes, credential changes, production writes, or external messages.

## Quality gates
Redo the decision if it recommends BUILD without a verified blocker, TEST without metric + stop condition, commercial build without buyer evidence, WATCH without a precise trigger, or creates work from a duplicated/already-implemented capability.

A stored report is not value. A signal creates value only when it changes a decision, launches a bounded test, enters a justified backlog, creates a commercial validation, becomes a proven reusable asset, receives a precise revisit trigger, or is explicitly discarded.