# Scenario: EDI Parent Repository Change

## Candidate Brief

vVARDIS operates an Azure-native EDI platform using API Management, Logic Apps
Standard, an Integration Account, Service Bus, and repository-managed
infrastructure. The platform supports multiple partners and X12 transaction
types. A change must preserve existing partner flows, control-number handling,
archiving, and promotion checks.

The interview assesses whether a candidate can understand an unfamiliar parent
repository, make a bounded integration change, and protect existing contracts
while using an AI coding agent.

## Working Repository

The interviewer provides a sanitized, pinned interview copy of the
`integration-edi` parent repository. The copy contains synthetic fixtures only
and no partner secrets, certificates, identifiers, or customer payloads.

Create the candidate branch in that repository at the start of the timed
session. Do not change live Azure resources or any production repository.

## Timed Task

The interviewer selects one bounded change already represented by synthetic
fixtures, for example:

- add routing for one new inbound X12 transaction type;
- add a partner-specific validation rule without changing shared behavior;
- correct an archive or acknowledgement regression and add a test; or
- add a deployable workflow from an existing non-deployable placeholder.

The concrete change request and expected fixture are revealed at the start of
the timed session. The repository and general architecture are available for
advance preparation.

Within 30 minutes, the candidate should:

1. identify the relevant repository path and existing pattern;
2. implement the smallest safe change;
3. add or update an automated regression check; and
4. run the most relevant local validation available in the repository.

## Acceptance Criteria

- Existing transaction types and partner routes remain unchanged unless the
  task explicitly modifies them.
- The implementation follows the repository's established workflow,
  infrastructure, and naming patterns.
- Synthetic EDI fixtures are used; no real customer payload is introduced.
- Control numbers, correlation identifiers, and archive behavior are preserved
  or explicitly tested where relevant.
- Failure behavior is visible and does not silently acknowledge an invalid
  document as successful.
- At least one focused regression check passes.
- The handoff identifies deployment, certificate, partner-agreement, and
  rollback considerations outside the timed slice.

## Discussion Prompts

Be ready to explain:

- where partner-specific behavior should end and shared behavior should begin;
- how idempotency and duplicate delivery should be handled;
- when to send X12 or AS2 acknowledgements and what not to acknowledge;
- how to promote the change through dev, staging, and production safely;
- which evidence would be required before enabling a real partner flow.

## Interviewer Setup Note

Keep the hidden task small enough for one vertical slice. The exercise must not
depend on undisclosed domain trivia. Supply the synthetic fixture, expected
outcome, and one failing or missing test at the start of the timed session.
