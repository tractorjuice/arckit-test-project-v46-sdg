# Project Requirements: Fuel Poverty Intervention Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Fuel Poverty Intervention Tracker (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Fuel Poverty Programme, DESNZ |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ, Ofgem, Energy suppliers, HMRC, DWP, DLUHC, NEA, Local Authorities |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies requirements for the Fuel Poverty Intervention Tracker — a system to identify fuel-poor households using linked LILEE data (Low Income Low Energy Efficiency), coordinate interventions (ECO4, Warm Home Discount, local schemes), and track progress toward the statutory fuel poverty target. An estimated 3.17 million households in England are fuel-poor. The tracker links income data (HMRC/DWP), energy performance data (EPC register), and intervention records to improve targeting accuracy from approximately 40% to 80%.

---

## Executive Summary

### Business Context

The UK government has a statutory target under the Fuel Poverty (England) Regulations 2014 to ensure that as many fuel-poor homes as reasonably practicable achieve EPC Band C by 2030. Progress is tracked using the LILEE (Low Income Low Energy Efficiency) metric, which requires linking household income data with dwelling energy efficiency data. Currently, fuel poverty statistics are published with a 2-3 year lag, ECO4 interventions frequently reach non-fuel-poor households, and an estimated 30% of eligible households miss out on the Warm Home Discount because they do not apply.

The Fuel Poverty Intervention Tracker addresses these gaps by linking cross-departmental data to identify fuel-poor households, directing interventions to those most in need, and providing real-time tracking of progress toward the statutory target.

### Objectives

- Identify fuel-poor households using linked LILEE data with 80% accuracy
- Improve ECO4 targeting — 60% of interventions reaching verified fuel-poor homes (currently ~35%)
- Achieve 90% auto-enrolment for Warm Home Discount eligible households
- Provide a quarterly fuel poverty dashboard replacing the current 2-3 year data lag
- Enable local authorities to identify fuel-poor households in their area for targeted outreach

### Expected Outcomes

- 80% targeting accuracy for fuel poverty interventions
- 200,000 additional fuel-poor households receiving ECO4 measures over 5 years
- GBP 150M energy bill savings for fuel-poor households through better-targeted interventions
- Real-time fuel poverty measurement for the first time
- 30% reduction in the fuel poverty gap (difference between required and actual energy costs)

### Project Scope

**In Scope**:

- LILEE identification engine — linking income (HMRC/DWP), EPC (DLUHC), and energy consumption data
- ECO4 intervention tracking (measures installed, pre/post EPC, household eligibility)
- Warm Home Discount auto-enrolment data matching
- Local authority fuel poverty mapping (LSOA-level data, household-level with data sharing basis)
- National and regional fuel poverty dashboard
- Intervention referral and coordination for energy suppliers and local authorities

**Out of Scope**:

- Energy tariff regulation (Ofgem scope)
- Smart meter rollout management
- New energy efficiency scheme design or funding
- Devolved administration fuel poverty programmes (Scotland, Wales have separate schemes)
- Energy supplier billing systems

---

## Business Requirements

### BR-001: LILEE Fuel Poverty Identification

**Description**: The system must link household income data (from HMRC/DWP), dwelling energy performance data (EPC register), and energy consumption data to identify households meeting the LILEE fuel poverty definition.

**Rationale**: Accurate identification is the foundation for all interventions. Current targeting relies on proxy indicators (benefit receipt, postcode) that miss many fuel-poor households and include many non-fuel-poor ones (ref: SD-1, SD-2).

**Success Criteria**:

- 80% accuracy in fuel poverty identification (validated against English Housing Survey sample)
- Coverage of 90% of English dwellings (some properties lack EPCs)
- Quarterly refresh of income and EPC data

**Priority**: MUST_HAVE

**Stakeholder**: DESNZ Minister (SD-1), Ofgem (SD-2)

---

### BR-002: ECO4 Targeting and Tracking

**Description**: The system must provide energy suppliers with a prioritised list of eligible fuel-poor properties for ECO4 interventions, track measures installed, and verify that interventions reach the intended target group.

**Rationale**: Currently ~35% of ECO4 interventions reach the most fuel-poor homes. Better targeting would improve scheme effectiveness and value for money (ref: SD-2, SD-3).

