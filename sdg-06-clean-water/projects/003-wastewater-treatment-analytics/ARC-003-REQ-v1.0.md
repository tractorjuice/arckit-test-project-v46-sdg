# Project Requirements: Wastewater Treatment Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Wastewater Treatment Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Wastewater Treatment Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Ofwat, Environment Agency, DEFRA, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Wastewater Treatment Analytics platform. The platform provides Ofwat with independent performance analytics for sewage treatment across the 11 water and sewerage companies in England and Wales, replacing the current self-reported annual performance reporting model.

---

## Executive Summary

### Business Context

The UK water industry faces a crisis of public trust. Water companies self-report performance data through Annual Performance Reports (APRs) that take 6 months to assure and are frequently challenged by environmental groups and media. Ofwat, as the economic regulator, needs independent, timely, and auditable performance data to support price review determinations (PR29) and enforcement actions. The Environment Act 2021 introduced legally binding storm overflow discharge reduction targets that require robust, continuous monitoring analytics.

Ofwat currently lacks the analytical platform to independently verify water company performance claims, compare companies on a normalised basis, or track compliance with Environment Act targets in real time. This platform will transform wastewater regulation from retrospective self-reporting to proactive, evidence-based oversight.

### Objectives

- Automate comparative performance assessment, reducing the assurance cycle from 6 months to 6 weeks
- Provide real-time storm overflow discharge tracking for all 15,000+ overflows
- Deliver standardised, normalised performance metrics enabling fair cross-company comparison
- Track compliance with Environment Act 2021 storm overflow reduction targets
- Publish performance data transparently for public accountability

### Expected Outcomes

- 60% reduction in industry assurance costs (GBP 24M annual saving)
- Real-time regulatory intelligence replacing retrospective annual reporting
- Evidence base for PR29 price review determinations
- Public trust improvement through independent, transparent performance data

### Project Scope

**In Scope**:
- Ingestion of water company operational telemetry (treatment works, storm overflows, sewer network)
- Standardised performance metric calculations (pollution incidents, compliance, overflow frequency)
- Comparative performance assessment with contextual normalisation
- Storm overflow discharge tracking and Environment Act target compliance
- Regulatory reporting automation (APR validation, Ofwat submissions)
- Public-facing performance dashboard
- Integration with EA enforcement data

**Out of Scope**:
- Water company internal SCADA system upgrades
- Drinking water quality analytics (DWI remit)
- Water resource planning analytics (Project 004)
- Raw water quality monitoring (Project 001)

---

## Business Requirements

### BR-001: Independent Comparative Performance Assessment

**Description**: Enable Ofwat to independently calculate and compare sewage treatment performance metrics across all 11 water and sewerage companies using standardised methodology applied to operational telemetry data.

**Rationale**: Current reliance on company self-reported data creates perverse incentives, inconsistent methodology application, and a 6-month assurance lag. Independent analytics strengthen regulatory credibility and enable faster intervention when performance deteriorates.

**Success Criteria**:
- All 11 companies' performance independently calculated
- Methodology consistency verified through automated validation
- Assurance cycle reduced from 6 months to 6 weeks
- Performance metrics available within 30 days of reporting period end

**Priority**: MUST_HAVE
**Stakeholder**: Ofwat CEO (SD-1)

---

### BR-002: Storm Overflow Compliance Tracking

**Description**: Track progress against Storm Overflow Discharge Reduction Plan targets at individual overflow level, providing automated progress reporting for Ministerial and Parliamentary use.

**Rationale**: The Environment Act 2021 and Storm Overflow Discharge Reduction Plan set legally binding targets. DEFRA faces judicial review risk if compliance cannot be demonstrated with auditable evidence.

**Success Criteria**:
- All 15,000+ overflows tracked against individual reduction targets
- Automated progress reports available on demand
- Historical trend analysis enabling trajectory projection
- Auditable methodology withstanding legal challenge

**Priority**: MUST_HAVE
**Stakeholder**: DEFRA Policy Director (SD-3)

---

### BR-003: Public Performance Transparency

**Description**: Publish water company sewage treatment performance data through a public dashboard, enabling citizens and consumer groups to scrutinise company performance and understand whether bill increases are delivering environmental improvement.

**Rationale**: 67% of water customers do not believe companies are doing enough. Independent, public performance data rebuilds trust and creates accountability pressure.

**Success Criteria**:
- All performance metrics published within 48 hours of calculation
- Dashboard accessible and understandable to non-expert users
- Both headline comparisons and normalised context available
- Public satisfaction > 65% in user research

**Priority**: SHOULD_HAVE
**Stakeholder**: Public/CCW (SD-4)

---

