# UK Government Enterprise Architecture Principles — SDG 16: Peace, Justice and Strong Institutions

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 16: Peace, Justice and Strong Institutions — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 16 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 16 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 16: Peace, Justice and Strong Institutions programme. These principles apply to five UK Government digital services:

- **001** — Digital Court Case Management (HMCTS)
- **002** — Legal Aid Digital Service (LAA)
- **003** — Open Government Data Portal (Cabinet Office)
- **004** — Anti-Fraud Analytics Platform (Cabinet Office)
- **005** — Citizen Participation Platform (DLUHC)

**Scope**: All technology projects, systems, and initiatives within the SDG 16 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, the HMCTS Reform Programme principles, the Open Government Partnership National Action Plan, the Government Counter Fraud Function standards, and the Nolan Principles of Public Life.

---

## I. Strategic Principles

### 1. Open Justice and Transparency

**Principle Statement**:
All systems MUST be designed to uphold the principle of open justice, ensuring that court proceedings, government decisions, and public data are accessible to citizens, media, and oversight bodies unless there is a lawful basis for restriction.

**Rationale**:
Open justice is a foundational constitutional principle — justice must not only be done, but must be seen to be done (R v Sussex Justices, ex parte McCarthy [1924]). The SDG 16 programme spans courts, legal aid, open government, fraud prevention, and citizen engagement — all domains where transparency is essential to public trust. The Open Government Partnership commits the UK to making government more accountable and responsive.

**Implications**:

- Default to publishing data openly unless there is a specific reason not to (security, privacy, sub judice)
- Design court systems to support public access to hearing lists, judgments, and case outcomes
- Implement clear, auditable redaction processes for sensitive information (victim identities, national security)
- Provide machine-readable open data feeds alongside human-readable interfaces
- Support media access to court information through dedicated interfaces
- Align with the Open Standards Principles and 5-star open data maturity model

**Validation Gates**:

- [ ] Default-open data policy documented with defined exceptions
- [ ] Redaction processes implemented and audited for accuracy
- [ ] Open data published to at least 3-star maturity (structured, open format, URI-identified)
- [ ] Public access to court listings and published judgments verified
- [ ] Compliance with Freedom of Information Act 2000 obligations verified

---

### 2. Rule of Law and Due Process

**Principle Statement**:
All systems MUST enforce procedural fairness, ensure complete audit trails for every decision affecting citizens' rights, and support the right to challenge decisions through appeal mechanisms.

**Rationale**:
The rule of law requires that decisions affecting citizens — court judgments, legal aid eligibility, fraud determinations — are made through fair processes, with complete records, and with the right to appeal. Automated or semi-automated decision-making must be explainable and challengeable. Article 6 of the European Convention on Human Rights (retained in UK law) guarantees the right to a fair hearing.

**Implications**:

- Every decision point must be recorded with the evidence considered, the rules applied, and the outcome
- Automated decision support must produce explainable outputs — no opaque algorithmic determinations on citizens' rights
- Appeal pathways must be designed into every system that makes or supports determinations
- Case history must be immutable and tamper-evident for evidential integrity
- Time-stamping must use an authoritative source with legal standing
- Retain decision records for periods compliant with court retention schedules and public records legislation

**Validation Gates**:

- [ ] Complete audit trail exists for every decision affecting a citizen's rights
- [ ] Automated decisions are explainable and can be manually reviewed
- [ ] Appeal mechanisms are designed and tested for every determination system
- [ ] Case records are immutable with tamper-evident logging
- [ ] Retention periods align with court retention schedules and Public Records Act requirements

---

### 3. Access to Justice

**Principle Statement**:
All citizen-facing systems MUST be designed to minimise barriers to accessing justice, legal aid, and government services, with particular attention to litigants in person, digitally excluded citizens, and those with protected characteristics.

**Rationale**:
Access to justice is under strain — legal aid cuts (LASPO Act 2012), court closures, and rising case backlogs mean that citizens increasingly navigate complex legal processes without professional representation. The HMCTS Reform Programme aims to make courts more accessible, but digital services risk creating new barriers if not designed inclusively. Approximately 40% of civil and family court users are litigants in person.

