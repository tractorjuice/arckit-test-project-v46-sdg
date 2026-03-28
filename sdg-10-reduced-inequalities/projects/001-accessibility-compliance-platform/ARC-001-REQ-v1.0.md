# Project Requirements: Accessibility Compliance Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Accessibility Compliance Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Accessibility Compliance Platform, GDS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Development Team, CDDO, EHRC, Disability Sector Advisory Group |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Accessibility Compliance Platform — a GDS-operated monitoring service for public sector website accessibility under the Public Sector Bodies Accessibility Regulations 2018 (PSBAR).

---

## Executive Summary

### Business Context

The Public Sector Bodies Accessibility Regulations 2018 require all public sector websites and mobile applications to meet WCAG 2.1 Level AA. Despite this legal obligation, the NAO's 2024 report found that fewer than 40% of public sector websites meet the standard. GDS currently has no centralised monitoring capability, relying on complaint-driven EHRC enforcement and ad hoc sample audits. The Accessibility Compliance Platform will provide automated scanning at scale, a blended assessment methodology combining automated and lived-experience testing, and actionable remediation guidance for departmental web teams.

### Objectives

- Establish automated WCAG 2.2 scanning across 12,000+ public sector websites
- Provide a blended assessment methodology combining automated scanning, expert review, and user testing
- Deliver developer-friendly API for CI/CD integration
- Track compliance trends and remediation progress over time
- Generate enforcement-grade evidence for EHRC

### Expected Outcomes

- 95% of in-scope public sector websites scanned monthly within 12 months
- Public sector WCAG 2.2 compliance rate increased from 40% to 70% within 24 months
- Cost per website assessed reduced from GBP 5,000-15,000 (manual) to GBP 50-200 (automated + sampled blended)
- 50+ departments integrating scanning API into CI/CD pipelines within 24 months

### Project Scope

**In Scope**:

- Automated WCAG 2.2 scanning engine (axe-core and WAVE integration)
- Compliance dashboard with organisation, sector, and geographic views
- Blended assessment workflow (automated + manual + user testing)
- Developer API for CI/CD integration
- Remediation guidance engine with plain-English fix recommendations
- Lived-experience testing panel management
- EHRC reporting and evidence package generation

**Out of Scope**:

- Scanning private sector websites (Phase 2 consideration)
- Mobile application accessibility testing (Phase 2)
- Direct remediation services (GDS provides guidance, departments fix)
- PSBAR enforcement decisions (EHRC responsibility)

---

## Business Requirements

### BR-001: Centralised Accessibility Monitoring

**Description**: GDS must have a centralised platform to monitor accessibility compliance across all in-scope public sector websites, replacing the current fragmented, complaint-driven approach.

**Rationale**: Without centralised monitoring, PSBAR compliance is unmeasured and unmanaged. The NAO has called for proactive monitoring capability.

**Success Criteria**:

- 95% of in-scope websites registered and scanned within 12 months
- Compliance dashboard available to GDS, CDDO, and EHRC

**Priority**: MUST_HAVE

**Stakeholder**: GDS Director General (SD-1)

---

### BR-002: Blended Assessment Methodology

**Description**: The platform must support a blended accessibility assessment combining automated scanning, expert manual review, and testing by disabled users, with clear weighting and scoring.

**Rationale**: Automated tools detect only 30-40% of WCAG violations. Lived-experience testing is essential for credible assessment, particularly for cognitive accessibility.

**Success Criteria**:

- Blended methodology published and peer-reviewed
- 500+ websites receiving blended assessment annually
- Lived-experience panel of 200+ disabled testers operational

**Priority**: MUST_HAVE

**Stakeholder**: RNIB (SD-3), Scope (SD-5)

---

### BR-003: Enforcement Evidence Generation

**Description**: The platform must generate compliance evidence packages suitable for EHRC enforcement proceedings against persistently non-compliant public sector bodies.

**Rationale**: EHRC needs reliable evidence to exercise its PSBAR enforcement powers. The platform must produce timestamped, verifiable compliance records.

