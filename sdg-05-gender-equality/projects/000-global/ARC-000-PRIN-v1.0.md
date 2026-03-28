# UK Government Enterprise Architecture Principles — SDG 5: Gender Equality

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 5: Gender Equality — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 5 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 5 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 5: Gender Equality programme. These principles apply to four UK Government digital services:

- **001** — Gender Pay Gap Reporting Platform (GEO)
- **002** — Domestic Abuse Case Management (Home Office)
- **003** — Workplace Equality Monitoring (EHRC)
- **004** — Women in STEM Tracking Dashboard (DSIT)

**Scope**: All technology projects, systems, and initiatives within the SDG 5 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Secure by Design, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, Equality Act 2010, the Domestic Abuse Act 2021, and the UK National Action Plan on Women, Peace and Security.

**Domain Sensitivity**: This programme handles data spanning employer pay gap disclosures, domestic abuse survivor case records, workplace discrimination complaints, and workforce diversity metrics. Several of these data categories carry life-safety implications — particularly domestic abuse case management — demanding principles that go beyond standard government digital service requirements.

---

## I. Strategic Principles

### 1. Trauma-Informed Design

**Principle Statement**:
All systems handling domestic abuse, discrimination, or personal vulnerability data MUST be designed using trauma-informed principles, ensuring that technology interactions do not re-traumatise users or place them at risk.

**Rationale**:
The Domestic Abuse Act 2021 recognised that survivors of domestic abuse interact with multiple agencies during periods of extreme vulnerability. Digital services that are insensitive to trauma — through harsh language, inflexible processes, or surveillance-vulnerable interfaces — can cause harm and deter people from seeking help. The Home Office Domestic Abuse Statutory Guidance mandates trauma-informed approaches across all agencies.

**Implications**:

- Design interfaces that allow users to stop and resume at any point without data loss
- Avoid countdown timers, aggressive session warnings, or language that implies judgement
- Provide clear exit routes (quick-exit buttons) for users who may be monitored by an abuser
- Allow proxy access where survivors cannot safely interact with the system directly
- Content and microcopy must be reviewed by specialist domestic abuse services
- Avoid requiring users to repeatedly recount traumatic experiences across service boundaries

**Validation Gates**:

- [ ] Trauma-informed design review conducted with specialist domestic abuse service input
- [ ] Quick-exit functionality tested and accessible from every page
- [ ] Proxy access and safe contact mechanisms implemented and tested
- [ ] Session management designed to avoid re-traumatisation (no aggressive timeouts)
- [ ] Content reviewed by specialist organisations (e.g., Women's Aid, Refuge)
- [ ] User research conducted with survivors in safe, ethical research settings

---

### 2. User-Centred Design

**Principle Statement**:
All systems MUST be designed around the needs of end users, with services that are simple, inclusive, and accessible to everyone who needs them.

**Rationale**:
The users of these services span a wide spectrum — from large employers completing pay gap submissions, to domestic abuse survivors in crisis, to EHRC enforcement officers, to STEM researchers. Each user group has distinct needs, technical capabilities, and risk profiles. The GDS Service Standard mandates user-centred design, and the Equality Act 2010 requires reasonable adjustments for disabled users.

**Implications**:

- Conduct user research with representative users, including those with disabilities, low digital literacy, and limited English proficiency
- Design for assisted digital journeys — not all users can self-serve online
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement
- Support multiple languages where user populations require it (e.g., Welsh language for EHRC services)
- Use plain language appropriate to the service audience — employer-facing and survivor-facing language differ fundamentally
- Provide clear status information so users understand where they are in a process

**Validation Gates**:

- [ ] User research conducted with representative sample including vulnerable users
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Assisted digital pathway defined and tested
- [ ] Content reviewed for plain language and readability appropriate to each user group
- [ ] User satisfaction metrics defined and baseline established
- [ ] Service assessed against GDS Service Standard points 1-3

---

### 3. Survivor Safety as a Non-Negotiable Constraint

**Principle Statement**:
All architecture decisions affecting domestic abuse services MUST be evaluated through a survivor safety lens. No feature, integration, or data-sharing arrangement may be implemented if it creates a risk of abuser discovery, location tracking, or coercive control enablement.

**Rationale**:
Domestic abuse perpetrators routinely use technology as a tool of coercive control — monitoring devices, intercepting communications, and tracking locations. Any system that processes domestic abuse data must assume that a perpetrator may have access to the survivor's device, email, browser history, or postal address. The Domestic Abuse Commissioner and specialist services such as Refuge and Women's Aid have documented extensive cases of technology-facilitated abuse.

**Implications**:

- All notifications (email, SMS, letter) must be evaluated for interception risk before implementation
- Browser history, page titles, and URL structures must not reveal service purpose
- Correspondence addresses must support safe alternatives (e.g., refuge addresses, c/o organisations)
- Data shared between agencies must use controlled disclosure protocols — never bulk sharing
- Location data must never be stored or transmitted for survivor-related records
- Two-factor authentication must offer non-SMS options (abusers may control the phone)

**Validation Gates**:

- [ ] Survivor safety impact assessment completed for all features and integrations
- [ ] Notification channels reviewed for interception risk
- [ ] Browser history and URL structure reviewed for safe browsing
- [ ] Safe address and contact mechanisms implemented
- [ ] Location data handling policy reviewed and approved by specialist organisations
- [ ] Authentication options reviewed for coercive control scenarios

---

### 4. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
This programme handles data spanning employer financial disclosures, domestic abuse survivor records (including location and identity), workplace discrimination complaints, and personal diversity characteristics. A breach of domestic abuse case data could directly endanger lives. A breach of pay gap data before publication could constitute market-sensitive information. NCSC guidance, UK GDPR, and the Secure by Design framework mandate proactive security.

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
- [ ] Enhanced security controls for domestic abuse data — encryption at field level, access logging with alerting

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10
- Domestic Abuse Act 2021 (data protection provisions)

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed for each service
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] Security testing plan defined and executed before go-live
- [ ] Incident response runbook created with defined escalation paths
- [ ] NCSC Secure by Design assessment completed
- [ ] Domestic abuse data breach response plan includes specialist agency notification

---

### 5. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Gender equality services experience significant demand variation — pay gap reporting has a single annual deadline (4 April) creating extreme seasonal load, workplace equality monitoring peaks around employment tribunal cycles, and domestic abuse services experience demand surges following high-profile cases or awareness campaigns. Systems must handle both sustained growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Capacity plan for peak scenarios (e.g., 10,000+ employers submitting pay gap data in final week)

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
Domestic abuse case management is a life-safety service — downtime means caseworkers cannot access risk assessments, safety plans, or multi-agency referrals. Pay gap reporting downtime near the statutory deadline creates compliance risk for thousands of employers. Resilience is not optional for any service in this programme.

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
The SDG 5 programme spans multiple departments (GEO, Home Office, EHRC, DSIT) and must integrate with existing government platforms and external bodies. The Technology Code of Practice mandates the use of open standards. Multi-agency domestic abuse case management requires controlled interoperability with police, health, local authority, and third-sector systems.

**Implications**:

- Use open standards for data exchange and interface contracts
- Version all interfaces with a documented backward compatibility strategy
- Publish interface specifications in a discoverable catalogue
- No direct database access across system boundaries
- Prefer asynchronous communication for non-real-time interactions
- Align with cross-government standards (e.g., GDS API standards)

**Validation Gates**:

- [ ] Interface specifications published using open standard formats
- [ ] Versioning strategy defined with deprecation policy
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified in contracts
- [ ] No direct database coupling across systems
- [ ] Compliance with GDS API technical and data standards verified

---

### 8. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. For domestic abuse case management, undetected service degradation could mean caseworkers cannot access safety plans during a crisis. For pay gap reporting, undetected submission failures near the statutory deadline create mass compliance risk. Instrumentation is a first-class architectural requirement.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (submissions received, cases created, referrals made, complaints processed)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 7 years (domestic abuse case records retention requirements)
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
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Equality Act 2010, and departmental data governance policies.

