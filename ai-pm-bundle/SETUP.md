# Project Setup Playbook

This file is a practical bootstrap guide for a fresh GPT or agent using this bundle in a new project.

Use this playbook when a user gives you:
- this bundle,
- one or more project source documents,
- and asks you to initialize project artifacts according to the methodology.

Read `README.md` first, then follow this file.

---

## 1. Core principle

Do **not** generate high-value project artifacts from thin information.

Your job is to create artifacts that are useful in real project delivery, not just formally complete. If key inputs are missing, you must actively gather them before finalizing an artifact.

For each artifact:
1. read the methodology activity and mapping,
2. collect existing source documents first,
3. identify missing critical information,
4. ask the user focused follow-up questions,
5. produce a draft with explicit assumptions only where necessary,
6. mark unresolved items clearly.

Never present assumptions as confirmed facts.

---

## 2. Source-of-truth order

Use information in this order of trust:

1. explicit user instruction in the current conversation,
2. uploaded or provided project source documents,
3. accepted project artifacts already present in the workspace,
4. methodology guidance from this bundle,
5. clearly marked assumptions.

The methodology tells you **how** to structure work.
Project source documents tell you **what is true** for the project.

---

## 3. Setup outcome

The minimum valuable bootstrap outcome is:
- `artifacts/project-charter.md`
- `artifacts/scope-baseline.md`
- `artifacts/risk-register.csv`
- `artifacts/methodology-execution-log.md`
- `artifacts/decision-log.md`

If enough information exists, also create:
- `artifacts/raci.md`
- `artifacts/communication-plan.md`
- `artifacts/architecture-summary.md`
- `artifacts/metrics.md`
- `artifacts/backlog.md`
- `artifacts/roadmap.md`

Do not force later-phase artifacts if the project is not ready.

---

## 4. Platform-agnostic setup sequence

### Step 1: orient yourself
Read these files first:
- `README.md`
- `agents/pm-orchestrator.md`
- `mappings/README.md`
- `mappings/methodology-to-artifacts.yaml`
- `mappings/methodology-to-skills.yaml`
- `mappings/methodology-to-checks.yaml`
- relevant methodology docs for initiation and planning

Then inspect the project sources and group them into:
- contract / commercial docs,
- project brief / proposal,
- discovery notes,
- technical solution docs,
- delivery constraints,
- existing project artifacts.

### Step 2: identify current phase
Determine which phase the project is actually in:
- initiation,
- planning,
- delivery,
- closure,
- pause.

Default to **initiation/planning** unless the evidence clearly shows later phases.

### Step 3: create the workspace structure
Before generating artifacts, establish a stable project-instance structure:
- keep the bundle in one shared location inside the project workspace, for example `pm-bundle/`,
- create `project-config.yaml` as the local project-instance entry point,
- create `sources/README.md` as the source catalog if original source docs will remain in place,
- create `artifacts/` as the destination for generated PM outputs,
- decide the working document language early and keep generated artifacts in one language.

Use one shared methodology location plus one shared artifacts location. Do not scatter copies of the same templates or mappings across the workspace.

### Step 4: create a setup inventory
Before generating artifacts, prepare a simple inventory with:
- available source docs,
- already existing artifacts,
- missing but required artifacts,
- unknowns blocking artifact quality,
- recommended next artifact to create.

Show this inventory to the user in concise form.

### Step 5: gather missing information
Before each artifact, check whether the available sources are sufficient.
If not, ask for more detail or existing documents.

Use focused, artifact-specific questions. Do not ask everything at once.
Ask only for the highest-value missing information.

### Step 6: draft artifact
Create the artifact using the bundle templates and methodology.

Each draft must include:
- content grounded in source docs,
- explicit assumptions section,
- unresolved questions section,
- links/references to source documents where practical.

### Step 7: update control artifacts
After each artifact is created or updated, also update:
- `artifacts/methodology-execution-log.md`
- `artifacts/decision-log.md` if a decision was made,
- project status of assumptions/open questions.

---

## 5. Codex-specific setup sequence

Use this section when the bundle should be convenient to operate inside Codex, not only as a generic methodology pack.

### Step 1: register the repo-local PM agent
Create a repo-local agent config under `.codex/agents/pm_orchestrator.toml`.

The agent should:
- read `pm-bundle/README.md`, `pm-bundle/SETUP.md`, and `pm-bundle/agents/pm-orchestrator.md`,
- use `project-config.yaml` as the workspace entry point,
- treat `sources/README.md` as the source catalog,
- write PM outputs into `artifacts/`,
- honor the selected working language,
- prefer repo-local native skills for artifact-specific transformations.

