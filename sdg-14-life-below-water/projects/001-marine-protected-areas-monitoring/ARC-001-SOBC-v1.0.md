# Strategic Outline Business Case (SOBC): Marine Protected Areas Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Marine Protected Areas Monitoring (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Marine Protected Areas Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MPA Programme Board, DEFRA Finance, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case establishes the strategic justification for investment in a Marine Protected Areas Monitoring platform. It follows HM Treasury Green Book guidance and supports the DEFRA Spending Review submission for marine conservation technology investment.

---

## Executive Summary

**Purpose**: The UK has designated 178 Marine Protected Areas covering over 38% of UK waters, yet lacks a comprehensive digital monitoring capability to assess their condition, enforce protections, and report against international obligations. This SOBC makes the case for investing in a unified MPA surveillance platform.

**Problem Statement**: MPA condition assessment is fragmented across five agencies, relies on periodic in-situ surveys with multi-year gaps, and cannot detect or deter illegal activity in real time. The UK risks non-compliance with OSPAR Convention obligations and cannot demonstrate progress against the 25 Year Environment Plan marine targets.

**Proposed Solution**: A cloud-hosted digital platform integrating satellite remote sensing, acoustic survey data, vessel tracking (VMS/AIS), dive survey records, and citizen science observations to provide near-real-time MPA condition monitoring, automated reporting, and enforcement support.

**Strategic Fit**: Directly supports the 25 Year Environment Plan target for a well-managed, ecologically coherent MPA network; the Fisheries Act 2020 sustainability objectives; OSPAR Convention obligations; and the UK's commitment to the Global Biodiversity Framework 30x30 target.

**Investment Required**: GBP 8.2M over 3 years

- Capital: GBP 5.5M
- Operational (3 years): GBP 2.7M

**Expected Benefits**: GBP 14.8M over 5 years

- Reporting efficiency: GBP 2.4M
- Survey optimisation: GBP 3.6M
- Enforcement effectiveness: GBP 1.8M
- Avoided compliance penalties: GBP 4.0M
- Ecosystem service value protection: GBP 3.0M

**Return on Investment**:

- NPV: GBP 4.1M (discounted at 3.5%)
- Payback Period: 28 months
- ROI: 80%

**Recommended Option**: Option 2: Integrated Monitoring Platform

**Key Risks**:

1. Scientific community rejects automated assessment methodology — mitigated by JNCC co-design and phased validation
2. VMS data access delayed by MMO data sharing negotiations — mitigated by parallel AIS integration
3. Fishing industry legal challenge to evidence-based restriction — mitigated by early NFFO engagement and transparency

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK's international reporting obligations are legally binding and reputational failure is not an option. The investment is modest relative to the value of marine ecosystem services protected (estimated at GBP 47 billion per annum for UK waters). The platform enables evidence-based marine management that benefits both conservation and sustainable fishing.

**Next Steps if Approved**:

1. Secure DEFRA SRO and Finance Director approval: April 2026
2. Detailed requirements and architecture design: Q2 2026
3. Alpha development and GDS assessment: Q3 2026
4. Beta with JNCC validation programme: Q4 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The UK has progressively designated 178 Marine Protected Areas since 2009, covering Marine Conservation Zones, Special Areas of Conservation, Special Protection Areas, and the recently announced Highly Protected Marine Areas. However, the monitoring infrastructure has not kept pace with designation ambition. MPA condition assessment data is held in fragmented databases across JNCC, Natural England, Cefas, NRW, and NatureScot, with no unified view of the MPA network's ecological health.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DEFRA Minister | SD-1 | Cannot demonstrate MPA progress to Parliament | Reputational and political risk | CRITICAL |
| JNCC | SD-2 | Fragmented data prevents network-level assessment | OSPAR non-compliance risk | CRITICAL |
| Natural England | SD-3 | 65% of MCZs lack current condition assessment | Management decisions based on outdated evidence | HIGH |
| MMO | SD-5 | VMS data not overlaid on MPA boundaries | Infringements undetected for hours | HIGH |
| NFFO | SD-4 | Assessment methodology not transparent | Industry distrust of evidence base | HIGH |

