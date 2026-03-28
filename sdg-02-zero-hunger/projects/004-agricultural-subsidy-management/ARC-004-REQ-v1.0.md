# Project Requirements: Agricultural Subsidy Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Agricultural Subsidy Management (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DEFRA Environmental Land Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Rural Payments Agency, Natural England, NFU |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Agricultural Subsidy Management platform covering ELM scheme application, agreement management, payment processing, environmental outcome monitoring, and national reporting. Traceable to ARC-004-STKE-v1.0 and aligned with ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

The UK's departure from the EU Common Agricultural Policy (CAP) enabled a fundamental shift in agricultural support from area-based direct payments (Basic Payment Scheme) to outcomes-based Environmental Land Management (ELM) schemes. The Agriculture Act 2020 establishes three ELM schemes:

- **Sustainable Farming Incentive (SFI)**: Accessible to all farmers, pays for sustainable farming actions (soil health, integrated pest management, hedgerow management)
- **Countryside Stewardship (CS)**: Mid-tier and higher-tier environmental management, paying for habitat creation, flood risk management, and water quality improvement
- **Landscape Recovery (LR)**: Large-scale, landscape-level environmental projects (peatland restoration, species reintroduction, natural flood management)

BPS direct payments are being progressively reduced through agricultural transition. Approximately 100,000 farm holdings in England received BPS; the target is for 80% to participate in at least one ELM scheme by Q4 2028. Total annual ELM spending is projected at £2.4B by 2028.

### Objectives

- Deliver a digital service for SFI, CS, and LR applications processing 100,000+ farm holdings
- Achieve 99.9% payment accuracy and 100% compliance with 30-day government payment SLA
- Provide a simple, farmer-friendly application process accessible on mobile devices in rural areas
- Support environmental outcome monitoring through satellite/remote sensing integration
- Enable RPA to manage the BPS-to-ELM transition without payment gaps

### Expected Outcomes

- 80,000+ farm holdings with active ELM agreements by Q4 2028
- £2.4B annual payments processed accurately and on time
- Application completion time < 2 hours for standard SFI actions (vs. current BPS average of 6+ hours)
- 90% of environmental monitoring conducted via remote sensing, minimising farmer burden
- Positive NAO value-for-money assessment

### Project Scope

**In Scope**:

- SFI, CS, and LR scheme application and agreement management
- Payment calculation engine (action-based, outcome-based, capital items)
- Land parcel management integrated with Rural Land Register
- Environmental outcome monitoring (satellite, remote sensing, field inspection)
- Farmer and agent portals (web and mobile)
- RPA caseworker portal for agreement management and inspections
- Payment processing and reconciliation
- National reporting and analytics
- API for National Food Strategy Dashboard (Project 005) and Food Supply Chain Platform (Project 001)

**Out of Scope**:

- BPS legacy payment processing (managed through existing RPA systems until wind-down)
- Devolved nation agricultural schemes (Scotland, Wales, Northern Ireland)
- Market support schemes (e.g., fruit and vegetables, school milk)
- Farm business grants and capital investment schemes (separate DEFRA programme)

---

## Business Requirements

### BR-001: ELM Scheme Application Processing

**Description**: The platform must enable farmers and their agents to apply for SFI, CS, and LR scheme actions through a digital service, with application processing completing within defined SLAs.

**Rationale**: Replacing BPS with ELM requires a new application system. The current system processes approximately 85,000 BPS claims annually; ELM is expected to process 100,000+ applications across three schemes.

**Success Criteria**:

- Standard SFI application completed in < 2 hours by farmer
- Application processing time: SFI < 5 working days, CS < 20 working days, LR < 40 working days
- Application completion rate > 90% (applications started vs submitted)
- Agent delegation supported for all scheme types

**Priority**: MUST_HAVE

---

### BR-002: Accurate and Timely Payment Processing

**Description**: The platform must calculate and process payments for all ELM schemes with 99.9% accuracy and 100% compliance with the 30-day government payment SLA.

**Rationale**: The 2015 BPS payment crisis caused severe financial hardship for farmers and political damage. Payment reliability is the single most critical success factor (Stakeholder Driver SD-2).

**Success Criteria**:

- Payment accuracy > 99.9% (validated against manual sample)
- 100% of payments made within 30-day SLA from valid claim
- Payment value reconciliation within +/-0.01% of total scheme budget
- Overpayment recovery process established for error correction

**Priority**: MUST_HAVE

---

### BR-003: Simple Farmer Experience

