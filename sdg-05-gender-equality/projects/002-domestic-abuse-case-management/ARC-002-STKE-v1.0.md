# Stakeholder Drivers & Goals Analysis: Domestic Abuse Case Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Domestic Abuse Case Management (Project 002) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Domestic Abuse Digital Programme, Home Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Home Office VAWG Team, Domestic Abuse Commissioner, MARAC National Coordination |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Domestic Abuse Case Management system, their drivers, goals, and measurable outcomes. This system will provide multi-agency case management for domestic abuse support services, enabling coordinated risk assessment, safety planning, and information sharing across police, health, social services, housing, and specialist domestic abuse services.

### Key Findings

The most critical alignment exists around improving survivor safety through better information sharing — police, health, social services, and specialist DA services all recognise that fragmented case management endangers lives. The most significant tension lies between the imperative for multi-agency information sharing (to identify and manage risk) and the equally vital need to protect survivor data from abuser discovery or misuse. The Domestic Abuse Commissioner's push for a single integrated case view must be balanced against the practical reality that different agencies have different data governance regimes, different legal bases for processing, and different levels of data security maturity. Survivor advocacy organisations are strongly supportive but insist on trauma-informed design and survivor control over their own data.

### Critical Success Factors

- Zero data breaches that expose survivor location or identity to perpetrators — this is a life-safety requirement
- MARAC information sharing latency reduced from days to minutes for high-risk cases
- Survivor consent preferences respected throughout all information sharing
- System passes Domestic Abuse Commissioner's review for trauma-informed design
- Integration with police, health, and social services achievable within existing legal frameworks

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for better multi-agency coordination. Critical tension between information sharing for safety and data protection for survivor privacy. Additional complexity from the diverse governance regimes of participating agencies and the sensitivity of coercive control dynamics in system design.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Home Secretary | Ministerial sponsor (VAWG) | HIGH | HIGH | Manage Closely — Ministerial briefings |
| Home Office VAWG Director | Programme sponsor | HIGH | HIGH | Manage Closely — Programme board |
| SRO, DA Digital Programme | Programme accountability | HIGH | HIGH | Manage Closely — Weekly governance |
| Home Office SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |
| Home Office Safeguarding Lead | Policy guidance | HIGH | HIGH | Manage Closely — Safeguarding requirements |
| Home Office Digital | Technical delivery | MEDIUM | HIGH | Keep Informed — Architecture, sprint reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Domestic Abuse Commissioner | Independent | Oversight, advocacy | HIGH | HIGH |
| Police forces (NPCC DA lead) | Policing | MARAC chair, risk assessment | HIGH | HIGH |
| NHS England Safeguarding | NHS | Health data sharing | HIGH | HIGH |
| Local Authority Social Services | Local government | Children's and adult safeguarding | HIGH | HIGH |
| Women's Aid Federation | Charity | Specialist DA services | MEDIUM | HIGH |
| Refuge | Charity | Safe accommodation, National DA Helpline | MEDIUM | HIGH |
| SafeLives | Charity | MARAC coordination, DASH-RIC training | MEDIUM | HIGH |
| Ministry of Justice | Government | Family courts, perpetrator programmes | MEDIUM | MEDIUM |
| MHCLG (Housing) | Government | Housing duties under DA Act | MEDIUM | HIGH |
| Survivors (via advocacy) | Citizens | Service users | LOW | HIGH |
| Children's Commissioner | Independent | Children affected by DA | MEDIUM | HIGH |
| ICO | Regulator | Data protection oversight | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HO SIRO          |  * Home Secretary   |
        |  * ICO              |  * VAWG Director    |
        |                     |  * SRO              |
        |                     |  * DA Commissioner  |
 P      |                     |  * Police (NPCC)    |
 O      |                     |  * NHS Safeguarding |
 W      |                     |  * Local Auth SS    |
 E      |                     |  * HO Safeguarding  |
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Women's Aid      |
        |                     |  * Refuge           |
        |                     |  * SafeLives        |
        |                     |  * Survivors        |
        |                     |  * Children's Comm  |
        |                     |  * MoJ              |
        |                     |  * MHCLG Housing    |
        |                     |  * HO Digital       |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Domestic Abuse Commissioner — Joined-Up Multi-Agency Response

**Stakeholder**: Domestic Abuse Commissioner

