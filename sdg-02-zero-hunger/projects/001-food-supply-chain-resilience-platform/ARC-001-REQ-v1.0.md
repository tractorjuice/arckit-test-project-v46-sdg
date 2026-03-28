# Project Requirements: Food Supply Chain Resilience Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Food Supply Chain Resilience Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, DEFRA Food Resilience Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Food Standards Agency, Cabinet Office Food Strategy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Food Supply Chain Resilience Platform. It provides the basis for design, development, testing, and acceptance of the system, traceable to the stakeholder drivers and goals identified in ARC-001-STKE-v1.0 and aligned with the architecture principles in ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

The UK imports approximately 46% of its food supply, with critical dependencies on specific import corridors (e.g., Calais-Dover for fresh produce, Rotterdam-Felixstowe for ambient goods). Post-Brexit border controls, including Sanitary and Phytosanitary (SPS) checks at Border Control Posts (BCPs), have introduced new friction points. COVID-19, the 2021 HGV driver shortage, and the 2022 egg supply crisis exposed the government's limited visibility of supply chain status.

DEFRA currently relies on manual processes -- phone calls to industry contacts, weekly trade association reports, and ad-hoc data requests -- to assess supply chain health. Response times during crises are measured in days rather than hours. The Food Supply Chain Resilience Platform will replace these fragmented processes with a near-real-time monitoring capability covering the top 20 food categories by volume.

The platform aligns with the Government Food Strategy 2022, the UK Food Security Report (required under the Agriculture Act 2020, Section 19), and DEFRA's 2025-2030 Digital Strategy. It will serve as the authoritative source for supply chain risk data consumed by the National Food Strategy Dashboard (Project 005).

### Objectives

- Provide near-real-time (< 4 hours latency) monitoring of UK food supply chain status across major food categories
- Enable evidence-based ministerial briefings and crisis response coordination within 2 hours of a detected disruption
- Integrate data from commercial supply chain actors, border systems, and domestic production indicators
- Deliver self-service analytics for DEFRA policy analysts and FSA food safety teams
- Publish standardised supply chain metrics via API for the National Food Strategy Dashboard (Project 005)

### Expected Outcomes

- > 60% of UK food supply (by volume) monitored in near-real-time by Q4 2027
- Crisis detection-to-ministerial-briefing time reduced from 3-7 days to < 4 hours
- 50+ active data providers connected to the platform
- 90% of DEFRA food policy analysts using the platform as their primary monitoring tool
- Quantified supply chain risk scores for all 20 monitored food categories

### Project Scope

**In Scope**:

- Real-time data ingestion from retailers, importers, border systems, and port operators
- Supply chain risk scoring and alert engine
- Analyst dashboards and self-service reporting
- API for cross-government data sharing (Project 005)
- Integration with FSA food safety surveillance systems
- SPS check data from Border Control Posts

**Out of Scope**:

- Direct consumer-facing services (this is an internal government platform)
- Food pricing analytics (separate DEFRA initiative)
- Agricultural production forecasting (handled by Project 004)
- International supply chain monitoring beyond UK import corridors
- Procurement or commercial contract management

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO, Food Resilience Programme | Senior Responsible Owner | DEFRA | Decision maker |
| DEFRA Chief Digital Officer | Architecture Oversight | DEFRA | Technical governance |
| Food Supply Chain Analysis Team Lead | Product Owner | DEFRA | Requirements definition |
| FSA Head of Surveillance | Co-user and Data Partner | FSA | Requirements input, joint steering |
| DEFRA SIRO | Information Risk Owner | DEFRA | Data governance sign-off |
| DEFRA Cyber Security Lead | Security Architect | DEFRA | Security review |
| CDDO Assessment Team | Standards Assurance | CDDO | Service assessment gates |
| Cabinet Office Food Strategy Unit | Data Consumer (Project 005) | Cabinet Office | API requirements |
| Major Retailer Data Leads | Data Providers | Industry | Data feed specifications |
| HMRC Border Force IT | Data Provider | HMRC | Integration specifications |

---

## Business Requirements

### BR-001: Real-Time Supply Chain Visibility

**Description**: The platform must provide near-real-time visibility of UK food supply chain status, enabling DEFRA and FSA to detect disruptions before they reach consumer-visible levels.

**Rationale**: Currently, DEFRA has no systematic way to monitor food supply chains in real time. Crises are detected reactively through media reports or industry tip-offs, leading to delayed government response (Stakeholder Driver SD-1).

**Success Criteria**:

- Data latency from source event to platform visibility < 4 hours for 80% of data feeds
- Coverage of > 60% of UK food supply by volume
- Monitoring of top 20 food categories by consumption volume

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Secretary of State (SD-1), FSA (SD-8)

---

### BR-002: Evidence-Based Crisis Response

**Description**: The platform must enable rapid, evidence-based ministerial briefings and crisis coordination during food supply disruptions.

**Rationale**: During the 2022 egg shortage, the ministerial briefing was delayed by 5 days due to manual data gathering. Ministers need pre-formatted situation reports within hours (Stakeholder Driver SD-1, SD-5).

**Success Criteria**:

- Automated situation report generation within 30 minutes of alert trigger
- Crisis briefing pack available for ministerial review within 2 hours
- Historical crisis response playbooks integrated into the platform

