# Project Requirements: Apprenticeship Matching Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Apprenticeship Matching Service (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, AMS Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | AMS Programme Board, ESFA, Development Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Apprenticeship Matching Service (AMS), which will replace the ageing Find an Apprenticeship service with a modern, skills-matched platform connecting apprentices with employers.

---

## Executive Summary

### Business Context

Apprenticeship vacancy fill rates stand at 65%, while youth unemployment remains stubbornly above 10%. The current Find an Apprenticeship service is a basic vacancy listing with no skills matching, limited employer support, and poor mobile experience. The AMS will introduce intelligent matching based on skills, interests, location, and aptitude — bringing the apprenticeship search experience in line with modern recruitment platforms while maintaining the equity objectives that differentiate government services from commercial alternatives.

### Objectives

- Replace Find an Apprenticeship with a modern, mobile-first matching platform
- Introduce skills-based matching between apprentice profiles and employer vacancies
- Integrate with the Apprenticeship Service employer accounts and ESFA funding systems
- Ensure equitable access for disadvantaged young people (care leavers, SEND, FSM-eligible)
- Reduce time from application to apprenticeship start

### Project Scope

**In Scope**:

- Apprentice profile creation and skills assessment
- Employer vacancy listing with structured skills requirements
- Skills-based matching algorithm
- Application management workflow (apply, shortlist, interview, offer)
- Training provider directory and matching
- Integration with Apprenticeship Service and ESFA funding
- Mobile-responsive design (mobile-first for apprentice experience)
- Employer dashboard (vacancy management, candidate pipeline)
- Disadvantage targeting and monitoring

**Out of Scope**:

- Apprenticeship training delivery management (ESFA systems)
- Levy management and transfer functionality (Apprenticeship Service)
- End-point assessment management (IfATE/EPAO systems)
- Careers guidance content (Careers & Enterprise Company)

---

## Business Requirements

### BR-1: Skills-Based Matching

**Description**: Match apprenticeship seekers with vacancies based on skills, interests, aptitude, location, and accessibility requirements — not just keyword search.

**Rationale**: Current keyword-based search misses relevant opportunities and surfaces irrelevant ones. Skills matching improves fill rates and retention.

**Success Criteria**:

- 80% of apprentices report matched vacancies are "relevant" or "highly relevant"
- Vacancy fill rate increases from 65% to 80%
- 12-month retention rate for matched apprenticeships exceeds 75%

**Priority**: MUST_HAVE

---

### BR-2: Equitable Access for Disadvantaged Groups

**Description**: The platform must proactively support access for disadvantaged young people, including care leavers, young people with SEND, those eligible for FSM, and those from areas of high deprivation.

**Rationale**: SDG 4 requires inclusive education. Apprenticeships are a critical social mobility route, and the matching service must not inadvertently disadvantage already-marginalised groups.

**Success Criteria**:

- 30% of successful matches involve disadvantaged young people
- Accessibility: WCAG 2.2 Level AA, Easy Read summaries, BSL video descriptions for top vacancies
- Anonymised applications available to reduce bias
- Monitoring dashboard tracks outcomes by disadvantage indicator

**Priority**: MUST_HAVE

---

### BR-3: Employer Vacancy Management

**Description**: Enable employers to create, manage, and promote apprenticeship vacancies through a self-service portal with guided vacancy creation for SMEs.

**Rationale**: Employer experience is critical — if creating a vacancy is complex, SMEs will not participate. Large employers need bulk management tools.

**Success Criteria**:

- SME vacancy creation in under 15 minutes with guided flow
- Large employer bulk vacancy upload via CSV/API
- Vacancy quality validation (clear description, salary, location, training provider)
- 70% of employers rate vacancy creation as "easy" or "very easy"

**Priority**: MUST_HAVE

---

### BR-4: Application Management Workflow

**Description**: Provide a structured workflow from application through shortlisting, interview scheduling, offer, and confirmed start — with status tracking for both parties.

**Rationale**: The current process often involves email-based communication with no tracking, leading to lost applications and poor candidate experience.

**Success Criteria**:

- Apprentices can track application status in real time
- Employers can shortlist, communicate with, and progress candidates through the workflow
- Automated notifications at each stage transition
- Time from application to offer measurable and reported

**Priority**: MUST_HAVE

---

### BR-5: ESFA Funding Integration

**Description**: Integrate with ESFA funding systems so that confirmed matches automatically trigger the correct funding pathway (Levy, co-investment, or SME incentive).

