# Project instructions

## Current boundary

- Do not begin the site audit, implementation, refactoring, or deployment until the user explicitly asks after the planning phase.
- The next phase is planning only: determine a token-efficient workflow, model assignments, and reasoning levels suitable for a ChatGPT $20 subscription with five-hour usage windows.

## Project goal

- Update the E-design theme generator and its CSS coverage for the current Shikimori sites.
- Audit and support `shikimori.rip` first. Audit `shikimori.io` only after the `.rip` work reaches its planned completion checkpoint.
- Find and style currently unsupported page elements and states while following the visual language of every existing project style.
- Preserve the original styles. Do not redesign, reinterpret, modernize, normalize, or otherwise change their intended appearance.

## Resource constraints

- Work economically within recurring five-hour token windows. Expect work to pause when a window is exhausted and resume later.
- Prefer the least expensive model and reasoning level that can reliably complete each bounded task. Reserve stronger models and higher reasoning for orchestration, difficult conflicts, and selected reviews.
- Keep durable, concise checkpoints in the repository so work can resume without repeating discovery.
- Avoid redundant browsing, repeated verification, speculative investigations, optional tasks, and work done "just in case."
- Do not create new tests, test frameworks, test fixtures, or unrelated QA infrastructure.
- Use only the minimum verification needed to establish that a requested change works. Do not perform extra regression passes unless a concrete risk or failure justifies them.

## Change discipline

- Keep changes strictly scoped to compatibility and generator support.
- Do not perform unrelated refactors, renames, formatting passes, dependency upgrades, framework migrations, or architectural rewrites.
- Prefer small maintainable additions to existing selectors and variables over replacing established CSS.
- Do not remove existing style behavior unless it is demonstrably obsolete and the user has approved the change.
- Treat authenticated browser access as a scarce sequential resource. Do not let multiple agents manipulate the same browser/profile concurrently.

## Delivery direction

- The updated generator is intended to be a forked continuation rather than an overwrite of the original upstream project.
- The intended final delivery is a fork under the user's GitHub account with its own GitHub Pages generator page.
- Do not create the fork, push changes, publish GitHub Pages, or modify remote settings until the user explicitly authorizes those actions.
- Until the first push is requested, work locally on the dedicated `codex/shikimori-compatibility` branch and keep the existing `origin` unchanged.
- Before the first push, preserve the original repository as the `upstream` remote and configure the user's fork as `origin`.
- Maintain Git history with small, scoped commits at meaningful resumable checkpoints. Do not commit unrelated user changes.

## Planning requirements

- Before implementation, produce a phased plan optimized for the subscription limits.
- The plan must assign Luna, Terra, and Sol only where each is justified and must choose the orchestrator's Sol reasoning level.
- Define resumable checkpoints and completion criteria without adding new project tests or unnecessary documentation.