**Consequences of Inaction**:

- OSPAR Convention non-compliance: UK unable to report MPA condition at the 2027 Quality Status Report, risking formal Convention process and reputational damage
- 25 Year Environment Plan failure: Unable to demonstrate "well-managed MPA network" target by 2030
- Enforcement gap widens: Without real-time monitoring, illegal fishing in MPAs continues to degrade protected features
- Survey budget inefficiency: GBP 4M annual survey spend not optimised — sites surveyed on schedule rather than evidence need
- International credibility: UK's post-Brexit claim to be a global ocean conservation leader undermined by inability to monitor its own MPAs

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: This business case is informed by stakeholder analysis documented in `ARC-001-STKE-v1.0`.

**Primary Drivers**:

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | DEFRA Minister | POLITICAL | Demonstrate MPA progress to Parliament | 25 Year Environment Plan delivery |
| SD-2 | JNCC | COMPLIANCE | OSPAR Convention reporting obligations | International treaty compliance |
| SD-3 | Natural England | OPERATIONAL | Evidence-based MCZ management | Effective site protection |
| SD-5 | MMO | OPERATIONAL | Real-time MPA enforcement | Regulatory effectiveness |
| SD-4 | NFFO | FINANCIAL | Transparent evidence for management decisions | Industry trust and compliance |

**Strategic Alignment**:

- **25 Year Environment Plan**: Target 4.1 — "A well-managed, ecologically coherent network of Marine Protected Areas"
- **Fisheries Act 2020**: Section 1 — Sustainability objective requiring science-based fisheries management
- **OSPAR Convention**: Articles 6-10 — Monitoring and assessment of the marine environment
- **UK Marine Strategy Part Two**: Commitment to monitoring programmes for GES indicators
- **Global Biodiversity Framework**: 30x30 target — protect 30% of ocean by 2030 (UK claims ~38% but must demonstrate effective management)
- **Blue Belt Programme**: Extension of monitoring approach to UK Overseas Territories

### A1.3 Stakeholder Goals

**Goals Addressed** (from ARC-001-STKE-v1.0):

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | JNCC/Minister | MPA sites with current condition assessment | 35% (62 sites) | 90% (160 sites) | 24 months |
| G-2 | MMO | MPA infringement detection time | >2 hours | <15 minutes | 9 months |
| G-3 | JNCC | OSPAR report preparation time | 6 months | 2 weeks | 12 months |
| G-4 | MCS/NFFO | Open datasets published | 5 | 50+ | 18 months |

### A1.4 Scope

**In Scope**:

- MPA condition assessment data platform (ingest, store, process, visualise, report)
- Satellite and remote sensing data integration
- VMS/AIS vessel tracking integration for enforcement
- Citizen science data pathway
- OSPAR/MSFD automated reporting
- Public-facing MPA dashboard
- Mobile field access for officers

**Out of Scope** (for this phase):

- Fisheries quota management (Project 002)
- Marine pollution monitoring (Project 003)
- Coastal erosion monitoring (Project 004)
- Marine spatial planning tool
- Survey vessel scheduling and logistics
- Direct enforcement case management (MMO existing system)

**Dependencies**:

- **Internal**: DEFRA Cloud Platform provisioning, DEFRA Identity integration
- **External**: MMO VMS data feed access, UKHO bathymetric data licence, Copernicus satellite data service continuity
- **Technical**: JNCC condition assessment methodology approval for automated application

### A1.5 Why Now?

**Urgency Factors**:

- OSPAR Quality Status Report 2027 preparation begins Q3 2026 — UK must have improved data or face reporting gaps
- Global Biodiversity Framework 30x30 commitment requires demonstrable effective management, not just designation
- Highly Protected Marine Areas (HPMAs) announced 2023 require enhanced monitoring before designation
- Blue Belt Programme expanding to additional Overseas Territories — monitoring approach must be scalable
- Fisheries Management Plans under the Fisheries Act 2020 require MPA condition data as input

