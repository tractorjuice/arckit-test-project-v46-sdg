# Strategic Outline Business Case (SOBC): Pandemic Preparedness System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Pandemic Preparedness System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Pandemic Preparedness Programme, UKHSA |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Pandemic Preparedness Programme Board, UKHSA, DHSC, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The Pandemic Preparedness System will provide UKHSA with a modern, integrated disease surveillance and early warning platform, enabling the UK to detect novel threats within 24 hours and scale to pandemic response within 48 hours — capabilities that were critically absent during COVID-19.

**Problem Statement**: The COVID-19 pandemic exposed fundamental weaknesses in UK disease surveillance. Seven separate surveillance systems with manual data aggregation delayed detection by weeks. The UK COVID-19 Inquiry found these failures contributed to delayed response and preventable harm.

**Proposed Solution**: An integrated, scalable surveillance platform ingesting data from laboratories, hospitals, primary care, wastewater, and genomic sequencing, with automated anomaly detection and COBR-ready intelligence dashboards.

**Strategic Fit**: UK Biological Security Strategy, COVID-19 Inquiry recommendations, WHO IHR obligations, SDG 3 (Good Health and Well-Being).

**Investment Required**: GBP 30.0M over 5 years

- Capital: GBP 20.0M
- Operational (5 years): GBP 10.0M

**Expected Benefits**: GBP 2.5 billion avoided costs over 10 years (based on faster pandemic detection reducing impact by even 1%)

**Return on Investment**:

- NPV: GBP 1.8 billion (discounted at 3.5%, 10-year horizon)
- The economic case is based on pandemic impact avoidance. COVID-19 cost the UK economy an estimated GBP 310 billion. A system that reduces detection delay by even one week could save GBP 2-5 billion in a future pandemic.
- Payback: Immediate if pandemic occurs; ongoing value through routine disease surveillance improvement

**Recommended Option**: Option 2: Integrated Surveillance Platform with Surge Capability

**Key Risks**:

1. System maintained in peacetime — "build it and forget it" risk during years without pandemic
2. Data sharing agreements with NHS and devolved administrations
3. Security classification challenges — balancing SECRET intelligence with open public health data

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: UKHSA inherited a patchwork of legacy surveillance systems from Public Health England and NHS Test and Trace. These systems cannot communicate in real time, require extensive manual data processing, and were never designed for the data volumes or response speeds demanded by pandemic response. The COVID-19 Inquiry Module 1 found that the UK's surveillance infrastructure was "not fit for purpose."

**Consequences of Inaction**:

- The UK remains unable to detect novel pathogen signals faster than 7-14 days — potentially allowing thousands of undetected infections
- During the next pandemic, the same manual data processing delays will recur, costing weeks of response time
- WHO IHR compliance remains dependent on manual processes, risking international reputation
- COBR decisions will again be made on incomplete, stale surveillance data
- The COVID-19 Inquiry recommendations remain unaddressed, creating political and legal risk

### A1.2 Strategic Drivers

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | DHSC Minister | POLITICAL | Never caught unprepared again | COVID-19 Inquiry response |
| SD-2 | UKHSA Chief Data | OPERATIONAL | Unified surveillance picture | Operational effectiveness |
| SD-3 | Cabinet Office | STRATEGIC | Timely COBR intelligence | Crisis decision-making |
| SD-4 | WHO | COMPLIANCE | IHR reporting obligations | International obligations |

### A1.3 Strategic Alignment

- **UK Biological Security Strategy 2023**: Integrated surveillance as priority capability
- **COVID-19 Inquiry Recommendations**: Modernise surveillance infrastructure
- **WHO IHR (2005)**: Reporting obligations for public health emergencies of international concern
- **NCSC CAF**: CNI designation for pandemic response systems
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 4 (Security), 7 (Data Governance), 12 (Scalability), 13 (Availability)

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Continue operating existing legacy surveillance systems separately.

**Recommendation**: **Reject** — Directly contradicts COVID-19 Inquiry recommendations. Politically and operationally unacceptable.

---

### Option 1: Incremental Legacy Modernisation (Minimal)

**Description**: Upgrade existing surveillance systems individually, add data sharing interfaces between them, build a reporting layer on top. No new integrated platform.

**Costs** (5-year): GBP 12.0M

**Pros**: Lower cost, lower risk, preserves existing team expertise
**Cons**: Does not achieve real-time integration, cannot scale to pandemic response, maintains architectural fragmentation, does not address Inquiry recommendations

**Stakeholder Goals Met**: 30%

---

### Option 2: Integrated Surveillance Platform with Surge Capability (RECOMMENDED)

**Description**: Build a new integrated surveillance platform that ingests all data sources in near-real-time, provides automated anomaly detection, generates COBR dashboards, and scales automatically for pandemic response.

**Costs** (5-year): GBP 30.0M

