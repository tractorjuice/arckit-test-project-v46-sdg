# Project Requirements: Net Zero Tracking Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Net Zero Tracking Dashboard (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Net Zero Dashboard |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Dashboard Programme Board, DESNZ Digital, CCC Secretariat, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Net Zero Tracking Dashboard — a public-facing digital service providing authoritative tracking of UK progress towards its legally binding net zero by 2050 target and interim carbon budget milestones.

---

## Executive Summary

### Business Context

The UK's Climate Change Act 2008 (as amended) sets a legally binding target of net zero greenhouse gas emissions by 2050, with five-yearly carbon budgets providing interim milestones. The Climate Change Committee publishes annual progress reports, but no single government service provides an integrated, real-time view of UK emissions performance against these targets. The Net Zero Tracking Dashboard will consolidate emissions data from the National Atmospheric Emissions Inventory (NAEI), DESNZ energy statistics, and sectoral sources into a single authoritative dashboard.

### Objectives

- Provide a single, CCC-endorsed, publicly accessible view of UK net zero progress
- Track emissions performance against the Sixth Carbon Budget (2033-2037) and subsequent budgets
- Enable sectoral analysis across the seven NAEI sectors (energy supply, business, transport, public, residential, agriculture, LULUCF)
- Deliver open, machine-readable data via public API
- Meet GDS Service Standard and WCAG 2.2 Level AA accessibility requirements

### Expected Outcomes

- CCC references dashboard data in its 2027 annual progress report
- 500+ API consumers within 6 months of launch
- Dashboard becomes the primary UK net zero data source cited in media, academic, and NGO analysis
- Reduced duplication of emissions tracking across government departments

### Project Scope

**In Scope**:

- UK territorial greenhouse gas emissions tracking (all Kyoto basket gases: CO2, CH4, N2O, HFCs, PFCs, SF6, NF3)
- Sectoral breakdown aligned with NAEI categories
- Carbon budget tracking (4th, 5th, 6th Carbon Budgets)
- Devolved nation views (England, Scotland, Wales, Northern Ireland)
- Public API for data access
- Open data publication under Open Government Licence

**Out of Scope**:

- Consumption-based emissions (scope 3 / imported emissions)
- Real-time emissions monitoring (satellite or sensor data)
- Company-level emissions disclosure
- Policy effectiveness modelling or forecasting
- International comparisons (Phase 2)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | DESNZ | Decision maker |
| Service Owner | Service accountability | DESNZ | Requirements definition |
| Chief Statistician | Methodology governance | DESNZ | Methodology approval |
| CCC Secretariat | Independent scrutiny | CCC | Methodology co-creation |
| Product Manager | Feature prioritisation | DESNZ Digital | Requirements elicitation |
| Data Architect | Data pipeline design | DESNZ Digital | Technical oversight |
| DEFRA Climate Team | LULUCF and agriculture data | DEFRA | Data provider |
| Met Office | Climate projections | Met Office | Data provider |

---

## Business Requirements

### BR-001: Authoritative Net Zero Progress Tracking

**Description**: Provide a single, authoritative view of UK greenhouse gas emissions performance against legally binding carbon budgets and the net zero 2050 target.

**Rationale**: Multiple government bodies produce emissions data (NAEI, DESNZ statistics, devolved inventories) creating confusion. A single dashboard endorsed by the CCC eliminates contradictory narratives.

**Success Criteria**:

- Dashboard data reconciles with published DESNZ official statistics (within rounding tolerance)
- CCC endorses methodology and references dashboard in annual progress report
- Dashboard becomes the most-cited government source for UK emissions data

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State for Energy Security and Net Zero

---

### BR-002: Sectoral Emissions Analysis

**Description**: Enable analysis of emissions by sector (energy supply, business, transport, public, residential, agriculture, LULUCF) and sub-sector to identify areas of progress and concern.

**Rationale**: Net zero progress is uneven across sectors. Policy makers, CCC, and NGOs need sectoral granularity to assess which sectors are on track and which require policy intervention.

**Success Criteria**:

- Seven NAEI sectors displayed with trend analysis from 1990 baseline
- Sub-sector drill-down available for at least the three largest emitting sectors
- Year-on-year change rates calculated and displayed

**Priority**: MUST_HAVE

**Stakeholder**: CCC, DESNZ Climate Analysis Team

---

### BR-003: Carbon Budget Tracking

