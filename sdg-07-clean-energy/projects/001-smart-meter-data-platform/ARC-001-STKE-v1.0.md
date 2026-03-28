# Stakeholder Drivers & Goals Analysis: Smart Meter Data Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Smart Meter Data Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Smart Meter Data Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Smart Meter Programme Board, DESNZ Digital, CDDO, Ofgem, DCC |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Smart Meter Data Platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The platform will provide national-scale collection, processing, and analytics of data from 53 million smart meters across Great Britain.

### Key Findings

The Smart Meter Data Platform operates at the intersection of consumer data rights and national energy policy. The strongest alignment exists between DESNZ policy objectives (using meter data to drive Net Zero) and Ofgem's regulatory mandate (ensuring data-driven energy market competition). The most significant tension exists between the ambition for granular data analytics to support energy policy and the consumer privacy imperative — half-hourly consumption data reveals intimate details of household life. DCC's role as the existing data communications infrastructure creates both an enabler (established data flows) and a constraint (protocol limitations and cost structures). Energy suppliers occupy a complex position as both data sources and potential competitors for consumer engagement.

### Critical Success Factors

- Ingest and process 2.5 billion half-hourly meter readings per day without data loss at sustained throughput
- Maintain consumer trust through transparent data use, robust consent management, and visible privacy controls
- Deliver actionable energy insights to householders within 4 hours of meter reading collection
- Achieve GDS service assessment pass at Beta to maintain CDDO confidence and unlock continued funding
- Integrate with DCC infrastructure within the constraints of the Smart Energy Code

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for a national smart meter data platform and the strategic value of energy consumption analytics for Net Zero. Significant tensions between policy ambition for data access, consumer privacy expectations, energy supplier commercial interests, and DCC's role as intermediary infrastructure provider. The scale of data processing (53 million meters) creates genuine technical risk that concerns all stakeholders.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Energy Security and Net Zero | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, Net Zero alignment |
| DESNZ Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Smart Meter Data Platform | Programme Sponsor (DESNZ) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DESNZ Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance, digital strategy |
| Smart Meter Programme Director | End-to-end programme delivery | HIGH | HIGH | Manage Closely — Programme governance, supplier management |
| DESNZ SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DESNZ Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| DESNZ Data Protection Officer | Data privacy compliance | MEDIUM | HIGH | Keep Informed — DPIA process, consent framework |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Delivery cadence, risks | MEDIUM | HIGH | Keep Informed — Stand-ups, risk escalation |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| GDS Service Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| Ofgem | Regulator | Energy market regulation, data access framework | HIGH | HIGH |
| Data Communications Company (DCC) | Smart meter infrastructure | Data transport provider | HIGH | HIGH |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Information Commissioner's Office (ICO) | Regulator | Data protection oversight | HIGH | MEDIUM |
| Energy suppliers (Big Six + independents) | Licensed suppliers | Data sources and consumers | HIGH | HIGH |
| Distribution Network Operators (DNOs) | Network operators | Grid data consumers | MEDIUM | HIGH |
| National Grid ESO | System operator | Grid balancing data consumer | MEDIUM | HIGH |
| Householders (53M meters) | Citizens | Data subjects and service users | LOW | HIGH |
| Citizens Advice | Charity | Consumer advocacy | LOW | HIGH |
| Fuel poverty charities (NEA, Age UK) | Charities | Vulnerable consumer advocacy | LOW | HIGH |
| Smart Energy GB | Campaign body | Public communications | LOW | MEDIUM |
| Academic researchers | Universities | Energy research data users | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end data platform service and user outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination and policy implementation | HIGH / MEDIUM | Keep Satisfied — Security compliance gates, incident reporting |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk, signs off risk acceptance | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security, NIS assessment, GovAssure liaison | MEDIUM / HIGH | Keep Informed — Security architecture reviews, pen test scheduling |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • Secretary of     │
        │  • NAO              │    State (DESNZ)    │
        │  • ICO              │  • Permanent Sec.   │
        │  • DESNZ SIRO       │  • SRO              │
        │  • DESNZ Finance    │  • CDO (DESNZ)      │
 P      │  • CDDO             │  • Smart Meter Dir  │
 O      │  • SSRO / DSO       │  • Ofgem            │
 W      │                     │  • DCC              │
 E      │                     │  • Energy Suppliers  │
 R      ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Smart Energy GB  │  • Householders     │
        │  • Academic         │  • Citizens Advice  │
        │    Researchers      │  • Fuel poverty     │
        │                     │    charities (NEA)  │
        │                     │  • DNOs             │
        │                     │  • National Grid ESO│
        │                     │  • Product Manager  │
        │                     │  • Delivery Manager │
        │                     │  • GDS Assessment   │
        │                     │  • DPO              │
        │                     │  • Cyber Sec Lead   │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State for Energy Security and Net Zero — Net Zero Delivery

