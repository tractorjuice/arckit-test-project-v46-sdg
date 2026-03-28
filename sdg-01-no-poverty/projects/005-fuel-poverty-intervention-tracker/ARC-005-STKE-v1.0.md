# Stakeholder Drivers & Goals Analysis: Fuel Poverty Intervention Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
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
| **Distribution** | DESNZ, Ofgem, Energy suppliers, Local Authorities, NEA, Citizens Advice |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Fuel Poverty Intervention Tracker, a system to identify fuel-poor households and coordinate interventions (ECO4 energy efficiency measures, Warm Home Discount, local authority fuel poverty schemes). The UK uses the LILEE definition (Low Income Low Energy Efficiency) — households are fuel-poor if they have low income AND live in a home with poor energy efficiency (EPC rating below Band C). An estimated 3.17 million households in England are fuel-poor.

### Key Findings

The strongest alignment is around improving targeting of fuel poverty interventions — DESNZ, Ofgem, energy suppliers, and local authorities all want to reach the households most in need rather than those who are merely most accessible. The primary tension is between data sharing (which improves targeting) and privacy concerns (sharing income, housing, and energy data across organisations raises significant UK GDPR and citizen trust issues). Energy suppliers obligated under ECO4 have commercial incentives to target the easiest installations rather than the most fuel-poor households — the tracker must rebalance this incentive.

### Critical Success Factors

- Accurate identification of fuel-poor households using linked LILEE data (income, EPC, energy consumption)
- ECO4 and Warm Home Discount targeting improved — interventions reach the most fuel-poor, not just the most accessible
- Data sharing agreements in place with HMRC (income data), DWP (benefit data), DLUHC (EPC data), and Ofgem (energy data)
- Local authorities can identify fuel-poor households in their area for targeted outreach
- Privacy and data protection standards maintained — citizen consent and data minimisation

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong operational alignment on improving intervention targeting. Significant data governance complexity across multiple departments and regulators. Energy supplier cooperation uncertain — ECO4 obligations create perverse incentives around targeting.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DESNZ Minister for Energy | Fuel poverty policy ownership | HIGH | HIGH | Manage Closely |
| DESNZ Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely |
| SRO, Fuel Poverty Programme | Programme sponsor | HIGH | HIGH | Manage Closely |
| DESNZ CDIO | Digital leadership | HIGH | MEDIUM | Keep Satisfied |
| DESNZ Fuel Poverty Statistics Team | Data and evidence | MEDIUM | HIGH | Keep Informed |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Ofgem | Energy regulator | ECO4 and WHD oversight | HIGH | HIGH |
| Energy suppliers (Big 6 + others) | Obligated parties under ECO4 | HIGH | HIGH |
| National Energy Action (NEA) | Fuel poverty charity | Advocacy and delivery | MEDIUM | HIGH |
| Citizens Advice | Consumer advocacy | LOW | HIGH |
| Local Authority housing/energy officers | Delivery partners | MEDIUM | HIGH |
| HMRC | Income data provider | HIGH | MEDIUM |
| DWP | Benefit data provider | HIGH | MEDIUM |
| DLUHC | EPC data owner | MEDIUM | MEDIUM |
| Fuel-poor households | Citizens | Service beneficiaries | LOW | HIGH |
| ECO installers | Delivery contractors | LOW | HIGH |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * DESNZ Minister   |
        |  * HMRC             |  * Permanent Sec.   |
        |  * DWP              |  * SRO              |
        |                     |  * Ofgem            |
        |                     |  * Energy suppliers  |
 P      |                     |                     |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * DLUHC (EPC data) |  * Fuel-poor h/holds|
        |                     |  * NEA              |
        |                     |  * Citizens Advice  |
        |                     |  * Local authorities|
        |                     |  * ECO installers   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DESNZ Minister — Meet Fuel Poverty Target

**Stakeholder**: Minister for Energy, DESNZ

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate measurable progress toward the government's statutory fuel poverty target: as many fuel-poor homes as reasonably practicable to achieve EPC Band C by 2030 (Fuel Poverty (England) Regulations 2014).

**Context & Background**: The statutory target requires improving the energy efficiency of fuel-poor homes. Progress has stalled — the number of fuel-poor households increased from 2.5 million to 3.17 million between 2020 and 2024, driven by energy price increases. The Minister needs better data to target interventions and evidence to demonstrate progress to Parliament. Current measurement relies on modelled estimates with 2-3 year time lag.

**Driver Intensity**: CRITICAL

**Enablers**: Real-time tracking of ECO4 and WHD interventions against the fuel-poor population; linked LILEE data enabling accurate targeting; local authority identification of fuel-poor homes; measurable reduction in fuel poverty gap

