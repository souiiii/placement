# AGENTS.md — Codex Navigation Guide

## Purpose

This file tells Codex **where to look, what to read, what to update, and how to avoid unnecessary work**.

It is a routing guide, not a duplicate of the planner requirements.

Detailed rules live in `Requirements/`.

---

# 1. Core operating rule

> **Use the smallest amount of context needed for the current task.**

Do not recursively read or deeply analyze the repository.

For planning, Codex usually only needs to understand:

- what each source is;
- which track it belongs to;
- whether it is primary, supporting, practice-oriented, optional, or pending;
- its approximate size/density;
- its major sections/topics;
- enough information to estimate a realistic duration.

Codex does **not** need to fully understand, summarize, fact-check, rewrite, or memorize study notes in order to build the planner.

---

# 2. Cheap source-inspection protocol

When estimating or classifying a source, use this order:

1. filename/path;
2. file metadata;
3. size / line count / word count / page count;
4. headings / table of contents / section titles;
5. a small targeted sample only if needed.

Stop as soon as **scope + role + rough workload** are clear.

Do not by default:

- read large Markdown files line-by-line;
- inspect every code block/example;
- parse every embedded image;
- deeply compare paired notes;
- summarize entire sources;
- load all of `Sources/` into context;
- reopen raw notes after workload estimates have already been saved.

A recursive **directory listing** is allowed. Recursive **content analysis** is not.

---

# 3. Project map

