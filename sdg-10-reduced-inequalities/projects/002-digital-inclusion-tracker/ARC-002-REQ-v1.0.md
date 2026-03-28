# Project Requirements: Digital Inclusion Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Digital Inclusion Tracker (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Digital Inclusion Tracker, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Digital Inclusion Team, Ofcom, ONS, Good Things Foundation |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Digital Inclusion Tracker — a DSIT-operated platform measuring digital skills gaps, internet access disparities, and digital engagement levels across the UK, integrating data from the Lloyds Consumer Digital Index, Ofcom Connected Nations, ONS surveys, and community digital inclusion programmes.

---

## Executive Summary

### Business Context

Approximately 10 million adults in the UK lack foundational digital skills, and 1.7 million households have no internet access. Digital exclusion correlates strongly with age, disability, socioeconomic deprivation, and geographic location. Current measurement is fragmented across annual publications from Lloyds Bank, Ofcom, ONS, and DfE, with no unified view enabling targeted intervention planning. The Digital Inclusion Tracker will integrate these data sources into a single geospatial platform with a composite Digital Inclusion Index.

### Objectives

- Integrate five or more authoritative digital inclusion data sources into a unified platform
- Provide geographic disaggregation to local authority level for all inclusion metrics
- Develop a peer-reviewed composite Digital Inclusion Index
- Enable local authority benchmarking and intervention planning
- Track the impact of government and community digital inclusion programmes

### Expected Outcomes

- 5+ data sources integrated within 12 months
- 80%+ of metrics available at local authority level
- Composite Digital Inclusion Index published with ONS endorsement within 18 months
- 100+ local authorities actively using the platform within 18 months
- 10+ local digital inclusion programmes informed by platform data within 18 months

### Project Scope

**In Scope**:

- Data integration from Lloyds Consumer Digital Index, Ofcom Connected Nations, ONS Internet Access survey, DfE Essential Digital Skills, Good Things Foundation programme data
- Geospatial dashboard with local authority, LSOA, and constituency views
- Composite Digital Inclusion Index development
- Local authority benchmarking tool
- Open data publication of aggregated metrics
- Community programme impact tracking

**Out of Scope**:

- Individual-level digital skills assessment tools
- Direct digital skills training delivery
- Broadband infrastructure deployment
- Devolved administration-specific dashboards (collaboration with devolved governments is in scope)

---

## Business Requirements

### BR-001: Unified Digital Inclusion Data Platform

**Description**: DSIT must have a single platform integrating multiple digital inclusion data sources to replace fragmented annual publications.

**Rationale**: Policy-makers cannot form a coherent picture of digital exclusion from scattered, inconsistent data sources published on different timescales with different methodologies.

**Success Criteria**:

- 5+ data sources integrated and accessible via single dashboard
- Data updated within 10 working days of source publication
- Single API providing access to all integrated data

**Priority**: MUST_HAVE

**Stakeholder**: DSIT Minister (SD-1)

---

### BR-002: Geographic Disaggregation

**Description**: All metrics must be available at local authority level minimum, with LSOA-level data where source data permits.

**Rationale**: National averages mask enormous local variation. Local authorities need granular data to target interventions at the most digitally excluded communities within their boundaries.

**Success Criteria**:

- 80%+ of metrics available at local authority level
- Confidence intervals published for all small-area estimates
- ONS geographic boundary data integrated and kept current

**Priority**: MUST_HAVE

**Stakeholder**: Local authorities (SD-4), DSIT Minister (SD-1)

---

### BR-003: Composite Digital Inclusion Index

**Description**: The platform must calculate a composite index combining connectivity, digital skills, usage, motivation, and outcomes dimensions.

**Rationale**: A single composite measure enables benchmarking, trend tracking, and policy prioritisation. Existing indices (e.g., IMD) do not directly measure digital inclusion.

**Success Criteria**:

- Index methodology published and peer-reviewed
- ONS endorsement obtained
- Annual publication alongside dimensional breakdowns

**Priority**: SHOULD_HAVE

**Stakeholder**: DSIT Minister (SD-1), Ofcom (SD-2)

---

### BR-004: Community Programme Impact Integration

**Description**: The platform must integrate data from community-level digital inclusion programmes (National Databank, library digital skills courses, charity programmes) to make grassroots impact visible.

**Rationale**: Community programmes reach the most excluded populations but their impact is invisible in national statistics. Integration validates grassroots investment and improves intervention targeting.

**Success Criteria**:

- Data integration API available for community programme providers
- Privacy-preserving aggregation of individual intervention data
- Community data displayed alongside national statistics with clear quality indicators

**Priority**: SHOULD_HAVE

**Stakeholder**: Good Things Foundation (SD-3)

