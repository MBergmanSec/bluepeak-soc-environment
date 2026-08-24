# Escalation Guide

## Purpose

This document provides a simple framework for assessing the severity of security incidents and determining when escalation is required.

Severity is based on both technical evidence and potential business impact.

Security tool severity ratings may assist triage but do not determine the final incident severity.

---

## Severity Levels

| Severity | Description | Typical Response |
|---|---|---|
| Low | Limited security concern with little or no business impact. Activity may be benign, expected or already contained. | Investigate as required, document findings and close when appropriate. |
| Medium | Suspicious activity requiring investigation, but no confirmed significant compromise or major business impact. | Investigate, gather additional evidence and monitor for escalation indicators. |
| High | Credible evidence of compromise or significant risk to important users, systems or business data. | Prioritise investigation, notify appropriate personnel and consider containment. |
| Critical | Confirmed or highly credible incident presenting major operational, safety, widespread or sensitive-data impact. | Immediate escalation and coordinated incident response. |

---

## Factors Affecting Severity

Analysts should consider:

- Strength of the available evidence
- Importance of the affected system
- Privileges of the affected account
- Type and sensitivity of affected data
- Number of users or systems affected
- Evidence of persistence or lateral movement
- Potential operational disruption
- Whether suspicious activity is continuing

Severity may change as new evidence becomes available.

---

## Business Context

Technical severity and business severity are not always the same.

For example, suspicious activity affecting a privileged administrator account or critical business server may require greater priority than similar activity affecting a low-risk endpoint.

Analysts should consider what the affected asset or identity means to BluePeak before determining severity.

---

## Escalation

An incident should be escalated when:

- Significant compromise is confirmed or strongly suspected
- Critical systems or business processes may be affected
- Privileged accounts appear compromised
- Sensitive information may have been accessed or exposed
- Activity appears to be spreading between systems
- Containment action may be required
- The analyst cannot safely resolve the incident within their authority
- Business impact exceeds normal SOC handling

Analysts should escalate when the available evidence justifies action rather than waiting for complete certainty.

---

## Escalation Information

Where possible, escalation should include:

- What happened
- Systems and users involved
- Relevant evidence
- Current severity
- Known or potential business impact
- Actions already taken
- Outstanding questions
- Recommended next action

---

## Guiding Principle

Escalation is a risk decision.

The objective is to provide decision-makers with enough reliable information to take appropriate action while clearly communicating any uncertainty.