# Project Requirements: SDG Progress Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | SDG Progress Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SDG Progress Dashboard Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | ONS SDG Team, UKSA, Cabinet Office SDG Unit, CDDO, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the ONS SDG Progress Dashboard, which will monitor and report UK progress against the 244 UN SDG indicators, supporting the UK's Voluntary National Review commitments, UNSD reporting obligations, and evidence-based policy making.

---

## Executive Summary

### Business Context

The UK committed to the 2030 Agenda for Sustainable Development and reports progress through Voluntary National Reviews (VNRs) at the UN High-Level Political Forum. Currently, UK SDG data is scattered across 20+ source departments and agencies, approximately 180 of 244 indicators have data, and the VNR data preparation process takes 8 weeks of manual effort. The SDG Progress Dashboard will provide a single, authoritative, publicly accessible platform for UK SDG monitoring.

### Objectives

- Cover 200+ of 244 UN SDG indicators with published data and methodology
- Implement SDMX-compliant data exchange with UN Statistics Division
- Launch a public dashboard with open API, meeting WCAG 2.1 AA and GDS standards
- Enable automated VNR data preparation, reducing effort by 70%
- Provide sub-national disaggregation (England, Scotland, Wales, Northern Ireland) for 60%+ of indicators

### Expected Outcomes

- Authoritative UK SDG monitoring platform recognised by UNSD and peer countries
- VNR data preparation time reduced from 8 weeks to < 2 weeks
- 10,000+ monthly unique visitors within 6 months of launch
- Evidence-based SDG policy making through comprehensive indicator data

### Project Scope

**In Scope**:

- All 244 UN SDG indicators (data where UK sources exist; gap analysis where they do not)
- Public-facing dashboard with interactive visualisations
- Open API for programmatic data access
- SDMX data exchange with UNSD
- Sub-national disaggregation where data permits
- Metadata and methodology documentation per indicator
- Integration with Cross-Government Data Sharing Platform (Project 002) for source data

**Out of Scope**:

- Source data collection or survey design (handled by ONS and source departments)
- Policy recommendations or commentary (Cabinet Office responsibility)
- Devolved administration SDG platforms (Scotland, Wales, NI have their own; APIs enable integration)
- Global SDG data for non-UK countries (covered by UNSD Global SDG Database)

---

## Business Requirements

### BR-1: Comprehensive SDG Indicator Coverage

**Description**: Cover 200+ of 244 UN SDG indicators with published data, methodology documentation, and data quality assessment.

**Rationale**: The UK's credibility in SDG reporting depends on comprehensive coverage. Gaps must be identified and documented, not hidden.

**Success Criteria**:

- 200+ indicators with published data
- 100% of Tier 1 indicators covered (internationally established methodology)
- 90% of Tier 2 indicators covered
- Gap analysis published for indicators without UK data sources

**Priority**: MUST_HAVE

**Stakeholder**: UKSA/ONS (SD-1), UNSD (SD-3)

---

### BR-2: Statistical Independence Compliance

**Description**: Ensure all dashboard outputs comply with the UKSA Code of Practice for Statistics (Trustworthiness, Quality, Value) and maintain ONS independence from political interference.

**Rationale**: Statistical credibility is the foundation of the dashboard's value. Any perception of political influence would undermine trust domestically and internationally.

**Success Criteria**:

- UKSA Code of Practice compliance verified by UKSA Assessment Team
- Pre-release access controls technically enforced
- Publication pipeline isolated from policy intervention
- All indicators published with methodology and quality information

**Priority**: MUST_HAVE

**Stakeholder**: UKSA (SD-1)

---

### BR-3: SDMX Data Exchange with UNSD

**Description**: Implement automated SDMX-compliant data submission to the UN Statistics Division.

**Rationale**: UNSD collects national SDG data via SDMX for the annual Secretary-General's SDG Progress Report.

**Success Criteria**:

- Automated SDMX submission to UNSD
- 100% metadata completeness for submitted indicators
- Submission within UNSD reporting deadlines (typically May each year)

**Priority**: MUST_HAVE

**Stakeholder**: UNSD (SD-3)

---

### BR-4: Public Dashboard with Open API

**Description**: Provide a publicly accessible dashboard with interactive visualisations and an open API for civil society, researchers, and international audiences.

**Rationale**: Open access supports transparency (SD-5), devolved administration integration (SD-4), and international comparability.

**Success Criteria**:

- Dashboard accessible without authentication
- API providing JSON, CSV, and SDMX formats
- WCAG 2.1 AA accessibility
- GDS Service Standard compliance
- 10,000+ monthly unique visitors within 6 months

**Priority**: MUST_HAVE

**Stakeholder**: Cabinet Office (SD-2), Civil society (SD-5), Devolved administrations (SD-4)

---

### BR-5: VNR Evidence Platform

**Description**: Support UK Voluntary National Review preparation with machine-readable data, trend analysis, and automated report generation.

**Rationale**: Current VNR preparation takes 8 weeks of manual effort. Automation will improve quality and reduce resource demand.

**Success Criteria**:

- VNR data preparation time < 2 weeks
- All VNR indicators sourced from dashboard
- Trend analysis auto-generated with statistical commentary

**Priority**: SHOULD_HAVE

**Stakeholder**: Cabinet Office SDG Unit (SD-2)

---

### BR-6: Sub-National Disaggregation

**Description**: Provide SDG indicator data disaggregated by nation (England, Scotland, Wales, Northern Ireland) where source data permits.

**Rationale**: Devolved administrations have their own SDG strategies and need sub-national data.

**Success Criteria**:

- Sub-national data for 60%+ of indicators
- API supports filtering by nation
- Methodology notes for indicators where sub-national disaggregation is not possible

**Priority**: SHOULD_HAVE

