# Project Requirements: Disability Confident Employer Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Disability Confident Employer Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Disability Confident Employer Portal, DWP |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DWP Disability Employment Directorate, Business Disability Forum, Scope, CBI |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Disability Confident Employer Portal — a DWP-operated platform for managing the Disability Confident employer accreditation scheme, including digital application workflows, evidence-based assessment, Access to Work integration, and disability employment gap tracking.

---

## Executive Summary

### Business Context

The Disability Confident scheme currently has over 19,000 employer members across three levels (Committed, Employer, Leader). Despite this scale, the disability employment gap remains at approximately 28 percentage points. The Work and Pensions Committee has criticised the scheme as "too easy to pass" through self-assessment alone. The current administration relies on PDF forms, email submissions, and manual processing with 6-8 week turnaround times. The portal will digitise the scheme, introduce evidence-based assessment for higher levels, integrate with DWP Access to Work, and enable tracking of whether participation actually improves disability employment outcomes.

### Objectives

- Digitise the Disability Confident accreditation workflow end-to-end
- Introduce evidence-based assessment for Levels 2 (Employer) and 3 (Leader)
- Integrate with DWP Access to Work for seamless workplace adjustment referrals
- Track disability employment metrics at employer level
- Maintain scheme participation while raising quality standards

### Expected Outcomes

- Application-to-certification time reduced from 8 weeks to 2 weeks
- 100% of Level 2-3 certifications evidence-based within 18 months
- 500+ Access to Work referrals per quarter via portal within 12 months
- 50%+ of Level 2-3 employers reporting workforce disability data within 24 months
- Disability employment gap reduction measurable among scheme participants within 36 months

### Project Scope

**In Scope**:

- Digital application and renewal workflow for all three scheme levels
- Evidence upload and validation for Levels 2-3
- Disabled employee anonymous feedback mechanism
- Employer public profiles with inclusion practices
- DWP Access to Work referral integration
- Workforce disability data collection and reporting
- Public-facing employer search for jobseekers
- Analytics dashboard for DWP scheme managers

**Out of Scope**:

- Disability Confident scheme policy design (DWP policy team responsibility)
- Access to Work grant processing (separate DWP system)
- Job matching or vacancy management (DWP Find a Job is separate)
- BDF Disability Smart certification (separate scheme, but alignment considered)

---

## Business Requirements

### BR-001: Digital Accreditation Workflow

**Description**: Employers must be able to apply for, renew, and manage their Disability Confident accreditation entirely through a digital self-service portal.

**Rationale**: The current paper/email process takes 8 weeks and is a barrier to employer participation. Digital processing enables faster certification and better data collection.

**Success Criteria**:

- Application-to-certification time of 2 weeks average
- 90%+ digital completion rate (applications started vs submitted)
- Employer satisfaction score above 7/10

**Priority**: MUST_HAVE

**Stakeholder**: CBI/FSB (SD-3)

---

### BR-002: Evidence-Based Assessment (Levels 2-3)

**Description**: Level 2 (Disability Confident Employer) and Level 3 (Disability Confident Leader) certifications must require evidence of disability inclusion practices, replacing pure self-assessment.

**Rationale**: Self-assessment without evidence has been criticised as allowing employers to claim Disability Confident status without genuine practice change. Evidence-based assessment strengthens scheme credibility.

**Success Criteria**:

- Evidence review completed for 100% of Level 2-3 applications within 18 months
- Evidence categories: recruitment practices, reasonable adjustments, employee feedback, workforce data
- Certification downgrade/revocation process for non-compliant employers

**Priority**: MUST_HAVE

**Stakeholder**: Scope (SD-2), DWP Minister (SD-1)

---

### BR-003: Access to Work Integration

**Description**: The portal must integrate with DWP Access to Work, enabling employers to make referrals for workplace adjustments and employees to access support through their employer's Disability Confident profile.

**Rationale**: Disability Confident employers should actively facilitate Access to Work support for their disabled employees. Integration makes this seamless rather than requiring separate application processes.

**Success Criteria**:

- Access to Work referral form accessible from employer portal
- 500+ referrals per quarter via portal within 12 months
- Referral-to-adjustment average time tracked and published

