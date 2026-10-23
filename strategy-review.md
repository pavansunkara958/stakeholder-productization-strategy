# Stakeholder Management & Productization Strategy Review

**Initiative:** Veridian IT Support Agent — internal AI assistant, post-pilot
**To:** Executive Committee · **From:** Delivery lead · **Date:** 22 October 2026
**Decision:** fund the move from project to internal product, on the operating model below

---

## 1 · The actual problem

The pilot worked: 1,180 tickets, 61% resolved without a human, zero unauthorized privileged
grants, CSAT 4.3 against a 3.6 baseline. Adoption since has been uneven, and the reflex
reading — "a change problem, send more comms" — is wrong and would waste the quarter.

Uneven adoption has **two causes in two populations**, needing opposite responses:

| Population | Behaviour | Cause | Wrong response |
|---|---|---|---|
| Corporate functions (EN) | high usage, high CSAT | in scope, works | — |
| Benelux / DACH (31% of staff) | near-zero usage | **the product has no Dutch or German** | awareness campaign |
| Service desk L1 | active scepticism | **manual escalation path; they absorb the failures** | "overcome resistance" |

The first needs product work. The second is a legitimate operational objection from the
dependency that makes the service viable. Neither is addressed by engagement.
**Diagnosing adoption resistance before engineering a response to it is the highest-leverage
item here** — Kotter's "remove obstacles" is routinely read as *remove the people
obstructing*, when the obstacle is a missing feature and an unbuilt integration.

---

## 2 · Stakeholder map

Influence and interest per PMI stakeholder analysis; the grid position determines engagement
intensity, not seniority.

| Stakeholder | Infl. | Int. | Expected benefit | Concern | Likely resistance | Position |
|---|---|---|---|---|---|---|
| **CIO** | High | High | cost down, visible AI win | overcommitting publicly | low — sponsor | **Manage closely** |
| **CFO / Finance BP** | High | Med | capacity released, €560k opportunity | benefit never lands; pilot numbers inflated | **med — demands re-baselined data** | Manage closely |
| **CISO** | **High** | High | fewer manual access changes; audit trail | privilege escalation via injection | **med — vetoes scope growth without controls** | **Manage closely** |
| **Head of Service Delivery** | High | High | queue relief | agent tickets land back on L1 half-solved | **high — owns the pain if it fails** | **Manage closely** |
| **Service desk L1 (≈60)** | **Med** | High | fewer repetitive resets | job security; worse tickets, not fewer | **high — passive, shown as non-referral** | **Keep satisfied — underweighted** |
| Business unit leads | Med | Med | staff unblocked faster | another unused tool | low–med | Keep informed |
| Employees | Low | High | 4.2h → under a minute | "a bot instead of help" | low, if the human exit is visible | Keep informed |
| HR Ops | Med | Low | channel reuse | AI messaging to 28k staff | low | Keep informed |
| Platform team | Med | Med | reusable runtime | unfunded support desk | medium | Keep satisfied |
| Works council (NL/DE) | **High** | Low | — | job impact of automation | **unknown — not consulted** | **Engage before expansion** |

**Service desk L1 is the most underweighted group here.** Low formal influence, decisive
informal influence: they are the escalation path, every failure arrives on their desk, and
they can quietly stop referring employees to the agent. Their resistance is rational — in
the pilot they absorbed the manual approval relay. A dependency with a cost, not an attitude
to fix.

**The works council holds a veto nobody has exercised.** Automation affecting Dutch and
German staff is consultable. Consulting them *before* the language expansion is scoped costs
a meeting; after, it costs the roadmap.

---

## 3 · Engagement plan