### Step 2: create native Codex skills for repeatable PM transformations
If the bundle will be used repeatedly in Codex, convert the reusable bundle skill contracts into repo-local native skills under `.codex/skills/<skill-name>/`.

Each native skill should contain at minimum:
- `SKILL.md`
- `agents/openai.yaml`

Recommended initial skills from this bundle:
- `source-to-charter`
- `source-to-scope`
- `source-to-risk-register`
- `solution-to-backlog`
- `backlog-to-roadmap`
- `meeting-to-actions`
- `project-state-to-status-report`
- `project-closeout`

### Step 3: keep shared methodology assets centralized
Keep the shared methodology in `pm-bundle/`:
- `templates/`
- `mappings/`
- `methodology/`
- shared skill contracts in `skills/`

Do **not** duplicate shared templates, mappings, or methodology references into each native skill unless you explicitly need the skill to be portable outside this repository.

Preferred layering:
- native invocation layer: `.codex/skills/`
- shared methodology layer: `pm-bundle/`
- project outputs: `artifacts/`

### Step 4: validate the Codex layer
Before declaring setup complete, check that:
- the PM agent exists under `.codex/agents/`,
- each native skill has valid frontmatter in `SKILL.md`,
- each native skill has `agents/openai.yaml`,
- the agent can read the shared bundle from `pm-bundle/`,
- generated outputs land in `artifacts/`.

If the standard skill validator is unavailable because of missing dependencies, do a structural fallback check:
- `SKILL.md` exists,
- `name` and `description` frontmatter exist,
- `agents/openai.yaml` exists,
- `display_name`, `short_description`, and `default_prompt` exist.

### Step 5: environment-specific lessons learned
These setup issues are worth calling out explicitly:
- On Windows, ZIP extraction may fail when the archive contains files that differ only by case.
- Creation of `.codex/skills/` may require elevated permission even when `.codex/agents/` is writable.
- Some validator scripts may depend on packages not installed in the runtime by default.
- Keep one shared copy of the methodology assets in `pm-bundle/`; copying them into every skill creates drift.

---

## 6. Custom GPT-specific setup sequence

Use this section when the bundle is being turned into a Custom GPT in ChatGPT.

### Step 1: create the GPT in the GPT editor
Build or edit the Custom GPT in the GPT editor on the web.
Use the bundle as the source for both instructions and knowledge.

### Step 2: split behavior from reference material
Put **behavioral rules** into the GPT Instructions field:
- incremental bootstrap,
- source-first questioning,
- artifact-by-artifact progression,
- assumptions policy,
- language normalization,
- preference for useful artifacts over generic filler.

Put **reference material** into GPT Knowledge:
- methodology overview,
- key methodology activity docs,
- mappings,
- templates,
- orchestration reference,
- setup guidance.

### Step 3: recommended knowledge pack
Use a compact knowledge pack rather than uploading the entire repository blindly.
Recommended items:
- `README.md`
- `SETUP.md`
- `agents/pm-orchestrator.md`
- `mappings/README.md`
- `mappings/methodology-to-artifacts.yaml`
- `mappings/methodology-to-skills.yaml`
- `mappings/methodology-to-checks.yaml`
- the templates most relevant to setup

### Step 4: ignore repo-specific wrappers
Inside Custom GPT, ignore runtime-specific repo wrappers such as:
- `.codex/`
- repo-local validator assumptions
- agent registration files for non-GPT runtimes

Treat the bundle as a knowledge-and-instructions pack, not as a repository-native automation runtime.

### Step 5: bootstrap each project through uploaded source docs
When using the Custom GPT on a real project:
- ask the user to upload the project source documents,
- inspect the uploaded evidence,
- create a concise setup inventory,
- ask for missing high-value inputs,
- then draft the first useful artifact.

### Step 6: validate the Custom GPT behavior
Before treating the Custom GPT as ready, confirm that it:
- reads the bundle guidance before drafting,
- asks for missing source docs or focused details,
- keeps assumptions explicit,
- does not generate many empty artifacts from weak inputs,
- follows the intended bootstrap sequence.

---

## 7. GitHub Copilot-specific setup sequence

Use this section when the bundle should be convenient to operate inside GitHub Copilot.

### Step 1: set repository-wide instructions
Create `.github/copilot-instructions.md` for repository-wide PM bundle behavior.
This file should tell Copilot to:
- read `pm-bundle/README.md` and `pm-bundle/SETUP.md`,
- prefer project source docs over assumptions,
- ask for missing details before finalizing artifacts,
- write outputs into `artifacts/`.

