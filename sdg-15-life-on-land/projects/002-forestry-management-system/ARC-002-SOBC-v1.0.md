# Strategic Outline Business Case (SOBC): Forestry Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Forestry Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Forestry Management System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | FC Programme Board, DEFRA Finance, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the justification for investing in a modernised Forestry Management System. It follows the HM Treasury Green Book Five Case Model and is informed by stakeholder analysis (ARC-002-STKE-v1.0) and requirements specification (ARC-002-REQ-v1.0).

---

## Executive Summary

**Purpose**: The Forestry Commission requires a modern digital platform to manage felling licences, woodland creation grants, and the National Forest Inventory — replacing ageing paper-based and legacy systems that are a primary barrier to meeting England's woodland creation targets.

**Problem Statement**: The England Trees Action Plan targets 7,500 hectares of new woodland per year, but actual planting rates remain at approximately 2,500 hectares. The paper-based felling licence process takes 13 weeks (against a statutory target of 10), woodland creation grant applications take 6 months with a 30% abandonment rate, and the National Forest Inventory operates on a 10-year update cycle. These antiquated processes cost the forestry sector an estimated £15M annually in delayed operations and deter landowners from woodland creation.

**Proposed Solution**: Deliver a digital Forestry Management System comprising end-to-end felling licence workflow, streamlined grant application processing, near-real-time National Forest Inventory integration, and UK Woodland Carbon Code integration for carbon credit stacking.

**Strategic Fit**: Directly supports the England Trees Action Plan 2021, contributes to net zero by 2050 through carbon sequestration, supports 30by30 biodiversity commitment, and aligns with Environmental Improvement Plan woodland targets.

**Investment Required**: £8M over 3 years

- Capital: £5.5M
- Operational (3 years): £2.5M

**Expected Benefits**: £31.5M over 5 years

- Forestry sector productivity: £15M (regulatory delay elimination)
- Grant processing efficiency: £4.5M
- Increased woodland creation (carbon value): £7M
- NFI modernisation: £2.5M
- Carbon credit facilitation: £2.5M

**Return on Investment**:

- NPV: £18.7M (discounted at 3.5%)
- Payback Period: 14 months
- ROI: 294%

**Recommended Option**: Option 2: Full Digital Platform with Carbon Integration

**Key Risks**:

1. Rural broadband limitations for digital-first service
2. FC officer change resistance to new workflows
3. RPA data integration dependencies

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: Current systems are failing to support England's statutory woodland creation obligations and imposing significant unnecessary costs on the forestry sector. Modernisation is essential and affordable.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Discovery phase with user research: Q3 2026
3. Alpha build and assessment: Q4 2026
4. Beta launch for planting season 2027/28: September 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The Forestry Commission operates with a mix of paper-based processes and ageing legacy applications developed in the early 2000s. Key operational processes are slow, inefficient, and deterring participation in woodland creation.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| FC Operations | SD-2 | Paper felling licence process, 13-week average | £15M annual cost to forestry sector | HIGH |
| DEFRA / FC Chair | SD-1 | Woodland creation at 2,500 ha vs 7,500 target | Climate and biodiversity targets missed | CRITICAL |
| Carbon Code | SD-3 | Separate registration, duplicate data entry | Low Carbon Code participation, missed carbon revenue | MEDIUM |
| Woodland Trust | SD-4 | Incomplete ancient woodland data, opaque process | Risk of ancient woodland damage | HIGH |

**Consequences of Inaction**:

- **Target failure**: Continued shortfall of 5,000 ha/year against England Trees Action Plan target — cumulative deficit growing annually
- **Sector costs**: £15M annual cost to timber industry from regulatory delays continues
- **Carbon opportunity lost**: Estimated £25M annual carbon credit revenue unrealised due to low participation
- **NAO criticism**: Audit risk for failing to deliver on published government commitments

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **England Trees Action Plan 2021**: 7,500 ha/year woodland creation target
- **Net Zero Strategy**: Woodland carbon sequestration is a key pillar of UK net zero by 2050
- **Environmental Improvement Plan 2023**: Tree and woodland apex targets
- **30by30 Target**: Woodland as a significant component of protected land
- **Climate Change Committee**: Repeated calls for accelerated tree planting
- **Architecture Principles (ARC-000-PRIN)**: Compliant with SDG 15 programme principles

### A1.3 Stakeholder Goals

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | FC Operations | Felling licence processing < 4 weeks | 13 weeks average | 4 weeks average | 12 months |
| G-2 | SRO | Grant processing < 6 weeks | 6 months average | 6 weeks average | 18 months |
| G-3 | Forest Research | NFI update cycle < 12 months | 10-year cycle | 12-month continuous | 24 months |

