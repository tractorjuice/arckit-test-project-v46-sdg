# Project Requirements: Universal Credit Modernisation

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Universal Credit Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Universal Credit Modernisation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | UC Modernisation Programme Board, DWP Digital, CDDO, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Universal Credit Modernisation programme. It provides a comprehensive specification traceable to the stakeholder analysis (ARC-001-STKE-v1.0) and architecture principles (ARC-000-PRIN-v1.0), and forms the basis for solution design, procurement, and acceptance testing. UC processes GBP 36B+ annually for approximately 6 million households; requirements reflect this scale and criticality.

---

## Executive Summary

### Business Context

Universal Credit is the UK's single largest welfare programme, consolidating six legacy benefits into one monthly payment for working-age adults. The current digital platform, while operational, has accumulated significant technical debt since its original deployment. Processing times for new claims average 23 working days, claimant satisfaction sits at 68%, and the system struggles under surge demand as demonstrated during the COVID-19 pandemic when claims increased 7x in weeks.

The modernisation programme will replace the legacy claims processing engine, introduce real-time eligibility assessment, and deliver a mobile-first claimant experience aligned to the GDS Service Standard. The programme must maintain uninterrupted payment operations throughout — any disruption to payments for 6 million households would be a programme-ending event with immediate human consequences.

This requirements specification is informed by the stakeholder drivers analysis (ARC-001-STKE-v1.0), which identified twelve key stakeholder drivers ranging from Ministerial demand for visible improvement to HMRC's need for reliable data exchange.

### Objectives

- Reduce average new claim processing time from 23 working days to 10 working days by March 2028
- Achieve 85% claimant satisfaction (currently 68%) through simplified, accessible digital journeys
- Support 9 million concurrent monthly users with sub-2-second page load times
- Enable policy rule changes to be deployed within 2 weeks without full system redeployment
- Deliver interoperability with HMRC RTI, local authority housing systems, and devolved administration platforms
- Achieve WCAG 2.2 Level AA compliance across all claimant-facing interfaces

### Expected Outcomes

- GBP 180M annual operational savings through automation of manual assessment processes
- 56% reduction in claimant contact centre calls ("where is my claim?")
- 95%+ assessment accuracy on first calculation, reducing mandatory reconsiderations
- Zero unplanned payment disruptions during migration
- GDS service assessment pass at Beta and Live gates

### Project Scope

**In Scope**:

- New claims processing engine with configurable rules engine
- Claimant-facing digital service (GOV.UK integrated, mobile-first)
- Work Coach and Service Centre agent tooling
- HMRC Real Time Information (RTI) integration modernisation
- Local authority housing costs data exchange
- Scottish choices and devolved policy configuration
- GOV.UK Notify integration for claimant communications
- GOV.UK Pay integration for advances and alternative payments

**Out of Scope**:

- Legacy benefit migration (JSA, ESA, Tax Credits) — separate programme
- Sanctions and compliance regime redesign — policy change, not technology
- Jobcentre Plus physical estate changes
- Work Programme / Employability provider systems (interface only)
- Pension Credit and State Pension systems

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| Secretary of State for Work and Pensions | Executive Sponsor | DWP | Decision maker — Ministerial oversight |
| DWP Permanent Secretary | Accounting Officer | DWP | Decision maker — spend controls |
| SRO, UC Modernisation | Programme Sponsor | DWP | Requirements approval |
| DWP CDIO | Technical Authority | DWP Digital | Architecture governance |
| UC Service Owner | Service Accountability | DWP | Requirements definition |
| UC Operations Director | Operational Delivery | DWP | Operational readiness |
| DWP SIRO | Information Risk | DWP | DPIA sign-off |
| HMRC RTI Programme Lead | Integration Partner | HMRC | RTI interface specification |
| CDDO Assessment Lead | Standards Assurance | Cabinet Office | GDS Service Standard |
| Citizens Advice Policy Lead | Claimant Advocacy | Citizens Advice | User research input |
| Claimant representatives | End Users | Citizens | User acceptance |

---

## Business Requirements

### BR-001: Uninterrupted Benefit Payments During Modernisation

**Description**: The modernisation programme must maintain continuous, accurate benefit payments to all 6 million UC households throughout the transition period, with zero unplanned payment disruptions.

**Rationale**: UC payments are the primary income source for millions of vulnerable households. Any disruption causes immediate hardship — inability to pay rent, buy food, or heat homes. This is the single most critical requirement (ref: SD-3 — UC Operations Director).

**Success Criteria**:

- Zero unplanned payment disruptions affecting more than 0.01% of claimants
- Payment accuracy maintained at 95%+ throughout transition
- Rollback capability exercised and proven before each migration phase

**Priority**: MUST_HAVE

**Stakeholder**: UC Operations Director (SD-3), Secretary of State (SD-1)

---

### BR-002: Reduced Claim Processing Time

**Description**: Reduce average new claim processing time from 23 working days to 10 working days, enabling claimants to receive their first payment faster.

**Rationale**: The current processing time, combined with the five-week wait policy, creates severe financial hardship for new claimants. Faster processing is the most impactful improvement the programme can deliver (ref: SD-1, SD-6).

**Success Criteria**:

- Average new claim processing time of 10 working days or fewer by March 2028
- Assessment accuracy maintained at 95%+ (speed must not compromise accuracy)
- 50% reduction in advance payment requests (proxy for reduced hardship during processing)

**Priority**: MUST_HAVE

**Stakeholder**: UC Service Owner (Goal G-1), Secretary of State (SD-1), Claimants (SD-6)

---

### BR-003: Improved Claimant Satisfaction

**Description**: Achieve 85% claimant satisfaction with the UC digital service, measured through transaction-level satisfaction surveys aligned to GDS measurement framework.

