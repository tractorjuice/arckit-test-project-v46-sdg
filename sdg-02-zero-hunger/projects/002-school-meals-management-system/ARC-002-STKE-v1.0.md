# Stakeholder Drivers & Goals Analysis: School Meals Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | School Meals Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DfE Free School Meals Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Digital, HMRC, DWP, Local Authorities, Cabinet Office Food Strategy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the School Meals Management System, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The system manages free school meals (FSM) eligibility determination, auto-enrolment through the Eligibility Checking Service (ECS), and meal delivery tracking for approximately 1.9 million eligible pupils across England.

### Key Findings

The strongest driver alignment exists between the DfE's policy mandate to reduce child hunger and HMRC/DWP's ability to provide benefits data for eligibility verification. The primary tension is between the desire for maximum uptake (auto-enrolling all eligible families) and data protection requirements for children's personal data. Local authorities occupy a critical intermediary role but have widely varying digital capabilities, creating an implementation challenge.

### Critical Success Factors

- Achieving seamless integration with HMRC and DWP benefits systems for auto-eligibility checking
- Ensuring all 152 local authorities can interact with the system regardless of their technical maturity
- Protecting children's personal data to the highest standards (ICO Children's Code)
- Reducing the FSM eligibility gap (estimated 11% of eligible families not claiming)

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Stakeholders share a common goal of ensuring no eligible child misses out on free school meals. Tensions exist around data sharing between departments and the burden on local authorities, but these are implementation challenges rather than strategic conflicts.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-1: DfE Minister for Schools | Minister | HIGH | HIGH | Ministerial briefings, policy alignment |
| S-2: DfE Director of School Food | Programme Sponsor | HIGH | HIGH | Programme board, strategic direction |
| S-3: SRO, FSM Programme | Senior Responsible Owner | HIGH | HIGH | Weekly programme board |
| S-4: DfE Chief Digital Officer | Digital Strategy Lead | HIGH | HIGH | Architecture reviews, technology decisions |
| S-5: DfE Data Protection Officer | Privacy Lead | HIGH | MEDIUM | DPIA reviews, data governance |
| S-6: DfE Finance Director | Budget Holder | HIGH | MEDIUM | Quarterly business case reviews |
| S-7: DfE Schools Policy Team | Policy Analysts | MEDIUM | HIGH | Sprint reviews, policy input |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-8: HMRC Benefits Data Team | HMRC | Data provider (tax credits, UC) | HIGH | MEDIUM |
| S-9: DWP Universal Credit Team | DWP | Data provider (UC entitlements) | HIGH | MEDIUM |
| S-10: Local Authority Education Leads (x152) | Local Authorities | Service delivery partners | MEDIUM | HIGH |
| S-11: School Business Managers | Schools | End users, meal delivery | LOW | HIGH |
| S-12: Parents and Carers | Citizens | Beneficiaries | LOW | HIGH |
| S-13: School Catering Providers | Private sector | Meal delivery data | LOW | MEDIUM |
| S-14: Cabinet Office (Project 005) | Cross-govt dashboard | Data consumer | MEDIUM | MEDIUM |
| S-15: CDDO | Spend control / assurance | HIGH | MEDIUM |
| S-16: ICO | Data protection regulator | HIGH | MEDIUM |
| S-17: Food Foundation / Child Poverty Action Group | Charities | Campaign groups, advocacy | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend | HIGH / HIGH | Manage Closely -- steering board |
| Service Owner | Owns end-to-end FSM eligibility service | HIGH / HIGH | Manage Closely -- service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed -- sprint reviews |
| Delivery Manager | Manages delivery cadence and risks | MEDIUM / HIGH | Keep Informed -- stand-ups |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied -- spend control |
| DfE CDIO | Departmental digital strategy | HIGH / MEDIUM | Keep Satisfied -- strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Protective security risk at board level | HIGH / MEDIUM | Keep Satisfied -- security risk escalation |
| DfE SIRO | Information and cyber security risk, DPIA sign-off | HIGH / MEDIUM | Keep Satisfied -- information risk decisions |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed -- security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * S-5 DPO          |  * S-1 Minister     |
        |  * S-6 Finance Dir  |  * S-2 Director     |
        |  * S-8 HMRC         |  * S-3 SRO          |
        |  * S-9 DWP          |  * S-4 CDO          |
 P      |  * S-15 CDDO        |                     |
 O      |  * S-16 ICO         |                     |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * S-13 Catering    |  * S-7 Policy Team  |
        |    Providers        |  * S-10 Local Auth  |
        |                     |  * S-11 Schools     |
        |                     |  * S-12 Parents     |
        |                     |  * S-14 Cab Office  |
        |                     |  * S-17 Charities   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DfE Minister for Schools -- Child Hunger Elimination

