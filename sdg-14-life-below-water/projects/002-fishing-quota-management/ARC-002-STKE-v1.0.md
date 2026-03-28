# Stakeholder Drivers & Goals Analysis: Fishing Quota Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Fishing Quota Management (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Fishing Quota Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Quota Programme Board, MMO, DEFRA Marine, ICES Advisory, Fishing Industry |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Fishing Quota Management system, their underlying drivers, how these manifest into goals, and the measurable outcomes that will satisfy those goals. The system will replace the MMO's current catch reporting and quota allocation processes with a digital platform supporting electronic logbook (eLogbook) submission, real-time quota monitoring, and automated allocation management under the Fisheries Act 2020.

### Key Findings

The Fishing Quota Management programme faces a fundamental tension between the fishing industry's demand for simplicity, speed, and fairness in quota allocation, and the regulatory complexity introduced by the Fisheries Act 2020's eight fisheries objectives. Post-Brexit, the UK has independent quota-setting responsibility for the first time, creating both opportunity (tailored UK allocation) and risk (bilateral negotiation complexity with EU and Norway). The strongest alignment is around reducing the administrative burden on fishers — both the industry and MMO want faster, simpler catch reporting. The most significant conflict is between the small-scale fleet (<10m vessels, ~4,600 boats) seeking greater quota access and the large-scale fleet (>10m, ~1,400 vessels) that holds the majority of existing quota allocation.

### Critical Success Factors

