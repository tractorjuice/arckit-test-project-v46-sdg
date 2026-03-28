# Project Requirements: Land Use Planning Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Land Use Planning Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Land Use Analytics |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, DEFRA Digital, Natural England, Environment Agency, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Land Use Planning Analytics platform — a system for monitoring land use change across England using satellite imagery (Sentinel-2), environmental datasets, and administrative records to support evidence-based environmental policy, Environmental Improvement Plan target reporting, and proportionate compliance monitoring for Environmental Land Management schemes.

---

## Executive Summary

### Business Context

DEFRA is legally required to report progress against Environmental Improvement Plan (EIP) targets set under the Environment Act 2021, yet currently lacks systematic, timely data on land use change across England. Existing data sources are fragmented: the UKCEH Land Cover Map is updated every 5-7 years, the National Forest Inventory on a 10-year cycle, and the agricultural census relies on self-reported data. The Office for Environmental Protection (OEP) has criticised insufficient monitoring evidence. Simultaneously, the transition from Common Agricultural Policy to Environmental Land Management (ELM) schemes creates a need for cost-effective compliance monitoring to replace expensive physical inspections.

Satellite earth observation — particularly Sentinel-2 (free, 10m resolution, 5-day revisit) — offers the capability to detect land use changes at national scale within weeks rather than years, at a fraction of the cost of field surveys. Several EU member states already use satellite monitoring for agricultural compliance under the Common Agricultural Policy.

### Objectives

- Establish automated satellite imagery processing pipeline detecting major land use changes within 30 days
- Integrate 5+ authoritative environmental datasets into a unified analytical platform
- Support EIP target reporting with standardised environmental metrics
- Enable risk-based ELM scheme compliance monitoring with transparent governance
- Provide open data access for research and public accountability

### Expected Outcomes

- EIP annual report produced in 4 weeks (from 12 months)
- Land use change detected within 30 days (from years/never)
- ELM compliance monitoring cost reduced by 60% through satellite-based risk targeting
- DEFRA analysts have access to unified land use intelligence within 12 months

### Project Scope

**In Scope**:

- Sentinel-2 satellite imagery acquisition, processing, and analysis pipeline
- Land use change detection algorithms (vegetation indices, classification)
- Integration with UKCEH Land Cover Map, National Forest Inventory, Agricultural Land Classification, Priority Habitat Inventory, SSSI condition data
- Environmental analytics dashboards for EIP target reporting
- Risk-based compliance indicators for ELM scheme monitoring
- Farmer self-service data portal
- Open data publication API
- SSSI and protected site change alerting for Natural England

**Out of Scope**:

- Purchasing additional satellite data (beyond freely available Sentinel-2 and Copernicus data)
- Physical field survey operations (data consumed only)
- Direct ELM enforcement decisions (platform provides intelligence, not decisions)
- Urban land use change monitoring (focus on rural and semi-rural)
- Real-time monitoring (near-real-time, not streaming)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | DEFRA | Decision maker |
| DEFRA Chief Scientific Adviser | Scientific authority | DEFRA | Methodology validation |
| Environmental Analysis Director | Policy evidence lead | DEFRA | Analytics requirements |
| Natural England | Protected sites | NDPB | Habitat monitoring |
| Environment Agency | Environmental regulation | NDPB | Land contamination, water quality |
| RPA | ELM scheme administration | Executive agency | Compliance monitoring |
| NFU | Farming sector | Industry body | Proportionality review |
| UKCEH | Land cover science | Research council | Methodology, validation |
| ICO | Data protection | Regulator | Privacy, surveillance proportionality |

---

## Business Requirements

### BR-1: Automated Land Use Change Detection

**Description**: Establish an automated processing pipeline that ingests Sentinel-2 satellite imagery and detects land use changes across England within 30 days of occurrence, covering major transition types (grassland to arable, woodland loss, peatland drainage, built development on agricultural land).

**Rationale**: Timely change detection is the foundation of evidence-based environmental policy. Current methods detect changes years or decades after they occur — far too late for policy intervention. The Sentinel-2 constellation provides free, high-resolution imagery every 5 days, making automated national-scale monitoring technically feasible.

