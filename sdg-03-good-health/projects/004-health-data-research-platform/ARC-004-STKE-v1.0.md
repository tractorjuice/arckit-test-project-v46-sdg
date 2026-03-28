# Stakeholder Drivers & Goals Analysis: Health Data Research Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Health Data Research Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Health Data Research Platform Programme, DHSC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Health Data Research Programme Board, DHSC Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Health Data Research Platform — a Trusted Research Environment (TRE) providing accredited researchers with secure access to de-identified health datasets for analytics, epidemiology, AI/ML model development, and population health research.

### Key Findings

The Health Data Research Platform navigates the fundamental tension in health data: the immense public value of making health data available for research (new treatments, better public health policy, pandemic preparedness) versus the individual right to privacy and the risk of re-identification or misuse. The strongest alignment exists around creating a secure, governed environment where data does not leave the platform. The most significant conflict is between the speed of research access (researchers need data quickly) and the rigour of data governance (Information Governance teams need thorough review).

### Critical Success Factors

- Data does not leave the Trusted Research Environment — analysis comes to the data, not data to the analyst
- Five Safes framework implemented: Safe People, Safe Projects, Safe Settings, Safe Data, Safe Outputs
- Accreditation by the UK Statistics Authority as a Trusted Research Environment
- Researcher onboarding time reduced from 6 months to 6 weeks
- Public trust maintained through transparency, patient and public involvement, and National Data Opt-Out compliance

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the value of health data research and the need for a secure platform. Tensions between research speed (academic community), governance rigour (IG professionals), commercial access (life sciences industry), and public trust (patient groups).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DHSC Chief Scientific Adviser | Scientific leadership | HIGH | HIGH | Manage Closely — Research strategy |
| SRO, Health Data Research Platform | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DHSC CDIO | Technology strategy | HIGH | HIGH | Manage Closely — Architecture, cloud strategy |
| DHSC SIRO / Caldicott Guardian | Data governance | HIGH | HIGH | Manage Closely — Data access decisions |
| NHS England Director of Data | NHS data provision | HIGH | HIGH | Manage Closely — Data supply agreements |
| IG Team Lead | Information governance | HIGH | MEDIUM | Keep Satisfied — DPIA, data access review |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Health Data Research UK (HDR UK) | Research infrastructure | Strategic partner | HIGH | HIGH |
| UKRI / NIHR | Research funders | Funding and strategy | HIGH | HIGH |
| University Research Teams | Academic community | Platform users | LOW | HIGH |
| Life Sciences Industry (ABPI) | Pharmaceutical companies | Data consumers (de-identified) | MEDIUM | HIGH |
| ICO | Regulator | Data protection oversight | HIGH | MEDIUM |
| UK Statistics Authority | Accreditation body | TRE accreditation | HIGH | HIGH |
| Patient and Public Groups | Citizens | Data subjects, public trust | MEDIUM | HIGH |
| Genomics England | Partner | Genomic data provision | MEDIUM | HIGH |
| ONS | Government | Census and demographic data | MEDIUM | MEDIUM |
| HM Treasury | Government | Funding approval | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * ICO              |  * DHSC Chief Sci   |
        |  * HM Treasury      |  * SRO              |
        |  * IG Team Lead     |  * DHSC CDIO        |
        |                     |  * SIRO/Caldicott   |
 P      |                     |  * NHS England Data |
 O      |                     |  * HDR UK           |
 W      |                     |  * UKRI/NIHR        |
 E      |                     |  * UK Stats Auth    |
 R      +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * ONS              |  * University Teams |
        |                     |  * ABPI/Pharma      |
        |                     |  * Patient Groups   |
        |                     |  * Genomics England |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: DHSC Chief Scientific Adviser — Accelerate Health Research for Population Benefit

**Stakeholder**: DHSC Chief Scientific Adviser

**Driver Category**: STRATEGIC

**Driver Statement**: Enable world-class health data research that translates into better treatments, improved public health policy, and enhanced pandemic preparedness, maintaining the UK's position as a global leader in health data science.

**Context & Background**: The UK has unique health data assets — the NHS provides universal coverage with cradle-to-grave records. However, accessing this data for research is slow, fragmented, and inconsistent. Other countries (Denmark, Finland, Israel) are building national health data platforms. The UK risks losing its competitive advantage in health data research.

**Driver Intensity**: CRITICAL

---

### SD-2: Patient and Public Groups — Trust, Transparency, and Control

**Stakeholder**: Patient and public involvement groups

**Driver Category**: ETHICAL / PERSONAL

**Driver Statement**: Ensure that health data is used for genuine public benefit with full transparency about who is accessing data, for what purpose, and with what safeguards. Patients must retain the right to opt out and must be confident their data cannot be re-identified.

**Context & Background**: The care.data programme (2013-2016) was abandoned after public backlash over insufficient transparency and consent. Any health data platform must learn from this failure. Public trust is the prerequisite for data availability — without it, opt-out rates will be high and the platform will have insufficient data for meaningful research.

**Driver Intensity**: HIGH

---

### SD-3: University Research Teams — Fast, Flexible Data Access

**Stakeholder**: Academic health data researchers

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Access high-quality, linked health datasets within weeks (not months), with the analytical tools needed for cutting-edge research (R, Python, Jupyter, GPU compute for ML), without bureaucratic barriers that delay research and jeopardise grant timelines.

