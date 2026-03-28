# Strategic Outline Business Case (SOBC): Accessibility Compliance Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Accessibility Compliance Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Accessibility Compliance Platform, GDS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Leadership, CDDO, Cabinet Office Finance, EHRC |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the rationale, options, and indicative costs for establishing a centralised Accessibility Compliance Platform to monitor public sector website accessibility under the Public Sector Bodies Accessibility Regulations 2018 (PSBAR). It follows the HM Treasury Green Book five-case model and is informed by stakeholder analysis (ARC-001-STKE-v1.0) and requirements (ARC-001-REQ-v1.0).

---

## Executive Summary

**Purpose**: Establish a GDS-operated platform to monitor, assess, and drive improvement in public sector website accessibility, addressing the NAO finding that fewer than 40% of public sector websites meet WCAG 2.1 Level AA despite six years of PSBAR legislation.

**Problem Statement**: There is no centralised monitoring of public sector accessibility compliance. EHRC enforcement is complaint-driven and resource-constrained. GDS conducts only sample-based manual audits covering fewer than 500 of 12,000+ in-scope websites. Accessibility failures exclude disabled citizens from government services.

**Proposed Solution**: Build a cloud-native platform integrating axe-core and WAVE automated scanning engines with a blended assessment methodology (automated + expert review + lived-experience testing), providing a compliance dashboard, developer API, and EHRC enforcement evidence capability.

**Strategic Fit**: Directly supports the Equality Act 2010 duty, PSBAR 2018 compliance, GDS Service Standard (Point 5: accessibility), and the UK Digital Strategy commitment to inclusive digital services.

**Investment Required**: GBP 5.8M over 3 years

- Capital: GBP 2.8M
- Operational (3 years): GBP 3.0M

**Expected Benefits**: GBP 12.4M over 3 years

- Cost avoidance: GBP 9.0M (vs commissioning equivalent manual audits)
- Efficiency: GBP 2.4M (departmental remediation cost reduction)
- Social value: GBP 1.0M (improved disabled citizen access to services)

**Return on Investment**:

- NPV: GBP 5.8M (discounted at 3.5%)
- Payback Period: 14 months
- ROI: 114%

**Recommended Option**: Option 2: Balanced Approach — Automated scanning at scale with blended assessment for high-risk sites

**Key Risks**:

1. Disability sector rejects automated-only assessment as "accessibility theatre"
2. Departments lack resources to remediate identified accessibility failures
3. EHRC enforcement methodology diverges from platform assessment approach

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The current state of public sector accessibility compliance is untenable — fewer than 40% compliance rate despite legal obligation. The platform offers a 114% ROI through cost avoidance versus manual auditing, while providing the monitoring capability that NAO has called for. Failure to act risks further NAO and PAC criticism.

**Next Steps if Approved**:

1. Secure GDS/Cabinet Office funding approval: Q2 2026
2. Discovery phase with disability sector engagement: Q2-Q3 2026
3. Alpha build with axe-core scanning proof of concept: Q3-Q4 2026
4. Develop Outline Business Case (OBC): Q4 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The PSBAR 2018 requires all public sector websites and mobile applications to meet WCAG 2.1 Level AA. Six years after legislation, compliance remains poor. GDS has no centralised monitoring capability, relying on ad hoc sample audits of fewer than 500 websites from an estimated 12,000+ in scope.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| GDS Director General | SD-1 | No visibility into compliance landscape | Cannot report progress to ministers | CRITICAL |
| EHRC | SD-2 | Complaint-driven enforcement, expensive manual audits | Fewer than 50 enforcement actions per year | HIGH |
| RNIB | SD-3 | Automated tools miss 60% of barriers | Disabled citizens encounter undiscovered barriers | HIGH |
| Dept web teams | SD-4 | No actionable guidance, lengthy PDF audit reports | Accessibility failures persist in production | MEDIUM |

**Consequences of Inaction**:

- Continued PSBAR non-compliance across 60%+ of public sector websites, excluding disabled citizens from government services
- Further NAO and PAC criticism of GDS's failure to provide monitoring capability (follow-up report expected 2027)
- EHRC enforcement remains reactive and under-resourced, with no improvement trajectory
- UK falls behind EU Member States implementing the European Accessibility Act with centralised monitoring

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: ARC-001-STKE-v1.0

