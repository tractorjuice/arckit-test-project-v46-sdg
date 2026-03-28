# Project Requirements: Innovation Funding Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Innovation Funding Platform (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Innovation Funding Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Innovation Funding Programme Board, UKRI Digital, Research Council CEOs |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Innovation Funding Platform — a modern grants application and portfolio management system replacing the legacy Je-S (Joint Electronic Submission) system for UKRI's seven Research Councils and Innovate UK.

---

## Executive Summary

### Business Context

UKRI distributes approximately GBP 8 billion annually in research and innovation funding through seven Research Councils and Innovate UK. The legacy Je-S system — the primary application platform for over a decade — is universally regarded as inadequate: researchers rate it 2.1/5.0, application preparation takes 30-40 hours with an estimated 15-20 hours wasted on system friction, and the platform cannot provide cross-council portfolio analytics that UKRI needs for Treasury spending reviews.

The Innovation Funding Platform will replace Je-S with a modern, user-centred grants application service that dramatically reduces researcher administrative burden, enables council-specific funding scheme configuration, integrates with institutional research management systems, and provides portfolio analytics across all UKRI funding.

### Objectives

- Replace Je-S with a modern, accessible grants application platform
- Reduce researcher application preparation time by 40%
- Enable cross-council portfolio analytics for spending review evidence
- Integrate with institutional research management systems (Pure, Symplectic, Worktribe)
- Support all seven Research Council funding schemes through configurable workflows

### Expected Outcomes

- Researcher satisfaction increase from 2.1/5.0 to 4.0/5.0
- 500,000 researcher-hours per year recovered (GBP 25M equivalent)
- Treasury portfolio queries answered within 24 hours (vs 2-4 weeks)
- Application completion rates improved by 20%
- Integration with top 50 universities' research management systems

### Project Scope

**In Scope**:

- Grant application submission (all UKRI funding schemes)
- Peer review management and assignment
- Grant award and post-award management
- Full Economic Costing (fEC) integration
- ORCID integration for researcher identification
- Cross-council portfolio analytics and reporting
- Institutional API integration (Pure, Symplectic, Worktribe)
- Research output tracking (publications, datasets, impact)
- Council-specific scheme configuration

**Out of Scope**:

- Financial payments processing (separate finance system)
- PhD studentship management (separate DTP/CDT systems)
- Innovate UK commercial grant processes (future phase — different regulatory framework)
- Historical Je-S data migration beyond active grants (archive access provided separately)
- Research ethics approval processes (institutional responsibility)

---

## Business Requirements

### BR-001: Modern Grant Application Experience

**Description**: The platform must provide a grant application experience rated >4.0/5.0 by researchers, with auto-save, profile reuse, ORCID integration, and intuitive navigation.

**Rationale**: Je-S satisfaction is 2.1/5.0. Poor UX wastes researcher time, reduces application quality, and damages UK research competitiveness. Researchers in competitor nations (US NSF, EU ERC) use significantly better systems.

**Success Criteria**:

- Researcher satisfaction score >4.0/5.0 (survey at submission)
- Application preparation time reduced by 40%
- Application completion rate >90% (vs current ~75%)
- Zero reported data loss incidents

**Priority**: MUST_HAVE

**Stakeholder**: Researchers, UKRI CEO

---

### BR-002: Council-Specific Scheme Configuration

**Description**: The platform must support all current UKRI funding schemes across seven Research Councils through configuration rather than custom code, enabling councils to define their own application forms, review criteria, and workflow stages.

**Rationale**: Each Research Council has evolved domain-specific processes. Forcing homogenisation reduces assessment quality. The platform must be flexible enough for EPSRC's large consortium applications and MRC's clinical trial costing while maintaining a consistent core experience.

**Success Criteria**:

- All current UKRI funding schemes configurable on the platform
- New scheme creation in <5 working days without code changes
- Council-specific terminology and branding supported
- Cross-council reporting maintained despite scheme diversity

**Priority**: MUST_HAVE

**Stakeholder**: Research Council CEOs

---

### BR-003: Cross-Council Portfolio Analytics

**Description**: The platform must provide analytics showing UKRI's research portfolio across all councils by theme, institution, researcher, geographic region, and impact area.

**Rationale**: UKRI cannot currently answer Treasury cross-council questions quickly. Spending review responses take 2-4 weeks of manual data collection. This undermines UKRI's case for funding protection.

