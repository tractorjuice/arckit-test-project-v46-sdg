# Project Requirements: Levelling Up Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Levelling Up Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Levelling Up Dashboard, DLUHC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Cities & Local Growth Unit, ONS, Regional Mayors, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Levelling Up Dashboard — a DLUHC-operated geospatial platform monitoring regional inequality metrics and tracking Levelling Up Fund allocations against the 12 Levelling Up missions.

---

## Executive Summary

### Business Context

The Levelling Up and Regeneration Act 2023 requires the government to set missions for reducing geographic inequalities and report progress annually. Currently, data on regional inequality is scattered across ONS subnational statistics, the Index of Multiple Deprivation (IMD), departmental publications, and fund allocation spreadsheets. No single platform provides a unified, geospatial view linking inequality metrics to Levelling Up investment. The Dashboard will provide this capability, serving ministers, parliamentarians, regional mayors, local authority leaders, and the public.

### Objectives

- Create a unified geospatial platform integrating inequality metrics and fund allocation data
- Track progress against all 12 Levelling Up missions with standardised metrics
- Provide geographic analysis from LSOA to national level
- Enable fund allocation tracking with project-level transparency
- Publish data as open data for independent scrutiny

### Expected Outcomes

- Dashboard live with 15+ inequality metrics within 12 months
- 100% of major Levelling Up funds tracked with geographic mapping
- 10,000+ monthly active users within 12 months
- ONS endorsement of methodology within 18 months
- Data used in at least 5 parliamentary reports within 24 months

### Project Scope

**In Scope**:

- IMD/IoD integration with interactive geospatial mapping
- ONS subnational indicators (productivity, pay, health, education, crime, housing)
- Levelling Up Fund allocation tracking (Rounds 1-3, Towns Fund, UKSPF, Community Ownership Fund)
- Mission progress metrics aligned to Levelling Up White Paper
- Geographic analysis at LSOA, MSOA, local authority, constituency, and region levels
- Open data publication
- Ministerial briefing and parliamentary question support views

**Out of Scope**:

- Causal analysis of fund impact (observational data only; evaluation is separate)
- Real-time economic data (GDP, employment updated monthly; others quarterly/annually)
- Devolved administration policy-specific dashboards
- Fund application processing (separate systems)

---

## Business Requirements

### BR-001: Integrated Geospatial Inequality Dashboard

**Description**: DLUHC must have a public-facing geospatial dashboard integrating multiple inequality metrics with interactive mapping from LSOA to national level.

**Rationale**: Regional inequality data is currently scattered across multiple publications. Ministers, mayors, and local leaders need a single source for geographic inequality analysis.

**Success Criteria**:

- 15+ inequality metrics mapped geospatially
- 5+ geographic levels navigable interactively
- Dashboard publicly accessible and free to use

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1)

---

### BR-002: Levelling Up Fund Allocation Tracking

**Description**: The dashboard must track all major Levelling Up fund allocations, mapping them to geographic areas and linking to relevant outcome metrics.

**Rationale**: Parliamentary and public accountability requires transparent tracking of where Levelling Up money is going and what it is achieving.

**Success Criteria**:

- 100% of major fund allocations tracked
- Fund data updated within 5 working days of allocation announcements
- Project-level granularity where available

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Commons Committee (SD-4)

---

### BR-003: Mission Progress Tracking

**Description**: The dashboard must track progress against all 12 Levelling Up missions with standardised, comparable metrics over time.

**Rationale**: The Levelling Up and Regeneration Act 2023 requires mission reporting. Standardised metrics enable comparison across missions and geographies.

**Success Criteria**:

- All 12 missions represented with at least 2 metrics each
- Trend data showing direction of travel
- Mission-level summary view suitable for ministerial briefings

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1)

---

### BR-004: ONS-Compliant Statistical Methodology

**Description**: All statistical methodology must comply with the Code of Practice for Statistics and achieve ONS endorsement.

**Rationale**: The dashboard will be scrutinised by the UK Statistics Authority, NAO, and academic researchers. Non-compliant methodology would undermine credibility and invite formal censure.

**Success Criteria**:

- ONS written endorsement of methodology
- Code of Practice compliance confirmed
- No adverse UK Statistics Authority findings

**Priority**: MUST_HAVE

**Stakeholder**: ONS (SD-2)

---

### BR-005: Open Data Publication

**Description**: All aggregated metrics and fund allocation data must be published as open data in machine-readable formats.

**Rationale**: Open data enables independent scrutiny by IFS, think tanks, academics, and journalists, strengthening accountability and public trust.

**Success Criteria**:

- All dashboard data downloadable in CSV, JSON, GeoJSON
- API available for programmatic access
- Open Government Licence applied

**Priority**: SHOULD_HAVE

**Stakeholder**: Commons Committee (SD-4), IFS

---

## Functional Requirements

### User Personas

#### Persona 1: Minister / Special Adviser

- **Role**: Secretary of State or SpAd preparing for PMQs, debates, or media
- **Goals**: Quickly find positive Levelling Up stories for specific constituencies, see headline mission progress
- **Pain Points**: Data is in PDFs and spreadsheets, cannot answer constituency-specific questions quickly
- **Technical Proficiency**: Low

