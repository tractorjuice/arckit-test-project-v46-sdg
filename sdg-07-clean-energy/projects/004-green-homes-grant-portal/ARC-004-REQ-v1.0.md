# Project Requirements: Green Homes Grant Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Green Homes Grant Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Green Homes Grant Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Programme Board, Local Authorities, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Green Homes Grant Portal — a digital platform for applying, managing, and tracking government home energy efficiency grants across multiple concurrent schemes.

---

## Executive Summary

### Business Context

The UK government provides over £1 billion annually in home energy efficiency grants through multiple schemes: the Green Homes Grant, Boiler Upgrade Scheme (BUS), Home Upgrade Grant (HUG), Local Authority Delivery Scheme (LADS), and ECO4. The 2020 Green Homes Grant scheme failed due to administrative complexity, an overwhelmed IT system, and contractor availability issues. A new, resilient digital platform is needed to manage the next generation of grant programmes and deliver the Net Zero Strategy's target of 600,000 heat pump installations per year by 2028.

### Objectives

- Process 500,000 grant applications per year across multiple concurrent schemes
- Determine eligibility within 48 hours using automated data verification
- Disburse grant payments within 30 days of approved work completion
- Prevent fraud through automated detection while maintaining applicant-friendly processes
- Track energy efficiency outcomes by linking grants to EPC and smart meter data

### Expected Outcomes

- £1 billion+ in grants disbursed annually to 500,000 households
- 2 MtCO2e annual carbon reduction from funded improvements
- Average household energy bill reduction of £300/year for grant recipients
- 95% applicant satisfaction with the application process
- <2% fraud rate (vs industry average of 5-7% for government grants)

### Project Scope

**In Scope**:
- Householder application portal on GOV.UK
- Local authority grant management dashboard
- Installer registration and work completion reporting
- Automated eligibility checking (EPC, income, property type)
- Grant payment processing
- Fraud detection and prevention
- Outcome tracking (EPC improvement, energy savings)

**Out of Scope**:
- Installer training and certification (MCS responsibility)
- Energy supplier ECO obligation management (Ofgem responsibility)
- Physical home assessments
- Heat pump or insulation product procurement

---

## Business Requirements

### BR-1: Multi-Scheme Grant Application

**Description**: The portal must support concurrent operation of multiple grant schemes with different eligibility criteria, grant values, and delivery models on a single platform.
**Success Criteria**: 4+ schemes operational simultaneously; scheme-specific eligibility rules configurable without code changes; new schemes deployable within 4 weeks
**Priority**: MUST_HAVE

### BR-2: Automated Eligibility Determination

**Description**: The system must determine applicant eligibility automatically by cross-referencing property data (EPC register), income data (DWP benefits database), and geographic data (local authority area).
**Success Criteria**: 80% of applications determined automatically within 48 hours; manual review required only for edge cases
**Priority**: MUST_HAVE

### BR-3: Fraud Prevention

**Description**: The system must detect and prevent fraudulent applications, duplicate claims, installer gaming, and inflated cost quotes.
**Success Criteria**: 95% fraud detection rate; <2% overall fraud rate; fraud checks add no more than 2 business days to processing
**Priority**: MUST_HAVE

### BR-4: Grant Payment Processing

**Description**: The system must process grant payments to householders or installers within 30 days of approved work completion evidence submission.
**Success Criteria**: 95% of payments within 30 days; integration with government payment systems (BACS)
**Priority**: MUST_HAVE

### BR-5: Outcome Tracking

**Description**: The system must track the energy efficiency outcome of each grant-funded installation by linking to EPC before/after ratings and, where available, smart meter consumption data.
**Success Criteria**: 90% of completed grants linked to post-installation EPC; energy savings quantified for policy reporting
**Priority**: SHOULD_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Homeowner Helen

- **Role**: Householder applying for a grant to install a heat pump
- **Goals**: Get financial help to replace gas boiler; simple application process; know when money arrives
- **Pain Points**: Confused by multiple schemes; does not know which she's eligible for; worried about upfront costs
- **Technical Proficiency**: Low

#### Persona 2: Local Authority Officer Lisa

- **Role**: Council housing officer managing HUG scheme delivery in her area
- **Goals**: Manage grant allocations, track installer performance, report to DESNZ on spend and outcomes
- **Pain Points**: Manual spreadsheet-based processes; multiple systems; reporting burden
- **Technical Proficiency**: Medium

#### Persona 3: Installer Ian

- **Role**: MCS-certified heat pump installer
- **Goals**: Receive confirmed grant approvals before starting work; submit completion evidence digitally; get paid promptly
- **Pain Points**: Previous scheme left installers unpaid; unclear approval status; paper-based evidence submission
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-1: Scheme-Aware Application Form

**Description**: Present householders with a single application entry point that automatically identifies eligible schemes based on property and household characteristics.

**Acceptance Criteria**:
- [ ] Given a householder entering their postcode and property type, when eligibility is checked, then all applicable schemes are presented with grant values and conditions
- [ ] Given a selected scheme, when the application form is displayed, then only scheme-relevant questions are shown (progressive disclosure)
- [ ] Given a completed application, when submitted, then a reference number and expected timeline are provided immediately

**Priority**: MUST_HAVE

#### FR-2: Automated Eligibility Engine

**Description**: Cross-reference application data with EPC register, DWP benefits database, and council tax records to determine eligibility automatically.

**Acceptance Criteria**:
- [ ] Given an applicant address, when checked against the EPC register, then current EPC rating and eligible improvements are retrieved within 10 seconds
- [ ] Given an applicant claiming income-based eligibility, when checked against DWP data (with consent), then benefit status is verified within 24 hours
- [ ] Given all data checks complete, when eligibility is determined, then the applicant receives notification within 48 hours