**Primary Drivers**:

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | GDS Director General | STRATEGIC | Demonstrate measurable accessibility improvement | Programme credibility |
| SD-2 | EHRC | COMPLIANCE | Enforcement-grade evidence at scale | Legal compliance |
| SD-3 | RNIB | CUSTOMER | Lived experience in compliance assessment | Inclusion integrity |
| SD-6 | Cabinet Office Finance | FINANCIAL | Cost-efficient monitoring vs manual audits | Value for money |

**Strategic Alignment**:

- **Equality Act 2010**: Duty to make reasonable adjustments and anticipatory duty for service providers
- **PSBAR 2018**: Legal requirement for public sector website accessibility
- **GDS Service Standard (Point 5)**: Make sure everyone can use the service
- **UK Digital Strategy**: Commitment to inclusive digital services
- **Architecture Principles**: Principles 1 (Inclusive Design), 2 (WCAG 2.2 AA Minimum), 20 (Social Model of Disability)

### A1.3 Scope

**In Scope**:

- Automated WCAG 2.2 scanning engine
- Compliance dashboard and analytics
- Blended assessment workflow
- Developer API for CI/CD integration
- Lived-experience testing panel management
- EHRC enforcement evidence generation

**Out of Scope**:

- Private sector website scanning (Phase 2)
- Mobile application testing (Phase 2)
- Direct remediation services

### A1.4 Why Now?

**Urgency Factors**:

- NAO follow-up report on digital accessibility expected 2027 — GDS needs demonstrable progress
- European Accessibility Act implementation across EU creating comparator expectations
- WCAG 2.2 published in 2023 — UK public sector has not systematically assessed against new standard
- EHRC has signalled intention to increase PSBAR enforcement activity

**Opportunity Cost of Delay**:

- GBP 250K per month in continued manual audit costs for the limited sampling GDS currently performs
- Reputational damage from continued NAO/PAC criticism
- Growing accessibility debt across public sector websites becomes harder to remediate

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Scanning Coverage**: Achieve 95% coverage of in-scope websites within 12 months
   - **Measure**: Websites scanned / total in-scope websites
   - **Threshold**: Minimum 80%

2. **Compliance Improvement**: Public sector WCAG 2.2 compliance rate improves measurably
   - **Measure**: Percentage of scanned sites meeting WCAG 2.2 AA
   - **Threshold**: From 40% to 55% within 18 months

3. **Disability Sector Endorsement**: Blended assessment methodology endorsed by major disability charities
   - **Measure**: Formal endorsement from RNIB, Scope, AbilityNet
   - **Threshold**: At least 2 of 3 endorse

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current ad hoc sample-based manual auditing by GDS accessibility team.

**Costs** (3-year):

- Capital: GBP 0
- Operational: GBP 4.5M (GDS accessibility team salaries, manual audit commissions)
- Total: GBP 4.5M

**Benefits**: GBP 0 (no improvement in monitoring capability)

**Pros**:

- No upfront investment
- No implementation risk

**Cons**:

- Only 500 of 12,000+ websites audited
- NAO/PAC criticism continues
- EHRC enforcement remains complaint-driven
- Compliance rate stagnates at ~40%
- UK falls behind EU accessibility monitoring

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable baseline. NAO criticism will intensify and disabled citizens remain excluded from government services.

---

### Option 1: Automated Scanning Only

**Description**: Deploy automated scanning (axe-core) across all public sector websites without blended assessment or lived-experience testing.

**Costs** (3-year) — ROM (+-40%):

- Capital: GBP 1.2M (platform development, cloud infrastructure setup)
- Operational: GBP 1.5M over 3 years (hosting, scanning costs, team)
- Total 3-year TCO: GBP 2.7M

**Benefits** (3-year):

- Cost avoidance vs manual audits: GBP 7.0M
- Departmental efficiency: GBP 1.0M
- Total: GBP 8.0M

**Net Benefit**: GBP 5.3M

**Pros**:

- Lower cost than balanced approach
- Rapid deployment (6 months to MVP)
- Comprehensive coverage achievable quickly

**Cons**:

- Automated tools detect only 30-40% of WCAG violations
- Disability sector will reject as "accessibility theatre"
- EHRC may not accept automated-only evidence for enforcement
- Cognitive accessibility almost entirely missed

**Stakeholder Impact**:

- GDS Director General (SD-1): Partially met — coverage achieved but credibility undermined
- EHRC (SD-2): Not met — evidence may be insufficient for enforcement
- RNIB (SD-3): Not met — lived experience excluded
- Dept web teams (SD-4): Partially met — guidance available but limited to automated findings

**Stakeholder Goals Met**: 35%

**Recommendation**: **Reject** — Cost effective but fatally undermines credibility with disability sector and EHRC.

---

### Option 2: Balanced Approach (RECOMMENDED)

**Description**: Automated scanning at scale for all websites, combined with blended assessment (automated + expert review + lived-experience testing) for the 500 highest-traffic and highest-risk websites. Developer API for CI/CD integration.

**Costs** (3-year) — ROM (+-30%):

- Capital: GBP 2.8M
  - Platform development: GBP 1.5M
  - Scanning engine integration: GBP 0.4M
  - Blended assessment tooling: GBP 0.3M
  - Cloud infrastructure setup: GBP 0.3M
  - Lived-experience panel setup: GBP 0.3M
- Operational: GBP 3.0M over 3 years
  - Cloud hosting and scanning: GBP 0.5M/year
  - Platform team (6 FTE): GBP 0.4M/year
  - Lived-experience panel compensation: GBP 0.1M/year
- Total 3-year TCO: GBP 5.8M

**Benefits** (3-year):

| Benefit ID | Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Cost avoidance vs manual auditing | SD-6 G-1 | FINANCIAL | GBP 1.5M | GBP 3.5M | GBP 4.0M | GBP 9.0M |
| B-002 | Departmental remediation efficiency | SD-4 G-4 | OPERATIONAL | GBP 0.2M | GBP 0.8M | GBP 1.4M | GBP 2.4M |
| B-003 | Improved disabled citizen access | SD-3 G-3 | SOCIAL | GBP 0.1M | GBP 0.4M | GBP 0.5M | GBP 1.0M |
| **Total** | | | | **GBP 1.8M** | **GBP 4.7M** | **GBP 5.9M** | **GBP 12.4M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 11.4M
- Total Costs PV: GBP 5.6M
- **NPV: GBP 5.8M**

**Return on Investment**:

- **ROI: 114%** over 3 years
- **Payback Period: 14 months**

**Pros**:

- 85% of stakeholder goals met
- Comprehensive automated coverage with credible blended assessment
- Developer API enables shift-left accessibility testing
- Disability sector endorsement achievable through lived-experience inclusion
- Positive NPV GBP 5.8M

**Cons**:

- Higher upfront investment than Option 1
- Blended assessment complex to operationalise
- 12-month implementation timeline for full capability

**Stakeholder Impact**:

- GDS Director General (SD-1): Met — comprehensive coverage with credible methodology
- EHRC (SD-2): Met — blended evidence suitable for enforcement proceedings
- RNIB (SD-3): Met — lived-experience testing integrated into assessment
- Dept web teams (SD-4): Met — developer API with actionable guidance
- Scope (SD-5): Met — cognitive accessibility addressed through user testing
- Cabinet Office Finance (SD-6): Met — 114% ROI, significant cost avoidance

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive Audit Service

**Description**: Full-service accessibility audit platform providing automated scanning, expert review, and lived-experience testing for all 12,000+ websites, with GDS-provided remediation consultancy.

**Costs** (3-year) — ROM (+-40%):

- Capital: GBP 6.5M
- Operational: GBP 9.0M over 3 years
- Total 3-year TCO: GBP 15.5M

**Benefits** (3-year): GBP 15.0M (marginally higher than Option 2)

**Net Benefit**: GBP -0.5M (negative due to diminishing returns at scale)

**Pros**:

- 100% of stakeholder goals met
- Every website receives full blended assessment
- Remediation support accelerates improvement

**Cons**:

- GBP 15.5M cost is disproportionate
- Requires 50+ FTE lived-experience testing panel
- 24-month implementation delays initial value delivery
- Negative NPV — not value for money

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Negative NPV. Diminishing returns from full blended assessment of all 12,000 sites do not justify the cost. The balanced approach covers 95% of citizen impact through prioritised blended assessment.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-year cost | GBP 4.5M | GBP 2.7M | GBP 5.8M | GBP 15.5M |
| 3-year benefit | GBP 0 | GBP 8.0M | GBP 12.4M | GBP 15.0M |
| NPV | -GBP 4.5M | GBP 4.5M | GBP 5.8M | -GBP 0.5M |
| Stakeholder goals met | 0% | 35% | 85% | 100% |
| Disability sector endorsement | No | No | Yes | Yes |
| Implementation time | N/A | 6 months | 12 months | 24 months |
| **Recommendation** | **Reject** | **Reject** | **RECOMMENDED** | **Reject** |

---

# PART C: COMMERCIAL CASE

## C1. Procurement Approach

**Strategy**: Build on open source (axe-core is open source), supplemented by commercial API integrations (WAVE API) and Crown Commercial Service framework procurement for cloud hosting.

**Key Procurements**:

- Cloud hosting: CCS G-Cloud framework (estimated GBP 150K/year)
- WAVE API licence: Direct commercial agreement (estimated GBP 30K/year)
- Specialist accessibility consultancy for blended assessment methodology: CCS Digital Outcomes & Specialists

**Make vs Buy**: Build. No commercial off-the-shelf platform provides the combination of automated scanning, blended assessment workflow, and EHRC evidence generation required. axe-core (open source) provides the scanning foundation.

---

# PART D: FINANCIAL CASE

## D1. Funding Requirements

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (development) | GBP 2.0M | GBP 0.5M | GBP 0.3M | GBP 2.8M |
| Operational (hosting, team, panel) | GBP 0.8M | GBP 1.0M | GBP 1.2M | GBP 3.0M |
| **Total** | **GBP 2.8M** | **GBP 1.5M** | **GBP 1.5M** | **GBP 5.8M** |

**Funding Source**: Cabinet Office / GDS programme budget

**Budget Confidence**: ROM +-30% at SOBC stage. OBC will refine to +-15%.

---

# PART E: MANAGEMENT CASE

## E1. Governance

- **SRO**: GDS Director General
- **Programme Board**: GDS, CDDO, EHRC (observer), RNIB (observer), Cabinet Office Finance
- **Delivery Methodology**: Agile (GDS service design phases: Discovery, Alpha, Beta, Live)
- **Assurance**: GDS Service Assessment at Alpha, Beta, and Live gates

## E2. Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|-------------|
| SOBC approval | Q2 2026 | This document |
| Discovery complete | Q3 2026 | SOBC approval |
| Alpha complete (scanning POC) | Q4 2026 | Discovery findings |
| Beta launch (scanning at scale) | Q2 2027 | Alpha assessment pass |
| Blended assessment operational | Q3 2027 | Panel recruitment |
| Live service | Q4 2027 | Beta assessment pass |

## E3. Risk Summary

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Disability sector rejects methodology | MEDIUM | HIGH | Co-design with RNIB, Scope, Mencap from Discovery |
| Departments cannot remediate | HIGH | HIGH | Central remediation fund advocacy, prioritised guidance |
| EHRC enforcement divergence | MEDIUM | MEDIUM | Joint GDS-EHRC methodology working group |
| axe-core sustainability | LOW | HIGH | Deque-backed, large community; contingency for fork |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PSBAR 2018 | Legislation | legislation.gov.uk | Monitoring and enforcement framework | N/A |
| HM Treasury Green Book | Guidance | GOV.UK | Five-case business case methodology | N/A |
| NAO Digital Accessibility 2024 | Report | NAO | 40% compliance finding, monitoring gap | N/A |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers informing strategic case | projects/001-accessibility-compliance-platform/ |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | Functional and NFR requirements | projects/001-accessibility-compliance-platform/ |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Accessibility Compliance Platform
**Model**: Claude Opus 4.6
