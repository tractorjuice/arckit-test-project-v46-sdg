# UK Government Enterprise Architecture Principles — SDG 11: Sustainable Cities and Communities

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | SDG 11: Sustainable Cities and Communities — Cross-Project Governance (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Chief Architect, SDG 11 Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | All SDG 11 project teams, Enterprise Architecture Review Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the mandatory architecture principles governing all technology decisions across the SDG 11: Sustainable Cities and Communities programme. These principles apply to five UK Government digital services:

- **001** — Smart City IoT Platform (DLUHC)
- **002** — Urban Planning Analytics (DLUHC)
- **003** — Public Transport Optimisation (DfT)
- **004** — Heritage Asset Management (DCMS)
- **005** — Air Quality Monitoring Network (DEFRA)

**Scope**: All technology projects, systems, and initiatives within the SDG 11 programme
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the formal exception process (Section VI)

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

**Governing Context**: These principles align with the GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Essentials Plus, UK GDPR, Data Protection Act 2018, Public Sector Bodies Accessibility Regulations 2018, and domain-specific standards including ETSI EN 303 645 (IoT security), INSPIRE Directive (geospatial data), Bus Open Data Service (BODS), and Clean Air Framework Directive 2008/50/EC.

---

## I. Strategic Principles

### 1. Citizen-Centred Urban Design

**Principle Statement**:
All systems MUST be designed around the needs of urban residents, commuters, heritage visitors, and communities affected by air quality, with services that are inclusive, transparent, and respectful of citizen autonomy in public spaces.

**Rationale**:
The citizens served by SDG 11 programmes interact with cities daily — commuters navigating transport networks, residents affected by air pollution, communities living near heritage sites, planners shaping neighbourhoods. Systems that collect data in public spaces or influence urban decisions carry a particular obligation to be transparent and accountable. The GDS Service Standard mandates user-centred design, and the smart cities context adds obligations around surveillance ethics, environmental justice, and community participation in planning decisions.

**Implications**:

- Conduct user research with diverse urban populations including disabled residents, elderly, digitally excluded communities, and non-English speakers
- Design for assisted digital journeys — not all residents can interact with smart city dashboards or planning portals
- Meet accessibility standards (WCAG 2.2 Level AA minimum) as a legal requirement
- Provide clear information to citizens about what sensor data is collected in public spaces and why
- Support community participation in planning processes through multiple channels
- Use plain language for air quality alerts, planning notifications, and transport information

**Validation Gates**:

- [ ] User research conducted with representative urban populations including vulnerable groups
- [ ] Accessibility audit passed at WCAG 2.2 Level AA
- [ ] Privacy impact of public-space data collection communicated to citizens
- [ ] Community engagement mechanisms tested with diverse demographic groups
- [ ] Service assessed against GDS Service Standard points 1–3

---

### 2. IoT Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All IoT devices, sensor networks, and edge computing infrastructure MUST comply with ETSI EN 303 645 baseline security requirements. Connected devices in public infrastructure are critical national assets and MUST be secured against compromise from day one.

**Rationale**:
Smart city sensor networks deployed across urban environments — traffic sensors, air quality monitors, environmental detectors — represent a large attack surface. Compromised IoT devices can be weaponised in botnets, provide false data leading to dangerous decisions (e.g., incorrect air quality readings suppressing health warnings), or be used as pivot points into wider government networks. The Product Security and Telecommunications Infrastructure Act 2022 and ETSI EN 303 645 set baseline requirements.

**Mandatory Controls**:

- [ ] No universal default passwords — each device has a unique credential
- [ ] Software update mechanism with integrity verification for all deployed devices
- [ ] Secure boot and firmware validation to prevent tampering
- [ ] Encrypted communication between devices and gateways (TLS 1.3 minimum)
- [ ] Device identity management with certificate-based authentication
- [ ] Vulnerability disclosure policy published for all IoT components
- [ ] Hardware security modules or secure enclaves for cryptographic key storage where feasible
- [ ] Network segmentation isolating IoT traffic from corporate and citizen-facing networks
- [ ] Device lifecycle management including secure decommissioning and data wiping

**Compliance Frameworks**:

- ETSI EN 303 645 (IoT Cyber Security)
- Product Security and Telecommunications Infrastructure Act 2022
- NCSC Secure by Design
- NCSC Connected Places Cyber Security Principles
- DCMS Code of Practice for Consumer IoT Security

**Exceptions**:

- NONE. IoT security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:

- [ ] ETSI EN 303 645 compliance assessment completed for all device types
- [ ] Penetration testing performed on IoT infrastructure before deployment
- [ ] Device inventory maintained with firmware version tracking
- [ ] Incident response plan covers IoT-specific scenarios (device compromise, data poisoning)
- [ ] Supply chain security assessed for all IoT hardware vendors

---

### 3. Geospatial Data Interoperability

**Principle Statement**:
All systems handling location data MUST use open geospatial standards and MUST be interoperable with Ordnance Survey, INSPIRE, and cross-government spatial data infrastructure.

**Rationale**:
Every project in the SDG 11 programme is inherently spatial — sensor locations, planning boundaries, transport routes, heritage site coordinates, air quality monitoring stations. Geospatial data locked in proprietary formats or incompatible coordinate systems prevents the joined-up urban analysis that makes smart cities work. The INSPIRE Directive (retained in UK law post-Brexit), Ordnance Survey data standards, and the Geospatial Commission's strategy mandate interoperability.

**Implications**:

- Use OGC standards for data exchange: GeoJSON, GML, WFS, WMS, WMTS
- Reference Ordnance Survey National Grid (OSGB36/EPSG:27700) and WGS84 (EPSG:4326) coordinate systems with documented transformation parameters
- Publish spatial data as INSPIRE-compliant metadata through data.gov.uk
- Use Unique Property Reference Numbers (UPRNs) and Unique Street Reference Numbers (USRNs) for address and street referencing
- Adopt the British National Grid for internal spatial analysis
- Support Open Geospatial Consortium API standards for web service interfaces
- Integrate with the National Underground Asset Register (NUAR) where infrastructure data is relevant

**Validation Gates**:

- [ ] All spatial data published using OGC-compliant formats
- [ ] Coordinate reference systems documented with transformation approach
- [ ] INSPIRE metadata published for applicable datasets
- [ ] UPRN/USRN referencing used for address and street data
- [ ] Interoperability tested with Ordnance Survey and data.gov.uk infrastructure

---

### 4. Open Data for Planning and Transparency

**Principle Statement**:
All non-personal urban data SHOULD be published as open data by default, enabling democratic scrutiny of planning decisions, transport performance, heritage conservation, and environmental quality.

**Rationale**:
Open data underpins democratic accountability in urban governance. Citizens have a right to understand air quality in their neighbourhood, transport performance affecting their commute, planning applications near their homes, and the condition of heritage assets in their community. The Technology Code of Practice mandates open data publication, and sector-specific regulations (BODS for transport, AURN for air quality) require real-time data publication. Open data also enables third-party innovation — independent air quality apps, community planning tools, and heritage tourism services.

**Implications**:

- Publish non-personal data under the Open Government Licence (OGL) via data.gov.uk
- Use machine-readable formats (CSV, JSON, GeoJSON) with persistent URIs
- Provide real-time data feeds where applicable (transport, air quality) via APIs
- Comply with Bus Open Data Service (BODS) requirements for transport data
- Publish planning application data in structured formats per MHCLG data standards
- Maintain a public data catalogue with discovery metadata
- Apply statistical disclosure control to prevent re-identification of individuals from aggregated data

**Validation Gates**:

- [ ] Non-personal datasets identified and published on data.gov.uk
- [ ] Real-time feeds available for time-sensitive data (transport, air quality)
- [ ] Data published under OGL with clear licensing
- [ ] Machine-readable formats used with documented schemas
- [ ] Statistical disclosure control applied to aggregated data

---

### 5. Defence-in-Depth Security (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement from day one across all layers from IoT edge to cloud.

**Rationale**:
SDG 11 systems handle diverse sensitive data — citizen location patterns from transport, personal planning objections, heritage asset vulnerability assessments, and health-related air quality exposure data. The smart city context adds unique risks: sensor networks in public spaces, edge computing nodes in street furniture, and real-time data streams that could reveal population movement patterns. NCSC Connected Places guidance specifically addresses cyber security for smart city infrastructure.

**Zero Trust Pillars**:

1. **Identity-Based Access**: No network-based trust; every request from every device authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest without exception, including IoT telemetry
4. **Continuous Verification**: Monitor, log, and analyse all access patterns for anomalies across cloud and edge

**Mandatory Controls**:

- [ ] Multi-factor authentication for all staff and administrative access
- [ ] Service-to-service authentication using mutual authentication or signed tokens
- [ ] Secrets managed via a dedicated secrets management solution (never in code, config, or firmware)
- [ ] Network segmentation with IoT, corporate, and citizen-facing zones isolated
- [ ] Encryption at rest for all data stores containing personal or sensitive data
- [ ] Encrypted transport for all network communication including sensor telemetry
- [ ] Structured, immutable audit logging of all authentication and authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning, IoT firmware analysis)

