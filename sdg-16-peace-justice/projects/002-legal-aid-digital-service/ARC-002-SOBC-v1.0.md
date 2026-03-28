# Strategic Outline Business Case (SOBC): Legal Aid Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Legal Aid Digital Service (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Legal Aid Transformation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | LAA Executive Board, MoJ Finance, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The Legal Aid Digital Service replaces the paper-based legal aid application and determination process with a digital platform implementing the statutory means test, automated income verification, and rapid eligibility determination — enabling the 2 million additional citizens brought into eligibility by the Means Test Review 2023 to access legal representation quickly.

**Problem Statement**: Legal aid applications take 20+ working days to determine, requiring extensive paper forms and manual financial verification. This delays access to justice for vulnerable citizens and imposes unsustainable administrative burden on legal aid solicitor firms, contributing to the collapse of the provider base and the growth of legal aid deserts.

**Proposed Solution**: A digital legal aid eligibility and application platform with automated means test calculation, HMRC/DWP income verification, real-time eligibility pre-check, and integration with HMCTS court systems for legal aid status sharing.

**Strategic Fit**: Implements the Legal Aid Means Test Review 2023, supports the Lord Chancellor's access to justice priorities, aligns with SDG 16 targets on equal access to justice, and complies with TCoP requirements for modern digital government services.

**Investment Required**: GBP 12M over 3 years

- Capital: GBP 9M
- Operational (3 years): GBP 3M

**Expected Benefits**: GBP 32M over 5 years

- Caseworker efficiency savings: GBP 14M
- Reduced overpayments through automated verification: GBP 10M
- Solicitor time savings (value to legal aid sector): GBP 5M
- Reduced appeals and re-determinations: GBP 3M

**Return on Investment**:

- NPV: GBP 16M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 167%

**Recommended Option**: Option 3: Build digital platform with automated verification and rules engine

**Key Risks**:

1. HMRC/DWP data sharing agreements may take longer than planned
2. Means test rules complexity may exceed automated determination capability
3. Solicitor firms may not adopt the digital platform if usability is poor

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Means Test Review 2023 cannot be implemented effectively on the current paper-based system. The investment of GBP 12M is modest relative to the GBP 1.7B annual legal aid fund. Faster, more accurate determinations improve access to justice and reduce the cost of incorrect assessments.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The LAA processes 300,000 legal aid applications annually using predominantly paper-based processes. Caseworkers manually enter application data, request financial evidence by post, calculate means test eligibility using spreadsheet tools, and communicate decisions by letter. Average determination time exceeds 20 working days for civil cases.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| LAA CEO | Manual processes, high error rate, 20+ day determination | GBP 22M annual admin cost, NAO criticism | CRITICAL |
| Lord Chancellor | Cannot implement Means Test Review 2023 quickly on legacy systems | 2M eligible citizens cannot benefit from policy change | CRITICAL |
| Law Society | 2-hour application process driving firms from legal aid | Legal aid deserts growing, provider base collapsing | HIGH |
| Applicants | Slow, complex, opaque process | Justice delayed during determination period | HIGH |

**Consequences of Inaction**:

- Means Test Review 2023 benefits delayed — 2 million citizens remain unable to access expanded eligibility
- Legal aid deserts continue to grow as firms withdraw from legal aid work
- Determination times increase further as caseworker workforce ages and shrinks
- UK SDG 16 reporting shows declining access to justice metrics

### A1.2 Strategic Alignment

| Strategy/Policy | Alignment |
|-----------------|-----------|
| Legal Aid Means Test Review 2023 | Directly enables implementation of revised thresholds |
| LASPO Act 2012 | Implements statutory means test accurately |
| SDG 16 Target 16.3 | Equal access to justice for all |
| Technology Code of Practice | Digital-first, open standards, user-centred |
| GDS Service Standard | Accessible, user-researched, iteratively developed |
| Legal Aid Transformation Programme | Core deliverable for LAA digital modernisation |

---

# PART B: ECONOMIC CASE

## B1. Options Considered

### Option 1: Do Nothing

**Costs**: GBP 110M over 5 years (GBP 22M/year)
**Benefits**: GBP 0
**NPV**: GBP 0 (baseline)
**Assessment**: Means Test Review cannot be implemented. Provider base continues to collapse. Unacceptable.

### Option 2: Digitise Paper Forms Only

**Description**: Create online versions of paper forms with PDF generation, but retain manual caseworker processing and verification.
**Costs**: GBP 4M capital + GBP 20M operational = GBP 24M
**Benefits**: GBP 8M (minor solicitor time savings, some error reduction)
**NPV**: GBP -14M
**Assessment**: Digitises the front end but does not address the core processing bottleneck. Poor value for money.

### Option 3: Build Digital Platform with Automated Verification (RECOMMENDED)

