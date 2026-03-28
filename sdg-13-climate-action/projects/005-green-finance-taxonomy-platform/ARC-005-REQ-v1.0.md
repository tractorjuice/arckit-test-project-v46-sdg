# Project Requirements: Green Finance Taxonomy Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Green Finance Taxonomy Platform (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Green Finance Taxonomy Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Green Finance Programme Board, HMT Digital, FCA, GTAG, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Green Finance Taxonomy Platform — a digital service providing a machine-readable classification engine that determines whether economic activities qualify as environmentally sustainable under the UK Green Taxonomy, supporting the UK's Green Finance Strategy and FCA Sustainability Disclosure Requirements.

---

## Executive Summary

### Business Context

The UK Government committed to developing a UK Green Taxonomy as part of its Green Finance Strategy. The EU Taxonomy Regulation (2020) has set the global benchmark, and the UK needs its own science-based classification system that is internationally interoperable while reflecting UK-specific economic context. The Green Technical Advisory Group (GTAG) has published recommendations on taxonomy criteria. The FCA's Sustainability Disclosure Requirements (SDR) and anti-greenwashing rule create regulatory demand for an objective classification mechanism. The platform will serve financial institutions managing an estimated GBP 2 trillion in ESG-labelled assets.

### Objectives

- Launch an API-first classification service covering energy, transport, buildings, and manufacturing sectors within 12 months
- Achieve GTAG endorsement of all classification criteria before launch
- Deliver sub-second API response time enabling real-time investment screening
- Provide EU Taxonomy interoperability mapping for cross-border investment
- Implement robust "do no significant harm" (DNSH) screening to prevent greenwashing
- Enable FCA to reference platform classifications in SDR supervisory assessments

### Expected Outcomes

- 50+ financial institutions integrated within 6 months of launch
- FCA formally recognises platform classifications for SDR compliance purposes
- UK Green Taxonomy referenced in at least 100 green bond prospectuses within 18 months
- Zero successful greenwashing challenges based on platform classifications
- EU-UK taxonomy interoperability mapping enables cross-border fund compliance

### Project Scope

**In Scope**:

- Classification engine for economic activities against GTAG-defined criteria
- "Do no significant harm" (DNSH) screening across 6 environmental objectives
- API-first service with sub-second classification response time
- Bulk classification for portfolio screening (10,000+ activities per request)
- EU Taxonomy interoperability mapping
- Classification audit trail and decision explainability
- Sector coverage: energy, transport, buildings, manufacturing (at launch)
- Transition activity classification with time-bound pathway requirements

**Out of Scope**:

- ESG rating or scoring (this is not an ESG ratings agency)
- Company-level sustainability assessment (activity-level classification only)
- Portfolio construction or investment advice
- Regulatory enforcement (FCA responsibility)
- Agriculture, forestry, and water sectors (Phase 2)

---

## Business Requirements

### BR-001: Machine-Readable Classification Service

**Description**: Provide an API-first classification engine that returns definitive, auditable taxonomy alignment decisions for economic activities in real-time.

**Rationale**: Financial institutions need machine-readable classifications for automated investment screening, fund labelling, and regulatory reporting. Manual classification processes are too slow and inconsistent.

**Success Criteria**:

- Sub-second API response time for individual classification queries
- Bulk classification of 10,000+ activities within 60 seconds
- Classification decisions are deterministic — same input always produces same output
- Audit trail for every classification decision

**Priority**: MUST_HAVE

---

### BR-002: GTAG-Endorsed Criteria

**Description**: Implement classification criteria endorsed by the Green Technical Advisory Group, with transparent, science-based thresholds for each economic activity and environmental objective.

**Rationale**: GTAG endorsement provides scientific credibility. Without it, the taxonomy is vulnerable to greenwashing accusations and academic criticism.

**Success Criteria**:

- Formal GTAG endorsement letter for all launch sectors
- Criteria documentation published openly with scientific references
- DNSH screening methodology peer-reviewed by independent academic institutions

