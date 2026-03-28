# Strategic Outline Business Case: UK Emissions Trading Registry

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | UK Emissions Trading Registry (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, UK ETS Registry Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | UK ETS Programme Board, DESNZ Digital, HM Treasury, FCA, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in a modernised UK Emissions Trading Scheme Registry, following HM Treasury Green Book five-case model methodology.

---

## Executive Summary

**Purpose**: The UK ETS Registry is the regulated digital system managing carbon allowance accounts, transactions, and compliance for approximately 1,000 obligated installations and aviation operators. The current interim registry requires modernisation to meet FCA financial-grade standards, support growing market complexity, and enable potential EU ETS linkage.

**Problem Statement**: The interim UK ETS Registry, established rapidly post-Brexit, lacks financial-grade KYC/AML controls, has limited scalability, and does not meet FCA expectations for a market infrastructure handling GBP 5 billion in annual auction revenue. The EU ETS precedent (EUR 5 billion VAT carousel fraud) demonstrates the consequences of inadequate registry security.

**Proposed Solution**: Build a modern, cloud-native registry platform with FCA-grade financial crime controls, real-time transaction monitoring, automated auction settlement, and four-nation regulatory access.

**Strategic Fit**: Directly supports UK ETS legislation (GHG Emissions Trading Scheme Order 2020), UK carbon pricing policy, and net zero delivery mechanism.

**Investment Required**: GBP 28.0M over 3 years

- Capital: GBP 18.0M
- Operational (3 years): GBP 10.0M

**Expected Benefits**: GBP 65.0M over 5 years

- Protected auction revenue: GBP 25.0B annually (registry failure risk valued at GBP 50M)
- Fraud prevention (EU ETS precedent): GBP 8.0M avoided loss
- Operator efficiency gains: GBP 3.5M
- Regulatory efficiency: GBP 3.5M

**Return on Investment**:

- NPV: GBP 28.5M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 132%

**Recommended Option**: Option 2: Modern Financial-Grade Registry Platform

**Key Risks**:

1. FCA supervisory expectations exceed initial scope — mitigated by early FCA engagement
2. ICE Futures integration complexity — mitigated by dedicated integration workstream
3. Four-nation governance delays decision-making — mitigated by clear RACI and escalation

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK ETS generates approximately GBP 5 billion annually in auction revenue and is the UK's primary carbon pricing mechanism. A registry failure during the compliance window would impose automatic penalties on obligated entities, damage market confidence, and potentially disrupt auction revenue. The interim registry is not sustainable for a market of this scale and regulatory significance. Investment is modest relative to the revenue it protects.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The interim UK ETS Registry was established under urgency following Brexit. While functional, it lacks the financial-grade controls expected by the FCA for a market handling GBP 5 billion in annual transactions. KYC/AML processes are largely manual. Transaction monitoring is basic. The four regulators (EA, SEPA, NRW, DAERA) have limited self-service access. Auction settlement with ICE Futures Europe involves manual reconciliation steps.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| UK ETS Authority | SD-1 | Interim registry lacks financial-grade controls | Regulatory risk | CRITICAL |
| FCA | SD-2 | KYC/AML inadequate for financial market infrastructure | Market integrity risk | CRITICAL |
| Operators | SD-3 | Complex EU ETS-style interface, manual processes | High compliance burden | HIGH |
| HM Treasury | SD-4 | Manual auction settlement, reconciliation risk | Revenue risk | HIGH |
| ICE Futures | SD-5 | Limited API integration, manual processes | Settlement risk | HIGH |

**Consequences of Inaction**:

- FCA escalates supervisory concerns — potential enforcement action
- Carbon credit fraud (EU ETS lost EUR 5 billion to VAT carousel) — reputational and financial damage
- Registry failure during surrender window — automatic penalties for operators, legal challenges
- Market confidence erosion — reduced auction participation, lower allowance prices, lower revenue
- EU ETS linkage impossible without modern, interoperable registry

### A1.2 Strategic Alignment

- **GHG Emissions Trading Scheme Order 2020**: Statutory registry requirements
- **UK Carbon Pricing Policy**: ETS is the primary carbon pricing mechanism
- **FCA Market Integrity**: MiFID-classified financial market infrastructure
- **Net Zero Strategy**: Carbon pricing signals drive decarbonisation investment
- **Architecture Principles**: Security by Design (P5), Availability (P14), Audit Trail (P6)

### A1.3 Why Now?

- FCA supervisory assessment scheduled for Q3 2027 — modernisation must be underway
- EU ETS linkage negotiations require interoperable, modern registry
- UK ETS cap reduction accelerating — scheme complexity increasing annually
- Current vendor contract expires 2028 — procurement window requires early planning

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **100% Compliance Window Availability**: Zero downtime during 1 March - 30 April surrender period
2. **FCA Assessment Pass**: No major findings in supervisory assessment
3. **Zero Fraud Incidents**: No account compromise or fraudulent transactions

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (3-year): GBP 0 capital; GBP 12.0M operational (existing contract, manual processes)

**Benefits**: GBP 0

**Risks**: FCA enforcement, fraud exposure, auction disruption

**Recommendation**: **Reject** — regulatory and financial risk unacceptable

---

### Option 1: Minimal Upgrade to Existing Platform

**Description**: Patch existing registry with additional KYC/AML controls and monitoring. Limited architectural change.

**Costs** (3-year): GBP 8.0M

**Benefits** (3-year): GBP 12.0M

**Stakeholder Goals Met**: 40% (KYC improved but scalability, integration, and UX unchanged)

**Recommendation**: **Reject** — does not address scalability or EU ETS linkage requirements

---

### Option 2: Modern Financial-Grade Registry (RECOMMENDED)

**Description**: Cloud-native registry platform with FCA-grade KYC/AML, real-time transaction monitoring, automated auction settlement, four-nation regulatory dashboards, and API integration with ICE Futures Europe.

**Costs** (3-year) - ROM (+/-30%):

- Capital: GBP 18.0M
- Operational: GBP 10.0M
- Total 3-year TCO: GBP 28.0M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------------|------------|------|--------|--------|--------|--------|--------|-------|
| B-001 | Protected auction revenue (risk reduction) | FINANCIAL | GBP 5.0M | GBP 10.0M | GBP 12.0M | GBP 12.0M | GBP 11.0M | GBP 50.0M |
| B-002 | Fraud prevention | RISK | GBP 0.5M | GBP 1.5M | GBP 2.0M | GBP 2.0M | GBP 2.0M | GBP 8.0M |
| B-003 | Operator efficiency | OPERATIONAL | GBP 0.3M | GBP 0.7M | GBP 0.8M | GBP 0.8M | GBP 0.9M | GBP 3.5M |
| B-004 | Regulatory efficiency | OPERATIONAL | GBP 0.2M | GBP 0.5M | GBP 0.8M | GBP 1.0M | GBP 1.0M | GBP 3.5M |
| **Total** | | | **GBP 6.0M** | **GBP 12.7M** | **GBP 15.6M** | **GBP 15.8M** | **GBP 14.9M** | **GBP 65.0M** |

**NPV** (3.5% discount): GBP 28.5M

**Payback Period**: 18 months

**Stakeholder Goals Met**: 90%

---

### Option 3: Blockchain-Based Distributed Registry

**Description**: Distributed ledger technology (DLT) based registry with decentralised transaction processing.

**Costs** (3-year): GBP 45.0M

**Benefits** (5-year): GBP 55.0M (marginal improvement over Option 2)

**Recommendation**: **Reject** — technology immaturity for regulated financial systems, FCA concerns about DLT governance, excessive cost with marginal benefit

---

## B3. Recommended Option

**Option 2: Modern Financial-Grade Registry** — Best risk-adjusted NPV, achievable timeline, regulatory confidence.

**Optimism Bias**: +40% uplift: GBP 28.0M --> GBP 39.2M. NPV still strongly positive at GBP 18.3M.

---

# PART C: COMMERCIAL CASE

**Recommended Route**: Competitive tender for registry platform build and managed service. G-Cloud for cloud hosting. Direct award for ICE Futures integration (specialist requirement).

**Contract Structure**: 3+2+2 year managed service contract. Fixed-price build milestones. Outcome-based SLAs with financial penalties for non-compliance.

**Social Value**: 10% weighting — prioritise UK-based development, green data centre hosting.

---

# PART D: FINANCIAL CASE

**Total Investment**: GBP 28.0M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | GBP 10.0M | GBP 8.0M | GBP 0.0M | GBP 18.0M |
| OpEx | GBP 2.5M | GBP 3.5M | GBP 4.0M | GBP 10.0M |
| **Total** | **GBP 12.5M** | **GBP 11.5M** | **GBP 4.0M** | **GBP 28.0M** |

**Funding Source**: DESNZ Climate Programme Fund + HM Treasury ETS revenue hypothecation (registry costs funded from auction proceeds)

**Affordability**: Registry costs represent 0.56% of annual ETS auction revenue (GBP 5B) — highly affordable relative to revenue protected.

---

# PART E: MANAGEMENT CASE

## E1. Governance

**SRO**: Director of Carbon Markets, DESNZ

**Steering Committee**: SRO (Chair), DESNZ Finance, FCA Observer, UK ETS Authority Representative, ICE Futures Europe Liaison, DESNZ CDIO

## E2. Key Milestones

| Milestone | Date | Owner |
|-----------|------|-------|
| FCA requirements workshop | Month 2 | Compliance Lead |
| ICE integration specification agreed | Month 4 | Technical Lead |
| KYC/AML controls operational | Month 10 | Compliance Lead |
| Parallel running with existing registry | Month 14 | SRO |
| Go-live (outside surrender window) | Month 16 | SRO |
| First compliance cycle on new platform | Month 20 | SRO |
| FCA supervisory assessment | Month 22 | DESNZ SIRO |

## E3. Risk Management

| Risk ID | Description | Likelihood | Impact | Score | Mitigation |
|---------|-------------|------------|--------|-------|------------|
| R-001 | FCA requirements exceed scope | Medium | Critical | 12 | Early FCA engagement, joint requirements workshops |
| R-002 | ICE integration complexity | Medium | Critical | 12 | Dedicated integration workstream, POC at Month 4 |
| R-003 | Migration data loss | Low | Critical | 9 | Parallel running, reconciliation, rollback plan |
| R-004 | Four-nation governance delays | Medium | Major | 9 | Clear RACI, delegated authority thresholds |
| R-005 | Vendor capability insufficient | Medium | Major | 9 | Rigorous procurement evaluation, reference sites |
| R-006 | Go-live during surrender window | Low | Critical | 9 | Hard constraint: go-live only June-December |
| R-007 | Carbon market fraud during transition | Low | Critical | 9 | Parallel systems, enhanced monitoring during transition |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: Modern Financial-Grade Registry

**Investment**: GBP 28.0M over 3 years

**Expected Return**: GBP 65.0M over 5 years (NPV GBP 28.5M, ROI 132%)

**Go/No-Go**: **PROCEED**

**Next Steps**:

1. FCA formal requirements engagement — Month 1
2. ICE Futures integration scoping — Month 1
3. Competitive procurement for registry vendor — Month 2
4. Detailed requirements: `/arckit.requirements` — Complete (ARC-003-REQ-v1.0)

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO | | |
| | DESNZ Finance Director | | |
| | FCA Representative | | |
| | HM Treasury ETS Revenue Team | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GHG Emissions Trading Scheme Order 2020 | Legislation | legislation.gov.uk | Registry requirements | N/A |
| HM Treasury Green Book | Guidance | GOV.UK | Appraisal methodology | N/A |
| EU ETS Fraud Report (Europol) | Analysis | Europol | EUR 5B VAT carousel fraud | N/A |
| FCA Carbon Markets Supervision | Regulatory | FCA | Market integrity expectations | N/A |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: UK Emissions Trading Registry (Project 003)
**Model**: Claude Opus 4.6
