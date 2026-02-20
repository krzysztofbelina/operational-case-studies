# Deterministic Structural Instability in Daily NAV Reconciliation  
### Governance Failure in Capacity Planning and Automation Sequencing  



> All structural terms and notation are formally defined in Appendix A.


---

# PART I — GOVERNANCE ANALYSIS  

## Executive Diagnosis  

This case documents a structurally unstable operating model in a regulated daily NAV reconciliation environment.

The failure was not technical.  
It was not behavioural.  
It was not caused by insufficient effort.

It was a **capacity stability violation tolerated at governance level**.

Automation did not create the instability.  
It accelerated and exposed an already negative structural margin.

The system operated for a prolonged period with:

- Average inflow exceeding structural capacity  
- Overtime institutionalised as pseudo-capacity  
- No formal stability metric (ρ)  
- No hard release gate tied to capacity conditions  
- No quantitative assessment of tool-induced service time elasticity  

The outcome was not a tool failure.

It was a **capacity breach materialisation event** that forced recapitalisation through emergency headcount expansion.

---

## Governance Failure Points  

### 1️⃣ Capacity Condition Was Never Defined

No formal stability constraint existed such as:

> ρ ≤ 1 (or ≤ 0.9 with volatility buffer)

Instead, the primary KPI was:

> NAV delivered on time.

As long as output remained green, structural instability was tolerated.

This is a classic control design flaw:
output metric substituted for system stability metric.

---

### 2️⃣ Overtime Was Treated as Capacity

Overtime was permanent, not exceptional.

~10 hours per day became standard.
Only 4 days per month were non-overtime.

This converted:

- Human buffer  
into  
- Structural dependency.

Governance implicitly accepted:

> ρ > 1 (without overtime)

as normal.

This eliminated recovery window.

---

### 3️⃣ Automation Sequencing Error

The tool was mandatory.
It increased Average Investigation Time (AIT) from:

30 minutes → 45 minutes (+50%)

Automation was introduced while:

- Structural margin < 0  
- Backlog already persistent  
- No recovery window existed  

This sequencing ensured that service-time increase would immediately deepen instability.

---

### 4️⃣ No Quantified Stability Gate

No one calculated:

- Daily Resolution Capacity (DRC)
- Utilisation ratio (ρ)
- Structural Margin (SM)
- Overtime-equivalent FTE burn

Deployment occurred without numerical veto condition.

This is not an execution flaw.

It is a governance design omission.

---

# PART II — MATHEMATICAL MODEL  

## 1️⃣ Structural Definitions  

DI = Daily Inflow (breaks/day)  
AIT = Average Investigation Time (minutes/break)  
IW = Investigation Window (minutes/day/FTE)  
DRC = Daily Resolution Capacity (breaks/day)  
ρ = Utilisation Ratio = DI / DRC  

FTE equivalence calculations use **observed effective working time (10h/day)** rather than contractual 8h baseline.

---

## 2️⃣ Baseline Parameters  

Effective makers: 9.5 FTE  

Structural IW: 360 min/day  
Observed overtime IW: 450 min/day  

AIT baseline: 30 min  
AIT post-tool: 45 min  

DI baseline: 150–160 breaks/day  
Spike DI: 500 breaks/day  

---

## 3️⃣ Structural Capacity (Pre-Tool)  

Breaks per FTE:

360 / 30 = 12  

DRC_structural:

9.5 × 12 = 114/day  

Utilisation:

150–160 / 114 = 1.32–1.40  

Steady-state instability confirmed.

---

### With Overtime  

450 / 30 = 15  

9.5 × 15 = 142.5/day  

150–160 / 142.5 = 1.05–1.12  

Even with permanent overtime, ρ > 1.

No recovery capacity existed.

---

## 4️⃣ Structural Margin  

SM = DRC_structural − DI  

114 − 150 = −36  
114 − 160 = −46  

Negative structural margin persisted daily.

---

## 5️⃣ Post-Tool Capacity  

360 / 45 = 8  

9.5 × 8 = 76/day  

450 / 45 = 10  

9.5 × 10 = 95/day  

Utilisation post-tool:

150–160 / 95 = 1.58–1.68  

Instability materially deepened.

---

## 6️⃣ Overtime Financial Distortion  

Overtime hours per month:

9.5 FTE × 2h × 22 days = 418 hours  

Equivalent FTE:

418 / 160 ≈ 2.6 FTE  

The system consumed the equivalent of 2.6 additional FTE  
without formal hiring.

---

## 7️⃣ Tool-Induced Capacity Destruction  

AIT increase: +15 minutes  

150 breaks × 15 min = 2250 minutes/day  

= 37.5 hours/day  

FTE equivalent:

37.5 / 10 ≈ 3.75 FTE  

Automation destroyed capacity equivalent to ~3.75 FTE per day.

---

## 8️⃣ Backlog as Frozen Throughput  

Backlog: 600 breaks  

600 × 45 = 27,000 minutes  

= 450 hours  

450 / 10 = 45 FTE-days  

Backlog is not a count.  
It is frozen productive capacity.

---

## 9️⃣ Spike Stress  

Pre-tool with overtime:

500 / 142.5 = 3.51  

Post-tool:

500 / 95 = 5.26  

Single spike injects:

500 − 95 = 405 backlog units  

Two spike days:

+810 backlog  

No recovery window possible.

---

## 🔟 Stability Condition  

System stable iff:

ρ ≤ 1  
AND  
Backlog(t+1) ≤ Backlog(t)

Observed:

ρ > 1 (persistent)  
Backlog increasing  

Structural instability confirmed.

---

# PART III — GOVERNANCE CONSEQUENCES  

## What Actually Happened  

1. System operated below structural stability headcount  
2. Overtime masked deficit  
3. Tool increased service time  
4. Capacity dropped further  
5. Backlog accelerated  
6. Review compressed  
7. Operational stress intensified  
8. Team attrition occurred  
9. Emergency headcount expansion: 10 → 16  

This was not collapse in a binary sense.

It was a **forced recapitalisation triggered by prolonged structural instability**.

---

## Final Governance Insight  

The critical failure was not tool quality.

It was the absence of a stability gate.

Automation was deployed into a system already violating:

> DI ≤ DRC

Time constraints in high-volume regulated operations are non-negotiable.

When arithmetic constraints are ignored,
the system will not fail morally.

It will fail mechanically.
