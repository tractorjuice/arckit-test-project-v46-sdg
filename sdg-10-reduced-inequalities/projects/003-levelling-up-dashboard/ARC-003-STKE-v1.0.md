# Stakeholder Drivers & Goals Analysis: Levelling Up Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Levelling Up Dashboard (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Levelling Up Dashboard, DLUHC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Levelling Up Directorate, Cities & Local Growth Unit, Regional Mayors, ONS |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Levelling Up Dashboard, their underlying drivers, how these manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Levelling Up Dashboard must serve two fundamentally different audiences with conflicting needs: ministers and senior officials who want headline metrics showing progress against Levelling Up missions, and local leaders (regional mayors, council leaders, LEP chairs) who want granular, actionable data showing how their areas compare and where funding is making a difference. The most significant tension is between the political pressure to show improvement and the statistical reality that meaningful regional inequality reduction takes decades to manifest in outcome data. ONS insists on methodological rigour that may produce uncomfortable truths; ministers want narrative-friendly data that demonstrates return on investment.

### Critical Success Factors

- Integrate Index of Multiple Deprivation (IMD), Index of Deprivation (IoD), ONS subnational statistics, and Levelling Up Fund allocation data into a single geospatial platform within 12 months
- Provide real-time fund allocation tracking against all 12 Levelling Up missions
- Enable geographic analysis at LSOA, MSOA, local authority, and constituency levels
- Publish as open data to support independent scrutiny and academic research
- Withstand scrutiny from NAO, IFS, and academic researchers on methodology

### Stakeholder Alignment Score

**Overall Alignment**: LOW

Fundamental tensions between political messaging needs, statistical rigour requirements, local accountability demands, and the inherent timescales of inequality reduction. The dashboard will be used by stakeholders with opposing objectives — some to demonstrate success, others to highlight failure.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Levelling Up | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DLUHC Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Levelling Up Dashboard | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DLUHC Director, Cities & Local Growth | Policy directorate | HIGH | HIGH | Manage Closely — Data requirements, fund tracking |
| DLUHC Chief Analyst | Analytical standards | HIGH | HIGH | Manage Closely — Methodology approval |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews |
| DLUHC CDIO | Technology oversight | HIGH | MEDIUM | Keep Satisfied — Architecture governance |
| DLUHC Finance | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| ONS (Office for National Statistics) | Statistics authority | Data provider, methodology authority | HIGH | HIGH |
| HM Treasury | Funding department | Levelling Up Fund allocation approval | HIGH | MEDIUM |
| Regional mayors | Combined authorities | Major data consumers, accountability | MEDIUM | HIGH |
| Local authority leaders/CEOs | ~340 local authorities | Data consumers, fund recipients | LOW | HIGH |
| NAO (National Audit Office) | Parliament | Value for money audit | HIGH | MEDIUM |
| IFS (Institute for Fiscal Studies) | Think tank | Independent analysis of Levelling Up impact | LOW | HIGH |
| House of Commons Levelling Up Committee | Parliament | Scrutiny of Levelling Up policy | HIGH | HIGH |
| Local Enterprise Partnerships (LEPs) | Business-led partnerships | Economic development data consumers | LOW | MEDIUM |
| Ordnance Survey | Partner | Geospatial data and mapping services | MEDIUM | MEDIUM |
| What Works Centre for Local Economic Growth | Research body | Evidence of intervention effectiveness | LOW | HIGH |
| Citizens in left-behind areas | Citizens | Ultimate beneficiaries | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of     |
        |  * DLUHC CDIO       |    State            |
        |  * DLUHC Finance    |  * Permanent Sec.   |
        |  * NAO              |  * SRO              |
 P      |                     |  * DLUHC Director   |
 O      |                     |  * Chief Analyst    |
 W      |                     |  * ONS              |
 E      |                     |  * Commons Committee|
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * LEPs             |  * Regional mayors  |
        |  * Ordnance Survey  |  * Local authority  |
        |                     |    leaders          |
        |                     |  * IFS              |
        |                     |  * What Works Centre|
        |                     |  * Citizens         |
        |                     |  * Service Owner    |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Demonstrable Levelling Up Progress

**Stakeholder**: Secretary of State for Levelling Up, Housing and Communities

**Driver Category**: STRATEGIC

**Driver Statement**: Provide a credible, public-facing dashboard that demonstrates measurable progress against Levelling Up missions, supporting the government's political narrative that Levelling Up funding is reducing regional inequalities.

**Context & Background**:
The Levelling Up and Regeneration Act 2023 requires the government to report on missions and metrics. The Secretary of State faces regular parliamentary scrutiny on whether Levelling Up is working. A compelling dashboard with improving trends is essential for political credibility, but the data must also be robust enough to withstand NAO and academic scrutiny.

**Driver Intensity**: CRITICAL

**Enablers**:

- Data that shows trends over time, not just snapshots
- Narrative-friendly visualisations for ministerial use
- Attribution analysis linking fund allocations to outcome improvements

