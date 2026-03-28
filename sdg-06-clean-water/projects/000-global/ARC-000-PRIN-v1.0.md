# UK Government Enterprise Architecture Principles — SDG 6: Clean Water and Sanitation

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit:principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 6: Clean Water and Sanitation — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 6 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 6 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 6: Clean Water and Sanitation programme. These principles apply to four UK Government digital services:

- **001** — Water Quality Monitoring Platform (DEFRA)
- **002** — Flood Risk Management System (Environment Agency)
- **003** — Wastewater Treatment Analytics (Ofwat)
- **004** — Water Resource Planning Tool (DEFRA)

**Scope**: All technology projects, systems, and initiatives within the SDG 6 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Environment Act 2021, Water Framework Directive (retained EU law), Flood and Water Management Act 2010, and the 25 Year Environment Plan.

---

## I. Strategic Principles

### 1. Environmental Data Integrity

**Principle Statement**:
All systems MUST ensure the integrity, accuracy, and provenance of environmental monitoring data from point of collection through to regulatory reporting.

**Rationale**:
Environmental data underpins regulatory compliance decisions, public health warnings, and long-term policy planning. Inaccurate water quality readings could lead to unsafe bathing water designations, missed pollution incidents, or flawed flood warnings that endanger life. The Environment Act 2021 imposes statutory duties on data accuracy for water company performance reporting. Data integrity is not merely a technical concern — it is a public safety imperative.

**Implications**:

- Implement cryptographic data signing at the sensor/IoT edge to guarantee provenance
- Maintain immutable audit trails for all environmental measurements from collection to publication
- Apply automated validation rules at ingestion to detect sensor drift, calibration errors, and outliers
- Timestamp all readings with GPS-synchronised UTC time at source, not at receipt
- Implement data reconciliation checks between field sensors and laboratory confirmatory samples
- Support chain-of-custody documentation for legally admissible environmental evidence

**Validation Gates**:

- [ ] Data provenance traceable from sensor to published dataset
- [ ] Automated quality assurance rules applied at ingestion with anomaly flagging
- [ ] Immutable audit trail verified for all environmental measurements
- [ ] Calibration records linked to measurement data for all monitoring equipment
- [ ] Data accuracy validated against laboratory reference samples (minimum quarterly)

---

### 2. IoT Sensor Reliability and Resilience

**Principle Statement**:
All IoT sensor networks MUST be designed for continuous operation in harsh environmental conditions with automated health monitoring, failover capability, and graceful degradation.

**Rationale**:
Environmental monitoring sensors operate in challenging conditions — submerged in rivers, exposed to flood waters, mounted on sewage outfalls, or deployed in remote catchment areas with limited connectivity. Sensor failure during a pollution incident or flood event could result in loss of life or irreversible environmental damage. The Environment Agency's flood warning service requires 99.5% sensor availability during high-risk periods.

**Implications**:

- Design sensors for IP68 or higher ingress protection rating appropriate to deployment environment
- Implement redundant communication pathways (cellular, LoRaWAN, satellite) for remote sites
- Deploy battery backup with solar or kinetic energy harvesting for off-grid locations
- Automated health monitoring with proactive alerting when sensors approach failure thresholds
- Graceful degradation — system must continue operating with reduced sensor coverage rather than failing entirely
- Maintain a register of all deployed sensors with firmware versions, calibration dates, and maintenance schedules

**Validation Gates**:

- [ ] Sensor uptime meets 99.5% availability target (99.9% during high-risk periods)
- [ ] Redundant communication pathways tested and documented for all remote sites
- [ ] Battery and power supply resilience tested for minimum 72-hour autonomous operation
- [ ] Automated health monitoring and alerting operational for all deployed sensors
- [ ] Sensor maintenance schedule defined with maximum calibration interval documented

---

### 3. Real-Time Data Ingestion and Processing

**Principle Statement**:
All systems MUST support real-time or near-real-time data ingestion with end-to-end latency appropriate to the operational criticality of the data — flood warning data within 2 minutes, water quality alerts within 5 minutes, and routine monitoring within 15 minutes.

