# SOC Investigation Standards

## Purpose

This document defines the minimum quality standards expected for security investigations performed by the BluePeak Logistics Security Operations team.

The objective is to produce investigations that are clear, evidence-based and understandable to another analyst without requiring additional explanation.

---

## Investigation Structure

Key findings should follow the structure:

**Observation → Evidence → Assessment → Confidence → Actions**

### Observation

State what was observed without immediately assigning meaning or intent.

### Evidence

Record the information supporting the observation.

Evidence should be relevant, attributable and timestamped where appropriate.

### Assessment

Explain what the available evidence indicates.

Facts should be clearly separated from assumptions and hypotheses.

### Confidence

State the level of confidence in the assessment:

- High
- Medium
- Low

Confidence should reflect the strength and completeness of the available evidence.

### Actions

Record actions already taken and any recommended next steps.

---

## Evidence Standards

Investigations should:

- Preserve relevant timestamps
- Identify affected users and systems
- Record important searches or evidence sources
- Distinguish observed facts from interpretation
- Correlate multiple sources where useful
- Avoid conclusions unsupported by available evidence

Not every available log or event needs to be included.

Only evidence that contributes to understanding or resolving the investigation should be documented.

---

## Investigation Language

Analysts should use objective language that reflects the strength of the evidence.

Prefer:

- "The evidence indicates..."
- "Activity is consistent with..."
- "No evidence was identified..."
- "Unable to confirm..."
- "Further investigation is recommended..."

Avoid presenting assumptions as established facts.

---

## Business Context

Technical findings should be considered alongside the role of the affected user, system or business process.

Where relevant, investigations should explain why the activity matters to BluePeak rather than describing technical events in isolation.

---

## Investigation Quality

A completed investigation should allow another analyst to understand:

- What happened
- What evidence was reviewed
- What the evidence indicates
- What remains uncertain
- Why the final decision was made
- What should happen next

An investigation does not need to answer every possible question.

It needs enough reliable evidence to support a reasonable conclusion or escalation decision.