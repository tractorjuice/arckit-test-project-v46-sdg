# Project Requirements: Teacher Recruitment Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Teacher Recruitment Portal (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, TRP Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | TRP Programme Board, DfE Teacher Supply Division, Development Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Teacher Recruitment Portal (TRP), which will provide a unified digital service for discovering, applying to, and onboarding into Initial Teacher Training programmes in England.

---

## Executive Summary

### Business Context

England faces a severe teacher recruitment crisis with secondary ITT targets missed for 11 consecutive years in shortage subjects. The current recruitment journey is fragmented across Get Into Teaching (information), DfE Apply / UCAS Teacher Training (applications), and individual provider websites (course details). This fragmentation creates a poor candidate experience, high abandonment rates (35%), and disproportionately deters career changers and candidates from underrepresented backgrounds. The TRP will unify the entire journey from initial interest through application, offer, pre-employment checks, and training start.

### Objectives

- Unify the teacher recruitment journey from discovery through application to onboarding
- Increase applications for shortage subjects (Physics, Maths, MFL, Computing) by 25%
- Reduce application abandonment from 35% to below 15%
- Integrate DBS and TRA checks to reduce offer-to-start time
- Improve diversity of the applicant pool

### Project Scope

**In Scope**:

- "Route finder" tool — guided assessment to recommend suitable ITT routes
- Course search and comparison (by subject, location, provider, route)
- Unified application form (replacing UCAS Teacher Training and legacy systems)
- Provider profiles with course details, Ofsted grades, and trainee satisfaction
- Application tracking for candidates and providers
- DBS enhanced disclosure integration
- TRA qualified teacher status and prohibition check integration
- Bursary/scholarship eligibility calculator
- Get Into Teaching marketing campaign integration
- Diversity monitoring and reporting

**Out of Scope**:

- ITT programme delivery and assessment (provider systems)
- Early Career Framework support (Teaching School Hubs)
- International teacher recruitment (separate programme)
- Supply teacher recruitment (commercial sector)

---

## Business Requirements

### BR-1: Unified Recruitment Journey

**Description**: Provide a single digital service covering the complete teacher recruitment journey from initial exploration ("Is teaching right for me?") through route selection, course discovery, application, offer management, pre-employment checks, and confirmed start.

**Rationale**: Candidates currently navigate 3-5 separate systems. Each handoff creates abandonment risk. A unified journey reduces friction and improves conversion.

**Success Criteria**:

- Candidate can progress from initial interest to submitted application in a single session
- 90% of ITT applications submitted through the portal within 18 months
- Application abandonment rate below 15%
- Candidate satisfaction (CSAT) score above 4.0/5.0

**Priority**: MUST_HAVE

---

### BR-2: Increase Shortage Subject Applications

**Description**: The portal must actively encourage and facilitate applications for shortage subjects through targeted messaging, bursary/scholarship visibility, and career changer support.

**Rationale**: Without targeted intervention, the portal will replicate existing application patterns (over-supply in popular subjects, under-supply in shortage subjects).

**Success Criteria**:

- 25% increase in shortage subject applications within 2 recruitment cycles
- Bursary/scholarship information displayed prominently at decision points
- Career changer route clearly signposted with relevant experience examples
- Subject-specific marketing campaigns integrated into the portal journey

**Priority**: MUST_HAVE

---

### BR-3: Course Search and Comparison

**Description**: Enable candidates to search, filter, and compare ITT courses by subject, location, provider type, route (PGCE, QTS, School Direct, SCITT), Ofsted grade, salary/bursary, and trainee satisfaction.

**Rationale**: Informed course choice reduces mismatched applications and improves trainee retention.

**Success Criteria**:

- All accredited ITT courses in England listed with consistent, structured information
- Filter by commute time (not just distance), salary/unsalaried, and provider Ofsted grade
- Course comparison (side-by-side) for up to 3 courses
- Provider profiles include trainee completion rates and employment rates

**Priority**: MUST_HAVE

---

### BR-4: Simplified Application Form

**Description**: Provide a single, streamlined application form that replaces the current UCAS and DfE Apply forms, pre-populating information where possible and reducing repetitive data entry.

**Rationale**: The current application form has 35% abandonment. Career changers report it takes 4-6 hours to complete. Simplification is the single highest-impact improvement.

**Success Criteria**:

- Application completable in under 90 minutes for a career changer (currently 4-6 hours)
- Candidate enters personal information once, regardless of number of course choices
- Work experience captured in flexible format (not requiring precise dates for historical roles)
- Personal statement guidance with examples provided (subject-specific)
- Application saves progress and can be resumed across devices

**Priority**: MUST_HAVE

---

### BR-5: Provider Application Management

**Description**: Provide ITT providers with a dashboard to manage received applications, communicate with candidates, schedule interviews, make offers, and track the candidate pipeline.

**Rationale**: Providers need practical tools to replace their existing application management workflows.

**Success Criteria**:

- Providers can view, filter, and sort applications by subject, status, and date
- Structured interview scheduling with candidate communication
- Offer management (conditional/unconditional, conditions tracking)
- Pipeline analytics showing conversion rates from application to start
- Bulk communication capability for provider open events

**Priority**: MUST_HAVE

---

### BR-6: DBS and TRA Integration

**Description**: Integrate DBS enhanced disclosure and TRA prohibition/QTS checks into the post-offer workflow, reducing manual processing and time-to-start.

**Rationale**: DBS checks currently take 4-6 weeks and involve paper-based forms. Integration reduces this to 2-3 weeks and eliminates manual data re-entry.

**Success Criteria**:

- DBS enhanced disclosure application initiated digitally from the portal
- TRA prohibition and QTS status checks automated at point of offer
- Average time from conditional offer to confirmed start reduced from 14 to 10 weeks
- Providers notified immediately when DBS clearance is received

**Priority**: SHOULD_HAVE

---

### BR-7: Route Finder Tool

**Description**: A guided assessment tool that asks candidates about their circumstances (degree subject, work experience, financial needs, location preferences) and recommends suitable ITT routes in plain language.

**Rationale**: The variety of ITT routes (PGCE, QTS-only, School Direct salaried/unsalaried, SCITT, Teach First, assessment-only) confuses candidates. A route finder manages complexity on behalf of the user.

**Success Criteria**:

- Route finder completable in under 5 minutes
- Recommendations explain the rationale in plain language
- Bursary/scholarship eligibility calculated automatically
- Links directly to matching courses from recommendation

**Priority**: MUST_HAVE

---

### BR-8: Diversity Monitoring and Targeted Marketing

**Description**: Monitor application diversity (ethnicity, gender, disability, socioeconomic background) and integrate with Get Into Teaching marketing campaigns to target underrepresented groups.

**Rationale**: The teaching profession does not reflect the diversity of the pupil population. Data-driven targeting of marketing campaigns is essential for improving diversity.

**Success Criteria**:

- Diversity data collected (voluntary) at application with demographic dashboard
- Marketing campaign effectiveness measurable by source, channel, and demographic
- Geographic targeting for areas with acute shortages
- Conversion funnel analysis by demographic group to identify barriers

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Dr. Chen — Career Changer (Physics)

- **Role**: Materials scientist, 8 years in industry, PhD in Physics
- **Goals**: Understand if she can train while earning; find a school-based route near Bristol; know what bursary she qualifies for
- **Pain Points**: Tried Get Into Teaching website — overwhelmed by acronyms (PGCE, SCITT, QTS); started UCAS form — abandoned after 2 hours; does not understand the difference between School Direct salaried and unsalaried
- **Technical Proficiency**: High
- **Context**: Motivated by desire to "give back" but cannot afford unpaid training; needs salary or substantial bursary

#### Persona 2: Jordan — Recent Graduate (English)

- **Role**: English Literature graduate (2:1), considering teaching or publishing
- **Goals**: Compare teaching with other career options; find a training provider near Manchester; understand what the first year of teaching is like
- **Pain Points**: Unsure if teaching is right for him; overwhelmed by choice of providers; does not know anyone who teaches
- **Technical Proficiency**: High (digital native)

#### Persona 3: Ms. Okoro — SCITT Director

- **Role**: Director of a School-Centred Initial Teacher Training programme (30 trainees/year)
- **Goals**: Attract quality candidates for her SCITT; manage applications efficiently; fill all training places before September
- **Pain Points**: Receives applications through 3 different channels; loses candidates to larger providers; cannot compete on marketing budget with universities
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-1: Route Finder Assessment

**Description**: Guided assessment recommending suitable ITT routes based on candidate circumstances.

**Relates To**: BR-7

