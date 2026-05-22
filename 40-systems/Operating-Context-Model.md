# Operating Context Model

This file explains how the personal Agent OS should be used across projects and platforms.

## Core Rule

- The personal Agent OS is the canonical source of truth
- Project files should inherit from it by default
- Projects should only deviate when I explicitly decide they should
- Platform-specific files should stay thin and mainly point to the right personal and project context
- Skills should be canonical in the Agent OS and adapted per harness rather than duplicated per harness

## Architecture

Use a three-layer model:

1. Personal core
2. Project overlay
3. Thin platform wrapper

### 1. Personal Core

The personal core is the stable operating system that should apply across most work unless explicitly overridden.

Primary files:

- `00-core/00-Identity.md`
- `00-core/01-Operating-Principles.md`
- `00-core/02-Communication-Style.md`
- `00-core/03-Work-Standards-and-Quality-Bar.md`
- `00-core/04-Decision-Making-Framework.md`

These files define who I am, how I want work to get done, how communication should work, what quality looks like, and how decisions should be made.

### 2. Project Overlay

Each project should have its own files for context that is specific to that project.

Typical project-layer content:

- project purpose
- goals and success criteria
- constraints
- stakeholders
- project-specific standards
- active risks and decisions
- project-specific workflows or skills

The project layer should inherit from the personal core by default.

Override only when:

- the project genuinely needs different rules
- the deviation is explicit
- the reason is clear

### 3. Thin Platform Wrapper

Platform-specific files should usually be lightweight wrappers, not separate operating systems.

Examples:

- `AGENTS.md`
- `CLAUDE.md`
- Cursor rules
- Codex or CLI agent instruction files

Their job is mainly to:

- identify the project
- point to or summarize the relevant personal core files
- point to or summarize the relevant project files
- note any platform-specific constraints

They should not become competing copies of the personal OS.

For skills, use the same rule:

- the skill body belongs in `20-skills/`
- the project-specific context belongs in the project wrapper
- the harness-specific file should be a thin adapter only

Do not create separate long-form Claude and Codex versions of the same skill unless the underlying workflow truly differs.

## Default Inheritance Rule

- inherit from the personal Agent OS by default
- adopt the personal core unless the project explicitly overrides it
- if a project overrides the personal OS, say so clearly and narrowly

Recommended language for project files:

```md
This project inherits the default standards, operating principles, communication style, and decision framework from the personal Agent OS unless this file explicitly states otherwise.
```

Recommended language for a narrow override:

```md
Override for this project:
- [specific rule]

Reason:
- [why this project requires a deviation]
```

## Override Principles

Overrides should be explicit, narrow, justified, local to the project, and reviewed periodically.

Avoid:

- silent drift from the personal core
- broad project files that accidentally replace the whole OS
- duplicate instructions that slowly diverge

## Recommended Project Pattern

For each meaningful project, maintain:

1. A project context file
2. A project goals or strategy file
3. A project-specific agent or instruction file when needed

Suggested pattern:

```text
project/
  AGENTS.md
  docs/
    project-context.md
    goals.md
    decisions.md
    risks.md
```

Where:

- `AGENTS.md` is the thin wrapper
- `project-context.md` describes the project
- `goals.md` defines objectives and success
- `decisions.md` records important choices
- `risks.md` records open concerns and tripwires

## Platform Guidance

### ChatGPT, Claude, Gemini

Use these primarily with:

- a compact personal profile derived from the core files
- a project context overlay when working on a specific project

Do not try to load the entire OS every time. Load the minimum necessary context.

### Codex / CLI Agents / Cursor

These tools are usually better served by:

- a thin project wrapper such as `AGENTS.md`
- project files that inherit from the personal core
- explicit file references when possible

For these tools, the project layer is usually more important than a rich platform-specific personal profile.

When these tools support skill files or instruction files directly, treat those as adapters to the canonical skill rather than a second source of truth.

### Claude Code And Similar Harnesses

Apply the same pattern:

- keep the durable skill in `20-skills/`
- keep project context in the project wrapper
- keep any `CLAUDE.md`, command file, or harness instruction file thin

If the Claude-facing file needs examples or invocation help, include only what is needed to activate the canonical skill correctly.

### Antigravity

Treat Antigravity like other agentic work environments:

- use a thin project wrapper
- point it to the relevant project files
- inherit from the personal core by default
- keep any tool-specific instructions narrow and operational

As with Codex, CLI agents, and Cursor, the project layer should usually matter more than a rich platform-specific profile.

### Google Docs

Use Google Docs primarily as:

- a drafting surface
- a review surface
- a staging layer for material that may later be turned into project or platform files

It should not be the canonical source of the OS.

### Voice Assistants

Voice assistants may need a much shorter conversational subset of the core.

If needed, create a short version later that emphasizes:

- tone
- brevity
- question pacing
- practical next steps

## Future Tools

When adopting a new tool in the future, default to the same model:

- personal core remains canonical
- project files provide the main operating context
- tool-specific instructions stay thin unless the tool truly requires more

For any new tool, ask:

1. Can it reference files directly?
2. Does it need a thin wrapper or a pasted profile?
3. What is the smallest useful subset of the personal core?
4. What project files matter most for the work?
5. Is any genuine override needed, or is inheritance enough?
6. Can the tool adapt the canonical skill directly, or does it tempt me into creating a duplicate?

Do not build a new standalone operating system for each new platform unless there is a clear and lasting reason.

## Load Strategy

Default to minimum viable context.

### Minimum Load

Use:

- core personal style and principles
- the immediate project context
- the specific task context
- current priorities when they materially affect the task

### Extended Load

Add only when relevant:

- role files
- skills
- templates
- current priorities
- decision or quality standards for higher-stakes work

## File Relationship Rule

- inherit first
- override second
- document the override

The burden of proof should be on the override, not on the inheritance.

## Practical Goal

The goal of this mapping system is:

- one canonical personal operating system
- many project overlays
- very thin platform wrappers
- one canonical version of each durable skill
- thin harness adapters instead of duplicated skill libraries

This should reduce duplication, stale instructions, and conflicting prompt systems while keeping the OS portable across tools.
