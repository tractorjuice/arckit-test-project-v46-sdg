# Project Requirements: SEND Case Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | SEND Case Management System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, SEND Case Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SEND Programme Board, DfE SEND Division, Development Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the SEND Case Management System, which will digitise and standardise the Education, Health and Care (EHC) plan process across local authorities in England, enabling statutory compliance, multi-agency collaboration, and parent transparency.

---

## Executive Summary

### Business Context

The SEND system in England is under severe strain. Over 576,000 children have EHC plans, 43% of new plans are issued late, and SEND Tribunal appeals have doubled. Local authorities use fragmented digital tools — often spreadsheets — to manage complex multi-agency processes. Parents experience an opaque, adversarial system. The SEND Case Management System will provide a standardised digital workflow from initial referral through assessment, plan issuance, annual review, and transition, integrating health and social care inputs within a single platform.

### Objectives

- Digitise the end-to-end EHC plan lifecycle (referral, assessment, plan, review, transition)
- Enable statutory timeline compliance (20-week EHC assessment, 14-week annual review)
- Provide parents with real-time visibility of their child's case progress
- Integrate health assessment workflows with NHS ICBs
- Standardise EHC plan quality through structured templates and quality checks

### Expected Outcomes

- Reduction in late EHC plans from 43% to below 15%
- 30% reduction in SEND Tribunal appeals
- 40% reduction in parent complaints about lack of communication
- GBP 45M annual saving in reduced Tribunal costs across all LAs
- Improved outcomes for children with SEND through timely, coordinated provision

### Project Scope

**In Scope**:

- EHC needs assessment workflow (referral to plan issuance)
- Annual review workflow
- Parent/carer portal with case tracking
- Health assessment request/response workflow (NHS ICB integration)
- SENCO referral and annual review coordination portal
- LA case management dashboard with statutory timeline tracking
- Structured EHC plan templates with quality validation
- Reporting and analytics (LA-level and national)

**Out of Scope**:

- Clinical health record management (NHS systems of record)
- Social care case management (separate LA systems)
- School SEND provision mapping tools (Phase 2)
- Mediation service booking (separate SEND mediation services)

---

## Business Requirements

### BR-1: Digitise End-to-End EHC Plan Lifecycle

**Description**: Provide a digital workflow covering the complete EHC plan lifecycle from initial request through assessment, plan issuance, annual review, plan amendment, and transition/cessation.

**Rationale**: Most LAs manage this process through a combination of document management systems, spreadsheets, and paper files, leading to missed deadlines, lost documents, and inconsistent processes.

**Success Criteria**:

- All 20 stages of the EHC assessment process digitised with statutory timeline tracking
- Automated deadline notifications to caseworkers at key milestones
- Document upload and version control for all assessment evidence
- 80% of LAs transitioned from legacy systems within 24 months

**Priority**: MUST_HAVE
**Stakeholder**: LA SEND Teams (SD-2), Minister (SD-1)

---

### BR-2: Parent Case Tracking Portal

**Description**: Provide parents and carers with real-time online access to the status of their child's EHC assessment or annual review, with milestone notifications.

**Rationale**: Parents report that lack of transparency is their primary frustration. Real-time tracking reduces complaint volumes and builds trust.

**Success Criteria**:

- Parents can view current case stage, next expected milestone, and estimated timeline
- Automated notifications sent at each stage transition (email/SMS via GOV.UK Notify)
- Parent portal meets WCAG 2.2 AA and is usable on mobile devices
- 60% of active parents access the portal at least once per assessment cycle

**Priority**: MUST_HAVE
**Stakeholder**: Parents (SD-3)

---

### BR-3: Statutory Timeline Compliance Engine

**Description**: Enforce statutory timelines (20-week EHC assessment, 6-week health advice, 14-week annual review) through automated tracking, escalation alerts, and management reporting.

**Rationale**: 43% of EHC plans are issued late. Automated timeline tracking with escalation is essential for compliance.

**Success Criteria**:

- System tracks all statutory deadlines and displays countdown indicators
- Automated escalation alerts when cases approach deadline (2 weeks, 1 week, overdue)
- Management dashboard showing compliance rates by caseworker, team, and LA
- Cases exceeding statutory timeline automatically flagged for senior review

