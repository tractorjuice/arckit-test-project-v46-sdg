# Project Requirements: Forestry Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Forestry Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Forestry Digital |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | FC Programme Board, DEFRA Digital, Forestry Commission, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive requirements for the Forestry Management System — the digital platform enabling the Forestry Commission to manage felling licences, woodland creation grants, the National Forest Inventory, and UK Woodland Carbon Code integration for woodland creation and sustainable forestry management in England.

---

## Executive Summary

### Business Context

The Forestry Commission regulates forestry in England through felling licences (Forestry Act 1967), administers woodland creation grants (England Woodland Creation Offer, Countryside Stewardship), and maintains the National Forest Inventory. Current systems are predominantly paper-based or use ageing legacy applications that cannot support the scale and pace of woodland creation needed to meet the England Trees Action Plan target of 7,500 hectares per year. The timber industry estimates that regulatory delays cost £15M annually in deferred harvesting operations.

The system must also integrate with the UK Woodland Carbon Code to enable landowners to certify carbon credits from woodland creation, supporting net zero targets and providing additional financial incentive for tree planting.

### Objectives

- Digitise end-to-end felling licence workflow reducing processing time from 13 weeks to 4 weeks
- Streamline woodland creation grant applications to accelerate planting towards 7,500 ha/year target
- Modernise the National Forest Inventory with near-real-time satellite and LiDAR integration
- Integrate UK Woodland Carbon Code verification to enable carbon credit stacking
- Provide real-time reporting on national woodland creation progress

### Expected Outcomes

- Felling licence processing time reduced from 13 weeks to 4 weeks within 12 months
- Woodland creation grant processing reduced from 6 months to 6 weeks
- Annual woodland creation rate increased from 2,500 ha/year to 5,000 ha/year (trajectory to 7,500)
- National Forest Inventory update cycle reduced from 10 years to 12 months

### Project Scope

**In Scope**:

- Digital felling licence application, assessment, and issuance
- Woodland creation grant application and assessment (EWCO, Countryside Stewardship Woodland)
- National Forest Inventory data management with satellite/LiDAR integration
- UK Woodland Carbon Code verification integration
- FC officer mobile inspection and field assessment tools
- Restocking condition tracking and compliance monitoring
- Reporting dashboards for national woodland creation progress
- GIS-based site mapping with environmental constraint overlays

**Out of Scope**:

- Scotland and Wales forestry systems (separate bodies)
- Timber market trading platform
- Physical forest management operations (harvesting, planting — data consumed only)
- Tree Preservation Order management (local authority responsibility)
- Urban tree management

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | Forestry Commission | Decision maker |
| FC Chief Forester | Professional standards | Forestry Commission | Standards compliance |
| FC Operations Director | Operational delivery | Forestry Commission | Process design |
| FC Digital Director | IT strategy | Forestry Commission | Architecture |
| Woodland owners | End users | Private sector | Requirements input |
| Confor | Industry representation | Timber sector | Industry requirements |
| Natural England | Environmental oversight | NDPB | Environmental constraints |
| Woodland Trust | Conservation advocacy | Charity | Environmental standards |
| Forest Research | Evidence base | FC research agency | Inventory methodology |

---

## Business Requirements

### BR-1: Digital Felling Licence Workflow

**Description**: Replace the paper-based felling licence application, assessment, and issuance process with an end-to-end digital workflow that includes GIS-based site identification, automated environmental constraint checking, digital officer assessment, and electronic licence issuance.

**Rationale**: The Forestry Act 1967 requires felling licences for timber harvesting above 5 cubic metres per quarter. The current paper-based process averages 13 weeks against a statutory target of 10 weeks, causing £15M annual cost to the forestry sector in delayed operations. Digital processing can automate routine checks and enable parallel assessment workflows.

**Success Criteria**:

- Average felling licence processing time < 4 weeks
- 100% of applications received digitally within 18 months
- Automated environmental constraint checking covering 100% of known designations

**Priority**: MUST_HAVE

**Stakeholder**: FC Operations Director, Confor

---

### BR-2: Streamlined Woodland Creation Grant Processing

**Description**: Deliver a digital grant application and assessment workflow for England Woodland Creation Offer (EWCO) and Countryside Stewardship Woodland Management options, with pre-populated data, automated environmental checks, and integrated carbon code registration.

**Rationale**: Grant processing delays are the primary barrier to accelerating woodland creation. Current processing takes 6 months on average, meaning applicants frequently miss the November-March planting season. The England Trees Action Plan requires a step-change in processing efficiency.

