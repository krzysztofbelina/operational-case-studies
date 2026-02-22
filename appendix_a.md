# Appendix A — Structural Definitions & Notation

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

Example used in the case:
10 nominal makers → 9.5 effective FTE

---

# 2️⃣ Time Metrics

## IW — Investigation Window

Available investigation time per FTE per day.

Two variants:

- **IW_structural** = 360 minutes/day  
  (baseline sustainable time without overtime)

- **IW_total** = 450 minutes/day  
  (includes 2 hours overtime)

Structural models use IW_structural.

---

## AIT — Average Investigation Time

Average time required to fully close one material break.

Includes:
- document retrieval
- reconciliation logic
- recalculation
- booking correction
- commentary
- system input

Case values:

- AIT_pre_tool = 30 min/break
- AIT_post_tool = 45 min/break

AIT is an observed operational average.

---

# 3️⃣ Volume Metrics

## DI — Daily Inflow

Number of new material breaks entering the system per day.

Case values:

- DI_baseline = 150–160 breaks/day
- DI_spike ≈ 500 breaks/day

Measured in breaks/day.

---

## Same-Day Closures

Number of breaks fully resolved within the same operational day.

Represents realised throughput, not theoretical maximum capacity.

---

## Backlog

Open unresolved breaks carried forward.

Case reference:

Backlog ≈ 600 breaks

Backlog represents deferred processing time.

---

# 4️⃣ Capacity Metrics

## DRC — Daily Resolution Capacity

Maximum breaks resolvable per day.

Formula:

DRC = (Effective FTE × IW) / AIT

Measured in breaks/day.

Two variants:

- DRC_structural (using IW_structural)
- DRC_overtime (using IW_total)

---

## Structural Capacity

Structural Capacity = DRC calculated using IW_structural (no overtime).

It represents sustainable system throughput without relying on extended working hours.

---

## ρ (rho) — Utilisation Ratio

Primary stability metric.

Definition:

ρ = DI / DRC

Interpretation:

- ρ < 1 → stable (inflow ≤ capacity)
- ρ = 1 → critical boundary
- ρ > 1 → unstable (backlog grows deterministically)

This is a deterministic first-order stability indicator.

---

## Structural Margin (SM)

SM = DRC_structural − DI

- SM ≥ 0 → positive margin
- SM < 0 → structural deficit

Measured in breaks/day.

---

## Recovery Window

Available excess structural capacity allowing backlog reduction when DI temporarily exceeds DRC.

Recovery Window exists only if:

DRC_structural > DI

Without structural margin, no recovery is possible after spike events.

---

# 5️⃣ Control Metrics

## Review Time

Average time required by checker to review one break.

Case reference:

2 minutes per break (average observed)

---

## Review Compression

Situation where required review time exceeds available checker time, leading to reduced review depth.

Observed during spike periods when execution dropped significantly below required review demand.

---

# 6️⃣ Financial Translation Metrics

## Overtime Hours

Total additional hours worked beyond structural IW.

Example:

9.5 FTE × 2h × 22 days = 418h/month

Converted to implicit FTE equivalent:

418 / 160 ≈ 2.6 FTE

---

## FTE-Equivalent

Conversion of time (hours) into full-time equivalent resource.

Reference:

1 FTE-month ≈ 160 hours

Used for structural comparison only.

---

## Frozen Throughput

Backlog converted into time equivalent:

Backlog × AIT

Example:

600 × 45 min = 27,000 minutes  
= 450 hours  
≈ 45 FTE-days (at 10h/day operational reality)

Represents embedded unresolved workload.

---

## Recapitalisation

Increase in headcount required to restore positive structural margin and re-establish system stability.

In the case study, headcount expansion was required to offset accumulated structural deficit.

---

# 7️⃣ Stability Condition (Deterministic)

System considered structurally stable when:

- ρ ≤ 1  
- Backlog non-increasing  
- Review capacity ≥ required review demand  

This is a simplified deterministic model.

It does not model stochastic variance or arrival dispersion.

---

# 8️⃣ Model Scope Limitations

This case uses a first-order deterministic capacity model.

Not included:

- Service time distribution
- Arrival variance modeling
- Multi-stage queue formalisation
- Probabilistic delay modeling

Purpose:

Structural governance diagnosis, not academic queue modelling.

---