**Rationale**:
Environmental events unfold rapidly. River levels can rise by metres within hours during flash floods. Sewage spills can contaminate bathing waters within minutes. The Environment Agency's Flood Forecasting Centre requires sub-2-minute telemetry to issue timely flood warnings under the Civil Contingencies Act 2004. Delayed data costs lives.

**Implications**:

- Implement event-driven streaming architecture for time-critical environmental data
- Define tiered latency SLAs based on data criticality (flood: <2 min, pollution: <5 min, routine: <15 min)
- Use message queuing with guaranteed delivery for sensor telemetry
- Design for burst ingestion during storm events when thousands of sensors report simultaneously
- Implement data backfill mechanisms for when sensors reconnect after communication outages
- Monitor end-to-end latency continuously with alerting on SLA breaches

**Validation Gates**:

- [ ] End-to-end latency measured and within SLA for each data tier
- [ ] Burst ingestion tested at 10x normal volume (storm scenario simulation)
- [ ] Data backfill mechanism tested for 24-hour communication outage recovery
- [ ] Latency monitoring and alerting operational in production
- [ ] Message delivery guarantees documented (at-least-once for all tiers)

---

### 4. Geospatial Data Standards and Interoperability

**Principle Statement**:
All systems MUST use open geospatial standards (OGC, INSPIRE) and the British National Grid (OSGB36) or WGS84 coordinate reference systems, with full interoperability across DEFRA, Environment Agency, Ordnance Survey, and Met Office datasets.

**Rationale**:
Water management is inherently spatial — catchment boundaries, flood zones, river networks, bathing water locations, and sewage treatment works all require precise geospatial representation. The UK INSPIRE regulations (retained EU law) mandate interoperable spatial data for environmental themes. Incompatible coordinate systems or non-standard spatial formats create dangerous errors in flood zone mapping and pollution source tracing.

**Implications**:

- Use OGC standards (WMS, WFS, WCS, GeoJSON, GeoPackage) for all spatial data exchange
- Store spatial data with explicit coordinate reference system (CRS) metadata — never assume
- Align with Ordnance Survey MasterMap and OS Open Data for base mapping
- Implement INSPIRE-compliant metadata for all environmental spatial datasets
- Support dynamic re-projection between OSGB36 (British National Grid) and WGS84 (GPS/web mapping)
- Integrate with DEFRA's Data Services Platform for authoritative catchment and water body boundaries

**Validation Gates**:

- [ ] All spatial data published using OGC-compliant services and formats
- [ ] Coordinate reference system explicitly declared in all spatial datasets
- [ ] INSPIRE metadata records published for all environmental spatial data themes
- [ ] Interoperability tested with Ordnance Survey, Met Office, and Environment Agency spatial services
- [ ] Spatial accuracy validated against Ordnance Survey reference data

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems are classified as Critical National Infrastructure (CNI) under the NIS Regulations 2018. A cyber attack on flood warning systems could prevent timely evacuations. Compromise of water quality monitoring could mask contamination events. IoT sensor networks present an expanded attack surface requiring specific operational technology (OT) security controls. NCSC guidance on CNI protection and the Secure by Design framework mandate proactive, defence-in-depth security.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrative access
- [ ] Service-to-service authentication using mutual TLS or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or firmware)
- [ ] Network segmentation between IT and OT (IoT sensor) networks with deny-by-default policies
- [ ] Encryption at rest for all data stores containing environmental monitoring or personal data
- [ ] Encrypted transport for all network communication including sensor telemetry
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing including IoT firmware vulnerability assessment
- [ ] Incident response plan specific to CNI scenarios (coordinated with NCSC)

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- NIS Regulations 2018 (CNI designation)
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- NCSC CAF (Cyber Assessment Framework) for water sector operators

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed for each service including IoT attack vectors
- [ ] Security controls mapped to NIS Regulations and NCSC CAF requirements
- [ ] Security testing plan executed including IoT/OT penetration testing
- [ ] Incident response runbook created with NCSC CNI escalation procedures
- [ ] IT/OT network segmentation verified through penetration testing

