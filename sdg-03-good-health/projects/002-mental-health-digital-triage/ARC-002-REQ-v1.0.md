# Project Requirements: Mental Health Digital Triage

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Mental Health Digital Triage (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Mental Health Digital Triage, NHS England |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Mental Health Digital Triage Programme Board, NHS England Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Mental Health Digital Triage system — an AI-assisted mental health assessment and routing platform that provides immediate triage for people seeking mental health support, routing them to the most appropriate level of care while maintaining the highest clinical safety standards.

---

## Executive Summary

### Business Context

One in four adults in England experiences a mental health condition each year, yet only 25% receive treatment. IAPT services have waiting times exceeding 18 weeks in some areas. Mental health crisis services face increasing demand, with many people presenting at A&E because they cannot access timely community mental health support. The mental health workforce shortage means that clinical capacity cannot grow fast enough to meet demand through traditional assessment pathways alone.

The Mental Health Digital Triage system will use validated clinical assessment instruments (PHQ-9, GAD-7, AUDIT, PCL-5) combined with AI-assisted risk stratification to provide immediate triage, routing individuals to the right level of care — from self-help resources to urgent crisis intervention. The system augments clinical capacity; it does not replace clinical judgement.

### Objectives

- Provide immediate digital triage for people seeking mental health support (< 15 minutes to complete)
- Reduce IAPT referral-to-assessment waiting time by 40%
- Achieve 99.9% sensitivity for high-risk detection (suicide, self-harm, psychosis)
- Route patients to the appropriate level of care based on clinical evidence
- Comply with MHRA AI as Medical Device requirements, DCB0129/DCB0160, and UK GDPR

### Project Scope

**In Scope**:

- Digital self-assessment using validated clinical instruments
- AI-assisted risk stratification and care pathway routing
- Integration with IAPT referral systems
- Crisis escalation pathway with immediate handoff to crisis teams
- Clinician review dashboard for AI-assisted triage results
- Patient safety net — automatic escalation for incomplete or concerning assessments

**Out of Scope**:

- Ongoing therapeutic interventions (CBT, counselling)
- Medication prescribing or management
- Inpatient mental health bed management
- Children and young people's mental health (separate service)
- Replacement of face-to-face clinical assessment (augmentation only)

---

## Business Requirements

### BR-1: Immediate Digital Mental Health Triage

**Description**: People seeking mental health support must be able to complete a digital triage assessment within 15 minutes, available 24/7, that routes them to the appropriate level of care.

**Rationale**: Current assessment pathways require face-to-face appointments with waiting times of weeks. Digital triage provides immediate initial assessment, accelerating access to support.

**Success Criteria**:

- 90% of users complete the digital assessment within 15 minutes
- Triage available 24 hours a day, 7 days a week, 365 days a year
- Triage result provided immediately upon completion

**Priority**: MUST_HAVE

---

### BR-2: Clinical Safety — High-Risk Detection

**Description**: The system must detect individuals at high risk of suicide, self-harm, or acute psychosis with 99.9% sensitivity and immediately escalate to clinical crisis teams.

**Rationale**: Missing a high-risk individual in digital triage could result in serious patient harm or death. Clinical safety is the overriding requirement.

**Success Criteria**:

- 99.9% sensitivity for high-risk categorisation
- Immediate escalation to crisis team within 5 minutes of high-risk detection
- Zero unmitigated false negatives in prospective clinical validation study

**Priority**: MUST_HAVE

---

### BR-3: Algorithmic Fairness and Bias Elimination

**Description**: The AI risk stratification must demonstrate statistically equivalent accuracy across all protected characteristics, with independent audit evidence published before deployment.

**Rationale**: Mental health outcomes already vary significantly across ethnic groups, socioeconomic backgrounds, and genders. An AI system that perpetuates or amplifies existing biases is clinically and ethically unacceptable.

**Success Criteria**:

- < 2% accuracy variance across age, sex, ethnicity, and disability groups
- Independent algorithmic bias audit completed and published
- Service user advisory group endorsement of fairness approach

**Priority**: MUST_HAVE

---

### BR-4: MHRA Regulatory Compliance

**Description**: The system must comply with MHRA requirements for AI/ML as a Medical Device, including pre-market evidence, clinical investigation, and post-market surveillance.

**Rationale**: An AI system that makes clinical risk assessments may be classified as a medical device by the MHRA. Regulatory non-compliance could result in enforcement action and patient safety risk.

**Success Criteria**:

- MHRA classification confirmed and, if applicable, conformity assessment completed
- Clinical investigation evidence package submitted and accepted
- Post-market surveillance plan in operation from day one of clinical use

**Priority**: MUST_HAVE

---

### BR-5: Human Assessment Option

**Description**: All users must have the option to request a human-only assessment pathway at any point during the digital triage process, with clear information about expected wait times for each option.

**Rationale**: Service user organisations and the Royal College of Psychiatrists require that digital triage never becomes a mandatory gateway. People in mental distress must feel in control of their assessment pathway.

**Success Criteria**:

- "Speak to a person" option visible at every stage of digital assessment
- Human assessment pathway wait time displayed alongside digital pathway
- At least 15% of users choosing human pathway (indicating genuine choice, not forced digital)

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Aisha, Self-Referral for Anxiety

- **Role**: 28-year-old university researcher experiencing worsening anxiety
- **Goals**: Get an initial assessment quickly, understand her options, access IAPT talking therapy
- **Pain Points**: Waited 14 weeks for IAPT last time, anxiety makes phone calls difficult, wants control over when she engages
- **Technical Proficiency**: High — comfortable with digital health tools

#### Persona 2: Mark, Crisis Presentation

- **Role**: 45-year-old construction worker experiencing suicidal thoughts after relationship breakdown
- **Goals**: Get help urgently, does not want to go to A&E, reluctant to speak to anyone face-to-face
- **Pain Points**: Stigma about mental health, does not know where to go for help, fears being sectioned
- **Technical Proficiency**: Medium — uses smartphone but not familiar with health apps

#### Persona 3: Dr Okonkwo, IAPT Clinical Lead

- **Role**: Clinical psychologist leading IAPT service in a large urban Trust
- **Goals**: Triage incoming referrals more efficiently, ensure high-risk cases are identified early, reduce assessment DNA rates
- **Pain Points**: Overwhelmed by referral volume, cannot assess patients quickly enough, high-risk cases sometimes not identified until first appointment
- **Technical Proficiency**: High — uses clinical IT systems daily

---

### Functional Requirements Detail

#### FR-1: Validated Clinical Assessment Instruments

**Description**: The system must administer validated clinical assessment instruments (PHQ-9 for depression, GAD-7 for anxiety, AUDIT for alcohol, PCL-5 for PTSD) using clinically validated digital formats.

**Relates To**: BR-1, UC-1

**Acceptance Criteria**:

- [ ] Given a user begins triage, when the assessment starts, then the PHQ-9 is administered as the initial screening instrument
- [ ] Given a PHQ-9 score indicating moderate depression (10-14), when the assessment continues, then additional instruments are offered based on clinical pathway logic
- [ ] Given any instrument response indicating suicidal ideation (PHQ-9 Q9 score >= 1), when detected, then immediate risk assessment pathway is triggered

**Priority**: MUST_HAVE

---

#### FR-2: AI-Assisted Risk Stratification

**Description**: The system must use a clinically validated AI/ML model to stratify risk level based on assessment responses, demographic context, and clinical indicators, categorising into: Crisis (immediate), Urgent (24-hour), Routine (standard pathway), Self-Help (guided resources).

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given assessment responses, when the AI model processes them, then a risk category is assigned with confidence score
- [ ] Given a Crisis risk categorisation, when assigned, then automatic escalation to crisis team occurs within 5 minutes
- [ ] Given any risk categorisation, when presented to the clinician review dashboard, then the AI reasoning is explainable (factors contributing to the categorisation are listed)

**Priority**: MUST_HAVE

---

#### FR-3: Crisis Escalation Pathway

**Description**: When the system detects an individual at immediate risk, it must immediately escalate to NHS crisis services with all relevant assessment data, while maintaining engagement with the individual.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a Crisis risk categorisation, when escalation is triggered, then the system sends assessment data to the local crisis team via secure MESH message within 2 minutes
- [ ] Given escalation is in progress, when the user is on-screen, then the system displays supportive messaging, Samaritans contact details (116 123), and confirmation that help is being arranged
- [ ] Given a crisis escalation, when 5 minutes have elapsed without crisis team acknowledgement, then automatic escalation to the on-call consultant psychiatrist occurs

**Priority**: MUST_HAVE

---

#### FR-4: Clinician Review Dashboard

**Description**: The system must provide IAPT and crisis clinicians with a dashboard showing all triage results, AI risk categorisations with explanations, and tools to review, override, or confirm the AI assessment.

**Relates To**: BR-2, UC-3

**Acceptance Criteria**:

- [ ] Given a clinician accesses the dashboard, when they view a triage result, then the AI risk categorisation, confidence score, and contributing factors are displayed
- [ ] Given a clinician disagrees with the AI categorisation, when they override it, then the override is recorded with the clinician's rationale for model improvement
- [ ] Given multiple pending triage results, when the dashboard is viewed, then results are sorted by risk level (Crisis first, then Urgent, then Routine)

**Priority**: MUST_HAVE

---

#### FR-5: IAPT Referral Integration

**Description**: The system must integrate with IAPT referral management systems to automatically create referrals for patients triaged to IAPT-appropriate pathways, pre-populated with assessment data.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a Routine risk categorisation suggesting IAPT suitability, when the referral is created, then assessment scores (PHQ-9, GAD-7) and triage summary are automatically populated
- [ ] Given a referral is created, when it reaches the IAPT system, then it complies with the IAPT Minimum Data Set requirements
- [ ] Given a patient is already known to IAPT services, when triaged, then the existing IAPT record is linked

**Priority**: MUST_HAVE

---

#### FR-6: Patient Safety Net — Incomplete Assessments

**Description**: The system must monitor for incomplete assessments and concerning patterns (repeated access without completion, escalating scores across sessions) and trigger clinician review.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a user abandons the assessment after completing PHQ-9 Q9 (suicidal ideation question) with a score >= 1, when abandonment is detected, then a safety net alert is generated for clinical review
- [ ] Given a user completes the assessment 3 times in 7 days with escalating scores, when the pattern is detected, then a clinician alert is generated
- [ ] Given a safety net alert, when generated, then it appears on the clinician dashboard within 5 minutes with full context

**Priority**: MUST_HAVE

---

#### FR-7: Human Assessment Pathway Option

**Description**: Users must be able to opt out of digital assessment at any point and be routed to a human assessment pathway with clear wait time information.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a user at any stage of digital assessment, when they select "Speak to a person", then they are presented with human assessment options (telephone, video, face-to-face) and expected wait times
- [ ] Given the user selects telephone assessment, when the request is submitted, then a callback is scheduled within the clinical team's SLA
- [ ] Given a user switches from digital to human pathway, when assessment data exists, then it is made available to the assessing clinician (with user consent)

**Priority**: MUST_HAVE

---

#### FR-8: Multilingual and Accessible Assessment

**Description**: The assessment must be available in multiple languages and accessible formats, including Easy Read, audio, and British Sign Language (BSL).

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a user selects a non-English language, when the assessment is presented, then clinically validated translations of PHQ-9, GAD-7, and other instruments are used
- [ ] Given a user selects Easy Read format, when the assessment is presented, then simplified language with supporting images is used
- [ ] Given a user requires BSL, when the assessment is presented, then BSL video translations of each question are available

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-1: Assessment Response Time

**Requirement**: Assessment page transitions must complete within 1 second at the 95th percentile.

**Rationale**: Users in mental distress have limited patience and concentration. Slow responses increase abandonment.

**Priority**: CRITICAL

---

#### NFR-P-2: Crisis Escalation Time

**Requirement**: From high-risk detection to crisis team notification must complete within 2 minutes (p99).

**Priority**: CRITICAL

---

### Availability Requirements

#### NFR-A-1: 24/7 Availability

**Requirement**: The digital assessment service must achieve 99.99% availability (4.4 minutes maximum unplanned downtime per month). Mental health crises do not observe office hours.

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Mental Health Data Protection

**Requirement**: Mental health assessment data is classified as OFFICIAL-SENSITIVE and is special category data under UK GDPR Article 9. Enhanced access controls must restrict access to authorised mental health clinicians only.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Anonymised Data for AI Training

**Requirement**: AI model training must use only de-identified data processed through NHS Digital's Trusted Research Environment model. No patient-identifiable data in training datasets.

**Priority**: CRITICAL

---

### Compliance Requirements

#### NFR-C-1: MHRA AI as Medical Device

**Requirement**: Full compliance with MHRA Software as a Medical Device and AI/ML guidance. Clinical investigation evidence required before deployment.

**Priority**: CRITICAL

---

#### NFR-C-2: Clinical Safety Standards

**Requirement**: Full compliance with DCB0129 (manufacture) and DCB0160 (deployment). Clinical Safety Case Report approved before clinical use.

**Priority**: CRITICAL

---

#### NFR-C-3: UK GDPR Article 22 — Automated Decision-Making

**Requirement**: Compliance with UK GDPR Article 22 regarding automated decision-making that produces legal or similarly significant effects. The system must not make autonomous clinical decisions — AI categorisation must be reviewed by a clinician before clinical action is taken, except for Crisis escalation where immediate human intervention is initiated.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Trauma-Informed Design

**Requirement**: The assessment interface must follow trauma-informed design principles — language must be gentle, non-judgmental, and empowering. Users must feel in control of the process at all times.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Integration with IAPT Case Management Systems

**Purpose**: Automatically create and populate IAPT referrals with assessment data.

**Integration Type**: Asynchronous via NHS MESH and/or FHIR R4

**Priority**: CRITICAL

---

### INT-2: Integration with NHS Crisis Resolution Teams

**Purpose**: Immediate escalation of high-risk triage results to local crisis teams.

**Integration Type**: Real-time notification via secure API with MESH fallback

**Priority**: CRITICAL

---

### INT-3: Integration with PDS

**Purpose**: Patient identity verification using NHS Number.

**Integration Type**: Real-time FHIR R4 API

**Priority**: CRITICAL

---

## Data Requirements

### DR-1: Assessment Response Data

**Description**: Individual question responses from validated clinical instruments (PHQ-9, GAD-7, etc.).

**Data Classification**: OFFICIAL-SENSITIVE (mental health special category data)

**Data Retention**: 8 years (NHS Records Management Code — mental health records)

**HL7 FHIR Mapping**: FHIR R4 QuestionnaireResponse resource

---

### DR-2: AI Risk Categorisation Output

**Description**: AI model output including risk category, confidence score, contributing factors, and model version.

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 8 years (clinical decision audit trail)

**Explainability**: Contributing factors stored for clinical review and model audit

---

### DR-3: Clinician Override Records

**Description**: Records of clinician overrides of AI categorisation, including override rationale.

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 8 years

**Purpose**: Model improvement training data (after de-identification) and clinical governance audit

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| IAPT assessment wait | 28 days | 17 days | 12 months | IAPT MDS reporting |
| High-risk sensitivity | N/A | 99.9% | Pre-deployment | Clinical validation study |
| Assessment completion rate | N/A | 85% | 6 months | Platform analytics |
| User satisfaction | N/A | 4.0/5 | 6 months | Post-assessment survey |
| Algorithmic bias variance | N/A | < 2% | Pre-deployment | Independent audit |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| MHRA AI as Medical Device | Guidance | MHRA | Regulatory classification | N/A — external reference |
| PHQ-9 Validation | Clinical Evidence | Kroenke et al. | Depression screening validity | N/A — external reference |
| NICE Digital Health Standards | Standard | NICE | Evidence tiers for digital health | N/A — external reference |
| DCB0129 | Standard | NHS Digital | Clinical risk management | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Mental Health Digital Triage
**Model**: Claude Opus 4.6
