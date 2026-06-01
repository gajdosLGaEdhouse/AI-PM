# Lessons Learned: Tips, Tricks, and Gotchas

**Purpose:** Practical wisdom from setting up the Compliance Dashboard project  
**Audience:** PMs setting up similar projects  
**Status:** Recommended reading after completing bootstrap

---

## Key Insights from This Project

### 1. Scope Creep is the #1 Risk

**What Happened:**
Initially, stakeholders wanted to include ML anomaly detection in MVP. This would have added 2-3 months and $150K.

**What We Did:**
- Froze scope by Week 4
- Explicitly deferred ML to Phase 2
- Used change control process
- Tracked scope creep as active risk

**Takeaway:**
Scope clarity is the best defense against creep. Write down what's OUT of scope as explicitly as what's in scope.

---

### 2. Getting Stakeholder Alignment Early Saves Months

**What Happened:**
We spent Week 1 getting all stakeholders to agree on success criteria. It felt slow at the time.

**What We Discovered:**
Without that alignment, every deliverable would have triggered 2-3 weeks of disagreement.

**Takeaway:**
Spend time on the charter and scope while stakeholders are available. Delays here save delays later.

---

### 3. Source Documents Must Be Current

**What Happened:**
We used an outdated proposal that didn't reflect recent regulatory changes. We found out in Week 3.

**Fix:**
We had to update scope and re-validate with stakeholders.

**Takeaway:**
Before creating artifacts, verify that source documents are current. Ask: "When was this last updated? Has anything changed?" If unsure, ask for a refresh.

---

### 4. Write Down Assumptions, Don't Hide Them

**What Happened:**
We assumed the legacy system integration would be straightforward. The CIO reviewed the plan and said "Actually, that system is being decommissioned."

**Result:**
We had to revise architecture, but caught it before development started.

**Takeaway:**
Always list assumptions explicitly in scope baseline. Have the technical owner review them. Hidden assumptions become project killers.

---

### 5. Decision Log Prevents "I Thought We Decided" Conflicts

**What Happened:**
In Month 2, VP Operations said "I didn't realize we were doing hybrid delivery." But it was clearly in the charter.

**Fix:**
We pointed to the decision log, showed when the decision was made, who approved it, and the rationale.

**Takeaway:**
Decision log is not bureaucracy—it's documentation. It prevents weeks of re-fighting old battles.

---

### 6. Risk Register Should Evolve, Not Stay Static

**What Happened:**
We created the risk register in Week 1, then ignored it for 6 weeks.

**Result:**
We hit a risk (CIO security concerns) that we'd identified but hadn't actively managed.

**Takeaway:**
Update risk register monthly. Move managed risks to lower priority. Add new risks as they emerge. Use it in steering meetings.

---

### 7. Execution Log Builds Trust

**What Happened:**
In a steering meeting, the CFO asked "Are we following the methodology or just making stuff up?"

**What Saved Us:**
We showed the execution log. Every artifact, every decision, every activity was documented with dates and owners.

**Takeaway:**
The execution log shows discipline and due diligence. It's powerful in steering committees and audits.

---

## Tips for Success

### Tip 1: Use Meetings to Review, Not Create

**Wrong Way:** Stakeholders in a meeting trying to write the charter together.
**Result:** 4 hours of rambling, no decision, scheduling next meeting.

**Right Way:** PM drafts charter from sources. Present to stakeholders. "Does this look right?" "Any concerns?" "Approved?"
**Result:** 30 minutes, clear output, decision made.

**Lesson:** Write artifacts between meetings. Use meetings to validate and decide.

---

### Tip 2: Charter Should Be Concise

**Wrong:** 15-page charter with every detail
**Result:** Nobody reads it

**Right:** 2-3 page charter with clear sections
**Result:** Leadership reads it, understands it, approves it

**Lesson:** Concise wins. Detail goes in other artifacts (scope, architecture, backlog).

---

### Tip 3: Get Technical Review of Scope

**What We Did:**
We had the Solution Architect review scope baseline.

**What She Found:**
- Feature X was technically infeasible (timeline constraint)
- Feature Y had hidden integration complexity
- Feature Z should be easier than we thought

**Result:** Scope was more realistic, timeline was more accurate.

**Lesson:** Scope needs both business AND technical review. Gaps emerge from technical perspective.

---

### Tip 4: Risk Register Needs an Owner

**Wrong:** PM creates risk register, nobody looks at it
**Result:** Risks happen anyway

**Right:** Assign risk owners. Have them update status monthly. Report in steering meetings.
**Result:** Risks are actively managed, not surprises

**Lesson:** A risk without an owner will be ignored.

---

### Tip 5: Use Change Control From Day 1

**What We Did:**
When stakeholders requested scope changes, we didn't say "No."

We said "Let's log this as a change request. We can evaluate it at the Month 3 gate. For now, it stays out of scope."

