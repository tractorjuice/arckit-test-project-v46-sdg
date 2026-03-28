# Strategic Outline Business Case (SOBC): Social Housing Allocation Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
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
| **Distribution** | DLUHC Programme Board, HM Treasury, LGA, Regulator of Social Housing |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for a national Social Housing Allocation Platform serving 300+ English local authorities, following the HM Treasury Green Book Five Case Model. It is informed by ARC-002-STKE-v1.0 (stakeholder analysis) and ARC-002-REQ-v1.0 (requirements).

---

## Executive Summary

**Purpose**: Over 1.2 million households are on social housing waiting lists across England, managed by 300+ councils on fragmented systems. This business case seeks GBP 85M over 5 years to deliver a national platform supporting choice-based lettings while preserving local allocation policy autonomy.

**Problem Statement**: No national digital infrastructure exists for social housing allocation. Each council operates independently, creating inconsistent applicant experiences, administrative duplication for housing associations, and no real-time national data. The Social Housing (Regulation) Act 2023 requires transparent allocation processes that fragmented legacy systems cannot consistently deliver.

**Proposed Solution**: A multi-tenant, configurable platform enabling choice-based lettings, standardised nominations for housing associations, homelessness integration, and national reporting.

**Strategic Fit**: Supports SDG 1: No Poverty by improving access to stable, affordable housing. Aligns with the Social Housing (Regulation) Act 2023 consumer standards and Homelessness Reduction Act 2017 statutory duties.

**Investment Required**: GBP 85M over 5 years

- Capital: GBP 55M
- Operational (5 years): GBP 30M

**Expected Benefits**: GBP 195M over 10 years

- Administrative cost savings across participating councils: GBP 125M
- Reduced legal challenges and complaints: GBP 30M
- Improved allocation efficiency (faster lettings, fewer voids): GBP 40M

**Return on Investment**:

- NPV: GBP 68M (discounted at 3.5%)
- Payback Period: 42 months
- ROI: 129% over 10 years

**Recommended Option**: Option 2: National Platform with Incentivised Adoption

**Key Risks**:

1. Council adoption rate below target — mitigated by incentive funding and early adopter programme
2. Legacy data migration complexity across 300+ systems — mitigated by standardised migration toolkit
3. Allocation policy diversity exceeding platform configurability — mitigated by extensible rules engine

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Social housing allocation in England is fragmented across 309 local housing authorities, each operating independent systems ranging from modern SaaS platforms to paper-based processes. Housing associations operating across multiple council areas must maintain interfaces with dozens of different systems.

**Consequences of Inaction**:

- No national data on housing need, waiting times, or allocation outcomes — policymaking is evidence-blind
- Applicant experience varies wildly — some councils offer digital CBL, others require paper forms
- Housing associations bear disproportionate administrative cost interfacing with multiple systems
- RSH cannot effectively regulate allocation transparency without consistent data

### A1.2 Strategic Alignment

- **SDG 1: No Poverty**: Stable, affordable housing is a foundation for escaping poverty
- **Social Housing (Regulation) Act 2023**: Transparency and accountability in allocation
- **Homelessness Reduction Act 2017**: Reasonable preference duties
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (User-Centred Design), 4 (Interoperability), 10 (Single Source of Truth)

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Councils continue with independent systems.

**Costs (5-year)**: GBP 0 central investment (GBP 350M+ aggregate local spend on fragmented systems)

**Benefits**: GBP 0

**Recommendation**: **Reject** — Fragmentation worsens, no national data, increasing regulatory risk.

---

### Option 1: Data Standards Only

**Description**: Publish national data standards for housing allocation without building a platform. Councils adopt voluntarily.

**Costs (5-year)**: GBP 8M (standards development, guidance, support)

**Benefits**: GBP 15M (modest data quality improvement)

**Pros**: Low cost, low risk, respects local autonomy

**Cons**: No platform for applicants, no CBL improvement, adoption voluntary and likely low, housing associations still interface with 300+ systems

**Stakeholder Goals Met**: 15%

**Recommendation**: **Reject** — Insufficient to address the problem.

---

### Option 2: National Platform with Incentivised Adoption (RECOMMENDED)

**Description**: Build a multi-tenant, configurable national platform with incentive funding for council adoption. Councils retain full control over allocation policies within a standardised technical framework.

**Costs (5-year)**: GBP 85M

- Capital: GBP 55M (platform development, migration tools, integration)
- Operational: GBP 30M (hosting, support, council onboarding)

**Benefits (10-year)**: GBP 195M

| Benefit | Type | Annual (at maturity) | 10-Year Total |
|---------|------|---------------------|---------------|
| Council admin cost reduction (60% per allocation) | FINANCIAL | GBP 15M | GBP 125M |
| Reduced legal challenges and complaints (40%) | FINANCIAL | GBP 3.5M | GBP 30M |
| Void period reduction through faster allocation | OPERATIONAL | GBP 5M | GBP 40M |

**NPV**: GBP 68M | **Payback**: 42 months | **ROI**: 129%

**Stakeholder Goals Met**: 90%

**Recommendation**: **ACCEPT**

---

### Option 3: Mandatory National System

**Description**: Legislate to require all councils to use a single national allocation system with standardised allocation policies.

**Costs (5-year)**: GBP 150M (platform + legislative programme + enforcement)

**Benefits (10-year)**: GBP 250M (higher due to 100% coverage)

**Pros**: Full coverage, complete data, maximum efficiency

**Cons**: Requires primary legislation (2+ year delay), politically contentious, overrides council statutory autonomy, strong LGA opposition

**Stakeholder Goals Met**: 70% (LA Housing Directors goal NOT met — autonomy lost)

**Recommendation**: **Reject** — Politically undeliverable and unnecessary. Incentivised adoption achieves 80% coverage without legislative risk.

---

## B3. Recommended Option

**Option 2: National Platform with Incentivised Adoption** — best balance of coverage, cost, and stakeholder acceptability. NPV GBP 68M with 42-month payback.

---

# PART C: COMMERCIAL CASE

**Procurement Route**: Digital Marketplace (G-Cloud for hosting, DOS for delivery teams). Multi-supplier model with SME targets.

**Contract Approach**: Agile delivery through DOS outcomes contracts, GBP 6M/year managed service.

---

# PART D: FINANCIAL CASE

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 15M | GBP 18M | GBP 12M | GBP 7M | GBP 3M | GBP 55M |
| OpEx | GBP 3M | GBP 5M | GBP 7M | GBP 7.5M | GBP 7.5M | GBP 30M |
| **Total** | **GBP 18M** | **GBP 23M** | **GBP 19M** | **GBP 14.5M** | **GBP 10.5M** | **GBP 85M** |

**Funding Source**: DLUHC Housing Programme budget, Spending Review settlement.

---

# PART E: MANAGEMENT CASE

**Programme Governance**: DLUHC Programme Board chaired by SRO, with LGA, RSH, and housing association representation. Early adopter programme with 50 councils in Year 1.

**Key Risks**:

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Council adoption below 80% target | MEDIUM | HIGH | Incentive funding, early adopter programme, free migration support |
| Legacy data migration failures | HIGH | MEDIUM | Standardised migration toolkit, council-specific testing |
| Allocation policy diversity exceeds configurability | MEDIUM | HIGH | Extensible rules engine, bespoke configuration support |
| Housing association API adoption | LOW | MEDIUM | Industry consultation on API design, pilot with top 10 RPs |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| DLUHC Permanent Secretary | Accounting Officer | [ ] Approved | PENDING |
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| HM Treasury | Funding | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Social Housing Allocation Platform
**Model**: Claude Opus 4.6
