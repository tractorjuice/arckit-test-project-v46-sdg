# UK Government Enterprise Architecture Principles — SDG 15: Life on Land

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 15: Life on Land — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 15 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 15 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 15: Life on Land programme. These principles apply to four UK Government digital services:

- **001** — Biodiversity Net Gain Platform (DEFRA)
- **002** — Forestry Management System (Forestry Commission)
- **003** — Land Use Planning Analytics (DEFRA)
- **004** — Wildlife Crime Intelligence (NCA)

**Scope**: All technology projects, systems, and initiatives within the SDG 15 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, Environment Act 2021, and the Environmental Improvement Plan 2023.

---

## I. Strategic Principles

### 1. Environmental Data Integrity

**Principle Statement**:
All systems MUST treat environmental and ecological data as a critical national asset, ensuring its accuracy, provenance, and scientific rigour throughout the entire data lifecycle.

**Rationale**:
The SDG 15 programme underpins legally binding environmental targets — the Environment Act 2021 mandates biodiversity net gain, the UK Biodiversity Framework commits to protecting 30% of land by 2030 (30by30), and international obligations under CITES and the Convention on Biological Diversity require accurate reporting. Inaccurate environmental data leads to flawed planning decisions, habitat loss, and failure to meet statutory targets. The Biodiversity Metric 4.0 calculations that determine developer obligations depend on precise baseline habitat data.

**Implications**:

- All ecological survey data must carry provenance metadata (surveyor, methodology, date, conditions)
- Habitat condition assessments must use the Biodiversity Metric 4.0 classification and scoring system consistently
- Geospatial data must use British National Grid (OSGB36) or WGS84 with documented coordinate reference systems
- Remote sensing data (Sentinel-2, aerial photography) must include processing chain metadata and accuracy assessments
- Wildlife crime intelligence must follow the National Intelligence Model and 5x5x5 grading standards
- Data corrections must be auditable with full version history preserved

**Validation Gates**:

- [ ] Data provenance metadata schema defined and enforced at ingest
- [ ] Biodiversity Metric 4.0 calculations independently verifiable with documented inputs
- [ ] Geospatial data accuracy validated against known control points
- [ ] Data quality metrics defined per pipeline (completeness, accuracy, timeliness)
- [ ] Audit trail maintained for all data corrections and amendments

---

### 2. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Environmental services experience significant demand variation — BNG credit applications surge when major developments receive planning permission, forestry grant applications peak in planting seasons (November-March), land use change detection runs intensive batch processing on satellite imagery cycles (Sentinel-2 revisit every 5 days), and wildlife crime intelligence demand spikes during enforcement operations. Systems must handle both sustained growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (e.g., BNG mandate coming into force for small developments, major enforcement operations)

**Validation Gates**:

- [ ] System can scale horizontally (add more instances without architecture change)
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates linear capacity growth with added resources
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Cost model accounts for variable capacity and peak scenarios

---

### 3. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
These services support statutory processes with legal deadlines — BNG plans must be agreed before development can commence, felling licences have seasonal windows, and wildlife crime intelligence supports time-critical enforcement operations including CITES border seizures. System downtime directly delays planning decisions, forestry operations, and criminal investigations.

**Implications**:

- Implement circuit breakers for all external dependencies (Natural England APIs, Ordnance Survey, Sentinel Hub)
- Use timeouts on all network calls with sensible defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services
- Design for eventual consistency where immediate consistency is not required

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical paths
- [ ] Fault injection or chaos engineering testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined per service
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented and user-facing messaging defined

---

### 4. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 15 programme spans multiple organisations (DEFRA, Forestry Commission, NCA, Natural England, local planning authorities) and must integrate with existing government platforms and external data sources. The Technology Code of Practice mandates open standards to avoid lock-in and enable cross-government data sharing. Environmental data must flow between systems — habitat assessments inform planning decisions, forestry carbon data feeds national greenhouse gas inventories, and wildlife crime intelligence is shared internationally via INTERPOL and Europol.

**Implications**:

- Use open standards for geospatial data exchange (OGC WFS/WMS, GeoJSON, GeoPackage)
- Version all interfaces with a documented backward compatibility strategy
- Publish interface specifications in a discoverable API catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (GOV.UK API standards, DEFRA data services platform)
- Support OGC and INSPIRE standards for environmental spatial data

**Validation Gates**:

