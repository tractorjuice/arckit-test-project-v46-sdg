# Project Requirements: Global Britain Trade Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
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
| **Distribution** | DBT Digital, HMRC Trade, UK Export Finance, ONS Trade Statistics, SDG 17 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Global Britain Trade Platform, covering FTA impact modelling, trade data integration, business-facing trade services, and SDG 17 trade indicator monitoring.

---

## Executive Summary

### Business Context

Post-Brexit, the UK has negotiated independent FTAs with 73+ countries. However, FTA utilisation rates are not systematically measured, trade data sits in silos (HMRC customs, DBT promotion, UKEF export finance), and UK businesses struggle to navigate fragmented government trade services. The Global Britain Trade Platform will integrate trade data, measure FTA effectiveness, support exporters, and monitor SDG 17 trade-related targets.

### Objectives

- Measure FTA utilisation rates for all UK FTAs with quarterly updates
- Integrate HMRC CDS data with DBT trade promotion and UKEF export finance data
- Launch an integrated trade portal for UK businesses, achieving 50,000 monthly users
- Support SDG 17.11 monitoring (developing country export share)
- Enable FTA impact modelling connecting trade policy to real trade flows

### Expected Outcomes

- Evidence-based UK trade policy informed by FTA utilisation data
- GBP 2-5B estimated tariff savings from increased FTA awareness and utilisation
- GBP 500M-1B additional exports from simplified trade services
- Demonstrable UK contribution to SDG 17 trade targets

### Project Scope

**In Scope**:

- FTA utilisation measurement and reporting
- HMRC CDS trade data integration (aggregated, anonymised)
- Business-facing integrated trade portal (tariff lookup, FTA guidance, export support, UKEF products)
- FTA impact modelling tools for trade policy analysis
- SDG 17 trade indicator monitoring (17.10, 17.11, 17.12)
- Developing Countries Trading Scheme (DCTS) utilisation tracking

**Out of Scope**:

- HMRC customs enforcement and compliance systems
- FTA negotiation support systems (OFFICIAL-SENSITIVE, separate secure environment)
- UKEF credit assessment and underwriting systems
- Business grants administration
- Customs declaration processing

---

## Business Requirements

### BR-1: FTA Utilisation Measurement

**Description**: Measure and report FTA utilisation rates (percentage of eligible trade using preferential tariff rates) for all UK FTAs, with quarterly granularity.

**Rationale**: The UK cannot evaluate FTA effectiveness without knowing how much eligible trade actually uses preferential tariffs. No systematic measurement currently exists.

**Success Criteria**:

- FTA utilisation rates published quarterly for all UK FTAs
- Disaggregation by HS chapter (sector), partner country, and business size (SME vs. large)
- Historical baseline from first available data point
- Comparison methodology with EU FTA utilisation rates (where comparable)

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), DBT Trade Policy (SD-4)

---

### BR-2: Integrated Trade Data Platform

**Description**: Integrate aggregated HMRC customs data, DBT trade promotion records, and UKEF export finance data to provide a unified view of UK trade performance.

**Rationale**: Trade data is currently siloed. HMRC holds customs declarations, DBT holds trade promotion activity, UKEF holds export finance records. No unified view exists.

**Success Criteria**:

- Aggregated trade data available with < 30-day lag (vs. current 60 days)
- 100% UK goods trade coverage from HMRC CDS
- Trade promotion activity linkable to trade flow outcomes
- UKEF export finance correlated with export growth in target markets

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), HMRC (SD-2)

---

### BR-3: Business-Facing Trade Portal

**Description**: Provide UK businesses with a single portal for tariff lookup, FTA rules of origin guidance, export support, and UKEF finance options.

**Rationale**: UK businesses currently navigate 4+ separate government services for trade information. Only 1 in 10 UK businesses export, partly due to complexity.

**Success Criteria**:

- Single entry point for tariff, FTA, export support, and finance information
- 50,000 monthly unique business users within 12 months of launch
- User satisfaction 4.0/5.0 (GDS standard)
- UKEF referrals: 500/month

**Priority**: MUST_HAVE

**Stakeholder**: UK businesses (SD-3), UKEF (SD-5)

---

### BR-4: FTA Impact Modelling

**Description**: Provide trade policy analysts with tools to model the economic impact of existing and proposed FTAs, connecting modelling outputs to real trade flow data.

**Rationale**: UK is legally required to publish FTA impact assessments and conduct post-implementation reviews. Current models are disconnected from live trade data.

**Success Criteria**:

- FTA impact dashboard showing actual vs. predicted trade flows for each FTA
- Post-implementation review data available within 3 years of FTA entry-into-force
- Modelling inputs refreshed with latest HMRC trade data (< 30-day lag)

**Priority**: SHOULD_HAVE

**Stakeholder**: DBT Trade Policy (SD-4), International Trade Committee

