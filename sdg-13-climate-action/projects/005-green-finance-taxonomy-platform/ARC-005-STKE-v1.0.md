# Stakeholder Drivers & Goals Analysis: Green Finance Taxonomy Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Green Finance Taxonomy Platform (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Green Finance Taxonomy Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Green Finance Programme Board, HMT Digital, FCA, Green Technical Advisory Group, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Green Finance Taxonomy Platform, a digital service that provides a definitive classification engine for determining whether economic activities qualify as "green" under the UK Green Taxonomy. The platform will enable financial institutions, corporates, and regulators to classify investments and activities against science-based criteria, supporting the UK's Green Finance Strategy and preventing greenwashing.

### Key Findings

The strongest alignment exists between HMT's ambition to position London as the global centre for green finance and the financial sector's demand for regulatory clarity on what constitutes a "green" investment. The FCA's parallel work on Sustainability Disclosure Requirements (SDR) and the anti-greenwashing rule creates a ready regulatory framework. The primary tension is between financial sector demands for a simple, binary (green/not green) classification and the scientific complexity of establishing credible thresholds that withstand academic scrutiny. A secondary tension exists between the desire for UK-specific taxonomy criteria and the need for international interoperability with the EU Taxonomy, ASEAN Taxonomy, and other emerging frameworks.

### Critical Success Factors

- Achieve Green Technical Advisory Group (GTAG) endorsement of classification criteria before launch — GTAG credibility underpins the taxonomy's scientific legitimacy
- Provide API-first classification service that financial institutions can integrate into existing investment workflows
- Ensure interoperability mapping with EU Taxonomy to avoid creating trade barriers for cross-border investment
- Deliver classification decisions within seconds to support real-time investment screening
- Prevent the platform from becoming a greenwashing tool through robust "do no significant harm" (DNSH) screening

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for a UK Green Taxonomy, but significant tensions on scope (transition activities inclusion), strictness of criteria (ambitious vs pragmatic), international alignment (EU equivalence vs UK-specific), and the pace of sector coverage. The financial sector wants rapid, comprehensive coverage; scientists want rigorous, evidence-based criteria that take time to develop.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Chancellor of the Exchequer | Minister | HIGH | MEDIUM | Keep Satisfied — Budget/Mansion House briefings |
| Economic Secretary to the Treasury | City Minister | HIGH | HIGH | Manage Closely — Green finance policy |
| HMT Permanent Secretary | Accounting Officer | HIGH | MEDIUM | Keep Satisfied — Programme board |
| SRO, Green Finance Taxonomy | Programme Sponsor (HMT) | HIGH | HIGH | Manage Closely — Weekly programme board |
| HMT Green Finance Team | Policy owners | HIGH | HIGH | Manage Closely — Requirements, criteria |
| HMT CDIO | Digital strategy | HIGH | MEDIUM | Keep Satisfied — Architecture governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Green Technical Advisory Group (GTAG) | Independent advisory | Scientific criteria governance | HIGH | HIGH |
| FCA | Financial regulator | SDR enforcement, anti-greenwashing rule | HIGH | HIGH |
| PRA | Prudential regulator | Climate risk in financial stability | HIGH | MEDIUM |
| Bank of England | Central bank | Climate stress testing, TCFD | HIGH | MEDIUM |
| The Investment Association | Industry body | Asset management industry | MEDIUM | HIGH |
| UK Finance | Industry body | Banking industry | MEDIUM | HIGH |
| Association of British Insurers (ABI) | Industry body | Insurance industry | MEDIUM | HIGH |
| London Stock Exchange Group (LSEG) | Market infrastructure | Green bond listings | MEDIUM | HIGH |
| Institutional investors (pension funds) | Financial sector | ESG/green investment mandates | LOW | HIGH |
| Corporate issuers (FTSE 350) | Industry | Green bond issuance, sustainability reporting | LOW | HIGH |
| CCC | Statutory body | Net zero pathway alignment | MEDIUM | MEDIUM |
| DESNZ | Partner department | Net zero policy, carbon budgets | MEDIUM | MEDIUM |
| European Commission (DG FISMA) | EU | EU Taxonomy equivalence | MEDIUM | MEDIUM |
| ISSB | International standards | Sustainability disclosure standards | MEDIUM | MEDIUM |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| Environmental NGOs | Civil society | Greenwashing scrutiny | LOW | HIGH |
| Academic researchers | Universities | Taxonomy science | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * Chancellor       |  * City Minister    |
        |  * HMT Perm Sec     |  * SRO              |
        |  * HMT CDIO         |  * Green Finance    |
        |  * PRA              |    Team             |
        |  * Bank of England  |  * GTAG             |
 P      |  * CDDO             |  * FCA              |
 O      |                     |                     |
 W      |                     |                     |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * EU Commission    |  * Investment Assoc |
        |  * ISSB             |  * UK Finance       |
        |                     |  * ABI              |
        |                     |  * LSEG             |
        |                     |  * Pension funds    |
        |                     |  * Corporate issuers|
        |                     |  * CCC              |
        |                     |  * NGOs             |
        |                     |  * Academics        |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: HMT Green Finance Team — Establish UK as Global Green Finance Centre

