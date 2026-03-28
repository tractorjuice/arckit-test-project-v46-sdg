# Stakeholder Drivers & Goals Analysis: Smart City IoT Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Smart City IoT Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart City IoT Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart City IoT Programme Board, DLUHC Digital, CDDO, Local Authority Partners |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Smart City IoT Platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The platform will provide a shared, secure infrastructure for deploying and managing connected sensors across urban environments, serving as the foundational data layer for the wider SDG 11 programme.

### Key Findings

The Smart City IoT Platform faces a fundamental tension between the ambition for a unified national IoT platform and the reality that local authorities have existing sensor deployments, legacy contracts, and varying levels of digital maturity. The strongest alignment exists around reducing duplication — most local authorities are deploying sensors independently, creating fragmented data and duplicated procurement. The most significant conflict is between citizen privacy advocates (concerned about pervasive urban surveillance) and local authority operational teams (who want granular data for service optimisation). NCSC and the Geospatial Commission are strong allies, as this platform directly supports their strategies.

### Critical Success Factors

- Demonstrate interoperability with at least 5 existing local authority sensor networks within 12 months
- Achieve ETSI EN 303 645 compliance across all connected devices to maintain NCSC confidence
- Publish aggregated sensor data as open data on data.gov.uk to demonstrate transparency and value
- Onboard 20 local authorities in the first phase to prove scalability and cross-authority value
- Maintain citizen trust by implementing visible privacy protections and clear public communication

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for a shared IoT platform to reduce fragmentation and cost, but significant tensions around data ownership (local vs. central), privacy (surveillance concerns vs. operational value), procurement impact (disrupting existing vendor relationships), and governance (who controls the platform long-term). Local authorities' varying digital maturity levels add complexity to adoption planning.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Local Government | DLUHC Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, levelling up narrative |
| DLUHC Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Smart City IoT Platform | Programme Sponsor (DLUHC) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DLUHC Chief Digital Officer | Digital strategy leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Geospatial Commission | Cross-government geospatial strategy | HIGH | HIGH | Manage Closely — National spatial data infrastructure alignment |
| DLUHC Data Ethics Team | Data governance and ethics | MEDIUM | HIGH | Keep Informed — Ethics review, DPIA input |
| DLUHC Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| DLUHC SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| NCSC | National Cyber Security Centre | IoT security guidance | HIGH | HIGH |
| Local Authority Chief Executives | 333 English local authorities | Adoption partners | HIGH | HIGH |
| Local Authority Digital Teams | LA digital/IT departments | Implementation partners | MEDIUM | HIGH |
| UK Smart Cities Network | Cross-sector smart cities body | Standards and best practice | MEDIUM | HIGH |
| Information Commissioner's Office | ICO | Data protection oversight | HIGH | HIGH |
| Ordnance Survey | Geospatial data partner | Spatial data infrastructure | MEDIUM | HIGH |
| IoT Device Manufacturers | Industry | Hardware suppliers | MEDIUM | HIGH |
| Urban Residents | Citizens | Data subjects and beneficiaries | LOW | HIGH |
| Privacy Campaign Groups | Big Brother Watch, Liberty, ORG | Civil liberties advocacy | LOW | HIGH |
| Connected Places Catapult | Innovate UK | Innovation and commercialisation | MEDIUM | MEDIUM |
| HM Treasury | HMT | Funding approval | HIGH | MEDIUM |
| National Audit Office | NAO | Value for money audit | HIGH | MEDIUM |
| Surveillance Camera Commissioner | Oversight body | Camera and sensor oversight | MEDIUM | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for IoT Platform outcomes and spend | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end platform service and local authority outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and adoption targets | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |
| CDIO (DLUHC) | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security, IoT security assessment | MEDIUM / HIGH | Keep Informed — Security architecture reviews, pen testing |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Minister for     |
        |  * NAO              |    Local Government |
        |  * DLUHC Perm Sec   |  * SRO              |
        |  * DLUHC SIRO       |  * DLUHC CDO        |
        |  * DLUHC Finance    |  * Geospatial Comm. |
 P      |  * CDDO             |  * NCSC             |
 O      |  * SSRO / DSO       |  * LA Chief Execs   |
 W      |                     |  * ICO              |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Connected Places |  * Urban Residents  |
        |    Catapult         |  * Privacy Groups   |
        |                     |  * LA Digital Teams |
        |                     |  * Smart Cities Net.|
        |                     |  * Ordnance Survey  |
        |                     |  * IoT Manufacturers|
        |                     |  * Surveillance Cam.|
        |                     |  * Data Ethics Team |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Minister for Local Government — Levelling Up Through Smart Infrastructure