**Priority**: MUST_HAVE
**Stakeholder**: LA SEND Teams (SD-2), SEND Tribunal (SD-5)

---

### BR-4: Multi-Agency Health Assessment Integration

**Description**: Enable digital health assessment requests from LA SEND teams to NHS ICBs, with structured response submission and automated tracking of the 6-week health advice deadline.

**Rationale**: Health advice is the most common bottleneck in the EHC assessment process. Digital request-response reduces administrative overhead and improves timeliness.

**Success Criteria**:

- LA caseworkers can send structured health assessment requests to ICBs digitally
- ICB clinicians can submit health advice through structured templates
- 6-week deadline tracked with automated reminders to ICB contacts
- Average health advice turnaround reduced from 8 weeks to 4 weeks

**Priority**: MUST_HAVE
**Stakeholder**: NHS ICBs (SD-4)

---

### BR-5: Structured EHC Plan Quality Framework

**Description**: Provide structured EHC plan templates with quality validation rules that ensure plans contain all required sections (as specified by SEND Code of Practice) and that provision is specific, measurable, and quantified.

**Rationale**: Poor-quality EHC plans are the primary cause of Tribunal appeals. Parents win 96% of appeals, indicating systemic quality failure at the plan-writing stage.

**Success Criteria**:

- Templates enforce all SEND Code of Practice required sections
- Quality validation checks that outcomes are specific and measurable
- Provision must be quantified (hours per week, not "regular" or "as needed")
- Quality score generated per plan; plans below threshold flagged for review

**Priority**: MUST_HAVE
**Stakeholder**: SEND Tribunal (SD-5), Parents (SD-3)

---

### BR-6: SENCO Referral and Review Coordination

**Description**: Provide SENCOs with a portal to submit initial EHC assessment requests, coordinate annual review evidence, and communicate with LA SEND teams.

**Rationale**: SENCOs currently submit referrals by email or post, with no confirmation of receipt or tracking. Annual review paperwork is exchanged manually.

**Success Criteria**:

- SENCOs can submit referral requests with structured forms and evidence upload
- Annual review coordination workflow with school evidence submission
- Automated confirmation of receipt and case reference number
- SENCO workload for SEND administration reduced by 30%

**Priority**: SHOULD_HAVE
**Stakeholder**: SENCOs (SD-6)

---

## Functional Requirements

### User Personas

#### Persona 1: Helen — LA SEND Caseworker

- **Role**: EHC Plan Caseworker, London Borough of Hackney
- **Goals**: Manage 80+ active EHC cases within statutory timelines; coordinate assessment inputs; write quality plans
- **Pain Points**: Uses 4 different systems; manually tracks deadlines in a spreadsheet; frequently misses 20-week deadline due to late health advice; spends 30% of time chasing colleagues for information
- **Technical Proficiency**: Medium

#### Persona 2: Ahmed — Parent of Child with Autism

- **Role**: Father of 7-year-old with autism, requesting EHC needs assessment
- **Goals**: Understand where his son's case is in the process; ensure health and education evidence is considered; receive decision within 20 weeks
- **Pain Points**: Submitted request 14 weeks ago; received no communication; called LA SEND team 6 times with no callback; does not understand the process or timeline
- **Technical Proficiency**: Medium (uses smartphone daily)

#### Persona 3: Dr. Osei — NHS Speech and Language Therapist

- **Role**: Senior Speech and Language Therapist, NHS ICB
- **Goals**: Respond to EHC assessment requests within 6-week deadline; submit structured advice that is useful for plan writing
- **Pain Points**: Receives requests by post or email, often without sufficient information; has a backlog of 40+ requests; no tracking of outstanding requests; health advice format varies between LAs
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-1: EHC Needs Assessment Workflow

