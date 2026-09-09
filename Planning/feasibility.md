> **STALE — historical analysis only.** The Phase 2 re-estimation and mandatory-IWT-lab-only attendance policy supersede this report’s workload, capacity assumptions and proposed cuts. See `workload_revision.md` and `State/approved_constraints.json`. No revised feasibility has been performed.

# Feasibility — 10–16 September 2026

**The full approved plan is infeasible.** Its **6,585 minutes (109h 45m)** exceed a defensible focused-study capacity of **3390 minutes (56h 30m)** by **3,195 minutes (53h 15m)**. Even omitting the conditional RecSys numericals allowance leaves **3,105 minutes (51h 45m)** of overload. No cut, estimate change or task change has been applied.

This analysis reuses [source mapping](source_map.json), [approved estimates](workload_estimates.json), [task inventory](task_inventory.json), [selected resources](resource_research.md), [availability](../Requirements/availability.md) and the relevant [master requirements](../Requirements/master_requirements.md). State files were empty at the start. The latest user instructions supply the approval status for the existing workload. No raw notes, new resources, study timetable or calendar were inspected/created.

## Clock time and fixed commitments

Seven calendar days contain 168 hours. The permitted 09:00–22:30 window provides **13h 30m per day × 7 = 94h 30m (5,670 minutes)**. The remaining 73h 30m lies outside the preparation boundary and is not available capacity.

| Item | Minutes | Hours | Treatment |
|---|---:|---:|---|
| Gross permitted clock time | 5,670 | 94h 30m | Starting capacity |
| Daily lunch and dinner | −840 | −14h 00m | Seven one-hour lunches and seven one-hour dinners |
| Friday namaz, incremental | −90 | −1h 30m | 12:30–15:00 is 150 minutes, but its 60-minute lunch overlap is already deducted |
| Mandatory Monday IWT lab | −120 | −2h 00m | Attendance only |
| Selected CV / RecSys / EPQ classes | −180 | −3h 00m | One one-hour class per subject; attendance only |
| Clock time after fixed commitments | **4,440** | **74h 00m** | Not all focused-study capacity |
| Rest, transitions and contingency | −1,050 | −17h 30m | 150 minutes per day, described below |
| **Realistic focused-study capacity** | **3,390** | **56h 30m** | Includes all study, questionnaires, verification and mocks |

The fixed unavailable union is **1,230 minutes (20h 30m)** within the active windows. Meals, namaz and classes are never counted as preparation. The final mock and daily midsem study consume the workload/capacity above; they are not extra deductions on top of it.

## Attendance selection for the capacity calculation

Count whole class meetings rather than contact hours. This is the least disruptive simple selection from the listed timetable: cluster attendance next to the fixed lunch break or mandatory lab, using only two attendance days and leaving the final preparation day free of optional classes. It selects existing classes for arithmetic, not study blocks or a new timetable.

| Subject | Listed meetings in the window | Selected existing meeting | Attendance | Why this choice |
|---|---:|---|---:|---|
| IWT | 5, including Friday and Monday labs as one meeting each | Monday 14 Sep, mandatory lab 10:00–12:00 | 1/5 = 20% | Mandatory lab alone satisfies the approximate target |
| CV | 3 | Thursday 10 Sep, 12:00–13:00 | 1/3 ≈ 33% | Immediately before lunch; one is the minimum sensible whole class |
| RecSys | 3 | Thursday 10 Sep, 14:00–15:00 | 1/3 ≈ 33% | Immediately after lunch, on the same attendance day as CV |
| EPQ | 3 | Monday 14 Sep, 09:00–10:00 | 1/3 ≈ 33% | Directly before the mandatory IWT lab |

Total: four meetings, **300 minutes**. Zero meetings would not satisfy the practical one-class guidance for CV/RecSys/EPQ; exact 20% is impossible with three listed meetings. All other optional meetings are unselected. Blockchain, EMC and TW classes do not happen and reserve no time.

The Friday lab's exact morning time is unspecified, but it is optional and not selected; investigating it would not change this result. The meeting-based IWT count follows availability.md. Different institutional lab-period accounting could change the percentage, not the massive workload shortfall.

## Rest, transitions and focused capacity

Use **150 minutes per day** as a planning allowance: **90 minutes of real rest**, **30 minutes of transitions/logistics**, and **30 minutes of contingency**. These are distinct from meals and are not hidden study time. This is an explicit planning judgment, not a measured personal productivity limit.

