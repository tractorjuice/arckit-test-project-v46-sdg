# Project Requirements: Waste Management Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Waste Management Analytics (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Waste Management Analytics |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Environment Agency, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Waste Management Analytics platform — a DEFRA-owned national waste tracking and reporting platform that digitises waste transfer notes, aggregates waste data from local authorities and waste operators, and provides analytics for enforcement, policy evaluation, and operational optimisation.

---

## Executive Summary

### Business Context

England produces approximately 220 million tonnes of waste annually, yet the national waste data infrastructure relies on paper-based waste transfer notes, manual WasteDataFlow returns from 333 local authorities, and waste statistics published with a 2-year lag. The Environment Agency cannot detect waste crime patterns in near-real-time. Local authorities cannot benchmark their recycling performance against comparable councils. DEFRA's policy team cannot evaluate whether the Resources and Waste Strategy and Environment Act 2021 policies are working because the data arrives too late and at insufficient granularity.

The Waste Management Analytics platform will digitise the waste transfer note system, automate data collection from council waste management systems, and provide analytics that serve enforcement (EA), operations (councils), statistics (DEFRA), and policy evaluation (DEFRA).

### Objectives

- Digitise waste transfer notes across England, replacing 10 million+ paper WTNs annually
- Aggregate waste data from 333 local authorities with automated extraction (no manual re-keying)
- Reduce national waste statistics publication lag from 2 years to 3 months
- Provide the Environment Agency with near-real-time waste flow analytics for enforcement
- Deliver operational analytics that help local authorities optimise waste services

### Expected Outcomes

- 80% of local authorities generating digital WTNs within 18 months
- National waste statistics published quarterly with 3-month lag
- 30% increase in waste crime detection through analytics
- GBP 50M annual savings across local authorities through operational optimisation

### Project Scope

**In Scope**:

- Digital waste transfer note generation, storage, and retrieval
- Automated data ingestion from council waste management systems
- National waste analytics platform with dashboards for EA, councils, and DEFRA
- Waste flow anomaly detection for enforcement intelligence
- Local authority benchmarking and operational analytics
- Policy impact analytics (EPR, consistent collections, DRS evaluation)
- Integration with Circular Economy Marketplace (Project 002)

**Out of Scope**:

- Replacement of council waste management operational systems (collection routing, bin assignment)
- Hazardous waste consignment note system (separate regulatory regime)
- International waste shipment tracking (Basel Convention)
- Scotland, Wales, and Northern Ireland (devolved — Phase 2)

---

## Business Requirements

### BR-1: Digital Waste Transfer Note System

**Description**: Replace the paper-based waste transfer note system with a digital standard that meets duty of care requirements, provides tamper-evident audit trails, and is accessible to all waste producers, carriers, and receivers.

**Rationale**: Paper WTNs are easily falsified, frequently lost, and impossible to aggregate for analysis. Digitisation is the foundation for all waste tracking and enforcement capability.

**Success Criteria**:

- Digital WTNs generated for all marketplace transactions and directly by waste operators
- WTNs meet Environmental Protection (Duty of Care) Regulations 1991 requirements
- Tamper-evident audit trail for every WTN
- 10 million+ paper WTNs replaced annually

**Priority**: MUST_HAVE

---

### BR-2: Automated Data Collection from Local Authorities

**Description**: Automatically ingest waste data from local authority waste management systems without requiring manual data entry by council officers, using standardised APIs and adapters for major vendor systems.

**Rationale**: Manual WasteDataFlow reporting consumes officer time and introduces errors. Automated collection is essential for timeliness and data quality.

**Success Criteria**:

- Adapters for the 5 major council waste management systems (covering ~80% of councils)
- No manual re-keying required for councils using supported systems
- Data quality validation at point of ingestion
- WasteDataFlow reporting replaced (not duplicated)

**Priority**: MUST_HAVE

---

### BR-3: National Waste Analytics Platform

**Description**: Provide a multi-stakeholder analytics platform serving Environment Agency enforcement, local authority operational optimisation, DEFRA statistics production, and DEFRA policy evaluation — each with appropriate access controls and tailored dashboards.

**Rationale**: Different stakeholders need different views of the same data. A single platform with role-based access is more cost-effective and ensures data consistency.

**Success Criteria**:

- Role-based dashboards for EA (enforcement), councils (operations), DEFRA statistics, and DEFRA policy
- Quarterly national waste statistics publication with 3-month lag
- Waste flow anomaly detection for EA enforcement
- Local authority benchmarking against peer councils

**Priority**: MUST_HAVE

---

## Functional Requirements

### FR-1: Digital Waste Transfer Note Generation

**Description**: The system must generate digital waste transfer notes capturing all information required by duty of care regulations, with immutable audit trails and support for both web and mobile interfaces.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a waste transfer occurs, when the transferor initiates a digital WTN, then the system captures: waste description (EWC code), quantity (tonnes), date/time, transferor identity (with permit/licence), transferee identity (with permit/licence), collection/delivery point, special handling instructions
- [ ] Given a WTN is created, when both parties confirm, then the WTN is finalised with a tamper-evident hash and timestamp
- [ ] WTN creation supported via web interface and mobile app (for field operatives at waste transfer stations)
- [ ] Bulk WTN creation supported via CSV upload and API for high-volume operators

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-2: Council Waste Data Ingestion API

**Description**: The system must provide a standardised data ingestion API with pre-built adapters for major council waste management systems, enabling automated data collection without manual re-keying.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a council uses a supported waste management system (Whitespace, Bartec, Yotta, Contender, Alloy), when the adapter runs, then waste collection data is ingested automatically on a daily schedule
- [ ] Given a council uses an unsupported system, when they use the standardised API, then they can push data in the defined format
- [ ] Data ingestion validates against a defined schema: waste type (EWC code), collection method, tonnage, destination, recycling/disposal outcome
- [ ] Data quality issues flagged at ingestion with clear error messages to council data contacts

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-3: Waste Flow Anomaly Detection

**Description**: The system must analyse waste flow data to detect anomalous patterns indicative of waste crime — volume mismatches between production and disposal, impossible transport routes, unlicensed operators, and permitted capacity breaches.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given waste flow data is analysed, when a volume mismatch exceeds 20% between waste produced (WTN outgoing) and waste received (WTN incoming) for an operator, then an anomaly alert is generated for EA review
- [ ] Given an operator's received waste exceeds their permitted annual capacity by 10%, then a capacity breach alert is generated
- [ ] Given waste is transferred to an operator whose permit has expired or been revoked, then an immediate alert is generated
- [ ] Anomaly alerts triaged into HIGH (immediate action), MEDIUM (investigation within 7 days), LOW (monitoring) based on configurable risk scoring

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-4: Local Authority Benchmarking Dashboard

**Description**: The system must provide local authority waste officers with benchmarking dashboards comparing their council's performance against peer councils with similar characteristics (population, urbanisation, demographics, deprivation).

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a council officer accesses their dashboard, when they view benchmarks, then they see their recycling rate, contamination rate, residual waste per household, and cost per tonne compared to their peer group
- [ ] Peer groups defined by DEFRA classification (urban/rural, population band, deprivation quintile)
- [ ] Time series showing trends over 12 months, 3 years, and 5 years
- [ ] Drill-down capability into waste stream composition (dry recycling, food waste, garden waste, residual)

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

### FR-5: National Waste Statistics Production

**Description**: The system must produce quarterly national waste statistics meeting ONS quality standards, replacing the current annual WasteDataFlow publication with a 2-year lag.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given quarterly data collection is complete, when the statistics pipeline runs, then national waste statistics are produced within 3 months of the quarter end
- [ ] Statistics include: total waste arisings, recycling rate, landfill rate, energy recovery rate, by material type and by region
- [ ] Data quality assessment published alongside statistics (coverage rate, estimation methods used for non-reporting councils)
- [ ] Exportable in formats required by Eurostat, OECD, and UNFCCC waste reporting

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-6: Policy Impact Analytics

**Description**: The system must provide analytics tools enabling DEFRA policy teams to evaluate the impact of waste policies (EPR for packaging, consistent collections, deposit return scheme) by comparing waste outcomes before and after policy implementation at local authority level.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a policy implementation date and affected councils, when the analysis runs, then the system shows before/after comparison of relevant waste metrics
- [ ] Control group selection: councils not yet subject to the policy can serve as a control
- [ ] Seasonal adjustment applied to waste data (waste volumes vary seasonally)
- [ ] Results exportable for ministerial briefings and parliamentary reporting

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