**Rationale**: Claimant satisfaction at 68% is below the GDS benchmark. Improved satisfaction demonstrates that modernisation is delivering for citizens (ref: SD-1, SD-6, SD-12).

**Success Criteria**:

- 85% satisfaction score on GDS-standard transaction survey by March 2028
- Net Promoter Score improvement from current baseline
- 40% reduction in complaints to DWP and ICE (Independent Case Examiner)

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Claimants (SD-6), Citizens Advice (SD-12)

---

### BR-004: Policy Agility

**Description**: Enable policy rule changes (eligibility criteria, payment calculations, thresholds, tapers) to be configured and deployed within 2 weeks without full system redeployment.

**Rationale**: UC policy changes frequently — annual uprating, Budget announcements, emergency measures (e.g., COVID uplift). Currently, policy changes require months of development. A configurable rules engine enables DWP to respond to policy at pace (ref: SD-4, SD-11).

**Success Criteria**:

- Annual uprating changes deployed within 5 working days of confirmation
- New policy rules testable in isolation before production deployment
- Devolved policy variations (Scottish choices) configurable without codebase forking

**Priority**: MUST_HAVE

**Stakeholder**: DWP CDIO (SD-4), Devolved Administrations (SD-11)

---

### BR-005: Demonstrable Value for Money

**Description**: Deliver measurable operational savings of GBP 180M per year by Year 3 through automation of manual assessment processes, reduced error rates, and channel shift.

**Rationale**: HM Treasury requires evidence-based benefits realisation to justify the investment. The programme must demonstrate value for money to satisfy the Accounting Officer and survive NAO scrutiny (ref: SD-2, SD-5).

**Success Criteria**:

- GBP 180M annual savings quantified and independently verified by Year 3
- Benefits realisation tracked quarterly against baselined metrics
- Cost per claim processed reduced by 40%

**Priority**: MUST_HAVE

**Stakeholder**: HM Treasury (SD-5), DWP Permanent Secretary (SD-2)

---

### BR-006: Cross-Departmental Data Interoperability

**Description**: Enable seamless, standards-based data exchange with HMRC (earnings), local authorities (housing costs), and devolved administrations (Scottish choices, Scottish Child Payment).

**Rationale**: UC assessment accuracy depends on timely, accurate data from partner organisations. Current batch-based data exchange introduces delays and errors (ref: SD-7, SD-10, SD-11).

**Success Criteria**:

- HMRC RTI data available within 24 hours of employer submission (current: up to 7 days)
- Local authority housing cost verification response time reduced to 3 working days (current: 10)
- All cross-departmental data flows governed by Digital Economy Act 2017 data sharing agreements

**Priority**: MUST_HAVE

**Stakeholder**: HMRC (SD-7), Local Authorities (SD-10), Devolved Administrations (SD-11)

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — New UC Claimant

- **Role**: Single parent, recently made redundant, first-time UC claimant
- **Goals**: Submit a claim quickly, understand what she's entitled to, receive payment as soon as possible
- **Pain Points**: Low digital confidence, accessing service on a smartphone with limited data, confused by jargon
- **Technical Proficiency**: Low

#### Persona 2: James — Work Coach

- **Role**: DWP Work Coach in a Jobcentre Plus office, managing 120 claimants
- **Goals**: Quickly review claimant circumstances, update commitments, refer to support services
- **Pain Points**: Slow system response times, too many clicks to complete common tasks, system downtime during peak hours
- **Technical Proficiency**: Medium

#### Persona 3: Fatima — Service Centre Agent

- **Role**: DWP Service Centre telephony agent handling UC enquiries
- **Goals**: Resolve claimant queries on first call, update case records accurately, manage high call volumes
- **Pain Points**: Multiple screens/systems, no single claimant view, cannot explain calculation breakdowns to claimants
- **Technical Proficiency**: Medium

#### Persona 4: Council Housing Officer

- **Role**: Local authority housing officer verifying housing costs and managing direct payments
- **Goals**: Respond to DWP housing cost verification requests, manage direct landlord payments, reconcile data
- **Pain Points**: Batch file formats, unclear specifications, no acknowledgement of submissions
- **Technical Proficiency**: Medium

---

### Use Cases

#### UC-1: Submit New UC Claim

**Actor**: Sarah (New UC Claimant)

**Preconditions**:

- Claimant has GOV.UK One Login verified identity or can verify via alternative route
- Claimant is of working age and not in receipt of a legacy benefit being migrated

**Main Flow**:

1. Claimant navigates to UC claim page via GOV.UK
2. System authenticates claimant via GOV.UK One Login
3. System pre-populates known information (name, NI number, address from government sources)
4. Claimant completes claim form in plain language sections (housing, children, health, work)
5. System validates entries and highlights errors in real time
6. System performs initial eligibility check and provides indicative entitlement
7. Claimant reviews and submits claim
8. System generates claim reference and provides clear next-steps guidance
9. System triggers identity verification and evidence-gathering workflows
10. System sends confirmation via GOV.UK Notify (SMS/email per claimant preference)

**Postconditions**:

- Claim registered in case management system with unique reference
- Claimant receives confirmation with expected timeline
- RTI data request triggered to HMRC
- Housing cost verification request sent to relevant local authority

**Alternative Flows**:

- **Alt 1a**: If GOV.UK One Login verification fails, system offers assisted digital pathway (telephone claim)
- **Alt 2a**: If pre-populated data is incorrect, claimant can amend and provide evidence

**Exception Flows**:

- **Ex 1**: If claimant abandons claim, system saves progress for 28 days and sends reminder via GOV.UK Notify
- **Ex 2**: If system detects potential legacy benefit overlap, routes to managed migration team

**Business Rules**:

- Claimant must be 18+ and under State Pension age
- Only one UC claim per household (couple claims joint)
- Scottish claimants offered Scottish choices at submission

