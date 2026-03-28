# Strategic Outline Business Case (SOBC): Water Quality Monitoring Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Water Quality Monitoring Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Quality Monitoring Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Investment Board, HM Treasury, Environment Agency, Ofwat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the strategic case for investing in a national Water Quality Monitoring Platform. It follows the HM Treasury Green Book five-case model and provides the evidence base for DEFRA Investment Board approval to proceed to the Outline Business Case (OBC) stage.

---

## Executive Summary

**Purpose**: Deliver a national platform that aggregates real-time water quality monitoring data across England's waterways, supporting regulatory enforcement, public transparency, and Water Framework Directive compliance.

**Problem Statement**: Water quality data is fragmented across multiple EA databases, water company systems, and third-party sources. No unified real-time view exists, undermining regulatory enforcement (62% prosecution success rate), public trust (34% trust water company data), and the UK's ability to demonstrate Environment Act 2021 compliance.

**Proposed Solution**: A cloud-hosted platform integrating IoT sensor networks, water company telemetry, and EA laboratory data into a single, authoritative, publicly accessible water quality service with real-time dashboards, open APIs, and automated WFD classification.

**Strategic Fit**: Directly delivers the Environment Act 2021 monitoring commitments, the Storm Overflow Discharge Reduction Plan, the 25 Year Environment Plan clean water objectives, and GDS Service Standard compliance.

**Investment Required**: GBP 18M over 3 years

- Capital: GBP 12M
- Operational (3 years): GBP 6M

**Expected Benefits**: GBP 47M over 5 years

- Public health improvement (reduced waterborne illness): GBP 10M
- EA enforcement efficiency gains: GBP 8M
- Water company assurance cost reduction: GBP 12M
- Economic benefit from improved bathing water confidence: GBP 17M

**Return on Investment**:

- NPV: GBP 22.3M (discounted at 3.5%)
- Payback Period: 28 months
- ROI: 161%

**Recommended Option**: Option 2: Balanced Platform Approach

**Key Risks**:

1. Water company non-cooperation with data integration requirements
2. IoT sensor reliability in harsh marine and riverine environments
3. Public backlash from publication of preliminary unvalidated data

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Environment Act 2021 creates statutory obligations for water quality monitoring that cannot be met with current fragmented systems. The platform delivers a positive NPV of GBP 22.3M, meets 85% of stakeholder goals, and is essential for UK environmental governance credibility.

**Next Steps if Approved**:

1. Secure GBP 18M funding approval from DEFRA Investment Board: Q2 2026
2. Define detailed requirements: `/arckit:requirements` (ARC-001-REQ-v1.0 complete)
3. Procurement via Digital Marketplace (G-Cloud/DOS): Q3 2026
4. Platform operational for 2027 bathing season: May 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
England's water quality monitoring infrastructure is fragmented, outdated, and inadequate for modern environmental governance. The EA's Water Information Management System (WIMS) stores historical laboratory results but has no real-time sensor integration. Water companies operate independent monitoring systems with inconsistent data standards. The public has no single, authoritative source for water quality information.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DEFRA Secretary of State | SD-1 | No visible action platform on sewage crisis | Sustained Parliamentary criticism, media pressure | CRITICAL |
| EA Director of Water Quality | SD-2 | Periodic sampling misses pollution events | 62% prosecution rate, 18-month investigations | CRITICAL |
| Water Companies | SD-3 | Inconsistent monitoring standards, high assurance costs | GBP 40M/year assurance, regulatory uncertainty | HIGH |
| Ofwat | SD-4 | Reliance on self-reported performance data | Weak evidence base for price reviews | HIGH |
| Campaign Groups | SD-5 | No real-time public access to water quality data | Public trust at 34%, campaign pressure | HIGH |

**Consequences of Inaction**:

