# Interview Scenarios

Each scenario is independent and must define:

- the candidate-visible context and task;
- the working repository and pinned baseline;
- the safe Azure scope, when applicable;
- functional and non-functional acceptance criteria;
- fixtures or starter assets required for a fair 30-minute exercise.

Scenario documentation must use synthetic data and must not expose production
configuration, customer payloads, secrets, or private certificates.

| Scenario | Primary capability |
|---|---|
| [R&D storage](rnd-storage/README.md) | Azure storage, data integrity, infrastructure as code |
| [EDI parent repository](edi-parent-repository/README.md) | Repository discovery, integration change, regression safety |