## Functional Requirements

### FR-001: Water Company Telemetry Ingestion

**Description**: Ingest operational telemetry data from 11 water and sewerage companies including treatment works performance, storm overflow EDMs, and sewer network monitors.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given a water company submits telemetry data via the standardised API, when validation passes, then data is ingested within the SLA
- [ ] Given data fails validation, then a detailed rejection report is returned to the company within 1 hour
- [ ] Given a company's data feed is interrupted for >4 hours, then Ofwat enforcement team is automatically notified
- [ ] Given telemetry data is ingested, then it is immutably stored with timestamp and source metadata for audit purposes

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-002: Standardised Performance Metric Calculation

**Description**: Calculate standardised performance metrics using Ofwat-defined methodology applied consistently across all companies. Metrics include: pollution incidents (categories 1-4), treatment works numeric permit compliance, storm overflow frequency and duration, and sewer flooding incidents.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given telemetry data for a reporting period, when the calculation engine runs, then all defined performance metrics are calculated per company
- [ ] Given the same input data, when the calculation is run multiple times, then results are identical (deterministic)
- [ ] Given methodology parameters are updated, then calculations can be re-run under both old and new methodology for comparison
- [ ] Given a metric result differs by >10% from the company's self-reported value, then an anomaly flag is raised for Ofwat review

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-003: Contextual Normalisation Engine

**Description**: Apply contextual normalisation to performance metrics accounting for infrastructure age, catchment characteristics, population density, rainfall, and network length — enabling fair cross-company comparison.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:
- [ ] Given raw performance metrics, when normalisation is applied, then normalised metrics per 1000km of sewer, per 10,000 connected properties, and rainfall-adjusted are calculated
- [ ] Given normalisation factors (sewer length, connected properties, rainfall) are updated, then normalised metrics are recalculated automatically
- [ ] Given both raw and normalised metrics are available, then users can toggle between views

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-004: Storm Overflow Discharge Dashboard

**Description**: Real-time public dashboard showing storm overflow discharge status for all 15,000+ overflows, with duration, frequency, receiving water body, and permit context.

**Relates To**: BR-002, BR-003

**Acceptance Criteria**:
- [ ] Given an overflow is actively discharging, then the dashboard shows real-time status with duration counter
- [ ] Given a user selects an overflow, then permit conditions, discharge history, and receiving water body status are displayed
- [ ] Given a user selects a water company, then aggregate statistics (total overflows, total spill hours, year-on-year trend) are displayed
- [ ] Given the dashboard is accessed on a mobile device, then it renders responsively with core functionality preserved

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-005: Environment Act Target Tracker

**Description**: Automated tracking of water company progress against Storm Overflow Discharge Reduction Plan targets at individual overflow and company level, with projection modelling.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a reporting period closes, when the tracker updates, then each overflow's status against its reduction target is calculated
- [ ] Given current performance trajectories, when the projection model runs, then estimated target achievement dates are calculated
- [ ] Given a company is projected to miss a legally binding target, then an automated alert is sent to Ofwat enforcement and DEFRA policy teams

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-006: Regulatory Reporting Automation

**Description**: Auto-generate Ofwat regulatory submissions (Annual Performance Report validation, periodic returns) from platform-calculated metrics, replacing manual company compilation.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given a reporting period closes, when the report generator runs, then APR-format reports are generated for each company
- [ ] Given a generated report is reviewed, then an Ofwat officer can approve, reject, or query specific metrics
- [ ] Given approval is granted, then the report is published on the Ofwat website in the standard format

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Telemetry Ingestion Latency

**Requirement**: End-to-end latency from water company data submission to platform availability:
- Storm overflow EDM data: < 1 hour
- Treatment works compliance data: < 4 hours
- Sewer network monitoring: < 4 hours

**Load Conditions**:
- Normal: ~50,000 data points per hour from 11 companies
- Peak (storm event): ~500,000 data points per hour

**Priority**: HIGH

---

#### NFR-P-2: Calculation Engine Performance

**Requirement**: Full comparative performance calculation across all 11 companies for a quarterly reporting period completed within 4 hours, enabling 6-week assurance cycle target.

**Priority**: HIGH

---

### Availability and Resilience

#### NFR-A-1: Platform Availability

**Requirement**:
- Telemetry ingestion: 99.9% availability
- Regulatory calculation engine: 99.5% (less time-critical, batch processing)
- Public dashboard: 99.9% availability
- Data must never be lost — append-only immutable storage

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Regulatory Data Isolation

**Requirement**: Strict data isolation between:
- Water company pre-publication data (company-specific access only)
- Ofwat regulatory analysis workspace (Ofwat staff only)
- Published performance data (public access)
- Enforcement investigation data (Ofwat enforcement + EA only)

