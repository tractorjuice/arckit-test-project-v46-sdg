# Project Requirements: Biodiversity Net Gain Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Biodiversity Net Gain Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, BNG Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | BNG Programme Board, DEFRA Digital, Natural England, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive requirements for the Biodiversity Net Gain Platform — the digital service enabling developers, Local Planning Authorities, habitat banks, and Natural England to manage the mandatory 10% biodiversity net gain obligation under the Environment Act 2021.

---

## Executive Summary

### Business Context

The Environment Act 2021 made biodiversity net gain (BNG) mandatory for most planning permissions in England. Developers must demonstrate a minimum 10% net gain in biodiversity value, measured using Natural England's Biodiversity Metric 4.0. The gain can be delivered on-site, off-site (through habitat banks), or through purchasing statutory credits from DEFRA. A national digital platform is required to manage the BNG credit registry, facilitate metric calculations, enable credit trading, and provide Local Planning Authorities with compliance verification tools.

Without this platform, BNG compliance relies on manual spreadsheet-based metric calculations, paper-based credit registration, and ad hoc arrangements between developers and habitat providers — creating inconsistency, fraud risk, and planning delays that threaten both environmental outcomes and housebuilding targets.

### Objectives

- Deliver a national BNG credit registry that prevents double-counting and fraud
- Implement the Biodiversity Metric 4.0 as a transparent, auditable digital calculation engine
- Create a credit marketplace connecting developers with habitat banks and statutory credits
- Enable LPAs to verify BNG compliance within standard planning determination timescales
- Establish 30-year habitat management tracking with financial security requirements

### Expected Outcomes

- Zero planning delays attributable to BNG compliance within 12 months of launch
- National biodiversity credit market valued at estimated £130M annually within 3 years
- 100% of BNG obligations registered with auditable metric calculations
- Measurable national net positive biodiversity outcome demonstrated within 5 years

### Project Scope

**In Scope**:

- Biodiversity Metric 4.0 calculation engine with full audit trail
- National biodiversity credit registry (on-site gains, off-site credits, statutory credits)
- Credit marketplace (search, purchase, registration)
- LPA compliance verification portal and API
- 30-year habitat management plan tracking and monitoring
- Developer application portal for BNG plans
- Natural England credit validation workflow
- Reporting and analytics dashboard

**Out of Scope**:

- Marine net gain (future Environment Act provision, not yet commenced)
- Habitat condition monitoring hardware (sensors, drones) — data consumed only
- Local authority planning application management systems (integration only)
- Ecological consultancy services — platform facilitates, does not replace, professional assessment
- Welsh and Scottish equivalents (England only for this phase)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | DEFRA | Decision maker |
| BNG Service Owner | Service accountability | DEFRA Digital | Service design, user outcomes |
| NE Chief Scientist | Scientific authority | Natural England | Metric validation |
| BNG Policy Lead | Policy intent | DEFRA | Requirements definition |
| LPA Planning Officers | End users | Local Authorities | User acceptance |
| Developers | End users | Private sector | Requirements input |
| Habitat bank operators | End users | Private sector | Marketplace design |
| Enterprise Architect | Technical oversight | DEFRA Digital | Architecture compliance |
| Security Lead | Security review | DEFRA / NCA | Security requirements |
| CDDO Assessor | Standards assurance | Cabinet Office | GDS compliance |

---

## Business Requirements

### BR-1: National Biodiversity Credit Registry

**Description**: Establish a single, authoritative national registry of all biodiversity credits — on-site gains, off-site credits, and statutory credits — that prevents double-counting, enables transparent tracking, and provides the legal record of BNG obligations.

**Rationale**: The Environment Act 2021 requires a register of biodiversity gain sites. Without a robust digital registry, credits could be counted against multiple developments, undermining the environmental purpose of BNG and creating significant fraud risk in what will become a multi-million pound market.

**Success Criteria**:

- Zero instances of double-counted credits
- 100% of registered credits traceable to verified habitat sites with geospatial boundaries
- Registry available as public record (appropriately anonymised)

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Secretary of State, Natural England

---

### BR-2: Biodiversity Metric 4.0 Calculation Engine

**Description**: Implement the Biodiversity Metric 4.0 as a digital calculation engine that produces transparent, auditable, and independently verifiable results for habitat baseline and post-development assessments.

