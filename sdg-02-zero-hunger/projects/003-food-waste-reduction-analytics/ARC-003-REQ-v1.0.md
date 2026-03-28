# Project Requirements: Food Waste Reduction Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Food Waste Reduction Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DEFRA Resources and Waste Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, WRAP, Environment Agency, Food and Drink Federation |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Food Waste Reduction Analytics platform, covering waste data collection, analysis, benchmarking, and reporting across the UK food supply chain. Traceable to ARC-003-STKE-v1.0 and aligned with ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

The UK generates approximately 9.5 million tonnes of food waste annually, valued at approximately £19 billion. The government has committed to halving per capita food waste by 2030 under SDG 12.3 and the Resources and Waste Strategy 2018. WRAP manages the Courtauld Commitment 2030 with approximately 200 food industry signatories, but current waste measurement relies on annual manual spreadsheet submissions with 12-18 month reporting lag and significant methodological uncertainty (+/-25%).

The food waste hierarchy (prevention, redistribution, animal feed, anaerobic digestion, composting, landfill) requires granular data to identify hotspots and track waste diversion. Without improved data infrastructure, the UK cannot credibly report SDG 12.3 progress or target interventions effectively.

### Objectives

- Establish a statistically robust national food waste baseline across all supply chain stages
- Automate waste data collection from Courtauld signatories and other industry participants
- Provide anonymised benchmarking enabling companies to compare waste performance
- Track progress against the 2030 halving target with < 6-month reporting lag
- Publish food waste metrics to the National Food Strategy Dashboard (Project 005)

### Expected Outcomes

- National food waste measurement confidence improved from +/-25% to +/-10%
- Reporting lag reduced from 18 months to < 6 months
- 200+ companies actively reporting waste data through the platform
- Identified waste reduction opportunities worth £500M/year across the supply chain
- UK able to credibly report SDG 12.3 progress at international reviews

### Project Scope

**In Scope**:

- Waste data collection portal for industry participants
- Automated data ingestion from waste management operators and local authorities
- Waste composition analysis and food waste hierarchy tracking
- Anonymised benchmarking tools for industry participants
- National food waste dashboard and trend reporting
- API for National Food Strategy Dashboard (Project 005)
- Integration with WRAP Food Waste Atlas

**Out of Scope**:

- Non-food waste streams (handled by separate DEFRA programmes)
- Consumer-facing food waste reduction campaigns (WRAP operational responsibility)
- International food loss tracking (pre-farm-gate, handled by FAO)
- Waste collection logistics optimisation

---

## Business Requirements

### BR-001: National Food Waste Measurement

**Description**: The platform must enable accurate measurement of food waste volumes across all supply chain stages with statistical confidence sufficient for international reporting.

**Rationale**: Current WRAP estimates have +/-25% uncertainty, insufficient for credible SDG 12.3 reporting.

**Success Criteria**:

- Measurement covering farm gate, manufacturing, retail, hospitality, and household waste
- Statistical confidence < +/-10% at national level
- Year-on-year comparability maintained through consistent methodology

**Priority**: MUST_HAVE

---

### BR-002: Automated Industry Data Collection

**Description**: The platform must automate food waste data collection from Courtauld Commitment signatories and other voluntary participants, replacing manual spreadsheet submissions.

**Rationale**: Current annual manual reporting creates 12-18 month lag, limiting the value of waste data for targeted intervention.

**Success Criteria**:

- Quarterly automated data collection from 80% of Courtauld signatories
- Data submission time per company reduced from 40 hours/year to < 4 hours/year
- Reporting lag reduced from 18 months to < 6 months

**Priority**: MUST_HAVE

---

### BR-003: Industry Benchmarking

**Description**: The platform must provide anonymised waste benchmarking, enabling companies to compare their waste intensity against sector averages and quartiles.

**Rationale**: Industry will participate in data sharing only if they receive actionable insights in return. Benchmarking is the primary incentive for voluntary participation.

**Success Criteria**:

- Sector-level benchmarks published for at least 10 food sub-sectors
- Individual company performance shown relative to sector quartiles
- Company-level data never disclosed to other participants or published

**Priority**: MUST_HAVE

