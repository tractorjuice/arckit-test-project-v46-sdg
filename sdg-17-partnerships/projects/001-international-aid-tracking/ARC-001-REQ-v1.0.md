# Project Requirements: International Aid Tracking

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | International Aid Tracking (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, International Aid Tracking Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | FCDO Digital, ICAI, CDDO, DAC Secretariat, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive business, functional, non-functional, integration, and data requirements for the International Aid Tracking platform. It traces requirements to stakeholder drivers (ARC-001-STKE-v1.0) and architecture principles (ARC-000-PRIN-v1.0).

---

## Executive Summary

### Business Context

The UK is one of the world's largest bilateral aid donors, disbursing approximately GBP 15 billion in Official Development Assistance (ODA) annually across 16 government departments. Current ODA tracking is fragmented across departmental systems, resulting in a 6-month lag for comprehensive UK ODA figures, inconsistent IATI data quality (71% score), and manual compilation of DAC statistical returns. The International Aid Tracking platform will consolidate ODA reporting, improve IATI compliance, and enable real-time ODA/GNI monitoring.

### Objectives

- Consolidate ODA reporting from 16 departments into a single federated platform
- Achieve IATI data quality score of 80%+ within 18 months
- Automate DAC CRS++ statistical return generation
- Provide ICAI with self-service access to non-classified ODA data
- Reduce time to produce comprehensive UK ODA figures from 6 months to 30 days

### Expected Outcomes

- UK maintains top-5 position in Publish What You Fund Aid Transparency Index
- HM Treasury achieves in-year ODA/GNI fiscal management capability
- ICAI evaluation turnaround improved by 40%
- 2,000+ staff hours/year saved through automated DAC reporting

### Project Scope

**In Scope**:

- All bilateral ODA activities managed by FCDO and other ODA-spending departments
- Multilateral ODA contributions (core and earmarked)
- IATI publication pipeline
- DAC CRS++ statistical reporting
- Cross-departmental ODA consolidation API
- ICAI data access portal

**Out of Scope**:

- Reform of departmental ODA programme management systems
- In-country project monitoring and evaluation tools
- ODA policy formulation and strategy
- Classified ODA programmes (handled via separate secure channel)

---

## Business Requirements

### BR-1: Comprehensive ODA Visibility

**Description**: Provide a single, authoritative view of all UK ODA across all 16 spending departments, updated within 30 days of quarter-end.

**Rationale**: Ministers, Treasury, and Parliament need timely, comprehensive ODA figures. Currently, 6 months are required to compile figures from all departments.

**Success Criteria**:

- All 16 ODA-spending departments contributing data
- Comprehensive UK ODA figure available within 30 days of quarter-end
- Figures reconciled with FCDO ARIES accounting system within 0.1% tolerance

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), HM Treasury (SD-2)

---

### BR-2: IATI Transparency Compliance

**Description**: Publish all UK ODA activity data to the IATI Registry in compliance with IATI Standard v2.03+, achieving a data quality score of 80%+.

**Rationale**: The UK has international commitments to aid transparency under the Busan Partnership. The IATI data quality score is publicly visible and affects the UK's Aid Transparency Index ranking.

**Success Criteria**:

- IATI Dashboard data quality score >= 80%
- 90% of activities updated within 30 days of change
- 100% of activities coded to CRS++ sectors
- 80% of activities with 3-year forward budget data

**Priority**: MUST_HAVE

**Stakeholder**: FCDO Head of Statistics (SD-4), Publish What You Fund (SD-6)

---

### BR-3: DAC Statistical Reporting Automation

**Description**: Automate the generation of OECD DAC CRS++ statistical returns, eliminating manual compilation and achieving zero manual corrections.

**Rationale**: Current DAC reporting requires 6 weeks of manual effort and 15% of records need correction. This is resource-intensive and error-prone.

**Success Criteria**:

- DAC statistical return generated automatically in < 1 day
- CRS++ validation pass rate at source: 99%+
- Zero manual corrections required for submission

**Priority**: MUST_HAVE

**Stakeholder**: FCDO Head of Statistics, OECD DAC (SD-4)

