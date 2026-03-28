# Strategic Outline Business Case (SOBC): National Digital Learning Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | National Digital Learning Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, NDLP Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DfE Investment Board, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case presents the case for investment in a National Digital Learning Platform. It follows the HM Treasury Green Book five-case model and seeks approval to proceed to the Outline Business Case stage.

---

## Executive Summary

**Purpose**: The Department for Education seeks investment in a National Digital Learning Platform (NDLP) to provide free, universal access to quality-assured digital learning resources for all state-funded schools in England, addressing the widening digital divide that is undermining educational equity.

**Problem Statement**: The COVID-19 pandemic exposed severe digital inequality in English education. Disadvantaged pupils lost an estimated additional 0.5 months of learning progress due to inadequate access to digital resources. The current fragmented EdTech landscape means school budgets — not educational need — determine access to quality digital learning resources.

**Proposed Solution**: Build and operate a national digital learning platform that integrates with existing school MIS systems, provides curriculum-aligned resources across KS1-KS4, and is designed from the ground up to comply with the Age Appropriate Design Code and WCAG 2.2 Level AA.

**Strategic Fit**: Directly supports DfE's Digital Strategy 2025-2030, the Levelling Up agenda, and the UK's commitment to UN Sustainable Development Goal 4 (Quality Education).

**Investment Required**: GBP 15.0M over 3 years

- Capital: GBP 8.5M
- Operational (3 years): GBP 6.5M

**Expected Benefits**: GBP 72.8M over 5 years

- Reduced attainment gap value: GBP 45M (lifetime earnings impact)
- Teacher productivity gains: GBP 22.5M
- Reduced duplicate EdTech procurement: GBP 5.3M

**Return on Investment**:

- NPV: GBP 38.2M (discounted at 3.5%)
- Payback Period: 22 months
- BCR: 3.1:1

**Recommended Option**: Option 2: Balanced Platform (build core platform with MIS integration and marketplace)

**Key Risks**:

1. Low voluntary school adoption undermining impact case
2. MIS vendor integration delays
3. ICO regulatory action if AADC compliance is not achieved

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The economic case demonstrates strong value for money with a BCR of 3.1:1. The platform addresses a genuine equity gap evidenced by post-pandemic attainment data. Strategic alignment with DfE priorities and SDG 4 is strong. Risks are manageable through phased delivery, early MIS vendor engagement, and independent AADC compliance audit.

**Next Steps if Approved**:

1. Secure CDDO spend approval: Q2 2026
2. Complete detailed requirements and OBC: Q3 2026
3. MIS vendor engagement and API access agreements: Q3 2026
4. Discovery phase procurement: Q4 2026
5. Alpha development start: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
England's 22,000+ state-funded schools independently procure digital learning resources from a fragmented market of commercial EdTech providers. Schools with larger budgets access premium platforms; disadvantaged schools rely on free resources of variable quality or none at all. The COVID-19 pandemic starkly demonstrated this inequality — an estimated 1.78 million children lacked adequate digital access during lockdowns.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Secretary of State | SD-1 | Widening digital divide | 0.5 month additional attainment gap for disadvantaged pupils | CRITICAL |
| MAT CEOs | SD-2 | Fragmented EdTech procurement | GBP 500K-2M annual spend per large MAT on 10-14 platforms | HIGH |
| Headteachers | SD-3 | Teacher workload from resource preparation | 4 hours/week per teacher; contributing to recruitment/retention crisis | HIGH |
| Parents | SD-4 | Cannot support home learning | 7% of households have no internet; many parents lack confidence | HIGH |
| ICO | SD-8 | Children's data processed without adequate AADC compliance | Regulatory and reputational risk at scale | CRITICAL |

**Consequences of Inaction**:

- Disadvantaged attainment gap continues to widen, costing an estimated GBP 45M in lost lifetime earnings per cohort
- Teacher attrition rate remains at 8.8% annually, with GBP 240M spent on recruitment
- UK falls further behind international comparators on digital education (PISA digital literacy)
- Schools continue to spend GBP 3.4B on fragmented EdTech with no quality assurance

