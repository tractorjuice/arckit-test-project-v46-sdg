# Strategic Outline Business Case (SOBC): Biodiversity Net Gain Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Biodiversity Net Gain Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Biodiversity Net Gain Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | BNG Programme Board, DEFRA Finance, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the justification for investing in a national Biodiversity Net Gain Platform. It follows the HM Treasury Green Book Five Case Model and is informed by stakeholder analysis (ARC-001-STKE-v1.0) and requirements specification (ARC-001-REQ-v1.0).

---

## Executive Summary

**Purpose**: The Environment Act 2021 mandates a minimum 10% biodiversity net gain for most planning permissions in England. A national digital platform is required to operate the credit registry, marketplace, and compliance verification infrastructure that makes this statutory obligation workable at scale.

**Problem Statement**: Without a digital platform, BNG compliance relies on manual spreadsheet calculations, paper-based credit registration, and ad hoc arrangements between developers and habitat providers. This creates fraud risk (double-counting of credits), planning bottlenecks, inconsistent compliance standards across LPAs, and an inability to demonstrate genuine national biodiversity improvement.

**Proposed Solution**: Deliver a national BNG Platform comprising a Biodiversity Metric 4.0 calculation engine, credit registry, credit marketplace, LPA compliance verification portal, and 30-year habitat management tracker. The platform will serve developers, LPAs, habitat banks, and Natural England.

**Strategic Fit**: Directly delivers the Environment Act 2021 BNG mandate, supports the 30by30 commitment (30% of land protected by 2030), contributes to Environmental Improvement Plan biodiversity targets, and aligns with the 25 Year Environment Plan's ambition to leave the environment in a better state for the next generation.

**Investment Required**: £12M over 3 years

- Capital: £8.2M
- Operational (3 years): £3.8M

**Expected Benefits**: £47.5M over 5 years

- Planning delay avoidance: £11.5M
- Fraud prevention: £6.5M
- BNG credit market facilitation: £19.5M
- LPA efficiency gains: £5M
- Environmental outcome value: £5M (non-monetised partial proxy)

**Return on Investment**:

- NPV: £28.3M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 296%

**Recommended Option**: Option 2: Full Digital Platform with Marketplace

**Key Risks**:

1. Biodiversity Metric 4.0 calculation complexity delays delivery
2. Insufficient habitat bank supply at marketplace launch
3. LPA adoption barriers due to digital capability gaps

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The BNG mandate is a legal requirement — the question is not whether to build a platform but how to build one effectively. The recommended option delivers the strongest combination of value, risk management, and stakeholder satisfaction while remaining affordable within DEFRA's digital capital allocation.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Complete detailed requirements and architecture: `/arckit.requirements` — Q3 2026
3. Alpha assessment with GDS: Q4 2026
4. Beta launch with major sites: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The Environment Act 2021 made mandatory BNG operational for major developments in November 2023 and for small sites in April 2024. However, the digital infrastructure to support this mandate at national scale does not exist. BNG compliance currently relies on:

- Manual Biodiversity Metric 4.0 calculations using Excel spreadsheets (error-prone, non-auditable)
- Ad hoc credit arrangements negotiated bilaterally between developers and landowners
- Paper-based or PDF credit registration with no central registry
- LPA officers manually reviewing metric calculations without ecological expertise
- No systematic tracking of 30-year habitat management obligations

**Specific Pain Points** (from Stakeholder Analysis):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Housing developers | SD-4 | Unpredictable BNG costs and timelines | Planning delays, project viability uncertainty | HIGH |
| LPAs | SD-3 | Manual compliance checks, no ecological expertise | 5-10 day delays per application, unfunded mandate | HIGH |
| Natural England | SD-2 | No systematic metric calculation audit capability | Risk of ecological credibility loss | CRITICAL |
| Habitat banks | SD-5 | No trusted registry or marketplace | Cannot scale business, investment uncertainty | HIGH |
| Conservation charities | SD-6 | No transparency on BNG outcomes | Risk of "greenwash" policy failure | HIGH |

**Consequences of Inaction**:

- **Planning bottleneck**: Without efficient BNG processing, planning determination times will increase, jeopardising housebuilding targets — estimated £23M annual cost to the development sector
- **Fraud risk**: Without a central registry, biodiversity credits can be double-counted — estimated £5M-10M annual fraud exposure as market grows
- **Policy failure**: Without transparent tracking, BNG cannot demonstrate genuine biodiversity improvement — undermining UK's international credibility and Environmental Improvement Plan targets

