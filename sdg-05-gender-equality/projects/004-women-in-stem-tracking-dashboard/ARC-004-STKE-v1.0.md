# Stakeholder Drivers & Goals Analysis: Women in STEM Tracking Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Women in STEM Tracking Dashboard (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Women in STEM Programme, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Programme Board, UKRI, Royal Society, Royal Academy of Engineering |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Women in STEM Tracking Dashboard, a platform that will track gender diversity across science, technology, engineering, and mathematics (STEM) sectors in the UK — from education pipeline through to senior leadership — providing the evidence base for policy interventions aimed at increasing women's participation in STEM.

### Key Findings

The strongest alignment exists around the need for better data on the STEM gender pipeline — DSIT, UKRI, learned societies, and industry all recognise that current data is fragmented, inconsistent, and published with significant time lag. The primary tension lies between researchers' desire for granular, individual-level data (essential for tracking career progression and attrition points) and data protection requirements that limit longitudinal tracking of individuals. A secondary tension exists between industry (which wants benchmarking data to demonstrate progress) and advocacy groups (which want accountability data to highlight failures).

### Critical Success Factors

- Dashboard provides a single authoritative source of STEM gender diversity data, replacing multiple inconsistent reports
- Data pipeline covers the full STEM journey: GCSE/A-level take-up, undergraduate/postgraduate enrolment, research funding, academic positions, industry workforce, and senior leadership
- Data published with no more than 6-month lag (current lag is 12-24 months for some sources)
- Intersectional analysis available (gender crossed with ethnicity, disability, socio-economic background)
- Dashboard cited by government, industry, and media as the definitive reference for STEM diversity

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Strong consensus that better STEM diversity data is needed. Moderate tension around data granularity vs privacy, and between benchmarking (positive framing) vs accountability (challenging framing).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for DSIT | Ministerial sponsor | HIGH | MEDIUM | Keep Satisfied — Ministerial briefings |
| DSIT Chief Scientific Adviser | Scientific leadership | HIGH | HIGH | Manage Closely — Strategic oversight |
| SRO, Women in STEM | Programme accountability | HIGH | HIGH | Manage Closely — Programme governance |
| DSIT Diversity and Inclusion Team | Policy ownership | MEDIUM | HIGH | Keep Informed — Policy requirements |
| DSIT Digital | Technical delivery | MEDIUM | HIGH | Keep Informed — Architecture, sprints |
| DSIT Analysis and Data | Statistical requirements | MEDIUM | HIGH | Keep Informed — Data standards |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| UKRI (UK Research and Innovation) | Research funder | Major data source | HIGH | HIGH |
| HESA (Higher Education Statistics Agency) | Statistics body | HE data source | HIGH | HIGH |
| Royal Society | Learned society | Research and advocacy | MEDIUM | HIGH |
| Royal Academy of Engineering | Learned society | Engineering focus | MEDIUM | HIGH |
| WISE Campaign | Charity | Women in STEM advocacy | LOW | HIGH |
| STEM Women | Organisation | Career platform for women in STEM | LOW | HIGH |
| BCS (The Chartered Institute for IT) | Professional body | Technology workforce data | LOW | HIGH |
| IET (Institution of Engineering and Technology) | Professional body | Engineering workforce data | LOW | HIGH |
| DfE (Department for Education) | Government | Education pipeline data | MEDIUM | MEDIUM |
| CBI / Tech UK | Industry bodies | Industry workforce data | MEDIUM | MEDIUM |
| ONS | Statistics body | Labour Force Survey, statistical standards | HIGH | MEDIUM |
| Universities (Russell Group) | HE sector | Institutional-level data | LOW | HIGH |
| Industry employers (FTSE 350) | Private sector | Workforce diversity data | LOW | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * Secretary of     |  * DSIT Chief Sci   |
        |    State (DSIT)     |    Adviser          |
        |  * ONS              |  * SRO              |
        |                     |  * UKRI             |
 P      |                     |  * HESA             |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |  * Industry         |  * Royal Society    |
        |    employers        |  * RAEng            |
        |                     |  * WISE Campaign    |
        |                     |  * DfE              |
        |                     |  * CBI/TechUK       |
        |                     |  * BCS / IET        |
        |                     |  * STEM Women       |
        |                     |  * Universities     |
        |                     |  * DSIT D&I Team    |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DSIT Chief Scientific Adviser — Evidence-Based STEM Diversity Policy

**Stakeholder**: DSIT Chief Scientific Adviser

**Driver Category**: STRATEGIC / POLICY

**Driver Statement**: Provide the government's Chief Scientific Adviser with a reliable, timely, and comprehensive evidence base on gender diversity in STEM, enabling targeted policy interventions at the specific pipeline stages where women are being lost — from education through to senior leadership.

**Context & Background**:
The UK's STEM workforce has persistent gender imbalances — women represent only 24% of the STEM workforce (WISE 2023), with particular underrepresentation in engineering (16%), computing (20%), and physics (23%). The pipeline "leaks" at specific transition points: GCSE to A-level subject choice, undergraduate to postgraduate, early career to mid-career, and mid-career to senior leadership. However, current data on these transitions is fragmented across DfE (education), HESA (higher education), UKRI (research funding), ONS (workforce), and individual professional bodies. No single dashboard provides a longitudinal view.

**Driver Intensity**: HIGH

**Enablers**:

- Automated data pipeline from 8+ sources with standardised definitions
- Longitudinal view showing pipeline leakage points across the STEM career journey
- International comparison capability (EU, OECD benchmarks)

**Blockers**:

- Data sharing agreements with HESA, UKRI, DfE, and ONS take time
- Different data sources use different STEM definitions and classification systems
- Longitudinal individual tracking not possible without unique identifier (data protection barrier)

