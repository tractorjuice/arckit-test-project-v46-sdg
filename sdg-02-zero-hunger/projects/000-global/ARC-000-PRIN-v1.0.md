# SDG 2 Zero Hunger -- Enterprise Architecture Principles

> **Template Origin**: Official | **ArcKit Version**: 4.1.1 | **Command**: `/arckit:principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 2 Zero Hunger -- Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-09 |
| **Last Modified** | 2026-03-09 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-09 |
| **Owner** | Chief Architect, SDG 2 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 2 project teams (DEFRA, DfE, Cabinet Office) |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-09 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the architecture principles governing all technology decisions across the five SDG 2 Zero Hunger projects: Food Supply Chain Resilience Platform (DEFRA), School Meals Management System (DfE), Food Waste Reduction Analytics (DEFRA), Agricultural Subsidy Management (DEFRA), and National Food Strategy Dashboard (Cabinet Office).

These principles ensure consistency, security, interoperability, and alignment with UK Government technology standards across all projects and initiatives within the programme.

**Scope**: All SDG 2 technology projects, systems, and initiatives across DEFRA, DfE, and Cabinet Office
**Authority**: SDG 2 Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process

**Philosophy**: These principles are **technology-agnostic** -- they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**UK Government Alignment**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Secure by Design principles, and the Government Functional Standard GovS 005 (Digital).

---

## I. Strategic Principles

### 1. User-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of their users, validated through research and testing with real users, and continuously improved based on evidence.

**Rationale**:
The GDS Service Standard mandates user-centred design for UK Government services. Food systems serve diverse users -- farmers, school administrators, policy analysts, citizens, food inspectors -- each with distinct needs and digital capabilities.

**Implications**:

- Conduct user research before and during development
- Design services that are inclusive and accessible to all users regardless of ability
- Prioritise user needs over internal organisational structures
- Test services with representative users across all projects
- Cross-reference user needs between the three DEFRA projects (001, 003, 004) where user groups overlap

**Validation Gates**:

- [ ] User research conducted with representative users
- [ ] User needs documented and prioritised
- [ ] Usability testing performed at each phase
- [ ] Accessibility audit completed (WCAG 2.2 Level AA minimum)
- [ ] User satisfaction metrics defined and tracked

---

### 2. Accessibility and Inclusion (NON-NEGOTIABLE)

**Principle Statement**:
All public-facing services MUST meet WCAG 2.2 Level AA as a minimum and comply with the Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018. Internal tools SHOULD meet the same standard.

**Rationale**:
Accessibility is a legal requirement for UK public sector digital services. The School Meals Management System (002) and Agricultural Subsidy Management (004) serve users with widely varying digital literacy and ability, making inclusive design essential.

**Implications**:

- Build accessibility into design from the start, not as a retrofit
- Support assistive technologies (screen readers, voice control, switch access)
- Provide alternative formats for content where needed
- Ensure colour contrast, text sizing, and navigation meet WCAG 2.2 AA
- Test with disabled users and assistive technology users
- Publish an accessibility statement for each public-facing service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Accessibility statement published and current
- [ ] Tested with assistive technologies
- [ ] Content available in alternative formats where required
- [ ] Accessibility included in acceptance criteria for all user stories

---

### 3. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load.

**Rationale**:
Demand patterns across SDG 2 projects are seasonal and event-driven. Agricultural subsidy windows create predictable peaks; food supply chain disruptions create unpredictable surges. The National Food Strategy Dashboard (005) must handle increased demand during policy announcements.

**Implications**:

- Design for stateless components that can be replicated
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Model seasonal demand patterns (school term times, harvest periods, subsidy windows)

**Validation Gates**:

- [ ] System can scale horizontally (add more instances)
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined
- [ ] Cost model accounts for variable capacity
- [ ] Seasonal demand profiles documented and tested

---

### 4. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
The Food Supply Chain Resilience Platform (001) is itself a resilience tool -- it cannot afford to be unavailable during the crises it monitors. All SDG 2 systems support critical government functions where downtime has direct impact on citizens.

**Implications**:

- Implement circuit breakers for external dependencies
- Use timeouts on all network calls
- Retry with exponential backoff for transient failures
- Graceful degradation when non-critical services fail
- Automated health checks and recovery
- Avoid cascading failures through bulkhead isolation
- Define explicit degraded-mode behaviour for each service

**Validation Gates**:

- [ ] Failure modes identified and mitigated for each external dependency
- [ ] Chaos engineering or fault injection testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined
- [ ] Automated failover tested
- [ ] Degraded mode behaviour documented and tested

---

### 5. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited. Preference MUST be given to open standards over proprietary protocols.

**Rationale**:
The Technology Code of Practice requires use of open standards. The five SDG 2 projects span three departments (DEFRA, DfE, Cabinet Office) and must interoperate. The National Food Strategy Dashboard (005) aggregates data from all other projects, making standard interfaces essential.

**Implications**:

- Use standardised, open protocols for all interfaces
- Version all interfaces with backward compatibility strategy
- Publish interface specifications as machine-readable contracts
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Adopt existing cross-government standards (e.g., registers, reference data)
- Use open data formats for public datasets

**Validation Gates**:

- [ ] Interface specifications published using open standard formats
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified
- [ ] No direct database coupling across systems
- [ ] Open standards used in preference to proprietary alternatives

---

### 6. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles, aligned with NCSC guidance and the Secure by Design framework. Security is NOT a feature to be added later -- it is a foundational requirement.

**Rationale**:
SDG 2 systems handle sensitive data including personal information (school meals eligibility, farmer financial data), supply chain intelligence, and agricultural subsidy payments. Compromise could affect food security, citizen finances, and government credibility.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest
4. **Continuous Verification**: Monitor, log, and analyse all access patterns

**Mandatory Controls**:

- [ ] Multi-factor authentication for all human access
- [ ] Service-to-service authentication (mutual authentication or signed tokens)
- [ ] Secrets management via secure vault (never in code or configuration files)
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest for all data stores
- [ ] Encrypted transport for all network communication
- [ ] Structured logging of all authentication/authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning)
- [ ] Dependency scanning for known vulnerabilities in supply chain

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus (mandatory)
- NCSC Cloud Security Principles
- NIST Cybersecurity Framework (reference)
- ISO 27001 (where contractually required)
- Cyber Assessment Framework (CAF) for critical national infrastructure elements

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to requirements
- [ ] Security testing plan defined and executed
- [ ] Incident response runbook created
- [ ] NCSC Secure by Design assessment completed

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. The Food Supply Chain Resilience Platform (001) and National Food Strategy Dashboard (005) require real-time operational awareness. All systems must support the government's operational capability requirements.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs across service boundaries
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates
- **Tracing**: Distributed trace context for request flows across services
- **Alerting**: Service Level Objective (SLO)-based alerting with actionable runbooks

**Required Instrumentation**:

- Request volume, latency distribution, error rate
- Resource utilisation (CPU, memory, I/O, network)
- Business metrics (transactions processed, data freshness, user actions)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: 7 years (aligned with government records retention)
- **Application logs**: 90 days minimum
- **Metrics**: 2 years with progressive aggregation

**Validation Gates**:

- [ ] Logging, metrics, tracing instrumented for all services
- [ ] Dashboards and alerts configured
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for common failure scenarios
- [ ] Capacity planning metrics tracked

---

## II. Data Principles

### 8. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and departmental data governance policies. All personal data MUST be stored and processed within UK jurisdiction unless explicitly authorised.

**Data Classification Tiers** (aligned with UK Government Security Classifications):

1. **OFFICIAL-PUBLIC**: Open data, published statistics, public dashboards
2. **OFFICIAL**: Internal operational data, non-sensitive business data
3. **OFFICIAL-SENSITIVE**: Personal data, commercial data, subsidy payment details, supply chain intelligence
4. **SECRET**: National security-related food supply intelligence (if applicable, handled under separate controls)

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- Cross-border data transfers require Data Protection Impact Assessment (DPIA) and appropriate safeguards
- Data processed by third parties requires Data Processing Agreements (DPAs)

**Data Retention**:

- Automatic deletion after defined retention period
- Legal hold process for Freedom of Information (FOI) requests and litigation
- Backup retention aligned with compliance and recovery requirements
- Agricultural subsidy records retained per EU Withdrawal Act requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores
- [ ] UK data residency confirmed for personal data
- [ ] Retention policies configured with automated deletion
- [ ] Access controls enforce least privilege and need-to-know
- [ ] Data Protection Impact Assessment (DPIA) completed where required

---

### 9. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability and troubleshooting.

**Rationale**:
The Food Waste Reduction Analytics project (003) and National Food Strategy Dashboard (005) depend on accurate, timely data from multiple sources. Poor data quality in Agricultural Subsidy Management (004) could lead to incorrect payments.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields
- **Consistency**: Cross-system data reconciliation (especially between DEFRA projects)
- **Accuracy**: Validation rules and constraints enforced at source
- **Timeliness**: Freshness Service Level Agreements (SLAs) defined and monitored

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows
- Transformation logic version-controlled and reviewable
- Data quality metrics tracked per pipeline
- Impact analysis capability for schema changes

**Validation Gates**:

- [ ] Data quality rules defined and automated
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts defined between producers and consumers
- [ ] Schema evolution strategy documented
- [ ] Data quality dashboards operational

---

### 10. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies must be clearly labelled and synchronised. The National Food Strategy Dashboard (005) MUST consume, not duplicate, authoritative data from source systems.

**Rationale**:
Multiple authoritative sources create inconsistency, reconciliation overhead, and data integrity issues. With five projects sharing food and agriculture data, clear ownership prevents conflict.

**Data Domain Ownership**:

| Data Domain | Authoritative Source | Consuming Projects |
|-------------|---------------------|--------------------|
| Supply chain risk data | 001 Food Supply Chain Resilience | 005 National Food Strategy Dashboard |
| School meals eligibility | 002 School Meals Management | 005 National Food Strategy Dashboard |
| Food waste metrics | 003 Food Waste Reduction Analytics | 005 National Food Strategy Dashboard |
| Subsidy and land management | 004 Agricultural Subsidy Management | 001, 003, 005 |
| Aggregated food strategy KPIs | 005 National Food Strategy Dashboard | External stakeholders |

**Implications**:

- Identify the system of record for each data domain
- Derived/cached copies are read-only and clearly labelled as such
- Synchronisation strategy defined for all derived copies
- Avoid bidirectional synchronisation (creates split-brain scenarios)

**Validation Gates**:

- [ ] System of record identified for each data entity
- [ ] Derived copies documented with synchronisation frequency
- [ ] No bidirectional synchronisation without conflict resolution strategy
- [ ] Master data management approach for shared reference data (farm identifiers, school identifiers, food categories)

---

### 11. Privacy by Design

**Principle Statement**:
All systems processing personal data MUST implement privacy by design and by default, complying with UK GDPR Article 25 and the Data Protection Act 2018.

**Rationale**:
The School Meals Management System (002) processes children's personal data and eligibility information. Agricultural Subsidy Management (004) processes farmer financial data. Both require heightened privacy protections.

**Implications**:

- Minimise personal data collection to what is strictly necessary
- Implement purpose limitation -- data used only for stated purposes
- Provide data subject rights mechanisms (access, rectification, erasure, portability)
- Pseudonymise or anonymise data for analytics where possible
- Conduct Data Protection Impact Assessments (DPIAs) for high-risk processing
- Implement consent management where required
- Apply special category data protections for children's data (002)

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed
- [ ] Privacy notice published and accessible
- [ ] Data subject rights processes operational
- [ ] Data minimisation evidenced in data model
- [ ] Lawful basis documented for each processing activity
- [ ] Children's data handled with enhanced protections where applicable

---

## III. Integration Principles

### 12. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, file systems, or tight runtime dependencies.

**Rationale**:
The five SDG 2 projects span three government departments with different release cadences, operational teams, and technology maturity. Loose coupling enables each project to evolve independently while maintaining interoperability.

**Implications**:

- Communicate through published APIs or asynchronous events
- No direct database access across system boundaries
- Each system manages its own data lifecycle
- Shared libraries kept minimal (favour duplication over coupling)
- Avoid distributed transactions across systems
- Cross-departmental integration through well-defined contracts

**Validation Gates**:

- [ ] Systems communicate via APIs or events, not shared databases
- [ ] No shared mutable state between systems
- [ ] Each system has independent data store
- [ ] Deployment of one system does not require deployment of another
- [ ] Interface changes versioned with backward compatibility

---

### 13. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous communication for non-real-time interactions to improve resilience and decoupling.

**Rationale**:
Cross-departmental data flows (DEFRA to Cabinet Office, DfE to Cabinet Office) do not require real-time synchronisation. Asynchronous patterns improve resilience when one department's systems are unavailable.

**When to Use Async**:

- Data aggregation feeds to the National Food Strategy Dashboard (005)
- Food waste metric reporting from supply chain partners
- Agricultural subsidy processing workflows
- Cross-departmental notifications and alerts

**When Synchronous is Acceptable**:

- Real-time user interactions (eligibility checks in 002, subsidy applications in 004)
- Query operations within a single system
- Authentication and authorisation flows

**Validation Gates**:

- [ ] Asynchronous patterns used for cross-departmental data flows
- [ ] Message durability and delivery guarantees defined
- [ ] Event schemas versioned and published
- [ ] Dead letter handling and error recovery configured
- [ ] Eventual consistency acceptable and documented for async flows

---

### 14. Reuse and Shared Platforms

**Principle Statement**:
Projects SHOULD reuse existing cross-government platforms and shared services before building custom solutions. Common capabilities across SDG 2 projects SHOULD be shared.

**Rationale**:
The Technology Code of Practice mandates reuse of existing government platforms. The three DEFRA projects (001, 003, 004) share common needs for geospatial data, farm identifiers, and agricultural reference data.

**Cross-Government Platforms to Consider**:

- GOV.UK Notify for notifications and correspondence
- GOV.UK Pay for subsidy payments and school meal transactions
- GOV.UK Sign In for citizen authentication
- GOV.UK Registers for authoritative reference data
- OS Data Hub for geospatial and mapping services

**Shared Capabilities Across SDG 2 Projects**:

- Authentication and authorisation
- Notification services
- Geospatial data processing (001, 003, 004)
- Reporting and dashboards
- Document management
- Audit logging

**Validation Gates**:

- [ ] Cross-government platforms evaluated before building custom
- [ ] Shared capabilities identified and architecture agreed
- [ ] Duplication of capability justified where it exists
- [ ] Reuse decisions documented in Architecture Decision Records (ADRs)

---

## IV. Quality Attributes

### 15. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected load with efficient use of computational resources.

**Performance Targets** (to be defined per system):

- **Response Time**: p50, p95, p99 latency targets per transaction type
- **Throughput**: Transactions per second appropriate to user base
- **Concurrency**: Simultaneous user capacity based on demand modelling
- **Resource Efficiency**: Cost-per-transaction targets

**Domain-Specific Considerations**:

- Food Supply Chain Resilience (001): Near-real-time alert processing for supply disruptions
- School Meals (002): Peak performance during term-start eligibility checking windows
- Food Waste Analytics (003): Batch processing efficiency for large datasets
- Agricultural Subsidy (004): Payment processing within government payment SLAs
- National Food Strategy Dashboard (005): Dashboard render times under peak policy interest

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at expected and peak capacity
- [ ] Performance metrics monitored in production
- [ ] Capacity planning model defined with cost projections

---

### 16. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Availability Expectations**:

| System Type | Minimum Availability | RTO | RPO |
|-------------|---------------------|-----|-----|
| Citizen-facing services (002, 004) | > 99.9% | < 1 hour | < 15 minutes |
| Operational dashboards (001, 005) | > 99.5% | < 4 hours | < 1 hour |
| Analytical platforms (003) | > 99.0% | < 8 hours | < 4 hours |

**High Availability Patterns**:

- Redundancy across availability zones
- Automated health checks and failover
- Active-active or active-passive configurations based on criticality
- Regular disaster recovery testing (at least annually)

**Validation Gates**:

- [ ] Availability SLA defined per system
- [ ] RTO and RPO requirements documented and tested
- [ ] Redundancy strategy implemented
- [ ] Failover tested regularly
- [ ] Backup and restore procedures validated
- [ ] Disaster recovery plan tested within the last 12 months

---

### 17. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and comprehensive documentation.

**Rationale**:
Food policy evolves with government priorities, post-Brexit regulatory changes, and emerging food security challenges. Systems must adapt without wholesale replacement.

**Implications**:

- Modular architecture with clear boundaries
- Separation of concerns (business logic, data access, presentation)
- Code is self-documenting with meaningful names
- Architecture Decision Records (ADRs) for significant choices
- Automated testing to enable confident refactoring
- Configuration externalised from code for policy rules (eligibility criteria, subsidy rates, food categories)

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices
- [ ] Policy rules externalised and configurable without code changes

---

## V. Development Practices

### 18. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines.

**Rationale**:
Manual infrastructure changes create drift, inconsistency, and undocumented state. Infrastructure as Code (IaC) enables repeatability, auditability, and disaster recovery across all five projects.

**Implications**:

- All infrastructure defined in declarative code
- Infrastructure changes go through code review
- Environments are reproducible from code
- No manual changes to production infrastructure
- Infrastructure versioned alongside application code
- Separate environments for development, testing, staging, and production

**Validation Gates**:

- [ ] Infrastructure defined as code
- [ ] Infrastructure code version-controlled
- [ ] Automated deployment pipeline for infrastructure
- [ ] No manual infrastructure changes in production
- [ ] Environment parity verified

---

### 19. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to production.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions (15-20% of tests)
- **End-to-End Tests**: Critical user journeys (5-10% of tests)

**Required Test Types**:

- Functional tests (does it work correctly?)
- Performance tests (does it meet response time targets?)
- Security tests (does it resist known attack vectors?)
- Accessibility tests (does it meet WCAG 2.2 AA?)
- Resilience tests (does it handle failures gracefully?)

**Validation Gates**:

- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly
- [ ] Accessibility tests included in CI pipeline

---

### 20. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution (unit, integration, accessibility)
4. **Security Scan**: Dependency scanning, static analysis, and secrets detection
5. **Deployment**: Automated deployment to environments
6. **Verification**: Smoke tests and health checks post-deployment

**Quality Gates**:

- All tests must pass
- No critical or high security vulnerabilities
- Code review approval required
- Accessibility checks pass
- Deployment requires production readiness checklist

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists
- [ ] Pipeline includes security and accessibility scanning
- [ ] Deployment is automated and repeatable
- [ ] Rollback capability tested and documented
- [ ] Change management process followed for production deployments

---

## VI. Government-Specific Principles

### 21. Technology Code of Practice Compliance

**Principle Statement**:
All technology decisions MUST comply with the UK Government Technology Code of Practice (TCoP) and be assessed against its 12 points.

**Rationale**:
TCoP compliance is mandatory for UK central government technology spending. It ensures alignment with government digital strategy and value for money.

**Key TCoP Points Relevant to SDG 2**:

- Define user needs (Point 1) -- align with Principle 1
- Make things accessible and inclusive (Point 2) -- align with Principle 2
- Be open and use open source (Point 3) -- prefer open source where appropriate
- Make use of open standards (Point 4) -- align with Principle 5
- Use cloud first (Point 5) -- prefer cloud hosting models
- Make things secure (Point 6) -- align with Principle 6
- Make privacy integral (Point 7) -- align with Principle 11
- Share, reuse, and collaborate (Point 8) -- align with Principle 14
- Integrate and adapt technology (Point 9) -- avoid lock-in
- Make better use of data (Point 10) -- align with Data Principles
- Define your purchasing strategy (Point 11) -- use government frameworks
- Meet the Service Standard (Point 12) -- comply with GDS Service Standard

**Validation Gates**:

- [ ] TCoP assessment completed for each project
- [ ] Spend control approval obtained where required
- [ ] Open source alternatives evaluated
- [ ] Vendor lock-in risks assessed and mitigated

---

### 22. Vendor Independence and Avoiding Lock-in

**Principle Statement**:
All systems SHOULD be designed to avoid dependency on a single vendor, proprietary format, or platform. Where proprietary services are used, exit strategies MUST be documented.

**Rationale**:
Government procurement rules require competitive tendering. Vendor lock-in restricts future options, increases costs, and reduces the ability to switch providers.

**Implications**:

- Use open standards and open data formats
- Abstract vendor-specific capabilities behind standard interfaces
- Ensure data can be exported in open formats
- Document exit strategy and data migration approach for each vendor dependency
- Prefer multi-cloud or cloud-agnostic patterns where cost-effective
- Include data portability clauses in contracts

**Validation Gates**:

- [ ] Vendor dependencies documented with exit strategies
- [ ] Data exportable in open, standard formats
- [ ] No proprietary APIs without abstraction layers
- [ ] Contract includes data portability and exit provisions
- [ ] Alternative vendors identified for critical services

---

## VII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the SDG 2 Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance
- Regulatory or legal requirements
- Transitional state during migration (time-bound)
- Pilot or proof-of-concept with defined end date
- Cost-prohibitive compliance with documented cost-benefit analysis

**Exception Request Requirements**:

- [ ] Justification with business and technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound, maximum 12 months)
- [ ] Remediation plan to achieve compliance

**Approval Process**:

1. Submit exception request to the SDG 2 Architecture team
2. Review by SDG 2 Architecture Review Board
3. Senior Responsible Owner (SRO) approval for exceptions to critical principles (2, 6, 11)
4. Document exception in project Architecture Decision Records (ADRs)
5. Quarterly review of all active exceptions

**Non-Negotiable Principles** (no exceptions permitted):

- Principle 2: Accessibility and Inclusion
- Principle 6: Security by Design
- Principle 11: Privacy by Design

---

## VIII. Governance and Compliance

### Architecture Review Gates

All SDG 2 projects must pass architecture reviews at key milestones, aligned with the GDS service phases:

**Discovery**:

- [ ] Architecture principles understood by project team
- [ ] High-level approach aligns with principles
- [ ] User needs identified and validated
- [ ] No obvious principle violations

**Alpha**:

- [ ] Architecture options explored with ADRs
- [ ] Prototypes tested against key quality attributes
- [ ] Security and data principles validated
- [ ] Cross-project dependencies identified

**Beta**:

- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Integration points with other SDG 2 projects tested
- [ ] Accessibility and security assessments completed

**Live**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified
- [ ] Monitoring and alerting operational
- [ ] Disaster recovery tested

### Enforcement

- Architecture reviews are **mandatory** for all SDG 2 projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound (maximum 12 months) and reviewed quarterly
- Retrospective reviews for compliance on live systems conducted annually
- Cross-project consistency reviews conducted quarterly across all five projects

---

## IX. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | User-Centred Design | Strategic | HIGH | User research, usability testing |
| 2 | Accessibility and Inclusion | Strategic | CRITICAL | WCAG 2.2 AA audit |
| 3 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 4 | Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO |
| 5 | Interoperability and Open Standards | Strategic | HIGH | API specs, versioning |
| 6 | Security by Design | Strategic | CRITICAL | Threat model, pen testing |
| 7 | Observability | Strategic | HIGH | Metrics, logs, traces |
| 8 | Data Sovereignty and Governance | Data | CRITICAL | UK GDPR compliance audit |
| 9 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage |
| 10 | Single Source of Truth | Data | HIGH | Data ownership map |
| 11 | Privacy by Design | Data | CRITICAL | DPIA, data minimisation |
| 12 | Loose Coupling | Integration | HIGH | Deployment independence |
| 13 | Asynchronous Communication | Integration | MEDIUM | Async patterns for cross-dept |
| 14 | Reuse and Shared Platforms | Integration | HIGH | GOV.UK platform adoption |
| 15 | Performance and Efficiency | Quality | HIGH | Load testing |
| 16 | Availability and Reliability | Quality | CRITICAL | SLA monitoring |
| 17 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests |
| 18 | Infrastructure as Code | Development | HIGH | IaC coverage |
| 19 | Automated Testing | Development | HIGH | Test coverage |
| 20 | CI/CD | Development | HIGH | Pipeline exists |
| 21 | TCoP Compliance | Government | HIGH | TCoP assessment |
| 22 | Vendor Independence | Government | HIGH | Exit strategies documented |

### Cross-Project Principle Dependencies

```
001 Food Supply Chain ──────┐
                            │
