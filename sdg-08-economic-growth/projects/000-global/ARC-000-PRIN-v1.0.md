# UK Government Enterprise Architecture Principles — SDG 8: Decent Work and Economic Growth

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 8: Decent Work and Economic Growth — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 8 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 8 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 8: Decent Work and Economic Growth programme. These principles apply to five UK Government digital services:

- **001** — Job Matching Platform (DWP)
- **002** — Skills Passport System (DfE)
- **003** — Labour Market Intelligence (ONS)
- **004** — Small Business Support Portal (DBT)
- **005** — Modern Slavery Reporting System (Home Office)

**Scope**: All technology projects, systems, and initiatives within the SDG 8 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Assessment Framework (CAF), UK GDPR, Data Protection Act 2018, the Public Sector Bodies Accessibility Regulations 2018, the Industrial Strategy, the Levelling Up White Paper, and the Modern Slavery Act 2015.

---

## I. Strategic Principles

### 1. User-Centred Design for Diverse Workforces

**Principle Statement**:
All systems MUST be designed around the needs of their users — jobseekers, learners, employers, small business owners, and compliance officers — with services that are simple, inclusive, and accessible regardless of digital literacy, disability, or language.

**Rationale**:
The SDG 8 programme serves an extraordinarily diverse user base. Jobseekers may include recently redundant professionals, school leavers, people with disabilities, refugees with limited English, and workers transitioning between industries. Small business owners often lack dedicated IT support. Modern slavery victims and their advocates operate in high-stress, time-critical contexts. Designing for the most complex user journeys first ensures services work for everyone. The GDS Service Standard mandates user-centred design, and the Equality Act 2010 requires reasonable adjustments.

**Implications**:

- Conduct user research with representative samples including people with low digital literacy, disabilities, limited English, and neurodivergent users
- Design for assisted digital journeys — Jobcentre Plus work coaches, business advisors, and charity workers must be able to use systems on behalf of users
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement under the Public Sector Bodies Accessibility Regulations 2018
- Support multiple languages where user need is evidenced (e.g., Welsh, BSL, common migrant languages for modern slavery reporting)
- Use plain English at a reading age appropriate for each service audience
- Design mobile-first — many jobseekers and small business owners primarily access services via smartphones

**Validation Gates**:

- [ ] User research conducted with representative sample including vulnerable and low-digital-literacy users
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Assisted digital pathway defined and tested with work coaches / business advisors
- [ ] Content reviewed for plain language and readability (reading age 9-11 for citizen-facing, 13-15 for professional-facing)
- [ ] Service assessed against GDS Service Standard points 1-3
- [ ] Mobile-first responsive design validated on common devices

---

### 2. AI Ethics and Algorithmic Fairness

**Principle Statement**:
All AI and machine learning systems MUST be designed, tested, and operated in accordance with the CDDO Data Ethics Framework, with mandatory bias testing, explainability, and human oversight for decisions that affect individuals' livelihoods.

**Rationale**:
The Job Matching Platform uses AI to recommend employment opportunities, and the Labour Market Intelligence platform uses predictive analytics to forecast skills gaps. These algorithms directly influence people's career paths and government policy. Algorithmic bias in job matching could systematically disadvantage protected groups (e.g., recommending lower-paid roles to women, or failing to match disabled candidates to suitable positions). The UK Government's approach to AI in public services requires transparency, fairness, and human accountability.

**Implications**:

- Conduct Equality Impact Assessments (EIAs) on all AI models before deployment and at regular intervals
- Implement bias detection across all nine protected characteristics under the Equality Act 2010
- Provide explainable AI outputs — users and work coaches must understand why a recommendation was made
- Maintain human-in-the-loop oversight for high-stakes decisions (e.g., benefit conditionality linked to job search activity)
- Publish algorithmic transparency records on GOV.UK as per CDDO Algorithmic Transparency Recording Standard
- Version control all training data and model parameters for auditability
- Establish an AI Ethics Board with external representation for ongoing governance

**Validation Gates**:

- [ ] Equality Impact Assessment completed and published
- [ ] Bias testing across protected characteristics documented with results
- [ ] Explainability mechanism implemented and user-tested
- [ ] Human override capability in place for all automated decisions affecting individuals
- [ ] Algorithmic Transparency Record published on GOV.UK
- [ ] Model versioning and audit trail in place
- [ ] AI Ethics Board established with terms of reference

