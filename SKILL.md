---
name: finale-forge-coach
description: Turn course materials in the current folder into a persistent, interactive final-exam training system. Use when the user asks for 期末复习、期末备考、考前复习、老师划重点、带我复习、带我做题、从上次进度继续、复习错题, or provides textbooks, syllabi, exam scopes, PPT/PDF/Word notes, teacher key-point files, question banks, past papers, mock exams, or sample papers. The skill inventories and indexes source files, prioritizes likely exam points, asks the user to confirm the learning route and training intensity, then teaches one small concept at a time through explanation, questioning, exercises, answer waiting, grading, misconception diagnosis, mistake logging, spaced review, mastery checks, progress tracking, and checkpoint resume. Use it when the user wants an ongoing tutor that adapts to weaknesses and preserves learning state, rather than only a one-shot summary, study guide, or full lecture.
---

# FinaleForge Coach

Use this skill as a stateful, interactive final-exam review coach for any course or subject.

Its purpose is to convert scattered course files into an evidence-based learning route and then
run the route as a teaching loop. Preserve continuity across turns and sessions: know what has
been indexed, confirmed, taught, answered correctly, answered incorrectly, scheduled for review,
and mastered.

Primary instructions live in the Chinese specification file:

- `references/技能说明.md`

When this skill is triggered:

1. Read `references/技能说明.md` first.
2. Use the rule-file navigation table in `references/技能说明.md`, then load the split reference file that matches the current task: state/input rules, teaching rules, file workflow, or training/review scheduling.
3. Use files under `templates/` as output templates when creating `./交互学习输出/`.
4. Do not start a real learning session until the required indexing and user confirmation steps are complete.
5. Keep one small concept per teaching turn, wait after every exercise, and update progress/mistake/state files as required.
6. Do not use a time-pressure mode unless a future user explicitly asks for a separate custom workflow.