**Description**: The platform must provide a farmer-friendly digital service that is significantly simpler than the BPS experience, accessible on mobile devices, and usable by people with low digital literacy.

**Rationale**: Farmer scepticism from BPS IT failures and concern about digital exclusion of older farmers. 30% of farm holdings managed by people over 65 (Stakeholder Driver SD-3).

**Success Criteria**:

- GDS Service Standard assessment passed at all stages
- User satisfaction score > 7/10 (vs BPS ~4/10)
- Mobile-responsive design functional on 3G connections
- Assisted digital support available for farmers unable to use the online service

**Priority**: MUST_HAVE

---

### BR-004: Environmental Outcome Monitoring

**Description**: The platform must support monitoring and verification of environmental outcomes from ELM actions using a combination of remote sensing and field inspection.

**Rationale**: Outcome-based payments require evidence of environmental delivery. Without monitoring, public money cannot be shown to deliver public goods (Stakeholder Driver SD-4).

**Success Criteria**:

- 90% of land-based actions monitored via remote sensing (satellite/aerial imagery)
- 10% annual field inspection sample for ground-truth validation
- Farmer self-reporting for actions not visible from remote sensing
- Environmental outcome indicators trackable at national and regional level

**Priority**: MUST_HAVE

---

### BR-005: BPS-to-ELM Transition Management

**Description**: The platform must support the managed transition from BPS to ELM, ensuring no farmer experiences a payment gap during the changeover.

**Rationale**: BPS direct payments are being progressively reduced. Farmers need to transition to ELM to maintain income. Any gap could cause farm business failures (Stakeholder Driver SD-3).

**Success Criteria**:

- Transition timeline and income impact modelling available to farmers
- Concurrent BPS delinked payments and ELM payments managed without conflict
- Farmer income continuity verified through payment data analysis

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Farmer (Direct Applicant)

- **Role**: Owner-occupier or tenant farmer, managing 50-500 hectares
- **Goals**: Apply for SFI actions, track agreement status, receive payments on time
- **Pain Points**: Complex forms, poor mobile experience in rural areas, unclear eligibility criteria
- **Technical Proficiency**: Low to Medium (age range 30-75, 30% over 65)

#### Persona 2: Farm Agent

- **Role**: Agricultural consultant or land agent acting on behalf of multiple farmers
- **Goals**: Manage applications for 50-200 clients efficiently, track payments, advise on scheme eligibility
- **Pain Points**: Cannot see all client agreements in one view, delegation permissions complex
- **Technical Proficiency**: Medium to High

#### Persona 3: RPA Caseworker

- **Role**: RPA agreement manager processing applications, managing inspections, resolving payment issues
- **Goals**: Process applications accurately and on time, manage inspection scheduling, resolve farmer queries
- **Pain Points**: Multiple legacy systems, manual workarounds, complex calculation rules
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-001: Scheme Application Portal

**Description**: The system must provide a web-based application portal enabling farmers and agents to apply for SFI, CS, and LR actions.

**Acceptance Criteria**:

- [ ] Given an authenticated farmer, when starting an application, then eligible scheme actions are displayed based on their land holdings
- [ ] Given land parcels, when displayed for selection, then maps from Rural Land Register are shown with current land use
- [ ] Given a completed application, when submitted, then confirmation is provided with estimated processing time
- [ ] Given a saved partial application, when returned to later, then all entered data is preserved

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: Land Parcel Management

**Description**: The system must integrate with the Rural Land Register to display, select, and manage land parcels for scheme applications.

**Acceptance Criteria**:

- [ ] Given a farmer's holding, when viewing land parcels, then OS mapping with parcel boundaries is displayed
- [ ] Given a land parcel, when selected for an action, then the eligible area is calculated automatically
- [ ] Given overlapping scheme actions on the same parcel, when submitted, then the system validates compatibility
- [ ] Given a boundary change, when notified by RPA, then affected agreements are flagged for review

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-003: Payment Calculation Engine

**Description**: The system must calculate payments for all ELM scheme actions, including per-hectare rates, capital items, and outcome-based payments.

**Acceptance Criteria**:

- [ ] Given an SFI agreement, when payment is due, then the amount is calculated based on agreed actions, rates, and area
- [ ] Given a CS agreement with capital items, when a claim is submitted with evidence, then capital payment is calculated
- [ ] Given an LR agreement with outcome milestones, when a milestone is verified, then milestone payment is released
- [ ] Given payment calculation, when processed, then calculation audit trail is stored for NAO review

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-004: Payment Processing and Reconciliation

