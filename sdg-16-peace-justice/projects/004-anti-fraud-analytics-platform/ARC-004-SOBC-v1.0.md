# Strategic Outline Business Case (SOBC): Anti-Fraud Analytics Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Anti-Fraud Analytics Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Government Counter Fraud Function, Cabinet Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office, HM Treasury, HMRC, DWP, NCA, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The Anti-Fraud Analytics Platform enables cross-government fraud detection by securely sharing and analysing data across departments to identify fraud patterns invisible to any single department — targeting the estimated GBP 33-58 billion annual fraud and error losses across government.

**Problem Statement**: Government departments detect fraud in isolation, unable to see cross-departmental patterns. Organised fraud groups exploit this gap, using fabricated identities and multi-scheme exploitation across tax, benefits, grants, and procurement. COVID-19 emergency schemes exposed this vulnerability with GBP 4.9 billion in Bounce Back Loan fraud alone.

**Proposed Solution**: A secure cross-government data sharing and analytics platform with identity resolution, pattern detection, and intelligence-grade referral capabilities, operating within a clear legal framework (Digital Economy Act 2017) and with full ICO engagement.

**Strategic Fit**: Delivers the Government Counter Fraud Function Strategy, supports SDG 16.5 (substantially reduce corruption and bribery), implements the Counter Fraud Functional Standard (GovS 013), and responds to NAO/PAC recommendations for improved cross-government fraud detection.

**Investment Required**: GBP 40M over 3 years

- Capital: GBP 30M
- Operational (3 years): GBP 10M

**Expected Benefits**: GBP 500M+ over 5 years

- Fraud prevented through deterrence and pre-payment checks: GBP 250M
- Fraud detected and recovered through cross-government matching: GBP 200M
- Reduced investigation costs through targeted analytics: GBP 30M
- Reduced duplicate fraud investigation across departments: GBP 20M

**Return on Investment**:

- NPV: GBP 380M (discounted at 3.5%)
- Payback Period: 8 months
- ROI: 1,150%

**Recommended Option**: Option 3: Build secure cross-government analytics platform

**Key Risks**:

1. Data sharing agreements delayed by legal/privacy negotiations
2. False positive rate undermining analyst trust and citizen rights
3. Algorithmic bias in fraud scoring
4. Security breach exposing cross-government fraud intelligence

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The GBP 33-58 billion annual fraud loss dwarfs the GBP 40M investment. Even detecting 0.3% of estimated losses would pay for the platform 10 times over. COVID-era fraud creates urgent political and fiscal imperative. Cross-government data sharing is the only way to identify organised fraud exploiting departmental silos. The Digital Economy Act 2017 provides the legal framework. ICO engagement from day one mitigates privacy risks.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Each department operates fraud detection in isolation. HMRC detects tax fraud. DWP detects benefits fraud. BEIS/DBT investigates COVID loan fraud. No central capability exists to match identities and transaction patterns across departments.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact |
|-------------|------------|--------|
| Minister | GBP 33-58B annual fraud losses, GBP 4.9B COVID loan fraud | Parliamentary/media criticism, public trust |
| HMRC/DWP | Cannot see cross-departmental exploitation patterns | Organised fraud undetected |
| NAO/PAC | Repeated recommendations for cross-govt approach unimplemented | Continued audit criticism |
| NCA | Referrals lack cross-departmental intelligence | Organised fraud networks not disrupted |

**Consequences of Inaction**:

- GBP 33-58 billion annual fraud losses continue unchecked
- Organised fraud groups continue to exploit departmental silos
- COVID-era fraud recovery efforts hampered by lack of cross-matching capability
- UK fails SDG 16.5 targets on reducing corruption

### A1.2 Strategic Alignment

| Strategy/Policy | Alignment |
|-----------------|-----------|
| Government Counter Fraud Function Strategy | Core capability — cross-government analytics |
| Counter Fraud Functional Standard (GovS 013) | Mandates cross-government cooperation |
| SDG 16.5 | Substantially reduce corruption and bribery |
| Spending Review outcomes | Protecting public money |
| NAO recommendations | Implements repeated recommendations |

---

# PART B: ECONOMIC CASE

## B1. Options

### Option 1: Do Nothing

**Costs**: GBP 0 incremental
**Benefits**: GBP 0
**Assessment**: GBP 33-58B annual losses continue. NAO criticism escalates. Unacceptable.

### Option 2: Bilateral Data Sharing Agreements

**Description**: Expand existing bilateral agreements between departments for specific fraud types (e.g., HMRC-DWP income matching, DWP-BEIS COVID loan checks).
**Costs**: GBP 8M over 5 years
**Benefits**: GBP 80M (limited to bilateral matches)
**NPV**: GBP 65M
**Assessment**: Useful but fundamentally limited. Cannot detect network fraud spanning 3+ departments. Does not scale.

### Option 3: Build Secure Cross-Government Analytics Platform (RECOMMENDED)

