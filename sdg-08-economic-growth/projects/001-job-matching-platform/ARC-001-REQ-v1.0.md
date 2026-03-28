# Project Requirements: Job Matching Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Job Matching Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Job Matching Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Job Matching Programme Board, DWP Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the AI-powered Job Matching Platform. It provides a traceable link from stakeholder goals (ARC-001-STKE-v1.0) to specific, testable requirements that will guide design and implementation.

---

## Executive Summary

### Business Context

The Department for Work and Pensions (DWP) operates the Find a Job service, which connects approximately 1.5 million active jobseekers (including 6 million Universal Credit households) with employer vacancies. The current service uses basic keyword matching, resulting in an 8% application-to-interview conversion rate. Employers report poor candidate quality, and jobseekers waste time applying for unsuitable roles. The AI-powered Job Matching Platform will replace Find a Job with an intelligent matching engine that considers skills, experience, location (including public transport accessibility), career aspirations, and labour market context.

### Objectives

- Increase application-to-interview conversion rate from 8% to 20% through AI-powered skills-based matching
- Reduce average UC claim duration for jobseeking claimants by 20% (from 9.2 to 7.5 months)
- Augment work coach capacity, increasing average caseload from 120 to 160 with maintained outcomes
- Achieve employer adoption of 50,000 active employers within 12 months
- Ensure algorithmic fairness with less than 5% variance across protected characteristics

### Expected Outcomes

- GBP 1.5B estimated annual UC payment savings from reduced claim duration
- GBP 180M annual operational efficiency from increased work coach capacity
- Improved jobseeker satisfaction and employment sustainability (75% at 6 months vs. 62% baseline)

### Project Scope

**In Scope**:
- AI matching engine for jobseeker-vacancy matching
- Work coach dashboard with AI recommendations and override capability
- Employer vacancy management portal with ATS integration
- Universal Credit integration for claimant commitment recording
- Skills taxonomy mapping (ESCO/SOC) and Skills Passport integration
- Bias monitoring and algorithmic transparency reporting

**Out of Scope**:
- Universal Credit payment calculations (remains in UC system)
- Training and skills provision (referral only, via Skills Passport)
- International job matching (UK vacancies only)
- Recruitment agency white-label service

---

## Business Requirements

### BR-001: AI-Powered Job Matching

**Description**: The platform must use artificial intelligence to match jobseekers to suitable vacancies based on skills, experience, qualifications, location, career aspirations, and individual circumstances, producing materially better matches than keyword search.

**Rationale**: The current Find a Job service's keyword matching produces an 8% application-to-interview rate. AI matching using skills taxonomies and contextual data can significantly improve match quality, reducing wasted effort for both jobseekers and employers.

**Success Criteria**:
- Application-to-interview conversion rate exceeds 20% (vs. 8% baseline)
- Jobseeker satisfaction with recommendation relevance exceeds 65%
- Employer satisfaction with candidate quality exceeds 70%

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Employers (SD-3), Jobseekers (SD-4)

---

### BR-002: Work Coach Augmentation

**Description**: The platform must provide work coaches with AI-generated job recommendations for their caseload, presented as suggestions that coaches can accept, modify, or override based on their professional judgement of individual circumstances.

**Rationale**: Work coaches have expertise in individual barriers, local labour markets, and employer relationships that AI cannot replicate. The system must augment, not replace, their professional judgement. Coach adoption is critical to platform success.

**Success Criteria**:
- Work coach caseload capacity increases from 120 to 160 with maintained outcome rates
- Work coach satisfaction with AI recommendations exceeds 3.5/5
- AI recommendation override rate monitored (target: 10-30% indicating appropriate coach engagement)

**Priority**: MUST_HAVE

**Stakeholder**: Work Coaches (SD-2), UC Operations Director

---

### BR-003: Universal Credit Integration

**Description**: The platform must integrate with the Universal Credit system to record job search activity, satisfy claimant commitment requirements, and report employment outcomes, without requiring dual-keying by work coaches or claimants.

**Rationale**: Approximately 6 million households claim UC. Jobseekers have claimant commitments mandating job search activity. The platform must record activity that satisfies these commitments and flow employment outcomes back to UC to adjust payments.

**Success Criteria**:
- Job search activity recorded in UC system within 5 minutes of platform interaction
- No dual-keying required for work coaches or claimants
- Employment outcomes (start dates, earnings) flow from HMRC RTI to UC via platform

**Priority**: MUST_HAVE

