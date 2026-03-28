# Stakeholder Drivers & Goals Analysis: Waste Management Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Waste Management Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Waste Management Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Environment Agency, Local Authority Waste Teams, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Waste Management Analytics platform, their underlying drivers, and how these drivers translate into goals and measurable outcomes.

### Key Findings

The Waste Management Analytics platform sits at the intersection of environmental regulation, local government operations, and national policy reporting. The dominant tension is between the Environment Agency's need for comprehensive, real-time waste tracking data for enforcement and local authorities' concern about the administrative burden of digital reporting requirements imposed on already-stretched waste teams. DEFRA's policy team needs aggregated national waste statistics for Resources and Waste Strategy reporting but struggles with the 2-year lag in current waste data publication (WasteDataFlow). The strongest alignment exists around digitising waste transfer notes — all stakeholders agree paper-based WTNs are inefficient, error-prone, and obstruct both compliance and analysis.

### Critical Success Factors

- Digitise waste transfer notes nationally, replacing the paper-based system with a digital standard
- Aggregate waste data from 333 local authorities into a single national analytics platform with less than 3 months data lag
- Provide the Environment Agency with near-real-time waste flow visibility for enforcement
- Deliver actionable analytics that help local authorities optimise collection routes, recycling rates, and disposal costs
- Integrate with the Circular Economy Marketplace (Project 002) for material flow tracking

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on digitising waste transfer notes and improving data quality. Significant tensions around data reporting burden on local authorities, data sharing between EA enforcement and council operations, and the pace of mandating digital reporting.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Environment | Minister | HIGH | HIGH | Manage Closely |
| DEFRA Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely |
| SRO, Waste Management Analytics | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely |
| DEFRA CDIO | Digital Leadership | HIGH | HIGH | Manage Closely |
| DEFRA Waste Statistics Team | National statistics production | MEDIUM | HIGH | Keep Informed |
| Service Owner | Service accountability | HIGH | HIGH | Manage Closely |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Environment Agency | Regulator | Waste enforcement | HIGH | HIGH |
| Local Authority Waste Teams | 333 councils | Data providers and users | MEDIUM | HIGH |
| WRAP | Delivery partner | Waste data expertise | MEDIUM | HIGH |
| Office for National Statistics (ONS) | Statistics | National statistics producer | MEDIUM | MEDIUM |
| Waste Management Industry | Private sector | Regulated operators | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding | HIGH | MEDIUM |
| Devolved Administrations | Scotland, Wales, NI | Devolved waste policy | MEDIUM | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of State|
        |  * DEFRA Perm Sec   |  * SRO              |
        |  * CDDO             |  * DEFRA CDIO       |
 P      |                     |  * Environment Agency|
 O      |                     |  * Service Owner    |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * ONS              |  * Local Authorities|
        |  * Devolved Admins  |  * Waste Statistics |
        |                     |  * WRAP             |
        |                     |  * Waste Industry   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Environment Agency — Real-Time Waste Flow Visibility for Enforcement

**Stakeholder**: Environment Agency

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Gain near-real-time visibility of waste flows across England to detect illegal waste activity (fly-tipping, permit breaches, illegal exports), identify organised waste crime networks, and target enforcement resources at the highest-risk operators and sites.

**Context & Background**:
Waste crime costs England an estimated GBP 1 billion annually. The EA's current enforcement capability is hampered by paper-based waste transfer notes that are easy to falsify, a 2-year lag in national waste data, and limited visibility of material movements between producer, carrier, and destination. Organised waste crime networks exploit these information gaps — routing waste through nominally compliant operators to illegal disposal sites. The EA needs a digital audit trail that tracks waste from producer to final destination in near-real-time, enabling pattern analysis to identify anomalous flows (e.g., an operator receiving far more waste than their permitted capacity allows).

**Driver Intensity**: CRITICAL

**Enablers**:

- Digital waste transfer notes with tamper-evident audit trails
- Near-real-time data feeds from waste operators and local authorities
- Analytics capability to detect anomalous waste flows (volume mismatches, impossible routes, unlicensed operators)
- Integration with EA permit and enforcement databases