**Stakeholder**: Secretary of State for Energy Security and Net Zero

**Driver Category**: STRATEGIC

**Driver Statement**: Demonstrate that the UK's £13.5 billion smart meter rollout delivers tangible benefits for consumers and measurable contribution to Net Zero targets. The smart meter programme has faced sustained criticism from NAO and Public Accounts Committee for delayed benefits realisation.

**Context & Background**: The smart meter programme was originally projected to deliver £19.5 billion in benefits. Multiple NAO reports have highlighted benefits shortfalls and cost overruns. Ministerial reputation depends on showing that the data generated by 53 million meters is being used effectively for energy policy, consumer empowerment, and carbon reduction.

**Driver Intensity**: CRITICAL

**Enablers**:
- A functioning national data platform that converts raw meter data into policy-actionable insights
- Consumer engagement features that demonstrate tangible household benefit

**Blockers**:
- Consumer privacy concerns that limit data access
- Technical complexity of processing data at national scale
- Energy supplier resistance to data sharing beyond regulatory minimums

**Related Stakeholders**: Ofgem, NAO, DCC, Householders

---

### SD-2: Ofgem — Data-Driven Energy Market Competition

**Stakeholder**: Ofgem

**Driver Category**: COMPLIANCE

**Driver Statement**: Enable a competitive energy market where consumers can make informed switching decisions based on accurate consumption data, and where innovative energy services can emerge using smart meter data — while protecting consumers from data misuse.

**Context & Background**: Ofgem's data access and privacy framework seeks to balance innovation with protection. The regulator wants to see smart meter data enabling new tariff products, demand flexibility services, and consumer engagement — but within a controlled regulatory framework. The Energy Act 2023 gave Ofgem new powers to mandate data sharing arrangements.

**Driver Intensity**: HIGH

**Enablers**:
- Standardised data access APIs that enable market innovation
- Robust consent management that gives consumers genuine control

**Blockers**:
- Fragmented data access across energy suppliers
- Consumer distrust of energy data sharing
- Legacy settlement systems that cannot use half-hourly data

**Related Stakeholders**: Energy suppliers, DCC, ICO, Householders

---

### SD-3: Data Communications Company (DCC) — Infrastructure Utilisation

**Stakeholder**: Data Communications Company (DCC)

**Driver Category**: OPERATIONAL

**Driver Statement**: Maximise the utilisation and value of the DCC smart meter communications infrastructure, demonstrating that the £2.5 billion+ investment in the WAN infrastructure delivers ongoing value beyond basic meter reading.

**Context & Background**: DCC operates the communications infrastructure connecting 53 million smart meters. Their costs are passed through to energy consumers via supplier charges. DCC needs to demonstrate that their infrastructure supports a growing ecosystem of value-added services to justify ongoing operational costs.

**Driver Intensity**: HIGH

**Enablers**:
- New data platform consuming DCC data at scale, validating the infrastructure investment
- Clear technical interface specifications that reduce integration cost

**Blockers**:
- Platform bypassing DCC infrastructure (e.g., using supplier-side data collection)
- Technical limitations of the current DCC WAN capacity
- Cost allocation disputes for enhanced data services

