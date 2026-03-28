# Project Requirements: NHS Appointment Booking Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | NHS Appointment Booking Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, NHS Appointment Booking Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NHS Appointment Booking Programme Board, DHSC Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive requirements for the NHS Appointment Booking Platform — a next-generation patient appointment and referral system that provides a single, unified digital service for patients to find, book, change, and cancel NHS appointments across primary and secondary care settings.

---

## Executive Summary

### Business Context

NHS appointment booking is currently fragmented across hundreds of separate systems — individual Trust Patient Administration Systems, GP clinical systems, the e-Referral Service, and various patient portals. This fragmentation creates confusion for patients, generates an estimated GBP 1.2 billion in annual costs from Did Not Attend (DNA) appointments, and prevents efficient appointment utilisation across the NHS.

The NHS Appointment Booking Platform will provide a patient-centred, standards-based booking layer that integrates with existing NHS systems via HL7 FHIR R4 APIs. It will be accessible through the NHS App, NHS.UK website, and telephony channels, giving patients a single place to manage all their NHS appointments.

This platform directly supports SDG 3 (Good Health and Well-Being) by improving access to healthcare services and reducing barriers that prevent patients from receiving timely care.

### Objectives

- Provide a unified patient-facing appointment booking service across primary and secondary care
- Reduce NHS DNA rates by 20%+ through intelligent reminders, easy cancellation, and rebooking
- Integrate with NHS national services (PDS, e-RS, GP Connect, Spine) using HL7 FHIR R4
- Reduce GP practice telephone booking volume by 40% within participating practices
- Comply with DCB0129/DCB0160 clinical safety standards, NHS DSPT, and UK GDPR

### Expected Outcomes

- 15% reduction in average referral-to-appointment waiting time within 18 months
- DNA rate reduced from 6.4% to below 5.0% within 12 months of launch
- GBP 150 million annual operational savings from DNA reduction and administrative efficiency
- 50%+ NHS Trust and GP practice adoption within 18 months
- Patient satisfaction score of 4.2/5 or higher for booking experience

### Project Scope

**In Scope**:

- Patient-facing appointment search, booking, change, and cancellation
- Integration with NHS App and NHS.UK as patient-facing channels
- FHIR R4-based integration with NHS Trust PAS/EPR systems
- GP Connect integration for primary care appointment booking
- e-Referral Service integration for referral-based bookings
- PDS integration for patient identity and demographics
- Multi-channel appointment reminders (SMS, email, push notification, letter)
- Appointment preparation information and pre-attendance instructions
- Accessibility compliance (WCAG 2.2 AA) and assisted digital pathways
- NHS login integration for patient authentication

**Out of Scope**:

- Replacement of Trust PAS or GP clinical systems (integration only)
- Clinical decision support or triage functionality (separate SDG 3 project)
- Video consultation booking (future phase)
- Private healthcare appointment booking
- Prescription management or repeat ordering

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Programme Sponsor | DHSC | Decision maker |
| Service Owner | Service accountability | DHSC | Requirements validation |
| Product Manager | Requirements prioritisation | DHSC Digital | Requirements definition |
| Lead Architect | Technical oversight | NHS England | Architecture decisions |
| Clinical Safety Officer | DCB0129/DCB0160 compliance | NHS England | Clinical safety review |
| DHSC SIRO | Information risk | DHSC | DPIA sign-off |
| Trust CIO Representatives | Integration requirements | NHS Trusts | Technical validation |
| GP Practice Managers | Primary care requirements | GP Practices | User acceptance |
| Patient Representatives | Patient needs | Healthwatch | User research input |

---

## Business Requirements

### BR-1: Unified Patient Appointment Management

**Description**: Patients must be able to find, book, change, and cancel NHS appointments across primary care (GP), secondary care (hospital outpatient), and community services through a single digital service.

**Rationale**: Fragmented booking systems confuse patients, increase DNA rates, and create administrative overhead. A unified service reduces barriers to accessing healthcare.

**Success Criteria**:

- Patients can view all their upcoming NHS appointments in one place
- Patients can book appointments across at least 5 care settings from a single interface
- Patient satisfaction score of 4.2/5 or higher for booking experience

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Patients/Carers (SD-3)

---

### BR-2: DNA Rate Reduction

