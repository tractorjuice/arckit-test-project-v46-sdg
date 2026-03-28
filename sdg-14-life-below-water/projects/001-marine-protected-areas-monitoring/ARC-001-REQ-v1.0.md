# Project Requirements: Marine Protected Areas Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Marine Protected Areas Monitoring (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Owner, MPA Monitoring Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MPA Programme Board, DEFRA Digital, JNCC, Natural England, Cefas, MMO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies the business, functional, non-functional, integration, and data requirements for the Marine Protected Areas Monitoring platform. It provides the authoritative requirements baseline for architecture design, development, testing, and acceptance.

---

## Executive Summary

### Business Context

The United Kingdom has designated 178 Marine Protected Areas — 91 Marine Conservation Zones (MCZs) under the Marine and Coastal Access Act 2009, and 87 Special Areas of Conservation (SACs) and Special Protection Areas (SPAs) with marine components under the Habitats Regulations. The UK Government is obligated under the OSPAR Convention and the transposed Marine Strategy Framework Directive to monitor these sites, assess their condition, and report on progress towards Good Environmental Status (GES).

Current MPA monitoring is fragmented across multiple agencies (JNCC, Natural England, Cefas, NRW, NatureScot), relies on periodic in-situ surveys with multi-year gaps between assessments, and stores data in disparate formats and systems. This prevents timely condition assessment, impedes enforcement, and makes OSPAR/MSFD reporting a labour-intensive manual exercise. The MPA Monitoring platform will create a unified surveillance capability integrating remote sensing, in-situ survey data, vessel tracking, and citizen science records.

### Objectives

- Establish a single authoritative platform for MPA condition assessment data across all UK marine conservation zones
- Integrate satellite remote sensing, acoustic survey, dive survey, and citizen science data sources into unified site assessments
- Enable near-real-time vessel activity monitoring within MPAs to support MMO enforcement
- Automate OSPAR and MSFD reporting with traceable evidence chains
- Publish MPA condition data as open data to support transparency, research, and public engagement

### Expected Outcomes

- 90% of UK MPAs with current condition assessment (baseline: 35%) within 24 months
- OSPAR reporting preparation time reduced from 6 months to 2 weeks
- Mean MPA infringement detection time reduced from >2 hours to <15 minutes
- 50+ marine datasets published as open data within 18 months
- 200+ registered API consumers within 12 months of launch

### Project Scope

**In Scope**:

- MPA condition assessment data management (ingest, store, process, visualise)
- Satellite and remote sensing data integration (Sentinel, Landsat, drone imagery)
- VMS/AIS vessel tracking integration for MPA boundary monitoring
- Acoustic survey data processing and habitat mapping
- Citizen science data submission and quality validation
- OSPAR/MSFD automated reporting
- Public-facing MPA condition dashboard
- Mobile access for field officers (Natural England, MMO)

**Out of Scope**:

- Marine spatial planning tool (separate DEFRA initiative)
- Fisheries quota management system (Project 002)
- Marine pollution monitoring (Project 003)
- Coastal erosion monitoring (Project 004)
- Survey vessel scheduling and logistics
- Direct regulatory enforcement case management (MMO existing system)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| DEFRA SRO | Executive Sponsor | DEFRA | Decision maker |
| Service Owner | Service accountability | DEFRA | Requirements validation |
| JNCC Marine Team | Scientific authority | JNCC | Data standards, methodology |
| Natural England Marine | Site management | Natural England | Operational requirements |
| Cefas Scientists | Marine science | Cefas | Scientific methods, calibration |
| MMO Compliance | Enforcement | MMO | Enforcement data requirements |
| DEFRA Enterprise Architect | Architecture oversight | DEFRA Digital | Technical oversight |
| DEFRA SIRO | Information risk | DEFRA | Security review |
| NFFO Representative | Industry voice | NFFO | Industry data access requirements |
| MCS Representative | NGO voice | MCS | Public data access, citizen science |

