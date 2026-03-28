# Stakeholder Drivers & Goals Analysis: NHS Appointment Booking Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | NHS Appointment Booking Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, NHS Appointment Booking Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NHS Appointment Booking Programme Board, DHSC Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the NHS Appointment Booking Platform programme, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The NHS Appointment Booking Platform faces a fundamental tension between Ministerial urgency to reduce waiting times visibly and the operational complexity of integrating with hundreds of NHS Trust Patient Administration Systems, GP clinical systems, and the existing e-Referral Service. The strongest alignment exists around improving patient experience and reducing Did Not Attend (DNA) rates — these goals satisfy political, clinical, operational, and financial drivers simultaneously. The most significant conflict is between the ambition for a single national booking platform and the autonomy of individual NHS Trusts and GP practices, which have invested heavily in existing booking solutions.

### Critical Success Factors

- Seamless integration with existing NHS national services (PDS, e-RS, GP Connect) without disruption to current booking workflows
- Demonstrable reduction in patient waiting times within 12 months to maintain Ministerial sponsorship
- Achieve GDS service assessment pass at Beta to maintain CDDO confidence and unlock continued funding
- DNA rate reduction of at least 20% through intelligent reminder and rebooking capabilities
- NHS Trust and GP practice adoption exceeding 50% within 18 months of launch

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for improved appointment booking and reduced waiting times, but significant tensions between national standardisation (DHSC/NHS England) and local autonomy (NHS Trusts/GP Practices), speed of delivery (Ministerial pressure) versus integration complexity (technical teams), and the scope of transformation (comprehensive platform versus incremental improvement to e-RS).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Health and Social Care | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DHSC Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Appointment Booking Programme | Programme Sponsor (DHSC) | HIGH | HIGH | Manage Closely — Weekly programme board |
| NHS England Chief Digital Officer | NHS Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance, NHS digital strategy |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews, patient outcomes |
| NHS England Chief Nursing Officer | Clinical standards and patient safety | HIGH | MEDIUM | Keep Satisfied — Clinical safety governance |
| DHSC SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DHSC Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Delivery cadence, risks | MEDIUM | HIGH | Keep Informed — Stand-ups, risk escalation |
| Clinical Safety Officer | DCB0129/DCB0160 compliance | MEDIUM | HIGH | Keep Informed — Clinical safety governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| GDS Service Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Care Quality Commission (CQC) | Regulator | Quality of care oversight | HIGH | MEDIUM |
| NHS Trust Chief Executives | 220+ NHS Trusts | System adopters | HIGH | HIGH |
| Royal College of GPs | Professional body | Primary care representation | MEDIUM | HIGH |
| GP Practice Managers | 6,500+ GP Practices | Primary care operations | MEDIUM | HIGH |
| Patients and Carers | Citizens | Service users | LOW | HIGH |
| Healthwatch England | Statutory body | Patient advocacy | LOW | HIGH |
| NHS Providers | Membership organisation | Trust representation | MEDIUM | MEDIUM |
| British Medical Association (BMA) | Trade union/professional body | Clinician representation | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end booking service and patient outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and NHS policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination and policy | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security, CAF assessment | MEDIUM / HIGH | Keep Informed — Security architecture reviews, pen testing |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of     |
        |  * NAO              |    State (DHSC)     |
        |  * CQC              |  * Permanent Sec.   |
        |  * DHSC SIRO        |  * SRO              |
        |  * DHSC Finance Dir |  * NHS England CDO  |
        |  * CDDO             |  * Service Owner    |
 P      |  * SSRO / DSO       |  * NHS Trust CEs    |
 O      |  * Chief Nursing Off|                     |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * NHS Providers    |  * Patients/Carers  |
        |  * BMA              |  * Healthwatch      |
        |                     |  * GP Practice Mgrs |
        |                     |  * Royal College GPs|
        |                     |  * Product Manager  |
        |                     |  * Delivery Manager |
        |                     |  * Clinical Safety  |
        |                     |    Officer          |
        |                     |  * GDS Assessment   |
        +---------------------+---------------------+
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Secretary of State (DHSC) | HIGH | HIGH | Manage Closely | Ministerial briefings, PQ lines, quarterly review |
| DHSC Permanent Secretary | HIGH | HIGH | Manage Closely | Programme board, accounting officer assurance |
| SRO | HIGH | HIGH | Manage Closely | Weekly programme board, decision escalation |
| NHS England CDO | HIGH | HIGH | Manage Closely | Architecture governance, NHS digital strategy |
| Service Owner | HIGH | HIGH | Manage Closely | Fortnightly service reviews, patient outcomes |
| NHS Trust Chief Executives | HIGH | HIGH | Manage Closely | Trust engagement programme, integration governance |
| HM Treasury | HIGH | MEDIUM | Keep Satisfied | Business case updates, spending review submissions |
| NAO | HIGH | MEDIUM | Keep Satisfied | Audit readiness, value for money evidence |
| CQC | HIGH | MEDIUM | Keep Satisfied | Quality impact assessments |
| DHSC SIRO | HIGH | MEDIUM | Keep Satisfied | Risk acceptance, DPIA sign-off |
| DHSC Finance Director | HIGH | MEDIUM | Keep Satisfied | Monthly spend reports, business case tracking |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control submissions, assessment gates |
| Patients and Carers | LOW | HIGH | Keep Informed | User research, accessibility testing, NHS.UK updates |
| Healthwatch England | LOW | HIGH | Keep Informed | Quarterly stakeholder forum, patient insight sharing |
| GP Practice Managers | MEDIUM | HIGH | Keep Informed | Integration working group, training programme |
| Royal College of GPs | MEDIUM | HIGH | Keep Informed | Clinical advisory group, primary care pathway design |
| Product Manager | MEDIUM | HIGH | Keep Informed | Sprint reviews, roadmap co-creation |
| Clinical Safety Officer | MEDIUM | HIGH | Keep Informed | Clinical safety governance, hazard review |
| BMA | MEDIUM | MEDIUM | Monitor | Policy consultations, workforce impact assessment |
| NHS Providers | MEDIUM | MEDIUM | Monitor | Sector briefings, integration roadmap |

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Visible Reduction in NHS Waiting Times

