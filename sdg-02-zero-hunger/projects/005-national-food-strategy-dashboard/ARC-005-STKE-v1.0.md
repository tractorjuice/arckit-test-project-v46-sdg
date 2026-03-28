# Stakeholder Drivers & Goals Analysis: National Food Strategy Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | National Food Strategy Dashboard (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, Cabinet Office Food Strategy Unit |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office, DEFRA, DfE, HM Treasury, No. 10 Policy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the National Food Strategy Dashboard, a cross-government monitoring platform that aggregates food system KPIs from all four SDG 2 operational projects (Food Supply Chain Resilience, School Meals Management, Food Waste Reduction Analytics, Agricultural Subsidy Management) and wider data sources. The dashboard provides ministers, policy makers, and the public with a coherent view of UK food system performance against the Government Food Strategy 2022 and Dimbleby Review recommendations.

### Key Findings

The strongest alignment is between the Cabinet Office's cross-government coordination mandate and DEFRA/DfE's need for a single place to demonstrate policy impact. The primary tension is between the desire for comprehensive, real-time data and the practical reality that source projects (001-004) deliver on different timelines, meaning the dashboard must operate with partial data during the first 18 months. Ministerial appetite for a public-facing dashboard creates both opportunity (transparency) and risk (premature publication of incomplete metrics).

### Critical Success Factors

- Securing reliable data feeds from all four source projects (001-004) with agreed quality SLAs
- Managing ministerial expectations about data availability during phased delivery
- Designing metrics that accurately represent food system health without oversimplification
- Delivering a public-facing dashboard that meets GDS Service Standard and is accessible to citizens

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

All stakeholders agree on the need for a cross-government food strategy monitoring capability. Tensions are primarily around timing, data availability, and the balance between public transparency and data readiness.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-1: Cabinet Secretary | Head of Civil Service | HIGH | MEDIUM | Keep Satisfied -- quarterly briefings |
| S-2: Minister for the Cabinet Office | Minister | HIGH | HIGH | Manage Closely -- ministerial briefings |
| S-3: Director, Food Strategy Unit | Programme Sponsor | HIGH | HIGH | Programme board |
| S-4: SRO, Food Strategy Dashboard | Senior Responsible Owner | HIGH | HIGH | Weekly programme board |
| S-5: Cabinet Office CDO | Digital Strategy Lead | HIGH | HIGH | Architecture reviews |
| S-6: No. 10 Policy Unit | PM's advisory team | HIGH | MEDIUM | Keep Satisfied -- policy briefings |
| S-7: Cabinet Office Data Team | Analytics and reporting | MEDIUM | HIGH | Sprint reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-8: DEFRA (Projects 001, 003, 004) | Data providers | HIGH | HIGH |
| S-9: DfE (Project 002) | Data provider | MEDIUM | MEDIUM |
| S-10: Food Standards Agency | Data provider | MEDIUM | MEDIUM |
| S-11: ONS | Statistics, methodology | MEDIUM | HIGH |
| S-12: Public (citizens) | Data consumers | LOW | HIGH |
| S-13: Henry Dimbleby / National Food Strategy Review | Advisory | LOW | HIGH |
| S-14: CDDO | Spend control / assurance | HIGH | MEDIUM |
| S-15: HM Treasury | Budget and performance | HIGH | MEDIUM |
| S-16: Parliamentary committees | Scrutiny | HIGH | MEDIUM |
| S-17: Food industry bodies (FDF, BRC, NFU) | Data quality interest | MEDIUM | MEDIUM |

---

## Stakeholder Drivers Analysis

### SD-1: Minister for the Cabinet Office -- Cross-Government Accountability

**Stakeholder**: S-2 Minister for the Cabinet Office

**Driver Category**: STRATEGIC

**Driver Statement**: Demonstrate cross-government delivery against the Government Food Strategy 2022, providing a single, authoritative view of UK food system performance for parliamentary accountability and public communication.

