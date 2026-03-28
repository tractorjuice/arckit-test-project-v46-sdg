# Project Requirements: Water Quality Monitoring Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Water Quality Monitoring Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Quality Monitoring Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Environment Agency, Ofwat, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Water Quality Monitoring Platform. It provides the basis for architecture design, procurement, and acceptance testing. Requirements are traceable to stakeholder drivers documented in ARC-001-STKE-v1.0.

---

## Executive Summary

### Business Context

The UK faces a water quality crisis. Sewage discharges into rivers and coastal waters have become the dominant environmental issue, with water companies recording over 3.6 million hours of storm overflow spills in 2023. The Environment Act 2021 introduced legally binding duties for continuous monitoring of storm overflows and progressive reduction targets under the Storm Overflow Discharge Reduction Plan.

DEFRA requires a national platform that aggregates water quality monitoring data from multiple sources — Environment Agency monitoring networks, water company self-monitoring systems, citizen science programmes, and new IoT sensor deployments — into a single, authoritative, publicly accessible service. This platform will underpin regulatory enforcement, Water Framework Directive reporting, public health advisories, and public transparency.

### Objectives

- Deploy real-time water quality monitoring at all 424 designated bathing waters in England
- Integrate continuous monitoring data from 15,000+ storm overflow discharge points
- Automate Water Framework Directive water body classification calculations
- Publish all water quality data as 5-star open data with API access
- Provide real-time public dashboards for bathing water quality and storm overflow status

### Expected Outcomes

- 25% reduction in bathing water-related illness through real-time contamination alerts
- 40% increase in successful pollution prosecution rate through evidence-quality continuous data
- 60% reduction in EA manual sampling effort through automated continuous monitoring
- 90%+ public awareness of water quality data availability within 3 years

### Project Scope

**In Scope**:
- IoT sensor network management for bathing water and storm overflow monitoring
- Data ingestion from water company operational telemetry (EDMs, flow monitors, SCADA)
- Data ingestion from EA National Laboratory Service analytical results
- Real-time public dashboards for bathing water quality and storm overflow status
- Open data API and bulk download service
- WFD water body classification automation
- Integration with DEFRA Data Services Platform and data.gov.uk

**Out of Scope**:
- Flood monitoring and forecasting (covered by Project 002)
- Water company internal SCADA system upgrades (water company responsibility)
- Drinking water quality monitoring (Drinking Water Inspectorate remit)
- Marine water quality beyond designated bathing waters (Cefas remit)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| DEFRA Water Quality Policy Director | Programme Sponsor | DEFRA | Decision maker |
| EA Director of Water Quality | Delivery Partner Lead | Environment Agency | Requirements, operations |
| Ofwat Director of Strategy | Regulatory Data Consumer | Ofwat | Performance data requirements |
| DEFRA CDIO | Technical Authority | DEFRA | Architecture oversight |
| DEFRA Chief Scientific Adviser | Methodology Authority | DEFRA | Data quality assurance |
| Water UK Technical Lead | Industry Coordinator | Water UK | Integration requirements |
| UKHSA Environmental Health Lead | Public Health Consumer | UKHSA | Health advisory requirements |

---

## Business Requirements

### BR-001: National Water Quality Data Aggregation

**Description**: Aggregate water quality monitoring data from all sources (EA sensors, water company telemetry, laboratory analysis, citizen science) into a single national platform providing a unified view of water quality across English waterways.

**Rationale**: Currently water quality data is fragmented across multiple EA databases (WIMS, bathing water explorer), water company systems, and third-party sources. No single view exists, preventing effective national-level analysis and public transparency.

**Success Criteria**:
- All 424 designated bathing waters monitored in real-time
- 15,000+ storm overflows integrated with continuous monitoring data
- 4,864 WFD surface water bodies with classification data
- Single API providing access to all water quality data sources

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Water Quality Policy Director (SD-1)

---

### BR-002: Public Transparency and Open Data