**Rationale**: The Biodiversity Metric 4.0 is the legally mandated tool for measuring biodiversity value. Its digital implementation must be scientifically accurate, fully transparent (showing all inputs, weightings, and intermediate calculations), and configurable to accommodate future metric versions without major re-engineering.

**Success Criteria**:

- Calculations match reference implementation to within 0.01 biodiversity units
- Full audit trail of all inputs, parameters, and intermediate results
- Qualified ecologist can verify any calculation within 30 minutes

**Priority**: MUST_HAVE

**Stakeholder**: Natural England Chief Scientist

---

### BR-3: Credit Marketplace

**Description**: Create a functioning marketplace that enables developers to search for, compare, and purchase biodiversity credits from habitat banks and statutory providers, with transparent pricing and availability information.

**Rationale**: Developers need a reliable mechanism to discharge BNG obligations when on-site delivery is not feasible. A transparent marketplace ensures competitive pricing, adequate supply, and efficient matching of development needs to habitat provision.

**Success Criteria**:

- Credits searchable by location, habitat type, and price
- Average time from credit search to confirmed purchase < 5 working days
- Market data published (aggregate pricing trends, supply/demand indicators)

**Priority**: MUST_HAVE

**Stakeholder**: Housing developers, Habitat banks

---

### BR-4: LPA Compliance Verification

**Description**: Enable Local Planning Authorities to verify BNG compliance for planning applications efficiently, using automated checks against the credit registry and metric calculations, without requiring specialist ecological expertise.

**Rationale**: LPAs are responsible for enforcing BNG conditions but most lack in-house ecologists. Without automated verification tools, BNG compliance checking will create an unfunded mandate that delays planning decisions and burdens already-stretched local authority resources.

**Success Criteria**:

- 90% of compliance checks completed within 2 working days
- No specialist ecological expertise required for standard verifications
- Integration available for at least 3 major planning management systems

**Priority**: MUST_HAVE

**Stakeholder**: Local Planning Authorities

---

### BR-5: 30-Year Habitat Management Accountability

**Description**: Establish digital tracking and enforcement mechanisms for the 30-year habitat management obligations attached to BNG credits, including management plan monitoring, compliance reporting, and financial security requirements.

**Rationale**: The 30-year management obligation is what ensures BNG delivers lasting biodiversity gain. Without systematic tracking, management plans will lapse and habitats will deteriorate — undermining the entire policy.

**Success Criteria**:

- 100% of registered obligations have active management plans and financial security
- Automated monitoring reminders at prescribed intervals
- Annual compliance reporting rate > 95%

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Policy, Conservation charities

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — Planning Officer (LPA)

- **Role**: Senior Planning Officer at a district council
- **Goals**: Verify BNG compliance quickly within planning determination timescales
- **Pain Points**: No ecological expertise, time pressure, fear of legal challenge
- **Technical Proficiency**: Medium

#### Persona 2: James — Development Manager (Housebuilder)

- **Role**: Planning Manager at a national housebuilder
- **Goals**: Achieve BNG compliance efficiently with predictable costs
- **Pain Points**: Uncertain credit availability, complex metric, planning delays
- **Technical Proficiency**: Medium

#### Persona 3: Dr. Emily — Ecologist (Habitat Bank)

- **Role**: Senior Ecologist managing a habitat bank portfolio
- **Goals**: Register habitats, create credits, sell to developers
- **Pain Points**: Slow validation, unclear pricing, 30-year financial exposure
- **Technical Proficiency**: High

#### Persona 4: Tom — Natural England Validator

- **Role**: NE Biodiversity Net Gain Validation Officer
- **Goals**: Validate credit applications accurately and efficiently
- **Pain Points**: High volume, complex assessments, inconsistent data quality
- **Technical Proficiency**: High

---

### Use Cases

#### UC-1: Developer Submits BNG Plan

**Actor**: James (Development Manager)

**Preconditions**:

- Planning application submitted or in preparation
- Ecological survey completed with Biodiversity Metric 4.0 assessment

**Main Flow**:

1. Developer logs in via GOV.UK One Login
2. System displays BNG plan creation form
3. Developer enters development site details (location, size, planning reference)
4. Developer uploads baseline habitat assessment data (or enters via guided form)
5. System runs Biodiversity Metric 4.0 calculation on baseline
6. Developer enters post-development habitat plans
7. System calculates net change and displays deficit/surplus
8. If deficit: System displays credit options (on-site improvement, off-site credits, statutory credits)
9. Developer selects credit approach and submits BNG plan
10. System generates BNG plan reference and sends confirmation

**Postconditions**:

- BNG plan registered in system with unique reference
- Metric calculation stored with full audit trail
- LPA notified of BNG plan submission

**Priority**: CRITICAL

---

#### UC-2: LPA Verifies BNG Compliance

**Actor**: Sarah (Planning Officer)

**Preconditions**:

- BNG plan submitted by developer
- Planning application under determination

**Main Flow**:

1. Planning officer accesses BNG verification portal (or planning system integration)
2. System displays BNG plan summary for the planning application
3. System shows automated compliance checks (metric calculation valid, credits available/registered, management plan in place)
4. System provides compliance recommendation (COMPLIANT / REQUIRES REVIEW / NON-COMPLIANT)
5. Planning officer reviews recommendation and supporting evidence
6. Planning officer records BNG condition decision

**Priority**: CRITICAL

---

#### UC-3: Habitat Bank Registers Credits

**Actor**: Dr. Emily (Ecologist)

**Preconditions**:

- Habitat creation site identified with baseline survey completed
- Habitat management plan prepared for 30-year period

**Main Flow**:

1. Habitat bank operator registers site with geospatial boundary
2. System validates site against environmental constraints (SSSI, ancient woodland proximity)
3. Operator uploads baseline habitat assessment and proposed enhancement plan
4. System runs Biodiversity Metric 4.0 calculation for projected gains
5. Operator submits credit creation application with management plan and financial security evidence
6. Natural England validates application
7. System registers credits in national registry with status "available for sale"

**Priority**: CRITICAL

---

### Functional Requirements Detail

#### FR-1: Biodiversity Metric 4.0 Calculation Engine

**Description**: The system must implement the complete Biodiversity Metric 4.0 calculation, including all habitat types, condition assessments, distinctiveness scores, strategic significance multipliers, temporal multipliers, and spatial risk multipliers.

**Relates To**: BR-2, UC-1, UC-3

**Acceptance Criteria**:

- [ ] Given a habitat baseline with known inputs, when calculation is run, then results match NE reference implementation to within 0.01 biodiversity units
- [ ] Given any completed calculation, when audit trail is requested, then all inputs, parameters, weightings, and intermediate results are displayed
- [ ] Given a metric version update, when new parameters are loaded, then existing calculations retain their original version parameters

**Data Requirements**:

- **Inputs**: Habitat type, area (hectares), condition, distinctiveness, strategic significance, location
- **Outputs**: Biodiversity units (baseline), biodiversity units (post-development), net change, percentage change
- **Validations**: Habitat type must be from approved classification list, area must be positive, condition must be valid for habitat type

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Natural England metric parameter data, habitat classification reference data

---

#### FR-2: Credit Registry

**Description**: The system must maintain a national registry of all biodiversity credits with unique identifiers, geospatial boundaries, ownership, status, and complete transaction history.

**Relates To**: BR-1, UC-3

**Acceptance Criteria**:

- [ ] Given a credit registration, when the credit is stored, then it receives a unique national identifier
- [ ] Given a credit, when it is allocated to a development, then it cannot be allocated to any other development (double-counting prevention)
- [ ] Given a credit, when its status changes, then the change is recorded with timestamp, actor, and reason

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Credit Search and Marketplace

**Description**: The system must enable developers to search for available credits by location (proximity to development), habitat type, price, and provider, with filtering and comparison capabilities.

**Relates To**: BR-3, UC-1

**Acceptance Criteria**:

- [ ] Given a development location, when search is performed, then available credits are returned sorted by proximity with distance displayed
- [ ] Given search results, when developer compares credits, then habitat type, unit price, provider, and management plan summary are shown
- [ ] Given a credit selection, when purchase is initiated, then the credit is temporarily reserved for 10 working days

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-4: LPA Compliance Verification API

**Description**: The system must provide an API and web portal for LPAs to verify BNG compliance for planning applications, with automated validation and clear compliance recommendations.

**Relates To**: BR-4, UC-2

**Acceptance Criteria**:

