# Project Requirements: Anti-Fraud Analytics Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Anti-Fraud Analytics Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Anti-Fraud Analytics Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Government Counter Fraud Function, Cabinet Office, HMRC, DWP, NCA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

---

## Executive Summary

### Business Context

The Government Counter Fraud Function estimates annual fraud and error losses across government at GBP 33-58 billion. Individual departments operate fraud detection in isolation, unable to see patterns that cross departmental boundaries. Organised fraud groups exploit this gap — using fabricated identities across tax, benefits, grants, and procurement to extract maximum public funds. The COVID-19 pandemic exposed this vulnerability dramatically, with GBP 4.9 billion in Bounce Back Loan fraud alone. The Counter Fraud Functional Standard (GovS 013) mandates cross-government cooperation, but no central analytics capability exists.

This project delivers a cross-government Anti-Fraud Analytics Platform that enables secure data sharing between departments, applies advanced analytics to detect fraud patterns invisible to individual departments, and generates intelligence-grade referrals for investigation and recovery.

### Objectives

- Establish secure cross-government fraud data sharing across 10+ departments
- Detect at least GBP 100M in previously unidentified cross-government fraud within 24 months
- Maintain false positive rate below 5% to protect citizen rights
- Generate intelligence-grade referrals for NCA and SFO for organised fraud networks
- Comply fully with UK GDPR, DPA 2018, and Digital Economy Act 2017 data sharing provisions

### Expected Outcomes

- GBP 100M+ in newly detected cross-government fraud within 24 months
- 10+ departments actively sharing data
- 50+ organised fraud network referrals to NCA within 24 months
- False positive rate below 5%
- Full ICO compliance with published DPIAs for all data sharing arrangements

### Project Scope

**In Scope**:

- Secure data ingestion platform for cross-government fraud data
- Identity resolution and matching across departmental datasets
- Fraud pattern detection analytics (rules-based and machine learning)
- Fraud alert management and investigation workflow
- Secure intelligence sharing with NCA and SFO
- Data sharing agreement management and compliance tracking
- Departmental dashboard showing fraud risk indicators
- DPIA management and ICO compliance reporting

**Out of Scope**:

- Departmental internal fraud detection systems (departments retain their own)
- Criminal prosecution (NCA/CPS/SFO responsibility)
- Tax investigation (HMRC responsibility)
- Benefits fraud investigation (DWP responsibility)
- Private sector fraud detection

---

## Business Requirements

### BR-1: Cross-Government Fraud Data Sharing

**Description**: The platform must enable secure, lawful data sharing between government departments for the specific purpose of fraud detection and prevention, compliant with the Digital Economy Act 2017, UK GDPR, and DPA 2018.

**Rationale**: Fraud crosses departmental boundaries. A fraudster claiming benefits from DWP while undeclaring income to HMRC is invisible to either department alone. The Counter Fraud Functional Standard mandates cross-government cooperation. The Digital Economy Act 2017 Part 5 provides the legal gateway for data sharing for fraud prevention purposes.

**Success Criteria**:

- 10+ departments sharing data through the platform within 18 months
- Each data sharing arrangement has an approved DPIA and documented legal basis
- Data shared is limited to the minimum necessary for fraud detection (data minimisation)
- All data sharing logged with immutable audit trail

**Priority**: MUST_HAVE
**Stakeholder**: Minister, Head of Counter Fraud Function, HMRC, DWP

---

### BR-2: Cross-Departmental Fraud Pattern Detection

**Description**: The platform must apply analytics to detect fraud patterns that are only visible when data from multiple departments is combined — including identity fraud (same person, different identities across departments), multi-scheme exploitation, and organised fraud networks.

**Rationale**: Individual departments detect fraud within their own data. The unique value of this platform is identifying patterns invisible to any single department. Identity resolution across departments is the critical capability.

**Success Criteria**:

- Detect at least GBP 100M in previously unidentified fraud within 24 months
- Identify 50+ organised fraud networks operating across departmental boundaries
- Analytics produce actionable alerts with sufficient evidence for departmental investigation
- False positive rate maintained below 5%

**Priority**: MUST_HAVE
**Stakeholder**: HMRC, DWP, NCA

---

### BR-3: Privacy and Data Protection Compliance

**Description**: The platform must implement privacy by design, with data minimisation, purpose limitation, proportionality assessment, citizen rights mechanisms, and full DPIA compliance for every data sharing arrangement.

**Rationale**: Cross-government fraud data sharing involves sensitive personal data. ICO engagement and compliance is essential for lawful operation and public trust. Citizens incorrectly flagged must have clear recourse.

**Success Criteria**:

- DPIA completed and approved for each data sharing arrangement
- Data minimisation verified — only necessary data fields shared
- Citizens incorrectly flagged can request human review and correction
- Data retained only for the period necessary for fraud prevention purposes
- Annual ICO audit with no adverse findings

**Priority**: MUST_HAVE
**Stakeholder**: ICO, Minister, Citizens

---

### BR-4: Intelligence-Grade Fraud Referrals

**Description**: The platform must generate referral packages for NCA and SFO that meet evidential standards for criminal investigation of serious and organised fraud.

**Rationale**: Cross-government analytics will identify organised fraud networks that meet the threshold for NCA investigation. Referrals must be evidence-based, structured, and legally compliant.

**Success Criteria**:

- Referral packages include network analysis, financial impact, and evidence chain
- NCA accepts 80%+ of referrals as meeting investigation threshold
- Referrals transmitted through secure intelligence sharing channels
- Data protection basis for law enforcement sharing documented per DPA 2018 LED provisions

**Priority**: SHOULD_HAVE
**Stakeholder**: NCA, SFO

---

## Functional Requirements

### FR-1: Secure Data Ingestion and Storage

**Description**: System must securely ingest data from departmental systems through encrypted channels, store data in an isolated, heavily access-controlled environment, and apply data classification controls.

**Acceptance Criteria**:

- [ ] Given a departmental data feed, when data is transmitted, then it is encrypted in transit (TLS 1.3+) and at rest (AES-256)
- [ ] Given ingested data, when stored, then it is logically separated by source department with department-specific access controls
- [ ] Given a data sharing agreement expiry, when the agreement lapses, then associated data is automatically quarantined pending renewal or deletion

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-2: Identity Resolution and Matching

**Description**: System must perform probabilistic and deterministic identity matching across departmental datasets to identify cases where the same individual appears under different identities, or where multiple claims are linked to the same identity.

**Acceptance Criteria**:

- [ ] Given records from two departments, when identity matching runs, then matches are scored with confidence level (high/medium/low)
- [ ] Given a high-confidence match, when reviewed by an analyst, then the matching evidence (name, date of birth, address, National Insurance number) is presented
- [ ] Given a match flagged as potential identity fraud, when investigated, then the investigation record is linked to all relevant departmental records

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-3: Fraud Pattern Analytics Engine

**Description**: System must apply rules-based and machine learning analytics to detect fraud patterns including multi-scheme exploitation, anomalous claim patterns, organised networks, and trend analysis.

**Acceptance Criteria**:

- [ ] Given configured fraud rules, when data is analysed, then matches are generated with risk scores and explanations
- [ ] Given machine learning models, when they produce fraud predictions, then each prediction includes an explainability output (features that contributed to the score)
- [ ] Given a new fraud pattern identified by analysts, when a new rule is created, then it can be deployed within 24 hours
- [ ] Given analytics output, when fraud alerts are generated, then no personally identifiable information is exposed to users without appropriate security clearance

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-4: Fraud Alert Management and Investigation Workflow

**Description**: System must provide counter fraud analysts with a workflow for triaging, investigating, and resolving fraud alerts, with full audit trail.

**Acceptance Criteria**:

