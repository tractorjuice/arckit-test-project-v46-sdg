# Strategic Outline Business Case: Heritage Asset Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Heritage Asset Management (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Heritage Asset Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Heritage Asset Management Programme Board, DCMS, Historic England, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for a digital heritage asset management platform, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Modernise the National Heritage List for England (NHLE) and heritage protection processes through a digital platform providing accurate spatial data, streamlined Listed Building Consent workflows, IoT structural monitoring, and API-enabled planning system integration.

**Problem Statement**: The NHLE contains 400,000+ entries, but approximately 60% have only point (pin) locations rather than accurate polygon boundaries, making spatial analysis unreliable. Conservation officer numbers have declined 35% since 2006. Heritage crime causes GBP 2 billion in damage annually, with much heritage loss resulting from planning decisions made with incomplete heritage data. Listed Building Consent determination takes an average of 12 weeks, with significant time spent on manual consultee management.

**Proposed Solution**: A digital heritage asset management platform providing NHLE data digitisation with polygon boundaries, automated LBC workflow management, IoT structural monitoring integration (Project 001), and real-time heritage data API for planning system integration (Project 002).

**Strategic Fit**: Supports Heritage Protection Reform, NPPF heritage policies (paragraphs 189-208), Heritage at Risk programme, and the SDG 11 urban sustainability agenda. Directly enables heritage constraint checking in Project 002 (Urban Planning Analytics).

**Investment Required**: GBP 8M over 3 years

- Capital: GBP 5.5M
- Operational (3 years): GBP 2.5M

**Expected Benefits**: GBP 28M over 5 years

- Heritage damage prevention: GBP 15M (reduced heritage crime and planning oversights)
- Conservation officer time savings: GBP 8M (30% LBC time reduction)
- Planning system efficiency: GBP 3M (automated heritage constraint checking via Project 002)
- Heritage tourism data value: GBP 2M (open data enabling heritage tourism)

**Return on Investment**:

- NPV: GBP 15.2M (discounted at 3.5%)
- Payback Period: 16 months
- ROI: 250%

**Recommended Option**: Option 2: Integrated Heritage Digital Platform

**Key Risks**:

1. NHLE data digitisation slower than planned (mitigation: phased approach, priority by Heritage at Risk status)
2. Legal sensitivity of NHLE record changes (mitigation: full audit trail, Historic England sign-off workflow)
3. Amenity society resistance to digital consultation (mitigation: multi-channel approach, training)

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: England's heritage protection system relies on a database (NHLE) with significant data quality issues — 60% of entries have point locations only, many descriptions are inadequate, and spatial data is insufficient for reliable automated constraint checking. Conservation officers (35% decline since 2006) spend significant time on administrative tasks: chasing amenity society consultations, manually checking heritage records, and tracking Listed Building Consent workflows in spreadsheets. Heritage crime costs GBP 2 billion annually, with much damage resulting from planning decisions made without adequate heritage awareness.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| Historic England | 60% of NHLE entries lack polygon boundaries | Cannot support spatial planning analytics | CRITICAL |
| Conservation Officers | Manual LBC workflow management | 35% of time on administration vs. assessment | HIGH |
| Planning Officers | Heritage constraint oversights (3-5%) | Unlawful damage to heritage assets | HIGH |
| Heritage Crime Partnership | Slow detection of unauthorised works | GBP 2B annual heritage crime damage | MEDIUM |

**Consequences of Inaction**:
- Heritage damage continues at GBP 2B/year with inadequate detection
- Project 002 (Urban Planning Analytics) cannot provide reliable heritage constraint checking
- Conservation officer resource crisis worsens without efficiency tools
- NHLE data quality degrades further as records are not maintained

### A1.2 Strategic Alignment

- **NPPF Heritage Policies (Paragraphs 189-208)**: Accurate heritage data enables proper application of NPPF heritage tests
- **Heritage at Risk Programme**: IoT monitoring enables proactive conservation rather than reactive crisis management
- **Heritage Protection Reform**: Digital NHLE enables faster, more consistent listing decisions
- **SDG 11 Programme**: Heritage asset data is a critical dependency for Project 002 (Urban Planning Analytics)
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 3 (Geospatial Interoperability), 10 (Data Quality), 11 (Single Source of Truth)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (5-year): GBP 0 additional, but GBP 2B/year heritage crime continues
**Benefits**: GBP 0
**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject**

### Option 1: NHLE Data Improvement Only

**Description**: Funded programme to digitise NHLE records with polygon boundaries. No workflow tools, no IoT integration, no API.
**Costs** (5-year): GBP 4M
**Benefits** (5-year): GBP 12M (heritage damage reduction from better data)
**Stakeholder Goals Met**: 30%
**Recommendation**: **Insufficient** — addresses data quality but not workflow, monitoring, or integration.

### Option 2: Integrated Heritage Digital Platform (RECOMMENDED)

