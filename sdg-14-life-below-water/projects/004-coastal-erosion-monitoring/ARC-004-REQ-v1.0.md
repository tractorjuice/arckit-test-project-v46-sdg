# Project Requirements: Coastal Erosion Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Coastal Erosion Monitoring (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Owner, Coastal Erosion Monitoring |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Coastal Programme Board, EA, DEFRA, Local Authorities, BGS, UKHO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies requirements for a coastal change mapping and prediction platform integrating LiDAR survey data, satellite imagery, wave/tide data, and geological information to produce erosion predictions informing Shoreline Management Plans, planning decisions, and public information.

---

## Executive Summary

### Business Context

England has approximately 6,000 km of coastline, of which approximately 2,800 km is at risk of erosion. The National Coastal Monitoring Programme (NCMP) surveys the coast using airborne LiDAR, aerial photography, and ground surveys, generating approximately 2 TB of data annually across six regional programmes. This data feeds into Shoreline Management Plans (SMPs) that set policy for each stretch of coast (hold the line, managed realignment, advance the line, or no active intervention) and informs the EA's GBP 5.2 billion FCERM investment programme.

Current coastal monitoring data is fragmented across regional programme databases, processed manually, and presented in formats inaccessible to non-specialist users. Erosion predictions are available at coarse spatial resolution and are not routinely updated. Local authority planners, infrastructure operators (Network Rail, National Highways), and coastal communities cannot easily access current erosion data for their locations.

### Objectives

- Integrate all six NCMP regional programmes into a unified national coastal change platform with automated LiDAR processing
- Deliver erosion predictions at 50m intervals along the English coastline at 20, 50, and 100-year timescales
- Provide a public-facing coastal erosion information service in plain English
- Enable local authority planners to access erosion data for planning application decisions
- Support EA business case development for FCERM investment with accurate erosion projections

### Expected Outcomes

- All 6 regional programmes integrated with automated LiDAR change detection
- 85% of eroding coastline with predictions at 50m resolution within 24 months
- 80+ local authorities using the platform for planning decisions within 24 months
- FCERM business case preparation time reduced by 40%
- Public service covering all at-risk coastal postcodes

### Project Scope

**In Scope**:

- LiDAR point cloud processing, DEM generation, and change detection
- Aerial photography management and coastal feature mapping
- Beach profile and topographic survey data management
- Erosion rate calculation and prediction modelling
- Wave and tide data integration (from EA, Channel Coastal Observatory, UKHO)
- Geological/geomorphological data integration (BGS)
- Climate change scenario modelling (UKCP18 sea level rise)
- Public-facing coastal erosion information service
- Local authority planning portal integration
- FCERM business case data provision
- Infrastructure risk alerting (API for Network Rail, National Highways)

**Out of Scope**:

- Flood risk modelling (EA existing FCRM tools)
- Marine Protected Areas monitoring (Project 001)
- Coastal pollution monitoring (Project 003)
- SMP policy determination (policy, not technical platform)
- Coastal defence design (engineering, not monitoring)
- Welsh, Scottish, Northern Irish coastline (separate administrations)

---

## Business Requirements

### BR-1: Unified National Coastal Change Platform

**Description**: Integrate data from all six NCMP regional monitoring programmes into a single platform with consistent data standards, automated processing, and version-controlled datasets.

**Rationale**: Current fragmentation across six regional programmes with different delivery partners, data formats, and processing pipelines prevents efficient national-scale analysis and creates data gaps at regional boundaries.

**Success Criteria**:

- All 6 regional programmes contributing data to a single platform
- LiDAR processing pipeline automated (point cloud to DEM to change analysis)
- Consistent coordinate reference system (OSGB36 with OSGM15 geoid model)
- Dataset version control with full provenance metadata

**Priority**: MUST_HAVE

---

### BR-2: Erosion Prediction at Planning Resolution

**Description**: Generate erosion predictions at 50m intervals along the eroding coastline at 20, 50, and 100-year timescales, incorporating climate change scenarios.

