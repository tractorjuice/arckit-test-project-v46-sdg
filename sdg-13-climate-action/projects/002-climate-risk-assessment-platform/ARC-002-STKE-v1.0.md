# Stakeholder Drivers & Goals Analysis: Climate Risk Assessment Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Climate Risk Assessment Platform (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Climate Risk Assessment Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Climate Risk Programme Board, DEFRA Digital, Environment Agency, Met Office, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Climate Risk Assessment Platform, which will enable systematic assessment of climate risks to UK infrastructure, communities, and natural assets. The platform will integrate UKCP18 climate projections with geospatial infrastructure data to produce risk scores that inform adaptation planning and investment decisions.

### Key Findings

Strong alignment exists between DEFRA's statutory duty under the Adaptation Reporting Power (Climate Change Act 2008, Section 62) and the infrastructure operators' need for consistent risk assessment methodologies. The primary tension is between the Environment Agency's desire for detailed, locality-specific risk assessments and National Highways/Network Rail's preference for portfolio-level risk aggregation. A secondary conflict exists between Met Office caution about communicating projection uncertainty and DEFRA's need for clear, actionable risk categories.

### Critical Success Factors

- Achieve Met Office endorsement of the platform's use of UKCP18 projections — misuse of climate science data would damage credibility
- Provide risk assessments that are actionable for infrastructure operators under the Adaptation Reporting Power
- Integrate with existing flood risk, coastal erosion, and heat risk datasets maintained by the Environment Agency
- Deliver consistent risk methodology that enables cross-sector comparison while respecting sector-specific vulnerability factors
- Pass GDS service assessment and meet accessibility standards for local authority users

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Consensus on the need for better climate risk assessment tools, but tensions between scientific precision (Met Office), operational practicality (infrastructure operators), statutory compliance (DEFRA), and local specificity (Environment Agency, local authorities). The multi-sector nature of infrastructure climate risk creates coordination challenges across transport, energy, water, telecoms, and health.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Environment, Food and Rural Affairs | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, CCRA alignment |
| DEFRA Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Climate Risk Platform | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA Climate Adaptation Team | Policy owners (Adaptation Reporting Power) | HIGH | HIGH | Manage Closely — Requirements, methodology |
| DEFRA Chief Scientific Adviser | Scientific methodology governance | HIGH | MEDIUM | Keep Satisfied — Methodology review |
| DEFRA CDIO | Digital strategy and technology | HIGH | MEDIUM | Keep Satisfied — Architecture governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Met Office Hadley Centre | Partner agency | UKCP18 climate projection data provider | HIGH | HIGH |
| Environment Agency | Executive agency | Flood risk data, climate adaptation | HIGH | HIGH |
| CCC Adaptation Committee | Statutory body | Independent adaptation assessment (CCRA) | HIGH | HIGH |
| National Highways | Infrastructure operator | Road network climate risk | MEDIUM | HIGH |
| Network Rail | Infrastructure operator | Rail network climate risk | MEDIUM | HIGH |
| National Grid ESO | Infrastructure operator | Energy network climate risk | MEDIUM | HIGH |
| Water companies (Ofwat regulated) | Infrastructure operators | Water infrastructure climate risk | MEDIUM | HIGH |
| Local authorities (152 upper tier) | Service delivery | Local adaptation planning | LOW | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Insurance industry (ABI) | Private sector | Climate risk pricing | LOW | HIGH |
| Academic researchers | Universities | Climate science, risk modelling | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | Owns the end-to-end platform service | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews |
| Delivery Manager | Manages delivery cadence, risks | MEDIUM / HIGH | Keep Informed — Stand-ups |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Secretary of     |
        |  * CDDO             |    State (DEFRA)    |
        |  * DEFRA CDIO       |  * Permanent Sec.   |
        |  * Chief Scientific |  * SRO              |
        |    Adviser          |  * Adaptation Team  |
 P      |                     |  * Met Office       |
 O      |                     |  * Environment      |
 W      |                     |    Agency           |
 E      |                     |  * CCC Adaptation   |
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * National Highways|
        |                     |  * Network Rail     |
        |                     |  * National Grid    |
        |                     |  * Water companies  |
        |                     |  * Local authorities|
        |                     |  * Insurance (ABI)  |
        |                     |  * Academics        |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Adaptation Team — Statutory Compliance with Adaptation Reporting Power