**Stakeholder**: UC Operations Director, Jobseekers (SD-4)

---

### BR-004: Employer Vacancy Management

**Description**: The platform must enable employers to post, manage, and track vacancies with minimal effort, including integration with major Applicant Tracking Systems (ATS) for automated vacancy import and outcome reporting.

**Rationale**: The platform is only valuable if employers use it. Find a Job had declining employer engagement. The new platform must compete with commercial alternatives on ease of use while offering unique value (access to UC claimant pool, work coach referrals).

**Success Criteria**:
- 50,000 active employers within 12 months
- Average vacancy posting time under 5 minutes
- ATS integration available for top 5 ATS platforms

**Priority**: MUST_HAVE

**Stakeholder**: Employers (SD-3)

---

### BR-005: Algorithmic Fairness and Transparency

**Description**: The platform must ensure that AI matching recommendations do not systematically disadvantage any group defined by protected characteristics under the Equality Act 2010, with mandatory bias testing, published transparency records, and independent audit.

**Rationale**: AI bias in job matching could systematically disadvantage women, ethnic minorities, disabled people, or older workers. This would violate the Equality Act, create political crisis, and undermine public trust in AI.

**Success Criteria**:
- Less than 5% variance in match quality metrics across all nine protected characteristics
- Algorithmic Transparency Record published on GOV.UK
- Quarterly independent bias audit completed and published
- Disparate impact ratio above 0.8 (four-fifths rule) for all protected groups

**Priority**: MUST_HAVE

**Stakeholder**: Jobseekers (SD-4), EHRC, ICO

---

### BR-006: Skills-Based Matching Using Open Standards

**Description**: The platform must use standardised skills taxonomies (ESCO mapped to UK SOC 2020) to match jobseekers to vacancies based on skills and competencies, not just job titles, enabling recognition of transferable skills across sectors.

**Rationale**: A nurse has transferable skills (empathy, attention to detail, crisis management) relevant to social work, customer service management, and health tech. Keyword matching misses these connections. Skills-based matching opens career pathways.

**Success Criteria**:
- Skills taxonomy covers 95% of active vacancy types
- Cross-sector skill transfer recommendations available for all occupational groups
- Integration with Skills Passport (Project 002) for verified credential matching

**Priority**: MUST_HAVE

**Stakeholder**: Jobseekers (SD-4), DfE/Skills Passport

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — UC Claimant Jobseeker

- **Role**: Unemployed, claiming Universal Credit, mandatory job search
- **Goals**: Find suitable work that fits around school hours, uses her retail management experience, and is accessible by bus
- **Pain Points**: Current system returns irrelevant results; location filter doesn't consider public transport; feels pressured to apply for anything
- **Technical Proficiency**: Medium (smartphone user, comfortable with apps)

#### Persona 2: James — Work Coach

- **Role**: Jobcentre Plus Work Coach, caseload of 130 claimants
- **Goals**: Help claimants find sustainable work; manage caseload efficiently; exercise professional judgement
- **Pain Points**: Spends 40% of time on admin; current system doesn't account for individual barriers; can't easily see local employer needs
- **Technical Proficiency**: High (uses multiple DWP systems daily)

#### Persona 3: Priya — SME Employer

- **Role**: HR manager at a 50-person manufacturing company
- **Goals**: Fill vacancies quickly with reliable candidates; avoid sifting through unsuitable applications
- **Pain Points**: Find a Job sends volume, not quality; no integration with her ATS; doesn't understand government job platforms
- **Technical Proficiency**: Medium

#### Persona 4: David — Large Employer Recruiter

- **Role**: Recruitment lead at a national retailer
- **Goals**: Bulk vacancy posting across 200+ locations; candidate pre-screening; diversity in shortlists
- **Pain Points**: Cannot bulk-upload vacancies; no API integration; manual outcome reporting
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: Jobseeker Profile Creation

**Description**: The system must enable jobseekers to create a profile including skills, experience, qualifications, location, transport preferences, availability, and career aspirations. Where the jobseeker authenticates via GOV.UK One Login, the system must pre-populate data from DWP/HMRC records with consent.

**Relates To**: BR-001, BR-006

**Acceptance Criteria**:
- [ ] Given a new jobseeker, when they authenticate via GOV.UK One Login, then known data (name, NI number, address, UC status) is pre-populated
- [ ] Given a jobseeker with a Skills Passport, when they link their passport, then verified credentials are imported automatically
- [ ] Given a jobseeker without digital access, when a work coach creates a profile on their behalf, then all features are available via the coach dashboard