**Stakeholder**: S-1 DfE Minister for Schools

**Driver Category**: STRATEGIC / CUSTOMER

**Driver Statement**: Ensure every eligible child in England receives free school meals, closing the estimated 11% eligibility gap where families do not claim despite being entitled. Demonstrate visible progress on child poverty reduction commitments.

**Context & Background**: Approximately 1.9 million pupils receive FSM in England. The Food Foundation estimates 215,000 additional children are eligible but not enrolled, often due to application barriers, stigma, or parents not knowing they qualify. Auto-enrolment through benefits data matching can eliminate administrative barriers. Political pressure from opposition and campaign groups (Marcus Rashford's campaign) keeps this high on the ministerial agenda.

**Driver Intensity**: CRITICAL

**Enablers**:
- Seamless integration with HMRC/DWP benefits data
- Auto-enrolment capability removing application barriers
- Opt-out rather than opt-in model where legally permissible

**Blockers**:
- Data protection constraints on cross-departmental data sharing
- Parental consent requirements for children's data
- Local authority variability in systems and processes

**Related Stakeholders**: S-2 (Director), S-7 (Policy Team), S-17 (Charities)

---

### SD-2: DfE Director of School Food -- Programme Efficiency

**Stakeholder**: S-2 DfE Director of School Food

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Replace the fragmented landscape of 152 different local authority systems with a single national platform, reducing administrative costs and enabling accurate national reporting on FSM uptake and delivery.

**Context & Background**: Currently, each local authority operates its own eligibility checking process. Some use the DfE Eligibility Checking Service (ECS) API, others use manual processes. Data quality and timeliness vary enormously. The Director needs a single source of truth for FSM statistics to report to Parliament and to distribute Pupil Premium funding accurately.

**Driver Intensity**: HIGH

**Enablers**:
- Standardised API for all local authorities
- Central data warehouse for national reporting
- Automated Pupil Premium funding calculations

**Blockers**:
- Local authority resistance to centralisation
- Legacy systems in smaller local authorities
- Political sensitivity of centralising a locally-delivered service

**Related Stakeholders**: S-3 (SRO), S-10 (Local Authorities), S-6 (Finance)

---

### SD-3: HMRC Benefits Data Team -- Secure Data Sharing

**Stakeholder**: S-8 HMRC Benefits Data Team

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Provide benefits data for FSM eligibility verification while maintaining strict compliance with HMRC data protection obligations and the Commissioners for Revenue and Customs Act 2005 (CRCA), which governs disclosure of taxpayer information.

**Context & Background**: HMRC holds tax credit and Universal Credit data that determines FSM eligibility. The CRCA creates strict legal boundaries on sharing this data. HMRC needs a lawful gateway (currently provided by regulations under the Education Act 1996) and technical safeguards ensuring data is used only for the stated purpose. Any breach could trigger parliamentary scrutiny and loss of public trust in the tax system.

**Driver Intensity**: HIGH

**Enablers**:
- Clear legal gateway under Education Act 1996 regulations
- Purpose-limited API with audit trail
- Data minimisation (yes/no eligibility response, not raw benefits data)

**Blockers**:
- Legal complexity of expanding data sharing beyond current scope
- Technical constraints in HMRC legacy systems
- HMRC institutional caution about data disclosure

**Related Stakeholders**: S-9 (DWP), S-5 (DPO), S-16 (ICO)

---

### SD-4: Local Authorities -- Manageable Implementation

**Stakeholder**: S-10 Local Authority Education Leads

**Driver Category**: OPERATIONAL

**Driver Statement**: Implement the new system without excessive burden on already-stretched local authority teams, ensuring it works with varying levels of technical capability (from London boroughs with dedicated digital teams to small rural authorities with one education officer).

**Context & Background**: Local authorities deliver FSM through their education departments. Digital maturity varies enormously: some have API-integrated systems, others rely on paper forms and spreadsheets. Any national system must accommodate this range without excluding less digitally mature authorities. Budget pressures mean local authorities cannot invest significantly in system integration.

**Driver Intensity**: HIGH

**Enablers**:
- Web-based portal requiring no local installation
- Bulk upload capability for authorities without API integration
- Training and onboarding support funded by DfE
- Local authority reference group for co-design

**Blockers**:
- 152 different existing systems and processes
- Staff turnover and training burden
- Resistance to changing established workflows

**Related Stakeholders**: S-11 (Schools), S-2 (Director)

---

### SD-5: Parents and Carers -- Simple, Stigma-Free Access

**Stakeholder**: S-12 Parents and Carers

**Driver Category**: CUSTOMER

**Driver Statement**: Access free school meals for their children without complex application processes, repeated evidence provision, or stigma. Ideally, be auto-enrolled without needing to apply at all.

**Context & Background**: Current application processes require parents to submit benefits evidence to their local authority or school. Many eligible families do not apply due to complexity, stigma, language barriers, or simply not knowing they qualify. The 11% eligibility gap disproportionately affects the most disadvantaged families, including those with low English literacy and those experiencing domestic abuse who may not control household finances.

**Driver Intensity**: CRITICAL

**Enablers**:
- Auto-enrolment via benefits data matching
- GOV.UK-standard accessible application for manual claims
- Multi-language support
- School-based support for families needing help

**Blockers**:
- Stigma associated with "free" school meals
- Digital exclusion for some families
- Data protection concerns about cross-government data sharing

**Related Stakeholders**: S-1 (Minister), S-17 (Charities), S-11 (Schools)

---

### SD-6: ICO -- Children's Data Protection

**Stakeholder**: S-16 ICO

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure the system complies with the Age Appropriate Design Code (Children's Code), UK GDPR Article 8 (conditions for children's consent), and best practice for processing children's personal data at scale. The ICO expects the highest standards for any system processing data about minors.

**Context & Background**: The ICO's Children's Code sets out 15 standards for online services likely to be accessed by children. While the School Meals system is not directly accessed by children, it processes their personal data including eligibility status (which reveals family financial circumstances). The ICO has indicated heightened scrutiny for government systems handling children's data.

**Driver Intensity**: HIGH

**Enablers**:
- Data Protection Impact Assessment (DPIA) completed before launch
- Data minimisation (collect only what is necessary)
- Purpose limitation (data used only for FSM eligibility)
- Transparent privacy notices in accessible formats

**Blockers**:
- Tension between auto-enrolment and data minimisation
- Complexity of consent models for children's data
- Cross-departmental data sharing governance

**Related Stakeholders**: S-5 (DPO), S-8 (HMRC), S-9 (DWP)

---

## Driver-to-Goal Mapping

### Goal G-1: Close the FSM Eligibility Gap

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: S-3 SRO

**Goal Statement**: Reduce the FSM eligibility gap from an estimated 11% to < 3% within 18 months of platform launch by implementing auto-enrolment for families receiving qualifying benefits.

**Why This Matters**: Approximately 215,000 eligible children are currently missing out on free school meals worth approximately £440/year per child (£94.6M total). Auto-enrolment removes application barriers for the most disadvantaged families.

**Success Metrics**:
- **Primary Metric**: FSM eligibility gap percentage
- **Secondary Metrics**:
  - Number of auto-enrolled pupils per term
  - Manual application volume (should decrease)
  - Pupil Premium funding accuracy

**Baseline**: 11% eligibility gap (estimated 215,000 unclaimed)

**Target**: < 3% eligibility gap (< 60,000 unclaimed)

**Measurement Method**: Comparison of ECS-verified eligible population against FSM registration data

---

### Goal G-2: Unified National Platform

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: S-4 CDO

**Goal Statement**: Deliver a single national platform used by all 152 local authorities for FSM eligibility management, replacing fragmented local systems, by Q2 2028.

**Why This Matters**: Eliminates data quality inconsistencies, enables accurate national reporting, and reduces aggregate local authority costs.

**Success Metrics**:
- **Primary Metric**: Number of local authorities onboarded
- **Secondary Metrics**:
  - Data consistency score across authorities
  - National reporting timeliness

**Baseline**: 152 different systems, varying ECS usage

**Target**: 152/152 local authorities on single platform

---

### Goal G-3: Compliant Cross-Departmental Data Sharing

**Derived From Drivers**: SD-3, SD-6

**Goal Owner**: S-5 DPO

**Goal Statement**: Establish lawful, ICO-compliant data sharing between DfE, HMRC, and DWP for FSM eligibility checking, with DPIA approval and annual ICO review, by system launch.

**Why This Matters**: The system's value depends on benefits data. Without compliant data sharing, auto-enrolment is impossible.

**Success Metrics**:
- **Primary Metric**: DPIA approved by DfE DPO and reviewed by ICO
- **Secondary Metrics**:
  - Zero ICO enforcement actions
  - Annual privacy audit pass rate

**Baseline**: Existing ECS data sharing agreement (limited scope)

**Target**: Expanded data sharing agreement covering auto-enrolment, DPIA approved, ICO positive assessment

---

### Goal G-4: Dashboard Data Feed for National Food Strategy

**Derived From Drivers**: SD-2

**Goal Owner**: S-4 CDO

**Goal Statement**: Publish FSM uptake metrics via standardised API for the National Food Strategy Dashboard (Project 005) with weekly data refresh by Q3 2028.

**Success Metrics**:
- **Primary Metric**: API availability > 99.5%
- **Secondary Metrics**: Data freshness < 7 days, metric coverage (uptake by region, age, ethnicity)

**Baseline**: No automated data feed

**Target**: Weekly automated data feed with full demographic breakdown

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Child Hunger

**Supported Goals**: G-1

**Outcome Statement**: An additional 155,000+ children receiving free school meals, worth approximately £68M annually in direct nutritional benefit.

**Business Value**:
- **Financial Impact**: £68M/year in food provision reaching previously unclaimed families
- **Strategic Impact**: Visible progress on child poverty reduction
- **Customer Impact**: Improved nutrition and educational outcomes for disadvantaged children

**Timeline**:
- Phase 1 (Months 1-6): 50,000 additional children auto-enrolled
- Phase 2 (Months 7-12): 100,000 cumulative
- Phase 3 (Months 13-18): 155,000 cumulative

---

### Outcome O-2: Administrative Efficiency

**Supported Goals**: G-2

**Outcome Statement**: 40% reduction in local authority staff time spent on FSM eligibility processing, saving an estimated £8M annually across 152 authorities.

**Business Value**:
- **Financial Impact**: £8M/year in local authority efficiency savings
- **Operational Impact**: Standardised processes, reduced error rates, faster eligibility determination

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Child hunger elimination | G-1 | Close eligibility gap | O-1 | 155K more children fed |
| Director | SD-2 | Programme efficiency | G-2 | Unified platform | O-2 | 40% admin savings |
| HMRC | SD-3 | Secure data sharing | G-3 | Compliant data sharing | O-1 | Enables auto-enrolment |
| Local Authorities | SD-4 | Manageable implementation | G-2 | Unified platform | O-2 | Standardised process |
| Parents | SD-5 | Simple, stigma-free access | G-1 | Close eligibility gap | O-1 | No application needed |
| ICO | SD-6 | Children's data protection | G-3 | Compliant data sharing | O-1 | Lawful processing |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Auto-enrolment ambition (SD-1, SD-5) vs data minimisation requirements (SD-3, SD-6). Auto-enrolment requires proactive cross-departmental data matching; data protection requires purpose limitation and minimisation.
  - **Resolution Strategy**: Implement a "check and notify" model rather than full data sharing -- HMRC confirms eligibility (yes/no) without sharing underlying benefits data. Parents notified and given opt-out window before enrolment.

- **Conflict 2**: National standardisation (SD-2) vs local authority autonomy (SD-4). Central platform risks alienating local authorities who value their existing processes.
  - **Resolution Strategy**: Phased rollout with local authority co-design. Platform provides standardised core with configurable local workflows. Pilot with 10 willing authorities before mandatory adoption.

**Synergies**:

- **Synergy 1**: Minister's eligibility gap closure (SD-1) aligns perfectly with parents' desire for stigma-free access (SD-5) -- auto-enrolment satisfies both.
- **Synergy 2**: HMRC's data minimisation requirement (SD-3) aligns with ICO's children's data protection stance (SD-6) -- both favour yes/no eligibility responses over raw data sharing.

---

## Communication & Engagement Plan

### Local Authorities

**Primary Message**: The new national platform will reduce your administrative burden by 40% and ensure no eligible child in your area misses out.

**Key Talking Points**:
- Web-based portal requiring no local system changes
- DfE-funded training and onboarding
- Co-designed with local authority reference group
- Phased rollout with voluntary early adoption

**Communication Frequency**: Monthly during implementation

**Preferred Channel**: Local Authority webinars, DfE Bulletin, regional workshops

---

## Change Impact Assessment

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Local Authorities | Own systems, manual processes | National platform, automated | HIGH | MEDIUM | Co-design, phased rollout, funded training |
| Schools | Paper forms, local systems | Digital portal, auto-enrolment alerts | MEDIUM | LOW | Training, helpdesk support |
| Parents | Application forms, evidence submission | Auto-enrolment, opt-out model | LOW | LOW | Clear communication, multi-language support |
| HMRC | Limited ECS API | Expanded eligibility API | LOW | MEDIUM | Legal gateway confirmed, technical API enhancement |

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Eligibility policy changes | Policy Team | Minister | LA reference group | All |
| Data sharing agreements | Legal Team | DPO/SIRO | HMRC, DWP, ICO | SRO |
| Platform architecture | CDO | SRO | CDDO, Security | All |
| Local authority onboarding | Delivery Manager | SRO | LA reference group | Minister |
| Budget allocation | Finance Director | SRO | DfE Perm Sec | All |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: HMRC/DWP Data Sharing Legal Challenge

**Related Stakeholders**: S-8 (HMRC), S-9 (DWP), S-16 (ICO)

**Risk Description**: Legal challenge to the expanded data sharing gateway for auto-enrolment, either from privacy campaigners or through ICO enforcement.

**Probability**: LOW

**Impact**: HIGH

**Mitigation Strategy**: Early ICO engagement, robust DPIA, purpose-limited data sharing (yes/no only), transparent privacy notices.

---

### Risk R-2: Local Authority Non-Adoption

**Related Stakeholders**: S-10 (Local Authorities)

**Risk Description**: Local authorities resist migrating to the national platform, particularly those with established local systems.

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Co-design with LA reference group; phased rollout with early adopters demonstrating value; funded migration support; ministerial direction as last resort.

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| CDO | PENDING | | PENDING |
| DPO | PENDING | | PENDING |
| LA Reference Group | PENDING | | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Education Act 1996 | Legislation | Parliament | Legal basis for FSM eligibility and data sharing | legislation.gov.uk |
| ICO Children's Code | Guidance | ICO | 15 standards for children's data processing | ico.org.uk |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 2 Programme | Governing architecture principles | ARC-000-PRIN-v1.0.md |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: School Meals Management System
**Model**: Claude Opus 4.6
