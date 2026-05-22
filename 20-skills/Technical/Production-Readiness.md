# Production Readiness

Use this skill to evaluate whether software is ready to move forward to the next stage of use or release.

## Purpose

This skill helps prevent false confidence, insecure shortcuts, weak validation, and premature shipping. It is designed for a non-technical PM using AI to build software, and it should favor honest readiness judgment over optimistic momentum.

Related files:
- `../../00-core/03-Work-Standards-and-Quality-Bar.md`
- `../../00-core/04-Decision-Making-Framework.md`
- `../../10-roles/Technical-Advisor.md`

## Context Check

Before using this skill:

- Identify the project and current release stage
- Confirm whether the target stage is `Prototype`, `v0`, or `v1`
- Identify the intended users and risk surface
- Identify whether real data, auth, payments, or sensitive actions are involved
- Review the source-of-truth project files and any active project `AGENTS.md`
- If key context is missing, ask one targeted question with likely options, brief tradeoffs, and a recommended default, or state assumptions explicitly when reasonable

## Core Rule

Do not use one universal readiness bar.

Readiness must be evaluated against the stage:

- `Prototype`
- `v0`
- `v1`

The goal is to apply the right rigor at the right time:

- do not overbuild too early
- do not under-protect too late
- never confuse momentum with readiness

## Universal Checks

At every stage, confirm:

- the software basically works for the intended use
- obvious security disasters are not present
- secrets are handled safely
- important assumptions and shortcuts are explicit
- the current stage is labeled honestly
- what has and has not been validated is clearly stated

## Prototype Gate

### Goal

Demonstrate the intended concept safely enough for limited demo, testing, or exploration.

### Absolute Blockers

- exposed secrets or unsafe secrets handling
- obviously unsafe auth or permission assumptions where user or data boundaries exist
- misleading claims about what has been validated
- use of real sensitive data without proper protection
- dependencies or integrations with obvious security or legal risk
- code or architecture so chaotic that it teaches the wrong lesson or makes the next step much harder

### Acceptable Shortcuts

- minimal tests if core behavior is manually checked
- rough UI
- manual workflows if documented
- limited logging and monitoring
- hardcoded non-sensitive demo data
- incomplete error handling outside core flows
- no scalability work yet
- partial documentation if assumptions and shortcuts are written down

### Standard

A prototype is good enough when it:

- demonstrates the intended thing
- is safe enough for its limited use
- makes shortcuts explicit
- can still be evolved or discarded cleanly

## v0 Gate

### Goal

Be safe enough for limited real use while providing enough foundation that a future engineer can understand it and not consider it reckless or opaque.

### Absolute Blockers

- no auth or broken permissions where auth matters
- unsafe secrets handling
- no testing or validation on critical paths
- meaningful data integrity risk
- undocumented prototype shortcuts still embedded in important flows
- no clear deploy process
- no rollback or recovery plan
- no logging on key flows
- confusing code with no explanation of structure, assumptions, or shortcuts
- known major dependency or security risk

### Can Still Be Imperfect

- UI polish
- broad test coverage outside critical flows
- advanced monitoring
- scalability beyond expected early usage
- architecture elegance
- some manual operational steps, if documented

### Standard

`v0` should be:

- safe enough
- understandable enough
- recoverable enough
- validated enough on what matters most

## v1 Gate

### Goal

Be ready for broader real use with serious confidence.

### Non-Negotiables

- strong testing of critical paths
- confidence in auth and permissions where relevant
- secrets and environment configuration handled correctly
- logging and monitoring on key flows
- a credible rollback or recovery path
- no major known security issues
- clear handling of important edge cases
- documentation that a future engineer can use to understand and operate the system
- clear deploy and operational ownership
- dependency review for major risks
- privacy, compliance, or data-handling review where relevant

### Can Still Be Imperfect

- elegance in every corner of the codebase
- full automation of every operational step
- optimization for scale you do not yet have
- exhaustive test coverage on low-risk paths

### Standard

`v1` should be:

- ready for broader real-world use
- understandable and operable
- not dependent on luck or mystery
- strong enough that failures are containable

## Readiness Categories

When evaluating readiness, check:

- correctness
- security
- secrets handling
- auth and permissions
- testing and validation
- data integrity
- logging and observability
- deployment and rollback
- dependencies
- documentation and handoff quality
- privacy or compliance where relevant
- edge cases on important flows

## Readiness Communication Rules

When reporting readiness, always:

- explicitly label the current stage
- say what was checked
- say what was not checked
- separate `blockers` from `concerns`
- give a `ship / don't ship / ship with caution` recommendation
- assign a confidence level
- identify the next best risk-reduction step
- never say `production-ready` without naming the basis for that claim

## Output Structure

1. Target stage
2. Readiness recommendation
3. Confidence level
4. What was checked
5. What was not checked
6. Blockers
7. Concerns
8. Recommended next steps

## Common Failure Modes

- applying a production bar to a prototype
- treating a prototype bar as enough for real users
- calling something ready without naming what was validated
- ignoring secrets, auth, or rollback because the product is early
- confusing code that works once with software that is safe to ship
- letting AI confidence replace technical judgment
