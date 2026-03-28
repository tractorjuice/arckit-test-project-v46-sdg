# Stakeholder Drivers & Goals Analysis: Forestry Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Forestry Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Forestry Management System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | FC Programme Board, DEFRA, Forestry Commission, Woodland Trust, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Forestry Management System, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The Forestry Management System programme operates at the intersection of ambitious woodland creation targets (England Trees Action Plan target of 7,500 hectares per year by 2024/25, not yet achieved) and the operational reality of processing felling licences, managing grant schemes, and maintaining the National Forest Inventory across a fragmented digital landscape. The strongest alignment exists around modernising grant application and felling licence processes — both the Forestry Commission and landowners agree current systems are slow and paper-heavy. The most significant conflict is between the urgency of accelerating woodland creation to meet climate and biodiversity targets and the need for rigorous environmental impact assessment to prevent inappropriate planting (monoculture conifers on peatland, afforestation of valuable grassland habitats).

### Critical Success Factors

- Digitise the felling licence workflow end-to-end to reduce processing time from 13 weeks to 4 weeks
- Enable real-time National Forest Inventory updates through integrated remote sensing and field survey data
- Streamline woodland creation grant applications (England Woodland Creation Offer, Countryside Stewardship) to accelerate planting rates
- Integrate UK Woodland Carbon Code verification to enable carbon credit certification alongside forestry management
- Maintain interoperability with DEFRA rural payments systems and Natural England environmental designations

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong alignment on the need for digital modernisation and faster processing. Moderate tension between woodland creation acceleration (FC, DEFRA policy) and ecological safeguards (Natural England, conservation charities concerned about inappropriate planting). Carbon market integration creates additional complexity around verification standards and financial accountability.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Forestry Commission Chair | FC Board | HIGH | HIGH | Manage Closely — Board briefings, strategic direction |
| FC Chief Executive | Operational leadership | HIGH | HIGH | Manage Closely — Programme board, delivery oversight |
| SRO, Forestry Digital | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| FC Chief Forester | Professional forestry standards | HIGH | HIGH | Manage Closely — Standards compliance, professional practice |
| FC Operations Director | Field operations, felling licences | HIGH | HIGH | Manage Closely — Operational readiness, process redesign |
| FC Digital Director | IT strategy and delivery | HIGH | HIGH | Manage Closely — Architecture governance, digital strategy |
| DEFRA SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| FC Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| FC Forest Management Directors (Area) | Regional operations | MEDIUM | HIGH | Keep Informed — Regional implementation, field testing |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DEFRA | Parent department | Policy, funding | HIGH | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Natural England | NDPB | Environmental designations, SSSI consent | HIGH | HIGH |
| Woodland Trust | Charity | Woodland creation advocacy, landowner support | MEDIUM | HIGH |
| Confor (Confederation of Forest Industries) | Industry body | Timber industry representation | MEDIUM | HIGH |
| Private woodland owners | Private sector | Felling licence applicants, grant recipients | LOW | HIGH |
| Landowners / Farmers | Private sector | Woodland creation land providers | LOW | HIGH |
| UK Woodland Carbon Code Registry | Voluntary standard | Carbon credit verification | MEDIUM | HIGH |
| Rural Payments Agency | Executive agency | Grant payment processing | MEDIUM | MEDIUM |
| Environment Agency | NDPB | Flood risk, water quality | MEDIUM | MEDIUM |
| Ordnance Survey | Government company | Geospatial data | LOW | MEDIUM |
| Forest Research | FC research agency | Evidence base, inventory methods | MEDIUM | HIGH |
| Local Authorities | Local government | Tree Preservation Orders, planning | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for Forestry Digital outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end forestry services and user outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed — Security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • FC Chair         │
        │  • CDDO             │  • FC Chief Exec    │
        │  • DEFRA SIRO       │  • SRO              │
        │  • FC Finance Dir   │  • FC Chief Forester│
        │  • SSRO / DSO       │  • FC Operations Dir│
 P      │                     │  • FC Digital Dir   │
 O      │                     │  • DEFRA            │
 W      │                     │  • Natural England  │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • DDaT Lead        │  • Woodland Trust   │
        │  • Ordnance Survey  │  • Confor           │
        │  • Local Authorities│  • Woodland owners  │
        │                     │  • Landowners       │
        │                     │  • Carbon Code      │
        │                     │  • Forest Research  │
        │                     │  • FC Area Directors│
        │                     │  • Env Agency       │
        │                     │  • RPA              │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA / FC Chair — Accelerating Woodland Creation to Meet National Targets

