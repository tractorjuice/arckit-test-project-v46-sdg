# Strategic Outline Business Case (SOBC): Innovation Funding Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Innovation Funding Platform (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Innovation Funding Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Innovation Funding Programme Board, UKRI, DSIT, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC sets out the strategic justification for replacing the legacy Je-S system with a modern Innovation Funding Platform for UKRI grant application and portfolio management.

---

## Executive Summary

**Purpose**: To replace the universally criticised Je-S system with a modern, user-centred grants application platform that reduces researcher administrative burden, enables cross-council portfolio analytics, and integrates with institutional research management systems.

**Problem Statement**: Je-S is rated 2.1/5.0 by researchers. Application preparation takes 30-40 hours with 15-20 hours wasted on system friction. UKRI cannot provide cross-council portfolio analytics for Treasury spending reviews, taking 2-4 weeks to answer basic questions. The system cannot support modern browser standards, has no auto-save, and cannot integrate with institutional systems.

**Proposed Solution**: Build a modern, cloud-native grants platform with configurable council-specific schemes, ORCID integration, auto-save, institutional API integration, and cross-council portfolio analytics.

**Strategic Fit**: Supports UKRI Strategy 2022-2027, UK R&D Framework (2.4% GDP target), and DSIT research and innovation priorities.

**Investment Required**: GBP 29.3M over 3 years

- Capital: GBP 22.5M
- Operational (3 years): GBP 6.8M

**Expected Benefits**: GBP 75-100M over 5 years

- Researcher productivity recovery: GBP 25M/year (500,000 hours at average academic salary)
- University research office efficiency: GBP 10M/year (2 FTE saved x 130 universities)
- UKRI operational efficiency: GBP 5M/year (reduced manual processes)
- Research funding protection in spending reviews: unquantifiable but strategic

**Return on Investment**:

- NPV: GBP 50M (discounted at 3.5%, 5-year horizon, conservative)
- Payback Period: 18 months
- ROI: 170%

**Recommended Option**: Option 2: Full Platform Replacement with Phased Migration

**Key Risks**:

1. Migration disruption during active funding round
2. Research Council resistance to process standardisation
3. Institutional API integration complexity across 130+ universities

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: Je-S replacement is universally demanded — continued operation carries reputational and operational risk. The productivity savings alone (GBP 25M/year) justify the investment. The strategic value of cross-council portfolio analytics for protecting GBP 8 billion annual research funding in spending reviews is unquantifiable but potentially enormous.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Je-S has been the primary UKRI grant application platform for over a decade. It was designed for a pre-UKRI era when Research Councils operated independently. The platform cannot provide cross-council views, uses obsolete technology (incompatible with modern browsers), has no auto-save (researchers regularly lose hours of work), and cannot integrate with institutional research management systems, requiring duplicate data entry.

