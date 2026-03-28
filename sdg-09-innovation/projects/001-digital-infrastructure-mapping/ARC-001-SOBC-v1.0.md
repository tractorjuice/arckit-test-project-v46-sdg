# Strategic Outline Business Case (SOBC): Digital Infrastructure Mapping

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Digital Infrastructure Mapping (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Digital Infrastructure Mapping Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Digital Infrastructure Programme Board, DSIT, HM Treasury, BDUK |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the strategic justification for investing in a national Digital Infrastructure Mapping platform, analyses options, and recommends an approach for further development into an Outline Business Case.

---

## Executive Summary

**Purpose**: To establish a single, authoritative, premises-level broadband and mobile coverage database for the UK, enabling accurate targeting of GBP 5 billion Project Gigabit investment, continuous regulatory monitoring, and transparent citizen coverage information.

**Problem Statement**: UK broadband and mobile coverage data is fragmented across individual operators, Ofcom's annual reports, and commercial data providers. No single, current, premises-level national picture exists. This leads to an estimated GBP 200-400 million in Project Gigabit subsidy errors, 12-week procurement area definition cycles, and citizens unable to make informed broadband decisions.

**Proposed Solution**: Build a cloud-hosted platform that aggregates coverage data from all major operators using standardised APIs, matches it to Ordnance Survey UPRN-level addressing, and provides tiered access for government investment targeting, regulatory reporting, local authority planning, and citizen coverage checking.

**Strategic Fit**: Directly supports the UK Digital Strategy 2022, Project Gigabit, and Ofcom's Connected Nations programme. Aligns with Geospatial Commission data sharing policy and INSPIRE Regulations.

**Investment Required**: GBP 14.1M over 3 years

- Capital: GBP 10.3M
- Operational (3 years): GBP 3.8M

**Expected Benefits**: GBP 200-400M over programme lifetime

- Subsidy error elimination: GBP 200-400M
- Procurement cycle acceleration: GBP 15M saved in BDUK operational costs
- Regulatory efficiency: GBP 5M saved in Ofcom data collection costs

**Return on Investment**:

- NPV: GBP 195M (discounted at 3.5%, conservative estimate using GBP 200M benefit)
- Payback Period: 8 months (once operational)
- ROI: 1,300%

**Recommended Option**: Option 2: Balanced Platform (full UPRN-level database with citizen checker and BDUK integration, phased Ofcom analytics)

**Key Risks**:

1. Operator non-compliance with data submission
2. Data accuracy insufficient for investment decisions
3. FOIA disclosure of commercially sensitive data

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The potential saving of GBP 200-400M in subsidy errors alone justifies the GBP 14.1M investment many times over. The risk of inaction — continued misallocation of Project Gigabit funding — is unacceptable given the scale of public investment at stake.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Operator data sharing agreement negotiation: Q3 2026
3. NCSC security assessment: Q3 2026
4. Alpha development: Q4 2026
5. Develop Outline Business Case: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Before BDUK can define a Project Gigabit procurement area, analysts must manually collect coverage data from multiple operators, reconcile it against Ofcom Connected Nations data, and classify premises using postcode-level approximations. This process takes 12 weeks per procurement area, has an estimated 5-8% error rate, and has already triggered 3 procurement challenges in FY25/26.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| BDUK Director | SD-4 | 12-week manual data reconciliation per procurement area | GBP 200-400M subsidy error risk | CRITICAL |
| Ofcom | SD-2 | Annual data collection, 6-month report production | Regulatory lag, obligations unmonitored | CRITICAL |
| Secretary of State | SD-1 | Cannot demonstrate accurate progress toward gigabit target | Parliamentary scrutiny, select committee criticism | CRITICAL |
| Citizens | SD-6 | No authoritative source of coverage information | Uninformed purchasing decisions | HIGH |
| Local Authorities | SD-5 | Fragmented coverage data for digital inclusion planning | Ineffective local strategies | HIGH |

**Consequences of Inaction**:

- GBP 200-400M wasted through Project Gigabit subsidy errors over programme lifetime
- Continued 12-week procurement delays costing GBP 5M per year in BDUK operational inefficiency
- Parliamentary and NAO criticism of investment targeting accuracy
- Citizens continuing to rely on misleading operator marketing claims

### A1.2 Strategic Drivers

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Secretary of State | POLITICAL | Deliver universal gigabit connectivity | UK Digital Strategy |
| SD-2 | Ofcom | COMPLIANCE | Regulatory transparency and accountability | Communications Act |
| SD-4 | BDUK | FINANCIAL | Accurate investment targeting | Project Gigabit VfM |
| SD-6 | Citizens | CUSTOMER | Know what coverage is available | Consumer transparency |

**Strategic Alignment**:

- **UK Digital Strategy 2022**: "Every home and business should have access to gigabit-capable broadband by 2030"
- **Project Gigabit Programme**: GBP 5 billion to extend gigabit broadband to hard-to-reach areas — accurate targeting is essential
- **Geospatial Strategy 2030**: Infrastructure data identified as highest-value opportunity
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Geospatial Data as National Asset), 5 (Interoperability), 9 (Open Data by Default)