---

### BR-5: SDG 17 Trade Indicator Monitoring

**Description**: Monitor and report UK's contribution to SDG 17 trade-related targets, particularly 17.11 (increase developing country exports).

**Rationale**: The UK Developing Countries Trading Scheme (DCTS) provides preferential market access to 65 developing countries. Monitoring utilisation demonstrates UK commitment to SDG 17.

**Success Criteria**:

- DCTS utilisation rate published annually by country
- LDC export share to UK tracked and reported
- Data supplied to ONS SDG Progress Dashboard (Project 003) for indicator 17.11.1
- Contribution to UK Voluntary National Review evidence base

**Priority**: SHOULD_HAVE

**Stakeholder**: Secretary of State (SD-1), ONS SDG Dashboard (Project 003)

---

## Functional Requirements

### User Personas

#### Persona 1: UK Business Exporter (SME)

- **Role**: Owner or export manager of a small/medium UK business
- **Goals**: Find out what tariff preferences exist for their products in target markets
- **Pain Points**: FTA texts are impenetrable; multiple government websites; does not know about UKEF
- **Technical Proficiency**: Low

#### Persona 2: DBT Trade Policy Analyst

- **Role**: Analyses FTA impact, prepares post-implementation reviews
- **Goals**: Access trade flow data linked to FTA provisions, model counterfactuals
- **Pain Points**: HMRC data arrives late and in raw form; no FTA utilisation metrics
- **Technical Proficiency**: High

#### Persona 3: DBT Export Adviser

- **Role**: Advises UK businesses on export opportunities in overseas markets
- **Goals**: Access market intelligence, FTA benefits, and UKEF products to advise businesses
- **Pain Points**: Information spread across multiple internal systems; cannot show business users integrated view
- **Technical Proficiency**: Medium

#### Persona 4: Parliamentary Researcher

- **Role**: Analyses trade policy for International Trade Committee
- **Goals**: Assess FTA performance, scrutinise government trade claims
- **Pain Points**: Published trade data lacks FTA attribution; modelling assumptions opaque
- **Technical Proficiency**: Medium-High

---

### Functional Requirements Detail

#### FR-1: FTA Utilisation Dashboard

**Description**: The system must calculate and display FTA utilisation rates from HMRC customs declaration data, showing the percentage of eligible trade using preferential tariff rates.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given HMRC CDS data, when FTA utilisation is calculated, then it shows the proportion of imports claiming preferential tariffs vs. total eligible imports under each FTA
- [ ] Given the utilisation dashboard, when filtered by FTA, then data is disaggregated by HS chapter, partner country, and quarter
- [ ] Given a specific FTA, when utilisation is low (< 50%), then the system highlights sectors with highest underutilisation
- [ ] Given historical data, when trend analysis is displayed, then utilisation trajectories show whether FTA uptake is improving post-entry-into-force

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Tariff Lookup and FTA Guidance

**Description**: The system must provide UK businesses with the ability to look up tariff rates for their products, identify applicable FTA preferences, and understand rules of origin requirements.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a UK exporter, when they enter their product (HS code or description) and destination country, then the system displays applicable tariff rates (MFN and any FTA preferential rate)
- [ ] Given an FTA preferential rate, when selected, then the system shows rules of origin requirements in plain language
- [ ] Given a product/country combination with no FTA, then the system shows the MFN rate and any pending FTA negotiations
- [ ] Given a business user, when they search by product description (not HS code), then the system suggests relevant HS codes using commodity code lookup

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-3: HMRC Trade Data Integration

**Description**: The system must ingest aggregated, anonymised trade data from HMRC Customs Declaration Service.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given HMRC CDS export data, when ingested, then it is aggregated at HS6/country level with trader identities suppressed
- [ ] Given ingested data, when validated, then it reconciles with published ONS trade statistics within 2% tolerance
- [ ] Given the data feed, when new data arrives, then the platform is updated within 24 hours of receipt
- [ ] Given data at HS6/country level, when a cell has fewer than 5 traders, then it is suppressed (statistical disclosure control)

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: UKEF Product Integration

**Description**: The system must display relevant UK Export Finance products alongside market and FTA information.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a user exploring an export market, when UKEF products are available for that market, then product summaries are displayed (insurance, lending, guarantees)
- [ ] Given a UKEF product, when selected, then a referral pathway to the UKEF application process is provided
- [ ] Given UKEF case study data, when relevant to the user's sector/market, then success stories are displayed
- [ ] Given UKEF product eligibility criteria, when a user's profile is known, then products are filtered for relevance

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-5: FTA Impact Analysis Tools

