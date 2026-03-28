# Project Requirements: National Food Strategy Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | National Food Strategy Dashboard (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, Cabinet Office Food Strategy Unit |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office, DEFRA, DfE, No. 10 Policy Unit, ONS |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the National Food Strategy Dashboard, covering data aggregation from SDG 2 source projects, KPI calculation, internal and public-facing dashboards, and ministerial reporting. Traceable to ARC-005-STKE-v1.0 and aligned with ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

The Government Food Strategy 2022 (responding to the Dimbleby National Food Strategy review) set out commitments across multiple departments: DEFRA (food production, waste, supply chains), DfE (school meals), DHSC (diet and health), and others. Currently there is no single view of progress against these commitments. Ministerial questions about food strategy delivery require days of manual data gathering across departments. Parliament, media, and the public have no accessible way to track government performance.

The National Food Strategy Dashboard will aggregate data from the four SDG 2 operational projects (001-004) and wider published sources (ONS food statistics, WRAP waste data, FSA food safety data) into a coherent monitoring platform. It will serve two audiences: internal government users (ministers, policy teams, No. 10) needing rapid access to food system KPIs, and the public requiring transparent performance reporting.

### Objectives

- Aggregate food system KPIs from Projects 001-004 and external data sources into a single platform
- Enable ministerial food strategy questions to be answered within 5 minutes (vs current 3+ days)
- Publish a public-facing dashboard on GOV.UK showing progress against Food Strategy commitments
- Provide alerting on deteriorating food system indicators for proactive policy intervention
- Deliver methodology-compliant metrics reviewed by ONS

### Expected Outcomes

- 50+ KPIs tracked across food supply, school meals, waste, agriculture, and nutrition
- Ministerial briefing preparation time reduced from 3+ days to < 5 minutes
- Public dashboard attracting 10,000+ quarterly visits
- FOI requests about food strategy progress reduced by 50%
- Cross-government policy coordination improved through shared data visibility

### Project Scope

**In Scope**:

- Data aggregation platform consuming APIs from Projects 001-004
- Internal government dashboard for ministers and policy teams
- Public-facing GOV.UK dashboard for citizens
- KPI calculation engine with methodology documentation
- Alerting system for deteriorating indicators
- Ministerial briefing pack auto-generation
- Integration with ONS for statistical methodology compliance

**Out of Scope**:

- Diet and health metrics (DHSC responsibility, data feed considered for Phase 2)
- Food pricing indices (ONS existing responsibility)
- International food system comparison (FAO responsibility)
- Operational management of source projects (001-004)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO, Food Strategy Dashboard | Programme Sponsor | Cabinet Office | Decision maker |
| Cabinet Office CDO | Architecture Oversight | Cabinet Office | Technical governance |
| Director, Food Strategy Unit | Strategic Direction | Cabinet Office | KPI selection |
| No. 10 Policy Unit | Strategic User | No. 10 | User requirements |
| DEFRA Data Liaison (Projects 001, 003, 004) | Data Provider | DEFRA | API specifications |
| DfE Data Liaison (Project 002) | Data Provider | DfE | API specifications |
| ONS Methodology Team | Statistical Quality | ONS | Methodology review |
| GDS Design Team | User Experience | GDS | GOV.UK Design System |
| CDDO Assessment Team | Standards Assurance | CDDO | Service assessment |

---

## Business Requirements

### BR-001: Cross-Government KPI Aggregation

**Description**: The platform must aggregate food system KPIs from all four SDG 2 source projects and external published data sources into a single authoritative dataset.

**Rationale**: No single view of food system performance exists. Data is scattered across departments, published on different schedules, and presented in incompatible formats.

**Success Criteria**:

- Data feeds from all 4 source projects operational
- Minimum 50 KPIs covering all food strategy commitment areas
- Data refresh: operational data weekly, statistical data quarterly
- Single source of truth for food strategy metrics (ARC-000-PRIN-v1.0 Principle 10)

**Priority**: MUST_HAVE

---

### BR-002: Ministerial Rapid Briefing

**Description**: The platform must enable policy teams to answer ministerial food strategy questions within 5 minutes, with auto-generated briefing packs.

**Rationale**: Current response time of 3+ days for cross-departmental data gathering is unacceptable for parliamentary questions and media enquiries.

**Success Criteria**:

- Ministerial briefing pack generated in < 2 minutes from dashboard
- Briefing covers all relevant KPIs with trend analysis
- Customisable briefing templates for different audiences (PM, Select Committee, media)

**Priority**: MUST_HAVE

---

### BR-003: Public Transparency Dashboard

