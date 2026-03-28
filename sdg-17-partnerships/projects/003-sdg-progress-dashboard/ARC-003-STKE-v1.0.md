# Stakeholder Drivers & Goals Analysis: SDG Progress Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | SDG Progress Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SDG Progress Dashboard Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | ONS SDG Team, UKSA, Cabinet Office SDG Unit, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the SDG Progress Dashboard programme, their underlying drivers, and how these map to programme goals and measurable outcomes. The ONS-led dashboard will monitor and report UK progress against all 244 UN SDG indicators, supporting the UK's Voluntary National Review (VNR) commitments and enabling evidence-based policy making.

### Key Findings

The SDG Progress Dashboard operates at the intersection of statistical independence, political sensitivity, and international reporting. The strongest alignment is around the need for a single, authoritative, publicly accessible platform showing UK SDG progress — this satisfies ONS's statistical mission, the UN reporting framework, civil society's transparency demands, and government's need for evidence-based policy. The most significant tension is between political stakeholders who want to present UK performance favourably and UKSA's requirement for statistical independence — the dashboard must present data without political spin, including indicators where UK progress is poor.

### Critical Success Factors

- Cover all 244 UN SDG indicators where UK data sources exist (currently approximately 180/244 have data)
- Maintain UKSA Code of Practice compliance for all published statistics
- Deliver a public-facing dashboard accessible to international audiences (WCAG 2.1 AA, multilingual metadata)
- Support the next UK Voluntary National Review with comprehensive, machine-readable SDG data
- Integrate data from 20+ source departments and agencies via the Cross-Government Data Sharing Platform (Project 002)

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong consensus on the need for a comprehensive SDG dashboard. UKSA's independence mandate provides a clear governance framework. Tensions exist around indicator selection (some departments resist publishing indicators where performance is poor), data timeliness (policy teams want current data while ONS requires statistical validation), and resource allocation (ONS has finite capacity and SDG monitoring competes with other statistical priorities).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| UK Statistics Authority (UKSA) Chair | Statistical governance | HIGH | HIGH | Manage Closely — Code of Practice compliance |
| National Statistician (ONS CEO) | ONS leadership | HIGH | HIGH | Manage Closely — Programme governance |
| SRO, SDG Progress Dashboard | Programme Sponsor (ONS) | HIGH | HIGH | Manage Closely — Weekly programme board |
| ONS SDG Team Lead | SDG indicator production | MEDIUM | HIGH | Keep Informed — Day-to-day delivery |
| ONS Digital Services Director | Technical platform | HIGH | MEDIUM | Keep Satisfied — Architecture, infrastructure |
| ONS Methodology Director | Statistical methodology | HIGH | MEDIUM | Keep Satisfied — Quality assurance |
| ONS International Team | UN reporting liaison | MEDIUM | HIGH | Keep Informed — SDMX, VNR preparation |
| ONS Data Science Campus | Advanced analytics | LOW | MEDIUM | Monitor — Data science innovation |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Cabinet Office SDG Unit | Cabinet Office | Policy coordination | HIGH | HIGH |
| CDDO | Cabinet Office | Digital standards | HIGH | MEDIUM |
| UN Statistics Division (UNSD) | United Nations | SDG indicator custodian | HIGH | HIGH |
| Inter-Agency Expert Group on SDGs (IAEG-SDGs) | United Nations | Indicator methodology | MEDIUM | HIGH |
| Source departments (20+) | Cross-government | Data providers | MEDIUM | MEDIUM |
| Devolved administrations | Scotland, Wales, NI | Sub-national SDG reporting | MEDIUM | HIGH |
| UK Stakeholders for Sustainable Development (UKSSD) | Civil society coalition | SDG advocacy | LOW | HIGH |
| Bond (UK NGO network) | Civil society | International development SDGs | LOW | HIGH |
| Academic researchers | Universities | SDG analysis | LOW | HIGH |
| International statistical offices | Foreign governments | Peer comparison | LOW | MEDIUM |
| OECD Statistics Directorate | OECD | SDG measurement methodology | MEDIUM | MEDIUM |
| World Bank Data Group | World Bank | Global SDG data | LOW | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * ONS Digital Dir  |  * UKSA Chair       |
        |  * ONS Methodology  |  * Nat Statistician |
        |  * CDDO             |  * SRO              |
        |                     |  * Cabinet Office   |
 P      |                     |    SDG Unit         |
 O      |                     |  * UNSD             |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * ONS Data Science |  * UKSSD            |
        |  * World Bank       |  * Bond             |
        |                     |  * Devolved admins  |
        |                     |  * Academic research|
        |                     |  * IAEG-SDGs        |
        |                     |  * Source depts     |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: UKSA / National Statistician — Statistical Independence and Quality