**Related Stakeholders**: Ofgem, Energy suppliers, DESNZ

---

### SD-4: Energy Suppliers — Commercial Data Control

**Stakeholder**: Energy suppliers (Big Six and independents)

**Driver Category**: FINANCIAL

**Driver Statement**: Maintain commercial advantage derived from customer energy data while complying with regulatory obligations to share data. Minimise additional costs imposed by government data platform requirements.

**Context & Background**: Energy suppliers currently hold the primary relationship with consumers and have invested heavily in their own smart meter data analytics. A national government data platform is perceived by some suppliers as a competitive threat — potentially disintermediating them from consumer engagement. Suppliers also bear the cost of DCC charges, which they seek to minimise.

**Driver Intensity**: HIGH

**Enablers**:
- Clear data sharing scope limited to regulatory purposes (not commercial displacement)
- Standardised interfaces that reduce supplier integration cost

**Blockers**:
- Government platform competing for consumer attention and engagement
- Unfunded mandates requiring suppliers to invest in new data sharing interfaces
- Risk of data leakage exposing commercially sensitive customer information

**Related Stakeholders**: Ofgem, DCC, Householders

---

### SD-5: Householders — Energy Cost Reduction and Privacy

**Stakeholder**: Householders (53 million smart meters)

**Driver Category**: CUSTOMER

**Driver Statement**: Reduce energy bills through better understanding of consumption patterns, access tailored energy efficiency advice, and maintain control over who can access personal energy data.

**Context & Background**: Energy costs have dominated household budgets since the 2022 energy crisis. The average dual-fuel bill exceeds £1,800/year. Householders want tools that help them reduce consumption but are wary of surveillance. Smart Energy GB research shows 72% of consumers support the smart meter programme but only 34% actively use their data. Trust in energy data handling is fragile — any perceived misuse could undermine public acceptance of the entire programme.

**Driver Intensity**: CRITICAL

**Enablers**:
- Intuitive consumer interface showing real-time consumption and cost
- Personalised energy saving recommendations
- Transparent, easy-to-use consent and privacy controls

**Blockers**:
- Complex energy data that consumers cannot interpret
- Lack of trust in government or supplier data handling
- Digital exclusion — fuel-poor households least likely to access online services

**Related Stakeholders**: Citizens Advice, Fuel poverty charities, Energy suppliers, ICO

---

### SD-6: National Grid ESO — Grid Balancing Intelligence

**Stakeholder**: National Grid ESO

**Driver Category**: OPERATIONAL

**Driver Statement**: Access aggregated demand-side data at sufficient granularity and timeliness to improve electricity system balancing, support demand flexibility services, and manage the integration of increasing volumes of intermittent renewable generation.

**Context & Background**: As renewable generation grows (target 50GW offshore wind by 2030), grid balancing becomes more complex. Smart meter demand data, aggregated at grid supply point level, provides crucial visibility into consumption patterns that help ESO forecast demand and manage flexibility. Currently this data is available only through estimated profiles — actual half-hourly data would transform balancing capability.

**Driver Intensity**: HIGH

**Enablers**:
- Near-real-time aggregated demand data by grid supply point
- Historical consumption profiles for demand forecasting models

**Blockers**:
- Privacy constraints limiting granularity of shared data
- Latency in DCC data collection (currently up to 24 hours for some readings)
- Data quality issues with missing or estimated reads

**Related Stakeholders**: DNOs, DCC, Ofgem

---

## Driver-to-Goal Mapping

### Goal G-1: Deliver National-Scale Meter Data Ingestion

**Derived From Drivers**: SD-1, SD-3, SD-6

**Goal Owner**: Smart Meter Programme Director

**Goal Statement**: Ingest, validate, and store half-hourly consumption data from 53 million smart meters within 4 hours of collection, achieving 99.5% data completeness by Q4 2027.

**Why This Matters**: Without reliable data ingestion at national scale, no downstream analytics, consumer services, or policy insights are possible. This is the foundation capability upon which all value depends.

