# Project Requirements: Sustainable Procurement Portal

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Sustainable Procurement Portal (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, Sustainable Procurement Portal |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Crown Commercial Service, DESNZ, DEFRA, SDG 12 Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the Sustainable Procurement Portal — a Crown Commercial Service-owned digital platform that integrates carbon scores, social value assessments, and circular economy metrics into government procurement evaluation, enabling contracting authorities to make sustainability-informed decisions with legal confidence.

---

## Executive Summary

### Business Context

The UK Government spends over GBP 300 billion annually through procurement. PPN 06/20 mandates a minimum 10% social value weighting, and PPN 06/21 requires Carbon Reduction Plans for contracts above GBP 5 million. Despite these policies, sustainability assessment in procurement remains inconsistent — each contracting authority interprets the requirements differently, procurement officers lack environmental expertise, and no digital tool exists to integrate sustainability scoring into evaluation workflows. The result: sustainability policies that exist on paper but do not systematically influence award decisions.

The Sustainable Procurement Portal will provide a unified platform integrating carbon scores from the Carbon Footprint Calculator (Project 001), social value assessments aligned with the Social Value Model (PPN 06/20), and circular economy metrics from the Waste Management Analytics platform (Project 003), delivering a single defensible sustainability score that procurement officers can apply alongside price and quality.

### Objectives

- Integrate carbon scores from the Carbon Footprint Calculator (Project 001) into procurement evaluation
- Deliver standardised sustainability scoring aligned with PPN 06/20 and PPN 06/21
- Provide contracting authorities with legally defensible evaluation methodology reviewed by GLD
- Create a supplier transparency dashboard showing sustainability scores and improvement guidance
- Enable sustainability benchmarking across contracting authorities

### Expected Outcomes

- 80% of central government procurements above GBP 5M using standardised sustainability scoring within 24 months
- Zero successful legal challenges based on sustainability scoring within 24 months
- 10,000 suppliers accessing sustainability dashboards within 12 months
- Measurable increase in sustainability weighting applied in procurement evaluations (baseline: inconsistent, target: minimum 10% consistently applied)

### Project Scope

**In Scope**:

- Unified sustainability scoring engine (carbon + social value + circular economy)
- Contracting authority evaluation interface integrated with procurement workflows
- Supplier sustainability dashboard with scores, benchmarks, and improvement guidance
- Carbon score API integration from Project 001
- PPN 06/20 Social Value Model scoring templates
- PPN 06/21 Carbon Reduction Plan evaluation automation
- Sustainability benchmarking across contracting authorities
- Audit trail for legal defensibility

**Out of Scope**:

- Replacement of existing e-procurement systems (Jaggaer, Bravo, etc.)
- Supplier registration and prequalification (existing CCS frameworks)
- Financial evaluation (price scoring remains in existing systems)
- Technical quality evaluation (remains in existing evaluation processes)
- International procurement (non-UK Government)

---

## Business Requirements

### BR-1: Unified Sustainability Score

**Description**: The portal must produce a single, composite sustainability score integrating carbon performance, social value, and circular economy metrics, normalised for sector and organisational size.

**Rationale**: Procurement officers need a single score they can apply with the same confidence as a price score. Multiple separate environmental metrics create complexity and inconsistency.

**Success Criteria**:

- Single composite score on a 0-100 scale integrating carbon, social value, and circular economy
- Score methodology published and reviewed by Government Legal Department
- Sector and size normalisation preventing unfair comparison across different industries

**Priority**: MUST_HAVE

---

### BR-2: Legal Defensibility

**Description**: The sustainability scoring methodology must be legally defensible under the Procurement Act 2023 and withstand challenge from unsuccessful bidders.

**Rationale**: Procurement challenges based on sustainability scoring could undermine the entire programme. Legal confidence is a prerequisite for contracting authority adoption.

**Success Criteria**:

- GLD review completed before deployment
- Complete audit trail for every score calculation
- Consistent methodology applied across all contracting authorities
- Zero successful legal challenges within 24 months

**Priority**: MUST_HAVE

---

### BR-3: Procurement Workflow Integration

**Description**: The sustainability score must be accessible within contracting authorities' existing procurement workflows, not requiring a separate login or system navigation.

**Rationale**: Procurement officers will not adopt a tool that adds steps to their workflow. Integration must be seamless.

**Success Criteria**:

- API and embeddable widget for integration with major e-procurement platforms
- Single sign-on with existing government authentication
- Score available at point of evaluation without leaving the procurement system

**Priority**: MUST_HAVE

---

### BR-4: Supplier Transparency

**Description**: Suppliers must be able to view their sustainability scores, understand how scores are calculated, see their sector benchmark position, and access guidance on improving their scores.

**Rationale**: Transparency drives genuine sustainability investment. If suppliers understand how scores affect competitiveness, they will invest in decarbonisation rather than presentation.

**Success Criteria**:

- Supplier dashboard showing composite score and component breakdown
- Sector benchmark position (quartile ranking)
- Improvement trajectory showing score trends over time
- Actionable guidance on improving each component score

**Priority**: MUST_HAVE

---

## Functional Requirements

### FR-1: Carbon Score Integration

**Description**: The system must consume normalised carbon intensity scores from the Carbon Footprint Calculator (Project 001) via API and incorporate them as the carbon component of the composite sustainability score.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a supplier has a completed carbon calculation in Project 001, when the sustainability score is calculated, then the carbon component reflects the supplier's normalised carbon intensity and sector benchmark position
- [ ] Given a supplier has no carbon calculation, when the sustainability score is calculated, then the carbon component uses industry average (with reduced confidence weighting) and the supplier is prompted to complete a calculation
- [ ] Carbon score updated automatically when the supplier submits a new calculation
- [ ] API integration with Project 001 achieving 99.9% availability and <500ms latency

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: Carbon Footprint Calculator API (Project 001, FR-9)

---

### FR-2: Social Value Assessment Engine

**Description**: The system must provide standardised social value assessment aligned with the Social Value Model themes defined in PPN 06/20, with scoring templates for each theme and sub-theme.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a procurement evaluation includes social value, when the evaluator accesses the portal, then they see the 5 Social Value Model themes with scoring guidance for each
- [ ] Themes: (1) COVID-19 recovery, (2) Tackling economic inequality, (3) Fighting climate change, (4) Equal opportunity, (5) Wellbeing
- [ ] Scoring templates provide standardised criteria and example evidence for each score level
- [ ] Social value commitments captured alongside scores for post-award monitoring

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-3: Circular Economy Metrics Integration

**Description**: The system must incorporate circular economy performance metrics from the Waste Management Analytics platform (Project 003) and from supplier self-declaration, including waste reduction, recycled content usage, and product longevity.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given a supplier reports circular economy data (recycled content %, waste reduction trajectory, product design for disassembly), when the sustainability score is calculated, then circular economy contributes to the composite score
- [ ] Where available, waste management data from Project 003 validates supplier declarations
- [ ] Circular economy scoring weighted by relevance to contract subject matter (high weight for manufacturing contracts, low weight for professional services)

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: Waste Management Analytics API (Project 003)

---

### FR-4: Composite Sustainability Score Calculation

**Description**: The system must calculate a composite sustainability score (0-100) from carbon, social value, and circular economy components, with configurable weighting and sector normalisation.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given component scores are available, when the composite score is calculated, then it applies the configured weighting (default: carbon 40%, social value 40%, circular economy 20%)
- [ ] Weightings configurable by contract type (construction contracts may weight circular economy higher)
- [ ] Sector normalisation applied — scores adjusted relative to sector averages
- [ ] Size adjustment for SMEs — improvement trajectory weighted alongside absolute performance
- [ ] Complete calculation audit trail recording every input, weight, and result

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

### FR-5: Contracting Authority Evaluation Interface

**Description**: The system must provide an evaluation interface where procurement officers access supplier sustainability scores, view component breakdowns, and apply sustainability weighting to procurement decisions.

**Relates To**: BR-2, BR-3

**Acceptance Criteria**:

- [ ] Given a procurement evaluation is in progress, when the evaluator accesses a supplier's sustainability score, then they see the composite score, component breakdown, sector benchmark, and improvement trajectory
- [ ] Evaluator can apply the sustainability score as a percentage weighting (minimum 10% per PPN 06/20) in the overall evaluation
- [ ] Evaluation rationale capture: evaluator records why the sustainability score was applied at the chosen weighting
- [ ] Scoring consistency check: if sustainability weighting varies across suppliers in the same procurement, the system flags the inconsistency

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-6: Supplier Sustainability Dashboard

**Description**: The system must provide a supplier-facing dashboard showing their sustainability scores, sector benchmarks, improvement trajectory, and actionable guidance on improving each component.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a supplier logs in, when they access their dashboard, then they see their composite sustainability score with component breakdown (carbon, social value, circular economy)
- [ ] Sector benchmark shows quartile position (top 25%, upper median, lower median, bottom 25%)
- [ ] Improvement trajectory chart shows score evolution over time (quarterly snapshots)
- [ ] Actionable guidance: for each component, top 3 actions that would improve the score
- [ ] Comparison: "Suppliers in the top quartile of your sector typically..." benchmarking guidance

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

### FR-7: Sustainability Benchmarking Across Contracting Authorities

**Description**: The system must provide CCS with a benchmarking dashboard showing how each contracting authority applies sustainability scoring, enabling identification of authorities that are not effectively implementing PPN 06/20 and PPN 06/21.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given CCS accesses the benchmarking dashboard, when they view contracting authority performance, then they see average sustainability weighting applied, number of procurements using sustainability scoring, and proportion of suppliers with carbon calculations
- [ ] Ranking of contracting authorities by sustainability implementation maturity
- [ ] Trend analysis showing improvement over time per authority
- [ ] Exportable report for ministerial briefings

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

### FR-8: Audit Trail and Legal Defensibility

**Description**: The system must maintain a complete, immutable audit trail of every sustainability score calculation, evaluation application, and weighting decision for legal defensibility.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Every score calculation recorded with timestamp, input data, weights applied, and result
- [ ] Every evaluation application recorded with evaluator identity, weighting chosen, rationale, and comparison with other suppliers
- [ ] Audit trail exportable in a format suitable for procurement challenge proceedings
- [ ] Records retained for 7 years (aligned with procurement record retention)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Score Retrieval Performance

**Requirement**: Sustainability score retrieval under 2 seconds for individual supplier lookup. Batch scoring for procurement lots (up to 50 suppliers) under 30 seconds.

**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.5% availability. Planned maintenance windows outside procurement submission deadlines (typically month-end and quarter-end). Score API available 99.9% during submission windows.

**Priority**: HIGH

---

### NFR-SEC-1: Score Confidentiality

**Requirement**: Individual supplier sustainability scores visible only to the supplier and authorised procurement evaluators. Aggregated sector data available publicly. Scores not shared between competing suppliers.

**Priority**: CRITICAL

---

### NFR-SEC-2: Evaluation Integrity

**Requirement**: Once a sustainability score is applied to a procurement evaluation, the score is locked and cannot be retrospectively modified. Any score update triggers a re-evaluation notification.

**Priority**: CRITICAL

---

### NFR-C-1: Procurement Act 2023 Compliance

**Requirement**: Scoring methodology compliant with Procurement Act 2023 transparency and proportionality requirements. Audit trail sufficient for Procurement Review Panel proceedings.

**Priority**: CRITICAL

---

### NFR-U-1: Procurement Officer Usability

**Requirement**: A procurement officer with no environmental expertise must be able to access and apply a sustainability score within their evaluation in under 5 minutes. No specialist training required beyond a 30-minute online introduction.

**Priority**: CRITICAL

---

## Integration Requirements

### INT-1: Carbon Footprint Calculator (Project 001)

**Purpose**: Consume normalised carbon intensity scores for the carbon component of sustainability scoring.

**Integration Type**: Real-time API (RESTful)

**Data Exchanged**: Carbon intensity score, sector benchmark position, calculation date, data quality score, Scope 1/2/3 breakdown

**SLA**: 99.9% availability, <500ms response time

**Priority**: CRITICAL

---

### INT-2: Waste Management Analytics (Project 003) — Future Phase

**Purpose**: Validate supplier circular economy claims against national waste data.

**Integration Type**: Batch (quarterly reconciliation)

**Priority**: COULD_HAVE (Phase 2)

---

### INT-3: E-Procurement Platform Integration

**Purpose**: Embed sustainability scores within existing procurement evaluation workflows.

**Integration Type**: Embeddable widget and RESTful API

**Target Platforms**: Jaggaer, Bravo, in-house systems (via standardised API)

**Priority**: MUST_HAVE

---

### INT-4: GOV.UK One Login

**Purpose**: Authentication for both contracting authority users and suppliers.

**Priority**: MUST_HAVE

---

## Dependencies and Risks

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Carbon Footprint Calculator (Project 001) not ready | MEDIUM | HIGH | Portal operates with estimated carbon scores until Calculator integration complete | SRO |
| R-2 | Legal challenge to sustainability scoring methodology | MEDIUM | HIGH | GLD review before launch, published methodology, comprehensive audit trail | CCS Legal |
| R-3 | Contracting authority adoption too slow | MEDIUM | HIGH | CCS mandate for frameworks, training programme, executive sponsorship | CCS Commercial Director |
| R-4 | Scoring methodology perceived as unfair to specific sectors | MEDIUM | MEDIUM | Sector normalisation, industry consultation, independent review | Product Manager |
| R-5 | E-procurement platform integration complexity | HIGH | MEDIUM | Standardised API, phased integration starting with Jaggaer, standalone fallback | Technical Lead |

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Procurements using sustainability scoring | ~5% (inconsistently) | 80% above GBP 5M | 24 months | Portal analytics |
| Successful legal challenges | N/A | 0 | 24 months | CCS legal records |
| Suppliers accessing dashboard | 0 | 10,000 | 12 months | Portal analytics |
| Average sustainability weighting applied | Inconsistent | Minimum 10% consistently | 12 months | Portal analytics |
| Supplier satisfaction with transparency | Unknown | 7/10 | 12 months | Survey |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PPN 06/20 | Procurement Note | GOV.UK | Social Value Model, 10% minimum weighting | N/A |
| PPN 06/21 | Procurement Note | GOV.UK | Carbon Reduction Plan requirements | N/A |
| Procurement Act 2023 | Legislation | legislation.gov.uk | New procurement framework, transparency requirements | N/A |
| Social Value Model | Guidance | GOV.UK | 5 themes, scoring methodology | N/A |
| ARC-004-STKE-v1.0 | Stakeholder Analysis | SDG 12 Programme | Stakeholder drivers and goals | `projects/004-sustainable-procurement-portal/` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Sustainable Procurement Portal (Project 004)
**Model**: Claude Opus 4.6
