# Project Requirements: Climate Adaptation Planning Tool

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Climate Adaptation Planning Tool (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Adaptation Planning Tool |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Adaptation Programme Board, DEFRA Digital, LGA, CCC Adaptation Committee, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Climate Adaptation Planning Tool — a digital service enabling local authorities to develop, manage, and monitor evidence-based climate adaptation plans using risk data from the Climate Risk Assessment Platform (Project 002).

---

## Executive Summary

### Business Context

The CCC has consistently identified local climate adaptation as a critical gap. Most of the 152 upper-tier local authorities in England lack dedicated climate adaptation plans, and where plans exist, quality varies enormously. Local authorities face capacity constraints (typically 0.5-2 FTEs for all climate work), lack specialist climate science expertise, and struggle to translate national climate risk assessments into local action plans. The National Adaptation Programme (NAP3) commits DEFRA to providing tools and evidence to support local adaptation.

### Objectives

- Enable 50% of upper-tier authorities (76+) to create evidence-based adaptation plans within 18 months
- Reduce adaptation plan development time from approximately 6 months to under 10 weeks
- Integrate with Climate Risk Assessment Platform (Project 002) for locally relevant risk evidence
- Produce structured plan outputs that enable CCC to assess national local adaptation progress
- Provide template adaptation actions aligned with CCRA3 priority risk areas

### Expected Outcomes

- 76+ local authorities with active adaptation plans on the platform within 18 months
- CCC includes tool-generated data in CCRA4 preparatory assessment
- Local authorities report 60%+ time saving vs manual plan development
- Measurable improvement in local adaptation plan quality (CCC-assessed)

### Project Scope

**In Scope**:

- Adaptation plan creation workflow with guided templates
- Risk evidence integration from Climate Risk Assessment Platform (Project 002)
- Template adaptation actions for 8 CCRA3 priority risk areas
- Progress tracking with measurable indicators
- Committee-ready report generation
- Peer benchmarking and best practice sharing
- Open data publication of anonymised plan summaries

**Out of Scope**:

- Climate risk assessment calculation (provided by Project 002)
- Funding application support for adaptation projects
- Detailed engineering design of adaptation measures
- Scotland, Wales, Northern Ireland (devolved responsibility — Phase 2 by invitation)

---

## Business Requirements

### BR-001: Local Authority Adoption

**Description**: Enable at least 50% of upper-tier local authorities in England (76 of 152) to create and maintain adaptation plans on the platform within 18 months of launch.

**Rationale**: Tool value depends on critical mass of adoption. Below 50%, the national picture is too incomplete for CCC assessment.

**Success Criteria**:

- 76+ authorities with active accounts and initiated plans within 18 months
- Onboarding time (registration to first section completed) under 2 hours
- No cost to local authorities (free tool, no licence fees)

**Priority**: MUST_HAVE

---

### BR-002: Evidence-Based Plan Templates

**Description**: Provide structured adaptation plan templates pre-populated with locally relevant climate risk data from the Climate Risk Assessment Platform (Project 002).

**Rationale**: Local authorities lack capacity to start from blank sheets. Pre-populated, evidence-based templates reduce effort and improve quality.

**Success Criteria**:

- Templates cover all 8 CCRA3 priority risk areas
- Risk data pre-populated from Project 002 for each authority's geographic area
- Templates customisable to local priorities without losing structured format

**Priority**: MUST_HAVE

---

### BR-003: CCC-Assessable Output

**Description**: Produce structured adaptation plan outputs that enable the CCC to assess local adaptation progress at a national level.

**Rationale**: CCC cannot currently assess local adaptation systematically. Structured outputs from a critical mass of authorities would transform CCC's ability to report on local adaptation progress.

**Success Criteria**:

- Standardised risk-action mappings covering 8+ CCRA risk areas
- Progress indicators defined for 80%+ of plan actions
- Anonymised aggregate data publishable as open data

**Priority**: MUST_HAVE

---

### BR-004: Accessibility for Non-Specialists

**Description**: Ensure the tool is usable by local authority officers without specialist climate science, GIS, or data analysis expertise.

**Rationale**: Most local authority climate officers manage adaptation alongside other duties. The tool must be accessible to generalist sustainability officers, emergency planners, and planning policy officers.

**Success Criteria**:

- Usable without training by an officer with no climate science background (validated by user testing)
- No GIS software required — map views embedded within the tool
- All climate risk information presented in plain language with supporting evidence accessible on demand
- WCAG 2.2 Level AA compliant

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Local Authority Climate Officer

- **Role**: Sustainability officer responsible for climate adaptation planning
- **Goals**: Create a credible adaptation plan for committee approval within limited time
- **Pain Points**: No template to start from, no local risk data, limited time (0.5 FTE)
- **Technical Proficiency**: Low-Medium

#### Persona 2: Elected Member (Councillor)

- **Role**: Portfolio holder for environment or council leader
- **Goals**: Understand local climate risks, approve adaptation plan, demonstrate action to residents
- **Pain Points**: Technical jargon, lengthy documents, unclear priorities
- **Technical Proficiency**: Low

#### Persona 3: DEFRA Policy Analyst

- **Role**: DEFRA NAP3 programme manager
- **Goals**: Monitor local adaptation progress nationally, report to Ministers, respond to CCC
- **Pain Points**: No systematic data on local adaptation plans, manual collection of information
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-001: Authority Registration and Onboarding

**Description**: Enable local authority officers to register, verify their authority affiliation, and begin plan creation within 30 minutes.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] Given a local authority officer, when they register with a .gov.uk email, then their authority is automatically identified
- [ ] Given registration completion, when first login occurs, then a guided onboarding introduces the tool in under 15 minutes
- [ ] Given onboarding completion, when the user starts a plan, then local risk data from Project 002 is pre-populated

