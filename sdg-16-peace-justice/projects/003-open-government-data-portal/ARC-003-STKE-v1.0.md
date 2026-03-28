# Stakeholder Drivers & Goals Analysis: Open Government Data Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Open Government Data Portal (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Open Government Programme, Cabinet Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office Transparency Team, CDDO, Government Data Quality Hub |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document analyses stakeholders for the Open Government Data Portal — a platform for publishing government transparency data, open datasets, and accountability information aligned with the UK's Open Government Partnership National Action Plan and SDG 16 commitments to transparent, accountable institutions.

### Key Findings

The Open Government Data Portal sits at the intersection of transparency advocacy, departmental compliance burden, and data quality concerns. The strongest alignment exists around the UK's international commitment to open government (OGP National Action Plan) — all stakeholders agree the UK must demonstrate leadership. The most significant conflict is between transparency advocates wanting maximum data publication and departmental data owners concerned about data quality, resource burden, and potential misinterpretation of published data.

### Critical Success Factors

- Achieve 4-star open data maturity for at least 80% of published datasets within 18 months
- Onboard 15+ government departments as active data publishers within 12 months
- Deliver a developer-friendly API that external organisations actively use
- Demonstrate compliance with the UK's 5th Open Government Partnership National Action Plan
- Maintain data quality standards that prevent publication of inaccurate or misleading data

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the principle of open government, but significant practical tensions between publication ambition and departmental capacity, between data freshness and data quality, and between maximising openness and protecting sensitive information.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for the Cabinet Office | Minister | HIGH | HIGH | Manage Closely — OGP commitments, transparency agenda |
| Cabinet Office Permanent Secretary | Accounting Officer | HIGH | MEDIUM | Keep Satisfied — Programme spend, governance |
| Head of Government Transparency | Programme lead | HIGH | HIGH | Manage Closely — Strategy, OGP delivery |
| CDDO | Digital standards | HIGH | HIGH | Manage Closely — Data standards, API design |
| Government Data Quality Hub | Data standards | MEDIUM | HIGH | Keep Informed — Quality frameworks, metadata |
| Departmental Data Leads | Data publication owners | MEDIUM | MEDIUM | Keep Informed — Onboarding, data supply |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Open Government Partnership (OGP) | International | International commitments | MEDIUM | HIGH |
| Information Commissioner's Office (ICO) | Regulator | FOI and data protection oversight | HIGH | MEDIUM |
| NAO | Parliament | Value for money, accountability data | HIGH | HIGH |
| Open Data Institute (ODI) | NGO | Open data advocacy and standards | LOW | HIGH |
| Transparency International UK | NGO | Anti-corruption, transparency | LOW | HIGH |
| mySociety | Charity | Civic technology, data reuse | LOW | HIGH |
| Academic researchers | Universities | Data consumers | LOW | HIGH |
| Journalists | Media | Data-driven investigations | LOW | HIGH |
| Public Accounts Committee | Parliament | Accountability and scrutiny | HIGH | MEDIUM |
| Citizens | Public | Open data beneficiaries | LOW | MEDIUM |

---

## Stakeholder Drivers Analysis

### SD-1: Minister for the Cabinet Office — International Leadership on Open Government

**Stakeholder**: Minister for the Cabinet Office

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate UK leadership on open government and transparency through delivery of the 5th OGP National Action Plan commitments, maintaining the UK's reputation as a global leader in open data and enabling positive reporting to the OGP Independent Reporting Mechanism.

**Context & Background**:
The UK was a founding member of the Open Government Partnership in 2011 and has historically been a global leader in open data (ranked in the top 5 on the Open Data Barometer). However, progress has stalled — the 4th National Action Plan received criticism for slow implementation. The Minister needs demonstrable delivery against the 5th National Action Plan to maintain the UK's international standing and credibility at OGP summits.

**Driver Intensity**: HIGH

**Enablers**:

- Modern, discoverable open data platform that showcases UK datasets
- Dashboard showing NAP commitment progress and dataset publication metrics
- High-profile dataset releases that demonstrate transparency (spending, contracts, beneficial ownership)

**Blockers**:

- Departmental reluctance to publish data due to quality concerns or resource constraints
- Legacy data.gov.uk platform limitations preventing modern data discovery
- FOI request volumes suggesting proactive publication gaps

**Related Stakeholders**: OGP (international reporting), CDDO (standards), NAO (accountability), Transparency International (advocacy)

---

### SD-2: NAO and Public Accounts Committee — Accountability and Scrutiny Data

**Stakeholder**: National Audit Office and Public Accounts Committee

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Access timely, accurate, machine-readable government financial and performance data to enable effective parliamentary scrutiny and value-for-money assessment, reducing reliance on bespoke data requests.

**Context & Background**:
The NAO conducts approximately 60 value-for-money studies per year, each requiring extensive data gathering from departments. Currently, much of this data is obtained through bespoke requests, which is slow and resource-intensive. If key accountability data (spending, contracts, workforce, performance) were proactively published as high-quality open data, scrutiny would be faster and more comprehensive. The Public Accounts Committee has repeatedly called for better transparency data.

**Driver Intensity**: HIGH

**Enablers**:

- Standardised, machine-readable spending and contracts data published proactively
- API access to government financial datasets
- Consistent metadata and data quality standards across departments

**Blockers**:

- Departments publishing low-quality or delayed data that cannot be relied upon for audit
- Inconsistent data formats across departments
- Data published as PDFs or images rather than machine-readable formats

**Related Stakeholders**: Minister (transparency), Departmental Data Leads (publishers), Transparency International (advocacy)

---

### SD-3: Open Data Institute and Civic Technology Community — Maximising Data Reuse

**Stakeholder**: Open Data Institute, mySociety, academic researchers

**Driver Category**: STRATEGIC / CUSTOMER

**Driver Statement**: Access government data through modern, developer-friendly APIs with comprehensive metadata, standard formats, and permissive licensing, enabling the creation of public-benefit applications, research, and civic technology.

**Context & Background**:
The UK civic technology community has built valuable public services on open data — TheyWorkForYou, WhatDoTheyKnow, FixMyStreet — but frequently encounters barriers: poor data quality, inconsistent formats, broken download links, missing metadata, and restrictive licensing. The ODI 5-star open data model provides a clear maturity framework. Most government datasets currently achieve 2-3 stars. The community wants 4-5 star data (linked, machine-readable, standardised URIs).

**Driver Intensity**: MEDIUM

**Enablers**:

- RESTful APIs for all published datasets with documentation
- Standard formats (CSV, JSON, GeoJSON) with consistent column naming
- Open Government Licence (OGL) applied by default
- Comprehensive metadata including update frequency, data dictionary, and quality indicators
- Persistent URIs for datasets enabling linked data approaches

**Blockers**:

- Data published as one-off dumps rather than maintained, versioned datasets
- Poor or missing metadata making data unusable without domain expertise
- Proprietary formats (Excel with macros, password-protected files)
- Broken links and abandoned datasets

**Related Stakeholders**: Academic researchers (analysis), journalists (investigation), Citizens (ultimate beneficiaries)

---

### SD-4: Departmental Data Leads — Manageable Publication Burden

**Stakeholder**: Data leads across 15+ government departments

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Publish open data in a way that is proportionate to departmental resources, does not create excessive workload, and does not expose the department to criticism for data quality issues, misinterpretation, or inadvertent disclosure of sensitive information.

**Context & Background**:
Departments already face significant data demands — FOI requests, parliamentary questions, ministerial briefings, NAO audit requests. Adding proactive open data publication creates additional burden. Data leads are concerned about publishing data that may be misinterpreted, taken out of context, or used to generate negative media coverage. They also face genuine data quality challenges — departmental data is often held in legacy systems with poor quality controls.

**Driver Intensity**: MEDIUM

