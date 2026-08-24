# Security Monitoring

## Purpose

This document provides an overview of the security telemetry collected by BluePeak Logistics to support threat detection, investigation and incident response.

BluePeak does not collect logs simply for the sake of collecting them. Monitoring is designed to provide the Security Operations team with the visibility required to detect, investigate and respond to threats affecting business operations.

---

# Monitoring Philosophy

BluePeak collects the telemetry required to:

- Detect suspicious activity
- Investigate security incidents
- Support incident response
- Improve visibility across business systems
- Meet operational and security requirements

Monitoring is regularly reviewed to ensure it remains relevant, effective and proportionate to the organisation's size and risk profile.

---

# Telemetry Sources

## Identity

- Active Directory
- Microsoft Entra ID
- Authentication Events
- Account Management Events

Purpose:

Monitor authentication activity, privilege changes and identity-related security events.

---

## Implemented Endpoint Telemetry

### BNE-FIN-WS01

BNE-FIN-WS01 is a domain-joined Windows workstation configured as a monitored BluePeak endpoint.

Telemetry currently collected:

- Windows Security Event Log
- Microsoft PowerShell Operational Log
- Sysmon Operational Log

Sysmon provides visibility into:

- Process creation
- Network connections
- File creation
- Registry activity
- DNS queries

### Log Collection

The workstation runs the Splunk Universal Forwarder.

Telemetry flow:

BNE-FIN-WS01
→ Splunk Universal Forwarder
→ TCP 9997
→ Splunk Enterprise
→ Searchable by SOC analyst

During implementation, the SplunkForwarder service account initially could not subscribe to the Sysmon Operational event channel.

The service account was added to the local Event Log Readers group and the SplunkForwarder service was restarted. Sysmon events were then successfully forwarded to Splunk.

### Splunk Sysmon Integration

Windows endpoint telemetry is collected using Sysmon and forwarded to the central Splunk Enterprise instance using the Splunk Universal Forwarder.

The Splunk Add-on for Sysmon is installed on the Splunk server to provide structured field extraction for Sysmon telemetry.

Current Sysmon fields available to analysts include:

- EventCode
- User
- Image
- ParentImage
- CommandLine
- ProcessId
- ProcessGuid
- Hashes

This allows analysts to investigate endpoint activity using structured SPL searches rather than parsing raw XML event data.

Example:

host="BNE-FIN-WS01" EventCode=1 Image="*\\powershell.exe"
| table _time User Image ParentImage CommandLine
| sort _time

### Validation

End-to-end ingestion was validated using controlled activity on BNE-FIN-WS01.

Splunk successfully received:

- Sysmon Event ID 1 — Process Create
- Sysmon Event ID 3 — Network Connection
- Sysmon Event ID 5 — Process Terminated
- Sysmon Event ID 11 — File Create
- Sysmon Event ID 12 — Registry Object Create/Delete
- Sysmon Event ID 13 — Registry Value Set
- Sysmon Event ID 22 — DNS Query

Windows Security and PowerShell Operational telemetry were also confirmed searchable from the same endpoint.

# Monitoring Roadmap

The wider BluePeak architecture defines additional telemetry sources that would be expected within the simulated enterprise.

These sources form part of the target monitoring architecture but should not be interpreted as currently implemented lab telemetry.

## Endpoint — Planned

- Microsoft Defender for Endpoint / EDR telemetry
- Additional Windows endpoints
- Additional server telemetry

## Network — Planned

- FortiGate firewall logs
- VPN activity

## Cloud — Planned

- Microsoft Entra ID
- Microsoft 365
- Exchange Online
- SharePoint Online
- Teams

## Infrastructure — Planned

- Hyper-V
- Core Windows servers
- File services
- Integration platform

As the technical lab develops, additional sources will be implemented and validated before being treated as available investigation telemetry.

# Security Operations

Security telemetry is centrally collected and analysed using Splunk Enterprise.

The Security Operations team uses this information to investigate alerts, identify suspicious activity and support incident response across the organisation.

---

# Guiding Principle

BluePeak prioritises collecting meaningful telemetry over collecting every available log.

Monitoring should improve the Security Operations team's ability to understand business activity, investigate incidents and make informed decisions.