**Priority**: CRITICAL

---

#### UC-2: Process Change of Circumstances

**Actor**: Claimant (self-reported) or automated data feed (HMRC RTI, local authority)

**Preconditions**:

- Active UC claim exists
- Change relates to a relevant circumstance (earnings, housing, household composition, health)

**Main Flow**:

1. Change received (claimant journal entry, RTI feed, or LA data)
2. System validates change against business rules
3. System recalculates entitlement using updated circumstances
4. If change affects payment amount, system generates comparison (before/after)
5. System applies change to next assessment period
6. Claimant notified of change and impact via GOV.UK Notify
7. Work Coach notified if change affects claimant commitment

**Postconditions**:

- Claim record updated with change details and audit trail
- Payment recalculated for current and future assessment periods
- Claimant and relevant staff notified

**Business Rules**:

- Changes reported within assessment period apply to that period
- Earnings changes from RTI applied automatically without claimant action
- Housing cost changes require local authority verification before application

**Priority**: CRITICAL

---

### Functional Requirements Detail

#### FR-001: GOV.UK One Login Integration

**Description**: The system must authenticate claimants using GOV.UK One Login, supporting identity proofing at the required confidence level for benefits claims.

**Relates To**: BR-003, UC-1

**Acceptance Criteria**:

- [ ] Given a claimant with a verified GOV.UK One Login, when they access the UC service, then they are authenticated without re-entering credentials
- [ ] Given a claimant without GOV.UK One Login, when they attempt to claim, then they are guided through identity verification or offered an assisted digital route
- [ ] Edge case: If GOV.UK One Login is unavailable, the system provides a degraded authentication pathway with appropriate security controls

**Data Requirements**:

- **Inputs**: Identity assertion from GOV.UK One Login (name, date of birth, NI number)
- **Outputs**: Authenticated session with claimant identity linked to UC claim
- **Validations**: NI number format validation, identity confidence level check

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: GOV.UK One Login platform availability and identity proofing level support

**Assumptions**: GOV.UK One Login will support the identity confidence level required for benefits claims by programme go-live

---

#### FR-002: Configurable Policy Rules Engine

**Description**: The system must implement a configurable rules engine that externalises UC policy rules (eligibility, calculation, tapers, caps, thresholds) from application code.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a policy rule change (e.g., annual uprating), when a policy officer updates the rules configuration, then new calculations apply from the specified effective date without code deployment
- [ ] Given a devolved policy variation (e.g., Scottish fortnightly payments), when a claimant is in Scotland and has elected Scottish choices, then the correct regional rules are applied
- [ ] Edge case: If conflicting rules exist (UK-wide and devolved), the system applies the correct precedence hierarchy and logs the decision

**Data Requirements**:

- **Inputs**: Policy rule definitions (thresholds, taper rates, caps, component rates), effective dates, geographic applicability
- **Outputs**: Calculated entitlement per assessment period, rule trace showing which rules were applied
- **Validations**: Rule consistency checks, regression testing against known scenarios

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Policy team to define rule structures and governance process

**Assumptions**: Policy rules can be expressed in a structured format amenable to a rules engine

---

#### FR-003: Real-Time Eligibility Indicative Check

**Description**: The system must provide claimants with an indicative eligibility and estimated entitlement during the claim process, before full verification is complete.

**Relates To**: BR-002, BR-003, UC-1

**Acceptance Criteria**:

- [ ] Given a claimant entering claim details, when they reach the review stage, then an indicative entitlement is displayed with clear caveats that it is subject to verification
- [ ] Given incomplete information, when the system cannot calculate a reliable estimate, then it explains what information is needed and why
- [ ] Edge case: If the claimant's circumstances are unusually complex, the system recommends contacting a Work Coach rather than providing a misleading estimate

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-002 (rules engine)

---

#### FR-004: Claimant Journal and Messaging

**Description**: The system must provide a secure journal for claimants to communicate with their Work Coach, report changes, upload evidence, and receive notifications.

**Relates To**: BR-003, UC-2

**Acceptance Criteria**:

- [ ] Given an authenticated claimant, when they access their journal, then they see a chronological timeline of messages, notifications, and actions
- [ ] Given a Work Coach sends a message, when the claimant next logs in, then they see the message highlighted as unread with a push notification sent via GOV.UK Notify
- [ ] Edge case: If evidence uploaded exceeds size limits, the system provides clear guidance on acceptable formats and sizes

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-005: Assessment Period Calculation Engine

**Description**: The system must correctly calculate UC entitlement for each monthly assessment period, incorporating all relevant components (standard allowance, child element, housing costs, disability elements, carer element, childcare costs, work allowance, taper).

**Relates To**: BR-001, BR-002, FR-002

**Acceptance Criteria**:

- [ ] Given a claimant's verified circumstances and RTI earnings data, when the assessment period ends, then the system calculates the correct UC payment within 24 hours
- [ ] Given earnings that cross the work allowance threshold, when the taper is applied, then the reduction is calculated at the correct taper rate (currently 55p per GBP 1)
- [ ] Edge case: If RTI data is missing for the assessment period, the system flags for manual review rather than issuing an incorrect payment

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-006: Payment Generation and Disbursement

**Description**: The system must generate payment instructions for all UC claimants and transmit to the DWP payment system for disbursement on the correct date.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a completed assessment, when the payment date arrives, then payment is disbursed to the claimant's nominated bank account via BACS
- [ ] Given a Scottish claimant who has elected fortnightly payments, when payment is due, then two payments are generated per assessment period
- [ ] Edge case: If the bank account is invalid or closed, the system alerts the claimant and Service Centre agent within 24 hours

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-007: Work Coach Case Management

