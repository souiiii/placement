# Planner Description — Meaning of Each Slot Type

## 1. Purpose of This File

This document explains what each major planner slot means and how it should be executed.

It exists so that the following chain stays unambiguous:

**Codex planner → calendar event → user → ChatGPT**

The actual calendar event should remain compact and practical. This document carries the deeper meaning behind the event type.

Codex should use these definitions consistently when constructing the planner.

---

# 2. General Rules for All Study Slots

Every study slot should have:

- a clear objective;
- a realistic duration based on actual workload;
- the exact source(s) or resource(s) to use;
- a compact description written in complete sentences;
- enough detail that the user can start immediately without deciding what the slot means.

Study slots should not be overloaded with unnecessary instructions.

The calendar should tell the user **what to do now**, while this document explains **what kind of work the slot represents**.

A study slot should never be treated as complete merely because a token number of questions were attempted.

The intended standard is meaningful coverage.

---

# 3. Full Revision

## Meaning

A **Full Revision** slot is used when the user needs to revisit an existing body of notes or already-learned material comprehensively.

The goal is not selective sampling.

The goal is to cover the relevant source sufficiently so that the user can later recall and explain the subject.

## What the user should do

The user should:

- work through the assigned portion of the notes;
- actively recall concepts instead of only rereading;
- pause on weak or forgotten concepts;
- make sure the planned source portion is actually covered;
- avoid turning the session into unrelated practice unless the event explicitly says so.

## What Codex should do

Codex should:

- use the saved workload estimate, or estimate from source size, headings/structure, and minimal targeted sampling when needed;
- decide how much can realistically fit in the slot;
- split long sources across multiple blocks if needed;
- avoid assuming one file equals one revision block;
- avoid using arbitrary question counts as the definition of completion.

Codex should not deeply read a full note merely to size a revision block.

## Typical examples

- OS full revision
- CN full revision
- DBMS full revision
- Java/OOP revision
- Node/backend revision
- EPQ notes coverage
- RecSys Unit 1 coverage

---

# 4. Practice

## Meaning

A **Practice** slot is used for material that requires active execution rather than passive reading.

The objective is to convert theoretical familiarity into usable skill.

## Typical areas

- SQL
- MongoDB
- JavaScript
- DSA
- numericals
- implementation-heavy technical material

## What the user should do

The user should:

- actively solve, write, implement, or calculate;
- avoid spending most of the slot watching explanations unless needed;
- use the assigned practice resource;
- check reasoning and implementation rather than only final answers.

## What Codex should do

Codex should:

- attach an actual practice resource whenever possible;
- prefer targeted problem sets/platforms over generic theory videos;
- use existing notes only as reference when the area is meant to be practice-first;
- estimate enough time for meaningful execution.

## Special rule

A practice slot must not become:

> “watch another lecture about the topic”

unless the planner intentionally includes a short learning component because it is necessary.

---

# 5. Final Verification

## Meaning

A **Final Verification** slot is the closure stage for a major subject.

It happens **after revision and relevant practice are substantially complete**.

The objective is to verify that the material is actually available from memory and can be explained in interview conditions.

## Execution

The user should use **ChatGPT for oral/interview-style verification**.

ChatGPT should test broad coverage rather than a narrow subset.

The user should answer without constantly referring to notes.

If needed, notes can be checked after an answer to correct gaps.

## Codex's responsibility

Codex should:

- schedule this only after the subject's main revision/practice work;
- identify the relevant subject in the calendar description;
- tell the user to use ChatGPT for verification;
- not pre-generate a large question bank itself.

## Examples

- OS — Final Verification
- DBMS — Final Verification
- CN — Final Verification
- Java/OOP — Final Verification

---

# 6. DSA Coverage

## Meaning

A **DSA Coverage** slot is part of the fixed breadth-oriented DSA plan.

Its purpose is to improve interview problem-solving readiness across the week.

It is not merely a “solve five random questions” block.

## What the user should do

Depending on the block, the user may:

- solve representative problems;
- identify the underlying pattern;
- explain the approach;
- implement the solution;
- analyze time/space complexity;
- solve under time pressure;
- revisit previously covered patterns when planned.