**Priority**: MUST_HAVE

**Stakeholder**: DEFRA Secretary of State (SD-1), SRO (SD-3)

---

### BR-003: Self-Service Analytics for Policy Teams

**Description**: The platform must provide self-service analytics capabilities enabling policy analysts to explore supply chain data without IT intervention.

**Rationale**: Currently, every data query requires a request to the DEFRA data team with a 3-5 day turnaround. Analysts need direct access to explore trends, run comparisons, and generate ad-hoc reports (Stakeholder Driver SD-5).

**Success Criteria**:

- 90% of routine analytical queries answerable through self-service dashboards
- Average time to answer a policy question reduced from 5 days to < 1 hour
- Analysts able to create custom reports without SQL knowledge

**Priority**: SHOULD_HAVE

**Stakeholder**: Food Supply Chain Analysis Team (SD-5)

---

### BR-004: Cross-Government Data Sharing

**Description**: The platform must publish standardised supply chain metrics through APIs for consumption by the National Food Strategy Dashboard (Project 005) and other authorised government systems.

**Rationale**: The Cabinet Office depends on reliable, timely supply chain data for the National Food Strategy Dashboard. Ad-hoc data sharing creates inconsistency and delays (Stakeholder Driver SD-10).

**Success Criteria**:

- Published RESTful API with versioned data contracts
- Data freshness SLA of < 6 hours for dashboard metrics
- API uptime > 99.5%

**Priority**: MUST_HAVE

**Stakeholder**: Cabinet Office (SD-10)

---

### BR-005: Industry Data Partnership

**Description**: The platform must support voluntary and regulatory data sharing with commercial supply chain actors while protecting commercially sensitive information.

**Rationale**: The platform's value depends on industry data. Retailers will only participate if their competitive data is protected from FOI disclosure and competitor access (Stakeholder Driver SD-9).

**Success Criteria**:

- Data sharing framework approved by DEFRA legal and SIRO
- Aggregation and anonymisation applied before cross-government sharing
- Industry advisory panel established and meeting quarterly
- FOI exemption (s.43 FOIA 2000) position documented and tested

**Priority**: MUST_HAVE

**Stakeholder**: Major Retailers (SD-9), SIRO (SD-7)

---

### BR-006: Food Safety Early Warning

**Description**: The platform must provide the FSA with early warning of supply chain disruptions that could affect food safety, including cold chain failures, supplier substitution, and contamination risks.

**Rationale**: Supply disruptions create food safety risks as suppliers cut corners to maintain supply. The FSA needs proactive intelligence rather than reactive detection after consumer harm (Stakeholder Driver SD-8).

**Success Criteria**:

- Food safety risk indicators defined for each monitored food category
- Automated alerts to FSA when safety-relevant thresholds are breached
- Integration with FSA's existing Food Surveillance System

**Priority**: MUST_HAVE

**Stakeholder**: FSA (SD-8)

---

## Functional Requirements

### User Personas

#### Persona 1: Policy Analyst (DEFRA)

- **Role**: Food Supply Chain Analyst, DEFRA Food Policy Team
- **Goals**: Monitor supply chain health, identify emerging risks, provide evidence-based advice to ministers
- **Pain Points**: Currently relies on phone calls and spreadsheets; 3-7 day lag in data; no single view of supply chain status
- **Technical Proficiency**: Medium (comfortable with dashboards, not SQL)

#### Persona 2: Food Safety Surveillance Officer (FSA)

- **Role**: Food Safety Surveillance Officer, FSA
- **Goals**: Detect supply chain disruptions that could affect food safety; trigger inspections at high-risk points
- **Pain Points**: Learns about supply disruptions after food safety incidents occur; no proactive intelligence
- **Technical Proficiency**: Medium

#### Persona 3: Crisis Response Coordinator (DEFRA)

- **Role**: Crisis Response Lead, DEFRA Emergency Planning
- **Goals**: Coordinate cross-government response during food supply crises; brief ministers rapidly
- **Pain Points**: No pre-prepared situation reports; manual coordination across departments
- **Technical Proficiency**: Low (needs pre-formatted outputs)

#### Persona 4: Data Integration Analyst (DEFRA Digital)

- **Role**: Data Engineer, DEFRA Digital Team
- **Goals**: Onboard new data providers, monitor data feed health, manage data quality
- **Pain Points**: No standard onboarding process; each data source requires bespoke integration
- **Technical Proficiency**: High

---

### Use Cases

#### UC-1: Monitor Supply Chain Dashboard

**Actor**: Policy Analyst

**Preconditions**:

- User authenticated via DEFRA SSO
- At least one data feed active for selected food category

**Main Flow**:

1. User navigates to supply chain dashboard
2. System displays overview map of UK food supply status by category
3. User selects a food category (e.g., "Fresh Produce - Salad Vegetables")
4. System displays category detail: import volumes, domestic production, stock levels, risk score
5. User drills down to specific import corridors or suppliers
6. System shows time-series data, trend analysis, and anomaly indicators

**Postconditions**:

- User has current supply chain status for selected category
- User activity logged for audit purposes

**Alternative Flows**:

- **Alt 3a**: If no data available for selected category, system displays "No Data" with reason and expected data availability date
- **Alt 4a**: If data is stale (> 24 hours), system displays warning banner with last update timestamp

