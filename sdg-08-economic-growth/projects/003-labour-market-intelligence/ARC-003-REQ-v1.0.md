# Project Requirements: Labour Market Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Labour Market Intelligence (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Head of Labour Market Statistics, ONS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | LMI Programme Board, ONS Digital, UKSA, DWP Analytics, DfE Skills Analysis |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Real-time Labour Market Intelligence platform, which will aggregate, process, and publish labour market data from administrative, survey, and novel data sources to produce near-real-time analytics and skills gap forecasting.

---

## Executive Summary

### Business Context

The UK's primary labour market data source — the Labour Force Survey (LFS) — has suffered declining response rates, leading to its downgrade from National Statistics to Experimental Statistics by the UK Statistics Authority. Meanwhile, policy departments (HM Treasury, DWP, DfE, DBT) need faster, more granular labour market data for decisions on skills investment, regional growth, and economic intervention. The LMI platform will fuse administrative data (HMRC RTI, DWP UC), survey data (transformed LFS), and novel data sources (online job postings, vacancy APIs) into a near-real-time analytical platform.

### Objectives

- Deliver weekly experimental labour market indicators with 5-day latency (vs. current 6-week lag)
- Provide local authority-level labour market data for 315 areas in England
- Establish skills gap forecasting using predictive analytics on vacancy and training data
- Support the ONS Integrated Data Service (IDS) for approved researcher access
- Feed labour market context into the Job Matching Platform (Project 001)

### Expected Outcomes

- Policy decisions informed by data that is weeks, not months, old
- Local authorities able to target skills investment based on local labour market evidence
- Skills gap forecasts enabling proactive rather than reactive workforce planning
- Restored confidence in UK labour market statistics

### Project Scope

**In Scope**:
- Real-time data ingestion pipeline for HMRC RTI, DWP UC, vacancy data
- Statistical processing and quality assurance engine
- Skills gap forecasting model
- Publication platform (dashboards, API, downloadable datasets)
- Secure research data access via ONS SRS
- Integration with NOMIS for dissemination

**Out of Scope**:
- Labour Force Survey transformation (separate ONS programme, but this platform consumes its outputs)
- Economic forecasting (OBR remit)
- Individual employer analysis (statistical aggregation only)

---

## Business Requirements

### BR-001: Near-Real-Time Labour Market Indicators

**Description**: The platform must produce and publish weekly experimental labour market indicators (employment rate, vacancy count, median earnings by sector and region) derived from administrative data, with defined quality measures and statistical caveats.

**Rationale**: The 6-week lag in current LFS-based statistics means policy decisions are based on an outdated picture. HMRC RTI data arrives daily and can produce near-real-time employment indicators. The ONS already publishes experimental RTI-based statistics — this platform will operationalise and enhance them.

**Success Criteria**:
- Weekly indicators published within 5 working days of reference period
- At least 10 indicators covering employment, earnings, and vacancies
- Quality measures (confidence intervals, coherence metrics) published alongside each indicator
- UKSA assessment of suitability for weekly publication obtained

**Priority**: MUST_HAVE

---

### BR-002: Local Authority-Level Granularity

**Description**: The platform must deliver labour market indicators at local authority level (315 areas in England, with devolved administrations data where available) with sufficient statistical robustness for local economic planning.

**Rationale**: National averages mask enormous regional variation. The employment rate in Hart (Hampshire) is 87%, while in Blackpool it is 69%. DWP work coaches, Local Enterprise Partnerships, and Combined Authorities need local data to allocate resources and design interventions. The Levelling Up White Paper requires granular data to measure progress.

**Success Criteria**:
- Indicators published for 95% of local authority areas (some may be suppressed for disclosure control)
- Confidence intervals within +/- 2 percentage points for local authority estimates
- Quarterly publication cycle for local data (monthly if sample/administrative coverage permits)

**Priority**: MUST_HAVE

---

### BR-003: Skills Gap Forecasting

**Description**: The platform must produce forward-looking skills gap forecasts by sector and region, identifying emerging skills shortages and declining skills demand to inform DfE skills investment and employer training decisions.

