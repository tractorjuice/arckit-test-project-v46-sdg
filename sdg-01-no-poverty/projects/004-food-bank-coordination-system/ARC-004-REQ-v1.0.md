# Project Requirements: Food Bank Coordination System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Food Bank Coordination System (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Food Insecurity Programme, Cross-Government (DEFRA lead) |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA, DWP, DHSC, Trussell Trust, IFAN, FareShare |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies requirements for a Food Bank Coordination System linking food banks (Trussell Trust network, IFAN members, independents) with referral agencies (Jobcentres, councils, GPs, schools, social workers) and surplus food redistribution organisations (FareShare). The system must serve a sector that is primarily volunteer-run, with limited digital infrastructure, while respecting the independence and dignity principles of food aid providers.

---

## Executive Summary

### Business Context

The UK food bank sector has grown dramatically — the Trussell Trust alone distributed 3 million emergency food parcels in 2024-25, up from 1.6 million five years earlier. The sector is fragmented: 1,400+ Trussell Trust food banks, 1,100+ IFAN independents, plus hundreds of community larders, pantries, and hot meal services. Referrals are primarily paper-based vouchers. Surplus food from retailers and manufacturers is redistributed by FareShare to approximately 8,500 organisations, but matching supply to demand is logistically complex.

There is no national coordination platform. Referral agencies cannot see food bank capacity. Food banks cannot predict demand. Surplus food is wasted when it cannot reach the right location in time. Government has no reliable national data on food insecurity prevalence.

### Objectives

- Enable digital referrals from Jobcentres, councils, GPs, and schools to food banks
- Coordinate surplus food redistribution to match supply with demand
- Provide a food bank location finder with real-time capacity information
- Generate anonymised national food insecurity data for policy analysis
- Respect food bank independence — platform must be opt-in

### Expected Outcomes

- 1 million digital referrals processed per year (replacing paper vouchers)
- 25% increase in surplus food redistribution (reduced waste, improved food bank supply)
- First-ever national quarterly food insecurity report
- 40% reduction in referral-to-food time (currently 2-3 days average, target same-day)
- GBP 12M annual food waste reduction value

### Project Scope

**In Scope**:

- Digital referral/voucher system for food bank referral agencies
- Food bank location finder with capacity/stock indicators
- Surplus food matching and logistics coordination (FareShare integration)
- Anonymised aggregate reporting on referral volumes and patterns
- Food bank stock management (basic — designed for volunteers)
- Referral to wider support services (benefits, debt advice, housing)

**Out of Scope**:

- Food bank operational management (staff rotas, volunteer management)
- Direct food procurement or purchasing
- Meal delivery services
- School meals administration
- Food hygiene and safety compliance (existing regulatory framework)

---

## Business Requirements

### BR-001: Digital Referral System

**Description**: Enable referral agencies to issue digital vouchers/referrals to food banks, replacing paper vouchers. The referral must be usable by the person in need without requiring a smartphone — SMS and printed QR codes must be supported.

**Rationale**: Paper vouchers are lost, expire, and cannot be tracked. Digital referrals improve speed and allow food banks to prepare for visitors (ref: SD-1, SD-2, SD-4).

**Success Criteria**:

- 80% of Jobcentre referrals issued digitally by Year 2
- Referral redeemable via SMS code, QR code, or verbal reference number
- Average referral-to-food time reduced from 2-3 days to same-day

**Priority**: MUST_HAVE

---

### BR-002: Food Bank Capacity and Location Finder

**Description**: Provide a public-facing tool showing food bank locations, opening hours, dietary accommodation, and current capacity indicators, enabling people and referral agents to find the nearest suitable food bank.

**Rationale**: People in crisis need to find help quickly, close to where they are. Current information is scattered across multiple websites and often outdated (ref: SD-4).

**Success Criteria**:

- Coverage of 80% of UK food banks (Trussell Trust, IFAN, and independents)
- Capacity indicators updated at least daily by participating food banks
- Dietary and cultural needs searchable (halal, kosher, vegetarian, allergen-free)

**Priority**: MUST_HAVE

