# Stakeholder Drivers & Goals Analysis: Small Business Support Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Small Business Support Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Small Business Support Portal Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SBSP Programme Board, DBT Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies stakeholders for the Integrated Small Business Support Portal, their drivers, goals, and measurable outcomes. The portal will provide a single, personalised entry point for SMEs to access government support — grants, loans, advice, regulatory guidance, export support, and procurement opportunities — replacing the current fragmented landscape of GOV.UK pages, British Business Bank tools, and departmental microsites.

### Key Findings

The strongest alignment is around simplification — every stakeholder agrees that the current SME support landscape is fragmented and confusing. The FSB reports that 60% of small businesses are unaware of government support they are eligible for. The most significant tension is between DBT's desire for a single portal and other departments' (HMRC, DSIT, Defra) reluctance to cede ownership of their business-facing content and services. The portal must aggregate without displacing departmental accountability.

### Critical Success Factors

- Achieve personalised journey based on business type, sector, size, and location within the first interaction
- Integrate with GOV.UK One Login and Companies House to pre-populate business context
- Aggregate grant and loan eligibility from at least 50 schemes across 10 departments
- Deliver measurable increase in SME awareness and uptake of government support
- Build trust with SME community through simplicity, speed, and relevance

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the problem (fragmentation) but significant disagreement on the solution architecture (single portal vs. federated content, DBT ownership vs. cross-government governance).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Business and Trade | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DBT Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Small Business Support Portal | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DBT Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Small Business Commissioner | Statutory role | HIGH | HIGH | Manage Closely — SME advocacy |
| DBT Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Federation of Small Businesses (FSB) | Membership body | SME advocacy | MEDIUM | HIGH |
| British Chambers of Commerce (BCC) | Membership body | Business representation | MEDIUM | HIGH |
| British Business Bank (BBB) | Public body | Finance programmes | HIGH | HIGH |
| HMRC | Partner department | Tax guidance, MTD | HIGH | MEDIUM |
| Companies House | Executive agency | Business registration data | MEDIUM | HIGH |
| DSIT | Partner department | Innovation grants (Innovate UK) | MEDIUM | HIGH |
| Defra | Partner department | Rural business grants | MEDIUM | MEDIUM |
| DLUHC | Partner department | Local growth fund | MEDIUM | MEDIUM |
| Local Enterprise Partnerships (LEPs) / Combined Authorities | Local bodies | Local business support | LOW | HIGH |
| GDS | Cabinet Office | GOV.UK platform, design standards | HIGH | MEDIUM |
| CDDO | Cabinet Office | Spend control, cross-gov standards | HIGH | MEDIUM |
| SME owners (sole traders, micro, small) | Citizens/businesses | Primary users | LOW | HIGH |
| Accountants and business advisors | Professional services | Intermediary users | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HMRC             │  • Secretary of     │
        │  • GDS              │    State (DBT)       │
        │  • CDDO             │  • Permanent Sec.   │
        │  • DBT Finance Dir  │  • SRO              │
        │                     │  • Chief Digital Off│
        │                     │  • Small Business   │
 P      │                     │    Commissioner      │
 O      │                     │  • British Business │
 W      │                     │    Bank              │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Defra            │  • FSB              │
        │  • DLUHC            │  • BCC              │
        │                     │  • SME owners       │
        │                     │  • Companies House  │
        │                     │  • DSIT / Innovate  │
        │                     │  • LEPs / CAs       │
        │                     │  • Accountants      │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State for Business and Trade — Close the SME Support Gap

**Stakeholder**: Secretary of State for Business and Trade

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver on the Industrial Strategy commitment to improve SME productivity by ensuring every small business can easily find and access the government support they are entitled to, closing the estimated 60% awareness gap.

**Context & Background**: The UK has 5.5 million SMEs contributing 52% of private sector turnover. But government support is scattered across GOV.UK, British Business Bank, Growth Hubs, LEP websites, and departmental microsites. An FSB survey found that 60% of eligible businesses were unaware of at least one support scheme they could access. The Levelling Up White Paper specifically committed to improving business support in underperforming regions.

