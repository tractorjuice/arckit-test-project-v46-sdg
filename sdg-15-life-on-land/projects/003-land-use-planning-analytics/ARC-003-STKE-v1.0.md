# Stakeholder Drivers & Goals Analysis: Land Use Planning Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Land Use Planning Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Land Use Planning Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, DEFRA Digital, Natural England, Environment Agency, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Land Use Planning Analytics platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Land Use Planning Analytics platform serves a critical evidence-gathering function — converting satellite imagery, environmental surveys, and administrative records into actionable intelligence about land use change across England. The strongest alignment exists around the need for systematic, automated land use change detection to replace fragmented, reactive monitoring. The most significant tension is between DEFRA's desire for comprehensive monitoring of all land use types (enabling evidence-based policy) and the concerns of farming and landowning stakeholders about surveillance and the regulatory consequences of detected land use changes (particularly conversion of permanent grassland, peatland drainage, or unauthorised development).

### Critical Success Factors

- Establish automated Sentinel-2 satellite imagery processing pipeline detecting land use changes within 30 days of occurrence
- Integrate with at least 5 authoritative land use datasets (UKCEH Land Cover Map, National Forest Inventory, Agricultural Land Classification, SSSI boundaries, Priority Habitat Inventory)
- Deliver actionable environmental impact analytics to support Environmental Improvement Plan target reporting
- Maintain public trust through transparent methodology and proportionate use of surveillance capabilities

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the value of better land use intelligence for policy-making. Significant tensions around data access rights, privacy implications of systematic land monitoring, and the regulatory consequences that may follow from detected changes. The farming sector is particularly sensitive to perceived surveillance.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Chief Scientific Adviser | Scientific leadership | HIGH | HIGH | Manage Closely — Methodology validation, evidence standards |
| SRO, Land Use Analytics | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DEFRA Environmental Analysis Director | Policy evidence lead | HIGH | HIGH | Manage Closely — Analytics requirements, EIP reporting |
| DEFRA SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA, surveillance proportionality |
| DEFRA Data Governance Board | Data standards and sharing | MEDIUM | HIGH | Keep Informed — Data sharing agreements, privacy |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| Natural England | NDPB | Environmental designations, habitat monitoring | HIGH | HIGH |
| Environment Agency | NDPB | Environmental regulation, land contamination | HIGH | HIGH |
| UK Centre for Ecology & Hydrology (UKCEH) | Research council | Land Cover Map, ecological modelling | MEDIUM | HIGH |
| Rural Payments Agency (RPA) | Executive agency | Agricultural land data, ELM scheme monitoring | HIGH | HIGH |
| Local Planning Authorities | Local government | Planning enforcement, Green Belt monitoring | MEDIUM | HIGH |
| National Farmers' Union (NFU) | Industry body | Agricultural sector representation | HIGH | HIGH |
| Country Land and Business Association (CLA) | Industry body | Landowner representation | MEDIUM | HIGH |
| Ordnance Survey | Government company | Geospatial data, MasterMap | MEDIUM | MEDIUM |
| UK Space Agency | Government agency | Sentinel programme, earth observation | LOW | MEDIUM |
| Joint Nature Conservation Committee (JNCC) | NDPB | UK-wide nature conservation | MEDIUM | HIGH |
| Office for National Statistics (ONS) | Government department | Natural capital accounts | MEDIUM | MEDIUM |
| Forestry Commission | NDPB | Woodland change detection | MEDIUM | HIGH |
| Information Commissioner's Office (ICO) | Regulator | Privacy, proportionality of surveillance | HIGH | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end analytics service | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control, assessment gates |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • DEFRA Chief Sci  │
        │  • CDDO             │  • SRO              │
        │  • DEFRA SIRO       │  • Chief Digital Off│
        │  • ICO              │  • Env Analysis Dir │
        │                     │  • Natural England  │
 P      │                     │  • Environment Agcy │
 O      │                     │  • RPA              │
 W      │                     │  • NFU              │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • UK Space Agency  │  • UKCEH            │
        │  • ONS              │  • LPAs             │
        │  • Ordnance Survey  │  • CLA              │
        │                     │  • JNCC             │
        │                     │  • Forestry Comm    │
        │                     │  • Data Gov Board   │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Environmental Analysis — Evidence-Based Environmental Policy

**Stakeholder**: DEFRA Environmental Analysis Director

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Deliver a comprehensive, near-real-time evidence base on land use change across England to support Environmental Improvement Plan (EIP) target reporting, 25 Year Environment Plan progress assessment, and evidence-based environmental policy-making.

**Context & Background**:
DEFRA is legally required to report progress against Environmental Improvement Plan targets (set under the Environment Act 2021) on an annual basis. Currently, land use change data is fragmented across multiple organisations (UKCEH Land Cover Map updated every 5-7 years, National Forest Inventory on a 10-year cycle, agricultural census annually but self-reported). The Office for Environmental Protection (OEP) has criticised the government for insufficient monitoring data to demonstrate progress on environmental targets. Without systematic, timely land use change intelligence, DEFRA cannot adequately assess whether policies are working or where intervention is needed.

