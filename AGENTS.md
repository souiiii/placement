# AGENTS.md — Codex Navigation & Operating Guide

## Purpose

This file is the **navigation guide for Codex**.

Its job is to help the AI find the right information quickly, avoid rereading the whole repository, reuse prior work, and know exactly which file to read or update for each planning task.

Do **not** treat this file as a duplicate of the project requirements. Detailed planner rules live in `Requirements/`.

---

# 1. Default behavior

Before doing any task:

1. Identify the exact task.
2. Use the routing tables in this file to read only the files needed for that task.
3. Check whether the result already exists in `Planning/`, `State/`, or `Output/`.
4. Reuse valid existing work instead of repeating research or analysis.
5. Read source files only when the current task genuinely depends on their content.
6. Save meaningful new analysis to the designated planning/state file.

> **Do not recursively read the whole repository by default.**

This is important for speed, context efficiency, and credit usage.

---

# 2. Project map

```text
placement/
├── AGENTS.md
├── README.md
│
├── Requirements/
│   ├── master_requirements.md
│   ├── availability.md
│   ├── planner_description.md
│   └── calendar_rules.md
│
├── Sources/
│   ├── Placement/
│   ├── Projects/
│   ├── Midsem/
│   ├── LSEG/
│   └── Resume/
│
├── Planning/
│   ├── source_map.json
│   ├── workload_estimates.json
│   ├── task_inventory.json
│   ├── resource_research.md
│   ├── planning_decisions.md
│   └── feasibility.md
│
├── State/
│   ├── planner_state.json
│   ├── approved_constraints.json
│   └── approved_cuts.json
│
└── Output/
    ├── draft_plan.md
    ├── final_plan.md
    └── calendar_events.json
```

---

# 3. Where to go for each kind of information

| Need | Read this |
|---|---|
| Overall goal, priorities, preparation philosophy, mandatory tracks, feasibility policy | `Requirements/master_requirements.md` |
| Dates, daily hours, meals, classes, attendance, namaz, hard scheduling constraints | `Requirements/availability.md` |
| Meaning of slot types such as Full Revision, Practice, Final Verification, Project Questionnaire, Mock | `Requirements/planner_description.md` |
| Calendar title style, descriptions, resource links, event validation, calendar behavior | `Requirements/calendar_rules.md` |
| Raw study/reference material | Relevant file under `Sources/` |
| Logical source groupings and source roles | `Planning/source_map.json` |
| Existing duration/workload estimates | `Planning/workload_estimates.json` |
| Full list of required planner tasks | `Planning/task_inventory.json` |
| Selected external resources and rationale | `Planning/resource_research.md` |
| Important prior reasoning/decisions | `Planning/planning_decisions.md` |
| Capacity/overload analysis | `Planning/feasibility.md` |
| Current project phase/progress | `State/planner_state.json` |
| User-approved hard constraints | `State/approved_constraints.json` |
| User-approved removals/cuts | `State/approved_cuts.json` |
| Proposed schedule | `Output/draft_plan.md` |
| User-approved final schedule | `Output/final_plan.md` |
| Structured events prepared for calendar creation | `Output/calendar_events.json` |

---

# 4. Authority order

If information conflicts, use this order of authority:

1. **User's newest explicit instruction**
2. **User-approved values stored in `State/`**
3. `Requirements/master_requirements.md`
4. `Requirements/availability.md`
5. `Requirements/planner_description.md`
6. `Requirements/calendar_rules.md`
7. Existing files in `Planning/`
8. Codex's own inference

Never override an explicit user-approved requirement simply because another schedule would appear more convenient.

If new evidence creates a real conflict with an approved decision, explain the conflict before changing the approved decision.

---

# 5. Task routing table

Use this table instead of loading unrelated files.

| Current task | Minimum files to read | File(s) to update |
|---|---|---|
| Inspect/classify a new source | relevant `Sources/...` file + `master_requirements.md` if role is unclear | `Planning/source_map.json` |
| Estimate a subject/source | relevant source + `Planning/source_map.json` + existing estimate if present | `Planning/workload_estimates.json` |
| Research an external study/practice resource | relevant requirement/slot rule + source role + existing research | `Planning/resource_research.md` |
| Build/update task inventory | `master_requirements.md` + `source_map.json` + `workload_estimates.json` + approved state | `Planning/task_inventory.json` |
| Choose college attendance | `Requirements/availability.md` + current task inventory | `Planning/planning_decisions.md` and relevant planning output |
| Run feasibility | `availability.md` + `task_inventory.json` + `workload_estimates.json` + approved state | `Planning/feasibility.md` |
| Propose cuts after overload | `feasibility.md` + `task_inventory.json` + `master_requirements.md` | `Planning/planning_decisions.md`; do **not** write to `approved_cuts.json` until user approves |
| Draft schedule | requirements needed for scheduling + approved state + feasibility + task inventory + estimates | `Output/draft_plan.md` |
| Validate draft | draft + `availability.md` + `calendar_rules.md` + requirements + approved state | fix `Output/draft_plan.md`; record important decisions if needed |
| Finalize approved schedule | approved draft + relevant state | `Output/final_plan.md`, `State/planner_state.json` |
| Prepare calendar event data | `final_plan.md` + `calendar_rules.md` + resource research | `Output/calendar_events.json` |
| Create live calendar events | `calendar_events.json` + explicit current user instruction | live calendar only after permission |
| Add newly received JD/resume/OA/CV material | new source + relevant requirement section | relevant `Sources/` path, then update source map/estimates as needed |

