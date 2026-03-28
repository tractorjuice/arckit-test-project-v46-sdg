# Project Requirements: Social Housing Allocation Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Social Housing Allocation Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Social Housing Digital Programme, DLUHC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Digital, LGA, Regulator of Social Housing, Housing Association Federation |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies the requirements for a national Social Housing Allocation Platform enabling fair, transparent allocation of social housing across England. It supports choice-based lettings (CBL), respects the Allocation of Housing (England) Regulations 2002, and integrates homelessness duties under the Homelessness Reduction Act 2017. The platform must serve 300+ local authorities, 1.2 million+ applicants, and major housing associations.

---

## Executive Summary

### Business Context

England has over 1.2 million households on social housing waiting lists, managed by 300+ local authorities each operating independent allocation systems. Processes range from modern digital platforms to paper-based applications. This fragmentation prevents national visibility, creates inconsistent applicant experiences, and imposes administrative burden on housing associations operating across multiple council areas.

The Social Housing (Regulation) Act 2023 strengthened consumer standards, requiring transparent allocation processes. The Homelessness Reduction Act 2017 requires councils to give reasonable preference to homeless applicants. A national platform creates the data infrastructure to support these statutory requirements while preserving local allocation policy autonomy.

### Objectives

- Deliver a national platform supporting choice-based lettings across 300+ English local authorities
- Preserve local authority control over allocation policies (banding, points, local connection)
- Provide applicants with transparent queue positions, property availability, and allocation decisions
- Enable housing associations to receive nominations through a single standardised interface
- Generate national housing allocation data for policy analysis and regulatory oversight

### Expected Outcomes

- 80% of English local authorities onboarded within 3 years (240 of 309)
- 75% applicant satisfaction with the application and bidding process
- 60% reduction in administrative cost per allocation for participating councils
- National real-time waiting list data available for the first time
- 40% reduction in allocation-related complaints and legal challenges

### Project Scope

**In Scope**:

- Applicant registration, assessment, and banding/points engine (configurable per council)
- Choice-based lettings — property advertising, applicant bidding, shortlisting
- Nominations interface for housing associations
- Allocation decision recording with audit trail and applicant notification
- Homelessness Reduction Act 2017 integration (reasonable preference flagging)
- National reporting and analytics dashboard
- Migration tools for legacy system data

**Out of Scope**:

- Tenancy management (post-allocation management is a separate system)
- New-build housing development pipeline (Homes England scope)
- Private rented sector allocation
- Council tax and housing benefit administration
- Physical housing stock condition surveys

---

## Business Requirements

### BR-001: Configurable Allocation Policy Engine

**Description**: The platform must support each council's unique allocation scheme, including banding systems, points-based systems, local connection criteria, and reasonable preference categories as required by the Allocation of Housing (England) Regulations 2002.

**Rationale**: Councils have statutory responsibility for their own allocation schemes. The platform must respect this autonomy to achieve adoption (ref: SD-2).

**Success Criteria**:

- Each council can configure its own banding/points scheme without code changes
- Statutory reasonable preference categories enforced across all schemes
- Allocation policy changes deployable within 5 working days

**Priority**: MUST_HAVE

**Stakeholder**: Local Authority Housing Directors (SD-2)

---

### BR-002: Choice-Based Lettings

**Description**: The platform must support choice-based lettings, enabling applicants to view available properties, express preferences (bid), and receive transparent shortlisting outcomes.

**Rationale**: CBL is the predominant allocation model in England, giving applicants meaningful choice and increasing letting success rates (ref: SD-3).

**Success Criteria**:

- Properties advertised with photos, floor plans, location, accessibility features, and rent
- Applicants can bid on properties matching their assessed needs
- Shortlisting applies council's allocation scheme transparently
- Applicants notified of outcome with explanation

**Priority**: MUST_HAVE

**Stakeholder**: Housing Applicants (SD-3)