---

### BR-004: Waste Hierarchy Tracking

**Description**: The platform must track food waste by disposal route (prevention, redistribution, animal feed, anaerobic digestion, composting, incineration, landfill) to measure progress on waste hierarchy compliance.

**Rationale**: The Resources and Waste Strategy requires waste to be managed according to the waste hierarchy. Measuring only total waste volume misses the critical question of how waste is managed.

**Success Criteria**:

- Waste data categorised by all seven hierarchy levels
- Trend analysis showing shift up the waste hierarchy over time
- Hotspot identification: sectors and regions with disproportionate landfill use

**Priority**: SHOULD_HAVE

---

## Functional Requirements

### FR-001: Industry Data Submission Portal

**Description**: The system must provide a web-based portal for industry participants to submit food waste data, with configurable reporting templates by sector.

**Acceptance Criteria**:

- [ ] Given a Courtauld signatory, when logging in, then a pre-populated submission form is presented for their sector
- [ ] Given waste data entry, when submitted, then automated validation checks are applied (range, completeness, consistency)
- [ ] Given a completed submission, when confirmed, then acknowledgement is sent and data enters processing pipeline
- [ ] Given bulk data, when uploaded via CSV/API, then data is validated and ingested without manual intervention

**Priority**: MUST_HAVE

---

### FR-002: Waste Data Ingestion from Local Authorities

**Description**: The system must ingest household food waste data from local authority waste collection records, standardising diverse reporting formats.

**Acceptance Criteria**:

- [ ] Given local authority waste returns, when submitted in their existing format, then data is normalised to the platform standard
- [ ] Given household waste composition analysis data, when available, then food waste proportion is extracted and stored
- [ ] Given 152+ reporting authorities, when ingesting data, then processing completes within 48 hours per quarterly cycle

**Priority**: MUST_HAVE

---

### FR-003: Benchmarking Dashboard

**Description**: The system must provide anonymised benchmarking dashboards showing individual company performance against sector quartiles.

**Acceptance Criteria**:

- [ ] Given an authenticated industry user, when accessing benchmarking, then their company's waste intensity is shown against sector quartile distribution
- [ ] Given sector data, when fewer than 5 companies in a sub-sector, then benchmarking is suppressed to prevent identification
- [ ] Given benchmarking data, when downloaded, then only the user's own data and anonymised sector data is included

**Priority**: MUST_HAVE

---

### FR-004: National Waste Dashboard

**Description**: The system must provide DEFRA policy users with a national-level dashboard showing food waste trends, hotspots, and progress against 2030 targets.

**Acceptance Criteria**:

- [ ] Given a policy user, when accessing the national dashboard, then total food waste is shown by supply chain stage with year-on-year trends
- [ ] Given the SDG 12.3 baseline, when compared to current data, then progress percentage is calculated and displayed
- [ ] Given geographic data, when mapped, then regional waste hotspots are visible

**Priority**: MUST_HAVE

---

### FR-005: Waste Composition Analysis

**Description**: The system must capture food waste composition data (food type, avoidable/unavoidable, packaging) to enable targeted waste reduction interventions.

**Priority**: SHOULD_HAVE

---

### FR-006: API for National Food Strategy Dashboard

**Description**: The system must publish food waste metrics via API for Project 005.

**Acceptance Criteria**:

- [ ] Given an authorised API consumer, when requesting waste metrics, then quarterly aggregated data is returned
- [ ] Given API versioning, when new version is released, then previous version available for 6 months

**Priority**: SHOULD_HAVE

---

## Non-Functional Requirements

### NFR-P-1: Performance

- Portal page load: < 3 seconds (p95)
- Data processing pipeline: quarterly batch completed within 72 hours
- Benchmarking calculations: updated within 24 hours of new data

**Priority**: MEDIUM

---

### NFR-A-1: Availability

**Requirement**: 99.0% uptime (analytical platform tier per ARC-000-PRIN-v1.0 Principle 16).

**RTO**: 8 hours | **RPO**: 4 hours

**Priority**: MEDIUM

---

### NFR-SEC-1: Data Confidentiality

