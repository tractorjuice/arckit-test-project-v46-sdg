# Stakeholder Drivers & Goals Analysis: Air Quality Monitoring Network

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
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
| **Distribution** | Air Quality Monitoring Programme Board, DEFRA, UKHSA, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Air Quality Monitoring Network, a real-time air pollution monitoring and alerting platform integrating DEFRA's Automatic Urban and Rural Network (AURN) with lower-cost sensor networks, IoT infrastructure (Project 001), and public health alerting systems.

### Key Findings

The Air Quality Monitoring Network exists at the intersection of environmental science, public health, and urban transport policy. The strongest alignment exists around improving public access to air quality information — citizens, health professionals, and local authorities all benefit from accurate, timely, localised air quality data. The most significant tensions are between scientific rigour (DEFRA and the Environment Agency insisting on MCERTS-certified reference-grade instruments) and coverage ambition (local authorities wanting dense networks of lower-cost sensors), and between transparent data publication (revealing pollution hotspots) and political sensitivity (Clean Air Zone compliance data showing cities failing legal limits).

### Critical Success Factors

- Integrate AURN reference-grade stations with lower-cost sensor networks through validated data fusion algorithms
- Achieve UK legal limit compliance monitoring with data quality accepted by DEFRA and the Environment Agency
- Deliver real-time air quality alerts to citizens within 5 minutes of threshold exceedance
- Support Clean Air Zone compliance monitoring for 30+ local authorities
- Publish air quality open data with API access on data.gov.uk meeting INSPIRE requirements

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for better air quality monitoring and public information. Tensions between scientific accuracy (reference-grade monitoring) and spatial coverage (lower-cost sensors), between transparent publication of pollution data and political management of compliance failures, and between DEFRA's national reporting obligations and local authority Clean Air Zone enforcement needs.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DEFRA Secretary of State | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, clean air narrative |
| DEFRA Chief Scientific Adviser | Scientific integrity | HIGH | HIGH | Manage Closely — Data quality standards |
| SRO, Air Quality Monitoring | Programme Sponsor (DEFRA) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DEFRA Air Quality Team | Policy and regulatory team | HIGH | HIGH | Manage Closely — Regulatory requirements |
| Environment Agency | Environmental regulator | HIGH | HIGH | Manage Closely — MCERTS standards, compliance |
| DEFRA Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| UK Health Security Agency (UKHSA) | Health protection | Public health alerting | HIGH | HIGH |
| Local Authority Environmental Health | 333 English LAs | Clean Air Zone operators | HIGH | HIGH |
| Clean Air Zone Cities | Bath, Birmingham, Bradford, Bristol, Portsmouth, Sheffield, Tyneside, GM | CAZ compliance monitoring | HIGH | HIGH |
| NHS England | Health service | Health impact data consumer | MEDIUM | HIGH |
| ClientEarth | Environmental law charity | Legal enforcement of air quality limits | HIGH | HIGH |
| Friends of the Earth / Greenpeace | Environmental campaign | Air quality campaigning | LOW | HIGH |
| British Lung Foundation / Asthma + Lung UK | Health charity | Patient advocacy | LOW | HIGH |
| Imperial College London / Kings College London | Academic | Air quality science, LAQN | MEDIUM | HIGH |
| National Physical Laboratory (NPL) | Measurement standards | Sensor calibration and traceability | MEDIUM | HIGH |
| CDDO | Cabinet Office | Spend control and assurance | HIGH | MEDIUM |
| DfT | Partner department | Transport emissions data | MEDIUM | HIGH |
| Citizens (especially parents, elderly, respiratory patients) | Public | Health-impacted groups | LOW | HIGH |
| Sensor Manufacturers | Industry | Lower-cost sensor suppliers | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | End-to-end air quality data service | HIGH / HIGH | Manage Closely — Service reviews |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control gates |

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA — Meeting Legal Air Quality Obligations

**Stakeholder**: DEFRA Air Quality Team and Secretary of State

**Driver Category**: COMPLIANCE / POLITICAL

**Driver Statement**: Ensure the UK meets its legally binding air quality limits under the Environment Act 2021 air quality targets and retained EU Ambient Air Quality Directive (2008/50/EC), with monitoring data of sufficient quality and coverage to satisfy legal scrutiny — particularly given ongoing ClientEarth litigation and judicial review risk.

**Context & Background**:
The UK has been found in breach of legal NO2 limits by the Supreme Court (R (ClientEarth) v Secretary of State for Environment, Food and Rural Affairs). The Environment Act 2021 introduced new PM2.5 targets (annual mean of 10 ug/m3 by 2040, interim target of 12 ug/m3). Compliance monitoring requires MCERTS-certified reference-grade instruments at specified locations. DEFRA's AURN network provides high-quality data but has only ~170 stations nationally — insufficient for the granular, localised monitoring needed for Clean Air Zone enforcement and public health alerting. The monitoring data is evidence in legal proceedings and must withstand scientific and legal challenge.