**Description**: The system must provide Work Coaches with a comprehensive case management interface to manage their caseload, set claimant commitments, record actions, and make referrals.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given a Work Coach logs in, when they access their caseload, then they see a prioritised list of claimants requiring action with key indicators (new claim, change of circumstances, missed appointment)
- [ ] Given a Work Coach updates a claimant commitment, when they save, then the commitment is reflected in the claimant's journal within 5 minutes
- [ ] Edge case: If the system is operating in degraded mode, the Work Coach can still view read-only claimant data from the last sync

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-008: Automated Decision Explainability

**Description**: The system must provide clear, plain-language explanations of how UC entitlement was calculated, including which rules were applied and what data was used.

**Relates To**: BR-003, SD-8 (ICO), SD-12 (Citizens Advice)

**Acceptance Criteria**:

- [ ] Given a claimant views their payment breakdown, when they access the explanation, then each component (standard allowance, housing, earnings deduction) is shown with the applicable rule and data source
- [ ] Given a mandatory reconsideration request, when a Decision Maker reviews the case, then the full calculation audit trail is available including the exact rules version applied
- [ ] Edge case: If a rule change occurred mid-assessment period, the explanation shows which rules applied to which portion of the period

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-002 (rules engine with audit trail)

---

#### FR-009: Assisted Digital Pathway

**Description**: The system must support assisted digital journeys for claimants who cannot self-serve online, including telephone claims and Jobcentre Plus face-to-face support.

**Relates To**: BR-003, Principle 1 (User-Centred Design), Principle 16 (Accessibility)

**Acceptance Criteria**:

- [ ] Given a claimant calling the UC helpline, when a Service Centre agent takes the call, then the agent can initiate and complete a claim on behalf of the claimant using the same backend system
- [ ] Given a claimant attending a Jobcentre Plus appointment, when a Work Coach assists with a digital task, then the Work Coach can access the claimant's account with appropriate delegation controls

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-010: GOV.UK Notify Integration

**Description**: The system must use GOV.UK Notify for all claimant communications (claim confirmations, payment notifications, appointment reminders, change of circumstances acknowledgements).

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given a payment is generated, when the payment date is confirmed, then a notification is sent via the claimant's preferred channel (SMS, email, or letter) through GOV.UK Notify
- [ ] Given a notification fails to deliver (bounced email, invalid phone), when the failure is detected, then the system records the failure and alerts the Service Centre

**Priority**: MUST_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Page Load Time

**Requirement**: All claimant-facing pages must load within 2 seconds at the 95th percentile, measured from the user's device.

- Claimant portal page load: < 2 seconds (p95)
- Staff tooling page load: < 3 seconds (p95)
- API response time (internal): < 200ms (p95)
- Assessment calculation time: < 30 seconds per claim

**Measurement Method**: Real User Monitoring (RUM) integrated into the service, with synthetic monitoring as backup.

**Load Conditions**:

- Peak load: 200,000 concurrent users (based on COVID-19 surge modelling)
- Average load: 50,000 concurrent users during business hours
- Monthly change of circumstances volume: 1.2 million
- Monthly new claims: 100,000+

**Priority**: CRITICAL

---

#### NFR-P-002: Throughput

**Requirement**: System must process 500,000 payment calculations per day during month-end assessment period processing.

**Scalability**: Must scale to 3x baseline capacity within 30 minutes for surge scenarios (e.g., policy change triggering mass reassessment of all 6 million claims).

**Priority**: CRITICAL

---

### Availability and Resilience Requirements

#### NFR-A-001: Availability Target

**Requirement**: System must achieve 99.95% uptime for claimant-facing services (26 minutes maximum unplanned downtime per month).

- Maximum planned downtime: 4 hours/month during agreed maintenance windows (Sunday 02:00-06:00)
- Maximum unplanned downtime: 26 minutes per month
- Staff-facing systems: 99.9% availability during business hours (Monday-Saturday 06:00-22:00)

**Maintenance Windows**: Sunday 02:00-06:00 GMT only. No planned downtime during payment processing windows (last 3 working days of each month).

**Priority**: CRITICAL

---

#### NFR-A-002: Disaster Recovery

**RPO (Recovery Point Objective)**: 5 minutes — maximum 5 minutes of data loss acceptable.

**RTO (Recovery Time Objective)**: 30 minutes — service must be restored within 30 minutes.

**Backup Requirements**:

- Backup frequency: Continuous replication to secondary region
- Backup retention: 90 days for operational recovery, 7 years for compliance/audit
- Geographic backup location: UK sovereign data centres, geographically separated

**Failover Requirements**:

- Automatic failover to secondary UK region: YES
- Failover time: < 15 minutes
- Regular DR testing: Quarterly with full failover exercise

**Priority**: CRITICAL

---

#### NFR-A-003: Fault Tolerance

**Requirement**: System must continue processing payments even if individual components fail. No single component failure may prevent payment generation.

**Resilience Patterns Required**:

- [x] Circuit breaker for all external dependencies (HMRC RTI, LA systems, GOV.UK services)
- [x] Retry with exponential backoff and jitter for transient failures
- [x] Timeout on all network calls (default 30 seconds, configurable per integration)
- [x] Bulkhead isolation between claimant-facing, staff-facing, and payment processing workloads
- [x] Graceful degradation: If HMRC RTI is unavailable, display last-known data with staleness warning

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: Claimants authenticate via GOV.UK One Login. Staff authenticate via DWP Active Directory with SAML 2.0 federation.

**Multi-Factor Authentication (MFA)**:

- Required for: All staff access, privileged operations, external access
- Claimant MFA: As determined by GOV.UK One Login identity proofing level
- MFA methods: Authenticator app, SMS (staff); GOV.UK One Login methods (claimants)

**Session Management**:

- Claimant session timeout: 30 minutes inactivity, 8 hours absolute
- Staff session timeout: 15 minutes inactivity for case-level access, 60 minutes for dashboard-only views
- Re-authentication required for: Payment overrides, manual adjustments exceeding GBP 5,000

**Priority**: CRITICAL

---

#### NFR-SEC-002: Authorisation

**Requirement**: Role-based access control (RBAC) with least privilege. No staff member may access claimant data without a legitimate business need.

**Roles and Permissions**:

- Claimant: Own claim data only
- Work Coach: Assigned caseload data, read-only for unassigned
- Service Centre Agent: Search and access any active claim (audited)
- Decision Maker: Assessment review and override capability
- Team Leader: Team management, quality assurance sampling
- System Administrator: Configuration only, no claimant data access

**Privilege Elevation**: Temporary elevated access via approval workflow (dual authorisation for production data access).

**Priority**: CRITICAL

---

#### NFR-SEC-003: Data Encryption

**Requirement**:

- Data in transit: TLS 1.3 minimum for all communications
- Data at rest: AES-256 encryption for all data stores
- Key management: UK sovereign key management service, keys never leave UK jurisdiction

**Encryption Scope**:

- [x] Database encryption at rest (all databases)
- [x] Backup encryption (encrypted before leaving compute environment)
- [x] File storage encryption (uploaded evidence, documents)
- [x] Application-level field encryption for PII (NI numbers, bank details, health information)

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-001: UK GDPR and Data Protection Act 2018 Compliance

**Applicable Regulations**: UK GDPR, Data Protection Act 2018, Digital Economy Act 2017

**Compliance Requirements**:

- [x] Data subject rights (access, rectification, erasure where lawful, portability)
- [x] Lawful basis documented for all processing (public task under Social Security legislation)
- [x] Privacy by design and by default (data minimisation, purpose limitation)
- [x] Data breach notification to ICO within 72 hours, to affected data subjects without undue delay
- [x] Data Protection Impact Assessment (DPIA) completed and approved by DWP DPO

**Data Residency**: All personal data must reside in UK sovereign data centres. No transfer outside UK without lawful basis and DPIA.

**Data Retention**: Claims data retained for 6 years after claim closure (aligned to DWP retention schedule). Anonymised for analytics after retention period.

**Priority**: CRITICAL

---

#### NFR-C-002: Audit Logging

**Requirement**: Comprehensive, immutable audit trail for all data access, changes, and decisions.

**Audit Log Contents** (for all sensitive operations):

- Who: User identity (staff ID, claimant reference, or system service)
- What: Action performed (view, create, update, delete, calculate, pay)
- When: Timestamp (UTC, millisecond precision)
- Where: System component, IP address
- Why: Context (case reference, request ID, business justification for access)
- Result: Success/failure with error details

**Log Retention**: 7 years for compliance and audit logs (immutable storage). Tamper-evident with cryptographic hashing.

**Log Integrity**: Logs must be written to an append-only store that is not modifiable by system administrators.

**Priority**: CRITICAL

---

#### NFR-C-003: Automated Decision-Making Transparency (UK GDPR Article 22)

**Requirement**: UC entitlement calculations constitute automated decision-making with significant effects. The system must support meaningful human review and provide explanations of automated decisions.

**Report Types**:

- Calculation breakdown: Available to claimant on demand, in plain language
- Decision audit trail: Available to Decision Makers for mandatory reconsideration
- Statistical reports: Available to NAO and Parliament for scrutiny

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-001: GDS Service Standard Compliance

**Requirement**: The claimant-facing service must pass GDS service assessments at Alpha, Beta, and Live gates.

**UX Standards**:

- GOV.UK Design System components and patterns
- WCAG 2.2 Level AA compliance (legal requirement)
- Mobile-first responsive design
- Browser support: Chrome, Firefox, Safari, Edge — last 2 versions; plus IE11 for assisted digital kiosks
- Content at reading age 9 or below for claimant-facing text

**User Onboarding**: Progressive disclosure of information during claim journey. No training required for claimants.

**Priority**: CRITICAL

---

#### NFR-U-002: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance across all claimant-facing and staff-facing interfaces.

**Accessibility Features**:

- [x] Keyboard navigation for all functions
- [x] Screen reader compatibility (JAWS, NVDA, VoiceOver)
- [x] High contrast mode
- [x] Adjustable font sizes (up to 200% without horizontal scrolling)
- [x] Alt text for all non-decorative images
- [x] Captions for video content

**Testing**: Automated accessibility testing in CI/CD (axe-core) plus manual testing with assistive technologies. User research with disabled claimants in every research round.

**Priority**: CRITICAL

---

#### NFR-U-003: Welsh Language Support

**Requirement**: Full Welsh language support for claimant-facing interfaces, in compliance with the Welsh Language (Wales) Measure 2011.

**Localisation Scope**:

- [x] All claimant-facing UI text available in Welsh
- [x] Welsh-language claim forms with equal prominence to English
- [x] Date and number formatting per locale
- [x] Welsh-language GOV.UK Notify templates

**Priority**: MUST_HAVE

---

### Maintainability and Supportability Requirements

#### NFR-M-001: Observability

**Requirement**: Comprehensive instrumentation for real-time monitoring, troubleshooting, and capacity planning.

**Telemetry Requirements**:

- **Logging**: Structured JSON logs with correlation IDs across all services
- **Metrics**: RED metrics (Rate, Errors, Duration) per service and endpoint
- **Tracing**: Distributed tracing with OpenTelemetry across all service boundaries
- **Dashboards**: Real-time operational dashboards for payment processing, claim volumes, system health
- **Alerts**: SLO-based alerting with actionable runbooks linked to each alert

**Priority**: CRITICAL

---

## Integration Requirements

### External System Integrations

#### INT-001: HMRC Real Time Information (RTI)

**Purpose**: Receive claimant earnings data from HMRC for UC assessment calculations.