**Description**: The platform must actively reduce Did Not Attend rates through intelligent reminders, easy cancellation, and real-time rebooking of cancelled slots.

**Rationale**: DNAs cost the NHS GBP 1.2 billion annually and waste clinical capacity. Reducing DNA rates improves access for other patients and releases operational savings.

**Success Criteria**:

- DNA rate reduced from 6.4% to below 5.0% for services using the platform
- 80% of patients receive at least one reminder before their appointment
- Cancelled appointment slots released for rebooking within 15 minutes

**Priority**: MUST_HAVE

**Stakeholder**: HM Treasury (SD-6), Patients/Carers (SD-3)

---

### BR-3: NHS Trust and GP Practice Integration

**Description**: The platform must integrate seamlessly with existing NHS Trust PAS/EPR systems and GP clinical systems without requiring those systems to be replaced.

**Rationale**: NHS Trusts and GP practices have invested significantly in existing systems. The platform must complement, not replace, these systems to achieve adoption.

**Success Criteria**:

- FHIR R4-based integration available for at least 4 major PAS vendors
- GP Connect integration operational for EMIS and TPP SystmOne
- Trust booking rules and clinical pathway logic respected by the platform

**Priority**: MUST_HAVE

**Stakeholder**: NHS Trust CEs (SD-2), GP Practice Managers (SD-5)

---

### BR-4: Operational Efficiency Savings

**Description**: The platform must deliver measurable reductions in NHS administrative costs associated with appointment booking and management.

**Rationale**: GP practices spend significant staff time on telephone booking. Trusts incur costs managing DNAs and appointment rescheduling. Digital efficiency savings support NHS financial sustainability.

**Success Criteria**:

- 40% reduction in telephone booking volume at participating GP practices
- GBP 150 million annual savings across the NHS within 3 years
- Appointment utilisation rate improved by 10% at participating Trusts

**Priority**: SHOULD_HAVE

**Stakeholder**: HM Treasury (SD-6), GP Practice Managers (SD-5)

---

### BR-5: Standards-Based Interoperability

**Description**: The platform must be built on open standards (HL7 FHIR R4 UK Core) and integrate with NHS national services, demonstrating the NHS digital interoperability strategy.

**Rationale**: NHS England's digital strategy mandates FHIR-first interoperability. The platform is a flagship programme that must demonstrate standards-based integration at national scale.

**Success Criteria**:

- All clinical data exchange uses HL7 FHIR R4 UK Core profiles
- APIs registered on the NHS API Catalogue
- Platform integrates with PDS, e-RS, GP Connect, NHS Spine, and NHS login

**Priority**: MUST_HAVE

**Stakeholder**: NHS England CDO (SD-4)

---

### BR-6: Clinical Safety Compliance

**Description**: The platform must comply with DCB0129 and DCB0160 clinical safety standards, with a maintained Clinical Safety Case demonstrating that the system does not introduce unacceptable clinical risk.

**Rationale**: Appointment booking affects patient safety — incorrect prioritisation of urgent referrals, delayed cancer pathway appointments, or lost referral data can cause patient harm.

**Success Criteria**:

- Clinical Safety Officer appointed and active throughout development
- Hazard Log maintained with all identified clinical hazards and mitigations
- DCB0129 and DCB0160 compliance confirmed by independent audit before go-live

**Priority**: MUST_HAVE

**Stakeholder**: Clinical Safety Officer, CQC, Chief Nursing Officer

---

### BR-7: Digital Inclusion and Accessibility

**Description**: The platform must be accessible to all patients including those with disabilities, low digital skills, and limited connectivity, with alternative channels for those who cannot use digital services.

**Rationale**: Health services must not create a two-tier system. Patients who cannot use digital services must not be disadvantaged in accessing appointments.

**Success Criteria**:

- WCAG 2.2 Level AA compliance verified
- Telephone booking maintained as primary alternative channel
- Assisted digital support available through NHS 111 and community organisations
- Service usable on 3G connection with low-specification device

**Priority**: MUST_HAVE

**Stakeholder**: Patients/Carers (SD-3), Healthwatch

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah, GP Patient

