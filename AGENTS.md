# AGENTS.md

## Purpose

This folder is the canonical Agent OS layer.

Use it for durable operating principles, reusable roles, repeatable skills, templates, and system logic that should work across projects and tools.

## Reading Order

Read these first:

1. `README.md`
2. `00-core/`
3. `40-systems/Operating-Context-Model.md`
4. the local current-context file or `30-templates/Current-Context-Template.md`

Only then pull in roles, skills, templates, or additional system docs as needed.

## How To Use This Folder

- Treat `00-core/` as the highest-authority layer.
- Treat `20-skills/` as the canonical skill library.
- Treat `30-templates/` as the default artifact shapes.
- Treat `40-systems/` as the canonical system-design and governance layer.

## Public And Private Split

This folder is designed to support a shared core plus an optional private overlay.

- The shared core should contain durable logic and reusable artifacts.
- The private overlay may contain live priorities, people notes, inboxes, and sensitive context.
- Do not make the shared core depend on private files.

## Editing Rules

- Keep changes scoped to the smallest useful layer.
- Prefer improving canonical files over creating duplicate variants.
- Add a new file only when the content is truly a distinct durable artifact.
- If a file mixes reusable logic with sensitive live context, separate the context rather than cloning the whole document.
- Ask follow-up questions one at a time. Do not bundle several questions into one paragraph, bullet list, numbered list, or "quick questions" section.
- Before committing or pushing Agent OS changes, recommend the Git path: direct to main only for tiny low-risk local or documentation fixes; branch + PR for behavior-changing, structural, shared, public, or higher-risk changes. Explain the reason briefly.

## Validation Rule

Before finalizing meaningful changes:

- check links, references, and reading order
- confirm the shared core still works without any private-only files
- preserve valuable logic when sanitizing sensitive content
