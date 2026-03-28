# Stakeholder Drivers & Goals Analysis: Gender Pay Gap Reporting Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Gender Pay Gap Reporting Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Gender Pay Gap Reporting Programme, GEO |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GEO Programme Board, CDDO, EHRC Enforcement Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Gender Pay Gap Reporting Platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The platform will replace the existing GOV.UK gender pay gap reporting service with an automated collection and analytics capability that improves data quality, reduces employer burden, and enables richer analysis of the UK's gender pay gap.

### Key Findings

The strongest alignment exists around improving data quality and reducing employer reporting burden — GEO, EHRC, employers, and trade unions all benefit from a more streamlined, accurate reporting process. The most significant tension lies between the Minister's desire for richer, more granular data (e.g., ethnicity pay gap, disability pay gap) and employers' concern about increased reporting burden. EHRC's enforcement role creates a secondary tension: employers want a supportive, guidance-led approach while EHRC needs robust data to identify non-compliance for enforcement action.

### Critical Success Factors

- Achieve 100% reporting compliance rate from eligible employers by the statutory deadline (4 April annually)
- Reduce employer reporting errors by 50% through automated validation and pre-population from HMRC RTI data
- Deliver actionable analytics that enable GEO to identify sectoral and regional pay gap trends
- Maintain uninterrupted service during the peak reporting window (January-April)
- Pass GDS service assessment at Beta to maintain CDDO confidence

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for improved data quality and reduced employer burden. Tension between data richness ambitions (GEO, trade unions) and reporting burden concerns (employers, CBI). Additional complexity from EHRC's dual role as both guidance provider and enforcement body.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Women and Equalities | Ministerial sponsor | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ lines |
| GEO Director | Programme sponsor (GEO) | HIGH | HIGH | Manage Closely — Weekly programme board |
| SRO, Pay Gap Reporting | Programme accountability | HIGH | HIGH | Manage Closely — Programme governance |
| GEO Head of Pay Gap Policy | Policy ownership | HIGH | HIGH | Manage Closely — Policy-tech alignment |
| GEO Digital Lead | Technical delivery oversight | MEDIUM | HIGH | Keep Informed — Sprint reviews, architecture |
| GEO Statisticians | Data analysis and publication | MEDIUM | HIGH | Keep Informed — Data model, reporting design |
| GEO Communications | Media handling, publication | MEDIUM | MEDIUM | Keep Satisfied — Publication timeline |
| Cabinet Office CDDO | Spend control and assurance | HIGH | MEDIUM | Keep Satisfied — Spend approvals, assessments |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| EHRC Enforcement Team | EHRC | Enforcement partner | HIGH | HIGH |
| HMRC RTI Team | HMRC | Data source (Real Time Information) | HIGH | HIGH |
| Employer representatives (CBI) | CBI | Reporting obligation holders | MEDIUM | HIGH |
| Employer representatives (FSB) | FSB | SME reporting concerns | MEDIUM | HIGH |
| Trade unions (TUC) | TUC | Advocacy for transparency | MEDIUM | HIGH |
| Women's equality organisations | Fawcett Society, Close the Gap | Advocacy and scrutiny | LOW | HIGH |
| GDS Service Assessment | Cabinet Office | Service standard assurance | MEDIUM | MEDIUM |
| ONS | ONS | Statistical standards alignment | MEDIUM | MEDIUM |
| Large employers (>250 employees) | Private and public sector | Primary reporters | LOW | HIGH |
| Employees/citizens | Public | Data consumers | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns end-to-end service and employer outcomes | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap |
| Delivery Manager | Manages delivery cadence, risks, dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control, assessment gates |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Information Risk Owner (SIRO) | Information risk ownership, DPIA sign-off | HIGH / MEDIUM | Keep Satisfied — Risk acceptance, DPIA |
| Departmental Security Officer (DSO) | Security policy implementation | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed — Architecture reviews, pen testing |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * Minister for     |
        |  * SIRO             |    Women & Equalities|
        |  * DSO              |  * GEO Director     |
        |  * GEO Comms        |  * SRO              |
 P      |                     |  * GEO Head of Policy|
 O      |                     |  * EHRC Enforcement |
 W      |                     |  * HMRC RTI         |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * ONS              |  * Employers (CBI)  |
        |                     |  * FSB (SMEs)       |
        |                     |  * TUC              |
        |                     |  * Fawcett Society  |
        |                     |  * GEO Digital Lead |
        |                     |  * GEO Statisticians|
        |                     |  * Large employers  |
        |                     |  * Employees/citizens|
        |                     |  * GDS Assessment   |
        +---------------------+---------------------+
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Minister for Women and Equalities | HIGH | HIGH | Manage Closely | Ministerial briefings, PQ preparation |
| GEO Director | HIGH | HIGH | Manage Closely | Weekly programme board |
| SRO | HIGH | HIGH | Manage Closely | Programme governance, decision escalation |
| GEO Head of Pay Gap Policy | HIGH | HIGH | Manage Closely | Policy-tech alignment sessions |
| EHRC Enforcement Team | HIGH | HIGH | Manage Closely | Joint enforcement data requirements |
| HMRC RTI Team | HIGH | HIGH | Manage Closely | Data feed governance, integration design |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control, service assessment |
| SIRO | HIGH | MEDIUM | Keep Satisfied | DPIA sign-off, risk acceptance |
| Employers (CBI/FSB) | MEDIUM | HIGH | Keep Informed | Employer consultation, user research |
| TUC | MEDIUM | HIGH | Keep Informed | Transparency advocacy, data access |
| Large employers | LOW | HIGH | Keep Informed | Reporting guidance, user testing |
| Employees/citizens | LOW | HIGH | Keep Informed | Published data, accessibility |
| GEO Statisticians | MEDIUM | HIGH | Keep Informed | Data model, analytics design |
| ONS | MEDIUM | MEDIUM | Monitor | Statistical standards alignment |