- Continued inability to demonstrate Environment Act 2021 compliance — judicial review risk estimated at HIGH
- Prosecution success rate remains at 62%, allowing polluters to escape accountability
- Public trust in water quality governance continues to decline below 34%
- GBP 40M annual assurance cost continues with no efficiency improvement
- UK fails to meet retained WFD reporting obligations, risking international credibility

### A1.2 Strategic Drivers

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | DEFRA Sec of State | POLITICAL | Visible action on water quality crisis | Environment Act delivery |
| SD-2 | EA Director | OPERATIONAL | Evidence-quality monitoring for enforcement | Regulatory effectiveness |
| SD-3 | Water Companies | FINANCIAL | Cost-effective standardised compliance | Industry efficiency |
| SD-5 | Campaign Groups | STRATEGIC | Public transparency and accountability | Democratic accountability |

**Strategic Alignment**:

- **Environment Act 2021**: Directly delivers Section 82 (storm overflow monitoring) and Section 81 (water company reporting) requirements
- **Storm Overflow Discharge Reduction Plan**: Provides the monitoring infrastructure to track legally binding reduction targets
- **25 Year Environment Plan**: "Goal 3: Clean and plentiful water" — continuous monitoring of all water bodies
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Environmental Data Integrity), 2 (IoT Sensor Reliability), 3 (Real-Time Ingestion), 8 (Open Data)

### A1.3 Scope

**In Scope**:
- IoT sensor network management (bathing waters, storm overflows)
- Water company data integration (EDMs, SCADA feeds)
- EA laboratory data integration (WIMS)
- Real-time public dashboards
- Open data API service
- WFD classification automation

**Out of Scope**:
- Physical sensor procurement and deployment (separate EA programme)
- Water company SCADA upgrades (company responsibility)
- Flood monitoring (Project 002)
- Drinking water quality (DWI remit)

### A1.4 Why Now?

**Urgency Factors**:

- Environment Act 2021 deadlines: continuous storm overflow monitoring required from 2025 onwards
- Storm Overflow Discharge Reduction Plan: progress tracking required from 2027
- 2027 bathing season: Ministerial commitment to real-time bathing water quality data
- Public pressure: sewage discharge crisis maintaining media and Parliamentary attention at highest levels

**Opportunity Cost of Delay**:

- GBP 3M/month in continued inefficient manual monitoring (EA cost)
- Each year of delay = one fewer year of continuous monitoring data for WFD trend analysis
- Political window for investment may close as media attention shifts

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Real-time data availability**: Water quality data from all designated bathing waters published within 15 minutes
   - **Measure**: Data latency monitoring
   - **Threshold**: 95% of readings within SLA

2. **Data quality and trust**: Published data is accurate, contextualised, and trusted by all stakeholders
   - **Measure**: Data quality score, stakeholder satisfaction survey
   - **Threshold**: >95% quality pass rate, >60% stakeholder trust

3. **Regulatory effectiveness**: Platform data supports successful enforcement actions
   - **Measure**: Prosecution success rate, investigation time
   - **Threshold**: >80% prosecution rate, <12 months investigation time

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current fragmented monitoring — EA WIMS database, periodic manual sampling, water company self-reporting.

**Costs** (3-year):
- Capital: GBP 0
- Operational: GBP 45M (continued EA monitoring + water company assurance costs)
- Total: GBP 45M

**Benefits**: GBP 0 (no improvement)

**Cons**:
- Environment Act 2021 compliance cannot be demonstrated
- Judicial review risk from environmental NGOs
- Prosecution success rate remains at 62%
- Public trust continues to decline
- GBP 40M annual assurance cost continues

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Fails to meet statutory obligations under the Environment Act 2021.

---

### Option 1: Minimal Enhancement — EA System Upgrade

**Description**: Upgrade EA's existing WIMS database to accept real-time sensor data from bathing waters only. No water company integration, no public dashboard, no open data API.

**Scope**:
- WIMS upgrade for real-time data ingestion
- Bathing water sensor integration (424 sites)
- Internal EA operational dashboard

