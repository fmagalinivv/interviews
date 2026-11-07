# Candidate Guide

## Purpose

This is an open-book, scenario-based technical interview. The goal is to show
how you understand an unfamiliar problem, direct an AI coding agent, validate
its work, and explain engineering trade-offs.

The interview is not a typing-speed test and you are not expected to complete
an entire production platform. The assigned scenario is intentionally scoped
so that its complete solution and acceptance criteria can be delivered in 30
minutes with a coding agent.

## Before the Interview

You may:

- read the assigned scenario and repository documentation;
- review relevant Azure and language documentation;
- install and verify Codex, Claude Code, or GLM.

Advance preparation is limited to study and tool setup. Do not create or save
task-specific prompts, notes, snippets, code, tests, configuration, diagrams,
documentation, templates, or other solution content before the interview. Do
not paste task-specific content prepared by another person or system.

All submitted content and every task-specific prompt used to produce it must
be created during the 30-minute live-development window.

## Session Structure

1. **Quick introduction — 5 minutes**
   - Confirm the scenario, working repository, baseline, and Azure sandbox.
   - State your assumptions and intended first step.
2. **Live development — 30 minutes**
   - Create your candidate branch.
   - Produce the complete scoped solution and satisfy all acceptance criteria.
   - Test and adjust the solution while sharing your reasoning.
   - Use only Codex, Claude Code, or GLM as the coding agent.
3. **Walk-through — 10 minutes**
   - Demonstrate the result and validation evidence.
   - Explain decisions, limitations, and the next safe increment.

## Branching

Create the branch at the start of the timed session:

```text
candidate/<candidate-id>/<scenario-id>/<yyyy-mm-dd>
```

Use the anonymized candidate identifier provided for the interview. Do not use
another candidate's branch or a prepared solution.

## Working With the Coding Agent

- State important requirements and constraints explicitly.
- Compose all task-specific prompts during the timed session.
- Inspect generated changes instead of accepting them blindly.
- Run focused checks and interpret failures before asking for more changes.
- Keep control of scope and be ready to explain what the agent produced.
- Record any important correction or constraint in the handoff.

## Azure Safety

vVARDIS provides a disposable non-production Azure subscription or resource
group when the scenario requires it.

- Confirm the active tenant and subscription before deployment.
- Use only the supplied identity and scope.
- Never access or modify production systems.
- Prefer infrastructure as code, managed identities, and least-privilege RBAC.
- Do not commit credentials, tokens, private certificates, customer payloads,
  health data, or local AI-tool state.
- Use synthetic fixtures only.
- Remove or document billable resources created during the exercise.

## Delivery Checklist

- The implementation is confined to the assigned scenario or working
  repository.
- Existing tests and contracts are preserved unless the task changes them.
- Every scenario acceptance criterion is satisfied.
- The most relevant validation command has been run.
- Run, test, and deployment instructions are concise and reproducible.
- `templates/handoff.md` is completed in the candidate branch.
- Production considerations outside the completed interview scope are
  documented.