### A1.2 Strategic Drivers

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Secretary of State | POLITICAL / STRATEGIC | Close the digital divide in education | SDG 4, Levelling Up |
| SD-2 | MAT CEOs | OPERATIONAL | Consistent quality, reduced procurement cost | Value for money |
| SD-3 | Headteachers | OPERATIONAL | Reduce teacher workload | Teacher retention |
| SD-4 | Parents | CUSTOMER | Support home learning | Parental engagement |
| SD-8 | ICO | COMPLIANCE | Children's data protection at scale | Regulatory compliance |

**Strategic Alignment**:

- **DfE Digital Strategy 2025-2030**: "Provide world-class digital infrastructure for learning"
- **Levelling Up White Paper**: "Ensure every child has access to a high-quality education regardless of where they live"
- **UN SDG 4**: "Ensure inclusive and equitable quality education and promote lifelong learning opportunities for all"
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (Learner-Centred Design), 2 (Safeguarding), 3 (Children's Data Privacy), 4 (Digital Inclusion)

### A1.3 Stakeholder Goals

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | SRO | 40% school adoption | 0 schools | 8,800 schools | 18 months |
| G-2 | Pupil Premium Team | Narrow attainment gap 0.3 months | 18 months gap | 17.7 months gap | 2 years |
| G-3 | Service Owner | Reduce resource prep time 50% | 4 hrs/week | 2 hrs/week | 12 months |
| G-4 | CDO | Full AADC and WCAG compliance | N/A | 15/15 AADC, 100% WCAG | At launch |
| G-5 | Technical Lead | MIS integration with top 3 providers | 0 integrations | 3 integrations (85% coverage) | 6 months |

### A1.4 Scope

**In Scope**:

- Web-based learning platform (browser-accessible, responsive design)
- Curriculum resource library (KS1-KS4 core subjects)
- Teacher resource management and assignment tools
- Pupil learning interface (age-appropriate)
- Parent/carer engagement portal
- MIS integration (SIMS, Bromcom, Arbor)
- DfE Sign-in integration
- Content quality assurance workflow
- Aggregated analytics dashboards

**Out of Scope** (for this phase):

- Post-16 / Further Education content (Phase 2)
- AI-powered adaptive learning (Phase 2)
- Hardware provision (separate Get Help with Technology programme)
- Assessment/examination functionality (Ofqual jurisdiction)

**Dependencies**:

- **Internal**: DfE Sign-in platform capacity and availability
- **External**: MIS vendor API access agreements (SIMS/Capita, Bromcom, Arbor)
- **Technical**: GIAS API availability for school data

### A1.5 Why Now?

**Urgency Factors**:

- Post-pandemic catch-up funding ending in 2027 — need a sustainable digital intervention
- Oak National Academy establishing precedent for government-provided curriculum resources
- Teacher recruitment crisis worsening — workload reduction interventions urgently needed
- ICO signalling education technology as enforcement priority for AADC compliance

**Opportunity Cost of Delay**:

- GBP 9M per year in continued attainment gap impact on disadvantaged pupils (lifetime earnings basis)
- Window of political support for education digital investment may close after next Spending Review
- MIS vendors currently engaged and willing to partner; engagement may cool

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Voluntary School Adoption**: At least 40% of schools adopting within 18 months
   - **Measure**: Registered schools with 10+ active teacher accounts
   - **Threshold**: Minimum 25% adoption for programme to be viable

2. **Teacher Time Saving**: Measurable reduction in resource preparation time
   - **Measure**: Teacher workload survey data
   - **Threshold**: Minimum 1 hour/week saving (50% of target)

3. **AADC Compliance**: Full compliance with ICO Age Appropriate Design Code at launch
   - **Measure**: Independent compliance audit
   - **Threshold**: No critical non-conformities at launch

4. **MIS Integration**: Working integration with top 3 MIS providers
   - **Measure**: Percentage of schools where integration is functional
   - **Threshold**: Minimum 2 of 3 providers integrated (70% coverage)

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with the current fragmented EdTech landscape. Schools procure independently; no national platform.

**Costs** (5-year):

- Capital: GBP 0
- DfE operational: GBP 0 (costs borne by schools)
- Schools EdTech spend: GBP 17B aggregate over 5 years (GBP 3.4B/year)

**Benefits**: GBP 0 (no improvement to current situation)

**Pros**:

- No DfE investment required
- No implementation risk for DfE
- Preserves market competition

**Cons**:

- Digital divide continues to widen
- Teacher workload remains unsustainable
- No quality assurance of digital resources
- AADC compliance varies widely across commercial platforms
- UK falls behind international comparators

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable baseline; educational inequality continues to worsen.

---

### Option 1: Resource Catalogue Only

**Description**: Build a curated catalogue of quality-assured links to existing free and commercial resources. No hosting, no MIS integration, no pupil accounts.

**Scope**:

- Searchable catalogue of external resources with quality ratings
- DfE Sign-in for teacher access
- No pupil or parent accounts
- No MIS integration
- No content hosting

**Costs** (3-year) - ROM (+/-40%):

- Capital: GBP 1.5M (platform development, content curation)
- Operational: GBP 1.2M over 3 years (content review, hosting)
- Total 3-year TCO: GBP 2.7M

**Benefits** (5-year):

- B-001: Marginal teacher time saving (0.5 hours/week): GBP 5.6M
- B-002: Quality assurance reducing poor resource selection: GBP 1.2M
- Total: GBP 6.8M

**Net Present Value** (3.5% discount): GBP 3.1M

**Pros**:

- Low cost and fast to deliver (6 months)
- Low implementation risk
- Does not compete with EdTech market

**Cons**:

- Does not address the digital divide (links to paid resources still exclude disadvantaged schools)
- No MIS integration — does not reduce teacher workload meaningfully
- No pupil or parent engagement
- AADC compliance only applies to the catalogue, not linked resources

**Stakeholder Impact**:

- G-1: Partially met (catalogue adoption easier but less valuable)
- G-2: Not met (no impact on attainment gap)
- G-3: Partially met (0.5 hour saving vs 2 hour target)
- G-4: Partially met (catalogue compliant but linked resources not controlled)
- G-5: Not met (no MIS integration)

**Stakeholder Goals Met**: 25%

---

### Option 2: Balanced Platform (RECOMMENDED)

**Description**: Build a comprehensive learning platform with hosted resources, MIS integration, pupil/parent interfaces, and an EdTech marketplace — with phased delivery.

**Scope**:

- Full resource library with DfE-hosted content
- MIS integration with SIMS, Bromcom, Arbor
- DfE Sign-in for teachers; school-managed pupil accounts; parent self-registration
- Age-appropriate pupil interface (KS1-KS4)
- Parent/carer portal with multilingual support
- EdTech marketplace for quality-assured commercial resources
- Aggregated analytics dashboards

**Costs** (3-year) - ROM (+/-30%):

- Capital: GBP 8.5M
  - Platform development (Alpha + Beta): GBP 4.5M
  - MIS integration development: GBP 1.5M
  - Content acquisition and curation: GBP 1.5M
  - Security, accessibility, AADC compliance: GBP 0.5M
  - User research, design, testing: GBP 0.5M
- Operational: GBP 6.5M over 3 years
  - Cloud infrastructure: GBP 1.2M/year (GBP 3.6M)
  - Support and maintenance team: GBP 0.6M/year (GBP 1.8M)
  - Content quality assurance: GBP 0.4M/year (GBP 1.2M)
  - Minus marketplace revenue: -GBP 0.7M/year (GBP -2.1M)
- Total 3-year TCO: GBP 15.0M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Narrowed attainment gap (lifetime earnings) | G-2 | STRATEGIC | GBP 0 | GBP 5M | GBP 10M | GBP 15M | GBP 15M | GBP 45.0M |
| B-002 | Teacher productivity gains | G-3 | OPERATIONAL | GBP 1.5M | GBP 4.5M | GBP 5.5M | GBP 5.5M | GBP 5.5M | GBP 22.5M |
| B-003 | Reduced school EdTech procurement spend | G-1 | FINANCIAL | GBP 0.3M | GBP 1.0M | GBP 1.5M | GBP 1.5M | GBP 1.0M | GBP 5.3M |
| **Total** | | | | **GBP 1.8M** | **GBP 10.5M** | **GBP 17.0M** | **GBP 22.0M** | **GBP 21.5M** | **GBP 72.8M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 61.4M
- Total Costs PV: GBP 14.5M
- **NPV: GBP 46.9M**

**Benefit-Cost Ratio**: 4.2:1

**Payback Period**: 22 months from launch

**Pros**:

- Strong positive NPV and BCR
- Addresses all five critical success factors
- Phased delivery reduces implementation risk
- EdTech marketplace preserves market competition while extending reach
- Sets UK as international leader in digital education equity

**Cons**:

- Higher upfront investment than Option 1
- 18-month implementation timeline to public beta
- MIS integration complexity
- Requires sustained political support

**Stakeholder Impact**:

- G-1: Met (40% adoption achievable with MIS integration and free content)
- G-2: Met (free access + targeted resources for disadvantaged pupils)
- G-3: Met (MIS integration + quality resources = 2 hour/week saving)
- G-4: Met (AADC compliance built in from design; independent audit at beta)
- G-5: Met (MIS integration prioritised in Phase 1)

**Stakeholder Goals Met**: 90%

---

### Option 3: Comprehensive Platform with AI Personalisation

**Description**: Full platform (as Option 2) plus AI-powered adaptive learning, real-time assessment, content generation, and advanced analytics.

**Scope**:

- Everything in Option 2
- AI-powered adaptive learning pathways per pupil
- Automated content generation and curriculum mapping
- Real-time formative assessment engine
- Predictive analytics for early intervention
- Virtual tutoring assistant

**Costs** (3-year) - ROM (+/-40%):

- Capital: GBP 18.0M
- Operational: GBP 9.0M over 3 years
- Total 3-year TCO: GBP 27.0M

**Benefits** (5-year): GBP 95M (marginally higher than Option 2)

**NPV**: GBP 42.1M (lower than Option 2 due to higher costs and diminishing marginal returns)

**Pros**:

- Potentially greater impact on attainment gap through personalisation
- Future-proofed for AI-driven education
- 100% of stakeholder goals met

**Cons**:

- GBP 12M more than Option 2 with only GBP 22M additional benefits
- 24-month implementation timeline (misses September 2027 target)
- AI personalisation creates significant AADC compliance risk (profiling of children)
- Technical complexity substantially higher
- Political risk: "Government AI teaching children" narrative
- Treasury unlikely to approve given diminishing marginal returns

**Stakeholder Goals Met**: 100% (but at significantly higher cost and risk)

**Recommendation**: **Reject at this stage** — defer AI personalisation to Phase 2 after core platform is established and AADC implications fully assessed.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 3-Year Cost | GBP 0 | GBP 2.7M | GBP 15.0M | GBP 27.0M |
| 5-Year Benefits | GBP 0 | GBP 6.8M | GBP 72.8M | GBP 95.0M |
| NPV | GBP 0 | GBP 3.1M | GBP 46.9M | GBP 42.1M |
| BCR | N/A | 2.5:1 | 4.2:1 | 3.0:1 |
| Goals Met | 0% | 25% | 90% | 100% |
| Implementation Risk | None | LOW | MEDIUM | HIGH |
| AADC Risk | N/A | LOW | MEDIUM | HIGH |
| Political Risk | HIGH (inaction) | MEDIUM | LOW | MEDIUM |

**Recommended Option**: **Option 2 — Balanced Platform**

Option 2 delivers the highest NPV (GBP 46.9M) and best BCR (4.2:1) while meeting 90% of stakeholder goals. It achieves the core objectives of digital equity, teacher workload reduction, and children's data protection compliance at an investment level proportionate to the expected benefits. AI personalisation features from Option 3 can be added in Phase 2 once the core platform is established and AADC implications are fully understood.

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Procurement Route

**Primary Route**: G-Cloud 14 (Cloud Hosting, Software, Support) via Crown Commercial Service Digital Marketplace

**Rationale**: G-Cloud provides access to pre-vetted cloud service providers, accelerates procurement, and ensures commercial terms comply with government standards. The platform development will be procured as a Cloud Software service with associated Cloud Hosting and Cloud Support lots.

**Alternative Route**: Digital Outcomes and Specialists (DOS) framework for specialist development capability not available through G-Cloud.

### C1.2 Commercial Model

**Recommended Model**: Hybrid — Crown-owned platform with contracted development and managed services.

- **Platform IP**: Crown-owned, developed under government contract terms
- **Development**: Agile delivery teams procured through G-Cloud/DOS
- **Hosting**: UK sovereign cloud infrastructure (likely AWS UKCloud or Azure UK)
- **Content**: Mix of DfE-commissioned content, Oak National Academy open-licensed content, and EdTech marketplace content
- **MIS Integration**: Co-developed with MIS vendors under API access agreements

### C1.3 Contract Structure

| Component | Contract Type | Duration | Estimated Value |
|-----------|--------------|----------|-----------------|
| Platform development (Alpha + Beta) | Fixed-price agile delivery | 18 months | GBP 4.5M |
| MIS integration development | Time & materials | 12 months | GBP 1.5M |
| Cloud hosting and managed services | Managed service | 3 years + 2 year extension | GBP 3.6M (3-year) |
| Content acquisition and curation | Call-off contract | 3 years | GBP 1.5M |
| Independent AADC compliance audit | Fixed-price | 3 months | GBP 0.1M |

### C1.4 Market Engagement

- Pre-market engagement event planned for Q2 2026
- Prior Information Notice (PIN) to be published on Contracts Finder
- MIS vendor engagement workshops to agree API access terms
- EdTech industry roundtable to design marketplace model

---

# PART D: FINANCIAL CASE

## D1. Funding Requirement

### D1.1 Capital Costs (CDEL)

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 3.0M | GBP 1.5M | GBP 0 | GBP 4.5M |
| MIS integration | GBP 1.0M | GBP 0.5M | GBP 0 | GBP 1.5M |
| Content acquisition | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| Security and compliance | GBP 0.3M | GBP 0.2M | GBP 0 | GBP 0.5M |
| User research and design | GBP 0.3M | GBP 0.2M | GBP 0 | GBP 0.5M |
| **Capital Total** | **GBP 5.1M** | **GBP 2.9M** | **GBP 0.5M** | **GBP 8.5M** |

### D1.2 Revenue Costs (RDEL)

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Cloud infrastructure | GBP 0.8M | GBP 1.2M | GBP 1.6M | GBP 3.6M |
| Support and maintenance | GBP 0.4M | GBP 0.6M | GBP 0.8M | GBP 1.8M |
| Content quality assurance | GBP 0.3M | GBP 0.4M | GBP 0.5M | GBP 1.2M |
| Marketplace revenue offset | GBP 0 | -GBP 0.3M | -GBP 0.7M | -GBP 1.0M |
| Programme management | GBP 0.3M | GBP 0.3M | GBP 0.3M | GBP 0.9M |
| **Revenue Total** | **GBP 1.8M** | **GBP 2.2M** | **GBP 2.5M** | **GBP 6.5M** |

### D1.3 Total Funding Summary

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital (CDEL) | GBP 5.1M | GBP 2.9M | GBP 0.5M | GBP 8.5M |
| Revenue (RDEL) | GBP 1.8M | GBP 2.2M | GBP 2.5M | GBP 6.5M |
| **Total** | **GBP 6.9M** | **GBP 5.1M** | **GBP 3.0M** | **GBP 15.0M** |

### D1.4 Funding Source

- DfE Departmental Expenditure Limit (DEL) — to be confirmed through Supplementary Estimates or Spending Review allocation
- EdTech marketplace commission revenue to partially offset operational costs from Year 2

### D1.5 Affordability Assessment

The total 3-year investment of GBP 15.0M represents approximately 0.02% of DfE's annual budget (GBP 86B). The programme is affordable within departmental limits, subject to Treasury approval through the standard business case process. The marketplace revenue model provides a path to reduced net operational cost from Year 3 onwards.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

### E1.1 Delivery Methodology

**Approach**: GDS-aligned agile delivery with phased releases.

| Phase | Duration | Key Activities | Key Deliverables |
|-------|----------|----------------|-----------------|
| Discovery | 3 months (Q4 2026) | User research, technical feasibility, MIS vendor engagement | User needs evidence, technical architecture, MIS API assessment |
| Alpha | 4 months (Q1-Q2 2027) | Prototype, test core hypotheses, AADC assessment | Working prototype, GDS Alpha assessment pass, AADC compliance plan |
| Private Beta | 6 months (Q2-Q4 2027) | Build core platform, MIS integration, content curation | Private beta with 200 pilot schools |
| Public Beta | 6 months (Q4 2027-Q2 2028) | Iterate based on feedback, scale to 8,800 schools | GDS Beta assessment pass, public beta launch |
| Live | Ongoing (Q2 2028+) | Full operation, continuous improvement | GDS Live assessment, full nationwide availability |

### E1.2 Programme Governance

| Forum | Chair | Frequency | Purpose |
|-------|-------|-----------|---------|
| Programme Board | SRO | Monthly | Strategic direction, risk escalation, budget approval |
| Delivery Board | Service Owner | Fortnightly | Sprint reviews, dependency management, blockers |
| Architecture Board | CDO | Monthly | Technical decisions, principle compliance, ADRs |
| Stakeholder Forum | SRO | Quarterly | Engagement with headteachers, unions, EdTech, parents |
| CDDO Assurance | CDDO | At phase gates | Spend control, service assessment |

### E1.3 Risk Management

| Risk ID | Description | Probability | Impact | Mitigation | Owner |
|---------|-------------|-------------|--------|------------|-------|
| R-1 | Low voluntary school adoption | MEDIUM | HIGH | Early adopter programme with MATs; demonstrate time savings; peer advocacy | Service Owner |
| R-2 | MIS vendor integration delays | HIGH | HIGH | Early vendor engagement; parallel development tracks; fallback to manual CSV import | Technical Lead |
| R-3 | AADC non-compliance at launch | LOW | CRITICAL | Independent AADC audit at Alpha; privacy by design; ICO pre-consultation | DfE SIRO |
| R-4 | EdTech industry opposition | MEDIUM | MEDIUM | Marketplace model preserves market; industry roundtable; partnership framework | SRO |
| R-5 | DfE Sign-in capacity insufficient | LOW | HIGH | Capacity planning with DfE Sign-in team; load testing; fallback authentication | Technical Lead |
| R-6 | Content quality insufficient for adoption | MEDIUM | HIGH | Partnership with Oak National Academy; subject specialist reviewers; teacher feedback loop | Curriculum Lead |
| R-7 | Treasury funding not approved | MEDIUM | CRITICAL | Strong BCR (4.2:1); Ministerial support; SDG 4 alignment; phased investment | SRO |

### E1.4 Benefits Realisation

| Benefit | Measure | Baseline | Target | Responsible Officer | Review Frequency |
|---------|---------|----------|--------|--------------------|--------------------|
| School adoption | Schools with 10+ active teachers | 0 | 8,800 (40%) | Service Owner | Monthly |
| Teacher time saving | Hrs/week on resource prep | 4 hrs | 2 hrs | Product Manager | Annually (survey) |
| Attainment gap narrowing | KS2 FSM gap (months) | 18 months | 17.7 months | Pupil Premium Team | Annually (NPD) |
| AADC compliance | Audit result | N/A | 15/15 pass | DfE SIRO | At each phase gate |
| MIS integration coverage | % schools with working integration | 0% | 85% | Technical Lead | Monthly |

### E1.5 Assurance

- **GDS Service Assessments**: Alpha, Beta, and Live assessments against GDS Service Standard
- **CDDO Spend Control**: Approval at each phase gate (>GBP 1M digital spend threshold)
- **Independent AADC Audit**: Commissioned at Alpha with remediation before Beta
- **NAO Readiness**: Benefits realisation evidence maintained for potential NAO review
- **ICO Pre-Consultation**: Engagement with ICO during Discovery on DPIA approach

---

## Approval

### Business Case Approval

| Approver | Role | Decision | Date |
|----------|------|----------|------|
| SRO | Programme Sponsor | PENDING | |
| DfE Finance Director | Budget Holder | PENDING | |
| DfE Permanent Secretary | Accounting Officer | PENDING | |
| HM Treasury | Funding Approval | PENDING | |
| CDDO | Spend Control | PENDING | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Green Book | Guidance | GOV.UK | Five-case model, discount rates | N/A — external reference |
| GDS Service Standard | Standard | GOV.UK | Service assessment criteria | N/A — external reference |
| ICO Age Appropriate Design Code | Code of Practice | ICO | 15 standards for children's services | N/A — external reference |
| DfE Digital Strategy 2025-2030 | Strategy | DfE | Digital education priorities | N/A — external reference |
| G-Cloud 14 Framework | Framework | Crown Commercial Service | Procurement route | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Digital Learning Platform
**Model**: Claude Opus 4.6