**Driver Intensity**: CRITICAL

**Enablers**:
- AURN network maintained and expanded as the authoritative reference layer
- Validated data fusion methodology that combines reference-grade with indicative sensors
- MCERTS accreditation maintained for all reference-grade stations

**Blockers**:
- Budget constraints limiting AURN expansion (each reference station costs £100-150K capital + £30K/year operating)
- Lower-cost sensors being used as de facto compliance monitors without adequate validation

---

### SD-2: Local Authority Environmental Health — Clean Air Zone Enforcement

**Stakeholder**: Local Authority Environmental Health Officers, Clean Air Zone Cities

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Access reliable, real-time, localised air quality data to monitor and enforce Clean Air Zones, assess the impact of traffic management measures, and fulfil statutory Air Quality Management Area (AQMA) obligations — with data granularity and coverage that the current AURN network cannot provide.

**Context & Background**:
Over 40 local authorities have declared Air Quality Management Areas where legal limits are exceeded. Eight cities are implementing Clean Air Zones with charging for polluting vehicles. Local authorities need dense, localised monitoring to assess whether their interventions are working — data from a single AURN station per city is insufficient. Many authorities have deployed their own monitoring using lower-cost sensors (Breathe London, AirSensa, etc.), but data quality is variable and interoperability with DEFRA systems is poor. Authorities want validated data they can use in enforcement decisions and report to DEFRA.

**Driver Intensity**: CRITICAL

**Enablers**:
- Dense sensor networks providing street-level air quality data
- Integration with CAZ ANPR and traffic management systems
- Data validated against nearest AURN reference station

**Blockers**:
- Cost of reference-grade monitoring at the density local authorities need
- DEFRA reluctance to accept lower-cost sensor data for compliance reporting

---

### SD-3: UKHSA — Protecting Public Health Through Timely Alerts

**Stakeholder**: UK Health Security Agency

**Driver Category**: PUBLIC HEALTH / OPERATIONAL

**Driver Statement**: Receive accurate, timely air quality data to issue health alerts and advice to vulnerable populations (respiratory patients, elderly, children), integrate with UKHSA health surveillance systems, and support epidemiological research linking air pollution exposure to health outcomes.

**Context & Background**:
Air pollution causes an estimated 28,000-36,000 premature deaths annually in the UK (COMEAP). UKHSA operates the Daily Air Quality Index (DAQI) alerting system but relies on AURN data that updates hourly with limited spatial resolution. Vulnerable individuals — asthma sufferers, COPD patients, pregnant women — need hyperlocal, near-real-time alerts to make informed decisions about outdoor activities. The 2022 Coroner's ruling in the Ella Adoo-Kissi-Debrah case established air pollution as a cause of death for the first time, creating legal precedent for the duty to warn.

**Driver Intensity**: CRITICAL

**Enablers**:
- Near-real-time data feeds (5-minute update frequency) to UKHSA alerting systems
- Hyperlocal pollution estimates (street-level, not city-average)
- Integration with NHS health records for exposure-outcome research

**Blockers**:
- Lower-cost sensor data quality insufficient for health alert thresholds
- Public confusion from conflicting readings between different sensor networks

---

### SD-4: ClientEarth — Legal Accountability for Air Quality Compliance

**Stakeholder**: ClientEarth (environmental law charity)

**Driver Category**: COMPLIANCE / ACCOUNTABILITY

**Driver Statement**: Ensure that air quality monitoring data is transparent, publicly accessible, scientifically robust, and of sufficient quality and coverage to enable independent verification of whether the UK is meeting its legal air quality obligations — particularly the new PM2.5 targets under the Environment Act 2021.

**Context & Background**:
ClientEarth has successfully brought multiple legal challenges against the UK Government for failing to meet air quality limits. They use monitoring data as evidence in court. Their interest in the platform is twofold: better monitoring coverage exposes more non-compliance areas, but the data must be of sufficient quality to withstand legal challenge. They are concerned that lower-cost sensor data might be used to show superficial compliance or that data might be selectively published.

**Driver Intensity**: HIGH

**Enablers**:
- All monitoring data published as open data with metadata on measurement uncertainty
- Clear distinction between reference-grade and indicative sensor data in public-facing outputs
- Complete historical data archive accessible for trend analysis and legal proceedings

**Blockers**:
- Government publishing only "good news" data or suppressing readings from non-compliant areas
- Mixing reference-grade and indicative data without clear quality labelling

---

## Driver-to-Goal Mapping

### Goal G-1: Integrate AURN with 5,000 Lower-Cost Sensors via Validated Data Fusion

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: DEFRA Chief Scientific Adviser

**Goal Statement**: Deploy and integrate at least 5,000 validated lower-cost air quality sensors with the 170-station AURN reference network, using scientifically peer-reviewed data fusion algorithms, within 24 months.

**Success Metrics**:
- **Primary Metric**: Number of validated sensors integrated with AURN reference network
- **Secondary Metrics**: Data fusion algorithm peer-review status; measurement uncertainty bounds