---

## Functional Requirements

### User Personas

#### Persona 1: DSIT Policy Analyst

- **Role**: DSIT digital inclusion policy team member
- **Goals**: Analyse national and regional digital inclusion trends, prepare ministerial briefings, target interventions
- **Pain Points**: Data in separate PDFs and spreadsheets, no geographic visualisation, no composite measure
- **Technical Proficiency**: Medium

#### Persona 2: Local Authority Digital Lead

- **Role**: Local authority officer responsible for digital inclusion programmes
- **Goals**: Benchmark local area, identify priority populations, evidence funding bids, track programme impact
- **Pain Points**: National data does not disaggregate to local level, cannot compare with similar authorities
- **Technical Proficiency**: Medium

#### Persona 3: Community Programme Manager

- **Role**: Manager at a digital inclusion charity (e.g., Good Things Foundation hub)
- **Goals**: Submit programme impact data, see local area context, demonstrate value to funders
- **Pain Points**: No platform to report outcomes, data stays in spreadsheets, impact invisible
- **Technical Proficiency**: Low to Medium

---

### Functional Requirements Detail

#### FR-001: Multi-Source Data Ingestion

**Description**: The system must ingest data from multiple external sources in various formats (CSV, JSON, API, PDF extraction) and normalise into a common data model.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given Lloyds Consumer Digital Index data (annual CSV), when published, then data is ingested within 10 working days
- [ ] Given Ofcom Connected Nations data (annual dataset), when published, then connectivity metrics are updated
- [ ] Given ONS Internet Access survey results, when published, then household access metrics are updated
- [ ] Given DfE Essential Digital Skills data, when published, then skills metrics are updated
- [ ] Given Good Things Foundation API data, when submitted, then programme data is integrated

**Priority**: MUST_HAVE

---

#### FR-002: Geospatial Dashboard

**Description**: The system must provide an interactive map-based dashboard showing digital inclusion metrics at multiple geographic levels (UK, region, local authority, constituency, LSOA/MSOA).

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a geographic level selection, when the map renders, then inclusion metrics are displayed as a choropleth
- [ ] Given a local authority, when clicked, then a detail panel shows all available metrics with trends
- [ ] Given a constituency, when selected, then local authority data is mapped to the parliamentary boundary
- [ ] Given LSOA data, when available, then zooming into an area reveals sub-local-authority variation

**Priority**: MUST_HAVE

---

#### FR-003: Local Authority Benchmarking

**Description**: The system must enable local authorities to compare their digital inclusion metrics against national averages, regional averages, and statistically similar authorities (CIPFA nearest neighbours).

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a local authority, when benchmarking is selected, then comparison with CIPFA nearest neighbours is displayed
- [ ] Given a metric, when compared, then the authority's rank and percentile are shown
- [ ] Given historical data, when trend view is selected, then improvement or regression relative to comparators is visible

**Priority**: SHOULD_HAVE

---

#### FR-004: Composite Index Calculation

**Description**: The system must calculate a composite Digital Inclusion Index from constituent dimensions (connectivity, skills, usage, motivation, outcomes) using a published, configurable weighting methodology.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given dimension scores, when the index is calculated, then a single composite score (0-100) is produced per geographic area
- [ ] Given dimension weights, when an analyst adjusts weights, then the composite score updates (sensitivity analysis mode)
- [ ] Given the composite score, when displayed, then constituent dimension scores are always visible alongside

**Priority**: SHOULD_HAVE

---

#### FR-005: Community Data Submission API

**Description**: The system must provide an API for community digital inclusion programme providers to submit programme outcome data (participants, digital skills improvements, data/device provision).

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a registered programme provider, when data is submitted via API, then it is validated and stored
- [ ] Given individual-level data, when aggregated, then no individual can be identified (k-anonymity threshold of 10)
- [ ] Given programme data, when displayed on dashboard, then it is visually distinguished from national statistical data

**Priority**: SHOULD_HAVE

---

#### FR-006: Open Data Publication

**Description**: The system must publish aggregated digital inclusion metrics as open data in machine-readable formats (CSV, JSON, GeoJSON), with metadata conforming to DCAT standards.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Given aggregated metrics, when published, then CSV, JSON, and GeoJSON formats are available
- [ ] Given published data, when accessed, then an Open Government Licence applies
- [ ] Given dataset metadata, when published, then it conforms to DCAT-AP-UK standards

**Priority**: SHOULD_HAVE

---

#### FR-007: Data Quality Indicators