**Description**: Comprehensive platform: NHLE digitisation, LBC workflow management, IoT monitoring integration, heritage data API, and heritage crime evidence repository.

**Costs** (5-year): GBP 10.5M (GBP 5.5M CapEx + GBP 5M OpEx)

**Benefits** (5-year):

| Benefit | Type | 5-Year Total |
|---------|------|--------------|
| Heritage damage prevention | RISK | GBP 15M |
| Conservation officer time savings | FINANCIAL | GBP 8M |
| Planning system efficiency (via Project 002) | OPERATIONAL | GBP 3M |
| Heritage tourism data value | STRATEGIC | GBP 2M |
| **Total** | | **GBP 28M** |

**NPV**: GBP 15.2M (3.5% discount rate)
**ROI**: 250%
**Payback**: 16 months
**Stakeholder Goals Met**: 85%

### Option 3: Full National Heritage Information System

**Description**: Comprehensive replacement of all heritage information systems including archaeological records, conservation area appraisals, and heritage tourism platforms.
**Costs** (5-year): GBP 30M
**Benefits** (5-year): GBP 32M
**Stakeholder Goals Met**: 100%
**Recommendation**: **Reject** — Marginal benefits over Option 2, double the cost, significant integration risk with established heritage sector systems.

## B3. Recommended Option

**Option 2**: Best value (NPV GBP 15.2M), addresses core heritage data and workflow needs, enables SDG 11 programme integration.

**Optimism Bias**: +40% on costs. Adjusted NPV still positive at GBP 11.0M.

---

# PART C: COMMERCIAL CASE

**Sourcing Route**: Digital Marketplace — G-Cloud for platform, DOS for heritage data specialists.
**Key Requirement**: Vendor must demonstrate heritage/conservation domain expertise and experience with spatial data digitisation at scale.
**Evaluation**: Technical 60%, Cost 30%, Social Value 10%.

**Social Value Focus**: Heritage skills training, conservation apprenticeships, digitisation employment in regional HE offices (not London-centric).

---

# PART D: FINANCIAL CASE

## D1. Budget

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 2M | GBP 1M | GBP 0.5M | GBP 3.5M |
| NHLE data digitisation | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| IoT monitoring integration | GBP 0.2M | GBP 0.2M | GBP 0.1M | GBP 0.5M |
| **CapEx Total** | **GBP 2.7M** | **GBP 1.7M** | **GBP 1.1M** | **GBP 5.5M** |
| Platform operations | GBP 0.4M | GBP 0.5M | GBP 0.6M | GBP 1.5M |
| NHLE data validation (ongoing) | GBP 0.3M | GBP 0.3M | GBP 0.4M | GBP 1.0M |
| **OpEx Total** | **GBP 0.7M** | **GBP 0.8M** | **GBP 1.0M** | **GBP 2.5M** |
| **Grand Total** | **GBP 3.4M** | **GBP 2.5M** | **GBP 2.1M** | **GBP 8M** |

**Funding Source**: DCMS Heritage Capital Programme (Spending Review 2025).
**Affordability**: **Affordable** — 2% of annual DCMS heritage funding.

---

# PART E: MANAGEMENT CASE

## E1. Delivery

**Methodology**: Agile with heritage sector governance gates.
**Phases**: Discovery (3 months), Alpha (3 months), Beta (6 months), Live (ongoing).
**Critical Dependency**: NHLE data digitisation is a multi-year effort — platform must deliver value before full digitisation completes. Prioritise Heritage at Risk entries and entries in areas where Project 002 is being deployed.

## E2. Key Risks

| Risk | Likelihood | Impact | Score | Mitigation |
|------|------------|--------|-------|------------|
| NHLE digitisation slower than planned | Medium | High | 12 | Phased by risk priority, automated boundary detection from OS MasterMap |
| Legal sensitivity of record changes | Medium | High | 12 | Full audit trail, HE sign-off workflow |
| Amenity society digital resistance | Medium | Medium | 9 | Multi-channel (digital + paper), volunteer training |
| IoT sensor reliability at heritage sites | Medium | Medium | 9 | Redundant sensors, non-invasive installation methods |
| Conservation officer digital skills gap | High | Medium | 12 | Training programme, UX designed for non-technical users |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: Integrated Heritage Digital Platform
**Investment**: GBP 8M over 3 years
**Expected Return**: GBP 28M over 5 years (NPV: GBP 15.2M)
**Go/No-Go**: **PROCEED**

**Next Steps**:
1. Secure DCMS funding approval: Q2 2026
2. Historic England partnership agreement: Q2 2026
3. NHLE digitisation pilot (1,000 records in target LPA areas): Q3 2026
4. API specification agreement with Project 002: Q2 2026
5. Amenity society engagement programme: Q3 2026

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Heritage Asset Management (Project 004)
**Model**: Claude Opus 4.6
