# UK Government Enterprise Architecture Principles — SDG 3: Good Health and Well-Being

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 3: Good Health and Well-Being — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 3 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 3 project teams, Enterprise Architecture Review Board, DHSC Digital |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 3: Good Health and Well-Being programme. These principles apply to five UK Government digital health services:

- **001** — NHS Appointment Booking Platform (DHSC)
- **002** — Mental Health Digital Triage (NHS England)
- **003** — Pandemic Preparedness System (UKHSA)
- **004** — Health Data Research Platform (DHSC)
- **005** — Social Prescribing Link Worker System (NHS)

**Scope**: All technology projects, systems, and initiatives within the SDG 3 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Assessment Framework (CAF), UK GDPR, Data Protection Act 2018, the Public Sector Bodies Accessibility Regulations 2018, the NHS Long Term Plan, the NHS Digital Data and Technology Standards, DCB0129/DCB0160 Clinical Safety Standards, and the Caldicott Principles.

---

## I. Strategic Principles

### 1. Patient-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of patients, service users, carers, and the clinical staff who serve them, with services that are simple, inclusive, and accessible to everyone who needs them.

**Rationale**:
The citizens served by these health programmes include patients booking NHS appointments, individuals in mental health crisis, populations at risk during pandemics, researchers requiring access to health data, and people seeking community wellbeing support. Many are in vulnerable situations — dealing with illness, anxiety, cognitive impairment, or low digital confidence. Systems that are difficult to use create barriers to essential healthcare, worsening health outcomes and increasing health inequalities. The GDS Service Standard and NHS Digital Service Manual mandate patient-centred design.

**Implications**:

- Conduct user research with representative patients including those with disabilities, low digital literacy, sensory impairments, and limited connectivity
- Design for assisted digital journeys — patients who cannot self-serve must have alternative pathways (telephone, in-person)
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement under the Public Sector Bodies Accessibility Regulations 2018
- Support multiple languages and Easy Read formats where appropriate for diverse patient populations
- Use plain language aligned with NHS content style guidance; avoid clinical jargon in patient-facing interfaces
- Provide clear appointment confirmations, status tracking, and next-step guidance so patients understand their care pathway
- Design for situational impairments — users may be unwell, stressed, or in pain when interacting with health services

**Validation Gates**:

- [ ] User research conducted with representative sample including patients with diverse needs and vulnerabilities
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Assisted digital pathway defined and tested for each patient-facing service
- [ ] Content reviewed against NHS content style guide for plain language and readability
- [ ] Patient satisfaction metrics defined and baseline established
- [ ] Service assessed against GDS Service Standard points 1–3 and NHS service standard

---

### 2. Clinical Safety by Design (NON-NEGOTIABLE)

**Principle Statement**:
All health IT systems MUST comply with DCB0129 (Clinical Risk Management: its Application in the Manufacture of Health IT Systems) and DCB0160 (Clinical Risk Management: its Application in the Deployment and Use of Health IT Systems). Clinical safety hazards MUST be identified, assessed, and mitigated before any system is deployed in a clinical context.

**Rationale**:
Health IT systems can directly affect patient safety. An appointment booking system that fails to prioritise urgent referrals, a mental health triage tool that misclassifies risk, or a pandemic surveillance platform that underreports cases can cause serious harm or death. The NHS mandates clinical risk management through DCB0129 and DCB0160 as a legal requirement. Clinical safety is not optional and cannot be deferred.

**Implications**:

- Appoint a Clinical Safety Officer (CSO) for each project as required by DCB0129
- Conduct and maintain a Clinical Risk Management Plan and Clinical Safety Case throughout the system lifecycle
- Perform Hazard Analysis and Risk Assessment (HARA) identifying potential clinical hazards, their severity, and mitigation controls
- Classify all hazards using the NHS risk matrix (consequence × likelihood)
- Ensure clinical safety testing is embedded in the testing strategy — not treated as a separate activity
- Maintain a Clinical Risk Management File with evidence of all safety activities
- Involve clinicians in design, testing, and deployment decisions
- Report clinical safety incidents through MHRA and NHS reporting mechanisms

**Validation Gates**:

- [ ] Clinical Safety Officer appointed and active for each project
- [ ] Clinical Risk Management Plan completed and approved
- [ ] Hazard Log maintained with all identified hazards, controls, and residual risk ratings
- [ ] Clinical Safety Case Report produced and approved before deployment
- [ ] DCB0129 and DCB0160 compliance confirmed by independent clinical safety audit
- [ ] Clinical incident reporting pathway established and tested

