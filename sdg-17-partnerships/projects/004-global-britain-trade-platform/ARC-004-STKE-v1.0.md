# Stakeholder Drivers & Goals Analysis: Global Britain Trade Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Global Britain Trade Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Global Britain Trade Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DBT Digital, HMRC Trade, UK Export Finance, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Global Britain Trade Platform, their underlying drivers, and how these map to programme goals and measurable outcomes. The platform will support international trade partnership management, FTA impact modelling, and UK trade data integration to advance SDG 17's trade-related targets.

### Key Findings

The Global Britain Trade Platform bridges domestic trade policy, international negotiation, and business-facing services. The strongest alignment is around the need for integrated trade data — HMRC customs data, DBT trade promotion data, UKEF export finance, and FTA utilisation rates are currently siloed, preventing a unified view of UK trade performance. The key tension is between DBT's desire for a business-facing platform that promotes UK exports and HMRC's primary focus on customs compliance and revenue protection. Additionally, trade negotiation data is highly sensitive (OFFICIAL-SENSITIVE) and must be segregated from public trade statistics.

### Critical Success Factors

- Integrate HMRC Customs Declaration Service data with DBT trade promotion records to measure FTA utilisation
- Model the trade impact of new and proposed FTAs to support negotiation and Parliamentary scrutiny
- Provide UK businesses with a single portal for trade opportunities, FTA tariff information, and export finance
- Maintain strict separation between public trade statistics and sensitive trade negotiation data
- Support SDG 17.11 (increase developing country exports) monitoring through preferential trade data analysis

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Agreement on the value of integrated trade data but significant cultural differences between DBT (promotion-focused, outward-facing) and HMRC (compliance-focused, enforcement-oriented). UK Export Finance operates semi-independently with its own systems. The International Trade Committee provides robust Parliamentary scrutiny. Post-Brexit FTA negotiations have created a dynamic policy environment requiring flexible, rapidly updatable systems.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Business and Trade | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DBT Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Global Britain Trade Platform | Programme Sponsor (DBT) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DBT Chief Digital Information Officer | Digital leadership | HIGH | HIGH | Manage Closely — Architecture, standards |
| DBT Trade Policy Director | FTA negotiation and policy | HIGH | HIGH | Manage Closely — Trade modelling requirements |
| DBT Export Promotion Director | Export support services | HIGH | HIGH | Manage Closely — Business-facing requirements |
| DBT Chief Economist | Trade impact analysis | MEDIUM | HIGH | Keep Informed — Economic modelling |
| DBT Finance Director | Budget management | HIGH | MEDIUM | Keep Satisfied — Spend controls |
| DBT SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| HMRC | Partner department | Customs data, trade statistics | HIGH | HIGH |
| UK Export Finance (UKEF) | Government | Export credit and finance | MEDIUM | HIGH |
| CDDO | Cabinet Office | Digital standards, spend control | HIGH | MEDIUM |
| International Trade Committee | House of Commons | Parliamentary scrutiny | HIGH | MEDIUM |
| Trade Remedies Authority (TRA) | Arms-length body | Anti-dumping, safeguard measures | MEDIUM | MEDIUM |
| WTO | International | Trade data standards, disputes | MEDIUM | MEDIUM |
| FTA partner countries | International | Bilateral trade monitoring | MEDIUM | HIGH |
| UK business community (exporters) | Private sector | Users of trade services | LOW | HIGH |
| CBI / Federation of Small Businesses | Business bodies | Trade policy advocacy | LOW | HIGH |
| British Chambers of Commerce (BCC) | Business body | Overseas market access | LOW | HIGH |
| Developing country trade partners | International | SDG 17.11 beneficiaries | LOW | MEDIUM |
| ONS | Statistical authority | Trade statistics methodology | MEDIUM | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * Secretary of     |
        |  * DBT Finance Dir  |    State            |
        |  * DBT SIRO         |  * Perm Sec         |
        |  * Int'l Trade Ctte |  * SRO              |
 P      |                     |  * DBT CDIO         |
 O      |                     |  * Trade Policy Dir |
 W      |                     |  * HMRC             |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Developing       |  * UKEF             |
        |    country partners |  * UK businesses    |
        |  * WTO              |  * CBI/FSB/BCC      |
        |  * ONS              |  * FTA partners     |
        |                     |  * TRA              |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Demonstrating Global Britain Trade Success

**Stakeholder**: Secretary of State for Business and Trade

**Driver Category**: STRATEGIC

