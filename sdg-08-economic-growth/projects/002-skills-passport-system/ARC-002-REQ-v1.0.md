# Project Requirements: Skills Passport System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Skills Passport System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Skills Passport System |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Skills Passport Programme Board, DfE Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Digital Skills Passport System, enabling individuals to hold, share, and verify digital credentials for qualifications, skills, and professional certifications using W3C Verifiable Credentials.

---

## Executive Summary

### Business Context

The UK qualifications landscape is fragmented across universities, awarding bodies (City & Guilds, Pearson, OCR), professional bodies (BCS, RICS, GMC), and employer-issued certifications. Verifying someone's qualifications requires contacting multiple institutions, costing time and money. Credential fraud costs UK employers an estimated GBP 7 billion annually. The Lifelong Loan Entitlement (launching 2027) requires a digital infrastructure for tracking modular learning across institutions and years. The Skills Passport will provide this infrastructure using W3C Verifiable Credentials, giving individuals ownership of their verified credentials.

### Objectives

- Enable individuals to hold verified digital credentials in a portable wallet
- Provide instant cryptographic credential verification for employers (< 2 seconds)
- Onboard 50 credential issuers within 12 months
- Support the Lifelong Loan Entitlement by tracking modular learning across institutions
- Integrate with the Job Matching Platform (Project 001) for skills-based matching

### Expected Outcomes

- GBP 500M annual savings from reduced credential fraud
- 90% reduction in credential verification time (from days to seconds)
- Foundation for Lifelong Loan Entitlement policy delivery

### Project Scope

**In Scope**:
- Credential wallet for individuals (web and mobile)
- Credential issuance framework for education providers and awarding bodies
- Credential verification API for employers and services
- Credential trust registry (list of recognised issuers)
- ESCO/SOC skills taxonomy mapping
- Integration with Job Matching Platform and UCAS

**Out of Scope**:
- Content or delivery of education/training (referral only)
- Assessment or examination systems
- Student finance applications (SLC integration deferred to Phase 2)
- International credential equivalency assessment (UK ENIC remains separate)

---

## Business Requirements

### BR-001: W3C Verifiable Credential Issuance

**Description**: The system must enable recognised education providers and awarding bodies to issue digitally signed credentials conforming to the W3C Verifiable Credentials Data Model 2.0 specification.

**Rationale**: W3C VCs provide cryptographic proof of authenticity, tamper detection, and portability. This open standard avoids vendor lock-in and enables international interoperability.

**Success Criteria**:
- 50 credential issuers active within 12 months
- 500,000 credentials issued in Year 1
- Credentials verifiable without contacting the issuing institution

**Priority**: MUST_HAVE

---

### BR-002: Individual Credential Wallet

**Description**: The system must provide every individual with a secure digital wallet where they can store, manage, and selectively share their verified credentials with employers, institutions, and government services.

**Rationale**: Individuals must own and control their credential data. The wallet enables selective disclosure — sharing only the credentials relevant to a specific purpose (e.g., sharing a first aid certificate with an employer without revealing degree classification).

**Success Criteria**:
- 1 million active wallet holders within 18 months
- Wallet accessible via web browser and native mobile apps (iOS, Android)
- Selective disclosure of individual credentials demonstrated

**Priority**: MUST_HAVE

---

### BR-003: Instant Credential Verification

**Description**: The system must enable any party to verify a credential's authenticity, status (active/revoked/expired), and issuer in under 2 seconds through a verification API, without needing to contact the issuing institution.

**Rationale**: Employers currently wait days for credential verification. Instant cryptographic verification eliminates this delay, reduces fraud, and enables real-time skills matching.

**Success Criteria**:
- Verification response time < 2 seconds (p99)
- 10,000 employers using verification API within 12 months
- Revocation status checked in real-time

**Priority**: MUST_HAVE

---

### BR-004: Credential Trust Registry

**Description**: The system must maintain a public trust registry of recognised credential issuers, mapping each issuer to the types of credentials they are authorised to issue, with clear differentiation between Ofqual-regulated qualifications and non-regulated certifications.