## What Codex should do

Codex should:

- create a fixed weekly DSA structure;
- cover major interview patterns;
- choose representative problems/resources;
- preserve breadth;
- avoid allowing one weak topic to consume excessive extra time;
- not automatically replan the week based on performance.

DSA Pattern Index and DSA mistake log may inform planning but should not automatically become separate slots.

---

# 7. LSEG OA Preparation

## Meaning

An **LSEG OA Preparation** slot focuses specifically on the 4 major and 3 minor questions from the user's LSEG online assessment.

This is separate from normal DSA preparation.

Use `Sources/LSEG/OA/` as the source of truth for the OA questions and their major/minor classification.

## Objective

The user should become capable of:

- solving the OA questions independently;
- explaining the approach;
- discussing complexity;
- handling edge cases;
- implementing/explaining them in Java.

## Codex's responsibility

Codex should:

- inspect the exact OA material supplied by the user;
- estimate time based on actual difficulty;
- schedule one or more blocks as required;
- keep this track separate from general DSA.

---

# 8. Project Revision

## Meaning

A **Project Revision** slot is a focused review of one interview project.

The three projects are:

- Velvet
- Eventually
- Relay

Each project must receive its own revision session before its questionnaire session.

## What the user should do

The user should revisit:

- project purpose;
- architecture;
- major features;
- implementation;
- technology choices;
- important data flows;
- authentication/security;
- personal contribution;
- known challenges;
- design trade-offs.

The project notes are the main reference.

## Codex's responsibility

Codex should:

- attach the relevant project source;
- schedule revision before questionnaire;
- give each of the three projects its own revision session.

---

# 9. Project Questionnaire

## Meaning

A **Project Questionnaire** slot is an interview-style oral session for one project.

It occurs after that project's revision session.

## Execution

The user should use **ChatGPT**.

ChatGPT will ask follow-up questions about areas such as:

- architecture;
- implementation;
- why particular technologies were chosen;
- trade-offs;
- bugs/challenges;
- authentication;
- security;
- scalability;
- data flow;
- personal contribution;
- alternative designs;
- improvements.

## Codex's responsibility

Codex should:

- schedule the slot;
- identify the project;
- direct the user to use ChatGPT;
- not generate the questionnaire in advance.

Required questionnaire sessions:

- Velvet
- Eventually
- Relay

---

# 10. Resume Review

## Meaning

A **Resume Review** slot prepares the user to defend and discuss the exact resume submitted to LSEG.

The submitted LSEG resume is the source of truth.

## What the user should do

The user should:

- review every meaningful line;
- refresh projects, technologies, achievements, and claims;
- make sure they can explain anything that may be questioned;
- identify likely follow-up questions.

## Interactive execution

Use ChatGPT where oral questioning is useful.

## Codex's responsibility

Codex should:

- use the submitted resume as the primary source;
- schedule appropriate review time;
- not invent facts or answers.

---

# 11. LSEG Role & Company Preparation

## Meaning

A **Role & Company** slot prepares the user specifically for LSEG and the Engineering Graduate Associate position.

This is not generic HR preparation.

## Primary inputs

- exact job description supplied by the user;
- current high-quality LSEG research;
- relevant company/business information.

## Objective

The user should be ready to discuss:

- what LSEG does;
- relevant business areas;
- why LSEG;
- why this role;
- how the role fits the user's background;
- what the position appears to require.

## Codex's responsibility

Codex should:

- research current high-quality sources;
- attach concise, relevant resources;
- avoid broad unrelated company research;
- use the supplied JD as the primary role-specific source.

---

# 12. HR / Behavioural Preparation

## Meaning

An **HR / Behavioural** slot prepares the user for non-technical interview questions.

It is separate from LSEG role/company research.

## Topics may include

- behavioural questions;
- STAR-style responses;
- teamwork;
- conflict;
- leadership;
- failure;
- strengths and weaknesses;
- motivation;
- communication;
- difficult situations;
- career goals.

## Execution

Interactive practice should use ChatGPT.

Codex should find suitable concise HR resources where useful but should not spend time generating a giant behavioural question bank.

---