---

# 6. Required planning workflow

Do not jump directly from raw sources to a final calendar.

Use this sequence unless the user explicitly requests a narrower task:

```text
1. Read relevant requirements/state
2. Inventory available source material
3. Build/update source_map.json
4. Inspect required source content
5. Build/update workload_estimates.json
6. Research external resources where needed
7. Build/update task_inventory.json
8. Calculate realistic available capacity
9. Run feasibility analysis
10. If infeasible: stop and ask user to approve trade-offs
11. Build draft plan
12. Validate draft against all hard constraints
13. Present/wait for approval
14. Produce final plan
15. Prepare calendar_events.json
16. Create live calendar events only when explicitly requested
```

Do not skip the feasibility gate.

---

# 7. Source-reading rules

## 7.1 Do not infer calendar time from file count

A file is a source, not automatically a task.

Do not assume:

- one file = one block;
- one folder = one day;
- every note deserves a dedicated event.

Use `Planning/source_map.json` to distinguish physical files from logical study units.

## 7.2 Respect logical groupings

Recommendation Systems has paired physical files that are studied together:

- Unit 1 ChatGPT + Unit 1 Codex = one logical Unit 1
- Unit 2 ChatGPT + Unit 2 Codex = one logical Unit 2
- Unit 3 ChatGPT + Unit 3 Codex = one logical Unit 3

Do not schedule paired files as separate units merely because two files exist.

## 7.3 Respect source roles

Sources may be classified as:

- primary revision source;
- practice reference;
- supporting/embedded reference;
- optional/redundant source;
- pending/incomplete source.

The source role should be stored in `Planning/source_map.json`.

## 7.4 Missing/empty sources

If a required source is missing or empty:

- do not hallucinate its content;
- record that it is pending;
- continue only with analysis that does not depend on the missing content;
- revisit estimates when the real source arrives.

## 7.5 Preserve source material

Do not rewrite study notes merely to make planning easier unless explicitly asked.

Planning analysis belongs in `Planning/` and `State/`, not inside the original source files.

---

# 8. Workload estimation rules

When estimating time:

- inspect actual source length and density;
- consider difficulty and familiarity;
- distinguish revision from first-pass learning;
- allow more time for practice than passive reading;
- allow realistic time for oral verification/questionnaire/mock sessions;
- split large logical units when required;
- combine small compatible tasks only when sensible;
- do not use a universal 60- or 90-minute block rule.

Most importantly:

> **Do not reduce an honest duration estimate just because the schedule is crowded.**

If the workload does not fit, use the feasibility process instead.

---

# 9. Feasibility gate

A final planner may not be produced until feasibility has been checked.

If realistic workload exceeds realistic capacity:

1. Stop before finalizing the plan.
2. Record the overload in `Planning/feasibility.md`.
3. Identify required, desirable, and redundant/optional work.
4. Propose specific trade-offs.
5. Record proposals in `Planning/planning_decisions.md` if useful.
6. Ask the user for approval.
7. Only user-approved removals belong in `State/approved_cuts.json`.

Never silently:

- drop a required task;
- shorten a task to an unrealistic duration;
- remove a source from coverage;
- treat a suggested cut as approved.

---

# 10. Core planning invariants

Detailed rules live in `Requirements/`, but every draft/final plan must preserve these invariants:

- LSEG receives the largest share of preparation time.
- At least one genuine midsem self-study block exists every day from Sep 10–16.
- Class attendance does not count as self-study.
- Prep starts no earlier than 9:00 AM and ends by 10:30 PM.
- Lunch is protected from 1:00–2:00 PM.
- Dinner is protected from 7:30–8:30 PM.
- Friday Sep 11, 12:30–3:00 PM is protected for namaz.
- Monday Sep 14 IWT Lab is mandatory.
- Blockchain, EMC, and TW classes are treated as not happening.
- Project revision occurs before project questionnaire.
- Core revision/practice occurs before final verification.
- LSEG OA preparation remains separate from normal DSA.
- The plan is fixed by default; do not automatically replan because of weak performance or a missed block.
- Sep 16 night contains the mandatory full mixed LSEG mock with ChatGPT.
- Late Sep 16 should emphasize consolidation rather than heavy new learning where possible.
- Real rest/buffer time must exist.

If a draft violates any invariant, fix the draft before presenting it.

---

# 11. External research rules

When a task needs outside resources:

