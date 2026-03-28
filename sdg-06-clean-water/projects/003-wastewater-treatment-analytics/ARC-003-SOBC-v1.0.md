# Strategic Outline Business Case (SOBC): Wastewater Treatment Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Wastewater Treatment Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Wastewater Treatment Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Ofwat Board, DEFRA Investment Board, HM Treasury, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in a Wastewater Treatment Analytics platform to transform Ofwat's regulatory capability from retrospective self-reported data analysis to proactive, independent, real-time performance monitoring. It follows the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Establish an independent analytics platform enabling Ofwat to assess water company sewage treatment performance using standardised, auditable methodology applied to operational telemetry data, replacing the current self-reported annual assurance model.

**Problem Statement**: Ofwat currently relies on water company self-reported Annual Performance Reports validated through a 6-month assurance process costing GBP 40M industry-wide. This model is slow (6 months lag), expensive, and undermined by public perception that companies can influence their own performance narrative. The Environment Act 2021 introduces legally binding storm overflow reduction targets requiring continuous, auditable tracking.

**Proposed Solution**: A cloud-hosted analytics platform ingesting water company operational telemetry (SCADA, EDMs, flow monitors) and applying standardised Ofwat methodology to independently calculate performance metrics, track Environment Act targets, and publish transparent performance data.

**Strategic Fit**: Supports Ofwat's statutory duties under the Water Industry Act 1991, delivers Environment Act 2021 compliance monitoring for DEFRA, and strengthens the evidence base for the PR29 price review determination.

**Investment Required**: GBP 12M over 3 years

- Capital: GBP 8M
- Operational (3 years): GBP 4M

**Expected Benefits**: GBP 52M over 5 years

- Industry assurance cost reduction: GBP 24M
- Ofwat regulatory efficiency gains: GBP 8M
- Earlier enforcement intervention (avoided environmental damage): GBP 12M
- Customer bill fairness (better-evidenced price reviews): GBP 8M

**Return on Investment**:

- NPV: GBP 33.6M (discounted at 3.5%)
- Payback Period: 20 months
- ROI: 333%

**Recommended Option**: Option 2: Independent Analytics Platform

**Key Risks**:

1. Water company legal challenges to Ofwat's data access powers
2. Methodology disputes delaying platform adoption
3. Data quality inconsistencies across 11 companies' heterogeneous SCADA systems

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The current self-reporting model is no longer credible given the sewage discharge crisis and Environment Act requirements. An independent analytics platform strengthens regulatory credibility, reduces industry assurance costs by GBP 24M over 5 years, and provides the evidence base for fair PR29 price determinations. The NPV of GBP 33.6M and ROI of 333% represent strong value for money.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Ofwat's regulatory performance assessment relies on water company Annual Performance Reports (APRs). Companies compile their own data, apply methodology with some interpretation flexibility, and submit to Ofwat for validation through external assurance. This process takes 6 months, costs GBP 40M industry-wide in assurance fees (ultimately paid by customers through bills), and has been criticised by environmental groups, Parliamentary committees, and the NAO.

The Environment Act 2021 introduced legally binding storm overflow discharge reduction targets with progressive milestones. These targets require continuous, auditable performance tracking — not annual retrospective reporting.

**Specific Pain Points** (from Stakeholder Analysis ARC-003-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Ofwat CEO | SD-1 | 6-month assurance cycle, reliance on self-reporting | Delayed regulatory action, credibility risk | CRITICAL |
| Water Companies | SD-2 | Inconsistent methodology application, high assurance costs | GBP 40M/year assurance, regulatory uncertainty | HIGH |
| DEFRA Policy Dir | SD-3 | Cannot track Environment Act target compliance | Judicial review risk, Parliamentary scrutiny | CRITICAL |
| Public / CCW | SD-4 | Cannot verify water company claims | 67% distrust company performance data | HIGH |

**Consequences of Inaction**:

- Ofwat PR29 price determination based on potentially unreliable self-reported data — risk of incorrect price caps
- Environment Act target compliance unverifiable — judicial review risk for DEFRA
- Public trust in water regulation continues to erode (currently 34% trust)
- GBP 40M annual assurance cost continues with no efficiency improvement
- Potential for water companies to underperform without timely detection

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **Water Industry Act 1991**: Ofwat's duty to ensure water companies meet their obligations
- **Environment Act 2021**: Storm overflow discharge reduction targets (Section 82)
- **Storm Overflow Discharge Reduction Plan**: Legally binding reduction milestones
- **Ofwat Strategy**: "Trust in water" — independent evidence for regulatory decisions
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Data Integrity), 9 (Data Quality and Lineage), 10 (Single Source of Truth)

