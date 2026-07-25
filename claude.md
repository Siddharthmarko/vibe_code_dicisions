# Claude Project Instructions

This is the main instruction file for the project.

The user only needs to reference `CLAUDE.md`. Claude must automatically read the relevant supporting rule files before working on a task.

Do not duplicate, summarize, rewrite, or explain the contents of the supporting files unless the user explicitly asks.

## Reasoning Check

Before every task:

* identify the selected Claude model, thinking mode, and effort level when visible;
* review the current request, previous prompts, and relevant conversation context;
* decide whether the selected reasoning level is appropriate for the task.

If a lower level is sufficient, continue with focused reasoning and minimal token usage.

If the task requires a higher model, thinking mode, or effort level than currently selected, tell the user what should be changed before continuing.

Do not use excessive reasoning or tokens for simple tasks.

## Supporting Rule Files

* `developmentRule.md`
* `graduallyDevelopment.md`
* `projectStage.md`
* `stageCompletionRule.md`

## Rule File Selection

### `developmentRule.md`

Read before:

* writing code;
* editing code;
* fixing bugs;
* creating features;
* refactoring;
* changing project behavior.

---

### `graduallyDevelopment.md`

Read before:

* extending existing code;
* improving an existing feature;
* making architectural changes;
* deciding whether to refactor;
* considering functionality planned for later.

---

### `projectStage.md`

Read before:

* starting a feature;
* selecting the next task;
* deciding what belongs in the current stage;
* deciding what should be deferred;
* moving between project stages.

---

### `stageCompletionRule.md`

Read only when a feature appears fully completed.

Use it before:

* closing a feature;
* updating stage progress;
* asking to move to the next stage.

Do not apply this rule while implementation is still in progress.

## Automatic Rule Loading

For every code-related task, automatically read:

1. `developmentRule.md`
2. `graduallyDevelopment.md`
3. `projectStage.md`

When the feature is fully completed, also read:

4. `stageCompletionRule.md`

For non-code tasks, read only the supporting files relevant to the request.

The user should not need to tag or mention the supporting files separately.

Follow the instructions inside each selected file directly.
