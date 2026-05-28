---
id: 04-05
phase: delivery
name: Customer reporting
purpose: Report project progress, deviations, risks, and next steps in a format the customer can act on.
inputs:
  - roadmap
  - status-evidence
  - risk-register
outputs:
  - status-report
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - progress vs plan visible
  - risks visible
  - decisions needed visible
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

# Customer reporting

## Why this activity matters
Report project progress, deviations, risks, and next steps in a format the customer can act on.

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