**Stakeholder**: Minister for Local Government (DLUHC)

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate that smart city technology can improve public services and quality of life across all regions — not just London and major cities — supporting the Levelling Up agenda and showing visible, measurable improvements to urban services that citizens and media can understand.

**Context & Background**:
The Levelling Up White Paper committed to spreading the benefits of technology-driven urban improvement beyond London and the South East. The Minister needs a platform that can be adopted by councils in Sunderland, Stoke, and Blackpool as readily as by Manchester or Bristol. Previous smart city initiatives have been criticised as "innovation theatre" — expensive pilots that never scale. The Minister needs a programme that delivers tangible, everyday improvements.

**Driver Intensity**: CRITICAL

**Enablers**:
- Platform designed for local authorities of all sizes and digital maturity levels
- Quick wins: tangible improvements visible within 6 months of deployment (e.g., bin collection optimisation, streetlight management)

**Blockers**:
- Platform perceived as London-centric or only for digitally advanced councils
- Privacy controversy that dominates media coverage and overshadows benefits

**Related Stakeholders**: Local Authority Chief Executives (SD-3), Privacy Campaign Groups (SD-6)

---

### SD-2: NCSC — Securing Critical National IoT Infrastructure

**Stakeholder**: National Cyber Security Centre

**Driver Category**: SECURITY / COMPLIANCE

**Driver Statement**: Ensure that government-sponsored IoT deployments in urban infrastructure set the gold standard for IoT security, complying with ETSI EN 303 645 and the Connected Places Cyber Security Principles, preventing smart city infrastructure from becoming a national security vulnerability.

**Context & Background**:
NCSC has published Connected Places Cyber Security Principles specifically addressing the risks of smart city deployments. Insecure IoT devices in public infrastructure represent a significant attack surface — compromised traffic sensors could cause accidents, manipulated environmental sensors could suppress health warnings. The PSTI Act 2022 sets baseline requirements, but NCSC expects government deployments to exceed these baselines. The Mirai botnet attack demonstrated the real-world consequences of insecure IoT at scale.

**Driver Intensity**: CRITICAL

**Enablers**:
- Dedicated IoT security architecture with device identity management
- NCSC engaged as architecture reviewer from Discovery phase

**Blockers**:
- Cost pressure leading to procurement of cheaper, less secure devices
- Local authorities deploying their own devices outside platform governance

**Related Stakeholders**: Cyber Security Lead, IoT Device Manufacturers (SD-5)

---

### SD-3: Local Authority Chief Executives — Reducing Fragmentation and Cost

**Stakeholder**: Local Authority Chief Executives (collectively)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Reduce the cost and complexity of deploying and managing smart city sensors by using a shared national platform, avoiding each council procuring, building, and operating its own IoT infrastructure while retaining local control over data and deployment priorities.

**Context & Background**:
Over 80 English local authorities have some form of smart city or IoT deployment, but these are overwhelmingly siloed — different vendors, different platforms, different data formats. Councils are spending £2-10M each on fragmented IoT infrastructure with limited interoperability. A shared platform could reduce per-authority costs by 40-60% while improving data quality and enabling cross-authority benchmarking. However, local authorities guard their autonomy fiercely and are wary of central government mandating technology choices.

**Driver Intensity**: HIGH

**Enablers**:
- Platform offered as opt-in, not mandated, with clear cost-benefit case per authority
- Local authorities retain ownership of their data and control deployment priorities

**Blockers**:
- Perception that DLUHC is centralising control over local services
- Existing vendor contracts that lock authorities into proprietary platforms for 3-5 years

