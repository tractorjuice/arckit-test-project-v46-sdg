# Strategic Outline Business Case (SOBC): Fuel Poverty Intervention Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Fuel Poverty Intervention Tracker (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Fuel Poverty Programme, DESNZ |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Programme Board, HM Treasury, Ofgem, HMRC, DWP |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in a Fuel Poverty Intervention Tracker, following the HM Treasury Green Book Five Case Model. It is informed by ARC-005-STKE-v1.0 (stakeholder analysis) and ARC-005-REQ-v1.0 (requirements). The tracker addresses the statutory fuel poverty target (Fuel Poverty (England) Regulations 2014) by improving identification and targeting of fuel-poor households for ECO4, Warm Home Discount, and local authority interventions.

---

## Executive Summary

**Purpose**: An estimated 3.17 million English households are fuel-poor under the LILEE definition (Low Income Low Energy Efficiency). The government has a statutory target to improve fuel-poor homes to EPC Band C by 2030, but progress has stalled. Current intervention targeting is inaccurate (~40%), fuel poverty data is 2-3 years out of date, and 30% of eligible households miss the Warm Home Discount. This business case seeks GBP 35M over 5 years for a data linkage and intervention tracking system.

**Problem Statement**: Fuel poverty interventions (ECO4, WHD, local schemes) are poorly targeted because no system links income data with energy efficiency data at household level. Energy suppliers target easy installations, not the most fuel-poor homes. DESNZ cannot track progress in real time. Eligible households miss support they are entitled to.

**Proposed Solution**: A secure data linkage system combining HMRC income data, DWP benefit data, DLUHC EPC register data, and Ofgem energy data to identify fuel-poor households, direct interventions, auto-enrol WHD, and track progress toward the statutory target.

**Strategic Fit**: Directly supports SDG 1: No Poverty by addressing energy poverty as a dimension of income poverty. Delivers the statutory fuel poverty target (Fuel Poverty (England) Regulations 2014). Aligns with Net Zero Strategy (energy efficiency reduces both fuel poverty and carbon emissions).

**Investment Required**: GBP 35M over 5 years

- Capital: GBP 22M
- Operational (5 years): GBP 13M

**Expected Benefits**: GBP 215M over 10 years

- Improved ECO4 targeting (GBP 150M in better-directed interventions reaching fuel-poor homes)
- WHD auto-enrolment (GBP 30M in additional WHD payments reaching eligible households)
- Energy bill savings for fuel-poor households from better-targeted interventions (GBP 25M)
- NHS cost avoidance from reduced cold-related illness (GBP 10M)

**Return on Investment**:

- NPV: GBP 112M (discounted at 3.5%)
- Payback Period: 28 months
- ROI: 514% over 10 years

**Recommended Option**: Option 2: Linked Data Platform with Secure Processing Environment

**Key Risks**:

1. HMRC data sharing agreement not achieved — mitigated by early Ministerial engagement, Digital Economy Act powers
2. Privacy concerns about linked income and housing data — mitigated by ICO engagement, strict data minimisation, aggregate-only outputs
3. EPC data coverage insufficient — mitigated by modelled estimates using VOA property data

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The UK government has a statutory obligation under the Fuel Poverty (England) Regulations 2014 to improve fuel-poor homes to EPC Band C by 2030. The primary instruments are ECO4 (energy supplier obligations, approximately GBP 1 billion/year), the Warm Home Discount (GBP 150/year per eligible household), and local authority schemes. However:

- **Targeting is poor**: An estimated 40% of ECO4 interventions reach non-fuel-poor households because suppliers lack data to identify fuel-poor homes accurately
- **Data is stale**: Fuel poverty statistics are published 2-3 years in arrears, preventing real-time policy adjustment
- **Eligible households miss out**: 30% of WHD-eligible households do not receive the discount because they do not apply
- **No intervention coordination**: Multiple schemes (ECO4, WHD, local authority, charitable) operate independently, sometimes duplicating effort on the same household while missing others entirely

**Consequences of Inaction**:

- Statutory target missed — 3.17 million households remain fuel-poor with inadequate progress
- GBP 400M+ per year of ECO4 funding partially misdirected to non-fuel-poor households
- An estimated 10,000+ excess winter deaths per year partly attributable to cold housing
- GBP 1.4 billion annual NHS cost from cold-related illness (respiratory, cardiovascular, mental health)
- Continued fuel poverty contributes to poverty traps — high energy costs force trade-offs on food, clothing, and other essentials

### A1.2 Strategic Alignment

