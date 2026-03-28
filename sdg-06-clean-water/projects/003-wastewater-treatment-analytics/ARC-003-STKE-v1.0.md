# Stakeholder Drivers & Goals Analysis: Wastewater Treatment Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Wastewater Treatment Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Wastewater Treatment Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Ofwat, Environment Agency, DEFRA, Water Companies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Wastewater Treatment Analytics platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This platform sits at the centre of the most politically contentious area of UK water management — sewage treatment performance and storm overflow discharges.

### Key Findings

The Wastewater Treatment Analytics platform must serve two fundamentally different constituencies: Ofwat as the economic regulator (focused on comparative performance assessment, price setting, and enforcement) and the general public (focused on whether their local river or beach is safe). The dominant tension is between water companies' desire to control performance narratives (through methodology choices, data presentation, and contextual framing) and the regulatory and public demand for independent, standardised, and transparent performance data. The Storm Overflow Discharge Reduction Plan creates legally binding targets that require robust, auditable analytics — making this platform critical to Environment Act 2021 compliance.

### Critical Success Factors

- Establish a single, trusted source of truth for sewage treatment performance metrics across all 11 water and sewerage companies in England and Wales
- Automate Ofwat's comparative performance assessment, reducing the annual data assurance cycle from 6 months to 6 weeks
- Provide real-time storm overflow discharge monitoring with public-facing dashboards
- Deliver auditable analytics supporting Environment Act 2021 storm overflow reduction targets
- Maintain regulatory independence while ensuring water company buy-in to methodology

### Stakeholder Alignment Score

**Overall Alignment**: LOW-MEDIUM

Fundamental alignment on the need for better wastewater performance data is undermined by deep tensions over methodology, data ownership, and publication timing. Water companies view the platform as a potential enforcement weapon. Ofwat views it as essential regulatory infrastructure. The public views it through the lens of the sewage discharge crisis. These perspectives are difficult to reconcile fully.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Ofwat Chief Executive | Agency leadership | HIGH | HIGH | Manage Closely — Programme board |
| Ofwat Director of Strategy and Performance | Programme sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| Ofwat Chief Economist | Methodology authority | HIGH | HIGH | Manage Closely — Methodology design |
| Ofwat Director of Enforcement | Enforcement use | HIGH | HIGH | Manage Closely — Evidence requirements |
| Ofwat Digital Director | Technical leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Ofwat Board | Governance oversight | HIGH | MEDIUM | Keep Satisfied — Board papers, milestone reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DEFRA Secretary of State | DEFRA | Policy sponsorship | HIGH | HIGH |
| DEFRA Water Policy Director | DEFRA | Environment Act compliance | HIGH | HIGH |
| Environment Agency CEO | Environment Agency | Environmental enforcement | HIGH | HIGH |
| EA Director of Water Quality | EA | Permit compliance monitoring | HIGH | HIGH |
| Water Companies (11 WaSCs) | Industry | Regulated entities | HIGH | HIGH |
| Water UK | Industry body | Industry coordination | MEDIUM | HIGH |
| Consumer Council for Water (CCW) | Consumer body | Customer representation | MEDIUM | HIGH |
| Surfers Against Sewage | Campaign group | Public advocacy | MEDIUM | HIGH |
| Rivers Trust | Charity | Environmental advocacy | LOW | HIGH |
| HM Treasury | HM Treasury | Funding | HIGH | MEDIUM |
| CDDO | Cabinet Office | Digital standards | HIGH | MEDIUM |
| NAO | Parliament | Value for money audit | HIGH | MEDIUM |
| General public / bill payers | Citizens | Service users | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Ofwat CEO        |
        |  * CDDO             |  * Ofwat Dir of     |
        |  * NAO              |    Strategy          |
        |  * Ofwat Board      |  * Ofwat Chief      |
        |                     |    Economist         |
 P      |                     |  * Ofwat Dir of     |
 O      |                     |    Enforcement       |
 W      |                     |  * DEFRA Sec of     |
 E      |                     |    State             |
 R      |                     |  * EA CEO           |
        |                     |  * Water Companies  |
        |                     |  * DEFRA Policy Dir |
        +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * General public   |
        |                     |  * CCW              |
        |                     |  * Surfers Against  |
        |                     |    Sewage            |
        |                     |  * Rivers Trust     |
        |                     |  * Water UK         |
        |                     |  * EA Water Quality |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Ofwat — Robust Comparative Performance Assessment

