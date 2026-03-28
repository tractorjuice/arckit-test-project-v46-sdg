# UK Government Enterprise Architecture Principles — SDG 9: Industry, Innovation and Infrastructure

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 9: Industry, Innovation and Infrastructure — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 9 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 9 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 9: Industry, Innovation and Infrastructure programme. These principles apply to five UK Government digital services:

- **001** — Digital Infrastructure Mapping (DSIT)
- **002** — Smart Transport Network (DfT)
- **003** — Innovation Funding Platform (UKRI)
- **004** — National Underground Asset Register (Geospatial Commission)
- **005** — Research Collaboration Hub (DSIT)

**Scope**: All technology projects, systems, and initiatives within the SDG 9 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Secure by Design, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, INSPIRE Regulations, and the UK Digital Strategy 2022.

---

## I. Strategic Principles

### 1. Geospatial Data as a National Asset

**Principle Statement**:
All systems handling location-based data MUST treat geospatial information as a strategic national asset, adopting open geospatial standards to ensure interoperability, accuracy, and reuse across government and the wider economy.

**Rationale**:
The SDG 9 programme is fundamentally spatial — broadband coverage maps, transport network topologies, underground asset locations, and research institution geographies all rely on accurate, interoperable geospatial data. The UK Geospatial Strategy and INSPIRE Regulations mandate open geospatial standards. Inconsistent spatial data leads to duplicated infrastructure investment, failed utility installations, and inaccurate coverage assessments that undermine policy decisions worth billions of pounds.

**Implications**:

- Use OS National Grid (OSGB36/EPSG:27700) as the primary coordinate reference system for UK-domestic data
- Support WGS84 (EPSG:4326) for international data exchange and web mapping
- Adopt OGC standards for geospatial data exchange (WFS, WMS, WMTS, GeoJSON, GeoPackage)
- Comply with INSPIRE Regulations for environmental and infrastructure spatial data
- Reference Ordnance Survey products (OS MasterMap, AddressBase Premium, OS Open Data) as authoritative geometry sources
- Implement spatial data quality metrics (positional accuracy, completeness, currency)
- Support the Unique Property Reference Number (UPRN) and Topographic Identifier (TOID) as persistent identifiers

**Validation Gates**:

- [ ] Coordinate reference systems documented with transformation approach
- [ ] OGC-compliant spatial data services exposed where applicable
- [ ] INSPIRE metadata published for relevant datasets
- [ ] Spatial data quality metrics defined and monitored
- [ ] UPRN/TOID adoption assessed for address and feature referencing

---

### 2. User-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of end users, with services that are simple, inclusive, and accessible to everyone who needs them — from broadband engineers in rural locations to research academics and local authority planners.

**Rationale**:
The SDG 9 programme serves diverse user groups with very different needs: telecoms engineers mapping coverage in remote areas with limited connectivity, transport planners modelling network capacity, academics applying for research funding under deadline pressure, utility workers locating underground assets on construction sites, and researchers seeking industry collaborators. The GDS Service Standard mandates user-centred design for all UK Government digital services.

**Implications**:

- Conduct user research with representative users across all service contexts, including field workers with intermittent connectivity
- Design for offline-capable and low-bandwidth scenarios where field use is expected
- Meet WCAG 2.2 Level AA as a legal minimum under the Public Sector Bodies Accessibility Regulations 2018
- Support multiple form factors (desktop for complex analysis, tablet/mobile for field operations)
- Provide progressive disclosure — simple views for routine tasks, advanced views for specialist analysis
- Use GDS Design System components and patterns for citizen-facing interfaces

**Validation Gates**:

- [ ] User research conducted with representative sample across all user archetypes
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Offline/low-bandwidth capability validated for field-use services
- [ ] Content reviewed for plain language and domain-appropriate terminology
- [ ] User satisfaction metrics defined and baseline established
- [ ] Service assessed against GDS Service Standard points 1-3

---

### 3. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns including seasonal and event-driven spikes.

**Rationale**:
Infrastructure data volumes are large and growing — OS MasterMap alone contains over 500 million features. Transport data streams from connected infrastructure generate millions of events daily. UKRI funding rounds create predictable but intense application surges. Systems must handle both sustained data growth and acute demand spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Implement spatial data tiling and partitioning strategies for large geospatial datasets
- Plan for streaming data ingestion from IoT sensors, transport feeds, and coverage monitoring equipment
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics with pre-scaling for predictable events (funding deadlines, reporting periods)
- Design data stores for petabyte-scale growth over programme lifetime

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates linear capacity growth with added resources
- [ ] Spatial data partitioning strategy documented for large datasets
- [ ] Cost model accounts for variable capacity and peak scenarios