# 13. Aptitude

## Meaning

An **Aptitude** slot covers aptitude-style preparation that may be relevant to LSEG.

Aptitude is required coverage, but it does not automatically require a standalone block.

## Codex's decision

Codex may:

- create a dedicated aptitude block; or
- integrate aptitude into broader LSEG/HR preparation.

The choice should depend on:

- expected relevance;
- available time;
- total workload;
- opportunity cost.

Aptitude should not disappear silently.

---

# 14. Midsem Coverage

## Meaning

A **Midsem Coverage** slot is genuine self-study for one of the five midsem subjects:

- EPQ
- Recommendation Systems
- Computer Vision
- Blockchain
- IWT

At least one such self-study block must exist every day from 10–16 September.

Class attendance does not count.

## Purpose

These slots keep midsem preparation strong while LSEG receives the majority of total preparation time.

---

# 15. EPQ Coverage

## Meaning

An EPQ study slot may use:

- full notes;
- revision notes;
- both, depending on phase.

## Planner logic

The full notes may require more than one block.

Revision notes are better suited to later consolidation and recall.

Codex should use source size, headings/structure, and saved estimates to judge workload. Investigate overlap only if deciding redundancy materially affects the planner; do not deeply compare the notes by default.

---

# 16. Recommendation Systems Coverage

## Logical source structure

Recommendation Systems must be treated as logical study units.

### Unit 1

- ChatGPT Unit 1
- Codex Unit 1

These are used side by side and count as **one logical Unit 1 source**.

### Unit 2

- ChatGPT Unit 2
- Codex Unit 2

Together form **one logical Unit 2 source**.

### Unit 3

- ChatGPT Unit 3
- Codex Unit 3

Together form **one logical Unit 3 source**.

### Final Revision

`FINAL_REVISION` is the RecSys final-revision source.

### Numericals

Numericals are optional as a separate block if they are already adequately covered by final revision material.

## Planner logic

Do not infer calendar block count from physical file count.

A long logical unit may require multiple blocks.

---

# 17. Computer Vision Coverage

## Meaning

Computer Vision is a mandatory active-learning midsem track.

## Current special condition

Reliable final source material may arrive later.

Codex must not invent detailed coverage based on unrelated old papers.

## When current material arrives

Codex should:

- inspect its scope/structure using page count, headings, and targeted sections only as needed;
- identify logical sections;
- estimate realistic study time;
- split the work across days if needed;
- preserve active CV preparation as mandatory.

---

# 18. Blockchain Coverage

## Meaning

Blockchain is a narrow, exam-targeted preparation track based on the lecturer's exact expected questions.

It should normally require around one dedicated block unless source inspection shows otherwise.

The block should cover:

- the provided theory questions;
- the provided gas/ether numericals.

Later recall may be integrated into broader midsem review.

---

# 19. IWT Coverage

## Meaning

IWT preparation is primarily HTML/CSS.

Approximately one dedicated coverage block is expected unless later source material shows a larger scope.

---

# 20. Consolidation

## Meaning

A **Consolidation** slot revisits already-covered material shortly before the interview/exams.

It is not intended for major new learning.

Typical uses:

- final revision notes;
- high-level recall;
- important formulas;
- interview-critical concepts;
- OA recap;
- project refresh;
- quick technical refresh.

Codex should increasingly favour consolidation as 16 September approaches.

---

# 21. Mixed Mock Interview

## Meaning

A **Mixed Mock Interview** is a broad simulation using ChatGPT.

The mandatory final mock occurs on the **night of 16 September**.

## Possible coverage

- core CS;
- DSA/problem solving;
- LSEG OA follow-ups;
- projects;
- resume;
- HR/behavioural;
- role/company understanding.

## Execution

Use ChatGPT.

Codex should only schedule and describe the session.

It should not pre-generate the full mock.

## Final-day rule

Heavy new learning should not be scheduled immediately before this mock.

The user should arrive mentally fresh enough to perform meaningfully.

---

# 22. Optional Earlier Checkpoint / Mock

An earlier mock or checkpoint is **optional**.

Codex may schedule one only if:

- the important coverage already fits;
- it provides meaningful value;
- it does not displace higher-priority preparation.