- [ ] Given a planning application reference, when compliance check is requested, then BNG plan status, metric calculation validity, and credit registration status are returned
- [ ] Given a compliant BNG plan, when automated checks pass, then system recommends "COMPLIANT" with supporting evidence
- [ ] Given a non-compliant plan, when issues are found, then system specifies exactly what is missing or invalid

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: LPA planning system API specifications (Idox, Uniform, NEC)

---

#### FR-5: 30-Year Management Plan Tracker

**Description**: The system must track habitat management obligations over their 30-year lifecycle, including scheduled management activities, monitoring requirements, compliance reporting, and financial security.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given a registered obligation, when a management milestone is due, then automated reminders are sent 30 days in advance
- [ ] Given a management obligation, when annual compliance report is due, then reporting template is issued and submission tracked
- [ ] Given a financial security expiry, when 6 months remain, then alert is raised to responsible authority

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-6: GOV.UK One Login Integration

**Description**: The system must authenticate users via GOV.UK One Login, with role-based access control differentiating between developers, LPA officers, habitat bank operators, Natural England validators, and public viewers.

**Relates To**: All use cases

**Acceptance Criteria**:

- [ ] Given a new user, when they access the platform, then they authenticate via GOV.UK One Login
- [ ] Given an authenticated user, when their role is determined, then appropriate permissions are applied
- [ ] Given a public viewer, when they access the registry, then they see anonymised credit data without authentication

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-7: Geospatial Site Mapping

**Description**: The system must enable users to define development sites and habitat sites using interactive maps, with integration to Ordnance Survey MasterMap, land registry boundaries, and environmental designation layers.

**Relates To**: UC-1, UC-3

**Acceptance Criteria**:

- [ ] Given a site location, when boundary is drawn on map, then area is calculated in hectares
- [ ] Given a site boundary, when submitted, then system overlays SSSI, ancient woodland, and priority habitat designations
- [ ] Given overlapping designations, when identified, then user is notified of additional requirements

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-8: Natural England Validation Workflow

**Description**: The system must provide Natural England with a structured workflow for validating habitat bank credit applications, with assessment tools, decision recording, and applicant communication.

**Relates To**: UC-3

**Acceptance Criteria**:

- [ ] Given a credit application, when assigned to validator, then assessment checklist is generated with all required verification points
- [ ] Given a validation decision, when recorded, then applicant is automatically notified with decision and any conditions
- [ ] Given a queue of applications, when prioritised, then system sorts by age, complexity, and strategic significance

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**: Platform must meet response time targets for interactive operations:

- Web page load time: < 2 seconds (95th percentile)
- Biodiversity Metric calculation: < 5 seconds for single site (95th percentile)
- Credit search results: < 3 seconds (95th percentile)
- API response time (LPA verification): < 500ms (95th percentile)

**Load Conditions**:

- Peak load: 500 concurrent users
- Average load: 50 transactions per second during business hours
- Metric calculations: 200 concurrent calculations during peak periods

**Priority**: HIGH

---

#### NFR-P-2: Throughput

**Requirement**: System must handle 10,000 BNG plan submissions per month and 50,000 compliance verification requests per month at steady state.

**Scalability**: Must scale to support 3x growth over 3 years as small sites mandate increases volume.

**Priority**: HIGH

---

### Availability and Resilience

#### NFR-A-1: Availability Target

**Requirement**: System must achieve 99.9% uptime during business hours (Monday-Friday 07:00-19:00 GMT).

- Maximum planned downtime: 4 hours per month (scheduled maintenance outside business hours)
- Maximum unplanned downtime: 8.7 hours per year

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: Maximum acceptable data loss = 15 minutes

**RTO**: Maximum acceptable downtime = 4 hours

**Backup Requirements**:

- Backup frequency: Continuous replication for credit registry, hourly for other data
- Backup retention: 7 years for audit compliance
- Geographic backup location: UK sovereign data centre, different availability zone

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: All users must authenticate via GOV.UK One Login (OIDC/OAuth 2.0).

**Multi-Factor Authentication**: Required for NE validators, LPA officers, and habitat bank operators.

**Session Management**:

- Session timeout: 30 minutes of inactivity
- Re-authentication required for credit purchase transactions

**Priority**: CRITICAL

---

#### NFR-SEC-2: Data Encryption

