# Master Requirements — LSEG + Midsem Planner

## 1. Purpose

This project exists to help Codex build a realistic, high-quality preparation planner for **10 September 2026 through 16 September 2026 inclusive**.

Important dates:

- **17 September 2026:** LSEG interview.
- **18 September 2026:** midsemester examinations begin.
- All major LSEG preparation should be substantially complete by the night of **16 September**.
- Midsem preparation must remain strong throughout the same period so that exam preparation is not left until after the interview.

The planner must optimize for **maximum LSEG readiness without allowing midsem preparation to collapse**.

---

## 2. Overall priority

The planner must follow this priority model:

1. **LSEG preparation receives the largest share of available preparation time.**
2. **Midsem preparation remains strong throughout the week.**
3. **Active Computer Vision preparation is mandatory.**
4. Required coverage must be realistic and meaningful, not merely represented by token calendar entries.
5. Redundant material should be cut before primary coverage is sacrificed.

The planner must not optimize for visual completeness at the cost of unrealistic block durations.

---

## 3. Division of responsibilities

### 3.1 Codex is the planner/orchestrator

Codex is responsible for:

- inspecting source material;
- estimating realistic workload;
- identifying logical study units;
- researching suitable external resources when required;
- deciding how work should be distributed across 10–16 September;
- performing feasibility analysis;
- maintaining persistent planning state inside this project;
- producing the draft and final planner;
- preparing calendar-event data;
- creating calendar events **only when explicitly instructed by the user**.

Codex is **not** the primary tutor or interview partner during execution.

Codex should not spend planning time generating large banks of mock questions, project interview questions, core-CS oral questions, or behavioural interview scripts unless specifically asked.

### 3.2 ChatGPT is the execution/preparation guide

During the actual week, the user will use ChatGPT for interactive preparation, including:

- core-subject oral/interview-style verification;
- project questionnaires;
- resume questioning;
- HR/behavioural practice;
- LSEG role/company questioning;
- mixed mock interviews;
- DSA discussion and explanation;
- clarification of difficult topics;
- plan adjustments if the user chooses to make changes.

Calendar descriptions must therefore be clear enough that the user can show a slot to ChatGPT and ChatGPT can understand what the slot is meant to accomplish.

---

## 4. Planning style

The planner should resemble the user's successful August-style planners in spirit:

- exact time blocks;
- clear deliverables;
- active practice where appropriate;
- explicit meals, classes, rest, buffer, namaz, and study periods;
- meaningful descriptions;
- direct resource links;
- minimal decision-making required when a block begins.

However, the new planner must correct the main weakness of the old planners:

> A small number of questions must never be treated as equivalent to full subject understanding or full topic coverage.

The plan must prioritize **complete coverage across days**, followed by revision, practice, and final verification where appropriate.

---

## 5. Fixed-plan philosophy

The planner should be designed as a **fixed plan for the week**, not an automatically adaptive system.

Codex must not automatically extend weak topics, steal time from later topics, or continuously reschedule the remaining week based on performance.

Examples:

- Struggling with one DSA pattern must not cause multiple additional hours to be taken from other planned areas.
- Missing a block must not automatically trigger a full replanning cycle.
- Poor performance in a verification block must not automatically expand that subject's allocation.

If changes are needed during the week, the user will decide them manually with ChatGPT and then explicitly ask Codex to update the plan if necessary.

---

## 6. Persistent planning state

Codex must persist its planning work inside this project.

It should save:

- source classifications;
- logical source groupings;
- workload estimates;
- resource research;
- feasibility calculations;
- planning decisions;
- user-approved cuts or trade-offs;
- draft scheduling logic;
- final approved plan state.

When later asked to create or finalize the planner, Codex must **read the saved project state first** and reuse prior analysis instead of redoing research and estimation from scratch.

Approved decisions must not be silently overwritten.

---

## 7. Feasibility is mandatory

Before finalizing the planner, Codex must perform a feasibility check.

The feasibility analysis must account for:

- realistic available study hours;
- source length;
- source density and difficulty;
- revision time;
- practice time;
- LSEG-specific preparation;
- DSA;
- OA preparation;
- projects;
- resume review;
- HR/behavioural preparation;
- role/company preparation;
- aptitude;
- midsem coverage;
- classes that will actually be attended;
- meals;
- namaz;
- rest;
- buffer;
- the mandatory final mock;
- realistic cognitive load.