**Success Criteria**:

- 60% of ECO4 interventions targeting verified fuel-poor homes (EPC Band D or below, LILEE-qualifying)
- Real-time tracking of measures installed against fuel poverty priority list
- Pre/post intervention EPC comparison for impact measurement

**Priority**: MUST_HAVE

**Stakeholder**: Ofgem (SD-2), Energy suppliers (SD-3)

---

### BR-003: Warm Home Discount Auto-Enrolment

**Description**: The system must match benefit receipt data (DWP) with energy supplier customer data to automatically enrol eligible households in the Warm Home Discount scheme without requiring them to apply.

**Rationale**: 30% of eligible households miss the WHD because they do not apply. Auto-enrolment ensures the most vulnerable receive support (ref: SD-5).

**Success Criteria**:

- 90% auto-enrolment rate for eligible households
- Data matching completed annually before the WHD payment window
- Disputes and corrections processed within 28 days

**Priority**: MUST_HAVE

**Stakeholder**: Fuel-poor households (SD-5), DESNZ

---

### BR-004: Local Authority Fuel Poverty Mapping

**Description**: The system must provide local authorities with fuel poverty data for their area at LSOA (Lower Layer Super Output Area) level, enabling targeted outreach and local scheme coordination.

**Rationale**: Local authorities have statutory energy efficiency duties but lack the data to identify fuel-poor households. Area-level data enables targeted campaigns and referrals (ref: SD-4).

**Success Criteria**:

- LSOA-level fuel poverty data available to all English local authorities
- Data updated quarterly
- Household-level identification available where data sharing agreement permits

**Priority**: MUST_HAVE

**Stakeholder**: Local Authority energy officers (SD-4)

---

### BR-005: Real-Time Fuel Poverty Dashboard

**Description**: The system must provide a national and regional dashboard showing fuel poverty prevalence, intervention coverage, progress toward the statutory target, and trend analysis.

**Rationale**: Current fuel poverty statistics are 2-3 years out of date. Real-time data enables evidence-based policy and accountability (ref: SD-1, SD-6).

**Success Criteria**:

- Dashboard updated quarterly with data no more than 3 months old
- National, regional, and local authority breakdowns
- Trend analysis showing progress toward 2030 EPC Band C target
- Published data accessible to researchers and advocacy organisations (anonymised)

**Priority**: SHOULD_HAVE

**Stakeholder**: DESNZ Minister (SD-1), NEA (SD-6)

---

## Functional Requirements

### FR-001: Cross-Departmental Data Linkage Engine

**Description**: The system must securely link datasets from HMRC (household income), DWP (benefit receipt), DLUHC (EPC register), and Ofgem (energy consumption/supplier data) to calculate LILEE fuel poverty status per dwelling.

**Acceptance Criteria**:

- [ ] Given household income data and EPC rating, when the LILEE calculation is applied, then the system correctly identifies whether the household is fuel-poor according to the statutory definition
- [ ] Given a dwelling with no EPC, when fuel poverty status is assessed, then the system flags as "data incomplete" and uses modelled estimates based on property type and age
- [ ] Edge case: If income data and EPC data cannot be linked (address mismatch), the system uses probabilistic matching with a confidence score and flags for manual review

**Data Requirements**:

- **Inputs**: Household income (HMRC self-assessment and PAYE), benefit receipt (DWP), EPC rating (DLUHC register), property type and age (VOA), energy supplier/tariff (Ofgem)
- **Outputs**: Fuel poverty flag (yes/no/data incomplete), fuel poverty gap (GBP), EPC rating, priority score for intervention
- **Validations**: LILEE calculation validated against English Housing Survey methodology

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Data sharing agreements with HMRC, DWP, DLUHC, Ofgem under Digital Economy Act 2017

---

### FR-002: ECO4 Eligible Property List

**Description**: The system must generate a prioritised list of ECO4-eligible fuel-poor properties, ranked by fuel poverty gap severity, suitable measures, and geographic clustering (for installer efficiency).

**Acceptance Criteria**:

