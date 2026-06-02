# Spec Writing

Use this skill to write a spec that aligns people around the problem, proposed solution, constraints, and acceptance criteria.

## Purpose

This skill helps produce specs that are useful for decision-making and implementation rather than vague background documents.

Related files:
- `../../00-core/03-Work-Standards-and-Quality-Bar.md`
- `../../00-core/04-Decision-Making-Framework.md`
- `../Strategy/Project-Intake.md`

## Context Check

Before using this skill:

- Identify the project, audience, and implementation context
- Confirm whether the spec is for product, technical implementation, or both
- Review existing project context, decisions, and constraints
- Check whether the document is net-new or revising an existing spec
- Check whether the implementation scope is too large for one useful increment
- If key context is missing, ask one targeted question with likely options, brief tradeoffs, and a recommended default, or state assumptions explicitly when reasonable

## When To Use

- Defining a feature or initiative before implementation
- Aligning stakeholders around scope and behavior
- Creating acceptance criteria or implementation guidance

## Core Principles

- Name the problem clearly
- Be explicit about scope and non-goals
- Make important decisions visible
- Define acceptance criteria that are testable
- Write for the people who need to act on the spec
- Right-size implementation plans before treating them as ready to build

## Workflow

## 1. Frame The Problem

Clarify:

- What problem is being solved
- Who it affects
- Why it matters now

## 2. Define The Solution

Describe:

- The proposed approach
- Key behaviors or requirements
- Important constraints
- Alternatives considered if relevant

## 3. Clarify Scope

State:

- What is included
- What is excluded
- Dependencies and open questions

## 4. Right-Size The Work

Before finalizing an implementation plan, check whether it spans multiple outcomes, multiple subsystems, unclear acceptance criteria, or more than one focused work session.

If the work is too large, recommend a smaller sequence that includes:

- Why the current plan is too large
- The recommended first increment
- The follow-on increments in order
- What each increment should prove or unlock

Default to suggesting the split, not rewriting plans or creating Linear issues automatically unless the user approves.

For Linear stories, keep the split in plain language, requirement-oriented, and free of starter code.

## 5. Define Acceptance Criteria

Write criteria that are concrete enough to validate after implementation.

## Output Structure

1. Problem
2. Context and goal
3. Proposed solution
4. Scope and non-goals
5. Constraints and dependencies
6. Recommended increments, when splitting is warranted
7. Acceptance criteria
8. Open questions or risks

## Quality Bar

A good spec:

- Is clear enough for implementation and review
- Resolves important ambiguity
- Defines what done means
- Identifies when the implementation should be split into smaller increments
- Surfaces open questions instead of hiding them

## Common Failure Modes

- Writing background instead of a spec
- Leaving scope implicit
- Omitting acceptance criteria
- Treating oversized implementation work as one buildable unit
- Describing a solution without the underlying problem