**Stakeholder**: DEFRA Secretary of State / FC Chair

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Accelerate woodland creation rates to meet the England Trees Action Plan target of 7,500 hectares per year, demonstrating progress on climate change mitigation (net zero by 2050) and biodiversity recovery (30by30), while the current rate falls significantly short.

**Context & Background**:
The England Trees Action Plan 2021 set ambitious woodland creation targets, but England has consistently underdelivered — planting rates have typically been 2,000-3,000 hectares per year against the 7,500 hectare target. The slow, paper-heavy grant application process (England Woodland Creation Offer, Countryside Stewardship Woodland Management) is frequently cited as a barrier. The Climate Change Committee has called the current rate of tree planting "woefully inadequate." The Forestry Commission faces scrutiny from both environmental campaigners and the NAO.

**Driver Intensity**: CRITICAL

**Enablers**:

- Streamlined digital grant application reducing processing time from 6 months to 6 weeks
- Pre-populated applications using existing land parcel and environmental designation data
- Automated environmental constraint checking (SSSI, ancient woodland, peatland) at application stage
- Real-time tracking of woodland creation progress against national targets

**Blockers**:

- Complex environmental safeguards that prevent rapid approval (but are ecologically necessary)
- Landowner reluctance due to long-term commitments and uncertain financial returns
- Limited FC operational capacity for site assessments and approvals
- Legacy IT systems that cannot support modern digital workflows

**Related Stakeholders**: Natural England (environmental constraints), Woodland Trust (planting advocacy), Landowners (land supply), HM Treasury (funding)

---

### SD-2: FC Operations Director — Modernising Felling Licence Workflow

**Stakeholder**: FC Operations Director

**Driver Category**: OPERATIONAL

**Driver Statement**: Replace the paper-based felling licence application and determination process with an end-to-end digital workflow, reducing the processing time from 13 weeks to 4 weeks while maintaining forestry standards and environmental safeguards.

**Context & Background**:
The felling licence process under the Forestry Act 1967 requires anyone felling more than 5 cubic metres of timber per calendar quarter to hold a felling licence. The current process is paper-intensive: applicants submit paper maps and forms, FC officers conduct site visits, cross-check environmental designations manually, and issue paper licences. The 13-week statutory determination period is frequently exceeded. The timber industry (via Confor) has repeatedly called for modernisation, noting that processing delays cost the forestry sector an estimated £15M annually in delayed harvesting operations.

**Driver Intensity**: HIGH

**Enablers**:

- Digital application with GIS-based site identification and automated constraint checking
- Automated cross-referencing with Natural England designations (SSSI, ancient woodland inventory)
- Digital felling licence issuance with geospatial boundary definitions
- Mobile-compatible field inspection tools for FC officers
- Integration with restocking conditions and compliance monitoring

**Blockers**:

- Rural broadband limitations for online applications in remote woodland areas
- FC officer resistance to changing established workflows
- Complexity of environmental constraint checking requiring professional judgement
- Integration with multiple legacy datasets (ancient woodland inventory, SSSI boundaries)

**Related Stakeholders**: Confor (industry advocacy), Woodland owners (applicants), Natural England (designations), Environment Agency (water quality)

---

### SD-3: UK Woodland Carbon Code — Verified Carbon Credit Integration

**Stakeholder**: UK Woodland Carbon Code Registry

**Driver Category**: STRATEGIC / FINANCIAL

**Driver Statement**: Integrate Woodland Carbon Code verification into the forestry management system to enable seamless carbon credit certification alongside woodland creation grants, reducing duplication and enabling landowners to stack environmental payments.