---

### 6. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning, with specific attention to environmental monitoring system health.

**Rationale**:
Environmental monitoring systems must be observable at two levels: the health of the technology platform itself, and the health of the environmental monitoring network (sensor status, data freshness, coverage gaps). A flood warning system that is technically running but receiving stale data from failed sensors is operationally blind. Both dimensions must be monitored.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, sensor health
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Environmental Health**: Sensor connectivity, data freshness, geographic coverage heatmaps
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Platform metrics: request volume, latency, error rates, resource utilisation
- Sensor network metrics: sensors online/offline, data freshness per station, communication pathway health
- Environmental metrics: readings received per hour, quality check pass/fail rates, data gaps by catchment
- Business metrics: flood warnings issued, pollution alerts generated, regulatory reports submitted
- Security events: authentication failures, policy violations, suspicious access to CNI systems

**Log Retention**:

- **Security/audit logs**: Minimum 2 years (aligned with NIS Regulations)
- **Environmental monitoring logs**: 6 years (aligned with Water Framework Directive reporting cycles)
- **Application logs**: 90 days minimum for troubleshooting
- **Metrics**: 2 years with progressive aggregation for trend analysis

**Validation Gates**:

- [ ] Platform and sensor network telemetry instrumented for all services
- [ ] Dashboards configured for both platform health and environmental monitoring coverage
- [ ] Service Level Objectives (SLOs) defined for platform and sensor network availability
- [ ] Runbooks created for all alerting scenarios including sensor network degradation
- [ ] Environmental data coverage gaps detectable and alertable in real time

---

## II. Data Principles

### 7. Data Sovereignty and Environmental Data Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Environmental Information Regulations 2004, and departmental data governance policies.

**Rationale**:
Environmental monitoring data has dual governance requirements: personal data (staff, reporters, complaint data) requires GDPR protection, while environmental data itself falls under the Environmental Information Regulations 2004 which create a presumption of public access. These competing obligations must be carefully managed. Additionally, the Environment Act 2021 requires specific data retention for water company performance reporting.

**Data Classification Tiers**:

1. **OFFICIAL — Open Environmental Data**: Monitoring readings, river levels, water quality results — presumption of publication under EIR 2004
2. **OFFICIAL**: Standard government business data, internal operational data
3. **OFFICIAL-SENSITIVE**: Enforcement investigation data, water company pre-publication performance data, vulnerability assessments of CNI assets
4. **SECRET**: Not expected in this programme; escalate if identified

**Data Residency**:

- All data MUST reside within UK sovereign data centres
- No transfer of personal or CNI-related data outside the UK
- Environmental monitoring data may be shared internationally through established scientific frameworks (e.g., European Environment Agency reporting) via agreed channels

**Data Retention**:

- Environmental monitoring data: minimum 6 years (WFD reporting cycle), indefinite for long-term trend datasets
- Flood event data: permanent retention (critical for return period analysis)
- Enforcement/prosecution data: 7 years post-case-closure
- Personal data: deletion within 12 months of last legitimate use
- Backup retention aligned with RPO and compliance requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores distinguishing personal from environmental data
- [ ] UK residency confirmed for all data storage and processing
- [ ] Retention policies configured with automated deletion for personal data
- [ ] Environmental Information Regulations compliance assessed — open data publication plan in place
- [ ] Data sharing agreements in place for cross-departmental and water company data flows

---

### 8. Open Data and Public Transparency

**Principle Statement**:
All non-sensitive environmental monitoring data MUST be published as open data by default, meeting the 5-star open data standard, enabling public scrutiny and third-party innovation.

**Rationale**:
The Environmental Information Regulations 2004 create a legal presumption that environmental data should be publicly accessible. The 25 Year Environment Plan commits to making environmental data freely available. Public transparency builds trust — particularly important given ongoing public concern about sewage discharges and water quality. Open data also enables academic researchers, conservation groups, and technology companies to create value from public investment in environmental monitoring.

