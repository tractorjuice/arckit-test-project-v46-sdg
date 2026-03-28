# Strategic Outline Business Case (SOBC): Labour Market Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Labour Market Intelligence (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Labour Market Intelligence Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | ONS Programme Board, UKSA, HM Treasury, DWP, DfE, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC assesses the case for investing in a real-time Labour Market Intelligence platform to transform the UK's employment statistics from lagged, survey-dependent indicators to near-real-time, multi-source analytics.

---

## Executive Summary

**Purpose**: Build a real-time analytical platform that fuses administrative data (HMRC RTI, DWP UC), transformed survey data (LFS), and novel data sources (online vacancies) to produce near-real-time, local-level labour market intelligence for policy, operations, and public use.

**Problem Statement**: The UK's primary labour market indicator — the Labour Force Survey — was downgraded from National Statistics due to declining response rates (below 40%). Policy departments are making decisions on employment, skills, and regional investment with data that is 6+ weeks old and lacks local granularity. During the COVID-19 pandemic, this lag had direct fiscal consequences — the furlough scheme was designed with severely outdated data.

**Proposed Solution**: An integrated data platform that ingests HMRC Real Time Information (50M+ records daily), DWP administrative data, and vacancy data to produce weekly national indicators and quarterly local authority-level analytics, published via dashboards, API, and open data.

**Strategic Fit**: Directly supports ONS's statutory duty under the Statistics and Registration Service Act 2007. Enables Levelling Up evidence base. Feeds labour market context into the Job Matching Platform (Project 001). Responds to the UK Statistics Authority's call for transformation of labour market statistics.

**Investment Required**: GBP 12M over 3 years

- Capital: GBP 8M
- Operational (3 years): GBP 4M

**Expected Benefits**: GBP 40M over 5 years

- Better policy decisions (reduced misallocation of skills funding): GBP 25M
- Operational efficiency (DWP, DfE analytical savings): GBP 8M
- Research community value: GBP 7M

**Return on Investment**:

- NPV: GBP 20M (discounted at 3.5%)
- Payback Period: 24 months
- ROI: 233%

**Recommended Option**: Option 2: Multi-Source Analytical Platform

**Key Risks**:

1. HMRC data sharing agreement renewal uncertainty
2. Statistical quality challenges when fusing administrative and survey data
3. Statistical disclosure control limiting local-level granularity

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The LFS quality crisis has created an urgent need — the UK cannot operate without reliable labour market data. The RTI-based approach has been proven experimentally during COVID-19. The investment is modest relative to the fiscal decisions (GBP billions in skills funding, UC spending, regional investment) that depend on accurate, timely labour market data.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
ONS publishes monthly labour market statistics based primarily on the Labour Force Survey. The LFS response rate has fallen below 40%, prompting the UK Statistics Authority to downgrade LFS-based estimates from National Statistics to Experimental Statistics. Meanwhile, HMRC RTI data (which covers all PAYE employment) is available daily but is only published as experimental statistics with limited granularity.

**Consequences of Inaction**:

- Policy decisions continue to be based on lagged, unreliable data
- GBP 3.8B Annual Skills Fund allocated without current local labour market evidence
- Levelling Up metrics cannot be measured at local level with confidence
- ONS reputational damage from LFS downgrade deepens
- International standing — UK statistics quality falls behind comparable countries

### A1.2 Strategic Drivers

| Driver ID | Stakeholder | Driver Type | Description |
|-----------|-------------|-------------|-------------|
| SD-1 | National Statistician | STRATEGIC | Restore confidence in labour market statistics |
| SD-2 | HM Treasury | FINANCIAL | Timelier data for fiscal decisions |
| SD-3 | DWP | OPERATIONAL | Local labour market data for JCP operations |
| SD-4 | HMRC | COMPLIANCE | Controlled access to RTI data |
| SD-5 | Academic Researchers | STRATEGIC | Open access to microdata |

### A1.5 Why Now?

- LFS quality crisis — cannot wait for survey transformation alone (multi-year programme)
- COVID-19 demonstrated value of real-time RTI data — need to make this permanent
- Levelling Up requires local-level evidence base urgently
- Job Matching Platform (Project 001) needs labour market context — data infrastructure must precede AI matching

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Weekly Indicators**: Published within 5 working days of reference period
2. **Local Granularity**: 95% of local authorities with publishable data
3. **UKSA Assessment**: Core indicators assessed as suitable for Official Statistics designation
4. **HMRC Satisfaction**: RTI data adequately protected in published outputs

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with LFS-based monthly statistics and ad-hoc RTI experimental statistics.

**Costs** (3-year): GBP 5M (existing LFS and RTI publication costs)
**Benefits**: GBP 0

**Cons**:
- LFS quality continues to deteriorate
- Policy decisions remain based on lagged data
- No local-level data for Levelling Up
- ONS reputation continues to suffer

**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject**

---

### Option 1: Enhanced RTI Publication

**Description**: Expand existing experimental RTI-based statistics with more indicators and local breakdown, without building a comprehensive multi-source platform.

**Costs** (3-year): GBP 5M
**Benefits** (5-year): GBP 20M

