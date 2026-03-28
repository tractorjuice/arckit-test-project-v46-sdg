# UK Government Enterprise Architecture Principles — SDG 17: Partnerships for the Goals

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 17: Partnerships for the Goals — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 17 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 17 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 17: Partnerships for the Goals programme. These principles apply to four UK Government digital services:

- **001** — International Aid Tracking (FCDO)
- **002** — Cross-Government Data Sharing Platform (Cabinet Office)
- **003** — SDG Progress Dashboard (ONS)
- **004** — Global Britain Trade Platform (DBT)

**Scope**: All technology projects, systems, and initiatives within the SDG 17 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Assessment Framework (CAF), UK GDPR, Data Protection Act 2018, the International Development Act 2002, the Official Statistics Code of Practice (UKSA), IATI data standard, OECD DAC statistical reporting directives, and WTO trade data standards.

---

## I. Strategic Principles

### 1. International Interoperability by Default

**Principle Statement**:
All systems MUST be designed to interoperate with international standards, data formats, and partner country systems, ensuring the UK can fulfil its global reporting obligations and support multilateral partnerships.

**Rationale**:
The SDG 17 programme spans international development, cross-government data exchange, statistical reporting, and global trade. Each domain operates within international frameworks — IATI for aid transparency, the UN SDG indicator framework for progress monitoring, WTO data standards for trade, and OECD DAC reporting for ODA. Systems that cannot interoperate with these frameworks undermine the UK's ability to meet treaty obligations, share data with partner nations, and report credibly to international bodies.

**Implications**:

- Adopt IATI data standard for all ODA financial flows and activity reporting
- Implement OECD DAC CRS++ (Creditor Reporting System) purpose codes for aid classification
- Support UN SDG indicator metadata standards (SDMX for statistical exchange)
- Publish trade data using WTO Integrated Trade Intelligence Portal (I-TIP) compatible formats
- Design APIs that accommodate partner country systems with varying levels of technical maturity
- Provide data in multiple languages where required by international agreements

**Validation Gates**:

- [ ] IATI compliance validated against the IATI Standard v2.03+
- [ ] DAC CRS++ codes implemented for all ODA classification
- [ ] SDMX-compliant statistical data exchange demonstrated
- [ ] API specifications published in OpenAPI 3.0 with international partner authentication
- [ ] Multi-language support assessed and implemented where treaty-required
- [ ] Interoperability tested with at least two partner country systems

---

### 2. Statistical Independence and Integrity

**Principle Statement**:
All statistical systems MUST preserve the independence of the UK Statistics Authority (UKSA) and comply with the Code of Practice for Statistics, ensuring that data collection, processing, and publication are free from political interference.

**Rationale**:
The ONS SDG Progress Dashboard and related statistical outputs are subject to the Statistics and Registration Service Act 2007. The Code of Practice for Statistics (Trustworthiness, Quality, and Value) requires that statistical production is separated from policy influence. Architecture decisions must enforce this separation technically, not merely procedurally, to maintain the UK's international credibility in SDG reporting.

**Implications**:

- Enforce role-based access control separating statistical production from policy teams
- Implement pre-release access controls compliant with UKSA pre-release access rules
- Provide tamper-evident audit trails for all data transformations from source to published statistic
- Design publication pipelines that cannot be interrupted or altered by non-statistical staff
- Support reproducibility — any published statistic must be reproducible from source data and documented methodology

**Validation Gates**:

- [ ] UKSA Code of Practice compliance assessment completed
- [ ] Pre-release access controls technically enforced (not just policy-based)
- [ ] Audit trail covers full data lineage from source to publication
- [ ] Publication pipeline isolated from policy intervention
- [ ] Reproducibility validated — published statistics can be regenerated from source

---

### 3. Aid Transparency and Accountability

**Principle Statement**:
All ODA-related systems MUST publish comprehensive, timely, and comparable information about UK development spending in accordance with the International Aid Transparency Initiative (IATI) and the International Development Act 2002.

**Rationale**:
The UK is a signatory to the Busan Partnership for Effective Development Co-operation and has commitments under the International Development Act 2002 to ensure that aid spending contributes to poverty reduction. ICAI (the Independent Commission for Aid Impact) scrutinises aid effectiveness, and the OECD DAC conducts peer reviews. Architecture must enable transparency by default, making aid data accessible to Parliament, civil society, partner country governments, and the public.

**Implications**:

- Publish all ODA activity data to the IATI Registry within 30 days of activity
- Implement DAC CRS++ sector codes, flow types, and tied/untied status for all disbursements
- Support results-based reporting linking spend to outcomes using IATI results framework
- Enable programmatic access to aid data through public APIs (aligning with FCDO DevTracker)
- Maintain classification controls for sensitive ODA programmes (security, conflict zones) while maximising transparency
- Design for forward-looking spend publication (IATI activity budgets for 3+ years)

**Validation Gates**:

- [ ] IATI data published to Registry within agreed timeliness targets
- [ ] DAC reporting validated against OECD CRS++ validation rules
- [ ] Results framework data linked to spend at activity level
- [ ] Public API available with at least annual publication of forward spend
- [ ] ICAI data access requirements assessed and accommodated
- [ ] Sensitive programme exclusions documented and minimised

---

### 4. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement, particularly given the international data flows, cross-government data sharing, and sensitive ODA programme data involved.

**Rationale**:
The SDG 17 programme handles data that spans classification levels (from PUBLIC statistical indicators to OFFICIAL-SENSITIVE diplomatic and aid programme data), crosses international boundaries, and involves cross-government data sharing where compromise of one department's data could cascade to others. NCSC Cyber Assessment Framework (CAF), GovAssure, and Secure by Design principles are mandatory.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request authenticated across government boundaries
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit (TLS 1.3+) and at rest (AES-256)
4. **Continuous Verification**: Monitor, log, and analyse all access patterns across departmental boundaries

**Mandatory Controls**:

- [ ] Multi-factor authentication for all human access, including cross-government federated identity
- [ ] Service-to-service authentication (mutual TLS, signed tokens) for all cross-department API calls
- [ ] Secrets management via secure vault (never in code or config files)
- [ ] Network segmentation with minimal trust zones, particularly between department data enclaves
- [ ] Encryption at rest for all data stores, with separate key management per classification tier
- [ ] Encrypted transport for all network communication including cross-border data transfers
- [ ] Structured logging of all authentication/authorisation events with 7-year retention for audit
- [ ] Regular security testing (penetration testing annually, vulnerability scanning weekly)
- [ ] NCSC CAF assessment completed and GovAssure certification maintained

**Compliance Frameworks**:

- NCSC Cyber Assessment Framework (CAF)
- GovAssure
- HMG Security Policy Framework
- Secure by Design (GDS/NCSC)
- UK GDPR (international data transfers require adequacy decisions or SCCs)

**Exceptions**:

- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] Threat model completed covering international data flows and cross-government sharing
- [ ] Security controls mapped to NCSC CAF outcomes
- [ ] ITHC (IT Health Check) / penetration testing completed
- [ ] Incident response runbook created covering cross-department breach scenarios
- [ ] International data transfer impact assessments completed (UK GDPR Chapter V)

---

### 5. Cross-Government Data Federation

**Principle Statement**:
All systems MUST support federated data access through a common API gateway and data catalogue, enabling authorised cross-department data sharing without creating centralised data lakes that concentrate risk.

**Rationale**:
SDG 17 requires data from across government — FCDO (aid), HMRC (trade), ONS (statistics), DBT (trade partnerships), BEIS, Defra, DHSC, and others. The cross-government data sharing platform (Project 002) must enable this without requiring departments to surrender control of their data or accept disproportionate security risk. The Government Data Quality Hub, the Data Standards Authority, and the DCAT-AP metadata standard provide the governance framework.

**Implications**:

- Implement a federated API gateway model — data remains in department systems, accessed via standardised APIs
- Use DCAT (Data Catalog Vocabulary) for metadata discovery across departments
- Enforce data sharing agreements (DSAs) technically — APIs only return data authorised under active DSAs
- Support multiple query patterns: real-time API, batch extract, and event-driven notification
- Design for heterogeneous department technology stacks (not all departments use the same cloud provider)
- Implement data minimisation — APIs return only the fields authorised, not entire datasets

**Validation Gates**:

- [ ] API gateway federates access without centralising data storage
- [ ] DCAT-compliant data catalogue published and searchable
- [ ] Data sharing agreements enforced technically at API level
- [ ] Department data sovereignty preserved — no department data copied without explicit consent
- [ ] Cross-department authentication via Government Identity Service or equivalent federation

---

### 6. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning, with particular attention to cross-system observability across the federated architecture.

**Rationale**:
The federated nature of SDG 17 systems means that problems in one department's service can cascade to others. Cross-government data sharing failures, IATI publication delays, or trade data feed interruptions must be detected and diagnosed quickly. Each system must be observable independently, and the programme must provide a unified view of cross-system health.