**Driver Category**: STRATEGIC / ADVOCACY

**Driver Statement**: Ensure that domestic abuse survivors receive a coordinated, joined-up response from all agencies involved in their case, eliminating the dangerous gaps in information sharing that have contributed to serious case reviews and domestic homicide reviews.

**Context & Background**:
The Domestic Abuse Commissioner's reports have repeatedly highlighted that fragmented information sharing between agencies is a critical factor in domestic homicide. The Domestic Abuse Act 2021 placed the Commissioner on a statutory footing with a mandate to improve the multi-agency response. Multiple Domestic Homicide Reviews (DHRs) have identified that agencies held individual pieces of information which, if shared, would have revealed escalating risk. The Commissioner's annual report calls for a "single view of risk" across agencies.

**Driver Intensity**: CRITICAL

**Enablers**:

- Technology platform enabling real-time information sharing between agencies
- Clear legal framework for sharing under Crime and Disorder Act 1998 and DA Act 2021
- Standardised risk assessment (DASH-RIC) used consistently across agencies

**Blockers**:

- Different data governance regimes across police, health, social services, and charities
- Survivor concerns about loss of control over their data
- Technology maturity varies enormously across participating agencies
- Cost of integration across hundreds of local delivery partnerships

**Related Stakeholders**: Police, NHS, local authorities, Women's Aid, SafeLives

---

### SD-2: Police Forces (NPCC) — Timely Risk Assessment and Intelligence

**Stakeholder**: National Police Chiefs' Council Domestic Abuse Lead

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Enable frontline officers and specialist DA teams to access up-to-date multi-agency risk information at the point of response, supporting the DASH-RIC risk assessment with information from health, social services, and specialist DA services that may not be available to police.

**Context & Background**:
Police are typically the first agency to encounter domestic abuse incidents. The DASH-RIC (Domestic Abuse, Stalking and Honour Based Violence Risk Identification Checklist) is the standard risk assessment tool, but officers completing it often lack information held by other agencies — GP records showing repeated A&E attendance, social services records showing children's welfare concerns, or specialist DA service records showing a pattern of coercive control. MARAC meetings are supposed to share this information, but they happen weekly or fortnightly, not in real-time.

**Driver Intensity**: CRITICAL

**Enablers**:

- Real-time access to multi-agency risk flags during incident response
- Automated MARAC referral when DASH-RIC score indicates high risk
- Mobile-accessible interface for officers at the scene

**Blockers**:

- Police IT systems vary across 43 forces in England and Wales
- Legal basis for real-time sharing more complex than retrospective MARAC sharing
- Risk of over-reliance on technology vs professional judgement

---

### SD-3: Survivors (via Advocacy Organisations) — Safety, Control, and Trust

