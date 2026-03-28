# Project Requirements: School Meals Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | School Meals Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DfE Free School Meals Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Digital, HMRC, DWP, Local Authorities, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the School Meals Management System, covering FSM eligibility determination, auto-enrolment via the Eligibility Checking Service (ECS), local authority management, and meal delivery tracking. Traceable to ARC-002-STKE-v1.0 and aligned with ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

Free school meals (FSM) in England serve approximately 1.9 million pupils through two programmes: Universal Infant Free School Meals (UIFSM) for all Reception, Year 1, and Year 2 pupils regardless of income, and benefits-based FSM for pupils in Years 3-13 whose families receive qualifying benefits (Universal Credit with net earnings threshold, Income Support, income-based JSA/ESA, Child Tax Credit below threshold, and support under Part VI of the Immigration and Asylum Act 1999).

The current system relies on the Eligibility Checking Service (ECS), which allows local authorities and schools to check individual pupil eligibility against HMRC and DWP benefits records. However, ECS is a check-on-request service -- it requires families to apply first. An estimated 11% of eligible families (approximately 215,000 children) do not claim, missing out on meals worth approximately £440/year per child and triggering approximately £1,480/year in Pupil Premium funding per pupil.

### Objectives

- Implement auto-enrolment to close the FSM eligibility gap from 11% to < 3%
- Provide a unified national platform for all 152 local authorities
- Integrate with HMRC and DWP benefits systems for real-time eligibility verification
- Enable accurate national reporting on FSM uptake for Pupil Premium funding allocation
- Publish FSM metrics to the National Food Strategy Dashboard (Project 005)

### Expected Outcomes

- 155,000+ additional children auto-enrolled, worth £68M/year in direct nutritional benefit
- 40% reduction in local authority FSM administration costs (estimated £8M/year savings)
- Accurate Pupil Premium allocation saving £12M/year in over/under-payments
- Real-time national visibility of FSM uptake by region, school, and demographic

### Project Scope

**In Scope**:

- Auto-enrolment engine using HMRC/DWP benefits data matching
- Local authority management portal
- School-level meal delivery tracking
- Pupil Premium funding calculation engine
- National reporting and analytics dashboards
- API for National Food Strategy Dashboard (Project 005)
- Parent/carer notification and opt-out management

**Out of Scope**:

- UIFSM logistics (universal provision does not require eligibility checking)
- School catering procurement
- Meal menu planning and nutritional analysis
- Holiday Activities and Food (HAF) programme (separate DfE initiative)
- Devolved nations (Scotland, Wales, Northern Ireland have separate schemes)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO, FSM Programme | Programme Sponsor | DfE | Decision maker |
| DfE CDO | Architecture Oversight | DfE | Technical governance |
| DfE DPO | Privacy and Data Protection | DfE | DPIA sign-off |
| HMRC Benefits Data Team Lead | Data Provider | HMRC | Integration design |
| DWP UC Data Team Lead | Data Provider | DWP | Integration design |
| LA Reference Group (10 pilot LAs) | Co-design Partners | Local Authorities | Requirements and testing |
| School Business Managers | End Users | Schools | User testing |
| Parent/Carer Representatives | Beneficiaries | Citizens | User research |
| CDDO Assessment Team | Standards Assurance | CDDO | Service assessment |

---

## Business Requirements

### BR-001: Automatic Eligibility Identification

**Description**: The system must automatically identify children eligible for benefits-based FSM by matching pupil records against HMRC and DWP benefits data, without requiring a parental application.

**Rationale**: The 11% eligibility gap exists primarily because families do not apply. Auto-identification removes this barrier (Stakeholder Driver SD-1, SD-5).

**Success Criteria**:

- Match accuracy > 98% (validated against manual verification sample)
- Eligibility gap reduced from 11% to < 3% within 18 months
- Processing of full national pupil cohort (6.5M pupils) completed within 48 hours per cycle

**Priority**: MUST_HAVE

**Stakeholder**: Minister (SD-1), Parents (SD-5)

---

### BR-002: Unified Local Authority Platform

**Description**: The system must provide a single national platform for FSM eligibility management used by all 152 local authorities, replacing fragmented local systems.

**Rationale**: Current fragmentation creates data inconsistency, prevents national reporting, and increases aggregate costs (Stakeholder Driver SD-2, SD-4).

**Success Criteria**:

- 152/152 local authorities onboarded within 24 months of launch
- 95% of eligibility checks processed through the platform
- Consistent data quality across all authorities

**Priority**: MUST_HAVE

**Stakeholder**: Director of School Food (SD-2), Local Authorities (SD-4)

---

### BR-003: Compliant Cross-Departmental Data Sharing

