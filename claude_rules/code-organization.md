# Code Organization Rules

## Purpose

These rules apply whenever AI is deciding whether to:

- create a new file;
- split an existing file;
- move code between files;
- reorganize folders;
- extract modules.

Always prefer the simplest organization that keeps related code together.

---

## Rule 1 — Prefer modifying existing files

Always extend the current file before creating a new one.

Do not create new files unless there is a clear architectural reason.

---

## Rule 2 — Every new file must have a purpose

Every new file should solve a real problem.

A new file should improve at least one of:

- Separation of responsibility
- Reusability
- Maintainability
- Testability

Otherwise, keep the code in the existing file.

---

## Rule 3 — Keep related code together

Code that changes together should stay together.

Avoid moving closely related logic into different files unless there is a strong reason.

---

## Rule 4 — Prefer cohesion over small files

High cohesion is more important than having many small files.

A larger, well-organized file is preferred over many tiny files.

---

## Rule 5 — Respect the existing architecture

Follow the project's existing patterns.

Do not introduce new architectural styles, folder structures, or design patterns unless explicitly requested.

---

## Rule 6 — Simplicity wins

When multiple implementations are possible, choose the simplest solution that satisfies the current requirements.

## Rule 7 — Plan File Changes Before Implementation

Before writing code, provide a brief implementation plan.

The plan must include:

- Existing files to modify.
- New files to create (if any).
- A short reason for each new file.
- Expected total number of files that will be modified, created, or deleted.

Do not create additional files that were not included in the plan.

If implementation reveals a new file is necessary, pause and explain:
- why the original plan changed;
- why the new file is required;
- why the existing files are no longer sufficient.

Wait for user approval before creating unplanned files.