---

### 3. Interoperability and NHS Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using NHS and international health data standards. HL7 FHIR R4 (UK Core) MUST be the default standard for health data exchange. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 3 programme spans DHSC, NHS England, UKHSA, and the wider NHS. Each project must integrate with existing NHS national services — the Personal Demographics Service (PDS), NHS Spine, the e-Referral Service (e-RS), GP Connect, the Summary Care Record, and NHS login. The Technology Code of Practice mandates open standards. HL7 FHIR R4 is the NHS-endorsed standard for health data interoperability, enabling joined-up care that improves patient outcomes.

**Implications**:

- Use HL7 FHIR R4 UK Core profiles as the default for all clinical data exchange
- Implement SNOMED CT for clinical terminology encoding across all services
- Use dm+d (Dictionary of Medicines and Devices) for medication data
- Register APIs on the NHS API Catalogue for discoverability
- Version all interfaces with documented backward compatibility strategies
- Publish interface specifications using OpenAPI 3.0 and FHIR Implementation Guides
- No direct database access across system boundaries
- Align with NHS Data Model and Dictionary standards
- Support NHS Number as the primary patient identifier across all systems

**Validation Gates**:

- [ ] HL7 FHIR R4 UK Core profiles implemented for all clinical data exchanges
- [ ] SNOMED CT coding applied for clinical terminology
- [ ] APIs registered on NHS API Catalogue
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication via NHS Identity and NHS CIS2 for staff, NHS login for patients
- [ ] No direct database coupling across systems
- [ ] Compliance with NHS Digital Interoperability Standards verified

---

### 4. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one. Health data demands the highest level of protection.

**Rationale**:
These systems process highly sensitive health data — medical conditions, mental health assessments, disease surveillance records, and genomic research data. Health data is classified as special category data under UK GDPR Article 9. A breach would cause severe harm to patients, undermine public trust in the NHS, and violate legal obligations. The NCSC Cyber Assessment Framework (CAF), NHS Data Security and Protection Toolkit (DSPT), and the Secure by Design framework mandate proactive security.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised using NHS Identity or equivalent
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible; role-based access aligned with legitimate clinical relationships
3. **Encryption Everywhere**: Data encrypted in transit (TLS 1.3+) and at rest (AES-256) without exception
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies; detect and respond to insider threats

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff access via NHS CIS2 smartcard or equivalent
- [ ] Service-to-service authentication using mutual TLS or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or environment variables)
- [ ] Network segmentation with N3/HSCN controls and deny-by-default policies
- [ ] Encryption at rest for all data stores containing patient or sensitive data
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all data access events (who accessed what patient record, when, and why)
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)
- [ ] Break-glass procedures for emergency clinical access with mandatory post-access audit

**Compliance Frameworks**:

- NCSC Cyber Assessment Framework (CAF)
- NHS Data Security and Protection Toolkit (DSPT) — all 10 standards met
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018 (special category health data provisions)
- HMG Security Policy Framework
- OWASP Top 10 (for application-layer controls)

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed for each service
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] NHS DSPT self-assessment completed with all mandatory assertions met
- [ ] Security testing plan defined and executed before go-live
- [ ] Incident response runbook created with defined escalation paths including NCSC and NHS Digital
- [ ] NCSC CAF assessment completed for critical national infrastructure services (pandemic preparedness)

---

### 5. Privacy by Design and the Caldicott Principles

**Principle Statement**:
All systems MUST embed privacy protections into the architecture from the outset, minimising personal health data collection, processing, and retention to what is strictly necessary. The Caldicott Principles MUST govern all decisions about patient-identifiable information.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. Health data receives additional protection under Article 9 as special category data. The Caldicott Principles — established specifically for the NHS — provide the ethical framework for handling patient information. Citizens must trust that their health data is protected; erosion of trust damages public health outcomes as patients withhold information from clinicians.

**The Seven Caldicott Principles**:

1. **Justify the purpose(s)** — every proposed use of patient data must be clearly defined
2. **Don't use patient-identifiable information unless absolutely necessary**
3. **Use the minimum necessary patient-identifiable information**
4. **Access to patient-identifiable information should be on a strict need-to-know basis**
5. **Everyone with access must understand their responsibilities**
6. **Comply with the law** — UK GDPR, DPA 2018, Common Law Duty of Confidentiality
7. **The duty to share information is as important as the duty to protect** — share where it benefits patient care