**Telemetry Requirements**:

- **Logging**: Structured JSON logs with W3C Trace Context correlation IDs across department boundaries
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates per department API
- **Tracing**: Distributed trace context propagated across federated API calls
- **Alerting**: SLO-based alerting with actionable runbooks, escalation to department service teams

**Required Instrumentation**:

- Request volume, latency distribution, error rate per department API endpoint
- Resource utilisation (CPU, memory, I/O, network) per service
- Business metrics (ODA disbursements processed, SDG indicators updated, trade records matched)
- Security events (cross-department auth failures, data sharing agreement violations)
- IATI publication timeliness (time from activity to Registry publication)

**Validation Gates**:

- [ ] Logging, metrics, tracing instrumented with cross-department correlation
- [ ] Dashboards and alerts configured for programme-level and department-level views
- [ ] SLOs defined per department API (availability, latency, error rate)
- [ ] Runbooks created for cross-department failure scenarios
- [ ] Capacity planning metrics tracked with growth projections

---

## II. Data Principles

### 7. Data Sovereignty and Classification

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK Government security classification policy, UK GDPR, and international data transfer regulations, with particular rigour for ODA programme data that may relate to conflict zones or sensitive diplomatic relationships.

**Data Classification Tiers**:

1. **OFFICIAL — PUBLIC**: Published SDG indicators, IATI data on the public registry, trade statistics
2. **OFFICIAL**: Internal cross-government data, unpublished draft statistics, routine ODA programme management
3. **OFFICIAL-SENSITIVE**: Sensitive ODA programme data (conflict, security, governance programmes), pre-release statistics, trade negotiation positions
4. **SECRET**: Exceptionally, intelligence-informed ODA targeting or sanctions-related trade data (out of scope for this programme but interfaces defined)

**Data Residency**:

- All data hosted within UK sovereign cloud (UK region of approved cloud providers)
- International data transfers (e.g., to partner country systems, IATI Registry, OECD DAC) require UK GDPR Chapter V compliance
- Cross-border transfer mechanisms: adequacy decisions, Standard Contractual Clauses, or public interest derogations for statistical data

**Data Retention**:

- ODA financial data: 7 years (National Audit Office requirements)
- Statistical microdata: retained per ONS retention schedule
- Trade data: retained per HMRC statutory requirements
- Audit logs: 7 years minimum

**Validation Gates**:

- [ ] Data classification performed for all data stores and API responses
- [ ] UK sovereign cloud hosting confirmed
- [ ] International data transfer impact assessments completed
- [ ] Retention policies configured with automated deletion
- [ ] Access controls enforce classification-appropriate security

---

### 8. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability, with particular importance given that published statistics and ODA reports are subject to Parliamentary scrutiny, NAO audit, and international peer review.

**Quality Standards**:

- **Completeness**: All 244 UN SDG indicators populated where UK data sources exist; ODA activities 100% coded to DAC CRS++ sectors
- **Consistency**: Cross-departmental data reconciled (e.g., HMRC trade data matches DBT trade records)
- **Accuracy**: ODA financial figures reconciled to FCDO ARIES accounting system within 0.1% tolerance
- **Timeliness**: IATI publication within 30 days; SDG indicators updated within 90 days of source release; trade data daily

**Lineage Requirements**:

- Source-to-target mapping documented for all data flows across department boundaries
- Transformation logic version-controlled and reproducible
- Data quality metrics tracked per pipeline, per department source
- Impact analysis capability for schema changes across federated APIs

**Validation Gates**:

- [ ] Data quality rules defined and automated for each department data feed
- [ ] Lineage metadata captured from source department to published output
- [ ] Data contracts established between producing and consuming departments
- [ ] Schema evolution strategy documented for cross-government APIs

---

### 9. Single Source of Truth per Domain

**Principle Statement**:
Every data domain MUST have a single authoritative source department. Derived copies must be clearly labelled and synchronised via the federated API gateway.

**Rationale**:
With multiple departments contributing data, the risk of contradictory figures is significant. If FCDO reports different ODA totals than the figures ONS publishes in the SDG Dashboard, or if DBT trade figures disagree with HMRC customs data, public trust and international credibility are undermined.

**Domain Ownership**:

| Data Domain | Authoritative Department | System of Record |
|-------------|------------------------|------------------|
| ODA financial flows | FCDO | ARIES |
| ODA activity data | FCDO | Activity Management System |
| Trade statistics | HMRC | Customs Declaration Service |
| Trade partnerships | DBT | Trade Partnerships CRM |
| SDG indicator values | ONS | SDG Data Platform |
| SDG metadata | ONS | SDG Metadata Registry |
| Cross-government data catalogue | Cabinet Office | Data Catalogue Service |
| Government spending (all) | HM Treasury | OSCAR |

**Implications**:

- The federated API gateway routes queries to the authoritative source, not to cached copies
- Caching is permitted for performance but must be labelled with freshness metadata
- No department may publish another department's data without referencing the authoritative source
- Reconciliation processes run daily for high-criticality data (ODA totals, trade balances)

**Validation Gates**:

- [ ] System of record identified and documented for each data entity
- [ ] Federated API gateway routes to authoritative sources
- [ ] Caches labelled with freshness/staleness metadata
- [ ] Daily reconciliation for ODA and trade financial data
- [ ] No bidirectional sync without explicit conflict resolution

---

## III. Integration Principles

### 10. API-First with Government API Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned APIs conforming to GDS API Technical and Data Standards. Direct database access across system boundaries is prohibited.

**Rationale**:
The federated architecture depends on reliable, well-documented APIs. GDS API Technical and Data Standards provide a common baseline for authentication, error handling, pagination, and versioning across government. APIs must also serve international partners with varying technical capabilities.

**Implications**:

- RESTful APIs with JSON payloads as default; bulk data export via CSV/SDMX where required
- API versioning via URL path (e.g., /v1/, /v2/) with minimum 12-month deprecation notice
- OAuth 2.0 / OpenID Connect for authentication; API keys for low-sensitivity public data
- Rate limiting per consumer with department-specific quotas
- Consistent error response format per GDS API standards
- API specifications published in OpenAPI 3.0 on the cross-government API catalogue

**Validation Gates**:

- [ ] API specifications published in OpenAPI 3.0
- [ ] GDS API Technical and Data Standards compliance verified
- [ ] Authentication model documented (OAuth 2.0 / API key per consumer type)
- [ ] Rate limiting and quota management implemented
- [ ] Deprecation policy defined with minimum 12-month notice

---

### 11. Event-Driven Architecture for Cross-Government Notifications

**Principle Statement**:
Systems SHOULD use event-driven communication for cross-department notifications, data change alerts, and asynchronous workflows to reduce temporal coupling and improve resilience.

**Rationale**:
Cross-government data sharing involves departments with different operational hours, maintenance windows, and reliability profiles. Synchronous dependencies between departments create fragile chains where one department's downtime cascades to others. Event-driven patterns decouple departments while maintaining data currency.

**When to Use Events**:

- ODA activity status changes (new disbursement, activity completion) — notify SDG Dashboard, DAC reporting
- Trade data updates — notify DBT of new HMRC customs declarations
- SDG indicator publication — notify FCDO, DBT, and policy teams of updated UK performance
- Data sharing agreement changes — notify affected departments of new/revoked access
- Cross-department data quality alerts — notify source department of downstream quality issues

**When Synchronous is Acceptable**:

- Real-time data queries where freshness is critical (e.g., current ODA commitment against budget)
- User-facing lookups (e.g., searching the data catalogue)
- Authentication and authorisation decisions

**Validation Gates**:

- [ ] Event-driven patterns used for cross-department notifications
- [ ] Message durability and at-least-once delivery guaranteed
- [ ] Event schemas versioned and published in the data catalogue
- [ ] Dead letter queues configured with alerting for failed deliveries
- [ ] Cross-department event routing tested for failure scenarios

---

## IV. Quality Attributes

### 12. Performance for International Scale

**Principle Statement**:
All systems MUST meet defined performance targets under expected load, accounting for international users (partner countries, multilateral organisations) accessing UK systems across global network infrastructure.

**Performance Targets**:

- **IATI Publication API**: < 500ms response time (p95), supporting bulk downloads of full UK ODA dataset (~50,000 activities)
- **Cross-Government API Gateway**: < 200ms response time (p95) for federated queries, < 2s for cross-department joins
- **SDG Dashboard**: < 2s page load time (p95) for international users on standard broadband
- **Trade Platform**: < 300ms API response time (p95), supporting real-time trade data integration

**Implications**:

- CDN deployment for public-facing dashboards and data downloads
- Geographic distribution for international API consumers
- Bulk data export mechanisms for partner countries with limited bandwidth
- Performance monitoring with geographic breakdown (UK, Europe, Africa, Asia, Americas)

**Validation Gates**:

- [ ] Performance targets defined per system with international user scenarios
- [ ] Load testing performed including simulated international latency
- [ ] CDN/geographic distribution implemented for public-facing services
- [ ] Performance monitoring includes geographic breakdown
- [ ] Bulk export available for bandwidth-constrained partners

---

### 13. Availability and Resilience

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss, with higher availability for systems supporting statutory reporting deadlines.

**Availability Targets**:

| System | Availability SLA | RTO | RPO | Rationale |
|--------|-----------------|-----|-----|-----------|
| Cross-Government API Gateway | 99.95% | 15 min | 0 min | Critical shared infrastructure |
| IATI Publication Service | 99.9% | 1 hour | 15 min | International commitments |
| SDG Dashboard | 99.9% | 1 hour | 1 hour | Public-facing, reputational |
| Trade Platform | 99.9% | 30 min | 5 min | Real-time trade data flows |
| Data Catalogue | 99.5% | 4 hours | 1 hour | Internal tool, not user-facing |

**Implications**:

- Multi-AZ deployment for all production services
- Automated failover tested quarterly
- Disaster recovery plan covering cross-government dependencies
- Heightened availability during statutory reporting periods (DAC annual returns, VNR publication, Budget/Spending Review)

**Validation Gates**:

- [ ] Availability SLAs defined per system
- [ ] RTO and RPO documented and tested
- [ ] Multi-AZ deployment confirmed
- [ ] DR plan tested including cross-department failure scenarios
- [ ] Heightened availability periods identified and resourced

---

### 14. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with modular architecture that can accommodate new SDG indicators, new data sharing agreements, new trade partnerships, and evolving international reporting standards without architectural rework.

**Rationale**:
The SDG framework is reviewed periodically (the current 2030 Agenda may be succeeded by a post-2030 framework). IATI standards evolve. New trade agreements create new data requirements. The architecture must accommodate these changes through configuration and extension, not redesign.

**Implications**:

- SDG indicator framework stored as configuration data, not hard-coded
- Data sharing agreement rules engine allows new departments/datasets without code changes
- Trade partnership configuration supports new FTA structures via metadata
- IATI standard version upgrades accommodated through adapter pattern
- Architecture Decision Records (ADRs) document all significant design choices

**Validation Gates**:

- [ ] New SDG indicators addable via configuration (no code deployment)
- [ ] New data sharing agreements activatable via admin interface
- [ ] IATI standard version upgradeable via adapter without core system changes
- [ ] ADRs document key architecture decisions
- [ ] Module boundaries clear with defined responsibilities

---

## V. Development Practices

### 15. Infrastructure as Code with Multi-Department Governance

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines, with governance processes that accommodate multi-department ownership.

**Rationale**:
The federated architecture spans multiple departments, each with their own cloud accounts, security boundaries, and change management processes. Infrastructure as Code ensures consistency, reproducibility, and auditability across this distributed landscape.

**Implications**:

- All infrastructure defined in declarative code (Terraform, CloudFormation, or equivalent)
- Shared infrastructure (API gateway, event bus, data catalogue) managed by Cabinet Office with cross-department change advisory board
- Department-specific infrastructure managed by each department within agreed standards
- Infrastructure changes go through code review with cross-department impact assessment for shared components
- No manual changes to production infrastructure

**Validation Gates**:

- [ ] All infrastructure defined as code
- [ ] Shared infrastructure change process includes cross-department review
- [ ] Department infrastructure complies with agreed standards
- [ ] Automated deployment pipelines for all environments
- [ ] No manual production changes

---

### 16. Continuous Integration, Deployment, and Compliance

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates including security scanning, accessibility testing, and IATI/SDMX schema validation.

**Rationale**:
The international reporting obligations mean that data format compliance is as critical as functional correctness. CI/CD pipelines must validate not just code quality but also data standard compliance.

**Pipeline Stages**:

1. **Source Control**: All changes committed to version control
2. **Build**: Automated compilation and packaging
3. **Test**: Unit, integration, and end-to-end tests
4. **Data Standard Validation**: IATI schema validation, SDMX structure validation, DAC CRS++ code validation
5. **Security Scan**: SAST, dependency scanning, container scanning
6. **Accessibility Test**: WCAG 2.1 AA automated checks
7. **Deployment**: Automated deployment to environments
8. **Smoke Test**: Post-deployment validation of key data flows

**Validation Gates**:

- [ ] Automated CI/CD pipeline exists for all services
- [ ] Data standard validation integrated into pipeline
- [ ] Security scanning integrated (SAST, dependency, container)
- [ ] Accessibility testing automated
- [ ] Deployment automated with rollback capability