---

## Business Requirements

### BR-1: Unified MPA Condition Assessment

**Description**: The platform must provide a single, authoritative view of condition status for all 178 UK Marine Protected Areas, integrating data from multiple sources and agencies.

**Rationale**: Current fragmentation across JNCC, Natural England, Cefas, NRW, and NatureScot databases means there is no single view of MPA network health. OSPAR and MSFD reporting requires manual collation of data from multiple sources, taking up to 6 months per reporting cycle.

**Success Criteria**:

- 100% of UK MPAs represented in the platform with at least baseline data
- Condition status (favourable/unfavourable declining/unfavourable recovering/unknown) available for each site
- Single data query can retrieve condition status across the full MPA network

**Priority**: MUST_HAVE

**Stakeholder**: JNCC Marine Team Director, DEFRA Minister

---

### BR-2: Evidence-Based MPA Management

**Description**: The platform must provide Natural England and equivalent devolved bodies with timely, site-specific evidence to inform MPA management advice, consent decisions, and survey prioritisation.

**Rationale**: Natural England manages 91 MCZs but lacks a systematic evidence platform. Management advice is often based on outdated survey data. Consent applications (e.g., offshore wind, cable routes) require current site condition information that is not readily available.

**Success Criteria**:

- Site-specific evidence summary available for each MCZ within 2 clicks
- Change detection alerts generated when new evidence suggests condition change
- Survey prioritisation tool ranking sites by evidence gap and conservation importance

**Priority**: MUST_HAVE

**Stakeholder**: Natural England Marine Director

---

### BR-3: MPA Enforcement Support

**Description**: The platform must provide MMO enforcement officers with real-time vessel activity data overlaid on MPA boundaries, with automated alerts for potential infringements.

**Rationale**: Current enforcement relies on delayed VMS data review and infrequent at-sea patrols. Under-12m vessels are not VMS-equipped, creating monitoring gaps in inshore MCZs.

**Success Criteria**:

- Real-time vessel tracking on MPA boundary map for VMS/AIS-equipped vessels
- Automated alert within 15 minutes when regulated vessel enters restricted MPA zone
- Digital evidence capture with chain-of-custody metadata

**Priority**: SHOULD_HAVE

**Stakeholder**: MMO Head of Compliance

---

### BR-4: OSPAR and MSFD Reporting Automation

**Description**: The platform must automate the preparation of UK marine conservation reports for OSPAR and MSFD obligations.

**Rationale**: Current OSPAR reporting requires 6 months of manual data collation, validation, and formatting. The UK Marine Strategy Part Two commits to regular monitoring programme reports.

**Success Criteria**:

- OSPAR reporting data extraction automated to <2 weeks preparation time
- Report templates populated automatically from platform data
- Data quality flags preserved through to reporting output

**Priority**: MUST_HAVE

**Stakeholder**: JNCC Marine Team Director, DEFRA Minister

---

### BR-5: Open Marine Data Publication

**Description**: The platform must publish MPA condition data as open data, enabling public scrutiny, academic research, and NGO accountability monitoring.

**Rationale**: Open data policy requires government data to be published openly unless there are specific reasons not to. Marine conservation data has significant public interest. The fishing industry demands transparency in the evidence base for management decisions.

**Success Criteria**:

- Non-sensitive datasets published via data.gov.uk with MEDIN-compliant metadata
- API access available for programmatic data retrieval
- Data published within 30 days of quality validation

**Priority**: SHOULD_HAVE

**Stakeholder**: MCS, NFFO, academic researchers

---

## Functional Requirements

### User Personas

#### Persona 1: Marine Scientist (JNCC/Cefas)

- **Role**: Conservation scientist conducting MPA condition assessments
- **Goals**: Integrate multiple data sources, apply standardised assessment methodology, produce peer-reviewable condition reports
- **Pain Points**: Fragmented data across systems, manual data collation, inability to reproduce previous assessments
- **Technical Proficiency**: High

