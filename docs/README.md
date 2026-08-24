# BluePeak Logistics — SOC Environment

> A business-driven SOC investigation environment built to demonstrate practical security analysis, evidence-based investigation and incident response.

## Overview

BluePeak Logistics is a fictional Australian logistics company created as the foundation for a realistic cybersecurity portfolio.

Instead of investigating isolated alerts in a generic home lab, the project places security activity inside a documented business environment.

BluePeak has defined departments, locations, users, business applications, infrastructure, operational processes and security procedures.

This means an investigation is not simply:

**"Why did PowerShell run?"**

It becomes:

**"Why did PowerShell run on this system, under this account, at this time — and does that activity make sense within the business?"**

That distinction is the core of the project.

---

## Project Objective

The objective of BluePeak is to demonstrate how a SOC analyst approaches security investigations when technical evidence must be interpreted alongside business context.

The project is designed around:

- Evidence-driven investigation
- Business impact
- Hypothesis testing
- Correlation across multiple telemetry sources
- Distinguishing suspicious activity from legitimate operations
- Clear assessment of uncertainty and confidence
- Practical escalation and response decisions

The environment is intentionally designed to contain legitimate activity that may initially appear suspicious.

An alert is treated as the beginning of an investigation — not the conclusion.

---

## BluePeak Logistics

BluePeak Logistics represents an Australian logistics organisation with more than 300 employees operating across a primary Brisbane location and smaller regional sites.

The company uses a hybrid technology environment combining cloud services with selected on-premises infrastructure.

Core technologies represented within the environment include:

- Microsoft Active Directory
- Microsoft Entra ID
- Microsoft 365
- Microsoft Hyper-V
- Windows endpoints and servers
- Sysmon
- Microsoft Defender
- Fortinet network security
- Splunk Enterprise

Business and technical decisions are documented within the repository so investigations can be assessed against an established environment rather than invented context during each case.

---

## Investigation Method

BluePeak investigations follow a consistent analytical approach:

**Observation → Evidence → Assessment → Confidence → Actions**

Analysts are expected to:

1. Understand the alert and business context.
2. Identify the questions that need to be answered.
3. Gather relevant evidence.
4. Test legitimate and malicious explanations.
5. Assess the evidence and potential business impact.
6. Reach a defensible conclusion or escalate when appropriate.
7. Document the reasoning clearly enough for another analyst to follow.

Investigations are not expected to answer every possible question.

They are expected to reach the best defensible decision supported by the evidence available at the time.

---

## Repository

```text
BluePeak-SOC-Environment/
├── Company/          Business and organisational context
├── Images/           Branding, diagrams and supporting visuals
├── Infrastructure/   Identity, network, server and asset architecture
├── Operations/       IT operations and known-good activity
├── SOC/              Monitoring, investigation and escalation processes
├── Standards/        Investigation quality standards
└── Templates/        Standard investigation case structure
```

See `REPOSITORY-STRUCTURE.md` for a more detailed repository map.

---

## Environment Design

BluePeak uses a hybrid architecture.

The Brisbane main office hosts the primary on-premises infrastructure, including:

- Two Active Directory Domain Controllers
- Hyper-V virtualisation
- Internal application and integration services
- File services
- Centralised Splunk security monitoring

Regional locations connect securely to central services while approved cloud platforms are accessed directly where appropriate.

Security telemetry is collected from relevant identity, endpoint, network, cloud and infrastructure sources.

The objective is meaningful investigative visibility rather than collecting every available log.

---

## Investigation Portfolio

BluePeak security investigations are developed using telemetry generated within the technical lab and assessed against the documented business and operational environment.

BluePeak security investigations will be added as the technical environment is implemented.

Cases will use the documented company, infrastructure and operational context contained within this repository.

Investigations may include activity involving:

- Identity and authentication
- Endpoint execution
- PowerShell
- Persistence
- Network activity
- Cloud services
- Privileged access
- Service accounts
- Legitimate administrative activity
- Multi-source event correlation

Each completed investigation will document the evidence, analytical reasoning, business impact, confidence and final outcome.

---

## Current Status

**Phase: Active SOC Investigation Development**

The business, infrastructure, operational and SOC documentation foundation has been established.

The technical lab is now operational with a monitored Windows endpoint forwarding Windows Security, PowerShell Operational and Sysmon telemetry into Splunk Enterprise.

The first documented investigation, **BP-001 — Suspicious PowerShell Execution**, has been completed using telemetry generated within the lab.

Current development is focused on:

- Expanding investigation scenarios
- Improving telemetry coverage
- Identifying and correcting monitoring gaps
- Developing analyst investigation and reporting skills
- Introducing endpoint detection and response capabilities
- Expanding the environment as required by future investigations

The environment will continue to evolve alongside the investigation portfolio.

## Why I Built This

Many cybersecurity labs demonstrate how to use a tool or identify a specific attack technique.

BluePeak is intended to go further.

The goal is to demonstrate the analytical process behind security operations: understanding what happened, determining whether it matters, communicating uncertainty and making a defensible decision using both technical evidence and business context.

The environment exists to support the investigations.

**The investigations are the portfolio.**