---

### BR-4: Independent Scrutiny Access

**Description**: Provide ICAI with self-service API access to all non-classified UK ODA data across all departments.

**Rationale**: ICAI independence requires direct data access without FCDO intermediation.

**Success Criteria**:

- 90% of ICAI data requests fulfilled via self-service
- Time from data request to access: < 1 day
- Historical data available for 7+ years

**Priority**: SHOULD_HAVE

**Stakeholder**: ICAI (SD-3)

---

### BR-5: ODA/GNI Fiscal Management

**Description**: Enable HM Treasury to monitor UK ODA spending against the GNI-linked target in near-real-time, with forecasting capability.

**Rationale**: ODA target is a percentage of GNI (a moving target). In-year fiscal management is currently impossible due to reporting lags.

**Success Criteria**:

- Provisional ODA/GNI ratio updated monthly
- Forecasting tool projecting year-end ODA/GNI based on commitment profiles
- Variance alerts when spending trajectory diverges from target by > 5%

**Priority**: SHOULD_HAVE

**Stakeholder**: HM Treasury (SD-2)

---

## Functional Requirements

### User Personas

#### Persona 1: FCDO Programme Manager

- **Role**: Manages ODA programmes in-country or from London
- **Goals**: Record ODA activities, disbursements, and results accurately and efficiently
- **Pain Points**: Double data entry (programme system and IATI), complex CRS++ coding
- **Technical Proficiency**: Medium

#### Persona 2: Departmental ODA Coordinator

- **Role**: Finance/policy officer in a non-FCDO ODA-spending department (e.g., BEIS, Defra)
- **Goals**: Submit quarterly ODA data with minimal effort
- **Pain Points**: Unfamiliar with CRS++ codes, ODA is secondary responsibility
- **Technical Proficiency**: Low-Medium

#### Persona 3: FCDO Statistician

- **Role**: Compiles DAC statistical returns and monitors IATI data quality
- **Goals**: Automated, validated reporting; comprehensive ODA visibility
- **Pain Points**: Manual data compilation across departments, error correction
- **Technical Proficiency**: High

#### Persona 4: ICAI Analyst

- **Role**: Conducts independent evaluations of UK aid effectiveness
- **Goals**: Access comprehensive ODA data quickly for evaluation design and analysis
- **Pain Points**: Bespoke data requests take 2-4 weeks, limited cross-departmental view
- **Technical Proficiency**: High

#### Persona 5: Treasury Economist

- **Role**: Monitors ODA/GNI ratio and forecasts ODA spending
- **Goals**: Near-real-time ODA spending visibility, forecasting tools
- **Pain Points**: 6-month lag in comprehensive ODA figures, GNI denominator changes
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: ODA Activity Registration

**Description**: The system must allow users to register new ODA activities with mandatory IATI and DAC CRS++ fields populated at creation.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a new ODA activity, when a user creates it, then all mandatory IATI fields are required (title, description, sector, country, dates, budget)
- [ ] Given an activity creation, when CRS++ sector is required, then the system presents a searchable lookup of valid DAC purpose codes with descriptions
- [ ] Given a non-FCDO department user, when creating an activity, then CRS++ codes are pre-suggested based on department and programme type

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-2: Cross-Departmental ODA Data Ingestion

**Description**: The system must ingest ODA data from all 16 departments via API, bulk upload (CSV/Excel), or manual entry.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given department data in CSV format, when uploaded, then data is validated against IATI/CRS++ schemas and errors reported per-row
- [ ] Given department API integration, when data is pushed, then it is validated and acknowledged within 5 seconds
- [ ] Given a department without API capability, when using bulk upload, then a template with pre-populated department codes is available

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: IATI Publication Pipeline

**Description**: The system must automatically generate IATI XML files and publish them to the IATI Registry within 30 days of activity update.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given updated activity data, when the publication pipeline runs, then IATI XML is generated compliant with IATI Standard v2.03+
- [ ] Given generated XML, when validated, then it passes the IATI Validator with zero errors
- [ ] Given validated XML, when published, then it appears on the IATI Registry within 24 hours of pipeline run

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: DAC CRS++ Statistical Return Generation

