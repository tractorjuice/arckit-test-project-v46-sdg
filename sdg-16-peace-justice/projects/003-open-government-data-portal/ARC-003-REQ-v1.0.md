# Project Requirements: Open Government Data Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Open Government Data Portal (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Open Government Data Portal |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office Transparency Team, CDDO, Government Data Quality Hub |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

---

## Executive Summary

### Business Context

The UK government's current open data platform (data.gov.uk) was launched in 2010 and has served well but now faces significant technical debt, poor discoverability, inconsistent data quality, and limited API capabilities. The 5th Open Government Partnership National Action Plan commits the UK to improving transparency and open data maturity. SDG 16.6 requires effective, accountable, and transparent institutions at all levels.

This project delivers a modern Open Government Data Portal that enables government departments to publish high-quality, machine-readable open data with comprehensive metadata, developer-friendly APIs, and automated data quality assessment — positioning the UK as a continued global leader in government transparency.

### Objectives

- Replace the ageing data.gov.uk platform with a modern, scalable open data portal
- Achieve 4-star open data maturity for at least 80% of published datasets
- Provide developer-friendly APIs enabling civic technology and research applications
- Automate data quality assessment and publication workflows for departments
- Deliver a transparency dashboard tracking OGP National Action Plan commitments

### Expected Outcomes

- 80% of datasets at 4-star open data maturity within 18 months
- 15+ departments actively publishing data monthly
- 100+ external applications consuming portal APIs
- 50% reduction in FOI requests for data that is proactively published
- UK ranking maintained in top 5 on Open Data Barometer

### Project Scope

**In Scope**:

- Data publishing platform with departmental self-service
- Dataset discovery, search, and download
- RESTful API for programmatic data access
- Automated data quality assessment (completeness, timeliness, format compliance)
- Metadata management aligned with DCAT-AP UK profile
- Transparency dashboard for OGP commitment tracking
- Data visualisation for key datasets (spending, contracts, workforce)
- Departmental onboarding and data pipeline tools

**Out of Scope**:

- Departmental source system changes (departments responsible for their own data)
- Geospatial data infrastructure (Ordnance Survey responsibility)
- Statistical data publication (ONS/UK Statistics Authority responsibility)
- Personal data publication (GDPR constraints)

---

## Business Requirements

### BR-1: Modern Open Data Publishing Platform

**Description**: The system must provide a modern, scalable platform for government departments to publish open datasets with comprehensive metadata, automated quality checks, and version control.

**Rationale**: The current data.gov.uk platform is technically outdated, has poor search and discovery, and does not enforce data quality standards. A modern platform is essential for the UK's OGP commitments and SDG 16.6 obligations.

**Success Criteria**:

- Departments can publish datasets in under 15 minutes through self-service interface
- Automated data quality score calculated for every published dataset
- Version history maintained for all datasets with change notifications
- 99.9% platform availability

**Priority**: MUST_HAVE
**Stakeholder**: Minister for the Cabinet Office, CDDO

---

### BR-2: Developer-Friendly API Access

**Description**: The system must provide RESTful APIs enabling developers, researchers, and civic technology organisations to programmatically access all published datasets with filtering, pagination, and format negotiation.

**Rationale**: Open data creates maximum value when it is machine-readable and accessible via APIs. The ODI and civic technology community (mySociety, OpenCorporates, etc.) require API access to build public-benefit applications.

**Success Criteria**:

- All datasets accessible via documented RESTful API
- API supports JSON, CSV, and GeoJSON output formats
- API rate limits sufficient for production applications (1,000 requests/minute per consumer)
- Comprehensive API documentation with interactive examples

**Priority**: MUST_HAVE
**Stakeholder**: ODI, mySociety, academic researchers

---

### BR-3: Automated Data Quality Assessment

**Description**: The system must automatically assess published datasets against defined quality criteria (completeness, format compliance, timeliness, metadata quality) and assign a data quality score visible to publishers and consumers.

**Rationale**: Data quality is the primary barrier to data reuse. Publishing low-quality data undermines trust and wastes consumer effort. Automated assessment creates transparency about quality and motivates improvement.

**Success Criteria**:

- Quality score calculated within 5 minutes of dataset publication
- Quality dimensions: completeness, format compliance, timeliness, metadata quality, accessibility
- Quality trends tracked over time per department
- Quality thresholds configurable (minimum 3-star for publication)

