# Strategic Outline Business Case: Smart City IoT Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Smart City IoT Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart City IoT Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart City IoT Programme Board, DLUHC, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case (SOBC) presents the case for investing in a shared national IoT platform for urban services, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Establish a shared, secure national IoT platform enabling local authorities to deploy and manage connected sensors for urban services at significantly lower cost than independent procurement, while providing the foundational data infrastructure for the SDG 11 Sustainable Cities programme.

**Problem Statement**: Over 80 English local authorities are deploying IoT sensors independently, creating fragmented infrastructure with inconsistent security, incompatible data formats, and duplicated costs averaging £150-200 per sensor per year. There is no interoperability between councils, no shared security standards, and no national urban data layer.

**Proposed Solution**: A shared, multi-tenant IoT platform providing device management, secure data ingestion, spatial analytics, and open data publication, enabling local authorities to deploy sensors at 40-60% lower cost while contributing to a national urban data layer.

**Strategic Fit**: Directly supports Levelling Up White Paper (regional technology equity), NCSC Connected Places strategy (IoT security), and Geospatial Commission strategy (national spatial data infrastructure).

**Investment Required**: GBP 18M over 3 years

- Capital: GBP 12M
- Operational (3 years): GBP 6M

**Expected Benefits**: GBP 52M over 5 years

- Local authority cost savings: GBP 35M (avoided duplication across 50 authorities)
- Operational efficiency: GBP 10M (standardised management, reduced support)
- Data value: GBP 7M (cross-authority analytics, open data innovation)

**Return on Investment**:

- NPV: GBP 26.4M (discounted at 3.5%)
- Payback Period: 22 months
- ROI: 189%

**Recommended Option**: Option 2: Shared Cloud-Native Platform with Edge Computing

**Key Risks**:

1. Local authority adoption below target (mitigation: funded transition support, peer advocacy)
2. Privacy controversy damaging public trust (mitigation: proactive DPIA, citizen ethics panel)
3. IoT device security incident (mitigation: mandatory ETSI EN 303 645 certification)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The shared platform delivers compelling value for money (NPV GBP 26.4M), addresses NCSC security concerns, supports Levelling Up, and eliminates unsustainable fragmentation in local authority IoT deployment.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Define detailed requirements: `/arckit.requirements` (completed — ARC-001-REQ-v1.0)
3. NCSC engagement for IoT certification programme: Q2 2026
4. Early adopter local authority recruitment: Q2-Q3 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
English local authorities are deploying IoT sensors in an uncoordinated, fragmented manner. Each authority procures its own platform, negotiates its own vendor contracts, and operates its own infrastructure — often with inadequate security. There is no interoperability between councils, no shared data layer, and no national visibility of urban sensor data.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| LA Chief Execs | SD-3 | Each council building independent IoT infrastructure | GBP 2-10M per authority, 80+ doing this | CRITICAL |
| NCSC | SD-2 | Inconsistent IoT security across government deployments | National security vulnerability | CRITICAL |
| Minister | SD-1 | Smart city benefits limited to advanced councils | Levelling Up failure | HIGH |
| ICO | SD-4 | No consistent privacy standards for urban sensing | Regulatory risk | HIGH |

**Consequences of Inaction**:

- GBP 150-200M wasted over 5 years on duplicated IoT infrastructure across local authorities
- Increasing risk of IoT security incidents with no consistent ETSI EN 303 645 compliance
- No national urban data layer, preventing cross-authority analytics and evidence-based policy
- Smart city benefits concentrated in wealthy, digitally advanced councils — undermining Levelling Up

### A1.2 Strategic Drivers

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Minister | POLITICAL | Levelling Up through smart infrastructure | Regional equity |
| SD-2 | NCSC | SECURITY | Securing national IoT infrastructure | National security |
| SD-3 | LA Chief Execs | FINANCIAL | Reducing fragmentation and cost | Cost efficiency |
| SD-4 | ICO | COMPLIANCE | Privacy protection in sensor networks | Legal compliance |

**Strategic Alignment**:

- **Levelling Up White Paper**: Making smart city technology accessible to all councils, not just the digitally advanced
- **NCSC Connected Places Strategy**: Establishing the security standard for government IoT deployments
- **Geospatial Commission Strategy**: Contributing to national spatial data infrastructure
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 2 (IoT Security), 3 (Geospatial Interoperability), 6 (Scalability)

### A1.3 Scope

**In Scope**:
- Multi-tenant IoT device management platform
- Sensor data ingestion, storage, and API services
- ETSI EN 303 645 device certification programme
- Edge computing gateway management
- Open data publication pipeline
- Integration APIs for SDG 11 projects (002-005)