**Description**: The system must automatically generate DAC CRS++ statistical returns in the format required by the OECD DAC Secretariat.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given all departmental ODA data for a reporting period, when the DAC return is generated, then it includes all mandatory CRS++ fields
- [ ] Given the generated return, when validated against DAC business rules, then 99%+ of records pass validation
- [ ] Given a validated return, when exported, then it is in the DAC-specified format (XML/CSV) ready for submission

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-5: ODA Dashboard and Reporting

**Description**: The system must provide interactive dashboards showing UK ODA by department, country, sector, channel, and time period.

**Relates To**: BR-1, BR-5

**Acceptance Criteria**:

- [ ] Given a user, when accessing the dashboard, then they can filter ODA data by department, country, sector (CRS++), year, and flow type
- [ ] Given a Ministerial user, when viewing the dashboard, then a summary view shows total UK ODA, ODA/GNI ratio (provisional), and top recipients
- [ ] Given a Treasury user, when viewing the forecast, then projected year-end ODA/GNI is displayed with confidence intervals

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-6: ICAI Self-Service Data Portal

**Description**: The system must provide ICAI analysts with authenticated API access to query all non-classified UK ODA data.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given an ICAI analyst with valid credentials, when querying the API, then they can access ODA data across all departments
- [ ] Given a classified ODA programme, when ICAI queries the API, then classified data is excluded unless the analyst has appropriate clearance
- [ ] Given an API query, when executed, then results include activity-level detail with financial flows, sectors, countries, and results data

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-7: Results Framework Reporting

**Description**: The system must capture ODA results (outputs, outcomes) linked to activities and financial spend.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an ODA activity, when results are recorded, then they are linked to the activity and published via IATI results framework
- [ ] Given published results, when viewed on the IATI Registry, then they include indicator definitions, baseline values, target values, and actual values
- [ ] Given a portfolio of activities, when results are aggregated, then sector/country-level results summaries are generated

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-8: Forward Budget Publication

**Description**: The system must publish forward-looking ODA budget data for 3+ years via IATI.

**Relates To**: BR-2, BR-5

**Acceptance Criteria**:

- [ ] Given ODA activities with multi-year budgets, when published via IATI, then forward budget data is available for at least 3 years
- [ ] Given budget revisions, when updated, then IATI forward budgets reflect the latest approved figures within 30 days

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: API Response Time

**Requirement**: All API endpoints must respond within 500ms at the 95th percentile under normal load.

- IATI publication API: < 500ms (p95)
- Dashboard queries: < 2 seconds (p95)
- Cross-departmental data ingestion API: < 5 seconds per batch of 100 records

**Load Conditions**:

- Peak load: 200 concurrent users (FCDO and departmental staff)
- Data volume: 50,000+ ODA activities, 500,000+ financial transactions

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: System must achieve 99.9% uptime (8.76 hours maximum downtime/year).

- IATI publication pipeline: 99.9% (international commitment)
- Dashboard: 99.9% (Ministerial access)
- Data ingestion API: 99.5% (batch processing acceptable)

**Maintenance Windows**: Saturday 02:00-06:00 UTC (minimise impact on international partners)

**Priority**: HIGH

#### NFR-A-2: Disaster Recovery

**RPO**: 15 minutes (financial data, ODA transactions)
**RTO**: 1 hour (full service restoration)

**Backup Requirements**:

- Continuous replication to secondary UK region
- Daily backups retained for 7 years (NAO audit requirement)

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Authentication and Access Control

**Requirement**: Multi-factor authentication for all users; federated identity for cross-government access.

- FCDO staff: Single sign-on via departmental identity provider
- Other departments: Federated authentication via Government Identity Service
- ICAI: Dedicated API credentials with audit logging
- Classification-based access: OFFICIAL data default; OFFICIAL-SENSITIVE requires additional authorisation

**Priority**: CRITICAL

#### NFR-SEC-2: Data Encryption

**Requirement**: AES-256 encryption at rest; TLS 1.3 in transit; separate key management for OFFICIAL-SENSITIVE data.