**Description**: The platform must publish a citizen-facing dashboard on GOV.UK showing government progress against Food Strategy commitments.

**Rationale**: Open government commitment and Dimbleby Review recommendation for food system transparency. Reduces FOI burden.

**Success Criteria**:

- Dashboard published on GOV.UK following GDS design patterns
- Quarterly data refresh for public metrics
- Clear methodology notes and data source attribution
- WCAG 2.2 Level AA accessibility compliance
- Plain English explanations of all KPIs

**Priority**: SHOULD_HAVE

---

### BR-004: Proactive Alerting

**Description**: The platform must detect deteriorating food system indicators and alert policy teams and No. 10 before issues become politically visible.

**Rationale**: Number 10 has been caught off-guard by food system issues. Proactive alerting enables pre-emptive policy response.

**Success Criteria**:

- Configurable alert thresholds for each KPI
- Alert notification via email and platform notification
- Alert severity classification (critical, high, medium, information)
- Monthly trend analysis identifying emerging concerns

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Cabinet Office Policy Analyst

- **Role**: Food Strategy Unit analyst
- **Goals**: Monitor food system KPIs, prepare ministerial briefings, identify emerging issues
- **Pain Points**: Currently spends days gathering data from multiple departments
- **Technical Proficiency**: Medium

#### Persona 2: No. 10 Policy Adviser

- **Role**: PM's Policy Unit adviser covering food/agriculture
- **Goals**: Quick overview of food system health, early warning of problems, briefing material
- **Pain Points**: No single view; relies on ad-hoc departmental submissions
- **Technical Proficiency**: Low (needs pre-formatted outputs)

#### Persona 3: Citizen

- **Role**: Member of the public interested in food policy
- **Goals**: Understand government performance on food strategy, access data for research/journalism
- **Pain Points**: Data scattered across multiple GOV.UK publications
- **Technical Proficiency**: Variable

---

### Functional Requirements Detail

#### FR-001: Data Aggregation Engine

**Description**: The system must ingest data from source project APIs and external published data sources, normalising formats and storing in a unified data warehouse.

**Acceptance Criteria**:

- [ ] Given a source project API (Projects 001-004), when data is available, then it is ingested within the defined refresh schedule
- [ ] Given external data sources (ONS, WRAP), when published data is updated, then the platform ingests the new data within 48 hours
- [ ] Given data ingestion failure, when a source is unavailable, then the last-known-good data is retained with a staleness indicator
- [ ] Given heterogeneous data formats, when ingested, then data is normalised to the platform's KPI data model

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-002: KPI Calculation Engine

**Description**: The system must calculate derived KPIs from raw source data, applying agreed methodology and producing trend analysis.

**Acceptance Criteria**:

- [ ] Given raw data from source projects, when KPI calculations run, then derived metrics are produced with confidence intervals
- [ ] Given time-series data, when trend analysis is requested, then year-on-year and quarter-on-quarter comparisons are displayed
- [ ] Given a KPI methodology change, when applied, then historical data is recalculated for comparability
- [ ] Given KPI methodology, when documented, then ONS-compliant methodology notes are published

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-003: Internal Government Dashboard

**Description**: The system must provide an interactive dashboard for government users with drill-down from headline food strategy KPIs to departmental detail.

**Acceptance Criteria**:

- [ ] Given an authenticated government user, when accessing the dashboard, then headline KPIs are displayed with traffic-light status
- [ ] Given a headline KPI, when clicked, then departmental breakdown and contributing metrics are shown
- [ ] Given a time range selector, when adjusted, then all metrics update to reflect the selected period
- [ ] Given dashboard filters (department, region, KPI category), when applied, then data is filtered in < 3 seconds

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-004: Ministerial Briefing Generator

**Description**: The system must auto-generate formatted ministerial briefing packs from dashboard data.

**Acceptance Criteria**:

- [ ] Given a briefing template, when generated, then all KPIs are populated with current data and trend arrows
- [ ] Given customisable briefing scope, when selected, then only relevant KPIs and departments are included
- [ ] Given a generated briefing, when exported, then it is available in PDF and DOCX format
- [ ] Given briefing generation, when requested, then it completes within 2 minutes

**Priority**: MUST_HAVE

**Complexity**: LOW

---

#### FR-005: Public Dashboard

**Description**: The system must provide a GOV.UK-hosted public dashboard showing food strategy progress.

**Acceptance Criteria**:

- [ ] Given any citizen, when visiting the public dashboard, then no authentication is required
- [ ] Given public KPIs, when displayed, then plain English descriptions and methodology links are provided
- [ ] Given data download, when requested, then CSV/ODS/JSON formats are available
- [ ] Given accessibility, when tested, then WCAG 2.2 Level AA compliance is confirmed
- [ ] Given data caveats, when applicable, then they are prominently displayed

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Alerting and Notification