**Rationale**:
These services process sensitive personal data including protected characteristics under the Equality Act 2010 (sex, gender reassignment, pregnancy and maternity), domestic abuse case records, employer pay data, and workforce diversity statistics. The processing of special category data under UK GDPR Article 9 requires explicit legal basis and enhanced safeguards.

**Data Classification Tiers**:

1. **OFFICIAL**: Published aggregate pay gap data, public STEM statistics
2. **OFFICIAL-SENSITIVE**: Individual employer pay data pre-publication, workforce diversity data, personal equality monitoring data
3. **OFFICIAL-SENSITIVE (DA)**: Domestic abuse case records, survivor identification data, perpetrator information, MARAC minutes — enhanced controls with need-to-know access enforcement

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- No transfer of personal data outside the UK without a lawful basis and Data Protection Impact Assessment
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017

**Data Retention**:

- Pay gap data: Retained for 10 years for trend analysis (aggregated/anonymised after 3 years)
- Domestic abuse case records: Retained per Home Office retention schedule (minimum 7 years, longer for safeguarding)
- Equality monitoring data: Retained for reporting periods then anonymised
- Automatic deletion or anonymisation after the defined retention period expires

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all personal data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed for all services
- [ ] Special category data processing basis documented under UK GDPR Article 9

---

### 10. Gender-Disaggregated Data Standards

**Principle Statement**:
All systems MUST collect, store, and report data using gender-disaggregated standards that enable meaningful analysis of gender disparities while respecting individual privacy and non-binary identities.

**Rationale**:
The core purpose of this programme is to measure, monitor, and reduce gender inequality. Data that is not disaggregated by gender cannot serve this purpose. The UN SDG indicator framework requires gender-disaggregated data. The Equality Act 2010 protects sex and gender reassignment as characteristics, requiring systems to handle both binary and non-binary gender identities. The ONS guidance on sex and gender data collection must inform data standards.

**Implications**:

- Implement consistent gender data fields across all services aligned with ONS harmonised standards
- Support collection of both sex (biological) and gender identity where both are relevant to the service purpose
- Allow non-binary, prefer-not-to-say, and self-describe options where appropriate
- Ensure reporting can produce sex-disaggregated and gender-disaggregated breakdowns
- Anonymisation thresholds must prevent identification of individuals in small cohorts (minimum cell size of 5)
- Intersectional analysis capability — gender crossed with ethnicity, disability, age, region

**Validation Gates**:

- [ ] Gender data fields aligned with ONS harmonised standards
- [ ] Non-binary and self-describe options available where service-appropriate
- [ ] Reporting produces gender-disaggregated breakdowns at required granularity
- [ ] Small cohort suppression rules implemented (minimum cell size of 5)
- [ ] Intersectional analysis capability tested and validated
- [ ] Data standards documented and shared across all programme services

---

### 11. Data Anonymisation and Statistical Disclosure Control

**Principle Statement**:
All systems producing aggregate statistics or published data MUST implement statistical disclosure control to prevent identification of individuals from aggregate data, with enhanced protections for domestic abuse and equality data.

**Rationale**:
Gender equality data frequently involves small populations — a single employer may have only three women in senior leadership, making gender pay gap data potentially identifying. Domestic abuse data in small geographic areas could identify survivors. The ONS Statistical Disclosure Control guidelines and the Code of Practice for Statistics require robust anonymisation for published data.

**Implications**:

- Implement minimum cell size thresholds (no fewer than 5 individuals per published cell)
- Apply complementary suppression to prevent derivation of suppressed cells
- Use perturbation or rounding for sensitive aggregate data
- Domestic abuse data must never be published at geographic granularity below local authority level
- Individual employer pay gap data may only be published in the aggregate form prescribed by the Equality Act 2010 (Specific Duties and Public Authorities) Regulations 2017
- Pseudonymise all data used for analytics, research, and trend reporting

**Validation Gates**:

- [ ] Statistical disclosure control rules implemented and tested
- [ ] Minimum cell size thresholds enforced in all reporting outputs
- [ ] Complementary suppression logic validated
- [ ] Domestic abuse data geographic suppression rules enforced
- [ ] Anonymisation and pseudonymisation approach reviewed by departmental statistician

---

### 12. Privacy by Design

**Principle Statement**:
All systems MUST embed privacy protections into the architecture from the outset, minimising personal data collection, processing, and retention to what is strictly necessary.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. This programme processes special category data (sex, gender reassignment, health data for domestic abuse survivors), requiring enhanced privacy protections. The Equality Act 2010 and the Domestic Abuse Act 2021 create specific data protection obligations for the services in scope.

**Implications**:

- Collect only the minimum personal data required for the stated purpose
- Implement purpose limitation — data collected for one purpose MUST NOT be repurposed without a lawful basis
- Pseudonymise or anonymise data wherever possible, especially for analytics and reporting
- Provide users with clear, accessible privacy notices
- Support data subject rights: access, rectification, erasure, portability, and objection
- Implement privacy-preserving analytics that do not require access to identifiable personal data
- Domestic abuse survivors must be able to exercise data subject rights without the perpetrator being notified

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service
- [ ] Data minimisation review conducted — no unnecessary data collected
- [ ] Privacy notices published in plain language
- [ ] Data subject rights mechanisms implemented and tested
- [ ] Pseudonymisation applied to analytics and reporting data
- [ ] Survivor-safe data subject rights process designed (no abuser notification)

---

### 13. Intersectionality in Data Architecture

**Principle Statement**:
All data models MUST support intersectional analysis — the ability to examine how gender interacts with other protected characteristics (ethnicity, disability, age, sexual orientation, religion, socio-economic status) to produce compounding disadvantage.

**Rationale**:
The Equality Act 2010 Section 14 (dual discrimination) and the Public Sector Equality Duty (PSED) require public bodies to consider the intersectional nature of disadvantage. A Black woman's experience of workplace inequality differs from a white woman's; a disabled woman in STEM faces different barriers from a non-disabled woman. Architecture that siloes gender data from other equality dimensions cannot support the evidence base needed for effective policy.

**Implications**:

- Data models must support multi-dimensional equality analysis without requiring separate data stores
- Collect protected characteristics in a way that enables cross-tabulation while maintaining statistical disclosure control
- Reporting dashboards must support intersectional filtering and comparison
- API endpoints must allow queries that cross equality dimensions
- Anonymisation must be tested against intersectional queries (small intersectional cohorts are highly identifiable)

**Validation Gates**:

- [ ] Data model supports cross-tabulation of gender with other protected characteristics
- [ ] Intersectional reporting tested with realistic data volumes
- [ ] Statistical disclosure control validated for intersectional queries
- [ ] API design supports multi-dimensional equality queries
- [ ] PSED compliance demonstrated through intersectional analysis capability

---

### 14. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, troubleshooting, and decision transparency.

**Rationale**:
Pay gap calculations inform enforcement action under the Equality Act. Domestic abuse risk assessments inform safety planning decisions. Workplace equality metrics inform EHRC compliance investigations. STEM diversity statistics inform research funding allocation. Poor data quality in any of these contexts leads to wrong decisions with real consequences for individuals and organisations.

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

## III. Integration Principles

### 15. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies.

**Rationale**:
The SDG 5 programme spans four projects across four departments (GEO, Home Office, EHRC, DSIT). Each team must be able to develop, deploy, and evolve their service independently. Domestic abuse case management has particularly strict boundary requirements — its data must not be accessible through generic cross-programme interfaces.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each system manages its own data lifecycle and data store
- Domestic abuse case management must have hardened boundaries — no generic programme-level data lake access
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across system boundaries

**Validation Gates**:

- [ ] All inter-system communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has its own independent data store
- [ ] Deployment of one system does not require simultaneous deployment of another
- [ ] Domestic abuse data boundaries hardened with explicit access controls

---

### 16. Controlled Multi-Agency Data Sharing