**Driver Intensity**: CRITICAL

---

### SD-2: FSB / BCC — Reduce Administrative Burden on Small Businesses

**Stakeholder**: Federation of Small Businesses (FSB) and British Chambers of Commerce (BCC)

**Driver Category**: OPERATIONAL

**Driver Statement**: Small businesses spend an average of 15 hours per month on government compliance and administration. Any new portal must reduce this burden, not add to it. The portal must be genuinely useful from the first visit, not another registration-heavy government website.

**Driver Intensity**: HIGH

---

### SD-3: British Business Bank — Improve Access to Finance for SMEs

**Stakeholder**: British Business Bank

**Driver Category**: STRATEGIC

**Driver Statement**: Channel more eligible SMEs towards BBB-supported finance products (Start Up Loans, Regional Growth Fund, Future Fund) by integrating eligibility checking and application into the portal journey.

**Driver Intensity**: HIGH

---

### SD-4: HMRC — Protect Tax Guidance Integrity

**Stakeholder**: HMRC

**Driver Category**: COMPLIANCE

**Driver Statement**: HMRC supports aggregation of business guidance but insists that tax-related content must remain authoritative from HMRC. The portal must not paraphrase or reinterpret tax guidance, as incorrect guidance creates liability.

**Driver Intensity**: HIGH

---

### SD-5: GDS — Maintain GOV.UK Design Consistency

**Stakeholder**: Government Digital Service

**Driver Category**: COMPLIANCE

**Driver Statement**: The portal must comply with GDS design standards and integrate with the GOV.UK publishing platform. GDS will resist a standalone portal that fragments the GOV.UK experience.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Increase SME Awareness of Government Support

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: SRO, Small Business Support Portal

**Goal Statement**: Increase the proportion of eligible SMEs aware of at least one relevant government support scheme from 40% to 75% within 18 months of portal launch, measured by annual business survey.

**Success Metrics**:
- **Primary Metric**: Awareness rate among eligible SMEs
- **Secondary Metrics**:
  - Portal unique visitors per month (target: 500,000 within 12 months)
  - Personalised recommendation accuracy (target: 80% of suggestions rated relevant by users)

---

### Goal G-2: Simplify Grant and Loan Application

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: Service Owner

**Goal Statement**: Reduce average time from first portal visit to grant/loan application submission from 3 hours (current cross-site journey) to 30 minutes through pre-populated forms and guided eligibility.

---

### Goal G-3: Aggregate Support Schemes Cross-Government

**Derived From Drivers**: SD-1

**Goal Owner**: DBT Chief Digital Officer

**Goal Statement**: Index and surface at least 200 government support schemes from 10+ departments with structured metadata enabling personalised recommendations based on business sector, size, location, and needs.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Secretary of State (DBT) | SD-1 | Close support gap | G-1, G-3 | Awareness, aggregation |
| FSB / BCC | SD-2 | Reduce admin burden | G-1, G-2 | Awareness, simplification |
| British Business Bank | SD-3 | Improve access to finance | G-2 | Simplify application |
| HMRC | SD-4 | Protect tax guidance | G-3 | Aggregation (with content controls) |
| GDS | SD-5 | GOV.UK consistency | G-1, G-3 | All (design compliance) |

### Conflict Analysis

- **Conflict 1**: DBT (SD-1) wants a single branded portal. GDS (SD-5) insists it should be part of GOV.UK. HMRC (SD-4) wants its content to remain on HMRC.gov.uk.
  - **Resolution Strategy**: COMPROMISE — Build as a GOV.UK service (satisfying GDS) that aggregates and links to departmental content (satisfying HMRC). Use deep linking with context passing rather than content duplication.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 1, 5, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Industrial Strategy | Policy | DBT | SME productivity | https://www.gov.uk/government/publications/industrial-strategy |
| Levelling Up White Paper | Policy | DLUHC | Regional business support | https://www.gov.uk/government/publications/levelling-up-the-united-kingdom |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Small Business Support Portal
**Model**: Claude Opus 4.6