**Priority**: SHOULD_HAVE

**Stakeholder**: DWP Minister (SD-1), disabled jobseekers (SD-5)

---

### BR-004: Disability Employment Gap Tracking

**Description**: The portal must collect anonymised workforce disability data from Level 2-3 employers to track whether scheme participation correlates with improved disability employment outcomes.

**Rationale**: Without outcome measurement, the scheme cannot demonstrate it is contributing to closing the disability employment gap, which is its stated purpose.

**Success Criteria**:

- 50%+ of Level 2-3 employers reporting workforce disability data within 24 months
- Employer-level disability employment rates tracked over time
- Sector-level aggregated analysis published annually

**Priority**: SHOULD_HAVE

**Stakeholder**: DWP Minister (SD-1), Scope (SD-2)

---

### BR-005: Employer Public Profiles

**Description**: Each certified employer must have a public profile displaying their Disability Confident level, specific inclusion practices, reasonable adjustment provisions, and (where consented) employee feedback scores.

**Rationale**: Disabled jobseekers need transparent information to make informed job application decisions. Public profiles incentivise genuine practice improvement.

**Success Criteria**:

- Public profiles available for all certified employers
- Inclusion practice categories standardised and comparable
- Employee feedback integrated (anonymised, aggregate scores only)
- Integration with DWP Find a Job to display DC status

**Priority**: SHOULD_HAVE

**Stakeholder**: Disabled jobseekers (SD-5)

---

## Functional Requirements

### User Personas

#### Persona 1: HR Director (Large Employer)

- **Role**: HR leader at a FTSE 250 company with existing Disability Confident Level 2
- **Goals**: Renew certification, upload evidence, access Access to Work referrals, demonstrate progress
- **Pain Points**: Current PDF process is manual, evidence collection not guided, no feedback on improvement areas
- **Technical Proficiency**: Medium

#### Persona 2: SME Owner

- **Role**: Owner of a 15-person business considering Level 1 (Committed)
- **Goals**: Understand scheme requirements, complete application quickly, access practical guidance
- **Pain Points**: Scheme documentation is long and jargon-heavy, unclear what Level 1 requires, worried about bureaucracy
- **Technical Proficiency**: Low to Medium

#### Persona 3: DWP Scheme Assessor

- **Role**: DWP staff member reviewing Level 2-3 applications
- **Goals**: Review evidence efficiently, make consistent assessment decisions, track case load
- **Pain Points**: Evidence arrives in mixed formats via email, no standardised review workflow, no decision support
- **Technical Proficiency**: Medium

#### Persona 4: Disabled Jobseeker

- **Role**: Disabled person searching for inclusive employers
- **Goals**: Find genuinely inclusive employers, understand what adjustments are offered, trust Disability Confident badge
- **Pain Points**: DC badge tells you nothing about actual practices, no way to compare employers, no employee feedback
- **Technical Proficiency**: Low to High (varies)

---

### Functional Requirements Detail

#### FR-001: Employer Registration and Profile

**Description**: Employers must be able to register, create an organisational profile (size, sector, locations), and manage their Disability Confident journey through a self-service portal.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a new employer, when they register, then they can create a profile using Companies House data auto-population
- [ ] Given a registered employer, when they log in, then they see their current DC level, certification expiry, and renewal pathway
- [ ] Given an employer with multiple sites, when registering, then they can add multiple workplace locations

**Priority**: MUST_HAVE

---

#### FR-002: Level 1 (Committed) Application

**Description**: Employers must be able to complete a Level 1 (Disability Confident Committed) application through a guided self-declaration workflow.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given an employer starting Level 1, when the application begins, then a guided workflow presents each commitment area
- [ ] Given all commitments confirmed, when submitted, then a Level 1 certificate is generated automatically (no manual review)
- [ ] Given certificate generation, when complete, then the employer profile is updated and public

**Priority**: MUST_HAVE

---

#### FR-003: Level 2-3 Application with Evidence Upload