---

## Stakeholder Drivers Analysis

### SD-1: Minister for Women and Equalities — Demonstrable Progress on Gender Pay Gap Closure

**Stakeholder**: Minister for Women and Equalities

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver a modernised pay gap reporting platform that demonstrates government commitment to closing the gender pay gap, enabling the Minister to point to improved data quality, higher compliance rates, and actionable insights in parliamentary debates and media.

**Context & Background**:
The gender pay gap has been a persistent political issue since mandatory reporting was introduced in 2017. The UK's median gender pay gap stood at 14.3% in 2023 (ONS). The Minister faces regular parliamentary questions, media scrutiny from organisations like the Fawcett Society, and international scrutiny through UN SDG 5 reporting. The current GOV.UK service has limited analytics capability and no automated data validation, undermining the credibility of published data.

**Driver Intensity**: CRITICAL

**Enablers**:

- Modern analytics platform enabling trend analysis and sectoral comparison
- Improved compliance rates providing more complete data for policy decisions
- Integration with HMRC RTI to validate employer submissions

**Blockers**:

- Employer resistance to additional reporting burden
- Treasury constraints on GEO digital spending
- EHRC capacity to enforce against non-compliant employers

**Related Stakeholders**: GEO Director, EHRC, TUC, Fawcett Society

---

### SD-2: EHRC Enforcement Team — Robust Data for Compliance Enforcement

**Stakeholder**: EHRC Enforcement Team

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Obtain timely, validated employer pay gap data that enables identification of non-compliant employers and supports enforcement action under Section 78 of the Equality Act 2010, reducing the manual effort required to identify and pursue non-reporters.

**Context & Background**:
EHRC is responsible for enforcing gender pay gap reporting obligations under the Equality Act 2010. Currently, identifying non-compliant employers requires manual cross-referencing of submissions against Companies House data. The lack of automated validation means many submissions contain errors that undermine enforcement credibility. EHRC has limited resources and must prioritise enforcement actions — better data enables more targeted use of their powers.

**Driver Intensity**: HIGH

**Enablers**:

- Automated compliance checking against Companies House employer registry
- Real-time dashboards showing submission status and compliance rates
- Data quality validation at point of submission reducing post-hoc error correction

**Blockers**:

- Legal complexity around EHRC access to pre-publication employer data
- Employer concerns about enforcement being prioritised over guidance
- Resource constraints within EHRC for digital engagement

**Related Stakeholders**: GEO Head of Policy, large employers, CBI