**Opportunity Cost of Delay**:

- GBP 400K/year continued manual OSPAR reporting costs
- GBP 800K/year survey budget inefficiency (sites surveyed on schedule not evidence need)
- Unmeasured enforcement losses from undetected MPA infringements
- Reputational cost of unable to report at OSPAR 2027

**Window of Opportunity**:

- DEFRA Spending Review allocation includes provision for marine digital transformation
- Copernicus Sentinel satellite constellation provides free, regular coverage of UK waters
- Cloud computing costs continue to decrease, making satellite data processing affordable
- Post-Brexit: UK can design monitoring to UK needs rather than EU-prescribed methods

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Scientific Credibility**: Data quality meets OSPAR peer-review standards
   - **Measure**: JNCC Scientific Advisory Committee endorsement
   - **Threshold**: Methodology approved before Beta launch

2. **Operational Adoption**: Natural England and MMO staff actively use the platform
   - **Measure**: Monthly active users
   - **Threshold**: >80% of target user population within 6 months of launch

3. **Data Integration**: Multiple data sources successfully integrated
   - **Measure**: Number of active data feeds
   - **Threshold**: Minimum 5 data sources operational at launch (satellite, acoustic, dive survey, VMS, citizen science)

4. **Reporting Automation**: OSPAR report generation substantially automated
   - **Measure**: Manual effort for OSPAR data preparation
   - **Threshold**: <2 weeks (from 6 months baseline)

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current fragmented monitoring approach across JNCC, Natural England, Cefas, NRW, and NatureScot.

**Costs** (5-year):

- Capital: GBP 0
- Operational: GBP 12.5M (continued survey programme, manual reporting, enforcement patrols)
- Total: GBP 12.5M

**Benefits**: GBP 0 (no improvement)

**Pros**:

- No upfront investment required
- No implementation risk
- No change management burden on scientific staff

**Cons**:

- OSPAR non-compliance risk escalates each reporting cycle
- 65% of MCZs remain without current condition assessment
- MPA enforcement capability does not improve
- Survey budget continues to be allocated without evidence-based prioritisation
- Unable to demonstrate 25 Year Environment Plan marine targets

**Risks**:

- OSPAR Convention process: reputational damage and potential formal proceedings
- Environmental degradation: unmonitored MPAs may be losing protected features undetected
- Political risk: media and NGO criticism of "paper parks"

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable risk of international treaty non-compliance and environmental harm.

---

### Option 1: Enhanced Manual Process

**Description**: Improve existing processes by standardising data formats, creating a shared database, and increasing survey frequency, without building a new digital platform.

**Scope**:

- Shared PostgreSQL/PostGIS database hosted on DEFRA infrastructure
- Standardised data submission templates for all agencies
- Manual VMS data review process with MPA boundary checking scripts
- Increased survey vessel time allocation

**Costs** (5-year) - ROM (+-40%):

- Capital: GBP 1.2M (database, data migration, training)
- Operational: GBP 14.0M over 5 years (increased survey costs, additional staff)
- Total 5-year TCO: GBP 15.2M

**Benefits** (5-year):

- Reporting efficiency: GBP 0.6M
- Improved data access: GBP 0.4M
- Total: GBP 1.0M

**Net Benefit**: GBP -14.2M

**Pros**:

- Lower upfront investment
- Minimal change management
- Uses familiar tools and processes

**Cons**:

- Does not address satellite/remote sensing integration
- No real-time enforcement capability
- Survey costs increase significantly to improve coverage
- Manual reporting remains labour-intensive
- Does not scale to Blue Belt Programme requirements

**Stakeholder Impact**:

- Minister Goal G-1: Partially met (50% coverage achievable with increased survey budget)
- MMO Goal G-2: Not met (manual VMS review, detection time remains >1 hour)
- JNCC Goal G-3: Partially met (reporting time reduced to 2 months, not 2 weeks)
- MCS/NFFO Goal G-4: Not met (no API access, limited open data)

