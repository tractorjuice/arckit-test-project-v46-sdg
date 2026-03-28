# UK Government Enterprise Architecture Principles — SDG 13: Climate Action

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 13: Climate Action — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 13 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 13 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 13: Climate Action programme. These principles apply to five UK Government digital services:

- **001** — Net Zero Tracking Dashboard (DESNZ)
- **002** — Climate Risk Assessment Platform (DEFRA)
- **003** — UK Emissions Trading Registry (DESNZ)
- **004** — Climate Adaptation Planning Tool (DEFRA)
- **005** — Green Finance Taxonomy Platform (HMT)

**Scope**: All technology projects, systems, and initiatives within the SDG 13 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the Climate Change Act 2008, the Net Zero Strategy (2021), the UK's Sixth Carbon Budget, the GDS Service Standard, the Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, the Environmental Information Regulations 2004, the Task Force on Climate-related Financial Disclosures (TCFD) recommendations, and the UK Green Taxonomy framework.

---

## I. Strategic Principles

### 1. Climate Data Integrity and Scientific Rigour

**Principle Statement**:
All systems MUST ensure the integrity, accuracy, and scientific rigour of climate data they process, store, and present. Data methodologies MUST be transparent, auditable, and aligned with internationally recognised standards (IPCC guidelines, GHG Protocol, UKCP18 projections).

**Rationale**:
Climate action decisions — carbon budgets, emissions trading, adaptation investments, green finance classifications — depend on trustworthy data. The Climate Change Committee (CCC) and international bodies (UNFCCC) require the UK to report emissions and progress using standardised, verifiable methodologies. Flawed data undermines policy credibility, misallocates public funds, and risks UK non-compliance with the Paris Agreement.

**Implications**:

- Use internationally recognised greenhouse gas accounting methodologies (GHG Protocol Scope 1/2/3, IPCC AR6 emission factors)
- Implement uncertainty quantification for all climate projections and emissions estimates
- Maintain full audit trails for data transformations from source to published figures
- Version-control all emission factor databases and climate projection datasets
- Ensure reproducibility — any published figure can be independently verified from source data
- Align with BEIS/DESNZ greenhouse gas reporting methodologies and NAEI (National Atmospheric Emissions Inventory) standards

**Validation Gates**:

- [ ] Data methodologies documented and aligned with IPCC/GHG Protocol standards
- [ ] Uncertainty bounds quantified and communicated for all projections
- [ ] Audit trail enables end-to-end traceability from source data to published figures
- [ ] Emission factor databases version-controlled with change history
- [ ] Independent verification of sample calculations completed
- [ ] Alignment with NAEI and DESNZ reporting standards confirmed

---

### 2. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Climate action services experience significant demand variation — ETS compliance deadlines create quarterly surges, CCC progress reports trigger public dashboard spikes, extreme weather events drive sudden interest in risk assessments, and Budget/Spending Review announcements spike green finance platform usage. Systems must handle both sustained growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (e.g., ETS surrender deadlines, CCC annual report publication, COP events)

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
The UK Emissions Trading Registry is a regulated financial system where downtime prevents obligated entities from meeting compliance deadlines. The Net Zero Tracking Dashboard informs Ministerial and CCC decision-making. Climate risk assessments feed into infrastructure investment decisions worth billions. These systems cannot afford extended outages — failures have regulatory, financial, and policy consequences.

**Implications**:

- Implement circuit breakers for all external dependencies (Met Office APIs, NAEI feeds, Companies House data)
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
The SDG 13 programme spans multiple departments (DESNZ, DEFRA, HMT) and must integrate with existing systems including the National Atmospheric Emissions Inventory, Met Office climate projections, HMRC tax data, FCA regulatory filings, Companies House registrations, and international bodies (UNFCCC, EU ETS successor registries). The Technology Code of Practice mandates open standards. Interoperability enables joined-up climate governance that reduces the reporting burden on businesses and local authorities.

**Implications**:

- Use open standards for data exchange (JSON-LD, CSV-W, GeoJSON for spatial data, NetCDF/CF conventions for climate data)
- Version all interfaces with a documented backward compatibility strategy
- Publish interface specifications in a discoverable catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (GDS API standards, INSPIRE Directive for geospatial data, CDDO Data Marketplace)

**Validation Gates**:

