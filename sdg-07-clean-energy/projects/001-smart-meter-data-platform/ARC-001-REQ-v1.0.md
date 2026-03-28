# Project Requirements: Smart Meter Data Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Smart Meter Data Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart Meter Data Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart Meter Programme Board, DESNZ Digital, DCC, Ofgem |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Smart Meter Data Platform — a national-scale system for collecting, processing, and analysing data from 53 million smart meters across Great Britain.

---

## Executive Summary

### Business Context

The UK has invested £13.5 billion in the smart meter rollout, installing approximately 53 million electricity and gas meters in domestic and small non-domestic premises. These meters generate half-hourly consumption readings transmitted via the Data Communications Company (DCC) infrastructure. Currently, this data is collected and held independently by individual energy suppliers, with no centralised government platform for national-scale analytics, consumer empowerment, or policy evaluation.

The Smart Meter Data Platform will establish a national data platform operated by DESNZ that ingests meter data via the DCC, provides consumers with personalised energy insights, and delivers anonymised analytics for policy evaluation, market monitoring, and grid balancing support.

### Objectives

- Ingest and process 2.5 billion half-hourly meter readings per day from 53 million smart meters
- Provide householders with personalised energy consumption insights via a GOV.UK-integrated web service
- Deliver anonymised, aggregated analytics to DESNZ, Ofgem, and National Grid ESO for policy and grid management
- Implement robust consumer consent management aligned with the Smart Energy Code and DCC consent framework
- Achieve GDS service assessment pass at Beta within 12 months

### Expected Outcomes

- 10 million registered householders actively using energy insights, saving an average of £50/year each (£500M aggregate annual savings)
- 3-5% reduction in average household energy consumption for active users, contributing 2.5 MtCO2e annual carbon reduction
- 5 core analytics products informing energy policy decisions across DESNZ, Ofgem, and National Grid ESO
- Zero reportable data privacy incidents; consumer trust maintained above 70%

### Project Scope

**In Scope**:
- Data ingestion from DCC for electricity and gas smart meters (SMETS2 and enrolled SMETS1)
- Consumer-facing web portal integrated with GOV.UK for energy insights
- Consent management aligned with DCC consent framework
- Anonymised analytics platform for government and regulatory users
- API layer for authorised third-party data access

**Out of Scope**:
- Smart meter installation or hardware
- DCC infrastructure upgrades
- Energy supplier billing systems
- Microgeneration and export metering (Phase 2)
- Non-domestic large-scale meters (industrial and commercial)

---

## Business Requirements

### BR-1: National Smart Meter Data Ingestion

**Description**: The platform must ingest half-hourly consumption data from all operational smart meters in Great Britain via the DCC infrastructure, creating a national repository of energy consumption data.

**Rationale**: A centralised data platform enables cross-supplier analytics, national policy evaluation, and consumer empowerment that individual supplier systems cannot provide. The Energy Act 2023 provides the legislative basis for government data access.

**Success Criteria**:
- 99.5% of expected meter readings ingested within 4 hours of collection
- Support for both SMETS2 and enrolled SMETS1 meter types
- Data validated against DCC technical specifications

**Priority**: MUST_HAVE
**Stakeholder**: DESNZ Smart Meter Programme Director

---

### BR-2: Consumer Energy Insights

**Description**: The platform must provide householders with understandable, actionable insights derived from their smart meter data, enabling them to reduce energy consumption and costs.

**Rationale**: Consumer benefit is the primary justification for the smart meter programme. The platform must demonstrate tangible household benefit to maintain political support and public trust.

**Success Criteria**:
- 10 million registered householders within 24 months of launch
- Consumer satisfaction score of 4.0/5.0 or above
- Measurable 3-5% consumption reduction for active users

**Priority**: MUST_HAVE
**Stakeholder**: Secretary of State for Energy Security and Net Zero

---

### BR-3: Policy and Regulatory Analytics

**Description**: The platform must deliver anonymised, aggregated energy consumption analytics to DESNZ, Ofgem, and National Grid ESO for policy evaluation, market monitoring, and grid balancing.