**Priority**: CRITICAL

---

#### UC-2: Respond to Supply Chain Alert

**Actor**: Crisis Response Coordinator

**Preconditions**:

- Alert triggered by risk scoring engine
- User has crisis response role permission

**Main Flow**:

1. System sends alert notification (email, SMS, platform notification)
2. User opens alert detail showing affected food category, severity, and evidence
3. User views auto-generated situation report with recommended actions
4. User acknowledges alert and initiates crisis response workflow
5. System records alert acknowledgement and tracks response actions
6. User generates ministerial briefing pack from template

**Postconditions**:

- Alert acknowledged and response initiated
- Audit trail of all actions recorded
- Ministerial briefing pack generated

**Exception Flows**:

- **Ex 1**: If alert is false positive, user marks as "Dismissed - False Positive" with justification

**Priority**: CRITICAL

---

#### UC-3: Onboard New Data Provider

**Actor**: Data Integration Analyst

**Preconditions**:

- Data sharing agreement signed
- Data provider has been vetted and approved by SIRO

**Main Flow**:

1. User creates new data source record with provider details and data classification
2. User configures data feed (API endpoint, file drop, format, frequency)
3. System validates connectivity and data format against schema
4. User maps source fields to platform data model
5. System runs data quality checks on initial data load
6. User activates data feed for production ingestion
7. System begins monitoring data feed health

**Postconditions**:

- New data source active and ingesting data
- Data quality baseline established
- Feed health monitoring active

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-001: Data Ingestion Engine

**Description**: The system must ingest data from multiple heterogeneous sources in near-real-time, supporting various formats and protocols.

**Relates To**: BR-001, UC-3

**Acceptance Criteria**:

- [ ] Given a retailer API data source, when data is pushed via webhook, then the platform processes it within 15 minutes
- [ ] Given a border control CSV file, when deposited in SFTP, then the platform processes it within 30 minutes
- [ ] Given a data feed failure, when the feed is unresponsive for > 2 consecutive intervals, then an alert is raised to the data integration team
- [ ] Given data with validation errors, when ingested, then invalid records are quarantined with error descriptions

**Data Requirements**:

- **Inputs**: Retailer stock/sales data (JSON/CSV), border crossing volumes (XML), port logistics data (API), domestic production estimates (CSV)
- **Outputs**: Normalised supply chain events in platform data model
- **Validations**: Schema validation, referential integrity, range checks, duplicate detection

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Data sharing agreements (BR-005), data provider technical readiness

---

#### FR-002: Risk Scoring Engine

**Description**: The system must calculate supply chain risk scores for each monitored food category based on configurable indicators and thresholds.

**Relates To**: BR-001, BR-006, UC-2

**Acceptance Criteria**:

- [ ] Given supply chain data for a food category, when risk indicators breach configured thresholds, then a risk score (0-100) is calculated
- [ ] Given a risk score exceeding the "High" threshold (>70), when confirmed by anomaly detection, then an automated alert is generated
- [ ] Given changing risk conditions, when new data arrives, then risk scores are recalculated within 15 minutes
- [ ] Given a new food category, when added to monitoring, then default risk indicators and thresholds are applied

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-001 (data ingestion), historical baseline data

---

#### FR-003: Analyst Dashboard

**Description**: The system must provide interactive dashboards enabling policy analysts to monitor supply chain status, explore trends, and generate reports.

**Relates To**: BR-003, UC-1

**Acceptance Criteria**:

- [ ] Given authenticated analyst access, when navigating to the dashboard, then a map-based overview of all monitored food categories is displayed
- [ ] Given a food category selected, when drilling down, then time-series data, trend lines, and anomaly indicators are shown
- [ ] Given a custom date range and filters, when applied, then data refreshes within 5 seconds
- [ ] Given a report configuration, when "Export" is selected, then report is generated in PDF or CSV format

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-001, FR-002

---

#### FR-004: Alert Management

**Description**: The system must manage supply chain alerts with configurable notification channels, escalation rules, and acknowledgement tracking.

**Relates To**: BR-002, UC-2

**Acceptance Criteria**:

- [ ] Given a risk score breach, when alert is generated, then notifications are sent via configured channels (email, SMS, platform)
- [ ] Given an unacknowledged critical alert, when 30 minutes has elapsed, then the alert is escalated to the next level
- [ ] Given an alert is acknowledged, when a response action is logged, then the audit trail records user, timestamp, and action taken

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-002, notification service (GOV.UK Notify)

---

#### FR-005: Situation Report Generator

**Description**: The system must auto-generate situation reports from alert data and templates, suitable for ministerial briefing.

**Relates To**: BR-002, UC-2

**Acceptance Criteria**:

- [ ] Given an active alert, when "Generate SitRep" is triggered, then a formatted report is produced within 2 minutes
- [ ] Given a SitRep template, when populated with current data, then all mandatory fields are completed with evidence-backed statements
- [ ] Given a completed SitRep, when approved, then it is published to the ministerial briefing channel

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-002, FR-004

---

#### FR-006: Cross-Government Data API

**Description**: The system must expose supply chain metrics via a versioned RESTful API for consumption by the National Food Strategy Dashboard (Project 005) and other authorised consumers.