**Success Criteria**:

- Average grant processing time < 6 weeks
- Grant application abandonment rate < 10% (from 30% current)
- 95% of environmental constraint checks automated

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA, FC Chair

---

### BR-3: National Forest Inventory Modernisation

**Description**: Transform the National Forest Inventory from a periodic, field-survey-based assessment (10-year cycle) to a continuous, near-real-time inventory integrating Sentinel-2 satellite imagery, LiDAR data, and targeted field surveys.

**Rationale**: The current NFI relies on periodic field surveys across sample plots, producing results that are years out of date. Policy decisions on woodland creation, carbon accounting, and biodiversity assessment require current data. Satellite-based monitoring can detect woodland creation, loss, and condition changes within months rather than years.

**Success Criteria**:

- Woodland extent updated within 12 months of change (from 10-year cycle)
- Satellite-detected changes validated by field assessment within 3 months
- NFI data publicly accessible through open data portal
- Woodland area estimates accurate within 2% of ground truth

**Priority**: SHOULD_HAVE

**Stakeholder**: Forest Research, DEFRA

---

### BR-4: UK Woodland Carbon Code Integration

**Description**: Enable seamless registration and verification of woodland creation projects under the UK Woodland Carbon Code within the forestry management system, allowing landowners to certify carbon credits alongside grant-funded woodland creation.

**Rationale**: Carbon revenue (approximately £15-25 per tCO2e) significantly improves the financial case for woodland creation. Currently, Carbon Code registration requires separate application, duplicate data submission, and independent verification — creating friction that deters landowner participation. Integration enables payment stacking and reduces administrative burden.

**Success Criteria**:

- Combined grant and Carbon Code application reducing data entry by 60%
- Automated carbon sequestration projections based on planting plans
- Carbon credit issuance integrated with UK Land Carbon Registry

**Priority**: SHOULD_HAVE

**Stakeholder**: Carbon Code Registry, Landowners

---

## Functional Requirements

### User Personas

#### Persona 1: Robert — Woodland Owner

- **Role**: Private woodland owner with 50 hectares of commercial forestry
- **Goals**: Apply for felling licence efficiently, plan restocking, access grants
- **Pain Points**: Paper forms, slow processing, unclear requirements, poor rural broadband
- **Technical Proficiency**: Low-Medium

#### Persona 2: Claire — FC Woodland Officer

- **Role**: Forestry Commission Woodland Officer covering a regional area
- **Goals**: Assess felling licence applications, conduct site inspections, process grants
- **Pain Points**: Paper-based workflow, manual environmental constraint checking, travel time
- **Technical Proficiency**: Medium

#### Persona 3: Mark — Forestry Agent

- **Role**: Professional forestry consultant managing multiple woodland estates
- **Goals**: Submit multiple applications efficiently, track portfolio, manage compliance
- **Pain Points**: Duplicate data entry, inconsistent processes across regions, lack of status visibility
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: Digital Felling Licence Application

**Description**: The system must enable woodland owners and forestry agents to submit felling licence applications digitally, with GIS-based site identification, species and volume details, and proposed restocking plans.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a woodland location, when user draws felling compartment on map, then area and grid reference are calculated automatically
- [ ] Given a felling application, when environmental constraints are checked, then SSSI, ancient woodland, and TPO overlaps are identified automatically
- [ ] Given a completed application, when submitted, then applicant receives confirmation with expected processing timeline

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Automated Environmental Constraint Checking

**Description**: The system must automatically cross-reference felling licence and grant applications against environmental designations (SSSI, ancient woodland, priority habitats, scheduled monuments, flood risk zones) and flag conflicts for officer review.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a site boundary, when constraint check runs, then all overlapping designations are identified within 30 seconds
- [ ] Given a constraint overlap, when flagged, then the specific regulation and required consultation is identified
- [ ] Given an ancient woodland buffer zone overlap, when detected, then application is automatically routed for specialist ecological review

**Data Requirements**:

- **Inputs**: Site boundary polygon, designation layers (NE, EA, Historic England, OS)
- **Outputs**: Constraint report listing all designations, distances, and required actions

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: FC Officer Digital Assessment Workflow

**Description**: The system must provide FC officers with a digital workflow for assessing felling licence applications, including checklist-based assessment, site visit scheduling, field data capture, and decision recording.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an assigned application, when officer opens assessment, then automated constraint check results are pre-populated
- [ ] Given a site visit requirement, when scheduled, then route optimisation suggests efficient visit sequences
- [ ] Given assessment completion, when decision is recorded, then licence is generated automatically (if approved)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-4: Mobile Field Inspection Tool