**Stakeholder**: UK Statistics Authority / National Statistician

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure that all SDG indicators published on the dashboard comply with the Code of Practice for Statistics (Trustworthiness, Quality, Value) and maintain ONS's reputation for statistical independence, accuracy, and impartiality.

**Context & Background**:
ONS's credibility depends on producing statistics that are free from political interference, methodologically sound, and transparently produced. SDG indicators are politically sensitive — they measure government performance on issues like poverty, inequality, and environmental sustainability. Any perception that indicator selection, methodology, or presentation is influenced by political considerations would undermine UKSA's authority and damage the UK's international statistical reputation.

**Driver Intensity**: CRITICAL

**Enablers**:

- Clear separation of statistical production from policy commentary
- Published methodology for each indicator
- Pre-release access controls compliant with UKSA rules
- Automated publication pipeline that cannot be interrupted by non-statistical staff

**Blockers**:

- Political pressure to delay or suppress unfavourable indicators
- Resource constraints forcing methodology shortcuts
- Departmental data providers withholding data

---

### SD-2: Cabinet Office SDG Unit — Policy Coordination and VNR Preparation

**Stakeholder**: Cabinet Office SDG Unit

**Driver Category**: STRATEGIC

**Driver Statement**: Use the SDG Dashboard as the authoritative evidence base for UK SDG policy coordination, Voluntary National Review preparation, and international reporting, demonstrating UK commitment to the 2030 Agenda.

**Context & Background**:
The UK is committed to the 2030 Agenda for Sustainable Development and presents Voluntary National Reviews (VNRs) to the UN High-Level Political Forum. The Cabinet Office SDG Unit coordinates cross-government SDG policy and needs a comprehensive, current data platform to identify gaps, prioritise interventions, and prepare VNR reports. The current process involves manually assembling data from multiple sources.

**Driver Intensity**: HIGH

**Enablers**:

- All 244 indicators available in machine-readable format
- Trend analysis showing progress trajectories
- Cross-referencing between SDG indicators and domestic policy frameworks
- VNR report generation from dashboard data

**Blockers**:

- Indicator gaps where UK data sources do not exist
- Lag between data collection and publication
- Difficulty comparing sub-national (England, Scotland, Wales, NI) performance

---

### SD-3: UN Statistics Division — Global SDG Monitoring Framework Compliance

**Stakeholder**: UN Statistics Division / IAEG-SDGs

**Driver Category**: COMPLIANCE

**Driver Statement**: Receive UK SDG data that is compliant with the Global SDG Indicator Framework methodology, reported in SDMX format, and submitted within UNSD reporting timelines to support the annual Secretary-General's SDG Progress Report.

**Context & Background**:
The IAEG-SDGs defines the methodology for each of the 244 SDG indicators. National statistical offices are responsible for producing compliant data. UNSD collects data via SDMX and through custodian agencies (e.g., WHO for health, UNESCO for education). The UK's reporting credibility depends on methodological alignment and timely submission.

**Driver Intensity**: HIGH

**Enablers**:

- SDMX-compliant data exchange with UNSD
- Methodology alignment with IAEG-SDGs indicator definitions
- Automated data submission pipeline
- Metadata compliant with SDMX metadata standard

**Blockers**:

- UK data sources that use different methodologies than IAEG-SDGs definitions
- Indicator disaggregation requirements that UK data does not support
- Resource constraints for methodology alignment work

---

### SD-4: Devolved Administrations — Sub-National SDG Reporting

**Stakeholder**: Scottish Government, Welsh Government, Northern Ireland Executive

**Driver Category**: OPERATIONAL

**Driver Statement**: Access UK SDG data disaggregated by nation (England, Scotland, Wales, Northern Ireland) and contribute devolved data sources to enable sub-national SDG monitoring that reflects devolved policy responsibilities.

