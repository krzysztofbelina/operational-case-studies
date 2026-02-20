# Case Template — Structural Governance Failure Analysis

This template standardises all case studies in this repository.

Each case must focus on:
- structural conditions,
- decision sequencing,
- stability constraints,
- and cost implications.

No storytelling.  
No personalisation.  
No tool debates.

---

# 1️⃣ Executive Diagnosis

1–2 short paragraphs.

State clearly:

- What structurally failed?
- Under what capacity condition?
- Why the failure was deterministic (not accidental)?

Frame failure as:
- stability violation,
- capacity breach,
- sequencing error,
- incentive distortion.

Avoid emotional or behavioural explanations unless structurally relevant.

---

# 2️⃣ Operating Environment

Briefly define:

- Industry context (regulated, audit-facing, high-volume, etc.)
- Operating model (e.g., maker–checker)
- Volume characteristics (baseline vs spike)
- Structural constraints (time, headcount, SLA, control layers)

Keep tight. Only constraints that matter mathematically.

---

# 3️⃣ Structural Stability Condition

Define explicitly:

- DI (Daily Inflow)
- AIT (Service Time)
- IW (Investigation Window)
- Effective FTE
- DRC (Daily Resolution Capacity)
- ρ = DI / DRC
- Structural Margin (SM)

State:

- Was ρ ≤ 1?
- Was structural margin positive?
- Did a recovery window exist?

This section anchors the case in deterministic logic.

---

# 4️⃣ Governance Decision Points

List 2–4 structurally decisive decisions.

For each:

### Decision #X — *Short Structural Title*

Explain:

- What was decided?
- What stability condition was ignored?
- What quantitative constraint was not evaluated?

**Structural Impact**
- Effect on DRC
- Effect on ρ
- Effect on backlog dynamics
- Effect on control integrity

Focus on decision logic, not individuals.

---

# 5️⃣ Sequencing Analysis (If Applicable)

If automation, transformation, or redesign was involved:

Clarify:

- Was the system stable before change?
- Did service time increase or decrease?
- Was margin restored before introducing friction?
- Was there a formal release gate tied to capacity sufficiency?

Explicitly state whether sequencing respected or violated:

> DI ≤ DRC

---

# 6️⃣ Backlog and Control Dynamics

Explain mechanically:

- Backlog(t+1) = Backlog(t) + (DI − DRC)
- Review demand vs review capacity
- Where compression occurred
- How control degradation emerged

Avoid blame language.

Focus on system behaviour under load.

---

# 7️⃣ Financial Translation (Order-of-Magnitude)

Translate structural distortion into economic impact.

Examples:

- Overtime-to-FTE equivalence
- Capacity destruction due to service-time expansion
- Backlog converted into FTE-days
- Recurring structural subsidy
- Forced recapitalisation

Quantify where structurally necessary.
Avoid precise salary figures.

---

# 8️⃣ Governance-Level Diagnosis

Clarify:

- Which metric substituted for stability?
- What KPI masked instability?
- Who absorbed hidden cost?
- What structural signal was ignored?

This section demonstrates judgment, not criticism.

---

# 9️⃣ Structural Outcome

Describe objectively:

- Was recapitalisation required?
- Did headcount expand?
- Did controls weaken?
- Did audit pressure increase?
- Did attrition occur?

Avoid the word "collapse" unless literal system failure occurred.

Prefer:

- instability materialisation,
- forced recapitalisation,
- capacity breach event,
- structural correction phase.

---

# 🔟 Transferable Insight

One short section answering:

- Why will this pattern repeat elsewhere?
- What early signal should governance monitor?
- What stability gate should exist before transformation?

Keep abstract and generalisable.

---

# Methodological Discipline

All cases must:

- Explicitly define structural variables.
- State stability condition (ρ).
- Distinguish structural capacity from overtime.
- Avoid personality-driven explanations.
- Avoid vendor or tool focus.
- Remain anonymised and non-attributive.

Optional:

If definitions are used, reference:

> See Appendix A — Structural Model Definitions & Stability Notation.

---

End of Template
