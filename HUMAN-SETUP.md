# Human Setup Guide
## Manual step-by-step setup with prompt examples

This guide is for a **human operator** who wants to set up and use the PM bundle manually in an LLM environment such as ChatGPT Custom GPT, Codex, GitHub Copilot, Claude, or another capable assistant.

This guide complements `SETUP.md`:
- `SETUP.md` is the **model-facing playbook**.
- `HUMAN-SETUP.md` is the **operator guide for you**.

---

## 1. What good setup looks like
A good setup does **not** start by asking the model to generate every artifact immediately.
It starts by making the model:
1. read the bundle,
2. inspect the real project evidence,
3. identify the likely phase,
4. tell you what is missing,
5. ask focused questions,
6. draft one useful artifact at a time.

The first success target is usually:
- project charter,
- scope baseline,
- risk register,
- methodology execution log,
- decision log.

---

## 2. Recommended manual workflow

### Step 1: give the model the bundle and project sources
Provide:
- the bundle,
- the project source docs,
- and a clear instruction to use the bundle as the governing methodology.

**Prompt example**
> Use this bundle as the governing methodology for project setup. Read `README.md` first, then `SETUP.md`. Inspect the uploaded project source documents, determine the likely phase, create a concise setup inventory, and ask me for any missing high-value information before finalizing artifacts.

### Step 2: check the first response
A good first response should:
- summarize the available evidence,
- identify the likely phase,
- list the first artifacts to initialize,
- ask only the highest-value missing questions.

If it jumps directly into writing many generic documents, stop it.

**Correction prompt**
> Stop. Do not generate more artifacts yet. First summarize the available evidence, identify the likely phase, list the missing critical information, and ask me the 3 to 5 highest-value questions.

### Step 3: answer only what matters now
Give the model either:
- an existing source document,
- or a short structured answer.

Prefer documents over retyping.

**Prompt example**
> Use the attached proposal deck and discovery notes as the source of truth for project goal, scope, and constraints. Keep assumptions explicit.

### Step 4: create one artifact at a time
Ask for a single artifact first.

**Prompt example**
> Draft `artifacts/project-charter.md` using the bundle template. Ground it in the provided source docs. If anything critical is still missing, ask me before finalizing.

### Step 5: review the artifact quality
Check whether the draft:
- reflects the real project,
- separates facts from assumptions,
- shows unresolved questions,
- is actually useful to the team.

**Review prompt**
> Review this draft for missing evidence, hidden assumptions, and sections that are too generic. Then propose the smallest set of changes needed to make it useful.

### Step 6: continue with the next artifact
Only move on once the current artifact is good enough.

Suggested order:
1. charter,
2. scope,
3. risk register,
4. execution log,
5. decision log,
6. RACI,
7. communication plan,
8. architecture summary,
9. metrics,
10. backlog,
11. roadmap.

---

## 3. Prompts that work well

### A. Bundle bootstrap
> Use this bundle as the governing methodology. Read `README.md` first, then `SETUP.md`. Inspect the project sources, identify the likely phase, create a concise setup inventory, and ask only the highest-value missing questions before drafting anything substantial.

### B. Source-first behavior
> Before drafting this artifact, tell me what you can already extract from the source docs, what is still missing, and whether there is an existing document I should upload instead of answering manually.

### C. Charter creation
> Draft `artifacts/project-charter.md` from the current sources using the official template structure. Keep assumptions explicit and do not finalize if the project goal or outputs remain vague.

### D. Scope creation
> Draft `artifacts/scope-baseline.md`. Make in-scope and out-of-scope boundaries explicit. If the boundary is still weak, ask me focused follow-up questions first.

### E. Risk register creation
> Create `artifacts/risk-register.csv` using the official category and status vocabulary from the bundle. Do not add generic filler risks with no evidence.

### F. Readiness review
> Based on the bundle mappings and current artifacts, assess whether the project is ready for planning review. Give a verdict, explain gaps, and recommend the next 3 actions.

---

## 4. When to stop and ask for better inputs
Pause setup and gather better source material if:
- the customer or contracting parties are still unclear,
- the project goal is generic or contradictory,
- there is no usable scope evidence,
- there are no milestone assumptions,
- the technical solution is unknown,
- the model starts filling the documents with obvious boilerplate.

---

## 5. Platform notes
### Custom GPT
Use the Custom GPT edition or upload the bundle knowledge files and paste the instruction set. Ask the GPT to bootstrap from project uploads one artifact at a time.

### Codex
Keep the shared methodology in `pm-bundle/` and use `.codex/` only as the native wrapper layer.

### GitHub Copilot
Use `.github/copilot-instructions.md` and optional path-specific instructions as adapters. Keep the bundle itself centralized.

---

## 6. Final rule of thumb
If you are unsure whether to ask for more input or let the model continue, prefer asking for more input.

The bundle is most valuable when it produces **fewer, better, evidence-grounded artifacts**.