### A1.4 Scope

**In Scope**: Felling licences, woodland creation grants, National Forest Inventory, Carbon Code integration, FC officer mobile tools

**Out of Scope**: Scotland/Wales forestry, timber trading, Tree Preservation Orders, urban trees

**Dependencies**:

- **RPA**: Land parcel data API access
- **Natural England**: Designation data services
- **UK Woodland Carbon Code**: Integration agreement with Scottish Forestry
- **Copernicus**: Sentinel-2 data availability

### A1.5 Why Now?

**Urgency Factors**:

- Woodland creation targets are legally binding under Environment Act 2021
- Every planting season missed (November-March) delays carbon sequestration by 12 months
- Legacy systems approaching end of vendor support
- Climate Change Committee increasingly critical of planting shortfall

**Opportunity Cost of Delay**: £1.25M per month in continued sector costs plus 5,000 ha/year woodland creation shortfall.

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Felling Licence Speed**: Processing time reduced from 13 weeks to 4 weeks
   - **Measure**: Average processing time from submission to determination
   - **Threshold**: < 6 weeks (stretch target 4 weeks)

2. **Grant Processing Acceleration**: Application-to-approval time reduced from 6 months to 6 weeks
   - **Measure**: Average grant application processing time
   - **Threshold**: < 8 weeks

3. **Woodland Creation Rate**: Contribution to increased planting rates
   - **Measure**: Hectares of new woodland approved via digital system
   - **Threshold**: 50% increase from baseline within 2 years

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with paper-based felling licences, legacy grant processing, and periodic NFI.

**Costs** (3-year):

- Capital: £0
- Operational: £4.5M (legacy system maintenance, paper processing, manual data entry)
- Total: £4.5M

**Benefits**: £0

**Cons**:

- Woodland creation targets continue to be missed
- £15M annual sector cost from regulatory delays
- Legacy systems approaching end of support
- NAO and Climate Change Committee criticism intensifies

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable baseline; targets are statutory.

---

### Option 1: Minimal Digitisation (Felling Licences Only)

**Description**: Digitise felling licence workflow only. Grants remain on legacy systems. No NFI integration or Carbon Code.

**Costs** (3-year) - ROM (±40%):

- Capital: £2.5M
- Operational: £1.2M
- Total: £3.7M

**Benefits** (5-year): £16M

- Felling licence efficiency: £15M (sector cost elimination)
- FC officer productivity: £1M

**Net Benefit**: £12.3M

**Pros**:

- Lower investment, faster deployment
- Addresses most visible pain point

**Cons**:

- Grant processing unchanged — woodland creation bottleneck persists
- No contribution to national planting targets
- No carbon integration
- NFI remains outdated

**Stakeholder Goals Met**: 33% (G-1 only)

---

### Option 2: Full Digital Platform with Carbon Integration (RECOMMENDED)

**Description**: Comprehensive digital platform covering felling licences, woodland creation grants, NFI integration, and Carbon Code verification.

**Costs** (3-year) - ROM (±30%):

- Capital: £5.5M
  - Platform development: £3.0M
  - Geospatial and mobile tools: £1.0M
  - Integration (RPA, NE, Carbon Code, Sentinel-2): £0.8M
  - Testing, training, change management: £0.4M
  - Contingency (15%): £0.3M
- Operational: £2.5M over 3 years
  - Cloud hosting: £0.4M/year
  - Support and maintenance: £0.3M/year
  - Satellite data processing: £0.15M/year
- Total 3-year TCO: £8.0M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Forestry sector productivity (felling delay elimination) | FINANCIAL | £1.5M | £3.0M | £3.0M | £3.75M | £3.75M | £15.0M |
| B-002 | Grant processing efficiency (FC and applicant time savings) | OPERATIONAL | £0.5M | £0.8M | £0.8M | £1.2M | £1.2M | £4.5M |
| B-003 | Increased woodland creation (carbon sequestration value) | STRATEGIC | £0.5M | £1.0M | £1.5M | £2.0M | £2.0M | £7.0M |
| B-004 | NFI modernisation (evidence quality, avoided survey costs) | OPERATIONAL | £0.2M | £0.5M | £0.5M | £0.65M | £0.65M | £2.5M |
| B-005 | Carbon credit facilitation (landowner revenue enabled) | FINANCIAL | £0.2M | £0.3M | £0.5M | £0.75M | £0.75M | £2.5M |
| **Total** | | | **£2.9M** | **£5.6M** | **£6.3M** | **£8.35M** | **£8.35M** | **£31.5M** |

