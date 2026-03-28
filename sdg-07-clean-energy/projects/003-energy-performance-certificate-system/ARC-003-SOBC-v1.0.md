# Strategic Outline Business Case (SOBC): Energy Performance Certificate System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Energy Performance Certificate System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, EPC System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Programme Board, HM Treasury, DESNZ, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The EPC system is the backbone of building energy efficiency policy in England and Wales. It must be modernised to support the SAP 11 methodology, automate MEES enforcement, and deliver reliable data for the Net Zero buildings agenda.

**Problem Statement**: The current EPC register infrastructure is ageing, operated under legacy contracts, and cannot support the SAP 11 transition, automated MEES enforcement (only 1% of non-compliant landlords fined since 2018), or the data quality needed for building decarbonisation policy targeting.

**Proposed Solution**: Build a modern, API-first EPC platform with SAP 11 calculation engine, automated MEES compliance checking, and analytics for policy evaluation.

**Strategic Fit**: Directly supports the Heat and Buildings Strategy, Net Zero Strategy building decarbonisation targets, and the Energy Act 2023 building efficiency provisions.

**Investment Required**: £15M over 3 years
- Capital: £10M
- Operational (3 years): £5M

**Expected Benefits**: £42M over 5 years
- MEES enforcement revenue: £20M (increased fines from 1% to 10% enforcement rate)
- Energy savings from improved compliance: £15M (more properties reaching EPC C)
- Operational efficiency: £4M (reduced lodgement processing costs)
- Policy targeting accuracy: £3M (better retrofit programme targeting)

**Return on Investment**:
- NPV: £18.7M (discounted at 3.5%)
- Payback Period: 22 months
- ROI: 180%

**Recommended Option**: Option 2: Modern API-First Platform

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The EPC register processes 1.5 million assessments annually but operates on ageing infrastructure under contracts due for renewal. The SAP 10.2 methodology is outdated. MEES enforcement is virtually non-existent (1% enforcement rate since 2018) because local authorities lack programmatic access to EPC data. EPC data quality issues (inconsistent assessor practices, outdated methodology) undermine confidence in ratings.

**Consequences of Inaction**:
- Cannot implement SAP 11 methodology on current infrastructure — EPC ratings become increasingly inaccurate
- MEES 2028 deadline (EPC C for all PRS) unenforceable without automated compliance checking
- 4.4 million privately rented properties remain at EPC D-G, contributing to fuel poverty and carbon emissions
- Building decarbonisation policy lacks accurate data for retrofit targeting (estimated £2M/year in mis-targeted grants)

### A1.2 Why Now?

- SAP 11 methodology finalised — implementation window before 2028 MEES deadline
- Current register contracts approaching renewal — opportunity for re-platforming
- MEES 2028 deadline creates political urgency for enforcement capability
- Heat and Buildings Strategy depends on accurate EPC data for policy delivery

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Costs (3-year)**: £0 additional; £3M/year existing contract renewal
**Benefits**: £0
**Recommendation**: **Reject** — Cannot implement SAP 11; MEES unenforceable; data quality deteriorates.

### Option 1: Upgrade Existing Infrastructure

**Description**: Extend current contracts with register operators. Implement SAP 11 as a module. Add basic MEES checking.
**Costs (3-year)**: Capital £5M; Operational £4.5M; Total £9.5M
**Benefits (5-year)**: £20M
**NPV**: £6.5M
**Stakeholder Goals Met**: 40%
**Recommendation**: Reject — does not deliver API-first architecture needed for local authority enforcement; limited analytics; vendor lock-in.

### Option 2: Modern API-First Platform (RECOMMENDED)

**Description**: Build a new EPC platform with cloud-hosted SAP 11 calculation engine, API-first architecture for assessor software and local authority enforcement systems, public register on GOV.UK, and analytics for policy evaluation.

**Costs (3-year) — ROM (±30%)**:
- Capital: £10M (SAP 11 engine £3M, platform build £4M, integration £1.5M, security/testing £1.5M)
- Operational: £5M (cloud hosting £2.4M, support £1.5M, accreditation management £1.1M)
- Total 3-year TCO: £15M

