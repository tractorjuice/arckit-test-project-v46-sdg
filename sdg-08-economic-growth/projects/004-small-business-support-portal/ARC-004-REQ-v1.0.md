# Project Requirements: Small Business Support Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Small Business Support Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Small Business Support Portal |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SBSP Programme Board, DBT Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Integrated Small Business Support Portal, providing a single personalised entry point for SMEs to access government support across grants, loans, advice, regulatory guidance, export support, and procurement opportunities.

---

## Executive Summary

### Business Context

The UK has 5.5 million SMEs, contributing 52% of private sector turnover and employing 16.7 million people. Government support for these businesses is scattered across GOV.UK, British Business Bank, Growth Hubs, LEP websites, Innovate UK, and departmental microsites. An FSB survey found that 60% of eligible businesses are unaware of support they could access. The portal will aggregate and personalise access to government business support, making it as easy to find a grant as it is to file a tax return.

### Objectives

- Increase SME awareness of government support from 40% to 75% within 18 months
- Reduce time from first visit to grant/loan application from 3 hours to 30 minutes
- Aggregate 200+ support schemes from 10+ departments with structured metadata
- Deliver personalised recommendations based on business type, sector, size, and location
- Integrate with GOV.UK One Login and Companies House for pre-populated business context

### Expected Outcomes

- GBP 2B additional government support accessed by SMEs annually (currently estimated GBP 3B under-claimed)
- 500,000 monthly portal visitors within 12 months
- Measurable increase in SME productivity through better access to innovation grants, export support, and training

### Project Scope

**In Scope**:
- Personalised business support finder with eligibility checking
- Grant and loan scheme directory with structured metadata from all departments
- Guided application journeys with pre-populated forms
- Integration with GOV.UK One Login and Companies House
- Regulatory guidance finder personalised by sector
- Export readiness assessment and market opportunity finder
- Procurement opportunity alerts from Contracts Finder

**Out of Scope**:
- Grant/loan assessment and approval (remains with issuing department/BBB)
- Tax calculations or filing (HMRC remit)
- Company registration (Companies House remit)
- Business banking or financial advisory services

---

## Business Requirements

### BR-001: Personalised Support Discovery

**Description**: The platform must determine the most relevant government support schemes for each business based on their sector (SIC code), size (employees, turnover), location, business age, and stated needs, presenting a personalised dashboard on first login.

**Rationale**: SMEs do not have time to browse 200+ schemes. Personalisation ensures they see what matters. A fish and chip shop in Grimsby needs different support than a biotech startup in Cambridge.

**Success Criteria**:
- 80% of personalised recommendations rated as relevant by users
- Average time to find relevant support < 5 minutes from first visit
- 75% of eligible SMEs aware of at least one relevant scheme within 18 months

**Priority**: MUST_HAVE

---

### BR-002: Cross-Government Scheme Aggregation

**Description**: The platform must aggregate support schemes from at least 10 government departments and public bodies, with structured metadata enabling search, filter, and eligibility matching.

**Rationale**: Support is currently scattered. DBT has export grants, DSIT has innovation funding, HMRC has R&D tax credits, BBB has loans, Defra has rural grants, DLUHC has local growth funds. No single place aggregates them.

**Success Criteria**:
- 200+ schemes indexed at launch, covering 10+ departments
- Scheme metadata includes: eligibility criteria, funding amount, deadline, sector, region
- Scheme data refreshed within 2 working days of departmental updates

**Priority**: MUST_HAVE

---

### BR-003: Simplified Application Journeys

**Description**: The platform must enable businesses to start grant/loan applications directly from the portal, with forms pre-populated from Companies House data and GOV.UK account, reducing duplication of information already held by government.

**Rationale**: An SME applying for a BBB Start Up Loan re-enters their company name, registration number, address, directors, and accounts — all of which Companies House already holds. Pre-population eliminates this friction.

**Success Criteria**:
- Average application time reduced from 3 hours to 30 minutes
- 70% of form fields pre-populated for businesses with Companies House registration
- Application submission routed to the correct departmental system seamlessly

**Priority**: SHOULD_HAVE

---

### BR-004: Regulatory Guidance Finder

**Description**: The platform must provide personalised regulatory guidance based on business sector, helping businesses understand their obligations (employment law, health and safety, environmental regulations, food hygiene) in plain English.

**Rationale**: SMEs spend an average of 15 hours per month on compliance. Much of this time is spent finding the right guidance. Sector-personalised guidance reduces this burden.

**Success Criteria**:
- Regulatory guidance available for top 20 SIC code sectors
- Content in plain English at reading age 13-15
- Links to authoritative departmental guidance (no paraphrasing of legal requirements)

**Priority**: SHOULD_HAVE

---

### BR-005: Mobile-First Design

**Description**: All portal functionality must be fully usable on a smartphone browser without app installation, reflecting the reality that many sole traders and micro-business owners primarily use mobile devices.

**Rationale**: 4.1 million sole traders may not have a desk or laptop. The portal must work on the device they have. The GDS design system is mobile-responsive, and the portal must go further with mobile-optimised journeys.

**Success Criteria**:
- All critical journeys completable on mobile browser
- Mobile usability score > 90 (Google Lighthouse)
- No feature requires desktop-only interaction

**Priority**: MUST_HAVE

---

## Functional Requirements

### FR-001: Business Profile Setup

**Description**: Enable businesses to create a profile by authenticating via GOV.UK One Login and importing data from Companies House.

