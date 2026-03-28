# Stakeholder Drivers & Goals Analysis: Agricultural Subsidy Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Agricultural Subsidy Management (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DEFRA Environmental Land Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Rural Payments Agency, NFU, Cabinet Office Food Strategy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Agricultural Subsidy Management platform, which manages the post-Brexit Environmental Land Management (ELM) schemes: Sustainable Farming Incentive (SFI), Countryside Stewardship (CS), and Landscape Recovery (LR). The platform replaces the legacy Basic Payment Scheme (BPS) infrastructure inherited from the EU Common Agricultural Policy, serving approximately 100,000 farm holdings across England.

### Key Findings

The strongest alignment exists between DEFRA's policy ambition for ELM and the farming community's need for a simpler, more reliable payment system than the troubled BPS/CAP delivery experience. The primary tension is between the complexity of outcome-based environmental payments (requiring monitoring and verification) and farmers' demand for simplicity and predictability. The Rural Payments Agency (RPA) occupies a critical position -- its historical delivery failures (2015 BPS crisis) create institutional caution that can slow innovation.

### Critical Success Factors

- Delivering a system significantly simpler than the BPS for farmers to use
- Accurately calculating and making payments within government payment SLAs (30 days)
- Supporting outcome-based environmental monitoring without excessive farmer burden
- Managing the transition from BPS to ELM without payment gaps for farmers
- Avoiding a repeat of the 2015 RPA IT crisis

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

DEFRA and farming stakeholders share the goal of a functioning ELM system, but perspectives on complexity, monitoring burden, and payment speed create significant tensions. RPA's risk-averse culture constrains innovation pace.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-1: DEFRA Secretary of State | Minister | HIGH | HIGH | Ministerial briefings |
| S-2: DEFRA Director of ELM | Programme Sponsor | HIGH | HIGH | Programme board |
| S-3: SRO, ELM Programme | Senior Responsible Owner | HIGH | HIGH | Weekly programme board |
| S-4: DEFRA Chief Digital Officer | Digital Strategy Lead | HIGH | HIGH | Architecture reviews |
| S-5: Rural Payments Agency (RPA) CEO | Delivery partner | HIGH | HIGH | Joint delivery board |
| S-6: RPA IT Director | System delivery | HIGH | HIGH | Technical design authority |
| S-7: DEFRA ELM Policy Team | Policy design | MEDIUM | HIGH | Sprint reviews, policy alignment |
| S-8: DEFRA Finance Director | Budget holder | HIGH | MEDIUM | Quarterly reviews |
| S-9: DEFRA SIRO | Information risk | HIGH | MEDIUM | Data governance |
| S-10: Natural England | Environmental advice and monitoring | HIGH | HIGH | Environmental standards design |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-11: National Farmers' Union (NFU) | Industry body | Farmer representative | HIGH | HIGH |
| S-12: Country Land and Business Association (CLA) | Industry body | Landowner representative | MEDIUM | HIGH |
| S-13: Tenant Farmers Association (TFA) | Industry body | Tenant farmer representative | LOW | HIGH |
| S-14: Farm advisers and agents | Private sector | Application support | MEDIUM | HIGH |
| S-15: CDDO | Spend control / assurance | HIGH | MEDIUM |
| S-16: HM Treasury | Budget approver | HIGH | LOW |
| S-17: NAO | Audit and accountability | HIGH | MEDIUM |
| S-18: Cabinet Office (Project 005) | Cross-govt dashboard | Data consumer | MEDIUM | MEDIUM |
| S-19: Environment Agency | Environmental regulation | MEDIUM | MEDIUM |

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Secretary of State -- ELM Policy Delivery

**Stakeholder**: S-1 DEFRA Secretary of State

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver the post-Brexit Environmental Land Management programme on time and on budget, demonstrating that the UK's agricultural policy outside the EU delivers better environmental outcomes while maintaining food production. Avoid a repeat of the 2015 RPA payment crisis.

