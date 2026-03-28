# Project Requirements: Flood Risk Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Flood Risk Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Flood Risk Management System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Environment Agency, DEFRA, Met Office, Lead Local Flood Authorities |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Flood Risk Management System. As a life-safety critical system, requirements are classified by their impact on public safety. This document is traceable to stakeholder analysis ARC-002-STKE-v1.0.

---

## Executive Summary

### Business Context

Flooding is the most significant natural hazard in England. Approximately 5.2 million properties are at risk of flooding from rivers, the sea, and surface water. The 2024 winter floods caused GBP 670M in damages and displaced 12,000 households. Climate change projections indicate a 30-60% increase in peak river flows by 2080 under RCP8.5 scenarios.

The Environment Agency operates the national Flood Warning Service under statutory duties in the Flood and Water Management Act 2010 and the Civil Contingencies Act 2004. The current system provides approximately 2 hours average warning lead time for fluvial flooding but has limited capability for surface water flood forecasting — the type of flooding that affects the most properties.

This programme will modernise the flood forecasting and warning system to double warning lead times, introduce surface water flood forecasting for Lead Local Flood Authorities, provide property-level flood intelligence for emergency responders, and launch a mobile-first public warning service.

### Objectives

- Increase average fluvial flood warning lead time from 2 hours to 4+ hours
- Deliver surface water flood forecasting capability to all 152 LLFAs
- Provide property-level flood depth predictions to Category 1 Responders
- Launch mobile app with location-aware personalised flood warnings
- Achieve 99.99% system availability during Met Office severe weather warnings

### Expected Outcomes

- 50% reduction in flood-related fatalities through earlier, more targeted warnings
- GBP 200M annual reduction in flood damage through improved emergency response preparation
- 70% of flood-risk properties receiving warnings via mobile push notification
- All 152 LLFAs with operational surface water flood forecasting

### Project Scope

**In Scope**:
- River level gauge telemetry system modernisation
- Hydrological forecasting model integration
- Met Office rainfall forecast data integration
- Surface water flood forecasting engine
- Rapid inundation mapping for property-level predictions
- Public warning dissemination (web, app, SMS, voice)
- Emergency responder decision support (Resilience Direct integration)
- LLFA surface water alerting service

**Out of Scope**:
- Physical flood defences and infrastructure
- Coastal erosion monitoring
- Water quality monitoring (Project 001)
- Emergency response coordination systems (Local Resilience Forum responsibility)

---

## Business Requirements

### BR-001: Extended Flood Warning Lead Time

**Description**: Increase the average flood warning lead time for fluvial (river) flooding from the current 2 hours to a minimum of 4 hours, enabling more effective evacuation and property protection.

**Rationale**: Every additional hour of warning reduces flood damage by approximately 20% (EA Flood Warning Cost-Benefit Study, 2023). The current 2-hour lead time is insufficient for effective property-level flood protection measures or safe evacuation of vulnerable residents.

**Success Criteria**:
- Average warning lead time >= 4 hours for fluvial flooding
- False alarm rate < 15% (down from current 25%)
- Warning coverage of actual flood events > 95%

**Priority**: MUST_HAVE
**Stakeholder**: EA Executive Director FCRM (SD-1)

---

### BR-002: Surface Water Flood Forecasting

**Description**: Deliver a surface water flood forecasting and alerting service that enables all 152 LLFAs in England to fulfil their statutory surface water flood risk management responsibilities.

**Rationale**: Surface water flooding affects more properties than fluvial flooding but currently has no forecasting or warning service. The Flood and Water Management Act 2010 gave LLFAs responsibility for surface water flood risk but provided no operational tools.

**Success Criteria**:
- All 152 LLFAs with access to surface water flood forecasting
- Surface water flood event detection rate > 70%
- LLFA user satisfaction > 80% "useful" or "very useful"

**Priority**: MUST_HAVE
**Stakeholder**: LLFAs (SD-3)

---

### BR-003: Property-Level Flood Intelligence

**Description**: Provide predicted flood depths at property level and road network impact assessments to Category 1 Responders within 30 minutes of a Flood Warning being issued.

**Rationale**: Emergency responders need actionable intelligence, not just area-based warnings. Property-level flood depth predictions enable targeted evacuation and resource deployment.

**Success Criteria**:
- Property-level predictions within 30 minutes of Flood Warning
- Depth accuracy within +/- 0.3m for 80% of properties
- Road network impact predictions for all A-roads and motorways

**Priority**: SHOULD_HAVE
**Stakeholder**: Category 1 Responders (SD-4)

---

### BR-004: Mobile-First Public Warning

**Description**: Launch a mobile application providing location-aware, personalised flood risk information and push notification warnings.

**Rationale**: Current Flood Warning Direct service reaches only 33% of at-risk properties. Post-event surveys show 35% of flooded residents received no warning. Mobile push notifications can reach citizens without pre-registration using location services.

**Success Criteria**:
- 3 million app downloads within 12 months
- Push notification delivery > 98% within 60 seconds
- Warning comprehension > 85% in user research