| Group | Approach | Owner | Cadence | Escalation | Success indicator |
|---|---|---|---|---|---|
| ExCo | 1-page written update, numbers only | Delivery lead | monthly | — | Q1 funding renewed without debate |
| CISO + security | review every scope change before build | Security architect | per change | CIO | zero scope changes reverted post-build |
| Service Delivery | working session, agenda set by **them** | Delivery lead | weekly | CIO | L1 referral rate > 40% by day 90 |
| **Service desk L1** | **floor time, not a town hall; 3 named reps in design reviews** | Service manager | fortnightly | Head of SD | **referrals rising, escalation complaints falling** |
| BU leads | per-unit adoption dashboard, self-serve | Delivery | monthly | Head of SD | ≥ 3 units request onboarding unprompted |
| Employees | in-tool only; no campaign | HR Ops | launch + week 4 | — | ≥ 45% cohort activation |
| Works council | formal consultation before DACH/Benelux | HR Ops | once, then as needed | CIO | written no-objection before build |

**The L1 row decides whether this scales.** Three named reps in design reviews turns the
loudest sceptics into the people who shaped it — and they find failure modes faster than the
delivery team, because they handle the tickets.

**No employee campaign, deliberately.** A tool that needs a campaign has an interface
problem. Success is that nobody had to be persuaded.

---

## 4 · Change and adoption scorecard

Prosci separates **individual** change metrics from **organizational** ones; both are here,
plus counter-metrics, because every row above the line can improve while the service gets
worse.

| # | Dimension | Metric | Target (day 90) | Source |
|---|---|---|---|---|
| 1 | Readiness | business units with named owner + comms slot | 100% of launch cohort | plan |
| 2 | Training | L1 staff completed escalation handling | ≥ 90% | LMS |
| 3 | Activation | cohort users with ≥ 1 session | ≥ 45% | telemetry |
| 4 | Usage | sessions per active user per month | ≥ 1.4 | telemetry |
| 5 | Feature adoption | % of sessions using in-scope intents | ≥ 80% | trace analysis |
| 6 | Proficiency | tasks completed without the human exit | ≥ 85% | trace analysis |
| 7 | Satisfaction | post-resolution CSAT | ≥ 3.6 | in-tool |
| 8 | Support volume | L1 tickets in in-scope categories | −25% vs baseline | ticket system |
| 9 | Process compliance | privileged changes with a verified approval token | **100%** | audit log |
| 10 | Realized value | capacity released (hours) | re-baselined, reported wk 8 | finance |

**Counter-metrics — equal weight, same dashboard panel:**

| Counter-metric | Threshold | Why it exists |
|---|---|---|
| **Reopen rate** (same user, same issue, < 48h) | < 8% | containment counts a *closed* ticket, not a solved one |
| **Escape-hatch rate** (user asks for a human mid-flow) | < 15% | usage up with escapes up means people are being funnelled, not served |
| **L1 referral rate** | > 40% | the honest measure of whether the service desk believes in it |
| **Routing-mix drift** | alarm on change | silent misrouting: error rate, latency and cost all *improve* when it happens |

**Row 9 is binary and non-negotiable.** 99% process compliance on privileged access changes
is a failed control, not a good score.

**Row 10 is deliberately unfilled.** The pilot's 61% was measured on volunteers; carrying it
into a business case would be a silent lie. It is re-baselined on a non-volunteer cohort and
reported at week 8 against the new figure. *A weaker number you trust beats a strong one you
cannot defend* — and it is the only thing that resolves the CFO's resistance in §2.

---

## 5 · Productization strategy

| | |
|---|---|
| **Target users** | employees with routine IT access needs — 1,200 at launch, 28,000 addressable |
| **Value proposition** | *Routine access problems resolved in under a minute, with no access control weakened.* The second clause is the product, not a caveat — it is why Security lets it scale |
| **MVP** | three intents: password reset (standard), group membership (non-privileged), catalogue software install |
| **Service boundaries** | **In:** those three, English, business-hours SLA. **Out:** MFA reset, privileged groups, hardware, VPN, non-English. **Never:** `remote_wipe`, P1 declaration — absent from the toolset, not gated |
| **Onboarding** | no training session; a 90-second video and one page of examples, in an existing channel |
| **Support** | T0 agent → T1 service desk → T2 approval review (0.5 FTE) → T3 platform. Token-verification failures bypass all of it to the SOC as P1 |
| **Governance** | Service owner: IT Service Delivery (scope, metrics, stop rule). Runtime: Platform. Scope changes need security review; model pinned, upgrades gated by a 24-case eval suite |
| **Funding** | **centrally funded 12 months, no chargeback** |
| **Operational risks** | three blocking integrations owned outside the project; single-region; entitlement staleness |

