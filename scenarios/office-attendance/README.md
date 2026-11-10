# Scenario: Office Attendance

## Candidate Brief

An international company wants a governed data product for analysing patterns
of office attendance. The available source information consists of Microsoft
Entra directory users, sign-in activity, mailbox time zones, named network
locations and office buildings.

The supplied fixture data is synthetic and was generated from anonymised
production-level distributions. It contains no production identities,
addresses, network ranges or event timestamps.

Source deliveries may contain repeated events, incomplete records, unresolved
users, ambiguous locations, failed sign-ins and timestamps affected by
daylight-saving transitions.

The resulting data product must allow attendance activity to be analysed by
person, time, location, source and sign-in characteristics while retaining
sufficient evidence to explain its results.

## Architecture Requirements

The solution must:

- follow a Bronze, Silver and Gold medallion architecture;
- use Open Data Contract Standard data contracts as the authoritative
  declaration of every persisted dataset;
- declare schemas, keys, relationships, grains and data-quality requirements;
- preserve source lineage and support repeatable processing;
- make invalid or unresolved data observable; and
- separate collected source evidence from business-facing attendance results.

No contract templates or predefined target schemas are supplied. Contract
design, dataset boundaries and processing decisions are part of the exercise.

## Timed Task

During the 45-minute live-development window, create the complete scoped
solution that:

1. processes the supplied fixture data;
2. defines the necessary ODCS contracts;
3. implements the medallion processing flow;
4. provides repeatable validation or automated tests; and
5. documents the completed solution in `SOLUTION.md`.

All implementation, contracts, tests, documentation and task-specific prompts
must be created during the timed session.

## Working Repository

Use this repository and keep the implementation under this scenario directory.
The interviewer supplies the pinned baseline commit. Create the candidate
branch at the start of the timed session.

## Constraints

- Use only the supplied synthetic fixtures.
- Do not connect to Microsoft Graph, Databricks or any production system.
- Do not introduce another schema or contract format beside ODCS.
- Do not modify the intended meaning of the source evidence.
- Keep every submitted artifact under this scenario directory.

## Acceptance Criteria

- The solution has identifiable Bronze, Silver and Gold boundaries.
- Every persisted dataset has an ODCS contract.
- The contracts declare the dataset schemas, grains, keys, relationships and
  data-quality requirements.
- Reprocessing the same source delivery produces a deterministic result.
- Source lineage remains available in the resulting data product.
- Invalid or unresolved source information remains observable.
- The supplied fixtures exercise the completed processing flow.
- At least one useful validation check or automated test runs successfully.
- `SOLUTION.md` explains the architecture, contracts, assumptions, setup,
  execution, validation evidence, limitations and production considerations.

## Discussion Prompts

Be ready to explain:

- how the contracts govern the implemented datasets;
- where each medallion boundary is drawn and why;
- how repeated, incomplete or ambiguous source information is represented;
- what evidence supports the business-facing attendance result;
- how the solution would change for incremental production processing; and
- what additional security, privacy and operational controls production would
  require.

## Fixture Data

The `fixtures/` directory contains production-derived synthetic records for
the source domains described above. The fixture generation deliberately
removes all production identifiers and values while retaining representative
data shapes and quality conditions.
