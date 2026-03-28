# Project Requirements: Women in STEM Tracking Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Women in STEM Tracking Dashboard (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Women in STEM Programme, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Programme Board, UKRI, HESA, DfE |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Women in STEM Tracking Dashboard, a data analytics platform providing comprehensive, timely, and intersectional data on gender diversity across the UK's STEM pipeline from education to senior leadership.

---

## Executive Summary

### Business Context

The UK faces persistent gender imbalances in science, technology, engineering, and mathematics. Women represent only 24% of the STEM workforce (WISE 2023), with acute underrepresentation in engineering (16%), computing (20%), and physics (23%). The "leaky pipeline" metaphor describes women's progressive attrition from STEM at each career stage. However, no single platform aggregates data across the full pipeline — from school subject choices through to boardroom representation — making it impossible to identify precisely where and why women leave STEM.

DSIT's Science and Technology Framework commits to growing the R&D workforce and improving diversity. UKRI's EDI Strategy commits to equitable research funding. Multiple organisations (WISE, Royal Society, RAEng, IET, BCS) publish partial datasets, but these use different definitions, different time periods, and different methodologies, creating an inconsistent and confusing picture.

The Women in STEM Tracking Dashboard will aggregate data from 8+ sources into a single, authoritative platform providing full-pipeline visibility, intersectional analysis, and timely publication.

### Objectives

- Establish the single authoritative source for UK STEM gender diversity data
- Provide full pipeline visibility from GCSE/A-level through to senior leadership
- Enable intersectional analysis (gender x ethnicity x disability x socio-economic background)
- Reduce data publication lag from 12-24 months to 6 months maximum
- Support international comparison with EU and OECD benchmarks

### Project Scope

**In Scope**:

- Data aggregation pipeline from HESA, UKRI, DfE, ONS, professional bodies
- Interactive public dashboard with pipeline visualisation
- Intersectional analysis capability with statistical disclosure control
- Open data API for researchers and organisations
- International comparison with Eurostat/OECD She Figures data
- Automated data quality monitoring and publication workflow
- Embeddable widgets for partner organisations

**Out of Scope**:

- Individual-level research data access (separate UKRI/HESA service)
- Employer-level workforce diversity reporting (covered by Project 003)
- STEM curriculum design or educational interventions
- Industry-specific detailed workforce analysis (e.g., cybersecurity skills gap)

---

## Business Requirements

### BR-1: Full STEM Pipeline Data Aggregation

**Description**: The platform must aggregate gender-disaggregated data across the full STEM pipeline, covering at least 8 stages from education through to senior leadership.

**Rationale**: No existing platform provides this full-pipeline view. Policy interventions require understanding of where in the pipeline women are lost, which varies by STEM discipline.

**Pipeline Stages Required**:

1. GCSE and A-level STEM subject entries (DfE)
2. Undergraduate STEM enrolment and completion (HESA)
3. Postgraduate (taught) STEM enrolment and completion (HESA)
4. Doctoral STEM enrolment and completion (HESA)
5. Research funding applications and awards (UKRI)
6. Early-career academic positions (HESA Staff record)
7. STEM industry workforce (ONS Labour Force Survey, professional bodies)
8. Senior leadership in STEM (FTSE Women in Science, professional body data)

**Success Criteria**:

- Data available for all 8 pipeline stages
- Data disaggregated by gender at each stage
- Data disaggregated by STEM discipline (physical sciences, biological sciences, engineering, computing, mathematics)
- Data updated within 6 months of source publication

**Priority**: MUST_HAVE

---

### BR-2: Intersectional Analysis Capability

**Description**: The platform must support analysis of STEM gender diversity intersected with ethnicity, disability, socio-economic background, and geographic region.

**Rationale**: The experience of women in STEM varies dramatically by ethnicity, disability status, and background. Black women leave STEM at higher rates than white women. Disabled women face additional barriers. Single-axis gender analysis masks these disparities.

**Success Criteria**:

- Intersectional queries across at least 3 dimensions (gender + 2 others)
- Statistical disclosure control preventing identification from small cohorts
- Visualisations that communicate intersectional patterns clearly

**Priority**: MUST_HAVE

