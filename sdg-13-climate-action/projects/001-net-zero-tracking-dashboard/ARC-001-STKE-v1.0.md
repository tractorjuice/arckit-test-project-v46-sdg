# Stakeholder Drivers & Goals Analysis: Net Zero Tracking Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Net Zero Tracking Dashboard (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Net Zero Tracking Dashboard Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Net Zero Dashboard Programme Board, DESNZ Digital, CDDO, CCC Secretariat |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Net Zero Tracking Dashboard, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The dashboard will provide a single, authoritative view of the UK's progress towards its legally binding net zero target by 2050 and interim carbon budget milestones.

### Key Findings

The strongest alignment exists between Ministerial desire for credible progress narratives and the CCC's demand for transparent, accurate tracking — both are served by a trusted, publicly accessible dashboard. The most significant tension is between DESNZ's need for rapid delivery to support upcoming COP commitments and the CCC's insistence on methodological rigour that takes time to validate. A secondary conflict exists between open data advocates who want granular, real-time data and industrial stakeholders concerned about commercially sensitive emissions disclosures.

### Critical Success Factors

- Achieve CCC endorsement of the dashboard methodology before public launch — CCC criticism at launch would be programme-ending
- Demonstrate alignment with NAEI data and DESNZ official statistics to avoid contradictory government figures
- Deliver a public-facing service that passes GDS service assessment and meets accessibility standards
- Provide actionable sectoral breakdowns (power, transport, buildings, industry, agriculture, LULUCF) that enable policy analysis
- Maintain data currency within 3 months of latest available NAEI and DESNZ energy statistics publications

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for transparent net zero tracking, but tensions between speed of delivery (political pressure for COP readiness), methodological rigour (CCC standards), data granularity (sectoral vs national), and commercial sensitivity (company-level vs aggregated data). Devolved administrations add complexity through separate emissions inventories and different net zero target dates.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Energy Security and Net Zero | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, COP preparedness |
| DESNZ Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Net Zero Dashboard | Programme Sponsor (DESNZ) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DESNZ Chief Statistician | Statistical methodology authority | HIGH | HIGH | Manage Closely — Methodology governance |
| DESNZ CDIO | Digital strategy and technology oversight | HIGH | MEDIUM | Keep Satisfied — Architecture governance |
| DESNZ SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DESNZ Climate Analysis Team | Emissions data producers | MEDIUM | HIGH | Keep Informed — Data requirements, methodology |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap |
| Delivery Manager | Delivery cadence, risks | MEDIUM | HIGH | Keep Informed — Stand-ups, risk escalation |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Climate Change Committee (CCC) | Statutory body | Independent scrutiny | HIGH | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| GDS Service Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Met Office | Partner agency | Climate projections data | MEDIUM | HIGH |
| DEFRA | Partner department | LULUCF and agriculture emissions | MEDIUM | HIGH |
| DfT | Partner department | Transport emissions data | MEDIUM | MEDIUM |
| Devolved Administrations | Scottish Gov, Welsh Gov, NI Executive | Separate inventories | MEDIUM | HIGH |
| Environmental NGOs | WWF, Greenpeace, Friends of the Earth | Public scrutiny and advocacy | LOW | HIGH |
| Academic researchers | Universities, research councils | Data consumers | LOW | HIGH |
| Energy-intensive industries | UK Steel, CBI, Make UK | Emissions data subjects | LOW | HIGH |
| Media | National press, specialist energy press | Public communication | LOW | HIGH |
| General public | Citizens | Dashboard users | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for dashboard outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end dashboard service and user outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation |
| Departmental Security Officer (DSO) | Day-to-day security coordination | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — DPIA sign-off |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed — Security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of     |
        |  * NAO              |    State (DESNZ)    |
        |  * DESNZ SIRO       |  * Permanent Sec.   |
        |  * CDDO             |  * SRO              |
 P      |  * DESNZ CDIO       |  * Chief Statistician|
 O      |  * SSRO / DSO       |  * CCC              |
 W      |                     |                     |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Met Office       |
        |                     |  * DEFRA            |
        |                     |  * DfT              |
        |                     |  * Devolved Admins  |
        |                     |  * NGOs             |
        |                     |  * Academics        |
        |                     |  * Industries       |
        |                     |  * Media            |
        |                     |  * General public   |
        |                     |  * GDS Assessment   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Credible Net Zero Narrative for International and Domestic Audiences

