# Project Requirements: Smart Transport Network

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Smart Transport Network (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart Transport Network Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart Transport Programme Board, DfT Digital, Network Rail, National Highways |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Smart Transport Network platform — a connected transport infrastructure management system that integrates real-time and timetabled data across bus, rail, road, and urban transit into a unified API and analytics platform.

---

## Executive Summary

### Business Context

UK transport data is fragmented across hundreds of organisations using different standards, systems, and governance models. Passengers outside London experience significantly inferior journey planning and real-time information compared to TfL users. The Bus Open Data Service (BODS) has improved bus data availability but quality remains variable — "ghost buses" (services shown but not running) are a persistent problem. Rail and road data exist in separate ecosystems with different standards. Combined authorities with new bus franchising powers need integrated multimodal data but are each building separate solutions at significant cost.

The Smart Transport Network platform will unify transport data across modes into a single API and analytics platform, improving passenger information quality, enabling cross-modal disruption management, and providing evidence for transport investment decisions.

### Objectives

- Integrate real-time and timetabled transport data across all modes into a unified API
- Improve bus real-time data quality (eliminate ghost buses, increase AVL coverage)
- Enable cross-modal disruption management with automated alternative route suggestions
- Provide transport authorities with analytics for network planning and performance monitoring
- Support journey planning applications with comprehensive, accurate multimodal data

### Expected Outcomes

- 15-point increase in Transport Focus passenger satisfaction for journey information
- 90% of bus services with reliable real-time AVL data (vs ~60% currently)
- Cross-modal disruption replan time reduced from 15 minutes to under 3 minutes
- Transport modelling costs reduced by 30% per major scheme
- 3-5% bus ridership increase from improved information (GBP 150-250M fare revenue over 5 years)

### Project Scope

**In Scope**:

- Bus data integration (BODS: timetables, real-time AVL, fares)
- Rail data integration (Network Rail Darwin: real-time, timetable)
- Strategic road network data (National Highways NTIS: incidents, traffic flow, variable message signs)
- Urban transit (TfL Unified API consumption, tram operators)
- NaPTAN stop/station reference data management
- Unified multimodal API for third-party consumers
- Data quality monitoring and "ghost bus" detection
- Cross-modal disruption management module
- Transport authority analytics dashboards

**Out of Scope**:

- Journey planning application (consumers of the API, not the platform itself)
- Ticketing and fares integration (separate programme)
- Active travel data (cycling, walking) — future phase
- Aviation and maritime transport
- Vehicle-to-infrastructure (V2I) connected vehicle data — future phase
- Local road network traffic data (153 highway authorities — future phase)

---

## Business Requirements

### BR-001: Unified Multimodal Transport Data API

**Description**: The platform must provide a single, unified API exposing timetable and real-time data for bus, rail, strategic road, and urban transit, enabling journey planning applications and transport authorities to consume comprehensive multimodal data from one source.

**Rationale**: Current fragmentation forces every journey planner, transport authority, and analytics tool to integrate separately with BODS, Darwin, NTIS, TfL, and individual operators — duplicating effort and creating inconsistency.

**Success Criteria**:

- API covers 95% of UK public transport services
- API latency < 200ms for timetable queries, < 500ms for real-time queries
- At least 50 third-party consumers using the API within 12 months of launch

**Priority**: MUST_HAVE

**Stakeholder**: DfT Secretary of State, Combined Authorities, Traveline

---

### BR-002: Bus Data Quality Improvement

**Description**: The platform must actively monitor and improve bus data quality, detecting ghost buses, late/missing real-time updates, and timetable-reality discrepancies, achieving 90% reliable real-time AVL coverage.

**Rationale**: Ghost buses are the number one passenger complaint about bus information. Current BODS data quality monitoring is limited. Without reliable data, passengers lose trust and choose private car over bus — undermining Net Zero transport objectives.

**Success Criteria**:

- 90% of bus services with reliable real-time AVL data
- Ghost bus detection rate >95%
- Data quality dashboards published for public transparency

**Priority**: MUST_HAVE

**Stakeholder**: DfT Bus Policy, Passengers, Combined Authorities

---

### BR-003: Cross-Modal Disruption Management

**Description**: The platform must enable automated cross-modal alternative route suggestions when disruption occurs, providing passengers with viable alternatives using other transport modes.

**Rationale**: When a train is cancelled, passengers need to know the next bus. When a motorway is closed, road users need public transport alternatives. Currently no system connects these modes for disruption response.

**Success Criteria**:

- Automated alternatives generated for all major corridor disruptions
- Passenger replan time reduced from 15 minutes to <3 minutes
- Alternatives available via API for third-party journey planners

**Priority**: SHOULD_HAVE

**Stakeholder**: Network Rail, National Highways, Combined Authorities, Passengers

---

### BR-004: Transport Authority Analytics

**Description**: The platform must provide transport authorities with analytics dashboards for network performance monitoring, service planning, and investment evidence.

**Rationale**: Combined authorities with franchising powers need integrated data to plan bus networks alongside rail and road. Currently each authority builds separate analytics at significant cost.

**Success Criteria**:

- Analytics dashboards available for all combined authority areas
- Performance metrics: punctuality, frequency, coverage, demand indicators
- Data exportable for transport modelling tools (EMME, SATURN, Visum)

**Priority**: SHOULD_HAVE

**Stakeholder**: Combined Authorities, DfT

---

## Functional Requirements

### User Personas

#### Persona 1: Journey Planning API Consumer

- **Role**: Developer at journey planning company or combined authority
- **Goals**: Consume comprehensive, accurate multimodal data via API
- **Pain Points**: Must currently integrate 5+ separate APIs; data format inconsistencies; varying reliability
- **Technical Proficiency**: High

#### Persona 2: DfT Bus Data Quality Analyst

- **Role**: Monitors BODS compliance and data quality
- **Goals**: Identify operators with poor data quality; track improvement over time
- **Pain Points**: Limited tooling for data quality analysis; manual investigation of complaints
- **Technical Proficiency**: Medium-High

#### Persona 3: Network Rail Disruption Manager

- **Role**: Manages incident response and passenger information during rail disruptions
- **Goals**: Quickly identify cross-modal alternatives for disrupted passengers
- **Pain Points**: No visibility of bus services near affected stations; manual coordination via phone
- **Technical Proficiency**: Medium

#### Persona 4: Combined Authority Transport Planner

- **Role**: Plans bus network under franchising powers
- **Goals**: Understand multimodal travel patterns; model impact of service changes
- **Pain Points**: Data fragmented by mode; no single view of transport in their area
- **Technical Proficiency**: Medium-High

---

### Functional Requirements Detail

#### FR-001: BODS Data Ingestion

**Description**: The system must ingest bus open data from the Bus Open Data Service (BODS) including timetables (TransXChange), real-time vehicle locations (SIRI-VM), and fares data.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Ingest TransXChange timetable data for all registered bus services in England
- [ ] Ingest SIRI-VM real-time AVL feeds from all participating operators
- [ ] Ingest bus fares data (NeTEx format) when available
- [ ] Data refresh: timetables daily, real-time continuous (< 30 second lag)
- [ ] Handle TransXChange schema versions 2.1 and 2.4

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: Rail Data Ingestion (Darwin)

**Description**: The system must ingest real-time train running data from Network Rail's Darwin feed and timetable data from ATOC/RDG.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Consume Darwin Push Port feed for real-time train movements
- [ ] Ingest planned timetable data (CIF format)
- [ ] Map Darwin station codes to NaPTAN stop identifiers
- [ ] Handle service cancellations, delays, platform changes, and late notices
- [ ] Data latency: < 15 seconds from Darwin publication to API availability

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-003: Strategic Road Network Data Ingestion

**Description**: The system must ingest National Highways NTIS data including traffic flow, incidents, roadworks, and variable message signs via DATEX II protocol.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:

- [ ] Ingest DATEX II feeds for incidents, roadworks, and traffic flow
- [ ] Map road locations to geographic coordinates for spatial queries
- [ ] Classify incident severity for disruption management triggers
- [ ] Data latency: < 60 seconds from NTIS publication

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-004: Unified Multimodal API

**Description**: The system must expose a unified REST API providing normalised access to timetable and real-time data across all integrated modes.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] API provides departure boards for any NaPTAN stop/station (all modes)
- [ ] API provides real-time vehicle positions within a geographic bounding box
- [ ] API provides timetable data by route, stop, operator, and time range
- [ ] API supports GTFS and GTFS-RT output formats for international interoperability
- [ ] API supports GeoJSON output for spatial queries
- [ ] API rate limiting: 1,000 requests/minute per consumer (configurable)
- [ ] API documentation published using OpenAPI 3.0 specification

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-005: Ghost Bus Detection

