# Stakeholder Drivers & Goals Analysis: Pandemic Preparedness System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Pandemic Preparedness System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Pandemic Preparedness Programme, UKHSA |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Pandemic Preparedness Programme Board, UKHSA Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Pandemic Preparedness System — a disease surveillance and early warning platform operated by the UK Health Security Agency (UKHSA) — their drivers, goals, and measurable outcomes.

### Key Findings

The Pandemic Preparedness System is driven by the lessons of COVID-19, where fragmented surveillance systems, manual data processing, and legacy infrastructure delayed the UK's ability to detect, characterise, and respond to a novel pathogen. The strongest alignment exists around building real-time surveillance capability and automated early warning. The most significant conflict is between national security classification requirements (intelligence agencies wanting restricted data sharing) and public health transparency (WHO obligations and public trust demanding open data).

### Critical Success Factors

- Achieve detection of novel pathogen signals within 24 hours of surveillance data availability (vs. weeks during early COVID-19)
- Integrate laboratory, hospital, primary care, wastewater, and genomic surveillance data into a single operational picture
- Scale from routine monitoring (tens of thousands of data points daily) to pandemic response (millions) within 48 hours
- Interoperate with WHO International Health Regulations (IHR) reporting and Five Eyes health security partners
- Maintain operational capability during peacetime to avoid the "build it and they won't maintain it" failure mode

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Strong cross-government consensus on the need for pandemic preparedness following the COVID-19 Inquiry findings. Primary tension is between security classification (COBR/intelligence community) and open data principles (WHO/public health community).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| UKHSA Chief Executive | Agency head | HIGH | HIGH | Manage Closely — Strategic direction |
| SRO, Pandemic Preparedness | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| UKHSA Chief Data and Surveillance Officer | Surveillance strategy | HIGH | HIGH | Manage Closely — Data architecture, analytics |
| UKHSA Chief Medical Adviser | Clinical and scientific leadership | HIGH | HIGH | Manage Closely — Surveillance science |
| UKHSA CDIO | Technology strategy | HIGH | HIGH | Manage Closely — Architecture, infrastructure |
| UKHSA SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, security classification |
| Epidemiology Teams | Operational surveillance | MEDIUM | HIGH | Keep Informed — User requirements, workflows |
| Laboratory Network Leads | Diagnostic data providers | MEDIUM | HIGH | Keep Informed — Data integration requirements |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DHSC Minister for Health Security | Government | Political sponsor | HIGH | HIGH |
| Cabinet Office (COBR) | Government | Crisis response coordination | HIGH | HIGH |
| Chief Medical Officer (CMO) | Government | Chief scientific adviser | HIGH | HIGH |
| WHO | International body | IHR reporting obligations | HIGH | MEDIUM |
| NHS England | Health service | Hospital surveillance data provider | MEDIUM | HIGH |
| Devolved Health Agencies | Scotland, Wales, NI | UK-wide surveillance | MEDIUM | HIGH |
| NCSC | Intelligence community | Cyber security for CNI | HIGH | MEDIUM |
| Five Eyes Health Security Partners | International | Intelligence sharing | MEDIUM | MEDIUM |
| Academic Research Community | Universities | Surveillance science, modelling | LOW | HIGH |
| Public | Citizens | Transparency, trust | LOW | HIGH |
| HM Treasury | Government | Funding | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * UKHSA CE         |
        |  * NCSC             |  * SRO              |
        |  * UKHSA SIRO       |  * DHSC Minister    |
        |                     |  * Cabinet Office   |
        |                     |  * CMO              |
 P      |                     |  * UKHSA Chief Data |
 O      |                     |  * UKHSA CDIO       |
 W      |                     |  * WHO              |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Five Eyes        |  * Epidemiology     |
        |                     |  * Lab Networks     |
        |                     |  * NHS England      |
        |                     |  * Devolved Agencies|
        |                     |  * Academic Research|
        |                     |  * Public           |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DHSC Minister — Never Again Caught Unprepared

**Stakeholder**: DHSC Minister for Health Security

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Ensure the UK is never again caught without the digital surveillance infrastructure needed to detect and respond to a pandemic. The COVID-19 Inquiry findings on surveillance failures must be addressed with demonstrable capability improvement.

**Driver Intensity**: CRITICAL

**Context & Background**: The COVID-19 Inquiry highlighted that the UK's surveillance infrastructure was fragmented, relied on manual data processing, and could not scale to pandemic response speed. The political cost of being seen as unprepared for the next pandemic is enormous.

---

### SD-2: UKHSA Chief Data Officer — Unified Surveillance Picture

**Stakeholder**: UKHSA Chief Data and Surveillance Officer

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Integrate all surveillance data sources (laboratory, hospital, primary care, wastewater, genomic, syndromic, mortality) into a single real-time operational picture, replacing the current patchwork of disconnected systems.

**Driver Intensity**: CRITICAL

---

