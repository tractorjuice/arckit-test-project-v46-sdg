# Stakeholder Drivers & Goals Analysis: School Performance Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | School Performance Analytics (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, School Performance Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SPA Programme Board, Ofsted Digital, DfE Analysis Directorate |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the School Performance Analytics (SPA) platform, their underlying drivers, and how these drivers translate into measurable goals and outcomes. The SPA will provide Ofsted inspectors, DfE analysts, and Regional Directors with a unified data platform for school inspection preparation, performance monitoring, and risk-based targeting.

### Key Findings

The SPA programme must navigate a fundamental tension between Ofsted's need for comprehensive, timely data to support fair and consistent inspections and the education sector's deep suspicion that data-driven inspection targeting creates perverse incentives and gaming behaviour. Headteachers and unions fear that automated data analysis will replace nuanced professional judgement. Simultaneously, Ofsted inspectors report spending 40% of pre-inspection preparation time manually collating data from disparate sources — time that should be spent on professional analysis.

### Critical Success Factors

- Reduce inspector pre-inspection data preparation time by 60% through automated data consolidation
- Maintain data quality with 99.5% accuracy against source systems (National Pupil Database, school census)
- Achieve acceptance from HM Chief Inspector that the platform enhances — not replaces — professional judgement
- Ensure data sharing complies with the Ofsted-DfE data sharing agreement and UK GDPR
- Pass GDS service assessment at Beta

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for better data tooling within Ofsted, but significant tensions between data-driven inspection targeting (Ofsted leadership) and sector fears about algorithmic judgement (headteachers, unions). DfE Analysis Directorate strongly supportive but sensitive to data governance boundaries.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| HM Chief Inspector | Ofsted Leadership | HIGH | HIGH | Manage Closely — Strategic direction, public messaging |
| Ofsted National Director (Schools) | Inspection Operations | HIGH | HIGH | Manage Closely — Inspection workflow integration |
| SRO, SPA Programme | Programme Sponsor (Ofsted) | HIGH | HIGH | Manage Closely — Weekly programme board |
| Ofsted Chief Operating Officer | Operational delivery | HIGH | HIGH | Manage Closely — Resource allocation, IT infrastructure |
| Ofsted Lead Inspectors | Inspection team leads | MEDIUM | HIGH | Keep Informed — User research, workflow design |
| Ofsted Data Analytics Team | Existing analytics capability | MEDIUM | HIGH | Keep Informed — Data pipeline design, QA |
| Ofsted SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, data sharing agreements |
| DfE Analysis Directorate | Data supplier (NPD, school census) | HIGH | HIGH | Manage Closely — Data access, quality, timeliness |
| DfE Regional Directors | Regional school oversight | MEDIUM | HIGH | Keep Informed — Regional performance dashboards |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| ICO | Regulator | Data protection oversight | HIGH | MEDIUM |
| Headteachers / Principals | Schools | Inspection subjects | MEDIUM | HIGH |
| Multi-Academy Trust CEOs | MATs | Strategic accountability | HIGH | HIGH |
| Teaching Unions (NEU, NASUWT, ASCL, NAHT) | Unions | Inspection fairness, workload | MEDIUM | HIGH |
| Exam Boards (AQA, OCR, Edexcel, WJEC) | Assessment providers | Results data supply | MEDIUM | MEDIUM |
| Parents and Carers | Citizens | School choice, transparency | LOW | HIGH |
| Education Select Committee | Parliament | Scrutiny of Ofsted methods | HIGH | MEDIUM |
| School governors | Governance | Accountability data | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * HM Chief Insp.   |
        |  * ICO              |  * National Dir.    |
        |  * Ofsted SIRO      |  * SRO              |
        |  * Education Select |  * COO (Ofsted)     |
        |    Committee         |  * DfE Analysis Dir.|
 P      |                     |  * MAT CEOs         |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * Exam Boards      |  * Headteachers     |
        |                     |  * Lead Inspectors  |
        |                     |  * Teaching Unions   |
        |                     |  * Parents/Carers   |
        |                     |  * Regional Dirs    |
        |                     |  * School governors |
        |                     |  * Data Analytics   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: HM Chief Inspector — Evidence-Based, Consistent Inspection

**Stakeholder**: HM Chief Inspector of Education, Children's Services and Skills

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Ensure that Ofsted inspections are underpinned by comprehensive, accurate, and timely data, enabling consistent professional judgements across all regions and inspection teams, and demonstrating to Parliament and the public that inspection is evidence-based, fair, and proportionate.

