# Project Requirements: Climate Risk Assessment Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Climate Risk Assessment Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Climate Risk Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Climate Risk Programme Board, DEFRA Digital, Met Office, Environment Agency, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Climate Risk Assessment Platform — a digital service that integrates UKCP18 climate projections with geospatial infrastructure data to produce standardised climate risk assessments for UK infrastructure operators and local authorities.

---

## Executive Summary

### Business Context

The UK Climate Change Risk Assessment (CCRA3) identifies 61 climate risks and opportunities across eight priority areas. Infrastructure operators are required to report on climate risks under the Adaptation Reporting Power (Climate Change Act 2008, Section 62). However, the third round of ARP reports revealed inconsistent methodologies, making cross-sector comparison difficult. This platform will provide a standardised, evidence-based climate risk assessment framework integrating UKCP18 probabilistic projections with asset-level vulnerability data.

### Objectives

- Provide a Met Office-endorsed climate risk assessment methodology for UK infrastructure
- Integrate UKCP18 climate projections with Environment Agency flood risk data and geospatial infrastructure data
- Reduce infrastructure operators' ARP reporting burden by 50% through pre-populated assessments
- Enable local authorities to access locally relevant climate risk evidence for adaptation planning
- Support compound risk assessment (heat + flood + drought combinations)

### Expected Outcomes

- 80% of Adaptation Reporting Power obligated entities using the platform for ARP4
- CCC rates ARP4 report quality as "significantly improved" compared to ARP3
- Met Office endorses platform's use of UKCP18 projections
- Local authorities access ward-level climate risk summaries for adaptation planning

### Project Scope

**In Scope**:

- Climate hazard assessment: heat, flooding (fluvial, pluvial, coastal), drought, windstorm, sea-level rise
- UKCP18 projection integration (RCP2.6, RCP4.5, RCP6.0, RCP8.5 scenarios)
- Asset-level risk scoring for infrastructure (transport, energy, water, telecoms)
- Local authority area-level risk summaries
- API for integration with asset management systems
- Compound risk assessment (multi-hazard combinations)

**Out of Scope**:

- Detailed engineering vulnerability assessment (requires sector-specific tools)
- Real-time weather event tracking or early warning
- Financial loss estimation (requires insurance/actuarial modelling)
- International climate risk (UK-only)

---

## Business Requirements

### BR-001: Standardised Climate Risk Methodology

**Description**: Provide a single, Met Office-endorsed methodology for assessing climate risks to UK infrastructure that enables consistent, comparable assessments across sectors.

**Rationale**: ARP3 reports used inconsistent methodologies. CCC cannot compare climate risk management across sectors.

**Success Criteria**:

- Met Office formal endorsement of UKCP18 projection usage methodology
- CCC confirms methodology enables meaningful cross-sector comparison
- Methodology documentation published openly

**Priority**: MUST_HAVE

---

### BR-002: Adaptation Reporting Power Support

**Description**: Enable infrastructure operators to produce ARP-compliant climate risk reports with 50% less effort than manual production.

**Rationale**: Current ARP process is burdensome and produces inconsistent quality. Platform should reduce burden while improving quality.

**Success Criteria**:

- Operators report 50%+ time reduction vs ARP3 process
- ARP4 report quality rated higher by CCC than ARP3
- 80%+ of obligated entities use platform

**Priority**: MUST_HAVE

---

### BR-003: Local Authority Climate Risk Evidence

**Description**: Provide locally relevant climate risk evidence at ward or LSOA level that supports local adaptation planning without requiring specialist GIS or climate science expertise.

**Rationale**: CCC identifies local adaptation as a critical gap. Most LAs lack specialist climate risk staff.

**Success Criteria**:

- Ward-level risk summaries available for all 152 upper-tier authorities in England
- Usable by non-specialist officers (no GIS or climate science training required)
- Risk summaries available in plain language with supporting evidence

**Priority**: SHOULD_HAVE

---

### BR-004: Compound Risk Assessment

**Description**: Assess compound climate risks where multiple hazards interact (e.g., drought followed by heavy rainfall causing worse flooding on baked ground).

**Rationale**: CCRA3 identifies compound and cascading risks as a critical gap. Individual hazard assessments underestimate real-world risk.

**Success Criteria**:

- Compound risk methodology covering at least 3 hazard combinations
- Compound risk scores distinguish from single-hazard scores
- Methodology peer-reviewed by climate science community

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Infrastructure Risk Manager

- **Role**: Climate risk lead at National Highways/Network Rail/water company
- **Goals**: Produce ARP-compliant risk assessments for asset portfolio, integrate with ISO 55001 asset management
- **Pain Points**: Manual data compilation from multiple sources, inconsistent methodology
- **Technical Proficiency**: Medium-High

