# Stakeholder Drivers & Goals Analysis: Anti-Fraud Analytics Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Anti-Fraud Analytics Platform (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Government Counter Fraud Function, Cabinet Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Government Counter Fraud Function, Cabinet Office, CDDO, HMRC, DWP, BEIS |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document analyses stakeholders for the Anti-Fraud Analytics Platform — a cross-government fraud detection and prevention system that enables data sharing and analytics across departments to identify fraud patterns, prevent losses, and recover public funds.

### Key Findings

The Anti-Fraud Analytics Platform operates in a high-stakes environment where the Government Counter Fraud Function estimates annual fraud and error losses across government at GBP 33-58 billion. The strongest stakeholder alignment exists around the shared recognition that fraud crosses departmental boundaries — a fraudster exploiting one department's schemes is likely exploiting others. The most significant conflict is between the imperative for cross-government data sharing (fraud detection) and data protection concerns (ICO, privacy advocates) about creating centralised databases of citizen financial information. The COVID-19 pandemic fraud (GBP 4.9 billion in Bounce Back Loan fraud alone) created urgent political impetus for improved cross-government fraud detection.

### Critical Success Factors

- Establish lawful data sharing framework across 10+ departments within the Counter Fraud Functional Standard
- Detect fraud patterns that individual departments cannot identify in isolation
- Maintain strict data protection compliance while enabling effective analytics
- Demonstrate measurable fraud prevention and recovery (target: GBP 100M+ additional recoveries within 2 years)
- Achieve Home Office and law enforcement trust for intelligence-grade fraud referrals

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong cross-government consensus that fraud losses are unacceptable and that data sharing is essential. Tensions between detection ambition and privacy safeguards, between central analytics and departmental data ownership, and between automated scoring and human oversight of fraud determinations.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for the Cabinet Office | Minister | HIGH | HIGH | Manage Closely — Counter fraud strategy |
| Head of Government Counter Fraud Function | Programme lead | HIGH | HIGH | Manage Closely — Strategy, standards, delivery |
| Cabinet Office Permanent Secretary | Accounting Officer | HIGH | MEDIUM | Keep Satisfied — Spend, governance |
| CDDO | Digital standards | MEDIUM | MEDIUM | Keep Informed — Architecture, data standards |
| Counter Fraud Centre of Expertise | Analytical capability | MEDIUM | HIGH | Keep Informed — Methods, training |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| HMRC Counter Fraud | HMRC | Major data contributor and consumer | HIGH | HIGH |
| DWP Counter Fraud | DWP | Major data contributor (benefits fraud) | HIGH | HIGH |
| BEIS/DBT Counter Fraud | BEIS/DBT | COVID loan fraud recovery | HIGH | HIGH |
| National Crime Agency (NCA) | Law enforcement | Organised fraud investigation | HIGH | HIGH |
| Serious Fraud Office (SFO) | Law enforcement | Complex fraud prosecution | MEDIUM | HIGH |
| HM Treasury | HM Treasury | Public finance protection | HIGH | MEDIUM |
| NAO | Parliament | Fraud loss reporting | HIGH | HIGH |
| Public Accounts Committee | Parliament | Fraud scrutiny | HIGH | MEDIUM |
| Information Commissioner's Office (ICO) | Regulator | Data protection oversight | HIGH | HIGH |
| Citizens | Public | Subject of fraud checks | LOW | MEDIUM |

---

## Stakeholder Drivers Analysis

### SD-1: Minister for the Cabinet Office — Reducing the Fraud Tax on Public Services

**Stakeholder**: Minister for the Cabinet Office

**Driver Category**: POLITICAL / FINANCIAL

**Driver Statement**: Demonstrate credible, measurable progress in reducing fraud and error losses across government (currently estimated at GBP 33-58 billion annually), recovering COVID-era fraud losses, and preventing future fraud through cross-government analytics — enabling positive responses to PAC scrutiny and media coverage.

**Context & Background**:
The Government Counter Fraud Function estimates total fraud and error across government at 0.5-5% of total expenditure (GBP 33-58 billion at 2024/25 spending levels). COVID-19 emergency schemes created unprecedented fraud exposure — the Bounce Back Loan Scheme alone suffered estimated GBP 4.9 billion in fraud. The NAO and PAC have repeatedly criticised the government's ability to detect and prevent cross-departmental fraud. The Counter Fraud Functional Standard (GovS 013) mandates departments to work together, but departmental data silos prevent effective cross-government detection.

**Driver Intensity**: CRITICAL

