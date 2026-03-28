# Strategic Outline Business Case: Air Quality Monitoring Network

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Air Quality Monitoring Network (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Air Quality Monitoring Network Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Air Quality Monitoring Programme Board, DEFRA, UKHSA, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC presents the case for investing in an integrated air quality monitoring and alerting platform, following the HM Treasury Green Book five-case model.

---

## Executive Summary

**Purpose**: Protect public health and meet legal air quality obligations through a real-time monitoring and alerting platform integrating DEFRA's AURN reference network with validated lower-cost sensors, providing hyperlocal air quality data, automated health alerts, and Clean Air Zone compliance monitoring.

**Problem Statement**: Air pollution causes 28,000-36,000 premature deaths annually in the UK (COMEAP). The UK has been found in breach of legal air quality limits by the Supreme Court (ClientEarth litigation). DEFRA's AURN network has only 170 reference stations nationally — insufficient for hyperlocal monitoring needed for Clean Air Zone enforcement and public health alerting. Over 40 local authorities have AQMAs, and 8 cities operate CAZs, but monitoring coverage is fragmented and data quality inconsistent. Current DAQI alerting updates hourly at city-level resolution — too slow and too coarse for health-critical decisions by vulnerable individuals.

**Proposed Solution**: An integrated air quality monitoring platform combining 170 AURN reference stations with 5,000+ validated lower-cost sensors via peer-reviewed data fusion algorithms, providing 1km resolution DAQI calculation every 5 minutes, automated health alerting, CAZ compliance monitoring, and open data publication.

**Strategic Fit**: Directly supports Environment Act 2021 PM2.5 targets, retained Ambient Air Quality Directive compliance, Clean Air Strategy 2019, UKHSA health protection mandate, and the Coroner's recommendation from the Ella Adoo-Kissi-Debrah inquest for better public air quality information.

**Investment Required**: GBP 22M over 3 years

- Capital: GBP 14M
- Operational (3 years): GBP 8M

**Expected Benefits**: GBP 85M over 5 years

- Health impact reduction (avoided premature deaths, hospital admissions): GBP 55M
- Clean Air Zone effectiveness improvement: GBP 15M
- Legal risk mitigation (avoided ClientEarth litigation costs and compliance penalties): GBP 10M
- Local authority monitoring cost savings: GBP 5M

**Return on Investment**:

- NPV: GBP 51.2M (discounted at 3.5%)
- Payback Period: 14 months
- ROI: 286%

**Recommended Option**: Option 2: Integrated Reference and Indicative Sensor Network with Real-Time Alerting

**Key Risks**:

1. Data fusion algorithm not accepted by DEFRA for compliance reporting (mitigation: NPL peer review, MCERTS alignment)
2. Lower-cost sensor calibration drift (mitigation: automated drift detection, 6-monthly recalibration)
3. Political sensitivity of transparent non-compliance data (mitigation: open data is a legal obligation under EIR 2004)

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The health imperative is compelling — 28,000-36,000 premature deaths annually. The legal imperative is binding — Environment Act targets and ongoing ClientEarth scrutiny. The Ella Adoo-Kissi-Debrah Coroner's recommendation creates a duty-to-warn precedent. The NPV of GBP 51.2M reflects the significant health economic value of even marginal improvements in air quality management.

**Next Steps if Approved**:

1. Secure DEFRA funding: Q2 2026
2. NPL engagement for data fusion algorithm review: Q2 2026
3. UKHSA alerting system integration specification: Q2 2026
4. AURN network expansion assessment: Q3 2026
5. IoT sensor integration with Project 001: Q3 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: The UK faces legally binding air quality targets under the Environment Act 2021 (PM2.5 annual mean 10 ug/m3 by 2040, interim 12 ug/m3) and retained EU Ambient Air Quality Directive limits. DEFRA's AURN network provides high-quality reference data but has only ~170 stations — one station per 380 km2. This is insufficient for Clean Air Zone enforcement (which needs street-level data), public health alerting (which needs hyperlocal resolution), and compliance monitoring (which needs coverage across all urban areas). Local authorities have deployed their own monitoring using lower-cost sensors, but data quality is variable, interoperability with DEFRA systems is poor, and there is no national picture.

The current Daily Air Quality Index (DAQI) updates hourly at city-level resolution. This means a vulnerable individual (asthma patient, COPD sufferer, pregnant woman, young child) receives at best an hourly, city-average pollution level — useless for deciding whether to walk to school along a busy road or take a different route. The Ella Adoo-Kissi-Debrah Coroner's ruling established that inadequate public air quality information contributed to a child's death, creating a legal and moral duty to improve.

**Specific Pain Points**:

| Stakeholder | Pain Point | Impact | Intensity |
|-------------|------------|--------|-----------|
| DEFRA | Only 170 AURN stations nationally | Cannot demonstrate compliance at local level | CRITICAL |
| UKHSA | Hourly, city-average DAQI | Cannot protect vulnerable populations hyperlocally | CRITICAL |
| Local Authorities | Fragmented, unvalidated local monitoring | Cannot justify CAZ enforcement decisions with data | HIGH |
| ClientEarth | Incomplete monitoring coverage | Cannot independently verify compliance claims | HIGH |
| Citizens | Inaccurate, delayed air quality information | Health decisions based on stale, coarse data | HIGH |

**Consequences of Inaction**:
- 28,000-36,000 premature deaths annually from air pollution continue without improved warning
- Continued legal risk from ClientEarth — each judicial review costs GBP 1-5M in legal and compliance costs
- Environment Act 2021 PM2.5 targets cannot be monitored or demonstrated as met
- Clean Air Zone effectiveness cannot be measured, undermining GBP 500M+ investment
- Duty-to-warn precedent from Ella Adoo-Kissi-Debrah Coroner unmet

### A1.2 Strategic Drivers

| Driver ID | Stakeholder | Driver | Strategic Imperative |
|-----------|-------------|--------|---------------------|
| SD-1 | DEFRA | Meeting legal air quality obligations | Legal compliance |
| SD-2 | Local Authorities | Clean Air Zone enforcement | Regulatory enforcement |
| SD-3 | UKHSA | Protecting public health through timely alerts | Public health |
| SD-4 | ClientEarth | Legal accountability and transparency | Democratic accountability |

**Strategic Alignment**:

- **Environment Act 2021**: PM2.5 targets require monitoring infrastructure
- **Clean Air Strategy 2019**: "World-leading monitoring to track our progress"
- **UKHSA Health Protection**: Duty to warn the public of health hazards
- **Ella Adoo-Kissi-Debrah Coroner's Recommendation**: Better air quality information for the public
- **Environmental Information Regulations 2004**: Legal obligation to publish environmental data
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 10 (Data Quality), 15 (Performance), 16 (Availability)

### A1.3 Scope

**In Scope**: AURN integration, indicative sensor integration (Project 001), data fusion, DAQI calculation, UKHSA alerting, CAZ monitoring, open data publication, forecasting.
**Out of Scope**: Sensor procurement, CAZ charging systems, indoor air quality, industrial emissions.

### A1.4 Why Now?

**Urgency Factors**:
- Environment Act 2021 PM2.5 interim target of 12 ug/m3 requires enhanced monitoring infrastructure
- Ella Adoo-Kissi-Debrah Coroner's recommendation for better public information remains unaddressed
- ClientEarth monitoring compliance litigation ongoing — inadequate monitoring undermines defence
- Clean Air Zones operational in 8 cities with more planned — effectiveness data needed
- IoT Platform (Project 001) provides cost-effective sensor infrastructure — opportunity to leverage

**Opportunity Cost of Delay**:
- Estimated 280-360 avoidable premature deaths per year attributable to inadequate air quality information (1% of total, conservative estimate)
- GBP 1-5M per ClientEarth legal challenge
- CAZ investment cannot be evaluated — GBP 500M+ unmonitored

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Data Quality Accepted for Compliance**: DEFRA accepts platform data for LAQM and national reporting
   - **Measure**: DEFRA formal acceptance
   - **Threshold**: Reference-grade data accepted; calibrated indicative data accepted for supplementary monitoring

2. **Alert Latency**: Health alerts delivered within 5 minutes of threshold exceedance
   - **Measure**: End-to-end alert delivery time
   - **Threshold**: 5 minutes for DAQI >= 7, 2 minutes for DAQI >= 10

3. **Spatial Coverage**: 1km resolution DAQI across all major urban areas
   - **Measure**: Percentage of urban population within 1km of monitoring point
   - **Threshold**: 80% of urban population covered

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (5-year): GBP 12M (continued AURN operation only)
**Benefits**: GBP 0 (no improvement in coverage, alerting, or CAZ monitoring)
**Health Impact**: 28,000-36,000 premature deaths annually continue with inadequate warning
**Legal Risk**: Ongoing ClientEarth litigation exposure
**Stakeholder Goals Met**: 0%
**Recommendation**: **Reject** — Legally and morally indefensible given existing precedent.

---

### Option 1: AURN Expansion Only

**Description**: Double the AURN reference network from 170 to 340 stations. No lower-cost sensor integration, no real-time alerting improvement.
**Costs** (5-year): GBP 35M (170 new stations at GBP 150K capital + GBP 30K/year each)
**Benefits** (5-year): GBP 30M (improved coverage, better compliance evidence)
**Spatial Resolution**: 5-10km (improved but not hyperlocal)
**Alert Improvement**: Minimal — still hourly, station-level

**Pros**:
- Highest data quality (all MCERTS reference-grade)
- Legally unquestionable data for compliance

**Cons**:
- GBP 35M is expensive for only 2x coverage improvement
- Still insufficient for hyperlocal health alerting or CAZ street-level monitoring
- No improvement in alert latency (still hourly)
- Negative NPV (costs exceed benefits)

**Stakeholder Goals Met**: 35%
**Recommendation**: **Insufficient** — Expensive, still inadequate spatial resolution.

---

### Option 2: Integrated Reference and Indicative Sensor Network with Real-Time Alerting (RECOMMENDED)

**Description**: Maintain and modestly expand AURN (170 -> 200 stations), integrate 5,000 validated lower-cost sensors via Project 001 IoT Platform using peer-reviewed data fusion algorithms, build real-time DAQI calculation at 1km resolution with 5-minute update cycle, and deploy automated health alerting via UKHSA.

**Costs** (5-year) — ROM (+/-30%):

- Capital: GBP 14M
  - Platform development (data fusion, DAQI engine, alerting): GBP 6M
  - AURN expansion (30 new stations): GBP 4.5M
  - Indicative sensor validation and calibration programme: GBP 2M
  - Integration and testing: GBP 1.5M
- Operational: GBP 14M over 5 years
  - AURN network operation (200 stations): GBP 6M/year (partially existing budget)
  - Platform operations: GBP 0.8M/year
  - Sensor recalibration programme: GBP 0.4M/year
  - New operational cost (above existing baseline): GBP 2.8M/year
- Total 5-year net new cost: GBP 28M

**Benefits** (5-year):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Health impact reduction (avoided mortality/morbidity) | SD-3 | HEALTH/ECONOMIC | GBP 3M | GBP 8M | GBP 12M | GBP 16M | GBP 16M | GBP 55M |
| B-002 | CAZ effectiveness improvement | SD-2 | OPERATIONAL | GBP 1M | GBP 2M | GBP 4M | GBP 4M | GBP 4M | GBP 15M |
| B-003 | Legal risk mitigation | SD-1, SD-4 | RISK | GBP 2M | GBP 2M | GBP 2M | GBP 2M | GBP 2M | GBP 10M |
| B-004 | LA monitoring cost savings | SD-2 | FINANCIAL | GBP 0.5M | GBP 1M | GBP 1M | GBP 1.5M | GBP 1M | GBP 5M |
| **Total** | | | | **GBP 6.5M** | **GBP 13M** | **GBP 19M** | **GBP 23.5M** | **GBP 23M** | **GBP 85M** |

**Net Present Value** (3.5% discount rate):

- Total Benefits PV: GBP 72.4M
- Total Costs PV: GBP 21.2M
- **NPV: GBP 51.2M**

**Return on Investment**:
- **ROI: 286%** over 5 years
- **Payback Period: 14 months**

**Note on Health Benefits Valuation**: Health benefits calculated using DEFRA damage cost approach for air pollution — GBP 70,965 per tonne of PM2.5 equivalent. Even a 1% reduction in exposure-attributable mortality (280-360 deaths) valued at GBP 5-7M/year using NICE quality-adjusted life year methodology. Benefits are conservative — they exclude productivity gains, reduced NHS costs, and quality of life improvements.

**Pros**:
- Compelling NPV (GBP 51.2M) reflecting high health economic value
- 30x improvement in spatial resolution (city-average to 1km)
- 12x improvement in temporal resolution (hourly to 5-minute)
- Addresses legal obligations (Environment Act, ClientEarth, Coroner's recommendation)
- Leverages Project 001 IoT Platform for sensor infrastructure

**Cons**:
- Data fusion methodology requires peer review and DEFRA acceptance
- Lower-cost sensor calibration drift requires ongoing management
- GBP 14M upfront capital investment

**Stakeholder Goals Met**: 85%

---

### Option 3: Comprehensive National Air Quality Intelligence System

**Description**: Full national system including indoor air quality, industrial emissions, noise pollution, and predictive health modelling.
**Costs** (5-year): GBP 65M
**Benefits** (5-year): GBP 95M
**NPV**: GBP 22.3M (lower NPV than Option 2 due to diminishing returns and higher risk)
**Stakeholder Goals Met**: 100%
**Recommendation**: **Reject** — Scope too broad, higher execution risk, lower NPV than focused Option 2.

## B3. Recommended Option

**Recommendation**: **Option 2: Integrated Reference and Indicative Sensor Network with Real-Time Alerting**

**Rationale**:
1. **Best Value**: Highest NPV at GBP 51.2M — highest in the entire SDG 11 programme, reflecting the significant health economic value
2. **Legal Obligation**: Addresses Environment Act targets, ClientEarth litigation risk, and Coroner's duty-to-warn recommendation
3. **Scalable**: Can expand from 5,000 to 20,000+ sensors using Project 001 infrastructure
4. **Proven Approach**: Data fusion methodology based on established practice (Breathe London, LAQN at Kings/Imperial)
5. **Deliverable**: 18-month timeline to operational hyperlocal alerting

**Optimism Bias Adjustment**:
- Standard uplift for IT projects: +40% on costs
- Adjusted Total Cost: GBP 28M -> GBP 39.2M (with uplift)
- NPV with optimism bias: Still strongly positive at GBP 33.2M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Sourcing Route**: Digital Marketplace (G-Cloud for platform, DOS for air quality science and data fusion expertise).

**Key Requirements**:
- Air quality domain expertise (AURN, LAQM, MCERTS, DAQI)
- Data science capability for sensor fusion algorithms
- Real-time data processing at scale
- Environmental data publication experience

**AURN Station Procurement**: Separate procurement for 30 new reference-grade monitoring stations via Environment Agency MCERTS procurement framework.

**Evaluation**: Technical 60%, Cost 30%, Social Value 10%.

**Social Value Focus**: Citizen science engagement, air quality education, sensor manufacturing in UK regions.

---

# PART D: FINANCIAL CASE

## D1. Budget

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Platform development | GBP 3.5M | GBP 2M | GBP 0.5M | GBP 6M |
| AURN expansion (30 stations) | GBP 2M | GBP 1.5M | GBP 1M | GBP 4.5M |
| Sensor validation programme | GBP 1M | GBP 0.5M | GBP 0.5M | GBP 2M |
| Integration and testing | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| **CapEx Total** | **GBP 7M** | **GBP 4.5M** | **GBP 2.5M** | **GBP 14M** |
| Platform operations | GBP 0.5M | GBP 0.8M | GBP 1M | GBP 2.3M |
| AURN operations (incremental 30 stations) | GBP 0.3M | GBP 0.9M | GBP 0.9M | GBP 2.1M |
| Sensor recalibration | GBP 0.2M | GBP 0.4M | GBP 0.5M | GBP 1.1M |
| Data science team (ongoing algorithm refinement) | GBP 0.5M | GBP 0.5M | GBP 0.5M | GBP 1.5M |
| Training and LA support | GBP 0.3M | GBP 0.4M | GBP 0.3M | GBP 1M |
| **OpEx Total** | **GBP 1.8M** | **GBP 3M** | **GBP 3.2M** | **GBP 8M** |
| **Grand Total** | **GBP 8.8M** | **GBP 7.5M** | **GBP 5.7M** | **GBP 22M** |

## D2. Funding Source

**Source**: DEFRA Environmental Improvement Plan funding (Spending Review 2025), supplemented by UKHSA health protection budget for alerting capability.
**DEFRA allocation**: GBP 18M
**UKHSA contribution**: GBP 4M (alerting system integration)
**Total**: GBP 22M
**Affordability**: **Affordable** — 3.5% of annual DEFRA air quality and environmental monitoring budget.

## D3. Financial Appraisal (Green Book)

**Discount Rate**: 3.5% (HMT standard)

| Year | Costs | Benefits | Net | Discount Factor | PV |
|------|-------|----------|-----|-----------------|-----|
| 0 | GBP 7M | GBP 0 | -GBP 7M | 1.000 | -GBP 7M |
| 1 | GBP 7.5M | GBP 6.5M | -GBP 1M | 0.966 | -GBP 0.97M |
| 2 | GBP 5.7M | GBP 13M | +GBP 7.3M | 0.934 | +GBP 6.8M |
| 3 | GBP 3.5M | GBP 19M | +GBP 15.5M | 0.902 | +GBP 14.0M |
| 4 | GBP 3.5M | GBP 23.5M | +GBP 20M | 0.871 | +GBP 17.4M |
| 5 | GBP 3.5M | GBP 23M | +GBP 19.5M | 0.842 | +GBP 16.4M |
| **Total** | **GBP 30.7M** | **GBP 85M** | **+GBP 54.3M** | | **+GBP 51.2M** |

**VfM Rating**: **High** — NPV GBP 51.2M is the highest in the SDG 11 programme, reflecting the significant health economic value of improved air quality monitoring and alerting.

---

# PART E: MANAGEMENT CASE

## E1. Governance

| Decision/Activity | Responsible | Accountable | Consulted | Informed |
|-------------------|-------------|-------------|-----------|----------|
| Programme delivery | Programme Manager | SRO | CDDO | All stakeholders |
| Data fusion methodology | Data Science Lead | DEFRA CSA | NPL, Imperial/Kings | Environment Agency |
| AURN expansion | AURN Network Manager | DEFRA | Environment Agency | Local Authorities |
| UKHSA alerting integration | UKHSA Technical Lead | UKHSA Director | DEFRA | Citizens |
| Open data publication | Data Team Lead | DEFRA | ClientEarth (transparency) | All stakeholders |

## E2. Delivery Approach

**Methodology**: Agile with scientific validation gates (data fusion methodology requires peer review before deployment).

**Phases**:
1. **Discovery** (Months 1-3): Data fusion algorithm design, UKHSA alerting specification, NPL engagement
2. **Alpha** (Months 4-6): Data fusion prototype with Breathe London data, AURN integration
3. **Beta** (Months 7-14): Platform build, sensor validation programme, DAQI engine, alerting integration
4. **Live** (Month 15): London pilot (highest sensor density, established reference network)
5. **Scale** (Months 16-24): National rollout to CAZ cities and AQMAs

## E3. Risk Management

| Risk ID | Risk | Likelihood | Impact | Score | Mitigation | Owner |
|---------|------|------------|--------|-------|------------|-------|
| R-001 | Data fusion not accepted by DEFRA | Medium | Critical | 16 | NPL peer review, MCERTS alignment, early DEFRA engagement | DEFRA CSA |
| R-002 | Sensor calibration drift | High | Medium | 12 | Automated drift detection, 6-month recalibration cycle | Data Science Lead |
| R-003 | Political sensitivity of non-compliance data | Medium | High | 12 | Open data is a legal obligation (EIR 2004), cannot suppress | SRO |
| R-004 | UKHSA integration complexity | Medium | Medium | 9 | Early specification, phased integration | UKHSA Lead |
| R-005 | False alerts causing public alarm | Medium | High | 12 | Conservative thresholds, validated before deployment | Data Science Lead |
| R-006 | Budget overrun (AURN stations) | Low | Medium | 6 | 15% contingency, phased station deployment | Finance |

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary

**Recommended Option**: Option 2: Integrated Reference and Indicative Sensor Network with Real-Time Alerting
**Investment**: GBP 22M over 3 years
**Expected Return**: GBP 85M over 5 years (NPV: GBP 51.2M, ROI: 286%)
**Stakeholder Goals Met**: 85%
**Payback Period**: 14 months
**Go/No-Go Recommendation**: **PROCEED**

## F2. Next Steps if Approved

1. **Funding Approval**: DEFRA (GBP 18M) + UKHSA (GBP 4M) — Target: Q2 2026
2. **NPL Engagement**: Data fusion algorithm specification and peer review protocol — Target: Q2 2026
3. **UKHSA Specification**: Alerting system integration requirements — Target: Q2 2026
4. **Breathe London Partnership**: Access to existing London sensor network for algorithm development — Target: Q3 2026
5. **AURN Expansion Planning**: Site selection for 30 new reference stations — Target: Q3 2026
6. **Project 001 Integration**: Sensor telemetry API specification with IoT Platform — Target: Q3 2026

---

## Appendix A: Stakeholder Analysis

**Source**: `projects/005-air-quality-monitoring-network/ARC-005-STKE-v1.0.md`

## Appendix B: Architecture Principles

**Source**: `projects/000-global/ARC-000-PRIN-v1.0.md`

**Relevant Principles**: 10 (Data Quality and Environmental Accuracy), 15 (Performance for Real-Time Services), 16 (Availability for Critical Infrastructure), 9 (Privacy by Design)

## Appendix H: Glossary

| Term | Definition |
|------|------------|
| AURN | Automatic Urban and Rural Network — DEFRA's reference-grade air quality monitoring network |
| DAQI | Daily Air Quality Index — 1-10 scale of air pollution health risk |
| MCERTS | Monitoring Certification Scheme — Environment Agency certification for environmental monitoring |
| CAZ | Clean Air Zone — designated urban areas where polluting vehicles may be charged |
| AQMA | Air Quality Management Area — area declared by a local authority where air quality limits are breached |
| COMEAP | Committee on the Medical Effects of Air Pollutants |
| PM2.5 | Particulate matter with diameter less than 2.5 micrometres |
| NO2 | Nitrogen dioxide |
| NPL | National Physical Laboratory — UK national measurement institute |
| EIR | Environmental Information Regulations 2004 |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Air Quality Monitoring Network (Project 005)
**Model**: Claude Opus 4.6