**Context & Background**: Ofsted faces sustained public and parliamentary scrutiny of inspection consistency. Different inspectors examining similar schools may reach different judgements partly because they access and interpret data differently during pre-inspection preparation. The HM Chief Inspector needs a platform that provides every inspector with the same data foundation, ensuring consistency while preserving professional judgement.

**Driver Intensity**: CRITICAL

**Enablers**:

- Political support for data-informed inspection
- Existing Ofsted data analytics capability that can be scaled
- DfE Analysis Directorate willingness to improve data feeds

**Blockers**:

- Sector perception that data-driven targeting is "algorithmic inspection"
- Legacy IT infrastructure within Ofsted constraining modernisation
- Data quality issues in source systems (particularly school census submissions)

---

### SD-2: Ofsted Lead Inspectors — Reduce Pre-Inspection Data Preparation

**Stakeholder**: Ofsted Lead Inspectors (approximately 250 HMI and OIs)

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Reduce the time spent manually collating school performance data from multiple sources before each inspection, enabling more time for professional analysis and preparation of key lines of enquiry.

**Context & Background**: Lead inspectors currently spend an estimated 6-8 hours per inspection manually downloading and cross-referencing data from IDSR (Ofsted's Inspection Data Summary Report), ASP (Analyse School Performance), school census data, attendance data, exclusion data, financial benchmarking data, and safeguarding referral data. This is inefficient, error-prone, and leaves insufficient time for professional analysis.

**Driver Intensity**: HIGH

---

### SD-3: DfE Analysis Directorate — Unified Data Platform

**Stakeholder**: DfE Analysis Directorate

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Create a unified analytical platform that consolidates education performance data from multiple DfE sources, reducing duplication and enabling consistent analysis for both DfE internal use and Ofsted inspection support.

**Context & Background**: DfE maintains multiple overlapping data systems — the National Pupil Database, Analyse School Performance (ASP), the school census collection system, IDSR, and various ad hoc analytical tools. These systems are maintained by different teams with inconsistent data models and update cycles. A unified platform would reduce maintenance overhead and improve data consistency.

**Driver Intensity**: HIGH

---

### SD-4: Headteachers — Fairness, Transparency, and No Algorithmic Judgement

**Stakeholder**: Headteachers and Principals

**Driver Category**: RISK / PERSONAL

**Driver Statement**: Ensure that any data analytics platform used by Ofsted enhances fair, nuanced professional judgement rather than replacing it with algorithmic school ratings, and that schools have visibility of the same data Ofsted uses.

**Context & Background**: The education sector has deep concerns about data-driven inspection. Historical controversies include RAISEonline (perceived as reducing schools to spreadsheet judgements), Ofsted's risk-based inspection targeting (perceived as penalising schools with volatile demographics), and the recent debates about "coasting schools" metrics. Headteachers want assurance that the platform will support, not replace, professional inspection.

**Driver Intensity**: CRITICAL

---

### SD-5: Teaching Unions — Inspection Workload and Accountability Culture

**Stakeholder**: Teaching Unions (NEU, NASUWT, ASCL, NAHT)

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure that the analytics platform does not increase the data burden on schools, does not create new accountability metrics, and supports a culture of school improvement rather than punitive judgement.

**Driver Intensity**: HIGH

---

### SD-6: Parents and Carers — Transparent School Performance Information

**Stakeholder**: Parents and Carers

**Driver Category**: CUSTOMER

**Driver Statement**: Access clear, understandable information about school performance that helps inform school choice and understand the quality of education their child receives.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Inspector Pre-Inspection Preparation by 60%

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: Ofsted National Director (Schools)

**Goal Statement**: Reduce the average time Ofsted lead inspectors spend on pre-inspection data preparation from 7 hours to under 3 hours per inspection by consolidating all data sources into a single dashboard.

**Success Metrics**:

- **Primary Metric**: Average hours spent on pre-inspection data preparation (inspector self-report and time tracking)
- **Secondary Metrics**: Inspector satisfaction with data quality and completeness; error rate in pre-inspection data packs

**Baseline**: 7 hours per inspection
**Target**: 3 hours per inspection (57% reduction)

---

### Goal G-2: Achieve 99.5% Data Accuracy Against Source Systems

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: Ofsted Data Analytics Team Lead

**Goal Statement**: Ensure that all data displayed on the SPA platform matches source system values with 99.5% accuracy, verified through automated reconciliation.

**Success Metrics**:

- **Primary Metric**: Data accuracy rate (automated reconciliation against NPD, school census, examination results)
- **Secondary Metrics**: Mean time to detect and resolve data discrepancies; number of inspector-reported data errors per term

**Baseline**: Current IDSR accuracy approximately 97% (manual reconciliation)
**Target**: 99.5% accuracy with automated reconciliation within 24 hours

---

### Goal G-3: Provide Schools with Same Data View as Inspectors

**Derived From Drivers**: SD-4, SD-5

**Goal Owner**: SRO

**Goal Statement**: Provide headteachers with access to the same school-level data dashboard that inspectors use, ensuring transparency and enabling self-evaluation using consistent data.

**Success Metrics**:

- **Primary Metric**: Percentage of schools accessing their data dashboard at least once per term
- **Secondary Metrics**: Headteacher satisfaction with data transparency; reduction in FOI requests for inspection data

**Baseline**: Schools currently access ASP (separate system, different data presentation)
**Target**: 80% of schools accessing their SPA dashboard at least termly within 12 months

---

### Goal G-4: Consolidate 6 Data Sources into Single Platform

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: DfE Analysis Directorate

**Goal Statement**: Consolidate data from IDSR, ASP, school census, attendance data, exclusion data, and financial benchmarking into a single analytical platform within 18 months.

**Success Metrics**:

- **Primary Metric**: Number of legacy data systems decommissioned
- **Secondary Metrics**: Data pipeline uptime; time from source data update to SPA availability

**Baseline**: 6 separate data systems with manual integration
**Target**: 1 unified platform with automated data pipelines

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| HM Chief Inspector | SD-1 | Consistent, evidence-based inspection | G-1 | 60% prep time reduction | O-1 | More consistent inspections |
| HM Chief Inspector | SD-1 | Consistent, evidence-based inspection | G-2 | 99.5% data accuracy | O-1 | More consistent inspections |
| Lead Inspectors | SD-2 | Reduce prep workload | G-1 | 60% prep time reduction | O-2 | Inspector efficiency |
| DfE Analysis Dir. | SD-3 | Unified data platform | G-4 | Consolidate 6 sources | O-3 | Reduced system duplication |
| Headteachers | SD-4 | Fairness and transparency | G-3 | Same data view as inspectors | O-1 | More consistent inspections |
| Teaching Unions | SD-5 | No new accountability burden | G-3 | Same data view as inspectors | O-1 | More consistent inspections |
| Parents | SD-6 | Transparent performance info | G-3 | Same data view as inspectors | O-4 | Better school choice info |

### Conflict Analysis

- **Conflict 1**: Ofsted leadership (SD-1) wants risk-based targeting using predictive analytics, but headteachers (SD-4) and unions (SD-5) oppose algorithmic school selection for inspection
  - **Resolution Strategy**: Compromise — use data to inform, not determine, inspection targeting. Predictive models flag schools for human review; final targeting decisions made by Regional Directors with professional judgement documented. Model methodology published for transparency.

- **Conflict 2**: DfE Analysis Directorate (SD-3) wants broad data sharing for analytical purposes, but Ofsted SIRO needs strict data minimisation and purpose limitation under UK GDPR
  - **Resolution Strategy**: Phase — establish data sharing agreement with specific, documented purposes. Analysis Directorate access limited to aggregated/anonymised data unless specific lawful basis for pupil-level data.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Data sharing agreements | Ofsted SIRO | HM Chief Inspector | ICO, DfE SIRO | All |
| Inspection workflow changes | National Director | HM Chief Inspector | Lead Inspectors, Unions | Schools |
| Platform architecture | Ofsted COO | SRO | CDDO, DfE Analysis Dir. | All |
| School-facing dashboard design | SRO | HM Chief Inspector | Headteachers, Governors | Parents |
| Go/No-go for live | SRO | HM Chief Inspector | All | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Education Inspection Framework | Framework | Ofsted | Inspection methodology | N/A — external reference |
| Ofsted-DfE Data Sharing Agreement | Agreement | Ofsted/DfE | Data sharing lawful basis | N/A — external reference |
| Analyse School Performance | Platform | DfE | Current school performance tool | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: School Performance Analytics
**Model**: Claude Opus 4.6
