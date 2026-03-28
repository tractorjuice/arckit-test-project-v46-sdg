# Stakeholder Drivers & Goals Analysis: Water Quality Monitoring Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Water Quality Monitoring Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Quality Monitoring Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Environment Agency, Ofwat, Natural England |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Water Quality Monitoring Platform, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The Water Quality Monitoring Platform sits at the intersection of environmental regulation, public health, and commercial water industry operations. The dominant tension is between water company commercial interests (minimising reporting burden and regulatory exposure) and the public interest in transparent, real-time environmental data — a tension made acute by the ongoing sewage discharge crisis. The strongest alignment exists around improving data timeliness and accuracy, which serves regulatory enforcement (Environment Agency), public transparency (DEFRA), and operational efficiency (water companies) simultaneously. The most significant conflict is between the speed of data publication demanded by environmental campaigners and the data validation requirements of water companies who risk reputational damage from unverified or misleading preliminary data.

### Critical Success Factors

- Deliver real-time water quality data for all designated bathing waters by the 2027 bathing season
- Achieve Environment Act 2021 compliance for continuous water quality monitoring at storm overflow discharge points
- Integrate water company self-monitoring data with EA independent monitoring without data quality degradation
- Publish open data meeting 5-star open data standards on data.gov.uk and the DEFRA Data Services Platform
- Maintain public trust through transparent methodology and clear communication of data limitations

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for better water quality data and modernised monitoring infrastructure. Significant tensions between water companies (concerned about cost, premature data publication, and enforcement exposure), environmental campaigners (demanding maximum transparency and real-time publication), and the EA (balancing enforcement capability with collaborative relationships with water companies). DEFRA policy officials navigate between Ministerial desire for visible action and the practical complexity of environmental monitoring.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Secretary of State | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ lines |
| DEFRA Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Water Quality Programme | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA Chief Digital Information Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DEFRA Chief Scientific Adviser | Scientific integrity | HIGH | MEDIUM | Keep Satisfied — Methodology review, data quality assurance |
| DEFRA Water Quality Policy Director | Policy ownership | HIGH | HIGH | Manage Closely — Policy alignment, WFD compliance |
| DEFRA Data Services Platform Team | Data publication | MEDIUM | HIGH | Keep Informed — API design, data formats |
| DEFRA SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DEFRA Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Environment Agency CEO | Environment Agency | Delivery partner / Regulator | HIGH | HIGH |
| EA Director of Water Quality | Environment Agency | Operational lead | HIGH | HIGH |
| EA National Laboratory Service | Environment Agency | Reference laboratory | MEDIUM | HIGH |
| Ofwat CEO | Ofwat | Economic regulator | HIGH | HIGH |
| Natural England | Natural England | Conservation designations | MEDIUM | MEDIUM |
| Water UK / Water Companies | Industry body | Regulated data providers | HIGH | HIGH |
| Surfers Against Sewage | Campaign group | Public advocacy | MEDIUM | HIGH |
| Rivers Trust | Charity | Citizen science, conservation | LOW | HIGH |
| Angling Trust | Membership body | Recreational water users | LOW | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Met Office | Met Office | Rainfall and weather data | MEDIUM | MEDIUM |
| UK Health Security Agency | UKHSA | Public health advisories | MEDIUM | HIGH |
| Local authorities | Multiple | Bathing water management | LOW | HIGH |
| General public (swimmers, water users) | Citizens | Service users | LOW | HIGH |
| Academic researchers | Universities | Environmental science | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end water quality data service | HIGH / HIGH | Manage Closely — Regular service reviews |
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
| Cyber Security Lead | Operational cyber security, NIS Regulations | MEDIUM / HIGH | Keep Informed — IoT security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * DEFRA Sec of     |
        |  * CDDO             |    State (Minister)  |
        |  * DEFRA SIRO       |  * DEFRA Perm Sec   |
        |  * DEFRA Finance    |  * SRO              |
        |  * DEFRA Chief Sci  |  * CDIO (DEFRA)     |
 P      |    Adviser          |  * EA CEO           |
 O      |  * SSRO / DSO       |  * EA Water Quality |
 W      |                     |  * Ofwat CEO        |
 E      |                     |  * Water Policy Dir |
 R      |                     |  * Water Companies  |
        +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Academic         |  * General public   |
        |    researchers      |  * Surfers Against  |
        |                     |    Sewage            |
        |                     |  * Rivers Trust     |
        |                     |  * Angling Trust    |
        |                     |  * Local authorities|
        |                     |  * UKHSA            |
        |                     |  * Natural England  |
        |                     |  * EA Lab Service   |
        |                     |  * DEFRA Data Team  |
        |                     |  * Met Office       |
        |                     |  * Cyber Sec Lead   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Secretary of State — Visible Action on Water Quality Crisis

