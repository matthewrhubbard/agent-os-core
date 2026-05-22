# Production Readiness Checklist

Use this checklist to evaluate whether a software project is ready to move to the next stage.

This checklist is designed to work with:

- `../20-skills/Technical/Production-Readiness.md`
- `../10-roles/Technical-Advisor.md`

## How To Use

1. Identify the target stage: `Prototype`, `v0`, or `v1`
2. Complete the universal checks
3. Complete the section for the target stage
4. Mark each item with:
   - `Pass`
   - `Concern`
   - `Fail`
   - `N/A`
5. For each item, add:
   - a short note
   - whether it is a blocker: `Yes` or `No`
6. End with an overall recommendation, confidence level, and next risk-reduction step

## Template

```md
# Production Readiness Review

## Project

- Project:
- Reviewer:
- Date:
- Target stage: `Prototype` / `v0` / `v1`

## Status Key

- `Pass`
- `Concern`
- `Fail`
- `N/A`

## Universal Checks

| Item | Status | Notes | Blocker? |
|---|---|---|---|
| Intended use is clearly defined |  |  |  |
| Current stage is explicitly labeled |  |  |  |
| What has been validated is clearly stated |  |  |  |
| What has not been validated is clearly stated |  |  |  |
| No obvious security disaster is present |  |  |  |
| Secrets are handled safely |  |  |  |
| Important shortcuts and assumptions are documented |  |  |  |

## Prototype Checks

Fill this section only if the target stage is `Prototype`.

| Item | Status | Notes | Blocker? |
|---|---|---|---|
| The prototype demonstrates the intended concept |  |  |  |
| Any user/data boundary is handled safely enough for the intended use |  |  |  |
| No real sensitive data is exposed or mishandled |  |  |  |
| Manual validation has been done on the core flow |  |  |  |
| Hardcoded data, manual steps, or rough edges are documented |  |  |  |
| The architecture is simple enough to evolve or discard cleanly |  |  |  |
| The prototype does not create false confidence about readiness |  |  |  |

## v0 Checks

Fill this section only if the target stage is `v0`.

| Item | Status | Notes | Blocker? |
|---|---|---|---|
| Core flows work correctly for limited real use |  |  |  |
| Auth and permissions work correctly where relevant |  |  |  |
| Critical-path validation or testing exists |  |  |  |
| Data integrity risks are understood and acceptable |  |  |  |
| Prototype shortcuts in important flows are documented or removed |  |  |  |
| Key flows have basic logging |  |  |  |
| There is a clear deploy process |  |  |  |
| There is a rollback or recovery path |  |  |  |
| Code structure, assumptions, and shortcuts are understandable to a future engineer |  |  |  |
| No major known dependency or security risk remains unaddressed |  |  |  |

## v1 Checks

Fill this section only if the target stage is `v1`.

| Item | Status | Notes | Blocker? |
|---|---|---|---|
| Critical paths have strong testing coverage |  |  |  |
| Auth and permissions have been reviewed with confidence |  |  |  |
| Secrets and environment configuration are handled correctly |  |  |  |
| Key flows have logging and monitoring |  |  |  |
| Rollback or recovery path is credible and understood |  |  |  |
| Important edge cases are handled |  |  |  |
| Documentation is sufficient for a future engineer to understand and operate the system |  |  |  |
| Deployment and operational ownership are clear |  |  |  |
| Dependencies have been reviewed for major risk |  |  |  |
| Privacy, compliance, and data-handling concerns have been reviewed where relevant |  |  |  |
| No major known security issue remains |  |  |  |

## Overall Recommendation

- Recommendation: `Ship` / `Don't Ship` / `Ship With Caution`
- Confidence: `High` / `Medium` / `Low`

## Blockers

- 

## Concerns

- 

## What Was Checked

- 

## What Was Not Checked

- 

## Next Risk-Reduction Step

- 
```

## Final Check

A strong completed review should:

- clearly identify the target stage
- distinguish blockers from concerns
- say what was and was not checked
- avoid claiming readiness without evidence
- make the next risk-reduction step obvious