**Priority**: MUST_HAVE
**Complexity**: HIGH

#### FR-3: Installer Matching and Approval

**Description**: Match approved applications with MCS-certified installers in the applicant's area and manage the installer assignment workflow.

**Acceptance Criteria**:
- [ ] Given an approved application, when an installer search is triggered, then MCS-certified installers within 30 miles are listed with availability and customer ratings
- [ ] Given an installer selected, when they accept the job, then a grant confirmation letter is generated for the householder confirming the approved amount

**Priority**: MUST_HAVE

#### FR-4: Work Completion and Evidence

**Description**: Allow installers to submit work completion evidence (photographs, MCS certificate, commissioning data) digitally for grant payment release.

**Acceptance Criteria**:
- [ ] Given completed installation work, when the installer submits evidence via the portal (photos, MCS certificate, commissioning report), then evidence is stored and quality-checked within 5 business days
- [ ] Given evidence approved, when payment is triggered, then the grant is paid within 30 days via BACS

**Priority**: MUST_HAVE

#### FR-5: Fraud Detection Engine

**Description**: Automated checks for duplicate applications, installer patterns, price anomalies, and identity verification.

**Acceptance Criteria**:
- [ ] Given a new application, when processed, then it is checked against existing applications for the same property (duplicate detection)
- [ ] Given installer pricing, when submitted, then quotes are compared against regional benchmarks and flagged if >30% above median
- [ ] Given an application flagged for fraud risk, when reviewed, then a manual review workflow is triggered with all supporting evidence presented to the reviewer

**Priority**: MUST_HAVE
**Complexity**: HIGH

#### FR-6: Local Authority Dashboard

**Description**: Provide local authorities with a management dashboard for HUG/LADS scheme administration.

**Acceptance Criteria**:
- [ ] Given a local authority user, when they log in, then they see their area's grant allocation, spend to date, applications pending, and installations completed
- [ ] Given reporting requirements, when an export is requested, then DESNZ-format quarterly reports are generated automatically

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### NFR-P-1: Application Portal Performance

**Requirement**: Application form pages must load within 2 seconds (p95). Eligibility determination API must respond within 10 seconds. System must handle 5,000 concurrent users during scheme announcement peaks.
**Priority**: HIGH

### NFR-A-1: Portal Availability

**Requirement**: 99.9% uptime. The 2020 scheme failed partly due to system unavailability during peak demand. Planned maintenance only between 02:00-06:00 UTC.
**RTO**: 1 hour. **RPO**: 0 for application data.
**Priority**: CRITICAL

### NFR-SEC-1: Data Protection

**Requirement**: UK GDPR compliance. Application data includes personal financial information (income, benefits status) classified as OFFICIAL-SENSITIVE. Integration with DWP data requires Information Sharing Agreement and Privacy Impact Assessment.
**Priority**: CRITICAL

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. The application process must be completable by users with low digital literacy. Assisted digital pathway via telephone support. Welsh language support.
**Priority**: CRITICAL

### NFR-SEC-2: Payment Security

**Requirement**: PCI-DSS-aligned controls for grant payment processing. Anti-money-laundering checks for payments above £10,000. Segregation of duties for payment approval.
**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: EPC Register

**Purpose**: Retrieve current EPC rating for applicant property; verify eligible improvements; link post-installation EPC for outcome tracking.
**Integration Type**: RESTful API (via EPC system — Project 003)
**Priority**: CRITICAL

### INT-2: DWP Benefits Database

**Purpose**: Verify income-based eligibility for means-tested schemes.
**Integration Type**: Secure data sharing via DWP API (requires Information Sharing Agreement)
**Priority**: MUST_HAVE

### INT-3: MCS Installer Database

**Purpose**: Verify installer MCS certification status and specialisms.
**Integration Type**: RESTful API query
**Priority**: MUST_HAVE

### INT-4: TrustMark Register

**Purpose**: Verify installer TrustMark registration for consumer protection.
**Integration Type**: RESTful API query
**Priority**: MUST_HAVE

### INT-5: Government Banking Service (BACS)

**Purpose**: Process grant payments to householders and installers.
**Integration Type**: Batch payment file submission
**Priority**: CRITICAL

### INT-6: GOV.UK One Login

**Purpose**: Householder identity verification and authentication.
**Integration Type**: OpenID Connect
**Priority**: MUST_HAVE

### INT-7: Smart Meter Data Platform

**Purpose**: Link grant-funded installations to energy consumption changes for outcome measurement.
**Integration Type**: Analytics API (via Smart Meter Data Platform — Project 001)
**Priority**: SHOULD_HAVE

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Applications processed/year | 0 (new system) | 500,000 | 12 months post-launch |
| Eligibility determination time | N/A | <48 hours (80% auto) | Launch |
| Payment processing time | N/A | <30 days | Launch |
| Fraud rate | N/A | <2% | Ongoing |
| Applicant satisfaction | N/A | 95% | 6 months post-launch |
| System availability | N/A | 99.9% | Launch |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-004-STKE-v1.0 | Stakeholder Analysis | This programme | Stakeholder drivers | `projects/004-green-homes-grant-portal/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 7 Programme | Governing principles | `projects/000-global/` |
| NAO Green Homes Grant Report | Audit | NAO | Lessons learned from 2020 scheme failure | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Green Homes Grant Portal (Project 004)
**Model**: Claude Opus 4.6 (1M context)