**Rationale**: Without a trust registry, verifiers cannot determine whether an issuer is legitimate. The registry also enforces Ofqual's requirement to differentiate regulated qualifications from unregulated micro-credentials.

**Success Criteria**:
- Trust registry published as open data
- All Ofqual-regulated awarding bodies included at launch
- Clear tier classification: Tier 1 (Ofqual regulated), Tier 2 (professional certifications), Tier 3 (non-regulated)

**Priority**: MUST_HAVE

---

### BR-005: Lifelong Learning Record

**Description**: The system must support accumulation of credentials over a lifetime, including partial qualifications (individual modules, credits), enabling the Lifelong Loan Entitlement to track modular learning across multiple institutions and years.

**Rationale**: The Lifelong Loan Entitlement allows individuals to study flexibly — taking individual modules from different institutions. The Skills Passport must track this accumulation to calculate remaining entitlement and credit transfer.

**Success Criteria**:
- Module-level credential tracking demonstrated
- Credit accumulation across institutions demonstrated
- SLC integration design agreed (implementation in Phase 2)

**Priority**: SHOULD_HAVE

---

### BR-006: Integration with Job Matching Platform

**Description**: The system must share verified credential data with the Job Matching Platform (Project 001) via API, with individual consent, to enable AI-powered skills-based job matching using verified qualifications rather than self-reported skills.

**Rationale**: AI job matching is only as good as its input data. Verified credentials provide ground truth for skills, replacing unreliable self-reported qualifications.

**Success Criteria**:
- API operational between Skills Passport and Job Matching Platform
- Measurable improvement in match quality when verified credentials are available
- Individual consent flow implemented and user-tested

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### FR-001: Credential Issuance Portal

**Description**: Provide credential issuers with a portal and API to issue W3C Verifiable Credentials to individuals, including batch issuance for graduation cohorts.

**Acceptance Criteria**:
- [ ] Given a university, when they issue a degree credential, then the credential conforms to W3C VC Data Model 2.0 with JSON-LD serialisation
- [ ] Given a graduation cohort of 5,000 students, when batch issuance is triggered, then all credentials are issued within 1 hour
- [ ] Given an issued credential, when the issuer needs to revoke it (e.g., academic misconduct), then the revocation is reflected in verification within 5 minutes

**Priority**: MUST_HAVE

---

### FR-002: Individual Credential Wallet

**Description**: Provide individuals with a wallet to store, view, and share credentials.

**Acceptance Criteria**:
- [ ] Given an individual receiving a credential, when they accept it, then it appears in their wallet with issuer branding
- [ ] Given an employer requesting verification, when the individual shares a credential, then only the selected credential is shared (selective disclosure)
- [ ] Given an individual without internet access, when they present a credential in person, then a QR code enables offline verification
- [ ] Given an individual who loses their device, when they re-authenticate, then all credentials are recoverable from encrypted backup

**Priority**: MUST_HAVE

---

### FR-003: Verification API

**Description**: Provide a public verification API that verifies credential authenticity, issuer status, and revocation status.

**Acceptance Criteria**:
- [ ] Given a valid credential, when verified, then response includes issuer identity, credential type, issuance date, and validity status
- [ ] Given a revoked credential, when verified, then the response clearly indicates revocation with reason code
- [ ] Given a credential from an unrecognised issuer, when verified, then the response indicates issuer not in trust registry

**Priority**: MUST_HAVE

---

### FR-004: Trust Registry Management

**Description**: Maintain the trust registry of recognised issuers with onboarding, suspension, and removal workflows.

**Acceptance Criteria**:
- [ ] Given a new issuer applying for registration, when their application is reviewed, then registration is completed within 20 working days
- [ ] Given an Ofqual-regulated awarding body, when they register, then their credentials are automatically classified as Tier 1
- [ ] Given a compliance concern, when an issuer is suspended, then all their credentials show a warning during verification

**Priority**: MUST_HAVE

---

### FR-005: Skills Taxonomy Mapping

**Description**: Map all credential types to the ESCO skills taxonomy and UK SOC 2020 codes, enabling skills-based search and matching.