**Success Criteria**:

- Cross-council portfolio dashboards available to UKRI leadership
- Treasury spending review queries answerable within 24 hours
- Trend analysis: funding by theme, institution, and region over time
- Research output and impact tracking linked to grants

**Priority**: MUST_HAVE

**Stakeholder**: UKRI CEO, DSIT, HM Treasury

---

### BR-004: Institutional Integration

**Description**: The platform must integrate with institutional research management systems via API to enable auto-population of applicant data, institutional costing, and post-award reporting.

**Rationale**: Researchers and research offices currently re-key data between institutional systems and Je-S. This wastes an estimated 2-3 FTE per large university and introduces data entry errors in costing.

**Success Criteria**:

- API integration with Pure, Symplectic, and Worktribe
- ORCID-based researcher profile auto-population
- fEC costing data exchange with institutional finance systems
- At least 50 universities with active API integration within 18 months

**Priority**: SHOULD_HAVE

**Stakeholder**: University Research Offices, Russell Group

---

## Functional Requirements

### User Personas

#### Persona 1: Principal Investigator (Researcher)

- **Role**: Academic submitting grant applications
- **Goals**: Submit high-quality applications with minimum administrative burden
- **Pain Points**: Je-S is slow, loses data, incompatible with modern browsers, cannot reuse previous application data
- **Technical Proficiency**: Low-Medium (focus is research, not IT)

#### Persona 2: Research Council Programme Manager

- **Role**: Manages funding calls, reviews, and awards for a Research Council
- **Goals**: Run funding rounds efficiently; assign reviewers; manage panels; issue awards
- **Pain Points**: Manual reviewer assignment; poor integration with panel meetings; limited analytics
- **Technical Proficiency**: Medium

#### Persona 3: Peer Reviewer

- **Role**: Academic reviewing grant applications
- **Goals**: Review applications efficiently; provide fair, constructive feedback
- **Pain Points**: Je-S review interface is poor; no offline access; conflict of interest management is manual
- **Technical Proficiency**: Low-Medium

#### Persona 4: University Research Office Administrator

- **Role**: Supports researchers with application preparation, costing, and compliance
- **Goals**: Ensure applications meet fEC requirements; institutional approvals; post-award reporting
- **Pain Points**: Duplicate data entry between institutional systems and Je-S; manual fEC transfer
- **Technical Proficiency**: Medium

#### Persona 5: UKRI Portfolio Analyst

- **Role**: Produces cross-council portfolio analysis for UKRI leadership and Treasury
- **Goals**: Answer funding distribution questions quickly; identify trends and gaps
- **Pain Points**: Data locked in council-specific silos; manual data collection takes weeks
- **Technical Proficiency**: High

---

### Functional Requirements Detail

#### FR-001: Application Form Builder

**Description**: The system must provide a configurable form builder enabling Research Council programme managers to create application forms for new funding schemes without developer involvement.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Drag-and-drop form builder with standard field types (text, number, date, file upload, table, budget)
- [ ] Conditional logic: show/hide sections based on answers
- [ ] Custom validation rules per field
- [ ] Template library of common form sections (Case for Support, Pathways to Impact, Data Management Plan)
- [ ] Preview and test mode before scheme publication
- [ ] Scheme creation achievable in <5 working days

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: ORCID Integration

**Description**: The system must integrate with ORCID to auto-populate researcher profiles, link publications and grants, and provide persistent researcher identification across applications.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] Researchers authenticate/link ORCID during registration
- [ ] Auto-populate: name, affiliation, publication list, previous grants from ORCID record
- [ ] Sync publications and outputs bidirectionally (with researcher consent)
- [ ] Use ORCID as persistent identifier across all UKRI applications
- [ ] Support ORCID API v3.0

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-003: Auto-Save and Draft Management

**Description**: The system must automatically save application progress every 30 seconds and maintain draft versions accessible from any device.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Auto-save every 30 seconds with visual confirmation
- [ ] Draft accessible from any device after login
- [ ] Version history: last 10 auto-save points recoverable
- [ ] Offline capability: work offline and sync when connected (progressive web app)
- [ ] No data loss under any failure scenario (network dropout, browser crash, session timeout)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-004: Full Economic Costing (fEC) Integration

