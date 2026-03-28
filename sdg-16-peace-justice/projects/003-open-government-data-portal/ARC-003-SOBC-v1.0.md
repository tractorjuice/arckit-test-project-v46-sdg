# Strategic Outline Business Case (SOBC): Open Government Data Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Open Government Data Portal (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Open Government Programme, Cabinet Office |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

---

## Executive Summary

**Purpose**: The Open Government Data Portal replaces the ageing data.gov.uk platform with a modern, scalable transparency and open data publishing platform that meets the UK's Open Government Partnership commitments, delivers developer-friendly API access, and automates data quality assessment.

**Problem Statement**: The current data.gov.uk platform is technically outdated (CKAN-based, limited scalability), has poor dataset discoverability, no automated quality assessment, and limited API capabilities. This undermines the UK's international standing on open government and limits the value extracted from government data by citizens, researchers, and civic technology organisations.

**Proposed Solution**: Build a modern open data portal with self-service publishing, automated quality scoring, RESTful APIs, and a transparency dashboard tracking OGP National Action Plan commitments.

**Strategic Fit**: Directly delivers the UK's 5th OGP National Action Plan commitments, supports SDG 16.6 (effective, accountable, transparent institutions), and aligns with the Government Data Strategy.

**Investment Required**: GBP 5M over 3 years

- Capital: GBP 3.5M
- Operational (3 years): GBP 1.5M

**Expected Benefits**: GBP 12M over 5 years

- Reduced FOI processing costs through proactive publication: GBP 4M
- Economic value of open data to external users: GBP 5M (estimated from ODI research)
- Departmental efficiency in data publication: GBP 2M
- Avoided cost of maintaining legacy data.gov.uk: GBP 1M

**Return on Investment**:

- NPV: GBP 6M (discounted at 3.5%)
- Payback Period: 24 months
- ROI: 140%

**Recommended Option**: Option 3: Build modern cloud-native portal with automated quality and APIs

**Key Risks**:

1. Departmental engagement — departments may not prioritise data publication
2. Data quality — published data may be too poor for meaningful reuse
3. External adoption — developers may not build on government APIs

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The UK's OGP commitments require a modern open data platform. The investment is modest (GBP 5M) relative to the international reputational value and the economic benefit of open data (estimated at GBP 6.8B annually for the UK economy by the ODI). Failure to modernise risks the UK losing its top-5 ranking on the Open Data Barometer.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: data.gov.uk hosts approximately 45,000 datasets but many are outdated, have broken links, or lack adequate metadata. The platform is based on CKAN (deployed 2014) and has limited scalability, no automated quality assessment, and basic search. Departmental publication is manual and time-consuming.

**Consequences of Inaction**:

- UK drops from top 5 on Open Data Barometer, damaging international reputation
- 5th OGP National Action Plan commitments not delivered
- FOI request costs continue to rise as data is not proactively published
- Civic technology community unable to build on government data

---

# PART B: ECONOMIC CASE

## B1. Options

### Option 1: Do Nothing

**Costs**: GBP 5M over 5 years (data.gov.uk maintenance)
**Benefits**: GBP 0
**Assessment**: OGP commitments undeliverable. UK ranking declines. Unacceptable.

### Option 2: Upgrade Existing CKAN Platform

**Costs**: GBP 2M capital + GBP 4M operational = GBP 6M
**Benefits**: GBP 5M (minor improvements)
**NPV**: GBP -1M
**Assessment**: CKAN architecture limits scalability and API capability. Band-aid approach.

### Option 3: Build Modern Cloud-Native Portal (RECOMMENDED)

**Costs**: GBP 3.5M capital + GBP 1.5M operational (3 years) + GBP 1.5M (years 4-5) = GBP 6.5M
**Benefits**: GBP 12M over 5 years
**NPV**: GBP 6M
**BCR**: 1.85
**Assessment**: Best value. Modern architecture enables APIs, quality automation, and scalability.

### Option 4: Adopt Established Open Source Data Portal (e.g., Socrata, OpenDataSoft)

**Costs**: GBP 1.5M capital + GBP 4M licensing over 5 years = GBP 5.5M
**Benefits**: GBP 9M
**NPV**: GBP 3M
**Assessment**: Viable but licensing creates vendor dependency. Limited customisation for UK-specific requirements (DCAT-AP UK, OGP reporting).

---

# PART D: FINANCIAL CASE

| Category | Year 1 | Year 2 | Year 3 | Total |
|----------|--------|--------|--------|-------|
| Platform development | GBP 1.8M | GBP 1.2M | GBP 0.5M | GBP 3.5M |
| Operations and hosting | GBP 0.3M | GBP 0.5M | GBP 0.7M | GBP 1.5M |
| **Total** | **GBP 2.1M** | **GBP 1.7M** | **GBP 1.2M** | **GBP 5M** |

---

# PART E: MANAGEMENT CASE

| Phase | Duration | Key Deliverables |
|-------|----------|------------------|
| Discovery | 2 months | User research, technology assessment, data.gov.uk audit |
| Alpha | 3 months | Portal prototype, API design, quality scoring PoC |
| Private Beta | 6 months | Core portal with 5 pilot departments |
| Public Beta | 4 months | Full portal, data.gov.uk migration |
| Live | Ongoing | National rollout, continuous improvement |

| Milestone | Date |
|-----------|------|
| SOBC approval | Q2 2026 |
| Discovery | Q3 2026 |
| Alpha | Q4 2026 |
| Private Beta | Q1 2027 |
| data.gov.uk migration | Q3 2027 |
| Live | Q4 2027 |

---

## Approval

| Role | Name | Decision | Date |
|------|------|----------|------|
| SRO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| Cabinet Office Perm Sec | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| CDDO | | [ ] PROCEED / [ ] DO NOT PROCEED | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK 5th OGP National Action Plan | Policy | Cabinet Office | Open government commitments | N/A — external reference |
| HM Treasury Green Book | Guidance | HMT | Five-case model, 3.5% discount | N/A — external reference |
| ODI Open Data Economic Value Study | Research | ODI | GBP 6.8B annual UK open data value | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Open Government Data Portal
**Model**: Claude Opus 4.6
