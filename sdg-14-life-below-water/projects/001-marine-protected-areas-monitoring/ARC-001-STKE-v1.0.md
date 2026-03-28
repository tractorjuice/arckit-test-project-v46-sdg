# Stakeholder Drivers & Goals Analysis: Marine Protected Areas Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
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
| **Distribution** | MPA Programme Board, DEFRA Digital, JNCC, Natural England, MMO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Marine Protected Areas Monitoring platform, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The MPA Monitoring programme sits at the intersection of conservation ambition, scientific rigour, and enforcement capability. The strongest alignment exists around improving the evidence base for MCZ condition assessments — this satisfies DEFRA's OSPAR/MSFD reporting obligations, JNCC's scientific mission, and Natural England's site management responsibilities simultaneously. The most significant conflict is between the pace of digital transformation desired by DEFRA Digital and the scientific community's insistence on validated, peer-reviewable data pipelines that require extensive calibration. A secondary tension exists between open data ambitions and the need to protect sensitive site location data that could enable exploitation.

### Critical Success Factors

- Deliver a single authoritative platform for MCZ condition assessment data, replacing fragmented spreadsheets and siloed databases across JNCC, Natural England, and Cefas
- Integrate remote sensing data (satellite, drone, acoustic survey) with in-situ sampling data to provide near-real-time site condition indicators
- Achieve OSPAR-compliant data quality standards that withstand international peer review
- Enable MMO enforcement officers to access MPA boundary and condition data in the field via mobile devices
- Maintain scientific credibility by preserving data provenance and uncertainty information throughout the processing chain

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for better MPA monitoring data and improved reporting capability. Tensions exist between scientific thoroughness (JNCC/Cefas) and delivery pace (DEFRA Digital), between open data publication (MEDIN/researchers) and enforcement sensitivity (MMO), and between comprehensive monitoring ambition and available survey budget (Natural England). The fishing industry views the platform with concern, fearing it will generate evidence used to extend or restrict fishing within MPAs.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Minister for the Environment | Ministerial sponsor | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DEFRA Chief Scientific Adviser | Scientific oversight | HIGH | HIGH | Manage Closely — Scientific advisory board, data quality governance |
| SRO, MPA Programme | Programme sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA CDIO | Digital strategy and technology oversight | HIGH | HIGH | Manage Closely — Architecture governance |
| JNCC Marine Team Director | Scientific authority for UK marine conservation | HIGH | HIGH | Manage Closely — Data standards, methodology governance |
| Natural England Marine Director | MPA site management and condition assessment | HIGH | HIGH | Manage Closely — Operational requirements, survey coordination |
| Cefas Chief Scientist | Marine science research and monitoring | HIGH | HIGH | Manage Closely — Scientific methods, sensor calibration |
| MMO Head of Compliance | MPA enforcement and monitoring | MEDIUM | HIGH | Keep Informed — Enforcement data requirements |
| DEFRA SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DEFRA Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case tracking |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| HM Treasury | HMT | Funding approval | HIGH | MEDIUM |
| OSPAR Commission | International treaty body | Reporting obligations | HIGH | MEDIUM |
| Marine Conservation Society (MCS) | Conservation NGO | Advocacy and citizen science | LOW | HIGH |
| Wildlife Trusts | Conservation NGO | Marine volunteer network | LOW | HIGH |
| NFFO (National Federation of Fishermen's Organisations) | Fishing industry body | Industry representation | MEDIUM | HIGH |
| IFCA (Inshore Fisheries and Conservation Authorities) | Statutory bodies | Inshore MPA management | MEDIUM | HIGH |
| UKHO (UK Hydrographic Office) | Charting authority | Bathymetric data supplier | MEDIUM | MEDIUM |
| MEDIN (Marine Environmental Data and Information Network) | Data standards body | Metadata standards | LOW | HIGH |
| Academic marine research community | Universities | Research users of MPA data | LOW | HIGH |
| Coastal communities | Public | Interest in local MPA health | LOW | HIGH |
| Blue Belt Programme | DEFRA/FCO | Overseas Territory MPA management | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for MPA Monitoring outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end MPA monitoring service and data outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |
| DDaT Profession Lead | Digital, Data & Technology capability and career framework | LOW / MEDIUM | Monitor — Capability assessments, recruitment support |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination and policy implementation | HIGH / MEDIUM | Keep Satisfied — Security compliance gates, incident reporting |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk, signs off risk acceptance | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security, CAF assessment, GovAssure liaison | MEDIUM / HIGH | Keep Informed — Security architecture reviews, pen test scheduling |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • DEFRA Minister   │
        │  • CDDO             │  • DEFRA Chief      │
        │  • DEFRA SIRO       │    Scientific Adviser│
        │  • DEFRA Finance    │  • SRO              │
        │  • OSPAR Commission │  • DEFRA CDIO       │
 P      │  • SSRO / DSO       │  • JNCC Marine Dir  │
 O      │                     │  • NE Marine Dir    │
 W      │                     │  • Cefas Chief Sci  │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • DDaT Lead        │  • MCS              │
        │  • Blue Belt        │  • Wildlife Trusts  │
        │                     │  • NFFO             │
        │                     │  • IFCAs            │
        │                     │  • MEDIN            │
        │                     │  • Academic          │
        │                     │    researchers       │
        │                     │  • MMO Compliance   │
        │                     │  • Coastal           │
        │                     │    communities       │
        │                     │  • Cyber Sec Lead   │
        │                     │  • Product Manager  │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| DEFRA Minister | HIGH | HIGH | Manage Closely | Ministerial briefings, PQ lines, quarterly programme review |
| DEFRA Chief Scientific Adviser | HIGH | HIGH | Manage Closely | Scientific advisory board, data quality governance |
| SRO | HIGH | HIGH | Manage Closely | Weekly programme board, decision escalation |
| DEFRA CDIO | HIGH | HIGH | Manage Closely | Architecture governance, digital strategy alignment |
| JNCC Marine Team Director | HIGH | HIGH | Manage Closely | Data standards governance, methodology review |
| Natural England Marine Director | HIGH | HIGH | Manage Closely | Operational requirements, survey coordination |
| Cefas Chief Scientist | HIGH | HIGH | Manage Closely | Scientific methods, sensor calibration standards |
| HM Treasury | HIGH | MEDIUM | Keep Satisfied | Business case updates, spending review submissions |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control submissions, service assessment gates |
| OSPAR Commission | HIGH | MEDIUM | Keep Satisfied | Reporting compliance, data quality evidence |
| DEFRA SIRO | HIGH | MEDIUM | Keep Satisfied | Risk acceptance, DPIA sign-off |
| DEFRA Finance Director | HIGH | MEDIUM | Keep Satisfied | Monthly spend reports, business case tracking |
| NFFO | MEDIUM | HIGH | Keep Informed | Industry consultation, data access transparency |
| IFCAs | MEDIUM | HIGH | Keep Informed | Inshore MPA data sharing, operational integration |
| MMO Compliance | MEDIUM | HIGH | Keep Informed | Enforcement data requirements, field access |
| MCS | LOW | HIGH | Keep Informed | Citizen science data integration, public dashboards |
| Wildlife Trusts | LOW | HIGH | Keep Informed | Volunteer survey data, community engagement |
| MEDIN | LOW | HIGH | Keep Informed | Metadata standards compliance |
| Academic researchers | LOW | HIGH | Keep Informed | Data access policy, API documentation |
| Coastal communities | LOW | HIGH | Keep Informed | Public-facing MPA health dashboards |
| Blue Belt Programme | MEDIUM | MEDIUM | Monitor | Overseas Territory integration potential |
| DDaT Profession Lead | LOW | MEDIUM | Monitor | Annual capability assessment |

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Minister — Demonstrable Progress on Marine Conservation Commitments

**Stakeholder**: DEFRA Minister for the Environment

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver visible, measurable progress against the 25 Year Environment Plan marine targets and OSPAR Convention obligations, enabling positive responses to parliamentary questions, Select Committee inquiries, and international reporting.

**Context & Background**:
The UK Government committed to achieving Good Environmental Status in UK waters under the Marine Strategy Framework Directive (now transposed into UK law). The 25 Year Environment Plan sets targets for a comprehensive, well-managed network of MPAs. The Minister faces scrutiny from the Environmental Audit Committee, marine conservation NGOs, and international partners (OSPAR, CBD). The current inability to provide real-time MPA condition data makes it difficult to demonstrate progress. Post-Brexit, the UK must show it can match or exceed EU marine conservation standards.

**Driver Intensity**: CRITICAL

**Enablers**:

- Real-time dashboard showing MPA network condition with trend indicators
- Automated OSPAR reporting with evidence of improving marine health indicators
- Positive case studies showing MPA recovery (species return, habitat restoration)
- Clear narrative linking monitoring investment to conservation outcomes

**Blockers**:

- Slow delivery due to scientific validation requirements
- MPA data showing deterioration (politically difficult even if scientifically accurate)
- NGO criticism that monitoring is not leading to stronger protection measures
- Industry lobbying against evidence-based fishing restrictions in MPAs

**Related Stakeholders**: JNCC (scientific evidence), OSPAR Commission (international reporting), MCS/Wildlife Trusts (advocacy), NFFO (industry concern)

---

### SD-2: JNCC Marine Team Director — Scientific Authority and Data Quality

**Stakeholder**: JNCC Marine Team Director

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Maintain JNCC's position as the authoritative source of marine conservation science for the UK Government, ensuring MPA condition assessment data meets internationally recognised quality standards and supports evidence-based policy.

**Context & Background**:
JNCC provides scientific advice to all four UK administrations on marine conservation. Their MPA condition assessments inform designation decisions, management measures, and OSPAR reporting. Current assessment processes are resource-intensive, relying on periodic surveys with long gaps between assessments. Some MCZs designated in 2013 have never had a full condition assessment. JNCC needs a monitoring platform that maintains scientific rigour while increasing assessment frequency and coverage. Their reputation depends on data quality — a flawed assessment that leads to incorrect policy would be severely damaging.

**Driver Intensity**: CRITICAL

**Enablers**:

- Automated quality assurance pipelines that flag anomalous data without discarding it
- Transparent methodology documentation accessible for peer review
- Integration of remote sensing with in-situ validation to increase spatial coverage
- Open data publication aligned with MEDIN standards for scientific reproducibility

**Blockers**:

- Pressure to publish data before adequate quality validation
- Loss of scientific control over data processing pipelines to software engineering teams
- Insufficient calibration and validation datasets for new remote sensing approaches
- Budget constraints limiting the ground-truth survey programme

**Related Stakeholders**: Cefas (scientific collaboration), Natural England (site assessments), MEDIN (data standards), academic researchers (data users)

---

### SD-3: Natural England Marine Director — Operational MPA Site Management

**Stakeholder**: Natural England Marine Director

**Driver Category**: OPERATIONAL

**Driver Statement**: Equip Natural England marine officers with timely, site-specific condition data to inform management advice, respond to consent applications, and prioritise survey effort across the 91 MCZs in English waters.

**Context & Background**:
Natural England is responsible for advising on the conservation of MCZs in English inshore and offshore waters. They currently manage site condition assessments using a combination of periodic diving surveys, drop-camera transects, acoustic surveys, and desk-based assessments. The backlog is significant — condition assessments are resource-constrained and many sites have not been assessed since designation. Natural England needs a platform that integrates multiple evidence sources (satellite imagery, acoustic data, citizen science records) to provide a more complete picture of site condition without replacing the need for in-situ verification entirely.

**Driver Intensity**: HIGH

**Enablers**:

- Integrated evidence platform showing all data sources for each MCZ on a single dashboard
- Automated change detection alerts (e.g., trawling activity detected within no-take zone)
- Mobile-accessible site information for field officers visiting MCZs
- Citizen science data integration (Seasearch diver reports, beach survey data)

**Blockers**:

- Multiple existing data systems that would need migration or integration
- Survey vessel time allocation constraints (limited DEFRA fleet capacity)
- Staff capacity to adopt new tools alongside existing operational commitments
- Different data formats across survey contractors and historical datasets

**Related Stakeholders**: JNCC (scientific standards), MMO (enforcement), IFCAs (inshore management), diving survey contractors

---

### SD-4: NFFO — Fair Treatment and Transparency in MPA Evidence

**Stakeholder**: National Federation of Fishermen's Organisations

**Driver Category**: FINANCIAL / RISK

**Driver Statement**: Ensure that MPA condition monitoring data is transparent, scientifically robust, and subject to independent review before it is used to justify additional fishing restrictions that affect livelihoods.

**Context & Background**:
The fishing industry has experienced successive spatial restrictions — MCZ designations, Highly Protected Marine Areas (HPMAs), offshore wind farm exclusion zones — each reducing available fishing grounds. NFFO members fear that a new monitoring platform will generate evidence used to justify further restrictions without adequate industry consultation or consideration of socio-economic impact. They want transparency in the data, methodology, and decision-making process. They also want their own observational data (fishers' ecological knowledge) to be valued alongside scientific survey data.

**Driver Intensity**: HIGH

**Enablers**:

- Open access to monitoring data and assessment methodologies
- Formal mechanism for industry data contribution (fisher observations, electronic monitoring)
- Socio-economic impact assessment alongside ecological condition assessment
- Industry representation on the scientific advisory board

**Blockers**:

- Perception that monitoring is conducted to justify predetermined outcomes
- Complex scientific data presented without accessible interpretation
- Exclusion from governance structures that determine how data is used
- Historical mistrust between fishing industry and conservation bodies

**Related Stakeholders**: IFCAs (inshore management), MMO (enforcement), DEFRA Minister (policy decisions), Cefas (scientific assessment)

---

### SD-5: MMO Head of Compliance — Effective MPA Enforcement

**Stakeholder**: MMO Head of Compliance and Enforcement

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Enable MMO enforcement officers to monitor vessel activity within MPAs in real time, detect potential infringements, and gather digital evidence that meets evidential standards for prosecution.

**Context & Background**:
The MMO is responsible for enforcing MPA regulations, including fishing restrictions within MCZs and HPMAs. Current enforcement relies on VMS position data (updated hourly for over-12m vessels), infrequent aerial surveillance, and at-sea patrols. Under-12m vessels are not VMS-equipped, creating a significant monitoring gap in inshore MCZs. The monitoring platform should integrate VMS/AIS data with MPA boundary data to provide automated alerts when vessels enter restricted zones, and the evidence chain must be robust enough for prosecution.

**Driver Intensity**: HIGH

**Enablers**:

- Real-time vessel tracking overlaid on MPA boundaries with automated alert generation
- Digital evidence capture with chain-of-custody metadata for prosecution
- Mobile access for enforcement officers at sea and in ports
- Integration with MMO's existing case management system

**Blockers**:

- Under-12m vessel tracking gap (no VMS requirement for small vessels)
- VMS data latency (hourly polling insufficient for real-time enforcement)
- Legal complexity of using remote sensing evidence in prosecution
- Resource constraints for at-sea enforcement response

**Related Stakeholders**: NFFO (industry relations), IFCAs (inshore enforcement), DEFRA Minister (enforcement policy), Cefas (scientific evidence for management measures)

---

### SD-6: Marine Conservation Society — Public Transparency and Citizen Science

**Stakeholder**: Marine Conservation Society (MCS)

**Driver Category**: CUSTOMER / ADVOCACY

**Driver Statement**: Ensure MPA condition data is publicly accessible, enabling informed public engagement with marine conservation, and integrate citizen science contributions (beach surveys, Seasearch dive records) as valued evidence sources.

**Context & Background**:
MCS runs the UK's largest marine citizen science programmes — annual beach clean and litter surveys, Seasearch volunteer diver surveys, and public engagement campaigns. They advocate for stronger MPA protection based on scientific evidence. MCS wants the monitoring platform to publish open data that enables NGOs and the public to hold government accountable for MPA condition, and to integrate citizen science data as a recognised evidence source alongside professional surveys.

**Driver Intensity**: MEDIUM

**Enablers**:

- Public-facing dashboard showing MPA condition for all UK sites
- API access for NGOs and researchers to download monitoring data
- Formal citizen science data submission pathway with quality validation
- Regular public reporting on MPA network health trends

**Blockers**:

- Data classified as OFFICIAL-SENSITIVE restricting public access
- Citizen science data not meeting professional quality standards
- Platform designed primarily for government users without public interface
- Scientific gatekeeping that undervalues non-professional observations

**Related Stakeholders**: Wildlife Trusts (citizen science), academic researchers (data users), coastal communities (public interest), MEDIN (data standards)

---

## Driver-to-Goal Mapping

### Goal G-1: Comprehensive MPA Condition Dashboard

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Statement**: Deliver a single, authoritative dashboard showing condition status for all 178 UK MPAs (91 MCZs, 87 SACs/SPAs with marine components), updated at least quarterly, with drill-down to individual site assessments.

**SMART Definition**:
- **Specific**: Dashboard covering all UK MPAs with standardised condition indicators
- **Measurable**: 100% site coverage with condition status (favourable/unfavourable/unknown), updated quarterly
- **Achievable**: Phased approach starting with MCZs, extending to SACs/SPAs
- **Relevant**: Directly supports OSPAR reporting, 25YEP targets, and site management
- **Time-bound**: MCZ coverage within 12 months, full MPA coverage within 24 months

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| MPA sites with current condition assessment | 35% | 90% | 24 months |
| Average assessment currency (age of most recent data) | 4.2 years | <1 year | 18 months |
| OSPAR reporting automation | 0% (manual) | 80% automated | 12 months |

---

### Goal G-2: Automated Infringement Detection

**Derived From Drivers**: SD-5, SD-1

**Goal Statement**: Deliver real-time vessel tracking overlaid on MPA boundaries with automated alert generation when regulated activities are detected within restricted zones.

**SMART Definition**:
- **Specific**: VMS/AIS data integrated with MPA boundary polygons, automated alert on zone entry
- **Measurable**: Alert generation within 15 minutes of zone entry for VMS-equipped vessels
- **Achievable**: Using existing VMS data feeds and published MPA boundary data
- **Relevant**: Directly supports MMO enforcement capability
- **Time-bound**: Operational within 9 months for over-12m vessels

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Mean detection time for MPA zone entry | >2 hours | <15 minutes | 9 months |
| Percentage of VMS-equipped vessels monitored | 60% | 98% | 6 months |
| Successful prosecutions supported by digital evidence | 12/year | 30/year | 18 months |

---

### Goal G-3: Open MPA Data Publication

**Derived From Drivers**: SD-4, SD-6, SD-2

**Goal Statement**: Publish MPA condition monitoring data as open data through MEDIN-compliant metadata records and accessible APIs, enabling industry scrutiny, NGO accountability monitoring, and academic research.

**SMART Definition**:
- **Specific**: All non-sensitive MPA data published via API and data.gov.uk with MEDIN metadata
- **Measurable**: Data available within 30 days of quality validation
- **Achievable**: Using existing MEDIN standards and data.gov.uk infrastructure
- **Relevant**: Satisfies open data policy, industry transparency demands, and scientific reproducibility
- **Time-bound**: First datasets published within 6 months, full catalogue within 18 months

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Datasets published as open data | 5 | 50+ | 18 months |
| API consumers (registered users) | 0 | 200+ | 12 months |
| Citizen science records integrated | 0 | 10,000+/year | 12 months |

---

## Conflict Analysis

### Conflict 1: Scientific Rigour vs Delivery Speed

**Stakeholders**: JNCC/Cefas (SD-2) vs DEFRA Digital/Minister (SD-1)

**Nature**: JNCC and Cefas require extensive calibration and validation before publishing data through the platform. DEFRA Digital wants rapid iterative delivery. The Minister wants visible progress quickly.

**Resolution Strategy**: PHASE — Deliver the platform infrastructure and historical data first (quick win), while running scientific validation in parallel. Publish data with explicit quality flags rather than waiting for full validation.

### Conflict 2: Open Data vs Enforcement Sensitivity

**Stakeholders**: MCS/NFFO/Researchers (SD-4, SD-6) vs MMO (SD-5)

**Nature**: Open data advocates want all MPA data published. MMO needs some vessel tracking and enforcement data to remain restricted for operational effectiveness.

**Resolution Strategy**: COMPROMISE — Publish ecological condition data openly. Restrict real-time vessel positions and active enforcement case data. Publish aggregated vessel activity data (not individual positions) with time delay.

### Conflict 3: Conservation Evidence vs Fishing Industry Concern

**Stakeholders**: JNCC/NE (SD-2, SD-3) vs NFFO (SD-4)

**Nature**: The fishing industry fears that improved monitoring will generate evidence for further restrictions. Conservation bodies see better evidence as essential for effective management.

**Resolution Strategy**: INNOVATE — Include socio-economic impact assessment alongside ecological condition. Establish industry advisory role in governance. Integrate fishers' ecological knowledge as a recognised data source.

---

## Communication Plan

| Stakeholder Group | Method | Frequency | Owner |
|-------------------|--------|-----------|-------|
| Programme Board (SRO, CDIO, JNCC, NE, Cefas) | Board meeting | Fortnightly | SRO |
| DEFRA Minister | Written briefing | Monthly | SRO |
| HM Treasury / CDDO | Spend report | Quarterly | Finance Director |
| Fishing industry (NFFO, IFCAs) | Industry liaison group | Quarterly | Service Owner |
| Conservation NGOs (MCS, Wildlife Trusts) | Stakeholder forum | Quarterly | Product Manager |
| Academic community | Newsletter, API documentation | Quarterly | Data Manager |
| Coastal communities | GOV.UK updates, local engagement | As needed | Communications |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Marine and Coastal Access Act 2009 | Legislation | UK Parliament | MCZ designation and management framework | legislation.gov.uk |
| 25 Year Environment Plan | Policy | HMG | Marine environment targets | gov.uk |
| OSPAR Quality Status Report | Standard | OSPAR | Assessment methodology and indicators | ospar.org |
| MEDIN Discovery Metadata Standard | Standard | MEDIN | Marine data metadata requirements | medin.org.uk |
| UK Marine Strategy Part Two | Policy | DEFRA | Monitoring programmes for GES indicators | gov.uk |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Marine Protected Areas Monitoring
**Model**: Claude Opus 4.6
