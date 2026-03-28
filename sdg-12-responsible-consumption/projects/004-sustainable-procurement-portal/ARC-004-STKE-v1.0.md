# Stakeholder Drivers & Goals Analysis: Sustainable Procurement Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Sustainable Procurement Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Sustainable Procurement Portal Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Crown Commercial Service, DESNZ, DEFRA, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Sustainable Procurement Portal, their underlying drivers, and how these drivers manifest into goals and measurable outcomes.

### Key Findings

The Sustainable Procurement Portal sits at the nexus of procurement policy, environmental accountability, and commercial reality. Crown Commercial Service must balance the government's sustainability ambitions (PPN 06/20 social value, PPN 06/21 carbon reduction, Net Zero Strategy) with procurement's fundamental obligations: value for money, fair competition, and timely contract award. The dominant tension is between environmental ambition (weighting carbon scores heavily in evaluation) and legal risk (suppliers challenging award decisions based on subjective or inconsistent environmental scoring). Contracting authorities want clear guidance and automated tools; they do not want the complexity of interpreting environmental data alongside price and quality. Suppliers want transparency — they need to understand how sustainability scores affect their competitiveness so they can invest in genuine decarbonisation rather than gaming metrics.

### Critical Success Factors

- Integrate carbon scores from the Carbon Footprint Calculator (Project 001) into procurement evaluation frameworks seamlessly
- Provide contracting authorities with clear, defensible sustainability scoring methodologies that withstand legal challenge
- Deliver a sustainability dashboard that works within existing procurement workflows (not a separate system)
- Enable transparency so suppliers understand how sustainability performance affects their competitiveness
- Support PPN 06/20 (social value) and PPN 06/21 (carbon reduction) compliance in a unified interface

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the principle of sustainable procurement. Significant tensions between the depth of sustainability assessment (environmental ambition) and the speed and simplicity of procurement processes (commercial efficiency). Procurement officers want a simple score; sustainability teams want nuanced assessment. Legal teams worry about challenge risk; policy teams want bold carbon weighting.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| CCS Chief Executive | Executive leadership | HIGH | HIGH | Manage Closely |
| SRO, Sustainable Procurement Portal | Programme Sponsor (CCS) | HIGH | HIGH | Manage Closely |
| CCS Commercial Director | Procurement operations | HIGH | HIGH | Manage Closely |
| CCS Policy and Standards Team | PPN compliance | HIGH | HIGH | Manage Closely |
| CCS Digital Team | Technology delivery | HIGH | HIGH | Manage Closely |
| Service Owner | Service accountability | HIGH | HIGH | Manage Closely |
| CCS Legal Team | Legal compliance | HIGH | MEDIUM | Keep Satisfied |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Minister for the Cabinet Office | Minister | Procurement policy sponsor | HIGH | HIGH |
| Contracting Authorities (200+) | Central government departments, NDPBs, agencies | Users of procurement frameworks | MEDIUM | HIGH |
| DESNZ | Partner department | Carbon Footprint Calculator (Project 001) | HIGH | HIGH |
| DEFRA | Partner department | Waste and circular economy data | MEDIUM | HIGH |
| Government suppliers | Private sector | Scored entities | LOW | HIGH |
| CDDO | Cabinet Office | Assurance & digital standards | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Procurement policy, funding | HIGH | MEDIUM |
| Government Legal Department (GLD) | Legal advisory | Procurement challenge risk | HIGH | MEDIUM |
| Social Enterprise UK | Charity | Social value advocacy | LOW | HIGH |
| SME Crown Representative | Cabinet Office | SME procurement access | MEDIUM | HIGH |
| National Audit Office | Parliament | Value for money audit | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * CCS Chief Exec   |
        |  * NAO              |  * SRO              |
        |  * CDDO             |  * Commercial Dir   |
        |  * GLD              |  * Policy & Standards|
 P      |  * CCS Legal        |  * DESNZ (Project 001)|
 O      |                     |  * Minister (CO)    |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Contracting      |
        |                     |    Authorities      |
        |                     |  * Government       |
        |                     |    Suppliers        |
        |                     |  * DEFRA            |
        |                     |  * Social Enterprise|
        |                     |    UK               |
        |                     |  * SME Crown Rep    |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: CCS Policy and Standards Team — Effective PPN Implementation

**Stakeholder**: CCS Policy and Standards Team

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Deliver digital tools that enable contracting authorities to implement PPN 06/20 (Taking Account of Social Value) and PPN 06/21 (Taking Account of Carbon Reduction Plans) consistently and effectively — moving beyond tick-box compliance to genuine sustainability impact in procurement decisions.

**Context & Background**:
CCS published PPN 06/20 (mandatory 10% social value weighting) and PPN 06/21 (mandatory Carbon Reduction Plans for contracts above GBP 5M). Three years on, implementation is inconsistent: some contracting authorities apply rigorous carbon scoring while others treat it as a pass/fail checkbox. The policy team needs digital tools that make consistent implementation the path of least resistance — standardised evaluation templates, automated scoring, and benchmarking so authorities know what "good" looks like. Without tools, policy is just words.