**Priority**: CRITICAL

#### NFR-SEC-3: Audit Logging

**Requirement**: All data access, modification, and export operations logged with user identity, timestamp, and action detail. Logs retained 7 years.

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: IATI Standard Compliance

**Requirement**: All published data must validate against IATI Standard v2.03+ schema. Automated validation in data pipeline.

**Priority**: CRITICAL

#### NFR-C-2: DAC CRS++ Compliance

**Requirement**: All ODA classification must use valid DAC CRS++ purpose codes, flow types, and tied/untied status. Validation at data entry.

**Priority**: CRITICAL

#### NFR-C-3: UK GDPR Compliance

**Requirement**: Personal data minimisation; DPIA completed; international data transfers via IATI Registry comply with UK GDPR Chapter V.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.1 Level AA compliance for all user interfaces. GDS Design System patterns used throughout.

**Priority**: CRITICAL

#### NFR-U-2: Non-FCDO Department Usability

**Requirement**: Departmental ODA coordinators with low ODA expertise must be able to submit quarterly data in under 30 minutes using pre-populated templates and guided CRS++ coding.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: FCDO ARIES Accounting System

**Purpose**: Reconcile ODA financial data with FCDO's primary accounting system.

**Integration Type**: Batch file transfer (daily)

**Data Exchanged**:

- **From ARIES to Platform**: ODA disbursement records, commitment records, exchange rates
- **From Platform to ARIES**: Reconciliation reports, discrepancy alerts

**Authentication**: Mutual TLS within FCDO network

**Priority**: CRITICAL

---

### INT-2: IATI Registry

**Purpose**: Publish UK ODA activity data to the international IATI Registry.

**Integration Type**: API (IATI Registry API v2)

**Data Exchanged**:

- **From Platform to IATI Registry**: IATI XML activity files, organisation files

**Authentication**: API key (IATI publisher credentials)

**SLA**: Publication within 24 hours of pipeline run

**Priority**: CRITICAL

---

### INT-3: Cross-Government Data Sharing Platform (Project 002)

**Purpose**: Ingest ODA data from non-FCDO departments via the federated API gateway.

**Integration Type**: RESTful API via federated gateway

**Data Exchanged**:

- **From Departments to Platform**: Quarterly ODA activity and financial data
- **From Platform to Departments**: Validation results, confirmation receipts

**Authentication**: OAuth 2.0 via Government Identity Service

**Priority**: MUST_HAVE

---

### INT-4: HMRC Real Time Information (for imputed ODA)

**Purpose**: Access HMRC data for calculating imputed student costs (a component of UK ODA).

**Integration Type**: Batch data sharing under Digital Economy Act 2017

**Data Exchanged**:

- **From HMRC to Platform**: Aggregated international student data

**Authentication**: Secure file transfer with encryption

**Priority**: SHOULD_HAVE

---

### INT-5: ONS SDG Progress Dashboard (Project 003)

**Purpose**: Supply ODA-related SDG indicator data (e.g., 17.2.1 — ODA as percentage of GNI).

**Integration Type**: Event-driven notification + API

**Data Exchanged**:

- **From Platform to ONS**: ODA/GNI ratio, ODA by sector/country for SDG indicator calculation

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: ODA Activity

**Description**: A discrete ODA programme, project, or contribution

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| iati_identifier | String(100) | Yes | Unique IATI activity ID | Format: GB-GOV-{dept}-{id} |
| title | String(500) | Yes | Activity title | Multi-language support |
| description | Text | Yes | Activity description | Min 50 characters |
| reporting_org | String(50) | Yes | Reporting department | Valid IATI org ID |
| recipient_country | String(2) | Yes | ISO 3166-1 alpha-2 | Valid country code |
| sector_code | String(5) | Yes | DAC CRS++ purpose code | Valid CRS++ code |
| flow_type | Enum | Yes | ODA flow type | [10=ODA, 20=OOF, 30=Private] |
| tied_status | Enum | Yes | Tied/untied status | [1=Untied, 2=Tied, 3=Partially tied] |
| status | Enum | Yes | Activity status | [1=Pipeline, 2=Implementation, 3=Finalisation, 4=Closed, 5=Cancelled] |
| start_date | Date | Yes | Planned/actual start | ISO 8601 |
| end_date | Date | Yes | Planned/actual end | ISO 8601 |