**Description**: Digital workflow covering all stages of the EHC needs assessment from initial request to plan issuance.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a parent/school submits an EHC assessment request, when it is received, then the system creates a case with a unique reference number and starts the 20-week clock
- [ ] Given a case reaches the 6-week decision point, when the LA decides whether to assess, then the system records the decision with rationale and notifies the parent
- [ ] Given health advice is requested, when the request is sent to the ICB, then the 6-week health advice deadline is tracked independently
- [ ] Given all assessment evidence is received, when the LA drafts an EHC plan, then the system validates the plan against the quality framework (BR-5)
- [ ] Edge case: When a case is paused due to parental request or exceptional circumstances, the statutory clock stops with documented reason

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-2: Parent Case Tracking Dashboard

**Description**: Real-time case status dashboard for parents showing current stage, next milestone, and estimated timeline.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a parent logs in, when they view their child's case, then they see a visual progress tracker showing completed, current, and upcoming stages
- [ ] Given a case transitions to a new stage, when the transition occurs, then the parent receives an automated notification (email or SMS)
- [ ] Given a parent has multiple children with SEND, when they log in, then they can view each child's case separately
- [ ] Edge case: When a case is delayed beyond the expected milestone date, the parent sees an updated estimate with explanation

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-3: Health Assessment Request/Response

**Description**: Structured digital workflow for requesting and receiving health assessment advice from NHS ICBs.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a caseworker initiates a health assessment request, when they submit it, then a structured request is sent to the designated ICB contact with all relevant child information
- [ ] Given an ICB clinician receives a request, when they access the platform, then they see a structured template for submitting health advice
- [ ] Given health advice is overdue, when the 6-week deadline approaches, then automated reminders are sent to the ICB at 2 weeks and 1 week remaining
- [ ] Edge case: When health advice is submitted late, the system records the delay reason and includes it in performance reporting

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-4: EHC Plan Quality Validation

**Description**: Automated quality checks on draft EHC plans to ensure compliance with SEND Code of Practice requirements.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a caseworker drafts an EHC plan, when they submit for review, then the system checks for all required sections (A-K as per SEND Code of Practice)
- [ ] Given an outcome is written, when quality validation runs, then outcomes are checked for specificity (not vague statements like "will make progress")
- [ ] Given provision is specified, when validation runs, then it checks that provision is quantified (e.g., "2 hours per week" not "regular support")
- [ ] Given validation issues are found, when the caseworker reviews, then specific guidance is provided on how to address each issue

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-5: Annual Review Workflow

**Description**: Digital workflow for annual reviews of existing EHC plans, including evidence collection from school, health, and social care.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an EHC plan exists, when the annual review is due, then the system automatically schedules the review and notifies all parties
- [ ] Given a review meeting is scheduled, when the school uploads evidence, then the caseworker and parent can access it before the meeting
- [ ] Given the review concludes, when the decision is recorded (maintain, amend, cease), then the appropriate workflow is triggered
- [ ] Edge case: When a plan amendment is required, the 12-week amendment timeline is automatically tracked

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-6: Statutory Timeline Dashboard (Management)

**Description**: Management dashboard showing statutory timeline compliance rates, bottleneck analysis, and workload distribution.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a SEND team manager accesses the dashboard, when they view it, then they see compliance rates (% within 20 weeks) by caseworker, by case type, and trend over time
- [ ] Given cases are approaching deadline, when viewed, then they are colour-coded (green/amber/red) based on remaining time vs remaining steps
- [ ] Given a bottleneck is identified (e.g., health advice delays), when analysed, then the dashboard shows average delay by assessment type and ICB

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-7: Document Management and Evidence Repository

**Description**: Secure document management for all assessment evidence, reports, correspondence, and EHC plan versions.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a document is uploaded, when stored, then it is encrypted at rest and tagged with case reference, document type, and date
- [ ] Given a plan is amended, when the new version is saved, then all previous versions are retained with full audit trail
- [ ] Given a parent requests access to their child's documents, when the request is processed, then all case documents are available for download

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-SEC-1: Children's Data Protection (CRITICAL)

**Requirement**: All children's data must be encrypted at rest (AES-256) and in transit (TLS 1.3+). Application-level encryption for SEND diagnosis, health data, and safeguarding information. Full AADC and UK GDPR compliance.

**Priority**: CRITICAL

---

### NFR-SEC-2: Multi-Agency Access Control

**Requirement**: Role-based access control supporting LA caseworkers, NHS clinicians, SENCOs, parents, and DfE analysts — each seeing only the data appropriate to their role and relationship to the child.