**Stakeholder**: DEFRA Secretary of State

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate decisive government action on the sewage discharge crisis through transparent, real-time water quality monitoring that rebuilds public trust in water environment management.

**Context & Background**:
The sewage discharge crisis has dominated environmental media coverage since 2022. Parliamentary questions on water quality outnumber any other DEFRA topic. The Environment Act 2021 introduced new duties on water companies for continuous monitoring of storm overflows, and the Storm Overflow Discharge Reduction Plan set legally binding targets. The Secretary of State needs a visible, data-driven platform that demonstrates these commitments are being delivered — not just in policy documents but in real, accessible public data.

**Driver Intensity**: CRITICAL

**Enablers**:
- Real-time public dashboard showing water quality status at bathing waters and storm overflows
- Clear, jargon-free presentation of monitoring data accessible to the general public
- Demonstrable increase in monitoring coverage (more sites, more parameters, more frequently)

**Blockers**:
- Water company resistance to real-time publication of self-monitoring data
- Technical complexity of deploying reliable sensors at thousands of storm overflow points
- Budget constraints from HM Treasury limiting pace of rollout

**Related Stakeholders**: DEFRA Permanent Secretary, EA CEO, Ofwat CEO, Surfers Against Sewage

---

### SD-2: Environment Agency — Regulatory Enforcement Capability

**Stakeholder**: EA Director of Water Quality

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Obtain accurate, timely, and legally admissible water quality data that supports regulatory enforcement actions against polluters and underpins Water Framework Directive reporting obligations.

**Context & Background**:
The Environment Agency's enforcement capability has been constrained by reliance on periodic manual sampling (typically 12-24 samples per year per site). This frequency cannot reliably detect intermittent pollution events. The EA's National Laboratory Service processes approximately 1 million samples per year but turnaround times of 5-15 days mean pollution events are often historical by the time results are available. The EA needs continuous, automated monitoring to detect events in real time and build evidence for prosecution.

**Driver Intensity**: CRITICAL

**Enablers**:
- Continuous automated monitoring at high-risk sites replacing periodic manual sampling
- Integration with EA's existing WIMS (Water Information Management System) database
- Chain-of-custody documentation meeting CPS evidence standards for prosecution cases
- Automated alerting when pollution thresholds are exceeded

**Blockers**:
- Sensor accuracy limitations for some parameters (phosphorus, specific pesticides)
- Legal challenge risk if automated sensor data is used for enforcement without laboratory confirmation
- Budget cuts to EA monitoring programmes reducing field staff for sensor maintenance

**Related Stakeholders**: EA National Laboratory Service, Water Companies, DEFRA Policy Director

---

### SD-3: Water Companies — Cost-Effective Compliance with Minimised Reputational Risk

**Stakeholder**: Water UK / Water Companies (collectively)

**Driver Category**: FINANCIAL / COMPLIANCE / RISK

**Driver Statement**: Meet Environment Act 2021 monitoring requirements at minimum cost while controlling the narrative around water quality data to avoid disproportionate reputational damage from preliminary or decontextualised data publication.

