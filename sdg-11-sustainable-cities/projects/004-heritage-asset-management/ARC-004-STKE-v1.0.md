# Stakeholder Drivers & Goals Analysis: Heritage Asset Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Heritage Asset Management (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Heritage Asset Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Heritage Asset Management Programme Board, DCMS, Historic England, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Heritage Asset Management platform, a digital system for managing listed buildings, scheduled monuments, conservation areas, registered parks and gardens, and World Heritage Sites across England. The platform will modernise the National Heritage List for England (NHLE), improve heritage crime detection, and streamline Listed Building Consent workflows.

### Key Findings

The Heritage Asset Management platform faces a tension between conservation purists who view digital tools with suspicion (heritage assessment requires nuanced professional judgement, not algorithms) and the operational reality of an under-resourced heritage sector struggling to protect 400,000+ listed assets. The strongest alignment exists around improving data quality in the NHLE — every stakeholder benefits from accurate, complete, and accessible heritage records. The most significant conflict is between development pressure (speed, housing targets) and heritage protection (thoroughness, conservation ethics), reflected in the stakeholders from DLUHC planning and DCMS heritage.

### Critical Success Factors

- Digitise and validate the complete NHLE dataset (400,000+ entries) with accurate spatial boundaries
- Reduce Listed Building Consent determination time by 30% through automated workflow and consultee management
- Integrate with the Urban Planning Analytics platform (Project 002) for seamless heritage constraint checking
- Deploy Heritage at Risk monitoring using IoT sensor data from Project 001 for structural monitoring
- Maintain trust of conservation professionals by positioning the platform as decision-support, not decision-making

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus that heritage data needs digital modernisation and NHLE data quality must improve. Tensions between speed of planning decisions (DLUHC/developer interest) and thoroughness of heritage assessment (Historic England/conservation societies). Heritage professionals are protective of their expertise and wary of systems that appear to automate judgement.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DCMS Secretary of State | Minister | HIGH | MEDIUM | Keep Satisfied — Ministerial briefings on heritage protection |
| DCMS Heritage Director | Policy ownership | HIGH | HIGH | Manage Closely — Policy alignment |
| SRO, Heritage Asset Management | Programme Sponsor (DCMS) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DCMS Digital Team | DCMS digital capability | MEDIUM | HIGH | Keep Informed — Technical delivery |
| DCMS Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Historic England | ALB of DCMS | NHLE custodian, statutory consultee | HIGH | HIGH |
| Local Authority Conservation Officers | 200+ LPAs with conservation teams | Platform users | HIGH | HIGH |
| National Trust | Charity | Major heritage asset owner | MEDIUM | HIGH |
| English Heritage Trust | Charity | Heritage site operator | MEDIUM | HIGH |
| Heritage Fund (NLHF) | DCMS ALB | Heritage funding body | MEDIUM | MEDIUM |
| Church of England (DAC) | Diocesan Advisory Committees | Ecclesiastical exemption | MEDIUM | HIGH |
| Society for the Protection of Ancient Buildings (SPAB) | Amenity society | Statutory consultee | LOW | HIGH |
| Victorian Society | Amenity society | Statutory consultee | LOW | HIGH |
| Georgian Group | Amenity society | Statutory consultee | LOW | HIGH |
| Twentieth Century Society | Amenity society | Statutory consultee | LOW | HIGH |
| Ancient Monuments Society | Amenity society | Statutory consultee | LOW | HIGH |
| Council for British Archaeology | Professional body | Archaeological interest | LOW | HIGH |
| Civic Voice | Community heritage group | Community engagement | LOW | HIGH |
| DLUHC Planning Directorate | Partner department | Planning system integration | HIGH | HIGH |
| Heritage Crime Prevention | Police/CPS/Historic England | Heritage crime enforcement | MEDIUM | HIGH |
| CDDO | Cabinet Office | Spend control and assurance | HIGH | MEDIUM |
| Property Developers | Industry | Planning applicants | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | End-to-end heritage data service | HIGH / HIGH | Manage Closely — Service reviews |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control gates |

---

## Stakeholder Drivers Analysis

### SD-1: Historic England — Modernising the National Heritage List

**Stakeholder**: Historic England

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Modernise the National Heritage List for England (NHLE) from a legacy database with incomplete spatial data and inconsistent records into a comprehensive, spatially-accurate, API-accessible digital platform that supports heritage protection, planning integration, and public engagement — while maintaining the integrity and authority of listing decisions that are legal instruments.