**Success Criteria**:

- Land use changes detected within 30 days of occurrence
- Detection accuracy > 90% for major land use transitions
- False positive rate < 5%
- Full England coverage processed per Sentinel-2 revisit cycle

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Chief Scientific Adviser

---

### BR-2: Unified Environmental Analytics Platform

**Description**: Integrate at least 5 authoritative environmental datasets into a single analytical platform with standardised metrics, enabling cross-dataset analysis and EIP target reporting.

**Rationale**: Environmental policy analysis currently requires manual data assembly from multiple organisations with different standards, formats, and update cycles. A unified platform enables analysts to answer complex questions about environmental trends without weeks of data preparation.

**Success Criteria**:

- 5+ authoritative datasets integrated (UKCEH LCM, NFI, ALC, PHI, SSSI condition)
- Standardised environmental metrics aligned with EIP apex targets
- Time to produce annual EIP land use assessment < 4 weeks (from 12 months)
- 50+ DEFRA analysts using platform within 12 months

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Environmental Analysis Director

---

### BR-3: Proportionate ELM Compliance Monitoring

**Description**: Provide risk-based compliance indicators for ELM scheme monitoring using satellite-derived evidence, enabling the RPA to target inspections efficiently while maintaining proportionate, transparent governance that preserves farmer trust.

**Rationale**: Physical farm inspections are expensive (approximately £500 per visit) and cover only 5% of agreements annually. Satellite monitoring can provide risk indicators for all agreements, enabling targeted inspections where satellite evidence suggests potential non-compliance. This must be balanced with governance that prevents satellite data being used punitively.

**Success Criteria**:

- Risk-based compliance indicators available for 100% of ELM agreements
- Physical inspection volume reduced by 60% while improving compliance detection
- Farmer trust score > 60% in annual survey
- Clear governance framework approved by ICO

**Priority**: SHOULD_HAVE

**Stakeholder**: RPA, NFU

---

### BR-4: Protected Site Change Alerting

**Description**: Provide Natural England with automated alerts when satellite imagery detects potential land use changes within or adjacent to SSSIs, SACs, SPAs, and Ramsar sites, enabling rapid response to possible damage.

**Rationale**: Natural England cannot maintain adequate manual monitoring coverage of 4,127 SSSIs across 8% of England's land area. Satellite-based alerting provides an early warning system for site condition changes, enabling targeted field assessment and early intervention before damage becomes irreversible.

**Success Criteria**:

- Automated change alerts for 100% of SSSI boundaries
- Alert generated within 30 days of detected change
- False alert rate < 10% (to avoid alert fatigue)
- Alert includes imagery comparison, change classification, and suggested response

**Priority**: SHOULD_HAVE

**Stakeholder**: Natural England

---

### BR-5: Farmer Self-Service Data Portal

**Description**: Provide farmers and landowners with access to satellite-derived data about their own holdings, enabling self-assessment of ELM compliance and land management planning.

**Rationale**: Transparency is essential for maintaining farmer trust in satellite monitoring. Farmers should see the same data that government agencies see about their land. Self-service access also enables proactive land management and supports the collaborative intent of ELM schemes.

**Success Criteria**:

- Farmer portal with satellite imagery and change detection for own holdings
- 10,000+ registered farmer users within 12 months
- Farmer satisfaction score > 7/10

**Priority**: SHOULD_HAVE

**Stakeholder**: NFU, Landowners

---

## Functional Requirements

### User Personas

#### Persona 1: Dr. Priya — DEFRA Environmental Analyst

- **Role**: Senior Environmental Analyst in DEFRA's Evidence and Analysis directorate
- **Goals**: Produce EIP target reports, analyse land use trends, support policy development
- **Pain Points**: Manual data assembly, inconsistent datasets, months to produce analysis
- **Technical Proficiency**: High (GIS, R/Python)

#### Persona 2: Richard — Natural England Site Officer

- **Role**: Natural England SSSI Responsible Officer covering a regional area
- **Goals**: Monitor SSSI condition, respond to damage, prioritise site visits
- **Pain Points**: Too many sites to visit, outdated condition assessments, reactive approach
- **Technical Proficiency**: Medium

