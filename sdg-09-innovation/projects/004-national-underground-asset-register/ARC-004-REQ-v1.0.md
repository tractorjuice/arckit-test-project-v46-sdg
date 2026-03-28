# Project Requirements: National Underground Asset Register

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | National Underground Asset Register (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, National Underground Asset Register Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NUAR Programme Board, Geospatial Commission, Utility Companies, NCSC |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the National Underground Asset Register (NUAR) — a secure digital platform providing a single view of underground pipes and cables to reduce accidental utility strikes during excavation works.

---

## Executive Summary

### Business Context

An estimated 60,000 utility strikes occur annually in the UK during excavation works, costing GBP 2.4 billion in direct costs (repairs, delays, emergency response) and causing service disruptions affecting millions of citizens. Three workers are killed each year. The root cause is fragmented, incomplete, and outdated underground asset information — before any excavation, contractors must separately contact each utility company, wait 5-10 working days for responses, and reconcile information received in different formats and accuracies.

NUAR will provide a single, secure digital platform where verified users can query underground asset locations before excavation, receiving a unified view of all known assets in the area within seconds rather than days.

### Objectives

- Provide a single, secure digital view of underground assets from all major UK utility owners
- Reduce utility strike incidents by 30% within 3 years of national rollout
- Reduce pre-excavation enquiry time from 5-10 working days to under 60 seconds
- Implement CNI-appropriate security controls assessed and approved by NCSC
- Comply with PAS 256 (Buried Asset Data Specification) for data interoperability

### Expected Outcomes

- 30% reduction in utility strikes (60,000 to 42,000 per year)
- GBP 720M annual cost saving across utility and construction sectors
- Zero fatalities from strikes where NUAR was consulted
- 90% user satisfaction for pre-excavation enquiry process

### Project Scope

**In Scope**:

- Underground asset data ingestion from gas, electricity, water, telecoms, and cable operators
- Secure, role-based access for verified excavation professionals
- Map-based spatial query interface for pre-excavation planning
- Mobile-responsive interface for on-site use
- PAS 256 compliant data model
- Asset data quality scoring and reporting
- NCSC-assessed security architecture
- Audit logging of all data access

**Out of Scope**:

- Above-ground infrastructure (pylons, substations, communications towers)
- Street furniture and highway assets (managed by local authorities separately)
- Private utility connections within property boundaries
- Real-time asset monitoring or IoT sensor integration (future phase)
- Automated excavation permit application

---

## Business Requirements

### BR-001: Comprehensive Underground Asset Database

**Description**: The platform must contain underground asset location data from all major UK utility asset owners covering 95% of UK buried infrastructure.

**Rationale**: The platform is only useful if it provides a comprehensive view. Missing a single gas main negates the safety benefit for that excavation.

**Success Criteria**:

- Data from all gas distribution networks (Cadent, SGN, NGN, WWU), all electricity DNOs, all water companies, and major telecoms operators
- 95% geographic coverage of UK
- Data freshness: updates from asset owners at least quarterly

**Priority**: MUST_HAVE

**Stakeholder**: Geospatial Commission, HSE

---

### BR-002: Secure Access with CNI Protection

**Description**: The platform must implement security controls meeting NCSC requirements for CNI-adjacent data, with verified user registration, role-based access, and comprehensive audit logging.

**Rationale**: Precise infrastructure location data could be used by hostile actors to plan physical attacks on gas, electricity, water, or telecoms networks. Security must balance rapid access for legitimate users with protection against misuse.

**Success Criteria**:

- NCSC security assessment passed
- User identity verified before access granted
- No bulk data extraction capability
- All access logged with who, what, when, where
- Zero data breaches

**Priority**: MUST_HAVE

**Stakeholder**: NCSC, Major Utilities, Geospatial Commission

---

### BR-003: Rapid Digital Pre-Excavation Enquiry

**Description**: The platform must enable verified users to query underground assets in a defined area and receive results within 60 seconds, available 24/7 on desktop and mobile devices.

**Rationale**: Current 5-10 working day plant enquiry process causes construction delays (GBP 500M/year estimated), encourages unsafe "dig and discover" behaviour, and is incompatible with emergency repair timescales.

**Success Criteria**:

- Query results in <60 seconds
- 24/7 availability (99.9%)
- Mobile-responsive for on-site tablet/smartphone use
- Results downloadable as PDF and GIS-compatible format

**Priority**: MUST_HAVE

**Stakeholder**: Construction Industry, Local Highway Authorities

---

## Functional Requirements

### User Personas

#### Persona 1: Construction Site Manager

- **Role**: Plans and manages excavation works
- **Goals**: Identify all underground assets before digging; comply with HSG47
- **Pain Points**: Waiting 5-10 days for plant enquiry responses; incomplete information; different formats from each utility
- **Technical Proficiency**: Low-Medium

#### Persona 2: Utility Asset Data Manager

- **Role**: Manages and submits underground asset data for their utility company
- **Goals**: Submit accurate, current data; maintain data quality; protect CNI-sensitive details
- **Pain Points**: Multiple data requests from different parties; legacy data quality issues; security concerns
- **Technical Proficiency**: High

#### Persona 3: Local Highway Authority Street Works Officer

- **Role**: Manages excavation permits and coordination on local roads
- **Goals**: Verify asset locations before issuing works permits; coordinate with utility companies
- **Pain Points**: Incomplete asset data; no single view; manual coordination
- **Technical Proficiency**: Medium

#### Persona 4: Emergency Repair Operative

- **Role**: Responds to emergency utility faults (gas leak, water main burst)
- **Goals**: Quickly identify other utilities in the area before emergency excavation
- **Pain Points**: No time for standard plant enquiry; must dig under time pressure; risk of secondary strikes
- **Technical Proficiency**: Low

---

### Functional Requirements Detail

#### FR-001: Asset Data Ingestion API

**Description**: The system must provide a secure API for utility asset owners to submit underground asset data in PAS 256 compliant format.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] API accepts asset data in PAS 256 GML and GeoJSON formats
- [ ] API supports full dataset replacement and incremental updates
- [ ] Data validation against PAS 256 schema before acceptance
- [ ] Detailed validation error reports returned for rejected submissions
- [ ] OAuth 2.0 authentication with utility-specific credentials
- [ ] Submission audit trail with timestamp and hash for integrity

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: Spatial Asset Query

