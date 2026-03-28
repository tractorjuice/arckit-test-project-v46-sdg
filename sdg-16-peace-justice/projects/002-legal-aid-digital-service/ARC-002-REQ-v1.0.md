# Project Requirements: Legal Aid Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Legal Aid Digital Service (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Legal Aid Digital Service |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | LAA Executive Board, MoJ Digital, CDDO, Law Society |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Legal Aid Digital Service — a platform enabling citizens and their legal representatives to apply for legal aid, undergo eligibility assessment via the statutory means test (as revised by the Means Test Review 2023), and receive determinations within 5 working days.

---

## Executive Summary

### Business Context

The Legal Aid Agency (LAA) administers the GBP 1.7 billion annual legal aid fund, processing approximately 300,000 applications per year across criminal and civil categories. The current application process is predominantly paper-based, with caseworkers manually entering data, verifying financial information through postal correspondence, and calculating eligibility using spreadsheet-based tools. Average determination time exceeds 20 working days for civil cases, during which applicants may be unable to access legal representation for urgent matters including domestic abuse, housing eviction, and immigration detention.

The Means Test Review 2023 raised income and capital thresholds and simplified some calculation rules, but the current systems cannot implement these changes efficiently. An estimated 2 million additional citizens become eligible under the revised thresholds.

### Objectives

- Implement the Means Test Review 2023 rules accurately in a digital rules engine
- Reduce application-to-determination time from 20+ working days to under 5 working days
- Reduce solicitor application completion time from 2 hours to under 30 minutes
- Provide real-time eligibility pre-check for citizens and legal advisers
- Integrate with HMRC and DWP for automated income and benefits verification

### Expected Outcomes

- 75% reduction in determination time (20 days to 5 days)
- 75% reduction in solicitor application time (120 minutes to 30 minutes)
- 99.9% means test calculation accuracy
- 2 million additional citizens assessed as eligible under revised thresholds
- 40% reduction in caseworker time per application through automated verification

### Project Scope

**In Scope**:

- Digital application portal for solicitors, barristers, and citizens
- Means test rules engine implementing LASPO Act 2012 (as amended) and Means Test Review 2023 rules
- Automated income verification via HMRC Real Time Information
- Benefits status verification via DWP Universal Credit data
- Real-time eligibility pre-check (indicative, non-binding)
- LAA caseworker review and determination workflow
- Integration with HMCTS case management for legal aid status at court
- Appeal and review mechanism for refused applications
- Reporting and management information

**Out of Scope**:

- Legal aid billing and payment system (separate LAA programme)
- Provider contract management
- Quality assurance of legal services delivered under legal aid
- Changes to the statutory means test rules themselves (policy responsibility of MoJ)

---

## Business Requirements

### BR-1: Digital Means Test Implementation

**Description**: The system must implement the complete statutory means test for legal aid eligibility as defined by LASPO 2012 (as amended), the Civil Legal Aid (Financial Resources and Payment for Services) Regulations 2013 (as amended by the Means Test Review 2023), and the Criminal Legal Aid (Financial Resources) Regulations 2013.

**Rationale**: The means test is the statutory gateway to legal aid. Accurate, rapid assessment is essential for access to justice. The revised 2023 thresholds expand eligibility to an estimated 2 million additional citizens.

**Success Criteria**:

- 99.9% calculation accuracy verified against test cases provided by MoJ Policy
- All Means Test Review 2023 threshold changes implemented correctly
- Passporting rules correctly applied (e.g., Universal Credit recipients with no income)
- Capital assessment includes all statutory disregards and allowances

**Priority**: MUST_HAVE
**Stakeholder**: MoJ Policy Team, LAA CEO

---

### BR-2: Rapid Eligibility Determination

**Description**: The system must enable eligibility determinations within 5 working days of application submission for all case types, with automated determination for straightforward cases and caseworker review for complex cases.

**Rationale**: Current 20+ day determination times deny citizens timely access to legal representation. Court hearings, eviction deadlines, and detention reviews create urgent time pressure.

**Success Criteria**:

- Average determination time under 5 working days across all categories
- Automated determination for clear-cut cases (estimated 60% of applications) within 1 working day
- Complex cases routed to caseworker review within 2 working days

**Priority**: MUST_HAVE
**Stakeholder**: LAA CEO, Applicants

---

### BR-3: Reduced Practitioner Administrative Burden

**Description**: The system must reduce the time solicitors and barristers spend completing legal aid applications from approximately 2 hours to under 30 minutes through digital forms, auto-population, and real-time validation.

**Rationale**: Administrative burden is a key factor in solicitor firms withdrawing from legal aid work, creating legal aid deserts (see SD-3). If the provider base collapses, expanded eligibility is meaningless.

**Success Criteria**:

- Average application completion time under 30 minutes
- Auto-population of financial data from HMRC/DWP where consent is given
- Real-time validation preventing submission errors
- Practice management software API for bulk/integrated applications

**Priority**: MUST_HAVE
**Stakeholder**: Law Society, Bar Council, LAPG

---

### BR-4: Citizen Self-Service Eligibility Check

**Description**: The system must provide citizens with a self-service eligibility pre-check that gives an indicative (non-binding) assessment of likely eligibility based on basic financial information, before they engage a solicitor.

**Rationale**: Many eligible citizens do not apply for legal aid because they assume they are ineligible. A simple pre-check increases take-up among eligible citizens and avoids wasted time for ineligible applicants.

**Success Criteria**:

- Pre-check completable in under 10 minutes
- Accuracy of indicative result above 90% (compared to full assessment)
- Plain language explanation of result and next steps
- Accessible to users with low digital literacy (reading age 9-11)

**Priority**: SHOULD_HAVE
**Stakeholder**: Citizens Advice, Applicants

---

## Functional Requirements

### FR-1: Digital Application Form

**Description**: System must provide a guided digital application form for legal aid covering applicant personal details, case details, and financial information (income, capital, outgoings).

**Relates To**: BR-1, BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given a solicitor completing an application, when they enter financial data, then real-time validation checks for completeness and consistency
- [ ] Given a citizen applying directly, when they reach a financial question, then contextual help explains what is being asked in plain language
- [ ] Given partial completion, when the user saves and returns, then all previously entered data is preserved
- [ ] Given a criminal case at the police station, when urgent representation is needed, then an expedited application pathway is available

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-2: Means Test Rules Engine

**Description**: System must implement the statutory means test as a configurable rules engine, calculating gross income, disposable income, and disposable capital against statutory thresholds, applying all allowances, disregards, and passporting rules.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given an applicant receiving Universal Credit with no income, when assessed, then they are passported to eligibility without detailed financial assessment
- [ ] Given an applicant with gross income of GBP 2,657/month (2023 threshold), when assessed, then the system correctly applies the gross income test
- [ ] Given an applicant with a partner, when assessed, then partner income and capital are aggregated unless a contrary interest exemption applies
- [ ] Given a rule change from MoJ, when the rules engine is updated, then changes can be deployed within 5 working days without code changes

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-3: Automated Income Verification (HMRC Integration)

**Description**: System must verify applicant income through HMRC Real Time Information (RTI) data with applicant consent, reducing the need for manual evidence gathering.

**Relates To**: BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given applicant consent, when income verification is requested, then HMRC RTI data is retrieved and compared against declared income
- [ ] Given a discrepancy between declared and verified income, then the case is flagged for caseworker review
- [ ] Given HMRC data is unavailable (self-employed, recent job change), then the system falls back to manual evidence submission

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: INT-1 (HMRC RTI integration)

---

### FR-4: Benefits Status Verification (DWP Integration)

**Description**: System must verify applicant benefits status through DWP data sharing to automatically apply passporting rules for means-tested benefit recipients.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given an applicant claiming Universal Credit, when DWP confirms receipt, then passporting to eligibility is applied automatically
- [ ] Given DWP data is unavailable or inconclusive, then the system requests manual evidence from the applicant

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM
**Dependencies**: INT-2 (DWP integration)

---

### FR-5: Caseworker Review Workflow

**Description**: System must provide LAA caseworkers with a workflow for reviewing complex cases, recording determination decisions with reasoning, and communicating decisions to applicants and their representatives.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a case flagged for caseworker review, when the caseworker opens it, then all application data, verification results, and rules engine assessment are displayed
- [ ] Given a determination decision, when the caseworker records it, then a decision letter is generated with clear reasoning citing the relevant regulations
- [ ] Given a refusal, when the decision is communicated, then the applicant is informed of their right to appeal and the process for doing so

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-6: Real-Time Eligibility Pre-Check

**Description**: System must provide a public-facing eligibility pre-check on GOV.UK that gives citizens an indicative assessment before formal application.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a citizen entering basic financial information, when the pre-check runs, then an indicative result is displayed within 30 seconds
- [ ] Given the pre-check result, when displayed, then it clearly states the result is indicative and directs to formal application
- [ ] Given a likely-eligible result, when displayed, then the system provides information on finding a legal aid solicitor in their area

**Priority**: SHOULD_HAVE
**Complexity**: LOW

---

### FR-7: HMCTS Legal Aid Status Integration

**Description**: System must provide real-time legal aid status to HMCTS case management systems so that courts know whether a defendant or party has legal aid representation.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a court hearing, when the court system queries legal aid status, then the current status (granted, pending, refused, withdrawn) is returned within 300ms
- [ ] Given a legal aid grant, when the grant is made, then the assigned solicitor details are available to the court system

