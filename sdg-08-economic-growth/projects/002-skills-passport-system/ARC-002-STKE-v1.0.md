# Stakeholder Drivers & Goals Analysis: Skills Passport System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Skills Passport System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Skills Passport Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Skills Passport Programme Board, DfE Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Digital Skills Passport System, their underlying drivers, derived goals, and measurable outcomes. The Skills Passport will enable individuals to hold verified digital credentials for qualifications, skills, and professional certifications, creating a portable, tamper-proof record usable across employers, education providers, and government services.

### Key Findings

The Skills Passport System faces a classic platform adoption challenge: its value depends on critical mass from both credential issuers (universities, awarding bodies, employers) and credential verifiers (employers, professional bodies, immigration services). The strongest driver alignment exists around reducing credential fraud — universities, professional regulators, and employers all suffer from fraudulent qualifications. The most significant tension is between DfE's desire for a centralised national system and the education sector's preference for a federated model that preserves institutional autonomy. Universities UK and individual universities will resist any system that positions DfE as gatekeeper of their credentials.

### Critical Success Factors

- Achieve adoption by at least 50 credential issuers (universities and awarding bodies) within the first year — without issuers, the passport has no credentials to hold
- Implement W3C Verifiable Credentials standard to ensure international interoperability and avoid vendor lock-in
- Integrate with the Job Matching Platform (Project 001) so skills data flows into job recommendations
- Obtain HESA and Ofqual endorsement to provide legitimacy with the education sector
- Demonstrate credential verification in under 2 seconds to compete with paper-based processes

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Agreement on the need for digital credentials, but disagreement on governance model (centralised vs. federated), data ownership (individual vs. institutional), and scope (academic qualifications only vs. all skills including informal learning). The international dimension (EU Digital Credentials Framework interoperability) adds complexity.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Education | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DfE Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Skills Passport | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DfE Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Director of Further Education and Skills | Policy ownership | HIGH | HIGH | Manage Closely — Skills policy alignment |
| DfE SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off |
| IfATE (Institute for Apprenticeships and Technical Education) | Qualifications standards | MEDIUM | HIGH | Keep Informed — Apprenticeship credential standards |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| Ofqual | Regulator | Qualifications regulation | HIGH | HIGH |
| HESA | Statutory body | Higher education data | HIGH | HIGH |
| Universities UK | Sector body | University representation | HIGH | HIGH |
| Individual Universities | Education providers | Credential issuers | MEDIUM | HIGH |
| Awarding Bodies (e.g., City & Guilds, Pearson) | Private sector | Qualification issuers | MEDIUM | HIGH |
| Professional Bodies (e.g., BCS, RICS, GMC) | Regulators | Professional credential issuers | MEDIUM | HIGH |
| Employers (large) | Private sector | Credential verifiers | MEDIUM | HIGH |
| Employers (SMEs) | Private sector | Credential verifiers | LOW | MEDIUM |
| Learners/Individuals | Citizens | Credential holders | LOW | HIGH |
| UCAS | Charity | University admissions | MEDIUM | HIGH |
| Student Loans Company (SLC) | Public body | Funding verification | MEDIUM | MEDIUM |
| UK NARIC (UK ENIC) | Public body | International credential recognition | MEDIUM | HIGH |
| DWP (Job Matching Platform) | Partner department | Skills data consumer | MEDIUM | HIGH |
| EU Commission (DG EAC) | International | Digital Credentials Framework interop | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for Skills Passport outcomes and spend | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | Owns end-to-end Skills Passport service | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews |
| Delivery Manager | Manages delivery cadence and risks | MEDIUM / HIGH | Keep Informed — Stand-ups |
| CDDO | Assurance and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • Secretary of     │
        │  • DfE SIRO         │    State (Education) │
        │  • CDDO             │  • Permanent Sec.   │
        │                     │  • SRO              │
        │                     │  • Chief Digital Off│
        │                     │  • Dir of FE/Skills │
 P      │                     │  • Ofqual           │
 O      │                     │  • HESA             │
 W      │                     │  • Universities UK  │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Employers (SME)  │  • Learners         │
        │  • EU Commission    │  • Individual Unis  │
        │                     │  • Awarding Bodies  │
        │                     │  • Professional     │
        │                     │    Bodies            │
        │                     │  • UCAS             │
        │                     │  • UK ENIC          │
        │                     │  • DWP (Job Match)  │
        │                     │  • IfATE            │
        │                     │  • Employers (large)│
        │                     │  • SLC              │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State for Education — Deliver Lifelong Learning Infrastructure

**Stakeholder**: Secretary of State for Education

**Driver Category**: STRATEGIC

**Driver Statement**: Create the digital infrastructure for the Lifelong Loan Entitlement (LLE) by providing every citizen with a portable record of qualifications and skills that supports modular, flexible learning throughout their career.