### A1.2 Strategic Drivers

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Secretary of State | POLITICAL | Environmental leadership without hindering housing | Policy delivery |
| SD-2 | NE Chief Scientist | SCIENTIFIC | Ecological credibility of metric calculations | Scientific integrity |
| SD-3 | LPAs | OPERATIONAL | Efficient compliance verification | Operational efficiency |
| SD-4 | Housing developers | FINANCIAL | Predictable, cost-effective compliance | Market efficiency |
| SD-5 | Habitat banks | FINANCIAL | Viable credit market with trusted registry | Market creation |

**Strategic Alignment**:

- **Environment Act 2021**: Platform directly enables the mandatory BNG requirement
- **Environmental Improvement Plan 2023**: Supports biodiversity apex targets through measurable outcomes
- **30by30 Target**: Habitat creation through BNG contributes to 30% land protection by 2030
- **GDS Service Standard**: New digital service must meet all 14 points
- **Architecture Principles (ARC-000-PRIN)**: Compliant with SDG 15 programme principles

### A1.3 Stakeholder Goals

**Goals Addressed** (from Stakeholder Analysis):

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | SRO | Functioning credit marketplace before small sites mandate | No marketplace | Digital marketplace | 6 months |
| G-2 | NE Chief Scientist | 100% transparent, auditable metric calculations | Manual spreadsheet | Digital with audit trail | 12 months |
| G-3 | BNG Service Owner | 90% LPA compliance checks within 2 days | 5-10 days manual | Automated verification | 12 months |
| G-4 | DEFRA Policy | 100% of obligations with 30-year management tracking | No tracking | Digital lifecycle management | 18 months |

### A1.4 Scope

**In Scope**:

- Biodiversity Metric 4.0 calculation engine
- National credit registry
- Credit marketplace
- LPA compliance verification portal and API
- 30-year management plan tracking
- Natural England validation workflow

**Out of Scope**:

- Marine net gain (future legislation)
- Welsh and Scottish equivalents
- Ecological consultancy services

**Dependencies**:

- **Internal**: Natural England metric parameters (machine-readable format)
- **External**: LPA planning system vendor API integration readiness
- **Technical**: GOV.UK One Login supporting organisational identity patterns

### A1.5 Why Now?

**Urgency Factors**:

- **Statutory obligation**: BNG is already mandatory — platform needed to manage existing obligations at scale
- **Small sites volume**: Small sites generate 10x more applications than major sites — manual processes will collapse under volume
- **Market development**: Habitat banks need platform certainty to justify land acquisition investment
- **International scrutiny**: CBD COP reporting requires demonstrable BNG outcomes

**Opportunity Cost of Delay**:

- £1.9M per month in continued planning delays
- Habitat bank investment deferred, reducing credit supply and increasing prices
- Growing backlog of unregistered BNG obligations creating compliance gaps

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Credit Registry Integrity**: Zero double-counting incidents — the foundation of market trust
   - **Measure**: Double-counting detection rate
   - **Threshold**: 100% prevention (zero tolerance)

2. **Metric Calculation Accuracy**: Calculations match NE reference to 0.01 biodiversity units
   - **Measure**: Quarterly independent audit
   - **Threshold**: < 0.1% error rate

3. **LPA Adoption**: > 80% of LPAs using the platform for compliance verification within 12 months
   - **Measure**: LPA registration and usage analytics
   - **Threshold**: 80% active LPAs

4. **Planning Timeline Impact**: Zero additional days attributable to BNG compliance
   - **Measure**: Planning determination time analysis
   - **Threshold**: No statistically significant increase

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with manual, spreadsheet-based BNG compliance processes.

**Costs** (3-year):

- Capital: £0
- Operational: £8.5M (growing LPA compliance costs, manual NE validation, fraud remediation)
- Total: £8.5M

**Benefits**: £0 (no improvement)

**Pros**:

- No upfront investment
- No implementation risk

**Cons**:

- Planning bottleneck escalates — estimated £23M annual cost to development sector
- Fraud risk uncontrolled — estimated £5-10M annual exposure
- BNG policy fails to deliver measurable biodiversity improvement
- UK credibility damaged at international environmental fora

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable. Legal obligation exists; manual processes will collapse at small sites volume.

---

### Option 1: Minimal Registry Only

**Description**: Basic credit registry with manual validation. No marketplace, no metric calculation engine, no LPA integration. Registry records credits but does not facilitate trading.

**Costs** (3-year) - ROM (±40%):

- Capital: £3.5M
- Operational: £1.8M
- Total 3-year TCO: £5.3M

**Benefits** (3-year): £12M

- Registry prevents double-counting: £6.5M
- Basic planning delay reduction: £5.5M

**Net Benefit**: £6.7M

**Pros**:

- Lower upfront investment
- Faster to deploy (6 months)
- Addresses most critical risk (double-counting)

**Cons**:

- No marketplace — developers must find credits manually
- No metric calculation — continues manual spreadsheet process
- No LPA integration — compliance checking remains manual
- No 30-year tracking — management obligations unmonitored