**Description**: Employers must be able to apply for Level 2 (Employer) or Level 3 (Leader) with structured evidence upload across defined evidence categories.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given an employer applying for Level 2, when the application starts, then evidence categories are presented with guidance
- [ ] Given evidence upload, when files are submitted, then they are virus-scanned, stored securely, and linked to the application
- [ ] Given evidence categories (recruitment, adjustments, retention, feedback), when all are addressed, then the application is marked ready for review
- [ ] Given incomplete evidence, when gaps are identified, then the system highlights missing areas with guidance

**Priority**: MUST_HAVE

---

#### FR-004: Evidence Assessment Workflow

**Description**: DWP assessors must be able to review, score, and decide on Level 2-3 applications through a structured assessment workflow with decision support.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a submitted application, when assigned to an assessor, then all evidence is presented in a structured review interface
- [ ] Given evidence categories, when reviewed, then the assessor can score each category and add comments
- [ ] Given the assessment, when completed, then a recommendation is generated (approve, conditional, reject)
- [ ] Given a decision, when finalised, then the employer is notified with detailed feedback

**Priority**: MUST_HAVE

---

#### FR-005: Disabled Employee Feedback

**Description**: Disabled employees of certified employers must be able to provide anonymous feedback on their employer's disability inclusion practices.

**Relates To**: BR-002, BR-005

**Acceptance Criteria**:

- [ ] Given a certified employer, when an employee accesses the feedback form, then no identifying information is collected
- [ ] Given feedback, when submitted, then it is aggregated and only displayed when 10+ responses are received (anonymity threshold)
- [ ] Given aggregate feedback, when included in employer profile, then it shows scores across inclusion dimensions
- [ ] Given feedback trends, when assessed alongside evidence, then assessors can identify discrepancies

**Priority**: SHOULD_HAVE

---

#### FR-006: Access to Work Referral

**Description**: The portal must provide a referral pathway to DWP Access to Work, enabling employers and employees to initiate workplace adjustment support.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given a certified employer's portal, when Access to Work is selected, then a pre-populated referral form is presented
- [ ] Given a completed referral, when submitted, then it is transmitted to Access to Work systems via API
- [ ] Given a referral, when Access to Work processes it, then the status is visible in the employer portal

**Priority**: SHOULD_HAVE

---

#### FR-007: Workforce Disability Data Collection

**Description**: The portal must collect anonymised workforce disability data from Level 2-3 employers on an annual basis.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a Level 2-3 employer, when annual data submission is due, then a structured data entry form is presented
- [ ] Given workforce data (total employees, disabled employees, new hires, retention rates), when submitted, then it is stored securely
- [ ] Given employer-level data, when aggregated to sector level, then no individual employer can be identified in published reports

**Priority**: SHOULD_HAVE

---

#### FR-008: Public Employer Search

**Description**: Disabled jobseekers must be able to search for Disability Confident employers by location, sector, size, and DC level, viewing public profiles.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given the public search, when a location and sector are entered, then matching DC employers are listed
- [ ] Given an employer profile, when viewed, then DC level, inclusion practices, and (where available) employee feedback are displayed
- [ ] Given the search results, when sorted, then Level 3 (Leader) employers can be prioritised

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Application Workflow Response

**Requirement**: All portal pages must load within 2 seconds at p95. Evidence upload must support files up to 50MB with progress indicator.

**Priority**: MUST_HAVE

---

#### NFR-P-002: Concurrent Employers

**Requirement**: Support 500 concurrent employer sessions, scaling to 2,000 during renewal peak periods.

**Priority**: SHOULD_HAVE

---

### Security Requirements

#### NFR-SEC-001: Data Classification

**Requirement**: Employer profile data and scheme membership classified OFFICIAL. Employee feedback data, workforce disability data, and evidence documents classified OFFICIAL-SENSITIVE.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Employee Feedback Anonymity

**Requirement**: Employee feedback system must guarantee anonymity. No IP addresses, device fingerprints, or timestamps that could identify individuals may be stored alongside feedback. Feedback only published when 10+ responses received per employer.

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Authentication

**Requirement**: Employer access via GOV.UK One Login. DWP assessor access via DWP SSO. Jobseeker access to public profiles without authentication.

**Priority**: MUST_HAVE

---

### Accessibility Requirements

#### NFR-ACC-001: Platform Accessibility