Water companies MUST NOT be able to see other companies' pre-publication data. Ofwat enforcement team data MUST be isolated from general Ofwat staff where investigations are ongoing.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Audit Trail and Evidence Integrity

**Requirement**: Complete, immutable audit trail for all data from ingestion to published metric. Must support regulatory and legal proceedings:
- Every data point traceable to source submission with timestamp
- Every calculation reproducible from stored inputs and versioned methodology
- Audit log tamper-evident (cryptographic chaining)

**Priority**: CRITICAL

---

## Integration Requirements

### INT-001: Water Company SCADA/Telemetry APIs

**Purpose**: Ingest operational telemetry from 11 water and sewerage companies' SCADA and monitoring systems.

**Integration Type**: Company pushes data to platform via standardised REST API

**Data Exchanged**:
- **Companies to Platform**: Treatment works flow/quality data, EDM status, sewer level/flow data, pump station data

**Authentication**: OAuth 2.0 with company-specific client credentials, IP allowlisting
**SLA**: Data submitted within 4 hours of operational reading, API availability 99.9%
**Priority**: CRITICAL

---

### INT-002: Environment Agency Enforcement Data

**Purpose**: Integrate EA pollution incident and enforcement data to correlate with treatment performance.

**Integration Type**: Batch API (daily) + event-driven alerts for new incidents

**Data Exchanged**:
- **EA to Platform**: Pollution incident reports (category, location, cause, responsible company), enforcement actions, prosecution outcomes

**Priority**: HIGH

---

### INT-003: Ofwat PR29 Data Pipeline

**Purpose**: Feed calculated performance metrics into Ofwat's price review analytical framework.

**Integration Type**: Batch export (quarterly)

**Data Exchanged**:
- **Platform to Ofwat PR29**: Normalised performance metrics, trend data, company comparisons, confidence intervals

**Priority**: HIGH

---

## Data Requirements

### Data Entities

#### Entity: Treatment Works Performance Record

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| record_id | UUID | Yes | Unique record identifier | Primary key |
| works_id | String(20) | Yes | Treatment works identifier | FK to Works register |
| company_id | String(10) | Yes | Water company identifier | FK to Company |
| period_start | Date | Yes | Reporting period start | Not null |
| period_end | Date | Yes | Reporting period end | After start |
| parameter | String(50) | Yes | Measured parameter | Controlled vocabulary |
| permit_limit | Decimal | Yes | Numeric permit limit | Not null |
| measured_value | Decimal | Yes | Measured/calculated value | Not null |
| compliance_status | Enum | Yes | Pass/fail against permit | ['compliant','non_compliant','under_review'] |
| source | Enum | Yes | Data source | ['telemetry','manual_sample','company_reported'] |
| quality_flag | Enum | Yes | Data quality status | ['validated','provisional','suspect'] |

**Data Volume**: ~10 million records per year
**Data Classification**: OFFICIAL (pre-publication: OFFICIAL-SENSITIVE)
**Data Retention**: Indefinite (regulatory records spanning multiple price review periods)

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Water company SCADA systems are heterogeneous (different vendors, protocols, data formats). Platform must define a standardised API — protocol translation is the company's responsibility.

**TC-2**: Ofwat's existing analytical tools (Excel-based models, SAS) must be progressively replaced, not immediately deprecated. Parallel running required for minimum 2 years.

### Business Constraints

**BC-1**: Platform must be operational for PR29 data collection beginning 2028.

**BC-2**: Programme budget capped at GBP 12M over 3 years.

**BC-3**: Methodology must be legally defensible — all calculation approaches subject to formal consultation with the water industry before adoption.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Assurance cycle duration | 6 months | 6 weeks | 2028 |
| Industry assurance cost | GBP 40M/year | GBP 16M/year | 2028 |
| Storm overflows tracked | 0 (platform) | 15,000+ | Dec 2027 |
| Data anomalies detected | Ad-hoc | Automated real-time | 2027 |
| Public dashboard availability | N/A | 99.9% | Launch |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Stakeholder Analysis | Architecture | ARC-003-STKE-v1.0 | Stakeholder drivers and goals | `projects/003-wastewater-treatment-analytics/ARC-003-STKE-v1.0.md` |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | Governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Water Industry Act 1991 | Legislation | legislation.gov.uk | Ofwat regulatory powers | N/A — external reference |
| Environment Act 2021 | Legislation | legislation.gov.uk | Storm overflow duties | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wastewater Treatment Analytics (Project 003)
**AI Model**: Claude Opus 4.6 (1M context)