---

### 3. Skills Data Portability and Interoperability

**Principle Statement**:
All skills, qualifications, and employment data MUST be represented using open, portable standards that enable individuals to own and share their data across systems, employers, and education providers without vendor lock-in.

**Rationale**:
The Skills Passport and Job Matching Platform must exchange data about qualifications, competencies, and work history. Currently, skills data is siloed across UCAS, Ofqual, professional bodies, and employer HR systems. The UK needs a portable, verifiable skills ecosystem aligned with the W3C Verifiable Credentials standard and the European Digital Credentials Framework to support labour mobility and lifelong learning. The Technology Code of Practice mandates open standards to avoid lock-in.

**Implications**:

- Adopt W3C Verifiable Credentials (VCs) for digital qualifications and skill badges
- Use the European Skills, Competences, Qualifications and Occupations (ESCO) taxonomy as the primary skills classification, mapped to UK SOC codes
- Implement decentralised identity standards (W3C DID) to give individuals control over their credentials
- Expose all skills data via open APIs conforming to HESA, Ofqual, and DfE data standards
- Ensure backward compatibility with existing qualification databases (Learner Records Service, Register of Regulated Qualifications)
- Support data export in machine-readable formats (JSON-LD, CBOR) for portability

**Validation Gates**:

- [ ] W3C Verifiable Credentials standard implemented for credential issuance and verification
- [ ] Skills taxonomy mapped to ESCO and UK SOC 2020 codes
- [ ] Individual data portability demonstrated (export and import across systems)
- [ ] API specifications published conforming to relevant education data standards
- [ ] No proprietary credential formats used
- [ ] Interoperability tested with at least two external credential verifiers

---

### 4. Labour Market Data Quality and Statistical Integrity

**Principle Statement**:
All systems generating or consuming labour market data MUST comply with the UK Statistics Authority Code of Practice for Statistics, ensuring data is trustworthy, high quality, and of public value.

**Rationale**:
The Labour Market Intelligence platform aggregates data from HMRC Real Time Information (RTI), ONS surveys, NOMIS, the Annual Survey of Hours and Earnings, and DWP administrative data. This data informs government policy on skills investment, regional growth, and economic planning. Poor data quality or statistical malpractice would undermine policy decisions affecting millions of workers and thousands of businesses. ONS has a statutory duty under the Statistics and Registration Service Act 2007.

**Implications**:

- Classify all statistical outputs according to the Code of Practice (National Statistics, Official Statistics, experimental statistics)
- Implement data quality scoring at point of ingestion with automated validation rules
- Maintain full data lineage from source to published output
- Apply statistical disclosure control to prevent identification of individuals or businesses
- Publish methodology statements alongside all analytical outputs
- Separate analytical outputs from political commentary — pre-release access protocols must be followed
- Design for reproducibility — all transformations must be version-controlled and replayable

**Validation Gates**:

- [ ] UK Statistics Authority Code of Practice compliance assessment completed
- [ ] Data quality scoring implemented with defined thresholds for acceptance
- [ ] End-to-end data lineage documented and queryable
- [ ] Statistical disclosure control applied and tested
- [ ] Methodology statements published for all analytical outputs
- [ ] Pre-release access protocol documented and enforced
- [ ] Reproducibility demonstrated for all published statistics

---

### 5. SME Digital Inclusion

**Principle Statement**:
All business-facing services MUST be designed to be accessible to the smallest businesses, including sole traders with no dedicated IT function, without requiring specialist software, training, or paid subscriptions.

**Rationale**:
The UK has 5.5 million SMEs, of which 4.1 million are sole traders. Many lack dedicated digital skills. The Small Business Support Portal must serve a hairdresser in Hartlepool and a tech startup in Shoreditch with equal effectiveness. The Levelling Up White Paper commits the government to closing the digital divide for businesses, and the Industrial Strategy prioritises SME productivity. Requiring complex integrations, proprietary software, or subscription services would exclude the businesses most in need of support.

**Implications**:

