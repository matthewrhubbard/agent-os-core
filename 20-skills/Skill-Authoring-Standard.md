# Skill Authoring Standard

Use this file as the default standard for creating new portable skills in the Agent OS.

## Purpose

Skills should be reusable across projects, tools, and contexts without blindly carrying over stale assumptions. A skill should help execute a kind of work well, not accidentally mix contexts.

Canonical skill content should live here in the Agent OS, not in separate hand-maintained copies for each AI harness.

## What A Skill Is

A skill is a repeatable operating procedure for a specific kind of work.

Good examples:

- Decision memos
- Strategy analysis
- Meeting prep
- Code review
- Project intake
- Email drafting

A skill is not:

- A broad life philosophy
- A project memory file
- A platform-specific prompt wrapper
- A generic brainstorm with no workflow
- A duplicate Claude-only or Codex-only rewrite of the same operating procedure

## Default Skill Structure

Most skills should include:

1. Title
2. Purpose
3. Related files
4. Context check
5. When to use
6. Core principles
7. Workflow
8. Output structure
9. Quality bar
10. Common failure modes

## Context Check Pattern

Every portable skill should begin by orienting to the current context before doing work.

Use a section like this:

```md
## Context Check

Before using this skill:

- Identify the current project, domain, or life area
- Identify the relevant source-of-truth files
- Confirm the intended audience and output
- Check whether assumptions may be stale or imported from another context
- If key context is missing, ask one targeted question with likely options, brief tradeoffs, and a recommended default, or state assumptions explicitly when reasonable
```

This does not solve all context drift. It does reduce obvious cross-project or cross-session mistakes.

## Writing Guidelines

- Keep skills portable and platform-neutral
- Prefer plain English over platform jargon
- Use concise sections and predictable headings
- Avoid unnecessary verbosity
- Make the workflow concrete enough to execute
- Link to core files when the skill depends on them

## Canonical Source Rule

- The durable skill body should live once in `20-skills/`
- Harness-specific files should adapt the skill, not re-express it from scratch
- Do not maintain parallel copies of the same skill for Claude, Codex, Cursor, or other tools unless the workflow is materially different
- If a tool needs special invocation syntax, file references, or formatting, keep that logic in a thin wrapper or manifest
- If a harness-specific file becomes long, opinionated, or workflow-heavy, move the durable content back into the canonical skill and shrink the wrapper

## Harness Adapter Pattern

When a skill needs to work across tools:

1. Keep the operating procedure in the canonical skill file
2. Keep project context in the project wrapper such as `AGENTS.md`
3. Keep tool-specific instructions in a thin adapter

Thin adapters may include:

- how the harness discovers or invokes the skill
- what files it should read first
- tool constraints such as command format, context limits, or manifest fields

Thin adapters should not include:

- a rewritten workflow
- duplicated quality standards
- a separate version of the same failure modes
- project-specific context that belongs in the project wrapper

## Scope Guidelines

- A skill should cover one kind of work well
- If a file starts trying to do several different jobs, split it
- Keep durable principles in `00-core/`
- Keep role-based behavior in `10-roles/`
- Keep project-specific context outside the core Agent OS unless it is intentionally templated

## Quality Bar

A good skill:

- Is easy to scan
- Tells the user when to use it
- Checks context before acting
- Produces better work than a generic prompt
- Makes quality and failure modes explicit
- Works across multiple projects and AI platforms

## Recommended Naming

- Use clean filenames without adding `Skill` redundantly inside `20-skills/`
- Prefer names like `Strategy-Analysis.md` over `Strategy-Analysis-Skill.md`
- If a platform later needs different naming, handle that in `40-systems/Operating-Context-Model.md`
