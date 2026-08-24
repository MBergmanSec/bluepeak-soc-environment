# Asset Inventory

## Purpose

This document provides a high-level inventory of the primary technology assets used by BluePeak Logistics.

It is intended as a quick reference for IT operations and security investigations rather than a complete hardware register.

---

## Core Server Infrastructure

| Asset | Type | Role | Location |
|---|---|---|---|
| HV01 | Physical Server | Hyper-V Host | Brisbane |
| HV02 | Physical Server | Hyper-V Host | Brisbane |
| DC01 | Virtual Server | Active Directory / DNS | Brisbane |
| DC02 | Virtual Server | Active Directory / DNS | Brisbane |
| APP01 | Virtual Server | Business Integration Services | Brisbane |
| FS01 | Virtual Server | File Services | Brisbane |
| SPLUNK01 | Virtual Server | Security Monitoring | Brisbane |

---

## Network Infrastructure

BluePeak operates centrally managed network infrastructure across its offices and warehouse locations.

Primary network assets include:

- FortiGate firewalls
- Managed network switches
- Corporate wireless access points
- Site-to-site VPN infrastructure

Detailed network design is documented separately in `Network-Overview.md`.

---

## End-User Devices

BluePeak employees use company-managed Windows laptops and workstations appropriate to their roles.

Individual endpoints are identified using BluePeak's workstation naming standard.

Corporate endpoints are centrally managed and protected using BluePeak's endpoint security controls.

---

## Operational Devices

BluePeak also operates technology supporting warehouse and business operations, including:

- Warehouse scanners and handheld devices
- Network printers
- IP phones
- Security cameras
- Physical access-control devices

These devices are separated from standard corporate endpoints where appropriate.

---

## Device Naming

BluePeak uses a consistent naming convention for corporate endpoints to make devices easier to identify during administration and security investigations.

### Workstation Format

`[LOCATION]-[DEPARTMENT]-[TYPE][NUMBER]`

Example:

`BNE-FIN-WS014`

This identifies:

- `BNE` — Brisbane
- `FIN` — Finance
- `WS` — Workstation
- `014` — Device number

### Common Device Types

| Code | Device Type |
|---|---|
| WS | Workstation |
| LT | Laptop |

Department and location codes follow the names used throughout BluePeak's existing business documentation.

Server naming follows the established role-based convention, such as `DC01`, `APP01` and `FS01`.


## Inventory Management

This inventory records asset types that are relevant to understanding the BluePeak environment.

Individual assets may be added as the environment is built or when they become relevant to an investigation.

The inventory should remain useful and maintainable rather than attempting to document unnecessary detail.