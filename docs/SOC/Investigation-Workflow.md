# Investigation Workflow

## Purpose

This document defines the standard workflow used by the BluePeak Logistics Security Operations team when investigating security alerts and incidents.

The workflow provides consistency without requiring analysts to follow a rigid technical checklist.

---

## 1. Triage

Establish what has been reported and determine the initial scope.

Identify:

- What triggered the investigation
- Affected user or account
- Affected system or application
- Time of the activity
- Available telemetry
- Potential business impact

The initial alert should be treated as a starting point rather than proof that malicious activity occurred.

---

## 2. Investigate

Determine what questions need to be answered and gather relevant evidence.

Evidence may come from:

- Splunk
- Endpoint telemetry
- Identity and authentication logs
- Firewall and VPN logs
- Cloud services
- Business documentation
- IT or user confirmation

Investigation should be driven by questions rather than searches performed without a clear purpose.

---

## 3. Assess

Correlate the available evidence and determine the most likely explanation for the activity.

Consider:

- Does the activity match normal behaviour?
- Is there a legitimate operational explanation?
- Does the evidence support the initial alert?
- Are there alternative explanations?
- Is additional evidence required?
- What is the potential business impact?

Facts should remain separate from assumptions or hypotheses.

---

## 4. Decide

Based on the available evidence, determine the appropriate outcome.

Possible outcomes include:

- Close as benign or expected activity
- Continue investigation
- Request additional information
- Recommend containment
- Escalate the incident

The decision should reflect both technical evidence and business impact.

---

## 5. Document

Record the investigation so another analyst can understand what occurred and how the conclusion was reached.

The final record should clearly identify:

- Key observations
- Supporting evidence
- Assessment
- Business impact
- Confidence level
- Actions taken or recommended
- Final outcome

---

## Investigation Principle

The purpose of an investigation is not to answer every possible question.

An investigation is complete when sufficient evidence exists to support a reasonable conclusion or justify further escalation.