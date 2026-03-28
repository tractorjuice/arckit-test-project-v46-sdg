# Stakeholder Drivers & Goals Analysis: Urban Planning Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Urban Planning Analytics (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Urban Planning Analytics Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Urban Planning Analytics Programme Board, DLUHC Planning Directorate, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Urban Planning Analytics platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes required for success. The platform will provide data-driven spatial planning and development control tools, enabling local planning authorities to make faster, more consistent, and better-evidenced planning decisions aligned with the National Planning Policy Framework (NPPF).

### Key Findings

The Urban Planning Analytics platform faces a central tension between the ambition to modernise a fundamentally paper-based, discretionary planning system and the deeply entrenched practices of 330+ local planning authorities with varying resources and digital capabilities. The strongest alignment exists around reducing planning application processing times — developers, citizens, and government all want faster decisions. The most significant conflict is between developers seeking predictability and speed versus community groups seeking meaningful participation and protection of local character. Heritage England's concerns about automated heritage impact assessment add a further dimension of complexity.

### Critical Success Factors

- Reduce average planning application determination time from 8 weeks to 5 weeks for minor applications by providing automated constraint checks and policy analysis
- Achieve structured data publication from 50 local planning authorities within 12 months, compliant with DLUHC planning data standards
- Integrate heritage constraint data from the National Heritage List for England (NHLE) to prevent planning decisions that damage listed buildings
- Maintain democratic legitimacy — the platform must support, not replace, community engagement in planning decisions
- Pass GDS service assessment at Beta demonstrating user-centred design with planning officers, applicants, and community members

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus that the planning system needs digital modernisation, but significant disagreements about pace of change, extent of automation, and the balance between speed and community participation. Local planning authorities are under severe resourcing pressure (40% reduction in planning staff since 2010), creating urgency but also change fatigue.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Housing and Planning | DLUHC Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, housing delivery narrative |
| DLUHC Chief Planner | Professional planning leadership | HIGH | HIGH | Manage Closely — Professional standards, policy alignment |
| SRO, Urban Planning Analytics | Programme Sponsor (DLUHC) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DLUHC Planning Data Team | DLUHC data standards for planning | HIGH | HIGH | Manage Closely — Data model co-design |
| DLUHC Digital Planning Programme | Existing planning reform programme | HIGH | HIGH | Manage Closely — Integration, avoiding duplication |
| DLUHC Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Local Planning Authorities | 330+ English LPAs | Platform users and data publishers | HIGH | HIGH |
| Historic England | ALB of DCMS | Heritage constraint consultee | HIGH | HIGH |
| Royal Town Planning Institute (RTPI) | Professional body | Professional standards | MEDIUM | HIGH |
| Home Builders Federation | Industry body | Planning applicant representative | MEDIUM | HIGH |
| CPRE (Campaign to Protect Rural England) | Charity | Environmental and heritage protection | LOW | HIGH |
| Community and Parish Councils | Local governance | Planning consultation participants | LOW | HIGH |
| Planning Inspectorate (PINS) | ALB of DLUHC | Appeals and examination | HIGH | MEDIUM |
| Ordnance Survey | Geospatial data partner | Spatial base data | MEDIUM | HIGH |
| CDDO | Cabinet Office | Spend control and assurance | HIGH | MEDIUM |
| Planning Software Vendors | Industry | Existing market participants | MEDIUM | HIGH |
| GDS Service Assessment | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| Neighbourhood Forum Groups | Community | Neighbourhood plan makers | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | Owns end-to-end planning analytics service | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control gates |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * DLUHC Finance    |  * Minister for     |
        |  * CDDO             |    Housing/Planning |
        |  * Planning         |  * DLUHC Chief      |
        |    Inspectorate     |    Planner          |
        |                     |  * SRO              |
 P      |                     |  * DLUHC Planning   |
 O      |                     |    Data Team        |
 W      |                     |  * Historic England |
 E      |                     |  * LPAs             |
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * RTPI             |
        |                     |  * Home Builders Fed|
        |                     |  * CPRE             |
        |                     |  * Community Councils|
        |                     |  * Ordnance Survey  |
        |                     |  * Planning Software|
        |                     |  * Neighbourhood    |
        |                     |    Forums           |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Minister for Housing and Planning — Accelerating Housing Delivery Through Planning Reform

**Stakeholder**: Minister for Housing and Planning (DLUHC)

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Accelerate planning decision-making to unblock housing delivery, demonstrating that digital tools can make the planning system faster, more predictable, and more consistent — supporting the government's target of 300,000 new homes per year.