**Costs** (3-year) — ROM (+/-40%):
- Capital: GBP 5M
- Operational: GBP 3M
- Total: GBP 8M

**Benefits** (3-year): GBP 6M
- EA monitoring efficiency: GBP 4M
- Partial prosecution improvement: GBP 2M

**Net Benefit**: GBP -2M (costs exceed benefits)

**Pros**:
- Lower upfront investment
- Uses existing EA infrastructure
- Lower implementation risk

**Cons**:
- Does not integrate water company data — Environment Act compliance gap
- No public dashboard — Ministerial commitment not met
- No open data — EIR compliance gap
- Does not address storm overflow monitoring requirement

**Stakeholder Goals Met**: 25%

**Recommendation**: **Reject** — Fails to meet Environment Act requirements and Ministerial commitments.

---

### Option 2: Balanced Platform Approach (RECOMMENDED)

**Description**: Cloud-hosted national platform integrating IoT sensors, water company telemetry, and EA data. Public dashboards for bathing water and storm overflow status. Open data API. Automated WFD classification.

**Scope**:
- Platform for data ingestion from all sources (sensors, water companies, EA labs)
- Real-time public dashboards (bathing water, storm overflows)
- Open data API with bulk download
- WFD classification automation
- Integration with DEFRA Data Services Platform

**Costs** (3-year) — ROM (+/-30%):
- Capital: GBP 12M
  - Platform development and integration: GBP 6M
  - Data ingestion infrastructure: GBP 3M
  - Public dashboard and API development: GBP 2M
  - Security (CNI controls, pen testing): GBP 1M
- Operational: GBP 6M over 3 years
  - Cloud hosting (UK sovereign): GBP 1.2M/year
  - Support and maintenance: GBP 0.5M/year
  - Data quality assurance team (3 FTE): GBP 0.3M/year
- Total 3-year TCO: GBP 18M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Source | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|---------------------|--------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Public health improvement | G-1 | SOCIAL | GBP 0.5M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 2.5M | GBP 10M |
| B-002 | EA enforcement efficiency | G-2, G-3 | OPERATIONAL | GBP 0.5M | GBP 2M | GBP 2M | GBP 1.75M | GBP 1.75M | GBP 8M |
| B-003 | Assurance cost reduction | G-2 | FINANCIAL | GBP 0 | GBP 2.4M | GBP 2.4M | GBP 3.6M | GBP 3.6M | GBP 12M |
| B-004 | Beach tourism economic benefit | G-1, G-4 | ECONOMIC | GBP 1M | GBP 3M | GBP 4M | GBP 4.5M | GBP 4.5M | GBP 17M |
| **Total** | | | | **GBP 2M** | **GBP 9.4M** | **GBP 10.9M** | **GBP 12.35M** | **GBP 12.35M** | **GBP 47M** |

**Net Present Value** (3.5% discount rate):
- Total Benefits PV: GBP 40.3M
- Total Costs PV: GBP 18M
- **NPV: GBP 22.3M**

**Return on Investment**:
- **ROI: 161%** over 5 years
- **Payback Period: 28 months**

**Pros**:
- Meets Environment Act 2021 requirements
- Delivers Ministerial commitment for real-time bathing water data
- Positive NPV of GBP 22.3M
- 85% of stakeholder goals met
- Open data commitment delivers public transparency

**Cons**:
- GBP 18M investment required
- Water company integration complexity
- IoT sensor reliability risk in harsh environments

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive National Water Quality Observatory

**Description**: Full national water quality observatory with AI-powered predictive modelling, citizen science integration, international data exchange, and real-time ecological impact assessment.

**Costs** (3-year) — ROM (+/-40%):
- Capital: GBP 25M
- Operational: GBP 12M
- Total: GBP 37M

**Benefits** (5-year): GBP 55M

**Net Benefit**: GBP 18M (lower NPV than Option 2 due to higher costs with diminishing returns)

