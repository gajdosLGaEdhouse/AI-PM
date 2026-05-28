---
id: 02-03
phase: initiation
name: Scope definition
purpose: Define the expected scope of work in broad but precise terms, including boundaries and acceptance direction.
inputs:
  - project-goal
  - contract
  - discovery-notes
outputs:
  - project-charter
  - scope-baseline
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - in-scope items stated
  - out-of-scope items stated
  - acceptance direction drafted
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

# Scope definition

## Why this activity matters
Define the expected scope of work in broad but precise terms, including boundaries and acceptance direction.

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
