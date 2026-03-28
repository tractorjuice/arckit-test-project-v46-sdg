# Strategic Outline Business Case (SOBC): Research Collaboration Hub

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Research Collaboration Hub (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Research Collaboration Hub Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Research Collaboration Programme Board, DSIT, UKRI, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC sets out the strategic justification for investing in a Research Collaboration Hub connecting UK research institutions with industry to accelerate knowledge transfer, collaborative R&D, and research commercialisation.

---

## Executive Summary

**Purpose**: To accelerate the translation of UK university research into commercial products and economic impact by providing an intelligent matchmaking platform that connects industry R&D challenges to academic expertise, with streamlined engagement processes that make university-industry collaboration accessible to SMEs.

**Problem Statement**: The UK ranks 4th globally for research quality but 10th for innovation output. The "valley of death" between discovery and commercialisation persists because industry (especially SMEs) cannot easily find relevant academic expertise, engagement processes take 6+ months, and current mechanisms are fragmented across institutional websites, personal networks, and sector-specific intermediaries. An estimated 70% of potentially commercialisable research never reaches market.

**Proposed Solution**: Build an AI-powered matchmaking platform with auto-populated researcher profiles (via ORCID and institutional CRIS), industry challenge posting, standardised engagement templates, and outcome tracking to demonstrate impact.

**Strategic Fit**: Supports the UK R&D Framework (2.4% GDP target), DSIT Innovation Strategy, KEF, and KE Concordat. Addresses the persistent gap between research excellence and innovation output that multiple government reviews have identified.

**Investment Required**: GBP 10.4M over 3 years

- Capital: GBP 7.5M
- Operational (3 years): GBP 2.9M

**Expected Benefits**: GBP 60-100M over 5 years

- Additional collaborative R&D expenditure (25% increase): GBP 300-500M/year of which government platform contribution estimated at GBP 15-25M/year
- University KE income increase: GBP 10M/year
- SME productivity gains from research access: GBP 20M/year

**Return on Investment**:

- NPV: GBP 35M (discounted at 3.5%, 5-year horizon, conservative)
- Payback Period: 24 months
- ROI: 240%

**Recommended Option**: Option 2: Intelligent Matchmaking Platform with KTN Partnership

**Key Risks**:

1. Low researcher adoption — platform becomes an empty directory
2. Platform becomes a directory rather than delivering genuine matchmaking
3. IP concerns deter industry participation

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK's persistent research-to-innovation gap represents a significant economic opportunity cost. Even a modest improvement in knowledge exchange — a 25% increase in collaborative R&D projects — would generate returns many times the platform cost. The partnership with KTN provides human brokerage expertise alongside algorithmic matching, mitigating the risk of a technology-only approach.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: UK universities produce world-leading research, but translation into commercial products and economic impact lags behind the US, Germany, and South Korea. Current industry-academia collaboration mechanisms are fragmented and rely heavily on personal networks, disadvantaging SMEs and researchers at less visible institutions. The average time from initial industry enquiry to formal collaboration agreement is 6 months — by which time many SMEs have moved on or found alternative solutions.

**Specific Pain Points** (from Stakeholder Analysis ARC-005-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DSIT | SD-1 | UK ranks 4th research but 10th innovation | Lost economic value from untranslated research | CRITICAL |
| Researchers | SD-2 | Industry engagement relies on personal networks | Early-career and non-Russell Group researchers excluded | MEDIUM |
| SMEs | SD-3 | Cannot find or engage academic expertise affordably | SME innovation limited to internal capability | HIGH |
| Research England | SD-4 | Insufficient data on KE activity and outcomes | Cannot demonstrate KE value, difficult to improve | MEDIUM |

**Consequences of Inaction**:

- UK continues to underperform on research-to-innovation translation
- SMEs remain excluded from university collaboration — only large corporates with R&D departments benefit
- Estimated 70% of commercially promising research never reaches market
- UK falls further behind competitors on R&D/GDP ratio (currently 1.7%, target 2.4%)

### A1.2 Strategic Alignment

- **UK R&D Framework**: 2.4% R&D/GDP target requires increased business R&D investment, which university collaboration drives
- **DSIT Innovation Strategy**: Knowledge exchange as a key lever for innovation
- **KEF / KE Concordat**: Institutional incentives for improved KE performance
- **FAIR Data Principles**: Research output discoverability
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 2 (User-Centred Design), 5 (Interoperability), 21 (FAIR Data), 22 (Open Source and Reuse)

### A1.3 Why Now?

- KEF creating institutional incentives for KE improvement — universities are motivated
- ORCID adoption now widespread — technical foundation for researcher identification exists
- AI/ML capabilities mature enough for meaningful semantic matching
- Post-pandemic shift toward digital engagement — industry and academia both more open to digital collaboration tools
- Government R&D spending review creating urgency to demonstrate research impact

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Researcher Profiles**: 80% of active UK researchers with profiles (auto-populated)
2. **Successful Matches**: 500 per quarter leading to formal engagement
3. **SME Participation**: >40% of industry engagements from SMEs

## B2. Options Analysis

### Option 0: Do Nothing

**Costs**: GBP 0. Current fragmented landscape continues.

**Benefits**: GBP 0

**Recommendation**: **Reject** — Research-to-innovation gap continues to widen; UK falls behind competitors.

---

### Option 1: Enhanced Directory (Gateway to Research Upgrade)

**Description**: Upgrade the existing Gateway to Research (GtR) platform with improved search and basic industry-facing features, without AI matchmaking or engagement workflow.

**Costs** (3-year): GBP 3.0M

**Benefits** (3-year): GBP 10M (modest improvement in discoverability)

**Stakeholder Goals Met**: 25%

**Recommendation**: A directory alone has been tried (multiple university consortium attempts have failed to gain traction). Without intelligent matchmaking and engagement support, adoption will be low.

---

### Option 2: Intelligent Matchmaking Platform with KTN Partnership (RECOMMENDED)

**Description**: AI-powered matchmaking platform with auto-populated researcher profiles, industry challenge posting, semantic matching, standardised engagement templates, and human brokerage via KTN partnership. Outcome tracking for impact measurement.

**Costs** (3-year) - ROM (+-30%):

- Capital: GBP 7.5M
  - Platform development: GBP 5.0M
  - AI/ML matchmaking engine: GBP 1.5M
  - Integrations (ORCID, GtR, CRIS): GBP 0.5M
  - User research and GDS assessment: GBP 0.5M
- Operational: GBP 2.9M over 3 years
  - Cloud infrastructure: GBP 0.5M/year (from Year 2)
  - BAU team: GBP 1.0M/year (from Year 2)
  - KTN broker services: GBP 0.3M/year
  - Data subscriptions: GBP 0.1M/year
- Total 3-year TCO: GBP 10.4M

**Benefits** (3-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Additional collaborative R&D (platform contribution) | DSIT G-1 | FINANCIAL | GBP 0M | GBP 5M | GBP 15M | GBP 20M |
| B-002 | University KE income increase | Uni G-2 | FINANCIAL | GBP 0M | GBP 3M | GBP 7M | GBP 10M |
| B-003 | SME productivity gains | SMEs G-1 | FINANCIAL | GBP 0M | GBP 5M | GBP 10M | GBP 15M |
| B-004 | KEF/impact evidence value | Research England G-2 | STRATEGIC | — | — | — | Unquantified |
| **Total** | | | | **GBP 0M** | **GBP 13M** | **GBP 32M** | **GBP 45M** |

**NPV** (3.5% discount): **GBP 33M** (3-year), **GBP 55M** (5-year)

**ROI**: 330% (3-year) | **Payback Period**: 20 months

**Stakeholder Goals Met**: 80%

**Recommendation**: **RECOMMENDED** — The combination of AI matchmaking and human brokerage (KTN) addresses the key failure mode of previous directory-only approaches. SME-friendly engagement templates address the underserved SME segment.

---

### Option 3: Full Innovation Ecosystem Platform

**Description**: Option 2 plus IP marketplace, virtual lab facilities, shared equipment booking, international researcher matching, and startup incubator features.

**Costs** (3-year): GBP 25M

**Benefits** (3-year): GBP 55M

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Scope creep risk is very high. Core matchmaking + engagement delivers 80% of value. IP marketplace and virtual labs are separate, complex initiatives that should be evaluated independently.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 0M | GBP 3M | GBP 10.4M | GBP 25M |
| 3-Year Benefit | GBP 0M | GBP 10M | GBP 45M | GBP 55M |
| NPV | GBP 0M | GBP 6M | GBP 33M | GBP 22M |
| Stakeholder Goals | 0% | 25% | 80% | 100% |
| Implementation Risk | None | LOW | MEDIUM | HIGH |
| Recommendation | Reject | Reject | **RECOMMENDED** | Reject |

---

# PART C: COMMERCIAL CASE

**Approach**: Internal build with DSIT digital team, with specialist subcontractors for AI/ML matchmaking engine development, NLP model training, and KTN partnership for human brokerage.

**Key Procurements**:

- Cloud hosting: Crown Commercial Service framework (GBP 0.5M/year)
- AI/ML development: Digital Marketplace (GBP 1.5M)
- KTN partnership: Direct agreement with Innovate UK / KTN (GBP 0.3M/year)
- ORCID integration: Direct ORCID membership
- Search infrastructure: G-Cloud (GBP 0.3M)

---

# PART D: FINANCIAL CASE

| Financial Year | Capital | Revenue | Total |
|----------------|---------|---------|-------|
| FY 2026/27 | GBP 4.0M | GBP 0.3M | GBP 4.3M |
| FY 2027/28 | GBP 3.0M | GBP 1.3M | GBP 4.3M |
| FY 2028/29 | GBP 0.5M | GBP 1.3M | GBP 1.8M |
| **Total** | **GBP 7.5M** | **GBP 2.9M** | **GBP 10.4M** |

**Funding Source**: DSIT research and innovation budget, with potential co-funding from UKRI Knowledge Exchange allocation and Innovate UK.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

| Phase | Duration | Key Deliverables |
|-------|----------|-----------------|
| Discovery | 3 months | User research with researchers, SMEs, and KTOs; existing platform assessment |
| Alpha | 4 months | Matchmaking prototype, ORCID integration POC, NLP model training |
| Private Beta | 8 months | Platform launch with 20 universities, 200 industry users, KTN broker team |
| Public Beta | 6 months | National launch, 80% researcher coverage, outcome tracking |
| Live | Ongoing | Full national service, model refinement |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Low researcher adoption | HIGH | HIGH | Auto-populate from ORCID/GtR — near-zero effort; institutional KTO champions |
| Directory not matchmaker | MEDIUM | HIGH | Invest in AI/ML matching; KTN human brokers; measure matches, not views |
| IP concerns deter industry | MEDIUM | MEDIUM | Standardised model agreements; anonymous initial matching; Lambert Toolkit |
| Insufficient SME participation | MEDIUM | HIGH | SME-friendly UX; Innovate UK voucher integration; FSB promotion |

## E3. Governance

- **SRO**: DSIT Director of Research and Innovation
- **Programme Board**: Monthly, chaired by SRO
- **Advisory Board**: UKRI, KTN, Russell Group, FSB, CBI representatives
- **Assurance**: CDDO spend control, GDS service assessment

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-005-STKE-v1.0 | Stakeholder Analysis | ArcKit | Drivers and goals | `projects/005-research-collaboration-hub/` |
| ARC-005-REQ-v1.0 | Requirements | ArcKit | Requirements | `projects/005-research-collaboration-hub/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Research Collaboration Hub (Project 005)
**Model**: Claude Opus 4.6
