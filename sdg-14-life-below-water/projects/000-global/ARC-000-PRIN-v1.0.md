# UK Government Enterprise Architecture Principles — SDG 14: Life Below Water

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 14: Life Below Water — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 14 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 14 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 14: Life Below Water programme. These principles apply to four UK Government digital services:

- **001** — Marine Protected Areas Monitoring (DEFRA)
- **002** — Fishing Quota Management (MMO)
- **003** — Ocean Pollution Tracking (DEFRA)
- **004** — Coastal Erosion Monitoring (Environment Agency)

**Scope**: All technology projects, systems, and initiatives within the SDG 14 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the Marine and Coastal Access Act 2009, Fisheries Act 2020, OSPAR Convention, UK Marine Strategy (Part One and Part Two), the Marine Strategy Framework Directive (MSFD) transposed obligations, the 25 Year Environment Plan, the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, and the Public Sector Bodies Accessibility Regulations 2018.

---

## I. Strategic Principles

### 1. Ocean Data Interoperability and Open Standards

**Principle Statement**:
All marine and coastal systems MUST exchange data through well-defined, versioned interfaces using internationally recognised oceanographic and environmental data standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 14 programme spans multiple departments (DEFRA, MMO, Environment Agency) and must integrate with international bodies (ICES, OSPAR, IUCN) and existing UK platforms (MEDIN, Marine Online Assessment Tool, MAGIC). The Marine and Coastal Access Act 2009 mandates coordinated marine data management. The Technology Code of Practice mandates open standards to avoid vendor lock-in and enable cross-government data sharing. Interoperability enables joined-up marine governance — a fishing quota decision must be informed by conservation zone data, and pollution tracking must inform coastal erosion models.

**Implications**:

- Use INSPIRE-compliant geospatial standards (WMS, WFS, GML) for all spatial marine data
- Adopt MEDIN discovery metadata standard for all marine datasets
- Publish interface specifications (API contracts, event schemas) in a discoverable catalogue aligned with DATA.GOV.UK
- Version all interfaces with a documented backward compatibility strategy
- No direct database access across system boundaries
- Asynchronous communication for non-real-time interactions (e.g., batch catch reporting)
- Support OGC standards (SensorThings API, SOS) for real-time sensor data from buoys, AIS receivers, and survey equipment

**Validation Gates**:

- [ ] Interface specifications published (OpenAPI, AsyncAPI, OGC-compliant schemas)
- [ ] MEDIN metadata records created for all datasets
- [ ] Versioning strategy defined with backward compatibility policy
- [ ] Authentication and authorisation model documented
- [ ] No direct database coupling across system boundaries
- [ ] Data flows registered with DEFRA Data Catalogue

---

### 2. Geospatial First Design

**Principle Statement**:
All systems MUST treat geospatial data as a first-class citizen, with native support for marine coordinate systems, bathymetric depth references, and UK Continental Shelf boundaries.

**Rationale**:
Every entity in the SDG 14 programme has a spatial dimension — marine protected areas are defined by polygon boundaries, fishing vessels report positions via VMS/AIS, pollution incidents have source and plume coordinates, and coastal erosion is measured along survey transects. Systems that bolt on spatial capability as an afterthought create data quality issues, integration barriers, and inability to perform the spatial analyses (overlap detection, proximity alerts, change detection) that are fundamental to marine governance.

**Implications**:

- Store all geographic data in standards-compliant spatial data types (WGS 84, OSGB36 where appropriate)
- Support marine-specific coordinate needs (depth/bathymetric references relative to Chart Datum)
- Integrate with UKHO Admiralty data products for charting and bathymetry
- Enable spatial queries (within MCZ boundary, proximity to vessel, intersection with pollution plume)
- Design for the UK Continental Shelf Boundary and Exclusive Economic Zone (EEZ) as fundamental reference layers
- Render spatial data on interactive maps using GDS-compliant design patterns

**Validation Gates**:

- [ ] Spatial data types used natively (not text-encoded coordinates)
- [ ] Coordinate reference systems documented and transformation capabilities tested
- [ ] Spatial indexing implemented for performance
- [ ] UK EEZ and UKCS boundary reference layers integrated
- [ ] UKHO bathymetric data integration tested
- [ ] Map-based interfaces meet WCAG 2.2 Level AA with non-visual alternatives

---

### 3. Environmental Data Provenance and Scientific Rigour