**Stakeholder**: Secretary of State for Energy Security and Net Zero

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Provide a credible, transparent, publicly accessible demonstration of UK progress towards net zero that supports the UK's international climate leadership position and enables positive responses to parliamentary questions, media scrutiny, and COP commitments.

**Context & Background**:
The UK's legally binding net zero by 2050 target under the Climate Change Act 2008 creates ongoing parliamentary and media scrutiny. The CCC's annual progress reports have repeatedly criticised the gap between ambition and delivery. The Secretary of State needs a trusted dashboard that shows genuine, verifiable progress — or at minimum, honest tracking that enables course-correction narratives. The UK's COP presidency legacy and ongoing UNFCCC engagement require demonstrable transparency.

**Driver Intensity**: CRITICAL

**Enablers**:

- CCC-endorsed methodology that pre-empts criticism
- Real-time or near-real-time data updates showing momentum
- Sectoral breakdowns enabling positive narratives in areas of genuine progress
- International comparability with other G7 nations' tracking approaches

**Blockers**:

- Contradictory figures from different government sources
- CCC public criticism of methodology or data gaps
- Dashboard showing worsening trajectory that becomes a media story
- Delays that miss COP or international reporting deadlines

**Related Stakeholders**: Permanent Secretary (accountability), CCC (independent scrutiny), NGOs (advocacy), Media (public communication)

---

### SD-2: Climate Change Committee — Methodologically Rigorous, Independent Tracking

**Stakeholder**: Climate Change Committee (CCC)

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure the dashboard uses methodologically sound, transparent approaches to emissions tracking that align with CCC's own analysis, enable independent verification, and do not create misleading impressions of progress. The CCC needs confidence that the dashboard will not undermine its statutory role in holding government to account.

**Context & Background**:
The CCC is the independent statutory body advising on emissions targets and reporting progress under the Climate Change Act 2008. The CCC produces its own annual progress reports with detailed sectoral analysis. A government dashboard that shows different figures, uses different methodologies, or presents a rosier picture than CCC analysis would create public confusion and undermine both the CCC's authority and the dashboard's credibility. The CCC needs to be confident in the dashboard's methodology before it can publicly endorse it.

**Driver Intensity**: CRITICAL

**Enablers**:

- Early CCC involvement in methodology design (co-creation, not post-hoc review)
- Transparent methodology documentation published alongside the dashboard
- Use of NAEI as the authoritative emissions data source (consistent with CCC practice)
- Clear communication of uncertainty bounds and data limitations
- Ability for CCC to reproduce dashboard figures from published source data

**Blockers**:

- Proprietary or opaque methodologies that CCC cannot independently verify
- Cherry-picking of metrics that show progress while omitting areas of failure
- Political interference in data presentation or methodology choices
- Dashboard launch without CCC pre-review

**Related Stakeholders**: Secretary of State (political sponsor), DESNZ Chief Statistician (methodology), Academic researchers (peer review)

---

### SD-3: DESNZ Chief Statistician — Alignment with Official Statistics Standards

**Stakeholder**: DESNZ Chief Statistician

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Ensure the dashboard complies with the UK Statistics Authority Code of Practice for Statistics, uses published DESNZ official statistics as the authoritative source, and does not create a parallel set of unofficial climate figures that could undermine the credibility of the official statistical outputs.

**Context & Background**:
DESNZ publishes official statistics on UK greenhouse gas emissions, energy consumption, and energy prices. These publications follow the UK Statistics Authority Code of Practice, with pre-announced publication dates, orderly release procedures, and quality assurance processes. A dashboard that re-processes or re-presents these figures without proper statistical governance risks breaching the Code of Practice and attracting criticism from the Office for Statistics Regulation (OSR).

**Driver Intensity**: HIGH

**Enablers**:

- Dashboard consumes published official statistics as its primary data source
- Clear distinction between official statistics and modelled/estimated data
- Orderly release alignment — dashboard updates coordinated with statistical publication dates
- Pre-publication access protocols that comply with Code of Practice

**Blockers**:

- Dashboard producing figures that contradict official statistics
- Real-time data feeds that create unofficial interim estimates
- Pressure to publish data before official statistical quality assurance is complete

**Related Stakeholders**: CCC (data consumer), Secretary of State (political use of data), Academic researchers (data quality expectations)

---

### SD-4: Environmental NGOs — Transparency and Accountability

**Stakeholder**: Environmental NGOs (WWF, Greenpeace, Friends of the Earth, Green Alliance, E3G)

**Driver Category**: CUSTOMER / COMPLIANCE

**Driver Statement**: Access granular, open, machine-readable emissions data that enables independent scrutiny of government climate action, identification of policy gaps, and evidence-based advocacy for stronger climate policies.