**Description**: The system must provide FC officers with a mobile application for field inspections, supporting offline operation in areas with poor connectivity, GPS-based site location, photo capture, and digital form completion.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given poor/no mobile connectivity, when officer conducts inspection, then data is stored locally and synced when connection restored
- [ ] Given a GPS position, when officer arrives at site, then application boundary and compartment details are displayed on map
- [ ] Given field observations, when officer captures photos, then images are geotagged and linked to application

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-5: Woodland Creation Grant Application

**Description**: The system must enable landowners and agents to submit EWCO and Countryside Stewardship Woodland Management applications, with pre-populated land parcel data, species selection guidance, and automated eligibility checking.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an RPA-registered land parcel, when selected, then parcel boundaries, area, and current land use are pre-populated from RPA data
- [ ] Given a proposed planting scheme, when species are selected, then system validates suitability for soil type and ecological zone
- [ ] Given application submission, when eligibility checks run, then grant rate and estimated payment are calculated

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: RPA land parcel data API, soil data (Cranfield University/UKCEH)

---

#### FR-6: National Forest Inventory Data Integration

**Description**: The system must ingest, process, and manage National Forest Inventory data from satellite imagery (Sentinel-2, aerial photography), LiDAR surveys, and field assessments, maintaining a continuous woodland extent and condition dataset.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a Sentinel-2 acquisition, when processed, then woodland change detection results available within 7 days
- [ ] Given a detected woodland change, when validated, then NFI updated with change type, date, and evidence
- [ ] Given an NFI query, when accessed via API, then current woodland extent data returned in OGC-compliant format

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-7: Carbon Code Registration Integration

**Description**: The system must integrate with the UK Woodland Carbon Code to enable combined grant and carbon registration applications, automated carbon projection calculations, and credit verification workflow.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a woodland creation application, when Carbon Code registration is selected, then shared data fields are pre-populated (no duplicate entry)
- [ ] Given a planting plan with species mix, when carbon projection runs, then estimated tCO2e sequestration is calculated per year over rotation
- [ ] Given Carbon Code verification, when completed, then carbon credits are registered on UK Land Carbon Registry via API

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**:

- Web page load time: < 3 seconds (95th percentile) — accommodating rural broadband
- Environmental constraint check: < 30 seconds for single site
- Map rendering with designation overlays: < 5 seconds
- API response time: < 500ms (95th percentile)

**Load Conditions**:

- Peak load: 200 concurrent users (planting season November-March)
- Average load: 50 concurrent users
- Batch processing: NFI satellite imagery processing overnight

**Priority**: HIGH

---

### Availability

#### NFR-A-1: Availability Target

**Requirement**: 99.5% uptime during business hours (Monday-Friday 08:00-18:00 GMT).

- Maximum planned downtime: 8 hours per month
- Maximum unplanned downtime: 43.8 hours per year
- Seasonal availability: Higher availability required during planting season (November-March)

**Priority**: HIGH

---

#### NFR-A-2: Offline Capability

**Requirement**: Mobile field inspection application must function fully offline, with data synchronisation when connectivity is restored. Offline capability must support inspection workflows for up to 5 days without connectivity.

**Priority**: MUST_HAVE (critical for rural forestry operations)

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: Users authenticate via GOV.UK One Login. FC officers additionally authenticate through FC Active Directory integration for internal tools.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Data Classification

**Requirement**: All data classified as OFFICIAL. Landowner personal data and financial grant details subject to additional access controls under UK GDPR.

**Priority**: CRITICAL

---

### Compliance

#### NFR-C-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance. Additional consideration for users with limited digital literacy (many woodland owners are older, rural demographics).

**Priority**: CRITICAL

---

#### NFR-C-2: Environmental Data Standards

**Requirement**: All geospatial data must comply with INSPIRE Regulations 2009 for environmental spatial data publication. Woodland extent data must be published as open data.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: RPA Land Parcel Data

**Purpose**: Pre-populate grant applications with registered land parcel boundaries and current land use data

**Integration Type**: Real-time API

**Data Exchanged**: Land parcel boundaries, areas, current land use classification, ownership reference

**Priority**: CRITICAL

---

### INT-2: Natural England Designation Data

**Purpose**: Environmental constraint checking for felling licences and grant applications

**Integration Type**: OGC WFS (spatial data service)