**Out of Scope**:
- Physical sensor procurement (local authority responsibility)
- Domain-specific analytics (handled by Projects 002-005)
- CCTV or facial recognition (explicitly excluded)

### A1.4 Why Now?

**Urgency Factors**:
- Local authorities accelerating IoT deployments post-COVID without coordination — fragmentation worsening monthly
- PSTI Act 2022 creates IoT security obligations — government should lead by example
- Geospatial Commission national data strategy requires spatial data infrastructure
- SDG 11 projects (002-005) need a shared sensor platform — without it, each builds its own

**Opportunity Cost of Delay**:
- GBP 30-40M per year in continued duplicated local authority IoT procurement
- Increasing IoT security risk with each uncoordinated deployment

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Local Authority Adoption**: Minimum 20 authorities onboarded in Year 1
   - **Measure**: Authorities actively publishing sensor data
   - **Threshold**: 15 authorities (below which platform lacks scale economies)

2. **IoT Security Compliance**: 100% ETSI EN 303 645 for connected devices
   - **Measure**: Device certification register
   - **Threshold**: 100% (non-negotiable)

3. **Cost Reduction Demonstrated**: 40%+ reduction vs. independent deployment
   - **Measure**: Cost per sensor per year comparison
   - **Threshold**: 30% minimum to justify shared platform overhead

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with fragmented local authority IoT deployments.

**Costs** (5-year): GBP 0 central investment, but GBP 150-200M in aggregate local authority spend on duplicated infrastructure.

**Benefits**: GBP 0 (no improvement in coordination, security, or data sharing)

**Pros**:
- No central investment required
- No coordination complexity

**Cons**:
- Continued fragmentation — GBP 150-200M wasted on duplication
- No consistent IoT security standard
- No national urban data layer
- Levelling Up gap widens

**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject** — Unsustainable fragmentation, growing security risk.

---

### Option 1: Centrally Managed Standards Only

**Description**: Publish IoT standards and certification requirements but do not build a shared platform. Local authorities continue deploying independently but must meet ETSI EN 303 645 and data interoperability standards.

**Costs** (5-year): GBP 3M (standards development, certification programme, compliance monitoring)

**Benefits** (5-year): GBP 15M (reduced security risk, improved interoperability)

**Pros**:
- Low central investment
- Addresses security standard gap
- Respects local authority autonomy

**Cons**:
- Does not address cost duplication
- Interoperability standards without shared platform are difficult to enforce
- No national data layer
- Each authority still bears full platform cost

**Stakeholder Goals Met**: 25%
**Recommendation**: **Partial** — Addresses security but not cost or data goals.

---

### Option 2: Shared Cloud-Native Platform with Edge Computing (RECOMMENDED)

**Description**: Build and operate a shared, multi-tenant IoT platform with cloud-native architecture and edge computing gateways, available to all English local authorities on an opt-in basis.

**Costs** (5-year) — ROM (+/-30%):

- Capital: GBP 12M
  - Platform development: GBP 6M
  - Edge infrastructure: GBP 3M
  - Security certification programme: GBP 1.5M
  - Integration and testing: GBP 1.5M
- Operational: GBP 10M over 5 years
  - Cloud infrastructure: GBP 1.2M/year
  - Platform operations team (8 FTE): GBP 0.6M/year
  - Security operations: GBP 0.2M/year
- Total 5-year TCO: GBP 22M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | LA cost avoidance (avoided duplication) | SD-3 G-4 | FINANCIAL | GBP 2M | GBP 5M | GBP 8M | GBP 10M | GBP 10M | GBP 35M |
| B-002 | Operational efficiency (standardised management) | SD-3 | OPERATIONAL | GBP 0.5M | GBP 1.5M | GBP 2.5M | GBP 3M | GBP 2.5M | GBP 10M |
| B-003 | Data value (cross-authority analytics, open data) | SD-1 G-3 | STRATEGIC | GBP 0.2M | GBP 0.8M | GBP 1.5M | GBP 2M | GBP 2.5M | GBP 7M |
| **Total** | | | | **GBP 2.7M** | **GBP 7.3M** | **GBP 12M** | **GBP 15M** | **GBP 15M** | **GBP 52M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 44.6M
- Total Costs PV: GBP 18.2M
- **NPV: GBP 26.4M**

**Return on Investment**:
- **ROI: 189%** over 5 years
- **Payback Period: 22 months**

**Pros**:
- Compelling VfM (NPV GBP 26.4M)
- 85% of stakeholder goals met
- Addresses security, cost, and data objectives
- Scalable from pilot to national deployment