**Relates To**: BR-004, INT-001

**Acceptance Criteria**:

- [ ] Given an authorised API consumer, when requesting supply chain metrics, then data is returned in < 500ms (p95)
- [ ] Given API versioning, when a new version is released, then the previous version remains available for 6 months
- [ ] Given API rate limiting, when a consumer exceeds 1000 requests/minute, then requests are throttled with appropriate error response

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-001, FR-002, API gateway

---

#### FR-007: Data Quality Monitoring

**Description**: The system must continuously monitor data feed quality and report on completeness, timeliness, and accuracy.

**Relates To**: BR-001, UC-3

**Acceptance Criteria**:

- [ ] Given an active data feed, when completeness drops below 90%, then a data quality alert is raised
- [ ] Given a data quality dashboard, when accessed, then feed health is displayed with traffic-light indicators
- [ ] Given a data provider SLA breach, when detected, then the breach is logged and the provider notified

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-001

---

#### FR-008: Audit Trail

**Description**: The system must maintain a comprehensive audit trail of all user actions, data access, alert responses, and system events.

**Relates To**: BR-005, NFR-C-2

**Acceptance Criteria**:

- [ ] Given any user action, when performed, then who/what/when/where/result is logged
- [ ] Given audit log data, when queried by authorised auditors, then results are returned with full detail
- [ ] Given audit logs, when stored, then they are immutable and retained for 7 years

**Priority**: MUST_HAVE

**Complexity**: LOW

---

#### FR-009: User and Role Management

**Description**: The system must support role-based access control with distinct permission levels for DEFRA analysts, FSA users, crisis coordinators, data engineers, and API consumers.

**Relates To**: NFR-SEC-1, NFR-SEC-2

**Acceptance Criteria**:

- [ ] Given a DEFRA analyst role, when accessing the platform, then only non-commercially-sensitive aggregated data is visible
- [ ] Given an FSA user role, when accessing the platform, then food safety-relevant data and alerts are accessible
- [ ] Given a crisis coordinator role, when responding to alerts, then SitRep generation and escalation functions are available
- [ ] Given an API consumer role, when accessing the API, then only published metrics (not raw commercial data) are returned

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-010: Food Category Configuration

**Description**: The system must allow administrators to configure monitored food categories, including risk indicators, thresholds, data source mappings, and alert rules.

**Relates To**: BR-001, FR-002

**Acceptance Criteria**:

- [ ] Given admin permissions, when creating a new food category, then risk indicators and thresholds can be configured through a UI
- [ ] Given a food category configuration change, when saved, then the change takes effect within the next data processing cycle
- [ ] Given the UK food consumption classification, when configuring categories, then alignment with ONS food categories is enforced

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**: The platform must deliver responsive user experience under expected load conditions.

- Dashboard page load time: < 3 seconds (95th percentile)
- API response time: < 500ms (95th percentile)
- Risk score recalculation: < 15 minutes from data receipt
- Report generation: < 2 minutes for standard SitRep

**Measurement Method**: Application Performance Monitoring (APM) tooling in production

**Load Conditions**:

- Peak load: 200 concurrent users (during a supply crisis)
- Average load: 50 concurrent users, 100 API calls/minute
- Data volume: 500,000 supply chain events per day at full scale

**Priority**: HIGH

---

#### NFR-P-2: Throughput

**Requirement**: System must process 500,000 supply chain events per day at full scale, with capacity to handle 3x surge during crisis periods.

**Scalability**: Must scale horizontally to support 1.5M events/day within 30 minutes of demand increase.

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: System must achieve 99.5% uptime (operational dashboard tier per ARC-000-PRIN-v1.0 Principle 16).

- Maximum planned downtime: 4 hours/month for maintenance (outside business hours)
- Maximum unplanned downtime: 43.8 hours/year

**Maintenance Windows**: Weekends 02:00-06:00 GMT

**Priority**: HIGH

---

#### NFR-A-2: Disaster Recovery

**RPO (Recovery Point Objective)**: Maximum acceptable data loss = 1 hour

**RTO (Recovery Time Objective)**: Maximum acceptable downtime = 4 hours

**Backup Requirements**:

- Backup frequency: Hourly incremental, daily full
- Backup retention: 90 days
- Geographic backup location: Secondary UK region

**Failover Requirements**:

- Automatic failover to secondary availability zone: YES
- Failover time: < 15 minutes

**Priority**: HIGH

---

#### NFR-A-3: Fault Tolerance

**Requirement**: System must gracefully degrade when external data feeds or downstream systems fail.

**Resilience Patterns Required**:

- [x] Circuit breaker for external data feeds
- [x] Retry with exponential backoff for transient data source failures
- [x] Timeout on all network calls (30 seconds maximum)
- [x] Bulkhead isolation between data ingestion and user-facing services
- [x] Graceful degradation: dashboards show last-known-good data with staleness warnings

**Priority**: HIGH

---

### Security Requirements

#### NFR-SEC-1: Authentication

**Requirement**: All users must authenticate via DEFRA Azure AD SSO with SAML 2.0. FSA users authenticate via FSA Azure AD with federated trust.

**Multi-Factor Authentication (MFA)**:

- Required for: All users (DEFRA policy), crisis response functions, admin functions
- MFA methods: Microsoft Authenticator, hardware security keys