```text
placement/
├── AGENTS.md
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

# 4. Routing table

| Need | Read |
|---|---|
| Overall goals, priorities, required tracks, feasibility rules | `Requirements/master_requirements.md` |
| Dates, hours, meals, classes, attendance, namaz | `Requirements/availability.md` |
| Meaning of planner slot types | `Requirements/planner_description.md` |
| Calendar naming, descriptions, resources, event rules | `Requirements/calendar_rules.md` |
| Raw study material | only the relevant file under `Sources/` |
| Logical source grouping / source role | `Planning/source_map.json` |
| Existing time estimates | `Planning/workload_estimates.json` |
| Required tasks and dependencies | `Planning/task_inventory.json` |
| Chosen external resources | `Planning/resource_research.md` |
| Important prior decisions | `Planning/planning_decisions.md` |
| Capacity / overload result | `Planning/feasibility.md` |
| Current phase | `State/planner_state.json` |
| Approved constraints | `State/approved_constraints.json` |
| Approved cuts | `State/approved_cuts.json` |
| Proposed schedule | `Output/draft_plan.md` |
| Approved schedule | `Output/final_plan.md` |
| Calendar-ready events | `Output/calendar_events.json` |

---

# 5. Authority order

If information conflicts:

1. user's newest explicit instruction;
2. user-approved state in `State/`;
3. `Requirements/master_requirements.md`;
4. `Requirements/availability.md`;
5. `Requirements/planner_description.md`;
6. `Requirements/calendar_rules.md`;
7. existing `Planning/` analysis;
8. Codex inference.

Do not override an approved requirement for convenience.

---

# 6. Planning workflow

Use this sequence:

```text
1. Read relevant requirements/state
2. Inventory Sources/ using metadata
3. Build/update source_map.json
4. Estimate workload using size + headings + minimal targeted reading
5. Research only external resources that are actually needed
6. Build/update task_inventory.json
7. Calculate realistic available capacity
8. Run feasibility analysis
9. If infeasible, stop and ask for trade-off approval
10. Build draft plan
11. Validate hard constraints/dependencies
12. Present for approval
13. Produce final plan
14. Prepare calendar_events.json
15. Create live calendar events only when explicitly requested
```

Do not skip feasibility.

Do not use Step 4 as a deep note-analysis phase.

---

# 7. Source mapping rules

A file is not automatically a calendar block.

Do not assume:

- one file = one block;
- one folder = one day;
- every source deserves dedicated time.

Use `Planning/source_map.json` to record logical units and source roles.

Useful source roles:

- `primary_revision`
- `practice_reference`
- `supporting_embedded`
- `scope_definition`
- `optional_or_redundant`
- `pending_or_incomplete`

Important established mappings should be taken from the requirements/source structure rather than rediscovered through deep analysis.

Examples:

- paired RecSys ChatGPT + Codex files form one logical unit per unit;
- DSA pattern/mistake files are supporting references;
- JSON and Java Collections are supporting material;
- MongoDB reference material is inside `Node_Backend.md`;
- JavaScript notes are reference material, while JS preparation is practice-oriented;
- IWT scope is defined by its README;
- the LSEG JD is the primary role-specific source.

---

# 8. Workload estimation

The goal is a **realistic duration estimate**, not a source summary.

Estimate using:

- size / word count / page count;
- number of major sections;
- source role;
- whether the user is revising or learning;
- whether active practice is required;
- cognitive density;
- whether several files form one logical unit;
- required verification/questionnaire/mock time.

Store compact evidence in `Planning/workload_estimates.json`.

Example:

```json
{
  "id": "os_revision",
  "source": "Sources/Placement/Core/OS.md",
  "role": "primary_revision",
  "inspection": "metadata+headings",
  "estimated_minutes": 150,
  "confidence": "medium"
}
```

Do not store detailed chapter summaries.

If confidence is low because material is incomplete or unusually dense, mark the estimate provisional instead of automatically reading the entire source.

---

# 9. When deeper reading is justified

Read deeper only when a specific planning question cannot be answered cheaply.

Examples:

- the source has no useful headings;
- two sources may be heavily redundant and that decision materially affects feasibility;
- a JD section must be checked for topic relevance;
- an exact OA/question sheet must be inspected to determine question type/count;
- the user explicitly asks for content analysis.

Even then, read only the smallest targeted portion needed.

---

# 10. Feasibility gate

A final planner cannot be produced until feasibility is checked.

If required workload exceeds realistic capacity:

1. stop;
2. record the overload in `Planning/feasibility.md`;
3. separate required, desirable, and redundant/optional work;
4. propose trade-offs;
5. ask the user for approval;
6. put only approved removals in `State/approved_cuts.json`.

Never silently:

- drop required work;
- shrink durations unrealistically;
- treat suggested cuts as approved.

Feasibility should use:

- `workload_estimates.json`;
- `task_inventory.json`;
- `availability.md`;
- approved state.

Do **not** reopen raw study notes during feasibility unless an estimate is missing or stale.

---

# 11. External resource research

Check `Planning/resource_research.md` before researching.

Research only for the exact task that needs it.

Prefer:

- short targeted videos when equally suitable;
- strong written/documentation resources when better;
- real practice platforms/problem sets for practice blocks;
- high signal-to-time ratio.

Avoid broad courses/playlists for narrow tasks.

Save final useful selections in `Planning/resource_research.md` so later stages do not research them again.

---

# 12. Persistence and reuse

Save planning work here:

| Result | Save to |
|---|---|
| Source role/grouping/status | `Planning/source_map.json` |
| Duration estimate | `Planning/workload_estimates.json` |
| Required task/dependency | `Planning/task_inventory.json` |
| External resource choice | `Planning/resource_research.md` |
| Important decision | `Planning/planning_decisions.md` |
| Feasibility result | `Planning/feasibility.md` |
| Current phase | `State/planner_state.json` |
| Approved constraint | `State/approved_constraints.json` |
| Approved cut | `State/approved_cuts.json` |
| Proposed schedule | `Output/draft_plan.md` |
| Approved schedule | `Output/final_plan.md` |
| Calendar-ready events | `Output/calendar_events.json` |

Before repeating work, check whether it already exists.

If new source material arrives, update only the affected:

- source-map entry;
- estimate;
- task;
- feasibility calculation;
- schedule section.

Do not rerun the entire project unnecessarily.

---

# 13. Calendar safety

Never create, modify, move, or delete live calendar events unless the user's **current explicit instruction** authorizes it.

A final plan or `calendar_events.json` is not permission to touch the live calendar.

---

# 14. Minimal-read examples

## Estimate a large note

```text
1. check source_map.json
2. measure file size/words
3. extract headings
4. inspect a small sample only if necessary
5. estimate duration
6. save estimate
```

Do not read the full note unless there is a specific unresolved planning question.

## RecSys

Treat each ChatGPT + Codex pair as one logical unit.

Use combined size + headings + revision status.

Do not deeply compare the pair.

## Feasibility

Use saved estimates and task inventory.

Do not reopen raw sources.

## Draft/final planner

Use requirements, approved state, estimates, inventory, feasibility, and resource research.

Do not redo source analysis.

---

# 15. Final operating principle

For every task, ask:

> **What is the minimum information I need to understand the scope and estimate the time accurately?**

Use:

- `Requirements/` for rules;
- `Sources/` for lightweight scope/size inspection;
- `Planning/` for reusable analysis;
- `State/` for approved/current decisions;
- `Output/` for planner deliverables.

The planner should be accurate because Codex understands **scope and workload**, not because it deeply read every study note.
