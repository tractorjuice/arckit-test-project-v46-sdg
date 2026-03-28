# UK Government Enterprise Architecture Principles — SDG 12: Responsible Consumption and Production

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 12: Responsible Consumption and Production — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 12 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 12 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 12: Responsible Consumption and Production programme. These principles apply to four UK Government digital services:

- **001** — Carbon Footprint Calculator (DESNZ)
- **002** — Circular Economy Marketplace (DEFRA)
- **003** — Waste Management Analytics (DEFRA)
- **004** — Sustainable Procurement Portal (Crown Commercial Service)

**Scope**: All technology projects, systems, and initiatives within the SDG 12 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, Environment Act 2021, Net Zero Strategy, Resources and Waste Strategy, GHG Protocol Corporate Standard, PPN 06/20 (Social Value), and PPN 06/21 (Carbon Reduction Plans).

---

## I. Strategic Principles

### 1. User-Centred Design for Environmental Action

**Principle Statement**:
All systems MUST be designed around the needs of end users — from procurement officers calculating carbon footprints to waste operators logging transfer notes — with services that are simple, inclusive, and reduce barriers to sustainable behaviour.

**Rationale**:
Environmental compliance and sustainability reporting are complex domains. Users include SME manufacturers unfamiliar with Scope 1/2/3 emissions accounting, local authority waste teams using disparate legacy systems, and procurement officers navigating PPN 06/21 carbon reduction plans. If digital tools are difficult to use, organisations default to non-compliance or manual workarounds that produce unreliable data. The GDS Service Standard mandates user-centred design, and the environmental urgency demands services that make the sustainable choice the easy choice.

**Implications**:

- Conduct user research with representative users across the supply chain, including SMEs with limited environmental expertise
- Design guided workflows that translate complex environmental standards (GHG Protocol, waste hierarchy) into actionable steps
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement
- Provide contextual help explaining environmental terminology (Scope 1/2/3 emissions, embodied carbon, waste transfer duty of care)
- Support multiple channels — not all waste operators or small suppliers can self-serve online
- Provide calculators and estimation tools so users without specialist knowledge can produce compliant outputs

**Validation Gates**:

- [ ] User research conducted with representative users including SMEs and non-specialist environmental users
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Environmental terminology guidance embedded in user journeys
- [ ] Guided workflows tested for usability by non-specialist users
- [ ] Service assessed against GDS Service Standard points 1-3

---

### 2. GHG Protocol Compliance by Design

**Principle Statement**:
All systems that calculate, report, or compare greenhouse gas emissions MUST implement the GHG Protocol Corporate Standard methodology, ensuring consistent Scope 1, Scope 2, and Scope 3 emissions accounting across all services in the programme.

**Rationale**:
The GHG Protocol is the internationally recognised standard for corporate emissions accounting and is mandated by PPN 06/21 for suppliers to the Crown. Inconsistent calculation methodologies across the four SDG 12 services would produce incomparable data, undermine procurement decisions, and erode confidence in government reporting to the UNFCCC and COP commitments. A shared calculation methodology is the foundation of credible environmental governance.

**Implications**:

- Implement Scope 1 (direct emissions), Scope 2 (energy indirect), and Scope 3 (value chain) categorisation in all carbon-related data models
- Use BEIS/DESNZ UK Government GHG Conversion Factors as the authoritative emissions factor source, updated annually
- Support both location-based and market-based Scope 2 accounting methods
- Maintain auditable calculation chains from raw activity data to reported tCO2e figures
- Align reporting boundaries with GHG Protocol organisational and operational boundary definitions
- Provide transparent uncertainty quantification for Scope 3 estimates

**Validation Gates**:

- [ ] Calculation engine validated against GHG Protocol Corporate Standard requirements
- [ ] BEIS/DESNZ conversion factors integrated with annual update mechanism
- [ ] Both location-based and market-based Scope 2 methods supported
- [ ] Calculation audit trail from activity data to tCO2e output is complete and queryable
- [ ] Scope 3 estimation methodology documented with uncertainty ranges

---

### 3. Circular Economy First