**Context & Background**:
The UK Woodland Carbon Code is a voluntary standard for verifying carbon sequestration from woodland creation. It is administered by Scottish Forestry but applies across the UK. Currently, landowners must separately register with the Carbon Code, submit duplicate site information, and undergo separate verification — creating friction and cost that deters participation. Carbon credits from woodland creation are increasingly valuable (current market price approximately £15-25 per tCO2e) and represent a significant financial incentive for landowners to plant trees.

**Driver Intensity**: MEDIUM

**Enablers**:

- Shared data model between forestry management and Carbon Code reducing duplicate data entry
- Automated carbon sequestration projections based on species mix, soil type, and location
- Integration with UK Land Carbon Registry for credit issuance
- Combined grant application and Carbon Code registration workflow

**Blockers**:

- Different governance structures (FC for forestry grants, Scottish Forestry for Carbon Code)
- Additionality requirements that may conflict with grant-funded woodland creation
- Complex carbon accounting methodology requiring specialist knowledge
- Market immaturity and policy uncertainty around voluntary carbon markets

**Related Stakeholders**: DEFRA (net zero policy), Landowners (revenue stacking), Forest Research (carbon modelling), Financial institutions (carbon market)

---

### SD-4: Woodland Trust — Protecting Ancient Woodland and Promoting Native Species

**Stakeholder**: Woodland Trust

**Driver Category**: ENVIRONMENTAL / COMPLIANCE

**Driver Statement**: Ensure the Forestry Management System prevents inappropriate felling of ancient woodland, promotes native species diversity in new planting, and provides transparent data on the condition and extent of the UK's woodland heritage.

**Context & Background**:
The Woodland Trust campaigns for the protection and restoration of ancient woodland — woodland that has existed continuously since at least 1600. Ancient woodland is irreplaceable and covers only 2.5% of England. The Trust is concerned that digital systems could accelerate approval processes at the expense of thorough environmental checks, and that woodland creation targets could incentivise monoculture conifer planting over biodiverse native woodland.

**Driver Intensity**: HIGH

**Enablers**:

- Mandatory ancient woodland proximity check in all felling licence and grant applications
- Automated ancient woodland inventory cross-referencing with buffered impact zones
- Species diversity requirements embedded in grant application assessment criteria
- Public access to National Forest Inventory data showing woodland type and condition

**Blockers**:

- Incomplete or inaccurate ancient woodland inventory data
- Pressure to approve planting schemes quickly without adequate ecological review
- Commercial forestry interests favouring fast-growing non-native species
- Limited public transparency of forestry management data

**Related Stakeholders**: Natural England (designations), FC Chief Forester (standards), Conservation charities (biodiversity), Forest Research (evidence)

---

## Driver-to-Goal Mapping

### Goal G-1: Digitised Felling Licence Workflow

**Derived From Drivers**: SD-2

**Goal Owner**: FC Operations Director

**Goal Statement**: Deliver an end-to-end digital felling licence application, assessment, and issuance workflow that reduces average processing time from 13 weeks to 4 weeks within 12 months of launch.

**Why This Matters**: The timber industry loses an estimated £15M annually from delayed felling operations. A digital workflow eliminates paper handling, automates constraint checking, and enables mobile field inspections.

**Success Metrics**:

- **Primary Metric**: Average felling licence processing time < 4 weeks (from 13 weeks baseline)
- **Secondary Metrics**:
  - 100% of applications received digitally within 18 months
  - FC officer productivity increase of 40% (applications processed per FTE)
  - Applicant satisfaction score > 8/10

**Baseline**: 13-week average processing time, paper-based process

**Target**: 4-week average processing time, fully digital process

---

### Goal G-2: Accelerated Woodland Creation Grants

**Derived From Drivers**: SD-1

**Goal Owner**: SRO, Forestry Digital

**Goal Statement**: Reduce woodland creation grant application processing time from 6 months to 6 weeks, with automated environmental constraint checking, contributing to achieving the 7,500 hectare annual planting target.

**Why This Matters**: Grant processing delays are a primary barrier to woodland creation. Faster approvals directly translate to more trees planted per planting season (November-March).

**Success Metrics**:

- **Primary Metric**: Average grant application processing time < 6 weeks
- **Secondary Metrics**:
  - Woodland creation rate increases by 50% within 2 years
  - Grant application abandonment rate decreases from 30% to <10%
  - Automated environmental constraint check coverage > 95% of application area