**Acceptance Criteria**:
- [ ] Given a BSc Computer Science credential, when mapped, then associated ESCO skills (programming, data analysis, etc.) are attached
- [ ] Given a search for "project management skills," when queried, then credentials conferring project management competency are returned regardless of credential title

**Priority**: MUST_HAVE

---

### FR-006: UCAS Integration

**Description**: Enable UCAS to verify qualifications via the Skills Passport during the university admissions process.

**Acceptance Criteria**:
- [ ] Given a UCAS applicant with Skills Passport credentials, when UCAS requests verification, then grades and qualifications are verified in real-time
- [ ] Given the applicant's consent, when credentials are shared with UCAS, then only admissions-relevant credentials are disclosed

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### NFR-P-001: Verification Response Time

**Requirement**: Credential verification must complete within 2 seconds at p99, including cryptographic signature validation and revocation status check.

**Load Conditions**: 10,000 concurrent verification requests (UCAS clearing day scenario)
**Priority**: MUST_HAVE

---

### NFR-SEC-001: Cryptographic Standards

**Requirement**: Use EdDSA (Ed25519) or ECDSA (P-256) for credential signatures. Support JSON-LD with BBS+ signatures for selective disclosure. Key management via HSM-backed key vault.

**Priority**: MUST_HAVE

---

### NFR-SEC-002: Individual Data Sovereignty

**Requirement**: Individuals must be able to export all their credential data in a standard format (W3C VC JSON-LD) and delete their wallet at any time. Credential data must not be stored centrally — the wallet is the canonical store.

**Priority**: MUST_HAVE

---

### NFR-A-001: Platform Availability

**Requirement**: Verification API: 99.9% availability. Wallet service: 99.9% availability. Issuance portal: 99.5% availability.

**Priority**: MUST_HAVE

---

### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all citizen-facing interfaces. Screen reader compatibility for credential presentation. High contrast QR codes for offline verification.

**Priority**: MUST_HAVE

---

### NFR-C-001: Ofqual Regulatory Compliance

**Requirement**: All regulated qualifications must be clearly differentiated from non-regulated credentials. Credential metadata must include RQF level where applicable. Ofqual endorsement of classification schema required before launch.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: Job Matching Platform (Project 001)

**Purpose**: Share verified credentials for skills-based job matching
**Integration Type**: Real-time API with OAuth 2.0 consent
**Data Exchanged**: Verified credentials (qualifications, skills, certifications) with individual consent
**Priority**: SHOULD_HAVE

---

### INT-002: UCAS

**Purpose**: Real-time qualification verification during admissions
**Integration Type**: Real-time API
**Data Exchanged**: Qualification grades, institution, completion status
**Priority**: SHOULD_HAVE

---

### INT-003: Learner Records Service (DfE)

**Purpose**: Import existing qualification records for pre-population
**Integration Type**: Batch import with individual consent
**Data Exchanged**: Historical qualification records
**Priority**: SHOULD_HAVE

---

### INT-004: Ofqual Register of Regulated Qualifications

**Purpose**: Validate credential types against regulated qualification register
**Integration Type**: Reference data feed (daily)
**Data Exchanged**: Regulated qualification metadata (title, level, awarding body)
**Priority**: MUST_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must implement W3C Verifiable Credentials Data Model 2.0 — no proprietary credential formats
**TC-2**: Must deploy on UK sovereign cloud
**TC-3**: Must support decentralised identity (W3C DID) for institutional issuers

### Business Constraints

**BC-1**: Budget capped at GBP 15M over 3 years
**BC-2**: Must obtain Ofqual endorsement before public launch
**BC-3**: Must not require mandatory participation from universities (voluntary adoption model)

### Assumptions

**A-1**: W3C VC 2.0 specification will remain stable through development period
**A-2**: Universities will adopt voluntarily if the architecture preserves institutional autonomy
**A-3**: GOV.UK One Login will support DID-based authentication by Beta

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-002-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals, conflicts | `projects/002-skills-passport-system/ARC-002-STKE-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 3, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| W3C VC Data Model 2.0 | Standard | W3C | Credential format | https://www.w3.org/TR/vc-data-model-2.0/ |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Skills Passport System
**Model**: Claude Opus 4.6
