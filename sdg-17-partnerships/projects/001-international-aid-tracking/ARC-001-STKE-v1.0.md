# Stakeholder Drivers & Goals Analysis: International Aid Tracking

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | International Aid Tracking (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, International Aid Tracking Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | FCDO Digital, ICAI, CDDO, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the International Aid Tracking programme, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The International Aid Tracking programme operates at the intersection of political accountability, international treaty obligations, and operational efficiency. The strongest alignment exists around improving IATI data quality and timeliness — this satisfies Ministerial transparency commitments, ICAI scrutiny requirements, OECD DAC peer review expectations, and operational needs for better programme management data. The most significant conflict is between FCDO's desire for comprehensive real-time ODA tracking and the practical constraints of collecting data from over 30 delivery partners, multilateral channels, and cross-departmental ODA (ODA is spent by 16 UK Government departments, not just FCDO).

### Critical Success Factors

- Achieve IATI data quality score above 80% (currently 71%) to maintain UK's position as a transparency leader
- Consolidate cross-departmental ODA reporting into a single platform, reducing the current 6-month lag in comprehensive UK ODA figures
- Deliver DAC CRS++ compliant reporting that passes OECD validation without manual correction
- Provide ICAI with self-service access to ODA data to support their evaluations without bespoke data requests
- Maintain uninterrupted DAC statistical reporting throughout system transition

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for better ODA data quality and transparency. Significant tension between FCDO's desire for a single comprehensive platform and other ODA-spending departments' (BEIS, Defra, DHSC) resistance to reporting through an FCDO-controlled system. Treasury's focus on ODA as a percentage of GNI creates pressure for real-time tracking that conflicts with the statistical rigour required for official ODA figures.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Foreign, Commonwealth & Development Affairs | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| FCDO Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, International Aid Tracking | Programme Sponsor (FCDO) | HIGH | HIGH | Manage Closely — Weekly programme board |
| FCDO Chief Digital Information Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Director, International Development | Policy leadership for ODA | HIGH | HIGH | Manage Closely — Policy requirements, reporting needs |
| FCDO Head of Statistics | ODA statistical reporting lead | HIGH | HIGH | Manage Closely — DAC reporting, data quality |
| FCDO Finance Director | ODA budget management | HIGH | MEDIUM | Keep Satisfied — Financial reconciliation |
| FCDO SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |
| FCDO Programme Managers | Day-to-day ODA programme management | MEDIUM | HIGH | Keep Informed — User research, requirements input |
| FCDO Country Office Staff | In-country ODA delivery | LOW | HIGH | Keep Informed — Training, data collection |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO (Central Digital & Data Office) | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | ODA/GNI ratio monitoring, funding | HIGH | HIGH |
| ICAI (Independent Commission for Aid Impact) | Parliament | Independent scrutiny of UK aid | HIGH | HIGH |
| National Audit Office (NAO) | Parliament | Value for money audit of ODA | HIGH | MEDIUM |
| International Development Committee (IDC) | House of Commons | Parliamentary oversight | HIGH | MEDIUM |
| OECD DAC Secretariat | OECD | ODA statistical reporting standards | HIGH | HIGH |
| IATI Secretariat | UNDP-hosted | IATI data standard governance | MEDIUM | HIGH |
| Other ODA-spending departments (BEIS, Defra, DHSC, etc.) | Cross-government | ODA data contributors | MEDIUM | MEDIUM |
| Multilateral organisations (World Bank, UN agencies) | International | Multilateral ODA channel partners | MEDIUM | MEDIUM |
| Developing country partner governments | International | ODA recipients, mutual accountability | LOW | HIGH |
| Bond (UK NGO network) | Civil society | Aid transparency advocacy | LOW | HIGH |
| Publish What You Fund | Civil society | Aid transparency index ranking | LOW | HIGH |
| UK Export Finance (UKEF) | Government | ODA-eligible export credits | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end ODA tracking service | HIGH / HIGH | Manage Closely — Service reviews, user outcomes |
| Product Manager | Prioritises features against user needs and DAC/IATI requirements | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk escalation |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |
| FCDO CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * FCDO Secretary   |
        |  * NAO              |    of State         |
        |  * IDC              |  * FCDO Perm Sec    |
        |  * FCDO SIRO        |  * SRO              |
 P      |  * FCDO Finance Dir |  * HM Treasury      |
 O      |                     |  * ICAI             |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * UKEF             |  * OECD DAC         |
        |  * Multilaterals    |  * IATI Secretariat |
        |                     |  * Bond/PWYF        |
        |                     |  * Partner countries|
        |                     |  * Programme Mgrs   |
        |                     |  * Country Office   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: FCDO Secretary of State — Political Accountability for Aid Spending

**Stakeholder**: Secretary of State for Foreign, Commonwealth & Development Affairs

**Driver Category**: STRATEGIC

**Driver Statement**: Demonstrate to Parliament and the public that UK ODA is spent effectively, reaches intended beneficiaries, and delivers measurable development outcomes, supporting the International Development Strategy (2022) commitment to "honest and open" aid.

**Context & Background**:
Following the merger of DFID and FCO in 2020 and the reduction of the ODA/GNI target from 0.7% to 0.5%, Parliamentary and public scrutiny of aid spending has intensified. The International Development Committee regularly challenges Ministers on aid effectiveness. The Secretary of State needs near-real-time visibility of where UK aid money flows, what results it achieves, and how it compares internationally.

**Driver Intensity**: CRITICAL

**Enablers**:

- Single platform showing all UK ODA (not just FCDO's share)
- Results data linked to financial data at activity level
- Dashboard suitable for Ministerial briefing at short notice

**Blockers**:

- 16 departments spend ODA independently with different systems
- Results data is inherently lagging (outcomes take years to materialise)
- Classification constraints on sensitive ODA programmes

**Related Stakeholders**: HM Treasury (ODA/GNI ratio), ICAI (scrutiny), IDC (Parliamentary oversight)

---

### SD-2: HM Treasury — ODA/GNI Ratio Management

**Stakeholder**: HM Treasury (International Finance Directorate)

**Driver Category**: FINANCIAL

**Driver Statement**: Monitor UK ODA spending in near-real-time against the GNI-linked target to manage fiscal risk, avoid underspend (political embarrassment) or overspend (fiscal pressure), and ensure accurate forecasting for Spending Review settlements.

**Context & Background**:
The UK's ODA target is set as a percentage of GNI, which is itself a moving target revised quarterly by ONS. Treasury needs to match ODA spending across 16 departments against a denominator that changes, creating a complex fiscal management challenge. The current 6-month lag in comprehensive ODA figures makes in-year fiscal management difficult.

**Driver Intensity**: CRITICAL

**Enablers**:

- Real-time ODA spending dashboard covering all departments
- Integration with OSCAR for cross-government spend visibility
- Forecasting tools linking ODA commitments to expected disbursement profiles

**Blockers**:

- Different departments report ODA at different frequencies and granularities
- Multilateral contributions and imputed costs complicate real-time tracking
- Statistical ODA figures (official) lag behind management accounting figures

**Related Stakeholders**: FCDO Finance Director, Other ODA-spending departments, ONS (GNI)

---

### SD-3: ICAI — Independent Scrutiny of Aid Effectiveness

**Stakeholder**: Independent Commission for Aid Impact

**Driver Category**: COMPLIANCE

**Driver Statement**: Access comprehensive, granular, and timely ODA data to conduct independent evaluations of UK aid effectiveness without relying on bespoke data requests to FCDO (which introduce delay and potential bias).

**Context & Background**:
ICAI is the independent body established to scrutinise UK aid. Currently, each ICAI evaluation requires a bespoke data request to FCDO, which can take weeks to fulfil and may not include data from other ODA-spending departments. ICAI's credibility depends on independent access to comprehensive data.

**Driver Intensity**: HIGH

**Enablers**:

- Self-service access to ODA data across all departments
- Activity-level data with results, financial flows, and geographic breakdowns
- Historical data for trend analysis across evaluation cycles

**Blockers**:

- Classification restrictions on some ODA programmes
- Departmental resistance to providing granular data to external scrutiny
- Data quality variations across departments

**Related Stakeholders**: NAO, IDC, Bond network

---

### SD-4: OECD DAC Secretariat — Statistical Reporting Compliance

**Stakeholder**: OECD Development Assistance Committee Secretariat

**Driver Category**: COMPLIANCE

**Driver Statement**: Receive UK ODA statistical returns that are complete, accurate, correctly coded to CRS++ purpose codes, and submitted within DAC reporting deadlines, enabling meaningful international comparisons and peer review.

**Context & Background**:
The UK undergoes DAC Peer Review approximately every 5 years (last: 2020). The DAC CRS++ reporting framework requires detailed coding of every ODA activity by sector, channel, flow type, and tied/untied status. Current UK reporting requires significant manual effort to compile and validate, with some coding applied retrospectively rather than at activity creation.

**Driver Intensity**: HIGH

**Enablers**:

- CRS++ codes assigned at activity creation, validated in real-time
- Automated DAC statistical return generation
- Validation against DAC business rules before submission

**Blockers**:

- Legacy systems lacking CRS++ coding at source
- Staff unfamiliarity with DAC coding requirements
- Cross-departmental ODA reported through different classifications

**Related Stakeholders**: FCDO Head of Statistics, Other ODA-spending departments

---

### SD-5: Other ODA-Spending Departments — Minimal Reporting Burden

**Stakeholder**: BEIS, Defra, DHSC, Home Office, and 12 other departments that spend ODA

**Driver Category**: OPERATIONAL

**Driver Statement**: Fulfil ODA reporting obligations with minimal additional administrative burden on departmental staff, without surrendering control of programme data to FCDO or adopting an FCDO-centric system that does not reflect their operational context.

**Context & Background**:
Sixteen UK Government departments spend ODA, but most lack dedicated ODA tracking systems. ODA reporting is often a secondary function performed by finance teams alongside their primary departmental responsibilities. These departments resist solutions that increase their workload or require them to adopt FCDO's system architecture and terminology.

**Driver Intensity**: MEDIUM

**Enablers**:

- Simple API or upload interface for ODA data submission
- Pre-populated CRS++ coding based on department and programme type
- Automated validation with clear error messages
- Departmental data remains under departmental control

**Blockers**:

- FCDO-centric design that assumes FCDO terminology and workflow
- Complex manual data entry requirements
- Lack of dedicated ODA staff in smaller departments

**Related Stakeholders**: FCDO, HM Treasury, CDDO

---

### SD-6: Developing Country Partners — Mutual Accountability

**Stakeholder**: Partner country governments receiving UK ODA

**Driver Category**: STRATEGIC

**Driver Statement**: Access timely, comprehensive information about UK aid flows to their country to support national development planning, budget management, and mutual accountability commitments under the Global Partnership for Effective Development Co-operation.

**Context & Background**:
The Busan Partnership (2011) commits donors to making aid information available to partner countries to support country-led development. Many partner countries struggle to integrate donor data into their national budgets due to late, incomplete, or inconsistent reporting. The IATI standard was designed to address this, but UK IATI data currently varies in timeliness and granularity.

**Driver Intensity**: MEDIUM

**Enablers**:

- Forward-looking budget data published via IATI (3-year activity budgets)
- Country-level data accessible without FCDO intermediation
- Data in formats usable by partner country Aid Information Management Systems (AIMS)

**Blockers**:

- Classification restrictions on some country programmes
- Partner countries have varying technical capacity to consume API data
- Language barriers (IATI data primarily in English)

**Related Stakeholders**: Multilateral organisations, Bond network

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve IATI Data Quality Score Above 80%

**Derived From Drivers**: SD-1, SD-3, SD-4, SD-6

**Goal Owner**: FCDO Head of Statistics

**Goal Statement**: Improve UK IATI data quality score from 71% to 80%+ within 18 months, as measured by the IATI Dashboard data quality assessment.

**Why This Matters**: Higher data quality satisfies transparency commitments (SD-1), enables independent scrutiny (SD-3), aligns with DAC reporting standards (SD-4), and provides partner countries with usable data (SD-6).

**Success Metrics**:

- **Primary Metric**: IATI Dashboard data quality score >= 80%
- **Secondary Metrics**:
  - Timeliness: 90% of activities updated within 30 days of change
  - Completeness: 100% of activities coded to CRS++ sectors
  - Forward-looking: 80% of activities with 3-year budget data

**Baseline**: 71% IATI quality score (2025 assessment)

**Target**: 80%+ IATI quality score

**Measurement Method**: IATI Dashboard quarterly assessment (automated)

---

### Goal G-2: Consolidate Cross-Departmental ODA Reporting

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: SRO, International Aid Tracking

**Goal Statement**: Reduce the time to produce comprehensive UK ODA figures from 6 months to 30 days by consolidating reporting from all 16 ODA-spending departments into a single platform within 24 months.

**Why This Matters**: Enables real-time ODA/GNI monitoring (SD-2), provides Ministers with current data (SD-1), while minimising burden on non-FCDO departments (SD-5).

**Success Metrics**:

- **Primary Metric**: Time from quarter-end to comprehensive UK ODA figure <= 30 days
- **Secondary Metrics**:
  - 16/16 ODA-spending departments reporting through the platform
  - Automated DAC statistical return generation (no manual compilation)

**Baseline**: 6 months to produce comprehensive UK ODA figures

**Target**: 30 days

**Measurement Method**: Date of comprehensive ODA figure availability vs. quarter-end date

---

### Goal G-3: Enable ICAI Self-Service Data Access

**Derived From Drivers**: SD-3

**Goal Owner**: Director, International Development

**Goal Statement**: Provide ICAI with self-service API access to all non-classified UK ODA data across all departments within 12 months, eliminating bespoke data request processes.

**Why This Matters**: Directly addresses ICAI's independence requirement (SD-3) and reduces FCDO administrative burden.

**Success Metrics**:

- **Primary Metric**: ICAI data requests fulfilled via self-service (target: 90%)
- **Secondary Metrics**:
  - Time from ICAI data request to data access: < 1 day (currently 2-4 weeks)
  - ICAI satisfaction with data access (annual survey)

**Baseline**: 0% self-service; 100% via bespoke request (2-4 week turnaround)

**Target**: 90% self-service; < 1 day access

---

### Goal G-4: Automated DAC CRS++ Reporting

**Derived From Drivers**: SD-4, SD-5

**Goal Owner**: FCDO Head of Statistics

**Goal Statement**: Automate DAC CRS++ statistical return generation, achieving zero manual corrections required for submission, within 18 months.

**Why This Matters**: Satisfies DAC reporting compliance (SD-4) while reducing manual burden on departmental staff (SD-5).

**Success Metrics**:

- **Primary Metric**: DAC statistical return generated without manual correction
- **Secondary Metrics**:
  - CRS++ validation pass rate at source: 99%+
  - Time to generate DAC return: < 1 day (currently 6 weeks)

**Baseline**: 6 weeks manual compilation; 15% of records require correction

**Target**: < 1 day automated generation; 0% manual corrections

---

## Goal-to-Outcome Mapping

### Outcome O-1: UK Maintains Top-5 Aid Transparency Ranking

**Supported Goals**: G-1, G-2, G-4

**Outcome Statement**: UK maintains or improves its position in the top 5 of the Publish What You Fund Aid Transparency Index, demonstrating global leadership in development transparency.

**Measurement Details**:

- **KPI**: Aid Transparency Index rank
- **Current Value**: 4th (2024 assessment)
- **Target Value**: Top 3
- **Measurement Frequency**: Biennial (PWYF assessment cycle)
- **Data Source**: Publish What You Fund Aid Transparency Index

**Business Value**:

- **Strategic Impact**: Supports UK's "force for good" narrative and Global Britain positioning
- **Operational Impact**: Better data quality reduces manual reporting overhead by estimated 2,000 staff hours/year
- **International Impact**: Strengthens UK credibility in DAC peer review and Global Partnership monitoring

---

### Outcome O-2: Real-Time Fiscal Management of ODA/GNI Target

**Supported Goals**: G-2

**Outcome Statement**: HM Treasury achieves in-year visibility of UK ODA spending against GNI target, reducing fiscal risk of underspend/overspend and improving Spending Review accuracy.

**Measurement Details**:

- **KPI**: Time lag between ODA spend and consolidated reporting
- **Current Value**: 6 months
- **Target Value**: 30 days
- **Measurement Frequency**: Quarterly
- **Data Source**: Cross-departmental ODA platform

**Business Value**:

- **Financial Impact**: Avoidance of ODA underspend/overspend (estimated GBP 50-200M fiscal management improvement)
- **Strategic Impact**: Improved Treasury confidence in ODA forecasting

---

### Outcome O-3: Independent Scrutiny Without Friction

**Supported Goals**: G-3

**Outcome Statement**: ICAI conducts evaluations 40% faster through self-service data access, increasing the number of evaluations per parliamentary session.

**Measurement Details**:

- **KPI**: Average time from evaluation inception to data availability
- **Current Value**: 4-6 weeks
- **Target Value**: < 1 day
- **Measurement Frequency**: Per evaluation
- **Data Source**: ICAI evaluation tracker

---

## Complete Traceability Matrix

### Stakeholder -> Driver -> Goal -> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Political accountability | G-1 | IATI quality 80%+ | O-1 | Top-5 transparency |
| Secretary of State | SD-1 | Political accountability | G-2 | Consolidated reporting | O-2 | Real-time ODA/GNI |
| HM Treasury | SD-2 | ODA/GNI management | G-2 | Consolidated reporting | O-2 | Real-time ODA/GNI |
| ICAI | SD-3 | Independent scrutiny | G-3 | Self-service access | O-3 | Faster evaluations |
| OECD DAC | SD-4 | Statistical compliance | G-4 | Automated DAC returns | O-1 | Top-5 transparency |
| Other departments | SD-5 | Minimal burden | G-2 | Consolidated reporting | O-2 | Real-time ODA/GNI |
| Other departments | SD-5 | Minimal burden | G-4 | Automated DAC returns | O-1 | Top-5 transparency |
| Partner countries | SD-6 | Mutual accountability | G-1 | IATI quality 80%+ | O-1 | Top-5 transparency |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: FCDO (SD-1) wants a single comprehensive ODA platform, but other departments (SD-5) resist surrendering data control to FCDO
  - **Resolution Strategy**: Federated architecture — data remains in department systems, accessed via standardised APIs. FCDO manages the aggregation layer but does not hold departmental source data. (Aligns with Principle 5: Cross-Government Data Federation)

- **Conflict 2**: Treasury (SD-2) wants real-time ODA figures for fiscal management, but FCDO Head of Statistics requires statistical rigour that takes time to validate
  - **Resolution Strategy**: Two-tier reporting — management accounts (near-real-time, marked as provisional) for Treasury fiscal management, alongside official statistics (validated, published on ONS schedule) for Parliamentary and international reporting

- **Conflict 3**: ICAI (SD-3) wants unrestricted data access, but some ODA programmes have classification restrictions (conflict zones, sensitive governance programmes)
  - **Resolution Strategy**: Default to maximum access with specific programme-level exemptions documented and minimised. ICAI security-cleared analysts can access OFFICIAL-SENSITIVE data under controlled conditions.

**Synergies**:

- **Synergy 1**: Improving IATI data quality (G-1) simultaneously satisfies Ministerial transparency (SD-1), DAC compliance (SD-4), ICAI scrutiny (SD-3), and partner country needs (SD-6)
- **Synergy 2**: Automated CRS++ coding (G-4) reduces burden on other departments (SD-5) while improving DAC compliance (SD-4)

---

## Communication & Engagement Plan

### Secretary of State / Ministers

**Primary Message**: The International Aid Tracking platform will give you real-time visibility of all UK aid spending, enabling you to answer Parliamentary Questions with current data and demonstrate aid effectiveness to the public.

**Key Talking Points**:

- Near-real-time ODA dashboard replacing the current 6-month reporting lag
- UK will strengthen its top-5 aid transparency ranking
- Supports delivery of the International Development Strategy

**Communication Frequency**: Monthly Ministerial briefing; ad hoc for PQ support

**Preferred Channel**: Ministerial submission with dashboard demo

---

### ICAI

**Primary Message**: Self-service data access will eliminate the weeks-long wait for bespoke data requests, enabling faster, more comprehensive evaluations.

**Key Talking Points**:

- API access to all non-classified ODA data across all departments
- Historical data for trend analysis across evaluation cycles
- FCDO is investing in data quality that will improve evaluation evidence base

**Communication Frequency**: Quarterly liaison meetings

**Preferred Channel**: Technical briefings with ICAI analysts

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| FCDO Programme Managers | Manual IATI reporting, retrospective CRS++ coding | Real-time coded data entry, automated IATI publication | HIGH | MEDIUM | Training, user research, demonstrate time savings |
| Other ODA departments | Spreadsheet-based annual ODA returns | API/upload quarterly submission | MEDIUM | HIGH | Simple interface, pre-populated coding, minimal fields |
| FCDO Statistics | Manual DAC return compilation (6 weeks) | Automated generation (1 day) | HIGH | LOW | Collaborative design, quality assurance role preserved |
| ICAI | Bespoke data requests (2-4 weeks) | Self-service API (< 1 day) | HIGH | LOW | Early API access, training on data platform |

### Change Readiness

**Champions** (Enthusiastic supporters):

- FCDO Head of Statistics — directly benefits from automated DAC reporting
- ICAI — self-service access is a long-standing request
- Publish What You Fund — UK transparency leadership is their mission

**Fence-sitters** (Neutral, need convincing):

- FCDO Programme Managers — support the vision but concerned about data entry burden
- HM Treasury — supportive if real-time data is truly achievable

**Resisters** (Opposed or sceptical):

- Other ODA departments — perceive additional reporting burden without direct benefit
  - Strategy: Demonstrate simplified interface, pre-populated coding, reduced manual effort vs. current spreadsheet process

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Programme budget approval | FCDO Finance Director | FCDO Permanent Secretary | HM Treasury, CDDO | All stakeholders |
| Architecture decisions | Solution Architect | FCDO CDIO | CDDO, cross-dept architects | Programme team |
| Data standard selection (IATI/DAC) | FCDO Head of Statistics | SRO | OECD DAC, IATI Secretariat | All departments |
| Cross-department data sharing | Data Sharing Lead | SRO | All ODA departments, ICO | CDDO |
| Go/No-go for go-live | SRO | FCDO Permanent Secretary | Steering Committee | All stakeholders |
| IATI publication policy | FCDO Head of Statistics | Director, Int'l Development | IATI Secretariat, PWYF | Ministers |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day delivery decisions)
2. **Level 2**: SRO and Programme Board (scope, timeline, budget, cross-department disputes)
3. **Level 3**: FCDO Permanent Secretary (strategic direction, Ministerial escalation, Treasury disputes)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| FCDO CDIO | PENDING | | PENDING |
| FCDO Head of Statistics | PENDING | | PENDING |
| HM Treasury representative | PENDING | | PENDING |
| ICAI representative | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme SRO | | | |
| FCDO CDIO | | | |
| Director, International Development | | | |

---

## Appendices

### Appendix A: Key References

- International Development Act 2002
- International Development Strategy (2022)
- IATI Standard v2.03
- OECD DAC Statistical Reporting Directives
- Busan Partnership for Effective Development Co-operation (2011)
- UK Voluntary National Review (2019, 2023)
- Publish What You Fund Aid Transparency Index methodology
- ARC-000-PRIN-v1.0 (SDG 17 Architecture Principles)

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: International Aid Tracking
**Model**: Claude Opus 4.6
