# Agent instructions

- Read `PROJECT.md` before planning or implementing work for the current compatibility initiative.
- Keep changes strictly scoped to the user's requested work.
- Preserve the original styles. Do not redesign, reinterpret, modernize, normalize, or otherwise change their intended appearance.

## Resource constraints

- Work economically within the available token windows.
- Prefer the least expensive model and reasoning level that can reliably complete each bounded task. Reserve stronger models and higher reasoning for orchestration, difficult conflicts, and selected reviews.
- Keep durable, concise checkpoints in the repository so work can resume without repeating discovery.
- Avoid redundant browsing, repeated verification, speculative investigations, optional tasks, and work done "just in case."
- Do not create new tests, test frameworks, test fixtures, or unrelated QA infrastructure.
- Use only the minimum verification needed to establish that a requested change works. Do not perform extra regression passes unless a concrete risk or failure justifies them.

## Change discipline

- Do not perform unrelated refactors, renames, formatting passes, dependency upgrades, framework migrations, or architectural rewrites.
- Prefer small maintainable additions to existing selectors and variables over replacing established CSS.
- Do not remove existing style behavior unless it is demonstrably obsolete and the user has approved the change.
- Treat authenticated browser access as a scarce sequential resource. Do not let multiple agents manipulate the same browser/profile concurrently.

## Git

- Do not create the fork, push changes, publish GitHub Pages, or modify remote settings until the user explicitly authorizes those actions.
- Until the first push is requested, work locally on the dedicated `codex/shikimori-compatibility` branch and keep the existing `origin` unchanged.
- Before the first push, preserve the original repository as the `upstream` remote and configure the user's fork as `origin`.
- Maintain Git history with small, scoped commits at meaningful resumable checkpoints. Do not commit unrelated user changes.