**Context & Background**:
The NHLE contains records for approximately 400,000 listed buildings, 20,000 scheduled monuments, 1,700 registered parks and gardens, 46 registered battlefields, and 33 World Heritage Sites. Many records date from the 1947-1970 resurvey and have imprecise spatial boundaries (a pin on a map rather than a polygon), inconsistent descriptions, and no photographs. Historic England has been incrementally improving data quality but needs a step-change to support digital planning integration. However, NHLE entries are legal instruments — a listing description defines what is protected, and errors have legal consequences.

**Driver Intensity**: CRITICAL

**Enablers**:
- Funded programme to digitise and validate all 400,000+ NHLE entries with accurate polygons
- API-first design enabling direct integration with planning systems

**Blockers**:
- Data quality improvement is labour-intensive (heritage professional review required per record)
- Legal sensitivity — errors in digitised records could affect planning decisions and enforcement

---

### SD-2: Local Authority Conservation Officers — Better Tools for Overwhelmed Teams

**Stakeholder**: Local Authority Conservation Officers

**Driver Category**: OPERATIONAL / RESOURCE

**Driver Statement**: Provide conservation officers with digital tools that reduce administrative burden (managing Listed Building Consent applications, statutory consultee notifications, Heritage at Risk monitoring) so they can focus professional time on the heritage assessment and advice that requires specialist expertise.

**Context & Background**:
Conservation officer numbers have declined 35% since 2006 (Historic England Heritage Indicators). Many local authorities now share conservation officers across multiple councils or have no dedicated officer at all. The remaining officers spend significant time on administrative tasks — chasing statutory consultees (amenity societies have 21 days to respond), managing consent workflows, and manually checking NHLE records. Better digital tools could return 30-40% of their time to professional heritage work.

**Driver Intensity**: HIGH

**Enablers**:
- Automated consultee notification and response tracking
- Integrated NHLE lookup within the LBC application workflow
- Heritage at Risk monitoring alerts from IoT sensors (Project 001)

**Blockers**:
- Many conservation officers are not digitally confident
- Existing heritage management systems (mostly spreadsheets and Access databases) resist migration

---

### SD-3: Amenity Societies — Preserving Statutory Consultation Rights

**Stakeholder**: SPAB, Victorian Society, Georgian Group, Twentieth Century Society, Ancient Monuments Society, Council for British Archaeology

**Driver Category**: COMPLIANCE / DEMOCRATIC

**Driver Statement**: Ensure that digital heritage management preserves and improves the statutory consultation process for amenity societies, providing adequate information, adequate time, and genuine consideration of expert advice — not using digitalisation as a pretext to streamline away inconvenient objections.

**Context & Background**:
The six national amenity societies are statutory consultees on Listed Building Consent applications involving demolition or significant alteration. They are volunteer-led organisations with limited resources, processing thousands of consultations annually. The current system (PDF notifications via email or post) is inefficient for both sides. Amenity societies want a digital system that gives them better information (photos, plans, heritage significance statements) with efficient response mechanisms, but are wary of any system that shortens consultation periods or treats their responses as checkbox exercises.

**Driver Intensity**: HIGH

**Enablers**:
- Digital consultation portal with rich application information (photos, plans, heritage statements)
- Structured response templates that capture amenity society expertise effectively
- Clear audit trail showing how consultation responses influenced decisions

**Blockers**:
- Platform designed around speed metrics that incentivise quick consultee responses over thorough ones
- Digital-only consultation excluding volunteer consultees who prefer paper-based processes

---

### SD-4: Heritage Crime Prevention — Detecting and Prosecuting Heritage Crime

**Stakeholder**: Heritage Crime Prevention Partnership (Historic England, CPS, Police, CIfA)

**Driver Category**: ENFORCEMENT / RISK

**Driver Statement**: Use digital monitoring and IoT sensor data to detect unauthorised works to listed buildings and scheduled monuments earlier, providing the evidence chain needed for enforcement action and prosecution of heritage crime, which currently causes an estimated £2 billion in damage annually.

**Context & Background**:
Heritage crime includes unauthorised demolition or alteration of listed buildings, unlawful metal detecting on scheduled monuments, theft of architectural features (lead roofing, stone carvings), and arson. Detection is typically slow — unauthorised works may be completed before anyone notices. IoT sensors (vibration, temperature, acoustic) from Project 001 could provide early warning of unauthorised works at high-risk sites. The digital platform could also provide rapid access to listing records and photographic evidence needed for enforcement.