**Stakeholder**: DEFRA Climate Adaptation Team

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Deliver a platform that enables DEFRA to exercise its Adaptation Reporting Power effectively — providing infrastructure operators with a consistent, evidence-based methodology for assessing and reporting climate risks, reducing the reporting burden while improving the quality and comparability of adaptation reports.

**Context & Background**:
The Climate Change Act 2008 (Section 62) gives the Secretary of State the power to direct infrastructure operators to report on their climate risks and adaptation actions. The third round of Adaptation Reporting Power reports (ARP3) revealed inconsistent methodologies, making cross-sector comparison difficult. DEFRA needs a platform that provides a consistent risk assessment framework while being flexible enough to accommodate sector-specific vulnerability factors.

**Driver Intensity**: CRITICAL

**Enablers**:

- Consistent risk assessment methodology that infrastructure operators can adopt
- Integration with UKCP18 projections endorsed by Met Office
- Sector-specific vulnerability templates co-created with operators
- Reduced reporting burden through pre-populated risk assessments

**Blockers**:

- Infrastructure operators reluctant to adopt a government-mandated methodology
- Met Office restrictions on UKCP18 data redistribution
- Insufficient granularity for locality-specific assessments
- Over-engineered platform that operators find difficult to use

**Related Stakeholders**: Met Office (data), Environment Agency (flood risk), CCC Adaptation Committee (scrutiny), infrastructure operators (users)

---

### SD-2: Met Office Hadley Centre — Responsible Use of Climate Projection Data

**Stakeholder**: Met Office Hadley Centre

**Driver Category**: STRATEGIC / RISK

**Driver Statement**: Ensure the platform uses UKCP18 climate projections responsibly and accurately, communicating uncertainty appropriately, not over-interpreting projections for specific locations, and maintaining Met Office's scientific reputation.

**Context & Background**:
UKCP18 provides probabilistic climate projections for the UK at various spatial and temporal resolutions. The projections include significant uncertainty, especially at local scales and for variables like extreme precipitation. The Met Office is concerned about platforms that present projections as precise predictions, strip out uncertainty bounds, or use spatial resolutions finer than the underlying model supports. Misuse of UKCP18 data in a government platform would undermine confidence in Met Office science.

**Driver Intensity**: HIGH

**Enablers**:

- Joint technical governance between Met Office and platform team on projection use
- Clear communication of uncertainty ranges on all projection-derived outputs
- Appropriate spatial aggregation (not presenting 12km grid data as precise local predictions)
- Met Office review of risk score methodology before launch

**Blockers**:

- User demand for precise local predictions that projections cannot support
- Oversimplification of uncertainty into single-number risk scores
- Platform using superseded or draft projection data
- No formal Met Office review process integrated into platform governance

**Related Stakeholders**: DEFRA Chief Scientific Adviser (scientific governance), CCC Adaptation Committee (methodology scrutiny), Academic researchers (peer review)

---

### SD-3: Environment Agency — Integration with Existing Flood and Coastal Risk Data

**Stakeholder**: Environment Agency

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Ensure the platform integrates with existing Environment Agency flood risk data, coastal erosion maps, and climate adaptation evidence rather than duplicating them, and that the platform adds value to EA's own climate risk assessment capabilities.

