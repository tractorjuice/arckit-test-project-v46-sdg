# Strategic Outline Business Case (SOBC): Skills Passport System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Skills Passport System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Skills Passport Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Programme Board, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC assesses the case for investing in a Digital Skills Passport System using W3C Verifiable Credentials to enable portable, verified digital qualifications for UK citizens, supporting the Lifelong Loan Entitlement and skills-based employment.

---

## Executive Summary

**Purpose**: Create the digital credential infrastructure that enables every UK citizen to hold, share, and verify their qualifications and skills in a portable, tamper-proof digital wallet, supporting lifelong learning and skills-based job matching.

**Problem Statement**: UK qualifications are siloed across hundreds of institutions and awarding bodies. Credential verification takes days and costs money. Credential fraud costs employers an estimated GBP 7 billion annually. The Lifelong Loan Entitlement (launching 2027) requires digital infrastructure to track modular learning across institutions — this infrastructure does not exist.

**Proposed Solution**: A federated platform using W3C Verifiable Credentials where education providers and awarding bodies issue digitally signed credentials to individuals' secure wallets, enabling instant cryptographic verification by employers and institutions.

**Strategic Fit**: Directly enables the Lifelong Loan Entitlement policy. Supports the Skills for Jobs White Paper. Integrates with the Job Matching Platform (Project 001) for verified skills-based matching. Aligns with the European Digital Credentials Framework for international interoperability.

**Investment Required**: GBP 15M over 3 years

- Capital: GBP 10M
- Operational (3 years): GBP 5M

**Expected Benefits**: GBP 55M over 5 years

- Reduced credential fraud: GBP 35M (employer savings)
- Credential verification efficiency: GBP 12M
- LLE policy enablement: GBP 8M (administrative savings)

**Return on Investment**:

- NPV: GBP 28M (discounted at 3.5%)
- Payback Period: 26 months
- ROI: 267% over 5 years

**Recommended Option**: Option 2: Federated Verifiable Credentials Platform

**Key Risks**:

1. University sector refusal to adopt if architecture perceived as centralised
2. W3C VC standard implementation inconsistencies across issuers
3. Insufficient employer adoption of cryptographic verification

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Lifelong Loan Entitlement creates a hard policy deadline — without digital credential tracking, LLE cannot operate as designed. The federated architecture (Option 2) addresses university autonomy concerns while delivering the national framework DfE needs. The fraud reduction benefits alone justify the investment.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Qualifications data is fragmented across universities, awarding bodies (City & Guilds, Pearson, OCR), professional bodies (BCS, RICS, GMC), and employer-issued certifications. To verify a candidate's qualifications, an employer must contact each institution separately — a process taking days to weeks and costing GBP 10-50 per verification. The Learner Records Service holds some data but is incomplete and not designed for real-time verification.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| Employers | Manual credential verification (3-10 days per candidate) | GBP 7B annual fraud cost, hiring delays | CRITICAL |
| Learners | No portable credential record; lost if institution closes | Career mobility limited | HIGH |
| DfE | No infrastructure for LLE modular learning tracking | LLE policy delivery at risk | CRITICAL |
| Universities | Transcript services are revenue but labour-intensive | Operational cost, student frustration | MEDIUM |
| Ofqual | Cannot distinguish regulated from unregulated credentials | Qualification framework integrity | HIGH |

**Consequences of Inaction**:

- Lifelong Loan Entitlement launches without digital credential tracking — manual processes, high error rate
- GBP 7B annual credential fraud continues unabated
- UK falls behind EU (European Digital Credentials Framework operational by 2027)
- Skills-based job matching (Project 001) relies on unverified self-reported skills

### A1.2 Strategic Drivers

| Driver ID | Stakeholder | Driver Type | Description |
|-----------|-------------|-------------|-------------|
| SD-1 | Secretary of State (Education) | STRATEGIC | Enable Lifelong Loan Entitlement |
| SD-2 | Universities UK | STRATEGIC | Preserve institutional autonomy in credential issuance |
| SD-3 | Employers | FINANCIAL | Instant, reliable credential verification |
| SD-4 | Learners | PERSONAL | Own and control their credential data |
| SD-5 | Ofqual | COMPLIANCE | Maintain qualification framework integrity |

