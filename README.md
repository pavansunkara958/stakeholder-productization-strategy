# Stakeholder Management & Productization Strategy Review

**Initiative:** Veridian IT Support Agent — an internal AI assistant that has completed a
six-week pilot with good technical results and uneven enterprise adoption.
**Question:** how does this move from project delivery to scalable organizational value?

## → [**strategy-review.md**](strategy-review.md) ←

**The deliverable.** A strategy memo covering all five required areas. **2,100 words total**,
of which ~700 is narrative and ~1,400 sits inside eight tables — the brief asks for a
stakeholder matrix, a metric table *and* a 90-day plan, and those three alone carry most of
the count. The argument is in the prose; the tables are the evidence it rests on.

| § | Covers | Required artifact |
|---|---|---|
| 1 | Diagnosis — why adoption is uneven | |
| 2 | Stakeholder map: influence, interest, benefits, concerns, resistance | **stakeholder matrix** |
| 3 | Engagement plan: approach, owner, cadence, escalation, success indicator | |
| 4 | Change & adoption scorecard — 10 dimensions plus 4 counter-metrics | **adoption metric table** |
| 5 | Productization strategy: users, value prop, MVP, boundaries, onboarding, support, governance, funding, roadmap, risks | roadmap |
| 6 | Prioritized 90-day action plan | **90-day plan** |

Everything is in that one file — no supporting documents to chase.

---

## The three arguments it makes

### 1 · Uneven adoption is a diagnosis, not a comms problem

The reflex response to patchy adoption is an awareness campaign. Here that would waste the
quarter, because the two non-adopting populations have unrelated causes: 31% of staff get
near-zero value because **the product has no Dutch or German**, and the service desk is
sceptical because **they absorb the failures of a manual escalation path**. One needs
product work. The other is a legitimate operational objection from the dependency that makes
the service viable.

Kotter's "remove obstacles" step is routinely read as *remove the people obstructing*. In
this case the obstacle is a missing feature and an unbuilt integration.

### 2 · The most important stakeholder is the one with the least formal influence

Service desk L1 sits mid-grid on the PMI matrix and is the group that decides whether this
scales. They are the escalation path, so every failure arrives on their desk, and they can
quietly stop referring employees to the agent — resistance that never appears as an
objection in any meeting, only as a flat usage curve.

The engagement plan handles them with floor time and **three named reps seconded into design
reviews**, not a town hall. They find failure modes faster than the delivery team because
they handle the tickets.

### 3 · The headline number is the one to distrust first

Pilot containment was 61% against a 55% target — measured on an **opt-in** cohort. It
appears in the scorecard with its value deliberately unfilled, pending a re-baseline on a
non-volunteer population in days 25–40.

Reporting a weaker number you can defend is also the only thing that resolves the CFO's
resistance, which is itself rational: she has seen pilot figures fail to survive contact with
general release before.

**And the counter-metrics carry equal weight.** Containment counts a *closed* ticket, not a
solved one — so reopen rate and escape-hatch rate sit on the same dashboard panel, not in an
appendix. Process compliance on privileged access (row 9) is binary: 99% is a failed control,
not a good score.

---

## One recommendation worth flagging

**Central funding for 12 months, no chargeback.** Per-ticket chargeback is the instinctive
answer for an internal platform and the wrong one before the product is proven: it creates an
adoption barrier exactly where adoption is the goal, it makes the product optimize for
whoever pays rather than for value, and it loads a metering build onto a team already
carrying three blocking dependencies. Revisit at month 12, when €0.04 against €6.80 is
defensible rather than projected.

---

## Frameworks used

| Framework | Where it does work |
|---|---|
| **PMI stakeholder analysis** | §2 — influence/interest grid sets engagement intensity, not seniority |
| **Prosci change metrics** | §4 — individual-level and organizational-level metrics kept distinct |
| **Prosci ADKAR** | §5 — onboarding staged with one measurable signal per stage |
| **Kotter 8-step** | §1 — "remove obstacles", read correctly |
| **Product lifecycle** (Harvard DCE / Atlassian) | §5 — Now / Next / Later horizons, each gated by evidence |

- https://www.pmi.org/learning/library/stakeholder-analysis-pivotal-practice-projects-8905
- https://www.prosci.com/blog/metrics-for-measuring-change-management
- https://www.kotterinc.com/methodology/8-steps/
- https://professional.dce.harvard.edu/blog/what-does-the-product-management-lifecycle-look-like/
- https://www.atlassian.com/agile/product-management/product-development

---

*Veridian Group is a composite enterprise used across this course. Figures are illustrative
and internally consistent with the pilot evidence in the companion stakeholder-demo
repository.*