**Context & Background**:
The Environment Agency maintains the most comprehensive set of flood risk and coastal erosion datasets in England. These include Flood Map for Planning, Risk of Flooding from Rivers and Sea, and the National Flood Risk Assessment (NaFRA). The EA is also a Reporting Authority under the Adaptation Reporting Power and produces its own climate adaptation reports. The EA needs assurance that the new platform will integrate with, not replace, its existing data and tools.

**Driver Intensity**: HIGH

**Enablers**:

- API integration with EA flood risk data services (already available as open data)
- Co-creation of compound risk methodology (flood + heat + drought combinations)
- EA involvement in platform governance and methodology review
- Platform enhances EA's existing tools rather than competing with them

**Blockers**:

- Platform duplicating EA data with different quality standards
- Inconsistent flood risk categorisation between EA and platform outputs
- Platform consuming EA data without acknowledging limitations or update cycles

**Related Stakeholders**: DEFRA Adaptation Team (policy owner), Met Office (projection data), Local authorities (flood risk consumers)

---

### SD-4: Infrastructure Operators — Actionable, Proportionate Risk Assessments

**Stakeholder**: National Highways, Network Rail, National Grid ESO, water companies

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Receive actionable, proportionate climate risk assessments that can be integrated into existing asset management and investment planning processes without requiring specialist climate science expertise, while meeting Adaptation Reporting Power obligations efficiently.

**Context & Background**:
Infrastructure operators have mature asset management frameworks (ISO 55001), existing risk registers, and established investment planning cycles (5-year Asset Management Plans, regulatory price reviews). They need climate risk data in formats compatible with these processes — not standalone academic climate reports. The reporting burden of ARP3 was significant; operators want a platform that reduces this burden while improving output quality.

**Driver Intensity**: MEDIUM

**Enablers**:

- Risk outputs in standard risk register formats (likelihood x consequence matrices)
- Integration with asset management systems via APIs
- Pre-populated risk assessments based on asset location and type
- Clear translation of climate projections into engineering-relevant parameters (e.g., days above 35C, 1-in-100-year flood depth increase)

**Blockers**:

- Risk outputs requiring specialist climate science interpretation
- Incompatible risk frameworks that don't align with ISO 55001 or sector regulators
- One-size-fits-all methodology that ignores sector-specific vulnerability factors
- Platform mandating methodology changes that disrupt established risk processes

**Related Stakeholders**: DEFRA Adaptation Team (reporting requirements), Met Office (projection data), CCC Adaptation Committee (reporting quality assessment)

---

### SD-5: Local Authorities — Locally Relevant Adaptation Planning Evidence

**Stakeholder**: Local authorities (152 upper-tier authorities in England)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Access locally relevant climate risk evidence that supports local climate adaptation planning, infrastructure investment decisions, and local plan policies, without requiring specialist climate science or GIS expertise.

**Context & Background**:
Local authorities are responsible for local planning, emergency planning, and public health — all of which require climate risk evidence. However, most local authorities lack specialist climate science or GIS staff. The CCC has repeatedly identified local adaptation as a gap. Local authorities need a platform that provides ready-to-use, locally relevant risk assessments covering heat, flood, drought, and coastal erosion at a resolution useful for planning decisions.

**Driver Intensity**: MEDIUM

**Enablers**:

- Ward-level or LSOA-level risk summaries accessible without GIS skills
- Integration with local planning systems and emergency planning tools
- Clear, plain-language risk categories (not probabilistic distributions)
- Template adaptation plans based on risk profile

**Blockers**:

- Platform requiring GIS expertise or specialist software
- Risk assessments too coarse for local planning decisions
- No support for non-technical users
- Cost barriers for local authorities with limited digital budgets

**Related Stakeholders**: DEFRA Adaptation Team (policy framework), Environment Agency (flood risk data), CCC (local adaptation gap evidence)

---

## Driver-to-Goal Mapping

### Goal G-1: Deliver Met Office-Endorsed Risk Assessment Methodology

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: DEFRA Chief Scientific Adviser