The mandatory Sep 16 night mock must never be sacrificed for an earlier one.

---

# 23. Rest / Buffer

## Meaning

A **Rest / Buffer** slot is deliberate recovery time.

It is not hidden study time.

Its purpose may include:

- mental recovery;
- transition between heavy subjects;
- preventing fatigue;
- absorbing minor real-world delays;
- maintaining performance across the long preparation day.

## Codex's responsibility

Codex should place these realistically based on surrounding workload.

The planner should not fill every available minute with intensive study.

These blocks must be clearly labelled.

---

# 24. Lunch

## Meaning

Lunch is a protected daily block.

Time:

- **1:00 PM–2:00 PM**

Do not schedule study inside it.

It must appear explicitly in the planner.

---

# 25. Dinner

## Meaning

Dinner is a protected daily block.

Time:

- **7:30 PM–8:30 PM**

Do not schedule study inside it.

It must appear explicitly in the planner.

---

# 26. Class

## Meaning

A **Class** slot exists only to satisfy attendance requirements.

It does **not** count as meaningful study/preparation time.

## Rule

Even if the user attends:

- CV;
- RecSys;
- EPQ;
- IWT;

the planner must still schedule genuine self-study separately.

Codex should choose optional classes based on minimal disruption to the preparation plan.

---

# 27. Namaz

## Meaning

On Friday, 11 September:

- **12:30 PM–3:00 PM**

is fully protected for namaz.

This period is unavailable for study or other planner work.

The calendar should label it explicitly.

---

# 28. Intentional Downtime

If Codex intentionally leaves a period unallocated to study, it should still represent the purpose clearly when appropriate.

Examples:

- rest;
- buffer;
- transition;
- personal time.

The planner should avoid unexplained gaps inside the active day.

---

# 29. Resource Research

## Meaning

Codex may research external resources to support a future study slot.

This is planner work, not user study time.

## Resource preference

Prefer:

1. short, targeted videos;
2. high-quality written resources when better;
3. documentation/problem platforms where appropriate.

Selection should optimize:

- relevance;
- correctness;
- quality;
- appropriate depth;
- time efficiency.

Do not choose an entire course when a targeted resource is sufficient.

---

# 30. Resource Use in Calendar Descriptions

Each study event should include the specific resources needed for that slot.

Descriptions should be concise.

A good description should answer:

- What am I doing?
- What source do I open?
- What is the purpose?
- Do I need ChatGPT for this?

It should not become a long lesson plan.

---

# 31. Sequence Rules

Codex should preserve the following important sequences:

### Core subject

**Revision → Practice if needed → Final Verification**

### Project

**Revision → Questionnaire**

### LSEG OA

**Question review/understanding → independent solving/explanation → later recap if planned**

### End of week

**Coverage → consolidation → final mixed mock**

Codex should not invert these sequences without a clear reason.

---

# 32. Block Duration

There is no universal default study-block length.

The content decides the duration.

Codex should:

- use saved workload estimates or lightweight source/workload inspection;
- estimate realistic time;
- split large tasks;
- combine small compatible tasks when sensible;
- preserve rest and transitions.

Avoid arbitrary rules such as:

- every block is 60 minutes;
- every PDF gets 90 minutes;
- every subject gets exactly one session.

---

# 33. Completion Standard

A block is considered properly designed when its planned objective can realistically be completed inside the assigned time.

Do not define completion using shallow metrics such as:

- “solve 5 questions” for an entire topic;
- “read one PDF” regardless of size;
- “watch one video” regardless of whether the subject is understood.

The intended standard is:

> **meaningful coverage appropriate to the slot's purpose.**

---

# 34. Relationship Between This File and Calendar Events

The calendar should remain natural and readable.

For example:

- `⚙️ OS — Full Revision`
- `🎤 Velvet — Questionnaire`
- `🗃️ SQL — Practice`
- `🎯 LSEG — Full Mock`

The event description gives the **specific instructions and links**.

This file defines the **deeper meaning of the slot type**.

Codex may use internal machine-readable slot IDs in project state if useful, but the user-facing calendar should not look excessively robotic.