**Rationale**: Current predictions are at coarse resolution (500m-1km sections) and mostly derived from the SMP2 process (2010-2011). Local authority planners need finer resolution for individual planning application decisions. UKCP18 climate projections must be incorporated.

**Success Criteria**:

- 85% of eroding coastline with predictions at 50m intervals
- Predictions at 20, 50, and 100-year timescales
- Climate change scenarios (low, medium, high emissions) reflected
- Prediction uncertainty quantified and displayed

**Priority**: MUST_HAVE

---

### BR-3: Public Coastal Erosion Information

**Description**: Provide a public-facing service where coastal residents can access erosion risk information for their location in plain English, including SMP policy, predicted timeline, and available support.

**Rationale**: Current erosion information is buried in technical SMP documents. Coastal communities have a right to know the erosion risk to their properties. Transparent communication supports community resilience.

**Success Criteria**:

- All at-risk coastal postcodes covered
- Risk presented in plain English with uncertainty explanation
- SMP policy (hold the line/managed realignment/no intervention) clearly displayed
- Links to adaptation support and compensation schemes

**Priority**: SHOULD_HAVE

---

### BR-4: Planning Application Support

**Description**: Enable local authority planners to query erosion risk for specific locations, receiving a report suitable for inclusion in planning application decisions.

**Rationale**: NPPF requires consideration of coastal change in planning. Approximately 100 coastal local authorities need accessible erosion data for planning decisions.

**Success Criteria**:

- Location-based erosion risk query returning 20, 50, 100-year predictions
- Downloadable evidence report for planning files
- Integration API for local authority planning portals

**Priority**: SHOULD_HAVE

---

### BR-5: FCERM Investment Evidence

**Description**: Provide erosion data and projections that support EA business cases for coastal protection investment, including property counts at risk, infrastructure value, and benefit-cost calculations.

**Rationale**: The EA's GBP 5.2 billion FCERM programme requires evidence-based business cases. Better erosion data enables more accurate benefit quantification and more compelling HM Treasury submissions.

**Success Criteria**:

- Erosion predictions linked to Ordnance Survey AddressBase property data
- Properties at risk counts at 20, 50, 100-year timescales per coastal section
- Infrastructure assets at risk (rail, road, utilities) identified and valued
- Data exportable in format suitable for Partnership Funding calculator

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Coastal Geomorphologist (EA/NCMP)

- **Role**: Analyses LiDAR data to calculate erosion rates and update predictions
- **Goals**: Process survey data efficiently, validate erosion models, publish updated predictions
- **Pain Points**: Manual LiDAR processing, inconsistent regional data formats, slow analysis workflows
- **Technical Proficiency**: High

#### Persona 2: Local Authority Planner

- **Role**: Determines planning applications in coastal zones
- **Goals**: Access current erosion risk data for specific sites, produce evidence for planning reports
- **Pain Points**: Cannot access current data, relies on outdated SMP information, no standard format
- **Technical Proficiency**: Medium

#### Persona 3: Coastal Resident

- **Role**: Homeowner or business owner in an erosion-affected area
- **Goals**: Understand erosion risk to their property, know what protection is planned, find support information
- **Pain Points**: Technical language, information difficult to find, conflicting local rumours
- **Technical Proficiency**: Low

#### Persona 4: FCERM Programme Manager (EA)

- **Role**: Develops business cases for coastal protection investment
- **Goals**: Quantify properties and infrastructure at risk, calculate benefits for Green Book appraisal
- **Pain Points**: Manual data collation, inconsistent erosion estimates, time-consuming BCR calculations
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-1: LiDAR Data Processing Pipeline

**Description**: Automated pipeline to ingest airborne LiDAR point cloud data, generate Digital Elevation Models (DEMs), and compute change analysis between survey epochs.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given LiDAR point cloud data (LAZ/LAS format) is uploaded, when processing is triggered, then a DEM is generated at 1m resolution within 48 hours
- [ ] Given DEMs from two survey epochs, when change detection is run, then volumetric change (erosion/accretion) is calculated and visualised
- [ ] Given the processing pipeline completes, when quality checks pass, then results are published with full provenance metadata
- [ ] Edge case: When LiDAR data quality is poor (gaps, noise), then automated quality flags are applied and manual review is prompted

