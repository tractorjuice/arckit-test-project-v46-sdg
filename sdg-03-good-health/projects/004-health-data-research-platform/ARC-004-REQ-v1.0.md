# Project Requirements: Health Data Research Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Health Data Research Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Health Data Research Platform, DHSC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Health Data Research Programme Board, DHSC Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

---

## Executive Summary

### Business Context

The UK possesses one of the world's most valuable health data assets through the NHS — universal coverage, cradle-to-grave records, and standardised coding systems. However, accessing this data for research is fragmented, slow (3-12 months), and inconsistent. The Goldacre Review ("Better, Broader, Safer," 2022) recommended a network of Trusted Research Environments (TREs) where analysis comes to the data, rather than data being extracted and sent to researchers.

This platform will provide a secure, governed, UKSA-accredited Trusted Research Environment where accredited researchers can access de-identified, linked health datasets using modern analytical tools, while data never leaves the secure environment.

### Objectives

- Provide a UKSA-accredited Trusted Research Environment for health data research
- Reduce researcher data access time from 6 months to 6 weeks for standard requests
- Host linked datasets across primary care, secondary care, mortality, genomics, and social determinants
- Implement the Five Safes framework (Safe People, Projects, Settings, Data, Outputs)
- Maintain public trust through transparency, National Data Opt-Out compliance, and PPI governance

### Project Scope

**In Scope**:

- Secure TRE infrastructure (compute, storage, networking in UK sovereign cloud)
- Data ingestion and linkage pipelines for NHS and partner datasets
- Researcher workspace provisioning with analytical tools (R, Python, Stata, Jupyter, GPU compute)
- Automated Information Governance workflow for data access applications
- Secure output checking (statistical disclosure control)
- Researcher accreditation and training
- Public transparency register of approved research projects
- National Data Opt-Out implementation

**Out of Scope**:

- Clinical decision support (separate from research use)
- Individual patient care (no identifiable data for clinical purposes)
- Data collection (uses existing NHS data flows)
- Research ethics review (separate to UKSA/IG governance)

---

## Business Requirements

### BR-1: Trusted Research Environment Infrastructure

**Description**: Provide a secure, isolated compute environment where accredited researchers can analyse health datasets without data leaving the environment.

**Rationale**: The Goldacre Review principle: "analysis comes to the data." Data extraction to researcher laptops creates uncontrollable copies and re-identification risk.

**Success Criteria**:

- No data egress — all analysis performed within the TRE
- Researcher workspace provisioned within 24 hours of approved access
- Compute resources scalable to support 500 concurrent researchers

**Priority**: MUST_HAVE

---

### BR-2: Accelerated Data Access Governance

**Description**: Implement an automated IG workflow that reduces standard research application review from 6 months to 6 weeks while maintaining governance rigour.

**Rationale**: Current data access processes are the primary barrier to health data research. Automated workflows for standard requests can accelerate access without compromising governance.

**Success Criteria**:

- Standard applications processed within 6 weeks (application to data access)
- Automated checks for researcher accreditation, project approval, and data matching
- Full audit trail of all access decisions

**Priority**: MUST_HAVE

---

### BR-3: Multi-Source Data Linkage

**Description**: Link datasets across primary care (GPES), secondary care (HES), mortality (ONS), genomics (Genomics England), prescriptions, and social determinants into research-ready datasets.

**Rationale**: The greatest research value comes from linked datasets that enable longitudinal, multi-dimensional analysis. Individual datasets in isolation have limited research utility.

**Success Criteria**:

- At least 6 core datasets linked via pseudonymised NHS Number
- Linkage quality metrics published (match rate, false positive rate)
- Data dictionary and metadata published for all datasets

**Priority**: MUST_HAVE

---

### BR-4: Five Safes Framework Implementation

**Description**: Implement the UK Statistics Authority Five Safes framework as the governance model for data access.

**Rationale**: UKSA TRE accreditation requires demonstrable compliance with the Five Safes.

**Success Criteria**:

- **Safe People**: All researchers ONS-accredited and trained before access
- **Safe Projects**: All research applications independently reviewed for public benefit
- **Safe Settings**: TRE environment with no data egress, session recording, audit logging
- **Safe Data**: All data de-identified to ONS/UKSA standards before researcher access
- **Safe Outputs**: Statistical disclosure control applied to all outputs before release