**Description**: The system must process payments to farmer bank accounts via BACS, with full reconciliation and audit trail.

**Acceptance Criteria**:

- [ ] Given a calculated payment, when approved by RPA caseworker, then BACS payment file is generated
- [ ] Given a payment, when processed, then payment is made within 30-day SLA from valid claim
- [ ] Given payment reconciliation, when run daily, then all payments are matched to agreements and bank transactions
- [ ] Given a payment error, when detected, then overpayment recovery or underpayment correction is initiated

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-005: Environmental Monitoring Dashboard

**Description**: The system must provide an environmental monitoring dashboard showing outcome indicators from remote sensing and field inspection data.

**Acceptance Criteria**:

- [ ] Given satellite imagery, when processed, then land-use change and vegetation indices are calculated per parcel
- [ ] Given field inspection results, when recorded, then they are linked to the relevant agreement and parcel
- [ ] Given monitoring data, when aggregated nationally, then environmental outcome trends are visible
- [ ] Given a non-compliance finding, when recorded, then payment adjustment is calculated

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-006: Agent Delegation

**Description**: The system must support farm agents managing applications and agreements on behalf of multiple farmers.

**Acceptance Criteria**:

- [ ] Given an agent with delegation authority, when logging in, then a list of all delegating farmers is displayed
- [ ] Given delegation, when granted, then the agent can view and manage agreements but not modify bank details
- [ ] Given a farmer revoking delegation, when processed, then agent access is removed immediately

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-007: RPA Caseworker Portal

**Description**: The system must provide a caseworker portal for RPA staff to process applications, manage inspections, and resolve payment queries.

**Acceptance Criteria**:

- [ ] Given a caseworker, when viewing their queue, then applications are prioritised by SLA deadline
- [ ] Given an application, when reviewed, then the caseworker can approve, reject, or request further information
- [ ] Given an inspection, when scheduled, then the caseworker can assign an inspector and record results
- [ ] Given a payment query, when raised by a farmer, then the caseworker can trace the full payment calculation

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-008: API for Cross-Programme Data Sharing

**Description**: The system must publish agricultural subsidy and land management data via API for Projects 001, 003, and 005.

**Acceptance Criteria**:

- [ ] Given an authorised consumer (Project 005), when requesting subsidy metrics, then aggregated data is returned
- [ ] Given an authorised consumer (Project 001), when requesting agricultural production indicators, then relevant data is shared
- [ ] Given API versioning, when new version released, then previous version available for 6 months

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements

### NFR-P-1: Performance

- Portal page load: < 2 seconds (p95) on 3G connection
- Map rendering: < 5 seconds for 100-parcel holding
- Payment calculation: < 30 seconds per agreement
- Batch payment processing: 100,000 payments processed within 24 hours

**Peak load**: 20,000 concurrent users during SFI application window (January-March)

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% uptime (citizen-facing service tier). Scheduled maintenance only outside farming business hours (weekday evenings, weekends).

**RTO**: 1 hour | **RPO**: 15 minutes

**Priority**: CRITICAL

---

### NFR-SEC-1: Authentication

**Requirement**: Farmers authenticate via Government Gateway or GOV.UK One Login. Agents via Rural Payments Agency agent credentials. RPA staff via DEFRA Azure AD.

**MFA**: Required for all payment-related functions, agent delegation, and RPA access.

**Priority**: CRITICAL

---

### NFR-SEC-2: Financial Controls

**Requirement**: All payment calculations subject to four-eyes principle (caseworker approval). Payments above £50,000 require senior approval. Full audit trail for NAO access.

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility and Digital Inclusion

**Requirement**: WCAG 2.2 Level AA compliance. Mobile-responsive design optimised for rural 3G connectivity. Assisted digital support channel (telephone and face-to-face) for digitally excluded farmers.

**Priority**: CRITICAL

---

## Integration Requirements

#### INT-001: Rural Land Register

**Purpose**: Land parcel data, boundary mapping, and area calculations.

**Integration Type**: Real-time API

**Priority**: MUST_HAVE

---

#### INT-002: OS Data Hub

**Purpose**: Ordnance Survey mapping for land parcel display and geospatial analysis.

**Integration Type**: Real-time API (OS Maps API, OS Features API)

**Priority**: MUST_HAVE

---

#### INT-003: BACS Payment System

**Purpose**: Process farmer payments via BACS Approved Bureau.