**Compliance Frameworks**:

- NCSC Cyber Essentials Plus
- NCSC Secure by Design
- NCSC Connected Places Cyber Security Principles
- UK GDPR and Data Protection Act 2018
- HMG Security Policy Framework
- OWASP Top 10 and OWASP IoT Top 10

**Exceptions**:

- NONE. Security principles are non-negotiable.

**Validation Gates**:

- [ ] Threat model completed for each service including IoT attack vectors
- [ ] Security controls mapped to requirements and compliance obligations
- [ ] Penetration testing completed including IoT and edge infrastructure
- [ ] Incident response runbook created with defined escalation paths
- [ ] NCSC Connected Places assessment completed for smart city components

---

### 6. Scalability for Urban-Scale Sensor Networks

**Principle Statement**:
All systems MUST be designed to handle the data volumes, velocity, and variety generated by city-scale sensor networks, with the ability to dynamically scale from pilot deployments to full metropolitan coverage.

**Rationale**:
Smart city deployments scale dramatically — from 100 sensors in a pilot borough to 100,000+ across a metropolitan area. Air quality monitoring generates continuous time-series data from hundreds of stations. Transport systems process millions of passenger journeys daily. Systems must handle this growth without re-architecture, and must accommodate burst patterns (rush hour, pollution events, planning consultation deadlines).