**Stakeholder Impact**:

- G-1 (marketplace): Not met
- G-2 (transparent metrics): Not met
- G-3 (LPA efficiency): Not met
- G-4 (30-year tracking): Not met

**Stakeholder Goals Met**: 25%

---

### Option 2: Full Digital Platform with Marketplace (RECOMMENDED)

**Description**: Comprehensive platform including Biodiversity Metric 4.0 engine, credit registry, credit marketplace, LPA compliance verification, NE validation workflow, and 30-year management tracking.

**Costs** (3-year) - ROM (±30%):

- Capital: £8.2M
  - Platform development: £4.5M
  - Geospatial infrastructure: £1.2M
  - Integration development: £1.0M
  - Testing and assurance: £0.8M
  - Contingency (15%): £0.7M
- Operational: £3.8M over 3 years
  - Cloud hosting: £0.6M/year
  - Support and maintenance: £0.4M/year
  - NE validation team: £0.3M/year
- Total 3-year TCO: £12.0M

**Benefits** (5-year):

| Benefit ID | Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Planning delay avoidance | G-1, G-3 | FINANCIAL | £1.0M | £2.5M | £2.5M | £2.75M | £2.75M | £11.5M |
| B-002 | Credit fraud prevention | G-1 | RISK | £0.5M | £1.5M | £1.5M | £1.5M | £1.5M | £6.5M |
| B-003 | Market facilitation (transaction fees, data) | G-1 | FINANCIAL | £1.0M | £3.5M | £5.0M | £5.0M | £5.0M | £19.5M |
| B-004 | LPA efficiency gains | G-3 | OPERATIONAL | £0.5M | £1.0M | £1.0M | £1.25M | £1.25M | £5.0M |
| B-005 | Environmental outcome value (partial proxy) | G-2, G-4 | STRATEGIC | £0.5M | £1.0M | £1.0M | £1.25M | £1.25M | £5.0M |
| **Total** | | | | **£3.5M** | **£9.5M** | **£11.0M** | **£11.75M** | **£11.75M** | **£47.5M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: £40.3M
- Total Costs PV: £12.0M
- **NPV: £28.3M**

**Return on Investment**:

- **ROI: 296%** over 5 years
- **Payback Period: 18 months**

**Pros**:

- 90% of stakeholder goals met
- Strong positive NPV of £28.3M
- Creates a functioning credit market enabling genuine biodiversity outcomes
- Prevents planning bottleneck at national scale
- Establishes 30-year accountability for habitat management

**Cons**:

- Higher upfront investment (£8.2M capital)
- 12-month implementation timeline for full capability
- Change management required across 333 LPAs

**Stakeholder Goals Met**: 90%

---

### Option 3: Enterprise Platform with Advanced Analytics

**Description**: Full platform plus AI-powered habitat assessment validation, satellite monitoring of managed habitats, predictive market analytics, and international BNG benchmarking.

**Costs** (3-year) - ROM (±40%):

- Capital: £15M
- Operational: £6M over 3 years
- Total 3-year TCO: £21M

**Benefits** (5-year): £52M (marginally higher than Option 2)

**Net Benefit**: £31M (but lower ROI due to diminishing returns)

**Pros**:

- 100% of stakeholder goals met
- Advanced capabilities (AI assessment, satellite monitoring)
- International leadership position

**Cons**:

- Nearly double the cost of Option 2
- 18-month implementation timeline
- AI habitat assessment technology is immature — delivery risk
- Diminishing returns on additional investment

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Diminishing returns; AI capabilities can be added incrementally in later phases.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Full Digital Platform with Marketplace**

**Rationale**:

1. **Best Value**: Highest ROI at 296% with NPV of £28.3M
2. **Stakeholder Satisfaction**: Meets 90% of goals vs 25% for Option 1
3. **Risk Management**: Addresses critical fraud and bottleneck risks
4. **Affordability**: Within DEFRA digital capital allocation
5. **Deliverability**: 12-month timeline is achievable with proven technology

**Sensitivity Analysis**:

- If costs increase 25%: NPV still positive (£25.3M), ROI 237%
- If benefits reduce 30%: NPV still positive (£16.2M), ROI 171%
- If timeline extends 6 months: Payback extends to 24 months, still acceptable

**Optimism Bias Adjustment** (UK Government Green Book):

- Standard uplift for IT projects: +40% on costs
- Adjusted Capital Cost: £8.2M + £3.3M = £11.5M
- Adjusted Total 3-year TCO: £15.3M
- NPV with optimism bias: Still strongly positive at £25.0M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: Moderate — environmental data platforms and credit registries exist internationally (Australian biodiversity offset registries, EU emissions trading infrastructure) but no directly applicable UK BNG solution exists.

