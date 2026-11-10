# Fixture Provenance

The fixture set was generated on 2026-11-10 from aggregate characteristics of
the production Office Attendance datasets. Production was queried only for
counts, categorical distributions, null rates and approximate event-count
percentiles. No production row was exported or written to this repository.

The generated fixture preserves representative characteristics:

- named network locations and buildings are small reference datasets;
- mailbox time-zone coverage is incomplete relative to the directory;
- non-interactive sign-ins are more common than interactive sign-ins;
- activity outside named office networks is more common than office-network
  activity;
- both successful and failed sign-ins occur;
- repeated deliveries, unresolved identities, missing time zones, ambiguous
  network ranges and daylight-saving transitions are represented.

Disclosure controls:

- tenant, user, event, run, application, location and building identifiers are
  newly generated scenario identifiers;
- names and email addresses are fictional and use `example.invalid`;
- IP addresses come only from RFC 5737 documentation ranges;
- office names, addresses and coordinates are fictional;
- timestamps are newly selected scenario timestamps and are not shifted or
  transformed production timestamps;
- categorical combinations are constructed for the exercise rather than
  copied from individual production records.

The files are therefore production-derived synthetic fixtures, not
pseudonymised production rows.
