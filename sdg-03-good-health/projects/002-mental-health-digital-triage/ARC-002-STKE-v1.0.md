# Stakeholder Drivers & Goals Analysis: Mental Health Digital Triage

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
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
| **Distribution** | Mental Health Digital Triage Programme Board, NHS England Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Mental Health Digital Triage programme, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Mental Health Digital Triage programme operates at the intersection of clinical safety, AI governance, and mental health service access. The strongest alignment exists around reducing waiting times for mental health assessment and ensuring people in crisis receive immediate appropriate support. The most significant conflict is between clinical safety (ensuring AI-assisted triage does not miss high-risk individuals) and service access (reducing bottlenecks that delay assessment). The use of AI in mental health assessment creates particular sensitivity around algorithmic bias, explainability, and the irreplaceable role of human clinical judgement.

### Critical Success Factors

- Clinical safety validation demonstrating AI-assisted triage matches or exceeds clinician accuracy for risk categorisation
- Zero missed high-risk cases — sensitivity for suicide risk and self-harm must be 99.9%+
- Integration with existing IAPT (Improving Access to Psychological Therapies) referral pathways
- Service user trust in AI-assisted assessment — co-designed with people with lived experience
- Compliance with MHRA regulatory requirements for AI/ML as a Medical Device

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need to reduce mental health assessment waiting times and improve crisis response. Significant tensions between AI innovation advocates (NHS England Digital) and clinical safety concerns (Royal College of Psychiatrists, CQC). Service user organisations supportive but insistent on co-design, transparency, and the right to human-only assessment pathways.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| NHS England National Director for Mental Health | Strategic sponsor | HIGH | HIGH | Manage Closely — Strategic direction, policy alignment |
| SRO, Mental Health Digital Triage | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| NHS England Chief Digital Officer | Digital strategy oversight | HIGH | HIGH | Manage Closely — AI governance, architecture |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews, user outcomes |
| Clinical Lead (Consultant Psychiatrist) | Clinical safety and pathway design | HIGH | HIGH | Manage Closely — Clinical governance, algorithm validation |
| Clinical Safety Officer | DCB0129/DCB0160 compliance | MEDIUM | HIGH | Keep Informed — Clinical safety governance |
| NHS England SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, AI risk acceptance |
| AI Ethics Lead | Algorithmic fairness and bias | MEDIUM | HIGH | Keep Informed — Bias testing, explainability review |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| MHRA | Regulator | AI as Medical Device regulation | HIGH | HIGH |
| CQC | Regulator | Quality and safety of mental health services | HIGH | MEDIUM |
| ICO | Regulator | Data protection, AI decision-making, Art. 22 | HIGH | MEDIUM |
| Royal College of Psychiatrists | Professional body | Clinical standards, workforce impact | HIGH | HIGH |
| Mind (charity) | Mental health charity | Service user advocacy | MEDIUM | HIGH |
| Samaritans | Charity | Crisis support, suicide prevention expertise | MEDIUM | HIGH |
| Service Users and Carers | Citizens | People with lived experience of mental health | LOW | HIGH |
| IAPT Service Providers | NHS Trusts | Referral pathway recipients | MEDIUM | HIGH |
| Mental Health Crisis Teams | NHS Trusts | Crisis response teams | MEDIUM | HIGH |
| HM Treasury | Government | Funding approval | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * NHS England MH   |
        |  * ICO              |    Director          |
        |  * CQC              |  * SRO              |
        |  * NHS England SIRO |  * NHS England CDO  |
 P      |                     |  * Service Owner    |
 O      |                     |  * Clinical Lead    |
 W      |                     |  * MHRA             |
 E      |                     |  * RCPsych          |
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Service Users    |
        |                     |  * Mind             |
        |                     |  * Samaritans       |
        |                     |  * IAPT Providers   |
        |                     |  * Crisis Teams     |
        |                     |  * AI Ethics Lead   |
        |                     |  * Clinical Safety  |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: NHS England MH Director — Reduce Mental Health Assessment Waiting Times

**Stakeholder**: NHS England National Director for Mental Health

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Deliver measurable reductions in mental health assessment waiting times, particularly for IAPT and crisis services, demonstrating the NHS commitment to parity of esteem between mental and physical health.

**Context & Background**:
Mental health services face unprecedented demand. IAPT waiting times exceed 18 weeks in some areas. One in four adults experience a mental health condition annually, but only 25% receive treatment. The NHS Long Term Plan commits to an additional 2 million people accessing NHS mental health services by 2028/29. Digital triage can accelerate initial assessment and routing without requiring additional clinical staff.