**Principle Statement**:
All systems MUST be designed to promote and enable circular economy outcomes — prioritising waste prevention, reuse, repair, and remanufacturing over recycling and disposal, consistent with the waste hierarchy defined in the Environment Act 2021.

**Rationale**:
The UK Resources and Waste Strategy (2018) and Environment Act 2021 establish the waste hierarchy (prevention > reuse > recycling > recovery > disposal) as the guiding framework for UK waste and resource policy. Digital services in this programme must embed this hierarchy in their logic, algorithms, and decision support — not merely present data. The Circular Economy Marketplace (Project 002) and Waste Management Analytics (Project 003) must actively drive materials up the waste hierarchy rather than passively tracking disposal.

**Implications**:

- Material matching algorithms MUST prioritise reuse and remanufacturing pathways before recycling
- Waste classification MUST use European Waste Catalogue (EWC) codes with extensions for circular economy readiness assessment
- Decision support tools MUST present options ordered by waste hierarchy position
- Analytics MUST track circular economy metrics (material circularity indicator, reuse rates, waste prevention rates) alongside traditional tonnage metrics
- Product and material data models MUST support lifecycle attributes (durability, reparability, recyclability, recycled content percentage)

**Validation Gates**:

- [ ] Waste hierarchy logic embedded in all material/waste routing decisions
- [ ] EWC classification implemented with circular economy extensions
- [ ] Material matching algorithms demonstrably prioritise higher-hierarchy outcomes
- [ ] Circular economy metrics defined and tracked alongside weight-based metrics
- [ ] Product lifecycle attributes captured in data model

---

### 4. Supply Chain Transparency

**Principle Statement**:
All systems MUST support end-to-end supply chain transparency for environmental impact data, enabling traceability from raw material extraction through manufacturing, distribution, use, and end-of-life management.

**Rationale**:
Scope 3 emissions (supply chain) typically represent 80-90% of an organisation's total carbon footprint. PPN 06/21 requires suppliers to publish Carbon Reduction Plans covering their supply chains. Without supply chain transparency, carbon footprint calculations are estimates at best and greenwashing at worst. The Environment Act 2021 introduces extended producer responsibility (EPR) requiring producers to track materials through the full lifecycle. Supply chain transparency is both an environmental imperative and a regulatory requirement.

**Implications**:

- Data models MUST support multi-tier supply chain data (Tier 1 direct suppliers through to raw material origin)
- Systems MUST provide mechanisms for suppliers to contribute environmental data without exposing commercially sensitive information
- Support progressive disclosure — basic data from all suppliers, detailed data from high-impact suppliers
- Implement data quality scoring for supply chain environmental data (measured vs estimated vs industry average)
- Enable aggregation and anonymisation for sector-level reporting without revealing individual supplier data
- Align with emerging UK and EU digital product passport requirements

**Validation Gates**:

- [ ] Multi-tier supply chain data model implemented
- [ ] Supplier data contribution mechanism protects commercial sensitivity
- [ ] Data quality scoring distinguishes measured, estimated, and average data
- [ ] Aggregation and anonymisation tested for sector-level reporting
- [ ] Alignment with digital product passport standards assessed

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one.

**Rationale**:
These systems handle commercially sensitive environmental data — supplier carbon footprints, waste composition data, procurement decisions, and supply chain information. A breach would expose competitive intelligence, enable greenwashing through data manipulation, and undermine public trust in government environmental reporting. Environmental data integrity is essential for credible climate action. NCSC guidance, UK GDPR, and the Secure by Design framework mandate proactive security.

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
- [ ] Encryption at rest for all data stores containing commercial or personal data
- [ ] Encrypted transport for all network communication (no exceptions)
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning, dependency auditing)
- [ ] Environmental data integrity controls (hash chains, digital signatures) to prevent tampering with emissions and waste data

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed and reviewed for each service
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] Security testing plan defined and executed before go-live
- [ ] Incident response runbook created with defined escalation paths
- [ ] Environmental data integrity controls verified through tamper-detection testing

---