---

### BR-003: Housing Association Nominations API

**Description**: The platform must provide a standardised API for housing associations to receive nominations, confirm offers, and report lettings outcomes.

**Rationale**: Housing associations managing stock across multiple councils currently interface with dozens of different systems. A single API reduces administrative overhead and improves data quality (ref: SD-5).

**Success Criteria**:

- Single API serving all council nomination requests
- Real-time vacancy reporting by housing associations
- Offer acceptance/rejection workflow with audit trail

**Priority**: MUST_HAVE

**Stakeholder**: Housing Associations (SD-5)

---

### BR-004: Homelessness Integration

**Description**: The platform must integrate with council homelessness services to ensure applicants owed duties under the Homelessness Reduction Act 2017 receive appropriate reasonable preference and outcomes are tracked.

**Rationale**: Statutory requirement to give reasonable preference to homeless applicants. H-CLIC reporting requires outcome data (ref: SD-6).

**Success Criteria**:

- Automatic reasonable preference flagging for applicants with homelessness duty
- H-CLIC compatible data export for DLUHC reporting
- Outcome tracking (housed, duty discharged, lost contact)

**Priority**: MUST_HAVE

**Stakeholder**: Homelessness and Rough Sleeping Directorate (SD-6)

---

### BR-005: National Reporting Dashboard

**Description**: The platform must generate national and local reporting on waiting list composition, allocation outcomes, waiting times, and demographic analysis.

**Rationale**: No real-time national data currently exists. DLUHC, RSH, and Parliament need evidence-based housing allocation data (ref: SD-1, SD-4).

**Success Criteria**:

- Real-time national dashboard updated daily
- Council-level drill-down showing local performance
- Demographic and equalities analysis capability
- Annual LAHS data automatically generated from platform data

**Priority**: MUST_HAVE

**Stakeholder**: DLUHC Minister (SD-1), RSH (SD-4)

---

## Functional Requirements

### FR-001: Applicant Self-Service Registration

**Description**: Applicants must be able to register, provide household details, upload evidence, and track their application status through an accessible digital service.

**Acceptance Criteria**:

- [ ] Given a housing applicant, when they access the registration service, then they can complete an application in plain language without housing jargon
- [ ] Given an applicant with limited digital skills, when they need assistance, then an assisted digital pathway is available (telephone, in-person at council office)
- [ ] Edge case: If an applicant is registered with multiple councils (cross-boundary), the system prevents duplicate registrations and supports cross-referral

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-002: Property Advertising and Bidding

**Description**: Available properties must be advertised with sufficient detail for informed choice, and applicants must be able to bid within defined bidding cycles.

**Acceptance Criteria**:

- [ ] Given an available property, when it is advertised, then it shows rent, property type, bedrooms, accessibility features, location map, and photos
- [ ] Given an eligible applicant, when they bid on a property, then they receive confirmation and can track their position in the shortlist
- [ ] Edge case: If a property is withdrawn mid-cycle, all bidders are notified with explanation

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-003: Automated Shortlisting

**Description**: The system must automatically generate a shortlist for each property based on the council's allocation scheme, ranking applicants by band/priority, waiting time, and property suitability.

**Acceptance Criteria**:

- [ ] Given a property with bids, when the bidding cycle closes, then the system generates a ranked shortlist applying the council's configured allocation scheme
- [ ] Given a shortlisted applicant, when an offer is made, then the allocation decision is recorded with full audit trail
- [ ] Edge case: If two applicants have equal priority and waiting time, the tie-break rule (per council configuration) is applied and documented

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-004: Allocation Decision Audit Trail

**Description**: Every allocation decision must be fully auditable — recording which applicants bid, how they were ranked, why the successful applicant was selected, and why others were not.

**Acceptance Criteria**:

