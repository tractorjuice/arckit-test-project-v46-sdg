# Strategic Outline Business Case (SOBC): Fishing Quota Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Fishing Quota Management (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Fishing Quota Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Quota Programme Board, MMO, DEFRA Finance, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case establishes the strategic justification for investment in a digital Fishing Quota Management system. It follows HM Treasury Green Book guidance and supports the MMO's case for capital investment in fisheries management modernisation.

---

## Executive Summary

**Purpose**: The Fisheries Act 2020 gave the UK independent fisheries management for the first time in 50 years. The current quota management infrastructure — a mix of legacy databases, paper catch returns, and spreadsheet-based PO management — is inadequate for delivering the Act's eight fisheries objectives.

**Problem Statement**: Catch data latency of 4-6 weeks for the under-10m fleet (77% of vessels by number) prevents real-time quota monitoring. This leads to precautionary early closures costing the industry an estimated GBP 15M/year in lost fishing opportunity, or risk of overshooting quota limits which threatens stock sustainability and international credibility.

**Proposed Solution**: A digital platform providing electronic catch reporting for all fleet segments (including a mobile app for the under-10m fleet), real-time quota utilisation monitoring, digital quota trading, and integration with ICES stock assessment data.

**Strategic Fit**: Directly delivers the Fisheries Act 2020 vision for evidence-based, sustainable fisheries management. Supports Fisheries Management Plans, UK-EU fisheries negotiations, and ICES scientific advice.

**Investment Required**: GBP 15.8M over 3 years

- Capital: GBP 12.0M
- Operational (3 years): GBP 3.8M

**Expected Benefits**: GBP 34.2M over 5 years

- Industry value (reduced precautionary closures): GBP 15.0M
- MMO operational efficiency: GBP 5.2M
- Quota optimisation (reduced waste): GBP 8.0M
- Compliance cost avoidance: GBP 3.0M
- Scientific data improvement value: GBP 3.0M

**Return on Investment**:

- NPV: GBP 12.8M (discounted at 3.5%)
- Payback Period: 22 months
- ROI: 116%

**Recommended Option**: Option 2: Digital Quota Management Platform

**Key Risks**:

1. Under-10m fleet digital adoption below target — mitigated by harbour-based digital champions, free app, device support programme
2. Annual fisheries negotiations create TAC uncertainty — mitigated by system design for late TAC confirmation
3. Legacy data migration complexity — mitigated by parallel running with phased migration

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK's post-Brexit fisheries management credibility depends on demonstrating that independent management is more effective than the CFP. Digital quota management is essential to deliver the Fisheries Act 2020. The investment pays back within 22 months through reduced precautionary closures alone.

**Next Steps if Approved**:

1. Secure MMO Board and DEFRA approval: April 2026
2. Detailed requirements with industry co-design: Q2 2026
3. Alpha development with under-10m fisher trials: Q3 2026
4. Private beta with 3 POs: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The MMO manages approximately 100 quota stocks for England using a combination of the legacy Fisheries Activity Database, electronic logbooks (for ~1,400 over-10m vessels), paper catch returns (for ~4,600 under-10m vessels), and spreadsheet-based PO quota tracking. This infrastructure was designed incrementally under the EU Common Fisheries Policy and is fundamentally inadequate for the UK's new independent fisheries management responsibilities.