**Description**: Publish all non-sensitive water quality data as open data at 5-star open data standard, enabling public scrutiny, academic research, and third-party innovation.

**Rationale**: The Environmental Information Regulations 2004 create a presumption of public access to environmental data. The 25 Year Environment Plan commits to transparent environmental data. Public trust requires independent, accessible data — particularly given the sewage discharge crisis.

**Success Criteria**:
- 5-star open data score (linked, machine-readable, open format, open licence, linked data)
- 50+ third-party applications using the API within 12 months
- 1 million+ data downloads per year
- 100% of published data has quality status flags

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Secretary of State (SD-1), Campaign groups (SD-5)

---

### BR-003: Regulatory Enforcement Support

**Description**: Provide the Environment Agency with evidence-quality water quality data that supports regulatory investigation and prosecution of water pollution offences.

**Rationale**: EA enforcement capability is currently constrained by periodic manual sampling. Continuous monitoring data enables detection of intermittent pollution events and provides temporal evidence for prosecution.

**Success Criteria**:
- Data provenance chain meeting Crown Prosecution Service evidence standards
- Automated alerting when pollution thresholds exceeded
- Investigation time reduction from 18 months to 7 months average

**Priority**: MUST_HAVE

**Stakeholder**: EA Director of Water Quality (SD-2)

---

### BR-004: WFD Reporting Automation

**Description**: Automate Water Framework Directive water body classification calculations, enabling annual provisional assessments instead of the current 6-yearly manual classification cycle.

**Rationale**: The current 6-year WFD classification cycle is too slow for responsive regulatory action. Automated provisional assessments using continuous data would enable earlier intervention when water body status is deteriorating.

**Success Criteria**:
- Automated provisional classification for all 4,864 surface water bodies
- >95% concordance with manual classification methodology
- Classification update within 30 days of data collection

**Priority**: SHOULD_HAVE