---

### SD-3: Employers (CBI/FSB) — Reduced Reporting Burden

**Stakeholder**: Employer representative bodies (CBI, FSB)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Minimise the time and cost employers spend on gender pay gap reporting by pre-populating data from existing HMRC submissions, simplifying the calculation methodology, and providing clear, actionable guidance integrated into the reporting workflow.

**Context & Background**:
Employers report that the current process is burdensome, requiring manual data extraction, complex calculations (particularly around bonus pay and part-time workers), and a separate submission process. The CBI estimates that large employers spend an average of 40 staff-hours per annual submission. The FSB raises concerns about extending reporting to smaller employers. Errors are common because the calculation methodology is genuinely complex.

**Driver Intensity**: HIGH

**Enablers**:

- Pre-population of pay data from HMRC RTI reducing manual data entry
- Built-in calculation engine eliminating manual spreadsheet work
- Contextual guidance at each step of the reporting journey
- API for employers with payroll systems to submit programmatically

**Blockers**:

- HMRC data may not map perfectly to pay gap calculation requirements
- Employer payroll systems vary enormously in capability
- Resistance from employers to any expansion of reporting scope

**Related Stakeholders**: HMRC RTI Team, large employers, FSB, Minister

---

### SD-4: TUC and Women's Equality Organisations — Greater Transparency and Accountability

**Stakeholder**: TUC, Fawcett Society, Close the Gap

**Driver Category**: STRATEGIC / ADVOCACY

**Driver Statement**: Ensure the platform publishes detailed, accessible, and comparable pay gap data that enables workers, unions, and equality organisations to hold employers accountable, with enhanced reporting requirements covering ethnicity, disability, and action plan obligations.

**Context & Background**:
Trade unions and equality organisations have consistently argued that the current reporting regime is insufficient — employers report headline figures without context, there is no requirement to publish action plans, and enforcement against non-reporters is perceived as weak. The TUC has called for mandatory action plans, ethnicity pay gap reporting, and lower thresholds for employer size. The Fawcett Society publishes annual analysis showing slow progress on pay gap closure.

**Driver Intensity**: HIGH

**Enablers**:

- Open data APIs enabling independent analysis of employer data
- Enhanced analytics showing sectoral and regional trends
- Platform capability to accommodate future mandatory action plan requirements

**Blockers**:

- Legislative change required for mandatory action plans (not in platform scope)
- Employer resistance to additional disclosure
- Tension between transparency and employer engagement

**Related Stakeholders**: Minister, EHRC, employers, employees/citizens

---

### SD-5: HMRC RTI Team — Controlled, Standardised Data Integration

**Stakeholder**: HMRC Real Time Information Team

**Driver Category**: OPERATIONAL / TECHNICAL

**Driver Statement**: Provide a controlled, secure, and well-governed data feed from RTI payroll data to the pay gap platform, ensuring that HMRC data is used only for its stated purpose, data quality responsibilities are clearly delineated, and integration does not create additional operational burden on HMRC systems.

**Context & Background**:
HMRC RTI processes approximately 50 million employment records monthly. Providing a data feed to GEO requires a formal data sharing agreement under the Digital Economy Act 2017, a defined API specification, and clear data quality responsibilities. HMRC is protective of RTI data integrity and wary of creating dependencies that increase operational risk to a critical national tax system.

**Driver Intensity**: MEDIUM

**Enablers**:

- Well-defined API specification with clear data ownership and quality responsibilities
- Formal data sharing agreement with legal basis under Digital Economy Act 2017
- Minimal impact on HMRC RTI operational systems (read-only, batch or near-real-time)

**Blockers**:

- HMRC RTI data model may not align perfectly with pay gap calculation requirements
- HMRC governance processes for new data sharing arrangements are lengthy
- Risk of HMRC being blamed for data quality issues that arise from the mapping

**Related Stakeholders**: GEO Digital Lead, employers, CDDO

---

### SD-6: GEO Statisticians — Rigorous, Publishable Analytics

**Stakeholder**: GEO Statistical Team

**Driver Category**: OPERATIONAL / PROFESSIONAL

**Driver Statement**: Access validated, clean employer pay gap data through a modern analytics environment that enables the production of National Statistics-quality publications, trend analysis, and policy-relevant research without requiring manual data cleaning.