**Integration Type**: Batch file transfer (daily BACS submission)

**Priority**: MUST_HAVE

---

#### INT-004: Satellite/Remote Sensing Service

**Purpose**: Environmental monitoring using satellite imagery (Sentinel-2, commercial providers) for land-use verification.

**Integration Type**: Batch data feed (weekly imagery processing)

**Priority**: SHOULD_HAVE

---

#### INT-005: Natural England Designations API

**Purpose**: Retrieve environmental designation data (SSSI, AONB, SAC, SPA) for eligibility and compliance checking.

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Key Data Entities

#### Entity 1: Farm Holding

| Attribute | Type | Required | Description | Classification |
|-----------|------|----------|-------------|---------------|
| holding_id | UUID | Yes | System identifier | OFFICIAL |
| sbi | String(9) | Yes | Single Business Identifier | OFFICIAL-SENSITIVE |
| holding_name | String(255) | Yes | Farm name | OFFICIAL |
| total_area_ha | Decimal | Yes | Total holding area in hectares | OFFICIAL |
| owner_name | String(255) | Yes | Primary owner | OFFICIAL-SENSITIVE |
| bank_sort_code | String(6) | Yes | Payment bank details | OFFICIAL-SENSITIVE |
| bank_account | String(8) | Yes | Payment account number | OFFICIAL-SENSITIVE |

**Data Volume**: 100,000+ holdings

**Data Classification**: OFFICIAL-SENSITIVE (financial data)

---

#### Entity 2: ELM Agreement

| Attribute | Type | Required | Description | Classification |
|-----------|------|----------|-------------|---------------|
| agreement_id | UUID | Yes | Unique agreement identifier | OFFICIAL |
| holding_id | UUID | Yes | Farm holding reference | OFFICIAL |
| scheme | Enum | Yes | SFI / CS / LR | OFFICIAL |
| status | Enum | Yes | Draft / Submitted / Active / Expired / Terminated | OFFICIAL |
| start_date | Date | Yes | Agreement start | OFFICIAL |
| end_date | Date | Yes | Agreement end | OFFICIAL |
| annual_value | Decimal | Yes | Annual payment value | OFFICIAL-SENSITIVE |
| actions | JSON | Yes | List of agreed actions with parcels and rates | OFFICIAL |

**Data Volume**: 150,000+ agreements (some holdings have multiple)

---

## Constraints and Assumptions

**TC-1**: Must integrate with existing RPA systems during BPS transition period (parallel running).

**TC-2**: Must deploy to DEFRA/RPA approved cloud environment.

**TC-3**: Must use Rural Land Register as authoritative source for land parcel data.

**BC-1**: Budget capped at £45M over 5 years (aligned with SR25 allocation for ELM digital delivery).

**BC-2**: Must process first SFI payments through the new platform by Q1 2028.

**BC-3**: Payment accuracy must meet NAO audit standards from day one.

**A-1**: Rural Land Register data is accurate and current (risk: known data quality issues in some regions).

**A-2**: Satellite imagery resolution is sufficient for outcome monitoring of SFI actions (risk: cloud cover in UK limits satellite utility).

**A-3**: Farmers with limited digital literacy can complete applications with agent support or assisted digital channel.

---

## Budget

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Platform development | £18.0M | Application, payment, monitoring |
| RPA integration | £8.0M | Legacy system integration, data migration |
| Land register integration | £4.0M | Geospatial systems, mapping |
| Remote sensing capability | £3.0M | Satellite data, processing pipeline |
| Testing and assurance | £4.0M | Performance, security, payment accuracy testing |
| Training and change management | £2.0M | RPA staff, farmers, agents |
| Infrastructure (5 years) | £4.0M | Cloud hosting |
| Contingency (10%) | £2.0M | Risk buffer |
| **Total** | **£45.0M** | Over 5 years |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| ELM | Environmental Land Management |
| SFI | Sustainable Farming Incentive |
| CS | Countryside Stewardship |
| LR | Landscape Recovery |
| BPS | Basic Payment Scheme (legacy CAP) |
| RPA | Rural Payments Agency |
| SBI | Single Business Identifier (farm holding reference) |
| BACS | Bankers' Automated Clearing Services |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Architecture Principles
- ARC-004-STKE-v1.0 -- Agricultural Subsidy Management Stakeholder Analysis
- Agriculture Act 2020
- NAO BPS Early Review 2015
- DEFRA ELM Policy Design documents

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Agricultural Subsidy Management
**Model**: Claude Opus 4.6
