# Mission Zero Radar — Public Release Gate v0.1

## Purpose
Release only when the decision layer demonstrably suppresses noise and routes useful signals into bounded action.

## Required gates
1. Frozen calibration v0.5 exact verdict agreement >= 80% on a founder-reviewed 30-case set.
2. Final fresh holdout v0.3 exact verdict agreement >= 80% with labels frozen before first run.
3. False BUILD_NOW rate <= 10% on cases whose gold verdict is not BUILD_NOW.
4. False actionable rate (BUILD/TEST/VALIDATE/PRODUCTIZE when gold is WATCH/PARK/IGNORE) <= 15%.
6. 100% of TEST_NOW outputs include a measurable metric and stop condition.
5. 100% of COMMERCIAL_VALIDATE outputs require buyer/need evidence before build.
7. Duplicate/already-implemented signals are suppressed or routed to re-test, not rebuilt.
8. Public package contains no Hermes-private paths, credentials, client data, internal architecture secrets, or non-public commercial evidence.

## Product KPI
Primary: useful decisions / surfaced signals.
Secondary: founder attention saved, false action rate, bounded-test conversion, validated commercial hypotheses, duplicate suppression.

## Release posture
No SaaS build before the free skill proves useful to external users. Public v0.1 should be a portable skill + examples + evaluation rubric + transparent limitations.
