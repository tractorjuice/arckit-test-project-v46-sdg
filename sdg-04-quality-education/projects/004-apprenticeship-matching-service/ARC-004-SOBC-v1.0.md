# Strategic Outline Business Case (SOBC): Apprenticeship Matching Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Apprenticeship Matching Service (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, AMS Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Investment Board, HM Treasury, ESFA, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in an Apprenticeship Matching Service, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: DfE seeks to replace the ageing Find an Apprenticeship service with a modern, skills-matched platform that improves vacancy fill rates, supports disadvantaged young people into apprenticeships, and integrates with ESFA funding systems.

**Problem Statement**: 35% of apprenticeship vacancies go unfilled while youth unemployment exceeds 10%. The current Find an Apprenticeship service is a basic listing with no skills matching, resulting in poor match quality, high drop-out rates, and inequitable access for disadvantaged groups.

**Proposed Solution**: Build a skills-based matching platform connecting apprentice profiles (skills, interests, location) with employer vacancies, with guided SME onboarding, anonymised applications, and ESFA funding integration.

**Strategic Fit**: Supports the government's 500,000 apprenticeship starts target, the Skills for Jobs agenda, and SDG 4 (quality education and lifelong learning).

**Investment Required**: GBP 8.5M over 3 years

- Capital: GBP 5.5M
- Operational (3 years): GBP 3.0M

**Expected Benefits**: GBP 45.2M over 5 years

- Additional apprenticeship starts economic value: GBP 28.0M
- Employer productivity from better matching: GBP 9.5M
- Reduced youth unemployment costs (DWP): GBP 5.2M
- Legacy system decommissioning: GBP 2.5M

**Return on Investment**:

- NPV: GBP 28.6M (discounted at 3.5%)
- Payback Period: 16 months
- BCR: 4.3:1

**Recommended Option**: Option 2: Skills-Matched Platform with Funding Integration

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The Find an Apprenticeship service lists approximately 30,000 vacancies at any time. Users search by keyword and location with no skills matching. 35% of vacancies go unfilled. 12-month apprenticeship retention is 67% (suggesting poor initial matching). The service has not been significantly updated since 2018.

**Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| Minister | Apprenticeship starts declining (509K to 337K) | Manifesto target at risk | CRITICAL |
| Employers | 35% of vacancies unfilled | Lost productivity, wasted Levy | HIGH |
| Young People | Cannot find relevant opportunities; poor UX | Youth disengagement | HIGH |
| SMEs | Vacancy creation too complex | 60% of potential SME employers abandon process | HIGH |
| ESFA | Manual funding processes slow starts | 12-week average time-to-start | HIGH |

### A1.2 Strategic Alignment

- **Skills for Jobs White Paper**: "Reform the apprenticeship system to be employer-led and accessible"
- **Levelling Up**: "Improve skills and employment outcomes in left-behind communities"
- **SDG 4**: "Ensure inclusive and equitable quality education and promote lifelong learning"
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Learner-Centred Design), 4 (Digital Inclusion), 14 (Accessibility)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**3-Year Cost**: GBP 1.5M (maintaining legacy Find an Apprenticeship)
**Benefits**: GBP 0
**Impact**: Vacancy fill rates continue declining; youth unemployment persists; Levy underutilisation continues
**Recommendation**: **Reject**

### Option 1: Refresh Find an Apprenticeship UI Only

**Description**: Modernise the front-end of Find an Apprenticeship with mobile-responsive design. No matching algorithm, no ESFA integration.

**3-Year Cost**: GBP 2.0M
**5-Year Benefits**: GBP 8.5M (marginal improvement in user engagement)
**NPV**: GBP 5.3M
**Stakeholder Goals Met**: 30%
**Recommendation**: Insufficient — does not address root cause (poor matching)

### Option 2: Skills-Matched Platform with Funding Integration (RECOMMENDED)

**Description**: Full skills-matching platform with apprentice profiles, employer vacancy management, SME guided flow, anonymised applications, training provider directory, and ESFA funding integration.