### 6. Observability and Environmental Metrics Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time operational monitoring and MUST additionally instrument environmental performance metrics as first-class observability signals.

**Rationale**:
We cannot govern what we cannot measure. These services exist to measure, report, and reduce environmental impact. Operational observability ensures service reliability; environmental observability ensures the programme delivers on its SDG 12 commitments. Carbon intensity per transaction, waste diversion rates, and circular economy throughput are as important as p95 latency.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end request tracing
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, saturation
- **Tracing**: Distributed trace context propagated across all service boundaries
- **Alerting**: SLO-based alerting with actionable runbooks linked to each alert
- **Environmental Metrics**: Carbon intensity per calculation, waste tonnes processed per period, material match success rate, procurement sustainability score distribution

**Required Instrumentation**:

- Request volume, latency distribution, error rate per endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (calculations performed, materials matched, waste notes processed, procurement assessments completed)
- Environmental metrics (total tCO2e calculated, waste hierarchy distribution, material circularity rates)
- Security events (authentication failures, policy violations, suspicious patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 2 years (aligned with UK Government retention standards)
- **Application logs**: 90 days minimum for troubleshooting
- **Environmental reporting data**: 7 years minimum (aligned with Environment Act reporting obligations)
- **Metrics**: 2 years with progressive aggregation for trend analysis

**Validation Gates**:

- [ ] Logging, metrics, and tracing instrumented for all services
- [ ] Environmental performance dashboards configured alongside operational dashboards
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for all alerting scenarios
- [ ] Environmental reporting data retention meets statutory requirements

---

## II. Data Principles

### 7. Data Sovereignty and Environmental Data Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, the Environment Act 2021 reporting requirements, and departmental data governance policies.

**Rationale**:
These services process a combination of personal data (supplier contact details, procurement officer identities), commercially sensitive data (supplier carbon footprints, waste composition, supply chain structures), and public interest environmental data (national emissions inventories, waste statistics). Environmental data has dual obligations: commercial sensitivity for individual organisations and transparency requirements for public accountability. Data governance must balance these competing demands.

**Data Classification Tiers**:

1. **OFFICIAL**: Published environmental data, aggregated statistics, public reporting
2. **OFFICIAL-SENSITIVE (Commercial)**: Individual supplier carbon footprints, waste composition data, supply chain structures, procurement scoring
3. **OFFICIAL-SENSITIVE (Personal)**: Contact details, user accounts, supplier representative information

**Data Residency**:

- All data MUST reside within UK sovereign data centres
- No transfer of personal or commercially sensitive data outside the UK without lawful basis
- Environmental reporting data intended for international frameworks (UNFCCC, SDG reporting) may be shared in aggregated, anonymised form

**Data Retention**:

- Environmental reporting data: 7 years minimum (Environment Act 2021 compliance)
- Waste transfer notes: 3 years minimum (duty of care regulations)
- Carbon calculation audit trails: 7 years (aligned with financial audit requirements)
- Personal data: Retention periods defined per purpose, with automatic deletion or anonymisation
- Aggregated statistics: Indefinite retention for trend analysis and policy evaluation

**Validation Gates**:

- [ ] Data classification performed for all data stores and data flows
- [ ] UK residency confirmed for all data storage and processing
- [ ] Retention policies configured with automated deletion or anonymisation
- [ ] Environmental data retention meets Environment Act statutory requirements
- [ ] Data sharing agreements in place for all cross-departmental data flows

---

### 8. Privacy by Design with Environmental Transparency

**Principle Statement**:
All systems MUST embed privacy protections from the outset while simultaneously supporting the public transparency obligations of environmental reporting — balancing individual data protection with the collective right to environmental information.

**Rationale**:
UK GDPR Article 25 mandates data protection by design and by default. However, the Environmental Information Regulations 2004 (EIR) create a presumption of disclosure for environmental information held by public authorities. The architecture must resolve this tension: protecting commercial confidentiality and personal data while enabling public access to aggregated environmental performance data. The Aarhus Convention (ratified by the UK) enshrines the public's right to environmental information.

**Implications**:

- Collect only the minimum personal data required for each purpose (data minimisation)
- Separate personally identifiable data from environmental performance data at the architecture level
- Implement aggregation and anonymisation pipelines that produce publishable environmental statistics without revealing individual supplier data
- Support Environmental Information Regulations requests through pre-prepared anonymised datasets
- Provide clear privacy notices explaining what data is collected, why, and the basis for any environmental transparency disclosures
- Support data subject rights: access, rectification, erasure, portability, and objection

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service
- [ ] Architectural separation between personal/commercial data and publishable environmental data
- [ ] Anonymisation pipeline tested — individual suppliers not identifiable from published data
- [ ] EIR disclosure readiness assessed
- [ ] Privacy notices published in plain language

---

### 9. Environmental Data Quality and Lineage

**Principle Statement**:
Environmental data pipelines MUST maintain auditable data quality standards and provide end-to-end lineage from raw activity data to reported environmental metrics.

**Rationale**:
Environmental decisions — procurement exclusions based on carbon scores, waste enforcement actions, national emissions reporting — have significant economic and regulatory consequences. Poor data quality leads to wrong decisions: a supplier unfairly excluded from procurement or a recycling facility incorrectly rated. Emissions data reported to UNFCCC and used in UK Climate Change Act progress reports must be defensible. Lineage enables accountability when figures are challenged by industry, NGOs, or international bodies.

**Quality Standards**:

- **Completeness**: All mandatory emissions scopes and waste categories populated; gaps flagged with estimation method used
- **Consistency**: Cross-system reconciliation between carbon calculator, procurement portal, and waste analytics
- **Accuracy**: Emissions factors validated against BEIS/DESNZ published values; waste weights validated against weighbridge data where available
- **Timeliness**: Freshness SLAs defined per data flow — real-time for waste tracking, quarterly for carbon reporting
- **Provenance**: Every data point tagged with source (measured, estimated, industry average) and confidence level

**Lineage Requirements**:

- Source-to-target mapping documented for all environmental data flows
- Emissions calculation chains fully auditable (activity data x emissions factor = tCO2e)
- Data quality metrics tracked per pipeline with alerting on degradation
- Impact analysis capability for emissions factor updates (what changes when BEIS updates conversion factors?)

**Validation Gates**:

- [ ] Data quality rules defined and automated with monitoring
- [ ] Emissions calculation lineage fully auditable from activity data to tCO2e
- [ ] Data provenance tagging (measured/estimated/average) implemented
- [ ] Emissions factor update impact analysis capability tested
- [ ] Data contracts defined between SDG 12 services

---

### 10. Single Source of Truth for Environmental Reference Data

**Principle Statement**:
Every environmental data domain MUST have a single authoritative source. Derived copies MUST be clearly labelled with source and freshness. Critical reference data — emissions factors, waste classification codes, material properties — MUST be managed centrally across all four services.

**Rationale**:
If the Carbon Footprint Calculator uses different emissions factors than the Sustainable Procurement Portal, procurement decisions will be inconsistent with reported footprints. If Waste Management Analytics uses different EWC classifications than the Circular Economy Marketplace, materials cannot be matched accurately. Shared environmental reference data must have a single, versioned, authoritative source.

**Implications**:

- BEIS/DESNZ GHG Conversion Factors managed as a single versioned dataset consumed by all services
- European Waste Catalogue (EWC) codes maintained as a shared classification with circular economy extensions
- Material properties database (recyclability, embodied carbon, hazardousness) managed centrally
- Supplier environmental profiles stored once and referenced by both Carbon Footprint Calculator and Procurement Portal
- Cross-service data synchronisation with documented lag tolerances and version tracking

**Validation Gates**:

- [ ] Single authoritative source identified for each environmental reference dataset
- [ ] Emissions factors, waste codes, and material properties managed centrally with versioning
- [ ] All four services consume shared reference data from the same source
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No contradictory environmental data across services

---

## III. Integration Principles

### 11. Loose Coupling Across Departmental Boundaries

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, shared file systems, or tight runtime dependencies — especially critical given that the four services span DESNZ, DEFRA, and Crown Commercial Service.

**Rationale**:
The SDG 12 programme spans three departments with different governance structures, technology stacks, and release cadences. Each team must be able to develop, deploy, and evolve their service independently. DESNZ's Carbon Footprint Calculator and DEFRA's Waste Management Analytics serve different user communities with different operational rhythms. Tight coupling between services creates cross-departmental coordination overhead that would cripple delivery.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each service manages its own data lifecycle and data store
- Environmental reference data shared through a managed data service, not direct database access
- Interface contracts owned by the producing team with consumer input on design
- Avoid distributed transactions across departmental boundaries; use compensating actions or sagas

**Validation Gates**:

- [ ] All inter-service communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across departmental boundaries
- [ ] Each service has its own independent data store
- [ ] Deployment of one service does not require simultaneous deployment of another
- [ ] Interface changes versioned with backward compatibility guarantees

---

### 12. Event-Driven Environmental Data Flows

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for environmental data exchange to improve resilience, enable real-time waste tracking, and support audit trail requirements.

**Rationale**:
Environmental data flows are inherently event-driven: a waste transfer occurs, a carbon calculation is completed, a material becomes available for reuse, a procurement assessment is scored. Event-driven patterns capture the temporal dimension essential for environmental auditing (when did this waste leave the producer? when was it received by the recycler?). They also enable the Circular Economy Marketplace to react in near-real-time to newly available materials.

**When to Use Asynchronous Patterns**:

- Waste transfer notifications between producers and receivers
- Material availability alerts for the Circular Economy Marketplace
- Carbon calculation completion events triggering procurement score updates
- Cross-departmental data sharing (DESNZ to DEFRA, DEFRA to CCS)
- Audit trail events and compliance logging

**When Synchronous Communication is Acceptable**:

- Real-time carbon calculation during user sessions
- Procurement decision support queries requiring immediate response
- User authentication and authorisation checks

**Validation Gates**:

- [ ] Asynchronous patterns used for cross-service environmental data flows
- [ ] Message durability and delivery guarantees defined (at-least-once for environmental events)
- [ ] Event schemas versioned and published in a shared schema registry
- [ ] Dead letter handling and error recovery procedures defined
- [ ] Event replay capability available for audit reconstruction and data recovery

---

## IV. Quality Attributes

### 13. Performance and Resource Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected and peak load with efficient use of computational resources — and SHOULD minimise their own environmental footprint through green software practices.

**Rationale**:
It would be ironic for sustainability-focused services to have an excessive computational carbon footprint. Beyond standard performance requirements, these services should demonstrate green software engineering: right-sizing infrastructure, using carbon-aware computing where available, and avoiding wasteful over-provisioning. Users include procurement officers working to deadlines and waste operators in the field — slow systems waste their time and may cause them to bypass digital processes.

**Performance Targets** (to be defined per service):

- **Response Time**: p95 latency targets appropriate to the user journey (< 2 seconds for page loads, < 5 seconds for complex carbon calculations)
- **Throughput**: Transactions per second at expected and peak load (waste tracking may spike at month-end reporting)
- **Resource Efficiency**: Utilisation targets that balance responsiveness with computational carbon footprint

**Green Software Implications**:

- Right-size infrastructure to avoid idle resource waste
- Implement auto-scaling to match demand patterns (scale down during off-peak)
- Consider carbon intensity of compute regions when selecting deployment locations
- Optimise data processing pipelines to minimise unnecessary computation
- Cache frequently-accessed reference data (emissions factors, waste codes) to reduce repeated lookups

**Validation Gates**:

- [ ] Performance requirements defined with measurable targets per service
- [ ] Load testing performed at expected and peak capacity
- [ ] Infrastructure right-sizing reviewed — no persistent over-provisioning
- [ ] Green software practices documented and measured

---

### 14. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss, with targets reflecting the regulatory and operational criticality of each service.

**Rationale**:
Waste Management Analytics and the Circular Economy Marketplace have operational dependencies — waste cannot be held indefinitely, and materials available for reuse have time-limited value. The Carbon Footprint Calculator and Procurement Portal have regulatory reporting deadlines. Availability targets must reflect these operational realities.

**Availability Targets** (to be defined per service based on criticality):

- **Waste Management Analytics**: 99.9% (8.7 hours downtime per year) — operational waste tracking is time-critical
- **Circular Economy Marketplace**: 99.9% — material matching has time-limited value
- **Carbon Footprint Calculator**: 99.5% — calculation can tolerate planned maintenance windows
- **Sustainable Procurement Portal**: 99.5% — procurement cycles have defined submission windows

**High Availability Patterns**:

- Redundancy across multiple availability zones
- Automated health checks with self-healing recovery
- Regular disaster recovery testing (at least annually, quarterly for critical services)

**Validation Gates**:

- [ ] Availability SLA defined per service based on operational criticality
- [ ] RTO and RPO requirements documented and achievable
- [ ] Redundancy strategy implemented and tested
- [ ] Failover tested regularly with documented results
- [ ] Backup and restore procedures validated

---

### 15. Maintainability and Policy Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns enabling rapid adaptation to evolving environmental regulations, emissions factors, waste classification changes, and procurement policy updates.

**Rationale**:
Environmental policy evolves rapidly. BEIS/DESNZ updates GHG Conversion Factors annually. The Environment Act 2021 introduces new extended producer responsibility schemes over multiple years. PPN requirements are updated periodically. The UK Emissions Trading Scheme scope may expand. Systems that hard-code policy rules require expensive rework for each change. Externalised, configurable policy engines are essential.

**Implications**:

- Emissions factors externalised as configurable data, not hard-coded in calculation logic
- Waste classification rules managed as versioned configuration, not embedded in code
- Procurement scoring criteria (PPN 06/21 thresholds, social value weightings) configurable without code deployment
- Business rule engines or configuration-driven approaches for policy logic
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to validate policy changes do not break existing calculations

**Validation Gates**:

- [ ] Emissions factors updateable without code deployment
- [ ] Waste classification changes achievable through configuration
- [ ] Procurement scoring criteria configurable by policy teams
- [ ] Automated regression tests validate existing calculations after policy updates
- [ ] Architecture Decision Records document key choices

---

### 16. Accessibility and Inclusion

**Principle Statement**:
All citizen-facing and business-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be usable by the widest possible range of users, including SME operators, local authority staff, and field-based waste operatives.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Users of these services include waste operatives working in the field on mobile devices, SME manufacturers with varying digital literacy, local authority staff using assistive technologies, and procurement officers across hundreds of public bodies. Environmental compliance should not be limited by digital accessibility barriers.

**Implications**:

- Design using progressive enhancement — core functionality works without client-side scripting
- Test with assistive technologies (screen readers, voice control, switch access)
- Ensure waste tracking interfaces work on mobile devices in field conditions (variable connectivity, outdoor lighting)
- Provide offline capability for waste transfer note capture in low-connectivity environments
- Publish an accessibility statement for each service

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Mobile field use tested for waste tracking interfaces
- [ ] Accessibility statement published and maintained
- [ ] Offline capability tested for field-based operations

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines. Manual changes to production infrastructure are prohibited.

**Rationale**:
Manual infrastructure changes create configuration drift, inconsistency between environments, and undocumented state. Infrastructure as Code enables repeatability, auditability, and disaster recovery — all critical for government services handling regulated environmental data. Reproducible environments also enable consistent performance testing for emissions calculations.

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

### 18. Automated Testing with Environmental Validation

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment, with specific emphasis on environmental calculation accuracy and regulatory compliance validation.

**Rationale**:
An error in the carbon calculation engine that produces incorrect tCO2e figures could lead to flawed procurement decisions, inaccurate national emissions reporting, and loss of credibility in UK climate commitments. Waste classification errors could route hazardous materials to inappropriate facilities. Environmental calculation accuracy requires the same rigour as financial calculation accuracy in banking systems.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests) — including emissions factor application and waste classification logic
- **Integration Tests**: Test component interactions and data flows (15-20% of tests) — including cross-service environmental data exchange
- **End-to-End Tests**: Critical user journeys and cross-service flows (5-10% of tests)