**Description**: The system must enable users to query underground assets within a defined area (polygon, buffer around a point, or buffer around a line) and receive all known assets in that area.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Query by: point + radius, polygon drawing, line + buffer, postcode + radius
- [ ] Results show: asset type, owner, approximate depth, material, size/diameter, installation date (where known)
- [ ] Results displayed on map with OS base mapping
- [ ] Results colour-coded by asset type (gas=yellow, electricity=black, water=blue, telecoms=green, per NJUG colour coding)
- [ ] Tabular results alongside map for accessibility
- [ ] Query area limited to 500m x 500m to prevent bulk data extraction
- [ ] Response time <60 seconds for standard query

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-003: User Registration and Verification

**Description**: The system must verify user identity and legitimate purpose before granting access to underground asset data.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Registration requires: name, employer, role, purpose (excavation planning, highway management, utility, emergency services)
- [ ] Identity verification via government identity service or employer verification
- [ ] Employer verification: check against Companies House or utility/contractor register
- [ ] Approval within 24 hours for standard registration; immediate for pre-approved employers
- [ ] Annual re-verification of active accounts
- [ ] Account suspension for misuse

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-004: Asset Data Quality Scoring

**Description**: The system must assess and display data quality scores for each asset record, indicating confidence in positional accuracy, currency, and completeness.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Quality score based on: positional accuracy (surveyed vs estimated), age of record, completeness of attributes
- [ ] Quality score displayed alongside each asset on query results
- [ ] Traffic light indicator: Green (high confidence), Amber (moderate), Red (low confidence)
- [ ] Asset owner notified of low-quality records for improvement
- [ ] Aggregate quality dashboard per utility company

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-005: Mobile Field Application

**Description**: The system must provide a mobile-responsive interface optimised for on-site use on tablets and smartphones, including offline map caching.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Responsive design functional on 7-inch tablet and smartphone screens
- [ ] GPS-based location: "Show assets near me" using device GPS
- [ ] Offline map caching: download area map and asset data for offline use in areas without mobile signal
- [ ] Pinch-zoom and pan on map interface
- [ ] Usable with work gloves (large touch targets)
- [ ] Low-bandwidth mode: text-based results when connection is poor

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Comprehensive Audit Trail

**Description**: The system must log every data access event with sufficient detail for security investigation and regulatory compliance.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Log: user ID, query area (bounding box), asset types returned, timestamp, IP address, device type
- [ ] Logs immutable (write-once storage)
- [ ] Logs retained for minimum 2 years
- [ ] Anomaly detection: alert on unusual query patterns (volume, timing, geographic spread)
- [ ] Audit reports available to utility data owners showing access to their data

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-007: Discrepancy Reporting

**Description**: The system must allow users to report discrepancies between displayed asset data and actual conditions found during excavation.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] User can submit: "Asset found not on map" or "Asset on map not found" or "Asset location inaccurate"
- [ ] Photo upload capability for evidence
- [ ] GPS location captured automatically on mobile
- [ ] Reports routed to relevant asset owner for investigation
- [ ] Report status tracking (submitted, under investigation, resolved)

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Spatial Query Response Time