- [ ] Given a fuel-poor property with EPC Band D or below, when the system generates the priority list, then it includes recommended measures (cavity wall, loft, solid wall insulation, boiler replacement, heat pump) based on EPC recommendations
- [ ] Given an energy supplier's ECO4 obligation, when they query the system, then they receive a prioritised list of eligible properties in their designated area with pre-verified eligibility

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-003: Intervention Recording and Tracking

**Description**: Energy suppliers and local authorities must record completed interventions (measure type, cost, installer, date) linked to the fuel-poor property record.

**Acceptance Criteria**:

- [ ] Given a completed ECO4 intervention, when the supplier records it, then the property's fuel poverty status is updated with the expected EPC improvement
- [ ] Given a post-intervention EPC assessment, when the new rating is lodged, then the system calculates the actual fuel poverty gap change
- [ ] Edge case: If the intervention does not improve the EPC as expected (poor installation quality), the system flags for Ofgem compliance review

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-004: Warm Home Discount Data Matching

**Description**: The system must match DWP benefit data with energy supplier customer data to identify WHD-eligible households and automate enrolment.

**Acceptance Criteria**:

- [ ] Given a household receiving qualifying benefits, when the annual data match is run, then eligible households are flagged to their energy supplier for automatic WHD credit
- [ ] Given a household that has changed energy supplier since last match, when the new supplier data is available, then the match is updated

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-005: Local Authority Dashboard

**Description**: Each local authority must be able to view fuel poverty data for their area, including LSOA-level maps, property-level data (where data sharing permits), intervention coverage, and gap analysis.

**Acceptance Criteria**:

- [ ] Given a local authority user, when they access their dashboard, then they see a map of fuel poverty prevalence at LSOA level with colour-coded severity
- [ ] Given LSOA data, when drilling down, then the user sees the number of fuel-poor homes, intervention coverage, and remaining gap
- [ ] Edge case: If the local authority does not have a data sharing agreement for household-level data, then only aggregate LSOA data is shown

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-SEC-001: Data Protection and Linkage Governance

**Requirement**: All cross-departmental data linkage must comply with the Digital Economy Act 2017, UK GDPR, and Data Protection Act 2018. Data minimisation applied — linked dataset contains only the minimum fields required for LILEE calculation. No raw income data stored — only income band flags. Independent DPIA reviewed by ICO.

**Data Governance**:

- Data linkage performed in a secure, accredited research environment (ONS Secure Research Service model)
- Only aggregated outputs leave the secure environment (individual records do not)
- Data sharing agreements reviewed and renewed annually
- Data Protection Impact Assessment completed before any data linkage
- Household-level data shared with local authorities only under specific data sharing powers

**Priority**: CRITICAL

---

### NFR-SEC-002: Secure Data Processing Environment

**Requirement**: All data linkage and processing must occur within an accredited secure environment meeting ONS Secure Research Service standards (ISO 27001, UK Government security policy). No data leaves the environment except as approved aggregate outputs.

**Priority**: CRITICAL

---

### NFR-P-001: Data Processing Performance

**Requirement**: Full LILEE data linkage across approximately 25 million English dwellings must complete within 48 hours per quarterly refresh cycle.

**Priority**: HIGH

---

### NFR-A-001: Dashboard Availability

**Requirement**: National and local authority dashboards available 99.5% during business hours. Data refresh quarterly.

**Priority**: MEDIUM

---

### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA for all dashboards and user interfaces. Plain language explanations of fuel poverty metrics for non-technical users.

**Priority**: HIGH

---

## Integration Requirements

### INT-001: HMRC — Household Income Data

**Purpose**: Income data (banded, not exact amounts) for LILEE calculation.

**Integration Type**: Secure batch data transfer under Digital Economy Act 2017 data sharing agreement.

**Data Exchanged**: Anonymised household income band linked by address (UPRN).

**SLA**: Annual data provision with quarterly supplementary updates.

**Owner**: HMRC

**Priority**: CRITICAL

---

### INT-002: DWP — Benefit Receipt Data

**Purpose**: Identify households receiving qualifying benefits for WHD auto-enrolment and ECO4 eligibility.

**Integration Type**: Secure batch data transfer under existing WHD data sharing powers.

**Data Exchanged**: Benefit receipt flags (yes/no per qualifying benefit) linked by NINO/address.

**Owner**: DWP

**Priority**: CRITICAL

---

### INT-003: DLUHC — EPC Register