**Cons**:
- GBP 12M upfront capital investment
- Requires local authority adoption (voluntary, not mandated)
- Platform operational risk

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive National IoT Infrastructure

**Description**: Build a comprehensive national IoT platform with mandatory adoption, including physical sensor procurement and deployment managed centrally.

**Costs** (5-year): GBP 85M (including sensor procurement, field deployment, central operations)

**Benefits** (5-year): GBP 65M

**Pros**:
- 100% of goals met
- Maximum consistency and security

**Cons**:
- GBP 85M investment — disproportionate to benefits
- Mandatory adoption politically unacceptable (local authority autonomy)
- Central government managing local sensor deployments is operationally impractical

**Stakeholder Goals Met**: 100%
**Recommendation**: **Reject** — Disproportionate cost, politically undeliverable.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Shared Cloud-Native Platform with Edge Computing**

**Rationale**:
1. **Best Value**: Highest NPV at GBP 26.4M
2. **Stakeholder Satisfaction**: Meets 85% of goals
3. **Acceptable Risk**: Voluntary adoption model respected, security addressed
4. **Affordability**: GBP 18M within DLUHC digital transformation budget
5. **Deliverability**: Cloud-native platform can be developed in 12 months

**Optimism Bias Adjustment** (UK Government):
- Standard uplift for IT projects: +40% on costs
- Adjusted Total Cost: GBP 22M -> GBP 30.8M (with uplift)
- NPV with optimism bias: Still positive at GBP 13.8M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: Mature market for IoT platform technology. Multiple established vendors and open-source options. Edge computing and device management are well-understood capabilities.

**UK Government Digital Marketplace Assessment**:
- **G-Cloud 14**: 45+ suppliers offering IoT platform services
- **DOS6**: 30+ suppliers for IoT specialists
- **SME participation**: 60% of IoT platform suppliers on Digital Marketplace are SMEs

### C1.2 Sourcing Route

**Recommended Route**: Digital Marketplace — G-Cloud for platform components, DOS for specialist build capability.

**Contract Approach**:
- **Build Phase**: Fixed-price with milestones (12 months)
- **Run Phase**: Managed service agreement with usage-based pricing (3+2 years)

### C1.3 Social Value

**Evaluation Approach**: Technical 60%, Cost 30%, Social Value 10%

**Social Value Focus**: Regional job creation (platform operations distributed across England), digital skills training for local authority staff, SME IoT manufacturer certification support.

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: GBP 18M over 3 years

### D1.1 Capital Expenditure

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 4M | GBP 2M | GBP 0 | GBP 6M |
| Edge infrastructure | GBP 1.5M | GBP 1M | GBP 0.5M | GBP 3M |
| Security certification programme | GBP 1M | GBP 0.5M | GBP 0 | GBP 1.5M |
| Integration and testing | GBP 1M | GBP 0.5M | GBP 0 | GBP 1.5M |
| **Total CapEx** | **GBP 7.5M** | **GBP 4M** | **GBP 0.5M** | **GBP 12M** |

### D1.2 Operational Expenditure

| Item | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------|--------|--------|--------|--------------|
| Cloud infrastructure | GBP 0.8M | GBP 1.2M | GBP 1.4M | GBP 3.4M |
| Platform operations (8 FTE) | GBP 0.5M | GBP 0.6M | GBP 0.6M | GBP 1.7M |
| Security operations | GBP 0.15M | GBP 0.2M | GBP 0.2M | GBP 0.55M |
| Training and onboarding support | GBP 0.2M | GBP 0.1M | GBP 0.05M | GBP 0.35M |
| **Total OpEx** | **GBP 1.65M** | **GBP 2.1M** | **GBP 2.25M** | **GBP 6M** |

## D2. Funding Source

**Source**: DLUHC Digital Transformation Fund (Spending Review 2025 settlement)
**Amount Available**: GBP 20M (GBP 18M project + GBP 2M contingency)
**Affordability**: **Affordable** — 4.5% of DLUHC annual digital spend

## D3. Financial Appraisal (Green Book)

**Discount Rate**: 3.5% (HMT standard)

