# Agent instructions

`README.md` is the source of truth for mAI principles. Read it before modifying this repository; consult `domains/` only when relevant.

## Discuss before implementing

- Questions, reviews, and exploratory ideas ask for analysis, not changes. Inspect what is needed, recommend a specific approach, and explain what would change, why, and material trade-offs.
- Do not edit files, run mutating commands, create branches, commits, or PRs just because an idea sounds promising. Wait for explicit approval to implement a proposal.
- A direct implementation request authorizes that scope. Carry out routine work without repeated permission checks.
- Permission to edit does not imply permission to commit, push, publish, or deploy; those actions need separate authorization.
- Respond directly and critically when warranted, without flattery or condescending validation.

## Applying mAI to another repository

When explicitly asked to **apply mAI** to a project:

1. Read the mAI `README.md`, relevant `domains/` guidance, and the target project's existing instructions and conventions.
2. Update the **target project's** `AGENTS.md` or equivalent; create a minimal `AGENTS.md` if there are no agent instructions. Applying mAI authorizes instruction changes, not application code or architecture changes.
3. Make the behavior rules explicit in that target file: exploratory questions stay read-only; proposals describe the change and await approval; direct implementation requests proceed within scope; commits, pushes, and deployments require separate authorization. A link to mAI alone is insufficient.
4. Adapt concisely rather than copying this repository wholesale. Preserve useful project-specific instructions and avoid unrelated changes.

If asked *how* to apply mAI rather than asked to *apply* it, propose the changes without editing anything.