002 School Meals ───────────┤ Shared Principles
                            │ (Principles 5, 10, 12, 13, 14)
003 Food Waste Analytics ───┤──────────────────────────────────→ 005 National Food
                            │                                     Strategy Dashboard
004 Agricultural Subsidy ───┘
         │
         └── DEFRA projects (001, 003, 004) share:
             - Principle 14: Geospatial platform reuse
             - Principle 10: Agricultural reference data
             - Principle 12: Cross-system APIs
```

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14-point service standard for government services | gov.uk/service-manual |
| Technology Code of Practice | Policy | GOV.UK | 12-point code for government technology decisions | gov.uk/guidance/the-technology-code-of-practice |
| NCSC Secure by Design | Guidance | NCSC | Security principles for government systems | ncsc.gov.uk |
| UK GDPR / DPA 2018 | Legislation | ICO | Data protection requirements | ico.org.uk |
| WCAG 2.2 | Standard | W3C | Web Content Accessibility Guidelines Level AA | w3.org/WAI |
| GovS 005 Digital | Functional Standard | Cabinet Office | Government functional standard for digital | gov.uk |

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-03-09
**ArcKit Version**: 4.1.1
**Project**: SDG 2 Zero Hunger -- Cross-Project Governance (Project 000)
**AI Model**: Claude Opus 4.6 (1M context)