**Rationale**: Manual funding processes delay apprenticeship starts and create errors. Automated integration reduces time-to-start and ensures funding compliance.

**Success Criteria**:

- Funding pathway automatically determined based on employer type, apprenticeship standard, and apprentice characteristics
- Zero manual funding interventions required for standard matches
- Funding confirmation communicated to employer and training provider within 48 hours of confirmed start

**Priority**: MUST_HAVE

---

### BR-6: Training Provider Discovery

**Description**: Enable apprentices and employers to discover and compare training providers for their chosen apprenticeship standard, with quality ratings and Ofsted grades.

**Rationale**: Training provider quality varies significantly. Transparent quality information helps apprentices and employers make informed choices.

**Success Criteria**:

- Training providers listed with Ofsted grade, achievement rate, employer satisfaction, and learner satisfaction
- Providers filterable by location, standard, delivery mode (day release, block release, remote)
- Provider profiles include apprentice testimonials and employer references

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Jade — 17-year-old from Wolverhampton

- **Role**: A-level student considering apprenticeship vs university
- **Goals**: Explore apprenticeships in digital marketing; understand earning potential; find opportunities within commuting distance
- **Pain Points**: Current site looks "old-fashioned" compared to Indeed; cannot filter by commute time; job descriptions are confusing with jargon
- **Technical Proficiency**: High (digital native, uses smartphone for everything)
- **Context**: First in family to consider post-18 options; eligible for FSM; no car

#### Persona 2: Mark — Operations Director, Manufacturing SME (45 employees)

- **Role**: Wants to hire 2 engineering apprentices but overwhelmed by the process
- **Goals**: Post a vacancy, find suitable candidates, understand funding, select a training provider
- **Pain Points**: Tried Apprenticeship Service last year, gave up after 2 hours of forms; does not understand Levy/co-investment; received 40 applications but none were suitable
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-1: Apprentice Profile and Skills Assessment

**Description**: Enable apprenticeship seekers to create a profile including interests, skills self-assessment, qualifications, location, and accessibility needs.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a young person visits the platform, when they start profile creation, then they complete a 10-minute guided skills and interests assessment
- [ ] Given a user completes the assessment, when they view their profile, then they see suggested apprenticeship sectors and standards based on their responses
- [ ] Given a user has SEND or accessibility needs, when they indicate this, then the platform adjusts the experience (e.g., simplified language, extended time for assessments)
- [ ] Edge case: Users without qualifications can still create a meaningful profile based on skills and interests

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-2: Intelligent Vacancy Matching

**Description**: Match apprentice profiles with employer vacancies using skills, interests, location, and accessibility requirements.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an apprentice has a completed profile, when they view recommendations, then they see vacancies ranked by match score with explanation of why each is recommended
- [ ] Given an employer has a vacancy, when they view candidates, then they see matched profiles ranked by suitability
- [ ] Given location is a filter, when applied, then results show commute time by public transport (not just distance)
- [ ] Edge case: When no strong matches exist, the system suggests related apprenticeship standards the user may not have considered

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-3: Employer Vacancy Creation (SME Flow)

**Description**: Guided vacancy creation for SME employers with step-by-step wizard, plain language guidance, and automatic mapping to apprenticeship standards.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given an SME employer starts vacancy creation, when they describe the role in plain language, then the system suggests matching apprenticeship standards
- [ ] Given an employer selects a standard, when they proceed, then required skills, salary guidance, and training provider options are pre-populated
- [ ] Given an employer completes the wizard, when the vacancy is submitted, then it is published within 24 hours after automated quality checks
- [ ] Edge case: Employers who cannot identify a matching standard are connected to NAS helpline

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-4: Application Tracking Pipeline

**Description**: End-to-end application workflow from apply through shortlist, interview, offer, and confirmed start.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given an apprentice applies for a vacancy, when the application is submitted, then the employer receives a notification and the apprentice sees "Application Submitted" status
- [ ] Given an employer shortlists a candidate, when the status changes, then the apprentice is notified and can see "Shortlisted" status
- [ ] Given an employer makes an offer, when accepted, then both parties see confirmed match status and the ESFA funding integration is triggered
- [ ] Edge case: When an apprentice is unsuccessful, they receive constructive feedback prompts (optional for employer to complete)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-5: ESFA Funding Pathway Integration