**Stakeholder**: Secretary of State for Health and Social Care

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver visible, measurable reductions in NHS appointment waiting times and improve patient access to services, enabling positive responses to parliamentary questions, media scrutiny, and the government's NHS recovery plan commitments.

**Context & Background**:
NHS waiting lists reached record levels following the COVID-19 pandemic, with over 7.5 million patients on waiting lists. The elective care backlog has become a defining political issue. The Secretary of State needs demonstrable digital improvements to appointment booking as evidence of the government's NHS recovery plan delivering results. The SDG 3 alignment creates additional international reporting obligations.

**Driver Intensity**: CRITICAL

**Enablers**:

- Cross-government commitment to NHS digital transformation with ring-fenced funding
- NHS Long Term Plan digital-first mandate providing strategic cover
- Patient demand for digital booking (65% of patients prefer online booking per NHS survey data)

**Blockers**:

- NHS Trust resistance to national standardisation of booking systems
- Legacy PAS (Patient Administration Systems) with limited interoperability
- Competing priorities across NHS England (staff pay, infrastructure, social care)

**Related Stakeholders**: DHSC Permanent Secretary, NHS England CDO, HM Treasury

---

### SD-2: NHS Trust Chief Executives — Operational Autonomy and Local Flexibility

**Stakeholder**: NHS Trust Chief Executives (collectively)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Maintain operational autonomy over appointment scheduling, ensure any national platform integrates seamlessly with existing Trust PAS and clinical workflow systems, and avoid unfunded mandates that divert resources from frontline care.

**Context & Background**:
NHS Trusts have invested significantly in their own appointment booking and patient flow management systems, often deeply integrated with their PAS (Cerner, Epic, System C, etc.). Previous national IT programmes (NPfIT) failed in part because they underestimated local operational needs. Trust CEs are protective of their operational autonomy and sceptical of top-down national platforms that may not accommodate their specific clinical pathways.

**Driver Intensity**: HIGH

**Enablers**:

- Platform designed as a complementary layer rather than a replacement for Trust systems
- FHIR-based integration that works with existing PAS/EPR systems
- Trust involvement in design and piloting

**Blockers**:

- Perception of "another NPfIT" — national system imposed on local organisations
- Integration costs falling on Trust IT budgets
- Risk of disruption to existing booking workflows during transition

**Related Stakeholders**: NHS Providers, GP Practice Managers, BMA

---

