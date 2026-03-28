# Strategic Outline Business Case (SOBC): Debt Advice Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
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
| **Distribution** | MaPS Board, HM Treasury, FCA, StepChange, Citizens Advice |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investment in a Debt Advice Digital Service operated by MaPS, following the HM Treasury Green Book Five Case Model. It is informed by ARC-003-STKE-v1.0 (stakeholder analysis) and ARC-003-REQ-v1.0 (requirements).

---

## Executive Summary

**Purpose**: An estimated 9 million UK adults have problem debt, but fewer than 700,000 access free advice annually. This business case seeks GBP 42M over 5 years to deliver a digital debt advice service providing financial health assessment, Breathing Space processing, and seamless referral to regulated advice providers.

**Problem Statement**: Demand for free debt advice consistently exceeds supply. Wait times for telephone advice often exceed 30 minutes. The Breathing Space scheme is largely manual, taking 5 days to process. Early intervention is proven to reduce debt severity and associated costs to individuals, creditors, and government — but most people only seek help at crisis point.

**Proposed Solution**: A digital-first debt advice platform providing 24/7 financial health assessment, automated Breathing Space processing, and warm referral to StepChange, Citizens Advice, and community agencies for regulated advice.

**Strategic Fit**: Directly supports SDG 1: No Poverty by preventing debt-driven poverty. Aligns with MaPS statutory objective to improve financial wellbeing, the Debt Respite Scheme Regulations 2020, and FCA Consumer Duty.

**Investment Required**: GBP 42M over 5 years

- Capital: GBP 28M
- Operational (5 years): GBP 14M

**Expected Benefits**: GBP 135M over 10 years

- Cost avoidance through early debt intervention: GBP 65M (reduced insolvency, homelessness, mental health costs)
- Efficiency savings in Breathing Space processing: GBP 20M
- Freed capacity in human advice channels (handling more complex cases): GBP 35M
- Creditor cost reduction through digital Breathing Space: GBP 15M

**Return on Investment**:

- NPV: GBP 58M (discounted at 3.5%)
- Payback Period: 36 months
- ROI: 221% over 10 years

**Recommended Option**: Option 2: Digital Triage and Breathing Space Platform

**Key Risks**:

1. FCA regulatory concerns about automated advice boundary — mitigated by early regulatory engagement and clear guidance/advice distinction
2. Digital exclusion of most vulnerable users — mitigated by maintaining human channels and assisted digital routes
3. Low creditor API adoption for Breathing Space — mitigated by phased rollout starting with major creditors

**Go/No-Go Recommendation**: **PROCEED**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: MaPS commissions free debt advice through contracts with StepChange Debt Charity, Citizens Advice, and approximately 200 community debt advice agencies. Annual capacity is approximately 700,000 people. An estimated 9 million UK adults have problem debt — the advice gap is approximately 8.3 million people per year. Those who do seek help wait an average of 12 months from first experiencing debt problems before contacting an advice provider, by which time debts have typically grown by 40%.

**Consequences of Inaction**:

- Continued GBP 8.3 billion annual cost to government from problem debt (homelessness, mental health, NHS, criminal justice)
- Breathing Space processing remains manual and slow, delaying protection for people in crisis
- Debt advice demand continues to exceed supply, with wait times rising
- Early intervention opportunity missed — each GBP 1 spent on debt advice saves GBP 2.98 in wider costs (MaPS research)

### A1.2 Strategic Alignment

- **SDG 1: No Poverty**: Debt is a primary driver of poverty; earlier intervention prevents debt-driven destitution
- **MaPS UK Strategy for Financial Wellbeing 2020-2030**: Target to increase access to debt advice
- **Debt Respite Scheme Regulations 2020**: Breathing Space digitisation
- **FCA Consumer Duty**: Ensuring good outcomes for consumers in financial difficulty
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (User-Centred), 5 (Security by Design), 8 (Privacy by Design)

## B2. Options Analysis

### Option 0: Do Nothing

**Costs (5-year)**: GBP 0 digital investment (GBP 350M+ in debt advice commissioning, no efficiency gain)

**Benefits**: GBP 0