**Pros**:
- 100% stakeholder goals met
- World-leading capability
- AI-powered predictive pollution modelling

**Cons**:
- GBP 37M investment — may exceed DEFRA budget envelope
- 24-month implementation (misses 2027 bathing season commitment)
- AI/ML maturity risk for environmental predictions

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Diminishing returns, misses bathing season deadline, exceeds budget.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Balanced Platform Approach**

**Rationale**:
1. **Best Value**: Highest NPV at GBP 22.3M with 161% ROI
2. **Compliance**: Meets Environment Act 2021 statutory requirements
3. **Deliverability**: Achievable within 2027 bathing season Ministerial deadline
4. **Affordability**: GBP 18M within DEFRA budget envelope
5. **Stakeholder Satisfaction**: 85% of goals met

**Optimism Bias Adjustment** (HM Treasury Green Book):
- Standard uplift for IT projects: +40% on costs
- Adjusted Total Cost: GBP 18M -> GBP 25.2M (with uplift)
- NPV with optimism bias: GBP 15.1M (still positive)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: Mature — environmental data platforms, IoT telemetry solutions, and open data services are well-established technology categories with multiple UK Government-experienced suppliers.

**UK Government Digital Marketplace Assessment**:
- **G-Cloud 14**: 45+ suppliers offering environmental monitoring platforms and IoT data services
- **DOS6**: 30+ suppliers for environmental data specialists
- **SME participation**: 60%+ of relevant suppliers are SMEs

### C1.2 Sourcing Route

**Recommended Route**: Digital Marketplace — DOS6 for platform development, G-Cloud for cloud hosting

**Rationale**: Compliant with Cabinet Office procurement policy, competitive market, SME access, rapid procurement timeline.

### C1.3 Contract Approach

- **Build**: Fixed-price with milestones (18-month implementation)
- **Run**: Managed service (3-year initial, 2+2 extensions)
- **IP**: Crown owns all bespoke development

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: GBP 18M over 3 years

### D1.1 Capital Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 4M | GBP 2M | GBP 0 | GBP 6M |
| Data ingestion infrastructure | GBP 2M | GBP 1M | GBP 0 | GBP 3M |
| Public dashboard & API | GBP 1.5M | GBP 0.5M | GBP 0 | GBP 2M |
| Security (CNI controls) | GBP 0.7M | GBP 0.3M | GBP 0 | GBP 1M |
| **Total CapEx** | **GBP 8.2M** | **GBP 3.8M** | **GBP 0** | **GBP 12M** |

### D1.2 Operational Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Cloud hosting (UK sovereign) | GBP 1.2M | GBP 1.2M | GBP 1.2M | GBP 3.6M |
| Support and maintenance | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| Data quality team (3 FTE) | GBP 0.3M | GBP 0.3M | GBP 0.3M | GBP 0.9M |
| **Total OpEx** | **GBP 2M** | **GBP 2M** | **GBP 2M** | **GBP 6M** |

### D1.3 Total Cost of Ownership

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 8.2M | GBP 3.8M | GBP 0 | GBP 12M |
| OpEx | GBP 2M | GBP 2M | GBP 2M | GBP 6M |
| **Total** | **GBP 10.2M** | **GBP 5.8M** | **GBP 2M** | **GBP 18M** |

## D2. Funding Source

**Source**: DEFRA Environmental Improvement Programme budget (Spending Review 2025 settlement)
**Amount Available**: GBP 20M allocated for water quality digital infrastructure
**Approval Path**: DEFRA Investment Board (up to GBP 20M), HM Treasury notification

## D3. Affordability

- Total IT budget (DEFRA): GBP 280M/year
- This project: 3.6% of annual IT budget (Year 1)
- Assessment: **Affordable** within existing settlement

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: DEFRA Water Quality Policy Director
**Steering Committee**: DEFRA CDIO, EA Director of Water Quality, Ofwat Digital Director, DEFRA Finance Director

### E1.1 Approval Gates

