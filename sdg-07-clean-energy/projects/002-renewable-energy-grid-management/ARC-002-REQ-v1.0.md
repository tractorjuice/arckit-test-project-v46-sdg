# Project Requirements: Renewable Energy Grid Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Renewable Energy Grid Management (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Renewable Energy Grid Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | National Grid ESO Programme Board, DESNZ, Ofgem |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Renewable Energy Grid Management platform — a real-time system for monitoring, forecasting, and optimising the integration of renewable generation into the GB electricity grid.

---

## Executive Summary

### Business Context

The UK has committed to 50GW of offshore wind capacity by 2030 and a fully decarbonised power system by 2035. As renewable generation grows from approximately 42% (2024) to 70%+ of electricity supply, the grid management challenge transforms fundamentally. Unlike dispatchable thermal generation, wind and solar output is intermittent, non-synchronous, and distributed. National Grid ESO's existing control systems were designed for a fleet of large, predictable, synchronous generators. A new platform is needed to manage a grid dominated by thousands of distributed, intermittent renewable assets.

### Objectives

- Provide sub-second real-time visibility of all transmission-connected renewable generation assets
- Deliver AI-powered renewable generation forecasting with 95% accuracy at 4-hour horizon
- Reduce renewable curtailment by 20% through optimised balancing and constraint management
- Enable safe grid operation at 70%+ instantaneous renewable penetration
- Integrate with the Balancing Mechanism and demand flexibility markets

### Expected Outcomes

- £160M annual reduction in consumer balancing costs (BSUoS) through reduced curtailment
- Grid stability maintained at 70%+ renewable penetration without frequency excursions
- 2.5 MtCO2e additional annual carbon reduction through avoided curtailment (more renewable energy used)
- Investor confidence in UK renewable deployment through demonstrated grid accommodation capability

### Project Scope

**In Scope**:
- Real-time telemetry ingestion from renewable generation assets (wind, solar, battery, biomass)
- AI/ML forecasting engine for wind and solar generation output
- Grid constraint management and curtailment optimisation
- Integration with ESO Balancing Mechanism and ancillary services markets
- Control room dashboard and decision support tools
- DNO data exchange for distributed generation visibility

**Out of Scope**:
- Physical grid infrastructure upgrades (transmission lines, substations)
- Generator hardware or SCADA system modifications
- Consumer-facing applications
- Interconnector flow management (separate ESO programme)

---

## Business Requirements

### BR-1: Real-Time Renewable Generation Visibility

**Description**: The platform must provide ESO control room operators with sub-second visibility of active power output from all transmission-connected renewable generation assets, and 15-minute aggregated data from distribution-connected generation.

**Rationale**: Grid balancing decisions require accurate, real-time knowledge of current generation output. With thermal plant, output is predictable and controllable. With renewables, output varies with weather and must be continuously monitored. Currently, ESO has limited real-time visibility of smaller renewable assets and no direct visibility of distribution-connected generation.

**Success Criteria**:
- 95% of transmission-connected renewable capacity visible with <1 second latency
- 80% of distribution-connected renewable capacity visible with <15 minute latency
- Data quality: <0.1% missing or invalid readings

**Priority**: MUST_HAVE
**Stakeholder**: ESO Chief Engineer

---

### BR-2: Renewable Generation Forecasting

**Description**: The platform must forecast wind and solar generation output at asset, regional, and national levels with sufficient accuracy to reduce forecast-driven curtailment.

**Rationale**: Curtailment often results from conservative forecasts that over-estimate constraint risk. Improved forecasting accuracy directly reduces unnecessary curtailment, saving consumers £160M+ annually and increasing renewable energy utilisation.

**Success Criteria**:
- 95% forecast accuracy at 4-hour horizon (national aggregate)
- 90% forecast accuracy at 24-hour horizon (regional level)
- 85% forecast accuracy at 48-hour horizon (day-ahead market)

**Priority**: MUST_HAVE
**Stakeholder**: ESO Market Development

---

### BR-3: Curtailment Optimisation

**Description**: The platform must optimise curtailment decisions to minimise wasted renewable energy while maintaining grid safety constraints.

**Rationale**: UK wind curtailment exceeded 8.5 TWh in 2024 at a cost of over £800M to consumers. A significant proportion of this curtailment is precautionary rather than physically necessary. Better data and algorithms can safely reduce curtailment without compromising grid security.

**Success Criteria**:
- 20% reduction in annual curtailment volume (from 8.5 TWh baseline)
- All curtailment decisions auditable with justification trail
- No grid security events attributable to reduced curtailment margins

**Priority**: MUST_HAVE
**Stakeholder**: Ofgem, Renewable generators

---

## Functional Requirements

### FR-1: Telemetry Ingestion Engine

**Description**: The system must ingest real-time telemetry data from renewable generation assets via multiple protocols (IEC 61850, IEC 60870-5-104, DNP3, ICCP/TASE.2).

**Relates To**: BR-1

**Acceptance Criteria**:
- [ ] Given a wind farm transmitting IEC 61850 data, when a measurement sample is sent, then it is received and processed within 500ms
- [ ] Given a solar farm transmitting via ICCP/TASE.2, when telemetry is received, then active power, reactive power, and availability are captured
- [ ] Given a telemetry gap exceeding 10 seconds, when detected, then an alert is raised to the control room with estimated output based on last known state and weather model

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-2: AI Forecasting Engine

**Description**: The system must generate renewable generation forecasts using machine learning models combining weather data (Met Office, ECMWF), historical generation patterns, and real-time telemetry.

