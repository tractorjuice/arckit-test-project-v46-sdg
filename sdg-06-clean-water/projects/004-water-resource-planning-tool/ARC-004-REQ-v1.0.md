# Project Requirements: Water Resource Planning Tool

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Water Resource Planning Tool (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Resource Planning Tool Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA, Environment Agency, Ofwat, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Water Resource Planning Tool. The tool enables long-term water supply and demand planning under climate change scenarios, supporting DEFRA's National Framework for Water Resources and water company WRMP29 preparation.

---

## Executive Summary

### Business Context

England faces a projected supply-demand deficit of 4 billion litres per day by 2050 under central climate change projections. The 2022 drought — the driest summer since 1976 — resulted in hosepipe bans affecting 33 million customers and exposed the fragility of current water resource planning. Water companies must prepare Water Resource Management Plans (WRMPs) every 5 years, but currently use diverse proprietary models with inconsistent climate assumptions, making national-level supply-demand assessment difficult.

DEFRA's National Framework for Water Resources (2020) called for regional coordination through 5 Regional Water Resource Groups and a common analytical approach. This project delivers the common modelling platform, enabling consistent climate scenario application, standardised supply-demand balance calculation, and national aggregation of regional plans.

### Objectives

- Deliver a common modelling platform for all 17 water companies and 5 regional groups for WRMP29
- Integrate UKCP18 probabilistic climate projections at catchment scale
- Enable 25-50 year supply-demand scenario planning with quantified uncertainty
- Integrate Environmental Flow Indicators for abstraction sustainability assessment
- Support strategic infrastructure option appraisal (reservoirs, transfers, desalination)

### Expected Outcomes

- 100% of water companies using common platform for WRMP29 (consistent methodology)
- 50% reduction in WRMP preparation time through standardised tools
- National supply-demand balance view available for first time (aggregated from regional plans)
- Climate uncertainty explicitly quantified in all supply-demand assessments

### Project Scope

**In Scope**:
- Supply-demand balance modelling at Water Resource Zone level
- UKCP18 climate projection integration (all RCP scenarios)
- Demand forecasting (population growth, per capita consumption, climate effects on demand)
- Deployable output assessment (yield from sources under drought scenarios)
- Environmental flow constraint modelling
- Strategic option appraisal framework (cost-benefit for new infrastructure)
- Regional plan integration and national aggregation
- Scenario comparison and sensitivity analysis tools

**Out of Scope**:
- Water quality modelling (Project 001)
- Flood risk modelling (Project 002)
- Operational water supply management (day-to-day system control)
- Hydraulic network modelling (detailed pipe-level analysis)

---

## Business Requirements

### BR-001: Common Modelling Platform

**Description**: Provide a common water resource modelling platform that all 17 water companies and 5 regional groups use for WRMP29 preparation, ensuring consistent methodology application.

**Rationale**: Current diversity of proprietary models (AQUATOR, Miser, WATHNET, bespoke Excel) makes national-level assessment impossible and enables inconsistent methodology application. A common platform ensures like-for-like comparison and regional plan compatibility.

**Success Criteria**:
- 17/17 water companies using the platform for WRMP29
- 5/5 regional groups producing plans using common methodology
- Zero methodology inconsistencies between regional plans

**Priority**: MUST_HAVE
**Stakeholder**: DEFRA Water Resources Policy Director (SD-1)

---

### BR-002: Climate-Integrated Scenario Planning

**Description**: Integrate UKCP18 probabilistic climate projections into water resource supply-demand modelling, enabling scenario analysis spanning 2030-2085 with quantified uncertainty.

**Rationale**: The 2022 drought demonstrated that historical drought records are insufficient for future planning. UKCP18 provides probabilistic climate projections that quantify the range of possible futures. Without explicit climate integration, WRMPs risk either over- or under-investing in new supply.

**Success Criteria**:
- All four RCP scenarios (2.6, 4.5, 6.0, 8.5) available at catchment scale
- Uncertainty quantified at 10th, 50th, and 90th percentile for all projections
- Demand-side climate effects modelled (hot weather demand increase)

**Priority**: MUST_HAVE
**Stakeholder**: DEFRA Climate Adaptation Team, Water Companies (SD-1, SD-3)

---

### BR-003: Environmental Flow Integration

**Description**: Integrate Environmental Flow Indicators and protected site water needs as constraints in water resource planning, ensuring supply options are automatically assessed against environmental limits.

**Rationale**: The Environment Act 2021 strengthened the duty to protect water resources for the environment. Approximately 28% of surface water bodies in England have unsustainable abstraction. Supply options that worsen abstraction sustainability are not viable regardless of water supply benefit.

**Success Criteria**:
- Environmental Flow Indicators integrated as planning constraints for all water bodies
- Supply options automatically assessed against abstraction sustainability
- Protected site water needs (SSSIs, SACs) flagged as absolute constraints

**Priority**: MUST_HAVE
**Stakeholder**: EA Water Resources Director (SD-2), Natural England (SD-4)

---

### BR-004: Strategic Infrastructure Option Appraisal

**Description**: Provide a structured framework for appraising strategic infrastructure options (new reservoirs, inter-regional transfers, desalination, water recycling) against supply-demand deficit scenarios, using HM Treasury Green Book-compliant cost-benefit analysis.

**Rationale**: Strategic infrastructure investments of GBP 500M-2B+ require rigorous option appraisal. The South East Strategic Reservoir alone is estimated at GBP 2.2B. Options must be compared on consistent economic, environmental, and social criteria.

**Success Criteria**:
- Option appraisal framework compliant with HM Treasury Green Book
- Environmental and social value quantified alongside financial cost
- Options ranked by net present value, environmental impact, and deliverability

**Priority**: SHOULD_HAVE
**Stakeholder**: Ofwat, Water Companies (SD-3)

---

## Functional Requirements

### FR-001: Supply-Demand Balance Model

**Description**: Calculate water supply-demand balance at Water Resource Zone (WRZ) level for planning horizons of 5, 10, 25, and 50 years under multiple climate and demand scenarios.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:
- [ ] Given a WRZ configuration with supply sources and demand projections, when the model runs, then a supply-demand balance is calculated for each planning year
- [ ] Given multiple climate scenarios are selected, when the model runs, then supply-demand balance is calculated for each scenario with uncertainty bands
- [ ] Given the model detects a supply-demand deficit, then the deficit is quantified in Ml/d with timing and probability

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-002: UKCP18 Climate Scenario Engine

**Description**: Ingest and process UKCP18 probabilistic climate projections, downscaling to catchment level for use in supply assessment and demand forecasting.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a UKCP18 RCP scenario is selected, when the climate engine processes projections, then catchment-level temperature, precipitation, and evapotranspiration changes are available at monthly resolution
- [ ] Given probabilistic projections, when uncertainty analysis runs, then 10th, 50th, and 90th percentile outcomes are presented for each variable
- [ ] Given a drought severity scenario (e.g., 1 in 500 year), when the model runs, then the supply impact is quantified with confidence intervals

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-003: Demand Forecasting

**Description**: Project future water demand based on population growth (ONS projections), per capita consumption trends, climate effects on demand, metering penetration, and demand management measures.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given ONS population projections and local plan housing targets, when demand is forecast, then per-WRZ demand projections are produced for 5-50 year horizons
- [ ] Given a hot-dry climate scenario, when demand effects are modelled, then increased peak demand and drought demand are quantified
- [ ] Given planned demand management measures (smart meters, leakage reduction), when their effects are modelled, then demand reduction is quantified with delivery uncertainty

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-004: Deployable Output Assessment

**Description**: Calculate deployable output (water available from supply sources) under drought conditions, accounting for source reliability, treatment capacity, network constraints, and environmental flow requirements.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:
- [ ] Given a drought scenario, when deployable output is calculated, then yield from each source is assessed against drought severity
- [ ] Given Environmental Flow Indicators are applied, when a source is constrained, then the reduced yield is reflected in deployable output
- [ ] Given climate change affects drought frequency/severity, then deployable output is recalculated under future climate scenarios

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-005: Environmental Flow Constraint Modelling

**Description**: Apply Environmental Flow Indicators (EFIs) and Habitats Directive flow requirements as constraints in supply-demand modelling, automatically flagging supply options that breach environmental limits.

**Relates To**: BR-003

**Acceptance Criteria**:
- [ ] Given a water body has an EFI, when a supply option would increase abstraction, then the model flags whether the option complies with or breaches the EFI
- [ ] Given a protected site (SSSI, SAC) has defined water needs, then these are treated as absolute constraints (cannot be overridden)
- [ ] Given an abstraction is already assessed as unsustainable, then the model enforces abstraction reduction in future planning periods

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-006: Option Appraisal Framework

**Description**: Structured assessment of supply-demand intervention options with Green Book-compliant cost-benefit analysis, environmental impact assessment, and social value scoring.

**Relates To**: BR-004

**Acceptance Criteria**:
- [ ] Given a supply-demand deficit, when supply options are defined, then each option is appraised against cost (NPV), environmental impact, and social value criteria
- [ ] Given multiple options are appraised, when ranking is requested, then options are presented in a consistent decision matrix with multi-criteria scoring
- [ ] Given discount rates and optimism bias are applied (HM Treasury Green Book), then financial appraisal is compliant with public sector requirements

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

### FR-007: Regional Plan Integration

**Description**: Aggregate Water Resource Zone-level plans into regional group plans and national overview, enabling cross-regional transfer analysis and national supply-demand balance.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given all WRZ plans within a regional group are complete, when aggregation runs, then a regional supply-demand balance is produced
- [ ] Given inter-regional transfer options exist, when modelled, then the donor and recipient impacts are assessed simultaneously
- [ ] Given all 5 regional plans are complete, when national aggregation runs, then a national supply-demand overview is produced

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Model Run Time

**Requirement**: Supply-demand balance model run times:
- Single WRZ, single scenario: < 5 minutes
- Single WRZ, full ensemble (100 climate scenarios): < 2 hours
- Full regional group (all WRZs, all scenarios): < 8 hours (batch overnight)
- National aggregation: < 1 hour

**Priority**: HIGH

---

#### NFR-P-2: Interactive Dashboard Performance

**Requirement**: Scenario comparison dashboard:
- Scenario switching: < 3 seconds
- Map rendering: < 2 seconds
- Chart/graph rendering: < 1 second
- Data export: < 30 seconds for standard reports

**Priority**: MEDIUM

---

### Availability and Resilience

#### NFR-A-1: Platform Availability

**Requirement**: 99.5% availability (batch processing platform, not real-time critical). Planned maintenance windows acceptable with 48-hour notice.

**Priority**: MEDIUM

---

### Scalability Requirements

#### NFR-S-1: Concurrent Users

**Requirement**: Support 200 concurrent users (water company planners, regional group coordinators, DEFRA/EA/Ofwat analysts) during WRMP preparation peak periods (typically 6 months before submission deadline).

**Priority**: HIGH

---

### Data Requirements

#### DR-001: UKCP18 Climate Data

**Requirement**: Platform must ingest and store UKCP18 probabilistic projections (12km grid, daily resolution) for all RCP scenarios. Estimated storage: 5TB.

**Priority**: MUST_HAVE

---

#### DR-002: Historical Hydrological Records

**Requirement**: 100+ years of historical flow records for key rivers (EA NRFA dataset), used for drought sequence analysis and model calibration.

**Priority**: MUST_HAVE

---

#### DR-003: ONS Population Projections

**Requirement**: Subnational population projections (local authority level) for 25-year planning horizon.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: UKCP18 Climate Data (Met Office Hadley Centre)

**Purpose**: Ingest probabilistic climate projections for supply and demand modelling.

**Integration Type**: Batch file transfer (NetCDF format) + API for specific scenarios

**Data Exchanged**:
- **Hadley Centre to Platform**: Temperature, precipitation, evapotranspiration projections at 12km grid

**SLA**: Updated when new UKCP releases are published (approximately annually)
**Priority**: MUST_HAVE

---

### INT-002: EA National River Flow Archive (NRFA)

**Purpose**: Historical river flow data for drought analysis and model calibration.

**Integration Type**: Batch download + API for specific gauging stations

**Data Exchanged**:
- **NRFA to Platform**: Daily mean flow records, peak flow records, low flow statistics, catchment descriptors

**Priority**: MUST_HAVE

---

### INT-003: EA Abstraction Licensing Database

**Purpose**: Current abstraction licence conditions, Environmental Flow Indicators, and sustainability assessments.

**Integration Type**: API (read-only) + quarterly batch sync

**Data Exchanged**:
- **EA to Platform**: Abstraction licence details (location, quantity, conditions), EFI values, sustainability assessment results

**Priority**: MUST_HAVE

---

### INT-004: Ofwat Price Review Data

**Purpose**: Feed supply-demand balance evidence into Ofwat's price review analytical framework.

**Integration Type**: Batch export (aligned with WRMP submission cycle)

**Data Exchanged**:
- **Platform to Ofwat**: Supply-demand balance results, option appraisals, investment requirements

**Priority**: HIGH

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: UKCP18 climate projections are on a 12km grid. Downscaling to catchment level introduces additional uncertainty that must be quantified.

**TC-2**: Some water companies have complex conjunctive-use systems (groundwater + surface water + transfers) that require bespoke modelling within the common framework.

### Business Constraints

**BC-1**: Platform must be operational by Q1 2028 for WRMP29 preparation.

**BC-2**: Programme budget capped at GBP 8M over 3 years.

**BC-3**: Water companies must retain ability to model company-specific operational constraints within the common framework.

### Assumptions

**A-1**: Water companies will adopt the common platform if DEFRA/EA/Ofwat jointly mandate its use for WRMP29.

**A-2**: UKCP18 remains the definitive UK climate projection dataset through the WRMP29 cycle.

**A-3**: ONS subnational population projections are sufficiently accurate for water demand forecasting.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Companies using common platform | 0 | 17 | Q1 2028 |
| Regional groups integrated | 0 | 5 | Q3 2028 |
| WRMP preparation time | 18 months | 9 months | WRMP29 cycle |
| Climate scenarios available | Varies by company | 4 RCPs, full probabilistic | Q3 2027 |
| National supply-demand view | Not available | Available | Q4 2028 |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Stakeholder Analysis | Architecture | ARC-004-STKE-v1.0 | Stakeholder drivers and goals | `projects/004-water-resource-planning-tool/ARC-004-STKE-v1.0.md` |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | Governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| National Framework for Water Resources | Strategy | GOV.UK | Regional planning framework | N/A — external reference |
| UKCP18 Science Overview | Scientific Report | Met Office | Climate projection methodology | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Resource Planning Tool (Project 004)
**AI Model**: Claude Opus 4.6 (1M context)
