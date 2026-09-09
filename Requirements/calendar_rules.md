# Calendar Rules — Event Formatting, Descriptions, Resources, and Creation Behavior

## 1. Purpose

This document defines how the final planner should be represented in the calendar.

The calendar should be:

- easy to scan;
- immediately actionable;
- natural rather than robotic;
- detailed enough to execute without additional interpretation;
- consistent with the user's preferred August-style planners;
- compact enough that event descriptions remain practical.

The calendar is an execution interface, not a database dump.

---

# 2. Calendar Creation Permission

Codex must **not create, modify, or delete calendar events automatically** merely because a draft or final planner exists.

Calendar creation should occur only when the user explicitly asks Codex to create the events.

Until that point, Codex should:

- prepare event data;
- validate the schedule;
- save the draft/final plan;
- save event metadata internally if useful;
- avoid touching the live calendar.

---

# 3. Every Planned Period Must Be Intentional

Inside the active planning day, all meaningful periods should be represented intentionally.

This includes:

- study blocks;
- practice blocks;
- verification blocks;
- project sessions;
- classes;
- lunch;
- dinner;
- namaz;
- rest;
- buffer;
- mock interviews;
- other intentional downtime.

Avoid unexplained gaps caused by incomplete planning.

If time is intentionally left unused, label it naturally where appropriate, for example:

- `🛑 Rest / Buffer`
- `🌙 Wind Down`
- `🚶 Transition / Break`

Do not create filler events merely to eliminate every visual gap. The event should represent a real purpose.

---

# 4. Event Title Style

Titles should be:

- short;
- clear;
- natural;
- easy to scan;
- slightly stylish;
- allowed to use emoji;
- specific enough to identify the subject and activity.

The user likes a little visual personality.

Preferred style examples:

- `⚙️ OS — Full Revision`
- `🌐 CN — Full Revision`
- `🗃️ DBMS — Full Revision`
- `☕ Java/OOP — Revision`
- `🧩 DSA — Trees + Graphs`
- `🗃️ SQL — Practice`
- `🍃 MongoDB — Practice`
- `⚡ JavaScript — Practice`
- `🧠 RecSys — Unit 2`
- `👁️ CV — Active Coverage`
- `⛓️ Blockchain — Question Set`
- `🎨 IWT — HTML/CSS`
- `📄 Velvet — Revision`
- `🎤 Velvet — Questionnaire`
- `🏢 LSEG — Role & Company`
- `🗣️ HR — Behavioural Prep`
- `📑 Resume — Review`
- `🎯 LSEG — Full Mock`
- `🍽️ Lunch`
- `🍛 Dinner`
- `🕌 Namaz`
- `🛑 Rest / Buffer`
- `🏫 CV — Class`

Codex may choose different suitable emoji, but titles should remain tasteful and readable.

---

# 5. Avoid Robotic User-Facing Labels

Do not make the visible calendar look like an internal task database.

Avoid titles such as:

- `TYPE_FINAL_VERIFY_OS`
- `TASK_013_DBMS_REVISION`
- `P0_OS_1`
- `[MANDATORY][CORE][REVISION] OS`

Internal IDs may exist in project state if useful.

The visible calendar should stay human-friendly.

Priority should normally remain in project state rather than cluttering the event title.

---

# 6. Event Descriptions Are Required for Study/Prep Slots

Every meaningful study/preparation event must contain a description.

A description should be:

- compact;
- specific;
- written in complete sentences;
- immediately actionable;
- linked to the correct source/resource;
- aligned with the slot definition in `planner_description.md`.

A good description should answer:

1. What should I do in this block?
2. What source/resource should I open?
3. What is the purpose of the block?
4. Should ChatGPT be used?
5. Is there anything intentionally excluded because it has another dedicated slot?

---

# 7. Description Length

Descriptions should be concise enough to read quickly when opening the event.

Preferred length:

- usually 2–5 short sentences;
- plus resource links;
- slightly longer only when the slot genuinely needs extra clarification.

Avoid:

- mini essays;
- repeating the entire planner philosophy;
- long topic lists when the source itself already defines coverage;
- copied notes;
- unnecessary motivational text.