**Implications**:

- Design for horizontal scaling with stateless processing of sensor telemetry
- Implement time-series data storage optimised for high-volume ingest and fast aggregation queries
- Support edge computing to pre-process data at source, reducing bandwidth and latency
- Plan for data volumes of 100,000+ sensor readings per minute at full deployment
- Implement data tiering: hot (real-time alerts), warm (recent analytics), cold (historical archive)
- Use message queuing or event streaming for decoupled sensor data ingestion
- Capacity plan for seasonal and event-driven spikes (transport disruption, pollution episodes)

**Validation Gates**:

- [ ] System tested at projected full-scale deployment volumes (100K+ sensors)
- [ ] Edge processing strategy defined to reduce central processing load
- [ ] Time-series data storage benchmarked for ingest and query performance
- [ ] Auto-scaling configured and tested for burst scenarios
- [ ] Data tiering strategy implemented with defined retention per tier

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning across distributed IoT, edge, and cloud infrastructure.

**Rationale**:
Smart city systems are inherently distributed — sensors in street furniture, edge gateways in cabinets, cloud processing, and citizen-facing dashboards. Observability must span this entire chain. A failed air quality sensor providing stale data could suppress health warnings. An undetected transport data feed failure could cause journey planners to route passengers incorrectly.

**Telemetry Requirements**:

- **Logging**: Structured logs with correlation IDs for end-to-end tracing from sensor to dashboard
- **Metrics**: Device health, data freshness, processing latency, error rates, data quality scores
- **Tracing**: Distributed trace context propagated from edge ingestion to API response
- **Alerting**: SLO-based alerting with runbooks for sensor failures, data staleness, and processing delays

**Required Instrumentation**:

- Device connectivity status and last-seen timestamps for all IoT endpoints
- Data freshness metrics per sensor and per data stream
- Processing pipeline throughput and latency at each stage
- Business metrics (sensors reporting, air quality alerts issued, transport feeds active)
- Security events (device authentication failures, anomalous data patterns)

**Log Retention**:

- **Security/audit logs**: Minimum 2 years (aligned with UK Government retention standards)
- **Sensor telemetry**: 90 days hot, 2 years warm, 7 years cold archive for regulatory compliance
- **Application logs**: 90 days minimum for troubleshooting

**Validation Gates**:

- [ ] End-to-end observability from IoT device to citizen-facing interface
- [ ] Device health dashboards configured with automated alerting on connectivity loss
- [ ] Data freshness SLOs defined per data stream with alerting on staleness
- [ ] Runbooks created for common IoT failure scenarios (device offline, data drift, gateway failure)
- [ ] Capacity planning metrics tracked and reviewed monthly

---

## II. Data Principles

### 8. Data Sovereignty and Governance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and departmental data governance policies, with particular attention to the privacy implications of urban sensor data.

**Rationale**:
Smart city sensors can incidentally capture personal data — transport ticketing data reveals travel patterns, air quality sensors with cameras can capture images, and aggregated sensor data at sufficient granularity can reveal individual behaviour. Data governance must be rigorous, with clear classification of what constitutes personal data in the urban sensing context.

**Data Classification Tiers**:

1. **OFFICIAL**: Aggregated urban statistics, published open data, planning application metadata
2. **OFFICIAL-SENSITIVE**: Granular location data, individual transport journeys, planning objection details, heritage vulnerability assessments
3. **SECRET**: Not expected in this programme; escalate if identified

**Data Residency**:

- All personal data MUST reside within UK sovereign data centres
- IoT telemetry containing location data MUST be processed within UK jurisdiction
- Cross-departmental data sharing MUST be governed by data sharing agreements compliant with the Digital Economy Act 2017 where applicable
- Edge processing nodes MUST NOT transmit unprocessed sensor data outside UK networks

