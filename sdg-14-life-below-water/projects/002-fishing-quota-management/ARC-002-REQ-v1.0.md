# Project Requirements: Fishing Quota Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Fishing Quota Management (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Owner, Fishing Quota Management |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Quota Programme Board, MMO, DEFRA Marine, Cefas, NFFO, NUTFA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document specifies the business, functional, non-functional, integration, and data requirements for the Fishing Quota Management system. It provides the authoritative baseline for a digital platform supporting electronic catch reporting, real-time quota monitoring, and quota allocation management under the Fisheries Act 2020.

---

## Executive Summary

### Business Context

The United Kingdom's departure from the EU Common Fisheries Policy has transferred full responsibility for fishing quota management to UK administrations. The Marine Management Organisation manages approximately 100 quota stocks for England, allocating Total Allowable Catch (TAC) through Fixed Quota Allocations to Producer Organisations and a pool allocation for the under-10m fleet. Current catch reporting relies on a mix of electronic logbooks (eLogbooks) for the over-10m fleet and paper-based catch returns for the under-10m fleet, creating data latency of 4-6 weeks for small vessels.

The Fisheries Act 2020 establishes eight fisheries objectives — including sustainability, scientific evidence, and national benefit — requiring a more sophisticated, data-driven approach to quota management. Fisheries Management Plans (FMPs) mandate species-specific management measures that require accurate, timely catch data to implement and monitor.

### Objectives

- Replace paper-based catch reporting with digital catch recording for all fleet segments, including a simple mobile app for the under-10m fleet
- Provide real-time quota utilisation monitoring with automated threshold alerts to prevent quota overshoots
- Integrate ICES stock assessment data to link quota allocation decisions to scientific evidence
- Support Producer Organisation quota pool management and digital quota trading
- Enable Fisheries Management Plan monitoring with species-specific catch tracking

### Expected Outcomes

- Under-10m electronic catch reporting adoption at 80% within 18 months
- Catch data latency reduced from 4-6 weeks to <48 hours for all fleet segments
- Quota utilisation accuracy improved from +-15% to +-3%
- Quota trading processing time reduced from 5 days to same-day
- Paper catch returns reduced by 90%

### Project Scope

**In Scope**:

- Electronic catch reporting (eLogbook) for all vessel sizes including under-10m mobile app
- Real-time quota utilisation monitoring and dashboard
- Quota allocation management (FQA, pool, in-year allocation)
- Producer Organisation quota pool management portal
- Quota trading and swap processing
- ICES stock assessment data integration
- Fisheries Management Plan catch monitoring
- VMS/AIS catch validation (cross-referencing catch area with vessel position)
- Buyer and seller registration and first-sale note processing

**Out of Scope**:

- Vessel licensing (existing MMO system)
- Marine Protected Areas monitoring (Project 001)
- Marine pollution tracking (Project 003)
- Aquaculture quota and licensing
- Recreational fishing catch reporting
- Fish health and disease monitoring

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| MMO SRO | Executive Sponsor | MMO | Decision maker |
| MMO Head of Quota | Operations lead | MMO | Requirements authority |
| Cefas Stock Team | Scientific adviser | Cefas | Scientific data integration |
| NFFO Representative | Large-scale fleet voice | NFFO | Industry requirements |
| NUTFA Representative | Small-scale fleet voice | NUTFA | Under-10m requirements |
| PO Manager (representative) | Quota pool management | PO | Quota trading requirements |
| MMO Enterprise Architect | Architecture oversight | MMO | Technical oversight |
| IFCA Representative | Inshore fisheries | IFCA | Inshore catch data |

---

## Business Requirements

### BR-1: Digital Catch Reporting for All Fleet Segments

**Description**: The system must enable all UK fishing vessels to submit catch reports electronically, replacing paper-based catch returns with a digital process that works for both large commercial trawlers and small inshore boats.

**Rationale**: Paper-based catch returns from the under-10m fleet create a 4-6 week data lag, making real-time quota management impossible and leading to precautionary early quota closures or risk of overshoot.

**Success Criteria**:

- 80% of under-10m fleet submitting electronically within 18 months
- Average catch report submission time <5 minutes
- Paper catch returns reduced by 90%

**Priority**: MUST_HAVE

**Stakeholder**: MMO Head of Quota, NUTFA, NFFO

---

### BR-2: Real-Time Quota Utilisation Monitoring

**Description**: The system must provide real-time visibility of quota utilisation for all managed stocks, with automated alerts at configurable thresholds (70%, 85%, 95%) and projected quota exhaustion dates.

**Rationale**: Current quota monitoring has significant latency for under-10m catches. This leads to either precautionary early closures (damaging to industry) or late closures (risking overshoot and ICES non-compliance).

**Success Criteria**:

- Quota utilisation accuracy within +-3%
- Automated alerts generated within 1 hour of threshold breach
- Projected exhaustion date calculated daily for all stocks above 50% utilisation

**Priority**: MUST_HAVE

**Stakeholder**: MMO Head of Quota, Fisheries Minister

---

### BR-3: Science-Based Quota Allocation

**Description**: The system must integrate ICES stock assessment data and Cefas scientific surveys, providing an auditable link between scientific advice and quota allocation decisions as required by the Fisheries Act 2020.

**Rationale**: The Fisheries Act 2020 establishes a "scientific evidence" objective. Quota decisions must be demonstrably linked to the best available science.

**Success Criteria**:

- 95% of quota stocks with linked ICES/Cefas scientific advice data
- All quota decisions with documented scientific rationale
- Decision audit trail meeting NAO examination standards

**Priority**: MUST_HAVE

**Stakeholder**: Cefas Stock Team, DEFRA Marine Policy

---

### BR-4: Digital Quota Trading

**Description**: The system must enable Producer Organisations to trade, swap, and transfer quota allocations digitally, with same-day processing and transparent pricing.

**Rationale**: Current quota trading is a manual, paper-based process taking up to 5 working days. This prevents optimal quota utilisation, as POs cannot react quickly to in-season changes in fishing patterns.

**Success Criteria**:

- Quota trade processing time reduced from 5 days to same-day
- All PO-to-PO quota trades recorded with price transparency
- Year-end reconciliation automated

**Priority**: SHOULD_HAVE

**Stakeholder**: NFFO, Producer Organisations

---

### BR-5: Fisheries Management Plan Monitoring

**Description**: The system must support monitoring of catch data against Fisheries Management Plan targets for each species, including bycatch tracking and discard monitoring.

**Rationale**: FMPs are statutory requirements under the Fisheries Act 2020. Each plan sets species-specific management measures that require continuous monitoring.

**Success Criteria**:

- All published FMPs with monitoring dashboards in the system
- Bycatch and discard data captured alongside target species
- FMP progress reports generated automatically quarterly

**Priority**: SHOULD_HAVE

**Stakeholder**: DEFRA Marine Policy, Cefas

---

## Functional Requirements

### User Personas

#### Persona 1: Vessel Skipper (Over-10m)

- **Role**: Skipper of a commercial fishing vessel >10m, already using eLogbook
- **Goals**: Submit catch reports quickly at sea, view remaining quota for target species, plan fishing trips based on quota availability
- **Pain Points**: Slow eLogbook software, species list too long, poor connectivity at sea
- **Technical Proficiency**: Medium

#### Persona 2: Small-Scale Fisher (Under-10m)

- **Role**: Owner-operator of a small inshore fishing vessel <10m, currently submitting paper catch returns
- **Goals**: Submit catch reports quickly in harbour, understand quota pool status, minimal paperwork
- **Pain Points**: Paper forms are slow, no visibility of quota pool utilisation, digital exclusion
- **Technical Proficiency**: Low to Medium

#### Persona 3: Producer Organisation Manager

- **Role**: Administrative manager of a PO managing quota on behalf of member vessels
- **Goals**: Monitor member catches against PO allocations, trade quota with other POs, generate regulatory reports
- **Pain Points**: Spreadsheet-based quota tracking, manual reconciliation, slow trade processing
- **Technical Proficiency**: Medium

