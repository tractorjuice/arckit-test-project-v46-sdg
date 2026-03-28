# Project Requirements: Digital Infrastructure Mapping

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Digital Infrastructure Mapping (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Digital Infrastructure Mapping Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Digital Infrastructure Programme Board, DSIT Digital, Ofcom, BDUK |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Digital Infrastructure Mapping platform — a national broadband and 5G coverage mapping service that provides authoritative, premises-level coverage data to inform public investment, regulatory oversight, and citizen information.

---

## Executive Summary

### Business Context

The UK Government has committed GBP 5 billion through Project Gigabit to deliver gigabit-capable broadband to hard-to-reach areas. Accurate, current, premises-level coverage data is essential to ensure this investment reaches genuinely unserved premises. Currently, coverage data is fragmented across individual operators, Ofcom's annual Connected Nations report, and various commercial data providers — none of which provides a single, authoritative, regularly updated national picture at premises level.

The Digital Infrastructure Mapping platform will aggregate coverage data from all major fixed and mobile operators, integrate with Ordnance Survey addressing data for UPRN-level accuracy, and provide tiered access to coverage information for government (investment targeting), regulators (compliance monitoring), local authorities (planning), and citizens (coverage checking).

### Objectives

- Establish a single, authoritative, UPRN-level national broadband and mobile coverage database
- Integrate with BDUK procurement systems to automate Project Gigabit investment targeting
- Provide Ofcom with continuous coverage monitoring capability beyond annual Connected Nations reporting
- Deliver a citizen-facing coverage checker on GOV.UK
- Publish open data on aggregate coverage statistics via data.gov.uk

### Expected Outcomes

- GBP 200-400M savings through elimination of Project Gigabit subsidy errors
- Reduction in coverage data reconciliation time from 12 weeks to 2 weeks per BDUK procurement area
- 1 million citizen coverage lookups per month within 6 months of public launch
- Quarterly regulatory coverage reporting (vs annual)

### Project Scope

**In Scope**:

- Fixed broadband coverage (FTTC, FTTP, cable, FWA) at UPRN level
- Mobile coverage (4G, 5G) at 100m grid resolution
- Operator data submission API and portal
- BDUK investment targeting integration
- Ofcom regulatory reporting interface
- Citizen-facing coverage checker (GOV.UK)
- Open data publication on data.gov.uk
- Crowdsourced coverage verification mechanism

**Out of Scope**:

- Satellite broadband coverage mapping (future phase)
- Community network and small ISP coverage (future phase)
- Network quality metrics (latency, jitter, packet loss) — coverage only
- Commercial broadband comparison / switching functionality
- Devolved administration broadband programme management tools (Scotland R100, Wales)

---

## Business Requirements

### BR-001: National Coverage Database

**Description**: The platform must provide a single, authoritative database of broadband and mobile coverage across all UK premises, aggregating data from all operators with >1% market share.

**Rationale**: Fragmented coverage data leads to subsidy errors (GBP 200-400M risk), incomplete regulatory reporting, and uninformed citizen decisions.

**Success Criteria**:

- Coverage data available for >98% of UK residential and business premises
- Data from all operators with >1% market share ingested and reconciled
- Coverage records updated at least monthly

**Priority**: MUST_HAVE

**Stakeholder**: DSIT Secretary of State, BDUK Director

---

### BR-002: Investment Targeting Accuracy

**Description**: The platform must enable BDUK to accurately classify premises as served, underserved, or unserved for Project Gigabit procurement area definition, with an error rate below 2%.

**Rationale**: Over-build wastes public money; under-build leaves citizens without connectivity. Current 5-8% error rate is unacceptable for a GBP 5 billion programme.

**Success Criteria**:

- Premises classification accuracy >98% (validated by post-contract audit)
- Procurement area definition time reduced from 12 weeks to 2 weeks
- Automated integration with BDUK procurement management system

**Priority**: MUST_HAVE

**Stakeholder**: BDUK Director, HM Treasury

---

### BR-003: Regulatory Compliance Monitoring

**Description**: The platform must enable Ofcom to monitor operator compliance with coverage obligations (USO, spectrum licence conditions, voluntary commitments) on a continuous basis rather than annually.

**Rationale**: Annual reporting creates a 6-12 month lag in identifying coverage obligation breaches. Continuous monitoring enables proactive regulatory intervention.

**Success Criteria**:

- Connected Nations report production time reduced from 6 months to 2 months
- Quarterly interim coverage reports enabled
- Operator-specific obligation tracking dashboards available

**Priority**: SHOULD_HAVE

**Stakeholder**: Ofcom

---

### BR-004: Citizen Coverage Information

**Description**: The platform must provide citizens with an accessible, authoritative way to check broadband and mobile coverage at their address.

**Rationale**: Citizens cannot make informed broadband purchasing decisions without accurate coverage information. Operator marketing claims ("up to" speeds) are misleading.

**Success Criteria**:

- Coverage checker live on GOV.UK
- 1 million lookups per month within 6 months
- User satisfaction >4.0/5.0
- WCAG 2.2 Level AA compliance

**Priority**: SHOULD_HAVE

**Stakeholder**: Citizens, DSIT Secretary of State

---

### BR-005: Open Data Publication

**Description**: The platform must publish aggregate coverage statistics as open data on data.gov.uk, supporting third-party analysis and academic research.

**Rationale**: INSPIRE Regulations and the UK Open Data Strategy require publication of government-held geographic data. Coverage data is a nationally significant geospatial dataset.

**Success Criteria**:

- Aggregate coverage statistics published quarterly on data.gov.uk
- INSPIRE-compliant metadata published
- API access for bulk data consumers

**Priority**: SHOULD_HAVE

**Stakeholder**: Geospatial Commission, Open Data Institute

---

## Functional Requirements

### User Personas

#### Persona 1: BDUK Procurement Manager

- **Role**: Defines procurement areas for Project Gigabit contracts
- **Goals**: Accurately identify unserved and underserved premises for each procurement area
- **Pain Points**: Manual data reconciliation from multiple operator sources; outdated data; postcode-level rather than premises-level data
- **Technical Proficiency**: Medium

#### Persona 2: Ofcom Analyst

- **Role**: Monitors operator coverage obligations and produces Connected Nations reports
- **Goals**: Access current, operator-specific coverage data with analytical tools for trend analysis
- **Pain Points**: Annual data collection cycle; inconsistent data formats across operators; limited independent verification
- **Technical Proficiency**: High

#### Persona 3: Local Authority Digital Officer

- **Role**: Develops local digital inclusion strategy and processes telecoms planning applications
- **Goals**: Understand coverage levels in their area by technology and speed tier
- **Pain Points**: Fragmented data sources; no GIS-compatible coverage data; no API access
- **Technical Proficiency**: Medium

#### Persona 4: Citizen

- **Role**: Checking broadband and mobile coverage at their address
- **Goals**: Understand what broadband speeds and mobile coverage are actually available
- **Pain Points**: Misleading operator "up to" speed claims; no single source of truth; technical jargon
- **Technical Proficiency**: Low

#### Persona 5: Telecoms Operator Data Manager

- **Role**: Submits coverage data on behalf of their operator
- **Goals**: Meet regulatory submission requirements with minimum effort; ensure commercially sensitive data is protected
- **Pain Points**: Multiple different data requests from DSIT, Ofcom, BDUK, local authorities; inconsistent formats
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: Operator Data Submission API

**Description**: The system must provide a secure API for telecoms operators to submit coverage data in a standardised format, supporting both incremental updates and full dataset replacement.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] API accepts coverage data in GeoJSON and GeoPackage formats
- [ ] API supports incremental updates (delta submissions) and full dataset replacement
- [ ] API validates data against the defined coverage data schema before acceptance
- [ ] API returns detailed validation error reports for rejected submissions
- [ ] API enforces authentication via OAuth 2.0 with operator-specific credentials
- [ ] API supports submissions up to 10GB per upload (compressed)

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: UPRN-Level Coverage Matching