**Data Retention**:

- Retention periods defined per data category aligned with departmental retention schedules and environmental monitoring regulations
- Air quality data retained for minimum 5 years per Clean Air Framework requirements
- Transport data retained per DfT data management standards
- Automatic deletion or anonymisation after the defined retention period expires
- Heritage records maintained as permanent public records where applicable

**Validation Gates**:

- [ ] Data classification performed for all sensor data types, distinguishing personal from non-personal
- [ ] UK residency confirmed for all personal data storage and processing
- [ ] Retention policies configured with sector-specific requirements (environmental, transport, heritage)
- [ ] Data sharing agreements in place for all cross-departmental data flows
- [ ] Data Protection Impact Assessment completed for all services processing personal data

---

### 9. Privacy by Design in Public Spaces

**Principle Statement**:
All systems collecting data in public spaces MUST embed privacy protections from the outset, minimising personal data collection and implementing privacy-preserving techniques for urban analytics.

**Rationale**:
Smart city sensors operate in public spaces where citizens cannot opt out of the physical environment. This creates a heightened obligation to minimise personal data collection and implement privacy-preserving analytics. UK GDPR Article 25 mandates data protection by design, and the Information Commissioner has issued specific guidance on surveillance and smart cities.

**Implications**:

- Implement data minimisation at the sensor level — capture only what is needed for the stated purpose
- Use privacy-preserving techniques: aggregation at source, differential privacy, k-anonymity for location data
- No persistent tracking of individuals through sensor networks unless explicitly authorised (e.g., Automatic Number Plate Recognition under specific legal powers)
- Publish clear signage and digital notices informing the public about sensor data collection
- Support data subject rights: access, rectification, erasure where data is identifiable
- Conduct surveillance camera assessment per Surveillance Camera Code of Practice where applicable
- Implement data minimisation for transport ticketing — journey analytics should not require individual tracking

**Validation Gates**:

- [ ] Data Protection Impact Assessment (DPIA) completed for each service involving public-space sensing
- [ ] Privacy-preserving analytics techniques implemented (aggregation, differential privacy)
- [ ] Public notification mechanisms in place for sensor-equipped areas
- [ ] No persistent individual tracking without explicit legal basis documented
- [ ] Surveillance Camera Commissioner Code of Practice compliance assessed where applicable

---

### 10. Data Quality and Environmental Accuracy

**Principle Statement**:
Data pipelines MUST maintain data quality standards appropriate to the decisions they inform, with particular rigour for environmental measurements that trigger public health actions.

**Rationale**:
Air quality readings that trigger health warnings must be accurate — false positives cause unnecessary alarm, false negatives suppress life-saving warnings. Transport data informing journey planning must be timely — stale data sends passengers to cancelled services. Planning data must be complete — missing heritage constraints lead to unlawful demolition of listed buildings. Data quality is not abstract; it has direct consequences for public health and safety.

**Quality Standards**:

- **Completeness**: No unexpected gaps in time-series sensor data; gap-filling algorithms documented and validated
- **Accuracy**: Environmental sensors calibrated to MCERTS (Monitoring Certification Scheme) standards where applicable
- **Consistency**: Cross-sensor validation for overlapping measurement areas
- **Timeliness**: Data freshness SLAs defined per use case (real-time for alerts, hourly for analytics, daily for reporting)
- **Traceability**: Sensor calibration records, data processing algorithms, and quality flags maintained

**Lineage Requirements**:

- Source-to-dashboard lineage documented for all data flows
- Transformation and aggregation logic version-controlled and auditable
- Data quality metrics tracked per sensor, per pipeline, with alerting on degradation
- Impact analysis capability for sensor decommissioning or algorithm changes

**Validation Gates**:

- [ ] Sensor calibration procedures documented and schedules maintained
- [ ] Data quality scores published per data stream
- [ ] Gap-filling and interpolation algorithms documented with uncertainty quantification
- [ ] MCERTS compliance verified for regulatory environmental monitoring stations
- [ ] Data contracts defined between sensor networks and consuming applications

---

### 11. Single Source of Truth for Urban Data

**Principle Statement**:
Every spatial and reference data domain MUST have a single authoritative source. Urban data shared across multiple projects MUST reference common registers and avoid duplication.

**Rationale**:
Five projects sharing urban data creates high risk of inconsistency. A road closure known to the transport system but not the air quality system leads to incorrect pollution modelling. A heritage listing recorded in DCMS systems but not reflected in planning data leads to planning approvals that damage listed buildings. Authoritative sources must be unambiguous.

**Implications**:

- Use Ordnance Survey MasterMap as the authoritative spatial base layer
- Reference the National Heritage List for England (NHLE) as the authoritative source for listed buildings and scheduled monuments
- Use DEFRA's AURN network as the authoritative source for reference-grade air quality measurements
- Adopt NaPTAN (National Public Transport Access Nodes) as the authoritative stop/station reference
- Derived or cached copies clearly labelled with source attribution and freshness
- Avoid bidirectional synchronisation between projects — one project owns each data domain

**Validation Gates**:

- [ ] System of record identified and documented for each data domain
- [ ] Authoritative government registers referenced (OS, NHLE, AURN, NaPTAN)
- [ ] Derived copies documented with synchronisation frequency and acceptable staleness
- [ ] No bidirectional sync without documented conflict resolution strategy
- [ ] Master data management approach defined for shared reference data (e.g., geographic boundaries, organisation codes)

---

## III. Integration Principles

### 12. Transport Data Standards Compliance

**Principle Statement**:
All systems handling public transport data MUST comply with mandatory UK transport data standards including BODS, GTFS, SIRI, and NaPTAN, enabling interoperability with journey planners, accessibility tools, and transport operators.

**Rationale**:
The Bus Services Act 2017 and subsequent regulations mandate the publication of transport data through the Bus Open Data Service (BODS). The DfT requires local authorities and operators to publish timetable, fares, and real-time data in specified formats. Non-compliance is a regulatory breach, and poor transport data excludes passengers from making informed travel choices.

**Implications**:

- Publish timetable data in TransXChange format via BODS
- Publish real-time vehicle location and prediction data in SIRI-VM and GTFS-RT formats
- Use NaPTAN codes for all stop and station references
- Publish fares data in NeTEx format as required by BODS
- Support multi-modal journey planning through standardised data exchange
- Maintain ATCO codes for transport operators and services
- Comply with DfT's Accessible Information Regulations for real-time passenger information

**Validation Gates**:

- [ ] BODS compliance verified for all published transport datasets
- [ ] Real-time feeds published in SIRI-VM or GTFS-RT format
- [ ] NaPTAN references used for all stops and stations
- [ ] Fares data published in NeTEx format where required
- [ ] DfT transport data quality dashboard showing compliance scores

---

### 13. Loose Coupling Across Urban Domains

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, enabling independent evolution of transport, planning, heritage, air quality, and IoT domains without creating cascading dependencies.

**Rationale**:
The SDG 11 programme spans five projects across four departments (DLUHC, DfT, DCMS, DEFRA). Each team must develop, deploy, and evolve their service independently. A transport data format change must not break the air quality modelling pipeline. A heritage database migration must not disrupt the planning system. Cross-domain integration must be resilient to the pace differences between departments.

**Implications**:

- Communicate through published APIs or asynchronous events — never through shared databases
- Each project manages its own data lifecycle and data store
- Define clear domain boundaries: transport, planning, heritage, air quality, IoT infrastructure
- Use event-driven patterns for cross-domain notifications (e.g., road closure affecting air quality model)
- Interface contracts owned by the producing team with consumer input on design
- Avoid distributed transactions across departmental boundaries

**Validation Gates**:

- [ ] All inter-project communication uses APIs or events, not direct data store access
- [ ] No shared mutable state across project boundaries
- [ ] Each project has independent data stores and deployment pipelines
- [ ] Deployment of one project does not require simultaneous deployment of another
- [ ] Interface contracts documented with versioning and backward compatibility guarantees

---

### 14. Event-Driven Urban Data Integration

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for cross-domain data flows, enabling real-time urban intelligence without tight coupling between transport, environment, planning, and heritage systems.

**Rationale**:
Urban events cascade across domains — a traffic incident affects air quality, a major planning development affects transport capacity, a pollution episode triggers heritage protection measures. Event-driven integration enables these cross-domain reactions without requiring each system to poll others or maintain synchronous connections to departments with different operational rhythms.

**When to Use Asynchronous Patterns**:

- Cross-departmental event notification (e.g., road closure from DfT to DEFRA air quality model)
- Sensor data streaming from IoT platform to consuming applications
- Planning application notifications to heritage and transport consultees
- Air quality threshold exceedance alerts to public health and transport systems

**When Synchronous Communication is Acceptable**:

- Real-time citizen queries (journey planning, air quality check, planning search)
- Read-only reference data lookups (heritage listing status, NaPTAN stop details)
- User authentication and authorisation flows

**Validation Gates**:

- [ ] Event-driven patterns used for all cross-departmental data flows
- [ ] Event schemas versioned and published in a shared catalogue
- [ ] Message durability and delivery guarantees defined (at-least-once minimum)
- [ ] Dead letter handling and error recovery procedures documented
- [ ] Event replay capability available for disaster recovery and debugging

---

## IV. Quality Attributes

### 15. Performance for Real-Time Urban Services