**Related Stakeholders**: LA Digital Teams, DLUHC CDO, IoT Device Manufacturers

---

### SD-4: ICO — Privacy Protection in Urban Sensor Networks

**Stakeholder**: Information Commissioner's Office

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure that urban sensor deployments comply with UK GDPR and the Data Protection Act 2018, with particular attention to the privacy implications of pervasive sensing in public spaces, adequate Data Protection Impact Assessments, and citizens' ability to understand and exercise their data rights.

**Context & Background**:
The ICO has identified smart cities as a priority area for proactive regulatory engagement. The distinction between personal and non-personal data in the IoT context is not always clear — an air quality sensor that records foot traffic counts may not capture personal data, but a sensor network dense enough to track individual movement patterns does. The ICO expects DLUHC to set an exemplary standard for privacy-by-design in public-space sensing.

**Driver Intensity**: HIGH

**Enablers**:
- DPIA conducted before any sensor deployment, published transparently
- Privacy-preserving analytics (aggregation at source, differential privacy) embedded in platform architecture

**Blockers**:
- Pressure from operational teams to collect granular data for maximum analytical value
- Scope creep from environmental sensing to surveillance (e.g., adding cameras to air quality stations)

**Related Stakeholders**: Privacy Campaign Groups (SD-6), DLUHC SIRO, Surveillance Camera Commissioner

---

### SD-5: IoT Device Manufacturers — Open, Competitive Market Access

**Stakeholder**: IoT Device Manufacturers (industry collective)

**Driver Category**: COMMERCIAL / STRATEGIC

**Driver Statement**: Ensure the platform uses open standards for device integration, enabling a competitive market of IoT hardware suppliers rather than locking into a single vendor's proprietary ecosystem, while maintaining interoperability through well-defined device onboarding specifications.

**Context & Background**:
The UK IoT hardware market includes global manufacturers and innovative UK SMEs. A government platform that mandates proprietary protocols or certifies only specific vendors would distort the market and risk vendor lock-in. Conversely, completely open integration without security certification creates risk. The balance requires open standards (MQTT, CoAP, LwM2M) with a certification process that any compliant manufacturer can pass.

**Driver Intensity**: MEDIUM

**Enablers**:
- Open device onboarding standards based on industry protocols (MQTT, LwM2M)
- Device certification programme accessible to SMEs (not prohibitively expensive)

**Blockers**:
- Platform architecture favouring one vendor's proprietary protocol stack
- Certification costs or timescales that exclude smaller manufacturers

**Related Stakeholders**: NCSC (security certification), Connected Places Catapult

---

### SD-6: Privacy Campaign Groups — Preventing Urban Surveillance Infrastructure

**Stakeholder**: Big Brother Watch, Liberty, Open Rights Group

**Driver Category**: CIVIL LIBERTIES / COMPLIANCE

**Driver Statement**: Prevent the Smart City IoT Platform from becoming pervasive surveillance infrastructure, ensuring that sensor deployments are proportionate, transparent, subject to democratic oversight, and that citizens retain meaningful control over their data in public spaces.

**Context & Background**:
Privacy groups have legitimate concerns that smart city infrastructure normalises surveillance. Once a dense sensor network exists, the temptation to repurpose it — adding facial recognition, tracking protest movements, monitoring specific communities — is significant. International examples (Sidewalk Labs in Toronto, Chinese social credit systems) have shown how smart city technology can erode civil liberties. These groups expect robust governance, transparency, and genuine constraints on data use.

**Driver Intensity**: HIGH

**Enablers**:
- Clear, published data use policies with legally binding constraints on repurposing
- Independent oversight mechanism (e.g., citizen data ethics panel)
- Transparent DPIA process with public consultation

**Blockers**:
- Opaque decision-making about what sensors collect and how data is used
- Incremental scope creep adding surveillance capability to environmental sensors

**Related Stakeholders**: ICO (SD-4), Urban Residents, Surveillance Camera Commissioner

---

## Driver-to-Goal Mapping

### Goal G-1: Onboard 20 Local Authorities to Shared IoT Platform in Year 1

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: SRO, Smart City IoT Platform