**Description**: The system must implement lawful, purpose-limited data sharing between DfE, HMRC, and DWP for FSM eligibility determination, compliant with UK GDPR, Data Protection Act 2018, CRCA 2005, and ICO Children's Code.

**Rationale**: Auto-enrolment depends on benefits data. Data sharing must be legally robust and privacy-preserving (Stakeholder Driver SD-3, SD-6).

**Success Criteria**:

- DPIA approved by DfE DPO with ICO positive assessment
- Data sharing limited to eligibility confirmation (yes/no), not raw benefits data
- Zero ICO enforcement actions or data breach incidents
- Annual privacy audit pass

**Priority**: MUST_HAVE

**Stakeholder**: HMRC (SD-3), ICO (SD-6)

---

### BR-004: Pupil Premium Funding Accuracy

**Description**: The system must provide accurate FSM registration data to support Pupil Premium funding calculations, eliminating discrepancies between eligibility and registration data.

**Rationale**: Pupil Premium funding (£1,480 per FSM-eligible primary pupil, £1,050 per secondary) is allocated based on FSM registration. Inaccurate data leads to £12M/year in estimated over/under-payments.

**Success Criteria**:

- Pupil Premium data reconciliation accuracy > 99.5%
- Funding calculation available within 5 working days of census date
- Discrepancy resolution process completed within 10 working days

**Priority**: MUST_HAVE

**Stakeholder**: DfE Finance (S-6)

---

## Functional Requirements

### User Personas

#### Persona 1: Local Authority FSM Officer

- **Role**: Education Benefits Officer, local authority
- **Goals**: Process eligibility checks efficiently, manage appeals, report FSM uptake to council
- **Pain Points**: Manual processes, multiple systems, high workload during term start
- **Technical Proficiency**: Low to Medium (varies by authority)

#### Persona 2: School Business Manager

- **Role**: School business manager responsible for meal ordering and Pupil Premium tracking
- **Goals**: Know which pupils are FSM-eligible, track meal uptake, claim Pupil Premium
- **Pain Points**: Delayed eligibility notifications, parents not returning forms, manual tracking
- **Technical Proficiency**: Medium

#### Persona 3: Parent/Carer

- **Role**: Parent or carer of school-age child
- **Goals**: Ensure child receives free meals if eligible, without complex processes or stigma
- **Pain Points**: Confusing application process, evidence requirements, stigma
- **Technical Proficiency**: Low to Medium

---

### Functional Requirements Detail

#### FR-001: Eligibility Matching Engine

**Description**: The system must match pupil records against HMRC/DWP benefits data to determine FSM eligibility automatically.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a national pupil database extract, when matched against HMRC/DWP data, then eligible pupils are identified with > 98% accuracy
- [ ] Given a pupil with qualifying benefits, when matched, then eligibility status is confirmed within 24 hours
- [ ] Given a pupil whose circumstances change (gains/loses eligibility), when the next matching cycle runs, then their status is updated
- [ ] Given a matching ambiguity (partial name match, address discrepancy), then the record is flagged for manual review

**Data Requirements**:

- **Inputs**: Pupil records (name, DOB, address, parent/carer details), HMRC benefits status, DWP UC status
- **Outputs**: Eligibility determination (eligible/not eligible/manual review), confidence score
- **Validations**: Name matching algorithms, address normalisation, DOB validation

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: Auto-Enrolment and Parent Notification

**Description**: The system must automatically enrol identified eligible pupils and notify parents/carers with an opt-out mechanism.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:

- [ ] Given a newly identified eligible pupil, when confirmed by matching engine, then parent/carer is notified via GOV.UK Notify
- [ ] Given a notification sent, when 14 days have passed without opt-out, then the pupil is auto-enrolled for FSM
- [ ] Given a parent opting out, when opt-out is received, then the pupil is not enrolled and the decision is recorded
- [ ] Given notifications, when sent, then they are available in English and the top 10 community languages

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-003: Local Authority Management Portal

**Description**: The system must provide a web-based portal for local authorities to manage FSM eligibility, view auto-enrolment status, handle appeals, and generate reports.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given an LA officer login, when accessing the portal, then a dashboard shows FSM statistics for their authority area
- [ ] Given a manual eligibility check request, when submitted with pupil details, then ECS returns a result within 10 seconds
- [ ] Given an appeal, when submitted by a parent, then it is routed to the relevant LA officer with supporting evidence
- [ ] Given reporting needs, when generating a report, then data can be filtered by school, ward, age group, and eligibility type

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-004: School Meal Delivery Tracking