---

### 4. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
Infrastructure services underpin critical national operations — transport disruption information, utility strike avoidance, and broadband deployment coordination. Downtime in these systems has cascading real-world consequences: delayed infrastructure projects, safety risks from missing underground asset data, and transport network failures affecting millions of passengers daily.

**Implications**:

- Implement circuit breakers for all external dependencies including Ofcom APIs, Ordnance Survey services, and transport data feeds
- Use timeouts on all network calls with sensible defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable (e.g., serve cached coverage data if live feed is down)
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services
- Design for eventual consistency where immediate consistency is not required

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical paths
- [ ] Fault injection or chaos engineering testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined per service
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented with user-facing messaging defined

---

### 5. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards and domain-specific protocols. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 9 programme spans multiple departments (DSIT, DfT, UKRI, Geospatial Commission) and must integrate with existing government platforms, commercial telecoms operators, transport authorities, utility companies, and research institutions. The Technology Code of Practice mandates open standards. Domain-specific interoperability standards (BODS, TransXChange, INSPIRE, PAS 256) enable data exchange across organisational boundaries.

**Implications**:

- Use domain-standard data formats: TransXChange and SIRI for public transport, BODS for bus data, NaPTAN for stops, ATCO-CIF for timetables, GTFS for international interoperability
- Adopt PAS 256 for underground asset data exchange
- Publish API specifications using OpenAPI 3.0 for REST APIs and AsyncAPI for event-driven interfaces
- Version all interfaces with a documented backward compatibility strategy
- Align with GDS API technical and data standards
- Support INSPIRE metadata and data exchange standards for spatial datasets
- Use persistent identifiers (UPRN, TOID, ATCO codes, ORCID, DOI) for cross-system referencing

**Validation Gates**:

- [ ] Domain-specific data standards adopted and documented
- [ ] Interface specifications published using open standard formats
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified

---

### 6. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle Critical National Infrastructure (CNI) data — the precise locations of underground utilities, transport network control systems, broadband infrastructure topology, and nationally significant research data. A breach could enable physical attacks on infrastructure, disrupt transport networks, or compromise intellectual property of national strategic importance. The NCSC Critical National Infrastructure guidance and the National Cyber Security Strategy mandate proactive security for infrastructure-related systems.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrative access
- [ ] Service-to-service authentication using mutual TLS or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code or configuration)
- [ ] Network segmentation with minimal trust zones and deny-by-default policies
- [ ] Encryption at rest for all data stores containing infrastructure, personal, or sensitive data
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)
- [ ] CNI-specific threat modelling for infrastructure location data

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- NCSC CAF (Cyber Assessment Framework) for CNI-adjacent systems
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed for each service, including CNI threat scenarios
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] Security testing plan defined and executed before go-live
- [ ] Incident response runbook created with defined escalation paths
- [ ] NCSC Secure by Design assessment completed

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
Infrastructure systems operate continuously and serve diverse, distributed users. A transport data feed failure at 06:00 affects millions of commuters. An inaccurate coverage map wastes Project Gigabit investment. Observability must detect issues before they impact users and provide the data needed for evidence-based capacity planning.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, spatial query performance
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (coverage data records processed, funding applications submitted, asset records ingested, transport data feeds active)
- Geospatial query performance (spatial index hit rates, tile generation times)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 2 years (aligned with UK Government retention standards)
- **Application logs**: 90 days minimum for troubleshooting
- **Metrics**: 2 years with progressive aggregation for trend analysis

**Validation Gates**:

- [ ] Logging, metrics, and tracing instrumented for all services
- [ ] Dashboards configured for operational and business metrics
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for all alerting scenarios
- [ ] Capacity planning metrics tracked and reviewed monthly

---

## II. Data Principles

### 8. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and departmental data governance policies. Infrastructure data MUST be governed with additional CNI sensitivity controls where applicable.

**Rationale**:
These services process a mixture of open data (coverage maps, transport timetables), commercially sensitive data (telecoms operator network plans, utility asset details), and personal data (researcher profiles, funding applicant information). Some infrastructure location data is CNI-sensitive. Data governance must be rigorous, risk-proportionate, and auditable.

**Data Classification Tiers**:

1. **OFFICIAL — Open**: Publishable infrastructure data (aggregate coverage statistics, public transport timetables, open research outputs)
2. **OFFICIAL**: Standard government business data with baseline controls (funding applications, internal reports)
3. **OFFICIAL-SENSITIVE — Commercial**: Commercially sensitive infrastructure data (operator-specific coverage data, utility asset details under commercial confidence)
4. **OFFICIAL-SENSITIVE — CNI**: Critical National Infrastructure location data requiring enhanced access controls (precise underground asset coordinates, network topology details)

**Data Residency**:

- All data MUST reside within UK sovereign data centres
- No transfer of infrastructure data outside the UK without explicit approval from the data owner and a Data Protection Impact Assessment
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017 where applicable

**Data Retention**:

- Retention periods defined per data category aligned with departmental retention schedules
- Infrastructure data retained for the operational lifetime of the asset plus regulatory requirements
- Automatic deletion or anonymisation after the defined retention period expires
- Legal hold process documented for litigation, investigation, or audit requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows, with CNI sensitivity assessment
- [ ] UK residency confirmed for all data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental and commercial data flows
- [ ] Data Protection Impact Assessment completed where required

---

### 9. Open Data by Default

**Principle Statement**:
All non-sensitive infrastructure data SHOULD be published as open data unless there is a specific, documented reason not to. Open data MUST use open formats and be accompanied by machine-readable metadata.

**Rationale**:
The UK Government Open Data Strategy and the Geospatial Commission's policy on open data for infrastructure require that publicly funded data be made available for reuse. Open infrastructure data drives economic growth — broadband coverage data enables investment decisions, transport data powers journey planning apps, and research output data accelerates innovation. The UK's ranking on the Open Data Barometer depends on making infrastructure data available.

**Implications**:

- Publish infrastructure data on data.gov.uk with appropriate metadata
- Use open formats (CSV, GeoJSON, GeoPackage, ODS) rather than proprietary formats
- Provide API access for high-volume and real-time data (coverage feeds, transport status)
- Apply Open Government Licence (OGL) or Creative Commons licences as appropriate
- Maintain a public data catalogue with DCAT metadata for discovery
- Implement tiered access: open data freely available, commercial-in-confidence data via controlled access, CNI data via secure channels only
- Separate aggregated/anonymised data (publishable) from granular commercial data (restricted)

**Validation Gates**:

- [ ] Data publication assessment completed — each dataset categorised as open, controlled, or restricted
- [ ] Open datasets published on data.gov.uk with DCAT metadata
- [ ] Open licence applied to all openly published data
- [ ] API endpoints available for high-volume data consumers
- [ ] Reasons for restricting datasets documented and reviewed annually

---

### 10. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Decisions made using these systems — where to invest in broadband, how to route transport services, which research to fund, where underground assets are located — have significant financial and safety consequences. An inaccurate underground asset record causes utility strikes costing an average of GBP 5,000 per incident, with over 60,000 strikes per year in the UK. Poor coverage data leads to misallocated Project Gigabit funding.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; validation at point of entry
- **Consistency**: Cross-system data reconciliation with defined tolerances
- **Accuracy**: Positional accuracy targets defined per data type (e.g., +/- 0.5m for underground assets, +/- 50m for coverage predictions)
- **Timeliness**: Freshness SLAs defined and monitored per data flow (e.g., transport data within 30 seconds, coverage data within 24 hours)
- **Conformance**: Adherence to domain data models (PAS 256, TransXChange, INSPIRE)

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows
- Transformation logic version-controlled and auditable
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for schema changes
- Provenance tracking for regulatory and safety-critical data (who submitted, when, from what source)

**Validation Gates**:

- [ ] Data quality rules defined and automated with monitoring
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts defined between producers and consumers
- [ ] Schema evolution strategy documented with backward compatibility approach
- [ ] Positional accuracy targets defined and validated for geospatial data

---

### 11. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
Multiple departments and commercial operators contribute to and consume infrastructure data. A broadband coverage figure must be consistent whether viewed by DSIT policy officials, Ofcom regulators, or local authority planners. An underground asset location must be the same whether queried by a gas engineer or a water company. Contradictory data creates safety risks and undermines trust.

**Implications**:

- Identify the system of record for each data domain (e.g., Ofcom for coverage data, NaPTAN for transport stop identifiers, ORCID for researcher identifiers)
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Synchronisation strategy defined for all derived copies with documented lag tolerances
- Avoid bidirectional synchronisation — it creates split-brain scenarios and data conflicts
- Leverage cross-government authoritative sources where they exist (OS AddressBase, GOV.UK Registers)

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data

