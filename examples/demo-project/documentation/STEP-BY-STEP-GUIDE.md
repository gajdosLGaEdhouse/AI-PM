# Step-by-Step Guide: Creating Artifacts for Your Project

**Purpose:** Detailed guidance for creating each artifact in the AI-PM Bundle  
**Audience:** Project managers and teams setting up a new project  
**Estimated Time:** 4-6 hours for complete bootstrap setup

---

## Before You Start

### Prerequisites
1. ✅ You have read `../../ai-pm-bundle/README.md`
2. ✅ You have read `../../ai-pm-bundle/SETUP.md` (model playbook)
3. ✅ You have your project source documents ready
4. ✅ You have key stakeholders identified
5. ✅ You have created `project-config.yaml`

### Setup Your Workspace
```
your-project/
├── project-config.yaml
├── sources/
│   ├── README.md (source catalog)
│   ├── business-case.md
│   ├── technical-proposal.md
│   └── stakeholder-list.md
├── artifacts/
│   └── (will create files here)
└── documentation/
    └── (guidance files)
```

---

## Part 1: Project Charter (45 minutes)

### Purpose
The project charter officially authorizes the project and defines its fundamental parameters: goal, scope, success criteria, and key stakeholders.

### When to Create
**First** - This is the foundational artifact

### Template Reference
See `../../ai-pm-bundle/templates/project-charter.template.md`

### Methodology Basis
- Activity 02-01: Contract review
- Activity 02-02: Project goal definition
- Activity 02-03: Scope definition
- Activity 02-05: Roles and responsibilities
- Activity 02-06: Project governance

### Information You'll Need

**From source documents:**
- Business case (business goal, expected outputs, business value)
- Project proposal or brief
- Stakeholder list (key parties and roles)

**Questions to answer before starting:**
1. Who ordered this project? (Customer/Executive)
2. What specific business problem does it solve?
3. What are the main deliverables?
4. How will success be measured?
5. Who are the key stakeholders?
6. What is the expected timeline?
7. What governance approach will we use?

### Step-by-Step Creation

**Step 1: Extract Executive Summary**
- Project name and code
- Business goal (one sentence that states the business value)
- Main outputs
- Expected timeline
- Budget range

*Source:* Extract from business-case.md

*Example for Compliance Dashboard:*
> **Goal:** Automate transaction compliance monitoring to reduce manual review costs by 75%, improve accuracy to <0.1% error rate, and enable real-time regulatory reporting.

**Step 2: Identify Contracting Parties**
- Who is the customer/ordering party?
- Who is the supplier/delivery party?
- Who represents each side?

*Source:* Extract from stakeholder-list.md

**Step 3: Define Success Criteria**
These should be SMART (Specific, Measurable, Achievable, Relevant, Time-bound)

*Example for Compliance Dashboard:*
- Accuracy: 99%+ in transaction categorization (baseline: 98%)
- Speed: Regulatory reports in 2-4 hours (baseline: 3-5 days)
- Coverage: 90%+ of transactions auto-processed (baseline: 0%)
- System uptime: 99.5%+
- User adoption: 90%+ within 6 weeks of launch
- ROI: Positive in 12 months

**Step 4: List Key Stakeholders & Roles**
- Sponsor (approver)
- Business owner (defines requirements)
- Delivery lead (responsible for delivery)
- Technical authority
- Quality assurance
- Others (finance, legal, etc.)

*Source:* Extract from stakeholder-list.md

**Step 5: Define Governance**
- Decision-making authority
- Escalation path
- Committee structure
- Steering meetings

**Step 6: State Assumptions & Constraints**
- What are we assuming about the business, market, or technology?
- What constraints exist (budget, timeline, people)?

**Step 7: Add Scope Boundaries (High-Level)**
What's roughly in and out? (More detail in scope-baseline.md)

