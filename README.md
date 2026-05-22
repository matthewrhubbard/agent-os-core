# Agent OS

This folder is a portable operating system for working with AI tools across projects and platforms.

## Structure

- `00-core/`: stable, high-authority files about identity, principles, and standards
- `10-roles/`: role-based operating modes that are active and usable, plus `_drafts/` for unfinished role ideas
- `15-people/`: optional collaborator and team-context notes
- `20-skills/`: repeatable procedures for recurring kinds of work
- `30-templates/`: reusable document and planning templates
- `40-systems/`: governance, operating context, current-context patterns, iteration, and maintenance
- `90-inbox/`: optional private capture area for ideas and improvements
- `99-archive/`: inactive or superseded material

## Canonical Files

- `00-core/` is the highest-authority layer for operating rules
- `40-systems/Operating-Context-Model.md` defines how the OS should be used across projects and tools
- `30-templates/Current-Context-Template.md` is the public-safe template for live current context
- `20-skills/` is the canonical layer for durable reusable skills across harnesses

## Reading Order

If entering the OS cold, start here:

1. `00-core/`
2. `40-systems/Operating-Context-Model.md`
3. `30-templates/Current-Context-Template.md` or your local current-context file
4. only then pull in roles, skills, or templates as needed

## Public And Private Layers

This system works best as:

- one shared core for durable principles, roles, skills, templates, and system logic
- one optional private overlay for live priorities, people notes, inboxes, and other sensitive context

If you are publishing or collaborating in a public repo, keep the shared core canonical and move private live context into a separate private layer rather than maintaining two full versions.

## Optional Private Overlay

The shared core is meant to stand on its own, but many users will want a private overlay that adds live context the public repo should not contain.

Common private-overlay docs include:

- a live current-context or priorities file
- collaborator, stakeholder, or relationship notes
- an inbox or change queue
- weekly reviews or operating retrospectives
- sensitive decision logs
- private project overlays with local constraints, notes, or planning context

These are categories, not a required structure.

The main rule is simple:

- the shared core may inform the private overlay
- the private overlay should not be required for the shared core to make sense

## Operating Rule

Core files should be treated as the highest-authority sources. Support files should link back to them where relevant.

Do not maintain separate long-form skill libraries per harness when a single canonical skill plus thin adapters will do.