- **Role**: 42-year-old working mother, regular GP attendee
- **Goals**: Book GP appointments quickly without calling during the 8am rush, manage family members' appointments, receive reminders
- **Pain Points**: Cannot get through on the phone at 8am, forgets appointment times, different booking system for each family member
- **Technical Proficiency**: Medium — uses NHS App for COVID pass, comfortable with smartphone apps

#### Persona 2: James, Hospital Outpatient

- **Role**: 67-year-old retiree with multiple long-term conditions, attends 4 hospital clinics
- **Goals**: See all upcoming hospital appointments in one view, change appointment times to avoid transport difficulties, understand what to prepare for each visit
- **Pain Points**: Receives appointment letters weeks in advance then forgets, cannot easily change appointment, different Trust portals for different hospitals
- **Technical Proficiency**: Low — uses a basic smartphone, needs large text and simple navigation

#### Persona 3: Dr Patel, GP Partner

- **Role**: GP partner managing a busy urban practice with 12,000 patients
- **Goals**: Reduce telephone booking demand on reception staff, see appointment utilisation data, maintain clinical control over appointment types
- **Pain Points**: 8am telephone surge overwhelms reception, high DNA rate, cannot easily identify underutilised appointment slots
- **Technical Proficiency**: High — uses EMIS Web daily, comfortable with clinical IT systems

---

### Use Cases

#### UC-1: Patient Books GP Appointment Online

**Actor**: Sarah (GP Patient)

**Preconditions**:

- Patient is registered with a GP practice that uses the platform
- Patient has an NHS login account linked to their NHS Number
- GP practice has published available appointment slots via GP Connect

**Main Flow**:

1. Patient opens NHS App and selects "Book an appointment"
2. System displays patient's registered GP practice
3. Patient selects appointment type (routine, urgent, nurse, specific clinician)
4. System queries GP Connect for available slots matching criteria
5. System displays available appointment slots with date, time, and clinician
6. Patient selects preferred slot
7. System confirms booking with GP clinical system via GP Connect
8. System displays confirmation with appointment details, location, and preparation instructions
9. System sends confirmation notification (push notification and/or SMS)

**Postconditions**:

- Appointment created in GP clinical system
- Confirmation sent to patient
- Appointment visible in patient's NHS App appointment list

**Alternative Flows**:

- **Alt 3a**: If no appointments of requested type available, system offers alternative types or next available date
- **Alt 7a**: If GP Connect returns booking failure, system displays error message and suggests telephone booking

**Business Rules**:

- Patient can only book at their registered GP practice for routine appointments
- Urgent same-day appointments limited to one per patient per day
- Advance booking window determined by GP practice configuration (typically 2-4 weeks)

**Priority**: CRITICAL

---

#### UC-2: Patient Cancels and Rebooks Hospital Appointment

**Actor**: James (Hospital Outpatient)

**Preconditions**:

- Patient has an existing hospital outpatient appointment booked through the platform or visible via e-RS
- Patient is authenticated via NHS login

**Main Flow**:

1. Patient opens NHS App and views upcoming appointments
2. Patient selects the hospital appointment to change
3. System displays appointment details and options: Cancel, Change Date/Time
4. Patient selects "Change Date/Time"
5. System queries Trust PAS via FHIR for alternative available slots in the same clinic
6. System displays alternative slots
7. Patient selects new preferred slot
8. System confirms change with Trust PAS
9. System releases original slot for other patients
10. System sends updated confirmation to patient

**Postconditions**:

- Original appointment cancelled in Trust PAS
- New appointment booked in Trust PAS
- Original slot released and available for rebooking
- Updated confirmation sent to patient

**Alternative Flows**:

- **Alt 5a**: If no alternative slots available within acceptable timeframe, offer to join waiting list for cancellations
- **Alt 4a**: If patient selects "Cancel" without rebooking, system confirms cancellation and advises contacting GP if re-referral needed

**Business Rules**:

- Appointment changes must maintain referral pathway continuity (cancer 2WW cannot be moved beyond pathway deadline)
- Minimum 24-hour notice required for cancellation (configurable per Trust)
- Two-week-wait cancer referral appointments flagged with warning if patient attempts to reschedule

**Priority**: CRITICAL

---

#### UC-3: Clinician Reviews Appointment Utilisation Dashboard

**Actor**: Dr Patel (GP Partner)

**Preconditions**:

- Clinician authenticated via NHS CIS2 smartcard
- GP practice has been using the platform for at least 30 days

