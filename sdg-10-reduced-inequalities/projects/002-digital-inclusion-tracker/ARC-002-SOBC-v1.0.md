# Strategic Outline Business Case (SOBC): Digital Inclusion Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Digital Inclusion Tracker (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Digital Inclusion Tracker, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Leadership, CDDO, HM Treasury, Ofcom, Good Things Foundation |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the rationale, options, and indicative costs for building a Digital Inclusion Tracker — a DSIT-operated platform that integrates digital skills, connectivity, and usage data to provide a unified, geospatial view of digital exclusion across the UK. It follows the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Create a unified data platform that integrates multiple digital inclusion data sources to enable evidence-based policy-making, targeted intervention planning, and transparent measurement of digital exclusion across the UK.

**Problem Statement**: Digital inclusion data is fragmented across annual publications from Lloyds Bank, Ofcom, ONS, and DfE, published on different timescales with different methodologies. No unified platform enables geographic analysis, benchmarking, or intervention targeting. Policy-makers and local authorities operate blind to local digital exclusion patterns.

**Proposed Solution**: Build a geospatial data platform integrating five or more authoritative data sources into a unified data model with interactive mapping, local authority benchmarking, a composite Digital Inclusion Index, and community programme impact tracking.

**Strategic Fit**: Directly supports the UK Digital Strategy commitment to improving digital inclusion, Levelling Up White Paper missions (broadband, skills), and the government's digital-by-default service strategy which depends on digital inclusion for success.

**Investment Required**: GBP 3.2M over 3 years

- Capital: GBP 1.8M
- Operational (3 years): GBP 1.4M

**Expected Benefits**: GBP 7.8M over 3 years

- Efficiency: GBP 3.0M (replacing fragmented analysis across departments and local authorities)
- Better targeting of GBP 200M+ annual digital inclusion spend: GBP 3.5M (5% improvement in targeting efficiency)
- Social value: GBP 1.3M (accelerated digital inclusion through better-targeted interventions)

**Return on Investment**:

- NPV: GBP 4.0M (discounted at 3.5%)
- Payback Period: 16 months
- ROI: 144%

**Recommended Option**: Option 2: Balanced Approach — Unified platform with five data sources, geospatial analysis, and community data integration

**Key Risks**:

1. Data latency — most sources update annually, undermining perceived real-time value
2. Small-area estimates statistically unreliable for some metrics
3. Composite index methodology contested by data providers

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK spends over GBP 200M annually on digital inclusion programmes with no unified measurement of impact or targeting. A GBP 3.2M platform that improves targeting efficiency by even 5% delivers significant value. The platform also fulfils the UK Digital Strategy commitment to measure and track digital inclusion.

**Next Steps if Approved**:

1. Secure DSIT funding approval: Q2 2026
2. Data sharing agreements with Lloyds, Ofcom, ONS: Q2-Q3 2026
3. Discovery phase with local authorities: Q3 2026
4. Alpha with geospatial dashboard prototype: Q4 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Approximately 10 million UK adults lack foundational digital skills and 1.7 million households have no internet access. The UK spends over GBP 200M annually on digital inclusion programmes (government, charity, private sector), but there is no unified measurement platform to target these investments or track their impact.