**Priority**: MUST_HAVE

---

#### FR-002: Adaptation Plan Builder

**Description**: Provide a guided, section-by-section plan builder with templates for each CCRA3 priority risk area.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given the plan builder, when accessed, then sections for each CCRA3 risk area are available as templates
- [ ] Given a risk area section, when opened, then pre-populated local risk data and suggested actions are shown
- [ ] Given suggested actions, when reviewed, then the user can accept, modify, reject, or add custom actions
- [ ] Given each action, when defined, then fields for timeline, owner, cost estimate, and success indicator are available
- [ ] Given the plan, when saved, then progress is preserved and the user can return to any section at any time

**Priority**: MUST_HAVE

---

#### FR-003: Risk-to-Action Mapping

**Description**: Map climate risks (from Project 002) to recommended adaptation actions, enabling authorities to see which actions address which risks.

**Relates To**: BR-002, BR-003

**Acceptance Criteria**:

- [ ] Given a climate risk, when displayed in the plan builder, then suggested adaptation actions are linked to that risk
- [ ] Given an adaptation action, when defined, then it is linked to one or more climate risks
- [ ] Given the complete plan, when viewed as a matrix, then a risk-to-action coverage map shows which risks have actions and which gaps remain
- [ ] Given a risk with no actions, when identified, then a warning highlights the gap

**Priority**: MUST_HAVE

---

#### FR-004: Progress Tracking Dashboard

**Description**: Track progress of adaptation plan implementation with measurable indicators and RAG status.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given each adaptation action, when assigned a progress indicator, then current status (not started/in progress/completed) is trackable
- [ ] Given the authority dashboard, when accessed, then overall plan progress is shown as percentage complete with RAG status
- [ ] Given a reporting period, when due, then automated progress report prompts are sent to the plan owner
- [ ] Given the progress data, when aggregated nationally, then DEFRA can see overall local adaptation progress

**Priority**: MUST_HAVE

---

#### FR-005: Committee Report Generator

**Description**: Generate committee-ready reports from the adaptation plan in formats suitable for elected member scrutiny.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a completed or in-progress plan, when report generation is requested, then a formatted PDF/Word document is produced
- [ ] Given the report, when generated, then it includes executive summary, risk overview, action plan, and progress summary
- [ ] Given the report, when reviewed by elected members, then it is in plain language without technical jargon
- [ ] Given the report, when compared to peer authorities, then benchmarking data is included (opt-in)

