# Project Requirements: Modern Slavery Reporting System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Modern Slavery Reporting System (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Modern Slavery Reporting System |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MS Reporting Programme Board, Home Office Digital, NCA, IASC, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Modern Slavery Transparency Compliance platform, replacing the current GOV.UK Modern Slavery Statement Registry with a structured data platform enabling compliance monitoring, supply chain risk analysis, and law enforcement intelligence sharing.

---

## Executive Summary

### Business Context

The Modern Slavery Act 2015, section 54, requires commercial organisations with turnover exceeding GBP 36 million to publish an annual transparency statement describing the steps they have taken to prevent modern slavery in their operations and supply chains. Approximately 17,000 organisations are in scope. The current GOV.UK Modern Slavery Statement Registry accepts unstructured PDF uploads, making it impossible to systematically analyse compliance quality, identify supply chain patterns, or support law enforcement investigations. The Independent Anti-Slavery Commissioner has repeatedly called for a platform that enables "comparison, analysis, and accountability at scale."

### Objectives

- Transition 90% of in-scope organisations to structured data submission within 24 months
- Enable automated cross-referencing of statements with Companies House, trade data, and sector risk profiles
- Deliver law enforcement data sharing gateway to NCA handling OFFICIAL-SENSITIVE intelligence
- Publish public transparency dashboard for civil society accountability
- Automate compliance monitoring and escalation for non-submitting organisations

### Expected Outcomes

- Step change in transparency — statements become comparable, not just available
- 95% on-time compliance rate (currently estimated at 60-70%)
- Identification of 500+ high-risk supply chain patterns per year for enforcement prioritisation
- Reduced modern slavery in UK supply chains through deterrence and detection

### Project Scope

**In Scope**:
- Structured modern slavery statement submission portal
- Compliance monitoring and enforcement escalation engine
- Supply chain risk analysis and cross-referencing
- Law enforcement data sharing gateway (NCA, GLAA, police forces)
- Public transparency dashboard
- Whistleblower/anonymous tip-off channel
- Companies House and trade data integration