**Priority**: MUST_HAVE
**Stakeholder**: Citizens in flood-risk areas (SD-5)

---

## Functional Requirements

### FR-001: River Level Gauge Telemetry Ingestion

**Description**: Ingest real-time river level data from the EA's network of approximately 1,500 gauging stations with sub-minute latency.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given a gauge transmits a reading, when the platform receives it, then the reading is available to the forecasting engine within 90 seconds
- [ ] Given a gauge goes offline, when no data received for 2x reporting interval, then an automated alert is raised to the Area Flood Risk Manager
- [ ] Given a gauge reports an implausible reading (rate of change > 1m in 5 minutes without upstream trigger), then the reading is flagged for review

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-002: Hydrological Forecasting Engine

**Description**: Run ensemble hydrological flood forecasting models using observed river levels and Met Office ensemble rainfall predictions to produce probabilistic flood level forecasts.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given new river level and rainfall forecast data, when the model run is triggered, then ensemble forecasts (minimum 20 members) are produced within 15 minutes
- [ ] Given a forecast indicates >30% probability of Flood Warning threshold exceedance, then a Flood Guidance Statement is automatically generated
- [ ] Given a rapid-onset event (thunderstorm), when the model detects divergence from forecast, then an immediate re-run is triggered

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-003: Surface Water Flood Forecasting

**Description**: Generate surface water flood risk assessments combining Met Office rainfall forecasts with urban topography, drainage capacity, and soil moisture data.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a Met Office rainfall forecast exceeding surface water thresholds for a local authority area, when the surface water model runs, then a risk assessment is generated within 30 minutes
- [ ] Given an LLFA receives a surface water alert, then the alert includes affected areas, predicted ponding depths, and suggested response actions
- [ ] Given the alert system is used by an LLFA officer with no hydrological training, then the interface uses traffic-light risk levels with plain language explanations

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-004: Rapid Inundation Mapping

**Description**: Generate predicted flood extent and depth maps at property level within 30 minutes of a Flood Warning, using calibrated 2D hydraulic models and real-time river level data.

**Relates To**: BR-003

**Acceptance Criteria**:
- [ ] Given a Flood Warning is issued, when the rapid inundation model runs, then property-level flood depth maps are available within 30 minutes
- [ ] Given property-level depths are predicted, then affected properties are listed with predicted depth, time to peak, and recommended action
- [ ] Given road network data is available, then impassable roads are identified and alternative routes suggested

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

### FR-005: Mobile Application — Personalised Flood Warnings

**Description**: Native iOS and Android application providing location-aware flood risk information and push notification warnings.

**Relates To**: BR-004

**Acceptance Criteria**:
- [ ] Given a user enables location services, when a Flood Warning is issued for their area, then a push notification is delivered within 60 seconds
- [ ] Given a user opens the app, when they view the map, then their current location is shown with real-time flood risk status
- [ ] Given a Severe Flood Warning is issued, then the notification includes specific action instructions ("move to higher ground", "do not drive through floodwater")
- [ ] Given the user has limited connectivity, then the last-known flood risk status is available offline

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-006: Resilience Direct Integration

**Description**: Automatically publish flood forecasts, inundation maps, and property-level impact assessments to the multi-agency Resilience Direct platform for emergency responder access.

**Relates To**: BR-003

**Acceptance Criteria**:
- [ ] Given a Flood Warning is issued, when intelligence is generated, then it is published to Resilience Direct within 35 minutes
- [ ] Given intelligence includes predicted flood extents, then they are overlaid on Resilience Direct mapping with standard symbology
- [ ] Given a multi-agency incident is declared, then pre-formatted situation reports are auto-generated hourly

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Gauge Data Latency

**Requirement**: End-to-end latency from river level gauge reading to availability in the forecasting engine:
- Target: < 90 seconds (p95)
- Maximum acceptable: < 2 minutes (p99)

**Load Conditions**:
- Normal: 1,500 gauges reporting every 15 minutes = 100 readings/minute
- Storm event: 1,500 gauges reporting every 1 minute = 1,500 readings/minute
- Extreme: 1,500 gauges at 1-minute + 3,000 additional temporary gauges = 4,500 readings/minute

**Priority**: CRITICAL

---

#### NFR-P-2: Forecast Model Run Time

**Requirement**: Complete ensemble hydrological forecast run (minimum 20 members) within 15 minutes of trigger, including data retrieval, model execution, and output publication.

**Priority**: CRITICAL

---

#### NFR-P-3: Public App Performance

**Requirement**: Mobile application performance:
- App launch to interactive: < 3 seconds on 4G
- Push notification delivery: < 60 seconds from issue to device
- Map interaction: < 200ms response
- Offline mode: last-known state available without connectivity

**Priority**: CRITICAL

---

### Availability and Resilience Requirements

#### NFR-A-1: Life-Safety Availability

**Requirement**: System availability tiered by operational criticality:
- During Met Office Amber/Red weather warnings: 99.99% (5 minutes downtime per month)
- Normal winter flood season (October-March): 99.95% (22 minutes per month)
- Summer (April-September): 99.9% (44 minutes per month)