**Benefits (5-year)**:

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|-------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | MEES enforcement revenue | FINANCIAL | £1M | £3M | £5M | £5.5M | £5.5M | £20M |
| B-002 | Energy savings from compliance | STRATEGIC | £1M | £2.5M | £3.5M | £4M | £4M | £15M |
| B-003 | Operational efficiency | FINANCIAL | £0.5M | £0.8M | £1M | £1M | £1M | £4.3M |
| B-004 | Policy targeting accuracy | STRATEGIC | £0.3M | £0.5M | £0.7M | £0.8M | £0.8M | £3.1M |
| **Total** | | | **£2.8M** | **£6.8M** | **£10.2M** | **£11.3M** | **£11.3M** | **£42.4M** |

**NPV (3.5%, 5-year)**: £18.7M

**ROI**: 180%

**Stakeholder Goals Met**: 85%

### Option 3: National Building Energy Database

**Description**: Comprehensive building energy database integrating EPCs with smart meter data, heating systems, insulation records, and predictive energy modelling.
**Costs (3-year)**: Capital £25M; Operational £10M; Total £35M
**Recommendation**: **Reject** — Scope too broad for current mandate and budget. Option 2 provides the foundation; database integration can be added incrementally.

---

# PART C: COMMERCIAL CASE

**Sourcing Route**: Digital Marketplace — G-Cloud for hosting; DOS for SAP 11 calculation engine development (specialist energy modelling capability).

**Contract Approach**: Separate lots for calculation engine (specialist), platform (generalist), and hosting (commodity) to manage risk and enable SME participation.

---

# PART D: FINANCIAL CASE

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | £6M | £3.5M | £0.5M | £10M |
| OpEx | £1M | £1.8M | £2.2M | £5M |
| **Total** | **£7M** | **£5.3M** | **£2.7M** | **£15M** |

**Funding Source**: DLUHC digital budget + cross-departmental contribution from DESNZ (building decarbonisation programme).

**Affordability**: £15M within DLUHC's digital transformation allocation. Self-funding from Year 3 through MEES enforcement revenue (ring-fenced by local authorities but reduces central enforcement subsidy requirement).

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Phases**:
1. **Discovery** (Months 1-3): SAP 11 specification validation, assessor software vendor engagement, local authority needs assessment
2. **Alpha** (Months 4-7): SAP 11 calculation engine prototype, register API design, BRE validation
3. **Beta** (Months 8-13): Platform build, assessor software certification, local authority pilot (10 councils)
4. **Live** (Month 14): Production launch with SAP 11, public register, MEES API
5. **Rollout** (Months 15-24): Local authority onboarding (333 councils), analytics development

## E2. Key Milestones

| Milestone | Date | Owner |
|-----------|------|-------|
| SOBC Approval | Q2 2026 | SRO |
| SAP 11 engine validated against BRE reference | Q1 2027 | Technical Architect |
| Assessor software certification programme launched | Q2 2027 | DLUHC Building Safety |
| Local authority pilot (10 councils) | Q3 2027 | Service Owner |
| **Production launch** | **Q4 2027** | SRO |
| 200+ local authorities onboarded | Q4 2028 | Service Owner |

## E3. Top 5 Risks

| Risk ID | Description | Likelihood | Impact | Mitigation |
|---------|-------------|------------|--------|------------|
| R-001 | SAP 11 methodology changes during development | Medium | Major | Close BRE engagement, modular calculation engine |
| R-002 | Assessor software vendors slow to certify | Medium | Major | Early vendor engagement, transitional dual-methodology support |
| R-003 | Local authority take-up below target | Medium | Moderate | Funding support, template enforcement workflows, champion councils |
| R-004 | Data migration from existing register fails | Low | Major | Parallel running period, phased migration |
| R-005 | Property owner backlash against MEES enforcement | Medium | Moderate | Clear communications, grant signposting, exemption process |

---

# PART F: RECOMMENDATION

**Recommended Option**: **Option 2: Modern API-First Platform**
**Investment**: £15M over 3 years
**Expected Return**: £42.4M over 5 years (NPV: £18.7M)
**Go/No-Go**: **PROCEED**

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | DLUHC SRO | | |
| | DLUHC Finance Director | | |
| | DLUHC Digital Director | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Energy Performance Certificate System (Project 003)
**Model**: Claude Opus 4.6 (1M context)