| Gate | Criteria | Approving Body | Timing |
|------|----------|----------------|--------|
| Gate 0: SOBC Approval | Business case approved | DEFRA Investment Board | Q2 2026 |
| Gate 1: Requirements Approved | Stakeholders signed off | SRO | Q2 2026 |
| Gate 2: Procurement Award | Vendor selected | SRO + Commercial | Q3 2026 |
| Gate 3: Beta Assessment | GDS Beta assessment passed | GDS + SRO | Q1 2027 |
| Gate 4: Go-Live (Bathing Season) | UAT passed, operational readiness | Steering Committee | May 2027 |
| Gate 5: Benefits Realisation | 12-month benefits review | Steering Committee | May 2028 |

## E2. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|--------------|
| SOBC Approval | June 2026 | This document |
| Requirements Complete | June 2026 | ARC-001-REQ-v1.0 |
| Procurement Award | September 2026 | SOBC approval |
| Alpha | December 2026 | Vendor onboarded |
| Beta Assessment (GDS) | March 2027 | Alpha complete |
| **Bathing Season Go-Live** | **May 2027** | Beta assessment passed |
| Storm Overflow Integration | December 2027 | Water company onboarding |
| Benefits Review | May 2028 | 12 months post-live |

## E3. Risk Management

### Top 5 Strategic Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation |
|---------|------------------|------------|--------|-------|------------|
| R-001 | Water company non-cooperation | Medium | High | 12 | Environment Act powers, Ofwat licence conditions |
| R-002 | IoT sensor reliability in harsh environments | Medium | High | 12 | Redundant sensors, store-and-forward, maintenance SLA |
| R-003 | Public backlash from preliminary data | Medium | Medium | 9 | Data quality flagging, contextual information, comms strategy |
| R-004 | 2027 bathing season deadline missed | Low | Critical | 9 | Phased delivery, early procurement, MVP scope definition |
| R-005 | CNI cyber security incident | Low | Critical | 9 | NCSC consultation, pen testing, dedicated SOC |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: **Option 2: Balanced Platform Approach**
**Investment**: GBP 18M over 3 years
**Expected Return**: GBP 47M over 5 years (NPV: GBP 22.3M, ROI: 161%)
**Stakeholder Goals Met**: 85%
**Payback Period**: 28 months
**Go/No-Go Recommendation**: **PROCEED to requirements and procurement phase**

## F2. Next Steps if Approved

1. **Funding Approval**: DEFRA Investment Board confirms GBP 18M allocation — Target: June 2026
2. **Team Mobilisation**: SRO appoints Programme Manager and core team — Target: June 2026
3. **Procurement**: DOS6 competition for platform development — Target: September 2026
4. **Alpha/Beta**: Iterative build targeting bathing season go-live — Target: May 2027
5. **Storm Overflow Phase**: Water company integration — Target: December 2027
6. **Benefits Review**: 12-month post-live assessment — Target: May 2028

---

## Appendix A: Stakeholder Analysis

**Source**: `projects/001-water-quality-monitoring-platform/ARC-001-STKE-v1.0.md`

## Appendix B: Architecture Principles

**Source**: `projects/000-global/ARC-000-PRIN-v1.0.md`

## Appendix H: Glossary

| Term | Definition |
|------|------------|
| SOBC | Strategic Outline Business Case |
| NPV | Net Present Value |
| EDM | Event Duration Monitor |
| WIMS | Water Information Management System |
| WFD | Water Framework Directive |
| CNI | Critical National Infrastructure |
| EIR | Environmental Information Regulations |

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO / DEFRA Water Quality Policy Director | | |
| | DEFRA Finance Director | | |
| | DEFRA CDIO | | |
| | EA Director of Water Quality | | |

**Approval Decision**: PENDING

---

**Generated by**: ArcKit `/arckit:sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Quality Monitoring Platform (Project 001)
**AI Model**: Claude Opus 4.6 (1M context)