The calendar description should support execution, not replace the source material.

---

# 8. Description Structure

Descriptions should be written naturally.

A fixed visible template such as:

`OBJECTIVE:`
`RESOURCE:`
`MODE:`

is **not required**.

Codex may use a consistent internal structure while writing the final description as natural prose.

Example:

> Revise the complete OS notes assigned to this block, focusing on active recall rather than passive rereading. Cover the planned sections fully and leave oral testing for the dedicated final-verification slot. Use the linked OS notes as the primary source.

This is preferred over:

> OBJECTIVE: OS  
> TASK: READ  
> RESOURCE: X  
> VERIFY: LATER

---

# 9. Resource Links

Study events should contain direct resource links whenever a useful link exists.

Examples:

- local/Notion-equivalent note reference;
- YouTube video;
- article;
- documentation;
- coding practice platform;
- problem set;
- project notes;
- resume/JD reference;
- OA question source.

Codex should attach only the resources needed for that block.

Do not dump a large list of loosely related links into every description.

---

# 10. Resource Quality

The user prefers videos, but **relevance and quality are more important than format**.

Preferred order when equally suitable:

1. targeted video;
2. strong written explanation;
3. documentation;
4. practice platform/problem set.

Codex should judge resources based on:

- relevance to the exact block;
- correctness;
- quality;
- appropriate depth;
- time efficiency.

Avoid:

- weak SEO articles;
- overly broad playlists;
- outdated material;
- long courses for a narrow task;
- duplicated resources that teach the same thing.

---

# 11. Targeted Resources Over Broad Courses

Prefer a short, focused resource that directly matches the event.

Example:

For a 60-minute Git/GitHub review, prefer:

- a concise targeted Git interview/revision resource;

rather than:

- a 9-hour beginner Git course.

Use broad playlists/courses only when the planned block genuinely requires broad learning.

---

# 12. Practice Events Need Practice Resources

For practice-heavy areas, the event description should prioritize execution.

Examples:

### SQL
Use:
- SQL problem sets;
- query practice platforms;
- targeted interview exercises.

Do not make the primary instruction:
> Watch an SQL lecture.

unless a short explanation is necessary before practice.

### MongoDB
Use:
- CRUD/query exercises;
- aggregation practice;
- schema/query reasoning where relevant.

### JavaScript
Use:
- coding/interview practice;
- execution/output questions;
- targeted active exercises.

Existing JavaScript notes are reference-only unless needed.

### DSA
Use:
- selected problems;
- pattern-based practice;
- timed solving where planned.

---

# 13. Notes as Primary Sources vs Reference Sources

Codex must respect source roles.

Some events should use notes as the primary source.

Examples:

- OS full revision;
- CN full revision;
- DBMS revision;
- EPQ coverage;
- RecSys coverage;
- project revision.

Other events may use notes only as references.

Examples:

- JavaScript practice;
- SQL practice;
- MongoDB practice.

The existence of a note file does not mean the event should revolve around reading it.

---

# 14. ChatGPT-Driven Events

If a slot requires ChatGPT for execution, the description must say so explicitly.

Examples:

### Final verification
> Use ChatGPT for oral interview-style verification of the full subject. Answer from memory and use the notes only to correct gaps afterward.

### Project questionnaire
> Use ChatGPT for a full Velvet project questionnaire. Answer aloud and allow follow-up probing on architecture, implementation, trade-offs, security, scalability, and personal contribution.

### HR practice
> Use ChatGPT for behavioural interview practice using the prepared LSEG/HR context.

### Full mock
> Use ChatGPT for a mixed LSEG mock covering core CS, DSA, OA follow-ups, projects, resume, HR, and role/company understanding.

Codex should not generate the interactive content in advance unless specifically asked.

---

# 15. Revision Event Descriptions

A full-revision event description should:

- identify the source;
- identify the planned portion if the source was split;
- emphasize full coverage;
- discourage shallow sampling;
- mention later verification if relevant.

Example:

> Revise the assigned DBMS sections completely using the linked interview notes. Use active recall and make sure each planned section is covered rather than sampling a few questions. SQL execution practice is handled separately.

---

# 16. Practice Event Descriptions

A practice event description should:

- name the skill;
- point to the selected practice resource;
- state the intended mode of work;
- avoid unnecessary theory drift.

Example:

> Practise SQL queries using the linked problem set, focusing on joins, grouping, subqueries, window functions, and query reasoning at interview speed. Use the DBMS notes only if a concept needs a quick refresh.

---

# 17. Verification Event Descriptions

A verification event should clearly indicate that it is not another revision block.

Example:

> Use ChatGPT for an oral OS interview-style verification. Answer without notes first and cover the subject broadly, including processes/threads, scheduling, synchronization, deadlocks, memory management, and paging. Check the notes only after an answer when needed.

The exact topic list should reflect the actual source and should not be invented if the source differs.

---

# 18. Project Revision Event Descriptions

Each project revision event should identify the project and its source.

Example:

> Review the Velvet project notes and refresh the architecture, feature flow, technical choices, authentication/security, challenges, and your own contribution. The dedicated questionnaire session later will test the project orally.

Revision must occur before questionnaire.

---

# 19. Project Questionnaire Event Descriptions

Each questionnaire description should explicitly use ChatGPT.

Example:

> Use ChatGPT for a Velvet interview questionnaire. Answer aloud without relying on notes unless stuck, and allow follow-up questions on architecture, implementation decisions, trade-offs, failures, security, scalability, and improvements.

Codex does not need to attach a prewritten question list.

---

# 20. LSEG OA Event Descriptions

The event should reference the exact OA materials supplied by the user.

Example:

> Re-solve the assigned LSEG OA questions independently and explain each approach in Java. Check edge cases and time/space complexity, and make sure you can discuss the solution rather than only reproduce code.

Do not count this as general DSA coverage.

---

# 21. Role & Company Event Descriptions

The event should use:

- the supplied LSEG JD;
- concise current LSEG research;
- only the business/role context relevant to interview readiness.

Example:

> Review the supplied Engineering Graduate Associate JD and the linked LSEG company resources. Be ready to explain what LSEG does, why this role fits you, and how your projects/skills align with the position.

---

# 22. HR Event Descriptions

HR descriptions should direct the user toward active answering rather than passive reading.

Example:

> Review the linked behavioural framework briefly, then use ChatGPT to practise concise answers around teamwork, conflict, failure, strengths/weaknesses, motivation, and leadership. Keep answers grounded in real experiences.

---

# 23. Resume Event Descriptions

Resume preparation must use the exact LSEG-submitted resume.

Example:

> Review every meaningful line of the submitted LSEG resume and make sure you can explain each project, technology, achievement, and claim. Use ChatGPT for follow-up questioning where useful.

Do not use a different resume version unless the user explicitly changes the source of truth.

---

# 24. Midsem Event Descriptions

Midsem events should clearly identify:

- subject;
- logical unit/source;
- whether the block is first-pass coverage, revision, numericals, or consolidation.

Examples:

- `🧠 RecSys — Unit 1`
- `⚡ EPQ — Notes Coverage`
- `👁️ CV — Active Coverage`
- `⛓️ Blockchain — Question Set`
- `🎨 IWT — HTML/CSS`

Class attendance does not replace these events.

---

# 25. RecSys Event Rules

RecSys physical files must be mapped to logical units.

For example:

- ChatGPT Unit 1 + Codex Unit 1 = one logical Unit 1 source;
- same for Units 2 and 3.

A calendar event should say:

`🧠 RecSys — Unit 1`

not:

`RecSys ChatGPT Unit 1`
followed by
`RecSys Codex Unit 1`

unless Codex's workload analysis proves the logical unit must be split across time.

If split, use natural titles such as:

- `🧠 RecSys — Unit 1 (Part 1)`
- `🧠 RecSys — Unit 1 (Part 2)`

---

# 26. CV Event Rules

Until reliable current CV material exists:

- do not invent detailed event topics from weak/old sources;
- do not attach unrelated older papers as primary coverage;
- preserve CV as a mandatory active-preparation track.