**Description**: The system must automatically detect "ghost buses" — services shown as running in timetable data but with no corresponding real-time vehicle position data — and flag these for operator investigation.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Compare timetabled departures against real-time AVL data in near-real-time
- [ ] Flag services with no AVL data within 5 minutes of scheduled departure
- [ ] Distinguish between: (a) service not running, (b) AVL equipment failure, (c) service running but delayed
- [ ] Daily ghost bus report per operator published to data quality dashboard
- [ ] Alert operators when ghost bus rate exceeds threshold (configurable per operator)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Cross-Modal Alternative Routes

**Description**: The system must generate cross-modal alternative route suggestions when disruption is detected, identifying viable bus alternatives for cancelled trains and public transport alternatives for road closures.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Detect disruption events from rail (cancellations, significant delays) and road (closures, severe congestion)
- [ ] For each affected station/junction, identify bus services within 1km catchment
- [ ] Generate alternative multimodal route suggestions with estimated journey times
- [ ] Publish alternatives via API within 2 minutes of disruption detection
- [ ] Include walking directions from station to nearest bus stop (using OS road network)

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-007: NaPTAN Reference Data Management

**Description**: The system must maintain and serve NaPTAN (National Public Transport Access Nodes) reference data as the authoritative stop and station identifier set.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Ingest NaPTAN dataset with daily update cycle
- [ ] Expose NaPTAN search API (by name, location, ATCO code, NaPTAN ID)
- [ ] Map between NaPTAN identifiers and operator-specific stop identifiers
- [ ] Track stop/station status (active, temporarily closed, permanently closed)