**Implications**:

- Appoint a Caldicott Guardian for the programme to oversee patient data decisions
- Conduct Data Protection Impact Assessments (DPIAs) for all services processing patient data
- Implement pseudonymisation by default for analytics, research, and secondary uses
- Support data subject rights: access, rectification, erasure, portability, and objection
- Implement granular consent management where patients control data sharing preferences
- Ensure transparency — patients must be able to see who has accessed their record and why
- De-identify data for research purposes using NHS Digital's Trusted Research Environment model

**Validation Gates**:

- [ ] Caldicott Guardian appointed and actively engaged
- [ ] DPIAs completed for each service and reviewed by the Data Protection Officer
- [ ] Data minimisation review conducted — no unnecessary patient data collected
- [ ] Privacy notices published in plain language, meeting NHS transparency requirements
- [ ] Data subject rights mechanisms implemented and tested
- [ ] Pseudonymisation or de-identification applied to all secondary use data
- [ ] National Data Opt-Out respected across all services

---

### 6. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning. Health service systems MUST additionally provide clinical operational dashboards and patient pathway visibility.

**Rationale**:
We cannot operate what we cannot observe. For health services, operational blindness translates directly to delayed appointments, undetected system degradation affecting mental health triage, or missed pandemic signals. Instrumentation is a first-class architectural requirement. Additionally, health services must report operational metrics to NHS England and DHSC.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing; access logs for patient data must include user identity and justification
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, queue depths
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert
- **Clinical Metrics**: Appointment wait times, triage response times, referral completion rates

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (appointments booked, triage assessments completed, referrals processed, surveillance alerts raised)
- Security events (authentication failures, break-glass access, suspicious data access patterns)
- Patient pathway metrics (time from referral to appointment, time from triage to clinical review)

**Log Retention**:

- **Security/audit logs**: Minimum 8 years (aligned with NHS Records Management Code of Practice 2021)
- **Clinical audit logs**: 8 years minimum (patient data access records)
- **Application logs**: 90 days minimum for troubleshooting
- **Metrics**: 2 years with progressive aggregation for trend analysis

**Validation Gates**:

- [ ] Logging, metrics, and tracing instrumented for all services
- [ ] Dashboards configured for operational, clinical, and business metrics
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for all alerting scenarios
- [ ] Capacity planning metrics tracked and reviewed monthly
- [ ] Patient data access audit trail queryable for Caldicott review and subject access requests

---

## II. Data Principles

### 7. Data Sovereignty and Health Data Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Common Law Duty of Confidentiality, and NHS data governance policies. All patient data MUST reside within UK sovereign infrastructure.

**Rationale**:
These services process large volumes of sensitive patient health data — appointment records, mental health assessments, disease surveillance intelligence, and research datasets. Health data is special category data under UK GDPR and is additionally subject to the Common Law Duty of Confidentiality. Mishandling this data causes direct harm to patients and violates legal obligations.

**Data Classification Tiers**:

1. **OFFICIAL**: Standard NHS business data with baseline controls (e.g., anonymised aggregate statistics)
2. **OFFICIAL-SENSITIVE**: Patient-identifiable data, clinical records, mental health assessments, genomic data — enhanced controls required
3. **SECRET**: National security health intelligence (pandemic threat assessments) — highest controls

**Data Residency**:

- All patient data MUST reside within UK sovereign data centres
- No transfer of patient data outside the UK without Caldicott Guardian approval, a lawful basis, and a DPIA
- Cross-organisational data sharing MUST be governed by Data Sharing Agreements and Data Processing Agreements
- Research data access MUST use Trusted Research Environments (TREs) — data does not leave the secure environment

**Data Retention**:

- Clinical records: Aligned with NHS Records Management Code of Practice 2021 (typically 8 years after last treatment, longer for specific categories)
- Research data: As specified in the research protocol and ethics approval
- Pandemic surveillance data: Retained for epidemiological trend analysis as specified by UKHSA retention schedule
- Automatic deletion or anonymisation after the defined retention period expires

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all patient data storage and processing
- [ ] Retention policies configured aligned with NHS Records Management Code of Practice
- [ ] Data Sharing Agreements in place for all cross-organisational data flows
- [ ] Data Protection Impact Assessments completed for all services processing patient data
- [ ] National Data Opt-Out implemented and tested