**Result:** 
- Scope stayed stable
- No conflict about what's in/out
- Month 3 gate: We approved 2 important changes and deferred others

**Lesson:** Change control is not a blocker, it's a decision-making process. Use it from day 1.

---

### Tip 6: Communicate the Plan Early and Often

**What We Did:**
After charter approval, we sent a one-page summary to all stakeholders:
- "Here's what we're building (summary)"
- "Here's why (business goal)"
- "Here's the timeline"
- "Here's how you'll stay involved"

**Result:** 
- Fewer surprises
- More aligned stakeholders
- Fewer mid-project pivots

**Lesson:** Over-communicate the plan. Brief email > no communication.

---

## Gotchas to Avoid

### Gotcha 1: "We Can Detail That Later"

**The Problem:**
When scope is vague, people say "We'll detail that during design."

**Why It's a Gotcha:**
You start design with unclear scope → team builds the wrong thing → rework → delay.

**Prevention:**
Spend extra time on scope now. Get specific. If you can't be specific, it means you're missing information.

---

### Gotcha 2: Forgetting About Constraints

**The Problem:**
You create scope, then discover: "Oh, we have to use this technology" or "We only have 3 people" or "Budget is 40% less."

**Why It's a Gotcha:**
Constraints force scope cuts → mid-project re-planning → team loses confidence.

**Prevention:**
Identify constraints BEFORE finalizing scope. List them explicitly. Factor them into realistic scope.

---

### Gotcha 3: Stakeholder Disagreement on Scope

**The Problem:**
CCO wants Feature X. CTO says it's infeasible. CFO says it's too expensive.

**Why It's a Gotcha:**
Project proceeds without clarity → different people building different things → chaos.

**Prevention:**
Doc disagreements in decision log. Get sponsor to decide. Record decision. Move forward with clarity.

---

### Gotcha 4: Ignoring Risk Register

**The Problem:**
You identify risks but don't actively manage them.

**Why It's a Gotcha:**
Risks happen anyway, but you've already spent the budget/timeline. No mitigation options left.

**Prevention:**
Update risk register monthly. Actively manage high-risk items. Report in steering meetings.

---

### Gotcha 5: Artifacts Becoming Obsolete

**The Problem:**
You create the charter in May. By August, everything has changed, but you don't update it.

**Why It's a Gotcha:**
Artifacts become "that thing we wrote in May" instead of "our current reality."

**Prevention:**
Schedule artifact updates:
- After each phase gate
- When major decisions change scope/timeline
- Monthly for execution log and risk register
- Quarterly for others

---

## When to Use Each Artifact

### Project Charter
**Use When:**
- Kick off the project
- Present to executive stakeholder
- Onboard new team members
- Revisit project purpose (Month 3, Month 6)

### Scope Baseline
**Use When:**
- Planning what to build
- Evaluating change requests
- Onboarding developers
- Resolving "Is that in scope?" questions

### Risk Register
**Use When:**
- Weekly ops meeting (high risks)
- Monthly steering meeting (all risks)
- Planning mitigation activities
- Making go/no-go decisions

### Execution Log
**Use When:**
- Auditing how project was set up
- Learning what worked/didn't work
- End-of-project retrospective
- Showing discipline to stakeholders

### Decision Log
**Use When:**
- Explaining why we chose X over Y
- Revisiting old decisions
- Onboarding team members
- Steering meetings (what major decisions were made)

---

## What Worked Well

✅ **Weekly steering ops sync** - Kept leadership aligned, caught issues early  
✅ **Explicit scope boundaries** - Prevented most of the scope creep  
✅ **Risk register with owners** - Active management prevented surprises  
✅ **Documented decisions** - Prevented re-fighting old battles  
✅ **Monthly execution log update** - Showed progress and discipline  

---

## What We'd Do Differently

🔧 **Earlier technical review of scope** - Caught 2-3 feasibility issues later than ideal  
🔧 **More explicit integration assumptions** - Would have refined scope earlier  
🔧 **Stakeholder training on the process** - Could have gotten buy-in faster  
🔧 **Phase gate criteria defined upfront** - Had to improvise Month 3 gate  

---

## In Summary

The AI-PM Bundle works because it:

1. ✅ Forces clarity before building (no vague goals)
2. ✅ Grounds decisions in evidence (not guesses)
3. ✅ Manages stakeholder alignment (prevents chaos)
4. ✅ Creates audit trails (shows due diligence)
5. ✅ Scales from bootstrap to full project

Your success will depend on:

1. 📋 Getting good source documents
2. 🤝 Getting stakeholder involvement early
3. 📝 Keeping artifacts current throughout
4. 🎯 Using artifacts for actual decisions, not just paperwork
5. 🔄 Having discipline in the process

---

**Created:** May 28, 2026  
**Based on:** Compliance Dashboard project experience  
**Status:** Recommended reading