**Principle Statement**:
All citizen-facing systems MUST meet defined performance targets, with particular attention to real-time services where latency affects safety (air quality alerts) and usability (journey planning).

**Rationale**:
Urban citizens need fast answers — a commuter checking bus times at a cold bus stop, a parent checking air quality before taking children to the park, a planner reviewing heritage constraints during a site visit. Slow systems waste citizens' time and, for air quality alerts, can have health consequences. Many users access services on mobile devices with variable connectivity.

**Performance Targets** (to be defined per service):

- **Air quality alerts**: End-to-end from sensor reading to citizen notification < 5 minutes
- **Journey planning queries**: API response < 500ms at p95
- **Planning application search**: Page load < 2 seconds at p95
- **IoT telemetry ingestion**: Sensor-to-storage latency < 30 seconds at p99
- **Heritage asset search**: Full-text and spatial query response < 1 second at p95

**Implications**:

- Performance requirements informed by user research and safety analysis
- Load testing performed before production deployment at projected scale
- Optimise for mobile users on variable connectivity (progressive loading, offline capability)
- Edge caching for frequently-accessed spatial data and reference layers
- Continuous performance monitoring with alerting on degradation

**Validation Gates**:

- [ ] Performance targets defined per service with safety-critical thresholds identified
- [ ] Load testing performed at projected full-scale deployment
- [ ] Mobile performance tested on representative devices and network conditions
- [ ] Continuous monitoring with alerting on SLO breaches
- [ ] Capacity planning model reviewed quarterly

---

### 16. Availability for Critical Urban Infrastructure

**Principle Statement**:
All systems MUST meet defined availability targets reflecting their criticality to public safety, transport operations, and regulatory compliance.

**Rationale**:
Air quality monitoring feeds into public health warnings — unavailability means citizens are not warned of dangerous pollution. Transport data feeds journey planners used by millions daily — unavailability causes passenger confusion and overcrowding. Heritage and planning systems have statutory consultation deadlines — unavailability can delay development or allow unlawful works to proceed.

**Availability Targets** (defined by service criticality):

- **Air quality monitoring and alerts**: 99.95% (critical public health function, 4.4 hours downtime/year max)
- **Transport real-time feeds**: 99.9% (high-impact passenger information, 8.7 hours downtime/year max)
- **IoT platform core**: 99.9% (sensor data ingestion must be continuous)
- **Planning portal**: 99.5% (statutory deadlines, but not safety-critical)
- **Heritage database**: 99.5% (reference service, not real-time critical)

**High Availability Patterns**:

- Redundancy across multiple availability zones for all citizen-facing services
- Automated health checks and self-healing for IoT gateway infrastructure
- Active-active configurations for air quality alerting pipeline
- Regular disaster recovery testing (at least annually, quarterly for safety-critical services)

**Validation Gates**:

- [ ] Availability SLAs defined per service based on safety and citizen impact assessment
- [ ] RTO and RPO requirements documented and achievable with current architecture
- [ ] Redundancy strategy implemented and tested for safety-critical services
- [ ] Failover tested regularly with documented results
- [ ] DR procedures validated including IoT infrastructure recovery

---

### 17. Accessibility and Digital Inclusion

**Principle Statement**:
All citizen-facing systems MUST meet WCAG 2.2 Level AA as a minimum and MUST be designed to be usable by the widest possible range of urban residents, including those with limited digital access, disabilities, and language barriers.

**Rationale**:
The Public Sector Bodies Accessibility Regulations 2018 make WCAG 2.2 Level AA a legal requirement. Urban services must reach everyone — the elderly resident checking air quality, the wheelchair user planning an accessible journey, the non-English speaker submitting a planning objection. Environmental justice requires that air quality information reaches the communities most affected by pollution, who are disproportionately from disadvantaged backgrounds.

**Implications**:

- Design using progressive enhancement — core functionality works without JavaScript
- Provide air quality information in multiple languages for diverse urban communities
- Ensure transport information is accessible to screen reader users and those with cognitive disabilities
- Support accessible formats for planning documents (not just PDFs)
- Publish accessibility statements for each service
- Test with assistive technologies including screen readers, voice control, and switch access

**Validation Gates**:

- [ ] WCAG 2.2 Level AA compliance verified through automated and manual testing
- [ ] Tested with at least two assistive technologies
- [ ] Keyboard-only navigation tested for all user journeys
- [ ] Multi-language support assessed for communities most affected by environmental inequality
- [ ] Accessibility statements published and maintained

---

### 18. Maintainability and Policy Adaptability

**Principle Statement**:
All systems MUST be designed for change, with business rules externalised to accommodate evolving planning policy, transport regulations, heritage listing criteria, and air quality standards without requiring system re-architecture.