### A1.3 Why Now?

**Urgency Factors**:

- PR29 data collection starts 2028 — platform must be operational to inform the price review
- Environment Act storm overflow targets require tracking from 2027
- Public and Parliamentary pressure on water company accountability at historic highs
- NAO value for money review of water regulation expected 2027 — Ofwat needs to demonstrate modern regulatory capability

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Regulatory independence**: Platform calculation results independent of water company influence
   - **Measure**: Audit trail verification, methodology transparency
   - **Threshold**: Zero instances of company data manipulation post-ingestion

2. **Assurance efficiency**: Reduce annual assurance cycle from 6 months to 6 weeks
   - **Measure**: Time from period end to validated performance assessment
   - **Threshold**: Maximum 8 weeks

3. **Industry adoption**: All 11 water and sewerage companies integrated
   - **Measure**: Companies providing telemetry data feeds
   - **Threshold**: Minimum 9 of 11 by Year 1, 11 of 11 by Year 2

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current self-reported APR model and manual assurance process.

**Costs** (5-year):
- Operational: GBP 60M (annual assurance costs GBP 40M x 5 years / 3 = GBP 66M, plus Ofwat staff)
- Total: GBP 60M

**Benefits**: GBP 0

**Consequences**:
- PR29 based on potentially unreliable data — mispriced customer bills
- Environment Act compliance unverifiable
- Regulatory credibility continues to decline
- NAO likely critical value for money assessment

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Does not meet Environment Act requirements, regulatory credibility at risk.

---

### Option 1: Enhanced Self-Reporting with Digital Submission

**Description**: Upgrade Ofwat's data collection to require digital submission in standardised formats with automated validation rules. Companies still calculate their own metrics but submit via structured API.

**Costs** (3-year) — ROM (+/-40%):
- Capital: GBP 3M
- Operational: GBP 1.5M
- Total: GBP 4.5M

**Benefits** (5-year): GBP 15M
- Partial assurance cost reduction (20%): GBP 8M
- Faster validation: GBP 4M
- Better data standardisation: GBP 3M

**Stakeholder Goals Met**: 35%

**Recommendation**: **Reject** — Does not address fundamental problem of self-reporting. Does not provide independent analytics capability.

---

### Option 2: Independent Analytics Platform (RECOMMENDED)

**Description**: Cloud-hosted platform ingesting operational telemetry from water companies and independently calculating performance metrics using Ofwat-defined methodology.

**Costs** (3-year) — ROM (+/-30%):
- Capital: GBP 8M
  - Platform development: GBP 4M
  - Water company integration (11 companies): GBP 2M
  - Public dashboard and reporting: GBP 1M
  - Security and audit trail: GBP 1M
- Operational: GBP 4M over 3 years
  - Cloud hosting: GBP 0.6M/year
  - Support and maintenance: GBP 0.4M/year
  - Methodology and data quality team (4 FTE): GBP 0.35M/year
- Total 3-year TCO: GBP 12M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Assurance cost reduction (60%) | FINANCIAL | GBP 2M | GBP 4.8M | GBP 4.8M | GBP 6M | GBP 6M | GBP 23.6M |
| B-002 | Ofwat regulatory efficiency | OPERATIONAL | GBP 0.5M | GBP 1.5M | GBP 2M | GBP 2M | GBP 2M | GBP 8M |
| B-003 | Earlier enforcement (avoided damage) | ENVIRONMENTAL | GBP 0 | GBP 2M | GBP 3M | GBP 3.5M | GBP 3.5M | GBP 12M |
| B-004 | Better-evidenced price review | FINANCIAL | GBP 0 | GBP 0 | GBP 2M | GBP 3M | GBP 3M | GBP 8M |
| **Total** | | | **GBP 2.5M** | **GBP 8.3M** | **GBP 11.8M** | **GBP 14.5M** | **GBP 14.5M** | **GBP 51.6M** |

**Net Present Value** (3.5% discount rate):
- Total Benefits PV: GBP 45.6M
- Total Costs PV: GBP 12M
- **NPV: GBP 33.6M**

**Return on Investment**:
- **ROI: 333%** over 5 years
- **Payback Period: 20 months**

**Stakeholder Goals Met**: 85%

---

### Option 3: Full Regulatory Intelligence Platform with AI

**Description**: Comprehensive platform with AI-powered anomaly detection, predictive compliance modelling, and automated enforcement recommendation engine.

**Costs** (3-year): GBP 22M
**Benefits** (5-year): GBP 60M
**NPV**: GBP 27.4M (lower than Option 2)