- LA caseworkers: Full case access for their caseload
- NHS clinicians: Access to assessment requests assigned to them; submit advice only
- SENCOs: Access to their school's pupils' cases; submit evidence and referrals
- Parents: Access to their own child's case status and documents
- DfE analysts: Aggregated, anonymised national data only

**Priority**: CRITICAL

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability. Enhanced availability during EHC plan submission windows and Tribunal deadline periods.

**Priority**: HIGH

---

### NFR-P-1: Response Time

**Requirement**: Page load within 2 seconds at p95. Document upload/download within 5 seconds for files up to 50MB.

**Priority**: HIGH

---

### NFR-C-1: Children and Families Act 2014 Compliance

**Requirement**: System must support all statutory requirements of the Children and Families Act 2014 Part 3 (EHC needs assessment, plan issuance, annual review, mediation, appeal rights notification).

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: NHS ICB Health Assessment Systems

**Purpose**: Digital health assessment request and response exchange.
**Integration Type**: API-based (structured messages) with email fallback
**Data Exchanged**: Assessment request (child demographics, reason, specific advice needed) / Health advice response (structured clinical advice)
**Priority**: CRITICAL

---

### INT-2: DfE Sign-in

**Purpose**: Authentication for SENCOs and school-based users.
**Integration Type**: SAML 2.0 / OpenID Connect
**Priority**: MUST_HAVE

---

### INT-3: Get Information About Schools (GIAS)

**Purpose**: Authoritative school data for linking pupils to schools.
**Integration Type**: Daily batch synchronisation
**Priority**: MUST_HAVE

---

### INT-4: GOV.UK Notify

**Purpose**: Parent notifications (case status updates, milestone alerts).
**Integration Type**: Real-time API
**Priority**: MUST_HAVE

---

### INT-5: SEND Tribunal Case Management

**Purpose**: Exchange case data when appeals are registered, reducing duplicate data entry.
**Integration Type**: Batch API (Phase 2)
**Priority**: COULD_HAVE

---

## Data Requirements

### DR-1: SEND Case Record

**Attributes**: case_id (UUID), child_upn (String), child_name, date_of_birth, la_code, school_urn, case_type (EHC assessment, annual review, amendment), current_stage, stage_start_date, statutory_deadline, assigned_caseworker, health_advice_status, social_care_advice_status, parent_contact

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Duration of EHC plan + 6 years after cessation (aligned with limitation period)
**Data Volume**: 600,000 active cases, 150,000 new assessments/year

---

### DR-2: EHC Plan Document

**Attributes**: plan_id, case_id, version, sections_a_to_k (structured content), provision_details (quantified), quality_score, status (draft, consultation, final, amended), created_date, approved_date

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Duration of plan + 6 years
**Data Volume**: 576,000 active plans

---

### DR-3: Health Advice Record

**Attributes**: advice_id, case_id, icb_code, clinician_type, request_date, deadline_date, response_date, advice_content (structured), late_flag

**Data Classification**: OFFICIAL-SENSITIVE (health data)
**Data Retention**: Same as case record
**Data Volume**: 150,000 requests/year

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| EHC plans issued within 20 weeks | 57% | 85% | 18 months | Platform data |
| Parent complaint volume | ~25,000/year | ~15,000/year | 24 months | LA complaints data |
| Tribunal appeal registrations | ~14,000/year | ~9,800/year | 24 months | SENDIST data |
| Health advice within 6 weeks | ~55% | ~80% | 18 months | Platform data |
| LA adoption | 0 | 122/152 LAs | 24 months | Platform registrations |
| Parent portal engagement | 0% | 60% of active parents | 12 months | Platform analytics |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| CAMHS | Child and Adolescent Mental Health Services |
| EHC Plan | Education, Health and Care Plan |
| ICB | Integrated Care Board (NHS) |
| IPSEA | Independent Provider of Special Education Advice |
| SENCO | Special Educational Needs Coordinator |
| SENDIST | SEND Tribunal |
| SOSSEN | SOS!SEN — charity supporting parents |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SEND Case Management System
**Model**: Claude Opus 4.6