**Relates To**: BR-2

**Acceptance Criteria**:
- [ ] Given current weather data and historical patterns, when a forecast is generated, then national wind output forecast achieves 95% accuracy at 4-hour horizon
- [ ] Given a forecast model, when new actual generation data arrives, then the model retrains within 1 hour and forecasts update automatically
- [ ] Given multiple weather data sources, when inputs disagree, then the ensemble approach weights sources by recent accuracy performance

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-3: Constraint Management and Curtailment Optimiser

**Description**: The system must calculate optimal curtailment dispatch to resolve grid constraints with minimum renewable energy waste.

**Relates To**: BR-3

**Acceptance Criteria**:
- [ ] Given a thermal constraint on a transmission boundary, when the optimiser runs, then it identifies the minimum curtailment required to resolve the constraint
- [ ] Given multiple generators that could be curtailed, when selecting which to curtail, then the algorithm minimises total curtailment cost (volume x price) while respecting Grid Code obligations
- [ ] Given a curtailment instruction, when issued, then a full audit trail is recorded (constraint, calculation, alternative options considered, decision rationale)

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-4: Control Room Dashboard

**Description**: The system must provide ESO control room engineers with a real-time operational dashboard showing national renewable generation status, forecasts, constraints, and recommended actions.

**Relates To**: BR-1, BR-2, BR-3

**Acceptance Criteria**:
- [ ] Given the dashboard, when viewed, then it displays current national renewable output by technology (wind, solar, battery, biomass) with <2 second refresh
- [ ] Given a forecast divergence >10% from actual, when detected, then a visual alert is displayed with recommended control actions
- [ ] Given a constraint event, when occurring, then the dashboard highlights affected boundaries, constrained generators, and recommended curtailment dispatch

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Telemetry Latency

**Requirement**: End-to-end telemetry processing latency must not exceed 1 second from generator SCADA to control room dashboard for transmission-connected assets.
**Priority**: CRITICAL

### NFR-P-2: Forecasting Computation

**Requirement**: National wind and solar forecast must be recalculated within 5 minutes of new weather model data availability. Intra-day updates must complete within 60 seconds.
**Priority**: HIGH

### NFR-A-1: Platform Availability

**Requirement**: 99.99% uptime (52.6 minutes maximum unplanned downtime per year). The platform is classified as critical national infrastructure supporting real-time grid balancing.
**RTO**: <5 minutes. **RPO**: 0 (no data loss).
**Priority**: CRITICAL

### NFR-SEC-1: Critical Infrastructure Security

**Requirement**: NIS Regulations compliance as an operator of essential services. Operational technology (OT) network isolation from corporate IT. NCSC CAF (Cyber Assessment Framework) alignment. Annual penetration testing by NCSC-approved provider.
**Priority**: CRITICAL

### NFR-SEC-2: SCADA Security

**Requirement**: All SCADA/telemetry connections must use encrypted transport. IEC 62351 security for IEC 61850/60870 protocols. Certificate-based authentication for all telemetry data sources.
**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Generator SCADA Systems

**Purpose**: Receive real-time telemetry from renewable generation assets.
**Integration Type**: Real-time telemetry via IEC 61850, IEC 60870-5-104, ICCP/TASE.2
**Data Exchanged**: Active power (MW), reactive power (MVAr), availability, status, wind speed, irradiance
**SLA**: <1 second latency, 99.99% availability
**Priority**: CRITICAL

### INT-2: Met Office Weather Data

**Purpose**: Weather forecast inputs for generation forecasting models.
**Integration Type**: Scheduled data feed (hourly updates, 15-minute resolution)
**Data Exchanged**: Wind speed/direction at hub height, solar irradiance, temperature, cloud cover — by geographic grid
**Priority**: MUST_HAVE

### INT-3: ESO Balancing Mechanism

**Purpose**: Submit and manage curtailment instructions and balancing actions.
**Integration Type**: Real-time API with the Balancing Mechanism systems (BMRS)
**Data Exchanged**: Bid-offer data, Physical Notifications, curtailment instructions, settlement data
**Priority**: MUST_HAVE

### INT-4: DNO Data Exchange Platform

**Purpose**: Receive aggregated distributed generation data from DNOs.
**Integration Type**: Near-real-time API (15-minute resolution)
**Data Exchanged**: Aggregated active power output by Grid Supply Point from distribution-connected generation
**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: The platform must operate within National Grid ESO's existing OT network architecture, with strict separation from corporate IT and internet-facing systems.

**TC-2**: Generator SCADA integration depends on generator cooperation and in some cases hardware upgrades at the generator end — this is outside the project scope but creates a dependency.

**TC-3**: Met Office weather data is available under existing Crown copyright arrangements but model resolution may limit forecasting accuracy for individual small assets.

### Assumptions

**A-1**: Generators will provide telemetry access under Grid Code obligations. If generators resist, Ofgem enforcement may be required.

**A-2**: The existing ESO OT network has sufficient bandwidth for the additional telemetry data volumes. Network capacity assessment to be completed in Discovery phase.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-002-STKE-v1.0 | Stakeholder Analysis | This programme | Stakeholder drivers and goals | `projects/002-renewable-energy-grid-management/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 7 Programme | Governing principles | `projects/000-global/` |
| Grid Code | Technical Standard | National Grid ESO | Connection and operation requirements | N/A — external reference |
| Future Energy Scenarios | Planning | National Grid ESO | Renewable capacity projections | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Renewable Energy Grid Management (Project 002)
**Model**: Claude Opus 4.6 (1M context)