**Driver Intensity**: MEDIUM

**Enablers**:
- IoT sensor integration for structural monitoring at Heritage at Risk sites
- Digital evidence repository with timestamped photographs and listing records
- Automated alerts when planning applications are submitted for assets on Heritage at Risk Register

**Blockers**:
- Sensor deployment costs at 400,000+ sites (only feasible for highest-risk assets)
- Legal admissibility of IoT sensor evidence in heritage crime prosecutions not yet tested

---

## Driver-to-Goal Mapping

### Goal G-1: Digitise 100% of NHLE Records with Accurate Spatial Boundaries

**Derived From Drivers**: SD-1

**Goal Owner**: Historic England Digital Director

**Goal Statement**: Complete digital validation and spatial boundary mapping (polygons, not points) for 100% of NHLE entries within 3 years, with 50% completed in Year 1.

**Success Metrics**:
- **Primary Metric**: Percentage of NHLE entries with validated polygon boundaries
- **Secondary Metrics**: Data completeness score per record; error rate in digitised records

**Baseline**: Approximately 40% of NHLE entries have accurate polygon boundaries
**Target**: 100% polygon coverage, <0.1% error rate
**Measurement Method**: NHLE data quality dashboard, quarterly audit

---

### Goal G-2: Reduce Listed Building Consent Determination Time by 30%

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: SRO, Heritage Asset Management

**Goal Statement**: Reduce the average determination time for Listed Building Consent applications by 30% (from 12 weeks to 8.4 weeks) through automated workflow management and digital consultation, while maintaining or improving consultation quality.

**Success Metrics**:
- **Primary Metric**: Average LBC determination time in participating authorities
- **Secondary Metrics**: Consultee response rate; consultee satisfaction with digital process

**Baseline**: 12 weeks average LBC determination time
**Target**: 8.4 weeks average (30% reduction)
**Measurement Method**: Planning statistics, platform workflow analytics

---

### Goal G-3: Deploy IoT Structural Monitoring at 500 Heritage at Risk Sites

**Derived From Drivers**: SD-4, SD-1

**Goal Owner**: Historic England Heritage at Risk Team

**Goal Statement**: Deploy IoT structural monitoring sensors (vibration, moisture, temperature) at 500 priority Heritage at Risk sites within 18 months, integrated with the Heritage Asset Management platform for automated alerting.

**Success Metrics**:
- **Primary Metric**: Number of Heritage at Risk sites with active IoT monitoring
- **Secondary Metrics**: Unauthorised works detection rate; mean time to alert

**Baseline**: 0 sites with IoT monitoring (manual inspection only, annual cycle)
**Target**: 500 sites monitored, alerts within 1 hour of anomaly detection
**Measurement Method**: IoT platform dashboard, incident log

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Historic England | SD-1 | Modernise NHLE | G-1 | 100% digitisation | O-1 | Authoritative heritage data |
| Conservation Officers | SD-2 | Better tools, less admin | G-2 | 30% LBC time reduction | O-2 | Efficient heritage protection |
| Amenity Societies | SD-3 | Preserve consultation | G-2 | Better LBC workflow | O-2 | Efficient heritage protection |
| Heritage Crime | SD-4 | Detection and evidence | G-3 | IoT at 500 sites | O-3 | Proactive heritage monitoring |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DLUHC wants faster planning decisions (including LBC) to support housing delivery, but Amenity Societies (SD-3) want thorough consultation that takes time and Heritage professionals (SD-1) insist that heritage assessment cannot be rushed.
  - **Resolution Strategy**: Speed improvements come from administrative efficiency (automated notifications, digital responses, parallel processing), not from reducing assessment or consultation time. Statutory 21-day consultation period maintained.

**Synergies**:

- **Synergy 1**: NHLE digitisation (SD-1) directly enables planning integration (Project 002) and heritage crime detection (SD-4) — the same data improvement serves multiple stakeholders

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Planning (Listed Buildings and Conservation Areas) Act 1990 | Legislation | legislation.gov.uk | LBC requirements, amenity society consultation | N/A — external reference |
| Heritage at Risk Register | Dataset | Historic England | Priority heritage assets | N/A — external reference |
| NHLE Data Services | API | Historic England | Heritage constraint data | N/A — external reference |
| Heritage Crime Programme | Policy | Historic England / CPS | Heritage crime enforcement | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Heritage Asset Management (Project 004)
**Model**: Claude Opus 4.6