**Priority**: MUST_HAVE
**Complexity**: MEDIUM
**Dependencies**: INT-3 (HMCTS integration)

---

## Non-Functional Requirements (NFRs)

### NFR-P-1: Response Time

**Requirement**: Page load time below 2 seconds at p95. Means test calculation below 5 seconds. HMRC income verification below 10 seconds (dependent on HMRC API).

**Load Conditions**: Peak 2,000 concurrent users (solicitors submitting applications during court hours), 5,000 daily applications at peak.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% uptime during business hours (Monday-Friday 08:00-20:00). 99.5% outside business hours. Police station duty solicitor applications require 24/7 availability at 99.5%.

**Priority**: CRITICAL

---

### NFR-SEC-1: Data Protection

**Requirement**: All applicant financial data encrypted at rest (AES-256) and in transit (TLS 1.3+). HMRC and DWP data subject to additional handling controls per data sharing agreements. Applicant consent recorded and auditable. Data retained per LAA retention schedule (6 years after case closure).

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. Plain language at reading age 9-11 for citizen-facing content. Welsh language support. Easy Read format for key guidance.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: HMRC Real Time Information (RTI)

**Purpose**: Verify applicant employment income against HMRC payroll data.
**Integration Type**: Real-time API with applicant consent
**Authentication**: Government Gateway / OAuth 2.0
**SLA**: Response within 10 seconds at p95
**Priority**: MUST_HAVE

---

### INT-2: DWP Benefits Verification

**Purpose**: Verify receipt of means-tested benefits for passporting to eligibility.
**Integration Type**: Real-time API
**Authentication**: Cross-government authentication
**SLA**: Response within 5 seconds at p95
**Priority**: SHOULD_HAVE

---

### INT-3: HMCTS Case Management

**Purpose**: Provide real-time legal aid status to courts; receive case references for linking.
**Integration Type**: Real-time API (RESTful)
**SLA**: Response within 300ms at p95
**Priority**: MUST_HAVE

---

### INT-4: GOV.UK Notify

**Purpose**: Send determination decisions, application updates, and reminders via email, SMS, and letter.
**Integration Type**: API
**Priority**: MUST_HAVE

---

## Data Requirements

### Key Data Entities

| Entity | Description | Volume | Classification | Retention |
|--------|-------------|--------|---------------|-----------|
| Application | Legal aid application with personal and case details | 300,000/year | OFFICIAL-SENSITIVE | 6 years after case closure |
| Financial Assessment | Income, capital, and outgoings data | 300,000/year | OFFICIAL-SENSITIVE | 6 years after case closure |
| Determination | Eligibility decision with reasoning | 300,000/year | OFFICIAL-SENSITIVE | 6 years after case closure |
| Provider | Legal aid solicitor/barrister registration | 5,000 active | OFFICIAL | Active + 3 years |
| HMRC Verification | Income verification response data | 200,000/year | OFFICIAL-SENSITIVE | 6 years after determination |

### Data Migration

**Scope**: Active legal aid certificates from current LAA systems. Historical application data for reference only (read-only archive).

**Strategy**: Phased migration by case category, starting with criminal (simpler) then civil (complex).

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Average determination time | 20+ working days | Under 5 working days | 12 months |
| Application completion time (solicitor) | 120 minutes | Under 30 minutes | 6 months |
| Means test accuracy | ~95% | 99.9% | 6 months |
| Automated determination rate | 0% | 60% | 12 months |
| Citizen pre-check completion rate | N/A (new) | 80% | 12 months |

---

## Dependencies and Risks

| Risk ID | Description | Probability | Impact | Mitigation |
|---------|-------------|-------------|--------|------------|
| R-1 | HMRC RTI API not available or performant | MEDIUM | HIGH | Fallback to manual evidence, phased verification |
| R-2 | Means test rules too complex for automated engine | LOW | HIGH | Extensive test cases from MoJ Policy, tiered automation |
| R-3 | Solicitor firms do not adopt digital application | MEDIUM | HIGH | Practitioner working group, training, maintain paper route during transition |
| R-4 | Incorrect automated determinations | LOW | CRITICAL | 100% audit of automated decisions in first 3 months, human review threshold |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| LASPO | Legal Aid, Sentencing and Punishment of Offenders Act 2012 |
| Means Test | Statutory financial eligibility assessment for legal aid |
| Passporting | Automatic eligibility for legal aid based on receipt of certain benefits |
| RTI | Real Time Information — HMRC payroll data system |
| Determination | LAA decision on legal aid eligibility |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 16 Architecture Principles
- ARC-002-STKE-v1.0 — Legal Aid Digital Service Stakeholder Analysis
- Legal Aid Means Test Review 2023 (MoJ)
- LASPO Act 2012

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Legal Aid Digital Service
**Model**: Claude Opus 4.6