- [ ] Interface specifications published using open standard formats (OpenAPI, OGC)
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified in contracts
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified
- [ ] INSPIRE metadata requirements met for environmental datasets

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle sensitive data across multiple classification levels — wildlife crime intelligence includes law enforcement sensitive material (up to OFFICIAL-SENSITIVE), biodiversity credit transactions involve significant financial values, and land ownership data reveals personal information. The wildlife crime intelligence system must meet NCA security standards. A breach could compromise ongoing criminal investigations, enable environmental fraud, or expose the locations of protected species to poachers.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrative access
- [ ] Service-to-service authentication using mutual authentication or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or environment variables)
- [ ] Network segmentation with minimal trust zones and deny-by-default policies
- [ ] Encryption at rest for all data stores containing personal or sensitive data
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)
- [ ] Protected species location data subject to additional access controls and redaction rules

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10 (for application-layer controls)
- NCA security standards (for wildlife crime intelligence)

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed for each service
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] Security testing plan defined and executed before go-live
- [ ] Incident response runbook created with defined escalation paths
- [ ] NCSC Secure by Design assessment completed

---

### 6. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. For services underpinning statutory environmental processes, operational blindness directly translates to undetected service degradation affecting planning decisions, grant payments, and enforcement operations. Instrumentation is a first-class architectural requirement.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (BNG credits issued, felling licences processed, habitat assessments completed, intelligence submissions received)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 7 years (aligned with criminal investigation requirements)
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

### 7. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with regulatory requirements, corporate data governance policies, and environmental data sharing obligations.

**Data Classification Tiers**:

1. **PUBLIC**: Published environmental data, open datasets (habitat maps, woodland inventories)
2. **OFFICIAL**: Standard operational data (BNG applications, felling licence records, land use assessments)
3. **OFFICIAL-SENSITIVE**: Protected species locations, wildlife crime intelligence (5x5x5 graded), commercially sensitive biodiversity credit valuations
4. **SECRET**: NCA operational intelligence relating to organised wildlife trafficking networks (managed within NCA secure infrastructure)

**Data Residency**:

- All data must reside within UK sovereign data centres
- Environmental data subject to INSPIRE Directive transposition requirements for publication
- Wildlife crime intelligence shared internationally only through authorised CITES/INTERPOL channels

**Data Retention**:

- Environmental monitoring data: Permanent retention (national environmental record)
- BNG habitat management plans: Minimum 30 years (aligned with statutory habitat management period)
- Wildlife crime intelligence: Aligned with Management of Police Information (MoPI) retention schedules
- Application and transaction data: 7 years minimum for audit purposes
- Legal hold process for active investigations and litigation

**Validation Gates**:

- [ ] Data classification performed for all data stores
- [ ] Residency requirements mapped to infrastructure
- [ ] Retention policies configured with automated lifecycle management
- [ ] Access controls enforce least privilege and need-to-know
- [ ] INSPIRE metadata publication obligations documented and automated

---

### 8. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability and troubleshooting.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; habitat surveys must include all mandatory Biodiversity Metric 4.0 fields
- **Consistency**: Cross-system data reconciliation between DEFRA, Natural England, and Local Planning Authority datasets
- **Accuracy**: Ecological data validated against known habitat classification standards; geospatial accuracy within defined tolerances
- **Timeliness**: Satellite imagery processed within 48 hours of acquisition; BNG credit status updates reflected within 4 hours

**Lineage Requirements**:

- Source-to-target mapping documented for all environmental data flows
- Transformation logic version-controlled and reviewable (particularly Biodiversity Metric calculations)
- Data quality metrics tracked per pipeline with automated alerting on threshold breaches
- Impact analysis capability for changes to habitat classification standards or metric weightings

**Validation Gates**:

- [ ] Data quality rules defined and automated for all pipelines
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts between producers and consumers documented
- [ ] Schema evolution strategy documented with impact assessment process

---

### 9. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies must be clearly labelled and synchronised.

**Rationale**:
Environmental data is consumed by multiple systems — habitat baseline data informs BNG calculations, forestry data, and land use analytics. Multiple authoritative sources create inconsistency, reconciliation overhead, and regulatory risk. A single BNG credit appearing in two registries would be catastrophic.

**Authoritative Sources**:

- **Habitat data**: Natural England habitat inventory (master), consumed by BNG Platform and Land Use Analytics
- **Woodland data**: Forestry Commission National Forest Inventory (master), consumed by Land Use Analytics
- **Species records**: National Biodiversity Network (NBN) Atlas (master), consumed by all projects
- **Land parcel data**: Ordnance Survey MasterMap and Rural Payments Agency Land Parcel Identification System
- **Wildlife crime intelligence**: NCA National Wildlife Crime Unit (master)

**Validation Gates**:

- [ ] System of record identified for each data entity
- [ ] Derived copies documented with sync frequency and staleness tolerance
- [ ] No bidirectional sync without conflict resolution strategy
- [ ] Master data management strategy defined for shared reference data (habitat classifications, species lists)

---

## III. Integration Principles

### 10. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, file systems, or tight runtime dependencies.

**Rationale**:
Loose coupling enables independent deployment, technology diversity, team autonomy, and system evolution. The SDG 15 programme spans organisationally independent bodies (DEFRA, Forestry Commission, NCA) with different technology stacks, security requirements, and delivery cadences. Tight coupling would create delivery bottlenecks and operational fragility.

