# Project Requirements: Energy Performance Certificate System

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
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
| **Distribution** | DLUHC Programme Board, DESNZ, Accreditation Bodies |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the digital Energy Performance Certificate (EPC) system covering assessment lodgement, the public register, SAP 11 calculation engine, and MEES enforcement APIs.

---

## Executive Summary

### Business Context

The Energy Performance Certificate system rates the energy efficiency of buildings on a scale from A (most efficient) to G (least efficient). EPCs are legally required for property sales, lettings, and new builds under the Energy Performance of Buildings Regulations 2012. Approximately 1.5 million assessments are lodged annually. The existing register infrastructure, operated by contracted providers (Landmark and Quidos), needs modernisation to support the SAP 11 methodology transition, MEES enforcement automation, and integration with the wider building decarbonisation agenda.

### Objectives

- Replace the current EPC register with a modern, API-first digital platform
- Implement the SAP 11 energy assessment calculation engine
- Enable automated MEES compliance checking for local authority enforcement
- Provide a public-facing EPC lookup service integrated with GOV.UK
- Deliver analytics for building decarbonisation policy evaluation

### Expected Outcomes

- 1.5 million assessments processed annually with <24 hour turnaround
- 10x improvement in MEES enforcement rate (from 1% to 10% of non-compliant properties receiving enforcement action)
- Accurate national building energy efficiency dataset supporting Net Zero policy targeting
- Reduced assessor lodgement costs through digital-first workflow

---

## Business Requirements

### BR-1: EPC Assessment Lodgement

**Description**: The system must accept, validate, and store EPC assessment data from accredited assessors via approved assessor software.
**Success Criteria**: 1.5M assessments per year processed; <24 hour turnaround from submission to certificate availability
**Priority**: MUST_HAVE
**Stakeholder**: DLUHC Building Safety Division

### BR-2: Public EPC Register

**Description**: The system must provide a public-facing service for consumers, conveyancers, and estate agents to look up EPC ratings by address or certificate number.
**Success Criteria**: 99.9% availability; search results within 2 seconds; WCAG 2.2 AA compliant
**Priority**: MUST_HAVE
**Stakeholder**: Homebuyers, estate agents, mortgage lenders

### BR-3: SAP 11 Calculation Engine

**Description**: The system must implement the SAP 11 methodology as a validated calculation engine that assessor software can use for consistent EPC rating determination.
**Success Criteria**: 100% compliance with SAP 11 specification; validated against BRE reference implementation; certified by DLUHC
**Priority**: MUST_HAVE
**Stakeholder**: DLUHC Building Safety Division, assessors

### BR-4: MEES Compliance API

**Description**: The system must provide APIs for local authorities to check MEES compliance of privately rented properties, supporting enforcement of minimum EPC C by 2028.
**Success Criteria**: API available to all 333 local authorities in England; response time <1 second; coverage of 4.4M PRS properties
**Priority**: MUST_HAVE
**Stakeholder**: DLUHC, local authorities

---

## Functional Requirements

### FR-1: Assessment Data Ingestion

**Description**: Accept EPC assessment data from approved assessor software via a standardised API.

**Acceptance Criteria**:
- [ ] Given an accredited assessor submitting via approved software, when assessment data is submitted, then it is validated against SAP 11 schema and accepted or rejected with specific error codes within 30 seconds
- [ ] Given a valid submission, when processed, then an EPC certificate number is generated and the certificate is available on the public register within 24 hours
- [ ] Given a submission from non-accredited software, when received, then it is rejected with an appropriate error message

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

### FR-2: SAP 11 Calculation API

**Description**: Provide a RESTful API implementing the SAP 11 energy assessment methodology for use by assessor software.

**Acceptance Criteria**:
- [ ] Given building characteristics (dimensions, insulation, heating system, ventilation), when submitted to the calculation API, then the correct SAP rating (1-100) and EPC band (A-G) are returned within 5 seconds
- [ ] Given the BRE SAP 11 reference test cases, when processed, then results match the reference implementation within 0.1% tolerance
- [ ] Given a calculation request, when processed, then the full breakdown of energy demand by component is returned for the certificate

**Priority**: MUST_HAVE
**Complexity**: HIGH

### FR-3: Public Register Search

**Description**: Allow the public to search for EPCs by postcode, address, or certificate reference number.

**Acceptance Criteria**:
- [ ] Given a valid postcode, when searched, then all EPCs for that postcode are returned ranked by most recent
- [ ] Given a certificate number, when searched, then the full EPC certificate is displayed including rating, recommendations, and environmental impact
- [ ] Given an address search, when a current valid EPC exists, then it is displayed prominently with validity date and MEES status indicator

**Priority**: MUST_HAVE
**Complexity**: LOW

### FR-4: MEES Compliance Checker

**Description**: Provide an API and web interface for local authorities to check whether a privately rented property meets MEES requirements.