**Implications**:

- Design for litigants in person as the primary user, not as an edge case
- Provide guided journeys that explain legal processes in plain language (reading age appropriate for the audience)
- Support assisted digital access through court staff, Citizens Advice, and legal aid providers
- Ensure all services meet WCAG 2.2 Level AA as a legal requirement
- Provide multi-channel access (online, telephone, paper, face-to-face) where appropriate
- Offer language support for Welsh (Welsh Language Act 1993) and major community languages

**Validation Gates**:

- [ ] User research conducted with litigants in person, digitally excluded users, and users with disabilities
- [ ] Plain language review completed for all citizen-facing content
- [ ] Assisted digital pathway defined and tested with intermediary organisations
- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Welsh language obligations met for Wales-applicable services
- [ ] Multi-channel access tested end-to-end

---

### 4. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Justice system demand is inherently variable — court case volumes fluctuate with legislative changes, legal aid applications surge after policy announcements, fraud detection workloads spike during crises (COVID loan fraud exceeded £4.9 billion). The 2024 Crown Court backlog exceeded 67,000 cases. Systems must handle both sustained growth and acute demand spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (e.g., legislative changes triggering mass case re-assessments, consultation deadlines)

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates linear capacity growth with added resources
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Cost model accounts for variable capacity and peak scenarios

---

### 5. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
Court hearings cannot be adjourned because a case management system is down. Legal aid eligibility checks cannot be deferred when a citizen faces a court deadline. Fraud detection systems operating in real-time cannot afford gaps in coverage. Downtime in justice systems has direct consequences — cases delayed, rights denied, fraud undetected.

**Implications**:

- Implement circuit breakers for all external dependencies
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

### 6. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 16 programme spans HMCTS, the Legal Aid Agency, Cabinet Office, and DLUHC. Cross-government integration is essential — the Common Platform must share data with legal aid systems, fraud analytics must consume data from multiple departments, and open data must be publishable in standard formats. The Technology Code of Practice mandates open standards to avoid lock-in and enable interoperability.

**Implications**:

- Use open standards for data exchange and interface contracts
- Version all interfaces with a documented backward compatibility strategy
- Publish interface specifications in a discoverable API catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (GOV.UK API standards, Common Platform data standards)

**Validation Gates**:

- [ ] Interface specifications published using open standard formats (OpenAPI, AsyncAPI)
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified in contracts
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified

---

### 7. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle highly sensitive data — criminal case evidence, legal aid financial assessments, fraud intelligence, and citizen identity information. Court case data may include victim and witness details requiring the highest protection. A breach of fraud analytics data could compromise active investigations. A breach of legal aid data could expose citizens' financial vulnerabilities. NCSC guidance, UK GDPR, and the Government Security Classification Policy mandate proactive security.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and judicial access
- [ ] Service-to-service authentication using mutual authentication or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or environment variables)
- [ ] Network segmentation with minimal trust zones and deny-by-default policies
- [ ] Encryption at rest for all data stores containing personal, case, or investigative data
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- Government Security Classification Policy
- OWASP Top 10 (for application-layer controls)
- Judicial Office security standards for case data

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

### 8. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. For court case management systems, observability enables detection of processing delays that could breach statutory time limits. For fraud detection, operational metrics reveal gaps in coverage. For open data platforms, usage analytics demonstrate public value.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (cases progressed, legal aid applications processed, datasets published, fraud alerts raised, consultation responses received)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 7 years (aligned with court retention schedules and Public Records Act)
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

### 9. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, court data retention schedules, and departmental data governance policies.

**Rationale**:
These services process some of the most sensitive data in government — criminal case evidence, witness protection information, legal aid financial assessments, fraud intelligence, and citizen identity data. Mishandling court data undermines justice. Mishandling fraud intelligence compromises investigations. Data governance must be rigorous, documented, and auditable.

**Data Classification Tiers**:

1. **OFFICIAL**: Standard government business data — open data publications, anonymised statistics
2. **OFFICIAL-SENSITIVE**: Personal data, legal aid assessments, case management data, fraud referrals — enhanced controls required
3. **SECRET**: Fraud intelligence linked to organised crime, witness protection data, national security-related cases — highest controls

**Data Residency**:

- All personal and case data MUST reside within UK sovereign data centres
- No transfer of personal data outside the UK without a lawful basis and Data Protection Impact Assessment
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017 and the Counter Fraud Function data sharing powers

**Data Retention**:

- Retention periods defined per data category aligned with court retention schedules, Public Records Act 1958, and departmental retention policies
- Automatic deletion or anonymisation after the defined retention period expires
- Legal hold process documented for active litigation, appeals, and ongoing investigations
- Backup retention aligned with RPO and compliance requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all personal and case data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed where required

---

### 10. Privacy by Design

**Principle Statement**:
All systems MUST embed privacy protections into the architecture from the outset, minimising personal data collection, processing, and retention to what is strictly necessary.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. Citizens interacting with courts, legal aid, and government consultations should not have to surrender more personal information than necessary. Legal aid applicants share intimate financial details. Court users may be victims of crime. Fraud detection must balance investigative needs against privacy rights. The right to privacy must be balanced against the principle of open justice.

**Implications**:

- Collect only the minimum personal data required for the stated purpose (data minimisation)
- Implement purpose limitation — data collected for legal aid eligibility MUST NOT be shared with fraud detection without a lawful basis
- Pseudonymise or anonymise data wherever possible, especially for analytics and open data publishing
- Provide citizens with clear, accessible privacy notices explaining what data is collected and why
- Support data subject rights: access, rectification, erasure (where compatible with legal obligations), portability, and objection
- Implement privacy-preserving analytics for fraud detection that do not require unnecessary access to identifiable personal data

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service
- [ ] Data minimisation review conducted — no unnecessary data collected
- [ ] Privacy notices published in plain language
- [ ] Data subject rights mechanisms implemented and tested
- [ ] Pseudonymisation or anonymisation applied to analytics, reporting, and open data

---

### 11. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Decisions made by these systems — case progression, legal aid eligibility, fraud risk scores, open data accuracy — directly affect people's lives and public trust. Poor data quality in court records can lead to miscarriages of justice. Inaccurate legal aid means tests deny eligible citizens access to representation. Fraudulent patterns missed due to poor data quality cost the public purse billions. Lineage enables accountability when decisions are challenged.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; validation at point of entry
- **Consistency**: Cross-system data reconciliation with defined tolerances
- **Accuracy**: Validation rules and constraints enforced at source; anomaly detection for outliers
- **Timeliness**: Freshness SLAs defined and monitored per data flow

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows
- Transformation logic version-controlled and auditable
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for schema changes

**Validation Gates**:

- [ ] Data quality rules defined and automated with monitoring
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts defined between producers and consumers
- [ ] Schema evolution strategy documented with backward compatibility approach

---

### 12. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
The justice system depends on accurate, consistent records. A defendant's bail status must be consistent across the Common Platform, court listing system, and prison service. A citizen's legal aid eligibility must be consistent between the LAA system and the court that needs to know whether the defendant is represented. Multiple authoritative sources create inconsistency and risk to justice outcomes.

**Implications**:

- Identify the system of record for each data domain (e.g., Common Platform for case data, LAA for legal aid status)
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Synchronisation strategy defined for all derived copies with documented lag tolerances
- Avoid bidirectional synchronisation — it creates split-brain scenarios and data conflicts
- Leverage cross-government authoritative sources where they exist

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data

---

## III. Integration Principles

### 13. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 16 programme spans five projects across four organisations (HMCTS, LAA, Cabinet Office, DLUHC). Each team must be able to develop, deploy, and evolve their service independently. Tight coupling between court management and legal aid systems would create coordination overhead and deployment risk.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across system boundaries; use compensating actions or sagas instead
- Interface contracts owned by the producing team with consumer input on design

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees

---

### 14. Event-Driven Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability.

**Rationale**:
Many cross-system workflows in the justice domain are inherently asynchronous — a case progressing from magistrates' to Crown Court, a legal aid determination being communicated to the court, a fraud referral being sent for investigation, a consultation closing and responses being aggregated. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Cross-organisational notifications (e.g., case transfer, legal aid status change, fraud referral)
- Non-real-time business processes (e.g., batch fraud scoring, consultation response aggregation)
- Integration with unreliable or slow external systems
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (e.g., legal aid eligibility pre-check)
- Read-only queries where the response is needed to proceed (e.g., case status lookup)
- Transactions requiring immediate consistency within a single service boundary

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time cross-system flows
- [ ] Message durability and delivery guarantees defined (at-least-once, exactly-once)
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined
- [ ] Event replay capability available for recovery and debugging

---

## IV. Quality Attributes

### 15. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources.

**Rationale**:
Court hearings operate to strict schedules — a slow case management system wastes judicial time and delays justice. Legal aid eligibility checks must respond quickly to meet court deadlines. Fraud detection algorithms must process transactions in near real-time to prevent loss. Citizens participating in consultations should not face slow, frustrating interfaces. Public sector cost efficiency requires responsible use of computational resources.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to the user journey (e.g., < 2 seconds for page loads)
- **Throughput**: Transactions per second at expected and peak load
- **Concurrency**: Simultaneous user capacity for normal and surge scenarios
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly

---

### 16. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
Court systems must be available during sitting hours — a case management outage during a trial causes adjournments, wastes judicial time, and delays justice for defendants, victims, and witnesses. Legal aid systems must be available for solicitors preparing cases. Fraud detection systems must operate continuously to prevent loss.

**Availability Targets** (to be defined per service based on criticality):

- **Uptime SLA**: Minimum 99.9% for court-facing services during sitting hours (8.7 hours downtime per year maximum)
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime before service is restored
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss measured in time

**High Availability Patterns**:

- Redundancy across multiple availability zones or data centres
- Automated health checks with self-healing recovery
- Active-active or active-passive configurations based on service criticality
- Regular disaster recovery testing (quarterly for court and fraud systems)

**Validation Gates**:

- [ ] Availability SLA defined per service based on impact assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 17. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Justice system rules change with legislation (Sentencing Act 2020, Police, Crime, Sentencing and Courts Act 2022), legal aid regulations evolve with policy reviews (Means Test Review 2023), fraud methods evolve constantly, and open data standards advance. Systems must accommodate these changes without fundamental re-architecture.

**Implications**:

- Modular architecture with clear boundaries between legal/policy logic and infrastructure
- Externalise business rules where feasible so legislative changes do not require code deployments
- Separation of concerns: business logic, data access, presentation, and integration layers
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to enable confident refactoring and policy updates

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries defined with clear responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices
- [ ] Legislative or policy rule changes achievable without full system redeployment

---

### 18. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Court users include elderly litigants, people with learning disabilities, victims of crime in distress, and citizens with limited English proficiency. Legal aid applicants may be in crisis situations (eviction, domestic abuse) where cognitive load is already high. Inaccessible systems deny access to justice.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Provide alternative formats for content where required (Easy Read for learning disabilities)
- Publish an accessibility statement for each service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow connections

---

## V. Development Practices

### 19. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. For systems handling court evidence and fraud intelligence, auditability of infrastructure changes is a security requirement. Infrastructure as Code enables repeatability, auditability, and disaster recovery.

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

### 20. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to any shared environment.

**Rationale**:
These systems make decisions affecting citizens' access to justice, legal representation, and exposure to fraud. Defects in case progression logic, legal aid eligibility calculations, or fraud scoring algorithms have direct consequences for individuals and public finances. Automated testing provides a safety net that manual testing alone cannot match.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test component interactions and data flows (15–20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5–10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct outcomes?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (does it meet latency and throughput targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- Regression tests for legislative rule changes

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly in the pipeline

