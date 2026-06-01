# DEMO-WALKTHROUGH: Complete Setup Guide

**Purpose:** End-to-end demonstration of the AI-PM Bundle setup process  
**Time Required:** 45-60 minutes to read + follow  
**Audience:** Anyone wanting to understand how to use the bundle  
**Outcome:** Understanding of how source docs become artifacts

---

## Overview

This walkthrough shows the complete journey from project initiation through bootstrap artifact creation for a realistic software development project.

**Project Scenario:**
- **What:** AI-Powered Compliance Dashboard (SaaS web app)
- **Who:** RegTech Finance Inc. (customer) + TechBuild Solutions (delivery)
- **Goal:** Automate compliance monitoring, reduce costs, mitigate regulatory risk
- **Timeline:** 6 months to MVP launch

---

## The Five Phases of This Demo

```
Phase 1: Preparation         (Read business case, understand scenario)
    ↓
Phase 2: Workspace Setup     (Create project-config.yaml, folders)
    ↓
Phase 3: Create Artifacts    (Charter, Scope, Risks, Logs)
    ↓
Phase 4: Validate & Review   (Steering committee sign-off)
    ↓
Phase 5: Next Steps          (What happens next)
```

---

## Phase 1: Preparation (5 minutes)

### What You're Setting Up

**The Business Context:**
RegTech Finance Inc. manually reviews 10,000+ transactions daily for compliance. The process is:
- Expensive: 4 analysts at $120K each = $480K/year
- Slow: Takes 3-5 days to generate regulatory reports
- Error-prone: ~2% error rate
- Unscalable: Can't grow without proportional staffing

**The Solution:**
Build a web-based compliance dashboard that:
- Automatically flags suspicious transactions using configurable rules
- Generates regulatory reports in 2-4 hours (not 3-5 days)
- Maintains 99%+ accuracy (vs. 98% current)
- Scales to 5x transaction volume without more analysts

**The Business Value:**
- Save $360K annually (reduce to 1 analyst)
- Improve accuracy and audit readiness
- Enable growth without compliance bottleneck
- ROI: 16% in Year 1, payback in 10 months

### Where to Find Information

The source documents are in `sources/`:
- `business-case.md` - Business justification, ROI, success criteria
- `stakeholder-list.md` - Key people and engagement strategy
- (In real projects: market analysis, technical proposal, requirements, etc.)

### Key Players

**Customer Organization (RegTech Finance Inc.):**
- John Martinez (CFO) - Executive sponsor
- Sarah Chen (CCO) - Project sponsor, defines compliance requirements
- Michael Torres (VP Operations) - Business owner
- David Kim (CIO) - Technical sponsor
- Lisa Park + team (Compliance Analysts) - End users

**Delivery Organization (TechBuild Solutions):**
- Sarah Williams - Project Manager
- Dr. Marcus Bennett - Solution Architect
- Alex Johnson - Technical Lead
- Maria Gonzalez - QA Lead

---

## Phase 2: Workspace Setup (5 minutes)

### Creating the Project Instance

A "project instance" is your local workspace for this specific project.

**Structure:**
```
examples/demo-project/
├── project-config.yaml           # ← Entry point
├── sources/                       # Original project documents
│   ├── README.md                 # Catalog
│   ├── business-case.md
│   ├── stakeholder-list.md
│   └── (market analysis, technical proposal, etc.)
│
├── artifacts/                    # Generated PM artifacts
│   ├── project-charter.md
│   ├── scope-baseline.md
│   ├── risk-register.csv
│   ├── methodology-execution-log.md
│   ├── decision-log.md
│   └── (extended artifacts for planning phase)
│
└── documentation/                # Guides and tutorials
    ├── STEP-BY-STEP-GUIDE.md
    ├── FAQ.md
    ├── METHODOLOGY-EXTENSIONS.md
    └── LESSONS-LEARNED.md
```

