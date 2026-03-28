# Strategic Outline Business Case (SOBC): Small Business Support Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Small Business Support Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Small Business Support Portal Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DBT Programme Board, HM Treasury, CDDO, British Business Bank |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC assesses the case for investing in an integrated Small Business Support Portal to replace the fragmented landscape of government business support services with a single personalised entry point.

---

## Executive Summary

**Purpose**: Create a single, personalised digital portal where any of the UK's 5.5 million SMEs can discover, assess eligibility for, and apply for government support — grants, loans, advice, regulatory guidance, export assistance, and procurement opportunities.

**Problem Statement**: Government support for SMEs is scattered across GOV.UK, British Business Bank, Growth Hubs, LEP websites, Innovate UK, and departmental microsites. An FSB survey found 60% of eligible businesses are unaware of at least one support scheme they could access. An estimated GBP 3 billion in government support goes unclaimed annually because businesses cannot find it.

**Proposed Solution**: A GOV.UK service that aggregates 200+ support schemes from 10+ departments, personalises recommendations based on business type, sector, size, and location, and simplifies application through pre-populated forms using Companies House and GOV.UK account data.

**Strategic Fit**: Directly delivers the Industrial Strategy commitment to SME productivity. Supports Levelling Up by ensuring businesses in underperforming regions can access support equally. Aligns with GDS Service Standard.

**Investment Required**: GBP 8M over 3 years

- Capital: GBP 5M
- Operational (3 years): GBP 3M

**Expected Benefits**: GBP 35M over 5 years

- Additional government support accessed by SMEs: GBP 25M (economic value of unlocked funding)
- SME administrative time savings: GBP 7M
- Departmental efficiency (reduced duplicate enquiries): GBP 3M

**Return on Investment**:

- NPV: GBP 18M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 338%

**Recommended Option**: Option 2: Personalised Aggregation Portal on GOV.UK

**Key Risks**:

1. Departmental resistance to sharing scheme data and ceding portal real estate
2. GOV.UK One Login business account functionality not ready for Beta
3. Scheme data quality varies across departments

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The GBP 3B annual under-claim of government support represents a significant market failure in information provision. The portal investment is modest (GBP 8M) relative to the support it will unlock. The technology is straightforward — the challenge is cross-departmental cooperation, which requires Ministerial and Cabinet Office backing.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
A sole trader hairdresser in Sunderland who wants to expand her business faces a maze of websites: GOV.UK for general guidance, British Business Bank for Start Up Loans, the North East LEP for regional grants, Innovate UK for innovation funding, HMRC for R&D tax credits, and her local council for business rates relief. She does not know which she is eligible for, where to start, or how to apply. She spends 2 hours searching, gives up, and does not access GBP 15,000 in support she is eligible for.

**Consequences of Inaction**:

- GBP 3B annual under-claim of government support continues
- SME productivity gap with G7 peers persists
- Levelling Up ambitions undermined — businesses in disadvantaged regions least likely to find support
- Government spends on support schemes that fail to reach target businesses
- FSB and BCC continue to criticise government for fragmented support

### A1.2 Strategic Alignment

- **Industrial Strategy**: "Improve SME access to government support services"
- **Levelling Up White Paper**: "Every community should have access to the same quality of business support"
- **GDS Service Standard**: "Make the service simple to use" — current fragmentation violates this principle

### A1.5 Why Now?

- GOV.UK One Login maturing — enables personalised business accounts for first time
- Companies House API provides rich business data for pre-population
- Post-COVID recovery — SMEs need support access more than ever
- Cross-departmental digital infrastructure (GOV.UK platform) mature enough to support aggregation

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Scheme Coverage**: 200+ schemes from 10+ departments indexed at launch
2. **Personalisation Accuracy**: 80% of recommendations rated relevant by users
3. **Application Simplification**: Average time to application reduced to 30 minutes
4. **SME Adoption**: 500,000 monthly visitors within 12 months

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Maintain current fragmented landscape.

**Costs** (3-year): GBP 2M (existing GOV.UK business pages)
**Benefits**: GBP 0

**Cons**:
- GBP 3B annual under-claim continues
- SME productivity gap persists
- Political pressure from FSB/BCC continues

**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject**

---

### Option 1: Curated GOV.UK Business Section

**Description**: Improve GOV.UK business content with better information architecture and a simple eligibility questionnaire that links to departmental pages.

**Costs** (3-year): GBP 3M
**Benefits** (5-year): GBP 15M

**Pros**:
- Low cost and risk
- GDS-compliant
- Fast to deliver (3 months)

**Cons**:
- Content curation only — no true personalisation
- No pre-populated applications
- Schemes still managed by individual departments — fragmentation continues
- Limited impact on awareness gap

**Stakeholder Goals Met**: 30%

---

### Option 2: Personalised Aggregation Portal on GOV.UK (RECOMMENDED)