**Out of Scope**:
- Criminal investigation case management (NCA's own systems)
- Victim support services (Salvation Army contract, separate)
- International modern slavery reporting (other jurisdictions)
- Section 1-53 enforcement of Modern Slavery Act (criminal offences)

---

## Business Requirements

### BR-001: Structured Data Statement Submission

**Description**: The system must enable organisations to submit modern slavery statements as structured data using a defined schema, replacing the current unstructured PDF upload. The schema must capture: steps taken, supply chain description, risk areas identified, due diligence processes, training provided, and effectiveness metrics.

**Rationale**: The current PDF-based system makes it impossible to analyse, compare, or systematically review statements. Structured data enables the IASC, NCA, and civil society to assess compliance quality at scale.

**Success Criteria**:
- 90% of statements submitted as structured data within 24 months
- Schema covers all six areas required by section 54(5) of the Modern Slavery Act
- Average submission time under 45 minutes for returning organisations (with pre-populated fields)
- PDF upload retained as fallback with OCR extraction into structured fields

**Priority**: MUST_HAVE

---

### BR-002: Compliance Monitoring and Escalation

**Description**: The system must automatically identify organisations that are in scope (GBP 36M+ turnover) but have not submitted a statement, and escalate non-compliance through defined enforcement pathways.

**Rationale**: Currently there is no systematic identification of non-compliant organisations. The government does not know with certainty how many organisations are in scope or which have not submitted. Cross-referencing with Companies House accounts data can identify in-scope organisations.

**Success Criteria**:
- 95% of in-scope organisations identified through Companies House cross-referencing
- Automated reminders sent 3 months, 1 month, and 1 week before submission deadline
- Non-compliance escalation to the Modern Slavery Unit within 30 days of deadline
- On-time submission rate reaches 95% (from estimated 60-70%)

**Priority**: MUST_HAVE

---

### BR-003: Supply Chain Risk Analysis

**Description**: The system must cross-reference modern slavery statements with external data sources (Companies House, HMRC trade data, sector risk profiles, geographic risk indices) to generate risk scores that prioritise enforcement attention.

**Rationale**: Not all supply chains carry equal risk. Agriculture, food processing, construction, textiles, and domestic work are high-risk sectors. Supply chains sourced from certain geographies (Xinjiang, parts of South-East Asia, Sub-Saharan Africa) carry elevated risk. Automated risk scoring enables targeted enforcement rather than random checking.

**Success Criteria**:
- Risk scoring algorithm covers sector, geography, supply chain complexity, and statement quality
- 500+ high-risk patterns identified per year
- Risk methodology reviewed and endorsed by IASC and domain experts
- False positive rate below 30% (validated by NCA assessment of flagged cases)

**Priority**: SHOULD_HAVE

---

### BR-004: Law Enforcement Data Sharing Gateway

**Description**: The system must provide a secure data sharing gateway enabling NCA, GLAA, and territorial police forces to access supply chain data, risk scores, and cross-referenced intelligence at OFFICIAL-SENSITIVE classification, with full audit trail.

**Rationale**: NCA's Modern Slavery and Human Trafficking Unit needs structured supply chain data to inform intelligence assessments and investigations. Current public statements are insufficiently structured for intelligence use. The gateway must be architecturally separated from the public platform.

**Success Criteria**:
- Secure gateway operational handling OFFICIAL-SENSITIVE data
- NCA and GLAA access operational within 6 months of platform launch
- Full audit trail of all law enforcement queries
- DPIA completed and approved for intelligence sharing

**Priority**: MUST_HAVE

---

### BR-005: Public Transparency Dashboard

**Description**: The system must publish a public dashboard enabling citizens, journalists, NGOs, and researchers to search, compare, and analyse modern slavery statements by sector, geography, turnover band, and quality metrics.

**Rationale**: Transparency is the core purpose of section 54. The dashboard enables civil society accountability and creates reputational incentive for compliance quality.

**Success Criteria**:
- Dashboard searchable by organisation name, sector, geography, and turnover
- Year-on-year comparison for individual organisations
- Sector-level benchmarking showing average compliance quality
- Open data API for researchers and NGOs

**Priority**: MUST_HAVE

---

### BR-006: Anonymous Tip-Off Channel

**Description**: The system must provide a secure, anonymous channel for whistleblowers, workers, and the public to report suspected modern slavery in supply chains, with reports triaged and routed to appropriate enforcement agencies.

**Rationale**: Workers within exploitative supply chains are often the first to identify modern slavery. A secure, anonymous reporting channel lowers the barrier to reporting. The channel must protect reporter identity even from system administrators.

**Success Criteria**:
- Anonymous submission requiring no personal data
- End-to-end encryption of tip-off content
- Triage workflow routing reports to NCA, GLAA, or relevant police force
- Reporter able to check status of their report via anonymous token

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### FR-001: Structured Statement Submission

**Description**: Guided submission flow capturing structured data across six statutory areas.

**Acceptance Criteria**:
- [ ] Given an in-scope organisation, when they begin submission, then company data is pre-populated from Companies House
- [ ] Given the six statutory areas, when the user completes each section, then structured data is captured (not free text only) with drop-down selections for risk categories, geographies, and due diligence measures
- [ ] Given a returning organisation, when they begin a new year's statement, then last year's responses are pre-populated for review and update
- [ ] Given an organisation unable to complete structured submission, when they upload a PDF, then OCR extracts key fields for structured storage

**Priority**: MUST_HAVE

---

### FR-002: In-Scope Organisation Identification

**Description**: Automatically identify organisations in scope by cross-referencing Companies House accounts data with the GBP 36M turnover threshold.

**Acceptance Criteria**:
- [ ] Given Companies House annual accounts data, when turnover exceeds GBP 36M, then the organisation is flagged as in-scope
- [ ] Given group structures, when a parent company has GBP 36M+ consolidated turnover, then all subsidiaries are flagged
- [ ] Given an organisation newly exceeding the threshold, when identified, then they receive notification of their obligation within 30 days

**Priority**: MUST_HAVE

---

### FR-003: Compliance Tracking and Escalation

**Description**: Track submission deadlines and escalate non-compliance.

**Acceptance Criteria**:
- [ ] Given a financial year end, when the submission deadline approaches (6 months after FY end), then automated reminders are sent at 3 months, 1 month, and 1 week
- [ ] Given non-submission 30 days after deadline, when escalation triggers, then a referral is created for the Modern Slavery Unit
- [ ] Given the IASC dashboard, when viewing compliance rates, then sector-level and overall compliance percentages are displayed in real-time

**Priority**: MUST_HAVE

---

### FR-004: Risk Scoring Engine

**Description**: Generate supply chain risk scores using multi-factor analysis.

**Acceptance Criteria**:
- [ ] Given a submitted statement, when the risk engine analyses it, then a risk score (0-100) is generated based on sector risk, geographic risk, supply chain complexity, and statement quality
- [ ] Given a high-risk score (>70), when flagged, then the organisation appears on the NCA priority list
- [ ] Given the risk methodology, when it is updated, then all historical statements are re-scored and the methodology change is logged

**Priority**: SHOULD_HAVE

---

### FR-005: Law Enforcement Access Portal

**Description**: Secure portal for NCA, GLAA, and police to query supply chain data and risk scores.

**Acceptance Criteria**:
- [ ] Given an NCA analyst, when they authenticate (MFA + role-based access), then they can search by organisation, sector, geography, and risk score
- [ ] Given a query, when results are returned, then cross-referenced intelligence (Companies House directors, trade routes, related entities) is included
- [ ] Given all queries, when logged, then a complete audit trail captures user, query parameters, results viewed, and data exported

**Priority**: MUST_HAVE

---

### FR-006: Public Transparency Dashboard

**Description**: Public-facing dashboard for searching and comparing statements.

**Acceptance Criteria**:
- [ ] Given a citizen, when they search by organisation name, then the latest statement is displayed with structured data visualisation
- [ ] Given a journalist, when they filter by sector, then sector-level compliance quality comparison is shown
- [ ] Given an API consumer, when they query the open data API, then structured statement data is returned in JSON format

**Priority**: MUST_HAVE

---

### FR-007: Anonymous Tip-Off Submission

**Description**: Secure anonymous reporting channel.

**Acceptance Criteria**:
- [ ] Given a whistleblower, when they submit a tip-off, then no personal data is required
- [ ] Given a submission, when it is stored, then content is end-to-end encrypted at rest
- [ ] Given a tip-off token, when the reporter returns to check status, then they see the current triage status without revealing their identity

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### NFR-SEC-001: Dual Classification Architecture

**Requirement**: The public compliance platform must operate at OFFICIAL. The law enforcement data sharing gateway must operate at OFFICIAL-SENSITIVE. These must be architecturally separated with a controlled data gateway between them.

**Priority**: MUST_HAVE

---

### NFR-SEC-002: Whistleblower Protection

**Requirement**: Anonymous tip-off system must provide end-to-end encryption, no IP logging, no metadata that could identify the reporter, and secure token-based status checking. System administrators must not be able to identify reporters.

**Priority**: MUST_HAVE

---

### NFR-SEC-003: Audit Trail

**Requirement**: Complete, tamper-evident audit trail for all compliance actions, law enforcement queries, and data exports. Audit logs retained for 7 years. Cryptographic hashing for log integrity.

**Priority**: MUST_HAVE

---

### NFR-A-001: Availability

**Requirement**: Public platform: 99.9% availability. Law enforcement gateway: 99.95% availability (time-sensitive intelligence). Tip-off channel: 99.9% availability.

**Priority**: MUST_HAVE

---

### NFR-P-001: Statement Submission Performance

**Requirement**: Statement submission form loads within 2 seconds. PDF OCR extraction completes within 60 seconds. Risk score calculation completes within 30 seconds of submission.

**Priority**: MUST_HAVE

---

### NFR-C-001: Modern Slavery Act Compliance

**Requirement**: Full compliance with Modern Slavery Act 2015, section 54, including coverage of all six statutory areas in the structured schema.

**Priority**: MUST_HAVE

---

### NFR-C-002: UK GDPR — Whistleblower Data

**Requirement**: Tip-off data processing under Article 6(1)(e) (public task). DPIA completed for whistleblower data processing. Data minimisation — no personal data collected from reporters. Reported data about third parties processed under law enforcement exemption where appropriate.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Companies House

**Purpose**: Identify in-scope organisations and pre-populate company data
**Integration Type**: Daily batch (turnover threshold monitoring) + real-time API (company data lookup)
**Data Exchanged**: Company registration, SIC code, turnover, directors, group structure
**Priority**: MUST_HAVE

---

### INT-002: HMRC Trade Data

**Purpose**: Cross-reference supply chain declarations with actual trade data (import/export by country and commodity)
**Integration Type**: Quarterly batch under data sharing agreement
**Data Exchanged**: Aggregated import data by company (country of origin, commodity code, value)
**Priority**: SHOULD_HAVE

---

### INT-003: NCA Intelligence Systems

**Purpose**: Law enforcement data sharing
**Integration Type**: Secure API (OFFICIAL-SENSITIVE)
**Data Exchanged**: Risk scores, structured statement data, cross-referenced entity data
**Authentication**: Mutual TLS, MFA, role-based access
**Priority**: MUST_HAVE

---

### INT-004: GLAA Licensing Database

**Purpose**: Cross-reference modern slavery risk with GLAA licence status for regulated sectors
**Integration Type**: Reference data feed
**Data Exchanged**: GLAA licence holder data, compliance history
**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Law enforcement gateway must be hosted on Home Office secure infrastructure (separate from public platform)
**TC-2**: Whistleblower channel must be architecturally isolated from systems that log IP addresses
**TC-3**: All infrastructure on UK sovereign cloud

### Business Constraints

**BC-1**: Budget capped at GBP 10M over 3 years
**BC-2**: IASC endorsement required before public launch
**BC-3**: NCA data sharing agreement required before law enforcement gateway goes live

### Assumptions

**A-1**: Companies House accounts data is sufficiently current to identify in-scope organisations (filed annually)
**A-2**: Organisations will transition to structured submission if the process is simpler than PDF upload
**A-3**: HMRC will agree to share aggregated trade data under existing legal gateway

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-005-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals, conflicts | `projects/005-modern-slavery-reporting-system/ARC-005-STKE-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 6, 7, 11 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Modern Slavery Act 2015 | Legislation | UK Parliament | Section 54 transparency | https://www.legislation.gov.uk/ukpga/2015/30 |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Modern Slavery Reporting System
**Model**: Claude Opus 4.6
