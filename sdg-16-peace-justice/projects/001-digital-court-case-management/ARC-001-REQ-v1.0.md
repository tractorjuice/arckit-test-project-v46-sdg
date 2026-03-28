# Project Requirements: Digital Court Case Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Digital Court Case Management (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, HMCTS Digital Court Case Management |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | HMCTS Reform Programme Board, HMCTS Digital, CDDO, Judicial Office, CPS |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Digital Court Case Management system. It provides a comprehensive specification to guide architecture design, development, procurement, and testing activities within the HMCTS Reform Programme.

---

## Executive Summary

### Business Context

The Crown Court backlog exceeds 67,000 cases, with defendants waiting over two years for trial in some jurisdictions. The existing case management landscape is fragmented across legacy systems (Libra for magistrates' courts, XHIBIT for Crown Court, and various bespoke systems for tribunals) that do not interoperate effectively. The HMCTS Reform Programme (GBP 1.3 billion) has delivered individual digital services but lacks an integrated, end-to-end digital case management capability.

This project delivers a modern, integrated digital case management system that supports case progression from first hearing to disposal across criminal, civil, and family jurisdictions. The system integrates with the Common Platform for cross-agency case data sharing with CPS, police, HMPPS, and defence practitioners.

### Objectives

- Reduce Crown Court case backlog by 20% within 18 months through improved case progression tracking and scheduling optimisation
- Eliminate duplicate data entry across HMCTS, CPS, and defence practitioner systems through Common Platform integration
- Provide judges with digital case management tools that support active case management duties under the Criminal Procedure Rules
- Enable court users (including litigants in person) to access case information and receive proactive notifications through self-service channels
- Achieve GDS service assessment pass at Beta and Live

### Expected Outcomes

- 25% reduction in average time from charge to Crown Court trial completion (52 weeks to 39 weeks)
- 30% reduction in cracked and ineffective trial rate through better case readiness tracking
- 80% judicial user satisfaction score within 6 months of deployment
- 90% task completion rate for litigant in person self-service journeys
- Zero duplicate data entry for case data shared with CPS via Common Platform

### Project Scope

**In Scope**:

- End-to-end case management for criminal cases (magistrates' and Crown Court)
- Case listing and scheduling with judicial approval workflows
- Common Platform integration for CPS case file exchange
- Defence practitioner portal for case access and document filing
- Citizen-facing case status and notification service
- Judicial case management dashboard and tools
- Integration with legal aid status (LAA), custody status (HMPPS), and police evidence systems

**Out of Scope**:

- Civil and family court case management (Phase 2)
- Tribunal case management (separate programme)
- Sentencing guidelines calculator (Sentencing Council responsibility)
- Court building management and facilities
- Jury management system (separate HMCTS service)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| HMCTS CEO | Executive Sponsor | HMCTS | Decision maker |
| SRO, HMCTS Reform | Programme Sponsor | HMCTS | Decision maker |
| HMCTS Service Owner | Product accountability | HMCTS | Requirements definition |
| HMCTS CDIO | Technical oversight | HMCTS Digital | Architecture decisions |
| Lord Chief Justice | Judicial leadership | Judiciary | Judicial requirements approval |
| Senior Presiding Judge | Circuit deployment | Judicial Office | Judicial workflow validation |
| CPS Digital Director | Integration partner | CPS | Common Platform requirements |
| Bar Council representative | Practitioner requirements | Bar Council | Defence practitioner workflows |
| Law Society representative | Solicitor requirements | Law Society | Solicitor workflows |
| Victims' Commissioner | Victim experience | Independent | Victim notification requirements |
| HMCTS SIRO | Security oversight | HMCTS | Security and data requirements |
| LAA Integration Lead | Legal aid integration | LAA | Integration requirements |

---

## Business Requirements

### BR-1: End-to-End Digital Case Progression

**Description**: The system must enable end-to-end digital tracking and management of criminal cases from first hearing through to disposal, replacing paper-based case files and manual tracking processes.

**Rationale**: The current fragmented landscape of legacy systems prevents effective case progression tracking, contributing to the 67,000-case Crown Court backlog. Digital case management enables proactive identification of cases at risk of delay.

**Success Criteria**:

- 100% of criminal cases tracked digitally from first hearing to disposal
- Case progression milestones visible to all authorised parties in real-time
- Automated alerts for cases approaching statutory time limits or overdue milestones

**Priority**: MUST_HAVE

**Stakeholder**: HMCTS CEO, Lord Chancellor

---

### BR-2: Judicial Case Management Support

**Description**: The system must provide judges and magistrates with digital tools that support their active case management duties under the Criminal Procedure Rules, while preserving full judicial discretion over all decisions.

**Rationale**: Criminal Procedure Rules impose a duty on courts to actively manage cases. Judges need information to identify cases requiring attention. The system must support — not constrain — judicial decision-making (see Stakeholder Driver SD-2).

**Success Criteria**:

- Judges can view their entire caseload with priority indicators at a glance
- Case management directions can be recorded and tracked digitally
- System provides advisory information only — all decisions remain with the judge
- No individual judicial performance metrics generated

**Priority**: MUST_HAVE

**Stakeholder**: Lord Chief Justice, Senior Presiding Judge

---

### BR-3: Cross-Agency Digital Case File Exchange

**Description**: The system must exchange case file data with CPS, police, and defence practitioners through the Common Platform, eliminating duplicate data entry and ensuring data consistency across the criminal justice system.

**Rationale**: Duplicate data entry wastes professional time and introduces inconsistency. Poor case file quality is a major contributor to cracked and ineffective trials, directly impacting the backlog (see Stakeholder Driver SD-4).

**Success Criteria**:

- Zero duplicate data entry for case data shared between HMCTS and CPS
- Case file data consistent across all systems within 5 minutes of update
- Defence practitioners can access case materials through a single portal

**Priority**: MUST_HAVE

**Stakeholder**: CPS, Bar Council, Law Society

---

### BR-4: Citizen-Facing Case Information and Notifications

**Description**: The system must provide court users (defendants, witnesses, victims, litigants in person) with self-service access to case information and proactive notifications about hearing dates, changes, and outcomes.

**Rationale**: Citizens currently have limited visibility into case progress, often relying on solicitors or phone calls to the court. Litigants in person (40% of civil/family users) are particularly underserved. Proactive notifications reduce unnecessary court attendance and citizen anxiety (see Stakeholder Driver SD-6).

**Success Criteria**:

- Citizens can check case status online without phoning the court
- Proactive notifications sent for hearing dates, changes, and outcomes via preferred channel
- 90% task completion rate for litigant in person self-service journeys
- Notifications in plain language at appropriate reading level

**Priority**: MUST_HAVE

**Stakeholder**: Court users, Victims' Commissioner, Citizens Advice

---

### BR-5: Operational Efficiency and Backlog Reduction

**Description**: The system must deliver measurable operational efficiency gains that contribute to reducing the Crown Court backlog, including optimised scheduling, reduced administrative overhead, and improved case readiness tracking.

**Rationale**: The GBP 1.3 billion HMCTS Reform Programme investment must demonstrate value for money through measurable efficiency gains. The Crown Court backlog is a political priority requiring urgent improvement (see Stakeholder Drivers SD-1, SD-3).

**Success Criteria**:

- 20% reduction in Crown Court backlog within 18 months
- 25% reduction in average charge-to-trial time
- 30% reduction in cracked and ineffective trial rate
- 15% reduction in court staff time on administrative tasks

**Priority**: MUST_HAVE

**Stakeholder**: Lord Chancellor, HMCTS CEO, HM Treasury

---

## Functional Requirements

### User Personas

#### Persona 1: Judge / Magistrate

- **Role**: Presiding judicial officer
- **Goals**: Manage caseload efficiently, ensure fair and timely justice, maintain oversight of case progression
- **Pain Points**: Paper-based case files, no single view of caseload, difficulty tracking overdue case management directions
- **Technical Proficiency**: Medium (varies significantly across judiciary)

#### Persona 2: Court Legal Adviser / Clerk

- **Role**: Legal adviser to magistrates, case administration
- **Goals**: Prepare cases for hearing, record outcomes, manage case progression, advise magistrates
- **Pain Points**: Multiple systems, manual data entry, inconsistent case file quality
- **Technical Proficiency**: Medium-High

#### Persona 3: Defence Practitioner (Barrister/Solicitor)

- **Role**: Legal representative for defendant
- **Goals**: Access case materials efficiently, file documents, check listings, manage multi-court caseload
- **Pain Points**: Multiple logins, desktop-only access, duplicate data entry, poor listing information
- **Technical Proficiency**: Medium (varies; some sole practitioners have limited IT support)

#### Persona 4: Litigant in Person

- **Role**: Unrepresented court user
- **Goals**: Understand the process, check hearing dates, submit documents, know what to expect
- **Pain Points**: Legal jargon, complex processes, no professional guidance, digital exclusion
- **Technical Proficiency**: Low-Medium

#### Persona 5: Listing Officer

- **Role**: Court scheduling and listing
- **Goals**: Optimise court utilisation, balance judicial availability with case readiness, minimise adjournments
- **Pain Points**: Manual scheduling, limited visibility of case readiness, late changes
- **Technical Proficiency**: High

---

### Use Cases

#### UC-1: Record Case Outcome After Hearing

**Actor**: Court Legal Adviser

**Preconditions**:

- Hearing has concluded
- Legal adviser has authority to record the outcome for this court

**Main Flow**:

1. Legal adviser selects the case from the day's court list
2. System displays the case details and hearing information
3. Legal adviser records the hearing outcome (verdict, sentence, adjournment, directions)
4. System validates the outcome against business rules (e.g., sentencing range validation)
5. Legal adviser confirms and submits the outcome
6. System updates case status across all integrated systems via Common Platform
7. System triggers notifications to relevant parties (defendant, victim, witnesses, CPS, defence)

**Postconditions**:

- Case outcome recorded with timestamp and court legal adviser identity
- Case status updated in Common Platform
- Notifications queued for delivery

**Alternative Flows**:

- **Alt 1a**: If outcome requires judicial sign-off (e.g., complex directions), system routes to judge for approval
- **Alt 2a**: If outcome affects custody status, system triggers HMPPS notification

**Priority**: CRITICAL

---

#### UC-2: Judge Reviews Case Management Dashboard

**Actor**: Judge

**Preconditions**:

- Judge is authenticated with judicial credentials
- Judge has cases assigned to their list

**Main Flow**:

1. Judge opens the case management dashboard
2. System displays all assigned cases with priority indicators (overdue directions, approaching time limits, trial-ready status)
3. Judge selects a case requiring attention
4. System displays the full case summary, case management history, and outstanding directions
5. Judge records a case management direction (e.g., set timetable, request further information)
6. System records the direction and notifies relevant parties

**Postconditions**:

- Case management direction recorded with judicial identity and timestamp
- Parties notified of new direction with compliance deadline
- Case priority indicators updated

**Priority**: CRITICAL

---

#### UC-3: Litigant in Person Checks Case Status

**Actor**: Litigant in Person

**Preconditions**:

- Litigant has a case reference number or authenticated account

**Main Flow**:

1. Litigant accesses the case status service via GOV.UK
2. System prompts for case reference number or authenticated login
3. System displays case status in plain language (next hearing date, location, what to prepare)
4. Litigant optionally signs up for notifications
5. System confirms notification preferences

**Alternative Flows**:

- **Alt 1a**: If litigant cannot find their case reference, system provides guidance on how to obtain it
- **Alt 2a**: If case has reporting restrictions, system displays only information permitted for public access

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-1: Case Registration and Initiation

**Description**: System must support registration of new cases from all entry points (police charge, summons, committal, transfer, appeal).

**Relates To**: BR-1, UC-1

**Acceptance Criteria**:

- [ ] Given a police charge sheet, when a case is registered, then a unique case reference is generated and the case appears in the court listing
- [ ] Given a committal from magistrates' court, when the case is transferred to Crown Court, then all case history and documents transfer automatically
- [ ] Given a case with multiple defendants, when registered, then each defendant is linked to the case with individual progression tracking

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: Common Platform integration (INT-1)

---

#### FR-2: Case Progression Tracking

**Description**: System must track case progression through defined milestones from first hearing to disposal, with automated alerts for overdue milestones and approaching statutory time limits.

**Relates To**: BR-1, BR-5, UC-2

**Acceptance Criteria**:

- [ ] Given a case in progress, when a milestone becomes overdue, then an alert is generated for the responsible party and the listing officer
- [ ] Given a custody case, when custody time limits are approaching, then the system alerts the listing officer and judge 14 days before expiry
- [ ] Given a case management direction, when the compliance deadline passes without action, then an automated chaser is sent to the non-compliant party

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: FR-1 (case registration)

---

#### FR-3: Judicial Case Management Dashboard

**Description**: System must provide judges with a dashboard showing their complete caseload with priority indicators, overdue items, and case readiness status.

**Relates To**: BR-2, UC-2

**Acceptance Criteria**:

- [ ] Given a judge with assigned cases, when they open the dashboard, then all cases are displayed with priority colour coding (red: overdue, amber: approaching deadline, green: on track)
- [ ] Given a case with overdue directions, when displayed on the dashboard, then the specific overdue items are highlighted with days overdue
- [ ] Given the dashboard, when a judge selects a case, then the full case summary, chronology, and outstanding actions are displayed within 2 seconds

**Priority**: MUST_HAVE
**Complexity**: MEDIUM
**Dependencies**: FR-2 (progression tracking)

---

#### FR-4: Court Listing and Scheduling

**Description**: System must support court listing officers in scheduling hearings, managing judicial availability, estimating hearing duration, and optimising court utilisation.

**Relates To**: BR-5, UC-2

**Acceptance Criteria**:

- [ ] Given available courtrooms and judicial sitting days, when a hearing needs scheduling, then the system suggests optimal hearing slots based on case readiness, judicial availability, and courtroom suitability
- [ ] Given a scheduled hearing, when a listing change is required, then all parties are notified automatically via their preferred channel
- [ ] Given court utilisation data, when the system generates reports, then listing officers can identify underutilised courts and scheduling inefficiencies

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: FR-1, FR-2, INT-1

---

#### FR-5: Document Management and Digital Case File

**Description**: System must support creation, upload, storage, and retrieval of case documents as part of a digital case file, with version control and access controls based on party role.

**Relates To**: BR-1, BR-3, UC-1

**Acceptance Criteria**:

- [ ] Given a case file, when a document is uploaded by any party, then it is virus-scanned, stored securely, and made available to authorised parties only
- [ ] Given document access controls, when a defence practitioner accesses the case file, then they see only documents disclosed to the defence
- [ ] Given a document with reporting restrictions, when accessed, then the restriction is clearly displayed and the access is logged

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: INT-1 (Common Platform), NFR-SEC-3 (encryption)

---

#### FR-6: Citizen Case Status and Notifications

**Description**: System must provide citizens with self-service access to case status and send proactive notifications about hearing dates, changes, and outcomes through multiple channels.

**Relates To**: BR-4, UC-3

**Acceptance Criteria**:

- [ ] Given a court user with a valid case reference, when they check case status, then the current status, next hearing date, and required actions are displayed in plain language
- [ ] Given a hearing date change, when the change is confirmed, then all affected parties are notified within 1 hour via their preferred channel (email, SMS, letter)
- [ ] Given a litigant in person, when they access the service, then guided help explains each stage of the process with links to support services

**Priority**: MUST_HAVE
**Complexity**: MEDIUM
**Dependencies**: INT-3 (GOV.UK Notify)

---

#### FR-7: Defence Practitioner Portal

**Description**: System must provide defence practitioners (barristers and solicitors) with a mobile-responsive portal for accessing case materials, filing documents, and managing their multi-court caseload.

**Relates To**: BR-3, UC-2

**Acceptance Criteria**:

- [ ] Given a defence practitioner, when they log in, then they see all their active cases across all courts with next hearing dates
- [ ] Given a case file, when a practitioner accesses it on a mobile device, then documents are readable and key actions are performable
- [ ] Given multiple cases in different courts on the same day, when the practitioner views their schedule, then a unified daily view shows all hearings with timing and location

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM
**Dependencies**: FR-5 (document management), INT-1 (Common Platform)

---

#### FR-8: Reporting and Management Information

**Description**: System must generate management information reports on case volumes, progression times, backlog trends, cracked/ineffective trial rates, and court utilisation.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given authorised management users, when they access reports, then current backlog count, trend, and projection are available in real-time
- [ ] Given a reporting period, when cracked and ineffective trial data is requested, then reasons for cracked/ineffective trials are categorised and presented
- [ ] Given the system, when generating reports, then no individual judicial performance data is identifiable (aggregate only)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM
**Dependencies**: FR-2 (progression data)

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**: Web page load time below 2 seconds at 95th percentile. API response time below 500ms at 95th percentile. Case search results returned within 1 second.

**Load Conditions**:

- Peak load: 15,000 concurrent users (judges, court staff, practitioners during morning listing)
- Average load: 5,000 concurrent users during court sitting hours (09:00-17:00)
- Data volume: 5 million active cases, 50 million historical cases

**Priority**: CRITICAL

---

#### NFR-P-2: Throughput

**Requirement**: System must handle 500 case outcome recordings per minute at peak (end-of-day batch from magistrates' courts). Must support 10,000 notification deliveries per hour.

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: 99.9% uptime during court sitting hours (Monday-Friday, 08:00-18:00). 99.5% uptime outside court hours.

- Maximum planned downtime: 4 hours per month, outside court sitting hours only
- Maximum unplanned downtime during sitting hours: 15 minutes per incident

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: 5 minutes (maximum data loss for case records)
**RTO**: 30 minutes during court sitting hours, 4 hours outside

**Backup Requirements**:

- Continuous replication to secondary UK data centre
- Daily encrypted backups retained for 7 years (court records retention)
- Geographic backup within UK sovereign infrastructure

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: Multi-factor authentication for all judicial and administrative users. Single sign-on integration with HMCTS staff identity provider and professional body credentials (Bar Council, Law Society).

**Session Management**:

- Session timeout: 30 minutes inactivity for administrative users, 60 minutes for judicial users (longer hearings)
- Re-authentication required for recording case outcomes and accessing sensitive documents

**Priority**: CRITICAL

---

#### NFR-SEC-2: Authorisation

**Requirement**: Role-based access control with granular permissions based on role (judge, court staff, prosecutor, defence practitioner, citizen) and case involvement. Defence practitioners can only access cases where they are on record.

**Priority**: CRITICAL

---

#### NFR-SEC-3: Data Encryption

**Requirement**: TLS 1.3+ for all data in transit. AES-256 encryption at rest for all data stores. Application-level encryption for witness protection data and special measures information.

**Priority**: CRITICAL

---

#### NFR-SEC-4: Audit Logging

**Requirement**: Immutable audit log of all case data access and modifications. Logs must record who, what, when, where, and why for every case record interaction. Audit logs retained for 7 years minimum.

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: Data Protection Compliance

**Applicable Regulations**: UK GDPR, Data Protection Act 2018, court data retention schedules, Public Records Act 1958

**Compliance Requirements**:

- [ ] Data subject rights implemented (subject to legal exemptions for court records)
- [ ] Privacy notices published for all citizen-facing services
- [ ] Data Protection Impact Assessment completed and approved by HMCTS SIRO
- [ ] Data retained according to court retention schedules (criminal case records: minimum 7 years, serious crime: 30+ years)

**Priority**: CRITICAL

---

#### NFR-C-2: Open Justice Compliance

**Requirement**: System must support the principle of open justice — court listings, hearing outcomes, and published judgments must be accessible to the public and media unless subject to reporting restrictions.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all user interfaces. Easy Read summaries available for key citizen-facing content.

**Accessibility Features**:

- [ ] Keyboard navigation for all functions
- [ ] Screen reader compatibility (tested with JAWS and NVDA)
- [ ] High contrast mode
- [ ] Adjustable font sizes
- [ ] Plain language at reading age 9-11 for citizen-facing content
- [ ] Welsh language support for Wales courts

**Priority**: CRITICAL

---

#### NFR-U-2: Mobile Responsiveness

**Requirement**: Defence practitioner portal and citizen-facing services must be fully functional on mobile devices (phones and tablets). Judicial dashboard should be optimised for tablet use in courtrooms.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Integration with Common Platform

**Purpose**: Bi-directional case data exchange between HMCTS case management and the Common Platform for CPS, police, and defence access.

**Integration Type**: Real-time API (RESTful) with event-driven notifications for case updates

**Data Exchanged**:

- **To Common Platform**: Case outcomes, hearing dates, judicial directions, listing changes
- **From Common Platform**: CPS case files, prosecution evidence, police charge data, defence representation details

**Authentication**: OAuth 2.0 with mutual TLS
**SLA**: API response time below 500ms at p95, 99.9% availability during court hours
**Priority**: CRITICAL

---

### INT-2: Integration with Legal Aid Agency (LAA)

**Purpose**: Real-time legal aid status checking to confirm defendant representation status for court hearings.

**Integration Type**: Real-time API (RESTful)

**Data Exchanged**:

- **To LAA**: Legal aid status query (defendant identifier, case reference)
- **From LAA**: Legal aid grant status, assigned solicitor, representation order details

**Authentication**: OAuth 2.0
**SLA**: API response time below 300ms at p95
**Priority**: HIGH

---

### INT-3: Integration with GOV.UK Notify

**Purpose**: Multi-channel notification delivery to court users (email, SMS, letter).

**Integration Type**: API (RESTful)

**Data Exchanged**:

- **To GOV.UK Notify**: Notification requests with recipient details, template ID, and personalisation data

**Authentication**: API key
**SLA**: Notification delivery within 1 hour of request
**Priority**: MUST_HAVE

---

### INT-4: Integration with HMPPS (Prison and Probation)

**Purpose**: Exchange defendant custody status and sentence information.

**Integration Type**: Event-driven (asynchronous)

**Data Exchanged**:

- **To HMPPS**: Sentencing outcomes, remand decisions, bail conditions
- **From HMPPS**: Custody status, prison location, release dates

**Priority**: HIGH

---

## Data Requirements

### Data Entities

#### Entity 1: Case

**Description**: A legal case being managed through the court system.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| case_reference | String(20) | Yes | Unique case reference (URN format) | Primary key, immutable |
| jurisdiction | Enum | Yes | Court jurisdiction | ['magistrates', 'crown', 'civil', 'family'] |
| case_type | Enum | Yes | Type of case | ['indictable', 'either_way', 'summary', 'appeal'] |
| status | Enum | Yes | Current case status | ['active', 'adjourned', 'disposed', 'archived'] |
| court_centre | String(10) | Yes | Court centre code | Foreign key to court reference data |
| created_at | Timestamp | Yes | Case creation timestamp | Indexed, immutable |

**Data Volume**: 5 million active cases, 50 million historical cases
**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Criminal cases: minimum 7 years from disposal; serious crime: 30+ years

---

#### Entity 2: Hearing

**Description**: A scheduled or completed court hearing within a case.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| hearing_id | UUID | Yes | Unique hearing identifier | Primary key |
| case_reference | String(20) | Yes | Parent case reference | Foreign key to Case |
| hearing_type | Enum | Yes | Type of hearing | ['plea', 'trial', 'sentence', 'mention', 'directions'] |
| scheduled_date | Date | Yes | Scheduled hearing date | Indexed |
| courtroom | String(10) | No | Courtroom identifier | Foreign key to court rooms |
| judge_id | String(20) | No | Assigned judge identifier | Foreign key to judicial users |
| outcome | Enum | No | Hearing result | ['adjourned', 'convicted', 'acquitted', 'dismissed', 'committed'] |

**Data Volume**: 20 million hearings per year
**Data Classification**: OFFICIAL-SENSITIVE

---

### Data Migration Requirements

**Migration Scope**: Active cases from XHIBIT (Crown Court) and Libra (magistrates' courts). Historical cases to be archived with read-only access.

**Migration Strategy**: Phased migration by court circuit, with parallel running during transition.

**Data Validation**: Automated reconciliation comparing case counts and hearing counts between legacy and new system, with manual review for discrepancies above 0.1%.

**Rollback Plan**: Legacy systems maintained in read-only mode for 12 months post-migration, with reactivation capability.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with Common Platform APIs as they currently exist — cannot mandate Common Platform changes
**TC-2**: Must deploy on UK sovereign cloud infrastructure (Crown Hosting or approved UK cloud provider)
**TC-3**: Must comply with HMCTS technology standards and approved technology stack

### Business Constraints

**BC-1**: Court operations must not be disrupted during migration — phased rollout by court circuit mandatory
**BC-2**: Budget capped within HMCTS Reform Programme approved allocation
**BC-3**: Must achieve GDS service assessment pass at Beta before wider rollout

### Assumptions

**A-1**: Common Platform APIs will be stable and performant at the required throughput
**A-2**: Judicial users will have access to suitable devices in courtrooms (tablets or laptops)
**A-3**: Defence practitioners will adopt digital case file access if usability is adequate

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Crown Court backlog | 67,000 cases | 54,000 cases | 18 months | HMCTS statistics |
| Average charge-to-trial time | 52 weeks | 39 weeks | 18 months | Case management data |
| Cracked/ineffective trial rate | 40% | 28% | 12 months | Court outcome data |
| Duplicate data entry incidents | ~60% of data re-entered | 0% via Common Platform | 12 months | System analytics |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability (court hours) | 99.9% | Uptime monitoring |
| API response time (p95) | < 500ms | APM tooling |
| Error rate | < 0.1% | Log aggregation |
| Deployment frequency | Weekly | CI/CD metrics |
| Mean time to recovery (MTTR) | < 15 minutes | Incident tracking |

### User Adoption Metrics

| Metric | Target | Timeline | Measurement Method |
|--------|--------|----------|-------------------|
| Judicial adoption rate | 90% | 12 months post-deploy | System analytics |
| Judicial satisfaction score | 80% | 6 months post-deploy | Survey |
| LiP task completion rate | 90% | 12 months post-deploy | Web analytics |
| Practitioner portal adoption | 75% | 12 months post-deploy | System analytics |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| Common Platform API stability | Stable APIs for case data exchange | HMCTS/CPS | Q2 2026 | At Risk | HIGH — no integration without stable APIs |
| Courtroom device provisioning | Tablets/laptops for judges in courtrooms | HMCTS Ops | Q3 2026 | On Track | HIGH — judicial adoption blocked |
| LAA API availability | Legal aid status checking API | LAA | Q3 2026 | On Track | MEDIUM — manual workaround available |
| HMPPS integration | Custody status exchange | HMPPS Digital | Q4 2026 | On Track | MEDIUM — manual notification continues |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Common Platform integration delays | HIGH | HIGH | Early integration testing, fallback to manual data transfer | HMCTS CDIO |
| R-2 | Judicial rejection of digital case files | MEDIUM | HIGH | Co-design with judiciary, phased adoption, paper fallback | SRO |
| R-3 | Data migration quality issues | MEDIUM | HIGH | Automated reconciliation, manual review, extended parallel running | Data Migration Lead |
| R-4 | Court sitting hours availability constraints | MEDIUM | MEDIUM | Deploy updates outside court hours, zero-downtime deployment pattern | Platform Team |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| HMCTS CEO | Executive Sponsor | [ ] Approved | PENDING | |
| Service Owner | Product accountability | [ ] Approved | PENDING | |
| HMCTS CDIO | Enterprise Architect | [ ] Approved | PENDING | |
| HMCTS SIRO | Security | [ ] Approved | PENDING | |
| Judicial Office | Judicial requirements | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| Common Platform | Cross-CJS digital case management platform shared by HMCTS and CPS |
| Cracked Trial | A trial that does not proceed on the day because a plea is entered or the case is otherwise resolved |
| Ineffective Trial | A trial that cannot proceed on the day due to failures in case preparation |
| LiP | Litigant in Person — a court user without legal representation |
| URN | Unique Reference Number for a criminal case |
| XHIBIT | Legacy Crown Court case management and display system |
| Libra | Legacy magistrates' court case management system |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 16 Architecture Principles
- ARC-001-STKE-v1.0 — Digital Court Case Management Stakeholder Analysis
- HMCTS Reform Programme Business Case
- Criminal Procedure Rules 2020 (as amended)

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Court Case Management
**Model**: Claude Opus 4.6
