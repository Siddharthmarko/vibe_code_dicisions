# Incremental Development Rules

## Development Level

Write code at a beginner-to-intermediate level unless the task specifically requires a more advanced implementation.

Do not begin with highly abstract, optimized, or production-ready code.

Prefer code that is:

* simple;
* readable;
* easy to explain;
* easy to test;
* easy to extend later.

## Work With the Existing Code

Assume the project is under active development.

Before making changes:

1. Review the existing implementation.
2. Understand the current project structure and coding style.
3. Identify the files and modules related to the task.
4. Extend or improve the existing implementation instead of replacing it unnecessarily.

Do not rewrite working beginner-level code into an advanced architecture unless the current task requires that change.

## Build Gradually

Develop the project one requirement at a time.

For each task:

1. Implement only what is currently required.
2. Keep the implementation appropriate for the current stage of the project.
3. Avoid adding unrelated features.
4. Avoid premature abstractions and optimization.
5. Leave clear extension points for future improvements.

It is acceptable to use:

* placeholders;
* TODO comments;
* simple interfaces;
* template functions;
* empty modules intended for later work;

provided they are clearly marked and do not break the current application.

## Avoid Overengineering

Do not add complexity for possible future requirements.

Do not create unnecessary:

* design patterns;
* base classes;
* factories;
* generic frameworks;
* configuration layers;
* caching systems;
* background workers;
* advanced error-handling systems;
* performance optimizations.

Add these only when a real requirement justifies them.

## Maintain Project Consistency

When implementing a task, review related parts of the project.

Check whether the change also requires updates to:

* models;
* schemas;
* services;
* routes;
* dependencies;
* configuration;
* database migrations;
* tests;
* documentation;
* imports;
* type definitions.

Update affected files when necessary so the project remains consistent.

Do not modify unrelated files.

## Refactor Gradually

Refactor only when the existing code creates a real problem, such as:

* repeated logic;
* unclear responsibilities;
* difficult testing;
* growing complexity;
* inconsistent behavior;
* tight coupling.

Improve the code step by step as the project grows.

Do not perform a large architectural rewrite unless explicitly requested.




## Future Development

Consider how the current implementation may evolve, but implement only what is required now.

When future work is expected:

* keep functions small;
* use clear names;
* avoid unnecessary coupling;
* leave TODO comments where useful;
* define simple extension points;
* document important assumptions.

Do not implement future features in advance.

## Before Completing a Task

Before finishing:

1. Confirm that the current requirement is implemented.
2. Review all changed files.
3. Check whether related files also require updates.
4. Remove broken imports and unused code.
5. Confirm that existing behavior still works.
6. Add or update relevant tests.
7. Keep the project runnable.
8. Clearly mention any placeholders, TODOs, or deferred improvements.

## Core Rule

Build the simplest correct implementation for the current stage of the project, while keeping the code clear enough to improve gradually in future tasks.
rule :- 
Do not create dedicated single functions. Wait until a function is used in multiple places before extracting it.