**Baseline**: 6-month average processing, 2,500 ha/year creation rate

**Target**: 6-week average processing, 5,000 ha/year creation rate (trajectory to 7,500)

---

### Goal G-3: Real-Time National Forest Inventory

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: Forest Research

**Goal Statement**: Update the National Forest Inventory from a periodic (10-year cycle) assessment to a continuous, near-real-time inventory integrating satellite imagery, LiDAR data, and field surveys, providing current woodland extent and condition data within 12 months of any change.

**Success Metrics**:

- **Primary Metric**: Time from woodland change event to inventory update < 12 months (from 10-year cycle)
- **Secondary Metrics**:
  - Satellite-detected change events validated within 3 months
  - Woodland extent accuracy within 2% of ground truth
  - Public data portal with current inventory accessible to all

---

## Goal-to-Outcome Mapping

### Outcome O-1: Increased Woodland Creation Contributing to Net Zero and Biodiversity

**Supported Goals**: G-2, G-3

**Outcome Statement**: England's annual woodland creation rate increases from approximately 2,500 hectares to 5,000 hectares within 2 years, with native broadleaf species comprising at least 60% of new planting, contributing measurably to net zero carbon targets and the 30by30 biodiversity commitment.

**Business Value**:

- **Financial Impact**: £25M additional carbon sequestration value annually, £15M in forestry sector productivity gains
- **Strategic Impact**: Demonstrable progress on England Trees Action Plan and net zero trajectory
- **Operational Impact**: FC processing capacity doubled through automation
- **Customer Impact**: Landowner confidence in grant process, increased participation

### Outcome O-2: Efficient, Transparent Forestry Regulation

**Supported Goals**: G-1, G-3

**Outcome Statement**: The forestry sector experiences a modern, transparent regulatory environment with digital felling licences processed in 4 weeks, real-time inventory data, and integrated compliance monitoring — eliminating £15M annual cost of regulatory delays.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA / FC Chair | SD-1 | Woodland creation targets | G-2 | Faster grant processing | O-1 | Increased woodland creation |
| FC Operations Dir | SD-2 | Modernise felling workflow | G-1 | Digital felling licence | O-2 | Efficient forestry regulation |
| Carbon Code | SD-3 | Carbon credit integration | G-2 | Integrated grant/carbon process | O-1 | Net zero contribution |
| Woodland Trust | SD-4 | Ancient woodland protection | G-3 | Real-time inventory | O-1 | Native species, biodiversity |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DEFRA/FC (SD-1) want to accelerate woodland creation approvals, but Woodland Trust (SD-4) and Natural England want thorough environmental assessment to prevent inappropriate planting on peatland or biodiverse grassland.
  - **Resolution Strategy**: Automated environmental constraint checking at application stage — GIS-based screening identifies issues early, fast-tracking appropriate schemes while flagging sensitive sites for detailed assessment. This maintains safeguards without blanket delays.

**Synergies**:

- **Synergy 1**: FC Operations (SD-2) and the timber industry both benefit from faster felling licence processing — shared interest in digital modernisation.
- **Synergy 2**: Carbon Code integration (SD-3) and woodland creation acceleration (SD-1) are mutually reinforcing — carbon revenue makes woodland creation more financially attractive to landowners.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | FC Finance | FC Chief Exec | DEFRA, HM Treasury | All stakeholders |
| Felling licence workflow design | Product Manager | FC Operations Dir | Confor, NE | Woodland owners |
| Grant process redesign | Policy Lead | SRO | DEFRA, RPA | Landowners, Woodland Trust |
| Architecture decisions | Technical Lead | FC Digital Dir | Security, Forest Research | Business |
| Environmental safeguard rules | FC Chief Forester | NE | Woodland Trust, EA | Applicants |

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| FC Chief Forester | | | |
| FC Digital Director | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| England Trees Action Plan 2021 | Policy | DEFRA | Woodland creation targets | N/A |
| Forestry Act 1967 | Legislation | legislation.gov.uk | Felling licence requirements | N/A |
| UK Woodland Carbon Code | Standard | Scottish Forestry | Carbon credit verification | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Forestry Management System
**Model**: Claude Opus 4.6
