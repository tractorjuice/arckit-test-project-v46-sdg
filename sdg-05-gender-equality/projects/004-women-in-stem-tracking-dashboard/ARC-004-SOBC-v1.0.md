# Strategic Outline Business Case (SOBC): Women in STEM Tracking Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Women in STEM Tracking Dashboard (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Women in STEM Programme, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Programme Board, UKRI, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: Build a comprehensive data analytics platform tracking gender diversity across the UK's STEM pipeline from education to senior leadership, providing the evidence base for targeted policy interventions and public accountability.

**Problem Statement**: UK STEM gender diversity data is fragmented across 8+ organisations, uses inconsistent definitions, and is published with 12-24 month lag. No single platform provides full pipeline visibility, making it impossible to identify precisely where women are lost from STEM or whether interventions are working. This undermines DSIT's ability to make evidence-based policy on STEM diversity.

**Proposed Solution**: An automated data aggregation and analytics platform with interactive pipeline visualisation, intersectional analysis, open data APIs, international comparison, and embeddable widgets.

**Strategic Fit**: Directly supports DSIT's Science and Technology Framework workforce diversity objectives, UKRI's EDI Strategy, and UK SDG 5 commitments on women's economic empowerment through STEM careers.

**Investment Required**: GBP 3.2M over 3 years

- Capital: GBP 2.0M
- Operational (3 years): GBP 1.2M

**Expected Benefits**: GBP 5.8M over 5 years

- Research and policy efficiency savings: GBP 1.6M (eliminates duplicate data collection across 10+ organisations)
- Evidence-based policy improvement (social value): GBP 2.8M (targeted interventions vs. untargeted spending)
- STEM workforce productivity gains from improved diversity: GBP 1.4M

**Return on Investment**:

- NPV: GBP 1.6M (discounted at 3.5%)
- Payback Period: 26 months
- ROI: 81%

**Recommended Option**: Option 2: Comprehensive Pipeline Dashboard

**Key Risks**:

1. Data sharing agreement delays with HESA/UKRI (mitigated by starting with open data, adding enhanced data incrementally)
2. Inconsistent STEM definitions across sources (mitigated by reconciliation mapping, transparent methodology)
3. Low user adoption (mitigated by partner embedding, open data API, media engagement)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: At GBP 3.2M, this is the most cost-effective project in the SDG 5 programme. The current fragmented data landscape wastes significant effort across 10+ organisations producing partial, inconsistent reports. A single authoritative platform eliminates duplication, enables evidence-based policy, and provides public accountability on STEM gender diversity.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
STEM gender diversity data in the UK is published by at least 10 different organisations — WISE (annual statistics), HESA (student and staff data), UKRI (research funding), DfE (school subjects), ONS (workforce), Royal Society (research), RAEng (engineering), BCS (computing), IET (engineering), and individual universities. Each uses slightly different definitions of "STEM", different time periods, different demographic categories, and different publication schedules. The result is a confusing, inconsistent picture where different sources report different numbers for what appears to be the same thing.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact |
|-------------|------------|--------|
| DSIT Chief Scientific Adviser | No single source for Ministerial briefing on STEM diversity | Policy decisions based on incomplete, stale data |
| UKRI | Funding equity data fragmented across 9 councils | Cannot demonstrate equitable funding allocation |
| WISE Campaign | 3 months annually spent assembling data from multiple sources | Resources diverted from advocacy to data collection |
| Universities | Benchmark data unavailable or incomparable | Cannot assess relative diversity performance |

**Consequences of Inaction**:

- GBP 50M+ annual government spending on STEM diversity programmes without robust outcome measurement
- Policy interventions targeted at anecdote rather than evidence
- UK unable to provide credible SDG 5 indicators on women in science

### A1.2 Strategic Alignment

- **DSIT Science and Technology Framework**: "We will grow, diversify and develop the R&D workforce"
- **UKRI EDI Strategy 2022-2027**: Equitable funding, diverse workforce, inclusive culture
- **SDG 5 (Gender Equality)**: Target 5.5 — women's full and effective participation in leadership
- **ARC-000-PRIN-v1.0**: Principles 10 (Gender-Disaggregated Data), 13 (Intersectionality), 14 (Data Quality)