- **SDG 1: No Poverty**: Fuel poverty is a direct dimension of income poverty — cold homes cause health harm, educational underachievement, and economic disadvantage
- **Fuel Poverty (England) Regulations 2014**: Statutory target — this tracker is the primary mechanism for improved targeting
- **Net Zero Strategy**: Energy efficiency improvements reduce both fuel poverty and carbon emissions — co-benefit
- **Levelling Up**: Fuel poverty is geographically concentrated in northern England, coastal areas, and rural communities
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 5 (Security by Design), 7 (Data Sovereignty), 8 (Privacy by Design), 10 (Single Source of Truth)

## B2. Options Analysis

### Option 0: Do Nothing

**Costs (5-year)**: GBP 0

**Benefits**: GBP 0

**Consequences**: Statutory target missed. GBP 2B+ in ECO4 funding continues to be partially misdirected. 30% of WHD-eligible households continue to miss out. No real-time data for policy.

**Recommendation**: **Reject** — Statutory obligation not met. Intervention funding wasted.

---

### Option 1: Enhanced Survey-Based Estimation

**Description**: Increase the English Housing Survey sample size to improve fuel poverty estimation accuracy and timeliness. No data linkage.

**Costs (5-year)**: GBP 8M

**Benefits (10-year)**: GBP 15M (better estimates but no targeting improvement)

**Pros**: Low complexity, no data sharing required

**Cons**: Survey-based, not population-based — cannot identify individual households. Does not improve ECO4 targeting. Does not enable WHD auto-enrolment. Data still modelled with 12-18 month lag.

**Stakeholder Goals Met**: 15%

**Recommendation**: **Reject** — Does not solve the targeting problem.

---

### Option 2: Linked Data Platform with Secure Processing Environment (RECOMMENDED)

**Description**: Secure data linkage platform combining HMRC income data, DWP benefit data, DLUHC EPC data, and Ofgem energy data within an accredited secure research environment (ONS SRS model). Individual-level data never leaves the secure environment; only approved aggregate outputs and eligibility flags are released.

**Costs (5-year)**: GBP 35M

- Capital: GBP 22M (secure environment, data linkage engine, dashboards, APIs)
- Operational: GBP 13M (data management, security, quarterly refresh, support)

**Benefits (10-year)**: GBP 215M

| Benefit | Type | Annual (at maturity) | 10-Year Total |
|---------|------|---------------------|---------------|
| Improved ECO4 targeting (redirecting GBP 400M/yr to fuel-poor homes) | EFFICIENCY | GBP 18M | GBP 150M |
| WHD auto-enrolment (additional eligible households receiving GBP 150/yr) | FINANCIAL | GBP 4M | GBP 30M |
| Household energy bill savings from better interventions | FINANCIAL | GBP 3M | GBP 25M |
| NHS cost avoidance (cold-related illness reduction) | HEALTH | GBP 1.5M | GBP 10M |

**NPV**: GBP 112M | **Payback**: 28 months | **ROI**: 514%

**Stakeholder Goals Met**: 90%

**Recommendation**: **ACCEPT** — Strongly positive NPV, delivers statutory obligation, co-benefits for health and climate.

---

### Option 3: Open Data Approach

**Description**: Publish modelled fuel poverty risk scores at postcode level using publicly available data (EPC register, IMD, census), without linking individual income data.

**Costs (5-year)**: GBP 5M

**Benefits (10-year)**: GBP 30M (modest targeting improvement using proxies)

**Pros**: No data sharing agreements needed, quick to deliver, open data transparency

**Cons**: Accuracy limited to ~55% (postcode-level proxy, not household-level). Cannot enable WHD auto-enrolment (requires individual matching). Misses fuel-poor households in affluent postcodes and includes non-fuel-poor households in deprived postcodes.

**Stakeholder Goals Met**: 35%

**Recommendation**: **Reject** — Insufficient accuracy. Does not enable WHD auto-enrolment or household-level targeting.

---

## B3. Recommended Option

**Option 2: Linked Data Platform** — the only option that delivers household-level fuel poverty identification, enables WHD auto-enrolment, and provides the targeting accuracy required to meet the statutory target. Strongly positive NPV (GBP 112M) with 28-month payback. Data governance risks managed through secure research environment and ICO engagement.

**Sensitivity Analysis**:

- If costs increase 30%: NPV still GBP 98M (strongly positive)
- If benefits reduce 30%: NPV still GBP 52M (positive)
- If HMRC data sharing delayed 12 months: Payback extends to 40 months — still acceptable
- Combined pessimistic scenario (costs +30%, benefits -30%): NPV GBP 38M — still positive

**Optimism Bias Adjustment** (HM Treasury Green Book):

- Standard uplift for data/analytics programme: +30%
- Adjusted Total Cost: GBP 35M + GBP 10.5M = GBP 45.5M (with optimism bias)
- NPV with optimism bias: GBP 101M — still strongly positive

---

# PART C: COMMERCIAL CASE

**Procurement Route**: ONS Secure Research Service for data linkage environment (existing facility). Digital Marketplace (G-Cloud for cloud dashboards, DOS for development teams).