**Priority**: MUST_HAVE

---

#### FR-002: AI Job Recommendation Engine

**Description**: The system must generate personalised job recommendations for each jobseeker based on their profile, using machine learning models trained on skills taxonomies, historical employment outcomes, and labour market context.

**Relates To**: BR-001, BR-005

**Acceptance Criteria**:
- [ ] Given a completed jobseeker profile, when the recommendation engine runs, then at least 10 relevant vacancies are returned ranked by suitability score
- [ ] Given each recommendation, when the jobseeker views it, then an explanation is provided showing why the role was recommended (skills match, location, salary)
- [ ] Given a recommendation that the jobseeker considers unsuitable, when they provide feedback, then future recommendations adjust accordingly
- [ ] Edge case: When no vacancies match within 30 miles, the system suggests remote roles or nearby roles with public transport analysis

**Priority**: MUST_HAVE

---

#### FR-003: Bias Detection and Monitoring

**Description**: The system must continuously monitor AI recommendations for bias across all nine protected characteristics, with automated alerts when variance exceeds defined thresholds.

**Relates To**: BR-005

**Acceptance Criteria**:
- [ ] Given production recommendations over a 7-day window, when bias monitoring runs, then variance across protected groups is calculated and logged
- [ ] Given variance exceeding 5% for any characteristic, when detected, then automated alert sent to Data Science team and AI Ethics Board
- [ ] Given a bias incident, when the model is adjusted, then the adjustment is logged with rationale in the model version history

**Priority**: MUST_HAVE

---

#### FR-004: Work Coach Dashboard

**Description**: The system must provide work coaches with a dashboard showing their caseload, AI-generated recommendations for each claimant, and tools to accept, modify, or override recommendations with recorded rationale.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a work coach logging in, when the dashboard loads, then their full caseload is displayed with priority indicators
- [ ] Given a claimant record, when the coach reviews it, then AI recommendations are shown alongside claimant circumstances and local labour market context
- [ ] Given a coach override of an AI recommendation, when the coach provides a rationale, then the override is recorded and used to improve future model accuracy
- [ ] Given a coach referral to an employer, when the employer receives it, then the referral is tagged as "work coach recommended"

**Priority**: MUST_HAVE

---

#### FR-005: Employer Vacancy Posting

**Description**: The system must enable employers to post vacancies with structured data including role description, required skills (using ESCO taxonomy), location, salary, working pattern, and accessibility information.

**Relates To**: BR-004

**Acceptance Criteria**:
- [ ] Given an employer, when posting a vacancy, then the system suggests ESCO skills based on the job title and description
- [ ] Given an SME employer, when posting their first vacancy, then the guided flow completes in under 5 minutes
- [ ] Given a large employer with ATS integration, when vacancies are created in their ATS, then they automatically appear on the platform within 15 minutes

**Priority**: MUST_HAVE

---

#### FR-006: Universal Credit Activity Recording

**Description**: The system must record jobseeker activity (searches, applications, interviews, outcomes) and transmit it to the Universal Credit system in real-time to satisfy claimant commitment requirements.

**Relates To**: BR-003

**Acceptance Criteria**:
- [ ] Given a jobseeker applying for a role, when the application is submitted, then the activity is recorded in UC within 5 minutes
- [ ] Given a work coach referral, when the jobseeker attends an interview, then attendance is recorded automatically via employer confirmation
- [ ] Given UC system unavailability, when the platform cannot transmit activity, then activity is queued and transmitted when connectivity resumes, with no data loss

**Priority**: MUST_HAVE

---

#### FR-007: Location and Commute Analysis

**Description**: The system must calculate commute feasibility for each vacancy-jobseeker combination using public transport data, not just straight-line distance, and factor commute time into match scoring.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given a jobseeker's location and a vacancy location, when calculating commute, then public transport journey time is used (bus, train, tram)
- [ ] Given a maximum commute preference of 45 minutes, when matching, then only vacancies reachable within 45 minutes by public transport are included
- [ ] Given a jobseeker with a car, when they indicate driving, then driving time and parking availability are also considered

**Priority**: SHOULD_HAVE

---

#### FR-008: Career Pathway Recommendations

**Description**: The system must suggest career progression pathways showing how a jobseeker's current skills could lead to higher-skilled, higher-paid roles with additional training or experience.