#### Persona 4: MMO Quota Manager

- **Role**: MMO official responsible for national quota allocation and monitoring
- **Goals**: Monitor all quota stocks in real-time, approve in-year allocations, generate ICES/DEFRA reports
- **Pain Points**: Data latency, manual report preparation, reconciliation errors
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: Electronic Catch Reporting (eLogbook)

**Description**: The system must provide electronic catch reporting for all vessel sizes, with species, weight, ICES area, gear type, and effort data captured per fishing trip.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a skipper completing a fishing trip, when they submit a catch report, then species weight, ICES area, gear type, and landing port are recorded
- [ ] Given an under-10m vessel, when the skipper opens the mobile app in harbour, then a simplified catch entry form is presented with recent species pre-populated
- [ ] Given limited connectivity, when a catch report is saved offline, then it queues for automatic submission when connectivity returns
- [ ] Edge case: When a catch includes a quota species at <50kg, then the system allows quick-entry without full trip detail

**Data Requirements**:

- **Inputs**: Vessel ID, species (FAO code), weight (kg), ICES statistical rectangle, gear type (EU gear code), landing port, date
- **Outputs**: Confirmed catch report with unique reference, quota deduction confirmation
- **Validations**: Species code against FAO species list, ICES area valid, weight positive and within vessel capacity limits

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-2: Real-Time Quota Dashboard

**Description**: The system must display current quota utilisation for all managed stocks, with percentage used, remaining tonnes, trend graph, and projected exhaustion date.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given the quota dashboard is loaded, when a stock is selected, then current utilisation (%), remaining tonnes, monthly trend, and projected exhaustion date are displayed
- [ ] Given quota utilisation exceeds a threshold (70%, 85%, 95%), when the threshold is breached, then automated alerts are sent to MMO quota managers and relevant POs
- [ ] Given a new catch report is processed, when it affects a quota stock, then the dashboard updates within 2 hours

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-3: Quota Allocation Management

**Description**: The system must manage the annual quota allocation process, including FQA calculation, PO allocations, under-10m pool allocation, and in-year adjustments.

**Relates To**: BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given annual TAC is confirmed after fisheries negotiations, when entered into the system, then FQA allocations are calculated for all POs based on track record
- [ ] Given under-10m pool quota, when allocated, then pool utilisation is tracked in real-time with automatic monthly allocation periods
- [ ] Given an in-year allocation adjustment is approved, when processed, then all affected PO balances are updated and notifications sent

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: Digital Quota Trading Platform

**Description**: The system must provide a marketplace for POs to offer, request, and complete quota trades and swaps, with same-day processing.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a PO has surplus quota for a species, when they list it for trade, then other POs can view the offer and submit trade requests
- [ ] Given a quota trade is agreed between two POs, when confirmed by both parties, then quota balances are adjusted within the same business day
- [ ] Given a quota swap (species A for species B), when processed, then both species balances are adjusted simultaneously

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-5: ICES Stock Data Integration

**Description**: The system must ingest ICES stock assessment outputs (MSY reference points, biomass estimates, TAC advice) and link them to quota allocation records.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given ICES publishes new stock advice, when data is ingested, then MSY reference points and TAC advice are displayed alongside current quota for that stock
- [ ] Given a quota allocation decision is made, when recorded, then the system captures the scientific advice considered and any deviation rationale
- [ ] Given a user queries a quota stock, when detailed view is accessed, then scientific advice history and stock trend data are displayed

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-6: VMS/AIS Catch Validation

**Description**: The system must cross-reference catch report fishing area with VMS/AIS vessel position data to validate that the declared catch area matches the vessel's actual location.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a catch report declaring fishing in ICES area VIIe, when VMS data shows the vessel was in VIIf, then a validation warning is generated for MMO review
- [ ] Given VMS data confirms the declared area, when processed, then the catch report is auto-validated

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

**Dependencies**: FR-1 (catch reporting), MMO VMS data feed

---

#### FR-7: Mobile Catch Reporting App (Under-10m)

