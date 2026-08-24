# Known Good Activity

## Purpose

This document records common authorised activity that may appear unusual during security monitoring or investigation.

It provides operational context but should not be used to automatically classify activity as benign.

Analysts should verify that observed activity matches the expected user, system, time and purpose.

---

## Routine IT Activity

Normal IT administration may generate activity commonly associated with security alerts.

Examples include:

- PowerShell execution
- Remote administration
- Software installation
- Service creation or modification
- Administrative logons
- Account and group changes
- System restarts
- Network troubleshooting
- Endpoint security actions

The presence of these activities alone does not confirm malicious behaviour.

---

## Scheduled Maintenance

BluePeak performs planned maintenance to support patching, upgrades and infrastructure changes.

Maintenance may occur outside normal business hours to reduce disruption.

Typical maintenance activity may include:

- Windows updates
- Server restarts
- Software updates
- Network configuration changes
- Security tool updates
- Application maintenance

Approved maintenance should have a documented business or technical purpose.

Activity occurring during a maintenance period should still be verified against the expected systems, accounts and actions.

---

## Automated Activity

Some BluePeak systems perform legitimate automated actions without direct user interaction.

Examples may include:

- Scheduled tasks
- Integration processes
- Backup operations
- Security scans
- Software deployment
- System health checks

Service accounts may be used for authorised automated activity where required.

---

## Investigation Use

Known-good activity provides context, not proof.

An analyst should consider:

- Is the account expected to perform this activity?
- Is the affected system appropriate?
- Does the timing make sense?
- Does the activity match its expected purpose?
- Is there supporting operational or change information?

Activity that does not match the expected context should be investigated further.

---

## Maintenance Records

Specific maintenance windows and approved changes are recorded when required rather than permanently defining all maintenance as trusted activity.

This allows BluePeak to distinguish expected operational activity from suspicious behaviour occurring at a convenient time.