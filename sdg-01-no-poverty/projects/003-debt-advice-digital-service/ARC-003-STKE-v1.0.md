# Stakeholder Drivers & Goals Analysis: Debt Advice Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Debt Advice Digital Service (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Debt Advice Digital Programme, Money and Pensions Service |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MaPS Board, FCA, StepChange, Citizens Advice, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Debt Advice Digital Service, their drivers, goals, and measurable outcomes. The service will provide a digital-first debt advice and financial guidance platform, operated by the Money and Pensions Service (MaPS), integrating with FCA-regulated debt advice providers (StepChange, Citizens Advice, community agencies) and supporting the statutory Breathing Space scheme.

### Key Findings

There is strong stakeholder alignment on expanding access to free debt advice — MaPS, FCA, debt advice providers, and creditors all recognise that early intervention reduces the human and economic cost of problem debt. The principal tension is between MaPS's drive for digital-first efficiency and debt advice charities' insistence that vulnerable people in crisis need human support (telephone, face-to-face). The FCA requires that any digital advice tool providing debt solutions (DROs, IVAs, bankruptcy) meets regulatory standards for suitability — automated advice cannot simply replace qualified human judgement.

### Critical Success Factors

- Digital service supplements, not replaces, existing telephone and face-to-face debt advice channels
- Breathing Space applications processed digitally end-to-end with creditor notification
- FCA regulatory requirements for debt advice met through appropriate human oversight of debt solutions
- Integration with StepChange, Citizens Advice, and community debt advice agencies for seamless referral
- Service accessible to people in financial crisis on any device, including low-specification smartphones

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong alignment on expanding access and improving early intervention. Moderate tension on the role of digital vs human advice for complex cases and vulnerable people.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| MaPS Chief Executive | Organisation leader | HIGH | HIGH | Manage Closely |
| MaPS Board | Governance | HIGH | HIGH | Manage Closely |
| SRO, Debt Advice Digital | Programme sponsor | HIGH | HIGH | Manage Closely |
| MaPS CDIO | Digital leadership | HIGH | MEDIUM | Keep Satisfied |
| MaPS Debt Advice Commissioning | Service commissioning | MEDIUM | HIGH | Keep Informed |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| FCA | Financial Conduct Authority | Regulator | HIGH | HIGH |
| HM Treasury | Government | Sponsor department | HIGH | MEDIUM |
| StepChange Debt Charity | Delivery partner | HIGH | HIGH | Manage Closely |
| Citizens Advice | Delivery partner | HIGH | HIGH | Manage Closely |
| Community debt advice agencies | Delivery partners | MEDIUM | HIGH | Keep Informed |
| People in problem debt | Citizens | Service users | LOW | HIGH |
| Creditors (banks, utilities, councils) | Industry | Breathing Space participants | MEDIUM | HIGH |
| Insolvency Service | Partner body | DRO/bankruptcy processing | MEDIUM | HIGH |
| DWP | Partner department | UC claimant referrals | MEDIUM | MEDIUM |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * MaPS CE          |
        |  * HM Treasury      |  * MaPS Board       |
        |  * MaPS CDIO        |  * SRO              |
        |                     |  * FCA              |
        |                     |  * StepChange       |
 P      |                     |  * Citizens Advice  |
 O      +---------------------+---------------------+
 W      |                     |                     |
 E      |      MONITOR        |    KEEP INFORMED    |
 R      |                     |                     |
   Low  |                     |  * People in debt   |
        |                     |  * Creditors        |
        |                     |  * Insolvency Svc   |
        |                     |  * Community agencies|
        |                     |  * DWP              |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: MaPS — Expand Access to Free Debt Advice

**Stakeholder**: Money and Pensions Service (MaPS)

**Driver Category**: STRATEGIC

**Driver Statement**: Expand access to free debt advice from 700,000 to 1.5 million people per year by providing a digital channel that reaches people earlier in their debt journey, before crisis point.

