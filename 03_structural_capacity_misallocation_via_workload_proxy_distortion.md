# Structural Capacity Misallocation via Workload Proxy Distortion



> All structural terms and notation are formally defined in Appendix B.


---

# PART I — EXECUTIVE CONTEXT

This case analyses a staffing allocation decision that was:

- mathematically correct,
- governance-approved,
- KPI-compliant,
- within formal review thresholds.

No arithmetic error occurred.

The imbalance emerged from workload dimensional insufficiency in the allocation driver.

Objective:

Demonstrate how a formally compliant staffing model can embed slow, governance-tolerated degradation.

---

# PART II — FORMAL REVIEW FRAMEWORK

## Review-Level Allocation Driver

Allocation rule:

fund_count × AIT_fund

Client A  
- 22 funds  
- AIT_fund_A = 57 min  

Client B  
- 18 funds  
- AIT_fund_B = 44 min  

Proxy workload:

A = 22 × 57 = 1,254  
B = 18 × 44 = 792  

Ratio A/B = 1.58  

Rounded allocation:

A → 2 FTE  
B → 1 FTE  

---

## Formal Review KPI Threshold

Governance tolerance band:

±30% variance in proxy workload per FTE

Proxy workload per FTE:

A = 1,254 / 2 = 627  
B = 792 / 1 = 792  

Variance relative to A:

(792 − 627) / 627 = 26.3%  

26.3% < 30% threshold  

Result:

Allocation formally within governance tolerance.

---

## Utilisation Reporting Framework

- Utilisation reported per team.
- No cross-client utilisation benchmarking during staffing review.
- No formal utilisation threshold linked to headcount decisions.
- Required_FTE not computed at review stage.

---

## Ageing Threshold

Formal backlog ageing breach threshold:

30 days open.

Volume drift below ageing breach does not trigger staffing escalation.

---

# PART III — STRUCTURAL PARAMETERS

Fixed structural assumptions:

- IW_structural = 360 min/day  
- DRC = (FTE × IW_structural) / AIT_break  
- ρ = DI / DRC  
- SM = DRC − DI  
- Backlog recurrence:

B(t+1) = B(t) + DI − DRC  

No stochastic modelling.  
No seasonality modelled.  
No feedback-loop AIT inflation modelled.

---

# PART IV — OPERATIONAL MEASUREMENT (BREAK LEVEL)

Observed steady-state parameters:

Client A  
- DI_A = 14 breaks/day  
- AIT_break_A = 42 min  

Client B  
- DI_B = 15 breaks/day  
- AIT_break_B = 30 min  

Break generation occurs at subfund / transaction level.

Fund aggregation does not preserve break-generation monotonicity.

---

# PART V — STRUCTURAL CAPACITY

## Client A

FTE_A = 2  

DRC_A = (2 × 360) / 42  
= 720 / 42  
= 17.14 breaks/day  

ρ_A = 14 / 17.14  
= 0.82  

SM_A = 17.14 − 14  
= +3.14  

Workload_minutes_A = 14 × 42  
= 588 min/day  

Per-FTE workload_A = 588 / 2  
= 294 min  

Utilisation_A = 294 / 360  
= 82%

Interpretation:

- Below structural saturation  
- Positive recovery window  
- Elevated utilisation without deficit  

---

## Client B

FTE_B = 1  

DRC_B = (1 × 360) / 30  
= 360 / 30  
= 12 breaks/day  

ρ_B = 15 / 12  
= 1.25  

SM_B = 12 − 15  
= −3  

Workload_minutes_B = 15 × 30  
= 450 min/day  

Per-FTE workload_B = 450 min  

Utilisation_B = 450 / 360  
= 125%

Structural deficit = 90 min/day  

Interpretation:

- Above structural capacity  
- No recovery window  
- Deterministic backlog drift  

---

# PART VI — REQUIRED CAPACITY

Required_FTE_B = 450 / 360  
= 1.25 FTE  

Allocated_FTE_B = 1  

Under-allocation = 0.25 FTE  

Daily structural deficit:

90 minutes  

---

# PART VII — BACKLOG DYNAMICS

Backlog recurrence:

B(t+1) = B(t) + DI − DRC

t = operational day index (discrete time step)

B(t) = backlog at day t

For Client B:

ΔB/day = 15 − 12  
= +3  

Monthly drift (20 working days):

+60 breaks  

6-month drift:

+360 breaks  

Embedded processing time:

360 × 30  
= 10,800 minutes  
= 180 hours  
= 30 FTE-days  

Volume drift persists without spike events.

---

# PART VIII — GOVERNANCE VISIBILITY GAP

At review layer:

- Proxy workload per FTE within ±30% band.
- Allocation formally compliant.
- No cross-client utilisation benchmarking requirement.
- No Required_FTE validation rule.
- No staffing trigger below 30-day ageing threshold.

At operational layer:

- Client B operates at 125% structural utilisation.
- Persistent ΔB = +3/day.
- Structural deficit = 0.25 FTE.

Because staffing validation relied on aggregated proxy  
and not on break-level capacity alignment,  

structural overload remained governance-compliant.

---

# PART IX — WORKLOAD DIMENSIONAL INSUFFICIENCY

The allocation driver:

fund_count × AIT_fund

- does not map to break-generation mechanism,
- does not preserve workload monotonicity versus DI,
- collapses operational variance at aggregated level.

Under fund aggregation:

Client A appears heavier.

Under operational measurement:

Client B exceeds structural capacity.

This is dimensional insufficiency in workload representation,  
not computational error.

---

# PART X — ROUNDING AMPLIFICATION

Continuous proxy ratio = 1.58  

Required_FTE_B = 1.25  

Rounded allocation = 1  

Rounding gap = 0.25 FTE  

Continuous proxy distortion  
→ discrete staffing asymmetry  

Dimensional insufficiency  
→ persistent structural deficit.

---

# PART XI — RISK TRANSLATION

Persistent structural deficit increases probability of:

- ageing threshold breach over time,
- review compression,
- SLA timing erosion,
- control fragility.

Backlog represents deferred processing and deferred validation exposure.

---

# PART XII — PRE-MORTEM CONTROL RULE

Before staffing sign-off, governance must require:

- DI per client  
- break-level AIT  
- Required_FTE validation  
- Structural margin (SM) calculation  
- Backlog slope (ΔB/day) assessment  

A workload driver is structurally invalid if:

- it misorders workload under finer granularity,
- it diverges materially from Required_FTE,
- it permits persistent ΔB > 0 under steady-state conditions.

---

# PART XIII — MODEL SCOPE

Deterministic first-order structural model.

Fixed structural baseline:

- IW_structural = 360 min/day  

No probabilistic queue modelling.

Purpose:

Identify slow structural degradation caused by workload dimensional insufficiency  
before escalation into visible operational instability.
---
