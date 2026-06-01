# Frequently Asked Questions

## General Questions

### Q: What is the AI-PM Bundle?
**A:** It's a portable, methodology-driven project management system designed to work with LLMs and human operators. It combines methodology guidance, reusable templates, mappings, and setup playbooks.

### Q: Why should I use it instead of my current approach?
**A:** The bundle:
- Ensures consistent PM practices across projects
- Works well with AI assistants (LLMs)
- Focuses on quality artifacts over speed/volume
- Provides clear methodology guidance
- Includes templates and mappings ready to use
- Emphasizes source-grounded decisions

### Q: How is this different from Agile/Scrum/Waterfall?
**A:** The bundle is methodology-agnostic. It can work with agile, waterfall, hybrid, or custom approaches. It focuses on the PM practice layer (how to organize knowledge) rather than the delivery method layer.

### Q: Can I use this for non-software projects?
**A:** Yes, with adaptation. The bundle is designed around Edhouse methodology which applies to various project types. You may need to customize templates and phases for your domain.

---

## Using the Demo Project

### Q: How should I use this demo-project?
**A:** Three ways:
1. **Learn:** Study the demo to understand the bundle
2. **Template:** Copy it as a starting point for your project
3. **Reference:** Come back to it when you need examples

### Q: Can I modify the demo project?
**A:** Yes, but keep a copy of the original. The demo is designed as a reference and template.

### Q: What if my project is different from the demo?
**A:** The process is the same even if the domain is different:
1. Gather source documents
2. Create project configuration
3. Follow the artifact sequence
4. Keep control logs

---

## Creating Artifacts

### Q: How long does bootstrap setup take?
**A:** 
- With good source documents: 4-6 hours
- With weak/missing sources: 8-10 hours (much of it asking for clarification)
- Full project setup (bootstrap + extended): 2-3 weeks during initiation/planning

### Q: Do I have to create artifacts in the recommended order?
**A:** The recommended order minimizes rework:
1. Charter (defines project)
2. Scope (defines what to build)
3. Risk (identifies blockers)
4. Execution log (tracks what we did)
5. Decision log (records key decisions)

But you can adapt based on your needs.

### Q: What if source documents are missing or weak?
**A:** 
1. Mark artifacts as DRAFT
2. Explicitly list missing information
3. Use artifacts to drive conversation ("Here's what I inferred. What are we missing?")
4. Don't guess or invent

### Q: How detailed should the charter be?
**A:** 2-3 pages usually:
- Executive summary (1 page)
- Scope overview (1/2 page)
- Success criteria (1/4 page)
- Stakeholders/governance (1/2 page)
- Assumptions (1/4 page)

If it's longer, you're adding detail that belongs in other artifacts.

### Q: When is scope "good enough"?
**A:** When:
- In-scope items are specific (not vague)
- Out-of-scope items are explicit
- Constraints are documented
- A developer could start building from this
- Stakeholders agree on MVP boundaries

---

## Using with LLMs

### Q: Can I have an LLM create these artifacts?
**A:** Yes, if you:
- Provide good source documents
- Use the bundle's SETUP.md playbook
- Review and validate LLM output
- Own final approval

### Q: How do I get a good result from an LLM?
**A:** 
1. Upload source documents first
2. Instruct the LLM to use the bundle
3. Ask for one artifact at a time
4. Review for source grounding before proceeding
5. Ask follow-up questions if gaps appear

See `../../SETUP.md` and `../../HUMAN-SETUP.md` for detailed guidance.

### Q: How much does the LLM help?
**A:** It accelerates:
- Extracting information from sources
- Organizing thoughts
- Drafting documents
- But YOU must:
- Verify source grounding
- Validate stakeholder alignment
- Approve final artifacts

---

## Methodology & Adaptation

### Q: Can I adapt the methodology for my context?
**A:** Yes. The bundle is extensible:
- Add custom phases
- Create project-specific templates
- Modify artifact sequence if needed
- But keep the core principle: source-grounded, quality-first

See `documentation/METHODOLOGY-EXTENSIONS.md`

### Q: How do I handle a project that's already started?
**A:** 
1. Collect whatever artifacts exist
2. Gather source documents from the project
3. Create control artifacts (execution log, decision log) for historical actions
4. Use the bundle going forward
5. Document what was already done