**Context & Background**: ELM is DEFRA's flagship post-Brexit agricultural policy, replacing the area-based Basic Payment Scheme with outcomes-based environmental payments. The Agriculture Act 2020 provides the legislative foundation. BPS direct payments are being progressively reduced (delinked from 2024), creating urgency to establish functioning ELM schemes before farmers lose income. The 2015 BPS crisis, when RPA failed to make payments to 12,000 farmers on time, created lasting political damage and institutional trauma.

**Driver Intensity**: CRITICAL

**Enablers**:
- Proven technology platform with demonstrated payment reliability
- Phased transition maintaining farmer income continuity
- Positive farmer engagement and scheme uptake
- Clear environmental outcome metrics

**Blockers**:
- RPA institutional caution from 2015 experience
- Policy complexity of outcome-based payments
- Skills gap in DEFRA/RPA for modern digital delivery
- Farmer scepticism from previous IT failures

---

### SD-2: RPA -- Reliable Payment Delivery

**Stakeholder**: S-5 RPA CEO, S-6 RPA IT Director

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Deliver accurate, timely payments to 100,000+ farm holdings without the failures that characterised the 2015 BPS launch. Maintain RPA's recovery of reputation achieved since 2018 through reliable BPS delivery.

**Context & Background**: RPA was placed under special measures following the 2015 BPS crisis, when an IT system failure delayed payments to thousands of farmers, some of whom faced financial ruin. Since then, RPA has rebuilt its reputation through consistent BPS delivery. The ELM transition represents the highest risk to this recovery. The RPA CEO has made clear that reliability must not be sacrificed for innovation.

**Driver Intensity**: CRITICAL

**Enablers**:
- Robust testing and parallel running before go-live
- Phased migration from BPS to ELM
- Proven integration patterns with DEFRA systems
- Adequate development and testing time

**Blockers**:
- Aggressive policy timeline pressuring IT delivery
- Legacy system dependencies (BPS infrastructure)
- Staff attrition (experienced BPS team retiring)
- Complex calculation rules for outcome-based payments

---

### SD-3: Farmers -- Simplicity and Predictability

**Stakeholder**: S-11 NFU, S-12 CLA, S-13 TFA

**Driver Category**: CUSTOMER / FINANCIAL

**Driver Statement**: Access ELM schemes through a simple, reliable digital service that minimises paperwork, provides predictable payments, and does not require specialist advisers. Maintain income continuity during the BPS-to-ELM transition.

**Context & Background**: Farmers overwhelmingly want a simpler system than BPS, which required complex mapping of land parcels, cross-compliance checks, and entitlement trading. ELM adds new complexity through outcome-based payments that require environmental monitoring. The NFU has warned that scheme complexity will deter uptake, particularly among older farmers and small holdings. Approximately 30% of farm holdings are managed by people over 65, many with limited digital literacy.

**Driver Intensity**: CRITICAL

**Enablers**:
- Simple, GOV.UK-standard application process
- Predictable payment schedules (monthly or quarterly)
- Mobile-friendly design for field use
- Integration with mapping systems for land parcel management
- Support for agents acting on behalf of farmers

**Blockers**:
- Outcome-based monitoring complexity
- Digital exclusion of older/rural farmers
- Broadband limitations in rural areas
- Distrust from previous IT failures

---

### SD-4: Natural England -- Environmental Outcomes

**Stakeholder**: S-10 Natural England

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Ensure ELM schemes deliver genuine environmental outcomes (biodiversity, water quality, carbon sequestration, flood risk reduction) and that the platform supports robust outcome monitoring and verification.

**Context & Background**: Natural England provides environmental evidence and advice for ELM scheme design. They are responsible for defining environmental outcome indicators and advising on monitoring approaches. The shift from compliance-based (BPS) to outcomes-based (ELM) payments requires new monitoring capabilities -- satellite imagery, environmental sensors, farm-level reporting, and field inspections.

**Driver Intensity**: HIGH

**Enablers**:
- Satellite/remote sensing integration for land-use monitoring
- Geospatial data integration with OS Data Hub and Rural Land Register
- Standardised environmental outcome indicators
- Farm-level environmental reporting tools