- Design all business interactions to be completable via a standard web browser on a smartphone
- Provide guided journeys with progressive disclosure — don't overwhelm first-time users
- Integrate with existing business tools (Companies House WebFiling, HMRC Self Assessment, MTD for VAT) via GOV.UK accounts where possible
- Offer offline-capable functionality for areas with poor connectivity
- Provide telephone and in-person support channels for businesses that cannot self-serve
- Avoid mandatory use of proprietary file formats or commercial software
- Design APIs that small businesses can use without enterprise middleware

**Validation Gates**:

- [ ] All critical journeys completable via mobile browser without app installation
- [ ] User testing conducted with sole traders and micro-businesses (1-9 employees)
- [ ] Integration with GOV.UK account and existing HMRC/Companies House services demonstrated
- [ ] Offline capability assessed and implemented where appropriate
- [ ] Non-digital channel (telephone, face-to-face) availability confirmed
- [ ] No proprietary software or paid subscription required for core functionality

---

### 6. Modern Slavery Supply Chain Transparency

**Principle Statement**:
All supply chain data and modern slavery reporting systems MUST be designed to maximise transparency, enable cross-referencing of reports, and support both proactive identification and reactive investigation of modern slavery in supply chains.

**Rationale**:
The Modern Slavery Act 2015 (section 54) requires commercial organisations with a turnover of GBP 36 million or more to publish an annual modern slavery statement. The Modern Slavery Reporting System must make these statements discoverable, comparable, and analysable. The Independent Anti-Slavery Commissioner has repeatedly highlighted that the current GOV.UK Modern Slavery Statement Registry lacks the analytical capability to identify patterns across supply chains. This principle ensures the architecture supports both compliance and active detection.

**Implications**:

- Structure modern slavery statements as machine-readable data (not just PDF uploads) using defined schemas
- Enable cross-referencing of statements with Companies House data, trade data, and known high-risk sectors/geographies
- Support anonymous tip-off and whistleblower functionality with appropriate safeguards
- Design for data sharing with law enforcement (NCA, police forces) with appropriate access controls
- Implement risk-scoring algorithms for supply chains based on sector, geography, and labour practices
- Maintain full audit trail of all statement submissions, amendments, and compliance actions
- Support multi-language input for international supply chain reporting

**Validation Gates**:

- [ ] Machine-readable statement schema defined and published
- [ ] Cross-referencing with Companies House and trade data demonstrated
- [ ] Whistleblower/tip-off channel implemented with security review
- [ ] Law enforcement data sharing gateway designed with DPIA completed
- [ ] Risk scoring methodology documented and reviewed by domain experts
- [ ] Full audit trail for all compliance actions
- [ ] Multi-language support for international reporting assessed

---

### 7. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement. Systems handling employment data, personal credentials, and modern slavery intelligence require OFFICIAL or OFFICIAL-SENSITIVE classification controls.

**Rationale**:
The SDG 8 programme handles highly sensitive data: personal employment histories, benefit conditionality records, verifiable credentials, business financial data, and modern slavery intelligence. A breach of the Modern Slavery Reporting System could endanger victims. A breach of the Job Matching Platform could expose millions of CVs and employment records. The NCSC Cyber Assessment Framework (CAF), GovAssure, and Cyber Essentials Plus are mandatory for all government systems.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit (TLS 1.3) and at rest (AES-256)
4. **Continuous Verification**: Monitor, log, and analyse all access patterns

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrator access
- [ ] Service-to-service authentication (mutual TLS or signed tokens)
- [ ] Secrets management via secure vault (never in code or configuration)
- [ ] Network segmentation with micro-segmentation for high-sensitivity zones (modern slavery intelligence)
- [ ] Encryption at rest for all data stores (AES-256 minimum)
- [ ] Encrypted transport for all network communication (TLS 1.3)
- [ ] Structured logging of all authentication/authorisation events
- [ ] Regular security testing (annual ITHC, continuous vulnerability scanning)
- [ ] GovAssure assessment completion for all in-scope systems

**Compliance Frameworks**:

- NCSC Cyber Assessment Framework (CAF)
- Cyber Essentials Plus
- GovAssure
- UK GDPR / Data Protection Act 2018
- OFFICIAL and OFFICIAL-SENSITIVE handling procedures (Government Security Classifications)

