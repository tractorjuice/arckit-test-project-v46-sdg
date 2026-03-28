# Stakeholder Drivers & Goals Analysis: Modern Slavery Reporting System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Modern Slavery Reporting System (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Modern Slavery Reporting Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MS Reporting Programme Board, Home Office Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies stakeholders for the Modern Slavery Transparency Compliance platform, their drivers, goals, and outcomes. The platform will replace the current GOV.UK Modern Slavery Statement Registry with an intelligent system that enables structured data submission, cross-referencing of supply chain risks, compliance monitoring, and data sharing with law enforcement.

### Key Findings

The strongest alignment is around the inadequacy of the current system — the Independent Anti-Slavery Commissioner, NGOs, businesses, and law enforcement all agree that the existing PDF-based registry is not fit for purpose. However, significant tensions exist between transparency advocates (who want maximum data publication) and businesses (who fear reputational damage from structured data that enables comparison). Law enforcement stakeholders need intelligence-grade data sharing capabilities that require OFFICIAL-SENSITIVE handling, creating a dual-classification challenge within a single platform.

### Critical Success Factors

- Achieve structured data submission from all 17,000+ organisations in scope (GBP 36M+ turnover) within 2 years
- Enable cross-referencing of statements with Companies House, trade data, and sector risk profiles
- Provide law enforcement data sharing gateway meeting NCA requirements
- Maintain business confidence through fair, proportionate compliance assessment
- Support the Independent Anti-Slavery Commissioner's analytical capability

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Agreement on the need for system modernisation, but fundamental tensions between transparency, enforcement, and business compliance burden.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Home Secretary | Minister | HIGH | MEDIUM | Keep Satisfied — Ministerial briefings on enforcement outcomes |
| Home Office Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Modern Slavery Reporting | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| Director of Modern Slavery Unit | Policy ownership | HIGH | HIGH | Manage Closely — Policy requirements |
| Home Office Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Home Office SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, intelligence data handling |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Independent Anti-Slavery Commissioner (IASC) | Statutory role | Oversight and advocacy | HIGH | HIGH |
| National Crime Agency (NCA) | Law enforcement | Modern Slavery and Human Trafficking Unit | HIGH | HIGH |
| Police forces (43 territorial forces) | Law enforcement | Local investigation | MEDIUM | HIGH |
| Gangmasters and Labour Abuse Authority (GLAA) | Regulator | Labour exploitation enforcement | MEDIUM | HIGH |
| Companies (GBP 36M+ turnover) | Regulated entities | Statement submitters | HIGH | HIGH |
| Industry bodies (e.g., BRC, CBI) | Membership bodies | Business representation | MEDIUM | HIGH |
| Anti-Slavery International | NGO | Advocacy | LOW | HIGH |
| The Salvation Army | Charity | Victim support (government contractor) | LOW | HIGH |
| Companies House | Executive agency | Company data | MEDIUM | MEDIUM |
| HMRC | Partner department | Trade data, NMW enforcement | MEDIUM | MEDIUM |
| Foreign, Commonwealth and Development Office (FCDO) | Partner department | Overseas supply chains | MEDIUM | MEDIUM |
| CDDO | Cabinet Office | Cross-government standards | HIGH | MEDIUM |
| ICO | Regulator | Data protection (whistleblower data) | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Home Secretary   │  • Permanent Sec.   │
        │  • ICO              │  • SRO              │
        │  • CDDO             │  • Director of MS   │
        │  • Home Office SIRO │    Unit              │
        │                     │  • Chief Digital Off│
        │                     │  • IASC             │
 P      │                     │  • NCA              │
 O      │                     │  • Companies (scope)│
 W      ├─────────────────────┼─────────────────────┤
 E      │                     │                     │
 R      │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • FCDO             │  • GLAA             │
        │                     │  • Police forces    │
        │                     │  • Industry bodies  │
        │                     │  • Anti-Slavery Intl│
        │                     │  • Salvation Army   │
        │                     │  • Companies House  │
        │                     │  • HMRC             │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Independent Anti-Slavery Commissioner — Enable Analytical Oversight

**Stakeholder**: Independent Anti-Slavery Commissioner (IASC)

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: The IASC needs the ability to analyse modern slavery statements at scale — comparing year-on-year progress, identifying sectors with weak compliance, and spotting patterns that indicate supply chain risk. The current PDF-based registry makes this impossible without manual review of 17,000+ statements.

**Context & Background**: The IASC's Annual Report has repeatedly criticised the registry as a "tick-box exercise" that enables compliance without transparency. Businesses submit statements of varying quality with no structured data, making it impossible to assess whether they are genuinely addressing modern slavery risk or merely meeting the minimum legal requirement.

**Driver Intensity**: CRITICAL

---

### SD-2: National Crime Agency — Intelligence-Grade Data Sharing

**Stakeholder**: NCA Modern Slavery and Human Trafficking Unit

**Driver Category**: OPERATIONAL