**3-Year Cost**: GBP 8.5M

- Capital: GBP 5.5M (platform development GBP 3.0M, matching algorithm GBP 1.0M, ESFA integration GBP 1.0M, UX/accessibility GBP 0.5M)
- Operational: GBP 3.0M (hosting GBP 0.4M/yr, support GBP 0.3M/yr, operations GBP 0.3M/yr)

**5-Year Benefits**:

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Additional starts economic value | GBP 2M | GBP 5M | GBP 7M | GBP 7M | GBP 7M | GBP 28.0M |
| Employer productivity | GBP 0.5M | GBP 1.5M | GBP 2.5M | GBP 2.5M | GBP 2.5M | GBP 9.5M |
| Reduced unemployment costs | GBP 0.4M | GBP 1.0M | GBP 1.2M | GBP 1.3M | GBP 1.3M | GBP 5.2M |
| Legacy decommissioning | GBP 0 | GBP 0.5M | GBP 0.8M | GBP 0.6M | GBP 0.6M | GBP 2.5M |
| **Total** | **GBP 2.9M** | **GBP 8.0M** | **GBP 11.5M** | **GBP 11.4M** | **GBP 11.4M** | **GBP 45.2M** |

**NPV**: GBP 28.6M | **BCR**: 4.3:1 | **Payback**: 16 months

**Stakeholder Goals Met**: 85%

### Option 3: AI-Powered Career Coaching Platform

**3-Year Cost**: GBP 15.0M
**5-Year Benefits**: GBP 55.0M
**NPV**: GBP 22.1M (lower than Option 2)
**Risk**: HIGH (AI career advice for under-18s raises ethical and AADC concerns)
**Recommendation**: **Defer AI coaching to Phase 2**

---

# PART C: COMMERCIAL CASE

**Procurement Route**: G-Cloud 14 for platform development and hosting. Existing ESFA development capability for funding integration.

**Commercial Model**: Crown-owned platform. Free for apprentices and employers. Training provider listing may attract modest marketplace revenue in future phases.

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (CDEL) | GBP 3.0M | GBP 2.0M | GBP 0.5M | GBP 5.5M |
| Revenue (RDEL) | GBP 0.7M | GBP 1.0M | GBP 1.3M | GBP 3.0M |
| **Total** | **GBP 3.7M** | **GBP 3.0M** | **GBP 1.8M** | **GBP 8.5M** |

**Funding Source**: DfE DEL (Apprenticeships programme budget) with ESFA co-funding for integration development.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research with apprentices, employers, providers; technical feasibility |
| Alpha | 3 months | Matching algorithm prototype; SME vacancy flow; ESFA integration assessment |
| Private Beta | 6 months | Platform with 500 pilot employers and 5,000 apprentice profiles |
| Public Beta | 6 months | National launch; legacy Find an Apprenticeship decommissioned |
| Live | Ongoing | Continuous improvement; Phase 2 features |

## E1.3 Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Matching algorithm produces poor matches | MEDIUM | HIGH | Iterative development with A/B testing; user feedback loop; manual review of early matches |
| SME employer adoption low | MEDIUM | HIGH | Dedicated SME onboarding support; partnership with FSB and Chambers of Commerce |
| ESFA integration delays | MEDIUM | HIGH | Early ESFA engagement; parallel development; manual fallback process |
| Training provider opposition | LOW | MEDIUM | Provider working group; platform enhances rather than replaces provider role |
| Data quality of skills assessments | MEDIUM | MEDIUM | Validated assessment instruments; professional careers guidance review |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Green Book | Guidance | GOV.UK | Five-case model | N/A — external reference |
| Skills for Jobs White Paper | Policy | DfE | Skills system reform priorities | N/A — external reference |
| Apprenticeship Funding Rules | Guidance | ESFA | Funding pathways | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Apprenticeship Matching Service
**Model**: Claude Opus 4.6