**Requirement**:

- Data in transit: TLS 1.3 minimum
- Data at rest: AES-256 encryption for all data stores
- Key management: AWS KMS or equivalent UK sovereign service

**Priority**: CRITICAL

---

#### NFR-SEC-3: Fraud Prevention

**Requirement**: The system must implement controls to prevent biodiversity credit fraud, including:

- Double-counting prevention (atomic credit allocation)
- Manipulation detection for metric calculations (anomaly detection on inputs)
- Identity verification for credit sellers (KYB checks for habitat bank operators)
- Transaction audit trail with immutable logging

**Priority**: CRITICAL

---

### Compliance and Regulatory

#### NFR-C-1: Data Privacy

**Applicable Regulations**: UK GDPR, Data Protection Act 2018

**Requirements**:

- [ ] DPIA completed and approved before processing personal data
- [ ] Data subject rights (access, deletion, portability) implemented
- [ ] Privacy notice published on GOV.UK
- [ ] Landowner location data appropriately anonymised in public registry view

**Priority**: CRITICAL

---

#### NFR-C-2: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance (legal requirement under Public Sector Bodies Accessibility Regulations 2018)

**Features**:

- [ ] Keyboard navigation for all functions including map interactions
- [ ] Screen reader compatibility for all content including metric results
- [ ] High contrast mode
- [ ] GDS Design System components throughout

**Priority**: CRITICAL

---

### Usability

#### NFR-U-1: GDS Service Standard

**Requirement**: Platform must meet all 14 points of the GDS Service Standard, passing Alpha and Beta service assessments.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Ordnance Survey MasterMap

**Purpose**: Provide accurate geospatial base mapping and land parcel boundaries

**Integration Type**: Real-time API

**Data Exchanged**:

- **From OS to BNG Platform**: MasterMap topographic features, land parcel boundaries, address data
- **From BNG Platform to OS**: None (read-only consumer)

**Authentication**: OS Data Hub API key

**Priority**: CRITICAL

---

### INT-2: Natural England Designated Sites

**Purpose**: Overlay SSSI, SAC, SPA, and Ramsar designations on site maps for constraint checking

**Integration Type**: OGC WFS/WMS

**Data Exchanged**:

- **From NE to BNG Platform**: Designated site boundaries, condition status, impact risk zones

**Priority**: CRITICAL

---

### INT-3: LPA Planning Systems

**Purpose**: Enable BNG compliance verification within existing planning workflows

**Integration Type**: RESTful API (platform provides API, LPA systems consume)

**Data Exchanged**:

- **From BNG Platform to LPA**: BNG plan status, compliance verification result, credit registration status
- **From LPA to BNG Platform**: Planning application reference, determination outcome

**Authentication**: OAuth 2.0 client credentials

**Priority**: HIGH

---

### INT-4: GOV.UK One Login

**Purpose**: User authentication and identity verification

**Integration Type**: OIDC/OAuth 2.0

**Priority**: CRITICAL

---

### INT-5: GOV.UK Pay

**Purpose**: Payment processing for statutory credit purchases

**Integration Type**: RESTful API

**Priority**: HIGH

---

## Data Requirements

### Data Entities

#### Entity 1: Biodiversity Credit

**Description**: A registered unit of biodiversity value available for allocation against BNG obligations

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| credit_id | UUID | Yes | National unique identifier | Primary key |
| site_id | UUID | Yes | Reference to habitat site | Foreign key |
| habitat_type | Enum | Yes | Biodiversity Metric habitat classification | From NE classification list |
| biodiversity_units | Decimal(10,4) | Yes | Number of biodiversity units | Positive, calculated |
| status | Enum | Yes | Credit lifecycle status | ['pending_validation', 'available', 'reserved', 'allocated', 'retired'] |
| price_per_unit | Decimal(10,2) | No | Listed price (private market) | Positive or null |
| provider_id | UUID | Yes | Habitat bank or statutory provider | Foreign key |
| allocated_to | UUID | No | Development/obligation reference | Null until allocated |
| management_plan_id | UUID | Yes | 30-year management plan | Foreign key |
| created_at | Timestamp | Yes | Registration timestamp | Indexed |
| allocated_at | Timestamp | No | Allocation timestamp | Null until allocated |