**Context & Background**:
Environmental NGOs are sophisticated data users who produce their own analyses of UK climate performance. They use NAEI data, DESNZ statistics, and CCC reports as primary sources. A government dashboard could either help (by making data more accessible and interoperable) or hinder (by presenting a curated view that obscures inconvenient trends). NGOs want open data, API access, and downloadable datasets — not just polished visualisations.

**Driver Intensity**: HIGH

**Enablers**:

- Open API providing access to underlying data (not just visualisations)
- Downloadable datasets in machine-readable formats (CSV, JSON)
- Sectoral and sub-sectoral granularity enabling detailed analysis
- Historical time series enabling trend analysis back to 1990 baseline
- Open Government Licence enabling unrestricted reuse

**Blockers**:

- Dashboard providing only visualisations with no underlying data access
- Data aggregated to a level that prevents meaningful scrutiny
- Paywalls or restrictive licensing on climate data
- Selective presentation of metrics that show favourable progress

**Related Stakeholders**: Academic researchers (similar data needs), Media (story identification), CCC (parallel analysis)

---

### SD-5: Devolved Administrations — Recognition of Separate Targets and Inventories

**Stakeholder**: Devolved Administrations (Scottish Government, Welsh Government, Northern Ireland Executive)

**Driver Category**: POLITICAL / OPERATIONAL

**Driver Statement**: Ensure the dashboard accurately represents devolved emissions inventories, acknowledges separate statutory targets (Scotland's net zero by 2045, Wales's 2050 target pathway), and does not present UK-wide aggregates that obscure devolved performance.

**Context & Background**:
Scotland has its own Climate Change (Emissions Reduction Targets) (Scotland) Act 2019 with a net zero target of 2045 — five years ahead of the UK target. Wales has its own carbon budget pathway under the Environment (Wales) Act 2016. Northern Ireland has the Climate Change Act (Northern Ireland) 2022. Each devolved administration has its own emissions inventory derived from the UK NAEI. A UK-wide dashboard must respect these separate statutory frameworks and data ownership while providing a coherent UK-wide picture.

**Driver Intensity**: MEDIUM

**Enablers**:

- Separate dashboard views for each nation with their own targets and baselines
- Use of devolved administration-approved inventory figures
- Joint governance with devolved statisticians on data presentation
- Acknowledgement of different policy levers and trajectories

**Blockers**:

- Dashboard showing only UK-wide figures that obscure devolved performance
- Methodology changes imposed without devolved administration consultation
- Attribution of UK-wide progress to Westminster policy when devolved actions contributed

**Related Stakeholders**: Secretary of State (UK-wide narrative), CCC (UK-wide and devolved analysis), DESNZ Chief Statistician (data methodology)

---

## Driver-to-Goal Mapping

### Goal G-1: Establish CCC-Endorsed Dashboard Methodology

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: DESNZ Chief Statistician

**Goal Statement**: Achieve formal CCC endorsement of the dashboard methodology within 6 months of project initiation, prior to public launch.

**Why This Matters**: Without CCC endorsement, the dashboard will face immediate public criticism from the body Parliament trusts most on climate issues, undermining political credibility (SD-1) and scientific integrity (SD-2).

**Success Metrics**:

- **Primary Metric**: Written CCC endorsement of methodology received
- **Secondary Metrics**:
  - Zero OSR concerns raised about statistical methodology
  - CCC able to reproduce dashboard figures from published NAEI data

**Baseline**: No integrated dashboard exists; CCC produces its own progress reports

**Target**: CCC-endorsed, publicly launched dashboard with transparent methodology documentation

**Measurement Method**: Formal CCC correspondence; OSR compliance assessment

**Dependencies**:

- CCC willingness to engage in co-creation (not just review)
- NAEI data availability and freshness

**Risks to Achievement**:

- CCC may be reluctant to endorse a government-produced dashboard (perceived independence risk)
- Methodology disagreements on scope 3 treatment or LULUCF accounting

---

### Goal G-2: Deliver Open, Machine-Readable Data Access

**Derived From Drivers**: SD-4, SD-2, SD-5

**Goal Owner**: Service Owner

**Goal Statement**: Provide open API and downloadable dataset access to all underlying dashboard data within 3 months of dashboard launch, published under the Open Government Licence.

**Why This Matters**: Open data access satisfies NGO scrutiny needs (SD-4), enables CCC independent verification (SD-2), and supports devolved administration use (SD-5).