**Rationale**: National-scale consumption analytics do not currently exist outside estimated settlement data. Actual meter data enables evidence-based energy policy, fuel poverty identification, and grid demand forecasting.

**Success Criteria**:
- 5 core analytics products operational within 18 months
- Analytics cited in at least 3 published policy documents per year
- Data latency from collection to analytics availability under 24 hours

**Priority**: MUST_HAVE
**Stakeholder**: DESNZ Chief Analyst

---

### BR-4: Consumer Privacy and Consent

**Description**: The platform must implement robust consent management, ensuring consumers have genuine control over who accesses their granular energy data, aligned with the Smart Energy Code and UK GDPR.

**Rationale**: Consumer trust is the foundation of the smart meter data ecosystem. Half-hourly data reveals household occupancy and lifestyle patterns. Without consumer confidence in data handling, registration and engagement targets will not be met.

**Success Criteria**:
- Zero reportable data privacy incidents
- Consumer trust score maintained above 70%
- DCC consent framework fully implemented

**Priority**: MUST_HAVE
**Stakeholder**: DESNZ Data Protection Officer, ICO

---

### BR-5: Third-Party Data Access

**Description**: The platform must provide a controlled, consent-based API for authorised third parties (energy services companies, researchers, local authorities) to access consumer energy data.

**Rationale**: The energy transition requires an ecosystem of innovative services built on smart meter data. The government platform should enable this ecosystem while maintaining consumer protection, rather than restricting data to government use only.

**Success Criteria**:
- API available within 24 months of platform launch
- At least 20 authorised third-party organisations accessing data within 12 months of API launch
- All access audited and consent-verified

**Priority**: SHOULD_HAVE
**Stakeholder**: Ofgem

---

## Functional Requirements

### User Personas

#### Persona 1: Householder Hannah

- **Role**: Domestic energy consumer with smart meter
- **Goals**: Understand energy consumption, reduce bills, compare usage patterns
- **Pain Points**: Cannot interpret raw kWh data, does not understand tariff structures, worried about privacy
- **Technical Proficiency**: Low

#### Persona 2: Analyst Ahmed

- **Role**: DESNZ energy policy analyst
- **Goals**: Access national consumption trends, evaluate policy impact, identify fuel poverty patterns
- **Pain Points**: Currently relies on estimated settlement data with significant lag and limited granularity
- **Technical Proficiency**: High

#### Persona 3: Grid Operator Grace

- **Role**: National Grid ESO demand forecasting analyst
- **Goals**: Access aggregated demand data for grid balancing, improve renewable integration forecasting
- **Pain Points**: Currently uses estimated demand profiles; actual data would significantly improve accuracy
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: DCC Data Ingestion Pipeline

**Description**: The system must connect to the DCC infrastructure and ingest half-hourly meter reading data for all registered smart meters.

**Relates To**: BR-1

**Acceptance Criteria**:
- [ ] Given a valid DCC connection, when half-hourly data is transmitted, then readings are received and acknowledged within 60 seconds
- [ ] Given SMETS2 meter readings in DLMS/COSEM format, when received, then data is parsed and stored correctly
- [ ] Given enrolled SMETS1 readings via the DCC Adapter, when received, then data is parsed using the appropriate SMETS1-to-SMETS2 mapping
- [ ] Given a meter reading that fails validation, when processed, then the reading is quarantined with error code and flagged for investigation

**Data Requirements**:
- **Inputs**: DLMS/COSEM meter reading data via DCC DUIS (DCC User Interface Specification), meter MPAN, reading timestamp, consumption value (kWh), register type
- **Outputs**: Validated, stored consumption records indexed by MPAN and timestamp
- **Validations**: Value range checks, timestamp sequence checks, duplicate detection, meter registration verification

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: DCC technical interface agreement, DCC UIT environment access

---

#### FR-2: Consumer Registration and Authentication

**Description**: The system must allow householders to register, verify their identity, and link their smart meter(s) to their account.

**Relates To**: BR-2