**Driver Statement**: Demonstrate measurable success of post-Brexit trade policy, showing that new FTAs deliver tangible benefits to UK businesses and that the UK is an outward-looking, trading nation, supporting the Export Strategy target of GBP 1 trillion in exports by 2030.

**Context & Background**:
Post-Brexit, the UK has negotiated FTAs with Australia, New Zealand, CPTPP, and others, while rolling over EU FTAs. Ministers face Parliamentary scrutiny on whether these agreements deliver promised benefits. The Export Strategy sets an ambitious GBP 1 trillion export target. The Secretary of State needs data that demonstrates FTA utilisation, export growth, and trade partnership outcomes.

**Driver Intensity**: CRITICAL

**Enablers**:

- Integrated platform linking FTA provisions to actual trade flows
- FTA utilisation measurement (what percentage of eligible trade uses FTA preferential tariffs)
- Export growth dashboards by market, sector, and business size
- Success stories and case studies from trade promotion programmes

**Blockers**:

- FTA utilisation data sits in HMRC (customs declarations), not DBT
- Time lag between FTA entry-into-force and measurable trade impact
- Attribution challenge — export growth has many causes beyond FTAs

---

### SD-2: HMRC — Customs Data Integrity and Revenue Protection

**Stakeholder**: HMRC (Customs and International Trade Directorate)

**Driver Category**: COMPLIANCE

**Driver Statement**: Maintain the integrity and security of Customs Declaration Service data, ensuring that any data sharing with DBT does not compromise customs enforcement, revenue protection, or trader confidentiality.

**Context & Background**:
HMRC processes approximately 300 million customs declarations per year through the Customs Declaration Service (CDS). This data contains commercially sensitive trader information and is used for customs enforcement, revenue collection, and trade statistics. HMRC has statutory obligations around trader confidentiality and is cautious about sharing granular data that could identify individual businesses.

**Driver Intensity**: HIGH

**Enablers**:

- Aggregated/anonymised data sharing (no individual trader identification)
- Clear legal basis under Digital Economy Act 2017 or Statistics of Trade Act 1947
- Data sharing agreement with DBT approved by HMRC SIRO
- HMRC retains control of its data (federated access, not data copy)

**Blockers**:

- Requests for trader-level granular data
- Unclear legal basis for sharing
- Reputational risk if trader data is breached

---

### SD-3: UK Businesses — Simple Access to Trade Opportunities

**Stakeholder**: UK businesses (exporters, SMEs, large corporates)

**Driver Category**: OPERATIONAL

**Driver Statement**: Access a single, simple portal that tells them what tariff preferences exist under FTAs, how to use them, what export support is available, and what trade opportunities exist in target markets, without navigating multiple government websites and databases.

**Context & Background**:
UK businesses currently navigate multiple government services: Check How to Export Goods (HMRC), great.gov.uk (DBT), UK Export Finance portal (UKEF), Trade Remedies Service (TRA), and individual FTA legal texts. SMEs in particular lack the resource to navigate this complexity. The Export Strategy acknowledges that only 1 in 10 UK businesses export, partly due to complexity and perceived risk.

**Driver Intensity**: MEDIUM

**Enablers**:

- Single portal integrating tariff lookup, FTA rules of origin, export support, and finance
- Plain language guidance (not legal FTA text)
- Personalised recommendations based on business sector and target market
- Integration with great.gov.uk export support journey

**Blockers**:

- Fragmented service ownership across DBT, HMRC, UKEF
- FTA legal complexity that is difficult to simplify without losing accuracy
- Different departments' resistance to ceding "their" user journey to a unified platform

---

### SD-4: DBT Trade Policy — FTA Impact Modelling

**Stakeholder**: DBT Trade Policy Directorate

**Driver Category**: STRATEGIC

**Driver Statement**: Access sophisticated trade impact modelling tools that quantify the economic effects of existing and proposed FTAs, supporting negotiation strategy, Parliamentary scrutiny, and post-implementation review commitments.

**Context & Background**:
The UK is legally required to publish impact assessments for new FTAs and conduct post-implementation reviews. DBT economists use Computable General Equilibrium (CGE) models and gravity models, but these are currently disconnected from live trade data. Connecting modelling tools to real HMRC trade flows would enable continuous FTA performance monitoring, not just point-in-time assessments.

**Driver Intensity**: HIGH

**Enablers**:

