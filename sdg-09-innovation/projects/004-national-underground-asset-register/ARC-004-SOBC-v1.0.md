# Strategic Outline Business Case (SOBC): National Underground Asset Register

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | National Underground Asset Register (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, National Underground Asset Register Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NUAR Programme Board, Geospatial Commission, HM Treasury, NCSC |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC sets out the strategic justification for investing in a National Underground Asset Register providing a single, secure digital view of underground pipes and cables to reduce accidental utility strikes.

---

## Executive Summary

**Purpose**: To create a secure digital platform providing a single view of underground utility assets (gas, electricity, water, telecoms) to reduce the estimated 60,000 annual utility strikes in the UK, saving lives and reducing GBP 2.4 billion in annual costs.

**Problem Statement**: Before any excavation, contractors must separately contact each utility company to request underground asset information. This takes 5-10 working days, responses arrive in different formats with varying accuracy, and the information is frequently incomplete. The result: 60,000 utility strikes per year, 3 worker fatalities, GBP 2.4 billion in costs, and millions of citizens affected by service disruptions.

**Proposed Solution**: Build a secure platform where utility companies submit underground asset data in PAS 256 format, and verified users can query all assets in a defined area within 60 seconds, with CNI-appropriate security controls assessed by NCSC.

**Strategic Fit**: Directly supports the UK Geospatial Strategy 2030, HSE safety objectives, and the National Infrastructure Strategy. Identified by the Geospatial Commission as the highest-value geospatial data opportunity.

**Investment Required**: GBP 12.7M over 3 years

- Capital: GBP 9.0M
- Operational (3 years): GBP 3.7M

**Expected Benefits**: GBP 720M per year (30% reduction in GBP 2.4B annual strike costs)

- Utility repair cost savings: GBP 500M/year
- Construction delay reduction: GBP 150M/year
- Emergency service cost savings: GBP 50M/year
- Safety benefits (injuries prevented): GBP 20M/year

**Return on Investment**:

- NPV: GBP 1.8B (discounted at 3.5%, 5-year horizon)
- Payback Period: 1 month (once operational at scale)
- ROI: 5,500%

**Recommended Option**: Option 2: Secure National Platform with Verified Access

**Key Risks**:

1. Major utility refusing to share data citing CNI security concerns
2. Data accuracy insufficient for safety-critical use
3. Liability if strike occurs despite using platform data

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The benefit-to-cost ratio is extraordinary — GBP 720M annual savings for a GBP 12.7M investment. The safety case alone (3 fatalities and hundreds of injuries per year) provides moral imperative. The Geospatial Commission has identified this as the single highest-value geospatial data opportunity in the UK.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The UK has approximately 1.5 million kilometres of underground utility infrastructure — gas pipes, electricity cables, water mains, sewers, and telecoms cables. Before any excavation (road works, construction, utility maintenance), contractors must identify what lies beneath. The current process requires contacting each utility company separately, waiting 5-10 working days for each response, and reconciling responses in different formats. Many smaller contractors skip this process entirely due to time and cost, leading to uninformed excavation and preventable strikes.

**Specific Pain Points** (from Stakeholder Analysis ARC-004-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Geospatial Commission | SD-1 | 60,000 strikes/year, GBP 2.4B cost | National economic cost, safety | CRITICAL |
| Major Utilities | SD-2 | Thousands of third-party strikes per year on their assets | Repair costs, safety incidents, service disruptions | CRITICAL |
| Construction Industry | SD-3 | 5-10 day wait for plant enquiry responses | GBP 500M/year construction delays | HIGH |
| HSE | SD-4 | 3 fatalities, hundreds of injuries per year | Worker safety | HIGH |

**Consequences of Inaction**:

- 60,000 strikes per year continue at GBP 2.4B annual cost
- 3 worker deaths per year from preventable incidents
- Millions of citizens affected by gas leaks, power cuts, water outages, broadband interruptions
- Construction productivity continues to be hampered by slow plant enquiry process

### A1.2 Strategic Alignment

- **UK Geospatial Strategy 2030**: Underground asset data identified as highest-value opportunity
- **National Infrastructure Strategy**: Efficient infrastructure maintenance and investment
- **HSE HSG47**: Regulatory framework for avoiding underground service damage
- **PAS 256**: British Standard for buried asset data specification
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Geospatial Data), 6 (Security by Design), 8 (Data Sovereignty), 10 (Data Quality)

### A1.3 Why Now?

- PAS 256 standard now published — technical data model available for interoperability
- NCSC has published specific CNI data protection guidance — security approach is clear
- Utility companies increasingly digitising asset records — data quality improving
- Construction industry productivity agenda creating political support
- Post-Grenfell safety culture shift creating appetite for proactive safety measures

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Utility Participation**: All major gas, electricity, water, and telecoms asset owners submitting data
2. **Security Approval**: NCSC assessment passed for CNI-adjacent data handling
3. **Response Speed**: Pre-excavation enquiry in <60 seconds (vs 5-10 days)

## B2. Options Analysis

### Option 0: Do Nothing

**Costs**: GBP 0 additional capital. GBP 2.4B/year continues as cost to economy.

**Benefits**: GBP 0

**Recommendation**: **Reject** — 3 deaths and 60,000 strikes per year continue. Morally and economically unacceptable.

---

### Option 1: Enhanced Existing Service (LSBUD Upgrade)

**Description**: Fund enhancement of the existing Linesearch beforeUdig (LSBUD) service with improved digital interface and faster processing, but maintaining the current separate-enquiry model.

**Costs** (3-year): GBP 5.0M

**Benefits** (3-year): GBP 300M (15% strike reduction through faster processing)

**Stakeholder Goals Met**: 30%

**Recommendation**: Incremental improvement but does not address the fundamental problem — data remains siloed by utility company with no unified view.

---

### Option 2: Secure National Platform — Verified Access (RECOMMENDED)

**Description**: New platform where all major utilities submit data in PAS 256 format. Verified users query all assets in a defined area through a single interface. NCSC-assessed security architecture with anti-aggregation controls.

**Costs** (3-year) - ROM (+-30%):

- Capital: GBP 9.0M
  - Platform development: GBP 6.0M
  - NCSC security assessment and architecture: GBP 1.5M
  - OS data licensing: GBP 0.5M
  - Data onboarding: GBP 1.0M
- Operational: GBP 3.7M over 3 years
  - Secure cloud infrastructure: GBP 1.0M/year (from Year 2)
  - BAU team: GBP 1.2M/year (from Year 2)
  - OS licensing: GBP 0.2M/year
  - NCSC annual assessment: GBP 0.1M/year
- Total 3-year TCO: GBP 12.7M

**Benefits** (3-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Utility repair cost savings (30% reduction) | Utilities G-1 | FINANCIAL | GBP 0M | GBP 250M | GBP 500M | GBP 750M |
| B-002 | Construction delay reduction | Contractors G-3 | FINANCIAL | GBP 0M | GBP 75M | GBP 150M | GBP 225M |
| B-003 | Emergency service savings | HSE G-3 | FINANCIAL | GBP 0M | GBP 25M | GBP 50M | GBP 75M |
| B-004 | Safety benefits (injuries prevented) | HSE G-3 | SAFETY | GBP 0M | GBP 10M | GBP 20M | GBP 30M |
| **Total** | | | | **GBP 0M** | **GBP 360M** | **GBP 720M** | **GBP 1,080M** |

**NPV** (3.5% discount): **GBP 1,000M** (3-year)

**ROI**: 8,400% over 3 years | **Payback Period**: 1 month (once operational at scale)

**Stakeholder Goals Met**: 85%

**Recommendation**: **RECOMMENDED** — Extraordinary benefit-to-cost ratio. The safety case alone justifies investment.

---

### Option 3: Comprehensive National Register with Real-Time Monitoring

**Description**: Option 2 plus real-time IoT sensor integration, automated excavation permits, above-ground infrastructure, and local authority street furniture.

**Costs** (3-year): GBP 30M

**Benefits** (3-year): GBP 1,200M (marginally higher)

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject at SOBC** — IoT integration and above-ground infrastructure add cost and complexity without proportionate benefit. Core underground asset register delivers 90% of the value.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 0M | GBP 5M | GBP 12.7M | GBP 30M |
| 3-Year Benefit | GBP 0M | GBP 300M | GBP 1,080M | GBP 1,200M |
| NPV | GBP 0M | GBP 280M | GBP 1,000M | GBP 1,050M |
| Stakeholder Goals | 0% | 30% | 85% | 100% |
| Implementation Risk | None | LOW | MEDIUM | HIGH |
| Recommendation | Reject | Reject | **RECOMMENDED** | Reject |

---

# PART C: COMMERCIAL CASE

**Approach**: Internal build by Geospatial Commission digital team with specialist subcontractors for CNI security architecture and geospatial database engineering.

**Key Procurements**:

- Secure cloud hosting: Crown Hosting / sovereign cloud (GBP 1.0M/year)
- NCSC security assessment: NCSC-approved assessors (GBP 0.3M)
- Ordnance Survey licensing: PSMA + AddressBase Premium
- PAS 256 compliance consultancy: BSI / specialist (GBP 0.2M)

---

# PART D: FINANCIAL CASE

| Financial Year | Capital | Revenue | Total |
|----------------|---------|---------|-------|
| FY 2026/27 | GBP 5.0M | GBP 0.2M | GBP 5.2M |
| FY 2027/28 | GBP 3.5M | GBP 1.5M | GBP 5.0M |
| FY 2028/29 | GBP 0.5M | GBP 2.0M | GBP 2.5M |
| **Total** | **GBP 9.0M** | **GBP 3.7M** | **GBP 12.7M** |

**Funding Source**: Geospatial Commission budget (Cabinet Office), with potential cost recovery from utility company subscriptions in steady state.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research with contractors and utilities, security assessment scope |
| Alpha | 4 months | Prototype, NCSC initial assessment, PAS 256 data model validation |
| Private Beta (Region 1) | 6 months | North East England pilot with 5 major utilities |
| Private Beta (National) | 6 months | National rollout, all major utilities onboarded |
| Live | Ongoing | Full national service |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Utility data refusal | MEDIUM | CRITICAL | NCSC security assessment first; regulatory backstop if needed |
| Data accuracy insufficient | HIGH | HIGH | Quality scoring; disclaimers; feedback mechanism; safety not solely platform-dependent |
| NCSC assessment failure | LOW | CRITICAL | Engage NCSC from Discovery; iterate security architecture |
| Liability for inaccurate data | MEDIUM | HIGH | Clear T&Cs — platform supplements not replaces on-site detection; insurance |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-004-STKE-v1.0 | Stakeholder Analysis | ArcKit | Drivers and goals | `projects/004-national-underground-asset-register/` |
| ARC-004-REQ-v1.0 | Requirements | ArcKit | Requirements | `projects/004-national-underground-asset-register/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Underground Asset Register (Project 004)
**Model**: Claude Opus 4.6
