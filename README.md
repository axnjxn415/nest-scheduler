# nest-scheduler

Self-hosted scheduler and control API for a Google Nest thermostat, built on Google's
[Smart Device Management (SDM) API](https://developers.google.com/nest/device-access).

The SDM API cannot read or write the thermostat's built-in weekly schedule, so this
service owns the schedule itself: a small always-on backend holds a table of
`(days, time, target temperature)` entries and pushes setpoint commands to the
thermostat at each transition.

- **Single user.** One household, one thermostat, one Google account. No multi-tenancy.
- **Self-hosted.** Runs on the owner's own server. No hosted service, no third-party
  backend, no analytics.
- **Reads and writes only this household's own thermostat**, using credentials the owner
  authorized for their own account.

Status: early. See [PRIVACY.md](PRIVACY.md) and [TERMS.md](TERMS.md).
