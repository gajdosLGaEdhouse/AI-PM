---
id: 03-02
phase: planning
name: Solution design
purpose: Describe the target solution, major components, interfaces, environments, and technical decisions.
inputs:
  - scope-baseline
  - current-state-analysis
  - technical-notes
outputs:
  - architecture-summary
recommended_techniques:
  - working sessions
  - structured review
  - traceable decision-making
checks:
  - major components visible
  - interfaces visible
  - important technical choices visible
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

# Solution design

## Why this activity matters
Describe the target solution, major components, interfaces, environments, and technical decisions.

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