### SD-3: Patients and Carers — Simple, Accessible Appointment Management

**Stakeholder**: Patients and Carers

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Access a single, simple digital service to find, book, change, and cancel NHS appointments across all care settings, with clear information about waiting times and appointment preparation, accessible to people of all abilities and digital confidence levels.

**Context & Background**:
Patients currently navigate a fragmented landscape of booking systems — NHS App for some GP services, individual Trust patient portals, telephone booking, e-RS for consultant referrals. The lack of a unified experience creates confusion, missed appointments, and wasted NHS resources. 38% of DNAs are attributed to patients being unable to rebook or cancel easily. Elderly patients, those with disabilities, and people with limited English face particular barriers.

**Driver Intensity**: HIGH

**Enablers**:

- NHS App as existing patient-facing channel with 30+ million registered users
- NHS login providing single sign-on for patient authentication
- Patient demand for digital booking demonstrated in NHS user research

**Blockers**:

- Digital exclusion — approximately 10 million adults in the UK have low digital skills
- Fragmented Trust systems providing inconsistent data quality for appointment availability
- Patient concerns about data privacy and security

**Related Stakeholders**: Healthwatch England, Royal College of GPs, Clinical Safety Officer

---

### SD-4: NHS England Chief Digital Officer — NHS Digital Strategy Alignment

**Stakeholder**: NHS England Chief Digital Officer

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Ensure the appointment booking platform exemplifies NHS digital strategy — built on open standards (HL7 FHIR), integrated with NHS national services, using NHS.UK Design System, and demonstrating the art of the possible for NHS digital transformation.

**Context & Background**:
NHS England's digital strategy positions interoperability and open standards as foundational. The appointment booking platform is a flagship programme that must demonstrate that modern, patient-centred digital services can be delivered nationally while respecting local operational needs. Success validates the FHIR-first strategy; failure undermines the broader digital transformation programme.

**Driver Intensity**: HIGH

**Enablers**:

- Existing NHS national service infrastructure (Spine, PDS, e-RS, GP Connect)
- NHS FHIR UK Core profiles maturing with strong vendor engagement
- NHS.UK Design System providing consistent patient-facing components

**Blockers**:

- Varying FHIR maturity across NHS Trust PAS/EPR vendors
- Legacy Spine interfaces requiring ongoing support alongside FHIR migration
- Resource competition with other NHS digital programmes

**Related Stakeholders**: SRO, Product Manager, CDDO

---

### SD-5: GP Practice Managers — Reduced Administrative Burden

**Stakeholder**: GP Practice Managers

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Reduce the administrative burden of appointment management on GP practice staff, decrease telephone call volumes for booking and cancellation, and integrate seamlessly with existing GP clinical systems without requiring practice-level infrastructure changes.

**Context & Background**:
GP practices handle an estimated 340 million appointments per year. A significant proportion of practice staff time is spent managing appointment bookings by telephone — answering the "8am rush" for same-day appointments. Practice managers need digital solutions that reduce this burden without creating new administrative overhead from a separate national platform that does not integrate with their clinical system.

**Driver Intensity**: HIGH

**Enablers**:

- GP Connect FHIR APIs already available for major GP clinical systems (EMIS, TPP SystmOne)
- NHS App integration with GP services establishing patient digital channel
- Strong GP practice demand for reduced telephone volume

**Blockers**:

- Fear that online booking increases total demand rather than shifting channel
- GP clinical system supplier co-operation required for deep integration
- Training and change management burden on already-stretched practice teams

**Related Stakeholders**: Royal College of GPs, BMA, Patients and Carers

---

### SD-6: HM Treasury — Value for Money and Cost Containment

**Stakeholder**: HM Treasury

**Driver Category**: FINANCIAL / COMPLIANCE

**Driver Statement**: Ensure the appointment booking platform delivers demonstrable value for money, reduces NHS operational costs associated with DNAs and appointment management, and operates within approved spending review allocations without creating ongoing unfunded cost pressures.

**Context & Background**:
NHS DNAs cost the NHS an estimated GBP 1.2 billion per year. HM Treasury has approved digital transformation funding within the NHS spending review settlement, but expects clear evidence of return on investment and ongoing cost reduction. Previous NHS IT programmes have had significant cost overruns, and Treasury is cautious about large-scale health IT investments.