**Context & Background**: MaPS commissions free debt advice in England through contracts with StepChange, Citizens Advice, and community agencies. Current capacity is approximately 700,000 people per year, primarily through telephone and face-to-face. An estimated 9 million people in the UK have problem debt, but most do not seek advice until crisis point. A digital channel could reach people earlier — when interventions are less costly and more effective.

**Driver Intensity**: CRITICAL

**Enablers**: User-friendly digital tool for financial health assessment; seamless referral to regulated advice providers; integration with Breathing Space scheme; mobile-first design for lower-income users

**Blockers**: Digital exclusion among those most in need; FCA regulatory constraints on automated advice; resistance from advice providers concerned about quality; inadequate funding for digital development

---

### SD-2: FCA — Regulatory Compliance for Debt Advice

**Stakeholder**: Financial Conduct Authority

**Driver Category**: COMPLIANCE / REGULATORY

**Driver Statement**: Ensure any digital debt advice service meets FCA standards for regulated debt advice, including suitability assessments for debt solutions (DROs, IVAs, bankruptcy, debt management plans).

**Context & Background**: Debt advice that recommends formal insolvency solutions is an FCA-regulated activity. The FCA has seen harm from poor-quality commercial debt management companies and is cautious about automated advice replacing qualified human judgement for complex cases. Any digital service must clearly distinguish between general financial guidance (unregulated) and specific debt advice recommending solutions (regulated).

**Driver Intensity**: CRITICAL

**Enablers**: Clear regulatory boundary in the digital service; human oversight for debt solution recommendations; transparent algorithms that can be audited; FCA engagement from design phase

**Blockers**: Automated recommendation engine that doesn't meet suitability standards; insufficient human review capacity; unclear boundary between guidance and advice

---

### SD-3: People in Problem Debt — Accessible, Non-Judgemental Support

**Stakeholder**: People experiencing problem debt (estimated 9 million in the UK)

**Driver Category**: CUSTOMER / USER

**Driver Statement**: Access free, confidential, non-judgemental debt advice that is available when needed (including evenings and weekends), explains options in plain language, and provides a clear path to becoming debt-free.

**Context & Background**: People in debt often experience shame, anxiety, and mental health impacts. Many avoid seeking help because of stigma, long wait times for telephone advice (often 30+ minutes), or fear of judgement. A digital channel offers privacy, 24/7 availability, and the ability to engage at the user's own pace. However, those in crisis (bailiff action, eviction, utility disconnection) need immediate human support.

**Driver Intensity**: CRITICAL

**Enablers**: 24/7 digital availability; non-judgemental tone and design; clear, jargon-free explanations; immediate warm transfer to human advisers for crisis cases; Breathing Space application to stop creditor action

**Blockers**: Digital exclusion (no internet, no device); mental health crisis requiring immediate human intervention; complex debt situations (multiple creditors, joint debts, business debts) that resist digital triage

---

### SD-4: StepChange and Citizens Advice — Supplement, Not Replace, Human Advice

**Stakeholder**: StepChange Debt Charity, Citizens Advice

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Ensure the digital service supplements existing telephone and face-to-face channels rather than replacing them, with seamless warm handoff to human advisers for complex or vulnerable cases.

**Context & Background**: StepChange and Citizens Advice are the largest free debt advice providers in the UK. They support the principle of digital access but are concerned that a digital-first approach could exclude the most vulnerable people or reduce funding for human advice channels. They want the digital service to triage and handle straightforward cases, freeing human advisers for the complex cases where they add most value.

**Driver Intensity**: HIGH

**Enablers**: Clear triage that routes complex cases to human advisers; data sharing to avoid people repeating their story; continued commissioning funding for telephone and face-to-face; joint service design

**Blockers**: Digital service seen as replacement for human advice; MaPS reducing commissioning budgets on the basis that digital replaces human; poor handoff experience where people fall through gaps

---

### SD-5: Creditors — Efficient Breathing Space Administration

