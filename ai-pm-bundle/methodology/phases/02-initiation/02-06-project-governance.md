---
id: 02-06
phase: initiation
name: Project governance
purpose: Define how the project will be run, where project state lives, and how changes and decisions are handled.
inputs:
  - project-charter
  - commercial-basis
  - delivery-constraints
outputs:
  - project-charter
  - decision-log
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - delivery mode visible
  - change-handling logic visible
  - documentation location visible
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

# Project governance

## Why this activity matters
Define how the project will be run, where project state lives, and how changes and decisions are handled.

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