**Driver Intensity**: HIGH

**Enablers**:

- Clear financial case based on DNA reduction (GBP 1.2bn annual cost)
- NHS operational efficiency savings from reduced telephone booking
- Evidence from other countries' national booking systems showing positive ROI

**Blockers**:

- History of NHS IT cost overruns reducing Treasury confidence
- Difficulty quantifying benefits until system is operational
- Integration costs potentially higher than initial estimates

**Related Stakeholders**: NAO, DHSC Finance Director, CDDO

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Patient Waiting Times Through Optimised Booking

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: SRO, Appointment Booking Programme

**Goal Statement**: Reduce average time from GP referral to first outpatient appointment by 15% across participating NHS Trusts within 18 months of platform launch.

**Why This Matters**: Waiting times are the primary political driver (SD-1), the primary patient concern (SD-3), and a key metric for demonstrating the value of NHS digital strategy (SD-4).

**Success Metrics**:

- **Primary Metric**: Average referral-to-appointment time (days) across participating Trusts
- **Secondary Metrics**:
  - Percentage of patients offered a choice of appointment within 2 weeks
  - Patient-reported experience of waiting time (NHS Patient Survey)

**Baseline**: Average 56 days referral-to-first-outpatient across all specialties (NHS England RTT data)

**Target**: Average 48 days (15% reduction) within 18 months

**Measurement Method**: NHS England Referral to Treatment (RTT) statistical publications, filtered for participating Trusts

**Dependencies**:

- NHS Trust PAS integration providing real-time slot availability
- e-RS integration for referral pathway data
- Sufficient Trust adoption (minimum 50% of acute Trusts)

**Risks to Achievement**:

- Trust PAS integration delays reducing the pool of available bookable slots
- Clinician resistance to patient-initiated booking for certain specialties
- Demand exceeds supply — platform makes unmet demand visible rather than reducing waits

---

### Goal G-2: Reduce Did Not Attend (DNA) Rate

**Derived From Drivers**: SD-1, SD-3, SD-6

**Goal Owner**: Service Owner

**Goal Statement**: Reduce the national NHS DNA rate from 6.4% to below 5.0% within 12 months of platform launch through intelligent reminders, easy rebooking, and patient-controlled cancellation.

**Why This Matters**: DNAs waste GBP 1.2 billion of NHS resources annually (SD-6), frustrate patients waiting for appointments (SD-3), and are a visible metric of NHS efficiency for Ministers (SD-1).

**Success Metrics**:

- **Primary Metric**: DNA rate (%) across participating Trusts and GP practices
- **Secondary Metrics**:
  - Patient cancellation rate (increased cancellations indicate patients managing their own bookings)
  - Rebooking rate (patients rebooking rather than simply not attending)

**Baseline**: 6.4% DNA rate nationally (NHS England Hospital Activity Statistics)

**Target**: Below 5.0% DNA rate for services using the platform

**Measurement Method**: Hospital Episode Statistics (HES) and GP Appointments data

**Dependencies**:

- Patient notification infrastructure (NHS Notify integration)
- Patient ability to cancel and rebook through the platform
- Trust willingness to release cancelled slots for rebooking in real time

**Risks to Achievement**:

- Patients still not engaging with digital reminders (digital exclusion)
- Trust PAS not supporting real-time slot release for rebooking
- Reminder fatigue reducing effectiveness over time

---

### Goal G-3: Achieve 50% NHS Trust Adoption Within 18 Months

**Derived From Drivers**: SD-2, SD-4, SD-5

**Goal Owner**: SRO

**Goal Statement**: Onboard at least 110 of the 220 NHS acute Trusts and 3,250 of 6,500 GP practices to the platform within 18 months of live launch.

**Why This Matters**: The platform delivers value only at scale. Trust adoption depends on addressing operational autonomy concerns (SD-2), demonstrating standards-based integration (SD-4), and reducing administrative burden (SD-5).

**Success Metrics**:

- **Primary Metric**: Number of NHS Trusts and GP practices actively using the platform
- **Secondary Metrics**:
  - Percentage of appointment types available on the platform per Trust
  - Trust satisfaction score with integration and support

**Baseline**: 0 (new platform)

**Target**: 110 Trusts, 3,250 GP practices within 18 months

**Measurement Method**: Platform analytics, Trust onboarding tracker

**Dependencies**:

- FHIR integration adapters available for major PAS vendors (Cerner, Epic, System C, Meditech)
- GP Connect integration operational for EMIS and TPP SystmOne
- NHS England mandate or strong incentive for Trust adoption

**Risks to Achievement**:

- Trust resistance driven by NPfIT legacy concerns
- PAS vendor delays in developing FHIR integration capabilities
- Insufficient onboarding support resources for simultaneous Trust deployments

---

### Goal G-4: Deliver Measurable Operational Efficiency Savings

**Derived From Drivers**: SD-5, SD-6

**Goal Owner**: DHSC Finance Director

**Goal Statement**: Deliver GBP 150 million annual operational savings across the NHS through reduced DNA costs, decreased telephone booking volumes, and optimised appointment utilisation within 3 years of full deployment.

**Why This Matters**: Financial sustainability is essential for Treasury support (SD-6) and GP practice staff wellbeing (SD-5).

**Success Metrics**:

- **Primary Metric**: Total annual operational savings (GBP) attributed to the platform
- **Secondary Metrics**:
  - Telephone booking volume reduction per GP practice
  - Appointment utilisation rate improvement

**Baseline**: GBP 1.2 billion annual DNA cost; estimated 60% of GP appointment bookings made by telephone

**Target**: GBP 150 million annual savings (12.5% of DNA costs plus administrative efficiency)

**Measurement Method**: NHS costing data, GP practice telephony data, before-and-after comparison

**Dependencies**:

- Sufficient adoption (Goal G-3 must be achieved)
- DNA rate reduction (Goal G-2 must be achieved)
- Trust operational changes to release savings (not just efficiency but actual cost reduction)

**Risks to Achievement**:

- Savings may be absorbed by demand growth rather than released as cash savings
- Attribution difficulty — multiple factors affect DNA rates and operational costs
- GP practices redirect saved time to clinical care (valuable but not cashable)

---

## Goal-to-Outcome Mapping

### Outcome O-1: Improved Patient Access to NHS Services

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Patients across England can find, book, change, and cancel NHS appointments through a single digital service, with average waiting times reduced by 15% and DNA rates below 5%.

**Measurement Details**:

- **KPI**: Patient access composite score (waiting time + booking satisfaction + DNA rate)
- **Current Value**: 56-day average wait, 6.4% DNA rate, fragmented booking
- **Target Value**: 48-day average wait, <5% DNA rate, unified booking
- **Measurement Frequency**: Monthly
- **Data Source**: NHS England RTT data, HES, NHS Patient Survey
- **Report Owner**: Service Owner

**Business Value**:

- **Financial Impact**: GBP 150M annual savings from DNA reduction and operational efficiency
- **Strategic Impact**: Flagship demonstration of NHS digital transformation delivering for patients
- **Operational Impact**: Reduced administrative burden on NHS staff
- **Patient Impact**: Better access, less waiting, more control over appointments

**Timeline**:

- **Phase 1 (Months 1-6)**: 30 pilot Trusts live, initial DNA reduction measurable
- **Phase 2 (Months 7-12)**: 80 Trusts live, 15% DNA reduction in pilot sites
- **Phase 3 (Months 13-18)**: 110+ Trusts live, waiting time reduction measurable
- **Sustainment (Year 2+)**: Full national coverage, sustained improvement

**Stakeholder Benefits**:

- **Secretary of State**: Visible evidence of NHS improvement for parliamentary reporting
- **Patients**: Single place to manage all NHS appointments
- **GP Practices**: Reduced telephone volume, less administrative burden
- **NHS Trusts**: Higher appointment utilisation, reduced DNA waste

---

## Complete Traceability Matrix