#### Persona 2: Marine Officer (Natural England)

- **Role**: Field officer responsible for MCZ site management and consent advice
- **Goals**: Access current site condition data in the field, respond to consent applications, prioritise survey visits
- **Pain Points**: Outdated site information, no mobile access, reliance on paper-based field records
- **Technical Proficiency**: Medium

#### Persona 3: Enforcement Officer (MMO)

- **Role**: Marine enforcement officer monitoring vessel compliance with MPA regulations
- **Goals**: Detect infringements in real time, gather prosecution-grade evidence, coordinate at-sea response
- **Pain Points**: Delayed VMS data, manual boundary checking, evidence not meeting prosecution standards
- **Technical Proficiency**: Medium

#### Persona 4: Citizen Scientist (MCS/Seasearch)

- **Role**: Trained volunteer diver or beach surveyor contributing observation data
- **Goals**: Submit survey observations, see how their data contributes to site assessments, track local MPA health
- **Pain Points**: No feedback on submitted data, unclear submission standards, sense of data being ignored
- **Technical Proficiency**: Low to Medium

---

### Functional Requirements Detail

#### FR-1: Multi-Source Data Ingestion

**Description**: The system must ingest marine monitoring data from multiple sources: satellite imagery (Sentinel-2, Landsat), acoustic survey data (multibeam, sidescan sonar), dive survey records, drop-camera video analysis, grab sample results, and citizen science observations.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given satellite imagery from Copernicus, when data is received, then it is processed and available within 24 hours
- [ ] Given acoustic survey data in GeoTIFF or BAG format, when uploaded, then spatial extents are calculated and data is spatially indexed
- [ ] Given a citizen science record from Seasearch, when submitted via the web form, then it enters the quality validation queue
- [ ] Edge case: When data format is unrecognised, then the system rejects with clear error message and logs the failure

**Data Requirements**:

- **Inputs**: Satellite raster (GeoTIFF), acoustic raster (BAG/GeoTIFF), survey records (CSV/JSON), species observations (Darwin Core)
- **Outputs**: Standardised observation records with quality flags, spatial indices, metadata records
- **Validations**: Coordinate bounds within UK EEZ, date range validation, mandatory field completeness

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Copernicus data access agreement, UKHO bathymetric data licence

---

#### FR-2: MPA Condition Assessment Engine

**Description**: The system must apply standardised assessment methodologies to calculate condition status for each MPA, using the full range of available evidence.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given multiple evidence sources for a single MCZ, when assessment is triggered, then condition status is calculated using the JNCC-approved methodology
- [ ] Given a condition assessment, when completed, then the assessment includes confidence score and evidence summary
- [ ] Given a change in condition status, when detected, then alerts are generated to site managers and JNCC

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-1 (data ingestion), JNCC methodology documentation

---

#### FR-3: Interactive MPA Map Viewer

**Description**: The system must provide an interactive map viewer showing all UK MPAs with condition status, overlaid with vessel activity, survey coverage, and environmental data layers.

**Relates To**: BR-1, BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given the map viewer is loaded, when zoomed to UK waters, then all 178 MPAs are displayed with colour-coded condition status
- [ ] Given an MPA is selected, when clicked, then a summary panel shows condition status, last assessment date, key indicators, and trend
- [ ] Given VMS/AIS data is available, when the enforcement layer is enabled, then vessel positions are shown in near-real-time
- [ ] Edge case: When map contains >1000 features at current zoom level, then clustering is applied for performance

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-1, FR-2, UK EEZ boundary data, UKHO bathymetry

---

#### FR-4: VMS/AIS Vessel Tracking Integration

