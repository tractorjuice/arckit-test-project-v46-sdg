# Stakeholder Drivers & Goals Analysis: Social Prescribing Link Worker System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Social Prescribing Link Worker System (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Social Prescribing Digital Programme, NHS England |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Social Prescribing Programme Board, NHS England |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Social Prescribing Link Worker System — a platform connecting patients with community support services such as exercise groups, befriending services, debt advice, arts activities, and nature-based interventions. Link workers act as the bridge between NHS primary care and the voluntary, community, and social enterprise (VCSE) sector.

### Key Findings

Social prescribing operates at the intersection of the NHS and the voluntary sector — two worlds with fundamentally different cultures, funding models, and technology maturity. The strongest alignment exists around reducing GP workload for non-clinical presentations and improving patient wellbeing outcomes. The most significant conflict is between the NHS's need for structured data and outcome measurement (to justify funding) and the VCSE sector's concern that excessive data collection and reporting requirements will overwhelm small community organisations and damage the trusting, informal relationships that make social prescribing effective.

### Critical Success Factors

- Link worker referral workflow integrated with GP clinical systems (EMIS, TPP SystmOne) to avoid double-keying
- Community organisation directory maintained and accurate — services must be current, with capacity data
- Outcome measurement that demonstrates impact without overburdening VCSE organisations
- Platform accessible and usable by small community organisations with limited IT capability
- Patient consent and data sharing governance clear and simple for link workers to explain

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Broad consensus that social prescribing improves wellbeing and reduces GP demand. Tensions between NHS data requirements and VCSE sector capacity, between national standardisation and local community diversity, and between demonstrating measurable outcomes and respecting the qualitative nature of social prescribing impact.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| NHS England Director of Primary Care | Strategic sponsor | HIGH | HIGH | Manage Closely — Primary care strategy alignment |
| SRO, Social Prescribing Digital | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| NHS England Personalised Care Team | Social prescribing policy | HIGH | HIGH | Manage Closely — Policy requirements |
| Primary Care Network (PCN) Clinical Directors | Local primary care leadership | HIGH | HIGH | Manage Closely — Adoption, integration requirements |
| Social Prescribing Link Workers | Frontline users | MEDIUM | HIGH | Keep Informed — User requirements, co-design |
| GP Partners | Referring clinicians | MEDIUM | HIGH | Keep Informed — Referral workflow design |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| National Academy for Social Prescribing (NASP) | National body | Strategic partner | HIGH | HIGH |
| VCSE organisations (community groups, charities) | Voluntary sector | Service providers | MEDIUM | HIGH |
| Local authorities | Local government | Community service commissioning | MEDIUM | HIGH |
| Sport England | NDPBs | Physical activity programmes | LOW | HIGH |
| Patients (social prescribing recipients) | Citizens | Service users | LOW | HIGH |
| HM Treasury | Government | Funding | HIGH | MEDIUM |
| NHSE Digital | NHS | GP system integration | MEDIUM | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * NHS Eng Dir PC   |
        |                     |  * SRO              |
        |                     |  * NHS Eng Pers Care|
        |                     |  * PCN Clin Dirs    |
 P      |                     |  * NASP             |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * Sport England    |  * Link Workers     |
        |                     |  * GPs              |
        |                     |  * VCSE Orgs        |
        |                     |  * Local Authorities|
        |                     |  * Patients         |
        |                     |  * NHSE Digital     |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: NHS England Primary Care — Reduce GP Workload for Non-Clinical Presentations

**Stakeholder**: NHS England Director of Primary Care

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Reduce the 20-30% of GP consultations that are primarily about non-clinical social needs (loneliness, housing, debt, inactivity) by providing a structured digital pathway from GP referral to community support, freeing GP time for clinical care.

**Context & Background**: GPs report that a significant proportion of consultations (estimated 20-30%) involve patients whose primary need is social rather than clinical — loneliness, social isolation, housing problems, financial difficulty, lack of physical activity. These patients repeatedly consult their GP because they have nowhere else to go. Social prescribing provides an alternative pathway, but without a digital system linking GPs to link workers and community services, the referral process is manual, inconsistent, and poorly tracked.

**Driver Intensity**: HIGH

---

### SD-2: VCSE Organisations — Simple Referral Management Without Bureaucratic Burden

**Stakeholder**: Voluntary, community, and social enterprise organisations

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Receive referrals from link workers through a simple digital system that does not require complex IT infrastructure, extensive data entry, or onerous reporting requirements that divert resources from delivering services to people who need them.

**Context & Background**: The VCSE sector is enormously diverse — from large national charities to a single volunteer running a walking group. Most community organisations have minimal IT capability (a mobile phone, perhaps a shared laptop). They are already stretched by funding reporting requirements from multiple commissioners. Any digital platform must be accessible to a volunteer with a smartphone and must not create additional administrative burden that makes community organisations reluctant to participate.

**Driver Intensity**: HIGH

---

### SD-3: Patients — Access to Local Support Without Stigma

**Stakeholder**: Social prescribing recipients (patients)

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Access community activities and support that improve wellbeing — exercise groups, befriending services, arts activities, nature walks, debt advice — through a warm, personal introduction from a link worker, not a cold referral into an anonymous system.