**Description**: The system must support Full Economic Costing data entry and calculation, with API integration to institutional finance systems for automatic cost population.

**Relates To**: BR-001, BR-004

**Acceptance Criteria**:

- [ ] fEC cost categories: Directly Incurred, Directly Allocated, Indirect, Exceptions
- [ ] Staff cost calculation with FTE, salary scale, and increment date
- [ ] Equipment, travel, and consumables cost entry
- [ ] API for institutional finance systems to push cost data
- [ ] Automatic calculation of fEC total and UKRI contribution (typically 80%)
- [ ] Estate and indirect cost rates auto-populated from institutional data

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-005: Peer Review Management

**Description**: The system must support the full peer review lifecycle: reviewer identification, invitation, assignment, conflict of interest management, review submission, and panel coordination.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Reviewer database searchable by expertise, availability, and review history
- [ ] Automated conflict of interest detection (co-author, same institution, recent collaboration)
- [ ] Reviewer invitation with accept/decline workflow
- [ ] Review form configurable per scheme (assessment criteria, scoring scales)
- [ ] Panel meeting support: agenda generation, score aggregation, ranking
- [ ] Reviewer performance tracking (response time, quality scores)

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-006: Cross-Council Portfolio Dashboard

**Description**: The system must provide portfolio analytics dashboards showing funding distribution across councils, themes, institutions, and regions.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Dashboard: total funding by council, year, and funding scheme
- [ ] Geographic distribution: funding by region, constituency, and institution
- [ ] Thematic analysis: funding by research theme (cross-council classification)
- [ ] Researcher demographics: career stage, gender, ethnicity (aggregated, anonymised)
- [ ] Research output tracking: publications, citations, impact case studies linked to grants
- [ ] Export: CSV, Excel, PDF for Treasury submissions
- [ ] Drill-down from aggregate to individual grant level

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-007: Application Reuse and Templates

**Description**: The system must allow researchers to reuse sections from previous applications and save personal templates for common application components.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Import sections from previous applications (own applications only)
- [ ] Personal template library for common components (CV, track record, data management plan)
- [ ] Institutional template library (shared by research office)
- [ ] Auto-populate applicant details from ORCID profile and previous applications
- [ ] Clear indication of reused vs new content

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-008: Research Output Tracking

**Description**: The system must track research outputs (publications, datasets, software, patents, impact case studies) linked to funded grants using persistent identifiers (DOI, ORCID).

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Link publications to grants using DOI
- [ ] Link datasets to grants using DOI (DataCite)
- [ ] Auto-discover outputs via Crossref, DataCite, and Europe PMC APIs
- [ ] Researcher self-report for non-indexed outputs
- [ ] Impact narrative capture for REF impact case study preparation
- [ ] Output metrics: citations, downloads, altmetrics

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Application Form Response Time

**Requirement**: Page load time <2 seconds (p95). Auto-save operation <1 second. Form submission <5 seconds including validation.

**Load Conditions**: 5,000 concurrent users during peak (funding deadline day). Average 500 concurrent users.

**Priority**: MUST_HAVE

---

#### NFR-P-002: Portfolio Analytics Query Time

**Requirement**: Standard portfolio dashboard queries <5 seconds. Complex cross-council ad-hoc queries <30 seconds.

**Priority**: SHOULD_HAVE

---

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.9% availability. 99.99% during funding submission deadline periods (final 48 hours of open calls).

**Priority**: MUST_HAVE

---

#### NFR-A-002: Disaster Recovery

**RPO**: 0 (zero data loss — auto-save data must survive any failure) | **RTO**: 1 hour

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: Federated authentication via institutional IdP (Shibboleth/SAML via UK Access Management Federation) plus ORCID. MFA required for programme managers and administrators.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Application Confidentiality

**Requirement**: Grant applications are confidential. Access restricted to: applicant, named co-investigators, institutional research office (with applicant consent), assigned reviewers (application sections only, not costing), council programme managers. Strict access logging.

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Reviewer Anonymity

**Requirement**: Reviewer identities are confidential to applicants. Reviewer comments and scores visible to programme managers and panel chairs only. Anonymised feedback returned to applicants.

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-001: UK GDPR Compliance

**Requirement**: DPIA completed. Privacy notices published. Researcher consent for ORCID data synchronisation. Right to erasure supported (with retention exceptions for audit requirements on funded grants).