#### Persona 2: Regional Mayor

- **Role**: Elected regional mayor (e.g., Greater Manchester, West Midlands)
- **Goals**: Track fund allocations to region, benchmark against other regions, identify intra-regional disparities
- **Pain Points**: Fund data scattered, cannot see cumulative investment picture, limited LSOA analysis
- **Technical Proficiency**: Low to Medium (via analysts)

#### Persona 3: DLUHC Policy Analyst

- **Role**: DLUHC analyst supporting Levelling Up policy development
- **Goals**: Deep-dive analysis of inequality patterns, correlate fund allocations with outcomes, prepare evidence for policy papers
- **Pain Points**: Time-consuming data assembly from multiple sources, no geospatial analysis tool
- **Technical Proficiency**: High

#### Persona 4: Academic Researcher / Think Tank Analyst

- **Role**: IFS, IPPR, university researcher studying regional inequality
- **Goals**: Download comprehensive datasets, replicate government analysis, publish independent findings
- **Pain Points**: Data not machine-readable, methodology not transparent, no API
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: Interactive Geospatial Map

**Description**: The system must provide an interactive map of the UK displaying inequality metrics as choropleth layers, navigable from national overview to LSOA-level detail.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given the dashboard, when it loads, then a UK map displays with the default inequality metric as a choropleth
- [ ] Given a map, when the user zooms in, then the geographic level transitions (national -> region -> local authority -> LSOA)
- [ ] Given a geographic area, when clicked, then a detail panel shows all available metrics with values and trends
- [ ] Given multiple metrics, when a different metric is selected, then the choropleth updates

**Priority**: MUST_HAVE

---

#### FR-002: IMD/IoD Integration

**Description**: The system must integrate Index of Multiple Deprivation (IMD) and Indices of Deprivation (IoD) data at LSOA level, with all seven deprivation domains and the overall IMD score.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given IMD data, when loaded, then all 32,844 LSOAs in England display deprivation deciles
- [ ] Given the seven deprivation domains, when a domain is selected, then the choropleth shows that domain's ranking
- [ ] Given an LSOA, when selected, then all seven domain scores and the composite IMD score are displayed

**Priority**: MUST_HAVE

---

#### FR-003: Fund Allocation Tracker

**Description**: The system must display all Levelling Up Fund allocations on the map, linked to geographic areas, with project-level details and amounts.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a fund allocation, when data is entered, then it appears on the map at the correct geographic location
- [ ] Given a local authority, when selected, then all fund allocations to that area are listed with amounts and project names
- [ ] Given a fund round, when filtered, then only allocations from that round are displayed
- [ ] Given cumulative allocations, when viewed at regional level, then total investment per region is calculated

**Priority**: MUST_HAVE

---

#### FR-004: Mission Progress Dashboard

**Description**: The system must display a mission-level summary view showing progress against each of the 12 Levelling Up missions with trend indicators.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given the 12 missions, when the mission view loads, then each mission shows a headline metric with direction of travel
- [ ] Given a mission, when clicked, then supporting metrics and geographic breakdown are displayed
- [ ] Given trend data, when displayed, then green/amber/red status indicators show whether on track

**Priority**: MUST_HAVE

---

#### FR-005: Constituency Lookup

**Description**: The system must enable lookup by parliamentary constituency, mapping LSOA data to constituency boundaries for parliamentary question support.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a constituency name or MP name, when searched, then the constituency area is highlighted on the map
- [ ] Given a constituency, when selected, then aggregated metrics (population-weighted from LSOAs) are displayed
- [ ] Given a constituency, when fund allocations are viewed, then projects within the constituency boundary are listed

**Priority**: MUST_HAVE

---

#### FR-006: Data Download and API

**Description**: The system must provide data download in CSV, JSON, and GeoJSON formats, and a RESTful API for programmatic access to all published data.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given a dataset, when download is requested, then CSV, JSON, and GeoJSON formats are available
- [ ] Given the API, when a geographic area and metric are specified, then data is returned in JSON
- [ ] Given the API, when accessed without authentication, then public data is returned (open access)
- [ ] Given a dataset, when published, then DCAT-AP-UK metadata is generated

**Priority**: SHOULD_HAVE

---

#### FR-007: Comparator Analysis

**Description**: The system must enable comparison of inequality metrics between user-selected geographic areas (e.g., two constituencies, two local authorities, a region vs national average).

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given two or more areas, when selected for comparison, then metrics are displayed side by side
- [ ] Given a comparison, when a chart view is selected, then bar or line charts render the comparison
- [ ] Given national average, when an area is compared, then deviation from national average is highlighted

**Priority**: SHOULD_HAVE

---

#### FR-008: Statistical Methodology Documentation

**Description**: The system must display methodology notes, data sources, confidence intervals, and caveats for every metric, accessible in-context from the dashboard.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a metric, when the methodology link is clicked, then source, methodology, and limitations are displayed
- [ ] Given a small-area estimate, when displayed, then confidence interval is shown
- [ ] Given a metric with known limitations, when displayed, then caveats are prominently noted

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Map Rendering

