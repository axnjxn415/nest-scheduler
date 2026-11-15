# Privacy Policy

_Last updated: 15 November 2026_

`nest-scheduler` is a personal, self-hosted application operated by its owner for their
own household. It is not a commercial service and has no users other than its operator.

## Who operates this application

The individual who deploys it on their own hardware. There is no company, no hosted
service, and no third-party operator.

## What data is accessed

With the operator's explicit Google OAuth consent, the application accesses data from the
operator's **own** Google Nest thermostat through Google's Smart Device Management API:

- Thermostat identity and connectivity status
- Ambient temperature and humidity measured at the thermostat
- HVAC operating state (heating / cooling / off), mode, and Eco state
- Target temperature setpoints

It also writes to that same thermostat: target temperature, HVAC mode, Eco mode, and fan
timer commands.

The application accesses **no other Google data**. It requests a single OAuth scope,
`https://www.googleapis.com/auth/sdm.service`, and no others. It does not access email,
contacts, calendar, files, cameras, or any other device or service.

## Where data is stored

Entirely on the operator's own server. Specifically:

- A local database file containing the schedule the operator created, and a log of
  commands sent to the thermostat and their results.
- OAuth credentials (client secret and refresh token), held in server-side configuration
  readable only by the operating system account that runs the service.

No data is transmitted anywhere except to Google's own API endpoints in order to read and
control the operator's thermostat.

## What data is shared

None. Data is not sold, rented, shared, published, or transmitted to any third party.
There are no advertising, analytics, tracking, or telemetry components.

## Retention and deletion

Schedule entries and the command log persist until the operator deletes them or deletes
the database file. Deleting the deployment deletes all stored data. Authorization can be
revoked at any time by the operator at
[myaccount.google.com/permissions](https://myaccount.google.com/permissions), which
immediately and permanently ends the application's access to Google data.

## Google API Services User Data Policy

Use of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements. Google user data is used solely to provide the
thermostat scheduling and control features described above, and for no other purpose.

## Children

The application is not directed to children and collects no information about them.

## Changes

Changes to this policy will be committed to this repository, where the revision history
is publicly visible.

## Contact

Via an issue on this repository.
