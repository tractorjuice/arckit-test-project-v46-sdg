# Project Requirements: Workplace Equality Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Workplace Equality Monitoring (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Workplace Equality Platform, EHRC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | EHRC Board, GEO, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for a platform enabling EHRC to monitor workplace equality compliance, support employer reporting, and provide public transparency on employer equality performance.

---

## Executive Summary

### Business Context

The Equality and Human Rights Commission (EHRC) is the statutory body responsible for enforcing equality legislation in England, Wales, and Scotland. The Equality Act 2010 provides EHRC with investigation powers (Section 20), compliance agreements (Section 23), and court application powers (Section 24). However, EHRC's ability to deploy these powers effectively is hampered by a lack of systematic equality data. Currently, enforcement targets are identified reactively through media coverage, complaints, and political pressure rather than through data-driven analysis.

The Workplace Equality Monitoring platform will aggregate equality data from multiple sources (gender pay gap reports, workforce diversity returns, employment tribunal outcomes, PSED publications), apply risk-scoring algorithms to identify potential compliance failures, and provide a public transparency dashboard enabling workers and civil society to scrutinise employer performance.

### Objectives

- Enable EHRC to identify employers with systemic equality compliance risks through automated data analysis
- Provide a unified equality reporting interface reducing employer burden
- Publish a public equality transparency dashboard
- Support PSED compliance for public sector organisations
- Generate evidence for EHRC strategic enforcement decisions

### Project Scope

**In Scope**:

- Equality data aggregation from existing sources (pay gap reports, tribunal data, PSED publications)
- Employer compliance risk-scoring engine (internal EHRC tool)
- Employer self-service reporting portal for voluntary equality data
- Public transparency dashboard with employer equality indicators
- PSED compliance framework for public sector bodies
- Integration with Gender Pay Gap Reporting Platform (Project 001)
- Intersectional equality analysis capability

**Out of Scope**:

- Individual employee complaint handling (EHRC existing case management)
- Employment tribunal case management (MoJ HMCTS system)
- Mandatory new reporting obligations (requires legislative change)

---

## Business Requirements

### BR-1: Automated Equality Compliance Risk Detection

**Description**: The platform must aggregate equality data from multiple sources and apply risk-scoring algorithms to identify employers with patterns suggesting systemic equality non-compliance, enabling EHRC to prioritise enforcement resources.

**Rationale**: EHRC has finite enforcement resources. Data-driven prioritisation ensures these resources target employers where intervention will have the greatest impact on equality outcomes.

**Success Criteria**:

- Risk-scoring engine processes data from 20,000+ employers
- 60% of enforcement targets identified proactively rather than reactively
- Risk scores validated against historic enforcement outcomes (retrospective accuracy test)

**Priority**: MUST_HAVE

---

### BR-2: Unified Employer Equality Reporting

**Description**: The platform must provide a single reporting interface where employers can submit equality data, with pre-population from existing data sources to minimise duplicate reporting.

**Rationale**: Employers currently submit equality data to multiple bodies (GEO for pay gap, EHRC for inquiries, departmental HR for workforce diversity) in different formats. A unified interface reduces burden and improves data quality.

**Success Criteria**:

- Pre-population of pay gap data from the Gender Pay Gap Reporting Platform (Project 001)
- Single sign-on with employer account across equality reporting services
- Employer satisfaction score of 60%+ with reporting process

**Priority**: MUST_HAVE

---

### BR-3: Public Equality Transparency Dashboard

**Description**: The platform must publish employer equality indicators in an accessible, searchable public dashboard, enabling employees, unions, and civil society to scrutinise employer equality performance.

**Rationale**: Public transparency is the most powerful accountability mechanism for workplace equality. The TUC and equality organisations have consistently called for accessible employer equality data.

**Success Criteria**:

- Dashboard searchable by employer, sector, region, and protected characteristic
- Open data API for independent analysis
- 50,000+ monthly unique visitors within 12 months

**Priority**: MUST_HAVE

---

### BR-4: PSED Compliance Framework

**Description**: The platform must provide public sector bodies with a standardised framework for demonstrating compliance with the Public Sector Equality Duty, including evidence upload, equality analysis templates, and compliance self-assessment.

