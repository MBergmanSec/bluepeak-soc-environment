\# BluePeak SOC Environment



BluePeak Logistics is a simulated enterprise SOC environment I am building to develop and demonstrate practical security monitoring, investigation and incident response skills.



Instead of treating each lab as an isolated exercise, BluePeak provides a persistent fictional organisation with its own users, endpoints, infrastructure, business context, security monitoring standards and investigation process.



The technical lab generates real endpoint telemetry which I investigate through Splunk and document as SOC cases.



## Live Investigation Portfolio

**[View the BluePeak SOC Investigation Portal](https://mbergmansec.github.io/bluepeak-soc-environment/)**



The portal provides a recruiter-friendly view of completed investigations, including investigation timelines, SPL queries, evidence screenshots, analyst assessments, recommended actions and identified monitoring gaps.



\---



\## Current Lab



The implemented lab currently includes:



\- Splunk Enterprise

\- Splunk Universal Forwarder

\- Sysmon

\- Windows Security auditing

\- PowerShell Operational logging

\- Windows endpoint telemetry



Current telemetry includes:



\- Process creation

\- File creation

\- Network connections

\- DNS queries

\- Authentication activity

\- PowerShell activity



The wider BluePeak architecture includes additional planned infrastructure and telemetry sources which will be implemented progressively as the lab develops.



\---



\## Investigation Approach



BluePeak investigations follow an evidence-led workflow:



\*\*Observation → Evidence → Assessment → Confidence → Actions\*\*



The objective is not to force every alert into a malicious or benign conclusion.



Investigations document what the available telemetry supports, what remains unverified, and what additional evidence or response actions would be required.



\---



\## Current Investigations



\### BP-001 — Suspicious PowerShell Execution



\*\*Host:\*\* `BNE-FIN-WS01`  

\*\*Department:\*\* Finance  

\*\*Disposition:\*\* Escalated  

\*\*Assessment:\*\* Highly Suspicious



BP-001 involved unusual PowerShell execution followed by temporary file creation, DNS activity and user discovery.



The investigation identified:



\- PowerShell execution using `ExecutionPolicy Bypass`

\- Hidden PowerShell activity

\- File creation within the LocalAdmin Temp directory

\- DNS resolution initiated by PowerShell

\- `cmd.exe` execution of `whoami`

\- Discovery output redirected to an additional temporary file



No associated outbound network connection was confirmed from the available telemetry.



Host isolation and escalation were recommended.



The investigation also exposed a monitoring gap: successful Windows logon auditing was disabled during the incident period. The configuration was corrected and Event ID 4624 ingestion was subsequently validated in Splunk.



\*\*\[View BP-001 Investigation](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-001.html)\*\*



\---



\## BluePeak Documentation



The fictional enterprise environment provides context for investigations and defines what activity should or should not be considered normal.



\### Environment



\- \[Company Overview](docs/Company/Company-Overview.md)

\- \[Technology Overview](docs/Infrastructure/Technology-Overview.md)

\- \[Network Overview](docs/Infrastructure/Network-Overview.md)

\- \[Asset Inventory](docs/Infrastructure/Asset-Inventory.md)

\- \[Identity and Authentication](docs/Infrastructure/Identity%20and%20Authentication.md)



\### SOC Operations



\- \[Security Monitoring](docs/SOC/Security-Monitoring.md)

\- \[Investigation Workflow](docs/SOC/Investigation-Workflow.md)

\- \[Escalation Guide](docs/SOC/Escalation-Guide.md)

\- \[Incident Response Philosophy](docs/SOC/Incident-Response-Philosophy.md)



\### Investigation Standards



\- \[SOC Investigation Standards](docs/Standards/SOC-Investigation-Standards.md)

\- \[Investigation Checklist](docs/Standards/Investigation-Checklist.md)

\- \[Known Good Activity](docs/Operations/Known-Good-Activity.md)



The full documentation set is available under \[`/docs`](docs/).



\---



\## Why BluePeak Exists



The goal of this project is to practise the work expected of a SOC analyst rather than only completing guided labs.



That includes:



\- Writing and refining SPL

\- Investigating endpoint telemetry

\- Correlating activity across multiple event types

\- Building timelines

\- Separating evidence from assumptions

\- Recognising legitimate administrative activity

\- Identifying telemetry gaps

\- Making escalation and containment decisions

\- Writing clear investigation reports



As the environment develops, additional cases will introduce different attack behaviours, benign activity, false positives and new telemetry sources.



\---



\## Project Status



\*\*Active Development\*\*



Completed:



\- BluePeak enterprise and SOC documentation foundation

\- Splunk/Sysmon endpoint monitoring

\- Windows Security telemetry

\- PowerShell telemetry

\- BP-001 investigation

\- Recruiter-facing investigation portal



Next:



\- Additional SOC investigations

\- Expanded endpoint coverage

\- EDR integration

\- Detection engineering

\- Additional enterprise telemetry



\---



\## Disclaimer



BluePeak Logistics is a fictional organisation created for cybersecurity training and portfolio purposes.



The organisation, users and investigation scenarios are simulated. Security telemetry shown in the investigation portfolio is generated through hands-on activity within the lab environment.