### 7.1 If the plan is unrealistic

If the requested workload does not fit realistically:

1. **Stop before finalizing the schedule.**
2. Explain the estimated required workload versus realistic available time.
3. Identify the major sources of overload.
4. Separate material into:
   - required;
   - desirable;
   - redundant/optional.
5. Propose specific cuts, compressions, or trade-offs.
6. **Wait for user approval before removing anything.**

Codex must never silently remove a task or source.

Codex must never make a task unrealistically short merely to force it into the calendar.

---

## 8. Source count does not equal block count

This is a hard rule.

> **One document does not equal one study block.**

Codex must estimate block duration from the actual content.

Examples:

- One large document may require multiple blocks across multiple days.
- Two short documents may fit into one block.
- A logical study unit may consist of multiple physical files.
- A supporting file may receive no dedicated block at all.

The **content, density, purpose, and plausible completion time** determine scheduling.

Codex should automatically split large logical units across multiple blocks/days when necessary.

---

## 9. Core-subject learning model

For major core subjects, the intended preparation flow is:

### Phase 1 — Full revision

The user wants complete coverage of the relevant notes.

The plan should not sample a few questions and declare the subject finished.

### Phase 2 — Practice where required

Practice-heavy areas must receive practical work rather than passive revision.

Examples include:

- SQL;
- MongoDB;
- numericals;
- coding/implementation-heavy material.

### Phase 3 — Final verification

After a major subject's revision/practice is complete, a dedicated closure/verification block should confirm that the material is actually retained.

For these blocks:

> **Use ChatGPT for oral/interview-style verification.**

Codex schedules the slot and explains its purpose. ChatGPT conducts the actual verification.

---

## 10. Dedicated placement/technical tracks

The following areas are eligible for and should normally receive **dedicated scheduled preparation blocks**:

### Core / interview fundamentals

- Operating Systems
- Computer Networks
- DBMS
- Java / OOP
- Node.js / Backend
- System Design

### Practice-heavy areas

- JavaScript practice
- SQL practice
- MongoDB practice

### Additional technical areas

- React
- Next.js
- TypeScript
- Git / GitHub
- Python
- AI fundamentals

"Dedicated" does **not** mean "exactly one block."

Codex must inspect the source/workload and choose realistic duration and splitting.

---

## 11. Reference-only and integrated material

Not every source deserves its own calendar event.

The following types of material should normally be integrated into larger relevant blocks:

- JSON;
- Java Collections Framework;
- Extra Fundamental Topics;
- Redis where relevant;
- DSA Pattern Index;
- DSA mistake log;
- similar small supporting references.

Examples:

- Java Collections can be used inside Java/OOP or DSA implementation work.
- JSON can be used inside Node/backend preparation.
- Redis can be integrated into backend/system-design preparation where relevant.
- Extra fundamentals can be used during broader core/interview consolidation.
- DSA Pattern Index can help Codex design DSA coverage.
- DSA mistake log can inform question selection/review.

A source existing in `Sources/` must **not** be interpreted as evidence that it deserves dedicated calendar time.

---

## 12. JavaScript-specific rule

JavaScript deserves dedicated preparation time.

However:

- the user's existing JavaScript notes are **reference material**;
- they should not be the primary preparation method;
- Codex should later identify a better external practice/preparation resource;
- the event should focus on active preparation/practice rather than simply reading the notes.

The same principle may be used for other practice-heavy topics when a high-quality external practice source is more useful than passive note reading.

---

## 13. DSA requirements

DSA is a major independent track.

The goal is:

> Maximize the user's ability to solve a reasonable coding question presented during the interview.

The plan must **not** be based only on "solve N questions per day."

The DSA plan should be fixed in advance and breadth-oriented because there is not enough time for unlimited weakness remediation.

Codex should design DSA coverage around:

- major interview patterns;
- representative problems;
- implementation ability;
- pattern recognition;
- timed solving;
- explaining the approach;
- complexity analysis;
- planned re-exposure/revision where useful.

It may use a mixture of easy, medium, and carefully chosen harder problems.

If the user struggles with a pattern, that should not automatically consume additional hours that were allocated to other required preparation.

DSA supporting pages such as the pattern index and mistake log are references for planning, not automatically standalone study sessions.

---

## 14. LSEG OA preparation

