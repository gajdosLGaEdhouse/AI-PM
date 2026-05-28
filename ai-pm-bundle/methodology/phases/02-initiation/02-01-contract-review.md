---
id: 02-01
phase: initiation
name: Contract review
purpose: Review the contract or commercial basis and extract delivery, time, budget, and constraint signals.
inputs:
  - contract
  - offer
  - commercial-summary
outputs:
  - project-charter
  - decision-log
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - contract scope captured
  - dates or timing constraints captured
  - commercial constraints visible
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

# Contract review

## Why this activity matters
Review the contract or commercial basis and extract delivery, time, budget, and constraint signals.

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
