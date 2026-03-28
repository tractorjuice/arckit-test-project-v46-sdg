# Stakeholder Drivers & Goals Analysis: Flood Risk Management System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Flood Risk Management System (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Flood Risk Management System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Environment Agency, DEFRA, Met Office, Lead Local Flood Authorities |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Flood Risk Management System, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. Flood warning and forecasting is life-safety critical infrastructure — stakeholder analysis must prioritise the safety of citizens in flood-risk areas above all other considerations.

### Key Findings

The Flood Risk Management System operates at the intersection of meteorological science, hydrological modelling, emergency response, and public communication. The dominant driver is the protection of human life — the Environment Agency has a statutory duty under the Flood and Water Management Act 2010 to warn citizens of flood risk. The primary tension is between the speed of warning dissemination (earlier warnings save more lives but have higher false-alarm rates) and warning accuracy (reducing false alarms maintains public trust but delays dissemination). A secondary tension exists between the EA's national system and Lead Local Flood Authorities who have surface water flooding responsibilities but limited resources and technical capability to operate sophisticated forecasting tools.

### Critical Success Factors

- Reduce flood warning lead time from current average of 2 hours to 4+ hours for fluvial flooding
- Achieve sub-2-minute data latency from river level gauge to forecasting model
- Integrate Met Office Unified Model rainfall forecasts with EA hydrological models in near-real-time
- Deliver surface water flood forecasting capability for Lead Local Flood Authorities
- Maintain 99.99% system availability during Met Office severe weather warnings

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Strong alignment across all stakeholders on the fundamental objective of protecting life and property from flooding. The primary disagreements are technical (modelling approaches, warning threshold calibration) and organisational (national vs local responsibilities, data sharing arrangements with insurers). No stakeholder opposes the programme objectives.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| EA Chief Executive | Agency leadership | HIGH | HIGH | Manage Closely — Programme board |
| EA Executive Director of Flood and Coastal Risk Management | Programme sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| EA Flood Forecasting Centre (joint with Met Office) | Operational forecasting | HIGH | HIGH | Manage Closely — Technical design authority |
| EA Flood Warning Duty Officers | Operational warning decisions | MEDIUM | HIGH | Keep Informed — User research, training |
| EA Area Flood Risk Managers (x6 areas) | Regional delivery | MEDIUM | HIGH | Keep Informed — Requirements, testing |
| EA Digital, Data & Technology Director | Technical leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| EA SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DEFRA Secretary of State | DEFRA | Ministerial oversight | HIGH | MEDIUM |
| DEFRA Flood Policy Director | DEFRA | Policy sponsorship | HIGH | HIGH |
| Met Office Chief Scientist | Met Office | Joint forecasting partner | HIGH | HIGH |
| Met Office Flood Forecasting Centre team | Met Office | Operational partner | HIGH | HIGH |
| Lead Local Flood Authorities (152 in England) | Local councils | Surface water flood risk | MEDIUM | HIGH |
| Category 1 Responders (police, fire, ambulance, NHS) | Emergency services | Flood response coordination | MEDIUM | HIGH |
| Local Resilience Forums (38 in England) | Multi-agency partnerships | Emergency planning | MEDIUM | HIGH |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| CDDO | Cabinet Office | Spend control, digital standards | HIGH | MEDIUM |
| Association of British Insurers | ABI | Flood insurance risk modelling | MEDIUM | HIGH |
| Flood Re | Flood Re | Flood insurance scheme | MEDIUM | HIGH |
| National Flood Forum | Charity | Flood-affected communities | LOW | HIGH |
| Internal Drainage Boards | IDBs | Low-lying area drainage | LOW | HIGH |
| Network Rail, Highways England | Infrastructure operators | Transport infrastructure protection | MEDIUM | MEDIUM |
| Citizens in flood-risk areas (~5.2M properties) | Public | Life safety, property protection | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * DEFRA Sec of     |  * EA Chief Exec    |
        |    State            |  * EA Exec Dir FCRM |
        |  * HM Treasury      |  * EA DDaT Director |
        |  * CDDO             |  * DEFRA Flood      |
        |  * EA SIRO          |    Policy Director   |
        |                     |  * Met Office Chief  |
 P      |                     |    Scientist         |
 O      |                     |  * EA Flood          |
 W      |                     |    Forecasting Centre|
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |                     |  * Citizens (5.2M   |
        |                     |    properties)       |
        |                     |  * LLFAs (152)      |
        |                     |  * Cat 1 Responders |
        |                     |  * Local Resilience  |
        |                     |    Forums            |
        |                     |  * ABI / Flood Re   |
        |                     |  * National Flood    |
        |                     |    Forum             |
        |                     |  * EA Warning Duty   |
        |                     |    Officers          |
        |                     |  * EA Area Managers  |
        |                     |  * Network Rail / HE|
        |                     |  * IDBs             |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: EA Executive Director FCRM — Faster, More Accurate Flood Warnings

