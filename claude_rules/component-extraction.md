# Component Extraction Rules

## Purpose

These rules apply after the decision has been made that code may leave the current file.

Use these rules when deciding whether to extract:

- components;
- hooks;
- utilities;
- helper functions;
- services;
- modules.

The goal is to extract code only when it improves the current project, not for possible future reuse.

---

## Rule 1 — File length is not a reason to split

Do not split a file simply because it becomes long.

A file with several hundred lines is acceptable if it still represents a single responsibility.

---

## Rule 2 — Split by responsibility, not by size

Create a new component, hook, or module only when it has a clear and independent responsibility.

Bad:

- Splitting only to reduce line count.
- Splitting only because the JSX looks long.

Good:

- Independent UI section.
- Independent business logic.
- Independent state management.
- Independent feature.

---

## Rule 3 — Follow the Rule of Two

Do not extract helpers, utilities, hooks, or components until the same logic is needed in at least two places, unless extraction significantly improves clarity.

Avoid speculative abstractions.

---

## Rule 4 — No future-proof abstractions

Do not create reusable systems, helper layers, service layers, or wrappers based on possible future requirements.

Build only for the current requirements.