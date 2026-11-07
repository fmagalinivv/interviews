# Interviewer Guide

## Before the Interview

1. Select one scenario and send its candidate-visible files in advance.
2. Pin the baseline commit and verify the starter state from a clean clone.
3. Prepare an anonymized candidate identifier and repository access.
4. Provide a disposable Azure subscription or resource group when required.
5. Verify that the candidate can authenticate, but do not provide production
   access or reusable credentials.

Preparation is open-book. Candidates may prepare notes and prompts, but the
implementation used for assessment must start on the interview branch during
the timed session.

## During the Interview

Use the structure in the root README:

- 5 minutes: introduction, environment check, assumptions;
- 30 minutes: live implementation;
- 10 minutes: demonstration and review.

The candidate may use Codex, Claude Code, or GLM. They should remain able to
explain what the agent changed and how the result was validated.

Do not penalize a candidate for deliberately reducing scope when they explain
the trade-off and complete a coherent vertical slice.

## Evaluation

Score each dimension from 1 to 4 and record evidence rather than impressions.

| Dimension | Evidence to look for |
|---|---|
| Problem framing | Identifies the critical path, risks, and assumptions |
| Agent use | Gives useful constraints, reviews output, corrects mistakes |
| Implementation | Produces a coherent, maintainable vertical slice |
| Security | Uses safe identity, data, network, and secret-handling patterns |
| Validation | Runs meaningful checks and interprets failures correctly |
| Communication | Explains decisions, limitations, and next steps clearly |

Do not score candidates on prompt style, typing speed, or the volume of code.

## Closeout

- Ask the candidate to complete `templates/handoff.md` in their branch.
- Record the baseline commit, candidate branch, tool used, and Azure scope.
- Revoke temporary access and clean up billable resources.
- Retain or delete the branch according to the recruiting data-retention rule.