- [ ] Given a fraud alert, when assigned to an analyst, then all relevant cross-departmental data is presented in a single investigation view
- [ ] Given an investigation conclusion, when the analyst records it, then the outcome (confirmed fraud, false positive, insufficient evidence) is logged
- [ ] Given a confirmed fraud case, when the analyst creates a referral, then a structured referral package is generated for the relevant department or NCA

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-5: Data Sharing Agreement Management

**Description**: System must track all data sharing agreements, their legal basis, expiry dates, DPIA status, and compliance requirements, with automated alerts for expiring agreements.

**Acceptance Criteria**:

- [ ] Given a data sharing agreement, when it is registered, then the legal basis, data types, purpose, and expiry are recorded
- [ ] Given an agreement approaching expiry, when 30 days remain, then the agreement owner and platform administrator are alerted
- [ ] Given an expired agreement, when the expiry date passes without renewal, then data ingestion from that department is automatically suspended

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-6: Departmental Fraud Risk Dashboard

**Description**: System must provide departmental counter fraud teams with a dashboard showing fraud risk indicators, alert volumes, investigation outcomes, and recovery values relevant to their department.

**Acceptance Criteria**:

- [ ] Given a departmental user, when they access the dashboard, then they see only data and alerts relevant to their department
- [ ] Given dashboard metrics, when displayed, then they include alert volume, false positive rate, confirmed fraud value, and recovery rate
- [ ] Given trend data, when analysed, then emerging fraud patterns are highlighted for the department

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Performance

**Requirement**: Identity matching batch processing to complete daily runs within 4 hours. Real-time fraud scoring for high-priority data streams within 30 seconds. Dashboard load within 3 seconds.

**Load Conditions**: 50 million records across departments. 500,000 new records per day at peak.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability. Batch processing windows overnight. Real-time scoring 24/7 for departments with continuous transaction streams (HMRC, DWP).

**Priority**: HIGH

---

### NFR-SEC-1: Security (CRITICAL)

**Requirement**: Security Clearance (SC) required for all platform administrators and analysts. Encryption at rest and in transit mandatory. Network isolation from general government networks. Penetration testing quarterly. NCSC Secure by Design assessment. Insider threat monitoring. Break-glass access procedures for emergency data access.

**Data Classification**: OFFICIAL-SENSITIVE (bulk fraud data), potential SECRET elements for organised crime intelligence.

**Priority**: CRITICAL

---

### NFR-SEC-2: Audit and Accountability

**Requirement**: Immutable audit log of all data access, queries, exports, and investigations. Log retained for 7 years. Tamper-evident logging with cryptographic verification. Regular audit by internal audit team.

**Priority**: CRITICAL

---

### NFR-C-1: Data Protection Compliance

**Requirement**: UK GDPR Article 6(1)(e) (public task) as primary legal basis. Digital Economy Act 2017 Part 5 for data sharing gateway. DPIA required for each data sharing arrangement. Data minimisation enforced at ingestion. Purpose limitation enforced — data used only for fraud detection. Citizen rights: right to information, right to human review of automated decisions, right to rectification of incorrect fraud flags.

**Priority**: CRITICAL

---

### NFR-C-2: Algorithmic Transparency

**Requirement**: All fraud scoring algorithms must produce explainable outputs. No fully automated decisions on individual citizens without human review. Algorithm impact assessments conducted for machine learning models. Model bias testing conducted before deployment. Algorithm descriptions published (at sufficient abstraction to prevent gaming).

**Priority**: HIGH

---

## Integration Requirements

### INT-1: HMRC Data Feed

**Purpose**: Tax, PAYE, and self-assessment data for income verification and tax fraud cross-matching.
**Integration Type**: Batch file transfer (encrypted, daily)
**Authentication**: Mutual TLS, dedicated secure channel
**Data Volume**: 40 million records, daily delta updates
**Legal Basis**: Digital Economy Act 2017 Part 5, specific data sharing agreement
**Priority**: MUST_HAVE

