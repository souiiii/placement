# Planning decisions

Decisions worth preserving across sessions, newest phase last. Estimates, durations and scope are recorded elsewhere and are not restated here.

## Phase 3 — feasibility (recorded 9 September 2026)

- Capacity is computed as 09:00–22:30 gross minus meals, Friday namaz, the mandatory Monday lab and a **150 min/day rest/transition/contingency allowance** (90 rest + 30 transitions + 30 contingency). That allowance is a planning judgment and the only real buffer; it is never re-labelled as study.
- Removing the optional-class attendance target returned 180 minutes and moved capacity from 3,390 to **3,570**. Against a 3,565-minute workload the margin is **5 minutes**.
- The mock (120) plus debrief (15) is 135 minutes and **cannot fit the 120-minute post-dinner window on 16 September**, and the debrief cannot spill into the 17 September interview day. The mock is therefore pinned pre-dinner and the 20:30–22:30 slot on 16 September is midsem-only. This is arithmetic, not preference.

## Phase 4 — scheduling (recorded 9 September 2026)

Draft schedule in `Output/draft_plan.md`; 60 nonzero tasks, 3,565 minutes, day partition identical to the feasibility result.

- **Week shape:** core theory and the DSA pattern base first (Thu–Fri), practice chains and DSA bulk mid-week (Sat), OA and timed solving (Sun), the shorter web/tech tracks on Monday's lab-fragmented day, OA close-out and remaining project sessions (Tue), pure consolidation then the mock (Wed). Demanding technical work early in each day, oral rehearsal later.
- **DBMS before SQL and Node/backend before MongoDB** are scheduled a day apart in each case, because their practice-review blocks host the DBMS and backend closure checkpoints.
- **Five tasks are split across sessions** — `dsa.practice` (105+90+45, deliberately spread for breadth across five DSA days), the three RecSys units (90+60 or 60+90 around a meal rather than one 2½-hour sitting) and `cv.reserved_preparation` (120 Mon + 60 Tue). Permitted by the inventory's task semantics and `master_requirements.md` §8.
- **Merged blocks only within a `session_group_id`** (SQL, MongoDB, JavaScript, resume, role/company, HR). Nothing marked `separate_session_required` is merged: the six project sessions and the mock each hold their own block.
- **Project pairs are spaced across days** — Velvet revision Sun → questionnaire Mon; Relay revision Sun → questionnaire Tue; Eventually revision Tue → questionnaire Wed — so each questionnaire tests recall rather than short-term memory.
- **The 5-minute slack sits in Tuesday's wind-down.** It is reported as true unused slack, not folded into a study block.
- **No optional class is scheduled.** `State/approved_constraints.json` supersedes the ~20% attendance target; the Monday lab is the only attendance event, and it does not satisfy Monday's midsem requirement (CV does).
- **No separate verification blocks exist.** The seven zero-minute checkpoints live inside their named hosts per the approved Phase 2 preparation mode, which supersedes `master_requirements.md` §9 phase 3.
- **Friday's namaz** is rendered as two events (12:30–13:00, 14:00–15:00) around the fixed lunch hour so both protected periods appear explicitly without overlapping. Nothing is scheduled inside 12:30–15:00.
- `Output/final_plan.md` and `Output/calendar_events.json` are deliberately left empty pending approval, per the `AGENTS.md` §6 workflow and the calendar-permission rules.