### Stakeholder -> Driver -> Goal -> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Reduce waiting times visibly | G-1 | 15% wait time reduction | O-1 | Improved patient access |
| Secretary of State | SD-1 | Reduce waiting times visibly | G-2 | DNA rate below 5% | O-1 | Improved patient access |
| NHS Trust CEs | SD-2 | Operational autonomy | G-3 | 50% Trust adoption | O-1 | Improved patient access |
| Patients/Carers | SD-3 | Simple appointment management | G-1 | 15% wait time reduction | O-1 | Improved patient access |
| Patients/Carers | SD-3 | Simple appointment management | G-2 | DNA rate below 5% | O-1 | Improved patient access |
| NHS England CDO | SD-4 | NHS digital strategy alignment | G-3 | 50% Trust adoption | O-1 | Improved patient access |
| GP Practice Managers | SD-5 | Reduced admin burden | G-4 | GBP 150M savings | O-1 | Improved patient access |
| HM Treasury | SD-6 | Value for money | G-4 | GBP 150M savings | O-1 | Improved patient access |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: NHS Trust CEs (SD-2) want operational autonomy and local flexibility, but the Secretary of State (SD-1) and NHS England CDO (SD-4) need national standardisation for waiting time reduction and digital strategy alignment.
  - **Resolution Strategy**: Design the platform as a **standards-based integration layer** rather than a replacement system. Trusts retain their PAS/EPR and clinical workflows; the national platform provides a patient-facing booking experience that integrates via FHIR APIs. Trusts can opt in incrementally, starting with specific appointment types. NHS England provides funding for Trust-side integration work.

- **Conflict 2**: GP Practice Managers (SD-5) want reduced administrative burden, but fear online booking will increase total demand rather than shift channel, creating more work not less.
  - **Resolution Strategy**: Implement appointment booking with **demand management features** — online booking is constrained to the same appointment pool as telephone booking, not additional capacity. Provide practices with analytics showing channel shift (telephone to digital) and overall demand management data. Pilot with willing practices to build evidence base.

- **Conflict 3**: HM Treasury (SD-6) demands demonstrable cost savings, but NHS Trusts may absorb efficiency gains into clinical activity rather than releasing cashable savings.
  - **Resolution Strategy**: Define benefits in terms of both **cashable savings** (reduced DNA costs, reduced temporary staffing) and **non-cashable benefits** (more patients seen, better utilisation). Present Treasury with a blended business case that demonstrates value for money even if not all savings are cashable. Use NHS Improvement's activity costing methodology.

**Synergies**:

- **Synergy 1**: Secretary of State (SD-1) and Patients (SD-3) share the goal of reduced waiting times — a single investment delivers both political and citizen outcomes
- **Synergy 2**: GP Practice Managers (SD-5) and HM Treasury (SD-6) both benefit from reduced telephone booking volume — administrative efficiency delivers both staff wellbeing and financial savings

---

## Communication & Engagement Plan

### Secretary of State

**Primary Message**: The NHS Appointment Booking Platform will deliver visible, measurable reductions in waiting times and DNAs within 12 months, demonstrating the government's commitment to NHS digital transformation.

**Key Talking Points**:

- Platform will be visible to patients through the NHS App — 30+ million registered users
- DNA reduction target of 20%+ saves GBP 150M+ annually
- Patient choice and control over appointments — a manifesto commitment delivered

**Communication Frequency**: Monthly briefings, quarterly programme review

**Preferred Channel**: Ministerial briefing papers, PQ lines prepared proactively

### NHS Trust Chief Executives

**Primary Message**: The platform integrates with your existing systems via open standards — it complements your PAS rather than replacing it, and NHS England is funding Trust-side integration.

**Key Talking Points**:

- FHIR-based integration — works with Cerner, Epic, System C, and other major PAS vendors
- Trusts retain control of appointment scheduling rules and clinical pathway logic
- Incremental adoption — start with specific appointment types and expand

**Communication Frequency**: Monthly Trust CIO forum, quarterly CEO briefing

**Preferred Channel**: NHS England regional team engagement, digital peer network events

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Patients | Multiple booking systems, telephone-dependent | Single digital booking service via NHS App | HIGH | LOW | User research, phased rollout, assisted digital support |
| GP Practice Staff | 60% telephone booking, manual cancellation handling | Digital-first booking with phone as secondary channel | HIGH | MEDIUM | Evidence from pilots, training, preserved telephone option |
| NHS Trust Booking Teams | Trust-specific PAS booking, limited patient self-service | Integrated national booking with Trust PAS | MEDIUM | HIGH | FHIR integration support, funded implementation, pilot-first approach |
| Clinicians | Limited visibility of patient booking behaviour | Dashboard showing DNA risk, appointment utilisation | LOW | LOW | Clinical advisory group input, opt-in analytics |

### Change Readiness

**Champions** (Enthusiastic supporters):