**Chargeback is the wrong instrument here, and it is the mistake internal platforms usually
make.** Per-ticket charging does three harmful things before the product is proven: it
creates an adoption barrier exactly where adoption is the goal, it makes the product optimize
for whoever pays rather than for value, and it loads a metering build onto a team already
carrying three blocking dependencies. Revisit at month 12, when the unit economics (€0.04 vs
€6.80) are defensible rather than projected.

**Roadmap:**

| Horizon | Scope | Gate |
|---|---|---|
| **Now** (0–90d) | 3 intents, 1,200 users, EN | the 90-day plan below |
| **Next** (3–6m) | Dutch + German (31% of staff); MFA reset with dual approval | works council no-objection; C1 proven in production for one full cycle |
| **Later** (6–12m) | VPN + device intents; self-service onboarding; multi-region | each needs its own pilot — an intent with no data is an assumption |

**MFA reset is sequenced after the language work despite being the larger containment win.**
It is the classic account-takeover vector. A control that works in staging is a control that
has not met real traffic, so it waits until the approval integration has run a full
production cycle.

---

## 6 · 90-day action plan

| Day | Action | Owner | Success | Blocking? |
|---|---|---|---|---|
| 0–7 | Diagnose the two adoption causes; stop the generic comms plan | Delivery | diagnosis accepted by ExCo | — |
| 0–14 | 3 named L1 reps seconded into design reviews | Service mgr | attending, raising defects | **Yes** |
| 0–21 | ServiceNow approval integration; SOC alarm on token failures | Platform | 20 approvals, no manual step | **Yes** |
| 0–21 | Entitlement sync ≤ 15 min, else KB public-tier only | Identity | 48h at target lag | **Yes** |
| 14–21 | After-hours drill; kill-switch rehearsal (< 60s) | Ops / Platform | on-call lead signs off | **Yes** |
| 21–25 | Go/no-go against 10 release criteria | Service owner | all gates green | **Yes** |
| **25** | **Launch — 1,200 users, 3 intents** | Delivery | — | — |
| 25–40 | **Re-baseline containment, non-volunteer cohort** | Delivery | new figure replaces 61% | **Yes (business case)** |
| 30–45 | Works council consultation before DACH/Benelux | HR Ops | written no-objection | **Yes (Next horizon)** |
| 40–60 | Reopen-rate + escape-hatch instrumentation | Delivery | same panel as containment | — |
| 45–75 | Language routing measured weekly | Delivery | 0 false negatives in 100 | — |
| 60 | Mid-point review: scorecard + counter-metrics | Service owner | kill or continue, explicitly | — |
| 75–90 | DACH scoping; CFO case on re-baselined data | Delivery / Finance | funding decision for Next | — |
| 90 | ExCo decision: scale, hold, or stop | ExCo | — | — |

**Stop rule, agreed in advance:** any unauthorized privileged grant, or CSAT below 3.6 for
two consecutive weeks, and the flag goes off — no meeting needed to authorise it. Agreeing
the stop condition while everyone is optimistic is what makes it usable later.

**Three of the four blocking items are owned by teams outside this project.** That is the
schedule risk; the engineering is understood.

---

## References

PMI stakeholder analysis · Prosci change metrics and ADKAR · Kotter 8-step change model ·
Harvard DCE product management lifecycle · Atlassian product development lifecycle.
Links in [README.md](README.md).