The logistics allowance assumes no substantial commute beyond the short transitions it covers, with attendance clustered as above. Any longer travel or substantial tool setup lowers capacity further; none is treated as free. On other days, the allowance protects ordinary task switching and personal logistics. A new mandatory prayer or commitment not listed in availability.md would likewise reduce capacity.

| Day | Gross min | Meals | Classes | Extra namaz | Rest/buffer | Focused capacity |
|---|---:|---:|---:|---:|---:|---:|
| Thursday 10 Sep | 810 | 120 | 120 | 0 | 150 | 420 (7h 00m) |
| Friday 11 Sep | 810 | 120 | 0 | 90 | 150 | 450 (7h 30m) |
| Saturday 12 Sep | 810 | 120 | 0 | 0 | 150 | 540 (9h 00m) |
| Sunday 13 Sep | 810 | 120 | 0 | 0 | 150 | 540 (9h 00m) |
| Monday 14 Sep | 810 | 120 | 180 | 0 | 150 | 360 (6h 00m) |
| Tuesday 15 Sep | 810 | 120 | 0 | 0 | 150 | 540 (9h 00m) |
| Wednesday 16 Sep | 810 | 120 | 0 | 0 | 150 | 540 (9h 00m) |
| **Total** | **5,670** | **840** | **300** | **90** | **1,050** | **3,390 (56h 30m)** |

This implies about eight focused hours per day on average, with nine on unconstrained days: ambitious sustained preparation, not a relaxed week. No study topics or start/end times are assigned in this table. Later scheduling must protect daily midsem self-study and enough energy for the final mock.

A single sensitivity check is enough: allowing only two hours of rest/buffer daily raises capacity to **60h**, still **49h 45m short**; three hours daily lowers it to **53h**, **56h 45m short**. Even the unrealistic zero-rest ceiling of **74h** is **35h 45m short**. The conclusion does not depend on fine-tuning breaks, attendance choices or uncertain CV detail.

## Workload and requirement status

| Workload | Minutes | Hours |
|---|---:|---:|
| LSEG / placement | 4,815 | 80h 15m |
| Required midsem excluding separate conditional numericals | 1,680 | 28h 00m |
| Conditional RecSys numericals, retained in baseline | 90 | 1h 30m |
| Midsem baseline including conditional allowance | 1,770 | 29h 30m |
| **Full baseline** | **6,585** | **109h 45m** |
| **Overload against realistic capacity** | **3,195** | **53h 15m** |

The estimates and task inventory reconcile exactly. Existing overlapping references are already integrated: there is no extra block for JSON, Collections, Extra Fundamentals, Redis or DSA reference files to remove. Classes cannot reduce this workload.

- **REQUIRED as currently approved — 6,495 minutes (108h 15m):** every baseline unit except the separate conditional RecSys numericals allowance. This includes all six core subjects, additional technical tracks, active JavaScript/SQL/MongoDB/DSA, all seven OA tasks, three ordered project pairs, resume, company, HR, aptitude, final mock, EPQ, RecSys units/final revision, mandatory CV reserve, Blockchain and IWT. Secondary technical tracks remain required until the user explicitly approves a deferral; they are not relabelled optional here.
- **DESIRABLE — no extra baseline minutes:** an earlier optional mock, extra weak-topic attempts and wider resource coverage beyond the approved scope. Not adding them saves **zero** from the 6,585-minute baseline.
- **REDUNDANT-OR-CONDITIONAL — 90 minutes provisionally:** only the separate RecSys numericals allowance is an identified conditional candidate. Its redundancy has not been established. Supporting resources have no standalone budget, so integrating them again saves **zero**. RecSys paired notes are not presumed duplicates.

Major contributors:

| Allocation group | Minutes | Hours |
|---|---:|---:|
| Core revision, practice and verification | 1290 | 21h 30m |
| Additional technical subjects | 765 | 12h 45m |
| JavaScript / SQL / MongoDB practice | 570 | 9h 30m |
| General DSA | 720 | 12h 00m |
| LSEG OA: 4 Major + 3 Minor | 465 | 7h 45m |
| Three projects: revision + questionnaires | 420 | 7h 00m |
| Resume / company / HR / aptitude / final mock | 585 | 9h 45m |
| EPQ | 300 | 5h 00m |
| RecSys, including conditional numericals | 780 | 13h 00m |
| CV reserve | 480 | 8h 00m |
| Blockchain + IWT | 210 | 3h 30m |