**Acceptance Criteria**:

- [ ] Given a career changer indicates a physics degree and salary requirement, when they complete the route finder, then School Direct salaried and bursary-eligible PGCE routes are recommended
- [ ] Given a recent graduate with a 2:2 indicates primary teaching interest, when they complete the route finder, then routes with no minimum degree classification for primary are highlighted
- [ ] Given a candidate has teaching experience abroad, when they indicate this, then the assessment-only route is included in recommendations
- [ ] Edge case: When no routes match the candidate's criteria, the system suggests alternative paths (e.g., Subject Knowledge Enhancement before application)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-2: Course Search and Comparison

**Description**: Searchable course directory with filtering and side-by-side comparison.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a candidate searches for Physics PGCE courses near Bristol, when results appear, then courses are sorted by commute time with salary, bursary, and provider Ofsted grade visible
- [ ] Given a candidate selects 3 courses to compare, when the comparison view loads, then key attributes are displayed side-by-side (location, salary, route, provider grade, trainee satisfaction, employment rate)
- [ ] Given a course has limited places, when viewed, then remaining places are displayed (if >0) or "Course full" badge shown
- [ ] Edge case: When a provider has not submitted updated course data, the listing shows "Information from [year]" with last-updated date

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-3: Unified Application Form

**Description**: Single application form for up to 4 course choices, with save-and-resume and progressive disclosure.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a candidate starts an application, when they enter personal details, then these are pre-populated for all course choices
- [ ] Given a candidate saves progress, when they return on a different device, then they can resume from where they left
- [ ] Given a career changer enters work experience, when they describe roles, then they can use free-text descriptions rather than rigid date-range formats
- [ ] Given a candidate submits an application, when it is received by the provider, then the candidate sees "Submitted" status and the provider sees the complete application
- [ ] Edge case: When a provider declines a candidate, the candidate can redirect their application to alternative courses without re-entering information

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-4: Bursary and Scholarship Calculator

**Description**: Automated calculator showing bursary/scholarship eligibility based on subject, degree classification, and training route.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a candidate with a First in Physics selects a PGCE course, when the calculator runs, then it shows the GBP 28,000 tax-free bursary and GBP 30,000 scholarship option
- [ ] Given a candidate with a 2:2 in History, when the calculator runs, then it shows that History does not attract a bursary and explains alternative financial support
- [ ] Given bursary amounts change between recruitment cycles, when DfE updates the data, then the calculator reflects new amounts within 24 hours

**Priority**: MUST_HAVE
**Complexity**: LOW

---

#### FR-5: Provider Application Dashboard

**Description**: Dashboard for ITT providers to manage applications, track candidates through the pipeline, and communicate with applicants.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a provider accesses their dashboard, when they view applications, then they see a pipeline view (Received, Shortlisted, Interview Scheduled, Offered, Accepted, Declined)
- [ ] Given a provider wants to schedule an interview, when they select a candidate, then they can propose dates and the candidate receives an automated notification
- [ ] Given a provider makes an offer, when the offer is recorded, then the candidate receives a notification with response deadline and the DBS/TRA integration is triggered
- [ ] Edge case: When a candidate holds multiple offers, all providers see "Offer pending response" without knowing the identity of competing providers

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-6: DBS Enhanced Disclosure Integration

**Description**: Digital initiation of DBS enhanced disclosure from within the portal at point of conditional offer.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given a provider issues a conditional offer, when DBS check is required, then the candidate receives a guided workflow to complete DBS application within the portal
- [ ] Given DBS clearance is received, when the update arrives via DBS API, then the provider is automatically notified and the condition is marked as satisfied
- [ ] Given DBS disclosure reveals information, when the provider is notified, then the handling follows DBS code of practice (not automatic rejection)

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

#### FR-7: Get Into Teaching Campaign Integration

**Description**: Integration with Get Into Teaching marketing campaigns, enabling campaign-specific landing pages, source tracking, and conversion analytics.

**Relates To**: BR-8

**Acceptance Criteria**:

- [ ] Given a candidate arrives from a Get Into Teaching campaign, when they access the portal, then the campaign source is tracked through to application submission
- [ ] Given a subject-specific campaign is running (e.g., "Teach Physics"), when the landing page loads, then it shows Physics-specific content, bursary information, and course search pre-filtered to Physics
- [ ] Given campaign analytics are requested, when the report generates, then it shows conversion rates from campaign click to application submission by subject and demographic

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Page Load Time