#### Persona 3: Helen — Farmer (ELM Agreement Holder)

- **Role**: Tenant farmer with Sustainable Farming Incentive agreement
- **Goals**: Understand compliance status, plan land management, access evidence
- **Pain Points**: Uncertainty about compliance expectations, fear of penalties
- **Technical Proficiency**: Low-Medium

---

### Functional Requirements Detail

#### FR-1: Sentinel-2 Imagery Processing Pipeline

**Description**: The system must automatically acquire, process, and analyse Sentinel-2 satellite imagery for England, producing cloud-free composite images and vegetation indices at 10m resolution.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a new Sentinel-2 acquisition, when imagery is available on Copernicus Data Space, then download and processing initiates automatically within 24 hours
- [ ] Given cloud-contaminated pixels, when cloud masking is applied, then cloud-free composites are generated using multi-temporal fusion
- [ ] Given processed imagery, when vegetation indices are calculated (NDVI, EVI, NDWI), then index values are produced at 10m resolution for all non-cloud pixels

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Land Use Change Detection

**Description**: The system must detect land use changes by comparing current satellite imagery against historical baselines and reference datasets, classifying changes into defined categories.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given current and historical imagery, when change detection runs, then changes are classified into categories (grassland to arable, woodland loss, built development, peatland change, wetland change)
- [ ] Given a detected change, when confidence score is calculated, then only changes above 85% confidence threshold are flagged as confirmed
- [ ] Given confirmed changes, when mapped, then change polygons are generated with area, location, and classification

**Change Categories**:

| Category | Description | EIP Relevance |
|----------|-------------|---------------|
| Grassland to arable | Permanent grassland conversion | Habitat loss, soil carbon |
| Woodland loss | Tree cover removal | Carbon, biodiversity |
| Built development | Agricultural to urban | Land take, soil sealing |
| Peatland change | Drainage, extraction, restoration | Carbon, water quality |
| Wetland change | Drainage or creation | Biodiversity, flood risk |
| Habitat creation | New habitat establishment | BNG, 30by30 |

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Environmental Dataset Integration

**Description**: The system must ingest, harmonise, and index environmental datasets from multiple authoritative sources, providing a unified query interface.

**Relates To**: BR-2

**Datasets Required**:

| Dataset | Source | Update Frequency | Format |
|---------|--------|------------------|--------|
| UK Land Cover Map | UKCEH | 5-7 years | GeoTIFF/Shapefile |
| National Forest Inventory | FC/Forest Research | Continuous (target) | GeoPackage |
| Agricultural Land Classification | Natural England | Periodic | Shapefile |
| Priority Habitat Inventory | Natural England | Annual | GeoPackage |
| SSSI Condition Assessment | Natural England | Variable | API/CSV |
| Environmental Stewardship/ELM | RPA | Monthly | API |

**Acceptance Criteria**:

- [ ] Given a new dataset release, when ingested, then data is harmonised to common spatial reference and classification scheme within 7 days
- [ ] Given multiple datasets for same area, when queried, then all relevant layers are returned with metadata on source, date, and quality
- [ ] Given a spatial query, when executed, then results from all integrated datasets are returned within 10 seconds

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: EIP Target Reporting Dashboards

**Description**: The system must provide analytical dashboards aligned with Environmental Improvement Plan apex targets, showing progress indicators, trends, and drill-down capability.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given EIP apex targets, when dashboard loads, then current progress indicators are displayed with trend direction
- [ ] Given a national indicator, when user drills down, then regional and local breakdown is available
- [ ] Given a reporting period, when annual report is requested, then standardised metrics are exported in publication-ready format

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: SSSI Change Alert System

**Description**: The system must monitor satellite imagery within SSSI boundaries and buffer zones, generating automated alerts when potential land use changes are detected.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a detected change within an SSSI boundary, when alert is generated, then NE site officer receives notification with imagery comparison, change classification, and affected feature
- [ ] Given an SSSI buffer zone (configurable, default 500m), when change is detected within buffer, then alert is generated with lower priority
- [ ] Given an alert, when site officer reviews, then they can mark as "confirmed change", "false alarm", or "requires site visit"

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-6: ELM Risk-Based Compliance Indicators

