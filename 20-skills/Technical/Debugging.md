# Debugging

Use this skill to investigate a bug or failure systematically and converge on the most likely cause before making changes.

## Purpose

This skill helps avoid random trial-and-error by turning debugging into a disciplined process of observation, hypothesis, testing, and narrowing.

Related files:
- `../../00-core/01-Operating-Principles.md`
- `../../00-core/04-Decision-Making-Framework.md`
- `Spec-Writing.md`

## Context Check

Before using this skill:

- Identify the project, system, or workflow where the issue appears
- Confirm the expected behavior and the observed behavior
- Identify recent changes, environment details, and reproduction steps
- Check whether the issue may belong to a different layer than first assumed
- If key context is missing, ask one targeted question with likely options, brief tradeoffs, and a recommended default, or state assumptions explicitly when reasonable

## When To Use

- A feature behaves incorrectly
- A system fails intermittently
- A workflow breaks after recent changes
- The cause of a problem is unclear

## Core Principles

- Reproduce before fixing
- Narrow the problem before changing code
- Prefer evidence over intuition alone
- Change one thing at a time when isolating causes
- Distinguish symptom from root cause

## Workflow

## 1. Define The Failure Clearly

Capture:

- Expected behavior
- Actual behavior
- Reproduction steps
- Scope and frequency

## 2. Gather Evidence

Review:

- Logs
- Error messages
- Inputs and outputs
- Recent changes
- Environment differences

## 3. Form Hypotheses

List plausible explanations, then rank them by fit to the evidence.

## 4. Test Narrowly

Run targeted checks that eliminate or confirm hypotheses efficiently.

## 5. Fix And Verify

Once the likely root cause is found:

- Apply the smallest sound fix
- Verify the problem is resolved
- Check for related regressions

## Output Structure

1. Problem statement
2. Reproduction details
3. Evidence gathered
4. Leading hypotheses
5. Most likely root cause
6. Recommended fix
7. Verification plan

## Quality Bar

A good debugging process:

- Produces a clear problem statement
- Narrows the search space deliberately
- Grounds conclusions in evidence
- Verifies the fix rather than assuming it worked

## Common Failure Modes

- Fixing before reproducing
- Changing several things at once
- Confusing correlation with cause
- Stopping after the symptom disappears once