**Description**: The system must provide trade policy analysts with tools to compare actual post-FTA trade flows with pre-FTA baselines and model predictions.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given an FTA, when post-implementation review data is requested, then the system shows actual trade flows vs. predicted flows from the impact assessment
- [ ] Given actual vs. predicted comparison, when divergence exceeds 20%, then the system flags for analyst investigation
- [ ] Given historical trade data, when a counterfactual is requested, then the system estimates what trade would have been without the FTA (using gravity model approach)
- [ ] Given modelling outputs, when published, then they include confidence intervals and methodology documentation

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-6: DCTS Utilisation Tracking

**Description**: The system must track utilisation of the UK Developing Countries Trading Scheme by beneficiary country.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given HMRC import data, when DCTS preference claims are identified, then utilisation rates are calculated per beneficiary country
- [ ] Given DCTS utilisation data, when published, then it supports SDG indicator 17.11.1 (developing country share of global exports)
- [ ] Given the DCTS, when a country graduates from LDC status, then the system adjusts calculations accordingly
- [ ] Given annual DCTS data, when compiled, then it is submitted to ONS SDG Progress Dashboard (Project 003) via API

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-7: Export Opportunity Matching

**Description**: The system must match UK businesses with export opportunities based on their sector, products, and target markets.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a registered UK business with a profile (sector, HS codes, target markets), when new trade opportunities arise, then the business receives notifications
- [ ] Given trade promotion events (trade missions, exhibitions), when relevant to a user's profile, then they are surfaced
- [ ] Given great.gov.uk integration, when a business navigates from trade opportunities, then they can access DBT export support services seamlessly

**Priority**: COULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Trade Portal Performance

**Requirement**: Business-facing portal must respond within 2 seconds at the 95th percentile. Tariff lookup must respond within 500ms.

- Tariff lookup API: < 500ms (p95)
- Dashboard pages: < 2 seconds (p95)
- Trade data API: < 300ms (p95)
- FTA impact model execution: < 30 seconds for country-level analysis

**Load Conditions**:

- Peak load: 5,000 concurrent business users
- Trade data queries: 100,000/month
- Tariff lookups: 200,000/month

**Priority**: HIGH

---

### Availability Requirements

#### NFR-A-1: Trade Portal Availability

**Requirement**: 99.9% uptime for business-facing portal. Trade data API: 99.9%.

**RTO**: 30 minutes
**RPO**: 5 minutes

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Trader Data Protection

**Requirement**: Individual trader data from HMRC must never be identifiable on the platform. Statistical disclosure control applied at all aggregation levels (minimum 5 traders per cell).

**Priority**: CRITICAL

#### NFR-SEC-2: Trade Negotiation Segregation

**Requirement**: Trade negotiation data and modelling assumptions (OFFICIAL-SENSITIVE) must be strictly segregated from the public-facing platform. No data leakage between environments.

**Priority**: CRITICAL

#### NFR-SEC-3: Authentication

**Requirement**: Business users may access public tariff information without authentication. Registered features (export opportunity matching, personalised recommendations) require GOV.UK One Login. Internal DBT/HMRC users authenticated via departmental SSO.

**Priority**: HIGH

---

### Compliance Requirements

#### NFR-C-1: Statistics of Trade Act 1947

**Requirement**: Trade data handling must comply with the Statistics of Trade Act 1947, which governs the confidentiality of customs declarations.

**Priority**: CRITICAL

#### NFR-C-2: GDS Service Standard

**Requirement**: Business-facing portal must meet all 14 points of the GDS Service Standard, pass GDS service assessment, and use GDS Design System.

**Priority**: MUST_HAVE

#### NFR-C-3: Accessibility

**Requirement**: WCAG 2.1 Level AA compliance. Support for screen readers, keyboard navigation, high contrast mode.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: HMRC Customs Declaration Service

**Purpose**: Ingest aggregated, anonymised UK trade data.

**Integration Type**: Batch data transfer (daily) via Cross-Government Data Sharing Platform (Project 002)

**Data Exchanged**:

- **From HMRC to Platform**: Aggregated goods trade data at HS6/country level, preferential tariff claims, DCTS preference utilisation

**Authentication**: Data sharing agreement under Statistics of Trade Act 1947 / Digital Economy Act 2017

**SLA**: Data available within 30 days of customs declaration

**Priority**: CRITICAL

---

### INT-2: UK Trade Tariff Database

**Purpose**: Provide current MFN and preferential tariff rates for all HS codes and partner countries.

**Integration Type**: API (existing HMRC UK Trade Tariff API)

**Data Exchanged**:

- **From HMRC to Platform**: Tariff rates, rules of origin, FTA tariff staging schedules

**Priority**: MUST_HAVE

---

### INT-3: UKEF Systems

**Purpose**: Display UKEF product information and enable referrals.

**Integration Type**: RESTful API

**Data Exchanged**:

- **From UKEF to Platform**: Product catalogue, eligibility criteria, case studies
- **From Platform to UKEF**: Referral requests with business context

