# Stakeholder Drivers & Goals Analysis: Wildlife Crime Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Wildlife Crime Intelligence (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Wildlife Crime Intelligence Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, NCA, NWCU, DEFRA, Border Force, Police Wildlife Crime Officers, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Wildlife Crime Intelligence platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals.

### Key Findings

The Wildlife Crime Intelligence platform addresses a critical gap in UK law enforcement capability — the lack of a unified digital platform for wildlife crime intelligence that connects the National Wildlife Crime Unit (NWCU), territorial police forces, Border Force, CITES Management Authority, and international partners. The strongest alignment exists around establishing a single intelligence platform that replaces fragmented spreadsheets and email-based intelligence sharing. The most significant tension is between the NCA's desire for a comprehensive intelligence system meeting national security standards and the practical reality that most wildlife crime intelligence is generated and actioned by under-resourced police Wildlife Crime Officers (WCOs) who need simple, accessible tools — not enterprise-grade intelligence platforms.

### Critical Success Factors

- Deliver a National Intelligence Model (NIM) compliant platform accessible to all 43 territorial police forces in England and Wales
- Implement 5x5x5 intelligence grading and sanitisation for secure cross-agency sharing
- Integrate with CITES permit management for border enforcement of endangered species trade
- Enable international intelligence exchange with INTERPOL Environmental Security and Europol
- Maintain OFFICIAL-SENSITIVE security accreditation while remaining accessible to frontline WCOs

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for a unified intelligence platform, but significant tensions between NCA-level security requirements and police force accessibility, between comprehensive data collection and proportionate surveillance, and between ambitious digital capability and the limited resources available for wildlife crime enforcement in most police forces.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| NCA Director General (Threats) | NCA leadership | HIGH | HIGH | Manage Closely — Strategic direction, resource allocation |
| NWCU Head | Unit leadership | HIGH | HIGH | Manage Closely — Operational requirements, intelligence standards |
| SRO, Wildlife Crime Intelligence | Programme Sponsor (NCA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| NCA Chief Technology Officer | IT strategy | HIGH | HIGH | Manage Closely — Architecture, security accreditation |
| NCA SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — Risk acceptance, DPIA |
| NWCU Intelligence Analysts | Intelligence production | MEDIUM | HIGH | Keep Informed — User requirements, workflow design |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DEFRA | Government department | CITES Management Authority, policy | HIGH | HIGH |
| Border Force | Home Office | CITES border enforcement | HIGH | HIGH |
| Police Wildlife Crime Officers (WCOs) | 43 territorial police forces | Frontline intelligence gathering | MEDIUM | HIGH |
| NPCC Wildlife Crime Lead | National Police Chiefs' Council | Police coordination | HIGH | HIGH |
| Crown Prosecution Service (CPS) | Prosecution authority | Evidence standards, prosecution decisions | HIGH | MEDIUM |
| INTERPOL Environmental Security | International organisation | International intelligence exchange | MEDIUM | HIGH |
| Europol | EU agency | European intelligence coordination | MEDIUM | MEDIUM |
| RSPB Investigations | Charity | Intelligence source, raptor persecution | MEDIUM | HIGH |
| RSPCA | Charity | Animal welfare intelligence | LOW | HIGH |
| Animal and Plant Health Agency (APHA) | Executive agency | CITES scientific authority | MEDIUM | HIGH |
| HM Revenue & Customs | Government department | Financial investigation, POCA | MEDIUM | MEDIUM |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| ICO | Regulator | Surveillance, data protection | HIGH | MEDIUM |
| Partnership for Action Against Wildlife Crime (PAW) | Multi-agency partnership | Stakeholder coordination | MEDIUM | HIGH |
| World Wildlife Fund (WWF) | International charity | Wildlife trade policy advocacy | LOW | HIGH |
| Environmental Investigation Agency (EIA) | NGO | Undercover wildlife crime investigation | LOW | HIGH |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at NCA board level | HIGH / HIGH | Manage Closely — Security risk, accreditation |
| NCA Security Officer | Day-to-day security coordination | HIGH / HIGH | Manage Closely — Security compliance, vetting |
| Senior Information Risk Owner (SIRO) | Information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — Information risk decisions |
| Cyber Security Lead | Operational cyber security, penetration testing | MEDIUM / HIGH | Keep Informed — Architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • NCA Dir Gen      │
        │  • CDDO             │  • NWCU Head        │
        │  • ICO              │  • SRO              │
        │  • NCA SIRO         │  • NCA CTO          │
        │  • CPS              │  • DEFRA (CITES)    │
 P      │                     │  • Border Force     │
 O      │                     │  • NPCC WC Lead     │
 W      │                     │  • SSRO / NCA Sec   │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Europol          │  • Police WCOs      │
        │  • HMRC             │  • NWCU Analysts    │
        │                     │  • RSPB Invest.     │
        │                     │  • RSPCA            │
        │                     │  • APHA             │
        │                     │  • INTERPOL         │
        │                     │  • PAW              │
        │                     │  • WWF / EIA        │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: NCA / NWCU Head — Unified National Intelligence Picture for Wildlife Crime

**Stakeholder**: NWCU Head / NCA Director General (Threats)

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Establish a single, authoritative national intelligence picture for wildlife crime across the UK, enabling strategic threat assessment, coordinated enforcement operations, and evidence-based resource allocation — replacing the current fragmented landscape of spreadsheets, email chains, and inconsistent local recording.

**Context & Background**:
The National Wildlife Crime Unit (NWCU) is a small unit (approximately 12 staff) funded jointly by DEFRA and the Home Office, hosted within NCA. It coordinates the UK's response to wildlife crime across the seven UK wildlife crime priorities (badger persecution, bat persecution, CITES issues, freshwater pearl mussels, poaching, raptor persecution, and trade in endangered species). Currently, intelligence arrives via multiple channels — emails from police WCOs, RSPB reports, Border Force seizure notifications, CITES permit alerts — with no single system to collate, grade, analyse, and disseminate. The NWCU Strategic Assessment repeatedly identifies poor intelligence flow as the primary barrier to effective enforcement.

**Driver Intensity**: CRITICAL

**Enablers**:

- Single platform for intelligence submission, grading (5x5x5), analysis, and dissemination
- National Intelligence Model (NIM) compliant processes built into the platform workflow
- Automated intelligence product generation (problem profiles, subject profiles, strategic assessments)
- Secure, role-based access for all contributing agencies with appropriate sanitisation

**Blockers**:

- 43 territorial police forces with different IT systems, priorities, and levels of engagement
- Many police forces have only part-time or no dedicated WCOs (wildlife crime is not a policing priority for many forces)
- NCA security requirements may create access barriers for police force and charity contributors
- Small NWCU team with limited capacity to manage platform implementation alongside operational duties

**Related Stakeholders**: Police WCOs (intelligence contributors), Border Force (CITES enforcement), RSPB (intelligence source), INTERPOL (international exchange)

---

### SD-2: Border Force — CITES Border Enforcement and Permit Verification

**Stakeholder**: Border Force

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Provide Border Force officers with real-time access to CITES permit data, species identification tools, and intelligence alerts at ports of entry, enabling effective enforcement of international wildlife trade controls and rapid identification of illegal shipments.

**Context & Background**:
The UK is a significant market for international wildlife trade — both legal (requiring CITES permits) and illegal. Border Force officers at airports, seaports, and postal hubs must identify whether wildlife products require CITES permits, verify permit authenticity, and cross-reference against intelligence about known trafficking routes and suspects. Currently, CITES permit verification relies on checking paper permits against DEFRA's CITES permit database — a slow process that creates delays at border control. The UK committed to strengthened CITES enforcement as part of the Illegal Wildlife Trade Conference outcomes.

**Driver Intensity**: HIGH

**Enablers**:

- Real-time API integration between CITES permit database and Border Force targeting systems
- Species identification support tools (image recognition, morphological guides) for non-specialist officers
- Intelligence alerts for high-risk consignments, routes, and subjects
- Mobile-compatible tools for inspection at port/airport environments

**Blockers**:

- Border Force IT infrastructure constraints and security requirements
- Limited wildlife expertise among Border Force officers (generalist role)
- Volume of legitimate trade making risk-based targeting essential
- Different CITES permit systems used by exporting countries

**Related Stakeholders**: DEFRA CITES Authority (permits), APHA (species identification), NWCU (intelligence), HMRC (financial investigation)

---

### SD-3: Police Wildlife Crime Officers — Accessible, Practical Intelligence Tools

**Stakeholder**: Police Wildlife Crime Officers (WCOs) across 43 territorial forces

**Driver Category**: OPERATIONAL / PRACTICAL

**Driver Statement**: Provide simple, accessible tools that enable part-time and full-time WCOs to submit intelligence, search for patterns, and access operational guidance without requiring specialist IT training or NCA-grade security infrastructure.

**Context & Background**:
Wildlife Crime Officers in territorial police forces range from full-time dedicated officers (few forces, e.g., Metropolitan Police, Police Scotland) to officers with wildlife crime as one of many responsibilities (most forces). Many WCOs are PCs or DCs who handle wildlife crime alongside other duties. They typically work from standard police issue laptops with force-managed IT environments. Any intelligence platform must be accessible from these environments without requiring separate NCA credentials, VPN access, or specialist training. Previous law enforcement systems that required complex access procedures were simply not used by frontline officers.

**Driver Intensity**: HIGH

**Enablers**:

- Web-based platform accessible from standard police force IT environments
- Simple intelligence submission form taking < 10 minutes to complete
- Pre-populated species and offence type lists based on UK wildlife crime priorities
- Mobile app for field intelligence reporting (e.g., reporting poisoned raptors, illegal traps)
- Automated feedback showing how submitted intelligence contributed to operations

**Blockers**:

- NCA security requirements creating access barriers for police force networks
- Force IT policies blocking access to external platforms
- Lack of dedicated time for intelligence reporting in busy policing schedules
- Inconsistent management support for wildlife crime across forces

**Related Stakeholders**: NPCC WC Lead (policing coordination), NWCU (intelligence consumers), Chief Constables (resource allocation), RSPB (joint investigations)

---

### SD-4: RSPB Investigations — Raptor Persecution Intelligence Partnership

**Stakeholder**: RSPB Investigations Team

**Driver Category**: ENVIRONMENTAL / OPERATIONAL

**Driver Statement**: Establish a structured intelligence-sharing partnership that enables RSPB's substantial raptor persecution intelligence (satellite-tagged bird data, field observations, informant reports) to be systematically fed into the national intelligence picture, leading to more prosecutions and deterrence.

**Context & Background**:
The RSPB's Investigations Team is a significant intelligence source — particularly for raptor persecution (illegal killing of birds of prey, predominantly on driven grouse moors). RSPB monitors satellite-tagged raptors and can identify suspicious tag failures and locations. Currently, intelligence sharing is informal and relationship-dependent. RSPB has publicly criticised the lack of prosecutions despite strong intelligence, suggesting information is lost or not actioned within the policing system. A structured digital channel for intelligence sharing would improve both the quantity and quality of intelligence flowing into the system.

**Driver Intensity**: HIGH

**Enablers**:

- Dedicated intelligence submission channel for accredited NGO investigators
- Satellite tag tracking data integration (with appropriate access controls)
- Feedback mechanism showing intelligence status and actions taken
- Clear memorandum of understanding on intelligence sharing, handling, and disclosure

**Blockers**:

- Sensitivity around NGO access to law enforcement intelligence systems
- Concerns about disclosure and legal privilege in ongoing investigations
- Political sensitivity of raptor persecution (grouse moor management interests)
- Data quality and standardisation of NGO-generated intelligence

**Related Stakeholders**: NWCU (intelligence consumers), Police WCOs (investigators), CPS (prosecution), NPCC WC Lead (coordination)

---

## Driver-to-Goal Mapping

### Goal G-1: National Wildlife Crime Intelligence Platform

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: NWCU Head

**Goal Statement**: Deliver a National Intelligence Model (NIM) compliant wildlife crime intelligence platform accessible to all 43 territorial police forces, NWCU, Border Force, and accredited partner organisations within 18 months, achieving >80% of active WCOs submitting intelligence through the platform within 12 months of launch.

**Success Metrics**:

- **Primary Metric**: >80% of active WCOs using platform for intelligence submission (from ~30% ad hoc reporting)
- **Secondary Metrics**:
  - 100% of intelligence graded using 5x5x5 system on platform
  - Time from intelligence submission to dissemination reduced from weeks to 48 hours
  - Strategic threat assessment produced annually using platform analytics
  - Number of intelligence-led operations increases by 50%

---

### Goal G-2: Integrated CITES Enforcement at Border

**Derived From Drivers**: SD-2

**Goal Owner**: Border Force Wildlife Lead

**Goal Statement**: Integrate CITES permit verification and wildlife crime intelligence alerts into Border Force targeting systems, enabling real-time risk assessment of wildlife trade consignments with species identification support, within 12 months.

**Success Metrics**:

- **Primary Metric**: Real-time CITES permit verification available at all major ports (from manual lookup)
- **Secondary Metrics**:
  - Border seizures of illegal wildlife products increase by 30%
  - Permit verification time reduced from 30 minutes to < 2 minutes
  - Species identification accuracy > 95% for CITES Appendix I species

---

### Goal G-3: Structured NGO Intelligence Partnership

**Derived From Drivers**: SD-4

**Goal Owner**: NWCU Head

**Goal Statement**: Establish a structured intelligence-sharing framework with accredited NGO investigators (RSPB, RSPCA, EIA), with digital submission channels and feedback mechanisms, within 6 months of platform launch.

**Success Metrics**:

- **Primary Metric**: >90% of RSPB investigation intelligence submitted through structured digital channel
- **Secondary Metrics**:
  - Intelligence-to-prosecution conversion rate increases by 25%
  - Feedback provided on 100% of submitted intelligence within 10 working days

---

## Goal-to-Outcome Mapping

### Outcome O-1: Disruption of Organised Wildlife Crime Networks

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: The number of intelligence-led enforcement operations against organised wildlife crime networks increases by 50%, with a 30% increase in successful prosecutions, contributing to the UK's international commitments on combating illegal wildlife trade.

**Business Value**:

- **Financial Impact**: Increased POCA asset recovery from wildlife crime (currently under-pursued), estimated £2M annually
- **Strategic Impact**: UK demonstrates international leadership on wildlife crime enforcement, supporting CITES and IWT Conference commitments
- **Operational Impact**: NWCU transitions from reactive to proactive intelligence-led operations
- **Customer Impact**: Public confidence in wildlife protection, deterrent effect on offenders

### Outcome O-2: Effective CITES Border Enforcement

**Supported Goals**: G-2

**Outcome Statement**: The UK's CITES border enforcement achieves real-time permit verification and risk-based targeting, resulting in a 30% increase in illegal wildlife trade seizures and zero delays to legitimate CITES trade.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| NCA / NWCU | SD-1 | Unified intelligence picture | G-1 | National intelligence platform | O-1 | Disrupt wildlife crime networks |
| Border Force | SD-2 | CITES border enforcement | G-2 | Integrated CITES enforcement | O-2 | Effective border enforcement |
| Police WCOs | SD-3 | Accessible intelligence tools | G-1 | Accessible platform | O-1 | Intelligence-led operations |
| RSPB Investigations | SD-4 | Raptor persecution intelligence | G-3 | NGO intelligence partnership | O-1 | Increased prosecutions |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: NCA (SD-1) requires OFFICIAL-SENSITIVE security controls, but police WCOs (SD-3) need simple access from standard police IT environments.
  - **Resolution Strategy**: Tiered access model — WCOs access a "submission and search" tier at OFFICIAL from police networks; NWCU analysts work at OFFICIAL-SENSITIVE for sensitive intelligence products; sanitised intelligence disseminated at appropriate classification. Platform architecturally supports both tiers.

- **Conflict 2**: RSPB (SD-4) wants comprehensive access to intelligence outcomes, but law enforcement must protect operational security and ongoing investigations.
  - **Resolution Strategy**: Structured feedback on intelligence status (received/actioned/closed) without operational detail. MoU defines clear boundaries. RSPB does not access law enforcement intelligence — they contribute to it.

**Synergies**:

- **Synergy 1**: All stakeholders agree that the current fragmented approach is failing. Unified platform benefits everyone.
- **Synergy 2**: CITES permit integration (SD-2) and national intelligence (SD-1) are mutually reinforcing — border seizure intelligence feeds into strategic assessment.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | NCA Finance | NCA Director General | DEFRA, Home Office | All stakeholders |
| Intelligence standards | NWCU Head | NCA Director General | NPCC WC Lead, CPS | Police forces, NGOs |
| Security accreditation | NCA CTO | NCA SSRO | NCSC, Cyber Security Lead | All users |
| Architecture decisions | Technical Lead | NCA CTO | Border Force IT, Police IT | Business |
| NGO access framework | NWCU Head | SRO | RSPB, RSPCA, PAW | Police WCOs |
| CITES integration | DEFRA CITES Authority | SRO | Border Force, APHA | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Wildlife and Countryside Act 1981 | Legislation | legislation.gov.uk | Protected species and habitats offences | N/A |
| CITES | International convention | cites.org | Endangered species trade controls | N/A |
| National Intelligence Model | Standard | College of Policing | Intelligence management framework | N/A |
| UK Wildlife Crime Priorities | Policy | DEFRA/Home Office | Seven priority crime types | N/A |
| Proceeds of Crime Act 2002 | Legislation | legislation.gov.uk | Financial investigation powers | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wildlife Crime Intelligence
**Model**: Claude Opus 4.6