**Driver Intensity**: CRITICAL

**Enablers**:

- Automated satellite imagery analysis providing land use change detection within 30 days
- Integration of multiple authoritative datasets into a unified analytical platform
- Standardised environmental impact metrics aligned with EIP targets
- Automated annual reporting dashboards for EIP target progress

**Blockers**:

- Data fragmentation across organisations with different standards and update cycles
- Cloud processing costs for large-scale satellite imagery analysis
- Methodological challenges in distinguishing land use change from seasonal variation
- Political sensitivity of reporting environmental decline

**Related Stakeholders**: OEP (environmental scrutiny), Natural England (habitat monitoring), JNCC (biodiversity reporting), ONS (natural capital accounts)

---

### SD-2: NFU / Farming Sector — Proportionate Monitoring Without Surveillance

**Stakeholder**: National Farmers' Union (NFU) and Country Land and Business Association (CLA)

**Driver Category**: PRIVACY / OPERATIONAL

**Driver Statement**: Ensure land use monitoring is proportionate, transparent, and does not create a surveillance infrastructure that is used punitively against farmers and landowners, with clear governance over how detected land use changes are used in regulatory enforcement.

**Context & Background**:
The farming sector is highly sensitive to government monitoring of agricultural land, particularly in the context of Environmental Land Management (ELM) schemes where payments are conditional on environmental outcomes. Farmers fear that automated satellite monitoring will be used to detect and penalise non-compliance — creating a "Big Brother" dynamic that undermines the collaborative approach intended by ELM. The NFU has publicly stated that monitoring must be proportionate and support farmers rather than police them. Historical experience with cross-compliance inspections under the Common Agricultural Policy created lasting distrust.

**Driver Intensity**: HIGH

**Enablers**:

- Transparent methodology published openly, with farmer consultation on monitoring approaches
- Clear governance framework limiting how change detection data can be used in enforcement
- Farmer access to their own land use data to self-assess compliance
- Monitoring data used primarily for support and early intervention, not penalty

**Blockers**:

- Perception of satellite surveillance as intrusive and punitive
- Lack of transparency about how monitoring data feeds into regulatory enforcement
- Historical distrust from CAP cross-compliance inspection regime
- Concerns about data accuracy and false positive change detections

**Related Stakeholders**: RPA (ELM scheme monitoring), DEFRA Policy (regulatory framework), ICO (privacy proportionality)

---

### SD-3: Natural England — Habitat Condition and Protected Site Monitoring

**Stakeholder**: Natural England

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Establish automated monitoring of SSSI condition, Priority Habitat extent, and protected species habitats using satellite-derived land use change data, reducing reliance on infrequent manual site condition assessments.

**Context & Background**:
Natural England is responsible for monitoring 4,127 SSSIs covering approximately 8% of England's land area. Current condition assessment relies on manual site visits on a 6-year cycle — many sites have not been assessed for over a decade. Natural England lacks the field staff to maintain adequate monitoring coverage. Satellite-based change detection could provide early warning of habitat deterioration, illegal activity, and condition change between manual assessments.

**Driver Intensity**: HIGH

**Enablers**:

- Automated change detection alerts for SSSI boundaries and buffer zones
- Habitat condition proxy indicators derived from vegetation indices (NDVI, EVI)
- Integration with Natural England's Designated Sites system
- Priority-based field assessment triggered by satellite-detected changes

**Blockers**:

- Satellite resolution limitations for fine-grained habitat condition assessment
- Difficulty distinguishing between different habitat types from satellite data alone
- Integration complexity with Natural England's legacy Designated Sites database
- Validation requirement — satellite detections must be ground-truthed before action

**Related Stakeholders**: JNCC (UK-wide coordination), UKCEH (methodology), Environment Agency (water-dependent habitats), Forestry Commission (woodland)

---

### SD-4: RPA — ELM Scheme Monitoring and Compliance

**Stakeholder**: Rural Payments Agency

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Utilise satellite-based land use change detection to support Environmental Land Management (ELM) scheme monitoring, enabling risk-based compliance assessment and reducing the cost and burden of physical farm inspections.

**Context & Background**:
The RPA administers ELM schemes (Sustainable Farming Incentive, Countryside Stewardship, Landscape Recovery) which make payments conditional on environmental outcomes. Current compliance monitoring relies on costly physical inspections covering a small percentage of agreements. Satellite monitoring could enable risk-based targeting of inspections, reducing costs while improving coverage. The EU already uses satellite monitoring for Common Agricultural Policy compliance in several member states.

**Driver Intensity**: MEDIUM

**Enablers**:

- Automated detection of agreement boundary and land use changes
- Risk-based inspection targeting using satellite-derived indicators
- Integration with RPA's Rural Payments data and agreement management systems
- Farmer self-service access to satellite imagery for their own holdings

**Blockers**:

- Accuracy requirements for regulatory enforcement (legal challenge risk from false positives)
- Farmer resistance to satellite-based compliance monitoring (SD-2 tensions)
- Integration with RPA legacy systems and data standards
- Regulatory framework for using satellite evidence in enforcement decisions

---

## Driver-to-Goal Mapping

