# Stakeholder Drivers & Goals Analysis: Labour Market Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Labour Market Intelligence (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Labour Market Intelligence Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | LMI Programme Board, ONS Digital, DWP Analytics, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Real-time Labour Market Intelligence platform, their drivers, goals, and measurable outcomes. The platform will aggregate, analyse, and publish real-time labour market data from administrative sources (HMRC RTI, DWP UC, Companies House), survey data (LFS, ASHE), and novel data sources (online job postings, vacancy APIs) to produce near-real-time labour market analytics and skills gap forecasting.

### Key Findings

The strongest alignment is around the need for timelier labour market data — the current Labour Force Survey (LFS) publishes with a 6-week lag, and the recent reduction in LFS response rates has undermined data quality. HM Treasury, DfE, and DWP all need faster, more granular data for policy decisions. The most significant tension is between ONS's commitment to statistical independence and the policy departments' desire for data outputs shaped to support specific policy narratives. ONS must maintain its statutory independence while delivering data that is genuinely useful for policy.

### Critical Success Factors

- Maintain ONS statistical independence — the UK Statistics Authority must approve the methodology
- Achieve near-real-time data refresh (weekly or better) compared to current monthly/quarterly cycles
- Successfully integrate HMRC RTI administrative data at sufficient granularity without compromising taxpayer confidentiality
- Deliver local-level labour market data (NUTS3/local authority level) to support Levelling Up decisions
- Establish the platform as the authoritative source for UK labour market intelligence, replacing fragmented departmental analyses

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Unusually strong alignment driven by the LFS quality crisis — all stakeholders agree that current labour market statistics are not fit for purpose. Tensions exist around data granularity (local vs. national), timeliness vs. accuracy trade-offs, and access to unpublished data.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| National Statistician | Head of ONS | HIGH | HIGH | Manage Closely — Strategic direction, statistical independence |
| Deputy National Statistician (Data Capability) | ONS Digital and Data leadership | HIGH | HIGH | Manage Closely — Architecture, data engineering |
| SRO, LMI Programme | Programme Sponsor | HIGH | HIGH | Manage Closely — Programme board |
| Head of Labour Market Statistics | ONS Labour Market Division | HIGH | HIGH | Manage Closely — Statistical methodology |
| ONS SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, data sharing agreements |
| ONS Data Engineering | Platform development | MEDIUM | HIGH | Keep Informed — Technical delivery |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| UK Statistics Authority (UKSA) | Regulator | Statistical regulation | HIGH | HIGH |
| HM Treasury | Policy customer | Economic forecasting | HIGH | HIGH |
| DWP | Partner department | Labour market policy | HIGH | HIGH |
| DfE | Partner department | Skills policy | HIGH | HIGH |
| DBT | Partner department | Industrial strategy | MEDIUM | HIGH |
| Bank of England | Independent body | Monetary policy | HIGH | MEDIUM |
| HMRC | Data supplier | RTI earnings data | HIGH | HIGH |
| Office for Budget Responsibility (OBR) | Independent body | Fiscal forecasting | HIGH | MEDIUM |
| Devolved Administrations | Scotland, Wales, NI | Devolved skills/employment policy | MEDIUM | HIGH |
| Local Authorities | Local government | Local economic planning | LOW | HIGH |
| Academic Researchers | Universities | Labour economics research | LOW | HIGH |
| Recruitment industry (REC) | Private sector | Vacancy data, market insights | LOW | MEDIUM |
| CDDO | Cabinet Office | Cross-government data standards | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Bank of England  │  • National         │
        │  • OBR              │    Statistician      │
        │  • ONS SIRO         │  • Dep. Nat. Stat.  │
        │  • CDDO             │  • SRO              │
        │                     │  • Head of Labour   │
        │                     │    Market Stats      │
 P      │                     │  • UKSA             │
 O      │                     │  • HM Treasury      │
 W      │                     │  • DWP              │
 E      │                     │  • DfE              │
        │                     │  • HMRC (data)      │
        ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • REC              │  • DBT              │
        │                     │  • Devolved Admins  │
        │                     │  • Local Authorities│
        │                     │  • Academic         │
        │                     │    Researchers       │
        │                     │  • ONS Data Eng.    │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: National Statistician — Restore Confidence in Labour Market Statistics

**Stakeholder**: National Statistician

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: The LFS response rate has fallen below 40%, undermining the quality of the UK's primary source of labour market data. The National Statistician must deliver a transformation that restores confidence in employment statistics by supplementing survey data with administrative and novel data sources, while maintaining Code of Practice compliance.

**Context & Background**: The UKSA downgraded the Labour Force Survey from National Statistics to Experimental Statistics in 2023 due to quality concerns. This was a significant reputational blow. The Transformed Labour Force Survey programme is underway, but the LMI platform is the broader data infrastructure needed to support a multi-source approach to labour market measurement. The National Statistician has publicly committed to restoring quality by 2027.

**Driver Intensity**: CRITICAL

---

### SD-2: HM Treasury — Timelier Data for Fiscal Decisions