**Goal Statement**: Achieve Met Office endorsement of the platform's climate risk methodology within 6 months, ensuring responsible use of UKCP18 projections with appropriate uncertainty communication.

**Success Metrics**:

- **Primary Metric**: Written Met Office endorsement of methodology
- **Secondary Metrics**:
  - Uncertainty bounds displayed on all projection-derived outputs
  - Spatial resolution appropriate to underlying model capability

**Baseline**: No standardised platform; inconsistent methodologies across ARP3 reports

**Target**: Met Office-endorsed, standardised risk assessment methodology

---

### Goal G-2: Integrate with Environment Agency Data Services

**Derived From Drivers**: SD-3, SD-1

**Goal Owner**: Technical Lead

**Goal Statement**: Establish API integration with Environment Agency flood risk, coastal erosion, and hydrology data services within 9 months, enabling compound risk assessments.

**Success Metrics**:

- **Primary Metric**: Live API integration with EA flood risk data services
- **Secondary Metrics**:
  - Compound risk methodology (flood + heat + drought) validated
  - EA data freshness within 48 hours of source updates

---

### Goal G-3: Reduce Adaptation Reporting Power Reporting Burden by 50%

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Reduce the time infrastructure operators spend producing ARP reports by 50% through pre-populated risk assessments and standardised reporting templates.

**Success Metrics**:

- **Primary Metric**: Operator-reported time reduction in ARP report production
- **Secondary Metrics**:
  - 80% of infrastructure operators using platform for ARP4
  - Cross-sector comparability rating improved (assessed by CCC)

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA Adaptation | SD-1 | Statutory compliance | G-1 | Met Office methodology | O-1 | Standardised risk assessment |
| DEFRA Adaptation | SD-1 | Statutory compliance | G-3 | Reduce reporting burden | O-1 | Standardised risk assessment |
| Met Office | SD-2 | Responsible projection use | G-1 | Met Office methodology | O-1 | Standardised risk assessment |
| Environment Agency | SD-3 | Data integration | G-2 | EA data integration | O-1 | Standardised risk assessment |
| Infrastructure Ops | SD-4 | Actionable risk | G-3 | Reduce reporting burden | O-1 | Standardised risk assessment |
| Local Authorities | SD-5 | Local evidence | G-2 | EA data integration | O-1 | Standardised risk assessment |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Met Office caution about projection uncertainty (SD-2) vs operators' need for clear, actionable risk categories (SD-4)
  - **Resolution Strategy**: Tiered outputs — detailed probabilistic data for specialists, simplified risk categories for operators with clear uncertainty statements

- **Conflict 2**: Environment Agency wants locality-specific flood risk detail (SD-3) vs infrastructure operators want portfolio-level aggregation (SD-4)
  - **Resolution Strategy**: Multi-scale — asset-level risk scores that aggregate to portfolio/sector views

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Risk methodology | Chief Scientific Adviser | SRO | Met Office, EA, CCC | Operators |
| Data source selection | Data Architect | Chief Scientific Adviser | Met Office, EA | Product Manager |
| Feature prioritisation | Product Manager | Service Owner | Operators, LAs | Delivery team |
| Budget approval | Finance Director | Permanent Secretary | HM Treasury | CDDO |
| Go/no-go for launch | SRO | Permanent Secretary | Met Office, EA, CCC | All stakeholders |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Climate Change Act 2008 (Section 62) | Legislation | legislation.gov.uk | Adaptation Reporting Power | N/A — external reference |
| UKCP18 Science Overview | Scientific report | Met Office | Climate projection methodology | N/A — external reference |
| UK Climate Change Risk Assessment 3 (CCRA3) | Statutory report | CCC | Priority climate risks | N/A — external reference |
| Third ARP Reports | Reports | DEFRA | Infrastructure operator climate risk reports | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Climate Risk Assessment Platform (Project 002)
**Model**: Claude Opus 4.6
