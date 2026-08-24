# Service Accounts

## Purpose

This document records the primary non-user accounts used to support automated services within the BluePeak Logistics environment.

Service accounts are created only where required and should be limited to the systems and permissions necessary for their function.

---

## Service Account Inventory

| Account | Purpose | Expected System |
|---|---|---|
| svc_integration | Business application integration services | APP01 |
| svc_splunk | Splunk services and supporting processes | SPLUNK01 |
| svc_backup | Backup operations | Core server infrastructure |

Additional service accounts are documented when a genuine operational requirement is introduced.

---

## Expected Behaviour

Service accounts are intended for automated system activity rather than normal employee use.

Unless specifically required by the service, service accounts should not:

- Be used for interactive user logons
- Access unrelated workstations
- Perform unrelated administrative activity
- Be used for general IT administration

Activity outside the expected role of a service account should be investigated.

---

## Security

Service account permissions should follow the principle of least privilege.

Credentials should be protected and access limited to authorised systems and administrators.

Changes to service account permissions or usage should have a legitimate operational purpose.

---

## Investigation Use

Service accounts can generate legitimate activity that initially appears unusual.

During an investigation, analysts should compare observed activity against the documented purpose and expected systems for the account.

Unexpected authentication, privilege use or activity outside the account's normal role may indicate misconfiguration, credential misuse or compromise.