---

### 8. Data Quality and Clinical Data Integrity

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and clinical decision transparency. Clinical data used for patient care decisions MUST meet the highest quality standards.

**Rationale**:
Decisions made by these systems — appointment prioritisation, mental health risk assessment, pandemic response activation, research conclusions — directly affect patient safety and public health. Poor data quality in a triage algorithm leads to wrong clinical decisions. Poor data quality in a pandemic surveillance system leads to delayed responses. Lineage enables accountability and clinical governance.

**Quality Standards**:

- **Completeness**: NHS Number, demographics, and clinical codes validated at point of entry
- **Consistency**: Cross-system reconciliation with PDS as the authoritative source for patient demographics
- **Accuracy**: SNOMED CT and dm+d coding enforced; clinical validation rules applied at source
- **Timeliness**: Freshness SLAs defined per data flow — real-time for urgent clinical data, near-real-time for surveillance

**Lineage Requirements**:

- Source-to-target mapping documented for all clinical data flows
- Transformation logic version-controlled and auditable for clinical governance review
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for schema changes (clinical safety implications of data model changes)

**Validation Gates**:

- [ ] Data quality rules defined and automated with monitoring
- [ ] Lineage metadata captured and queryable for clinical governance
- [ ] Data contracts defined between producing and consuming systems
- [ ] Schema evolution strategy documented with clinical safety assessment for changes
- [ ] NHS Data Quality Maturity Index assessment completed

---

### 9. Single Source of Truth for Patient Identity

**Principle Statement**:
The NHS Personal Demographics Service (PDS) MUST be the single authoritative source for patient demographic data. Every data domain MUST have a clearly identified system of record. Derived copies MUST be clearly labelled and synchronised.

**Rationale**:
Patient safety depends on accurate identification. A patient's name, date of birth, NHS Number, and address changing in one system but not another leads to wrong patient errors, failed communications, and clinical risk. The PDS is the national master for patient demographics and must be treated as authoritative.

**Implications**:

- Use PDS as the master for patient demographics (name, address, date of birth, NHS Number, GP registration)
- Implement PDS synchronisation (MESH or FHIR) to keep local caches current
- Use NHS Number as the primary patient identifier — never create local patient identifiers as primary keys
- Derived or cached copies are read-only and clearly labelled with source and freshness
- Avoid bidirectional synchronisation — it creates split-brain scenarios and patient safety risk
- For clinical systems of record, identify and document the authoritative source (e.g., GP clinical system for primary care data, hospital PAS for secondary care data)

**Validation Gates**:

- [ ] PDS integration implemented for patient demographics
- [ ] NHS Number used as primary patient identifier across all services
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without a documented conflict resolution strategy
- [ ] Patient matching and merging procedures defined for duplicate record management

---

## III. Integration Principles

### 10. Loose Coupling with NHS National Services

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies. Integration with NHS national services (Spine, PDS, e-RS, GP Connect) MUST use the approved NHS integration patterns.

**Rationale**:
The SDG 3 programme spans five projects across DHSC, NHS England, UKHSA, and the wider NHS. Each team must be able to develop, deploy, and evolve their service independently. NHS national services have their own release cycles and availability characteristics — systems must be resilient to changes in these shared dependencies.

**Implications**:

- Communicate through published APIs (FHIR, REST) or asynchronous events (MESH, event streaming) — never through shared databases
- Each system manages its own data lifecycle and data store
- Integration with NHS Spine must use the NHS Spine Integration Engine or equivalent approved pattern
- Use NHS MESH for asynchronous file-based messaging where required by NHS national service interfaces
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across system boundaries; use compensating actions or sagas

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] NHS national service integrations use approved patterns (Spine Integration Engine, MESH, GP Connect FHIR)
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees
- [ ] Resilience patterns implemented for NHS Spine and PDS dependency (circuit breakers, caching, graceful degradation)

---

### 11. Event-Driven Health Data Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for non-real-time interactions to improve resilience, decoupling, and auditability of health data flows.

**Rationale**:
Many cross-organisational health workflows are inherently asynchronous — a GP referral does not require an immediate response from the hospital booking system, pandemic surveillance data does not need real-time processing for trend analysis, and research data access requests follow a governed approval workflow. Event-driven patterns reduce temporal coupling and improve fault tolerance.