**Priority**: MUST_HAVE

---

### BR-5: Public Transparency and National Data Opt-Out

**Description**: Maintain public trust through a published register of approved research projects, regular public engagement, and full compliance with the National Data Opt-Out.

**Rationale**: The care.data programme failed due to insufficient transparency. Public trust is essential — without it, opt-out rates increase and data quality degrades.

**Success Criteria**:

- Public register of all approved research projects updated within 7 days of approval
- National Data Opt-Out applied to all datasets before researcher access
- Annual public engagement events demonstrating research outcomes and societal benefit
- National Data Opt-Out rate remains below 5%

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Professor Williams, Academic Epidemiologist

- **Role**: Professor of epidemiology at a Russell Group university studying diabetes outcomes
- **Goals**: Access linked primary care and hospital data for a 5-year longitudinal cohort study, run complex statistical models in R
- **Pain Points**: Current data access took 9 months, data arrived as CSV files on a laptop, linkage quality unknown
- **Technical Proficiency**: High — expert R/Stata user, needs GPU for ML models

#### Persona 2: Dr Obi, Pharmaceutical Researcher

- **Role**: Data scientist at a pharmaceutical company designing a clinical trial
- **Goals**: Access de-identified population-level data to identify suitable trial sites and estimate patient populations
- **Pain Points**: Commercial access to NHS data is politically sensitive, unclear application process, long approval times
- **Technical Proficiency**: High — Python, PySpark, machine learning

#### Persona 3: Sarah Chen, IG Lead

- **Role**: Information Governance lead reviewing data access applications
- **Goals**: Review applications thoroughly but quickly, ensure compliance with legal basis and Five Safes, maintain audit trail
- **Pain Points**: Manual paper-based review process, inconsistent standards across applications, backlog of 40+ applications
- **Technical Proficiency**: Medium — uses IG management systems, not analytical tools

---

### Functional Requirements Detail

#### FR-1: Researcher Workspace Provisioning

**Description**: The system must provision isolated virtual desktop environments for accredited researchers with pre-installed analytical tools, access only to approved datasets, and no internet connectivity or data egress capability.

**Acceptance Criteria**:

- [ ] Given an approved research application, when workspace is provisioned, then the researcher can log in within 24 hours with all approved datasets accessible
- [ ] Given a researcher workspace, when the researcher attempts to copy data to clipboard, USB, or network, then the action is blocked and audit-logged
- [ ] Given a researcher workspace, when the researcher requires GPU compute for ML training, then GPU resources can be provisioned within 4 hours

**Priority**: MUST_HAVE

---

#### FR-2: Automated IG Application Workflow

**Description**: The system must provide a digital application workflow for data access requests with automated checks, reviewer assignment, and progress tracking.

**Acceptance Criteria**:

- [ ] Given a researcher submits an application, when automated checks run, then researcher accreditation, institutional agreement, and ethics approval are validated within 1 business day
- [ ] Given an application passes automated checks, when assigned to IG reviewer, then the reviewer receives the application with pre-populated compliance checklist
- [ ] Given an IG reviewer approves an application, when approval is granted, then workspace provisioning is triggered automatically

**Priority**: MUST_HAVE

---

#### FR-3: Data Linkage Pipeline

**Description**: The system must link datasets from multiple sources using pseudonymised NHS Number, with linkage quality metrics and deterministic/probabilistic matching.

**Acceptance Criteria**:

- [ ] Given primary care and secondary care datasets, when linkage is performed, then records are linked via pseudonymised NHS Number with > 95% match rate
- [ ] Given linked datasets, when quality metrics are calculated, then match rate, false positive rate, and false negative rate are published in the data dictionary
- [ ] Given National Data Opt-Out list, when applied to linked datasets, then all opted-out patients are excluded before researcher access

**Priority**: MUST_HAVE

---

#### FR-4: Statistical Disclosure Control (Safe Outputs)

**Description**: All outputs from the TRE (tables, charts, model coefficients, aggregate statistics) must pass through statistical disclosure control before release to prevent re-identification.

**Acceptance Criteria**:

- [ ] Given a researcher submits an output for release, when SDC review is performed, then tables with cell counts < 10 are suppressed
- [ ] Given an output contains potential re-identification risk, when flagged, then it is held for manual SDC review
- [ ] Given an output passes SDC, when released, then the output is logged with researcher identity, project, and release date

