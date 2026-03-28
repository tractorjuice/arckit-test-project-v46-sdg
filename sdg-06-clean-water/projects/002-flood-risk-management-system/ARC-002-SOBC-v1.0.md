# Strategic Outline Business Case (SOBC): Flood Risk Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Flood Risk Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Flood Risk Management System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Environment Agency Board, DEFRA Investment Board, HM Treasury, Met Office |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the strategic case for modernising the national Flood Risk Management System. As a life-safety critical system classified as Critical National Infrastructure, this business case emphasises the human cost of inadequate flood warning alongside financial analysis. It follows the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Modernise the national flood forecasting and warning system to double warning lead times, introduce surface water flood forecasting, provide property-level intelligence to emergency responders, and launch a mobile-first public warning service.

**Problem Statement**: The current system provides approximately 2-hour average flood warning lead time — insufficient for effective evacuation. Surface water flooding (affecting 3 million properties) has no forecasting capability. The 2024 winter floods caused GBP 670M in damages and displaced 12,000 households, with 35% of flooded residents receiving no warning at all.

**Proposed Solution**: A modernised forecasting and warning platform integrating high-density gauge networks, Met Office ensemble rainfall forecasts, 2D rapid inundation mapping, surface water flood modelling, and multi-channel public warning dissemination including a mobile app.

**Strategic Fit**: Delivers the Environment Agency's statutory duties under the Flood and Water Management Act 2010 and Civil Contingencies Act 2004. Aligned with the National Flood and Coastal Erosion Risk Management Strategy and the UK Climate Change Adaptation Programme.

**Investment Required**: GBP 25M over 3 years

- Capital: GBP 18M
- Operational (3 years): GBP 7M

**Expected Benefits**: GBP 145M over 5 years

- Avoided flood damage: GBP 100M
- Avoided emergency response costs: GBP 15M
- Avoided health and social costs: GBP 20M
- Insurance industry benefits: GBP 10M

**Return on Investment**:

- NPV: GBP 98.7M (discounted at 3.5%)
- Payback Period: 14 months
- ROI: 480%

**Recommended Option**: Option 2: Integrated Forecasting and Warning Platform

**Key Risks**:

1. Joint EA/Met Office governance complexity for coupled forecasting system
2. Computational constraints for real-time ensemble hydrological modelling
3. Low mobile app adoption among at-risk populations (elderly, digitally excluded)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: Flood warning is a statutory life-safety duty. Every additional hour of warning lead time prevents an estimated GBP 50M in annual flood damage nationally. The system pays for itself within 14 months. The human cost of inaction — measured in lives lost and communities devastated — makes this investment imperative.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The EA's National Flood Forecasting System (NFFS) was last significantly upgraded in 2010. It provides approximately 2-hour average warning lead time for fluvial flooding and has no surface water flood forecasting capability. The gauge telemetry system operates on ageing infrastructure with single communication pathways. The Flood Warning Direct notification service reaches only 33% of at-risk properties.