**When to Use Asynchronous Patterns**:

- Clinical referrals and appointment notifications between organisations
- Pandemic surveillance data ingestion from laboratory and clinical sources
- Research data access requests and approval workflows
- Audit trail events and compliance logging
- Social prescribing referral notifications between NHS and community organisations

**When Synchronous Communication is Acceptable**:

- Real-time patient identity verification (PDS lookup during appointment booking)
- Urgent clinical lookups during consultation (Summary Care Record access)
- Triage risk assessments requiring immediate clinical decision support
- Patient authentication via NHS login

**Validation Gates**:

- [ ] Asynchronous patterns used for non-real-time cross-organisational health data flows
- [ ] Message durability and delivery guarantees defined (at-least-once for clinical messages)
- [ ] Event schemas versioned and published using FHIR messaging profiles where applicable
- [ ] Dead letter handling and error recovery procedures defined for clinical message failures
- [ ] NHS MESH configured for national service messaging where required

---

## IV. Quality Attributes

### 12. Scalability and Elasticity for NHS Demand Patterns

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on NHS demand patterns including seasonal variation, flu season, Monday morning surges, and pandemic response scaling.

**Rationale**:
NHS digital services experience significant demand variation. Appointment booking surges on Monday mornings and after bank holidays. Mental health services see increased demand during winter and around Christmas. Pandemic surveillance must scale from routine monitoring to national emergency response within hours. Systems must handle both sustained growth and acute spikes.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes within UK sovereign infrastructure
- Capacity plan for pandemic surge scenarios (100x normal load within 48 hours for pandemic systems)
- Use auto-scaling based on demand metrics with cost controls
- Design for the "Monday morning effect" — plan for 3-5x average load during GP booking windows

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Pandemic surge scenario tested for UKHSA services (100x scaling within 48 hours)
- [ ] Cost model accounts for variable capacity including seasonal peaks
- [ ] "Monday morning effect" load testing completed for appointment booking services

---

### 13. Availability and Clinical Service Continuity

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss. Clinical-facing systems MUST achieve availability levels that ensure patient safety is never compromised by system downtime.

**Rationale**:
NHS services are critical to patient welfare. An appointment booking system outage means patients cannot access healthcare. A mental health triage failure during out-of-hours means vulnerable people cannot get crisis support. Pandemic surveillance downtime means disease signals are missed. Availability targets must reflect the clinical impact of system failure.

**Availability Targets**:

- **Patient-facing booking systems**: 99.95% (26 minutes downtime per month maximum)
- **Mental health triage (24/7)**: 99.99% (4.4 minutes downtime per month maximum)
- **Pandemic surveillance**: 99.9% in routine mode, 99.99% during active pandemic response
- **Research platform**: 99.5% (3.6 hours downtime per month; planned maintenance windows acceptable)
- **Social prescribing**: 99.9% during NHS operating hours

**High Availability Patterns**:

- Redundancy across multiple availability zones within UK sovereign cloud regions
- Automated health checks with self-healing recovery
- Active-active configurations for critical clinical services
- Regular disaster recovery testing (quarterly for patient-facing services, monthly during pandemic activation)

**Validation Gates**:

- [ ] Availability SLA defined per service based on clinical impact assessment
- [ ] RTO defined: 15 minutes for critical clinical services, 4 hours for non-critical
- [ ] RPO defined: zero data loss for clinical transactions, 1 hour for analytical workloads
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Business Continuity Plan including manual clinical fallback procedures

---

### 14. Performance for Clinical Workflows

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load. Clinical-facing systems MUST provide response times that do not delay patient care or clinical decision-making.

**Rationale**:
Clinicians operate under extreme time pressure. A GP has an average of 10 minutes per consultation — a slow appointment booking system consumes that time. Mental health triage must provide risk assessment results within seconds to support safe clinical decisions. Patients accessing services may be unwell, anxious, or in pain — slow systems cause abandonment and missed care.

**Performance Targets**:

- **Patient-facing pages**: < 1.5 seconds load time (p95) over 3G mobile connection
- **API response time**: < 300ms (p95) for clinical lookups (PDS, SCR)
- **Triage risk calculation**: < 2 seconds (p99) for mental health assessment scoring
- **Appointment search and booking**: < 3 seconds (p95) for available slot retrieval
- **Pandemic dashboard refresh**: < 5 seconds for national surveillance overview