**Priority**: MUST_HAVE

---

#### FR-5: Public Research Register

**Description**: A public-facing website listing all approved research projects, their purpose, datasets used, and published findings.

**Acceptance Criteria**:

- [ ] Given a research application is approved, when the register is updated, then the project summary, principal investigator, institutional affiliation, and datasets accessed are published within 7 days
- [ ] Given a research project publishes findings, when the researcher notifies the platform, then the publication link is added to the register entry
- [ ] Given the public accesses the register, when they search, then they can filter by disease area, dataset, institution, and date

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Security Requirements

#### NFR-SEC-1: Zero Data Egress

**Requirement**: The TRE must have no technical pathway for data to leave the environment. No internet access, no clipboard, no USB, no screen sharing, no email from within the TRE.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Session Recording and Audit

**Requirement**: All researcher sessions must be audit-logged with query history, data accessed, and outputs generated. Session recording capability for forensic investigation.

**Priority**: CRITICAL

---

### Availability Requirements

#### NFR-A-1: Availability Target

**Requirement**: 99.5% availability during standard research hours (Monday-Friday 8am-8pm). Planned maintenance windows acceptable outside these hours.

**Priority**: HIGH

---

### Scalability Requirements

#### NFR-S-1: Concurrent Researcher Support

**Requirement**: Support 500 concurrent researcher sessions with independent compute resources.

**Priority**: HIGH

---

### Compliance Requirements

#### NFR-C-1: UKSA TRE Accreditation

**Requirement**: Full compliance with UK Statistics Authority Trusted Research Environment accreditation standards including Five Safes framework.

**Priority**: CRITICAL

---

#### NFR-C-2: UK GDPR — Lawful Basis for Research

**Requirement**: All data processing must have a documented lawful basis under UK GDPR Article 6(1)(e) (public task) and Article 9(2)(j) (scientific research), with appropriate safeguards under Section 19 DPA 2018.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: GPES (General Practice Extraction Service)

**Purpose**: Primary care data from GP clinical systems.

**Data Exchanged**: Pseudonymised patient records (diagnoses, prescriptions, consultations)

**Priority**: CRITICAL

---

### INT-2: Hospital Episode Statistics (HES)

**Purpose**: Secondary care hospital admission, outpatient, and A&E data.

**Data Exchanged**: Pseudonymised episode-level hospital activity data

**Priority**: CRITICAL

---

### INT-3: ONS Mortality Data

**Purpose**: Death registrations linked to cause of death (ICD-10 coded).

**Priority**: CRITICAL

---

### INT-4: Genomics England Research Environment

**Purpose**: Genomic sequencing data linked to clinical records.

**Priority**: SHOULD_HAVE

---

### INT-5: National Data Opt-Out Service

**Purpose**: Apply patient opt-out preferences before any data is made available to researchers.

**Priority**: CRITICAL

---

## Data Requirements

### DR-1: Pseudonymised Patient Research Record

**Description**: Linked, de-identified patient-level record combining data from multiple sources.

**Data Classification**: OFFICIAL-SENSITIVE (de-identified but potentially re-identifiable through linkage)

**Data Retention**: As specified in research protocol and Data Sharing Agreement (typically duration of study + 10 years)

---

### DR-2: Research Application and Governance Record

**Description**: Full audit trail of data access applications, reviews, approvals, and conditions.

**Data Classification**: OFFICIAL

**Data Retention**: 10 years after project completion

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Data access time | 6 months | 6 weeks | 12 months | Application tracking |
| UKSA accreditation | Not accredited | Accredited | 12 months post-launch | UKSA assessment |
| Concurrent researchers | N/A | 500 | Go-live | Platform monitoring |
| National Data Opt-Out rate | 3.3% | < 5% (maintained) | Ongoing | NHS Digital |
| Public register entries | 0 | 100+ projects | 18 months | Register analytics |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Goldacre Review | Report | DHSC | TRE architecture, Five Safes | N/A — external reference |
| UKSA TRE Standards | Standard | UKSA | Accreditation criteria | N/A — external reference |
| National Data Opt-Out | Policy | NHS Digital | Patient opt-out mechanism | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Health Data Research Platform
**Model**: Claude Opus 4.6