**Goal Statement**: Onboard at least 20 local authorities (representing diverse geographies and digital maturity levels) to the shared IoT platform within 12 months of platform launch, with each authority actively ingesting sensor data.

**Why This Matters**: Demonstrates viability of shared infrastructure (SD-3) and regional breadth supporting Levelling Up (SD-1).

**Success Metrics**:
- **Primary Metric**: Number of local authorities actively publishing sensor data via the platform
- **Secondary Metrics**:
  - Geographic distribution across English regions (minimum 6 of 9 regions represented)
  - Range of digital maturity levels (at least 5 authorities below Tier 1 digital maturity)
  - Total number of sensors connected

**Baseline**: 0 (new platform)
**Target**: 20 local authorities, 10,000+ sensors connected
**Measurement Method**: Platform analytics dashboard, quarterly adoption report

**Dependencies**:
- Platform MVP deployed and operational
- Pricing model agreed and published
- Local authority engagement programme resourced

**Risks to Achievement**:
- Local authorities delay due to existing contract commitments
- Procurement timescales extend beyond 12 months for some authorities

---

### Goal G-2: Achieve Full ETSI EN 303 645 Compliance for All Connected Devices

**Derived From Drivers**: SD-2

**Goal Owner**: NCSC Liaison / Cyber Security Lead

**Goal Statement**: All devices connected to the Smart City IoT Platform comply with ETSI EN 303 645 baseline security requirements, verified through a published device certification programme, by platform launch.

**Why This Matters**: Ensures government IoT deployment sets security gold standard (SD-2) and prevents the platform from becoming a national security vulnerability.

**Success Metrics**:
- **Primary Metric**: Percentage of connected device types with ETSI EN 303 645 compliance certification
- **Secondary Metrics**:
  - Number of device manufacturers completing certification
  - Mean time to patch critical firmware vulnerabilities across device fleet

**Baseline**: No current IoT security certification programme
**Target**: 100% of connected device types certified compliant
**Measurement Method**: Device certification register, quarterly firmware audit

---

### Goal G-3: Publish Aggregated Urban Data as Open Data Within 6 Months

**Derived From Drivers**: SD-1, SD-4, SD-6

**Goal Owner**: DLUHC Chief Data Officer

**Goal Statement**: Publish aggregated, non-personal sensor data from the IoT platform as open data on data.gov.uk within 6 months of first deployment, demonstrating transparency and enabling third-party innovation.

**Why This Matters**: Builds citizen trust (SD-6), demonstrates ICO-compliant transparency (SD-4), and provides visible public value supporting Ministerial narrative (SD-1).

**Success Metrics**:
- **Primary Metric**: Number of open datasets published on data.gov.uk
- **Secondary Metrics**:
  - Third-party applications using the open data APIs
  - Public download/API call volumes

**Baseline**: 0 (new platform)
**Target**: Minimum 10 aggregated datasets published, 5+ third-party applications registered
**Measurement Method**: data.gov.uk analytics, API usage dashboard

---

### Goal G-4: Demonstrate 40% Cost Reduction vs. Independent Local Authority Deployment

**Derived From Drivers**: SD-3

**Goal Owner**: DLUHC Finance Director

**Goal Statement**: Demonstrate a minimum 40% reduction in total cost of ownership for local authorities using the shared platform compared to independent IoT infrastructure procurement, validated by NAO-accepted cost comparison methodology.

**Why This Matters**: Provides the compelling financial case for local authority adoption (SD-3) and VfM evidence for HM Treasury.

**Success Metrics**:
- **Primary Metric**: Cost per sensor per year on shared platform vs. independent deployment benchmark
- **Secondary Metrics**:
  - Procurement time reduction (days from requirement to deployed sensor)
  - Operational staff time saved per authority

**Baseline**: Average LA independent IoT deployment cost: £150-200 per sensor per year
**Target**: Shared platform cost: £60-90 per sensor per year (40-60% reduction)
**Measurement Method**: Cost comparison study, quarterly financial reporting

---

## Goal-to-Outcome Mapping

### Outcome O-1: Unified National IoT Data Layer for Urban Services