- Real-time trade data feeds from HMRC for FTA impact measurement
- Historical trade data for counterfactual analysis (what would trade have been without FTA)
- Tariff schedule data for all FTAs (including staging/phase-down schedules)
- Integration with CGE/gravity model inputs

**Blockers**:

- HMRC trade data latency (currently ~2 months for validated figures)
- Attribution methodology for isolating FTA effects from other trade drivers
- Sensitivity of ongoing negotiation positions (modelling assumptions are OFFICIAL-SENSITIVE)

---

### SD-5: UK Export Finance — Export Credit Integration

**Stakeholder**: UK Export Finance (UKEF)

**Driver Category**: OPERATIONAL

**Driver Statement**: Integrate UKEF products (export credit insurance, direct lending, guarantees) into the trade platform to increase awareness and uptake of export finance, supporting the UKEF mandate to help UK businesses win international contracts.

**Context & Background**:
UKEF is the UK's export credit agency, providing GBP 6-8 billion annually in export finance support. Awareness of UKEF products remains low among SMEs. Integrating UKEF into the trade platform would surface relevant finance options at the point where businesses are exploring export opportunities.

**Driver Intensity**: MEDIUM

**Enablers**:

- API integration between trade platform and UKEF systems
- UKEF product eligibility displayed alongside market/FTA information
- Referral pathway from trade platform to UKEF application process
- UKEF case study data contributing to trade success metrics

**Blockers**:

- UKEF systems are legacy and may not support modern API integration without investment
- Credit assessment data is highly confidential and cannot be exposed on shared platform
- UKEF operates semi-independently with its own governance

---

## Driver-to-Goal Mapping

### Goal G-1: FTA Utilisation Measurement

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: DBT Chief Economist

**Goal Statement**: Measure FTA utilisation rates (percentage of eligible trade using preferential tariffs) for all UK FTAs, with quarterly updates, within 18 months.

**Success Metrics**:

- **Primary Metric**: FTA utilisation rate published quarterly for all UK FTAs
- **Secondary Metrics**:
  - FTA utilisation by sector (HS chapter level)
  - FTA utilisation by business size (SME vs. large)
  - Comparison with EU utilisation rates for equivalent FTAs

**Baseline**: No systematic FTA utilisation measurement exists

**Target**: Quarterly FTA utilisation reports covering all UK FTAs

---

### Goal G-2: Integrated Trade Portal for Businesses

**Derived From Drivers**: SD-1, SD-3, SD-5

**Goal Owner**: DBT Export Promotion Director

**Goal Statement**: Launch a single trade portal integrating tariff lookup, FTA guidance, export support, and UKEF finance options, achieving 50,000 monthly unique business users within 12 months of launch.

**Success Metrics**:

- **Primary Metric**: Monthly unique business users: 50,000
- **Secondary Metrics**:
  - User satisfaction: 4.0/5.0 (GDS standard)
  - Referrals to UKEF: 500/month
  - FTA tariff lookups: 100,000/month

**Baseline**: great.gov.uk ~30,000 monthly users; separate HMRC tariff tool ~40,000 monthly users; no integration

**Target**: 50,000 monthly users on integrated platform

---

### Goal G-3: Real-Time Trade Data Integration

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: DBT CDIO

**Goal Statement**: Establish automated data feeds from HMRC CDS providing aggregated UK trade data to the platform with a maximum 30-day lag (vs. current 60-day lag), within 24 months.

**Success Metrics**:

- **Primary Metric**: Trade data lag: < 30 days from customs declaration to platform availability
- **Secondary Metrics**:
  - Data coverage: 100% of UK goods trade
  - Reconciliation with published ONS trade statistics: within 2% tolerance
  - Automated data quality checks: 99% pass rate

**Baseline**: 60-day lag; manual data extraction; limited coverage

**Target**: < 30 days; automated; 100% goods trade coverage

---

### Goal G-4: SDG 17.11 Monitoring (Developing Country Exports)

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: DBT Trade Policy Director

**Goal Statement**: Monitor and report UK's contribution to SDG 17.11 (increase developing country exports), tracking preferential trade scheme utilisation by Least Developed Countries (LDCs) and developing countries, within 18 months.

**Success Metrics**:

- **Primary Metric**: LDC preferential trade scheme utilisation rate published annually
- **Secondary Metrics**:
  - UK Developing Countries Trading Scheme (DCTS) utilisation by country
  - Value of developing country exports to UK under preferential terms
  - Contribution to ONS SDG Dashboard (Project 003) indicator 17.11.1