**Context & Background**:
Water companies face legally binding requirements to install continuous monitoring at all storm overflows by 2030 (with 100% coverage already achieved for Event Duration Monitors). The industry estimates the total monitoring programme cost at GBP 1.6 billion. Companies want to ensure monitoring data is presented in appropriate context — a storm overflow operating within its permitted conditions during heavy rainfall is not the same as an illegal discharge, but public perception often conflates the two. Companies also want to avoid a situation where real-time data is published before quality assurance, potentially triggering unwarranted enforcement action or public panic.

**Driver Intensity**: HIGH

**Enablers**:
- Standardised monitoring requirements (avoiding 11 different company approaches)
- Clear data quality flagging so preliminary data is distinguished from validated data
- Contextual information published alongside raw data (rainfall, permit conditions, upstream conditions)
- Reasonable data validation windows before publication (24-48 hours for non-urgent data)

**Blockers**:
- Pressure from campaigners for immediate real-time publication without validation windows
- Inconsistent regulatory expectations between EA and Ofwat
- Risk that open data enables hostile media stories without operational context

**Related Stakeholders**: Ofwat CEO, EA Director, Surfers Against Sewage, DEFRA Secretary of State

---

### SD-4: Ofwat — Robust Performance Data for Price Review and Enforcement

**Stakeholder**: Ofwat CEO

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Obtain standardised, auditable water company performance data that supports fair and evidence-based price review determinations and enforcement of licence conditions.

**Context & Background**:
Ofwat's price review process (PR29, covering 2030-2035) will set the prices water companies can charge customers and the investment programmes they must deliver. This process depends on accurate performance data — including environmental performance metrics like pollution incidents, bathing water quality, and storm overflow performance. Currently, Ofwat relies largely on water company self-reported data validated through annual assurance processes. A common monitoring platform with independent data collection would strengthen Ofwat's evidence base and reduce the risk of data gaming.

**Driver Intensity**: HIGH

**Enablers**:
- Independent data collection (not relying solely on water company self-reporting)
- Standardised performance metrics aligned with Ofwat methodology statements
- Automated data validation reducing the annual assurance burden
- Historical data enabling trend analysis across multiple price review periods

**Blockers**:
- Water company opposition to independent monitoring of their operational performance
- Methodological differences between Ofwat performance metrics and EA environmental monitoring
- Cost of maintaining parallel monitoring infrastructure

**Related Stakeholders**: Water Companies, EA Director, DEFRA Finance Director

---

### SD-5: Surfers Against Sewage / Environmental Campaign Groups — Maximum Transparency

**Stakeholder**: Surfers Against Sewage, Rivers Trust, Angling Trust (collectively)

**Driver Category**: STRATEGIC / CUSTOMER

**Driver Statement**: Achieve real-time, unrestricted public access to water quality data at every bathing water, river, and storm overflow discharge point in England, enabling citizen scrutiny of water company performance and evidence-based campaigning.

**Context & Background**:
Environmental campaign groups have driven much of the public and political momentum behind water quality monitoring improvements. Surfers Against Sewage's Safer Seas & Rivers Service already provides real-time sewage pollution alerts using water company Event Duration Monitor data and Met Office rainfall forecasts. These groups want the government platform to go further — more parameters, more locations, more frequent updates, and no data delay or filtering that could be perceived as protecting water company interests.

**Driver Intensity**: HIGH

**Enablers**:
- Real-time data publication (no validation delay for safety-critical parameters)
- Open API access enabling third-party applications and analysis
- Geographic coverage beyond designated bathing waters to include all rivers and coastal waters
- Historical data access enabling trend analysis and accountability

**Blockers**:
- Water company pressure for validation windows before publication
- DEFRA concerns about publishing data that may be misleading without expert context
- Technical limitations of sensor technology for some parameters of public interest

**Related Stakeholders**: General public, DEFRA Secretary of State, Water Companies, Media

---

### SD-6: UK Health Security Agency — Timely Public Health Risk Assessment