**Integration Type**: Batch file transfer (current) transitioning to near-real-time event-driven (target)

**Data Exchanged**:

- **From HMRC to UC**: Employee earnings submissions (pay, tax, NI), employer details, employment start/end dates
- **From UC to HMRC**: Claimant RTI data requests, data quality exception reports

**Integration Pattern**: Target: Event-driven near-real-time (within 24 hours of employer submission). Interim: Enhanced batch (4x daily).

**Authentication**: Mutual TLS with HMRC Government Gateway infrastructure.

**Error Handling**: Dead letter queue for unprocessable records. Automated retry for transient failures. Manual review queue for data quality exceptions. Monthly reconciliation between HMRC and UC records.

**SLA**: 99.5% availability, < 24 hours data freshness for RTI records.

**Owner**: HMRC RTI Programme (joint governance with DWP)

**Priority**: CRITICAL

---

#### INT-002: Local Authority Housing Systems

**Purpose**: Exchange housing cost verification data and direct payment instructions with approximately 300 local authority housing systems.

**Integration Type**: API-based (target), transitioning from batch file exchange (current)

**Data Exchanged**:

- **From UC to LA**: Housing cost verification requests, tenant details
- **From LA to UC**: Verified housing costs, tenancy confirmation, rent changes, direct payment instructions

**Integration Pattern**: RESTful API with webhook notifications for status changes. Legacy batch adapter for councils unable to adopt API.

**Authentication**: OAuth 2.0 with DWP API Management gateway.

**SLA**: 3 working days verification response time.

**Owner**: DLUHC (standards), individual local authorities (implementation)

**Priority**: HIGH

---

#### INT-003: GOV.UK One Login

**Purpose**: Claimant identity verification and authentication.

**Integration Type**: Real-time API (OpenID Connect / SAML 2.0)

**Data Exchanged**:

- **From GOV.UK One Login to UC**: Identity assertion (verified name, date of birth, NI number)
- **From UC to GOV.UK One Login**: Authentication requests

**Authentication**: OpenID Connect with signed JWTs.

**SLA**: 99.9% availability, < 2 seconds authentication response time.

**Owner**: GDS

**Priority**: CRITICAL

---

#### INT-004: GOV.UK Notify

**Purpose**: All claimant and staff notifications (SMS, email, letter).

**Integration Type**: Real-time API

**Data Exchanged**:

- **From UC to GOV.UK Notify**: Notification requests (templates, personalisation data)
- **From GOV.UK Notify to UC**: Delivery receipts, failure notifications

**Authentication**: API key with team-level access control.

**SLA**: 99.95% availability for API, best-effort delivery for SMS/email.

**Owner**: GDS

**Priority**: HIGH

---

#### INT-005: DWP Payment System (BACS)

**Purpose**: Generate and transmit payment instructions for UC disbursement.

**Integration Type**: Batch file transfer (BACS submission cycle)

**Data Exchanged**:

- **From UC to Payment System**: Payment instructions (claimant bank details, amounts, payment dates)
- **From Payment System to UC**: Payment confirmations, rejection notifications

**Authentication**: Mutual TLS, file-level encryption.

**Error Handling**: Rejected payments automatically flagged for Service Centre agent review. Claimant notified within 24 hours of payment failure.

**SLA**: 100% of payment files submitted within BACS cut-off times. Zero data loss tolerance.

**Owner**: DWP Finance Operations

**Priority**: CRITICAL

---

## Data Requirements

### Data Entities

#### Entity 1: Claim

**Description**: Represents a UC claim for an individual or couple.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| claim_id | UUID | Yes | Unique claim identifier | Primary key |
| claimant_nino | String(9) | Yes | National Insurance number | Format validated, encrypted at rest |
| claim_type | Enum | Yes | Single or joint claim | ['single', 'joint'] |
| status | Enum | Yes | Claim lifecycle status | ['draft', 'submitted', 'assessing', 'active', 'closed', 'suspended'] |
| start_date | Date | Yes | Claim start date | Not future-dated |
| region | Enum | Yes | Geographic region for policy rules | ['england', 'scotland', 'wales', 'northern_ireland'] |
| created_at | Timestamp | Yes | Record creation | Indexed |
| updated_at | Timestamp | Yes | Last modification | Indexed |

**Relationships**:

- One-to-many with AssessmentPeriod
- One-to-many with ClaimComponent (housing, children, health)
- Many-to-one with Claimant

**Data Volume**: 6 million active claims, 100,000+ new claims per month, 1.2 million changes per month.

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 6 years after claim closure.

---

#### Entity 2: Assessment Period

**Description**: Monthly assessment period for calculating UC entitlement.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| period_id | UUID | Yes | Unique period identifier | Primary key |
| claim_id | UUID | Yes | Parent claim | Foreign key to Claim |
| start_date | Date | Yes | Period start | Monthly cycle |
| end_date | Date | Yes | Period end | start_date + 1 month |
| earnings | Decimal | No | Verified earnings from RTI | Non-negative |
| entitlement | Decimal | Yes | Calculated UC amount | Non-negative |
| payment_status | Enum | Yes | Payment lifecycle | ['pending', 'calculated', 'approved', 'paid', 'adjusted'] |
| rules_version | String | Yes | Policy rules version applied | For audit trail |

**Data Volume**: 72 million records per year (6M claims x 12 months).

**Data Classification**: OFFICIAL-SENSITIVE

---

### Data Quality Requirements

**Data Accuracy**: Assessment calculations must be 95%+ accurate on first calculation. All calculations auditable against rules version and input data.

**Data Completeness**: All mandatory fields enforced at point of entry. Missing RTI data flagged rather than defaulted.

**Data Consistency**: Cross-system reconciliation between UC, HMRC RTI, and payment system run daily with exception reporting.