**Step 8: Draft the Document**
Use template structure:
```
# Project Charter: [Project Name]

## Executive Summary
[1-2 paragraphs with business goal and expected value]

## Project Scope (High-Level)
**In Scope:**
- [Main deliverables]

**Out of Scope:**
- [Major items explicitly excluded]

## Success Criteria
[List of measurable success factors]

## Key Stakeholders
[Table: Name, Role, Interests]

## Governance & Decision-Making
[Sponsors, committees, escalation]

## Timeline
[Estimated phases and key dates]

## Assumptions & Constraints
[List explicit assumptions]
[List constraints: budget, timeline, etc.]

## Approvals
[Signature section]
```

### Quality Checks

✅ **Does the charter clearly state:**
- What problem does this solve?
- What will be delivered?
- How will we know it's successful?
- Who makes decisions?
- When should it be done?

✅ **Is it grounded in source documents?** Can you trace each statement back to a source?

✅ **Are assumptions explicit?** Any guess or assumption is clearly marked as such.

✅ **Is it realistic?** Can a team actually achieve these criteria?

✅ **Is it concise?** Charter should be 2-3 pages, not 10.

### Output
**File:** `artifacts/project-charter.md`  
**Owner:** Project Manager  
**Review with:** Executive Sponsor, Business Owner

### Next
Once approved, move to Scope Baseline

---

## Part 2: Scope Baseline (45 minutes)

### Purpose
The scope baseline explicitly defines what work is included and excluded, plus constraints, dependencies, and acceptance criteria.

### Template Reference
See `../../ai-pm-bundle/templates/scope-baseline.template.md`

### Methodology Basis
- Activity 02-03: Scope definition
- Activity 03-01: Current-state analysis
- Activity 03-02: Solution design

### Information You'll Need

**From source documents:**
- Project proposal / technical proposal
- Business case (benefits and scope)
- Requirements documents
- Discovery workshop notes

**Key questions:**
1. What specific features are in scope for MVP?
2. What is explicitly out of scope (or deferred)?
3. What are integration points and dependencies?
4. What constraints apply (technology, budget, people)?
5. What does "done" look like (acceptance criteria)?

### Step-by-Step Creation

**Step 1: List In-Scope Items (MVP)**
Specific, detailed list of what will be built/delivered

*Example for Compliance Dashboard MVP:*
- Real-time transaction monitoring (all transaction types)
- Configurable rule engine (if-then rules, 50+ rules in MVP)
- Executive dashboard (key metrics, drill-down capability)
- Regulatory report generation (CSV, PDF formats, 5 standard reports)
- User management (role-based access control, 3 roles)
- Audit logging (all user actions, system changes)
- Integration with existing transaction database
- Performance: <2 second response time for queries

**Step 2: List Out-of-Scope Items (Future Phases)**
Explicitly state what will NOT be in MVP

*Example:*
- Machine learning anomaly detection (Phase 2)
- External data feed integration (Phase 2)
- Mobile application (Phase 3)
- Multi-language support (Phase 3)
- Advanced analytics (Phase 3)

**Note:** These become Phase 2/3 work, not rejected work

**Step 3: Identify Dependencies & Constraints**

*Dependencies (things that depend on external work):*
- Regulatory rule definitions from Compliance team (timeline: Week 2)
- Access to transaction database schema from IT (timeline: Week 1)
- Historical transaction data for testing (timeline: Week 3)

*Constraints:*
- Technology: Must use existing tech stack (Java, PostgreSQL, React)
- Budget: $594K total for 6 months
- Timeline: MVP must launch by Nov 30
- People: Max 7 delivery team members

**Step 4: State Assumptions**
What are we assuming about the business and technical environment?

*Examples:*
- Assumption: Legacy system integration will be straightforward (medium risk)
- Assumption: Regulatory requirements will remain stable during project (mitigation: build flexible rule engine)
- Assumption: Current transaction volume remains <10K/day (constraint if volume increases)

**Step 5: Define Acceptance Criteria**
How will we know the scope is complete and acceptable?

