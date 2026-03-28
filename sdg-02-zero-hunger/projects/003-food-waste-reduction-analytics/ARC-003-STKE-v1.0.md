# Stakeholder Drivers & Goals Analysis: Food Waste Reduction Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Food Waste Reduction Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DEFRA Resources and Waste Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, WRAP, Environment Agency, Cabinet Office Food Strategy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Food Waste Reduction Analytics platform, a data system tracking food waste volumes and composition across the UK supply chain -- from farm gate through manufacturing, retail, hospitality, and household. The platform will measure progress against the UK's commitment to halve food waste by 2030 (SDG 12.3) and support the Courtauld Commitment 2030 and Resources and Waste Strategy.

### Key Findings

Strong alignment exists between DEFRA's policy mandate, WRAP's operational role in waste reduction, and the food industry's desire to benchmark performance. The primary tension is between the government's need for granular, comparable waste data and the food industry's reluctance to disclose waste volumes that could be commercially embarrassing or used punitively. The Environment Agency's regulatory interest in waste reporting creates both an enforcement mechanism and an industry trust barrier.

### Critical Success Factors

- Establishing a trusted data reporting framework that industry participants adopt voluntarily
- Integrating with WRAP's existing Courtauld Commitment reporting infrastructure
- Delivering comparable waste metrics across heterogeneous measurement methodologies
- Demonstrating value to industry through benchmarking and insight, not just compliance reporting

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Government and WRAP share strong alignment. Industry participation is conditional on data confidentiality and perceived mutual benefit. The Environment Agency's regulatory posture creates tension with voluntary participation goals.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-1: DEFRA Minister for Environment | Minister | HIGH | HIGH | Ministerial briefings |
| S-2: DEFRA Director of Resources and Waste | Programme Sponsor | HIGH | HIGH | Programme board |
| S-3: SRO, Food Waste Programme | Senior Responsible Owner | HIGH | HIGH | Weekly programme board |
| S-4: DEFRA Chief Digital Officer | Digital Strategy Lead | HIGH | HIGH | Architecture reviews |
| S-5: DEFRA Resources and Waste Policy Team | Policy Analysts | MEDIUM | HIGH | Sprint reviews |
| S-6: DEFRA SIRO | Information Risk Owner | HIGH | MEDIUM | Data governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-7: WRAP (Waste & Resources Action Programme) | Delivery partner | Data partner, Courtauld host | HIGH | HIGH |
| S-8: Environment Agency | Regulator | Waste regulation and reporting | HIGH | MEDIUM |
| S-9: Food and Drink Federation (FDF) | Industry body | Manufacturing sector representative | MEDIUM | HIGH |
| S-10: British Retail Consortium (BRC) | Industry body | Retail sector representative | MEDIUM | HIGH |
| S-11: UKHospitality | Industry body | Hospitality sector representative | LOW | HIGH |
| S-12: Local Authorities (waste collection) | Service delivery | Household waste data providers | MEDIUM | MEDIUM |
| S-13: Cabinet Office (Project 005) | Cross-govt dashboard | Data consumer | MEDIUM | MEDIUM |
| S-14: CDDO | Spend control / assurance | HIGH | MEDIUM |
| S-15: Food manufacturers (Courtauld signatories) | Industry | Data providers | MEDIUM | MEDIUM |
| S-16: ONS | Statistics | Methodology partner | LOW | MEDIUM |

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Minister -- SDG 12.3 Target Achievement

**Stakeholder**: S-1 DEFRA Minister for Environment

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Demonstrate measurable progress towards the UK commitment to halve per capita food waste by 2030 (SDG 12.3 target), with credible, internationally comparable data to report at UN reviews.

**Context & Background**: The UK committed to SDG 12.3 at the UN General Assembly and reports progress through the Voluntary National Review. Current measurement relies on WRAP's estimates with significant methodological uncertainties. The Minister needs a robust data platform to credibly claim progress or explain shortfalls.

**Driver Intensity**: CRITICAL

**Enablers**:
- Granular, verifiable waste data from across the supply chain
- Internationally comparable measurement methodology (aligned with FAO Food Loss Index)
- Year-on-year trend tracking with statistical confidence

**Blockers**:
- Industry reluctance to report waste data transparently
- Methodological fragmentation across supply chain stages
- Political sensitivity of publishing waste data that shows insufficient progress

---

### SD-2: WRAP -- Courtauld Commitment Delivery

**Stakeholder**: S-7 WRAP

**Driver Category**: OPERATIONAL

**Driver Statement**: Enhance the data infrastructure supporting the Courtauld Commitment 2030, enabling WRAP to track signatory progress, provide benchmarking insights, and report aggregate achievements. Replace the current labour-intensive manual reporting with automated data collection.

**Context & Background**: WRAP manages the Courtauld Commitment 2030 with approximately 200 signatories across the food supply chain. Current reporting is annual, manual (spreadsheet submissions), and delayed by 12-18 months. WRAP needs near-real-time data to provide timely interventions and demonstrate Courtauld value to signatories considering renewal.

**Driver Intensity**: HIGH

**Enablers**:
- Automated data collection from signatories
- Benchmarking tools showing individual vs sector performance
- Integration with WRAP's existing Food Waste Atlas

