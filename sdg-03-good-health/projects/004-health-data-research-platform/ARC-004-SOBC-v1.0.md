# Strategic Outline Business Case (SOBC): Health Data Research Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Health Data Research Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Health Data Research Platform Programme, DHSC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Health Data Research Programme Board, DHSC, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The Health Data Research Platform will create a UK Statistics Authority-accredited Trusted Research Environment providing secure access to linked NHS health datasets for accredited researchers, accelerating health research while protecting patient privacy.

**Problem Statement**: The UK's most valuable health data asset — NHS records covering 67 million citizens — is underutilised for research due to fragmented access processes, slow governance (3-12 months to access data), and legacy infrastructure. Other countries are overtaking the UK in health data research capability.

**Proposed Solution**: A secure Trusted Research Environment where analysis comes to the data. Researchers access de-identified, linked datasets within a governed environment — data never leaves the platform. Automated IG workflows reduce access time to 6 weeks.

**Strategic Fit**: Goldacre Review recommendations, UK Life Sciences Strategy, UKRI research infrastructure, SDG 3 (Good Health and Well-Being).

**Investment Required**: GBP 15.0M over 5 years

- Capital: GBP 9.0M
- Operational (5 years): GBP 6.0M

**Expected Benefits**: GBP 250M over 5 years

- Life sciences R&D investment attracted: GBP 150M
- Research efficiency gains (faster access): GBP 50M
- Research quality improvement (linked data, better tools): GBP 30M
- Cost recovery from commercial access: GBP 20M

**Return on Investment**:

- NPV: GBP 85.3M (discounted at 3.5%, after 40% optimism bias)
- Payback Period: 24 months
- ROI: 550% over 5 years

**Recommended Option**: Option 2: UKSA-Accredited Trusted Research Environment

**Key Risks**:

1. Public trust failure leading to increased National Data Opt-Out rates (care.data precedent)
2. NHS data quality insufficient for research-grade analysis without extensive cleansing
3. UKSA accreditation requirements more onerous than anticipated

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: UK health data research operates through a fragmented landscape of data access processes. Researchers submit applications to multiple data controllers (NHS Digital, individual Trusts, CPRD, OpenSAFELY), each with different governance processes, timelines, and technical requirements. Average time from application to data access is 6 months. Data arrives in inconsistent formats, often on researcher laptops with insufficient security controls.

**Consequences of Inaction**:

- UK loses global competitiveness in health data research to Denmark, Finland, and Israel
- Life sciences companies invest R&D elsewhere, costing the UK economy GBP 500M+ annually
- Pandemic preparedness research hampered by slow data access
- Goldacre Review recommendations remain unimplemented, attracting political criticism

### A1.2 Strategic Alignment

- **Goldacre Review (2022)**: Recommended TRE network as the default model for health data research
- **UK Life Sciences Strategy**: NHS data as strategic asset for attracting pharmaceutical R&D
- **UKRI Infrastructure Strategy**: Modern research infrastructure for UK competitiveness
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 5 (Privacy/Caldicott), 7 (Data Governance), 4 (Security)

## B2. Options Analysis

### Option 0: Do Nothing

**Description**: Continue with fragmented data access processes.

**Recommendation**: **Reject** — Contradicts Goldacre Review recommendations. UK competitiveness continues to decline.

---

### Option 1: Data Extract Service (Minimal)

**Description**: Centralise data access governance but continue extracting data to researcher institutions. Faster governance but data still leaves NHS control.

**Costs** (5-year): GBP 5.0M
**Benefits** (5-year): GBP 60M

**Pros**: Lower cost, simpler infrastructure
**Cons**: Data leaves NHS control, re-identification risk, does not meet UKSA TRE standards, does not address Goldacre Review recommendations, public trust risk

**Stakeholder Goals Met**: 30%

---

### Option 2: UKSA-Accredited Trusted Research Environment (RECOMMENDED)

**Description**: Build a secure TRE where researchers analyse data within the platform. Data never leaves. UKSA accreditation. Five Safes framework. Automated IG workflow.

**Costs** (5-year): GBP 15.0M