**Driver Statement**: NCA needs structured supply chain data that can be cross-referenced with intelligence holdings to identify potential modern slavery in supply chains. This requires a secure data sharing gateway handling OFFICIAL-SENSITIVE material, with appropriate access controls and audit trail.

**Context & Background**: NCA currently has no systematic way to use modern slavery statements for intelligence purposes. Statements are public documents, but linking them with intelligence requires a secure analytical environment. The platform must support both the public-facing compliance function and a restricted intelligence-sharing function.

**Driver Intensity**: HIGH

---

### SD-3: Companies in Scope — Proportionate Compliance Burden

**Stakeholder**: Companies with GBP 36M+ turnover (approximately 17,000 organisations)

**Driver Category**: COMPLIANCE / FINANCIAL

**Driver Statement**: Businesses accept the reporting obligation but want a system that is proportionate, clear, and does not create competitive disadvantage for compliant firms. They fear that structured data will enable unfair comparison between companies that are genuinely addressing risks and those that simply have less complex supply chains.

**Context & Background**: Current compliance is binary — submit a statement or face reputational risk. The quality varies enormously. Major retailers (e.g., Tesco, M&S) invest significantly in supply chain due diligence, while others produce minimal statements. A structured system risks penalising transparent companies (who disclose more risk information) while rewarding opaque ones.

**Driver Intensity**: HIGH

---

### SD-4: NGOs — Maximum Transparency and Public Accountability

**Stakeholder**: Anti-Slavery International, Walk Free, FLEX

**Driver Category**: STRATEGIC

**Driver Statement**: NGOs want maximum public transparency — structured data that enables civil society to hold businesses accountable, with public dashboards showing compliance quality, sector comparisons, and year-on-year improvement.

**Driver Intensity**: HIGH

---

### SD-5: GLAA — Labour Market Enforcement Data

**Stakeholder**: Gangmasters and Labour Abuse Authority

**Driver Category**: OPERATIONAL

**Driver Statement**: GLAA needs supply chain data that helps identify labour exploitation risks in agriculture, food processing, and construction — sectors where GLAA has enforcement powers. Cross-referencing modern slavery statements with GLAA licensing data would enhance risk-based targeting.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Structured Data Submission for All In-Scope Organisations

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: Director of Modern Slavery Unit

**Goal Statement**: Transition 90% of in-scope organisations (approximately 15,300 of 17,000) from PDF statement submission to structured data submission within 24 months of platform launch.

**Success Metrics**:
- **Primary Metric**: Percentage of statements submitted as structured data
- **Secondary Metrics**:
  - Average statement quality score (to be defined)
  - Submission compliance rate (target: 95% on-time)

---

### Goal G-2: Enable Cross-Referencing and Risk Scoring

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: SRO, Modern Slavery Reporting

**Goal Statement**: Implement automated cross-referencing of modern slavery statements with Companies House data, international trade data, and sector risk profiles to generate risk scores that prioritise enforcement attention.

---

### Goal G-3: Establish Law Enforcement Data Sharing Gateway

**Derived From Drivers**: SD-2

**Goal Owner**: Home Office Chief Digital Officer / NCA

**Goal Statement**: Deliver a secure data sharing gateway between the compliance platform and NCA intelligence systems, handling OFFICIAL-SENSITIVE data with full audit trail, within 12 months of platform launch.

---

### Goal G-4: Publish Public Transparency Dashboard

**Derived From Drivers**: SD-4

**Goal Owner**: IASC (advisory) / Service Owner (delivery)

**Goal Statement**: Launch a public dashboard enabling citizens, journalists, and NGOs to search, compare, and analyse modern slavery statements by sector, geography, and quality metrics.

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: NGOs (SD-4) want maximum transparency with public dashboards comparing company performance. Companies (SD-3) fear that transparency will penalise those who disclose more risks. A company reporting 15 supply chain risks looks worse than one reporting none, even if the first is more diligent.
  - **Resolution Strategy**: INNOVATE — Design the scoring methodology to reward disclosure quality, not just risk absence. "Number of risks identified AND mitigated" scores higher than "no risks reported." Publish methodology transparently.

- **Conflict 2**: NCA (SD-2) needs OFFICIAL-SENSITIVE intelligence capabilities within the platform. The public transparency dashboard (SD-4) must be strictly separated. Architectural separation is essential.
  - **Resolution Strategy**: PHASE — Build two architecturally separate components: a public compliance platform (OFFICIAL) and a restricted intelligence platform (OFFICIAL-SENSITIVE) linked by a controlled data gateway. Law enforcement data never appears on the public platform.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 6, 7, 11 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Modern Slavery Act 2015 | Legislation | UK Parliament | Section 54 transparency | https://www.legislation.gov.uk/ukpga/2015/30 |
| IASC Annual Report 2025 | Report | IASC | Registry critique | https://www.antislaverycommissioner.co.uk/ |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Modern Slavery Reporting System
**Model**: Claude Opus 4.6