**Context & Background**:
Housing delivery consistently falls short of the 300,000 annual target, with the planning system frequently cited as a bottleneck. Average determination times for major applications exceed 26 weeks. Planning reform is politically contentious — the 2020 White Paper was largely abandoned after political backlash. Digital modernisation offers a less controversial route to improvement than legislative reform.

**Driver Intensity**: CRITICAL

**Enablers**:
- Demonstrable time savings: even 1-week reduction in determination times is politically significant
- Platform positioned as helping planners, not replacing them

**Blockers**:
- Perception that automation reduces democratic scrutiny of planning decisions
- RTPI opposition to de-professionalisation of planning

---

### SD-2: Local Planning Authorities — Doing More with Less

**Stakeholder**: Local Planning Authorities (collectively)

**Driver Category**: OPERATIONAL / RESOURCE

**Driver Statement**: Enable planning officers to process applications more efficiently with better data and automated constraint checking, given severe resource constraints (40% staff reduction since 2010, 25% of planning officer posts vacant, increasing application volumes).

**Context & Background**:
Local planning authorities are in crisis — the RTPI's 2025 workforce survey showed 25% vacancy rates for planning officers, with many authorities relying on expensive agency planners. Applications are increasing due to permitted development reforms creating more complex prior approval cases. Planning officers spend significant time on manual tasks — checking constraints, cross-referencing policies, chasing consultee responses — that could be automated or data-assisted. However, planning is fundamentally a professional judgement exercise, and officers are wary of systems that constrain their discretion.

**Driver Intensity**: CRITICAL

**Enablers**:
- Automated constraint checking (heritage, flood, ecology) saving 2-3 hours per application
- Structured data reducing manual policy cross-referencing
- Integration with existing back-office planning systems (Idox, NEC/Civica)

**Blockers**:
- Poor data quality in existing planning systems requiring manual cleanup
- Resistance from experienced officers who see automation as de-skilling

---

### SD-3: Historic England — Protecting Heritage Through Better Data

**Stakeholder**: Historic England

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure that planning analytics integrates authoritative heritage data from the National Heritage List for England (NHLE) so that planning decisions properly assess impact on listed buildings, conservation areas, scheduled monuments, and registered parks and gardens, preventing unlawful harm to heritage assets.

**Context & Background**:
Heritage crime (unauthorised works to listed buildings) costs an estimated £2 billion annually. A significant proportion of heritage damage occurs through planning decisions made without adequate heritage impact assessment — planners unaware of nearby listed buildings, missing conservation area boundaries, or incomplete knowledge of heritage significance. Historic England wants the planning analytics platform to surface heritage constraints automatically, flag applications requiring Listed Building Consent, and trigger statutory consultation where required.

**Driver Intensity**: HIGH

**Enablers**:
- Direct NHLE API integration providing real-time heritage constraint data
- Automatic flagging of applications within conservation areas or affecting listed building settings

**Blockers**:
- Heritage impact assessment requires professional judgement beyond automated checks
- Incomplete NHLE data for some asset types (e.g., locally listed buildings held by individual authorities)

---

### SD-4: Community and Parish Councils — Meaningful Participation in Planning

**Stakeholder**: Community and Parish Councils, Neighbourhood Forum Groups

**Driver Category**: DEMOCRATIC / SOCIAL

**Driver Statement**: Ensure that digital planning tools enhance rather than diminish community participation in planning decisions, with accessible consultation interfaces, plain-language summaries of applications, and genuine consideration of community views in the analytics that inform decisions.

**Context & Background**:
Planning is one of the few areas where citizens have a direct statutory right to participate in decisions affecting their community. Community groups fear that a "data-driven" planning system will prioritise speed and developer interests over community input. The existing system — posting site notices and receiving handwritten letters — is low-tech but understood. Digital alternatives must be more accessible, not less. Parish councils often lack digital skills and broadband connectivity.

**Driver Intensity**: HIGH

**Enablers**:
- Accessible, plain-language consultation interfaces that work on mobile devices
- Clear visualisation of planning applications with 3D views and impact simulations

**Blockers**:
- Digital-only consultation excluding elderly or digitally excluded residents
- Analytics that reduce community objections to data points rather than democratic input

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Minor Application Determination Time from 8 Weeks to 5 Weeks

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: SRO, Urban Planning Analytics

**Goal Statement**: Reduce the average determination time for minor planning applications from 8 weeks to 5 weeks in participating local planning authorities within 18 months of platform adoption.

**Why This Matters**: Directly supports housing delivery targets (SD-1) and reduces workload pressure on planning officers (SD-2).