**Recommendation**: **Reject** — AI enforcement prediction maturity insufficient, legal challenges likely, water company opposition would be extreme.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Independent Analytics Platform**

**Rationale**:
1. **Best Value**: Highest NPV at GBP 33.6M
2. **Regulatory credibility**: Independent analytics ends self-reporting criticism
3. **Environment Act compliance**: Continuous target tracking
4. **PR29 readiness**: Operational before PR29 data collection
5. **Cost efficiency**: GBP 24M industry assurance cost reduction

**Optimism Bias Adjustment**:
- Adjusted Total Cost: GBP 12M -> GBP 16.8M (with 40% uplift)
- NPV with optimism bias: GBP 28.8M (still strongly positive)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace — G-Cloud for cloud platform, DOS6 for development services

**Contract Approach**:
- **Build**: Agile delivery, time-and-materials (GBP 8M budget)
- **Run**: Managed service (3+2 years)
- **Data access**: Water company data provision mandated under Water Industry Act 1991 section 202

**Social Value**: Minimum 10% weighting. Focus on water sector workforce development and environmental benefit quantification.

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 12M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 5M | GBP 3M | GBP 0 | GBP 8M |
| OpEx | GBP 1.35M | GBP 1.35M | GBP 1.3M | GBP 4M |
| **Total** | **GBP 6.35M** | **GBP 4.35M** | **GBP 1.3M** | **GBP 12M** |

## D2. Funding Source

**Source**: Ofwat operating budget (funded through water company licence fees — ultimately recovered from customer bills)
**Amount Available**: GBP 15M available within current settlement for regulatory modernisation
**Assessment**: **Affordable** — platform costs ultimately reduce industry-wide costs by GBP 24M

## D3. Value for Money

**Qualitative Assessment**:
- Economy: GBP 24M industry assurance cost reduction exceeds total platform cost
- Efficiency: 6-month assurance cycle reduced to 6 weeks
- Effectiveness: Independent analytics providing evidence-based regulation

**Overall VfM Rating**: **HIGH** — every GBP 1 invested returns GBP 4.30 over 5 years

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: Ofwat Director of Strategy and Performance
**Steering Committee**: Ofwat CEO, DEFRA Water Policy Director, EA Director of Water Quality, Water UK representative (advisory)

## E2. Key Milestones

| Milestone | Date |
|-----------|------|
| SOBC Approval | Q2 2026 |
| Methodology consultation with industry | Q3 2026 |
| Procurement Award | Q4 2026 |
| First company integration (pilot — 2 companies) | Q2 2027 |
| Storm overflow dashboard live | Q4 2027 |
| All 11 companies integrated | Q2 2028 |
| **PR29 data collection** | **Q3 2028** |
| Benefits Review | Q3 2029 |

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | Water company legal challenge to data access | Medium | High | 12 | Legal opinion confirming WIA 1991 powers, DEFRA Ministerial backing |
| R-002 | Methodology disputes delay adoption | High | Medium | 12 | Formal consultation process, published rationale, phased implementation |
| R-003 | Data quality inconsistencies across companies | High | Medium | 12 | Standardised API specification, data quality toolkit, remediation support |
| R-004 | Company gaming of telemetry data | Low | High | 8 | Anomaly detection algorithms, cross-reference with EA enforcement data |
| R-005 | PR29 timeline missed | Low | Critical | 9 | Early start, phased integration, parallel running with existing APR process |

---

# PART F: RECOMMENDATION & NEXT STEPS

**Recommended Option**: **Option 2: Independent Analytics Platform**
**Investment**: GBP 12M over 3 years
**Expected Return**: GBP 52M over 5 years (NPV: GBP 33.6M, ROI: 333%)
**Go/No-Go**: **PROCEED**

**Next Steps**:
1. Ofwat Board approval — Target: Q2 2026
2. Methodology consultation with water industry — Target: Q3 2026
3. Procurement via Digital Marketplace — Target: Q4 2026
4. Pilot integration (2 companies) — Target: Q2 2027
5. Full integration (11 companies) — Target: Q2 2028
6. PR29 data collection operational — Target: Q3 2028

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO / Ofwat Dir of Strategy | | |
| | Ofwat Chief Executive | | |
| | Ofwat Chief Economist | | |
| | DEFRA Water Policy Director | | |

**Approval Decision**: PENDING

---

**Generated by**: ArcKit `/arckit:sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wastewater Treatment Analytics (Project 003)
**AI Model**: Claude Opus 4.6 (1M context)