- NHS England Digital team — sees platform as flagship for FHIR strategy
- Patient advocacy groups (Healthwatch) — strong demand from patient feedback
- Early adopter NHS Trusts with existing FHIR capability

**Fence-sitters** (Neutral, need convincing):

- GP Practice Managers — supportive in principle but need evidence of reduced workload not increased
- Mid-tier NHS Trusts — willing but need funded integration support

**Resisters** (Opposed or skeptical):

- NHS Trusts with recent PAS investments — concerned about disruption to existing booking workflows
- Some clinical specialties — worried about patient self-booking for complex care pathways
- GP clinical system vendors — concerned about commoditisation of booking functionality

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DHSC Finance Director | DHSC Permanent Secretary | HM Treasury, CDDO | All stakeholders |
| Requirements prioritisation | Product Manager | Service Owner | Patients, Trusts, GPs, Clinicians | All stakeholders |
| Architecture decisions | Lead Architect | NHS England CDO | Security, Clinical Safety, Trust CIOs | All stakeholders |
| Clinical safety decisions | Clinical Safety Officer | Chief Nursing Officer | Clinicians, CQC | All stakeholders |
| Trust onboarding decisions | Onboarding Lead | SRO | Trust CIOs, GP Practice Managers | NHS Providers |
| Go/No-go for go-live | SRO | DHSC Permanent Secretary | All | All |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, Trust engagement issues)
3. **Level 3**: SRO / DHSC Permanent Secretary (strategic direction, major conflicts, Ministerial escalation)

---

## Risk Register (Stakeholder-Related)

### Risk R-1: NHS Trust Adoption Below Target

**Related Stakeholders**: NHS Trust CEs, SRO, Secretary of State

**Risk Description**: NHS Trusts resist adoption due to concerns about operational disruption, integration costs, or perceived lack of local flexibility, resulting in adoption below the 50% target.

**Impact on Goals**: G-1 (waiting time reduction requires scale), G-3 (adoption target), G-4 (savings require adoption)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Early Trust engagement, funded integration support, pilot programme with willing Trusts to build evidence, incremental adoption model

**Contingency Plan**: Focus on GP Connect integration for primary care bookings if secondary care adoption is slow, delivering value through GP appointment booking while Trust adoption builds

---

### Risk R-2: Patient Digital Exclusion

**Related Stakeholders**: Patients/Carers, Healthwatch, Secretary of State

**Risk Description**: Significant patient populations cannot access the digital booking service due to low digital skills, lack of internet access, or accessibility barriers, creating a two-tier appointment booking experience.

**Impact on Goals**: G-1 (inequitable access), G-2 (DNA reduction limited to digitally active patients)

**Probability**: HIGH

**Impact**: MEDIUM

**Mitigation Strategy**: Maintain telephone booking as primary alternative, fund assisted digital support in libraries and community centres, design for lowest common denominator device and connectivity, WCAG 2.2 AA compliance, Easy Read content

**Contingency Plan**: Partner with voluntary sector organisations to provide in-person booking support for digitally excluded patients

---

### Risk R-3: PAS Vendor Integration Delays

**Related Stakeholders**: NHS Trust CEs, NHS England CDO, GP Practice Managers

**Risk Description**: Major PAS/EPR vendors (Cerner, Epic, System C) do not deliver FHIR appointment booking APIs to the required standard and timeline, blocking Trust integration.

**Impact on Goals**: G-3 (adoption depends on integration), G-1 (waiting time reduction requires Trust data)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Early vendor engagement programme, NHS England leveraging procurement framework requirements for FHIR compliance, develop intermediate integration adapters for legacy systems

**Contingency Plan**: Deploy lightweight web portal for Trusts without FHIR-capable PAS, with manual data entry as interim measure

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| Service Owner | PENDING | | PENDING |
| NHS England CDO | PENDING | | PENDING |
| Clinical Safety Officer | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| Service Owner | | | |
| Enterprise Architect | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| NHS Long Term Plan | Strategy | NHS England | Digital-first appointment booking | N/A — external reference |
| NHS e-Referral Service | System | NHS Digital | Current referral booking system | N/A — external reference |
| GP Connect FHIR Specification | Standard | NHS Digital | GP appointment booking API | N/A — external reference |
| NHS Patient Survey 2025 | Report | NHS England | Patient booking preferences | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: NHS Appointment Booking Platform
**Model**: Claude Opus 4.6
