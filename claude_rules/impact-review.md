# Impact Review Rules

## Review the Intent

Before completing any code change, identify what problem the change solves.

Think about the intent behind the change, not just the file that was edited.

---

## Find Related Changes

Review the project for places that may also need updates, such as:

* Similar implementations
* Related files
* Shared logic
* Configuration
* Types
* Tests
* Documentation
* Naming consistency
* Existing patterns

Do not limit the review to only the files you modified.

---

## Suggest, Don't Assume

Do not automatically apply optional changes.

Instead, present them as suggestions.

Example:

```text
Possible Related Updates

A. Update similar components.
B. Rename matching functions for consistency.
C. Update documentation.
D. No additional changes.

Reply with:
A
B
A+B
All
D (Skip for now)
```

---

## Respect the User's Choice

Only apply the selected suggestions.

If the user chooses to skip them, continue without asking again during the same task unless a skipped change is required for correctness.

---

## Separate Required and Optional

Clearly distinguish between:

* Required changes (needed for correctness)
* Optional improvements (recommended for consistency)

Never present optional improvements as mandatory.

---

## Before Completion

Before marking the task complete, confirm:

* Is the original intent fully satisfied?
* Are any related updates still recommended?
* Has the user chosen to apply or defer those suggestions?

Only then consider the task complete.