**Data Exchanged**: SSSI boundaries, ancient woodland inventory, priority habitat inventory, SAC/SPA/Ramsar boundaries

**Priority**: CRITICAL

---

### INT-3: UK Woodland Carbon Code Registry

**Purpose**: Carbon credit registration and verification for woodland creation projects

**Integration Type**: RESTful API

**Data Exchanged**: Project registration, carbon projections, verification status, credit issuance

**Priority**: HIGH

---

### INT-4: Ordnance Survey

**Purpose**: Base mapping and addressing for site identification

**Integration Type**: OS Data Hub APIs (mapping, features, places)

**Priority**: CRITICAL

---

### INT-5: Sentinel-2 / Copernicus Data

**Purpose**: Satellite imagery for National Forest Inventory change detection

**Integration Type**: Copernicus Data Space API (batch download and processing)

**Priority**: HIGH

---

## Data Requirements

### Data Entities

#### Entity 1: Felling Licence

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| licence_id | UUID | Yes | Unique identifier | Primary key |
| applicant_id | UUID | Yes | Applicant reference | Foreign key |
| site_boundary | Geometry | Yes | Felling compartment boundary | Valid polygon |
| species | JSONB | Yes | Species, volume, area details | Validated against FC species list |
| restocking_plan | JSONB | Yes | Proposed restocking species and timeline | Required for approval |
| status | Enum | Yes | Application lifecycle | ['draft', 'submitted', 'assessment', 'site_visit', 'approved', 'refused', 'expired'] |
| decision_date | Date | No | Date of decision | Null until determined |
| conditions | Text[] | No | Licence conditions | Set at approval |

**Data Volume**: 5,000 applications/year, growing to 8,000

**Data Retention**: 20 years (forestry rotation cycle)

---

#### Entity 2: Woodland Creation Grant

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| grant_id | UUID | Yes | Unique identifier | Primary key |
| scheme | Enum | Yes | Grant scheme | ['EWCO', 'CS_WOODLAND', 'CS_MAINTENANCE'] |
| land_parcels | Geometry[] | Yes | Planting site boundaries | RPA parcel references |
| species_mix | JSONB | Yes | Proposed species and percentages | Min 3 native species for EWCO |
| area_hectares | Decimal | Yes | Total planting area | Positive |
| grant_value | Decimal | Yes | Calculated grant amount | Based on scheme rates |
| carbon_code_ref | String | No | Carbon Code project reference | If carbon stacking |

**Data Volume**: 3,000 applications/year, target 10,000

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must accommodate poor rural broadband — pages must load within 3 seconds on 2 Mbps connections

**TC-2**: Mobile app must work offline for extended periods in remote woodland locations

**TC-3**: Must deploy on UK sovereign cloud infrastructure

**TC-4**: Must support OSGB36 and WGS84 coordinate reference systems

### Business Constraints

**BC-1**: System must be operational for the 2027/28 planting season (go-live by September 2027)

**BC-2**: Total programme budget £8M over 3 years

**BC-3**: Must maintain service continuity during transition from legacy FC systems

### Assumptions

**A-1**: RPA will provide API access to land parcel data within the required timescale

**A-2**: UK Woodland Carbon Code governance will support API-based integration

**A-3**: FC officers will be provided with suitable mobile devices for field inspections

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Felling licence processing time | 13 weeks | 4 weeks | 12 months | Platform analytics |
| Grant processing time | 6 months | 6 weeks | 18 months | Platform analytics |
| Annual woodland creation rate | 2,500 ha/yr | 5,000 ha/yr | 2 years | NFI data |
| Grant abandonment rate | 30% | <10% | 12 months | Application tracking |
| NFI update frequency | 10-year cycle | 12-month cycle | 2 years | Inventory records |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| EWCO | England Woodland Creation Offer — DEFRA/FC grant scheme |
| Felling Licence | Permission required under Forestry Act 1967 to fell >5m3 per quarter |
| NFI | National Forest Inventory — comprehensive survey of UK woodland |
| Restocking | Obligation to replant after felling (usually condition of licence) |
| UK Woodland Carbon Code | Voluntary standard for woodland carbon credit verification |
| Compartment | Defined area of woodland managed as a unit |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 15 Architecture Principles
- ARC-002-STKE-v1.0 — Forestry Management System Stakeholder Analysis
- England Trees Action Plan 2021
- Forestry Act 1967
- UK Woodland Carbon Code Requirements

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Forestry Management System
**Model**: Claude Opus 4.6
