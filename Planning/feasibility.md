# Feasibility — 10–16 September 2026 (revised workload)

**The revised plan fits, but with effectively no margin.** Realistic focused-study capacity under the mandatory-lab-only attendance rule is **3,570 minutes (59h 30m)**. The accepted revised workload is **3,565 minutes (59h 25m)**, including the 45 conditional RecSys numerical minutes. The margin is **+5 minutes (0.14%)**. Excluding the conditional numericals the workload is **3,520 minutes (58h 40m)** and the margin is **+50 minutes**.

Day-level and dependency feasibility also pass, subject to two placement rules that scheduling must honour (Wednesday's mock window and the pre-mock partition). No estimate, duration, task or scope has been changed by this analysis. Package A and Package B are superseded and are not revived.

Inputs used: [revised estimates](workload_estimates.json), [task inventory](task_inventory.json), [revision report](workload_revision.md), [availability](../Requirements/availability.md) and [approved constraints](../State/approved_constraints.json). No source notes were reopened and no resource research was performed.

---

## 1. Capacity under the current attendance rule

The permitted window is 09:00–22:30, i.e. **810 minutes × 7 days = 5,670 minutes (94h 30m)** of gross clock time. Deductions are the preserved fixed commitments only.

| Item | Minutes | Hours | Treatment |
|---|---:|---:|---|
| Gross permitted clock time | 5,670 | 94h 30m | Starting point |
| Daily lunch and dinner | −840 | −14h 00m | 7 × 60 lunch + 7 × 60 dinner |
| Friday namaz, incremental | −90 | −1h 30m | 12:30–15:00 is 150 min; its 60-min lunch overlap is already deducted |
| Mandatory Monday IWT lab | −120 | −2h 00m | Attendance only; never counted as study |
| Optional class attendance | −0 | −0h 00m | **Removed** by the current attendance rule |
| Clock time after fixed commitments | **4,620** | **77h 00m** | Not yet focused capacity |
| Rest, transitions and contingency | −1,050 | −17h 30m | Preserved allowance of 150 min/day |
| **Realistic focused-study capacity** | **3,570** | **59h 30m** | All study, questionnaires, checks and mocks |

The rest allowance is unchanged from the previous analysis: **90 minutes real rest + 30 minutes transitions/logistics + 30 minutes contingency per day**. It is a planning judgment, not hidden study time, and it is the only genuine buffer in this plan.

The only capacity change against the stale report is the attendance rule: dropping the four optional CV/RecSys/EPQ/IWT meetings returns **+180 minutes**, moving capacity from 3,390 to 3,570.

### Per-day focused capacity

| Day | Gross | Meals | Class | Namaz | Rest/buffer | Focused capacity |
|---|---:|---:|---:|---:|---:|---:|
| Thursday 10 Sep | 810 | 120 | 0 | 0 | 150 | **540** (9h 00m) |
| Friday 11 Sep | 810 | 120 | 0 | 90 | 150 | **450** (7h 30m) |
| Saturday 12 Sep | 810 | 120 | 0 | 0 | 150 | **540** (9h 00m) |
| Sunday 13 Sep | 810 | 120 | 0 | 0 | 150 | **540** (9h 00m) |
| Monday 14 Sep | 810 | 120 | 120 | 0 | 150 | **420** (7h 00m) |
| Tuesday 15 Sep | 810 | 120 | 0 | 0 | 150 | **540** (9h 00m) |
| Wednesday 16 Sep | 810 | 120 | 0 | 0 | 150 | **540** (9h 00m) |
| **Total** | **5,670** | **840** | **120** | **90** | **1,050** | **3,570** (59h 30m) |

---

## 2. Aggregate comparison

| Quantity | Minutes | Hours |
|---|---:|---:|
| LSEG / placement workload | 2,500 | 41h 40m |
| Midsem workload, excluding conditional numericals | 1,020 | 17h 00m |
| Conditional RecSys numericals | 45 | 0h 45m |
| Midsem workload, including conditional | 1,065 | 17h 45m |
| **Revised total workload** | **3,565** | **59h 25m** |
| Realistic focused capacity | 3,570 | 59h 30m |
| **Margin, conditional numericals included** | **+5** | **+0h 05m** |
| **Margin, conditional numericals excluded** | **+50** | **+0h 50m** |

Utilisation is **99.86%** of focused capacity with the conditional block, **98.6%** without it. Average committed load is **8h 29m of focused work per day** across seven consecutive days, on top of the fixed commitments.

### Sensitivity to the rest allowance

The result is entirely determined by the preserved 150 min/day rest allowance, and is not robust to changing it.

| Rest/buffer per day | Capacity | Margin vs 3,565 |
|---:|---:|---:|
| 120 min | 3,780 (63h 00m) | +215 |
| **150 min (preserved)** | **3,570 (59h 30m)** | **+5** |
| 180 min | 3,360 (56h 00m) | −205 |
| 210 min | 3,150 (52h 30m) | −415 |

Raising daily rest by even 30 minutes makes the plan infeasible by 3h 25m. This is recorded as a risk, not as a proposed change.

---

## 3. Day-level feasibility

Aggregate fit is not sufficient, because two structural constraints bind particular days.

### 3.1 Wednesday 16 September — the mock window is the tightest point

`final_mixed_mock.interview` (120 min) plus `final_mixed_mock.debrief` (15 min) is a **135-minute ordered block that must occur on the night of 16 September**, and the debrief must finish inside the active window because 17 September is the interview day and lies outside the planning window.

The post-dinner window on 16 September is **20:30–22:30 = 120 minutes exactly**. The 135-minute block therefore **does not fit after dinner**. The only placement that satisfies every preserved constraint is the pre-dinner evening: **mock 17:15–19:15, debrief 19:15–19:30**, ending exactly at the dinner boundary.

Two consequences follow and must be carried into scheduling:

- Every one of the mock's **30 LSEG prerequisites must be complete by 17:15 on 16 September**, not merely "by Wednesday".
- The **20:30–22:30 slot on 16 September can hold midsem work only**, since all remaining LSEG tasks are prerequisites of a mock that has already run.

This is a hard placement rule, not an infeasibility.

### 3.2 The pre-mock partition still closes

Applying 3.1, capacity splits as follows.

| Window | Focused minutes | Admissible work |
|---|---:|---|
| Thu–Tue (all days) | 3,030 | LSEG or midsem |
| Wed daytime, 09:00–17:15 | ≤285 | LSEG or midsem |
| Wed mock block, 17:15–19:30 | 135 | Mock + debrief only |
| Wed 20:30–22:30 | ≤120 | Midsem only |
| **Total** | **3,570** | |

Pre-mock LSEG work is 2,500 − 135 = **2,365 minutes** and must fit in the 3,315 minutes of Thu–Tue plus Wed daytime. That leaves **950 minutes** in those windows for midsem, and Wed evening supplies at most 120 more: **1,070 available against 1,065 required**. The partition closes with the same 5-minute slack as the aggregate — no additional day-level loss appears, but none is absorbed either.

### 3.3 A demonstrated feasible day-level allocation

This is a minute budget proving day-level fit, **not a timetable**. No start times other than the mock placement are assigned.

| Day | Capacity | LSEG | Midsem | Mock | Slack |
|---|---:|---:|---:|---:|---:|
| Thursday 10 Sep | 540 | 390 | 150 | — | 0 |
| Friday 11 Sep | 450 | 300 | 150 | — | 0 |
| Saturday 12 Sep | 540 | 390 | 150 | — | 0 |
| Sunday 13 Sep | 540 | 390 | 150 | — | 0 |
| Monday 14 Sep | 420 | 300 | 120 | — | 0 |
| Tuesday 15 Sep | 540 | 310 | 225 | — | 5 |
| Wednesday 16 Sep | 540 | 285 | 120 | 135 | 0 |
| **Total** | **3,570** | **2,365** | **1,065** | **135** | **5** |

Every day carries a genuine midsem self-study block of at least 120 minutes, distinct from any class. Six of seven days are booked to the minute.

### 3.4 Dependency and ordering checks

- **RecSys chain** (`unit_1`, `unit_2`, `unit_3` → `final_revision` → conditional `numericals`, 570 min total) fits the midsem column above: units on 10/11/12 Sep at 150 each, final revision (75) and the conditional numericals (45) together in the 120-minute midsem slot on 16 Sep. The conditional block is scheduled last in its own chain, so removing it removes 45 minutes cleanly and disturbs nothing upstream.
- **EPQ**: `epq_full_notes.consolidate` (60) precedes `epq_revision.consolidate` (90); both land in the 14–15 Sep midsem allocation.
- **Project ordering**: all three revision → questionnaire pairs remain separate and ordered; total 310 minutes, no day-level obstruction.
- **Integrated closure checks**: `dbms.verify` requires `sql_practice.review`, and `node_backend.verify` requires `mongodb_practice.review`. Both are zero-additional-minute checkpoints, but they impose real ordering: DBMS and Node/backend preparation must precede their SQL/MongoDB practice chains, which must in turn finish before the mock. Chain lengths are 75+105 = 180 and 120+90 = 210 minutes respectively — comfortable within six pre-mock days.
- **Longest chain**: DSA (`refresh` 30 → `practice` 240 → `timed` 90 → `review` 60 = 420 minutes, depth 4). Spread across 10–15 Sep it needs about 70 minutes per day; no day is forced to absorb it whole.
- **Longest single task**: `dsa.practice` at 240 minutes. The largest uninterrupted window on every day is at least 240 minutes (09:00–13:00 on unfragmented days; 14:00–19:30 gives 330 on Monday, 15:00–19:30 gives 270 on Friday), so it fits contiguously if wanted, and the inventory permits splitting it in any case.
- **Fragmented days**: Monday's mandatory lab splits the day into 09:00–10:00, 12:00–13:00, 14:00–19:30 and 20:30–22:30; Friday's namaz leaves 09:00–12:30, 15:00–19:30 and 20:30–22:30. Both still clear their reduced 420 and 450 minute loads, and both retain a ≥270-minute contiguous block.

**Day-level and dependency feasibility pass.**

---

## 4. Conditional RecSys numericals

The 45-minute `recsys_numericals.conditional_practice` block is treated exactly as recorded: **required in the totals, conditional in status, redundancy unverified, not cut**. It is the terminal node of the RecSys chain, so it is the single cleanest item to drop if capacity is later needed — dropping it moves the margin from +5 to +50 minutes. No such decision is made or recommended here.

---

## 5. Risks and assumptions

The plan is feasible on the recorded numbers. It is not resilient, because the margin is 5 minutes and several inputs are explicitly low confidence.

1. **Zero effective margin.** Any single 10-minute overrun consumes the entire aggregate slack. The real buffer is the 1,050-minute rest/contingency allowance, which must not be re-labelled as study to absorb overruns.
2. **CV scope is provisional.** `cv.reserved_preparation` is 180 minutes against an indicative 120–360 range with no confirmed syllabus. The upper end alone adds 180 minutes and breaks feasibility.
3. **RecSys first-pass status unconfirmed.** Units 1–3 are 150 each against an indicative 120–210 range. The upper end adds 180 minutes and breaks feasibility.
4. **DSA fluency unmeasured.** 420 minutes against an indicative 300–540 range; the upper end adds 120 minutes and breaks feasibility.
5. **Rest allowance sensitivity.** 180 minutes of daily rest instead of 150 produces a 205-minute deficit. Feasibility depends on the preserved allowance holding in practice.
6. **No commute, setup or environment time is assumed.** MongoDB practice presumes a working environment; LeetCode presumes usable access. Substantial setup or travel would come straight out of the 5-minute margin.
7. **Wednesday's mock placement is fixed by arithmetic**, not by preference. If the mock must instead run after dinner, the debrief has nowhere inside the window to go.
8. **Midsem exam order is still unknown.** It may later change the relative emphasis of the 15–16 September midsem blocks, but not these totals.

If any of items 2–4 is confirmed at the upper end, the correct response is a focused re-estimate of that specific track, not an automatic cut elsewhere.

---

## 6. Result

**FEASIBLE — READY FOR SCHEDULING**, with a +5 minute margin including the conditional RecSys numericals and +50 minutes without them, and with the Wednesday mock placement rule and pre-mock partition from section 3 binding on the schedule.

No timetable has been produced. No cut, deferral or estimate change has been applied, and the superseded Package A and Package B proposals remain withdrawn.