**Acceptance Criteria**:
- [ ] Given a householder, when they register, then they can verify their identity using GOV.UK One Login
- [ ] Given a verified identity, when the householder enters their MPAN, then the system validates ownership via the ECOES (Electricity Central Online Enquiry Service) database
- [ ] Given a validated MPAN, when linked to the account, then the householder can view their consumption data within 5 minutes

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-3: Consumer Energy Dashboard

**Description**: The system must provide an interactive web dashboard showing householders their energy consumption in understandable formats.

**Relates To**: BR-2

**Acceptance Criteria**:
- [ ] Given a registered consumer, when they view the dashboard, then they see daily, weekly, and monthly consumption in kWh and estimated cost (£)
- [ ] Given consumption data, when displayed, then comparisons are shown against similar households (size, region, property type)
- [ ] Given seasonal patterns, when the consumer views trends, then energy-saving recommendations are displayed based on their consumption profile
- [ ] Given a tariff rate input, when the consumer enters their tariff, then cost projections are calculated and displayed

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-4: Consent Management

**Description**: The system must implement the DCC consent framework, allowing consumers to grant, modify, and revoke consent for data access at different granularity levels.

**Relates To**: BR-4

**Acceptance Criteria**:
- [ ] Given a registered consumer, when they visit privacy settings, then they see current consent status for all data access parties
- [ ] Given a consent request, when the consumer grants consent, then the decision is recorded with timestamp, scope (monthly/daily/half-hourly), and purpose
- [ ] Given an existing consent, when the consumer revokes consent, then data access is terminated within 24 hours
- [ ] Given a third-party data request, when no valid consent exists, then the request is rejected with appropriate error code

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-5: Anonymised Analytics Platform

**Description**: The system must provide DESNZ, Ofgem, and National Grid ESO analysts with access to anonymised, aggregated energy consumption data through dashboards and data export.

**Relates To**: BR-3

**Acceptance Criteria**:
- [ ] Given national meter data, when an analyst queries consumption by region, then aggregated data is returned with a minimum group size of 10 meters (k-anonymity)
- [ ] Given time-series data, when an analyst requests trends, then data is available within 24 hours of collection
- [ ] Given an analytics query, when executed, then results can be exported in CSV, JSON, or Parquet format
- [ ] Given aggregated data, when displayed, then no individual household can be re-identified

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-6: Third-Party API

**Description**: The system must provide a RESTful API for authorised third parties to access consumer energy data (with consent) and anonymised aggregates.

**Relates To**: BR-5

**Acceptance Criteria**:
- [ ] Given an authorised third party, when they request consumer data, then consent is verified before data is returned
- [ ] Given a valid API request, when processed, then response time is under 500ms for single-meter queries
- [ ] Given an API consumer, when they access the API, then all requests are logged with organisation ID, endpoint, timestamp, and data scope

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Data Ingestion Throughput

**Requirement**: The system must sustain ingestion of 2.5 billion meter readings per day (approximately 29,000 readings per second average, 150,000 per second peak).

**Load Conditions**:
- Sustained: 53 million meters x 48 half-hourly readings/day = 2.544 billion readings/day
- Peak: 5x sustained rate during catch-up after DCC maintenance windows
- Data volume: Approximately 500 GB raw data per day

**Priority**: CRITICAL

---

#### NFR-P-2: Consumer Portal Response Time

**Requirement**: Consumer-facing web pages must load within 2 seconds (p95) and API responses within 200ms (p95).

**Measurement Method**: Real User Monitoring (RUM) and synthetic monitoring from UK geographic regions.

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Platform Availability

**Requirement**: The data ingestion pipeline must achieve 99.95% uptime (4.4 hours maximum unplanned downtime per year). The consumer portal must achieve 99.9% uptime.

**Maintenance Windows**: Planned maintenance between 02:00-06:00 UTC, with DCC coordination to avoid coinciding with DCC maintenance windows.

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: 1 hour for consumption data; 0 for consumer consent records (no data loss acceptable)
**RTO**: 15 minutes for ingestion pipeline; 1 hour for consumer portal

