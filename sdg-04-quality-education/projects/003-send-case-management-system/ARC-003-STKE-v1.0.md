# Stakeholder Drivers & Goals Analysis: SEND Case Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | SEND Case Management System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, SEND Case Management Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SEND Programme Board, DfE SEND Division, Local Authority SEND Leads |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the SEND Case Management System, their underlying drivers, and how these translate into goals and measurable outcomes. The system will digitise and standardise the Education, Health and Care (EHC) plan process across local authorities in England.

### Key Findings

The SEND system in England is in crisis. Over 576,000 children have EHC plans (up 60% since 2019), 43% of new EHC plans are issued late (outside the 20-week statutory timeframe), and SEND Tribunal appeals have doubled in five years. The most acute tension exists between parents — who experience a fragmented, adversarial system — and local authorities, who are overwhelmed by demand with inadequate digital tools. Both groups align on the need for a better system, but disagree on whether the solution is more funding, systemic reform, or digital enablement. The Children and Families Act 2014 obligations remain unchanged, making compliance increasingly difficult without technological intervention.

### Critical Success Factors

- Reduce the percentage of late EHC plans from 43% to below 15% within 18 months of deployment
- Achieve adoption by at least 80% of local authorities within 24 months
- Enable parents to track EHC plan progress in real time, reducing complaint volume by 40%
- Integrate with health and social care systems to support genuine multi-agency working
- Maintain compliance with the Children and Families Act 2014 statutory timelines

### Stakeholder Alignment Score

**Overall Alignment**: LOW-MEDIUM

All stakeholders agree the current system is failing children, but there is significant disagreement about whether a digital platform can address what many view as a fundamentally under-resourced system. Parents' groups fear digital tools will be used to automate refusals. Local authorities fear an unfunded mandate. Health services worry about data sharing obligations they cannot resource.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Children, Families and Wellbeing | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DfE Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, SEND Programme | Programme Sponsor (DfE) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DfE SEND Division Director | Policy lead | HIGH | HIGH | Manage Closely — Policy alignment |
| DfE CDO | Digital leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DfE SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, children's data |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Local Authority SEND Teams | 152 LAs | Primary users | HIGH | HIGH |
| Parents and Carers of Children with SEND | Citizens | Beneficiaries and advocates | LOW | HIGH |
| SEND Tribunal (SENDIST) | First-tier Tribunal | Dispute resolution | HIGH | HIGH |
| NHS Integrated Care Boards (ICBs) | NHS | Health assessment providers | HIGH | HIGH |
| Schools (SENCOs) | Schools | Referral originators and plan implementers | MEDIUM | HIGH |
| Parent Carer Forums / IPSEA / SOSSEN | Charities | Advocacy and legal support | MEDIUM | HIGH |
| Local Government Association (LGA) | LGA | LA collective voice | HIGH | MEDIUM |
| Educational Psychologists (EPs) | LAs/independent | Assessment providers | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |
| Ofsted/CQC | Joint inspectors | SEND area inspections | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * Minister         |
        |  * Ofsted/CQC       |  * Permanent Sec.   |
        |  * DfE SIRO         |  * SRO              |
        |  * LGA              |  * SEND Division Dir|
        |                     |  * CDO              |
 P      |                     |  * LA SEND Teams    |
 O      |                     |  * NHS ICBs         |
 W      |                     |  * SEND Tribunal    |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Parents/Carers   |
        |                     |  * SENCOs           |
        |                     |  * Parent Forums    |
        |                     |  * Ed. Psychologists|
        |                     |  * IPSEA/SOSSEN     |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Minister — Deliver SEND Reform and Reduce Tribunal Appeals

**Stakeholder**: Minister for Children, Families and Wellbeing

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver visible, systemic improvement to the SEND system that reduces parent dissatisfaction, decreases SEND Tribunal appeals, and demonstrates the government's commitment to inclusive education — without requiring primary legislation or unaffordable new funding.

**Context & Background**: SEND Tribunal appeals have doubled in 5 years, with parents winning 96% of cases — indicating systemic local authority failure rather than frivolous appeals. The SEND Review Green Paper (2022) identified digital transformation as a key enabler. The Minister needs demonstrable progress to respond to sustained advocacy from parent groups and the Disability Charities Consortium.

**Driver Intensity**: CRITICAL

**Enablers**:

- Cross-party consensus that the SEND system needs reform
- SEND Review commitments provide policy mandate
- DfE SEND Division has dedicated transformation budget

**Blockers**:

- Local authority funding constraints — digital tools seen as unfunded mandate
- NHS reluctance to commit to cross-system data sharing
- Scale: 152 local authorities with different legacy systems and processes

---

### SD-2: Local Authority SEND Teams — Manage Demand with Inadequate Resources

**Stakeholder**: Local Authority SEND Teams (152 LAs)

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Manage an overwhelming and growing volume of EHC plan requests, statutory assessments, and annual reviews within the 20-week statutory timeline, despite severe capacity constraints and inadequate digital tools.

**Context & Background**: EHC plan numbers have grown by 60% since 2019, while LA SEND team capacity has not kept pace. Many LAs use a combination of spreadsheets, document management systems, and paper files to manage the EHC process. The statutory 20-week timeline is routinely breached, exposing LAs to Tribunal costs (average GBP 15,000 per appeal), Ofsted/CQC Written Statements of Action, and reputational damage.

**Driver Intensity**: CRITICAL

---

### SD-3: Parents and Carers — Transparency, Timeliness, and Being Heard