**Description**: Track cumulative emissions against the statutory carbon budget limits set by the Climate Change Act 2008.

**Rationale**: Carbon budgets are the primary legal mechanism for driving emissions reductions. Tracking cumulative emissions against budget limits enables assessment of whether the UK is on track to meet legally binding targets.

**Success Criteria**:

- 4th (2023-2027), 5th (2028-2032), and 6th (2033-2037) Carbon Budgets displayed
- Cumulative emissions tracked against budget limits with remaining budget calculation
- Projected trajectory based on current reduction rate displayed alongside actual emissions

**Priority**: MUST_HAVE

**Stakeholder**: CCC, Secretary of State

---

### BR-004: Open Data Access

**Description**: Provide all dashboard data as open data via public API and downloadable datasets under the Open Government Licence.

**Rationale**: Environmental Information Regulations 2004 create a presumption of disclosure. Open data enables academic research, NGO scrutiny, and private sector innovation.

**Success Criteria**:

- Public REST API with documented endpoints serving all dashboard data
- Downloadable datasets in CSV, JSON, and machine-readable formats
- All data published under Open Government Licence v3.0
- API documentation published on GOV.UK API catalogue

**Priority**: MUST_HAVE

**Stakeholder**: Environmental NGOs, Academic researchers

---

### BR-005: Devolved Nation Views

**Description**: Provide separate views for England, Scotland, Wales, and Northern Ireland showing emissions against their respective statutory targets and baselines.

**Rationale**: Each devolved nation has separate statutory targets and emissions inventories. A UK-wide dashboard must respect these frameworks.

**Success Criteria**:

- Separate nation pages showing emissions against nation-specific targets
- Scotland's 2045 net zero target and annual targets displayed
- Wales's carbon budget pathway displayed
- Northern Ireland's Climate Change Act targets displayed

**Priority**: SHOULD_HAVE

**Stakeholder**: Devolved Administrations

---

## Functional Requirements

### User Personas

#### Persona 1: Policy Analyst

- **Role**: DESNZ / DEFRA climate policy analyst
- **Goals**: Assess sectoral emissions trends, identify policy gaps, prepare Ministerial briefings
- **Pain Points**: Currently manually compiles data from multiple DESNZ publications
- **Technical Proficiency**: High

#### Persona 2: CCC Researcher

- **Role**: CCC progress report analyst
- **Goals**: Verify UK emissions data, compare against CCC's own analysis, identify discrepancies
- **Pain Points**: Reconciling different data sources and methodologies
- **Technical Proficiency**: High

#### Persona 3: Journalist / Public User

- **Role**: Environment correspondent or interested citizen
- **Goals**: Understand UK climate progress, find headline figures, download data for articles
- **Pain Points**: Current data is buried in statistical publications and difficult to interpret
- **Technical Proficiency**: Low to Medium

#### Persona 4: NGO Data Analyst

- **Role**: Climate data analyst at environmental NGO
- **Goals**: Download structured data, run independent analysis, challenge government claims
- **Pain Points**: Manual data extraction from PDF/Excel, inconsistent formats across sources
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: National Emissions Summary

**Description**: Display UK total greenhouse gas emissions for the most recent year available, with comparison to the 1990 baseline and the previous year.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:

- [ ] Given the dashboard homepage, when a user lands, then they see the latest UK total emissions in MtCO2e
- [ ] Given the latest data, when displayed, then the percentage change from 1990 baseline is shown
- [ ] Given the latest data, when displayed, then the percentage change from the previous year is shown
- [ ] Given the emissions figure, when hovered/clicked, then the data source and publication date are shown

**Priority**: MUST_HAVE

---

#### FR-002: Sectoral Emissions Breakdown

**Description**: Display emissions breakdown by the seven NAEI sectors with interactive charts and data tables.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given the sectoral view, when a user navigates to it, then all seven NAEI sectors are displayed
- [ ] Given each sector, when displayed, then the emissions figure, percentage of total, and trend direction are shown
- [ ] Given a sector, when a user clicks on it, then sub-sector breakdown is shown (for sectors with sub-sectors)
- [ ] Given the sectoral view, when accessed, then an accessible data table alternative to charts is available

**Priority**: MUST_HAVE

---

#### FR-003: Carbon Budget Progress Tracker

