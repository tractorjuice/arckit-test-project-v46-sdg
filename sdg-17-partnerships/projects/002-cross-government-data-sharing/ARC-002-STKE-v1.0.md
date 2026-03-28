# Stakeholder Drivers & Goals Analysis: Cross-Government Data Sharing Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Cross-Government Data Sharing Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Cross-Government Data Sharing Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office Digital, CDDO, Government Data Quality Hub, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Cross-Government Data Sharing Platform, their underlying drivers, and how these map to programme goals and measurable outcomes. The platform will enable secure, governed data exchange between UK Government departments to support SDG 17 objectives and broader cross-government data needs.

### Key Findings

The Cross-Government Data Sharing Platform sits at the centre of a long-standing tension in UK Government: departments recognise the value of shared data but are deeply protective of their data sovereignty, security boundaries, and operational independence. The strongest alignment is around the need for a discoverable data catalogue — all departments want to know what data exists across government. The deepest conflict is around access control: departments want to share data on their terms, with granular control over who sees what, while consuming departments want frictionless access. The Digital Economy Act 2017 provides a legal gateway for data sharing, but its implementation has been slow and inconsistent.

### Critical Success Factors

- Achieve adoption by at least 10 departments within 18 months, each publishing at least 5 datasets to the catalogue
- Establish a federated architecture that preserves department data sovereignty while enabling discovery and governed access
- Implement data sharing agreements as machine-readable, enforceable policies (not just PDF documents)
- Demonstrate compliance with UK GDPR, Digital Economy Act 2017, and departmental information governance requirements
- Deliver measurable reduction in the time from data request to data access (target: 80% reduction)

### Stakeholder Alignment Score

**Overall Alignment**: LOW-MEDIUM