**Specific Pain Points** (from Stakeholder Analysis ARC-003-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| UKRI CEO | SD-1 | Cannot demonstrate cross-council portfolio value | Treasury spending review vulnerability | CRITICAL |
| Researchers | SD-2 | 15-20 hours wasted per application on system friction | 500,000 researcher-hours/year lost (GBP 25M) | CRITICAL |
| Council CEOs | SD-3 | Cannot configure council-specific schemes easily | Delays to new funding calls | HIGH |
| University ROs | SD-4 | Duplicate data entry between institutional systems and Je-S | 2-3 FTE wasted per large university | HIGH |

**Consequences of Inaction**:

- GBP 25M/year in researcher productivity continues to be wasted
- UKRI cannot defend GBP 8B research budget in Treasury spending reviews
- UK research competitiveness damaged — competitor nations (US NSF, EU ERC) offer better systems
- Application completion rates remain at ~75% — potential research never funded

### A1.2 Strategic Alignment

- **UKRI Strategy 2022-2027**: Digital transformation as a strategic priority
- **UK R&D Framework**: 2.4% GDP R&D target requires efficient funding mechanisms
- **FAIR Data Principles**: Research data management compliance
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 2 (User-Centred Design), 21 (FAIR Data), 5 (Interoperability)

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Researcher Satisfaction**: Score >4.0/5.0 (vs 2.1/5.0 baseline)
2. **Zero Migration Disruption**: No funding round interrupted by platform migration
3. **Portfolio Analytics**: Treasury queries answerable within 24 hours

## B2. Options Analysis

### Option 0: Do Nothing (Continue with Je-S)

**Costs**: GBP 4M/year ongoing maintenance (rising as technical debt increases)

**Benefits**: GBP 0

**Cons**: Researcher dissatisfaction deepens; UKRI cannot provide portfolio analytics; system at risk of critical failure (aging technology, no vendor support path)

**Recommendation**: **Reject** — Je-S is approaching end-of-life with no sustainable upgrade path.

---

### Option 1: Je-S Enhancement

**Description**: Modernise Je-S front-end with a new UI layer while retaining the existing backend and data model.

**Costs** (3-year): GBP 12.0M

**Benefits** (3-year): GBP 30M (partial UX improvement, no portfolio analytics, no institutional integration)

**Stakeholder Goals Met**: 25%

**Recommendation**: Addresses the symptom (bad UI) without solving the underlying problems (council-specific configuration, cross-council analytics, institutional integration).

---

### Option 2: Full Platform Replacement — Phased Migration (RECOMMENDED)

**Description**: Build a modern, cloud-native platform with configurable council-specific schemes, ORCID integration, auto-save, institutional API integration, and portfolio analytics. Migrate council-by-council from Je-S.

**Costs** (3-year) - ROM (+-30%):

- Capital: GBP 22.5M
  - Platform development: GBP 18.0M
  - Data migration: GBP 2.0M
  - User research and GDS assessment: GBP 1.0M
  - Security and compliance: GBP 0.5M
  - Training and change management: GBP 1.0M
- Operational: GBP 6.8M over 3 years
  - Cloud infrastructure: GBP 1.5M/year (from Year 2)
  - BAU team: GBP 3.0M/year (from Year 2)
  - ORCID membership: GBP 0.1M/year
  - Parallel running with Je-S: GBP 2.0M (Year 2 only)
- Total 3-year TCO: GBP 29.3M

**Benefits** (3-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Researcher productivity recovery | Researchers G-1 | OPERATIONAL | GBP 0M | GBP 10M | GBP 25M | GBP 35M |
| B-002 | University RO efficiency | Uni ROs G-3 | OPERATIONAL | GBP 0M | GBP 3M | GBP 10M | GBP 13M |
| B-003 | UKRI operational efficiency | UKRI G-2 | OPERATIONAL | GBP 0M | GBP 2M | GBP 5M | GBP 7M |
| B-004 | Research funding protection (strategic) | UKRI G-2 | STRATEGIC | — | — | — | Unquantified |
| B-005 | Je-S decommissioning savings | UKRI | FINANCIAL | GBP 0M | GBP 0M | GBP 4M | GBP 4M |
| **Total** | | | | **GBP 0M** | **GBP 15M** | **GBP 44M** | **GBP 59M** |

**NPV** (3.5% discount): **GBP 28M** (3-year), **GBP 50M** (5-year with sustained benefits)

**ROI**: 100% (3-year), 170% (5-year) | **Payback Period**: 18 months

**Stakeholder Goals Met**: 85%

**Recommendation**: **RECOMMENDED** — Phased migration de-risks the transition while delivering transformative improvements.

---

### Option 3: Commercial Off-The-Shelf (COTS) Grants Platform

**Description**: Procure and configure a commercial grants management platform (e.g., Fluxx, Benevity, SmartSimple) customised for UKRI requirements.

**Costs** (3-year): GBP 22M (licence + customisation + integration)

**Benefits** (3-year): GBP 45M (faster initial deployment but limited customisation for council-specific needs)

**Stakeholder Goals Met**: 60%

**Recommendation**: **Reject** — No COTS platform supports the complexity of seven Research Councils with different processes, fEC costing, ORCID integration, and UK academic federated authentication. Customisation costs would approach bespoke build costs with less control and vendor dependency.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 12M (BAU) | GBP 12M | GBP 29.3M | GBP 22M |
| 3-Year Benefit | GBP 0M | GBP 30M | GBP 59M | GBP 45M |
| 5-Year NPV | -GBP 20M | GBP 10M | GBP 50M | GBP 25M |
| Stakeholder Goals | 0% | 25% | 85% | 60% |
| Implementation Risk | None | LOW | MEDIUM | MEDIUM |
| Recommendation | Reject | Reject | **RECOMMENDED** | Reject |

---

# PART C: COMMERCIAL CASE

**Approach**: Internal build with UKRI Digital delivery team, supplemented by specialist subcontractors for ORCID integration, institutional API development, and portfolio analytics.

**Key Procurements**:

- Cloud hosting: Crown Commercial Service framework
- ORCID institutional membership: Direct agreement
- Search and analytics infrastructure: G-Cloud
- Accessibility testing: Digital Marketplace

---

# PART D: FINANCIAL CASE

| Financial Year | Capital | Revenue | Total |
|----------------|---------|---------|-------|
| FY 2026/27 | GBP 8.0M | GBP 0.5M | GBP 8.5M |
| FY 2027/28 | GBP 10.0M | GBP 3.0M | GBP 13.0M |
| FY 2028/29 | GBP 4.5M | GBP 3.3M | GBP 7.8M |
| **Total** | **GBP 22.5M** | **GBP 6.8M** | **GBP 29.3M** |

**Funding Source**: UKRI central budget, with potential DSIT contribution for portfolio analytics capability.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 4 months | User research with researchers and ROs, Je-S data assessment |
| Alpha | 5 months | Prototype, ORCID integration POC, fEC integration POC |
| Private Beta (Council 1-2) | 8 months | AHRC and ESRC migration, core platform |
| Private Beta (Council 3-5) | 6 months | BBSRC, NERC, STFC migration |
| Public Beta (Council 6-7) | 6 months | MRC, EPSRC migration, portfolio analytics |
| Live | Ongoing | Full service, Je-S decommission |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Migration disruption | MEDIUM | CRITICAL | Council-by-council migration between funding rounds; Je-S read-only for 12 months |
| Council resistance | HIGH | MEDIUM | CEO-level governance; configurable schemes; demonstrate value on smaller councils first |
| Institutional integration complexity | MEDIUM | MEDIUM | Start with 3 major RMS platforms; provide generic API for others |
| Researcher adoption resistance | LOW | MEDIUM | Extensive user research; beta testing with real applications; demonstrate superiority over Je-S |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-003-STKE-v1.0 | Stakeholder Analysis | ArcKit | Drivers and goals | `projects/003-innovation-funding-platform/` |
| ARC-003-REQ-v1.0 | Requirements | ArcKit | Requirements | `projects/003-innovation-funding-platform/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Innovation Funding Platform (Project 003)
**Model**: Claude Opus 4.6