**Enablers**:

- Automated data pipeline from departmental systems to the portal (reducing manual effort)
- Clear data quality framework with defined thresholds (not perfection, but fitness for purpose)
- Standardised metadata templates that are quick to complete
- Central support team to help departments prepare data for publication
- Clear guidance on handling data that may be misinterpreted (contextual notes, caveats)

**Blockers**:

- Requirement to publish data that does not exist in machine-readable form in departmental systems
- No additional budget or staff for open data publication
- Lack of senior departmental sponsorship for transparency (seen as "nice to have")
- Fear of media criticism for publishing imperfect data

**Related Stakeholders**: CDDO (standards), ICO (FOI compliance), NAO (accountability expectations), Minister (political expectations)

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 4-Star Open Data Maturity for 80% of Published Datasets

**Derived From Drivers**: SD-1, SD-2, SD-3
**Goal Owner**: Head of Government Transparency
**Goal Statement**: Achieve 4-star open data maturity (machine-readable, open format, URI-identified, linked) for at least 80% of datasets published on the portal within 18 months.

**Success Metrics**:

- **Primary Metric**: Percentage of datasets at 4-star maturity or above
- **Baseline**: Estimated 30% of current data.gov.uk datasets at 4-star
- **Target**: 80% at 4-star or above
- **Measurement Method**: Automated data quality assessment on portal

---

### Goal G-2: Onboard 15+ Departments as Active Publishers

**Derived From Drivers**: SD-1, SD-4
**Goal Owner**: Head of Government Transparency
**Goal Statement**: Onboard at least 15 government departments as active data publishers (publishing at least monthly) within 12 months, with automated data pipelines where possible.

**Success Metrics**:

- **Primary Metric**: Number of departments actively publishing (monthly or more frequently)
- **Baseline**: Approximately 8 departments publishing regularly on data.gov.uk
- **Target**: 15+ departments
- **Measurement Method**: Portal publishing analytics

---

### Goal G-3: Developer API Adoption — 100+ Active External Applications

**Derived From Drivers**: SD-3
**Goal Owner**: CDDO
**Goal Statement**: Achieve 100+ active external applications consuming portal APIs within 18 months.

**Success Metrics**:

- **Primary Metric**: Number of registered API consumers with >100 requests/month
- **Target**: 100+ active applications
- **Measurement Method**: API management platform analytics

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Minister | SD-1 | International OGP leadership | G-1 | 4-star maturity 80% |
| Minister | SD-1 | International OGP leadership | G-2 | 15+ dept publishers |
| NAO/PAC | SD-2 | Accountability data for scrutiny | G-1 | 4-star maturity 80% |
| ODI/civic tech | SD-3 | Developer-friendly data reuse | G-3 | 100+ API consumers |
| Dept data leads | SD-4 | Manageable publication burden | G-2 | 15+ dept publishers |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Transparency advocates (SD-1, SD-2, SD-3) want maximum data publication at highest quality, while departmental data leads (SD-4) want manageable burden and protection from misinterpretation criticism.
  - **Resolution Strategy**: Tiered publication model — mandatory publication of high-value reference datasets (spending, contracts, workforce) with central support; voluntary publication of additional datasets with quality guidance. Quality caveats and contextual notes permitted alongside data.

- **Conflict 2**: NAO (SD-2) wants accountability data that may be politically sensitive, while departments resist proactive publication of performance data that could attract negative scrutiny.
  - **Resolution Strategy**: Central mandate from Minister for defined accountability datasets, backed by Ministerial Direction if necessary. FOI analysis to identify frequently requested data that should be proactively published.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK 5th OGP National Action Plan | Policy | Cabinet Office | Transparency commitments | N/A — external reference |
| Open Data Charter | International | OGP | Open data principles | N/A — external reference |
| 5-star Open Data Model | Framework | Tim Berners-Lee/ODI | Data maturity levels | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Open Government Data Portal
**Model**: Claude Opus 4.6