**Principle Statement**:
Systems supporting multi-agency work (particularly domestic abuse case management) MUST implement controlled, auditable, purpose-limited data sharing with explicit consent management and disclosure logging.

**Rationale**:
Multi-Agency Risk Assessment Conferences (MARACs) require information sharing between police, health, social services, housing, and specialist domestic abuse services. This sharing must be controlled, proportionate, and auditable — the MARAC Operating Protocol and the Crime and Disorder Act 1998 Section 115 provide the legal framework. Uncontrolled data sharing endangers survivors.

**Implications**:

- Implement disclosure logging for every data share — who, what, to whom, when, why, legal basis
- Support consent-based and non-consent-based sharing with clear legal basis documentation
- Data shared for MARAC purposes must not be retained by receiving agencies beyond the purpose
- Implement view-only access where full data transfer is not required
- Information sharing agreements must be version-controlled and machine-readable where possible
- Third-party specialist services (charities, refuges) must be treated as data processors with appropriate contracts

**Validation Gates**:

- [ ] Disclosure logging implemented for all inter-agency data shares
- [ ] Legal basis documented for each data sharing arrangement
- [ ] Information sharing agreements in place and version-controlled
- [ ] Consent management (where applicable) implemented and auditable
- [ ] Data minimisation applied to all shared datasets
- [ ] Third-party data processing agreements in place for all receiving organisations

---

## IV. Quality Attributes

### 17. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources.

**Rationale**:
The pay gap reporting platform must handle extreme peak loads near the statutory deadline (potentially 10,000+ employers submitting in the final days). Domestic abuse case management must deliver instant access to risk assessments for caseworkers in crisis situations. Performance requirements must be defined per service based on operational criticality.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to the user journey
- **Throughput**: Transactions per second at expected and peak load
- **Concurrency**: Simultaneous user capacity for normal and surge scenarios
- **Resource Efficiency**: Utilisation targets that balance responsiveness with cost

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity
- [ ] Performance metrics monitored in production with alerting
- [ ] Capacity planning model defined and reviewed quarterly

---

### 18. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss. Domestic abuse case management services require the highest availability tier.

**Rationale**:
Domestic abuse case management is a life-safety service — unavailability during a crisis could prevent a caseworker from accessing a safety plan or perpetrator risk assessment. Pay gap reporting unavailability near the statutory deadline creates mass employer compliance risk. Availability targets must reflect service criticality and the impact of downtime on users.

**Availability Targets**:

- **Domestic Abuse Case Management**: 99.95% uptime (26 minutes maximum monthly downtime)
- **Pay Gap Reporting Platform**: 99.9% uptime, with enhanced availability (99.95%) during reporting window (January-April)
- **Workplace Equality Monitoring**: 99.9% uptime
- **Women in STEM Dashboard**: 99.5% uptime (primarily analytical, not transactional)

**Validation Gates**:

- [ ] Availability SLA defined per service based on criticality assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated through regular testing

---

### 19. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing and employer-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by people with the widest possible range of abilities, devices, and connectivity.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. The Equality Act 2010 requires reasonable adjustments. Domestic abuse survivors may be accessing services from shared devices, public libraries, or mobile phones with limited data — services must work in constrained environments. Employer-facing services must be accessible to SMEs without dedicated IT support.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Support standard text resizing and high-contrast modes
- Ensure all interactive elements are keyboard-accessible
- Provide alternative formats for content where required
- Publish an accessibility statement for each service
- Domestic abuse services must be usable on low-specification mobile devices over slow connections

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Accessibility statement published and maintained
- [ ] Service usable on low-specification devices and slow connections

---

### 20. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and sufficient documentation for teams to understand and modify the system confidently.

**Rationale**:
Gender equality legislation and policy evolve — pay gap reporting thresholds may change, new protected characteristics may be added, MARAC protocols are updated, STEM diversity targets are revised. Systems must accommodate policy changes without requiring fundamental re-architecture. The Equality Act 2010 has been amended multiple times since enactment.

**Implications**:

- Modular architecture with clear boundaries between policy logic and infrastructure
- Externalise business rules (e.g., pay gap calculation thresholds, reporting deadlines) so policy changes do not require code deployments
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