**Rationale**: Current skills planning is reactive — by the time a shortage is identified through employer surveys, it has been building for 2-3 years. Predictive analytics using vacancy data, training enrolment data, and demographic trends can provide 12-24 month forward visibility.

**Success Criteria**:
- Quarterly skills gap forecast published for top 25 SOC occupation groups
- Forecast accuracy validated against actual outcomes (target: +/- 10% at 12 months)
- Regional disaggregation for 9 English regions plus Scotland, Wales, NI

**Priority**: SHOULD_HAVE

---

### BR-004: Statistical Disclosure Control

**Description**: All published data must comply with ONS statistical disclosure control policies, preventing identification of individual persons or businesses in published statistics.

**Rationale**: The platform uses individual-level administrative data (RTI, UC). Statistical outputs must be aggregated and perturbed to prevent identification. HMRC's data sharing agreement requires strict disclosure control as a condition of access.

**Success Criteria**:
- Automated SDC applied to all outputs before publication
- No output cell with fewer than 10 observations published without perturbation
- HMRC satisfied that RTI data is adequately protected in published outputs

**Priority**: MUST_HAVE

---

### BR-005: Code of Practice Compliance

**Description**: All statistical outputs must comply with the UK Statistics Authority Code of Practice for Statistics, including trustworthiness, quality, and value pillars.

**Rationale**: ONS has a statutory duty to comply with the Code. The platform's outputs will be assessed by the Office for Statistics Regulation (OSR) for designation as Official Statistics or National Statistics.

**Success Criteria**:
- OSR assessment completed for core indicators
- Pre-release access protocols documented and enforced
- Methodology notes published for all indicators
- Quality and Methodology Information (QMI) documents published

**Priority**: MUST_HAVE

---

## Functional Requirements

### FR-001: Data Ingestion Pipeline

**Description**: The system must ingest data from multiple sources with automated quality checks, deduplication, and linkage.

**Acceptance Criteria**:
- [ ] Given HMRC RTI data, when a daily batch arrives, then it is ingested, validated, and available for processing within 4 hours
- [ ] Given DWP UC administrative data, when a weekly extract arrives, then it is linked to RTI data via pseudonymised key
- [ ] Given online vacancy data (Indeed, LinkedIn, Reed feeds), when scraped/received, then vacancies are deduplicated and classified by SOC code
- [ ] Given a data quality failure, when validation rules detect anomalies, then the batch is quarantined and an alert is raised

**Priority**: MUST_HAVE

---

### FR-002: Statistical Processing Engine

**Description**: The system must apply seasonal adjustment, weighting, imputation, and statistical disclosure control to produce publication-ready indicators.

**Acceptance Criteria**:
- [ ] Given raw administrative data, when statistical processing runs, then seasonal adjustment (X-13ARIMA-SEATS) is applied to time series
- [ ] Given small area estimates, when SDC is applied, then no output cell risks individual identification
- [ ] Given a new reference period, when processing completes, then all indicators are produced within 3 working days

**Priority**: MUST_HAVE

---

### FR-003: Skills Gap Forecasting Model

**Description**: The system must use machine learning to forecast skills demand and supply by occupation and region.

**Acceptance Criteria**:
- [ ] Given historical vacancy data, qualification completions, and demographic data, when the model runs, then 12-month skills gap forecasts are produced by SOC group and region
- [ ] Given forecast outputs, when validated against actual outcomes, then accuracy is within +/- 10% for national estimates
- [ ] Given a skills gap forecast, when published, then methodology and model confidence intervals are included

**Priority**: SHOULD_HAVE

---

### FR-004: Publication Platform

**Description**: The system must publish indicators via interactive dashboards, API, and downloadable datasets.

**Acceptance Criteria**:
- [ ] Given publication day, when indicators are released, then dashboards update automatically at the pre-announced time
- [ ] Given a policy analyst, when they access the API, then they can query indicators by region, sector, time period, and occupation
- [ ] Given a researcher, when they download data, then CSV and JSON formats are available with full metadata

**Priority**: MUST_HAVE

---

### FR-005: Secure Research Data Access

**Description**: The system must provide approved researchers with access to linked microdata via the ONS Secure Research Service (SRS) under the Five Safes framework.