**Main Flow**:

1. Clinician logs into practice management dashboard
2. System displays appointment utilisation summary for current week
3. Clinician selects date range and appointment type filters
4. System displays: booking rate, DNA rate, cancellation rate, channel split (online vs telephone)
5. Clinician identifies underutilised appointment types
6. Clinician adjusts appointment template based on insights

**Postconditions**:

- Clinician has visibility of booking patterns and utilisation data
- No patient-identifiable data displayed in aggregate dashboard

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-1: Patient Authentication via NHS Login

**Description**: The system must authenticate patients using NHS login (NHS Identity) with identity proofing level P9 for booking and managing appointments.

**Relates To**: BR-1, BR-7, UC-1

**Acceptance Criteria**:

- [ ] Given a patient with an NHS login account at P9 level, when they access the booking service, then they are authenticated via NHS login OAuth 2.0 flow
- [ ] Given a patient without an NHS login account, when they access the service, then they are guided through NHS login registration
- [ ] Given a patient with P5 identity proofing, when they attempt to book, then the system requests identity uplift to P9

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: NHS login API, NHS Identity Service

---

#### FR-2: Appointment Search and Availability Display

**Description**: The system must query appointment availability from GP Connect and Trust FHIR APIs and display available slots to the patient with relevant filtering options.

**Relates To**: BR-1, BR-3, UC-1, UC-2

**Acceptance Criteria**:

- [ ] Given a registered GP patient, when they search for appointments, then the system displays available slots from their practice within the configured booking window
- [ ] Given a hospital outpatient referral, when the patient searches for appointments, then the system displays available slots across eligible Trusts within the referral pathway
- [ ] Given no available slots, when the patient searches, then the system displays the next available date and offers to notify when earlier slots become available

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: GP Connect Appointment Management API, Trust FHIR Scheduling API

---

#### FR-3: Appointment Booking Confirmation

**Description**: The system must confirm appointment bookings with the source clinical system and provide the patient with a confirmation including date, time, location, clinician, and preparation instructions.

**Relates To**: BR-1, UC-1

**Acceptance Criteria**:

- [ ] Given a patient selects an available slot, when the booking is submitted, then the system creates the appointment in the source clinical system and returns confirmation within 5 seconds
- [ ] Given a successful booking, when confirmation is displayed, then it includes appointment date/time, location with directions, clinician name, and any preparation instructions
- [ ] Given a booking fails (slot taken by another patient), when the error occurs, then the system displays a clear message and offers alternative slots

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-4: Appointment Cancellation and Rebooking

**Description**: The system must allow patients to cancel appointments and rebook alternative slots, with the cancelled slot released for other patients in real time.

**Relates To**: BR-2, UC-2

**Acceptance Criteria**:

- [ ] Given a patient with an existing appointment, when they cancel, then the appointment is cancelled in the source clinical system within 30 seconds
- [ ] Given a cancelled appointment slot, when released, then it becomes available for other patients within 15 minutes
- [ ] Given a two-week-wait cancer referral, when the patient attempts to cancel, then the system displays a clinical safety warning and advises contacting the clinical team

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-5: Multi-Channel Appointment Reminders

**Description**: The system must send appointment reminders via patient-selected channels (SMS, email, push notification, letter) at configurable intervals before the appointment.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a patient with a booked appointment, when the reminder interval is reached (default: 7 days, 1 day before), then the system sends a reminder via the patient's preferred channel
- [ ] Given a reminder sent via SMS, when the patient receives it, then it includes appointment date/time, location, and a link to confirm/cancel/change
- [ ] Given a patient who has not confirmed attendance 24 hours before the appointment, when the final reminder is sent, then it offers one-tap cancellation to release the slot

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: NHS Notify service for SMS/email delivery

---

#### FR-6: PDS Integration for Patient Demographics

**Description**: The system must use the Personal Demographics Service as the authoritative source for patient identity and demographics, synchronising patient records via FHIR.

**Relates To**: BR-5, Architecture Principle 9

**Acceptance Criteria**:

- [ ] Given a patient authenticates, when their record is loaded, then demographics are retrieved from PDS using NHS Number
- [ ] Given a PDS record update (address change), when the patient next accesses the service, then updated demographics are reflected
- [ ] Given PDS is temporarily unavailable, when a patient accesses the service, then cached demographics are used with a freshness indicator

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-7: e-Referral Service Integration