**Implications**:

- Publish environmental monitoring data through DEFRA's Data Services Platform and data.gov.uk
- Use machine-readable open formats (CSV, JSON, GeoJSON, OGC APIs) — not locked PDFs
- Provide bulk download capability alongside API access
- Publish metadata describing data collection methods, quality assurance procedures, and known limitations
- Update published data at frequencies matching operational use (real-time for flood levels, daily for water quality)
- Maintain historical data access — do not overwrite; version and append

**Validation Gates**:

- [ ] Environmental monitoring data published on data.gov.uk and DEFRA Data Services Platform
- [ ] Data published in machine-readable open formats with API access
- [ ] Metadata published describing collection methods and quality assurance
- [ ] Publication frequency matches operational data update frequency
- [ ] Historical data accessible and versioned (no destructive updates)

---

### 9. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and regulatory reporting transparency.

**Rationale**:
Environmental data quality directly affects public health decisions and regulatory enforcement. A false positive on E. coli levels triggers unnecessary bathing water closures and public alarm. A false negative masks genuine contamination risks. Water quality data used in Environment Act 2021 reporting must be demonstrably traceable from sensor through processing to published figure. Ofwat's methodology statements require auditable data lineage for water company performance metrics.

**Quality Standards**:

- **Completeness**: No unexpected gaps in time-series data; gap-filling algorithms documented and flagged
- **Consistency**: Cross-sensor reconciliation within catchment areas; outlier detection against hydrological norms
- **Accuracy**: Validation against laboratory reference samples; sensor calibration records linked to readings
- **Timeliness**: Freshness SLAs defined per data type (flood: <2 min, water quality: <15 min, resource planning: daily)

**Lineage Requirements**:

- Source-to-publication mapping documented for all environmental data flows
- Transformation logic (unit conversions, averaging, gap-filling) version-controlled and auditable
- Data quality metrics tracked per sensor, per parameter, per catchment
- Impact analysis capability for methodology changes (what changes if we recalibrate sensor X?)

**Validation Gates**:

- [ ] Data quality rules automated with monitoring and anomaly alerting
- [ ] Lineage metadata captured from sensor to published dataset
- [ ] Data contracts defined between data producers (sensors, labs, water companies) and consumers (regulators, public)
- [ ] Methodology change impact analysis capability demonstrated

---

### 10. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
Environmental data is consumed by multiple agencies — DEFRA, Environment Agency, Ofwat, Natural England, water companies, and the public. If river level data differs between the EA Flood Information Service and the DEFRA Data Services Platform, public trust is undermined and operational confusion results. Authoritative sources must be unambiguous, especially during incident response when multiple agencies are making real-time decisions.

**Implications**:

- Environment Agency is the authoritative source for flood level and flood risk data
- DEFRA is the authoritative source for Water Framework Directive water body classification
- Ofwat is the authoritative source for water company performance metrics
- Water companies are the authoritative source for their own operational telemetry (treatment works, network)
- Met Office is the authoritative source for rainfall and weather forecast data
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Avoid bidirectional synchronisation — it creates data conflicts during incidents

**Validation Gates**:

- [ ] System of record identified and documented for each environmental data domain
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Authoritative source agreements in place with Met Office, Ordnance Survey, and water companies

---

## III. Integration Principles

### 11. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 6 programme spans four projects across three organisations (DEFRA, Environment Agency, Ofwat). Each team must be able to develop, deploy, and evolve their service independently. During incident response (e.g., major flooding), systems must continue operating even if partner systems are degraded. Tight coupling creates single points of failure in critical national infrastructure.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across system boundaries; use compensating actions or sagas
- Interface contracts owned by the producing team with consumer input on design
- Design for partner system unavailability — cache critical reference data locally

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] System continues operating (potentially degraded) when partner systems are unavailable

---

### 12. Environmental Monitoring Interoperability

**Principle Statement**:
Systems SHOULD use established environmental data exchange standards (WaterML 2.0, SensorThings API, INSPIRE themes) and MUST integrate with existing UK Government environmental monitoring infrastructure.