**Required Test Types**:

- Functional tests (does it produce correct environmental outcomes?)
- Environmental calculation validation (verified against known-good calculation examples from GHG Protocol guidance)
- Accessibility tests (automated WCAG checks as part of the pipeline)
- Performance tests (do complex multi-scope carbon calculations meet latency targets?)
- Security tests (dependency scanning, static analysis, environmental data integrity)
- Regression tests for emissions factor updates (do existing calculations produce updated results with new factors?)

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Emissions calculation tests validated against GHG Protocol reference examples
- [ ] Waste classification tests cover all EWC code categories
- [ ] Critical user journeys have end-to-end tests
- [ ] Performance and security tests run regularly in the pipeline

---

### 19. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
Frequent, small, automated deployments reduce risk compared to large, infrequent, manual releases. Quality gates ensure that only code meeting defined standards reaches production. This enables rapid response to emissions factor updates, regulatory changes, and security vulnerabilities.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation, packaging, and artifact creation
3. **Test**: Automated test execution (unit, integration, environmental calculation, accessibility, security)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secrets detection
5. **Deployment**: Automated deployment to environments with progressive rollout

**Quality Gates**:

- All automated tests must pass (including environmental calculation validation)
- No critical or high security vulnerabilities
- Peer review approval required
- Accessibility checks passed
- Production deployment requires documented change approval

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for each service
- [ ] Pipeline includes environmental calculation validation, security scanning, and accessibility checks
- [ ] Deployment is automated and repeatable across all environments
- [ ] Rollback capability tested and documented