**Description**: Central analytics platform with secure data ingestion from 10+ departments, identity resolution, pattern detection, and referral workflow.
**Costs**: GBP 30M capital + GBP 10M operational (3 years) + GBP 12M (years 4-5) = GBP 52M
**Benefits**: GBP 500M+ over 5 years
**NPV**: GBP 380M
**BCR**: 9.6
**Assessment**: Transformative capability. Addresses the fundamental problem of departmental silos. Massive return on investment. Requires careful privacy safeguards.

### Option 4: Procure Commercial Fraud Analytics Platform

**Description**: Procure an enterprise fraud analytics platform and deploy within government.
**Costs**: GBP 25M capital + GBP 20M licensing = GBP 45M
**Benefits**: GBP 350M (limited by vendor platform constraints)
**NPV**: GBP 260M
**Assessment**: Viable but raises significant data sovereignty concerns — government fraud intelligence handled by a commercial vendor. Security classification constraints may be incompatible with vendor operating models.

---

## B2. Options Appraisal Summary

| Criterion | Option 1 | Option 2 | Option 3 (REC) | Option 4 |
|-----------|----------|----------|----------------|----------|
| Cross-dept detection capability | 1 | 3 | 5 | 4 |
| Privacy compliance | 5 (no data shared) | 3 | 4 | 3 |
| Data sovereignty | 5 | 5 | 5 | 2 |
| Scalability | 1 | 2 | 5 | 4 |
| Value for money | 1 | 3 | 5 | 4 |
| **Weighted Score** | **2.2** | **3.0** | **4.8** | **3.4** |
| **5-year NPV** | **GBP 0** | **GBP 65M** | **GBP 380M** | **GBP 260M** |

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Platform development | GBP 12M | GBP 10M | GBP 3M | GBP 25M |
| Data sharing and legal | GBP 2M | GBP 1.5M | GBP 0.5M | GBP 4M |
| Security infrastructure | GBP 1M | GBP 0 | GBP 0 | GBP 1M |
| Operations and hosting | GBP 1.5M | GBP 2.5M | GBP 3M | GBP 7M |
| Training and onboarding | GBP 1M | GBP 1M | GBP 1M | GBP 3M |
| **Total** | **GBP 17.5M** | **GBP 15M** | **GBP 7.5M** | **GBP 40M** |

## Benefits Realisation

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Fraud prevented | GBP 10M | GBP 40M | GBP 60M | GBP 70M | GBP 70M | GBP 250M |
| Fraud detected/recovered | GBP 5M | GBP 30M | GBP 50M | GBP 57.5M | GBP 57.5M | GBP 200M |
| Investigation efficiency | GBP 2M | GBP 5M | GBP 8M | GBP 7.5M | GBP 7.5M | GBP 30M |
| Reduced duplication | GBP 1M | GBP 3M | GBP 5M | GBP 5.5M | GBP 5.5M | GBP 20M |
| **Total** | **GBP 18M** | **GBP 78M** | **GBP 123M** | **GBP 140.5M** | **GBP 140.5M** | **GBP 500M** |

---

# PART E: MANAGEMENT CASE

| Phase | Duration | Key Deliverables |
|-------|----------|------------------|
| Discovery | 3 months | Legal framework, ICO engagement, departmental data mapping |
| Alpha | 6 months | Identity resolution PoC with HMRC-DWP data, DPIA, security architecture |
| Private Beta | 9 months | Platform with 5 departments, initial fraud detection, NCA referral pilot |
| Public Beta | 6 months | 10+ departments, full analytics, operational dashboards |
| Live | Ongoing | Continuous improvement, model refinement, new department onboarding |

| Milestone | Date |
|-----------|------|
| SOBC approval | Q2 2026 |
| ICO engagement start | Q3 2026 |
| First DPIA approved | Q4 2026 |
| Alpha PoC with HMRC-DWP | Q1 2027 |
| Private Beta (5 depts) | Q3 2027 |
| First GBP 10M fraud detected | Q4 2027 |
| 10+ departments live | Q1 2028 |
| GBP 100M cumulative detection | Q2 2028 |

---

## Approval

| Role | Name | Decision | Date |
|------|------|----------|------|
| SRO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| Cabinet Office Perm Sec | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| HM Treasury | | [ ] PROCEED / [ ] DO NOT PROCEED | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Government Counter Fraud Function Strategy | Strategy | Cabinet Office | Cross-government fraud objectives | N/A — external reference |
| Counter Fraud Functional Standard (GovS 013) | Standard | Cabinet Office | Departmental counter fraud obligations | N/A — external reference |
| Digital Economy Act 2017 Part 5 | Legislation | legislation.gov.uk | Data sharing gateways | N/A — external reference |
| NAO Fraud Landscape Reports | Report | NAO | GBP 33-58B estimate, COVID fraud | N/A — external reference |
| HM Treasury Green Book | Guidance | HMT | Five-case model, 3.5% discount | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Anti-Fraud Analytics Platform
**Model**: Claude Opus 4.6
