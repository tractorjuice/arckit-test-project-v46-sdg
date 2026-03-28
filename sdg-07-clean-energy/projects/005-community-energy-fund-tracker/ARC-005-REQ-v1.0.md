# Project Requirements: Community Energy Fund Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Community Energy Fund Tracker (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Community Energy Fund Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Programme Board, Community Energy England, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Community Energy Fund Tracker — a platform for managing community renewable energy project funding, generation monitoring, and community benefit tracking across 1,000+ projects.

---

## Executive Summary

### Business Context

The UK has approximately 300+ community energy organisations operating 5,000+ renewable energy installations with a combined capacity of 300MW. These range from single rooftop solar panels on a village hall to multi-megawatt wind farms owned by community cooperatives. Government supports community energy through the Community Energy Fund, Rural Community Energy Fund, and local authority schemes. Currently, fund management is fragmented across spreadsheets, email correspondence, and inconsistent reporting formats. DESNZ cannot aggregate sector-wide performance data, community groups spend excessive volunteer time on administration, and the sector cannot demonstrate its collective impact to justify continued political and financial support.

### Objectives

- Provide a unified platform for managing 1,000+ community energy project grants
- Automate generation data collection from community energy installations
- Track community benefit disbursement and social impact
- Deliver a public-facing community energy impact dashboard
- Reduce project reporting burden by 60%

### Expected Outcomes

- 1,000+ projects tracked with total funding of £200M+
- 300 GWh annual community generation monitored automatically
- £30M annual community benefit disbursement visible and tracked
- 60% reduction in volunteer time spent on project administration
- Sector-wide data available for policy evaluation and public communications

### Project Scope

**In Scope**:
- Fund application and grant management workflow
- Project registration and milestone tracking
- Automated generation data collection (inverter/meter feeds)
- Community benefit tracking and reporting
- Public-facing impact dashboard
- DESNZ and funder reporting

**Out of Scope**:
- Community share offer platforms (Ethex, Crowdfunder)
- Planning permission applications
- Grid connection applications
- Energy supplier Feed-in Tariff / Smart Export Guarantee administration

---

## Business Requirements

### BR-1: Fund Application and Grant Management

**Description**: The platform must manage the full lifecycle of community energy fund applications — from initial expression of interest through application, assessment, approval, disbursement, and closedown.
**Success Criteria**: Support 500+ new applications per year across 3+ funding programmes; average time from application to decision <60 days
**Priority**: MUST_HAVE

### BR-2: Project Portfolio Management

**Description**: The platform must provide DESNZ and fund managers with a portfolio view of all funded community energy projects, their status, milestones, and financial position.
**Success Criteria**: Real-time portfolio dashboard; project health RAG status; financial tracking against budget
**Priority**: MUST_HAVE

### BR-3: Automated Generation Monitoring

**Description**: The platform must automatically collect generation data from community energy installations to eliminate manual reporting and provide accurate, timely generation statistics.
**Success Criteria**: 80% of projects with automated generation data collection; monthly generation reports without manual input
**Priority**: SHOULD_HAVE

### BR-4: Community Benefit Tracking

**Description**: The platform must track how community energy organisations disburse community benefit funds — fuel poverty payments, education programmes, community facility improvements, local reinvestment.
**Success Criteria**: 90% of funded projects reporting community benefit annually; public dashboard showing sector-wide community benefit
**Priority**: MUST_HAVE

### BR-5: Public Impact Dashboard

**Description**: The platform must provide a public-facing dashboard showing the collective impact of community energy — total generation, carbon reduction, community benefit disbursement, and project locations.
**Success Criteria**: Publicly accessible; updated monthly; used by CEE, DESNZ, and media for sector communications
**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Community Group Coordinator Claire

- **Role**: Volunteer coordinator of a community energy cooperative
- **Goals**: Apply for funding, report on project progress, record community benefit spending
- **Pain Points**: Limited time (volunteer, not paid staff); confused by reporting requirements; technology not her strength
- **Technical Proficiency**: Low

#### Persona 2: Fund Manager Fatima