**Success Metrics**:

- **Primary Metric**: Public API with documented endpoints serving all dashboard data
- **Secondary Metrics**:
  - 500+ API consumers within 6 months of launch
  - Datasets available in CSV, JSON, and machine-readable formats
  - All data under Open Government Licence

**Baseline**: DESNZ emissions statistics published as Excel/ODS downloads

**Target**: API-first data access with real-time endpoints and bulk download capability

**Measurement Method**: API analytics, download counts, user feedback

---

### Goal G-3: Achieve GDS Service Assessment Pass

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: SRO

**Goal Statement**: Pass GDS service assessment at Alpha and Beta gates within the programme timeline, demonstrating user-centred design, accessibility, and open standards compliance.

**Why This Matters**: GDS assessment pass is required for a public-facing government service and demonstrates credibility (SD-1) and compliance with government digital standards (SD-3).

**Success Metrics**:

- **Primary Metric**: GDS assessment passed at Beta
- **Secondary Metrics**:
  - WCAG 2.2 Level AA compliance verified
  - User research conducted with 5+ user groups
  - Service available on all major browsers and mobile devices

**Baseline**: No existing service

**Target**: GDS-assessed, accessible, performant public service

**Measurement Method**: GDS assessment panel decision; accessibility audit results

---

## Goal-to-Outcome Mapping

### Outcome O-1: Trusted National Net Zero Progress Tracking

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Establish the Net Zero Tracking Dashboard as the single, authoritative, publicly trusted source for UK net zero progress, referenced by CCC, media, and international bodies.

**Measurement Details**:

- **KPI**: Dashboard referenced as authoritative source in CCC annual progress report
- **Current Value**: No dashboard exists; multiple disparate data sources
- **Target Value**: CCC references dashboard in 2027 progress report
- **Measurement Frequency**: Annual
- **Data Source**: CCC progress report citations
- **Report Owner**: SRO

**Business Value**:

- **Strategic Impact**: UK credibility in international climate negotiations (COP, UNFCCC)
- **Operational Impact**: Reduced duplication of emissions tracking across government
- **Customer Impact**: Public and NGO access to transparent climate progress data

**Timeline**:

- **Phase 1 (Months 1-6)**: Methodology agreed with CCC, Alpha prototype
- **Phase 2 (Months 7-12)**: Beta launch with core functionality
- **Phase 3 (Months 13-18)**: Public launch, API release, open data
- **Sustainment (Year 2+)**: Continuous data updates, expanded coverage

**Stakeholder Benefits**:

- **Secretary of State**: Credible narrative for COP and parliamentary scrutiny
- **CCC**: Transparent data for independent progress assessment
- **NGOs**: Open data access for advocacy and analysis
- **Public**: Understanding of national climate progress

---

## Complete Traceability Matrix

### Stakeholder --> Driver --> Goal --> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Credible net zero narrative | G-1 | CCC-endorsed methodology | O-1 | Trusted tracking |
| Secretary of State | SD-1 | Credible net zero narrative | G-3 | GDS assessment pass | O-1 | Trusted tracking |
| CCC | SD-2 | Methodological rigour | G-1 | CCC-endorsed methodology | O-1 | Trusted tracking |
| CCC | SD-2 | Methodological rigour | G-2 | Open data access | O-1 | Trusted tracking |
| Chief Statistician | SD-3 | Official statistics alignment | G-1 | CCC-endorsed methodology | O-1 | Trusted tracking |
| NGOs | SD-4 | Transparency and accountability | G-2 | Open data access | O-1 | Trusted tracking |
| Devolved Admins | SD-5 | Separate targets recognition | G-2 | Open data access | O-1 | Trusted tracking |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Secretary of State wants rapid delivery for COP readiness (SD-1) but CCC requires thorough methodology validation that takes time (SD-2)
  - **Resolution Strategy**: Phase — launch with core national-level tracking first (achievable quickly), add sectoral and sub-national granularity iteratively. CCC engaged from day one on methodology.

- **Conflict 2**: NGOs want maximum data granularity including company-level emissions (SD-4) but industry stakeholders want commercially sensitive data aggregated (implicit driver)
  - **Resolution Strategy**: Compromise — publish sectoral and sub-sectoral aggregations openly; company-level data only where already publicly reported (e.g., EU ETS/UK ETS verified emissions).

**Synergies**:

- **Synergy 1**: CCC methodology endorsement (SD-2) directly enables the Secretary of State's credible narrative (SD-1) — one action satisfies both
- **Synergy 2**: Open data access (SD-4) enables CCC independent verification (SD-2) and devolved administration use (SD-5)

