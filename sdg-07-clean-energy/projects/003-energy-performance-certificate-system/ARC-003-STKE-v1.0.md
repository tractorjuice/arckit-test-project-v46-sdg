# Stakeholder Drivers & Goals Analysis: Energy Performance Certificate System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Energy Performance Certificate System (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, EPC System Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Programme Board, DESNZ, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies stakeholders for the digital transformation of the Energy Performance Certificate (EPC) system — the rating framework that measures building energy efficiency across England and Wales. The platform will replace the current register and assessment lodgement infrastructure, implementing the updated SAP 11 methodology and enabling the Minimum Energy Efficiency Standards (MEES) regulatory framework.

### Key Findings

The EPC system sits at a critical juncture: the transition from SAP 10 to SAP 11 methodology, increasing MEES requirements (minimum EPC rating C for rented properties by 2028), and growing recognition that EPCs must evolve beyond a transaction-triggered assessment to a living building energy profile. The strongest alignment is between DLUHC's regulatory enforcement needs and DESNZ's Net Zero building decarbonisation targets. The key tension is between property owners (who bear improvement costs) and tenants/buyers (who benefit from energy-efficient homes). Assessor quality and consistency remains a persistent challenge.

### Critical Success Factors

- Process 1.5 million EPC assessments annually with <24 hour turnaround from assessment to lodgement
- Implement SAP 11 methodology accurately and consistently across all assessor software
- Enable automated MEES compliance checking for local authority enforcement
- Maintain public register availability for property transactions (used by conveyancers, mortgage lenders, estate agents)
- Achieve WCAG 2.2 AA accessibility for the public-facing register

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Broad agreement on the need for EPC system modernisation, but tensions between landlords (cost of improvements), assessors (methodology changes affecting business), local authorities (enforcement resource constraints), and DLUHC/DESNZ (ambition to raise minimum standards).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DLUHC Minister for Housing | Ministerial sponsor | HIGH | HIGH | Manage Closely — MEES policy |
| DLUHC Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, EPC System | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly governance |
| DLUHC Digital Director | Technology leadership | HIGH | HIGH | Manage Closely — Architecture |
| DLUHC Building Safety Division | EPC policy ownership | HIGH | HIGH | Manage Closely — SAP methodology |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DESNZ | Partner department | Building decarbonisation policy | HIGH | HIGH |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| Energy assessors (DEAs) | Accredited professionals | Assessment data sources | MEDIUM | HIGH |
| Accreditation bodies (Elmhurst, Stroma, etc.) | Industry | Assessor quality assurance | MEDIUM | HIGH |
| Local authorities (333 in England) | Enforcement bodies | MEES enforcement | MEDIUM | HIGH |
| Property owners/landlords | Regulated parties | Must obtain EPCs, meet MEES | LOW | HIGH |
| Homebuyers and tenants | Consumers | Use EPC data for decisions | LOW | HIGH |
| Estate agents | Industry | Require EPC for marketing | LOW | HIGH |
| Mortgage lenders | Financial institutions | Use EPC for lending decisions | MEDIUM | MEDIUM |
| Register operators (Landmark/Quidos) | Current contractors | Operate existing register | MEDIUM | HIGH |

---

## Stakeholder Drivers Analysis

### SD-1: DLUHC — Enforce Minimum Energy Efficiency Standards

**Stakeholder**: DLUHC Minister for Housing
**Driver Category**: COMPLIANCE
**Driver Statement**: Enforce the Minimum Energy Efficiency Standards (MEES) requiring all rented properties to achieve EPC rating C by 2028, supporting the UK's building decarbonisation targets. Enforcement requires a reliable, digital-first EPC system that local authorities can query programmatically.
**Driver Intensity**: CRITICAL

### SD-2: DESNZ — Building Decarbonisation Data

**Stakeholder**: DESNZ
**Driver Category**: STRATEGIC
**Driver Statement**: Use EPC data to track building energy efficiency improvements nationally, target retrofit programmes (Green Homes Grant, ECO), and measure progress toward Net Zero buildings. Current EPC data quality and coverage gaps limit policy effectiveness.
**Driver Intensity**: HIGH

### SD-3: Energy Assessors — Methodology Transition