- [ ] Interface specifications published using open standard formats
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified in contracts
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle commercially sensitive emissions data (individual company carbon allowances), financially significant trading registry data (UK ETS allowances worth billions annually), critical national infrastructure risk assessments, and green finance classifications that affect investment flows. The UK ETS Registry is a target for fraud and market manipulation. Climate risk data for critical infrastructure is sensitive. A breach could enable carbon credit fraud, market manipulation, or compromise national resilience planning.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff, registry participants, and administrative access
- [ ] Service-to-service authentication using mutual authentication or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or environment variables)
- [ ] Network segmentation with minimal trust zones and deny-by-default policies
- [ ] Encryption at rest for all data stores containing emissions data, financial data, or risk assessments
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all authentication, authorisation, and transaction events
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- FCA cyber resilience requirements (for ETS Registry and Green Finance Platform)
- OWASP Top 10

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
We cannot operate what we cannot observe. The UK ETS Registry must demonstrate compliance with financial services operational standards. Climate dashboards must be available during high-profile moments (CCC annual progress report, COP events, Budget announcements). Operational blindness directly translates to undetected service degradation and missed compliance deadlines.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (emissions reported, allowances traded, risk assessments completed, taxonomy classifications processed)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 7 years (aligned with UK ETS compliance period and financial regulatory requirements)
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
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Environmental Information Regulations 2004, and departmental data governance policies.

**Rationale**:
Climate action systems process a wide range of data — from publicly available emissions inventories to commercially sensitive company-level emissions data and financially regulated trading records. The Environmental Information Regulations 2004 create proactive disclosure obligations for environmental data, while commercial confidentiality and market sensitivity require careful access controls. Correct classification and governance ensures both transparency and protection.

**Data Classification Tiers**:

1. **OFFICIAL — Published**: National emissions inventories, climate projections, published risk assessments — proactively disclosed under EIR 2004
2. **OFFICIAL**: Standard government business data with baseline controls
3. **OFFICIAL-SENSITIVE — Commercial**: Company-level emissions data, ETS account holdings, green taxonomy classification applications — enhanced controls required
4. **OFFICIAL-SENSITIVE — Market Sensitive**: UK ETS price-sensitive data, auction results pre-publication — strict access controls and insider trading prevention

**Data Residency**:

- All data MUST reside within UK sovereign data centres
- No transfer of commercially sensitive or personal data outside the UK without a lawful basis
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017 where applicable

**Data Retention**:

- UK ETS transaction records: minimum 7 years (aligned with EU ETS successor requirements and financial regulatory obligations)
- Climate projection datasets: retained indefinitely as scientific record (versioned)
- Company emissions data: retained for the compliance period plus 5 years
- Automatic deletion or anonymisation after the defined retention period expires

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] EIR 2004 proactive disclosure obligations assessed and implemented

---

### 8. Environmental Data Transparency

**Principle Statement**:
All environmental and climate data MUST be published openly by default, with restrictions applied only where there is a clear legal basis (commercial confidentiality, market sensitivity, or personal data).

**Rationale**:
The Environmental Information Regulations 2004 create a presumption of disclosure for environmental data. The UK's credibility in international climate negotiations depends on transparent reporting. Open data enables academic research, civil society scrutiny, and private sector innovation. The Aarhus Convention (ratified by the UK) requires public access to environmental information.

**Implications**:

- Publish national and sectoral emissions data as open data (machine-readable, API-accessible)
- Provide climate projection data in standard scientific formats (NetCDF with CF conventions)
- Aggregate company-level data to protect commercial confidentiality while enabling sectoral analysis
- Publish UK ETS market data (auction results, aggregate compliance data) after any market-sensitivity embargo expires
- Use the Open Government Licence for published data unless a different licence is required
- Implement FAIR data principles (Findable, Accessible, Interoperable, Reusable) for all published datasets

**Validation Gates**:

- [ ] Default position is open publication; restrictions justified and documented for each restricted dataset
- [ ] Published data is machine-readable and API-accessible
- [ ] Data published under Open Government Licence or appropriate alternative
- [ ] FAIR data principles applied to all published datasets
- [ ] EIR 2004 exemptions documented where data is restricted

---

### 9. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Carbon budget accounting, ETS compliance determinations, climate risk scores, and green taxonomy classifications are consequential decisions. The UK's Nationally Determined Contribution under the Paris Agreement depends on accurate emissions accounting. Poor data quality leads to incorrect carbon budget tracking, wrongful compliance penalties, misguided adaptation spending, or greenwashing in financial markets. Lineage enables accountability when figures are challenged by the CCC, NAO, or international reviewers.