**Acceptance Criteria**:
- [ ] Given a property UPRN (Unique Property Reference Number), when queried by an authenticated local authority user, then the system returns current EPC rating, MEES compliance status, and exemption status
- [ ] Given a batch of property UPRNs, when submitted, then MEES compliance status is returned for all within 30 seconds for batches up to 1,000 properties
- [ ] Given a non-compliant property, when identified, then the system provides the recommended improvements and estimated cost to reach EPC C

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

### FR-5: Assessor Accreditation Verification

**Description**: Verify assessor accreditation status in real-time during assessment lodgement.

**Acceptance Criteria**:
- [ ] Given an assessor ID, when submitted with an assessment, then accreditation status is verified against accreditation body registers in real-time
- [ ] Given an expired or revoked accreditation, when detected, then the assessment submission is rejected with appropriate notification

**Priority**: MUST_HAVE
**Complexity**: LOW

---

## Non-Functional Requirements

### NFR-P-1: Register Search Performance

**Requirement**: Public register search must return results within 2 seconds (p95). Assessment lodgement API must respond within 30 seconds (p95).
**Priority**: HIGH

### NFR-P-2: Assessment Volume

**Requirement**: Support 1.5 million assessments per year with peak capacity of 15,000 per day (property transaction peaks in spring/autumn).
**Priority**: HIGH

### NFR-A-1: Register Availability

**Requirement**: 99.9% uptime for public register (8.7 hours maximum downtime per year). The register is a dependency for property transactions and must not block conveyancing.
**RTO**: 1 hour. **RPO**: 1 hour.
**Priority**: CRITICAL

### NFR-SEC-1: Data Protection

**Requirement**: UK GDPR compliance. EPC data includes property addresses linked to energy characteristics — classified as OFFICIAL. Assessor personal data classified as OFFICIAL-SENSITIVE. All data stored in UK sovereign infrastructure.
**Priority**: CRITICAL

### NFR-U-1: Accessibility

**Requirement**: Public register must achieve WCAG 2.2 Level AA. Welsh language support for the public interface.
**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Assessor Software Systems

**Purpose**: Receive assessment data from accredited assessor software (Elmhurst, Stroma, ECMK, etc.).
**Integration Type**: RESTful API with assessor software certification programme
**Priority**: CRITICAL

### INT-2: Accreditation Body Registers

**Purpose**: Verify assessor accreditation status in real-time.
**Integration Type**: RESTful API query to each accreditation body
**Priority**: MUST_HAVE

### INT-3: AddressBase (Ordnance Survey)

**Purpose**: Address matching and UPRN lookup for property identification.
**Integration Type**: Batch and real-time API
**Priority**: MUST_HAVE

### INT-4: Local Authority Enforcement Systems

**Purpose**: Provide MEES compliance data to local authority housing enforcement teams.
**Integration Type**: RESTful API (GDS-standard) with local authority authentication
**Priority**: MUST_HAVE

### INT-5: DESNZ Policy Analytics

**Purpose**: Provide anonymised EPC analytics for building decarbonisation policy evaluation.
**Integration Type**: Scheduled data export and analytics API
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Entity: EPC Certificate

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| certificate_number | String(24) | Yes | Unique EPC reference (e.g., 1234-5678-9012-3456-7890) |
| uprn | String(12) | Yes | Unique Property Reference Number |
| address | Object | Yes | Full address including postcode |
| sap_rating | Integer(1-100) | Yes | SAP 11 energy efficiency rating |
| epc_band | Enum(A-G) | Yes | EPC band derived from SAP rating |
| environmental_impact | Integer(1-100) | Yes | CO2 emissions rating |
| assessment_date | Date | Yes | Date of assessment |
| valid_until | Date | Yes | Expiry date (10 years from assessment) |
| assessor_id | String | Yes | Accredited assessor reference |
| property_type | Enum | Yes | Detached/Semi/Terrace/Flat/Bungalow |
| recommendations | Array[Object] | Yes | Energy improvement recommendations with estimated costs and savings |

**Data Volume**: 1.5M new certificates/year; 25M+ historical certificates in register

**Data Retention**: 10 years (aligned with EPC validity period); historical certificates retained indefinitely for trend analysis

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Assessment turnaround | 3-5 days | <24 hours | 6 months post-launch |
| Register search response | 5 seconds | <2 seconds | Launch |
| MEES enforcement rate | 1% | 10% | 24 months post-launch |
| SAP 11 calculation accuracy | N/A | 100% match to BRE reference | Launch |
| Local authority API adoption | 0 | 200+ councils | 24 months post-launch |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-003-STKE-v1.0 | Stakeholder Analysis | This programme | Stakeholder drivers | `projects/003-energy-performance-certificate-system/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 7 Programme | Governing principles | `projects/000-global/` |
| SAP 11 Methodology | Technical | BRE | Calculation methodology | N/A — external reference |
| Energy Performance of Buildings Regulations 2012 | Legislation | legislation.gov.uk | Legal framework | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Energy Performance Certificate System (Project 003)
**Model**: Claude Opus 4.6 (1M context)