**Description**: The system must generate risk scores for ELM scheme agreements based on satellite-derived evidence, enabling the RPA to target compliance inspections proportionately.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given an ELM agreement with spatial extent, when satellite data is analysed, then compliance risk score is calculated (LOW/MEDIUM/HIGH)
- [ ] Given a HIGH risk score, when reviewed, then supporting evidence (imagery, change detection, vegetation index anomaly) is provided
- [ ] Given risk scores, when aggregated, then RPA can sort and filter agreements by risk level for inspection planning

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-7: Farmer Self-Service Portal

**Description**: The system must provide a portal where farmers can view satellite imagery and change detection results for their own land holdings.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given an authenticated farmer, when they access the portal, then satellite imagery for their registered land parcels is displayed
- [ ] Given their land parcels, when change detection has run, then any detected changes are shown with classification and confidence level
- [ ] Given a detected change, when farmer reviews, then they can provide context ("planned management activity", "query this detection")

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Batch Processing

**Requirement**: Satellite imagery processing pipeline must complete full England Sentinel-2 acquisition within 48 hours of data availability.

- Sentinel-2 tile processing: < 5 minutes per tile (approximately 300 tiles for England)
- Change detection analysis: < 2 hours for full England coverage
- Dashboard refresh: Nightly batch update with latest processed results

**Priority**: HIGH

---

#### NFR-P-2: Interactive Query

**Requirement**: Interactive analytics queries must return results within acceptable timescales:

- Simple spatial queries (single location): < 5 seconds
- Complex analytical queries (regional trends): < 30 seconds
- Dashboard page load: < 5 seconds with pre-computed indicators

**Priority**: HIGH

---

### Availability

#### NFR-A-1: Availability Target

**Requirement**: 99.0% uptime for analytical dashboards and farmer portal. Batch processing pipeline can tolerate planned downtime with catch-up processing.

**Priority**: MEDIUM

---

### Security

#### NFR-SEC-1: Data Classification

**Requirement**: Platform operates at OFFICIAL. Individual farmer compliance data classified as OFFICIAL with restricted access (only RPA compliance officers and the individual farmer).

**Priority**: CRITICAL

---

#### NFR-SEC-2: Surveillance Proportionality

**Requirement**: DPIA must specifically address the proportionality of satellite-based land monitoring. Data access controls must prevent systematic surveillance of individual farmers. Aggregate analytics preferred over individual-level monitoring where possible.

**Priority**: CRITICAL

---

### Compliance

#### NFR-C-1: INSPIRE Compliance

**Requirement**: All environmental spatial datasets produced by the platform must comply with INSPIRE Regulations 2009 for metadata and publication.

**Priority**: HIGH

---

#### NFR-C-2: Open Data

**Requirement**: Aggregate land use change data and environmental indicators must be published as open data via API and download, supporting government transparency commitments.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Copernicus Data Space (Sentinel-2)

**Purpose**: Satellite imagery acquisition

**Integration Type**: API (download) and cloud processing (Copernicus Data Space Ecosystem)

**Data Exchanged**: Sentinel-2 Level-2A (surface reflectance) imagery tiles

**Priority**: CRITICAL

---

### INT-2: UKCEH Land Cover Map

**Purpose**: Baseline land cover classification for change detection

**Integration Type**: File-based (periodic dataset delivery)

**Priority**: CRITICAL

---

### INT-3: Natural England Designated Sites API

**Purpose**: SSSI, SAC, SPA boundaries for protected site alerting

**Integration Type**: OGC WFS

**Priority**: HIGH

---

### INT-4: RPA Land Data and ELM Agreements

**Purpose**: Farm boundary data and ELM agreement spatial extents for compliance monitoring

**Integration Type**: RESTful API

**Priority**: HIGH

---

### INT-5: BNG Platform (Project 001)

**Purpose**: Share habitat creation data and biodiversity outcome monitoring