**Priority**: MUST_HAVE

---

### BR-003: FCA Regulatory Integration

**Description**: Enable the FCA to reference platform classifications in SDR supervisory assessments, providing regulated firms with a definitive classification source for sustainability claims.

**Rationale**: The anti-greenwashing rule requires sustainability claims to be substantiated. Platform classifications provide the objective evidence base.

**Success Criteria**:

- FCA formally recognises platform classifications for SDR compliance
- Classification output format compatible with FCA regulatory reporting requirements
- Auditable decision trail suitable for FCA enforcement evidence

**Priority**: MUST_HAVE

---

### BR-004: EU Taxonomy Interoperability

**Description**: Provide interoperability mapping between UK Green Taxonomy and EU Taxonomy criteria, enabling cross-border investment classification.

**Rationale**: London-based fund managers manage EU-domiciled funds. Cross-border investment requires dual classification capability.

**Success Criteria**:

- Published interoperability mapping covering shared sectors
- API supports dual UK/EU taxonomy classification queries
- Financial sector confirms mapping is usable for cross-border compliance

**Priority**: SHOULD_HAVE

---

### BR-005: Greenwashing Prevention

**Description**: Implement robust DNSH screening and transition activity controls that prevent the taxonomy from being used to legitimise environmentally harmful activities.

**Rationale**: NGO and media scrutiny will be intense. A single high-profile greenwashing case enabled by taxonomy classification would undermine the entire framework.

**Success Criteria**:

- DNSH screening applied across all 6 environmental objectives for every classification
- Transition activities require mandatory time-bound decarbonisation pathway
- No NGO-identified greenwashing case attributable to taxonomy classification within 12 months of launch

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: ESG Fund Manager

- **Role**: Portfolio manager at asset management firm managing sustainable investment funds
- **Goals**: Screen investments for taxonomy alignment, produce SDR-compliant fund reports, substantiate sustainability claims
- **Pain Points**: Inconsistent ESG ratings, no definitive classification standard, greenwashing risk
- **Technical Proficiency**: Medium (uses portfolio management systems, not a developer)

#### Persona 2: Compliance Officer

- **Role**: Regulatory compliance officer at bank/asset manager
- **Goals**: Produce FCA SDR reports, verify sustainability claims, maintain audit trail
- **Pain Points**: Ambiguous regulations, no objective classification source, manual processes
- **Technical Proficiency**: Medium

#### Persona 3: Fintech Developer

- **Role**: Software developer building ESG data products
- **Goals**: Integrate taxonomy API into investment platform, build taxonomy screening tools
- **Pain Points**: No standardised taxonomy API, inconsistent data formats, poor documentation
- **Technical Proficiency**: High

#### Persona 4: Corporate Sustainability Officer

- **Role**: Head of sustainability at FTSE 350 company
- **Goals**: Classify company activities for green bond issuance, transition plan development
- **Pain Points**: Unclear criteria, no self-service classification tool, expensive consultancy
- **Technical Proficiency**: Low-Medium

---

### Functional Requirements Detail

#### FR-001: Activity Classification API

**Description**: Provide a RESTful API that accepts economic activity descriptions and returns taxonomy alignment classification.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given an activity description with sector, activity type, and performance data, when submitted to the API, then a classification result is returned within 500ms
- [ ] Given the classification result, when returned, then it includes: aligned/not_aligned/transition/insufficient_data status
- [ ] Given each classification, when returned, then it includes the decision rationale referencing specific criteria thresholds
- [ ] Given each classification, when processed, then an immutable audit record is created with inputs, outputs, criteria version, and timestamp

**Priority**: MUST_HAVE

---

#### FR-002: Bulk Classification API

**Description**: Process bulk classification requests for portfolio-level screening.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a batch of up to 10,000 activities, when submitted, then all classifications are returned within 60 seconds
- [ ] Given the bulk response, when returned, then each activity has an individual classification with rationale
- [ ] Given the bulk response, when aggregated, then portfolio-level taxonomy alignment percentage is calculated
- [ ] Given a bulk request, when processed asynchronously for very large batches, then a callback/polling mechanism is provided