**Data Requirements**:

- **Inputs**: LAS/LAZ point cloud files, flight line metadata, ground control point data
- **Outputs**: DEM (GeoTIFF), difference model, erosion/accretion volumes, change polygons
- **Validations**: Coordinate system check, point density minimum, vertical accuracy validation

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Erosion Rate Calculation

**Description**: Calculate historical erosion rates from multi-epoch survey data using cliff top/toe position mapping, beach profile analysis, and volumetric change assessment.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given cliff top position data from multiple surveys, when erosion rate is calculated, then annual erosion rate (m/year) is produced at 50m intervals
- [ ] Given beach profile data from multiple surveys, when analysis is run, then beach volume change is calculated per profile
- [ ] Given erosion rates, when displayed, then confidence intervals are shown reflecting data quality and number of survey epochs

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Erosion Prediction Model

**Description**: Generate erosion predictions at 20, 50, and 100-year timescales incorporating historical rates, UKCP18 sea level rise scenarios, and geological resistance factors.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given historical erosion rates and UKCP18 scenarios, when prediction model is run, then erosion extent is projected at 20, 50, and 100 years
- [ ] Given prediction results, when displayed, then uncertainty bounds (5th/50th/95th percentile) are shown
- [ ] Given a climate scenario is selected (low/medium/high emissions), when applied, then predictions adjust to reflect accelerated sea level rise
- [ ] Edge case: When a coastal defence is present, then the prediction model accounts for defended vs undefended scenarios

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-2, UKCP18 data, BGS geological mapping

---

#### FR-4: Interactive Coastal Map Viewer

**Description**: Interactive map showing the English coastline with erosion prediction overlays, survey coverage, SMP policies, and historical change data.

**Relates To**: BR-1, BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given the map loads, when England's coastline is displayed, then erosion prediction zones (20, 50, 100 year) are shown as coloured bands
- [ ] Given a section of coast is selected, when clicked, then erosion rate, prediction, SMP policy, and last survey date are displayed
- [ ] Given a time slider is adjusted, when moved from 2026 to 2126, then the predicted shoreline position animates
- [ ] Given LiDAR survey coverage is toggled, when displayed, then survey dates and extents are shown

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: Planning Portal Erosion Lookup

**Description**: API and web interface for local authority planners to query erosion risk for a specific location (postcode or grid reference) and receive a structured risk report.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a planner enters a postcode, when the query is submitted, then a report shows 20/50/100-year erosion risk with SMP policy and confidence level
- [ ] Given the report is generated, when downloaded, then a PDF suitable for planning file inclusion is produced
- [ ] Given the API is called programmatically, when valid coordinates are provided, then a JSON response with erosion data is returned within 2 seconds

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-6: Property and Infrastructure Risk Assessment

**Description**: Overlay erosion predictions with Ordnance Survey AddressBase property data and infrastructure datasets (rail, road, utilities) to calculate assets at risk.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given erosion predictions at 50m resolution, when overlaid with AddressBase, then properties within each prediction zone are counted
- [ ] Given infrastructure datasets (Network Rail, National Highways), when analysed, then infrastructure assets within erosion zones are identified and valued
- [ ] Given a coastal section is selected, when an FCERM report is generated, then properties at risk, infrastructure value, and projected timeline are presented

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-3, OS AddressBase licence, infrastructure datasets

---

#### FR-7: Public Coastal Erosion Service

**Description**: Public-facing web service where residents can search by postcode and view erosion risk, SMP policy, and support information in plain English.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a resident enters their postcode, when it is in an erosion risk area, then risk level (high/medium/low/negligible) is displayed with timeline
- [ ] Given the risk information is displayed, when the SMP policy section is shown, then policy is explained in plain English (not acronyms)
- [ ] Given the resident's area has "no active intervention" policy, when displayed, then links to adaptation support schemes and community resilience resources are provided
- [ ] Edge case: When a postcode is not in an erosion risk area, then a clear "no identified erosion risk" message is shown

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-8: Climate Scenario Modelling

