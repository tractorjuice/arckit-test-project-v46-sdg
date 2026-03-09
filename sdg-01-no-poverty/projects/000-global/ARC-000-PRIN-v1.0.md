# UK Government Enterprise Architecture Principles — SDG 1: No Poverty

> **Template Origin**: Official | **ArcKit Version**: 4.1.1 | **Command**: `/arckit:principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 1: No Poverty — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-09 |
| **Last Modified** | 2026-03-09 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-09 |
| **Owner** | Chief Architect, SDG 1 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 1 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-09 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 1: No Poverty programme. These principles apply to five UK Government digital services:

- **001** — Universal Credit Modernisation (DWP)
- **002** — Social Housing Allocation Platform (DLUHC)
- **003** — Debt Advice Digital Service (MaPS)
- **004** — Food Bank Coordination System (Cross-gov)
- **005** — Fuel Poverty Intervention Tracker (DESNZ)

**Scope**: All technology projects, systems, and initiatives within the SDG 1 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, and the Public Sector Bodies Accessibility Regulations 2018.

---

## I. Strategic Principles

### 1. User-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of end users, with services that are simple, inclusive, and accessible to everyone who needs them.

**Rationale**:
The citizens served by these programmes — benefits claimants, social housing applicants, people in debt, food bank users, fuel-poor households — are among the most vulnerable in society. Systems that are difficult to use create barriers to essential support, increasing poverty rather than reducing it. The GDS Service Standard mandates user-centred design for all UK Government digital services.

**Implications**:

- Conduct user research with representative users, including those with low digital literacy, disabilities, and limited connectivity
- Design for assisted digital journeys — not all users can self-serve online
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement
- Support multiple channels (online, telephone, face-to-face) where appropriate
- Use plain language at a reading age appropriate for the service audience
- Provide clear status information so users understand where they are in a process

**Validation Gates**:

- [ ] User research conducted with representative sample including vulnerable users
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Assisted digital pathway defined and tested
- [ ] Content reviewed for plain language and readability
- [ ] User satisfaction metrics defined and baseline established
- [ ] Service assessed against GDS Service Standard points 1–3

---

### 2. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Poverty-related services experience significant demand variation — benefits processing surges at month-end, housing applications spike seasonally, food bank demand increases during cost-of-living crises. Systems must handle both sustained growth and acute spikes without degradation or manual intervention.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (e.g., policy changes triggering mass re-assessments)

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
These services support vulnerable citizens who depend on them for essential needs — income, housing, food, heating. Downtime has direct human impact: a benefits system outage means families cannot access money for food and rent. Resilience is not optional.

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

### 4. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 1 programme spans multiple departments (DWP, DLUHC, MaPS, DESNZ) and must integrate with existing government platforms. The Technology Code of Practice mandates the use of open standards to avoid lock-in and enable cross-government data sharing. Interoperability enables joined-up services that reduce the burden on citizens.

**Implications**:

- Use open standards for data exchange and interface contracts
- Version all interfaces with a documented backward compatibility strategy
- Publish interface specifications (API contracts, event schemas) in a discoverable catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (e.g., GOV.UK Registers, GDS API standards)

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
These systems handle highly sensitive personal data — financial circumstances, health conditions, housing status, family composition. A breach would cause severe harm to vulnerable citizens and erode public trust in government services. NCSC guidance, UK GDPR, and the Secure by Design framework mandate proactive security.

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

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10 (for application-layer controls)

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
We cannot operate what we cannot observe. For services supporting vulnerable citizens, operational blindness directly translates to undetected service degradation. Instrumentation is a first-class architectural requirement.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (applications processed, claims assessed, referrals made)
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

### 7. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and departmental data governance policies.

**Rationale**:
These services process large volumes of sensitive personal data about vulnerable citizens. Mishandling this data causes direct harm and violates legal obligations. Data governance must be rigorous, documented, and auditable.

**Data Classification Tiers**:

1. **OFFICIAL**: Standard government business data with baseline controls
2. **OFFICIAL-SENSITIVE**: Personal data, financial data, vulnerability indicators — enhanced controls required
3. **SECRET**: Not expected in this programme; escalate if identified

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- No transfer of personal data outside the UK without a lawful basis and Data Protection Impact Assessment
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017 where applicable

**Data Retention**:

- Retention periods defined per data category aligned with departmental retention schedules
- Automatic deletion or anonymisation after the defined retention period expires
- Legal hold process documented for litigation, investigation, or audit requirements
- Backup retention aligned with RPO and compliance requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all personal data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed where required

---

### 8. Privacy by Design

**Principle Statement**:
All systems MUST embed privacy protections into the architecture from the outset, minimising personal data collection, processing, and retention to what is strictly necessary.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. Citizens interacting with poverty-related services should not have to surrender more personal information than is necessary, and their data must be protected throughout its lifecycle.

**Implications**:

- Collect only the minimum personal data required for the stated purpose (data minimisation)
- Implement purpose limitation — data collected for one purpose MUST NOT be repurposed without a lawful basis
- Pseudonymise or anonymise data wherever possible, especially for analytics and reporting
- Provide citizens with clear, accessible privacy notices explaining what data is collected and why
- Support data subject rights: access, rectification, erasure, portability, and objection
- Implement privacy-preserving analytics that do not require access to identifiable personal data

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service
- [ ] Data minimisation review conducted — no unnecessary data collected
- [ ] Privacy notices published in plain language
- [ ] Data subject rights mechanisms implemented and tested
- [ ] Pseudonymisation or anonymisation applied to analytics and reporting data

---

### 9. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Decisions made by these systems — benefits entitlements, housing allocations, debt advice, fuel poverty assessments — directly affect people's lives. Poor data quality leads to wrong decisions. Lineage enables accountability when decisions are challenged.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; validation at point of entry
- **Consistency**: Cross-system data reconciliation with defined tolerances
- **Accuracy**: Validation rules and constraints enforced at source; anomaly detection for outliers
- **Timeliness**: Freshness SLAs defined and monitored per data flow

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows
- Transformation logic version-controlled and auditable
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for schema changes (what breaks if field X changes?)

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
Multiple departments sharing citizen data creates high risk of inconsistency. A citizen's address changing in one system but not another leads to wrong decisions, failed communications, and citizen distress. Authoritative sources must be unambiguous.

**Implications**:

- Identify the system of record for each data domain (e.g., citizen identity, address, benefits status)
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Synchronisation strategy defined for all derived copies with documented lag tolerances
- Avoid bidirectional synchronisation — it creates split-brain scenarios and data conflicts
- Leverage cross-government authoritative sources where they exist (e.g., registers, identity services)

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data (e.g., geographic areas, organisation codes)

---

## III. Integration Principles

### 11. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 1 programme spans five projects across four departments. Each team must be able to develop, deploy, and evolve their service independently. Tight coupling between systems creates coordination overhead, deployment risk, and organisational bottlenecks.

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
Many cross-departmental workflows in the poverty reduction programme are inherently asynchronous — a change of circumstances notification from DWP to DLUHC does not require an immediate synchronous response. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Cross-departmental notifications (e.g., change of circumstances, new referral)
- Non-real-time business processes (e.g., batch eligibility assessments, report generation)
- Integration with unreliable or slow external systems
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (e.g., eligibility check during application)
- Read-only queries where the response is needed to proceed
- Transactions requiring immediate consistency within a single service boundary

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
Citizens in poverty often access services from low-specification devices over slow connections. Slow systems waste citizens' time and may cause them to abandon applications for support they urgently need. Public sector cost efficiency requires responsible use of computational resources.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to the user journey (e.g., < 2 seconds for page loads)
- **Throughput**: Transactions per second at expected and peak load
- **Concurrency**: Simultaneous user capacity for normal and surge scenarios
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost

**Implications**:

- Performance requirements defined before implementation, informed by user research
- Load testing performed before every production deployment
- Performance monitoring continuous with alerting on degradation
- Optimise for the slowest expected client (low-end mobile on 3G connection)
- Caching strategies defined for expensive or frequently-accessed data

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
Benefits systems, housing allocation, and fuel poverty interventions are critical services. Unavailability means vulnerable citizens cannot access support. Availability targets must reflect the service criticality and the impact of downtime on citizens.

**Availability Targets** (to be defined per service based on criticality):

- **Uptime SLA**: Minimum 99.9% for citizen-facing services (8.7 hours downtime per year maximum)
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime before service is restored
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss measured in time

**High Availability Patterns**:

- Redundancy across multiple availability zones or data centres
- Automated health checks with self-healing recovery
- Active-active or active-passive configurations based on service criticality
- Regular disaster recovery testing (at least annually, quarterly for critical services)

**Validation Gates**:

- [ ] Availability SLA defined per service based on citizen impact assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 15. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Government policy changes frequently. Benefits rules, housing allocation criteria, fuel poverty definitions, and debt advice regulations all evolve over time. Systems must accommodate policy changes without requiring fundamental re-architecture. Staff turnover in government also means systems must be understandable by new team members.

**Implications**:

- Modular architecture with clear boundaries between policy logic and infrastructure concerns
- Externalise business rules where feasible so policy changes do not require code deployments
- Separation of concerns: business logic, data access, presentation, and integration layers
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to enable confident refactoring and policy updates

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries defined with clear responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices
- [ ] Business rule changes achievable without full system redeployment

---

### 16. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Beyond compliance, the users of these services disproportionately include people with disabilities, older citizens, people with low digital literacy, and people using older or low-specification devices. Inaccessible systems exclude the very people they are meant to serve.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Provide alternative formats for content where required
- Publish an accessibility statement for each service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow connections

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — all critical for government services handling sensitive personal data.

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
These systems make decisions affecting vulnerable people's lives. Defects in benefits calculations, housing allocations, or eligibility assessments cause real harm. Automated testing provides a safety net that manual testing alone cannot match in coverage or consistency.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test component interactions and data flows (15–20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5–10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct outcomes?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (does it meet latency and throughput targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- Regression tests for policy rule changes (do existing scenarios still produce correct results?)

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
Frequent, small, automated deployments reduce risk compared to large, infrequent, manual releases. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to policy changes and security vulnerabilities.

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

### 20. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice and GDS Service Manual require government teams to make source code open where possible. Reusing existing solutions — especially GOV.UK components, cross-government platforms, and established open source — reduces cost, accelerates delivery, and benefits from community security review.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (e.g., GOV.UK Notify, GOV.UK Pay, GOV.UK Verify successor)
- Use established open source components where they meet requirements and have active maintenance
- Publish source code openly unless it contains security-sensitive logic or configuration
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
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on citizens if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 5) or Privacy by Design (Principle 8)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] User research evidence supports design approach (Principle 1)
- [ ] Data classification and privacy approach defined (Principles 7, 8)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 5)
- [ ] Accessibility approach validated (Principle 16)

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
| 1 | User-Centred Design | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 2 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 3 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO verification |
| 4 | Interoperability and Open Standards | Strategic | HIGH | API specs, versioning, TCoP compliance |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 6 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 7 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, retention policies |
| 8 | Privacy by Design | Data | CRITICAL | DPIA, data minimisation, subject rights |
| 9 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 10 | Single Source of Truth | Data | HIGH | System of record documented per domain |
| 11 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 12 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 13 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring, targets met |
| 14 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 15 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, ADRs |
| 16 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, assistive tech testing |
| 17 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 18 | Automated Testing | Development | HIGH | Test coverage, pipeline integration |
| 19 | Continuous Integration and Deployment | Development | HIGH | Pipeline exists, security scanning |
| 20 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (User-Centred Design), 4 (Open Standards), 16 (Accessibility), 20 (Open Source) |
| Technology Code of Practice | 4 (Open Standards), 5 (Security), 17 (IaC), 20 (Open Source and Reuse) |
| NCSC Secure by Design | 5 (Security by Design), 17 (IaC), 18 (Automated Testing), 19 (CI/CD) |
| UK GDPR / DPA 2018 | 7 (Data Sovereignty), 8 (Privacy by Design), 9 (Data Quality) |
| Public Sector Accessibility Regulations | 1 (User-Centred Design), 16 (Accessibility and Inclusion) |
| HM Treasury Green Book | 2 (Scalability), 13 (Performance), 14 (Availability), 20 (Reuse) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-03-09
**ArcKit Version**: 4.1.1
**Project**: SDG 1: No Poverty — Cross-Project Governance (Project 000)
**AI Model**: Claude Opus 4.6 (1M context)
