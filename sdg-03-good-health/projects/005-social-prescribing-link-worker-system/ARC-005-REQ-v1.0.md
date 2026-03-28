# Project Requirements: Social Prescribing Link Worker System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Social Prescribing Link Worker System (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Social Prescribing Digital Programme, NHS England |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Social Prescribing Programme Board, NHS England |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

---

## Executive Summary

### Business Context

Social prescribing connects patients with community support for non-clinical needs — loneliness, social isolation, physical inactivity, housing, debt, and mental wellbeing. The NHS Long Term Plan committed to 1,000 social prescribing link workers in Primary Care Networks by 2023/24, subsequently expanded to over 3,500. However, the digital infrastructure supporting social prescribing is fragmented — link workers use spreadsheets, local databases, or incompatible commercial systems. There is no national platform for referral management, community service discovery, or outcome tracking.

The Social Prescribing Link Worker System will provide a national platform connecting GPs, link workers, and community organisations, with integrated referral management, a living community service directory, and outcome measurement aligned with the NASP minimum dataset.

### Objectives

- Provide integrated GP-to-link-worker referral workflow within EMIS and TPP SystmOne
- Maintain a national community service directory with 95%+ accuracy
- Enable link workers to manage caseloads, track patient journeys, and record outcomes via mobile
- Collect NASP minimum dataset for 80%+ of social prescribing referrals
- Support VCSE organisations with simple referral receipt and outcome reporting

### Project Scope

**In Scope**:

- GP referral integration with EMIS Web and TPP SystmOne
- Link worker caseload management (web and mobile)
- National community service directory with local service listings
- VCSE organisation portal for referral management and outcome reporting
- Patient outcome measurement (ONS4 wellbeing, PHQ-2, activity levels)
- NASP minimum dataset collection and reporting
- Referral outcome feedback to GP clinical record

**Out of Scope**:

- Clinical mental health referrals (separate system — Project 002)
- Commissioning and contract management for VCSE organisations
- Patient-facing self-referral (future phase)
- Financial payments to VCSE organisations
- Video consultations between link workers and patients

---

## Business Requirements

### BR-1: GP-Integrated Social Prescribing Referral

**Description**: GPs and primary care staff must be able to create social prescribing referrals from within their clinical system (EMIS, TPP SystmOne) without opening a separate application, with referral outcome visible in the patient record.

**Rationale**: GPs will not use a separate system to make referrals. Integration with the clinical workflow is essential for adoption.

**Success Criteria**:

- Referral created from within EMIS/SystmOne in under 2 minutes
- Referral outcome (attended, completed, declined) visible in GP patient record
- 80%+ of GP practices in participating PCNs using integrated referral within 12 months

**Priority**: MUST_HAVE

---

### BR-2: Community Service Directory

**Description**: The platform must maintain a searchable, accurate directory of community services available for social prescribing, including service description, location, capacity, accessibility information, and contact details.

**Rationale**: Link workers need to find suitable local services for patients. Current directories are outdated, incomplete, and maintained in spreadsheets. An inaccurate directory undermines link worker confidence and wastes patient and link worker time.

**Success Criteria**:

- Directory covers at least 50,000 community services nationally
- 95% accuracy validated through quarterly audits
- Services searchable by location, category, accessibility, and availability
- VCSE organisations can update their own listings

**Priority**: MUST_HAVE

---

### BR-3: Link Worker Caseload Management

**Description**: Link workers must have a mobile-friendly caseload management tool showing their active referrals, patient contact history, upcoming appointments, and outcome tracking.

**Rationale**: Link workers are mobile — they visit patients at home, attend community groups, and work across multiple GP practices. They need a tool that works on a smartphone, not a desktop PC.

**Success Criteria**:

- Full caseload visible on mobile device
- Patient contact notes recorded in under 1 minute
- Outcome measurement tools (ONS4, PHQ-2) completable on mobile
- Offline capability for areas with poor connectivity