- check `Planning/resource_research.md` first;
- reuse an existing valid resource choice rather than researching again;
- prefer short targeted videos when equally suitable;
- use strong written resources/documentation when better;
- use actual practice platforms/problem sets for practice blocks;
- avoid oversized playlists/courses for narrow tasks;
- optimize for relevance, correctness, quality, depth, and time efficiency.

Store useful final selections and rationale in `Planning/resource_research.md`.

Do not repeatedly research the same topic unless:

- the existing resource is missing/broken/outdated;
- new requirements change the task;
- the user explicitly asks for alternatives.

---

# 12. Persistence rules

After meaningful work, save the result to the correct file.

| New information produced | Save to |
|---|---|
| Source meaning/grouping/role | `Planning/source_map.json` |
| Duration estimate | `Planning/workload_estimates.json` |
| Required task/dependency | `Planning/task_inventory.json` |
| External resource choice | `Planning/resource_research.md` |
| Important reasoning/decision | `Planning/planning_decisions.md` |
| Capacity/overload result | `Planning/feasibility.md` |
| Current phase/progress | `State/planner_state.json` |
| Explicit user-approved constraint | `State/approved_constraints.json` |
| Explicit user-approved removal/cut | `State/approved_cuts.json` |
| Proposed schedule | `Output/draft_plan.md` |
| Approved schedule | `Output/final_plan.md` |
| Calendar-ready event data | `Output/calendar_events.json` |

Do not duplicate the same analysis across multiple files unless there is a clear reason.

---

# 13. State and prior-work reuse

Before repeating work, inspect the designated existing file.

Examples:

- Before estimating OS again, check `workload_estimates.json`.
- Before researching JavaScript practice again, check `resource_research.md`.
- Before deciding whether RecSys numericals are separate, check `source_map.json` and `planning_decisions.md`.
- Before creating a new draft, check `planner_state.json`, `approved_constraints.json`, `approved_cuts.json`, and existing output.

Existing work may be updated when new evidence arrives, but do not discard it without reason.

If an estimate changes because a new source was added, update the estimate and record the reason where useful.

---

# 14. Inputs that may arrive later

The project may receive new material after initial analysis, including:

- exact LSEG job description;
- exact resume submitted to LSEG;
- 4 major LSEG OA questions;
- 3 minor LSEG OA questions;
- current Computer Vision PPTs/notes;
- official midsem timetable.

When new material arrives:

1. place/use it in the appropriate `Sources/` location;
2. update `source_map.json`;
3. update affected estimates/tasks/resources;
4. rerun only the affected part of feasibility/planning where possible;
5. preserve unrelated approved decisions.

Do **not** rerun the entire project unnecessarily.

---

# 15. Output semantics

## `Output/draft_plan.md`

A proposed schedule. It is not automatically approved.

## `Output/final_plan.md`

The user-approved planner.

## `Output/calendar_events.json`

Structured calendar-ready event data derived from the approved final plan.

Generating a final plan or `calendar_events.json` does **not** imply permission to touch the live calendar.

---

# 16. Calendar safety

Never create, modify, move, or delete live calendar events unless the user's **current explicit instruction** authorizes calendar action.

A previous statement such as “eventually create my calendar” is not sufficient permission.

Before live creation, validate against `Requirements/calendar_rules.md` and `Requirements/availability.md`.

---

# 17. Editing discipline

Prefer updating the existing designated project files rather than creating new planning files.

Do not create unnecessary folders, duplicate state files, scratch files, or alternate requirement documents unless they materially improve the workflow and the user has requested or approved them.

Keep:

- human-readable reasoning in Markdown;
- structured planner state/data in JSON;
- source material under `Sources/`;
- outputs under `Output/`.

---

# 18. Minimal-read principle

Use the smallest sufficient context for the current task.

Examples:

### If asked to estimate DBMS revision time
Read:
- `Planning/source_map.json`
- `Sources/Placement/Core/DBMS.md`
- existing DBMS entry in `Planning/workload_estimates.json`
- only the relevant requirement section if needed

Do **not** load all project notes, all midsem notes, or the entire calendar rulebook.

### If asked to choose which CV class to attend
Read:
- `Requirements/availability.md`
- current task schedule/inventory
- relevant approved constraints

Do **not** reread all technical notes.

### If asked to build the final calendar event descriptions
Read:
- `Output/final_plan.md`
- `Requirements/calendar_rules.md`
- `Requirements/planner_description.md` where slot meaning is needed
- `Planning/resource_research.md`

Do **not** redo workload estimation unless a contradiction is found.

---

# 19. Final operating principle

For every task, ask internally:

> **What is the smallest set of files I need to read, what prior work can I reuse, and where should I persist the result?**

Use this file as the routing map.

Use `Requirements/` for rules.
Use `Sources/` for raw material.
Use `Planning/` for analysis.
Use `State/` for approved/current state.
Use `Output/` for planner deliverables.

Do not get lost in the repository, and do not redo work that has already been completed and saved.