**Supported Goals**: G-1, G-3

**Outcome Statement**: A functioning national IoT data platform serving 20+ local authorities, publishing open data, and providing the foundational sensor infrastructure for the wider SDG 11 programme.

**Measurement Details**:
- **KPI**: Local authorities connected and actively publishing sensor data
- **Current Value**: 0
- **Target Value**: 20+ authorities, 10,000+ sensors
- **Measurement Frequency**: Monthly
- **Data Source**: Platform analytics
- **Report Owner**: Platform Service Owner

**Business Value**:
- **Financial Impact**: £30-50M cumulative savings across local authorities over 5 years through shared infrastructure
- **Strategic Impact**: First national urban IoT data layer, enabling cross-authority benchmarking and urban intelligence
- **Operational Impact**: Standardised IoT operations reducing per-authority management overhead
- **Citizen Impact**: Better urban services informed by comprehensive sensor data

---

### Outcome O-2: Trusted, Secure Urban Sensing Infrastructure

**Supported Goals**: G-2, G-3

**Outcome Statement**: A demonstrably secure and privacy-respecting IoT platform that maintains citizen trust and meets the highest standards of IoT security and data protection.

**Measurement Details**:
- **KPI**: Zero critical security incidents; public trust score maintained above 60%
- **Current Value**: N/A (new platform)
- **Target Value**: Zero critical incidents, trust score >60%
- **Measurement Frequency**: Monthly (security), Annually (trust survey)
- **Data Source**: Security operations centre, citizen survey
- **Report Owner**: Cyber Security Lead

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Levelling up through smart infrastructure | G-1 | 20 LAs onboarded | O-1 | Unified national IoT layer |
| Minister | SD-1 | Levelling up through smart infrastructure | G-3 | Open data published | O-1 | Unified national IoT layer |
| NCSC | SD-2 | Securing IoT infrastructure | G-2 | ETSI compliance | O-2 | Trusted secure platform |
| LA Chief Execs | SD-3 | Reducing fragmentation and cost | G-1 | 20 LAs onboarded | O-1 | Unified national IoT layer |
| LA Chief Execs | SD-3 | Reducing fragmentation and cost | G-4 | 40% cost reduction | O-1 | Unified national IoT layer |
| ICO | SD-4 | Privacy protection | G-3 | Open data (transparency) | O-2 | Trusted secure platform |
| IoT Manufacturers | SD-5 | Open market access | G-2 | Device certification | O-2 | Trusted secure platform |
| Privacy Groups | SD-6 | Preventing surveillance | G-3 | Open data (transparency) | O-2 | Trusted secure platform |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Local authority operational teams want granular, high-frequency sensor data for service optimisation, but privacy campaign groups (SD-6) and ICO (SD-4) want data minimisation and aggregation at source to prevent surveillance capability.
  - **Resolution Strategy**: Implement privacy by design with configurable aggregation levels. Granular data available only for specific, DPIA-assessed use cases with time-limited retention. Aggregated data is the default for analytics and open data publication.

- **Conflict 2**: NCSC (SD-2) wants strict device security certification that may exclude smaller manufacturers, but IoT Manufacturers (SD-5) want accessible certification that SMEs can afford.
  - **Resolution Strategy**: Tiered certification with a lightweight self-assessment for low-risk sensors and full third-party assessment for devices in critical infrastructure. DCMS-funded certification support for UK SMEs.

**Synergies**:

- **Synergy 1**: Minister's Levelling Up driver (SD-1) aligns perfectly with LA cost reduction driver (SD-3) — shared infrastructure benefits smaller authorities most
- **Synergy 2**: ICO privacy requirements (SD-4) and Privacy Groups' concerns (SD-6) are satisfied by the same architectural decision — privacy-preserving analytics with published DPIAs

---

## Communication & Engagement Plan

### Local Authority Chief Executives

**Primary Message**: The Smart City IoT Platform reduces your costs by 40% while giving you access to a national sensor network — you keep control of your data and deployment priorities.