---

## VI. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:

- Technical constraints in a partner country system that prevent standard interoperability
- Regulatory or legal requirements in a specific jurisdiction
- Transitional state during department system migration
- Pilot/proof-of-concept with defined end date
- Classification constraints requiring isolated architecture (e.g., conflict-zone ODA programmes)

**Exception Request Requirements**:

- [ ] Justification with business/technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment including impact on international reporting obligations
- [ ] Expiration date (exceptions are time-bound, maximum 12 months)
- [ ] Remediation plan to achieve compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team
2. Review by SDG 17 Architecture Review Board
3. CTO/CDIO approval for exceptions to critical principles
4. Document exception in project architecture documentation
5. Quarterly review of all exceptions with mandatory remediation or renewal

---

## VII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones:

**Discovery/Alpha**:

- [ ] Architecture principles understood by all department teams
- [ ] High-level approach aligns with principles including international interoperability
- [ ] No obvious principle violations
- [ ] Cross-department data flows identified and data sharing agreements initiated

**Beta/Design**:

- [ ] Detailed architecture documented with cross-department integration design
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Security and data principles validated by NCSC/department security teams
- [ ] IATI/SDMX/DCAT compliance verified in design

**Pre-Production**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed including cross-department integration testing
- [ ] Operational readiness verified across all participating departments
- [ ] International partner integration tested where applicable

### Enforcement

- Architecture reviews are **mandatory** for all SDG 17 projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound (max 12 months) and reviewed quarterly
- Cross-department architectural decisions require consensus or escalation to the SDG 17 Programme Board

---

## VIII. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | International Interoperability by Default | Strategic | CRITICAL | IATI/SDMX/DAC compliance testing |
| 2 | Statistical Independence and Integrity | Strategic | CRITICAL | UKSA Code of Practice assessment |
| 3 | Aid Transparency and Accountability | Strategic | CRITICAL | IATI Registry publication, ICAI review |
| 4 | Security by Design | Strategic | CRITICAL | NCSC CAF, GovAssure, pen testing |
| 5 | Cross-Government Data Federation | Strategic | HIGH | Federated API testing, DCAT catalogue |
| 6 | Observability and Operational Excellence | Strategic | HIGH | Metrics, logs, traces, cross-dept correlation |
| 7 | Data Sovereignty and Classification | Data | CRITICAL | Classification audit, data transfer assessments |
| 8 | Data Quality and Lineage | Data | HIGH | Quality metrics, lineage metadata |
| 9 | Single Source of Truth per Domain | Data | HIGH | Reconciliation, authoritative source routing |
| 10 | API-First with Government API Standards | Integration | HIGH | GDS API standards compliance |
| 11 | Event-Driven Cross-Government Notifications | Integration | MEDIUM | Event schema validation, DLQ monitoring |
| 12 | Performance for International Scale | Quality | HIGH | Load testing with international scenarios |
| 13 | Availability and Resilience | Quality | CRITICAL | SLA monitoring, DR testing |
| 14 | Maintainability and Evolvability | Quality | MEDIUM | Configuration-driven extensibility |
| 15 | Infrastructure as Code | DevOps | HIGH | IaC coverage, cross-dept governance |
| 16 | CI/CD with Data Standard Compliance | DevOps | HIGH | Pipeline with IATI/SDMX validation |

### Key Legislation and Standards

| Reference | Relevance |
|-----------|-----------|
| International Development Act 2002 | Legal basis for UK ODA, duty to poverty reduction |
| Statistics and Registration Service Act 2007 | ONS independence, Code of Practice for Statistics |
| UK GDPR / Data Protection Act 2018 | Personal data protection, international transfers |
| Official Statistics Code of Practice (UKSA) | Trustworthiness, Quality, Value for statistical outputs |
| IATI Standard v2.03 | International aid transparency data format |
| OECD DAC Statistical Reporting Directives | ODA definition, CRS++ codes, flow types |
| SDMX (Statistical Data and Metadata eXchange) | International statistical data exchange standard |
| GDS Service Standard | 14-point standard for UK Government digital services |
| Technology Code of Practice (TCoP) | Cross-government technology standards |
| NCSC Cyber Assessment Framework | Cyber security assessment for critical services |
| GDS API Technical and Data Standards | Government API design standards |
| DCAT (Data Catalog Vocabulary) | Metadata standard for data catalogues |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 17: Partnerships for the Goals
**Model**: Claude Opus 4.6