**Enablers**:

- Cross-government data sharing platform with legal basis established
- Demonstrated fraud detection that individual departments could not achieve alone
- Publicisable fraud prevention and recovery figures (GBP saved/recovered)
- Strong governance framework satisfying ICO and privacy concerns

**Blockers**:

- Data sharing agreements taking too long to negotiate between departments
- ICO concerns about proportionality of cross-government data sharing
- Departments reluctant to share data that reveals their own fraud control failures
- Technical integration challenges with diverse departmental systems

**Related Stakeholders**: HM Treasury (public finance), NAO/PAC (scrutiny), NCA (enforcement), ICO (privacy)

---

### SD-2: HMRC and DWP Counter Fraud Teams — Cross-Government Intelligence

**Stakeholder**: HMRC Counter Fraud and DWP Counter Fraud

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Access cross-government data to identify fraud patterns that are invisible within a single department's data — particularly organised fraud groups that exploit multiple government schemes simultaneously, and identity fraud where the same fabricated identities are used across tax credits, benefits, and government grants.

**Context & Background**:
HMRC and DWP are the two largest fraud-exposed departments (combined annual fraud losses estimated at GBP 10-15 billion). Both have sophisticated internal counter fraud capabilities but are limited to their own data. Organised fraud groups deliberately exploit the gap between departments — claiming benefits from DWP while undeclaring income to HMRC, or using the same fabricated identities across both. Cross-government matching would expose these patterns immediately.

**Driver Intensity**: CRITICAL

**Enablers**:

- Secure data sharing platform with sub-second matching capabilities
- Standardised identity resolution across government datasets
- Analytics capability to detect multi-scheme exploitation patterns
- Secure intelligence sharing with NCA for organised fraud investigation

**Blockers**:

- Data sharing legal basis contested or unclear for specific data types
- Departments unwilling to share data that reveals internal control weaknesses
- Different data formats and quality standards across departments
- Alert fatigue from high false-positive rates in matching algorithms

**Related Stakeholders**: NCA (enforcement), BEIS/DBT (COVID loan fraud), ICO (proportionality), Citizens (false positive impact)

---

### SD-3: Information Commissioner's Office — Proportionate and Lawful Data Processing

**Stakeholder**: Information Commissioner's Office

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure that cross-government fraud data sharing is conducted on a clear lawful basis, is proportionate to the fraud risk being addressed, includes appropriate safeguards for citizen rights, and does not create a disproportionate surveillance capability.

**Context & Background**:
The ICO supports counter-fraud efforts but has consistently emphasised that data sharing must be proportionate, necessary, and conducted on a clear legal basis (UK GDPR Article 6). The ICO is concerned about the creation of centralised databases that aggregate citizen data across departments, the risk of false positives leading to citizens being incorrectly flagged as fraudulent, and the potential for function creep where fraud data sharing infrastructure is repurposed for other government objectives. The Digital Economy Act 2017 provides some legal basis for data sharing, but specific data sharing arrangements require individual DPIAs and ICO engagement.

**Driver Intensity**: HIGH

**Enablers**:

- Clear legal basis documented for each data sharing arrangement
- Data Protection Impact Assessments completed and published
- Proportionality assessments showing why less intrusive alternatives are insufficient
- False positive rate monitoring with clear remediation for incorrectly flagged citizens
- Data minimisation — sharing only the minimum data necessary for fraud detection
- Time-limited data retention with automated deletion

**Blockers**:

- Blanket cross-government data sharing without case-by-case justification
- No mechanism for citizens to challenge fraud flags or request human review
- Data retained indefinitely "just in case"
- Function creep beyond fraud detection

**Related Stakeholders**: Citizens (rights), Minister (political sensitivity), HMRC/DWP (data contributors), NCA (intelligence consumers)

---

### SD-4: National Crime Agency — Intelligence-Grade Fraud Referrals

**Stakeholder**: National Crime Agency

**Driver Category**: OPERATIONAL

**Driver Statement**: Receive intelligence-grade fraud referrals from the cross-government analytics platform that meet evidential standards for criminal investigation, targeting organised fraud networks rather than individual low-value opportunistic fraud.

**Context & Background**:
The NCA's economic crime command investigates serious and organised fraud. They need referrals that identify fraud networks (not just individual cases), provide sufficient evidence for investigation, and meet the threshold for NCA involvement (typically organised, cross-border, or high-value). Current departmental referrals are often poorly evidenced or target low-value cases that are better handled departmentally.

**Driver Intensity**: MEDIUM