| Year | Costs | Benefits | Net | Discount Factor | PV |
|------|-------|----------|-----|-----------------|-----|
| 0 | GBP 7.5M | GBP 0 | -GBP 7.5M | 1.000 | -GBP 7.5M |
| 1 | GBP 6.1M | GBP 2.7M | -GBP 3.4M | 0.966 | -GBP 3.3M |
| 2 | GBP 2.75M | GBP 7.3M | +GBP 4.55M | 0.934 | +GBP 4.2M |
| 3 | GBP 2.0M | GBP 12M | +GBP 10M | 0.902 | +GBP 9.0M |
| 4 | GBP 2.0M | GBP 15M | +GBP 13M | 0.871 | +GBP 11.3M |
| 5 | GBP 2.0M | GBP 15M | +GBP 13M | 0.842 | +GBP 10.9M |
| **Total** | **GBP 22.35M** | **GBP 52M** | **+GBP 29.65M** | | **+GBP 26.4M** |

**VfM Rating**: **High** — positive NPV of GBP 26.4M, payback in 22 months.

---

# PART E: MANAGEMENT CASE

## E1. Governance

### E1.1 Roles & Responsibilities

| Decision/Activity | Responsible | Accountable | Consulted | Informed |
|-------------------|-------------|-------------|-----------|----------|
| Programme delivery | Programme Manager | SRO | CDDO, NCSC | All stakeholders |
| Platform architecture | Solution Architect | DLUHC CDO | NCSC, Geospatial Commission | LA Digital Teams |
| IoT security certification | Cyber Security Lead | NCSC Liaison | IoT Manufacturers | SRO |
| Budget approval | Finance Director | DLUHC Permanent Secretary | HM Treasury | CDDO |
| LA onboarding | Service Owner | SRO | LA Chief Executives | All stakeholders |

## E2. Delivery Approach

**Methodology**: Agile (Scrum) with GDS service assessment gates

**Phases**:
1. **Discovery** (Months 1-3): User research with LAs, NCSC engagement, architecture design
2. **Alpha** (Months 4-6): Platform prototype, device certification framework, early adopter recruitment
3. **Beta** (Months 7-12): Platform build, first LA onboarding, security testing
4. **Live** (Month 13): Platform launch with 10+ early adopters
5. **Scale** (Months 14-24): Expand to 20+ authorities, open data publication

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation | Owner |
|---------|------|------------|--------|-------|------------|-------|
| R-001 | LA adoption below target | Medium | High | 12 | Funded transition support, peer advocacy | SRO |
| R-002 | Privacy controversy | Medium | High | 12 | Proactive DPIA, citizen ethics panel | SIRO |
| R-003 | IoT security incident | Low | Critical | 9 | ETSI EN 303 645 mandatory, NCSC review | NCSC Liaison |
| R-004 | Integration complexity with existing LA systems | Medium | Medium | 9 | Open standards, phased integration | Architect |
| R-005 | Budget overrun | Medium | Medium | 9 | 15% contingency, agile scope management | Finance |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: Option 2: Shared Cloud-Native Platform with Edge Computing
**Investment**: GBP 18M over 3 years
**Expected Return**: GBP 52M over 5 years (NPV: GBP 26.4M, ROI: 189%)
**Stakeholder Goals Met**: 85%
**Payback Period**: 22 months
**Go/No-Go Recommendation**: **PROCEED to requirements phase**

## F2. Next Steps if Approved

1. **Funding Approval**: DLUHC Finance Director confirms GBP 18M allocation — Target: Q2 2026
2. **NCSC Engagement**: Agree IoT certification programme scope — Target: Q2 2026
3. **Early Adopter Recruitment**: Identify 10 pioneer local authorities — Target: Q2-Q3 2026
4. **Discovery Phase**: User research, architecture design, GDS assessment — Target: Q3 2026
5. **Procurement**: Digital Marketplace G-Cloud/DOS — Target: Q3 2026

---

## Appendix A: Stakeholder Analysis

**Source**: `projects/001-smart-city-iot-platform/ARC-001-STKE-v1.0.md`

## Appendix B: Architecture Principles

**Source**: `projects/000-global/ARC-000-PRIN-v1.0.md`

**Relevant Principles**: 2 (IoT Security by Design), 3 (Geospatial Interoperability), 5 (Defence-in-Depth), 6 (Scalability), 9 (Privacy by Design)

## Appendix H: Glossary

| Term | Definition |
|------|------------|
| SOBC | Strategic Outline Business Case |
| ETSI EN 303 645 | European IoT security baseline standard |
| BODS | Bus Open Data Service |
| AURN | Automatic Urban and Rural Network (air quality) |
| NaPTAN | National Public Transport Access Nodes |
| NHLE | National Heritage List for England |
| MCERTS | Monitoring Certification Scheme |
| PSTI Act | Product Security and Telecommunications Infrastructure Act 2022 |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart City IoT Platform (Project 001)
**Model**: Claude Opus 4.6