**Description**: Display cumulative emissions against carbon budget limits with progress bars and trajectory projections.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given the carbon budget view, when a user navigates to it, then the 4th, 5th, and 6th Carbon Budgets are displayed
- [ ] Given a carbon budget period, when active, then cumulative emissions are shown against the budget limit
- [ ] Given current emissions trajectory, when projected, then estimated end-of-period emissions are calculated
- [ ] Given a budget at risk of being exceeded, when projected overshoot detected, then a clear warning is displayed

**Priority**: MUST_HAVE

---

#### FR-004: Time Series Chart

**Description**: Display interactive time series chart of UK emissions from 1990 to latest year with selectable gases and sectors.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Given the time series view, when a user navigates to it, then a chart showing 1990-present emissions is displayed
- [ ] Given the chart, when a user selects specific gases, then the chart updates to show selected gases only
- [ ] Given the chart, when a user selects specific sectors, then the chart updates to show selected sectors only
- [ ] Given the chart, when a user hovers over a data point, then the exact value and year are displayed
- [ ] Given the chart, when an accessible alternative is needed, then a data table view is available

**Priority**: MUST_HAVE

---

#### FR-005: Public API

**Description**: Provide a RESTful API serving all dashboard data with documented endpoints, versioning, and rate limiting.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given the API, when a user requests emissions data, then JSON response is returned within 500ms
- [ ] Given the API, when filtering by year/sector/gas/nation, then the appropriate subset is returned
- [ ] Given the API, when version v1 is specified, then backward-compatible responses are guaranteed
- [ ] Given the API, when rate limit exceeded, then a clear 429 response with retry-after header is returned
- [ ] Given the API, when accessed, then no authentication is required for public data

**Priority**: MUST_HAVE

---

#### FR-006: Data Download

**Description**: Enable users to download dashboard data in CSV, JSON, and ODS formats.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given any data view, when a user clicks download, then data is available in CSV, JSON, and ODS formats
- [ ] Given a download, when generated, then metadata headers include data source, publication date, and licence
- [ ] Given a download, when opened in spreadsheet software, then column headers are clear and data is correctly formatted

**Priority**: MUST_HAVE

---

#### FR-007: Devolved Nation Dashboard

**Description**: Provide separate dashboard views for England, Scotland, Wales, and Northern Ireland with nation-specific targets and baselines.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given the nation selector, when a user selects Scotland, then Scotland's emissions are shown against the 2045 target
- [ ] Given the nation selector, when a user selects Wales, then Wales's emissions are shown against its carbon budget pathway
- [ ] Given a nation view, when comparing to UK total, then the nation's share of UK emissions is shown

**Priority**: SHOULD_HAVE

---

#### FR-008: Methodology Documentation

**Description**: Publish comprehensive methodology documentation alongside the dashboard explaining data sources, calculations, and limitations.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given the methodology page, when accessed, then it explains all data sources, calculation methods, and limitations
- [ ] Given any dashboard figure, when clicked for more info, then a link to the relevant methodology section is provided
- [ ] Given the methodology, when reviewed by CCC, then it is endorsed as transparent and reproducible

**Priority**: MUST_HAVE

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Page Load Time

**Requirement**: Dashboard pages must load within 2 seconds at 95th percentile on a standard broadband connection.

**Measurement Method**: Synthetic monitoring from 3 UK locations

**Priority**: MUST_HAVE

#### NFR-P-002: API Response Time

**Requirement**: API responses must be returned within 500ms at 95th percentile for standard queries.

**Measurement Method**: API monitoring with latency tracking

**Priority**: MUST_HAVE

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.9% uptime (maximum 8.7 hours downtime per year), with enhanced availability during CCC progress report publication weeks and COP events.

**Priority**: MUST_HAVE

#### NFR-A-002: Disaster Recovery

**RPO**: 1 hour | **RTO**: 4 hours

**Priority**: MUST_HAVE

### Security Requirements

#### NFR-SEC-001: Data Classification

**Requirement**: All published dashboard data is OFFICIAL (public). Administration interfaces OFFICIAL-SENSITIVE with MFA.

**Priority**: MUST_HAVE

#### NFR-SEC-002: API Security

**Requirement**: Public API requires no authentication. Rate limiting at 1,000 requests per hour per IP. Admin API requires OAuth 2.0 with MFA.

**Priority**: MUST_HAVE

### Accessibility Requirements

#### NFR-U-001: WCAG Compliance

