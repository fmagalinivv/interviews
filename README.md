# vVARDIS Technical Interviews

This repository contains practical, scenario-based technical interviews for
vVARDIS engineering and architecture roles. Each scenario provides enough
business and technical context for a candidate to study in advance, then asks
the candidate to deliver the complete scoped solution during the interview.

The interview evaluates how a candidate frames a problem, directs an AI coding
agent, validates the result, and explains trade-offs. It is not a typing-speed
exercise or a test of memorized syntax.

## Repository Contents

| Path | Purpose |
|---|---|
| `scenarios/` | Candidate-visible use cases and acceptance criteria |
| `templates/` | Reusable notes and handoff templates |
| `CANDIDATE.md` | Candidate preparation, session, and delivery guide |

Initial scenarios:

1. [R&D storage](scenarios/rnd-storage/README.md) — build a secure Azure
   foundation for high-volume laboratory data.
2. [EDI parent repository](scenarios/edi-parent-repository/README.md) — make a
   bounded change to an Azure-native EDI repository without breaking existing
   transaction flows.

## Candidate Preparation

Candidates receive the assigned scenario before the interview and may:

- read the scenario, repository documentation, and linked public material;
- install and verify one of the permitted coding agents;
- review the relevant Azure and language documentation.

Advance preparation is study and tool setup only. Candidates must not create
or save task-specific prompts, notes, snippets, code, tests, configuration,
diagrams, documentation, templates, or other solution content beforehand.
Every submitted artifact, and every task-specific prompt used to produce it,
must be created during the 30-minute live-development window.

## Standard Interview Structure

1. **Quick introduction — 5 minutes**
   - Introductions and role context.
   - Confirm the scenario, working repository, branch, and Azure sandbox.
   - Candidate states assumptions and intended first step.
2. **Live development — 30 minutes**
   - Candidate creates a branch from the supplied baseline.
   - Candidate may use only Codex, Claude Code, or GLM as the coding agent.
   - Candidate produces the complete scoped solution, runs all required checks,
     and adjusts the result while sharing their screen and reasoning.
3. **Walk-through — 10 minutes**
   - Demonstrate the result and available evidence.
   - Explain important decisions, limitations, and the next safe increment.

The interviewer may ask clarifying questions, but should not steer the
candidate toward a hidden implementation.

## Branching and Delivery

Create the interview branch at the start of the timed exercise:

```text
candidate/<candidate-id>/<scenario-id>/<yyyy-mm-dd>
```

Use an anonymized candidate identifier in shared or retained repositories.
Commit only source, tests, documentation, and safe configuration. Do not commit
credentials, tokens, private certificates, production data, or local AI-tool
state.

Each scenario declares its working repository. A scenario may use a starter
area in this repository or a sanitized, pinned copy of a parent repository.

## Azure Environment

vVARDIS provides a dedicated non-production Azure subscription or resource
group for the interview. The supplied scope is disposable and contains no
production data.

Candidates must:

- use only the supplied identity and Azure scope;
- verify the active tenant and subscription before deployment;
- prefer repeatable infrastructure as code;
- avoid tenant-wide or subscription-wide changes unless the scenario requires
  them explicitly;
- remove or document any billable resources created during the exercise.

## What Is Assessed

- problem framing and prioritization;
- effective, transparent use of the coding agent;
- correctness and maintainability of the implementation;
- security and operational judgement;
- validation through tests, tooling, or deployment evidence;
- ability to explain trade-offs and production considerations outside the
  completed interview scope.

The amount of generated code is not a success measure.