**Stakeholder Goals Met**: 25%

---

### Option 2: Integrated Monitoring Platform (RECOMMENDED)

**Description**: Cloud-hosted digital platform integrating satellite remote sensing, acoustic survey data, vessel tracking, dive survey records, and citizen science observations, with automated condition assessment, enforcement alerts, and OSPAR reporting.

**Scope**:

- Cloud-native platform on DEFRA AWS with geospatial data services
- Satellite data processing pipeline (Sentinel-2, Sentinel-1)
- VMS/AIS integration with automated MPA boundary alerting
- Condition assessment engine with JNCC-approved methodology
- Interactive map viewer with condition dashboard
- Mobile field access with offline capability
- Open data API and MEDIN metadata publication
- OSPAR/MSFD report generator

**Costs** (5-year) - ROM (+-30%):

- Capital: GBP 5.5M
  - Platform development: GBP 3.0M
  - Data integration and migration: GBP 0.8M
  - Satellite processing infrastructure: GBP 0.7M
  - Security accreditation and testing: GBP 0.4M
  - Training and change management: GBP 0.3M
  - Contingency (10%): GBP 0.3M
- Operational: GBP 2.7M over 3 years (GBP 4.5M over 5 years)
  - Cloud hosting: GBP 0.4M/year
  - Support and maintenance: GBP 0.3M/year
  - Data feed licences (AIS provider): GBP 0.1M/year
  - Ongoing development: GBP 0.1M/year
- Total 5-year TCO: GBP 10.0M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Reporting efficiency (OSPAR, MSFD) | JNCC G-3 | FINANCIAL | GBP 0.1M | GBP 0.5M | GBP 0.6M | GBP 0.6M | GBP 0.6M | GBP 2.4M |
| B-002 | Survey optimisation (evidence-based prioritisation) | NE G-1 | FINANCIAL | GBP 0.2M | GBP 0.8M | GBP 0.8M | GBP 0.9M | GBP 0.9M | GBP 3.6M |
| B-003 | Enforcement effectiveness (infringement detection) | MMO G-2 | OPERATIONAL | GBP 0.1M | GBP 0.3M | GBP 0.4M | GBP 0.5M | GBP 0.5M | GBP 1.8M |
| B-004 | Avoided OSPAR compliance risk and penalties | JNCC G-3 | RISK | GBP 0.0M | GBP 0.5M | GBP 1.0M | GBP 1.0M | GBP 1.5M | GBP 4.0M |
| B-005 | Ecosystem service value protection (avoided degradation) | Minister G-1 | STRATEGIC | GBP 0.0M | GBP 0.5M | GBP 0.5M | GBP 1.0M | GBP 1.0M | GBP 3.0M |
| **Total** | | | | **GBP 0.4M** | **GBP 2.6M** | **GBP 3.3M** | **GBP 4.0M** | **GBP 4.5M** | **GBP 14.8M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 12.9M
- Total Costs PV: GBP 8.8M
- **NPV: GBP 4.1M**

**Return on Investment**:

- **ROI: 80%** over 5 years
- **Payback Period: 28 months**

**Pros**:

- 90% of stakeholder goals met
- Positive NPV of GBP 4.1M
- Scalable to Blue Belt Programme and future MPA designations
- Enables evidence-based marine management
- Supports open data and transparency commitments
- Modern architecture attracts and retains digital talent

**Cons**:

- Higher upfront investment than Option 1
- 18-month full implementation timeline
- Scientific methodology validation required in parallel
- Change management across multiple agencies

**Stakeholder Impact**:

- Minister Goal G-1: Met (90% coverage, near-real-time condition data)
- MMO Goal G-2: Met (<15 minute detection for VMS-equipped vessels)
- JNCC Goal G-3: Met (2 weeks OSPAR prep, automated report generation)
- MCS/NFFO Goal G-4: Met (50+ open datasets, API access)

**Stakeholder Goals Met**: 90%

---

### Option 3: Comprehensive Marine Intelligence Platform