**Description**: The system must integrate with the NHS e-Referral Service to display referral-based appointment booking options and maintain referral pathway integrity.

**Relates To**: BR-3, BR-5

**Acceptance Criteria**:

- [ ] Given a patient with an active e-RS referral, when they access the booking service, then the referral-based appointment options are displayed
- [ ] Given a booking made through the platform for an e-RS referral, when confirmed, then the e-RS referral status is updated to "booked"
- [ ] Given a two-week-wait cancer referral, when displayed, then it is visually flagged as urgent with pathway deadline information

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-8: GP Connect Integration

**Description**: The system must integrate with GP Connect Appointment Management FHIR APIs to query availability, book, and cancel appointments at GP practices using EMIS Web and TPP SystmOne.

**Relates To**: BR-3, BR-5, UC-1

**Acceptance Criteria**:

- [ ] Given a GP practice using EMIS Web with GP Connect enabled, when a patient searches for appointments, then available slots are returned via GP Connect FHIR API
- [ ] Given a GP practice using TPP SystmOne, when a patient books an appointment, then the booking is created via GP Connect and visible in SystmOne
- [ ] Given a GP Connect API returns an error, when the patient attempts to book, then a user-friendly error message is displayed with telephone booking as fallback

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-9: Trust FHIR Scheduling Integration

**Description**: The system must integrate with NHS Trust PAS/EPR systems via HL7 FHIR R4 Scheduling resources to query availability, book, and cancel hospital outpatient appointments.

**Relates To**: BR-3, BR-5, UC-2

**Acceptance Criteria**:

- [ ] Given a Trust with a FHIR-enabled PAS, when the platform queries availability, then available outpatient slots are returned using FHIR Schedule and Slot resources
- [ ] Given a patient books a hospital appointment, when confirmed, then the booking is created in the Trust PAS via FHIR and includes patient NHS Number, appointment type, and referring clinician
- [ ] Given a Trust PAS does not support FHIR, when integration is required, then a standards-based adapter is available for legacy HL7v2 messaging

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-10: Appointment Preparation Information

**Description**: The system must display appointment-specific preparation instructions (fasting requirements, documents to bring, directions to department) sourced from Trust or practice configuration.

**Relates To**: BR-1, UC-1

**Acceptance Criteria**:

- [ ] Given an appointment type with preparation requirements, when the booking is confirmed, then preparation instructions are displayed and included in the confirmation message
- [ ] Given a blood test appointment requiring fasting, when preparation is displayed, then the fasting requirement is clearly stated with timeframe
- [ ] Given an appointment at a hospital site, when directions are displayed, then they include department location, parking, and public transport information

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

#### FR-11: Family and Carer Appointment Management

**Description**: The system must allow parents and authorised carers to view and manage appointments for dependants (children under 16, patients with Power of Attorney).

**Relates To**: BR-1, UC-1

**Acceptance Criteria**:

- [ ] Given a parent with linked child records in PDS, when they access the service, then they can view and manage appointments for their children
- [ ] Given a carer with registered Power of Attorney, when they access the service, then they can manage appointments on behalf of the patient
- [ ] Given a young person turns 16, when they next access the service, then parental access is reviewed and the young person has independent access

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-12: Appointment Waiting List Management

**Description**: The system must allow patients to join a waiting list for earlier appointment slots when no suitable slots are currently available.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given no suitable appointment slots available, when the patient requests to join the waiting list, then they are added to a cancellation notification list
- [ ] Given a slot becomes available matching waiting list criteria, when the slot is released, then patients on the waiting list are notified in priority order
- [ ] Given a patient is offered a waiting list slot, when they accept, then the booking is confirmed and they are removed from the waiting list

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Page Load Time

**Requirement**: Patient-facing pages must load within 1.5 seconds at the 95th percentile, including on 3G mobile connections.

**Measurement Method**: Real User Monitoring (RUM) via browser performance API

**Load Conditions**:

- Peak load: 50,000 concurrent users (Monday 8am GP booking surge)
- Average load: 500 appointment bookings per minute
- Data volume: 60 million patient records linked via PDS

**Priority**: CRITICAL