**Success Metrics**:
- **Primary Metric**: Average determination time (weeks) for minor applications in platform LPAs
- **Secondary Metrics**:
  - Percentage of applications determined within statutory time limits
  - Planning officer time per application (hours)

**Baseline**: 8.2 weeks average (DLUHC planning statistics Q4 2025)
**Target**: 5.0 weeks average
**Measurement Method**: DLUHC quarterly planning statistics for participating authorities

---

### Goal G-2: Achieve Zero Heritage Constraint Oversights in Platform-Assisted Decisions

**Derived From Drivers**: SD-3

**Goal Owner**: Historic England Liaison

**Goal Statement**: Achieve zero instances of planning decisions made through the platform where a statutory heritage constraint was not identified to the planning officer, verified through annual audit against NHLE records.

**Why This Matters**: Prevents unlawful damage to heritage assets and gives Historic England confidence in digital planning tools.

**Success Metrics**:
- **Primary Metric**: Number of heritage constraint oversights identified in annual audit
- **Secondary Metrics**:
  - Heritage consultation trigger rate (should increase with better constraint identification)
  - Listed Building Consent application identification rate

**Baseline**: Estimated 3-5% heritage constraint oversight rate in manual processes
**Target**: 0% oversight rate for NHLE-listed constraints
**Measurement Method**: Annual audit comparing platform constraint data against NHLE

---

### Goal G-3: Publish Structured Planning Data from 50 LPAs

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: DLUHC Planning Data Team

**Goal Statement**: 50 local planning authorities publishing structured planning application data in DLUHC data standard format via the platform within 12 months.

**Why This Matters**: Creates the national planning data infrastructure needed for analytics and policy monitoring.

**Success Metrics**:
- **Primary Metric**: Number of LPAs publishing compliant structured data
- **Secondary Metrics**:
  - Data completeness score per LPA
  - Timeliness of data publication (lag from decision to publication)

**Baseline**: 14 LPAs publishing partial structured data (current DLUHC pathfinder)
**Target**: 50 LPAs publishing compliant structured data
**Measurement Method**: DLUHC planning data dashboard

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Accelerate housing delivery | G-1 | Reduce determination time | O-1 | Faster, consistent planning |
| Minister | SD-1 | Accelerate housing delivery | G-3 | 50 LPAs structured data | O-1 | Faster, consistent planning |
| LPAs | SD-2 | Do more with less | G-1 | Reduce determination time | O-1 | Faster, consistent planning |
| Historic England | SD-3 | Heritage protection through data | G-2 | Zero heritage oversights | O-2 | Protected heritage assets |
| Community groups | SD-4 | Meaningful participation | G-1 | Faster decisions (if accessible) | O-1 | Faster, consistent planning |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Minister (SD-1) and developers want faster planning decisions, but Community Groups (SD-4) want more time for meaningful consultation and participation.
  - **Resolution Strategy**: Speed improvements come from automating back-office tasks (constraint checking, policy lookup), not from shortening consultation periods. Statutory consultation periods maintained; time savings achieved pre- and post-consultation.

- **Conflict 2**: Automated heritage constraint checking (SD-3) is valuable but Historic England is concerned that automation may create false confidence — planners ticking a "heritage clear" box without professional assessment of setting and significance.
  - **Resolution Strategy**: Platform flags heritage constraints and triggers professional assessment, but does not provide automated heritage impact conclusions. Clear UX labelling: "Constraints identified — professional heritage impact assessment required."

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Platform architecture | Solution Architect | SRO | DLUHC Chief Planner, Historic England | All stakeholders |
| Planning data standards | DLUHC Planning Data Team | DLUHC Chief Planner | LPAs, RTPI, OS | Planning software vendors |
| Heritage integration design | Historic England Liaison | SRO | Historic England, conservation officers | LPAs |
| Community engagement UX | UX Research Lead | Service Owner | Community groups, parish councils | All stakeholders |
| Budget approval | Finance Director | DLUHC Permanent Secretary | CDDO, HM Treasury | All stakeholders |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| National Planning Policy Framework (NPPF) | Policy | DLUHC | Planning decision framework | N/A — external reference |
| Levelling Up and Regeneration Act 2023 | Legislation | legislation.gov.uk | Planning data duties | N/A — external reference |
| DLUHC Planning Data Standards | Standard | DLUHC | Structured planning data model | N/A — external reference |
| NHLE Data Services | API | Historic England | Heritage constraint data | N/A — external reference |
| RTPI Workforce Survey 2025 | Report | RTPI | Planning officer capacity crisis | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Urban Planning Analytics (Project 002)
**Model**: Claude Opus 4.6