**Description**: The system must provide a native mobile app optimised for the under-10m fleet, with offline capability, simplified species entry, and harbour-friendly design.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a fisher in a harbour with intermittent connectivity, when they open the app, then their most recent vessel profile and common species are pre-loaded
- [ ] Given the fisher submits a catch report, when they tap "Submit", then the report is queued for upload and confirmed when connectivity is available
- [ ] Given the app is used on a small screen (5-inch phone), then all input controls are usable with work-worn hands (large touch targets)
- [ ] Edge case: When the fisher catches multiple species, then a rapid multi-species entry mode allows species and weight to be entered in <30 seconds per species

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-8: Landing Declaration and First Sale Note

**Description**: The system must capture landing declarations and first sale notes digitally, linking catch data through to first sale for full traceability.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given fish is landed and sold, when the buyer submits a first sale note, then catch-to-sale traceability is established
- [ ] Given a landing declaration is submitted, when it differs from the catch report by >10%, then a reconciliation flag is raised

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**:

- Catch report submission: <3 seconds (95th percentile) when online
- Quota dashboard load: <2 seconds (95th percentile)
- Quota trade processing: <30 seconds
- API response time: <500ms (95th percentile)

**Load Conditions**:

- Peak concurrent users: 500 (evening landings period, 16:00-20:00)
- Catch reports: up to 5,000/day during peak fishing season (July-September)
- Quota dashboard views: up to 2,000/day during quota opening periods

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: 99.9% availability. Fishing does not stop for weekends or bank holidays — the system must be available 24/7/365.

**Maintenance Windows**: Rolling deployments with zero-downtime, no scheduled maintenance windows.

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: 15 minutes (catch data is financially significant and cannot be reconstructed)

**RTO**: 1 hour

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: Vessel skippers authenticate via MMO login (username + password + vessel registration number). PO managers and MMO staff via DEFRA Identity with MFA.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Commercial Sensitivity

**Requirement**: Individual vessel catch data is commercially sensitive. Vessel-level data accessible only to the vessel owner, their PO, and MMO. Aggregated data may be published.

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Under-10m Fleet Accessibility

**Requirement**: The mobile app must be usable by fishers with limited digital literacy, in outdoor conditions (bright light, wet hands), on standard smartphones. Interface in English and Welsh.

**Priority**: CRITICAL

---

#### NFR-U-2: Offline Capability

**Requirement**: Core catch reporting must function fully offline, with automatic synchronisation when connectivity is restored. Offline data must be stored securely on device.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: ICES Stock Assessment Database

**Purpose**: Ingest stock assessment outputs for TAC advice and MSY reference points.

**Integration Type**: Batch API (annual primary advice, quarterly updates)

**Data Exchanged**: Stock codes, MSY reference points (Fmsy, Bmsy), TAC advice, stock status

**Priority**: MUST_HAVE

---

### INT-2: MMO VMS Data Feed

**Purpose**: Cross-reference vessel positions with declared catch areas for validation.

**Integration Type**: Near-real-time API (polling every 5 minutes)

**Data Exchanged**: Vessel ID, position, timestamp, speed

**Priority**: SHOULD_HAVE

---

### INT-3: MMO Vessel Registry

**Purpose**: Validate vessel registration, licence, and gear authorisation data.

**Integration Type**: Real-time API

**Data Exchanged**: Vessel registration number, licence conditions, authorised gears, owner details

**Priority**: MUST_HAVE

---

### INT-4: Devolved Administration Quota Systems

**Purpose**: Share quota utilisation data with Scottish, Welsh, and Northern Irish fisheries administrations for UK-level stock monitoring.

**Integration Type**: API (real-time quota data exchange)

