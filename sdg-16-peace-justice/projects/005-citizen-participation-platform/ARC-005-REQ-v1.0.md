# Project Requirements: Citizen Participation Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Citizen Participation Platform (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Citizen Participation Platform |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DLUHC Digital, Cabinet Office Consultation Hub, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

---

## Executive Summary

### Business Context

The UK Government runs approximately 500+ formal consultations per year, with thousands more informal engagements. Current processes are fragmented — departments use a mix of PDF-based consultations published on GOV.UK, commercial survey tools (SmartSurvey, Citizen Space), email responses, and bespoke platforms. There is no standard approach, no central response analysis capability, and limited evidence that consultations reach beyond organised stakeholders. Public trust in government consultations is low (18% believe they influence policy, British Social Attitudes 2024).

SDG 16.7 requires responsive, inclusive, participatory, and representative decision-making. The Open Government Partnership National Action Plan commits the UK to strengthening citizen engagement. The Levelling Up agenda explicitly aims to give communities a greater voice.

### Objectives

- Provide a standardised, cross-government digital platform for public consultations and citizen engagement
- Increase participation from underrepresented communities by 30%
- Reduce consultation time and cost by 50% through standardised workflows and automated analysis
- Ensure 90% of consultations publish "You Said, We Did" outcome reports demonstrating citizen influence
- Support deliberative engagement methods (citizens' assemblies, participatory budgeting) alongside standard consultations

### Expected Outcomes

- 50% reduction in average consultation cycle time (9 months to 4.5 months)
- 30% increase in responses from underrepresented demographic groups
- 90% of consultations publish structured outcome impact reports
- 200+ government consultations per year running on the platform
- Platform supports both central and local government engagement

### Project Scope

**In Scope**:

- Consultation creation, publishing, and management platform
- Citizen-facing response submission (online, SMS integration, postal scanning)
- Response analysis tools (quantitative analysis, NLP for open-text responses)
- "You Said, We Did" outcome reporting
- Participatory budgeting module for local spending decisions
- Discussion forums with moderation for deliberative engagement
- GOV.UK consultation page integration
- Cross-government consultation reporting dashboard
- Accessibility compliance (WCAG 2.2 Level AA, Easy Read, Welsh language)

**Out of Scope**:

- Parliamentary petition system (Parliament's responsibility)
- Electoral registration and voting systems (Electoral Commission)
- FOI request management (separate system)
- Social media engagement management
- Face-to-face citizen engagement event management (complementary, not platform-based)

---

## Business Requirements

### BR-1: Standardised Consultation Management

**Description**: The system must provide a standardised workflow for creating, publishing, managing, analysing, and reporting on government consultations, compliant with the Government Consultation Principles.

**Rationale**: Current fragmentation across 20+ departments using different tools creates inconsistency, prevents cross-government reporting, and makes it impossible to assess the overall quality and impact of government consultations.

**Success Criteria**:

- 200+ consultations per year running on the platform within 18 months
- Consultation creation time reduced from 2 weeks to 2 days
- Built-in compliance checks for Government Consultation Principles (minimum period, mandatory government response)
- Cross-government reporting on consultation volumes, response rates, and outcomes

**Priority**: MUST_HAVE
**Stakeholder**: Cabinet Office Consultation Hub

---

### BR-2: Inclusive and Accessible Citizen Participation

**Description**: The system must be designed to maximise participation from diverse communities, including those who are digitally excluded, have disabilities, speak community languages, or live in deprived areas.

**Rationale**: Current consultations disproportionately attract responses from organised stakeholders, older demographics, and higher socioeconomic groups. SDG 16.7 requires representative participation. The Levelling Up agenda requires giving voice to underrepresented communities.

**Success Criteria**:

- 30% increase in responses from underrepresented groups within 18 months
- WCAG 2.2 Level AA compliance for all citizen-facing features
- Easy Read versions of consultation documents
- Welsh language support for all citizen-facing content
- SMS response pathway for non-digital citizens
- Community language summaries for major consultations

**Priority**: MUST_HAVE
**Stakeholder**: DLUHC Minister, Citizens, Disability Rights UK

---

### BR-3: Transparent Outcome Reporting

**Description**: The system must enable and enforce publication of structured outcome reports ("You Said, We Did") that demonstrate how citizen responses influenced the policy decision.

**Rationale**: The single biggest driver of consultation fatigue is the perception that responses are ignored. Transparent outcome reporting is essential to rebuilding trust in participatory processes.

**Success Criteria**:

- 90% of consultations publish outcome reports within 6 months of close
- Outcome reports structured to show: what was proposed, what citizens said, what was changed, what was not changed and why
- System enforces government response publication as a mandatory workflow step

**Priority**: MUST_HAVE
**Stakeholder**: DLUHC Minister, Citizens, Involve

---

### BR-4: Response Analysis and NLP

**Description**: The system must provide automated analysis tools for consultation responses, including quantitative analysis (closed questions), NLP-based thematic analysis (open-text responses), and campaign response identification.

**Rationale**: Large consultations (10,000+ responses) cannot be manually analysed in a timely manner. NLP-based analysis accelerates response processing while maintaining quality. Campaign response identification ensures transparency about organised lobbying.

**Success Criteria**:

- Automated quantitative analysis for closed questions (charts, statistics, cross-tabulation)
- NLP thematic analysis identifying top 10 themes from open-text responses with 85% accuracy
- Campaign response identification (bulk identical or near-identical responses) with transparency reporting
- Analysis available within 2 weeks of consultation close for consultations with fewer than 5,000 responses

**Priority**: SHOULD_HAVE
**Stakeholder**: Cabinet Office, Departmental policy teams

---

### BR-5: Deliberative Engagement Support

**Description**: The system must support deliberative engagement methods beyond standard consultations, including structured discussion forums, evidence review, and participatory budgeting.

**Rationale**: Standard consultations (12-week open comment) capture opinions but not deliberation. Deliberative methods produce more representative and considered citizen input, as demonstrated by Climate Assembly UK and participatory budgeting in 30+ UK local authorities.

**Success Criteria**:

- Discussion forum with moderation, evidence linking, and structured dialogue
- Participatory budgeting module allowing citizens to allocate notional budgets
- Support for citizens' assembly processes (information provision, question iteration, voting)
- Clear guidance for departments on when to use standard vs. deliberative methods

**Priority**: SHOULD_HAVE
**Stakeholder**: Involve, Democratic Society, Local authorities

---

## Functional Requirements

### FR-1: Consultation Builder

**Description**: System must provide a template-based consultation builder enabling departmental policy teams to create consultations with question design, supporting documents, and metadata.

**Acceptance Criteria**:

- [ ] Given a departmental user, when they create a consultation, then templates are available for different consultation types (policy consultation, planning consultation, regulatory consultation)
- [ ] Given question design, when the user adds questions, then multiple question types are supported (multiple choice, free text, ranking, Likert scale, budget allocation)
- [ ] Given the consultation, when it is submitted for publication, then compliance checks verify Government Consultation Principles requirements (minimum period, accessibility, government response commitment)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-2: Citizen Response Interface

**Description**: System must provide an accessible, user-friendly response interface for citizens to read consultation documents and submit responses.

**Acceptance Criteria**:

- [ ] Given a citizen accessing a consultation, when they view it, then the consultation purpose, key questions, and supporting evidence are presented in plain language
- [ ] Given a citizen submitting a response, when they complete questions, then progress is saved automatically and they can return later
- [ ] Given a citizen with accessibility needs, when they use the service, then all functionality is keyboard-navigable, screen-reader compatible, and available in Welsh for Wales-relevant consultations
- [ ] Given a non-digital citizen, when their postal response is received, then it is scanned/transcribed and included in the analysis

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

### FR-3: Response Analysis Dashboard

**Description**: System must provide policy teams with a real-time analysis dashboard showing response volumes, demographics, quantitative results, and NLP-generated themes from open-text responses.

**Acceptance Criteria**:

- [ ] Given consultation responses, when the dashboard is accessed, then real-time response count, demographic breakdown, and quantitative summary are displayed
- [ ] Given open-text responses, when NLP analysis runs, then the top themes, sentiment distribution, and representative quotes are displayed
- [ ] Given campaign responses (identical or near-identical), when detected, then they are flagged separately with count and analysis distinguishing campaign from individual responses

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

### FR-4: "You Said, We Did" Report Generator

**Description**: System must generate structured outcome reports showing how consultation responses influenced the policy decision.

**Acceptance Criteria**:

- [ ] Given a completed consultation, when the policy team creates an outcome report, then a structured template is provided with sections for citizen views, policy response, and changes made
- [ ] Given the outcome report, when published, then it is linked to the original consultation and notification sent to respondents who opted in
- [ ] Given a consultation that has been closed for 6 months without a published outcome report, then the platform alerts the departmental head and Cabinet Office

**Priority**: MUST_HAVE
**Complexity**: LOW

---

### FR-5: Participatory Budgeting Module

**Description**: System must support participatory budgeting exercises where citizens allocate a notional budget across defined spending categories.

**Acceptance Criteria**:

- [ ] Given a participatory budgeting exercise, when a citizen allocates budget, then they can distribute a fixed total across categories using sliders or input fields
- [ ] Given budget allocations from all participants, when aggregated, then the average allocation and distribution are displayed as interactive visualisations
- [ ] Given local authority usage, when a council creates a participatory budget, then they can define categories, descriptions, and total budget

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

### FR-6: Discussion Forum with Moderation

**Description**: System must provide a moderated discussion forum for deliberative consultations, enabling citizens to discuss evidence and form considered views.

**Acceptance Criteria**:

- [ ] Given a deliberative consultation, when a discussion forum is enabled, then citizens can post comments, reply to others, and reference evidence documents
- [ ] Given user-generated content, when moderation rules are applied, then abusive, off-topic, or illegal content is flagged for moderator review before publication
- [ ] Given a discussion thread, when NLP analysis is applied, then the key themes and points of agreement/disagreement are summarised

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

### FR-7: GOV.UK Integration

**Description**: System must integrate with GOV.UK consultation publishing to ensure consultations appear in the standard GOV.UK consultation finder.

**Acceptance Criteria**:

- [ ] Given a consultation published on the platform, when it goes live, then it appears in the GOV.UK consultation finder with correct metadata
- [ ] Given a consultation close, when the outcome report is published, then it appears linked to the original GOV.UK consultation page

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Response Time

**Requirement**: Page load below 2 seconds at p95. Response submission confirmation within 3 seconds. NLP analysis refresh within 30 minutes of new responses.

**Load Conditions**: Peak 50,000 concurrent users (major national consultation deadline). Average 5,000 concurrent users. Up to 500,000 responses per consultation.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% uptime. Consultation deadlines are time-critical — no downtime on consultation close dates.

**Priority**: HIGH

---

### NFR-SEC-1: Security and Privacy

**Requirement**: Anonymous responses supported — no mandatory personal data collection. Where demographic monitoring is offered, it is optional and clearly separated from consultation responses. Responses encrypted at rest. No personally identifiable response data shared with policy teams unless explicitly consented.

**Priority**: HIGH

---

### NFR-U-1: Accessibility

**Requirement**: WCAG 2.2 Level AA. Easy Read support. Welsh language for Wales consultations. Reading age 9-11 for citizen-facing content. Mobile-responsive design. SMS response pathway for non-digital access.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: GOV.UK Consultation Finder

**Purpose**: Publish consultations to GOV.UK and link outcome reports.
**Integration Type**: API (GOV.UK Publishing API)
**Priority**: MUST_HAVE

---

### INT-2: GOV.UK Notify

**Purpose**: Send consultation launch notifications, deadline reminders, and outcome report alerts to subscribers.
**Integration Type**: API
**Priority**: MUST_HAVE

---

### INT-3: GOV.UK One Login

**Purpose**: Optional authenticated access for citizens wanting to track their consultation responses and receive outcome notifications.
**Integration Type**: OpenID Connect
**Priority**: SHOULD_HAVE

---

## Data Requirements

### Key Data Entities

| Entity | Description | Volume | Classification | Retention |
|--------|-------------|--------|---------------|-----------|
| Consultation | Consultation definition with questions and metadata | 500/year | OFFICIAL | Indefinite (public record) |
| Response | Individual citizen response | 2 million/year | OFFICIAL (anonymised) | Indefinite (public record) |
| Outcome Report | Government response to consultation | 500/year | OFFICIAL | Indefinite (public record) |
| Publisher Account | Departmental consultation creator | 200 accounts | OFFICIAL | Active + 1 year |
| Discussion Post | Forum discussion contribution | 500,000/year | OFFICIAL | Aligned to consultation retention |

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Consultation cycle time | 9 months avg | 4.5 months avg | 18 months |
| Underrepresented group responses | ~15% | 20%+ | 18 months |
| Outcome report publication rate | ~60% | 90% | 12 months |
| Consultations on platform | 0 | 200+ per year | 18 months |
| Citizen satisfaction with process | 18% trust | 35% trust | 24 months |

---

## Dependencies and Risks

| Risk ID | Description | Probability | Impact | Mitigation |
|---------|-------------|-------------|--------|------------|
| R-1 | Departments do not adopt the platform (prefer existing tools) | HIGH | HIGH | Ministerial mandate, demo clear efficiency gains, migration support |
| R-2 | Low citizen participation despite platform improvements | MEDIUM | HIGH | Active outreach, community partnerships, multi-channel access |
| R-3 | NLP analysis produces inaccurate thematic summaries | MEDIUM | MEDIUM | Human review of NLP output, quality threshold before publication |
| R-4 | Discussion forums attract abuse or organised disruption | MEDIUM | MEDIUM | Moderation framework, community guidelines, automated detection |
| R-5 | Consultation fatigue — too many consultations dilute participation | LOW | MEDIUM | Consultation calendar coordination, priority flagging for major consultations |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| Government Consultation Principles | Cabinet Office guidance on running government consultations |
| Participatory Budgeting | Citizens directly deciding how to allocate a portion of public budget |
| Citizens' Assembly | Randomly selected citizens deliberating on a policy question |
| NLP | Natural Language Processing — automated text analysis |
| Easy Read | Accessible document format using simple words and images |
| LSOA | Lower Layer Super Output Area — geographic unit for deprivation measurement |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — SDG 16 Architecture Principles
- ARC-005-STKE-v1.0 — Citizen Participation Platform Stakeholder Analysis
- Government Consultation Principles (Cabinet Office)
- UK 5th OGP National Action Plan

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Citizen Participation Platform
**Model**: Claude Opus 4.6