**Quality Standards**:

- **Completeness**: No unexpected gaps in emissions time series; validation at point of entry
- **Consistency**: Cross-source reconciliation between NAEI, DESNZ statistics, and devolved administration data
- **Accuracy**: Emission factor validation, uncertainty quantification, anomaly detection for outlier submissions
- **Timeliness**: Freshness SLAs defined per data flow (e.g., UK ETS transaction data within 24 hours, annual emissions inventory within statutory deadlines)

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows (Met Office raw data through to published risk scores)
- Transformation logic version-controlled and auditable
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for methodology changes (what happens to published figures if an emission factor is revised?)

**Validation Gates**:

- [ ] Data quality rules defined and automated with monitoring
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts defined between producers and consumers
- [ ] Schema evolution strategy documented with backward compatibility approach

---

### 10. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
Multiple departments and agencies produce climate data — DESNZ publishes emissions statistics, DEFRA publishes adaptation data, Met Office publishes climate projections, the Environment Agency publishes flood risk data, and BEIS successor bodies publish energy data. Conflicting figures between government systems undermine public trust and create confusion for businesses attempting compliance. Authoritative sources must be unambiguous.

**Implications**:

- Designate the system of record for each data domain (e.g., NAEI for national emissions, Met Office for UKCP18 projections, UK ETS Registry for allowance holdings)
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Synchronisation strategy defined for all derived copies with documented lag tolerances
- Avoid bidirectional synchronisation — it creates split-brain scenarios and data conflicts
- Leverage existing authoritative sources (NAEI, Met Office, ONS energy statistics) rather than creating competing datasets

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data (e.g., SIC codes, geographic areas, emission factor tables)

---

## III. Integration Principles

### 11. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 13 programme spans five projects across three departments (DESNZ, DEFRA, HMT). Each team must be able to develop, deploy, and evolve their service independently. The Net Zero Dashboard must not fail because the ETS Registry is undergoing maintenance. Climate risk assessments must not be blocked by green finance taxonomy updates. Tight coupling creates coordination overhead, deployment risk, and organisational bottlenecks.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Shared libraries kept minimal; favour duplication over coupling where the cost of coordination exceeds the cost of duplication
- Avoid distributed transactions across system boundaries; use compensating actions or sagas instead
- Interface contracts owned by the producing team with consumer input on design

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees

---

### 12. Event-Driven Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability.

**Rationale**:
Many cross-departmental workflows in the climate programme are inherently asynchronous — an emissions report submission to the ETS Registry triggers compliance checking, the Net Zero Dashboard consumes published emissions data after processing, climate risk assessments incorporate Met Office projections when updated periodically, and green taxonomy classifications reference emissions data but do not need real-time access.

**When to Use Asynchronous Patterns**:

- Cross-departmental notifications (e.g., new emissions data published, adaptation plan submitted)
- Non-real-time business processes (e.g., batch emissions calculations, annual inventory compilation)
- Integration with external systems (Met Office, NAEI, Companies House, FCA filings)
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (e.g., ETS allowance balance check)
- Read-only queries where the response is needed to proceed (e.g., taxonomy classification lookup)
- Transactions requiring immediate consistency within a single service boundary (e.g., ETS allowance transfer)

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time cross-system flows
- [ ] Message durability and delivery guarantees defined (at-least-once, exactly-once)
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined
- [ ] Event replay capability available for recovery and debugging

---

## IV. Quality Attributes

### 13. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources.

**Rationale**:
The Net Zero Dashboard serves Ministers, CCC members, journalists, and the public — slow page loads undermine credibility. The ETS Registry must process allowance transfers and surrenders within seconds during compliance windows. Climate risk assessments involve computationally intensive geospatial analysis. Green finance taxonomy classification must be responsive enough for fund managers making investment decisions. Public sector cost efficiency requires responsible use of computational resources, and climate programmes should practise what they preach on resource efficiency.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to the user journey (e.g., < 2 seconds for dashboard pages, < 500ms for ETS balance queries)
- **Throughput**: Transactions per second at expected and peak load
- **Concurrency**: Simultaneous user capacity for normal and surge scenarios
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost and carbon footprint

**Implications**:

- Performance requirements defined before implementation, informed by user research
- Load testing performed before every production deployment
- Performance monitoring continuous with alerting on degradation
- Caching strategies defined for expensive computations (climate projections, risk scores)
- Consider the carbon footprint of compute — right-size infrastructure, use efficient algorithms

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly

---

### 14. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
The UK ETS Registry is a regulated financial system with statutory availability requirements — obligated entities must be able to surrender allowances by the compliance deadline. The Net Zero Dashboard must be available during high-profile moments (CCC annual progress report, Prime Minister's climate statements, COP events). Climate risk assessments feed into time-sensitive infrastructure investment decisions. Unavailability at critical moments has regulatory, reputational, and policy consequences.

**Availability Targets** (to be defined per service based on criticality):

- **UK ETS Registry**: 99.95% uptime (4.4 hours downtime per year maximum) — regulated financial system
- **Net Zero Dashboard**: 99.9% uptime (8.7 hours per year) — citizen and ministerial facing
- **Climate Risk Platform**: 99.5% uptime — professional users, batch processing acceptable
- **Adaptation Planning Tool**: 99.5% uptime — local authority professional users
- **Green Finance Platform**: 99.9% uptime — financial services integration

**High Availability Patterns**:

- Redundancy across multiple availability zones or data centres
- Automated health checks with self-healing recovery
- Active-active or active-passive configurations based on service criticality
- Regular disaster recovery testing (quarterly for ETS Registry, annually for others)

**Validation Gates**:

- [ ] Availability SLA defined per service based on criticality and regulatory requirements
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 15. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Climate policy evolves rapidly. Carbon budget targets are revised, ETS cap levels change annually, UKCP18 projections are updated, green taxonomy criteria evolve as the science develops, and adaptation priorities shift with new climate evidence. The EU's Carbon Border Adjustment Mechanism (CBAM) creates new integration requirements. Systems must accommodate policy and regulatory changes without requiring fundamental re-architecture.

**Implications**:

- Modular architecture with clear boundaries between policy/regulation logic and infrastructure concerns
- Externalise business rules where feasible (emission factor tables, ETS cap schedules, taxonomy criteria) so policy changes do not require code deployments
- Separation of concerns: business logic, data access, presentation, and integration layers
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to enable confident refactoring and policy updates

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries defined with clear responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices
- [ ] Policy/regulation changes achievable without full system redeployment

---

### 16. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. The Net Zero Dashboard is a public-facing service. Climate adaptation planning tools are used by local authority officers with varying digital skills and equipment. Environmental Information Regulations require information to be accessible. Climate action must be inclusive — communities most affected by climate change often have the least digital access.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Provide alternative formats for complex climate data visualisations (data tables, downloadable datasets)
- Publish an accessibility statement for each service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Complex visualisations have accessible alternatives (data tables, textual summaries)

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — all critical for regulated systems like the UK ETS Registry and services that feed Ministerial decision-making.

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

### 18. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to any shared environment.

**Rationale**:
These systems produce data that informs legally binding carbon budgets, regulated financial markets, infrastructure investment decisions, and international treaty compliance. Defects in emissions calculations, ETS compliance determinations, or risk score algorithms have material consequences. Automated testing provides a safety net that manual testing alone cannot match.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test component interactions and data flows (15–20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5–10% of tests)

**Required Test Types**:

- Functional tests (do emissions calculations produce correct results?)
- Regression tests for methodology changes (do existing scenarios still produce correct results when emission factors are updated?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (does it meet latency and throughput targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly in the pipeline

---

### 19. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent, manual releases. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to policy changes (e.g., revised emission factors, updated ETS cap, new taxonomy criteria) and security vulnerabilities.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, accessibility, security)
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

### 20. Sustainable Digital Architecture

**Principle Statement**:
Teams MUST consider the environmental impact of their technology choices, minimising the carbon footprint of digital services through efficient architecture, right-sized infrastructure, and responsible use of compute resources.

**Rationale**:
A programme dedicated to climate action must practise what it preaches. DEFRA's Greening Government ICT strategy and the GDS Technology Code of Practice encourage sustainable technology choices. Cloud infrastructure has a carbon footprint. Data centres consume energy. Inefficient algorithms waste compute. Teams should measure and minimise the environmental impact of their digital services, using cloud provider sustainability tools and choosing efficient architectures.

**Implications**:

- Measure the carbon footprint of cloud infrastructure using provider sustainability dashboards
- Right-size compute resources — avoid persistent over-provisioning
- Use serverless and event-driven patterns where appropriate to avoid idle resource consumption
- Optimise data storage — archive cold data to efficient storage tiers, avoid unnecessary data duplication
- Choose UK-based cloud regions powered by renewable energy where available
- Report the digital carbon footprint alongside service performance metrics

**Validation Gates**:

- [ ] Cloud carbon footprint measured and reported
- [ ] Infrastructure right-sizing reviewed quarterly
- [ ] Serverless or event-driven patterns used where appropriate
- [ ] Data archival policies implemented to reduce storage footprint
- [ ] UK cloud regions with renewable energy sourcing preferred

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on programme objectives if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 5) or Environmental Data Transparency (Principle 8)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] Climate data methodology approach defined and aligned with IPCC/GHG Protocol (Principle 1)
- [ ] Data classification and transparency approach defined (Principles 7, 8)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 5)
- [ ] Accessibility approach validated (Principle 16)
- [ ] Sustainable digital architecture assessment completed (Principle 20)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Climate data integrity verification completed (Principle 1)

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
| 1 | Climate Data Integrity and Scientific Rigour | Strategic | CRITICAL | Methodology audit, reproducibility testing, NAEI alignment |
| 2 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 3 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO verification |
| 4 | Interoperability and Open Standards | Strategic | HIGH | API specs, versioning, TCoP compliance |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 6 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 7 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, EIR compliance |
| 8 | Environmental Data Transparency | Data | CRITICAL | Open data publication, EIR 2004, FAIR principles |
| 9 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata, methodology versioning |
| 10 | Single Source of Truth | Data | HIGH | System of record documented per domain |
| 11 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 12 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 13 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring, targets met |
| 14 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing, regulatory compliance |
| 15 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, ADRs, externalised rules |
| 16 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, assistive tech testing |
| 17 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 18 | Automated Testing | Development | HIGH | Test coverage, pipeline integration |
| 19 | Continuous Integration and Deployment | Development | HIGH | Pipeline exists, security scanning |
| 20 | Sustainable Digital Architecture | Development | MEDIUM | Carbon footprint measured, right-sizing applied |

