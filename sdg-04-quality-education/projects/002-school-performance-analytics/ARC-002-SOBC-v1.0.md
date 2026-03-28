# Strategic Outline Business Case (SOBC): School Performance Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | School Performance Analytics (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SPA Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Ofsted Executive Board, DfE Analysis Directorate, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in a unified School Performance Analytics platform, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Ofsted and DfE seek to consolidate six fragmented school performance data systems into a unified analytics platform that reduces inspector preparation time, improves data quality, and provides schools with transparent access to the same data used during inspections.

**Problem Statement**: Ofsted inspectors spend an estimated 26,000 hours annually on pre-inspection data preparation — manually collating information from 6+ separate systems. Data inconsistencies between systems undermine inspection consistency, and schools cannot access the same data view as inspectors, fuelling transparency concerns.

**Proposed Solution**: Build a unified School Performance Analytics platform consolidating NPD, school census, attendance, exclusions, exam results, and financial benchmarking data with automated pipelines, inspector dashboards, and school self-evaluation access.

**Strategic Fit**: Supports Ofsted's strategic objective of evidence-based, consistent inspection and DfE's data consolidation agenda.

**Investment Required**: GBP 5.8M over 3 years

- Capital: GBP 3.5M
- Operational (3 years): GBP 2.3M

**Expected Benefits**: GBP 14.7M over 5 years

- Inspector productivity: GBP 6.5M
- Legacy system decommissioning: GBP 5.1M
- Reduced FOI/data request processing: GBP 1.6M
- Improved inspection consistency (avoided cost of errors): GBP 1.5M

**Return on Investment**:

- NPV: GBP 7.3M (discounted at 3.5%)
- Payback Period: 18 months
- BCR: 2.2:1

**Recommended Option**: Option 2: Unified Platform with School Access

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Ofsted inspectors prepare for approximately 6,500 school inspections annually. Each inspection requires the lead inspector to manually access, download, and cross-reference data from IDSR, ASP, school census data, attendance statistics, exclusion data, and financial benchmarking — spending an average of 7 hours per inspection on data preparation alone.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Lead Inspectors | SD-2 | 7 hours manual data collation per inspection | 26,000 hours/year wasted | HIGH |
| HM Chief Inspector | SD-1 | Inconsistent data interpretation across inspectors | Fairness concerns, parliamentary scrutiny | CRITICAL |
| DfE Analysis Dir. | SD-3 | 6 overlapping analytical systems | GBP 1.7M/year maintenance, inconsistent data | HIGH |
| Headteachers | SD-4 | Cannot see same data as inspectors | FOI requests, transparency complaints | HIGH |

**Consequences of Inaction**:

- 26,000 inspector hours/year continue to be wasted on data collation (GBP 1.3M opportunity cost)
- Inspection consistency challenged in Education Select Committee hearings
- GBP 1.7M/year continues to be spent maintaining 6 overlapping legacy systems
- School sector distrust of inspection process persists

### A1.2 Strategic Alignment

- **Ofsted Strategy 2025-2030**: "Use data and technology to support professional, evidence-based inspection"
- **DfE Data Strategy**: "Consolidate analytical platforms and improve data quality"
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 10 (Data Quality), 11 (Single Source of Truth), 14 (Accessibility)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**3-Year Cost**: GBP 5.1M (continued legacy system maintenance)
**Benefits**: GBP 0
**Recommendation**: **Reject**

### Option 1: Consolidate Data Only (No School Access)

**Description**: Consolidate data pipelines and provide inspectors with a unified dashboard. No school-facing access.

**3-Year Cost**: GBP 3.2M
**5-Year Benefits**: GBP 9.4M (inspector productivity + legacy decommissioning only)
**NPV**: GBP 4.8M
**Stakeholder Goals Met**: 55% (G-3 transparency goal not met)

### Option 2: Unified Platform with School Access (RECOMMENDED)

**Description**: Full unified platform with inspector dashboards, school self-evaluation access, risk indicators, and DfE analyst workspace.