**Blockers**:

- Regional inequality metrics move slowly — visible improvement may take 5-10 years
- ONS methodology may show unflattering truths
- Opposition will use the same data to highlight areas of failure

---

### SD-2: ONS — Methodological Rigour and Statistical Independence

**Stakeholder**: Office for National Statistics

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure that all statistics presented on the dashboard meet the Code of Practice for Statistics, maintain clear separation between official statistics and political commentary, and do not misrepresent data through selective presentation or misleading visualisations.

**Context & Background**:
ONS has a statutory obligation to ensure statistics are trustworthy, high quality, and serve the public good. Previous government dashboards have been criticised by the UK Statistics Authority for misleading presentations. ONS will not endorse a dashboard that cherry-picks metrics or presents data out of context.

**Driver Intensity**: CRITICAL

**Enablers**:

- Joint ONS-DLUHC methodology panel
- All statistical methodology published transparently
- Dashboard displays confidence intervals and data quality indicators

**Blockers**:

- Political pressure to present data favourably
- Tension between statistical rigour and user-friendly simplification
- ONS publication timelines may not align with political needs

---

### SD-3: Regional Mayors — Local Accountability and Fund Tracking

**Stakeholder**: Regional mayors (Greater Manchester, West Midlands, West Yorkshire, etc.)

**Driver Category**: OPERATIONAL

**Driver Statement**: Track Levelling Up Fund allocations to their regions, benchmark against other regions, and demonstrate to constituents that devolution is delivering measurable improvements in their area.

**Context & Background**:
Regional mayors have their own democratic mandates and need data to demonstrate effectiveness. They want to show how their regions are performing relative to others and how Levelling Up funds are being spent. They also want early warning of emerging inequalities within their regions.

**Driver Intensity**: HIGH

**Enablers**:

- Region-level dashboards with customisable views
- Fund allocation tracking with project-level granularity
- Exportable data for mayoral reports and press releases

**Blockers**:

- Some fund allocation decisions made centrally without mayoral input
- Difficulty attributing outcome changes to specific fund allocations
- Intra-regional inequality masked by regional averages

---

### SD-4: House of Commons Levelling Up Committee — Scrutiny Evidence

**Stakeholder**: House of Commons Levelling Up, Housing and Communities Committee

**Driver Category**: COMPLIANCE

**Driver Statement**: Access robust, independently verifiable data to scrutinise whether Levelling Up policy is achieving its stated missions and whether public money is being well spent, with sufficient granularity to examine specific areas and programmes.

**Driver Intensity**: HIGH

**Enablers**:

- Open data publication enabling independent analysis
- Downloadable datasets in machine-readable formats
- Historical data for trend analysis

**Blockers**:

- Government may resist transparency on underperforming areas
- Data latency may limit scrutiny of recent fund allocations

---

### SD-5: Local Authority Leaders — Granular Area Data and Fair Funding

**Stakeholder**: Local authority leaders and CEOs

**Driver Category**: OPERATIONAL

**Driver Statement**: Access LSOA-level deprivation and inequality data to identify pockets of deprivation within their boundaries, support funding bids with evidence, and demonstrate the impact of local interventions to their residents.

**Driver Intensity**: MEDIUM

**Enablers**:

- LSOA/MSOA level geospatial visualisation
- IMD and IoD integration with Levelling Up fund data
- Benchmarking against statistically similar areas (CIPFA nearest neighbours)

**Blockers**:

- Data availability at sub-local-authority level varies significantly by metric
- Small area estimation introduces statistical uncertainty
- Capacity of smaller authorities to use complex data tools

---

## Driver-to-Goal Mapping

### Goal G-1: Integrated Geospatial Inequality Dashboard

**Derived From Drivers**: SD-1, SD-3, SD-5

**Goal Owner**: DLUHC Director, Cities & Local Growth

**Goal Statement**: Launch a public-facing geospatial dashboard integrating IMD, IoD, ONS subnational statistics, and Levelling Up Fund allocation data, with visualisation from LSOA to national level, within 12 months.

**Success Metrics**:

- **Primary Metric**: Dashboard live with 15+ inequality metrics mapped geospatially
- **Secondary Metrics**:
  - Monthly active users
  - Data sources integrated
  - Geographic levels available

**Baseline**: No centralised Levelling Up data platform; data scattered across DLUHC, ONS, and departmental publications

**Target**: Dashboard live, 15+ metrics, 5+ geographic levels, 10,000+ monthly users within 12 months

---

### Goal G-2: Levelling Up Fund Allocation Tracking

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Provide real-time tracking of all Levelling Up Fund allocations (Rounds 1-3, Towns Fund, UK Shared Prosperity Fund, Community Ownership Fund) mapped to geographic areas and linked to outcome metrics, within 12 months.

**Success Metrics**:

- **Primary Metric**: Percentage of fund allocations tracked with geographic mapping
- **Secondary Metrics**:
  - Fund allocation to outcome metric correlation visibility
  - Timeliness of fund allocation data updates