**Data Timeliness**: RTI earnings data no older than 24 hours. Housing cost data no older than 10 working days. Payment data reconciled within 1 working day of BACS processing.

**Data Lineage**: Full source-to-calculation lineage maintained for every assessment, enabling Decision Makers to trace any payment to its input data and applied rules.

---

### Data Migration Requirements

**Migration Scope**: All active UC claims (approximately 6 million) and 24 months of assessment history from the legacy platform.

**Migration Strategy**: Phased migration by geographic region over 12 months, with parallel running during each phase. No big-bang migration.

**Data Transformation**: Legacy claim data transformed to new data model. Mapping specification to be developed during design phase.

**Data Validation**: Automated comparison of entitlement calculations between legacy and new system for migrated claims. 100% validation before cutover.

**Rollback Plan**: Rollback capability maintained for 30 days post-cutover per region. Legacy system kept operational in read-only mode during parallel run.

**Migration Timeline**: 12 months phased by region, starting with smallest caseload areas for early learning.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy to UK sovereign cloud infrastructure — no data processing or storage outside UK jurisdiction.

**TC-2**: Must integrate with existing DWP payment infrastructure (BACS) — wholesale replacement of payment systems is out of scope.

**TC-3**: Must maintain backward compatibility with legacy batch interfaces for local authorities unable to adopt APIs within the programme timeline.

**TC-4**: Must use GOV.UK Design System for all citizen-facing interfaces.

---

### Business Constraints

**BC-1**: Zero tolerance for unplanned payment disruptions — any migration approach that risks payment continuity will be rejected.

**BC-2**: Budget envelope of GBP 495M over 5 years as per Spending Review settlement.

**BC-3**: Must pass GDS service assessments at Alpha, Beta, and Live gates to continue.

**BC-4**: Annual UC uprating must be supported throughout the modernisation — cannot freeze policy changes during migration.

---

### Assumptions

**A-1**: GOV.UK One Login will support the identity proofing confidence level required for benefits claims by Q4 2026.

**A-2**: HMRC will commit to improving RTI data freshness from 7 days to 24 hours within the programme timeline.

**A-3**: A minimum of 60% of local authorities will be capable of adopting API-based data exchange within 24 months.

**A-4**: DWP can recruit and retain sufficient digital talent to reduce reliance on external suppliers to below 30% of the delivery team.

**Validation Plan**: Each assumption will be tested during the Alpha phase. Assumptions that fail validation will trigger a risk escalation and potential requirements revision.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Average claim processing time | 23 working days | 10 working days | March 2028 | Case management system reporting |
| Claimant satisfaction | 68% | 85% | March 2028 | GDS transaction survey |
| Assessment accuracy (first calculation) | 88% | 95% | March 2028 | Quality assurance sampling |
| Annual operational savings | GBP 0 | GBP 180M | Year 3 | Benefits realisation tracking |
| Cost per claim processed | GBP 312 | GBP 187 | Year 3 | Finance reporting |

---

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability (claimant-facing) | 99.95% | Uptime monitoring |
| Page load time (p95) | < 2 seconds | Real User Monitoring |
| API response time (p95) | < 200ms | APM tooling |
| Payment file accuracy | 100% | BACS reconciliation |
| Deployment frequency | Weekly | CI/CD metrics |
| Mean time to recovery (MTTR) | < 15 minutes | Incident tracking |

---

### User Adoption Metrics

| Metric | Target | Timeline | Measurement Method |
|--------|--------|----------|-------------------|
| Digital channel adoption (new claims) | 90% | 12 months post-launch | Channel analytics |
| Claimant self-service rate (changes) | 75% | 12 months post-launch | Case management |
| Work Coach satisfaction with new tooling | 80% | 6 months post-launch | Staff survey |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| GOV.UK One Login readiness | Identity proofing level support | GDS | Q4 2026 | At Risk | HIGH — blocks claimant authentication |
| HMRC RTI data freshness | 24-hour data availability | HMRC | Q2 2027 | On Track | HIGH — delays processing time improvement |
| LA API adoption | 60% of councils on API | DLUHC / LAs | Q4 2027 | At Risk | MEDIUM — batch fallback available |
| DWP cloud platform | UK sovereign cloud environment | DWP Digital | Q3 2026 | On Track | CRITICAL — blocks all deployment |
| Staff training programme | 25,000+ staff trained | DWP Operations | Ongoing | On Track | HIGH — blocks phased rollout |

---

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-001 | Payment disruption during migration | LOW | CRITICAL | Phased migration, parallel running, rehearsals, rollback capability | UC Operations Director |
| R-002 | HMRC unable to improve RTI freshness | MEDIUM | HIGH | Interim enhanced batch (4x daily), design for variable data freshness | HMRC Programme Lead |
| R-003 | Local authorities unable to adopt API | HIGH | MEDIUM | Batch adapter maintained as fallback, central funding for LA integration | DLUHC |
| R-004 | GOV.UK One Login not ready at required confidence level | MEDIUM | HIGH | Alternative identity verification pathway, phased GOV.UK One Login adoption | GDS |
| R-005 | Digital talent recruitment shortfall | HIGH | MEDIUM | Competitive salary benchmarking, apprenticeship programme, managed service partners | DWP HR/Digital |
| R-006 | Policy changes during migration add complexity | HIGH | MEDIUM | Configurable rules engine, protected policy sprint capacity, change freeze negotiations | SRO |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Speed of Delivery vs Operational Safety

**Conflicting Requirements**:

- **Requirement A**: BR-002 — Reduce processing time to 10 days by March 2028 (Ministerial urgency)
- **Requirement B**: BR-001 — Zero unplanned payment disruptions (operational safety)

**Stakeholders Involved**:

- **Secretary of State** (SD-1): Wants rapid, visible improvement for political messaging
- **UC Operations Director** (SD-3): Wants cautious, phased approach to protect payments

**Nature of Conflict**: Aggressive timeline creates pressure to accelerate migration, increasing the risk of payment disruptions. Cautious migration timelines delay the processing time improvements that are politically essential.

**Resolution Strategy**: PHASE

**Decision**: Phased delivery — quick wins on claimant experience (portal, notifications) in Phase 1 (6 months), followed by cautious migration of processing engine in Phase 2 (12 months) with extensive parallel running.

**Rationale**: Separating the claimant experience layer from the processing engine allows visible improvements without risking payment integrity. Phase 1 delivers Ministerial quick wins; Phase 2 delivers the processing time improvement with full safety controls.

**Decision Authority**: SRO with Programme Board endorsement.

---

### Conflict C-2: Investment Scale vs Treasury Cost Containment

**Conflicting Requirements**:

- **Requirement A**: BR-004 — Configurable rules engine requires significant upfront investment
- **Requirement B**: BR-005 — GBP 180M annual savings target requires cost discipline

**Stakeholders Involved**:

- **DWP CDIO** (SD-4): Wants comprehensive modernisation with long-term architectural quality
- **HM Treasury** (SD-5): Wants minimum viable investment with maximum measurable return

**Resolution Strategy**: COMPROMISE

**Decision**: Invest in rules engine for highest-change policy areas first (earnings taper, annual uprating, Scottish choices). Extend to remaining policy areas in subsequent phases.

**Decision Authority**: DWP Permanent Secretary (Accounting Officer) with Treasury spending team endorsement.

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Requirements Approval | Stakeholder sign-off on this document | May 2026 | Stakeholder review |
| Alpha Assessment | GDS Alpha assessment pass | September 2026 | User research evidence |
| Beta (Private) Launch | Private beta with limited claimant cohort | March 2027 | Cloud platform, core integrations |
| Beta Assessment | GDS Beta assessment pass | June 2027 | Private beta evidence |
| Phase 1 Go-Live | New claimant portal and communications | September 2027 | Beta assessment pass |
| Phase 2 Go-Live | New processing engine (phased by region) | March 2028 | Phase 1 stable, staff training |
| Live Assessment | GDS Live assessment pass | June 2028 | Phase 2 stable |

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (internal team) | GBP 120M | 200 FTE over 3 years |
| Cloud infrastructure | GBP 45M | UK sovereign cloud, 5-year commitment |
| System integration services | GBP 85M | HMRC, LA, GOV.UK platform integrations |
| Migration and parallel running | GBP 65M | 12-month phased migration |
| Testing (performance, security, accessibility) | GBP 25M | Including penetration testing |
| Training and change management | GBP 35M | 25,000+ staff |
| Contingency (25%) | GBP 95M | Per Green Book guidance |
| **Total (5-year programme)** | **GBP 470M** | Within GBP 495M envelope |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Cloud infrastructure | GBP 18M/year | Includes DR and scaling headroom |
| Managed services and support | GBP 12M/year | Vendor support, service management |
| Internal staff (BAU team) | GBP 25M/year | Reduced from current GBP 40M through automation |
| Licences and subscriptions | GBP 5M/year | Tooling, monitoring, security |
| **Total** | **GBP 60M/year** | Down from current GBP 85M/year (GBP 25M saving) |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| UC Service Owner | Service Accountability | [ ] Approved | PENDING | |
| DWP CDIO | Enterprise Architect | [ ] Approved | PENDING | |
| DWP SIRO | Information Security | [ ] Approved | PENDING | |
| DWP DPO | Data Protection | [ ] Approved | PENDING | |
| CDDO Assessment Lead | Standards Compliance | [ ] Approved | PENDING | |

### Sign-Off

By signing below, stakeholders confirm that requirements are complete, understood, and approved to proceed to design phase.

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, UC Modernisation | _________ | PENDING |
| DWP CDIO | _________ | PENDING |
| UC Service Owner | _________ | PENDING |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| UC | Universal Credit — the single benefit replacing six legacy benefits |
| RTI | Real Time Information — HMRC system for employer earnings reporting |
| BACS | Bankers' Automated Clearing Services — UK payment clearing system |
| Assessment Period | Monthly period over which UC entitlement is calculated |
| Taper | Rate at which UC is reduced as earnings increase (currently 55%) |
| Work Allowance | Earnings threshold before taper applies (varies by circumstance) |
| Scottish Choices | Devolved options for UC delivery in Scotland (fortnightly payments, direct housing payments) |
| NINO | National Insurance Number |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — Enterprise Architecture Principles (SDG 1: No Poverty)
- ARC-001-STKE-v1.0 — Stakeholder Drivers & Goals Analysis (UC Modernisation)
- GDS Service Standard — https://www.gov.uk/service-manual/service-standard
- Technology Code of Practice — https://www.gov.uk/guidance/the-technology-code-of-practice

### Appendix C: Requirement Traceability to Stakeholder Drivers

| Requirement | Stakeholder Drivers | Architecture Principles |
|-------------|-------------------|----------------------|
| BR-001 | SD-1, SD-3 | Principle 3 (Resilience), Principle 14 (Availability) |
| BR-002 | SD-1, SD-5, SD-6 | Principle 13 (Performance) |
| BR-003 | SD-1, SD-6, SD-12 | Principle 1 (User-Centred Design), Principle 16 (Accessibility) |
| BR-004 | SD-4, SD-11 | Principle 15 (Maintainability) |
| BR-005 | SD-2, SD-5 | Principle 20 (Open Source and Reuse) |
| BR-006 | SD-7, SD-10, SD-11 | Principle 4 (Interoperability), Principle 11 (Loose Coupling) |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Universal Credit Modernisation
**Model**: Claude Opus 4.6
