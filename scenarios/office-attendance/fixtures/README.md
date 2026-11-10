# Office Attendance Fixtures

These fixtures are operationally derived synthetic data for the interview
scenario. They must contain no source names, email addresses, identifiers, IP
addresses, network ranges, office names, coordinates or event timestamps.

The fixture set is generated from aggregate operational characteristics and
then reviewed before publication. Values that could identify a person,
location, tenant, application or network are replaced with newly generated
scenario values. IP addresses use documentation-only ranges and locations are
fictional.

Files:

| File | Source domain |
|---|---|
| `directory_users.csv` | Microsoft Entra directory users |
| `mailbox_timezones.csv` | Mailbox time-zone settings |
| `named_locations.csv` | Named network locations and IP ranges |
| `buildings.csv` | Office buildings |
| `signin_events.csv` | Sign-in event deliveries |

See `PROVENANCE.md` for the derivation and disclosure controls applied to the
fixture set.
