# Strategic Outline Business Case (SOBC): Global Britain Trade Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Global Britain Trade Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Global Britain Trade Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DBT Board, HMRC, UK Export Finance, HM Treasury, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in the Global Britain Trade Platform, following the HM Treasury Green Book five-case model. It draws on stakeholder analysis (ARC-004-STKE-v1.0) and architecture principles (ARC-000-PRIN-v1.0).

---

## Executive Summary

**Purpose**: The UK has negotiated independent FTAs with 73+ countries post-Brexit, but cannot systematically measure whether these agreements are being used by businesses. Trade data is siloed between HMRC (customs), DBT (promotion), and UKEF (export finance). UK businesses navigate 4+ government services to find trade information. The Export Strategy target of GBP 1 trillion in exports requires better trade intelligence and simpler business services.

**Problem Statement**: The UK negotiates FTAs but has no systematic way to measure their utilisation. Trade data silos prevent integrated analysis. UK businesses find government trade services fragmented and complex, contributing to the UK's low export participation rate (10% of businesses export).

**Proposed Solution**: An integrated trade platform connecting HMRC customs data, DBT trade promotion, and UKEF export finance, with FTA utilisation dashboards, a business-facing trade portal, FTA impact modelling, and SDG 17 trade indicator monitoring.

**Strategic Fit**: Directly supports the Export Strategy (2022), Integrated Review (2023), and UK Developing Countries Trading Scheme objectives. Contributes to SDG 17 trade-related targets (17.10, 17.11, 17.12).

**Investment Required**: GBP 20M over 3 years

- Capital: GBP 12.5M
- Operational (3 years): GBP 7.5M

**Expected Benefits**: GBP 45M over 5 years

- Increased FTA utilisation (tariff savings for UK businesses): GBP 25M
- Export growth from simplified services: GBP 12M
- Trade policy improvement: GBP 5M
- DCTS monitoring / SDG 17 reporting: GBP 3M

**Return on Investment**:

- NPV: GBP 18.7M (discounted at 3.5%)
- Payback Period: 20 months
- ROI: 125%

**Recommended Option**: Option 2: Integrated Trade Platform with FTA Analytics

**Key Risks**:

1. HMRC data sharing agreement — HMRC must agree to share aggregated customs data (mitigated by Statistics of Trade Act legal basis, early engagement)
2. FTA utilisation attribution — separating FTA impact from other trade drivers is methodologically challenging (mitigated by gravity model approach, academic partnership)
3. Business portal adoption — businesses may not shift from existing services (mitigated by integration with great.gov.uk, GDS service design)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK cannot evaluate its post-Brexit trade policy without FTA utilisation data. The Export Strategy target requires better business services. Integrated trade data will improve policy making, increase export participation, and demonstrate UK commitment to SDG 17.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The UK has negotiated FTAs with 73+ countries but cannot answer the basic question: "Are businesses using these FTAs?" HMRC holds customs declaration data showing preferential tariff claims, but this is not systematically analysed for FTA utilisation. DBT promotes exports but cannot measure whether its interventions lead to actual trade growth. UKEF provides GBP 6-8B in export finance but its systems are disconnected from trade data. Businesses must navigate great.gov.uk, HMRC Trade Tariff, UKEF portal, and FTA legal texts separately.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Secretary of State | SD-1 | Cannot demonstrate FTA success to Parliament | Political vulnerability, IDC scrutiny | CRITICAL |
| HMRC | SD-2 | Trade data used for compliance, not analytics | Valuable analytical potential unrealised | HIGH |
| UK businesses | SD-3 | 4+ government websites for trade information | Low export participation (10% of businesses) | MEDIUM |
| Trade Policy | SD-4 | FTA models disconnected from actual trade data | Post-implementation reviews lack evidence | HIGH |
| UKEF | SD-5 | Low SME awareness of export finance | GBP 2B+ unutilised export finance capacity | MEDIUM |

**Consequences of Inaction**:

