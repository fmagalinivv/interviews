# Scenario: R&D Laboratory Storage

## Candidate Brief

vVARDIS R&D generates large MicroCT datasets on laboratory workstations. The
current process relies on local storage, direct transfers, SharePoint for some
collaboration, and an LTO tape process. Data volume is approximately 1.5–4 TB
per week. Raw and reconstructed datasets must remain distinguishable and their
integrity must be demonstrable.

vVARDIS wants a secure Azure-based foundation for controlled ingestion and
long-term retention. This is an interview use case, not authorization to change
the production architecture.

## Timed Task

During the 30-minute implementation window, create the complete scoped solution
that:

1. provisions or defines the core Azure storage resources through
   infrastructure as code;
2. protects the storage against anonymous access and accidental deletion;
3. submits one synthetic laboratory dataset and its metadata with a SHA-256
   integrity value; and
4. includes a repeatable validation command or automated test.

All implementation, tests, documentation, and task-specific prompts must be
created during the timed session. The solution must satisfy every acceptance
criterion below.

## Required Metadata

Use at least these fields in the synthetic submission:

| Field | Example |
|---|---|
| `project_id` | `100114` |
| `site` | `schlieren` |
| `instrument` | `microct-01` |
| `dataset_type` | `raw` or `reconstructed` |
| `run_id` | `run-2026-001` |
| `acquisition_date` | ISO-8601 date/time |
| `retention_class` | `15y-minimum` |
| `checksum_sha256` | SHA-256 digest of the submitted file |

All fixtures must be synthetic and small.

## Working Repository

Use this repository and keep the implementation under this scenario directory.
The interviewer supplies the pinned baseline commit. Create the candidate
branch at the start of the timed session.

## Azure Scope

vVARDIS supplies a disposable non-production Azure subscription or resource
group. The implementation must verify the selected subscription before any
deployment and must not use production data or credentials.

## Acceptance Criteria

- Infrastructure is repeatable and parameterized for the supplied Azure scope.
- Public or anonymous blob access is disabled.
- The design uses identity-based access; shared account keys are not embedded
  in source or instructions.
- Deletion protection and versioning or an equivalent recovery control are
  represented and explained.
- A synthetic file can be associated with the required metadata and checksum.
- At least one useful validation check runs locally or against the sandbox.
- The handoff explains retention/immutability, networking, monitoring, restore,
  and QMS considerations that remain outside the timed slice.

## Discussion Prompts

Be ready to explain:

- the difference between backup, archive, and immutable retention;
- how upload identity and least privilege should work;
- how a restore would be proven;
- what changes when datasets contain sensitive or regulated information;
- how the design would handle 1.5–4 TB of new data each week.
