# Strategic Outline Business Case (SOBC): Levelling Up Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Levelling Up Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Levelling Up Dashboard, DLUHC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Leadership, HM Treasury, ONS, Regional Mayors |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the rationale, options, and indicative costs for building a Levelling Up Dashboard — a DLUHC-operated geospatial platform for monitoring regional inequality and tracking Levelling Up Fund allocations against the 12 Levelling Up missions. It follows the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Create a unified geospatial platform providing transparent, statistically robust monitoring of regional inequality metrics and Levelling Up Fund allocations, supporting the statutory reporting obligations under the Levelling Up and Regeneration Act 2023.

**Problem Statement**: The Levelling Up and Regeneration Act 2023 requires mission reporting, but data is scattered across ONS subnational statistics, Index of Multiple Deprivation publications, and departmental fund allocation spreadsheets. No single platform links inequality metrics to investment. Ministers cannot answer constituency-specific questions, regional mayors cannot track fund impact, and parliamentary scrutiny lacks a centralised evidence base.

**Proposed Solution**: Build a public-facing geospatial dashboard integrating IMD/IoD data, ONS subnational indicators, and Levelling Up Fund allocation data, with interactive mapping from LSOA to national level, mission progress tracking, and open data publication.

**Strategic Fit**: Directly supports the Levelling Up and Regeneration Act 2023 reporting requirements, Levelling Up White Paper missions, and ministerial accountability for GBP 4.8 billion in Levelling Up Funds.

**Investment Required**: GBP 6.5M over 3 years

- Capital: GBP 3.5M
- Operational (3 years): GBP 3.0M

**Expected Benefits**: GBP 15.2M over 3 years

- Efficiency: GBP 4.5M (replacing fragmented analysis across DLUHC, HMT, and local authorities)
- Better fund allocation decisions: GBP 8.0M (1-2% improvement in GBP 4.8B fund targeting)
- Democratic accountability value: GBP 2.7M (parliamentary, mayoral, public scrutiny)

**Return on Investment**:

- NPV: GBP 7.6M (discounted at 3.5%)
- Payback Period: 12 months
- ROI: 134%

**Recommended Option**: Option 2: Balanced Approach — Full geospatial dashboard with IMD, ONS, and fund data integration

**Key Risks**:

1. Dashboard reveals worsening inequalities, creating political pressure to suppress data
2. UK Statistics Authority criticises data presentation as non-compliant with Code of Practice
3. Fund allocation tracking reveals poor value for money in specific projects

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Levelling Up and Regeneration Act 2023 creates a statutory obligation to report on missions. The current fragmented data landscape makes this impossible at the required level of geographic detail. The dashboard fulfils a legal obligation while improving the targeting of GBP 4.8 billion in Levelling Up investment.

**Next Steps if Approved**:

1. Secure DLUHC/HMT funding approval: Q2 2026
2. ONS methodology co-development: Q2-Q3 2026
3. Discovery with regional mayors and local authorities: Q3 2026
4. Alpha (geospatial prototype with IMD data): Q4 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The Levelling Up and Regeneration Act 2023 requires the government to set measurable missions for reducing geographic inequalities and report progress annually to Parliament. Since enactment, GBP 4.8 billion has been allocated through Levelling Up Funds (Rounds 1-3), the Towns Fund, UK Shared Prosperity Fund, and Community Ownership Fund. Yet there is no centralised platform linking fund allocations to inequality outcome metrics.