**Principle Statement**:
All environmental observations, measurements, and derived indicators MUST carry full provenance metadata — including sensor calibration, sampling methodology, quality assurance flags, and uncertainty estimates — enabling scientific peer review and regulatory audit.

**Rationale**:
Data from the SDG 14 programme underpins legally binding decisions: MCZ condition assessments determine protection measures, catch data inform quota allocations under the Fisheries Act 2020, pollution monitoring data trigger enforcement action, and coastal erosion data inform managed realignment and compensation decisions. Data without provenance is scientifically unusable and legally challengeable. The UK Marine Strategy requires Good Environmental Status (GES) indicators that meet OSPAR quality standards.

**Implications**:

- Record sensor metadata (instrument type, calibration date, accuracy specification) for all automated observations
- Implement quality flags (ISO 19157 data quality) on all measurement values
- Track data lineage from raw observation through processing to derived indicator
- Version all derived datasets with reproducible processing pipelines
- Support uncertainty quantification (confidence intervals, error bounds)
- Maintain chain of custody for regulatory enforcement data (marine pollution, illegal fishing)

**Validation Gates**:

- [ ] Provenance metadata schema defined and populated for all datasets
- [ ] Quality flag vocabulary aligned with OSPAR/ICES standards
- [ ] Data lineage traceable from source sensor to published indicator
- [ ] Processing pipelines version-controlled and reproducible
- [ ] Uncertainty estimates published alongside all derived indicators
- [ ] Chain of custody requirements met for enforcement-grade data

---

### 4. Scalability and Elasticity for Variable Marine Operations

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on seasonal patterns, weather events, and policy-driven surges.

**Rationale**:
Marine operations have pronounced seasonal and event-driven variability. Fishing activity peaks during quota year openings and seasonal species runs. Pollution incident response requires immediate surge capacity. Coastal survey campaigns generate massive LiDAR datasets seasonally. Storm events trigger simultaneous demand across all four services. Systems must handle both growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (storm events, quota year opening, pollution incidents)
- Design data ingestion pipelines for burst capacity (VMS position reports during fleet-wide activity)

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Cost model accounts for variable capacity and seasonal peaks
- [ ] Burst ingestion capacity tested (>100,000 VMS positions/hour)

---

### 5. Resilience and Fault Tolerance for Critical Marine Safety

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention. Systems with safety-of-life implications MUST maintain core functionality during any single component failure.

**Rationale**:
Marine systems have safety-critical dimensions: VMS tracking enables search and rescue coordination, pollution alerts protect public health at bathing waters, and coastal erosion warnings inform evacuation decisions. Beyond safety, fishing quota systems must maintain accurate running totals — an error could result in illegal overfishing or unjust quota closure affecting fishing community livelihoods. Resilience is not optional.

**Implications**:

- Implement circuit breakers for all external dependencies
- Use timeouts on all network calls with sensible defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services
- Safety-critical components (VMS tracking, pollution alerts) must have hot standby capability
- Design for eventual consistency where immediate consistency is not required

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical paths
- [ ] Fault injection testing performed for safety-critical components
- [ ] RTO and RPO defined per service (safety-critical: RTO <15 minutes, RPO <5 minutes)
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented with user-facing messaging
- [ ] Safety-critical components tested under single-component failure scenarios

---

### 6. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement.

**Rationale**:
The SDG 14 programme handles sensitive data: fishing vessel positions (commercially sensitive and security-relevant near offshore installations), marine pollution intelligence (potential enforcement evidence), coastal erosion survey data (land valuation and planning implications), and conservation site condition data. The NCSC Cyber Assessment Framework (CAF) applies to critical national infrastructure that includes maritime surveillance. Fishing quota systems are targets for fraud. DEFRA systems must meet the Government Security Standard (GovS 007).

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest
4. **Continuous Verification**: Monitor, log, and analyse all access patterns

**Mandatory Controls**:

- [ ] Multi-factor authentication for all human access
- [ ] Service-to-service authentication (mutual TLS, signed tokens, or equivalent)
- [ ] Secrets management via secure vault (never in code or config files)
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest for all data stores (AES-256 minimum)
- [ ] Encrypted transport for all network communication (TLS 1.3)
- [ ] Structured logging of all authentication/authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning)
- [ ] VMS and AIS data classified as OFFICIAL-SENSITIVE where vessel identification is possible