**Data Volume**: 50,000 credits Year 1, 200,000 by Year 3

**Data Classification**: OFFICIAL

**Data Retention**: 30 years minimum (aligned with management obligation period)

---

#### Entity 2: Habitat Site

**Description**: A defined land parcel where biodiversity gain is created, enhanced, or maintained

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| site_id | UUID | Yes | Unique identifier | Primary key |
| boundary | Geometry (Polygon) | Yes | Geospatial boundary | Valid polygon, OSGB36/WGS84 |
| area_hectares | Decimal(10,4) | Yes | Site area | Calculated from boundary |
| baseline_habitat | JSONB | Yes | Baseline habitat assessment data | Biodiversity Metric 4.0 schema |
| proposed_habitat | JSONB | Yes | Post-intervention habitat plan | Biodiversity Metric 4.0 schema |
| management_plan | Document | Yes | 30-year management plan | PDF/DOCX |
| financial_security | JSONB | Yes | Bond/insurance details | Required for off-site |

**Data Volume**: 10,000 sites Year 1, 50,000 by Year 3

---

### Data Quality Requirements

**Data Accuracy**: Biodiversity Metric calculations must match NE reference implementation to 0.01 units. Geospatial boundaries accurate to 1 metre.

**Data Completeness**: All mandatory fields required before credit registration. Incomplete applications held in draft status.

**Data Consistency**: Credit totals reconciled daily. No orphaned credits or unlinked obligations.

**Data Timeliness**: Credit status updates reflected within 4 hours. Metric parameter updates applied within 24 hours of NE publication.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy on UK sovereign cloud infrastructure (UK Government Cloud First policy)

**TC-2**: Must use GOV.UK One Login for authentication (cross-government standard)

**TC-3**: Must comply with GDS Service Standard and Technology Code of Practice

**TC-4**: Geospatial components must support OSGB36 (British National Grid) and WGS84 coordinate reference systems

### Business Constraints

**BC-1**: Platform must be operational before small sites BNG mandate comes into force

**BC-2**: Total programme budget capped at £12M over 3 years

**BC-3**: Must use DEFRA's existing cloud hosting account

### Assumptions

**A-1**: Natural England will provide validated Biodiversity Metric 4.0 parameters in machine-readable format

**A-2**: GOV.UK One Login will support the required user roles and organisational identity patterns

**A-3**: At least 3 LPA planning system vendors will develop API integrations within 12 months of specification publication

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Planning delays from BNG | 5-10 days | 0 days | 12 months | LPA determination time analysis |
| BNG credit market volume | £0 | £130M/year | 3 years | Platform transaction data |
| Credit double-counting incidents | Unknown | 0 | Ongoing | Registry integrity checks |
| LPA compliance check time | 5-10 days | 2 days | 6 months | Platform analytics |
| 30-year compliance reporting rate | 0% | >95% | 2 years | Registry compliance data |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.9% | Uptime monitoring |
| API response time (p95) | < 500ms | APM tooling |
| Metric calculation accuracy | 0.01 unit tolerance | NE reference validation |
| Error rate | < 0.1% | Log aggregation |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| PENDING | SRO | [ ] Approved | PENDING | |
| PENDING | NE Chief Scientist | [ ] Approved | PENDING | |
| PENDING | BNG Service Owner | [ ] Approved | PENDING | |
| PENDING | DEFRA Security | [ ] Approved | PENDING | |
| PENDING | CDDO Assessor | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| BNG | Biodiversity Net Gain — mandatory 10% improvement in biodiversity value |
| Biodiversity Metric 4.0 | Natural England's calculation tool for measuring biodiversity value |
| Biodiversity Unit | The unit of measurement for biodiversity value in the metric |
| Habitat Bank | Organisation creating habitats to generate biodiversity credits for sale |
| Statutory Credit | DEFRA-sold credit of last resort at premium pricing |
| LPA | Local Planning Authority |
| 30-year obligation | Statutory requirement to manage BNG habitats for minimum 30 years |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 15 Architecture Principles
- ARC-001-STKE-v1.0 — BNG Platform Stakeholder Analysis
- Environment Act 2021, Part 6
- Natural England Biodiversity Metric 4.0 User Guide
- GDS Service Standard

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Biodiversity Net Gain Platform
**Model**: Claude Opus 4.6