**Requirement**: WCAG 2.2 Level AAA for all user-facing components. As a disability inclusion platform, exemplary accessibility is a reputational necessity.

**Priority**: MUST_HAVE

---

#### NFR-ACC-002: Easy Read Version

**Requirement**: Key employer guidance and the employee feedback form must be available in Easy Read format for people with learning disabilities.

**Priority**: SHOULD_HAVE

---

### Availability Requirements

#### NFR-A-001: Uptime

**Requirement**: 99.5% uptime for the employer portal. 99.9% for the public employer search (used by disabled jobseekers).

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Companies House API

**Purpose**: Auto-populate employer registration data (company name, registered address, SIC code, employee count)

**Integration Type**: REST API

**Data Exchanged**: Company search results, company details

**Authentication**: Companies House API key

**Priority**: SHOULD_HAVE

---

### INT-002: DWP Access to Work

**Purpose**: Workplace adjustment referral pathway

**Integration Type**: REST API (internal DWP)

**Data Exchanged**: Referral details (employer, employee category, adjustment type requested), referral status updates

**Authentication**: Internal DWP service authentication

**Priority**: SHOULD_HAVE

---

### INT-003: DWP Find a Job

**Purpose**: Display Disability Confident status on job listings

**Integration Type**: REST API

**Data Exchanged**: Employer DC status, level, certification expiry

**Authentication**: Internal DWP service authentication

**Priority**: COULD_HAVE

---

### INT-004: GOV.UK One Login

**Purpose**: Employer authentication

**Integration Type**: OpenID Connect

**Data Exchanged**: Authentication tokens, user identity claims

**Priority**: MUST_HAVE

---

### INT-005: GOV.UK Notify

**Purpose**: Transactional emails (application confirmation, assessment outcome, renewal reminders, employee feedback invitations)

**Integration Type**: REST API

**Data Exchanged**: Email templates, recipient addresses, personalisation data

**Authentication**: GOV.UK Notify API key

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity: Employer

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| companies_house_number | String(8) | No | Companies House registration number |
| name | String(255) | Yes | Employer name |
| sector | Enum | Yes | SIC code / sector classification |
| size_band | Enum | Yes | micro, small, medium, large |
| locations | JSON | Yes | Array of workplace locations |
| dc_level | Enum | Yes | none, committed, employer, leader |
| certification_date | Date | No | Current certification date |
| expiry_date | Date | No | Certification expiry date |

#### Entity: Application

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| employer_id | UUID | Yes | Applying employer |
| level_applied | Enum | Yes | committed, employer, leader |
| status | Enum | Yes | draft, submitted, in_review, approved, rejected, conditional |
| submitted_date | Timestamp | No | When submitted |
| decision_date | Timestamp | No | When decision made |
| assessor_id | UUID | No | Assigned assessor |

#### Entity: EvidenceItem

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| application_id | UUID | Yes | Parent application |
| category | Enum | Yes | recruitment, adjustments, retention, culture, leadership |
| file_path | String(500) | Yes | Secure storage path |
| uploaded_date | Timestamp | Yes | When uploaded |
| assessor_score | Integer | No | Score (1-5) |
| assessor_comments | Text | No | Assessment comments |

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Application-to-certification time | 8 weeks | 2 weeks | 12 months | Portal workflow analytics |
| Evidence-based Level 2-3 certifications | 0% | 100% | 18 months | Assessment records |
| Access to Work referrals via portal | 0 | 500/quarter | 12 months | Referral tracking |
| Employers reporting workforce data | 0% | 50% of Level 2-3 | 24 months | Data submission logs |
| Scheme membership retention | 85% | 80%+ (during transition) | 18 months | Membership database |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Equality Act 2010 | Legislation | legislation.gov.uk | Reasonable adjustments duty | N/A |
| Disability Confident Scheme Guidance | Policy | GOV.UK | Scheme levels and criteria | N/A |
| National Disability Strategy | Strategy | GOV.UK | Employment gap targets | N/A |
| ARC-004-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | projects/004-disability-confident-employer-portal/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Disability Confident Employer Portal
**Model**: Claude Opus 4.6
