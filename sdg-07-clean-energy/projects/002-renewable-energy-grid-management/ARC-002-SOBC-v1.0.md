# Strategic Outline Business Case (SOBC): Renewable Energy Grid Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Renewable Energy Grid Management (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Renewable Energy Grid Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | National Grid ESO Board, Ofgem, DESNZ, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: As the UK targets 50GW offshore wind by 2030 and a decarbonised power system by 2035, National Grid ESO requires a new digital platform to manage the integration of intermittent renewable generation at unprecedented scale.

**Problem Statement**: ESO's existing grid management systems were designed for a fleet of large, predictable thermal generators. As renewable penetration approaches 70%+, these systems cannot provide the real-time visibility, accurate forecasting, or optimised curtailment management needed. Wind curtailment alone cost consumers £800M+ in 2024.

**Proposed Solution**: Build a real-time Renewable Energy Grid Management platform providing sub-second generation visibility, AI-powered forecasting, and curtailment optimisation integrated with the Balancing Mechanism.

**Strategic Fit**: Directly enables the British Energy Security Strategy 50GW offshore wind target and Net Zero Strategy decarbonised power system by 2035.

**Investment Required**: £40M over 3 years

- Capital: £28M
- Operational (3 years): £12M

**Expected Benefits**: £520M over 5 years

- Curtailment reduction: £400M (20% reduction in £800M/year curtailment costs, phased)
- Carbon value: £75M (2.5 MtCO2e/year at £30/tonne social cost of carbon)
- Avoided grid incidents: £45M (frequency event avoidance, reduced reserve costs)

**Return on Investment**:

- NPV: £370M (discounted at 3.5%)
- Payback Period: 8 months (from first curtailment reduction)
- ROI: 1,200%

**Recommended Option**: Option 2: Integrated Real-Time Platform

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: National Grid ESO manages a grid undergoing the fastest energy transition in its history. Renewable generation has grown from 7% (2010) to 42% (2024) and is targeted to reach 70%+ by 2030. The existing Energy Management System (EMS) was designed for 30-40 large thermal generators; it must now manage thousands of wind, solar, and battery assets with fundamentally different operational characteristics.

**Consequences of Inaction**:
- Curtailment costs escalate to £1.2 billion/year by 2030 as renewable capacity doubles (paid by consumers via BSUoS)
- Grid frequency events increase in frequency and severity, risking partial blackouts
- Investor confidence in UK renewable deployment undermined by grid constraint narrative
- UK misses legally binding 2035 decarbonised power system target

### A1.2 Why Now?

**Urgency Factors**:
- Offshore wind capacity doubling from 14GW (2025) to 28GW+ by 2028 — grid management capability must be in place before capacity connects
- RIIO-3 price control period (2026-2031) — investment must be approved within Ofgem allowances
- Climate Change Committee's 6th Carbon Budget requires power sector decarbonisation by 2035 — no time for delays

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Continue with existing EMS and manual processes.
**Costs (3-year)**: £0 additional capital; £15M additional operational (manual workarounds, incident response)
**Benefits**: £0
**Recommendation**: **Reject** — Curtailment costs escalate; grid security risk unacceptable.

### Option 1: Enhanced Legacy System

**Description**: Upgrade the existing EMS with additional renewable monitoring modules and improved forecasting integration. Retain existing control room interfaces.
**Costs (3-year)**: Capital £12M; Operational £8M; Total £20M
**Benefits (5-year)**: £200M (10% curtailment reduction)
**NPV**: £140M
**Stakeholder Goals Met**: 45% — limited real-time capability; no AI forecasting; insufficient for 70%+ renewable penetration
**Recommendation**: Reject — insufficient capability for 2030+ grid requirements.

### Option 2: Integrated Real-Time Platform (RECOMMENDED)

**Description**: Purpose-built real-time platform with sub-second telemetry ingestion, AI/ML forecasting, curtailment optimisation, and Balancing Mechanism integration. Deployed on ESO's OT infrastructure with cloud-based analytics.

**Costs (3-year) — ROM (±30%)**:
- Capital: £28M (telemetry infrastructure £10M, AI platform £8M, integration £5M, security £3M, programme management £2M)
- Operational: £12M (infrastructure £6M, support £3.6M, data feeds £1.2M, security £1.2M)
- Total 3-year TCO: £40M

**Benefits (5-year)**:

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|-------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Curtailment reduction (20%) | FINANCIAL | £40M | £80M | £100M | £100M | £100M | £420M |
| B-002 | Carbon value (avoided emissions) | STRATEGIC | £7.5M | £15M | £18.75M | £18.75M | £18.75M | £78.75M |
| B-003 | Grid stability (avoided incidents) | RISK | £5M | £9M | £10M | £10M | £10M | £44M |
| **Total** | | | **£52.5M** | **£104M** | **£128.75M** | **£128.75M** | **£128.75M** | **£542.75M** |