---

### BR-003: Surplus Food Redistribution Coordination

**Description**: Coordinate the matching of surplus food from retailers and manufacturers with food banks that need stock, integrating with FareShare logistics and direct retailer donation programmes.

**Rationale**: Approximately 3.6 million tonnes of food are wasted in the UK supply chain annually. Better coordination between surplus food sources and food banks reduces waste and improves food quality and variety (ref: SD-3).

**Success Criteria**:

- 25% increase in surplus food redistributed through platform coordination
- Real-time matching of surplus food availability to food bank demand
- Perishable food routed to nearest food bank within cold chain requirements

**Priority**: SHOULD_HAVE

---

### BR-004: Anonymised National Reporting

**Description**: Generate aggregate, anonymised national data on food bank referral volumes, reasons for referral, geographic distribution, and seasonal patterns.

**Rationale**: No consistent national food insecurity data exists. Government needs evidence to shape policy. Data must be anonymised and aggregate to protect individual dignity (ref: SD-1).

**Success Criteria**:

- Quarterly national reports published from Year 2
- Data covering 70% of food aid provision
- No individual-level data shared with government without explicit consent
- Independent data governance board established

**Priority**: SHOULD_HAVE

---

### BR-005: Wider Support Referral

**Description**: When a referral is made to a food bank, the system must offer (not mandate) onward referral to relevant support services — UC claim support, debt advice, housing support, mental health services.

**Rationale**: Food insecurity is usually a symptom of wider issues. "Not just food" is a sector principle — connecting people with root-cause support (ref: SD-5).

**Success Criteria**:

- Wider support referral offered at point of food bank referral
- 30% of food bank referrals result in at least one onward referral
- Local authority and charity support services listed per area

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### FR-001: Referral Agency Interface

**Description**: Referral agents (Work Coaches, council officers, GPs, social workers, school pastoral staff) must be able to issue a food bank referral through a simple web interface or API integrated into their existing systems.

**Acceptance Criteria**:

- [ ] Given a referral agent identifies food insecurity, when they create a referral, then a digital voucher is generated with a unique code redeemable at a named food bank
- [ ] Given a referral, when the food bank is selected, then the system defaults to the nearest open food bank with available capacity
- [ ] Edge case: If no food banks in the area have capacity, the system suggests alternatives within 5 miles and alerts the local coordinator

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-002: Voucher Redemption

**Description**: Food bank volunteers must be able to verify and redeem a digital voucher using a simple smartphone app, web interface, or manual code entry.

**Acceptance Criteria**:

- [ ] Given a person presents a digital voucher (SMS code, QR code, or verbal reference), when the volunteer enters/scans the code, then the referral is verified and marked as redeemed
- [ ] Given a voucher has expired (default 7 days), when presented, then the volunteer is alerted but can override with a reason (many food banks do not turn people away regardless of voucher status)
- [ ] Edge case: If the system is offline (common in volunteer-run locations), vouchers can be redeemed offline and synced later

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-003: Food Bank Stock Management (Basic)

**Description**: Food bank managers can record stock levels (high, medium, low, out of stock) for major categories (tinned goods, fresh, frozen, toiletries, baby items, pet food).

**Acceptance Criteria**:

- [ ] Given a food bank manager, when they update stock levels, then the food bank's capacity indicator is updated on the location finder
- [ ] Given low stock in a category, when the threshold is reached, then the system alerts the local surplus food coordinator (FareShare regional hub)
- [ ] Edge case: Stock management must work on a basic smartphone or tablet — no specialist hardware required

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

### FR-004: Surplus Food Matching

**Description**: When retailers or manufacturers have surplus food available, the system matches it with food banks that need stock in that category, within logistics constraints (distance, cold chain, expiry).

**Acceptance Criteria**:

- [ ] Given a retailer submits a surplus food alert, when matching food banks are identified, then the nearest food bank with matching need is notified within 1 hour
- [ ] Given perishable food with a 48-hour shelf life, when the system matches, then only food banks within the logistics delivery radius are considered
- [ ] Edge case: If no food bank can accept the surplus within the expiry window, the system escalates to FareShare regional hub for alternative community organisations

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