**Contract Approach**:

- Secure research environment: Service agreement with ONS (or equivalent accredited provider)
- Dashboard and API development: Agile delivery through DOS outcomes contracts
- Data management and refresh: Managed service (GBP 2.5M/year steady-state)

**Key Contract Terms**:

- All data processed within UK sovereign accredited secure environment
- Crown IP for all bespoke development
- No subprocessor access to linked individual-level data

---

# PART D: FINANCIAL CASE

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 7M | GBP 8M | GBP 4M | GBP 2M | GBP 1M | GBP 22M |
| OpEx | GBP 1.5M | GBP 2M | GBP 2.5M | GBP 3M | GBP 4M | GBP 13M |
| **Total** | **GBP 8.5M** | **GBP 10M** | **GBP 6.5M** | **GBP 5M** | **GBP 5M** | **GBP 35M** |

**Funding Source**: DESNZ fuel poverty programme budget, supplemented by Ofgem ECO4 administration levy.

**Affordability**: Programme represents less than 1% of annual ECO4 scheme value (GBP 1B/year). The targeting improvement alone (redirecting misdirected ECO4 funding to fuel-poor homes) justifies the investment many times over.

---

# PART E: MANAGEMENT CASE

**Programme Governance**: DESNZ Programme Board chaired by SRO, with Ofgem, HMRC, DWP, DLUHC, and NEA representation. Independent data governance panel with ICO observer.

**Key Risks**:

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| HMRC data sharing agreement not achieved | MEDIUM | CRITICAL | Early Ministerial engagement, DEA public interest case, legal advice |
| Privacy and civil liberties concerns | HIGH | HIGH | ICO engagement, DPIA, strict data minimisation, aggregate-only external outputs, independent governance |
| EPC data coverage below 60% | MEDIUM | HIGH | Modelled estimates from VOA property data, targeted EPC assessment programme |
| Address matching failure rate | MEDIUM | MEDIUM | UPRN-based matching, probabilistic algorithms, manual review |
| Energy suppliers do not adopt tracker for ECO4 | MEDIUM | MEDIUM | Ofgem adjusts ECO4 scoring to incentivise tracker-sourced referrals |

**Timeline**:

| Phase | Start | End | Key Deliverable |
|-------|-------|-----|-----------------|
| Data sharing agreements | Q2 2026 | Q4 2026 | HMRC, DWP, DLUHC, Ofgem agreements signed |
| Secure environment setup | Q3 2026 | Q1 2027 | Accredited data linkage environment operational |
| LILEE data linkage pilot | Q1 2027 | Q3 2027 | Pilot with 3 local authority areas |
| WHD auto-enrolment | Q3 2027 | Q4 2027 | Automated matching for 2027-28 WHD cycle |
| National dashboard (beta) | Q4 2027 | Q2 2028 | Quarterly fuel poverty dashboard live |
| ECO4 targeting system | Q1 2028 | Q3 2028 | Supplier-facing eligible property API |
| Full national rollout | Q3 2028 | | All English local authorities with access |

**Critical Path**: Data sharing agreements are on the critical path. Without HMRC agreement, the LILEE calculation cannot be performed and the entire programme is blocked. Ministerial engagement and legal groundwork must begin immediately upon SOBC approval.

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| DESNZ Permanent Secretary | Accounting Officer | [ ] Approved | PENDING |
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| HM Treasury | Funding Approval | [ ] Approved | PENDING |
| Ofgem | Regulatory Partner | [ ] Approved | PENDING |
| ICO | Data Protection Oversight | [ ] Approved | PENDING |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| LILEE | Low Income Low Energy Efficiency — the statutory fuel poverty metric |
| ECO4 | Energy Company Obligation (fourth iteration) — energy efficiency scheme funded by energy suppliers |
| WHD | Warm Home Discount — annual GBP 150 energy bill rebate for eligible households |
| EPC | Energy Performance Certificate — rating of a dwelling's energy efficiency (A-G) |
| UPRN | Unique Property Reference Number — nationally unique address identifier |
| Fuel Poverty Gap | Difference between a household's actual energy costs and the costs they would face in a home meeting minimum efficiency standards |
| ONS SRS | Office for National Statistics Secure Research Service — accredited environment for sensitive data analysis |
| DEA | Digital Economy Act 2017 — provides powers for data sharing in the public interest |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — Enterprise Architecture Principles (SDG 1: No Poverty)
- ARC-005-STKE-v1.0 — Stakeholder Drivers & Goals Analysis
- ARC-005-REQ-v1.0 — Requirements Specification
- Fuel Poverty (England) Regulations 2014
- HM Treasury Green Book — Appraisal and evaluation guidance
- Annual Fuel Poverty Statistics (DESNZ)

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fuel Poverty Intervention Tracker
**Model**: Claude Opus 4.6