**Specific Pain Points** (from Stakeholder Analysis ARC-002-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DSIT Minister | SD-1 | Cannot answer PQs on local digital inclusion | Ministerial embarrassment, poor targeting | CRITICAL |
| Ofcom | SD-2 | Connectivity data conflated with inclusion | Misleading policy conclusions | HIGH |
| Good Things Foundation | SD-3 | Community programme impact invisible | Grassroots investment undervalued | HIGH |
| Local authorities | SD-4 | No local-level data for intervention planning | Resources poorly targeted | MEDIUM |

**Consequences of Inaction**:

- GBP 200M+ annual digital inclusion spend continues without evidence-based targeting
- 10 million digitally excluded adults remain invisible at local level
- Government's digital-by-default strategy fails for the most disadvantaged populations
- UK falls behind international comparators with national digital inclusion indices

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **UK Digital Strategy**: "We will measure and track digital inclusion, ensuring everyone can participate in the digital economy"
- **Levelling Up White Paper**: Mission 4 (broadband) and mission-adjacent skills goals
- **Government digital-by-default strategy**: Depends on digital inclusion for channel shift
- **Architecture Principles**: Principles 3 (Digital-by-Default with Assisted Digital), 13 (Single Source of Truth), 19 (Levelling Up Missions Alignment)

### A1.3 Scope

**In Scope**:

- Integration of Lloyds Consumer Digital Index, Ofcom Connected Nations, ONS Internet Access survey, DfE Essential Digital Skills, Good Things Foundation programme data
- Geospatial dashboard (local authority, LSOA, constituency)
- Composite Digital Inclusion Index
- Local authority benchmarking
- Open data publication
- Community programme data API

**Out of Scope**:

- Individual digital skills assessment tools
- Broadband infrastructure deployment
- Direct digital skills training delivery

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Data Integration**: Five or more authoritative sources integrated within 12 months
   - **Measure**: Data sources operational
   - **Threshold**: Minimum 3

2. **Geographic Granularity**: 80%+ of metrics available at local authority level
   - **Measure**: Metric coverage at LA level
   - **Threshold**: Minimum 60%

3. **User Adoption**: 100+ local authorities actively using within 18 months
   - **Measure**: Monthly active local authority users
   - **Threshold**: Minimum 50

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue relying on separate annual publications from Lloyds, Ofcom, ONS, and DfE.

**Costs** (3-year):

- Capital: GBP 0
- Operational: GBP 1.5M (DSIT analyst time assembling data from separate sources)
- Total: GBP 1.5M

**Benefits**: GBP 0

**Cons**:

- No unified view of digital exclusion
- Cannot target interventions at local level
- GBP 200M+ digital inclusion spend poorly targeted
- Cannot fulfil UK Digital Strategy measurement commitment

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject**

---

### Option 1: Curated Data Publication

**Description**: DSIT publishes an annual curated report combining data from existing sources, with static maps and tables. No interactive platform.

**Costs** (3-year) — ROM (+-40%):

- Capital: GBP 0.2M (report design, data processing automation)
- Operational: GBP 0.6M over 3 years (analyst time, publication costs)
- Total: GBP 0.8M

**Benefits** (3-year): GBP 2.5M

**Pros**:

- Low cost
- Quick to implement (3 months)

**Cons**:

- Static — no interactive analysis or drilling down
- Annual publication cycle too slow for intervention planning
- No community data integration
- No local authority self-service benchmarking

**Stakeholder Goals Met**: 25%

---

### Option 2: Balanced Approach (RECOMMENDED)

**Description**: Interactive geospatial data platform integrating five data sources, with local authority benchmarking, composite index, community data API, and open data publication.

**Costs** (3-year) — ROM (+-30%):

- Capital: GBP 1.8M
  - Platform development: GBP 0.9M
  - Data integration and ETL: GBP 0.4M
  - Geospatial mapping: GBP 0.2M
  - Composite index methodology: GBP 0.15M
  - Community data API: GBP 0.15M
- Operational: GBP 1.4M over 3 years
  - Cloud hosting: GBP 0.15M/year
  - Platform team (4 FTE): GBP 0.3M/year
- Total 3-year TCO: GBP 3.2M

**Benefits** (3-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|------------|------|--------|--------|--------|--------------|
| B-001 | Analysis efficiency (replaces manual data assembly) | FINANCIAL | GBP 0.5M | GBP 1.0M | GBP 1.5M | GBP 3.0M |
| B-002 | Improved targeting of digital inclusion spend | FINANCIAL | GBP 0.5M | GBP 1.5M | GBP 1.5M | GBP 3.5M |
| B-003 | Accelerated digital inclusion through better targeting | SOCIAL | GBP 0.1M | GBP 0.5M | GBP 0.7M | GBP 1.3M |
| **Total** | | | **GBP 1.1M** | **GBP 3.0M** | **GBP 3.7M** | **GBP 7.8M** |

**NPV**: GBP 4.0M (at 3.5% discount rate)

**ROI**: 144% over 3 years

**Payback Period**: 16 months

**Stakeholder Impact**:

- DSIT Minister (SD-1): Met — evidence-based policy, PQ support
- Ofcom (SD-2): Met — connectivity dimension clearly separated from inclusion
- Good Things Foundation (SD-3): Met — community programme data integrated
- Local authorities (SD-4): Met — benchmarking and local-level data
- Age UK (SD-5): Met — age-disaggregated data included

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive Real-Time Platform

**Description**: Real-time digital inclusion platform with live data feeds, predictive analytics, and individual-level digital skills tracking.

**Costs** (3-year): GBP 8.5M

**Benefits** (3-year): GBP 9.0M

**NPV**: GBP 0.5M (marginal)

**Cons**:

- Most data sources are annual — "real-time" is misleading
- Individual-level tracking raises severe GDPR concerns
- Disproportionate cost for marginal benefit

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Marginal NPV does not justify GBP 8.5M investment.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-year cost | GBP 1.5M | GBP 0.8M | GBP 3.2M | GBP 8.5M |
| 3-year benefit | GBP 0 | GBP 2.5M | GBP 7.8M | GBP 9.0M |
| NPV | -GBP 1.5M | GBP 1.5M | GBP 4.0M | GBP 0.5M |
| Stakeholder goals met | 0% | 25% | 85% | 100% |
| Implementation time | N/A | 3 months | 12 months | 24 months |
| **Recommendation** | **Reject** | **Possible** | **RECOMMENDED** | **Reject** |

---

# PART C: COMMERCIAL CASE

## C1. Procurement Approach

**Strategy**: Build on open source geospatial tools (Leaflet/MapLibre, PostGIS), supplemented by CCS framework procurement for cloud hosting.

**Key Procurements**:

- Cloud hosting: CCS G-Cloud framework (estimated GBP 50K/year)
- ONS geographic data: Open data (free via OS OpenData and ONS Geoportal)
- Lloyds Consumer Digital Index data: Data sharing agreement (negotiated)

**Make vs Buy**: Build. No existing platform combines the specific data sources and composite index methodology required.

---

# PART D: FINANCIAL CASE

## D1. Funding Requirements

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital | GBP 1.3M | GBP 0.3M | GBP 0.2M | GBP 1.8M |
| Operational | GBP 0.35M | GBP 0.45M | GBP 0.60M | GBP 1.4M |
| **Total** | **GBP 1.65M** | **GBP 0.75M** | **GBP 0.80M** | **GBP 3.2M** |

**Funding Source**: DSIT programme budget

---

# PART E: MANAGEMENT CASE

## E1. Governance

- **SRO**: DSIT Director of Digital Infrastructure
- **Programme Board**: DSIT, Ofcom (observer), ONS (methodology advisory), Good Things Foundation (observer)
- **Delivery Methodology**: Agile (GDS phases)

## E2. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|-------------|
| SOBC approval | Q2 2026 | This document |
| Data sharing agreements signed | Q3 2026 | Lloyds, Ofcom, ONS negotiations |
| Discovery complete | Q3 2026 | SOBC approval |
| Alpha (dashboard prototype) | Q4 2026 | Data sharing agreements |
| Beta launch | Q2 2027 | Alpha assessment pass |
| Composite Index first edition | Q4 2027 | ONS methodology review |
| Live service | Q4 2027 | Beta assessment pass |

## E3. Risk Summary

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Data latency undermines value | HIGH | MEDIUM | Supplement with more frequent proxy indicators |
| Small-area estimates unreliable | HIGH | HIGH | Publish confidence intervals, use modelling techniques |
| Composite index methodology contested | MEDIUM | MEDIUM | ONS co-development, academic peer review |
| Lloyds data sharing agreement fails | MEDIUM | HIGH | ONS Internet Users survey as alternative source |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK Digital Strategy | Strategy | GOV.UK | Digital inclusion commitments | N/A |
| HM Treasury Green Book | Guidance | GOV.UK | Five-case business case methodology | N/A |
| Lloyds Consumer Digital Index 2025 | Research | Lloyds Bank | Digital skills gap evidence | N/A |
| ARC-002-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers | projects/002-digital-inclusion-tracker/ |
| ARC-002-REQ-v1.0 | Requirements | ArcKit | Requirements specification | projects/002-digital-inclusion-tracker/ |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Inclusion Tracker
**Model**: Claude Opus 4.6