**Rationale**:
The UK's environmental monitoring landscape includes established systems — the EA's National Flood Forecasting System, DEFRA's Water Quality Archive, Met Office Unified Model, and numerous water company SCADA systems. New platforms must integrate with this ecosystem, not replace it. International standards like WaterML 2.0 and OGC SensorThings API enable interoperability with European and global monitoring networks for transboundary water management and international reporting obligations.

**When to Use Asynchronous Patterns**:

- Cross-agency data sharing (e.g., water quality results to DEFRA, flood levels to EA)
- Batch ingestion from water company operational systems (daily/hourly feeds)
- Regulatory reporting data assembly (aggregation across multiple sources)
- Non-critical notifications (planned maintenance, routine status updates)

**When Synchronous Communication is Acceptable**:

- Real-time flood warning dissemination (life-safety critical)
- Interactive map queries for current river levels or water quality status
- Incident escalation requiring immediate acknowledgement

**Validation Gates**:

- [ ] Environmental data exchange uses WaterML 2.0 or OGC SensorThings API where applicable
- [ ] Integration tested with EA National Flood Forecasting System, Met Office Data Hub, and DEFRA Data Services
- [ ] Water company data feeds operational with defined SLAs and error handling
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined for all integrations

---

## IV. Quality Attributes

### 13. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load, with specific attention to storm event surge capacity and public-facing map rendering performance.

**Rationale**:
Environmental monitoring systems experience extreme load variation. During major flood events, the EA Flood Information Service receives millions of page views per hour from anxious citizens. Water quality dashboards see traffic spikes after media coverage of sewage spills. Systems must handle these surges while maintaining responsiveness. Public-facing map interfaces must render quickly on mobile devices used by citizens in flood-affected areas with potentially degraded connectivity.

**Performance Targets** (to be defined per service):

- **Flood warning pages**: p95 < 1 second (life-safety critical — citizens may be evacuating)
- **Water quality dashboards**: p95 < 3 seconds for map rendering
- **API response time**: p95 < 500ms for individual station queries, < 2 seconds for catchment queries
- **Sensor data ingestion**: sustained 10,000 readings/second, burst to 100,000/second during storms
- **Map tile rendering**: < 200ms per tile for pre-rendered, < 2 seconds for dynamic

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at 10x normal capacity (storm surge scenario)
- [ ] Performance metrics monitored in production with alerting on degradation
- [ ] Mobile performance tested on 3G connectivity with low-specification devices
- [ ] Map rendering performance validated for geographic areas with highest sensor density

---

### 14. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets, with flood warning systems classified as life-safety critical requiring 99.95% availability during high-risk periods.

**Rationale**:
Flood warning systems are life-safety critical infrastructure. The Environment Agency's Flood Warning Service operates under statutory duties to warn citizens of imminent flood risk. System unavailability during a flood event could prevent warnings reaching affected communities. Water quality monitoring supports public health decisions — bathing water advisories, drinking water safety alerts. Availability targets must reflect the potential for loss of life if systems fail at the wrong moment.

**Availability Targets**:

- **Flood warning systems**: 99.95% (26 minutes downtime per year maximum), 99.99% during Met Office severe weather warnings
- **Water quality public dashboards**: 99.9% (8.7 hours downtime per year)
- **Regulatory reporting systems**: 99.5% (43.8 hours per year — less time-critical)
- **Water resource planning**: 99.5% (batch processing, less time-critical)

**High Availability Patterns**:

- Multi-region deployment for flood warning systems with automatic failover
- Automated health checks with self-healing recovery
- Pre-computed static fallback pages for flood warnings if dynamic systems fail
- Regular disaster recovery testing (quarterly for flood systems, annually for others)

**Validation Gates**:

- [ ] Availability SLA defined per service based on life-safety and public health impact
- [ ] RTO and RPO requirements documented (flood: RTO 5 minutes, RPO 0 minutes)
- [ ] Multi-region failover tested for life-safety critical services
- [ ] Static fallback capability verified for flood warning dissemination
- [ ] DR testing conducted at defined frequency with documented results