### FR-7: Integration with Circular Economy Marketplace

**Description**: The system must consume material transfer events from the Circular Economy Marketplace (Project 002) to include marketplace-facilitated transfers in national waste flow tracking and reporting.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given a material transfer is completed on the Circular Economy Marketplace, when the transfer event is received, then the corresponding digital WTN data is ingested into the analytics platform
- [ ] Marketplace transfers tagged as circular economy outcomes in analytics (reuse, recycling, recovery)
- [ ] National statistics distinguish marketplace-facilitated circular economy transfers from conventional waste disposal

**Priority**: MUST_HAVE

**Complexity**: LOW

---

## Non-Functional Requirements

### NFR-P-1: Data Ingestion Performance

**Requirement**: Daily ingestion of waste data from 333 local authorities (estimated 500,000 records per day) completed within a 4-hour overnight processing window. Near-real-time WTN processing within 30 seconds.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability for WTN generation (waste transfers cannot wait). 99.5% for analytics dashboards (scheduled maintenance acceptable during off-peak hours).

**Priority**: CRITICAL

---

### NFR-SEC-1: EA Enforcement Data Access

**Requirement**: Environment Agency enforcement data access restricted to authorised EA officers. Anomaly alerts contain case references, not operator identities, until an investigation is formally opened. Data sharing agreement between DEFRA and EA in place before enforcement features go live.

**Priority**: CRITICAL

---

### NFR-SEC-2: Data Integrity

**Requirement**: All digital WTNs cryptographically hashed at creation. Hash chain maintained to detect any subsequent tampering. WTN data immutable once finalised.

**Priority**: CRITICAL

---

### NFR-U-1: Mobile Field Operations

**Requirement**: WTN generation interface usable on mobile devices at waste transfer stations and construction sites. Support offline WTN creation with synchronisation when connectivity returns.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Environment Agency Permits and Licences API

**Purpose**: Verify operator credentials for WTN generation and anomaly detection.

**Integration Type**: Real-time API

**Priority**: CRITICAL

---

### INT-2: Circular Economy Marketplace (Project 002)

**Purpose**: Consume material transfer events for national waste flow tracking.

**Integration Type**: Event-driven (consume marketplace transfer events)

**Priority**: MUST_HAVE

---

### INT-3: Council Waste Management Systems

**Purpose**: Automated data ingestion from council operational systems.

**Integration Type**: Batch (daily) via pre-built adapters and standardised API

**Systems**: Whitespace, Bartec, Yotta, Contender, Alloy (covering ~80% of councils)

**Priority**: MUST_HAVE

---

### INT-4: WasteDataFlow Replacement

**Purpose**: Replace existing WasteDataFlow reporting with automated data collection.

**Integration Type**: Data migration and parallel running during transition

**Priority**: MUST_HAVE

---

## Dependencies and Risks

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Council waste system heterogeneity prevents automated ingestion | HIGH | HIGH | Pre-built adapters for 5 major systems, standardised API for others | Technical Lead |
| R-2 | Councils resist new reporting requirements | MEDIUM | HIGH | Position as WasteDataFlow replacement (not addition), demonstrate local value | SRO |
| R-3 | Data quality too poor for national statistics designation | MEDIUM | HIGH | Validation at ingestion, data quality scoring, estimation for gaps | Statistics Lead |
| R-4 | EA enforcement use raises data sharing legal concerns | MEDIUM | MEDIUM | Legal review, formal data sharing agreement, DPIA | DEFRA Legal |
| R-5 | WasteDataFlow transition disrupts existing statistics | LOW | HIGH | Parallel running for 2 years, reconciliation between old and new | Statistics Lead |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Resources and Waste Strategy 2018 | Policy | GOV.UK | Waste data improvement commitments | N/A |
| Environment Act 2021 | Legislation | legislation.gov.uk | Waste tracking powers | N/A |
| Environmental Protection (Duty of Care) Regulations 1991 | Legislation | legislation.gov.uk | WTN requirements | N/A |
| ARC-003-STKE-v1.0 | Stakeholder Analysis | SDG 12 Programme | Stakeholder drivers and goals | `projects/003-waste-management-analytics/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Waste Management Analytics (Project 003)
**Model**: Claude Opus 4.6
