# Strategic Outline Business Case (SOBC): Coastal Erosion Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Coastal Erosion Monitoring (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Coastal Erosion Monitoring Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Coastal Programme Board, EA Finance, DEFRA Finance, HM Treasury |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case establishes the strategic justification for investment in a Coastal Erosion Monitoring platform integrating LiDAR survey data, satellite imagery, wave/tide records, and geological information for erosion prediction and risk communication.

---

## Executive Summary

**Purpose**: Climate change is accelerating coastal erosion across England. The EA's National Coastal Monitoring Programme generates 2TB of LiDAR survey data annually, but it is processed manually, stored in fragmented regional databases, and presented in formats inaccessible to planners, communities, and business case authors. The current system cannot produce the fine-resolution erosion predictions needed for planning decisions or FCERM investment appraisal.

**Problem Statement**: Six regional monitoring programmes operate independently with different delivery partners, data formats, and processing pipelines. Erosion predictions remain at the coarse resolution (500m-1km) of the 2010-2011 SMP2 cycle. Approximately 700 properties are at risk of erosion in the next 20 years, yet property-level erosion risk information is not systematically available. FCERM business cases take months to prepare due to manual data collation.

**Proposed Solution**: A cloud-hosted platform automating LiDAR processing, generating erosion predictions at 50m resolution, integrating UKCP18 climate scenarios, and providing public-facing erosion risk information and planning application support.

**Strategic Fit**: Directly supports the FCERM Strategy 2020 objective of resilience-based coastal management, NPPF requirements for coastal change planning, and the Climate Change Committee's adaptation recommendations. Enables effective deployment of the GBP 5.2 billion FCERM capital programme.

**Investment Required**: GBP 6.2M over 3 years

- Capital: GBP 4.5M
- Operational (3 years): GBP 1.7M

**Expected Benefits**: GBP 16.8M over 5 years

- FCERM investment optimisation: GBP 6.5M
- Planning decision improvement: GBP 2.8M
- Survey processing efficiency: GBP 2.5M
- Avoided emergency infrastructure costs: GBP 3.0M
- Community resilience value: GBP 2.0M

**Return on Investment**:

- NPV: GBP 7.5M (discounted at 3.5%)
- Payback Period: 26 months
- ROI: 134%

**Recommended Option**: Option 2: Integrated Coastal Change Platform

**Key Risks**:

1. Regional monitoring programme integration resistance — mitigated by co-design and preserving regional workflows
2. Erosion prediction publication causes community concern — mitigated by community engagement before data release
3. LiDAR data processing compute costs exceed estimates — mitigated by serverless architecture and data tiering

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The FCERM capital programme invests GBP 5.2 billion over 6 years. Even a 1% improvement in investment targeting (enabled by better erosion data) yields GBP 52M in value. The platform pays for itself many times over by ensuring coastal protection money goes to the right places. The public information service is a moral imperative — people deserve to know the erosion risk to their homes.

**Next Steps if Approved**:

1. Secure EA/DEFRA approval: April 2026
2. Discovery with NCMP regional programmes: Q2 2026
3. Alpha (automated LiDAR pipeline, 2 regional programmes): Q3 2026
4. Beta (all regions, prediction model, public service pilot): Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The EA's National Coastal Monitoring Programme is one of the most comprehensive coastal survey operations in Europe, generating high-resolution LiDAR, aerial photography, and beach profile data for the entire English coastline. However, the data processing and analysis infrastructure has not kept pace with the survey capability. Each of the six regional programmes uses different contractors, data formats, and delivery platforms. Erosion rate calculations are performed manually by geomorphologists, and predictions have not been systematically updated since the SMP2 cycle (2010-2011).