**Description**: A GOV.UK service that authenticates businesses via One Login, imports data from Companies House, and provides personalised scheme recommendations with eligibility assessment. Application forms pre-populated where possible.

**Costs** (3-year) - ROM (+/- 30%):

- Capital: GBP 5M
  - Eligibility engine and scheme aggregation: GBP 2M
  - GOV.UK One Login business integration: GBP 1M
  - Companies House integration and pre-population: GBP 0.8M
  - Content design and departmental coordination: GBP 0.7M
  - Procurement alerts and export tools: GBP 0.5M
- Operational: GBP 3M over 3 years
  - Hosting (GOV.UK PaaS): GBP 0.3M/year
  - Content and scheme data maintenance: GBP 0.5M/year
  - User support: GBP 0.2M/year
- Total 3-year TCO: GBP 8M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Additional support accessed by SMEs | ECONOMIC | GBP 2M | GBP 5M | GBP 6M | GBP 6M | GBP 6M | GBP 25M |
| B-002 | SME administrative time savings | OPERATIONAL | GBP 0.5M | GBP 1.5M | GBP 2M | GBP 2M | GBP 1M | GBP 7M |
| B-003 | Departmental enquiry reduction | OPERATIONAL | GBP 0.2M | GBP 0.5M | GBP 0.8M | GBP 0.8M | GBP 0.7M | GBP 3M |
| **Total** | | | **GBP 2.7M** | **GBP 7M** | **GBP 8.8M** | **GBP 8.8M** | **GBP 7.7M** | **GBP 35M** |

**NPV** (3.5%): GBP 18M
**ROI**: 338%
**Payback**: 18 months

**Stakeholder Goals Met**: 80%

**Pros**:
- Personalised, relevant recommendations
- Pre-populated applications saving SME time
- Cross-departmental aggregation solving the core problem
- GOV.UK compliance satisfying GDS
- Mobile-first design reaching sole traders

**Cons**:
- Cross-departmental coordination required (10+ departments)
- GOV.UK One Login business account dependency
- Scheme data quality varies across departments
- Content ownership disputes possible

---

### Option 3: Standalone Business Support Platform

**Description**: Purpose-built platform outside GOV.UK with full CRM, AI chatbot, and integrated payment processing.

**Costs** (3-year): GBP 20M
**Benefits** (5-year): GBP 45M

**Recommendation**: **Reject** — GDS will not approve a standalone platform outside GOV.UK. Duplicating GOV.UK infrastructure is wasteful. The additional features (CRM, chatbot, payments) are not justified at SOBC stage.

---

# PART C: COMMERCIAL CASE

**Approach**: In-house GDS/DBT Digital development on GOV.UK platform.

**Key Contracts**:
- GOV.UK platform hosting: Existing GDS agreement
- Content design consultancy: GBP 0.5M via DOS
- Companies House API: Existing free API (rate limit upgrade may be needed)

---

# PART D: FINANCIAL CASE

| Year | Capital | Operational | Total |
|------|---------|-------------|-------|
| 2026-27 | GBP 3M | GBP 0.5M | GBP 3.5M |
| 2027-28 | GBP 1.5M | GBP 1M | GBP 2.5M |
| 2028-29 | GBP 0.5M | GBP 1.5M | GBP 2M |
| **Total** | **GBP 5M** | **GBP 3M** | **GBP 8M** |

**Funding Source**: DBT Business Environment budget.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Timeline**:
- Discovery: Q2 2026 (3 months) — SME user research, scheme landscape mapping
- Alpha: Q3-Q4 2026 (6 months) — eligibility engine prototype, 5-department pilot
- Private Beta: Q1-Q2 2027 (6 months) — 10 departments, 50,000 beta users
- Public Beta: Q3-Q4 2027 (6 months) — national launch, GDS assessment
- Live: Q1 2028

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Departmental resistance to data sharing | HIGH | HIGH | Ministerial mandate, cross-departmental MoU, Cabinet Office backing |
| GOV.UK One Login business readiness | MEDIUM | HIGH | Early engagement with GDS, fallback to Companies House auth |
| Scheme data quality varies | HIGH | MEDIUM | Standardised metadata schema, departmental data quality SLAs |
| HMRC content duplication concern | MEDIUM | MEDIUM | Deep-linking to HMRC.gov.uk, no content paraphrasing |
| SME adoption in disadvantaged areas | MEDIUM | HIGH | Non-digital channels (telephone, Growth Hubs), partnership with FSB/BCC |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-004-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals | `projects/004-small-business-support-portal/ARC-004-STKE-v1.0.md` |
| ARC-004-REQ-v1.0 | Requirements | SDG 8 Programme | Requirements | `projects/004-small-business-support-portal/ARC-004-REQ-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 1, 5, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Industrial Strategy | Policy | DBT | SME productivity | https://www.gov.uk/government/publications/industrial-strategy |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Small Business Support Portal
**Model**: Claude Opus 4.6
