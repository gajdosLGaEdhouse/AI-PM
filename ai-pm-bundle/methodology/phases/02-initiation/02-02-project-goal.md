---
id: 02-02
phase: initiation
name: Project goal
purpose: Define a concise and testable project goal, target value, and intended user benefit.
inputs:
  - contract
  - project-brief
  - discovery-notes
outputs:
  - project-charter
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - goal is visible
  - business value is visible
  - goal aligns with commercial basis
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

# Project goal

## Why this activity matters
Define a concise and testable project goal, target value, and intended user benefit.

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