**Description**: Full marine intelligence platform incorporating AI-driven predictive analytics, autonomous underwater vehicle (AUV) integration, advanced machine learning for species identification from imagery, and real-time 3D habitat modelling.

**Scope**:

- All of Option 2 plus:
- AI/ML species identification from underwater imagery and video
- AUV mission planning and data integration
- Predictive habitat condition modelling
- Real-time 3D seabed visualisation
- Integration with international MPA networks (OSPAR, Mediterranean, Antarctic)

**Costs** (5-year) - ROM (+-40%):

- Capital: GBP 14.0M
- Operational: GBP 8.0M over 5 years
- Total 5-year TCO: GBP 22.0M

**Benefits** (5-year): GBP 18.5M (marginally higher than Option 2 due to improved species ID automation)

**Net Benefit**: GBP -3.5M (diminishing returns on additional investment)

**Pros**:

- 100% of stakeholder goals met with capability exceeding requirements
- Future-proofed for 10+ years
- World-leading marine monitoring capability
- AI automation reduces long-term operational costs

**Cons**:

- GBP 14M capital investment is difficult to justify at SOBC stage
- AI/ML models for marine species identification not yet proven at scale
- AUV technology still maturing for routine monitoring
- Significantly higher implementation risk
- 30-month implementation timeline

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject at SOBC stage** — Scope and risk disproportionate. Elements (AI species ID, AUV integration) could be pursued in future phases once Option 2 is established.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 5-Year TCO | GBP 12.5M | GBP 15.2M | GBP 10.0M | GBP 22.0M |
| 5-Year Benefits | GBP 0 | GBP 1.0M | GBP 14.8M | GBP 18.5M |
| NPV | -GBP 12.5M | -GBP 14.2M | GBP 4.1M | -GBP 3.5M |
| Stakeholder Goals Met | 0% | 25% | 90% | 100% |
| Implementation Risk | None | Low | Medium | High |
| OSPAR Compliance | No | Partial | Yes | Yes |
| Scalability | None | Low | High | Very High |

**Recommended Option**: **Option 2 — Integrated Monitoring Platform**

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Approach**: Mixed procurement leveraging existing DEFRA framework agreements and G-Cloud for specialist components.

**Key Procurement Elements**:

| Component | Procurement Route | Estimated Value | Timeline |
|-----------|------------------|-----------------|----------|
| Platform development | DEFRA Digital Outcomes and Specialists 6 | GBP 3.0M | Q2 2026 |
| Cloud hosting | AWS DEFRA Enterprise Agreement | GBP 2.0M (5-year) | Existing |
| Satellite data processing | G-Cloud 14 | GBP 0.7M | Q2 2026 |
| AIS data feed | Direct award (specialist market) | GBP 0.5M (5-year) | Q2 2026 |
| Security testing | Crown Commercial Service Cyber Security | GBP 0.4M | Q3 2026 |

**Insourcing Strategy**: Build internal DEFRA capability for ongoing platform management, reducing supplier dependency post-delivery. Target 70% insourced operation by Year 2.

---

# PART D: FINANCIAL CASE

## D1. Cost Summary

| Category | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|----------|--------|--------|--------|--------|--------|-------|
| Capital | GBP 3.5M | GBP 2.0M | GBP 0.0M | GBP 0.0M | GBP 0.0M | GBP 5.5M |
| Operational | GBP 0.5M | GBP 0.9M | GBP 0.9M | GBP 0.9M | GBP 0.9M | GBP 4.1M* |
| **Total** | **GBP 4.0M** | **GBP 2.9M** | **GBP 0.9M** | **GBP 0.9M** | **GBP 0.9M** | **GBP 9.6M** |

*Note: Operational costs shown for full 5-year period; SOBC investment case covers 3-year capital plus 5-year operational.

## D2. Funding Source

- DEFRA Spending Review 2025 allocation for marine digital transformation
- Blue Belt Programme co-funding for Overseas Territory scalability (potential GBP 0.5M contribution)

## D3. Affordability Assessment