**Description**: The system must match operator coverage data to individual premises using Ordnance Survey AddressBase Premium UPRNs, providing premises-level coverage status for every residential and commercial address.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Coverage data matched to UPRN using spatial intersection and address matching
- [ ] Match rate >95% for residential premises, >90% for commercial premises
- [ ] Unmatched records flagged for manual review
- [ ] Coverage status per UPRN includes: technology type, maximum speed, operator, date last verified

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-003: Multi-Operator Coverage Reconciliation

**Description**: The system must reconcile coverage data from multiple operators to produce a single, deduplicated, premises-level view showing all available services per UPRN.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Multiple operator records per UPRN reconciled into unified coverage record
- [ ] Conflicting data flagged (e.g., operator claims coverage but crowdsourced data contradicts)
- [ ] "Best available" coverage calculated per premises across all operators
- [ ] Historical coverage data retained for trend analysis

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-004: BDUK Procurement Area Analysis Tool

**Description**: The system must provide BDUK users with tools to define procurement areas, classify premises as served/underserved/unserved based on coverage thresholds, and export premises lists for procurement.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Users can define procurement area boundaries (polygon drawing, postcode selection, local authority boundary)
- [ ] System classifies premises within the area using configurable speed thresholds
- [ ] Classification results exportable as CSV with UPRN, address, coverage status, and operator
- [ ] Integration with BDUK procurement management system via API
- [ ] Audit trail of all procurement area definitions and classifications

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-005: Citizen Coverage Checker