**Key Talking Points**:
- Cost savings: £60-90 per sensor per year vs £150-200 independently
- Data ownership: Your data stays yours, you choose what to share
- Security: NCSC-assured IoT infrastructure you don't have to build yourself

**Communication Frequency**: Monthly
**Preferred Channel**: Local Government Association events, CDDO roundtables, direct briefings
**Success Story**: "Council X reduced environmental monitoring costs by 50% and improved coverage from 12 sensors to 200"

---

## Change Impact Assessment

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| LA Digital Teams | Managing independent IoT platforms | Adopting shared platform, managing local deployment | HIGH | MEDIUM | Transition support, training, co-design of platform features |
| IoT Vendors | Selling proprietary platforms to individual LAs | Certifying devices for open platform | HIGH | HIGH | Open standards, vendor engagement programme, market opportunity messaging |
| Urban Residents | Unaware of sensor deployments | Informed through transparency measures | LOW | LOW | Clear communication, published DPIAs, open data |

### Change Readiness

**Champions**:
- Geospatial Commission — directly supports their national spatial data strategy
- NCSC — sets the IoT security standard they've been advocating

**Fence-sitters**:
- Mid-tier local authorities — need clear cost-benefit evidence and peer examples

**Resisters**:
- Local authorities with recent proprietary IoT investments — need migration path and transition funding
- Privacy campaign groups — need genuine engagement, not PR

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Local Authority Adoption Below Target

**Related Stakeholders**: LA Chief Executives, Minister
**Risk Description**: Fewer than 20 local authorities adopt the platform in Year 1 due to procurement timescales, existing contracts, or perceived loss of autonomy
**Impact on Goals**: G-1 (adoption target), G-4 (cost reduction requires scale)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Early adopter programme with funded transition support; peer-to-peer advocacy through LGA; flexible onboarding that accommodates existing contracts
**Contingency Plan**: Extend Phase 1 timeline, focus on quality of adoption over quantity

### Risk R-2: Privacy Controversy Damages Public Trust

**Related Stakeholders**: Privacy Groups, ICO, Minister, Urban Residents
**Risk Description**: Media coverage frames the IoT platform as government surveillance, damaging citizen trust and political support
**Impact on Goals**: G-3 (open data undermined by controversy), G-1 (political support withdrawn)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Proactive privacy engagement from day one; published DPIAs; citizen data ethics panel; invite privacy groups as critical friends
**Contingency Plan**: Commissioned independent privacy audit; Ministerial statement on data use constraints

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | Solution Architect | SRO | NCSC, CDDO, Geospatial Commission | All stakeholders |
| Budget approval | Finance Director | DLUHC Permanent Secretary | HM Treasury | All stakeholders |
| Device certification | Cyber Security Lead | NCSC Liaison | IoT Manufacturers | Local Authorities |
| Privacy approach | Data Ethics Team | DLUHC SIRO | ICO, Privacy Groups | All stakeholders |
| Local authority onboarding | Platform Service Owner | SRO | LA Chief Executive, LA Digital | Minister |
| Go-live decision | SRO | DLUHC Permanent Secretary | Steering Committee | All stakeholders |

### Escalation Path

1. **Level 1**: Product Manager / Service Owner (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, cross-stakeholder conflicts)
3. **Level 3**: SRO / DLUHC Permanent Secretary (strategic direction, major conflicts, Ministerial implications)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| DLUHC CDO | PENDING | | PENDING |
| NCSC Liaison | PENDING | | PENDING |
| ICO Representative | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| DLUHC Chief Digital Officer | | | |
| Enterprise Architect | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| NCSC Connected Places Cyber Security Principles | Guidance | NCSC | IoT security in urban infrastructure | N/A — external reference |
| ETSI EN 303 645 | Standard | ETSI | IoT baseline security | N/A — external reference |
| Geospatial Commission Strategy | Strategy | Cabinet Office | National spatial data infrastructure | N/A — external reference |
| ICO Smart Cities Guidance | Guidance | ICO | Privacy in urban sensing | N/A — external reference |
| Levelling Up White Paper | Policy | DLUHC | Regional technology equity | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart City IoT Platform (Project 001)
**Model**: Claude Opus 4.6