**Baseline**: Limited monitoring of DCTS utilisation; no link to SDG framework

**Target**: Annual SDG 17.11 report with country-level utilisation data

---

## Goal-to-Outcome Mapping

### Outcome O-1: Evidence-Based UK Trade Policy

**Supported Goals**: G-1, G-3, G-4

**Outcome Statement**: UK trade policy decisions are informed by real-time trade data and FTA performance measurement, improving negotiation outcomes and policy targeting.

**Business Value**:

- **Strategic Impact**: Better FTA negotiations informed by utilisation data from existing agreements
- **Financial Impact**: Increased FTA utilisation worth estimated GBP 2-5B in tariff savings for UK businesses
- **International Impact**: Demonstrable contribution to SDG 17.11 (developing country exports)

---

### Outcome O-2: UK Export Growth Acceleration

**Supported Goals**: G-2

**Outcome Statement**: UK businesses increase export participation and value through simplified access to trade information, FTA guidance, and export finance, contributing to the GBP 1 trillion export target.

**Business Value**:

- **Financial Impact**: Estimated GBP 500M-1B additional exports from improved FTA awareness and UKEF uptake
- **Citizen Impact**: Export-supported jobs in UK regions

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Trade success | G-1 | FTA utilisation | O-1 | Evidence-based policy |
| Secretary of State | SD-1 | Trade success | G-2 | Trade portal | O-2 | Export growth |
| HMRC | SD-2 | Data integrity | G-3 | Data integration | O-1 | Evidence-based policy |
| UK businesses | SD-3 | Simple access | G-2 | Trade portal | O-2 | Export growth |
| Trade Policy | SD-4 | FTA modelling | G-1 | FTA utilisation | O-1 | Evidence-based policy |
| UKEF | SD-5 | Export credit | G-2 | Trade portal | O-2 | Export growth |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DBT (SD-1) wants granular trader-level data to measure FTA impact; HMRC (SD-2) insists on aggregated/anonymised data to protect trader confidentiality
  - **Resolution Strategy**: Statistical Disclosure Control — HMRC provides aggregated data at HS6 commodity/country level, suppressing cells with fewer than 5 traders. DBT accepts aggregated analysis rather than trader-level data.

- **Conflict 2**: Businesses (SD-3) want a single unified portal; DBT, HMRC, and UKEF each want to maintain their own service identity and user journey
  - **Resolution Strategy**: Federated front-end — single discovery point with branded service journeys. Users start on the trade platform, then seamlessly transition to HMRC (tariff details), DBT (export support), or UKEF (finance) as needed, with shared navigation and session context.

**Synergies**:

- **Synergy 1**: FTA utilisation measurement (G-1) serves both political accountability (SD-1) and economic modelling (SD-4)
- **Synergy 2**: Integrated portal (G-2) increases UKEF product visibility (SD-5) while simplifying business access (SD-3)

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | Solution Architect | DBT CDIO | HMRC Digital, CDDO | UKEF, TRA |
| Trade data sharing | Data Lead | SRO | HMRC SIRO, ICO | ONS |
| Business user experience | UX Lead | DBT Export Promotion Dir | UK businesses, BCC, CBI | HMRC, UKEF |
| FTA modelling methodology | DBT Chief Economist | Trade Policy Director | HMRC Statistics | Int'l Trade Committee |
| Security architecture | Security Architect | DBT SIRO | NCSC, HMRC Security | Programme team |
| SDG reporting | SDG Lead | SRO | ONS, Cabinet Office SDG Unit | FCDO |

### Escalation Path

1. **Level 1**: Product Manager (day-to-day delivery decisions)
2. **Level 2**: SRO and Programme Board (cross-department disputes, scope, budget)
3. **Level 3**: DBT Permanent Secretary (strategic disputes with HMRC, Ministerial escalation)

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme SRO | | | |
| DBT CDIO | | | |
| DBT Trade Policy Director | | | |
| HMRC representative | | | |

---

## Appendices

### Appendix A: Key References

- Export Strategy (2022)
- Integrated Review Refresh (2023)
- UK Developing Countries Trading Scheme (DCTS) regulations
- Statistics of Trade Act 1947
- Digital Economy Act 2017
- UN SDG Target 17.11 (developing country exports)
- WTO Trade Facilitation Agreement
- ARC-000-PRIN-v1.0 (SDG 17 Architecture Principles)

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Global Britain Trade Platform
**Model**: Claude Opus 4.6