### Step 2: add path-specific instructions where useful
If needed, add `.github/instructions/*.instructions.md` files to target:
- `artifacts/`
- `sources/`
- `pm-bundle/`

Use them only where path-specific behavior adds value.

### Step 3: optionally add `AGENTS.md`
If the Copilot environment supports agent-style guidance, add `AGENTS.md` in the repository root or a relevant subtree.
Use it as a thin adapter layer, not as the canonical storage for methodology content.

### Step 4: keep shared methodology centralized
Keep methodology, mappings, templates, and skill contracts in `pm-bundle/`.
Avoid duplicating them into `.github/` files. The Copilot files should be wrappers and routing hints, not parallel copies of the bundle.

### Step 5: validate the Copilot layer
Before declaring setup complete, check that:
- repository-wide instructions exist,
- path-specific instructions are only used where they help,
- Copilot still asks for missing evidence before finalizing high-value artifacts,
- shared methodology assets remain centralized in `pm-bundle/`.

---

## 8. Mandatory behavior during setup

### 8.1 Ask before pretending certainty
If critical information is missing, ask for it.
Examples of critical gaps:
- no confirmed customer or contracting party,
- no usable project goal,
- no scope boundaries,
- no identified stakeholders,
- no timeline assumptions,
- no known technical constraints,
- no acceptance expectations,
- no risk context.

### 8.2 Prefer existing source docs over conversation-only reconstruction
When possible, ask the user to provide an existing document rather than retyping information.
For example:
- contract summary,
- project brief,
- discovery notes,
- architecture proposal,
- milestone plan,
- stakeholder list,
- communication conventions,
- QA/test strategy.

### 8.3 Draft incrementally
Do not attempt to create every artifact in one pass if the inputs are weak.
Create the highest-value artifact first, validate it, then continue.

### 8.4 Keep assumptions visible
Whenever assumptions are necessary, place them in a dedicated section. Do not bury them in normal prose.

### 8.5 Keep artifacts useful
Prefer a smaller artifact with real project value over a longer artifact filled with generic filler text.

### 8.6 Normalize the working language early
Choose the working language early and keep these aligned:
- generated artifacts,
- active templates,
- runtime-specific wrapper text if present.

### 8.7 Keep shared bundle assets centralized
Native wrappers are the invocation layer, not the canonical storage layer for shared methodology.

Prefer:
- runtime-specific wrappers where needed,
- `pm-bundle/` for shared methodology, mappings, templates, and skill contracts.

### 8.8 Treat environment friction as part of setup
Extraction quirks, permission boundaries, and validator dependencies are setup concerns, not side issues.
If they appear:
- document them,
- resolve them explicitly,
- update the setup instructions so the next user does not rediscover them.

---

## 9. Artifact-by-artifact bootstrap guidance

### 9.1 Project charter
Use template: `templates/project-charter.template.md`
Methodology basis:
- 02-01 Contract review
- 02-02 Project goal
- 02-03 Scope definition
- 02-05 Roles and responsibilities
- 02-06 Project governance

#### Minimum required inputs
- project name
- customer / ordering party
- supplier / delivery party
- subject of project
- project goal / business value
- expected outputs
- core team or at least key roles

#### Ask for more if missing
If any of the following is weak or absent, ask for more details or existing docs:
- contract or proposal summary,
- who the customer is,
- what the project is meant to achieve,
- what is being delivered,
- who owns business and delivery decisions,
- key dates or milestones,
- project delivery mode,
- where technical documentation will live.

#### Good questions to ask
- Do you already have a contract summary, offer, or project brief I should use as the source of truth?
- Who are the contracting parties and the key people on each side?
- What is the concrete business goal and expected benefit for the customer?
- What are the main outputs of the project?
- Do you already have a milestone plan or target dates?
- How do you intend to run the project: agile, waterfall, or hybrid?

#### Do not finalize if missing
Do not finalize the charter if project goal and outputs are still vague.

### 9.2 Scope baseline
Use template: `templates/scope-baseline.template.md`
Methodology basis:
- 02-03 Scope definition
- 03-01 Current-state analysis
- 03-02 Solution design

#### Minimum required inputs
- in-scope items
- out-of-scope items
- constraints
- dependencies
- assumptions
- acceptance criteria or at least acceptance approach

#### Ask for more if missing
Ask for existing discovery notes, proposal decks, workshop notes, or scope summaries.

