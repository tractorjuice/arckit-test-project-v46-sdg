# Project Requirements: Debt Advice Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Debt Advice Digital Service (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Debt Advice Digital Programme, MaPS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MaPS Board, FCA, StepChange, Citizens Advice, Insolvency Service |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Debt Advice Digital Service — a platform providing financial health assessment, debt advice triage, Breathing Space applications, and seamless referral to FCA-regulated debt advice providers (StepChange, Citizens Advice, community agencies). It addresses the estimated 9 million UK adults with problem debt, of whom only 700,000 currently access free advice annually.

---

## Executive Summary

### Business Context

An estimated 9 million adults in the UK have problem debt, but fewer than 8% access free debt advice each year. The primary barriers are stigma, long wait times for telephone advice, limited awareness of available support, and digital exclusion. MaPS commissions free debt advice through StepChange, Citizens Advice, and community agencies, but demand consistently exceeds capacity.

The Breathing Space scheme (Debt Respite Scheme Regulations 2020) provides 60-day protection from creditor action, but the application process is largely manual. The FCA regulates debt advice that recommends formal insolvency solutions (DROs, IVAs, bankruptcy), creating a clear regulatory boundary the digital service must respect.

### Objectives

- Provide 24/7 digital financial health assessment and debt advice triage
- Process Breathing Space applications digitally end-to-end
- Seamlessly refer complex cases to human debt advisers (telephone, video, face-to-face)
- Meet FCA regulatory requirements for the boundary between guidance and regulated advice
- Reach 500,000 additional people per year through the digital channel

### Expected Outcomes

- 1.5 million people accessing debt advice annually (up from 700,000)
- 80% of Breathing Space applications processed digitally
- GBP 15M annual cost savings through digital triage (freeing human advisers for complex cases)
- 30% reduction in average time from first contact to debt solution implementation

### Project Scope

**In Scope**:

- Financial health assessment tool (income, expenditure, debts analysis)
- Debt options navigator (plain language explanation of available solutions)
- Breathing Space application and creditor notification system
- Referral to FCA-regulated debt advice providers (warm handoff)
- Creditor integration API for Breathing Space
- Outcome tracking and reporting

**Out of Scope**:

- Provision of regulated debt advice (remains with StepChange, CA, community agencies)
- Debt management plan administration
- Commercial debt advice services
- Credit scoring or credit reference agency integration

---

## Business Requirements

### BR-001: Digital Financial Health Assessment

**Description**: Provide a confidential, non-judgemental digital tool where users can input their income, expenditure, and debts to receive a clear picture of their financial situation and available options.

**Rationale**: Most people do not seek debt advice because they are unaware of their options or feel ashamed. A private, 24/7 digital tool lowers the barrier to seeking help (ref: SD-1, SD-3).

**Success Criteria**:

- 500,000 completed financial health assessments per year through the digital channel
- Average completion time under 20 minutes
- 70% of users report improved understanding of their options

**Priority**: MUST_HAVE

---

### BR-002: Breathing Space Digital Processing

**Description**: Enable end-to-end digital processing of Breathing Space applications, including eligibility assessment, application submission, creditor notification, and moratorium management.

**Rationale**: The current process is largely manual, taking 5 days average. Digital processing reduces this to 1 day, providing faster protection for people in crisis (ref: SD-5).

**Success Criteria**:

- 80% of Breathing Space applications processed digitally
- Average processing time reduced from 5 days to 1 day
- Creditors notified within 24 hours of moratorium start

**Priority**: MUST_HAVE

---

### BR-003: Seamless Referral to Human Advisers

**Description**: When the digital assessment identifies a complex case, vulnerability, or need for regulated debt advice, the service must provide a warm handoff to a human adviser at StepChange, Citizens Advice, or a community agency — without requiring the person to repeat their story.

**Rationale**: Digital triage handles straightforward cases; complex cases need human expertise. The transition must be seamless to avoid people falling through gaps (ref: SD-4).

**Success Criteria**:

- 95% of referrals include a complete case summary passed to the receiving adviser
- Average wait time for telephone callback under 30 minutes during business hours
- Zero data loss during handoff

**Priority**: MUST_HAVE

---

### BR-004: FCA Regulatory Compliance

**Description**: The digital service must clearly distinguish between general financial guidance (unregulated, provided directly by the platform) and specific debt advice recommending solutions (regulated, requiring human adviser involvement).

**Rationale**: FCA regulatory requirement. The digital service can inform and triage but cannot recommend specific insolvency solutions without human oversight (ref: SD-2).

**Success Criteria**:

- Clear regulatory boundary implemented in the user journey
- All debt solution recommendations involve a qualified debt adviser (telephone, video, or in-person)
- FCA supervisory visit finds no regulatory concerns

**Priority**: MUST_HAVE

---

### BR-005: Creditor API for Breathing Space

**Description**: Provide a standardised API enabling creditors to receive Breathing Space notifications, acknowledge moratoriums, and report compliance.

**Rationale**: Automated creditor notification reduces administrative burden and ensures faster protection for debtors (ref: SD-5).

**Success Criteria**:

- API adopted by creditors covering 80% of consumer debt by volume
- Automated acknowledgement from creditors within 48 hours
- Dispute resolution workflow for contested debts

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### FR-001: Income and Expenditure Assessment

**Description**: The system must guide users through a structured income and expenditure assessment, categorising spending and calculating disposable income.

**Acceptance Criteria**:

- [ ] Given a user starting the assessment, when they enter income sources, then the system categorises and totals all income (employment, benefits, other)
- [ ] Given expenditure entries, when the user completes all categories, then the system calculates disposable income and flags spending above Standard Financial Statement (SFS) trigger figures
- [ ] Edge case: If the user has irregular income (self-employed, zero-hours), the system supports average calculations over 3-6 months

