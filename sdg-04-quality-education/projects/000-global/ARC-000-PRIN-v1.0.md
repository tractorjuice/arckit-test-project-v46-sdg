# UK Government Enterprise Architecture Principles — SDG 4: Quality Education

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 4: Quality Education — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 4 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 4 project teams, Enterprise Architecture Review Board, DfE Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 4: Quality Education programme. These principles apply to five UK Government digital services:

- **001** — National Digital Learning Platform (DfE)
- **002** — School Performance Analytics (Ofsted)
- **003** — SEND Case Management System (DfE)
- **004** — Apprenticeship Matching Service (DfE)
- **005** — Teacher Recruitment Portal (DfE)

**Scope**: All technology projects, systems, and initiatives within the SDG 4 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, the Children Act 2004, the Age Appropriate Design Code (ICO), the Public Sector Bodies Accessibility Regulations 2018, and DfE's Digital Strategy 2025-2030.

---

## I. Strategic Principles

### 1. Learner-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of learners, educators, parents, and carers, with services that are simple, inclusive, and accessible to everyone who needs them — regardless of age, ability, or digital confidence.

**Rationale**:
The users of education services span an extraordinarily wide range — from 4-year-old reception pupils to adult apprentices, from digitally confident teachers to parents with limited English, from SEND coordinators to school governors. The GDS Service Standard mandates user-centred design, and the education context demands particular attention to age-appropriate design, safeguarding, and the needs of children and young people with additional needs.

**Implications**:

- Conduct user research with representative users including children, young people, parents with low digital literacy, users with SEND, and users for whom English is an additional language
- Design age-appropriate interfaces that comply with the ICO Age Appropriate Design Code for services likely to be accessed by under-18s
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement under the Public Sector Bodies Accessibility Regulations 2018
- Support assisted digital journeys — not all parents, carers, or education professionals can self-serve online
- Use plain language appropriate to the audience; parent-facing content should be readable at age 9-11 reading level
- Provide clear status information so users understand where they are in a process (e.g., application progress, assessment outcomes)

**Validation Gates**:

- [ ] User research conducted with representative sample including children, parents, and users with SEND
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Age Appropriate Design Code compliance assessed for services accessed by under-18s
- [ ] Assisted digital pathway defined and tested
- [ ] Content reviewed for plain language and readability appropriate to each audience
- [ ] Service assessed against GDS Service Standard points 1-3

---

### 2. Safeguarding by Design (NON-NEGOTIABLE)

**Principle Statement**:
All systems handling data about children, young people, or vulnerable adults MUST embed safeguarding protections into the architecture from the outset. Safeguarding is NOT a feature to be added later — it is a foundational requirement that takes precedence over all other considerations.

**Rationale**:
The Children Act 2004, Working Together to Safeguard Children 2023, and Keeping Children Safe in Education place statutory duties on education providers and government agencies to safeguard children. Systems that process children's data, education records, or SEND information must protect children from harm, prevent unauthorised disclosure of sensitive information, and support multi-agency safeguarding workflows.

**Implications**:

- Implement strict access controls that prevent unauthorised access to children's personal data
- Support safeguarding referral workflows across agency boundaries (schools, local authorities, social care, police)
- Design data sharing to comply with the Information Sharing Advice for Practitioners guidance
- Ensure that data about looked-after children, children in need, and children subject to protection plans has enhanced access controls
- Implement audit trails that capture all access to safeguarding-sensitive data
- Design systems to support the "child's voice" — children's views and wishes must be capturable and auditable
- Never expose children's location data, contact details, or images without appropriate safeguarding review

**Validation Gates**:

- [ ] Safeguarding impact assessment completed for each service
- [ ] Access controls verified for all children's data categories
- [ ] Multi-agency data sharing complies with statutory guidance
- [ ] Audit trail captures all access to safeguarding-sensitive records
- [ ] Looked-after children data has enhanced protection controls
- [ ] Service assessed against Keeping Children Safe in Education requirements

---

### 3. Children's Data Privacy (NON-NEGOTIABLE)