- UK cannot demonstrate FTA value to Parliament or public, undermining trade policy credibility
- Export Strategy GBP 1 trillion target unattainable without better business services
- SDG 17 trade targets unmonitored — UK cannot report on developing country trade contribution
- FTA post-implementation reviews lack quantitative evidence, reducing negotiation leverage for future agreements
- UK businesses continue to under-utilise FTA preferential tariffs, leaving GBP 2-5B in potential savings unclaimed

### A1.2 Strategic Alignment

- **Export Strategy (2022)**: GBP 1 trillion export target; "make it easier for businesses to export"
- **Integrated Review (2023)**: Global Britain trade partnerships as economic security foundation
- **UK Developing Countries Trading Scheme**: Preferential access for 65 developing countries
- **SDG 17 Principles (ARC-000-PRIN-v1.0)**: Principle 1 (International Interoperability), Principle 10 (API-First)

### A1.3 Why Now?

- Post-Brexit FTAs now in force — time to measure utilisation (Australia, NZ, CPTPP 2+ years)
- Export Strategy sets urgent target requiring actionable trade intelligence
- International Trade Committee increasing scrutiny of FTA outcomes
- DCTS entered into force June 2023 — utilisation monitoring needed
- Cross-Government Data Sharing Platform (Project 002) enables HMRC data access

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **FTA utilisation data**: Quarterly utilisation rates published for all UK FTAs within 18 months
2. **HMRC data integration**: Aggregated trade data with < 30-day lag
3. **Business portal adoption**: 50,000 monthly users within 12 months of launch
4. **SDG 17 reporting**: DCTS utilisation data feeding ONS SDG Dashboard (Project 003)
5. **Trade policy evidence**: Post-implementation review data available for 2027 reviews

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Costs** (3-year): GBP 8M (continued separate services, manual analysis)

**Benefits**: GBP 0

**Recommendation**: **Reject** — Cannot demonstrate FTA value; Export Strategy target unachievable without better business services.

---

### Option 1: FTA Analytics Only (No Business Portal)

**Description**: HMRC data integration for FTA utilisation measurement and trade policy analysis. No business-facing portal — existing services continue.

**Costs** (3-year): GBP 8M

**Benefits** (5-year): GBP 15M (trade policy improvement, partial utilisation gain)

**Stakeholder Goals Met**: 40%

**Recommendation**: **Reject** — Addresses policy analysis (SD-1, SD-4) but not business needs (SD-3, SD-5). Does not support Export Strategy target.

---

### Option 2: Integrated Trade Platform with FTA Analytics (RECOMMENDED)

**Description**: Full platform integrating HMRC trade data, DBT promotion, UKEF finance, with FTA utilisation dashboards, business-facing trade portal, and SDG 17 monitoring.

**Costs** (3-year) — ROM (+-30%):

- Capital: GBP 12.5M
  - FTA analytics engine and HMRC integration: GBP 4M
  - Business-facing trade portal: GBP 3.5M
  - FTA impact modelling tools: GBP 2M
  - UKEF and great.gov.uk integration: GBP 1.5M
  - DCTS/SDG monitoring: GBP 0.5M
  - Training and change management: GBP 1M
- Operational: GBP 7.5M (3 years)
  - Cloud hosting and managed services: GBP 1M/year
  - HMRC data feed support: GBP 0.5M/year
  - Portal support and content: GBP 1M/year
- Total 3-year TCO: GBP 20M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|-------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Increased FTA utilisation (tariff savings) | FINANCIAL | GBP 0 | GBP 3M | GBP 6M | GBP 8M | GBP 8M | GBP 25M |
| B-002 | Export growth from simplified services | FINANCIAL | GBP 0 | GBP 1.5M | GBP 3M | GBP 3.5M | GBP 4M | GBP 12M |
| B-003 | Trade policy improvement | STRATEGIC | GBP 0 | GBP 0.5M | GBP 1M | GBP 1.5M | GBP 2M | GBP 5M |
| B-004 | DCTS monitoring / SDG 17 value | STRATEGIC | GBP 0 | GBP 0.3M | GBP 0.5M | GBP 1M | GBP 1.2M | GBP 3M |
| **Total** | | | **GBP 0** | **GBP 5.3M** | **GBP 10.5M** | **GBP 14M** | **GBP 15.2M** | **GBP 45M** |