A useful lower bound: keeping DSA (720), OA (465), all project pairs (420), final mock (150) and all required midsem work (1,680) alone needs **3,435 minutes (57h 15m)**. That already exceeds capacity by 45 minutes before any core revision, additional technology, resume, HR, company or aptitude work. Small efficiencies cannot preserve all existing depth.

## Proposed trade-offs — none applied

A reduction below an approved estimate is a proposal to do less or different work, not evidence that the original workload can be completed faster. Moving work out of this week is a true deferral and leaves it unprepared before the interview unless separately completed; no future time is assumed available.

### Package A — limited repeat-reading reductions; insufficient on its own

| Proposal | Current → proposed min | Saved | Consequence |
|---|---:|---:|---|
| EPQ full notes + revision notes | 300 → 180 | 120 | Omit repeated reading while retaining the approved recall and numerical work, justified by confirmed substantial first-pass completion |
| RecSys final revision | 150 → 90 | 60 | Omit its 60-minute repeat-reading component; retain 30 minutes recall and 60 minutes numerical consolidation |
| Separate RecSys numericals | 90 → 0 | 90 | Omit a separate pass only with explicit approval; overlap remains unverified |
| **Total** | | **270 (4h 30m)** | **No saving is credited twice in Package B** |

This leaves **6,315 minutes (105h 15m)** and **2,925 minutes (48h 45m)** of overload. These are plausible lower-impact reductions in repeat work, not a feasible weekly package or proven redundancy. All other budgets remain unchanged under A.

### Package B — selective preparation within the fixed week

**Recommended only if the dates/boundaries are fixed and the user accepts substantial scope loss.** It keeps every OA task at its approved time, all three projects with revision before separate questionnaires, the full final mock/debrief, the complete provisional CV reserve, and unchanged Blockchain/IWT. It reduces DSA volume explicitly and makes core preparation selective; it does not satisfy the original full-note coverage requirement.

| Track / group | Current min | Proposed min | Saved min | Type and scope consequence |
|---|---:|---:|---:|---|
| OS / CN / DBMS / Java-OOP | 750 | 360 | 390 | True scope reduction: targeted revision plus separate verification replaces full-note preparation. |
| Node/backend + System Design | 540 | 0 | 540 | True deferral of dedicated preparation; incidental project/mock discussion is not equivalent coverage. |
| React / Next.js / TypeScript / Git-GitHub / Python / AI fundamentals | 765 | 0 | 765 | True deferral of dedicated tracks, including their practice/recall; no claim these are redundant or irrelevant to the JD. |
| JavaScript / SQL / MongoDB practice | 570 | 0 | 570 | True deferral of three required active-practice tracks; their time is not hidden inside other sessions. |
| General DSA | 720 | 480 | 240 | Reduced practice volume and re-exposure; keep breadth, Java implementation, timed solving and explanation. |
| All seven OA tasks | 465 | 465 | 0 | Unchanged. |
| Three project pairs | 420 | 300 | 120 | Shorter revision and questionnaires; retain all six separate ordered sessions. |
| Resume | 90 | 60 | 30 | Shorter review and questioning, with fewer follow-ups. |
| LSEG role/company | 135 | 90 | 45 | Shorter source study and rehearsal; exact JD remains primary. |
| HR/behavioural | 120 | 90 | 30 | Fewer rehearsal repetitions; remains distinct from company preparation. |
| Aptitude | 90 | 45 | 45 | One timed practice component instead of two; remove separate refresh, preserve error review. |
| Final mixed mock | 150 | 150 | 0 | Unchanged full interview and debrief. |
| EPQ | 300 | 180 | 120 | Reduce repeated reading using confirmed prior preparation; preserve recall and numerical components. |
| RecSys Units 1–3 | 540 | 360 | 180 | True depth reduction: less concept-coverage and worked-method practice; not full coverage at a faster speed. |
| RecSys final revision | 150 | 90 | 60 | Omit the repeat reading component; preserve active recall and numerical consolidation. |
| Separate RecSys numericals | 90 | 0 | 90 | Conditional omission requiring explicit approval; redundancy is not established. |
| CV | 480 | 480 | 0 | Mandatory provisional reserve unchanged. |
| Blockchain + IWT | 210 | 210 | 0 | Unchanged narrow-scope preparation, including IWT Web/HTTP/URL and HTML/CSS. |
| **Total** | **6,585** | **3,360** | **3,225** | **All changes require approval** |