**Stakeholder**: Devolved administrations (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: ONS SDG Analyst

- **Role**: Produces SDG indicator data, writes methodology, manages data quality
- **Goals**: Efficient indicator production workflow, clear publication pipeline
- **Pain Points**: Manual data compilation from 20+ sources, inconsistent formats
- **Technical Proficiency**: High

#### Persona 2: Cabinet Office SDG Policy Officer

- **Role**: Uses SDG data for policy coordination and VNR preparation
- **Goals**: Comprehensive, current data for policy analysis and international reporting
- **Pain Points**: Data scattered across departments, manual VNR compilation
- **Technical Proficiency**: Medium

#### Persona 3: Public/Researcher

- **Role**: Civil society analyst, academic, or citizen interested in UK SDG progress
- **Goals**: Access open, comprehensive SDG data for analysis and accountability
- **Pain Points**: Data hard to find, not machine-readable, methodology unclear
- **Technical Proficiency**: Variable (Low to High)

#### Persona 4: UNSD Correspondent

- **Role**: Receives UK SDG data submissions for global monitoring
- **Goals**: Complete, timely, SDMX-compliant data with full metadata
- **Pain Points**: Late submissions, incomplete metadata, format inconsistencies
- **Technical Proficiency**: High

#### Persona 5: Devolved Administration Analyst

- **Role**: Uses UK SDG data for Scotland/Wales/NI SDG reporting
- **Goals**: Sub-national data, API access, methodology alignment
- **Pain Points**: UK-level data not disaggregated, different methodologies
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: SDG Indicator Data Management

**Description**: The system must support the ingestion, validation, storage, and publication of data for all 244 UN SDG indicators.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given SDG indicator data from a source department, when ingested, then it is validated against the IAEG-SDGs methodology for that indicator
- [ ] Given validated data, when stored, then it includes indicator ID, value, year, disaggregation dimensions, source, and quality assessment
- [ ] Given multiple time series for an indicator, when displayed, then trend analysis (direction, rate of change) is automatically calculated

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Metadata and Methodology Publication

**Description**: The system must publish comprehensive metadata for each indicator including methodology, data source, quality assessment, and comparability notes.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given an indicator, when viewed by a user, then methodology documentation is accessible (data source, calculation method, coverage, limitations)
- [ ] Given an indicator, when metadata is requested via API, then SDMX-compliant metadata is returned
- [ ] Given an indicator with a proxy methodology (different from IAEG-SDGs), then this is clearly flagged with explanation

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-3: Interactive Public Dashboard

**Description**: The system must provide an interactive web-based dashboard with visualisations of UK SDG progress, accessible without authentication.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a public user, when accessing the dashboard, then they can browse all 17 SDGs and drill into individual targets and indicators
- [ ] Given an indicator, when selected, then an interactive chart shows the time series with trend line and RAG status (on track / requires attention / deteriorating)
- [ ] Given the dashboard, when used by an international user, then page load time is < 2 seconds on standard broadband
- [ ] Given the dashboard, when tested for accessibility, then it passes WCAG 2.1 AA automated and manual testing

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: Open API

**Description**: The system must provide an open API returning SDG indicator data in JSON, CSV, and SDMX formats.

**Relates To**: BR-4, BR-6

**Acceptance Criteria**:

- [ ] Given a public API consumer, when querying an indicator, then data is returned in the requested format (JSON default, CSV and SDMX supported)
- [ ] Given an API query, when filtering by SDG goal, target, indicator, year, or nation, then only matching data is returned
- [ ] Given the API, when documented, then an OpenAPI 3.0 specification is publicly available with interactive documentation
- [ ] Given API consumers, when usage grows, then rate limiting prevents abuse while ensuring fair access (1,000 requests/minute default)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: SDMX Data Exchange with UNSD

**Description**: The system must generate and submit SDMX-compliant data files to the UN Statistics Division.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given all published UK SDG data, when the SDMX export is triggered, then data is formatted according to UNSD's SDMX data structure definition
- [ ] Given the SDMX export, when metadata is included, then it covers all mandatory SDMX metadata attributes
- [ ] Given the export, when submitted to UNSD, then it is accepted without validation errors

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-6: Sub-National Disaggregation

**Description**: The system must support sub-national disaggregation of indicators by England, Scotland, Wales, and Northern Ireland.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given an indicator with sub-national data, when displayed, then users can toggle between UK-level and nation-level views
- [ ] Given an indicator without sub-national data, when viewed, then a note explains why disaggregation is not available
- [ ] Given the API, when queried with a nation filter, then only data for that nation is returned

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-7: VNR Report Generation

**Description**: The system must support automated generation of data tables and visualisations for the UK Voluntary National Review.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a VNR preparation request, when triggered, then the system generates a comprehensive data pack with all indicators, trends, and RAG assessments
- [ ] Given the data pack, when exported, then it is in formats usable by the VNR drafting team (Excel, PDF, accessible web)
- [ ] Given trend analysis, when generated, then statistical commentary is auto-produced (e.g., "Indicator 1.2.1 improved from X to Y between 2015 and 2025, representing a Z% improvement")

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-8: Indicator Gap Analysis

**Description**: The system must track and display which of the 244 indicators have data, which have gaps, and what actions are planned to fill gaps.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given the full set of 244 indicators, when the gap analysis is viewed, then each indicator shows a status: Data Available, Data In Development, No UK Data Source, Not Applicable to UK
- [ ] Given indicators with gaps, when viewed, then a narrative explains why data is missing and what work is planned

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Dashboard Performance

**Requirement**: Dashboard pages must load within 2 seconds at the 95th percentile for users worldwide.

- Individual indicator page: < 1.5 seconds (p95)
- SDG goal overview page: < 2 seconds (p95)
- API query response: < 500ms (p95)
- SDMX bulk export: < 30 seconds for full UK dataset

**Priority**: HIGH

---

### Availability Requirements

#### NFR-A-1: Public Dashboard Availability

**Requirement**: 99.9% uptime for the public dashboard and API. Heightened availability during VNR periods and UNSD reporting deadlines.

**RTO**: 1 hour
**RPO**: 1 hour (published statistical data can be regenerated from source)

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Pre-Release Access Controls

**Requirement**: Unpublished indicator data must be accessible only to authorised ONS staff. Pre-release access controls must comply with UKSA pre-release access rules, technically enforced with audit trail.

**Priority**: CRITICAL

#### NFR-SEC-2: Publication Pipeline Integrity

**Requirement**: The publication pipeline must be isolated from non-ONS intervention. No external user or system can modify, delay, or suppress indicator publication.

**Priority**: CRITICAL

---

### Compliance Requirements

#### NFR-C-1: UKSA Code of Practice

**Requirement**: All published statistics must comply with the Code of Practice for Statistics (Trustworthiness, Quality, Value). UKSA Assessment Team review required pre-launch.

**Priority**: CRITICAL

#### NFR-C-2: Accessibility

**Requirement**: WCAG 2.1 Level AA compliance. Compliance with Public Sector Bodies Accessibility Regulations 2018.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Cross-Government Data Sharing Platform (Project 002)

**Purpose**: Ingest SDG indicator source data from 20+ departments via federated API gateway.

**Integration Type**: RESTful API via federated gateway

**Data Exchanged**:

- **From Departments to ONS**: Source data for SDG indicators (e.g., DWP employment data for Goal 8, Defra environment data for Goals 14-15, DHSC health data for Goal 3)

**Priority**: MUST_HAVE

---

### INT-2: UNSD SDG Data Portal

**Purpose**: Submit UK SDG data to UN Statistics Division.

**Integration Type**: SDMX data submission (file-based or API)

**Data Exchanged**:

- **From ONS to UNSD**: UK SDG indicator values, metadata

**Priority**: MUST_HAVE

---

### INT-3: International Aid Tracking Platform (Project 001)

**Purpose**: Receive ODA-related SDG indicator data (e.g., 17.2.1 ODA as % of GNI).

**Integration Type**: Event-driven notification + API

**Data Exchanged**:

- **From Project 001 to ONS**: ODA/GNI data, ODA by sector for SDG-related indicators

**Priority**: SHOULD_HAVE

---

### INT-4: Global Britain Trade Platform (Project 004)

**Purpose**: Receive trade-related SDG indicator data (e.g., 17.11.1 developing country exports).

**Integration Type**: API

**Data Exchanged**:

- **From Project 004 to ONS**: Trade data for SDG 17 trade indicators

**Priority**: SHOULD_HAVE

---

### INT-5: Devolved Administration Platforms

**Purpose**: Provide API access for Scotland, Wales, and NI to embed UK SDG data.

**Integration Type**: Open API (same as public API, with additional sub-national filtering)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: SDG Indicator

**Description**: A single SDG indicator value for a specific time period, geography, and disaggregation

**Key Attributes**: indicator_id (e.g., 1.2.1), goal, target, indicator_name, value, unit, year, geography (UK/England/Scotland/Wales/NI), disaggregation_dimensions, source_department, quality_tier, methodology_url

**Data Volume**: ~50,000 data points (244 indicators x multiple years x disaggregations)

**Data Classification**: OFFICIAL (published as open data once released)

#### Entity 2: Indicator Metadata

**Description**: Methodology, source, quality assessment for each indicator

**Key Attributes**: indicator_id, methodology, data_source, calculation_method, coverage, limitations, tier_classification, IAEG_methodology_alignment, update_frequency, next_update_date

**Data Volume**: 244 metadata records

**Data Classification**: OFFICIAL — PUBLIC

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use ONS existing statistical infrastructure and tooling where possible

**TC-2**: Must support SDMX data structures as defined by UNSD

**TC-3**: Must deploy on ONS-approved cloud infrastructure (currently AWS)

### Business Constraints

**BC-1**: Budget cap of GBP 8M over 3 years

**BC-2**: UKSA must approve the statistical framework before publication

**BC-3**: ONS SDG team has 8 FTE — platform must automate to be sustainable

### Assumptions

**A-1**: Source departments will provide data via Cross-Government Data Sharing Platform (Project 002)

**A-2**: IAEG-SDGs indicator framework remains stable through 2030 (minor revisions expected)

**A-3**: Devolved administrations will engage collaboratively on sub-national disaggregation

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| SDG indicators with data | ~180 | 200+ | 18 months | Indicator count |
| Monthly unique visitors | 0 | 10,000+ | 6 months post-launch | Web analytics |
| API consumers | 0 | 50+ registered | 12 months | API registration |
| VNR prep time | 8 weeks | < 2 weeks | 18 months | Time tracking |
| Sub-national coverage | ~30% | 60%+ | 18 months | Indicator audit |
| UNSD submission | Manual | Automated SDMX | 12 months | Submission records |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| National Statistician | ONS CEO | [ ] Approved | PENDING | |
| UKSA Assessment Team | Statistical compliance | [ ] Approved | PENDING | |
| Cabinet Office SDG Unit | Policy coordination | [ ] Approved | PENDING | |
| CDDO | Cross-government standards | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| SDG | Sustainable Development Goal — 17 goals adopted by UN in 2015 |
| SDMX | Statistical Data and Metadata eXchange — ISO standard for statistical data |
| VNR | Voluntary National Review — country report to UN on SDG progress |
| IAEG-SDGs | Inter-Agency Expert Group on SDGs — defines indicator methodology |
| UKSA | UK Statistics Authority — independent body overseeing UK statistics |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 17 Architecture Principles
- ARC-003-STKE-v1.0 — SDG Progress Dashboard Stakeholder Analysis
- UN General Assembly Resolution 70/1 (2030 Agenda)
- Global SDG Indicator Framework (A/RES/71/313)
- UKSA Code of Practice for Statistics

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG Progress Dashboard
**Model**: Claude Opus 4.6