**Description**: The system must ingest VMS and AIS position data, overlay vessel tracks on MPA boundaries, and generate automated alerts when vessels enter restricted zones.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a VMS position report for a vessel within an MPA boundary, when processed, then an alert is generated within 15 minutes
- [ ] Given AIS data feed, when received, then vessel positions are updated on the map in near-real-time
- [ ] Given a vessel track crossing an MPA boundary, when the enforcement view is accessed, then entry/exit times and duration within zone are calculated
- [ ] Edge case: When VMS data is delayed beyond 2 hours, then the system displays data age warning

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

**Dependencies**: MMO VMS data feed, AIS data provider agreement, MPA boundary polygon dataset

---

#### FR-5: Citizen Science Data Submission

**Description**: The system must provide a web-based submission pathway for citizen science data (Seasearch dive records, MCS beach survey results), with automated quality validation and feedback to submitters.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a citizen scientist with credentials, when they submit a dive survey record, then it is validated against species taxonomy, coordinate bounds, and mandatory fields
- [ ] Given a submitted record passes validation, when processed, then the submitter receives confirmation and the record enters the evidence base with appropriate quality flags
- [ ] Given a submitted record fails validation, when reviewed, then the submitter receives specific feedback on what needs correction

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: Seasearch data schema, MCS litter survey taxonomy

---

#### FR-6: OSPAR Report Generation

**Description**: The system must generate OSPAR-compliant reporting outputs, including MPA network status, indicator values, and trend analysis, in the required submission format.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a reporting period is selected, when report generation is triggered, then OSPAR-formatted data is produced within 24 hours
- [ ] Given generated report data, when reviewed, then all data values are traceable to source observations via provenance metadata
- [ ] Given report generation is complete, when exported, then output matches OSPAR submission format specifications

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-2 (condition assessment), OSPAR reporting format specification

---

#### FR-7: Mobile Field Access

**Description**: The system must provide a mobile-optimised interface for Natural England marine officers and MMO enforcement officers operating in the field, with offline capability.

**Relates To**: BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given a field officer with a mobile device, when accessing the platform, then the mobile interface displays site information and map view
- [ ] Given an area with no connectivity, when the officer has pre-loaded site data, then offline access to cached MPA data is available
- [ ] Given the device regains connectivity, when sync is triggered, then offline-collected data uploads automatically

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-8: Survey Prioritisation Engine

**Description**: The system must recommend MCZ survey priorities based on evidence gaps, time since last assessment, conservation importance, and detected change indicators.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given the current evidence base, when prioritisation is run, then a ranked list of MCZs is produced with justification scores
- [ ] Given a new data submission for a site, when processed, then the prioritisation ranking is recalculated

**Priority**: COULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-1, FR-2

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**:

- Map viewer initial load: <3 seconds (95th percentile)
- MPA condition summary retrieval: <1 second (95th percentile)
- VMS/AIS position data refresh: <30 seconds latency from source
- Report generation: <30 minutes for full OSPAR national report

**Load Conditions**:

- Peak concurrent users: 200 (during OSPAR reporting period)
- Average concurrent users: 50
- VMS position reports: up to 50,000/hour during peak fishing activity

**Priority**: HIGH

---

#### NFR-P-2: Data Ingestion Throughput

**Requirement**: The system must process satellite imagery at a rate of at least 100 GB/day during survey campaign periods, with acoustic survey data at 50 GB/day.

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: System must achieve 99.5% uptime during business hours (08:00-20:00 UTC), 99.0% overall.

**Maintenance Windows**: Sundays 02:00-06:00 UTC

**Priority**: HIGH

---

#### NFR-A-2: Disaster Recovery

**RPO**: 1 hour for transactional data, 24 hours for imagery/raster data

**RTO**: 4 hours

**Backup Requirements**: Daily incremental, weekly full, 90-day retention, geo-redundant storage

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Authentication and Authorisation

**Requirement**: All users must authenticate via DEFRA Identity (OAuth 2.0). Role-based access control with marine-specific roles (Scientist, Enforcement Officer, Site Manager, Public User, Citizen Scientist).

**MFA**: Required for enforcement data access and administrative functions.

**Priority**: CRITICAL

---