**Requirement**: Asset query for a 100m x 100m area must return results in <10 seconds (p95). Query for maximum area (500m x 500m) in <60 seconds (p95).

**Load Conditions**: 2,000 concurrent users during working hours (Mon-Sat 06:00-18:00)

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.9% availability during working hours (Mon-Sat 06:00-22:00). 99.5% outside working hours.

**Rationale**: Excavation primarily occurs during working hours. Emergency access required 24/7.

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: CNI Data Protection

**Requirement**: Security architecture assessed and approved by NCSC. Encryption at rest (AES-256) and in transit (TLS 1.3). Network segmentation isolating asset data from public internet. No bulk data extraction capability.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Access Controls

**Requirement**: Role-based access control: (1) Standard user — query by area, limited area size; (2) Highway authority — extended query area, permit integration; (3) Asset owner — manage own data, view access logs; (4) Administrator — user management, audit review.

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Anti-Aggregation Controls

**Requirement**: System must prevent users from systematically querying adjacent areas to reconstruct a complete network map. Rate limiting: maximum 20 queries per hour per user. Sequential adjacent queries flagged for review.

**Priority**: MUST_HAVE

---

### Geospatial Requirements

#### NFR-GEO-001: Coordinate Reference System

**Requirement**: Store data in OSGB36 (EPSG:27700). Serve data in both OSGB36 and WGS84. Use OSTN15 for transformations.

**Priority**: MUST_HAVE

---

#### NFR-GEO-002: Positional Accuracy

**Requirement**: Display positional accuracy per asset record. Minimum accuracy for inclusion: +/- 5m for surveyed assets, +/- 10m for estimated positions. Accuracy clearly labelled to users.

**Priority**: MUST_HAVE

---

#### NFR-GEO-003: PAS 256 Compliance

**Requirement**: Data model compliant with PAS 256:2022 (Buried asset information — Specification for data). All asset attributes aligned with PAS 256 vocabulary.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Ordnance Survey (Base Mapping)

**Purpose**: Authoritative base mapping for asset visualisation

**Integration Type**: Tile service (WMTS) + AddressBase Premium for address search

**Priority**: MUST_HAVE

---

### INT-002: LSBUD (Linesearch beforeUdig)

**Purpose**: Transition pathway — existing plant enquiry service data

**Integration Type**: Data migration + API integration during transition

**Priority**: SHOULD_HAVE

---

### INT-003: Street Manager (DfT)

**Purpose**: Link asset data to excavation permit applications

**Integration Type**: Real-time API

**Priority**: COULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Underground Asset

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| asset_id | UUID | Yes | Unique asset identifier | Primary key |
| owner_id | UUID | Yes | Asset owner (utility company) | FK to owner |
| asset_type | Enum | Yes | Type of utility | Gas, Electricity, Water, Sewage, Telecoms, Cable |
| geometry | LineString/Point | Yes | Asset geometry (route or point) | OSGB36 |
| depth_m | Decimal | No | Approximate depth in metres | > 0 |
| diameter_mm | Integer | No | Pipe/cable diameter | > 0 |
| material | String | No | Construction material | |
| voltage_kv | Decimal | No | For electricity cables | > 0 |
| pressure_bar | Decimal | No | For gas pipes | > 0 |
| install_date | Date | No | Installation date | |
| accuracy_m | Decimal | Yes | Positional accuracy in metres | > 0 |
| source_type | Enum | Yes | How position was determined | Surveyed, Estimated, Historical |
| last_verified | Date | No | Date position last verified | |

**Data Volume**: Estimated 500 million asset segments nationally

**Data Classification**: OFFICIAL-SENSITIVE — CNI

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Year 1-2) | GBP 6.0M | 20 FTE delivery team |
| Security architecture and NCSC assessment | GBP 1.5M | CNI-grade security |
| Infrastructure (Year 1-3) | GBP 2.0M | Secure cloud hosting |
| OS data licensing | GBP 0.5M | Base mapping, AddressBase |
| Data migration and onboarding | GBP 1.0M | Utility company data ingestion |
| Contingency (15%) | GBP 1.7M | |
| **Total** | **GBP 12.7M** | Over 3 years |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Secure cloud infrastructure | GBP 1.0M | CNI-grade hosting |
| BAU team | GBP 1.2M | 7 FTE including security ops |
| OS licensing | GBP 0.2M | Annual renewal |
| NCSC annual assessment | GBP 0.1M | Ongoing compliance |
| **Total** | **GBP 2.5M/year** | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-004-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | `projects/004-national-underground-asset-register/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |
| PAS 256:2022 | Standard | BSI | Buried asset data specification | N/A — external reference |
| HSG47 | Guidance | HSE | Avoiding danger from underground services | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Underground Asset Register (Project 004)
**Model**: Claude Opus 4.6