---

### 21. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to legislative changes and security vulnerabilities.

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

### 22. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice and GDS Service Manual require government teams to make source code open where possible. Reusing existing solutions — especially GOV.UK components, cross-government platforms, and established open source — reduces cost, accelerates delivery, and benefits from community security review. Exception: fraud detection algorithms where publication would enable adversarial gaming.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (e.g., GOV.UK Notify, GOV.UK Pay, Common Platform components)
- Use established open source components where they meet requirements and have active maintenance
- Publish source code openly unless it contains security-sensitive or fraud-sensitive logic
- Contribute improvements back to open source projects used by the programme
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] Government shared platforms evaluated before building bespoke alternatives
- [ ] Third-party dependency register maintained with licence compliance
- [ ] Source code published openly or justification documented for exceptions
- [ ] No proprietary lock-in to a single vendor's ecosystem without documented justification

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle (e.g., judicial independence requirements)
- Transitional state during migration from legacy systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on citizens and justice outcomes if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 7) or Privacy by Design (Principle 10)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] User research evidence supports design approach (Principle 3)
- [ ] Data classification and privacy approach defined (Principles 9, 10)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 7)
- [ ] Accessibility approach validated (Principle 18)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings

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
| 1 | Open Justice and Transparency | Strategic | CRITICAL | Open data policy, redaction audit, FOI compliance |
| 2 | Rule of Law and Due Process | Strategic | CRITICAL | Audit trails, explainable decisions, appeal mechanisms |
| 3 | Access to Justice | Strategic | CRITICAL | LiP user research, plain language, assisted digital |
| 4 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 5 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO verification |
| 6 | Interoperability and Open Standards | Strategic | HIGH | API specs, versioning, TCoP compliance |
| 7 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 8 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 9 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, retention policies |
| 10 | Privacy by Design | Data | CRITICAL | DPIA, data minimisation, subject rights |
| 11 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 12 | Single Source of Truth | Data | HIGH | System of record documented per domain |
| 13 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 14 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 15 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring, targets met |
| 16 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 17 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, ADRs |
| 18 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, assistive tech testing |
| 19 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 20 | Automated Testing | Development | HIGH | Test coverage, pipeline integration |
| 21 | Continuous Integration and Deployment | Development | HIGH | Pipeline exists, security scanning |
| 22 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Open Justice), 3 (Access to Justice), 6 (Open Standards), 18 (Accessibility), 22 (Open Source) |
| Technology Code of Practice | 6 (Open Standards), 7 (Security), 19 (IaC), 22 (Open Source and Reuse) |
| NCSC Secure by Design | 7 (Security by Design), 19 (IaC), 20 (Automated Testing), 21 (CI/CD) |
| UK GDPR / DPA 2018 | 9 (Data Sovereignty), 10 (Privacy by Design), 11 (Data Quality) |
| Public Sector Accessibility Regulations | 3 (Access to Justice), 18 (Accessibility and Inclusion) |
| HM Treasury Green Book | 4 (Scalability), 15 (Performance), 16 (Availability), 22 (Reuse) |
| HMCTS Reform Programme | 1 (Open Justice), 2 (Rule of Law), 3 (Access to Justice), 6 (Interoperability) |
| Open Government Partnership | 1 (Open Justice and Transparency), 9 (Data Sovereignty) |
| Government Counter Fraud Function | 7 (Security), 9 (Data Sovereignty), 11 (Data Quality) |
| Nolan Principles of Public Life | 1 (Transparency), 2 (Due Process), 3 (Access to Justice) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| HMCTS Reform Programme | Programme | HMCTS | Court modernisation principles | N/A — external reference |
| Open Government Partnership NAP | Policy | Cabinet Office | Transparency commitments | N/A — external reference |
| Government Counter Fraud Function | Standard | Cabinet Office | Counter fraud standards | N/A — external reference |
| LASPO Act 2012 | Legislation | legislation.gov.uk | Legal aid scope and eligibility | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 16: Peace, Justice and Strong Institutions — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