**Implications**:

- Performance requirements defined before implementation, informed by clinical workflow analysis
- Load testing performed before every production deployment
- Performance monitoring continuous with alerting on degradation
- Optimise for the slowest expected client (low-end mobile on 3G connection for patient-facing services)
- Caching strategies defined for expensive lookups (PDS, GP practice lists)

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service and user journey
- [ ] Load testing performed at expected and peak capacity including Monday morning surge
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly
- [ ] Clinical workflow timing analysis confirming system does not delay patient care

---

## V. Development Practices

### 15. Infrastructure as Code within NHS Approved Cloud

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines to NHS-approved cloud infrastructure. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. For health services processing patient data, infrastructure must be reproducible, auditable, and deployed only to NHS-approved cloud platforms that meet DSPT and sovereignty requirements.

**Implications**:

- All infrastructure defined in declarative code within version control
- Infrastructure changes go through the same code review process as application code
- Environments are reproducible from code — no snowflake configurations
- No manual changes to production infrastructure (enforced through access controls)
- Deployment only to NHS-approved cloud platforms with UK sovereignty and DSPT compliance
- Infrastructure code includes security controls, network segmentation, and encryption configuration

**Validation Gates**:

- [ ] All infrastructure defined as code in version control
- [ ] Infrastructure code goes through peer review before deployment
- [ ] Environments reproducible from code (tested through regular rebuilds)
- [ ] No manual infrastructure changes in production (enforced, not just policy)
- [ ] Cloud platform approved for NHS workloads (NHS Digital cloud guidance compliance)

---

### 16. Automated Testing with Clinical Safety Validation

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment. Systems with clinical safety implications MUST include automated validation of clinical safety controls as part of the test suite.