**Data Volume**: ~50,000 active activities; 200,000+ historical

**Data Classification**: OFFICIAL (default); OFFICIAL-SENSITIVE for some programmes

#### Entity 2: Financial Transaction

**Description**: ODA financial flow (commitment, disbursement, expenditure)

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| transaction_id | UUID | Yes | Unique identifier | Primary key |
| activity_id | String(100) | Yes | Parent activity | Foreign key to Activity |
| transaction_type | Enum | Yes | Type of flow | [C=Commitment, D=Disbursement, E=Expenditure] |
| value | Decimal(15,2) | Yes | Amount | > 0 |
| currency | String(3) | Yes | ISO 4217 currency | Default: GBP |
| transaction_date | Date | Yes | Date of transaction | ISO 8601 |
| provider_org | String(50) | Yes | Funding department | Valid org ID |
| receiver_org | String(50) | No | Receiving organisation | Valid org ID if provided |

**Data Volume**: ~500,000 transactions/year

**Data Classification**: OFFICIAL

---

### Data Quality Requirements

**Data Accuracy**: ODA financial figures reconciled to ARIES within 0.1% tolerance

**Data Completeness**: All mandatory IATI and CRS++ fields populated; zero null mandatory fields

**Data Consistency**: Cross-departmental ODA totals reconciled quarterly; discrepancies > 1% flagged for investigation

**Data Timeliness**: Departmental data received within 30 days of quarter-end; IATI updated within 30 days of activity change

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with FCDO ARIES accounting system (Oracle-based, limited API capability)

**TC-2**: Must deploy on UK sovereign cloud (AWS GovCloud UK or equivalent)

**TC-3**: Must support federated access via Cross-Government Data Sharing Platform (Project 002)

### Business Constraints

**BC-1**: Must maintain uninterrupted DAC statistical reporting during transition (no gap in UK ODA figures)

**BC-2**: Budget cap of GBP 15M over 3 years

**BC-3**: Must not require departmental system replacement — federated ingestion from existing systems

### Assumptions

**A-1**: All 16 ODA-spending departments will participate (some may require Ministerial direction)

**A-2**: IATI Standard v2.03 will remain stable during implementation (v3.0 not expected before 2028)

**A-3**: Cross-Government Data Sharing Platform (Project 002) will be available for integration within 12 months

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| IATI data quality score | 71% | 80%+ | 18 months | IATI Dashboard |
| Time to comprehensive UK ODA figure | 6 months | 30 days | 24 months | Platform analytics |
| DAC return manual corrections | 15% of records | 0% | 18 months | DAC submission validation |
| ICAI self-service fulfilment | 0% | 90% | 12 months | API analytics |
| Aid Transparency Index rank | 4th | Top 3 | 24 months | PWYF assessment |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| FCDO CDIO | Enterprise Architect | [ ] Approved | PENDING | |
| FCDO Head of Statistics | DAC/IATI compliance | [ ] Approved | PENDING | |
| CDDO | Cross-government standards | [ ] Approved | PENDING | |
| ICAI | Independent scrutiny | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| ODA | Official Development Assistance — government aid promoting economic development |
| IATI | International Aid Transparency Initiative — global data standard for aid |
| DAC | Development Assistance Committee — OECD body governing ODA definitions |
| CRS++ | Creditor Reporting System — DAC activity-level reporting framework |
| GNI | Gross National Income — denominator for ODA/GNI target |
| ICAI | Independent Commission for Aid Impact — UK aid scrutiny body |
| ARIES | FCDO's primary accounting and financial management system |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 17 Architecture Principles
- ARC-001-STKE-v1.0 — International Aid Tracking Stakeholder Analysis
- IATI Standard v2.03 Technical Documentation
- OECD DAC Statistical Reporting Directives (DCD/DAC(2023)21/REV3)

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: International Aid Tracking
**Model**: Claude Opus 4.6
