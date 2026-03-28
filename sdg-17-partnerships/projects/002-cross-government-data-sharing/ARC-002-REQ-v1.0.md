# Project Requirements: Cross-Government Data Sharing Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Cross-Government Data Sharing Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Cross-Government Data Sharing Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office Digital, CDDO, Government Data Quality Hub, ICO, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Cross-Government Data Sharing Platform. It provides the shared data infrastructure that supports the International Aid Tracking (Project 001), SDG Progress Dashboard (Project 003), and Global Britain Trade Platform (Project 004).

---

## Executive Summary

### Business Context

UK Government departments hold vast data assets, but sharing data between departments is slow (3-6 months for a data sharing agreement), fragmented (bespoke point-to-point integrations), and often abandoned (40% of data requests never fulfilled). The Cross-Government Data Sharing Platform will provide a discoverable data catalogue, federated API gateway, and machine-readable data sharing agreement framework to enable secure, governed, and efficient cross-departmental data exchange.

### Objectives

- Create a DCAT-compliant cross-government data catalogue with 10+ departments within 18 months
- Implement a federated API gateway that enables governed data access without centralising data
- Reduce data sharing agreement execution time from 3-6 months to under 2 weeks
- Support SDG 17 programme data flows (ODA, statistics, trade) and broader cross-government needs
- Demonstrate UK GDPR compliance and ICO approval for the data sharing framework

### Expected Outcomes

- 80% reduction in data request to access time
- GBP 100M+ fraud detection through data matching capabilities
- GBP 15M/year savings from reduced duplicate data collection
- 50+ active cross-department data feeds within 24 months

### Project Scope

**In Scope**:

- Cross-government data catalogue (metadata discovery)
- Federated API gateway (governed data access)
- Data sharing agreement management system
- Authentication and authorisation federation
- Monitoring, audit, and compliance reporting

**Out of Scope**:

- Department-internal data management systems
- Data warehouse or data lake (data remains in source departments)
- Business intelligence or analytics tools
- Open data publication (covered by data.gov.uk)

---

## Business Requirements

### BR-1: Cross-Government Data Discovery

**Description**: Enable any authorised government user to discover what datasets exist across government, who owns them, and how to request access.

**Rationale**: Currently, departments do not know what data other departments hold. Data discovery relies on personal networks and ad hoc enquiries.

**Success Criteria**:

- 10+ departments with published catalogue entries within 18 months
- 200+ datasets catalogued
- Search queries: 500+ per month within 6 months of launch

**Priority**: MUST_HAVE

**Stakeholder**: Minister for the Cabinet Office (SD-1), CDDO (SD-3)

---

### BR-2: Federated Data Access

**Description**: Enable governed data access across departments without requiring data to be copied out of source systems.

**Rationale**: Department data sovereignty concerns (SD-2) make centralised data lakes unacceptable. Federated access preserves departmental control while enabling sharing.

**Success Criteria**:

- 50+ active cross-department data feeds via API gateway
- Data remains in source department infrastructure at all times
- Access controls enforced by source department

**Priority**: MUST_HAVE

**Stakeholder**: Department Data Leads (SD-2), Minister (SD-1)

---

### BR-3: Rapid Data Sharing Agreement Execution

**Description**: Reduce the time to establish a data sharing agreement from 3-6 months to under 2 weeks through standardised templates, machine-readable policies, and automated compliance checks.

**Rationale**: The current manual DSA process is the primary bottleneck for cross-government data sharing. Lengthy negotiations mean time-critical policy analysis proceeds without cross-departmental data.

**Success Criteria**:

- Median time from request to access: < 10 working days
- Standardised DSA template adopted across government
- Machine-readable DSA policies enforced by API gateway
- 80%+ of requests fulfilled within 10 working days

**Priority**: MUST_HAVE

**Stakeholder**: Minister (SD-1), CDDO (SD-3)

---

### BR-4: Lawful and Auditable Data Sharing