**Rationale**: PSED compliance is currently inconsistent across public bodies. A standardised framework raises the quality floor and provides EHRC with visibility of compliance across the public sector.

**Success Criteria**:

- Standardised PSED evidence framework published and adopted by 200+ public bodies
- Equality analysis template used for 80%+ of new policies and decisions
- EHRC can assess PSED compliance status across public sector from platform data

**Priority**: SHOULD_HAVE

---

### BR-5: Intersectional Equality Analysis

**Description**: The platform must support intersectional analysis — examining how protected characteristics interact (e.g., gender and ethnicity, gender and disability) to identify compounding disadvantage patterns.

**Rationale**: The Equality Act 2010 Section 14 (dual discrimination) and PSED guidance require consideration of intersectional impacts. Single-axis analysis misses patterns of compounding disadvantage.

**Success Criteria**:

- Intersectional queries across at least three protected characteristics
- Statistical disclosure control for intersectional cohorts
- Intersectional analysis available in both EHRC internal and public dashboard views

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Helen — EHRC Enforcement Analyst

- **Role**: Senior analyst in EHRC enforcement division responsible for identifying investigation targets
- **Goals**: Identify employers with systemic equality failures; build evidence packages for Section 20 investigations; track enforcement outcomes
- **Pain Points**: Currently relies on media monitoring and complaints; no systematic data analysis capability; cannot identify patterns across protected characteristics
- **Technical Proficiency**: High

#### Persona 2: David — HR Director (Private Sector)

- **Role**: HR Director at a FTSE 100 company, responsible for equality and diversity compliance
- **Goals**: Demonstrate compliance with equality obligations; understand how EHRC assesses his employer; benchmark against sector peers
- **Pain Points**: Multiple reporting obligations to different bodies; no single view of compliance status; fear of enforcement based on incomplete data
- **Technical Proficiency**: Medium

#### Persona 3: Councillor Priya — Local Authority Equality Lead

- **Role**: Elected member with equality portfolio on a metropolitan borough council
- **Goals**: Ensure council meets PSED obligations; publish meaningful equality objectives; demonstrate due regard in decision-making
- **Pain Points**: No standardised PSED compliance framework; relies on officers' interpretation; equality analysis quality varies widely
- **Technical Proficiency**: Low-Medium

---

### Functional Requirements Detail

#### FR-1: Equality Data Aggregation Engine

**Description**: The system must ingest equality data from multiple sources including the Gender Pay Gap Reporting Platform (Project 001), Employment Tribunal outcomes (HMCTS), workforce diversity returns, and EHRC complaint records.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given pay gap data from Project 001, when ingested, then data is matched to employer records by Companies House number
- [ ] Given tribunal outcome data, when ingested, then discrimination findings are categorised by protected characteristic and employer
- [ ] Given data from multiple sources, when aggregated, then employer equality profile is updated with source attribution and freshness indicators

**Priority**: MUST_HAVE

---

#### FR-2: Compliance Risk-Scoring Engine

**Description**: The system must calculate a composite equality compliance risk score for each employer based on available data, using a transparent, auditable algorithm that can withstand judicial review if challenged.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an employer with data from multiple sources, then a risk score is calculated using a documented, auditable algorithm
- [ ] Given the risk-scoring algorithm, then it is reviewable by EHRC legal and publishable (transparency)
- [ ] Given risk scores, then EHRC enforcement analysts can filter and rank employers by risk level
- [ ] Given a risk score, then the contributing factors are explainable (not a black box)

**Priority**: MUST_HAVE

---

#### FR-3: Employer Self-Service Portal

**Description**: The system must provide an employer portal for voluntary submission of equality data beyond mandatory requirements, with pre-population from existing data sources.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an employer, then they can view their current equality data as held by EHRC
- [ ] Given pre-populated pay gap data, then employers can review and supplement with additional voluntary data
- [ ] Given voluntary submission, then employers can add narrative context to their equality data

**Priority**: MUST_HAVE

---

#### FR-4: Public Transparency Dashboard