## V. Development Practices

### 21. Equality Act 2010 Compliance by Design

**Principle Statement**:
All systems MUST embed Equality Act 2010 compliance into their architecture, ensuring that public sector equality duty reporting, reasonable adjustments, and non-discrimination requirements are met through system design rather than manual workarounds.

**Rationale**:
The Public Sector Equality Duty (PSED) under Section 149 of the Equality Act 2010 requires public bodies to have due regard to eliminating discrimination, advancing equality of opportunity, and fostering good relations. Systems that produce equality data, monitor compliance, or support enforcement must embed these legal requirements into their architecture.

**Implications**:

- Pay gap calculation algorithms must precisely implement the Equality Act 2010 (Specific Duties and Public Authorities) Regulations 2017
- EHRC enforcement workflows must align with Equality Act enforcement provisions
- All services must support reasonable adjustments for disabled users as a core capability, not an add-on
- PSED reporting must be producible from system data without manual data collection
- Gender pay gap calculations must handle edge cases defined in ACAS and GEO guidance

**Validation Gates**:

- [ ] Pay gap calculation logic validated against GEO published guidance and test cases
- [ ] EHRC enforcement workflow aligned with Equality Act provisions
- [ ] Reasonable adjustment capability built into all user-facing services
- [ ] PSED reporting capability demonstrated from system data

---

### 22. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. For services handling domestic abuse data, infrastructure changes must be auditable and reproducible to maintain the security posture required for this data classification.

**Implications**:

- All infrastructure defined in declarative code within version control
- Infrastructure changes go through the same code review process as application code
- Environments are reproducible from code
- No manual changes to production infrastructure
- Infrastructure code versioned alongside application code

**Validation Gates**:

- [ ] All infrastructure defined as code in version control
- [ ] Infrastructure code goes through peer review before deployment
- [ ] Environments reproducible from code
- [ ] No manual infrastructure changes in production

---

### 23. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to any shared environment.

**Rationale**:
Pay gap calculations must be mathematically accurate — errors could lead to incorrect enforcement action or allow non-compliant employers to pass validation. Domestic abuse risk assessment tools must produce correct outputs — errors could understate risk and endanger survivors. Automated testing provides the safety net that manual testing alone cannot match.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions and data flows (15-20% of tests)
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (do calculations produce correct outcomes?)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (does it meet latency and throughput targets?)
- Security tests (dependency scanning, static analysis, dynamic testing)
- Policy compliance tests (do pay gap calculations match GEO test cases?)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly in the pipeline

---

