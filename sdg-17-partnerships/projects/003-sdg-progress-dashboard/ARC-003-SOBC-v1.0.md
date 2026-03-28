# Strategic Outline Business Case (SOBC): SDG Progress Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | SDG Progress Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SDG Progress Dashboard Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | ONS Board, UKSA, Cabinet Office SDG Unit, HM Treasury, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in the ONS SDG Progress Dashboard, following the HM Treasury Green Book five-case model. It draws on stakeholder analysis (ARC-003-STKE-v1.0) and architecture principles (ARC-000-PRIN-v1.0).

---

## Executive Summary

**Purpose**: The UK committed to the 2030 Agenda for Sustainable Development but lacks a comprehensive, authoritative platform for monitoring UK SDG progress. Current SDG data is scattered across 20+ departments, approximately 180 of 244 indicators have data, and VNR preparation takes 8 weeks of manual effort.

**Problem Statement**: The UK cannot present a credible, comprehensive picture of its SDG progress to the international community, civil society, or its own Parliament. Data gaps, scattered sources, and manual compilation undermine the UK's ability to meet its 2030 Agenda commitments.

**Proposed Solution**: An ONS-led public SDG Progress Dashboard covering 200+ indicators, with SDMX-compliant data exchange with UNSD, open API for civil society and researchers, sub-national disaggregation, and automated VNR data preparation.

**Strategic Fit**: Supports the UK Voluntary National Review commitments, the Statistics and Registration Service Act 2007 (ONS mandate), and the SDG 17 programme's statistical reporting requirements. Aligns with Principle 2 (Statistical Independence) of the programme architecture.

**Investment Required**: GBP 8M over 3 years

- Capital: GBP 5M
- Operational (3 years): GBP 3M

**Expected Benefits**: GBP 12.5M over 5 years

- VNR and SDG reporting efficiency: GBP 4M
- Cross-government policy improvement from evidence base: GBP 5M
- Reduced duplicate statistical production: GBP 2M
- International statistical credibility: GBP 1.5M (avoided reputational costs)

**Return on Investment**:

- NPV: GBP 3.2M (discounted at 3.5%)
- Payback Period: 28 months
- ROI: 56%

**Recommended Option**: Option 2: Comprehensive Dashboard with Open API and SDMX

**Key Risks**:

1. Source department data availability — 20+ departments must provide data (mitigated by Cross-Government Data Sharing Platform, Project 002)
2. Indicator methodology alignment — UK methods may differ from IAEG-SDGs definitions (mitigated by phased approach, proxy indicators clearly labelled)
3. ONS resource constraints — 8 FTE SDG team must sustain 200+ indicators (mitigated by automation)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK's credibility on sustainable development depends on comprehensive, authoritative SDG monitoring. ONS is the natural home for this capability, and the investment is modest relative to the policy and reputational value.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The UK's SDG monitoring capability is fragmented. ONS maintains an SDG data platform covering approximately 180 of 244 indicators, but it lacks sub-national disaggregation, automated SDMX reporting to UNSD, and the interactive visualisation needed for public engagement and policy use. Data from 20+ source departments arrives in inconsistent formats and timelines. VNR preparation requires 8 weeks of manual data assembly.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| UKSA/ONS | SD-1 | Platform does not meet Code of Practice for modern statistics | Reputational risk to UK statistical authority | CRITICAL |
| Cabinet Office | SD-2 | VNR preparation takes 8 weeks; data gaps embarrassing | UK credibility at UN diminished | HIGH |
| UNSD | SD-3 | UK SDMX submissions late and incomplete | UK data omitted from global reports | HIGH |
| Civil society | SD-5 | Data not machine-readable; limited API access | Independent scrutiny difficult | MEDIUM |

**Consequences of Inaction**:

- UK presents increasingly outdated VNR with growing indicator gaps
- UNSD global SDG reports use estimated rather than actual UK data
- Civil society shadow reports highlight UK's data transparency shortcomings
- Policy decisions made without comprehensive SDG evidence base
- Devolved administrations develop separate, inconsistent SDG platforms

### A1.2 Strategic Alignment

- **Statistics and Registration Service Act 2007**: ONS mandate to produce comprehensive national statistics
- **UK Voluntary National Review commitments**: Comprehensive, evidence-based reporting to UN
- **UKSA Code of Practice**: Trustworthiness, Quality, Value — modern statistics must be accessible, timely, and coherent
- **SDG 17 Principles (ARC-000-PRIN-v1.0)**: Principle 2 (Statistical Independence), Principle 1 (International Interoperability)

### A1.3 Why Now?