**Stakeholder**: HM Treasury

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Treasury needs near-real-time labour market indicators to inform fiscal forecasting, Budget decisions, and intervention design. The current 6-week lag between data collection and publication is inadequate for economic management in a rapidly changing labour market.

**Context & Background**: During the COVID-19 pandemic, the furlough scheme was designed and calibrated with severely lagged labour market data. Real-time PAYE data (RTI) proved invaluable but was available only as experimental statistics. Treasury wants operational-quality real-time data as a permanent capability.

**Driver Intensity**: HIGH

---

### SD-3: DWP — Granular Local Labour Market Data for Jobcentre Operations

**Stakeholder**: DWP (Labour Market Policy and UC Operations)

**Driver Category**: OPERATIONAL

**Driver Statement**: DWP needs local-level labour market data (local authority or travel-to-work area) to inform Jobcentre operations, work coach priorities, and claimant commitment design. National averages mask enormous regional variation.

**Context & Background**: A work coach in Hartlepool faces a fundamentally different labour market to one in Cambridge. Current NOMIS data provides some local granularity but is delayed and limited in scope. The Job Matching Platform (Project 001) needs local labour market context to inform AI recommendations.

**Driver Intensity**: HIGH

---

### SD-4: HMRC — Controlled Access to RTI Data

**Stakeholder**: HMRC

**Driver Category**: COMPLIANCE

**Driver Statement**: HMRC will share RTI data for statistical purposes under existing legal gateways but requires strict controls on granularity, access, and publication to protect taxpayer confidentiality. RTI data must not be used in ways that could identify individual employers or employees.

**Driver Intensity**: HIGH

---

### SD-5: Academic Researchers — Open Access to Microdata

**Stakeholder**: Academic researchers (labour economists, social scientists)

**Driver Category**: STRATEGIC

**Driver Statement**: Researchers want access to detailed microdata for labour market research, subject to appropriate safeguards. Currently, access to linked administrative data is slow, bureaucratic, and inconsistent across departments.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Deliver Weekly Labour Market Indicators

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: Head of Labour Market Statistics

**Goal Statement**: Publish experimental weekly labour market indicators (employment, vacancies, earnings) based on administrative data, with defined quality measures, within 6 months of platform launch.

**Success Metrics**:
- **Primary Metric**: Publication frequency (target: weekly vs. current monthly)
- **Secondary Metrics**:
  - Data latency (target: 5 working days vs. current 6 weeks)
  - User satisfaction among policy customers (target: 80% rate as improvement)

---

### Goal G-2: Deliver Local Authority-Level Labour Market Data

**Derived From Drivers**: SD-3

**Goal Owner**: Deputy National Statistician

**Goal Statement**: Publish labour market indicators at local authority level (315 areas in England) with sufficient sample size/administrative coverage to be statistically robust, within 12 months.

**Success Metrics**:
- **Primary Metric**: Geographic granularity of published data
- **Secondary Metrics**:
  - Confidence intervals at local authority level (target: within +/- 2 percentage points)
  - Coverage of local authorities with publishable data (target: 95%)

---

### Goal G-3: Establish Secure Research Data Access

**Derived From Drivers**: SD-4, SD-5

**Goal Owner**: ONS SIRO

**Goal Statement**: Provide approved researchers with access to linked labour market microdata via the ONS Secure Research Service (SRS) within 20 working days of application, while maintaining Five Safes framework compliance.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| National Statistician | SD-1 | Restore statistical confidence | G-1 | Weekly indicators |
| HM Treasury | SD-2 | Timelier fiscal data | G-1 | Weekly indicators |
| DWP | SD-3 | Local labour market data | G-2 | LA-level data |
| HMRC | SD-4 | Controlled RTI access | G-1, G-2, G-3 | All (data source) |
| Academic Researchers | SD-5 | Open microdata access | G-3 | Research access |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: HM Treasury (SD-2) wants fast, frequent data publication. ONS statistical methodology (SD-1) requires quality assurance that takes time. Faster publication may mean lower accuracy.
  - **Resolution Strategy**: PHASE — Publish weekly experimental indicators with clear quality caveats alongside established monthly National Statistics. Users choose timeliness vs. accuracy based on their needs.

- **Conflict 2**: DWP (SD-3) and Academic Researchers (SD-5) want granular data. HMRC (SD-4) requires statistical disclosure control that limits granularity. The more granular the data, the higher the risk of identifying individual taxpayers.
  - **Resolution Strategy**: INNOVATE — Use synthetic data and cell perturbation methods to enable granular publication while protecting confidentiality. Provide researchers with access to unperturbed microdata only via the Secure Research Service.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 4, 11, 12, 13 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| UK Statistics Authority Code of Practice | Standard | UKSA | Trustworthiness, quality, value | https://code.statisticsauthority.gov.uk/ |
| Statistics and Registration Service Act 2007 | Legislation | UK Parliament | ONS statutory duties | https://www.legislation.gov.uk/ukpga/2007/18 |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Labour Market Intelligence
**Model**: Claude Opus 4.6