**Stakeholder**: UKHSA (UK Health Security Agency)

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Receive timely water quality data for designated bathing waters and recreational waters to inform public health risk assessments and issue appropriate advisories to protect human health.

**Context & Background**:
UKHSA (and previously PHE) provides public health advice on bathing water quality and waterborne disease risk. Current bathing water classification is based on the previous season's sampling data — a retrospective measure that does not protect swimmers from real-time contamination events. UKHSA needs timely data (ideally within hours) on faecal indicator organisms and other health-relevant parameters to issue same-day advisories.

**Driver Intensity**: MEDIUM

**Enablers**:
- Near-real-time faecal indicator organism data at bathing waters during the bathing season
- Automated alerting when health-relevant thresholds are exceeded
- Integration with UKHSA's existing health protection notification systems

**Blockers**:
- Sensor technology limitations for E. coli and intestinal enterococci (rapid methods exist but accuracy varies)
- Regulatory bathing water classification still based on traditional laboratory methods

**Related Stakeholders**: EA Director, Local authorities, General public

---

## Driver-to-Goal Mapping

### Goal G-1: Real-Time Bathing Water Quality Dashboard

**Derived From Drivers**: SD-1, SD-5, SD-6

**Goal Owner**: DEFRA Water Quality Policy Director

**Goal Statement**: Deploy real-time water quality monitoring at all 424 designated bathing waters in England, publishing data to a public dashboard within 15 minutes of collection, by the start of the 2027 bathing season.

**Why This Matters**: Satisfies Ministerial demand for visible action (SD-1), campaign group transparency requirements (SD-5), and UKHSA need for timely health data (SD-6). This is the most politically visible deliverable.

**Success Metrics**:
- **Primary Metric**: Number of designated bathing waters with real-time monitoring (target: 424)
- **Secondary Metrics**:
  - Data publication latency (target: < 15 minutes from collection)
  - Public dashboard availability (target: 99.9% during bathing season May-September)
  - Public satisfaction with information quality (target: 70%+ positive in user research)

**Baseline**: 85 bathing waters with near-real-time monitoring (EA pilot sites)
**Target**: 424 bathing waters with real-time monitoring
**Measurement Method**: Automated monitoring of sensor deployment register and data pipeline latency metrics

**Dependencies**:
- Sensor procurement and deployment programme funded and resourced
- Landowner access agreements for sensor installation at all 424 sites
- Communication infrastructure (cellular/LoRaWAN) available at all sites

**Risks to Achievement**:
- Sensor supply chain delays (global semiconductor shortages)
- Landowner access refusals at private bathing water sites
- Sensor reliability in coastal marine environments (salt corrosion, biofouling)

---

### Goal G-2: Storm Overflow Continuous Monitoring Integration

**Derived From Drivers**: SD-1, SD-2, SD-3, SD-4

**Goal Owner**: EA Director of Water Quality

**Goal Statement**: Integrate continuous monitoring data from all 15,000+ storm overflows in England into the platform, with validated data published within 24 hours, by December 2027.

**Why This Matters**: Delivers the Environment Act 2021 monitoring commitment (SD-1), provides EA with enforcement evidence (SD-2), standardises water company reporting (SD-3, SD-4).

**Success Metrics**:
- **Primary Metric**: Percentage of storm overflows with integrated continuous monitoring (target: 100%)
- **Secondary Metrics**:
  - Data validation turnaround (target: < 24 hours for routine, < 2 hours for pollution alerts)
  - Data quality score (target: > 95% of readings passing automated QA)

**Baseline**: Event Duration Monitor data from ~14,500 overflows (binary spill/no-spill only)
**Target**: Continuous flow and quality monitoring integrated from all 15,000+ overflows
**Measurement Method**: Automated tracking via platform ingestion metrics

---

### Goal G-3: WFD-Compliant Water Body Classification

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: EA Director of Water Quality

**Goal Statement**: Automate Water Framework Directive water body classification calculations using continuous monitoring data, reducing the classification cycle from 6 years to annual provisional assessments, by Q4 2027.