**Strategic Alignment**:

- **Skills for Jobs White Paper**: Digital credentials for employer-led skills development
- **Lifelong Loan Entitlement**: Modular learning tracking across institutions
- **Industrial Strategy**: Skills portability for workforce mobility and productivity
- **Technology Code of Practice**: Open standards (W3C), avoid vendor lock-in

### A1.3 Scope

**In Scope**:
- W3C Verifiable Credential issuance framework
- Individual credential wallet (web and mobile)
- Verification API for employers and services
- Trust registry of recognised issuers
- ESCO/SOC skills taxonomy mapping
- Integration with Job Matching Platform (Project 001) and UCAS

**Out of Scope**:
- Education/training delivery
- Student finance (SLC integration Phase 2)
- International credential equivalency (UK ENIC separate)
- Assessment/examination systems

### A1.5 Why Now?

**Urgency Factors**:

- Lifelong Loan Entitlement launching 2027 — digital credential infrastructure needed 12 months before
- W3C Verifiable Credentials 2.0 specification finalised — standard now mature enough for government adoption
- EU Digital Credentials Framework launching 2027 — UK must maintain interoperability for labour mobility
- Job Matching Platform (Project 001) in development — skills data integration opportunity

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Issuer Adoption**: 50 credential issuers within 12 months
2. **Credential Verification Speed**: < 2 seconds for 99.9% of verifications
3. **University Sector Support**: Russell Group and at least 20 post-92 universities participating
4. **Ofqual Endorsement**: Classification schema approved before public launch

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Rely on existing paper/PDF credentials and ad-hoc digital initiatives (Digitary, Blockcerts experiments).

**Costs** (3-year): GBP 3M (continued LRS maintenance)
**Benefits**: GBP 0

**Pros**:
- No investment risk

**Cons**:
- LLE cannot operate effectively without digital credential tracking
- GBP 7B annual fraud cost continues
- UK credential infrastructure falls behind EU
- Skills-based job matching operates on unverified data

**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject**

---

### Option 1: Centralised Credential Database

**Description**: DfE operates a centralised database of all UK qualifications, with issuers submitting credential data to DfE for storage and verification.

**Costs** (3-year): GBP 12M
**Benefits** (5-year): GBP 50M

**Pros**:
- Simpler architecture
- DfE has full control and visibility
- Faster to build

**Cons**:
- University sector will boycott — perceived as government takeover of credential issuance
- Single point of failure and attack target
- Vendor lock-in (centralised database not portable)
- Does not meet W3C VC standard (centralised, not decentralised)
- International interoperability compromised

**Stakeholder Goals Met**: 40% (G-1 partially met, G-2 not met — autonomy violated)
**Recommendation**: **Reject** — University sector resistance makes this undeliverable.

---

### Option 2: Federated Verifiable Credentials Platform (RECOMMENDED)

**Description**: Decentralised architecture using W3C Verifiable Credentials where each institution is a sovereign issuer with its own DID (Decentralised Identifier). DfE operates the trust registry (which issuers are recognised) but does not control or store credentials. Individuals hold credentials in their own wallet.

**Costs** (3-year) - ROM (+/- 30%):

- Capital: GBP 10M
  - VC issuance framework and SDK: GBP 3M
  - Credential wallet (web and mobile): GBP 2.5M
  - Verification API and trust registry: GBP 2M
  - Skills taxonomy mapping and integration: GBP 1.5M
  - Issuer onboarding and testing tools: GBP 1M
- Operational: GBP 5M over 3 years
  - Cloud hosting (UK sovereign): GBP 1M/year
  - Issuer support and onboarding team: GBP 0.5M/year
  - Security and cryptographic operations: GBP 0.2M/year