- Maintain uninterrupted quota monitoring and catch recording throughout transition — any data gap risks overfishing beyond Total Allowable Catch (TAC)
- Achieve adoption by the under-10m fleet, which currently submits paper-based catch returns with significant time lag
- Integrate with ICES stock assessment data to enable science-based quota allocation
- Support the new Fisheries Management Plans required under the Fisheries Act 2020
- Deliver a system that works reliably in ports and harbours with limited connectivity

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for digital catch reporting and reduced administrative burden. Significant tensions between small-scale and large-scale fleet interests on quota allocation, between speed of reporting and data accuracy, and between open quota data and commercial sensitivity. The devolved administrations add complexity through different quota management arrangements.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Fisheries Minister | Ministerial sponsor | HIGH | HIGH | Manage Closely — Ministerial briefings |
| MMO Chief Executive | Organisation sponsor | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Quota Management | Programme sponsor (MMO) | HIGH | HIGH | Manage Closely — Weekly programme board |
| MMO Head of Quota Management | Quota allocation operations | HIGH | HIGH | Manage Closely — Operational requirements |
| MMO Head of Compliance | Enforcement and monitoring | HIGH | HIGH | Manage Closely — Compliance data needs |
| MMO CDIO | Digital strategy | HIGH | HIGH | Manage Closely — Architecture governance |
| Cefas Stock Assessment Team | Scientific stock advice | HIGH | HIGH | Manage Closely — Scientific data integration |
| DEFRA Marine Policy | Fisheries policy and legislation | HIGH | MEDIUM | Keep Satisfied — Policy requirements |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| ICES (International Council for the Exploration of the Sea) | Advisory body | Scientific advice provider | HIGH | MEDIUM |
| NFFO | Large-scale fleet representative | Industry body | HIGH | HIGH |
| NUTFA (New Under Ten Fishermen's Association) | Small-scale fleet representative | Industry body | MEDIUM | HIGH |
| Producer Organisations (POs) | Quota management bodies | Quota holders | HIGH | HIGH |
| IFCAs | Statutory bodies | Inshore fisheries management | MEDIUM | HIGH |
| Devolved Administrations (Scotland, Wales, NI) | Scottish Government Marine Directorate, Welsh Government | Separate quota management | HIGH | HIGH |
| EU Commission (DG MARE) | European Union | Annual fisheries negotiations | HIGH | MEDIUM |
| Norway (Directorate of Fisheries) | Norway | Joint stock negotiations | MEDIUM | MEDIUM |
| Fish processors and merchants | Private sector | Supply chain | LOW | HIGH |
| Seafish | Industry body | Economics and training | LOW | MEDIUM |
| Environmental NGOs (MCS, Greenpeace, ClientEarth) | Conservation bodies | Sustainability advocacy | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • DEFRA Marine     │  • Fisheries Minister│
        │    Policy           │  • MMO CEO          │
        │  • ICES             │  • SRO              │
        │  • EU DG MARE       │  • MMO Quota Head   │
        │  • Devolved Admins  │  • MMO Compliance   │
 P      │                     │  • MMO CDIO         │
 O      │                     │  • Cefas Stock Team │
 W      │                     │  • NFFO             │
 E      │                     │  • Producer Orgs    │
 R      ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Norway           │  • NUTFA            │
        │  • Seafish          │  • IFCAs            │
        │                     │  • Fish processors  │
        │                     │  • Environmental    │
        │                     │    NGOs             │
        │                     │  • Coastal          │
        │                     │    communities      │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Fisheries Minister — Delivering the Fisheries Act 2020 Vision

**Stakeholder**: DEFRA Fisheries Minister

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate that post-Brexit independent fisheries management delivers tangible benefits — fairer quota allocation, sustainable stocks, reduced bureaucracy for fishers, and a thriving UK fishing industry.

**Context & Background**:
The Fisheries Act 2020 received Royal Assent as a flagship post-Brexit legislation, establishing eight fisheries objectives including sustainability, precautionary approach, ecosystem, scientific evidence, bycatch, equal access, national benefit, and climate change. The Minister needs a digital platform that enables Fisheries Management Plans (FMPs), supports evidence-based quota decisions, and demonstrates that UK-controlled fisheries management is an improvement over the EU Common Fisheries Policy. Parliamentary and media scrutiny of post-Brexit fishing arrangements remains intense.

**Driver Intensity**: CRITICAL

**Enablers**:

- Digital platform demonstrating modern fisheries management
- Real-time quota utilisation dashboards visible to Parliament
- Evidence of reduced discards and improved stock sustainability
- Positive industry feedback on reduced bureaucratic burden

**Blockers**:

- Annual fisheries negotiations with EU creating uncertainty in quota volumes
- Industry dissatisfaction with quota allocation perceived as unfair
- Overfishing incidents that attract media attention
- System delivery delays undermining credibility

**Related Stakeholders**: MMO CEO (delivery), NFFO/NUTFA (industry satisfaction), Cefas (scientific evidence), EU DG MARE (negotiations)

---

### SD-2: MMO Head of Quota Management — Accurate, Timely Quota Monitoring

**Stakeholder**: MMO Head of Quota Management

**Driver Category**: OPERATIONAL

**Driver Statement**: Replace manual catch return processing with real-time digital catch reporting, enabling accurate quota monitoring that prevents overshoot and supports timely quota allocation decisions.

**Context & Background**:
The MMO currently manages approximately 100 quota stocks for England. Catch data arrives through a mix of electronic logbooks (for over-10m vessels) and paper-based catch returns (under-10m fleet, submitted monthly). Paper returns create a 4-6 week data lag, meaning quota utilisation calculations are always behind reality. This has led to precautionary early quota closures that frustrate the industry, or late closures that risk overshoot. The under-10m fleet accounts for approximately 4,600 vessels and their catches are poorly quantified in near-real-time.

**Driver Intensity**: CRITICAL

**Enablers**:

- Mandatory electronic catch reporting for all vessel sizes
- Real-time quota utilisation dashboard with automated alerts at threshold levels (70%, 85%, 95%)
- Integration with VMS/AIS for effort validation
- Automated monthly quota allocation reconciliation

**Blockers**:

- Legislative change required for mandatory eLogbook for under-10m vessels
- Connectivity challenges in remote ports and at sea
- Industry resistance to increased reporting obligations for small vessels
- Legacy data migration from current quota management systems

**Related Stakeholders**: NUTFA (under-10m fleet), NFFO (over-10m fleet), Cefas (stock data), IFCAs (inshore quota)

---

### SD-3: NFFO — Fair, Transparent Quota Allocation for the Commercial Fleet

**Stakeholder**: National Federation of Fishermen's Organisations

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Ensure the digital quota management system maintains the existing Fixed Quota Allocation (FQA) system's stability while providing transparency in allocation decisions, rapid quota trading, and reduced reporting burden.

**Context & Background**:
NFFO represents the over-10m fleet and Producer Organisations that hold the majority of UK quota through the FQA system. Their members are commercially dependent on predictable, tradable quota allocations. They want the system to streamline quota trading between POs, reduce eLogbook submission complexity, and provide clear sight of quota availability per species per area. They are concerned that digital transformation might be used to fundamentally change the allocation system (redistributing quota from large-scale to small-scale fleet).

**Driver Intensity**: HIGH

**Enablers**:

- Digital quota trading platform enabling instant PO-to-PO transfers
- Simplified eLogbook submission with species auto-identification
- Real-time quota balance visibility per vessel and per PO
- Historical catch data accessible for business planning

**Blockers**:

- Any system change that threatens FQA stability
- Complex reporting requirements added digitally
- System downtime during fishing operations
- Data used to challenge existing quota allocations

**Related Stakeholders**: Producer Organisations (quota holders), MMO Quota Head (allocation), NUTFA (competing interests)

---

### SD-4: NUTFA — Greater Quota Access for Small-Scale Fleet

**Stakeholder**: New Under Ten Fishermen's Association

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Use the digital platform transition to address the historic imbalance in quota allocation, giving the under-10m fleet (which comprises 77% of the UK fleet by number) greater visibility, fairer quota access, and a voice in fisheries management.

**Context & Background**:
The under-10m fleet comprises approximately 4,600 vessels but holds only about 4% of UK quota by value. These vessels are owner-operated, serve coastal communities, and supply local fish markets. NUTFA sees the new digital system as an opportunity to improve the visibility of small-scale catches (currently under-reported due to paper returns), demonstrate the fleet's economic and social contribution, and advocate for quota reallocation under the Fisheries Act's "national benefit" objective.

**Driver Intensity**: HIGH

**Enablers**:

- Simple mobile catch reporting app that works in harbour with limited connectivity
- Transparent quota utilisation data showing all fleet segments
- Data demonstrating small-scale fleet economic and social value
- Digital platform for under-10m quota pool management

**Blockers**:

- Complex digital reporting requirements unsuitable for small vessels
- Cost of digital equipment for owner-operators with thin margins
- System designed around large-scale fleet workflows
- Data used to justify further restrictions on small-scale fishing

**Related Stakeholders**: NFFO (competing quota interests), IFCAs (inshore management), coastal communities (economic dependency)

---

### SD-5: Cefas Stock Assessment Team — Science-Based Quota Decisions

**Stakeholder**: Cefas Stock Assessment Team

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Ensure the quota management system integrates ICES stock assessment data and UK scientific survey results, enabling quota allocations that are based on the best available scientific evidence as required by the Fisheries Act 2020.

**Context & Background**:
Cefas contributes to ICES stock assessments for North-East Atlantic fish stocks. The Fisheries Act 2020 establishes a "scientific evidence" objective requiring quota decisions to be based on the best available science. Currently, stock assessment outputs (Maximum Sustainable Yield estimates, biomass trends, recruitment data) are shared with MMO via spreadsheets and reports. A direct data pipeline from Cefas stock assessment models to the quota management system would enable faster, more transparent linkage between scientific advice and quota decisions.

**Driver Intensity**: HIGH

**Enablers**:

- API integration between Cefas stock assessment databases and MMO quota system
- Quota decision audit trail showing scientific evidence considered
- Real-time catch data feeding back into stock assessment models
- Dashboard linking quota decisions to MSY reference points

**Blockers**:

- Political pressure to set quotas above scientific advice
- Different data formats between ICES, Cefas, and MMO systems
- Complexity of multi-species, mixed-fishery stock interactions
- Uncertainty in stock assessments for data-limited species

**Related Stakeholders**: ICES (international advice), DEFRA Marine Policy (fisheries objectives), Environmental NGOs (sustainability)

---

### SD-6: Producer Organisations — Efficient Quota Pool Management

**Stakeholder**: Producer Organisations (approximately 20 POs in England)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Streamline quota pool management with real-time visibility of member catches against PO quota holdings, automated quota swap/trade processing, and reduced administrative overhead.

**Context & Background**:
POs manage quota on behalf of their member vessels. They allocate quota to members, monitor uptake, arrange quota swaps and trades with other POs, and reconcile at year-end. This is currently a manual, spreadsheet-heavy process with significant reconciliation effort. POs need a system that shows real-time catch versus allocation for all members, enables instant quota transfers, and automates regulatory reporting.

**Driver Intensity**: MEDIUM

**Enablers**:

- Real-time PO dashboard showing member catch vs allocation by species
- Digital quota trading marketplace between POs
- Automated catch reconciliation with MMO records
- Annual reporting automation

**Blockers**:

- System designed without PO workflow consideration
- Loss of PO autonomy in quota management decisions
- Data sharing between POs revealing competitive information
- System complexity exceeding PO administrative capacity

**Related Stakeholders**: NFFO (PO federation), MMO Quota Head (allocation), vessel skippers (data submitters)

---

## Driver-to-Goal Mapping

### Goal G-1: Real-Time Quota Monitoring

**Derived From Drivers**: SD-2, SD-3, SD-6

**Goal Statement**: Provide real-time quota utilisation monitoring for all quota stocks, with automated alerts when utilisation reaches warning thresholds.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Catch data latency (over-10m) | 24 hours | <2 hours | 6 months |
| Catch data latency (under-10m) | 4-6 weeks | <48 hours | 12 months |
| Quota utilisation accuracy | +-15% | +-3% | 12 months |

---

### Goal G-2: Digital Catch Reporting for All Fleet Segments

**Derived From Drivers**: SD-2, SD-4

**Goal Statement**: Deliver electronic catch reporting capability for all UK fishing vessels, including a simple mobile app for the under-10m fleet.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Under-10m vessels submitting electronically | 5% | 80% | 18 months |
| Mean catch report submission time | 25 minutes (paper) | 5 minutes (digital) | 12 months |
| Paper catch returns received | 55,000/year | <5,500/year | 18 months |

---

### Goal G-3: Science-Linked Quota Allocation

**Derived From Drivers**: SD-5, SD-1

**Goal Statement**: Integrate ICES stock assessment data with quota allocation processes, providing an auditable link between scientific advice and quota decisions.

**Success Metrics**:

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Quota stocks with linked scientific advice | 40% | 95% | 12 months |
| Quota decisions with documented science rationale | 60% | 100% | 12 months |

---

## Conflict Analysis

### Conflict 1: Large-Scale vs Small-Scale Fleet Quota Access

**Stakeholders**: NFFO (SD-3) vs NUTFA (SD-4)

**Nature**: NFFO wants to preserve the FQA system. NUTFA wants digital transparency to build the case for reallocation. Both sides view the new system through this lens.

**Resolution Strategy**: COMPROMISE — System provides transparent data to all fleet segments without prejudging allocation policy. Quota allocation methodology remains a policy decision outside the system scope. System supports multiple allocation models including FQA and pool-based.

### Conflict 2: Reporting Simplicity vs Data Granularity

**Stakeholders**: NUTFA/fishers (SD-4) vs Cefas/MMO (SD-5, SD-2)

**Nature**: Fishers want minimal reporting burden. Scientists and regulators need detailed, accurate data (species, weight, area, gear type, bycatch).

**Resolution Strategy**: INNOVATE — Use pre-filled forms based on vessel profile, recent fishing area (from VMS), and gear registered. Only require confirmation/correction rather than full manual entry. Species identification assistance via photograph-based AI suggestions.

---

## Communication Plan

| Stakeholder Group | Method | Frequency | Owner |
|-------------------|--------|-----------|-------|
| Programme Board (SRO, MMO, DEFRA, Cefas) | Board meeting | Fortnightly | SRO |
| Fisheries Minister | Written briefing | Monthly | SRO |
| Large-scale fleet (NFFO, POs) | Industry liaison group | Monthly | Service Owner |
| Small-scale fleet (NUTFA) | Harbour roadshows, digital comms | Monthly | Product Manager |
| IFCAs | Technical working group | Quarterly | Delivery Manager |
| Devolved administrations | Cross-admin coordination | Quarterly | DEFRA Marine Policy |
| Environmental NGOs | Stakeholder newsletter | Quarterly | Communications |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Fisheries Act 2020 | Legislation | UK Parliament | Eight fisheries objectives, FMP framework | legislation.gov.uk |
| Joint Fisheries Statement | Policy | UK Fisheries Administrations | Joint approach to fisheries management | gov.uk |
| ICES Advice | Scientific | ICES | Stock assessment and TAC recommendations | ices.dk |
| Fisheries Management Plans | Policy | DEFRA/MMO | Species-specific management plans | gov.uk |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Fishing Quota Management
**Model**: Claude Opus 4.6
