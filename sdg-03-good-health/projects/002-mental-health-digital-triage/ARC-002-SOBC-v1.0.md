# Strategic Outline Business Case (SOBC): Mental Health Digital Triage

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Mental Health Digital Triage (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Mental Health Digital Triage Programme, NHS England |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Mental Health Digital Triage Programme Board, NHS England Digital, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case presents the case for investment in an AI-assisted mental health triage and routing platform, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: The Mental Health Digital Triage programme will deploy an AI-assisted assessment and routing platform that provides immediate mental health triage, reducing IAPT waiting times by 40% and ensuring individuals at high risk receive crisis intervention within minutes.

**Problem Statement**: One in four adults experiences mental health conditions annually, but only 25% receive treatment. IAPT waiting times exceed 18 weeks in some areas. Mental health crisis presentations at A&E are increasing because community services cannot assess and route patients quickly enough.

**Proposed Solution**: A clinically validated, AI-assisted digital triage system using validated instruments (PHQ-9, GAD-7) with ML risk stratification, integrated with IAPT services and crisis teams. AI augments clinical capacity — clinicians remain in the loop for all clinical decisions.

**Strategic Fit**: NHS Long Term Plan mental health parity of esteem, NHS mental health workforce strategy, SDG 3 (Good Health and Well-Being).

**Investment Required**: GBP 18.0M over 3 years

- Capital: GBP 12.5M
- Operational (3 years): GBP 5.5M

**Expected Benefits**: GBP 95M over 5 years

- Reduced A&E mental health presentations: GBP 40M
- IAPT throughput improvement: GBP 35M
- Crisis team efficiency: GBP 20M

**Return on Investment**:

- NPV: GBP 28.4M (discounted at 3.5%, after 40% optimism bias)
- Payback Period: 24 months
- ROI: 210% over 5 years

**Recommended Option**: Option 2: AI-Assisted Clinical Triage with Clinician Oversight

**Key Risks**:

1. MHRA regulatory pathway uncertainty for AI as Medical Device in mental health
2. Algorithmic bias against minority ethnic communities with existing mental health disparities
3. Clinical safety — false negative for high-risk patient could result in serious patient harm

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Mental health services are in crisis. Demand has increased 30% since the COVID-19 pandemic while workforce growth has been limited. IAPT services — the primary route for adults with common mental health conditions — have waiting times of 6-18 weeks depending on area. One in three people referred to IAPT do not attend their first assessment appointment because they have deteriorated, recovered, or given up waiting. A&E mental health presentations have increased 24% in three years, costing GBP 2,500 per attendance compared to GBP 150 for a community assessment.

**Consequences of Inaction**:

- IAPT waiting times continue to grow as demand outstrips clinical assessment capacity
- A&E mental health presentations increase further, costing GBP 400M+ annually
- Individuals at high risk remain unidentified for weeks during IAPT waiting periods
- Mental health workforce burnout accelerates as clinicians face unsustainable caseloads
- NHS Long Term Plan target of 2 million additional people accessing mental health services unachievable

### A1.2 Strategic Alignment

- **NHS Long Term Plan**: Additional 2 million people accessing NHS mental health services by 2028/29
- **NHS Mental Health Implementation Plan**: Digital-first approaches to improve access and reduce waits
- **Parity of Esteem**: Equivalent investment and access standards for mental and physical health
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Patient-Centred), 2 (Clinical Safety), 5 (Privacy/Caldicott)

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Continue with current IAPT assessment pathways. Wait times continue to grow.

**Costs** (5-year): GBP 0 capital, GBP 2bn continued A&E costs, continued IAPT underperformance
**Benefits**: GBP 0

**Recommendation**: **Reject** — Unacceptable. Waiting times and A&E presentations will continue to increase.

---

### Option 1: Digital Self-Assessment Without AI (Minimal)

**Description**: Deploy validated questionnaires (PHQ-9, GAD-7) online for self-completion, with results sent to IAPT services for manual clinical review. No AI risk stratification.

**Costs** (5-year): GBP 5.0M total
**Benefits** (5-year): GBP 25M (primarily IAPT admin efficiency)

**Pros**: Low cost, low regulatory burden, low clinical risk
**Cons**: Does not reduce clinical assessment workload (still requires manual review), no real-time crisis detection, limited impact on waiting times

**Stakeholder Goals Met**: 25%

---

### Option 2: AI-Assisted Clinical Triage with Clinician Oversight (RECOMMENDED)

**Description**: AI-assisted triage using validated instruments with ML risk stratification. AI provides risk categorisation and routing recommendation; clinicians review and confirm all categorisations. Crisis escalation pathway with automatic notification to crisis teams for high-risk individuals.

**Costs** (5-year): GBP 18.0M total