- Total 3-year TCO: GBP 15M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Reduced credential fraud | FINANCIAL | GBP 2M | GBP 5M | GBP 8M | GBP 10M | GBP 10M | GBP 35M |
| B-002 | Verification efficiency (employer savings) | OPERATIONAL | GBP 1M | GBP 2M | GBP 3M | GBP 3M | GBP 3M | GBP 12M |
| B-003 | LLE administrative savings | FINANCIAL | GBP 0 | GBP 1M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 8M |
| **Total** | | | **GBP 3M** | **GBP 8M** | **GBP 13M** | **GBP 15.5M** | **GBP 15.5M** | **GBP 55M** |

**NPV** (3.5%): GBP 28M
**ROI**: 267% over 5 years
**Payback**: 26 months

**Stakeholder Goals Met**: 90%

**Pros**:
- University autonomy preserved — each institution is a sovereign issuer
- W3C standard compliance ensures international interoperability
- No single point of failure — decentralised architecture
- Individuals own their data — portable across systems
- Integrates with EU Digital Credentials Framework

**Cons**:
- More complex architecture than centralised option
- Requires issuer onboarding effort
- Cryptographic key management complexity
- Adoption dependent on voluntary university participation

---

### Option 3: Full Decentralised Identity Platform

**Description**: Comprehensive Self-Sovereign Identity (SSI) platform covering not just credentials but all government identity interactions, using blockchain-based DID infrastructure.

**Costs** (3-year): GBP 30M
**Benefits** (5-year): GBP 65M (marginally higher)

**Pros**:
- Future-proofed for broader SSI adoption
- Maximum individual sovereignty

**Cons**:
- Scope creep — identity is a cross-government problem beyond DfE's remit
- Blockchain infrastructure adds cost and complexity without proportionate benefit for credentials
- GDS and GOV.UK One Login team would resist parallel identity platform
- Delivery risk HIGH — 24+ month timeline

**Recommendation**: **Reject** — Scope exceeds DfE's remit. Credential focus (Option 2) delivers specific benefits without identity platform complexity.

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Approach**: In-house core platform development with specialist VC/cryptography consultancy via CCS DOS framework.

**Key Contracts**:
- W3C VC/DID specialist consultancy: GBP 2M via DOS
- Mobile wallet development: GBP 1.5M via DOS
- Cloud hosting: CCS G-Cloud
- Issuer SDK and testing: In-house DfE Digital

---

# PART D: FINANCIAL CASE

## D1. Funding Profile

| Year | Capital | Operational | Total |
|------|---------|-------------|-------|
| 2026-27 | GBP 5M | GBP 1M | GBP 6M |
| 2027-28 | GBP 3.5M | GBP 1.7M | GBP 5.2M |
| 2028-29 | GBP 1.5M | GBP 2.3M | GBP 3.8M |
| **Total** | **GBP 10M** | **GBP 5M** | **GBP 15M** |

**Funding Source**: DfE Skills and Further Education budget.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile with GDS phases

**Timeline**:
- Discovery: Q2 2026 (3 months)
- Alpha: Q3-Q4 2026 (6 months) — VC proof-of-concept with 5 pilot issuers
- Private Beta: Q1-Q2 2027 (6 months) — 20 issuers, 50,000 wallet holders
- Public Beta: Q3-Q4 2027 (6 months) — 50 issuers, LLE integration
- Live: Q1 2028 (aligned with LLE launch)

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| University sector boycott | MEDIUM | CRITICAL | Federated architecture, co-design, sector governance |
| VC standard implementation inconsistencies | HIGH | HIGH | UK credential profile, conformance testing, issuer SDK |
| Employer verification adoption | MEDIUM | HIGH | Free verification API, ATS integration partnerships |
| Key management complexity | MEDIUM | MEDIUM | HSM-backed infrastructure, key rotation automation |
| LLE policy delay | LOW | HIGH | Modular delivery — credential platform valuable without LLE |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-002-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals, conflicts | `projects/002-skills-passport-system/ARC-002-STKE-v1.0.md` |
| ARC-002-REQ-v1.0 | Requirements | SDG 8 Programme | Requirements | `projects/002-skills-passport-system/ARC-002-REQ-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 3, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Skills Passport System
**Model**: Claude Opus 4.6