---

#### NFR-P-2: API Response Time

**Requirement**: Backend API responses must complete within 300ms at the 95th percentile for appointment search and booking operations.

**Scalability**: Must handle 3x projected growth over 3 years without architecture change

**Priority**: CRITICAL

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: The patient-facing booking service must achieve 99.95% availability (26 minutes maximum unplanned downtime per month).

- Maximum planned downtime: 4 hours per month during off-peak window (Tuesday 2am-6am)
- Maximum unplanned downtime: 26 minutes per month

**Maintenance Windows**: Tuesday 2:00-6:00 AM GMT for planned maintenance

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO (Recovery Point Objective)**: Zero data loss for confirmed appointment bookings (synchronous replication)

**RTO (Recovery Time Objective)**: 15 minutes for patient-facing booking service

**Backup Requirements**:

- Continuous replication to secondary UK availability zone
- Daily full backup retained for 90 days
- Geographic backup location: Secondary UK sovereign data centre

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Patient Authentication

**Requirement**: All patients must authenticate via NHS login at identity proofing level P9 (verified identity) for appointment booking and management.

**Session Management**:

- Session timeout: 20 minutes of inactivity (NHS standard)
- Absolute session timeout: 4 hours
- Re-authentication required for: cancelling appointments, changing notification preferences

**Priority**: CRITICAL

---

#### NFR-SEC-2: Staff Authentication

**Requirement**: All NHS staff accessing the management dashboard must authenticate via NHS CIS2 smartcard authentication with role-based access control.

**Roles and Permissions**: Aligned with NHS National RBAC model (R8000 series)

**Priority**: CRITICAL

---

#### NFR-SEC-3: Data Encryption

**Requirement**:

- Data in transit: TLS 1.3+ for all connections
- Data at rest: AES-256 encryption for all patient data stores
- Key management: NHS-approved key management solution

**Priority**: CRITICAL

---

#### NFR-SEC-4: Audit Logging

**Requirement**: Comprehensive audit trail for all patient data access, appointment booking, cancellation, and change events.

**Audit Log Contents**:

- Who: User/service identity (NHS Number for patients, NHS CIS2 identity for staff)
- What: Action performed (view, book, cancel, change)
- When: Timestamp (UTC, millisecond precision)
- Where: System component
- Why: Legitimate relationship or purpose

**Log Retention**: 8 years (NHS Records Management Code of Practice)

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: UK GDPR and Health Data Protection

**Applicable Regulations**: UK GDPR (special category health data), Data Protection Act 2018, Common Law Duty of Confidentiality

**Compliance Requirements**:

- [ ] Lawful basis for processing: Public task (Article 6(1)(e)) and health care purposes (Article 9(2)(h))
- [ ] Data subject rights: access, rectification, erasure (subject to clinical retention), portability
- [ ] Privacy notice published on NHS.UK
- [ ] Data breach notification within 72 hours to ICO
- [ ] DPIA completed and approved by Caldicott Guardian

**Data Residency**: UK sovereign data centres only

**Priority**: CRITICAL

---

#### NFR-C-2: NHS Data Security and Protection Toolkit

**Requirement**: The service must complete the NHS DSPT self-assessment with all mandatory assertions met before processing patient data.

**Priority**: CRITICAL

---

#### NFR-C-3: Clinical Safety Standards

**Requirement**: Full compliance with DCB0129 (manufacture) and DCB0160 (deployment) clinical safety standards.

**Clinical Hazards Identified** (preliminary):

- CH-1: Urgent referral not prioritised correctly — patient delay (Severity: Major, Likelihood: Low)
- CH-2: Appointment cancellation not communicated to clinical system — patient thinks appointment exists (Severity: Considerable, Likelihood: Very Low)
- CH-3: Wrong patient booking due to identity mismatch — wrong patient attends (Severity: Major, Likelihood: Very Low)

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all patient-facing interfaces.

**Accessibility Features**:

- [ ] Keyboard navigation for all booking functions
- [ ] Screen reader compatibility (tested with JAWS, NVDA, VoiceOver)
- [ ] High contrast mode
- [ ] Adjustable font sizes (up to 200% without loss of function)
- [ ] Alt text for all images and icons
- [ ] BSL video for key booking instructions

**Priority**: CRITICAL

