# AGENTS Template

Use this template to create a project-level `AGENTS.md` file that gives AI agents a clear, practical briefing for working in a specific project.

This template follows current cross-tool best practices:

- keep `AGENTS.md` as a plain markdown file in the project root
- make it easy to scan
- put the most actionable instructions near the top
- state source-of-truth files explicitly
- include concrete build, test, and validation commands
- keep project-specific overrides narrow and explicit

Related files:

- `../40-systems/Operating-Context-Model.md`
- `../00-core/01-Operating-Principles.md`
- `../00-core/03-Work-Standards-and-Quality-Bar.md`
- `../20-skills/Skill-Authoring-Standard.md`

## When To Use

Use this template when creating a new project-level `AGENTS.md` for:

- Codex / CLI agents
- Cursor
- Claude Code or similar agentic tools
- Antigravity
- any future tool that can read or benefit from project-level instructions

## How To Use This Template

Recommended workflow:

1. Copy this template into the project root as `AGENTS.md`
2. Fill in only what is real and useful for the project
3. Keep the file short enough to scan quickly
4. Activate only the role files that are genuinely relevant
5. Add overrides only when the project truly needs them
6. Confirm commands are real and current
7. Run the final checklist at the bottom before treating the file as done

Suggested AI workflow:

- Start with this template
- Ask the AI to interview you to fill it out
- Have the AI draft the file
- Have the AI review the completed file against the final checklist

## Template

```md
# AGENTS.md

## Inheritance

This project inherits the default standards, operating principles, communication style, and decision framework from the personal Agent OS unless this file explicitly states otherwise.

If this project overrides the personal OS, the override should be narrow, explicit, and justified.

## Project Overview

- Project:
- Purpose:
- Primary users or customers:
- Current stage:
- Definition of success:

## Source Of Truth

Read these first before making meaningful changes:

- `README.md`
- `docs/project-context.md`
- `docs/goals.md`
- `docs/decisions.md`
- `docs/risks.md`

Add or remove files based on the real project.

## What The Agent Should Optimize For

- Primary objective:
- Secondary objectives:
- Non-goals:
- Key constraints:

## Active Role Files

Use this section to activate role files from the personal Agent OS when they are relevant to this project.

Only include roles that are genuinely useful for the project.

Example:

- `10-roles/Technical-Advisor.md` for technical decisions, architecture, code explanation, and production-safety guidance
- `10-roles/AI-Mentor.md` for prompting, model/tool choice, context strategy, evaluation, and agent workflow design
- `10-roles/Chief-of-Staff.md` for prioritization, focus, and follow-through support

If no extra role files are needed, omit this section or say so explicitly.

## Reusable Skills

Use this section to point agents at canonical skills in the personal Agent OS when the project repeatedly needs a specific kind of work.

Do not copy the body of the skill into this file. Reference the canonical skill and add only brief project-specific activation notes.

Example:

- `20-skills/Strategy/Decision-Memos.md` for decision writeups in this project
- `20-skills/Technical/Code-Review.md` for review passes focused on bugs, regressions, and missing tests

Optional project note format:

- `20-skills/...`
  - Use when:
  - Project-specific caution:

## Key People

Keep this section brief. Include only project-relevant notes.

- Decision-maker:
- Project owner:
- Key collaborators:
- Stakeholders:

Optional working notes:

- Who needs extra context
- Who decides quickly or slowly
- Who should review sensitive changes

## Project-Specific Standards

Only include standards that are truly project-specific.

- Architecture:
- Code style:
- Testing expectations:
- Security or privacy requirements:
- Performance constraints:
- UX or product principles:

## Explicit Overrides

Only fill this out when the project genuinely needs to deviate from the personal OS.

Example:

- Override:
  - Use longer-form explanation than usual in this repo because artifacts are reused as stakeholder docs.
- Reason:
  - This project serves both implementation and executive communication needs.

## Do

- Read the source-of-truth files first
- Keep changes scoped to the task
- Prefer small diffs unless a larger change is clearly justified
- Explain assumptions when context is missing
- Update related docs when the change affects behavior, decisions, or constraints
- Validate changed files with the smallest useful command first

## Don't

- Do not invent requirements that are not in the project files
- Do not use stale context from another project
- Do not rewrite large areas of the codebase unless asked or clearly necessary
- Do not add dependencies without justification
- Do not skip validation when a targeted check is available
- Do not override personal OS instructions silently

## Commands

Use the most targeted command that gives confidence.

### Setup

- Install dependencies: `...`
- Start development environment: `...`

### Validation

- Lint changed files: `...`
- Typecheck changed files: `...`
- Run relevant tests: `...`
- Run full test suite only when needed: `...`

### Build

- Build project: `...`

## Preferred Workflow

1. Read the project overview and source-of-truth files.
2. Confirm the actual task and constraints.
3. Check whether the personal OS is enough or whether a project-specific override applies.
4. Make the smallest useful change that solves the problem.
5. Validate with targeted commands first.
6. Summarize what changed, risks, and next steps clearly.

## Decision And Escalation Rules

- Ask before destructive or high-blast-radius changes.
- Ask before adding major dependencies or changing architecture significantly.
- Ask when project files conflict or when requirements are materially unclear.
- Before substantial work, consider whether the current model is appropriate for the task. If the task appears overpowered or underpowered for the current model, suggest a better fit before proceeding.
- Skip the model-fit check for simple, low-stakes questions where the overhead would outweigh the benefit.
- When asking the user to choose, provide `2-3` options, brief pros and cons, and a recommended default only when the choice has meaningful tradeoffs or ambiguity.
- Proceed with stated assumptions when the risk is low and the benefit of momentum is high.

## Current Priorities

Keep this section current if the project is active.

- Primary:
- Secondary:
- Known risks:
- Open decisions:

## Notes For Future Agents

- Important context that is easy to miss:
- Known sharp edges:
- Historical decisions that still matter:
```

## Final Checklist

Before treating a project `AGENTS.md` as complete, confirm:

- the file lives in the project root
- the inheritance statement is present
- the project purpose and success criteria are clear
- source-of-truth files are real, current, and worth reading first
- objectives, non-goals, and constraints are explicit
- reusable skills are referenced rather than copied
- active role files are intentionally chosen rather than copied by default
- project-specific standards are actually project-specific
- overrides are narrow, explicit, and justified
- do/don't rules are useful and not generic filler
- commands are real, current, and appropriately scoped
- key people are included only if they materially help the agent
- current priorities are current or omitted
- the file does not duplicate large amounts of existing documentation
- the file is short enough to scan quickly
- an agent could read it and work safely within minutes
- template instructions, examples, and checklist scaffolding have been removed from the finished `AGENTS.md`
- the final file has been compressed into a clean operational briefing that contains only live project instructions