**Baseline**: 170 AURN reference stations, ~2,000 unvalidated local authority sensors
**Target**: 170 AURN + 5,000 validated lower-cost sensors = 5,170 stations integrated
**Measurement Method**: Platform station inventory, data quality dashboard

---

### Goal G-2: Deliver Real-Time Air Quality Alerts Within 5 Minutes

**Derived From Drivers**: SD-3

**Goal Owner**: UKHSA Air Quality Alerting Team

**Goal Statement**: Deliver automated air quality health alerts to citizens within 5 minutes of a DAQI threshold exceedance, via push notifications, SMS, API, and GOV.UK, with hyperlocal resolution (1km grid).

**Success Metrics**:
- **Primary Metric**: Alert delivery latency (sensor reading to citizen notification)
- **Secondary Metrics**: Alert accuracy (false positive/negative rates); citizen subscription numbers

**Baseline**: Hourly DAQI updates, city-level resolution, manual alert process
**Target**: 5-minute latency, 1km resolution, fully automated alerting
**Measurement Method**: Platform alerting pipeline metrics, citizen feedback surveys

---

### Goal G-3: Support Clean Air Zone Monitoring for 30+ Local Authorities

**Derived From Drivers**: SD-2

**Goal Owner**: SRO, Air Quality Monitoring Network

**Goal Statement**: Provide validated air quality monitoring data (NO2, PM2.5, PM10, O3) to at least 30 local authorities for Clean Air Zone compliance monitoring and AQMA assessment within 18 months.

**Success Metrics**:
- **Primary Metric**: Number of local authorities using platform for CAZ/AQMA monitoring
- **Secondary Metrics**: DEFRA acceptance of platform data for annual status reports

**Baseline**: 8 CAZ cities with independent monitoring, variable quality
**Target**: 30+ LAs using standardised platform monitoring
**Measurement Method**: Authority adoption tracker, DEFRA annual status report submissions

---

### Goal G-4: Publish Complete Air Quality Open Data on data.gov.uk

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: DEFRA Data Team

**Goal Statement**: Publish all air quality monitoring data (reference-grade and validated indicative) as open data on data.gov.uk with INSPIRE-compliant metadata, clear data quality flags, and historical archive access within 12 months.

**Success Metrics**:
- **Primary Metric**: Datasets published on data.gov.uk with INSPIRE metadata
- **Secondary Metrics**: API call volumes; third-party application registrations; data download volumes

**Baseline**: AURN data published on uk-air.defra.gov.uk (limited API, no INSPIRE metadata)
**Target**: Complete dataset on data.gov.uk, INSPIRE compliant, real-time API, historical archive
**Measurement Method**: data.gov.uk analytics, API usage metrics

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DEFRA | SD-1 | Legal compliance | G-1 | AURN + 5000 sensors | O-1 | Comprehensive monitoring |
| DEFRA | SD-1 | Legal compliance | G-4 | Open data published | O-1 | Comprehensive monitoring |
| Local Authorities | SD-2 | CAZ enforcement | G-3 | 30+ LAs supported | O-2 | Effective CAZ monitoring |
| UKHSA | SD-3 | Public health alerts | G-2 | 5-minute alerts | O-3 | Timely health protection |
| ClientEarth | SD-4 | Legal accountability | G-4 | Open data published | O-1 | Comprehensive monitoring |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Local authorities (SD-2) want dense, affordable sensor networks for street-level monitoring, but DEFRA (SD-1) and the Environment Agency insist on MCERTS-certified reference-grade instruments for compliance data, which cost 10-50x more per station.
  - **Resolution Strategy**: Tiered data quality framework — reference-grade for compliance, validated indicative sensors for supplementary monitoring with clear uncertainty labelling. Data fusion algorithms co-calibrate indicative sensors against nearest reference station. Published methodology peer-reviewed by NPL.

- **Conflict 2**: ClientEarth (SD-4) wants all monitoring data published transparently including non-compliant areas, but DEFRA and local authority politicians may be uncomfortable with data that exposes failures to meet legal limits.
  - **Resolution Strategy**: All data published as open data by default — this is a legal obligation under the Environmental Information Regulations 2004. No selective publication. Data quality flags ensure responsible interpretation.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environment Act 2021 | Legislation | legislation.gov.uk | PM2.5 targets, environmental monitoring | N/A — external reference |
| Ambient Air Quality Directive 2008/50/EC (retained) | Legislation | legislation.gov.uk | Air quality limit values | N/A — external reference |
| MCERTS Scheme | Standard | Environment Agency | Environmental monitoring certification | N/A — external reference |
| AURN Technical Guidance | Standard | DEFRA | Reference-grade monitoring requirements | N/A — external reference |
| R (ClientEarth) v SoS EFRA | Case law | Supreme Court | Legal obligation to meet air quality limits | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Air Quality Monitoring Network (Project 005)
**Model**: Claude Opus 4.6
