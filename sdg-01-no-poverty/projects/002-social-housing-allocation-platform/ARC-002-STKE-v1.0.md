# Stakeholder Drivers & Goals Analysis: Social Housing Allocation Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Social Housing Allocation Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Social Housing Digital Programme, DLUHC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Digital, Local Authority Housing Directors, Regulator of Social Housing |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Social Housing Allocation Platform, their drivers, goals, and measurable outcomes. The platform aims to create a fair, transparent, and efficient system for allocating social housing across England, replacing fragmented council-level systems with a national platform that supports choice-based lettings (CBL) while respecting local allocation policies.

### Key Findings

The strongest stakeholder alignment exists around the need for transparency and fairness in allocation — councils, applicants, housing associations, and the Regulator all share this goal. The most significant tension is between local autonomy (councils want to retain control of their allocation policies under the Allocation of Housing (England) Regulations 2002) and national consistency (DLUHC wants standardised data and comparable outcomes). Homelessness charities push for stronger priority for rough sleepers and those owed a duty under the Homelessness Reduction Act 2017, while some councils resist additional priority categories that strain already limited stock.

### Critical Success Factors

- Local authorities retain control of their allocation policies within a nationally consistent framework
- Applicants can see available properties and express preferences (choice-based lettings) through an accessible digital service
- Transparent queue position and allocation decisions reduce complaints and legal challenges
- Integration with homelessness systems ensures statutory duties under the Homelessness Reduction Act 2017 are met
- Platform operates across 300+ local authorities with diverse existing systems and policies

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for modernisation and transparency, but significant tension between national standardisation and local autonomy. Housing associations operating across multiple councils are strong advocates for consistency; councils are cautious about losing policy flexibility.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DLUHC Minister for Housing | Ministerial oversight | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DLUHC Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Social Housing Digital Programme | Programme sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DLUHC CDIO | Digital leadership | HIGH | MEDIUM | Keep Satisfied — Architecture governance |
| Homelessness and Rough Sleeping Directorate | Policy owner | HIGH | HIGH | Manage Closely — Policy alignment |
| DLUHC Data and Analysis Team | Data and evidence | MEDIUM | HIGH | Keep Informed — Data standards, reporting |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Local Authority Housing Directors | 300+ councils | Service operators | HIGH | HIGH |
| Regulator of Social Housing (RSH) | Regulator | Oversight | HIGH | MEDIUM |
| Housing Applicants | Citizens | Service users | LOW | HIGH |
| Housing Associations (RPs) | Registered Providers | Property providers | MEDIUM | HIGH |
| Shelter and Crisis | Charities | Advocacy | LOW | HIGH |
| LGA (Local Government Association) | Sector body | Representation | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |
| Homes England | NDPB | Funding and development | MEDIUM | MEDIUM |
| ICO | Regulator | Data protection | HIGH | MEDIUM |
| DWP | Partner department | UC housing element integration | MEDIUM | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * DLUHC Minister   |
        |  * ICO              |  * Permanent Sec.   |
        |  * RSH              |  * SRO              |
        |                     |  * LA Housing Dirs  |
 P      |                     |  * Homelessness Dir |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * Homes England    |  * Housing Appls    |
        |                     |  * Housing Assocs   |
        |                     |  * Shelter/Crisis   |
        |                     |  * LGA              |
        |                     |  * DWP              |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DLUHC Minister — Visible Progress on Housing Waiting Lists

**Stakeholder**: Minister for Housing

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate measurable progress in reducing social housing waiting lists and improving the fairness of allocation, supporting manifesto commitments on housing.

**Context & Background**: Over 1.2 million households are on social housing waiting lists in England. The system is fragmented across 300+ councils, with inconsistent policies and limited data visibility. The Minister needs demonstrable improvement and national data to respond to parliamentary questions and media scrutiny.

**Driver Intensity**: CRITICAL

**Enablers**: National dataset on waiting lists and allocation outcomes; transparent allocation criteria; success stories from early adopter councils

**Blockers**: Council resistance to national platform; political sensitivity of allocation decisions; insufficient new housing supply (platform cannot solve the supply problem)

**Related Stakeholders**: Permanent Secretary, Shelter/Crisis, Housing Applicants

---

### SD-2: Local Authority Housing Directors — Retain Local Allocation Policy Control

**Stakeholder**: Local Authority Housing Directors (300+ councils)

**Driver Category**: OPERATIONAL / POLITICAL

**Driver Statement**: Retain full control over local allocation policies (reasonable preference categories, local connection criteria, banding schemes) while gaining operational efficiencies from a shared platform.

