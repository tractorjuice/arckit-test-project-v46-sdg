# Project Requirements: Ocean Pollution Tracking

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Ocean Pollution Tracking (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Owner, Ocean Pollution Tracking |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Pollution Programme Board, DEFRA, EA, Cefas, MCA, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies the requirements for a platform monitoring marine litter, chemical contamination, sewage discharges, oil spills, and microplastic pollution across UK waters, supporting OSPAR MSFD Descriptor 8 and 10 reporting and public bathing water information.

---

## Executive Summary

### Business Context

Marine pollution in UK waters is a high-profile environmental and public health concern. Storm overflow discharges, marine litter, chemical contaminants, oil spills, and emerging threats such as microplastics affect bathing water quality, marine ecosystems, and coastal communities. Monitoring data is currently fragmented across the Environment Agency's Water Information Management System (WIMS), the EDM data portal, Cefas CSEMP database, MCA oil spill records, and NGO beach survey data. This fragmentation prevents holistic pollution assessment, delays incident response, and complicates OSPAR MSFD reporting for Descriptors 8 (contaminants) and 10 (marine litter).

The Environment Act 2021 introduced new duties for water company storm overflow monitoring and reporting, generating vast volumes of Event Duration Monitoring data. Public demand for real-time water quality information — driven by campaigns from Surfers Against Sewage, Marine Conservation Society, and media coverage — has made marine pollution a tier-one political issue.

### Objectives

- Integrate all marine pollution monitoring data streams into a unified evidence platform
- Deliver real-time public dashboards for bathing water quality and sewage discharge status
- Enable EA enforcement officers to build prosecution-grade evidence cases digitally
- Automate OSPAR MSFD Descriptor 8 and 10 reporting
- Support oil spill detection via satellite SAR data and AIS vessel correlation

### Expected Outcomes

- All 420+ designated bathing waters with real-time pollution risk indicators
- Pollution incident response data assembly time reduced from 4 hours to <30 minutes
- OSPAR reporting preparation reduced from 4 months to 3 weeks
- 100,000+ monthly public dashboard users within 12 months of launch
- 80% of enforcement cases supported by digital evidence

### Project Scope

**In Scope**:

- Storm overflow (EDM) data ingestion and real-time display
- Bathing water quality sample data management and classification
- Marine litter beach survey data management (MCS, EA, OSPAR)
- Chemical contaminant monitoring data integration (Cefas CSEMP)
- Oil spill satellite detection integration (Sentinel-1 SAR)
- Microplastics monitoring data (emerging — framework for future integration)
- Public-facing pollution dashboard with bathing water focus
- EA enforcement evidence management
- OSPAR MSFD Descriptor 8 and 10 automated reporting
- Citizen pollution incident reporting

**Out of Scope**:

- Inland river pollution monitoring (EA existing WIMS scope)
- Water company infrastructure investment planning (Ofwat/water company scope)
- Marine Protected Areas monitoring (Project 001)
- Fishing activity monitoring (Project 002)
- Air quality monitoring
- Radioactive substance discharge monitoring (EA separate regulatory regime)

---

## Business Requirements

### BR-1: Real-Time Sewage Discharge Monitoring

**Description**: The platform must ingest water company Event Duration Monitoring (EDM) data in near-real-time and display storm overflow discharge status at all monitored outfalls, with linkage to affected bathing waters.

**Rationale**: The Environment Act 2021 requires near-real-time publication of storm overflow data. Public and parliamentary demand for transparency is intense. Current EDM data publication is delayed by 24-48 hours.

**Success Criteria**:

- EDM spill event data displayed within 2 hours of occurrence
- All monitored storm overflows (15,000+) with current status on the map
- Bathing waters within 2km of spilling outfall flagged with pollution warning

**Priority**: MUST_HAVE

---

### BR-2: Bathing Water Quality Dashboard

**Description**: The platform must provide a public-facing dashboard showing current and historical bathing water quality for all 420+ designated sites, combining EA sampling data with EDM discharge alerts and predictive water quality modelling.

**Rationale**: The Bathing Water Regulations 2013 require annual classification of bathing waters. The public needs actionable, timely information — not just annual classifications. SAS and others provide partial services; a government platform must be the authoritative source.

**Success Criteria**:

- All 420+ bathing waters with real-time pollution risk indicator
- Daily updated risk assessment during bathing season (May-September)
- Historical classification trends visible for each site
- API access for third-party app developers (SAS, local councils)

**Priority**: MUST_HAVE

---

### BR-3: Marine Litter Evidence Management

**Description**: The platform must manage marine litter survey data from multiple sources (MCS beach surveys, EA monitoring, OSPAR beach litter surveys) with standardised categorisation enabling trend analysis and OSPAR Descriptor 10 reporting.

**Rationale**: Marine litter (particularly plastics) is a priority pollution concern under OSPAR and the UK Marine Strategy. Data currently resides in separate databases with inconsistent categorisation.

**Success Criteria**:

- All UK beach litter survey data integrated with OSPAR-standard categorisation
- Trend analysis showing litter density per 100m of beach over time
- OSPAR Descriptor 10 reporting data extracted automatically

**Priority**: SHOULD_HAVE

---

### BR-4: Pollution Enforcement Evidence

**Description**: The platform must enable EA enforcement officers to assemble digital evidence for pollution prosecution cases, with chain-of-custody metadata, photographic evidence capture, and sample result linkage.

**Rationale**: EA brings approximately 50 prosecution cases per year for marine pollution. Digital evidence assembly currently takes 3+ days of manual collation from multiple systems.

**Success Criteria**:

- Evidence package assembled digitally within 4 hours
- Photographic evidence with GPS, timestamp, and officer ID metadata
- Chain of custody audit trail from sample collection through lab analysis to prosecution file

**Priority**: SHOULD_HAVE

---

### BR-5: OSPAR MSFD Reporting Automation

**Description**: The platform must automate data extraction and report preparation for OSPAR MSFD Descriptor 8 (contaminants) and Descriptor 10 (marine litter) assessments.

**Rationale**: Current OSPAR reporting requires 4 months of manual data collation across EA and Cefas datasets. The UK reports every 6 years with interim assessments.

**Success Criteria**:

- OSPAR Descriptor 8 and 10 data extraction automated to <3 weeks preparation
- All data traceable to source with quality flags
- Report templates populated from platform data

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: EA Water Quality Officer

- **Role**: Monitors bathing water quality, responds to pollution incidents, takes enforcement action
- **Goals**: View real-time pollution status, correlate EDM data with sample results, build enforcement evidence
- **Pain Points**: Multiple systems, manual data collation, field access limitations
- **Technical Proficiency**: Medium

#### Persona 2: Public Beach User

- **Role**: Member of the public checking water quality before visiting a beach
- **Goals**: Know whether it is safe to swim today, understand pollution history of local beaches
- **Pain Points**: Information scattered across websites, data not timely, technical language
- **Technical Proficiency**: Low

#### Persona 3: Cefas Contamination Scientist

- **Role**: Analyses contaminant trends in UK waters for OSPAR/MSFD reporting
- **Goals**: Access integrated pollution data for trend analysis, prepare OSPAR assessment reports
- **Pain Points**: Data in separate systems, manual collation, format inconsistencies
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: EDM Data Ingestion and Real-Time Display

**Description**: Ingest Event Duration Monitoring data from all water companies in near-real-time and display spill status (spilling/not spilling) on an interactive map.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a water company reports a spill start event, when data is received, then the outfall status changes to "spilling" within 2 hours on the public map
- [ ] Given a spill ends, when the stop event is received, then the outfall reverts to "not spilling" with spill duration recorded
- [ ] Given 15,000+ monitored outfalls, when the map loads, then clustering is applied at wide zoom with individual outfall display at local zoom
- [ ] Edge case: When an EDM monitor malfunctions and reports continuous spilling, then data quality flag highlights potential equipment fault

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Bathing Water Quality Assessment

**Description**: Calculate and display a daily pollution risk indicator for each designated bathing water, combining EA sample results, EDM discharge data, rainfall, and tidal conditions.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a bathing water location, when the risk assessment runs daily, then a risk level (low/medium/high) is calculated and displayed
- [ ] Given a nearby storm overflow is spilling, when detected, then the bathing water risk is elevated with advisory notice
- [ ] Given EA sample results are received, when processed, then the annual classification calculation is updated

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Marine Litter Survey Data Management

**Description**: Ingest and standardise beach litter survey data from MCS Great British Beach Clean, EA monitoring, and OSPAR reference beach surveys.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given MCS uploads annual beach clean survey data, when ingested, then litter items are mapped to OSPAR standard categories
- [ ] Given litter density is calculated, when displayed, then items per 100m of surveyed beach are shown with year-on-year trend
- [ ] Given OSPAR Descriptor 10 reporting is triggered, when data is extracted, then output matches OSPAR submission format

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-4: Satellite Oil Spill Detection Integration

**Description**: Ingest Sentinel-1 SAR satellite imagery processing results to detect potential oil slicks and correlate with AIS vessel tracks for source identification.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given Sentinel-1 SAR imagery detects a potential slick, when processed, then the slick polygon is displayed on the pollution map
- [ ] Given a slick detection, when AIS data is overlaid, then vessels transiting the area in the preceding 24 hours are listed
- [ ] Edge case: When natural surface films cause SAR false positives, then confidence scoring distinguishes likely oil from biological films

**Priority**: COULD_HAVE

**Complexity**: HIGH

---

#### FR-5: Citizen Pollution Reporting

**Description**: Enable members of the public to report pollution incidents (beach litter, suspicious discharges, oil sheens) via a mobile-optimised web form with photo upload and GPS location.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a citizen observes pollution, when they submit a report via mobile, then location, photo, and description are captured
- [ ] Given a report is submitted, when triaged by EA, then a response status is visible to the reporter
- [ ] Given multiple reports in the same area, when clustered, then EA receives an aggregated incident alert

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-6: Enforcement Evidence Package Builder

**Description**: Enable EA officers to assemble prosecution evidence packages digitally, linking incident reports, sample results, photographic evidence, EDM data, and witness statements.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given an enforcement investigation, when an officer creates a case, then relevant data sources (EDM, samples, photos) can be linked to the case
- [ ] Given evidence is added to a case, when recorded, then chain-of-custody metadata (who, when, what) is immutably logged
- [ ] Given a case is complete, when exported, then a prosecution-ready evidence bundle is generated in PDF format

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-7: Public Bathing Water Dashboard

**Description**: Provide a GOV.UK-styled public dashboard where citizens can search for a beach and view current pollution risk, annual classification, nearby discharge status, and historical trends.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a user searches for "Brighton Beach", when results are displayed, then current risk level, annual classification, and nearest outfall status are shown
- [ ] Given a bathing water is displayed, when the user views history, then a 5-year classification trend chart is shown
- [ ] Given the dashboard is accessed on a mobile device, when rendered, then the layout is responsive and usable on 5-inch screens

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements

### Performance

#### NFR-P-1: Response Time

- Public dashboard page load: <2 seconds (95th percentile)
- EDM data ingestion to display: <2 hours
- Map viewer with 15,000+ outfalls: <4 seconds initial load

**Priority**: HIGH

### Availability

#### NFR-A-1: Availability Target

- 99.5% availability (public dashboard is not safety-critical but has high political visibility)
- Peak availability during bathing season (May-September): 99.9%

**Priority**: HIGH

### Security

#### NFR-SEC-1: Public vs Restricted Data

- Public data: Bathing water quality, EDM spill events, beach litter surveys, annual classifications
- Restricted data: Enforcement evidence, unpublished sample results, detailed outfall engineering data
- OFFICIAL-SENSITIVE: Active enforcement case data

**Priority**: CRITICAL

### Usability

#### NFR-U-1: Public Accessibility

- WCAG 2.2 Level AA compliance for all public-facing pages
- Plain English — no technical jargon on public dashboard
- Welsh language support for Welsh bathing waters

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Water Company EDM Data Feeds

**Purpose**: Ingest near-real-time storm overflow Event Duration Monitoring data from all water companies in England.

**Integration Type**: API (REST, near-real-time polling every 15 minutes)

**Data Exchanged**: Outfall ID, spill start/stop timestamps, spill duration, permit reference

**Authentication**: API key per water company

**Priority**: MUST_HAVE

---

### INT-2: EA WIMS (Water Information Management System)

**Purpose**: Ingest bathing water sample results and water quality monitoring data.

**Integration Type**: API (batch daily)

**Data Exchanged**: Sample location, date, E. coli count, intestinal enterococci count, parameters

**Priority**: MUST_HAVE

---

### INT-3: Cefas CSEMP Database

**Purpose**: Integrate chemical contaminant monitoring data for OSPAR Descriptor 8 reporting.

**Integration Type**: API (batch quarterly)

**Data Exchanged**: Sampling station, date, contaminant concentrations, matrix (sediment/water/biota), quality flags

**Priority**: SHOULD_HAVE

---

### INT-4: MCS Beach Survey Data

**Purpose**: Ingest annual Great British Beach Clean survey data and regular beach litter monitoring results.

**Integration Type**: Batch file upload (annual primary dataset, quarterly updates)

**Data Exchanged**: Beach ID, survey date, litter items by OSPAR category, volunteer count

**Priority**: SHOULD_HAVE

---

### INT-5: Copernicus Sentinel-1 SAR

**Purpose**: Ingest processed SAR imagery for oil slick detection.

**Integration Type**: Batch (daily download via Copernicus API)

**Data Exchanged**: Detected slick polygons, confidence score, acquisition timestamp

**Priority**: COULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Pollution Incident

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| incident_id | UUID | Yes | Unique identifier | Primary key |
| incident_type | Enum | Yes | Type of pollution | sewage/oil/litter/chemical/unknown |
| location | Geometry(Point) | Yes | Incident location | Within UK waters/coast |
| reported_date | Timestamp | Yes | When reported | |
| source | String(100) | No | Identified source | |
| severity | Enum | Yes | Impact severity | low/medium/high/critical |
| status | Enum | Yes | Investigation status | reported/investigating/resolved/enforcing |
| affected_bathing_waters | Array(UUID) | No | Impacted bathing waters | Foreign keys |

**Data Volume**: ~5,000 incidents/year

#### Entity 2: EDM Spill Event

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| event_id | UUID | Yes | Unique identifier | Primary key |
| outfall_id | String(20) | Yes | Permitted outfall reference | |
| water_company | String(50) | Yes | Operating water company | |
| spill_start | Timestamp | Yes | Spill start time | |
| spill_end | Timestamp | No | Spill end time (null if ongoing) | After spill_start |
| duration_hours | Decimal | No | Calculated duration | >=0 |
| location | Geometry(Point) | Yes | Outfall location | |
| permit_reference | String(30) | Yes | EA permit number | |

**Data Volume**: ~300,000 spill events/year across all water companies

**Data Classification**: OFFICIAL (public data under Environment Act)

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with EA's existing WIMS database — not a replacement

**TC-2**: Water company EDM data formats are not fully standardised — platform must handle company-specific variations

**TC-3**: Must deploy on DEFRA/EA shared cloud infrastructure

### Business Constraints

**BC-1**: Budget cap of GBP 6M capital over 2 years

**BC-2**: Public dashboard must be live before May 2027 bathing season

**BC-3**: Water company data sharing is regulated by Ofwat — cannot impose new data formats without regulatory process

### Assumptions

**A-1**: All water companies will provide API access to EDM data (regulatory requirement under Environment Act)

**A-2**: EA WIMS API is available and performant for batch data extraction

**A-3**: Sentinel-1 SAR oil slick detection processing service is available from Copernicus or commercial provider

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Bathing waters with real-time risk indicator | 0 | 420+ | 12 months | Platform count |
| EDM data latency | 48 hours | <2 hours | 9 months | Pipeline metrics |
| Public dashboard monthly users | 0 | 100,000+ | 12 months post-launch | Analytics |
| OSPAR reporting prep time | 4 months | 3 weeks | 18 months | Process measurement |
| Enforcement cases with digital evidence | 25% | 80% | 18 months | EA records |
| Pollution data sources integrated | 3 | 8+ | 18 months | Platform count |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| EDM | Event Duration Monitoring — electronic monitoring of storm overflow discharge events |
| MSFD | Marine Strategy Framework Directive — EU directive transposed into UK law |
| CSEMP | Clean Seas Environment Monitoring Programme — Cefas contaminant monitoring |
| WIMS | Water Information Management System — EA water quality database |
| SAR | Synthetic Aperture Radar — satellite imaging for oil spill detection |
| OSPAR | Convention for the Protection of the Marine Environment of the North-East Atlantic |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Ocean Pollution Tracking
**Model**: Claude Opus 4.6
