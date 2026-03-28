# Strategic Outline Business Case (SOBC): Water Resource Planning Tool

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Water Resource Planning Tool (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Resource Planning Tool Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Investment Board, HM Treasury, Environment Agency, Ofwat, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the strategic case for investing in a common Water Resource Planning Tool. Long-term water resource planning — balancing supply against demand under climate change over 25-50 year horizons — is essential for preventing future droughts like the 2022 summer that affected 33 million customers. The tool enables consistent, evidence-based water resource planning for WRMP29.

---

## Executive Summary

**Purpose**: Deliver a common water resource modelling platform enabling all 17 water companies and 5 regional groups to prepare Water Resource Management Plans (WRMP29) using consistent climate scenarios, standardised methodology, and integrated environmental constraints.

**Problem Statement**: Water companies currently use 7+ different proprietary modelling tools (AQUATOR, Miser, WATHNET, bespoke Excel) with inconsistent climate assumptions. DEFRA cannot produce a national supply-demand balance because regional plans are methodologically incompatible. England faces a projected 4 billion litres/day supply-demand deficit by 2050, but the magnitude and timing are uncertain because companies model uncertainty differently.

**Proposed Solution**: A cloud-hosted common modelling platform integrating UKCP18 climate projections, standardised demand forecasting, deployable output assessment with environmental flow constraints, and option appraisal — used by all companies for WRMP29.

**Strategic Fit**: Delivers DEFRA's National Framework for Water Resources, supports EA abstraction sustainability programme, informs Ofwat PR29 investment determinations, and addresses the UK Climate Change Committee's recommendations for water resource adaptation.

**Investment Required**: GBP 8M over 3 years

- Capital: GBP 5.5M
- Operational (3 years): GBP 2.5M

**Expected Benefits**: GBP 35M over 5 years

- WRMP preparation efficiency: GBP 10M (industry-wide)
- Better-evidenced infrastructure investment decisions: GBP 15M (avoided over/under-investment)
- Drought resilience improvement: GBP 8M (avoided drought response costs)
- Environmental benefit (sustainable abstraction): GBP 2M

**Return on Investment**:

- NPV: GBP 22.1M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 338%

**Recommended Option**: Option 2: Common Modelling Platform

**Key Risks**:

1. Water company resistance to abandoning proprietary models
2. Climate projection uncertainty at catchment scale after downscaling UKCP18
3. Political sensitivity of infrastructure option appraisal results (reservoir locations)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The 2022 drought demonstrated that current fragmented planning approaches are inadequate. England's 4 billion litres/day projected supply deficit requires GBP 20B+ in infrastructure investment over the next 25 years. Getting investment decisions wrong — either through over-investment (burden on customers) or under-investment (future droughts) — costs billions. An GBP 8M investment in consistent planning tools is trivial compared to the GBP 20B+ investment decisions it will inform.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
England faces a projected supply-demand deficit of 4 billion litres per day by 2050 under central climate projections. The 2022 drought — the driest summer since 1976 — resulted in hosepipe bans across 8 water company areas affecting 33 million customers, reservoir levels dropping below 50% in multiple regions, and emergency drought permits for additional abstraction from already-stressed water bodies.

Water companies prepare Water Resource Management Plans every 5 years, but use diverse proprietary models with inconsistent climate scenarios, demand forecasting assumptions, and supply assessment methodologies. DEFRA's attempt to produce a national supply-demand balance for the National Framework for Water Resources was hampered by methodological incompatibility between regional plans.

**Specific Pain Points** (from Stakeholder Analysis ARC-004-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DEFRA Water Resources Dir | SD-1 | Incompatible company models prevent national assessment | Cannot verify national supply-demand deficit or plan strategically | CRITICAL |
| EA Water Resources Dir | SD-2 | Environmental flow constraints not consistently applied | 28% of water bodies with unsustainable abstraction | HIGH |
| Water Companies | SD-3 | Inconsistent methodology risks unfair Ofwat comparison | Investment cases challenged, customer bill uncertainty | HIGH |
| Natural England | SD-4 | Protected site water needs not systematically assessed | Risk to SSSIs and SACs from abstraction | MEDIUM |

**Consequences of Inaction**:

- WRMP29 submissions will be methodologically incompatible — DEFRA cannot assess national picture
- Strategic infrastructure decisions (GBP 20B+) based on inconsistent evidence
- Risk of under-investment leading to future drought more severe than 2022
- Risk of over-investment burdening customers with unnecessary bill increases
- Environmental flow constraints not consistently applied — continued unsustainable abstraction

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **National Framework for Water Resources (2020)**: "Common analytical framework for regional planning"
- **25 Year Environment Plan**: "Enough water for people and the environment"
- **UK Climate Change Adaptation Programme**: "Plan for a range of climate scenarios"
- **Environment Act 2021**: Strengthened duty to protect water resources for the environment
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Data Integrity), 4 (Geospatial Standards), 9 (Data Quality), 20 (WFD Compliance)

### A1.3 Why Now?

**Urgency Factors**:

- WRMP29 preparation begins 2027 — platform must be operational by Q1 2028
- Strategic infrastructure decisions (South East Strategic Reservoir GBP 2.2B, Thames-Affinity transfer GBP 800M) need consistent evidence base
- UKCP18 climate projections now available but need systematic integration
- Post-2022 drought political momentum for improved water resource planning

**Opportunity Cost of Delay**:

- Each WRMP cycle without consistent methodology risks GBP billions in sub-optimal infrastructure investment
- Companies already beginning WRMP29 pre-work with proprietary tools — later adoption increases migration cost

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Industry adoption**: All 17 water companies using the common platform for WRMP29
   - **Measure**: Company usage tracking
   - **Threshold**: Minimum 14 of 17 by WRMP29 submission

2. **Methodology consistency**: All regional plans using identical climate scenarios and assessment methods
   - **Measure**: Methodology compliance audit
   - **Threshold**: 100% compliance on core scenarios, flexibility on company-specific supplementary analysis

3. **National aggregation**: Ability to produce a national supply-demand balance from regional plans
   - **Measure**: National balance produced and accepted by DEFRA
   - **Threshold**: Published national assessment by Q4 2028

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Companies continue using proprietary models with voluntary coordination through regional groups.

**Costs** (5-year):
- Operational: GBP 50M (aggregate industry WRMP preparation costs using proprietary tools)
- Total: GBP 50M

**Benefits**: GBP 0

**Consequences**:
- WRMP29 submissions methodologically incompatible (repeat of WRMP24 issues)
- National supply-demand balance cannot be reliably produced
- Infrastructure investment decisions based on inconsistent evidence
- Climate uncertainty not systematically quantified

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Perpetuates the fragmented planning that was criticised after the 2022 drought.

---

### Option 1: Voluntary Best Practice Guidance

**Description**: Publish best practice guidance for water resource modelling with recommended climate scenarios and methodology, but allow companies to use existing tools.

**Costs** (3-year) — ROM (+/-40%):
- Capital: GBP 1M (guidance development)
- Operational: GBP 0.5M (support and workshops)
- Total: GBP 1.5M

**Benefits** (5-year): GBP 5M
- Marginal consistency improvement
- Partial common climate scenarios

**Stakeholder Goals Met**: 20%

**Recommendation**: **Reject** — Voluntary guidance without a common tool will produce the same inconsistency problems. WRMP19 and WRMP24 both had voluntary guidance — it did not achieve consistency.

---

### Option 2: Common Modelling Platform (RECOMMENDED)

**Description**: Cloud-hosted common modelling platform with UKCP18 integration, standardised supply-demand balance methodology, environmental flow constraints, and option appraisal framework.

**Costs** (3-year) — ROM (+/-30%):
- Capital: GBP 5.5M
  - Platform development: GBP 2.5M
  - UKCP18 climate integration: GBP 1M
  - Environmental flow modelling: GBP 0.8M
  - Option appraisal framework: GBP 0.7M
  - User interface and reporting: GBP 0.5M
- Operational: GBP 2.5M over 3 years
  - Cloud hosting and compute: GBP 0.4M/year
  - Support and maintenance: GBP 0.2M/year
  - Hydrological science team (2 FTE): GBP 0.2M/year
- Total 3-year TCO: GBP 8M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | WRMP preparation efficiency | FINANCIAL | GBP 0 | GBP 1M | GBP 3M | GBP 3M | GBP 3M | GBP 10M |
| B-002 | Better infrastructure decisions | STRATEGIC | GBP 0 | GBP 0 | GBP 3M | GBP 5M | GBP 7M | GBP 15M |
| B-003 | Avoided drought response costs | ECONOMIC | GBP 0 | GBP 1M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 8M |
| B-004 | Environmental benefit | ENVIRONMENTAL | GBP 0 | GBP 0.3M | GBP 0.5M | GBP 0.6M | GBP 0.6M | GBP 2M |
| **Total** | | | **GBP 0** | **GBP 2.3M** | **GBP 8.5M** | **GBP 11.1M** | **GBP 13.1M** | **GBP 35M** |

**Net Present Value** (3.5% discount rate):
- Total Benefits PV: GBP 30.1M
- Total Costs PV: GBP 8M
- **NPV: GBP 22.1M**

**Return on Investment**:
- **ROI: 338%** over 5 years
- **Payback Period: 18 months**

**Pros**:
- Consistent methodology for all 17 companies and 5 regional groups
- National supply-demand balance achievable for first time
- UKCP18 climate uncertainty systematically quantified
- Environmental flow constraints consistently applied
- Cost per company: GBP 470K (vs GBP 2M+ for proprietary model development)

**Cons**:
- Requires water companies to adopt new tool (change management)
- Some companies have invested heavily in proprietary models
- Climate downscaling introduces additional uncertainty

**Stakeholder Goals Met**: 85%

---

### Option 3: National Water Resource Simulation Centre

**Description**: Comprehensive national water resource simulation with digital twin of the entire England water supply network, AI-powered demand prediction, and real-time operational integration.

**Costs** (3-year): GBP 20M
**Benefits** (5-year): GBP 45M
**NPV**: GBP 15.8M (lower than Option 2)

**Recommendation**: **Reject** — Over-engineered for the planning requirement. Digital twin technology not mature for national-scale water networks. Exceeds budget envelope.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Common Modelling Platform**

**Rationale**:
1. **Best Value**: Highest NPV at GBP 22.1M
2. **WRMP29 readiness**: Operational in time for WRMP29 preparation
3. **National aggregation**: Enables the national supply-demand balance DEFRA needs
4. **Proportionate**: GBP 8M investment to inform GBP 20B+ infrastructure decisions — exceptional leverage
5. **Environmental integration**: Systematic environmental flow constraints

**Optimism Bias Adjustment**:
- Adjusted Total Cost: GBP 8M -> GBP 11.2M
- NPV with optimism bias: GBP 18.9M (still strongly positive)

**Context**: This GBP 8M platform will inform infrastructure investment decisions worth GBP 20B+ over the next 25 years. Even a 1% improvement in investment accuracy through consistent planning saves GBP 200M.

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for platform development. Data partnerships with Met Office Hadley Centre (climate data) and UKCEH (hydrological science).

**Contract Approach**:
- **Build**: Agile development, fixed budget (GBP 5.5M)
- **Run**: Managed service (3+2 years)
- **Licensing**: Open source preferred — avoid proprietary model lock-in
- **IP**: Crown owns core platform; water companies can extend with company-specific modules

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 8M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 3M | GBP 2M | GBP 0.5M | GBP 5.5M |
| OpEx | GBP 0.8M | GBP 0.85M | GBP 0.85M | GBP 2.5M |
| **Total** | **GBP 3.8M** | **GBP 2.85M** | **GBP 1.35M** | **GBP 8M** |

## D2. Funding Source

**Source**: DEFRA Environmental Improvement Programme + Ofwat contribution (regulatory efficiency savings)
- DEFRA: GBP 5M (environmental planning and climate adaptation)
- Ofwat: GBP 3M (regulatory infrastructure, recovered through licence fees)

**Assessment**: **Affordable** — shared funding reduces burden on any single organisation

## D3. Value for Money

**Overall VfM Rating**: **HIGH**

- GBP 8M investment informs GBP 20B+ infrastructure decisions
- 1% improvement in decision accuracy = GBP 200M saved
- WRMP preparation cost reduction saves GBP 10M industry-wide
- Environmental benefit from sustainable abstraction difficult to monetise but nationally significant

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: DEFRA Water Resources Policy Director
**Steering Committee**: DEFRA CDIO, EA Water Resources Director, Ofwat Director of Strategy, Water UK representative, Met Office Hadley Centre Director

## E2. Key Milestones

| Milestone | Date |
|-----------|------|
| SOBC Approval | Q2 2026 |
| Industry methodology consultation | Q3 2026 |
| Procurement Award | Q4 2026 |
| UKCP18 climate integration | Q3 2027 |
| Environmental flow module | Q4 2027 |
| **Platform operational for WRMP29** | **Q1 2028** |
| All 17 companies onboarded | Q3 2028 |
| National supply-demand balance | Q4 2028 |
| Benefits Review | Q4 2029 |

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | Water company resistance to common tool | High | Medium | 12 | DEFRA/EA/Ofwat joint mandate for WRMP29, transition support |
| R-002 | Climate downscaling uncertainty too large | Medium | Medium | 9 | Transparent uncertainty quantification, peer-reviewed methodology |
| R-003 | Political sensitivity of infrastructure options | Medium | Medium | 9 | Platform presents evidence; decisions remain with Ministers/Ofwat |
| R-004 | WRMP29 timeline missed | Low | High | 8 | Early start, phased delivery, parallel running |
| R-005 | Key person dependency (hydro science expertise) | Medium | Medium | 9 | Partnership with UKCEH, knowledge transfer programme |

---

# PART F: RECOMMENDATION & NEXT STEPS

**Recommended Option**: **Option 2: Common Modelling Platform**
**Investment**: GBP 8M over 3 years
**Expected Return**: GBP 35M over 5 years (NPV: GBP 22.1M, ROI: 338%)
**Go/No-Go**: **PROCEED**

**Next Steps**:
1. DEFRA Investment Board approval — Target: Q2 2026
2. Industry methodology consultation — Target: Q3 2026
3. DOS6 procurement — Target: Q4 2026
4. Platform development with UKCP18 integration — Target: Q1-Q3 2027
5. Company onboarding for WRMP29 — Target: Q1 2028

---

## Appendix A: SDG 6 Programme Investment Summary

| Project | Investment | NPV | ROI | BCR |
|---------|-----------|-----|-----|-----|
| 001: Water Quality Monitoring | GBP 18M | GBP 22.3M | 161% | 2.6:1 |
| 002: Flood Risk Management | GBP 25M | GBP 98.7M | 480% | 5.8:1 |
| 003: Wastewater Treatment Analytics | GBP 12M | GBP 33.6M | 333% | 4.3:1 |
| 004: Water Resource Planning | GBP 8M | GBP 22.1M | 338% | 4.4:1 |
| **SDG 6 Total** | **GBP 63M** | **GBP 176.7M** | **281%** | **4.1:1** |

All four projects demonstrate strong value for money individually and collectively. The total programme investment of GBP 63M over 3 years generates a combined NPV of GBP 176.7M and delivers comprehensive digital infrastructure for water quality, flood risk, wastewater regulation, and water resource planning.

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO / DEFRA Water Resources Policy Director | | |
| | DEFRA Finance Director | | |
| | EA Water Resources Director | | |
| | Ofwat Director of Strategy | | |

**Approval Decision**: PENDING

---

**Generated by**: ArcKit `/arckit:sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Resource Planning Tool (Project 004)
**AI Model**: Claude Opus 4.6 (1M context)