**Purpose**: Energy Performance Certificate ratings for all assessed English dwellings.

**Integration Type**: Bulk data extract from Open EPC data and supplementary register data.

**Data Exchanged**: EPC rating (A-G), property type, age, recommended measures, assessment date, UPRN.

**Owner**: DLUHC

**Priority**: CRITICAL

---

### INT-004: Ofgem — Energy Supplier and ECO4 Data

**Purpose**: Energy supplier customer data for WHD matching; ECO4 measure data for intervention tracking.

**Integration Type**: Secure batch transfer (supplier data); API for ECO4 measure recording.

**Owner**: Ofgem

**Priority**: HIGH

---

### INT-005: VOA — Property Data

**Purpose**: Property type, age, and council tax band for modelled estimates where EPC data is missing.

**Integration Type**: Bulk data extract.

**Owner**: Valuation Office Agency

**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: All data linkage must occur within an ONS SRS-equivalent accredited secure research environment.

**TC-2**: Individual-level linked data must not leave the secure environment — only approved aggregate outputs.

**TC-3**: UK sovereign infrastructure for all data processing and storage.

### Business Constraints

**BC-1**: Data sharing agreements must be in place with HMRC, DWP, DLUHC, and Ofgem before system development can commence — these are on the critical path.

**BC-2**: Budget envelope of GBP 35M over 5 years.

**BC-3**: Energy suppliers cannot be compelled to use the system for ECO4 targeting (but Ofgem can adjust scoring criteria to incentivise it).

### Assumptions

**A-1**: HMRC will agree to data sharing under Digital Economy Act 2017 for fuel poverty targeting (public interest determination required).

**A-2**: EPC data is available for at least 60% of English dwellings (coverage is improving but incomplete).

**A-3**: Energy suppliers will use the system if it reduces their ECO4 customer identification costs.

**A-4**: Probabilistic address matching between HMRC, DWP, and EPC datasets achieves 85%+ match rate using UPRN.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Fuel poverty identification accuracy | ~40% (proxy targeting) | 80% (LILEE-validated) | Year 2 |
| ECO4 interventions reaching fuel-poor homes | ~35% | 60% | Year 3 |
| WHD auto-enrolment rate | 70% | 90% | Year 2 |
| Fuel poverty data lag | 2-3 years | 3 months (quarterly) | Year 2 |
| Local authority dashboard coverage | 0 | 100% of English LAs | Year 2 |
| Fuel-poor households receiving interventions per year | 350,000 | 550,000 | Year 3 |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Status | Impact if Delayed |
|------------|-------------|-------|--------|-------------------|
| HMRC data sharing agreement | Digital Economy Act public interest determination | HMRC | At Risk | CRITICAL — blocks LILEE calculation |
| DWP data sharing agreement | Benefit receipt data for WHD matching | DWP | On Track | HIGH — blocks WHD auto-enrolment |
| EPC register data quality | Coverage and accuracy of EPC data | DLUHC | On Track | MEDIUM — modelled estimates as fallback |
| Secure research environment | ONS SRS or equivalent accreditation | ONS/DESNZ | On Track | CRITICAL — blocks all data linkage |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation |
|---------|-------------|-------------|--------|------------|
| R-001 | HMRC data sharing not agreed | MEDIUM | CRITICAL | Early engagement, Ministerial support, legal advice on DEA powers |
| R-002 | EPC data coverage below 60% | MEDIUM | HIGH | Modelled estimates for uncertified properties using VOA property data |
| R-003 | Address matching failure rate too high | MEDIUM | HIGH | UPRN-based matching, probabilistic matching algorithms, manual review queue |
| R-004 | Energy suppliers do not adopt the system | MEDIUM | MEDIUM | Ofgem adjusts ECO4 scoring to incentivise tracker use |
| R-005 | Privacy and civil liberties concerns about linked data | HIGH | HIGH | ICO engagement, independent DPIA, strict data minimisation, aggregate-only outputs |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| DESNZ Permanent Secretary | Accounting Officer | [ ] Approved | PENDING |
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| Ofgem | Regulatory Partner | [ ] Approved | PENDING |
| ICO | Data Protection Oversight | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fuel Poverty Intervention Tracker
**Model**: Claude Opus 4.6
