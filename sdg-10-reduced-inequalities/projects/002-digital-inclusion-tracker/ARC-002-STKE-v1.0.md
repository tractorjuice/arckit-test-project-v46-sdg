# Stakeholder Drivers & Goals Analysis: Digital Inclusion Tracker

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Digital Inclusion Tracker (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Digital Inclusion Tracker, DSIT |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DSIT Digital Inclusion Team, CDDO, Ofcom, Good Things Foundation |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Digital Inclusion Tracker, their underlying drivers, how these manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Digital Inclusion Tracker faces a fundamental measurement challenge: the most digitally excluded populations are, by definition, the hardest to measure digitally. DSIT wants a comprehensive platform that integrates Lloyds Bank Consumer Digital Index data, Ofcom Connected Nations data, ONS survey data, and local authority digital skills programme outcomes into a unified view of digital exclusion across the UK. The primary tension is between Ofcom's infrastructure-focused view of digital inclusion (connectivity, coverage, speed) and the voluntary sector's skills-and-confidence-focused view (digital literacy, motivation, trust). A secondary tension exists between DSIT's desire for real-time dashboarding and the reality that most inclusion data is collected annually or quarterly.

### Critical Success Factors

- Integrate at least five authoritative data sources (Lloyds Consumer Digital Index, Ofcom Connected Nations, ONS Internet Access survey, DfE Essential Digital Skills, Good Things Foundation programme data) within 12 months
- Provide geographic disaggregation to local authority level for all inclusion metrics
- Enable local authorities to benchmark their digital inclusion performance against national averages and similar areas
- Establish a composite Digital Inclusion Index that combines connectivity, skills, and usage dimensions
- Demonstrate the platform's utility for targeting interventions by informing at least 10 local digital inclusion programmes within 18 months

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Agreement on the need for better digital inclusion measurement, but disagreement on what "digital inclusion" means (connectivity vs skills vs usage vs outcomes), whose data is authoritative, and whether the tracker should be a passive monitoring tool or an active intervention planning platform.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DSIT Minister for Tech and the Digital Economy | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DSIT Director of Digital Infrastructure | DSIT Senior Leadership | HIGH | HIGH | Manage Closely — Strategic direction, budget |
| DSIT Digital Inclusion Policy Lead | Policy ownership | HIGH | HIGH | Manage Closely — Policy alignment, data requirements |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews |
| CDDO Director | Cross-government digital assurance | HIGH | MEDIUM | Keep Satisfied — Spend control, standards |
| DSIT Data and Analytics Team | Data pipeline ownership | MEDIUM | HIGH | Keep Informed — Data integration, quality |
| DSIT Finance | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Ofcom | Regulator | Communications data provider, connectivity regulator | HIGH | HIGH |
| Lloyds Banking Group | Private sector | Consumer Digital Index data provider | MEDIUM | MEDIUM |
| Good Things Foundation | Charity | Digital inclusion programmes, National Databank | MEDIUM | HIGH |
| Local authority digital teams | ~340 local authorities | Data consumers, local intervention planners | LOW | HIGH |
| ONS | Statistics authority | Survey data provider, methodology governance | HIGH | MEDIUM |
| DfE (Department for Education) | Partner department | Essential Digital Skills framework owner | MEDIUM | MEDIUM |
| Age UK | Charity | Older people's digital inclusion advocacy | LOW | HIGH |
| Libraries Connected | Sector body | Library-based digital inclusion delivery | LOW | HIGH |
| Citizens Online | Charity | Digital inclusion measurement expertise | LOW | HIGH |
| Rural Services Network | Membership body | Rural connectivity advocacy | LOW | HIGH |
| Devolved administrations | Scottish/Welsh/NI governments | Digital inclusion in devolved contexts | MEDIUM | MEDIUM |
| Digitally excluded citizens | Citizens | Ultimate beneficiaries | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO Director    |  * DSIT Minister    |
        |  * DSIT Finance     |  * DSIT Director of |
        |  * ONS              |    Digital Infra    |
        |                     |  * DSIT Policy Lead |
 P      |                     |  * Service Owner    |
 O      |                     |  * Ofcom            |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Devolved admins  |  * Good Things Fdn  |
        |  * Lloyds Banking   |  * Local authorities|
        |    Group            |  * Age UK           |
        |  * DfE              |  * Libraries Connctd|
        |                     |  * Citizens Online  |
        |                     |  * Rural Services   |
        |                     |  * Excluded citizens|
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DSIT Minister — Evidence-Based Digital Inclusion Policy

**Stakeholder**: DSIT Minister for Tech and the Digital Economy

**Driver Category**: STRATEGIC

**Driver Statement**: Provide a robust evidence base for digital inclusion policy decisions, including targeting of government digital inclusion programmes and demonstrating progress against UK Digital Strategy commitments.

**Context & Background**:
The UK Digital Strategy committed to improving digital inclusion but lacked a centralised measurement platform. Current evidence is fragmented across Lloyds Bank Consumer Digital Index (annual, sample-based), Ofcom Connected Nations (annual, infrastructure-focused), and ONS surveys (periodic, high-level). Ministers need a unified view to answer parliamentary questions and direct resources.

**Driver Intensity**: CRITICAL

**Enablers**:

- Data sharing agreements with Lloyds, Ofcom, ONS, DfE
- Geographic disaggregation enabling constituency-level analysis for parliamentary questions
- Clear visualisations suitable for ministerial briefings

**Blockers**:

- Data latency (most sources annual or quarterly, not real-time)
- Different methodologies across data sources making composite indices complex
- Devolved policy areas creating gaps in UK-wide coverage

---

### SD-2: Ofcom — Connectivity Infrastructure Monitoring

**Stakeholder**: Ofcom

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure the tracker accurately represents broadband and mobile connectivity data from Connected Nations reports, using Ofcom's methodology and quality standards, without misrepresenting infrastructure coverage as a proxy for digital inclusion.

**Context & Background**:
Ofcom publishes detailed connectivity data annually in Connected Nations. They are concerned that a digital inclusion tracker might conflate connectivity availability with actual usage and skills, creating misleading policy conclusions (e.g., "broadband is available therefore people are included").

**Driver Intensity**: HIGH

**Enablers**:

- Clear distinction between connectivity metrics and inclusion metrics in dashboard
- API-based data feed from Ofcom to ensure data currency
- Joint methodology review process

**Blockers**:

- Ofcom's data release cycle may not align with tracker update frequency
- Granularity limitations on connectivity data at small geographic areas

---

### SD-3: Good Things Foundation — Community-Level Inclusion Data

**Stakeholder**: Good Things Foundation

**Driver Category**: CUSTOMER

**Driver Statement**: Integrate grassroots digital inclusion programme data from the National Databank and National Digital Inclusion Network into the tracker, making visible the impact of community-level interventions that are invisible in national-level surveys.

**Context & Background**:
Good Things Foundation operates the National Databank (providing free mobile data to digitally excluded people) and coordinates the National Digital Inclusion Network (3,800+ community organisations). They hold rich data on individual interventions but lack a platform to demonstrate aggregate impact alongside national statistics.

**Driver Intensity**: HIGH

**Enablers**:

- Data integration API for community programme data
- Privacy-preserving aggregation methodology for individual-level intervention data
- Recognition of community programmes alongside national infrastructure investment

**Blockers**:

- Quality and consistency of community-level data collection
- Privacy concerns around aggregating individual intervention data
- Data format standardisation across 3,800+ organisations

---

### SD-4: Local Authority Digital Teams — Benchmarking and Intervention Planning

**Stakeholder**: Local authority digital teams (~340 authorities)

**Driver Category**: OPERATIONAL

**Driver Statement**: Access local-area digital inclusion data to benchmark performance, identify priority populations and geographies, and plan targeted digital inclusion interventions — replacing the current approach of relying on national averages that mask local variation.

**Context & Background**:
Local authorities deliver many frontline digital inclusion programmes (library digital skills courses, council website accessibility, social care digital tools) but lack granular local data to target interventions. The Index of Multiple Deprivation provides deprivation data but does not directly measure digital inclusion dimensions.

**Driver Intensity**: MEDIUM

**Enablers**:

- Local authority level disaggregation for all metrics
- Benchmarking tool comparing similar local authorities
- Exportable data in open formats for local analysis

**Blockers**:

- Small sample sizes making local authority level estimates unreliable for some data sources
- Lack of standardised local-level digital inclusion data collection
- Local authority capacity to act on insights

---

### SD-5: Age UK — Older People's Digital Exclusion Visibility

**Stakeholder**: Age UK

**Driver Category**: CUSTOMER

**Driver Statement**: Ensure the tracker makes visible the disproportionate digital exclusion of older people (particularly those aged 75+), challenging the assumption that digital exclusion is solely a connectivity or skills issue when for many older people it is about confidence, trust, motivation, and physical accessibility of devices.

**Driver Intensity**: MEDIUM

**Enablers**:

- Age-disaggregated data for all inclusion metrics
- Inclusion of motivation and confidence dimensions alongside skills and connectivity
- Integration of Age UK survey data on older people's digital experiences

**Blockers**:

- Limited age-disaggregated data at local authority level
- Resistance to expanding "digital inclusion" beyond skills and connectivity

---

## Driver-to-Goal Mapping

### Goal G-1: Unified Digital Inclusion Data Platform

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: DSIT Director of Digital Infrastructure

**Goal Statement**: Integrate at least five authoritative digital inclusion data sources into a single platform with standardised APIs and a unified data model within 12 months of project start.

**Why This Matters**: Fragmented data prevents coherent policy-making (SD-1), risks misrepresentation of connectivity vs inclusion (SD-2), and excludes community-level impact data (SD-3).

**Success Metrics**:

- **Primary Metric**: Number of data sources integrated and operational
- **Secondary Metrics**:
  - Data freshness (time from source update to platform update)
  - API uptime and response time
  - Data quality score per source

**Baseline**: No centralised platform; data in separate publications and spreadsheets

**Target**: 5+ sources integrated, dashboard operational, quarterly update cycle minimum

---

### Goal G-2: Geographic Disaggregation to Local Authority Level

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Provide all digital inclusion metrics with geographic disaggregation to local authority level (and LSOA where data permits) within 12 months, enabling constituency-level parliamentary questions and local intervention planning.

**Success Metrics**:

- **Primary Metric**: Percentage of metrics available at local authority level
- **Secondary Metrics**:
  - Number of local authorities actively using the platform
  - Confidence intervals published for small-area estimates

**Baseline**: Most national data only available at region or country level

**Target**: 80%+ of metrics available at local authority level

---

### Goal G-3: Composite Digital Inclusion Index

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: DSIT Digital Inclusion Policy Lead

**Goal Statement**: Develop a peer-reviewed composite Digital Inclusion Index combining connectivity, skills, usage, motivation, and outcomes dimensions within 18 months, with transparent methodology and annual publication.

**Success Metrics**:

- **Primary Metric**: Index published with methodology paper
- **Secondary Metrics**:
  - Academic peer review completed
  - ONS methodology endorsement
  - Index cited in policy documents

**Baseline**: No composite UK digital inclusion index exists

**Target**: First edition published within 18 months, ONS endorsement within 24 months

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DSIT Minister | SD-1 | Evidence-based policy | G-1 | Unified data platform | O-1 | Better targeted inclusion programmes |
| DSIT Minister | SD-1 | Evidence-based policy | G-2 | Geographic disaggregation | O-1 | Better targeted inclusion programmes |
| DSIT Minister | SD-1 | Evidence-based policy | G-3 | Composite inclusion index | O-2 | UK digital inclusion improvement |
| Ofcom | SD-2 | Accurate connectivity data | G-1 | Unified data platform | O-1 | Better targeted inclusion programmes |
| Good Things Fdn | SD-3 | Community data integration | G-1 | Unified data platform | O-1 | Better targeted inclusion programmes |
| Local authorities | SD-4 | Benchmarking and planning | G-2 | Geographic disaggregation | O-1 | Better targeted inclusion programmes |
| Age UK | SD-5 | Older people visibility | G-3 | Composite inclusion index | O-2 | UK digital inclusion improvement |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Ofcom (SD-2) wants clear separation between connectivity and inclusion metrics, while DSIT Minister (SD-1) wants a single composite score for simplicity. A composite index that blends connectivity with skills could mislead policy.
  - **Resolution Strategy**: Composite index published with clear dimension breakdowns. Headline composite score available but dashboard always shows dimension-level detail. Ofcom co-authors methodology section on connectivity dimension.

- **Conflict 2**: Good Things Foundation (SD-3) wants community-level data integrated, but ONS is concerned about data quality from non-standardised community reporting undermining the platform's statistical credibility.
  - **Resolution Strategy**: Community data displayed in a separate layer with clear quality indicators. National statistical data distinguished from programme-level data. Joint quality framework developed.

**Synergies**:

- **Synergy 1**: DSIT Minister's evidence needs (SD-1) and local authorities' planning needs (SD-4) both benefit from the same geographic disaggregation infrastructure
- **Synergy 2**: Age UK's older people focus (SD-5) and Good Things Foundation's community data (SD-3) provide complementary perspectives that strengthen the composite index

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Data Latency Undermines Perceived Value

**Related Stakeholders**: DSIT Minister, local authorities

**Risk Description**: Most data sources update annually. Ministers and local authorities expect near-real-time dashboards. If data is always 6-12 months old, the platform may be perceived as a historical archive rather than a decision-support tool.

**Probability**: HIGH | **Impact**: MEDIUM

**Mitigation Strategy**: Supplement annual survey data with more frequent proxy indicators (e.g., library digital skills course registrations, National Databank SIM allocations). Set clear expectations about data freshness per source.

---

### Risk R-2: Small Area Estimates Unreliable

**Related Stakeholders**: Local authorities, DSIT Policy Lead

**Risk Description**: Sample-based surveys (Lloyds, ONS) produce unreliable estimates at local authority level, particularly for small authorities, leading to misleading benchmarking.

**Probability**: HIGH | **Impact**: HIGH

**Mitigation Strategy**: Publish confidence intervals alongside all small-area estimates. Use statistical modelling (small area estimation techniques) to improve reliability. Flag estimates with wide confidence intervals.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Data source selection | DSIT Data Team | Service Owner | Ofcom, ONS, Lloyds, Good Things Fdn | Local authorities |
| Composite index methodology | DSIT Policy Lead | DSIT Director | ONS, Ofcom, Age UK, academics | All stakeholders |
| Budget approval | DSIT Finance | SRO | CDDO | All |
| Architecture decisions | Technical Lead | SRO | CDDO, Security | Development team |
| Data quality standards | DSIT Data Team | ONS (advisory) | Data providers | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Lloyds Consumer Digital Index | Research | Lloyds Bank | Digital skills and engagement data | N/A — external reference |
| Ofcom Connected Nations | Report | Ofcom | Connectivity coverage and quality | N/A — external reference |
| UK Digital Strategy | Strategy | GOV.UK | Digital inclusion commitments | N/A — external reference |
| ONS Internet Access Survey | Statistics | ONS | Household internet access data | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Inclusion Tracker
**Model**: Claude Opus 4.6