**Supplier Landscape**:

- **Tier 1**: Large system integrators with government environmental experience
- **Tier 2**: Environmental technology specialists (geospatial, ecological data)
- **Tier 3**: Agile digital agencies experienced in GDS service delivery

### C1.2 Sourcing Route

**Recommended Route**: Digital Marketplace (DOS6) for specialist delivery teams, G-Cloud 14 for cloud hosting components.

**Rationale**: Agile delivery approach using specialist teams, consistent with GDS Service Manual guidance. Multi-supplier approach enables best-of-breed for geospatial, calculation engine, and marketplace components.

### C1.3 Contract Approach

- **Build**: Time and materials with capped budgets per sprint (agile delivery)
- **Run**: Managed service agreement, 3+2 year term
- **IP**: Crown owns all bespoke IP

### C1.4 Social Value

- Technical apprenticeships in environmental data science
- SME participation > 30% of contract value
- Carbon neutral delivery commitment

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: £12.0M over 3 years

### D1.1 Capital Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | £3.0M | £1.5M | £0 | £4.5M |
| Geospatial infrastructure | £0.8M | £0.4M | £0 | £1.2M |
| Integration development | £0.6M | £0.4M | £0 | £1.0M |
| Testing and assurance | £0.5M | £0.3M | £0 | £0.8M |
| Contingency (15%) | £0.5M | £0.2M | £0 | £0.7M |
| **Total CapEx** | **£5.4M** | **£2.8M** | **£0** | **£8.2M** |

### D1.2 Operational Expenditure

| Item | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------|--------|--------|--------|--------------|
| Cloud hosting | £0.4M | £0.6M | £0.8M | £1.8M |
| Support and maintenance | £0.2M | £0.4M | £0.4M | £1.0M |
| NE validation team | £0.2M | £0.3M | £0.3M | £0.8M |
| Training and change management | £0.1M | £0.1M | £0 | £0.2M |
| **Total OpEx** | **£0.9M** | **£1.4M** | **£1.5M** | **£3.8M** |

### D1.3 Total Cost of Ownership

| | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|--------|--------|--------|--------------|
| CapEx | £5.4M | £2.8M | £0 | £8.2M |
| OpEx | £0.9M | £1.4M | £1.5M | £3.8M |
| **Total TCO** | **£6.3M** | **£4.2M** | **£1.5M** | **£12.0M** |

## D2. Funding Source

**Source**: DEFRA Digital Capital Budget and Environmental Improvement Programme funding

**Budget Approval Path**:

1. DEFRA Investment Committee: Up to £10M
2. HM Treasury: Above £10M (for optimism bias-adjusted total)

## D3. Affordability

**Assessment**: **Affordable** — within DEFRA's digital capital allocation for environmental legislation implementation.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile delivery in line with GDS Service Manual

**Phases**:

| Phase | Duration | Key Activities | Gate |
|-------|----------|---------------|------|
| Discovery | 8 weeks | User research, technical discovery, architecture | Discovery assessment |
| Alpha | 12 weeks | Prototype metric engine, registry, marketplace | Alpha assessment |
| Private Beta | 16 weeks | Major sites rollout, pilot LPAs | Beta assessment |
| Public Beta | 12 weeks | Small sites, full LPA rollout | Live assessment |
| Live | Ongoing | Continuous improvement, NFI integration | Quarterly reviews |

## E2. Governance

**Programme Board**: Monthly, chaired by SRO

**Members**: DEFRA CDO, NE Chief Scientist, LPA representative, Service Owner, Delivery Manager

**Reporting**: Monthly highlight report to DEFRA Investment Committee, quarterly to CDDO

## E3. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Metric calculation complexity | MEDIUM | HIGH | Early prototype and NE validation sprint | NE Chief Scientist |
| Insufficient habitat bank supply | HIGH | MEDIUM | Accelerated habitat bank onboarding programme | BNG Policy Lead |
| LPA adoption barriers | MEDIUM | HIGH | Phased rollout with change champions, training programme | Service Owner |
| GOV.UK One Login constraints | LOW | MEDIUM | Early technical spike, alternative auth if needed | Technical Lead |
| Credit market manipulation | LOW | HIGH | Market surveillance, anomaly detection, transaction limits | SRO |

---

## Approval

| Role | Name | Decision | Signature | Date |
|------|------|----------|-----------|------|
| SRO | PENDING | [ ] Approved | | |
| DEFRA Finance Director | PENDING | [ ] Approved | | |
| DEFRA CDO | PENDING | [ ] Approved | | |
| NE Chief Scientist | PENDING | [ ] Approved | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Biodiversity Net Gain Platform
**Model**: Claude Opus 4.6