**Acceptance Criteria**:
- [ ] Given an approved researcher, when they request access, then a linked analytical dataset is available within 20 working days
- [ ] Given the SRS environment, when a researcher runs analysis, then no data can be exported without output checking

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### NFR-P-001: Data Processing Throughput

**Requirement**: Ingest and process 50 million RTI records daily within a 4-hour overnight processing window.

**Priority**: MUST_HAVE

---

### NFR-P-002: Dashboard Performance

**Requirement**: Dashboard page load time < 3 seconds at p95, including complex visualisations with 315 local authority areas.

**Priority**: MUST_HAVE

---

### NFR-SEC-001: Data Classification

**Requirement**: All individual-level administrative data classified OFFICIAL-SENSITIVE. Published aggregated statistics classified OFFICIAL. Secure research environment classified OFFICIAL-SENSITIVE with enhanced controls.

**Priority**: MUST_HAVE

---

### NFR-SEC-002: Pre-Release Access Control

**Requirement**: Pre-release access to unpublished statistics must be limited, time-boxed (maximum 24 hours before publication), and logged, in accordance with the Pre-release Access to Official Statistics Order 2008.

**Priority**: MUST_HAVE

---

### NFR-A-001: Platform Availability

**Requirement**: Publication platform: 99.5% availability. Data processing pipeline: 99.0% (batch processing with retry). API: 99.9% availability.

**Priority**: MUST_HAVE

---

### NFR-C-001: Statistics Authority Code of Practice

**Requirement**: Full compliance with the Code of Practice for Statistics including: transparent methodology; clear presentation and communication; orderly, pre-announced release; trustworthy production; quality assurance throughout.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: HMRC Real Time Information (RTI)

**Purpose**: Primary administrative data source for employment and earnings
**Integration Type**: Daily batch file transfer via secure gateway
**Data Exchanged**: Pseudonymised employment records (employer, employee, earnings, start/end dates)
**Authentication**: HMRC secure data sharing gateway with dual-key access
**Priority**: MUST_HAVE

---

### INT-002: DWP Universal Credit Administrative Data

**Purpose**: Benefit claimant data for labour market analysis
**Integration Type**: Weekly batch extract
**Data Exchanged**: Pseudonymised claimant records (conditionality group, claim duration, age band, region)
**Priority**: MUST_HAVE

---

### INT-003: Online Vacancy Data (Indeed, LinkedIn, Reed)

**Purpose**: Near-real-time vacancy demand indicators
**Integration Type**: Daily API feeds and web scraping
**Data Exchanged**: Vacancy metadata (title, sector, location, salary, skills required)
**Priority**: SHOULD_HAVE

---

### INT-004: Job Matching Platform (Project 001)

**Purpose**: Provide labour market context for AI matching recommendations
**Integration Type**: Real-time API
**Data Exchanged**: Local labour market indicators (vacancy rates, sector growth, skills demand)
**Priority**: SHOULD_HAVE

---

### INT-005: NOMIS

**Purpose**: Dissemination of local area statistics
**Integration Type**: Data feed for NOMIS publication
**Data Exchanged**: Published indicators for local authority areas
**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy within ONS secure data environment (ONS cloud platform or approved equivalent)
**TC-2**: RTI data cannot leave the ONS/HMRC secure perimeter
**TC-3**: All statistical processing must be reproducible (version-controlled code and data)

### Business Constraints

**BC-1**: Budget capped at GBP 12M over 3 years
**BC-2**: UKSA must approve methodology before designating outputs as Official Statistics
**BC-3**: HMRC data sharing agreement renewal required annually

### Assumptions

**A-1**: HMRC will continue to share RTI data under existing legal gateway
**A-2**: Online vacancy data providers will offer API access (commercial terms to be negotiated)
**A-3**: Transformed LFS will produce data compatible with the platform's schema by 2027

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-003-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals | `projects/003-labour-market-intelligence/ARC-003-STKE-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 4, 11, 12, 13 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Code of Practice for Statistics | Standard | UKSA | Statistical standards | https://code.statisticsauthority.gov.uk/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Labour Market Intelligence
**Model**: Claude Opus 4.6