**Description**: The system must detect KPI threshold breaches and trend deterioration, sending alerts to configured recipients.

**Acceptance Criteria**:

- [ ] Given a KPI threshold configuration, when the threshold is breached, then an alert is generated
- [ ] Given a sustained negative trend (3+ consecutive periods), when detected, then a trend alert is generated
- [ ] Given an alert, when generated, then notification is sent via email (GOV.UK Notify) and platform notification
- [ ] Given alert configuration, when managed by policy team, then thresholds are adjustable without developer involvement

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-007: Data Quality Monitoring

**Description**: The system must monitor the health, freshness, and quality of all source data feeds.

**Acceptance Criteria**:

- [ ] Given a data feed, when health is monitored, then availability, freshness, and completeness are tracked
- [ ] Given a data feed failure, when detected, then an operational alert is raised and stakeholders notified
- [ ] Given data quality metrics, when displayed, then a data health dashboard shows feed status for all sources

**Priority**: MUST_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements

### NFR-P-1: Performance

- Internal dashboard page load: < 3 seconds (p95)
- Public dashboard page load: < 2 seconds (p95)
- Briefing generation: < 2 minutes
- Data refresh: within 24 hours of source update

**Peak load**: 1,000 concurrent users for public dashboard during policy announcements

**Priority**: HIGH

---

### NFR-A-1: Availability

**Internal dashboard**: 99.5% uptime

**Public dashboard**: 99.9% uptime (citizen-facing service)

**RTO**: Internal 4 hours, Public 1 hour | **RPO**: 1 hour

**Priority**: HIGH

---

### NFR-SEC-1: Authentication

**Internal dashboard**: Cross-government SSO (Azure AD federation). No. 10 users via Cabinet Office AD.

**Public dashboard**: No authentication required (open data).

**Priority**: HIGH

---

### NFR-SEC-2: Data Classification

**Requirement**: All data published on the public dashboard must be classified OFFICIAL-PUBLIC and approved for publication by the Food Strategy Unit. Internal dashboard may display OFFICIAL data not yet approved for public release.

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility and Design

**Requirement**: GOV.UK Design System compliance for public dashboard. WCAG 2.2 Level AA. Data visualisations must work without JavaScript (progressive enhancement). Plain English content at reading age 9 per GOV.UK content guidelines.

**Priority**: CRITICAL

---

## Integration Requirements

#### INT-001: Food Supply Chain Resilience Platform (Project 001)

**Purpose**: Consume supply chain risk scores, food category status, and alert summaries.

**Data**: Supply chain risk metrics, alert counts, coverage statistics

**Frequency**: Weekly data refresh

**Priority**: MUST_HAVE

---

#### INT-002: School Meals Management System (Project 002)

**Purpose**: Consume FSM uptake metrics, eligibility gap data, and Pupil Premium statistics.

**Data**: FSM registration counts by LA/region/demographic, eligibility gap percentage, auto-enrolment rates

**Frequency**: Weekly data refresh (term-time), monthly summary

**Priority**: MUST_HAVE

---

#### INT-003: Food Waste Reduction Analytics (Project 003)

**Purpose**: Consume food waste metrics and SDG 12.3 progress data.

**Data**: Total food waste by supply chain stage, waste hierarchy breakdown, year-on-year trend

**Frequency**: Quarterly data refresh

**Priority**: MUST_HAVE

---

#### INT-004: Agricultural Subsidy Management (Project 004)

**Purpose**: Consume ELM scheme uptake, payment statistics, and environmental outcome metrics.

**Data**: ELM agreement counts, payment values, uptake by scheme/region, environmental outcome indicators

**Frequency**: Monthly data refresh

**Priority**: MUST_HAVE

---

#### INT-005: ONS Food Statistics

**Purpose**: Ingest published food-related statistics (food security, household expenditure, nutrition).

**Data**: Family Food Survey data, Living Costs and Food Survey, food price indices

**Frequency**: On publication (annual/quarterly)

**Priority**: SHOULD_HAVE

---

#### INT-006: GOV.UK Notify

**Purpose**: Send alert notifications to policy teams.

**Priority**: SHOULD_HAVE

---

## Data Requirements

### KPI Framework