- **Role**: DESNZ community energy fund manager
- **Goals**: Assess applications, monitor project delivery, produce Ministerial briefings, ensure VfM
- **Pain Points**: No portfolio overview; manual data aggregation from email reports; cannot answer basic questions about sector performance without weeks of data collection
- **Technical Proficiency**: Medium

#### Persona 3: Community Member Mike

- **Role**: Local resident in a community with a community-owned wind turbine
- **Goals**: See how much energy the turbine generates, how much community benefit it produces, and where that money goes
- **Pain Points**: No visibility of project performance; relies on annual AGM report
- **Technical Proficiency**: Low

---

### Functional Requirements Detail

#### FR-1: Fund Application Workflow

**Description**: Guide community groups through the fund application process with a step-by-step form tailored to the specific funding programme.

**Acceptance Criteria**:
- [ ] Given a community group, when they start an application, then they are guided through scheme-specific questions with save-and-return capability
- [ ] Given a submitted application, when received by DESNZ, then it is assigned to a fund manager and the applicant receives acknowledgement within 24 hours
- [ ] Given an assessed application, when approved, then grant offer letter is generated and sent digitally for acceptance

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

#### FR-2: Project Registration and Milestones

**Description**: Register funded projects with key milestones (planning, grid connection, construction, commissioning) and track progress.

**Acceptance Criteria**:
- [ ] Given an approved project, when registered, then a milestone timeline is created based on the project type (solar, wind, hydro, battery)
- [ ] Given a milestone due date, when approaching, then automated reminders are sent to the project coordinator
- [ ] Given a delayed milestone, when the delay exceeds 30 days, then the fund manager is alerted with project context

**Priority**: MUST_HAVE
**Complexity**: LOW

#### FR-3: Generation Data Collection

**Description**: Collect generation data automatically from community energy installations via inverter monitoring APIs, smart meter feeds, or manual entry as a fallback.

**Acceptance Criteria**:
- [ ] Given a solar installation with an inverter monitoring system (e.g., SolarEdge, Enphase, SMA), when connected via API, then generation data is collected daily without manual intervention
- [ ] Given a wind turbine with SCADA, when connected, then generation data is collected hourly
- [ ] Given an installation without automated monitoring, when a project coordinator enters monthly generation manually, then the data is validated against expected output ranges

**Priority**: SHOULD_HAVE
**Complexity**: HIGH (due to diversity of monitoring systems)

#### FR-4: Community Benefit Recording

**Description**: Allow community groups to record how they disburse community benefit funds.

**Acceptance Criteria**:
- [ ] Given a community energy organisation, when they record a benefit disbursement, then they categorise it (fuel poverty, education, community facility, local reinvestment, other) and provide amount and description
- [ ] Given annual reporting, when due, then an automated report is generated from recorded benefits for funder review
- [ ] Given benefit data, when aggregated across all projects, then sector-wide community benefit statistics are available for the public dashboard

**Priority**: MUST_HAVE
**Complexity**: LOW

#### FR-5: Public Impact Dashboard

**Description**: Provide a public-facing, map-based dashboard showing community energy project locations, generation output, and community benefit.

**Acceptance Criteria**:
- [ ] Given the dashboard, when viewed by the public, then a map shows all community energy projects with location, technology type, and capacity
- [ ] Given a project on the map, when selected, then generation history, carbon savings, and community benefit summary are displayed
- [ ] Given national statistics, when viewed, then total community energy generation (GWh), carbon reduction (tCO2e), and community benefit (£) are displayed with year-on-year trends

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Portal Performance

**Requirement**: Application form pages load within 3 seconds (p95). Dashboard updates within 10 seconds. Public impact dashboard handles 1,000 concurrent users during media coverage peaks.
**Priority**: MEDIUM

### NFR-A-1: Availability

**Requirement**: 99.5% uptime. Community energy projects are not time-critical operations — planned maintenance during evenings/weekends is acceptable. RTO: 4 hours. RPO: 24 hours.
**Priority**: HIGH

### NFR-SEC-1: Data Protection

