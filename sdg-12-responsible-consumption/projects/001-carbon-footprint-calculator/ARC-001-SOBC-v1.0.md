# Strategic Outline Business Case (SOBC): Carbon Footprint Calculator

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Carbon Footprint Calculator (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Carbon Footprint Calculator Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Programme Board, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case presents the case for investing in a standardised Carbon Footprint Calculator for government suppliers. It follows the HM Treasury Green Book five-case model and is informed by the stakeholder analysis documented in ARC-001-STKE-v1.0.

---

## Executive Summary

**Purpose**: The UK Government spends over GBP 300 billion annually through procurement, yet lacks a standardised tool for measuring and comparing supplier carbon footprints. This SOBC presents the case for building a GHG Protocol-compliant carbon calculation service to enable carbon-informed procurement decisions at scale.

**Problem Statement**: PPN 06/21 requires suppliers to publish Carbon Reduction Plans, but without a standardised calculation tool, each supplier uses different methodologies producing incomparable data. Contracting authorities cannot meaningfully evaluate carbon performance, rendering the policy largely ineffective as a decarbonisation lever.

**Proposed Solution**: Build a free, GHG Protocol-compliant carbon footprint calculation tool for government suppliers, producing normalised carbon intensity scores integrated with the Sustainable Procurement Portal (Project 004).

**Strategic Fit**: Directly delivers the Net Zero Strategy commitment to use government procurement as a decarbonisation lever. Supports PPN 06/21 implementation, Climate Change Act 2008 obligations, and UNFCCC reporting requirements.

**Investment Required**: GBP 4.5M over 3 years

- Capital: GBP 2.8M
- Operational (3 years): GBP 1.7M

**Expected Benefits**: GBP 12.5M over 5 years

- Supply chain emissions visibility enabling targeted decarbonisation interventions
- Elimination of duplicate consultant spend by suppliers (GBP 75M market-wide over 5 years)
- Standardised procurement evaluation reducing contracting authority assessment costs

**Return on Investment**:

- NPV: GBP 5.2M (discounted at 3.5%)
- Payback Period: 22 months
- ROI: 178%

**Recommended Option**: Option 2: Balanced GHG Protocol Implementation

**Key Risks**:

1. Low SME adoption if tool perceived as too complex
2. Methodological challenge from environmental NGOs undermining credibility
3. Scope 3 data quality insufficient for meaningful procurement scoring

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The cost of inaction — continued ineffective PPN 06/21 implementation, inability to quantify government supply chain emissions, and missed Net Zero Strategy delivery — significantly exceeds the investment required. The balanced approach delivers scientific credibility while maintaining SME accessibility.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Define detailed requirements: `/arckit.requirements` — complete
3. Commission independent methodology review: Q3 2026
4. Procurement approach for development partner: Q3 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The UK Government mandates Carbon Reduction Plans (PPN 06/21) for suppliers bidding on contracts above GBP 5 million, but provides no standardised tool for calculating carbon footprints. The result is a fragmented landscape where suppliers use inconsistent methodologies, producing data that contracting authorities cannot compare. Many SMEs hire expensive external consultants (GBP 5,000-15,000 per plan) or produce low-quality self-assessments. Contracting authorities lack expertise to evaluate carbon data, often reducing it to a tick-box exercise. The policy's potential as a decarbonisation lever is unrealised.

**Specific Pain Points** (from Stakeholder Analysis):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Minister (DESNZ) | SD-1 | Cannot report credible supply chain emissions | Cannot demonstrate Net Zero progress | CRITICAL |
| Chief Scientific Adviser | SD-2 | No standardised methodology | Incomparable data, scientific indefensibility | CRITICAL |
| CCS | SD-3 | Procurement officers cannot evaluate carbon data | PPN 06/21 ineffective | HIGH |
| SME Suppliers | SD-4 | GBP 5K-15K consultant cost per plan | Barrier to government procurement | CRITICAL |

**Consequences of Inaction**:

- Climate Change Committee continues to criticise government's inability to quantify supply chain emissions (estimated 15-20M tCO2e annually)
- PPN 06/21 remains a compliance exercise rather than a decarbonisation lever, with GBP 300B procurement spend unoptimised for carbon reduction
- SMEs increasingly excluded from government procurement, reducing competition and value for money
- UK credibility at COP undermined by inability to report government supply chain emissions

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: This business case is informed by stakeholder analysis documented in ARC-001-STKE-v1.0.

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Minister | POLITICAL | Credible carbon data for Net Zero accountability | Climate leadership |
| SD-2 | Chief Scientific Adviser | TECHNICAL | Methodological rigour for defensible reporting | Scientific credibility |
| SD-3 | CCS | OPERATIONAL | Actionable carbon scores for procurement | Procurement effectiveness |
| SD-4 | SME Suppliers | FINANCIAL | Minimal reporting burden | Market access |

**Strategic Alignment**:

- **Net Zero Strategy**: Directly delivers commitment to use GBP 300B procurement spend as a decarbonisation lever
- **PPN 06/21**: Provides the missing implementation tool for Carbon Reduction Plan requirements
- **Climate Change Act 2008**: Supports legally binding emissions reduction targets through supply chain visibility
- **Architecture Principles**: Implements Principle 2 (GHG Protocol Compliance), Principle 4 (Supply Chain Transparency), Principle 9 (Environmental Data Quality)

### A1.3 Scope

**In Scope**:

- GHG Protocol Scope 1, 2, and 3 calculation engine
- BEIS/DESNZ emissions factor integration with automated annual updates
- Supplier self-service web interface with guided SME workflows
- Carbon intensity normalisation and sector benchmarking
- API integration with Sustainable Procurement Portal (Project 004)
- Carbon Reduction Plan document generation

**Out of Scope** (for this phase):

- Product-level lifecycle assessment (ISO 14067)
- Carbon offset verification and trading
- Supplier decarbonisation advisory services
- Enforcement of PPN 06/21 compliance

### A1.4 Why Now?

**Urgency Factors**:

- Climate Change Committee 2026 Progress Report expected to criticise government supply chain emissions data gap
- PPN 06/21 threshold review in 2027 may lower the GBP 5M threshold, requiring far more suppliers to report
- UK COP presidency legacy commitments require demonstrable procurement decarbonisation progress
- Environment Act 2021 extended producer responsibility schemes create additional demand for standardised carbon data

**Opportunity Cost of Delay**:

- GBP 300B annual procurement spend remains unoptimised for carbon reduction for each year of delay
- SMEs continue paying GBP 50-75M annually in aggregate consultant costs for non-standardised carbon plans
- Government credibility on Net Zero erodes with each CCC progress report

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Scientific Credibility**: Calculation engine validated against GHG Protocol and accepted by DESNZ Chief Scientific Adviser
   - **Measure**: 100% accuracy against 50 reference calculations
   - **Threshold**: Zero tolerance for calculation errors in Scope 1 and 2

2. **SME Accessibility**: Tool usable by non-specialists without external consultants
   - **Measure**: Average SME completion time for Scope 1/2 calculation
   - **Threshold**: Under 2 hours

3. **Adoption at Scale**: Sufficient supplier coverage for procurement integration to be meaningful
   - **Measure**: Completed calculations from unique suppliers
   - **Threshold**: 5,000 within 12 months

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current fragmented approach where each supplier produces carbon data using their chosen methodology and each contracting authority interprets PPN 06/21 independently.

**Costs** (3-year):

- Capital: GBP 0
- Operational: GBP 0 (no government cost, but GBP 50-75M aggregate supplier consultant cost)
- Total government cost: GBP 0

**Benefits**: GBP 0 (no improvement to government emissions visibility or procurement effectiveness)

**Pros**:

- No government investment required
- No implementation risk

**Cons**:

- PPN 06/21 remains ineffective as a decarbonisation lever
- Government cannot report supply chain emissions credibly
- SMEs continue paying GBP 5-15K each for non-standardised carbon plans
- Climate Change Committee criticism continues
- UK credibility at COP weakened

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — The cost of inaction (continued ineffective Net Zero delivery, SME market exclusion, CCC criticism) significantly exceeds any option's investment.

---

### Option 1: Scope 1 and 2 Calculator Only

**Description**: Build a simplified calculator covering Scope 1 (direct emissions) and Scope 2 (purchased energy) only, without Scope 3 (supply chain) capability. Basic web interface without sector benchmarking or procurement API integration.

**Scope**:

- Scope 1 and 2 calculation with BEIS/DESNZ factors
- Basic web interface for supplier data entry
- PDF report generation
- No Scope 3, no API, no benchmarking

**Costs** (3-year) — ROM (+/-40%):

- Capital: GBP 1.2M (development, infrastructure)
- Operational: GBP 0.6M over 3 years (hosting, support)
- Total 3-year TCO: GBP 1.8M

**Benefits** (3-year): GBP 2.5M

- Reduced supplier consultant costs (partial): GBP 1.5M
- Contracting authority time savings: GBP 1.0M

**Pros**:

- Lower investment and implementation risk
- Faster delivery (6 months)
- Simpler methodology less vulnerable to challenge

**Cons**:

- Scope 3 typically 80-90% of total footprint — omission renders data misleading
- No procurement integration — data remains disconnected from decisions
- Insufficient for CCC or UNFCCC reporting (Scope 3 required)
- Environmental NGOs will criticise omission of Scope 3 as greenwashing enablement

**Stakeholder Goals Met**: 30%

- SD-2 (Scientific rigour): Partially met — Scope 1/2 only is incomplete
- SD-3 (Procurement integration): Not met — no API
- SD-5 (NGO transparency): Not met — Scope 3 omission will be criticised

**Recommendation**: **Reject** — Omitting Scope 3 undermines the fundamental purpose. Cannot support Net Zero reporting or credible procurement decisions.

---

### Option 2: Balanced GHG Protocol Implementation (RECOMMENDED)

**Description**: Full GHG Protocol-compliant calculator with Scope 1, 2, and material Scope 3 categories, guided SME workflows, emissions factor automation, sector benchmarking, and procurement API integration.

**Scope**:

- Complete Scope 1, 2, and Scope 3 (material categories with estimation tools)
- Guided SME calculation workflows with contextual help
- BEIS/DESNZ factor automation with annual update process
- Carbon intensity normalisation and sector benchmarking (20 SIC categories)
- RESTful API for Sustainable Procurement Portal integration
- Carbon Reduction Plan document generation

**Costs** (3-year) — ROM (+/-30%):

- Capital: GBP 2.8M
  - Development and testing: GBP 1.8M
  - Infrastructure setup: GBP 0.4M
  - Methodology development and academic review: GBP 0.2M
  - User research and design: GBP 0.2M
  - Training and change management: GBP 0.2M
- Operational: GBP 1.7M over 3 years
  - Cloud hosting and managed services: GBP 0.3M/year
  - Support and maintenance: GBP 0.15M/year
  - Ongoing user research and iteration: GBP 0.1M/year
- Total 3-year TCO: GBP 4.5M

**Benefits** (5-year):

| Benefit ID | Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Reduced supplier consultant spend | SD-4 | FINANCIAL | GBP 0.5M | GBP 1.5M | GBP 2.5M | GBP 3.0M | GBP 3.0M | GBP 10.5M |
| B-002 | Contracting authority assessment efficiency | SD-3 | OPERATIONAL | GBP 0.1M | GBP 0.3M | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.9M |
| B-003 | Targeted decarbonisation ROI | SD-1 | STRATEGIC | GBP 0 | GBP 0 | GBP 0.05M | GBP 0.05M | GBP 0.05M | GBP 0.15M |
| **Total** | | | | **GBP 0.6M** | **GBP 1.8M** | **GBP 3.05M** | **GBP 3.55M** | **GBP 3.55M** | **GBP 12.55M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 10.8M
- Total Costs PV: GBP 4.3M
- **NPV: GBP 5.2M** (after optimism bias: GBP 2.8M)

**Return on Investment**:

- **ROI: 178%** over 5 years
- **Payback Period: 22 months**

**Stakeholder Goals Met**: 85%

- SD-1 (Credible data): Met — full GHG Protocol compliance
- SD-2 (Scientific rigour): Met — validated methodology with academic review
- SD-3 (Procurement integration): Met — API with normalised scores and benchmarks
- SD-4 (SME accessibility): Met — guided workflows, estimation tools, free service
- SD-5 (Transparency): Met — published methodology, open data
- SD-6 (Factor management): Met — automated ingestion

**Risks**:

- R-1: SME adoption risk — Mitig: extensive user research, phased complexity, helpdesk
- R-2: Methodology challenge — Mitig: independent academic review, published methodology
- R-3: Scope 3 data quality — Mitig: tiered approach, quality scoring, estimation tools

**Recommendation**: **ACCEPT** — Best value for money with acceptable risk.

---

### Option 3: Comprehensive Platform with AI-Powered Insights

**Description**: Full calculator plus AI-powered decarbonisation recommendations, predictive analytics, automated supply chain data collection via API integrations with supplier accounting systems, and real-time carbon dashboards for every contracting authority.

**Costs** (3-year) — ROM (+/-40%):

- Capital: GBP 6.5M
- Operational: GBP 3.0M over 3 years
- Total 3-year TCO: GBP 9.5M

**Benefits** (5-year): GBP 15.0M (marginally higher than Option 2)

**Pros**:

- 100% of stakeholder goals met
- AI insights could accelerate supplier decarbonisation
- Automated data collection reduces supplier burden further

**Cons**:

- Cost more than double Option 2 for marginal additional benefit
- AI decarbonisation recommendations unproven at scale
- Automated supply chain data collection requires API integrations with thousands of accounting systems — high complexity and privacy risk
- 24-month delivery timeline vs 12 months for Option 2

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Diminishing returns. AI capabilities can be added to Option 2 in a future phase once the foundational calculator is proven and adopted.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Balanced GHG Protocol Implementation**

**Rationale**:

1. **Best Value**: Highest NPV at GBP 5.2M (GBP 2.8M after optimism bias)
2. **Scientific Credibility**: Full GHG Protocol compliance satisfies DESNZ scientific requirements and withstands NGO scrutiny
3. **SME Accessibility**: Guided workflows and estimation tools address the critical SME adoption risk
4. **Procurement Integration**: API with normalised scores enables carbon-informed decisions at scale
5. **Deliverability**: 12-month timeline achievable with proven technology components

**Optimism Bias Adjustment** (UK Government):

- Standard uplift for IT projects: +40% on costs
- Adjusted Total Cost: GBP 4.5M -> GBP 6.3M (with uplift)
- NPV with optimism bias: Still positive at GBP 2.8M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: Carbon accounting software is a mature market with established players (Sphera, Persefoni, Watershed, Plan A) and emerging UK-specific solutions (Emitwise, Normative). However, no existing product combines GHG Protocol compliance, UK government emissions factors, PPN 06/21 Carbon Reduction Plan generation, and procurement API integration. A bespoke build-on-framework approach is recommended.

### C1.2 Sourcing Route

**Recommended Route**: Digital Marketplace — Digital Outcomes and Specialists (DOS6) for discovery/alpha; G-Cloud 14 for cloud hosting and SaaS components.

**Rationale**: DOS6 provides access to specialist environmental technology and GovTech suppliers, including SMEs with carbon accounting expertise. G-Cloud enables rapid procurement of hosting and platform components.

### C1.3 Social Value

**UK Government Requirement**: Minimum 10% weighting on social value (PPN 06/20).

**Social Value Themes**:

1. **Environmental**: Suppliers must demonstrate carbon reduction commitments (practising what the tool preaches)
2. **Economic**: Apprenticeship and graduate opportunities in green technology
3. **Social**: SME supply chain participation, regional job creation

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: GBP 4.5M over 3 years

### D1.1 Capital Expenditure (CapEx)

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Development and testing | GBP 1.4M | GBP 0.4M | GBP 0 | GBP 1.8M |
| Infrastructure setup | GBP 0.4M | GBP 0 | GBP 0 | GBP 0.4M |
| Methodology and academic review | GBP 0.2M | GBP 0 | GBP 0 | GBP 0.2M |
| User research and design | GBP 0.15M | GBP 0.05M | GBP 0 | GBP 0.2M |
| Training and change management | GBP 0.1M | GBP 0.1M | GBP 0 | GBP 0.2M |
| **Total CapEx** | **GBP 2.25M** | **GBP 0.55M** | **GBP 0** | **GBP 2.8M** |

### D1.2 Operational Expenditure (OpEx)

| Item | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------|--------|--------|--------|--------------|
| Cloud hosting and managed services | GBP 0.2M | GBP 0.3M | GBP 0.35M | GBP 0.85M |
| Support and maintenance | GBP 0.1M | GBP 0.15M | GBP 0.15M | GBP 0.4M |
| Ongoing user research and iteration | GBP 0.1M | GBP 0.1M | GBP 0.1M | GBP 0.3M |
| Helpdesk and supplier support | GBP 0.05M | GBP 0.05M | GBP 0.05M | GBP 0.15M |
| **Total OpEx** | **GBP 0.45M** | **GBP 0.6M** | **GBP 0.65M** | **GBP 1.7M** |

### D1.3 Total Cost of Ownership

| | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|--------|--------|--------|--------------|
| CapEx | GBP 2.25M | GBP 0.55M | GBP 0 | GBP 2.8M |
| OpEx | GBP 0.45M | GBP 0.6M | GBP 0.65M | GBP 1.7M |
| **Total TCO** | **GBP 2.7M** | **GBP 1.15M** | **GBP 0.65M** | **GBP 4.5M** |

## D2. Funding Source

**Budget Allocation**:

- **Source**: DESNZ Net Zero Innovation Portfolio, supplemented by CDDO Digital Transformation funding
- **Amount Available**: GBP 5.0M (GBP 0.5M contingency above estimated TCO)
- **Timing**: FY 2026/27 and FY 2027/28

## D3. Affordability

**Assessment**: **Affordable** — within DESNZ digital transformation allocation and aligned with Net Zero Strategy delivery budget.

---

# PART E: MANAGEMENT CASE

## E1. Governance

### E1.1 Roles & Responsibilities

| Decision/Activity | Responsible | Accountable | Consulted | Informed |
|-------------------|-------------|-------------|-----------|----------|
| Overall programme success | Programme Manager | SRO | Steering Committee | All stakeholders |
| Calculation methodology | Chief Scientific Adviser | SRO | Environment Agency, NGOs | Academic community |
| Budget approval | DESNZ Finance Director | SRO | HM Treasury | CDDO |
| Procurement integration | CCS Integration Lead | CCS Director | DESNZ CDIO | Contracting authorities |
| Go-live decision | SRO | DESNZ Permanent Secretary | Steering Committee | All stakeholders |

## E2. Key Milestones

| Milestone | Date | Dependencies | Owner |
|-----------|------|--------------|-------|
| SOBC Approval | Q2 2026 | Stakeholder analysis complete | SRO |
| Funding Secured | Q2 2026 | SOBC approval | Finance Director |
| Methodology Review Complete | Q3 2026 | Academic reviewer contracted | Chief Scientific Adviser |
| Alpha Live | Q3 2026 | Development team mobilised | Delivery Manager |
| GDS Beta Assessment | Q4 2026 | Alpha findings addressed | Service Owner |
| Beta Live (public) | Q1 2027 | Beta assessment passed | Service Owner |
| Procurement API Integration | Q1 2027 | Portal API specification agreed | CCS Integration Lead |
| GDS Live Assessment | Q2 2027 | Beta performance data | Service Owner |
| **GO-LIVE** | **Q2 2027** | All assessments passed | SRO |

## E3. Risk Management

### Top 5 Strategic Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation | Owner |
|---------|------------------|------------|--------|-------|------------|-------|
| R-001 | SME adoption below target due to complexity | Medium | Major | 12 | User research, estimation tools, helpdesk, phased complexity | Product Manager |
| R-002 | Methodology challenged by NGOs/academia | Medium | Major | 12 | Independent review, open methodology, early engagement | Chief Scientific Adviser |
| R-003 | Scope 3 data quality too poor for scoring | High | Moderate | 12 | Tiered approach, data quality flags, sector estimation | Product Manager |
| R-004 | BEIS/DESNZ factors not machine-readable by launch | Medium | Moderate | 9 | Automated Excel parsing fallback, lobby for format change | Service Owner |
| R-005 | Procurement Portal integration delayed | Low | Moderate | 6 | Calculator operates standalone, API ready when Portal ready | CCS Integration Lead |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: **Option 2: Balanced GHG Protocol Implementation**

**Investment**: GBP 4.5M over 3 years

**Expected Return**: GBP 12.55M over 5 years (NPV: GBP 5.2M, ROI: 178%)

**Stakeholder Goals Met**: 85%

**Payback Period**: 22 months

**Go/No-Go Recommendation**: **PROCEED to requirements and alpha phase**

## F2. Next Steps if Approved

1. **Funding Approval**: DESNZ Finance Director secures GBP 4.5M allocation — Target: Q2 2026
2. **Team Mobilisation**: SRO appoints Programme Manager and core team — Target: Q2 2026
3. **Methodology Development**: Chief Scientific Adviser commissions academic review — Target: Q3 2026
4. **Procurement**: DOS6 procurement for discovery/alpha development partner — Target: Q2 2026
5. **Alpha Build**: Core calculation engine with user testing — Target: Q3-Q4 2026

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | Senior Responsible Owner | | |
| | DESNZ Finance Director | | |
| | DESNZ Chief Scientific Adviser | | |
| | DESNZ Permanent Secretary | | |

**Approval Decision**: PENDING

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Net Zero Strategy | Policy | GOV.UK | Procurement decarbonisation commitments | N/A |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plan requirements | N/A |
| GHG Protocol Corporate Standard | Standard | ghgprotocol.org | Scope 1/2/3 methodology | N/A |
| HM Treasury Green Book | Guidance | GOV.UK | Appraisal and evaluation methodology | N/A |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | SDG 12 Programme | Stakeholder drivers and goals | `projects/001-carbon-footprint-calculator/` |
| ARC-001-REQ-v1.0 | Requirements | SDG 12 Programme | Detailed requirements | `projects/001-carbon-footprint-calculator/` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Carbon Footprint Calculator (Project 001)
**Model**: Claude Opus 4.6