**Success Metrics**:
- **Primary Metric**: Data completeness rate (target: 99.5% of expected readings received within 4 hours)
- **Secondary Metrics**:
  - Ingestion throughput (2.5 billion reads/day sustained)
  - Data validation pass rate (target: 99.9% of reads pass validation)

**Baseline**: No centralised government data platform exists; suppliers collect data independently with variable completeness.

**Target**: 99.5% data completeness within 4 hours of collection window close.

**Measurement Method**: Automated monitoring of ingestion pipeline comparing expected readings (based on meter register) against actual readings received.

**Dependencies**:
- DCC data feeds operational and stable
- Energy supplier data sharing agreements in place
- Infrastructure scaled for national data volumes

**Risks to Achievement**:
- DCC WAN capacity constraints limiting data throughput
- Meter communication failures in areas with poor WAN coverage

---

### Goal G-2: Empower Consumers with Energy Insights

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: Service Owner

**Goal Statement**: Provide 10 million registered householders with personalised energy consumption insights, saving an average of £50/year per household through behavioural changes, by Q2 2028.

**Why This Matters**: Consumer benefit is the primary justification for the smart meter programme. If householders cannot see and act on their data, the programme fails its stated purpose and Ministerial credibility is damaged.

**Success Metrics**:
- **Primary Metric**: Number of registered consumers actively using the platform monthly (target: 10M)
- **Secondary Metrics**:
  - Average consumption reduction per active user (target: 3-5%)
  - Consumer satisfaction score (target: 4.0/5.0)

**Baseline**: Smart Energy GB reports 34% of smart meter households actively use their data.

**Target**: 10 million registered users with monthly active engagement; measurable consumption reduction.

**Measurement Method**: Platform analytics (registrations, monthly active users); consumption trend analysis comparing pre/post registration usage.

**Dependencies**:
- Consumer interface designed and tested with representative users
- DCC consent framework implemented for granular data access
- Energy supplier cooperation in directing consumers to the platform

**Risks to Achievement**:
- Consumer apathy — existing In-Home Displays already provide basic data
- Privacy concerns deterring registration
- Energy supplier resistance to directing consumers to a government platform

---

### Goal G-3: Enable Regulatory and Policy Analytics

**Derived From Drivers**: SD-1, SD-2, SD-6

**Goal Owner**: DESNZ Chief Analyst

**Goal Statement**: Deliver anonymised, aggregated energy consumption analytics to DESNZ, Ofgem, and National Grid ESO for policy evaluation, market monitoring, and grid balancing improvement by Q1 2028.

**Why This Matters**: The strategic rationale for a government data platform (rather than relying on supplier data) is the ability to produce cross-supplier, national-level analytics for policy purposes. This capability justifies the investment and differentiates the platform from commercial alternatives.

**Success Metrics**:
- **Primary Metric**: Number of policy-ready analytics products delivered (target: 5 core datasets)
- **Secondary Metrics**:
  - Time from data collection to policy dashboard availability (target: < 24 hours)
  - Number of government users accessing analytics (target: 200+ across DESNZ, Ofgem, ESO)

**Baseline**: No cross-supplier national consumption analytics exist outside settlement data (which is aggregated and delayed).

**Target**: 5 core analytics products covering consumption by region, fuel poverty indicators, demand flexibility potential, renewable self-generation impact, and carbon intensity correlation.

**Measurement Method**: Analytics platform usage metrics; policy team feedback surveys; citation in published policy documents.

**Dependencies**:
- Data ingestion at national scale (G-1)
- Anonymisation pipeline validated by ICO guidance
- Data sharing agreements with Ofgem and ESO

**Risks to Achievement**:
- Privacy constraints limiting analytical granularity
- Data quality insufficient for policy-grade analytics
- Resource constraints in DESNZ analytical teams

---

### Goal G-4: Maintain Consumer Privacy and Trust

**Derived From Drivers**: SD-2, SD-4, SD-5

**Goal Owner**: DESNZ Data Protection Officer