**Relates To**: BR-006

**Acceptance Criteria**:
- [ ] Given a jobseeker with retail experience, when viewing career pathways, then progression routes (e.g., retail manager, operations manager, buyer) are displayed with skills gap analysis
- [ ] Given a career pathway with a skills gap, when the jobseeker selects it, then relevant training opportunities are shown (linked to Skills Passport)

**Priority**: SHOULD_HAVE

---

#### FR-009: Employer Outcome Reporting

**Description**: The system must enable employers to report hiring outcomes (shortlisted, interviewed, offered, hired, still employed at 6 months) to close the feedback loop and improve AI model accuracy.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:
- [ ] Given an application, when the employer updates its status, then the AI model receives the outcome for training
- [ ] Given HMRC RTI data, when an employment start is detected for a matched jobseeker, then the outcome is automatically recorded

**Priority**: MUST_HAVE

---

#### FR-010: Algorithmic Transparency Reporting

**Description**: The system must generate and publish an Algorithmic Transparency Record on GOV.UK conforming to the CDDO Algorithmic Transparency Recording Standard.

**Relates To**: BR-005

**Acceptance Criteria**:
- [ ] Given the AI matching model, when the transparency record is generated, then it includes purpose, data used, model type, fairness metrics, and human oversight mechanisms
- [ ] Given an update to the model, when a new version is deployed, then the transparency record is updated within 5 working days

**Priority**: MUST_HAVE

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Job Search Response Time

**Requirement**: Job search results (AI-matched) must be returned within 500ms at p95 under peak load conditions.

**Load Conditions**:
- Peak: 50,000 concurrent users (mass redundancy event scenario)
- Average: 15,000 concurrent users
- Data volume: 500,000 active vacancies, 5 million jobseeker profiles

**Priority**: MUST_HAVE

---

#### NFR-P-002: Recommendation Engine Throughput

**Requirement**: The AI recommendation engine must process batch recommendations for all active jobseekers (5 million profiles) overnight for next-day coach dashboard availability, and real-time recommendations for individual jobseekers within 500ms.

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Authentication via GOV.UK One Login

**Requirement**: All jobseeker and employer authentication must use GOV.UK One Login. Work coach authentication must use DWP's internal SSO (Azure AD) with MFA.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Data Encryption

**Requirement**: All data at rest encrypted with AES-256. All data in transit encrypted with TLS 1.3. Application-level encryption for PII fields (NI number, date of birth, address).

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: AI Model Security

**Requirement**: AI model artefacts, training data, and hyperparameters must be stored in secure, access-controlled repositories. Model inference endpoints must be authenticated. Adversarial attack testing (model evasion, data poisoning) must be conducted before deployment.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Platform Availability

**Requirement**: 99.9% availability (43.8 minutes maximum downtime per month). RTO: 30 minutes. RPO: 5 minutes.

**Priority**: MUST_HAVE

---

### Accessibility Requirements

#### NFR-U-001: WCAG 2.2 Level AA

**Requirement**: Full WCAG 2.2 Level AA compliance for all citizen-facing interfaces. Screen reader compatibility (JAWS, NVDA, VoiceOver). Keyboard-only navigation for all functions.

**Priority**: MUST_HAVE (legal requirement under Public Sector Bodies Accessibility Regulations 2018)

---

### Compliance Requirements

#### NFR-C-001: UK GDPR Compliance

**Requirement**: Full compliance with UK GDPR including data subject rights (access, rectification, erasure, portability), lawful basis documentation, DPIA for AI processing, and 72-hour breach notification.

**Priority**: MUST_HAVE

---

#### NFR-C-002: Equality Act 2010 Compliance

**Requirement**: AI matching must comply with the Equality Act 2010. Bias testing must cover all nine protected characteristics. Positive action measures may be implemented where evidenced disparity exists.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Universal Credit System

**Purpose**: Record job search activity and employment outcomes for benefit conditionality

**Integration Type**: Real-time API (event-driven)

**Data Exchanged**:
- **To UC**: Job search activity events, application records, interview attendance, employment outcomes
- **From UC**: Claimant commitment details, conditionality group, appointment schedule

**Authentication**: Mutual TLS with DWP service mesh
**SLA**: 99.9% availability, < 200ms latency
**Priority**: MUST_HAVE

---

### INT-002: HMRC Real Time Information (RTI)

**Purpose**: Verify employment outcomes (start dates, earnings) for model training and UC payment adjustment