**Description**: The system must display data quality indicators (confidence intervals, sample sizes, data freshness) alongside all metrics, particularly for small-area estimates.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a small-area estimate, when displayed, then the confidence interval is shown
- [ ] Given a metric, when the source data is older than 12 months, then a data freshness warning is displayed
- [ ] Given community-reported data, when displayed, then quality grade (A-D) is shown based on sample size and methodology

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Dashboard Load Time

**Requirement**: Geospatial dashboard initial load within 3 seconds, subsequent geographic navigation within 1 second, for up to 200 concurrent users.

**Priority**: MUST_HAVE

---

#### NFR-P-002: Data Processing

**Requirement**: Full data refresh (all sources) must complete within 4 hours.

**Priority**: SHOULD_HAVE

---

### Security Requirements

#### NFR-SEC-001: Data Classification

**Requirement**: Aggregated metrics classified OFFICIAL. Raw community programme data with individual-level records classified OFFICIAL-SENSITIVE with restricted access.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Statistical Disclosure Control

**Requirement**: All published data must undergo statistical disclosure control to prevent identification of individuals. Minimum threshold of k=10 for all published aggregations.

**Priority**: MUST_HAVE

---

### Accessibility Requirements

#### NFR-ACC-001: Platform Accessibility

**Requirement**: WCAG 2.2 Level AA minimum. As a digital inclusion platform, it must itself be digitally inclusive — supporting low-bandwidth connections, older browsers, and assistive technologies.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Uptime

**Requirement**: 99.5% uptime for the public dashboard (21.9 hours maximum unplanned downtime per year). Lower SLA acceptable as data is not real-time critical.

**Priority**: SHOULD_HAVE

---

## Integration Requirements

### INT-001: Lloyds Consumer Digital Index

**Purpose**: Primary source for digital skills and engagement metrics

**Integration Type**: Annual batch import (CSV/Excel)

**Data Exchanged**: Digital skills levels, internet usage patterns, digital engagement scores by demographic and geography

**Priority**: MUST_HAVE

---

### INT-002: Ofcom Connected Nations

**Purpose**: Broadband and mobile connectivity metrics

**Integration Type**: Annual batch import (dataset download)

**Data Exchanged**: Broadband availability, speed, mobile coverage by geographic area

**Priority**: MUST_HAVE

---

### INT-003: ONS Internet Access Survey

**Purpose**: Household internet access and usage statistics

**Integration Type**: Annual batch import (CSV)

**Data Exchanged**: Internet access rates, device ownership, reasons for non-use, by demographic

**Priority**: MUST_HAVE

---

### INT-004: Good Things Foundation National Databank

**Purpose**: Community-level digital inclusion intervention data

**Integration Type**: REST API (provider-initiated)

**Data Exchanged**: Programme participants (anonymised), interventions delivered, outcomes achieved

**Authentication**: API key per registered programme provider

**Priority**: SHOULD_HAVE

---

### INT-005: ONS Geographies API

**Purpose**: Geographic boundary data for mapping and spatial analysis

**Integration Type**: REST API

**Data Exchanged**: Boundary polygons for LSOAs, MSOAs, local authorities, regions, constituencies

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity: GeographicArea

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | String(20) | Yes | ONS geographic code |
| name | String(255) | Yes | Area name |
| level | Enum | Yes | lsoa, msoa, local_authority, region, country |
| parent_id | String(20) | No | Parent geographic area |
| boundary_geojson | GeoJSON | Yes | Geographic boundary |

#### Entity: InclusionMetric

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| area_id | String(20) | Yes | Geographic area |
| dimension | Enum | Yes | connectivity, skills, usage, motivation, outcomes |
| metric_name | String(100) | Yes | Specific metric name |
| value | Decimal | Yes | Metric value |
| confidence_lower | Decimal | No | Lower confidence bound |
| confidence_upper | Decimal | No | Upper confidence bound |
| source | String(100) | Yes | Data source name |
| reference_period | String(20) | Yes | Time period (e.g., 2025-Q4) |
| quality_grade | Enum | No | A, B, C, D quality grade |

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Data sources integrated | 0 | 5+ | 12 months | Platform data catalogue |
| Metrics at local authority level | 0% | 80%+ | 12 months | Metric coverage analysis |
| Local authorities using platform | 0 | 100+ | 18 months | User analytics |
| Programmes informed by platform | 0 | 10+ | 18 months | Case study tracking |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK Digital Strategy | Strategy | GOV.UK | Digital inclusion targets | N/A |
| Lloyds Consumer Digital Index 2025 | Research | Lloyds Bank | Digital skills methodology | N/A |
| Ofcom Connected Nations 2025 | Report | Ofcom | Connectivity coverage methodology | N/A |
| ARC-002-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | projects/002-digital-inclusion-tracker/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Inclusion Tracker
**Model**: Claude Opus 4.6