**Blockers**:
- Signatory fatigue with data reporting requirements
- Varying data quality and measurement methodologies across signatories
- WRAP's limited technical capacity for platform development

---

### SD-3: Food Industry -- Competitive Benchmarking

**Stakeholder**: S-9 (FDF), S-10 (BRC), S-15 (Manufacturers)

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Participate in waste reporting only if commercially sensitive waste data is protected and the platform provides meaningful benchmarking insights that help reduce costs. Waste reduction is a cost-saving opportunity if supported by comparable data.

**Context & Background**: Food manufacturers and retailers have invested significantly in waste reduction (WRAP estimates £1.3B annual savings from Courtauld). However, absolute waste volumes are commercially sensitive -- a company reporting high waste could face media and investor scrutiny. Industry needs anonymised benchmarking showing their performance relative to sector averages without revealing individual company data.

**Driver Intensity**: MEDIUM

**Enablers**:
- Anonymised benchmarking with sector-level comparison
- Commercial confidentiality protections (FOI exemptions for company-level data)
- Actionable insights (hotspot analysis, best practice recommendations)
- Industry-governed data sharing framework

**Blockers**:
- Fear of regulatory use of voluntarily provided data
- Inconsistent measurement methodologies between companies
- Cost of implementing data feeds

---

### SD-4: Environment Agency -- Regulatory Intelligence

**Stakeholder**: S-8 Environment Agency

**Driver Category**: COMPLIANCE

**Driver Statement**: Gain improved visibility of food waste volumes at regulated sites (manufacturers, processors, large retailers with environmental permits) to support waste hierarchy enforcement and identify compliance risks.

**Context & Background**: The Environment Agency regulates waste under the Environmental Permitting Regulations and the waste hierarchy (prevention, reuse, recycling, recovery, disposal). Food waste sent to landfill is a priority target. The EA needs data to identify sites where waste prevention and redistribution opportunities are being missed.

**Driver Intensity**: MEDIUM

**Enablers**:
- Integration with EA waste returns and permit data
- Waste hierarchy compliance indicators
- Site-level waste composition data

**Blockers**:
- Industry resistance to sharing data that could trigger enforcement
- Legal boundaries between voluntary reporting and regulatory data
- Different data classification requirements between DEFRA and EA

---

## Driver-to-Goal Mapping

### Goal G-1: Measure National Food Waste Baseline

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: S-3 SRO

**Goal Statement**: Establish a statistically robust national food waste baseline covering all supply chain stages (farm gate, manufacturing, retail, hospitality, household) with annual updates, by Q4 2027.

**Success Metrics**:
- **Primary Metric**: Percentage of food waste (by weight and value) measured with confidence interval < +/-10%
- **Secondary Metrics**: Number of supply chain stages with data coverage, number of active data providers

**Baseline**: WRAP estimates with +/-25% confidence, 18-month reporting lag

**Target**: Comprehensive measurement with +/-10% confidence, < 6-month reporting lag

---

### Goal G-2: Enable Industry Benchmarking

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: S-7 WRAP

**Goal Statement**: Provide anonymised waste benchmarking to all Courtauld Commitment signatories, enabling individual companies to compare their waste intensity against sector quartiles, by Q2 2028.

**Success Metrics**:
- **Primary Metric**: Number of signatories actively using benchmarking tools
- **Secondary Metrics**: User satisfaction score, reported waste reduction actions taken

---

### Goal G-3: Publish Food Waste Metrics for National Dashboard

**Derived From Drivers**: SD-1

**Goal Owner**: S-4 CDO

**Goal Statement**: Publish food waste metrics via API for the National Food Strategy Dashboard (Project 005) with quarterly data refresh by Q3 2028.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Minister | SD-1 | SDG 12.3 progress | G-1 | National baseline | O-1 | Credible UN reporting |
| WRAP | SD-2 | Courtauld delivery | G-1, G-2 | Baseline + benchmarking | O-2 | 200 signatories tracking |
| Industry | SD-3 | Competitive benchmarking | G-2 | Industry benchmarking | O-3 | Cost savings from insights |
| EA | SD-4 | Regulatory intelligence | G-1 | National baseline | O-4 | Compliance visibility |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Government transparency (SD-1) vs industry confidentiality (SD-3). Publishing national waste figures requires industry data, but companies resist disclosing waste volumes.
  - **Resolution Strategy**: Publish only aggregated, anonymised data at sector level. Individual company data never disclosed. Data sharing agreement with explicit FOI protections.

- **Conflict 2**: Environment Agency enforcement use (SD-4) vs voluntary participation (SD-3). If industry fears data will be used for enforcement, voluntary reporting collapses.
  - **Resolution Strategy**: Legal firewall between voluntary Courtauld data and EA regulatory data. EA can access only data already required under environmental permits, not voluntarily reported data.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Resources and Waste Strategy 2018 | Policy | DEFRA | Food waste reduction targets, waste hierarchy | gov.uk |
| Courtauld Commitment 2030 | Agreement | WRAP | Industry waste reduction targets | wrap.org.uk |
| SDG 12.3 | International target | UN | Halve per capita food waste by 2030 | un.org |
| ARC-000-PRIN-v1.0 | Principles | SDG 2 | Governing architecture principles | ARC-000-PRIN-v1.0.md |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Food Waste Reduction Analytics
**Model**: Claude Opus 4.6