**Context & Background**: Social prescribing works because of the human relationship — the link worker understands the patient's situation, identifies suitable activities, and provides a warm introduction. The patient feels supported, not processed. The digital platform must support this human-centred approach, not replace it with an impersonal digital marketplace. Patients often feel stigmatised about needing help with social issues; the system must feel supportive and discreet.

**Driver Intensity**: MEDIUM

---

### SD-4: National Academy for Social Prescribing — Evidence Base and Outcome Measurement

**Stakeholder**: National Academy for Social Prescribing (NASP)

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Build a robust national evidence base for social prescribing by collecting consistent outcome data across the country, demonstrating the impact of social prescribing on patient wellbeing, NHS demand, and community cohesion to secure continued government funding.

**Context & Background**: Social prescribing has strong anecdotal support and growing evidence of benefit, but the evidence base is hampered by inconsistent data collection, lack of standardised outcomes, and the difficulty of attributing health improvements to specific social prescribing interventions. NASP needs a national platform that collects consistent minimum dataset information to build the evidence base needed to secure long-term NHS funding for social prescribing link workers.

**Driver Intensity**: HIGH

---

### SD-5: PCN Clinical Directors — Integration with GP Clinical Systems

**Stakeholder**: Primary Care Network Clinical Directors

**Driver Category**: OPERATIONAL

**Driver Statement**: Ensure social prescribing referrals can be made from within the GP clinical system (EMIS, SystmOne) without opening a separate application, and that referral outcomes are visible in the patient's GP record.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce GP Non-Clinical Consultations by 15%

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: NHS England Director of Primary Care

**Goal Statement**: Reduce GP consultations for primarily non-clinical social needs by 15% within participating PCNs within 18 months of platform deployment, through systematic social prescribing referral integrated with GP workflows.

**Baseline**: Estimated 20-30% of consultations for non-clinical needs

**Target**: 15% reduction in these consultations at participating PCNs

---

### Goal G-2: 90% of VCSE Organisations Rate Platform as "Easy to Use"

**Derived From Drivers**: SD-2

**Goal Owner**: SRO

**Goal Statement**: Achieve a user satisfaction score where 90% of participating VCSE organisations rate the platform as "easy to use" or "very easy to use" on the quarterly satisfaction survey.

---

### Goal G-3: National Social Prescribing Minimum Dataset Collection

**Derived From Drivers**: SD-4

**Goal Owner**: NASP

**Goal Statement**: Collect the NASP Social Prescribing Minimum Dataset from at least 80% of social prescribing referrals nationally within 2 years, enabling robust outcome analysis and evidence-based policy development.

**Baseline**: < 30% of referrals have consistent outcome data

**Target**: 80% minimum dataset completion rate

---

### Goal G-4: Community Service Directory Accuracy Above 95%

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: SRO

**Goal Statement**: Maintain a community service directory with 95%+ accuracy (services listed are currently operating, have capacity, and contact details are correct), validated through quarterly accuracy audits.

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: NASP (SD-4) needs consistent outcome data collection, but VCSE organisations (SD-2) fear that data requirements will be burdensome and deter small community groups from participating.
  - **Resolution Strategy**: Implement a **minimal mandatory dataset** (5-6 fields per referral outcome) that can be completed in under 2 minutes via smartphone. Richer outcome data is optional. Automated pre-population where possible. Show VCSE organisations how the data helps them demonstrate impact for their own funding applications.

- **Conflict 2**: PCN Clinical Directors (SD-5) want GP system integration, but the platform must also work for link workers who are not NHS employees and do not have access to NHS clinical systems.
  - **Resolution Strategy**: Design a **dual-interface model**: GP referral integration via EMIS/SystmOne for clinical teams (referral created within the clinical system), and a standalone web/mobile interface for link workers and VCSE organisations (accessible without NHS network or NHS CIS2 smartcard). Data flows between the two via secure APIs.

**Synergies**:

- **Synergy 1**: SD-1 (reduce GP workload) and SD-3 (patient access to support) both benefit from efficient referral — GPs spend less time on non-clinical consultations, patients get community support faster
- **Synergy 2**: SD-4 (evidence base) supports SD-1 (GP workload reduction) by providing the data to justify continued NHS investment in social prescribing

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform design | Product Manager | SRO | Link Workers, VCSE, Patients, GPs | All |
| GP system integration | Lead Developer | NHSE Digital | EMIS Health, TPP, PCN CDs | All |
| Minimum dataset design | NASP Data Lead | NASP | VCSE representative, Researchers | All |
| Community directory maintenance | Directory Manager | SRO | Local Authorities, VCSE | All |
| Data sharing governance | IG Lead | Caldicott Guardian | ICO, Patients | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| NHS Long Term Plan | Strategy | NHS England | Social prescribing commitment | N/A — external reference |
| NASP Social Prescribing Framework | Framework | NASP | Link worker model, outcomes | N/A — external reference |
| NHS Universal Personalised Care | Policy | NHS England | Personalised care model | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Social Prescribing Link Worker System
**Model**: Claude Opus 4.6