#### NFR-SEC-2: VMS Data Classification

**Requirement**: Individual vessel VMS position data must be classified OFFICIAL-SENSITIVE. Aggregated vessel activity data (heatmaps, area statistics) may be classified OFFICIAL.

**Priority**: CRITICAL

---

#### NFR-SEC-3: Encryption

**Requirement**: TLS 1.3 for all data in transit. AES-256 for all data at rest. Enhanced encryption for enforcement evidence data.

**Priority**: CRITICAL

---

### Compliance Requirements

#### NFR-C-1: UK GDPR Compliance

**Requirement**: Full UK GDPR compliance for processing of personal data (vessel skipper details, citizen science submitter information).

**Requirements**: DPIA completed, lawful basis documented, retention schedules implemented, data subject rights mechanisms functional.

**Priority**: CRITICAL

---

#### NFR-C-2: GDS Service Standard

**Requirement**: Service must pass GDS service assessment at Alpha and Beta stages.

**Priority**: HIGH

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance, including accessible alternatives to map-based visualisations for screen reader users.

**Priority**: CRITICAL

---

#### NFR-U-2: Offline Capability

**Requirement**: Core site information and map data must be available offline on mobile devices for field officers operating in areas with limited connectivity.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Copernicus Satellite Data Service

**Purpose**: Ingest Sentinel-2 optical imagery and Sentinel-1 SAR data for MPA habitat monitoring.

**Integration Type**: Batch file transfer (daily download via Copernicus Open Access Hub API)

**Data Exchanged**: Sentinel-2 Level-2A surface reflectance products, Sentinel-1 GRD products

**Authentication**: Copernicus Data Space API key

**Priority**: MUST_HAVE

---

### INT-2: MMO VMS Data Feed

**Purpose**: Receive vessel monitoring system position reports for MPA enforcement monitoring.

**Integration Type**: Near-real-time API feed (polling every 5 minutes)

**Data Exchanged**: Vessel ID, position (lat/lon), speed, course, timestamp

**Authentication**: Mutual TLS with MMO systems

**Priority**: SHOULD_HAVE

---

### INT-3: AIS Data Provider

**Purpose**: Receive Automatic Identification System vessel tracking data for comprehensive maritime awareness.

**Integration Type**: Real-time streaming (TCP/IP AIS data feed)

**Data Exchanged**: MMSI, vessel name, position, speed, course, vessel type

**Authentication**: API key with IP whitelisting

**Priority**: SHOULD_HAVE

---

### INT-4: UKHO Bathymetric Data

**Purpose**: Integrate UK Hydrographic Office bathymetric survey data and nautical chart data for depth context and seabed habitat mapping.

**Integration Type**: Batch file transfer (monthly updates)

**Data Exchanged**: Bathymetric grid data (BAG format), contour data

**Authentication**: UKHO data licence and API credentials

**Priority**: MUST_HAVE

---

### INT-5: MEDIN Metadata Catalogue

**Purpose**: Publish dataset discovery metadata to the Marine Environmental Data and Information Network catalogue.

**Integration Type**: Automated metadata publication via CSW (Catalogue Service for the Web)

**Data Exchanged**: ISO 19115/19139 metadata records

**Priority**: SHOULD_HAVE

---

### INT-6: Natural England MAGIC Map

**Purpose**: Integrate with the MAGIC (Multi-Agency Geographic Information for the Countryside) map service for MPA boundary reference data and designated site information.

**Integration Type**: WMS/WFS web service consumption

**Data Exchanged**: MPA boundary polygons, designation information, feature of interest data

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Marine Protected Area

