# UK Government Enterprise Architecture Principles — SDG 10: Reduced Inequalities

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 10: Reduced Inequalities — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 10 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 10 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 10: Reduced Inequalities programme. These principles apply to four UK Government digital services:

- **001** — Accessibility Compliance Platform (GDS)
- **002** — Digital Inclusion Tracker (DSIT)
- **003** — Levelling Up Dashboard (DLUHC)
- **004** — Disability Confident Employer Portal (DWP)

**Scope**: All technology projects, systems, and initiatives within the SDG 10 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018 (PSBAR), Equality Act 2010, and the Levelling Up and Regeneration Act 2023.

---

## I. Strategic Principles

### 1. Inclusive Design First

**Principle Statement**:
All systems MUST be designed using the social model of disability and inclusive design principles, ensuring that services are usable by the widest possible range of people without adaptation or specialised design.

**Rationale**:
The SDG 10 programme exists to reduce inequalities. Systems that are not themselves inclusive contradict the programme's purpose. The social model of disability recognises that people are disabled by barriers in society, not by their impairment or difference. Our systems must not be a barrier. The Equality Act 2010 duty to make reasonable adjustments is a legal baseline, not an aspiration.

**Implications**:

- Design for the full spectrum of human diversity from the outset — do not retrofit accessibility
- Apply the GDS inclusive design principles: consider users with permanent, temporary, and situational disabilities
- Conduct user research with disabled people, older people, people with low digital literacy, and people whose first language is not English
- Provide content in plain English (reading age 9 or below for citizen-facing content)
- Support multiple interaction modalities: visual, auditory, motor, cognitive
- Ensure all interactive elements are operable without relying on a single sense or capability

**Validation Gates**:

- [ ] Inclusive design review conducted at Discovery and Alpha
- [ ] User research includes participants with a range of access needs
- [ ] Content assessed against plain language standards
- [ ] Design tested with assistive technologies across multiple modalities
- [ ] Service designed to work without JavaScript (progressive enhancement)

---

### 2. WCAG 2.2 Level AA as Minimum Standard

**Principle Statement**:
All citizen-facing and staff-facing digital services MUST meet WCAG 2.2 Level AA conformance as a legal and programme minimum. Services SHOULD aspire to Level AAA where feasible.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 (PSBAR) require public sector websites and mobile applications to meet WCAG 2.1 Level AA. This programme adopts WCAG 2.2 as the baseline standard, which includes additional success criteria addressing mobile accessibility, cognitive accessibility, and dragging movements. For a programme dedicated to reducing inequalities, exceeding the legal minimum is expected.

**Implications**:

- Automated accessibility testing (axe-core, WAVE, Lighthouse) integrated into CI/CD pipelines
- Manual accessibility testing by trained testers for every release
- Testing with assistive technologies: screen readers (JAWS, NVDA, VoiceOver), voice recognition (Dragon), screen magnification, switch access
- Accessibility statements published and maintained for every service
- Accessibility bugs treated with the same severity as functional bugs — critical accessibility failures block deployment
- Staff-facing tools held to the same WCAG 2.2 AA standard as citizen-facing services

**Validation Gates**:

- [ ] Automated WCAG 2.2 checks pass in CI/CD pipeline (zero critical violations)
- [ ] Manual accessibility audit completed before Beta assessment
- [ ] Tested with at least three assistive technologies
- [ ] Keyboard-only navigation verified for all user journeys
- [ ] Accessibility statement published and linked from service footer
- [ ] Accessibility defect triage process documented and enforced

---

### 3. Digital-by-Default with Assisted Digital

**Principle Statement**:
Services MUST be designed as digital-first but MUST provide assisted digital support for users who cannot use digital channels independently.

**Rationale**:
The Lloyds Bank Consumer Digital Index consistently shows that approximately 10 million adults in the UK lack foundational digital skills, and 1.7 million households have no internet access. Digital exclusion correlates strongly with socioeconomic disadvantage — the very populations this programme serves. A digital-only approach would exclude those who need these services most.

**Implications**:

- Design the digital journey first, optimised for self-service
- Provide telephone, face-to-face, and paper-based alternatives where the service is essential
- Assisted digital support available through trained intermediaries (e.g., library staff, voluntary sector, Jobcentre work coaches)
- Design for low-bandwidth and intermittent connectivity scenarios
- Support older browsers and devices without losing core functionality
- Track channel usage to understand digital uptake and identify exclusion patterns

**Validation Gates**:

- [ ] Assisted digital pathway designed and tested with intermediaries
- [ ] Service works on low-specification devices and slow connections (3G equivalent)
- [ ] Non-digital alternatives documented and operational
- [ ] Channel analytics in place to monitor digital uptake and exclusion signals
- [ ] User research conducted with digitally excluded populations

---

### 4. Multi-Channel Access Parity

**Principle Statement**:
All service channels (digital, telephone, face-to-face, paper) MUST provide equivalent outcomes. No user should receive a worse outcome because of the channel they use.

**Rationale**:
The Equality Act 2010 requires that services do not discriminate against people with protected characteristics. If a user cannot use the digital channel due to disability, age, literacy, or lack of connectivity, they must still be able to access the service with equivalent timeliness and quality. Channel parity is a fairness requirement, not just a service design preference.

**Implications**:

- All channels access the same backend systems and business logic
- Processing times equivalent across channels (no penalty for non-digital submission)
- Staff using telephony or face-to-face channels have access to the same information as digital self-service users
- Paper-based submissions digitised at point of receipt and enter the same workflow
- Multi-language support consistent across channels (Welsh language as statutory minimum in Wales)

**Validation Gates**:

- [ ] All channels tested against same outcome metrics
- [ ] Processing time parity verified across channels
- [ ] Staff-facing tools support same functionality as citizen-facing digital service
- [ ] Welsh language provision confirmed for Welsh-facing services
- [ ] No channel-specific business logic that could produce different outcomes

---

### 5. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Inequality monitoring and accessibility compliance services experience significant demand variation — Levelling Up fund announcements trigger dashboard traffic spikes, new PSBAR enforcement waves drive accessibility scanning surges, and Disability Confident certification deadlines create batch processing peaks. Systems must handle both sustained growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple availability zones
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for surge scenarios (e.g., major policy announcements, fund deadlines)

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates linear capacity growth with added resources
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Cost model accounts for variable capacity and peak scenarios

---

### 6. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
The Accessibility Compliance Platform monitors thousands of public sector websites for PSBAR compliance — an outage means accessibility violations go undetected. The Levelling Up Dashboard informs ministerial decisions on fund allocation — data staleness has policy consequences. The Disability Confident Portal supports employers making inclusion commitments — unavailability disrupts the certification pipeline. Resilience is essential for programme credibility.

**Implications**:

- Implement circuit breakers for all external dependencies
- Use timeouts on all network calls with sensible defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical paths
- [ ] Fault injection or chaos engineering testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined per service
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented and user-facing messaging defined

---

### 7. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 10 programme spans GDS, DSIT, DLUHC, and DWP — four departments that must share data about accessibility compliance, digital inclusion metrics, regional inequality indicators, and disability employment. The Technology Code of Practice mandates open standards to avoid lock-in and enable cross-government data sharing. Interoperability enables joined-up services that reduce inequality rather than siloing responses.

**Implications**:

- Use open standards for data exchange (JSON, CSV, GeoJSON for spatial data)
- Version all interfaces with documented backward compatibility strategy
- Publish interface specifications in a discoverable API catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (GOV.UK Design System, GDS API standards, Open Data Institute standards)

**Validation Gates**:

- [ ] Interface specifications published using open standard formats (OpenAPI 3.0)
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified in contracts
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified

---

### 8. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle personal data about disabled people, digitally excluded populations, regional deprivation indicators, and employer disability practices. A breach would cause severe harm to vulnerable citizens, expose sensitive equality data, and erode public trust. NCSC guidance, UK GDPR, and the Secure by Design framework mandate proactive security.

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

### 9. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. For services that monitor inequality and accessibility, operational blindness directly translates to undetected gaps in coverage. Instrumentation is a first-class architectural requirement.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (websites scanned, inclusion scores calculated, fund allocations tracked, certifications processed)
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

### 10. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Equality Act 2010 (regarding special category data), and departmental data governance policies.

**Rationale**:
Several of these services process special category data under the Equality Act 2010 and UK GDPR Article 9 — disability status, health conditions, and ethnicity data used for inequality monitoring. This data requires enhanced protections beyond standard personal data controls.

**Data Classification Tiers**:

1. **OFFICIAL**: Standard government business data — accessibility scan results, public dashboard metrics
2. **OFFICIAL-SENSITIVE**: Personal data, disability status, digital skills assessments, employer certification details — enhanced controls required
3. **SECRET**: Not expected in this programme; escalate if identified

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- No transfer of personal data outside the UK without lawful basis and Data Protection Impact Assessment
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017