- 2030 Agenda has 4 years remaining — UK must demonstrate comprehensive monitoring before the deadline
- Next UK Voluntary National Review expected 2028 — platform must be operational
- Cross-Government Data Sharing Platform (Project 002) provides data infrastructure for source department feeds
- IAEG-SDGs indicator framework has stabilised (Tier 1/2 methodology established for most indicators)

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Indicator coverage**: 200+ of 244 indicators with published data within 18 months
2. **Statistical integrity**: UKSA Code of Practice compliance verified
3. **International compliance**: Automated SDMX submission to UNSD within 12 months
4. **Public engagement**: 10,000+ monthly unique visitors within 6 months of launch
5. **Sustainability**: Platform operable by existing ONS SDG team (8 FTE) through automation

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Costs** (3-year): GBP 2M (continued manual VNR preparation, ad hoc indicator maintenance)

**Benefits**: GBP 0

**Recommendation**: **Reject** — UK SDG credibility declines; VNR increasingly difficult to compile.

---

### Option 1: Basic Indicator Update

**Description**: Enhance existing ONS SDG data platform with additional indicators and minor UX improvements. No SDMX automation, no open API, no sub-national disaggregation.

**Costs** (3-year): GBP 3M

**Benefits** (5-year): GBP 4.5M

**Stakeholder Goals Met**: 30%

**Recommendation**: **Reject** — Incremental improvement that does not address SDMX compliance, open access, or VNR automation needs.

---

### Option 2: Comprehensive Dashboard with Open API and SDMX (RECOMMENDED)

**Description**: Full public dashboard with interactive visualisations, open API (JSON/CSV/SDMX), automated SDMX submission to UNSD, sub-national disaggregation, VNR report generation, and indicator gap analysis.

**Costs** (3-year) — ROM (+-30%):

- Capital: GBP 5M
  - Dashboard development: GBP 2.5M
  - API and SDMX pipeline: GBP 1M
  - Data integration (20+ sources via Project 002): GBP 1M
  - Accessibility and testing: GBP 0.5M
- Operational: GBP 3M (3 years)
  - Hosting and managed services: GBP 0.5M/year
  - Support and indicator maintenance: GBP 0.5M/year
- Total 3-year TCO: GBP 8M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|-------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | VNR and SDG reporting efficiency | OPERATIONAL | GBP 0.3M | GBP 0.8M | GBP 0.8M | GBP 1M | GBP 1.1M | GBP 4M |
| B-002 | Policy improvement from evidence | STRATEGIC | GBP 0 | GBP 0.5M | GBP 1M | GBP 1.5M | GBP 2M | GBP 5M |
| B-003 | Reduced duplicate statistical production | OPERATIONAL | GBP 0.2M | GBP 0.4M | GBP 0.4M | GBP 0.5M | GBP 0.5M | GBP 2M |
| B-004 | International credibility | STRATEGIC | GBP 0 | GBP 0.2M | GBP 0.3M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| **Total** | | | **GBP 0.5M** | **GBP 1.9M** | **GBP 2.5M** | **GBP 3.5M** | **GBP 4.1M** | **GBP 12.5M** |

**NPV** (3.5% discount, 5-year): **GBP 3.2M**

**ROI**: **56%**

**Payback Period**: **28 months**

**Stakeholder Impact**:

- UKSA/ONS SD-1: Met — Code of Practice compliant, modern platform
- Cabinet Office SD-2: Met — VNR preparation automated, comprehensive data
- UNSD SD-3: Met — automated SDMX submission
- Devolved admins SD-4: Partially met — sub-national data for 60%+ of indicators
- Civil society SD-5: Met — open API, machine-readable data

**Stakeholder Goals Met**: 85%

---

### Option 3: Global SDG Analytics Platform

**Description**: World-leading SDG platform with advanced analytics, AI-driven trend forecasting, interactive scenario modelling, and global comparison tools.

**Costs** (3-year): GBP 15M

**Benefits** (5-year): GBP 15M

**Recommendation**: **Reject** — Over-engineered for UK needs. Core value is comprehensive, authoritative, accessible data — not advanced analytics. Academic partners can build analytics on top of the open API.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Comprehensive Dashboard with Open API and SDMX**

**Rationale**:

1. **Best value**: Positive NPV, affordable investment
2. **Statistical integrity**: Designed for UKSA Code of Practice compliance
3. **International compliance**: Automated SDMX meets UNSD requirements
4. **Open access**: API enables civil society, researchers, and devolved administrations
5. **Sustainability**: Automated workflows manageable by existing 8 FTE team

**Optimism Bias Adjustment** (Green Book +40%):

- Adjusted Cost: GBP 8M -> GBP 11.2M
- NPV with optimism bias: GBP 0.3M (marginally positive, justified by strategic value)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: G-Cloud for dashboard and hosting components; DOS6 for SDMX and data integration development.

**Contract Approach**:

- **Build**: Time and materials with agile milestones (12 months for core, 6 months for sub-national)
- **Run**: Managed service (3+1+1 year)