**Backup Requirements**:
- Continuous replication for consent and account data
- Hourly incremental backup for consumption data
- Geographic backup to secondary UK data centre

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: Consumer authentication via GOV.UK One Login (OpenID Connect). Government analyst authentication via departmental SSO. Third-party API authentication via OAuth 2.0 client credentials with mTLS.

**Session Management**:
- Consumer session timeout: 30 minutes inactivity
- Analyst session timeout: 60 minutes inactivity
- API tokens: 1 hour expiry with refresh

**Priority**: CRITICAL

---

#### NFR-SEC-2: Encryption

**Requirement**:
- Data in transit: TLS 1.3 for all connections; mTLS for DCC and third-party API interfaces
- Data at rest: AES-256 encryption for all data stores containing personal energy data
- Field-level encryption for MPAN-to-identity mapping

**Priority**: CRITICAL

---

#### NFR-SEC-3: NIS Regulations Compliance

**Requirement**: The platform must comply with NIS Regulations 2018 as an operator of essential services, including incident reporting within 72 hours, annual security audit, and cyber security risk management framework.

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: UK GDPR and Data Protection Act 2018

**Requirement**: Full compliance with UK GDPR including data subject rights (access, rectification, erasure, portability), lawful basis for processing (public task for government analytics, consent for consumer features), and Data Protection Impact Assessment.

**Data Residency**: All personal data must reside within UK sovereign data centres.

**Priority**: CRITICAL

---

#### NFR-C-2: Smart Energy Code Compliance

**Requirement**: Data access and consent management must comply with the Smart Energy Code (SEC) Section H (Data Access), including DCC consent framework integration and permitted data access levels.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all consumer-facing interfaces. Energy data visualisations must have text alternatives and must not rely solely on colour.

**Additional Requirements**:
- Welsh language support for the consumer portal
- Plain English energy terminology with contextual help
- Support for screen readers and keyboard-only navigation

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: DCC Smart Meter Interface

**Purpose**: Primary data source — receive half-hourly consumption readings from 53 million smart meters via the DCC infrastructure.

**Integration Type**: Real-time data feed via DCC User Interface Specification (DUIS)

**Data Exchanged**:
- **From DCC to Platform**: Half-hourly consumption readings (kWh), meter status, alerts, firmware versions
- **From Platform to DCC**: Consent management requests, on-demand read requests

**Authentication**: DCC PKI infrastructure with mutual certificate authentication

**SLA**: 99.95% availability of DCC interface; readings available within 4 hours of collection

**Priority**: CRITICAL

---

### INT-2: GOV.UK One Login

**Purpose**: Consumer identity verification and authentication.

**Integration Type**: OpenID Connect (OIDC) federation

**Data Exchanged**:
- **From One Login to Platform**: Verified identity claims (name, verified identity level)
- **From Platform to One Login**: Authentication requests

**Priority**: MUST_HAVE

---

### INT-3: ECOES (Electricity Central Online Enquiry Service)

**Purpose**: Verify consumer ownership of MPAN (meter point) for account linking.

**Integration Type**: RESTful API query

**Data Exchanged**:
- **From Platform to ECOES**: MPAN lookup request with consumer address
- **From ECOES to Platform**: MPAN ownership confirmation

**Priority**: MUST_HAVE

---

### INT-4: National Grid ESO Data Feed

**Purpose**: Provide aggregated demand data for grid balancing and demand forecasting.

**Integration Type**: Event-driven data feed (aggregated, anonymised)

**Data Exchanged**:
- **From Platform to ESO**: Aggregated consumption by Grid Supply Point (GSP), half-hourly resolution, 4-hour latency

**Priority**: SHOULD_HAVE

---

### INT-5: Ofgem Regulatory Reporting

**Purpose**: Provide market monitoring data to Ofgem for regulatory purposes.

**Integration Type**: Scheduled batch data export

**Data Exchanged**:
- **From Platform to Ofgem**: Anonymised market-level consumption statistics, supplier performance metrics

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Meter Reading

