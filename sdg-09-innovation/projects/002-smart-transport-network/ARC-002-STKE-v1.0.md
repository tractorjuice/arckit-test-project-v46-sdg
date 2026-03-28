# Stakeholder Drivers & Goals Analysis: Smart Transport Network

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Smart Transport Network (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart Transport Network Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart Transport Programme Board, DfT Digital, Transport Operators |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Smart Transport Network platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Smart Transport Network platform must reconcile the fragmented nature of UK transport governance — with responsibilities split across DfT, Network Rail, National Highways, Transport for London, combined authorities, and hundreds of bus operators — with the user need for a seamless, integrated view of multimodal transport. The strongest alignment exists around improving passenger information quality and real-time reliability data. The most significant conflict is between the ambition for an integrated national platform and the operational reality that transport data is owned and managed by diverse organisations with different systems, standards, and commercial models.

### Critical Success Factors

- Achieve data submission compliance from the highly fragmented bus operator market (particularly smaller operators who lack technical capability)
- Integrate real-time data feeds from multiple sources (Network Rail Darwin, TfL Unified API, National Highways DATEX II, BODS) into a coherent multimodal view
- Deliver measurable improvement to passenger journey planning accuracy, particularly for multimodal journeys involving transfers between modes
- Meet Bus Open Data Service (BODS) regulatory requirements while adding value beyond compliance
- Support Network Rail, National Highways, and combined authorities in infrastructure management decision-making using integrated network data

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the principle of better-connected transport data. Significant tensions between national standardisation ambitions (DfT) and local operational autonomy (combined authorities, TfL). Bus operator compliance burden versus data quality requirements creates ongoing friction. Rail and road data ecosystems have evolved separately with different standards and governance models that are difficult to unify.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Transport | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DfT Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Smart Transport Network | Programme Sponsor (DfT) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DfT Chief Digital and Information Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DfT Bus Policy Team | Bus Services Act compliance | MEDIUM | HIGH | Keep Informed — BODS integration |
| DfT Rail Policy Team | Rail reform programme | MEDIUM | HIGH | Keep Informed — GBR data strategy |
| DfT SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off |
| DfT Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Network Rail | Infrastructure manager | Rail data provider (Darwin, TRUST) | HIGH | HIGH |
| National Highways | Strategic road network | Road data provider (DATEX II, NTIS) | HIGH | HIGH |
| Transport for London (TfL) | Regional authority | Multimodal data provider (Unified API) | HIGH | HIGH |
| Great British Railways (GBR) Transition Team | Rail reform | Future rail data governance | HIGH | HIGH |
| Combined Authorities (10) | Regional transport | Multimodal planning authorities | MEDIUM | HIGH |
| Bus Operators (large: First, Stagecoach, Arriva, Go-Ahead) | Commercial operators | Bus data providers (BODS) | MEDIUM | HIGH |
| Bus Operators (small/medium, ~500) | Commercial operators | Bus data providers, lower capability | LOW | MEDIUM |
| Traveline | Journey planning | Existing data aggregator | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Passengers / Citizens | Public | End users of transport information | LOW | HIGH |
| Office of Rail and Road (ORR) | Regulator | Rail performance monitoring | HIGH | MEDIUM |
| Traffic Commissioners | Regulator | Bus service registration | MEDIUM | MEDIUM |
| Ordnance Survey | Geospatial data | Road and rail geometry | MEDIUM | MEDIUM |
| NaPTAN National Dataset | DfT | Authoritative stop/station identifiers | MEDIUM | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for Smart Transport outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | Owns end-to-end transport data service | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews |
| Delivery Manager | Manages delivery cadence and risks | MEDIUM / HIGH | Keep Informed — Stand-ups |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Submissions |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Board-level protective security risk | HIGH / MEDIUM | Keep Satisfied — Quarterly review |
| Departmental Security Officer (DSO) | Security coordination | HIGH / MEDIUM | Keep Satisfied — Compliance gates |
| Senior Information Risk Owner (SIRO) | Information and cyber risk | HIGH / MEDIUM | Keep Satisfied — DPIA sign-off |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed — Architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • Secretary of     │
        │  • ORR              │    State (DfT)      │
        │  • CDDO             │  • Permanent Sec.   │
        │  • DfT SIRO         │  • SRO              │
        │  • DfT Finance Dir  │  • DfT CDIO         │
 P      │                     │  • Network Rail     │
 O      │                     │  • National Highways│
 W      │                     │  • TfL              │
 E      │                     │  • GBR Transition   │
 R      ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Small bus ops    │  • Passengers       │
        │                     │  • Combined Auths   │
        │                     │  • Large bus ops    │
        │                     │  • Traveline        │
        │                     │  • NaPTAN           │
        │                     │  • DfT Policy Teams │
        │                     │  • Traffic Comms    │
        │                     │  • Ordnance Survey  │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Deliver Better-Connected Transport

**Stakeholder**: Secretary of State for Transport

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate that government investment in transport data infrastructure translates into tangible improvements for passengers — more reliable journey planning, fewer "ghost buses," and seamless multimodal travel — supporting the government's Net Zero Transport Plan and levelling-up commitments.

**Context & Background**:
Transport connectivity is central to the levelling-up agenda. Passengers outside London experience significantly worse journey planning and real-time information than TfL users. The Bus Services Act 2017 mandated open bus data (BODS), but compliance has been uneven and data quality variable. The planned Great British Railways reform creates an opportunity to modernise rail data governance alongside bus and road data integration.

**Driver Intensity**: CRITICAL

**Enablers**:

- BODS regulatory framework already in place for bus data
- Network Rail Darwin feed established for rail real-time data
- GBR reform creating opportunity for rail data modernisation

**Blockers**:

- Fragmented transport governance across hundreds of organisations
- Legacy systems in rail (30+ year-old technology in some areas)
- Small bus operators lack capability for real-time data provision

**Related Stakeholders**: GBR Transition Team, Combined Authorities, Passengers

---

### SD-2: Network Rail — Infrastructure Intelligence for Performance Improvement

**Stakeholder**: Network Rail

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Leverage integrated transport data to improve network performance monitoring, predict and prevent disruption, coordinate cross-modal incident response, and provide evidence for regulatory performance reviews by the Office of Rail and Road.

**Context & Background**:
Network Rail manages 20,000 miles of track, 2,500 stations, and thousands of bridges, tunnels, and level crossings. Current performance monitoring relies on internal systems (TRUST, Darwin) with limited integration with road and bus networks. When a rail disruption occurs, passengers need multimodal alternatives — but rail, bus, and road data systems are not connected, making coordinated disruption response difficult.

**Driver Intensity**: HIGH

**Enablers**:

- Existing Darwin real-time train data feed (established, well-understood)
- Network Rail's digital strategy commitment to open data
- ORR performance framework creating incentive for improvement

**Blockers**:

- Legacy TRUST system limitations on data granularity
- Organisational complexity of TOC/FOC operator relationships
- Integration complexity across rail, bus, and road data models

**Related Stakeholders**: ORR, Train Operating Companies, Combined Authorities

---

### SD-3: Combined Authorities — Integrated Local Transport Planning

**Stakeholder**: Combined Authorities (Greater Manchester, West Midlands, West Yorkshire, etc.)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Access integrated, multimodal transport data for their region to plan bus networks under new franchising powers, coordinate with rail and road, model the impact of transport interventions, and provide passengers with unified multimodal journey information.

**Context & Background**:
The Bus Services Act 2017 gave combined authorities powers to franchise bus services. Greater Manchester's Bee Network is the first major franchised bus network outside London. Combined authorities need integrated data across all modes (bus, tram, rail, road) to plan networks effectively, but current data is siloed by mode and operator. Each combined authority is building its own integration solutions at significant cost.

**Driver Intensity**: HIGH

**Enablers**:

- New franchising powers create both mandate and motivation for data integration
- TfL's Unified API provides a proven model
- Combined authorities willing to co-invest and co-develop

**Blockers**:

- Each combined authority has different systems and capabilities
- Bus franchising transitions create period of dual-running with both commercial and franchised services
- Tension between national standardisation and local customisation needs

**Related Stakeholders**: Bus Operators, DfT Bus Policy, TfL, Passengers

---

### SD-4: Large Bus Operators — Regulatory Compliance with Minimum Burden

**Stakeholder**: First Group, Stagecoach, Arriva, Go-Ahead Group

**Driver Category**: COMPLIANCE / COMMERCIAL

**Driver Statement**: Meet Bus Open Data Service (BODS) requirements for timetable, real-time, and fares data publication with minimum incremental cost and administrative burden, while protecting commercially sensitive route-level revenue data.

**Context & Background**:
BODS mandates publication of timetable (TransXChange), real-time (SIRI-VM), and fares data for all local bus services in England. Large operators have invested in compliance but face ongoing costs for data quality maintenance. Operators are concerned that open data enables competitors to analyse their network strategies and that a government platform could eventually disintermediate their own customer-facing apps.

**Driver Intensity**: MEDIUM

**Enablers**:

- BODS compliance infrastructure already built and operational
- Industry standards (TransXChange, SIRI) well-established
- Commercial benefit of better passenger information driving ridership

**Blockers**:

- Ongoing data quality burden (timetable changes, real-time feed maintenance)
- Concern about commercially sensitive data exposure
- Fear of government platform competing with operator apps

**Related Stakeholders**: Traffic Commissioners, DfT Bus Policy, Combined Authorities

---

### SD-5: Passengers — Reliable, Real-Time Multimodal Journey Information

**Stakeholder**: Passengers / Citizens

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Get accurate, real-time information about all transport options for a journey — including bus, rail, tram, cycling, and walking — in a single place, with honest delay predictions and genuine multimodal alternatives when disruption occurs.

**Context & Background**:
Outside London, passengers face a fragmented information landscape: National Rail Enquiries for trains, individual bus operator apps, Traveline for buses (often without real-time data), and no integration between modes. "Ghost buses" — services shown as running but not appearing — erode trust. Multimodal journeys involving a bus-to-train transfer are particularly poorly served.

**Driver Intensity**: HIGH

**Enablers**:

- Smartphone ubiquity enables real-time multimodal information delivery
- Google and Apple Maps already aggregate some transport data, proving the model
- BODS has improved bus data availability (if not yet quality)

**Blockers**:

- Real-time bus data quality is poor (30-40% of services lack real-time tracking)
- No standardised cross-modal transfer time data
- Journey planning algorithms optimised for single modes, not multimodal

**Related Stakeholders**: Combined Authorities, Bus Operators, Network Rail, Traveline

---

### SD-6: National Highways — Connected Road Network Intelligence

**Stakeholder**: National Highways

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Integrate strategic road network (SRN) data with public transport and local road data to enable holistic traffic management, support modal shift policies, and provide evidence for road investment decisions through the Road Investment Strategy (RIS).

**Context & Background**:
National Highways manages England's motorways and major A-roads (4,300 miles). Current systems (NTIS, DATEX II feeds) focus on the SRN in isolation. Integration with bus and rail data would enable better understanding of modal shift impacts, improved diversion route management during SRN incidents, and evidence for multi-modal investment decisions.

**Driver Intensity**: MEDIUM

**Enablers**:

- DATEX II standard already adopted for SRN data exchange
- National Traffic Information Service (NTIS) provides comprehensive SRN data
- Road Investment Strategy (RIS3) requires evidence-based investment cases

**Blockers**:

- Local road data (managed by 153 local highway authorities) is fragmented and inconsistent
- Real-time SRN data volumes are very high (millions of events per day)
- Integration with public transport data requires new data models and standards

**Related Stakeholders**: DfT, Local Highway Authorities, Combined Authorities

---

## Driver-to-Goal Mapping

### Goal G-1: Unified Multimodal Transport Data Platform

**Derived From Drivers**: SD-1, SD-2, SD-3, SD-6

**Goal Owner**: SRO, Smart Transport Network

**Goal Statement**: Deliver a platform that integrates real-time and timetabled data across bus (BODS), rail (Darwin/GBR), strategic roads (NTIS/DATEX II), and urban transit (TfL, tram operators) into a single API by Q2 2028, covering 95% of UK public transport services.

**Why This Matters**: Fragmented transport data prevents effective multimodal journey planning, coordinated disruption response, and evidence-based investment planning.

**Success Metrics**:

- **Primary Metric**: Percentage of UK public transport services with data integrated into the platform
- **Secondary Metrics**:
  - Number of transport authorities consuming data via API
  - Data latency: real-time feeds < 30 seconds end-to-end
  - API availability: 99.95% uptime

**Baseline**: Data fragmented across BODS, Darwin, NTIS, TfL API, and individual operator feeds

**Target**: 95% of services integrated, unified API, < 30 second latency

---

### Goal G-2: Real-Time Bus Data Quality Improvement

**Derived From Drivers**: SD-1, SD-4, SD-5

**Goal Owner**: DfT Bus Policy Team

**Goal Statement**: Increase the percentage of local bus services with reliable real-time vehicle tracking data from approximately 60% to 90% by Q4 2027, with a "ghost bus" detection rate > 95%.

**Why This Matters**: "Ghost buses" — services shown on apps but not running — are the single biggest source of passenger complaint about bus information. Improving real-time data quality directly improves passenger trust and ridership.

**Success Metrics**:

- **Primary Metric**: Percentage of bus services with real-time AVL data
- **Secondary Metrics**:
  - Ghost bus detection rate
  - Real-time data freshness (average age of last position report)
  - Operator compliance rate with BODS real-time requirements

**Baseline**: ~60% of services with real-time data, limited ghost bus detection

**Target**: 90% real-time coverage, >95% ghost bus detection

---

### Goal G-3: Cross-Modal Disruption Management

**Derived From Drivers**: SD-2, SD-3, SD-6

**Goal Owner**: Network Rail / National Highways (joint)

**Goal Statement**: Enable automated cross-modal alternative route suggestions when disruption occurs on any mode, reducing passenger replan time from an average of 15 minutes to under 3 minutes for incidents affecting major corridors.

**Why This Matters**: When a train service is cancelled, passengers need to know the next bus or an alternative route. Currently this requires checking multiple apps and knowledge of local geography.

**Success Metrics**:

- **Primary Metric**: Average passenger replan time during disruption
- **Secondary Metrics**:
  - Number of cross-modal alternative suggestions served per disruption event
  - Passenger satisfaction with disruption information (post-incident survey)

**Baseline**: 15 minutes average replan time, no automated cross-modal alternatives

**Target**: < 3 minutes replan time, automated alternatives for major corridors

---

## Goal-to-Outcome Mapping

### Outcome O-1: Better-Connected UK Transport

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Deliver measurable improvement to passenger journey experience through integrated transport data, targeting a 15-point increase in Transport Focus passenger satisfaction for journey information quality by 2029.

**Measurement Details**:

- **KPI**: Transport Focus National Passenger Survey — journey information satisfaction
- **Current Value**: 72% satisfaction (bus), 78% satisfaction (rail)
- **Target Value**: 87% satisfaction (bus), 90% satisfaction (rail)
- **Measurement Frequency**: Annual
- **Data Source**: Transport Focus National Passenger Survey
- **Report Owner**: DfT Statistics and Analytics

**Business Value**:

- **Financial Impact**: Estimated 3-5% bus ridership increase from improved information, worth GBP 150-250M in fare revenue over 5 years
- **Strategic Impact**: Supports modal shift to public transport (Net Zero Transport Plan)
- **Operational Impact**: Coordinated disruption management reduces network-wide delay minutes
- **Customer Impact**: Passengers can plan and replan multimodal journeys confidently

---

### Outcome O-2: Evidence-Based Transport Investment

**Supported Goals**: G-1, G-3

**Outcome Statement**: Integrated transport data enables better investment decisions across road, rail, and bus, reducing the cost of transport modelling for major schemes by 30% and improving the accuracy of demand forecasts.

**Measurement Details**:

- **KPI**: Transport modelling cost per major scheme
- **Current Value**: GBP 2-5M per major scheme for transport modelling
- **Target Value**: GBP 1.4-3.5M per scheme (30% reduction)
- **Measurement Frequency**: Per scheme
- **Data Source**: DfT Major Projects Portfolio
- **Report Owner**: DfT Economics

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Better-connected transport | G-1 | Unified data platform | O-1 | Passenger satisfaction |
| Secretary of State | SD-1 | Better-connected transport | G-2 | Bus data quality | O-1 | Passenger satisfaction |
| Network Rail | SD-2 | Infrastructure intelligence | G-1 | Unified data platform | O-2 | Evidence-based investment |
| Network Rail | SD-2 | Infrastructure intelligence | G-3 | Disruption management | O-1 | Passenger satisfaction |
| Combined Authorities | SD-3 | Integrated local planning | G-1 | Unified data platform | O-1 | Passenger satisfaction |
| Bus Operators | SD-4 | Regulatory compliance | G-2 | Bus data quality | O-1 | Passenger satisfaction |
| Passengers | SD-5 | Reliable journey info | G-2 | Bus data quality | O-1 | Passenger satisfaction |
| National Highways | SD-6 | Connected road intelligence | G-1 | Unified data platform | O-2 | Evidence-based investment |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DfT wants national standardisation (SD-1) but Combined Authorities (SD-3) want local customisation to support franchise-specific needs (e.g., Greater Manchester Bee Network branding, West Midlands MaaS integration).
  - **Resolution Strategy**: Platform provides national baseline with extension points for local customisation. Combined authorities can add local data layers and branding on top of the national core.

- **Conflict 2**: Large bus operators (SD-4) want minimum data burden, but passengers (SD-5) want maximum data quality including real-time vehicle locations for every service.
  - **Resolution Strategy**: Phased approach — mandatory real-time AVL for operators above a fleet threshold, with DfT grant funding for smaller operators to adopt AVL technology. Data quality dashboards published publicly to create transparency and accountability.

**Synergies**:

- **Synergy 1**: Network Rail's disruption management needs (SD-2) and passengers' real-time information needs (SD-5) are directly aligned — the same cross-modal data integration serves both
- **Synergy 2**: Combined authorities' franchising data needs (SD-3) and DfT's BODS compliance monitoring (SD-1) are served by the same data quality infrastructure

---

## Communication & Engagement Plan

### Transport Operators (Network Rail, National Highways, Bus Operators)

**Primary Message**: The platform integrates your existing data feeds rather than replacing them, reducing duplication of data requests while improving the quality of passenger information that drives ridership and satisfaction.

**Key Talking Points**:

- Build on existing standards (TransXChange, SIRI, Darwin, DATEX II) rather than inventing new ones
- Reduce the multiple, fragmented data requests you receive from DfT, combined authorities, and third-party journey planners
- Better passenger information drives bus ridership (3-5% uplift from reliable real-time data, per TfL evidence)

**Communication Frequency**: Quarterly operator forum, monthly technical working groups

**Preferred Channel**: Industry working group + bilateral meetings for major operators

---

## Change Impact Assessment

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Network Rail | Darwin feed consumed by NRE and third parties separately | Darwin integrated into unified multimodal API | MEDIUM | LOW | Position as extension, not replacement |
| National Highways | NTIS/DATEX II consumed by traffic info providers | Road data integrated with public transport | MEDIUM | LOW | Demonstrate modal shift analysis value |
| Large Bus Operators | BODS compliance, data to Traveline | Single submission point, enhanced quality monitoring | LOW | MEDIUM | Demonstrate ridership benefit, reduce reporting burden |
| Small Bus Operators | Variable BODS compliance, limited real-time capability | Real-time AVL required, support provided | HIGH | HIGH | Grant funding for AVL equipment, technical support programme |
| Combined Authorities | Building separate regional data platforms | Use national platform with regional customisation | MEDIUM | MEDIUM | Co-design, extension API for local needs |
| Passengers | Multiple apps for different modes | Single integrated multimodal information source | LOW | LOW | User research, beta testing |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Small Bus Operator Non-Compliance

**Related Stakeholders**: Small/medium bus operators (~500)

**Risk Description**: Smaller operators lack technical capability and financial resources to provide real-time vehicle tracking data, leaving significant gaps in bus data coverage, particularly in rural areas.

**Impact on Goals**: G-2 (bus data quality)

**Probability**: HIGH

**Impact**: MEDIUM

**Mitigation Strategy**: DfT grant funding for AVL equipment; simplified data submission tools; partnerships with AVL technology providers for discounted rates

**Contingency Plan**: Accept lower real-time coverage for small operators initially; use timetable data with confidence indicators

---

### Risk R-2: TfL Opting Out of National Platform

**Related Stakeholders**: Transport for London

**Risk Description**: TfL considers its Unified API superior to the national platform and declines to participate, creating a gap in the national picture for London (the UK's largest transport network).

**Impact on Goals**: G-1 (unified platform), G-3 (disruption management)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Position national platform as complementary (consuming TfL API rather than replacing it); ensure TfL data standards are accommodated; demonstrate value of national integration for cross-boundary journeys

**Contingency Plan**: Consume TfL Unified API as an external source; accept London as a federated node rather than fully integrated

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Data standards and formats | Product Manager | SRO | Network Rail, NH, Bus Ops, TfL | Combined Authorities |
| API design and access model | Technical Lead | DfT CDIO | GDS, Traveline, OS | CDDO |
| Bus data quality thresholds | DfT Bus Policy | SRO | Bus operators, Traffic Comms | Combined Authorities |
| Architecture decisions | Technical Lead | DfT CDIO | NR, NH, GDS | CDDO |
| Go/No-go for launch | SRO | Permanent Secretary | All stakeholders | All |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day)
2. **Level 2**: Programme Board (scope, timeline, operator disputes)
3. **Level 3**: SRO / Permanent Secretary (strategic, cross-organisational)
4. **Level 4**: Secretary of State (inter-departmental, regulatory intervention)

---

## Validation & Sign-off

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| Network Rail | PENDING | | PENDING |
| National Highways | PENDING | | PENDING |
| TfL | PENDING | | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Bus Services Act 2017 | Legislation | legislation.gov.uk | Open data requirements for bus operators | N/A — external reference |
| BODS Technical Guidance | Standard | DfT | TransXChange, SIRI-VM specifications | N/A — external reference |
| NaPTAN Dataset | Dataset | DfT | National stop/station identifiers | N/A — external reference |
| Net Zero Transport Plan | Strategy | DfT | Modal shift targets | N/A — external reference |
| Plan for Rail (GBR) | White Paper | DfT | Rail reform and data governance | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart Transport Network (Project 002)
**Model**: Claude Opus 4.6