**Priority**: MUST_HAVE

**Complexity**: LOW

---

#### FR-008: Data Quality Dashboard

**Description**: The system must provide public and operator-facing dashboards showing data quality metrics by operator, mode, and geographic area.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Display real-time AVL coverage percentage per operator
- [ ] Display ghost bus rate per operator (daily, weekly, monthly trends)
- [ ] Display timetable accuracy (scheduled vs actual) per operator
- [ ] Public dashboard available without authentication
- [ ] Operator-specific detailed view with authentication

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: API Response Time

**Requirement**: Unified API p95 response time < 200ms for timetable queries, < 500ms for real-time queries including spatial search.

**Load Conditions**: 10,000 concurrent API consumers; 50,000 requests/minute peak

**Priority**: MUST_HAVE

---

#### NFR-P-002: Real-Time Data Latency

**Requirement**: End-to-end latency from operator data source to API availability: < 30 seconds for bus SIRI-VM, < 15 seconds for rail Darwin, < 60 seconds for road DATEX II.

**Priority**: MUST_HAVE

---

#### NFR-P-003: Data Ingestion Throughput

**Requirement**: System must handle ingestion of 500,000+ real-time vehicle position updates per minute across all modes during peak hours (07:00-09:00, 16:00-18:00).

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.95% availability for the unified API (26 minutes downtime per year). Real-time data feeds are critical infrastructure for passenger information.

**Priority**: MUST_HAVE

---

#### NFR-A-002: Disaster Recovery

**RPO**: 5 minutes for real-time data, 1 hour for reference data | **RTO**: 15 minutes

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: API Authentication

**Requirement**: All API consumers must authenticate via API key with OAuth 2.0 for elevated access. Rate limiting enforced per consumer.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Data Protection

**Requirement**: No personal data in the transport data model. Vehicle tracking data does not identify individuals. Real-time positions published with 30-second delay to prevent misuse.

**Priority**: MUST_HAVE

---

### Interoperability Requirements

#### NFR-I-001: Transport Data Standards

**Requirement**: System must support the following transport data standards:

- TransXChange 2.1 and 2.4 (bus timetables)
- SIRI-VM 2.0 (bus real-time)
- SIRI-SX (situation exchange / disruptions)
- CIF (Common Interface Format — rail timetables)
- DATEX II (road data)
- NeTEx (fares)
- GTFS and GTFS-RT (international interoperability output)
- NaPTAN (stop/station identifiers)

**Priority**: MUST_HAVE

---

#### NFR-I-002: Geospatial Standards

**Requirement**: All spatial data served in WGS84 (EPSG:4326) for web mapping. NaPTAN coordinates in OSGB36 transformed to WGS84 using OSTN15. GeoJSON output for all spatial queries.

**Priority**: MUST_HAVE

---

### Usability Requirements

#### NFR-U-001: API Developer Experience

**Requirement**: API documentation published using OpenAPI 3.0 with interactive sandbox. Onboarding from registration to first API call achievable in under 30 minutes.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Bus Open Data Service (BODS)

**Purpose**: Primary source of bus timetable, real-time, and fares data for England

**Integration Type**: Real-time streaming (SIRI-VM) + batch (TransXChange timetables)

**Data Exchanged**: Timetables (TransXChange), real-time positions (SIRI-VM), fares (NeTEx)

**SLA**: BODS availability aligned — if BODS is down, bus data is stale

**Priority**: MUST_HAVE

---

### INT-002: Network Rail Darwin

**Purpose**: Real-time train running data

**Integration Type**: Real-time streaming (Darwin Push Port)

**Data Exchanged**: Train movements, cancellations, delays, platform changes

**Authentication**: Darwin data feed subscription

**Priority**: MUST_HAVE

---

### INT-003: National Highways NTIS

**Purpose**: Strategic road network incidents, roadworks, and traffic flow

**Integration Type**: Real-time streaming (DATEX II)

**Data Exchanged**: Incidents, roadworks, traffic flow, VMS messages

**Authentication**: NTIS data feed subscription

**Priority**: SHOULD_HAVE

---

### INT-004: TfL Unified API

**Purpose**: London transport data (Tube, bus, DLR, Overground, Elizabeth line, tram)

**Integration Type**: Real-time API consumption

**Data Exchanged**: Departures, line status, arrivals, vehicle positions

**Authentication**: TfL API key

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Stop/Station (NaPTAN)

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| naptan_id | String | Yes | NaPTAN identifier |
| atco_code | String | Yes | ATCO code for bus stops |
| name | String | Yes | Stop/station name |
| latitude | Decimal | Yes | WGS84 latitude |
| longitude | Decimal | Yes | WGS84 longitude |
| stop_type | Enum | Yes | Bus, Rail, Tram, Ferry |
| status | Enum | Yes | Active, Temporary_Closed, Closed |

**Data Volume**: ~400,000 stops and stations

#### Entity 2: Vehicle Position

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| vehicle_id | String | Yes | Operator vehicle identifier |
| mode | Enum | Yes | Bus, Rail, Tram |
| operator_id | String | Yes | Operator code |
| latitude | Decimal | Yes | WGS84 latitude |
| longitude | Decimal | Yes | WGS84 longitude |
| bearing | Integer | No | Direction of travel (degrees) |
| speed | Decimal | No | Speed in km/h |
| timestamp | Timestamp | Yes | Position timestamp |
| trip_id | String | No | Timetable trip reference |

**Data Volume**: ~100,000 active vehicles at peak, ~500,000 position updates per minute

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Year 1-2) | GBP 12.0M | 30 FTE delivery team |
| Infrastructure (Year 1-3) | GBP 4.0M | Cloud hosting, streaming infrastructure |
| Data feed subscriptions | GBP 0.5M | Darwin, NTIS, TfL |
| Security and compliance | GBP 0.5M | Pen testing, GDS assessment |
| Contingency (15%) | GBP 2.6M | |
| **Total** | **GBP 19.6M** | Over 3 years |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Cloud infrastructure | GBP 2.5M | Streaming, compute, storage |
| BAU team | GBP 2.0M | 12 FTE |
| Data feed subscriptions | GBP 0.2M | Annual renewals |
| **Total** | **GBP 4.7M/year** | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-002-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | `projects/002-smart-transport-network/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart Transport Network (Project 002)
**Model**: Claude Opus 4.6