**Description**: Automatic determination of funding pathway based on employer type, standard, and apprentice characteristics.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a match is confirmed, when the system checks employer Levy status, then it automatically determines Levy drawdown, co-investment, or SME incentive pathway
- [ ] Given the funding pathway is determined, when the employer and provider are notified, then a funding commitment is confirmed within 48 hours
- [ ] Given an apprentice qualifies for additional support (SEND, care leaver), when funding is calculated, then additional support funding is automatically included

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-6: Anonymised Applications

**Description**: Option for employers to receive anonymised applications (no name, age, gender, ethnicity) to reduce unconscious bias in shortlisting.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an employer enables anonymised applications, when they review candidates, then personal details are hidden until shortlisting is complete
- [ ] Given an apprentice applies to an anonymised vacancy, when their application is submitted, then they are informed that initial review will be anonymous

**Priority**: SHOULD_HAVE
**Complexity**: LOW

---

## Non-Functional Requirements

### NFR-P-1: Mobile Performance

**Requirement**: Mobile page load within 2 seconds on 4G connection. Apprentice-facing flows must work on low-specification smartphones (Android 10+, 2GB RAM).

**Priority**: CRITICAL

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability. Enhanced availability during National Apprenticeship Week and UCAS results day.

**Priority**: HIGH

---

### NFR-SEC-1: Data Protection

**Requirement**: Full UK GDPR compliance. Apprentice data (including age, SEND status, care leaver status) classified as OFFICIAL-SENSITIVE. Anonymisation of analytics data. Right to erasure supported. AADC compliance where under-18 users are involved.

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. Easy Read summaries for top 100 vacancies. High-contrast mode. Screen reader compatible. BSL video descriptions for featured employers.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Apprenticeship Service (Employer Accounts)

**Purpose**: Link employer accounts from the Apprenticeship Service for Levy status, transfer availability, and account verification.
**Integration Type**: Real-time API
**Priority**: CRITICAL

---

### INT-2: ESFA Funding Systems

**Purpose**: Trigger funding commitments for confirmed matches.
**Integration Type**: Real-time API with batch reconciliation
**Priority**: CRITICAL

---

### INT-3: IfATE Apprenticeship Standards Database

**Purpose**: Authoritative source for apprenticeship standards, duties, KSBs, and assessment plans.
**Integration Type**: Daily batch synchronisation
**Priority**: MUST_HAVE

---

### INT-4: DfE Sign-in / GOV.UK One Login

**Purpose**: Authentication for employers and training providers.
**Integration Type**: SAML 2.0 / OpenID Connect
**Priority**: MUST_HAVE

---

### INT-5: Ofsted Data

**Purpose**: Training provider inspection grades and achievement rates for quality display.
**Integration Type**: Batch API (monthly)
**Priority**: SHOULD_HAVE

---

## Data Requirements

### DR-1: Apprentice Profile

**Attributes**: profile_id, name, date_of_birth, location (postcode), qualifications, skills_assessment_results, interests, accessibility_needs, disadvantage_indicators (FSM, care_leaver, SEND, IMD_decile), preferred_sectors, preferred_commute_time

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: 24 months after last activity, then deleted
**Data Volume**: 500,000 active profiles (Year 1), 1.2M (Year 3)

---

### DR-2: Apprenticeship Vacancy

**Attributes**: vacancy_id, employer_id, standard_id, title, description, location, salary, working_hours, required_skills, training_provider_id, start_date, closing_date, vacancies_available, anonymised_applications_enabled

**Data Classification**: OFFICIAL
**Data Volume**: 100,000 active vacancies at any time

---

### DR-3: Match Record

**Attributes**: match_id, apprentice_profile_id, vacancy_id, match_score, match_reasons, application_date, current_status (applied, shortlisted, interview, offered, confirmed, withdrawn, rejected), status_history, funding_pathway

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: 6 years (aligned with apprenticeship funding audit requirements)

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Vacancy fill rate | 65% | 80% | 18 months | Platform data |
| Successful matches (Year 1) | ~42,000 | 50,000 | 12 months | Confirmed starts |
| Disadvantaged matches | ~20% | 30% | 12 months | Platform analytics |
| Time to start | 12 weeks | 6 weeks | 12 months | Platform data |
| Apprentice match relevance | N/A | 80% rate "relevant" | 6 months | User survey |
| SME vacancy creation time | ~45 min | < 15 min | At launch | Platform analytics |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Apprenticeship Matching Service
**Model**: Claude Opus 4.6