**Requirement**: Initial map render within 3 seconds. Geographic level transition (zoom) within 1.5 seconds. LSOA-level choropleth rendering (32,844 polygons) within 3 seconds.

**Priority**: MUST_HAVE

---

#### NFR-P-002: Concurrent Users

**Requirement**: Support 1,000 concurrent users during peak periods (e.g., after ministerial announcements or fund allocation publications).

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Data Classification

**Requirement**: All published metrics classified OFFICIAL. Pre-publication data classified OFFICIAL-SENSITIVE until ministerially cleared for release.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Pre-Publication Access Controls

**Requirement**: Pre-publication data (especially fund allocation announcements) must be restricted to authorised DLUHC staff. Breach of pre-publication rules is a disciplinary offence under the Code of Practice for Statistics.

**Priority**: MUST_HAVE

---

### Accessibility Requirements

#### NFR-ACC-001: WCAG 2.2 Level AA

**Requirement**: WCAG 2.2 Level AA compliance. Particular attention to geospatial map accessibility — provide tabular data alternative for all map-based visualisations, ensuring screen reader users can access all data.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Uptime

**Requirement**: 99.9% uptime for the public dashboard. Higher SLA than Digital Inclusion Tracker because the dashboard directly supports ministerial decision-making and parliamentary accountability.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: ONS Subnational Indicators

**Purpose**: Economic and social metrics (productivity, pay, health, education, crime, housing) by local authority and region

**Integration Type**: API (ONS Beta API) and batch download

**Data Exchanged**: 50+ subnational indicators with time series

**Priority**: MUST_HAVE

---

### INT-002: Index of Multiple Deprivation

**Purpose**: LSOA-level deprivation data across seven domains

**Integration Type**: Batch import (CSV from DLUHC publication)

**Data Exchanged**: IMD scores, ranks, and domain scores for 32,844 LSOAs

**Priority**: MUST_HAVE

---

### INT-003: Levelling Up Fund Management Systems

**Purpose**: Fund allocation data by project and geographic area

**Integration Type**: Internal DLUHC data feed (database export or API)

**Data Exchanged**: Fund name, round, project name, amount, recipient organisation, geographic area, status

**Priority**: MUST_HAVE

---

### INT-004: Ordnance Survey Boundary Data

**Purpose**: Geographic boundary polygons for mapping

**Integration Type**: Batch import (GeoJSON/Shapefile from OS OpenData)

**Data Exchanged**: Boundary polygons for LSOAs, MSOAs, local authorities, constituencies, regions

**Priority**: MUST_HAVE

---

### INT-005: ONS Geographies API

**Purpose**: Geographic hierarchy and lookup (which LSOA is in which local authority, constituency, etc.)

**Integration Type**: REST API

**Data Exchanged**: Geographic hierarchy relationships, code lookups

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity: LevellingUpMission

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | Integer | Yes | Mission number (1-12) |
| name | String(255) | Yes | Mission title |
| target_year | Integer | Yes | Mission target year (e.g., 2030) |
| status | Enum | Yes | on_track, at_risk, off_track |
| headline_metric_id | UUID | No | Primary progress metric |

#### Entity: FundAllocation

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| fund_name | String(100) | Yes | Fund name (LUF, Towns Fund, UKSPF, etc.) |
| round | String(20) | No | Fund round if applicable |
| project_name | String(500) | Yes | Project name |
| amount_gbp | Decimal | Yes | Allocation amount in GBP |
| recipient_org | String(255) | Yes | Recipient organisation |
| area_id | String(20) | Yes | Geographic area code |
| announcement_date | Date | Yes | Date allocation announced |
| status | Enum | Yes | announced, in_delivery, completed, cancelled |

#### Entity: InequalityMetric

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| area_id | String(20) | Yes | Geographic area code |
| mission_id | Integer | No | Related Levelling Up mission |
| metric_name | String(100) | Yes | Metric name |
| value | Decimal | Yes | Metric value |
| period | String(20) | Yes | Time period |
| source | String(100) | Yes | Data source |
| methodology_note | Text | No | Methodology notes |

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Inequality metrics on dashboard | 0 | 15+ | 12 months | Platform metric catalogue |
| Fund allocations tracked | 0 | 100% of major funds | 12 months | Fund coverage analysis |
| Monthly active users | 0 | 10,000+ | 12 months | Web analytics |
| ONS methodology endorsement | None | Endorsed | 18 months | ONS letter |
| Parliamentary citations | 0 | 5+ | 24 months | Hansard search |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Levelling Up White Paper | Policy | GOV.UK | 12 missions, metrics framework | N/A |
| Levelling Up and Regeneration Act 2023 | Legislation | legislation.gov.uk | Statutory reporting requirements | N/A |
| IMD 2019 Technical Report | Methodology | DLUHC | IMD calculation methodology | N/A |
| Code of Practice for Statistics | Standard | UK Statistics Authority | Statistical quality standards | N/A |
| ARC-003-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | projects/003-levelling-up-dashboard/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Levelling Up Dashboard
**Model**: Claude Opus 4.6