### Q: What if stakeholders push back on the process?
**A:** 
1. Show them the demo project
2. Explain that this takes less time than fire-fighting
3. Commit to a compressed timeline for proof of concept
4. Use artifacts to show you're organized, not chaotic

---

## Common Challenges

### Q: What if the charter goal is still vague after reviewing sources?
**A:** Stop and ask:
- "What specific business problem does this solve?"
- "How will we know if we succeeded?"
- "What's the business value?"
Don't guess. Clarity on goal is non-negotiable.

### Q: What if scope keeps changing?
**A:** 
1. Use change control process
2. Freeze scope at a point (e.g., Week 4)
3. Put change requests into Phase 2
4. Document changes in decision log
5. Track scope creep in risk register

See `documentation/LESSONS-LEARNED.md` for scope management tips.

### Q: What if stakeholders disagree on priorities?
**A:** 
1. Document the disagreement in the decision log
2. Show both perspectives
3. Let the sponsor (CFO, executive) decide
4. Record the decision
5. Move forward with clarity

### Q: What if the team is small/remote?
**A:** The bundle works well for distributed teams:
- Written artifacts instead of unrecorded meetings
- Clear decision trails
- Asynchronous feedback
- Remote-friendly (no need to co-locate)

### Q: What if we're in a crisis and can't take time for this?
**A:** You're already in crisis. Taking 4-6 hours to create bootstrap artifacts:
- Prevents worse crises
- Aligns team
- Clarifies priorities
- Costs far less than firefighting

---

## Troubleshooting

### Q: My artifacts feel generic and unhelpful
**A:** 
1. Are they grounded in sources? (Or did you guess?)
2. Are they specific? (Or too vague?)
3. Did you involve stakeholders? (Or made decisions alone?)
4. Rework them focusing on specificity and grounding

### Q: Stakeholders won't read the artifacts
**A:** 
1. Make them shorter (2-3 pages max)
2. Add executive summaries
3. Present key decisions verbally
4. Use tables instead of prose
5. Highlight what matters to each stakeholder

### Q: We created artifacts but nothing changed
**A:** Artifacts are only useful if:
- You actually use them for decisions
- You reference them in meetings
- You update them when things change
- You hold team accountable to them

If not, they're just paperwork.

### Q: I don't know if we're done with bootstrap
**A:** You're done when:
- All 5 bootstrap artifacts exist
- Each is grounded in sources
- Steering committee approved
- No major open questions
- Execution log shows what was done
- Team is ready to move to planning phase

---

## Next Steps

### Q: What do I do after bootstrap is approved?
**A:** 
1. Move to planning phase
2. Create extended artifacts (RACI, communication plan, etc.)
3. Do detailed design and requirements
4. Create detailed backlog and roadmap
5. Prepare team for delivery phase

### Q: How do I keep the bundle up-to-date throughout the project?
**A:** 
1. Keep methodology execution log current (monthly)
2. Update decision log as decisions are made
3. Update risk register monthly
4. Keep other artifacts current as conditions change
5. Use artifacts to inform steering meetings

### Q: Can I use this bundle for program/portfolio management?
**A:** The demo shows single-project usage. For programs/portfolios:
- Apply the bundle at each project level
- Create program-level artifacts
- Use bundle to keep projects aligned
- Bundle is designed for flexibility here

See `documentation/METHODOLOGY-EXTENSIONS.md`

---

## Support & Resources

### Q: Where can I get more help?
**A:** 
- **Bundle overview:** `../../ai-pm-bundle/README.md`
- **Setup guide:** `../../ai-pm-bundle/SETUP.md` (for LLMs) or `../../HUMAN-SETUP.md` (for operators)
- **Detailed walkthrough:** `DEMO-WALKTHROUGH.md`
- **Artifact creation:** `STEP-BY-STEP-GUIDE.md`
- **Methodology:** `../../ai-pm-bundle/methodology/`
- **Templates:** `../../ai-pm-bundle/templates/`

### Q: Is there a community/support channel?
**A:** Check:
- GitHub discussions in the repo
- Methodology documentation in bundle
- Example projects (this demo)

### Q: How do I report issues or suggest improvements?
**A:** Open a GitHub issue in the `gajdosLGaEdhouse/AI-PM` repository with:
1. What you were trying to do
2. What happened
3. What you expected
4. Screenshots or examples if helpful

---

**Last Updated:** May 28, 2026  
**Status:** Comprehensive FAQ