- Capital: GBP 12.5M (AI development GBP 5M, clinical validation study GBP 2.5M, integration GBP 2M, MHRA regulatory GBP 1M, testing GBP 1M, design GBP 1M)
- Operational: GBP 5.5M (cloud GBP 1.5M, clinical team GBP 2M, AI model maintenance GBP 1M, support GBP 1M)

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Reduced A&E MH presentations | FINANCIAL | GBP 2M | GBP 6M | GBP 10M | GBP 11M | GBP 11M | GBP 40M |
| B-002 | IAPT throughput improvement | OPERATIONAL | GBP 3M | GBP 6M | GBP 8M | GBP 9M | GBP 9M | GBP 35M |
| B-003 | Crisis team efficiency | OPERATIONAL | GBP 1M | GBP 3M | GBP 5M | GBP 5.5M | GBP 5.5M | GBP 20M |
| **Total** | | | **GBP 6M** | **GBP 15M** | **GBP 23M** | **GBP 25.5M** | **GBP 25.5M** | **GBP 95M** |

**NPV** (3.5% discount): GBP 55.8M. With 40% optimism bias on costs (GBP 25.2M): **NPV = GBP 28.4M**

**Stakeholder Goals Met**: 85%

---

### Option 3: Fully Autonomous AI Triage (No Clinician Review)

**Description**: AI system autonomously triages and routes patients without clinician review for low and medium-risk categorisations.

**Costs** (5-year): GBP 15.0M total
**Benefits** (5-year): GBP 110M

**Pros**: Maximum throughput improvement, lowest ongoing clinical cost
**Cons**: Unacceptable clinical safety risk, MHRA regulatory challenge extreme, RCPsych opposition, likely UK GDPR Article 22 violation, public trust damage

**Stakeholder Goals Met**: 40% (clinical safety and regulatory goals not met)

**Recommendation**: **Reject** — Clinical safety, regulatory, and ethical risks are unacceptable for autonomous AI decision-making in mental health.

---

## B3. Recommended Option

**Recommendation**: **Option 2: AI-Assisted Clinical Triage with Clinician Oversight**

**Rationale**: Delivers 85% of stakeholder goals with manageable clinical safety risk (clinician always in the loop). NPV of GBP 28.4M after optimism bias. MHRA regulatory pathway achievable for AI-assisted (not autonomous) system. Clinician oversight addresses RCPsych and service user concerns.

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for AI development and clinical validation, G-Cloud for infrastructure

**Key Consideration**: Clinical validation study may require partnership with NHS research institution and NIHR funding for prospective clinical investigation required by MHRA.

**Contract Type**: Collaborative development agreement for AI model with Crown IP ownership; managed service for operational platform

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 18.0M over 5 years

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 6.0M | GBP 5.0M | GBP 1.5M | GBP 0 | GBP 0 | GBP 12.5M |
| OpEx | GBP 0.5M | GBP 1.0M | GBP 1.2M | GBP 1.4M | GBP 1.4M | GBP 5.5M |
| **Total** | **GBP 6.5M** | **GBP 6.0M** | **GBP 2.7M** | **GBP 1.4M** | **GBP 1.4M** | **GBP 18.0M** |

**Funding Source**: NHS Mental Health Ring-Fenced Investment (Spending Review 2025)

**Affordability**: GBP 18M represents 0.3% of the GBP 6bn mental health ring-fence over the Spending Review period. **Affordable.**

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: NHS England National Director for Mental Health

**Key Gate**: MHRA Regulatory Decision (Gate 3) — determines whether full conformity assessment is required before clinical deployment. This gate is on the critical path and could delay the programme by 6-12 months if classification is unfavourable.

## E2. Delivery Phases

1. **Discovery** (6 months): User research with service users, clinical pathway mapping, MHRA pre-submission engagement
2. **Alpha** (6 months): AI model prototype, clinical validation study design, ethics approval
3. **Clinical Validation** (12 months): Prospective clinical study comparing AI-assisted triage with standard clinical assessment
4. **Beta** (6 months): Integration with IAPT services, bias audit, MHRA submission
5. **Live** (ongoing): Phased deployment, post-market surveillance, continuous model improvement

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | MHRA requires full clinical investigation | Medium | Major | 12 | Early MHRA engagement, pre-submission meeting, phased regulatory approach |
| R-002 | Algorithmic bias against ethnic minorities | Medium | Critical | 16 | Diverse training data, independent bias audit, service user co-design |
| R-003 | False negative for high-risk patient | Low | Critical | 12 | 99.9% sensitivity target, safety net monitoring, clinician review |
| R-004 | Clinician resistance to AI-assisted triage | Medium | Moderate | 9 | Clinical co-design, RCPsych engagement, transparent AI explainability |
| R-005 | Service user trust in AI assessment | Medium | Major | 12 | Co-design with lived experience, human pathway option, transparency |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: AI-Assisted Clinical Triage with Clinician Oversight

**Investment**: GBP 18.0M over 5 years

**Expected Return**: GBP 95M over 5 years (NPV: GBP 28.4M after optimism bias)

**Go/No-Go**: **PROCEED to Discovery phase**

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO | | |
| | NHS England Finance Director | | |
| | NHS England CDO | | |
| | Clinical Lead | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Mental Health Digital Triage
**Model**: Claude Opus 4.6