**Priority**: SHOULD_HAVE

---

### INT-4: great.gov.uk

**Purpose**: Integrate with existing DBT export promotion platform.

**Integration Type**: Deep linking and shared session context

**Data Exchanged**:

- **Bidirectional**: User journey context, export opportunity data, trade event listings

**Priority**: SHOULD_HAVE

---

### INT-5: ONS SDG Progress Dashboard (Project 003)

**Purpose**: Supply trade-related SDG indicator data.

**Integration Type**: API

**Data Exchanged**:

- **From Platform to ONS**: SDG 17.10 (tariff prevalence), 17.11 (developing country exports), 17.12 (duty-free access) indicator values

**Priority**: SHOULD_HAVE

---

### INT-6: Cross-Government Data Sharing Platform (Project 002)

**Purpose**: Access HMRC trade data via federated API gateway; provide trade data to other SDG 17 projects.

**Integration Type**: RESTful API via federated gateway

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Trade Flow

**Description**: Aggregated UK trade data at HS6/country/period level

**Key Attributes**: hs6_code, partner_country (ISO 3166-1), flow_direction (import/export), period (YYYY-MM), value_gbp, quantity, unit, tariff_type (MFN/preferential/DCTS), fta_reference

**Data Volume**: ~2M records/year (HS6 x countries x months)

**Data Classification**: OFFICIAL (aggregated; no trader identification)

#### Entity 2: FTA Provision

**Description**: FTA tariff concession record

**Key Attributes**: fta_id, partner_country, hs_code_range, mfn_rate, preferential_rate, staging_schedule, rules_of_origin, entry_into_force_date

**Data Volume**: ~500,000 tariff lines across all UK FTAs

**Data Classification**: OFFICIAL — PUBLIC (FTA texts are public)

#### Entity 3: DCTS Beneficiary

**Description**: Developing country eligible for DCTS preferences

**Key Attributes**: country_code, country_name, dcts_framework (Comprehensive/Enhanced/Standard), ldc_status, graduation_date, eligible_hs_codes

**Data Volume**: 65 beneficiary countries

**Data Classification**: OFFICIAL — PUBLIC

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: HMRC trade data cannot include individual trader identification (Statistics of Trade Act 1947)

**TC-2**: FTA negotiation modelling environment must be physically/logically separated from public platform

**TC-3**: Must integrate with existing HMRC UK Trade Tariff API (cannot modify HMRC systems)

### Business Constraints

**BC-1**: Budget cap of GBP 20M over 3 years

**BC-2**: Must launch business-facing portal within 12 months to support Export Strategy targets

**BC-3**: FTA impact modelling must not reveal UK negotiation positions (OFFICIAL-SENSITIVE)

### Assumptions

**A-1**: HMRC will agree to data sharing arrangement for aggregated CDS data (Statistics of Trade Act 1947 basis)

**A-2**: UKEF will develop API capability for product catalogue access

**A-3**: great.gov.uk will support deep linking and session sharing

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| FTA utilisation measurement | None | All UK FTAs quarterly | 18 months | Platform analytics |
| Trade portal monthly users | 0 | 50,000 | 12 months post-launch | Web analytics |
| Trade data lag | 60 days | < 30 days | 24 months | Data pipeline monitoring |
| UKEF referrals | 0 | 500/month | 12 months | Referral tracking |
| DCTS utilisation report | None | Annual by country | 18 months | Platform analytics |
| User satisfaction | N/A | 4.0/5.0 | 6 months post-launch | User surveys |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| DBT CDIO | Enterprise Architect | [ ] Approved | PENDING | |
| DBT Trade Policy Director | Policy requirements | [ ] Approved | PENDING | |
| HMRC representative | Data sharing | [ ] Approved | PENDING | |
| UKEF representative | Export finance integration | [ ] Approved | PENDING | |
| CDDO | Cross-government standards | [ ] Approved | PENDING | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| FTA | Free Trade Agreement — bilateral or multilateral trade treaty |
| CDS | Customs Declaration Service — HMRC system processing UK customs declarations |
| DCTS | Developing Countries Trading Scheme — UK preferential trade for developing countries |
| HS Code | Harmonized System code — international product classification (6+ digits) |
| MFN | Most Favoured Nation — default WTO tariff rate without preferential agreement |
| UKEF | UK Export Finance — government export credit agency |
| CRS++ | Creditor Reporting System — OECD classification for aid and trade |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 17 Architecture Principles
- ARC-004-STKE-v1.0 — Global Britain Trade Platform Stakeholder Analysis
- Export Strategy (2022)
- UK Developing Countries Trading Scheme regulations
- Statistics of Trade Act 1947
- WTO Trade Facilitation Agreement

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Global Britain Trade Platform
**Model**: Claude Opus 4.6