#### Good questions to ask
- Do you have existing discovery notes, solution proposal, or workshop outputs I should use?
- What is explicitly in scope and explicitly out of scope?
- Are there customer dependencies, third-party systems, environments, or approvals?
- Are there acceptance criteria already agreed, even informally?
- What is excluded for the first release or MVP?

#### Do not finalize if missing
Do not finalize the scope if there is no clear boundary between included and excluded work.

### 9.3 Risk register
Use template: `templates/risk-register.template.csv`
Methodology basis:
- 02-04 Risk identification
- 03-04 Risk treatment

#### Minimum required inputs
- risk title and description
- category
- probability
- impact
- mitigation approach
- owner or at least owner candidate
- status

#### Ask for more if missing
Ask for known project risks, technical uncertainties, customer-side dependencies, staffing constraints, and schedule pressure.

#### Good questions to ask
- What are the biggest technical, time, staffing, and external risks right now?
- Are there any known customer dependencies that can delay validation or delivery?
- Are there open questions that could significantly change scope or architecture?
- Who should own risk tracking on this project?

#### Do not finalize if missing
Do not treat a generic risk list as complete. Mark it as initial and incomplete if ownership or mitigation is missing.

### 9.4 RACI / roles
Use template: `templates/raci.template.md`
Methodology basis:
- 02-05 Roles and responsibilities
- 03-05 Communication plan

#### Minimum required inputs
- named or role-based participants
- key project activities or decisions
- responsibility assignments

#### Ask for more if missing
Ask for:
- stakeholder list,
- customer-side roles,
- delivery team roles,
- approval authority,
- technical authority,
- QA authority.

### 9.5 Communication plan
Use template: `templates/communication-plan.template.md`
Methodology basis:
- 03-05 Communication plan
- 04-05 Customer reporting

#### Minimum required inputs
- parties involved
- communication channels
- meeting types and frequency
- escalation path
- project documentation location
- bug reporting mechanism

### 9.6 Architecture summary
Use template: `templates/architecture-summary.template.md`
Methodology basis:
- 03-02 Solution design

### 9.7 Metrics
Use template: `templates/metrics.template.md`
Methodology basis:
- 03-06 Metrics
- 04-04 Monitoring

### 9.8 Backlog and roadmap
Suggested templates:
- `templates/backlog.template.md`
- `templates/roadmap.template.md`
- `templates/status-report.template.md` for later reporting

Methodology basis:
- 03-03 Scope and estimates
- 04-04 Monitoring

---

## 10. How to ask for more information

When information is missing, prefer this order:
1. ask for an existing document,
2. ask for a short structured answer,
3. make a temporary assumption only if necessary.

### Good pattern
- State what you can already extract from sources.
- State what is still missing.
- Ask 2 to 5 focused questions.
- Explain why those answers materially improve the artifact.

### Example
“I can already draft the project goal, rough scope, and initial risks from the proposal. To make the charter actually useful, I still need who owns acceptance on the customer side, what the main milestone dates are, and whether the delivery mode is hybrid or fully agile. If you have a charter draft, contract summary, or milestone plan, send that; otherwise answer these three points directly.”

### Avoid
- giant questionnaires,
- vague prompts like “tell me more about the project”,
- silently inventing missing stakeholder or governance details.

---

## 11. What to do when the user has little information

If the user does not have more source material:
- produce a **draft** artifact,
- mark it clearly as draft,
- include an assumptions section,
- include open questions,
- include a “what to confirm next” section.

Use the artifact to drive the next conversation, not to pretend completeness.

---

## 12. Setup output format for the GPT

When bootstrapping a new project, use this operating rhythm:

### First response
- confirm you will use the bundle,
- summarize the project sources you found,
- state the likely project phase,
- list the first artifacts to initialize,
- ask only the highest-value missing questions.

### Subsequent responses
For each artifact:
- summarize source basis,
- list missing information,
- ask focused follow-ups if needed,
- then draft the artifact,
- then note what was updated in execution or decision tracking.

### Completion signal for setup
Setup is complete when:
- the minimum bootstrap artifacts exist,
- each has clear source grounding,
- key assumptions are visible,
- unresolved questions are explicitly tracked,
- the methodology execution log reflects what was done.

---

## 13. Non-negotiable rules

- Do not fabricate project facts.
- Do not hide assumptions.
- Do not optimize for speed over artifact quality.
- Do not create all artifacts from weak inputs just because templates exist.
- Always prefer one useful artifact plus 3 good questions over 8 generic documents.
- Do not let generated PM documents drift into mixed languages unintentionally.
- Do not duplicate shared methodology assets into every native wrapper without a portability reason.

This bundle is designed to support real project-management work. Setup quality matters more than setup speed.