**Integration Type**: Daily batch feed + event notification for new employment starts

**Data Exchanged**:
- **From HMRC**: Employment start/end events, earnings data (anonymised for model training, individual for UC verification)

**Authentication**: HMRC secure data sharing gateway
**SLA**: Daily batch within 3 working days, event notifications within 24 hours
**Priority**: MUST_HAVE

---

### INT-003: Skills Passport System (Project 002)

**Purpose**: Import verified credentials for skills-based matching

**Integration Type**: Real-time API with user consent

**Data Exchanged**:
- **From Skills Passport**: Verified credentials (qualifications, certifications, skills badges)
- **To Skills Passport**: Skills gap analysis, recommended training pathways

**Authentication**: OAuth 2.0 with individual consent
**Priority**: SHOULD_HAVE

---

### INT-004: Companies House

**Purpose**: Employer verification and vacancy enrichment

**Integration Type**: Real-time API

**Data Exchanged**:
- **From Companies House**: Company registration data, SIC codes, registered address, director information

**Authentication**: Companies House API key
**Priority**: SHOULD_HAVE

---

### INT-005: Public Transport APIs

**Purpose**: Commute time calculation for location-based matching

**Integration Type**: Real-time API

**Data Exchanged**:
- **From Transport APIs**: Journey times, route options, service frequency

**Authentication**: API key
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity: Jobseeker Profile

| Attribute | Type | Required | Description | Classification |
|-----------|------|----------|-------------|----------------|
| profile_id | UUID | Yes | Unique identifier | OFFICIAL |
| ni_number | String(9) | Yes | National Insurance number | OFFICIAL-SENSITIVE |
| name | String | Yes | Full name | OFFICIAL |
| date_of_birth | Date | Yes | Date of birth | OFFICIAL |
| address | Object | Yes | Current address | OFFICIAL |
| skills | Array[Skill] | Yes | ESCO-mapped skills | OFFICIAL |
| qualifications | Array[Credential] | No | Verified credentials from Skills Passport | OFFICIAL |
| work_history | Array[Employment] | Yes | Employment history | OFFICIAL |
| preferences | Object | Yes | Location, hours, salary preferences | OFFICIAL |
| uc_status | Enum | Yes | UC conditionality group | OFFICIAL |
| protected_characteristics | Object | Optional | Voluntary disclosure for bias monitoring | OFFICIAL-SENSITIVE |

**Data Volume**: 5 million active profiles, 20 million historical
**Retention**: Active profiles retained while claimant is active + 6 years. Anonymised for model training after 2 years.
**Classification**: OFFICIAL (profile data), OFFICIAL-SENSITIVE (NI number, protected characteristics)

---

### Data Quality Requirements

**Accuracy**: Skills taxonomy mapping validated against ESCO/SOC with automated quality checks
**Completeness**: Minimum viable profile (name, location, 3 skills) required for matching
**Consistency**: Cross-validated with UC, HMRC, and Skills Passport data sources
**Timeliness**: Vacancy data refreshed every 15 minutes; profile data updated on user interaction

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with DWP's existing UC system without requiring UC re-architecture
**TC-2**: Must deploy on UK sovereign cloud (AWS London or Azure UK South)
**TC-3**: Must use GOV.UK One Login for citizen authentication (GDS mandate)

### Business Constraints

**BC-1**: Must maintain uninterrupted UC benefit payments throughout development and rollout
**BC-2**: Total programme budget capped at GBP 25M over 3 years
**BC-3**: Must pass GDS service assessment at Beta before national rollout

### Assumptions

**A-1**: Employers will adopt the platform in sufficient numbers (validated via employer advisory panel)
**A-2**: HMRC will agree to amended data sharing agreement for AI-related RTI usage
**A-3**: GOV.UK One Login will be available and stable for DWP integration by Beta

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Application-to-interview rate | 8% | 20% | 12 months post-beta | Platform analytics |
| Average UC claim duration | 9.2 months | 7.5 months | 18 months post-rollout | DWP Stat-Xplore |
| Employment sustainability (6 months) | 62% | 75% | 18 months post-rollout | HMRC RTI |
| Active employer count | 25,000 | 50,000 | 12 months post-beta | Platform CRM |
| Work coach caseload | 120 | 160 | 12 months post-rollout | Workforce management |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals, conflicts | `projects/001-job-matching-platform/ARC-001-STKE-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Job Matching Platform
**Model**: Claude Opus 4.6