---

### INT-2: DWP Data Feed

**Purpose**: Benefits claim data for multi-scheme exploitation detection.
**Integration Type**: Batch file transfer (encrypted, daily)
**Data Volume**: 20 million records, daily delta updates
**Legal Basis**: Digital Economy Act 2017 Part 5, specific data sharing agreement
**Priority**: MUST_HAVE

---

### INT-3: Companies House Data

**Purpose**: Company director and beneficial ownership data for organised fraud network analysis.
**Integration Type**: API (RESTful, real-time)
**Data Volume**: 5 million company records
**Legal Basis**: Publicly available data, no additional legal basis required
**Priority**: SHOULD_HAVE

---

### INT-4: NCA Secure Intelligence Sharing

**Purpose**: Transmit intelligence-grade fraud referrals to NCA for organised crime investigation.
**Integration Type**: Secure messaging (government-approved secure channel)
**Authentication**: SC-cleared operators, hardware token authentication
**Legal Basis**: DPA 2018 Law Enforcement Directive provisions
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Key Data Entities

| Entity | Description | Volume | Classification | Retention |
|--------|-------------|--------|---------------|-----------|
| Person Record | Cross-department identity record | 60 million | OFFICIAL-SENSITIVE | 6 years from last activity |
| Fraud Alert | System-generated fraud indicator | 500,000/year | OFFICIAL-SENSITIVE | 6 years from resolution |
| Investigation | Analyst investigation record | 50,000/year | OFFICIAL-SENSITIVE | 7 years from closure |
| Data Sharing Agreement | Legal agreement metadata | 50 active | OFFICIAL | Active + 6 years |
| Audit Log | All system access and actions | 10 million entries/day | OFFICIAL-SENSITIVE | 7 years |

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Cross-government fraud detected (GBP) | GBP 0 (no capability) | GBP 100M+ | 24 months |
| Active data-sharing departments | 2 (bilateral HMRC-DWP) | 10+ | 18 months |
| False positive rate | N/A | Below 5% | 12 months |
| NCA referral acceptance rate | N/A | 80%+ | 24 months |
| ICO compliance (audit findings) | N/A | Zero adverse findings | Annual |

---

## Dependencies and Risks

| Risk ID | Description | Probability | Impact | Mitigation |
|---------|-------------|-------------|--------|------------|
| R-1 | Data sharing agreements delayed by legal/privacy negotiations | HIGH | HIGH | Early ICO engagement, template agreements, Ministerial escalation |
| R-2 | False positive rate exceeds 5%, undermining analyst trust and citizen rights | MEDIUM | HIGH | Iterative model tuning, human review for all matches, independent audit |
| R-3 | Departments reluctant to share data revealing their own fraud exposure | MEDIUM | HIGH | Ministerial mandate via Counter Fraud Functional Standard, data shared for cross-govt purpose only |
| R-4 | Algorithmic bias in fraud scoring disproportionately affecting demographic groups | MEDIUM | CRITICAL | Bias testing before deployment, independent algorithmic audit, Equality Impact Assessment |
| R-5 | Security breach exposing cross-government fraud intelligence | LOW | CRITICAL | SC clearance, network isolation, encryption, quarterly pen testing, insider threat monitoring |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| GovS 013 | Government Functional Standard for Counter Fraud |
| CFSL | Counter Fraud Standards and Landscape |
| LED | Law Enforcement Directive (Part 3 of DPA 2018) |
| DEA 2017 | Digital Economy Act 2017 — provides data sharing gateways |
| Identity Resolution | Matching records across systems to identify the same individual |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 16 Architecture Principles
- ARC-004-STKE-v1.0 — Anti-Fraud Analytics Platform Stakeholder Analysis
- Government Counter Fraud Functional Standard (GovS 013)
- Digital Economy Act 2017 Part 5

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Anti-Fraud Analytics Platform
**Model**: Claude Opus 4.6
