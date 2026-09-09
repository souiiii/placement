# Draft preparation plan — 10 to 16 September 2026

**Status: APPROVED as the scheduling baseline (9 September 2026).** This file is retained as the approved draft record. The finalized plan is `Output/final_plan.md` and the calendar-ready event data is `Output/calendar_events.json`; both are substantively identical to this draft. No live calendar event has been created (`calendar_rules.md` §2, `master_requirements.md` §37, `AGENTS.md` §13).

Every nonzero task in `Planning/task_inventory.json` is scheduled exactly once, at its accepted duration. No estimate, duration, scope, source mapping or approved constraint was changed. The day-level split reproduces the approved feasibility partition in `Planning/feasibility.md` exactly, day for day.

| | Minutes | Hours |
|---|---:|---:|
| LSEG / placement preparation | 2,365 | 39h 25m |
| Final mixed mock + debrief | 135 | 2h 15m |
| Midsem preparation (incl. 45 conditional) | 1,065 | 17h 45m |
| **Total scheduled preparation** | **3,565** | **59h 25m** |
| Protected rest / transition / contingency | 1,050 | 17h 30m |
| True unused slack (Tue 22:25–22:30, labelled) | 5 | 0h 05m |

## How the week is shaped

Coverage first, consolidation last. Core theory and the DSA pattern base open the week (Thu–Fri); the practice chains and the bulk of DSA sit in the middle (Sat); OA work and timed solving land on Sunday; Monday's lab-fragmented day carries the shorter web/tech tracks and the first project questionnaire; Tuesday closes the OA set, DSA review and the remaining project sessions; Wednesday is entirely consolidation — resume, role/company, HR, aptitude, the last questionnaire — then the mock. Demanding technical work is placed early in each day, oral rehearsal later. DSA appears on five separate days. Only the mandatory Monday lab is attended; no optional class is scheduled.

---

## Daily schedule

### Thursday 10 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–10:30 | ⚙️ OS — Targeted Refresh | `os.prepare` (90) | LSEG | 90 |
| 10:30–10:45 | ☕ Break | — | Rest/buffer | 15 |
| 10:45–12:15 | 🌐 CN — Targeted Refresh | `cn.prepare` (90) | LSEG | 90 |
| 12:15–13:00 | 🛑 Rest / Buffer | — | Rest/buffer | 45 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:15 | 🗃️ DBMS — Targeted Refresh | `dbms.prepare` (75) | LSEG | 75 |
| 15:15–15:45 | ☕ Break | — | Rest/buffer | 30 |
| 15:45–16:15 | 🧩 DSA — Pattern Refresh | `dsa.refresh` (30) | LSEG | 30 |
| 16:15–18:00 | 🧩 DSA — Practice (Part 1) | `dsa.practice` (105) | LSEG | 105 |
| 18:00–18:30 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 18:30–19:30 | 🧠 RecSys — Unit 1 (Part 1) | `recsys_unit_1.prepare` (60) | Midsem | 60 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–22:00 | 🧠 RecSys — Unit 1 (Part 2) | `recsys_unit_1.prepare` (90) | Midsem | 90 |
| 22:00–22:30 | 🌙 Wind Down | — | Rest/buffer | 30 |