**Data Retention**:

- Retention periods defined per data category aligned with departmental retention schedules
- Automatic deletion or anonymisation after defined retention period expires
- Legal hold process documented for litigation, investigation, or audit
- Backup retention aligned with RPO and compliance requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all personal data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed for services processing special category data

---

### 11. Privacy by Design

**Principle Statement**:
All systems MUST embed privacy protections into the architecture from the outset, minimising personal data collection, processing, and retention to what is strictly necessary.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. Citizens providing disability data, digital skills information, or regional deprivation data must trust that their information is handled with the utmost care. Special category data (disability, health, ethnicity) demands heightened privacy controls.

**Implications**:

- Collect only the minimum personal data required for the stated purpose (data minimisation)
- Implement purpose limitation — data collected for one purpose MUST NOT be repurposed without lawful basis
- Pseudonymise or anonymise data wherever possible, especially for analytics, dashboards, and reporting
- Provide citizens with clear, accessible privacy notices explaining what data is collected and why
- Support data subject rights: access, rectification, erasure, portability, and objection
- Implement privacy-preserving analytics that do not require access to identifiable personal data
- Aggregate inequality metrics to prevent identification of individuals in small geographic areas

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service
- [ ] Data minimisation review conducted — no unnecessary data collected
- [ ] Privacy notices published in plain language and accessible formats
- [ ] Data subject rights mechanisms implemented and tested
- [ ] Pseudonymisation or anonymisation applied to analytics and reporting data
- [ ] Statistical disclosure control applied to prevent re-identification in small area statistics

---

### 12. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Decisions informed by these systems — Levelling Up fund allocations, PSBAR enforcement priorities, digital inclusion interventions — directly affect communities and public spending. Poor data quality in the Index of Multiple Deprivation or Lloyds Digital Consumer Index feeds leads to misallocated resources. Lineage enables accountability when decisions are challenged.

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

### 13. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
Multiple departments sharing inequality data creates high risk of inconsistency. If IMD scores differ between DLUHC's dashboard and DSIT's inclusion tracker, policy decisions are undermined and public trust eroded. Authoritative sources must be unambiguous.

**Implications**:

- Identify the system of record for each data domain (e.g., ONS for census data, DLUHC for IMD, Lloyds for Digital Consumer Index)
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Synchronisation strategy defined for all derived copies with documented lag tolerances
- Avoid bidirectional synchronisation — it creates split-brain scenarios
- Leverage cross-government authoritative sources (ONS, OS data, GOV.UK Registers)

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data (geographic boundaries, organisation codes)

---

## III. Integration Principles

### 14. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 10 programme spans four projects across four departments. Each team must develop, deploy, and evolve their service independently. Tight coupling creates coordination overhead, deployment risk, and organisational bottlenecks.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across system boundaries; use compensating actions or sagas
- Interface contracts owned by the producing team with consumer input on design

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees

---

### 15. Event-Driven Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability.

**Rationale**:
Many cross-departmental workflows are inherently asynchronous — an accessibility scan result from GDS does not require an immediate response from DLUHC's dashboard. A new Disability Confident certification does not need to synchronously update the Levelling Up metrics. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Cross-departmental notifications (e.g., accessibility scan completion, new inclusion data release)
- Non-real-time business processes (e.g., batch compliance reporting, quarterly IMD updates)
- Integration with unreliable or slow external systems
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (e.g., live accessibility scan during website submission)
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

### 16. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources.

**Rationale**:
Citizens in inequality-affected communities often access services from low-specification devices over slow connections. Slow systems waste citizens' time and may cause them to abandon applications. The Accessibility Compliance Platform must scan thousands of websites efficiently without creating excessive load on scanned sites.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to user journey (< 2 seconds for page loads)
- **Throughput**: Transactions per second at expected and peak load
- **Concurrency**: Simultaneous user capacity for normal and surge scenarios
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly

---

### 17. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
The Levelling Up Dashboard informs ministerial decisions on billions of pounds of fund allocation. The Accessibility Compliance Platform underpins PSBAR enforcement. Unavailability means policy decisions lack data and compliance monitoring has gaps.

**Availability Targets** (to be defined per service based on criticality):

- **Uptime SLA**: Minimum 99.9% for citizen-facing services (8.7 hours downtime per year maximum)
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime before service is restored
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss measured in time

**Validation Gates**:

- [ ] Availability SLA defined per service based on impact assessment
- [ ] RTO and RPO requirements documented and achievable
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 18. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Equality legislation evolves. WCAG standards advance (2.2 today, 3.0 on the horizon). Levelling Up missions may be redefined by successive governments. Index of Multiple Deprivation methodology changes periodically. Systems must accommodate policy and standards changes without re-architecture.

**Implications**:

- Modular architecture with clear boundaries between policy logic and infrastructure
- Externalise business rules (e.g., WCAG success criteria mappings, IMD weightings) so changes do not require code deployments
- Separation of concerns: business logic, data access, presentation, integration
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to enable confident refactoring

**Validation Gates**:

- [ ] Architecture documentation exists and is current
- [ ] Module boundaries defined with clear responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records document key choices
- [ ] Business rule changes achievable without full system redeployment

---

### 19. Levelling Up Missions Alignment

**Principle Statement**:
All systems MUST support measurement and tracking against the Levelling Up missions defined in the Levelling Up White Paper and subsequent legislation, enabling transparent reporting on regional inequality reduction.

**Rationale**:
The Levelling Up and Regeneration Act 2023 established a legal framework for reducing geographic inequalities. The SDG 10 programme directly supports this agenda. All systems must produce data that can be disaggregated by region, local authority, and constituency to support Levelling Up reporting obligations.

**Implications**:

- All data models include geographic disaggregation (region, local authority, LSOA/MSOA)
- Metrics aligned to Levelling Up missions (education, health, crime, housing, broadband, transport, pride in place, well-being, pay, productivity, R&D, devolution)
- Data publishable as open data where not restricted by privacy
- Dashboard and reporting capabilities aligned to ministerial and parliamentary reporting cycles
- Interoperability with ONS geographies and boundary data

**Validation Gates**:

- [ ] Data models support geographic disaggregation to local authority level
- [ ] Metrics mapped to relevant Levelling Up missions
- [ ] Open data publication strategy defined
- [ ] Reporting aligned to parliamentary and ministerial cycles
- [ ] ONS geographic boundary data integrated and kept current

---

### 20. Social Model of Disability

**Principle Statement**:
All systems MUST adopt the social model of disability in their design, data models, and user interactions — focusing on removing barriers rather than categorising impairments.

**Rationale**:
The social model of disability, which underpins the Equality Act 2010, recognises that people are disabled by barriers in society rather than by their conditions. Systems that categorise users by impairment type risk reinforcing the medical model and creating stigmatising user experiences. The programme must model and measure barriers, not people.

**Implications**:

- Data models focus on barriers encountered, not impairment categories
- User interfaces do not require users to declare disability status unless strictly necessary and lawful
- Accessibility features are default, not opt-in — no "accessibility mode" toggle
- Disability Confident employer assessments focus on barrier removal evidence, not disability counts
- Analytics measure barrier prevalence, not disability prevalence
- Language throughout all services uses social model terminology

**Validation Gates**:

- [ ] Data models reviewed against social model principles
- [ ] User journeys do not require unnecessary disability disclosure
- [ ] Accessibility features enabled by default, not hidden behind toggles
- [ ] Language audit conducted for social model compliance
- [ ] Disability Confident assessment criteria focus on barrier removal

---

## V. Development Practices

### 21. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — critical for government services handling sensitive equality data.

**Validation Gates**:

- [ ] All infrastructure defined as code in version control
- [ ] Infrastructure code goes through peer review before deployment
- [ ] Environments reproducible from code
- [ ] No manual infrastructure changes in production

---

### 22. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment, including automated accessibility testing as a mandatory pipeline stage.