**Description**: Apply UKCP18 climate change projections (sea level rise, storm frequency) to erosion predictions, showing the impact of different emissions scenarios.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a coastal section, when the user selects RCP 2.6/4.5/8.5, then erosion predictions adjust to reflect the selected sea level rise scenario
- [ ] Given climate scenario comparison is selected, when displayed, then all three scenarios are shown side-by-side with difference highlighted

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

**Dependencies**: FR-3, UKCP18 data products

---

## Non-Functional Requirements

### Performance

#### NFR-P-1: Response Time

- Map viewer initial load: <3 seconds (95th percentile)
- Erosion lookup by postcode: <2 seconds
- LiDAR DEM generation (per survey epoch): <48 hours automated processing
- Property risk report generation: <30 seconds

**Priority**: HIGH

#### NFR-P-2: Data Volume

- Must handle 2TB+ of LiDAR data ingested annually
- Must store 20+ years of historical survey data (growing at ~2TB/year)
- Must support concurrent access by 100+ users during SMP review periods

**Priority**: HIGH

### Availability

#### NFR-A-1: Availability

- 99.5% availability for the public service
- LiDAR processing pipeline: 95% availability (not user-facing, batch)
- Planned maintenance: Weekday evenings 22:00-06:00

**Priority**: HIGH

### Security

#### NFR-SEC-1: Data Classification

- Survey data (LiDAR, aerial photography): OFFICIAL
- Property-level erosion risk data: OFFICIAL (sensitive publication considerations)
- EA internal business case data: OFFICIAL
- Individual property owner correspondence: OFFICIAL

**Priority**: HIGH

### Usability

#### NFR-U-1: Accessibility

- WCAG 2.2 Level AA for all public-facing services
- Map visualisation with text alternative for accessibility
- Plain English (reading age 9) for public erosion risk information

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: NCMP Regional Monitoring Programmes

**Purpose**: Ingest LiDAR, aerial photography, and beach profile data from all six regional programmes.

**Integration Type**: Batch file upload (quarterly survey campaigns) plus API for automated transfer

**Data Exchanged**: LiDAR point clouds (LAS/LAZ), DEMs (GeoTIFF), beach profiles (CSV), aerial photography (JPEG/TIFF)

**Priority**: MUST_HAVE

---

### INT-2: UKCP18 Climate Projections

**Purpose**: Integrate Met Office UKCP18 sea level rise projections for climate-adjusted erosion predictions.

**Integration Type**: Batch (annual update when new projections released)

**Data Exchanged**: Sea level rise projections by RCP scenario, regional storm frequency projections

**Priority**: MUST_HAVE

---

### INT-3: BGS Geological Mapping

**Purpose**: Integrate geological resistance data for erosion prediction (cliff lithology, geological structure).

**Integration Type**: WMS/WFS web service

**Data Exchanged**: Geological bedrock and superficial deposit mapping, cliff material classification

**Priority**: SHOULD_HAVE

---

### INT-4: Ordnance Survey AddressBase

**Purpose**: Overlay erosion predictions with property locations for risk counting and FCERM business cases.

**Integration Type**: Batch (annual update)

**Data Exchanged**: Property locations (UPRN, coordinates), property classification

**Priority**: MUST_HAVE

---

### INT-5: EA Wave and Tide Monitoring Network

**Purpose**: Integrate real-time and historical wave height, period, and tidal data for erosion event correlation.

**Integration Type**: Near-real-time API (wave buoy data) plus batch (historical records)

**Data Exchanged**: Wave height (Hs), wave period (Tp), tidal level, storm surge

**Priority**: SHOULD_HAVE

---

### INT-6: Channel Coastal Observatory

**Purpose**: Access historical beach profile data and coastal monitoring archives.

**Integration Type**: API/batch

