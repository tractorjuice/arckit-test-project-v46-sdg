# Project Requirements: Circular Economy Marketplace

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Circular Economy Marketplace (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Circular Economy Marketplace |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, WRAP, Environment Agency, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Circular Economy Marketplace — a DEFRA-owned digital platform connecting waste producers with recyclers, remanufacturers, and reuse organisations, enabling materials to be diverted from landfill to higher waste hierarchy outcomes.

---

## Executive Summary

### Business Context

The UK sends approximately 40 million tonnes of waste to landfill and energy-from-waste annually, despite significant proportions being suitable for reuse or recycling. No national digital marketplace exists to connect waste producers with organisations that can valorise these materials. Producers default to the cheapest disposal option (often landfill at GBP 103.70/tonne tax plus gate fees) because finding reuse or recycling outlets is fragmented, manual, and time-consuming. The Circular Economy Marketplace will create a national digital exchange where materials are matched with the highest possible waste hierarchy outcome, driving the UK towards its Resources and Waste Strategy goal of eliminating avoidable waste by 2050.

### Objectives

- Create a national marketplace connecting waste producers with verified recyclers, remanufacturers, and reuse organisations
- Implement material matching algorithms that prioritise the waste hierarchy (prevention > reuse > recycling > recovery > disposal)
- Integrate with Environment Agency operator verification for regulatory compliance
- Generate digital waste transfer notes meeting duty of care requirements
- Enable geographic matching to ensure economically viable transport distances

### Expected Outcomes

- 50,000 tonnes of materials diverted from landfill to higher hierarchy outcomes annually within 24 months
- 1,000 verified active participants within 12 months
- GBP 5M annual cost savings for local authorities through reduced landfill gate fees
- 15% of diverted materials going to reuse/repair pathways

### Project Scope

**In Scope**:

- Material listing, search, and matching platform
- Waste hierarchy-prioritised matching algorithms
- Operator verification (EA permits, waste carrier licences)
- Digital waste transfer note generation
- EWC code classification with circular economy extensions
- Geographic proximity matching
- Material quality assessment and grading
- Transaction tracking and audit trail

**Out of Scope**:

- Financial transactions (marketplace connects parties; commercial terms agreed bilaterally)
- Physical logistics and transport arrangement
- Hazardous waste specialist handling (signposted to licensed specialist operators)
- International waste shipment
- Carbon footprint calculation for materials (integration with Project 001 in future phase)

---

## Business Requirements

### BR-1: Waste Hierarchy-Driven Material Matching

**Description**: The marketplace must match materials to receivers in waste hierarchy order, presenting reuse and remanufacturing options before recycling, and recycling before energy recovery or disposal.

**Rationale**: The Environment Act 2021 and Resources and Waste Strategy mandate the waste hierarchy. The marketplace must embed this hierarchy in its algorithms, not merely display options.

**Success Criteria**:

- Material matching results ranked by waste hierarchy position
- 15% of matched materials directed to reuse/repair pathways
- Analytics tracking waste hierarchy distribution of all marketplace transactions

**Priority**: MUST_HAVE

---

### BR-2: Regulatory Compliance for All Transactions

**Description**: Every marketplace transaction must involve verified permitted operators with valid waste carrier licences, generating compliant digital waste transfer notes.

**Rationale**: The Environment Agency requires duty of care compliance for all waste transfers. The marketplace must not facilitate illegal waste activity.

**Success Criteria**:

- 100% of operators verified against EA permit and licence databases
- Digital waste transfer notes generated for every completed transfer
- Audit trail accessible to Environment Agency within 24 hours of request

**Priority**: MUST_HAVE

---

### BR-3: Marketplace Critical Mass

**Description**: The marketplace must achieve sufficient participation on both supply and demand sides to create a viable exchange within 12 months.

**Rationale**: A marketplace with only suppliers or only receivers has no value. Critical mass on both sides is essential for the platform to function.

**Success Criteria**:

- 1,000 verified active participants within 12 months
- At least 500 material listings per month
- At least 200 successful matches per month

**Priority**: MUST_HAVE

---

## Functional Requirements

### FR-1: Material Listing and Classification

**Description**: The system must enable waste producers to list available materials using EWC (European Waste Catalogue) codes with extensions for circular economy readiness (condition, quality, quantity, availability window, location).

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a waste producer lists a material, when they select an EWC code, then the system provides a guided classification with plain language descriptions alongside technical codes
- [ ] Given a material is listed, when circular economy attributes are entered, then the system captures condition (new/used/damaged), quality grade, quantity (tonnes/units), availability window (date range), and location (postcode)
- [ ] Given a material listing is submitted, when matching runs, then the material is automatically matched against registered receiver requirements
- [ ] Bulk listing supported via CSV upload for organisations listing multiple materials

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-2: Waste Hierarchy Material Matching Algorithm

**Description**: The system must match listed materials to registered receivers prioritised by waste hierarchy position, with geographic proximity as a secondary ranking factor.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a material is listed, when matching runs, then results are ordered: (1) reuse/repair organisations, (2) remanufacturers, (3) recyclers, (4) energy recovery operators
- [ ] Given multiple receivers at the same hierarchy level, when ranking runs, then geographic proximity determines order (nearest first)
- [ ] Given a material has no reuse/repair match, when the producer views results, then the system explains why no higher-hierarchy match was available and presents the next best option
- [ ] Matching algorithm weights configurable by DEFRA policy team (e.g., hierarchy weight vs distance weight)

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-3: Operator Verification

**Description**: The system must verify all marketplace participants against Environment Agency permit databases and waste carrier licence registers before enabling them to transact.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an operator registers, when verification runs, then the system checks EA waste permit database and waste carrier licence register via API
- [ ] Given an operator's permit has expired, when they attempt to list or receive materials, then the system blocks the transaction and notifies the operator
- [ ] Permit status re-verified weekly; operators with revoked or expired permits automatically suspended
- [ ] Verification results auditable and accessible to Environment Agency

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-4: Digital Waste Transfer Note Generation

**Description**: The system must generate digital waste transfer notes (WTNs) meeting duty of care requirements for every completed material transfer on the marketplace.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a material transfer is agreed, when both parties confirm, then the system generates a digital WTN containing: description of waste (EWC code), quantity, date of transfer, transferor details, transferee details, permit/licence numbers, and special handling instructions
- [ ] Digital WTN meets Environmental Protection (Duty of Care) Regulations 1991 requirements
- [ ] WTNs retained for minimum 3 years (duty of care retention requirement) and 7 years for enhanced compliance
- [ ] WTNs exportable as PDF and accessible via API for Waste Management Analytics (Project 003) integration

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-5: Geographic Proximity Search

**Description**: The system must enable material search and matching based on geographic proximity, using postcode-based distance calculation to ensure economically viable transport distances.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a receiver searches for materials, when they specify a postcode and radius, then results show materials within the specified distance ordered by hierarchy then proximity
- [ ] Default search radius: 50 miles (configurable by user)
- [ ] Distance calculated as road distance (not straight line) where mapping data available, falling back to straight line distance
- [ ] Transport carbon cost estimate displayed alongside distance (tCO2e for a standard 18-tonne vehicle)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-6: Material Quality Assessment and Grading

**Description**: The system must support standardised material quality grading aligned with WRAP quality protocols, enabling receivers to assess material suitability before committing to a transfer.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a producer lists a material, when they grade quality, then the system presents WRAP-aligned quality criteria specific to the material type
- [ ] Photo upload supported (minimum 2, maximum 10 photos per listing) for visual quality assessment
- [ ] Quality grades: A (reuse-ready), B (minor repair needed), C (recycling-grade), D (recovery only)
- [ ] Receiver can filter search results by minimum quality grade

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

### FR-7: Marketplace Analytics Dashboard

**Description**: The system must provide analytics dashboards showing marketplace performance, waste hierarchy distribution, and circular economy metrics for DEFRA policy reporting.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Dashboard shows: total tonnes listed, matched, transferred; waste hierarchy distribution; geographic heat map; material category breakdown
- [ ] Time series trends showing monthly/quarterly/annual progression
- [ ] Data exportable in CSV and JSON formats for integration with Waste Management Analytics (Project 003)
- [ ] Policy team can generate reports for ministerial briefings and parliamentary questions

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Search Response Time

**Requirement**: Material search results returned within 2 seconds for geographic searches within 100-mile radius. Matching algorithm notifications sent within 5 minutes of new listing.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability (8.7 hours maximum downtime per year). Marketplace must be available during business hours (06:00-22:00 UK time) when waste transfers are operationally active.

**Priority**: CRITICAL

---

### NFR-SEC-1: Operator Data Protection

**Requirement**: Operator permit and licence data accessed via EA APIs only, not stored locally. Marketplace transaction data classified as OFFICIAL. Operator commercial data (volumes, material types) protected from competitors.

**Priority**: CRITICAL

---

### NFR-U-1: Field Usability

**Requirement**: Material listing interface usable on mobile devices in outdoor conditions (construction sites, waste transfer stations). Offline listing capability with sync when connectivity returns.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Environment Agency Permits and Licences API

**Purpose**: Verify operator credentials in real-time.

**Data Exchanged**: Permit status, waste carrier licence validity, permitted waste types, site locations.

**Priority**: CRITICAL

---

### INT-2: Waste Management Analytics (Project 003) Integration

**Purpose**: Share material transfer data for national waste tracking and reporting.

**Data Exchanged**: Digital waste transfer notes, material volumes, hierarchy outcomes, geographic data.

**Integration Type**: Event-driven (material transfer events published to shared event bus).

**Priority**: MUST_HAVE

---

### INT-3: Carbon Footprint Calculator (Project 001) — Future Phase

**Purpose**: Calculate avoided emissions from material reuse and recycling versus landfill disposal.

**Priority**: COULD_HAVE (Phase 2)

---

## Dependencies and Risks

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Marketplace chicken-and-egg: insufficient participants on either side | HIGH | HIGH | Seed with WRAP networks, local authority partnerships, incentivise early adopters | Service Owner |
| R-2 | Waste management companies boycott or resist platform | MEDIUM | HIGH | Position as additional channel, enable waste companies as participants, industry consultation | SRO |
| R-3 | EA API integration delayed or unreliable | MEDIUM | HIGH | Manual verification fallback, dedicated EA liaison, staged integration | Technical Lead |
| R-4 | Material quality disputes between trading parties | HIGH | MEDIUM | Standardised quality grading, photo evidence, dispute resolution process | Product Manager |
| R-5 | Geographic matching finds no viable receivers within economic transport distance | MEDIUM | MEDIUM | Expand default radius, aggregate small volumes, transport partnership | Product Manager |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Resources and Waste Strategy 2018 | Policy | GOV.UK | Waste hierarchy, circular economy targets | N/A |
| Environment Act 2021 | Legislation | legislation.gov.uk | EPR, waste tracking, enforcement | N/A |
| WRAP Quality Protocols | Standard | wrap.org.uk | Material quality assessment | N/A |
| Environmental Protection (Duty of Care) Regulations 1991 | Legislation | legislation.gov.uk | Waste transfer note requirements | N/A |
| ARC-002-STKE-v1.0 | Stakeholder Analysis | SDG 12 Programme | Stakeholder drivers and goals | `projects/002-circular-economy-marketplace/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Circular Economy Marketplace (Project 002)
**Model**: Claude Opus 4.6