**Description**: The system must provide a public-facing, GOV.UK-hosted service where citizens can look up broadband and mobile coverage at their address or postcode.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Address lookup using postcode + house number/name
- [ ] Results show: broadband technologies available, estimated speed range, mobile coverage (4G/5G)
- [ ] Results presented in plain language (avoid technical jargon)
- [ ] Progressive disclosure: simple summary view + detailed technical view
- [ ] Coverage discrepancy reporting: citizen can report "this doesn't match my experience"
- [ ] WCAG 2.2 Level AA compliant
- [ ] Loads in <2 seconds on 3G connection

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Ofcom Regulatory Reporting Dashboard

**Description**: The system must provide Ofcom with analytical dashboards and data export capabilities for regulatory reporting, including operator-specific coverage obligation monitoring.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Dashboard shows national, regional, and local authority level coverage statistics
- [ ] Operator-specific coverage views with obligation compliance tracking
- [ ] Trend analysis: coverage change over time by technology, speed tier, geography
- [ ] Export data in formats compatible with Ofcom analytical tools (CSV, Excel, SAS)
- [ ] Scheduled report generation for Connected Nations data requirements

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-007: Map Visualisation

**Description**: The system must provide interactive map-based visualisation of coverage data at multiple scales (national overview, regional, local, premises-level).

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] Map displays coverage using Ordnance Survey base mapping
- [ ] Choropleth view: coverage percentage by local authority, ward, LSOA
- [ ] Premises-level view: individual premises colour-coded by coverage status
- [ ] Filter by technology (FTTC, FTTP, cable, FWA, 4G, 5G), speed tier, and operator
- [ ] Non-visual alternative available (tabular data, screen-reader-accessible summary)

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-008: Crowdsourced Coverage Verification

**Description**: The system must accept and process citizen-submitted coverage reports to identify discrepancies between operator-claimed coverage and actual user experience.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] Citizens can submit a coverage report (address, claimed service, actual experience)
- [ ] Reports aggregated and analysed for patterns indicating systematic operator over-reporting
- [ ] Reports visible to Ofcom analysts as a verification layer
- [ ] Automated spam/abuse detection on submissions
- [ ] Privacy: no personal data retained beyond what is necessary for the report

**Priority**: COULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Spatial Query Response Time

**Requirement**: Coverage lookup for a single UPRN must return results in <500ms (p95). Map tile requests must return in <300ms (p95).

**Load Conditions**: 500 concurrent users for internal tools; 5,000 concurrent users for citizen checker during peak (e.g., media coverage event)

**Priority**: MUST_HAVE

---

#### NFR-P-002: Data Ingestion Throughput

**Requirement**: The system must process a full national coverage dataset from a major operator (up to 30 million premises records) within 4 hours, including UPRN matching and reconciliation.

