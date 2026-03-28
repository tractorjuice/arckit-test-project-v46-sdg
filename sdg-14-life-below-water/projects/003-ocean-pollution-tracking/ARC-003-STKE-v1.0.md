# Stakeholder Drivers & Goals Analysis: Ocean Pollution Tracking

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Ocean Pollution Tracking (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Ocean Pollution Tracking Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Pollution Programme Board, DEFRA, EA, MCA, Cefas, Public Health |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Ocean Pollution Tracking platform, their underlying drivers, and how these manifest into goals. The platform will provide integrated monitoring of marine litter, chemical contamination, oil spills, sewage discharges, and microplastic pollution across UK waters, supporting OSPAR MSFD Descriptor 8 (contaminants) and Descriptor 10 (marine litter) reporting obligations.

### Key Findings

The Ocean Pollution Tracking programme addresses a domain with intense public and media interest — beach pollution, sewage discharges, and microplastics generate significant political pressure. The strongest alignment is around establishing a single pollution intelligence picture that enables rapid incident response and long-term trend monitoring. The primary tension is between the desire for real-time public transparency (water companies, sewage outflows) and the complexity of interpreting pollution data in context — raw data without scientific interpretation risks misleading the public and triggering disproportionate responses. Water companies are defensive stakeholders who view the platform as increasing regulatory scrutiny.

### Critical Success Factors

- Integrate the diverse pollution monitoring data streams (beach surveys, water quality sampling, Event Duration Monitoring for storm overflows, satellite oil spill detection, Cefas contaminant monitoring) into a unified evidence platform
- Deliver public-facing dashboards showing bathing water quality and sewage discharge status with accuracy sufficient to withstand media scrutiny
- Enable Environment Agency enforcement officers to access pollution incident data in the field
- Support OSPAR MSFD reporting for Descriptors 8 and 10 with automated data extraction
- Maintain data quality standards that withstand scientific peer review and legal challenge

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for better pollution monitoring and public transparency. Tensions between rapid public data release and scientific validation, between environmental ambition and water company investment timelines, and between local pollution concerns and national strategic monitoring. Water companies are key data providers but reluctant participants.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Secretary of State | Ministerial sponsor | HIGH | HIGH | Manage Closely — Ministerial briefings |
| SRO, Pollution Programme | Programme sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA Chief Scientific Adviser | Scientific oversight | HIGH | HIGH | Manage Closely — Data quality governance |
| Environment Agency Chief Executive | Regulation and enforcement | HIGH | HIGH | Manage Closely — EA integration requirements |
| EA Head of Water Quality | Bathing water and pollution monitoring | HIGH | HIGH | Manage Closely — Operational requirements |
| Cefas Marine Contamination Team | Contaminant science | HIGH | HIGH | Manage Closely — Scientific methods |
| Maritime and Coastguard Agency (MCA) | Oil spill response | MEDIUM | HIGH | Keep Informed — Incident response integration |
| DEFRA CDIO | Digital strategy | HIGH | MEDIUM | Keep Satisfied — Architecture governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Water Companies (United Utilities, Thames Water, etc.) | Regulated utilities | Data providers (EDM, discharge data) | HIGH | HIGH |
| Ofwat | Water regulator | Regulatory oversight | HIGH | MEDIUM |
| OSPAR Commission | International treaty body | Reporting obligations | HIGH | MEDIUM |
| Marine Conservation Society (MCS) | Conservation NGO | Beach clean data, advocacy | LOW | HIGH |
| Surfers Against Sewage (SAS) | Environmental NGO | Real-time water quality advocacy | LOW | HIGH |
| UK Health Security Agency (UKHSA) | Public health | Bathing water health risk | HIGH | MEDIUM |
| Local authorities | Coastal councils | Beach management, local response | MEDIUM | HIGH |
| Coastal communities | Public | Beach safety, local environment | LOW | HIGH |
| Academic marine pollution researchers | Universities | Research, microplastics science | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Ofwat            │  • DEFRA Sec of     │
        │  • OSPAR            │    State            │
        │  • UKHSA            │  • SRO              │
        │  • DEFRA CDIO       │  • DEFRA Chief Sci  │
        │                     │  • EA Chief Exec    │
 P      │                     │  • EA Water Quality │
 O      │                     │  • Cefas Marine     │
 W      │                     │  • Water Companies  │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Academic         │  • MCS              │
        │    researchers      │  • Surfers Against  │
        │                     │    Sewage           │
        │                     │  • MCA              │
        │                     │  • Local authorities│
        │                     │  • Coastal          │
        │                     │    communities      │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Secretary of State — Public Accountability on Water Pollution

**Stakeholder**: DEFRA Secretary of State

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver transparent, real-time public information on marine pollution — particularly sewage discharges — demonstrating government action on a high-profile environmental issue that generates sustained media and parliamentary pressure.

**Context & Background**:
Storm overflow discharges into rivers and the sea have become one of the most prominent environmental issues in UK public discourse. The Environment Act 2021 introduced new duties on water companies to reduce storm overflow discharges and on the EA to monitor and report. Parliamentary debates, media investigations, and public campaigns (led by SAS, MCS, and others) demand transparency. The Minister needs a platform that provides defensible, real-time pollution data and demonstrates accountability.

**Driver Intensity**: CRITICAL

**Enablers**:

- Real-time public dashboard showing sewage discharge status at every bathing water
- Automated alerts when pollution incidents affect public beaches
- Annual reporting showing trend improvement in water quality
- Clear attribution of pollution sources (water company, agricultural, shipping)

**Blockers**:

- Water company resistance to real-time data publication
- Data showing worsening trends during investment period
- Technical complexity of attributing pollution to specific sources
- Media oversimplification of complex environmental data

**Related Stakeholders**: EA (enforcement), water companies (data providers), SAS/MCS (advocacy), UKHSA (public health)

---

### SD-2: EA Head of Water Quality — Integrated Pollution Intelligence

**Stakeholder**: EA Head of Water Quality

**Driver Category**: OPERATIONAL

**Driver Statement**: Replace fragmented pollution monitoring databases with a single operational intelligence platform that enables rapid incident response, trend analysis, and evidence-based enforcement against polluters.

**Context & Background**:
The EA currently monitors bathing water quality at 400+ designated bathing waters, responds to pollution incidents, operates the Event Duration Monitoring (EDM) programme for storm overflows, and enforces against illegal discharges. Data sits in multiple systems — the Bathing Water Information System, EDM data portal, WIMS (Water Information Management System), and incident management systems. Linking a pollution incident to its source, assessing impact on bathing water quality, and building an enforcement case requires manual data collation across systems.

**Driver Intensity**: CRITICAL

**Enablers**:

- Unified pollution dashboard with all data sources on a single map
- Automated correlation between EDM spill events and bathing water sample results
- Mobile access for enforcement officers at beach and shoreline locations
- Digital evidence capture with chain-of-custody metadata for prosecution

**Blockers**:

- Legacy system migration complexity (WIMS has 30+ years of data)
- Multiple data owners across EA business areas
- Budget constraints for EA digital transformation
- Staff resistance to new workflows

**Related Stakeholders**: Water companies (EDM data), UKHSA (health risk assessment), local authorities (beach management)

---

### SD-3: Water Companies — Managing Regulatory Burden and Reputational Risk

**Stakeholder**: Water companies (collectively — United Utilities, Thames Water, Anglian Water, etc.)

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Comply with EDM monitoring and reporting requirements while managing reputational risk from real-time disclosure of storm overflow data, and demonstrating investment progress towards government targets.

**Context & Background**:
Water companies are required to monitor and report storm overflow discharges under the Environment Act 2021. They have committed to significant capital investment (>GBP 56 billion in AMP8, 2025-2030) to reduce storm overflow frequency. They view real-time public disclosure of discharge data with concern — the data is technically complex (a monitored spill event does not necessarily mean environmental harm) and media reporting tends to be simplistic. However, they recognise that transparency is now mandatory and that demonstrating improvement is in their long-term interest.

**Driver Intensity**: HIGH

**Enablers**:

- Clear, contextual presentation of EDM data (not just raw spill counts)
- Recognition of investment progress and improvement trends
- Standardised data submission format reducing compliance burden
- Opportunity to demonstrate environmental stewardship

**Blockers**:

- Raw data presented without context, leading to misleading public interpretation
- Inconsistent data standards across the platform
- Retrospective application of new monitoring standards to historical data
- Competitive disadvantage if companies' data is presented inconsistently

**Related Stakeholders**: Ofwat (regulatory investment), EA (enforcement), SAS/MCS (public advocacy), DEFRA Minister (political pressure)

---

### SD-4: Surfers Against Sewage — Real-Time Public Water Quality Information

**Stakeholder**: Surfers Against Sewage (SAS)

**Driver Category**: CUSTOMER / ADVOCACY

**Driver Statement**: Deliver real-time, public-facing water quality information at every bathing water and popular water recreation site, enabling water users to make informed decisions about when and where it is safe to swim, surf, or paddle.

**Context & Background**:
SAS operates the Safer Seas & Rivers Service, a public alert system based on water company EDM data and EA bathing water sample results. They want the government platform to go further — providing real-time pollution risk assessments, not just historical sample data. Their constituency is recreational water users who need actionable, timely information about water safety.

**Driver Intensity**: MEDIUM

**Enablers**:

- Real-time pollution risk indicator at each bathing water (not just annual classification)
- API access enabling SAS and others to build public-facing apps
- Clear communication of when water quality is poor and why
- Integration of citizen-reported pollution incidents

**Blockers**:

- Platform designed for regulatory use without public-facing capability
- Delayed data publication that is not useful for same-day decisions
- Over-cautious legal disclaimers that obscure safety information
- Lack of predictive capability (telling users about tomorrow, not yesterday)

**Related Stakeholders**: MCS (beach surveys), coastal communities (local interest), UKHSA (health risk), local authorities (beach management)

---

### SD-5: Cefas Marine Contamination Team — Scientific Evidence for MSFD

**Stakeholder**: Cefas Marine Contamination Team

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Ensure the pollution tracking platform integrates chemical contaminant monitoring data (heavy metals, persistent organic pollutants, microplastics) to support UK Marine Strategy MSFD Descriptor 8 (contaminants) and Descriptor 10 (marine litter) assessments.

**Context & Background**:
Cefas runs the Clean Seas Environment Monitoring Programme (CSEMP), monitoring contaminant concentrations in sediment, water, and biota across UK waters. They also contribute to OSPAR monitoring assessments. Current data is in specialist scientific databases. Integration with the broader pollution tracking platform would enable holistic assessment — linking near-shore pollution events (sewage, litter) with offshore contaminant trends and ecological impact indicators.

**Driver Intensity**: HIGH

**Enablers**:

- API integration between CSEMP database and the pollution platform
- Standardised contaminant data format supporting OSPAR reporting
- Spatial visualisation of contaminant trends alongside other pollution data
- Microplastics monitoring data integration as scientific methods mature

**Blockers**:

- Different temporal and spatial scales between beach monitoring and offshore sampling
- Contaminant data requiring specialist interpretation (not suitable for raw public display)
- Scientific uncertainty in microplastics monitoring methodologies
- Budget constraints for expanding CSEMP sampling programme

**Related Stakeholders**: OSPAR (international reporting), JNCC (conservation impact), academic researchers (microplastics)

---

### SD-6: MCA — Oil Spill Detection and Response Coordination

**Stakeholder**: Maritime and Coastguard Agency

**Driver Category**: OPERATIONAL

**Driver Statement**: Integrate satellite-based oil spill detection with the pollution tracking platform to enable faster response coordination and improved spill source identification.

**Context & Background**:
MCA operates the UK's National Contingency Plan for oil spill response. Satellite-based synthetic aperture radar (SAR) can detect oil slicks, but integration with other marine data (AIS vessel tracks, current models, historical spill records) is limited. MCA wants the platform to correlate oil slick detections with vessel movements to identify potential polluters, and to share spill data with EA for shoreline impact assessment.

**Driver Intensity**: MEDIUM

**Enablers**:

- Satellite SAR oil slick detection feed integrated into the platform
- AIS vessel track correlation for source identification
- Spill trajectory modelling integrated with coastal impact assessment
- Shared incident management between MCA (at sea) and EA (shoreline)

**Blockers**:

- SAR false positive rate (natural slicks vs oil spills)
- Real-time satellite data processing requirements
- Operational security concerns about sharing vessel track data
- Different incident management systems between MCA and EA

**Related Stakeholders**: EA (shoreline response), water companies (outfall proximity), coastal communities (local impact)

---

## Driver-to-Goal Mapping

### Goal G-1: Real-Time Public Pollution Dashboard

**Derived From Drivers**: SD-1, SD-4, SD-2

**Goal Statement**: Deliver a public-facing dashboard showing pollution status at all designated bathing waters, with real-time sewage discharge alerts and bathing water quality assessments.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Bathing waters with real-time pollution indicator | 0 | 420+ | 12 months |
| Public dashboard monthly users | 0 | 100,000+ | 12 months post-launch |
| Data latency (EDM to public display) | 48 hours | <2 hours | 9 months |

---

### Goal G-2: Integrated Pollution Evidence Platform

**Derived From Drivers**: SD-2, SD-5, SD-6

**Goal Statement**: Unify EA, Cefas, MCA, and water company pollution data into a single platform supporting incident response, trend analysis, and OSPAR reporting.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Pollution data sources integrated | 3 (siloed) | 8+ (unified) | 18 months |
| Pollution incident response data assembly time | 4 hours | <30 minutes | 12 months |
| OSPAR Descriptor 8/10 reporting automation | 0% | 70% | 18 months |

---

### Goal G-3: Enforcement Evidence Chain

**Derived From Drivers**: SD-2, SD-1

**Goal Statement**: Enable EA enforcement officers to build prosecution-grade evidence cases against polluters using digital evidence from the platform with full chain-of-custody metadata.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Pollution enforcement cases supported by digital evidence | 25% | 80% | 18 months |
| Mean evidence assembly time | 3 days | <4 hours | 12 months |

---

## Conflict Analysis

### Conflict 1: Real-Time Transparency vs Data Context

**Stakeholders**: SAS/public (SD-4) vs water companies (SD-3) vs DEFRA scientists (SD-5)

**Nature**: Public demands immediate raw data. Water companies want contextual presentation. Scientists insist on quality validation before publication.

**Resolution Strategy**: COMPROMISE — Publish EDM event data in near-real-time with clear status labels (spilling/not spilling). Bathing water risk assessment updated daily with scientific context. Contaminant trend data published after validation with lag.

### Conflict 2: Attribution vs Complexity

**Stakeholders**: DEFRA Minister (SD-1) vs EA (SD-2) vs water companies (SD-3)

**Nature**: Politicians want clear "who is responsible" attribution. EA recognises multiple sources (agriculture, sewage, shipping). Water companies resist being sole attribution target.

**Resolution Strategy**: INNOVATE — Source apportionment model that shows relative contribution of different pollution sources at each bathing water. Honest presentation of uncertainty.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environment Act 2021 | Legislation | UK Parliament | Storm overflow duties, monitoring requirements | legislation.gov.uk |
| OSPAR MSFD Descriptors 8, 10 | Standard | OSPAR | Contaminant and marine litter assessment criteria | ospar.org |
| Bathing Water Regulations 2013 | Legislation | UK Parliament | Bathing water quality standards | legislation.gov.uk |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Ocean Pollution Tracking
**Model**: Claude Opus 4.6