**Driver Intensity**: CRITICAL

**Enablers**:

- Standardised sustainability evaluation templates embedded in procurement workflows
- Automated carbon scoring from Project 001 integrated into evaluation frameworks
- Benchmarking showing how each authority's sustainability scoring compares to peers
- Training materials and guidance embedded in the tool, not separate documents

**Blockers**:

- Contracting authorities treating the portal as additional bureaucracy rather than enablement
- Carbon scores from Project 001 delayed or unreliable
- Legal uncertainty about the defensibility of sustainability scoring under procurement regulations
- Inconsistent adoption across contracting authorities

---

### SD-2: Contracting Authorities — Simple, Defensible Sustainability Assessment

**Stakeholder**: 200+ contracting authorities (central government departments, NDPBs, agencies)

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Access simple, standardised sustainability assessment tools that can be applied alongside price and quality evaluation without requiring specialist environmental expertise and without increasing the risk of procurement challenges.

**Context & Background**:
Procurement officers evaluate suppliers on price, quality, and social value. Adding carbon assessment creates anxiety: officers fear making inaccurate assessments that lead to legal challenges from unsuccessful bidders. Most procurement teams have no environmental expertise. They need a tool that provides a clear, defensible sustainability score they can apply with the same confidence as a price score. They do not want to become environmental assessors — they want a number they can trust.

**Driver Intensity**: HIGH

**Enablers**:

- A single sustainability score integrating carbon (from Project 001), social value, and circular economy metrics
- Pre-approved evaluation methodology that has been legally reviewed
- Automated scoring that reduces human judgement and subjectivity
- Training and worked examples showing how to apply scores

**Blockers**:

- Sustainability assessment requiring specialist knowledge procurement officers do not have
- Multiple separate scores (carbon score, social value score, circular economy score) that officers must combine manually
- Legal team advising against strong sustainability weighting due to challenge risk
- Inconsistent guidance from CCS on how to apply scores

---

### SD-3: Government Suppliers — Transparency and Fair Competition

**Stakeholder**: Government suppliers (large corporates and SMEs)

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Understand how sustainability performance affects competitiveness in government procurement, receive transparent feedback on sustainability scores, and have confidence that sustainability assessment is applied consistently across contracting authorities — not arbitrarily disadvantaging specific suppliers or sectors.

**Context & Background**:
Suppliers invest in sustainability when they believe it improves their competitive position. If sustainability scoring is opaque, inconsistent, or perceived as arbitrary, suppliers will not invest in genuine decarbonisation — they will invest in presentation. Large corporates with sustainability departments can present polished Carbon Reduction Plans; SMEs with genuine but undocumented environmental improvements may score poorly. Suppliers need transparency: what is being measured, how is it scored, and how does their score compare to competitors in their sector.

**Driver Intensity**: HIGH

**Enablers**:

- Published scoring methodology with worked examples
- Supplier sustainability dashboard showing their score, sector benchmark position, and improvement trajectory
- Feedback loop: suppliers see how their sustainability investment translates to improved competitiveness
- Sector-relative scoring that does not unfairly compare manufacturers to consultancies

**Blockers**:

- Opaque scoring methodology that suppliers cannot understand or challenge
- Inconsistent application across contracting authorities
- Scoring that penalises sectors with inherently higher emissions (manufacturing vs services)
- No feedback mechanism — suppliers invest in sustainability but cannot see the competitive benefit

---

### SD-4: CCS Legal Team — Procurement Challenge Risk Mitigation

**Stakeholder**: CCS Legal Team, Government Legal Department

**Driver Category**: RISK / COMPLIANCE

**Driver Statement**: Ensure sustainability scoring methodologies are legally defensible under the Procurement Act 2023, Public Contracts Regulations 2015 (during transition), and relevant case law — minimising the risk of successful procurement challenges based on environmental scoring.

**Context & Background**:
The Procurement Act 2023 (replacing PCR 2015) provides enhanced flexibility for sustainability in procurement but also introduces new transparency and challenge mechanisms. Unsuccessful suppliers can challenge award decisions if they believe sustainability scores were applied inconsistently, were based on inappropriate criteria, or were disproportionate to the subject matter of the contract. The legal team needs confidence that the portal's scoring methodology has been reviewed for legal compliance and that the audit trail is sufficient to defend against challenges.

**Driver Intensity**: CRITICAL

**Enablers**:

- Scoring methodology reviewed by Government Legal Department before deployment
- Complete audit trail of how each sustainability score was calculated and applied
- Consistency: same methodology applied identically across all contracting authorities
- Proportionality: sustainability weighting proportionate to contract subject matter

**Blockers**:

- Novel scoring methodology with no case law precedent
- Subjective elements in scoring that are difficult to defend under judicial review
- Inconsistent application across authorities creating precedent for challenge
- Insufficient documentation of scoring rationale

---

### SD-5: SME Crown Representative — Fair Access for Small Businesses

