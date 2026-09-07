# Mission Zero Radar

**Turn external signals into decisions, bounded tests, and explicit discard — not another AI-news digest.**

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
