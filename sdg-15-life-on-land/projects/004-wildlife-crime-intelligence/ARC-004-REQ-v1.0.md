# Project Requirements: Wildlife Crime Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Wildlife Crime Intelligence (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Wildlife Crime Intelligence |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, NCA, NWCU, DEFRA, Border Force, NPCC Wildlife Crime Lead, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Wildlife Crime Intelligence platform — a unified digital system enabling the National Wildlife Crime Unit (NWCU), territorial police forces, Border Force, and partner agencies to submit, grade, analyse, and disseminate wildlife crime intelligence in accordance with the National Intelligence Model (NIM) and 5x5x5 intelligence grading system.

---

## Executive Summary

### Business Context

Wildlife crime in the UK encompasses a range of offences from raptor persecution on grouse moors to international trafficking in endangered species. The National Wildlife Crime Unit (NWCU), a small team of approximately 12 staff hosted within the NCA and funded by DEFRA and the Home Office, coordinates the UK's response across seven priority crime types: badger persecution, bat persecution, CITES issues, freshwater pearl mussels, poaching, raptor persecution, and trade in endangered species.

Currently, wildlife crime intelligence is fragmented across email inboxes, local police force recording systems, RSPB databases, Border Force seizure records, and DEFRA CITES permit records. There is no single platform to collate, grade, analyse, and disseminate intelligence. The NWCU Strategic Assessment consistently identifies this fragmentation as the primary barrier to effective enforcement. The UK has committed internationally (through the Illegal Wildlife Trade Conference and CITES obligations) to strengthen wildlife crime enforcement.

### Objectives

- Deliver a NIM-compliant wildlife crime intelligence platform accessible to all 43 territorial police forces
- Implement 5x5x5 intelligence grading for all intelligence submissions
- Integrate CITES permit verification for Border Force enforcement at ports
- Enable structured intelligence sharing with accredited partner organisations (RSPB, RSPCA)
- Support international intelligence exchange with INTERPOL and Europol

### Expected Outcomes

- Intelligence-led enforcement operations increase by 50% within 2 years
- Time from intelligence submission to dissemination reduced from weeks to 48 hours
- Border seizures of illegal wildlife products increase by 30%
- 80% of active Wildlife Crime Officers submitting intelligence through the platform

### Project Scope

**In Scope**:

- Intelligence submission portal (web and mobile) for police WCOs and partner agencies
- 5x5x5 intelligence grading and sanitisation workflow
- National intelligence database with search and analysis capabilities
- CITES permit verification API for Border Force targeting systems
- Species identification support tools
- Intelligence product generation (problem profiles, subject profiles)
- Strategic threat assessment analytics
- Secure international intelligence exchange (INTERPOL I-24/7 format)
- Structured NGO intelligence-sharing framework
- Proceeds of Crime Act (POCA) financial investigation support tools

**Out of Scope**:

- General police crime recording systems (intelligence only, not case management)
- Prosecution case file management (CPS responsibility)
- Customs declarations processing (HMRC/Border Force systems)
- Wildlife rehabilitation and welfare (RSPCA operational systems)
- Forensic evidence management (DNA, toxicology)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Executive Sponsor | NCA | Decision maker |
| NWCU Head | Unit leadership | NWCU/NCA | Operational requirements |
| NCA CTO | IT strategy | NCA | Architecture, security |
| NPCC WC Lead | Police coordination | NPCC | Multi-force requirements |
| Border Force WC Lead | Border enforcement | Home Office | CITES integration |
| DEFRA CITES Authority | Permit management | DEFRA | CITES data integration |
| Police WCOs | Intelligence contributors | 43 forces | User acceptance |
| RSPB Investigations | Intelligence partner | RSPB | NGO intelligence framework |
| CPS | Prosecution authority | CPS | Evidence standards |
| INTERPOL Env Security | International partner | INTERPOL | International exchange |

---

## Business Requirements

### BR-1: Unified National Intelligence Database

**Description**: Establish a single, authoritative intelligence database for wildlife crime across the UK, compliant with the National Intelligence Model (NIM), enabling intelligence submission, grading, storage, analysis, and dissemination from a unified platform.