**Rationale**:
These systems inform decisions about inequality and enforce accessibility compliance. Defects in accessibility scanning logic, deprivation calculations, or certification workflows produce incorrect outcomes that harm the programme's mission. Accessibility testing must be first-class, not an afterthought.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions and data flows (15-20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct outcomes?)
- Accessibility tests (automated WCAG 2.2 checks in every pipeline run)
- Performance tests (does it meet latency and throughput targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- Visual regression tests (does the UI still meet design system standards?)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Accessibility tests mandatory in CI/CD pipeline
- [ ] Test coverage meets defined thresholds per service
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly

---

### 23. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk. Quality gates ensure only code meeting accessibility, security, and functional standards reaches production. This enables rapid response to WCAG updates, policy changes, and vulnerability disclosures.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Accessibility Check**: Automated WCAG 2.2 conformance verification
6. **Deployment**: Automated deployment to environments with progressive rollout

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes security scanning and accessibility checks
- [ ] Deployment is automated and repeatable
- [ ] Rollback capability tested and documented

---

### 24. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice requires government teams to make source code open where possible. Reusing GOV.UK components, axe-core for accessibility testing, and established open data standards reduces cost and accelerates delivery.

**Implications**:

- Evaluate government shared platforms before building bespoke (GOV.UK Notify, GOV.UK Pay, GOV.UK Design System)
- Use established open source accessibility tools (axe-core, pa11y, WAVE API)
- Publish source code openly unless it contains security-sensitive logic
- Contribute improvements back to open source projects
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] Government shared platforms evaluated before building bespoke alternatives
- [ ] Third-party dependency register maintained with licence compliance
- [ ] Source code published openly or justification documented
- [ ] No proprietary lock-in without documented justification

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy systems (time-bound)
- Pilot or proof-of-concept with a defined end date

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on citizens and equality outcomes
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 8) or Privacy by Design (Principle 11)
4. Equality Impact Assessment required for exceptions to Principles 1-4, 19-20
5. Document approved exception in project Architecture Decision Records
6. Quarterly review of all active exceptions

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by delivery team
- [ ] High-level approach aligns with principles
- [ ] User research evidence supports inclusive design approach (Principles 1-4)
- [ ] Data classification and privacy approach defined (Principles 10, 11)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested and approved where needed
- [ ] Security threat model completed (Principle 8)
- [ ] Accessibility approach validated with WCAG 2.2 audit (Principle 2)
- [ ] Equality Impact Assessment completed

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Accessibility audit passed with no critical WCAG 2.2 AA violations

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
| 1 | Inclusive Design First | Strategic | CRITICAL | User research, assistive tech testing |
| 2 | WCAG 2.2 Level AA Minimum | Strategic | CRITICAL | Automated + manual accessibility audit |
| 3 | Digital-by-Default with Assisted Digital | Strategic | HIGH | Assisted digital pathway tested |
| 4 | Multi-Channel Access Parity | Strategic | HIGH | Channel outcome equivalence verified |
| 5 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 6 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO |
| 7 | Interoperability and Open Standards | Strategic | HIGH | API specs, TCoP compliance |
| 8 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 9 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs |
| 10 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, DPIA |
| 11 | Privacy by Design | Data | CRITICAL | DPIA, data minimisation, subject rights |
| 12 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 13 | Single Source of Truth | Data | HIGH | System of record documented |
| 14 | Loose Coupling | Integration | HIGH | Deployment independence |
| 15 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 16 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring |
| 17 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 18 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, ADRs |
| 19 | Levelling Up Missions Alignment | Quality | HIGH | Geographic disaggregation, mission mapping |
| 20 | Social Model of Disability | Quality | CRITICAL | Barrier-focused data models, language audit |
| 21 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 22 | Automated Testing | Development | HIGH | Test coverage, accessibility in pipeline |
| 23 | Continuous Integration and Deployment | Development | HIGH | Pipeline with security + accessibility |
| 24 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Inclusive Design), 2 (WCAG 2.2), 3 (Assisted Digital), 7 (Open Standards), 24 (Open Source) |
| Technology Code of Practice | 7 (Open Standards), 8 (Security), 21 (IaC), 24 (Open Source and Reuse) |
| NCSC Secure by Design | 8 (Security by Design), 21 (IaC), 22 (Automated Testing), 23 (CI/CD) |
| UK GDPR / DPA 2018 | 10 (Data Sovereignty), 11 (Privacy by Design), 12 (Data Quality) |
| Equality Act 2010 | 1 (Inclusive Design), 4 (Channel Parity), 20 (Social Model of Disability) |
| PSBAR 2018 | 2 (WCAG 2.2 Level AA), 22 (Accessibility in pipeline) |
| Levelling Up White Paper | 19 (Levelling Up Missions Alignment), 13 (Single Source of Truth) |
| HM Treasury Green Book | 5 (Scalability), 16 (Performance), 17 (Availability), 24 (Reuse) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| PSBAR 2018 | Legislation | legislation.gov.uk | Public sector accessibility requirements | N/A — external reference |
| Equality Act 2010 | Legislation | legislation.gov.uk | Reasonable adjustments, protected characteristics | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| Levelling Up White Paper | Policy | GOV.UK | 12 Levelling Up missions | N/A — external reference |
| Lloyds Consumer Digital Index | Research | Lloyds Bank | Digital skills and inclusion data | N/A — external reference |
| UK Digital Strategy | Strategy | GOV.UK | Digital inclusion priorities | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 10: Reduced Inequalities — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