**Blockers**: Data sharing barriers between departments; 2-3 year data lag in current measurement; energy price volatility making fuel poverty numbers hard to influence through efficiency alone; insufficient ECO4 funding to reach all fuel-poor homes

---

### SD-2: Ofgem — Ensure ECO4 Meets Its Objectives

**Stakeholder**: Ofgem (Office of Gas and Electricity Markets)

**Driver Category**: REGULATORY / COMPLIANCE

**Driver Statement**: Ensure the Energy Company Obligation (ECO4) scheme delivers energy efficiency improvements to the intended target group — fuel-poor and low-income households — rather than being diverted to easier-to-treat but less needy properties.

**Context & Background**: ECO4 (2022-2026, with expected successor scheme ECO5) obliges large energy suppliers to fund energy efficiency improvements in qualifying homes. Ofgem administers the scheme and verifies compliance. Historically, suppliers have targeted the easiest installations (loft insulation in accessible homes) rather than the most impactful (solid wall insulation in hard-to-treat fuel-poor homes). A tracker that identifies fuel-poor homes would improve targeting.

**Driver Intensity**: HIGH

**Enablers**: Linked dataset identifying fuel-poor homes with low EPC ratings; supplier delivery tracking against fuel-poor targeting criteria; real-time compliance monitoring; post-intervention outcome measurement (did the home improve?)

**Blockers**: Suppliers gaming targeting criteria to claim easier installations; data quality issues in EPC register; inconsistent local authority flex eligibility criteria; supplier resistance to transparency on installation quality

---

### SD-3: Energy Suppliers — Efficient ECO4 Delivery with Clear Targeting

**Stakeholder**: Energy suppliers (British Gas, EDF, E.ON, OVO, Octopus, Scottish Power, and others with ECO4 obligations)

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Receive clear, actionable data on which households qualify for ECO4 to reduce the cost and complexity of customer identification, while meeting Ofgem compliance requirements efficiently.

**Context & Background**: Energy suppliers currently spend significant resources identifying eligible households for ECO4. They use a mix of benefit-checking services, local authority referrals, and customer self-declaration. The process is slow, expensive, and uncertain — suppliers frequently invest in customer identification only to discover ineligibility. A pre-identified pool of eligible fuel-poor homes would reduce identification costs and improve delivery efficiency.

**Driver Intensity**: HIGH

**Enablers**: Pre-qualified pool of eligible properties with EPC data; standardised referral from the tracker; clear eligibility verification API; reduced duplication of identification effort across suppliers

**Blockers**: Data sharing constraints preventing pre-identification; households not engaging with offers; hard-to-treat homes being commercially unattractive regardless of identification; supplier liability if data quality causes misidentification

---

### SD-4: Local Authorities — Identify and Support Fuel-Poor Households Locally

**Stakeholder**: Local Authority housing and energy officers

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Identify fuel-poor households in their area using linked data, enabling targeted outreach, ECO4 referrals, and coordination with local fuel poverty schemes (council tax support, hardship funds, insulation programmes).

**Context & Background**: Local authorities have a statutory duty under the Home Energy Conservation Act 1995 to improve energy efficiency in their area. Many operate fuel poverty schemes but lack data to identify eligible households. The LILEE definition requires income data (from HMRC/DWP) and energy efficiency data (EPC register) — neither of which local authorities hold. A tracker providing area-level fuel poverty data would transform local targeting.

**Driver Intensity**: HIGH

**Enablers**: Area-level fuel poverty maps at LSOA level; household-level identification (with appropriate data sharing basis); integration with council housing systems; ECO4 referral capability; Warm Home Discount auto-enrolment data

**Blockers**: Data sharing agreements not in place; council digital capability varies widely; resource constraints in environmental health and housing teams; households not engaging with cold outreach

---

### SD-5: Fuel-Poor Households — Warmer, Affordable Homes

**Stakeholder**: Approximately 3.17 million fuel-poor households in England

**Driver Category**: CUSTOMER / USER

**Driver Statement**: Live in a warm, energy-efficient home at an affordable cost. Receive energy efficiency improvements and financial support (Warm Home Discount, fuel vouchers) without navigating complex eligibility systems.

**Context & Background**: Fuel-poor households face a cruel trade-off — heat or eat. Many live in poorly insulated homes (EPC D or below) with high energy costs, on incomes that make these costs unaffordable. Fuel poverty causes cold-related illness, exacerbates respiratory and cardiovascular conditions, and contributes to excess winter deaths (estimated 10,000+ per year in England partly attributable to cold housing). Many eligible households do not claim available support because they are unaware of it or find the application process too complex.

**Driver Intensity**: CRITICAL

**Enablers**: Proactive identification and contact by trusted organisations (council, GP, energy supplier); simplified application for ECO4 and WHD; automated eligibility checking reducing burden on households; home visits for assessment and installation