**Why This Matters**: Enables more responsive regulatory action (SD-2) and provides Ofwat with current environmental performance data for price reviews (SD-4).

**Success Metrics**:
- **Primary Metric**: Water bodies with automated provisional classification (target: all 4,864 surface water bodies in England)
- **Secondary Metrics**:
  - Classification accuracy vs manual assessment (target: > 95% concordance)
  - Time from data collection to provisional classification (target: < 30 days)

**Baseline**: Manual classification every 6 years based on periodic sampling
**Target**: Annual automated provisional classification for all surface water bodies
**Measurement Method**: Concordance study comparing automated vs manual classification

---

### Goal G-4: Open Data Publication to 5-Star Standard

**Derived From Drivers**: SD-1, SD-5, SD-3

**Goal Owner**: DEFRA Data Services Platform Team

**Goal Statement**: Publish all water quality monitoring data as open data at 5-star open data standard, with API access, bulk download, and machine-readable metadata, within 6 months of platform launch.

**Why This Matters**: Delivers the transparency commitment (SD-1, SD-5) while ensuring data is published with appropriate context and quality flags (SD-3).

**Success Metrics**:
- **Primary Metric**: Open data maturity score (target: 5-star)
- **Secondary Metrics**:
  - API adoption (target: 50+ third-party applications within 12 months)
  - Data download volume (target: 1 million+ downloads per year)
  - Data quality flag coverage (target: 100% of published data has quality status)

**Baseline**: Limited open data publication via EA data services (CSV downloads, no API)
**Target**: 5-star open data with RESTful API, GeoJSON, bulk download, and INSPIRE metadata
**Measurement Method**: Open Data Institute assessment, API usage analytics

---

## Goal-to-Outcome Mapping

### Outcome O-1: Improved Public Health Protection at Bathing Waters

**Supported Goals**: G-1, G-4

**Outcome Statement**: Reduce the number of bathing water-related illness incidents by 25% within 2 years of platform launch through real-time contamination alerts enabling swimmers to avoid polluted water.

**Measurement Details**:
- **KPI**: Reported waterborne illness cases linked to bathing water exposure
- **Current Value**: ~400 reported cases per year (UKHSA estimate, likely under-reported)
- **Target Value**: < 300 reported cases per year
- **Measurement Frequency**: Annual (bathing season aggregate)
- **Data Source**: UKHSA health protection surveillance
- **Report Owner**: UKHSA

**Business Value**:
- **Health Impact**: Reduced waterborne illness, reduced NHS treatment costs (est. GBP 2M/year)
- **Economic Impact**: Increased beach tourism revenue (est. GBP 15M/year) from improved confidence
- **Strategic Impact**: Demonstrates UK environmental governance leadership

**Stakeholder Benefits**:
- **DEFRA Secretary of State**: Demonstrable health outcome improvement for Parliamentary reporting
- **UKHSA**: Evidence-based advisory capability replacing retrospective classification
- **General public**: Informed decisions about where and when to swim safely

---

### Outcome O-2: Enhanced Environmental Regulatory Enforcement

**Supported Goals**: G-2, G-3

**Outcome Statement**: Increase successful pollution prosecution rate by 40% and reduce average investigation time by 60% through continuous evidence-quality monitoring data.

**Measurement Details**:
- **KPI**: Successful prosecution rate for water pollution offences
- **Current Value**: 62% conviction rate, average 18 months investigation time
- **Target Value**: 87% conviction rate, average 7 months investigation time
- **Measurement Frequency**: Annual
- **Data Source**: EA enforcement database, CPS case tracking
- **Report Owner**: EA Director of Water Quality

---

### Outcome O-3: Water Company Performance Transparency

**Supported Goals**: G-2, G-4

**Outcome Statement**: Achieve 90%+ public awareness of water quality data availability and 70%+ trust in the accuracy and independence of published water quality data within 3 years.