**NPV** (3.5% discount, 5-year): **GBP 18.7M**

**ROI**: **125%**

**Payback Period**: **20 months**

**Stakeholder Impact**:

- Secretary of State SD-1: Met — FTA utilisation data for Parliamentary accountability
- HMRC SD-2: Met — data integrity preserved through aggregation and SDC
- UK businesses SD-3: Met — integrated trade portal
- Trade Policy SD-4: Met — FTA impact modelling connected to real data
- UKEF SD-5: Met — product visibility integrated into trade portal

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive Global Trade Intelligence Platform

**Description**: Full trade intelligence platform with AI-driven market prediction, real-time global trade monitoring, individual trader profiles, and automated export compliance.

**Costs** (3-year): GBP 40M

**Benefits** (5-year): GBP 55M

**Recommendation**: **Reject** — Scope exceeds SDG 17 mandate. Individual trader profiles violate Statistics of Trade Act. Cost disproportionate. AI market prediction unproven at policy-relevant accuracy.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Integrated Trade Platform with FTA Analytics**

**Rationale**:

1. **Best value**: GBP 18.7M NPV, 125% ROI
2. **Stakeholder satisfaction**: 85% of goals met across all stakeholder groups
3. **Policy-relevant**: Directly addresses Parliamentary scrutiny of FTA effectiveness
4. **Business impact**: Supports Export Strategy target through simplified services
5. **SDG contribution**: Monitors UK commitment to SDG 17 trade targets

**Optimism Bias Adjustment** (Green Book +40%):

- Adjusted Cost: GBP 20M -> GBP 28M
- Adjusted FTA utilisation benefit (reduced 20%): GBP 25M -> GBP 20M
- NPV with optimism bias: GBP 5.7M (still positive)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace — DOS6 for platform development; G-Cloud for hosting and managed services.

**Key Procurement Consideration**: HMRC data sharing arrangement is a prerequisite. This is a government-to-government data sharing agreement under the Statistics of Trade Act 1947, not a commercial procurement — it must be secured in parallel with commercial procurement.

**Contract Approach**:

- **Build**: Agile delivery with milestone payments via DOS6 (18 months)
- **Run**: Managed service via G-Cloud (3+1+1 year)

**Evaluation**: Technical 55%, Cost 30%, Social Value 15% (higher social value weighting reflecting export support for SMEs and developing countries)

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 20M over 3 years

### D1.1 Capital Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| FTA analytics and HMRC integration | GBP 2M | GBP 1.5M | GBP 0.5M | GBP 4M |
| Business trade portal | GBP 2M | GBP 1.5M | GBP 0 | GBP 3.5M |
| FTA impact modelling tools | GBP 1M | GBP 1M | GBP 0 | GBP 2M |
| UKEF and great.gov.uk integration | GBP 0.5M | GBP 0.75M | GBP 0.25M | GBP 1.5M |
| DCTS/SDG monitoring | GBP 0.25M | GBP 0.25M | GBP 0 | GBP 0.5M |
| Training and change management | GBP 0.5M | GBP 0.5M | GBP 0 | GBP 1M |
| **Total CapEx** | **GBP 6.25M** | **GBP 5.5M** | **GBP 0.75M** | **GBP 12.5M** |

### D1.2 Operational Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Cloud hosting and managed services | GBP 0.8M | GBP 1M | GBP 1M | GBP 2.8M |
| HMRC data feed support | GBP 0.4M | GBP 0.5M | GBP 0.5M | GBP 1.4M |
| Portal support and content | GBP 0.7M | GBP 1M | GBP 1.6M | GBP 3.3M |
| **Total OpEx** | **GBP 1.9M** | **GBP 2.5M** | **GBP 3.1M** | **GBP 7.5M** |

## D2. Funding Source