The LSEG OA track is **separate from general DSA**.

The user will provide:

- **4 major OA questions**
- **3 minor OA questions**

Codex must inspect the actual questions and allocate appropriate preparation time.

The goal is for the user to be able to:

- solve the questions independently;
- explain the intended approach;
- discuss time and space complexity;
- handle edge cases;
- implement/explain the solutions in **Java**.

The user's normal interview language is Java, even though JavaScript was used during the OA.

Codex should not count these OA questions as a substitute for general DSA coverage.

---

## 15. Project preparation

There are three interview projects:

- Velvet
- Eventually
- Relay

Each project requires **two separate sessions**.

### Required order for each project

1. Project revision
2. Project questionnaire

This produces **six project sessions total**.

The revision session must occur before the questionnaire session.

### Project revision

Use the relevant project notes/source material.

### Project questionnaire

The event should direct the user to **use ChatGPT**.

Codex does not need to pre-generate the questions.

The questionnaire is expected to cover areas such as:

- architecture;
- design choices;
- implementation;
- trade-offs;
- failures/challenges;
- authentication;
- security;
- data flow;
- scalability;
- personal contribution;
- alternatives;
- improvements.

---

## 16. Resume preparation

The user will provide the **exact resume submitted to LSEG**.

That submitted version is the source of truth.

Codex should schedule appropriate resume-review/preparation sessions.

Interactive resume questioning will be done using ChatGPT.

Codex should not invent answers or scripts on the user's behalf.

---

## 17. LSEG company/role preparation

LSEG role/company preparation is a **separate track from generic HR preparation**.

The user will provide the exact job description.

The JD should be treated as the primary role-specific source.

Codex should also research current, high-quality information about LSEG where useful, including:

- what the company does;
- relevant business areas;
- the role;
- likely expectations;
- why the role may fit the user's background.

This track should support questions such as:

- Why LSEG?
- Why this role?
- What does LSEG do?
- How does your experience align with the position?

---

## 18. HR / behavioural preparation

HR/behavioural preparation must have its own resource set and should not be merged blindly with company/role research.

It should cover preparation for areas such as:

- behavioural questions;
- STAR-style responses;
- teamwork;
- conflict;
- leadership;
- failure;
- strengths/weaknesses;
- motivation;
- communication;
- similar interview questions.

Actual interactive practice will be done with ChatGPT.

---

## 19. Aptitude

Aptitude is required coverage because it may be relevant to the LSEG interview process.

However, Codex may decide whether:

- aptitude deserves a dedicated practice block; or
- it is better integrated into broader LSEG/HR preparation.

The decision should be based on likely value and total workload.

Aptitude should not disappear from the plan without being consciously accounted for.

---

## 20. Midsem requirements

There are five active midsem tracks:

1. EPQ
2. Recommendation Systems
3. Computer Vision
4. Blockchain
5. IWT (HTML/CSS)

A **genuine self-study midsem block must exist every day from 10–16 September**.

College classes do **not** count toward this daily midsem-study requirement.

---

## 21. EPQ

EPQ currently has two important logical source groups:

1. full notes;
2. revision notes.

These two sources do not imply exactly two blocks.

Codex should inspect:

- source length;
- density;
- overlap;
- required coverage;
- likely revision time.

The full notes may require multiple coverage blocks.

The revision notes can be used later for consolidation, recall, and final review.

---

## 22. Recommendation Systems

Recommendation Systems contains multiple physical files, but Codex must treat them as logical study units.

### Unit 1

The ChatGPT version and Codex version are used **side by side** and together form **one logical Unit 1 source**.

### Unit 2

The ChatGPT version and Codex version are used **side by side** and together form **one logical Unit 2 source**.

### Unit 3

The ChatGPT version and Codex version are used **side by side** and together form **one logical Unit 3 source**.

### Final revision

`FINAL_REVISION` is the RecSys final revision source and forms another logical study unit.

### Numericals

A separate numericals source may exist.

It is **redundancy-sensitive**.

If the important numerical material is adequately covered in the final revision material, Codex should recommend omitting a separate numericals block rather than wasting scarce time.

Therefore the likely effective required RecSys coverage is:

1. Unit 1
2. Unit 2
3. Unit 3
4. Final revision

with numericals receiving separate time only if justified.

Again, **logical unit count does not determine block count**.

---

## 23. Computer Vision