#### Persona 2: Local Authority Planning Officer

- **Role**: Sustainability/emergency planning officer at upper-tier authority
- **Goals**: Access locally relevant climate risk evidence for local plan policies and adaptation planning
- **Pain Points**: No specialist climate science expertise, limited GIS skills
- **Technical Proficiency**: Low-Medium

#### Persona 3: DEFRA Adaptation Policy Analyst

- **Role**: DEFRA ARP programme manager
- **Goals**: Assess cross-sector climate risk trends, prepare Ministerial briefings, monitor ARP compliance
- **Pain Points**: Inconsistent ARP report quality preventing meaningful comparison
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-001: Climate Hazard Assessment

**Description**: Calculate climate hazard scores for specified locations using UKCP18 projections across multiple scenarios and time horizons.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a UK grid reference or postcode, when a hazard assessment is requested, then scores for heat, flood, drought, wind, and sea-level rise are returned
- [ ] Given a location, when assessed, then results are provided for 2030s, 2050s, and 2080s time horizons
- [ ] Given the assessment, when displayed, then uncertainty ranges from UKCP18 probabilistic projections are shown
- [ ] Given all hazard scores, when combined, then an overall climate risk rating is calculated

**Priority**: MUST_HAVE

---

#### FR-002: Asset-Level Risk Scoring

**Description**: Calculate climate risk scores for specific infrastructure assets by combining hazard scores with asset vulnerability factors.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Given an asset type (road, rail, substation, water treatment works) and location, when assessed, then a risk score combining hazard exposure and asset vulnerability is produced
- [ ] Given the risk score, when displayed, then it follows a standard likelihood x consequence risk matrix
- [ ] Given the risk assessment, when completed, then recommended adaptation actions are suggested based on risk level

**Priority**: MUST_HAVE

---

#### FR-003: Portfolio Risk Dashboard

**Description**: Provide infrastructure operators with a portfolio-level view of climate risk across all their assets, with aggregation, filtering, and export capabilities.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given an operator account, when the portfolio view is accessed, then a map and table of all assessed assets with risk scores is shown
- [ ] Given the portfolio, when filtered by hazard type, then only assets at risk from that hazard are displayed
- [ ] Given the portfolio, when exported, then a structured risk register in CSV/Excel format is generated
- [ ] Given the portfolio, when viewed as summary, then sector-appropriate aggregate risk statistics are shown

**Priority**: MUST_HAVE

---

#### FR-004: ARP Report Generator

**Description**: Generate structured Adaptation Reporting Power reports from platform risk assessments, pre-populated with asset risk data and recommended actions.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a completed portfolio assessment, when the ARP report is generated, then it follows DEFRA's ARP4 reporting template
- [ ] Given the report, when generated, then risk assessments, actions, and progress tracking are pre-populated
- [ ] Given the report, when edited by the operator, then customisation of actions and narrative is possible
- [ ] Given the final report, when submitted, then it is stored for DEFRA review and CCC analysis

**Priority**: MUST_HAVE

---

#### FR-005: Local Authority Risk Summary

**Description**: Provide ward-level climate risk summaries for local authority officers without requiring GIS skills or climate science expertise.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Given a local authority, when selected, then a summary of climate risks across all wards is displayed
- [ ] Given a ward, when selected, then a plain-language risk summary covering heat, flood, drought, and coastal erosion is shown
- [ ] Given the risk summary, when presented, then risk categories are plain language (low/medium/high/very high) with supporting evidence
- [ ] Given the summary, when exported, then a committee-ready briefing document in PDF/Word format is generated

**Priority**: SHOULD_HAVE

---

#### FR-006: Compound Risk Assessment

**Description**: Assess compound climate risks where multiple hazards interact or cascade.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a location, when compound risk is assessed, then interactions between hazard pairs are identified
- [ ] Given a compound risk, when displayed, then the additional risk from hazard interaction is quantified
- [ ] Given compound risk results, when compared to single-hazard results, then the incremental compound risk is visible

**Priority**: SHOULD_HAVE

---

#### FR-007: Risk Assessment API

**Description**: Provide a RESTful API enabling infrastructure operators to integrate risk assessments with asset management systems.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Given an API request with asset location and type, when processed, then a risk assessment JSON response is returned
- [ ] Given the API, when a bulk assessment is requested (up to 10,000 assets), then results are returned within 60 seconds
- [ ] Given the API, when versioned, then backward compatibility is maintained for at least 12 months

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Risk Assessment Response Time