---

### BR-3: Timely Data Publication

**Description**: The platform must publish data within 6 months of the source data collection period, significantly reducing the current 12-24 month lag.

**Rationale**: Policy decisions made on 2-year-old data risk targeting interventions at problems that have shifted. Timely data enables responsive policy.

**Success Criteria**:

- Maximum 6-month publication lag for each data source
- Automated data ingestion pipeline reducing manual processing
- Data freshness indicators visible on all dashboard pages

**Priority**: MUST_HAVE

---

### BR-4: International Benchmarking

**Description**: The platform must provide comparison with international STEM gender diversity data, enabling assessment of UK performance against EU and OECD countries.

**Rationale**: UK performance on women in STEM is context-dependent — below average on some measures, above on others. International comparison enables learning from countries with better outcomes and tracking relative progress.

**Success Criteria**:

- Comparison with at least 10 EU/OECD countries on key pipeline indicators
- Data sourced from Eurostat She Figures and OECD indicators
- Methodology differences noted transparently

**Priority**: SHOULD_HAVE

---

### BR-5: Open Data and Researcher Access

**Description**: The platform must provide open data APIs and downloadable datasets enabling independent analysis by researchers, organisations, and media.

**Rationale**: The platform's value as an authoritative source depends on enabling independent analysis. Restricting data access would undermine credibility and reduce impact.

**Success Criteria**:

- Versioned REST API with published documentation
- Bulk download in CSV and JSON formats
- API consumers registered and tracked (for usage analytics)
- Data licensed under Open Government Licence

**Priority**: MUST_HAVE

---

### BR-6: Embeddable Visualisations

**Description**: The platform must provide embeddable visualisation widgets that partner organisations (Royal Society, WISE, universities) can embed on their own websites.

**Rationale**: Maximum impact requires data reaching audiences where they already are, not just on the DSIT platform.

**Success Criteria**:

- Embeddable chart widgets with configurable parameters
- Widgets update automatically when new data is published
- Usage tracking for embedded widgets

**Priority**: COULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Professor Elena — Academic Researcher

- **Role**: Professor of Computer Science at a Russell Group university; chair of the department's EDI committee
- **Goals**: Understand the gender pipeline in her discipline; benchmark her department against national averages; identify specific transition points where intervention is most needed
- **Pain Points**: Currently assembles data from 5+ sources with different definitions; data is always 18+ months old; cannot do intersectional analysis (gender x ethnicity in computing)
- **Technical Proficiency**: High

#### Persona 2: James — DSIT Policy Adviser

- **Role**: Policy adviser in DSIT's Science, Innovation and Research directorate
- **Goals**: Brief the Minister on progress against STEM diversity targets; identify which policy interventions are working; compare UK with international peers
- **Pain Points**: No single source for full pipeline data; compiles Ministerial briefing from multiple reports with inconsistent figures; cannot show pipeline leakage points
- **Technical Proficiency**: Medium

#### Persona 3: Amira — WISE Campaign Manager

- **Role**: Campaign manager at WISE, producing the annual WISE Statistics report
- **Goals**: Access timely, granular STEM diversity data for the annual WISE report and campaign materials; identify specific sectors or pipeline stages for targeted campaigns
- **Pain Points**: Spends 3 months assembling data from multiple sources; data definitions vary between sources; some data sources charge for access
- **Technical Proficiency**: Medium

#### Persona 4: Sophie — Year 11 Student

- **Role**: 15-year-old considering A-level subject choices, interested in engineering but uncertain
- **Goals**: See evidence that women succeed in engineering; find role model data; understand career prospects
- **Pain Points**: Limited visible female role models in engineering; statistics presented in academic format not accessible to students
- **Technical Proficiency**: Medium-High (digital native but not data-literate)

---

### Functional Requirements Detail

#### FR-1: Automated Data Ingestion Pipeline

**Description**: The system must automatically ingest data from 8+ sources on a scheduled basis, validate data quality, reconcile definitions, and update the dashboard.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a new data release from HESA, when the scheduled ingestion runs, then data is validated and available in the dashboard within 24 hours
- [ ] Given data from different sources using different STEM definitions, then a reconciliation mapping is applied consistently
- [ ] Given data quality issues (missing fields, outliers), then the pipeline flags issues for manual review without blocking publication of valid data