**Stakeholder**: Parents and Carers of Children with SEND

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Navigate the EHC plan process without needing specialist legal knowledge, receive timely decisions, understand what is happening at every stage, and ensure their child's voice and needs are genuinely heard — not lost in bureaucratic processes.

**Context & Background**: Parents describe the EHC process as "adversarial," "Kafkaesque," and "traumatic." They report receiving no communication for weeks, not understanding where their case is in the process, receiving decisions without explanation, and being forced to appeal to Tribunal to obtain provision their child is legally entitled to. Parent Carer Forums consistently identify lack of transparency and timeliness as their top concerns.

**Driver Intensity**: CRITICAL

---

### SD-4: NHS Integrated Care Boards — Multi-Agency Statutory Obligations

**Stakeholder**: NHS Integrated Care Boards (ICBs)

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Fulfil statutory health assessment obligations within the EHC plan process without creating an unsustainable workload for overstretched NHS therapy services (speech and language, occupational therapy, CAMHS).

**Context & Background**: The Children and Families Act 2014 requires health services to contribute to EHC assessments within 6 weeks. ICBs struggle with this obligation due to therapy service waiting lists (often 12-18 months for CAMHS). A digital platform that streamlines the request-response process could reduce administrative overhead, but health data sharing across NHS-LA boundaries remains technically and governance-challenging.

**Driver Intensity**: HIGH

---

### SD-5: SEND Tribunal — Reduce Avoidable Appeals Through Better Process

**Stakeholder**: SEND Tribunal (SENDIST), First-tier Tribunal (Health, Education and Social Care Chamber)

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Reduce the volume of avoidable SEND Tribunal appeals by improving the quality of LA decision-making, the timeliness of EHC plan processes, and the transparency of communication with parents.

**Driver Intensity**: HIGH

---

### SD-6: SENCOs — Practical Tools for Coordination

**Stakeholder**: School Special Educational Needs Coordinators (SENCOs)

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Access practical digital tools that simplify SENCO administrative duties — referral submissions, annual review coordination, provision mapping, and communication with LA SEND teams — without adding to the already unsustainable SENCO workload.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Late EHC Plans from 43% to Below 15%

**Derived From Drivers**: SD-1, SD-2, SD-3
**Goal Owner**: DfE SEND Division Director
**Goal Statement**: Reduce the percentage of new EHC plans issued outside the 20-week statutory timeframe from 43% to below 15% across all local authorities within 18 months of platform deployment.

---

### Goal G-2: Enable Real-Time Case Tracking for Parents

**Derived From Drivers**: SD-3
**Goal Owner**: SRO, SEND Programme
**Goal Statement**: Provide parents and carers with a real-time online portal showing the current status of their child's EHC assessment or plan review, with automated milestone notifications, within 12 months of launch.

---

### Goal G-3: Achieve 80% Local Authority Adoption Within 24 Months

**Derived From Drivers**: SD-1, SD-2
**Goal Owner**: SRO
**Goal Statement**: Achieve platform adoption by at least 122 of 152 local authorities in England within 24 months, covering at least 80% of the EHC plan caseload.

---

### Goal G-4: Reduce SEND Tribunal Appeals by 30%

**Derived From Drivers**: SD-1, SD-5
**Goal Owner**: Minister
**Goal Statement**: Achieve a 30% reduction in SEND Tribunal appeal registrations within 2 years, through improved timeliness, transparency, and decision quality.

---

### Goal G-5: Integrate Health Assessment Workflow

**Derived From Drivers**: SD-4
**Goal Owner**: DfE CDO (jointly with NHS England)
**Goal Statement**: Deliver a digital health assessment request-and-response workflow between LA SEND teams and NHS ICBs, reducing the average health advice turnaround from 8 weeks to 4 weeks.

---

## Conflict Analysis

- **Conflict 1**: Parents (SD-3) want maximum transparency and data access, but local authorities (SD-2) worry that real-time tracking will increase complaint volumes during inevitable processing delays
  - **Resolution Strategy**: Phase — launch parent portal with status tracking but frame expectations clearly (statutory timeline explanation); provide LAs with bottleneck alerts to proactively manage cases approaching deadline

- **Conflict 2**: DfE (SD-1) wants mandatory platform adoption, but LGA and local authorities resist unfunded mandates
  - **Resolution Strategy**: Incentive — fund platform centrally; provide migration support; allow LAs to retain local flexibility within a standardised core process; demonstrate cost savings from reduced Tribunal exposure

- **Conflict 3**: NHS ICBs (SD-4) need health data sharing, but NHS information governance policies are more restrictive than LA policies for children's data
  - **Resolution Strategy**: Innovate — co-design data sharing with NHS England IG team; use DPIA to establish lawful basis under the Children and Families Act 2014 statutory duty; implement minimum viable data exchange (request/response, not full clinical record sharing)

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | CDO | SRO | CDDO, NHS England | LAs |
| Data sharing agreements | DfE SIRO | Permanent Secretary | ICO, NHS IG Lead | Parents |
| LA adoption strategy | SEND Division Dir. | SRO | LGA, LA SEND Leads | SENCOs |
| Health integration design | CDO | SRO | NHS ICBs, NHS England | Parents, EPs |
| Parent portal design | Service Owner | SRO | Parent Forums, IPSEA | SENCOs, LAs |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Children and Families Act 2014 | Legislation | legislation.gov.uk | EHC plan statutory framework | N/A — external reference |
| SEND Review Green Paper 2022 | Policy | DfE | SEND reform proposals | N/A — external reference |
| SEND Code of Practice | Statutory guidance | DfE | 0-25 SEND guidance | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SEND Case Management System
**Model**: Claude Opus 4.6