**Priority**: MUST_HAVE

---

#### FR-003: DNSH Screening Engine

**Description**: Screen each activity against "do no significant harm" criteria across 6 environmental objectives.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given an activity that meets substantial contribution criteria, when DNSH screening is applied, then all 6 environmental objectives are checked
- [ ] Given a DNSH failure on any objective, when detected, then the activity is classified as "not aligned" regardless of substantial contribution
- [ ] Given the DNSH result, when returned, then specific failed objectives and reasons are identified
- [ ] Environmental objectives screened: climate mitigation, climate adaptation, water, circular economy, pollution, biodiversity

**Priority**: MUST_HAVE

---

#### FR-004: Transition Activity Classification

**Description**: Classify transition activities with mandatory time-bound decarbonisation pathway requirements.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given an activity classified as "transition," when the classification is returned, then a mandatory transition pathway is referenced
- [ ] Given a transition classification, when accepted, then the entity must submit a time-bound decarbonisation plan
- [ ] Given a transition classification, when time-limited, then an expiry date is applied (maximum 5 years, renewable with progress evidence)
- [ ] Given a transition classification, when displayed, then it is clearly distinguished from "aligned" with separate labelling

**Priority**: MUST_HAVE

---

#### FR-005: Classification Criteria Management

**Description**: Enable GTAG and HMT to manage classification criteria through a structured criteria management workflow.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given new criteria, when proposed by GTAG, then they enter a draft/review/approved workflow
- [ ] Given approved criteria, when published, then they are versioned with effective dates
- [ ] Given criteria changes, when published, then all previously issued classifications remain valid against the criteria version used
- [ ] Given criteria updates, when applied, then a transition period allows reclassification of affected activities

**Priority**: MUST_HAVE

---

#### FR-006: EU Taxonomy Mapping

**Description**: Provide mapping between UK and EU taxonomy criteria for shared sectors.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given a UK taxonomy classification, when EU mapping is requested, then the equivalent EU taxonomy criteria and alignment status are returned
- [ ] Given divergent criteria, when identified, then the specific differences are documented
- [ ] Given a dual classification request, when submitted, then both UK and EU classifications are returned simultaneously

**Priority**: SHOULD_HAVE

---

#### FR-007: Self-Service Classification Portal

**Description**: Provide a web-based portal for users who need to classify individual activities without API integration.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given the portal, when accessed, then a guided wizard collects activity details step-by-step
- [ ] Given the wizard, when completed, then the classification result with full rationale is displayed
- [ ] Given the result, when displayed, then it can be downloaded as a PDF classification certificate
- [ ] Given the portal, when used by a non-technical user, then no API knowledge is required

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: API Response Time

**Requirement**: Single classification within 500ms at p95. Bulk classification (10,000 activities) within 60 seconds.

**Priority**: MUST_HAVE

#### NFR-P-002: Concurrent Users

**Requirement**: Support 500 concurrent API consumers with no degradation.

**Priority**: MUST_HAVE

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.9% uptime. Zero downtime during market hours (07:00-21:00 UK time, Monday-Friday).

**Priority**: MUST_HAVE

#### NFR-A-002: Disaster Recovery

**RPO**: 1 hour | **RTO**: 2 hours

**Priority**: MUST_HAVE

### Security Requirements

#### NFR-SEC-001: API Authentication

**Requirement**: API consumers authenticated via API keys (free tier, rate-limited) and OAuth 2.0 (premium tier, higher limits). Portal users authenticate via email verification.

**Priority**: MUST_HAVE

#### NFR-SEC-002: Classification Integrity

**Requirement**: All classification decisions cryptographically signed to prevent tampering. Classification certificates verifiable against platform records.

**Priority**: MUST_HAVE

#### NFR-SEC-003: Criteria Security

**Requirement**: Draft criteria (pre-publication) classified as OFFICIAL-SENSITIVE. Pre-publication access restricted to GTAG members and HMT Green Finance Team.

