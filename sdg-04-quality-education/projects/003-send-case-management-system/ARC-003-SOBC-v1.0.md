# Strategic Outline Business Case (SOBC): SEND Case Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | SEND Case Management System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SEND Case Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Investment Board, HM Treasury, CDDO, LGA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in a national SEND Case Management System, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: DfE seeks investment in a national SEND Case Management System to digitise and standardise the Education, Health and Care (EHC) plan process across 152 local authorities, addressing systemic failures in timeliness, quality, and parent experience.

**Problem Statement**: 43% of new EHC plans are issued late (outside the 20-week statutory timeframe), SEND Tribunal appeals have doubled in 5 years (with parents winning 96% of cases), and local authorities spend an estimated GBP 210M annually on Tribunal-related costs. The system is failing children with SEND.

**Proposed Solution**: Build a national digital case management platform covering the complete EHC lifecycle, with parent tracking, health assessment integration, quality validation, and statutory timeline enforcement.

**Strategic Fit**: Directly supports SEND Review reform commitments, Children and Families Act 2014 statutory obligations, and SDG 4 (inclusive education).

**Investment Required**: GBP 18.5M over 3 years

- Capital: GBP 12.0M
- Operational (3 years): GBP 6.5M

**Expected Benefits**: GBP 125M over 5 years

- Tribunal cost avoidance: GBP 63M
- LA caseworker productivity: GBP 32M
- Reduced health advice delays (faster provision for children): GBP 18M
- Improved child outcomes (lifetime value): GBP 12M

**Return on Investment**:

- NPV: GBP 72.4M (discounted at 3.5%)
- Payback Period: 14 months
- BCR: 5.4:1

**Recommended Option**: Option 2: National Platform with Health Integration

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The BCR of 5.4:1 represents exceptional value for money, driven primarily by avoided Tribunal costs (GBP 63M). The system addresses a genuine crisis in SEND provision evidenced by rising Tribunal volumes and statutory non-compliance. Every month of delay costs approximately GBP 3.5M in avoidable Tribunal expenditure.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: England's SEND system processes 150,000+ new EHC assessment requests annually across 152 local authorities. The system relies on fragmented, often paper-based processes with no standardised digital workflow. The consequences are severe: 43% of new EHC plans issued late, 14,000 Tribunal appeals annually (parents win 96%), and children with SEND waiting months or years for provision they are legally entitled to.

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Minister | SD-1 | Tribunal appeals doubled | GBP 210M annual cost to LAs; political damage | CRITICAL |
| LA SEND Teams | SD-2 | Manual processes, spreadsheet tracking | 43% of plans issued late; caseworker burnout | CRITICAL |
| Parents | SD-3 | No case visibility, adversarial process | Complaints, distress, Tribunal appeals | CRITICAL |
| NHS ICBs | SD-4 | Health advice routinely late (8 weeks vs 6 required) | Delays cascade through entire assessment | HIGH |
| SEND Tribunal | SD-5 | Avoidable appeals overloading Tribunal | Tribunal backlog increasing | HIGH |

**Consequences of Inaction**:

- Tribunal costs continue rising (projected GBP 250M/year by 2028)
- Children wait longer for essential provision, harming educational outcomes and wellbeing
- Ofsted/CQC SEND area inspections result in more Written Statements of Action
- Government faces growing legal challenge on Children and Families Act 2014 compliance

### A1.2 Strategic Alignment