*Examples:*
- All transaction types can be monitored with configurable rules
- Reports can be generated and distributed automatically
- System can handle 10K transactions/day with <2s response time
- 99%+ of categorized transactions match manual review
- All audit log entries retained for 7 years

**Step 6: Draft the Document**
Structure:
```
# Scope Baseline: [Project Name]

## In Scope (MVP)
[Detailed list of deliverables]

## Out of Scope (Future Phases)
[Items deferred to Phase 2/3]

## Constraints
[Technology, budget, timeline, people constraints]

## Dependencies
[External items, timelines]

## Assumptions
[Explicit assumptions with risk assessment]

## Acceptance Criteria
[How to know scope is complete]

## Known Gaps/Open Questions
[Items still to be clarified]
```

### Quality Checks

✅ **Is in-scope list:**
- Specific and detailed (not vague)?
- Realistic for the timeline?
- Grounded in source documents?

✅ **Are out-of-scope items:**
- Clearly deferred (not rejected)?
- Placed in clear phases?

✅ **Are constraints:**
- Realistic?
- Understood by all parties?

✅ **Are dependencies:**
- Identified?
- Have timelines?

✅ **Will stakeholders agree** this is the right scope for MVP?

### Output
**File:** `artifacts/scope-baseline.md`  
**Owner:** Project Manager + Solution Architect  
**Review with:** CCO (business owner), CIO (tech owner)

### Common Issues

**Issue:** Scope is too vague ("build a dashboard")  
**Fix:** Get specific - what metrics? which transaction types? which reports?

**Issue:** Stakeholders keep adding "just one more feature"  
**Fix:** Reference the scope baseline and change control process

**Issue:** Scope depends on unclear technology decisions  
**Fix:** Make tech decisions (or defer to technical design phase) BEFORE finalizing scope

---

## Part 3: Risk Register (30 minutes)

### Purpose
Identify, assess, and establish mitigation plans for project risks.

### Template Reference
See `../../ai-pm-bundle/templates/risk-register.template.csv`

### Methodology Basis
- Activity 02-04: Risk identification
- Activity 03-04: Risk treatment

### Information You'll Need

**Risk sources:**
- Business case (business risks, market risks)
- Technical proposal (technical risks)
- Stakeholder analysis (organizational/people risks)
- Similar past projects (lessons learned)

### Step-by-Step Creation

**Step 1: Identify Risks**
Ask: "What could go wrong and have significant impact?"

*Categories:*
- Technical risks (integration, performance, security)
- Business risks (scope, requirements, market)
- Resource risks (staffing, skills, availability)
- External risks (regulatory, market, dependencies)
- Organizational risks (change resistance, stakeholder conflicts)

*Example risks for Compliance Dashboard:*
- Integration complexity with legacy banking system
- Compliance rule definitions not ready on time
- Regulatory requirements change mid-project
- Scope creep from stakeholder feature requests
- System performance with high transaction volume
- Data security concerns from CIO
- User adoption challenges (staff sees tool as threat)

**Step 2: Assess Each Risk**
For each risk, determine:
- **Probability:** Low / Medium / High
- **Impact:** Low / Medium / High
- **Risk Level:** Prob × Impact = Low/Medium/High

*Example assessment:*

| Risk | Probability | Impact | Level |
|------|-------------|--------|-------|
| Scope creep | High | High | **High** |
| Integration complexity | Medium | High | **High** |
| User adoption resistance | Medium | Medium | **Medium** |
| CIO security concerns | Low | High | **Medium** |
| Regulatory change | Low | High | **Medium** |

**Step 3: Define Mitigation Strategy**
For each risk: "What will we do to reduce probability or impact?"

*Examples:*
- **Scope Creep**: Use change control process, freeze scope at Week 4, phase gate at Month 3
- **Integration Complexity**: Early architecture review with IT team (Week 1), prototype integration (Week 2)
- **User Adoption**: Early analyst involvement in design, comprehensive training plan, change management
- **CIO Security**: Security review in architecture phase, pen testing before launch
- **Regulatory Change**: Flexible rule engine design, maintain relationships with regulators