---

### SD-2: UKRI — Research Funding Diversity Accountability

**Stakeholder**: UKRI (UK Research and Innovation)

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Demonstrate that UKRI's GBP 8 billion annual research funding is distributed equitably by gender, with transparent data on application rates, success rates, and award values disaggregated by gender and intersecting characteristics.

**Context & Background**:
UKRI publishes annual diversity data showing persistent gender gaps in research funding — women submit fewer applications, have marginally lower success rates, and receive smaller average awards. UKRI's Equality, Diversity and Inclusion Strategy commits to addressing these gaps, but current reporting is fragmented across UKRI's nine constituent councils. The Women in STEM dashboard could provide a unified, public view of research funding equity.

**Driver Intensity**: HIGH

---

### SD-3: Royal Society and RAEng — Pipeline Visibility for Learned Societies

**Stakeholder**: Royal Society, Royal Academy of Engineering

**Driver Category**: STRATEGIC / ADVOCACY

**Driver Statement**: Access comprehensive pipeline data showing where women are being lost from STEM careers, enabling learned societies to design targeted fellowship programmes, mentoring schemes, and policy recommendations based on evidence rather than anecdote.

**Driver Intensity**: MEDIUM

---

### SD-4: WISE Campaign and STEM Women — Accountability and Inspiration

**Stakeholder**: WISE Campaign, STEM Women

**Driver Category**: ADVOCACY / SOCIAL

**Driver Statement**: Ensure the dashboard provides accessible, inspiring data that demonstrates both progress and remaining challenges in women's STEM participation, enabling advocacy campaigns and providing role model evidence for girls considering STEM careers.

**Driver Intensity**: MEDIUM

---

### SD-5: DfE — Education Pipeline Data Integration

**Stakeholder**: Department for Education

**Driver Category**: OPERATIONAL / POLICY

**Driver Statement**: Contribute education pipeline data (GCSE/A-level subject choices, apprenticeship starts, FE enrolment by gender) to the dashboard, enabling joined-up analysis of where girls disengage from STEM subjects.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Single Authoritative STEM Diversity Data Source

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: DSIT Analysis and Data Director

**Goal Statement**: Establish the Women in STEM Dashboard as the single authoritative source for UK STEM gender diversity data, cited by government, industry, and media in preference to multiple inconsistent sources.

**Success Metrics**:

- **Primary Metric**: Citation count in government publications, media, and academic papers
- **Target**: Cited as primary source in 80%+ of government STEM diversity publications within 24 months

---

### Goal G-2: Full Pipeline Visibility from Education to Leadership

**Derived From Drivers**: SD-1, SD-3, SD-5

**Goal Owner**: DSIT Chief Scientific Adviser

**Goal Statement**: Provide data covering the complete STEM pipeline — from GCSE/A-level subject choice through undergraduate/postgraduate enrolment, doctoral completion, early career, research funding, mid-career, and senior leadership — with gender disaggregation at each stage.

**Success Metrics**:

- **Primary Metric**: Number of pipeline stages with complete gender-disaggregated data
- **Target**: 8+ pipeline stages with data published within 6 months of collection period

---

### Goal G-3: Intersectional Analysis Capability

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: DSIT Diversity and Inclusion Team

**Goal Statement**: Enable intersectional analysis of STEM diversity — gender crossed with ethnicity, disability, socio-economic background, and geographic region — to identify compounding barriers.

**Success Metrics**:

- **Primary Metric**: Intersectional queries available across 3+ dimensions
- **Target**: Full intersectional analysis available within 18 months

---

### Goal G-4: Timely Data Publication

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: DSIT Analysis and Data Director

**Goal Statement**: Reduce the time lag between data collection and publication from 12-24 months to a maximum of 6 months, ensuring policy decisions are based on current data.

**Success Metrics**:

- **Primary Metric**: Average data publication lag
- **Baseline**: 12-24 months
- **Target**: 6 months maximum

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| DSIT CSA | SD-1 | Evidence-based policy | G-1 | Single authoritative source |
| DSIT CSA | SD-1 | Evidence-based policy | G-2 | Full pipeline visibility |
| UKRI | SD-2 | Funding accountability | G-1 | Single authoritative source |
| UKRI | SD-2 | Funding accountability | G-4 | Timely data |
| Royal Society/RAEng | SD-3 | Pipeline visibility | G-2 | Full pipeline visibility |
| WISE/STEM Women | SD-4 | Accountability | G-3 | Intersectional analysis |
| DfE | SD-5 | Education pipeline | G-2 | Full pipeline visibility |

### Conflict Analysis

- **Conflict 1**: Researchers (SD-1, SD-3) want individual-level longitudinal tracking but this conflicts with UK GDPR data minimisation
  - **Resolution Strategy**: Use aggregate cohort tracking rather than individual tracking. Publish data at cohort level (e.g., "women who started STEM PhDs in 2020") rather than tracking individual researchers.

- **Conflict 2**: Industry (CBI/TechUK) wants benchmarking data positioned positively but advocacy groups (WISE) want accountability data highlighting failures
  - **Resolution Strategy**: Dashboard provides both narrative frames — progress indicators (absolute and percentage improvement) alongside gap indicators (remaining disparity). Users choose their analytical perspective.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| WISE Statistics 2023 | Report | WISE Campaign | Women as 24% of STEM workforce | N/A |
| UKRI EDI Strategy | Strategy | UKRI | Funding equity commitments | N/A |
| DSIT Science and Technology Framework | Strategy | DSIT | R&D workforce diversity objectives | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Women in STEM Tracking Dashboard (Project 004)
**Model**: Claude Opus 4.6