**Data Exchanged**: Beach profile measurements, sediment transport data, historical survey records

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Coastal Survey

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| survey_id | UUID | Yes | Unique identifier | Primary key |
| survey_type | Enum | Yes | Type of survey | lidar/aerial_photo/beach_profile/topographic |
| survey_date | Date | Yes | Date of survey | |
| region | Enum | Yes | NCMP region | 6 regions |
| spatial_extent | Geometry(Polygon) | Yes | Survey coverage area | Within English coastline |
| data_files | Array(String) | Yes | Associated data file paths | |
| quality_rating | Enum | Yes | Data quality assessment | excellent/good/acceptable/poor |
| processing_status | Enum | Yes | Processing pipeline status | raw/processing/validated/published |

**Data Volume**: ~200 surveys/year, total archive 1,500+

#### Entity 2: Erosion Prediction

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| prediction_id | UUID | Yes | Unique identifier | Primary key |
| coastal_section_id | String(10) | Yes | 50m section reference | |
| location | Geometry(LineString) | Yes | Section geometry | On English coast |
| historical_rate_m_per_year | Decimal | Yes | Calculated historical erosion rate | |
| prediction_20yr_m | Decimal | Yes | Predicted erosion at 20 years | |
| prediction_50yr_m | Decimal | Yes | Predicted erosion at 50 years | |
| prediction_100yr_m | Decimal | Yes | Predicted erosion at 100 years | |
| climate_scenario | Enum | Yes | RCP scenario | rcp26/rcp45/rcp85 |
| confidence | Enum | Yes | Prediction confidence | high/medium/low |
| smp_policy | Enum | Yes | Shoreline Management Plan policy | hold_the_line/managed_realignment/advance/no_active_intervention |
| properties_at_risk_20yr | Integer | No | Property count within 20yr zone | >=0 |
| properties_at_risk_50yr | Integer | No | Property count within 50yr zone | >=0 |
| properties_at_risk_100yr | Integer | No | Property count within 100yr zone | >=0 |

**Data Volume**: ~56,000 sections (6,000km / 50m intervals, not all eroding)

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: LiDAR data volumes (2TB/year) require cloud-based processing with burst compute capability

**TC-2**: Must use OSGB36 coordinate system with OSGM15 geoid model for consistency with Ordnance Survey

**TC-3**: Must integrate with EA's existing Geomatics systems for survey scheduling

### Business Constraints

**BC-1**: Budget cap of GBP 5M capital over 2 years

**BC-2**: Six NCMP regional delivery partners have existing contracts — platform must accommodate their workflows

**BC-3**: Public service publication must be preceded by community engagement (cannot "surprise" communities with erosion data)

### Assumptions

**A-1**: UKCP18 climate projections remain the standard reference for UK climate adaptation planning

**A-2**: Ordnance Survey AddressBase will be available under Public Sector Mapping Agreement at no additional cost

**A-3**: NCMP LiDAR survey frequency will be maintained at current levels (1-2 year cycle for eroding coasts)

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Regional programmes integrated | 0 | 6/6 | 18 months | Platform status |
| LiDAR processing automation | 20% | 80% | 12 months | Pipeline metrics |
| Coastline with 50m predictions | 30% | 85% | 24 months | Coverage analysis |
| Local authorities using platform | 0 | 80+ | 24 months | User registration |
| FCERM business case prep time reduction | 0% | 40% | 18 months | Process measurement |
| Public service user satisfaction | n/a | >7/10 | 12 months post-launch | Survey |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| LiDAR | Light Detection and Ranging — airborne laser survey for terrain mapping |
| DEM | Digital Elevation Model — gridded surface height data |
| NCMP | National Coastal Monitoring Programme — EA-funded survey programme |
| SMP | Shoreline Management Plan — policy framework for coastal management |
| FCERM | Flood and Coastal Erosion Risk Management |
| UKCP18 | UK Climate Projections 2018 — Met Office climate change scenarios |
| OSGB36 | Ordnance Survey Great Britain 1936 — national coordinate system |
| RCP | Representative Concentration Pathway — climate emissions scenario |
| BCR | Benefit-Cost Ratio — HM Treasury Green Book appraisal metric |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Coastal Erosion Monitoring
**Model**: Claude Opus 4.6