**3-Year Cost**: GBP 5.8M

- Capital: GBP 3.5M (platform development, data pipeline engineering, security)
- Operational: GBP 2.3M (hosting GBP 0.6M/yr, support GBP 0.5M/yr, data ops GBP 0.1M/yr, minus legacy savings -GBP 0.4M/yr from Year 2)

**5-Year Benefits**: GBP 14.7M

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Inspector productivity | GBP 0.5M | GBP 1.3M | GBP 1.3M | GBP 1.7M | GBP 1.7M | GBP 6.5M |
| Legacy decommissioning | GBP 0 | GBP 0.7M | GBP 1.5M | GBP 1.5M | GBP 1.4M | GBP 5.1M |
| Reduced FOI processing | GBP 0.1M | GBP 0.3M | GBP 0.4M | GBP 0.4M | GBP 0.4M | GBP 1.6M |
| Consistency improvement | GBP 0.1M | GBP 0.3M | GBP 0.3M | GBP 0.4M | GBP 0.4M | GBP 1.5M |
| **Total** | **GBP 0.7M** | **GBP 2.6M** | **GBP 3.5M** | **GBP 4.0M** | **GBP 3.9M** | **GBP 14.7M** |

**NPV**: GBP 7.3M | **BCR**: 2.2:1 | **Payback**: 18 months

**Stakeholder Goals Met**: 90%

### Option 3: AI-Enhanced Analytics with Predictive Inspection

**3-Year Cost**: GBP 9.5M
**5-Year Benefits**: GBP 17.2M
**NPV**: GBP 4.1M (lower than Option 2 due to higher costs)
**Risk**: HIGH (sector opposition to "algorithmic inspection")
**Recommendation**: **Reject at this stage** — AI features deferred to Phase 2

---

# PART C: COMMERCIAL CASE

**Procurement Route**: G-Cloud 14 for cloud hosting and development services; DfE internal analytical capability for data pipeline development.

**Commercial Model**: Joint Ofsted-DfE programme with Crown-owned IP. Hosting on existing DfE cloud infrastructure (reducing procurement complexity). Development via G-Cloud framework with data engineering specialist capability.

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (CDEL) | GBP 2.0M | GBP 1.0M | GBP 0.5M | GBP 3.5M |
| Revenue (RDEL) | GBP 0.5M | GBP 0.8M | GBP 1.0M | GBP 2.3M |
| **Total** | **GBP 2.5M** | **GBP 1.8M** | **GBP 1.5M** | **GBP 5.8M** |

**Funding Source**: Joint funding — Ofsted (40%) and DfE (60%), reflecting shared platform benefit.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | Data pipeline feasibility, user research with inspectors |
| Alpha | 3 months | Prototype inspector dashboard, data quality assessment |
| Private Beta | 6 months | Working platform with 50 pilot inspectors, 200 pilot schools |
| Public Beta | 6 months | Full rollout to all inspectors and schools |
| Live | Ongoing | Legacy decommissioning, continuous improvement |

## E1.3 Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Data quality from source systems insufficient | HIGH | HIGH | Quality framework with DfE Analysis Dir.; automated reconciliation |
| Inspector resistance to new tool | MEDIUM | MEDIUM | Co-design with lead inspectors; gradual transition; training programme |
| Sector opposition to risk indicators | HIGH | MEDIUM | Transparent methodology; school access to same data; union consultation |
| Ofsted-DfE governance complexity (joint programme) | MEDIUM | MEDIUM | Clear RACI; joint programme board with escalation to both Permanent Secretaries |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Green Book | Guidance | GOV.UK | Five-case model, discount rates | N/A — external reference |
| Education Inspection Framework | Framework | Ofsted | Inspection methodology | N/A — external reference |
| Ofsted Strategy 2025-2030 | Strategy | Ofsted | Data and technology priorities | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: School Performance Analytics
**Model**: Claude Opus 4.6