**Rationale**: Intelligence fragmentation is the single largest barrier to effective wildlife crime enforcement. Critical intelligence about subjects, locations, and methodologies is currently trapped in individual officer emails, local police systems, and partner organisation databases. A unified platform enables pattern identification, strategic assessment, and coordinated enforcement that is impossible with fragmented data.

**Success Criteria**:

- Single authoritative intelligence database covering all 7 UK wildlife crime priorities
- All intelligence graded using 5x5x5 system
- Cross-referencing capability across subjects, locations, species, and methodologies
- Strategic threat assessment producible from platform data

**Priority**: MUST_HAVE

**Stakeholder**: NWCU Head, NCA Director General

---

### BR-2: Accessible Intelligence Submission for Police WCOs

**Description**: Provide a simple, accessible intelligence submission mechanism that enables Wildlife Crime Officers across all 43 territorial police forces to submit intelligence with minimal friction, from standard police IT environments, in under 10 minutes per submission.

**Rationale**: Most WCOs are not full-time wildlife crime officers — they handle wildlife crime alongside other duties with limited dedicated time. If intelligence submission takes too long, requires specialist access, or is too complex, WCOs simply will not use it. Previous systems failed because they were designed for intelligence analysts rather than frontline officers.

**Success Criteria**:

- Intelligence submission completed in < 10 minutes
- Platform accessible from standard police force IT environments (no separate VPN/credentials)
- Mobile submission capability for field reporting
- 80% of active WCOs using platform within 12 months

**Priority**: MUST_HAVE

**Stakeholder**: Police WCOs, NPCC WC Lead

---

### BR-3: CITES Permit Verification and Border Enforcement

**Description**: Integrate CITES permit data with Border Force targeting systems to enable real-time permit verification, species identification support, and intelligence alerts for wildlife trade consignments at ports of entry.

**Rationale**: The UK processes over 30,000 CITES permits annually. Border Force officers at airports, seaports, and postal hubs need rapid permit verification and intelligence about trafficking trends to identify illegal shipments among high volumes of legitimate trade. Current manual verification is slow and relies on officer expertise in species identification — a specialist skill most Border Force officers lack.

**Success Criteria**:

- Real-time CITES permit verification available at all major ports (from manual lookup)
- Species identification support for CITES Appendix I species with > 95% accuracy
- Intelligence alerts integrated into Border Force targeting workflow
- Permit verification time < 2 minutes (from 30 minutes)

**Priority**: MUST_HAVE

**Stakeholder**: Border Force, DEFRA CITES Authority

---

### BR-4: 5x5x5 Intelligence Grading and Sanitisation

**Description**: Implement the 5x5x5 intelligence grading system for all intelligence submissions, with automated sanitisation workflows that enable secure sharing at appropriate classification levels across agencies with different security clearances.

**Rationale**: The 5x5x5 system (source reliability, intelligence evaluation, handling conditions) is the national standard for intelligence management. It enables secure sharing by separating the intelligence content from the source identity. Sanitisation allows intelligence derived from sensitive sources (informants, covert operations) to be shared more widely in a form that protects the source.

**Success Criteria**:

- 100% of intelligence submissions graded using 5x5x5
- Automated sanitisation reducing NWCU analyst workload by 30%
- Handling conditions enforced by platform access controls
- Audit trail of all intelligence access and dissemination

**Priority**: MUST_HAVE

**Stakeholder**: NWCU Head, NCA CTO

---

### BR-5: Financial Investigation Support (POCA)

**Description**: Provide tools supporting financial investigation of wildlife crime under the Proceeds of Crime Act 2002, including financial profiling, suspicious transaction tracking, and asset recovery case management.

**Rationale**: Wildlife crime is increasingly recognised as a serious organised crime with significant financial dimensions — international trafficking in endangered species can generate millions of pounds. POCA provides powerful tools for disrupting criminal enterprises through financial investigation, but these are under-used in wildlife crime because of the lack of digital tools for financial analysis in this domain. The NCA's financial investigation capability should extend to wildlife crime.

**Success Criteria**:

- Financial profiling tool integrated with intelligence records
- Suspicious transaction pattern detection for wildlife trade
- POCA case tracking with asset recovery outcomes
- Integration with NCA financial investigation systems

**Priority**: SHOULD_HAVE