**Context & Background**: The Lifelong Loan Entitlement, due to launch in 2027, will provide individuals with a loan entitlement equivalent to four years of post-18 education, usable flexibly across further and higher education. This requires a digital record system that tracks modules, credits, and qualifications across multiple institutions over decades. The Skills Passport is the enabling infrastructure for this policy commitment.

**Driver Intensity**: CRITICAL

**Enablers**:
- Lifelong Loan Entitlement creating regulatory driver for credential tracking
- W3C Verifiable Credentials standard reaching maturity
- Strong DfE digital team with experience in GOV.UK services

**Blockers**:
- University sector resistance to centralised credential management
- Complexity of mapping existing qualification frameworks to digital credentials
- International interoperability requirements adding scope

**Related Stakeholders**: Ofqual (regulatory alignment), Universities UK (sector buy-in), IfATE (apprenticeship credentials)

---

### SD-2: Universities UK — Preserve Institutional Autonomy

**Stakeholder**: Universities UK and individual universities

**Driver Category**: STRATEGIC / PERSONAL

**Driver Statement**: Universities support digital credentials in principle but insist that credential issuance remains under institutional control. They will not accept a system where DfE acts as gatekeeper, and they want to maintain their own branding and quality reputation on issued credentials.

**Context & Background**: Universities are autonomous institutions, not government agencies. Their degrees carry institutional reputation — a degree from UCL carries different market value than a degree from a newer institution. Any system that homogenises credentials or positions government as the authority undermines institutional autonomy. The European approach (EBSI-based) is federated, and UK universities expect the same.

**Driver Intensity**: HIGH

**Enablers**:
- Federated architecture using decentralised identifiers (DIDs) where each institution is an independent issuer
- University branding preserved on digital credentials
- No government veto on credential issuance

**Blockers**:
- Centralised credential store controlled by DfE
- Mandatory participation without sector consultation
- Revenue implications if credentials bypass university transcript services

**Related Stakeholders**: Individual universities, HESA, Ofqual

---

### SD-3: Employers — Faster, Cheaper Credential Verification

**Stakeholder**: Employers (particularly large employers, regulated sectors)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Employers want instant, reliable verification of candidate qualifications without the cost and delay of manual checking. Credential fraud costs UK employers an estimated GBP 7 billion annually in hiring unsuitable candidates.

**Context & Background**: Current credential verification involves contacting institutions individually, waiting days or weeks for responses, and paying per-verification fees. Regulated sectors (healthcare, education, financial services) have statutory obligations to verify credentials. A digital system offering cryptographic verification in seconds would transform hiring efficiency, particularly for high-volume recruitment.

**Driver Intensity**: HIGH

**Enablers**:
- Cryptographic verification providing tamper-proof, instant results
- API integration with Applicant Tracking Systems
- Free or low-cost verification for employers

**Blockers**:
- Incomplete coverage — if only some credentials are digital, employers still need manual verification
- Trust — employers need to understand and trust cryptographic verification
- Regulatory acceptance — will regulators accept digital verification as sufficient?

---

### SD-4: Learners/Individuals — Own and Control Their Credential Data

**Stakeholder**: Learners (students, workers, lifelong learners)

**Driver Category**: PERSONAL

**Driver Statement**: Individuals want to own their qualification and skills data, share it selectively with employers and institutions, and never lose access to their records — even if an institution closes.