**Description**: Represents a designated marine conservation zone, SAC, SPA, or other protected area.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| mpa_id | UUID | Yes | Unique identifier | Primary key |
| designation_type | Enum | Yes | MCZ, SAC, SPA, HPMA | Controlled vocabulary |
| name | String(255) | Yes | Official site name | Not null |
| boundary_polygon | Geometry(MultiPolygon) | Yes | Site boundary in WGS84 | Valid geometry |
| area_km2 | Decimal | Yes | Area in square kilometres | >0 |
| designation_date | Date | Yes | Date of formal designation | |
| features_of_interest | JSONB | Yes | Protected features list | |
| condition_status | Enum | No | Current condition assessment | favourable/unfavourable_declining/unfavourable_recovering/unknown |
| last_assessment_date | Date | No | Date of most recent assessment | |
| managing_body | String(100) | Yes | Responsible organisation | |

**Data Volume**: ~178 records (relatively static), growing slowly as new designations occur

**Data Classification**: PUBLIC

---

#### Entity 2: Observation Record

**Description**: An individual environmental observation or measurement within or related to an MPA.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| observation_id | UUID | Yes | Unique identifier | Primary key |
| mpa_id | UUID | Yes | Associated MPA | Foreign key |
| observation_type | Enum | Yes | Survey type | dive/acoustic/satellite/grab/citizen_science |
| location | Geometry(Point) | Yes | Observation location in WGS84 | Within UK EEZ |
| depth_m | Decimal | No | Depth in metres below Chart Datum | |
| observation_date | Timestamp | Yes | Date and time of observation | |
| species_observed | JSONB | No | Species records (Darwin Core format) | |
| habitat_type | String(50) | No | EUNIS habitat classification | |
| quality_flag | Enum | Yes | Data quality indicator | good/suspect/bad/missing |
| source_system | String(100) | Yes | Originating system | |
| provenance | JSONB | Yes | Full provenance metadata | |

**Data Volume**: Year 1: 500,000 records, Year 3: 5,000,000 records

**Data Classification**: OFFICIAL (OFFICIAL-SENSITIVE if linked to enforcement)

---

#### Entity 3: Vessel Position

**Description**: A VMS or AIS position report for a fishing or other vessel.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| position_id | UUID | Yes | Unique identifier | Primary key |
| vessel_id | String(50) | Yes | Vessel identifier (anonymised for non-enforcement use) | |
| position | Geometry(Point) | Yes | Vessel position in WGS84 | |
| speed_knots | Decimal | No | Speed over ground | >=0 |
| course_degrees | Integer | No | Course over ground | 0-359 |
| timestamp | Timestamp | Yes | Position report time | |
| source | Enum | Yes | Data source | vms/ais |
| within_mpa | Boolean | Yes | Whether position is within any MPA boundary | Calculated field |
| mpa_id | UUID | No | MPA if within boundary | Foreign key |

**Data Volume**: ~50,000 positions/day (VMS), up to 1,000,000/day (AIS)

**Data Classification**: OFFICIAL-SENSITIVE (individual positions), OFFICIAL (aggregated)

---

### Data Quality Requirements

**Data Accuracy**: All geospatial data accurate to stated precision (VMS: 100m, AIS: 10m, survey: instrument-dependent). Quality flags mandatory on all observation records.

**Data Completeness**: Mandatory fields enforced at ingestion. Missing optional fields recorded as explicit nulls, not omitted.

**Data Consistency**: Cross-system reconciliation between VMS data held by MMO and ingested by MPA platform. Species taxonomy validated against WoRMS (World Register of Marine Species).

**Data Timeliness**: Satellite data: <24 hours from acquisition. VMS: <30 minutes from position report. Survey data: <30 days from survey completion.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy on DEFRA's approved cloud platform (currently AWS with Crown Hosting for OFFICIAL-SENSITIVE workloads)

**TC-2**: Must integrate with DEFRA Identity for authentication (no separate identity provider)

**TC-3**: VMS data feed format and frequency are controlled by MMO — platform must adapt to existing feed, not demand changes

### Business Constraints

**BC-1**: Budget cap of GBP 8M capital over 2 years (from DEFRA Spending Review allocation)

**BC-2**: Must demonstrate measurable progress within 12 months to maintain political sponsorship