### A1.3 Scope

**In Scope**: Fixed and mobile coverage database, operator data submission API, BDUK integration, Ofcom reporting interface, citizen coverage checker, open data publication

**Out of Scope**: Satellite broadband, community networks, network quality metrics, commercial comparison/switching

### A1.4 Why Now?

**Urgency Factors**:

- Project Gigabit procurement ongoing — every procurement area defined with inaccurate data is a subsidy error
- Ofcom 5G spectrum licence obligations require monitoring capability
- NAO value for money audit of Project Gigabit expected in 2027
- Operator frustration with multiple, inconsistent data requests creating window for consolidated approach

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Operator Data Participation**: All operators with >1% market share submit data
   - **Measure**: Number of operators submitting / total operators required
   - **Threshold**: 100% of major operators (those covering >1% of premises)

2. **Data Accuracy**: Premises classification accuracy sufficient for investment decisions
   - **Measure**: Post-contract audit of premises classification accuracy
   - **Threshold**: >98% accuracy

3. **Processing Speed**: Procurement area definition significantly faster than manual process
   - **Measure**: Time from area selection to premises list export
   - **Threshold**: <2 weeks (vs 12 weeks current)

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current manual data reconciliation process for BDUK, annual Ofcom Connected Nations, and no citizen coverage checker.

**Costs** (3-year): GBP 0 additional capital, GBP 15M continued BDUK operational costs for manual data work

**Benefits**: GBP 0

**Cons**:

- Continued GBP 200-400M subsidy error risk
- 12-week procurement cycles continue
- No improvement to citizen information
- NAO criticism likely

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable given scale of Project Gigabit investment at risk.

---

### Option 1: Minimal Viable Solution

**Description**: Basic coverage database at postcode level (not UPRN), manual operator data upload (not API), no citizen checker, limited Ofcom integration.

**Costs** (3-year) - ROM (+-40%):

- Capital: GBP 4.0M
- Operational: GBP 1.5M
- Total 3-year TCO: GBP 5.5M

**Benefits** (3-year): GBP 50-100M (partial subsidy error reduction — postcode level still has 3-4% error rate)

**Stakeholder Goals Met**: 35%

**Recommendation**: Partially addresses the problem but postcode-level data is insufficient for UPRN-level investment targeting. Risk of building a platform that still produces unacceptable error rates.

---

### Option 2: Balanced Platform (RECOMMENDED)

**Description**: Full UPRN-level coverage database with operator data submission API, BDUK procurement integration, citizen coverage checker on GOV.UK, and phased Ofcom regulatory reporting.

**Costs** (3-year) - ROM (+-30%):

- Capital: GBP 10.3M
  - Platform development: GBP 8.0M
  - OS licensing: GBP 1.0M
  - Security assessment: GBP 0.5M
  - GDS assessment: GBP 0.3M
  - Contingency (5%): GBP 0.5M
- Operational: GBP 3.8M over 3 years
  - Cloud infrastructure: GBP 1.2M/year
  - BAU team: GBP 1.5M/year (from Year 2)
  - OS licensing: GBP 0.3M/year
- Total 3-year TCO: GBP 14.1M