**Blockers**:

- Resistance from operators to real-time reporting (concern about surveillance)
- Data quality too poor for reliable anomaly detection
- Legal challenges around data sharing for enforcement purposes
- Insufficient EA analytical capacity to act on intelligence

---

### SD-2: Local Authority Waste Teams — Actionable Analytics Without Reporting Burden

**Stakeholder**: 333 local authority waste teams in England

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Access actionable waste analytics (recycling rates, contamination rates, collection efficiency, disposal costs) that help optimise waste services and reduce costs — without being required to manually enter data into yet another central government reporting system alongside the existing WasteDataFlow obligation.

**Context & Background**:
Local authorities already report quarterly to WasteDataFlow (DEFRA's existing waste statistics system), a process that consumes significant officer time. Many councils use separate waste management systems from different vendors, making data extraction manual and error-prone. Councils are under severe financial pressure — waste services compete for budget with social care, housing, and education. Councils want analytics that help them make better operational decisions (optimise collection routes, reduce contamination, benchmark against peer councils) but are hostile to additional reporting requirements that consume officer time without delivering local value.

**Driver Intensity**: HIGH

**Enablers**:

- Automated data extraction from existing council waste management systems (no manual re-keying)
- Analytics dashboards that provide operational value to councils (not just central government reporting)
- Benchmarking against comparable councils (similar demographics, geography, urbanisation)
- Integration with existing WasteDataFlow reporting to reduce duplication, not increase it

**Blockers**:

- Mandatory new reporting requirements on top of existing WasteDataFlow
- Platform requiring manual data entry by already-stretched council officers
- Analytics focused on central government needs with no value to councils
- Requirement to switch waste management systems or adopt a specific vendor platform

---

### SD-3: DEFRA Waste Statistics Team — Timely, Granular National Waste Data

**Stakeholder**: DEFRA Waste Statistics Team

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Reduce the current 2-year lag in national waste statistics publication to under 6 months, increase data granularity from annual national totals to quarterly local authority level, and improve data quality to meet ONS National Statistics standards.

**Context & Background**:
UK waste statistics are currently published by DEFRA with approximately a 2-year lag — the 2023/24 waste data will be published in late 2025. This lag makes the data nearly useless for policy evaluation and renders ministerial statements about waste trends inherently backward-looking. The Resources and Waste Strategy introduced new policies (consistency of collections, deposit return scheme, extended producer responsibility) that require timely evaluation. DEFRA's statistics team needs near-real-time data to evaluate policy effectiveness, respond to parliamentary questions with current figures, and report to international bodies (Eurostat, OECD) within their reporting windows.

**Driver Intensity**: HIGH

**Enablers**:

- Automated data collection from local authorities and waste operators replacing manual WasteDataFlow returns
- Standardised data model enabling consistent aggregation across 333 councils
- Data quality validation at point of entry (not retrospective cleaning)
- Near-real-time data pipeline with quarterly publication capability

**Blockers**:

- Council waste management systems too heterogeneous for automated extraction
- Data quality too poor for ONS National Statistics designation without manual cleaning
- Resistance from councils to more frequent reporting
- Legal basis for mandatory reporting unclear for private waste operators

---

### SD-4: DEFRA Resources and Waste Policy Team — Evidence for Policy Evaluation

**Stakeholder**: DEFRA Resources and Waste Policy Team

**Driver Category**: STRATEGIC

**Driver Statement**: Access timely, granular waste data to evaluate the effectiveness of Resources and Waste Strategy policies (consistent collections, EPR for packaging, deposit return scheme) and make evidence-based decisions on future policy interventions.

**Context & Background**:
The Environment Act 2021 introduced several major waste policies that are being phased in over 2024-2028. DEFRA's policy team needs to evaluate whether these policies are working — is EPR for packaging reducing packaging waste? Is consistent collection increasing recycling rates? Is the deposit return scheme reducing litter? Without timely data, policy evaluation is impossible and ministers cannot report progress to Parliament. The policy team also needs the ability to model "what if" scenarios — what would happen to national recycling rates if residual waste collections moved to fortnightly?

**Driver Intensity**: HIGH

**Enablers**:

- Near-real-time waste data with local authority granularity
- Analytical tools for policy impact assessment (before/after EPR, before/after consistent collections)
- Scenario modelling capability
- Data linkage between waste, recycling, and economic data

**Blockers**:

- Data lag too long for timely policy evaluation
- Data granularity insufficient for local impact assessment
- No causal analysis capability (correlation vs causation)
- Insufficient analytical skills within the policy team

---

## Driver-to-Goal Mapping

### Goal G-1: Digital Waste Transfer Notes Adopted by 80% of Local Authorities Within 18 Months

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: Service Owner

**Goal Statement**: Achieve adoption of digital waste transfer note generation by at least 80% of English local authorities (265 councils) within 18 months of launch.

**Success Metrics**:

- **Primary Metric**: Number of local authorities generating digital WTNs through the platform
- **Target**: 265 (80% of 333)
- **Secondary Metric**: Number of paper WTNs eliminated (target: 10 million per year)

---

### Goal G-2: National Waste Data Published Quarterly with Less Than 3 Months Lag

**Derived From Drivers**: SD-3, SD-4

**Goal Owner**: DEFRA Waste Statistics Team

**Goal Statement**: Reduce national waste statistics publication frequency from annual (2-year lag) to quarterly (3-month lag) within 24 months of platform launch.

**Success Metrics**:

- **Primary Metric**: Time from data period end to publication
- **Current**: ~24 months
- **Target**: 3 months

---

### Goal G-3: Waste Crime Detection Rate Increased by 30% Through Analytics

**Derived From Drivers**: SD-1

**Goal Owner**: Environment Agency

**Goal Statement**: Increase waste crime detection rate by 30% within 24 months through anomalous flow detection, permit breach identification, and real-time waste tracking analytics.

**Success Metrics**:

- **Primary Metric**: Number of waste crime cases identified through platform analytics
- **Baseline**: EA currently identifies ~1,200 significant waste crime cases annually
- **Target**: 1,560 cases (30% increase)

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Environment Agency | SD-1 | Real-time enforcement visibility | G-1 | Digital WTNs (80% adoption) |
| Environment Agency | SD-1 | Real-time enforcement visibility | G-3 | Waste crime detection (+30%) |
| Local Authorities | SD-2 | Actionable analytics without burden | G-1 | Digital WTNs (80% adoption) |
| DEFRA Statistics | SD-3 | Timely national data | G-2 | Quarterly publication (3-month lag) |
| DEFRA Policy | SD-4 | Policy evaluation evidence | G-2 | Quarterly publication (3-month lag) |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Environment Agency (SD-1) wants comprehensive, real-time waste tracking data from all operators, but Local Authorities (SD-2) resist additional reporting requirements that consume officer time without local benefit.
  - **Resolution Strategy**: Automated data extraction from existing council systems (no manual re-keying). Platform provides operational analytics that benefit councils (benchmarking, route optimisation, cost analysis) as incentive for participation. Digital WTNs save council time versus paper — net reduction in administrative burden.

- **Conflict 2**: DEFRA Statistics (SD-3) wants standardised data across 333 councils for aggregation, but councils use different waste management systems with incompatible data models.
  - **Resolution Strategy**: Platform provides a standardised data ingestion API with adapters for major council waste management systems (Whitespace, Bartec, Yotta). Data quality validation at ingestion, not retrospective cleaning.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Resources and Waste Strategy 2018 | Policy | GOV.UK | National waste data improvement commitments | N/A |
| Environment Act 2021 | Legislation | legislation.gov.uk | Waste tracking, EPR, enforcement | N/A |
| WasteDataFlow | System | wastedataflow.org | Current waste statistics collection | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Waste Management Analytics (Project 003)
**Model**: Claude Opus 4.6