**Rationale**:
Urban policy changes frequently — National Planning Policy Framework (NPPF) revisions, new Clean Air Zone regulations, updated heritage listing criteria, transport accessibility requirements. Systems must accommodate these policy changes through configuration rather than code changes. Staff turnover across government departments also means systems must be understandable by new team members.

**Implications**:

- Externalise environmental thresholds (air quality limit values, noise levels) as configuration
- Externalise planning policy rules so NPPF changes do not require code deployment
- Externalise heritage listing criteria and conservation area boundaries as reference data
- Modular architecture with clear separation between policy logic and platform infrastructure
- Architecture Decision Records (ADRs) for all significant technical choices
- Automated testing sufficient to validate policy rule changes without regression

**Validation Gates**:

- [ ] Environmental thresholds and policy rules externalised as configuration
- [ ] Policy change scenarios tested (e.g., new air quality limit value, NPPF amendment)
- [ ] Module boundaries defined with clear responsibilities
- [ ] ADRs document key design choices
- [ ] Business rule changes achievable without full system redeployment

---

## V. Development Practices

### 19. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines, including IoT device provisioning and edge computing configuration.

**Rationale**:
Smart city infrastructure includes cloud services, edge gateways, and IoT device fleets. Manual configuration of thousands of devices is error-prone and unauditable. Infrastructure as Code enables repeatable deployment, consistent configuration across device fleets, and rapid disaster recovery for distributed urban infrastructure.

**Implications**:

- All cloud infrastructure defined in declarative code within version control
- IoT device provisioning automated with fleet management tooling
- Edge gateway configuration managed as code with automated deployment
- Infrastructure changes go through code review before deployment
- No manual changes to production infrastructure or device configuration

**Validation Gates**:

- [ ] Cloud infrastructure defined as code in version control
- [ ] IoT device provisioning automated and repeatable
- [ ] Edge gateway configuration version-controlled
- [ ] No manual infrastructure changes in production (enforced, not just policy)
- [ ] Disaster recovery tested through infrastructure rebuild from code

---

### 20. Automated Testing Across the Stack

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment, including IoT firmware, edge processing logic, cloud services, and citizen-facing interfaces.

**Rationale**:
Defects in smart city systems have direct consequences — incorrect air quality readings suppress health warnings, faulty transport algorithms strand passengers, planning system errors allow unlawful development. Testing must cover the full stack from device firmware to user interface, with particular attention to data accuracy in environmental measurement pipelines.

**Test Pyramid**:

- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test sensor-to-cloud data flows and cross-service interactions (15–20%)
- **End-to-End Tests**: Critical citizen journeys and safety-critical alert paths (5–10%)

**Required Test Types**:

- Functional tests (correct data processing, accurate calculations)
- Data accuracy tests (sensor calibration validation, algorithm correctness)
- Accessibility tests (automated WCAG checks in CI/CD pipeline)
- Performance tests (latency under load, data ingestion throughput)
- Security tests (IoT firmware analysis, API penetration testing)
- Regression tests for policy rule changes

**Validation Gates**:

- [ ] Automated tests exist and pass before code is merged
- [ ] Test coverage meets defined thresholds per service
- [ ] Safety-critical alert paths have end-to-end tests
- [ ] Data accuracy tests validate sensor processing pipelines
- [ ] Security and accessibility tests run in CI/CD pipeline

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
- [ ] Risk assessment including impact on citizens and public safety if the principle is not met
- [ ] Expiration date — all exceptions are time-bound (maximum 12 months)
- [ ] Remediation plan with milestones to achieve full compliance

**Approval Process**:

1. Submit exception request to Enterprise Architecture team with supporting evidence
2. Review by Architecture Review Board (within 10 working days)
3. CTO/CIO approval required for exceptions to IoT Security by Design (Principle 2) or Defence-in-Depth Security (Principle 5)
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
- [ ] Data classification and privacy approach defined (Principles 8, 9)
- [ ] IoT security approach defined (Principle 2)

**Beta/Design**:

- [ ] Detailed architecture documented with traceability to principles
- [ ] Compliance with each principle validated through design review
- [ ] Exceptions requested, assessed, and approved where needed
- [ ] Security threat model completed including IoT attack vectors (Principles 2, 5)
- [ ] Geospatial interoperability validated (Principle 3)
- [ ] Transport data standards compliance verified (Principle 12)
- [ ] Accessibility approach validated (Principle 17)

**Pre-Production / Live Assessment**:

- [ ] Implementation matches approved architecture
- [ ] All validation gates passed for applicable principles
- [ ] Operational readiness verified (observability, runbooks, DR testing)
- [ ] GDS Service Standard assessment passed
- [ ] Penetration testing completed including IoT infrastructure
- [ ] ETSI EN 303 645 compliance verified for deployed IoT devices

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
| 1 | Citizen-Centred Urban Design | Strategic | CRITICAL | User research, accessibility audit, GDS assessment |
| 2 | IoT Security by Design | Strategic | CRITICAL | ETSI EN 303 645, pen testing, firmware analysis |
| 3 | Geospatial Data Interoperability | Strategic | HIGH | OGC standards, INSPIRE metadata, UPRN/USRN |
| 4 | Open Data for Planning and Transparency | Strategic | HIGH | data.gov.uk publication, OGL, machine-readable formats |
| 5 | Defence-in-Depth Security | Strategic | CRITICAL | Threat model, pen testing, NCSC Connected Places |
| 6 | Scalability for Urban-Scale Sensor Networks | Strategic | HIGH | Load testing at 100K+ sensors, auto-scaling |
| 7 | Observability and Operational Excellence | Strategic | HIGH | End-to-end monitoring, device health dashboards |
| 8 | Data Sovereignty and Governance | Data | CRITICAL | UK residency, classification, retention policies |
| 9 | Privacy by Design in Public Spaces | Data | CRITICAL | DPIA, aggregation at source, public notification |
| 10 | Data Quality and Environmental Accuracy | Data | CRITICAL | MCERTS calibration, quality scores, lineage |
| 11 | Single Source of Truth for Urban Data | Data | HIGH | OS, NHLE, AURN, NaPTAN references |
| 12 | Transport Data Standards Compliance | Integration | HIGH | BODS, GTFS-RT, SIRI-VM, NaPTAN |
| 13 | Loose Coupling Across Urban Domains | Integration | HIGH | Deployment independence, no shared databases |
| 14 | Event-Driven Urban Data Integration | Integration | MEDIUM | Async patterns for cross-departmental flows |
| 15 | Performance for Real-Time Urban Services | Quality | HIGH | Latency targets, mobile testing |
| 16 | Availability for Critical Urban Infrastructure | Quality | CRITICAL | SLA monitoring, DR testing |
| 17 | Accessibility and Digital Inclusion | Quality | CRITICAL | WCAG 2.2 AA, multi-language, assistive tech |
| 18 | Maintainability and Policy Adaptability | Quality | MEDIUM | Externalised rules, ADRs, policy change testing |
| 19 | Infrastructure as Code | Development | HIGH | IaC coverage, IoT provisioning automated |
| 20 | Automated Testing Across the Stack | Development | HIGH | Full-stack testing, data accuracy validation |

### Alignment to UK Government Frameworks

| Framework | Relevant Principles |
|-----------|-------------------|
| GDS Service Standard | 1 (Citizen-Centred), 4 (Open Data), 17 (Accessibility) |
| Technology Code of Practice | 3 (Geospatial Interoperability), 4 (Open Data), 5 (Security), 13 (Loose Coupling) |
| NCSC Secure by Design | 2 (IoT Security), 5 (Defence-in-Depth), 19 (IaC), 20 (Testing) |
| NCSC Connected Places | 2 (IoT Security), 5 (Defence-in-Depth), 9 (Privacy in Public Spaces) |
| UK GDPR / DPA 2018 | 8 (Data Sovereignty), 9 (Privacy by Design), 10 (Data Quality) |
| Public Sector Accessibility Regulations | 1 (Citizen-Centred), 17 (Accessibility and Inclusion) |
| INSPIRE Directive | 3 (Geospatial Interoperability), 4 (Open Data) |
| ETSI EN 303 645 | 2 (IoT Security by Design) |
| Clean Air Framework Directive | 10 (Data Quality), 16 (Availability) |
| Bus Services Act 2017 / BODS | 12 (Transport Data Standards) |
| NPPF | 4 (Open Data for Planning), 18 (Policy Adaptability) |
| HM Treasury Green Book | 6 (Scalability), 15 (Performance), 16 (Availability) |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |
| Technology Code of Practice | Standard | GOV.UK | Open standards, security, reuse | N/A — external reference |
| ETSI EN 303 645 | Standard | ETSI | IoT baseline security requirements | N/A — external reference |
| NCSC Connected Places | Guidance | NCSC | Smart city cyber security principles | N/A — external reference |
| INSPIRE Directive | Legislation | legislation.gov.uk | Geospatial data interoperability | N/A — external reference |
| BODS Technical Guidance | Standard | DfT | Bus open data publication requirements | N/A — external reference |
| MCERTS | Standard | Environment Agency | Environmental monitoring certification | N/A — external reference |
| UK GDPR | Legislation | legislation.gov.uk | Data protection requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility conformance criteria | N/A — external reference |
| NPPF | Policy | DLUHC | National planning policy framework | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: SDG 11: Sustainable Cities and Communities — Cross-Project Governance (Project 000)
**Model**: Claude Opus 4.6