**Description**: Individual half-hourly consumption reading from a smart meter.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| reading_id | UUID | Yes | Unique reading identifier | Primary key |
| mpan | String(13) | Yes | Meter Point Administration Number | Indexed, validated format |
| reading_timestamp | Timestamp | Yes | UTC timestamp of reading period start | Indexed, half-hourly intervals |
| consumption_kwh | Decimal(10,3) | Yes | Consumption in kWh for the period | >= 0, range validated |
| register_type | Enum | Yes | Import/Export, Economy7 registers | Validated against meter registration |
| data_source | Enum | Yes | DCC, Supplier, Estimated | Audit field |
| received_timestamp | Timestamp | Yes | When the reading was received by platform | Indexed |
| validation_status | Enum | Yes | Valid, Suspect, Failed | Indexed |

**Data Volume**: 2.5 billion records/day; approximately 900 billion records/year

**Data Classification**: OFFICIAL-SENSITIVE (individual readings linked to MPAN)

**Data Retention**: 13 months detailed, then aggregated to daily; aggregates retained for 10 years

---

#### Entity 2: Consumer Account

**Description**: Registered householder account linked to one or more smart meters.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| account_id | UUID | Yes | Unique account identifier | Primary key |
| one_login_subject | String(256) | Yes | GOV.UK One Login subject identifier | Unique, indexed |
| created_at | Timestamp | Yes | Account creation timestamp | Indexed |
| consent_status | JSON | Yes | Current consent grants by purpose | Versioned |
| linked_mpans | Array[String(13)] | Yes | Associated meter points | Validated via ECOES |

**Data Volume**: Target 10 million accounts within 24 months

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: Account data retained while active; deleted 12 months after account closure

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: DCC interface operates via the DCC User Interface Specification (DUIS) — the platform must implement this protocol; alternative data collection routes are not available for government users.

**TC-2**: SMETS1 meters enrolled with DCC use adapter firmware with limited functionality compared to SMETS2 — some data fields may not be available for all meters.

**TC-3**: All data must be hosted within UK sovereign cloud infrastructure (AWS London, Azure UK South, or equivalent).

### Assumptions

**A-1**: The Energy Act 2023 provides sufficient legal basis for DESNZ to access smart meter data via the DCC for the stated purposes. If challenged, an alternative legal basis must be established.

**A-2**: DCC WAN capacity is sufficient to support additional government data feeds alongside existing supplier data flows. If capacity is constrained, a phased rollout will be necessary.

**A-3**: GOV.UK One Login will be production-ready and available for integration at the time of consumer portal launch.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Data completeness | N/A (no platform) | 99.5% of expected readings | 12 months post-launch | Ingestion pipeline monitoring |
| Registered consumers | 0 | 10 million | 24 months post-launch | Platform analytics |
| Consumer satisfaction | N/A | 4.0/5.0 | Ongoing | In-service surveys |
| Policy analytics products | 0 | 5 core datasets | 18 months post-launch | Product delivery tracking |
| Privacy incidents | N/A | 0 reportable | Ongoing | ICO incident register |

---

## Dependencies and Risks

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | DCC interface capacity insufficient for government data feeds | MEDIUM | HIGH | Early capacity assessment, phased rollout | Technical Architect |
| R-2 | Consumer privacy incident damages trust and adoption | LOW | CRITICAL | Privacy-by-design, pen testing, consent framework | DESNZ DPO |
| R-3 | Energy supplier legal challenge to data sharing | LOW | HIGH | Legal basis validation, Ofgem regulatory backing | DESNZ Legal |
| R-4 | GOV.UK One Login not ready for integration | MEDIUM | MEDIUM | Alternative authentication fallback, early integration testing | Technical Architect |
| R-5 | Data volumes exceed infrastructure cost projections | MEDIUM | MEDIUM | Cloud auto-scaling, data lifecycle management, cost monitoring | Platform Engineer |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | This programme | Stakeholder drivers and goals | `projects/001-smart-meter-data-platform/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 7 Programme | Governing principles | `projects/000-global/` |
| DCC User Interface Specification | Technical | DCC | Interface protocol for meter data | N/A — external reference |
| Smart Energy Code Section H | Regulatory | SEC Company | Data access framework | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart Meter Data Platform (Project 001)
**Model**: Claude Opus 4.6 (1M context)
