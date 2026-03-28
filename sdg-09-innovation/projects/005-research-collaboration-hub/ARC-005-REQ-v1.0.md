# Project Requirements: Research Collaboration Hub

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Research Collaboration Hub (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Research Collaboration Hub Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Research Collaboration Programme Board, DSIT, UKRI, KTN |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the Research Collaboration Hub — a platform connecting UK research institutions with industry to accelerate knowledge transfer, collaborative R&D, and research commercialisation.

---

## Executive Summary

### Business Context

The UK ranks 4th globally for research quality but 10th for innovation output — a persistent "valley of death" between discovery and commercial application. Industry-academia collaboration is essential for translating publicly funded research into economic impact, but current mechanisms are fragmented: industry struggles to find relevant academic expertise, researchers lack industry connections, and university knowledge exchange offices operate in silos. SMEs are particularly underserved — lacking the networks and resources that large corporations use to engage universities.

The Research Collaboration Hub will provide an intelligent matchmaking platform connecting industry R&D challenges to academic expertise, with streamlined engagement processes that reduce the average time from initial enquiry to formal collaboration agreement from 6 months to 8 weeks.

### Objectives

- Build a comprehensive, searchable directory of UK research expertise
- Deliver AI-powered matchmaking between industry needs and academic capabilities
- Streamline the collaboration engagement process with standardised agreements
- Integrate with existing research systems (ORCID, Gateway to Research, institutional CRIS)
- Track collaboration outcomes to demonstrate impact and value for money

### Expected Outcomes

- 25% increase in university-industry collaborative R&D projects (15,000 to 18,750 per year)
- GBP 300-500M additional collaborative R&D expenditure per year
- Engagement time reduced from 6 months to 8 weeks
- 500 successful matches per quarter within 18 months
- SME participation rate >40% of industry engagements

### Project Scope

**In Scope**:

- Research expertise directory (auto-populated from ORCID, institutional CRIS, Gateway to Research)
- Industry R&D challenge posting and matching
- AI-powered matchmaking algorithms
- Standardised engagement templates (consultancy, sponsored research, licence)
- Collaboration workflow management (NDA, IP agreement, contract)
- Outcome tracking (publications, patents, spin-outs, revenue)
- FAIR-compliant research data discovery (metadata only, not data hosting)

**Out of Scope**:

- Financial transactions (contract management, not payments)
- Research data hosting (signpost to institutional repositories)
- IP valuation services (refer to specialist providers)
- Recruitment/PhD studentship matching
- Conference/event management

---

## Business Requirements

### BR-001: Research Expertise Discovery

**Description**: The platform must provide a comprehensive, searchable directory of UK research expertise covering 80% of active researchers, auto-populated from existing data sources.

**Rationale**: Industry cannot engage researchers they cannot find. Current discovery relies on personal networks, conference contacts, and Google Scholar searches — methods that systematically exclude researchers at less visible institutions and early-career researchers.

**Success Criteria**:

- 80% of active UK researchers (by publication output) with profiles
- Profile auto-population: <5 minutes for a researcher to have a basic profile
- Industry search satisfaction >4.0/5.0

**Priority**: MUST_HAVE

**Stakeholder**: DSIT, Industry, Researchers

---

### BR-002: Intelligent Matchmaking

**Description**: The platform must provide AI-powered matching of industry R&D challenges to relevant academic expertise, going beyond keyword search to understand research domains, capabilities, and collaboration potential.

**Rationale**: A directory alone is insufficient — industry users need proactive matching because they often cannot articulate their needs in academic terminology. Algorithmic matching plus human curation (via KTN) provides superior results.

**Success Criteria**:

- 500 successful matches per quarter (leading to formal engagement)
- Match relevance score >80% (industry user rates match as relevant)
- Matches include researchers from non-Russell Group universities in proportion to expertise

**Priority**: MUST_HAVE

**Stakeholder**: DSIT, Industry, KTN

---

### BR-003: Streamlined Engagement Process

**Description**: The platform must reduce the average time from initial industry enquiry to formal collaboration agreement from 6 months to 8 weeks through standardised templates, model contracts, and digital workflow support.

**Rationale**: Slow engagement processes cause SMEs to abandon university collaboration. IP negotiation alone typically takes 3 months. Standardised model agreements for common engagement types would dramatically accelerate the process.

**Success Criteria**:

- Average engagement time reduced from 6 months to 8 weeks
- Abandonment rate <20% (vs estimated >50% currently)
- SME participation rate >40% of industry engagements

**Priority**: SHOULD_HAVE

**Stakeholder**: Industry (SMEs), University Research Offices

---

### BR-004: Outcome Tracking and Impact Measurement

**Description**: The platform must track collaboration outcomes (publications, datasets, patents, spin-outs, commercial products, revenue) to demonstrate the impact and value for money of university-industry collaboration.

**Rationale**: DSIT and Treasury need evidence that investment in knowledge exchange infrastructure generates economic return. Outcome tracking also feeds into KEF and REF impact assessments.

**Success Criteria**:

- Collaboration outcomes tracked for >80% of platform-facilitated engagements
- Annual impact report publishable within 4 weeks of year-end
- Integration with HEBCIS return data for institutional reporting

**Priority**: SHOULD_HAVE

**Stakeholder**: DSIT, Research England, UKRI

---

## Functional Requirements

### User Personas

#### Persona 1: Industry R&D Manager (Large Corporate)

- **Role**: Seeks academic partners for specific R&D challenges
- **Goals**: Find top researchers in a specific domain; initiate collaboration quickly
- **Pain Points**: University websites are opaque; engagement processes are slow; IP terms unclear
- **Technical Proficiency**: Medium

#### Persona 2: SME Founder/CTO

- **Role**: Needs academic expertise to solve a specific technical problem
- **Goals**: Find a researcher who understands the problem; engage affordably and quickly
- **Pain Points**: Doesn't know where to start; university processes seem designed for large companies; cannot afford months of negotiation
- **Technical Proficiency**: Low-Medium

#### Persona 3: Academic Researcher

- **Role**: Open to industry collaboration but time-poor
- **Goals**: Be found by relevant industry partners; engage without excessive administration
- **Pain Points**: No time to maintain yet another profile; industry contacts are serendipitous, not systematic
- **Technical Proficiency**: Medium

#### Persona 4: University Knowledge Exchange Manager

- **Role**: Facilitates industry engagement for their institution
- **Goals**: Increase institutional KE metrics; manage IP and contracts; support researchers
- **Pain Points**: Reactive rather than proactive; limited visibility of industry demand; contract negotiation bottleneck
- **Technical Proficiency**: Medium

---

### Functional Requirements Detail

#### FR-001: Researcher Profile Auto-Population

**Description**: The system must auto-populate researcher profiles from ORCID, Gateway to Research (GtR), and institutional CRIS systems, requiring minimal manual input.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Import researcher data from ORCID (publications, affiliations, grants)
- [ ] Import grant data from Gateway to Research (UKRI-funded projects)
- [ ] Import institutional data from CRIS systems via API (where available)
- [ ] Generate research expertise tags using NLP analysis of publication abstracts
- [ ] Researcher can claim and edit their profile with one-click verification
- [ ] Profile usable within 5 minutes of ORCID authentication

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-002: Industry Challenge Posting

**Description**: The system must allow industry users to post R&D challenges describing their needs in business language, with guided categorisation to improve matching.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Guided challenge posting: problem description, domain, timeline, budget range, engagement type
- [ ] Natural language input with AI-assisted categorisation (industry terms mapped to research domains)
- [ ] Challenge visibility options: public, registered users only, or matched researchers only
- [ ] Challenge can be anonymous until industry user chooses to reveal identity
- [ ] Challenge expires after configurable period (default 90 days)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-003: AI-Powered Matchmaking Engine

**Description**: The system must match industry challenges to relevant researcher profiles using semantic analysis of research expertise, publication topics, and grant portfolios.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Semantic matching using NLP models trained on research abstracts and industry challenge descriptions
- [ ] Match quality score (0-100) indicating relevance confidence
- [ ] Matches consider: research topic relevance, industry collaboration history, geographic proximity (optional), capacity indicators
- [ ] Diversity: matches include researchers from diverse institutions, not just Russell Group
- [ ] Human override: KTN broker can curate and adjust matches
- [ ] Explainable matching: user can see why a match was suggested

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-004: Standardised Engagement Templates

**Description**: The system must provide model contract templates for common engagement types, pre-populated with standard terms.

**Relates To**: BR-003

**Acceptance Criteria**:

- [ ] Template library: consultancy agreement, sponsored research, collaborative R&D, licence, NDA
- [ ] SME-friendly terms: simplified language, shorter contracts, pre-agreed IP positions
- [ ] Lambert Toolkit integration: reference approved model agreements
- [ ] Digital signature support for faster execution
- [ ] Workflow: draft > institutional review > industry review > signed
- [ ] Average template-based agreement completion <8 weeks

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-005: Research Expertise Search

**Description**: The system must provide advanced search of research expertise by topic, institution, geographic region, and collaboration history.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Free-text search across researcher profiles, publications, and grants
- [ ] Filter by: institution, research council, geographic region, career stage, collaboration openness
- [ ] Search results ranked by relevance with match explanation
- [ ] Map view: geographic distribution of expertise
- [ ] Export search results as CSV for internal reporting

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Collaboration Outcome Tracking

**Description**: The system must track outcomes of platform-facilitated collaborations including publications, datasets, patents, spin-outs, and commercial products.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Link collaboration agreements to outcomes (publications via DOI, patents via patent number)
- [ ] Auto-discover publications linked to collaborations via Crossref/DataCite
- [ ] Manual outcome reporting for non-indexed outputs (commercial products, services)
- [ ] Annual impact dashboard: collaborations initiated, outcomes generated, economic value
- [ ] HEBCIS-compatible data export for institutional KE reporting

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Search Response Time

**Requirement**: Expertise search results returned in <3 seconds (p95). Matchmaking results for a posted challenge generated within 5 minutes.

**Load Conditions**: 1,000 concurrent users; 500 searches per hour peak

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-001: Availability Target

**Requirement**: 99.5% availability. No critical business processes dependent on real-time availability.

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Data Access Controls

**Requirement**: Two-tier profile model: public profile (published research, institutional affiliation) visible to all; gated profile (current projects, available IP, contact details) visible after registration and (optionally) NDA. Industry challenge details controlled by poster.

**Priority**: MUST_HAVE

---

#### NFR-SEC-002: Authentication

**Requirement**: Researchers authenticate via ORCID or institutional SSO (Shibboleth). Industry users authenticate via GOV.UK One Login or email verification with company domain check.

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-001: FAIR Data Principles

**Requirement**: All research metadata on the platform must comply with FAIR principles. Persistent identifiers (ORCID, DOI) used throughout. Machine-readable metadata in Dublin Core / DataCite formats.

**Priority**: MUST_HAVE

---

#### NFR-C-002: UK GDPR

**Requirement**: Researcher consent for profile population and visibility settings. Right to erasure supported. DPIA completed. Privacy notices published.

**Priority**: MUST_HAVE

---

### Usability Requirements

#### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA. GDS service assessment pass. Usable by industry users with low digital literacy.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: ORCID

**Purpose**: Researcher identification and profile auto-population

**Integration Type**: Real-time API (ORCID API v3.0)

**Priority**: MUST_HAVE

---

### INT-002: Gateway to Research (GtR)

**Purpose**: UKRI-funded grant data for researcher profiles

**Integration Type**: Real-time API

**Priority**: MUST_HAVE

---

### INT-003: Institutional CRIS Systems

**Purpose**: Institutional researcher data (where API available)

**Integration Type**: Real-time API (institution-by-institution)

**Priority**: SHOULD_HAVE

---

### INT-004: Crossref / DataCite

**Purpose**: Publication and dataset discovery for outcome tracking

**Integration Type**: Real-time API

**Priority**: SHOULD_HAVE

---

### INT-005: Knowledge Transfer Network (KTN) CRM

**Purpose**: Broker-curated matchmaking and engagement tracking

**Integration Type**: Real-time API

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Researcher Profile

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| orcid | String | Yes | ORCID identifier |
| name | String | Yes | Full name |
| institution | String | Yes | Primary affiliation |
| department | String | No | Department/school |
| expertise_tags | Array[String] | Yes | Research expertise keywords (auto-generated + manual) |
| publications_count | Integer | Yes | Total publication count |
| h_index | Integer | No | h-index (from Crossref/Scopus) |
| collaboration_openness | Enum | No | Open, Selective, Not_Currently_Available |
| profile_visibility | Enum | Yes | Public, Registered_Users, Private |

**Data Volume**: ~200,000 researcher profiles (active UK researchers)

#### Entity 2: Industry Challenge

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| challenge_id | UUID | Yes | Unique identifier |
| poster_id | UUID | Yes | Industry user ID |
| title | String(200) | Yes | Challenge title |
| description | Text | Yes | Problem description |
| domain_tags | Array[String] | Yes | Research domain tags |
| engagement_type | Enum | Yes | Consultancy, Sponsored_Research, Collaborative_RD, Licence |
| budget_range | Enum | No | <10K, 10-50K, 50-200K, 200K-1M, >1M |
| timeline | String | No | Desired engagement timeline |
| status | Enum | Yes | Open, Matched, In_Progress, Completed, Expired |

**Data Volume**: ~5,000 challenges per year (estimated)

---

## Budget

### Cost Estimate

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Development (Year 1-2) | GBP 5.0M | 15 FTE delivery team |
| AI/ML matchmaking engine | GBP 1.5M | NLP model development, training data |
| Infrastructure (Year 1-3) | GBP 1.0M | Cloud hosting, search infrastructure |
| Integration (ORCID, GtR, CRIS) | GBP 0.5M | API development, testing |
| User research and GDS assessment | GBP 0.5M | Industry and researcher engagement |
| KTN partnership | GBP 0.5M | Broker curation services |
| Contingency (15%) | GBP 1.4M | |
| **Total** | **GBP 10.4M** | Over 3 years |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Cloud infrastructure | GBP 0.5M | Including search, ML inference |
| BAU team | GBP 1.0M | 5 FTE |
| KTN broker services | GBP 0.3M | Ongoing human curation |
| Data feed subscriptions | GBP 0.1M | Crossref, Scopus |
| **Total** | **GBP 1.9M/year** | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-005-STKE-v1.0 | Stakeholder Analysis | ArcKit | Stakeholder drivers and goals | `projects/005-research-collaboration-hub/` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Governing principles | `projects/000-global/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Research Collaboration Hub (Project 005)
**Model**: Claude Opus 4.6