**Context & Background**:
GEO statisticians currently spend significant effort cleaning submitted data before it can be used for official publications. Data quality issues include incorrect calculations, missing fields, and outlier values that suggest errors. The current system provides limited analytical capability, requiring data exports to separate statistical tools. GEO aspires to Code of Practice for Statistics compliance for its pay gap publications.

**Driver Intensity**: MEDIUM

**Enablers**:

- Automated validation at point of submission reducing post-hoc cleaning
- Built-in analytics environment with statistical tools
- Data model designed for time-series analysis and cohort comparison

**Blockers**:

- Tension between automated rejection of submissions and employer experience
- Statistical disclosure control requirements for small employer cohorts
- Resource constraints for analytical tool development

**Related Stakeholders**: ONS, GEO Head of Policy, Minister

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 100% Employer Compliance Rate

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: EHRC Enforcement Team (enforcement); GEO Head of Policy (enablement)

**Goal Statement**: Achieve 100% reporting compliance from all eligible employers (those with 250+ employees) by the statutory deadline of 4 April each year, measured against the Companies House register of eligible employers.

**Why This Matters**: Non-compliance undermines the integrity of the entire dataset and the Minister's ability to make policy claims based on the data. Currently approximately 10% of eligible employers fail to report by the deadline.

**Success Metrics**:

- **Primary Metric**: Percentage of eligible employers who submit by 4 April
- **Secondary Metrics**:
  - Number of employers requiring EHRC enforcement action
  - Average submission date (earlier = better)

**Baseline**: ~90% compliance by deadline (2024/25)

**Target**: 100% compliance by deadline

**Measurement Method**: Automated comparison of submissions received against Companies House register of eligible employers

---

### Goal G-2: Reduce Employer Reporting Effort by 60%

**Derived From Drivers**: SD-3, SD-5

**Goal Owner**: GEO Digital Lead

**Goal Statement**: Reduce the average time employers spend on pay gap reporting from 40 staff-hours to 16 staff-hours per submission through pre-population, automated calculations, and integrated guidance.

**Why This Matters**: Reducing burden makes compliance easier, reduces errors, and builds goodwill with employer community — essential for any future expansion of reporting requirements.

**Success Metrics**:

- **Primary Metric**: Average employer-reported time to complete submission
- **Secondary Metrics**:
  - Percentage of employers using pre-populated data
  - Submission error rate

**Baseline**: 40 staff-hours average per submission

**Target**: 16 staff-hours average (60% reduction)

**Measurement Method**: Post-submission survey; analytics on time-to-complete within the platform

---

### Goal G-3: Improve Data Quality to National Statistics Standard

**Derived From Drivers**: SD-1, SD-6

**Goal Owner**: GEO Head of Statistics

**Goal Statement**: Achieve data quality sufficient for Code of Practice for Statistics designation of pay gap publications, with automated validation catching 95% of calculation errors at point of submission.

**Why This Matters**: Statistical credibility underpins the policy value of the data. Currently, data quality issues undermine confidence in published figures and require extensive post-hoc cleaning.

**Success Metrics**:

- **Primary Metric**: Percentage of submissions passing automated validation without manual correction
- **Secondary Metrics**:
  - Number of data quality issues identified post-publication
  - GEO statistician hours spent on data cleaning

**Baseline**: ~70% of submissions require some form of data correction

**Target**: 95% of submissions pass validation on first or second attempt

**Measurement Method**: Platform validation logs; statistician time-tracking

---

### Goal G-4: Enable Actionable Pay Gap Analytics

**Derived From Drivers**: SD-1, SD-4, SD-6

**Goal Owner**: GEO Head of Pay Gap Policy

**Goal Statement**: Deliver an analytics capability that enables GEO, EHRC, and the public to analyse pay gap data by sector, region, employer size, and over time, with open data APIs enabling independent analysis.

**Why This Matters**: Without actionable analytics, pay gap data is a compliance exercise rather than a policy tool. The Minister needs trend data to demonstrate progress; equality organisations need granular data for accountability.

**Success Metrics**:

- **Primary Metric**: Number of distinct analytics queries served per month
- **Secondary Metrics**:
  - Open data API usage (unique consumers)
  - Media citations of platform analytics

**Baseline**: No integrated analytics (data exported to spreadsheets)

**Target**: Self-service analytics dashboard with 10+ pre-built views; open API with 50+ registered consumers within 12 months

**Measurement Method**: Platform analytics; API usage tracking; media monitoring

---

## Goal-to-Outcome Mapping

### Outcome O-1: Improved Gender Pay Gap Policy Evidence Base

**Supported Goals**: G-1, G-3, G-4

**Outcome Statement**: GEO has a complete, validated, analytically-rich dataset enabling evidence-based policy development on gender pay gap closure, measured by the quality and impact of GEO publications and policy recommendations.

**Measurement Details**:

- **KPI**: Code of Practice for Statistics compliance achieved for annual publication
- **Current Value**: Not assessed
- **Target Value**: Full compliance within 24 months
- **Measurement Frequency**: Annual (aligned with statistical publication cycle)
- **Data Source**: UK Statistics Authority assessment
- **Report Owner**: GEO Head of Statistics

**Business Value**:

- **Strategic Impact**: Strengthened evidence base for Ministerial policy decisions on gender equality
- **Operational Impact**: 60% reduction in statistician time spent on data cleaning
- **Customer Impact**: Higher quality published data increasing public and media trust

**Timeline**:

- **Phase 1 (Months 1-6)**: Platform live, first reporting cycle with automated validation
- **Phase 2 (Months 7-12)**: Analytics dashboard operational, open data API launched
- **Phase 3 (Months 13-24)**: Second reporting cycle with trend analysis, Code of Practice assessment

---

### Outcome O-2: Employer Compliance and Engagement

**Supported Goals**: G-1, G-2

**Outcome Statement**: Employers find reporting easier and more valuable, measured by compliance rates, time-to-complete, and employer satisfaction scores.

**Measurement Details**:

- **KPI**: Employer satisfaction score with reporting process
- **Current Value**: Not systematically measured (anecdotal dissatisfaction)
- **Target Value**: 70% employer satisfaction within 12 months
- **Measurement Frequency**: Annual (post-reporting-cycle survey)
- **Data Source**: Employer survey
- **Report Owner**: GEO Digital Lead

---

## Complete Traceability Matrix

### Stakeholder -> Driver -> Goal -> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Progress on pay gap closure | G-1 | 100% compliance | O-1 | Policy evidence base |
| Minister | SD-1 | Progress on pay gap closure | G-4 | Actionable analytics | O-1 | Policy evidence base |
| EHRC | SD-2 | Enforcement data | G-1 | 100% compliance | O-2 | Employer compliance |
| Employers | SD-3 | Reduced burden | G-2 | 60% effort reduction | O-2 | Employer compliance |
| TUC/Fawcett | SD-4 | Transparency | G-4 | Actionable analytics | O-1 | Policy evidence base |
| HMRC RTI | SD-5 | Controlled integration | G-2 | 60% effort reduction | O-2 | Employer compliance |
| GEO Stats | SD-6 | Publishable analytics | G-3 | National Stats quality | O-1 | Policy evidence base |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: TUC/Fawcett (SD-4) want expanded reporting (action plans, ethnicity) but Employers (SD-3) want reduced burden
  - **Resolution Strategy**: Phase approach — deliver burden reduction first (pre-population, automated calculations) to build goodwill, then consult on expanded reporting for future phases. Platform architecture designed to accommodate future requirements without current mandate.

- **Conflict 2**: EHRC (SD-2) wants robust enforcement data but Employers (SD-3) want a supportive, guidance-led experience
  - **Resolution Strategy**: Separate enforcement data pipeline from employer-facing experience. Employers see guidance and support; EHRC receives compliance data through a separate secure channel. Platform design separates guidance layer from compliance monitoring.

**Synergies**:

- **Synergy 1**: Minister (SD-1) and GEO Stats (SD-6) both benefit from improved data quality — achieving G-3 satisfies both
- **Synergy 2**: Employers (SD-3) and HMRC (SD-5) both benefit from pre-population — reducing employer effort while using existing validated HMRC data

---

## Communication & Engagement Plan

### Minister for Women and Equalities

