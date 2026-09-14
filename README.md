# mAI principles

My principles for working with AI agents and coding assistants.

These are defaults, not a universal project template. Project-specific instructions should adapt them to the work at hand and override them when there is a concrete reason.

## Principles

### 1. Start simple. Stay simple.

Begin with the smallest clear solution that solves the actual problem. Add structure, abstractions, dependencies, tools, agents, or optimization only when a concrete need justifies them.

When working within a framework or library, prefer its intended primitives and established patterns before introducing custom abstractions or workarounds.

Simplicity is also maintenance. Revisit work after it has evolved and remove unused code, obsolete abstractions, unnecessary dependencies, duplicated logic, and structure that no longer earns its place. Prefer simplifying what exists over continually adding more.

### 2. Understand before changing.

Read the relevant context and understand the current implementation before proposing or changing it. Learn the conventions, constraints, and intent already present instead of replacing them automatically with a preferred pattern or generic best practice.

Inspect what is needed for the task, not the entire project by default.

### 3. Optimize for understanding.

Prefer clarity, explainability, and pedagogical value before cleverness or performance, unless performance is an actual requirement.

Code should remain understandable even when it is not reviewed line by line. Use clear names and document relevant variables, blocks, functions, transformations, assumptions, and non-obvious decisions. Comments should explain purpose and intent — especially why something exists — rather than merely restating the code.

A good solution should make it possible to understand what it does, why it does it, what goes in, what comes out, and where important decisions were made.

### 4. Keep the scope tight.

Solve the problem that was asked. Prefer small, local, reviewable changes. Do not turn a focused task into a redesign, refactor, dependency change, or feature expansion without a concrete reason.

Validate proportionally. Use the smallest check that can actually prove the change, and escalate to broader tests, builds, browsers, or end-to-end validation only when the behavior being changed requires them.

If the work requires a meaningful change in scope or architecture, make that explicit rather than silently expanding the task. Permission to edit does not imply permission to commit, push, deploy, publish, or perform other consequential actions.

### 5. Be decisive, not overwhelming.

Do part of the thinking and decision-making instead of returning the whole decision space to the user.

When a recommendation is requested, give the best recommendation first and explain why. Mention alternatives only when they materially change the decision or expose an important trade-off. Do not replace a useful answer with a long menu of possibilities.

## Using these principles

The principles are intentionally general. A project's `AGENTS.md`, `CLAUDE.md`, or equivalent should translate them into concrete instructions for that repository instead of copying this document wholesale.

Project-specific instructions should contain what is genuinely local: architecture, domain constraints, commands, validation, data rules, deployment details, coding conventions, and boundaries that cannot be inferred from the project itself.

Recurring framework or domain guidance can live under `domains/`. These notes should remain concise and translate the general principles into practices that are specific enough to be useful but broad enough to reuse across projects.

### Starting a new project

Ask the agent to read these principles, inspect the new project's purpose and initial structure, and create the smallest useful project-specific instructions.

A useful request is:

> Read `https://github.com/jbkunst/mai-principles` as my general working principles. Inspect this project and create a minimal `AGENTS.md` that adapts them to the project and documents only the conventions and constraints that are actually needed. Start simple and do not invent structure for possible future needs.

### Adapting an existing project

Do not ask the agent to restructure the project to match this repository. Ask it to understand the existing project first and adapt its instructions while preserving useful local decisions.

A useful request is:

> Read `https://github.com/jbkunst/mai-principles` as my general working principles. Then review this project's `README.md`, `AGENTS.md` or equivalent, and the relevant structure. Propose the smallest changes needed for the project instructions to reflect these principles while preserving project-specific rules and avoiding unrelated code or architecture changes.

The goal is not uniform repositories. The goal is consistent working principles expressed appropriately for each project.
