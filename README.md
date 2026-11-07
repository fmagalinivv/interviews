# vVARDIS Interviews

This repository contains practical, scenario-based interviews for
vVARDIS engineering and architecture roles. Each scenario provides enough
business and technical context for a candidate to study in advance, then asks
the candidate to deliver the complete scoped solution during the interview.

The interview evaluates how a candidate frames a problem, directs an AI coding
agent, validates the result, and explains trade-offs.

## Repository Contents

| Path | Purpose |
|---|---|
| `scenarios/` | Candidate-visible use cases and acceptance criteria |

Scenarios:

1. [R&D storage](scenarios/rnd-storage/README.md) — build a secure Azure
   foundation for high-volume laboratory data.

## Candidate Preparation

Candidates receive the assigned scenario before the interview and may:

- read the scenario, repository documentation, and linked public material;
- install and verify one of the permitted coding agents, required command line interfaces;

Advance preparation is study and tool setup only. Candidates must not create
or save task-specific prompts, notes, snippets, code, tests, configuration,
diagrams, documentation, templates, or other solution content beforehand.
Every submitted artifact, and every task-specific prompt used to produce it,
must be created during the 30-minute live-development window.

The submitted solution must include candidate-authored documentation covering
its architecture, assumptions, setup, deployment, execution, testing, security
decisions, validation evidence, and production considerations.

## Standard Interview Structure

1. **Quick introduction — 5 minutes**
   - Introductions and role context.
2. **Live development — 30 minutes**
   - Candidate creates a branch from the supplied baseline.
   - Candidate may use only Codex, Claude Code, or GLM as the agentic coding harnesses. No other tool is allowed.
   - Candidate produces the complete scoped solution, runs all required checks,
     and adjusts the result while sharing their screen and reasoning.
3. **Walk-through — 10 minutes**
   - Demonstrate the result and available evidence.
   - Explain important decisions, limitations, and the next safe increment.

## Branching and Delivery

Create the interview branch at the start of the timed exercise:

```text
candidate/<yyyy-mm-dd>
```

## Azure Environment

vVARDIS provides a dedicated non-production Azure subscription or resource
group for the interview. 

## What Is Assessed

- problem framing and prioritization;
- effective, transparent use of the coding agent;
- correctness and maintainability of the implementation;
- security and operational judgement;
- validation through tests, tooling, or deployment evidence;
- ability to explain trade-offs and production considerations