**Exceptions**: NONE. Security principles are non-negotiable. Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed by NCSC or accredited assessor
- [ ] Security controls mapped to NCSC CAF objectives
- [ ] GovAssure assessment scheduled and scoped
- [ ] Cyber Essentials Plus certification current
- [ ] Incident response plan created and tested (annual cyber exercise)

---

### 8. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load patterns.

**Rationale**:
Employment services experience significant demand variation — job searches surge during economic downturns, Universal Credit claim volumes spike after redundancy waves, and quarterly deadlines drive modern slavery statement submissions. The Job Matching Platform must handle surges when major employers announce redundancies (e.g., Tata Steel Port Talbot in 2024 affected 2,800 workers simultaneously). Skills Passport usage peaks during UCAS application season. Systems must handle both sustained growth and acute spikes without degradation.

**Implications**:

- Design for stateless components that can be replicated independently
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple availability zones within UK sovereign cloud
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics with defined upper bounds for cost control
- Capacity plan for peak scenarios (e.g., Budget Day policy announcements, mass redundancy events)

**Validation Gates**:

- [ ] System can scale horizontally without architecture change
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined with documented thresholds
- [ ] Cost model accounts for variable capacity and worst-case peak scenarios

---

### 9. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
The Job Matching Platform supports jobseekers who may have benefit conditionality requirements — failure to record job search activity could trigger sanctions, causing direct financial harm to vulnerable people. HMRC RTI data feeds are critical for real-time earnings verification. The Modern Slavery Reporting System handles time-sensitive intelligence. Resilience is not optional when system outages have direct human consequences.

**Implications**:

- Implement circuit breakers for all external dependencies (HMRC RTI, Companies House, DWP UC systems)
- Use timeouts on all network calls with sensible defaults
- Retry with exponential backoff and jitter for transient failures
- Graceful degradation when non-critical services are unavailable (e.g., recommendation engine down but job search still works)
- Automated health checks and self-healing recovery
- Bulkhead isolation to prevent cascading failures across services

**Validation Gates**:

- [ ] Failure modes identified and mitigated for all critical paths
- [ ] Fault injection or chaos engineering testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined per service
- [ ] Automated failover tested and documented
- [ ] Degraded mode behaviour documented with user-facing messaging defined

---

### 10. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The SDG 8 programme spans five departments (DWP, DfE, ONS, DBT, Home Office) and must integrate with numerous existing government systems — Universal Credit, HMRC RTI, Companies House, the Learner Records Service, NOMIS, and the Modern Slavery Statement Registry. The Technology Code of Practice mandates open standards. Cross-government interoperability reduces duplication, improves data quality, and enables joined-up services.

**Implications**:

- Use open standards for all data exchange (JSON, REST APIs, OpenAPI 3.1)
- Version all interfaces with documented backward compatibility strategy (minimum 12-month deprecation notice)
- Publish API specifications in the GOV.UK API catalogue
- Adopt GDS API technical and data standards
- Use asynchronous messaging (event-driven) for non-real-time data flows between departments
- No direct database access across system boundaries
- Implement GOV.UK Notify for citizen communications

**Validation Gates**:

- [ ] API specifications published in OpenAPI 3.1 format
- [ ] APIs registered in GOV.UK API catalogue
- [ ] Versioning strategy documented with deprecation timeline
- [ ] GDS API technical standards compliance confirmed
- [ ] No direct database coupling across system boundaries

---

## II. Data Principles

### 11. Data Sovereignty and UK Residency

**Principle Statement**:
All personal data, employment records, and modern slavery intelligence MUST reside within UK sovereign infrastructure. Cross-border data transfers require documented legal basis and DPIA approval.

**Rationale**:
Post-Brexit, the UK has its own data protection regime under the UK GDPR and Data Protection Act 2018. Employment data, benefit records, and modern slavery intelligence are classified OFFICIAL or OFFICIAL-SENSITIVE and must be hosted on platforms meeting UK Government security standards. The adequacy decision with the EU enables data flows for labour market statistics, but operational data must remain sovereign.

**Implications**:

- Host all systems on UK-sovereign cloud platforms (AWS UK regions, Azure UK regions, or Crown Hosting)
- Classify all data according to Government Security Classifications (OFFICIAL, OFFICIAL-SENSITIVE)
- Document legal basis for any cross-border data transfers (e.g., ONS statistical data sharing with Eurostat)
- Implement data residency controls preventing inadvertent storage outside UK jurisdiction
- Conduct DPIA for all data processing activities involving personal data
- Apply UK GDPR data minimisation — collect only what is necessary for the specific purpose

**Validation Gates**:

- [ ] All data hosted on UK-sovereign infrastructure confirmed
- [ ] Government Security Classification applied to all data stores
- [ ] DPIAs completed for all personal data processing
- [ ] Cross-border data transfer legal basis documented (where applicable)
- [ ] Data minimisation review completed

---

### 12. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability and troubleshooting. Employment and skills data quality directly affects individual outcomes and policy decisions.

**Rationale**:
Poor data quality in job matching leads to irrelevant recommendations, wasting jobseeker time and damaging trust. Inaccurate labour market statistics lead to misallocated skills funding. Incomplete modern slavery statements create gaps in supply chain oversight. Each system must enforce quality at source and maintain full lineage for audit.

**Quality Standards**:

- **Completeness**: No unexpected nulls in required fields; mandatory fields enforced at submission
- **Consistency**: Cross-system reconciliation between DWP, HMRC, and DfE data
- **Accuracy**: Validation rules enforced at source (e.g., NI number format, company registration number)
- **Timeliness**: Freshness SLAs defined per data domain (e.g., RTI earnings data within 3 working days)

**Validation Gates**:

- [ ] Data quality rules defined and automated for each data domain
- [ ] Lineage metadata captured from source to output
- [ ] Data contracts between producing and consuming systems documented
- [ ] Schema evolution strategy documented with backward compatibility

---

### 13. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies must be clearly labelled, read-only, and synchronised with defined freshness SLAs.

**Rationale**:
The SDG 8 programme involves multiple departments consuming shared reference data — employer records (Companies House), tax records (HMRC), qualification records (Ofqual/DfE), and benefit data (DWP). Without clear ownership, conflicting data creates reconciliation overhead and erodes user trust. For example, an employer's address must be authoritative from Companies House, not duplicated across five systems with different update frequencies.

**Authoritative Sources for SDG 8**:

| Data Domain | Authoritative Source | Consumers |
|------------|---------------------|-----------|
| Employer records | Companies House | All five projects |
| Personal tax/earnings | HMRC RTI | Job Matching, Labour Market Intelligence |
| Qualifications | Ofqual / DfE Learner Records | Skills Passport, Job Matching |
| Benefit status | DWP Universal Credit | Job Matching |
| Labour market statistics | ONS | Labour Market Intelligence, Job Matching |
| Modern slavery statements | Home Office Registry | Modern Slavery Reporting |

**Validation Gates**:

- [ ] System of record identified for each data entity
- [ ] Derived copies documented with synchronisation frequency and freshness SLA
- [ ] No bidirectional synchronisation without documented conflict resolution
- [ ] Master data management strategy for shared reference data (employer, person, location)

---

## III. Integration Principles

### 14. Universal Credit Integration First

**Principle Statement**:
The Job Matching Platform MUST integrate with Universal Credit as the primary design constraint, ensuring that job search activity, claimant commitments, and employment outcomes flow seamlessly between systems.

**Rationale**:
Approximately 6 million households claim Universal Credit. Jobseekers on UC have a Claimant Commitment that mandates job search activity. The Job Matching Platform must record activity that satisfies this commitment, and employment outcomes must flow back to UC to adjust payments. This integration is not optional — it is a core operating requirement. Failure to integrate creates dual-keying for work coaches and risks sanctions for claimants who have completed activity but whose records do not reflect it.

**Implications**:

- Design the Job Matching Platform's data model around UC Claimant Commitment categories
- Implement real-time event notifications for job applications, interviews, and outcomes
- Support work coach referral workflows with status tracking
- Handle UC consent and data sharing agreements as first-class concerns
- Plan for UC system maintenance windows and ensure graceful degradation
- Align authentication with DWP's identity verification standards (GOV.UK One Login)

**Validation Gates**:

- [ ] UC integration architecture agreed with DWP Digital
- [ ] Claimant Commitment activity recording tested end-to-end
- [ ] Work coach referral workflow demonstrated
- [ ] Consent model implemented and reviewed by DWP SIRO
- [ ] Graceful degradation during UC maintenance windows tested