**Priority**: MUST_HAVE

---

### BR-4: NASP Minimum Dataset Collection

**Description**: The platform must collect the NASP Social Prescribing Minimum Dataset for all referrals, enabling national outcome analysis and evidence-based policy.

**Rationale**: Without consistent national data, social prescribing cannot demonstrate its value and risks losing NHS funding.

**Success Criteria**:

- NASP minimum dataset fields collected for 80%+ of completed referrals
- Automated pre-population of fields where data is available from GP referral
- National aggregate reporting dashboard for NASP and NHS England

**Priority**: MUST_HAVE

---

### BR-5: VCSE Organisation Simplicity

**Description**: VCSE organisations must be able to receive referrals, confirm attendance, and report basic outcomes through an interface usable on a smartphone by a volunteer with minimal IT skills.

**Rationale**: The VCSE sector ranges from large charities with IT departments to a single volunteer running a weekly walking group from a mobile phone. The platform must work for the smallest community group.

**Success Criteria**:

- Referral notification received via SMS with one-tap confirmation
- Outcome reporting completable in under 2 minutes on a smartphone
- No training required — interface self-explanatory for basic smartphone users
- 90% of VCSE organisations rate as "easy to use"

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Dr Hussain, GP Partner

- **Role**: GP partner in an urban PCN with 15,000 patients
- **Goals**: Refer patients with social needs to link worker quickly, see outcome in patient record
- **Pain Points**: Currently emails link worker or writes on paper, no follow-up, does not know what services are available
- **Technical Proficiency**: High — uses EMIS Web all day

#### Persona 2: Emma, Social Prescribing Link Worker

- **Role**: Link worker covering 3 GP practices in a rural PCN
- **Goals**: Manage 40-patient caseload, find suitable local services, track patient progress, report outcomes
- **Pain Points**: Uses spreadsheet, no mobile tool, directory is an outdated PDF, outcomes collected on paper forms
- **Technical Proficiency**: Medium — comfortable with smartphone apps and basic IT

#### Persona 3: Margaret, Walking Group Volunteer

- **Role**: Retired nurse running a weekly walking group for 8-12 people
- **Goals**: Know when a new referral is coming, confirm attendance, let the link worker know how the patient is doing
- **Pain Points**: Not comfortable with complex IT, has a smartphone but uses it mainly for calls and messaging
- **Technical Proficiency**: Low — uses WhatsApp and basic smartphone functions

---

### Functional Requirements Detail

#### FR-1: EMIS Web Referral Integration

**Description**: The system must integrate with EMIS Web to allow GPs to create social prescribing referrals from within the clinical system, pre-populated with patient demographics and coded reason for referral.

**Acceptance Criteria**:

- [ ] Given a GP using EMIS Web, when they initiate a social prescribing referral, then the referral form opens within the EMIS interface with patient demographics pre-populated
- [ ] Given a referral is submitted, when it reaches the link worker, then it includes patient name, NHS Number, GP practice, coded reason (SNOMED CT), and free-text context
- [ ] Given a referral outcome is recorded by the link worker, when the outcome is updated, then it is written back to the EMIS patient record as a coded entry

**Priority**: MUST_HAVE

---

#### FR-2: TPP SystmOne Referral Integration

**Description**: Equivalent integration with TPP SystmOne for GP practices using that clinical system.

**Acceptance Criteria**:

- [ ] Given a GP using SystmOne, when they initiate a social prescribing referral, then the referral form opens within SystmOne with patient demographics pre-populated
- [ ] Given a referral outcome, when updated, then it is written back to the SystmOne patient record

**Priority**: MUST_HAVE

---

#### FR-3: Community Service Directory Search

**Description**: Link workers must be able to search the community service directory by location (postcode/radius), service category (physical activity, social, creative, nature, practical support), accessibility (wheelchair, sensory, language), and availability.

**Acceptance Criteria**:

- [ ] Given a link worker searches for services, when they enter a postcode and category, then services within 5 miles (configurable) are displayed sorted by distance
- [ ] Given search results, when displayed, then each service shows: name, description, meeting times, location, accessibility, capacity status, and contact details
- [ ] Given a service has no available capacity, when displayed in search results, then it is flagged as "Currently Full" with option to join waiting list

**Priority**: MUST_HAVE

---

#### FR-4: VCSE Organisation Self-Service Listing Management

**Description**: VCSE organisations must be able to register, create, and update their own service listings in the directory.

**Acceptance Criteria**:

- [ ] Given a VCSE organisation registers, when they create a listing, then it is reviewed and published within 3 business days
- [ ] Given a VCSE organisation needs to update availability, when they update their listing, then changes are reflected immediately (no review required for availability updates)
- [ ] Given a service has not been updated for 3 months, when the staleness threshold is reached, then an automatic reminder is sent to the organisation

**Priority**: MUST_HAVE

---

#### FR-5: Link Worker Mobile Caseload Dashboard

**Description**: A mobile-optimised dashboard for link workers showing their active caseload, upcoming appointments, overdue follow-ups, and outcome tracking status.

**Acceptance Criteria**:

- [ ] Given a link worker opens the mobile app, when the dashboard loads, then active cases are displayed with RAG status (Green: on track, Amber: follow-up due, Red: overdue)
- [ ] Given a link worker visits a patient, when they record a contact note, then the note is saved with date, time, and free-text in under 1 minute
- [ ] Given poor mobile connectivity, when the link worker records a note offline, then it syncs when connectivity is restored

**Priority**: MUST_HAVE

---

#### FR-6: Patient Outcome Measurement

**Description**: The system must support collection of patient wellbeing outcomes using validated instruments (ONS4 wellbeing questions, PHQ-2 for mental health screening) at referral, during, and at completion.

**Acceptance Criteria**:

- [ ] Given a patient is referred, when the link worker conducts initial assessment, then ONS4 baseline scores are recorded
- [ ] Given a patient completes social prescribing, when final assessment is conducted, then ONS4 and PHQ-2 are administered and compared to baseline
- [ ] Given outcome data exists, when aggregate reporting runs, then mean wellbeing improvement is calculable per service type, PCN, and region

**Priority**: MUST_HAVE

---

#### FR-7: VCSE Referral Notification and Confirmation

**Description**: VCSE organisations must receive referral notifications via SMS or email and confirm attendance with a single action.

**Acceptance Criteria**:

- [ ] Given a link worker refers a patient to a community group, when the referral is sent, then the VCSE contact receives an SMS with patient first name (no NHS Number), service type, and preferred start date
- [ ] Given the VCSE contact receives the SMS, when they tap "Confirm", then attendance confirmation is recorded and the link worker is notified
- [ ] Given a patient does not attend, when the VCSE contact taps "Did not attend", then the link worker is notified to follow up

**Priority**: MUST_HAVE

---

#### FR-8: NASP Minimum Dataset Reporting

**Description**: The system must generate NASP-compliant aggregate reports from referral and outcome data, providing national, regional, and PCN-level analysis.

**Acceptance Criteria**:

- [ ] Given NASP minimum dataset fields collected, when reporting is run, then aggregate statistics are generated by geography, referral reason, service type, and demographic
- [ ] Given a reporting period, when NASP requests data, then anonymised aggregate data is exportable in the NASP-specified format
- [ ] Given individual referral records, when data is anonymised for reporting, then no patient-identifiable information is included

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-1: Mobile App Performance

**Requirement**: Mobile app pages must load within 2 seconds on a 3G connection. Offline mode must allow note recording and later sync.

**Priority**: HIGH

---

### Availability Requirements

#### NFR-A-1: Availability Target

**Requirement**: 99.9% availability during NHS operating hours (Monday-Friday 8am-6pm). Reduced availability (99.5%) acceptable outside these hours.

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Patient Data Protection

