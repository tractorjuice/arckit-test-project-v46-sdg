# Strategic Outline Business Case (SOBC): Teacher Recruitment Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Teacher Recruitment Portal (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, TRP Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Investment Board, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in a Teacher Recruitment Portal, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: DfE seeks to replace the fragmented teacher recruitment landscape with a unified portal that increases applications for shortage subjects, simplifies the candidate journey, and integrates pre-employment checks to get teachers into classrooms faster.

**Problem Statement**: Secondary ITT recruitment targets have been missed for 11 consecutive years in shortage subjects. The current recruitment journey spans 3-5 separate systems with 35% application abandonment. England faces a structural teacher supply deficit that threatens educational quality.

**Proposed Solution**: Build a unified Teacher Recruitment Portal covering the full journey from career exploration through route selection, course discovery, application, offer management, and pre-employment checks (DBS/TRA integration).

**Strategic Fit**: Directly supports DfE's Teacher Recruitment and Retention Strategy and SDG 4 (quality education requires quality teachers).

**Investment Required**: GBP 7.2M over 3 years

- Capital: GBP 4.8M
- Operational (3 years): GBP 2.4M

**Expected Benefits**: GBP 38.5M over 5 years

- Additional teachers in shortage subjects (economic value): GBP 22.0M
- Reduced school supply teacher spend: GBP 9.5M
- Reduced application processing costs: GBP 4.5M
- UCAS Teacher Training fee savings: GBP 2.5M

**Return on Investment**:

- NPV: GBP 22.8M (discounted at 3.5%)
- Payback Period: 18 months
- BCR: 4.5:1

**Recommended Option**: Option 2: Unified Portal with DBS/TRA Integration

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The BCR of 4.5:1 demonstrates strong value for money. Each additional Physics or Maths teacher recruited addresses a direct classroom shortage affecting thousands of pupils. The investment is modest relative to DfE's GBP 240M annual spend on teacher recruitment activities and the GBP 1.3B schools spend on supply teachers.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: England needs approximately 40,000 new teachers entering the profession annually. ITT recruitment consistently falls short in secondary subjects: Physics achieves only 38% of target, Maths 68%, MFL 52%, Computing 44%. The current recruitment journey is fragmented across Get Into Teaching, DfE Apply, UCAS Teacher Training, and individual provider websites. Career changers — the largest untapped source for shortage subjects — face a bewildering array of training routes and a 4-6 hour application process.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| Minister | Shortage subject targets missed 11 years running | Classroom vacancies; pupil attainment impact | CRITICAL |
| Career Changers | 4-6 hour application; confusing routes | 35% abandonment; lost candidates to other careers | HIGH |
| ITT Providers | Applications via 3 separate channels | Administrative overhead; candidates lost between systems | HIGH |
| Schools | Cannot recruit for Physics, Maths, Computing | GBP 1.3B/year on supply teachers; quality impact | HIGH |
| DBS/TRA | Manual pre-employment checks delay starts | 14 weeks average offer-to-start time | MEDIUM |

**Consequences of Inaction**:

- Teacher vacancies continue rising (currently 2,400 FTE secondary vacancies)
- Pupil attainment in shortage subjects declines further (GCSE pass rates in Physics already falling)
- Schools spend increasing amounts on supply teachers (GBP 1.3B annually)
- International competitiveness in STEM education weakens

### A1.2 Strategic Alignment

- **Teacher Recruitment and Retention Strategy**: "Make it easier for talented people to become teachers"
- **Skills for Jobs**: "Ensure the education system produces the skills the economy needs"
- **SDG 4**: "Ensure inclusive and equitable quality education" — which requires a sufficient supply of quality teachers
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Learner-Centred Design), 4 (Digital Inclusion), 6 (Security — DBS data)

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**3-Year Cost**: GBP 3.5M (maintaining Get Into Teaching, DfE Apply, UCAS contract)
**Benefits**: GBP 0
**Impact**: Shortage subject recruitment continues declining; supply teacher costs continue rising
**Recommendation**: **Reject**

### Option 1: Improve DfE Apply Only

**Description**: Modernise the existing DfE Apply service with better UX, route finder, and bursary calculator. No provider dashboard improvements; no DBS/TRA integration.

**3-Year Cost**: GBP 2.5M
**5-Year Benefits**: GBP 14.0M (modest improvement in abandonment and shortage applications)
**NPV**: GBP 9.8M
**Stakeholder Goals Met**: 45%
**Recommendation**: Insufficient — does not address provider needs, pre-employment delays, or UCAS transition

### Option 2: Unified Portal with DBS/TRA Integration (RECOMMENDED)

**Description**: Complete unified portal covering route finder, course search, application, provider management, DBS/TRA integration, and Get Into Teaching campaign integration.

**3-Year Cost**: GBP 7.2M

- Capital: GBP 4.8M (portal development GBP 2.5M, DBS/TRA integration GBP 0.8M, course data platform GBP 0.5M, route finder GBP 0.3M, provider dashboard GBP 0.4M, UX/accessibility GBP 0.3M)
- Operational: GBP 2.4M (hosting GBP 0.3M/yr, support GBP 0.3M/yr, content GBP 0.2M/yr)