**Acceptance Criteria**:
- [ ] Given a registered business, when they authenticate and enter their company number, then company name, address, SIC code, directors, and incorporation date are pre-populated from Companies House
- [ ] Given a sole trader without Companies House registration, when they create a profile, then they can manually enter business details
- [ ] Given a returning user, when they log in, then their profile is pre-loaded with personalised recommendations updated since last visit

**Priority**: MUST_HAVE

---

### FR-002: Support Scheme Eligibility Engine

**Description**: Match businesses to eligible support schemes based on their profile attributes (sector, size, location, age, needs).

**Acceptance Criteria**:
- [ ] Given a business profile, when the eligibility engine runs, then all matching schemes are returned sorted by relevance
- [ ] Given a scheme with geographic restrictions, when a business outside the area views it, then it is excluded from results
- [ ] Given a scheme with a deadline, when the deadline is within 14 days, then a prominent warning is displayed
- [ ] Given a scheme that has closed, when it appears in results, then it is clearly marked as closed with a reopening date if available

**Priority**: MUST_HAVE

---

### FR-003: Grant Application Pre-Population

**Description**: Pre-populate grant and loan application forms with data from the business profile and Companies House.

**Acceptance Criteria**:
- [ ] Given a business applying for a BBB Start Up Loan, when the application form loads, then company details, director information, and accounts data are pre-populated
- [ ] Given pre-populated data, when the business reviews it, then they can correct any field before submission
- [ ] Given an application submission, when the form is submitted, then it is routed to the correct departmental processing system

**Priority**: SHOULD_HAVE

---

### FR-004: Procurement Opportunity Alerts

**Description**: Notify businesses of relevant public procurement opportunities from Contracts Finder based on their sector and capability profile.

**Acceptance Criteria**:
- [ ] Given a business in the IT services sector, when new Contracts Finder opportunities are published in IT, then the business receives an alert (email and/or dashboard)
- [ ] Given alert preferences, when the business configures them, then they can choose sectors, contract values, and geographic areas

**Priority**: COULD_HAVE

---

### FR-005: Export Readiness Assessment

**Description**: Provide businesses with an interactive export readiness assessment, identifying markets, trade barriers, and available export support.

**Acceptance Criteria**:
- [ ] Given a manufacturing business, when they complete the export readiness tool, then they receive a readiness score and recommended markets
- [ ] Given recommended markets, when the business selects one, then relevant trade agreements, tariff information, and DBT support services are shown

**Priority**: COULD_HAVE

---

## Non-Functional Requirements

### NFR-P-001: Page Load Time

**Requirement**: All pages must load within 2 seconds at p95 on a 4G mobile connection.

**Priority**: MUST_HAVE

---

### NFR-SEC-001: Authentication

**Requirement**: GOV.UK One Login for all business users. OAuth 2.0 for API access by intermediaries (accountants, advisors).

**Priority**: MUST_HAVE

---

### NFR-A-001: Availability

**Requirement**: 99.9% availability for the public portal. Maintenance windows permitted 02:00-06:00 UK time on weekdays only.

**Priority**: MUST_HAVE

---

### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance. Support for Welsh language content where required by Welsh Language Act 1993.

**Priority**: MUST_HAVE

---

### NFR-U-002: GDS Design System Compliance

**Requirement**: All interfaces must use the GOV.UK Design System components and patterns. Content must follow GDS content design principles.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: GOV.UK One Login

**Purpose**: Business user authentication
**Integration Type**: OIDC/SAML federation
**Priority**: MUST_HAVE

---

### INT-002: Companies House API

**Purpose**: Business data pre-population
**Integration Type**: Real-time API
**Data Exchanged**: Company registration data, SIC codes, accounts filing history
**Priority**: MUST_HAVE

---

### INT-003: British Business Bank

**Purpose**: Loan scheme eligibility and application routing
**Integration Type**: API and deep-linking
**Priority**: SHOULD_HAVE

---

### INT-004: Contracts Finder

**Purpose**: Procurement opportunity alerts
**Integration Type**: Daily data feed
**Data Exchanged**: Contract opportunities metadata
**Priority**: COULD_HAVE

---

### INT-005: HMRC (Guidance only)

**Purpose**: Link to authoritative tax guidance (not content duplication)
**Integration Type**: Deep-linking with context passing
**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must build on GOV.UK platform infrastructure (GDS mandate)
**TC-2**: Must use GOV.UK One Login for authentication
**TC-3**: Must not duplicate or paraphrase HMRC tax guidance (HMRC constraint)

### Business Constraints

**BC-1**: Budget capped at GBP 8M over 3 years
**BC-2**: Must obtain GDS service assessment pass at Alpha and Beta
**BC-3**: Cross-departmental scheme data sharing agreements required with each department

### Assumptions

**A-1**: Departments will provide structured scheme metadata via API or feed
**A-2**: GOV.UK One Login will support business accounts (not just individual) by Beta
**A-3**: Companies House API rate limits are sufficient for portal traffic

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-004-STKE-v1.0 | Stakeholder Analysis | SDG 8 Programme | Drivers, goals | `projects/004-small-business-support-portal/ARC-004-STKE-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 1, 5, 10 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Industrial Strategy | Policy | DBT | SME productivity | https://www.gov.uk/government/publications/industrial-strategy |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Small Business Support Portal
**Model**: Claude Opus 4.6