**Priority**: MUST_HAVE

---

#### FR-2: Interactive Pipeline Visualisation

**Description**: The system must provide an interactive visual representation of the STEM pipeline, showing the proportion of women at each stage, with the ability to filter by STEM discipline, time period, and geography.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given the pipeline view, then users can see the proportion of women at each of 8 pipeline stages
- [ ] Given a pipeline stage, then users can click to see detailed breakdown by discipline
- [ ] Given a time period selector, then users can see pipeline progression over 5+ years
- [ ] Given the pipeline, then "leakage points" (stages with the largest gender drop-off) are visually highlighted

**Priority**: MUST_HAVE

---

#### FR-3: Intersectional Analysis Dashboard

**Description**: The system must provide an intersectional analysis view enabling users to cross-tabulate STEM gender data with ethnicity, disability, and socio-economic indicators.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given intersectional query (e.g., Black women in engineering), then data is displayed with appropriate statistical disclosure control
- [ ] Given small cohorts, then cell suppression is applied (minimum 5) to prevent identification
- [ ] Given intersectional data, then visualisations clearly communicate patterns and disparities

**Priority**: MUST_HAVE

---

#### FR-4: International Comparison Module

**Description**: The system must provide comparison of UK STEM gender diversity metrics with selected EU/OECD countries.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a pipeline indicator, then users can compare UK performance with 10+ countries
- [ ] Given different national data definitions, then methodology differences are transparently noted
- [ ] Given international data, then it is sourced from official statistics (Eurostat, OECD)

**Priority**: SHOULD_HAVE

---

#### FR-5: Open Data API

**Description**: The system must provide a versioned REST API enabling programmatic access to all published data.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a registered API consumer, then they can query any published dataset
- [ ] Given the API, then it supports filtering by pipeline stage, discipline, year, and geography
- [ ] Given bulk download requests, then CSV and JSON exports are available
- [ ] Given API versioning, then existing consumers are not broken by new data fields

**Priority**: MUST_HAVE

---

#### FR-6: Embeddable Widget Generator

**Description**: The system must provide configurable embeddable chart widgets for partner organisations.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given a chart type and parameters, then the system generates an embed code (iframe/JavaScript)
- [ ] Given an embedded widget, then it updates automatically when new data is published
- [ ] Given widget usage, then analytics track where widgets are embedded and how often viewed

**Priority**: COULD_HAVE

---

#### FR-7: Data Quality Monitoring Dashboard

**Description**: The system must provide an internal dashboard showing data source status, ingestion health, quality scores, and publication readiness.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given 8+ data sources, then status shows last ingestion, next expected, and quality score
- [ ] Given a data quality issue, then alerts are sent to the data team
- [ ] Given publication readiness, then a workflow supports review and approval before public publication

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-1: Dashboard Response Time

**Requirement**: Dashboard pages load within 2 seconds (p95). Complex intersectional queries respond within 5 seconds (p95). Data pipeline ingestion completes within 4 hours per source.

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-1: 99.5% Availability

**Requirement**: 99.5% uptime (44 hours maximum downtime per year). This is primarily an analytical platform — brief planned downtime is acceptable with notice.

**RTO**: 8 hours | **RPO**: 24 hours

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-1: Data Classification

**Requirement**: All published data is OFFICIAL (aggregate statistics). Source data from HESA/UKRI may be OFFICIAL-SENSITIVE during processing and must be handled accordingly until aggregated.

**Priority**: MUST_HAVE

---

#### NFR-SEC-2: Statistical Disclosure Control

**Requirement**: All published data must pass statistical disclosure control — no cell with fewer than 5 individuals published. Complementary suppression applied to prevent derivation.

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-1: Code of Practice for Statistics

**Requirement**: The dashboard and its publications must comply with the UK Statistics Authority Code of Practice for Statistics (trustworthiness, quality, value) to support potential designation as Official Statistics.

**Priority**: SHOULD_HAVE

---

#### NFR-C-2: WCAG 2.2 Level AA