---

### 15. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with specific capacity for storm event surges when sensor volumes and public traffic increase by 10-100x normal levels.

**Rationale**:
Environmental monitoring systems experience extreme demand variation. A routine summer day generates baseline sensor readings and moderate public dashboard traffic. A named storm event simultaneously increases sensor reporting frequency (gauges moving to 1-minute intervals), public web traffic (millions checking flood risk), and data processing load (flood models running at high resolution). Systems must absorb this surge without degradation during the most critical operational period.

**Implications**:

- Design for stateless components that can be replicated independently
- Pre-scale for known high-risk periods (winter flood season October-March)
- Implement auto-scaling based on both platform metrics and environmental triggers (Met Office warnings)
- Capacity plan for concurrent storm events across multiple river catchments
- Use content delivery networks for public-facing map tiles and warning pages
- Test elasticity with realistic storm event simulations including data volume and public traffic

**Validation Gates**:

- [ ] System scales horizontally without architecture change
- [ ] Auto-scaling triggered by environmental conditions (Met Office warning level) as well as platform metrics
- [ ] Storm surge simulation tested at 10x normal sensor volume + 50x normal web traffic simultaneously
- [ ] Scaling achievable within 5 minutes of trigger to meet flood warning latency SLAs
- [ ] Cost model accounts for variable capacity with seasonal pre-scaling budgeted

---

### 16. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity — especially during emergency situations.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Flood warnings must reach everyone including those with visual impairments, cognitive disabilities, and hearing loss. Citizens in flood-affected areas may be using devices in challenging conditions — outdoors, in low light, with wet hands, on degraded mobile networks. Water quality information must be understandable by the general public, not just environmental scientists.

**Implications**:

- Design flood warning interfaces using progressive enhancement — core warnings work without JavaScript
- Support multiple notification channels (web, SMS, voice call, email) for flood warnings
- Present water quality data with clear, colour-independent status indicators (not just red/amber/green)
- Use plain language — "safe to swim" rather than "compliant with Bathing Water Regulations"
- Test with assistive technologies including screen readers, voice control, and switch access
- Ensure map interfaces have non-map alternatives for visually impaired users

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Flood warning information accessible without JavaScript
- [ ] Water quality status understandable without colour vision (verified through simulation)
- [ ] Mobile usability tested in outdoor conditions with degraded connectivity

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Environmental monitoring infrastructure is complex — hundreds of data ingestion endpoints, multiple geographic regions, IoT gateway configurations, and season-dependent scaling profiles. Manual infrastructure changes create drift and undocumented state. For CNI systems, infrastructure auditability is a NIS Regulations requirement. Infrastructure as Code enables repeatable disaster recovery, which is essential when flood events may physically damage hosting infrastructure.

**Implications**:

- All infrastructure defined in declarative code within version control
- Infrastructure changes go through the same code review process as application code
- Environments are reproducible from code — no snowflake configurations
- No manual changes to production infrastructure (enforced through access controls)
- IoT gateway and edge compute configurations managed as code alongside cloud infrastructure
- Seasonal scaling profiles (winter flood season) codified as infrastructure configuration

**Validation Gates**:

- [ ] All infrastructure defined as code in version control
- [ ] Infrastructure code goes through peer review before deployment
- [ ] Full environment rebuild demonstrated from code (tested annually)
- [ ] No manual infrastructure changes in production (enforced, not just policy)
- [ ] IoT gateway configurations managed as code with version control

---

### 18. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to any shared environment, with specific test suites for environmental data processing accuracy.