**Stakeholder**: SME Crown Representative (Cabinet Office)

**Driver Category**: STRATEGIC

**Driver Statement**: Ensure sustainability scoring does not create a de facto barrier to SME participation in government procurement — large corporates with sustainability departments should not gain unfair advantage from reporting capacity rather than genuine environmental performance.

**Context & Background**:
The government targets 33% of procurement spend with SMEs. The SME Crown Representative monitors whether procurement policies inadvertently exclude small businesses. Sustainability scoring risks disadvantaging SMEs who may have excellent environmental practices but lack the capacity to document them in the format large corporates use. The Carbon Footprint Calculator (Project 001) addresses the calculation barrier; the Procurement Portal must ensure the scoring methodology does not penalise SMEs for lower data quality when their actual environmental performance may be superior.

**Driver Intensity**: HIGH

**Enablers**:

- Sector-relative and size-adjusted scoring
- Data quality acknowledged in scoring (measured data scores higher but estimated data not penalised)
- Improvement trajectory weighted alongside absolute performance
- SME-specific guidance and support within the portal

**Blockers**:

- Absolute emissions scoring (large companies automatically score better due to offsetting capacity)
- Data quality penalties that disadvantage SMEs without monitoring systems
- Complex scoring methodology requiring specialist sustainability staff to navigate

---

## Driver-to-Goal Mapping

### Goal G-1: Unified Sustainability Score Integrated into 80% of Central Government Procurements Within 24 Months

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: CCS Commercial Director

**Goal Statement**: Deliver a unified sustainability score (combining carbon, social value, and circular economy metrics) integrated into procurement evaluation for at least 80% of central government procurements above GBP 5M within 24 months of portal launch.

**Success Metrics**:

- **Primary Metric**: Percentage of procurements using the portal's sustainability score
- **Target**: 80% of procurements above GBP 5M threshold
- **Secondary Metrics**: Average sustainability weighting applied (target: minimum 10%, aligned with PPN 06/20)

---

### Goal G-2: Zero Successful Procurement Challenges Based on Sustainability Scoring Within 24 Months

**Derived From Drivers**: SD-4

**Goal Owner**: CCS Legal Team

**Goal Statement**: Achieve zero successful legal challenges to procurement decisions based on the portal's sustainability scoring methodology within the first 24 months of operation.

**Success Metrics**:

- **Primary Metric**: Number of successful challenges citing sustainability scoring
- **Target**: Zero
- **Secondary Metric**: Number of challenges filed (target: fewer than 5, indicating methodology is perceived as fair)

---

### Goal G-3: Supplier Sustainability Transparency Dashboard Live Within 12 Months

**Derived From Drivers**: SD-3, SD-5

**Goal Owner**: Service Owner

**Goal Statement**: Deliver a supplier-facing sustainability dashboard showing their scores, sector benchmarks, improvement trajectory, and guidance on improving competitiveness, accessible to all registered government suppliers within 12 months of portal launch.

**Success Metrics**:

- **Primary Metric**: Number of suppliers accessing their sustainability dashboard
- **Target**: 10,000 suppliers within 12 months
- **Secondary Metric**: Supplier satisfaction with scoring transparency (target: 7/10)

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| CCS Policy | SD-1 | Effective PPN implementation | G-1 | 80% procurement adoption |
| Contracting Authorities | SD-2 | Simple, defensible assessment | G-1 | 80% procurement adoption |
| Government Suppliers | SD-3 | Transparency and fair competition | G-3 | Supplier dashboard |
| CCS Legal | SD-4 | Challenge risk mitigation | G-2 | Zero successful challenges |
| SME Crown Rep | SD-5 | Fair SME access | G-3 | Supplier dashboard |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: CCS Policy (SD-1) wants strong sustainability weighting (15-20%) to drive genuine decarbonisation impact, but CCS Legal (SD-4) wants conservative weighting (10%) to minimise legal challenge risk.
  - **Resolution Strategy**: Start at 10% (minimum PPN 06/20 requirement) with published guidance on how authorities can increase weighting to 15-20% for contracts where sustainability is particularly relevant to the subject matter. Build case law precedent at 10% before pushing higher weightings.

- **Conflict 2**: Contracting Authorities (SD-2) want a single simple score, but Environmental NGOs and sustainability advocates want nuanced multi-factor assessment showing carbon, social value, and circular economy as separate dimensions.
  - **Resolution Strategy**: Provide a single composite sustainability score for evaluation with drill-down capability showing component scores. Simple for procurement officers, detailed for sustainability teams and transparency reporting.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PPN 06/20 | Procurement Note | GOV.UK | Social Value in procurement (10% weighting) | N/A |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plans for suppliers | N/A |
| Procurement Act 2023 | Legislation | legislation.gov.uk | New procurement framework | N/A |
| Net Zero Strategy | Policy | GOV.UK | Procurement decarbonisation commitments | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Sustainable Procurement Portal (Project 004)
**Model**: Claude Opus 4.6