**Totals —** LSEG **390**, midsem **150**, fixed commitments **120**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–10:30 · ⚙️ OS — Targeted Refresh** — Refresh high-value and weak OS areas from `Sources/Placement/Core/OS.md` using retrieval first, then work the applied checks. Explain answers aloud and open the notes only to close gaps; this block also carries the OS closure check, so no separate verification slot exists.
- **10:45–12:15 · 🌐 CN — Targeted Refresh** — Refresh networking from `Sources/Placement/Core/CN.md` by recalling the high-value layers, protocols and trade-offs before reading. Verify weak explanations inside this block; CN closure is integrated here.
- **14:00–15:15 · 🗃️ DBMS — Targeted Refresh** — Refresh database concepts and reasoning from `Sources/Placement/Core/DBMS.md`. This must come before tomorrow's SQL chain, whose review block carries the DBMS closure check — do not add a separate DBMS verification session.
- **15:45–16:15 · 🧩 DSA — Pattern Refresh** — Use `Sources/Placement/Supporting/DSA_Pattern_Index.md` and the mistake log to re-fix the major interview patterns before solving starts. Targeted refresh only — no full notes pass.
- **16:15–18:00 · 🧩 DSA — Practice (Part 1)** — Solve representative problems from [LeetCode Top Interview 150](https://leetcode.com/studyplan/top-interview-150/) in Java, guided by the pattern index. Name the pattern, implement, and explain complexity during the attempt. Breadth over volume; completing the collection is not the goal.
- **18:30–19:30 · 🧠 RecSys — Unit 1 (Part 1)** — Work `Sources/Midsem/RecSys/unit1_chatgpt.md` and `unit1_codex.md` side by side as one logical unit. Cover concepts and methods with recall built in; no separate consolidation pass is scheduled.
- **20:30–22:00 · 🧠 RecSys — Unit 1 (Part 2)** — Continue the paired Unit 1 sources, finishing the methods and worked examples. Explain each method in your own words before checking it.

</details>

### Friday 11 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–10:15 | ☕ Java / OOP — Targeted Refresh | `java_oop.prepare` (75) | LSEG | 75 |
| 10:15–10:30 | ☕ Break | — | Rest/buffer | 15 |
| 10:30–12:30 | 🟩 Node.js / Backend — Targeted Refresh | `node_backend.prepare` (120) | LSEG | 120 |
| 12:30–13:00 | 🕌 Namaz | — | Fixed — namaz | 30 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:00 | 🕌 Namaz | — | Fixed — namaz | 60 |
| 15:00–15:30 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 15:30–16:40 | 🗃️ SQL — Refresh & Practice | `sql_practice.refresh` (10)<br>`sql_practice.practice` (60) | LSEG | 70 |
| 16:40–16:55 | ☕ Break | — | Rest/buffer | 15 |
| 16:55–17:30 | 🗃️ SQL — Timed Set & Error Review | `sql_practice.timed` (20)<br>`sql_practice.review` (15) | LSEG | 35 |
| 17:30–19:00 | 🧠 RecSys — Unit 2 (Part 1) | `recsys_unit_2.prepare` (90) | Midsem | 90 |
| 19:00–19:30 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–21:30 | 🧠 RecSys — Unit 2 (Part 2) | `recsys_unit_2.prepare` (60) | Midsem | 60 |
| 21:30–22:30 | 🌙 Wind Down | — | Rest/buffer | 60 |

**Totals —** LSEG **300**, midsem **150**, fixed commitments **210**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

Friday's protected 12:30–15:00 namaz window is shown as two namaz events with the fixed 13:00–14:00 lunch between them, so both protected periods appear explicitly and nothing overlaps. No preparation of any kind sits inside 12:30–15:00.

<details><summary>Session briefs</summary>

- **09:00–10:15 · ☕ Java / OOP — Targeted Refresh** — Check OOP and the relevant Collections through explanation and short implementation using `Sources/Placement/Core/Java_OOP.md` and the Collections reference. Java is the interview language, so write code rather than only reading. Closure is integrated here.
- **10:30–12:30 · 🟩 Node.js / Backend — Targeted Refresh** — Refresh backend concepts from `Sources/Placement/Core/Node_Backend.md`, using the JSON and Redis references where they come up. This precedes tomorrow's MongoDB chain, whose review block carries the backend closure check.
- **15:30–16:40 · 🗃️ SQL — Refresh & Practice** — Take the short syntax refresh you actually need, then write queries from [LeetCode SQL 50](https://leetcode.com/studyplan/top-sql-50/) — joins, grouping, subqueries, window functions. Use the DBMS notes only to unblock a concept; this is execution, not theory.
- **16:55–17:30 · 🗃️ SQL — Timed Set & Error Review** — Solve a distinct timed set, then review only the errors. Close with a brief DBMS reasoning check — this is the recorded DBMS closure checkpoint, so no extra DBMS session follows.
- **17:30–19:00 · 🧠 RecSys — Unit 2 (Part 1)** — Work `unit2_chatgpt.md` and `unit2_codex.md` side by side as one logical unit, covering concepts and methods with recall built in.
- **20:30–21:30 · 🧠 RecSys — Unit 2 (Part 2)** — Finish the paired Unit 2 sources, prioritising the methods and numerical steps you cannot yet reproduce unaided.

</details>

### Saturday 12 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–10:30 | 🏗️ System Design — Targeted Refresh | `system_design.prepare` (90) | LSEG | 90 |
| 10:30–10:45 | ☕ Break | — | Rest/buffer | 15 |
| 10:45–12:00 | 🍃 MongoDB — Refresh & Practice | `mongodb_practice.refresh` (10)<br>`mongodb_practice.practice` (65) | LSEG | 75 |
| 12:00–12:15 | 🍃 MongoDB — Review & Backend Closure | `mongodb_practice.review` (15) | LSEG | 15 |
| 12:15–13:00 | 🛑 Rest / Buffer | — | Rest/buffer | 45 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:20 | ⚡ JavaScript — Refresh & Practice | `javascript_practice.refresh` (10)<br>`javascript_practice.practice` (70) | LSEG | 80 |
| 15:20–15:35 | ☕ Break | — | Rest/buffer | 15 |
| 15:35–16:15 | ⚡ JavaScript — Timed Set & Review | `javascript_practice.timed` (25)<br>`javascript_practice.review` (15) | LSEG | 40 |
| 16:15–16:45 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 16:45–18:15 | 🧩 DSA — Practice (Part 2) | `dsa.practice` (90) | LSEG | 90 |
| 18:15–18:30 | ☕ Break | — | Rest/buffer | 15 |
| 18:30–19:30 | 🧠 RecSys — Unit 3 (Part 1) | `recsys_unit_3.prepare` (60) | Midsem | 60 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–22:00 | 🧠 RecSys — Unit 3 (Part 2) | `recsys_unit_3.prepare` (90) | Midsem | 90 |
| 22:00–22:30 | 🌙 Wind Down | — | Rest/buffer | 30 |

**Totals —** LSEG **390**, midsem **150**, fixed commitments **120**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–10:30 · 🏗️ System Design — Targeted Refresh** — Walk one focused design discussion using `Sources/Placement/Core/System_Design.md`, retrieving concepts and exposing weak trade-offs. Explanation and verification happen inside this walkthrough.
- **10:45–12:00 · 🍃 MongoDB — Refresh & Practice** — Take a short query-syntax refresh, then reconstruct pipelines from the [MongoDB aggregation tutorials](https://www.mongodb.com/docs/manual/tutorial/aggregation-complete-examples/) — filtering, grouping, arrays, joins. Attempt each before reading the worked solution, then run and compare. A working environment is a prerequisite.
- **12:00–12:15 · 🍃 MongoDB — Review & Backend Closure** — Review only the pipelines you got wrong, then close with a brief backend reasoning check. This is the recorded Node/backend closure checkpoint.
- **14:00–15:20 · ⚡ JavaScript — Refresh & Practice** — Refresh only the syntax you need, then solve selected exercises from [30 Days of JavaScript](https://leetcode.com/studyplan/30-days-of-javascript/). `Sources/Placement/Tech/JavaScript.md` is reference material — do not turn this into a reading block.
- **15:35–16:15 · ⚡ JavaScript — Timed Set & Review** — Solve a distinct set under a timer, then review errors and flag anything worth re-exposure. Do not repeat the whole practice pass.
- **16:45–18:15 · 🧩 DSA — Practice (Part 2)** — Continue representative problems from Top Interview 150 in Java, deliberately covering patterns you have not touched yet this week. Explain the approach and complexity as you solve.
- **18:30–19:30 · 🧠 RecSys — Unit 3 (Part 1)** — Work `unit3_chatgpt.md` and `unit3_codex.md` side by side as one logical unit, covering concepts and methods with recall built in.
- **20:30–22:00 · 🧠 RecSys — Unit 3 (Part 2)** — Finish the paired Unit 3 sources. This completes all three units, which the Wednesday final revision depends on.

</details>

### Sunday 13 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–09:45 | 🧩 DSA — Practice (Part 3) | `dsa.practice` (45) | LSEG | 45 |
| 09:45–10:00 | ☕ Break | — | Rest/buffer | 15 |
| 10:00–11:30 | 🧩 DSA — Timed Solving | `dsa.timed` (90) | LSEG | 90 |
| 11:30–12:00 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 12:00–12:50 | 💹 LSEG OA — Task 1: Market Data Integrity | `lseg_oa_task_1.prepare` (50) | LSEG | 50 |
| 12:50–13:00 | ☕ Break | — | Rest/buffer | 10 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:10 | 💹 LSEG OA — Task 2: Hierarchical Risk Limits | `lseg_oa_task_2.prepare` (70) | LSEG | 70 |
| 15:10–15:30 | ☕ Break | — | Rest/buffer | 20 |
| 15:30–16:40 | 💹 LSEG OA — Task 5: SLA Window Breaches | `lseg_oa_task_5.prepare` (70) | LSEG | 70 |
| 16:40–17:10 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 17:10–17:45 | 📄 Velvet — Revision | `project_velvet.revision` (35) | LSEG | 35 |
| 17:45–18:15 | 📄 Relay — Revision | `project_relay.revision` (30) | LSEG | 30 |
| 18:15–18:30 | ☕ Break | — | Rest/buffer | 15 |
| 18:30–19:30 | ⚡ EPQ — Theory Refresh | `epq_full_notes.consolidate` (60) | Midsem | 60 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–22:00 | 🎨 IWT — Web Fundamentals + HTML/CSS | `iwt.prepare` (90) | Midsem | 90 |
| 22:00–22:30 | 🌙 Wind Down | — | Rest/buffer | 30 |

**Totals —** LSEG **390**, midsem **150**, fixed commitments **120**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–09:45 · 🧩 DSA — Practice (Part 3)** — Close out the representative-problem pass with the patterns still uncovered. This is the last practice block — timed solving depends on it.
- **10:00–11:30 · 🧩 DSA — Timed Solving** — Solve distinct, previously unattempted problems under interview time pressure in Java. Commit to an approach quickly, state complexity, and log what went wrong for Tuesday's review. General DSA stays separate from the OA track.
- **12:00–12:50 · 💹 LSEG OA — Task 1: Market Data Integrity** — Re-read `Sources/LSEG/OA/Major/Task_1_Market_Data_Integrity.md`, refresh the map/set processing rules, then implement once in Java with tests and complexity discussed inside the attempt. Note the recorded source-fidelity caveat on this task.
- **14:00–15:10 · 💹 LSEG OA — Task 2: Hierarchical Risk Limits** — Work `Task_2_Hierarchical_Risk_Limits.md`: refresh hierarchy, inherited limits and violation rules, then write a substantive Java implementation and test the edge cases. Be able to talk through the design, not just reproduce it.
- **15:30–16:40 · 💹 LSEG OA — Task 5: SLA Window Breaches** — Work `Task_5_Monitoring_SLA_Window_Breaches.md`. Re-establish the sliding-window/deque invariants, implement once in Java, and combine edge-case and complexity checking into the same attempt.
- **17:10–17:45 · 📄 Velvet — Revision** — Refresh Velvet's architecture, decisions and implementation details from `Sources/Projects/Velvet.md` and note cues for likely follow-ups. Tomorrow's questionnaire depends on this session.
- **17:45–18:15 · 📄 Relay — Revision** — Refresh Relay's architecture, decisions and implementation details from `Sources/Projects/Relay.md`. Its questionnaire is on Tuesday.
- **18:30–19:30 · ⚡ EPQ — Theory Refresh** — Refresh EPQ theory by retrieval, using `Sources/Midsem/EPQ/notes.md` for targeted lookup rather than a linear pass. Numerical execution is handled in Tuesday's revision-notes block.
- **20:30–22:00 · 🎨 IWT — Web Fundamentals + HTML/CSS** — Use MDN's [How the web works](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/How_the_web_works) for clients/servers, DNS, TCP/IP, HTTP and URLs, then do the [HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Test_your_skills) and [CSS](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Test_your_skills) skills exercises. `Sources/Midsem/IWT/README.md` fixes the scope — stop at CSS.

</details>

### Monday 14 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–09:30 | 🔧 Git / GitHub — Workflow Refresh | `git_github.prepare` (30) | LSEG | 30 |
| 09:30–10:00 | 🚶 Transition / Break | — | Rest/buffer | 30 |
| 10:00–12:00 | 🏫 IWT — Lab (Mandatory) | — | Fixed — class | 120 |
| 12:00–12:15 | 🚶 Transition / Break | — | Rest/buffer | 15 |
| 12:15–13:00 | 🤖 AI Fundamentals — Concept Refresh | `ai_fundamentals.prepare` (45) | LSEG | 45 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:30 | ⚛️ React — Targeted Refresh | `react.prepare` (90) | LSEG | 90 |
| 15:30–15:50 | ☕ Break | — | Rest/buffer | 20 |
| 15:50–16:35 | ▲ Next.js — Targeted Refresh | `nextjs.prepare` (45) | LSEG | 45 |
| 16:35–16:50 | ☕ Break | — | Rest/buffer | 15 |
| 16:50–17:35 | 🔷 TypeScript — Targeted Refresh | `typescript.prepare` (45) | LSEG | 45 |
| 17:35–18:15 | 🛑 Rest / Buffer | — | Rest/buffer | 40 |
| 18:15–19:00 | 🎤 Velvet — Questionnaire | `project_velvet.questionnaire` (45) | LSEG | 45 |
| 19:00–19:30 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–22:30 | 👁️ CV — Active Coverage (Part 1) | `cv.reserved_preparation` (120) | Midsem | 120 |

**Totals —** LSEG **300**, midsem **120**, fixed commitments **240**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–09:30 · 🔧 Git / GitHub — Workflow Refresh** — Short rehearsal of the everyday workflow from `Sources/Placement/Tech/Git_GitHub.md` — branching, merge vs rebase, conflict resolution, undoing mistakes. Explain each aloud; this is a tool you already use.
- **10:00–12:00 · 🏫 IWT — Lab (Mandatory)** — Mandatory IWT lab attendance. This is not study time and does not replace today's midsem self-study block.
- **12:15–13:00 · 🤖 AI Fundamentals — Concept Refresh** — Refresh the key concepts in `Sources/Placement/Tech/AI_Fundamentals.md` through interview-style explanations. The OA evaluation-metric reasoning has its own short slot on Tuesday.
- **14:00–15:30 · ⚛️ React — Targeted Refresh** — Targeted behavioural and code checks against `Sources/Placement/Tech/React.md` — rendering, state, effects, keys, performance. Reason about small snippets rather than rereading the note; React closure is integrated here.
- **15:50–16:35 · ▲ Next.js — Targeted Refresh** — Refresh routing, rendering strategies and the decisions you actually made in your projects, using `Sources/Placement/Tech/NextJS.md`. Check by applying, not by rereading.
- **16:50–17:35 · 🔷 TypeScript — Targeted Refresh** — Refresh the type system from `Sources/Placement/Tech/TypeScript.md` with short typed snippets — generics, narrowing, utility types. Familiar material, so keep it applied.
- **18:15–19:00 · 🎤 Velvet — Questionnaire** — Use ChatGPT for a full Velvet questionnaire. Answer aloud without notes unless stuck, and let it probe architecture, implementation, trade-offs, security, scalability and your own contribution. Brief feedback is included in this slot.
- **20:30–22:30 · 👁️ CV — Active Coverage (Part 1)** — Mandatory active CV preparation, reserved pending reliable lecturer material. Work whatever confirmed scope exists when the block starts; do not invent topics from unrelated old papers. Today's IWT lab does not substitute for this block.

</details>

### Tuesday 15 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–10:00 | 💹 LSEG OA — Task 6: Portfolio Risk Metrics | `lseg_oa_task_6.prepare` (60) | LSEG | 60 |
| 10:00–10:15 | ☕ Break | — | Rest/buffer | 15 |
| 10:15–10:40 | 💹 LSEG OA — Task 3: DFS Cycle Detection Bugfix | `lseg_oa_task_3.prepare` (25) | LSEG | 25 |
| 10:40–10:55 | 💹 LSEG OA — Task 4: Order Book Zero-Quantity Bugfix | `lseg_oa_task_4.prepare` (15) | LSEG | 15 |
| 10:55–11:10 | 💹 LSEG OA — Task 7: Classification Evaluation Recap | `lseg_oa_task_7.prepare` (15) | LSEG | 15 |
| 11:10–11:40 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 11:40–12:40 | 🐍 Python — Language Refresh | `python.prepare` (60) | LSEG | 60 |
| 12:40–13:00 | ☕ Break | — | Rest/buffer | 20 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:00 | 🧩 DSA — Error Review & Re-exposure | `dsa.review` (60) | LSEG | 60 |
| 15:00–15:20 | ☕ Break | — | Rest/buffer | 20 |
| 15:20–16:00 | 🎤 Relay — Questionnaire | `project_relay.questionnaire` (40) | LSEG | 40 |
| 16:00–16:35 | 📄 Eventually — Revision | `project_eventually.revision` (35) | LSEG | 35 |
| 16:35–17:05 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 17:05–18:20 | ⛓️ Blockchain — Expected Question Set | `blockchain.prepare` (75) | Midsem | 75 |
| 18:20–19:20 | 👁️ CV — Active Coverage (Part 2) | `cv.reserved_preparation` (60) | Midsem | 60 |
| 19:20–19:30 | ☕ Break | — | Rest/buffer | 10 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–22:00 | ⚡ EPQ — Numericals & Cross-topic Revision | `epq_revision.consolidate` (90) | Midsem | 90 |
| 22:00–22:25 | 🌙 Wind Down | — | Rest/buffer | 25 |
| 22:25–22:30 | 🕓 Unused Slack | — | Unused slack | 5 |

**Totals —** LSEG **310**, midsem **225**, fixed commitments **120**, protected rest/buffer **150**, true unused slack **5** · day total **805** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–10:00 · 💹 LSEG OA — Task 6: Portfolio Risk Metrics** — Work `Task_6_Portfolio_Risk_Metrics.md`: refresh the preserved probability and boundary rules, implement once in Java, and test and explain in the same attempt.
- **10:15–10:40 · 💹 LSEG OA — Task 3: DFS Cycle Detection Bugfix** — Trace the state-tracking bug in `Task_3_DFS_Cycle_Detection_Bugfix.md` and produce a counterexample plus the fix. Focused debugging, not full algorithm reconstruction; note the recorded source-fidelity caveat.
- **10:40–10:55 · 💹 LSEG OA — Task 4: Order Book Zero-Quantity Bugfix** — Short trace of the zero-quantity deletion fix in `Task_4_Order_Book_Zero_Quantity_Bugfix.md`, covering edge cases and the explanation you would give an interviewer.
- **10:55–11:10 · 💹 LSEG OA — Task 7: Classification Evaluation Recap** — Check the preserved evaluation reasoning in `Task_7_Classification_Evaluation_Multiple_Select.md` with ChatGPT. The original options are missing — discuss only what is preserved and do not invent them or redo AI fundamentals.
- **11:40–12:40 · 🐍 Python — Language Refresh** — Recall and hands-on checks from `Sources/Placement/Tech/Python.md`. Java stays the interview language, so keep this to the idioms and standard-library work you would actually be asked about.
- **14:00–15:00 · 🧩 DSA — Error Review & Re-exposure** — Review only the errors and weak attempts from this week's practice and timed sets, with ChatGPT where an explanation helps. Re-attempt a small number of selected problems; do not repeat the whole pass.
- **15:20–16:00 · 🎤 Relay — Questionnaire** — Use ChatGPT for the Relay questionnaire, answering aloud and allowing follow-ups on design decisions, trade-offs, failures and your contribution. Brief feedback is included here.
- **16:00–16:35 · 📄 Eventually — Revision** — Refresh Eventually's architecture, decisions and implementation details from `Sources/Projects/Eventually.md`. Tomorrow's questionnaire depends on this session.
- **17:05–18:20 · ⛓️ Blockchain — Expected Question Set** — Work the lecturer's exact expected questions in `Sources/Midsem/Blockchain/questions.pdf`, including both gas/ether numericals. Stay inside this question set rather than expanding into broad syllabus study.
- **18:20–19:20 · 👁️ CV — Active Coverage (Part 2)** — Second reserved CV block, continuing from Monday against whatever confirmed material is available. Scope is still provisional — flag it if three hours is clearly not enough.
- **20:30–22:00 · ⚡ EPQ — Numericals & Cross-topic Revision** — Use `Sources/Midsem/EPQ/revision.md` mainly for numerical execution and cross-topic exam retrieval. Do not reread the theory already refreshed on Sunday or redo numericals you can already do.

</details>

### Wednesday 16 September 2026

| Time | Block | Task ID | Track | Min |
|---|---|---|---|---:|
| 09:00–09:45 | 📑 Resume — Review & Questioning | `resume.review` (20)<br>`resume.questionnaire` (25) | LSEG | 45 |
| 09:45–10:00 | ☕ Break | — | Rest/buffer | 15 |
| 10:00–11:15 | 🏢 LSEG — Role & Company | `lseg_role_company.study` (40)<br>`lseg_role_company.fit` (20)<br>`lseg_role_company.questionnaire` (15) | LSEG | 75 |
| 11:15–11:45 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 11:45–12:30 | 🎤 Eventually — Questionnaire | `project_eventually.questionnaire` (45) | LSEG | 45 |
| 12:30–13:00 | 🛑 Rest / Buffer | — | Rest/buffer | 30 |
| 13:00–14:00 | 🍽️ Lunch | — | Fixed — meal | 60 |
| 14:00–15:15 | 🗣️ HR — Behavioural Prep & Practice | `hr_behavioural.prepare` (20)<br>`hr_behavioural.practice` (55) | LSEG | 75 |
| 15:15–15:45 | ☕ Break | — | Rest/buffer | 30 |
| 15:45–16:30 | 🧮 Aptitude — Timed Test & Review | `aptitude.practice` (45) | LSEG | 45 |
| 16:30–17:15 | 🛑 Pre-Mock Reset | — | Rest/buffer | 45 |
| 17:15–19:15 | 🎯 LSEG — Full Mixed Mock | `final_mixed_mock.interview` (120) | Mock | 120 |
| 19:15–19:30 | 🎯 Mock — Debrief | `final_mixed_mock.debrief` (15) | Mock | 15 |
| 19:30–20:30 | 🍛 Dinner | — | Fixed — meal | 60 |
| 20:30–21:45 | 🧠 RecSys — Final Revision | `recsys_final_revision.consolidate` (75) | Midsem | 75 |
| 21:45–22:30 | 🧠 RecSys — Numericals (Conditional) | `recsys_numericals.conditional_practice` (45) | Midsem | 45 |

**Totals —** LSEG **285**, mock/debrief **135**, midsem **120**, fixed commitments **120**, protected rest/buffer **150**, true unused slack **0** · day total **810** minutes (09:00–22:30).

<details><summary>Session briefs</summary>

- **09:00–09:45 · 📑 Resume — Review & Questioning** — Refresh every meaningful claim in `Sources/Resume/submitted_resume.pdf`, then use ChatGPT for focused follow-ups with immediate feedback. The submitted version is the source of truth; do not re-run full project preparation here.
- **10:00–11:15 · 🏢 LSEG — Role & Company** — Read `Sources/LSEG/job_description.pdf` selectively alongside [LSEG About us](https://www.lseg.com/en/about-us), connect it to your actual resume experience, then close with one ChatGPT rehearsal of why LSEG, why this role and how you fit. Keep this distinct from HR practice.
- **11:45–12:30 · 🎤 Eventually — Questionnaire** — Use ChatGPT for the Eventually questionnaire, answering aloud and allowing follow-ups on architecture, trade-offs, data flow, security and improvements. Brief feedback is included here.
- **14:00–15:15 · 🗣️ HR — Behavioural Prep & Practice** — Outline your own examples against the [MIT STAR method](https://capd.mit.edu/resources/the-star-method-for-behavioral-interviews/), then run one ChatGPT rehearsal cycle across teamwork, conflict, failure, strengths and motivation. Keep answers grounded in real experience; no memorised scripts.
- **15:45–16:30 · 🧮 Aptitude — Timed Test & Review** — Take one [IndiaBIX timed aptitude test](https://www.indiabix.com/online-test/aptitude-test/) under its own timer, then review the errors in the same session. LSEG's exact assessment scope is unconfirmed, so this is a general baseline.
- **17:15–19:15 · 🎯 LSEG — Full Mixed Mock** — Use ChatGPT for the full two-hour mixed LSEG mock: core CS, DSA and problem solving, OA follow-ups, projects, resume, HR and role/company. Treat it as a real interview, not a short verification. All LSEG preparation is complete before this block begins.
- **19:15–19:30 · 🎯 Mock — Debrief** — Capture the mock's key feedback once — the two or three things to tighten before tomorrow. Do not restart preparation or re-run the interview.
- **20:30–21:45 · 🧠 RecSys — Final Revision** — Use `Sources/Midsem/RecSys/final_revision.md` to check cross-unit connections and unresolved numerical errors after Units 1–3. Do not redo every unit exercise.
- **21:45–22:30 · 🧠 RecSys — Numericals (Conditional)** — **Conditional block — retained, not approved as a cut.** Practise only numerical methods or gaps that the units and final revision did not already cover, using `Sources/Midsem/RecSys/numericals.md`. If the final revision has just covered everything, this block can be dropped; redundancy is still unverified.

</details>

---

## 1. Daily totals

| Day | LSEG | Mock | Midsem | Scheduled prep | Fixed commitments | Protected rest | True slack | Day |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Thu 10 Sep | 390 | — | 150 | 540 | 120 | 150 | 0 | 810 |
| Fri 11 Sep | 300 | — | 150 | 450 | 210 | 150 | 0 | 810 |
| Sat 12 Sep | 390 | — | 150 | 540 | 120 | 150 | 0 | 810 |
| Sun 13 Sep | 390 | — | 150 | 540 | 120 | 150 | 0 | 810 |
| Mon 14 Sep | 300 | — | 120 | 420 | 240 | 150 | 0 | 810 |
| Tue 15 Sep | 310 | — | 225 | 535 | 120 | 150 | 5 | 810 |
| Wed 16 Sep | 285 | 135 | 120 | 540 | 120 | 150 | 0 | 810 |
| **Total** | **2,365** | **135** | **1,065** | **3,565** | **1,050** | **1,050** | **5** | **5,670** |

Fixed commitments are meals (7×120), Friday namaz (90 minutes outside the lunch hour) and the mandatory Monday IWT lab (120). None is counted as preparation. Protected rest is exactly **150 minutes every day**, and the week's only true unused slack is the separately labelled **🕓 Unused Slack, Tuesday 22:25–22:30**. It is deliberately not rest and deliberately not study.

**Finishing a block early does not create extra work.** Reclaimed time stays buffer or slack — do not pull the next block forward, extend the current one, or add unplanned study. This is the fixed-plan rule in `master_requirements.md` §5.

## 2. Task reconciliation

All **60 nonzero tasks**, each appearing exactly once at its recorded duration. The seven zero-minute verification checkpoints are deliberately absent as events: they are integrated checks inside their named hosts.

| Task ID | Scheduled | Min | Once |
|---|---|---:|:--:|
| `os.prepare` | Thu 10 Sep 09:00–10:30 | 90 | ✅ |
| `cn.prepare` | Thu 10 Sep 10:45–12:15 | 90 | ✅ |
| `dbms.prepare` | Thu 10 Sep 14:00–15:15 | 75 | ✅ |
| `dsa.refresh` | Thu 10 Sep 15:45–16:15 | 30 | ✅ |
| `dsa.practice` | Thu 10 Sep 16:15–18:00 (105m); Sat 12 Sep 16:45–18:15 (90m); Sun 13 Sep 09:00–09:45 (45m) | 240 | ✅ |
| `recsys_unit_1.prepare` | Thu 10 Sep 18:30–19:30 (60m); Thu 10 Sep 20:30–22:00 (90m) | 150 | ✅ |
| `java_oop.prepare` | Fri 11 Sep 09:00–10:15 | 75 | ✅ |
| `node_backend.prepare` | Fri 11 Sep 10:30–12:30 | 120 | ✅ |
| `sql_practice.refresh` | Fri 11 Sep 15:30–16:40 | 10 | ✅ |
| `sql_practice.practice` | Fri 11 Sep 15:30–16:40 | 60 | ✅ |
| `sql_practice.timed` | Fri 11 Sep 16:55–17:30 | 20 | ✅ |
| `sql_practice.review` | Fri 11 Sep 16:55–17:30 | 15 | ✅ |
| `recsys_unit_2.prepare` | Fri 11 Sep 17:30–19:00 (90m); Fri 11 Sep 20:30–21:30 (60m) | 150 | ✅ |
| `system_design.prepare` | Sat 12 Sep 09:00–10:30 | 90 | ✅ |
| `mongodb_practice.refresh` | Sat 12 Sep 10:45–12:00 | 10 | ✅ |
| `mongodb_practice.practice` | Sat 12 Sep 10:45–12:00 | 65 | ✅ |
| `mongodb_practice.review` | Sat 12 Sep 12:00–12:15 | 15 | ✅ |
| `javascript_practice.refresh` | Sat 12 Sep 14:00–15:20 | 10 | ✅ |
| `javascript_practice.practice` | Sat 12 Sep 14:00–15:20 | 70 | ✅ |
| `javascript_practice.timed` | Sat 12 Sep 15:35–16:15 | 25 | ✅ |
| `javascript_practice.review` | Sat 12 Sep 15:35–16:15 | 15 | ✅ |
| `recsys_unit_3.prepare` | Sat 12 Sep 18:30–19:30 (60m); Sat 12 Sep 20:30–22:00 (90m) | 150 | ✅ |
| `dsa.timed` | Sun 13 Sep 10:00–11:30 | 90 | ✅ |
| `lseg_oa_task_1.prepare` | Sun 13 Sep 12:00–12:50 | 50 | ✅ |
| `lseg_oa_task_2.prepare` | Sun 13 Sep 14:00–15:10 | 70 | ✅ |
| `lseg_oa_task_5.prepare` | Sun 13 Sep 15:30–16:40 | 70 | ✅ |
| `project_velvet.revision` | Sun 13 Sep 17:10–17:45 | 35 | ✅ |
| `project_relay.revision` | Sun 13 Sep 17:45–18:15 | 30 | ✅ |
| `epq_full_notes.consolidate` | Sun 13 Sep 18:30–19:30 | 60 | ✅ |
| `iwt.prepare` | Sun 13 Sep 20:30–22:00 | 90 | ✅ |
| `git_github.prepare` | Mon 14 Sep 09:00–09:30 | 30 | ✅ |
| `ai_fundamentals.prepare` | Mon 14 Sep 12:15–13:00 | 45 | ✅ |
| `react.prepare` | Mon 14 Sep 14:00–15:30 | 90 | ✅ |
| `nextjs.prepare` | Mon 14 Sep 15:50–16:35 | 45 | ✅ |
| `typescript.prepare` | Mon 14 Sep 16:50–17:35 | 45 | ✅ |
| `project_velvet.questionnaire` | Mon 14 Sep 18:15–19:00 | 45 | ✅ |
| `cv.reserved_preparation` | Mon 14 Sep 20:30–22:30 (120m); Tue 15 Sep 18:20–19:20 (60m) | 180 | ✅ |
| `lseg_oa_task_6.prepare` | Tue 15 Sep 09:00–10:00 | 60 | ✅ |
| `lseg_oa_task_3.prepare` | Tue 15 Sep 10:15–10:40 | 25 | ✅ |
| `lseg_oa_task_4.prepare` | Tue 15 Sep 10:40–10:55 | 15 | ✅ |
| `lseg_oa_task_7.prepare` | Tue 15 Sep 10:55–11:10 | 15 | ✅ |
| `python.prepare` | Tue 15 Sep 11:40–12:40 | 60 | ✅ |
| `dsa.review` | Tue 15 Sep 14:00–15:00 | 60 | ✅ |
| `project_relay.questionnaire` | Tue 15 Sep 15:20–16:00 | 40 | ✅ |
| `project_eventually.revision` | Tue 15 Sep 16:00–16:35 | 35 | ✅ |
| `blockchain.prepare` | Tue 15 Sep 17:05–18:20 | 75 | ✅ |
| `epq_revision.consolidate` | Tue 15 Sep 20:30–22:00 | 90 | ✅ |
| `resume.review` | Wed 16 Sep 09:00–09:45 | 20 | ✅ |
| `resume.questionnaire` | Wed 16 Sep 09:00–09:45 | 25 | ✅ |
| `lseg_role_company.study` | Wed 16 Sep 10:00–11:15 | 40 | ✅ |
| `lseg_role_company.fit` | Wed 16 Sep 10:00–11:15 | 20 | ✅ |
| `lseg_role_company.questionnaire` | Wed 16 Sep 10:00–11:15 | 15 | ✅ |
| `project_eventually.questionnaire` | Wed 16 Sep 11:45–12:30 | 45 | ✅ |
| `hr_behavioural.prepare` | Wed 16 Sep 14:00–15:15 | 20 | ✅ |
| `hr_behavioural.practice` | Wed 16 Sep 14:00–15:15 | 55 | ✅ |
| `aptitude.practice` | Wed 16 Sep 15:45–16:30 | 45 | ✅ |
| `final_mixed_mock.interview` | Wed 16 Sep 17:15–19:15 | 120 | ✅ |
| `final_mixed_mock.debrief` | Wed 16 Sep 19:15–19:30 | 15 | ✅ |
| `recsys_final_revision.consolidate` | Wed 16 Sep 20:30–21:45 | 75 | ✅ |
| `recsys_numericals.conditional_practice` | Wed 16 Sep 21:45–22:30 | 45 | ✅ |
| **Total** | | **3,565** | |

Five tasks are delivered across more than one session, which `task_inventory.json` explicitly permits ("the aggregate dependencies express the preparation-to-closure sequence, not a requirement for uninterrupted multi-hour blocks") and `master_requirements.md` §8 encourages for large units: `dsa.practice` (105+90+45, spread deliberately for breadth), the three RecSys units (150 each, split around a meal rather than sat in one 2½-hour block) and `cv.reserved_preparation` (120+60). No task marked `separate_session_required` is merged with anything: the six project sessions and the mock each hold their own block.

Blocks that combine components of one `session_group_id` — permitted by the inventory ("components sharing session_group_id can be performed in one focused session") — are SQL practice, SQL timed+review, MongoDB refresh+practice, JavaScript refresh+practice, JavaScript timed+review, resume review+questioning (recorded as `separate_session_required: false`), role/company study+fit+questionnaire, and HR prep+practice. Components run inside each block in dependency order.

## 3. Dependency validation

| Chain | Order as scheduled | Result |
|---|---|:--:|
| Velvet: revision → questionnaire | Sun 13 Sep 17:10 → Mon 14 Sep 18:15 | **PASS** |
| Eventually: revision → questionnaire | Tue 15 Sep 16:00 → Wed 16 Sep 11:45 | **PASS** |
| Relay: revision → questionnaire | Sun 13 Sep 17:45 → Tue 15 Sep 15:20 | **PASS** |
| DSA: refresh → practice → timed → review | Thu 15:45 → Thu/Sat/Sun (last ends Sun 09:45) → Sun 10:00 → Tue 14:00 | **PASS** |
| DBMS → SQL chain → DBMS closure | `dbms.prepare` Thu 14:00 → SQL refresh/practice/timed Fri → `sql_practice.review` Fri 17:15–17:30 hosts `dbms.verify` | **PASS** |
| Node/backend → MongoDB chain → backend closure | `node_backend.prepare` Fri 10:30 → MongoDB refresh/practice Sat → `mongodb_practice.review` Sat 12:00–12:15 hosts `node_backend.verify` | **PASS** |
| JavaScript: refresh → practice → timed → review | Sat 14:00–15:20 then 15:35–16:15, in order inside each block | **PASS** |
| RecSys: Units 1–3 → final revision → conditional numericals | Thu / Fri / Sat → Wed 20:30 → Wed 21:45 | **PASS** |
| EPQ: full notes → revision notes | Sun 13 Sep 18:30 → Tue 15 Sep 20:30 | **PASS** |
| Resume: review → questionnaire; review → role/company fit | Wed 09:00 → 09:20 (same block, in order) → fit 10:40 | **PASS** |
| Role/company: study → fit → questionnaire | Wed 10:00 → 10:40 → 11:00, in order inside one block | **PASS** |
| HR: prepare → practice | Wed 14:00 → 14:20, in order inside one block | **PASS** |
| Integrated checkpoints (7 zero-minute) | Each host scheduled before the mock; no separate event created | **PASS** |
| Mock: all 30 prerequisites → interview → debrief | Last prerequisite `aptitude.practice` ends Wed 16:30; mock 17:15; debrief 19:15 | **PASS** |

The binding constraint is the mock: the latest LSEG prerequisite finishes at **16:30 on 16 September**, 45 minutes before the 17:15 start, with a labelled pre-mock reset in between.

## 4. Requirement validation

| # | Requirement | Source | Result |
|---|---|---|:--:|
| 1 | Planning window 10–16 Sep inclusive, all seven days scheduled | master §27, availability §1 | **PASS** |
| 2 | No preparation before 09:00 or after 22:30 | master §27, availability §2, calendar §33 | **PASS** |
| 3 | Lunch 13:00–14:00 protected and explicit, every day | availability §3, calendar §29 | **PASS** |
| 4 | Dinner 19:30–20:30 protected and explicit, every day | availability §3, calendar §29 | **PASS** |
| 5 | Friday 12:30–15:00 fully reserved for namaz, no preparation | availability §9, calendar §30 | **PASS** |
| 6 | Mandatory Monday IWT lab 10:00–12:00 preserved | availability §8, approved_constraints | **PASS** |
| 7 | No percentage attendance requirement; no optional class scheduled | `State/approved_constraints.json` (supersedes master §28 / availability §6, §11) | **PASS** |
| 8 | Class time never counted as preparation | availability §6, §12; planner §26 | **PASS** |
| 9 | Genuine midsem self-study block every single day | master §20, §26; availability §5 | **PASS** |
| 10 | Realistic rest/buffer present, clearly labelled, never study | availability §4, planner §23, calendar §31 | **PASS** |
| 11 | Every period inside the active day intentionally represented; no unexplained gaps | calendar §3, master §30 | **PASS** |
| 12 | Each project: revision before questionnaire, six separate sessions | master §15, planner §8–9 | **PASS** |
| 13 | Final mixed mock on the night of 16 Sep, after major preparation | master §34, availability §15 | **PASS** |
| 14 | No heavy new learning immediately before the mock | master §34, planner §21 | **PASS** |
| 15 | End-of-week taper toward consolidation | master §33, availability §15 | **PASS** |
| 16 | DSA breadth-oriented and distributed, kept separate from OA | master §13, §14 | **PASS** |
| 17 | All 7 OA tasks scheduled; not counted as general DSA | master §14, planner §7 | **PASS** |
| 18 | Practice tracks get practice resources, not lecture-watching | master §12, §29; calendar §12 | **PASS** |
| 19 | ChatGPT-driven slots identified explicitly | calendar §14, master §3.2 | **PASS** |
| 20 | Resource links attached to the blocks that need them | master §29, calendar §9–11 | **PASS** |
| 21 | Every study block has a compact description in complete sentences | master §31, calendar §6–8 | **PASS** |
| 22 | Natural, non-robotic event titles | master §30, calendar §4–5 | **PASS** |
| 23 | RecSys treated as logical units; split parts named naturally | master §22, calendar §25 | **PASS** |
| 24 | CV preserved as mandatory active track; no invented scope | master §23, calendar §26 | **PASS** |
| 25 | Blockchain kept to the lecturer's question set incl. both numericals | master §24, calendar §27 | **PASS** |
| 26 | IWT kept to confirmed scope through CSS | master §25, planner §19 | **PASS** |
| 27 | Supporting material integrated, no standalone blocks | master §11 | **PASS** |
| 28 | No task duration changed, no scope cut, no silent removal | master §7.1, §38 | **PASS** |
| 29 | Conditional RecSys numericals retained and marked conditional | master §22, inventory `fixed_plan_and_scope` | **PASS** |
| 30 | Integrated closure checks, no separate verification blocks | `State/approved_constraints.json` `preparation_mode` (supersedes master §9 phase 3) | **PASS** |
| 31 | Transitions physically plausible around the lab | calendar §32 | **PASS** |
| 32 | No live calendar events created | master §37, calendar §2, AGENTS §13 | **PASS** |

Two precedence notes, both resolved by `AGENTS.md` §5 (user-approved state in `State/` outranks the Requirements files) rather than by discarding a requirement:

- The approximately-20%-per-subject attendance target in `master_requirements.md` §28 and `availability.md` §6/§11 is explicitly removed by `State/approved_constraints.json`, which names those sections as superseded. Only the Monday lab is scheduled.
- The dedicated Phase-3 verification block in `master_requirements.md` §9 is superseded by the approved Phase 2 preparation mode: checking is integrated into each host task and the seven verification tasks carry zero additional minutes. They are therefore checkpoints inside named blocks, not missing events.

No genuine conflict between two active authorities was found.

## 5. Totals reconciliation

| Check | Expected | Scheduled | Result |
|---|---:|---:|:--:|
| Total scheduled preparation | 3,565 | 3,565 | **PASS** |
| LSEG / placement (incl. mock) | 2,500 | 2,500 | **PASS** |
| Midsem (incl. conditional) | 1,065 | 1,065 | **PASS** |
| Conditional RecSys numericals | 45 | 45 | **PASS** |
| Nonzero tasks scheduled exactly once | 60 | 60 | **PASS** |
| Task durations altered | 0 | 0 | **PASS** |
| Protected rest/buffer | 1,050 | 1,050 | **PASS** |
| True unused slack | 5 | 5 | **PASS** |
| Overlapping or missing periods | 0 | 0 | **PASS** |

Without the conditional numericals the week would be 3,520 minutes, leaving 50 minutes of slack.

## 6. Risks carried into execution

These are the feasibility risks unchanged by scheduling, not new findings:

1. **The week has 5 minutes of slack.** Any overrun has to be taken from the labelled rest/buffer, which is the only real reserve. Do not silently extend a block.
2. **CV scope is still provisional** at 180 minutes (Mon 120 + Tue 60) with no confirmed lecturer material. If the real scope is larger, that is a re-estimate of CV, not a raid on another track.
3. **RecSys first-pass status is unconfirmed** — Units 1–3 hold 150 minutes each on a low-confidence estimate.
4. **DSA fluency is unmeasured** at 420 minutes; the fixed-plan rule in `master_requirements.md` §5 applies — a weak pattern must not consume another track's time.
5. **Execution prerequisites are unverified:** a usable MongoDB environment for Saturday morning and LeetCode sign-in with Java execution. Substantial setup time is not budgeted anywhere.
6. **The Wednesday mock placement is fixed by arithmetic.** The 135-minute mock+debrief does not fit the 120-minute post-dinner window, so it sits pre-dinner at 17:15–19:30 and the 20:30–22:30 slot is midsem-only.
7. **The conditional RecSys numericals block may simply not be needed.** If Wednesday's final revision has already closed the numerical gaps, 21:45–22:30 should be dropped and the week finished early. Do not replace it with other study; its redundancy is still unverified, so it stays in the plan until you decide at the block itself.
8. **The midsem exam order is still unknown.** It may change the relative emphasis of the 15–16 September midsem blocks without changing any total.
