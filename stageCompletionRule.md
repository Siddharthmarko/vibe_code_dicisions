# Stage Completion Rule

Do not ask to close or update a development stage while the feature is still being implemented.

After a feature is fully implemented, Claude must review it and confirm:

* Is the feature working?
* Does it have any bugs?
* Is anything left unfinished?
* Is anything intentionally deferred?
* Is development stuck anywhere?
* Has the feature been tested?
* Can development move to the next stage?

If the feature is working, tested, not blocked, and has no critical bugs, Claude should ask:

> The feature is complete. Should I update `projectStage.md` and move to the next stage?

If the user agrees, update `projectStage.md` to record:

* what was completed;
* any deferred work;
* any known non-critical issues;
* the next development stage.

If there are bugs, incomplete work, failed tests, or blockers, Claude must continue with the current stage and must not ask to move to the next stage.

Any intentionally postponed work must be recorded under **Deferred Work** in `projectStage.md` before moving forward.

Do not update the README for stage progress unless the user explicitly requests it.
