# Mission Zero Radar

**Turn external signals into decisions, bounded tests, and explicit discard — not another AI-news digest.**

*Category: signal triage — strategic signal evaluation against your current project context. It is not a monitor and not a runtime action firewall: it decides whether a signal deserves action, it does not gate an agent's execution.*

Mission Zero Radar is a small, portable strategic-relevance skill for AI agents. It is designed for founders, operators, product teams, and autonomous-agent systems that already have enough information and need better judgment about what deserves action.

## The problem

Research agents are good at finding more things. That creates a second problem: every interesting model, repository, paper, competitor move, security incident, or business idea becomes another item someone has to read and evaluate.

Mission Zero Radar treats attention as a scarce operating resource. A signal is useful only if it changes a decision, justifies a bounded test, enters a real backlog, creates a commercial validation, becomes a reusable product/capability, has a precise revisit trigger, or is discarded.

## Core flow

`external signal + current context → strategic relevance → verdict → route → bounded next step`

Verdicts:
- `BUILD_NOW`
- `TEST_NOW`
- `COMMERCIAL_VALIDATE`
- `PRODUCTIZE`
- `WATCH`
- `PARK`
- `IGNORE`

The skill deliberately prefers `IGNORE` over vague “maybe useful later” watchlists.

## What makes it different

Mission Zero Radar is not a scraper, feed reader, trend score, or generic prioritization matrix. It assumes discovery already happened.

Its job is the harder boundary between **interesting** and **worth acting on now**. It requires project context, names the value path, separates facts from claims/gaps, forces a cheap reversible next step for tests, defines a stop condition, and makes opportunity cost explicit.

## Example

A new model claims comparable quality at 40% lower cost. If model cost is a live constraint, the correct answer is not “integrate it.” Mission Zero Radar returns `TEST_NOW`, routes it to evaluation, defines a representative benchmark, success metric, and rejection threshold.

If a popular tool looks useful but solves no current problem and has no defined revisit trigger, it returns `IGNORE` rather than growing a backlog.

## Quick start

1. Install (or copy `SKILL.md` into your agent's skill layer):

   ```bash
   npx skills add DonSerhioT/mission-zero-radar
   ```

2. Give the agent one external signal plus your current goal, bottleneck, existing capabilities, and constraints.
3. Require the structured output contract.
4. Treat `TEST_NOW` as a bounded experiment, `COMMERCIAL_VALIDATE` as buyer/need discovery, and `IGNORE` as a real decision — not a backlog item.

Minimal prompt:

```text
Use Mission Zero Radar on this signal.
Current goal: ...
Current bottleneck: ...
Existing capability: ...
Constraints: ...
Signal: ...
```

## Release evidence

The v0.1 decision rules were developed against a 457-signal historical operating corpus, then evaluated on frozen sets. The public repository does not include private historical data.

- frozen calibration: **25/30 = 83.3%** exact verdict agreement
- fresh frozen holdout: **17/20 = 85%** on first run
- full-contract release check: **19/20 = 95%** exact verdict agreement
- false `BUILD_NOW`: **0%**
- false actionable rate: **12.5%** (release limit: 15%)
- `TEST_NOW` with metric + stop condition: **100%**
- `COMMERCIAL_VALIDATE` requiring buyer/need evidence: **100%**

See `BENCHMARKS.md` for methodology and limitations.

## Limitations

Mission Zero Radar is a decision layer, not an oracle. It depends on accurate current context. It can misclassify borderline cases such as `PARK` vs `IGNORE` or `TEST_NOW` vs `COMMERCIAL_VALIDATE`. It should not be used as sole authorization for financial, destructive, deployment, credential, or external-communication actions.

## Files

- `SKILL.md` — portable agent skill
- `examples/sample_cases.jsonl` — small synthetic contrast set
- `evaluation/rubric.md` — evaluation criteria
- `BENCHMARKS.md` — measured release evidence
- `RELEASE_NOTES_v0.1.md` — release notes
- `LICENSE` — MIT

## Status

v0.1 — public-ready portable skill. Evaluation: 83.3% on frozen calibration and 85% on a fresh frozen holdout; full-contract release check passed structural gates with 0% false BUILD. See `BENCHMARKS.md`. Public examples are synthetic/anonymized; no private project data is included.

## Intended use

Use it as a free skill inside an agent, as a decision gate after research/monitoring, or as a building block for a recurring strategic radar. The skill recommends and routes; it should not autonomously execute destructive, financial, purchasing, deployment, or external-communication actions.
