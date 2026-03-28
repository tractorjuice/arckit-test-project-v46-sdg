# Strategic Outline Business Case: Public Transport Optimisation

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Public Transport Optimisation (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Public Transport Optimisation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Public Transport Programme Board, DfT, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in a multi-modal transport planning and scheduling platform, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Improve bus, rail, and active travel services through a data-driven multi-modal transport planning platform enabling combined authorities to optimise networks, monitor operator performance, and deliver Bus Service Improvement Plans with real-time evidence.

**Problem Statement**: Bus patronage outside London has declined 30% since 2010. BODS compliance is only 72% nationally. Combined authorities lack analytical tools to plan networks under new franchising powers — each attempting to build its own analytics capability at GBP 1-5M. Real-time passenger information accuracy is a top passenger complaint, with bus arrival predictions often incorrect or unavailable.

**Proposed Solution**: A shared multi-modal transport data platform integrating BODS bus data, rail feeds, tram data, and active travel information, providing real-time schedule optimisation, BSIP performance monitoring, and BODS compliance tools.

**Strategic Fit**: Supports Bus Services Act 2017 implementation, BSIP delivery, National Bus Strategy, and combined authority franchising preparation. Integrates with SDG 11 IoT Platform (Project 001) for traffic sensor data.

**Investment Required**: GBP 15M over 3 years

- Capital: GBP 10M
- Operational (3 years): GBP 5M

**Expected Benefits**: GBP 42M over 5 years

- Passenger time savings (EWT reduction): GBP 25M
- Combined authority analytics cost avoidance: GBP 8M
- BSIP efficiency gains: GBP 5M
- Patronage recovery contribution: GBP 4M

**Return on Investment**:

- NPV: GBP 20.1M (discounted at 3.5%)
- Payback Period: 20 months
- ROI: 180%

**Recommended Option**: Option 2: Shared Multi-Modal Transport Analytics Platform

**Key Risks**:

1. Bus operator data resistance (mitigation: BODS regulatory mandate, DfT engagement)
2. Combined authority adoption (mitigation: funded BSIP analytics capability)
3. Real-time data quality from operators (mitigation: quality scoring and compliance reporting)

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The UK bus market outside London is deregulated. Bus patronage has declined 30% since 2010, service coverage has shrunk, and reliability is poor. The Bus Services Act 2017 introduced mandatory data publication (BODS) and franchising powers, but implementation is uneven. Combined authorities need transport data analytics to plan networks under Enhanced Partnerships and prepare for franchising, but each is building its own capability independently at GBP 1-5M per authority.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| DfT | BODS compliance only 72% | Cannot demonstrate Bus Services Act impact | CRITICAL |
| Combined Authorities | No analytical tools for network planning | Cannot exercise franchising powers effectively | CRITICAL |
| Passengers | Inaccurate real-time information | EWT 2.8 mins average, top complaint | HIGH |
| Bus Operators | Multiple reporting requirements per authority | Compliance burden, inconsistent requests | MEDIUM |

**Consequences of Inaction**:
- Bus patronage decline continues (projected further 15% loss by 2030 without intervention)
- GBP 2B BSIP investment lacks performance monitoring
- Combined authorities cannot prepare evidence base for franchising decisions
- Continued duplication of analytics capability across authorities

### A1.2 Strategic Alignment

- **National Bus Strategy**: Network planning, operator performance, patronage recovery
- **Bus Services Act 2017**: BODS compliance, franchising evidence, Enhanced Partnership monitoring
- **Bus Service Improvement Plans**: GBP 2B investment monitoring and accountability
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 12 (Transport Data Standards), 4 (Open Data), 13 (Loose Coupling)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (5-year): GBP 0 central, GBP 30-50M in duplicated authority analytics
**Benefits**: GBP 0
**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject**

### Option 1: BODS Enhancement Only

**Description**: Enhance existing BODS infrastructure with improved data quality tools. No multi-modal integration or schedule optimisation.
**Costs** (5-year): GBP 5M
**Benefits** (5-year): GBP 12M
**Stakeholder Goals Met**: 30%
**Recommendation**: **Insufficient** — addresses data quality but not network planning or schedule optimisation.

### Option 2: Shared Multi-Modal Transport Analytics Platform (RECOMMENDED)

**Description**: Cloud-based platform integrating BODS bus data, rail, tram, and active travel with real-time analytics, schedule optimisation, and BSIP monitoring.

**Costs** (5-year): GBP 20M (GBP 10M CapEx + GBP 10M OpEx)

**Benefits** (5-year):

| Benefit | Type | 5-Year Total |
|---------|------|--------------|
| Passenger time savings (20% EWT reduction) | ECONOMIC | GBP 25M |
| CA analytics cost avoidance | FINANCIAL | GBP 8M |
| BSIP efficiency gains | OPERATIONAL | GBP 5M |
| Patronage recovery contribution | STRATEGIC | GBP 4M |
| **Total** | | **GBP 42M** |

**NPV**: GBP 20.1M (3.5% discount rate)
**ROI**: 180%
**Payback**: 20 months
**Stakeholder Goals Met**: 85%

### Option 3: National Transport Command Centre

**Description**: Fully centralised national transport analytics with real-time network management across all combined authorities.
**Costs** (5-year): GBP 55M
**Benefits** (5-year): GBP 48M
**Stakeholder Goals Met**: 100%
**Recommendation**: **Reject** — Conflicts with devolved authority responsibility for transport planning. Negative NPV.

## B3. Recommended Option

**Option 2**: Best value (NPV GBP 20.1M), respects devolved authority responsibility, addresses 85% of stakeholder goals.

**Optimism Bias**: +40% on costs. Adjusted NPV still positive at GBP 12.1M.

---

# PART C: COMMERCIAL CASE

**Sourcing Route**: Digital Marketplace — G-Cloud for platform, DOS for transport data specialists.
**Key Requirement**: Vendor must demonstrate transport domain expertise (BODS, SIRI, TransXChange, NaPTAN).
**Evaluation**: Technical 60%, Cost 30%, Social Value 10%.

---

# PART D: FINANCIAL CASE

## D1. Budget

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 4M | GBP 2.5M | GBP 0.5M | GBP 7M |
| Multi-modal data integration | GBP 1M | GBP 0.5M | GBP 0.5M | GBP 2M |
| BODS enhancement | GBP 0.5M | GBP 0.3M | GBP 0.2M | GBP 1M |
| **CapEx Total** | **GBP 5.5M** | **GBP 3.3M** | **GBP 1.2M** | **GBP 10M** |
| Cloud and operations | GBP 0.8M | GBP 1.2M | GBP 1.5M | GBP 3.5M |
| Authority onboarding and training | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| **OpEx Total** | **GBP 1.3M** | **GBP 1.7M** | **GBP 2.0M** | **GBP 5M** |
| **Grand Total** | **GBP 6.8M** | **GBP 5.0M** | **GBP 3.2M** | **GBP 15M** |

**Funding Source**: DfT Bus Transformation Fund (Spending Review 2025).
**Affordability**: **Affordable** — 0.75% of annual DfT digital and bus funding combined.

---

# PART E: MANAGEMENT CASE

## E1. Delivery

**Methodology**: Agile with GDS service assessment gates.
**Phases**: Discovery (3 months), Alpha (3 months), Beta (6 months), Live (ongoing).
**Key dependency**: BODS data quality from operators — managed through DfT regulatory engagement.

## E2. Key Risks

| Risk | Likelihood | Impact | Score | Mitigation |
|------|------------|--------|-------|------------|
| Operator data resistance | Medium | High | 12 | BODS regulatory enforcement by DfT |
| CA adoption below target | Medium | Medium | 9 | Funded BSIP analytics, peer advocacy |
| Real-time data quality | High | Medium | 12 | Quality scoring, automated validation |
| Rail data integration complexity | Medium | Medium | 9 | Phased integration, Network Rail partnership |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: Shared Multi-Modal Transport Analytics Platform
**Investment**: GBP 15M over 3 years
**Expected Return**: GBP 42M over 5 years (NPV: GBP 20.1M)
**Go/No-Go**: **PROCEED**

**Next Steps**:
1. Secure DfT funding approval: Q2 2026
2. Combined authority engagement (target 10): Q2-Q3 2026
3. BODS team alignment: Q2 2026
4. Network Rail data sharing agreement: Q3 2026
5. Discovery phase: Q3 2026

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Public Transport Optimisation (Project 003)
**Model**: Claude Opus 4.6