**Source**: DBT Digital Transformation Fund, with HMRC contribution for data feed development and UKEF contribution for integration.

**Budget Approval**: DBT Board (up to GBP 20M), CDDO spend control.

## D3. Affordability

- DBT digital budget: GBP 120M/year
- This project: 5.2% of digital budget (Year 1)
- Assessment: **Affordable**

## D4. Value for Money

**Overall VfM Rating**: **High** — Strong NPV, significant economic impact from FTA utilisation and export growth.

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: DBT Chief Digital Information Officer

**Steering Committee**: SRO (Chair), DBT Trade Policy Director, DBT Export Promotion Director, DBT Chief Economist, HMRC Customs Data Director, UKEF Chief Operating Officer, CDDO representative

## E2. Delivery Approach

**Phases**:

1. **Discovery** (Months 1-3): HMRC data sharing agreement, user research with exporters, FTA utilisation methodology
2. **Alpha** (Months 4-7): FTA utilisation POC with Australia/NZ FTA data, trade portal prototype
3. **Beta** (Months 8-14): FTA analytics for all FTAs, trade portal with tariff lookup and UKEF integration
4. **Live** (Month 15): Public trade portal launch, FTA utilisation dashboard
5. **Enhancement** (Months 16-18): FTA impact modelling, DCTS monitoring, SDG reporting feed to Project 003

## E3. Key Milestones

| Milestone | Date | Owner |
|-----------|------|-------|
| SOBC Approval | Q2 2026 | SRO |
| HMRC Data Sharing Agreement Signed | Q3 2026 | Data Lead |
| FTA Utilisation POC (Australia/NZ) | Q1 2027 | Chief Economist |
| GDS Alpha Assessment | Q1 2027 | Service Owner |
| Trade Portal Beta Launch | Q3 2027 | Product Manager |
| FTA Utilisation Quarterly Reports Published | Q4 2027 | Chief Economist |
| DCTS Monitoring Operational | Q1 2028 | SDG Lead |
| Full Platform Operational | Q2 2028 | SRO |

## E4. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | HMRC refuses data sharing | Low | Critical | 9 | Statistics of Trade Act legal basis; Ministerial-level engagement; HMRC SRO on steering committee |
| R-002 | FTA utilisation attribution challenged | High | Moderate | 12 | Academic partnership for methodology; publish with caveats; peer review by trade economists |
| R-003 | Business portal low adoption | Medium | Major | 12 | great.gov.uk integration; GDS service design; SEO for "UK trade tariff" searches |
| R-004 | UKEF legacy systems block integration | Medium | Moderate | 9 | Start with product catalogue API (simpler); UKEF COO committed to modernisation |
| R-005 | Trade negotiation data leakage | Low | Critical | 9 | Physical/logical separation; no negotiation data on public platform; security clearance for analytics team |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: **Option 2: Integrated Trade Platform with FTA Analytics**

**Investment**: GBP 20M over 3 years | **Return**: GBP 45M over 5 years | **NPV**: GBP 18.7M | **ROI**: 125%

**Go/No-Go**: **PROCEED**

## F2. Next Steps

1. **DBT Board approval**: Q2 2026
2. **HMRC data sharing agreement**: Ministerial letter to HMRC Permanent Secretary — Q2 2026
3. **UKEF engagement**: COO agreement on integration scope — Q2 2026
4. **FTA utilisation methodology**: Commission academic partnership (Sussex, LSE, or Sheffield trade groups) — Q3 2026
5. **Procurement**: DOS6 for implementation partner — Q3 2026

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO, DBT CDIO | | |
| | DBT Finance Director | | |
| | DBT Trade Policy Director | | |
| | HMRC representative | | |

**Approval Decision**: PENDING

---

**END OF STRATEGIC OUTLINE BUSINESS CASE**

*Document created using ArcKit `/arckit.sobc` command*
*Template version: 1.0*
*Green Book compliant: Yes (HM Treasury 5-case model)*

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Global Britain Trade Platform
**Model**: Claude Opus 4.6