**Priority**: MUST_HAVE

### Accessibility Requirements

#### NFR-U-001: Portal Accessibility

**Requirement**: Self-service portal meets WCAG 2.2 Level AA. API documentation accessible. GOV.UK Design System used for portal.

**Priority**: MUST_HAVE

### Compliance Requirements

#### NFR-C-001: FCA Recognition

**Requirement**: Platform classifications must meet FCA's requirements for use as evidence in SDR compliance assessments.

**Priority**: MUST_HAVE

#### NFR-C-002: Audit Trail

**Requirement**: Immutable audit trail for all classifications retained for 7 years. Each classification record includes: inputs, criteria version, DNSH results, output, timestamp, API consumer identity.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: FCA Regulatory Reporting

**Purpose**: Enable regulated firms to submit taxonomy alignment data as part of SDR regulatory returns.

**Integration Type**: Structured data export compatible with FCA reporting standards

**Priority**: MUST_HAVE

### INT-002: LSEG Green Bond Platform

**Purpose**: Provide taxonomy classification for green bond listings on London Stock Exchange.

**Integration Type**: REST API integration

**Priority**: SHOULD_HAVE

### INT-003: Companies House

**Purpose**: Verify corporate entities submitting classification requests for green bond issuance.

**Integration Type**: REST API (real-time lookup)

**Priority**: SHOULD_HAVE

### INT-004: EU Taxonomy Platform (EUAP)

**Purpose**: Cross-reference EU taxonomy criteria for interoperability mapping.

**Integration Type**: Data synchronisation (periodic, when EU criteria updated)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Classification Request

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique request identifier |
| api_consumer_id | UUID | Yes | Requesting entity |
| sector_code | String | Yes | NACE/SIC sector classification |
| activity_type | String | Yes | Economic activity description |
| performance_data | JSON | Yes | Activity performance metrics against criteria |
| request_timestamp | DateTime | Yes | When classification was requested |

#### Entity 2: Classification Decision

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique decision identifier |
| request_id | UUID | Yes | Associated request |
| uk_taxonomy_status | Enum | Yes | Aligned, not_aligned, transition, insufficient_data |
| substantial_contribution | JSON | Yes | Assessment against environmental objective |
| dnsh_results | JSON | Yes | DNSH screening results per objective |
| criteria_version | String | Yes | Version of criteria applied |
| decision_rationale | Text | Yes | Machine-readable reasoning |
| digital_signature | String | Yes | Cryptographic signature |
| decision_timestamp | DateTime | Yes | When decision was rendered |

#### Entity 3: Taxonomy Criteria

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique criteria identifier |
| sector | String | Yes | Economic sector |
| activity | String | Yes | Specific economic activity |
| environmental_objective | Enum | Yes | Which of 6 objectives this contributes to |
| threshold_metric | String | Yes | Performance metric name |
| threshold_value | Decimal | Yes | Numeric threshold |
| threshold_unit | String | Yes | Unit of measurement |
| version | String | Yes | Criteria version |
| effective_date | Date | Yes | When criteria become effective |
| gtag_endorsement_date | Date | No | Date GTAG endorsed |
| status | Enum | Yes | Draft, review, approved, superseded |

**Data Volume**: Approximately 500 criteria entries at launch; 10 million+ classifications per year

---

## Approval

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, HMT | _________ | PENDING |
| GTAG Chair | _________ | PENDING |
| FCA Representative | _________ | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK Green Finance Strategy | Policy | GOV.UK | Taxonomy commitment | N/A |
| GTAG Reports | Advisory | GOV.UK | Criteria recommendations | N/A |
| FCA SDR Policy Statement | Regulation | FCA | SDR framework, anti-greenwashing | N/A |
| EU Taxonomy Regulation | Legislation | EUR-Lex | Interoperability reference | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Green Finance Taxonomy Platform (Project 005)
**Model**: Claude Opus 4.6
