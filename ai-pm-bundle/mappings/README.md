# Mapping Layer

This directory turns the methodology into an executable control plane for the PM Orchestrator.

## Files
- `methodology-to-artifacts.yaml` maps each activity to the artifacts that should exist or be updated.
- `methodology-to-skills.yaml` maps each activity to the preferred skill invocation path.
- `methodology-to-checks.yaml` lists validation, readiness, and failure checks.

## Intended use
On each substantial request, the orchestrator should:
1. determine which methodology activity or phase is relevant,
2. load the matching mapping entries,
3. verify primary artifacts,
4. choose a default skill if generation or update is needed,
5. run the listed checks before marking the activity complete.