### FR-005: Anonymised Reporting Dashboard

**Description**: National and regional dashboard showing aggregate referral volumes, referral reasons, seasonal patterns, and geographic hotspots.

**Acceptance Criteria**:

- [ ] Given sufficient data (minimum 50 referrals per area per period), when a report is generated, then data is aggregated to prevent individual identification
- [ ] Given a geographic area with fewer than 50 referrals, when the report is generated, then the area is grouped with adjacent areas to prevent re-identification

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-001: Simplicity and Low Technical Requirements

**Requirement**: The platform must be usable by volunteers with no technical training, on basic smartphones or tablets. No specialist hardware required. Offline capability for voucher redemption.

**Priority**: CRITICAL

---

### NFR-A-001: Availability

**Requirement**: 99.5% availability for referral and voucher systems. Lower availability acceptable for reporting and analytics (99%). Planned maintenance outside food bank opening hours (typically Monday-Friday 09:00-15:00).

**Priority**: HIGH

---

### NFR-SEC-001: Privacy and Dignity

**Requirement**: No individual-level data shared with government without explicit, informed consent. Anonymisation applied to all aggregate reporting. Data minimisation — collect only what is needed for the referral. Data classification OFFICIAL-SENSITIVE for referral data (includes vulnerability indicators).

**Priority**: CRITICAL

---

### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA for all user interfaces. Service usable on low-specification devices. SMS-based voucher pathway for people without smartphones. Multi-language support for top community languages.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-001: DWP Jobcentre Systems

**Purpose**: Enable Work Coaches to issue food bank referrals from within existing DWP agent desktop.

**Integration Type**: API embedded in DWP agent tools.

**Priority**: HIGH

---

### INT-002: FareShare Surplus Food System

**Purpose**: Real-time surplus food availability and demand matching.

**Integration Type**: RESTful API with webhook notifications.

**Priority**: HIGH

---

### INT-003: Retailer Surplus Food Feeds

**Purpose**: Receive surplus food alerts from major retailers (Tesco, Asda, Sainsbury's, Co-op, etc.).

**Integration Type**: API or structured email/file integration (varies by retailer capability).

**Priority**: SHOULD_HAVE

---

### INT-004: Local Authority Case Management

**Purpose**: Enable council officers to issue referrals and receive aggregated local food insecurity data.

**Integration Type**: API and web interface.

**Priority**: SHOULD_HAVE

---

## Constraints and Assumptions

**TC-1**: Platform must work offline for voucher redemption — many food banks have poor connectivity.

**TC-2**: No specialist hardware — volunteers use personal smartphones or donated tablets.

**TC-3**: UK sovereign cloud deployment for all data containing personal information.

**BC-1**: Food bank adoption is voluntary — the platform cannot be mandated.

**BC-2**: Budget envelope of GBP 28M over 5 years.

**BC-3**: Platform must not be perceived as government normalising food banks as part of the welfare system.

**A-1**: Trussell Trust and IFAN will participate if governance is independent and data sharing is consensual.

**A-2**: Major retailers will provide surplus food data feeds if it reduces their food waste reporting burden.

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Digital referrals per year | 0 | 1,000,000 | Year 3 |
| Food banks onboarded | 0 | 2,000 (80% coverage) | Year 3 |
| Referral-to-food time | 2-3 days | Same day | Year 2 |
| Surplus food redistribution increase | 30,000 tonnes/yr | 37,500 tonnes/yr | Year 3 |
| National reporting coverage | 0% | 70% of food aid | Year 2 |

---

## Approval

| Reviewer | Role | Status | Date |
|----------|------|--------|------|
| SRO | Programme Sponsor | [ ] Approved | PENDING |
| Trussell Trust | Key Partner | [ ] Approved | PENDING |
| IFAN | Key Partner | [ ] Approved | PENDING |
| FareShare | Key Partner | [ ] Approved | PENDING |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Food Bank Coordination System
**Model**: Claude Opus 4.6