**Failover**: Automatic failover to secondary region within 2 minutes. Static fallback warning pages pre-deployed to CDN.

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: 0 minutes (no data loss for gauge telemetry — environmental evidence and safety-critical)
**RTO**: 5 minutes for forecasting engine during severe weather, 30 minutes otherwise

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: CNI Classification

**Requirement**: System is classified as Critical National Infrastructure under NIS Regulations 2018. Must comply with NCSC CAF (Cyber Assessment Framework) and HMG Security Policy Framework.

**Specific Controls**:
- [ ] Dedicated security operations monitoring during severe weather events
- [ ] Annual NCSC-coordinated penetration testing
- [ ] Supply chain security assessment for all third-party components
- [ ] Physical security for gauge telemetry communication infrastructure

**Priority**: CRITICAL

---

### Scalability Requirements

#### NFR-S-1: Storm Surge Capacity

**Requirement**: System must scale from baseline capacity to 10x within 5 minutes when Met Office issues Amber weather warning, and to 50x for Red warnings.

**Scaling Triggers**:
- Met Office Yellow warning: pre-scale to 3x baseline
- Met Office Amber warning: scale to 10x baseline
- Met Office Red warning: scale to 50x baseline
- Scaling must be automated — no manual intervention during severe weather events

**Priority**: CRITICAL

---

## Integration Requirements

### INT-001: Met Office Unified Model Integration

**Purpose**: Ingest deterministic and ensemble rainfall forecasts from the Met Office Unified Model for use in hydrological forecasting.

**Integration Type**: Real-time API + GRIB2 file transfer

**Data Exchanged**:
- **Met Office to EA**: Ensemble rainfall forecasts (MOGREPS-UK, 2.2km grid, 36hr forecast, hourly), deterministic UKV forecast, radar rainfall observations (1km, 5-minute)
- **EA to Met Office**: Observed river levels, flood model outputs (for Met Office Flood Guidance Statement)

**Authentication**: Mutual TLS with dedicated cross-agency link
**SLA**: Forecast data available within 10 minutes of Met Office model run completion
**Priority**: CRITICAL

---

### INT-002: Resilience Direct Platform

**Purpose**: Publish flood intelligence to the multi-agency emergency response platform.

**Integration Type**: Event-driven API (publish on warning/forecast update)

**Data Exchanged**:
- **EA to Resilience Direct**: Flood warnings, forecast data, inundation maps (GeoJSON), property impact lists, situation reports

**Priority**: HIGH

---

### INT-003: GOV.UK Notify Service

**Purpose**: Disseminate flood warnings via SMS, email, and letter channels.

**Integration Type**: REST API (GOV.UK Notify)

**Data Exchanged**:
- **EA to Notify**: Warning messages, recipient lists, personalisation data

**SLA**: Message submission to delivery < 60 seconds
**Priority**: CRITICAL

---

### INT-004: Apple/Google Push Notification Services

**Purpose**: Deliver mobile push notifications for flood warnings to app users.

**Integration Type**: REST API (APNs, FCM)

**SLA**: Notification delivery < 60 seconds from issue
**Priority**: CRITICAL

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Met Office Unified Model run times are fixed (00Z, 06Z, 12Z, 18Z). Flood forecasts cannot be more frequent than Met Office model updates unless using nowcasting techniques.

**TC-2**: 2D hydraulic models for rapid inundation mapping require pre-calibrated model domains. Coverage will be phased based on flood risk priority.

**TC-3**: Mobile push notifications require user opt-in on iOS. Cannot force-push without user consent.

### Business Constraints

**BC-1**: System must be operational for the 2027-28 winter flood season (October 2027).

**BC-2**: Programme budget capped at GBP 25M over 3 years.

**BC-3**: Joint EA/Met Office governance for the Flood Forecasting Centre must be maintained — no unilateral architectural decisions.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Fluvial warning lead time | 2 hours | 4 hours | Oct 2027 |
| False alarm rate | 25% | <15% | Oct 2027 |
| LLFAs with surface water forecasting | 0 | 152 | Mar 2028 |
| Mobile app downloads | 0 | 3 million | 12 months post-launch |
| Push notification delivery | N/A | <60 seconds | Launch |
| System availability (severe weather) | 99.9% | 99.99% | Oct 2027 |
| Flood-related fatalities | ~12/year (5yr avg) | <6/year | Year 2 |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Stakeholder Analysis | Architecture | ARC-002-STKE-v1.0 | Stakeholder drivers and goals | `projects/002-flood-risk-management-system/ARC-002-STKE-v1.0.md` |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | Governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Flood and Water Management Act 2010 | Legislation | legislation.gov.uk | EA flood warning duties | N/A — external reference |
| Civil Contingencies Act 2004 | Legislation | legislation.gov.uk | Category 1 Responder duties | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Flood Risk Management System (Project 002)
**AI Model**: Claude Opus 4.6 (1M context)