**Stakeholder**: EA Executive Director of Flood and Coastal Risk Management

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Increase flood warning lead time and accuracy to reduce loss of life and economic damage from flooding, delivering the EA's statutory duties under the Flood and Water Management Act 2010 and Civil Contingencies Act 2004.

**Context & Background**:
The EA currently operates approximately 1,100 river level gauges feeding the National Flood Forecasting System. The average flood warning lead time for fluvial (river) flooding is approximately 2 hours — often insufficient for effective evacuation. Surface water (pluvial) flooding provides even less warning, sometimes minutes. The 2024 winter floods caused GBP 670M in damages and displaced 12,000 households. The EA's internal review concluded that improved forecasting could have provided an additional 2 hours warning at 40% of affected locations, enabling more effective response. Climate change projections indicate flood frequency and severity will increase significantly.

**Driver Intensity**: CRITICAL

**Enablers**:
- Higher-density river gauge network with sub-minute telemetry
- Integration of Met Office probabilistic rainfall forecasts into hydrological models
- Machine learning-enhanced rapid inundation mapping
- Surface water flood forecasting capability (currently limited)

**Blockers**:
- Computational constraints for running high-resolution models in real-time
- Gauge network gaps in upland catchments where floods originate
- Communication infrastructure limitations in rural flood-prone areas
- Organisational complexity of joint EA/Met Office forecasting centre governance

---

### SD-2: Met Office — Integrated Hydrometeorological Forecasting

**Stakeholder**: Met Office Chief Scientist

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Achieve seamless integration between meteorological rainfall prediction and hydrological flood forecasting, enabling ensemble-based probabilistic flood warnings with quantified uncertainty.

**Context & Background**:
The Flood Forecasting Centre (FFC) is jointly operated by the EA and Met Office. Currently, the atmospheric and hydrological modelling systems are loosely coupled — Met Office provides rainfall forecasts that EA hydrologists manually interpret to run flood models. A fully coupled system would run ensemble hydrological forecasts directly from Met Office ensemble rainfall predictions, providing probabilistic flood risk assessments (e.g., "30% chance of property flooding at location X within 6 hours"). This represents a step-change in forecasting capability.

**Driver Intensity**: HIGH

**Enablers**:
- API-based real-time data exchange between Met Office and EA systems
- Shared high-performance computing infrastructure for coupled model runs
- Common data standards for meteorological and hydrological variables
- Joint scientific programme for coupled model development

**Blockers**:
- Different organisational cultures and technology stacks (Met Office on HPC, EA on cloud)
- Intellectual property considerations around Met Office model outputs
- Governance complexity of jointly owned operational systems

---

### SD-3: Lead Local Flood Authorities — Surface Water Flood Capability

**Stakeholder**: Lead Local Flood Authorities (152 councils in England)

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Obtain practical, usable surface water flood forecasting and warning tools that enable councils to fulfil their statutory responsibilities for surface water flood risk management without requiring specialist hydrological expertise.

**Context & Background**:
The Flood and Water Management Act 2010 gave upper-tier local authorities the role of Lead Local Flood Authority (LLFA) with responsibility for surface water, groundwater, and ordinary watercourse flooding. However, the EA's existing flood warning system covers only main rivers and the sea — leaving a gap for the type of flooding that causes the most widespread disruption (surface water flooding affected 3 million properties in England according to EA estimates). LLFAs typically lack the technical expertise and computational resources to operate sophisticated flood models.

**Driver Intensity**: HIGH

**Enablers**:
- Pre-configured surface water flood risk models requiring minimal local expertise
- Automated alerts based on Met Office rainfall forecasts and local topography
- Integration with council emergency planning and response systems
- Training programme for LLFA staff on using surface water forecasting tools