**Goal Statement**: Implement the DCC consent framework and achieve an ICO-endorsed privacy assessment, ensuring zero data privacy incidents and maintaining consumer trust scores above 70% throughout the programme by Q4 2027.

**Why This Matters**: Consumer trust is the foundation of the entire smart meter data ecosystem. A single high-profile privacy incident could undermine public acceptance of smart meters, damage the government's broader data sharing agenda, and trigger regulatory intervention.

**Success Metrics**:
- **Primary Metric**: Zero reportable data privacy incidents
- **Secondary Metrics**:
  - Consumer trust survey score (target: >70% trust in data handling)
  - Consent opt-in rate for granular data sharing (target: >50% of registered users)

**Baseline**: Smart Energy GB research shows 62% of consumers trust that their smart meter data is handled responsibly.

**Target**: Zero reportable incidents; trust score >70%; consent opt-in >50%.

**Measurement Method**: ICO incident reports; quarterly consumer trust survey; consent management system analytics.

**Dependencies**:
- DCC consent framework integration complete
- DPIA completed and approved by ICO
- Privacy-by-design architecture validated

**Risks to Achievement**:
- Data breach due to cyber attack or insider threat
- Energy supplier data handling incident attributed to the platform
- Negative media coverage of government data collection

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Household Energy Consumption

**Supported Goals**: G-1, G-2

**Outcome Statement**: Reduce average household energy consumption by 3-5% for active platform users, contributing to 2.5 MtCO2e annual carbon reduction by 2030.

**Measurement Details**:
- **KPI**: Average consumption reduction per active household (kWh/year)
- **Current Value**: Baseline consumption at registration
- **Target Value**: 3-5% reduction within 12 months of registration
- **Measurement Frequency**: Monthly
- **Data Source**: Smart meter consumption data (before/after comparison)
- **Report Owner**: DESNZ Chief Analyst

**Business Value**:
- **Financial Impact**: £500M aggregate consumer savings per year (10M households x £50 average saving)
- **Strategic Impact**: Demonstrates tangible smart meter programme benefit; supports Net Zero carbon budgets
- **Operational Impact**: Reduced peak demand reduces wholesale electricity costs
- **Customer Impact**: Measurable bill reduction, improved energy literacy

**Timeline**:
- **Phase 1 (Months 1-6)**: Platform launch, 1M registrations, initial engagement analytics
- **Phase 2 (Months 7-12)**: 5M registrations, first consumption impact data available
- **Phase 3 (Months 13-24)**: 10M registrations, statistically significant consumption reduction measured
- **Sustainment (Year 3+)**: Maintain engagement, expand features, deepen savings

### Outcome O-2: Data-Driven Energy Policy

**Supported Goals**: G-1, G-3

**Outcome Statement**: Deliver national energy consumption analytics that directly inform at least 3 major policy decisions per year, replacing estimated data with actual meter data.

**Measurement Details**:
- **KPI**: Number of published policy documents citing platform analytics
- **Current Value**: 0 (platform does not exist)
- **Target Value**: 3+ policy documents per year
- **Measurement Frequency**: Annually
- **Data Source**: DESNZ policy publication records
- **Report Owner**: DESNZ Policy Director

### Outcome O-3: Maintained Consumer Trust in Smart Metering

**Supported Goals**: G-4

**Outcome Statement**: Maintain public trust in smart meter data handling above 70%, enabling continued data sharing and programme expansion.