**Description**: The system must track daily meal uptake at school level, enabling monitoring of whether eligible pupils are actually receiving meals.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a school with FSM-eligible pupils, when daily meal counts are submitted, then uptake rates are calculated per school
- [ ] Given an eligible pupil consistently not taking meals, when detected (5+ consecutive days), then an alert is generated for the school
- [ ] Given meal delivery data, when aggregated nationally, then uptake reports are available by region and demographic

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-005: Pupil Premium Calculation Engine

**Description**: The system must calculate Pupil Premium funding entitlements based on FSM registration data aligned with School Census dates.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given School Census data, when processed, then Pupil Premium entitlements are calculated per school
- [ ] Given the "Ever 6" rule (pupil eligible if registered FSM at any point in last 6 years), when applied, then historical eligibility is correctly tracked
- [ ] Given calculated entitlements, when exported, then data is compatible with DfE funding allocation systems

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-006: National Reporting Dashboard

**Description**: The system must provide national-level dashboards showing FSM uptake, eligibility gap, auto-enrolment progress, and Pupil Premium data.

**Relates To**: BR-002, BR-004

**Acceptance Criteria**:

- [ ] Given a DfE policy user, when accessing the national dashboard, then FSM statistics are displayed by region, LA, school type, and demographic
- [ ] Given data refresh, when new data is processed, then dashboards update within 24 hours
- [ ] Given a data download request, when submitted, then data is exported in CSV/ODS format

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-007: API for National Food Strategy Dashboard (Project 005)

**Description**: The system must publish FSM uptake metrics via a versioned API for the National Food Strategy Dashboard.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given an authorised API consumer, when requesting FSM metrics, then data is returned in < 500ms
- [ ] Given weekly data refresh, when processed, then API data is updated within 24 hours
- [ ] Given API versioning, when a new version is released, then the previous version remains available for 6 months

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**:

- Portal page load time: < 2 seconds (95th percentile)
- Individual eligibility check (ECS): < 10 seconds
- Bulk eligibility matching (national cohort): < 48 hours per cycle
- Report generation: < 30 seconds

**Load Conditions**:

- Peak load: 5,000 concurrent users (term-start periods)
- Average load: 500 concurrent users
- Bulk processing: 6.5 million pupil records per matching cycle

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: System must achieve 99.9% uptime (citizen-facing service tier per ARC-000-PRIN-v1.0 Principle 16).

- Maximum planned downtime: 45 minutes/month
- Maximum unplanned downtime: 8.76 hours/year
- Critical availability periods: September (term start), January (spring census)

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: Maximum data loss = 15 minutes

**RTO**: Maximum downtime = 1 hour

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: Local authority users authenticate via their organisation's IdP federated through DfE Azure AD. Schools authenticate via DfE Sign-in. Parents authenticate via GOV.UK One Login.

**MFA**: Required for all local authority and DfE users. Encouraged for parent portal.

**Priority**: CRITICAL

---

#### NFR-SEC-2: Children's Data Protection

**Requirement**: All processing of children's personal data must comply with ICO Children's Code standards 1-15 and UK GDPR Article 8.

**Specific Controls**:

- Data minimisation: only collect data necessary for eligibility determination
- Purpose limitation: data used exclusively for FSM eligibility and Pupil Premium
- Enhanced access controls for children's records
- Anonymisation for analytics and reporting (no individual-level data in dashboards)
- Retention: pupil data retained only for Pupil Premium "Ever 6" tracking period plus 1 year

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance (mandatory). Parent-facing services must support multi-language content (top 10 community languages) and be usable by people with low digital literacy.

**Priority**: CRITICAL

---

## Integration Requirements

#### INT-001: HMRC Eligibility Checking Service (ECS)

**Purpose**: Verify FSM eligibility against HMRC tax credit and benefits records.

**Integration Type**: Real-time API (individual checks) + batch (bulk matching)

**Data Exchanged**:

- **To HMRC**: Pupil identifier, parent/carer details (name, DOB, NINO where available)
- **From HMRC**: Eligibility confirmation (eligible/not eligible), qualifying benefit type (anonymised)

**Authentication**: Mutual TLS, HMRC API key

**SLA**: Real-time: < 10 seconds; Batch: < 48 hours for 6.5M records

**Priority**: MUST_HAVE

---

#### INT-002: DWP Universal Credit API

**Purpose**: Verify FSM eligibility for families receiving Universal Credit with net earnings below threshold.

**Integration Type**: Real-time API + batch matching

**Data Exchanged**:

- **To DWP**: Parent/carer identifiers
- **From DWP**: UC eligibility confirmation (above/below threshold)

**Authentication**: Mutual TLS, DWP API gateway

**Priority**: MUST_HAVE

---

#### INT-003: GOV.UK Notify

**Purpose**: Send parent/carer notifications for auto-enrolment, opt-out confirmation, and eligibility changes.

**Priority**: MUST_HAVE

---

#### INT-004: GOV.UK One Login