**Priority**: MUST_HAVE

---

#### NFR-C-002: Equality and Diversity Monitoring

**Requirement**: Collect equality monitoring data (voluntary) at application. Data stored separately from application content. Never visible to reviewers. Used only for aggregated portfolio analytics.

**Priority**: MUST_HAVE

---

### Usability Requirements

#### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA. GDS service assessment pass. Usable by researchers with disabilities including visual impairment, motor impairment, and cognitive disabilities.

**Priority**: MUST_HAVE

---

#### NFR-U-002: Browser and Device Support

**Requirement**: Support latest 2 versions of Chrome, Firefox, Safari, Edge. Responsive design for tablet use. Progressive web app for offline capability.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: ORCID

**Purpose**: Researcher identification and profile auto-population

**Integration Type**: Real-time API (ORCID API v3.0)

**Data Exchanged**: Researcher profile, publications, affiliations, grants

**Authentication**: ORCID OAuth 2.0

**Priority**: MUST_HAVE

---

### INT-002: Research Management Systems (Pure, Symplectic, Worktribe)

**Purpose**: Institutional data exchange — researcher profiles, fEC costing, post-award reporting

**Integration Type**: Real-time API (REST)

**Data Exchanged**: Researcher profiles, fEC cost data, grant status updates, output data

**Authentication**: OAuth 2.0 with institutional credentials

**Priority**: SHOULD_HAVE

---

### INT-003: Crossref / DataCite / Europe PMC

**Purpose**: Research output discovery and linking

**Integration Type**: Real-time API

**Data Exchanged**: Publication metadata (DOI, title, authors, journal), dataset metadata, citation counts

**Authentication**: API key (Crossref, DataCite), open access (Europe PMC)

**Priority**: SHOULD_HAVE

---

### INT-004: UK Access Management Federation (Shibboleth)

**Purpose**: Federated authentication for university-based users

**Integration Type**: SAML 2.0 / OpenID Connect

**Data Exchanged**: Authentication assertion, institutional affiliation, email

**Authentication**: SAML 2.0 federation

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Grant Application

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| application_id | UUID | Yes | Unique application identifier |
| scheme_id | UUID | Yes | UKRI funding scheme |
| council | Enum | Yes | EPSRC, MRC, BBSRC, NERC, STFC, ESRC, AHRC |
| pi_orcid | String | Yes | Principal Investigator ORCID |
| title | String(500) | Yes | Application title |
| status | Enum | Yes | Draft, Submitted, In_Review, Funded, Rejected |
| submitted_date | Timestamp | No | Submission timestamp |
| fec_total | Decimal | No | Full Economic Cost total (GBP) |
| ukri_contribution | Decimal | No | UKRI funding requested (GBP) |

**Data Volume**: ~80,000 new applications per year, ~500,000 active grants

**Data Classification**: OFFICIAL-SENSITIVE (application content is confidential pre-award)

---

### Data Migration Requirements

**Migration Scope**: Active grants from Je-S (~150,000 records). Historical applications (read-only archive access).

**Migration Strategy**: Phased by Research Council, smallest first (AHRC, ESRC), largest last (EPSRC).

**Data Validation**: Parallel running — applications submitted on both systems compared for 3 months per council.

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Year 1-3) | GBP 18.0M | 35 FTE delivery team over 3 years |
| Infrastructure (Year 1-3) | GBP 3.0M | Cloud hosting, ORCID integration |
| Je-S data migration | GBP 2.0M | Data migration, parallel running |
| User research and GDS assessment | GBP 1.0M | Researcher engagement, accessibility |
| Security and compliance | GBP 0.5M | Pen testing, DPIA, accreditation |
| Training and change management | GBP 1.0M | University research offices, council staff |
| Contingency (15%) | GBP 3.8M | |
| **Total** | **GBP 29.3M** | Over 3 years |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Cloud infrastructure | GBP 1.5M | Including database, CDN, disaster recovery |
| BAU team | GBP 3.0M | 15 FTE |
| ORCID institutional membership | GBP 0.1M | Annual membership |
| Security monitoring | GBP 0.3M | SOC, vulnerability scanning |
| **Total** | **GBP 4.9M/year** | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-003-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | `projects/003-innovation-funding-platform/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Innovation Funding Platform (Project 003)
**Model**: Claude Opus 4.6