**Blockers**:
- Monitoring costs potentially exceeding payment value for small actions
- Scientific uncertainty about some environmental outcome indicators
- Farmer resistance to monitoring and verification processes

---

### SD-5: NAO -- Avoiding a Repeat Crisis

**Stakeholder**: S-17 NAO

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the ELM programme delivers value for money and avoids the systemic delivery failures documented in the NAO's 2015 report on BPS implementation. The NAO will conduct gateway reviews and publish value-for-money assessments.

**Context & Background**: The NAO's 2015 report "Early review of the Basic Payment Scheme" was highly critical of DEFRA and RPA. The ELM programme will be scrutinised from the outset. The NAO expects robust business case, benefits realisation, and risk management evidence.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Deliver Reliable ELM Payment Service

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: S-3 SRO

**Goal Statement**: Deliver a digital service processing SFI, CS, and LR applications and payments for 100,000+ farm holdings with 99.9% payment accuracy and 100% compliance with 30-day payment SLA, by Q1 2028.

**Success Metrics**:
- **Primary Metric**: Payment accuracy (% of payments correct first time)
- **Secondary Metrics**: Payment timeliness (% within 30-day SLA), farmer satisfaction score, application completion rate

**Baseline**: BPS: 98.5% accuracy, 95% within payment window

**Target**: ELM: > 99.9% accuracy, 100% within 30-day SLA

---

### Goal G-2: Achieve 80% ELM Uptake

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: S-2 Director of ELM

**Goal Statement**: Achieve 80% uptake of at least one ELM scheme among eligible farm holdings (approximately 80,000 holdings) by Q4 2028.

**Success Metrics**:
- **Primary Metric**: Number of holdings with active ELM agreements
- **Secondary Metrics**: Uptake by farm size, region, and scheme type

**Baseline**: SFI 2023 pilot: ~25,000 agreements

**Target**: 80,000+ active agreements across SFI, CS, and LR

---

### Goal G-3: Environmental Outcome Monitoring

**Derived From Drivers**: SD-4

**Goal Owner**: S-10 Natural England

**Goal Statement**: Establish environmental outcome monitoring for all ELM agreements, with remote sensing covering 90% of land-based actions and field inspection for 10% annual sample, by Q2 2028.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome |
|-------------|-----------|----------------|---------|--------------|---------|
| Secretary of State | SD-1 | ELM policy delivery | G-1, G-2 | Payments + uptake | Successful post-Brexit policy |
| RPA | SD-2 | Reliable payments | G-1 | Payment accuracy/timeliness | No repeat of 2015 crisis |
| Farmers | SD-3 | Simplicity, income | G-1, G-2 | Payments + uptake | Maintained livelihoods |
| Natural England | SD-4 | Environmental outcomes | G-3 | Outcome monitoring | Biodiversity, carbon gains |
| NAO | SD-5 | Value for money | G-1 | Payment accuracy | Positive VfM assessment |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Outcome-based monitoring ambition (SD-4) vs farmer simplicity (SD-3). Environmental outcomes require monitoring that farmers see as burdensome.
  - **Resolution Strategy**: Use remote sensing (satellite, drone) for 90% of monitoring, minimising farmer reporting burden. Field inspections for 10% annual sample only.

- **Conflict 2**: Innovation pace (SD-1) vs RPA reliability caution (SD-2). DEFRA wants rapid ELM delivery; RPA wants extensive testing.
  - **Resolution Strategy**: Phased delivery with SFI first (simplest scheme), parallel running with BPS, no big-bang migration.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Agriculture Act 2020 | Legislation | Parliament | ELM powers, BPS delinked payments | legislation.gov.uk |
| NAO BPS Early Review 2015 | Audit report | NAO | Lessons from BPS delivery failure | nao.org.uk |
| Environmental Land Management Schemes | Policy | DEFRA | SFI, CS, LR scheme designs | gov.uk |
| ARC-000-PRIN-v1.0 | Principles | SDG 2 | Governing architecture principles | ARC-000-PRIN-v1.0.md |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Agricultural Subsidy Management
**Model**: Claude Opus 4.6