---

## Communication & Engagement Plan

### CCC Secretariat

**Primary Message**: We are building this dashboard with you, not for you — your methodology input is essential and your independence is respected.

**Key Talking Points**:

- Co-creation of methodology, not post-hoc review
- Dashboard will use NAEI as authoritative source, consistent with CCC practice
- CCC's statutory role and independence will be clearly communicated on the dashboard

**Communication Frequency**: Fortnightly during methodology development; monthly thereafter

**Preferred Channel**: Joint working group meetings, shared methodology documentation

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| CCC Secretariat | Produce own progress analysis from NAEI | Co-produce methodology, reference shared dashboard | MEDIUM | MEDIUM | Early engagement, co-creation approach |
| DESNZ Statisticians | Publish standalone statistical releases | Feed data to live dashboard alongside statistical releases | MEDIUM | MEDIUM | Clear workflow design, no additional burden |
| NGO Analysts | Manually download and process DESNZ Excel files | API access to structured, machine-readable data | LOW | LOW | Better tools, not a threat |
| Devolved Administrations | Separate emissions reporting with limited UK context | Integrated UK dashboard with devolved views | MEDIUM | MEDIUM | Joint governance, respect for separate targets |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: CCC Refuses to Endorse Methodology

**Related Stakeholders**: CCC, Secretary of State

**Risk Description**: CCC may decline to endorse the dashboard methodology due to disagreements on scope, methodology, or independence concerns, undermining the dashboard's credibility at launch.

**Impact on Goals**: G-1 (methodology endorsement) directly blocked; G-1 failure cascades to O-1 (trusted tracking)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Early CCC engagement through co-creation (not consultation); methodology peer review by independent academics; transparent documentation enabling CCC verification.

**Contingency Plan**: Launch with "methodology reviewed by CCC" rather than "endorsed by CCC"; publish CCC feedback transparently.

---

### Risk R-2: Contradictory Figures Between Dashboard and Official Statistics

**Related Stakeholders**: DESNZ Chief Statistician, CCC, Media

**Risk Description**: Dashboard may display figures that appear to contradict published DESNZ official statistics due to different temporal coverage, scope, or rounding, generating media stories about "government can't agree its own climate figures."

**Impact on Goals**: G-1 (methodology endorsement), O-1 (trusted tracking)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Dashboard consumes official statistics directly; clear provenance labelling; coordinated publication timing; pre-release reconciliation process.

**Contingency Plan**: Rapid communication protocol with DESNZ press office; technical explainer published for journalists.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Methodology approval | Chief Statistician | SRO | CCC, Devolved Admins | All stakeholders |
| Data source selection | Data Architect | Chief Statistician | CCC, Met Office, DEFRA | Product Manager |
| Feature prioritisation | Product Manager | Service Owner | User research panel | Delivery team |
| Budget approval | Finance Director | Permanent Secretary | HM Treasury | CDDO |
| Go/no-go for launch | SRO | Permanent Secretary | CCC, GDS Assessment | All stakeholders |
| API design and scope | Technical Lead | CDIO | Open data community, NGOs | Delivery team |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: SRO / Service Owner (scope, methodology, stakeholder conflicts)
3. **Level 3**: DESNZ Permanent Secretary (strategic direction, CCC relationship, Ministerial requests)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| CCC Secretariat | PENDING | | PENDING |
| Chief Statistician | PENDING | | PENDING |
| Service Owner | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Sponsor | | | |
| Service Owner | | | |
| Enterprise Architect | | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

#### Interview with CCC Secretariat Representative — PENDING

**Key Points**: To be conducted during Discovery phase

### Appendix B: References

- Architecture Principles: `projects/000-global/ARC-000-PRIN-v1.0.md`
- Climate Change Act 2008
- CCC Annual Progress Reports
- DESNZ Greenhouse Gas Emissions Statistics
- UK Statistics Authority Code of Practice

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Climate Change Act 2008 | Legislation | legislation.gov.uk | Net zero target, carbon budgets, CCC mandate | N/A — external reference |
| CCC 2025 Progress Report | Statutory report | theccc.org.uk | Latest progress assessment | N/A — external reference |
| NAEI | Data | naei.beis.gov.uk | UK emissions inventory | N/A — external reference |
| UK Statistics Authority Code of Practice | Standard | statisticsauthority.gov.uk | Official statistics requirements | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Net Zero Tracking Dashboard (Project 001)
**Model**: Claude Opus 4.6