**Requirement**: WCAG 2.2 Level AA compliance. All charts must have accessible data table alternatives. Colour is not used as the sole means of conveying information.

**Priority**: MUST_HAVE (legal requirement)

#### NFR-U-002: GDS Design System

**Requirement**: Dashboard must use the GOV.UK Design System and GOV.UK Frontend components.

**Priority**: MUST_HAVE

### Compliance Requirements

#### NFR-C-001: Environmental Information Regulations

**Requirement**: All environmental data must be proactively disclosed under EIR 2004. Exemptions documented.

**Priority**: MUST_HAVE

#### NFR-C-002: Official Statistics Code

**Requirement**: Dashboard must not breach the UK Statistics Authority Code of Practice for Statistics. Publication coordinated with DESNZ statistical release calendar.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: NAEI Data Integration

**Purpose**: Consume UK greenhouse gas emissions inventory data as the authoritative emissions source.

**Integration Type**: Batch file transfer (annual, with quarterly provisional updates)

**Data Exchanged**: UK territorial emissions by gas, sector, sub-sector, and year (1990-present)

**Priority**: MUST_HAVE

### INT-002: DESNZ Energy Statistics

**Purpose**: Consume energy consumption and production data for energy-related emissions context.

**Integration Type**: Scheduled data feed (quarterly)

**Data Exchanged**: Energy consumption by fuel type, sector, and region

**Priority**: SHOULD_HAVE

### INT-003: Devolved Administration Inventories

**Purpose**: Consume Scotland, Wales, and Northern Ireland emissions inventories for nation-level views.

**Integration Type**: Batch file transfer (annual)

**Data Exchanged**: Devolved nation emissions by sector and year

**Priority**: SHOULD_HAVE

### INT-004: GOV.UK Publishing

**Purpose**: Publish methodology documentation on GOV.UK alongside the dashboard.

**Integration Type**: Content API

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Emissions Record

**Description**: A single emissions measurement for a specific gas, sector, year, and geographic area.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| id | UUID | Yes | Unique identifier | Primary key |
| year | Integer | Yes | Reporting year | 1990-present |
| gas | Enum | Yes | Greenhouse gas | CO2, CH4, N2O, HFCs, PFCs, SF6, NF3 |
| sector | String | Yes | NAEI sector code | NAEI sector taxonomy |
| sub_sector | String | No | NAEI sub-sector code | NAEI sub-sector taxonomy |
| nation | Enum | Yes | Geographic area | UK, England, Scotland, Wales, NI |
| value_mtco2e | Decimal | Yes | Emissions in MtCO2e | >= 0 |
| data_source | String | Yes | Source identifier | NAEI, DESNZ, devolved |
| publication_date | Date | Yes | When data was published | ISO 8601 |

**Data Volume**: Approximately 50,000 records (35 years x 7 gases x ~20 sectors x 5 nations)

#### Entity 2: Carbon Budget

**Description**: A statutory carbon budget period with its emissions limit.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| id | UUID | Yes | Unique identifier | Primary key |
| budget_number | Integer | Yes | Carbon budget number | 1-6+ |
| start_year | Integer | Yes | Budget period start | e.g., 2033 |
| end_year | Integer | Yes | Budget period end | e.g., 2037 |
| limit_mtco2e | Decimal | Yes | Budget limit in MtCO2e | e.g., 965 |
| cumulative_actual | Decimal | No | Cumulative actual emissions | Calculated |

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| CCC endorsement | No endorsement | Formal endorsement | 6 months | CCC correspondence |
| API consumers | 0 | 500+ | 12 months post-launch | API analytics |
| Media citations | N/A | Most-cited gov climate source | 18 months | Media monitoring |
| User satisfaction | N/A | 4.2/5.0 | 6 months post-launch | GDS satisfaction survey |

---

## Approval

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, DESNZ | _________ | PENDING |
| Chief Statistician, DESNZ | _________ | PENDING |
| CCC Secretariat Representative | _________ | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Climate Change Act 2008 | Legislation | legislation.gov.uk | Net zero target, carbon budgets | N/A |
| NAEI | Data | naei.beis.gov.uk | UK emissions inventory | N/A |
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A |
| WCAG 2.2 | Standard | W3C | Accessibility criteria | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Net Zero Tracking Dashboard (Project 001)
**Model**: Claude Opus 4.6