**Data Exchanged**: Quota stock utilisation by UK administration, TAC shares, trade notifications

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Catch Report

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| report_id | UUID | Yes | Unique report identifier | Primary key |
| vessel_id | String(12) | Yes | Vessel registration number | Foreign key to vessel registry |
| trip_start | Timestamp | Yes | Departure date/time | |
| trip_end | Timestamp | Yes | Return date/time | After trip_start |
| landing_port | String(6) | Yes | Port code | Valid UK port code |
| species_catches | JSONB | Yes | Array of species/weight/area | Non-empty |
| gear_type | String(6) | Yes | EU gear code | Valid gear code |
| ices_area | String(10) | Yes | ICES statistical rectangle | Valid ICES area |
| submission_method | Enum | Yes | Source of report | elogbook/mobile_app/paper_entry |
| vms_validated | Boolean | No | Whether VMS cross-check passed | |

**Data Volume**: ~500,000 reports/year, growing to 600,000 with under-10m digital adoption

**Data Classification**: OFFICIAL (OFFICIAL-SENSITIVE at vessel level)

---

#### Entity 2: Quota Stock

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| stock_id | String(20) | Yes | Species + area code | Primary key |
| species_code | String(3) | Yes | FAO species code | Valid FAO code |
| ices_area | String(10) | Yes | ICES management area | |
| annual_tac | Decimal | Yes | Total Allowable Catch (tonnes) | >0 |
| uk_share | Decimal | Yes | UK share of TAC (tonnes) | >0 |
| england_allocation | Decimal | Yes | England allocation (tonnes) | >0 |
| cumulative_catch | Decimal | Yes | Year-to-date catch (tonnes) | >=0 |
| utilisation_pct | Decimal | Yes | Calculated utilisation | 0-100+ |
| msy_fmsy | Decimal | No | ICES Fmsy reference point | |
| quota_year | Integer | Yes | Quota year | |

**Data Volume**: ~100 stocks/year

**Data Classification**: OFFICIAL

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with existing MMO vessel registry — no replacement of vessel licensing system

**TC-2**: Mobile app must work on Android 10+ and iOS 15+ (covering 95% of fisher smartphones)

**TC-3**: Must accommodate paper catch return data entry for non-adopting fishers during transition period

### Business Constraints

**BC-1**: Budget cap of GBP 12M capital over 3 years

**BC-2**: Mandatory eLogbook for under-10m requires secondary legislation — system must work with voluntary adoption initially

**BC-3**: Annual fisheries negotiations (EU, Norway) create TAC uncertainty until December each year — system must handle late TAC confirmation

### Assumptions

**A-1**: Under-10m fishers own smartphones capable of running a native app (estimated 85% currently)

**A-2**: Harbour Wi-Fi coverage sufficient for catch report upload in major landing ports

**A-3**: ICES will continue to provide stock assessment data in machine-readable format

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Under-10m electronic reporting | 5% | 80% | 18 months | System adoption data |
| Catch data latency (all fleet) | 4-6 weeks (u10m) | <48 hours | 12 months | Data pipeline metrics |
| Quota utilisation accuracy | +-15% | +-3% | 12 months | Reconciliation audit |
| Quota trade processing time | 5 days | Same-day | 9 months | System logs |
| Paper catch returns | 55,000/year | <5,500/year | 18 months | MMO records |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| MMO SRO | Executive Sponsor | [ ] Approved | | |
| MMO Head of Quota | Operations Lead | [ ] Approved | | |
| Cefas Stock Assessment Lead | Scientific Authority | [ ] Approved | | |
| NFFO Representative | Large Fleet | [ ] Approved | | |
| NUTFA Representative | Small Fleet | [ ] Approved | | |
| MMO Enterprise Architect | Architecture | [ ] Approved | | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| TAC | Total Allowable Catch — annual catch limit set for a fish stock |
| FQA | Fixed Quota Allocation — historic entitlement share used to allocate quota |
| PO | Producer Organisation — industry body managing quota on behalf of member vessels |
| MSY | Maximum Sustainable Yield — highest catch that can be taken indefinitely |
| FMP | Fisheries Management Plan — statutory plan under the Fisheries Act 2020 |
| eLogbook | Electronic logbook for digital catch reporting |
| VMS | Vessel Monitoring System — satellite tracking for fishing vessels |
| ICES | International Council for the Exploration of the Sea |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fishing Quota Management
**Model**: Claude Opus 4.6
