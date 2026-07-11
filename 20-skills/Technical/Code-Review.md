# Code Review

Use this skill to review code changes with a bias toward finding bugs, regressions, hidden risk, and missing validation.

## Purpose

This skill helps evaluate code for correctness, maintainability, behavior changes, and test coverage rather than providing shallow approval.

Related files:
- `../../00-core/03-Work-Standards-and-Quality-Bar.md`
- `../../00-core/04-Decision-Making-Framework.md`
- `Spec-Writing.md`

## Context Check

Before using this skill:

- Identify the project, repository, or subsystem under review
- Confirm the intended change and the surrounding context
- Review any relevant spec, ticket, or acceptance criteria
- Check whether assumptions are coming from another codebase or architecture
- If key context is missing, ask one targeted question with likely options, brief tradeoffs, and a recommended default, or state assumptions explicitly when reasonable

## When To Use

- Reviewing a pull request or patch
- Evaluating implementation against a spec
- Looking for regressions before merge or release

## Core Principles

- Prioritize correctness and risk over style nits
- Review behavior, not just syntax
- Consider edge cases and failure modes
- Check whether tests prove the important paths
- Be specific about why something is risky

## Workflow

## 1. Understand The Intended Change

Clarify:

- What problem the code is solving
- What behavior is supposed to change
- What should remain unchanged

## 2. Review The Implementation

Look for:

- Correctness bugs
- Regressions
- Fragile logic
- Missing validation
- State or data integrity problems
- Error handling gaps

## 3. Review Testing

Check:

- Whether tests exist
- Whether they cover the important paths
- Whether edge cases and failure modes are exercised

## Output Structure

1. Findings ordered by severity
2. Risks or open questions
3. Brief change summary only if useful

## Quality Bar

A strong code review:

- Finds the highest-risk issues first
- Ties findings to user or system behavior
- Explains why a problem matters
- Notes missing tests when relevant

## Common Failure Modes

- Focusing on formatting over behavior
- Approving code without understanding the intended change
- Missing edge cases
- Treating untested code as safe by default