**Pros**:
- Lower investment
- Builds on existing capability
- Faster to deliver (6 months)

**Cons**:
- RTI only covers PAYE employment — misses self-employment, unemployment, economic inactivity
- No integration with vacancy or skills data
- Limited analytical capability — publication only, not an analytical platform
- Does not address survey data fusion or skills gap forecasting

**Stakeholder Goals Met**: 35%
**Recommendation**: Viable but insufficient

---

### Option 2: Multi-Source Analytical Platform (RECOMMENDED)

**Description**: Comprehensive platform fusing RTI, DWP UC data, vacancy data, and transformed LFS to produce weekly national and quarterly local indicators, skills gap forecasts, and secure research data access.

**Costs** (3-year) - ROM (+/- 30%):

- Capital: GBP 8M
  - Data ingestion and linkage platform: GBP 3M
  - Statistical processing engine: GBP 2M
  - Publication platform (dashboards, API): GBP 1.5M
  - Skills gap forecasting model: GBP 1M
  - Secure research environment integration: GBP 0.5M
- Operational: GBP 4M over 3 years
  - Cloud computing (ONS platform): GBP 0.8M/year
  - Statistician and data science team: GBP 0.5M/year
- Total 3-year TCO: GBP 12M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Better skills funding allocation | FINANCIAL | GBP 2M | GBP 5M | GBP 6M | GBP 6M | GBP 6M | GBP 25M |
| B-002 | Analytical efficiency (DWP, DfE) | OPERATIONAL | GBP 1M | GBP 2M | GBP 2M | GBP 2M | GBP 1M | GBP 8M |
| B-003 | Research community value | STRATEGIC | GBP 0.5M | GBP 1.5M | GBP 2M | GBP 2M | GBP 1M | GBP 7M |
| **Total** | | | **GBP 3.5M** | **GBP 8.5M** | **GBP 10M** | **GBP 10M** | **GBP 8M** | **GBP 40M** |

**NPV** (3.5%): GBP 20M
**ROI**: 233%
**Payback**: 24 months

**Stakeholder Goals Met**: 85%

**Pros**:
- Comprehensive coverage (employment, unemployment, inactivity, vacancies, skills)
- Weekly timeliness (vs. 6-week lag)
- Local authority granularity for Levelling Up
- Skills gap forecasting — new analytical capability
- Platform serves multiple policy customers (Treasury, DWP, DfE, DBT)

**Cons**:
- Complex data linkage across departmental silos
- Statistical methodology development required for data fusion
- HMRC data sharing agreement must be renewed annually
- Disclosure control may limit some local area publication

---

### Option 3: National Data Observatory

**Description**: Comprehensive economic data observatory covering labour market, productivity, trade, and business demographics in a single platform.

**Costs** (3-year): GBP 25M
**Benefits** (5-year): GBP 55M

**Recommendation**: **Reject** — Scope exceeds LMI programme remit. Labour market focus (Option 2) delivers specific benefits without scope creep into broader economic statistics.

---

# PART C: COMMERCIAL CASE

**Approach**: In-house development by ONS Digital and Data Science Campus, leveraging existing ONS Integrated Data Service (IDS) infrastructure.

**Key Contracts**:
- Cloud platform: Existing ONS cloud agreement
- Specialist data linkage consultancy: GBP 1M via CCS DOS
- Vacancy data API licences (Indeed, LinkedIn): GBP 0.5M/year

---

# PART D: FINANCIAL CASE

| Year | Capital | Operational | Total |
|------|---------|-------------|-------|
| 2026-27 | GBP 4M | GBP 0.8M | GBP 4.8M |
| 2027-28 | GBP 3M | GBP 1.3M | GBP 4.3M |
| 2028-29 | GBP 1M | GBP 1.9M | GBP 2.9M |
| **Total** | **GBP 8M** | **GBP 4M** | **GBP 12M** |

**Funding Source**: ONS Core Statistics budget with cross-departmental contributions from DWP, DfE, and Treasury for platform usage.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Timeline**:
- Phase 1 (Q2-Q4 2026): Enhanced RTI weekly indicators — quick win
- Phase 2 (Q1-Q3 2027): Local authority-level data, vacancy integration
- Phase 3 (Q4 2027-Q2 2028): Skills gap forecasting, secure research access

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| HMRC data sharing renewal | LOW | CRITICAL | Early engagement, statutory gateway documentation |
| Statistical quality of fused data | MEDIUM | HIGH | Methodology peer review, UKSA assessment |
| Disclosure control limits local data | MEDIUM | MEDIUM | Synthetic data methods, cell perturbation |
| Vacancy data commercial terms | MEDIUM | MEDIUM | Multiple supplier strategy, web scraping fallback |
| LFS transformation delay | MEDIUM | LOW | Platform valuable without LFS — RTI and vacancy sufficient for initial indicators |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-003-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals | `projects/003-labour-market-intelligence/ARC-003-STKE-v1.0.md` |
| ARC-003-REQ-v1.0 | Requirements | SDG 8 Programme | Requirements | `projects/003-labour-market-intelligence/ARC-003-REQ-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 4, 11, 12 | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Labour Market Intelligence
**Model**: Claude Opus 4.6