**Rationale**:
These systems make decisions or provide information that affects patient safety. A defect in appointment booking could assign a cancer two-week-wait referral to a routine queue. A bug in mental health triage could misclassify a high-risk patient as low-risk. Automated testing provides a safety net that manual testing alone cannot match, and clinical safety testing must be an integral part of the pipeline.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test component interactions including NHS national service integrations (15–20% of tests)
- **End-to-End Tests**: Critical patient journeys and clinical safety scenarios (5–10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct clinical outcomes?)
- Clinical safety tests (does it correctly identify and route urgent cases?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (does it meet clinical response time targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- HL7 FHIR conformance tests (does data exchange comply with FHIR UK Core profiles?)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Clinical safety test scenarios defined with Clinical Safety Officer and included in automated suite
- [ ] Critical patient journeys have end-to-end tests
- [ ] FHIR conformance testing automated in pipeline
- [ ] Performance and security tests run regularly in the pipeline

---

### 17. Continuous Integration and Deployment with Clinical Governance

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage. Changes to clinical safety-critical components MUST additionally pass clinical governance review gates.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent, manual releases. However, health systems require additional governance for changes that affect clinical safety. The pipeline must enforce both technical quality gates and clinical safety gates without creating bottlenecks that delay critical safety patches.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, clinical safety, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Clinical Review Gate**: Changes flagged as clinically significant require CSO review
6. **Deployment**: Automated deployment with progressive rollout (canary or blue-green)

**Quality Gates**:

- All automated tests must pass including clinical safety scenarios
- No critical or high security vulnerabilities
- Peer review approval required
- Accessibility checks passed
- Clinical Safety Officer sign-off for changes affecting clinical logic
- Production deployment requires documented change approval

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes security scanning, accessibility checks, and clinical safety tests
- [ ] Clinical governance review gate implemented for clinically significant changes
- [ ] Deployment is automated and repeatable across all environments
- [ ] Rollback capability tested and documented with clinical safety assessment of rollback impact

---

### 18. Accessibility and Digital Inclusion for Health Services

**Principle Statement**:
All patient-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, health conditions, and devices.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. People accessing health services are disproportionately likely to have disabilities, visual or hearing impairments, cognitive difficulties, or to be elderly. They may be using assistive technologies, older devices, or accessing services in clinical environments with poor connectivity. Additionally, mental health conditions, pain, and medication side effects create situational impairments.

**Implications**:

- Design using progressive enhancement — core booking and triage functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing, high-contrast modes, and user font preferences
- Ensure all interactive elements are keyboard-accessible
- Provide British Sign Language (BSL) video content for deaf patients where clinically important
- Support Easy Read format for patients with learning disabilities
- Publish an accessibility statement for each service and provide accessible alternatives

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies (e.g., JAWS, VoiceOver)
- [ ] Keyboard-only navigation tested for all patient journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow (3G) connections
- [ ] Easy Read and BSL alternatives provided for critical health information

---

### 19. Open Source and NHS Reuse

**Principle Statement**:
Teams SHOULD use existing NHS shared platforms and open source solutions where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice requires government teams to make source code open where possible. The NHS has invested significantly in shared platforms — NHS login, NHS Notify, NHS.UK Design System, NHS API Management — and reusing these reduces cost, accelerates delivery, and provides consistent patient experience. Publishing code as open source benefits the wider health system.

**Implications**:

- Evaluate NHS shared platforms before building bespoke: NHS login (patient authentication), NHS Notify (notifications), NHS.UK Design System (frontend components), NHS API Management
- Use GOV.UK shared platforms where NHS-specific equivalents do not exist (GOV.UK Pay, GOV.UK PaaS)
- Use established open source health IT components where they meet requirements (e.g., HAPI FHIR Server, OpenEHR)
- Publish source code openly unless it contains security-sensitive logic or clinical safety-critical algorithms
- Contribute improvements back to NHS open source projects
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] NHS and GOV.UK shared platforms evaluated before building bespoke alternatives
- [ ] Third-party dependency register maintained with licence compliance
- [ ] Source code published openly or justification documented for exceptions
- [ ] No proprietary lock-in to a single vendor's health IT ecosystem without documented justification

---

### 20. Resilience and Fault Tolerance for Clinical Systems

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention. Clinical systems MUST have defined fallback procedures to ensure patient safety is maintained during system outages.

**Rationale**:
NHS national services (Spine, PDS, e-RS) experience planned and unplanned downtime. Laboratory systems, GP clinical systems, and hospital Patient Administration Systems have varying availability. Clinical systems must continue to function safely when dependencies are unavailable — a system that fails completely when the Spine is down is not acceptable for patient care.

**Implications**:

- Implement circuit breakers for all external dependencies including NHS national services
- Use timeouts on all network calls with clinically appropriate defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable (e.g., display cached patient demographics if PDS is temporarily down)
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services
- Define and document manual clinical fallback procedures for each critical system function

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical clinical paths
- [ ] Fault injection testing performed for NHS Spine and PDS unavailability scenarios
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined per service
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented with patient-facing messaging
- [ ] Manual clinical fallback procedures defined, tested, and communicated to clinical staff

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within acceptable cost or timescale
- Regulatory or legal requirements that conflict with a principle
- Transitional state during migration from legacy NHS systems (time-bound)
- Pilot or proof-of-concept with a defined end date and decision point
- Clinical safety requirement that necessitates deviation from a non-safety principle

**Exception Request Requirements**:

- [ ] Written justification with business, technical, and clinical rationale
- [ ] Alternative approach attempted and reason it was insufficient
- [ ] Compensating controls that partially address the principle's intent
- [ ] Risk assessment including clinical safety impact if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance
- [ ] Clinical Safety Officer review for any exception affecting clinical systems

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 4) or Privacy/Caldicott (Principle 5)
4. Clinical Safety Officer approval required for exceptions to Clinical Safety (Principle 2)
5. Document approved exception in the project's Architecture Decision Records
6. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS/NHS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] User research evidence supports design approach (Principle 1)
- [ ] Clinical safety approach defined and CSO appointed (Principle 2)
- [ ] Data classification and privacy approach defined (Principles 5, 7)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 4)
- [ ] HL7 FHIR integration approach validated (Principle 3)
- [ ] Accessibility approach validated (Principle 18)
- [ ] Clinical Safety Case Report drafted (Principle 2)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] DCB0129/DCB0160 compliance confirmed
- [ ] NHS DSPT self-assessment completed
- [ ] Penetration testing completed with no unresolved critical or high findings

### Enforcement

