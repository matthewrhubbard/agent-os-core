# Project Notes Convention

This file defines the default way project notes should be stored so they are easy to find, useful in AI chats, and safe to back up.

## Purpose

The goal is to keep meeting knowledge close to the work:

- Capture with the best live tool
- Store the durable version in the project
- Back up the project notes without creating duplicate systems or syncing repo internals

## Default Rule

Use this stack by default:

- `Granola` for live capture and structured post-call generation
- Project-local Markdown for the durable note of record
- `Google Drive` for backup of the notes layer, not the entire repo root

Google Docs should not be the default live note-taking surface when Granola is being used for the same meeting. That creates competing sources of truth.

## Canonical Project Layout

Each active project should have a notes area with this minimum structure:

```text
<project>/
  notes/
    meetings/
      2026/
        2026-05-22-customer-discovery-acme.md
    decisions/
    research/
```

Use this as the default unless the project has a strong reason to override it.

## Folder Rules

- `notes/meetings/` is for call notes, interviews, working sessions, and stakeholder conversations
- `notes/decisions/` is for decision memos or final decision records that outgrow a meeting note
- `notes/research/` is for synthesized observations that combine multiple meetings or sources
- Group meeting notes by year once a project has more than a handful of calls

## File Naming Rules

Meeting note filenames should follow:

`YYYY-MM-DD-short-topic.md`

Examples:

- `2026-05-22-user-interview-jane-doe.md`
- `2026-05-22-partner-call-figma.md`
- `2026-05-22-internal-roadmap-review.md`

Names should describe the meeting in a way that still makes sense later without opening the file.

## Workflow

### Before The Call

- Open or create the meeting in Granola
- Use the meeting brief or agenda you already prepared
- If needed, paste a short agenda into Granola so the generated note follows the right structure

### During The Call

- Let Granola capture the conversation
- Add only the lightest manual notes when they materially improve the result
- Mark especially important decisions, names, or follow-ups if they may be easy to miss

### After The Call

- Regenerate or clean up the Granola note if needed
- Save one durable Markdown note into the project using `30-templates/Meeting-Note-Template.md`
- Link any relevant project files, specs, issues, or follow-up documents
- Promote important conclusions into `notes/decisions/` or another project artifact when warranted

## Source Of Truth Rules

- Granola is the capture system, not the final archive of record
- The project Markdown file is the durable source for future AI and coding work
- Google Drive is a backup layer, not the main editing surface
- If a Google Doc exists only because it used to be the note-taking habit, either retire it or turn it into a stable template, not a second live note store

## Backup Rules

- Back up the project `notes/` folder or another intentionally scoped export folder
- Do not back up entire Git repo roots to Google Drive for desktop by default
- Avoid syncing hidden repo internals such as `.git/`

## Quality Bar

A good project note system:

- Produces one clear note of record per important meeting
- Makes project context retrievable by agents without extra translation
- Separates raw capture from durable judgment
- Preserves enough metadata to be useful later
- Avoids duplicate systems that drift apart