**Session Management**:

- Session timeout: 30 minutes of inactivity
- Absolute session timeout: 8 hours
- Re-authentication required for: SitRep approval, data export, admin functions

**Priority**: CRITICAL

---

#### NFR-SEC-2: Authorisation

**Requirement**: Role-based access control (RBAC) with data-level access restrictions to protect commercially sensitive data.

**Roles and Permissions**:

| Role | Dashboard | Raw Data | Commercial Data | Alerts | Admin | API |
|------|-----------|----------|-----------------|--------|-------|-----|
| Policy Analyst | Yes | Aggregated | No | Read | No | No |
| FSA Officer | Yes | Food safety relevant | No | Read/Respond | No | No |
| Crisis Coordinator | Yes | Aggregated | No | Full | No | No |
| Data Engineer | Yes | Yes | Yes | Read | Yes | No |
| SIRO/CDO | Yes | Aggregated | Summary | Read | Read | No |
| API Consumer | No | No | No | No | No | Published metrics |

**Priority**: CRITICAL

---

#### NFR-SEC-3: Data Encryption

**Requirement**:

- Data in transit: TLS 1.3 for all connections
- Data at rest: AES-256 encryption for all data stores
- Key management: Cloud provider KMS with DEFRA-controlled keys

**Encryption Scope**:

- [x] Database encryption at rest
- [x] Backup encryption
- [x] File storage encryption
- [x] Application-level field encryption for commercially sensitive data fields

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: Data Privacy Compliance

**Applicable Regulations**: UK GDPR, Data Protection Act 2018, Freedom of Information Act 2000

**Compliance Requirements**:

- [x] Limited personal data processing (platform primarily handles commercial/operational data)
- [x] FOI exemption assessment for commercially sensitive supply chain data (s.43 FOIA 2000)
- [x] Data Protection Impact Assessment (DPIA) for any personal data elements
- [x] Data sharing agreements with all commercial data providers

**Data Residency**: All data stored within UK sovereign data centres

**Data Retention**: Supply chain event data retained for 5 years; audit logs retained for 7 years

**Priority**: CRITICAL

---

#### NFR-C-2: Audit Logging

**Requirement**: Comprehensive audit trail for compliance and forensics.

**Audit Log Contents**:

- Who: User identity (authenticated principal)
- What: Action performed (data access, alert response, configuration change)
- When: Timestamp (UTC, millisecond precision)
- Where: System component and data source
- Why: Request context (correlation ID, session ID)
- Result: Success/failure with error details

**Log Retention**: 7 years for compliance logs (immutable storage)

**Log Integrity**: Tamper-evident logging with cryptographic hashing

**Priority**: CRITICAL

---

### Usability Requirements

#### NFR-U-1: User Experience

**Requirement**: System must be usable by policy analysts with medium technical proficiency without specialist training.

**UX Standards**:

- Consistent with GOV.UK Design System
- Accessibility: WCAG 2.2 Level AA compliance (ARC-000-PRIN-v1.0 Principle 2)
- Responsive design for tablet use during crisis meetings
- Browser support: Chrome, Firefox, Edge (last 2 versions)

**User Onboarding**: Interactive guided tour for new users, contextual help on dashboards

**Priority**: HIGH

---

#### NFR-U-2: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance (mandatory per ARC-000-PRIN-v1.0 Principle 2 and Public Sector Bodies Accessibility Regulations 2018).

**Accessibility Features**:

- [x] Keyboard navigation for all functions
- [x] Screen reader compatibility (JAWS, NVDA)
- [x] High contrast mode
- [x] Adjustable font sizes
- [x] Alt text for all data visualisations
- [x] Colour-blind-friendly chart palettes

**Testing**: Automated accessibility testing in CI/CD + manual testing with assistive technologies

**Priority**: CRITICAL

---

### Maintainability and Supportability Requirements

#### NFR-M-1: Observability

**Requirement**: Comprehensive instrumentation for monitoring and troubleshooting (ARC-000-PRIN-v1.0 Principle 7).

**Telemetry Requirements**:

- **Logging**: Structured JSON logs with correlation IDs, centralised aggregation
- **Metrics**: RED metrics (Rate, Errors, Duration) for all services
- **Tracing**: Distributed tracing with OpenTelemetry across data ingestion pipeline
- **Dashboards**: Real-time operational dashboards for data feed health, risk scores, user activity
- **Alerts**: SLO-based alerting with runbooks for data feed failures, performance degradation

**Priority**: HIGH

---

## Integration Requirements

### External System Integrations

#### INT-001: National Food Strategy Dashboard API (Project 005)

**Purpose**: Publish supply chain risk metrics for the National Food Strategy Dashboard.

**Integration Type**: Real-time API (RESTful)

**Data Exchanged**:

- **From Platform to Dashboard**: Supply chain risk scores, food category status, alert summaries, trend data
- **From Dashboard to Platform**: None (one-way data flow)

**Integration Pattern**: Request/response (REST API with API key authentication)

**Authentication**: OAuth 2.0 client credentials

**Error Handling**: Retry with exponential backoff, circuit breaker at consumer

**SLA**: < 500ms response time, > 99.5% availability

**Owner**: Cabinet Office Food Strategy Unit

**Priority**: MUST_HAVE