**Enablers**:

- Network analysis identifying connected fraud actors across government schemes
- Referral packages that meet NCA evidential standards
- Secure intelligence sharing channel between the platform and NCA
- Prioritisation of organised and high-value fraud over individual low-value cases

**Blockers**:

- High false-positive rate undermining referral credibility
- Referrals lacking sufficient evidence for criminal investigation
- Volume of referrals exceeding NCA investigation capacity
- Data protection restrictions preventing sharing of specific data types with law enforcement

**Related Stakeholders**: SFO (complex fraud), HMRC (prosecution capability), ICO (law enforcement data sharing basis)

---

## Driver-to-Goal Mapping

### Goal G-1: Detect GBP 100M+ in Previously Undetected Cross-Government Fraud Within 2 Years

**Derived From Drivers**: SD-1, SD-2
**Goal Owner**: Head of Government Counter Fraud Function
**Goal Statement**: Identify at least GBP 100 million in previously undetected cross-government fraud (fraud patterns visible only through cross-departmental data matching) within 24 months of platform deployment.

**Success Metrics**:

- **Primary Metric**: Value of newly detected cross-government fraud (GBP)
- **Baseline**: Zero (no cross-government matching capability currently)
- **Target**: GBP 100M+ within 24 months
- **Measurement Method**: Validated fraud case values from departmental counter fraud teams

---

### Goal G-2: Onboard 10+ Departments as Active Data Contributors

**Derived From Drivers**: SD-1, SD-2
**Goal Owner**: Head of Government Counter Fraud Function
**Goal Statement**: Establish data sharing agreements and active data feeds from at least 10 government departments within 18 months.

**Success Metrics**:

- **Primary Metric**: Number of departments with active data feeds
- **Baseline**: Limited bilateral arrangements between HMRC and DWP
- **Target**: 10+ departments
- **Measurement Method**: Platform data source registry

---

### Goal G-3: Maintain False Positive Rate Below 5%

**Derived From Drivers**: SD-3, SD-4
**Goal Owner**: Counter Fraud Centre of Expertise
**Goal Statement**: Maintain fraud alert false positive rate below 5% to ensure citizen rights are protected and investigator time is not wasted on false leads.

**Success Metrics**:

- **Primary Metric**: False positive rate (alerts investigated that are not fraud)
- **Target**: Below 5%
- **Measurement Method**: Audit of alert outcomes by counter fraud teams

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| Minister | SD-1 | Reduce fraud tax on public services | G-1 | GBP 100M+ detection |
| Minister | SD-1 | Reduce fraud tax on public services | G-2 | 10+ dept data sharing |
| HMRC/DWP | SD-2 | Cross-government intelligence | G-1 | GBP 100M+ detection |
| HMRC/DWP | SD-2 | Cross-government intelligence | G-2 | 10+ dept data sharing |
| ICO | SD-3 | Proportionate, lawful processing | G-3 | Sub-5% false positive |
| NCA | SD-4 | Intelligence-grade referrals | G-1 | GBP 100M+ detection |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: HMRC/DWP (SD-2) want comprehensive data sharing for maximum detection capability, while ICO (SD-3) requires data minimisation and proportionality assessment for each data type.
  - **Resolution Strategy**: Tiered data sharing — Tier 1 (identity matching data) shared broadly with clear legal basis; Tier 2 (detailed financial data) shared only for confirmed match investigation with additional safeguards. Each tier has a specific DPIA and ICO consultation.

- **Conflict 2**: NCA (SD-4) wants intelligence-grade referrals suitable for criminal prosecution, while ICO (SD-3) requires limits on data shared with law enforcement.
  - **Resolution Strategy**: Two-stage process — analytics platform identifies fraud patterns and alerts departmental counter fraud teams (administrative purpose, data protection basis: public task). Departments then make individual decisions to refer to NCA under separate law enforcement data sharing powers (LED provisions of DPA 2018).

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Government Counter Fraud Functional Standard (GovS 013) | Standard | Cabinet Office | Counter fraud requirements for departments | N/A — external reference |
| Cross-Government Fraud Landscape Annual Report | Report | Cabinet Office | GBP 33-58B annual fraud estimate | N/A — external reference |
| Digital Economy Act 2017 | Legislation | legislation.gov.uk | Data sharing powers for fraud prevention | N/A — external reference |
| Bounce Back Loan Scheme fraud | NAO Report | NAO | GBP 4.9B estimated fraud | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Anti-Fraud Analytics Platform
**Model**: Claude Opus 4.6
