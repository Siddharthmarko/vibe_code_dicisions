# Claude Project Instructions

This is the primary instruction file for the project.

The user only needs to reference `claude.md`.

Claude is responsible for automatically determining which supporting rule files are relevant to the current task and loading only those files.

Do not duplicate, summarize, rewrite, or explain the contents of supporting rule files unless the user explicitly requests it.

---

# Primary Objectives

Always prioritize the following:

1. Correctness
2. Simplicity
3. Project consistency
4. Incremental development
5. Maintainability
6. User control over architectural decisions

Never optimize for future possibilities at the expense of the current project stage.

---

# Reasoning Check

Before every task:

1. Identify:
   - selected Claude model (if visible)
   - thinking mode (if visible)
   - reasoning effort (if visible)

2. Review:
   - current request
   - previous prompts
   - recent conversation
   - current project state

3. Decide whether the selected reasoning level is appropriate.

If a lower reasoning level is sufficient:

- continue with focused reasoning
- minimize unnecessary thinking
- minimize token usage

If a higher reasoning level is required:

Explain why before continuing.

Never use high-effort reasoning for simple implementation tasks.

---

# General Workflow

For every request:

1. Understand the request.
2. Determine the project stage.
3. Load only the required rule files.
4. Decide whether planning is required.
5. Implement only the requested scope.
6. Review impact.
7. Suggest optional improvements.
8. Verify completion.
9. If applicable, update project stages only after user approval.

---

# Supporting Rule Files

Core

- planning.md
- development-rules.md
- incremental-development.md
- code-organization.md
- component-extraction.md

Project

- project-assessment.md
- project-foundation.md
- evaluation-engine.md
- project-stages.md
- stage-completion.md

Quality

- error-resolution.md
- impact-review.md
- enhancements.md

---

# Rule File Selection

Only load files required for the current task.

Never load every rule file.

---

## planning.md

Read before:

- implementing any feature
- modifying existing code
- refactoring
- changing architecture
- adding dependencies
- changing project structure

Purpose:

- understand the request
- review existing code
- explain implementation plan
- define affected files
- stay within scope

---

## project-assessment.md

Read before:

- evaluating an existing project
- determining project maturity
- deciding AI autonomy
- understanding an unfamiliar repository

---

## project-foundation.md

Read before:

- making architecture decisions
- deciding folder structure
- deciding naming conventions
- introducing project-wide patterns
- changing core project decisions

---

## evaluation-engine.md

Read before implementation begins.

Purpose:

Determine:

- whether implementation should begin
- whether planning is sufficient
- appropriate reasoning effort
- implementation scope
- AI autonomy

---

## development-rules.md

Read before:

- writing code
- editing code
- implementing features
- fixing bugs
- refactoring
- changing behavior

Purpose:

Ensure correct implementation order and maintain project integrity.

---

## incremental-development.md

Read before:

- extending existing code
- improving features
- deciding refactoring
- making architecture improvements

Purpose:

Ensure:

- gradual development
- beginner/intermediate complexity
- no overengineering
- consistent implementation

---

## code-organization.md

Read before deciding whether to:

- create new files
- split files
- move code
- reorganize folders
- introduce modules

Purpose:

Keep the project simple and cohesive.

---

## component-extraction.md

Read only after deciding code may leave the current file.

Purpose:

Determine whether:

- components
- hooks
- utilities
- services
- helper functions

should actually be extracted.

Avoid speculative abstractions.

---

## error-resolution.md

Read before:

- fixing errors
- debugging
- resolving build failures
- handling runtime issues

Purpose:

Ensure:

- root cause analysis
- evidence-based fixes
- minimal unrelated changes
- verified solutions

---

## impact-review.md

Read after implementation is complete.

Purpose:

Review the broader project impact.

Check whether related updates are recommended.

Separate:

- Required changes
- Optional consistency improvements

Never assume optional changes should be implemented.

---

## enhancements.md

Read after implementation and impact review.

Purpose:

Identify meaningful improvements.

Only recommend improvements appropriate for the current stage.

Never automatically implement optional enhancements.

Ask the user which improvements should be applied.

---

## project-stages.md

Read before:

- starting a feature
- selecting the next task
- deciding current stage work
- deciding deferred work
- updating progress

---

## stage-completion.md

Read only when a feature appears complete.

Before closing a stage verify:

- implementation complete
- required work finished
- tested
- project runnable
- no blockers remain

If deferred work exists:

Record it in `project-stages.md`.

Only after verification ask:

> The current stage is complete. Should I update `project-stages.md` and move to the next stage?

Never update project stages automatically.

Never update README unless explicitly requested.

---

# Rule Loading Priority

When multiple rule files apply, follow this order:

1. planning.md
2. project-assessment.md
3. project-foundation.md
4. evaluation-engine.md
5. development-rules.md
6. incremental-development.md
7. code-organization.md
8. component-extraction.md
9. error-resolution.md
10. impact-review.md
11. enhancements.md
12. stage-completion.md

Later rules supplement earlier rules.

If two rules appear to conflict:

1. Prefer correctness.
2. Prefer explicit user instructions.
3. Prefer project consistency.
4. Prefer simplicity.
5. Avoid future-proof abstractions.

---

# Automatic Rule Loading

Determine which rule files are relevant.

Load only those files.

Do not load unrelated rules.

The user should never need to manually specify supporting files.

---

# Core Principles

Always:

- implement one feature at a time
- keep the project runnable
- explain important decisions
- minimize unnecessary reasoning
- avoid unnecessary abstractions
- prefer existing files
- respect current architecture
- review implementation impact
- recommend optional improvements
- let the user choose optional changes

Never:

- overengineer
- optimize prematurely
- create unnecessary files
- refactor without reason
- change unrelated code
- assume optional improvements should be implemented
- move to the next stage automatically

---

# Success Criteria

A task is considered complete only when:

- the requested work is finished
- related required updates are completed
- optional updates have been presented
- the user's choices have been respected
- no project consistency issues remain
- the project remains runnable
- the current stage (if applicable) has been verified