**Stakeholder**: Ofwat Chief Executive and Chief Economist

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Establish an independent, auditable analytics platform that enables fair comparative assessment of water company sewage treatment performance, supporting evidence-based price review determinations and enforcement actions.

**Context & Background**:
Ofwat's price review process (PR29) will set customer bills and investment requirements for 2030-2035. Performance metrics — including pollution incidents, treatment works compliance, and storm overflow frequency — are central to this process. Currently, Ofwat relies on water company Annual Performance Reports (APRs) validated through external assurance. This process takes 6 months, costs GBP 40M industry-wide in assurance fees, and has been criticised for allowing companies to influence their own performance narrative through methodology choices and data presentation. An independent analytics platform would strengthen regulatory credibility.

**Driver Intensity**: CRITICAL

**Enablers**:
- Direct access to water company operational telemetry (SCADA data, flow monitors, EDMs)
- Standardised calculation methodology applied consistently across all 11 companies
- Automated data validation reducing reliance on company self-assurance
- Historical data enabling trend analysis and anomaly detection

**Blockers**:
- Water company resistance to providing raw operational data (commercial sensitivity claims)
- Legal challenges to Ofwat's data access powers under the Water Industry Act 1991
- Complexity of normalising performance data across companies with different infrastructure ages and catchment characteristics

---

### SD-2: Water Companies — Fair Comparison and Methodology Influence

**Stakeholder**: Water Companies (11 water and sewerage companies in England and Wales)

**Driver Category**: FINANCIAL / RISK / COMPLIANCE

**Driver Statement**: Ensure that any centralised analytics platform applies fair, contextualised methodology that accounts for differences in infrastructure age, catchment characteristics, population density, and investment cycles — avoiding simplistic league tables that mislead the public and distort regulatory outcomes.

**Context & Background**:
Water companies face intense public and political scrutiny. Simplified performance comparisons (e.g., "Company X had 10,000 sewage spills") do not account for network size, catchment rainfall, or permitted discharge conditions. Companies fear that a centralised platform will enable misleading comparisons that damage reputations and influence Ofwat enforcement disproportionately. However, companies also recognise that the current self-reported model is losing credibility and that independent analytics may ultimately be more defensible than self-reporting.

**Driver Intensity**: HIGH

**Enablers**:
- Contextual normalisation in all performance metrics (per km of sewer, per capita, rainfall-adjusted)
- Transparent methodology with industry consultation before implementation
- Company-specific commentary capability alongside standardised metrics
- Phased implementation with parallel running against existing reporting

**Blockers**:
- Pressure from campaigners and media for simple, unnormalised comparisons
- Inconsistent data quality across companies (varying SCADA system ages and reliability)
- Fear that independent analytics will reveal underperformance previously masked by self-reporting

---

### SD-3: DEFRA — Environment Act 2021 Compliance Monitoring

**Stakeholder**: DEFRA Water Policy Director

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Track progress against Storm Overflow Discharge Reduction Plan targets with sufficient granularity and auditability to demonstrate UK compliance with legally binding environmental commitments.

**Context & Background**:
The Environment Act 2021 and the Storm Overflow Discharge Reduction Plan set progressive targets: eliminate ecological harm from storm overflows by 2050, with interim targets for reductions in overflow frequency and duration. DEFRA needs a platform that tracks progress against these targets at the individual overflow level, providing auditable evidence for Parliamentary reporting and potential legal challenge. The targets are legally binding and DEFRA faces judicial review risk if progress cannot be demonstrated.

**Driver Intensity**: CRITICAL

**Enablers**:
- Individual storm overflow tracking against legally binding reduction targets
- Auditable methodology linking overflow performance to ecological impact
- Automated progress reporting for Parliamentary and Ministerial use
- Integration with EA environmental monitoring data for ecological outcome assessment