**Measurement Details**:
- **KPI**: Consumer trust survey score
- **Current Value**: 62% (Smart Energy GB baseline)
- **Target Value**: >70%
- **Measurement Frequency**: Quarterly
- **Data Source**: Consumer trust survey (representative sample, 2000+ respondents)
- **Report Owner**: DESNZ Communications Director

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Net Zero delivery | G-1 | National data ingestion | O-1 | Reduced consumption |
| Secretary of State | SD-1 | Net Zero delivery | G-2 | Consumer insights | O-1 | Reduced consumption |
| Secretary of State | SD-1 | Net Zero delivery | G-3 | Policy analytics | O-2 | Data-driven policy |
| Ofgem | SD-2 | Market competition | G-3 | Policy analytics | O-2 | Data-driven policy |
| Ofgem | SD-2 | Market competition | G-4 | Privacy and trust | O-3 | Consumer trust |
| DCC | SD-3 | Infrastructure value | G-1 | National data ingestion | O-1 | Reduced consumption |
| Energy suppliers | SD-4 | Commercial control | G-4 | Privacy and trust | O-3 | Consumer trust |
| Householders | SD-5 | Cost reduction and privacy | G-2 | Consumer insights | O-1 | Reduced consumption |
| Householders | SD-5 | Cost reduction and privacy | G-4 | Privacy and trust | O-3 | Consumer trust |
| National Grid ESO | SD-6 | Grid balancing | G-1 | National data ingestion | O-2 | Data-driven policy |
| National Grid ESO | SD-6 | Grid balancing | G-3 | Policy analytics | O-2 | Data-driven policy |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DESNZ (SD-1) wants maximum data granularity for policy analytics, but Householders (SD-5) and ICO want data minimisation and explicit consent for granular access.
  - **Resolution Strategy**: Tiered data access — monthly aggregates for policy without consent; half-hourly data only with explicit consumer consent via DCC framework. Anonymised aggregates for policy analytics where individual consent is not practical.

- **Conflict 2**: Energy suppliers (SD-4) want to maintain commercial control of customer data, but Ofgem (SD-2) and DESNZ (SD-1) want centralised government access for market monitoring and policy.
  - **Resolution Strategy**: Regulatory mandate for data sharing using Energy Act 2023 powers, with clear scope limitation — government platform for policy and consumer empowerment, not commercial competition. Supplier concerns addressed through data use transparency and governance board participation.

- **Conflict 3**: National Grid ESO (SD-6) needs near-real-time data for grid balancing, but DCC (SD-3) infrastructure has latency limitations (up to 24 hours for some meter types).
  - **Resolution Strategy**: Phased approach — use available near-real-time data from SMETS2 meters first; work with DCC on infrastructure upgrades for remaining meters. Accept estimated profiles as fallback for meters with high latency.

**Synergies**:

- **Synergy 1**: DESNZ (SD-1) and Householders (SD-5) both benefit from consumer energy insights — achieving G-2 satisfies both the Ministerial need for demonstrable programme benefits and the consumer need for bill reduction tools.
- **Synergy 2**: Ofgem (SD-2) and National Grid ESO (SD-6) both benefit from improved data quality — achieving G-1 and G-3 supports both market regulation and grid balancing improvement.

---

## Communication & Engagement Plan

### Secretary of State for Energy Security and Net Zero

**Primary Message**: The Smart Meter Data Platform will convert the UK's £13.5 billion smart meter investment into tangible consumer benefits and policy intelligence, directly supporting Net Zero delivery.

**Key Talking Points**:
- 10 million households empowered with personalised energy insights
- £500M aggregate annual consumer savings through behavioural change
- First-ever national-scale energy consumption analytics for policy evaluation

**Communication Frequency**: Monthly (via Ministerial briefing pack)
**Preferred Channel**: Ministerial briefing paper, quarterly programme board
**Success Story**: "10 million households using smart meter data to cut bills and carbon"

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| DCC | Data transport only | Data transport + platform integration | MEDIUM | LOW | Clear interface specs, phased integration |
| Energy suppliers | Own customer data exclusively | Share regulatory data with government platform | HIGH | HIGH | Regulatory mandate, clear scope limits, governance board |
| Householders | Limited data access via IHD | Rich online analytics and insights | MEDIUM | LOW | Usability testing, privacy-first design |
| National Grid ESO | Estimated demand profiles | Actual consumption data for balancing | MEDIUM | LOW | Phased data availability, format compatibility |
| Ofgem | Limited market visibility | National consumption analytics | LOW | LOW | Stakeholder on governance board |

### Change Readiness