**Stakeholder**: HMT Green Finance Team

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Deliver a credible, usable UK Green Taxonomy that positions London as the global centre for green finance, supports the UK's Green Finance Strategy, and demonstrates post-Brexit regulatory competitiveness alongside EU Taxonomy equivalence.

**Context & Background**:
The UK's Green Finance Strategy (2019, updated 2023) commits to establishing a UK Green Taxonomy. The EU Taxonomy Regulation (2020) has set the global benchmark, and the UK risks falling behind if it does not deliver its own framework. London's position as a global financial centre creates both opportunity (attract green capital flows) and pressure (provide regulatory clarity that matches or exceeds EU standards). The Mansion House Compact and Transition Plan Taskforce add further momentum.

**Driver Intensity**: CRITICAL

**Enablers**:

- Rapid sector coverage — at least energy, transport, buildings, manufacturing at launch
- API-first platform enabling fintech integration
- Interoperability mapping with EU Taxonomy for cross-border investment
- GTAG-endorsed criteria providing scientific credibility
- Transition activities included (unlike EU Taxonomy's initial approach) to demonstrate pragmatism

**Blockers**:

- Slow GTAG criteria development delaying launch
- Financial sector not adopting the taxonomy due to complexity
- EU refusing to recognise UK taxonomy equivalence
- Political interference in classification criteria undermining scientific credibility

**Related Stakeholders**: City Minister (political sponsor), FCA (regulatory enforcement), GTAG (scientific credibility), Financial sector (adoption)

---

### SD-2: FCA — Regulatory Integration with SDR and Anti-Greenwashing Rule

**Stakeholder**: Financial Conduct Authority

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Integrate the Green Taxonomy Platform with the FCA's Sustainability Disclosure Requirements (SDR) framework and anti-greenwashing rule, providing regulated firms with a definitive, machine-readable classification that reduces compliance costs and enables effective supervision.

**Context & Background**:
The FCA's SDR (effective 2024) introduces four sustainability investment labels (Sustainability Focus, Sustainability Improvers, Sustainability Impact, Sustainability Mixed Goals) and an anti-greenwashing rule requiring all sustainability claims to be "fair, clear and not misleading." The Green Taxonomy provides the objective criteria against which these claims can be assessed. The FCA needs a platform that produces auditable, consistent classification decisions that it can use as evidence in enforcement actions.

**Driver Intensity**: CRITICAL

**Enablers**:

- Machine-readable classification output (API, structured data)
- Auditable decision trail showing how each classification was determined
- Consistent interpretation of criteria across all users (no subjective judgement)
- Real-time classification API enabling fund managers to screen investments at scale
- Bulk classification capability for portfolio-level assessment

**Blockers**:

- Subjective classification criteria requiring expert judgement (not machine-readable)
- Platform producing advisory opinions rather than definitive classifications
- No audit trail for classification decisions
- Classification latency too high for real-time investment screening

**Related Stakeholders**: HMT Green Finance Team (policy owner), Financial sector (regulated firms), GTAG (criteria definition)

---

### SD-3: Green Technical Advisory Group — Scientific Integrity of Classification Criteria

**Stakeholder**: Green Technical Advisory Group (GTAG)

**Driver Category**: STRATEGIC / RISK

**Driver Statement**: Ensure the taxonomy classification criteria are grounded in robust climate science, aligned with 1.5C pathways, and include credible "do no significant harm" (DNSH) screening — the GTAG's reputation depends on the scientific integrity of the criteria it recommends.

**Context & Background**:
The GTAG was established by HMT to provide independent, science-based advice on Green Taxonomy criteria. GTAG members include climate scientists, environmental economists, and sustainability experts. The group's credibility depends on producing criteria that withstand academic and NGO scrutiny. The EU Taxonomy has faced criticism for including gas and nuclear under political pressure — GTAG is determined to avoid similar reputational damage to the UK taxonomy.

**Driver Intensity**: HIGH

**Enablers**:

- Criteria development process that is transparent, evidence-based, and peer-reviewed
- Clear separation between GTAG scientific recommendations and HMT political decisions
- DNSH screening that genuinely prevents harmful activities from gaining green classification
- Regular criteria review cycle aligned with evolving climate science (IPCC AR7)

**Blockers**:

- Political pressure to weaken criteria for politically favoured sectors
- Platform launching with criteria that GTAG has not endorsed
- Transition activity criteria that are too permissive, enabling greenwashing
- Insufficient GTAG resource to develop criteria across all sectors simultaneously

**Related Stakeholders**: HMT Green Finance Team (policy owner), FCA (enforcement), NGOs (scrutiny), Academic researchers (peer review)

---

### SD-4: Financial Sector — Simple, Rapid, Integrated Classification

**Stakeholder**: The Investment Association, UK Finance, ABI, pension funds, asset managers

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Access a fast, reliable, API-integrated classification service that enables real-time investment screening against Green Taxonomy criteria, with clear binary outcomes (aligned/not aligned) and minimal manual interpretation, reducing ESG compliance costs.

**Context & Background**:
Financial institutions manage billions of pounds in ESG-labelled funds and face increasing regulatory pressure (FCA SDR, anti-greenwashing rule) to substantiate sustainability claims. Current ESG classification relies on third-party data providers (MSCI, Sustainalytics) with inconsistent methodologies. A government-backed taxonomy with a machine-readable classification API would provide a single source of truth, reduce reliance on expensive third-party ESG ratings, and provide legal certainty for sustainability claims.

**Driver Intensity**: HIGH

**Enablers**:

- Sub-second API response time for individual classification queries
- Bulk classification API for portfolio screening (10,000+ activities per request)
- Clear documentation with worked examples for each sector
- Sandbox/test environment for integration development
- Classification results that can be referenced in regulatory filings (FCA-recognised)

**Blockers**:

- Complex, ambiguous criteria requiring manual expert interpretation
- Slow classification response time preventing real-time use
- Frequent criteria changes disrupting investment processes
- No API access — web-only interface requiring manual data entry

**Related Stakeholders**: FCA (regulatory recognition), GTAG (criteria complexity), HMT (policy framework)

---

### SD-5: Environmental NGOs — Preventing Greenwashing

**Stakeholder**: Environmental NGOs (ShareAction, ClientEarth, Carbon Tracker, E3G, Positive Money)

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure the Green Taxonomy Platform implements rigorous criteria that genuinely distinguish between green and non-green activities, includes robust DNSH screening, and does not enable financial institutions to greenwash fossil fuel investments as "transition" activities.

**Context & Background**:
NGOs have been highly critical of greenwashing in financial markets — ESG funds that hold fossil fuel companies, green bonds funding airport expansion, and banks claiming climate leadership while financing new oil and gas. The EU Taxonomy's inclusion of gas as a "transition" activity attracted strong NGO criticism. NGOs want the UK taxonomy to set a higher bar, with transparent criteria, genuine DNSH screening, and no political carve-outs for favoured sectors.

**Driver Intensity**: HIGH

**Enablers**:

- Open, machine-readable publication of all classification criteria
- Transparent decision logs showing how classifications are determined
- Robust DNSH screening that excludes activities with significant environmental harm
- Public reporting of aggregate classification statistics (what % of financial products achieve taxonomy alignment)
- Whistleblower mechanism for reporting suspected misclassification

**Blockers**:

- Weak transition activity criteria enabling fossil fuel greenwashing
- Opaque classification decisions with no public audit trail
- Political interference weakening GTAG recommendations
- No mechanism for challenging questionable classifications

**Related Stakeholders**: GTAG (scientific integrity), FCA (enforcement), Media (public scrutiny), Academic researchers (analysis)

---

## Driver-to-Goal Mapping

### Goal G-1: Launch API-First Classification Service

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: SRO

**Goal Statement**: Launch a public API classification service covering energy, transport, buildings, and manufacturing sectors within 12 months, with sub-second response time and bulk classification capability.

**Success Metrics**:

- **Primary Metric**: API live with 4+ sectors, sub-second response time
- **Secondary Metrics**:
  - 50+ financial institutions integrated within 6 months of launch
  - Bulk classification processing 10,000+ queries per request
  - 99.9% API availability

---

### Goal G-2: Achieve GTAG Endorsement of Classification Criteria

**Derived From Drivers**: SD-3, SD-1, SD-5

**Goal Owner**: HMT Green Finance Team Lead

**Goal Statement**: Achieve formal GTAG endorsement of classification criteria for all launch sectors within 9 months, including DNSH screening methodology.

**Success Metrics**:

- **Primary Metric**: Written GTAG endorsement of criteria for all launch sectors
- **Secondary Metrics**:
  - DNSH screening methodology peer-reviewed by at least 2 independent academic institutions
  - No significant NGO criticism of criteria scientific basis within 6 months of publication

---

### Goal G-3: Establish EU Taxonomy Interoperability

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: HMT Green Finance Team Lead

**Goal Statement**: Publish a formal interoperability mapping between UK Green Taxonomy and EU Taxonomy criteria within 6 months of UK taxonomy launch, enabling cross-border investment classification.

**Success Metrics**:

- **Primary Metric**: Published interoperability mapping document covering shared sectors
- **Secondary Metrics**:
  - API supports dual UK/EU taxonomy classification queries
  - Financial sector confirms mapping is usable for cross-border fund compliance

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| HMT Green Finance | SD-1 | Global green finance centre | G-1 | API classification service | O-1 | UK green finance leadership |
| HMT Green Finance | SD-1 | Global green finance centre | G-3 | EU interoperability | O-1 | UK green finance leadership |
| FCA | SD-2 | SDR integration | G-1 | API classification service | O-1 | UK green finance leadership |
| GTAG | SD-3 | Scientific integrity | G-2 | GTAG endorsement | O-1 | UK green finance leadership |
| Financial sector | SD-4 | Rapid classification | G-1 | API classification service | O-1 | UK green finance leadership |
| NGOs | SD-5 | Prevent greenwashing | G-2 | GTAG endorsement | O-1 | UK green finance leadership |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Financial sector wants simple, binary classification (SD-4) vs GTAG insists on nuanced, multi-criteria assessment (SD-3)
  - **Resolution Strategy**: Machine-readable criteria with automated classification engine — complexity handled by the platform, not the user. Binary output (aligned/not aligned/insufficient data) with detailed breakdown available on demand.

- **Conflict 2**: HMT wants to include transition activities for pragmatism (SD-1) vs NGOs see transition categories as greenwashing risk (SD-5)
  - **Resolution Strategy**: Separate "taxonomy-aligned" and "transition" classifications with distinct labels, strict time-bound transition pathways, and mandatory transition plan requirements.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Classification criteria | GTAG Chair | City Minister | FCA, financial sector, NGOs | All stakeholders |
| Platform architecture | Technical Lead | SRO | FCA, CDDO | Financial sector |
| Sector coverage sequencing | HMT Green Finance | City Minister | GTAG, financial sector | All stakeholders |
| API design | Technical Lead | HMT CDIO | Financial sector, FCA | GTAG |
| EU interoperability | HMT Green Finance | City Minister | EU Commission (DG FISMA) | FCA, financial sector |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK Green Finance Strategy | Policy | GOV.UK | Green taxonomy commitment | N/A — external reference |
| GTAG Reports | Advisory reports | GOV.UK | Taxonomy criteria recommendations | N/A — external reference |
| FCA SDR Policy Statement | Regulation | FCA | Sustainability labels, anti-greenwashing rule | N/A — external reference |
| EU Taxonomy Regulation | Legislation | EUR-Lex | EU classification framework, interoperability reference | N/A — external reference |
| TCFD Recommendations | Standard | FSB | Climate financial disclosure framework | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Green Finance Taxonomy Platform (Project 005)
**Model**: Claude Opus 4.6