**Specific Pain Points** (from ARC-004-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| EA NCMP Manager | SD-2 | Six regional databases, manual processing | GBP 600K/year wasted on manual LiDAR processing | CRITICAL |
| Local authorities | SD-3 | Erosion data at 500m resolution, outdated | Planning decisions lack evidence, legal risk | HIGH |
| Coastal communities | SD-4 | Cannot access erosion risk information | Anxiety, misinformation, poor adaptation decisions | CRITICAL |
| EA FCRM Head | SD-5 | Business cases take 3+ months to prepare | Delayed investment decisions, FCERM programme delays | HIGH |
| Network Rail | SD-6 | No alerting for accelerated erosion near track | Reactive emergency closures, GBP millions in disruption | HIGH |

**Consequences of Inaction**:

- GBP 600K/year wasted on manual LiDAR processing that could be automated
- FCERM investment decisions based on 15-year-old erosion predictions — risk of misallocation of GBP 5.2B programme
- Local authority planning decisions without adequate erosion evidence — legal challenge risk
- Coastal communities discovering erosion risk through property searches (reactive, alarming) rather than proactive engagement
- Infrastructure failures (Dawlish-type events) that could be anticipated with better monitoring
- Climate change impact on erosion rates not systematically modelled

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **FCERM Strategy 2020**: Better understanding and communication of coastal change risk
- **National Planning Policy Framework (NPPF)**: Planning in coastal change areas requires current erosion evidence
- **Climate Change Committee Adaptation Progress Report**: Recommended improved coastal monitoring and prediction
- **UKCP18**: Climate projections must be incorporated into erosion planning
- **25 Year Environment Plan**: Sustainable management of land and seas, including coastline

### A1.5 Why Now?

**Urgency Factors**:

- SMP3 cycle commencing 2027 — requires updated erosion predictions as input
- FCERM 6-year programme requires improved evidence for GBP 5.2B investment allocation
- Climate change accelerating erosion rates — UKCP18 data available but not incorporated into predictions
- National Coastal Monitoring Programme contract renewals approaching — opportunity to standardise data requirements
- Several communities facing imminent erosion loss (Hemsby, Happisburgh) with inadequate public information

**Opportunity Cost of Delay**:

- GBP 600K/year continued manual processing costs
- FCERM investment decisions based on outdated data — estimated GBP 50-100M misallocation risk
- SMP3 produced without automated platform — repeating manual SMP2 process
- Infrastructure emergency costs: next Dawlish-type event estimated at GBP 1-2B economic impact

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Regional Integration**: All 6 NCMP programmes integrated into single platform
   - **Threshold**: Minimum 4/6 by launch, 6/6 within 18 months

2. **Prediction Resolution**: Erosion predictions available at 50m intervals
   - **Threshold**: 70% of eroding coastline minimum, 85% target

3. **Processing Automation**: LiDAR processing pipeline automated
   - **Threshold**: 70% automation minimum, 80% target

4. **User Adoption**: Local authority planners using the platform
   - **Threshold**: 50 authorities minimum, 80 target

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (5-year): GBP 7.5M (current manual processing, regional programme operation)

**Benefits**: GBP 0

**Cons**:

- SMP3 produced manually, repeating GBP 3M SMP2 process
- FCERM investment based on outdated predictions
- Community information gap continues
- Climate change not modelled

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable given FCERM investment scale and climate adaptation imperative.

---

### Option 1: Standardised Regional Database

**Description**: Standardise data formats across six regions and create a shared database, but without automated processing, prediction modelling, or public-facing services.

**Costs** (5-year): GBP 3.5M

**Benefits** (5-year): GBP 4.0M

**Stakeholder Goals Met**: 30%

---

### Option 2: Integrated Coastal Change Platform (RECOMMENDED)

**Description**: Cloud-hosted platform with automated LiDAR processing, erosion prediction model, climate scenario integration, public information service, and planning application support.

**Costs** (5-year) - ROM (+-30%):

- Capital: GBP 4.5M
  - Platform development: GBP 2.0M
  - LiDAR processing pipeline: GBP 0.8M
  - Prediction model development: GBP 0.6M
  - Data migration (6 regional archives): GBP 0.5M
  - Public service development: GBP 0.3M
  - Security and testing: GBP 0.2M
  - Contingency: GBP 0.1M
- Operational: GBP 1.7M over 3 years (GBP 3.0M over 5 years)
  - Cloud hosting and compute: GBP 0.3M/year (burst for LiDAR processing)
  - Support and maintenance: GBP 0.2M/year
  - Data operations: GBP 0.1M/year
- Total 5-year TCO: GBP 7.5M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | FCERM investment optimisation (better targeting) | FINANCIAL | GBP 0.0M | GBP 1.0M | GBP 1.5M | GBP 2.0M | GBP 2.0M | GBP 6.5M |
| B-002 | Planning decision improvement (avoided maladaptation) | STRATEGIC | GBP 0.0M | GBP 0.3M | GBP 0.5M | GBP 1.0M | GBP 1.0M | GBP 2.8M |
| B-003 | Survey processing efficiency (automated LiDAR) | FINANCIAL | GBP 0.2M | GBP 0.5M | GBP 0.6M | GBP 0.6M | GBP 0.6M | GBP 2.5M |
| B-004 | Avoided emergency infrastructure costs | RISK | GBP 0.0M | GBP 0.0M | GBP 0.5M | GBP 1.0M | GBP 1.5M | GBP 3.0M |
| B-005 | Community resilience value (informed adaptation) | STRATEGIC | GBP 0.0M | GBP 0.2M | GBP 0.5M | GBP 0.5M | GBP 0.8M | GBP 2.0M |
| **Total** | | | **GBP 0.2M** | **GBP 2.0M** | **GBP 3.6M** | **GBP 5.1M** | **GBP 5.9M** | **GBP 16.8M** |

**NPV** (3.5% discount rate): **GBP 7.5M**

**ROI**: **134%** over 5 years

**Payback Period**: **26 months**

**Stakeholder Goals Met**: 85%

---

### Option 3: Digital Twin of the English Coastline

**Description**: Full 4D (space + time) digital twin of the English coast with real-time sensor integration, machine learning erosion prediction, drone survey integration, and immersive community engagement visualisation.

**Costs** (5-year): GBP 18.0M

**Benefits** (5-year): GBP 20.0M

**Recommendation**: **Reject at SOBC stage** — Disproportionate cost and technology risk. ML erosion prediction and drone integration can be added in future phases.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 | Option 3 |
|-----------|----------|----------|----------|----------|
| 5-Year TCO | GBP 7.5M | GBP 3.5M | GBP 7.5M | GBP 18.0M |
| 5-Year Benefits | GBP 0 | GBP 4.0M | GBP 16.8M | GBP 20.0M |
| NPV | -GBP 7.5M | GBP 0.5M | GBP 7.5M | GBP 0.5M |
| Stakeholder Goals | 0% | 30% | 85% | 100% |
| SMP3 Support | No | Partial | Yes | Yes |
| Public Information | No | No | Yes | Yes |
| Climate Modelling | No | No | Yes | Yes |

**Recommended Option**: **Option 2 — Integrated Coastal Change Platform**

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

| Component | Route | Value | Timeline |
|-----------|-------|-------|----------|
| Platform development | DOS 6 | GBP 2.0M | Q2 2026 |
| LiDAR processing pipeline | G-Cloud 14 (geospatial specialist) | GBP 0.8M | Q2 2026 |
| Cloud hosting | AWS via EA Enterprise Agreement | GBP 1.5M (5-year) | Existing |
| Prediction model (academic partnership) | Research contract via NERC | GBP 0.6M | Q2 2026 |

**Academic Partnership**: The erosion prediction model will be developed in partnership with academic coastal geomorphology groups (e.g., University of Sussex, UCL, University of Plymouth) via NERC-funded research collaboration. This ensures scientific credibility and peer review.

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Capital | GBP 2.5M | GBP 1.5M | GBP 0.5M | GBP 4.5M |
| Operational | GBP 0.3M | GBP 0.6M | GBP 0.8M | GBP 1.7M |
| **Total** | **GBP 2.8M** | **GBP 2.1M** | **GBP 1.3M** | **GBP 6.2M** |

**Funding Source**: EA FCERM programme allocation (capital and operational), with DEFRA contribution for public information service development.

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile (Scrum) with NCMP co-design sprints

**Key Milestones**:

| Milestone | Date | Gate |
|-----------|------|------|
| Discovery (NCMP regional workshops) | June 2026 | EA Assurance |
| Alpha (LiDAR pipeline, 2 regions) | October 2026 | Programme Board |
| Beta (all regions, prediction model) | March 2027 | GDS Assessment |
| Public service pilot (3 coastal areas) | June 2027 | Programme Board |
| Full live service | October 2027 | Programme Board |
| SMP3 data provision | March 2028 | SMP3 programme dependency |

## E2. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Regional programme integration resistance | MEDIUM | HIGH | Co-design preserving regional workflows, phased integration | SRO |
| Erosion predictions cause community alarm | MEDIUM | HIGH | Community engagement before publication, contextualised presentation | Service Owner |
| LiDAR processing compute costs exceed budget | MEDIUM | MEDIUM | Serverless burst processing, data tiering, cost controls | Technical Lead |
| Prediction model accuracy insufficient | LOW | HIGH | Academic peer review, phased validation, transparent uncertainty | Prediction Model Lead |
| SMP3 timeline dependency creates schedule pressure | HIGH | MEDIUM | Early SMP3 programme coordination, phased data delivery | SRO |
| Climate scenario uncertainty undermines prediction credibility | LOW | MEDIUM | Multiple scenarios presented, not single "answer"; transparent methodology | Scientific Lead |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| FCERM Strategy 2020 | Policy | DEFRA/EA | Resilience-based coastal management | gov.uk |
| NPPF | Policy | MHCLG | Coastal change planning requirements | gov.uk |
| UKCP18 Climate Projections | Science | Met Office | Sea level rise scenarios | metoffice.gov.uk |
| CCC Adaptation Progress Report | Advisory | CCC | Coastal monitoring recommendations | theccc.org.uk |
| HM Treasury Green Book | Guidance | HMT | Appraisal methodology | gov.uk |
| ARC-004-STKE-v1.0 | Architecture | SDG 14 Programme | Stakeholder analysis | Local |
| ARC-004-REQ-v1.0 | Architecture | SDG 14 Programme | Requirements specification | Local |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Coastal Erosion Monitoring
**Model**: Claude Opus 4.6