**Champions** (Enthusiastic supporters):
- DESNZ Policy team — want data for Net Zero policy evaluation
- National Grid ESO — want actual consumption data for grid balancing
- Fuel poverty charities — want better identification of vulnerable households

**Fence-sitters** (Neutral, need convincing):
- DCC — supportive in principle but concerned about additional infrastructure costs and scope
- Smaller energy suppliers — supportive of market transparency but concerned about integration costs

**Resisters** (Opposed or skeptical):
- Large energy suppliers — concerned about commercial data advantage erosion
- Privacy advocates — concerned about government access to household energy data

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Energy Supplier Non-Cooperation

**Related Stakeholders**: Energy suppliers, Ofgem
**Risk Description**: Large energy suppliers delay or obstruct data sharing, citing commercial sensitivity or technical constraints, undermining data completeness targets.
**Impact on Goals**: G-1 (data completeness), G-2 (consumer insights depend on complete data)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Secure Ofgem regulatory mandate under Energy Act 2023 powers; early supplier engagement through industry working groups; phased approach starting with willing suppliers.
**Contingency Plan**: Use DCC-route data collection (bypasses supplier systems) if supplier cooperation fails.

### Risk R-2: Consumer Privacy Incident

**Related Stakeholders**: Householders, ICO, Media
**Risk Description**: A data breach or misuse incident destroys consumer trust, triggering ICO investigation, negative media coverage, and consumer registration decline.
**Impact on Goals**: G-4 (trust), G-2 (consumer adoption)
**Probability**: LOW
**Impact**: CRITICAL
**Mitigation Strategy**: Privacy-by-design architecture; DCC consent framework; NCSC security assessment; regular penetration testing; incident response plan with ICO notification procedures.
**Contingency Plan**: Immediate containment, transparent public communication, ICO cooperation, independent security review.

### Risk R-3: DCC Capacity Constraints

**Related Stakeholders**: DCC, Energy suppliers, National Grid ESO
**Risk Description**: DCC WAN infrastructure cannot support the additional data traffic required for near-real-time government data feeds alongside existing supplier data flows.
**Impact on Goals**: G-1 (ingestion timeliness), G-6 (grid balancing data latency)
**Probability**: MEDIUM
**Impact**: MEDIUM
**Mitigation Strategy**: Early DCC capacity assessment; phased rollout starting with subset of meters; alternative data collection routes (supplier-side aggregation) as fallback.
**Contingency Plan**: Accept longer latency (24-hour instead of 4-hour) until DCC capacity upgraded; use estimated profiles as interim.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DESNZ Finance Director | SRO | HM Treasury, CDDO | All stakeholders |
| Data access scope | DESNZ DPO | SRO | Ofgem, ICO, Energy suppliers | Householders |
| DCC integration approach | Technical Architect | Smart Meter Programme Director | DCC, Ofgem | Suppliers |
| Consumer feature prioritisation | Product Manager | Service Owner | Citizens Advice, Householders | All |
| Go/No-go for go-live | SRO | Permanent Secretary | Steering Committee | All |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, supplier issues)
3. **Level 3**: SRO / Permanent Secretary (strategic direction, Ministerial concerns, regulatory issues)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| Ofgem representative | PENDING | | PENDING |
| DCC representative | PENDING | | PENDING |
| Consumer representative | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| DESNZ CDO | | | |
| Enterprise Architect | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Smart Energy Code | Industry Code | SEC Company | Data access framework, consent model | N/A — external reference |
| Ofgem Data Access and Privacy Framework | Regulatory | Ofgem | Consumer data rights, access levels | N/A — external reference |
| Energy Act 2023 | Legislation | legislation.gov.uk | Data sharing powers, smart meter governance | N/A — external reference |
| NAO Smart Meter Programme reports | Audit | NAO | Benefits realisation, cost analysis | N/A — external reference |
| Smart Energy GB public attitudes research | Research | Smart Energy GB | Consumer trust and engagement metrics | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Smart Meter Data Platform (Project 001)
**Model**: Claude Opus 4.6 (1M context)