**Context & Background**: Currently, researchers spend 3-12 months navigating data access processes — IG reviews, data sharing agreements, ethical approvals — before they can begin analysis. By the time data arrives, grant timelines are compressed, research questions have evolved, and data is outdated. Researchers need a platform that pre-authorises data access within governed boundaries.

**Driver Intensity**: HIGH

---

### SD-4: UK Statistics Authority — TRE Accreditation Standards

**Stakeholder**: UK Statistics Authority (UKSA)

**Driver Category**: COMPLIANCE / QUALITY

**Driver Statement**: Ensure the platform meets UKSA Trusted Research Environment accreditation standards, including the Five Safes framework, secure output checking, researcher accreditation, and transparent governance.

**Driver Intensity**: HIGH

---

### SD-5: Life Sciences Industry — Commercial Research Access

**Stakeholder**: ABPI (Association of the British Pharmaceutical Industry) and pharmaceutical companies

**Driver Category**: COMMERCIAL / STRATEGIC

**Driver Statement**: Access de-identified NHS health datasets for drug development, clinical trial design, real-world evidence generation, and health economics research, within a governed framework that maintains public trust while enabling commercial innovation.

**Context & Background**: The UK Life Sciences Strategy positions NHS data as a strategic asset for attracting pharmaceutical R&D investment to the UK. Companies will invest in UK research facilities if they can access high-quality health data. However, commercial access to NHS data is politically sensitive — the public must see clear benefit.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Researcher Data Access Time from 6 Months to 6 Weeks

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: SRO

**Goal Statement**: Reduce the average time from research application to data access from 6 months to 6 weeks through pre-approved data access agreements, automated IG review for standard requests, and pre-linked datasets within the TRE.

**Baseline**: 6 months average

**Target**: 6 weeks average for standard research applications

---

### Goal G-2: UK Statistics Authority TRE Accreditation

**Derived From Drivers**: SD-4

**Goal Owner**: SRO

**Goal Statement**: Achieve UK Statistics Authority Trusted Research Environment accreditation within 12 months of platform launch, demonstrating full compliance with the Five Safes framework.

---

### Goal G-3: Maintain Public Trust — Opt-Out Rate Below 5%

**Derived From Drivers**: SD-2

**Goal Owner**: Caldicott Guardian

**Goal Statement**: Maintain National Data Opt-Out rate below 5% (currently approximately 3.3%) by demonstrating transparent, governed, beneficial use of health data that maintains public trust.

**Baseline**: 3.3% National Data Opt-Out rate

**Target**: Maintain below 5%

---

### Goal G-4: Attract GBP 100M+ Annual Life Sciences R&D Investment

**Derived From Drivers**: SD-1, SD-5

**Goal Owner**: DHSC Chief Scientific Adviser

**Goal Statement**: The platform should be cited as a contributing factor in life sciences companies investing GBP 100M+ annually in UK-based health data research within 3 years of launch.

---

## Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Researchers (SD-3) want fast data access, but IG teams and patient groups (SD-2, SD-4) require thorough governance review before any access is granted.
  - **Resolution Strategy**: Implement a **tiered access model**: pre-approved aggregate/anonymised datasets available in days; standard de-identified linked datasets available within 6 weeks via automated IG workflow; bespoke sensitive data requests via full IG review (3 months). Most research can use the first two tiers, with the full review reserved for complex or sensitive requests.

- **Conflict 2**: Life sciences industry (SD-5) wants commercial access to NHS data, but patient groups (SD-2) and the public are concerned about NHS data being "sold" to pharmaceutical companies.
  - **Resolution Strategy**: Implement a **transparent commercial access framework**: commercial researchers pay cost-recovery fees (not profit), must demonstrate public benefit in their research, and their projects are listed on a public register. Data never leaves the TRE. Independent ethics review for all commercial applications. Patient and public involvement group reviews all commercial access applications.

**Synergies**:

- **Synergy 1**: SD-1 (research acceleration) and SD-5 (commercial access) both benefit from a well-governed TRE that provides fast, secure access
- **Synergy 2**: SD-2 (public trust) and SD-4 (UKSA accreditation) both drive rigorous governance, creating a single governance framework that serves both

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Data access approval (standard) | IG Automated Workflow | SIRO/Caldicott | Researcher, Data Steward | Patient Groups |
| Data access approval (sensitive) | IG Review Panel | Caldicott Guardian | Ethics Committee, Patient Groups | All |
| Commercial access approval | IG Review Panel | Caldicott Guardian | Patient Groups, DHSC Policy | Public Register |
| Platform architecture | Lead Architect | DHSC CDIO | HDR UK, NHS England | All |
| TRE accreditation | TRE Accreditation Lead | SRO | UKSA, IG Team | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Goldacre Review (Better, Broader, Safer) | Report | DHSC | TRE architecture recommendations | N/A — external reference |
| UK Statistics Authority TRE Standards | Standard | UKSA | Five Safes accreditation criteria | N/A — external reference |
| National Data Opt-Out | Policy | NHS Digital | Patient opt-out mechanism | N/A — external reference |
| UK Life Sciences Strategy | Strategy | UK Government | Health data as strategic asset | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Health Data Research Platform
**Model**: Claude Opus 4.6