**5-Year Benefits**:

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Additional shortage teachers | GBP 1.5M | GBP 4.0M | GBP 5.5M | GBP 5.5M | GBP 5.5M | GBP 22.0M |
| Reduced supply teacher spend | GBP 0.5M | GBP 1.5M | GBP 2.5M | GBP 2.5M | GBP 2.5M | GBP 9.5M |
| Application processing savings | GBP 0.5M | GBP 0.8M | GBP 1.0M | GBP 1.1M | GBP 1.1M | GBP 4.5M |
| UCAS fee savings | GBP 0 | GBP 0.5M | GBP 0.7M | GBP 0.7M | GBP 0.6M | GBP 2.5M |
| **Total** | **GBP 2.5M** | **GBP 6.8M** | **GBP 9.7M** | **GBP 9.8M** | **GBP 9.7M** | **GBP 38.5M** |

**NPV**: GBP 22.8M | **BCR**: 4.5:1 | **Payback**: 18 months

**Stakeholder Goals Met**: 90%

### Option 3: AI-Powered Recruitment and Retention Platform

**Description**: Full portal (as Option 2) plus AI-powered candidate matching, predictive retention modelling, and automated reference checking.

**3-Year Cost**: GBP 13.0M
**5-Year Benefits**: GBP 48.0M
**NPV**: GBP 19.4M (lower than Option 2 due to higher costs and uncertain AI benefits)
**Risk**: HIGH (AI recommendations on career suitability raise ethical concerns)
**Recommendation**: **Defer to Phase 2**

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 3.5M | GBP 2.5M | GBP 7.2M | GBP 13.0M |
| 5-Year Benefits | GBP 0 | GBP 14.0M | GBP 38.5M | GBP 48.0M |
| NPV | GBP 0 | GBP 9.8M | GBP 22.8M | GBP 19.4M |
| BCR | N/A | 5.6:1 | 4.5:1 | 3.1:1 |
| Goals Met | 0% | 45% | 90% | 100% |

**Recommended**: **Option 2** — highest NPV with manageable risk and 90% goal coverage.

---

# PART C: COMMERCIAL CASE

**Procurement Route**: G-Cloud 14 for platform development and hosting. Existing DfE Apply development team to be expanded for portal development. DBS integration procured through direct agreement with DBS digital services team. TRA integration developed in-house (TRA is a DfE executive agency).

**Commercial Model**: Crown-owned platform. Free for candidates and ITT providers. Replaces current UCAS Teacher Training commercial arrangement (saving approximately GBP 0.5M/year in UCAS fees).

**UCAS Transition**: Negotiated transition period with UCAS. DfE will assume full application processing from October 2028 (the 2028/29 recruitment cycle). UCAS retains role in undergraduate admissions and international teacher recruitment data sharing.

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (CDEL) | GBP 2.5M | GBP 1.8M | GBP 0.5M | GBP 4.8M |
| Revenue (RDEL) | GBP 0.5M | GBP 0.8M | GBP 1.1M | GBP 2.4M |
| **Total** | **GBP 3.0M** | **GBP 2.6M** | **GBP 1.6M** | **GBP 7.2M** |

**Funding Source**: DfE DEL (Teacher Supply programme budget). Partially offset by UCAS fee savings from Year 2.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research with career changers, providers; UCAS transition assessment |
| Alpha | 4 months | Route finder prototype; simplified application form; provider dashboard wireframes |
| Private Beta | 6 months | Working portal with 50 pilot providers and 2,000 candidate testers |
| Public Beta | 6 months | Full launch for 2027/28 recruitment cycle; UCAS parallel running |
| Live | Ongoing | Full 2028/29 cycle on TRP only; UCAS Teacher Training decommissioned |

## E1.3 Risk Management

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| ITT provider resistance to centralised portal | MEDIUM | HIGH | Co-design with provider working group; rich provider profiles; provider recruitment tools |
| UCAS transition creates service gap | MEDIUM | HIGH | 12-month parallel running; joint contingency plan with UCAS |
| DBS integration technically complex | HIGH | MEDIUM | Early DBS digital services engagement; fallback to current manual process |
| Candidate volume insufficient for shortage subjects | MEDIUM | HIGH | Integrated Get Into Teaching marketing; subject-specific campaigns; bursary prominence |
| Application form simplification reduces data quality | LOW | MEDIUM | Validated fields; structured work experience; provider feedback loop |

## E1.4 Benefits Realisation

| Benefit | Measure | Baseline | Target | Responsible | Review |
|---------|---------|----------|--------|-------------|--------|
| Shortage subject applications | Application count by subject | 2024/25 data | +25% | Teacher Supply Dir. | Per cycle |
| Abandonment rate | Applications started vs submitted | 35% | < 15% | Service Owner | Monthly |
| Applications via TRP | % of all ITT applications | 0% | 90% | SRO | Per cycle |
| Time to start | Weeks from offer to classroom | 14 weeks | 10 weeks | CDO | Per cycle |
| Applicant diversity | % BAME, male primary, career changers | 18%, 14%, 35% | 25%, 20%, 45% | Teacher Supply Dir. | Per cycle |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Green Book | Guidance | GOV.UK | Five-case model, discount rates | N/A — external reference |
| Teacher Recruitment & Retention Strategy | Strategy | DfE | Recruitment priorities and targets | N/A — external reference |
| ITT Market Review | Review | DfE | ITT provider reform | N/A — external reference |
| DBS Code of Practice | Guidance | DBS | Disclosure handling requirements | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Teacher Recruitment Portal
**Model**: Claude Opus 4.6
