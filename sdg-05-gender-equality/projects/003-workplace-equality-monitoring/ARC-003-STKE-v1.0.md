# Stakeholder Drivers & Goals Analysis: Workplace Equality Monitoring

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Workplace Equality Monitoring (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Workplace Equality Platform, EHRC |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | EHRC Board, EHRC Digital, GEO, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Workplace Equality Monitoring platform, which will enable the EHRC to monitor employer compliance with workplace equality duties under the Equality Act 2010, including the Public Sector Equality Duty (PSED), reasonable adjustment obligations, and discrimination complaint patterns.

### Key Findings

The strongest alignment exists around the need for a systematic, data-driven approach to equality monitoring — currently, EHRC relies heavily on reactive complaint handling rather than proactive pattern detection. The primary tension lies between EHRC's enforcement ambition (robust monitoring enabling targeted investigations) and employer concerns about regulatory burden and the risk of false-positive enforcement triggers. Trade unions strongly support enhanced monitoring but want employee-accessible transparency tools, which employers resist.

### Critical Success Factors

- EHRC can identify employers with systemic equality compliance failures through automated pattern detection
- Public sector bodies can demonstrate PSED compliance through the platform rather than separate processes
- Employers experience reduced reporting burden through integration with existing data sources (pay gap data, workforce diversity returns)
- Platform passes EHRC Board review for proportionality and fairness

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the principle of better equality monitoring. Tension between enforcement-oriented monitoring (EHRC, TUC) and employer concern about proportionality and burden.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| EHRC Chair | Strategic oversight | HIGH | HIGH | Manage Closely — Board governance |
| EHRC Chief Executive | Operational leadership | HIGH | HIGH | Manage Closely — Programme board |
| SRO, Workplace Equality Platform | Programme accountability | HIGH | HIGH | Manage Closely — Weekly governance |
| EHRC Enforcement Director | Enforcement strategy | HIGH | HIGH | Manage Closely — Enforcement requirements |
| EHRC Legal Director | Legal powers and constraints | HIGH | MEDIUM | Keep Satisfied — Legal basis review |
| EHRC Research and Analysis | Data and evidence requirements | MEDIUM | HIGH | Keep Informed — Analytics design |
| EHRC Digital | Technical delivery | MEDIUM | HIGH | Keep Informed — Architecture, sprints |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| GEO (Government Equalities Office) | Cabinet Office | Policy partner | HIGH | HIGH |
| Minister for Women and Equalities | Government | Ministerial sponsor | HIGH | MEDIUM |
| CDDO | Cabinet Office | Spend control | HIGH | MEDIUM |
| Employer bodies (CBI, IoD) | Private sector | Regulated entities | MEDIUM | HIGH |
| Trade unions (TUC, Unite) | Unions | Worker advocacy | MEDIUM | HIGH |
| Public sector employers | Government departments, LAs, NHS Trusts | PSED duty holders | LOW | HIGH |
| Employment Tribunal Service | MoJ | Adjudication | MEDIUM | MEDIUM |
| ACAS | Conciliation body | Dispute resolution | LOW | MEDIUM |
| Employees/workers | Citizens | Protected persons | LOW | HIGH |
| Disability Rights UK | Charity | Reasonable adjustments | LOW | HIGH |
| Stonewall | Charity | Sexual orientation/gender identity | LOW | HIGH |

---

## Stakeholder Drivers Analysis

### SD-1: EHRC Enforcement Director — Proactive, Evidence-Based Enforcement

**Stakeholder**: EHRC Enforcement Director

**Driver Category**: STRATEGIC / COMPLIANCE

**Driver Statement**: Shift EHRC enforcement from a predominantly reactive, complaint-driven model to a proactive, data-driven approach that identifies employers with systemic equality failures before they reach employment tribunal, enabling targeted use of EHRC's limited enforcement powers for maximum impact.

**Context & Background**:
EHRC has finite enforcement resources (Section 20 investigations, Section 23 agreements, Section 24 applications to court). Currently, enforcement targets are identified through media coverage, complaints, and ad hoc analysis rather than systematic data. The EHRC Strategic Plan 2022-2025 committed to "data-driven enforcement prioritisation". EHRC's last comprehensive monitoring report on employer compliance was published in 2019 — there is no systematic, ongoing monitoring capability.

**Driver Intensity**: CRITICAL

**Enablers**:

- Automated ingestion of equality data from multiple sources (pay gap reports, workforce diversity returns, tribunal outcomes)
- Pattern detection algorithms identifying clusters of complaints, high pay gaps, or absent PSED evidence
- Risk-scoring framework enabling enforcement resource prioritisation

**Blockers**:

- Legal proportionality concerns — automated risk scoring could be challenged judicially
- Data availability — many employers do not report beyond mandatory minimum
- Employer resistance to what they perceive as "surveillance"

---

### SD-2: Employer Bodies (CBI, IoD) — Proportionate, Supportive Regulation

**Stakeholder**: CBI, IoD

**Driver Category**: OPERATIONAL / COMPLIANCE

**Driver Statement**: Ensure that workplace equality monitoring is proportionate, does not create excessive reporting burden, integrates with existing reporting obligations (gender pay gap, PSED), and provides employers with constructive guidance alongside enforcement.

**Context & Background**:
Employers already face multiple equality reporting obligations — gender pay gap reporting, PSED annual reporting (for public sector), workforce diversity questionnaires, and tribunal responses. The CBI has consistently argued for regulatory streamlining and a "report once" principle. Employers fear that a monitoring platform could generate false-positive enforcement triggers based on incomplete data, leading to reputational damage before any finding of non-compliance.

**Driver Intensity**: HIGH

---

### SD-3: Trade Unions (TUC) — Transparency and Accountability

**Stakeholder**: TUC, Unite, Unison

**Driver Category**: ADVOCACY / STRATEGIC

**Driver Statement**: Ensure the platform provides meaningful transparency that enables workers and their representatives to hold employers accountable on equality, including access to employer equality data, complaint patterns, and PSED compliance status.

**Driver Intensity**: HIGH

---

### SD-4: Public Sector Employers — PSED Compliance Simplification

**Stakeholder**: Government departments, NHS Trusts, local authorities

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Simplify Public Sector Equality Duty compliance by providing a standardised reporting framework and evidence repository that replaces the current patchwork of inconsistent departmental approaches.

**Context & Background**:
The PSED requires public bodies to have due regard to eliminating discrimination, advancing equality, and fostering good relations. However, there is no standardised format for demonstrating compliance, leading to inconsistent quality. Some departments produce comprehensive equality analyses; others treat PSED as a tick-box exercise. A standardised platform would raise the quality floor and reduce the effort of bespoke compliance processes.

**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Automated Compliance Risk Identification

**Derived From Drivers**: SD-1

**Goal Owner**: EHRC Enforcement Director

**Goal Statement**: Enable EHRC to automatically identify the 50 highest-risk employers for equality compliance investigation each year through algorithmic analysis of available equality data, tribunal outcomes, and complaint patterns.

**Success Metrics**:

- **Primary Metric**: Number of enforcement actions initiated from platform-identified targets vs. reactive complaints
- **Target**: 60% of enforcement targets identified proactively within 24 months

---

### Goal G-2: Unified Equality Reporting for Employers

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: EHRC Research and Analysis Director

**Goal Statement**: Provide a single reporting interface where employers submit equality data once, satisfying multiple obligations (pay gap reporting feed, PSED evidence, workforce diversity reporting) without duplicate data entry.

**Success Metrics**:

- **Primary Metric**: Employer satisfaction with reporting process
- **Target**: 60% employer satisfaction (up from no systematic measurement)

---

### Goal G-3: Public Equality Transparency Dashboard

**Derived From Drivers**: SD-3

**Goal Owner**: EHRC Communications Director

**Goal Statement**: Publish a public-facing dashboard showing employer equality performance indicators, enabling workers, unions, and civil society to assess and compare employer records on equality.

**Success Metrics**:

- **Primary Metric**: Monthly unique visitors to transparency dashboard
- **Target**: 50,000 monthly unique visitors within 12 months

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary |
|-------------|-----------|----------------|---------|--------------|
| EHRC Enforcement | SD-1 | Proactive enforcement | G-1 | Automated risk identification |
| Employers (CBI) | SD-2 | Proportionate monitoring | G-2 | Unified reporting |
| TUC | SD-3 | Transparency | G-3 | Public dashboard |
| Public sector | SD-4 | PSED simplification | G-2 | Unified reporting |

### Conflict Analysis

- **Conflict 1**: EHRC Enforcement (SD-1) wants comprehensive monitoring data but Employers (SD-2) want minimal reporting burden
  - **Resolution Strategy**: Integrate with existing data sources (pay gap platform, Companies House) rather than creating new reporting obligations. Additional data collected on a voluntary basis with opt-in incentives (e.g., "Equality Mark" accreditation).

- **Conflict 2**: TUC (SD-3) wants maximum transparency but Employers (SD-2) fear reputational damage from incomplete data
  - **Resolution Strategy**: Published data uses validated, contextualised metrics rather than raw data. Employers can add narrative context. EHRC risk scores are internal-only (not published).

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Equality Act 2010 | Legislation | legislation.gov.uk | Protected characteristics, PSED, enforcement powers | N/A |
| EHRC Strategic Plan 2022-2025 | Strategy | EHRC | Enforcement priorities, data-driven approach | N/A |
| EHRC Enforcement Policy | Policy | EHRC | Investigation and compliance powers | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Workplace Equality Monitoring (Project 003)
**Model**: Claude Opus 4.6