**Context & Background**:
Scotland, Wales, and Northern Ireland have their own SDG implementation strategies and some have published their own VNR-equivalent reports. Devolved administrations want to report on SDG progress within their jurisdictions using consistent methodology but reflecting their distinct policy landscapes (e.g., Scotland's National Performance Framework already aligns with SDGs).

**Driver Intensity**: MEDIUM

**Enablers**:

- Sub-national disaggregation of UK indicators where data permits
- APIs enabling devolved administrations to embed UK SDG data in their own platforms
- Collaborative indicator development for devolved policy areas
- Recognition of devolved data sources alongside UK-wide data

**Blockers**:

- Many UK-wide indicators cannot be disaggregated to nation level
- Different data collection methods across devolved administrations
- Political sensitivities around comparative performance between nations

---

### SD-5: Civil Society (UKSSD, Bond) — Transparency and Accountability

**Stakeholder**: UK Stakeholders for Sustainable Development, Bond network, academic researchers

**Driver Category**: STRATEGIC

**Driver Statement**: Access open, machine-readable, comprehensive SDG data to hold the UK Government accountable for 2030 Agenda commitments, produce shadow reports, and conduct independent research on UK sustainable development progress.

**Context & Background**:
Civil society organisations produce shadow VNRs and annual assessments of UK SDG progress. Currently, they must assemble data from disparate sources, often with significant effort. A comprehensive, open dashboard would democratise access to SDG data and enable independent scrutiny.

**Driver Intensity**: MEDIUM

**Enablers**:

- Open data — all indicators available via public API without authentication
- Machine-readable formats (CSV, JSON, SDMX)
- Historical data for trend analysis
- Methodology documentation for each indicator
- Sub-national and demographic disaggregation

**Blockers**:

- Restricted access to any indicators
- Lack of API / programmatic access
- Missing methodology documentation

---

## Driver-to-Goal Mapping

### Goal G-1: Cover 200+ of 244 UN SDG Indicators

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: ONS SDG Team Lead

**Goal Statement**: Increase UK SDG indicator coverage from 180 to 200+ indicators within 18 months, with published methodology and data quality assessment for each.

**Success Metrics**:

- **Primary Metric**: Number of indicators with published data: 200+ (of 244)
- **Secondary Metrics**:
  - Tier 1 indicators (internationally established methodology): 100% coverage
  - Tier 2 indicators (methodology established, data gaps): 90% coverage
  - Methodology documentation published for each indicator

**Baseline**: ~180 indicators (2025)

**Target**: 200+ indicators

---

### Goal G-2: SDMX-Compliant Data Exchange with UNSD

**Derived From Drivers**: SD-3

**Goal Owner**: ONS International Team

**Goal Statement**: Implement automated SDMX data submission to UNSD, eliminating manual reporting and achieving 100% compliance with IAEG-SDGs metadata requirements within 12 months.

**Success Metrics**:

- **Primary Metric**: UNSD data submission fully automated via SDMX
- **Secondary Metrics**:
  - Metadata completeness: 100% of submitted indicators have compliant metadata
  - Submission timeliness: All data submitted within UNSD deadlines

---

### Goal G-3: Public Dashboard with Open API

**Derived From Drivers**: SD-2, SD-4, SD-5

**Goal Owner**: ONS Digital Services Director

**Goal Statement**: Launch a publicly accessible SDG Progress Dashboard with open API, sub-national disaggregation, and WCAG 2.1 AA accessibility within 18 months.

**Success Metrics**:

- **Primary Metric**: Dashboard live with public API access
- **Secondary Metrics**:
  - Monthly unique visitors: 10,000+ within 6 months of launch
  - API consumers: 50+ registered applications
  - Sub-national data available for 60%+ of indicators
  - WCAG 2.1 AA compliance verified

---

### Goal G-4: VNR Evidence Platform

**Derived From Drivers**: SD-2

**Goal Owner**: Cabinet Office SDG Unit

**Goal Statement**: Provide machine-readable data and automated report generation to support the next UK Voluntary National Review, reducing VNR data preparation time by 70%.

**Success Metrics**:

- **Primary Metric**: VNR data preparation time: < 2 weeks (vs. current ~8 weeks)
- **Secondary Metrics**:
  - All VNR indicators sourced from dashboard (zero bespoke data collection)
  - Trend analysis auto-generated for each indicator

---

## Goal-to-Outcome Mapping

### Outcome O-1: Authoritative UK SDG Monitoring

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: The UK has a single, authoritative, open platform for SDG monitoring recognised by UNSD, peer countries, and civil society as the definitive source of UK SDG data.

**Business Value**:

- **Strategic Impact**: Strengthens UK credibility in international SDG forums
- **Operational Impact**: Eliminates duplicate SDG data collection and publication efforts across government
- **International Impact**: Contributes to the global SDG monitoring framework quality

---

### Outcome O-2: Evidence-Based SDG Policy Making

**Supported Goals**: G-1, G-3, G-4

**Outcome Statement**: UK Government policy decisions on sustainable development are informed by comprehensive, current SDG indicator data, improving policy targeting and resource allocation.

**Business Value**:

- **Strategic Impact**: Policy decisions grounded in evidence rather than anecdote
- **Financial Impact**: Better resource allocation across SDG priorities (estimated GBP 5-10M efficiency gain)

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| UKSA/ONS | SD-1 | Statistical independence | G-1 | 200+ indicators | O-1 | Authoritative monitoring |
| Cabinet Office | SD-2 | Policy coordination | G-3 | Public dashboard | O-2 | Evidence-based policy |
| Cabinet Office | SD-2 | Policy coordination | G-4 | VNR evidence | O-2 | Evidence-based policy |
| UNSD | SD-3 | Global framework | G-2 | SDMX compliance | O-1 | Authoritative monitoring |
| Devolved admins | SD-4 | Sub-national data | G-3 | Public dashboard | O-1 | Authoritative monitoring |
| Civil society | SD-5 | Transparency | G-3 | Public dashboard | O-1 | Authoritative monitoring |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Cabinet Office (SD-2) wants all 244 indicators covered quickly; ONS (SD-1) insists on methodological rigour for each, which takes time
  - **Resolution Strategy**: Phased publication — Tier 1 indicators first (established methodology), then Tier 2 with methodology notes, then proxy indicators clearly labelled as experimental statistics

- **Conflict 2**: Policy teams want indicators presented with policy context and "good/bad" framing; UKSA (SD-1) requires statistical neutrality
  - **Resolution Strategy**: Separation of presentation layers — ONS publishes neutral data with methodology notes; Cabinet Office publishes a separate policy commentary document that references the dashboard data

**Synergies**:

- **Synergy 1**: Open API (G-3) simultaneously serves civil society transparency (SD-5), devolved administration needs (SD-4), and UNSD reporting (SD-3)
- **Synergy 2**: SDMX compliance (G-2) aligns with both UNSD requirements (SD-3) and ONS's existing statistical infrastructure (SD-1)

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Indicator methodology | ONS SDG Team Lead | National Statistician | IAEG-SDGs, UKSA | Source departments |
| Publication schedule | ONS SDG Team Lead | National Statistician | UKSA (pre-release) | All stakeholders |
| Platform architecture | ONS Digital Services | ONS CEO | CDDO, Cabinet Office | Source departments |
| Sub-national disaggregation | ONS SDG Team | ONS Methodology Dir | Devolved administrations | Cabinet Office |
| Policy commentary | Cabinet Office SDG Unit | Minister | ONS (factual review) | All stakeholders |

### Escalation Path

1. **Level 1**: ONS SDG Team Lead (day-to-day decisions)
2. **Level 2**: SRO and Programme Board (scope, timeline, indicator disputes)
3. **Level 3**: National Statistician / UKSA Chair (statistical independence issues, political interference)

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme SRO | | | |
| National Statistician | | | |
| Cabinet Office SDG Unit Head | | | |

---

## Appendices

### Appendix A: Key References

- Statistics and Registration Service Act 2007
- UKSA Code of Practice for Statistics
- UN General Assembly Resolution 70/1 (2030 Agenda)
- Global SDG Indicator Framework (IAEG-SDGs)
- SDMX (Statistical Data and Metadata eXchange) standard
- UK Voluntary National Review (2019, 2023)
- Scotland's National Performance Framework
- ARC-000-PRIN-v1.0 (SDG 17 Architecture Principles)

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG Progress Dashboard
**Model**: Claude Opus 4.6