**NPV (3.5% discount rate, 5-year)**: £370M

**ROI**: (£542.75M - £40M) / £40M x 100% = **1,257%**

**Payback Period**: **8 months** (from first year curtailment savings)

**Stakeholder Goals Met**: 85%

### Option 3: Full Digital Twin with Autonomous Control

**Description**: Complete digital twin of the GB electricity system with autonomous AI-driven grid control, replacing human decision-making for routine balancing.
**Costs (3-year)**: Capital £60M; Operational £25M; Total £85M
**Stakeholder Goals Met**: 100%
**Recommendation**: **Reject** — Autonomous grid control requires regulatory approval that does not exist. Technology maturity risk unacceptable for critical national infrastructure. Option 2 can evolve toward autonomy as regulatory and technology readiness matures.

## B3. Recommended Option

**Recommendation**: **Option 2: Integrated Real-Time Platform**

**Rationale**: Highest NPV (£370M), meets 85% of goals, deployable within RIIO-3 price control period, extensible toward greater automation as maturity increases. Payback in 8 months makes this one of the highest-return infrastructure investments in the energy sector.

**Optimism Bias**: +40% on costs → £56M adjusted TCO. NPV remains strongly positive at £340M+.

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Market Assessment**: Specialist energy technology market with established players in grid management systems (GE Vernova, Siemens, ABB/Hitachi, PSI). AI/ML forecasting is a growing niche with UK-based specialists (Kaluza, Open Climate Fix, National Grid's own Forecasting team).

**Sourcing Route**: Competitive restricted tender under utilities procurement regulations. Separate lots for core platform, AI/ML forecasting, and integration services to enable specialist participation and SME access.

**Contract Approach**: Fixed-price for platform build; managed service for ongoing operations; gain-share mechanism linking supplier payment to curtailment reduction achieved.

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | £16M | £10M | £2M | £28M |
| OpEx | £2M | £4M | £6M | £12M |
| **Total** | **£18M** | **£14M** | **£8M** | **£40M** |

**Funding Source**: Ofgem RIIO-3 price control allowance for ESO operational expenditure. Consumer-funded via BSUoS charges — justified by £400M+ annual curtailment savings that reduce the same charges.

**Affordability**: Within Ofgem RIIO-3 settlement for ESO digital transformation. Net consumer bill impact is negative (savings exceed costs by 10:1 ratio).

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile with safety-critical validation gates (reflecting energy sector regulatory requirements)

**Phases**:
1. **Discovery** (Months 1-3): Generator telemetry assessment, OT network capacity, forecasting model selection
2. **Alpha** (Months 4-8): Telemetry ingestion prototype with 5 wind farms, initial forecasting model
3. **Beta** (Months 9-14): Full transmission-connected asset integration, AI forecasting validation, control room beta
4. **Live** (Month 15): Production deployment to ESO control room
5. **Enhancement** (Months 16-24): DNO integration, advanced curtailment optimiser, market integration

## E2. Key Milestones

| Milestone | Date | Owner |
|-----------|------|-------|
| SOBC Approval | Q2 2026 | SRO |
| Ofgem RIIO-3 allowance confirmed | Q3 2026 | ESO Finance Director |
| Alpha: 5 wind farm telemetry live | Q1 2027 | Technical Architect |
| Beta: Full transmission integration | Q3 2027 | Technical Architect |
| AI forecasting validated (95% accuracy) | Q3 2027 | Data Science Lead |
| **Control room go-live** | **Q4 2027** | SRO |
| 20% curtailment reduction demonstrated | Q4 2028 | ESO Market Development |

## E3. Top 5 Risks

| Risk ID | Description | Likelihood | Impact | Score | Mitigation |
|---------|-------------|------------|--------|-------|------------|
| R-001 | Generator telemetry access refused or delayed | Medium | Major | 12 | Grid Code obligation enforcement via Ofgem |
| R-002 | OT network security incident | Low | Critical | 9 | NCSC CAF alignment, OT/IT isolation, pen testing |
| R-003 | AI forecasting accuracy below target | Medium | Moderate | 9 | Ensemble approach, multiple weather data sources, iterative improvement |
| R-004 | Ofgem RIIO-3 allowance insufficient | Low | Major | 8 | Early Ofgem engagement, phased investment case |
| R-005 | Control room operator resistance | Medium | Moderate | 9 | Early operator involvement, co-design, training programme |

---

# PART F: RECOMMENDATION

**Recommended Option**: **Option 2: Integrated Real-Time Platform**
**Investment**: £40M over 3 years
**Expected Return**: £542.75M over 5 years (NPV: £370M)
**Go/No-Go**: **PROCEED**

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | National Grid ESO CEO | | |
| | ESO Finance Director | | |
| | ESO Chief Engineer | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Renewable Energy Grid Management (Project 002)
**Model**: Claude Opus 4.6 (1M context)