**Compliance Frameworks**:

- NCSC Cyber Assessment Framework (CAF) for maritime CNI components
- Government Security Standard (GovS 007)
- UK GDPR and Data Protection Act 2018
- Cyber Essentials Plus certification

**Exceptions**: NONE. Security principles are non-negotiable.

**Validation Gates**:

- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to requirements
- [ ] Security testing plan defined
- [ ] Incident response runbook created
- [ ] NCSC CAF self-assessment completed for CNI components
- [ ] Cyber Essentials Plus certification obtained

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
Marine systems operate 24/7 across remote locations — offshore buoys, coastal radar stations, vessel tracking receivers. We cannot operate what we cannot observe. Instrumentation is a first-class architectural requirement. Operational dashboards must provide a unified view across all four services, enabling the Marine Management Organisation, Environment Agency, and DEFRA to monitor marine health holistically.

**Telemetry Requirements**:

- **Logging**: Structured JSON logs with correlation IDs across service boundaries
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, plus marine-specific metrics (sensor uptime, data completeness, quota utilisation)
- **Tracing**: Distributed trace context for request flows across multi-service transactions
- **Alerting**: SLO-based alerting with actionable runbooks, plus marine event alerts (quota threshold breach, pollution incident detection, coastal erosion trigger)

**Required Instrumentation**:

- Request volume, latency distribution, error rate for all APIs
- Sensor and data feed health (AIS receiver uptime, buoy telemetry freshness, LiDAR upload status)
- Business metrics (catch reports submitted, MCZ assessments completed, pollution incidents logged)
- Security events (authentication failures, policy violations, suspicious access patterns)

**Validation Gates**:

- [ ] Logging, metrics, and tracing instrumented across all services
- [ ] Operational dashboards deployed with cross-service marine health view
- [ ] Alerting configured with runbooks for all critical scenarios
- [ ] Sensor and data feed monitoring operational
- [ ] Log retention meets regulatory requirements (7 years for enforcement data)

---

### 8. User-Centred Design for Diverse Marine Stakeholders

**Principle Statement**:
All systems MUST be designed around the needs of end users, with services that are simple, accessible, and appropriate for the wide range of marine stakeholders — from fishing vessel skippers at sea to scientific researchers to coastal community residents.

**Rationale**:
The SDG 14 programme serves extraordinarily diverse users: fishing vessel crews submitting catch reports in challenging conditions (at sea, limited connectivity, time pressure), marine scientists conducting complex spatial analysis, coastal communities viewing erosion data about their homes, MMO enforcement officers in the field, and DEFRA policy makers requiring aggregate dashboards. The GDS Service Standard mandates user-centred design. Marine-specific challenges include intermittent connectivity at sea, use in harsh physical environments, and users with varying technical proficiency.

**Implications**:

- Conduct user research with representative users including fishers, scientists, enforcement officers, and coastal residents
- Design for offline-first where users operate at sea or in areas with limited connectivity
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement
- Support multiple channels (online, telephone, face-to-face at ports and harbours) where appropriate
- Use plain language at a reading age appropriate for the service audience
- Provide clear status information (quota remaining, assessment progress, alert status)
- Design for maritime-appropriate interfaces (large touch targets, high-contrast displays for outdoor/bright conditions)

**Validation Gates**:

- [ ] User research conducted with representative sample including fishers and coastal communities
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Offline-capable functionality tested in low/no connectivity environments
- [ ] Content reviewed for plain language and readability
- [ ] User satisfaction metrics defined and baseline established
- [ ] Service assessed against GDS Service Standard points 1-3

---

### 9. Sustainability and Environmental Impact

**Principle Statement**:
All systems MUST minimise their own environmental footprint, with measurable targets for energy efficiency, sustainable hosting, and responsible data management — consistent with the mission to protect the marine environment.

**Rationale**:
A programme dedicated to protecting the marine environment must lead by example in its own operations. The Greening Government ICT strategy requires departments to reduce ICT environmental impact. Cloud hosting choices, data retention policies, and compute efficiency directly affect the programme's carbon footprint. The irony of a marine conservation programme with excessive energy consumption would undermine credibility.

**Implications**:

- Select cloud regions with high renewable energy percentage
- Implement data lifecycle policies (archive or delete data that is no longer actively used)
- Optimise compute-intensive workloads (spatial analysis, LiDAR processing) for energy efficiency
- Measure and report the programme's ICT carbon footprint annually
- Prefer serverless and auto-scaling architectures that do not consume resources when idle
- Consider edge computing to reduce data transmission from remote marine sensors

**Validation Gates**:

- [ ] Cloud hosting sustainability metrics documented
- [ ] Data lifecycle and retention policies implemented
- [ ] ICT carbon footprint baseline established
- [ ] Energy-efficient compute patterns used for batch processing
- [ ] Annual sustainability report produced

---

### 10. Privacy by Design and Proportionate Data Collection

**Principle Statement**:
All systems MUST implement privacy by design, collecting only the minimum data necessary for the stated purpose, with clear retention periods and lawful bases under UK GDPR.

**Rationale**:
The SDG 14 programme processes personal data: fishing vessel skipper details, vessel tracking data that reveals commercial patterns, coastal property owner information in erosion zones, and enforcement case data. VMS data is particularly sensitive — it reveals fishing grounds that have significant commercial value. The Data Protection Act 2018 and UK GDPR apply. DPIAs must be completed before processing begins. Proportionality is essential — data collection must be justified against the specific marine governance purpose.

**Implications**:

- Complete Data Protection Impact Assessments (DPIAs) before processing personal data
- Document lawful basis for each data processing activity
- Implement retention schedules aligned with regulatory requirements (Fisheries Act, Marine and Coastal Access Act)
- Anonymise or pseudonymise data where identification is not required
- Provide data subject rights mechanisms (access, rectification, erasure where applicable)
- VMS position data must be access-controlled with audit trails
- Coastal property data linked to erosion zones must be handled with sensitivity

**Validation Gates**:

- [ ] DPIA completed and signed off by DPO for each service
- [ ] Lawful basis documented for all personal data processing
- [ ] Retention schedules implemented and automated
- [ ] Data subject rights mechanisms functional
- [ ] VMS data access controls and audit trails implemented
- [ ] Privacy notices published for all user-facing services

---

## II. Governance and Compliance

### Exception Process

Any project seeking an exception to these principles must:

1. **Document** the principle being excepted and the specific technical or business justification
2. **Assess** the risk impact of the exception using the programme risk framework
3. **Propose** compensating controls that partially address the principle's intent
4. **Submit** to the Enterprise Architecture Review Board for approval
5. **Time-bound** the exception with a remediation plan and review date

### Compliance Assessment

All projects within the SDG 14 programme must complete a principles compliance self-assessment at the following gates:

- **Discovery/Alpha**: Initial architecture assessment against all principles
- **Beta**: Detailed compliance evidence for all applicable principles
- **Live**: Full compliance validation before go-live
- **Post-Live**: Annual re-assessment during service operation

### Cross-Programme Coordination

The four SDG 14 projects share marine data infrastructure and must coordinate on:

- Shared geospatial reference data (MCZ boundaries, EEZ, bathymetry)
- Common authentication and authorisation (DEFRA Identity)
- Unified marine data catalogue (MEDIN-compliant metadata)
- Cross-service event notifications (pollution incident triggers coastal erosion alert)
- Consistent user experience patterns (GDS Design System compliance)

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Marine and Coastal Access Act 2009 | Legislation | UK Parliament | MCZ designation, marine planning, licensing | legislation.gov.uk |
| Fisheries Act 2020 | Legislation | UK Parliament | Fisheries objectives, quota allocation, sustainability | legislation.gov.uk |
| OSPAR Convention | Treaty | OSPAR Commission | Marine environment protection, monitoring obligations | ospar.org |
| UK Marine Strategy Part One | Policy | DEFRA | Good Environmental Status targets and indicators | gov.uk |
| 25 Year Environment Plan | Policy | HMG | Marine environment targets, biodiversity net gain | gov.uk |
| GDS Service Standard | Standard | GDS | 14 points of service design and delivery | service-manual.service.gov.uk |
| Technology Code of Practice | Standard | CDDO | Open standards, cloud first, share and reuse | gov.uk |
| NCSC Cyber Assessment Framework | Standard | NCSC | CAF objectives for CNI operators | ncsc.gov.uk |
| MEDIN Discovery Metadata Standard | Standard | MEDIN | Marine metadata for interoperability | medin.org.uk |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 14: Life Below Water
**Model**: Claude Opus 4.6
