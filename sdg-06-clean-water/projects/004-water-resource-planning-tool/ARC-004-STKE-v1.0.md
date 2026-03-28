# Stakeholder Drivers & Goals Analysis: Water Resource Planning Tool

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Water Resource Planning Tool (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Water Resource Planning Tool Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA, Environment Agency, Ofwat, Water Companies, Natural England |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Water Resource Planning Tool, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. Water resource planning operates on multi-decadal timescales — balancing future water demand against available supply under climate change uncertainty.

### Key Findings

The Water Resource Planning Tool sits at the intersection of long-term environmental planning, water company investment, and climate adaptation. The dominant tension is between water companies' desire for planning certainty (to justify investment to investors and Ofwat) and the inherent uncertainty of climate projections over 25-50 year horizons. A secondary tension exists between abstraction for public water supply and environmental flow requirements — taking water from rivers for homes means less water for ecosystems. The 2022 drought and subsequent hosepipe bans demonstrated that water resource planning failures have immediate public and political consequences.

### Critical Success Factors

- Integrate UKCP18 climate projections with regional water resource models at catchment scale
- Enable consistent supply-demand balance modelling across all 5 regional water resource groups
- Provide scenario planning capability covering 25-50 year horizons with quantified uncertainty
- Link water resource planning to Environmental Flow Indicators for abstraction sustainability
- Support the National Framework for Water Resources regional planning process

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong alignment on the need for better water resource planning tools, particularly after the 2022 drought. Tensions exist between environmental protection (reducing abstraction) and water supply security (maintaining headroom), and between national consistency (DEFRA/EA) and regional flexibility (water companies).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Water Resources Policy Director | Policy sponsorship | HIGH | HIGH | Manage Closely — Programme board |
| DEFRA Chief Scientific Adviser | Scientific methodology | HIGH | MEDIUM | Keep Satisfied — Methodology review |
| DEFRA Chief Digital Information Officer | Technical leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| DEFRA Climate Adaptation Team | Climate scenarios | MEDIUM | HIGH | Keep Informed — UKCP18 integration |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| EA Water Resources Director | Environment Agency | Co-regulator, abstraction licensing | HIGH | HIGH |
| EA National Water Resources Planner | Environment Agency | Technical lead | HIGH | HIGH |
| Ofwat Director of Strategy | Ofwat | Price review, investment approval | HIGH | HIGH |
| Water Companies (water resource planning teams) | Industry | Plan producers | HIGH | HIGH |
| Regional Water Resource Groups (x5) | Cross-company groups | Regional coordination | MEDIUM | HIGH |
| Natural England | Natural England | Protected site water needs | MEDIUM | HIGH |
| Met Office Hadley Centre | Met Office | Climate projection data | MEDIUM | MEDIUM |
| UK Centre for Ecology & Hydrology | UKCEH | Hydrological modelling science | MEDIUM | MEDIUM |
| Consumer Council for Water (CCW) | Consumer body | Customer impact | MEDIUM | MEDIUM |
| HM Treasury | HM Treasury | Funding | HIGH | LOW |
| General public | Citizens | Water supply reliability | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * DEFRA Water      |
        |  * DEFRA Chief Sci  |    Resources Policy  |
        |    Adviser          |  * DEFRA CDIO       |
        |                     |  * EA Water Res Dir |
 P      |                     |  * Ofwat Dir of     |
 O      |                     |    Strategy          |
 W      |                     |  * Water Companies  |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Regional Water   |
        |                     |    Resource Groups   |
        |                     |  * Natural England  |
        |                     |  * Met Office Hadley|
        |                     |  * UKCEH            |
        |                     |  * CCW              |
        |                     |  * DEFRA Climate    |
        |                     |    Adaptation Team   |
        |                     |  * General public   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA — National Water Security Under Climate Change

**Stakeholder**: DEFRA Water Resources Policy Director

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Ensure long-term national water security by providing DEFRA with the analytical capability to assess supply-demand balance across England under climate change scenarios, supporting the National Framework for Water Resources and informing the next round of Water Resource Management Plans (WRMP29).

**Context & Background**:
England faces a projected supply-demand deficit of 4 billion litres per day by 2050 under central climate projections. The 2022 drought demonstrated vulnerability — 8 water companies imposed temporary use bans (hosepipe bans), affecting 33 million customers. DEFRA's National Framework for Water Resources (2020) identified the need for regional coordination and strategic infrastructure (inter-regional transfers, new reservoirs, desalination). WRMP29, due 2029, will set water company investment plans for 2030-2060. DEFRA needs a common analytical platform to assess the national picture rather than relying on 17 separate water company submissions with inconsistent methodologies.

**Driver Intensity**: CRITICAL

**Enablers**:
- Common modelling platform for all water companies and regional groups
- UKCP18 climate projection integration at catchment scale
- Supply-demand balance scenarios with quantified uncertainty
- National-level aggregation of regional water resource plans

**Blockers**:
- Water company proprietary models and reluctance to share underlying data
- Scientific uncertainty in long-term climate projections (50+ year horizons)
- Political sensitivity of infrastructure decisions (new reservoirs, transfers)

---

### SD-2: Environment Agency — Sustainable Abstraction

**Stakeholder**: EA Water Resources Director

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Ensure that water resource planning maintains environmental flows in rivers and aquifers, delivering the EA's statutory duty to protect water resources for the environment under the Water Resources Act 1991 and Environment Act 2021.

**Context & Background**:
The EA's Environmental Flow Indicator (EFI) programme has identified that approximately 28% of surface water bodies in England have unsustainable abstraction levels. Climate change will increase pressure on water resources while simultaneously increasing environmental flow requirements (warmer water needs more flow for aquatic ecosystems). The EA needs the planning tool to integrate abstraction sustainability assessments into water resource planning, ensuring new supply options do not create or worsen unsustainable abstraction.

**Driver Intensity**: HIGH

---

### SD-3: Water Companies — Investment Certainty for Long-Term Planning

**Stakeholder**: Water companies (water resource planning teams)

**Driver Category**: FINANCIAL / OPERATIONAL

**Driver Statement**: Obtain robust, defensible supply-demand balance evidence that supports water resource investment cases through Ofwat's price review process, providing the certainty that investors and customers require.

**Context & Background**:
Water companies need to invest billions in new water supply infrastructure — South East Strategic Reservoir (est. GBP 2.2B), Thames-to-Affinity transfer (est. GBP 800M), desalination plants, water recycling. These investments are funded through customer bills and must be approved by Ofwat. Companies need robust supply-demand balance evidence to justify investment. Underinvestment risks supply failure; overinvestment burdens customers with unnecessary costs.

**Driver Intensity**: HIGH

---

### SD-4: Natural England — Protected Site Water Needs

**Stakeholder**: Natural England

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Ensure that water resource planning protects Sites of Special Scientific Interest (SSSIs), Special Areas of Conservation (SACs), and other protected sites from the impacts of water abstraction and drought.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Common Water Resource Modelling Platform

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: DEFRA Water Resources Policy Director

**Goal Statement**: Deliver a common water resource modelling platform used by all 17 water companies and 5 regional groups for WRMP29 preparation, with consistent climate scenarios, demand forecasting, and supply assessment methodology, operational by Q1 2028.

**Success Metrics**:
- **Primary Metric**: Water companies using the common platform for WRMP29 (target: 17/17)
- **Secondary Metrics**:
  - Methodology consistency score (target: 100% use common climate scenarios)
  - Regional plan integration (target: 5/5 regional groups producing coordinated plans)

---

### Goal G-2: Climate-Integrated Supply-Demand Scenarios

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: DEFRA Climate Adaptation Team

**Goal Statement**: Integrate UKCP18 probabilistic climate projections into water resource supply-demand modelling at catchment scale, producing scenario analyses spanning 2030-2085 with quantified uncertainty bands, by Q3 2027.

**Success Metrics**:
- **Primary Metric**: Climate scenarios available (target: RCP2.6, RCP4.5, RCP6.0, RCP8.5 at catchment scale)
- **Secondary Metrics**:
  - Uncertainty quantification (target: 10th, 50th, 90th percentile projections for all scenarios)
  - Spatial resolution (target: individual Water Resource Zone level)

---

### Goal G-3: Environmental Flow Integration

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: EA Water Resources Director

**Goal Statement**: Integrate Environmental Flow Indicators and protected site water needs into the water resource planning tool, enabling supply options to be automatically assessed against environmental constraints, by Q4 2027.

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Water companies (SD-3) want conservative (pessimistic) demand forecasts to justify investment. Ofwat wants realistic forecasts to avoid unnecessary customer bill increases.
  - **Resolution Strategy**: Transparent methodology with published scenario assumptions. Present a range of scenarios (low, central, high demand) rather than single point estimates. Ofwat determines which scenario to use for price review.

- **Conflict 2**: EA/Natural England (SD-2, SD-4) want environmental flow constraints that may reduce available supply. Water companies (SD-3) want maximum flexibility to abstract.
  - **Resolution Strategy**: Environmental constraints treated as non-negotiable planning parameters (consistent with Architecture Principle 20 — WFD compliance). Companies must plan around environmental limits.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| National Framework for Water Resources | Strategy | GOV.UK | Regional planning framework | N/A — external reference |
| Water Resources Act 1991 | Legislation | legislation.gov.uk | Abstraction licensing powers | N/A — external reference |
| UKCP18 Climate Projections | Scientific data | Met Office | Probabilistic climate scenarios | N/A — external reference |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | SDG 6 governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Water Resource Planning Tool (Project 004)
**AI Model**: Claude Opus 4.6 (1M context)
