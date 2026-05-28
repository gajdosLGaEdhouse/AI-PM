# Skill Contract: Source Docs to Initial Risk Register

## Purpose
Create an initial `artifacts/risk-register.csv` aligned to the official risk-register template.

## When to use
Use during initiation and planning, or whenever risks are spread across notes and not yet formalized.

## Primary methodology coverage
- 02-04 Risk identification
- 03-04 Risk treatment

## Required inputs
- at least two of:
  - project charter,
  - scope baseline,
  - solution design or architecture summary,
  - discovery notes,
  - roadmap or milestone draft.

## Output artifacts
- `artifacts/risk-register.csv`
- grouped top-risk summary
- suggested updates for the methodology execution log

## Required columns
- id
- kategorie_rizika
- nazev
- popis
- zdroj_rizika
- dopad_rizika
- stav_rizika
- pravdepodobnost
- mitigacni_plan
- stav_mitigace
- reakce_pokud_nastane
- owner
- trigger
- confidence
- linked_artifacts
- review_date

## Controlled vocabulary
### Categories
- Technické
- Časové
- Personální
- Externí
- Ostatní

### Risk status
- Otevřeno
- Uzavřeno

### Probability
- Vysoká
- Střední
- Nízká

### Mitigation status
- Akceptováno
- Zmírněno
- Převedeno
- Eliminováno

## Guardrails
- do not create generic filler risks with no evidence,
- do not assign false certainty,
- keep low-confidence risks marked as such.