**Requirement**: UK GDPR compliance. Project financial data and community group member details classified as OFFICIAL. Public dashboard data is aggregated and non-personal.
**Priority**: HIGH

### NFR-U-1: Accessibility and Simplicity

**Requirement**: WCAG 2.2 Level AA. Interface must be usable by volunteers with low technical proficiency. Mobile-responsive for use on smartphones during site visits. Welsh language support.
**Priority**: CRITICAL — the primary user group is non-technical volunteers.

---

## Integration Requirements

### INT-1: Inverter Monitoring Systems

**Purpose**: Automatically collect generation data from community solar installations.
**Integration Type**: REST APIs to SolarEdge, Enphase, SMA, GoodWe, Huawei monitoring platforms
**Priority**: SHOULD_HAVE

### INT-2: Ofgem FIT/SEG Register

**Purpose**: Verify community energy installation registration and accreditation.
**Integration Type**: Batch data exchange (Ofgem does not provide real-time API)
**Priority**: SHOULD_HAVE

### INT-3: Companies House API

**Purpose**: Verify community energy organisation registration (Community Benefit Societies, Co-operatives).
**Integration Type**: RESTful API
**Priority**: SHOULD_HAVE

### INT-4: GOV.UK One Login

**Purpose**: Authentication for community group coordinators and fund managers.
**Integration Type**: OpenID Connect
**Priority**: MUST_HAVE

### INT-5: Carbon Intensity API (National Grid ESO)

**Purpose**: Calculate carbon savings based on actual grid carbon intensity at time of generation.
**Integration Type**: RESTful API (National Grid ESO Carbon Intensity API — free, public)
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Entity: Community Energy Project

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| project_id | UUID | Yes | Unique project identifier |
| organisation_name | String | Yes | Community energy group name |
| technology | Enum | Yes | Solar/Wind/Hydro/Battery/Biomass |
| capacity_kw | Decimal | Yes | Installed capacity in kW |
| location | GeoJSON | Yes | Project location (lat/long) |
| commissioning_date | Date | No | Date of first generation |
| annual_generation_kwh | Integer | No | Actual annual generation |
| community_benefit_annual | Decimal | No | Annual community benefit disbursed (£) |
| fund_source | Enum | Yes | CEF/RCEF/Local Authority/Other |
| grant_amount | Decimal | Yes | Total grant awarded (£) |
| status | Enum | Yes | Application/Approved/InBuild/Operational/Closed |

**Data Volume**: 1,000+ projects; 5,000+ generation records per project per year

**Data Retention**: Project data retained for 10 years after project closure (funder audit requirement).

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Projects tracked | ~200 (in spreadsheets) | 1,000+ | 18 months post-launch |
| Automated generation data | 0% | 80% of solar projects | 24 months post-launch |
| Reporting time reduction | 100% (manual) | 40% (60% reduction) | 12 months post-launch |
| Community benefit tracked | ~30% of projects | 90% | 18 months post-launch |
| Public dashboard visits | 0 | 10,000/month | 12 months post-launch |

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Community energy installations use diverse monitoring equipment from dozens of manufacturers — the integration challenge is breadth rather than depth.

**TC-2**: Many community energy sites are in rural areas with limited internet connectivity — offline-capable mobile interface needed for site visits.

**TC-3**: Community energy organisations are predominantly volunteer-run — the platform must be learnable in under 30 minutes without training.

### Assumptions

**A-1**: Major inverter monitoring platform APIs (SolarEdge, Enphase, SMA) will remain available and stable. If an API is withdrawn, manual entry fallback is available.

**A-2**: GOV.UK One Login will support organisation-level accounts (not just individual citizens) by the time of platform launch. If not, a separate authentication mechanism will be needed.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-005-STKE-v1.0 | Stakeholder Analysis | This programme | Stakeholder drivers | `projects/005-community-energy-fund-tracker/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 7 Programme | Governing principles | `projects/000-global/` |
| Community Energy State of the Sector | Research | CEE | Sector statistics | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Community Energy Fund Tracker (Project 005)
**Model**: Claude Opus 4.6 (1M context)