Universal agreement that cross-government data discovery is needed. Significant disagreement on the operating model (centralised vs. federated), security architecture (shared infrastructure vs. department-controlled), and governance (who decides access). The history of previous failed cross-government data initiatives (e.g., Government Data Lake) creates scepticism about feasibility.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for the Cabinet Office | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| Cabinet Office Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Cross-Government Data Sharing | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| Chief Data Officer (CDO), Cabinet Office | Data strategy leadership | HIGH | HIGH | Manage Closely — Architecture, standards |
| CDDO Director | Cross-government digital assurance | HIGH | HIGH | Manage Closely — Standards, spend control |
| Government Data Quality Hub | Data standards and quality | MEDIUM | HIGH | Keep Informed — Standards development |
| Data Standards Authority | Cross-government data standards | MEDIUM | HIGH | Keep Informed — DCAT, API standards |
| Cabinet Office SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |
| Cabinet Office Security Team | Cyber security | HIGH | MEDIUM | Keep Satisfied — Security architecture |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Department Data Leads (all departments) | Cross-government | Data providers and consumers | HIGH | HIGH |
| ICO (Information Commissioner's Office) | Regulator | Data protection oversight | HIGH | MEDIUM |
| National Cyber Security Centre (NCSC) | Regulator | Cyber security assurance | HIGH | MEDIUM |
| NAO | Parliament | Value for money audit | HIGH | MEDIUM |
| ONS / UKSA | Statistical authority | Statistical data governance | MEDIUM | HIGH |
| HMRC | Major data holder | Tax and trade data | HIGH | MEDIUM |
| DWP | Major data holder | Benefits and employment data | HIGH | MEDIUM |
| NHS Digital / DHSC | Major data holder | Health data | HIGH | MEDIUM |
| Open Data Institute (ODI) | Civil society | Open data advocacy | LOW | HIGH |
| Alan Turing Institute | Research | Government data science | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes | HIGH / HIGH | Manage Closely |
| Service Owner | End-to-end data sharing service | HIGH / HIGH | Manage Closely |
| CDDO | Assurance and cross-government standards | HIGH / HIGH | Manage Closely |
| Chief Data Officer | Data strategy and governance | HIGH / HIGH | Manage Closely |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * ICO              |  * Minister         |
        |  * NCSC             |  * Perm Sec         |
        |  * NAO              |  * SRO              |
        |  * Cab Office SIRO  |  * CDO              |
 P      |  * HMRC             |  * CDDO             |
 O      |  * DWP              |  * Dept Data Leads  |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Alan Turing Inst |  * ONS/UKSA         |
        |                     |  * ODI              |
        |                     |  * Data Quality Hub |
        |                     |  * Data Standards   |
        |                     |    Authority        |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Cabinet Office Minister — Cross-Government Efficiency and Reform

**Stakeholder**: Minister for the Cabinet Office

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver the government's commitment to "better use of data across government" as set out in the National Data Strategy and the Integrated Review, demonstrating that data sharing can improve policy outcomes, reduce fraud, and drive efficiency.

**Context & Background**:
The National Data Strategy (2020) and subsequent government data commitments emphasise that government holds vast data assets but fails to use them effectively across departmental boundaries. High-profile examples (e.g., COVID-19 data sharing challenges, fraud detection gaps) have highlighted the cost of departmental data silos. The Cabinet Office owns the cross-government reform agenda.

**Driver Intensity**: CRITICAL

**Enablers**:

- Political mandate for cross-government data sharing
- Digital Economy Act 2017 providing legal gateway
- CDDO authority to set cross-government standards

**Blockers**:

- Departmental resistance to sharing "their" data
- History of failed cross-government data initiatives
- ICO scrutiny creating caution around data sharing

---

### SD-2: Department Data Leads — Data Sovereignty and Security

**Stakeholder**: Data leads across all major departments (collective)

**Driver Category**: RISK

**Driver Statement**: Maintain control over departmental data assets, ensuring that cross-government sharing does not compromise security, create compliance risk, or undermine departmental accountability for data quality and accuracy.

**Context & Background**:
Departments are legally accountable for their data under UK GDPR. Data breaches are reputationally damaging and carry financial penalties (ICO fines up to GBP 17.5M). Previous cross-government data initiatives required departments to copy data into centralised systems, creating security concerns and accountability ambiguity. Departments want to share data on their terms.

**Driver Intensity**: CRITICAL

**Enablers**:

- Federated architecture that keeps data in department systems
- Granular access controls under department authority
- Clear accountability model (data controller remains the source department)

**Blockers**:

- Centralised data lake approaches (copy data out of department control)
- "All or nothing" access models
- Unclear data controller/processor responsibilities

---

### SD-3: CDDO — Standards and Spend Control

**Stakeholder**: Central Digital and Data Office

**Driver Category**: OPERATIONAL

**Driver Statement**: Ensure cross-government data sharing is built on common standards (API, metadata, security) to prevent vendor lock-in, enable reuse, and provide value for money across the GBP 20B+ annual government digital spend.

**Context & Background**:
CDDO sets cross-government digital and data standards, including the Technology Code of Practice, GDS API standards, and the cross-government data ethics framework. CDDO has spend control authority over digital projects above GBP 1M. They need the platform to exemplify best practice.

**Driver Intensity**: HIGH

**Enablers**:

- Open standards (DCAT, OpenAPI, OAuth 2.0)
- Multi-cloud, vendor-neutral architecture
- Reusable components for other cross-government platforms

**Blockers**:

- Proprietary vendor platforms that create lock-in
- Bespoke solutions that cannot be reused
- Department-specific standards that fragment the ecosystem

---

### SD-4: ICO — Lawful Data Sharing

**Stakeholder**: Information Commissioner's Office

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure that cross-government data sharing has clear legal basis, proportionate data minimisation, transparency, and robust safeguards, demonstrating compliance with UK GDPR and the Data Protection Act 2018.

**Context & Background**:
The ICO has published guidance on data sharing including the Data Sharing Code of Practice. They support lawful data sharing but are concerned about mission creep, inadequate safeguards, and lack of transparency. The Digital Economy Act 2017 provides specific legal gateways for data sharing, but implementation must be demonstrably compliant.

**Driver Intensity**: HIGH

**Enablers**:

- Clear legal basis documented for each data sharing arrangement
- Data minimisation enforced technically (field-level access control)
- Transparency — public register of active data sharing agreements
- Data Protection Impact Assessments for each sharing arrangement

**Blockers**:

- Blanket access without purpose limitation
- Lack of transparency about what data is shared and why
- Insufficient safeguards for sensitive data categories

---

## Driver-to-Goal Mapping

### Goal G-1: Cross-Government Data Catalogue with 10+ Departments

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: Chief Data Officer, Cabinet Office

**Goal Statement**: Launch a DCAT-compliant cross-government data catalogue with at least 10 departments each publishing a minimum of 5 dataset descriptions within 18 months.

**Why This Matters**: Discovery is the prerequisite for sharing. Until departments know what data exists across government, they cannot request access.

**Success Metrics**:

- **Primary Metric**: Number of departments with published catalogue entries (target: 10+)
- **Secondary Metrics**:
  - Total datasets catalogued: 200+
  - Catalogue search queries per month: 500+
  - Time from catalogue discovery to access request: < 1 hour

**Baseline**: No single cross-government data catalogue exists; ad hoc knowledge sharing

**Target**: 10+ departments, 200+ datasets, searchable within 18 months

---

### Goal G-2: Federated API Gateway for Governed Data Access

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: SRO

**Goal Statement**: Implement a federated API gateway enabling governed data access across departments, with data remaining in source systems and access controlled by machine-readable data sharing agreements, within 24 months.

**Why This Matters**: Preserves department data sovereignty (SD-2) while enabling efficient sharing (SD-1) with auditable compliance (SD-4).

**Success Metrics**:

- **Primary Metric**: Active cross-department data feeds via API gateway: 50+
- **Secondary Metrics**:
  - Data sharing agreement execution time: < 5 days (vs. current 3-6 months)
  - API uptime: 99.95%
  - Compliance audit pass rate: 100%

**Baseline**: No standardised cross-department API gateway; bespoke point-to-point integrations

**Target**: 50+ active data feeds, < 5 days DSA execution

---

### Goal G-3: 80% Reduction in Data Request to Access Time

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: CDDO Director

**Goal Statement**: Reduce the average time from a department's data request to gaining access from 3-6 months to under 2 weeks within 24 months.

**Why This Matters**: The current data sharing process involves lengthy legal, governance, and technical negotiations. This delay means time-critical policy analysis often proceeds without cross-departmental data.

**Success Metrics**:

- **Primary Metric**: Median time from request to access: < 10 working days
- **Secondary Metrics**:
  - Proportion of requests fulfilled within 10 working days: 80%+
  - Number of abandoned data requests (due to delay): reduced by 90%

**Baseline**: 3-6 months average; 40% of requests abandoned

**Target**: < 10 working days; < 5% abandonment

---

## Goal-to-Outcome Mapping

### Outcome O-1: Data-Driven Cross-Government Policy Making

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Cross-government policy decisions are informed by data from multiple departments, improving policy design and reducing unintended consequences.

**Business Value**:

- **Strategic Impact**: Better policy outcomes through cross-departmental evidence
- **Financial Impact**: Estimated GBP 100M+ in fraud detection through data matching (based on DWP/HMRC data sharing precedent)
- **Operational Impact**: 80% reduction in data access time enables real-time policy analysis

---

### Outcome O-2: Reduced Duplication and Improved Data Quality

**Supported Goals**: G-1, G-2

**Outcome Statement**: Departments discover and reuse existing data rather than collecting it independently, reducing citizen burden and improving data consistency.

**Business Value**:

- **Financial Impact**: Estimated GBP 15M/year savings from reduced duplicate data collection
- **Citizen Impact**: "Tell us once" — citizens provide data once, it is shared lawfully across government

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Cross-govt efficiency | G-1 | Data catalogue | O-1 | Data-driven policy |
| Minister | SD-1 | Cross-govt efficiency | G-2 | Federated API gateway | O-1 | Data-driven policy |
| Dept Data Leads | SD-2 | Data sovereignty | G-2 | Federated API gateway | O-2 | Reduced duplication |
| CDDO | SD-3 | Standards & spend | G-1 | Data catalogue | O-2 | Reduced duplication |
| ICO | SD-4 | Lawful sharing | G-2 | Federated API gateway | O-1 | Data-driven policy |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Cabinet Office (SD-1) wants rapid cross-government data sharing, but departments (SD-2) want granular control and slow, cautious rollout
  - **Resolution Strategy**: Phased approach — start with low-sensitivity reference data (geographic codes, organisation registers), building trust before progressing to sensitive operational data

- **Conflict 2**: CDDO (SD-3) wants standardised APIs across all departments, but departments have legacy systems with incompatible data models
  - **Resolution Strategy**: Adapter pattern — departments expose data through standardised API specifications, with department-side adapters translating from legacy formats. Adapter development funded centrally.

**Synergies**:

- **Synergy 1**: The federated architecture (G-2) simultaneously satisfies department sovereignty concerns (SD-2) and ICO data minimisation requirements (SD-4)
- **Synergy 2**: The data catalogue (G-1) serves both cross-government sharing (SD-1) and standards compliance (SD-3)

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | Solution Architect | CDO, Cabinet Office | CDDO, NCSC, dept architects | All departments |
| Data sharing policy | Data Governance Lead | SRO | ICO, all department DPOs | Ministers |
| Department onboarding | Onboarding Team | CDO | Department data lead | CDDO |
| Security architecture | Security Architect | Cabinet Office SIRO | NCSC, department SIROs | Programme team |
| API standards | Data Standards Authority | CDDO Director | Department API leads | All departments |

### Escalation Path

1. **Level 1**: Product Manager (day-to-day decisions)
2. **Level 2**: SRO and Programme Board (cross-department disputes, scope, budget)
3. **Level 3**: Cabinet Office Permanent Secretary / CDDO Director (strategic disagreements between departments)

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme SRO | | | |
| Chief Data Officer | | | |
| CDDO Director | | | |

---

## Appendices

### Appendix A: Key References

- National Data Strategy (2020)
- Digital Economy Act 2017 (data sharing powers)
- ICO Data Sharing Code of Practice
- UK GDPR / Data Protection Act 2018
- DCAT (Data Catalog Vocabulary) specification
- GDS API Technical and Data Standards
- Cross-Government Data Ethics Framework
- ARC-000-PRIN-v1.0 (SDG 17 Architecture Principles)

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Cross-Government Data Sharing Platform
**Model**: Claude Opus 4.6