Once reliable material is added, titles/descriptions should reflect the actual content.

---

# 27. Blockchain Event Rules

Blockchain should use the lecturer-provided question set as the primary source.

The event description should cover:

- all expected theory questions;
- the included gas/ether numericals.

Do not expand the block into broad blockchain syllabus study unless later evidence shows that is necessary.

---

# 28. Class Event Formatting

Class events should be labelled naturally.

Examples:

- `🏫 CV — Class`
- `🏫 RecSys — Class`
- `🏫 EPQ — Class`
- `🏫 IWT — Lab`

Descriptions can remain minimal.

Example:

> Attendance block only. This does not count toward today's required midsem self-study.

For the mandatory Monday lab:

> Mandatory IWT lab attendance. This does not replace IWT self-study.

---

# 29. Lunch and Dinner Formatting

Use explicit events:

- `🍽️ Lunch`
- `🍛 Dinner`

No detailed description is necessary unless useful.

Times are fixed:

- Lunch: **1:00 PM–2:00 PM**
- Dinner: **7:30 PM–8:30 PM**

---

# 30. Namaz Formatting

Friday:

- **12:30 PM–3:00 PM**

Use a clear title such as:

`🕌 Namaz`

Do not schedule overlapping preparation.

---

# 31. Rest / Buffer Formatting

Use a natural title such as:

- `🛑 Rest / Buffer`
- `☕ Break`
- `🌙 Wind Down`

Choose the title that best matches the purpose.

Do not use buffer events as disguised work.

A description is optional unless Codex wants to clarify the purpose.

---

# 32. Transitions

Codex should keep the schedule physically plausible.

Do not create impossible chains such as:

- class ending at 12:00;
- intense study beginning at 12:00 at another location;
- no transition time where real movement is needed.

Short transition periods may be included inside:

- rest;
- buffer;
- meal;
- class-adjacent downtime.

Do not overengineer transitions if the locations make them unnecessary.

---

# 33. Day Start and End

Preparation must never start before:

- **9:00 AM**

Preparation must end by:

- **10:30 PM**

Do not create study blocks outside these boundaries.

A non-study personal event outside these hours is not required for this planner.

---

# 34. Final-Day Formatting

16 September should visually communicate consolidation.

Preferred event types late in the day include:

- verification;
- recap;
- resume;
- HR;
- role/company;
- light DSA/OA review;
- final mock.

The final event sequence should preserve the mandatory:

`🎯 LSEG — Full Mock`

on the night of 16 September.

Avoid a heavy new-learning block immediately beforehand.

---

# 35. Calendar Event Data Validation

Before calendar creation, Codex should validate that:

- no events overlap unintentionally;
- lunch and dinner are protected;
- Friday namaz is protected;
- mandatory Monday IWT lab is present;
- prep stays within 9:00 AM–10:30 PM;
- every day contains at least one genuine midsem self-study block;
- selected class attendance follows the attendance logic;
- project revision precedes project questionnaire;
- major verification occurs after revision/practice;
- Sep 16 full mock is present;
- resource links are attached to the correct events;
- event durations match workload estimates;
- no event was shortened only to make the schedule fit.

---

# 36. Event Edits After Finalization

Codex should not automatically revise the calendar during the week.

If the user explicitly requests a change:

- update only the affected part of the planner/calendar where possible;
- preserve unrelated approved events;
- respect all hard constraints;
- do not initiate broad replanning unless explicitly requested.

---

# 37. Calendar Readability Standard

The final calendar should feel like a high-quality personal execution plan.

A good day should be understandable at a glance.

The user should be able to see:

- what they are doing;
- when;
- why;
- what resource to open;
- where ChatGPT is needed;
- when they rest/eat/attend class.

The calendar should not require the user to reopen project-state JSON files to understand the day.

---

# 38. Final Principle

The calendar should be:

> **specific enough to execute immediately, but not so verbose or robotic that it becomes difficult to use.**

Codex should preserve the distinction between:

- detailed planning logic in project files;
- concise execution instructions in calendar events.