---

### 20. Open Source, Open Data, and Reuse

**Principle Statement**:
Teams SHOULD use existing open source solutions and government shared platforms where they meet requirements, SHOULD publish their own code as open source, and MUST publish environmental datasets as open data where they meet the criteria for public interest disclosure.

**Rationale**:
The Technology Code of Practice requires government teams to make source code open where possible. The Open Data White Paper and the Environmental Information Regulations 2004 create obligations to publish environmental data. Open emissions factors, waste classification data, and aggregated environmental metrics enable third-party innovation, academic research, and public scrutiny of government environmental commitments.

**Implications**:

- Evaluate existing government shared platforms before building bespoke (GOV.UK Notify, GOV.UK Pay, GOV.UK Forms)
- Use established open source components where they meet requirements
- Publish source code openly unless it contains security-sensitive logic
- Publish aggregated environmental datasets as open data on data.gov.uk
- Publish emissions factor methodologies and calculation documentation openly
- Maintain a register of third-party dependencies with licence compliance tracking

**Validation Gates**:

- [ ] Government shared platforms evaluated before building bespoke
- [ ] Environmental datasets identified for open data publication
- [ ] Source code published openly or justification documented
- [ ] Emissions calculation methodology published for peer review
- [ ] Third-party dependency register maintained with licence compliance

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
- [ ] Environmental impact assessment if the exception affects sustainability outcomes
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to Security by Design (Principle 5) or GHG Protocol Compliance (Principle 2)
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
- [ ] Environmental data model and GHG Protocol alignment assessed (Principles 2, 9)
- [ ] Data classification and privacy approach defined (Principles 7, 8)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed (Principle 5)
- [ ] Environmental calculation engine validated against GHG Protocol (Principle 2)
- [ ] Accessibility approach validated (Principle 16)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed with no unresolved critical or high findings
- [ ] Environmental data quality and lineage verified end-to-end

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
| 1 | User-Centred Design for Environmental Action | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 2 | GHG Protocol Compliance by Design | Strategic | CRITICAL | Calculation validation, BEIS factors, audit trail |
| 3 | Circular Economy First | Strategic | HIGH | Waste hierarchy logic, material matching, EWC codes |
| 4 | Supply Chain Transparency | Strategic | HIGH | Multi-tier data model, provenance tagging |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, data integrity |
| 6 | Observability and Environmental Metrics | Strategic | HIGH | Dashboards, SLOs, environmental metrics instrumented |
| 7 | Data Sovereignty and Environmental Governance | Data | CRITICAL | UK residency, classification, statutory retention |
| 8 | Privacy by Design with Environmental Transparency | Data | CRITICAL | DPIA, anonymisation, EIR readiness |
| 9 | Environmental Data Quality and Lineage | Data | HIGH | Calculation lineage, provenance, quality metrics |
| 10 | Single Source of Truth for Environmental Reference Data | Data | HIGH | Shared emissions factors, waste codes, material properties |
| 11 | Loose Coupling Across Departmental Boundaries | Integration | HIGH | Deployment independence, no shared databases |
| 12 | Event-Driven Environmental Data Flows | Integration | MEDIUM | Async patterns for cross-service flows |
| 13 | Performance and Resource Efficiency | Quality | HIGH | Load testing, green software practices |
| 14 | Availability and Reliability | Quality | CRITICAL | SLA monitoring, DR testing |
| 15 | Maintainability and Policy Evolvability | Quality | HIGH | Configurable policy rules, ADRs |
| 16 | Accessibility and Inclusion | Quality | CRITICAL | WCAG 2.2 AA, mobile field testing |
| 17 | Infrastructure as Code | Development | HIGH | IaC coverage, no manual changes |
| 18 | Automated Testing with Environmental Validation | Development | HIGH | Calculation validation, test coverage |
| 19 | Continuous Integration and Deployment | Development | HIGH | Pipeline with environmental checks |
| 20 | Open Source, Open Data, and Reuse | Development | MEDIUM | Open data publication, shared platforms |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (User-Centred Design), 4 (Supply Chain Transparency), 16 (Accessibility), 20 (Open Source/Data) |
| Technology Code of Practice | 4 (Transparency), 5 (Security), 11 (Loose Coupling), 17 (IaC), 20 (Reuse) |
| NCSC Secure by Design | 5 (Security by Design), 17 (IaC), 18 (Automated Testing), 19 (CI/CD) |
| UK GDPR / DPA 2018 | 7 (Data Sovereignty), 8 (Privacy by Design), 9 (Data Quality) |
| Environment Act 2021 | 2 (GHG Protocol), 3 (Circular Economy), 7 (Retention), 9 (Data Quality) |
| Net Zero Strategy | 2 (GHG Protocol), 4 (Supply Chain), 6 (Environmental Metrics), 13 (Green Software) |
| Resources and Waste Strategy | 3 (Circular Economy First), 10 (Shared Reference Data), 12 (Event-Driven Flows) |
| PPN 06/21 Carbon Reduction Plans | 2 (GHG Protocol), 4 (Supply Chain Transparency), 9 (Data Quality) |
| PPN 06/20 Social Value | 4 (Supply Chain Transparency), 20 (Open Data) |
| GHG Protocol Corporate Standard | 2 (GHG Protocol Compliance), 9 (Data Quality and Lineage), 10 (Reference Data) |
| Public Sector Accessibility Regulations | 1 (User-Centred Design), 16 (Accessibility and Inclusion) |
| HM Treasury Green Book | 13 (Performance), 14 (Availability), 15 (Maintainability), 20 (Reuse) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| Environment Act 2021 | Legislation | legislation.gov.uk | Waste hierarchy, EPR, environmental reporting | N/A — external reference |
| Net Zero Strategy | Policy | GOV.UK | National decarbonisation pathway | N/A — external reference |
| Resources and Waste Strategy | Policy | GOV.UK | Circular economy, waste reduction targets | N/A — external reference |
| GHG Protocol Corporate Standard | Standard | ghgprotocol.org | Scope 1/2/3 accounting methodology | N/A — external reference |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plan requirements for suppliers | N/A — external reference |
| PPN 06/20 | Procurement Note | GOV.UK | Social Value in procurement | N/A — external reference |
| BEIS/DESNZ GHG Conversion Factors | Data | GOV.UK | Annual emissions factors for UK reporting | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| Environmental Information Regulations 2004 | Legislation | legislation.gov.uk | Public right to environmental information | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 12: Responsible Consumption and Production — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