**Principle Statement**:
All systems processing data about children and young people MUST comply with the ICO Age Appropriate Design Code, UK GDPR, and the Data Protection Act 2018, with privacy protections that go beyond those applied to adult data.

**Rationale**:
UK GDPR Recital 38 states that children merit specific protection with regard to their personal data. The ICO's Age Appropriate Design Code sets 15 standards that apply to information society services likely to be accessed by children. Education systems inherently process large volumes of children's data — attainment, attendance, behaviour, SEND status, free school meal eligibility, ethnicity, and family circumstances. This data is highly sensitive and its misuse can cause lasting harm.

**Implications**:

- Apply data minimisation rigorously — collect only the minimum personal data required for the educational purpose
- Default all privacy settings to the highest level of protection (privacy by default)
- Do not use children's data for profiling, targeted advertising, or purposes beyond the stated educational purpose
- Provide age-appropriate transparency — explain data use in language children can understand
- Support parental rights to access, rectify, and request deletion of their child's data
- Implement data retention policies that automatically delete children's data when it is no longer needed for the educational purpose
- Conduct Data Protection Impact Assessments (DPIAs) for all processing of children's data

**Validation Gates**:

- [ ] ICO Age Appropriate Design Code compliance assessment completed
- [ ] DPIA completed for all processing of children's personal data
- [ ] Privacy settings default to highest protection level
- [ ] No profiling or non-educational use of children's data
- [ ] Age-appropriate privacy notices published
- [ ] Parental access and deletion rights mechanisms implemented and tested
- [ ] Data retention policies configured with automated deletion

---

### 4. Digital Inclusion and the Pupil Premium Gap

**Principle Statement**:
All systems MUST be designed to be usable by learners, parents, and educators regardless of their socioeconomic circumstances, digital access, or connectivity. Services MUST NOT widen the digital divide.

**Rationale**:
SDG 4 specifically targets inclusive and equitable quality education. The COVID-19 pandemic exposed the severe impact of the digital divide on disadvantaged pupils — those eligible for free school meals, looked-after children, and children in rural areas with poor connectivity. Education technology must narrow, not widen, this gap.

**Implications**:

- Design for low-bandwidth environments — services must function on slow connections (equivalent to 2G/3G)
- Support offline-capable functionality where feasible for core learning activities
- Ensure services work on low-specification devices (Chromebooks, older tablets, shared family devices)
- Provide non-digital alternatives for essential interactions (telephone, postal, face-to-face)
- Monitor usage analytics disaggregated by disadvantage indicators to detect and address digital exclusion
- Design for shared device scenarios — multiple family members may share a single device

**Validation Gates**:

- [ ] Service functional on low-bandwidth connections (tested at 3G speeds)
- [ ] Service usable on low-specification devices (tested on budget Chromebooks/tablets)
- [ ] Offline capability assessed and implemented where appropriate
- [ ] Non-digital alternatives documented and available
- [ ] Usage analytics disaggregated by pupil premium/FSM eligibility
- [ ] Shared device scenario tested (multiple accounts, privacy between users)

---

### 5. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on the academic calendar and predictable usage patterns.

**Rationale**:
Education services have highly predictable demand patterns tied to the academic calendar — September intake, January census, GCSE/A-level results days, UCAS deadlines, Ofsted inspection cycles, and teacher recruitment windows. Systems must handle both sustained term-time load and acute spikes (e.g., A-level results day, when millions of students access results simultaneously).

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for known peak events (results day: 10x normal traffic; census day: 5x normal)
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics with pre-scaling for known events
- Capacity plan for growth in user base as digital adoption increases

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing performed at expected peak capacity (results day scenario)
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Pre-scaling strategy defined for known calendar events
- [ ] Cost model accounts for variable capacity across the academic year

---