**Requirement**: All pages load within 2 seconds at p95. Course search returns results within 1 second.

**Peak Load**: 50,000 concurrent users during UCAS deadline day and results day periods.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability during the ITT recruitment cycle (October-July). 99.99% during application deadline periods. Maintenance windows permitted during August-September.

**Priority**: HIGH

---

### NFR-SEC-1: Data Protection

**Requirement**: Full UK GDPR compliance. Candidate personal data (including diversity monitoring) classified as OFFICIAL-SENSITIVE. DBS disclosure data handled under DBS code of practice with enhanced access controls and retention limits. Application data retained for the current cycle plus 2 years, then deleted.

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. Tested with screen readers. Mobile-first design (60% of candidates expected to use mobile). Plain language throughout — no unexplained acronyms.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: DfE Sign-in / GOV.UK One Login

**Purpose**: Authentication for ITT providers and school-based users.
**Integration Type**: SAML 2.0 / OpenID Connect
**Priority**: MUST_HAVE

---

### INT-2: DBS Enhanced Disclosure Service

**Purpose**: Digital DBS application and result notification for post-offer checks.
**Integration Type**: API (DBS e-Bulk or successor digital service)
**Data Exchanged**: Application submission; disclosure result notification
**Priority**: SHOULD_HAVE

---

### INT-3: Teaching Regulation Agency (TRA)

**Purpose**: Automated QTS check and prohibition check at point of offer.
**Integration Type**: Real-time API
**Data Exchanged**: Teacher reference number; QTS status; prohibition status
**Priority**: SHOULD_HAVE

---

### INT-4: Get Information About Schools (GIAS)

**Purpose**: School data for School Direct and SCITT course listings.
**Integration Type**: Daily batch synchronisation
**Priority**: MUST_HAVE

---

### INT-5: Student Loans Company (SLC)

**Purpose**: Bursary/scholarship payment administration for eligible trainees.
**Integration Type**: Batch file exchange (monthly)
**Priority**: COULD_HAVE

---

## Data Requirements

### DR-1: Candidate Profile

**Attributes**: candidate_id, name, email, phone, date_of_birth, nationality, degree_subject, degree_class, degree_institution, work_experience (structured), personal_statement, diversity_monitoring (voluntary: ethnicity, gender, disability, socioeconomic), accessibility_needs, preferred_subjects, preferred_locations, route_finder_results

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Current cycle + 2 years, then deleted
**Data Volume**: 200,000 active profiles per recruitment cycle

---

### DR-2: ITT Course Record

**Attributes**: course_id, provider_id, subject, route (PGCE, QTS, School Direct, SCITT), salary_status, bursary_amount, scholarship_available, location, ofsted_grade, trainee_satisfaction, completion_rate, employment_rate, places_available, application_deadline

**Data Classification**: OFFICIAL
**Data Volume**: 15,000 courses per cycle

---

### DR-3: Application Record

**Attributes**: application_id, candidate_id, course_choices (up to 4), status_per_choice, personal_statement, references (2), work_experience, qualifications, submission_date, provider_decision_date, dbs_status, tra_status

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Current cycle + 2 years
**Data Volume**: 160,000 applications per cycle

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Shortage subject applications | 2024/25 volumes | +25% | 2 recruitment cycles | Portal data |
| Application abandonment rate | 35% | < 15% | At launch | Portal analytics |
| Applications via unified portal | ~60% (DfE Apply) | 90% | 18 months | Portal data |
| Application completion time | 4-6 hours | < 90 minutes | At launch | Portal analytics |
| Diversity: BAME applications | 18% | 25% | 2 cycles | Diversity monitoring |
| Offer-to-start time | 14 weeks | 10 weeks | 12 months | Portal data |
| Candidate satisfaction | N/A | 4.0/5.0 | 6 months | User survey |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| DBS | Disclosure and Barring Service |
| ITT | Initial Teacher Training |
| PGCE | Postgraduate Certificate in Education |
| QTS | Qualified Teacher Status |
| SCITT | School-Centred Initial Teacher Training |
| SKE | Subject Knowledge Enhancement |
| TRA | Teaching Regulation Agency |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Teacher Recruitment Portal
**Model**: Claude Opus 4.6