**Requirement**: Single asset risk assessment within 3 seconds. Bulk assessment (10,000 assets) within 60 seconds.

**Priority**: MUST_HAVE

#### NFR-P-002: Geospatial Query Performance

**Requirement**: Geospatial queries (find all assets within a flood risk zone) within 5 seconds for datasets up to 1 million assets.

**Priority**: MUST_HAVE

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.5% uptime. Enhanced availability during ARP reporting deadlines (March-April annually).

**Priority**: MUST_HAVE

#### NFR-A-002: Disaster Recovery

**RPO**: 4 hours | **RTO**: 8 hours

**Priority**: MUST_HAVE

### Security Requirements

#### NFR-SEC-001: Data Classification

**Requirement**: Published risk methodology is OFFICIAL (public). Individual operator asset locations and risk assessments are OFFICIAL-SENSITIVE (commercial). Operator accounts require MFA.

**Priority**: MUST_HAVE

#### NFR-SEC-002: Operator Data Isolation

**Requirement**: Each operator's asset data and risk assessments are isolated. No operator can view another operator's data. DEFRA and CCC have read-only aggregated views.

**Priority**: MUST_HAVE

### Accessibility Requirements

#### NFR-U-001: WCAG Compliance

**Requirement**: WCAG 2.2 Level AA. Geospatial maps have accessible alternatives (data tables, text descriptions). Risk categories conveyed through text and pattern, not colour alone.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: UKCP18 Climate Projections

**Purpose**: Consume Met Office UKCP18 probabilistic climate projections for all hazard calculations.

**Integration Type**: Batch data ingest (updated when new projection releases occur, approximately annually)

**Data Exchanged**: Temperature, precipitation, wind, sea-level projections by RCP scenario, time horizon, and 12km grid cell

**Priority**: MUST_HAVE

### INT-002: Environment Agency Flood Risk Data

**Purpose**: Integrate EA flood risk data for flood hazard assessment.

**Integration Type**: API integration with EA open data services (real-time availability)

**Data Exchanged**: Flood zones, flood depth, flood probability, coastal erosion rates

**Priority**: MUST_HAVE

### INT-003: Ordnance Survey Geospatial

**Purpose**: Base mapping and address lookup for asset location.

**Integration Type**: API integration with OS Places and OS Maps

**Data Exchanged**: Address lookup, coordinates, base mapping tiles

**Priority**: MUST_HAVE

### INT-004: Climate Adaptation Planning Tool (Project 004)

**Purpose**: Provide risk assessment data to the Adaptation Planning Tool for local authority use.

**Integration Type**: Internal API (within SDG 13 programme)

**Data Exchanged**: Ward-level risk summaries, hazard scores, recommended adaptation actions

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Climate Hazard Score

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| location_grid_ref | String | Yes | OS grid reference (12km resolution) |
| hazard_type | Enum | Yes | Heat, flood, drought, wind, sea_level_rise |
| scenario | Enum | Yes | RCP2.6, RCP4.5, RCP6.0, RCP8.5 |
| time_horizon | Enum | Yes | 2030s, 2050s, 2080s |
| percentile_10 | Decimal | Yes | 10th percentile projection |
| percentile_50 | Decimal | Yes | 50th percentile (central) projection |
| percentile_90 | Decimal | Yes | 90th percentile projection |
| risk_category | Enum | Yes | Low, medium, high, very_high |

#### Entity 2: Asset Risk Assessment

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique identifier |
| operator_id | UUID | Yes | Infrastructure operator |
| asset_type | Enum | Yes | Road, rail, substation, water_treatment, etc. |
| location | Geometry | Yes | Asset geographic coordinates |
| hazard_exposure | JSON | Yes | Hazard scores for all hazard types |
| vulnerability_score | Decimal | Yes | Asset vulnerability (0-1) |
| risk_score | Decimal | Yes | Combined risk (exposure x vulnerability) |
| risk_category | Enum | Yes | Low, medium, high, very_high, critical |
| recommended_actions | JSON | No | Suggested adaptation measures |

---

## Approval

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, DEFRA | _________ | PENDING |
| Met Office Hadley Centre | _________ | PENDING |
| Environment Agency | _________ | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UKCP18 Science Overview | Scientific report | Met Office | Climate projection methodology | N/A |
| CCRA3 | Statutory report | CCC | 61 priority climate risks | N/A |
| Climate Change Act 2008 (S.62) | Legislation | legislation.gov.uk | Adaptation Reporting Power | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Climate Risk Assessment Platform (Project 002)
**Model**: Claude Opus 4.6