**Priority**: MUST_HAVE

---

### Availability and Resilience Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.9% availability for citizen-facing service; 99.5% for internal tools. Maximum planned downtime: 4 hours per month during off-peak.

**Priority**: MUST_HAVE

---

#### NFR-A-002: Disaster Recovery

**RPO**: 1 hour | **RTO**: 4 hours

**Backup Requirements**: Daily full backup, hourly incremental. Geographic backup: separate UK data centre.

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Tiered Access Control

**Requirement**: The system must implement role-based access control with three tiers: (1) Public — aggregate coverage data, citizen checker; (2) Regulatory — operator-specific data for Ofcom and BDUK under statutory authority; (3) Operator — own-data management and submission.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Data Encryption

**Requirement**: All data encrypted at rest (AES-256) and in transit (TLS 1.3). Operator-specific coverage data encrypted with operator-specific keys for additional isolation.

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Audit Logging

**Requirement**: All access to operator-specific coverage data logged with who, what, when, where, and why. Logs immutable and retained for 2 years minimum.

**Priority**: MUST_HAVE

---

### Geospatial Requirements

#### NFR-GEO-001: Coordinate Reference Systems

**Requirement**: System must store and serve data in OSGB36 (EPSG:27700) for UK-domestic use and WGS84 (EPSG:4326) for web mapping. Coordinate transformations must use OSTN15 for accuracy.

**Priority**: MUST_HAVE

---

#### NFR-GEO-002: Spatial Accuracy

**Requirement**: Fixed broadband coverage matched to UPRN with positional accuracy of the AddressBase Premium source (+/- 1m urban, +/- 10m rural). Mobile coverage at 100m grid resolution.

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-001: INSPIRE Compliance

**Requirement**: All published spatial datasets must comply with INSPIRE metadata regulations, including metadata publication in UK INSPIRE discovery service.

**Priority**: MUST_HAVE

---

#### NFR-C-002: UK GDPR Compliance

**Requirement**: Crowdsourced coverage reports must comply with UK GDPR data minimisation. No personal data retained beyond report processing. Privacy notice published. DPIA completed.

**Priority**: MUST_HAVE

---

#### NFR-C-003: FOIA and EIR Preparedness

**Requirement**: Data classification and access tiers designed to support section 43 (commercial interests) exemption for operator-specific data. Environmental Information Regulations (EIR) response procedures documented.

**Priority**: SHOULD_HAVE

---

### Usability Requirements

#### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all interfaces. Non-visual alternatives for all map-based content. Service usable on screen readers.

**Priority**: MUST_HAVE

---

#### NFR-U-002: GDS Design System

**Requirement**: Citizen-facing interfaces must use GOV.UK Design System components and patterns. Service must pass GDS service assessment.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Ordnance Survey AddressBase Premium

**Purpose**: Authoritative premises addressing and UPRNs for coverage matching

**Integration Type**: Batch file transfer (6-weekly update cycle) + COU (Change-Only Update) daily

**Data Exchanged**: UPRN, address, coordinates, classification (residential/commercial)

**Authentication**: OS Data Hub API key

**Priority**: MUST_HAVE

---

### INT-002: Ofcom Connected Nations Data

**Purpose**: Baseline coverage data and operator submission validation

**Integration Type**: Batch file transfer (annual + ad-hoc)

**Data Exchanged**: Operator coverage predictions, speed test data, methodology documentation

**Authentication**: Secure file transfer with Ofcom credentials

**Priority**: MUST_HAVE

---

### INT-003: BDUK Procurement Management System

**Purpose**: Automated premises classification for procurement area definition

**Integration Type**: Real-time API (REST)

**Data Exchanged**: Procurement area boundary, premises list with coverage classification, status updates

**Authentication**: OAuth 2.0 with government identity

**Priority**: MUST_HAVE

---

### INT-004: data.gov.uk

**Purpose**: Open data publication of aggregate coverage statistics

**Integration Type**: Batch file transfer (quarterly publication)

**Data Exchanged**: Aggregate coverage CSV, DCAT metadata, INSPIRE metadata