### 6. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
Education systems hold highly sensitive data about children, families, and educators — attainment data, SEND assessments, safeguarding records, DBS check outcomes, and financial information (free school meal eligibility, bursaries). The education sector is increasingly targeted by cyber attackers, as demonstrated by ransomware attacks on schools and Multi-Academy Trusts. NCSC guidance, UK GDPR, and the Secure by Design framework mandate proactive security.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrative access
- [ ] DfE Sign-in integration for federated identity across education services
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
- DfE Standards for Keeping Children Safe in Education (Annex C — online safety)
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
- [ ] DBS data handling compliant with Disclosure and Barring Service code of practice

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. Education services have critical time-sensitivity — an outage on results day or during the school census has immediate and widespread impact. Operational blindness directly translates to undetected service degradation affecting millions of learners, parents, and educators.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (applications submitted, assessments completed, matches made, reports generated)
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
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and DfE data governance policies, with enhanced protections for children's data.

**Rationale**:
Education services process vast volumes of sensitive personal data about children and young people — attainment, attendance, behaviour, SEND status, ethnicity, free school meal eligibility, exclusions, and safeguarding records. Mishandling this data causes direct harm to children and families and violates legal obligations.

**Data Classification Tiers**:

1. **OFFICIAL**: Standard education business data (school addresses, published performance data, curriculum content)
2. **OFFICIAL-SENSITIVE**: Personal data about children, parents, and staff — attainment records, attendance, teacher employment records, DBS outcomes
3. **OFFICIAL-SENSITIVE (Safeguarding)**: Safeguarding referrals, child protection plans, SEND assessments — highest controls required within OFFICIAL tier

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- No transfer of children's data outside the UK without explicit lawful basis and DPIA
- Cross-departmental data sharing MUST be governed by data sharing agreements (e.g., DfE-Ofsted data sharing agreement for school performance data)

**Data Retention**:

- Retention periods defined per data category aligned with DfE Information Management Framework
- Pupil-level data retained for the statutory period then automatically deleted or anonymised
- Legal hold process documented for Ofsted inspections, tribunal proceedings, and FOI requests
- Backup retention aligned with RPO and compliance requirements

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all personal data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed for all processing of children's data

---

### 9. Interoperability with the Education Data Ecosystem

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards, and MUST integrate with the existing education data ecosystem including Get Information About Schools (GIAS), DfE Sign-in, the National Pupil Database, and school Management Information Systems (MIS).

**Rationale**:
The UK education data landscape is complex — schools use diverse MIS systems (SIMS, Bromcom, Arbor, ScholarPack), DfE maintains authoritative registers (GIAS, Edubase successor), and data flows between schools, local authorities, DfE, Ofsted, and ESFA. Interoperability is essential to avoid duplicate data entry, maintain data quality, and deliver joined-up services. The Technology Code of Practice mandates open standards.

**Implications**:

- Integrate with DfE Sign-in for federated identity across education services
- Use Get Information About Schools (GIAS) as the authoritative source for school/establishment data
- Support Common Transfer File (CTF) and Common Basic Data Set (CBDS) standards for pupil data exchange
- Publish API specifications compliant with GDS API standards
- Integrate with school MIS systems via published APIs (not proprietary connectors)
- Support SIF (Schools Interoperability Framework) UK profile where applicable
- Version all interfaces with a documented backward compatibility strategy

**Validation Gates**:

- [ ] DfE Sign-in integration implemented and tested
- [ ] GIAS used as authoritative source for establishment data
- [ ] API specifications published using OpenAPI 3.0 format
- [ ] MIS integration tested with at least three major MIS providers (SIMS, Bromcom, Arbor)
- [ ] Common Transfer File/CBDS support verified
- [ ] Versioning strategy defined with deprecation policy

---

### 10. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Decisions made by education systems — school performance judgements, SEND provision allocation, apprenticeship funding, teacher suitability — directly affect children's life chances and educators' careers. Poor data quality leads to wrong decisions. Lineage enables accountability when decisions are challenged through tribunals, judicial review, or Ofsted inspection.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; validation at point of entry
- **Consistency**: Cross-system data reconciliation (e.g., pupil numbers in MIS must match school census)
- **Accuracy**: Validation rules and constraints enforced at source; anomaly detection for outliers
- **Timeliness**: Freshness SLAs defined and monitored (e.g., school performance data updated within 24 hours of publication)

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

### 11. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled and synchronised with defined freshness guarantees.