**Driver Intensity**: CRITICAL

**Enablers**:

- NHS Long Term Plan ring-fenced mental health investment
- Proven digital mental health assessment tools (PHQ-9, GAD-7) validating digital approach
- Post-pandemic acceptance of digital health services including mental health

**Blockers**:

- Clinician resistance to AI-assisted decision-making in mental health
- MHRA regulatory pathway for AI as Medical Device still evolving
- Public sensitivity about AI making decisions about mental health

---

### SD-2: Royal College of Psychiatrists — Clinical Safety and Professional Standards

**Stakeholder**: Royal College of Psychiatrists

**Driver Category**: COMPLIANCE / PROFESSIONAL

**Driver Statement**: Ensure that AI-assisted mental health triage maintains the highest clinical safety standards, does not replace clinical judgement for high-risk decisions, and does not deskill the mental health workforce.

**Context & Background**:
The Royal College has expressed concern about AI replacing clinical assessment in mental health, where nuance, context, and therapeutic relationship are essential. They support digital tools that augment clinician capability but oppose any system that makes autonomous clinical decisions about mental health risk without clinician oversight. They are particularly concerned about algorithmic bias affecting minority ethnic communities who already experience poorer mental health outcomes.

**Driver Intensity**: HIGH

**Enablers**:

- Positioning the system as "AI-assisted" not "AI-autonomous" — clinician always in the loop for risk decisions
- Transparent algorithm development with clinical co-design
- Published clinical validation evidence

**Blockers**:

- Any perception that the system replaces clinical assessment
- Evidence of algorithmic bias in mental health risk assessment
- Lack of explainability in AI decision-making

---

### SD-3: Service Users — Faster Access with Human Compassion

**Stakeholder**: Service Users (people with lived experience of mental health conditions)

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Access mental health support quickly without long waiting lists, with the option for digital or human assessment, and confidence that AI-assisted triage treats them as individuals not data points.

**Context & Background**:
People experiencing mental health difficulties face long waits for assessment, often at their most vulnerable. Many would welcome faster digital triage if it means quicker access to support. However, service user organisations emphasise that mental health assessment is deeply personal — people need to feel heard, believed, and treated as individuals. The system must never feel like a bureaucratic barrier or a cold algorithmic gatekeeping mechanism.

**Driver Intensity**: HIGH

**Enablers**:

- Co-design with people with lived experience from the outset
- Clear option for human-only assessment pathway
- Transparent explanation of how AI assessment informs (not determines) their care pathway

**Blockers**:

- System feels impersonal or dismissive of individual experience
- AI assessment perceived as gatekeeping to deny access to services
- Digital exclusion preventing vulnerable individuals from accessing the service

---

### SD-4: MHRA — Regulatory Compliance for AI as Medical Device

**Stakeholder**: MHRA (Medicines and Healthcare products Regulatory Agency)

**Driver Category**: COMPLIANCE / REGULATORY

**Driver Statement**: Ensure the AI-assisted triage system complies with UK regulatory requirements for AI/ML as a Medical Device, including evidence of safety, performance, and ongoing post-market surveillance.

**Context & Background**:
The MHRA's Software as a Medical Device and AI as a Medical Device guidance requires that AI systems used for clinical decision-making (including triage and risk assessment) may be classified as medical devices. This creates regulatory requirements for pre-market conformity assessment, clinical investigation evidence, and post-market surveillance. The regulatory pathway for AI in mental health is particularly complex given the subjective nature of mental health assessment.

**Driver Intensity**: CRITICAL

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce IAPT Assessment Waiting Time by 40%

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: NHS England National Director for Mental Health

**Goal Statement**: Reduce average time from IAPT referral to initial assessment from 28 days to 17 days within 12 months of deployment, by providing immediate digital triage that routes patients to the right level of care.

**Success Metrics**:

- **Primary Metric**: Average days from IAPT referral to initial assessment
- **Secondary Metrics**:
  - Percentage of patients receiving same-day digital triage
  - Patient-reported satisfaction with assessment speed

**Baseline**: 28 days average IAPT referral-to-assessment wait

**Target**: 17 days average (40% reduction)

---

### Goal G-2: Achieve 99.9% Sensitivity for High-Risk Detection

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: Clinical Lead (Consultant Psychiatrist)

**Goal Statement**: The AI-assisted triage system must achieve 99.9% sensitivity (true positive rate) for detecting high-risk individuals (suicide risk, self-harm, psychosis) requiring immediate clinical intervention, validated through prospective clinical study.