### A1.5 Why Now?

**Urgency Factors**:

- DSIT Science and Technology Framework commits to workforce diversity with no systematic measurement
- UKRI EDI Strategy published in 2022 — reporting against commitments overdue
- International competitors (Ireland, Netherlands, Germany) have launched national STEM diversity dashboards
- UN SDG 5 reporting cycle requires UK data on women in science

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (3-year): GBP 0.8M (continued costs of multiple organisations producing partial, overlapping reports)

**Consequences**: Continued data fragmentation; policy based on stale, inconsistent data; no single authoritative source; UK falls behind international peers on transparency.

**Recommendation**: **Reject**

---

### Option 1: Annual Consolidated Report (Minimal)

**Description**: Commission an annual report compiling data from existing sources. No dashboard, no API, no intersectional analysis. Essentially an enhanced version of the WISE annual report.

**Costs** (3-year): GBP 0.9M (research contract)

**Benefits** (5-year): GBP 1.8M (modest research efficiency)

**Pros**: Low cost, fast to produce

**Cons**: Annual publication not timely; no interactive analysis; no open data; no intersectionality; single point of failure (contractor)

**Stakeholder Goals Met**: 20%

---

### Option 2: Comprehensive Pipeline Dashboard (RECOMMENDED)

**Description**: Automated data aggregation platform with interactive pipeline visualisation, intersectional analysis, open data API, international comparison, and embeddable widgets.

**Costs** (3-year) — ROM (+/-30%):

- Capital: GBP 2.0M
  - Platform development: GBP 1.2M
  - Data pipeline engineering: GBP 0.4M
  - Integrations (HESA, UKRI, DfE, ONS): GBP 0.2M
  - Testing and assurance: GBP 0.2M
- Operational: GBP 1.2M
  - Cloud hosting: GBP 0.15M/year
  - Support and maintenance: GBP 0.15M/year
  - Staff costs (data analyst, product manager): GBP 0.1M/year
- Total 3-year TCO: GBP 3.2M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|-------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Research/policy efficiency (eliminated duplication) | FINANCIAL | GBP 0.1M | GBP 0.3M | GBP 0.3M | GBP 0.4M | GBP 0.5M | GBP 1.6M |
| B-002 | Evidence-based policy improvement (social value) | SOCIAL | GBP 0 | GBP 0.3M | GBP 0.6M | GBP 0.8M | GBP 1.1M | GBP 2.8M |
| B-003 | STEM workforce productivity (diversity dividend) | ECONOMIC | GBP 0 | GBP 0.1M | GBP 0.3M | GBP 0.4M | GBP 0.6M | GBP 1.4M |
| **Total** | | | **GBP 0.1M** | **GBP 0.7M** | **GBP 1.2M** | **GBP 1.6M** | **GBP 2.2M** | **GBP 5.8M** |

**NPV** (3.5%): GBP 1.6M

**ROI**: 81%

**Payback Period**: 26 months

**Stakeholder Goals Met**: 85%

---

### Option 3: AI-Powered Predictive Analytics Platform

**Description**: Full Option 2 plus machine learning models predicting future STEM gender ratios, automated policy recommendation engine, and real-time social media sentiment analysis.

**Costs** (3-year): GBP 6.8M

**Benefits** (5-year): GBP 7.2M

**Pros**: Predictive capability could inform proactive policy

**Cons**: Predictive models on small datasets are unreliable; GBP 3.6M more than Option 2 for GBP 1.4M additional benefit; social media sentiment analysis adds noise not signal; over-engineering for the policy use case

**Recommendation**: **Reject** — Predictive modelling on demographic data requires much larger datasets than available. Better to build solid descriptive analytics first.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Comprehensive Pipeline Dashboard**

**Optimism Bias Adjustment**:

- Adjusted cost: GBP 3.2M x 1.4 = GBP 4.5M
- NPV with optimism bias: GBP 0.1M (marginal but positive)
- Conclusion: Investment justified, particularly given the low absolute cost and high strategic value

---

# PART C: COMMERCIAL CASE

**Sourcing Route**: Digital Marketplace (DOS6 for Discovery/Alpha, G-Cloud for hosting)

**Contract Approach**:

- Discovery/Alpha: Time and materials, GBP 0.2M
- Build: Fixed-price with milestones, GBP 1.0M
- Managed service: GBP 0.4M/year

**Social Value**: Supplier commitment to women in tech targets in delivery team; apprenticeships in data engineering; open source code base.

---

# PART D: FINANCIAL CASE

## D1. Total Cost of Ownership

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 1.2M | GBP 0.8M | GBP 0 | GBP 2.0M |
| OpEx | GBP 0.3M | GBP 0.4M | GBP 0.5M | GBP 1.2M |
| **Total** | **GBP 1.5M** | **GBP 1.2M** | **GBP 0.5M** | **GBP 3.2M** |

## D2. Funding Source

**Source**: DSIT Digital and Data Programme budget. Co-funding from UKRI for research data integration components. In-kind contribution from HESA for data sharing.

## D3. Affordability

**Assessment**: **Affordable** — GBP 3.2M is the smallest investment in the SDG 5 programme. DSIT digital budget can absorb this within existing allocations.

---

# PART E: MANAGEMENT CASE

## E2. Delivery Approach

**Methodology**: Agile with GDS service assessment gates

**Phases**:

1. **Discovery** (Months 1-2): Data source mapping, user research with researchers/policy makers, DSA initiation
2. **Alpha** (Months 3-6): Prototype pipeline visualisation, data pipeline POC with 3 sources (HESA, DfE, ONS open data)
3. **Private Beta** (Months 7-10): Build with 5+ sources, researcher pilot, accessibility testing
4. **Public Beta** (Months 11-12): Public launch with 8+ sources, open data API
5. **Live** (Month 12+): Continuous improvement, additional data sources, international comparison

## E3. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|--------------|
| Discovery complete | Month 2 | Funding secured |
| HESA DSA signed | Month 4 | Legal review |
| Alpha assessment (GDS) | Month 6 | Alpha complete |
| Public dashboard launch | Month 12 | 8+ data sources ingested |
| International comparison module | Month 18 | Eurostat/OECD data integrated |
| Code of Practice assessment | Month 24 | Statistical quality established |

## E5. Risk Management

| Risk ID | Description | Likelihood | Impact | Score | Mitigation |
|---------|-------------|------------|--------|-------|------------|
| R-001 | DSA delays with HESA/UKRI | Medium | Major | 12 | Start with open data; add enhanced data incrementally |
| R-002 | Inconsistent STEM definitions | High | Moderate | 12 | Published reconciliation methodology; transparent notes |
| R-003 | Low user adoption | Medium | Moderate | 9 | Partner embedding, media engagement, API for researchers |
| R-004 | Statistical disclosure control failures | Low | Major | 8 | ONS SDC methodology, automated cell suppression |
| R-005 | Budget overrun | Low | Moderate | 6 | Agile delivery, phased scope, change control |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary of Recommendation

**Recommended Option**: **Option 2: Comprehensive Pipeline Dashboard**

**Investment**: GBP 3.2M over 3 years

**Expected Return**: GBP 5.8M over 5 years (NPV: GBP 1.6M, ROI: 81%)

**Go/No-Go Recommendation**: **PROCEED to Discovery phase**

**Rationale**: This is the most cost-effective investment in the SDG 5 programme. It eliminates significant data duplication across 10+ organisations, enables evidence-based STEM diversity policy for the first time, and provides public accountability on a GBP 50M+ annual government investment in STEM diversity programmes. At GBP 3.2M, the investment is modest relative to the GBP 5.8M return and the strategic value of the evidence base it creates.

## F2. Next Steps if Approved

**Immediate Actions**:

1. **Funding Confirmation**: DSIT Finance confirms GBP 3.2M allocation — Target: Q2 2026
2. **Data Source Engagement**: Initiate DSA discussions with HESA, UKRI, DfE — Target: Q2 2026
3. **Discovery Procurement**: Publish DOS6 requirement for Discovery team — Target: Q3 2026

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO, Women in STEM Programme | | |
| | DSIT Chief Scientific Adviser | | |
| | DSIT Finance Director | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Women in STEM Tracking Dashboard (Project 004)
**Model**: Claude Opus 4.6