**Measurement Details**:
- **KPI**: Public trust in water quality data (survey-based)
- **Current Value**: 34% trust water company self-reported data (YouGov polling, 2025)
- **Target Value**: 70% trust independently monitored data
- **Measurement Frequency**: Annual survey
- **Data Source**: Commissioned public opinion research

---

## Complete Traceability Matrix

### Stakeholder -> Driver -> Goal -> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA Secretary of State | SD-1 | Visible action on water quality | G-1 | Real-time bathing water dashboard | O-1 | Public health protection |
| DEFRA Secretary of State | SD-1 | Visible action on water quality | G-4 | Open data publication | O-3 | Performance transparency |
| EA Director | SD-2 | Enforcement capability | G-2 | Storm overflow integration | O-2 | Enhanced enforcement |
| EA Director | SD-2 | Enforcement capability | G-3 | WFD classification | O-2 | Enhanced enforcement |
| Water Companies | SD-3 | Cost-effective compliance | G-2 | Storm overflow integration | O-3 | Performance transparency |
| Ofwat CEO | SD-4 | Performance data for price review | G-3 | WFD classification | O-2 | Enhanced enforcement |
| Campaign Groups | SD-5 | Maximum transparency | G-1 | Bathing water dashboard | O-1 | Public health protection |
| Campaign Groups | SD-5 | Maximum transparency | G-4 | Open data publication | O-3 | Performance transparency |
| UKHSA | SD-6 | Public health risk assessment | G-1 | Bathing water dashboard | O-1 | Public health protection |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Water Companies (SD-3) want 24-48 hour data validation windows before publication, but Campaign Groups (SD-5) demand immediate real-time publication without delays.
  - **Resolution Strategy**: Tiered publication — safety-critical parameters (E. coli, sewage indicators) published immediately with "preliminary" flag; full validated dataset published within 24 hours. Water companies can append contextual notes within 48 hours but cannot delay initial publication.

- **Conflict 2**: EA (SD-2) needs evidence-quality data meeting CPS prosecution standards, but the cost of achieving laboratory-grade accuracy with continuous sensors exceeds DEFRA's budget envelope.
  - **Resolution Strategy**: Hybrid approach — continuous sensors for screening and alerting, with automated triggering of confirmatory manual sampling when thresholds are exceeded. Sensor data used for intelligence-led enforcement targeting; laboratory data used for prosecution evidence.

- **Conflict 3**: Water Companies (SD-3) want standardised monitoring to avoid competitive disadvantage, but some companies have already invested heavily in proprietary monitoring systems they want to continue using.
  - **Resolution Strategy**: Define mandatory data standards and API specifications rather than mandating specific sensor hardware. Companies can use existing systems if they meet data quality and interoperability requirements.

**Synergies**:

- **Synergy 1**: DEFRA Secretary of State's visibility driver (SD-1) aligns with Campaign Groups' transparency driver (SD-5) — both are served by the public dashboard (G-1).
- **Synergy 2**: EA's enforcement capability (SD-2) and Ofwat's performance data needs (SD-4) are both served by storm overflow integration (G-2) — shared investment in monitoring infrastructure.

---

## Communication & Engagement Plan

### DEFRA Secretary of State

**Primary Message**: The platform will deliver the most comprehensive, transparent water quality monitoring system in Europe, demonstrating the UK's post-Brexit environmental governance commitment.

**Key Talking Points**:
- Real-time data at all 424 designated bathing waters by 2027 bathing season
- Open data publication enabling citizen scrutiny and third-party innovation
- Directly delivering Environment Act 2021 monitoring commitments

**Communication Frequency**: Monthly Ministerial briefing, PQ lines as needed
**Preferred Channel**: Written briefing with visual dashboard prototype

### Water Companies

**Primary Message**: A standardised platform reduces individual company monitoring costs, provides consistent methodology that supports fair regulatory comparison, and includes appropriate data quality flagging.

**Key Talking Points**:
- Common standards reduce the risk of inconsistent regulatory expectations
- Data quality flags protect against unfair interpretation of preliminary data
- Platform investment counts towards companies' environmental programme commitments