---

#### INT-002: FSA Food Surveillance System

**Purpose**: Share food safety-relevant supply chain alerts and data with the FSA's existing surveillance platform.

**Integration Type**: Event-driven (pub/sub)

**Data Exchanged**:

- **From Platform to FSA**: Food safety alerts, supply disruption events with safety implications
- **From FSA to Platform**: Food safety incident data, inspection outcomes (for correlation)

**Integration Pattern**: Pub/sub with message queue

**Authentication**: Mutual TLS between DEFRA and FSA environments

**Error Handling**: Dead letter queue, manual review for failed deliveries

**SLA**: < 30 minutes delivery latency, guaranteed delivery

**Owner**: FSA Digital Team

**Priority**: MUST_HAVE

---

#### INT-003: HMRC Border Force Import Data

**Purpose**: Ingest import declaration volumes and SPS check outcomes from Border Control Posts.

**Integration Type**: Batch file transfer (daily) with near-real-time event feed for high-priority corridors

**Data Exchanged**:

- **From Border Force to Platform**: Import declaration counts by commodity code, SPS check pass/fail rates, port-of-entry volumes
- **From Platform to Border Force**: None

**Integration Pattern**: SFTP file transfer (batch), API webhook (real-time)

**Authentication**: API key + IP allowlisting

**SLA**: Daily batch by 06:00 GMT; real-time feed < 2 hours latency

**Owner**: HMRC Border Force IT

**Priority**: SHOULD_HAVE

---

#### INT-004: Retailer Data Feeds

**Purpose**: Ingest stock levels, sales velocity, and supply chain status from major UK retailers.

**Integration Type**: Near-real-time API push (webhook) or scheduled API pull

**Data Exchanged**:

- **From Retailers to Platform**: Aggregated stock levels, sales-to-forecast ratios, supply disruption flags, depot stock days
- **From Platform to Retailers**: Aggregated industry benchmarks (anonymised, opt-in)

**Integration Pattern**: Webhook (push) or scheduled poll (pull), retailer choice

**Authentication**: OAuth 2.0 per data sharing agreement

**Error Handling**: Retry with exponential backoff, data quality quarantine

**SLA**: Data freshness < 4 hours, agreed per data sharing agreement

**Owner**: Individual retailer IT teams

**Priority**: MUST_HAVE

---

#### INT-005: GOV.UK Notify

**Purpose**: Send alert notifications (email, SMS) to stakeholders.

**Integration Type**: Real-time API

**Data Exchanged**:

- **From Platform to Notify**: Notification requests (alert content, recipient lists)
- **From Notify to Platform**: Delivery status callbacks

**Integration Pattern**: REST API

**Authentication**: API key

**SLA**: < 5 minutes delivery for critical alerts

**Owner**: DEFRA Digital

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Supply Chain Event

**Description**: An observation of supply chain status from a data provider at a point in time.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| event_id | UUID | Yes | Unique identifier | Primary key |
| provider_id | UUID | Yes | Data provider reference | Foreign key |
| food_category_id | UUID | Yes | Food category reference | Foreign key |
| event_type | Enum | Yes | Type of observation | ['stock_level', 'import_volume', 'disruption_flag', 'quality_indicator'] |
| value | Decimal | Yes | Numeric value of observation | Non-negative |
| unit | String(50) | Yes | Unit of measurement | Standardised units |
| timestamp | Timestamp | Yes | When the observation was made | UTC, indexed |
| received_at | Timestamp | Yes | When the platform received it | UTC, indexed |
| data_quality_score | Decimal | No | Automated quality assessment | 0.0-1.0 |

**Data Volume**: 500,000 events/day at full scale (Year 1: 100,000/day)

**Data Classification**: OFFICIAL-SENSITIVE (commercially sensitive)

**Data Retention**: 5 years

---

#### Entity 2: Food Category

**Description**: A classification of food types aligned with ONS food consumption categories.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| category_id | UUID | Yes | Unique identifier | Primary key |
| name | String(255) | Yes | Category name | Unique |
| ons_code | String(20) | No | ONS classification code | Indexed |
| risk_score | Decimal | No | Current risk score | 0-100 |
| monitoring_status | Enum | Yes | Whether actively monitored | ['active', 'inactive', 'pending'] |

**Data Volume**: ~200 categories

**Data Classification**: OFFICIAL

---

#### Entity 3: Risk Alert

**Description**: A system-generated alert when supply chain risk indicators breach thresholds.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| alert_id | UUID | Yes | Unique identifier | Primary key |
| food_category_id | UUID | Yes | Affected food category | Foreign key |
| severity | Enum | Yes | Alert severity | ['critical', 'high', 'medium', 'low'] |
| risk_score | Decimal | Yes | Risk score at time of alert | 0-100 |
| trigger_indicators | JSON | Yes | Indicators that triggered alert | Structured JSON |
| status | Enum | Yes | Alert lifecycle status | ['active', 'acknowledged', 'resolved', 'dismissed'] |
| created_at | Timestamp | Yes | Alert creation time | UTC |
| acknowledged_by | UUID | No | User who acknowledged | Foreign key |
| acknowledged_at | Timestamp | No | Acknowledgement time | UTC |

**Data Volume**: ~50 alerts/day at full scale

