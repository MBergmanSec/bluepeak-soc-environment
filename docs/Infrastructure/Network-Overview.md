# Network Overview

## Purpose

This document provides a high-level overview of the BluePeak Logistics network.

It explains how BluePeak locations, users and core systems are connected without documenting detailed network configurations.

---

## Network Architecture

BluePeak uses a hub-and-spoke network design with the Brisbane main office acting as the primary location for on-premises infrastructure.

Regional offices and warehouse locations connect securely to Brisbane using site-to-site VPN connections.

Each location also maintains direct internet access for approved cloud services such as Microsoft 365.

This allows BluePeak to centrally manage internal services without unnecessarily routing all cloud traffic through Brisbane.

---

## Brisbane Main Office

Brisbane hosts BluePeak's primary technology infrastructure.

The site includes:

- Redundant business internet connectivity
- FortiGate firewall infrastructure
- Managed switching and wireless
- Hyper-V infrastructure
- Core server networks
- Corporate user networks
- IT management network
- Site-to-site VPN connectivity

Brisbane also hosts BluePeak's central Splunk environment and core on-premises services.

---

## Regional Locations

BluePeak's warehouse and regional office locations maintain their own business internet connections, firewall, switching and wireless infrastructure.

These locations connect securely to Brisbane for access to internal services while accessing approved cloud services directly through the internet.

Regional locations do not maintain dedicated server infrastructure unless a specific operational requirement justifies it.

---

## Network Segmentation

BluePeak separates devices and services according to their purpose and level of trust.

The main network segments are:

| Network | Purpose |
|---|---|
| Server | Core on-premises servers |
| Corporate | Employee workstations and laptops |
| IT Management | Infrastructure and administrative access |
| Warehouse Devices | Scanners and operational warehouse devices |
| Printers | Network-connected printers |
| Voice | Business telephony |
| Guest | Visitors and unmanaged personal devices |
| Physical Security | Cameras and access-control systems |

Communication between network segments is restricted and permitted only where required for legitimate business operations.

---

## Remote Access

Remote employees primarily access cloud services directly using company-managed devices.

Access to internal BluePeak resources requires secure remote access through the corporate VPN.

Remote access is protected using BluePeak's identity and authentication controls, including Multi-Factor Authentication and Conditional Access where applicable.

---

## Network Security

Fortinet technology provides BluePeak's primary network security platform.

FortiGate firewalls provide:

- Network filtering
- Site-to-site VPN connectivity
- Remote-access VPN
- Security monitoring
- Network traffic visibility

Relevant firewall and VPN telemetry is made available to the Security Operations team for monitoring and investigation.

---

## Design Principle

BluePeak's network is designed to provide secure and reliable connectivity without unnecessary complexity.

Network architecture and segmentation should support business operations while limiting unnecessary access between systems and providing useful security visibility.