**Context & Background**: The Government Food Strategy 2022 (the government's response to the Dimbleby Review) committed to numerous actions across DEFRA, DfE, DHSC, and other departments. Currently there is no single place to track progress. Parliamentary questions about food strategy delivery require manual data gathering across departments, taking days. The Minister needs a dashboard that provides instant answers.

**Driver Intensity**: HIGH

**Enablers**:
- Automated data feeds from all relevant departments
- Pre-defined KPIs aligned with Food Strategy commitments
- Ministerial briefing pack auto-generation
- Drill-down from headline metrics to departmental detail

**Blockers**:
- Source projects (001-004) delivering on different timelines
- Data quality and timeliness vary across departments
- Political sensitivity of publishing metrics showing poor performance
- Cross-departmental data governance complexity

---

### SD-2: No. 10 Policy Unit -- Strategic Early Warning

**Stakeholder**: S-6 No. 10 Policy Unit

**Driver Category**: STRATEGIC / RISK

**Driver Statement**: Have advance warning of emerging food system issues (supply disruptions, school meals coverage gaps, agricultural sector stress, food waste trends) before they become politically visible, enabling proactive rather than reactive Number 10 communications.

**Context & Background**: Number 10 has been caught off-guard by food system issues in the past (empty shelves during COVID, egg shortage 2022, school meals controversies). The Policy Unit needs a "single pane of glass" for food system health, alerting them to deteriorating trends before media or parliamentary pressure builds.

**Driver Intensity**: MEDIUM

---

### SD-3: DEFRA/DfE Data Teams -- Manageable Data Obligations

**Stakeholder**: S-8 (DEFRA), S-9 (DfE)

**Driver Category**: OPERATIONAL

**Driver Statement**: Publish data to the dashboard through standard APIs with clear specifications, without creating additional manual reporting burden on source project teams.

**Context & Background**: Source projects (001-004) are building their own systems with their own delivery pressures. Additional data obligations for the Cabinet Office dashboard could be seen as a distraction. Data providers need clear, stable API contracts and automated data publication -- not ad-hoc data requests.

**Driver Intensity**: MEDIUM

**Enablers**:
- Standardised API specifications agreed early
- Automated data feeds (no manual reports)
- Dashboard consumes existing APIs, not bespoke data extracts
- Data quality issues surfaced as feedback to source systems, not complaints

**Blockers**:
- Unstable API specifications if dashboard requirements change frequently
- Dashboard demanding data that source systems don't yet produce
- Misaligned release schedules creating integration friction

---

### SD-4: ONS -- Statistical Integrity

**Stakeholder**: S-11 ONS

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure dashboard metrics meet national statistics quality standards, with transparent methodology, appropriate caveats, and clear distinction between official statistics and operational data.

**Context & Background**: If the dashboard publishes food system metrics as national statistics, they must comply with the Code of Practice for Statistics. Even if classified as management information, the ONS expects transparent methodology. Poorly presented statistics could mislead policy decisions or public understanding.

**Driver Intensity**: MEDIUM

---

### SD-5: Citizens -- Transparent Food System Information

**Stakeholder**: S-12 Public

**Driver Category**: CUSTOMER

**Driver Statement**: Access clear, understandable information about UK food system performance -- supply chain health, school meals uptake, food waste progress, and agricultural sustainability -- as part of open government commitments.

**Context & Background**: The Dimbleby Review recommended greater transparency about the UK food system. Public interest in food issues is high (food prices, nutrition, environment). A public-facing dashboard demonstrates government accountability and supports informed public debate.

**Driver Intensity**: LOW

---

## Driver-to-Goal Mapping

### Goal G-1: Operational Cross-Government Dashboard

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: S-4 SRO

**Goal Statement**: Deliver an internal cross-government dashboard aggregating food system KPIs from Projects 001-004 and external sources, providing ministerial-level reporting within 2 clicks, by Q2 2028.

**Success Metrics**:
- **Primary Metric**: Time to answer a ministerial food strategy question (target: < 5 minutes vs current 3+ days)
- **Secondary Metrics**: Number of KPIs tracked, data source coverage, user satisfaction

**Baseline**: No dashboard; manual data gathering across departments

**Target**: 50+ KPIs, 4+ department data sources, < 5 minute query resolution

---

### Goal G-2: Public Food Strategy Dashboard

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: S-3 Director

**Goal Statement**: Publish a citizen-facing food strategy dashboard on GOV.UK showing progress against Government Food Strategy commitments, with quarterly updates, by Q4 2028.

**Success Metrics**:
- **Primary Metric**: Number of public dashboard visits per quarter
- **Secondary Metrics**: Media citations, FOI request reduction, accessibility compliance

---

### Goal G-3: Automated Data Integration

**Derived From Drivers**: SD-3

**Goal Owner**: S-5 CDO

**Goal Statement**: Establish automated data feeds from all four SDG 2 source projects via standardised APIs with agreed data quality SLAs, by Q3 2028.

**Success Metrics**:
- **Primary Metric**: Percentage of data feeds automated (target: 100%)
- **Secondary Metrics**: Data freshness compliance, API availability

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Minister | SD-1 | Cross-govt accountability | G-1, G-2 | Internal + public dashboards |
| No. 10 | SD-2 | Strategic early warning | G-1 | Internal dashboard with alerts |
| DEFRA/DfE | SD-3 | Manageable data obligations | G-3 | Automated API feeds |
| ONS | SD-4 | Statistical integrity | G-2 | Methodology-compliant public dashboard |
| Citizens | SD-5 | Transparency | G-2 | Public dashboard |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Rapid dashboard delivery (SD-1) vs source project readiness (SD-3). The dashboard cannot publish data that source projects haven't yet built APIs for.
  - **Resolution Strategy**: Phased dashboard delivery aligned with source project milestones. Start with available data (ONS statistics, existing DEFRA/DfE published data), add operational data as source APIs come online.

- **Conflict 2**: Public transparency ambition (SD-5) vs political sensitivity of incomplete metrics (SD-1). Publishing a public dashboard with gaps or negative trends creates political risk.
  - **Resolution Strategy**: Internal dashboard first (Q2 2028), public dashboard later (Q4 2028) once data is stable. Clear methodology notes and caveats on all public metrics.

**Synergies**:

- **Synergy 1**: All four source projects (001-004) need to publish metrics -- the dashboard provides a single consumer, reducing the number of ad-hoc data requests each project receives.
- **Synergy 2**: ONS methodology guidance (SD-4) benefits all source projects' data quality, not just the dashboard.

---

## Communication & Engagement Plan

### Cross-Government Data Providers (DEFRA, DfE)

**Primary Message**: The dashboard consumes your existing APIs -- we adapt to your data, not the other way around. Early API specification agreement prevents future friction.

**Communication Frequency**: Monthly during development, quarterly in operations

**Preferred Channel**: Cross-programme data board, bilateral technical meetings

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| KPI selection and methodology | Food Strategy Unit | Minister | ONS, DEFRA, DfE | All |
| API specifications | CDO | SRO | Source project teams | All |
| Public dashboard publication | Comms team | Minister | No. 10, ONS | All |
| Data quality escalation | Data team | SRO | Source project SROs | All |
| Budget allocation | Finance | SRO | HMT | All |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Source Project Data Unavailability

**Related Stakeholders**: S-8 (DEFRA), S-9 (DfE)

**Risk Description**: Source projects 001-004 deliver on different timelines. Dashboard may have significant data gaps during first 18 months.

**Probability**: HIGH

**Impact**: MEDIUM

**Mitigation**: Phased dashboard delivery; use existing published statistics as interim; clear communication about data availability timeline.

---

### Risk R-2: Ministerial Pressure for Premature Public Release

**Related Stakeholders**: S-2 (Minister), S-6 (No. 10)

**Risk Description**: Political pressure to publish public dashboard before data quality is sufficient, leading to inaccurate or misleading metrics.

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation**: Internal dashboard first; clear data quality criteria for public release; ONS methodology review before publication.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Government Food Strategy 2022 | Policy | DEFRA/Cabinet Office | Policy commitments and KPIs | gov.uk |
| Dimbleby National Food Strategy 2021 | Review | Independent | Recommendations for food system reform | nationalfoodstrategy.org |
| UK Code of Practice for Statistics | Standard | UK Statistics Authority | Quality, integrity, value standards | code.statisticsauthority.gov.uk |
| ARC-000-PRIN-v1.0 | Principles | SDG 2 | Governing architecture principles | ARC-000-PRIN-v1.0.md |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Food Strategy Dashboard
**Model**: Claude Opus 4.6