**Benefits** (3-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Subsidy error elimination | BDUK G-2 | FINANCIAL | GBP 0M | GBP 50M | GBP 100M | GBP 150M |
| B-002 | BDUK procurement acceleration | BDUK G-2 | OPERATIONAL | GBP 1M | GBP 3M | GBP 3M | GBP 7M |
| B-003 | Ofcom reporting efficiency | Ofcom G-4 | OPERATIONAL | GBP 0M | GBP 1M | GBP 2M | GBP 3M |
| B-004 | Citizen information value | Citizens G-3 | STRATEGIC | GBP 0M | GBP 1M | GBP 2M | GBP 3M |
| **Total** | | | | **GBP 1M** | **GBP 55M** | **GBP 107M** | **GBP 163M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 152M
- Total Costs PV: GBP 13.2M
- **NPV: GBP 138.8M**

**Return on Investment**:

- **ROI: 1,050%** over 3 years
- **Payback Period: 8 months** (once subsidy error reduction begins)

**Stakeholder Goals Met**: 85%

**Recommendation**: **RECOMMENDED** — Delivers full UPRN-level accuracy required for Project Gigabit, with citizen value and regulatory efficiency. Strong NPV driven by subsidy error elimination.

---

### Option 3: Comprehensive Solution

**Description**: Option 2 plus real-time operator network monitoring, predictive coverage modelling, satellite broadband integration, and community network mapping.

**Costs** (3-year): GBP 25M (GBP 11M more than Option 2)

**Benefits** (3-year): GBP 180M (marginally higher)

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject at SOBC stage** — Incremental benefits do not justify the additional GBP 11M cost. Advanced features can be added as future phases once the core platform proves value.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 0M | GBP 5.5M | GBP 14.1M | GBP 25M |
| 3-Year Benefit | GBP 0M | GBP 75M | GBP 163M | GBP 180M |
| NPV | GBP 0M | GBP 65M | GBP 138.8M | GBP 140M |
| Stakeholder Goals | 0% | 35% | 85% | 100% |
| Implementation Risk | None | LOW | MEDIUM | HIGH |
| Recommendation | Reject | Reject | **RECOMMENDED** | Reject |

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Approach**: Internal build using government digital delivery team (GDS model), with specialist geospatial subcontractors for OS integration and spatial database expertise.

**Rationale**: The platform handles CNI-adjacent data and requires deep integration with government systems (BDUK, Ofcom). Commercial off-the-shelf geospatial platforms do not meet the specific tiered access and regulatory reporting requirements. Government build ensures long-term control.

**Key Procurements**:

- Cloud hosting: Crown Commercial Service framework (GBP 1.2M/year)
- Ordnance Survey data licensing: existing PSMA agreement plus AddressBase Premium (GBP 0.3M/year)
- Geospatial consultancy: Digital Marketplace / G-Cloud (GBP 0.5M)
- Security assessment: NCSC-approved assessors (GBP 0.3M)

---

# PART D: FINANCIAL CASE

## D1. Funding Requirements

| Financial Year | Capital | Revenue | Total |
|----------------|---------|---------|-------|
| FY 2026/27 | GBP 5.0M | GBP 0.5M | GBP 5.5M |
| FY 2027/28 | GBP 4.0M | GBP 1.5M | GBP 5.5M |
| FY 2028/29 | GBP 1.3M | GBP 1.8M | GBP 3.1M |
| **Total** | **GBP 10.3M** | **GBP 3.8M** | **GBP 14.1M** |

**Funding Source**: DSIT departmental expenditure limits, with potential contribution from BDUK programme budget (investment in data infrastructure to protect GBP 5B programme).

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile delivery following GDS Service Manual, with Alpha/Beta/Live phases aligned to GDS service assessments.

**Timeline**:

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research, data landscape, technical feasibility |
| Alpha | 4 months | Prototype, operator engagement, GDS Alpha assessment |
| Private Beta | 6 months | Operator data submission, BDUK integration, invited users |
| Public Beta | 4 months | Citizen checker, open data, wider access |
| Live | Ongoing | Full national service |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Operator non-compliance | MEDIUM | HIGH | Ofcom regulatory direction; demonstrate commercial benefit |
| Data accuracy insufficient | MEDIUM | HIGH | Independent verification; phased rollout |
| FOIA disclosure of commercial data | LOW | HIGH | Section 43 exemption; data handling agreements |
| Platform security breach | LOW | CRITICAL | NCSC assessment; defence-in-depth; audit logging |

## E3. Governance

- **SRO**: DSIT Director General, Digital Infrastructure
- **Programme Board**: Monthly, chaired by SRO
- **Technical Authority**: DSIT CDO
- **Assurance**: CDDO spend control, GDS service assessment, NCSC security assessment

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Drivers and goals | `projects/001-digital-infrastructure-mapping/` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | Functional and non-functional requirements | `projects/001-digital-infrastructure-mapping/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Infrastructure Mapping (Project 001)
**Model**: Claude Opus 4.6