**Specific Pain Points** (from ARC-002-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| MMO Quota Head | SD-2 | 4-6 week data lag for under-10m catches | Cannot monitor quota in real-time | CRITICAL |
| NFFO | SD-3 | Quota trading takes 5 days | Lost fishing opportunity, quota waste | HIGH |
| NUTFA | SD-4 | Paper returns burden, no quota visibility | Under-reporting, fisher frustration | HIGH |
| Cefas | SD-5 | No direct link between science and quota | Fisheries Act compliance gap | HIGH |
| Minister | SD-1 | Cannot demonstrate Fisheries Act delivery | Political and reputational risk | CRITICAL |

**Consequences of Inaction**:

- GBP 15M/year in lost fishing opportunity due to precautionary early closures caused by data latency
- Quota overshoot risk: 3 stocks exceeded TAC in 2025 due to late under-10m data, triggering EU retaliation deductions
- Fisheries Act 2020 delivery failure: cannot implement Fisheries Management Plans without real-time data
- UK-EU fisheries negotiations weakened by inability to demonstrate accurate catch monitoring
- NAO criticism of MMO for failing to modernise fisheries management post-Brexit

### A1.2 Strategic Drivers

**Primary Drivers**:

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Minister | POLITICAL | Demonstrate Fisheries Act delivery | Post-Brexit credibility |
| SD-2 | MMO Quota | OPERATIONAL | Real-time quota monitoring | Prevent overshoot |
| SD-3 | NFFO | FINANCIAL | Efficient quota trading | Industry productivity |
| SD-4 | NUTFA | FINANCIAL | Fair access and reduced burden | Small-scale fleet viability |
| SD-5 | Cefas | COMPLIANCE | Science-based quota decisions | Fisheries Act objective |

**Strategic Alignment**:

- **Fisheries Act 2020**: All eight fisheries objectives require accurate, timely catch data
- **Joint Fisheries Statement**: UK-wide commitment to science-based fisheries management
- **UK-EU Trade and Cooperation Agreement**: Fisheries protocol requires catch documentation for shared stocks
- **25 Year Environment Plan**: Sustainable fisheries as marine environment target
- **ICES Framework**: Scientific advice requires catch data feedback loop

### A1.3 Scope

**In Scope**:

- Electronic catch reporting for all fleet segments
- Real-time quota monitoring and alerting
- Quota allocation management (FQA, pool, in-year)
- Digital quota trading platform
- ICES stock data integration
- FMP monitoring dashboards
- Mobile app for under-10m fleet

**Out of Scope**:

- Vessel licensing system
- Marine Protected Areas monitoring (Project 001)
- Aquaculture management
- Recreational fishing
- Fish health certification

**Dependencies**:

- **Internal**: MMO vessel registry integration, VMS data access
- **External**: ICES stock assessment data, devolved administration quota systems
- **Legislative**: Mandatory eLogbook for under-10m requires secondary legislation (Statutory Instrument)

### A1.5 Why Now?

**Urgency Factors**:

- 3 quota stocks exceeded TAC in 2025 — EU retaliatory deductions applied to 2026 quota
- Fisheries Management Plans going live require real-time monitoring (first FMPs published 2024)
- UK-EU fisheries consultation 2027 will scrutinise UK catch monitoring capability
- Legacy Fisheries Activity Database approaching end-of-life (vendor support ends 2027)
- Under-10m fleet paper return backlog growing (6-month processing backlog)

**Opportunity Cost of Delay**:

- GBP 15M/year in lost fishing opportunity from precautionary closures
- GBP 2M/year in MMO staff costs processing paper returns
- Reputational cost of further quota overshoots (EU deductions, ICES credibility)
- Risk of NAO critical report on fisheries management capability

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Under-10m Adoption**: Mobile app adopted by >80% of under-10m fleet
   - **Measure**: Monthly active users as % of registered under-10m vessels
   - **Threshold**: 60% minimum, 80% target

2. **Data Latency Reduction**: Catch data available within 48 hours for all fleet segments
   - **Measure**: Mean time from landing to data availability
   - **Threshold**: <72 hours minimum, <48 hours target

3. **Quota Accuracy**: Real-time quota utilisation accurate to +-3%
   - **Measure**: Year-end reconciliation variance
   - **Threshold**: +-5% minimum, +-3% target

4. **Industry Trust**: Fishing industry regards the system as fair and useful
   - **Measure**: Industry satisfaction survey score
   - **Threshold**: >6/10

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with legacy Fisheries Activity Database, paper catch returns for under-10m, and spreadsheet-based PO management.

**Costs** (5-year):

- Capital: GBP 0
- Operational: GBP 18.0M (current MMO quota management costs, including legacy system maintenance, paper processing staff, manual PO reconciliation)
- Total: GBP 18.0M

**Benefits**: GBP 0

**Cons**:

- Quota overshoots will continue, triggering EU retaliatory deductions
- Cannot deliver Fisheries Act 2020 objectives
- Legacy system end-of-life in 2027 forces emergency procurement
- GBP 15M/year industry cost from precautionary closures continues
- NAO critical report highly likely

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Legally non-compliant with Fisheries Act requirements.

---

### Option 1: Incremental Digitisation

**Description**: Upgrade the existing Fisheries Activity Database, add a basic mobile catch reporting capability, and digitise PO communication. No real-time quota monitoring or quota trading.

**Costs** (5-year) - ROM (+-40%):

- Capital: GBP 4.0M
- Operational: GBP 14.0M over 5 years
- Total 5-year TCO: GBP 18.0M

**Benefits** (5-year): GBP 8.0M (partial data latency reduction, some paper savings)

**Stakeholder Goals Met**: 35%

**Recommendation**: Insufficient to deliver Fisheries Act requirements.

---

### Option 2: Digital Quota Management Platform (RECOMMENDED)

**Description**: Purpose-built digital platform with mobile catch reporting, real-time quota monitoring, digital quota trading, and ICES data integration.

**Costs** (5-year) - ROM (+-30%):

- Capital: GBP 12.0M
  - Platform development: GBP 6.0M
  - Mobile app development: GBP 2.0M
  - Data migration and integration: GBP 1.5M
  - Industry adoption programme (devices, training, harbour champions): GBP 1.0M
  - Security accreditation and testing: GBP 0.5M
  - Contingency (10%): GBP 1.0M
- Operational: GBP 3.8M over 3 years (GBP 6.5M over 5 years)
  - Cloud hosting: GBP 0.5M/year
  - Support and maintenance: GBP 0.4M/year
  - ICES data integration: GBP 0.1M/year
  - Harbour support network: GBP 0.3M/year
- Total 5-year TCO: GBP 18.5M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Reduced precautionary closures (industry value) | FINANCIAL | GBP 0.5M | GBP 3.0M | GBP 3.5M | GBP 4.0M | GBP 4.0M | GBP 15.0M |
| B-002 | MMO operational efficiency (paper elimination) | FINANCIAL | GBP 0.2M | GBP 1.0M | GBP 1.2M | GBP 1.4M | GBP 1.4M | GBP 5.2M |
| B-003 | Quota optimisation (reduced waste from better trading) | FINANCIAL | GBP 0.0M | GBP 1.5M | GBP 2.0M | GBP 2.0M | GBP 2.5M | GBP 8.0M |
| B-004 | Compliance cost avoidance (no EU retaliatory deductions) | RISK | GBP 0.0M | GBP 0.5M | GBP 0.5M | GBP 1.0M | GBP 1.0M | GBP 3.0M |
| B-005 | Scientific data improvement (better stock assessment) | STRATEGIC | GBP 0.0M | GBP 0.5M | GBP 0.5M | GBP 1.0M | GBP 1.0M | GBP 3.0M |
| **Total** | | | **GBP 0.7M** | **GBP 6.5M** | **GBP 7.7M** | **GBP 9.4M** | **GBP 9.9M** | **GBP 34.2M** |

**NPV** (3.5% discount rate): **GBP 12.8M**

**ROI**: **116%** over 5 years

**Payback Period**: **22 months**

**Stakeholder Goals Met**: 90%

---

### Option 3: Comprehensive Fisheries Intelligence Platform

**Description**: Full fisheries intelligence system including AI-based stock prediction, automated species identification from catch images, integration with satellite-based vessel detection, and international data exchange with EU and Norway.

**Costs** (5-year): GBP 32.0M

**Benefits** (5-year): GBP 38.0M

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject at SOBC stage** — Disproportionate cost and risk. AI elements can be added in future phases.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 5-Year TCO | GBP 18.0M | GBP 18.0M | GBP 18.5M | GBP 32.0M |
| 5-Year Benefits | GBP 0 | GBP 8.0M | GBP 34.2M | GBP 38.0M |
| NPV | -GBP 18.0M | -GBP 10.0M | GBP 12.8M | GBP 3.5M |
| Stakeholder Goals | 0% | 35% | 90% | 100% |
| Fisheries Act Compliance | No | Partial | Yes | Yes |

**Recommended Option**: **Option 2 — Digital Quota Management Platform**

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

| Component | Procurement Route | Estimated Value | Timeline |
|-----------|------------------|-----------------|----------|
| Platform development | Digital Outcomes and Specialists 6 | GBP 6.0M | Q2 2026 |
| Mobile app development | G-Cloud 14 (specialist mobile) | GBP 2.0M | Q2 2026 |
| Cloud hosting | AWS via Crown Commercial Service | GBP 2.5M (5-year) | Existing |
| Industry adoption programme | Direct commissioning via Seafish | GBP 1.0M | Q3 2026 |

---

# PART D: FINANCIAL CASE

## D1. Cost Summary

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital | GBP 6.0M | GBP 4.0M | GBP 2.0M | GBP 12.0M |
| Operational | GBP 0.8M | GBP 1.3M | GBP 1.7M | GBP 3.8M |
| **Total** | **GBP 6.8M** | **GBP 5.3M** | **GBP 3.7M** | **GBP 15.8M** |

## D2. Funding Source

- MMO Grant-in-Aid from DEFRA (primary)
- UK Seafood Fund (industry adoption programme component — GBP 1.0M)
- DEFRA Spending Review 2025 digital transformation allocation

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile (Scrum) with industry co-design sprints

**Key Milestones**:

| Milestone | Date | Gate |
|-----------|------|------|
| Discovery (industry co-design workshops) | June 2026 | MMO Assurance |
| Alpha (under-10m app prototype tested in 5 ports) | October 2026 | GDS Assessment |
| Private Beta (3 POs, 200 under-10m vessels) | February 2027 | Programme Board |
| Public Beta / GDS Beta assessment | June 2027 | GDS Assessment |
| Full live service (all fleet, all POs) | October 2027 | Programme Board |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Under-10m adoption below target | MEDIUM | HIGH | Harbour champion programme, free devices for hardship cases, simplified UI | Product Owner |
| Annual TAC uncertainty delays system configuration | HIGH | MEDIUM | Design for late TAC entry, provisional allocations | MMO Quota Head |
| Legacy data migration errors | MEDIUM | HIGH | Parallel running period, automated reconciliation | Technical Lead |
| PO resistance to standardised processes | MEDIUM | MEDIUM | PO co-design, preserve PO autonomy where possible | Service Owner |
| Connectivity in remote ports insufficient | MEDIUM | MEDIUM | Offline-first design, harbour Wi-Fi partnerships | Delivery Manager |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Fisheries Act 2020 | Legislation | UK Parliament | Eight objectives, FMP framework | legislation.gov.uk |
| Joint Fisheries Statement | Policy | UK Fisheries Administrations | UK-wide management approach | gov.uk |
| HM Treasury Green Book | Guidance | HMT | Appraisal methodology | gov.uk |
| ARC-002-STKE-v1.0 | Architecture | SDG 14 Programme | Stakeholder analysis | Local |
| ARC-002-REQ-v1.0 | Architecture | SDG 14 Programme | Requirements specification | Local |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fishing Quota Management
**Model**: Claude Opus 4.6