**Data Classification**: OFFICIAL

---

### Data Quality Requirements

**Data Accuracy**: Each data provider's feed validated against agreed schema; anomaly detection for outlier values (> 3 standard deviations from rolling average flagged for review).

**Data Completeness**: Minimum 90% completeness threshold per data feed per day; feeds below threshold flagged on data quality dashboard.

**Data Consistency**: Cross-source reconciliation for overlapping data points (e.g., import volumes from Border Force vs. retailer import receipts).

**Data Timeliness**: Data freshness SLA defined per provider in data sharing agreement; default < 4 hours.

**Data Lineage**: Full source-to-platform lineage tracked for every data point, enabling audit of any risk score back to contributing raw data.

---

### Data Migration Requirements

**Migration Scope**: No legacy system migration. The platform is a new capability. Historical data from DEFRA spreadsheets and FSA reports may be bulk-loaded for baseline establishment.

**Migration Strategy**: Phased data provider onboarding (3 retailers in Phase 1, remaining in Phase 2).

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must deploy to DEFRA's approved cloud environment (currently AWS GovCloud or Azure UK Government regions).

**TC-2**: Must integrate with DEFRA Azure AD for user authentication (no alternative identity provider).

**TC-3**: Must use GOV.UK Notify for citizen-facing notifications (TCoP requirement).

**TC-4**: All data must reside within UK sovereign data centres (ARC-000-PRIN-v1.0 Principle 8).

---

### Business Constraints

**BC-1**: Total programme budget capped at £12M over 3 years (2025 Spending Review allocation).

**BC-2**: Must pass GDS Service Standard assessment at Alpha and Beta stages before proceeding.

**BC-3**: Data sharing agreements with at least 3 major retailers must be signed before Beta.

**BC-4**: Must not duplicate functionality already provided by the FSA's Food Surveillance System.

---

### Assumptions

**A-1**: Major retailers will agree to voluntary data sharing under appropriate legal protections (risk: if they refuse, regulatory powers under the Agriculture Act 2020 may be needed, adding 6-12 months).

**A-2**: HMRC Border Force can provide import data feeds within the required latency (risk: their systems may not support near-real-time export).

**A-3**: DEFRA Azure AD federation with FSA Azure AD is technically feasible for cross-organisation SSO.

**A-4**: The National Food Strategy Dashboard (Project 005) API specification will be agreed by Q2 2027.

**Validation Plan**: Each assumption validated during Discovery/Alpha phase with technical spikes and stakeholder engagement.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Supply chain coverage (% by volume) | 0% | > 60% | Q4 2027 | Platform telemetry vs ONS data |
| Crisis detection time | 3-7 days | < 4 hours | Q4 2027 | Time from event to alert |
| Ministerial briefing preparation time | 5+ days | < 2 hours | Q4 2027 | Process timing logs |
| Active data providers connected | 0 | 50+ | Q4 2028 | Provider registry |
| Policy analyst platform adoption | 0% | 90% | Q2 2028 | Active user analytics |

---

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.5% | Uptime monitoring |
| API response time (p95) | < 500ms | APM tooling |
| Data ingestion latency (p95) | < 4 hours | Pipeline metrics |
| Error rate | < 0.5% | Log aggregation |
| Data feed health (% feeds active) | > 95% | Feed monitoring dashboard |

---

### User Adoption Metrics

| Metric | Target | Timeline | Measurement Method |
|--------|--------|----------|-------------------|
| Active DEFRA analyst users | 40 users | 6 months post-launch | Analytics platform |
| Active FSA users | 15 users | 6 months post-launch | Analytics platform |
| Self-service queries per week | 200+ | 12 months post-launch | Usage analytics |
| User satisfaction score | > 7/10 | Ongoing | Quarterly user surveys |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| Data sharing agreements | Signed agreements with at least 3 major retailers | DEFRA Legal | Q2 2027 | At Risk | HIGH - no retailer data without agreements |
| Border Force data feed | HMRC technical capability to provide import data | HMRC Border Force IT | Q3 2027 | On Track | MEDIUM - can proceed without but reduced coverage |
| FSA system integration | Technical integration with FSA Food Surveillance System | FSA Digital | Q3 2027 | On Track | MEDIUM - manual workaround possible |
| Project 005 API spec | Agreed API specification for National Food Strategy Dashboard | Cabinet Office | Q2 2027 | On Track | LOW - can publish provisional API |
| GDS Alpha assessment | Pass GDS Service Standard Alpha assessment | CDDO | Q4 2026 | On Track | HIGH - cannot proceed to Beta without pass |

---

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Major retailers refuse voluntary data sharing | MEDIUM | HIGH | Prepare regulatory fallback under Agriculture Act 2020; demonstrate mutual benefit through industry advisory panel | SRO |
| R-2 | Data quality from heterogeneous sources is too poor for reliable risk scoring | MEDIUM | HIGH | Implement robust data quality monitoring; phased onboarding with quality gates; invest in data cleansing pipeline | CDO |
| R-3 | Platform fails to detect a real supply disruption, damaging credibility | LOW | HIGH | Extensive testing with historical crisis data; phased rollout alongside existing manual processes; parallel running period | SRO |
| R-4 | Commercially sensitive data breached, destroying industry trust | LOW | CRITICAL | Defence-in-depth security; field-level encryption for commercial data; regular penetration testing; FOI exemption framework | SIRO |
| R-5 | Cross-departmental data governance complexity delays integration | MEDIUM | MEDIUM | Early engagement with Cabinet Office and FSA data governance boards; pre-agreed data sharing protocols | CDO |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Data Granularity vs Commercial Confidentiality