**Rationale**:
The education sector suffers from data fragmentation — schools enter data into MIS systems, which is collected via school census, which feeds the National Pupil Database, which Ofsted and ESFA also consume. Inconsistencies between these sources cause confusion, duplicate effort, and incorrect decisions. Authoritative sources must be unambiguous.

**Implications**:

- GIAS is the system of record for establishment data (school name, address, type, status, URN, UKPRN)
- The National Pupil Database is the system of record for pupil-level attainment and characteristics
- DfE Sign-in is the authoritative identity provider for education professionals
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Avoid bidirectional synchronisation between systems

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
The SDG 4 programme spans five projects across two organisations (DfE and Ofsted). Each team must be able to develop, deploy, and evolve their service independently. Tight coupling creates coordination overhead, deployment risk, and organisational bottlenecks.

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

### 13. Event-Driven Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability.

**Rationale**:
Many cross-system workflows in the education programme are inherently asynchronous — a school census submission triggering data validation, an Ofsted inspection triggering data requests, a SEND assessment decision triggering provision notifications. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Cross-departmental notifications (e.g., Ofsted inspection notification to DfE)
- Non-real-time business processes (e.g., batch census processing, report generation)
- Integration with school MIS systems that batch-submit data
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time user interactions requiring immediate feedback (e.g., eligibility check during application)
- Read-only queries where the response is needed to proceed (e.g., GIAS establishment lookup)
- Transactions requiring immediate consistency within a single service boundary

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time cross-system flows
- [ ] Message durability and delivery guarantees defined (at-least-once, exactly-once)
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined
- [ ] Event replay capability available for recovery and debugging

---

## IV. Quality Attributes

### 14. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Education services serve users with SEND (approximately 1.6 million pupils in England), parents with disabilities, educators with varying digital confidence, and learners using assistive technologies. Inaccessible systems directly contradict the inclusive education mission of SDG 4.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access, eye gaze)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Provide alternative formats for educational content (audio, large print, Easy Read)
- Publish an accessibility statement for each service
- Test with SEND users and learners who use assistive technology in classroom settings

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow connections
- [ ] Tested with users who have SEND

---

### 15. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources.

**Rationale**:
Education users access services across a wide range of devices and connectivity — from school broadband to rural home connections, from managed desktop PCs to shared family smartphones. Slow services waste teachers' limited planning time, frustrate parents attempting to engage with their child's education, and may cause system-critical processes (census submissions, examination entries) to fail.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency < 2 seconds for page loads; < 500ms for API responses
- **Throughput**: Sufficient for known peak events (results day, census day)
- **Concurrency**: Scaled for full simultaneous access during peak periods
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity (including results day scenarios)
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed termly

---

### 16. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
Education services have time-critical deadlines — census submission windows, examination entry deadlines, Ofsted inspection data requests. Downtime during these periods has severe consequences: missed statutory deadlines, delayed results, and disruption to school operations affecting millions of learners.

**Implications**:

- Implement circuit breakers for all external dependencies (MIS systems, GIAS, DfE Sign-in)
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

### 17. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss, aligned to the academic calendar.

**Rationale**:
Education services are critical infrastructure during term time. Availability targets must reflect the academic calendar — higher availability requirements during census periods, examination seasons, and results days; lower requirements may be acceptable during school holidays for maintenance windows.

**Availability Targets**:

- **Citizen-facing services**: Minimum 99.9% uptime (8.7 hours downtime per year maximum)
- **Results day / census day**: 99.99% availability target with pre-scaling
- **Maintenance windows**: Preferably during school holidays or outside 07:00-22:00 term-time hours
- **RTO**: Maximum 1 hour for critical services; 4 hours for non-critical
- **RPO**: Maximum 15 minutes for transactional data; 1 hour for analytical data

**Validation Gates**:

- [ ] Availability SLA defined per service based on educational impact assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

## V. Development Practices

### 18. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — all critical for government services handling children's sensitive personal data.

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
These systems make decisions affecting children's educational opportunities, school judgements, SEND provision, and teacher careers. Defects in assessment calculations, performance metrics, or eligibility determinations cause real harm. Automated testing provides a safety net that manual testing alone cannot match.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions and data flows (15-20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (do calculations produce correct outcomes?)
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