**Context & Background**: The Allocation of Housing (England) Regulations 2002 give councils statutory responsibility for their allocation schemes. Each council's scheme reflects local circumstances — some use banding, others use points, some have extensive local connection criteria. Councils will resist any platform that imposes a one-size-fits-all policy. However, many are operating on outdated systems (some still paper-based) and welcome modernisation if it respects their autonomy.

**Driver Intensity**: CRITICAL

**Enablers**: Configurable allocation policy engine; local authority governance over their own scheme configuration; migration support from legacy systems; central funding for adoption

**Blockers**: Mandated national allocation policy overriding local schemes; unfunded mandates; loss of data sovereignty; inadequate training and change management

**Related Stakeholders**: LGA, DLUHC Minister, Housing Applicants

---

### SD-3: Housing Applicants — Fair, Transparent, Accessible Applications

**Stakeholder**: Housing applicants (1.2 million+ households on waiting lists)

**Driver Category**: CUSTOMER / USER

**Driver Statement**: Apply for social housing through a simple, accessible process that explains eligibility criteria, provides clear queue position, gives meaningful property choices, and treats applicants with dignity.

**Context & Background**: Many applicants are in vulnerable circumstances — homeless or at risk of homelessness, fleeing domestic abuse, living in overcrowded or unsuitable accommodation, or experiencing health conditions made worse by their housing. Current systems range from poor web portals to paper forms. Applicants often do not understand why they are placed in a particular band or how long they might wait. Choice-based lettings gives applicants some agency but is difficult to access for those with limited digital skills.

**Driver Intensity**: CRITICAL

**Enablers**: Plain language, accessible digital service with assisted digital routes; clear band/queue position display; property matching and alerts; mobile-first design; multi-language support

**Blockers**: Complex allocation policies that resist simplification; lack of available properties (system cannot create supply); digital exclusion among vulnerable applicants

**Related Stakeholders**: Shelter/Crisis, Citizens Advice, Local Authorities, DWP (UC housing element)

---

### SD-4: Regulator of Social Housing — Transparency and Consumer Standards

**Stakeholder**: Regulator of Social Housing (RSH)

**Driver Category**: COMPLIANCE / REGULATORY

**Driver Statement**: Ensure social housing allocation and management meets the revised consumer standards, with particular focus on the Transparency, Influence and Accountability Standard and the Tenancy Standard.

**Context & Background**: Following the Social Housing (Regulation) Act 2023, RSH has strengthened consumer regulation of social housing. The revised consumer standards require landlords to provide fair and transparent allocation processes. A national platform with consistent data standards enables RSH to fulfil its regulatory function more effectively.

**Driver Intensity**: HIGH

**Enablers**: Standardised allocation data enabling regulatory analysis; transparent allocation decision audit trails; tenant satisfaction data collection; complaint tracking

**Blockers**: Platform not covering housing association allocations (RP nominations); data quality issues in council systems; councils opting out of the platform

**Related Stakeholders**: Housing Associations, DLUHC, Housing Applicants

---

### SD-5: Housing Associations — Consistent Nominations Process Across Councils

**Stakeholder**: Housing Associations (Registered Providers)

**Driver Category**: OPERATIONAL

**Driver Statement**: Receive and process nomination requests from multiple councils through a single, consistent interface rather than dealing with 300+ different systems, formats, and processes.

**Context & Background**: Large housing associations operate across many local authority areas. Each council has its own system, data format, and nomination process. A housing association managing 50,000 homes across 40 councils currently interfaces with 40 different systems. A national platform with a standardised nominations API would dramatically reduce administrative overhead.

**Driver Intensity**: HIGH

**Enablers**: Standardised nominations API; consistent data formats for applicant information; single integration point for multi-council RPs; real-time vacancy and letting updates

**Blockers**: Platform not supporting RP direct lets (non-nominated allocations); inflexible API that doesn't support local variations; poor data quality in council nominations

**Related Stakeholders**: Local Authorities, RSH, DLUHC

---

### SD-6: Homelessness and Rough Sleeping Directorate — Statutory Duty Compliance

**Stakeholder**: DLUHC Homelessness and Rough Sleeping Directorate

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure the platform supports councils in meeting their statutory duties under the Homelessness Reduction Act 2017, including reasonable preference for homeless applicants and tracking of outcomes for those owed a prevention or relief duty.

**Context & Background**: The Homelessness Reduction Act 2017 placed new duties on councils to prevent and relieve homelessness. Councils must give reasonable preference to people who are homeless or threatened with homelessness. The platform must integrate with H-CLIC (Homelessness Case Level Information Collection) reporting and ensure homeless applicants are appropriately prioritised.