**Stakeholder**: Domestic Energy Assessors (DEAs)
**Driver Category**: OPERATIONAL
**Driver Statement**: Transition to SAP 11 methodology with minimal disruption to assessment workflows, fair pricing for lodgement, and confidence that the new system accurately reflects assessment quality.
**Driver Intensity**: HIGH

### SD-4: Property Owners — Cost of Compliance

**Stakeholder**: Landlords and property owners
**Driver Category**: FINANCIAL
**Driver Statement**: Minimise the cost and administrative burden of EPC compliance. Landlords face significant costs to improve properties to EPC C (average £5,000-£10,000 per property). They want an EPC system that is accurate, consistent, and does not penalise them unfairly.
**Driver Intensity**: HIGH

### SD-5: Local Authorities — Enforcement Capability

**Stakeholder**: 333 local authorities in England
**Driver Category**: COMPLIANCE
**Driver Statement**: Gain programmatic access to EPC data for MEES enforcement. Currently, enforcement is manual, resource-intensive, and inconsistent across councils. Only 1% of non-compliant landlords have been fined since MEES was introduced in 2018.
**Driver Intensity**: MEDIUM

---

## Driver-to-Goal Mapping

### Goal G-1: Digital-First EPC Register

**Derived From Drivers**: SD-1, SD-2, SD-5
**Goal Owner**: DLUHC Digital Director
**Goal Statement**: Deliver a modern, API-first EPC register that processes 1.5 million assessments annually with <24 hour turnaround, provides automated MEES compliance checking, and exposes data via GDS-standard APIs by Q2 2028.

### Goal G-2: SAP 11 Methodology Implementation

**Derived From Drivers**: SD-1, SD-3
**Goal Owner**: DLUHC Building Safety Division
**Goal Statement**: Implement the SAP 11 energy assessment methodology in the new platform, with validated calculation engine, assessor software certification, and transition plan from SAP 10, by Q4 2027.

### Goal G-3: MEES Enforcement Automation

**Derived From Drivers**: SD-1, SD-5
**Goal Owner**: DLUHC Building Safety Division
**Goal Statement**: Enable automated MEES compliance checking for all 4.4 million privately rented properties in England, with API access for local authority enforcement systems, by Q1 2028.

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DLUHC Minister | SD-1 | MEES enforcement | G-1 | Digital EPC register | O-1 | EPC C compliance by 2028 |
| DLUHC Minister | SD-1 | MEES enforcement | G-3 | Enforcement automation | O-1 | EPC C compliance by 2028 |
| DESNZ | SD-2 | Building decarb data | G-1 | Digital EPC register | O-2 | Net Zero buildings tracking |
| Assessors | SD-3 | Methodology transition | G-2 | SAP 11 implementation | O-3 | Consistent EPC ratings |
| Property owners | SD-4 | Cost of compliance | G-2 | SAP 11 implementation | O-3 | Consistent EPC ratings |
| Local authorities | SD-5 | Enforcement capability | G-3 | Enforcement automation | O-1 | EPC C compliance by 2028 |

### Conflict Analysis

- **Conflict 1**: DLUHC (SD-1) wants strict MEES enforcement, but property owners (SD-4) face significant improvement costs (£5,000-£10,000 per property).
  - **Resolution Strategy**: Phased compliance timeline with grace periods; link to Green Homes Grant funding for improvement costs; accurate EPCs ensure owners are not unfairly rated.

- **Conflict 2**: DESNZ (SD-2) wants comprehensive EPC data for policy analytics, but assessors (SD-3) are concerned about increased data collection burden and methodology complexity.
  - **Resolution Strategy**: Streamlined digital assessment tools that reduce assessor burden while capturing richer data; assessor software certification to ensure consistency.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Energy Performance of Buildings Regulations 2012 | Legislation | legislation.gov.uk | EPC legal framework | N/A |
| SAP 11 Methodology | Technical | BRE | Building energy assessment methodology | N/A |
| Domestic MEES Regulations | Legislation | legislation.gov.uk | Minimum EPC rating requirements | N/A |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Energy Performance Certificate System (Project 003)
**Model**: Claude Opus 4.6 (1M context)