**Rationale**:
Defects in environmental monitoring systems have direct real-world consequences. An error in flood level calculation could trigger false warnings causing unnecessary evacuations, or worse, fail to warn of genuine flood risk. Water quality calculation errors could result in contaminated bathing waters being declared safe. Automated testing must include domain-specific validation against known environmental datasets.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions and data flows (15-20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (correct processing of environmental data)
- Environmental scenario tests (replay of historical flood events, pollution incidents against system)
- Performance tests (storm surge simulation at 10x normal load)
- Security tests (IoT firmware scanning, API security testing, CNI-specific scenarios)
- Accessibility tests (automated WCAG checks in pipeline)
- Regression tests for calculation methodology changes

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Historical event replay tests validate correct system behaviour for known flood and pollution events
- [ ] Test coverage meets defined thresholds per service
- [ ] Security and accessibility tests integrated into CI/CD pipeline
- [ ] Calculation methodology changes validated against published reference datasets

---

### 19. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage. Deployment to life-safety critical systems requires additional approval gates.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent releases. However, for CNI systems like flood warnings, deployment timing must consider operational risk — deploying during an active flood event is unacceptable. Quality gates must include environmental data validation as well as standard software checks.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, environmental scenario, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Environmental Validation**: Replay of reference datasets through changed code
6. **Deployment**: Automated deployment with progressive rollout and automatic rollback

**Quality Gates**:

- All automated tests must pass including environmental scenario tests
- No critical or high security vulnerabilities
- Peer review approval required
- For flood warning systems: deployment window restricted to low-risk periods (no active Met Office warnings)
- Production deployment requires documented change approval via CAB or equivalent

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes environmental data validation alongside security and accessibility
- [ ] Deployment windows enforced for life-safety critical systems
- [ ] Rollback capability tested and achievable within 5 minutes
- [ ] Deployment frequency appropriate to service criticality (daily for dashboards, controlled for flood warnings)

---

### 20. Water Framework Directive Compliance by Design

**Principle Statement**:
All systems handling water quality data MUST be designed to support Water Framework Directive (retained EU law) reporting requirements, including water body classification, status assessment, and River Basin Management Plan reporting.

**Rationale**:
The Water Framework Directive (transposed into UK law and retained post-Brexit) provides the regulatory framework for water quality management in the UK. Systems must support the WFD classification methodology (ecological status, chemical status) and produce data in formats required for 6-yearly River Basin Management Plan reporting. Non-compliance risks infraction proceedings and undermines the UK's environmental governance credibility.

**Implications**:

- Implement WFD water body classification calculations using published EA methodology
- Store monitoring data at the water body level with linkage to WFD water body register
- Support the WFD one-out-all-out classification principle in status aggregation
- Generate data exports compatible with WISE (Water Information System for Europe) reporting formats
- Maintain traceability from individual monitoring results to water body classification decisions
- Version all classification methodology so historical assessments can be reproduced

**Validation Gates**:

- [ ] WFD classification calculations validated against EA published methodology
- [ ] Water body register aligned with EA's official water body delineation
- [ ] Data exportable in WISE-compatible formats for international reporting
- [ ] Classification methodology versioned with historical assessment reproducibility
- [ ] Audit trail from individual monitoring results to classification decision

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy monitoring systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including environmental and public safety impact if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 5) or life-safety principles (Principles 2, 3, 14)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] Environmental data standards approach defined (WaterML, INSPIRE, OGC)
- [ ] IoT sensor architecture approach validated (Principle 2)
- [ ] Data classification and open data approach defined (Principles 7, 8)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed including IoT/OT attack vectors (Principle 5)
- [ ] Geospatial interoperability tested with EA, Met Office, and OS services (Principle 4)
- [ ] Accessibility approach validated including emergency scenario usability (Principle 16)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] Storm surge load testing passed (Principle 15)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed including IoT/OT testing with no unresolved critical findings

### Enforcement