**Stakeholder**: NCA, HMRC

---

## Functional Requirements

### User Personas

#### Persona 1: PC Dave — Wildlife Crime Officer (Part-Time)

- **Role**: Police Constable with wildlife crime as one of many responsibilities in a rural force
- **Goals**: Submit intelligence quickly, search for known offenders, access species guides
- **Pain Points**: Limited time, standard police laptop, poor rural connectivity, minimal training
- **Technical Proficiency**: Low-Medium

#### Persona 2: Analyst Kate — NWCU Intelligence Analyst

- **Role**: Full-time intelligence analyst at NWCU
- **Goals**: Analyse patterns, produce intelligence products, manage dissemination
- **Pain Points**: Manual data collation from emails, inconsistent intelligence quality, limited tools
- **Technical Proficiency**: High

#### Persona 3: Officer Hassan — Border Force (Port)

- **Role**: Border Force Officer at a major airport
- **Goals**: Verify CITES permits quickly, identify suspicious consignments, seize illegal goods
- **Pain Points**: Manual permit checks, no species expertise, time pressure at border
- **Technical Proficiency**: Medium

#### Persona 4: Dr. Ruth — RSPB Senior Investigator

- **Role**: RSPB investigations team member focused on raptor persecution
- **Goals**: Submit intelligence on suspicious raptor deaths, track satellite-tagged birds, receive operational feedback
- **Pain Points**: Informal intelligence sharing, lack of feedback on submitted intelligence
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-1: Intelligence Submission Portal

**Description**: The system must provide a web-based and mobile intelligence submission form that enables WCOs and accredited partners to submit wildlife crime intelligence with structured data fields and 5x5x5 grading.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a WCO, when they access the submission form, then they can complete and submit intelligence in < 10 minutes
- [ ] Given a submission, when species is entered, then auto-complete suggests from UK species list with common and scientific names
- [ ] Given a submission, when 5x5x5 grading is selected, then system validates grading completeness before allowing submission
- [ ] Given poor connectivity, when using mobile app, then submission is stored locally and synced when connection restored

**Data Requirements**:

- **Inputs**: Subject details, location (grid reference or map pin), species involved, offence type, 5x5x5 grading, free-text narrative, attachments (photos, documents)
- **Outputs**: Intelligence reference number, acknowledgement, estimated processing time

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-2: 5x5x5 Grading and Handling Workflow

**Description**: The system must enforce 5x5x5 intelligence grading on all submissions and implement handling conditions that control access, dissemination, and retention based on the grading.

**Relates To**: BR-4

**5x5x5 Components**:

| Grade | Scale | Description |
|-------|-------|-------------|
| Source Evaluation (1st 5) | A-E, X | Reliability of source (A=always reliable, E=unreliable, X=untested) |
| Intelligence Evaluation (2nd 5) | 1-5 | Accuracy of intelligence (1=known true, 5=suspected false) |
| Handling Conditions (3rd 5) | 1-5 | Dissemination restrictions (1=unrestricted, 5=source's identity requires protection) |

**Acceptance Criteria**:

- [ ] Given a graded submission, when handling condition 5 (source protection) is applied, then source identity is separated from intelligence content in all views except NWCU analysts
- [ ] Given handling conditions, when intelligence is disseminated, then access controls enforce the handling restrictions automatically
- [ ] Given a time-limited handling condition, when expiry is reached, then system alerts NWCU analyst for review and potential downgrade

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Intelligence Search and Analysis

**Description**: The system must provide search and analysis capabilities enabling NWCU analysts to identify patterns across subjects, locations, species, time periods, and methodologies.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a subject name, when searched, then all related intelligence is returned (including aliases, associates, linked addresses)
- [ ] Given a location, when searched geospatially, then all intelligence within configurable radius is returned, with heat map visualisation
- [ ] Given a species, when trend analysis runs, then seasonal patterns, geographic hotspots, and method trends are displayed
- [ ] Given a time period and crime type, when analysis runs, then system generates a problem profile with key findings

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-4: CITES Permit Verification API

**Description**: The system must provide a real-time API for Border Force to verify CITES permit authenticity, check species against appendix listings, and receive intelligence alerts for consignments.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a CITES permit number, when verification is requested, then permit validity, species, quantities, and exporting country are returned within 2 seconds
- [ ] Given a species common name or scientific name, when looked up, then CITES appendix listing and trade restrictions are returned
- [ ] Given a consignment flagged as high-risk by intelligence, when scanned at port, then alert is displayed to Border Force officer with intelligence summary (sanitised)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: Species Identification Support

**Description**: The system must provide species identification tools for non-specialist users, including image-based identification, morphological guides, and common/scientific name cross-referencing for CITES-listed species.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a photo of a wildlife product (ivory, scales, feathers, shells), when uploaded, then system suggests most likely species with confidence score
- [ ] Given a species, when identification guide is accessed, then key morphological features, CITES listing, and legal status are displayed
- [ ] Given a common name, when entered, then scientific name, CITES appendix, and UK legal protection status are returned

**Priority**: SHOULD_HAVE

**Complexity**: HIGH (image recognition element)

---

#### FR-6: Intelligence Product Generation

**Description**: The system must support generation of standard intelligence products — problem profiles, subject profiles, and the annual strategic threat assessment — using data held in the platform.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a crime type, when problem profile is requested, then system generates a structured report with intelligence summary, trend analysis, key subjects, geographic analysis, and knowledge gaps
- [ ] Given a subject, when profile is requested, then all related intelligence, associates, locations, and criminal history summary are compiled
- [ ] Given a reporting period, when strategic assessment is generated, then all 7 priority crime types are analysed with threat ratings

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-7: International Intelligence Exchange

**Description**: The system must support structured intelligence exchange with INTERPOL Environmental Security and Europol, using agreed exchange formats and secure communication channels.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an intelligence item flagged for international sharing, when approved by NWCU analyst, then it is formatted for INTERPOL I-24/7 secure communication
- [ ] Given an incoming INTERPOL notice (Purple Notice for wildlife crime), when received, then it is ingested into the platform with appropriate handling
- [ ] Given a cross-border investigation, when intelligence package is prepared, then it includes UK legal context and handling restrictions for recipient

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

#### FR-8: NGO Intelligence Submission Channel

**Description**: The system must provide accredited NGO investigators (RSPB, RSPCA, EIA) with a dedicated intelligence submission channel with feedback mechanisms.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given an accredited NGO investigator, when they submit intelligence, then it enters the standard 5x5x5 grading workflow
- [ ] Given NGO-submitted intelligence, when actioned, then submitter receives feedback on status (received/under review/actioned/closed) within 10 working days
- [ ] Given satellite tag tracking data from RSPB, when submitted in bulk, then system can ingest structured datasets with geospatial and temporal data

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**:

- Intelligence submission form load: < 2 seconds
- Intelligence search (simple): < 3 seconds
- Intelligence search (complex/geospatial): < 10 seconds
- CITES permit verification API: < 2 seconds (95th percentile)
- Species identification (image): < 5 seconds

**Priority**: HIGH

---

### Availability

#### NFR-A-1: Availability Target

**Requirement**: 99.9% uptime for core intelligence platform (intelligence may be needed during time-critical enforcement operations at any hour).

- CITES verification API: 99.9% (port operations are 24/7)
- Intelligence submission: 99.5% (mobile offline capability provides resilience)

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Security Classification

**Requirement**: Platform must be accredited to handle OFFICIAL and OFFICIAL-SENSITIVE data. Specific intelligence items may be handled at OFFICIAL-SENSITIVE with appropriate marking and access controls.

**Security Accreditation**: NCA IT Security policy compliance required. Risk assessment and accreditation (RA&A) before go-live.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Access Control

**Requirement**: Tiered access model:

- **Tier 1 (Submission)**: Police WCOs, accredited NGOs — submit intelligence, search basic records — accessible from police force networks at OFFICIAL
- **Tier 2 (Analysis)**: NWCU analysts — full intelligence access, grading, dissemination — NCA secure environment at OFFICIAL-SENSITIVE
- **Tier 3 (Administration)**: NCA IT — system administration, audit, security management

**Priority**: CRITICAL

---

#### NFR-SEC-3: Audit Logging

**Requirement**: Comprehensive, immutable audit trail of all intelligence access, searches, and dissemination — supporting legal evidence chain and accountability.

**Audit Requirements**:

- Who accessed what intelligence, when, and from where
- All search queries recorded (for disclosure compliance)
- All dissemination decisions recorded with approver identity
- Logs retained for minimum 7 years (criminal investigation timeline)

**Priority**: CRITICAL

---

#### NFR-SEC-4: Protected Species Location Redaction

**Requirement**: Intelligence containing locations of protected species (particularly nesting sites of Schedule 1 birds) must have location data redacted to 10km grid square in Tier 1 views. Precise locations only visible to Tier 2 analysts and investigating officers.

**Priority**: CRITICAL (location disclosure could enable poaching)

---

### Compliance

#### NFR-C-1: Data Protection

**Requirement**: Compliance with UK GDPR, Data Protection Act 2018, and Law Enforcement Directive (Part 3 DPA 2018 for law enforcement processing). DPIA required before processing.

**Priority**: CRITICAL

---

#### NFR-C-2: RIPA Compliance

**Requirement**: Any features enabling surveillance-type activity (satellite tracking, pattern analysis of individuals) must comply with Regulation of Investigatory Powers Act 2000 and Investigatory Powers Act 2016. Authorisation workflows built into platform where applicable.

**Priority**: CRITICAL

---

#### NFR-C-3: Disclosure and CPIA

**Requirement**: The system must support Criminal Procedure and Investigations Act 1996 (CPIA) disclosure obligations — the ability to identify and disclose unused material relevant to prosecution.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: DEFRA CITES Permit Database

**Purpose**: Real-time CITES permit verification

**Integration Type**: RESTful API (real-time query)

**Data Exchanged**: Permit number, validity, species, quantities, exporting/importing country, permit holder

**Priority**: CRITICAL

---

### INT-2: Police National Computer (PNC)

**Purpose**: Criminal history checks on wildlife crime subjects

**Integration Type**: PNC gateway (read-only query)

**Data Exchanged**: Subject details, criminal history, wanted/missing alerts

**Authentication**: PNC user authentication, RBAC

**Priority**: HIGH

---

### INT-3: Border Force Targeting Systems

**Purpose**: Intelligence alerts for consignment risk assessment

**Integration Type**: RESTful API (push alerts)

**Data Exchanged**: Risk indicators, intelligence summaries (sanitised), species of concern

**Priority**: HIGH

---

### INT-4: INTERPOL I-24/7

**Purpose**: International intelligence exchange for cross-border wildlife crime

**Integration Type**: Secure messaging (INTERPOL communication format)

**Data Exchanged**: Intelligence reports, Purple Notices, diffusion notices

**Priority**: MEDIUM

---

### INT-5: National Biodiversity Network Atlas

**Purpose**: Species distribution and recording data for intelligence context

**Integration Type**: RESTful API

**Data Exchanged**: Species occurrence records, distribution maps

**Priority**: LOW

---

## Data Requirements

### Data Entities

#### Entity 1: Intelligence Report

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| report_id | UUID | Yes | Unique reference | Primary key |
| submitter_id | UUID | Yes | Submitting officer/organisation | Foreign key, audit |
| crime_priority | Enum | Yes | Wildlife crime priority | 7 UK priorities |
| species | String[] | Yes | Species involved | From UK species list |
| offence_type | Enum | Yes | Type of offence | From wildlife crime taxonomy |
| location | Geometry (Point/Polygon) | Yes | Location of activity | Grid reference or boundary |
| location_precision | Enum | Yes | Precision level | ['exact', '1km', '10km'] |
| date_of_activity | Date | No | When activity occurred | Approximate if unknown |
| narrative | Text | Yes | Intelligence narrative | Free text, max 5000 chars |
| source_evaluation | Char(1) | Yes | 5x5x5 source grade | A-E, X |
| intelligence_evaluation | Char(1) | Yes | 5x5x5 intelligence grade | 1-5 |
| handling_code | Char(1) | Yes | 5x5x5 handling condition | 1-5 |
| status | Enum | Yes | Lifecycle status | ['submitted', 'graded', 'actioned', 'closed'] |
| classification | Enum | Yes | Security classification | ['OFFICIAL', 'OFFICIAL-SENSITIVE'] |

**Data Volume**: 5,000 intelligence reports per year initially, target 15,000

**Data Retention**: Aligned with Management of Police Information (MoPI) retention schedules — typically 6 years for standard intelligence, longer for serious/organised crime

---

#### Entity 2: CITES Permit

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| permit_id | String | Yes | CITES permit number | Unique, country-prefixed |
| permit_type | Enum | Yes | Import/Export/Re-export | CITES permit types |
| species_scientific | String | Yes | Scientific name | CITES taxonomy |
| species_common | String | No | Common name | Localised |
| appendix | Enum | Yes | CITES appendix | I, II, III |
| quantity | Integer | Yes | Number of specimens/items | Positive |
| unit | String | Yes | Unit of measure | Pieces, kg, litres |
| exporting_country | String(2) | Yes | ISO country code | ISO 3166-1 |
| valid_from | Date | Yes | Permit validity start | |
| valid_to | Date | Yes | Permit validity end | |
| status | Enum | Yes | Permit status | ['valid', 'expired', 'revoked', 'used'] |

**Data Volume**: 30,000 permits per year

**Data Retention**: 10 years

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy on NCA-accredited infrastructure meeting OFFICIAL-SENSITIVE security requirements

**TC-2**: Must be accessible from 43 different police force IT environments (diverse browsers, firewalls, proxies)

**TC-3**: INTERPOL I-24/7 integration requires dedicated secure network connectivity

**TC-4**: PNC integration requires approved PNC gateway access

### Business Constraints

**BC-1**: NWCU has approximately 12 staff — platform must not create unsustainable operational overhead

**BC-2**: Total programme budget £5M over 3 years (joint DEFRA/Home Office funding)

**BC-3**: Must achieve security accreditation before processing operational intelligence

### Assumptions

**A-1**: DEFRA will provide CITES permit data via API within required timescale

**A-2**: Police forces will authorise access to the platform from force IT environments

**A-3**: NCA will provide hosting infrastructure meeting OFFICIAL-SENSITIVE requirements

**A-4**: INTERPOL will approve UK gateway for I-24/7 integration

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| WCO platform adoption | ~30% ad hoc | >80% active WCOs | 12 months | User analytics |
| Intelligence submission to dissemination | Weeks | 48 hours | 6 months | Platform workflow timing |
| Intelligence-led operations | Baseline year 1 | +50% | 2 years | NWCU operational records |
| CITES permit verification time | 30 minutes | < 2 minutes | 6 months | API response analytics |
| Border seizures | Baseline year 1 | +30% | 2 years | Border Force seizure data |
| POCA asset recovery from wildlife crime | < £500K/year | £2M/year | 3 years | NCA financial records |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.9% | Uptime monitoring |
| CITES API response time (p95) | < 2 seconds | APM tooling |
| Intelligence search time | < 10 seconds | Platform analytics |
| Security accreditation | Achieved pre-launch | NCA RA&A |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| NWCU | National Wildlife Crime Unit — UK coordination unit for wildlife crime |
| NCA | National Crime Agency — UK law enforcement agency hosting NWCU |
| WCO | Wildlife Crime Officer — police officer with wildlife crime responsibilities |
| 5x5x5 | Intelligence grading system (source evaluation, intelligence evaluation, handling) |
| NIM | National Intelligence Model — UK standard for intelligence-led policing |
| CITES | Convention on International Trade in Endangered Species |
| POCA | Proceeds of Crime Act 2002 |
| MoPI | Management of Police Information — retention and review standards |
| RIPA | Regulation of Investigatory Powers Act 2000 |

### Appendix B: UK Wildlife Crime Priorities

1. Badger persecution
2. Bat persecution
3. CITES issues (international trade)
4. Freshwater pearl mussels
5. Poaching (deer, fish, hare coursing)
6. Raptor persecution
7. Trade in endangered species (domestic)

### Appendix C: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 15 Architecture Principles
- ARC-004-STKE-v1.0 — Wildlife Crime Intelligence Stakeholder Analysis
- Wildlife and Countryside Act 1981
- CITES Convention
- National Intelligence Model (College of Policing)
- UK Wildlife Crime Priorities (DEFRA/Home Office)

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wildlife Crime Intelligence
**Model**: Claude Opus 4.6
