# AI PM Bundle

Reusable bundle for methodology-driven, AI-assisted project management based on the Edhouse project-management methodology.

## What this bundle is
This bundle is a **portable project-management operating system**.
It combines:
- structured methodology source docs,
- reusable templates,
- mappings between activities, artifacts, skills, and checks,
- one PM orchestration specification,
- artifact-focused skill contracts,
- platform-aware setup guidance.

The goal is to help a human or an LLM set up and maintain project artifacts that are actually useful in delivery, not just formally complete.

## What this bundle is not
This bundle is not tied to a single runtime.
It can be adapted for:
- Custom GPT,
- Codex,
- GitHub Copilot,
- other LLM-driven workflows.

The **core bundle is platform-agnostic**.
Platform-specific instructions belong in dedicated sections or adapter files.

## Read this first
Use this reading order:
1. `README.md` — entrypoint and bundle map
2. `SETUP.md` — model-facing setup playbook
3. `HUMAN-SETUP.md` — human operator guide
4. `agents/pm-orchestrator.md` — governing orchestration rules
5. `mappings/README.md` and mapping YAML files
6. the methodology files and templates needed for the current artifact

## Recommended usage modes
### Human-driven setup
Use `HUMAN-SETUP.md`.
This is the best starting point when a human is manually guiding the setup.

### Model-driven setup
Use `SETUP.md`.
This is the preferred playbook for an LLM or agent that is doing artifact bootstrap and control work.

## Quick start
1. Put the bundle into a workspace, usually as `pm-bundle/`.
2. Create a project instance with:
   - `project-config.yaml`
   - `sources/`
   - `artifacts/`
3. Give the LLM this instruction:

> Use this bundle as the governing methodology. Read `README.md` first, then `SETUP.md`. Inspect the available project sources, identify the likely phase, create a concise setup inventory, and initialize only the highest-value artifacts first. Ask for missing source documents or focused details before finalizing each artifact.

4. Start with the minimum bootstrap artifacts:
   - `artifacts/project-charter.md`
   - `artifacts/scope-baseline.md`
   - `artifacts/risk-register.csv`
   - `artifacts/methodology-execution-log.md`
   - `artifacts/decision-log.md`

## Directory map
- `README.md` — bundle entrypoint
- `SETUP.md` — model-facing setup playbook
- `HUMAN-SETUP.md` — human-facing operator guide
- `agents/` — orchestration rules
- `methodology/` — structured methodology activities
- `mappings/` — methodology-to-artifact / skill / check control layer
- `templates/` — reusable artifact templates
- `schemas/` — lightweight artifact schemas and conventions
- `skills/` — artifact transformation contracts
- `custom-gpt/` — Custom GPT adapter pack
- `examples/` — sample project-instance layout

## Core design rules
- Methodology tells you **how** to run the project.
- Source docs and accepted artifacts tell you **what is true** about the project.
- The orchestrator manages completeness, sequencing, consistency, and readiness.
- Skills are narrow, artifact-focused transforms.
- Missing information should trigger focused follow-up questions, not invented content.

## Bundle quality rule
Do not optimize for setup speed over artifact value.
Always prefer **one useful artifact plus a few focused questions** over many generic documents.