**Success Criteria**:

- Evidence packages meet EHRC evidentiary requirements
- Historical compliance data retained for trend analysis
- Audit trail for all assessment activities

**Priority**: SHOULD_HAVE

**Stakeholder**: EHRC (SD-2)

---

### BR-004: Developer Integration Capability

**Description**: The platform must provide APIs enabling departmental web teams to integrate accessibility scanning into their development and deployment workflows.

**Rationale**: Shift-left accessibility testing during development prevents violations reaching production, reducing remediation costs and improving citizen experience.

**Success Criteria**:

- Documented REST API available within 12 months
- 20+ departments integrating within 12 months
- Developer satisfaction score above 7/10

**Priority**: SHOULD_HAVE

**Stakeholder**: Departmental web teams (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: GDS Accessibility Analyst

- **Role**: GDS accessibility team member monitoring compliance landscape
- **Goals**: Identify worst-performing sectors and organisations, track improvement trends, prioritise outreach
- **Pain Points**: Currently relies on manual sample audits, no comprehensive view
- **Technical Proficiency**: High

#### Persona 2: Departmental Web Developer

- **Role**: Developer maintaining a departmental government website
- **Goals**: Scan own site during development, receive actionable fix guidance, demonstrate compliance
- **Pain Points**: Accessibility reports are jargon-heavy, tools produce different results, no clear prioritisation
- **Technical Proficiency**: High

#### Persona 3: EHRC Enforcement Officer

- **Role**: EHRC staff investigating PSBAR non-compliance
- **Goals**: Obtain reliable compliance evidence, view historical trends, generate enforcement-ready reports
- **Pain Points**: Current evidence gathering is manual and expensive
- **Technical Proficiency**: Medium

#### Persona 4: Lived-Experience Tester

- **Role**: Disabled person testing websites using assistive technologies
- **Goals**: Report accessibility barriers encountered, contribute to compliance assessment
- **Pain Points**: Testing tools are not themselves accessible, feedback not valued
- **Technical Proficiency**: Low to Medium

---

### Functional Requirements Detail

#### FR-001: Website Registration and Discovery

**Description**: The system must maintain a register of all in-scope public sector websites, with automated discovery of new sites and manual registration capability.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a URL, when submitted for registration, then the system validates it is a public sector website
- [ ] Given the GOV.UK domain list, when imported, then all domains are registered automatically
- [ ] Given a registered website, when its URL changes, then the system detects and updates the registration

**Priority**: MUST_HAVE

---

#### FR-002: Automated WCAG 2.2 Scanning

**Description**: The system must perform automated WCAG 2.2 Level AA compliance scanning using axe-core and WAVE engines, scanning all registered websites on a configurable schedule.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a registered website, when a scan is triggered, then all publicly accessible pages (up to configurable depth) are scanned
- [ ] Given a scan, when violations are found, then each violation is classified by WCAG success criterion, severity, and impact
- [ ] Given axe-core and WAVE results, when both engines scan the same page, then results are deduplicated and merged

**Data Requirements**:

- **Inputs**: URL, scan depth, scan schedule, WCAG version
- **Outputs**: Violation list with WCAG criterion, severity, element selector, remediation guidance
- **Validations**: URL must be accessible, response within 30 seconds

**Priority**: MUST_HAVE

---

#### FR-003: Compliance Dashboard

**Description**: The system must provide a web-based dashboard showing compliance status by organisation, sector, geographic region, and WCAG success criterion, with trend visualisations.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:

- [ ] Given scan results, when the dashboard loads, then compliance scores are displayed by organisation
- [ ] Given multiple scans over time, when a trend view is selected, then improvement or regression is visible
- [ ] Given a sector filter, when applied, then only organisations in that sector are displayed

**Priority**: MUST_HAVE

---

#### FR-004: Remediation Guidance Engine

**Description**: The system must provide plain-English remediation guidance for each detected violation, including code examples, before/after screenshots, and links to GDS Design System patterns.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a violation, when viewed in detail, then plain-English fix guidance is displayed
- [ ] Given a violation with a GDS Design System equivalent, when guidance is shown, then a link to the pattern is included
- [ ] Given guidance, when read by a non-specialist developer, then the fix can be understood without WCAG expertise

**Priority**: SHOULD_HAVE

---

#### FR-005: Developer API

**Description**: The system must provide a RESTful API enabling external systems to submit URLs for scanning, retrieve results, and integrate scanning into CI/CD pipelines.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a valid API key, when a scan request is submitted, then the scan is queued and a job ID returned
- [ ] Given a completed scan, when results are requested by job ID, then a structured JSON response is returned
- [ ] Given CI/CD integration, when a scan finds critical violations, then the API returns a non-zero exit code

**Priority**: SHOULD_HAVE

---

#### FR-006: Blended Assessment Workflow

**Description**: The system must support a workflow combining automated scan results, expert manual review findings, and lived-experience test reports into a single blended compliance assessment.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given automated scan results, when an expert review is added, then both are visible in the assessment
- [ ] Given lived-experience test results, when submitted by panel members, then they are incorporated into the blended score
- [ ] Given a blended assessment, when completed, then a composite compliance score is calculated with clear weighting

**Priority**: MUST_HAVE

---

#### FR-007: Lived-Experience Testing Panel Management

**Description**: The system must manage a panel of disabled testers, including recruitment, task assignment, compensation tracking, and accessibility of the testing tools themselves.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a new tester, when they register, then they can specify their assistive technologies, access needs, and availability
- [ ] Given a testing task, when assigned to panel members, then matched testers are notified via their preferred channel
- [ ] Given completed testing, when a tester submits findings, then compensation is automatically triggered

**Priority**: SHOULD_HAVE

---

#### FR-008: EHRC Evidence Package Generation

**Description**: The system must generate downloadable evidence packages for EHRC enforcement, including timestamped scan results, historical compliance trends, and accessibility statement analysis.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given a non-compliant organisation, when an evidence package is requested, then a PDF/HTML report is generated
- [ ] Given historical scan data, when included in the package, then trend data shows persistent non-compliance
- [ ] Given evidence data, when exported, then all data is timestamped and cryptographically signed

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Scan Throughput

**Requirement**: The system must be capable of scanning 12,000 websites per month, with each scan processing up to 100 pages per website.

**Measurement Method**: Platform scan completion logs

**Load Conditions**: 1.2 million pages scanned per month, distributed across scanning schedule

**Priority**: MUST_HAVE

---

#### NFR-P-002: Dashboard Response Time

**Requirement**: Dashboard pages must load within 2 seconds at p95 for up to 500 concurrent users.

**Priority**: MUST_HAVE

---

#### NFR-P-003: API Response Time

**Requirement**: API scan submission must respond within 500ms. Scan result retrieval must respond within 1 second at p95.

**Priority**: SHOULD_HAVE

---

### Security Requirements

#### NFR-SEC-001: Scanning Ethics

**Requirement**: The scanning engine must respect robots.txt, rate-limit requests to avoid overloading scanned sites, identify itself via User-Agent string, and not scan authenticated/private areas without explicit consent.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Data Classification

**Requirement**: All scan results classified OFFICIAL. Any data linking scan results to specific named individuals (e.g., lived-experience tester identities) classified OFFICIAL-SENSITIVE with enhanced access controls.

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Authentication and Authorisation

**Requirement**: All staff access authenticated via government SSO. API access authenticated via API keys with rate limiting. RBAC with roles: Admin, Analyst, Developer (API-only), EHRC (read-only enforcement data), Tester (panel members).

**Priority**: MUST_HAVE

---

### Accessibility Requirements

#### NFR-ACC-001: Platform Accessibility

**Requirement**: The platform itself MUST meet WCAG 2.2 Level AAA. As an accessibility compliance tool, it must be exemplary in its own accessibility.

**Priority**: MUST_HAVE

---

#### NFR-ACC-002: Assistive Technology Compatibility

**Requirement**: The platform must be fully functional with JAWS 2024+, NVDA 2024+, VoiceOver (macOS/iOS), TalkBack (Android), Dragon NaturallySpeaking, and ZoomText.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Uptime

**Requirement**: 99.9% uptime for the dashboard and API (8.7 hours maximum unplanned downtime per year).

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: axe-core Integration

**Purpose**: Primary automated accessibility testing engine

**Integration Type**: Embedded library (npm package) running within scanning workers

**Data Exchanged**: URLs submitted for scanning; WCAG violation results returned

**Priority**: MUST_HAVE

---

### INT-002: WAVE API Integration

**Purpose**: Secondary automated accessibility testing engine for cross-validation

**Integration Type**: REST API

**Data Exchanged**: URLs submitted; accessibility evaluation results returned

**Authentication**: API key

**Priority**: SHOULD_HAVE

---

### INT-003: GOV.UK Domain Registry

**Purpose**: Automated discovery and registration of public sector websites

**Integration Type**: Batch file import (CSV/JSON)

**Data Exchanged**: Domain names, organisation ownership, sector classification

**Priority**: MUST_HAVE

---

### INT-004: GDS Design System

**Purpose**: Link remediation guidance to GOV.UK Design System patterns and components

**Integration Type**: Static reference linking (URL-based)

**Data Exchanged**: Component references mapped to WCAG success criteria

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity: Website

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| url | String(2048) | Yes | Website URL |
| organisation_id | UUID | Yes | Owning organisation |
| sector | Enum | Yes | Government sector classification |
| registration_date | Timestamp | Yes | When registered |
| last_scan_date | Timestamp | No | Most recent scan |
| status | Enum | Yes | active, paused, deregistered |

#### Entity: ScanResult

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| website_id | UUID | Yes | Website scanned |
| scan_date | Timestamp | Yes | When scan executed |
| engine | Enum | Yes | axe-core, WAVE, manual, user-test |
| pages_scanned | Integer | Yes | Number of pages scanned |
| violations_count | Integer | Yes | Total violations found |
| compliance_score | Decimal | Yes | 0-100 compliance score |

#### Entity: Violation

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| scan_result_id | UUID | Yes | Parent scan result |
| wcag_criterion | String(20) | Yes | WCAG 2.2 success criterion (e.g., 1.1.1) |
| severity | Enum | Yes | critical, serious, moderate, minor |
| element_selector | String(500) | Yes | CSS selector of violating element |
| description | Text | Yes | Violation description |
| remediation_guidance | Text | No | Fix recommendation |

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use Crown Hosting or approved UK-sovereign cloud infrastructure (AWS GovCloud UK, Azure UK regions)

**TC-2**: Must integrate with GDS existing authentication infrastructure (Signon)

**TC-3**: Scanning must respect target website robots.txt and implement rate limiting

### Assumptions

**A-1**: GOV.UK domain registry data is available and maintained for automated website discovery

**A-2**: axe-core and WAVE APIs will remain available and license-compatible

**A-3**: Departmental web teams will have capacity to act on remediation guidance

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Public sector WCAG 2.2 compliance rate | 40% | 70% | 24 months | Automated scan results |
| Websites scanned monthly | 500 | 11,400 | 12 months | Platform analytics |
| Cost per website assessed | GBP 5,000-15,000 | GBP 50-200 | 12 months | Operating cost / websites |
| Departments using API | 0 | 50 | 24 months | API key registrations |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| GDS Director General | Business Sponsor | PENDING | | |
| GDS Head of Accessibility | Domain Expert | PENDING | | |
| EHRC | External Stakeholder | PENDING | | |
| RNIB | External Stakeholder | PENDING | | |
| CDDO | Assurance | PENDING | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PSBAR 2018 | Legislation | legislation.gov.uk | Monitoring and enforcement requirements | N/A |
| WCAG 2.2 | Standard | W3C | Success criteria for automated scanning rules | N/A |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | projects/001-accessibility-compliance-platform/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Accessibility Compliance Platform
**Model**: Claude Opus 4.6