**Blockers**:
- Scientific uncertainty in linking overflow frequency to ecological impact
- Disagreement between stakeholders on how to measure "ecological harm"
- 2050 target timeline creates urgency-complacency tension in near-term investment

---

### SD-4: General Public / Consumer Council for Water — Accountability and Value for Money

**Stakeholder**: General public (bill payers), Consumer Council for Water (CCW)

**Driver Category**: CUSTOMER / FINANCIAL

**Driver Statement**: Understand how well water companies are performing on sewage treatment, whether customer bill increases are delivering improved environmental outcomes, and hold underperforming companies to account.

**Context & Background**:
Water bills have increased significantly to fund environmental improvements, yet public perception is that sewage treatment is getting worse. CCW research shows that 67% of customers do not believe water companies are doing enough to prevent sewage pollution. Customers want clear, independent information showing whether their money is being spent effectively. The platform must make performance data accessible and understandable to non-expert audiences.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Automated Comparative Performance Assessment

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: Ofwat Chief Economist

**Goal Statement**: Automate the annual water company comparative performance assessment for sewage treatment, reducing the assurance cycle from 6 months to 6 weeks while improving data quality and consistency, operational by PR29 data collection (2028).

**Success Metrics**:
- **Primary Metric**: Time from data submission to validated comparative assessment (target: 6 weeks, from 6 months)
- **Secondary Metrics**:
  - Industry assurance cost reduction (target: 60% reduction, GBP 24M saving)
  - Data quality rejection rate (target: < 2% of submissions, from current ~8%)

---

### Goal G-2: Real-Time Storm Overflow Dashboard

**Derived From Drivers**: SD-3, SD-4

**Goal Owner**: DEFRA Water Policy Director

**Goal Statement**: Publish real-time storm overflow discharge status for all 15,000+ overflows in England, with duration, frequency, and contextual data, accessible to the public through a web dashboard and open API, by December 2027.

**Success Metrics**:
- **Primary Metric**: Storm overflows with real-time status on public dashboard (target: 100%)
- **Secondary Metrics**:
  - Data latency from EDM to dashboard (target: < 1 hour)
  - Public dashboard availability (target: 99.9%)
  - Public satisfaction with information clarity (target: 65%+)

---

### Goal G-3: Environment Act Target Tracking

**Derived From Drivers**: SD-3

**Goal Owner**: DEFRA Water Policy Director

**Goal Statement**: Provide automated progress tracking against all Storm Overflow Discharge Reduction Plan targets, with Ministerial-ready reporting available on demand, by Q2 2027.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Ofwat CEO | SD-1 | Comparative performance assessment | G-1 | Automated assessment |
| Water Companies | SD-2 | Fair comparison methodology | G-1 | Automated assessment |
| DEFRA Policy Dir | SD-3 | Environment Act compliance | G-2 | Storm overflow dashboard |
| DEFRA Policy Dir | SD-3 | Environment Act compliance | G-3 | Target tracking |
| Public / CCW | SD-4 | Accountability and VfM | G-2 | Storm overflow dashboard |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Ofwat (SD-1) wants independent analytics free from company influence. Water Companies (SD-2) want input into methodology to ensure fair comparison.
  - **Resolution Strategy**: Open methodology consultation with published rationale for decisions. Companies can comment on methodology but Ofwat retains final determination authority. All methodology decisions published with reasoning.

- **Conflict 2**: Public/campaigners want simple performance comparisons. Water Companies want normalised, contextualised metrics.
  - **Resolution Strategy**: Publish both — headline comparative metrics for public accessibility, plus detailed normalised analysis for technical users. Methodology document published explaining the difference.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Water Industry Act 1991 | Legislation | legislation.gov.uk | Ofwat's regulatory powers | N/A — external reference |
| Environment Act 2021 | Legislation | legislation.gov.uk | Storm overflow monitoring and reduction duties | N/A — external reference |
| Storm Overflow Discharge Reduction Plan | Policy | GOV.UK | Legally binding reduction targets | N/A — external reference |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | SDG 6 governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wastewater Treatment Analytics (Project 003)
**AI Model**: Claude Opus 4.6 (1M context)