---

#### NFR-U-2: NHS.UK Design System Compliance

**Requirement**: All patient-facing interfaces must use the NHS.UK Design System components and patterns.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Integration with NHS Personal Demographics Service (PDS)

**Purpose**: Retrieve and validate patient identity and demographics using NHS Number as the primary identifier.

**Integration Type**: Real-time FHIR R4 API

**Data Exchanged**:

- **From PDS to Platform**: Patient demographics (name, address, DoB, NHS Number, GP registration)
- **From Platform to PDS**: No writes (read-only consumer)

**Authentication**: NHS CIS2 mutual TLS

**SLA**: 99.9% availability, < 200ms response time

**Priority**: CRITICAL

---

### INT-2: Integration with NHS e-Referral Service (e-RS)

**Purpose**: Access referral-based appointment booking options and maintain referral pathway status.

**Integration Type**: Real-time API (e-RS FHIR interface)

**Data Exchanged**:

- **From e-RS to Platform**: Active referrals, available services, booking options
- **From Platform to e-RS**: Booking confirmations, cancellations, rebooking

**Authentication**: NHS CIS2

**SLA**: 99.5% availability, < 500ms response time

**Priority**: CRITICAL

---

### INT-3: Integration with GP Connect

**Purpose**: Query GP appointment availability, create bookings, and cancel appointments at GP practices.

**Integration Type**: Real-time FHIR R4 API (GP Connect Appointment Management)

**Data Exchanged**:

- **From GP System to Platform**: Available appointment slots, booking confirmations
- **From Platform to GP System**: Booking requests, cancellation requests

**Authentication**: Spine mutual TLS with JWT assertions

**SLA**: 99.5% availability, < 300ms response time

**Priority**: CRITICAL

---

### INT-4: Integration with NHS Notify

**Purpose**: Send appointment reminders, confirmations, and notifications to patients via SMS, email, and letter.

**Integration Type**: Asynchronous API

**Data Exchanged**:

- **From Platform to NHS Notify**: Notification requests (recipient, template, personalisation)
- **From NHS Notify to Platform**: Delivery status callbacks

**Authentication**: API key with IP allowlisting

**SLA**: 99.9% availability, SMS delivery within 60 seconds

**Priority**: MUST_HAVE

---

### INT-5: Integration with NHS Spine

**Purpose**: National service bus for PDS, e-RS, and other national service connectivity.

**Integration Type**: MESH messaging and Spine Core FHIR endpoints

**Authentication**: HSCN network connectivity with mutual TLS

**SLA**: 99.9% availability

**Priority**: CRITICAL

---

## Data Requirements

### DR-1: Patient Appointment Record

**Description**: Core appointment data entity linking patients to booked appointments.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| appointment_id | UUID | Yes | Unique appointment identifier | Primary key |
| nhs_number | String(10) | Yes | Patient NHS Number | Validated against PDS |
| appointment_type | SNOMED CT code | Yes | Clinical appointment type | SNOMED CT coded |
| status | Enum | Yes | Appointment status | booked, cancelled, attended, DNA |
| start_datetime | DateTime | Yes | Appointment start time | UTC, ISO 8601 |
| end_datetime | DateTime | Yes | Appointment end time | UTC, ISO 8601 |
| location_ods_code | String(10) | Yes | ODS code for provider | Validated against ODS |
| practitioner_sds_id | String | No | SDS identifier for clinician | When clinician-specific |
| source_system | String | Yes | Originating system identifier | FHIR endpoint URL |
| referral_id | UUID | No | Linked e-RS referral | When referral-based |
| created_at | DateTime | Yes | Record creation timestamp | UTC, ISO 8601 |

**Data Classification**: OFFICIAL-SENSITIVE (patient-identifiable health data)

**Data Retention**: 8 years after last appointment (NHS Records Management Code)

**HL7 FHIR Mapping**: Maps to FHIR R4 Appointment resource (UK Core profile)

---

### DR-2: Appointment Notification Record

