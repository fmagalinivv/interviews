# AGENTS.md

## Scope

- Applies to the whole repository.
- This is an interview repository containing multiple independent scenarios.
- Work only in the scenario assigned by the interviewer unless shared files
  must be changed to make that scenario work.

## Candidate and Agent Rules

- Permitted coding agents are Codex, Claude Code, and GLM only.
- Keep the candidate in control: state assumptions, show important prompts,
  inspect generated changes, and verify the result.
- Do not use a prepared solution, copy another candidate's branch, or read
  interviewer-private material.
- Do not modify scenario requirements, acceptance criteria, or evaluation
  guidance to make an implementation pass.
- Prefer a small working vertical slice over broad unfinished scaffolding.
- Record material assumptions and incomplete work in the scenario handoff.

## Security Rules

- Use only the vVARDIS-provided non-production Azure scope.
- Confirm the Azure tenant and subscription before any deployment.
- Never access or mutate production systems.
- Never commit secrets, tokens, credentials, private certificates, customer
  payloads, health data, or local AI-tool state.
- Use synthetic fixtures and anonymized candidate identifiers.
- Prefer managed identities, RBAC, and infrastructure as code over shared
  credentials and manual configuration.

## Repository Rules

- Branch from the interviewer-supplied baseline at the start of the timed
  session.
- Keep changes inside the assigned scenario or declared working repository.
- Preserve existing tests and contracts unless the scenario explicitly changes
  them.
- Include concise run, test, and deployment instructions.
- Do not commit generated build output or temporary deployment files.