**Priority**: MUST_HAVE
**Stakeholder**: Government Data Quality Hub, CDDO

---

### BR-4: Transparency Dashboard

**Description**: The system must provide a public-facing dashboard tracking the UK's progress against OGP National Action Plan commitments, including dataset publication metrics, data quality trends, and departmental compliance.

**Rationale**: OGP requires countries to report on commitment delivery. A public dashboard demonstrates accountability and provides evidence for the Independent Reporting Mechanism assessment.

**Success Criteria**:

- Real-time metrics on total datasets, quality scores, departmental activity
- OGP commitment progress tracking with status indicators
- Exportable data for OGP reporting
- Public accessibility without authentication

**Priority**: SHOULD_HAVE
**Stakeholder**: Minister, OGP, Transparency International

---

## Functional Requirements

### FR-1: Dataset Publishing and Management

**Description**: System must enable departmental publishers to upload, update, and manage datasets through a self-service web interface with version control.

**Acceptance Criteria**:

- [ ] Given a departmental publisher, when they upload a CSV dataset, then the system validates the format, generates a preview, and prompts for metadata
- [ ] Given an existing dataset, when the publisher uploads a new version, then the previous version is archived and a change notification sent to subscribers
- [ ] Given a dataset with scheduled updates (e.g., monthly spending), when the update is overdue, then the publisher and portal administrators are alerted

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-2: Dataset Discovery and Search

**Description**: System must provide full-text search, faceted filtering (by department, topic, format, quality score, date), and topic-based browsing for dataset discovery.

**Acceptance Criteria**:

- [ ] Given a search query, when results are returned, then they are ranked by relevance with quality score and last-updated date visible
- [ ] Given faceted filters, when a user selects "Cabinet Office" and "Spending", then only matching datasets are displayed
- [ ] Given a dataset detail page, when displayed, then metadata, quality score, download links, API endpoint, and related datasets are shown

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-3: RESTful Data API

**Description**: System must expose all published datasets via a RESTful API with documentation, authentication (API key), rate limiting, and content negotiation.

**Acceptance Criteria**:

- [ ] Given a valid API key, when a consumer requests a dataset, then data is returned in the requested format (JSON, CSV, GeoJSON) within 500ms
- [ ] Given a large dataset, when a consumer requests data, then pagination is applied with standard link headers
- [ ] Given API documentation, when a developer accesses it, then interactive examples demonstrate each endpoint

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-4: Automated Data Quality Scoring

**Description**: System must automatically assess each published dataset against quality dimensions and assign a composite quality score (0-100) with dimension-level breakdowns.

**Acceptance Criteria**:

- [ ] Given a newly published dataset, when quality assessment runs, then a score is assigned within 5 minutes covering completeness, format, timeliness, metadata, and accessibility
- [ ] Given a dataset below the minimum quality threshold, when published, then the publisher receives specific guidance on improvements needed
- [ ] Given quality scores over time, when the dashboard is viewed, then trends are visible per department and per dataset

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-5: Metadata Management (DCAT-AP UK)

**Description**: System must enforce metadata standards aligned with the DCAT Application Profile for UK Government, ensuring all datasets have discoverable, standardised metadata.

**Acceptance Criteria**:

- [ ] Given a dataset publication, when metadata is entered, then mandatory fields (title, description, publisher, licence, update frequency, contact) are enforced
- [ ] Given metadata, when exported, then it conforms to DCAT-AP UK JSON-LD schema
- [ ] Given a dataset, when it is harvested by external catalogues, then metadata is available via standard harvesting protocols (DCAT, CKAN API)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-6: Departmental Data Pipeline Integration

**Description**: System must support automated data ingestion from departmental source systems via scheduled API pulls, file upload (SFTP), or webhook triggers.

**Acceptance Criteria**:

- [ ] Given a configured data pipeline, when new data is available in the source system, then it is automatically ingested, quality-checked, and published
- [ ] Given a pipeline failure, when ingestion fails, then the publisher is notified with error details and the previous version remains live

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

### FR-7: Data Visualisation for Key Datasets

**Description**: System must provide basic interactive visualisations (charts, tables, maps) for high-value datasets including government spending, contracts, and workforce data.

**Acceptance Criteria**:

- [ ] Given a spending dataset, when a citizen accesses it, then a bar chart showing spending by department is displayed alongside the raw data download
- [ ] Given a contracts dataset, when filtered by department, then contract values and supplier names are displayed in an interactive table
- [ ] Given visualisations, when accessed on mobile, then they are responsive and usable

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Response Time

**Requirement**: Portal page load below 2 seconds at p95. API response below 500ms at p95. Search results below 1 second.

**Load Conditions**: Peak 5,000 concurrent users. Average 1,000 concurrent users. 50,000 datasets in catalogue.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% uptime. Maximum planned downtime 4 hours per month outside business hours.

**Priority**: HIGH

---

### NFR-SEC-1: Security

**Requirement**: Publisher authentication via government single sign-on. API consumers authenticated via API key. All data in transit encrypted (TLS 1.3+). Published data is public by design — no access control on published datasets. Publisher activity audit logged.

**Priority**: HIGH

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. Datasets downloadable in open formats (CSV, JSON) that are inherently accessible. Visualisations must include data tables as accessible alternatives.

**Priority**: CRITICAL

---

### NFR-I-1: Open Standards Compliance

**Requirement**: DCAT-AP UK metadata standard. Open Government Licence (OGL) applied by default. CSV on the Web (CSVW) for tabular data documentation. OpenAPI 3.0 for API documentation.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Government Single Sign-On

**Purpose**: Publisher authentication for departmental data managers.
**Integration Type**: SAML 2.0 / OAuth 2.0
**Priority**: MUST_HAVE

---

### INT-2: External Catalogue Harvesting

**Purpose**: Enable external data catalogues (European Data Portal, academic repositories) to harvest metadata.
**Integration Type**: DCAT-AP harvesting endpoint, CKAN-compatible API
**Priority**: SHOULD_HAVE

---

### INT-3: GOV.UK Notify

**Purpose**: Send notifications to data subscribers and publishers (dataset updates, quality alerts, overdue publications).
**Integration Type**: API
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Key Data Entities

| Entity | Description | Volume | Classification | Retention |
|--------|-------------|--------|---------------|-----------|
| Dataset | Published open data file with metadata | 50,000 datasets | PUBLIC | Indefinite (open data) |
| Dataset Version | Versioned snapshot of a dataset | 200,000 versions | PUBLIC | Indefinite |
| Metadata Record | DCAT-AP UK metadata for each dataset | 50,000 records | PUBLIC | Indefinite |
| Quality Assessment | Automated quality score and dimension scores | 200,000 assessments | OFFICIAL | 5 years |
| Publisher Account | Departmental data manager account | 500 accounts | OFFICIAL | Active + 1 year |
| API Consumer | Registered API consumer application | 5,000 registrations | OFFICIAL | Active + 1 year |

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Datasets at 4-star maturity | ~30% | 80% | 18 months |
| Active publishing departments | 8 | 15+ | 12 months |
| External API consumers | ~50 | 100+ | 18 months |
| Dataset publication time | 2+ hours | Under 15 minutes | 6 months |
| FOI requests for published data | Baseline TBD | 50% reduction | 24 months |

---

## Dependencies and Risks

| Risk ID | Description | Probability | Impact | Mitigation |
|---------|-------------|-------------|--------|------------|
| R-1 | Departments do not prioritise data publication | HIGH | HIGH | Ministerial mandate, central support team, automated pipelines |
| R-2 | Data quality too poor for meaningful publication | MEDIUM | MEDIUM | Quality framework with "good enough" thresholds, improvement guidance |
| R-3 | Low external API adoption | MEDIUM | MEDIUM | Developer outreach, hackathons, ODI partnership |
| R-4 | data.gov.uk migration data loss | LOW | HIGH | Full catalogue export, reconciliation, parallel running |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| DCAT-AP UK | Data Catalogue Vocabulary Application Profile for UK Government |
| OGP | Open Government Partnership |
| OGL | Open Government Licence |
| 5-star Open Data | Tim Berners-Lee's maturity model: 1-star (available) to 5-star (linked data) |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 16 Architecture Principles
- ARC-003-STKE-v1.0 — Open Government Data Portal Stakeholder Analysis
- UK 5th OGP National Action Plan
- 5-star Open Data Model

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Open Government Data Portal
**Model**: Claude Opus 4.6