- Architecture reviews are **mandatory** for all projects at each phase gate
- Principle violations must be remediated or exception-approved before production deployment
- Clinical safety principle violations are escalated to NHS England and cannot be overridden locally
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective compliance reviews conducted annually for live services

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | Patient-Centred Design | Strategic | CRITICAL | User research, accessibility audit, GDS/NHS assessment |
| 2 | Clinical Safety by Design | Strategic | CRITICAL | DCB0129/DCB0160 compliance, Hazard Log, CSO sign-off |
| 3 | Interoperability and NHS Standards | Strategic | CRITICAL | HL7 FHIR compliance, NHS API Catalogue registration |
| 4 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, DSPT, NCSC CAF |
| 5 | Privacy by Design and Caldicott | Data | CRITICAL | DPIA, Caldicott Guardian, National Data Opt-Out |
| 6 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, SLOs, clinical dashboards |
| 7 | Data Sovereignty and Health Data Governance | Data | CRITICAL | UK residency, classification, NHS retention compliance |
| 8 | Data Quality and Clinical Data Integrity | Data | CRITICAL | Quality metrics, lineage, SNOMED CT compliance |
| 9 | Single Source of Truth for Patient Identity | Data | CRITICAL | PDS integration, NHS Number as primary identifier |
| 10 | Loose Coupling with NHS National Services | Integration | HIGH | Deployment independence, Spine/PDS resilience |
| 11 | Event-Driven Health Data Integration | Integration | MEDIUM | Async patterns, FHIR messaging, NHS MESH |
| 12 | Scalability and Elasticity | Quality | HIGH | Load testing, pandemic surge, Monday morning scaling |
| 13 | Availability and Clinical Service Continuity | Quality | CRITICAL | SLA monitoring, DR testing, clinical fallback |
| 14 | Performance for Clinical Workflows | Quality | HIGH | Load testing, clinical workflow timing |
| 15 | Infrastructure as Code within NHS Approved Cloud | Development | HIGH | IaC coverage, NHS cloud approval |
| 16 | Automated Testing with Clinical Safety Validation | Development | HIGH | Test coverage, clinical safety tests, FHIR conformance |
| 17 | CI/CD with Clinical Governance | Development | HIGH | Pipeline exists, clinical review gates |
| 18 | Accessibility and Digital Inclusion | Quality | CRITICAL | WCAG 2.2 AA, assistive tech testing, Easy Read |
| 19 | Open Source and NHS Reuse | Development | MEDIUM | NHS platforms evaluated, code published |
| 20 | Resilience and Fault Tolerance | Quality | CRITICAL | Fault injection, clinical fallback procedures |

### Alignment to UK Government and NHS Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Patient-Centred Design), 3 (Interoperability), 18 (Accessibility), 19 (Open Source) |
| Technology Code of Practice | 3 (Interoperability), 4 (Security), 15 (IaC), 19 (Open Source and Reuse) |
| NCSC Cyber Assessment Framework | 4 (Security by Design), 15 (IaC), 16 (Automated Testing), 17 (CI/CD) |
| UK GDPR / DPA 2018 | 5 (Privacy/Caldicott), 7 (Data Sovereignty), 8 (Data Quality) |
| DCB0129 / DCB0160 Clinical Safety | 2 (Clinical Safety by Design), 16 (Clinical Safety Testing), 17 (Clinical Governance Gates) |
| NHS Long Term Plan | 1 (Patient-Centred), 3 (Interoperability/FHIR), 12 (Scalability), 18 (Digital Inclusion) |
| NHS Data Security and Protection Toolkit | 4 (Security), 5 (Privacy), 7 (Data Governance) |
| Caldicott Principles | 5 (Privacy by Design and Caldicott), 7 (Data Sovereignty), 9 (Single Source of Truth) |
| Public Sector Accessibility Regulations | 1 (Patient-Centred Design), 18 (Accessibility and Digital Inclusion) |
| HM Treasury Green Book | 12 (Scalability), 14 (Performance), 13 (Availability), 19 (Reuse) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| NCSC Cyber Assessment Framework | Guidance | NCSC | Security principles for CNI | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| DCB0129 | Standard | NHS Digital | Clinical risk management (manufacture) | N/A — external reference |
| DCB0160 | Standard | NHS Digital | Clinical risk management (deployment) | N/A — external reference |
| HL7 FHIR R4 UK Core | Standard | HL7 UK / NHS Digital | FHIR profiles for UK health data | N/A — external reference |
| Caldicott Principles | Guidance | UK Government | Patient data handling principles | N/A — external reference |
| NHS DSPT | Standard | NHS Digital | Data security and protection toolkit | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| NHS Long Term Plan | Strategy | NHS England | 10-year plan for NHS transformation | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 3: Good Health and Well-Being — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
