# Project Requirements: Domestic Abuse Case Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Domestic Abuse Case Management (Project 002) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Domestic Abuse Digital Programme, Home Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Home Office VAWG Team, Domestic Abuse Commissioner, MARAC National Coordination (RESTRICTED) |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for a multi-agency domestic abuse case management system. Due to the life-safety nature of this system, security and survivor safety requirements carry MUST_HAVE priority without exception.

---

## Executive Summary

### Business Context

Domestic abuse affects 2.3 million adults in England and Wales annually (ONS Crime Survey). The Domestic Abuse Act 2021 placed the Domestic Abuse Commissioner on a statutory footing and strengthened the multi-agency response framework. However, the technology supporting this response remains fragmented — police, health, social services, housing, and specialist DA services each maintain separate case records with limited information sharing. Multi-Agency Risk Assessment Conferences (MARACs) provide a structured sharing mechanism, but they operate on weekly or fortnightly cycles, creating dangerous delays in high-risk cases.

The Domestic Abuse Case Management system will provide a secure, trauma-informed multi-agency platform enabling real-time risk assessment, coordinated safety planning, and controlled information sharing — while maintaining the highest standards of survivor data protection.

### Objectives

- Enable real-time multi-agency information sharing for high-risk DA cases (within 15 minutes of identification)
- Reduce survivor re-traumatisation by eliminating the need to repeat their story to every agency
- Achieve zero data breaches exposing survivor safety information to perpetrators
- Support MARAC coordination with automated referral and structured information requests
- Provide aggregate analytics for policy development without compromising individual survivor safety

### Project Scope

**In Scope**:

- Multi-agency case management with role-based access
- DASH-RIC digital risk assessment with automated MARAC referral
- Survivor consent management with tiered sharing controls
- Secure information sharing with police, NHS, social services, and specialist DA services
- Safety planning tools with quick-exit and safe-browsing features
- Aggregate anonymised analytics for policy development
- Mobile-accessible interface for frontline workers

**Out of Scope**:

- Perpetrator management systems (separate Home Office programme)
- Family court case management (Ministry of Justice responsibility)
- Refuge accommodation booking (Women's Aid national system)
- Criminal justice case progression

---

## Business Requirements

### BR-1: Multi-Agency Real-Time Information Sharing

**Description**: Enable authorised practitioners across police, health, social services, and specialist DA services to share risk-relevant information about DA cases in real-time, with appropriate legal basis and consent management.

**Rationale**: Domestic Homicide Reviews consistently identify fragmented information as a contributing factor. The Domestic Abuse Act 2021 strengthens the duty on agencies to share information for safeguarding purposes.

**Success Criteria**:

- Information sharing latency reduced from days to 15 minutes for high-risk cases
- All sharing events logged with legal basis, consent status, and audit trail
- At least 75% of MARAC areas using the system within 24 months

**Priority**: MUST_HAVE

---

### BR-2: Survivor Safety as Primary Design Constraint

**Description**: The system must prioritise survivor safety in every design decision, ensuring that no feature, notification, or data-sharing mechanism can be exploited by a perpetrator to discover, locate, or further control a survivor.

**Rationale**: Technology-facilitated abuse is a significant and growing dimension of domestic abuse. Perpetrators monitor devices, intercept communications, and exploit institutional processes to maintain control.

**Success Criteria**:

- Survivor safety impact assessment completed for every feature
- Quick-exit functionality on every page
- No identifying information in URLs, page titles, or browser history
- Safe notification channels verified for each survivor

**Priority**: MUST_HAVE

---

### BR-3: Trauma-Informed User Experience

**Description**: The system must be designed using trauma-informed principles, ensuring that interactions do not re-traumatise survivors or create additional barriers to seeking help.

**Rationale**: Domestic Abuse Commissioner and specialist services (Women's Aid, Refuge) require trauma-informed design as a condition of endorsement.

**Success Criteria**:

- Domestic Abuse Commissioner endorsement obtained
- Women's Aid and Refuge design review passed
- Survivor user research conducted in safe, ethical settings

**Priority**: MUST_HAVE

---

### BR-4: DASH-RIC Digital Risk Assessment

**Description**: The system must support digital completion of the DASH-RIC (Domestic Abuse, Stalking and Honour Based Violence Risk Identification Checklist) with automated scoring and MARAC referral for high-risk cases.

**Rationale**: DASH-RIC is the national standard risk assessment tool. Digital completion enables consistent scoring, automated referral, and time-series analysis of risk escalation.

**Success Criteria**:

- DASH-RIC scores calculated consistently with SafeLives methodology
- High-risk cases automatically referred to MARAC
- Risk score trends visible to case coordinators

**Priority**: MUST_HAVE

---

### BR-5: MARAC Coordination Support

**Description**: The system must support MARAC coordination including meeting scheduling, information requests to agencies, action tracking, and outcome recording.

**Rationale**: MARACs are the primary multi-agency coordination mechanism for high-risk DA cases. Currently, MARAC coordinators manage this through email, spreadsheets, and manual processes.

**Success Criteria**:

- Automated information requests sent to relevant agencies before MARAC
- Action items tracked with responsible agency and completion dates
- MARAC minutes securely recorded and accessible to authorised agencies

**Priority**: MUST_HAVE

---

### BR-6: Aggregate Analytics for Policy Development

**Description**: The system must produce anonymised, aggregate analytics on DA prevalence, risk patterns, service demand, and multi-agency response effectiveness for policy development — without any risk of individual survivor identification.

**Rationale**: The Domestic Abuse Commissioner and Home Office require aggregate data to inform policy. Current data is fragmented and inconsistent across agencies.

**Success Criteria**:

- Aggregate dashboards available to policy teams with no individual-level data access
- Statistical disclosure control preventing identification from aggregate data
- Geographic granularity limited to local authority level minimum

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: PC Aisha — First Response Officer

- **Role**: Police constable responding to a domestic incident call
- **Goals**: Complete DASH-RIC at scene; check for previous incidents; identify children at risk; determine immediate safety actions
- **Pain Points**: No access to health or social services information at scene; paper DASH-RIC form; cannot see previous callout history from other forces
- **Technical Proficiency**: Medium (uses police mobile devices)

#### Persona 2: Maria — MARAC Coordinator

- **Role**: MARAC coordinator managing multi-agency meetings for a local authority area
- **Goals**: Schedule MARACs; request information from agencies; track actions; ensure all high-risk cases are heard; manage repeat referrals
- **Pain Points**: Manages everything via email and spreadsheets; chases agencies for information; no visibility of action completion
- **Technical Proficiency**: Medium

#### Persona 3: Dr. Patel — A&E Clinician

- **Role**: Emergency department consultant who frequently treats patients presenting with injuries consistent with domestic abuse
- **Goals**: Flag safeguarding concerns; check if patient is known to DA services; share relevant clinical information with MARAC when appropriate
- **Pain Points**: Uncertain about legal basis for sharing; no mechanism to check if patient has a MARAC case; time-pressured environment
- **Technical Proficiency**: Medium-High

#### Persona 4: Survivor accessing services (represented through advocacy)

- **Role**: Survivor of domestic abuse seeking support from specialist services
- **Goals**: Get help without having to repeatedly explain situation; feel confident information will not reach the perpetrator; maintain control over what is shared
- **Pain Points**: Has told story to 6+ agencies; fears perpetrator will find out about engagement; feels disempowered by institutional processes
- **Technical Proficiency**: Variable (may be using shared/monitored device)

---

### Functional Requirements Detail

#### FR-1: Digital DASH-RIC Assessment

**Description**: The system must provide a digital DASH-RIC form with automated scoring, risk-level determination (standard/medium/high), and automated referral generation for high-risk cases.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a completed DASH-RIC, when scored, then risk level matches SafeLives scoring methodology
- [ ] Given a high-risk score, then MARAC referral is automatically generated
- [ ] Given a mobile device, then DASH-RIC can be completed at the scene of an incident
- [ ] Given a partially completed DASH-RIC, then progress is saved and can be resumed

**Priority**: MUST_HAVE

---

#### FR-2: Multi-Agency Case Record

**Description**: The system must maintain a consolidated case record accessible to authorised practitioners across participating agencies, showing risk assessments, safety plans, agency involvement, and action items.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a case, then authorised practitioners from any participating agency can view relevant information
- [ ] Given agency-specific information, then access is restricted to practitioners with appropriate role and legal basis
- [ ] Given a case record, then the survivor's core narrative is recorded once and shared (with consent)
- [ ] Given multiple agencies contributing, then all contributions are time-stamped and attributed

**Priority**: MUST_HAVE

---

#### FR-3: Survivor Consent Management

**Description**: The system must implement granular consent management allowing survivors (or their advocates) to control what information is shared, with whom, and for what purpose — with override provisions for imminent risk to life.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a survivor, then they can specify which agencies may access their information
- [ ] Given consent withdrawal, then access is immediately revoked (except for safeguarding overrides)
- [ ] Given imminent risk to life, then mandatory sharing occurs with consent override logged and survivor notified (when safe)
- [ ] Given a survivor unable to consent (e.g., unconscious), then vital interests basis applies with full audit trail

**Priority**: MUST_HAVE

---

#### FR-4: Quick-Exit and Safe Browsing

**Description**: All user-facing pages must include a quick-exit button that immediately navigates to a neutral website, clears the page from browser history (where technically possible), and does not leave identifiable traces.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given any page, then a prominently placed quick-exit button is visible
- [ ] Given quick-exit activation, then browser navigates immediately to a neutral website (e.g., BBC Weather)
- [ ] Given page URLs, then they do not contain terms identifiable as domestic abuse services
- [ ] Given browser page titles, then they do not reveal service purpose

**Priority**: MUST_HAVE

---

#### FR-5: Secure Notification Channels

**Description**: The system must verify safe notification channels for each survivor before sending any communications, with support for non-digital channels where devices may be monitored.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a notification, then the system checks the survivor's safe contact preference before sending
- [ ] Given a monitored device risk, then alternative notification methods are available (via advocate, safe phone, in-person)
- [ ] Given email notifications, then subject lines and sender names do not reveal service purpose
- [ ] Given no safe digital channel, then the system supports in-person notification via caseworker

**Priority**: MUST_HAVE

---

#### FR-6: MARAC Workflow Engine

**Description**: The system must support the full MARAC workflow — referral, information gathering from agencies, meeting management, action assignment, and outcome recording.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a high-risk referral, then information requests are automatically sent to relevant agencies
- [ ] Given a MARAC meeting, then agenda is auto-generated from pending cases with information received
- [ ] Given action items, then responsible agencies receive notifications and deadlines
- [ ] Given repeat referrals, then the system flags the case with escalation guidance

**Priority**: MUST_HAVE

---

#### FR-7: Safety Planning Tools

**Description**: The system must provide safety planning tools that caseworkers can use collaboratively with survivors, with safe storage and controlled access to completed plans.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a case, then caseworkers can create and update safety plans using structured templates
- [ ] Given a safety plan, then it is encrypted at field level and accessible only to the survivor and their designated caseworker
- [ ] Given location information in a safety plan (e.g., refuge address), then this is stored with the highest encryption tier

**Priority**: MUST_HAVE

---

#### FR-8: Aggregate Analytics Dashboard

**Description**: The system must provide anonymised aggregate analytics for policy teams, with strict statistical disclosure control preventing individual identification.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given aggregate data, then no individual survivor can be identified from any published statistic
- [ ] Given geographic analysis, then minimum geographic unit is local authority level
- [ ] Given small cohorts, then cell suppression rules are enforced (minimum 5)
- [ ] Given policy users, then they have no access to individual-level data

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Security Requirements (ALL CRITICAL)

#### NFR-SEC-1: Field-Level Encryption for Survivor Safety Data

**Requirement**: Survivor location data, refuge addresses, safe contact details, and safety plans must be encrypted at field level (not just database-level encryption at rest), using dedicated encryption keys with restricted access.

**Priority**: MUST_HAVE

---

#### NFR-SEC-2: Break-Glass Access with Automatic Alerting

**Requirement**: Emergency access to restricted data must be available via a break-glass mechanism that automatically generates alerts to the system security team and the survivor's caseworker.

**Priority**: MUST_HAVE

---

#### NFR-SEC-3: Access Logging with Anomaly Detection

**Requirement**: All data access must be logged with user identity, role, legal basis, timestamp, and data accessed. Automated anomaly detection must flag unusual access patterns (e.g., a practitioner accessing cases outside their area or role).

**Priority**: MUST_HAVE

---

#### NFR-SEC-4: Zero-Trust Network Architecture

**Requirement**: The system must implement zero-trust network architecture with no implicit trust based on network location. Every request authenticated and authorised regardless of network origin.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-1: 99.95% Availability

**Requirement**: System must achieve 99.95% uptime (26 minutes maximum monthly downtime). This is a life-safety service — unavailability during a crisis could prevent access to a safety plan or risk assessment.

**RTO**: 30 minutes

**RPO**: 5 minutes

**Priority**: MUST_HAVE

---

### Performance Requirements

#### NFR-P-1: Real-Time Response for Frontline Workers

**Requirement**: Case record retrieval and DASH-RIC completion must respond within 2 seconds (p95) to support frontline officers at the scene of an incident.

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-1: Domestic Abuse Act 2021 Compliance

**Requirement**: The system must comply with all data protection provisions of the Domestic Abuse Act 2021 and the Domestic Abuse Statutory Guidance.

**Priority**: MUST_HAVE

---

#### NFR-C-2: MARAC Operating Protocol Compliance

**Requirement**: All MARAC-related workflows must comply with the SafeLives MARAC Operating Protocol.

**Priority**: MUST_HAVE

---

#### NFR-C-3: WCAG 2.2 Level AA Accessibility

**Requirement**: All interfaces must meet WCAG 2.2 Level AA, with additional consideration for users in crisis situations (large touch targets, clear language, minimal cognitive load).

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Integration with Police National Database (PND)

**Purpose**: Enable police practitioners to access previous DA incident records from other forces and contribute new incident records.

**Integration Type**: API-based (PND national API)

**Data Exchanged**: DA incident records, DASH-RIC assessments, suspect/perpetrator flags

**Priority**: MUST_HAVE

---

### INT-2: Integration with NHS Spine/Summary Care Record

**Purpose**: Enable authorised DA practitioners to check for relevant health flags (with appropriate legal basis) and enable clinicians to share safeguarding concerns.

**Integration Type**: NHS API (HL7 FHIR)

**Priority**: SHOULD_HAVE

---

### INT-3: Integration with Local Authority Case Management Systems

**Purpose**: Enable social workers to view DA case information and contribute children's/adults' safeguarding assessments.

**Integration Type**: API-based (standards vary by local authority; adapter pattern required)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity: Case

**Data Classification**: OFFICIAL-SENSITIVE (DA)

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| case_id | UUID | Yes | Unique identifier | Primary key |
| survivor_pseudonym | String(100) | Yes | Non-identifying reference | No real name in core record |
| risk_level | Enum | Yes | Current risk assessment | standard/medium/high |
| dash_ric_score | Integer | No | Latest DASH-RIC score | 0-24 |
| marac_status | Enum | Yes | MARAC referral status | not_referred/referred/active/closed |
| consent_tier | Enum | Yes | Survivor consent level | full/limited/emergency_only |
| agencies_involved | Array(String) | Yes | Participating agencies | Validated against agency registry |

**Data Retention**: Per Home Office retention schedule (minimum 7 years; indefinite for DHR-related cases)

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy to UK sovereign cloud at OFFICIAL-SENSITIVE classification
**TC-2**: Must support integration with 43 police forces with varying IT maturity
**TC-3**: Must work on police mobile devices and NHS clinical workstations

### Assumptions

**A-1**: Police forces will adopt the system through NPCC coordination (risk: individual force opt-out)
**A-2**: NHS information governance frameworks support clinical data sharing for DA safeguarding
**A-3**: The Crime and Disorder Act 1998 s.115 provides adequate legal basis for most sharing scenarios

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Data breaches exposing survivor data | Unknown | Zero | Ongoing |
| MARAC information sharing latency | 7-14 days | 15 minutes (high risk) | 12 months |
| Survivor re-traumatisation (repeat narratives) | 5+ agencies | 1 (core narrative recorded once) | 18 months |
| DA Commissioner endorsement | N/A | Obtained | Before public beta |
| MARAC areas using the system | 0 | 75% (of ~270 areas) | 24 months |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Domestic Abuse Case Management (Project 002)
**Model**: Claude Opus 4.6