**Blockers**:
- Extreme variation in LLFA capability (London boroughs vs rural counties)
- Funding constraints — many LLFAs have no dedicated flood risk budget
- Data quality issues with local drainage network information
- Political reluctance to issue warnings that may cause property value concerns

---

### SD-4: Category 1 Responders — Actionable Flood Intelligence

**Stakeholder**: Emergency services (police, fire, ambulance, NHS trusts)

**Driver Category**: OPERATIONAL

**Driver Statement**: Receive flood forecasts and warnings in formats that enable operational decision-making — not just "flooding expected" but "which roads will be impassable, which properties need evacuation, how deep and how fast."

**Context & Background**:
Current EA flood warnings provide geographic areas at risk and broad timing. Emergency responders need operational intelligence: predicted flood extents and depths at property level, road network impact predictions, estimated time to peak, and recession timing. The blue light services and NHS trusts have diverse IT systems and limited capacity to consume complex geospatial data — they need information pre-digested into actionable decision support.

**Driver Intensity**: HIGH

**Enablers**:
- Property-level flood depth predictions from rapid inundation modelling
- Road network impact predictions integrated with Highways England and council systems
- Pre-formatted incident briefing packs auto-generated from flood forecasts
- Integration with multi-agency Resilience Direct platform

**Blockers**:
- Model resolution insufficient for property-level predictions in all areas
- Emergency service IT systems vary significantly between forces/trusts
- Legal liability concerns around providing property-level flood depth predictions

---

### SD-5: Citizens in Flood-Risk Areas — Clear, Timely, Trusted Warnings

**Stakeholder**: 5.2 million properties at flood risk in England

**Driver Category**: CUSTOMER / RISK

**Driver Statement**: Receive flood warnings that are clear, timely, trustworthy, and actionable — telling people what to do, not just that flooding is possible — through channels they actually use, including mobile push notifications.

**Context & Background**:
The EA's Flood Warning Direct service reaches approximately 1.7 million registered properties. However, citizen research consistently shows that many people do not understand the severity coding system (Flood Alert vs Flood Warning vs Severe Flood Warning), do not know what actions to take, and do not receive warnings through their preferred channel. Post-event surveys from the 2024 floods found that 35% of flooded residents received no warning at all, and of those who did, 42% did not understand the severity.

**Driver Intensity**: CRITICAL

**Enablers**:
- Multi-channel notification (SMS, mobile app push, voice call, social media, smart speakers)
- Plain language warnings with specific action instructions
- Location-aware mobile app showing personalised flood risk in real-time
- Community flood warden network integration

**Blockers**:
- Low registration rates for flood warnings (only 33% of at-risk properties registered)
- Digital exclusion — many at-risk residents are elderly or have limited digital access
- Warning fatigue from historical false alarms reducing public response

---

## Driver-to-Goal Mapping

### Goal G-1: 4-Hour Fluvial Flood Warning Lead Time

**Derived From Drivers**: SD-1, SD-2, SD-5

**Goal Owner**: EA Flood Forecasting Centre

**Goal Statement**: Achieve minimum 4-hour average flood warning lead time for fluvial flooding events at EA-designated Flood Warning Areas, up from the current 2-hour average, by October 2027 (start of winter flood season).

**Success Metrics**:
- **Primary Metric**: Average warning lead time for fluvial flooding (target: 4 hours)
- **Secondary Metrics**:
  - False alarm rate (target: < 15%, down from current ~25%)
  - Warning coverage of actual flood events (target: > 95%)
  - Sensor data latency from gauge to model (target: < 2 minutes)

**Baseline**: 2-hour average warning lead time, 25% false alarm rate
**Target**: 4-hour average warning lead time, < 15% false alarm rate

---

### Goal G-2: Surface Water Flood Forecasting for LLFAs

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: EA Director of FCRM

**Goal Statement**: Deliver a surface water flood forecasting and alerting service available to all 152 LLFAs in England, requiring no specialist hydrological expertise to operate, by March 2028.

**Success Metrics**:
- **Primary Metric**: LLFAs with operational surface water forecasting capability (target: 152)
- **Secondary Metrics**:
  - LLFA user satisfaction (target: 80%+ find the tool "useful" or "very useful")
  - Surface water flood events detected and alerted (target: > 70%)