**ONS Internal Capability**: ONS Digital Services will lead architecture and data engineering, with external resource for frontend development and SDMX integration.

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 8M over 3 years

### D1.1 Capital Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Dashboard development | GBP 1.5M | GBP 1M | GBP 0 | GBP 2.5M |
| API and SDMX pipeline | GBP 0.7M | GBP 0.3M | GBP 0 | GBP 1M |
| Data integration (20+ sources) | GBP 0.5M | GBP 0.3M | GBP 0.2M | GBP 1M |
| Accessibility and testing | GBP 0.3M | GBP 0.2M | GBP 0 | GBP 0.5M |
| **Total CapEx** | **GBP 3M** | **GBP 1.8M** | **GBP 0.2M** | **GBP 5M** |

### D1.2 Operational Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Hosting and managed services | GBP 0.4M | GBP 0.5M | GBP 0.5M | GBP 1.4M |
| Support and indicator maintenance | GBP 0.4M | GBP 0.5M | GBP 0.7M | GBP 1.6M |
| **Total OpEx** | **GBP 0.8M** | **GBP 1M** | **GBP 1.2M** | **GBP 3M** |

## D2. Funding Source

**Source**: ONS Digital Investment Fund, with Cabinet Office contribution for cross-government policy value.

## D3. Affordability

- ONS total budget: GBP 600M/year
- This project: 0.5% of ONS budget (Year 1)
- Assessment: **Affordable**

## D4. Value for Money

**Overall VfM Rating**: **Medium-High** — Positive NPV, significant strategic and international value beyond monetised benefits.

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: ONS Deputy National Statistician (Population and Public Policy)

**Steering Committee**: SRO (Chair), ONS Digital Services Director, ONS Methodology Director, ONS International Team, Cabinet Office SDG Unit, UKSA Assessment representative (observer)

## E2. Delivery Approach

**Phases**:

1. **Discovery** (Months 1-3): Indicator gap analysis, user research, SDMX architecture
2. **Alpha** (Months 4-6): Dashboard prototype with 50 indicators, API proof of concept
3. **Beta** (Months 7-12): Full dashboard with 200+ indicators, SDMX submission, sub-national data
4. **Live** (Month 13): GDS service assessment, public launch
5. **Enhancement** (Months 14-18): VNR automation, advanced visualisation, devolved admin engagement

## E3. Key Milestones

| Milestone | Date | Owner |
|-----------|------|-------|
| SOBC Approval | Q2 2026 | SRO |
| Indicator Gap Analysis Complete | Q3 2026 | ONS SDG Team Lead |
| GDS Alpha Assessment | Q1 2027 | Service Owner |
| Dashboard Beta (200+ indicators) | Q3 2027 | Delivery Manager |
| Automated SDMX to UNSD | Q3 2027 | ONS International Team |
| GDS Beta Assessment | Q4 2027 | Service Owner |
| Public Launch | Q1 2028 | SRO |
| VNR Data Pack Generated | Q2 2028 | Cabinet Office SDG Unit |

## E4. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | Source department data not available | Medium | Major | 12 | Project 002 federated access; bilateral agreements as fallback |
| R-002 | IAEG methodology misalignment | High | Moderate | 12 | Phased approach; proxy indicators clearly labelled as experimental |
| R-003 | ONS team capacity (8 FTE) | High | Moderate | 12 | Automation from Day 1; external development for build phase |
| R-004 | Political pressure to suppress unfavourable indicators | Low | Critical | 9 | UKSA independence mandate; technical controls on publication pipeline |
| R-005 | SDMX implementation complexity | Medium | Moderate | 9 | ONS has SDMX expertise from economic statistics; early UNSD engagement |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: **Option 2: Comprehensive Dashboard with Open API and SDMX**

**Investment**: GBP 8M over 3 years | **Return**: GBP 12.5M over 5 years | **NPV**: GBP 3.2M | **ROI**: 56%

**Go/No-Go**: **PROCEED**

## F2. Next Steps

1. **ONS Board approval**: Q2 2026
2. **UKSA Assessment Team pre-engagement**: Q2 2026
3. **Indicator gap analysis**: Comprehensive assessment of 244 indicators against UK data sources — Q3 2026
4. **UNSD liaison**: Agree SDMX submission format and schedule — Q3 2026
5. **Procurement**: G-Cloud/DOS6 for external development resource — Q3 2026

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO, Deputy National Statistician | | |
| | ONS Finance Director | | |
| | National Statistician | | |

**Approval Decision**: PENDING

---

**END OF STRATEGIC OUTLINE BUSINESS CASE**

*Document created using ArcKit `/arckit.sobc` command*
*Template version: 1.0*
*Green Book compliant: Yes (HM Treasury 5-case model)*

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG Progress Dashboard
**Model**: Claude Opus 4.6
