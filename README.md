# BluePeak SOC Environment

BluePeak Logistics is a fictional enterprise environment for practising security monitoring and SOC investigations. The lab produces endpoint telemetry that I investigate in Splunk and document as case reports. The business context, users, hosts and procedures give the cases a consistent setting.

**[Explore the BluePeak investigation portfolio](https://mbergmansec.github.io/bluepeak-soc-environment/)** — five cases with evidence, SPL queries, analyst reasoning, outcomes and monitoring gaps.

## Investigation method

For blind-investigation cases, scenarios are prepared without disclosing the setup or intended outcome to me beforehand. I investigate the resulting lab telemetry cold, following the evidence rather than a walkthrough. Earlier cases also document hands-on lab work, but did not all follow this blind format. My reports separate observed facts from hypotheses, record what cannot be confirmed, and explain the decision to escalate or close the case.

**Observation → Evidence → Assessment → Confidence → Actions**

The cases include both escalations and legitimate activity. Alert severity, my assessment of the activity, and the final disposition are separate judgments.

## Published investigations

| Case | Published | Host | Alert severity | Disposition |
| --- | --- | --- | --- | --- |
| [BP-001 — Suspicious PowerShell Execution](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-001.html) | Aug 2026 | `BNE-FIN-WS01` | Medium | Escalated |
| [BP-002 — Suspicious Persistence and Masquerading](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-002.html) | Aug 2026 | `BNE-FIN-WS01` | Medium | Escalated |
| [BP-003 — Suspicious Browser-Data Collection and Staging](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-003.html) | Sep 2026 | `BNE-FIN-WS01` | Medium | Escalated |
| [BP-004 — Suspicious Administrative Activity](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-004.html) | Sep 2026 | `BNE-IT-WS02` | Medium | Closed — benign activity |
| [BP-005 — HR Endpoint Alert Triage & Correlation](https://mbergmansec.github.io/bluepeak-soc-environment/cases/BP-005.html) | Sep 2026 | `BNE-HR-WS03` | High | Closed — benign test activity |

These are publication months from the repository history, not timestamps of the simulated events. The three host names above are case identities; they do not claim three separate persistent VMs.

## Implemented lab and scope

- Splunk Enterprise and Universal Forwarder for collection and investigation
- Sysmon, Windows Security auditing and PowerShell Operational logging on lab endpoints
- Process, file, registry, DNS, network, authentication and script activity where available in each case

BluePeak's [enterprise documentation](docs/) describes the wider fictional organisation. Some documented systems and telemetry are planned rather than implemented; each case report identifies the evidence actually available for that investigation.

## Project documentation

- [Company overview](docs/Company/Company-Overview.md) and [asset inventory](docs/Infrastructure/Asset-Inventory.md)
- [Technology overview](docs/Infrastructure/Technology-Overview.md) and [identity and authentication](docs/Infrastructure/Identity%20and%20Authentication.md)
- [Security monitoring](docs/SOC/Security-Monitoring.md), [investigation workflow](docs/SOC/Investigation-Workflow.md) and [escalation guide](docs/SOC/Escalation-Guide.md)
- [Investigation standards](docs/Standards/SOC-Investigation-Standards.md), [checklist](docs/Standards/Investigation-Checklist.md) and [known good activity](docs/Operations/Known-Good-Activity.md)

## Status

Active development. BP-001 through BP-005 are published. I am continuing to add investigations and improve the lab's telemetry and investigation procedures.

BluePeak Logistics, its users and its case scenarios are fictional. The telemetry shown in the reports was generated through hands-on activity in the lab.