### SD-3: Cabinet Office (COBR) — Timely Intelligence for Crisis Decisions

**Stakeholder**: Cabinet Office (COBR)

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Receive timely, accurate, actionable health security intelligence to support COBR decision-making during health emergencies, with data presented in formats suitable for Ministerial and cross-government briefing.

**Driver Intensity**: HIGH

---

### SD-4: WHO — International Health Regulations Compliance

**Stakeholder**: World Health Organisation

**Driver Category**: COMPLIANCE / INTERNATIONAL

**Driver Statement**: Ensure the UK meets its International Health Regulations (IHR) reporting obligations, including notification of public health events of international concern within 24 hours and ongoing situation reporting.

**Driver Intensity**: HIGH

---

### SD-5: Academic Research Community — Open Data for Pandemic Science

**Stakeholder**: Academic researchers, epidemiologists, modellers

**Driver Category**: STRATEGIC / PERSONAL

**Driver Statement**: Access timely, high-quality, de-identified surveillance data to conduct epidemiological research, build predictive models, and contribute to pandemic preparedness science.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Detect Novel Pathogen Signals Within 24 Hours

**Derived From Drivers**: SD-1, SD-2, SD-3

**Goal Owner**: UKHSA Chief Data and Surveillance Officer

**Goal Statement**: Detect anomalous patterns in surveillance data that may indicate a novel pathogen or significant epidemiological change within 24 hours of data availability, compared to the 7-14 day detection window experienced during early COVID-19.

**Baseline**: 7-14 days for novel signal detection (COVID-19 early experience)

**Target**: < 24 hours from data availability to alert generation

---

### Goal G-2: Scale to Pandemic Response Within 48 Hours

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: UKHSA CDIO

**Goal Statement**: The system must scale from routine surveillance mode (processing 50,000 laboratory results daily) to full pandemic response mode (processing 5 million results daily) within 48 hours, without architectural changes or manual infrastructure provisioning.

**Baseline**: COVID-19 required 4-6 weeks to build data processing capacity

**Target**: 100x scaling within 48 hours via automated infrastructure scaling

---

### Goal G-3: Unified Operational Picture Across All Data Sources

**Derived From Drivers**: SD-2, SD-3

**Goal Owner**: UKHSA Chief Data and Surveillance Officer

**Goal Statement**: Integrate laboratory, hospital admission, GP syndromic surveillance, wastewater genomics, mortality, and genomic sequencing data into a single dashboard providing national and regional situational awareness.

**Baseline**: 7+ separate surveillance systems with manual data aggregation

**Target**: Single integrated dashboard with < 1 hour data latency for all sources

---

### Goal G-4: Automated IHR Reporting to WHO

**Derived From Drivers**: SD-4

**Goal Owner**: SRO

**Goal Statement**: Automate WHO International Health Regulations reporting so that notifiable events are reported within 24 hours with structured data in WHO-specified formats.

**Baseline**: Manual IHR reporting with inconsistent timeliness

**Target**: Automated reporting within 24 hours of event detection

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Cabinet Office (SD-3) requires some surveillance intelligence classified at SECRET for COBR briefings, but the academic community (SD-5) and WHO (SD-4) require open data sharing for pandemic science and international obligations.
  - **Resolution Strategy**: Implement a **tiered data classification model**: operational intelligence for COBR classified at appropriate level with need-to-know access; de-identified aggregate data published openly on UKHSA dashboard; WHO IHR data shared through established diplomatic channels. Raw surveillance data accessible to accredited researchers via Trusted Research Environments.

- **Conflict 2**: UKHSA (SD-2) wants real-time integration of all data sources, but NHS England and GP data owners have governance concerns about sharing clinical data with a security agency.
  - **Resolution Strategy**: Establish clear Data Sharing Agreements with NHS England that define the specific data elements shared (aggregate, de-identified where possible), the legal basis (public health legislation), and the purpose limitation (surveillance only, not individual patient management). Caldicott Guardian oversight of all clinical data flows.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Surveillance architecture | UKHSA CDIO | UKHSA CE | NHS England, Devolved Agencies | All |
| Data classification | UKHSA SIRO | UKHSA CE | NCSC, Cabinet Office | All |
| Crisis activation (pandemic mode) | UKHSA Chief Medical Adviser | DHSC Minister | CMO, COBR | All |
| WHO IHR reporting | Surveillance Lead | SRO | CMO, FCO | WHO |
| Budget approval | UKHSA Finance Director | UKHSA CE | HM Treasury | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| COVID-19 Inquiry Report | Report | UK COVID-19 Inquiry | Surveillance failures and recommendations | N/A — external reference |
| WHO International Health Regulations | Treaty | WHO | IHR reporting obligations | N/A — external reference |
| UK Biological Security Strategy | Strategy | UK Government | Pandemic preparedness priorities | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Pandemic Preparedness System
**Model**: Claude Opus 4.6