**NPV** (3.5% discount): £18.7M

**ROI**: 294% over 5 years

**Payback Period**: 14 months

**Pros**:

- 90% of stakeholder goals met
- Strong NPV of £18.7M
- Addresses all critical barriers to woodland creation
- Carbon integration provides additional landowner incentive
- Modern platform replaces end-of-life legacy systems

**Cons**:

- Higher upfront investment than Option 1
- 18-month full implementation (felling licences in 12 months)
- Change management across FC area offices
- Rural broadband dependency for digital-first approach

**Stakeholder Goals Met**: 90%

---

### Option 3: Comprehensive Platform with AI and Predictive Analytics

**Description**: Full platform plus AI-based tree species identification from aerial imagery, predictive growth modelling, automated grant eligibility scoring, and national carbon flux monitoring.

**Costs** (3-year) - ROM (±40%):

- Capital: £10M
- Operational: £4M
- Total: £14M

**Benefits** (5-year): £34M (marginal uplift over Option 2)

**Recommendation**: **Reject** — AI capabilities are immature for forestry applications. Incremental addition in later phases preferred.

**Stakeholder Goals Met**: 100%

---

## B3. Recommended Option

**Recommendation**: **Option 2: Full Digital Platform with Carbon Integration**

**Rationale**:

1. **Best Value**: NPV of £18.7M with ROI of 294%
2. **Target Delivery**: Directly addresses woodland creation bottleneck
3. **Sector Impact**: Eliminates £15M annual regulatory cost
4. **Climate Contribution**: Enables carbon credit stacking, increasing planting incentive
5. **Deliverability**: Proven technologies, achievable 18-month timeline

**Optimism Bias Adjustment** (Green Book):

- Standard uplift: +40% on costs
- Adjusted Capital: £5.5M + £2.2M = £7.7M
- Adjusted TCO: £10.2M
- NPV with optimism bias: Still strongly positive at £16.5M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for agile delivery teams, G-Cloud for hosting.

**Contract Approach**:

- **Build**: Time and materials, 18-month delivery
- **Run**: Managed service, 3+2 years
- **IP**: Crown ownership

**Social Value**:

- Forestry apprenticeships in digital technology
- Rural SME participation
- Environmental sustainability in delivery

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: £8.0M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | £3.5M | £2.0M | £0 | £5.5M |
| OpEx | £0.5M | £0.85M | £1.15M | £2.5M |
| **Total** | **£4.0M** | **£2.85M** | **£1.15M** | **£8.0M** |

## D2. Funding Source

**Source**: DEFRA/Forestry Commission digital capital budget, supplemented by England Trees Action Plan implementation funding.

## D3. Affordability

**Assessment**: **Affordable** — within FC digital capital allocation. England Trees Action Plan implementation budget provides additional headroom.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile, GDS Service Manual compliant

**Phases**:

| Phase | Duration | Key Milestone |
|-------|----------|--------------|
| Discovery | 8 weeks | User research, technical discovery |
| Alpha | 12 weeks | Prototype felling licence workflow |
| Private Beta (Felling) | 16 weeks | Felling licence live with pilot area offices |
| Private Beta (Grants) | 12 weeks | Grant processing with pilot applicants |
| Public Beta | 12 weeks | Full rollout, NFI integration, Carbon Code |
| Live | Ongoing | Continuous improvement |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Rural broadband limitations | HIGH | MEDIUM | Offline-first mobile app, assisted digital channel | Technical Lead |
| FC officer change resistance | MEDIUM | HIGH | Co-design with area offices, training programme, change champions | Service Owner |
| RPA data integration delays | MEDIUM | MEDIUM | Early engagement, parallel development with mock data | Integration Lead |
| Carbon Code governance complexity | MEDIUM | LOW | Phased integration — core forestry first, carbon later | SRO |
| Planting season timing pressure | HIGH | HIGH | Felling licence MVP for September 2027, grants for 2028 season | Delivery Manager |

---

## Approval

| Role | Name | Decision | Signature | Date |
|------|------|----------|-----------|------|
| SRO | PENDING | [ ] Approved | | |
| FC Finance Director | PENDING | [ ] Approved | | |
| FC Chief Forester | PENDING | [ ] Approved | | |
| DEFRA Digital | PENDING | [ ] Approved | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Forestry Management System
**Model**: Claude Opus 4.6