---

## III. Integration Principles

### 12. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 9 programme spans five projects across four organisations (DSIT, DfT, UKRI, Geospatial Commission). Each team must be able to develop, deploy, and evolve their service independently. Additionally, these systems integrate with dozens of external organisations (telecoms operators, transport authorities, utility companies, universities) whose systems evolve on their own schedules.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Shared libraries kept minimal; favour duplication over coupling where coordination cost exceeds duplication cost
- Avoid distributed transactions across system boundaries; use compensating actions or sagas
- Interface contracts owned by the producing team with consumer input on design

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees

---

### 13. Event-Driven Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability.

**Rationale**:
Many cross-departmental and cross-organisational workflows in the infrastructure programme are inherently asynchronous — a coverage data update from an operator does not require an immediate synchronous response from DSIT. A newly discovered underground asset does not require real-time notification to all consumers. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Infrastructure data updates from commercial operators (coverage data, asset records)
- Cross-departmental notifications (new funding award, transport disruption, asset update)
- Non-real-time business processes (batch coverage analysis, report generation, research output indexing)
- Integration with external partner systems that may be unreliable or slow
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (coverage lookup, nearest stop search, asset proximity query)
- Read-only queries where the response is needed to proceed (eligibility check during funding application)
- Transactions requiring immediate consistency within a single service boundary

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time cross-system flows
- [ ] Message durability and delivery guarantees defined (at-least-once, exactly-once)
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined
- [ ] Event replay capability available for recovery and debugging

---

## IV. Quality Attributes

### 14. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load, with particular attention to spatial query performance and real-time data feeds.

**Rationale**:
Infrastructure users expect responsive spatial queries — a utility worker looking up underground assets on-site needs results in seconds, not minutes. Transport passengers expect real-time departure information. Researchers under funding deadline pressure expect responsive application forms. Performance is a function of system value.

**Performance Targets** (to be defined per service):

- **Spatial Query Response Time**: p95 < 2 seconds for point-in-polygon and proximity queries
- **Map Tile Rendering**: < 500ms for standard zoom levels
- **Real-Time Data Feeds**: End-to-end latency < 30 seconds from source to consumer
- **API Response Time**: p95 < 200ms for non-spatial queries
- **Bulk Data Downloads**: Optimised for large dataset export (streaming, pagination, compression)

**Implications**:

- Performance requirements defined before implementation, informed by user research
- Load testing performed before every production deployment, including spatial query benchmarks
- Spatial indexing strategies (R-tree, quad-tree, H3) designed for query patterns
- Caching strategies for frequently accessed spatial tiles and reference data
- Optimise for the slowest expected client (mobile device on 3G in rural area)

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity, including spatial queries
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly

---

### 15. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss, with targets proportionate to the service criticality and user impact.

**Rationale**:
Transport data feeds serve millions of passengers daily. Underground asset data is queried before every excavation to prevent utility strikes that cause service outages and endanger workers. Broadband coverage data informs investment decisions worth hundreds of millions of pounds. Availability targets must reflect the real-world consequences of downtime.

**Availability Targets** (to be defined per service based on criticality):

- **Real-time transport data**: 99.95% availability (26 minutes downtime per year maximum)
- **Underground asset register**: 99.9% availability during working hours (Mon-Sat 06:00-22:00)
- **Coverage mapping platform**: 99.9% availability
- **Funding platform**: 99.9% availability with 99.99% during submission deadlines
- **Research collaboration hub**: 99.5% availability

**High Availability Patterns**:

- Redundancy across multiple availability zones
- Automated health checks with self-healing recovery
- Active-active configurations for real-time data services
- Regular disaster recovery testing (quarterly for critical services)

**Validation Gates**:

- [ ] Availability SLA defined per service based on user impact assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 16. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Infrastructure policy evolves — broadband universal service obligations change, transport accessibility requirements expand, research funding priorities shift with government strategy, underground asset registration requirements are updated. Systems must accommodate policy changes without requiring fundamental re-architecture. Standards evolve too (PAS 256 revisions, INSPIRE updates, new transport data formats).

**Implications**:

- Modular architecture with clear boundaries between policy logic and infrastructure concerns
- Externalise business rules (coverage thresholds, funding eligibility criteria, asset classification schemes) so policy changes do not require code deployments
- Separation of concerns: business logic, data access, spatial processing, presentation, and integration layers
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to enable confident refactoring and standard updates

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries defined with clear responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices
- [ ] Business rule changes achievable without full system redeployment

---

### 17. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing and professional-user systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Infrastructure services serve diverse users — visually impaired passengers relying on transport information, researchers with motor impairments using funding application forms, utility workers using mobile devices with gloves on construction sites. Map-based interfaces present particular accessibility challenges that must be addressed.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Provide non-visual alternatives for all map-based information (tabular views, text descriptions, screen-reader-accessible summaries)
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Publish an accessibility statement for each service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Non-visual alternatives available for all map-based content
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow connections

---

## V. Development Practices

### 18. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — all critical for government services handling CNI-adjacent data.

**Implications**:

- All infrastructure defined in declarative code within version control
- Infrastructure changes go through the same code review process as application code
- Environments are reproducible from code — no snowflake configurations
- No manual changes to production infrastructure (enforced through access controls)
- Infrastructure code versioned and deployed alongside application code

**Validation Gates**:

- [ ] All infrastructure defined as code in version control
- [ ] Infrastructure code goes through peer review before deployment
- [ ] Environments reproducible from code (tested through regular rebuilds)
- [ ] No manual infrastructure changes in production (enforced, not just policy)

---

### 19. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to any shared environment.

**Rationale**:
These systems produce data that informs investment decisions worth hundreds of millions of pounds and safety-critical operations (underground excavation, transport operations). Defects in coverage calculations, spatial queries, or funding allocations have real-world consequences. Automated testing provides a safety net that manual testing cannot match.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions and data flows (15-20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct outcomes?)
- Spatial accuracy tests (do geospatial queries return correct results within accuracy tolerances?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (do spatial queries meet latency targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- Data quality tests (do ingestion pipelines maintain quality thresholds?)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly in the pipeline
- [ ] Spatial accuracy tests validate geospatial query correctness

---

### 20. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent, manual releases. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to data standard changes, security vulnerabilities, and policy updates.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, spatial, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Deployment**: Automated deployment to environments with progressive rollout

**Quality Gates**:

- All automated tests must pass
- No critical or high security vulnerabilities
- Peer review approval required
- Accessibility checks passed
- Production deployment requires documented change approval

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes security scanning and accessibility checks
- [ ] Deployment is automated and repeatable across all environments
- [ ] Rollback capability tested and documented

---

### 21. FAIR Data Principles for Research

**Principle Statement**:
All research data and outputs within the programme MUST adhere to the FAIR principles — Findable, Accessible, Interoperable, and Reusable — to maximise the value of publicly funded research.

**Rationale**:
UKRI mandates FAIR data management for all funded research. The Research Collaboration Hub and Innovation Funding Platform must both produce and consume research data that meets FAIR standards. Non-FAIR data is effectively invisible to the research community, wasting public investment in its creation.

**FAIR Requirements**:

- **Findable**: Assign persistent identifiers (DOI for publications, ORCID for researchers), register in searchable catalogues
- **Accessible**: Provide open access where possible, with clear access conditions for restricted data
- **Interoperable**: Use community-agreed vocabularies, ontologies, and data formats
- **Reusable**: Apply clear licences, provide provenance metadata, meet domain-relevant community standards

**Implications**:

- Assign DOIs to all research outputs, datasets, and funding awards
- Use ORCID identifiers for all researcher records
- Implement research metadata standards (Dublin Core, DataCite, CERIF)
- Provide machine-readable data management plans
- Support embargo and controlled-access models for sensitive research data
- Track citation and reuse metrics for research outputs

**Validation Gates**:

- [ ] Persistent identifiers assigned to all research outputs and datasets
- [ ] FAIR assessment scoring applied to datasets and outputs
- [ ] Metadata standards implemented and validated
- [ ] Access conditions clearly documented for all research data
- [ ] Data management plan capabilities integrated into funding workflow

---

### 22. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice and GDS Service Manual require government teams to make source code open where possible. Reusing existing solutions — especially GOV.UK components, cross-government platforms, and established open source geospatial tools — reduces cost and accelerates delivery.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (GOV.UK Notify, GOV.UK Pay, GOV.UK Forms)
- Consider established open source geospatial tools (PostGIS, GeoServer, MapLibre, QGIS) before proprietary alternatives
- Use established open source components where they have active maintenance and security practices
- Publish source code openly unless it contains security-sensitive logic or CNI-related configuration
- Contribute improvements back to open source projects used by the programme
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] Government shared platforms evaluated before building bespoke alternatives
- [ ] Open source geospatial tools assessed for suitability
- [ ] Third-party dependency register maintained with licence compliance
- [ ] Source code published openly or justification documented for exceptions
- [ ] No proprietary lock-in to a single vendor's ecosystem without documented justification

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point
- Commercial partner constraints (e.g., operator data feeds in non-standard formats)

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on users and infrastructure if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 6) or Data Sovereignty (Principle 8)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] User research evidence supports design approach (Principle 2)
- [ ] Data classification and privacy approach defined (Principles 8, 9)
- [ ] Geospatial data standards approach defined (Principle 1)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed, including CNI scenarios (Principle 6)
- [ ] Accessibility approach validated, including map alternatives (Principle 17)
- [ ] Domain data standards compliance verified (Principle 5)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Spatial data quality metrics meeting defined thresholds

