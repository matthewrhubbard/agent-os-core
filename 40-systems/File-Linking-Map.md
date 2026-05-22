# File Linking Map

This file documents important relationships between files and which files should inform others.

## Core Authority

- `00-core/00-Identity.md` is the highest-authority statement of values and orientation
- `00-core/01-Operating-Principles.md` translates identity into default behavior
- `00-core/03-Work-Standards-and-Quality-Bar.md` defines what "good enough to ship" means
- `00-core/04-Decision-Making-Framework.md` governs decision quality across roles and skills

## Role Dependencies

- `10-roles/Chief-of-Staff.md` should draw from identity, operating principles, communication style, and the current-context layer
- `10-roles/Technical-Advisor.md` should align with decision-making, quality standards, and production-readiness guidance

## People Dependencies

- `15-people/People-Index.md` links to individual person files when a private people layer exists
- `15-people/Team-Operating-Map.md` should inform planning, meeting prep, and communication choices when team-context notes are being maintained

## Skill Dependencies

- `20-skills/Skill-Authoring-Standard.md` defines the default structure and context-check pattern for portable skills
- `20-skills/Strategy/Decision-Memos.md` depends on `00-core/04-Decision-Making-Framework.md`
- `20-skills/Strategy/Strategy-Analysis.md` depends on `00-core/01-Operating-Principles.md` and `00-core/04-Decision-Making-Framework.md`
- `20-skills/Strategy/Project-Intake.md` should connect to project brief templates and decision-making standards
- `20-skills/Execution/Meeting-Prep.md` should pull from people or stakeholder files when relevant
- `20-skills/Technical/Code-Review.md` should align with quality-bar expectations

## Template Dependencies

- `30-templates/Decision-Memo-Template.md` should mirror `20-skills/Strategy/Decision-Memos.md`
- `30-templates/Project-Brief-Template.md` should mirror `20-skills/Strategy/Project-Intake.md`
- `30-templates/Meeting-Brief-Template.md` should mirror `20-skills/Execution/Meeting-Prep.md`
- `30-templates/Meeting-Note-Template.md` should mirror `40-systems/Project-Notes-Convention.md`
- `30-templates/Person-Profile-Template.md` should stay compatible with any collaborator or stakeholder profile format used in the local overlay

## System Dependencies

- `40-systems/Operating-Context-Model.md` defines how personal core, project overlays, and thin wrappers should work together
- the current-context layer defines the live strategic summary of what matters now
- `40-systems/Context-Window-Management.md` defines when context should be compacted, moved into files, or restarted in a new chat
- `40-systems/Review-and-Iteration-System.md` defines how repeated friction should become OS improvements
- `40-systems/Project-Notes-Convention.md` defines where durable project notes should live and how meeting capture should move from tools like Granola into project files

## Current-Context Layer

Use one of these patterns:

- `30-templates/Current-Context-Template.md` for a public-safe or shared current-context file
- `40-systems/Current-Priorities.md` for a private live-context file when more personal specificity is appropriate

The current-context layer should inform prioritization, seasonality, and tradeoff decisions without becoming a required dependency for the public core.