**Driver Intensity**: HIGH

**Enablers**: Integration with H-CLIC; automatic reasonable preference flagging for homeless applicants; outcome tracking (housed, lost contact, refused); data sharing with homelessness teams

**Blockers**: Platform not covering prevention duty tracking (separate from allocation); data silos between homelessness and allocations teams within councils; inconsistent definitions of homelessness priority across council schemes

**Related Stakeholders**: Shelter/Crisis, Local Authorities, Housing Applicants

---

## Driver-to-Goal Mapping

### Goal G-1: National Visibility of Waiting Lists

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: DLUHC Data and Analysis Team

**Goal Statement**: Provide a national, real-time dashboard of social housing waiting list data (total applicants, band distribution, average wait times by area, allocation rates) by March 2028.

**Baseline**: No national real-time data; annual LAHS return (Local Authority Housing Statistics) is 12+ months stale.

**Target**: Real-time dashboard updated daily from live platform data.

**Measurement Method**: Platform analytics, compared against annual LAHS return for validation.

---

### Goal G-2: 80% of Councils Onboarded Within 3 Years

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: SRO

**Goal Statement**: Onboard at least 240 of 309 English local housing authorities onto the platform by March 2029, representing 80% coverage.

**Baseline**: 0 councils onboarded.

**Target**: 240 councils (80%) by March 2029.

---

### Goal G-3: Applicant Satisfaction of 75%

**Derived From Drivers**: SD-3

**Goal Owner**: Service Owner

**Goal Statement**: Achieve 75% applicant satisfaction with the housing application and bidding process by March 2028, measured through GDS transaction surveys.

**Baseline**: No consistent national baseline (varies by council, typically 45-60%).

**Target**: 75% satisfaction.

---

### Goal G-4: Allocation Decision Transparency

**Derived From Drivers**: SD-3, SD-4, SD-6

**Goal Owner**: Service Owner

**Goal Statement**: 100% of allocation decisions include a clear, auditable explanation of why the applicant was selected (or not), accessible to the applicant in plain language.

**Baseline**: Varies by council; many provide minimal explanation.

**Target**: 100% auditable, explainable decisions.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| DLUHC Minister | SD-1 | Visible waiting list progress | G-1 | National visibility dashboard |
| LA Housing Directors | SD-2 | Retain local policy control | G-2 | 80% council onboarding |
| Housing Applicants | SD-3 | Fair, transparent access | G-3, G-4 | 75% satisfaction, transparent decisions |
| RSH | SD-4 | Consumer standards compliance | G-1, G-4 | National data, transparent decisions |
| Housing Associations | SD-5 | Consistent nominations | G-2 | 80% council onboarding |
| Homelessness Directorate | SD-6 | Statutory duty compliance | G-4 | Transparent decisions |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DLUHC Minister (SD-1) wants national standardisation for comparable data; LA Housing Directors (SD-2) want local policy autonomy. Resolution: Configurable policy engine that enforces statutory minimums while permitting local variation. National data standards for reporting; local discretion on allocation criteria within legal framework.

- **Conflict 2**: Homelessness Directorate (SD-6) wants stronger priority for homeless applicants; some LAs resist additional priority categories that deplete stock available for other high-need groups (overcrowded families, disabled applicants). Resolution: Platform enforces statutory reasonable preference requirements; additional local priority categories remain at council discretion.

**Synergies**:

- Housing Associations (SD-5) and LAs (SD-2) both benefit from a modern shared platform — reduced admin burden and improved data exchange
- RSH (SD-4) and Applicants (SD-3) both want transparency — this is a shared win

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | DLUHC CDIO | SRO | LGA, Housing Associations | All |
| Allocation policy configuration | Individual LA | LA Housing Director | RSH, DLUHC Policy | Applicants |
| Data standards | DLUHC Data Team | SRO | LGA, RSH, Housing Assocs | All |
| Go/No-go for onboarding | LA Housing Director | SRO | CDDO | All |
| Budget approval | DLUHC Finance | Permanent Secretary | Treasury | All |

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| SRO | | | PENDING |
| DLUHC CDIO | | | PENDING |
| LGA Representative | | | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Allocation of Housing (England) Regulations 2002 | Legislation | legislation.gov.uk | Statutory allocation framework | N/A |
| Homelessness Reduction Act 2017 | Legislation | legislation.gov.uk | Prevention and relief duties | N/A |
| Social Housing (Regulation) Act 2023 | Legislation | legislation.gov.uk | Consumer standards regime | N/A |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 1 Programme | Governing principles | projects/000-global/ |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Social Housing Allocation Platform
**Model**: Claude Opus 4.6