**Description**: Record of notifications sent to patients for appointment reminders and confirmations.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| notification_id | UUID | Yes | Unique notification identifier | Primary key |
| appointment_id | UUID | Yes | Linked appointment | Foreign key |
| nhs_number | String(10) | Yes | Patient NHS Number | Validated |
| channel | Enum | Yes | Notification channel | sms, email, push, letter |
| template_id | String | Yes | NHS Notify template | NHS Notify template reference |
| sent_at | DateTime | Yes | Timestamp sent | UTC |
| delivery_status | Enum | Yes | Delivery status | pending, delivered, failed, bounced |

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 2 years

---

### DR-3: Audit Event Record

**Description**: Immutable audit trail of all data access and appointment transactions.

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 8 years (immutable storage)

**HL7 FHIR Mapping**: Maps to FHIR R4 AuditEvent resource

---

### Data Quality Requirements

**Data Accuracy**: NHS Number validated against PDS before any booking; SNOMED CT codes validated against NHS TRUD terminology server

**Data Completeness**: All mandatory appointment fields enforced at API level; incomplete bookings rejected

**Data Consistency**: PDS as single source of truth for demographics; appointment status reconciled with source clinical systems hourly

**Data Timeliness**: Real-time booking confirmation; appointment availability refreshed at minimum every 5 minutes

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with NHS Spine via HSCN network; public internet connectivity not permitted for backend NHS service integration

**TC-2**: Must use NHS-approved cloud infrastructure with UK sovereignty guarantees

**TC-3**: Must use NHS.UK Design System for patient-facing interfaces; no custom design frameworks

**TC-4**: Must support NHS CIS2 for staff authentication; cannot implement alternative staff identity

### Business Constraints

**BC-1**: Go-live target of Q4 2027 aligned with Ministerial commitment

**BC-2**: Total programme budget capped at GBP 25 million over 3 years

**BC-3**: Must use NHS Notify for patient notifications; cannot build bespoke notification infrastructure

### Assumptions

**A-1**: Major PAS vendors (Cerner, Epic, System C) will deliver FHIR Scheduling API support within the programme timeline

**A-2**: GP Connect Appointment Management API will remain supported and maintained by NHS England

**A-3**: NHS login adoption will continue to grow, reaching 40+ million registered users by launch

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| DNA rate | 6.4% | < 5.0% | 12 months post-launch | NHS Hospital Activity Statistics |
| Referral-to-appointment wait | 56 days | 48 days | 18 months post-launch | NHS RTT statistics |
| GP telephone booking volume | ~60% of bookings | < 36% of bookings | 12 months post-launch | GP practice telephony data |
| Annual NHS savings | GBP 0 | GBP 150M | 3 years post-launch | NHS costing data |
| Patient satisfaction | N/A | 4.2/5 | 6 months post-launch | In-app survey |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.95% | Uptime monitoring |
| API response time (p95) | < 300ms | APM tooling |
| Page load time (p95) | < 1.5s | Real User Monitoring |
| Error rate | < 0.1% | Log aggregation |
| FHIR conformance | 100% UK Core compliance | FHIR validation tooling |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| Service Owner | Service accountability | [ ] Approved | PENDING | |
| Lead Architect | Technical oversight | [ ] Approved | PENDING | |
| Clinical Safety Officer | Clinical safety | [ ] Approved | PENDING | |
| DHSC SIRO | Information risk | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|------------|
| DNA | Did Not Attend — patient who fails to attend a booked appointment |
| e-RS | Electronic Referral Service — NHS national referral booking system |
| GP Connect | NHS Digital API platform for GP system integration |
| PDS | Personal Demographics Service — national patient demographics master |
| PAS | Patient Administration System — Trust-level patient management system |
| FHIR | Fast Healthcare Interoperability Resources — HL7 health data standard |
| DSPT | Data Security and Protection Toolkit — NHS security self-assessment |
| DCB0129 | Clinical risk management standard for health IT manufacture |
| DCB0160 | Clinical risk management standard for health IT deployment |
| SNOMED CT | Systematized Nomenclature of Medicine Clinical Terms |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HL7 FHIR R4 UK Core | Standard | HL7 UK | FHIR profiles for UK health data | N/A — external reference |
| GP Connect Specification | Standard | NHS Digital | GP appointment booking API | N/A — external reference |
| NHS.UK Design System | Standard | NHS Digital | Frontend component library | N/A — external reference |
| DCB0129 | Standard | NHS Digital | Clinical risk management | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: NHS Appointment Booking Platform
**Model**: Claude Opus 4.6