**Step 4: Assign Owners**
Who will monitor this risk and execute the mitigation?

*Examples:*
- Scope creep → Project Manager (owns change control)
- Integration → Solution Architect (owns technical approach)
- Adoption → VP Operations + PM (owns change management)

**Step 5: Draft Risk Register (CSV or table)**

```
Risk ID,Risk Title,Category,Description,Probability,Impact,Risk Level,Mitigation Strategy,Owner,Status
R001,Scope Creep,Project Management,"Stakeholders request features outside agreed scope",High,High,High,"Change control process, scope freeze Week 4, phase gate Month 3",PM,Active
R002,Integration Complexity,Technical,"Legacy system integration proves more complex than expected",Medium,High,High,"Early arch review Week 1, prototype integration Week 2",Architect,Active
R003,User Adoption Resistance,Organizational,"Compliance team views tool as threat to jobs",Medium,Medium,Medium,"Analyst involvement in design, comprehensive training, change management",VP Ops,Active
...
```

### Quality Checks

✅ **Is each risk:**
- Specific (not vague)?
- Realistic?
- From actual project evidence?

✅ **Is mitigation:**
- Concrete (not "hope and pray")?
- Achievable?
- Owned?

✅ **Are high-risk items** receiving active attention?

✅ **Did you avoid** the temptation to list generic risks?

### Output
**File:** `artifacts/risk-register.csv`  
**Owner:** Project Manager  
**Review with:** Steering Committee

### Ongoing Maintenance
- Update monthly
- Move managed risks to lower priority
- Add new risks as they emerge
- Update mitigation status

---

## Part 4: Methodology Execution Log (15 minutes)

### Purpose
Audit trail of how the project was set up - what was done, when, by whom, why.

### Why It Matters
- Shows methodology compliance
- Helps future projects learn from this one
- Proves due diligence if questioned

### Step-by-Step Creation

**Step 1: Document Setup Activities**

