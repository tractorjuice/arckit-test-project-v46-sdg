# Stakeholder Drivers & Goals Analysis: Carbon Footprint Calculator

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Carbon Footprint Calculator (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Carbon Footprint Calculator Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DESNZ Digital, SDG 12 Programme Board, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Carbon Footprint Calculator, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The Carbon Footprint Calculator faces a fundamental tension between the government's need for accurate, comprehensive emissions data and the business community's concern about reporting burden. DESNZ requires robust Scope 1/2/3 emissions accounting to meet Net Zero Strategy commitments and UNFCCC reporting obligations, while SME suppliers fear that complex carbon calculation requirements will exclude them from government procurement. The strongest alignment exists around creating a standardised, easy-to-use calculation tool that reduces the current fragmented approach where every contracting authority interprets PPN 06/21 differently. Industry bodies (CBI, Make UK) support standardisation but want the tool to accept existing corporate reporting rather than requiring duplicate data entry.

### Critical Success Factors

- Deliver a GHG Protocol-compliant calculation engine that produces defensible Scope 1, 2, and 3 emissions figures accepted by all contracting authorities
- Achieve adoption by at least 5,000 suppliers within 12 months of launch, demonstrating that carbon reporting is accessible to SMEs
- Integrate BEIS/DESNZ GHG Conversion Factors with automated annual updates so calculations remain current without manual intervention
- Provide transparent, auditable calculation methodology that withstands scrutiny from environmental NGOs and academic reviewers
- Interoperate with the Sustainable Procurement Portal (Project 004) to enable seamless carbon scoring in procurement decisions

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for a standardised carbon calculation tool and the principle of GHG Protocol compliance. Significant tensions between the depth of Scope 3 data required (environmental ambition) and the practicality of collecting supply chain data from thousands of SME suppliers (business burden). DESNZ scientists want methodological rigour; procurement officers want a simple score; suppliers want minimal reporting effort. The devolved administrations add complexity through different procurement policy positions on carbon weighting.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Energy Security and Net Zero | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DESNZ Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Carbon Footprint Calculator | Programme Sponsor (DESNZ) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DESNZ CDIO | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance, digital strategy |
| DESNZ Chief Scientific Adviser | Methodology assurance | HIGH | HIGH | Manage Closely — GHG Protocol compliance, calculation validation |
| DESNZ Climate Science Team | Emissions factor management | MEDIUM | HIGH | Keep Informed — Factor updates, methodology reviews |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews, user outcomes |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap input |
| DESNZ SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DESNZ Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Crown Commercial Service | CCS | Procurement integration partner | HIGH | HIGH |
| GDS Service Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| Environment Agency | Regulator | Environmental reporting oversight | MEDIUM | HIGH |
| Climate Change Committee | Advisory body | Net Zero progress monitoring | MEDIUM | HIGH |
| UK Business Climate Hub | Cross-sector | SME carbon reporting platform | MEDIUM | HIGH |
| CBI (Confederation of British Industry) | Industry body | Business community voice | MEDIUM | HIGH |
| Make UK | Industry body | Manufacturing sector voice | LOW | HIGH |
| Federation of Small Businesses (FSB) | Industry body | SME advocacy | LOW | HIGH |
| Government suppliers (SMEs) | Private sector | Primary users of the tool | LOW | HIGH |
| Government suppliers (large corporates) | Private sector | Users with existing reporting | LOW | MEDIUM |
| Environmental NGOs (Green Alliance, WWF-UK) | Civil society | Methodology scrutiny | LOW | HIGH |
| Academic community | Universities | Methodology peer review | LOW | MEDIUM |
| Devolved Administrations | Scottish Government, Welsh Government | Devolved procurement policy | MEDIUM | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for Carbon Footprint Calculator outcomes and spend controls | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns the end-to-end service and user outcomes | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, and dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, and cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions, assessment gates |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation, quarterly review |
| Departmental Security Officer (DSO) | Day-to-day security coordination and policy | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — Information risk decisions, DPIA sign-off |
| Cyber Security Lead | Operational cyber security, GovAssure | MEDIUM / HIGH | Keep Informed — Security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Minister (DESNZ) |
        |  * DESNZ Perm Sec   |  * SRO              |
        |  * DESNZ SIRO       |  * CDIO (DESNZ)     |
        |  * DESNZ Finance    |  * Chief Scientific  |
 P      |  * CDDO             |    Adviser           |
 O      |  * SSRO / DSO       |  * Service Owner    |
 W      |                     |  * CCS (Procurement)|
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Academic         |  * SME Suppliers    |
        |    community        |  * CBI / Make UK    |
        |  * Large corporates |  * FSB              |
        |    (existing        |  * Product Manager  |
        |     reporting)      |  * Climate Science  |
        |                     |  * Environment Agency|
        |                     |  * Climate Change   |
        |                     |    Committee        |
        |                     |  * Environmental    |
        |                     |    NGOs             |
        |                     |  * Devolved Admins  |
        |                     |  * UK Business      |
        |                     |    Climate Hub      |
        |                     |  * GDS Assessment   |
        +---------------------+---------------------+
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Minister for Energy Security and Net Zero | HIGH | HIGH | Manage Closely | Ministerial briefings, PQ lines, Net Zero progress reporting |
| SRO | HIGH | HIGH | Manage Closely | Weekly programme board, decision escalation |
| DESNZ CDIO | HIGH | HIGH | Manage Closely | Architecture governance, digital strategy alignment |
| DESNZ Chief Scientific Adviser | HIGH | HIGH | Manage Closely | Methodology validation, GHG Protocol compliance sign-off |
| Service Owner | HIGH | HIGH | Manage Closely | Fortnightly service reviews, user outcome tracking |
| Crown Commercial Service | HIGH | HIGH | Manage Closely | Joint integration governance, procurement scoring alignment |
| HM Treasury | HIGH | MEDIUM | Keep Satisfied | Business case updates, spending review submissions |
| DESNZ Permanent Secretary | HIGH | MEDIUM | Keep Satisfied | Accounting officer assurance |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control submissions, service assessment gates |
| SME Suppliers | LOW | HIGH | Keep Informed | User research, beta testing, guidance materials |
| CBI / Make UK / FSB | LOW | HIGH | Keep Informed | Industry consultation, usability feedback |
| Environment Agency | MEDIUM | HIGH | Keep Informed | Environmental reporting standards alignment |
| Climate Change Committee | MEDIUM | HIGH | Keep Informed | Net Zero monitoring methodology |
| Environmental NGOs | LOW | HIGH | Keep Informed | Methodology transparency, open data publication |
| Devolved Administrations | MEDIUM | HIGH | Keep Informed | Procurement policy divergence working group |

---

## Stakeholder Drivers Analysis

### SD-1: Minister for Energy Security and Net Zero — Credible Carbon Data for Net Zero Accountability

**Stakeholder**: Minister for Energy Security and Net Zero

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver a credible, standardised carbon footprint calculation tool that demonstrates the government is using its procurement spend (over GBP 300 billion annually) to drive decarbonisation, providing defensible data for parliamentary reporting, COP commitments, and Climate Change Committee progress reviews.

**Context & Background**:
The UK's legally binding Net Zero target (Climate Change Act 2008, amended 2019) requires demonstrable progress across all sectors. Government procurement is a major lever — PPN 06/21 requires suppliers bidding for contracts above GBP 5 million to publish Carbon Reduction Plans, but without a standardised calculation tool, the quality and comparability of these plans varies enormously. The Climate Change Committee has repeatedly criticised the lack of consistent emissions data across government supply chains. The Minister needs a tool that produces data robust enough for international reporting (UNFCCC, SDG reporting) and parliamentary scrutiny (Environmental Audit Committee, Public Accounts Committee).

**Driver Intensity**: CRITICAL

**Enablers**:

- A GHG Protocol-compliant tool that produces internationally comparable emissions data
- Rapid adoption by a critical mass of suppliers (visible progress for parliamentary questions)
- Integration with DESNZ emissions reporting systems for national inventory alignment
- Positive endorsement from the Climate Change Committee

**Blockers**:

- Methodological disputes that undermine credibility (academic/NGO criticism)
- Low supplier adoption making the tool irrelevant
- Data quality too poor for international reporting
- Political opposition framing the tool as business burden

**Related Stakeholders**: Climate Change Committee (progress monitoring), Environmental NGOs (scrutiny), HM Treasury (value for money), CCS (procurement integration)

---

### SD-2: DESNZ Chief Scientific Adviser — Methodological Rigour and Scientific Credibility

**Stakeholder**: DESNZ Chief Scientific Adviser

**Driver Category**: TECHNICAL / COMPLIANCE

**Driver Statement**: Ensure the Carbon Footprint Calculator implements the GHG Protocol Corporate Standard with scientific rigour, producing emissions figures that are methodologically defensible, reproducible, and consistent with the UK's national greenhouse gas inventory methodology.

**Context & Background**:
The UK's national GHG inventory is compiled by Ricardo Energy & Environment under contract to DESNZ, using IPCC Tier methodologies. The Carbon Footprint Calculator must produce figures consistent with this inventory — if suppliers' reported footprints aggregate to figures inconsistent with national inventory estimates, credibility is undermined. The Chief Scientific Adviser needs assurance that the calculation engine correctly implements Scope 1 (direct combustion, process emissions, fugitive emissions), Scope 2 (purchased electricity, heat, steam — both location-based and market-based methods), and Scope 3 (15 upstream and downstream categories) with appropriate emissions factors, uncertainty quantification, and boundary definitions.

**Driver Intensity**: CRITICAL

**Enablers**:

- Direct involvement in calculation methodology design and validation
- Published methodology document open to peer review
- Validation dataset with known-good calculations for regression testing
- Annual update process aligned with BEIS/DESNZ conversion factor publication cycle

**Blockers**:

- Pressure to simplify methodology beyond what is scientifically defensible
- Political timelines overriding validation requirements
- Insufficient budget for independent methodology review
- Scope 3 estimation methods that are too crude to be meaningful

**Related Stakeholders**: Climate Science Team (factor management), Environment Agency (reporting), Academic community (peer review)

---

### SD-3: Crown Commercial Service — Actionable Carbon Scores for Procurement Decisions

**Stakeholder**: Crown Commercial Service (CCS)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Receive standardised, comparable carbon footprint scores from the Calculator that can be directly integrated into procurement evaluation frameworks, enabling contracting authorities to apply consistent carbon weighting across G-Cloud, DOS, and bespoke procurements without requiring specialist environmental expertise.

**Context & Background**:
CCS manages over GBP 30 billion of government procurement through frameworks and dynamic purchasing systems. PPN 06/21 requires Carbon Reduction Plans but provides limited guidance on how to score and compare them. Currently, each contracting authority interprets carbon data differently — some weight it at 5%, some at 15%, and some are unsure how to evaluate plans at all. CCS needs a normalised carbon score that procurement officers can apply as confidently as they apply price and quality scores. The Sustainable Procurement Portal (Project 004) is the consumer of these scores.

**Driver Intensity**: HIGH

**Enablers**:

- A simple, normalised carbon intensity score (e.g., tCO2e per GBP revenue) that enables comparison across sectors
- API integration between the Carbon Footprint Calculator and the Sustainable Procurement Portal
- Sector benchmarks enabling "better than average / worse than average" assessment
- Guidance materials that procurement officers can use without environmental specialist support

**Blockers**:

- Over-complex output that procurement officers cannot interpret
- Lack of sector benchmarks making cross-sector comparison meaningless
- Legal challenges from suppliers who feel carbon scoring disadvantages them
- Inconsistent adoption across contracting authorities

**Related Stakeholders**: Contracting authorities (users), SME suppliers (scored entities), DESNZ (methodology owner), Devolved Administrations (procurement policy)

---

### SD-4: SME Suppliers — Minimal Reporting Burden with Fair Assessment

**Stakeholder**: Government suppliers (SMEs) — approximately 60,000 SMEs on government frameworks

**Driver Category**: OPERATIONAL / FINANCIAL / RISK

**Driver Statement**: Complete carbon footprint reporting with minimal time, cost, and specialist knowledge, receiving a fair assessment that does not disadvantage smaller organisations lacking dedicated sustainability teams — and not being excluded from government procurement due to inability to produce complex emissions data.

**Context & Background**:
SMEs represent approximately 33% of government procurement spend. Most SMEs do not have environmental managers, sustainability consultants, or emissions monitoring systems. The current PPN 06/21 requirement forces many SMEs to hire external consultants (GBP 5,000-15,000 per Carbon Reduction Plan) or produce low-quality self-assessments. Many SMEs fear that carbon reporting requirements will become a de facto barrier to government work, concentrating contracts with large corporates who have established sustainability departments. The Federation of Small Businesses has raised this concern publicly.

**Driver Intensity**: CRITICAL

**Enablers**:

- A free, guided calculator with sector-specific templates and estimation tools
- Ability to use readily available data (energy bills, fuel receipts, travel records) without needing specialist measurement equipment
- Sector-relative scoring that assesses improvement trajectory, not just absolute emissions
- Clear guidance in plain language, avoiding environmental jargon
- Pre-populated data where possible (e.g., grid average emissions factors applied automatically)

**Blockers**:

- Complex, scientific interface requiring environmental expertise to navigate
- Requirement for data that SMEs do not routinely collect (Scope 3 supply chain data)
- Scoring that penalises small organisations for having smaller absolute footprints with less reduction potential
- Mandatory third-party verification requirements that add cost

**Related Stakeholders**: FSB (advocacy), CBI (industry), CCS (procurement), Minister (political risk if SMEs excluded)

---

### SD-5: Environmental NGOs — Transparency and Ambition

**Stakeholder**: Environmental NGOs (Green Alliance, WWF-UK, ClientEarth, Carbon Trust)

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure the Carbon Footprint Calculator implements genuinely robust Scope 1, 2, and 3 methodology, publishes its calculation methodology openly for scrutiny, and produces data that supports meaningful corporate accountability rather than enabling greenwashing through simplified metrics.

**Context & Background**:
Environmental NGOs are increasingly scrutinising corporate and government carbon claims. "Greenwashing" — making misleading environmental claims — has led to ASA rulings, legal challenges (ClientEarth), and reputational damage. NGOs will examine whether the Calculator's methodology is robust enough to produce meaningful data or whether it enables suppliers to present flattering carbon figures through selective boundary setting, inappropriate emissions factors, or omission of significant Scope 3 categories. NGOs also advocate for the tool's methodology and aggregated data to be published openly.

**Driver Intensity**: HIGH

**Enablers**:

- Open publication of calculation methodology for peer review
- Mandatory Scope 3 reporting (at least material categories) rather than Scope 1 and 2 only
- Transparent uncertainty quantification — acknowledging where estimates are used
- Published aggregated data enabling sector-level analysis
- Independent methodology review by credible academic institutions

**Blockers**:

- Simplified methodology that omits Scope 3 or allows suppliers to exclude material emissions categories
- Opaque calculation engine with no published methodology
- Aggregated data withheld from public scrutiny
- Political pressure to weaken methodology to reduce business burden

**Related Stakeholders**: Academic community (peer review), Climate Change Committee (scrutiny), Minister (political exposure), Chief Scientific Adviser (methodology integrity)

---

### SD-6: DESNZ Climate Science Team — Sustainable Factor Management

**Stakeholder**: DESNZ Climate Science Team (GHG Conversion Factors team)

**Driver Category**: OPERATIONAL

**Driver Statement**: Maintain a sustainable, scalable process for updating the Calculator's emissions factors annually in line with the BEIS/DESNZ GHG Conversion Factors publication, without creating additional manual workload for a team already stretched across national inventory and international reporting obligations.

**Context & Background**:
The DESNZ Climate Science Team publishes the UK Government GHG Conversion Factors annually (typically June/July). These factors cover over 1,000 emission sources across energy, transport, waste, materials, and more. Currently, the team publishes Excel spreadsheets that organisations manually consume. If the Carbon Footprint Calculator requires bespoke factor formats or manual upload processes, it creates additional work for a team of approximately 8 specialists who also maintain the national inventory for UNFCCC reporting. The team needs an automated, machine-readable factor ingestion process.

**Driver Intensity**: MEDIUM

**Enablers**:

- Machine-readable emissions factor format (API or structured data file) that can be consumed automatically
- Automated validation of factor updates against previous year (flag anomalies)
- Version-controlled factor sets enabling recalculation with historical factors
- Clear handoff process: Climate Science Team publishes factors, Calculator ingests them automatically

**Blockers**:

- Requirement for bespoke factor formatting or manual upload
- Calculation engine that requires code changes when factors are updated
- No version control — inability to reproduce historical calculations
- Unclear ownership of the factor update process

**Related Stakeholders**: Chief Scientific Adviser (methodology oversight), Service Owner (operational reliability), Supplier users (calculation accuracy)

---

## Driver-to-Goal Mapping

### Goal G-1: GHG Protocol-Compliant Calculation Engine Live by Q4 2026

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: DESNZ Chief Scientific Adviser

**Goal Statement**: Deliver a calculation engine implementing the GHG Protocol Corporate Standard for Scope 1, Scope 2 (location-based and market-based), and material Scope 3 categories, validated against 50 reference calculations, by Q4 2026.

**Why This Matters**: Without a scientifically validated calculation engine, the tool's outputs will not be credible for parliamentary reporting (SD-1), will fail scientific peer review (SD-2), and will be dismissed by NGOs as greenwashing infrastructure (SD-5).

**Success Metrics**:

- **Primary Metric**: 100% accuracy against GHG Protocol reference calculations (50 test cases)
- **Secondary Metrics**:
  - All 15 Scope 3 categories supported (at minimum as estimation where full data unavailable)
  - Uncertainty ranges produced for all Scope 3 estimates
  - Published methodology document available for peer review

**Baseline**: No standardised government carbon calculation tool exists

**Target**: Validated, live calculation engine accepted by DESNZ Chief Scientific Adviser

**Measurement Method**: Validation test suite run against GHG Protocol reference examples; independent methodology review by academic institution

---

### Goal G-2: 5,000 Suppliers Actively Using the Tool Within 12 Months of Launch

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Achieve 5,000 unique supplier registrations with completed carbon footprint calculations within 12 months of public launch.

**Why This Matters**: Political credibility (SD-1) requires demonstrable adoption. CCS needs a critical mass of scored suppliers for procurement integration to be meaningful (SD-3). Adoption proves the tool is accessible to SMEs (SD-4).

**Success Metrics**:

- **Primary Metric**: 5,000 completed calculations from unique suppliers
- **Secondary Metrics**:
  - At least 60% of completions from organisations with fewer than 250 employees (SME definition)
  - Average time to complete first calculation under 2 hours for Scope 1 and 2
  - User satisfaction score above 7/10

**Baseline**: Zero (new service)

**Target**: 5,000 completed calculations, 60% SME

**Measurement Method**: Service analytics (registration, completion, organisation size); quarterly user satisfaction survey

---

### Goal G-3: Automated Emissions Factor Updates Within 5 Working Days of DESNZ Publication

**Derived From Drivers**: SD-2, SD-6

**Goal Owner**: Product Manager

**Goal Statement**: Achieve automated ingestion of annual BEIS/DESNZ GHG Conversion Factor updates within 5 working days of publication, with zero manual data entry and automated regression testing of existing calculations.

**Why This Matters**: Stale emissions factors produce incorrect calculations (SD-2). Manual update processes are unsustainable for the Climate Science Team (SD-6).

**Success Metrics**:

- **Primary Metric**: Factor update completed within 5 working days of DESNZ publication
- **Secondary Metrics**:
  - Zero manual data entry in the update process
  - Automated regression tests pass against previous year's calculations
  - Version history maintained for all factor sets

**Baseline**: No automated process exists

**Target**: Automated ingestion with 5 working day turnaround

**Measurement Method**: Process log showing publication date, ingestion date, test results

---

### Goal G-4: Normalised Carbon Score API Integrated with Sustainable Procurement Portal by Q1 2027

**Derived From Drivers**: SD-3

**Goal Owner**: CCS Integration Lead

**Goal Statement**: Deliver a normalised carbon intensity score (tCO2e per GBP million revenue) via API, integrated with the Sustainable Procurement Portal (Project 004), with sector benchmarks enabling relative comparison, by Q1 2027.

**Why This Matters**: Without procurement integration, carbon calculations remain informational rather than decisional — procurement officers cannot act on data they cannot access within their evaluation workflow.

**Success Metrics**:

- **Primary Metric**: API delivering normalised carbon scores consumed by Procurement Portal
- **Secondary Metrics**:
  - Sector benchmarks published for at least 20 SIC code categories
  - API latency under 500ms for 95th percentile
  - Procurement officers able to apply carbon scoring without specialist support

**Baseline**: No integration exists; carbon data manually reviewed as PDF attachments

**Target**: Automated API integration with sector benchmarks

**Measurement Method**: API availability metrics; procurement officer usability testing; benchmark coverage review

---

## Goal-to-Outcome Mapping

### Outcome O-1: Government Supply Chain Emissions Visibility

**Supported Goals**: G-1, G-2, G-4

**Outcome Statement**: Achieve quantified carbon footprint visibility for suppliers representing at least 50% of central government procurement spend within 18 months of launch.

**Measurement Details**:

- **KPI**: Percentage of procurement spend covered by supplier carbon footprints
- **Current Value**: Less than 5% (only suppliers voluntarily publishing Carbon Reduction Plans under PPN 06/21)
- **Target Value**: 50% of central government procurement spend
- **Measurement Frequency**: Quarterly
- **Data Source**: CCS procurement data matched against Calculator registrations
- **Report Owner**: CCS Analytics Team

**Business Value**:

- **Strategic Impact**: UK Government can report supply chain emissions with quantified evidence at COP and UNFCCC
- **Operational Impact**: Procurement officers can make carbon-informed decisions for the first time at scale
- **Financial Impact**: Targeted carbon reduction support for high-impact suppliers yields greatest decarbonisation per pound invested
- **Policy Impact**: Evidence base for future strengthening of PPN 06/21 thresholds

**Timeline**:

- **Phase 1 (Months 1-6)**: 1,000 suppliers, 10% spend coverage
- **Phase 2 (Months 7-12)**: 5,000 suppliers, 30% spend coverage
- **Phase 3 (Months 13-18)**: 10,000 suppliers, 50% spend coverage

---

### Outcome O-2: Standardised Carbon Assessment Across Government

**Supported Goals**: G-1, G-3, G-4

**Outcome Statement**: Eliminate inconsistent carbon assessment methodologies across contracting authorities, achieving a single assessment standard used by at least 80% of central government contracting authorities within 24 months.

**Measurement Details**:

- **KPI**: Percentage of contracting authorities using standardised carbon scores from the Calculator
- **Current Value**: 0% (each authority interprets PPN 06/21 independently)
- **Target Value**: 80% of central government contracting authorities
- **Measurement Frequency**: Quarterly
- **Data Source**: CCS framework data, contracting authority survey
- **Report Owner**: CCS Policy Team

---

## Complete Traceability Matrix

### Stakeholder -> Driver -> Goal -> Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | Credible carbon data for Net Zero | G-1 | GHG Protocol engine | O-1 | Supply chain emissions visibility |
| Minister | SD-1 | Credible carbon data for Net Zero | G-2 | 5,000 suppliers | O-1 | Supply chain emissions visibility |
| Chief Scientific Adviser | SD-2 | Methodological rigour | G-1 | GHG Protocol engine | O-2 | Standardised assessment |
| Chief Scientific Adviser | SD-2 | Methodological rigour | G-3 | Automated factor updates | O-2 | Standardised assessment |
| CCS | SD-3 | Actionable carbon scores | G-4 | API integration | O-2 | Standardised assessment |
| SME Suppliers | SD-4 | Minimal burden, fair assessment | G-2 | 5,000 suppliers | O-1 | Supply chain visibility |
| Environmental NGOs | SD-5 | Transparency and ambition | G-1 | GHG Protocol engine | O-1 | Supply chain visibility |
| Climate Science Team | SD-6 | Sustainable factor management | G-3 | Automated factor updates | O-2 | Standardised assessment |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: DESNZ Chief Scientific Adviser (SD-2) wants comprehensive Scope 3 accounting across all 15 categories, but SME Suppliers (SD-4) cannot provide detailed supply chain data for most Scope 3 categories.
  - **Resolution Strategy**: Tiered approach — mandatory Scope 1 and 2 with full methodology, mandatory material Scope 3 categories (purchased goods, business travel, employee commuting) using estimation tools, optional detailed Scope 3 for organisations with data. Scoring adjusts for data completeness.

- **Conflict 2**: Environmental NGOs (SD-5) want maximum transparency including methodology publication and open data, but SME Suppliers (SD-4) are concerned about commercial sensitivity of their emissions data being published.
  - **Resolution Strategy**: Publish methodology and aggregated sector-level data openly. Individual supplier data shared only with contracting authorities during procurement, protected by commercial confidentiality provisions. Suppliers can opt in to public disclosure.

**Synergies**:

- **Synergy 1**: Minister's need for credible data (SD-1) aligns with Chief Scientific Adviser's demand for rigour (SD-2) — both are satisfied by GHG Protocol compliance
- **Synergy 2**: CCS need for standardisation (SD-3) aligns with SME desire for fairness (SD-4) — a single standard eliminates inconsistent interpretation

---

## Communication & Engagement Plan

### SME Suppliers

**Primary Message**: The Carbon Footprint Calculator makes carbon reporting simple, free, and fair — you can complete your assessment using data you already have (energy bills, fuel receipts, travel records), and you'll be assessed on your improvement journey, not penalised for your starting point.

**Key Talking Points**:

- Free to use — no consultant required
- Uses data you already collect (energy bills, mileage logs)
- Sector-relative scoring — compared to similar businesses, not global corporations
- Guidance in plain English, step-by-step

**Communication Frequency**: Monthly during beta, quarterly post-launch

**Preferred Channel**: GOV.UK guidance pages, trade body newsletters, webinars

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| SME Suppliers | No carbon reporting or ad hoc consultant-produced plans | Standardised self-service calculation | HIGH | MEDIUM | Free tool, guided workflow, plain language, helpdesk |
| Procurement Officers | Manual review of PDF Carbon Reduction Plans | Automated carbon score in evaluation framework | MEDIUM | LOW | Training, guidance, pilot with willing authorities |
| DESNZ Climate Science Team | Publish Excel spreadsheets manually consumed | Machine-readable factor API consumed automatically | LOW | LOW | Reduced workload, clear handoff process |
| Contracting Authorities | Independent PPN 06/21 interpretation | Standardised carbon scoring | MEDIUM | MEDIUM | CCS policy guidance, phased rollout, support |

---

## Risk Register (Stakeholder-Related)

### Risk R-1: SME Adoption Failure

**Related Stakeholders**: SME Suppliers, Minister, CCS

**Risk Description**: SMEs find the tool too complex, too time-consuming, or too intrusive, resulting in low adoption and the tool being perceived as another bureaucratic burden.

**Impact on Goals**: G-2 (adoption target), O-1 (spend coverage)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Extensive user research with SMEs during alpha/beta, sector-specific templates, estimation tools for Scope 3, plain language guidance, helpdesk support

**Contingency Plan**: Simplify to Scope 1 and 2 only for initial launch, add Scope 3 progressively

---

### Risk R-2: Methodological Challenge from NGOs or Academia

**Related Stakeholders**: Environmental NGOs, Academic community, Minister

**Risk Description**: The calculation methodology is criticised as insufficiently rigorous (enabling greenwashing) or as using inappropriate simplifications, undermining credibility.

**Impact on Goals**: G-1 (methodology validation), O-2 (standardised assessment)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Publish methodology openly, commission independent academic review, engage NGOs during design phase, implement transparent uncertainty quantification

**Contingency Plan**: Revise methodology based on peer review feedback before public launch

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DESNZ Finance Director | SRO | HM Treasury | CDDO |
| Calculation methodology | Chief Scientific Adviser | SRO | Environment Agency, NGOs | Academic community |
| Procurement integration | CCS Integration Lead | CCS Director | DESNZ CDIO | Contracting authorities |
| User experience design | Product Manager | Service Owner | SME Suppliers, FSB | CBI, Make UK |
| Go/No-go for go-live | SRO | DESNZ Permanent Secretary | Steering Committee | All stakeholders |
| Emissions factor updates | Climate Science Team | Chief Scientific Adviser | Service Owner | All users |

---

## Validation & Sign-off

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| SRO | | | |
| DESNZ CDIO | | | |
| Chief Scientific Adviser | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GHG Protocol Corporate Standard | Standard | ghgprotocol.org | Scope 1/2/3 methodology | N/A — external reference |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plan requirements | N/A — external reference |
| Net Zero Strategy | Policy | GOV.UK | National decarbonisation targets | N/A — external reference |
| BEIS/DESNZ GHG Conversion Factors | Data | GOV.UK | Annual emissions factors | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Carbon Footprint Calculator (Project 001)
**Model**: Claude Opus 4.6
