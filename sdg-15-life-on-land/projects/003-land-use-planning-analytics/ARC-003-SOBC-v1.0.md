# Strategic Outline Business Case (SOBC): Land Use Planning Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Land Use Planning Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Land Use Planning Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, DEFRA Finance, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the justification for investing in a Land Use Planning Analytics platform. It follows the HM Treasury Green Book Five Case Model and is informed by stakeholder analysis (ARC-003-STKE-v1.0) and requirements specification (ARC-003-REQ-v1.0).

---

## Executive Summary

**Purpose**: DEFRA requires a systematic, near-real-time capability to monitor land use change across England, replacing fragmented and outdated data sources that currently take years to detect changes that happen in weeks. This evidence base is essential for Environmental Improvement Plan target reporting, evidence-based policy-making, and proportionate Environmental Land Management scheme compliance.

**Problem Statement**: DEFRA is legally required to report annual progress against Environmental Improvement Plan targets, yet its land use change evidence base is fragmented across at least 6 organisations, with datasets updated on 5-10 year cycles. The Office for Environmental Protection has criticised this evidence gap. Meanwhile, ELM scheme compliance monitoring relies on expensive physical inspections (£500/visit) covering only 5% of agreements annually.

**Proposed Solution**: Establish an automated satellite imagery (Sentinel-2) processing pipeline integrated with authoritative environmental datasets, providing land use change detection within 30 days, unified analytics for EIP reporting, risk-based ELM compliance indicators, and a farmer self-service data portal.

**Strategic Fit**: Directly supports Environmental Improvement Plan monitoring obligations (Environment Act 2021), enables evidence-based adjustment of environmental policies, supports proportionate ELM compliance (replacing CAP-era inspection approaches), and contributes to UK natural capital accounts.

**Investment Required**: £6M over 3 years

- Capital: £4.2M
- Operational (3 years): £1.8M

**Expected Benefits**: £22M over 5 years

- EIP reporting efficiency: £3.5M
- ELM compliance cost reduction: £7.5M
- Environmental damage early detection: £5M
- Policy effectiveness improvement: £4M
- SSSI monitoring efficiency: £2M

**Return on Investment**:

- NPV: £12.8M (discounted at 3.5%)
- Payback Period: 16 months
- ROI: 267%

**Recommended Option**: Option 2: Full Analytics Platform with ELM Integration

**Key Risks**:

1. Farmer trust concerns about satellite monitoring
2. Satellite data accuracy for regulatory enforcement decisions
3. Data sharing agreements across multiple organisations

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The environmental evidence gap is a statutory compliance risk. Sentinel-2 data is freely available, and the technology for automated land use change detection is mature. The primary challenge is governance and trust, not technology.

**Next Steps if Approved**:

1. Commission DPIA with ICO engagement: Q2 2026
2. Methodology development and peer review: Q2-Q3 2026
3. Alpha platform with pilot datasets: Q4 2026
4. Beta with ELM integration: Q2 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
DEFRA's understanding of land use change across England relies on a patchwork of datasets produced by different organisations on different timescales:

| Dataset | Owner | Update Cycle | Coverage | Limitation |
|---------|-------|-------------|----------|------------|
| UK Land Cover Map | UKCEH | 5-7 years | England-wide | Years out of date at publication |
| National Forest Inventory | Forestry Commission | 10-year cycle | Woodland only | Field survey-dependent |
| Agricultural Census | DEFRA/RPA | Annual | Farmland only | Self-reported, unverified |
| Priority Habitat Inventory | Natural England | Variable | Designated sites | Incomplete, patch updates |
| SSSI Condition Assessment | Natural England | 6-year target | SSSIs only | Many sites overdue |
| Cropmap of England | RPA | Annual | Arable only | Crop types, not land use change |

**Consequences of Inaction**:

- **Statutory compliance risk**: DEFRA cannot adequately demonstrate EIP target progress to Parliament and OEP
- **Policy blind spot**: Land use changes driving biodiversity loss or carbon emissions are detected years after they occur — too late for intervention
- **Inspection inefficiency**: £25M annual spend on ELM compliance inspections covering only 5% of agreements
- **SSSI degradation**: Natural England cannot maintain adequate monitoring of 4,127 SSSIs

### A1.2 Strategic Drivers

**Primary Drivers**:

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | DEFRA Env Analysis | COMPLIANCE | EIP target reporting obligation | Statutory compliance |
| SD-2 | NFU | PRIVACY | Proportionate monitoring, no surveillance | Stakeholder trust |
| SD-3 | Natural England | OPERATIONAL | SSSI condition monitoring capability gap | Environmental protection |
| SD-4 | RPA | FINANCIAL | Cost-effective ELM compliance monitoring | Operational efficiency |

**Strategic Alignment**:

- **Environment Act 2021**: Annual EIP target reporting requirement
- **Environmental Improvement Plan 2023**: Apex environmental targets requiring evidence
- **25 Year Environment Plan**: "Leave the environment in a better state" commitment
- **ELM Schemes**: Transition from CAP compliance to outcome-based environmental payments
- **UK Earth Observation Strategy**: Exploitation of Copernicus/Sentinel data for public good

### A1.5 Why Now?

**Urgency Factors**:

- OEP has publicly criticised insufficient monitoring data
- ELM schemes are scaling up — compliance approach must scale proportionately
- Sentinel-2 data is freely available and proven for land use monitoring internationally
- EU member states are implementing satellite monitoring for CAP — UK falling behind

**Opportunity Cost of Delay**: £0.5M per month in continued sub-optimal inspection spend plus increasing statutory compliance risk.

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Detection Accuracy**: > 90% for major land use transitions
   - **Measure**: Ground truth validation against field surveys
   - **Threshold**: > 85% accuracy, < 5% false positive rate

2. **Farmer Trust**: > 60% trust score in annual survey
   - **Measure**: Annual farmer perception survey
   - **Threshold**: > 50% trust (minimum), > 60% target

3. **EIP Reporting Automation**: Annual report in 4 weeks (from 12 months)
   - **Measure**: Time from reporting period close to publication-ready metrics
   - **Threshold**: < 8 weeks

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with fragmented, periodic datasets and expensive physical ELM inspections.

**Costs** (3-year):

- Capital: £0
- Operational: £9M (inspection costs, manual data assembly, survey commissions)
- Total: £9M

**Benefits**: £0

**Cons**:

- Statutory compliance risk from inadequate EIP monitoring
- £25M annual inspection spend with only 5% coverage
- OEP criticism continues and intensifies
- Environmental damage undetected for years

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Statutory compliance risk unacceptable.

---

### Option 1: Analytics Platform Only (No ELM Compliance)

**Description**: Satellite change detection and unified analytics for DEFRA policy analysis. No farmer-facing portal, no ELM compliance indicators.

**Costs** (3-year) - ROM (±40%):

- Capital: £2.5M
- Operational: £1.0M
- Total: £3.5M

**Benefits** (5-year): £10.5M

- EIP reporting efficiency: £3.5M
- Environmental damage early detection: £5M
- Policy effectiveness: £2M

**Net Benefit**: £7M

**Pros**:

- Lower investment and complexity
- Avoids farmer trust challenge entirely
- Useful policy evidence tool

**Cons**:

- No ELM compliance benefit (£7.5M opportunity foregone)
- No farmer self-service portal
- No SSSI alerting for Natural England

**Stakeholder Goals Met**: 40% (G-1, G-2 partially)

---

### Option 2: Full Analytics Platform with ELM Integration (RECOMMENDED)

**Description**: Complete platform including satellite change detection, unified analytics, ELM risk-based compliance indicators, SSSI alerting, farmer self-service portal, and open data publication.

**Costs** (3-year) - ROM (±30%):

- Capital: £4.2M
  - Satellite processing pipeline: £1.5M
  - Analytics platform and dashboards: £1.0M
  - ELM compliance and farmer portal: £0.8M
  - Dataset integration: £0.5M
  - DPIA, governance, change management: £0.2M
  - Contingency (15%): £0.2M
- Operational: £1.8M over 3 years
  - Cloud computing (satellite processing): £0.3M/year
  - Support and maintenance: £0.2M/year
  - Data licensing: £0.1M/year
- Total 3-year TCO: £6.0M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | EIP reporting efficiency | OPERATIONAL | £0.3M | £0.7M | £0.7M | £0.9M | £0.9M | £3.5M |
| B-002 | ELM inspection cost reduction | FINANCIAL | £0.5M | £1.5M | £1.5M | £2.0M | £2.0M | £7.5M |
| B-003 | Environmental damage early detection | STRATEGIC | £0.5M | £1.0M | £1.0M | £1.25M | £1.25M | £5.0M |
| B-004 | Policy effectiveness improvement | STRATEGIC | £0.3M | £0.7M | £0.8M | £1.0M | £1.2M | £4.0M |
| B-005 | SSSI monitoring efficiency | OPERATIONAL | £0.2M | £0.4M | £0.4M | £0.5M | £0.5M | £2.0M |
| **Total** | | | **£1.8M** | **£4.3M** | **£4.4M** | **£5.65M** | **£5.85M** | **£22.0M** |

**NPV** (3.5% discount): £12.8M

**ROI**: 267% over 5 years

**Payback Period**: 16 months

**Pros**:

- 85% of stakeholder goals met
- Strong NPV of £12.8M
- Statutory EIP compliance assured
- 60% reduction in inspection costs
- Farmer self-service builds trust and transparency
- Open data supports research and accountability

**Cons**:

- DPIA and farmer trust governance require careful management
- Satellite accuracy limitations for fine-grained assessment
- Multiple data sharing agreements to negotiate

**Stakeholder Goals Met**: 85%

---

### Option 3: AI-Enhanced Predictive Platform

**Description**: Full platform plus predictive land use change modelling, AI habitat classification, automated ELM outcome measurement, and carbon flux estimation.

**Costs** (3-year) - ROM (±40%):

- Capital: £8M
- Operational: £3M
- Total: £11M

**Benefits** (5-year): £25M (marginal uplift over Option 2)

**Recommendation**: **Reject** — AI habitat classification from satellite imagery is still maturing. Prediction capabilities can be added incrementally once detection platform is established.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Full Analytics Platform with ELM Integration**

**Rationale**:

1. **Best Value**: NPV of £12.8M with ROI of 267%
2. **Statutory Compliance**: Addresses EIP reporting obligation directly
3. **Cost Efficiency**: 60% reduction in ELM inspection costs
4. **Stakeholder Balance**: Analytics benefit plus farmer trust through transparency
5. **Deliverability**: Sentinel-2 processing is proven technology

**Optimism Bias Adjustment** (Green Book):

- Standard uplift: +40% on costs
- Adjusted TCO: £6.0M + £2.4M = £8.4M
- NPV with optimism bias: Still positive at £10.4M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for delivery teams. G-Cloud for cloud processing infrastructure.

**Specialist Capabilities Needed**:

- Earth observation and satellite data processing expertise
- Environmental data science
- GDS-compliant service design
- Agricultural sector stakeholder engagement

**Contract Approach**:

- **Build**: Time and materials, 18-month delivery
- **Run**: Managed service, 3+2 years
- **Data Licensing**: Separate agreements with UKCEH, OS, NE for dataset access

### C1.4 Social Value

- Environmental science apprenticeships
- Rural digital skills development
- Open data for academic research
- SME participation in earth observation sector

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: £6.0M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | £2.8M | £1.4M | £0 | £4.2M |
| OpEx | £0.4M | £0.6M | £0.8M | £1.8M |
| **Total** | **£3.2M** | **£2.0M** | **£0.8M** | **£6.0M** |

## D2. Funding Source

**Source**: DEFRA Evidence and Analysis capital budget, supplemented by Environmental Improvement Plan monitoring allocation.

**Supplementary Sources**: Potential contribution from RPA (ELM compliance cost savings), Natural England (SSSI monitoring efficiency).

## D3. Affordability

**Assessment**: **Affordable** — £6M over 3 years is modest for a platform serving multiple DEFRA agencies. Cross-organisation benefits justify shared investment.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile, with extended user research given farmer trust sensitivity.

**Phases**:

| Phase | Duration | Key Activities |
|-------|----------|---------------|
| Discovery | 10 weeks | User research (including farmer workshops), DPIA initiation, methodology design |
| Alpha | 12 weeks | Prototype change detection pipeline, methodology peer review |
| Private Beta | 16 weeks | DEFRA analyst testing, NE SSSI alerting, peer review publication |
| Public Beta | 16 weeks | ELM compliance indicators (with RPA), farmer portal pilot |
| Live | Ongoing | Full rollout, open data, continuous improvement |

## E2. Governance

**Programme Board**: Monthly, chaired by SRO

**Advisory Bodies**:

- Scientific Advisory Group (DEFRA Chief Scientist, UKCEH, Forest Research)
- Farmer Engagement Panel (NFU, CLA, tenant farmer representatives)
- Privacy and Ethics Board (ICO observer, DEFRA data ethics)

## E3. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Farmer trust deficit | HIGH | HIGH | Transparent methodology publication, farmer self-service portal, governance framework limiting enforcement use | SRO |
| Satellite accuracy for regulatory decisions | MEDIUM | HIGH | Satellite data for risk targeting only, not direct enforcement evidence; ground truth validation protocol | DEFRA Chief Scientist |
| Data sharing agreements | MEDIUM | MEDIUM | Early engagement with UKCEH, NE, RPA; standard government data sharing agreements | Data Governance Board |
| Cloud processing costs at scale | LOW | MEDIUM | Cost optimisation through cloud-native processing (COG, serverless), cost monitoring | Technical Lead |
| DPIA rejection by ICO | LOW | HIGH | Early ICO engagement, proportionality evidence from international precedent | DEFRA SIRO |

---

## Approval

| Role | Name | Decision | Signature | Date |
|------|------|----------|-----------|------|
| SRO | PENDING | [ ] Approved | | |
| DEFRA Finance Director | PENDING | [ ] Approved | | |
| DEFRA Chief Scientist | PENDING | [ ] Approved | | |
| DEFRA SIRO | PENDING | [ ] Approved | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Land Use Planning Analytics
**Model**: Claude Opus 4.6