| Date | Activity | Owner | Artifact | Status | Notes |
|------|----------|-------|----------|--------|-------|
| May 28 | Initial setup | PM | project-config.yaml | Complete | Workspace structure created |
| May 28 | Source review | PM | sources/* | Complete | Business case, stakeholder list reviewed |
| May 28 | Create charter | PM | project-charter.md | Complete | Based on business case |
| May 28 | Create scope | PM + Architect | scope-baseline.md | Complete | Aligned with technical proposal |
| May 28 | Identify risks | PM | risk-register.csv | Complete | Extracted from multiple sources |
| May 29 | Steering review | PM + Sponsors | decision-log | In Progress | Charter/scope presented |
| May 30 | RACI definition | PM | raci.md | Pending | Roles and responsibilities |
| May 31 | Communication plan | PM | communication-plan.md | Pending | Stakeholder engagement strategy |

**Step 2: Add Key Decisions**

| Date | Decision | Owner | Rationale | Status |
|------|----------|-------|-----------|--------|
| May 28 | MVP scope frozen | Sponsor | Reduce risk by focusing Phase 1 | Approved |
| May 28 | Hybrid delivery model | PM | Agile dev, waterfall compliance gates | Approved |
| May 29 | Phase gate at Month 3 | CFO | Go/no-go decision before full delivery ramp | Approved |

**Step 3: Document Blockers or Issues**

| Date | Issue | Status | Resolution |
|------|-------|--------|------------|
| May 28 | CIO unclear on integration approach | Open | Arch review scheduled for June 1 |
| May 28 | Regulatory rules not finalized | Open | CCO will complete by June 15 |

### Output
**File:** `artifacts/methodology-execution-log.md`  
**Owner:** Project Manager  
**Update:** Monthly

---

## Part 5: Decision Log (15 minutes)

### Purpose
Record key project decisions, their rationale, and outcomes. This prevents "I thought we decided..." conflicts.

### Step-by-Step Creation

**Step 1: Document Setup Phase Decisions**

| Decision | Rationale | Date | Owner | Status | Follow-up |
|----------|-----------|------|-------|--------|-----------|
| MVP Scope Definition | Focus Phase 1 on core compliance functionality; ML/analytics → Phase 2 | May 28 | CCO + CTO | Approved | Communicate to dev team |
| Hybrid Delivery Model | Agile development with waterfall compliance approval gates | May 28 | PM | Approved | Define gate criteria |
| Technology Stack | Use existing tech stack (Java, React, PostgreSQL) for faster integration | May 29 | CIO + Architect | Approved | Confirm licenses and support |
| Phase Gate at Month 3 | Stop-go decision before full delivery ramp (readiness check) | May 29 | CFO + Sponsor | Approved | Define gate criteria |
| Stakeholder Change Control | CCO is owner of scope change decisions (customer-side) | May 29 | PM | Approved | Document in communication plan |

**Step 2: Link to Other Artifacts**
- Each decision should trace to the artifact it affects
- Example: "Hybrid Model → influences project roadmap and RACI"

### Output
**File:** `artifacts/decision-log.md`  
**Owner:** Project Manager  
**Review with:** Steering Committee

### Ongoing Maintenance
- Add decisions as they're made
- Update as decisions change
- Reference in steering meetings

---

## Quality Assurance for All Artifacts

### Before Finalizing Any Artifact

✅ **Grounding Check**
- Can I trace each statement back to a source document?
- Did I invent anything or make unsupported claims?

✅ **Completeness Check**
- Are critical decisions documented?
- Are assumptions explicit?
- Are open questions noted?

✅ **Clarity Check**
- Would a new team member understand this?
- Is terminology consistent?
- Is the document concise (not bloated)?

✅ **Stakeholder Check**
- Does this reflect what stakeholders actually said/agreed?
- Is there anything controversial I should flag?

### Red Flags (Stop and Ask)

🚩 **If the artifact seems incomplete**, ask for missing information rather than inventing it

🚩 **If stakeholders disagree** on a point, document the disagreement in the decision log rather than picking a side

🚩 **If assumptions are sketchy**, mark them clearly and plan to validate them soon

🚩 **If you have low confidence**, say so

---

## Timeline for Bootstrap Setup

```
May 28 (Today)
├─ Morning: Project charter draft
├─ Afternoon: Scope baseline draft
├─ End of day: Risk register initial

May 29
├─ Morning: Stakeholder steering review
├─ Afternoon: Revise artifacts based on feedback
├─ End of day: Finalize charter & scope

May 30
├─ Morning: Finalize risk register
├─ Afternoon: Create RACI and communication plan

May 31
├─ All: Extended artifacts if needed
├─ All: Final steering review
└─ Sign-off: Ready for planning phase
```

---

## Next Steps After Bootstrap

Once bootstrap artifacts are complete and approved:

1. **Move to Planning Phase** (Month 2)
   - Detailed requirements
   - Technical design
   - Refine backlog

2. **Create Extended Artifacts** (as needed)
   - RACI matrix
   - Communication plan
   - Architecture summary
   - Metrics framework
   - Detailed backlog
   - Project roadmap

3. **Phase Gate Review** (End of Month 3)
   - Readiness for delivery phase
   - Team readiness
   - Stakeholder alignment

---

## FAQ

**Q: What if the business case is weak?**  
A: Don't finalize the charter. Go back and ask for more clarity on business goal and value.

**Q: What if stakeholders disagree on scope?**  
A: Document the disagreement in the decision log. Have the sponsor make the call. Don't bury conflict.

**Q: How detailed should scope be?**  
A: Detailed enough that a developer knows what to build. Vague scope → project fails.

**Q: When do we do detailed requirements?**  
A: These artifacts are high-level. Detailed requirements come in planning/design phase.

**Q: Can I create these artifacts with an LLM?**  
A: Yes! See `../../SETUP.md` for the model-facing guide. But YOU still own grounding in source docs and final approval.

---

**Status:** Complete step-by-step guide  
**Last Updated:** May 28, 2026