**Blockers**: Distrust of energy suppliers (scam concerns); complex eligibility criteria; poor-quality installations that don't deliver promised savings; language barriers; tenant/landlord disputes over improvement consent; fear that engagement will reveal benefit fraud

---

### SD-6: National Energy Action (NEA) — Evidence-Based Fuel Poverty Policy

**Stakeholder**: National Energy Action

**Driver Category**: ADVOCACY / STRATEGIC

**Driver Statement**: Ensure fuel poverty policy is evidence-based, with real-time data on the fuel-poor population, intervention effectiveness, and remaining fuel poverty gap, enabling NEA to advocate for adequate funding and policy reform.

**Context & Background**: NEA is the UK's leading fuel poverty charity. They campaign for stronger fuel poverty policy, deliver practical energy advice, and conduct research. Currently, fuel poverty statistics are published with a 2-3 year lag, making real-time policy advocacy difficult. A tracker with current data would transform NEA's ability to hold government accountable for progress toward the statutory target.

**Driver Intensity**: MEDIUM

**Enablers**: Real-time fuel poverty dashboard; intervention tracking showing coverage vs need; fuel poverty gap analysis by region and tenure; EPC improvement tracking pre/post intervention

**Blockers**: Data quality issues undermining credibility; government controlling access to data for political management; tracker focused only on ECO4 (ignoring fuel poverty drivers like income and energy prices)

---

## Driver-to-Goal Mapping

### Goal G-1: Fuel Poverty Targeting Accuracy

**Derived From Drivers**: SD-1, SD-2, SD-3, SD-4

**Goal Owner**: SRO

**Goal Statement**: Achieve 80% accuracy in identifying fuel-poor households (validated against LILEE definition) for ECO4 and local authority interventions by March 2028.

**Baseline**: Current ECO4 targeting accuracy estimated at 40-50% (many interventions reach non-fuel-poor households).

**Target**: 80% of interventions delivered to verified fuel-poor households.

---

### Goal G-2: Real-Time Fuel Poverty Dashboard

**Derived From Drivers**: SD-1, SD-6

**Goal Owner**: DESNZ Fuel Poverty Statistics Team

**Goal Statement**: Provide a real-time national fuel poverty dashboard updated quarterly (replacing the current 2-3 year data lag) by March 2028.

**Baseline**: Annual fuel poverty statistics published 2-3 years in arrears.

**Target**: Quarterly dashboard with data no more than 3 months old.

---

### Goal G-3: ECO4 Intervention Coverage

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: Ofgem

**Goal Statement**: Ensure 60% of ECO4 interventions target homes with EPC Band D or below occupied by LILEE-qualifying households by March 2027.

**Baseline**: Estimated 35% of ECO4 interventions currently target the most fuel-poor homes.

**Target**: 60% targeting fuel-poor homes (Band D or below, LILEE-qualifying).

---

### Goal G-4: Warm Home Discount Auto-Enrolment

**Derived From Drivers**: SD-5

**Goal Owner**: DESNZ

**Goal Statement**: Achieve 90% auto-enrolment of eligible households into the Warm Home Discount scheme by March 2028, eliminating the need for eligible households to apply.

**Baseline**: Approximately 70% of eligible households receive WHD (30% do not claim).

**Target**: 90% coverage through automated eligibility matching.

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DESNZ and Ofgem (SD-1, SD-2) want household-level fuel poverty identification; HMRC and DWP are cautious about sharing income and benefit data for this purpose. Resolution: Data sharing under Digital Economy Act 2017 public interest powers. Data minimised to eligibility flags (yes/no) rather than income amounts. Independent DPIA reviewed by ICO.

- **Conflict 2**: Ofgem (SD-2) wants suppliers to target the most fuel-poor homes; energy suppliers (SD-3) have commercial incentives to target easier installations. Resolution: Tracker provides ranked priority list weighted by fuel poverty severity. ECO4 scoring adjusted by Ofgem to incentivise hard-to-treat fuel-poor homes. Compliance monitoring through tracker data.

**Synergies**:

- Local authorities (SD-4) and energy suppliers (SD-3) both benefit from pre-identified eligible households — reduces duplication of effort
- NEA (SD-6) and DESNZ (SD-1) both need real-time fuel poverty data — shared dashboard serves both

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Fuel Poverty (England) Regulations 2014 | Legislation | legislation.gov.uk | Statutory LILEE definition and target | N/A |
| ECO4 Order 2022 | Legislation | legislation.gov.uk | Energy company obligations | N/A |
| Warm Home Discount Regulations | Legislation | legislation.gov.uk | WHD eligibility and auto-enrolment | N/A |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 1 Programme | Governing principles | projects/000-global/ |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fuel Poverty Intervention Tracker
**Model**: Claude Opus 4.6