**Baseline**: Fund allocation data published in static spreadsheets and parliamentary written statements

**Target**: 100% of major Levelling Up funds tracked, updated within 5 working days of allocation announcements

---

### Goal G-3: ONS-Endorsed Methodology

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: DLUHC Chief Analyst

**Goal Statement**: Obtain ONS endorsement of the dashboard's statistical methodology and data presentation approach within 18 months, ensuring compliance with the Code of Practice for Statistics.

**Success Metrics**:

- **Primary Metric**: ONS written endorsement of methodology
- **Secondary Metrics**:
  - UK Statistics Authority review completed
  - Methodology paper peer-reviewed and published
  - No adverse findings from UK Statistics Authority

**Baseline**: No existing methodological framework for Levelling Up measurement

**Target**: ONS endorsement within 18 months, Code of Practice compliance confirmed

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Demonstrable progress | G-1 | Geospatial dashboard | O-1 | Transparent inequality tracking |
| Secretary of State | SD-1 | Demonstrable progress | G-2 | Fund allocation tracking | O-2 | Accountable fund spending |
| ONS | SD-2 | Methodological rigour | G-3 | ONS-endorsed methodology | O-1 | Transparent inequality tracking |
| Regional mayors | SD-3 | Local accountability | G-1 | Geospatial dashboard | O-2 | Accountable fund spending |
| Regional mayors | SD-3 | Local accountability | G-2 | Fund allocation tracking | O-2 | Accountable fund spending |
| Commons Committee | SD-4 | Scrutiny evidence | G-2 | Fund allocation tracking | O-1 | Transparent inequality tracking |
| Local authorities | SD-5 | Granular area data | G-1 | Geospatial dashboard | O-1 | Transparent inequality tracking |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Secretary of State (SD-1) wants data that supports a positive narrative, but ONS (SD-2) insists on presenting all data impartially, including areas where inequality is worsening.
  - **Resolution Strategy**: Dashboard presents data without political commentary. DLUHC ministers can reference dashboard data in speeches, but the platform itself maintains statistical neutrality. ONS reviews all default visualisation choices.

- **Conflict 2**: Regional mayors (SD-3) want attribution of improvements to Levelling Up funds, but ONS methodology (SD-2) cannot establish causality from observational data alone.
  - **Resolution Strategy**: Dashboard shows fund allocation alongside outcome trends but does not claim causality. A separate "What Works" section references evaluated evidence of intervention effectiveness from the What Works Centre.

**Synergies**:

- **Synergy 1**: Commons Committee scrutiny needs (SD-4) and ONS methodological rigour (SD-2) both benefit from open data publication and transparent methodology
- **Synergy 2**: Regional mayors' benchmarking needs (SD-3) and local authorities' granular data needs (SD-5) both require the same geospatial infrastructure and IMD integration

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Dashboard Shows Worsening Inequalities

**Related Stakeholders**: Secretary of State, regional mayors

**Risk Description**: The dashboard reveals that regional inequalities are widening despite Levelling Up investment, creating political embarrassment and undermining support for the programme.

**Probability**: MEDIUM | **Impact**: HIGH

**Mitigation Strategy**: Present data with appropriate caveats about timescales for structural change. Include leading indicators (fund allocation, programme starts) alongside lagging outcome indicators. Set realistic expectations about the timescale for measurable improvement.

---

### Risk R-2: UK Statistics Authority Criticism

**Related Stakeholders**: ONS, DLUHC Chief Analyst

**Risk Description**: The UK Statistics Authority finds the dashboard's presentation misleading or non-compliant with the Code of Practice, requiring withdrawal or significant rework.

**Probability**: MEDIUM | **Impact**: HIGH

**Mitigation Strategy**: Engage ONS and UK Statistics Authority from Discovery. Voluntary pre-assessment review before public launch. DLUHC Chief Analyst signs off all methodology and presentation choices.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Metric selection | DLUHC Chief Analyst | SRO | ONS, Secretary of State | All |
| Data presentation | Service Owner | DLUHC Chief Analyst | ONS, DLUHC Director | All |
| Budget approval | DLUHC Finance | SRO | CDDO | All |
| Architecture | Technical Lead | SRO | Ordnance Survey, CDDO | Development team |
| Fund data integration | DLUHC Director | Permanent Secretary | HM Treasury, fund managers | Regional mayors |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Levelling Up White Paper | Policy | GOV.UK | 12 missions, metrics framework | N/A — external reference |
| Levelling Up and Regeneration Act 2023 | Legislation | legislation.gov.uk | Statutory reporting obligations | N/A — external reference |
| Index of Multiple Deprivation | Dataset | DLUHC | Deprivation scores by LSOA | N/A — external reference |
| Code of Practice for Statistics | Standard | UK Statistics Authority | Trustworthiness, quality, value | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Levelling Up Dashboard
**Model**: Claude Opus 4.6