**Priority**: SHOULD_HAVE

---

#### FR-006: Peer Benchmarking

**Description**: Enable authorities to compare their adaptation plan coverage and progress against similar authorities.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given an authority, when benchmarking is requested, then comparison with similar authorities (by size, risk profile, region) is shown
- [ ] Given the benchmarking view, when displayed, then only anonymised aggregate data from opted-in authorities is shown
- [ ] Given a leading authority, when identified, then links to published case studies and contact details (if opted in) are provided

**Priority**: COULD_HAVE

---

#### FR-007: Best Practice Library

**Description**: Provide a searchable library of adaptation action case studies from leading local authorities.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] Given the library, when searched by risk area, then relevant case studies are returned
- [ ] Given a case study, when viewed, then it includes authority context, action taken, cost, outcome, and lessons learned
- [ ] Given a case study, when relevant to the user's plan, then it can be linked as a reference

**Priority**: COULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Page Load Time

**Requirement**: All pages load within 3 seconds on standard broadband. Plan builder auto-saves within 2 seconds.

**Priority**: MUST_HAVE

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.5% uptime. Planned maintenance during overnight hours (22:00-06:00 UK time).

**Priority**: MUST_HAVE

#### NFR-A-002: Disaster Recovery

**RPO**: 1 hour | **RTO**: 8 hours

**Priority**: MUST_HAVE

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: Authentication via .gov.uk email domain verification. MFA required for plan editing. Read-only public access to published plans.

**Priority**: MUST_HAVE

#### NFR-SEC-002: Data Isolation

**Requirement**: Each authority's draft plan data is isolated. Published plan summaries are open data. DEFRA has read-only access to aggregated progress data.

**Priority**: MUST_HAVE

### Accessibility Requirements

#### NFR-U-001: WCAG Compliance

**Requirement**: WCAG 2.2 Level AA. GOV.UK Design System components used throughout. Progressive enhancement — core functionality without JavaScript.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Climate Risk Assessment Platform (Project 002)

**Purpose**: Consume locally relevant climate risk data to pre-populate adaptation plan templates.

**Integration Type**: Internal API (within SDG 13 programme)

**Data Exchanged**: Ward-level risk summaries, hazard scores, recommended adaptation actions by risk area

**Priority**: MUST_HAVE

### INT-002: GOV.UK Accounts (Future)

**Purpose**: Single sign-on for local authority users through GOV.UK One Login (when available for professional users).

**Integration Type**: OIDC/OAuth 2.0

**Priority**: COULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Adaptation Plan

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique plan identifier |
| authority_id | String | Yes | Local authority ONS code |
| authority_name | String | Yes | Local authority name |
| plan_status | Enum | Yes | Draft, in_review, approved, published |
| created_date | DateTime | Yes | Plan creation date |
| last_modified | DateTime | Yes | Last modification date |
| overall_progress | Decimal | No | Percentage complete (0-100) |
| risk_areas_covered | Integer | No | Number of CCRA3 risk areas addressed |

#### Entity 2: Adaptation Action

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique action identifier |
| plan_id | UUID | Yes | Parent adaptation plan |
| risk_area | Enum | Yes | CCRA3 risk area |
| action_description | Text | Yes | Description of adaptation action |
| owner | String | No | Responsible officer/team |
| timeline | String | No | Implementation timeline |
| cost_estimate | Enum | No | Low (<50K), medium (50K-500K), high (>500K) |
| status | Enum | Yes | Not_started, in_progress, completed, deferred |
| success_indicator | Text | No | How success will be measured |

---

## Approval

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, DEFRA | _________ | PENDING |
| LGA Representative | _________ | PENDING |
| CCC Adaptation Committee | _________ | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| NAP3 | Policy | GOV.UK | Local adaptation commitments | N/A |
| CCRA3 | Statutory report | CCC | 8 priority risk areas | N/A |
| CCC Adaptation Progress Report | Statutory report | CCC | Local adaptation gap evidence | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Climate Adaptation Planning Tool (Project 004)
**Model**: Claude Opus 4.6