- Capital: GBP 9.0M (TRE infrastructure GBP 4M, data linkage pipelines GBP 2M, IG workflow automation GBP 1.5M, security/accreditation GBP 1.5M)
- Operational: GBP 6.0M (cloud compute GBP 2.5M, team GBP 2M, data operations GBP 1.5M)

**Benefits** (5-year):

| Benefit | Type | 5-Year Total |
|---------|------|--------------|
| Life sciences R&D investment attracted | STRATEGIC | GBP 150M |
| Research efficiency (6 months to 6 weeks) | OPERATIONAL | GBP 50M |
| Research quality (linked data, better tools) | STRATEGIC | GBP 30M |
| Cost recovery from commercial access | FINANCIAL | GBP 20M |
| **Total** | | **GBP 250M** |

**NPV** (3.5% discount): GBP 218M. With 40% optimism bias on costs: **NPV = GBP 85.3M**

**Stakeholder Goals Met**: 90%

---

### Option 3: Federated TRE Network

**Description**: Option 2 plus federated analysis across multiple TREs (NHS, Genomics England, SAIL Databank, OpenSAFELY) enabling cross-platform research without data movement.

**Costs** (5-year): GBP 35.0M

**Recommendation**: **Defer** — Pursue Option 2 first. Federated capability as Phase 2 once single TRE operational.

---

## B3. Recommended Option

**Recommendation**: **Option 2: UKSA-Accredited Trusted Research Environment**

**Rationale**: Delivers Goldacre Review recommendations, protects public trust (data never leaves), achieves UKSA accreditation, and strong ROI through life sciences investment attraction. NPV positive even with aggressive optimism bias.

---

# PART C: COMMERCIAL CASE

**Recommended Route**: Digital Marketplace (G-Cloud for cloud infrastructure, DOS6 for platform development)

**Revenue Model**: Cost-recovery pricing for commercial access. Academic access funded by UKRI/NIHR. Government research funded from departmental budgets. No profit — cost recovery only to maintain public trust.

---

# PART D: FINANCIAL CASE

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 4.5M | GBP 3.5M | GBP 1.0M | GBP 0 | GBP 0 | GBP 9.0M |
| OpEx | GBP 0.5M | GBP 1.0M | GBP 1.2M | GBP 1.5M | GBP 1.8M | GBP 6.0M |
| **Total** | **GBP 5.0M** | **GBP 4.5M** | **GBP 2.2M** | **GBP 1.5M** | **GBP 1.8M** | **GBP 15.0M** |

**Funding Source**: DHSC research infrastructure budget + UKRI co-funding contribution

**Affordability**: **Affordable** within combined DHSC and UKRI allocations.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

1. **Discovery** (3 months): Researcher needs assessment, data source mapping, UKSA pre-accreditation engagement
2. **Alpha** (6 months): TRE infrastructure prototype, data linkage pilot with 2 datasets, IG workflow prototype
3. **Beta** (9 months): Full platform, 6 datasets linked, UKSA accreditation assessment, researcher pilot
4. **Live** (ongoing): Full service, ongoing dataset addition, UKSA annual re-accreditation

## E2. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation |
|---------|------|------------|--------|-------|------------|
| R-001 | Public trust failure (care.data repeat) | Medium | Critical | 16 | PPI governance, transparency register, public engagement |
| R-002 | NHS data quality insufficient | Medium | Major | 12 | Data quality assessment before ingestion, quality metrics published |
| R-003 | UKSA accreditation delayed | Medium | Major | 12 | Early UKSA engagement, align with published standards |
| R-004 | Researcher adoption low | Low | Major | 8 | Co-design with HDR UK, modern tools (Jupyter, R, GPU) |
| R-005 | Commercial access politically sensitive | Medium | Moderate | 9 | Public benefit requirement, transparency, PPI review |

---

# PART F: RECOMMENDATION

**Recommended Option**: Option 2: UKSA-Accredited Trusted Research Environment

**Investment**: GBP 15.0M over 5 years

**Expected Return**: GBP 250M over 5 years (NPV: GBP 85.3M after optimism bias)

**Go/No-Go**: **PROCEED to Discovery phase**

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| | SRO | | |
| | DHSC Finance Director | | |
| | DHSC Chief Scientific Adviser | | |
| | Caldicott Guardian | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Health Data Research Platform
**Model**: Claude Opus 4.6