**Priority**: MUST_HAVE

---

### FR-002: Debt Options Navigator

**Description**: Based on the financial assessment, the system must present available debt solutions in plain language with clear pros and cons, without making a regulated recommendation.

**Acceptance Criteria**:

- [ ] Given a completed assessment, when options are presented, then the user sees all potentially relevant options (informal arrangements, DMP, DRO, IVA, bankruptcy, Breathing Space)
- [ ] Given each option, when the user selects "learn more", then a plain language explanation is provided including eligibility criteria, impact on credit, and duration
- [ ] Edge case: The system must not present any option as "recommended" — this crosses the regulatory boundary into regulated advice

**Priority**: MUST_HAVE

---

### FR-003: Breathing Space Application

**Description**: The system must enable debt advisers (and, where appropriate, the digital service directly for standard Breathing Space) to submit Breathing Space applications to the Insolvency Service register.

**Acceptance Criteria**:

- [ ] Given an eligible person, when the adviser submits a Breathing Space application, then the application is registered on the Insolvency Service Electronic Breathing Space Service within 1 working day
- [ ] Given a registered moratorium, when creditors are identified, then notifications are sent digitally within 24 hours
- [ ] Edge case: If a creditor disputes a listed debt, the system supports the dispute resolution process within the 60-day moratorium period

**Priority**: MUST_HAVE

---

### FR-004: Warm Referral to Advice Providers

**Description**: The system must transfer case data to the receiving debt advice provider securely, with the user's consent, so they do not have to repeat their story.

**Acceptance Criteria**:

- [ ] Given a referral, when the user consents to data sharing, then the complete financial assessment is transmitted to the receiving provider in SFS format
- [ ] Given a telephone callback referral, when the provider contacts the user, then they have the full case summary available
- [ ] Edge case: If the user declines data sharing, they can still be referred but must repeat their information

**Priority**: MUST_HAVE

---

### FR-005: Crisis Pathway

**Description**: The system must identify users in immediate crisis (bailiff action today, imminent eviction, utility disconnection, mental health crisis) and fast-track them to immediate human support.

**Acceptance Criteria**:

- [ ] Given a user indicating an immediate crisis, when the system detects crisis indicators, then the user is offered immediate telephone support (warm transfer or callback within 15 minutes)
- [ ] Given a mental health crisis moratorium eligibility, when the user or a care professional identifies mental health treatment, then the system initiates the mental health crisis Breathing Space pathway

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### NFR-P-001: Availability

**Requirement**: 99.9% availability for the financial health assessment tool (24/7 service). Breathing Space processing available during business hours (Monday-Friday 08:00-20:00).

**Priority**: HIGH

---

### NFR-SEC-001: Data Protection

**Requirement**: Full UK GDPR compliance. Financial data classified as OFFICIAL-SENSITIVE. Explicit consent required for data sharing with advice providers. Data retention limited to active case duration plus 6 years.

**Priority**: CRITICAL

---

### NFR-U-001: Accessibility and Tone

**Requirement**: WCAG 2.2 Level AA. Content at reading age 9 or below. Non-judgemental, supportive tone throughout. No financial jargon without plain-language explanation.

**Priority**: CRITICAL

---

### NFR-U-002: Mobile-First Design

**Requirement**: Full functionality available on mobile devices. Optimised for low-bandwidth connections. Service usable on devices with screen sizes from 320px width.

**Priority**: HIGH

---

## Integration Requirements

### INT-001: Insolvency Service — Breathing Space Register

**Purpose**: Submit and manage Breathing Space applications on the Electronic Breathing Space Service.

**Integration Type**: Real-time API

**Priority**: CRITICAL

---

### INT-002: StepChange / Citizens Advice — Case Referral

**Purpose**: Transfer case data (financial assessment in SFS format) to receiving advice providers.

**Integration Type**: Real-time API with consent management

**Priority**: CRITICAL

---

### INT-003: Creditor Notification API

**Purpose**: Notify creditors of Breathing Space moratoriums and receive acknowledgements.

**Integration Type**: RESTful API with webhook notifications

**Priority**: HIGH

---

### INT-004: DWP Universal Credit — Benefit Verification

**Purpose**: Verify benefit receipt status to support financial assessment accuracy.

**Integration Type**: API (subject to data sharing agreement)

**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

**TC-1**: FCA regulatory boundary must be respected — the digital service cannot provide regulated debt advice without human oversight.

**TC-2**: Standard Financial Statement (SFS) format must be used for income and expenditure data exchange with advice providers.

**BC-1**: Budget envelope of GBP 42M over 5 years.

**BC-2**: Existing MaPS commissioning contracts with advice providers must be maintained — digital service supplements, not replaces.

**A-1**: StepChange and Citizens Advice will adopt the referral API if it reduces their administrative burden and improves client experience.

**A-2**: Major creditors (top 20 by debt volume) will adopt the Breathing Space API within 18 months.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Annual users of digital service | 0 | 500,000 | Year 3 |
| Total people accessing advice (all channels) | 700,000 | 1,500,000 | Year 3 |
| Breathing Space digital processing rate | 20% | 80% | Year 2 |
| User satisfaction (digital channel) | N/A | 80% | Year 2 |
| Average time to Breathing Space protection | 5 days | 1 day | Year 2 |
| Referral completion rate (user reaches adviser) | N/A | 85% | Year 2 |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| MaPS Chief Executive | Organisation Leader | [ ] Approved | PENDING |
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| FCA Supervision | Regulator | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Debt Advice Digital Service
**Model**: Claude Opus 4.6