**Conflicting Requirements**:

- **Requirement A**: FR-001/BR-001 - Ingest granular supply chain data for accurate risk scoring
- **Requirement B**: BR-005/NFR-SEC-2 - Protect commercially sensitive data from competitor access and FOI disclosure

**Stakeholders Involved**:

- **Policy Analysts (SD-5)**: Want granular data for accurate analysis
- **Retailers (SD-9)**: Will only share data if competitive information is protected

**Resolution Strategy**: PHASE

**Decision**: Implement tiered data access model. Raw commercial data is ingested and used for risk scoring algorithms but is never directly visible to users. Analysts see aggregated, anonymised outputs. Risk scores are derived indicators, not raw commercial data.

**Impact on Requirements**:

- **Modified**: FR-003 (dashboard shows aggregated data, not raw feeds)
- **Added**: FR-009 with data-level access restrictions
- **Added**: NFR-SEC-2 with per-role data visibility matrix

---

### Conflict C-2: Real-Time Ambition vs Data Provider Readiness

**Conflicting Requirements**:

- **Requirement A**: BR-001 - Near-real-time monitoring (< 4 hours)
- **Requirement B**: Practical constraint - many data providers can only supply daily batch files

**Stakeholders Involved**:

- **Minister (SD-1)**: Wants real-time crisis visibility
- **Retailers/Border Force**: Cannot provide real-time data feeds in Phase 1

**Resolution Strategy**: PHASE

**Decision**: Phase 1 accepts daily batch for most providers with near-real-time for 3 pilot retailers. Phase 2 transitions remaining providers to near-real-time. Risk scoring adjusts confidence levels based on data freshness.

**Impact on Requirements**:

- **Modified**: BR-001 success criteria phased (Phase 1: < 24 hours, Phase 2: < 4 hours)
- **Added**: FR-002 includes data freshness as factor in risk score confidence

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Discovery Complete | User research, problem validation, options analysis | Q3 2026 | Budget approval |
| Alpha Assessment (GDS) | Demonstrate prototype solving user needs | Q4 2026 | Discovery findings |
| Beta Start | Begin building production service | Q1 2027 | Alpha assessment pass |
| 3 Retailers Connected | First data providers live | Q2 2027 | Data sharing agreements |
| Beta Assessment (GDS) | Demonstrate working service with real users | Q3 2027 | Beta development |
| Public Beta (Limited) | Service available to expanded user group | Q4 2027 | Beta assessment pass |
| Live Assessment (GDS) | Full service assessment | Q1 2028 | Public Beta |
| Full Scale Operations | 50+ data providers, all food categories | Q4 2028 | Provider onboarding |

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Alpha + Beta) | £4.5M | 15-person multidisciplinary team, 18 months |
| Infrastructure (3 years) | £1.8M | Cloud hosting, scaling for production |
| Data acquisition | £2.0M | Commercial data licensing, API access fees |
| Security and compliance | £0.8M | Penetration testing, DPIA, accreditation |
| Training and change management | £0.4M | Analyst training, user onboarding |
| Contingency (20%) | £2.5M | Risk buffer |
| **Total** | **£12.0M** | Over 3 years, within SR25 allocation |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Infrastructure | £0.6M/year | Cloud hosting, scaling |
| Data licensing | £0.7M/year | Ongoing commercial data fees |
| Support team | £0.5M/year | 2nd/3rd line support, on-call |
| **Total** | **£1.8M/year** | From Year 4 onwards |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| CDO | Enterprise Architect | [ ] Approved | PENDING | |
| FSA Head of Surveillance | Co-User Representative | [ ] Approved | PENDING | |
| SIRO | Information Risk | [ ] Approved | PENDING | |
| CDDO | Standards Assurance | [ ] Approved | PENDING | |

### Sign-Off

By signing below, stakeholders confirm that requirements are complete, understood, and approved to proceed to design phase.

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, Food Resilience Programme | _________ | PENDING |
| CDO, DEFRA | _________ | PENDING |
| FSA Head of Surveillance | _________ | PENDING |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| BCP | Border Control Post -- designated point of entry for SPS checks |
| SPS | Sanitary and Phytosanitary -- border checks for food, plant, and animal health |
| FOI/FOIA | Freedom of Information Act 2000 |
| SitRep | Situation Report -- standardised crisis briefing document |
| GDS | Government Digital Service |
| CDDO | Central Digital and Data Office |
| FSA | Food Standards Agency |
| ONS | Office for National Statistics |
| TCoP | Technology Code of Practice |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Architecture Principles
- ARC-001-STKE-v1.0 -- Food Supply Chain Resilience Platform Stakeholder Analysis
- UK Food Security Report (Agriculture Act 2020, Section 19)
- Government Food Strategy 2022
- GDS Service Standard (14 points)
- Technology Code of Practice (12 points)

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Food Supply Chain Resilience Platform
**Model**: Claude Opus 4.6