### Alignment to UK Government and Climate Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| Climate Change Act 2008 | 1 (Data Integrity), 7 (Data Governance), 8 (Transparency), 9 (Quality) |
| Net Zero Strategy 2021 | 1 (Data Integrity), 8 (Transparency), 10 (Single Source of Truth) |
| UK Sixth Carbon Budget | 1 (Data Integrity), 9 (Data Quality), 13 (Performance) |
| TCFD Recommendations | 1 (Data Integrity), 8 (Transparency), 9 (Data Quality) |
| UK Green Taxonomy | 1 (Data Integrity), 5 (Security), 8 (Transparency) |
| GDS Service Standard | 4 (Open Standards), 16 (Accessibility), 20 (Sustainability) |
| Technology Code of Practice | 4 (Open Standards), 5 (Security), 17 (IaC), 20 (Sustainability) |
| NCSC Secure by Design | 5 (Security), 17 (IaC), 18 (Testing), 19 (CI/CD) |
| UK GDPR / DPA 2018 | 7 (Data Sovereignty), 9 (Data Quality) |
| Environmental Information Regulations 2004 | 7 (Data Governance), 8 (Transparency) |
| HM Treasury Green Book | 2 (Scalability), 13 (Performance), 14 (Availability), 20 (Sustainability) |
| Public Sector Accessibility Regulations | 16 (Accessibility and Inclusion) |
| Paris Agreement / UNFCCC | 1 (Data Integrity), 8 (Transparency), 9 (Data Quality) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Climate Change Act 2008 | Legislation | legislation.gov.uk | Carbon budget framework, CCC mandate | N/A — external reference |
| Net Zero Strategy 2021 | Policy | GOV.UK | Net zero pathway, sector strategies | N/A — external reference |
| UK Sixth Carbon Budget | Statutory advice | CCC | Carbon budget levels, sector pathways | N/A — external reference |
| UKCP18 Climate Projections | Scientific data | Met Office | UK climate projection scenarios | N/A — external reference |
| TCFD Recommendations | Standard | FSB/TCFD | Climate financial disclosure framework | N/A — external reference |
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| Environmental Information Regulations 2004 | Legislation | legislation.gov.uk | Public access to environmental data | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| GHG Protocol | Standard | WBCSD/WRI | Greenhouse gas accounting standards | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 13: Climate Action — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