**The Principle:**
- Bundle lives in: `../../ai-pm-bundle/` (shared, read-only reference)
- Project sources: `sources/` (ground truth for what's true)
- Generated artifacts: `artifacts/` (what we'll create)

### Configuration File

Open `project-config.yaml`:
```yaml
project_id: compliance-dashboard-demo
project_name: AI-Powered Compliance Dashboard
active_phase: initiation
bundle_path: ../../ai-pm-bundle
sources_path: sources
artifacts_path: artifacts
```

This tells the PM tooling where everything lives.

---

## Phase 3: Create Bootstrap Artifacts (35 minutes)

The AI-PM Bundle defines a **minimum viable set** of artifacts. Create them in this order.

### Artifact 1: Project Charter (5 min)

**Purpose:** Authorize the project, define its goal and success criteria

**Where to find information:**
- Business case → business goal, ROI, success factors
- Stakeholder list → who's involved, decision authorities

**What to include:**

| Section | Content |
|---------|----------|
| **Executive Summary** | Project will automate compliance monitoring, reduce costs by $360K/year, improve accuracy to 99%+ |
| **Scope** | MVP: Dashboard, rules engine, reports. Phase 2: ML, analytics |
| **Success Criteria** | 99%+ accuracy, 2-4 hour reports, 90%+ auto-processing, 99.5% uptime |
| **Stakeholders** | CFO (sponsor), CCO (owner), CIO (technical authority) |
| **Governance** | Monthly steering committee, CCO owns scope decisions |
| **Timeline** | 6 months to MVP, Nov 30 target |

**Key principle:** Extract from sources, don't invent

**Output:** `artifacts/project-charter.md`

---

### Artifact 2: Scope Baseline (5 min)

**Purpose:** Define what IS and ISN'T included

**In Scope (MVP):**
- Real-time transaction monitoring
- Configurable rule engine
- Dashboard with metrics
- Regulatory report generation
- User/role management
- Audit logging
- Integration with existing systems

**Out of Scope (Future):**
- Machine learning anomaly detection
- External data feeds
- Mobile app
- Multi-language

**Constraints:**
- Budget: $594K
- Timeline: 6 months
- Technology: Use existing stack (Java, React, PostgreSQL)

**Key principle:** Make boundaries explicit so team knows what to build

**Output:** `artifacts/scope-baseline.md`

---

### Artifact 3: Risk Register (5 min)

**Purpose:** Identify and plan for what could go wrong

**Identified Risks:**

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Scope creep | High | High | Change control, freeze scope Week 4 |
| Integration complexity | Medium | High | Early arch review, prototype Week 2 |
| User resistance | Medium | Medium | Analyst involvement, training plan |
| CIO security concerns | Low | High | Security-first architecture |
| Regulatory changes | Low | High | Flexible rule engine design |

**Key principle:** Realistic risks with concrete mitigations, not vague "hope and pray"

**Output:** `artifacts/risk-register.csv`

---

### Artifact 4: Methodology Execution Log (5 min)

**Purpose:** Audit trail of what was done when

**What to record:**

| Date | Activity | Owner | Status |
|------|----------|-------|--------|
| May 28 | Initial setup | PM | Complete |
| May 28 | Create charter | PM | Complete |
| May 28 | Create scope | PM | Complete |
| May 28 | Create risks | PM | Complete |
| May 29 | Steering review | PM | Pending |

**Key principle:** Shows how the project was set up methodically, not ad-hoc

**Output:** `artifacts/methodology-execution-log.md`

---

### Artifact 5: Decision Log (5 min)

**Purpose:** Record key decisions and their rationale

**Key Decisions:**

| Decision | Rationale | Date | Status |
|----------|-----------|------|--------|
| MVP Scope Frozen | Focus Phase 1 on core; ML → Phase 2 | May 28 | Approved |
| Hybrid Model | Agile dev, waterfall compliance gates | May 28 | Approved |
| Phase Gate Month 3 | Stop-go before full delivery ramp | May 28 | Approved |

**Key principle:** Prevents "I thought we decided..." conflicts later

**Output:** `artifacts/decision-log.md`

---

## Phase 4: Validate & Review (10 minutes)

### Quality Checks

Before finalizing, ask:

✅ **Grounding:** Can I trace each statement back to a source document?  
✅ **Completeness:** Are critical decisions documented? Are assumptions explicit?  
✅ **Clarity:** Would a new team member understand this?  
✅ **Realism:** Can the team actually achieve these criteria?  

### Steering Committee Review

Present the artifacts:

**For CFO:**
> "Here's the charter. Does this capture the business goal? Is the ROI realistic? Do you approve this as the authorizing document?"

**For CCO:**
> "Here's the scope. Is this the MVP you wanted? Are the success criteria achievable? Any concerns?"

**For CIO:**
> "Here's the technical scope and risks. Are the integration points clear? Do you see any technical blockers?"

### Red Flags (Stop and Ask)

🚩 **If charter goal is vague** → ask for clarification before approving  
🚩 **If scope has major gaps** → research or ask, don't guess  
🚩 **If risks seem incomplete** → identify more or increase monitoring  
🚩 **If stakeholders disagree** → document disagreement, let sponsor decide

---

## Phase 5: Next Steps

Once bootstrap is approved:

### Immediate (Week 2-3)
- [ ] Steering committee formally approves charter and scope
- [ ] Begin planning phase
- [ ] Start detailed requirements and design
- [ ] Identify specific technical architecture
- [ ] Create detailed backlog

### Short-term (Month 2)
- [ ] Create extended artifacts:
  - RACI matrix (who decides what)
  - Communication plan (how we stay aligned)
  - Architecture summary (technical design)
  - Metrics framework (how to measure success)
  - Detailed backlog (what to build first)
  - Roadmap (timeline and phases)

### Month 3 Gate Review
- [ ] Planning phase complete?
- [ ] Team mobilized and ready?
- [ ] Stakeholder aligned?
- [ ] Go/no-go decision for delivery phase

### Month 4+ (Delivery Phase)
- [ ] Development begins
- [ ] Keep execution log current
- [ ] Track risks in risk register
- [ ] Record decisions as made
- [ ] Monthly status reports

---

## How This Maps to the Bundle

### What This Demo Shows

✅ Project structure and configuration  
✅ How source documents become artifacts  
✅ Minimum viable bootstrap set  
✅ Quality over speed principle  
✅ Methodology execution tracking  
✅ Control artifacts (decision log, execution log)  

### What the Demo References

✅ `../../ai-pm-bundle/README.md` - Bundle overview  
✅ `../../ai-pm-bundle/SETUP.md` - Model-facing playbook (what to do)  
✅ `../../ai-pm-bundle/HUMAN-SETUP.md` - Operator guide (how to guide the model)  
✅ `../../ai-pm-bundle/templates/` - Artifact templates  
✅ `../../ai-pm-bundle/mappings/` - Activity to artifact mapping  

---

## Core Principles in Action

### Principle 1: Methodology as Guidance
"The methodology tells you HOW to run the project"
- We use the bundle templates and mappings
- We follow the artifact sequence
- We apply the methodology activities

### Principle 2: Source Documents as Truth
"Source documents tell you WHAT is true about the project"
- Everything traces back to business case, proposal, stakeholder list
- We extract rather than invent
- Gaps trigger questions, not assumptions

### Principle 3: Quality Over Speed
"Prefer fewer, better, evidence-grounded artifacts"
- 5 solid artifacts > 10 generic documents
- Better to say "we don't know yet" than make stuff up
- Keep control artifacts (logs) current

### Principle 4: Explicit Assumptions
"Missing information should trigger focused questions"
- Any guess is clearly marked as an assumption
- Assumptions get tracked in risk register or decision log
- We commit to validating assumptions soon

### Principle 5: Orchestrator Manages Flow
"The PM orchestrator ensures completeness, sequencing, consistency"
- Artifacts are created in defined sequence
- Each artifact is reviewed before moving on
- Execution log proves due diligence

---

## Common Questions

**Q: Can I skip the business case and go straight to building?**  
A: No. If the business goal is unclear, the project will fail or get expensive. Take time to understand why first.

**Q: What if the team doesn't agree on scope?**  
A: Document the disagreement in the decision log. Have the sponsor make the call. Don't hide conflict.

**Q: When do we do detailed requirements?**  
A: These bootstrap artifacts are high-level. Detailed requirements come during planning phase (Month 2).

**Q: Can I use this with an LLM?**  
A: Yes! See `../../SETUP.md` for the model-facing guide. The bundle is designed to work with AI assistants. But YOU still own final approval and quality.

**Q: How long does full setup take?**  
A: Bootstrap (5 artifacts): 4-6 hours with good sources  
Extended (11 artifacts): 2-3 additional days during planning phase

**Q: What if sources are missing?**  
A: Create DRAFT artifacts with assumptions clearly marked. Use the artifacts to drive the conversation: "Here's what I can infer. What are we missing?"

---

## Your Next Move

### Option A: Study the Demo Artifacts
1. Open `artifacts/project-charter.md` and read it
2. Compare to `sources/business-case.md` - see the traceability
3. Review `artifacts/decision-log.md` - notice how decisions are framed
4. Look at `sources/stakeholder-list.md` - see how it feeds RACI

### Option B: Create Your Own Project
1. Copy this `demo-project/` folder as a template
2. Rename for your project
3. Update `project-config.yaml` with your project details
4. Replace source documents with your real project docs
5. Follow `documentation/STEP-BY-STEP-GUIDE.md` to create artifacts

### Option C: Deep Dive into Bundle
1. Read `../../ai-pm-bundle/README.md`
2. Review `../../ai-pm-bundle/SETUP.md` (model guide)
3. Review `../../ai-pm-bundle/HUMAN-SETUP.md` (operator guide)
4. Check out templates in `../../ai-pm-bundle/templates/`
5. Study mappings in `../../ai-pm-bundle/mappings/`

---

## Timeline Summary

```
Today (May 28)
├─ Read this walkthrough         (30 min)
├─ Review source documents       (20 min)
├─ Study artifacts               (20 min)
└─ Understand the process        (TOTAL: ~70 min)

Next Steps
├─ Copy demo-project as template
├─ Update for your project
├─ Follow STEP-BY-STEP-GUIDE.md
└─ Create bootstrap artifacts (4-6 hours)
```

---

## Reference Guide

**Key Documents:**
- `project-config.yaml` - Workspace entry point
- `sources/` - Project source documents (ground truth)
- `artifacts/` - Generated PM artifacts
- `documentation/` - Guides and templates

**For More Help:**
- **Bundle overview:** `../../ai-pm-bundle/README.md`
- **Detailed artifact creation:** `documentation/STEP-BY-STEP-GUIDE.md`
- **Common questions:** `documentation/FAQ.md`
- **Advanced topics:** `documentation/METHODOLOGY-EXTENSIONS.md`

---

**Demo Status:** Complete  
**Last Updated:** May 28, 2026  
**Next:** Read `STEP-BY-STEP-GUIDE.md` for hands-on artifact creation