### 24. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent releases. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to policy changes (e.g., updated pay gap reporting guidance) and security vulnerabilities.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artefact creation
3. **Test**: Automated test execution (unit, integration, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Deployment**: Automated deployment with progressive rollout

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes security scanning and accessibility checks
- [ ] Deployment is automated and repeatable across all environments
- [ ] Rollback capability tested and documented

---

### 25. Open Source and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, and SHOULD publish their own code as open source unless there is a specific reason not to.

**Rationale**:
The Technology Code of Practice requires government teams to make source code open where possible. Domestic abuse case management security logic MUST NOT be published as open source (it would reveal security architecture to potential abusers), but all other components should default to open.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (GOV.UK Notify, GOV.UK Pay)
- Use established open source components where they meet requirements
- Publish source code openly unless it contains security-sensitive logic
- Domestic abuse case management security architecture: CLOSED SOURCE (justified exception)
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] Government shared platforms evaluated before building bespoke alternatives
- [ ] Third-party dependency register maintained with licence compliance
- [ ] Source code published openly or justification documented for exceptions
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
- [ ] Risk assessment including impact on users (especially survivors) if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 4), Survivor Safety (Principle 3), or Privacy by Design (Principle 12)
4. Document approved exception in the project's Architecture Decision Records
5. Quarterly review of all active exceptions — expired exceptions escalated automatically

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key GDS service assessment milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach aligns with principles — no obvious violations
- [ ] User research evidence supports design approach (Principles 1, 2)
- [ ] Data classification and privacy approach defined (Principles 9, 12)
- [ ] Survivor safety assessment completed for domestic abuse services (Principle 3)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 4)
- [ ] Accessibility approach validated (Principle 19)
- [ ] Equality Act compliance validated (Principle 21)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Survivor safety review completed with specialist organisation input

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
| 1 | Trauma-Informed Design | Strategic | CRITICAL | Specialist review, quick-exit testing, survivor research |
| 2 | User-Centred Design | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 3 | Survivor Safety | Strategic | CRITICAL | Safety impact assessment, notification review, specialist input |
| 4 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC assessment |
| 5 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 6 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection testing, RTO/RPO verification |
| 7 | Interoperability and Open Standards | Strategic | HIGH | API specs, versioning, TCoP compliance |
| 8 | Observability | Strategic | HIGH | Metrics, logs, traces, SLOs defined |
| 9 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, retention policies |
| 10 | Gender-Disaggregated Data Standards | Data | CRITICAL | ONS alignment, intersectional analysis, SDC rules |
| 11 | Data Anonymisation and SDC | Data | CRITICAL | Cell size thresholds, suppression, statistician review |
| 12 | Privacy by Design | Data | CRITICAL | DPIA, data minimisation, subject rights |
| 13 | Intersectionality in Data Architecture | Data | HIGH | Cross-tabulation, multi-dimensional queries |
| 14 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 15 | Loose Coupling | Integration | HIGH | Deployment independence, no shared databases |
| 16 | Controlled Multi-Agency Data Sharing | Integration | CRITICAL | Disclosure logging, ISAs, legal basis documented |
| 17 | Performance and Efficiency | Quality | HIGH | Load testing, monitoring, targets met |
| 18 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 19 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, assistive tech testing |
| 20 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, ADRs |
| 21 | Equality Act Compliance by Design | Development | CRITICAL | Calculation validation, PSED reporting |
| 22 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 23 | Automated Testing | Development | HIGH | Test coverage, pipeline integration |
| 24 | Continuous Integration and Deployment | Development | HIGH | Pipeline exists, security scanning |
| 25 | Open Source and Reuse | Development | MEDIUM | Shared platforms evaluated, code published |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Trauma-Informed), 2 (User-Centred), 7 (Open Standards), 19 (Accessibility), 25 (Open Source) |
| Technology Code of Practice | 7 (Open Standards), 4 (Security), 22 (IaC), 25 (Open Source and Reuse) |
| NCSC Secure by Design | 4 (Security by Design), 22 (IaC), 23 (Automated Testing), 24 (CI/CD) |
| UK GDPR / DPA 2018 | 9 (Data Sovereignty), 12 (Privacy by Design), 14 (Data Quality) |
| Equality Act 2010 | 10 (Gender-Disaggregated Data), 13 (Intersectionality), 19 (Accessibility), 21 (EA Compliance) |
| Domestic Abuse Act 2021 | 1 (Trauma-Informed), 3 (Survivor Safety), 16 (Multi-Agency Sharing) |
| Public Sector Accessibility Regulations | 2 (User-Centred Design), 19 (Accessibility and Inclusion) |
| HM Treasury Green Book | 5 (Scalability), 17 (Performance), 18 (Availability), 25 (Reuse) |
| VAWG Strategy 2021 | 1 (Trauma-Informed), 3 (Survivor Safety), 16 (Multi-Agency Sharing) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| Equality Act 2010 | Legislation | legislation.gov.uk | Protected characteristics, PSED, pay gap reporting | N/A — external reference |
| Domestic Abuse Act 2021 | Legislation | legislation.gov.uk | DA definition, data protection, commissioner role | N/A — external reference |
| NCSC Secure by Design | Guidance | NCSC | Security principles for digital services | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements, special category data | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| ONS Sex and Gender Guidance | Guidance | ONS | Harmonised data collection standards | N/A — external reference |
| VAWG Strategy 2021 | Policy | Home Office | Violence against women and girls national strategy | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 5: Gender Equality — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