### Goal G-1: Automated Land Use Change Detection Pipeline

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: DEFRA Chief Scientific Adviser

**Goal Statement**: Establish an automated satellite imagery processing pipeline that detects land use changes across England within 30 days of occurrence, with a detection accuracy of >90% for major land use transitions, operational within 12 months.

**Success Metrics**:

- **Primary Metric**: Land use change detection within 30 days of occurrence (from years/never)
- **Secondary Metrics**:
  - Detection accuracy > 90% for major transitions (validated against ground truth)
  - False positive rate < 5% (to maintain stakeholder trust)
  - Processing throughput: Full England coverage per Sentinel-2 revisit cycle (5 days)

---

### Goal G-2: Unified Environmental Analytics Platform

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: DEFRA Environmental Analysis Director

**Goal Statement**: Integrate at least 5 authoritative land use datasets into a unified analytical platform providing standardised environmental impact metrics for EIP target reporting, delivering the first automated annual land use change assessment within 18 months.

**Success Metrics**:

- **Primary Metric**: Number of authoritative datasets integrated (target: 5+)
- **Secondary Metrics**:
  - EIP target reporting automated for at least 3 apex targets
  - Time to produce annual land use change assessment reduced from 12 months to 4 weeks
  - Platform used by at least 50 DEFRA analysts within 12 months

---

### Goal G-3: Transparent Monitoring with Farmer Trust

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: SRO, Land Use Analytics

**Goal Statement**: Establish a transparent governance framework for land use monitoring that enables proportionate compliance support, with farmer access to their own data and published methodology, achieving >60% farmer trust score in annual survey within 24 months.

**Success Metrics**:

- **Primary Metric**: Farmer trust score > 60% in annual survey
- **Secondary Metrics**:
  - 100% of methodology published and peer-reviewed
  - Farmer self-service data portal with > 10,000 registered users
  - DPIA approved by ICO with proportionality confirmed

---

## Goal-to-Outcome Mapping

### Outcome O-1: Evidence-Based Environmental Policy and Target Delivery

**Supported Goals**: G-1, G-2

**Outcome Statement**: DEFRA has near-real-time intelligence on land use change across England, enabling evidence-based policy adjustments and demonstrable progress reporting against Environmental Improvement Plan targets.

**Business Value**:

- **Financial Impact**: £3M annual saving from automated monitoring replacing manual surveys, avoided costs from early detection of environmental damage
- **Strategic Impact**: Credible environmental target reporting, OEP scrutiny satisfied
- **Operational Impact**: Policy interventions targeted at areas of actual change rather than assumptions
- **Customer Impact**: Public confidence in government environmental commitments

### Outcome O-2: Proportionate, Trusted Environmental Monitoring

**Supported Goals**: G-1, G-3

**Outcome Statement**: Land use monitoring is established as a trusted, proportionate tool that supports environmental outcomes while respecting landowner privacy, with transparent governance and farmer self-service access.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA Env Analysis | SD-1 | Evidence-based policy | G-1, G-2 | Change detection, unified analytics | O-1 | Evidence-based policy |
| NFU / Farming sector | SD-2 | Proportionate monitoring | G-3 | Transparent governance, farmer trust | O-2 | Trusted monitoring |
| Natural England | SD-3 | Habitat monitoring | G-1 | Automated detection | O-1 | Environmental evidence |
| RPA | SD-4 | ELM compliance | G-1, G-3 | Detection + governance | O-1, O-2 | Efficient compliance |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DEFRA (SD-1) and Natural England (SD-3) want comprehensive monitoring capability, but NFU (SD-2) fears surveillance and punitive use of detected changes.
  - **Resolution Strategy**: Governance framework with clear data use limitations — monitoring data used for support and early intervention by default, enforcement only through existing regulatory processes with human review. Farmer self-service access to their own data builds trust through transparency.

- **Conflict 2**: RPA (SD-4) wants to use satellite data for ELM compliance, but accuracy limitations create legal risk if satellite evidence alone triggers enforcement.
  - **Resolution Strategy**: Satellite data used for risk-based inspection targeting (not as direct evidence). All enforcement actions require ground-truth verification. Published accuracy metrics and appeal mechanisms.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DEFRA Finance | SRO | HM Treasury, CDDO | All stakeholders |
| Monitoring methodology | DEFRA Chief Scientist | SRO | UKCEH, NE, Forest Research | NFU, CLA |
| Data governance and privacy | Data Governance Board | DEFRA SIRO | ICO, NFU | All users |
| Architecture decisions | Technical Lead | Chief Digital Officer | Security, UKCEH | Business |
| Data sharing agreements | Data Governance Board | SRO | NE, EA, RPA, OS | All data consumers |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environmental Improvement Plan 2023 | Policy | DEFRA | Apex environmental targets | N/A |
| Environment Act 2021 | Legislation | legislation.gov.uk | Environmental target framework | N/A |
| UK GDPR | Regulation | ICO | Data protection, proportionality | N/A |
| Sentinel-2 Technical Guide | Technical | ESA/Copernicus | Satellite imagery specifications | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Land Use Planning Analytics
**Model**: Claude Opus 4.6