**Communication Frequency**: Quarterly industry forum, monthly technical working group
**Preferred Channel**: Industry working group, bilateral meetings with Water UK

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| EA field monitoring teams | Manual sampling, laboratory analysis | Sensor network management, data analysis | HIGH | MEDIUM | Reskilling programme, enhanced analytical role |
| Water companies | Self-reported data, annual assurance | Continuous monitored data, real-time publication | HIGH | HIGH | Industry working group, phased rollout, fair methodology |
| EA National Laboratory Service | Primary data source for water quality | Confirmatory role, quality assurance | MEDIUM | MEDIUM | Repositioned as quality assurance authority |
| General public | Limited, retrospective information | Real-time, accessible dashboards | HIGH | LOW | Public launch campaign, user research-informed design |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Water Company Non-Cooperation

**Related Stakeholders**: Water Companies, Ofwat, EA
**Risk Description**: Water companies may resist integration, delay data feeds, or challenge the platform's methodology to protect commercial interests.
**Impact on Goals**: G-2 (storm overflow integration), G-4 (open data)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Leverage Environment Act 2021 statutory powers to compel data provision; Ofwat to include platform cooperation in licence conditions.
**Contingency Plan**: EA independent monitoring to fill gaps if water company data is unavailable.

### Risk R-2: Public Backlash from Preliminary Data

**Related Stakeholders**: Water Companies, General public, Campaign Groups
**Risk Description**: Publication of preliminary unvalidated data could trigger public panic or unfair media coverage, undermining water company cooperation and platform credibility.
**Impact on Goals**: G-1, G-4
**Probability**: MEDIUM
**Impact**: MEDIUM
**Mitigation Strategy**: Clear data quality labelling, contextual information (rainfall, permit conditions), public communication strategy developed with water companies and campaign groups.

### Risk R-3: Campaign Group Criticism of Data Limitations

**Related Stakeholders**: Surfers Against Sewage, Rivers Trust
**Risk Description**: Campaign groups may criticise the platform for not being transparent enough, too slow to publish, or not covering enough parameters/locations.
**Impact on Goals**: G-1, G-4
**Probability**: HIGH
**Impact**: MEDIUM
**Mitigation Strategy**: Early engagement with campaign groups on design, phased roadmap with ambitious but achievable targets, open API enabling third-party innovation.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DEFRA Finance Director | DEFRA Permanent Secretary | HM Treasury, CDDO | All stakeholders |
| Monitoring methodology | EA Director of Water Quality | DEFRA Chief Scientific Adviser | Water Companies, UKHSA | Campaign groups, public |
| Data publication policy | DEFRA Policy Director | DEFRA Secretary of State | EA, Ofwat, Water Companies | Campaign groups, public |
| Architecture decisions | DEFRA CDIO | SRO | EA Digital, Cyber Security | Vendors |
| Go/No-go for go-live | SRO | DEFRA Permanent Secretary | All stakeholders | All |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, cross-stakeholder conflicts)
3. **Level 3**: SRO (strategic direction, major conflicts, Ministerial escalation)

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| DEFRA Water Quality Policy Director | | | |
| EA Director of Water Quality | | | |
| Enterprise Architect | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environment Act 2021 | Legislation | legislation.gov.uk | Storm overflow monitoring duties | N/A — external reference |
| Storm Overflow Discharge Reduction Plan | Policy | GOV.UK | Monitoring targets and timelines | N/A — external reference |
| Water Framework Directive | Retained EU Law | legislation.gov.uk | Water body classification methodology | N/A — external reference |
| 25 Year Environment Plan | Policy | GOV.UK | Clean water commitments | N/A — external reference |
| Bathing Water Regulations 2013 | Legislation | legislation.gov.uk | Bathing water quality standards | N/A — external reference |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | SDG 6 governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Quality Monitoring Platform (Project 001)
**AI Model**: Claude Opus 4.6 (1M context)