### 20. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice and GDS Service Manual require government teams to make source code open where possible. Reusing existing solutions — especially GOV.UK components, GOV.UK Notify, GOV.UK Pay, and DfE design patterns — reduces cost, accelerates delivery, and benefits from community review.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (GOV.UK Notify for communications, GOV.UK Pay for payments, DfE Sign-in for identity)
- Use established open source components where they meet requirements and have active maintenance
- Publish source code openly unless it contains security-sensitive logic
- Maintain a register of third-party dependencies with licence compliance tracking
- Reuse DfE-specific design patterns and components where they exist

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
- School MIS vendor limitations requiring interim workarounds

**Exception Request Requirements**:

- [ ] Written justification with business and technical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including impact on children and learners if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Safeguarding by Design (Principle 2), Children's Data Privacy (Principle 3), or Security by Design (Principle 6)
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
- [ ] Data classification and privacy approach defined (Principles 3, 8)
- [ ] Safeguarding approach defined (Principle 2)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 6)
- [ ] Accessibility approach validated (Principle 14)
- [ ] Age Appropriate Design Code assessment completed (Principle 3)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Safeguarding controls verified in production configuration

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
| 1 | Learner-Centred Design | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 2 | Safeguarding by Design | Strategic | CRITICAL | Safeguarding impact assessment, access controls verified |
| 3 | Children's Data Privacy | Strategic | CRITICAL | AADC compliance, DPIA, privacy by default |
| 4 | Digital Inclusion and the Pupil Premium Gap | Strategic | HIGH | Low-bandwidth testing, disadvantage analytics |
| 5 | Scalability and Elasticity | Strategic | HIGH | Load testing, academic calendar scaling |
| 6 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 7 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 8 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, retention policies |
| 9 | Interoperability with Education Data Ecosystem | Data | HIGH | DfE Sign-in, GIAS, MIS integration tested |
| 10 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 11 | Single Source of Truth | Data | HIGH | System of record documented per domain |
| 12 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 13 | Event-Driven Integration | Integration | MEDIUM | Async patterns for non-real-time flows |
| 14 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, SEND user testing |
| 15 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring, targets met |
| 16 | Resilience and Fault Tolerance | Quality | CRITICAL | Fault injection testing, RTO/RPO verification |
| 17 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 18 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 19 | Automated Testing | Development | HIGH | Test coverage, pipeline integration |
| 20 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government and Education Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Learner-Centred Design), 9 (Open Standards), 14 (Accessibility), 20 (Open Source) |
| Technology Code of Practice | 9 (Interoperability), 6 (Security), 18 (IaC), 20 (Open Source and Reuse) |
| NCSC Secure by Design | 6 (Security by Design), 18 (IaC), 19 (Automated Testing) |
| UK GDPR / DPA 2018 | 3 (Children's Data Privacy), 8 (Data Sovereignty), 10 (Data Quality) |
| ICO Age Appropriate Design Code | 1 (Learner-Centred Design), 3 (Children's Data Privacy) |
| Children Act 2004 / KCSIE | 2 (Safeguarding by Design), 3 (Children's Data Privacy) |
| Public Sector Accessibility Regulations | 1 (Learner-Centred Design), 14 (Accessibility and Inclusion) |
| HM Treasury Green Book | 5 (Scalability), 15 (Performance), 17 (Availability), 20 (Reuse) |
| DfE Digital Strategy | 4 (Digital Inclusion), 9 (Interoperability), 11 (Single Source of Truth) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| ICO Age Appropriate Design Code | Code of Practice | ICO | 15 standards for children's online services | N/A — external reference |
| Children Act 2004 | Legislation | legislation.gov.uk | Safeguarding duties | N/A — external reference |
| Keeping Children Safe in Education | Statutory guidance | DfE | School safeguarding requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| DfE Sign-in | Platform | DfE | Federated identity for education services | N/A — external reference |
| Get Information About Schools (GIAS) | Register | DfE | Authoritative school/establishment data | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 4: Quality Education — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