| Domain | Example KPIs | Source | Refresh |
|--------|-------------|--------|---------|
| Supply Chain | Supply chain coverage %, risk score trends, alert counts | Project 001 | Weekly |
| School Meals | FSM uptake %, eligibility gap %, auto-enrolment rate | Project 002 | Weekly |
| Food Waste | Total food waste (Mt), SDG 12.3 progress %, waste hierarchy mix | Project 003 | Quarterly |
| Agriculture | ELM uptake %, payment accuracy %, environmental outcomes | Project 004 | Monthly |
| Food Security | Household food insecurity %, food price inflation | ONS/DEFRA | Quarterly |

### Key Data Entities

#### Entity 1: KPI Definition

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| kpi_id | UUID | Yes | Unique identifier |
| name | String(255) | Yes | KPI display name |
| domain | Enum | Yes | Supply Chain / School Meals / Waste / Agriculture / Security |
| methodology | Text | Yes | Calculation methodology (ONS-reviewed) |
| source_project | Enum | Yes | Project 001-004 or External |
| unit | String(50) | Yes | Unit of measurement |
| target_value | Decimal | No | Government target (if defined) |
| alert_threshold | Decimal | No | Alert trigger threshold |
| public_visibility | Boolean | Yes | Whether published on public dashboard |

#### Entity 2: KPI Data Point

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| datapoint_id | UUID | Yes | Unique identifier |
| kpi_id | UUID | Yes | KPI reference |
| period | DateRange | Yes | Reporting period |
| value | Decimal | Yes | KPI value |
| confidence_interval | Decimal | No | Statistical confidence |
| source_timestamp | Timestamp | Yes | When source data was produced |
| ingested_at | Timestamp | Yes | When platform received data |

**Data Volume**: ~250,000 data points/year (50 KPIs x multiple geographies x weekly/monthly/quarterly)

**Data Classification**: OFFICIAL (internal); OFFICIAL-PUBLIC (public dashboard subset)

---

## Constraints and Assumptions

**TC-1**: Must deploy to Cabinet Office approved cloud environment.

**TC-2**: Public dashboard must be hosted on GOV.UK infrastructure.

**TC-3**: Data feeds from source projects dependent on those projects' delivery timelines.

**BC-1**: Budget capped at £4.5M over 3 years.

**BC-2**: Public dashboard must have ministerial sign-off before publication.

**A-1**: Source projects (001-004) will deliver APIs on agreed schedules (risk: delays propagate to dashboard).

**A-2**: ONS will provide methodology review within 3 months of request (risk: ONS resource constraints).

**A-3**: GOV.UK publishing team will support dashboard hosting (risk: GOV.UK platform limitations for interactive content).

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Time to answer ministerial food strategy question | 3+ days | < 5 minutes | Q2 2028 |
| KPIs tracked | 0 | 50+ | Q3 2028 |
| Source project API feeds operational | 0/4 | 4/4 | Q3 2028 |
| Public dashboard quarterly visits | 0 | 10,000+ | Q1 2029 |
| FOI request reduction (food strategy) | Baseline TBD | -50% | Q4 2029 |

---

## Timeline and Milestones

| Milestone | Target Date | Dependencies |
|-----------|-------------|--------------|
| Discovery Complete | Q3 2026 | Budget approval |
| Alpha Assessment (GDS) | Q1 2027 | KPI framework agreed with ONS |
| Internal Dashboard MVP | Q2 2028 | At least 2 source project APIs live |
| All Source APIs Connected | Q3 2028 | Projects 001-004 delivery |
| Public Dashboard Launch | Q4 2028 | ONS methodology review, ministerial approval |

---

## Budget

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Platform development | £2.0M | Data aggregation, dashboards, briefing engine |
| Integration with source projects | £0.8M | API consumption, data normalisation |
| GOV.UK public dashboard | £0.5M | Public-facing design, accessibility |
| ONS methodology engagement | £0.2M | Statistical review and methodology documentation |
| Infrastructure (3 years) | £0.5M | Cloud hosting, GOV.UK |
| Security and compliance | £0.2M | Pen testing, data classification |
| Contingency (15%) | £0.3M | Risk buffer |
| **Total** | **£4.5M** | Over 3 years |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| KPI | Key Performance Indicator |
| Dimbleby Review | Independent National Food Strategy Review (2021) |
| Government Food Strategy | Government response to Dimbleby Review (2022) |
| GOV.UK | UK Government's digital platform |
| GDS | Government Digital Service |
| ONS | Office for National Statistics |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Architecture Principles
- ARC-005-STKE-v1.0 -- National Food Strategy Dashboard Stakeholder Analysis
- Government Food Strategy 2022
- National Food Strategy (Dimbleby Review) 2021
- UK Code of Practice for Statistics

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Food Strategy Dashboard
**Model**: Claude Opus 4.6