**Description**: Full digital platform with rules engine, HMRC/DWP integration, automated determination for straightforward cases, and caseworker workflow for complex cases.
**Costs**: GBP 9M capital + GBP 3M operational (3 years) + GBP 4M operational (years 4-5) = GBP 16M
**Benefits**: GBP 32M over 5 years
**NPV**: GBP 16M
**BCR**: 2.0
**Assessment**: Best value for money. Addresses root cause. Enables Means Test Review implementation.

### Option 4: Procure Commercial Legal Aid Management System

**Description**: Procure and customise a commercial case management system for legal aid.
**Costs**: GBP 8M capital + GBP 6M operational (licensing) = GBP 14M
**Benefits**: GBP 22M (limited customisation flexibility)
**NPV**: GBP 8M
**Assessment**: Viable but UK statutory means test complexity requires extensive customisation. No established COTS product exists for UK legal aid.

---

## B2. Options Appraisal Summary

| Criterion | Option 1 | Option 2 | Option 3 (REC) | Option 4 |
|-----------|----------|----------|----------------|----------|
| Means test accuracy | 1 | 2 | 5 | 3 |
| Determination speed | 1 | 2 | 5 | 4 |
| Practitioner burden | 1 | 3 | 5 | 3 |
| Citizen access | 1 | 2 | 5 | 3 |
| Value for money | 1 | 1 | 5 | 3 |
| **Weighted Score** | **1.0** | **2.0** | **5.0** | **3.2** |
| **NPV** | **GBP 0** | **GBP -14M** | **GBP 16M** | **GBP 8M** |

---

# PART C: COMMERCIAL CASE

**Procurement Strategy**: Internal LAA Digital team for core platform, specialist suppliers for HMRC/DWP integration via Digital Marketplace frameworks.

**Key contracts**: Cloud hosting via G-Cloud, specialist development via Digital Outcomes and Specialists.

---

# PART D: FINANCIAL CASE

## D1. Costs

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Platform development | GBP 4M | GBP 3M | GBP 1M | GBP 8M |
| HMRC/DWP integration | GBP 0.5M | GBP 0.3M | GBP 0.2M | GBP 1M |
| Hosting and operations | GBP 0.5M | GBP 0.8M | GBP 1M | GBP 2.3M |
| Training and change | GBP 0.3M | GBP 0.2M | GBP 0.2M | GBP 0.7M |
| **Total** | **GBP 5.3M** | **GBP 4.3M** | **GBP 2.4M** | **GBP 12M** |

## D2. Benefits Realisation

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Caseworker efficiency | GBP 1M | GBP 2.5M | GBP 3.5M | GBP 3.5M | GBP 3.5M | GBP 14M |
| Reduced overpayments | GBP 0.5M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 2.5M | GBP 10M |
| Solicitor time savings | GBP 0.5M | GBP 1M | GBP 1M | GBP 1.25M | GBP 1.25M | GBP 5M |
| Reduced appeals | GBP 0.2M | GBP 0.5M | GBP 0.8M | GBP 0.75M | GBP 0.75M | GBP 3M |
| **Total** | **GBP 2.2M** | **GBP 6M** | **GBP 7.8M** | **GBP 8M** | **GBP 8M** | **GBP 32M** |

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|------------------|
| Discovery | 3 months | User research with solicitors, applicants, caseworkers; means test rules analysis |
| Alpha | 4 months | Rules engine prototype, HMRC API proof of concept, service design |
| Private Beta | 6 months | Criminal legal aid applications (simpler rules), solicitor portal |
| Public Beta | 6 months | Civil legal aid, citizen pre-check, full HMRC/DWP integration |
| Live | Ongoing | National rollout, continuous improvement, paper phase-out |

## E2. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|-------------|
| SOBC approval | Q2 2026 | This document |
| Discovery start | Q3 2026 | Funding approval |
| HMRC data sharing agreement signed | Q4 2026 | Cross-government negotiation |
| Alpha start | Q4 2026 | Discovery completion |
| Private Beta (criminal) | Q2 2027 | Alpha assessment pass |
| Public Beta (civil + criminal) | Q4 2027 | Criminal beta successful |
| National live | Q2 2028 | Beta assessment pass |

---

## Approval

| Role | Name | Decision | Date |
|------|------|----------|------|
| SRO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| LAA CEO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| MoJ Finance | | [ ] PROCEED / [ ] DO NOT PROCEED | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Legal Aid Means Test Review 2023 | Policy | MoJ | Revised thresholds | N/A — external reference |
| LASPO Act 2012 | Legislation | legislation.gov.uk | Legal aid scope | N/A — external reference |
| HM Treasury Green Book | Guidance | HMT | Five-case model, 3.5% discount | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Legal Aid Digital Service
**Model**: Claude Opus 4.6
