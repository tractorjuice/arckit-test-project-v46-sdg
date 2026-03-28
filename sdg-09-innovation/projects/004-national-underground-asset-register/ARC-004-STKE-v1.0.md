# Stakeholder Drivers & Goals Analysis: National Underground Asset Register

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | National Underground Asset Register (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, National Underground Asset Register Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NUAR Programme Board, Geospatial Commission, Utility Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the National Underground Asset Register (NUAR), their underlying drivers, goals, and measurable outcomes. NUAR is a digital platform providing a single, secure view of underground pipes and cables to reduce accidental utility strikes during excavation works.

### Key Findings

NUAR addresses a costly and dangerous problem — an estimated 60,000 utility strikes occur annually in the UK, costing GBP 2.4 billion in direct costs and causing service disruptions affecting millions of citizens. The strongest alignment exists around the safety imperative — every stakeholder agrees that reducing utility strikes saves lives, reduces costs, and improves service reliability. The most significant conflict is around data sharing: utility companies are willing to share asset location data for safety purposes but deeply concerned about the security of precise infrastructure location data (which is CNI-sensitive) and the commercial implications of revealing network topology to competitors.

### Critical Success Factors

- Achieve data submission from all major utility asset owners (gas, electricity, water, telecoms, cable) — the platform is only as good as the data contributed
- Implement security controls sufficient to protect CNI-sensitive infrastructure location data while enabling rapid access for legitimate excavation planning
- Deliver a user experience that is faster and more accurate than the current plant enquiry process (which averages 5-10 working days per response)
- Comply with PAS 256 (Buried Asset Data Specification) to ensure data interoperability across utility sectors
- Build trust with utility companies through demonstrable data security, controlled access, and clear data ownership principles

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong safety-driven alignment on reducing utility strikes. Tensions exist around data security controls (utilities want maximum protection, users want easy access), data quality obligations (utilities question whose responsibility it is to maintain accuracy), and cost sharing (who pays for ongoing platform operation).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Geospatial Commission Director | Programme Sponsor | HIGH | HIGH | Manage Closely — Programme board |
| Cabinet Office Minister | Ministerial sponsor | HIGH | HIGH | Manage Closely — Ministerial briefings |
| SRO, NUAR | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| Geospatial Commission CTO | Technical leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| National Grid (Gas & Electricity) | Utility | Major asset owner — gas transmission, electricity transmission | HIGH | HIGH |
| Cadent Gas | Utility | Gas distribution network (largest) | HIGH | HIGH |
| UK Power Networks (UKPN) | Utility | Electricity distribution (SE England) | HIGH | HIGH |
| Other DNOs (WPD, SSEN, NPG, ENW) | Utility | Regional electricity distribution | MEDIUM | HIGH |
| Thames Water, Severn Trent, United Utilities | Water | Major water and sewerage companies | HIGH | HIGH |
| BT/Openreach | Telecoms | Underground telecoms infrastructure | HIGH | HIGH |
| Virgin Media O2 | Telecoms | Cable infrastructure | MEDIUM | HIGH |
| National Highways | Road authority | SRN excavation and asset crossings | HIGH | HIGH |
| Local Highway Authorities (153) | Road authority | Local road excavation management | MEDIUM | HIGH |
| Construction industry (contractors) | Commercial | Primary users — excavation planning | LOW | HIGH |
| Health and Safety Executive (HSE) | Regulator | Worker safety regulation | HIGH | MEDIUM |
| Ofgem | Regulator | Gas and electricity regulation | HIGH | MEDIUM |
| Ofwat | Regulator | Water industry regulation | HIGH | MEDIUM |
| Ordnance Survey | Geospatial data | Authoritative base mapping | MEDIUM | HIGH |
| LSBUD (Linesearch beforeUdig) | Existing service | Current plant enquiry operator | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| NCSC | National security | CNI data protection guidance | HIGH | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HSE              │  • Geospatial Comm. │
        │  • Ofgem            │    Director          │
        │  • Ofwat            │  • SRO              │
        │  • CDDO             │  • National Grid    │
        │                     │  • Cadent Gas       │
 P      │                     │  • UKPN / DNOs      │
 O      │                     │  • Major Water Cos  │
 W      │                     │  • BT/Openreach     │
 E      │                     │  • National Highways│
 R      │                     │  • NCSC             │
        ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │                     │  • Contractors      │
        │                     │  • Local Highway    │
        │                     │    Authorities       │
        │                     │  • VMO2             │
        │                     │  • Ordnance Survey  │
        │                     │  • LSBUD            │
        │                     │  • Product Manager  │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Geospatial Commission — Reduce Utility Strike Costs and Safety Incidents

**Stakeholder**: Geospatial Commission Director

**Driver Category**: STRATEGIC / SAFETY

**Driver Statement**: Reduce the estimated 60,000 annual utility strikes and their GBP 2.4 billion cost by providing a single, secure, accurate digital platform for underground asset information, accessible to anyone planning excavation works.

**Context & Background**:
The Geospatial Commission identified underground asset data as one of the highest-value opportunities in its National Geospatial Strategy. Currently, before any excavation, contractors must contact each utility company separately to request plant information — a process that takes 5-10 working days and frequently returns incomplete or outdated information. Strikes cause gas leaks (safety risk), power cuts (economic disruption), water main bursts (flooding), and fibre cuts (communications outage). Three workers are killed annually in utility strike incidents.

**Driver Intensity**: CRITICAL

**Enablers**:

- Geospatial Commission mandate and cross-government authority
- Strong safety case creates utility company obligation to participate
- PAS 256 standard provides technical data model for interoperability

**Blockers**:

- Utility companies concerned about CNI data security
- Fragmented asset ownership (hundreds of asset owners nationally)
- Variable data quality across utilities (some records pre-date digitalisation)

**Related Stakeholders**: National Grid, Cadent, UKPN, HSE, NCSC

---

### SD-2: National Grid / Major Utilities — Protect CNI While Improving Safety

**Stakeholder**: National Grid, Cadent Gas, UKPN

**Driver Category**: SECURITY / COMPLIANCE / SAFETY

**Driver Statement**: Share underground asset location data to prevent strikes on their infrastructure (which cause safety incidents, service disruptions, and costly repairs) while ensuring that precise infrastructure location data — classified as Critical National Infrastructure — is protected against hostile actors who could use it to plan physical attacks on energy or water networks.

**Context & Background**:
Major utilities experience thousands of third-party strikes per year — Cadent alone reports ~5,000 gas pipe strikes annually. Each strike is a safety risk (gas explosion potential), a regulatory risk (HSE investigation), and a financial cost (GBP 3,000-50,000 per incident depending on severity). However, the precise location of gas transmission pipelines, electricity substations, and water treatment works is CNI-sensitive data. The NCSC has published specific guidance on protecting utility infrastructure data. Utilities need confidence that the platform's security meets CNI standards before sharing.

**Driver Intensity**: CRITICAL

**Enablers**:

- Strong financial incentive (cost of strikes vs cost of data sharing)
- NCSC guidance provides clear security requirements
- Existing data sharing precedent through LSBUD (current plant enquiry service)

**Blockers**:

- CNI data classification requires enhanced security controls beyond standard government platforms
- Concern about aggregation risk (combining multiple utility datasets reveals more than any single dataset)
- Legacy data quality — some gas pipe records are hand-drawn plans from the 1970s

**Related Stakeholders**: NCSC, HSE, LSBUD, Construction contractors

---

### SD-3: Construction Industry — Faster, More Reliable Plant Information

**Stakeholder**: Construction contractors, civil engineering firms, ground workers

**Driver Category**: OPERATIONAL / SAFETY

**Driver Statement**: Get complete, accurate, and timely information about all underground assets in an excavation area through a single request, reducing the current 5-10 working day wait and multiple separate enquiries to a single query with results in minutes, reducing the risk of utility strikes.

**Context & Background**:
Before any excavation, contractors must identify underground assets. Currently this requires contacting each utility company separately via LSBUD or directly, waiting 5-10 working days for responses (sometimes longer), and reconciling multiple responses in different formats. Incomplete responses lead to "dig and discover" — the dangerous practice of excavating without full knowledge of underground assets. Faster, more reliable information would improve both safety and productivity (construction delays due to plant enquiry waits cost the industry an estimated GBP 500M per year).

**Driver Intensity**: HIGH

**Enablers**:

- Digital delivery enables near-instant results vs postal/email responses
- Smartphone and tablet access for on-site use
- Unified view eliminates the need to reconcile multiple separate responses

**Blockers**:

- Not all contractors are digitally capable (particularly smaller firms)
- Historical reliance on paper-based processes
- Concern about liability if platform data is inaccurate and a strike occurs

**Related Stakeholders**: National Highways, Local Highway Authorities, HSE

---

### SD-4: Health and Safety Executive — Reduce Worker Injuries and Deaths

**Stakeholder**: Health and Safety Executive (HSE)

**Driver Category**: COMPLIANCE / SAFETY

**Driver Statement**: Reduce the incidence of worker injuries and fatalities from utility strikes through better pre-excavation information, supporting enforcement of HSE guidance (HSG47: Avoiding danger from underground services).

**Context & Background**:
HSE publishes HSG47 which requires employers to take reasonable steps to identify underground services before excavation. Three workers are killed and hundreds injured annually in strike incidents. HSE investigations frequently find that plant information was incomplete, outdated, or not obtained at all. A reliable, accessible digital register would strengthen the HSG47 compliance framework and provide an evidence base for enforcement.

**Driver Intensity**: HIGH

**Enablers**:

- Existing HSG47 regulatory framework
- Clear link between better information and reduced incidents
- HSE enforcement powers create incentive for contractor compliance

**Blockers**:

- HSE cannot mandate use of a specific platform (only that reasonable steps are taken)
- Liability framework unclear if platform data is inaccurate

**Related Stakeholders**: Construction contractors, Major utilities

---

## Driver-to-Goal Mapping

### Goal G-1: Comprehensive Underground Asset Database

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: SRO, NUAR

**Goal Statement**: Establish a platform containing underground asset data from all major UK utility asset owners (gas, electricity, water, telecoms) covering 95% of the UK's buried infrastructure by Q4 2027.

**Success Metrics**:

- **Primary Metric**: Percentage of UK underground infrastructure represented in the platform
- **Secondary Metrics**:
  - Number of asset owners submitting data
  - Data coverage by geographic area
  - Data freshness: average age of asset records

**Baseline**: Fragmented data across individual utility companies, accessed via separate enquiries

**Target**: 95% coverage, all major asset owners participating

---

### Goal G-2: Secure Access Model Compliant with CNI Requirements

**Derived From Drivers**: SD-2

**Goal Owner**: Geospatial Commission CTO

**Goal Statement**: Implement a security model assessed and approved by NCSC that protects CNI-sensitive infrastructure location data while enabling rapid access for legitimate excavation planning, achieving NCSC sign-off by Q2 2027.

**Success Metrics**:

- **Primary Metric**: NCSC security assessment pass
- **Secondary Metrics**:
  - Zero data breaches
  - User identity verification time < 24 hours for new registrations
  - Audit trail completeness: 100% of data access logged

---

### Goal G-3: Rapid Digital Plant Enquiry

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: Product Manager

**Goal Statement**: Reduce plant enquiry response time from 5-10 working days (current average) to under 60 seconds for a standard digital query, available 24/7 including mobile access for on-site use.

**Success Metrics**:

- **Primary Metric**: Enquiry response time (5-10 days to < 60 seconds)
- **Secondary Metrics**:
  - User satisfaction score > 4.0/5.0
  - Mobile usage percentage (target: >40% of queries from mobile devices)
  - 24/7 availability: 99.9%

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Utility Strikes and Associated Costs

**Supported Goals**: G-1, G-3

**Outcome Statement**: Reduce annual utility strikes by 30% (from 60,000 to 42,000) within 3 years of national rollout, saving an estimated GBP 720 million in annual strike costs.

**Measurement Details**:

- **KPI**: Annual utility strike incidents
- **Current Value**: ~60,000 per year
- **Target Value**: ~42,000 per year (30% reduction)
- **Measurement Frequency**: Annual
- **Data Source**: Utility company incident reports, HSE RIDDOR data

**Business Value**:

- **Financial Impact**: GBP 720M annual cost savings across the utility and construction sectors
- **Strategic Impact**: UK infrastructure maintenance more efficient and safer
- **Operational Impact**: Fewer emergency repairs, fewer service disruptions
- **Customer Impact**: Fewer gas leaks, power cuts, water outages, broadband interruptions

---

### Outcome O-2: Improved Worker Safety

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Zero fatalities from utility strikes where the NUAR platform was consulted prior to excavation.

**Measurement Details**:

- **KPI**: Worker fatalities from utility strikes (where NUAR was used)
- **Current Value**: 3 fatalities per year (all causes)
- **Target Value**: Zero fatalities where NUAR consulted
- **Measurement Frequency**: Annual
- **Data Source**: HSE RIDDOR reports, NUAR usage logs

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Geospatial Commission | SD-1 | Reduce strike costs | G-1 | Comprehensive database | O-1 | Reduced strikes |
| Geospatial Commission | SD-1 | Reduce strike costs | G-3 | Rapid enquiry | O-1 | Reduced strikes |
| Major Utilities | SD-2 | Protect CNI, improve safety | G-1 | Comprehensive database | O-1 | Reduced strikes |
| Major Utilities | SD-2 | Protect CNI, improve safety | G-2 | Secure access model | O-2 | Worker safety |
| Construction Industry | SD-3 | Faster plant info | G-3 | Rapid enquiry | O-1 | Reduced strikes |
| HSE | SD-4 | Reduce injuries and deaths | G-3 | Rapid enquiry | O-2 | Worker safety |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Construction contractors (SD-3) want instant, open access to asset location data. Utilities (SD-2) want strict access controls to protect CNI-sensitive data.
  - **Resolution Strategy**: Verified user registration with identity checks; tiered data granularity (contractors see asset proximity and type, not detailed network topology); all access logged and auditable; NCSC-approved security controls.

- **Conflict 2**: Geospatial Commission (SD-1) wants comprehensive data from all asset owners. Utilities are concerned about the aggregation risk — individual datasets are manageable, but combining gas, electricity, water, and telecoms reveals the complete critical infrastructure picture.
  - **Resolution Strategy**: View-level access controls — users see only assets relevant to their excavation area, not the full national dataset. Aggregated views restricted to authorised government users. Security architecture prevents bulk data extraction.

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Utility Refusal to Share Data

**Related Stakeholders**: National Grid, Cadent, Water companies

**Risk Description**: One or more major utility companies refuse to share data, citing CNI security concerns, rendering the platform incomplete for the areas they serve.

**Probability**: MEDIUM | **Impact**: CRITICAL

**Mitigation Strategy**: NCSC security assessment to build confidence; regulatory backstop via potential legislative requirement; demonstrate that aggregated risk is managed through access controls

---

### Risk R-2: Data Accuracy Insufficient for Safety-Critical Use

**Related Stakeholders**: Construction contractors, HSE

**Risk Description**: Historical asset data is inaccurate (some records pre-date GPS), leading to strikes despite using the platform, creating liability risk and undermining confidence.

**Probability**: HIGH | **Impact**: HIGH

**Mitigation Strategy**: Clear disclaimers that platform data supplements (not replaces) on-site detection; data quality scoring per asset record; utility company data improvement programme; feedback mechanism for contractors to report discrepancies

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PAS 256 | Standard | BSI | Buried asset data specification | N/A — external reference |
| HSG47 | Guidance | HSE | Avoiding danger from underground services | N/A — external reference |
| UK Geospatial Strategy | Strategy | Geospatial Commission | Underground asset priority | N/A — external reference |
| NCSC CNI Guidance | Guidance | NCSC | Protecting critical infrastructure data | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Underground Asset Register (Project 004)
**Model**: Claude Opus 4.6