**Stakeholder**: Creditors (banks, building societies, utility companies, local authorities)

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Receive Breathing Space notifications digitally and respond efficiently, reducing the administrative burden of the scheme while meeting statutory obligations under the Debt Respite Scheme (Breathing Space Moratorium and Mental Health Crisis Moratorium) (England and Wales) Regulations 2020.

**Context & Background**: The Breathing Space scheme gives people in problem debt legal protection from creditor action for 60 days (standard) or the duration of mental health crisis treatment. Creditors must freeze interest, charges, and enforcement. Currently, notifications are processed through a mix of electronic and manual channels. A digital end-to-end process would reduce administrative cost for both creditors and debt advice providers.

**Driver Intensity**: MEDIUM

**Enablers**: Standardised API for Breathing Space notifications; automated creditor lookup; digital response and acknowledgement workflow; bulk processing capability for large creditors

**Blockers**: Creditors unable to invest in API integration (especially smaller creditors); inconsistent creditor data quality; disputes about debt ownership

---

## Driver-to-Goal Mapping

### Goal G-1: Reach 1.5 Million People Per Year

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: MaPS Chief Executive

**Goal Statement**: Provide debt advice or financial guidance to 1.5 million people per year by March 2029 (up from 700,000), with the digital channel handling at least 500,000 of these.

**Baseline**: 700,000 people per year (telephone and face-to-face)

**Target**: 1.5 million (700K existing channels + 500K digital + 300K improved early intervention)

---

### Goal G-2: Breathing Space Digital Processing

**Derived From Drivers**: SD-5, SD-1

**Goal Owner**: SRO

**Goal Statement**: Process 80% of Breathing Space applications digitally end-to-end by March 2028, reducing average processing time from 5 days to 1 day.

**Baseline**: 5 days average, mostly manual

**Target**: 1 day, 80% fully digital

---

### Goal G-3: User Satisfaction 80%

**Derived From Drivers**: SD-3, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Achieve 80% user satisfaction with the digital debt advice service by March 2028.

**Baseline**: No digital channel baseline; telephone satisfaction approximately 85%

**Target**: 80% digital channel satisfaction

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| MaPS | SD-1 | Expand access to 1.5M | G-1 | 1.5M people per year |
| FCA | SD-2 | Regulatory compliance | G-1 (quality gate) | FCA standards met |
| People in debt | SD-3 | Accessible, non-judgemental | G-1, G-3 | Access + satisfaction |
| StepChange/CA | SD-4 | Supplement human advice | G-1, G-3 | Warm handoff, quality |
| Creditors | SD-5 | Efficient Breathing Space | G-2 | Digital BS processing |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: MaPS (SD-1) wants digital-first efficiency; StepChange/CA (SD-4) want to protect human advice channels. Resolution: Digital service handles triage and straightforward cases; complex/vulnerable cases warm-transferred to human advisers. Commissioning funding for human channels maintained.

- **Conflict 2**: FCA (SD-2) requires human oversight for debt solution recommendations; MaPS (SD-1) wants scalable digital advice. Resolution: Digital service provides financial health assessment and options information (unregulated guidance); regulated debt advice (specific solution recommendation) requires human adviser sign-off, which can be provided via video call or telephone.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Service design | MaPS Digital | SRO | FCA, StepChange, CA | All |
| Regulatory boundary | FCA | FCA | MaPS, advice providers | Creditors |
| Commissioning model | MaPS Commissioning | MaPS CE | StepChange, CA, Treasury | All |
| Breathing Space process | MaPS/Insolvency Service | MaPS CE | Creditors, advice providers | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Debt Respite Scheme Regulations 2020 | Legislation | legislation.gov.uk | Breathing Space moratorium rules | N/A |
| FCA Debt Advice Sourcebook (CONC 8) | Regulation | FCA | Regulated debt advice requirements | N/A |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 1 Programme | Governing principles | projects/000-global/ |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Debt Advice Digital Service
**Model**: Claude Opus 4.6
