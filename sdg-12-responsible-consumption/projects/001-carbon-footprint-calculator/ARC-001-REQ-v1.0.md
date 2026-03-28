# Project Requirements: Carbon Footprint Calculator

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Carbon Footprint Calculator (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Carbon Footprint Calculator |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Digital, CCS Integration Team, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Carbon Footprint Calculator — a DESNZ-owned digital service enabling government suppliers to calculate and report their greenhouse gas emissions in compliance with the GHG Protocol Corporate Standard and PPN 06/21 Carbon Reduction Plan requirements.

---

## Executive Summary

### Business Context

The UK Government spends over GBP 300 billion annually through procurement. PPN 06/21 requires suppliers bidding for contracts above GBP 5 million to publish Carbon Reduction Plans, yet no standardised government tool exists for calculating carbon footprints. Suppliers use inconsistent methodologies, producing incomparable data that contracting authorities cannot meaningfully evaluate. The Carbon Footprint Calculator will provide a free, GHG Protocol-compliant calculation engine that standardises emissions reporting across the government supply chain, enabling carbon-informed procurement decisions for the first time at scale.

The tool addresses a critical gap in the UK's Net Zero Strategy delivery infrastructure. The Climate Change Committee has identified government procurement as an under-exploited decarbonisation lever. By providing a standardised calculation tool, the government can quantify its supply chain emissions (estimated at 15-20 million tCO2e annually) and target reduction interventions where they will have greatest impact.

### Objectives

- Deliver a GHG Protocol-compliant calculation engine covering Scope 1, Scope 2, and material Scope 3 emissions categories
- Enable SME suppliers to complete carbon footprint assessments within 2 hours using readily available business data
- Produce normalised carbon intensity scores for integration with the Sustainable Procurement Portal (Project 004)
- Automate annual BEIS/DESNZ GHG Conversion Factor updates with zero manual data entry
- Publish calculation methodology openly for peer review and public scrutiny

### Expected Outcomes

- 50% of central government procurement spend covered by standardised supplier carbon footprints within 18 months
- 80% of contracting authorities using standardised carbon scores within 24 months
- 5,000 supplier calculations completed within 12 months of launch, 60% from SMEs
- Elimination of inconsistent PPN 06/21 carbon assessment across contracting authorities

### Project Scope

**In Scope**:

- GHG Protocol Scope 1, 2, and 3 calculation engine with BEIS/DESNZ conversion factors
- Supplier self-service web interface with guided calculation workflows
- Sector-specific estimation tools for SMEs lacking detailed emissions data
- Normalised carbon intensity scoring and sector benchmarking
- API for Sustainable Procurement Portal integration
- Annual emissions factor update automation
- Carbon Reduction Plan generation from calculation outputs
- Open methodology documentation

**Out of Scope**:

- Product-level carbon footprinting (lifecycle assessment / ISO 14067) — future phase
- Scope 3 Category 11 (use of sold products) detailed modelling — available as estimation only
- Carbon offset verification and trading
- Direct enforcement of PPN 06/21 compliance (policy responsibility of CCS)
- Supplier decarbonisation advisory services (signposted to UK Business Climate Hub)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | DESNZ | Decision maker |
| Service Owner | Service accountability | DESNZ | Service governance |
| Chief Scientific Adviser | Methodology authority | DESNZ | Calculation validation |
| Product Manager | Requirements prioritisation | DESNZ | Requirements definition |
| CCS Integration Lead | Procurement integration | CCS | Integration requirements |
| Climate Science Team Lead | Emissions factors | DESNZ | Factor management |
| Enterprise Architect | Technical oversight | DESNZ Digital | Architecture review |
| Security Lead | Security assurance | DESNZ | Security review |
| SME User Representatives | User acceptance | FSB, Make UK | Usability testing |

---

## Business Requirements

### BR-1: Standardised Carbon Calculation Methodology

**Description**: The service must implement a single, standardised carbon calculation methodology based on the GHG Protocol Corporate Standard, producing consistent results regardless of which supplier uses it or when they use it.

**Rationale**: Currently, suppliers use disparate methodologies producing incomparable data. Standardisation is essential for fair procurement evaluation and credible national reporting.

**Success Criteria**:

- All calculations use the same GHG Protocol-compliant methodology
- Two suppliers with identical operations produce identical carbon footprints
- Methodology published and accepted by DESNZ Chief Scientific Adviser

**Priority**: MUST_HAVE

**Stakeholder**: DESNZ Chief Scientific Adviser (SD-2)

---

### BR-2: Accessible to SME Suppliers

**Description**: The service must be usable by SME suppliers without specialist environmental expertise, external consultants, or specialised measurement equipment.

**Rationale**: SMEs represent 33% of government procurement spend. If the tool excludes SMEs, the government loses a significant decarbonisation lever and faces political risk (SD-4).

**Success Criteria**:

- Average completion time under 2 hours for Scope 1 and 2 calculation
- 60% of completed calculations from organisations with fewer than 250 employees
- User satisfaction score above 7/10 from SME users

**Priority**: MUST_HAVE

**Stakeholder**: SME Suppliers (SD-4), FSB

---

### BR-3: Procurement Integration

**Description**: The service must produce normalised carbon scores that can be consumed by the Sustainable Procurement Portal (Project 004) via API, enabling automated carbon evaluation in procurement decisions.

**Rationale**: Carbon data is only valuable for decarbonisation if it influences procurement decisions. Without integration, carbon reporting remains a compliance exercise with no impact on supplier behaviour (SD-3).

**Success Criteria**:

- API delivering normalised carbon intensity scores (tCO2e per GBP million revenue)
- Sector benchmarks for at least 20 SIC code categories
- Scores consumed by Sustainable Procurement Portal without manual intervention

**Priority**: MUST_HAVE

**Stakeholder**: Crown Commercial Service (SD-3)

---

### BR-4: Scientific Credibility and Transparency

**Description**: The service must produce scientifically defensible emissions calculations with published methodology, auditable calculation chains, and transparent uncertainty quantification.

**Rationale**: The Calculator's credibility depends on scientific rigour. NGOs, the Climate Change Committee, and academic researchers will scrutinise the methodology and outputs (SD-5).

**Success Criteria**:

- Methodology document published on GOV.UK and open for peer review
- Calculation audit trail showing activity data, emissions factors applied, and resulting tCO2e
- Independent academic review completed before public launch

**Priority**: MUST_HAVE

**Stakeholder**: Environmental NGOs (SD-5), Chief Scientific Adviser (SD-2)

---

### BR-5: Annual Emissions Factor Currency

**Description**: The service must incorporate updated BEIS/DESNZ GHG Conversion Factors within 5 working days of annual publication, with automated ingestion and regression testing.

**Rationale**: Stale emissions factors produce incorrect calculations. The update process must be automated to avoid creating unsustainable workload for the Climate Science Team (SD-6).

**Success Criteria**:

- Factor updates ingested within 5 working days of DESNZ publication
- Zero manual data entry in the update process
- Regression tests confirm existing calculations produce updated results

**Priority**: MUST_HAVE

**Stakeholder**: Climate Science Team (SD-6)

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — SME Operations Manager

- **Role**: Operations Manager at a 50-person IT services company
- **Goals**: Complete carbon footprint calculation for government contract bid; demonstrate commitment to Net Zero
- **Pain Points**: No environmental expertise; unsure what data to collect; intimidated by carbon terminology
- **Technical Proficiency**: Medium (comfortable with web apps, not specialist tools)

#### Persona 2: David — Corporate Sustainability Manager

- **Role**: Sustainability Manager at a 5,000-person engineering firm
- **Goals**: Submit standardised carbon data for government procurement; align with existing CDP disclosure
- **Pain Points**: Already reports to CDP; does not want to duplicate effort; needs tool to accept existing data
- **Technical Proficiency**: High (experienced with carbon reporting platforms)

#### Persona 3: Rachel — Procurement Officer

- **Role**: Category Manager at a central government department
- **Goals**: Evaluate supplier carbon performance as part of procurement scoring
- **Pain Points**: Cannot interpret raw emissions data; needs normalised, comparable scores
- **Technical Proficiency**: Medium (comfortable with procurement systems)

---

### Functional Requirements Detail

#### FR-1: Scope 1 Direct Emissions Calculation

**Description**: The system must calculate Scope 1 direct GHG emissions from sources owned or controlled by the reporting organisation, including stationary combustion (gas, oil, coal), mobile combustion (fleet vehicles), process emissions, and fugitive emissions (refrigerants, SF6).

**Relates To**: BR-1, BR-4

**Acceptance Criteria**:

- [ ] Given a user enters natural gas consumption in kWh, when the calculation runs, then Scope 1 emissions are calculated using BEIS/DESNZ natural gas emission factor and reported in tCO2e
- [ ] Given a user enters fleet vehicle mileage by fuel type, when the calculation runs, then mobile combustion emissions are calculated per vehicle category
- [ ] Given a user enters refrigerant type and quantity lost, when the calculation runs, then fugitive emissions are calculated using GWP values from BEIS/DESNZ factors
- [ ] Edge case: If a user has no Scope 1 sources (e.g., fully serviced office), the system accepts zero Scope 1 with explanation

**Data Requirements**:

- **Inputs**: Fuel type, fuel quantity (kWh, litres, or tonnes), vehicle type, mileage, refrigerant type, refrigerant quantity
- **Outputs**: tCO2e by Scope 1 sub-category, total Scope 1 tCO2e
- **Validations**: Fuel quantities must be positive; vehicle mileage must be realistic (flag if >100,000 miles/vehicle/year)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-2: Scope 2 Energy Indirect Emissions Calculation

**Description**: The system must calculate Scope 2 indirect GHG emissions from purchased electricity, heat, steam, and cooling, supporting both location-based and market-based accounting methods as defined by the GHG Protocol Scope 2 Guidance.

**Relates To**: BR-1, BR-4

**Acceptance Criteria**:

- [ ] Given a user enters electricity consumption in kWh, when the calculation runs, then location-based Scope 2 emissions are calculated using UK grid average factor
- [ ] Given a user provides evidence of a renewable electricity contract (REGO-backed), when market-based method is selected, then Scope 2 market-based emissions reflect the contractual factor
- [ ] Given a user has purchased heat or steam from a district heating network, when the calculation runs, then heat/steam emissions are calculated using appropriate factors
- [ ] Both location-based and market-based Scope 2 figures are reported (GHG Protocol dual reporting requirement)

**Data Requirements**:

- **Inputs**: Electricity consumption (kWh), electricity tariff type (grid/renewable), heat/steam consumption (kWh), supplier evidence for market-based claims
- **Outputs**: Scope 2 location-based tCO2e, Scope 2 market-based tCO2e
- **Validations**: Market-based claims require supporting evidence (REGO certificate reference or supplier declaration)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-3: Scope 3 Value Chain Emissions Calculation

**Description**: The system must calculate Scope 3 indirect emissions across the 15 GHG Protocol Scope 3 categories, with mandatory estimation for material categories and optional detailed calculation for organisations with supply chain data.

**Relates To**: BR-1, BR-2, BR-4

**Acceptance Criteria**:

- [ ] Given a user selects their sector (SIC code), when Scope 3 estimation runs, then material Scope 3 categories are identified based on sector profile
- [ ] Given a user enters purchased goods and services spend by category, when the calculation runs, then Category 1 emissions are estimated using spend-based emission factors
- [ ] Given a user enters business travel data (flights, rail, road), when the calculation runs, then Category 6 emissions are calculated using distance-based or spend-based factors
- [ ] Given a user enters employee commuting survey data, when the calculation runs, then Category 7 emissions are calculated
- [ ] Given a user cannot provide Scope 3 data for a non-material category, when the category is marked as not material, then the system accepts the exclusion with documented justification

**Data Requirements**:

- **Inputs**: SIC code, annual procurement spend by category, business travel records, employee commuting data, waste generation data, upstream/downstream transport data
- **Outputs**: tCO2e by Scope 3 category, materiality assessment, data quality score per category
- **Validations**: Material categories cannot be excluded without justification; spend data must sum to a reasonable proportion of total turnover

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-7 (emissions factor management)

---

#### FR-4: Carbon Intensity Normalisation and Sector Benchmarking

**Description**: The system must produce normalised carbon intensity scores (tCO2e per GBP million revenue) and compare these against sector benchmarks derived from aggregated calculator data and published industry averages.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a completed calculation, when normalisation runs, then the system produces tCO2e per GBP million revenue
- [ ] Given sufficient sector data exists (minimum 30 suppliers per SIC code), when benchmarking runs, then the supplier is positioned against sector quartiles (top 25%, median, bottom 25%)
- [ ] Given insufficient sector data, when benchmarking is attempted, then the system displays "insufficient data for benchmarking" and uses published industry averages as proxy

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: Carbon Reduction Plan Generation

**Description**: The system must generate a PPN 06/21 compliant Carbon Reduction Plan document from the calculation outputs, including baseline emissions, reduction targets, and action plan template.

**Relates To**: BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given a completed calculation, when the user requests a Carbon Reduction Plan, then the system generates a document meeting PPN 06/21 requirements
- [ ] The generated plan includes: organisational boundary, baseline year emissions, current year emissions, reduction targets, planned reduction actions
- [ ] The plan is downloadable as PDF and accessible as an online page

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-6: Supplier Registration and Authentication

**Description**: The system must provide secure supplier registration and authentication, linking supplier accounts to Companies House registration numbers for identity verification.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a supplier registers with a Companies House number, when validation runs, then the system verifies the company exists via Companies House API
- [ ] Given a registered supplier returns, when they authenticate, then they access their previous calculations and can update them
- [ ] Multi-factor authentication required for all supplier accounts

**Priority**: MUST_HAVE

**Complexity**: LOW

---

#### FR-7: Emissions Factor Management

**Description**: The system must manage versioned sets of BEIS/DESNZ GHG Conversion Factors, supporting automated ingestion, version control, and the ability to recalculate historical submissions with updated factors.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given DESNZ publishes new conversion factors, when the update process runs, then factors are ingested from the published machine-readable format within 5 working days
- [ ] Given a factor set is versioned, when a historical calculation is viewed, then the system shows which factor version was used
- [ ] Given a new factor set is ingested, when regression testing runs, then all reference calculations are validated against known-good results
- [ ] The system maintains at least 5 years of historical factor sets

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-8: Calculation Audit Trail

**Description**: The system must maintain a complete, immutable audit trail of every calculation, including inputs, emissions factors applied, methodology version, and resulting outputs.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a calculation is completed, when the audit trail is queried, then every input value, emissions factor, and intermediate calculation step is retrievable
- [ ] Audit trail entries are immutable — completed calculations cannot be modified, only superseded by new versions
- [ ] Audit trail supports export for independent verification

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-9: Procurement Integration API

**Description**: The system must expose a RESTful API providing normalised carbon scores, sector benchmarks, and calculation metadata for consumption by the Sustainable Procurement Portal (Project 004) and other authorised government systems.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given an authorised system requests a supplier's carbon score, when the API is called with the supplier identifier, then the API returns normalised carbon intensity, sector benchmark position, and calculation date
- [ ] API uses OAuth 2.0 for authentication and authorisation
- [ ] API versioned (v1) with documented backward compatibility policy
- [ ] API specification published as OpenAPI 3.0

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-4 (normalisation)

---

#### FR-10: Guided SME Calculation Workflow

**Description**: The system must provide a guided, step-by-step calculation workflow for SME users, with contextual help, estimation tools, and sector-specific templates that enable completion using readily available business data.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an SME user starts a calculation, when they select their sector, then the system pre-selects relevant Scope 3 categories and provides sector-appropriate estimation tools
- [ ] Given a user does not know their exact energy consumption, when they use the estimation tool, then the system estimates consumption from annual energy spend and average tariff rates
- [ ] Contextual help tooltips explain every term (Scope 1, CO2e, emissions factor, etc.) in plain English
- [ ] Progress indicator shows completion percentage and estimated remaining time

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Calculation Response Time

**Requirement**: Carbon calculations must complete within defined latency targets.

- Scope 1 and 2 calculation: < 3 seconds (95th percentile)
- Full Scope 1, 2, and 3 calculation: < 10 seconds (95th percentile)
- API carbon score retrieval: < 500ms (95th percentile)

**Load Conditions**: 500 concurrent users during peak procurement submission periods

**Priority**: HIGH

---

#### NFR-P-2: Throughput

**Requirement**: System must handle 1,000 concurrent calculation sessions and 100 API requests per second during peak procurement submission windows (typically quarter-end).

**Scalability**: Must scale horizontally to support 3x growth over 3 years (15,000 registered suppliers).

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Authentication and Access Control

**Requirement**: All users must authenticate via GOV.UK One Login. Supplier data accessible only to the owning supplier and authorised government procurement systems.

**Multi-Factor Authentication**: Required for all accounts.

**Session Management**: 30-minute inactivity timeout; 8-hour absolute session timeout.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Data Encryption

**Requirement**: All data encrypted in transit (TLS 1.3+) and at rest (AES-256). Supplier commercial data classified as OFFICIAL-SENSITIVE (Commercial).

**Priority**: CRITICAL

---

#### NFR-SEC-3: Environmental Data Integrity

**Requirement**: Calculation audit trails must be tamper-evident using cryptographic hash chains. Completed calculations cannot be modified — only superseded by new versions.

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: GHG Protocol Compliance

**Requirement**: The calculation engine must implement the GHG Protocol Corporate Standard (Revised Edition, 2015), the GHG Protocol Scope 2 Guidance (2015), and the GHG Protocol Corporate Value Chain (Scope 3) Standard (2011).

**Priority**: CRITICAL

---

#### NFR-C-2: UK GDPR and Data Protection

**Requirement**: Full compliance with UK GDPR and Data Protection Act 2018. DPIA required before launch. Personal data (supplier contact details) processed under legitimate interest basis; commercial emissions data processed under public task basis.

**Priority**: CRITICAL

---

#### NFR-C-3: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance. Service must be usable with screen readers, keyboard navigation, and high contrast mode. Complex calculation interfaces must have accessible alternatives.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: SME Usability Target

**Requirement**: An SME Operations Manager with no environmental expertise must be able to complete a Scope 1 and 2 carbon footprint calculation within 2 hours using only readily available business data (energy bills, fuel receipts, vehicle records).

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Integration with BEIS/DESNZ GHG Conversion Factors

**Purpose**: Ingest and maintain current emissions factors for all calculation categories.

**Integration Type**: Batch file ingestion (annual, with automated monitoring for publication)

**Data Exchanged**:

- **From DESNZ to Calculator**: Complete emissions factor dataset (1,000+ factors across energy, transport, waste, materials)
- **Format**: Machine-readable (CSV or JSON, as published by DESNZ)

**Priority**: CRITICAL

---

### INT-2: Integration with Sustainable Procurement Portal (Project 004)

**Purpose**: Provide normalised carbon scores for procurement evaluation.

**Integration Type**: Real-time API (RESTful)

**Data Exchanged**:

- **From Calculator to Portal**: Normalised carbon intensity score, sector benchmark position, calculation date, data quality score, Scope 1/2/3 breakdown
- **From Portal to Calculator**: Supplier identifier lookup

**Authentication**: OAuth 2.0 with mutual TLS

**SLA**: 99.9% availability during procurement submission windows; < 500ms response time

**Priority**: MUST_HAVE

---

### INT-3: Integration with Companies House API

**Purpose**: Verify supplier identity during registration; retrieve SIC codes for sector classification.

**Integration Type**: Real-time API

**Data Exchanged**:

- **From Companies House to Calculator**: Company name, registration number, SIC codes, registered address, company status

**Priority**: MUST_HAVE

---

### INT-4: Integration with GOV.UK One Login

**Purpose**: Provide secure authentication for supplier users.

**Integration Type**: OIDC/OAuth 2.0

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Supplier Profile

**Description**: Registered supplier organisation with identity, sector, and financial data.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| supplier_id | UUID | Yes | Unique identifier | Primary key |
| companies_house_number | String(8) | Yes | Companies House registration | Validated via API |
| organisation_name | String(255) | Yes | Legal entity name | From Companies House |
| sic_codes | Array[String] | Yes | Standard Industrial Classification | From Companies House |
| annual_revenue_gbp | Decimal | Yes | Annual revenue for normalisation | Positive, > 0 |
| employee_count | Integer | Yes | Number of employees | Positive |
| reporting_year | String(7) | Yes | Financial year (e.g., 2025/26) | Format validated |

**Data Classification**: OFFICIAL-SENSITIVE (Commercial)

**Data Retention**: Active while supplier account exists; anonymised 7 years after last activity

---

#### Entity 2: Carbon Calculation

**Description**: A completed emissions calculation for a specific supplier and reporting period.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| calculation_id | UUID | Yes | Unique identifier | Primary key |
| supplier_id | UUID | Yes | Owning supplier | Foreign key |
| reporting_year | String(7) | Yes | Reporting period | Format validated |
| factor_set_version | String(10) | Yes | Emissions factor version used | Must exist |
| scope_1_tco2e | Decimal | Yes | Total Scope 1 emissions | >= 0 |
| scope_2_location_tco2e | Decimal | Yes | Scope 2 location-based | >= 0 |
| scope_2_market_tco2e | Decimal | Yes | Scope 2 market-based | >= 0 |
| scope_3_tco2e | Decimal | Yes | Total Scope 3 emissions | >= 0 |
| total_tco2e | Decimal | Yes | Total emissions | Sum of scopes |
| carbon_intensity | Decimal | Yes | tCO2e per GBP M revenue | Calculated |
| data_quality_score | Enum | Yes | Overall data quality | measured/estimated/mixed |
| status | Enum | Yes | Calculation status | draft/completed/superseded |
| completed_at | Timestamp | No | Completion timestamp | Set on completion |

**Data Volume**: 5,000 Year 1; 15,000 Year 3

**Data Classification**: OFFICIAL-SENSITIVE (Commercial)

**Data Retention**: 7 years from calculation date (aligned with financial audit requirements)

---

#### Entity 3: Emissions Factor Set

**Description**: A versioned collection of BEIS/DESNZ GHG Conversion Factors.

**Data Volume**: ~1,000 factors per annual set; 5+ years maintained

**Data Classification**: OFFICIAL (public data)

**Data Retention**: Indefinite (required for historical calculation reproduction)

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with GOV.UK One Login for authentication (mandated for new government services)

**TC-2**: Must deploy to UK sovereign cloud infrastructure (UK GDPR data residency)

**TC-3**: Must use BEIS/DESNZ published emissions factors as the sole authoritative source (no third-party factor databases)

### Business Constraints

**BC-1**: Launch must align with the next PPN 06/21 reporting cycle (Q4 2026)

**BC-2**: Total programme budget capped at GBP 4.5M over 3 years

**BC-3**: Service must be free for suppliers to use (funded by DESNZ, not supplier fees)

### Assumptions

**A-1**: DESNZ will publish GHG Conversion Factors in a machine-readable format by 2026 (currently Excel only)

**A-2**: Companies House API will remain available and free for government services

**A-3**: SME suppliers have access to their energy bills and vehicle fuel records (not specialist monitoring equipment)

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Supplier calculations completed | 0 | 5,000 | 12 months post-launch | Service analytics |
| SME proportion of completions | 0% | 60% | 12 months post-launch | Organisation size analysis |
| Procurement spend with carbon data | <5% | 50% | 18 months post-launch | CCS spend data matching |
| Contracting authorities using scores | 0% | 80% | 24 months post-launch | CCS framework data |
| Average SME completion time | N/A | <2 hours | 6 months post-launch | Session analytics |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.5% | Uptime monitoring |
| Calculation response time (p95) | < 10 seconds | APM tooling |
| API response time (p95) | < 500ms | APM tooling |
| Factor update turnaround | < 5 working days | Process log |
| GHG Protocol validation accuracy | 100% (50 test cases) | Validation test suite |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| BEIS/DESNZ machine-readable factors | Factors published in machine-readable format | DESNZ Climate Science | Q3 2026 | At Risk | HIGH — manual ingestion required |
| GOV.UK One Login integration | Authentication service available for new services | GDS | Q3 2026 | On Track | HIGH — custom auth needed |
| Sustainable Procurement Portal API | API specification agreed for integration | CCS / Project 004 | Q4 2026 | On Track | MEDIUM — delayed integration |
| Companies House API | Continued free API access | Companies House | Ongoing | On Track | LOW — alternative verification |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | SMEs find tool too complex, low adoption | MEDIUM | HIGH | Extensive user research, estimation tools, plain language | Product Manager |
| R-2 | Methodology challenged by NGOs/academia | MEDIUM | HIGH | Publish methodology, commission independent review | Chief Scientific Adviser |
| R-3 | Scope 3 data quality too poor for meaningful scoring | HIGH | MEDIUM | Tiered approach, data quality scoring, sector estimation | Product Manager |
| R-4 | BEIS/DESNZ factors not available in machine-readable format | MEDIUM | MEDIUM | Automated Excel parsing as fallback, lobby for format change | Service Owner |
| R-5 | Procurement Portal integration delayed | LOW | MEDIUM | Calculator operates standalone until integration ready | CCS Integration Lead |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Executive Sponsor | [ ] Approved | | |
| Chief Scientific Adviser | Methodology Authority | [ ] Approved | | |
| CCS Integration Lead | Procurement Integration | [ ] Approved | | |
| Security Lead | Security Review | [ ] Approved | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GHG Protocol Corporate Standard | Standard | ghgprotocol.org | Scope 1/2/3 methodology | N/A |
| GHG Protocol Scope 2 Guidance | Standard | ghgprotocol.org | Location/market-based methods | N/A |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plan requirements | N/A |
| BEIS/DESNZ GHG Conversion Factors 2025 | Data | GOV.UK | UK emissions factors | N/A |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | SDG 12 Programme | Stakeholder drivers and goals | `projects/001-carbon-footprint-calculator/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Carbon Footprint Calculator (Project 001)
**Model**: Claude Opus 4.6