**Stakeholder**: Survivors of domestic abuse (represented by Women's Aid, Refuge, SafeLives)

**Driver Category**: PERSONAL / SAFETY

**Driver Statement**: Have confidence that seeking help will not put them at greater risk; that their information will be handled safely; that they will not have to repeatedly recount their trauma to different agencies; and that they retain control over what is shared and with whom.

**Context & Background**:
Survivors consistently report that engaging with services requires them to tell their story repeatedly to police, social workers, housing officers, GPs, and specialist DA services. Each retelling is re-traumatising. Many survivors fear that sharing information with one agency will result in uncontrolled disclosure — particularly to the perpetrator via family court proceedings or housing records. Technology-facilitated abuse is a growing concern: perpetrators monitor devices, intercept mail, and track online activity.

**Driver Intensity**: CRITICAL

**Enablers**:

- Single case record reducing the need to repeat information
- Granular consent management allowing survivors to control what is shared
- Quick-exit functionality and safe-browsing design for all interfaces
- Proxy access through specialist DA services for survivors who cannot safely access directly

**Blockers**:

- Trust deficit — many survivors have had negative experiences with statutory agencies
- Complexity of consent in coercive control situations (consent may not be freely given)
- Tension between survivor control and safeguarding duties (e.g., children at risk)

---

### SD-4: NHS England Safeguarding — Clinical Information Sharing

**Stakeholder**: NHS England Safeguarding Lead

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Enable proportionate sharing of relevant health information (A&E attendance patterns, GP safeguarding concerns, mental health service involvement) with MARAC and police DA teams, within the legal framework of the Data Protection Act 2018 and NHS information governance.

**Context & Background**:
Health services hold critical information for DA risk assessment — patterns of injury, frequent A&E attendance, mental health presentations linked to abuse, and children's developmental concerns. NHS information governance has historically been a barrier to sharing, with clinicians uncertain about their legal basis. The NHSE Safeguarding Adults Framework and the Information Sharing Agreement for MARACs provide a framework, but implementation is inconsistent.

**Driver Intensity**: HIGH

**Enablers**:

- Clear clinical information sharing protocols integrated into the system
- Automated flagging of relevant health information for MARAC
- Training and guidance for clinicians on legal basis for sharing

**Blockers**:

- NHS IG culture tends toward caution (reluctance to share)
- Integration with diverse NHS IT systems (multiple EPR vendors)
- Risk of breaching patient confidentiality if sharing is too broad

---

### SD-5: Local Authority Social Services — Safeguarding Children and Vulnerable Adults

**Stakeholder**: Local Authority Social Services Directors

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Ensure that children and vulnerable adults in households affected by domestic abuse are identified and safeguarded through coordinated multi-agency assessment, with social services records contributing to and receiving information from the DA case management system.

**Context & Background**:
The Children Act 1989 and Care Act 2014 place duties on local authorities to safeguard children and vulnerable adults. Domestic abuse is a factor in a significant proportion of child protection cases. Social workers need timely access to police callout history, DASH-RIC scores, and specialist DA service assessments. The "toxic trio" (domestic abuse, substance misuse, mental health) requires cross-agency visibility. Serious Case Reviews have repeatedly found that children were known to multiple agencies but no single agency had the full picture.

**Driver Intensity**: HIGH

---

### SD-6: Women's Aid — Trauma-Informed, Survivor-Led Service Design

**Stakeholder**: Women's Aid Federation of England

**Driver Category**: ADVOCACY / PROFESSIONAL

**Driver Statement**: Ensure that the case management system is designed with trauma-informed principles, that survivor voices are central to design decisions, and that the system does not replicate the power dynamics of abuse by removing survivor agency over their own data.

**Context & Background**:
Women's Aid runs the Live Chat service, the Survivors' Forum, and coordinates a network of local DA services. Their "Change That Lasts" model emphasises survivor-led approaches where professionals work alongside survivors rather than doing things to them. Women's Aid has raised concerns about previous multi-agency systems that prioritised agency convenience over survivor safety — particularly around notifications, browser history, and data portability.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Zero Data Breaches Exposing Survivor Safety Information

**Derived From Drivers**: SD-3, SD-6

**Goal Owner**: Home Office SIRO

**Goal Statement**: Achieve zero data breaches or uncontrolled disclosures that expose survivor location, identity, or engagement with DA services to perpetrators or unauthorised parties, measured through incident tracking and audit.

**Success Metrics**:

- **Primary Metric**: Number of data breaches exposing survivor safety data
- **Secondary Metrics**: Number of audit findings on access controls; survivor trust survey scores

**Baseline**: Not currently measured (no integrated system)

**Target**: Zero breaches; quarterly audit with zero critical findings

---

### Goal G-2: MARAC Information Sharing Within 15 Minutes for High-Risk Cases

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: SafeLives (MARAC coordination)

**Goal Statement**: Reduce multi-agency information sharing latency from days (current MARAC cycle) to 15 minutes for cases identified as high risk through DASH-RIC, enabling real-time risk management.

**Success Metrics**:

- **Primary Metric**: Time from DASH-RIC high-risk identification to multi-agency information visibility
- **Secondary Metrics**: Number of cases where real-time sharing identified previously unknown risk factors

**Baseline**: 7-14 days (current MARAC meeting cycle)

**Target**: 15 minutes for high-risk cases; 4 hours for medium-risk cases

---

### Goal G-3: Reduce Survivor Re-Traumatisation Through Single Case Record

**Derived From Drivers**: SD-3, SD-6

**Goal Owner**: Domestic Abuse Commissioner

**Goal Statement**: Reduce the number of times survivors are required to recount their experience to different agencies from an average of 5+ agencies to once, through a shared case record accessible to authorised agencies.

**Success Metrics**:

- **Primary Metric**: Number of agencies requiring survivors to repeat their core narrative
- **Secondary Metrics**: Survivor satisfaction with information handling

**Baseline**: Average 5+ repetitions (each agency collects independently)

**Target**: Core narrative recorded once, shared with consent to authorised agencies

---

### Goal G-4: Achieve Domestic Abuse Commissioner Approval for Trauma-Informed Design

**Derived From Drivers**: SD-3, SD-6

**Goal Owner**: Home Office VAWG Director

**Goal Statement**: Obtain formal endorsement from the Domestic Abuse Commissioner that the system meets trauma-informed design standards, with specialist DA services (Women's Aid, Refuge, SafeLives) validating the user experience.

**Success Metrics**:

- **Primary Metric**: Formal Commissioner endorsement obtained
- **Secondary Metrics**: Women's Aid and Refuge design review sign-off

**Baseline**: No existing system

**Target**: Commissioner endorsement before public beta

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DA Commissioner | SD-1 | Joined-up response | G-2 | 15-min sharing | O-1 | Safer multi-agency response |
| Police (NPCC) | SD-2 | Timely risk assessment | G-2 | 15-min sharing | O-1 | Safer multi-agency response |
| Survivors | SD-3 | Safety and control | G-1 | Zero breaches | O-2 | Survivor trust and safety |
| Survivors | SD-3 | Safety and control | G-3 | Single case record | O-2 | Survivor trust and safety |
| NHS | SD-4 | Clinical sharing | G-2 | 15-min sharing | O-1 | Safer multi-agency response |
| Social Services | SD-5 | Child safeguarding | G-2 | 15-min sharing | O-1 | Safer multi-agency response |
| Women's Aid | SD-6 | Trauma-informed design | G-4 | Commissioner approval | O-2 | Survivor trust and safety |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Police/NHS/Social Services want broad information sharing (SD-2, SD-4, SD-5) but Survivors (SD-3) need granular control over their data
  - **Resolution Strategy**: Tiered consent model — mandatory sharing for imminent risk to life (legal basis: vital interests), consent-based sharing for lower-risk situations. Survivor notified of all disclosures (except where notification would endanger).

- **Conflict 2**: DA Commissioner (SD-1) wants a "single view of risk" but ICO requires data minimisation and purpose limitation
  - **Resolution Strategy**: Implement "risk flags" model — agencies share risk-relevant flags rather than full case records. Full case detail available only with explicit legal basis and audited access.

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Survivor Data Breach Leading to Physical Harm

**Related Stakeholders**: Survivors, Women's Aid, DA Commissioner

**Risk Description**: A data breach, unauthorised access, or technical flaw exposes a survivor's location, identity, or engagement with DA services to a perpetrator, resulting in physical harm or death.

**Impact on Goals**: G-1 (zero breaches), G-4 (Commissioner endorsement)

**Probability**: LOW (with appropriate controls)

**Impact**: CRITICAL (life-safety)

**Mitigation Strategy**: Field-level encryption for location data; break-glass access logging with automatic alerts; penetration testing by specialist DA-aware security testers; survivor safety impact assessment for all features

**Contingency Plan**: Immediate ICO notification, police notification, survivor safety plan activation, system lockdown pending investigation

---

### Risk R-2: Agency Reluctance to Share Information

**Related Stakeholders**: NHS, local authorities, police

**Risk Description**: Individual agencies or local areas refuse to participate or share information due to data governance concerns, risk aversion, or lack of technical capability, creating inconsistent coverage.

**Probability**: HIGH

**Impact**: HIGH

**Mitigation Strategy**: Home Office Ministerial direction; clear legal basis documentation; information sharing agreement template; phased rollout with willing early adopters

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Domestic Abuse Act 2021 | Legislation | legislation.gov.uk | DA definition, Commissioner role, data provisions | N/A |
| MARAC Operating Protocol | Guidance | SafeLives | Multi-agency sharing framework | N/A |
| DASH-RIC | Tool | SafeLives | Standardised risk assessment | N/A |
| VAWG Strategy 2021 | Policy | Home Office | National strategy for tackling VAWG | N/A |
| Crime and Disorder Act 1998 s.115 | Legislation | legislation.gov.uk | Legal basis for information sharing | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Domestic Abuse Case Management (Project 002)
**Model**: Claude Opus 4.6