**Requirement**: All public-facing components must meet WCAG 2.2 Level AA. Interactive visualisations must have accessible alternatives (data tables, screen-reader-compatible summaries).

**Priority**: MUST_HAVE

---

#### NFR-C-3: Open Government Licence

**Requirement**: All published data licensed under the Open Government Licence v3.0.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Integration with HESA Data

**Purpose**: Ingest higher education student and staff data disaggregated by gender, subject, level, and institution.

**Integration Type**: Annual batch (HESA open data API or data sharing agreement for enhanced data)

**Data Exchanged**: Student enrolment, completion, degree classification by gender and STEM subject; staff data by gender, grade, and discipline

**Priority**: MUST_HAVE

---

### INT-2: Integration with UKRI Funding Data

**Purpose**: Ingest research funding application and award data disaggregated by gender.

**Integration Type**: Annual batch (UKRI open data or data sharing agreement)

**Priority**: MUST_HAVE

---

### INT-3: Integration with DfE Education Data

**Purpose**: Ingest GCSE and A-level subject entry data disaggregated by gender.

**Integration Type**: Annual batch (DfE Statistics publication API)

**Priority**: MUST_HAVE

---

### INT-4: Integration with ONS Labour Force Survey

**Purpose**: Ingest STEM workforce data disaggregated by gender, sector, and occupation.

**Integration Type**: Quarterly batch (ONS API or published datasets)

**Priority**: MUST_HAVE

---

### INT-5: Integration with Eurostat/OECD

**Purpose**: Ingest international STEM gender diversity data for benchmarking.

**Integration Type**: Annual batch (Eurostat She Figures, OECD indicators)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Key Data Entities

#### Entity: Pipeline Stage Data Point

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| data_point_id | UUID | Yes | Unique identifier |
| pipeline_stage | Enum | Yes | GCSE/A-level/UG/PGT/PGR/early_career/workforce/leadership |
| stem_discipline | Enum | Yes | physical_sciences/biological_sciences/engineering/computing/mathematics/all_stem |
| year | Integer | Yes | Data collection year |
| gender | Enum | Yes | female/male/other/unknown |
| count | Integer | Yes | Number of individuals |
| percentage | Decimal(5,2) | Yes | Percentage of gender within stage/discipline |
| source | String | Yes | Data source (HESA/UKRI/DfE/ONS/etc.) |
| ethnicity | String | No | Ethnic group (for intersectional analysis) |
| disability | Boolean | No | Disability status |
| region | String | No | Geographic region |

**Data Classification**: OFFICIAL (aggregate) / OFFICIAL-SENSITIVE (individual-level source data during processing)

**Data Retention**: Published aggregate data retained indefinitely for trend analysis. Source data retained per DSA terms.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Pipeline stages with data | Fragmented across sources | 8+ stages | 12 months |
| Data publication lag | 12-24 months | 6 months maximum | 12 months |
| Monthly unique visitors | 0 | 25,000 | 12 months |
| Open data API consumers | 0 | 100+ | 18 months |
| Citation as primary source | Multiple competing sources | 80%+ of government STEM diversity publications | 24 months |
| Intersectional dimensions | Not available | 3+ dimensions | 18 months |
| Partner embedding widgets | 0 | 20+ organisations | 24 months |

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use GOV.UK Design System for public-facing dashboard
**TC-2**: Must comply with ONS statistical disclosure control guidelines
**TC-3**: Must deploy to UK government cloud infrastructure

### Business Constraints

**BC-1**: Budget cap of GBP 3.5M total programme cost over 3 years
**BC-2**: Must be operational with initial data sources within 12 months
**BC-3**: Data sharing agreements with HESA and UKRI must be in place before enhanced data can be ingested

### Assumptions

**A-1**: HESA, UKRI, and DfE will agree to data sharing arrangements within 6 months
**A-2**: ONS Labour Force Survey data remains publicly available
**A-3**: Professional bodies (BCS, IET) will contribute workforce data voluntarily
**A-4**: Eurostat She Figures data is available under compatible licensing

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Women in STEM Tracking Dashboard (Project 004)
**Model**: Claude Opus 4.6
