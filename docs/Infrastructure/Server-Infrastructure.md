# Server Infrastructure

## Purpose

This document provides a high-level overview of the core server infrastructure supporting BluePeak Logistics.

It describes the purpose of BluePeak's primary servers and virtualisation environment without documenting detailed hardware specifications or configurations.

---

## Infrastructure Model

BluePeak's primary server infrastructure is located at the Brisbane main office.

Microsoft Hyper-V provides the virtualisation platform for core server workloads.

BluePeak maintains a small, centralised server environment and uses cloud services where practical rather than hosting unnecessary infrastructure internally.

---

## Hyper-V Infrastructure

BluePeak operates two Hyper-V hosts:

| Host | Purpose |
|---|---|
| HV01 | Virtualisation Host |
| HV02 | Virtualisation Host |

The two hosts provide the platform for BluePeak's core virtual server workloads and reduce reliance on a single physical host.

---

## Core Servers

| Server | Role | Location |
|---|---|---|
| DC01 | Active Directory and DNS | Brisbane |
| DC02 | Active Directory and DNS | Brisbane |
| APP01 | Business Integration Services | Brisbane |
| FS01 | File Services | Brisbane |
| SPLUNK01 | Security Monitoring | Brisbane |

---

## DC01 and DC02

DC01 and DC02 provide BluePeak's core Active Directory and DNS services.

They support:

- User and computer authentication
- Active Directory services
- Internal DNS
- Group Policy
- Access to internal resources

Operating two Domain Controllers provides redundancy for critical identity services.

---

## APP01

APP01 provides internal application and integration services.

BluePeak uses several cloud-hosted business platforms, and APP01 supports integrations and automated processes that allow these systems to exchange information with internal services where required.

Because APP01 supports multiple business processes, disruption or suspicious activity affecting this server may have wider operational impact.

---

## FS01

FS01 provides central file services for BluePeak.

It stores shared business information used by authorised departments and employees.

Access is controlled through BluePeak's identity and access controls.

Activity affecting FS01 may be relevant to investigations involving unauthorised access, data theft, ransomware or unusual user behaviour.

---

## SPLUNK01

SPLUNK01 hosts BluePeak's central Splunk Enterprise environment.

Relevant security telemetry from across the organisation is collected and analysed through Splunk to support:

- Security monitoring
- Alert investigation
- Incident response
- Event correlation

SPLUNK01 is primarily managed by the Security Operations team.

---

## Server Administration

Core infrastructure is managed by BluePeak's internal IT team.

Security Operations monitors relevant server activity and works with IT when investigations require administrative action, containment or infrastructure changes.

This separation provides clear ownership while allowing IT and Security to work together during incidents.

---

## Design Principle

BluePeak maintains only the server infrastructure required to support business operations.

Additional server roles or services are introduced when there is a clear operational, technical or security requirement rather than being deployed unnecessarily.