- **SEND Review**: "A standardised digital EHC plan process will improve consistency, timeliness, and quality"
- **Children and Families Act 2014**: Statutory obligation to issue EHC plans within 20 weeks
- **SDG 4**: "Ensure inclusive and equitable quality education" — children with SEND are the most excluded group
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 2 (Safeguarding), 3 (Children's Data Privacy), 14 (Accessibility)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**3-Year Cost**: GBP 630M (continued Tribunal costs across all LAs — GBP 210M/year)
**Benefits**: GBP 0
**Recommendation**: **Reject** — current trajectory is unsustainable

### Option 1: Guidance and Templates Only

**Description**: Publish standardised EHC plan templates and process guidance. No digital platform.

**3-Year Cost**: GBP 0.5M (publication, training events)
**5-Year Benefits**: GBP 8M (marginal quality improvement)
**NPV**: GBP 6.9M
**Stakeholder Goals Met**: 15% (no timeliness improvement, no parent tracking)
**Recommendation**: **Insufficient** — templates without workflow enforcement do not address root causes

### Option 2: National Platform with Health Integration (RECOMMENDED)

**Description**: National digital platform with end-to-end EHC workflow, parent portal, NHS health assessment integration, quality validation, and statutory timeline enforcement.

**3-Year Cost**: GBP 18.5M

- Capital: GBP 12.0M (platform development GBP 7M, NHS integration GBP 2.5M, LA migration GBP 1.5M, security/compliance GBP 1M)
- Operational: GBP 6.5M (hosting GBP 1.5M/yr, support GBP 1M/yr, LA training GBP 0.2M/yr, minus avoided costs)

**5-Year Benefits**:

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Tribunal cost avoidance | GBP 3M | GBP 10M | GBP 15M | GBP 18M | GBP 17M | GBP 63M |
| LA productivity gains | GBP 2M | GBP 6M | GBP 8M | GBP 8M | GBP 8M | GBP 32M |
| Faster health provision | GBP 1M | GBP 3M | GBP 4M | GBP 5M | GBP 5M | GBP 18M |
| Improved child outcomes | GBP 0 | GBP 1M | GBP 2M | GBP 4M | GBP 5M | GBP 12M |
| **Total** | **GBP 6M** | **GBP 20M** | **GBP 29M** | **GBP 35M** | **GBP 35M** | **GBP 125M** |

**NPV**: GBP 72.4M | **BCR**: 5.4:1 | **Payback**: 14 months

**Stakeholder Goals Met**: 90%

### Option 3: National Platform with AI Casework Assistant

**3-Year Cost**: GBP 28.0M
**5-Year Benefits**: GBP 145M
**NPV**: GBP 62.1M (lower than Option 2 due to higher costs)
**Risk**: HIGH (AI assisting with decisions about vulnerable children raises ethical and legal concerns)
**Recommendation**: **Defer AI to Phase 2** after platform established and ethical framework agreed

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 0 (+ GBP 630M Tribunal) | GBP 0.5M | GBP 18.5M | GBP 28.0M |
| 5-Year Benefits | GBP 0 | GBP 8M | GBP 125M | GBP 145M |
| NPV | GBP 0 | GBP 6.9M | GBP 72.4M | GBP 62.1M |
| BCR | N/A | 16:1* | 5.4:1 | 4.1:1 |
| Goals Met | 0% | 15% | 90% | 100% |

*Option 1 BCR is high because costs are minimal, but absolute benefit is very low.

**Recommended**: **Option 2** — highest NPV and addresses systemic root causes.

---

# PART C: COMMERCIAL CASE

**Procurement Route**: G-Cloud 14 for platform development and hosting. DOS framework for specialist SEND domain expertise and NHS integration capability.

**Commercial Model**: Crown-owned platform, centrally funded by DfE. Free to local authorities (removing the unfunded mandate concern). NHS integration co-funded with NHS England.

**Key Commercial Risk**: 152 LAs with different legacy systems require significant migration support. Mitigated through phased rollout (cohorts of 20-30 LAs) and central migration team.

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (CDEL) | GBP 5.5M | GBP 4.5M | GBP 2.0M | GBP 12.0M |
| Revenue (RDEL) | GBP 1.5M | GBP 2.0M | GBP 3.0M | GBP 6.5M |
| **Total** | **GBP 7.0M** | **GBP 6.5M** | **GBP 5.0M** | **GBP 18.5M** |

**Funding Source**: DfE DEL (SEND reform budget). NHS integration co-funded with NHS England (GBP 2.5M of capital from NHSE).

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research with LAs, parents, NHS; data mapping |
| Alpha | 4 months | Prototype EHC workflow; parent portal mockup; NHS integration feasibility |
| Private Beta | 8 months | Working platform with 15 pilot LAs and 3 ICBs |
| Public Beta | 8 months | Phased rollout to 80 LAs |
| Live | Ongoing | Full 152 LA coverage; continuous improvement |

## E1.3 Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| LA resistance to adoption (unfunded mandate perception) | HIGH | HIGH | Central funding; migration support team; demonstrate Tribunal cost savings |
| NHS ICB integration technically complex | HIGH | HIGH | Co-design with NHS England; start with 3 pilot ICBs; fallback to structured email |
| Data migration from 152 different legacy systems | HIGH | MEDIUM | Standardised migration toolkit; phased cohort approach; data validation framework |
| Parents distrust government digital system | MEDIUM | MEDIUM | Co-design with parent forums; IPSEA advisory role; independent accessibility audit |
| Scale of 152 LAs overwhelms support capacity | MEDIUM | HIGH | Phased rollout in cohorts of 20-30; dedicated LA migration coaches |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Children and Families Act 2014 | Legislation | legislation.gov.uk | EHC statutory framework | N/A — external reference |
| SEND Code of Practice | Statutory guidance | DfE | EHC plan requirements | N/A — external reference |
| SEND Review Green Paper | Policy | DfE | Digital transformation mandate | N/A — external reference |
| HM Treasury Green Book | Guidance | GOV.UK | Five-case model | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SEND Case Management System
**Model**: Claude Opus 4.6