**Primary Message**: The new platform will deliver higher compliance rates, better data quality, and actionable analytics that strengthen the evidence base for pay gap policy.

**Key Talking Points**:

- Pre-population from HMRC data will reduce employer burden and increase compliance
- Built-in analytics will enable trend analysis for the first time
- Platform is designed to accommodate future reporting expansion (ethnicity, action plans)

**Communication Frequency**: Monthly (more frequently during reporting window)

**Preferred Channel**: Ministerial briefings, written submissions

### Employers (CBI/FSB)

**Primary Message**: The new platform will significantly reduce your reporting burden through automated calculations and HMRC data pre-population — making compliance easier than ever.

**Key Talking Points**:

- 60% reduction in time to complete reporting
- Built-in calculation engine eliminates spreadsheet errors
- API available for employers who want to automate submissions from payroll systems

**Communication Frequency**: Quarterly; intensified during reporting window

**Preferred Channel**: Employer forums, CBI/FSB engagement, GOV.UK guidance

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Employers | Manual data extraction, spreadsheet calculations, GOV.UK form | Pre-populated data, automated calculations, guided submission | MEDIUM | LOW | Reduced burden = positive change |
| EHRC | Manual cross-referencing for enforcement | Automated compliance dashboards | MEDIUM | LOW | Reduces enforcement effort |
| GEO Statisticians | Manual data cleaning, spreadsheet analysis | Validated data, integrated analytics | HIGH | LOW | Significant improvement to workflow |
| HMRC RTI | No data sharing with GEO | New data feed to GEO platform | MEDIUM | MEDIUM | Clear DSA, minimal operational impact |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: HMRC Data Sharing Agreement Delays

**Related Stakeholders**: HMRC RTI Team, GEO Digital Lead, Employers

**Risk Description**: The data sharing agreement under the Digital Economy Act 2017 may take longer than planned, delaying the pre-population feature that is critical to employer burden reduction.

**Impact on Goals**: G-2 (effort reduction) significantly impacted; G-3 (data quality) partially impacted

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Early engagement with HMRC data governance; parallel workstream for manual submission fallback; Ministerial escalation path if DSA delayed beyond 6 months

**Contingency Plan**: Platform launches with manual submission capability; pre-population added as enhancement once DSA is in place

---

### Risk R-2: Employer Resistance to Changed Process

**Related Stakeholders**: CBI, FSB, large employers

**Risk Description**: Employers may resist changes to their established reporting processes, particularly if the pre-populated data does not match their own calculations, creating confusion and complaints.

**Impact on Goals**: G-1 (compliance), G-2 (effort reduction)

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Extensive employer user research during Discovery/Alpha; employer pilot programme with 50 diverse employers; clear override mechanism allowing employers to correct pre-populated data

**Contingency Plan**: Enhanced guidance and support during first reporting cycle; dedicated helpline for pre-population queries

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | GEO Finance | SRO | CDDO | All stakeholders |
| Policy requirements | GEO Head of Policy | Minister | EHRC, employers | TUC, Fawcett |
| Technical architecture | GEO Digital Lead | SRO | CDDO, HMRC | GEO Stats |
| HMRC data sharing | GEO Data Lead | SRO | HMRC RTI, SIRO | CDDO |
| Go/no-go for go-live | SRO | Minister (via submission) | All | All |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: SRO / GEO Director (scope, timeline, budget variances)
3. **Level 3**: Minister for Women and Equalities (strategic direction, cross-departmental issues)

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| SRO, Pay Gap Reporting | | | |
| GEO Director | | | |
| GEO Head of Pay Gap Policy | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Equality Act 2010 (Section 78) | Legislation | legislation.gov.uk | Pay gap reporting obligation | N/A — external |
| Equality Act 2010 (Specific Duties) Regulations 2017 | Legislation | legislation.gov.uk | Calculation methodology, deadlines | N/A — external |
| ACAS Gender Pay Gap Guidance | Guidance | ACAS | Calculation methodology details | N/A — external |
| Digital Economy Act 2017 | Legislation | legislation.gov.uk | Data sharing legal basis | N/A — external |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Gender Pay Gap Reporting Platform (Project 001)
**Model**: Claude Opus 4.6