---

### 15. Loose Coupling Between Departments

**Principle Statement**:
Systems MUST be loosely coupled through published APIs and asynchronous events, avoiding shared databases, file systems, or tight runtime dependencies between departmental systems.

**Rationale**:
Five departments with different release cadences, security postures, and change management processes must interoperate. Tight coupling between DWP and HMRC systems, for example, would mean that a DWP release could break HMRC data feeds. Loose coupling enables independent evolution while maintaining interoperability.

**Implications**:

- Communicate through published APIs or asynchronous event streams
- No direct database access across departmental boundaries
- Each department manages its own data lifecycle and schema evolution
- Use event-driven integration for cross-departmental data flows (e.g., employment outcome events from Job Matching to UC)
- Implement contract testing between departmental APIs
- Design for eventual consistency — accept that cross-departmental data may be minutes, not seconds, out of sync

**Validation Gates**:

- [ ] Systems communicate via APIs or events, not direct database access
- [ ] No shared mutable state between departmental systems
- [ ] Each system has independent data store and deployment pipeline
- [ ] Interface contracts version-controlled and change-managed
- [ ] Contract tests in place for all cross-departmental integrations

---

## IV. Quality Attributes

### 16. Performance Under Peak Employment Events

**Principle Statement**:
All systems MUST meet defined performance targets under expected peak load, including mass redundancy events, Budget Day policy announcements, and UCAS clearing periods.

**Rationale**:
The Job Matching Platform may receive 10x normal traffic when a major employer announces redundancies. The Skills Passport sees peak demand during UCAS application season. The Modern Slavery Reporting System experiences deadline-driven spikes at the end of financial year. Performance degradation during these events would undermine public trust and could cause direct harm (e.g., jobseekers unable to record activity for benefit conditionality).

**Performance Targets**:

- Job search response time: < 500ms (p95) under peak load
- Skills credential verification: < 2 seconds (p95) including cryptographic validation
- Labour market dashboard: < 3 seconds page load (p95) with complex visualisations
- Modern slavery statement submission: < 5 seconds (p95) including file upload
- API response time for all inter-system calls: < 200ms (p95)

**Validation Gates**:

- [ ] Performance targets defined per service with measurable SLIs
- [ ] Load testing performed at 3x expected peak capacity
- [ ] Performance monitoring continuous in production with alerting
- [ ] Capacity planning model covers worst-case scenarios

---

### 17. Availability and Reliability

**Principle Statement**:
All citizen-facing systems MUST achieve a minimum 99.9% availability (43.8 minutes downtime per month maximum). Intelligence and enforcement systems (Modern Slavery) MUST achieve 99.95%.

**Rationale**:
Jobseekers may face benefit sanctions if they cannot demonstrate job search activity due to system unavailability. Modern slavery intelligence is time-sensitive — delays could endanger victims. Business support services must be available during extended business hours.

**Availability Targets**:

| Service | Target | RTO | RPO |
|---------|--------|-----|-----|
| Job Matching Platform | 99.9% | 30 min | 5 min |
| Skills Passport | 99.9% | 1 hour | 15 min |
| Labour Market Intelligence | 99.5% | 4 hours | 1 hour |
| Small Business Support Portal | 99.9% | 1 hour | 15 min |
| Modern Slavery Reporting | 99.95% | 15 min | 1 min |

**Validation Gates**:

- [ ] Availability SLAs defined per service
- [ ] RTO and RPO requirements documented and tested
- [ ] Redundancy strategy implemented across availability zones
- [ ] Automated failover tested quarterly
- [ ] Disaster recovery procedure validated annually

---

### 18. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning. Operational dashboards must surface service health to both technical teams and senior stakeholders.

**Rationale**:
Five departments operating interconnected services need shared visibility into system health. When the Job Matching Platform reports slow response times, operators must determine whether the root cause is in their system, the HMRC RTI feed, or the Skills Passport verification endpoint. Distributed tracing across departmental boundaries is essential.

**Telemetry Requirements**:

- **Logging**: Structured JSON logs with correlation IDs spanning cross-departmental calls
- **Metrics**: RED metrics (Rate, Errors, Duration) per service endpoint
- **Tracing**: Distributed tracing with W3C Trace Context propagation across departmental boundaries
- **Dashboards**: Service-level dashboards for NOC teams plus executive summary dashboards for SROs
- **Alerting**: SLO-based alerting with actionable runbooks

**Validation Gates**:

- [ ] Logging, metrics, and tracing instrumented for all services
- [ ] Cross-departmental trace context propagation demonstrated
- [ ] Dashboards and alerts configured for each service
- [ ] SLOs and SLIs defined per service
- [ ] Runbooks created for common failure scenarios

---

## V. Development Practices

### 19. Infrastructure as Code on UK Sovereign Cloud

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines to UK sovereign cloud platforms.

**Rationale**:
Reproducible infrastructure enables disaster recovery, environment parity, and audit. UK Government systems must be hosted on approved platforms — currently AWS (London and Ireland regions), Azure (UK South and UK West), or Crown Hosting Data Centres. Infrastructure as Code ensures consistency across development, staging, and production environments.

**Validation Gates**:

- [ ] Infrastructure defined as code (Terraform, CloudFormation, or equivalent)
- [ ] Infrastructure code version-controlled in departmental repositories
- [ ] Automated deployment pipeline for infrastructure changes
- [ ] No manual infrastructure changes in production
- [ ] UK sovereign cloud hosting confirmed for all environments

---

### 20. Automated Testing Including Bias and Fairness

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment. AI/ML components MUST additionally undergo bias testing and fairness validation as part of the CI/CD pipeline.

**Rationale**:
Standard automated testing ensures functional correctness. However, for the Job Matching Platform and Labour Market Intelligence system, bias can emerge gradually as training data changes. Automated bias testing in the CI/CD pipeline catches fairness regressions before they reach production and affect real jobseekers.

**Test Requirements**:

- **Unit Tests**: Minimum 80% code coverage
- **Integration Tests**: API contract tests between departmental systems
- **End-to-End Tests**: Critical user journeys (job application, credential verification, statement submission)
- **Performance Tests**: Load testing at 3x peak capacity
- **Security Tests**: SAST, DAST, and dependency scanning
- **Bias Tests** (AI systems): Fairness metrics across protected characteristics with defined thresholds
- **Accessibility Tests**: Automated WCAG 2.2 checks in CI/CD pipeline

**Validation Gates**:

- [ ] Automated test suites exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Bias testing integrated into CI/CD for AI/ML components
- [ ] Accessibility testing automated in pipeline
- [ ] Performance tests run on every release candidate

---

### 21. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage. Deployment to production must be automated, repeatable, and auditable.

**Rationale**:
Five departments with different delivery cadences must maintain interoperability. CI/CD with contract testing ensures that a release by one department does not break another's integration. Automated deployment reduces human error and enables rapid rollback.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control (Git)
2. **Build**: Automated compilation, packaging, and container image creation
3. **Test**: Automated test execution including bias and accessibility checks
4. **Security Scan**: SAST, DAST, dependency vulnerability scanning, and secrets detection
5. **Contract Test**: API contract verification against consuming systems
6. **Deployment**: Automated deployment to staging, then production with approval gate
7. **Smoke Test**: Post-deployment verification of critical paths

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for all services
- [ ] Pipeline includes security scanning and contract testing
- [ ] Deployment is automated and repeatable with audit trail
- [ ] Rollback capability tested and documented
- [ ] Blue-green or canary deployment strategy for zero-downtime releases

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints that prevent compliance within the delivery timeline
- Regulatory or legal requirements that conflict with a principle
- Transitional state during legacy system migration
- Pilot or proof-of-concept with defined end date and scope

**Exception Request Requirements**:

- [ ] Justification with business and technical rationale
- [ ] Alternative approach and compensating controls documented
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound, maximum 12 months)
- [ ] Remediation plan to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team
2. Review by SDG 8 Architecture Review Board
3. Chief Architect approval for standard exceptions; CTO/CIO escalation for Security (Principle 7) or AI Ethics (Principle 2) exceptions
4. Document exception in project architecture documentation
5. Quarterly review of all active exceptions

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones aligned with the GDS service assessment process:

**Discovery**:

- [ ] Architecture principles understood by the delivery team
- [ ] High-level approach documented and aligned with principles
- [ ] No obvious principle violations identified

**Alpha**:

- [ ] Detailed architecture design documented
- [ ] Compliance with each principle assessed and validated
- [ ] Exceptions requested and approved where necessary
- [ ] Security and AI ethics principles validated by specialist reviewers

**Beta (Public)**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed with evidence
- [ ] GDS service assessment passed
- [ ] Operational readiness verified (monitoring, alerting, runbooks)

**Live**:

- [ ] Production system matches approved architecture
- [ ] Ongoing compliance monitoring in place
- [ ] Retrospective review scheduled for 3 months post-launch

### Enforcement

- Architecture reviews are **mandatory** for all projects across all five departments
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound (maximum 12 months) and reviewed quarterly
- The SDG 8 Architecture Review Board meets monthly to review compliance across all five projects
- Retrospective reviews for compliance on live systems conducted annually

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | User-Centred Design for Diverse Workforces | Strategic | CRITICAL | User research, accessibility audit |
| 2 | AI Ethics and Algorithmic Fairness | Strategic | CRITICAL | EIA, bias testing, transparency record |
| 3 | Skills Data Portability and Interoperability | Strategic | HIGH | VC standard compliance, data export |
| 4 | Labour Market Data Quality and Statistical Integrity | Strategic | HIGH | Code of Practice compliance, lineage |
| 5 | SME Digital Inclusion | Strategic | HIGH | Mobile testing, non-digital channels |
| 6 | Modern Slavery Supply Chain Transparency | Strategic | CRITICAL | Machine-readable schema, cross-referencing |
| 7 | Security by Design | Strategic | CRITICAL | Threat model, GovAssure, ITHC |
| 8 | Scalability and Elasticity | Strategic | HIGH | Load testing, auto-scaling |
| 9 | Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO |
| 10 | Interoperability and Open Standards | Strategic | HIGH | API specs, GOV.UK catalogue |
| 11 | Data Sovereignty and UK Residency | Data | CRITICAL | UK hosting, DPIA |
| 12 | Data Quality and Lineage | Data | HIGH | Quality scoring, lineage |
| 13 | Single Source of Truth | Data | HIGH | Authoritative sources mapped |
| 14 | Universal Credit Integration First | Integration | CRITICAL | UC integration testing |
| 15 | Loose Coupling Between Departments | Integration | HIGH | Contract testing |
| 16 | Performance Under Peak Employment Events | Quality | HIGH | Load testing at 3x peak |
| 17 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 18 | Observability and Operational Excellence | Quality | HIGH | Telemetry, dashboards |
| 19 | Infrastructure as Code on UK Sovereign Cloud | DevOps | HIGH | IaC coverage, UK hosting |
| 20 | Automated Testing Including Bias and Fairness | DevOps | HIGH | Test coverage, bias metrics |
| 21 | Continuous Integration and Deployment | DevOps | HIGH | Pipeline exists, contract tests |

---

**Document Version History**

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-28 | ArcKit AI | Initial draft |
| 1.0 | 2026-03-28 | ArcKit AI | Ratified version |

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14-point service standard | https://www.gov.uk/service-manual/service-standard |
| Technology Code of Practice | Standard | GOV.UK | Open standards, avoid lock-in | https://www.gov.uk/guidance/the-technology-code-of-practice |
| NCSC Cyber Assessment Framework | Framework | NCSC | Security objectives | https://www.ncsc.gov.uk/collection/caf |
| UK Statistics Authority Code of Practice | Standard | UKSA | Trustworthiness, quality, value | https://code.statisticsauthority.gov.uk/ |
| Modern Slavery Act 2015 | Legislation | UK Parliament | Section 54 transparency | https://www.legislation.gov.uk/ukpga/2015/30 |
| Industrial Strategy | Policy | DBT | SME productivity, skills | https://www.gov.uk/government/publications/industrial-strategy |
| W3C Verifiable Credentials | Standard | W3C | Digital credential interoperability | https://www.w3.org/TR/vc-data-model-2.0/ |
| CDDO Algorithmic Transparency Standard | Standard | CDDO | AI transparency recording | https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 8: Decent Work and Economic Growth
**Model**: Claude Opus 4.6