**Description**: The system must provide a public-facing dashboard displaying employer equality indicators, searchable and filterable by name, sector, region, and protected characteristic.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given published data, then users can search by employer name
- [ ] Given sector or region, then users can view aggregate equality metrics
- [ ] Given an employer, then users can see pay gap data, tribunal history (published), and PSED status (public sector)
- [ ] Given the dashboard, then it complies with WCAG 2.2 Level AA and GOV.UK Design System

**Priority**: MUST_HAVE

---

#### FR-5: PSED Compliance Self-Assessment

**Description**: The system must provide public sector bodies with a self-assessment framework for PSED compliance, including templates for equality analysis, equality objectives, and annual reporting.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a public sector body, then they can complete a PSED self-assessment using a standardised framework
- [ ] Given equality analysis templates, then bodies can complete and store analyses against specific decisions and policies
- [ ] Given PSED compliance data across public sector, then EHRC can view aggregate compliance status

**Priority**: SHOULD_HAVE

---

#### FR-6: Open Data API

**Description**: The system must provide a versioned REST API for published equality data, enabling independent analysis by researchers, unions, and civil society.

**Relates To**: BR-3

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: EHRC staff authenticate via departmental SSO. Employer users authenticate via GOV.UK One Login. Public dashboard requires no authentication.

**Priority**: MUST_HAVE

---

#### NFR-SEC-2: Data Protection

**Requirement**: Full UK GDPR compliance. Risk scores classified as OFFICIAL-SENSITIVE (internal EHRC use only — not published). Employee complaint data anonymised in all external views.

**Priority**: MUST_HAVE

---

### Performance Requirements

#### NFR-P-1: Dashboard Response Time

**Requirement**: Public dashboard pages load within 2 seconds (p95). Risk-scoring batch processing completes within 4 hours for 20,000+ employers.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-1: 99.9% Availability

**Requirement**: 99.9% uptime for public dashboard and employer portal. EHRC internal tools: 99.5% uptime (business hours).

**RTO**: 4 hours | **RPO**: 1 hour

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-1: Equality Act 2010 Alignment

**Requirement**: All protected characteristics defined in the platform must align precisely with the Equality Act 2010 definitions. Risk-scoring must be defensible under judicial review.

**Priority**: MUST_HAVE

---

#### NFR-C-2: WCAG 2.2 Level AA

**Requirement**: All public-facing components must meet WCAG 2.2 Level AA. GOV.UK Design System for all citizen-facing interfaces.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Integration with Gender Pay Gap Reporting Platform (Project 001)

**Purpose**: Ingest validated employer pay gap data to feed the equality data aggregation engine.

**Integration Type**: API (consume open data API from Project 001)

**Priority**: MUST_HAVE

---

### INT-2: Integration with HMCTS Employment Tribunal Data

**Purpose**: Ingest employment tribunal outcomes involving discrimination claims.

**Integration Type**: Batch data feed (quarterly)

**Priority**: SHOULD_HAVE

---

### INT-3: Integration with Companies House

**Purpose**: Employer validation and SIC code classification.

**Integration Type**: REST API

**Priority**: MUST_HAVE

---

## Data Requirements

### Key Data Entities

#### Entity: Employer Equality Profile

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| employer_id | UUID | Yes | Unique identifier |
| companies_house_number | String(8) | Yes | CH registration |
| pay_gap_data | JSON | No | Latest pay gap metrics (from Project 001) |
| tribunal_outcomes | Array(JSON) | No | Discrimination findings |
| psed_status | Enum | No | PSED compliance status (public sector only) |
| risk_score | Decimal(5,2) | No | EHRC internal risk score |
| risk_score_factors | JSON | No | Contributing factors to risk score |

**Data Classification**: OFFICIAL (published data); OFFICIAL-SENSITIVE (risk scores, internal analysis)

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Proactive enforcement targets (vs reactive) | 10% | 60% | 24 months |
| Employer satisfaction with reporting | Not measured | 60% | 12 months |
| Public dashboard monthly visitors | 0 | 50,000 | 12 months |
| PSED compliance self-assessments completed | 0 | 200+ public bodies | 24 months |
| Risk-scoring retrospective accuracy | N/A | 75% alignment with historic outcomes | 18 months |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Workplace Equality Monitoring (Project 003)
**Model**: Claude Opus 4.6
