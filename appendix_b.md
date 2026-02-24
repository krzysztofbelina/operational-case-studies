# Appendix B — Structural Definitions & Notation

This appendix defines all structural terms, variables, and operational concepts used in the case study.

The purpose of this document is clarity, auditability, and definitional discipline.

---

# 1️⃣ Core Operational Units

## FTE — Full-Time Equivalent

**Definition**

A unit representing one full-time operational resource.

In this case:
- 1 FTE = 1 operational employee
- Structural reference capacity = 360 effective working minutes/day

FTE does **not** include overtime in structural calculations.

---

## Effective FTE

Effective FTE accounts for:

- leave  
- sick days  
- cross-role interruptions  
- partial allocation  

All capacity calculations use Effective FTE.

---

# 2️⃣ Time Metrics

## IW — Investigation Window

Available investigation time per FTE per day.

In this case:

IW = 360 minutes/day  
(baseline sustainable time without overtime)

---

## AIT_break — Average Investigation Time per Break

Average time required to fully close one material break.

Includes:

- document retrieval  
- reconciliation logic  
- recalculation  
- booking correction  
- commentary  
- system input  

AIT_break is an observed operational average.

---

# 3️⃣ Volume Metrics

## DI — Daily Inflow

Number of new material breaks entering the system per day.

Measured in breaks/day.

---

## Backlog (B)

Open unresolved breaks carried forward.

Backlog represents deferred processing time.

Backlog evolution equation:

B(t+1) = B(t) + DI − DRC

If DI > DRC → backlog increases deterministically.  
If DI < DRC → backlog decreases deterministically.

---

# 4️⃣ Capacity Metrics

## DRC — Daily Resolution Capacity

Maximum breaks resolvable per day.

Formula:

DRC = (Effective FTE × IW) / AIT_break

Measured in breaks/day.

---

## ρ (rho) — Utilisation Ratio

Primary stability metric.

Definition:

ρ = DI / DRC

Interpretation:

- ρ < 1 → stable (inflow ≤ capacity)  
- ρ = 1 → critical boundary  
- ρ > 1 → unstable (backlog grows deterministically)

---

## Structural Margin (SM)

SM = DRC − DI

- SM ≥ 0 → positive margin  
- SM < 0 → structural deficit  

Measured in breaks/day.

---

# 5️⃣ KPI Structure

Case 03 distinguishes two structurally different KPI layers.

---

## Review-Level KPI (Proxy Layer)

Staffing driver used during allocation review.

Defined as:

W_proxy = Fund_Count × AIT_fund

Where:

- Fund_Count = number of funds under mandate  
- AIT_fund = average time per fund (review metric)

W_proxy measures review-level workload.

It does **not** measure break generation.

---

## Operational-Level KPI (True Workload Layer)

Real operational workload driver.

Defined as:

W_real = DI × AIT_break

W_real determines actual capacity requirement.

Staffing validity must be tested against W_real.

---

# 6️⃣ Utilisation

Per-FTE operational utilisation:

U = W_real / (Effective FTE × IW)

Interpretation:

- U ≤ 1 → within structural capacity  
- U > 1 → structural overload  

Utilisation is an operational-level metric.

---

# 7️⃣ Required FTE

Required_FTE = W_real / IW

Under-allocation gap:

FTE_gap = Required_FTE − Allocated_FTE

If FTE_gap > 0 → structural under-allocation exists.

---

# 8️⃣ Rounding Gap

When staffing decisions use integer allocation:

Rounded_FTE = floor(Required_FTE)

Rounding Gap:

R_gap = Required_FTE − Rounded_FTE

If R_gap > 0 → structural deficit is embedded at allocation stage.

Rounding converts continuous requirement into discrete capacity.

---

# 9️⃣ Tolerance Band (Review-Level)

Tolerance Band (TB) represents accepted variance in proxy workload during staffing review.

TB applies only to W_proxy.

No formal utilisation variance threshold was defined at operational level.

This creates dimensional asymmetry between review-layer validation and operational capacity reality.

---

# 🔟 Dimensional Sufficiency Condition

A staffing driver is dimensionally sufficient only if:

It preserves ordering of true workload.

Formal condition:

If W_real_A > W_real_B  
then W_proxy_A ≥ W_proxy_B

If this condition fails → dimensional insufficiency exists.

Dimensional insufficiency means the proxy does not preserve workload monotonicity.

---

# 1️⃣1️⃣ Monotonicity Failure

Monotonicity failure occurs when:

W_proxy_A ≥ W_proxy_B  
but  
W_real_A < W_real_B

This indicates representational distortion in allocation logic.

---

# 1️⃣2️⃣ Staffing Validity Condition

Staffing allocation is structurally valid only if:

Allocated_FTE ≥ Required_FTE  

and  

ρ ≤ 1  

Failure of either condition implies structural instability.

---

# 1️⃣3️⃣ Ageing Threshold

Ageing threshold represents maximum tolerated backlog age before escalation.

In this case:

Ageing threshold = 30 days.

If SM < 0 persists, ageing threshold breach becomes deterministic over time.

---

# 1️⃣4️⃣ Model Scope

This case uses a first-order deterministic capacity model.

Not included:

- service time distribution  
- arrival variance modeling  
- multi-stage queue formalisation  
- probabilistic delay modeling  
- feedback loops between backlog and AIT  

Purpose:

Structural governance diagnosis of allocation logic.

---