**Integration Type**: Event-driven (async)

**Priority**: MEDIUM

---

### INT-6: Forestry Management System (Project 002)

**Purpose**: Woodland change detection feeds National Forest Inventory

**Integration Type**: Event-driven (async)

**Priority**: MEDIUM

---

## Data Requirements

### Data Entities

#### Entity 1: Land Use Change Event

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| event_id | UUID | Yes | Unique identifier | Primary key |
| location | Geometry (Polygon) | Yes | Change area boundary | Valid polygon |
| change_type | Enum | Yes | Change classification | From defined categories |
| detection_date | Date | Yes | Date change detected | Indexed |
| estimated_change_date | Date | No | Estimated date change occurred | Derived from imagery timeline |
| confidence | Decimal(3,2) | Yes | Detection confidence score | 0.00-1.00 |
| area_hectares | Decimal(10,4) | Yes | Area affected | Calculated |
| source_imagery | JSONB | Yes | Sentinel-2 scene references | Before/after pairs |
| validation_status | Enum | Yes | Ground-truth status | ['unvalidated', 'confirmed', 'false_positive', 'requires_visit'] |

**Data Volume**: 50,000 detected events per year (England)

**Data Retention**: Permanent (environmental monitoring record)

---

#### Entity 2: Satellite Image Composite

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| composite_id | UUID | Yes | Unique identifier | Primary key |
| tile_reference | String | Yes | Sentinel-2 tile grid reference | MGRS format |
| period | DateRange | Yes | Compositing period | Typically 10-30 days |
| cloud_coverage | Decimal | Yes | Percentage cloud remaining | Target < 10% |
| bands | Raster | Yes | Multi-band composite image | GeoTIFF, COG format |
| vegetation_indices | Raster | Yes | Derived NDVI, EVI, NDWI | GeoTIFF, COG |

**Data Volume**: ~6,000 composites per year (300 tiles x 20 periods)

**Data Retention**: 10 years for trend analysis

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use freely available Sentinel-2 data (no budget for commercial satellite imagery)

**TC-2**: Cloud computing for satellite processing must be within DEFRA's cloud hosting

**TC-3**: Satellite resolution (10m) limits detection to changes > 0.1 hectare

### Business Constraints

**BC-1**: Total programme budget £6M over 3 years

**BC-2**: DPIA must be approved by ICO before farmer-level data processing commences

**BC-3**: Methodology must be peer-reviewed and published before operational use

### Assumptions

**A-1**: Sentinel-2 constellation continues to operate with current revisit frequency

**A-2**: UKCEH will provide Land Cover Map data under existing government licence

**A-3**: RPA will provide ELM agreement spatial data via API within required timescale

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| EIP report production time | 12 months | 4 weeks | 18 months | Process timing |
| Change detection latency | Years/never | 30 days | 12 months | Pipeline analytics |
| ELM inspection cost | £500/visit at 5% coverage | £200/visit at 2% coverage (satellite-targeted) | 2 years | RPA cost data |
| Farmer self-service users | 0 | 10,000 | 18 months | Portal analytics |
| Detection accuracy | N/A | >90% | 12 months | Ground truth validation |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| Sentinel-2 | ESA/Copernicus earth observation satellite constellation, 10m resolution, 5-day revisit |
| NDVI | Normalised Difference Vegetation Index — measure of vegetation health/density |
| EVI | Enhanced Vegetation Index — improved vegetation index for high biomass areas |
| NDWI | Normalised Difference Water Index — measure of water content |
| COG | Cloud-Optimised GeoTIFF — efficient format for cloud-hosted raster data |
| EIP | Environmental Improvement Plan — statutory targets under Environment Act 2021 |
| ELM | Environmental Land Management — post-CAP agricultural support schemes |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 15 Architecture Principles
- ARC-003-STKE-v1.0 — Land Use Planning Analytics Stakeholder Analysis
- Environmental Improvement Plan 2023
- Copernicus Sentinel-2 Technical Guide
- UKCEH Land Cover Map Technical Documentation

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Land Use Planning Analytics
**Model**: Claude Opus 4.6
