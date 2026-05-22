# Context Window Management

This file defines how to preserve context quality, reduce token waste, and decide when to compact, summarize, document, or start a new chat.

## Purpose

The goal is not to maximize thread length. The goal is to maintain high-quality context, strong reasoning, and efficient use of tokens.

Default principle:

- preserve the context that still matters
- drop the context that no longer helps
- move durable knowledge into files
- use fresh chats when the current thread becomes cluttered or drifts from the work

## Core Rule

Do not assume that longer threads are better threads.

As chats grow, they often accumulate:

- stale assumptions
- abandoned ideas
- repeated explanations
- wrong level of detail
- mixed work modes
- irrelevant emotional or exploratory residue

When this happens, context quality falls even if raw context quantity rises.

## Warning Signs

The thread may be degrading when:

- the AI repeats itself
- responses get longer but less precise
- stale context starts leaking into answers
- abandoned ideas keep resurfacing
- the AI confuses earlier exploratory thinking with current decisions
- too many unrelated subtopics are mixed together
- the current work has shifted from strategy to execution, or from one project to another
- the thread contains many dead paths that are no longer relevant

## When To Compact

Compact the working context when:

- a major decision has been made
- a long brainstorm has narrowed into a clearer direction
- the conversation is about to switch modes
- too much dead context has accumulated
- the AI is beginning to respond with excess length or drift

Compaction should preserve:

- the current objective
- decisions made
- active constraints
- open risks
- next steps
- source-of-truth files

## When To Summarize Into A File

Move information into a durable file when:

- it is likely to be reused
- it defines priorities, decisions, or requirements
- it should become source-of-truth
- the chat has produced a stable artifact
- the same context would otherwise need to be restated repeatedly

Common destinations:

- core files
- role files
- skills
- templates
- project `AGENTS.md`
- project docs

## When To Start A New Chat

Start a new chat when:

- switching to a different project
- switching to a substantially different workstream
- the current thread has become cluttered
- the work now depends more on durable files than on conversational history
- you want to test whether the docs and wrappers are sufficient on their own
- the thread contains too much exploratory residue to be worth cleaning manually

New chats are especially useful when:

- moving from Agent OS design into project implementation
- moving from strategy into coding
- moving from one repo to another
- moving from broad research into a focused execution task

## What To Preserve

When compacting or restarting, preserve:

- the real question or objective
- the current priority stack
- decisions made
- important assumptions
- active risks
- next steps
- relevant source-of-truth files
- any explicit overrides or constraints

## What To Drop

When compacting or restarting, usually drop:

- abandoned ideas
- repeated explanations
- superseded drafts
- stale assumptions
- side trails that are no longer relevant
- excessive intermediate reasoning that has already been distilled into a better artifact

## Durable Context Rule

Use files for durable context.

Prefer:

- personal OS files for stable personal rules
- project files for project-specific truth
- templates for repeatable artifacts
- inbox or change files for proposed system improvements

Do not rely on chat history as the long-term memory layer when a file would be better.

## Practical Workflow

When a thread starts getting heavy:

1. Ask what still matters in this thread.
2. Distill the useful context.
3. Move durable information into the right file.
4. Drop dead context.
5. Continue in the same thread only if the remaining context is still coherent.
6. Start a new chat if a cleaner entrypoint would improve quality.

## Chief Of Staff Rule

The Chief of Staff should protect context quality the same way it protects time and attention.

That includes:

- noticing when a thread is bloated
- recommending compaction
- recommending a file summary
- recommending a fresh chat when the context has become inefficient

## Success Standard

This system is working when:

- answers stay sharp as work progresses
- threads do not become bloated by default
- durable knowledge moves into files instead of living only in chat memory
- new chats can pick up work quickly from the file system
- token usage supports the work instead of being consumed by preventable repetition