The investment falls within DEFRA's delegated authority for technology programmes. HM Treasury approval is not required at SOBC stage but will be sought for OBC if capital exceeds GBP 5M single-year threshold.

---

# PART E: MANAGEMENT CASE

## E1. Programme Governance

| Role | Person/Body | Responsibility |
|------|-------------|---------------|
| SRO | DEFRA Director of Marine | Overall accountability |
| Programme Board | SRO + JNCC + NE + MMO + DEFRA Digital | Strategic decisions |
| Scientific Advisory Board | JNCC-chaired with Cefas, academic experts | Methodology governance |
| Product Owner | DEFRA Digital | Feature prioritisation |
| Delivery Manager | DEFRA Digital | Delivery cadence |
| Industry Advisory Group | NFFO, IFCAs | Industry engagement |

## E2. Delivery Approach

**Methodology**: Agile (Scrum) within GDS service design framework

**Key Milestones**:

| Milestone | Date | Gate |
|-----------|------|------|
| Discovery complete | June 2026 | DEFRA Assurance Review |
| Alpha complete / GDS Alpha assessment | September 2026 | GDS Assessment |
| Beta launch (private beta with JNCC/NE) | January 2027 | Programme Board |
| Public beta / GDS Beta assessment | April 2027 | GDS Assessment |
| Live service | July 2027 | Programme Board |
| OSPAR 2027 report supported by platform | September 2027 | OSPAR deadline |

## E3. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Scientific methodology rejection | MEDIUM | HIGH | JNCC co-design from Discovery, phased validation | JNCC Director |
| VMS data access delay | MEDIUM | MEDIUM | Parallel AIS integration, DEFRA board escalation | SRO |
| Cloud cost overrun (satellite processing) | LOW | MEDIUM | Serverless architecture, data tiering, cost alerts | Technical Lead |
| Industry legal challenge | LOW | HIGH | NFFO advisory group, open methodology, legal review | SRO |
| Multi-agency adoption resistance | MEDIUM | MEDIUM | Change management programme, co-design workshops | Service Owner |
| Cybersecurity incident on VMS data | LOW | HIGH | OFFICIAL-SENSITIVE controls, pen testing, CAF compliance | DEFRA CISO |

## E4. Benefits Realisation

| Benefit | Measure | Baseline | Target | Owner | Tracking Frequency |
|---------|---------|----------|--------|-------|--------------------|
| OSPAR reporting automation | Preparation time | 6 months | 2 weeks | JNCC | Per reporting cycle |
| Survey optimisation | Budget efficiency ratio | 40% evidence-targeted | 85% evidence-targeted | Natural England | Annually |
| Enforcement detection | Mean detection time | >2 hours | <15 minutes | MMO | Monthly |
| MPA coverage | Sites with current assessment | 35% | 90% | JNCC | Quarterly |
| Open data publication | Published datasets | 5 | 50+ | Data Manager | Quarterly |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Green Book | Guidance | HMT | Appraisal and evaluation methodology | gov.uk |
| Marine and Coastal Access Act 2009 | Legislation | UK Parliament | MCZ designation framework | legislation.gov.uk |
| Fisheries Act 2020 | Legislation | UK Parliament | Sustainability objectives | legislation.gov.uk |
| OSPAR Convention | Treaty | OSPAR | Monitoring obligations | ospar.org |
| 25 Year Environment Plan | Policy | HMG | Marine targets | gov.uk |
| Blue Belt Programme | Policy | DEFRA/FCDO | Overseas Territory MPA management | gov.uk |
| UK Marine Strategy Part Two | Policy | DEFRA | Monitoring programmes | gov.uk |
| ARC-001-STKE-v1.0 | Architecture | SDG 14 Programme | Stakeholder drivers and goals | Local |
| ARC-001-REQ-v1.0 | Architecture | SDG 14 Programme | Requirements specification | Local |
| ARC-000-PRIN-v1.0 | Architecture | SDG 14 Programme | Architecture principles | Local |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Marine Protected Areas Monitoring
**Model**: Claude Opus 4.6