---

### Goal G-3: Property-Level Flood Intelligence for Emergency Responders

**Derived From Drivers**: SD-4

**Goal Owner**: EA Area Flood Risk Manager (lead region TBD)

**Goal Statement**: Provide property-level predicted flood depth and road network impact data to Category 1 Responders via the Resilience Direct platform within 30 minutes of a Flood Warning being issued, by October 2027.

**Success Metrics**:
- **Primary Metric**: Time from Flood Warning to property-level intelligence delivery (target: < 30 min)
- **Secondary Metrics**:
  - Prediction accuracy (target: flood depth within +/- 0.3m for 80% of properties)
  - Emergency responder satisfaction (target: 75%+ find intelligence "actionable")

---

### Goal G-4: Mobile-First Public Warning Service

**Derived From Drivers**: SD-5

**Goal Owner**: EA Digital Director

**Goal Statement**: Launch a mobile application providing location-aware, personalised flood risk information and push notification warnings, achieving 3 million downloads within 12 months of launch.

**Success Metrics**:
- **Primary Metric**: App downloads (target: 3 million within 12 months)
- **Secondary Metrics**:
  - Push notification delivery rate (target: > 98% within 60 seconds)
  - User comprehension of warning severity (target: > 85% correctly interpret warning level)
  - Accessibility audit pass at WCAG 2.2 Level AA

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| EA Exec Dir FCRM | SD-1 | Faster, more accurate warnings | G-1 | 4-hour warning lead time | O-1 | Reduced flood deaths/damage |
| Met Office | SD-2 | Integrated hydrometeorological forecasting | G-1 | 4-hour warning lead time | O-1 | Reduced flood deaths/damage |
| LLFAs | SD-3 | Surface water flood capability | G-2 | Surface water forecasting for LLFAs | O-2 | Reduced surface water flood impact |
| Cat 1 Responders | SD-4 | Actionable flood intelligence | G-3 | Property-level intelligence | O-1 | Reduced flood deaths/damage |
| Citizens | SD-5 | Clear, timely, trusted warnings | G-4 | Mobile-first warning service | O-1 | Reduced flood deaths/damage |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: EA (SD-1) wants longer warning lead times which increases false alarm rates, but Citizens (SD-5) lose trust when warnings prove false.
  - **Resolution Strategy**: Probabilistic messaging — communicate uncertainty honestly. "70% chance of property flooding" rather than binary warning/no-warning. Phase in probabilistic communication with public research on comprehension.

- **Conflict 2**: LLFAs (SD-3) want simple tools requiring no expertise, but surface water modelling is inherently complex and uncertain.
  - **Resolution Strategy**: Two-tier system — automated alerting for all LLFAs with simple traffic-light risk levels, plus advanced tools for LLFAs with specialist capability. Training programme for authorities wanting to move to advanced tier.

**Synergies**:

- **Synergy 1**: All stakeholders benefit from faster, more accurate forecasting (G-1) — this is the foundation that improves every downstream capability.
- **Synergy 2**: Property-level intelligence (G-3) required by responders also enables personalised public warnings (G-4).

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | EA Finance Director | EA Chief Executive | DEFRA, HM Treasury | All stakeholders |
| Forecasting methodology | EA/Met Office FFC | EA Exec Dir FCRM | Met Office Chief Scientist | LLFAs, responders |
| Warning dissemination policy | EA Area Managers | EA Exec Dir FCRM | Cat 1 Responders, LLFAs | Public, NFF |
| Architecture decisions | EA DDaT Director | SRO | Met Office Digital, NCSC | Vendors |
| Go/No-go for go-live | SRO | EA Chief Executive | DEFRA, Met Office | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Flood and Water Management Act 2010 | Legislation | legislation.gov.uk | EA flood warning duty, LLFA responsibilities | N/A — external reference |
| Civil Contingencies Act 2004 | Legislation | legislation.gov.uk | Category 1 Responder duties | N/A — external reference |
| National Flood and Coastal Erosion Risk Management Strategy | Strategy | GOV.UK | EA strategic objectives for flood risk | N/A — external reference |
| Architecture Principles | Architecture | ARC-000-PRIN-v1.0 | SDG 6 governing principles | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Flood Risk Management System (Project 002)
**AI Model**: Claude Opus 4.6 (1M context)