### Enforcement

- Architecture reviews are **mandatory** for all projects at each phase gate
- Principle violations must be remediated or exception-approved before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective compliance reviews conducted annually for live services

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | Geospatial Data as a National Asset | Strategic | CRITICAL | Spatial standards, INSPIRE compliance, accuracy targets |
| 2 | User-Centred Design | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 3 | Scalability and Elasticity | Strategic | HIGH | Load testing, spatial partitioning, scaling metrics |
| 4 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO verification |
| 5 | Interoperability and Open Standards | Strategic | HIGH | Domain standards adopted, API specs, TCoP compliance |
| 6 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC/CNI assessment |
| 7 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 8 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, CNI classification, retention policies |
| 9 | Open Data by Default | Data | HIGH | Data publication assessment, data.gov.uk listing |
| 10 | Data Quality and Lineage | Data | CRITICAL | Quality metrics, positional accuracy, lineage metadata |
| 11 | Single Source of Truth | Data | HIGH | System of record documented per domain |
| 12 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 13 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 14 | Performance and Efficiency | Quality | HIGH | Load testing, spatial query benchmarks |
| 15 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 16 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, ADRs |
| 17 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, map alternatives, assistive tech testing |
| 18 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 19 | Automated Testing | Development | HIGH | Test coverage, spatial accuracy tests |
| 20 | Continuous Integration and Deployment | Development | HIGH | Pipeline exists, security scanning |
| 21 | FAIR Data Principles | Data | HIGH | Persistent identifiers, FAIR scoring, metadata standards |
| 22 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 2 (User-Centred Design), 5 (Open Standards), 17 (Accessibility), 22 (Open Source) |
| Technology Code of Practice | 5 (Open Standards), 6 (Security), 18 (IaC), 22 (Open Source and Reuse) |
| NCSC Secure by Design | 6 (Security by Design), 18 (IaC), 19 (Automated Testing), 20 (CI/CD) |
| UK GDPR / DPA 2018 | 8 (Data Sovereignty), 10 (Data Quality) |
| INSPIRE Regulations | 1 (Geospatial Data), 5 (Interoperability), 9 (Open Data) |
| UK Digital Strategy | 1 (Geospatial), 2 (User-Centred), 5 (Interoperability), 22 (Reuse) |
| UK Geospatial Strategy | 1 (Geospatial Data), 9 (Open Data), 10 (Data Quality), 11 (Single Source of Truth) |
| National Infrastructure Strategy | 1 (Geospatial), 3 (Scalability), 4 (Resilience), 15 (Availability) |
| UKRI Open Access Policy | 9 (Open Data), 21 (FAIR Data Principles) |
| Public Sector Accessibility Regulations | 2 (User-Centred Design), 17 (Accessibility and Inclusion) |
| HM Treasury Green Book | 3 (Scalability), 14 (Performance), 15 (Availability), 22 (Reuse) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| INSPIRE Regulations | Regulation | legislation.gov.uk | Geospatial data sharing obligations | N/A — external reference |
| UK Geospatial Strategy 2030 | Strategy | Geospatial Commission | Geospatial data policy | N/A — external reference |
| PAS 256 | Standard | BSI | Underground asset data model | N/A — external reference |
| FAIR Principles | Guidance | GO FAIR | Findable, Accessible, Interoperable, Reusable | N/A — external reference |
| UK Digital Strategy 2022 | Strategy | DSIT | Digital infrastructure and innovation | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 9: Industry, Innovation and Infrastructure — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