**Context & Background**: When institutions close (e.g., BPP University's campus restructuring, or historical polytechnic mergers), accessing transcripts becomes difficult. Individuals have no portable copy of their verified credentials. The W3C Verifiable Credentials model gives individuals a "wallet" containing cryptographically signed credentials they can present to anyone, without needing the issuing institution to be online.

**Driver Intensity**: MEDIUM

---

### SD-5: Ofqual — Maintain Regulatory Integrity of Qualifications Framework

**Stakeholder**: Ofqual (Office of Qualifications and Examinations Regulation)

**Driver Category**: COMPLIANCE

**Driver Statement**: The Skills Passport must accurately represent the status and level of regulated qualifications, must not enable the presentation of unregulated training as equivalent to regulated qualifications, and must align with the Regulated Qualifications Framework (RQF).

**Context & Background**: Ofqual regulates qualifications in England. The Skills Passport could potentially be used to present non-regulated micro-credentials alongside regulated qualifications in a way that misleads employers. Ofqual requires clear differentiation and accurate level mapping.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Establish Federated Credential Issuance Network

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: SRO, Skills Passport Programme

**Goal Statement**: Onboard 50 credential issuers (universities and awarding bodies) issuing W3C Verifiable Credentials through the Skills Passport network within 12 months of platform launch.

**Success Metrics**:
- **Primary Metric**: Number of active credential issuers
- **Secondary Metrics**:
  - Number of credentials issued (target: 500,000 in Year 1)
  - Credential types covered (degrees, apprenticeships, professional certifications)

**Baseline**: 0 (new capability)
**Target**: 50 issuers, 500,000 credentials in Year 1

---

### Goal G-2: Enable Instant Credential Verification

**Derived From Drivers**: SD-3

**Goal Owner**: Service Owner

**Goal Statement**: Deliver credential verification in under 2 seconds for 99.9% of verification requests, with cryptographic proof of authenticity, at no cost to verifying employers.

**Success Metrics**:
- **Primary Metric**: Verification response time (p99 < 2 seconds)
- **Secondary Metrics**:
  - Employer verification adoption (target: 10,000 employers in Year 1)
  - Fraud detection rate (credentials flagged as invalid)

---

### Goal G-3: Integrate with Job Matching Platform

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: DfE Chief Digital Officer / DWP CDIO (joint)

**Goal Statement**: Establish real-time skills data sharing between the Skills Passport and Job Matching Platform so that verified credentials inform AI job matching recommendations, with individual consent.

**Success Metrics**:
- **Primary Metric**: Percentage of Job Matching Platform users with linked Skills Passport credentials
- **Secondary Metrics**:
  - Improvement in match quality when credentials are available vs. self-reported skills

---

### Goal G-4: Ensure Regulatory Compliance and Qualification Integrity

**Derived From Drivers**: SD-5

**Goal Owner**: Director of Further Education and Skills

**Goal Statement**: Implement credential classification system that clearly differentiates RQF-regulated qualifications from non-regulated micro-credentials, with Ofqual endorsement of the classification schema.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State (Education) | SD-1 | Lifelong learning infrastructure | G-1 | Federated credential network | O-1 | Portable credentials |
| Universities UK | SD-2 | Institutional autonomy | G-1 | Federated credential network | O-1 | Portable credentials |
| Employers | SD-3 | Faster verification | G-2 | Instant verification | O-2 | Reduced fraud |
| Learners | SD-4 | Own credential data | G-1 | Federated credential network | O-1 | Portable credentials |
| Ofqual | SD-5 | Qualification integrity | G-4 | Regulatory compliance | O-3 | Trusted framework |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DfE (SD-1) wants a national system with comprehensive coverage, but Universities UK (SD-2) insists on federated architecture preserving institutional autonomy. DfE's policy ambition implies a degree of central control that universities will resist.
  - **Resolution Strategy**: INNOVATE — Use W3C DID (Decentralised Identifiers) architecture where each institution is a sovereign issuer. DfE operates the trust registry (which institutions are recognised issuers) but does not control credential issuance. This satisfies DfE's need for a national framework while preserving institutional autonomy.

- **Conflict 2**: Employers (SD-3) want comprehensive coverage of all credentials, but Ofqual (SD-5) wants clear separation of regulated and unregulated credentials. Including micro-credentials and informal learning alongside degrees risks confusion.
  - **Resolution Strategy**: COMPROMISE — Implement credential tiers with clear visual and metadata differentiation: Tier 1 (Ofqual regulated), Tier 2 (recognised professional certifications), Tier 3 (non-regulated micro-credentials and employer-issued badges). Employers can filter by tier.

---

## Risk Register (Stakeholder-Related)

### Risk R-1: University Sector Boycott

**Related Stakeholders**: Universities UK, individual universities
**Risk Description**: If the architecture is perceived as centralising control with DfE, major universities may refuse to participate, fatally undermining the platform.
**Probability**: MEDIUM
**Impact**: CRITICAL
**Mitigation Strategy**: Federated DID architecture from the start; extensive co-design with Russell Group and post-92 universities; sector representation on governance board

### Risk R-2: Credential Standard Fragmentation

**Related Stakeholders**: Awarding bodies, professional bodies, EU Commission
**Risk Description**: Different credential issuers adopt different implementations of W3C VCs, creating interoperability issues despite nominally following the same standard.
**Probability**: HIGH
**Impact**: HIGH
**Mitigation Strategy**: Publish UK Skills Passport credential profile (constrained VC implementation); provide issuer SDK and testing tools; mandatory conformance testing before issuer onboarding

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DfE Finance Director | SRO | HM Treasury, CDDO | All |
| Credential standard selection | Lead Architect | Chief Digital Officer | Ofqual, HESA, UUK | Issuers |
| Issuer onboarding criteria | Service Owner | Director of FE/Skills | Ofqual, UUK | Issuers |
| Architecture decisions | Lead Architect | Chief Digital Officer | CDDO | Development teams |
| Integration with Job Matching | Joint DfE/DWP working group | SRO (DfE) + SRO (DWP) | CDDO | Both programme boards |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 3, 4, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| W3C Verifiable Credentials Data Model 2.0 | Standard | W3C | Credential format | https://www.w3.org/TR/vc-data-model-2.0/ |
| Lifelong Loan Entitlement | Policy | DfE | Policy context | https://www.gov.uk/government/publications/lifelong-loan-entitlement |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Skills Passport System
**Model**: Claude Opus 4.6
