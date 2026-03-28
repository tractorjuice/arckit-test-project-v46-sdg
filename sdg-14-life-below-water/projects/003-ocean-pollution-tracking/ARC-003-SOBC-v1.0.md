# Strategic Outline Business Case (SOBC): Ocean Pollution Tracking

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Ocean Pollution Tracking (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Ocean Pollution Tracking Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Pollution Programme Board, DEFRA Finance, EA Finance, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case establishes the strategic justification for investment in an Ocean Pollution Tracking platform integrating marine litter, chemical contamination, sewage discharges, and oil spill monitoring data.

---

## Executive Summary

**Purpose**: Marine pollution is one of the highest-profile environmental issues in the UK, yet monitoring data is fragmented across multiple agencies and systems. The public cannot access timely, reliable information about water quality at the beaches they visit. The Environment Act 2021 created new monitoring duties but no unified platform to integrate the data.

**Problem Statement**: Storm overflow EDM data, bathing water sample results, marine litter surveys, chemical contaminant monitoring, and oil spill records sit in separate systems managed by different organisations. EA enforcement officers manually collate data from 4+ systems to build prosecution cases. OSPAR MSFD reporting requires 4 months of manual data assembly.

**Proposed Solution**: A cloud-hosted pollution intelligence platform integrating all marine pollution data streams, with a public-facing bathing water dashboard, enforcement evidence management, and automated OSPAR reporting.

**Strategic Fit**: Delivers Environment Act 2021 transparency commitments, supports OSPAR MSFD Descriptor 8 and 10 obligations, and directly addresses the government's commitment to cleaner seas in the 25 Year Environment Plan.

**Investment Required**: GBP 7.5M over 3 years

- Capital: GBP 5.0M
- Operational (3 years): GBP 2.5M

**Expected Benefits**: GBP 18.6M over 5 years

- EA operational efficiency: GBP 3.6M
- Public health value (reduced illness from informed bathing decisions): GBP 6.0M
- Enforcement effectiveness: GBP 2.0M
- OSPAR reporting automation: GBP 1.5M
- Tourism value (confidence in bathing water quality): GBP 5.5M

**Return on Investment**:

- NPV: GBP 7.2M (discounted at 3.5%)
- Payback Period: 24 months
- ROI: 148%

**Recommended Option**: Option 2: Integrated Pollution Intelligence Platform

**Key Risks**:

1. Water company EDM data quality inconsistent — mitigated by data validation layer and Ofwat regulatory engagement
2. Public misinterpretation of pollution data — mitigated by user research, contextual presentation, clear communications
3. Legacy WIMS migration complexity — mitigated by API integration rather than data migration

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Environment Act 2021 creates a legal obligation for near-real-time pollution data publication. Public and parliamentary pressure is intense and sustained. The investment is modest relative to water company investment in infrastructure (GBP 56 billion AMP8). The platform protects public health and UK tourism value.

**Next Steps if Approved**:

1. Secure DEFRA/EA joint approval: April 2026
2. Discovery with water company data providers: Q2 2026
3. Alpha with 3 pilot bathing waters: Q3 2026
4. Public beta before May 2027 bathing season: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Marine pollution monitoring in the UK is the responsibility of multiple agencies using separate systems. The EA monitors bathing water quality at 420+ sites through its WIMS database, processes EDM data from water companies, and responds to pollution incidents. Cefas runs the CSEMP programme monitoring chemical contaminants. MCA responds to oil spills at sea. MCS and SAS run citizen science beach survey programmes. None of these data sources are integrated.

**Specific Pain Points** (from ARC-003-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DEFRA Minister | SD-1 | Cannot provide real-time public pollution data | Political and reputational risk | CRITICAL |
| EA Water Quality | SD-2 | Data in 4+ separate systems | Incident response delay | CRITICAL |
| Water companies | SD-3 | EDM data lacks public context | Reputational damage | HIGH |
| SAS | SD-4 | No government real-time water quality service | Public health risk | MEDIUM |
| Cefas | SD-5 | OSPAR reporting manually collated | Compliance burden | HIGH |

**Consequences of Inaction**:

- Environment Act 2021 transparency commitment undelivered — parliamentary and legal challenge risk
- Public health impact: ~400,000 cases of gastrointestinal illness annually from bathing in polluted water (UKHSA estimate), many preventable with timely information
- OSPAR MSFD non-compliance for Descriptors 8 and 10
- Continued media and NGO criticism of government inaction
- Tourism sector impact: poor water quality perception affects GBP 17 billion coastal tourism industry

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **Environment Act 2021**: Sections 79-86 — storm overflow monitoring and reporting duties
- **Bathing Water Regulations 2013**: Annual classification and public information requirements
- **OSPAR Convention**: MSFD Descriptors 8 (contaminants) and 10 (marine litter)
- **25 Year Environment Plan**: Clean and plentiful water, thriving marine environment
- **Resources and Waste Strategy**: Marine litter reduction targets
- **Storm Overflow Discharge Reduction Plan**: Government target to eliminate ecological harm from overflows

### A1.5 Why Now?

**Urgency Factors**:

- Environment Act 2021 near-real-time reporting obligation in force — DEFRA must deliver
- May 2027 bathing season is the target for public dashboard launch
- Water companies investing GBP 56 billion in AMP8 (2025-2030) — data platform needed to track effectiveness
- OSPAR next assessment cycle requires improved UK data contribution
- Public and media pressure at sustained high level — parliamentary questions weekly

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Public Dashboard Live**: Before May 2027 bathing season
   - **Threshold**: Public dashboard operational covering all 420+ bathing waters

2. **EDM Data Integration**: Near-real-time from all water companies
   - **Threshold**: <2 hours data latency for 90% of water companies

3. **Public Trust**: Dashboard data is accurate and contextualised
   - **Threshold**: <1% data corrections required post-publication

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (5-year): GBP 8.0M (continued separate system operation)

**Benefits**: GBP 0

**Recommendation**: **Reject** — Legally non-compliant with Environment Act 2021.

---

### Option 1: Enhanced EA Bathing Water Page

**Description**: Upgrade the existing EA bathing water profiles on GOV.UK with EDM data display. No integration with Cefas, MCA, or litter data.

**Costs** (5-year): GBP 3.5M

**Benefits** (5-year): GBP 5.0M

**Stakeholder Goals Met**: 35%

---

### Option 2: Integrated Pollution Intelligence Platform (RECOMMENDED)

**Description**: Cloud-hosted platform integrating EDM, bathing water samples, marine litter, contaminants, and oil spill data with public dashboard, enforcement tools, and OSPAR reporting.

**Costs** (5-year) - ROM (+-30%):

- Capital: GBP 5.0M
  - Platform development: GBP 2.5M
  - EDM integration (all water companies): GBP 0.8M
  - Legacy data integration (WIMS, CSEMP): GBP 0.7M
  - Public dashboard development: GBP 0.5M
  - Security and testing: GBP 0.3M
  - Contingency: GBP 0.2M
- Operational: GBP 2.5M over 3 years (GBP 4.2M over 5 years)
  - Cloud hosting: GBP 0.3M/year
  - Support and maintenance: GBP 0.3M/year
  - Data operations: GBP 0.2M/year
- Total 5-year TCO: GBP 9.2M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | EA operational efficiency | FINANCIAL | GBP 0.2M | GBP 0.7M | GBP 0.8M | GBP 0.9M | GBP 1.0M | GBP 3.6M |
| B-002 | Public health value (avoided illness) | STRATEGIC | GBP 0.0M | GBP 1.0M | GBP 1.5M | GBP 1.5M | GBP 2.0M | GBP 6.0M |
| B-003 | Enforcement effectiveness | OPERATIONAL | GBP 0.1M | GBP 0.3M | GBP 0.5M | GBP 0.5M | GBP 0.6M | GBP 2.0M |
| B-004 | OSPAR reporting automation | FINANCIAL | GBP 0.0M | GBP 0.3M | GBP 0.3M | GBP 0.4M | GBP 0.5M | GBP 1.5M |
| B-005 | Tourism confidence value | STRATEGIC | GBP 0.0M | GBP 0.5M | GBP 1.0M | GBP 2.0M | GBP 2.0M | GBP 5.5M |
| **Total** | | | **GBP 0.3M** | **GBP 2.8M** | **GBP 4.1M** | **GBP 5.3M** | **GBP 6.1M** | **GBP 18.6M** |

**NPV** (3.5% discount rate): **GBP 7.2M**

**ROI**: **148%** over 5 years

**Payback Period**: **24 months**

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive Environmental Monitoring Platform

**Description**: Full environmental intelligence platform covering marine, river, groundwater, and atmospheric pollution with AI-driven predictive modelling and automated source attribution.

**Costs** (5-year): GBP 20.0M

**Benefits** (5-year): GBP 22.0M

**Recommendation**: **Reject at SOBC stage** — Scope too broad, disproportionate risk. Marine-focused Option 2 delivers the critical bathing water and OSPAR requirements.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 5-Year TCO | GBP 8.0M | GBP 3.5M | GBP 9.2M | GBP 20.0M |
| 5-Year Benefits | GBP 0 | GBP 5.0M | GBP 18.6M | GBP 22.0M |
| NPV | -GBP 8.0M | GBP 1.5M | GBP 7.2M | GBP 0.5M |
| Stakeholder Goals | 0% | 35% | 85% | 100% |
| Env Act Compliance | No | Partial | Yes | Yes |
| OSPAR Compliance | No | No | Yes | Yes |

**Recommended Option**: **Option 2**

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

| Component | Route | Value | Timeline |
|-----------|-------|-------|----------|
| Platform development | DOS 6 | GBP 2.5M | Q2 2026 |
| Cloud hosting | AWS via DEFRA EA | GBP 1.5M (5-year) | Existing |
| Water company integration | Direct (regulatory requirement) | GBP 0.8M | Q2 2026 |

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital | GBP 3.0M | GBP 2.0M | GBP 0.0M | GBP 5.0M |
| Operational | GBP 0.5M | GBP 0.8M | GBP 1.2M | GBP 2.5M |
| **Total** | **GBP 3.5M** | **GBP 2.8M** | **GBP 1.2M** | **GBP 7.5M** |

**Funding Source**: Joint DEFRA/EA allocation from Spending Review 2025.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Key Milestones**:

| Milestone | Date | Gate |
|-----------|------|------|
| Discovery | June 2026 | DEFRA/EA Assurance |
| Alpha (3 pilot bathing waters with EDM) | October 2026 | GDS Assessment |
| Beta (all bathing waters, public dashboard) | February 2027 | GDS Assessment |
| Live for bathing season 2027 | May 2027 | Programme Board |
| Full integration (Cefas, litter, enforcement) | October 2027 | Programme Board |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Water company EDM data quality issues | HIGH | MEDIUM | Data validation layer, Ofwat regulatory engagement | Technical Lead |
| Public misinterpretation of raw data | MEDIUM | HIGH | User research, contextual presentation, plain English | Product Owner |
| WIMS integration technical complexity | MEDIUM | MEDIUM | API integration not data migration, EA technical SMEs | Technical Lead |
| Political pressure for premature launch | MEDIUM | HIGH | Phased approach, pilot evidence before public launch | SRO |
| Bathing season deadline creates schedule risk | HIGH | HIGH | Hard scope control, MVP for season 2027, features post-launch | Delivery Manager |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environment Act 2021 | Legislation | UK Parliament | Storm overflow duties | legislation.gov.uk |
| Bathing Water Regulations 2013 | Legislation | UK Parliament | Quality standards | legislation.gov.uk |
| Storm Overflow Discharge Reduction Plan | Policy | DEFRA | Reduction targets | gov.uk |
| OSPAR CEMP Guidelines | Standard | OSPAR | Contaminant monitoring | ospar.org |
| HM Treasury Green Book | Guidance | HMT | Appraisal methodology | gov.uk |
| ARC-003-STKE-v1.0 | Architecture | SDG 14 Programme | Stakeholder analysis | Local |
| ARC-003-REQ-v1.0 | Architecture | SDG 14 Programme | Requirements specification | Local |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Ocean Pollution Tracking
**Model**: Claude Opus 4.6