- [ ] Given an allocation decision, when an applicant requests an explanation, then a plain-language summary is available showing their band, position, and the reason they were not offered the property
- [ ] Given a legal challenge to an allocation, when the decision is reviewed, then the full ranking, rules applied, and data used are retrievable

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-005: DWP Universal Credit Integration

**Description**: The platform must exchange data with DWP's Universal Credit system to verify housing costs and support direct payment of housing element to landlords.

**Acceptance Criteria**:

- [ ] Given an applicant in receipt of UC housing element, when they are allocated a property, then the housing costs data is exchanged with DWP
- [ ] Given a direct payment arrangement, when the landlord requests direct payment, then the platform facilitates the request to DWP

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

**Dependencies**: DWP UC Modernisation (Project 001) integration readiness

---

## Non-Functional Requirements

### NFR-P-001: Response Time

**Requirement**: Applicant-facing pages must load within 2 seconds (p95). Property search results returned within 3 seconds. Shortlisting calculation completed within 60 seconds per property.

**Priority**: HIGH

---

### NFR-A-001: Availability

**Requirement**: 99.9% availability during bidding cycles (typically Monday-Friday). Planned maintenance permitted outside bidding cycles (weekends 02:00-06:00).

**Priority**: HIGH

---

### NFR-SEC-001: Data Protection

**Requirement**: Full UK GDPR compliance. Housing applicant data classified as OFFICIAL-SENSITIVE (includes vulnerability, health, domestic abuse, homelessness circumstances). Data residency within UK.

**Priority**: CRITICAL

---

### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA. Service must be usable by applicants with low digital literacy on low-specification mobile devices. Multi-language support for top 10 community languages per council area.

**Priority**: CRITICAL

---

### NFR-S-001: Multi-Tenancy

**Requirement**: Platform must support 300+ councils as tenants with complete data isolation. Each council's applicant data, allocation policies, and configuration fully separated.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-001: Legacy Allocation System Migration

**Purpose**: Migrate applicant data, waiting list positions, and allocation history from legacy council systems.

**Integration Type**: Batch data migration with validation

**Priority**: CRITICAL

---

### INT-002: H-CLIC Reporting Integration

**Purpose**: Generate H-CLIC compatible homelessness data returns for DLUHC.

**Integration Type**: Batch export (quarterly)

**Priority**: HIGH

---

### INT-003: DWP Universal Credit

**Purpose**: Housing costs verification and direct payment management.

**Integration Type**: Real-time API (target), batch file (interim)

**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must support multi-tenancy for 300+ councils with complete data isolation.

**TC-2**: Must integrate with diverse legacy systems across councils (no single standard).

**TC-3**: Must deploy on UK sovereign cloud infrastructure.

### Business Constraints

**BC-1**: Councils cannot be mandated to adopt the platform — adoption must be incentivised.

**BC-2**: Platform must not override councils' statutory allocation scheme powers.

**BC-3**: Budget envelope of GBP 85M over 5 years.

### Assumptions

**A-1**: At least 50 early adopter councils will onboard in Year 1 to prove the platform.

**A-2**: Legacy system data can be mapped to a common data model (may require council-specific transformations).

**A-3**: Housing associations will adopt the nominations API if it reduces their administrative burden.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Councils onboarded | 0 | 240 (80%) | March 2029 | Platform analytics |
| Applicant satisfaction | ~50% (varies) | 75% | March 2028 | GDS transaction survey |
| Cost per allocation | GBP 850 (average) | GBP 340 | Year 3 | Council financial reporting |
| Allocation complaints | Varies | 40% reduction | Year 2 | Council complaint data |
| Average time to allocation | 18 months (national avg) | Platform cannot reduce — supply constraint | N/A | Tracked for reporting |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| DLUHC CDIO | Technical Authority | [ ] Approved | PENDING |
| LGA Representative | Sector Body | [ ] Approved | PENDING |
| RSH | Regulator | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Social Housing Allocation Platform
**Model**: Claude Opus 4.6