**BC-3**: Scientific methodology must be approved by JNCC Scientific Advisory Committee before implementation

### Assumptions

**A-1**: Copernicus data service will continue to provide free access to Sentinel imagery post-Brexit

**A-2**: MMO will provide VMS data feed access under existing DEFRA data sharing agreement

**A-3**: UKHO will licence bathymetric data for government use at no cost under OGL or partnership agreement

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| MPA sites with current condition assessment | 35% | 90% | 24 months | Platform dashboard |
| OSPAR report preparation time | 6 months | 2 weeks | 12 months | Process measurement |
| MPA infringement detection time | >2 hours | <15 minutes | 9 months | Alert log analysis |
| Open datasets published | 5 | 50+ | 18 months | data.gov.uk count |
| Registered API consumers | 0 | 200+ | 12 months | API gateway metrics |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.5% (business hours) | Uptime monitoring |
| Map viewer load time (p95) | <3 seconds | APM tooling |
| VMS data latency | <30 minutes | Data pipeline monitoring |
| Data ingestion throughput | 100 GB/day (satellite) | Pipeline metrics |
| API response time (p95) | <500ms | APM tooling |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| DEFRA Cloud Platform | AWS environment provisioned with OFFICIAL-SENSITIVE accreditation | DEFRA Digital | Q2 2026 | On Track | HIGH |
| MMO VMS Data Feed | API access to vessel monitoring system data | MMO | Q2 2026 | At Risk | MEDIUM |
| JNCC Methodology | Approved condition assessment methodology for automated application | JNCC | Q3 2026 | On Track | HIGH |
| UKHO Data Licence | Bathymetric data access agreement | UKHO | Q2 2026 | On Track | MEDIUM |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Scientific community rejects automated assessment methodology | MEDIUM | HIGH | Early JNCC engagement, phased validation, peer review | JNCC Marine Dir |
| R-2 | VMS data access delayed by MMO data sharing negotiations | MEDIUM | MEDIUM | Proceed with AIS data initially, escalate via DEFRA board | Product Owner |
| R-3 | Satellite data processing compute costs exceed budget | LOW | MEDIUM | Use serverless architecture, implement data tiering | Technical Lead |
| R-4 | Fishing industry legal challenge to data publication | LOW | HIGH | NFFO early engagement, legal review of data classification | SRO |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| DEFRA SRO | Executive Sponsor | [ ] Approved | | |
| JNCC Marine Team Director | Scientific Authority | [ ] Approved | | |
| Natural England Marine Director | Site Management | [ ] Approved | | |
| MMO Head of Compliance | Enforcement | [ ] Approved | | |
| DEFRA Enterprise Architect | Architecture | [ ] Approved | | |
| DEFRA SIRO | Security | [ ] Approved | | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| MCZ | Marine Conservation Zone — designated under the Marine and Coastal Access Act 2009 |
| SAC | Special Area of Conservation — designated under the Habitats Regulations |
| SPA | Special Protection Area — designated under the Birds Directive |
| HPMA | Highly Protected Marine Area — highest level of marine protection |
| VMS | Vessel Monitoring System — satellite tracking for fishing vessels >12m |
| AIS | Automatic Identification System — maritime transponder system |
| GES | Good Environmental Status — objective of the Marine Strategy Framework Directive |
| OSPAR | Convention for the Protection of the Marine Environment of the North-East Atlantic |
| MEDIN | Marine Environmental Data and Information Network |
| EUNIS | European Nature Information System — habitat classification |
| WoRMS | World Register of Marine Species — authoritative species taxonomy |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 14 Architecture Principles
- ARC-001-STKE-v1.0 — Stakeholder Drivers & Goals Analysis
- Marine and Coastal Access Act 2009
- UK Marine Strategy Part Two — Monitoring Programmes
- OSPAR Intermediate Assessment 2024

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Marine Protected Areas Monitoring
**Model**: Claude Opus 4.6
