\# BluePeak SOC Environment



BluePeak Logistics is a simulated enterprise environment built to develop and demonstrate practical SOC analyst skills through hands-on security investigations.



Rather than working through isolated security labs, BluePeak provides a persistent fictional organisation with its own endpoints, users, infrastructure, security tooling, monitoring strategy and investigation process.



The objective is to investigate realistic activity using telemetry generated inside the lab and document conclusions based on the evidence available.



\## Current Environment



BluePeak currently uses:



\- Splunk Enterprise for centralised log analysis and investigation

\- Splunk Universal Forwarder for endpoint log collection

\- Sysmon for detailed Windows endpoint telemetry

\- Windows Security auditing

\- PowerShell Operational logging

\- Windows virtual machines representing BluePeak endpoints



Telemetry currently includes process creation, network connections, DNS queries, file creation, Windows authentication events and PowerShell activity.



\## Investigation Method



Investigations follow an evidence-led SOC workflow:



1\. Review the initial alert or suspicious activity

2\. Establish the affected host and user context

3\. Build a timeline from available telemetry

4\. Pivot across relevant data sources

5\. Separate observed evidence from assumptions

6\. Assess severity and confidence

7\. Recommend containment or escalation where appropriate

8\. Document telemetry gaps and investigation limitations



Not every investigation is designed to produce a confirmed compromise. Where the available telemetry cannot prove something, that limitation is documented rather than assumed.



\## Investigations



\### BP-001 — Suspicious PowerShell Execution



\*\*Host:\*\* BNE-FIN-WS01  

\*\*Department:\*\* Finance  

\*\*Disposition:\*\* Escalated  

\*\*Assessment:\*\* Highly Suspicious



The investigation identified unusual PowerShell execution followed by:



\- Hidden PowerShell activity

\- File creation within the user's Temp directory

\- PowerShell-generated DNS activity

\- `cmd.exe` execution of `whoami`

\- Discovery output written to an additional temporary file



No associated outbound network connection was confirmed from the available telemetry.



Host isolation and escalation were recommended.



The investigation also exposed a monitoring gap in Windows logon auditing. Successful logon auditing was subsequently enabled and validated through Splunk.



\## Portfolio Interface



This repository includes a lightweight web interface for presenting BluePeak investigations.



The interface is intentionally simple. The investigation process, telemetry and analyst reasoning are the focus of the project.



Each case includes:



\- Executive summary

\- Evidence timeline

\- SPL used during investigation

\- Splunk evidence screenshots

\- Analyst assessment

\- Recommended actions

\- Investigation limitations

\- Monitoring or engineering findings



\## Project Status



BluePeak is an ongoing project.



Future development will include additional investigation scenarios, expanded enterprise telemetry, endpoint detection and response (EDR), and further detection and monitoring engineering.



\## Disclaimer



BluePeak Logistics is a fictional organisation created for cybersecurity training and portfolio purposes.



The environment and scenarios are simulated. Investigation evidence shown in this project is generated from hands-on lab telemetry.