- Architecture reviews are **mandatory** for all projects at each phase gate
- Principle violations must be remediated or exception-approved before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective compliance reviews conducted annually for live services
- NIS Regulations compliance reviewed annually with NCSC

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | Environmental Data Integrity | Strategic | CRITICAL | Provenance, audit trail, quality checks |
| 2 | IoT Sensor Reliability and Resilience | Strategic | CRITICAL | 99.5% uptime, redundant comms, health monitoring |
| 3 | Real-Time Data Ingestion and Processing | Strategic | CRITICAL | Latency SLAs met, burst capacity tested |
| 4 | Geospatial Data Standards | Strategic | HIGH | OGC/INSPIRE compliance, CRS metadata |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, CNI controls, IoT security |
| 6 | Observability and Operational Excellence | Strategic | HIGH | Platform + sensor health monitoring |
| 7 | Data Sovereignty and Environmental Governance | Data | CRITICAL | UK residency, EIR compliance, retention |
| 8 | Open Data and Public Transparency | Data | HIGH | data.gov.uk publication, open formats |
| 9 | Data Quality and Lineage | Data | CRITICAL | Sensor-to-publication traceability |
| 10 | Single Source of Truth | Data | HIGH | Authoritative sources documented |
| 11 | Loose Coupling | Integration | HIGH | Deployment independence, partner resilience |
| 12 | Environmental Monitoring Interoperability | Integration | HIGH | WaterML, SensorThings, EA/Met Office integration |
| 13 | Performance and Efficiency | Quality | HIGH | Storm surge load testing, mobile performance |
| 14 | Availability and Reliability | Quality | CRITICAL | 99.95% for flood, multi-region, static fallback |
| 15 | Scalability and Elasticity | Quality | HIGH | 10x surge capacity, seasonal pre-scaling |
| 16 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, emergency usability |
| 17 | Infrastructure as Code | Development | HIGH | IaC coverage including IoT gateways |
| 18 | Automated Testing | Development | HIGH | Environmental scenario replay testing |
| 19 | Continuous Integration and Deployment | Development | HIGH | Environmental validation, deployment windows |
| 20 | Water Framework Directive Compliance | Development | CRITICAL | WFD classification, WISE reporting |

### Alignment to UK Government and Environmental Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 4 (Open Standards), 5 (Security), 16 (Accessibility), 8 (Open Data) |
| Technology Code of Practice | 4 (Geospatial Standards), 5 (Security), 17 (IaC), 8 (Open Data) |
| NCSC Secure by Design / CAF | 5 (Security by Design), 2 (IoT Resilience), 17 (IaC) |
| NIS Regulations 2018 | 5 (Security), 14 (Availability), 6 (Observability) |
| Environment Act 2021 | 1 (Data Integrity), 9 (Data Quality), 20 (WFD Compliance) |
| Water Framework Directive | 1 (Data Integrity), 9 (Data Quality), 20 (WFD Compliance) |
| 25 Year Environment Plan | 8 (Open Data), 1 (Data Integrity), 4 (Geospatial) |
| Environmental Information Regulations 2004 | 7 (Data Governance), 8 (Open Data) |
| UK GDPR / DPA 2018 | 7 (Data Sovereignty), 5 (Security) |
| Public Sector Accessibility Regulations | 16 (Accessibility and Inclusion) |
| Flood and Water Management Act 2010 | 3 (Real-Time Ingestion), 14 (Availability), 2 (Sensor Reliability) |
| HM Treasury Green Book | 15 (Scalability), 13 (Performance), 14 (Availability) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| Environment Act 2021 | Legislation | legislation.gov.uk | Water company duties, environmental monitoring | N/A — external reference |
| Water Framework Directive | Retained EU Law | legislation.gov.uk | Water body classification, reporting cycles | N/A — external reference |
| 25 Year Environment Plan | Policy | GOV.UK | Clean water commitments, open data | N/A — external reference |
| NIS Regulations 2018 | Legislation | legislation.gov.uk | CNI operator requirements | N/A — external reference |
| NCSC CAF | Guidance | NCSC | Cyber Assessment Framework for water sector | N/A — external reference |
| Environmental Information Regulations 2004 | Legislation | legislation.gov.uk | Public access to environmental data | N/A — external reference |
| Flood and Water Management Act 2010 | Legislation | legislation.gov.uk | Flood risk management duties | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 6: Clean Water and Sanitation — Cross-Project Governance (Project 000)
**AI Model**: Claude Opus 4.6 (1M context)