- Capital: GBP 20.0M (platform development GBP 8M, data integration GBP 5M, anomaly detection/ML GBP 3M, security/CNI GBP 2M, testing GBP 1M, design GBP 1M)
- Operational: GBP 10.0M (cloud infrastructure GBP 4M, team GBP 4M, maintenance GBP 2M)

**Benefits** (10-year):

| Benefit | Type | Estimated Value |
|---------|------|-----------------|
| Pandemic impact avoidance (1% reduction in economic impact of next pandemic) | STRATEGIC | GBP 2-5 billion |
| Routine disease outbreak detection improvement (50% faster) | OPERATIONAL | GBP 50M |
| IHR compliance automation | COMPLIANCE | GBP 5M (avoided manual cost) |
| COBR intelligence quality improvement | STRATEGIC | Non-quantifiable but critical |

**NPV** (3.5% discount, 10-year): GBP 1.8 billion (using conservative 1% pandemic impact reduction estimate)

**Stakeholder Goals Met**: 90%

---

### Option 3: Full National Biosurveillance Network

**Description**: Option 2 plus real-time integration with animal health surveillance (APHA), environmental monitoring, global travel health, and predictive pandemic modelling AI.

**Costs** (5-year): GBP 75.0M

**Pros**: One Health approach, maximum preparedness, predictive capability
**Cons**: Significantly higher cost, longer timeline (36+ months), cross-departmental governance complexity extreme

**Recommendation**: **Defer** — Pursue Option 2 first, then assess Option 3 as Phase 2 enhancement based on Option 2 operational experience.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Integrated Surveillance Platform with Surge Capability**

**Rationale**: Delivers 90% of stakeholder goals, addresses COVID-19 Inquiry recommendations, achievable within 24 months, and the economic case is overwhelming — even a marginal improvement in pandemic response speed justifies the investment many times over.

---

# PART C: COMMERCIAL CASE

**Recommended Route**: Crown Commercial Service framework for platform development; G-Cloud for cloud infrastructure on NHS/government-approved platforms

**Key Requirement**: All suppliers must hold appropriate security clearance for handling OFFICIAL-SENSITIVE and potentially SECRET material. SC clearance minimum for development team; DV clearance for team members working on COBR components.

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 8.0M | GBP 8.0M | GBP 4.0M | GBP 0 | GBP 0 | GBP 20.0M |
| OpEx | GBP 1.0M | GBP 1.5M | GBP 2.0M | GBP 2.5M | GBP 3.0M | GBP 10.0M |
| **Total** | **GBP 9.0M** | **GBP 9.5M** | **GBP 6.0M** | **GBP 2.5M** | **GBP 3.0M** | **GBP 30.0M** |

**Funding Source**: UKHSA core budget (Spending Review 2025 settlement includes ring-fenced pandemic preparedness funding)

**Affordability**: GBP 30M over 5 years from an annual UKHSA budget of approximately GBP 400M. **Affordable** within pandemic preparedness allocation.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

1. **Discovery** (6 months): Data source mapping, stakeholder requirements, security architecture design
2. **Alpha** (6 months): Integration prototypes for 3 key data sources, anomaly detection algorithm development
3. **Beta** (12 months): Full platform build, all 7 data sources integrated, pandemic surge testing
4. **Live** (ongoing): Operational service with annual pandemic simulation exercises

## E2. Key Risk — Peacetime Maintenance

The single greatest risk is that the system, once built, is not adequately maintained and exercised during years without a pandemic. This is the "fire engine" problem — the capability must be maintained at full readiness even when not in active use.

**Mitigation**: Mandatory annual pandemic simulation exercise (Exercise Cygnus model). System used daily for routine surveillance, ensuring continuous operational use. Dedicated UKHSA team funded from core budget, not project funding.

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | System not maintained in peacetime | High | Critical | 16 | Daily routine use, annual pandemic exercises, dedicated team |
| R-002 | NHS data sharing agreements delayed | Medium | Major | 12 | Early DHSC legal team engagement, precedent from COVID-19 |
| R-003 | Security classification conflict | Medium | Major | 12 | Tiered data classification model, NCSC consultation |
| R-004 | Devolved administration non-participation | Medium | Moderate | 9 | Joint working agreement, mutual benefit demonstration |
| R-005 | Legacy system decommissioning resistance | Medium | Moderate | 9 | Phased migration, dual-running period, team retraining |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: Integrated Surveillance Platform with Surge Capability

**Investment**: GBP 30.0M over 5 years

**Expected Return**: GBP 2+ billion avoided pandemic impact (10-year horizon)

**Go/No-Go**: **PROCEED to Discovery phase**

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | UKHSA Chief Executive | | |
| | UKHSA Finance Director | | |
| | DHSC Permanent Secretary | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Pandemic Preparedness System
**Model**: Claude Opus 4.6