**Stakeholder**: EA Director of Water Quality (SD-2), Ofwat (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: Environmental Monitoring Officer (EA)

- **Role**: EA field officer responsible for water quality monitoring
- **Goals**: Monitor sensor health, investigate pollution alerts, compile regulatory evidence
- **Pain Points**: Manual data collection, delayed laboratory results, multiple disconnected systems
- **Technical Proficiency**: Medium-High

#### Persona 2: Citizen Water Quality Checker

- **Role**: Member of public wanting to check if a bathing water or river is safe
- **Goals**: Quick, clear answer on water quality at a specific location
- **Pain Points**: Confusing scientific terminology, outdated data, no mobile access
- **Technical Proficiency**: Low

#### Persona 3: Water Company Environmental Manager

- **Role**: Water company staff responsible for environmental compliance
- **Goals**: Monitor treatment works performance, track storm overflow activity, submit regulatory returns
- **Pain Points**: Multiple reporting requirements, inconsistent data standards, manual data collation
- **Technical Proficiency**: High

#### Persona 4: Open Data Developer

- **Role**: Third-party developer building applications using water quality data
- **Goals**: Programmatic access to comprehensive, well-documented, reliable water quality data
- **Pain Points**: Inconsistent APIs, poor documentation, unreliable data availability
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: IoT Sensor Data Ingestion

**Description**: Ingest real-time telemetry data from IoT water quality sensors deployed at bathing waters, river monitoring stations, and storm overflow discharge points.

**Relates To**: BR-001

**Acceptance Criteria**:
- [ ] Given a sensor reading is transmitted, when the platform receives it, then the reading is stored within the latency SLA (see NFR-P-1)
- [ ] Given a sensor transmits an out-of-range value, when the platform validates it, then the reading is flagged as suspect and not published until reviewed
- [ ] Given a sensor goes offline, when the platform detects no data for 2x the expected reporting interval, then an automated health alert is raised

**Data Requirements**:
- **Inputs**: Sensor ID, timestamp (UTC), parameter code, measured value, unit, quality flag, GPS coordinates, battery level, signal strength
- **Outputs**: Validated time-series records, sensor health status, data quality metrics
- **Validations**: Range checks per parameter, rate-of-change checks, cross-sensor consistency

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: Sensor network deployment (external programme)

---

#### FR-002: Water Company Data Feed Integration

**Description**: Ingest data from water company operational telemetry systems including Event Duration Monitors (EDMs), flow monitors, and SCADA systems via standardised APIs.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:
- [ ] Given a water company submits EDM data via the API, when the data passes validation, then it is ingested within the latency SLA
- [ ] Given a water company data feed fails, when the platform detects the failure, then an automated alert is sent to the company and EA within 30 minutes
- [ ] Given data is submitted in a non-compliant format, when validation fails, then a detailed error message is returned with the specific validation failure

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-003: Real-Time Public Dashboard — Bathing Water Quality

**Description**: Provide a public-facing web application displaying real-time water quality status at all designated bathing waters, with map-based navigation, parameter detail, and historical trends.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a citizen navigates to the dashboard, when they select a bathing water, then the current water quality status is displayed with a clear safe/caution/poor indicator
- [ ] Given new sensor data arrives, when it is validated, then the dashboard updates within 5 minutes
- [ ] Given a citizen uses a mobile device on 3G connection, when loading the dashboard, then the page is interactive within 3 seconds

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-004: Real-Time Public Dashboard — Storm Overflow Status

**Description**: Provide a public-facing web application displaying real-time storm overflow discharge status for all 15,000+ overflows, with duration tracking, frequency statistics, and regulatory context.

**Relates To**: BR-002, BR-003

**Acceptance Criteria**:
- [ ] Given a citizen views the storm overflow map, when an overflow is actively discharging, then it is displayed with a clear visual indicator and duration counter
- [ ] Given an overflow event ends, when the EDM reports cessation, then the dashboard updates within 1 hour showing event duration
- [ ] Given a citizen selects a specific overflow, then permit conditions, event history, and receiving water body are displayed

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-005: Open Data API

**Description**: Provide a RESTful API with OGC-compliant geospatial services enabling programmatic access to all published water quality data.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a developer queries the API for a specific station, when the request is valid, then current and historical readings are returned in JSON/GeoJSON format
- [ ] Given a developer requests bulk download for a catchment, when the area is valid, then data is returned as a downloadable file (CSV, GeoJSON, GeoPackage)
- [ ] Given the API receives a malformed request, when validation fails, then a standardised error response (RFC 7807) is returned

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-006: WFD Classification Engine

**Description**: Implement automated Water Framework Directive water body classification calculations using the EA's published methodology, producing provisional status assessments.

**Relates To**: BR-004

**Acceptance Criteria**:
- [ ] Given continuous monitoring data for a water body, when a classification run is triggered, then ecological and chemical status are calculated using the one-out-all-out principle
- [ ] Given a classification result differs from the previous assessment, when the difference is >1 status class, then a manual review flag is raised
- [ ] Given methodology parameters are updated, then previous classifications can be recalculated under the new methodology

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

#### FR-007: Automated Pollution Alerting

**Description**: Detect potential pollution events from sensor data patterns and automatically alert EA monitoring officers with event details, location, and likely source.

**Relates To**: BR-003

**Acceptance Criteria**:
- [ ] Given sensor readings exceed pollution thresholds, when the exceedance is confirmed by 2 consecutive readings, then an alert is sent to the EA duty officer within 5 minutes
- [ ] Given an alert is raised, then the alert includes location, parameter, readings, trend, upstream context, and nearby permitted discharges
- [ ] Given a false alarm is identified, then the officer can dismiss it with a reason code for machine learning improvement

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Data Ingestion Latency

**Requirement**: End-to-end data latency from sensor reading to platform availability:
- Flood/pollution alerts: < 2 minutes
- Bathing water quality: < 5 minutes
- Storm overflow status: < 15 minutes
- Routine monitoring: < 60 minutes

**Measurement Method**: Automated latency monitoring comparing sensor timestamp to platform ingestion timestamp

**Load Conditions**:
- Normal: 5,000 sensor readings per minute
- Storm event: 50,000 sensor readings per minute (10x burst)
- Annual peak: 100,000 readings per minute during severe weather events

**Priority**: CRITICAL

---

#### NFR-P-2: Dashboard Response Time

**Requirement**: Public dashboard page load and interaction performance:
- Map initial load: < 3 seconds on 4G, < 5 seconds on 3G
- Station detail page: < 2 seconds
- Map pan/zoom: < 200ms per interaction
- Search: < 1 second for results

**Priority**: HIGH

---

#### NFR-P-3: API Response Time

**Requirement**: API response times at 95th percentile:
- Single station current reading: < 200ms
- Station historical data (1 year): < 2 seconds
- Catchment aggregate query: < 5 seconds
- Bulk export initiation: < 10 seconds (async job)

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Platform Availability

**Requirement**:
- Public dashboard: 99.9% availability (8.7 hours downtime per year)
- Data ingestion pipeline: 99.95% availability (4.4 hours downtime per year)
- API: 99.9% availability
- During bathing season (May-September): 99.95% for dashboard

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: 0 minutes for sensor data (no data loss acceptable — environmental evidence)
**RTO**: 30 minutes for data ingestion, 2 hours for public dashboard

**Backup Requirements**:
- Continuous replication to secondary region
- Point-in-time recovery capability for 30 days
- Annual DR test with documented results

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: CNI Security Controls

**Requirement**: Platform classified as supporting Critical National Infrastructure. Must comply with NCSC CAF (Cyber Assessment Framework) for water sector operators and NIS Regulations 2018.

**Mandatory Controls**:
- [ ] Network segmentation between IoT ingestion layer and application layer
- [ ] Mutual TLS for all sensor-to-platform communication
- [ ] DDoS protection for public-facing services
- [ ] NCSC-approved encryption for data at rest and in transit
- [ ] Annual penetration testing including IoT attack vectors
- [ ] Incident response plan coordinated with NCSC

**Priority**: CRITICAL

---

#### NFR-SEC-2: Data Classification and Access Control

**Requirement**: Role-based access control enforcing data classification:
- Open environmental data: public access (no authentication)
- Enforcement investigation data: EA enforcement officers only
- Water company pre-publication data: company-specific access
- System administration: MFA-protected, privileged access management

**Priority**: CRITICAL

---

### IoT-Specific Requirements

#### NFR-IOT-1: Sensor Uptime

**Requirement**: Deployed IoT sensors must maintain 99.5% availability measured monthly, with 99.9% during high-risk periods (bathing season, storm events).

**Measurement Method**: Automated sensor health monitoring — sensor is "available" when reporting readings within expected intervals.

**Priority**: CRITICAL

---

#### NFR-IOT-2: Sensor Data Quality

**Requirement**: Automated data quality checks must flag at minimum:
- Out-of-range values (configurable per parameter)
- Stuck sensor readings (identical values for > 6 hours)
- Rate-of-change violations (physiologically impossible changes)
- Calibration drift (deviation from co-located reference instrument)

**Priority**: HIGH

---

#### NFR-IOT-3: Sensor Communication Resilience

**Requirement**: Sensors must support store-and-forward capability for minimum 72 hours of readings during communication outages, with automatic data backfill when connectivity is restored.

**Priority**: HIGH

---

### Geospatial Requirements

#### DR-GEO-1: Coordinate Reference Systems

**Requirement**: All spatial data must be stored with explicit CRS metadata. Platform must support:
- British National Grid (OSGB36 / EPSG:27700) for UK mapping
- WGS84 (EPSG:4326) for GPS and web mapping
- Dynamic re-projection between CRS on request

**Priority**: MUST_HAVE

---

#### DR-GEO-2: Spatial Data Standards

**Requirement**: All spatial data services must comply with OGC standards:
- WMS 1.3.0 for map image services
- WFS 2.0 for vector feature services
- GeoJSON for API responses
- GeoPackage for bulk download

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Environment Agency WIMS Integration

**Purpose**: Bidirectional integration with EA's Water Information Management System (WIMS) — the authoritative database for water quality monitoring results.

**Integration Type**: Real-time API (new data push) + batch reconciliation (daily)

**Data Exchanged**:
- **Platform to WIMS**: Validated sensor readings, automated quality flags
- **WIMS to Platform**: Laboratory analytical results, manual sampling data, historical records

**Authentication**: Mutual TLS with EA API gateway
**SLA**: < 5 minute latency for real-time push, daily reconciliation by 06:00 UTC
**Priority**: CRITICAL

---

### INT-002: Met Office Rainfall Data

**Purpose**: Ingest real-time and forecast rainfall data to contextualise water quality readings and predict storm overflow events.

**Integration Type**: Real-time API (Met Office DataHub)

**Data Exchanged**:
- **Met Office to Platform**: Rainfall radar observations (5-minute intervals), rainfall gauge network data, weather forecast data (rainfall probability, intensity)

**Authentication**: API key via Met Office DataHub
**SLA**: < 10 minute latency for radar observations
**Priority**: HIGH

---

### INT-003: Water Company EDM/SCADA Feeds

**Purpose**: Ingest Event Duration Monitor and SCADA data from 11 water and sewerage companies.

**Integration Type**: Real-time API (company push to platform API)

**Data Exchanged**:
- **Water Companies to Platform**: EDM status (spilling/not spilling), flow rates, treatment works operational parameters

**Authentication**: OAuth 2.0 with company-specific client credentials
**Error Handling**: Automated data gap alerts, company notification within 30 minutes of detected feed failure
**SLA**: < 15 minute latency for EDM data
**Priority**: CRITICAL

---

### INT-004: DEFRA Data Services Platform

**Purpose**: Publish validated water quality data to DEFRA's Data Services Platform for open data distribution.

**Integration Type**: Event-driven (publish on validation complete)

**Data Exchanged**:
- **Platform to DEFRA DSP**: Validated water quality datasets, metadata records, quality reports

**Priority**: HIGH

---

### INT-005: UKHSA Health Protection Systems

**Purpose**: Automated alerting to UKHSA when bathing water quality exceeds health-relevant thresholds.

**Integration Type**: Event-driven (webhook notification)

**Data Exchanged**:
- **Platform to UKHSA**: Bathing water alert notifications (location, parameters, values, advisory recommendation)

**Priority**: HIGH

---

## Data Requirements

### Data Entities

#### Entity: Water Quality Reading

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| reading_id | UUID | Yes | Unique reading identifier | Primary key |
| station_id | String(20) | Yes | Monitoring station identifier | FK to Station |
| timestamp | Timestamp(UTC) | Yes | Reading timestamp at source | Not null, indexed |
| parameter_code | String(10) | Yes | Determinand code (EA coding) | FK to Parameter |
| value | Decimal(12,4) | Yes | Measured value | Range-checked per parameter |
| unit | String(20) | Yes | Measurement unit | Controlled vocabulary |
| quality_flag | Enum | Yes | Data quality status | ['raw','validated','suspect','rejected'] |
| method_code | String(10) | No | Analytical method | Controlled vocabulary |
| source_system | String(50) | Yes | Originating system | Not null |
| ingestion_timestamp | Timestamp(UTC) | Yes | Platform receipt time | Auto-generated |

**Data Volume**: ~500 million readings per year (Year 1), growing to ~2 billion per year by Year 3
**Data Classification**: OFFICIAL — Open Environmental Data
**Data Retention**: Indefinite (environmental monitoring records)

#### Entity: Monitoring Station

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| station_id | String(20) | Yes | Unique station identifier | Primary key |
| station_name | String(200) | Yes | Human-readable name | Not null |
| station_type | Enum | Yes | Station category | ['bathing_water','river','storm_overflow','treatment_works'] |
| easting | Integer | Yes | OSGB36 easting | Valid range |
| northing | Integer | Yes | OSGB36 northing | Valid range |
| latitude | Decimal(9,6) | Yes | WGS84 latitude | -90 to 90 |
| longitude | Decimal(9,6) | Yes | WGS84 longitude | -180 to 180 |
| wfd_water_body_id | String(20) | No | WFD water body reference | FK to WFD register |
| operator | String(100) | Yes | Operating organisation | Not null |
| status | Enum | Yes | Operational status | ['active','maintenance','decommissioned'] |

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with EA's existing WIMS database which uses Oracle 19c and cannot be replaced within this programme's scope.

**TC-2**: Water company SCADA systems use diverse protocols (Modbus, DNP3, OPC-UA). Platform must accept data via standardised API — protocol translation is water company responsibility.

**TC-3**: IoT sensor deployment at bathing waters requires landowner consent. Platform must function with partial sensor coverage during phased rollout.

### Business Constraints

**BC-1**: Public dashboard must be operational before the 2027 bathing season (May 2027) — this is a Ministerial commitment.

**BC-2**: Total programme budget capped at GBP 18M over 3 years (capital + operational).

**BC-3**: Must use UK-sovereign cloud hosting (UK Government Cloud First policy, NIS Regulations).

### Assumptions

**A-1**: Water companies will comply with statutory obligations to provide data feeds. If challenged, DEFRA/Ofwat will exercise enforcement powers.

**A-2**: Cellular network coverage is available at 90%+ of bathing water sites. Satellite backup required for remaining sites.

**A-3**: EA National Laboratory Service will continue providing reference sample analysis for sensor calibration validation.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Bathing waters with real-time monitoring | 85 (pilot) | 424 | May 2027 | Sensor deployment register |
| Storm overflows integrated | 0 (platform) | 15,000+ | Dec 2027 | Platform ingestion metrics |
| Public dashboard monthly visitors | 0 | 2 million | 12 months post-launch | Web analytics |
| Open data API consumers | 0 | 50+ | 12 months post-launch | API key registrations |
| EA manual sampling reduction | 1M samples/year | 400K samples/year | Year 2 | EA sampling programme data |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| DEFRA Water Quality Policy Director | Programme Sponsor | [ ] Approved | | |
| EA Director of Water Quality | Delivery Partner | [ ] Approved | | |
| DEFRA CDIO | Technical Authority | [ ] Approved | | |
| DEFRA SIRO | Information Risk | [ ] Approved | | |
| Ofwat Director of Strategy | Regulatory Consumer | [ ] Approved | | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|------------|
| EDM | Event Duration Monitor — device recording when storm overflows are discharging |
| SCADA | Supervisory Control and Data Acquisition — industrial control system for treatment works |
| WIMS | Water Information Management System — EA's water quality database |
| WFD | Water Framework Directive — EU directive (retained in UK law) governing water quality |
| WRE | Water Resources East — one of 5 regional water resource groups |
| OSGB36 | Ordnance Survey Great Britain 1936 — British National Grid coordinate system |
| OGC | Open Geospatial Consortium — standards body for geospatial data |
| CRS | Coordinate Reference System |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Stakeholder Analysis | Architecture | ARC-001-STKE-v1.0 | Stakeholder drivers and goals | `projects/001-water-quality-monitoring-platform/ARC-001-STKE-v1.0.md` |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | Governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Environment Act 2021 | Legislation | legislation.gov.uk | Monitoring duties | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Quality Monitoring Platform (Project 001)
**AI Model**: Claude Opus 4.6 (1M context)