**Specific Pain Points** (from Stakeholder Analysis ARC-002-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| EA Exec Dir FCRM | SD-1 | 2-hour warning lead time | GBP 670M flood damage (2024), 12 lives lost in 5 years | CRITICAL |
| Met Office | SD-2 | Loosely coupled met/hydro models | Cannot exploit ensemble probabilistic forecasting | HIGH |
| LLFAs (152) | SD-3 | No surface water flood forecasting | 3M properties at risk with zero warning capability | HIGH |
| Cat 1 Responders | SD-4 | Area-based warnings lack operational detail | Inefficient resource deployment, delayed evacuations | HIGH |
| Citizens | SD-5 | 35% of flooded residents received no warning | Loss of life, uninsured losses, mental health trauma | CRITICAL |

**Consequences of Inaction**:

- Climate change will increase flood frequency 30-60% by 2080 — current system will become progressively inadequate
- Average annual flood damage of GBP 1.1B will increase to GBP 1.5-2.0B without improved warning
- Loss of life: approximately 12 flood-related deaths per 5 years — potentially reducible by 50% with better warnings
- Surface water flooding will remain entirely without forecasting or warning
- Emergency responders will continue making decisions without property-level intelligence

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **Flood and Water Management Act 2010**: EA statutory duty to warn and inform about flood risk
- **Civil Contingencies Act 2004**: Category 1 Responder duty to warn and advise the public
- **National Flood and Coastal Erosion Risk Management Strategy**: "Better prepare our communities" and "Make better use of data"
- **UK Climate Change Adaptation Programme**: "Reduce the risk from flooding"
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 2 (IoT Sensor Reliability), 3 (Real-Time Ingestion), 14 (Availability — 99.99%), 16 (Accessibility)

### A1.3 Why Now?

**Urgency Factors**:

- Climate change is accelerating: 2024 was the wettest year on record for much of England
- Current NFFS infrastructure reaching end-of-life — vendor support ending 2028
- Met Office Unified Model upgrade (2027) creates opportunity for coupled hydrometeorological forecasting
- 2024 floods created political momentum and public expectation for improved warnings

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Warning lead time**: Achieve 4-hour average for fluvial flooding
   - **Measure**: Automated post-event analysis comparing warning issue time to flood threshold exceedance
   - **Threshold**: Minimum 3 hours (target 4 hours)

2. **System availability during severe weather**: 99.99% during Met Office Amber/Red warnings
   - **Measure**: Automated availability monitoring
   - **Threshold**: Zero unplanned outages during Amber/Red warnings

3. **Warning reach**: Push notification delivery to >70% of at-risk properties
   - **Measure**: Notification delivery analytics + post-event surveys
   - **Threshold**: 50% minimum (target 70%)

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue operating the current NFFS until vendor support ends in 2028, then face emergency replacement.

**Costs** (5-year):
- Operational: GBP 35M (current system maintenance escalating as support ends)
- Emergency replacement costs: GBP 30M+ (rushed procurement with no competitive tension)
- Total: GBP 65M

**Benefits**: GBP 0 (no improvement; degradation as system ages)

**Consequences**:
- Continued GBP 1.1B annual flood damage without improved warnings
- Vendor support ending 2028 creates cliff-edge operational risk
- No surface water flood warning capability
- Potential loss of life that improved warnings could prevent

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable risk to life and statutory duty failure.

---

### Option 1: NFFS Incremental Upgrade

**Description**: Upgrade existing NFFS with improved gauge telemetry and enhanced warning dissemination. No fundamental modelling change, no surface water capability, no mobile app.

**Costs** (3-year) — ROM (+/-40%):
- Capital: GBP 8M
- Operational: GBP 4M
- Total: GBP 12M

**Benefits** (5-year): GBP 40M
- Marginal warning lead time improvement: +30 minutes (not transformative)
- Improved gauge reliability: fewer data gaps during floods

**Stakeholder Goals Met**: 30%

**Recommendation**: **Reject** — Insufficient improvement in warning lead time. Does not address surface water flooding gap or mobile warning reach.

---

### Option 2: Integrated Forecasting and Warning Platform (RECOMMENDED)

**Description**: New cloud-hosted platform with coupled hydrometeorological forecasting (joint EA/Met Office), high-density gauge network, surface water flood modelling, rapid inundation mapping, and multi-channel warning dissemination including mobile app.

**Costs** (3-year) — ROM (+/-30%):
- Capital: GBP 18M
  - Forecasting engine (coupled hydrometeorological): GBP 6M
  - Gauge telemetry modernisation: GBP 4M
  - Surface water flood modelling: GBP 3M
  - Rapid inundation mapping: GBP 2M
  - Mobile app and warning dissemination: GBP 2M
  - Security (CNI controls): GBP 1M
- Operational: GBP 7M over 3 years
  - Cloud hosting (multi-region, UK sovereign): GBP 1.5M/year
  - Met Office data and model integration: GBP 0.5M/year
  - Support, maintenance, and on-call: GBP 0.3M/year
- Total 3-year TCO: GBP 25M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Avoided flood damage (better warnings) | ECONOMIC | GBP 10M | GBP 20M | GBP 20M | GBP 25M | GBP 25M | GBP 100M |
| B-002 | Avoided emergency response costs | ECONOMIC | GBP 1M | GBP 3M | GBP 3M | GBP 4M | GBP 4M | GBP 15M |
| B-003 | Avoided health/social costs | SOCIAL | GBP 2M | GBP 4M | GBP 4M | GBP 5M | GBP 5M | GBP 20M |
| B-004 | Insurance industry benefit | FINANCIAL | GBP 1M | GBP 2M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 10M |
| **Total** | | | **GBP 14M** | **GBP 29M** | **GBP 29M** | **GBP 36.5M** | **GBP 36.5M** | **GBP 145M** |

**Net Present Value** (3.5% discount rate):
- Total Benefits PV: GBP 123.7M
- Total Costs PV: GBP 25M
- **NPV: GBP 98.7M**

**Return on Investment**:
- **ROI: 480%** over 5 years
- **Payback Period: 14 months**

**Pros**:
- Doubles warning lead time (2 hours -> 4 hours)
- Introduces surface water flood forecasting for 3 million additional properties
- NPV of GBP 98.7M — overwhelming value for money
- Mobile app reaches citizens not registered for Flood Warning Direct
- 85% of stakeholder goals met

**Cons**:
- GBP 25M investment required
- Joint EA/Met Office governance adds organisational complexity
- Computational requirements for ensemble forecasting are significant

**Stakeholder Goals Met**: 85%

---

### Option 3: National Flood Resilience Centre of Excellence

**Description**: State-of-the-art facility with AI-powered forecasting, nationwide 2D hydraulic models, citizen-level personalised risk assessments, and integration with smart city infrastructure.

**Costs** (3-year): GBP 45M
**Benefits** (5-year): GBP 170M

**NPV**: GBP 89.5M (lower than Option 2 due to higher costs)

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Higher cost with diminishing returns. AI flood prediction maturity insufficient for operational deployment. Misses winter 2027-28 deadline.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Integrated Forecasting and Warning Platform**

**Rationale**:
1. **Highest NPV**: GBP 98.7M — overwhelmingly positive value for money
2. **Life-safety impact**: Potentially preventing 50% of flood-related deaths through earlier warnings
3. **Statutory compliance**: Delivers EA's flood warning duty to modern standards
4. **Deliverability**: Achievable for winter 2027-28 flood season
5. **Surface water gap**: Addresses the most significant gap in current capability

**Optimism Bias Adjustment** (HM Treasury Green Book):
- Standard uplift: +40% on costs
- Adjusted Total Cost: GBP 25M -> GBP 35M
- NPV with optimism bias: GBP 88.7M (still overwhelmingly positive)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for platform development. Direct partnership with Met Office for forecasting integration (Crown body collaboration, no procurement required).

**Contract Approach**:
- **Build**: Time-and-materials with agile delivery (fixed budget, flexible scope)
- **Run**: Managed service with SLA-linked payments reflecting life-safety criticality
- **Met Office**: Memorandum of Understanding for joint forecasting system

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: GBP 25M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 10M | GBP 6M | GBP 2M | GBP 18M |
| OpEx | GBP 2.3M | GBP 2.3M | GBP 2.4M | GBP 7M |
| **Total** | **GBP 12.3M** | **GBP 8.3M** | **GBP 4.4M** | **GBP 25M** |

## D2. Funding Source

**Source**: EA Flood and Coastal Erosion Risk Management Grant-in-Aid (DEFRA allocation)
**Amount Available**: GBP 30M allocated in Spending Review 2025 for flood warning modernisation
**Assessment**: **Affordable** within allocated settlement

## D3. Financial Appraisal

**Value for Money Assessment**: **HIGH**

- Economy: competitive procurement, cloud-based reducing infrastructure costs
- Efficiency: automation reducing manual forecasting effort by 40%
- Effectiveness: doubles warning lead time, addressing the most impactful capability gap

**Benefit-Cost Ratio**: 5.8:1 (GBP 145M benefits / GBP 25M costs)

This is among the highest BCRs for flood risk management interventions, comparable to physical flood defences protecting high-value urban areas.

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: EA Executive Director of Flood and Coastal Risk Management
**Joint Governance**: EA/Met Office Flood Forecasting Centre Board for forecasting components

## E2. Key Milestones

| Milestone | Date |
|-----------|------|
| SOBC Approval | Q2 2026 |
| Procurement Award | Q3 2026 |
| Alpha (forecasting engine) | Q4 2026 |
| Beta Assessment (GDS) | Q2 2027 |
| Gauge network modernisation complete | Q3 2027 |
| **Winter 2027-28 Go-Live** | **October 2027** |
| Surface water forecasting for LLFAs | March 2028 |
| Mobile app launch | Q4 2027 |
| Benefits Review (Year 1) | October 2028 |

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | EA/Met Office governance disagreement delays decisions | Medium | High | 12 | Joint Programme Board with escalation to EA/Met Office CEOs |
| R-002 | Ensemble forecasting computational constraints | Medium | High | 12 | Cloud-based HPC, progressive model complexity increase |
| R-003 | Low mobile app adoption among elderly/digitally excluded | High | Medium | 12 | Multi-channel approach (voice call, SMS, community wardens) |
| R-004 | October 2027 deadline missed | Low | Critical | 9 | MVP scoping, early procurement, phased delivery |
| R-005 | Gauge network modernisation delayed by supply chain | Medium | Medium | 9 | Early procurement, strategic stock, temporary solutions |

---

# PART F: RECOMMENDATION & NEXT STEPS

**Recommended Option**: **Option 2: Integrated Forecasting and Warning Platform**
**Investment**: GBP 25M over 3 years
**Expected Return**: GBP 145M over 5 years (NPV: GBP 98.7M, ROI: 480%, BCR: 5.8:1)
**Go/No-Go**: **PROCEED**

**Next Steps**:
1. EA Board approval — Target: Q2 2026
2. Met Office MoU for joint forecasting — Target: Q2 2026
3. DOS6 procurement for platform development — Target: Q3 2026
4. Alpha development — Target: Q4 2026
5. Operational for winter 2027-28 flood season — Target: October 2027

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO / EA Exec Dir FCRM | | |
| | EA Finance Director | | |
| | EA DDaT Director | | |
| | DEFRA Flood Policy Director | | |
| | Met Office Chief Scientist | | |

**Approval Decision**: PENDING

---

**Generated by**: ArcKit `/arckit:sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Flood Risk Management System (Project 002)
**AI Model**: Claude Opus 4.6 (1M context)
