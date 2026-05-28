---
id: 04-04
phase: delivery
name: Monitoring
purpose: Continuously monitor state, metrics, risks, and plan changes so the team can react early.
inputs:
  - metrics
  - roadmap
  - risk-register
  - backlog
outputs:
  - status-report
  - updated-roadmap
  - updated-risk-register
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - health can be assessed quickly
  - roadmap and risks kept current
  - monitoring leads to action
ai_tasks:
  - extract grounded facts from source material
  - highlight missing evidence and weak assumptions
  - draft the target artifact structure
  - recommend follow-up questions before finalization
done_when:
  - primary artifacts exist or are explicitly not applicable
  - assumptions are visible
  - execution note is updated
---

# Monitoring

## Why this activity matters
Continuously monitor state, metrics, risks, and plan changes so the team can react early.

## What good output looks like
A good result is grounded in source evidence, useful to delivery, and traceable to the artifacts listed above.

## Common mistakes
- treating assumptions as facts,
- writing generic filler text,
- ignoring dependencies or ownership,
- skipping execution traceability.

## AI assistance
AI should help by extracting facts, drafting a structured artifact, surfacing gaps, and keeping the execution note current.

## Human decisions required
A human owner must confirm business commitments, final priorities, risk appetite, and any decision that changes scope, timing, quality expectations, architecture, or customer commitment.

## Project execution (Provedeni)
```yaml
project_execution:
  status: not-started
  owner: TBD
  decision_summary: ""
  rationale: ""
  links: []
  last_reviewed: null
```