**Requirement**: Company-level waste data must be protected from disclosure. Data sharing agreement must include FOI exemption provisions (s.41 FOIA 2000 -- information provided in confidence, s.43 -- commercial interests).

**Specific Controls**:

- Company-level data accessible only to the submitting company and authorised DEFRA/WRAP analysts
- Benchmarking outputs use k-anonymity (minimum 5 companies per benchmark group)
- API outputs for Project 005 aggregated to sector/national level only
- Audit trail for all data access

**Priority**: CRITICAL

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance. Portal must be usable by sustainability officers with varied technical proficiency.

**Priority**: HIGH

---

## Integration Requirements

### INT-001: WRAP Food Waste Atlas

**Purpose**: Bidirectional data exchange with WRAP's existing waste data repository.

**Data Exchanged**: Waste survey data, composition analysis, signatory reporting data

**Priority**: MUST_HAVE

---

### INT-002: Environment Agency Waste Returns

**Purpose**: Ingest regulated waste data from environmental permit returns (manufacturing, processing sites).

**Data Exchanged**: Waste volumes by type and disposal route from permitted sites

**Integration Pattern**: Annual batch file exchange

**Priority**: SHOULD_HAVE

---

### INT-003: Local Authority Waste Data (WasteDataFlow)

**Purpose**: Ingest household waste collection data from the WasteDataFlow national reporting system.

**Data Exchanged**: Quarterly household waste tonnage by waste stream and collection method

**Priority**: MUST_HAVE

---

## Data Requirements

### Key Data Entities

#### Entity 1: Waste Report

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| report_id | UUID | Yes | Unique identifier |
| reporter_id | UUID | Yes | Reporting organisation |
| reporting_period | DateRange | Yes | Quarter/year covered |
| supply_chain_stage | Enum | Yes | Farm/manufacturing/retail/hospitality/household |
| total_food_waste_tonnes | Decimal | Yes | Total food waste weight |
| disposal_route_breakdown | JSON | Yes | Breakdown by waste hierarchy level |
| measurement_method | Enum | Yes | Direct measurement/estimate/modelled |
| confidence_level | Enum | Yes | High/medium/low |

**Data Volume**: 50,000 reports/year at full scale

**Data Classification**: OFFICIAL-SENSITIVE (commercially sensitive)

---

## Constraints and Assumptions

**TC-1**: Must deploy to DEFRA cloud environment.

**TC-2**: Must integrate with WRAP's existing infrastructure (legacy systems).

**BC-1**: Budget capped at £6.5M over 3 years.

**BC-2**: Voluntary industry participation model (no regulatory mandate for data submission).

**A-1**: Courtauld signatories will adopt automated reporting if it reduces their reporting burden (risk: if not, manual collection continues).

**A-2**: Local authority waste composition data is available at sufficient granularity to estimate household food waste (risk: many authorities do not conduct composition analysis).

---

## Budget

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Platform development | £2.8M | Portal, ingestion, analytics |
| WRAP integration | £0.8M | Atlas integration, data migration |
| Data acquisition | £0.5M | LA data standardisation, composition studies |
| Infrastructure (3 years) | £1.2M | Cloud hosting, data storage |
| Security and compliance | £0.4M | Pen testing, data sharing agreements |
| Contingency (15%) | £0.8M | Risk buffer |
| **Total** | **£6.5M** | Over 3 years |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| WRAP | Waste and Resources Action Programme |
| Courtauld Commitment | Voluntary industry agreement to reduce food and drink waste |
| SDG 12.3 | UN target: halve per capita food waste by 2030 |
| WasteDataFlow | National database for municipal waste reporting |
| Waste Hierarchy | Prevention > Redistribution > Animal Feed > AD > Composting > Incineration > Landfill |
| k-anonymity | Statistical disclosure control: minimum k individuals per group |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Architecture Principles
- ARC-003-STKE-v1.0 -- Food Waste Reduction Analytics Stakeholder Analysis
- Resources and Waste Strategy 2018
- Courtauld Commitment 2030 (WRAP)
- SDG 12.3 Champions Lead Coalition methodology

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Food Waste Reduction Analytics
**Model**: Claude Opus 4.6