**Requirement**: Patient data shared with link workers is limited to referral-relevant information (name, contact, reason for referral). VCSE organisations receive only first name and service type — no NHS Number, no clinical data. UK GDPR Article 6(1)(e) public task as lawful basis.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Link Worker Authentication

**Requirement**: Link workers authenticate via NHS Identity or employer-issued credentials with MFA. VCSE organisation contacts authenticate via email/SMS verification (lower assurance appropriate for limited data access).

**Priority**: HIGH

---

### Usability Requirements

#### NFR-U-1: VCSE Digital Inclusion

**Requirement**: VCSE-facing interfaces must be usable by volunteers with basic smartphone skills. No training required. Maximum 3 taps to confirm attendance or report an outcome.

**Priority**: CRITICAL

---

#### NFR-U-2: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all interfaces. NHS.UK Design System for NHS-facing components.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: EMIS Web Integration

**Purpose**: GP referral creation and outcome feedback within EMIS clinical system.

**Integration Type**: EMIS Partner API (FHIR R4 Task resource for referrals)

**Priority**: CRITICAL

---

### INT-2: TPP SystmOne Integration

**Purpose**: GP referral creation and outcome feedback within SystmOne clinical system.

**Integration Type**: SystmOne Units API (FHIR R4 Task resource)

**Priority**: CRITICAL

---

### INT-3: PDS Integration

**Purpose**: Patient identity validation for referred patients.

**Integration Type**: FHIR R4 Patient lookup via NHS Number

**Priority**: MUST_HAVE

---

### INT-4: NHS Notify

**Purpose**: SMS and email notifications to link workers and VCSE organisations.

**Integration Type**: NHS Notify API

**Priority**: MUST_HAVE

---

## Data Requirements

### DR-1: Social Prescribing Referral Record

**Description**: Core referral data linking patient, GP, link worker, and community service.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| referral_id | UUID | Yes | Unique referral identifier | Primary key |
| nhs_number | String(10) | Yes | Patient NHS Number | Validated against PDS |
| referring_practice_ods | String | Yes | GP practice ODS code | Validated |
| referral_reason | SNOMED CT | Yes | Coded reason for referral | Social prescribing codes |
| link_worker_id | UUID | Yes | Assigned link worker | Foreign key |
| service_id | UUID | No | Community service referred to | Foreign key to directory |
| status | Enum | Yes | Referral status | referred, accepted, active, completed, declined |
| baseline_ons4 | JSON | No | ONS4 wellbeing baseline scores | 4 integer values 0-10 |
| outcome_ons4 | JSON | No | ONS4 wellbeing outcome scores | 4 integer values 0-10 |

**Data Classification**: OFFICIAL-SENSITIVE (patient-identifiable)

**Data Retention**: 5 years after referral completion

---

### DR-2: Community Service Directory Entry

**Description**: Service listing in the community directory.

**Data Classification**: OFFICIAL (public information)

**Data Retention**: Active while service operates; archived 12 months after closure

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| GP non-clinical consultations | 20-30% of total | 15% reduction | 18 months | GP practice data |
| NASP minimum dataset completion | < 30% | 80%+ | 24 months | Platform analytics |
| VCSE usability rating | N/A | 90% "easy/very easy" | 12 months | Quarterly survey |
| Directory accuracy | Unknown | 95%+ | 12 months | Quarterly audit |
| Patient wellbeing improvement | N/A | Mean 1.5 point ONS4 increase | 18 months | Outcome data |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| NHS Long Term Plan | Strategy | NHS England | Social prescribing commitment | N/A — external reference |
| NASP Framework | Framework | NASP | Minimum dataset, link worker model | N/A — external reference |
| ONS4 Wellbeing Questions | Instrument | ONS | 4 validated wellbeing questions | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Social Prescribing Link Worker System
**Model**: Claude Opus 4.6
