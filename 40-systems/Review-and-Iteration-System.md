# Review and Iteration System

This file defines how the Agent OS should be reviewed, improved, and kept current over time.

## Purpose

The Agent OS should improve when repeated friction appears. The goal is not to patch every mistake. The goal is to notice recurring failure patterns and convert them into better system design.

## Core Loop

Use this cycle:

1. Detect
2. Propose
3. Capture
4. Review
5. Adopt or reject

## 1. Detect

When something goes wrong in a chat, project, or workflow, first ask:

- Was this a one-off execution mistake?
- Or does it reveal a structural gap in the Agent OS?

Examples of likely structural issues:

- repeated formatting misses
- repeated need to restate preferences
- stale or wrong context reuse
- weak project inheritance
- unclear priorities
- outputs that miss the right level of depth
- workflow friction from too many steps or duplicate files
- recurring quality misses despite existing instructions

Do not propose an OS change for every isolated error. Reserve changes for problems that are likely to recur or meaningfully improve quality, speed, clarity, or consistency.

## 2. Propose

If the issue appears structural, propose a specific fix:

- name the failure pattern briefly
- say why it is likely systemic
- propose the smallest useful improvement
- identify where the fix should live

Possible homes:

- `00-core/`
- `10-roles/`
- `20-skills/`
- `30-templates/`
- `40-systems/`
- project `AGENTS.md`

## 3. Capture

Record proposed changes in:

- `90-inbox/Changes-To-Make.md`

Each captured item should include:

- observed problem
- proposed fix
- recommended file or layer
- priority
- status: proposed / adopted / rejected / deferred

## 4. Review

Review captured changes on a regular cadence:

- quick weekly scan
- fuller biweekly or monthly review
- larger architectural cleanup when the OS starts to feel bloated or inconsistent

The weekly scan should follow `40-systems/AgentOS-Weekly-Review-System.md`.

During review, ask:

- is this problem recurring enough to justify a change?
- is the proposed fix the smallest good fix?
- should it live in the personal core, a role, a skill, a template, or a project file?
- would this change improve future chats or just memorialize a one-off annoyance?

The weekly review should also detect:

- interview loops
- repeated questions after the contract is already clear
- stale queue items
- approved items that still have not been implemented

## 5. Adopt Or Reject

For each proposed change:

- adopt it
- reject it
- defer it

When a change is adopted:

- update the actual file
- update `Change-Log.md` when the change is meaningful
- remove the item from `Changes-To-Make.md`

If the user approves a change but wants implementation to happen later:

- add it to `90-inbox/Approved-Changes.md`
- implement it in the approved follow-up step
- remove it from both live queues after implementation

## Chief Of Staff Connection

The Chief of Staff should notice recurring friction and convert it into system improvements rather than repeated annoyance.

Examples:

- recurring drift in priorities
- repeated overcommitment
- repeated workflow complexity
- repeated low-value tasks or formatting misses

## Project-Level Version

This same loop should also apply inside projects.

If a problem is project-specific rather than personal, prefer fixing:

- the project `AGENTS.md`
- project docs
- project templates

before changing the personal core.

## Success Standard

This system is working when:

- the same preventable mistake happens less often
- recurring annoyances become explicit improvements
- the OS gets sharper without becoming bloated
- changes are driven by recurring reality, not theoretical perfectionism
- live queues stay short, current, and free of stale accepted items