**Specific Pain Points** (from Stakeholder Analysis ARC-003-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Secretary of State | SD-1 | Cannot demonstrate Levelling Up progress by constituency | PQ exposure, credibility gap | CRITICAL |
| ONS | SD-2 | Risk of misleading data presentation | Code of Practice violation | CRITICAL |
| Regional mayors | SD-3 | Cannot track fund allocations to regions | Accountability gap | HIGH |
| Commons Committee | SD-4 | No centralised evidence base for scrutiny | Ineffective oversight | HIGH |

**Consequences of Inaction**:

- Statutory reporting obligation unmet — annual mission progress report to Parliament lacks geographic depth
- GBP 4.8 billion in Levelling Up investment lacks transparent tracking and outcome measurement
- Ministers vulnerable to PQs on constituency-specific inequality without ready data
- NAO value-for-money audit cannot link spending to outcomes

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **Levelling Up and Regeneration Act 2023**: Statutory mission reporting obligation
- **Levelling Up White Paper**: 12 missions with measurable targets
- **HM Treasury Green Book**: Evidence-based appraisal of public spending
- **Transparency agenda**: Open data and public accountability
- **Architecture Principles**: Principles 13 (Single Source of Truth), 19 (Levelling Up Missions Alignment), 12 (Data Quality and Lineage)

### A1.3 Scope

**In Scope**:

- IMD/IoD integration at LSOA level
- ONS subnational indicators (50+)
- Levelling Up Fund allocation tracking
- Mission progress dashboard
- Geographic analysis (LSOA to national)
- Open data publication and API
- Constituency lookup for PQ support

**Out of Scope**:

- Causal impact evaluation (separate evaluation programme)
- Fund application processing
- Real-time economic data (monthly GDP, employment)

### A1.4 Why Now?

**Urgency Factors**:

- First annual Levelling Up mission progress report due to Parliament
- NAO planning value-for-money study of Levelling Up Funds for 2027
- Regional mayors elected with mandates to track devolution impact
- Levelling Up and Regeneration Act statutory obligations now in force

**Opportunity Cost of Delay**:

- GBP 500K per month in DLUHC analyst time assembling data manually for ministerial briefings
- Risk of Code of Practice breach if data published without ONS-endorsed methodology
- GBP 4.8 billion spending decisions made without geospatial impact analysis

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Data Integration**: 15+ inequality metrics with geographic mapping live within 12 months
   - **Measure**: Metrics operational on dashboard
   - **Threshold**: Minimum 10

2. **Fund Coverage**: 100% of major Levelling Up funds tracked
   - **Measure**: Fund allocation data coverage
   - **Threshold**: Minimum 80%

3. **ONS Endorsement**: Methodology endorsed by ONS/UK Statistics Authority
   - **Measure**: Written endorsement
   - **Threshold**: No adverse findings

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with fragmented data publications and manual briefing preparation.

**Costs** (3-year):

- Capital: GBP 0
- Operational: GBP 6.0M (DLUHC analyst team, manual data assembly, ad hoc publications)
- Total: GBP 6.0M

**Benefits**: GBP 0

**Cons**:

- Statutory reporting obligation met with minimum quality
- No geographic analysis capability
- GBP 4.8B spend lacks transparent tracking
- Vulnerable to NAO and PAC criticism

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject**

---

### Option 1: Static Publication with Maps

**Description**: DLUHC publishes annual Levelling Up progress report with static maps and downloadable data tables.

**Costs** (3-year) — ROM (+-40%):

- Capital: GBP 0.5M
- Operational: GBP 1.5M
- Total: GBP 2.0M

**Benefits** (3-year): GBP 5.0M

**Pros**:

- Meets minimum statutory requirement
- Lower cost
- Quicker to deliver (6 months)

**Cons**:

- No interactive analysis — mayors and local leaders cannot explore their areas
- No real-time fund tracking
- Annual cycle too slow for parliamentary accountability
- No constituency lookup for PQ support

**Stakeholder Goals Met**: 30%

---

### Option 2: Balanced Approach (RECOMMENDED)

**Description**: Interactive geospatial dashboard with IMD/IoD, ONS subnational indicators, fund allocation tracking, mission progress, constituency lookup, and open data API.

**Costs** (3-year) — ROM (+-30%):

- Capital: GBP 3.5M
  - Platform development: GBP 1.5M
  - Geospatial engine and mapping: GBP 0.6M
  - Data integration (ONS, IMD, funds): GBP 0.5M
  - Mission progress framework: GBP 0.3M
  - Fund tracking system: GBP 0.3M
  - Open data API: GBP 0.3M
- Operational: GBP 3.0M over 3 years
  - Cloud hosting (high-performance geospatial): GBP 0.3M/year
  - Platform team (5 FTE): GBP 0.5M/year
  - ONS methodology liaison: GBP 0.1M/year
  - Data quality assurance: GBP 0.1M/year
- Total 3-year TCO: GBP 6.5M

**Benefits** (3-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|------------|------|--------|--------|--------|--------------|
| B-001 | Analysis efficiency (replaces manual data assembly) | FINANCIAL | GBP 0.5M | GBP 1.5M | GBP 2.5M | GBP 4.5M |
| B-002 | Better fund allocation decisions (1-2% improvement on GBP 4.8B) | FINANCIAL | GBP 1.0M | GBP 3.0M | GBP 4.0M | GBP 8.0M |
| B-003 | Democratic accountability (parliamentary, mayoral, public) | SOCIAL | GBP 0.3M | GBP 1.0M | GBP 1.4M | GBP 2.7M |
| **Total** | | | **GBP 1.8M** | **GBP 5.5M** | **GBP 7.9M** | **GBP 15.2M** |

**NPV**: GBP 7.6M (at 3.5% discount rate)

**ROI**: 134% over 3 years

**Payback Period**: 12 months

**Stakeholder Impact**:

- Secretary of State (SD-1): Met — constituency-level data, mission progress, PQ support
- ONS (SD-2): Met — co-developed methodology, Code of Practice compliant
- Regional mayors (SD-3): Met — regional fund tracking, benchmarking
- Commons Committee (SD-4): Met — open data, transparent methodology
- Local authorities (SD-5): Met — LSOA-level data, comparator analysis

**Stakeholder Goals Met**: 90%

---

### Option 3: Real-Time Analytics Platform

**Description**: Real-time geospatial analytics with predictive modelling, automated fund impact estimation, and machine learning-driven inequality forecasting.

**Costs** (3-year): GBP 15.0M

**Benefits** (3-year): GBP 18.0M

**NPV**: GBP 2.0M

**Cons**:

- Most inequality data is annual — "real-time" is misleading
- Predictive modelling of inequality is academically contested
- ONS unlikely to endorse ML-driven estimates as official statistics
- Disproportionate cost for marginal benefit over Option 2

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Low NPV relative to cost, methodological credibility risks.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-year cost | GBP 6.0M | GBP 2.0M | GBP 6.5M | GBP 15.0M |
| 3-year benefit | GBP 0 | GBP 5.0M | GBP 15.2M | GBP 18.0M |
| NPV | -GBP 6.0M | GBP 2.5M | GBP 7.6M | GBP 2.0M |
| Stakeholder goals met | 0% | 30% | 90% | 100% |
| ONS endorsement | N/A | Unlikely | Achievable | Risk |
| **Recommendation** | **Reject** | **Possible** | **RECOMMENDED** | **Reject** |

---

# PART C: COMMERCIAL CASE

## C1. Procurement Approach

**Strategy**: Build on open source geospatial stack (PostGIS, MapLibre GL JS, GeoServer), with CCS framework procurement for cloud hosting.

**Key Procurements**:

- Cloud hosting: CCS G-Cloud (estimated GBP 100K/year — higher due to geospatial workloads)
- Ordnance Survey data: OS OpenData (free for public sector)
- ONS data: Open data (free, API access)
- Specialist geospatial development: CCS Digital Outcomes & Specialists

**Make vs Buy**: Build. No commercial platform combines UK-specific inequality metrics, Levelling Up Fund tracking, and LSOA-level geospatial analysis.

---

# PART D: FINANCIAL CASE

## D1. Funding Requirements

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital | GBP 2.5M | GBP 0.6M | GBP 0.4M | GBP 3.5M |
| Operational | GBP 0.7M | GBP 1.0M | GBP 1.3M | GBP 3.0M |
| **Total** | **GBP 3.2M** | **GBP 1.6M** | **GBP 1.7M** | **GBP 6.5M** |

**Funding Source**: DLUHC programme budget, with potential HM Treasury co-funding given value-for-money benefits to central fund allocation decisions.

---

# PART E: MANAGEMENT CASE

## E1. Governance

- **SRO**: DLUHC Permanent Secretary (given statutory reporting obligation)
- **Programme Board**: DLUHC, HM Treasury, ONS, CDDO
- **Advisory Panel**: Regional mayors (rotating), IFS, What Works Centre
- **Delivery Methodology**: Agile (GDS phases)
- **Assurance**: GDS Service Assessment, ONS methodology review, UK Statistics Authority pre-assessment

## E2. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|-------------|
| SOBC approval | Q2 2026 | This document |
| ONS methodology co-development starts | Q2 2026 | SOBC approval |
| Discovery complete | Q3 2026 | SOBC approval |
| Alpha (IMD geospatial prototype) | Q4 2026 | ONS data access |
| Beta (full dashboard with fund tracking) | Q2 2027 | Alpha pass, fund data integration |
| ONS methodology endorsement | Q3 2027 | Methodology paper published |
| Live service | Q4 2027 | Beta pass, ONS endorsement |

## E3. Risk Summary

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Dashboard shows worsening inequalities | MEDIUM | HIGH | Present with appropriate caveats, leading indicators alongside lagging |
| UK Statistics Authority criticism | MEDIUM | HIGH | ONS co-development, pre-assessment, transparent methodology |
| Fund data reveals poor VfM | MEDIUM | MEDIUM | Data presentation is neutral — evaluation is separate |
| Pre-publication data leak | LOW | HIGH | Strict OFFICIAL-SENSITIVE classification, access controls, pre-release access rules |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Levelling Up and Regeneration Act 2023 | Legislation | legislation.gov.uk | Statutory mission reporting | N/A |
| Levelling Up White Paper | Policy | GOV.UK | 12 missions framework | N/A |
| HM Treasury Green Book | Guidance | GOV.UK | Five-case business case methodology | N/A |
| Index of Multiple Deprivation 2019 | Dataset/Methodology | DLUHC | LSOA deprivation scoring | N/A |
| ARC-003-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers | projects/003-levelling-up-dashboard/ |
| ARC-003-REQ-v1.0 | Requirements | ArcKit | Requirements specification | projects/003-levelling-up-dashboard/ |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Levelling Up Dashboard
**Model**: Claude Opus 4.6