**Success Metrics**:

- **Primary Metric**: Sensitivity for high-risk categorisation (validated against clinician assessment)
- **Secondary Metrics**:
  - False negative rate for high-risk cases
  - Time from high-risk detection to clinical review

**Baseline**: N/A (new system)

**Target**: 99.9% sensitivity, < 15 minutes from detection to clinical review

---

### Goal G-3: MHRA Regulatory Approval

**Derived From Drivers**: SD-4

**Goal Owner**: SRO

**Goal Statement**: Achieve MHRA regulatory approval (or confirmation that approval is not required) for the AI-assisted triage system before any clinical deployment.

**Success Metrics**:

- **Primary Metric**: MHRA classification decision and, if required, conformity assessment completion
- **Secondary Metrics**:
  - Clinical investigation evidence package complete
  - Post-market surveillance plan approved

**Baseline**: N/A (pre-regulatory)

**Target**: MHRA clearance before clinical deployment

---

### Goal G-4: Eliminate Algorithmic Bias Across Protected Characteristics

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: AI Ethics Lead

**Goal Statement**: Demonstrate statistically equivalent triage accuracy across all protected characteristics (age, sex, ethnicity, disability) with independent audit evidence published before deployment.

**Success Metrics**:

- **Primary Metric**: Triage accuracy parity across demographic groups (< 2% variance)
- **Secondary Metrics**:
  - Independent bias audit completed and published
  - Service user advisory group endorsement

**Baseline**: N/A (pre-deployment)

**Target**: < 2% accuracy variance across all protected characteristics

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| NHS England MH Director | SD-1 | Reduce MH waiting times | G-1 | 40% IAPT wait reduction | O-1 | Faster access to MH support |
| RCPsych | SD-2 | Clinical safety standards | G-2 | 99.9% high-risk sensitivity | O-2 | Safe AI-assisted triage |
| Service Users | SD-3 | Faster access, human option | G-1 | 40% IAPT wait reduction | O-1 | Faster access to MH support |
| Service Users | SD-3 | Faster access, human option | G-4 | No algorithmic bias | O-2 | Safe AI-assisted triage |
| MHRA | SD-4 | Regulatory compliance | G-3 | MHRA approval | O-2 | Safe AI-assisted triage |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: NHS England MH Director (SD-1) wants rapid deployment to reduce waiting times, but RCPsych (SD-2) and MHRA (SD-4) require extensive clinical validation and regulatory approval before any clinical use.
  - **Resolution Strategy**: Phase the deployment — immediate deployment for low-risk administrative triage (routing to correct service), with AI-assisted clinical risk assessment introduced only after clinical validation study completion and MHRA regulatory clearance. This delivers waiting time improvements early while clinical safety evidence builds.

- **Conflict 2**: Service Users (SD-3) want fast access to assessment, but also want the right to refuse AI assessment and have a human-only pathway, which could create longer waits for those choosing the human pathway.
  - **Resolution Strategy**: Always offer both pathways with transparent information about expected wait times for each. Digital triage reduces overall system load, benefiting those who choose human assessment too (shorter queues). Frame digital triage as additional capacity, not replacement.

**Synergies**:

- **Synergy 1**: SD-1 (waiting time reduction) and SD-3 (service user access) are fundamentally aligned — faster triage benefits both political reporting and patient experience
- **Synergy 2**: SD-2 (clinical safety) and SD-4 (MHRA compliance) both drive thorough clinical validation, creating a single validation programme serving both needs

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| AI algorithm design | Lead Data Scientist | Clinical Lead | RCPsych, Service Users, AI Ethics | All |
| Clinical safety decisions | Clinical Safety Officer | Clinical Lead | MHRA, CQC | All |
| MHRA regulatory strategy | Regulatory Affairs Lead | SRO | MHRA, Clinical Lead | All |
| Service user engagement | Service User Lead | Service Owner | Mind, Samaritans | All |
| Go/No-go for clinical deployment | SRO | NHS England MH Director | Clinical Lead, MHRA, CSO | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| MHRA AI as Medical Device Guidance | Guidance | MHRA | Classification and regulatory pathway | N/A — external reference |
| NHS Long Term Plan | Strategy | NHS England | Mental health parity of esteem | N/A — external reference |
| NICE Digital Health Technology Standards | Standard | NICE | Evidence standards for digital health | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Mental Health Digital Triage
**Model**: Claude Opus 4.6