**Purpose**: Parent/carer authentication for manual applications and opt-out management.

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Pupil Record

| Attribute | Type | Required | Description | Classification |
|-----------|------|----------|-------------|---------------|
| pupil_id | UUID | Yes | System identifier | OFFICIAL |
| upn | String(13) | Yes | Unique Pupil Number | OFFICIAL-SENSITIVE |
| first_name | String(100) | Yes | Pupil first name | OFFICIAL-SENSITIVE |
| surname | String(100) | Yes | Pupil surname | OFFICIAL-SENSITIVE |
| dob | Date | Yes | Date of birth | OFFICIAL-SENSITIVE |
| school_urn | String(6) | Yes | School URN | OFFICIAL |
| la_code | String(3) | Yes | Local authority code | OFFICIAL |
| fsm_eligible | Boolean | Yes | Current eligibility status | OFFICIAL-SENSITIVE |
| fsm_start_date | Date | No | Date eligibility started | OFFICIAL-SENSITIVE |
| ever6_flag | Boolean | Yes | Eligible at any point in last 6 years | OFFICIAL-SENSITIVE |

**Data Volume**: 6.5 million pupil records (England)

**Data Classification**: OFFICIAL-SENSITIVE (children's personal data)

**Data Retention**: Active records + 7 years post-leaving (Pupil Premium "Ever 6" + audit)

---

### Data Quality Requirements

**Data Accuracy**: Eligibility determination accuracy > 98%, validated by annual sample audit.

**Data Consistency**: Cross-referenced with School Census data (3 times/year) for reconciliation.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use DfE Sign-in service for school authentication.

**TC-2**: HMRC ECS API has a rate limit of 10,000 real-time checks per hour; bulk matching requires separate batch interface.

**TC-3**: Must deploy to DfE approved cloud environment.

---

### Business Constraints

**BC-1**: Auto-enrolment requires regulatory change (amendment to Education (Free School Lunches) Regulations). Timeline dependent on parliamentary schedule.

**BC-2**: Must be operational before autumn term start (September) for launch year.

**BC-3**: Budget capped at £8.5M over 3 years.

---

### Assumptions

**A-1**: HMRC and DWP will agree to expanded data sharing gateway for auto-enrolment (risk: legal challenge adds 12+ months).

**A-2**: Local authorities will adopt the platform if adequate training and support is provided.

**A-3**: Parents will not significantly opt out of auto-enrolment (estimated < 2% opt-out rate based on Scottish experience).

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| FSM eligibility gap | 11% (~215K children) | < 3% (~60K) | 18 months post-launch | ECS data vs registration |
| LA onboarding | 0/152 | 152/152 | 24 months post-launch | Platform adoption tracking |
| Pupil Premium accuracy | ~95% | > 99.5% | 12 months post-launch | Funding reconciliation |
| Admin cost reduction | Baseline TBD | 40% reduction | 24 months post-launch | LA cost surveys |

---

## Timeline and Milestones

| Milestone | Target Date | Dependencies |
|-----------|-------------|--------------|
| Discovery Complete | Q3 2026 | Budget approval |
| Alpha Assessment (GDS) | Q1 2027 | Regulatory change timeline confirmed |
| Private Beta (10 pilot LAs) | Q3 2027 | HMRC/DWP API agreements |
| Public Beta (all LAs) | Q1 2028 | Pilot evaluation |
| Live Service | September 2028 | GDS Live assessment |

---

## Budget

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Platform development | £3.5M | Eligibility engine, portal, APIs |
| HMRC/DWP integration | £1.5M | API development, testing, data matching |
| LA onboarding and training | £1.0M | 152 authorities, regional workshops |
| Security and DPIA | £0.5M | Pen testing, DPIA, ICO engagement |
| Infrastructure (3 years) | £1.5M | Cloud hosting |
| Contingency (15%) | £0.5M | Risk buffer |
| **Total** | **£8.5M** | Over 3 years |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| FSM | Free School Meals |
| UIFSM | Universal Infant Free School Meals (Reception, Y1, Y2) |
| ECS | Eligibility Checking Service |
| UPN | Unique Pupil Number |
| URN | Unique Reference Number (school identifier) |
| Pupil Premium | Additional school funding for disadvantaged pupils |
| Ever 6 | Pupil registered FSM at any point in the last 6 years |
| CRCA | Commissioners for Revenue and Customs Act 2005 |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Architecture Principles
- ARC-002-STKE-v1.0 -- School Meals Management System Stakeholder Analysis
- Education Act 1996 (FSM provisions)
- Education (Free School Lunches) Regulations
- ICO Children's Code (Age Appropriate Design Code)

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: School Meals Management System
**Model**: Claude Opus 4.6