**Description**: Ensure all data sharing has a documented legal basis, is proportionate, and is fully auditable for ICO and NAO scrutiny.

**Rationale**: ICO expects demonstrable compliance with UK GDPR. Digital Economy Act 2017 provides gateways but requires documented implementation.

**Success Criteria**:

- Every active data share has a documented legal basis
- Data minimisation enforced technically (field-level access control)
- Complete audit trail of all data access events (7-year retention)
- Annual ICO compliance review passed

**Priority**: MUST_HAVE

**Stakeholder**: ICO (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: Department Data Publisher

- **Role**: Data lead or analyst responsible for making department datasets discoverable
- **Goals**: Publish dataset metadata, manage access requests, monitor usage
- **Pain Points**: No standardised catalogue; unclear what to publish; concerns about misuse
- **Technical Proficiency**: Medium-High

#### Persona 2: Department Data Consumer

- **Role**: Analyst or policy officer who needs data from another department
- **Goals**: Find relevant datasets, request access, consume data via API
- **Pain Points**: Does not know what data exists; DSA process takes months; bespoke integrations
- **Technical Proficiency**: Medium

#### Persona 3: Data Governance Officer

- **Role**: Departmental DPO or information governance lead
- **Goals**: Approve data sharing agreements, ensure compliance, audit access
- **Pain Points**: Paper-based DSA process; no visibility of actual data access patterns
- **Technical Proficiency**: Medium

#### Persona 4: Platform Administrator

- **Role**: Cabinet Office platform operations team
- **Goals**: Manage the federated gateway, onboard departments, monitor platform health
- **Pain Points**: Multi-cloud environment; heterogeneous department systems
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: DCAT-Compliant Data Catalogue

**Description**: The system must provide a searchable data catalogue where departments publish metadata about their datasets using DCAT (Data Catalog Vocabulary) standard.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a department publisher, when they create a catalogue entry, then DCAT mandatory fields are required (title, description, publisher, contact, theme, access rights, update frequency)
- [ ] Given a catalogue entry, when published, then it is discoverable via full-text search and faceted filtering (department, theme, classification, format)
- [ ] Given the catalogue, when queried via API, then it returns DCAT-AP compliant JSON-LD

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-2: Federated API Gateway

**Description**: The system must provide an API gateway that routes data requests to source department APIs, enforcing access control based on active data sharing agreements.

**Relates To**: BR-2, BR-4

**Acceptance Criteria**:

- [ ] Given a consumer with a valid DSA, when they query the gateway, then the request is routed to the source department API and the response returned
- [ ] Given a consumer without a valid DSA, when they query the gateway, then the request is denied with a 403 response indicating how to request access
- [ ] Given a DSA with field-level restrictions, when data is returned, then restricted fields are excluded from the response
- [ ] Given an API request, when processed, then the gateway logs the request metadata (consumer, dataset, timestamp, response status) without logging the data payload

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Data Sharing Agreement Management

**Description**: The system must provide a workflow for creating, reviewing, approving, and revoking data sharing agreements with machine-readable policy enforcement.

**Relates To**: BR-3, BR-4

**Acceptance Criteria**:

- [ ] Given a data consumer, when they request access to a dataset, then a DSA workflow is initiated with pre-populated template
- [ ] Given a DSA request, when submitted, then the source department's data governance officer receives a notification for review
- [ ] Given an approved DSA, when activated, then the API gateway automatically grants access according to DSA terms
- [ ] Given a DSA expiry or revocation, when the date passes, then API access is automatically revoked

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: Cross-Government Authentication Federation

**Description**: The system must authenticate users from any government department using their departmental identity, without requiring separate platform credentials.

**Relates To**: BR-2, BR-4

**Acceptance Criteria**:

- [ ] Given a user with departmental SSO, when accessing the platform, then they are authenticated via SAML 2.0 or OpenID Connect federation
- [ ] Given an authenticated user, when their department is identified, then their access is limited to datasets permitted under active DSAs for that department
- [ ] Given a service-to-service API call, when authenticated, then mutual TLS or OAuth 2.0 client credentials are used

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-5: Usage Monitoring and Analytics

**Description**: The system must provide dashboards showing data sharing activity: which departments are sharing, which datasets are most accessed, and DSA pipeline status.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a platform administrator, when viewing the dashboard, then they see: active DSAs, pending requests, API call volumes by department, and error rates
- [ ] Given a department data publisher, when viewing their datasets, then they see: consumers, access frequency, data volume transferred, and DSA status
- [ ] Given the Minister, when viewing the summary, then they see: number of departments participating, total datasets catalogued, total data shares active, and trend data

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-6: Data Quality Alerts

**Description**: The system must detect and notify source departments when data quality issues are detected by consuming departments.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a consuming department, when they report a data quality issue, then the source department's data lead receives a notification with details
- [ ] Given repeated quality issues for a dataset, when a threshold is breached, then an escalation is triggered to the data governance officer
- [ ] Given a quality issue resolution, when the source department confirms the fix, then the consuming department is notified

**Priority**: COULD_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: API Gateway Performance

**Requirement**: Federated API gateway must add no more than 50ms latency to source department API response times at the 95th percentile.

- Catalogue search: < 500ms (p95)
- DSA workflow actions: < 2 seconds (p95)
- Gateway throughput: 1,000 requests per second sustained

**Priority**: CRITICAL

---

### Availability and Resilience Requirements

#### NFR-A-1: Gateway Availability

**Requirement**: API gateway must achieve 99.95% uptime (26 minutes maximum downtime/year). This is critical shared infrastructure for the SDG 17 programme and broader cross-government data sharing.

**RTO**: 15 minutes (automated failover)
**RPO**: 0 minutes (active-active replication)

**Priority**: CRITICAL

#### NFR-A-2: Catalogue Availability

**Requirement**: Data catalogue must achieve 99.9% uptime.

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Zero-Trust Architecture

**Requirement**: All access decisions must be identity-based, verified per-request, with no implicit trust based on network location. Cross-department API calls must use mutual TLS or equivalent.

**Priority**: CRITICAL

#### NFR-SEC-2: Data Isolation

**Requirement**: Data from different departments must be logically isolated. No department can access another department's data without an active DSA enforced by the gateway. Gateway logs must not contain data payloads.

**Priority**: CRITICAL

#### NFR-SEC-3: Encryption

**Requirement**: TLS 1.3 for all data in transit; AES-256 at rest for catalogue, DSA, and audit data. Separate key management per department for any cached data.

**Priority**: CRITICAL

#### NFR-SEC-4: NCSC CAF Compliance

**Requirement**: Platform must achieve NCSC Cyber Assessment Framework compliance and maintain GovAssure certification.

**Priority**: CRITICAL

---

### Compliance Requirements

#### NFR-C-1: UK GDPR Compliance

**Requirement**: Full UK GDPR compliance including Article 5 principles, lawful basis documentation, DPIA, and data subject rights support.

**Priority**: CRITICAL

#### NFR-C-2: Digital Economy Act 2017

**Requirement**: Data sharing arrangements must comply with DEA 2017 gateways where used as legal basis. Approved researcher arrangements for statistical data sharing.

**Priority**: CRITICAL

#### NFR-C-3: Audit Trail

**Requirement**: Complete, tamper-evident audit trail of all data access decisions, DSA approvals, and API calls. 7-year retention. Auditable by ICO, NAO, and departmental DPOs.

**Priority**: CRITICAL

---

### Scalability Requirements

#### NFR-S-1: Department Onboarding Scale

**Requirement**: Platform must support onboarding of all central government departments (approx. 25 ministerial departments, 20 non-ministerial departments, 400+ executive agencies and public bodies) without architectural changes.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Department APIs (Federated)

**Purpose**: Route data requests to source department APIs.

**Integration Type**: RESTful API routing via gateway

**Authentication**: OAuth 2.0 / mutual TLS per department

**Key Consumers**: Project 001 (ODA data), Project 003 (SDG data), Project 004 (trade data)

**Priority**: CRITICAL

---

### INT-2: Government Identity Service

**Purpose**: Federated authentication across departments.

**Integration Type**: SAML 2.0 / OpenID Connect

**Priority**: CRITICAL

---

### INT-3: data.gov.uk

**Purpose**: Synchronise open data catalogue entries with the national open data portal.

**Integration Type**: DCAT harvest (one-way sync)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Dataset Catalogue Entry

**Description**: Metadata describing a dataset available for sharing

**Key Attributes**: DCAT standard fields — title, description, publisher, theme, spatial/temporal coverage, distribution format, access rights, update frequency, contact point

**Data Volume**: 1,000+ entries within 3 years

**Data Classification**: OFFICIAL (metadata only; data remains in source systems)

#### Entity 2: Data Sharing Agreement

**Description**: Formal agreement between data provider and consumer departments

**Key Attributes**: Provider department, consumer department, legal basis, purpose, datasets covered, field-level permissions, start date, expiry date, review schedule, approval chain

**Data Volume**: 500+ active DSAs within 3 years

**Data Classification**: OFFICIAL

#### Entity 3: API Access Log

**Description**: Audit record of every API call through the federated gateway

**Key Attributes**: Timestamp, consumer identity, dataset requested, source department, response status code, latency, data volume (bytes, not content)

**Data Volume**: ~10M records/year (1,000 req/sec peak)

**Data Classification**: OFFICIAL

**Retention**: 7 years

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must support multi-cloud — departments use AWS, Azure, and GCP; gateway cannot mandate a single provider

**TC-2**: Must not require departments to replace existing systems — adapter pattern for integration

**TC-3**: Must deploy on UK sovereign cloud for gateway and catalogue components

### Business Constraints

**BC-1**: Budget cap of GBP 25M over 3 years (including central platform and department adapter funding)

**BC-2**: Cannot mandate department participation — adoption must be incentivised, not forced (except via Ministerial direction)

**BC-3**: Must launch with at least 3 departments to demonstrate value (target: FCDO, HMRC, ONS for SDG 17)

### Assumptions

**A-1**: Government Identity Service or equivalent federation mechanism will be available within 12 months

**A-2**: Departments will allocate resource to develop API adapters (centrally funded)

**A-3**: ICO will support the standardised DSA framework (early engagement planned)

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Departments participating | 0 | 10+ | 18 months | Platform analytics |
| Datasets catalogued | 0 | 200+ | 18 months | Catalogue count |
| Active cross-dept data feeds | 0 | 50+ | 24 months | Gateway analytics |
| DSA execution time | 3-6 months | < 2 weeks | 18 months | Workflow analytics |
| Abandoned data requests | 40% | < 5% | 24 months | Request tracking |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| CDO, Cabinet Office | Data strategy | [ ] Approved | PENDING | |
| CDDO Director | Cross-government standards | [ ] Approved | PENDING | |
| ICO representative | Data protection | [ ] Approved | PENDING | |
| NCSC representative | Cyber security | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| DCAT | Data Catalog Vocabulary — W3C standard for data catalogue metadata |
| DSA | Data Sharing Agreement — formal agreement governing cross-department data exchange |
| DEA | Digital Economy Act 2017 — provides legal gateways for cross-government data sharing |
| Federated Gateway | API routing layer that directs requests to source department APIs |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 17 Architecture Principles
- ARC-002-STKE-v1.0 — Cross-Government Data Sharing Stakeholder Analysis
- National Data Strategy (2020)
- ICO Data Sharing Code of Practice
- DCAT Application Profile for data portals in Europe (DCAT-AP)
- GDS API Technical and Data Standards

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Cross-Government Data Sharing Platform
**Model**: Claude Opus 4.6