**Implications**:

- Communicate through published APIs or asynchronous events
- No direct database access across system boundaries
- Each system manages its own data lifecycle
- Shared libraries kept minimal (favour duplication over coupling)
- Avoid distributed transactions across systems
- BNG credit registry must be independently deployable from the habitat assessment service

**Validation Gates**:

- [ ] Systems communicate via APIs or events, not shared databases
- [ ] No shared mutable state across organisational boundaries
- [ ] Each system has independent data store
- [ ] Deployment of one system does not require deployment of another
- [ ] Interface changes versioned with backward compatibility

---

### 11. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous communication for non-real-time interactions to improve resilience and decoupling.

**Rationale**:
Asynchronous patterns reduce temporal coupling, improve fault tolerance, and enable better scalability. Environmental data processing — satellite imagery analysis, batch habitat scoring, intelligence report distribution — is inherently suited to asynchronous processing.

**When to Use Async**:

- Satellite imagery ingest and land use change detection processing
- BNG credit lifecycle events (application submitted, assessment complete, credit issued)
- Wildlife crime intelligence distribution to partner agencies
- Forestry grant application workflow stages
- Automated environmental impact notifications to Local Planning Authorities

**When Synchronous is Acceptable**:

- Real-time BNG credit balance queries during planning application decisions
- Interactive habitat condition assessment tools
- Wildlife crime intelligence search queries during active operations
- User-facing form submissions requiring immediate validation

**Validation Gates**:

- [ ] Async patterns used for non-real-time flows
- [ ] Message durability and delivery guarantees defined
- [ ] Event schemas versioned and published
- [ ] Dead letter queues and error handling configured

---

## IV. Quality Attributes

### 12. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected load with efficient use of computational resources.

**Performance Targets** (define for each system):

- **Response Time**: p50, p95, p99 latency targets per operation type
- **Throughput**: Requests per second, batch processing items per hour
- **Concurrency**: Simultaneous user and API consumer capacity
- **Resource Efficiency**: CPU/memory utilisation targets, satellite imagery processing throughput

**Implications**:

- Performance requirements defined before implementation
- Load testing performed before production deployment
- Performance monitoring continuous, not just point-in-time
- Optimise hot paths identified through profiling (particularly Biodiversity Metric calculations and geospatial queries)
- Caching strategies for expensive operations (habitat classification lookups, species distribution maps)

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at expected capacity
- [ ] Performance metrics monitored in production
- [ ] Capacity planning model defined

---

### 13. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Availability Targets**:

- **BNG Platform**: 99.9% (planning decisions depend on credit availability queries)
- **Forestry Management System**: 99.5% (seasonal peaks during planting season)
- **Land Use Analytics**: 99.0% (batch processing tolerant of planned downtime)
- **Wildlife Crime Intelligence**: 99.9% (operational intelligence must be available for enforcement actions)

**High Availability Patterns**:

- Redundancy across availability zones
- Automated health checks and failover
- Active-active for BNG credit registry and wildlife crime intelligence
- Regular disaster recovery testing

**Validation Gates**:

- [ ] Availability SLA defined per service
- [ ] RTO and RPO requirements documented
- [ ] Redundancy strategy implemented
- [ ] Failover tested regularly
- [ ] Backup and restore procedures validated

---

### 14. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and comprehensive documentation.

**Rationale**:
Environmental policy evolves — the Biodiversity Metric is regularly updated (currently 4.0, with future versions expected), habitat classification standards change, and wildlife crime legislation is amended. Systems must accommodate policy changes without major re-engineering.

**Implications**:

- Biodiversity Metric calculation logic externalised as configurable rules, not hard-coded
- Habitat classification taxonomies managed as reference data, not compiled constants
- Architecture Decision Records (ADRs) for all significant technology and design choices
- Automated testing to enable confident refactoring when metric or policy changes occur

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records document key choices
- [ ] Policy-dependent logic externalised and configurable

---

## V. Development Practices

### 15. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines.

**Rationale**:
Manual infrastructure changes create drift, inconsistency, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery. For systems handling statutory environmental data, infrastructure reproducibility is essential for audit and compliance.

**Validation Gates**:

- [ ] Infrastructure defined as code
- [ ] Infrastructure code version-controlled
- [ ] Automated deployment pipeline for infrastructure
- [ ] No manual infrastructure changes in production

---

### 16. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to production.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions, API contracts, geospatial query accuracy (15-20% of tests)
- **End-to-End Tests**: Critical user journeys — BNG credit application lifecycle, felling licence workflow, intelligence submission (5-10% of tests)

**Required Test Types**:

- Functional tests (does it work?)
- Performance tests (is it fast enough for Biodiversity Metric calculations at scale?)
- Security tests (is it secure, particularly for wildlife crime intelligence?)
- Resilience tests (does it handle failures gracefully?)
- Data quality tests (are environmental calculations accurate?)

**Validation Gates**:

- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical paths have end-to-end tests
- [ ] Performance tests run regularly
- [ ] Biodiversity Metric calculation accuracy validated against reference datasets

---

### 17. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution including environmental data validation
4. **Security Scan**: Dependency and code vulnerability scanning
5. **Deployment**: Automated deployment to environments

**Quality Gates**:

- All tests must pass (including Biodiversity Metric accuracy tests)
- No critical security vulnerabilities
- Code review approval required
- Environmental data schema validation passed
- Deployment requires production readiness checklist

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists
- [ ] Pipeline includes security scanning
- [ ] Deployment is automated and repeatable
- [ ] Rollback capability tested

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance (e.g., NCA legacy system integration)
- Regulatory or legal requirements (e.g., CITES reporting format mandates)
- Transitional state during migration from legacy environmental systems
- Pilot/proof-of-concept with defined end date

**Exception Request Requirements**:

- [ ] Justification with business/technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound)
- [ ] Remediation plan to achieve compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team
2. Review by architecture review board
3. CTO/CIO approval for exceptions to critical principles
4. Document exception in project architecture documentation
5. Regular review of exceptions (quarterly)

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood
- [ ] High-level approach aligns with principles
- [ ] No obvious principle violations
- [ ] Environmental data standards identified

**Beta/Design**:

- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Security and data principles validated
- [ ] Environmental data lineage documented

**Pre-Production**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified
- [ ] Environmental data quality thresholds met

### Enforcement

- Architecture reviews are **mandatory** for all projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective reviews for compliance on live systems

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | Environmental Data Integrity | Strategic | CRITICAL | Provenance metadata, metric accuracy |
| 2 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 3 | Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO |
| 4 | Interoperability and Open Standards | Strategic | HIGH | API specs, OGC/INSPIRE compliance |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing |
| 6 | Observability | Strategic | HIGH | Metrics, logs, traces |
| 7 | Data Sovereignty and Governance | Data | CRITICAL | Classification, retention, INSPIRE |
| 8 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 9 | Single Source of Truth | Data | HIGH | Authoritative sources defined |
| 10 | Loose Coupling | Integration | HIGH | Deployment independence |
| 11 | Asynchronous Communication | Integration | MEDIUM | Async patterns used |
| 12 | Performance and Efficiency | Quality | HIGH | Load testing |
| 13 | Availability and Reliability | Quality | CRITICAL | SLA monitoring |
| 14 | Maintainability and Evolvability | Quality | HIGH | Configurable policy logic |
| 15 | Infrastructure as Code | DevOps | HIGH | IaC coverage |
| 16 | Automated Testing | DevOps | HIGH | Test coverage |
| 17 | CI/CD | DevOps | HIGH | Pipeline exists |

### Environmental Legislation and Standards Reference

| Legislation / Standard | Relevance | Projects Affected |
|------------------------|-----------|-------------------|
| Environment Act 2021 | Mandatory BNG, biodiversity targets, habitat regulations | 001, 002, 003 |
| Biodiversity Metric 4.0 | Calculation standard for habitat value | 001, 003 |
| England Trees Action Plan 2021 | Woodland creation targets, tree planting | 002 |
| Wildlife and Countryside Act 1981 | Protected species and habitats | 001, 003, 004 |
| CITES (Convention on International Trade in Endangered Species) | International wildlife trade controls | 004 |
| UK Biodiversity Framework | 30by30 target, species recovery | 001, 002, 003 |
| Environmental Improvement Plan 2023 | Apex environmental targets | 001, 002, 003 |
| Forestry Act 1967 | Felling licence requirements | 002 |
| UK Woodland Carbon Code | Carbon credit verification | 002 |
| INSPIRE Regulations 2009 | Environmental spatial data publication | 001, 002, 003 |
| National Intelligence Model | Intelligence grading and management | 004 |
| Proceeds of Crime Act 2002 | Financial investigation of wildlife crime | 004 |

---

**Document Version History**

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-28 | ArcKit AI | Initial draft |
| 1.0 | 2026-03-28 | ArcKit AI | Ratified version |

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Environment Act 2021 | Legislation | legislation.gov.uk | BNG mandate, biodiversity targets | N/A |
| Biodiversity Metric 4.0 | Technical Standard | Natural England | Habitat scoring methodology | N/A |
| Environmental Improvement Plan 2023 | Policy | DEFRA | Apex environmental targets | N/A |
| Technology Code of Practice | Standard | CDDO | Open standards, cloud-first | N/A |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 15: Life on Land
**Model**: Claude Opus 4.6