**Authentication**: data.gov.uk publisher credentials

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Premises Coverage Record

**Description**: Coverage status for an individual premises (UPRN)

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| uprn | BigInt | Yes | Unique Property Reference Number | OS AddressBase FK |
| operator_id | UUID | Yes | Submitting operator | FK to operator |
| technology | Enum | Yes | Coverage technology | FTTC, FTTP, Cable, FWA, 4G, 5G |
| max_download_speed | Integer | Yes | Maximum download Mbps | > 0 |
| max_upload_speed | Integer | Yes | Maximum upload Mbps | > 0 |
| coverage_status | Enum | Yes | Status | Available, Planned, Under_Review |
| planned_date | Date | No | Expected availability date | Future date if Planned |
| last_verified | Timestamp | Yes | When coverage was last verified | Indexed |
| submission_date | Timestamp | Yes | When data was submitted | Indexed |

**Data Volume**: ~150 million records (30M premises x 5 operators average)

**Data Classification**: OFFICIAL-SENSITIVE — Commercial (operator-specific), OFFICIAL (aggregated)

---

### Data Quality Requirements

**Data Accuracy**: UPRN match rate >95% for residential, >90% for commercial. Speed data validated against known technology capabilities.

**Data Completeness**: No null values in required fields. Coverage status required for every submitted UPRN.

**Data Timeliness**: Operator submissions at least monthly. Data freshness dashboard visible to Ofcom.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with Ordnance Survey AddressBase Premium under existing government licence terms

**TC-2**: Must deploy on UK sovereign cloud infrastructure (Crown Hosting or equivalent)

**TC-3**: Citizen-facing service must be hosted on GOV.UK infrastructure (or subdomain)

### Business Constraints

**BC-1**: Budget cap of GBP 15 million for platform development over 3 years

**BC-2**: Must achieve GDS service assessment pass at Alpha and Beta stages

**BC-3**: Operator data submission format must be agreed with Ofcom to avoid conflicting requirements

### Assumptions

**A-1**: Ofcom will exercise regulatory power to compel operator data submission if voluntary participation is insufficient

**A-2**: Ordnance Survey AddressBase Premium will continue to be available to government under current licensing terms

**A-3**: BDUK procurement management system has a documented API for integration

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Project Gigabit subsidy accuracy | 92-95% | >98% | Year 2 | Post-contract audit |
| Procurement area definition time | 12 weeks | 2 weeks | Year 1 | BDUK process tracking |
| Citizen coverage lookups | 0 | 1M/month | 6 months post-launch | GOV.UK analytics |
| Operator data submission frequency | Annual | Monthly | Year 1 | Submission monitoring |
| Connected Nations production time | 6 months | 2 months | Year 2 | Ofcom reporting timeline |

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Year 1-2) | GBP 8.0M | 25 FTE delivery team |
| Infrastructure (Year 1-3) | GBP 2.5M | Cloud hosting, OS licensing |
| Ordnance Survey data licensing | GBP 1.0M | AddressBase Premium 3-year licence |
| Security assessment and pen testing | GBP 0.5M | NCSC assessment, annual pen tests |
| GDS service assessment and support | GBP 0.3M | Assessment preparation, user research |
| Contingency (15%) | GBP 1.8M | |
| **Total** | **GBP 14.1M** | Over 3 years |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Cloud infrastructure | GBP 1.2M | Including spatial database, CDN |
| OS data licensing | GBP 0.3M | Annual licence renewal |
| Support and maintenance team | GBP 1.5M | 8 FTE BAU team |
| Security monitoring | GBP 0.2M | SOC, vulnerability scanning |
| **Total** | **GBP 3.2M/year** | |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| BDUK Director | Investment targeting | [ ] Approved | PENDING | |
| Ofcom | Regulatory requirements | [ ] Approved | PENDING | |
| DSIT CDO | Technical architecture | [ ] Approved | PENDING | |
| DSIT SIRO | Information risk | [ ] Approved | PENDING | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | `projects/001-digital-infrastructure-mapping/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Infrastructure Mapping (Project 001)
**Model**: Claude Opus 4.6