Exact proposed component limits for review:

- **OS, CN and DBMS:** 90 minutes each = 45 targeted revision + 15 recall + 30 separate verification. **Java/OOP:** 90 = 30 targeted revision + 30 implementation + 30 separate verification. Broad verification identifies gaps; it does not replace omitted revision. This explicitly waives full-source coverage for these four subjects.
- **Node/backend, System Design, React, Next.js, TypeScript, Git/GitHub, Python, AI fundamentals, JavaScript practice, SQL practice and MongoDB practice:** zero dedicated minutes in this week. Their discussion may arise within existing project/resume/mock work, but that is limited exposure and saves no additional minutes. Their JD/resume relevance has not been reassessed; the user must accept these particular deferrals or nominate equivalent replacements before a schedule can be considered.
- **DSA:** 480 = 60 pattern refresh + 270 representative Java implementation + 90 timed solving + 60 re-exposure/complexity explanation. Preserve major-pattern breadth, but accept fewer representative attempts and less repetition than the approved 720 minutes. OA remains entirely separate.
- **Velvet and Eventually:** 105 each = 60 revision + a separate 45-minute questionnaire. **Relay:** 90 = 45 revision + a separate 45-minute questionnaire. All six sessions and their order remain mandatory; interview-questioning depth decreases.
- **Resume:** 60 = 30 review + 30 later questioning. **Role/company:** 90 = 20 JD review + 25 company study + 20 role-fit preparation + 25 questioning. **HR:** 90 = 30 preparation + 45 ChatGPT practice + 15 feedback. **Aptitude:** 45 = 30 timed practice + 15 error review. These are shorter passes/fewer repetitions, not removal of the tracks or a merger of HR and company work.
- **EPQ:** full-note refresh 90 = 45 revision + 30 recall + 15 numericals; revision-note consolidation 90 = 30 recall + 60 numericals. **RecSys Units 1–3:** 120 each = 60 concept coverage + 30 method/numerical practice + 30 recall, still using each paired source as one unit. **RecSys final revision:** 90 = 30 recall + 60 numericals. The three unit reductions sacrifice coverage/depth; they are not justified as removal of duplicate paired files.
- **CV 480, Blockchain 90, IWT 120, OA 465 and final mock 150:** unchanged. The final mock remains 120 interview + 30 debrief. CV is still a provisional reserve, not a known sufficient duration.

Package B totals: **LSEG/placement 2,040 minutes (34h)** and **midsem 1,320 minutes (22h)**, combined **3,360 minutes (56h)**. LSEG retains the largest share (about 61%); midsem retains substantial work across all five subjects, including eight hours of CV. Daily midsem self-study must still be enforced in later scheduling, and classes never substitute for it.

There is **30 minutes of unallocated capacity** beyond the already-deducted rest/buffer allowance. This is an aggregate capacity fit only, not a validated schedule or a guarantee that the reduced coverage is sufficient. If the separate 90-minute RecSys numericals task must be retained, Package B becomes **57h 30m**, which is **one hour over capacity** after using the 30-minute margin. Additional CV material, commute or setup could also require another decision.

## Approval required before proceeding

1. **Choose the scope direction:** Package A alone is insufficient. Approve Package B's explicitly reduced preparation contract, or identify a different set of required-track deferrals/reductions totalling at least **3,195 minutes**. Keeping all original scope requires additional usable preparation time outside the current constraints; none has been identified or assumed.
2. **For Package B, explicitly accept** targeted rather than full-note OS/CN/DBMS/Java preparation; the eleven named dedicated-track deferrals; DSA 720→480; project pairs 420→300 with ordering intact; and the stated resume/company/HR/aptitude reductions.
3. **Accept the midsem changes:** EPQ 300→180, RecSys unit coverage 540→360, final revision 150→90, and the proposed separate-numericals omission 90→0 despite unresolved redundancy. CV, Blockchain, IWT and daily genuine midsem self-study remain protected.

The attendance selection and capacity assumptions above are analysis choices already authorised by this task; they are not requests to loosen the attendance or daily boundaries. No proposed cut has been entered into approved_cuts.json. Workload estimates, task inventory, source map and resources are unchanged. After the user's decision, only approved scope changes may be recorded, dependencies adjusted (including DBMS verification if SQL is deferred), and feasibility rechecked before any draft schedule.