**Recommendation**: **Reject** — Advice gap widens, Breathing Space remains manual.

---

### Option 1: Enhanced Digital Content Only

**Description**: Improve MoneyHelper website content with better debt advice information, self-help guides, and downloadable budget tools. No interactive assessment or Breathing Space digitisation.

**Costs (5-year)**: GBP 5M

**Benefits (10-year)**: GBP 12M (modest awareness improvement)

**Stakeholder Goals Met**: 10%

**Recommendation**: **Reject** — Information alone does not overcome barriers to seeking advice.

---

### Option 2: Digital Triage and Breathing Space Platform (RECOMMENDED)

**Description**: Interactive financial health assessment, automated Breathing Space processing, warm referral to human advisers, creditor API. Supplements existing human advice channels.

**Costs (5-year)**: GBP 42M

**Benefits (10-year)**: GBP 135M

**NPV**: GBP 58M | **Payback**: 36 months | **ROI**: 221%

**Stakeholder Goals Met**: 85%

**Recommendation**: **ACCEPT**

---

### Option 3: Full Digital Debt Advice Service

**Description**: End-to-end digital debt advice including regulated solution recommendations, online DRO applications, and digital debt management plan administration.

**Costs (5-year)**: GBP 95M

**Benefits (10-year)**: GBP 180M

**Pros**: Maximum digital coverage

**Cons**: FCA regulatory risk — automated regulated advice is unproven at scale and creates significant consumer protection concerns. Requires FCA authorisation for MaPS as a regulated firm (currently exempt for guidance). StepChange and CA oppose this model as it threatens their role.

**Stakeholder Goals Met**: 60% (FCA and advice provider goals NOT met)

**Recommendation**: **Reject** — Regulatory risk and stakeholder opposition make this undeliverable in the current regulatory framework.

---

## B3. Recommended Option

**Option 2** — best balance of impact, regulatory compliance, and stakeholder acceptability. Strongly positive NPV (GBP 58M) with manageable risk.

---

# PART D: FINANCIAL CASE

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 8M | GBP 10M | GBP 6M | GBP 3M | GBP 1M | GBP 28M |
| OpEx | GBP 1.5M | GBP 2.5M | GBP 3M | GBP 3.5M | GBP 3.5M | GBP 14M |
| **Total** | **GBP 9.5M** | **GBP 12.5M** | **GBP 9M** | **GBP 6.5M** | **GBP 4.5M** | **GBP 42M** |

**Funding Source**: MaPS levy funding (Financial Guidance and Claims Act 2018) supplemented by HM Treasury digital transformation allocation.

---

# PART E: MANAGEMENT CASE

**Programme Governance**: MaPS Programme Board chaired by SRO, with FCA observer status, StepChange/CA representatives, and creditor industry body representation.

**Key Risks**:

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| FCA regulatory concerns | MEDIUM | CRITICAL | Early regulatory engagement, clear guidance/advice boundary, FCA sandbox if needed |
| Digital exclusion of vulnerable users | HIGH | HIGH | Maintain human channels, assisted digital, partnership with libraries and community centres |
| Low creditor API adoption | MEDIUM | MEDIUM | Start with top 20 creditors (80% volume), industry body engagement |
| Advice provider resistance | MEDIUM | HIGH | Joint service design, protected commissioning budgets, evidence of complementary value |
| Data breach of sensitive financial data | LOW | CRITICAL | Security by Design, pen testing, DPIA, ICO engagement |

**Timeline**:

| Phase | Start | End |
|-------|-------|-----|
| Discovery/Alpha | Q3 2026 | Q1 2027 |
| Beta (Private) | Q1 2027 | Q3 2027 |
| Beta (Public) with early adopter creditors | Q3 2027 | Q1 2028 |
| Live — financial assessment + Breathing Space | Q1 2028 | |
| Creditor API expansion | Q2 2028 | Q4 2028 |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| MaPS Chief Executive | Organisation Leader | [ ] Approved | PENDING |
| HM Treasury | Funding | [ ] Approved | PENDING |
| FCA | Regulatory | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Debt Advice Digital Service
**Model**: Claude Opus 4.6