Computer Vision is a **mandatory active-preparation track**.

Current reliable source material is incomplete.

The lecturer's PPTs/notes are expected to be the most useful current source, but they may arrive later.

Codex must not invent the active scope from unrelated older papers or weak evidence.

Until reliable material is available:

- preserve CV as a mandatory track;
- do not hallucinate a detailed source structure;
- be ready to incorporate new CV material when added.

Once proper material arrives:

1. inspect the actual content;
2. identify logical sections;
3. estimate workload;
4. fit it realistically into the remaining days;
5. split across multiple days if necessary.

Active CV preparation cannot simply be dropped because the material arrived late.

---

## 24. Blockchain

Blockchain should normally receive approximately **one dedicated study block**, unless source inspection shows that more time is genuinely required.

The lecturer has supplied a narrow list of exact expected questions, including two gas/ether numericals.

This is therefore a constrained exam-preparation task rather than broad syllabus exploration.

Later recall may be integrated into general midsem revision rather than automatically receiving another full block.

---

## 25. IWT

IWT preparation is primarily HTML/CSS.

Approximately **one dedicated study block** is expected to be sufficient unless later material shows that the scope is larger.

---

## 26. Daily midsem rule

This is a hard constraint:

> **At least one genuine midsem self-study block must be scheduled every day from 10 September through 16 September.**

A college class does **not** count.

The purpose is to make sure all midsem material receives meaningful coverage before the LSEG interview.

---

## 27. Planning window and daily boundaries

The planner covers:

- **10 September 2026**
- **11 September 2026**
- **12 September 2026**
- **13 September 2026**
- **14 September 2026**
- **15 September 2026**
- **16 September 2026**

Daily preparation rules:

- Prep must **not start before 9:00 AM**.
- Prep must **end by 10:30 PM**.
- **Lunch: 1:00 PM–2:00 PM**.
- **Dinner: 7:30 PM–8:30 PM**.
- Realistic rest/buffer periods must exist.
- The schedule must not attempt to fill every available minute with heavy study.

The detailed timetable belongs in the availability file, but these boundaries are hard requirements.

---

## 28. Class attendance

Class attendance exists only as an attendance constraint and must not be counted as preparation time.

The actually relevant subjects for attendance during this period are:

- IWT
- Computer Vision
- Recommendation Systems
- EPQ

The following classes do **not** happen and should be ignored:

- Blockchain
- EMC
- TW

The preferred target is approximately **20% attendance for each active subject**, measured in whole classes where practical.

Codex should choose which optional classes to attend based on which combination causes the **least disruption to the preparation plan**.

### Mandatory class

The **Monday IWT lab is mandatory**.

### Friday namaz

On Friday, **12:30 PM–3:00 PM must remain completely free** for namaz.

No study should be scheduled during that period.

The detailed class timetable should be maintained in the separate availability file.

---

## 29. Resource-selection policy

Codex should attach high-quality resources to study-block descriptions where appropriate.

### Format preference

The user prefers:

1. **videos first**;
2. articles/written resources are also acceptable;
3. documentation/problem platforms are acceptable when better suited to the task.

### Selection criteria

Resource quality must be judged by:

1. relevance to the exact block;
2. technical correctness;
3. quality;
4. appropriate depth;
5. time efficiency.

Codex should prefer **short, targeted resources** over large courses/playlists unless broad coverage is genuinely needed.

Do not attach a long playlist merely because it exists.

For practice blocks, prefer actual practice resources.

Examples:

- SQL practice → SQL problem set/platform;
- MongoDB practice → query/aggregation exercises;
- JavaScript practice → active coding/interview practice;
- theory revision → targeted video/article when it improves understanding.

Existing notes may still be attached as references.

---

## 30. Calendar execution style

Every planned period inside the active day should be intentionally represented.

This includes:

- study;
- class;
- lunch;
- dinner;
- rest;
- buffer;
- namaz;
- questionnaire;
- mock;
- intentional downtime.

There should not be unexplained calendar holes simply because the planner forgot to label them.

### Titles

Titles should be:

- short;
- clear;
- readable;
- slightly stylish;
- allowed to use suitable emoji.

Examples of the intended feel:

- `⚙️ OS — Full Revision`
- `🗃️ SQL — Practice`
- `🧠 RecSys — Unit 2`
- `🧩 DSA — Trees + Graphs`
- `📄 Velvet — Revision`
- `🎤 Velvet — Questionnaire`
- `🏢 LSEG — Role & Company`
- `🗣️ HR — Behavioural Prep`
- `🎯 LSEG — Full Mock`
- `🍽️ Lunch`
- `🕌 Namaz`
- `🛑 Rest / Buffer`

Avoid excessive robotic naming.

---

## 31. Study-block descriptions

Every study/preparation event must have a **compact but meaningful description written in complete sentences**.

The description should make clear:

- what the user should do;
- what source/resource should be used;
- the purpose of the session;
- relevant direct links;
- whether ChatGPT should be used.

Descriptions should be useful when the event opens, but should not become long lesson plans.

---

## 32. Planner description document

The project will contain a separate `planner_description.md`.

That document should explain what major slot types mean, such as:

- Full Revision
- Practice
- Final Verification
- Project Revision
- Project Questionnaire
- Resume Review
- HR Prep
- Role/Company Prep
- Mock Interview
- Midsem Coverage
- Rest/Buffer

This document acts as the semantic bridge between:

**Codex planner → calendar slot → user → ChatGPT**

Visible robotic tags such as `TYPE=FINAL_VERIFY` are not required unless Codex needs internal machine-readable IDs in project state.

---

## 33. End-of-week taper

Codex should decide the exact day-by-day balance, but the overall direction should be:

### Earlier/middle days

More emphasis on:

- new coverage;
- full revision;
- technical learning;
- practice.

### Later days

Increasing emphasis on:

- consolidation;
- final verification;
- recall;
- LSEG OA review;
- project questionnaires;
- resume;
- HR/behavioural work;
- LSEG role/company readiness;
- DSA interview readiness.

Heavy new learning should be avoided late on 16 September unless it is genuinely mandatory and could not have been completed earlier.

---

## 34. Mandatory final mock

The night of **16 September** must contain a **full mixed LSEG mock interview with ChatGPT**.

This is mandatory.

The mock should be positioned after most major preparation is complete.

It should be able to mix:

- core CS;
- DSA/problem solving;
- LSEG OA follow-ups;
- projects;
- resume;
- HR/behavioural;
- LSEG role/company understanding.

Codex should avoid scheduling heavy new learning immediately before this block.

An earlier checkpoint/mock is optional and should be added only if Codex judges it useful and feasible after higher-priority coverage is protected.

---

## 35. Local source snapshots

The preferred workflow is to place local Markdown/PDF snapshots of relevant material inside this project rather than making Codex depend on live Notion access.

This allows Codex to:

- inspect exact content;
- measure length;
- inspect headings;
- judge density;
- estimate workload consistently;
- reuse analysis reproducibly.

The source map must distinguish **physical files** from **logical study units**.

Example:

- `unit1_chatgpt.md`
- `unit1_codex.md`

together form one logical RecSys Unit 1 source.

A physical file's presence must never automatically create a calendar block.

---

## 36. Important inputs that will be added later

The project may initially be incomplete.

The user will add/provide:

- exact LSEG job description;
- exact resume submitted to LSEG;
- 4 major LSEG OA questions;
- 3 minor LSEG OA questions;
- current Computer Vision PPTs/notes/material when available;
- official midsem timetable when released.

The midsem **start date of 18 September is confirmed**, even though the exact subject order is not yet available.

Codex should incorporate new inputs when added without discarding previously approved planning decisions unless the new information genuinely requires a change.

---

## 37. Calendar creation permission

Codex must **not create or modify calendar events merely because a draft/final plan exists**.

Calendar creation happens only when the user explicitly asks Codex to do so.

Until that explicit instruction, Codex should only maintain planning files and outputs inside this project.

---

## 38. Core planning philosophy

The central rule is:

> **Optimize for complete meaningful coverage, not checkbox completion.**

Do not use these flawed assumptions:

- "5 questions completed = topic mastered."
- "1 PDF = 1 study block."
- "Every note deserves a dedicated event."
- "Everything must fit even if durations become unrealistic."

Instead:

1. inspect the actual workload;
2. identify logical study units;
3. classify sources correctly;
4. estimate realistic durations;
5. revise major material fully;
6. practise areas that require practice;
7. verify retention;
8. preserve breadth;
9. remove redundancy before important coverage;
10. consolidate before the interview.

The planner must be ambitious, but it must remain executable.
