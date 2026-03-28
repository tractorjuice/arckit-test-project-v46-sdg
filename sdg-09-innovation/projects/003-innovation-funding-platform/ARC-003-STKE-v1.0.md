# Stakeholder Drivers & Goals Analysis: Innovation Funding Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
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
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Innovation Funding Platform, their underlying drivers, goals, and measurable outcomes. The platform replaces the legacy Je-S (Joint Electronic Submission) system with a modern grants application and portfolio management service.

### Key Findings

The Innovation Funding Platform sits at the intersection of researcher frustration with legacy systems (Je-S is widely regarded as one of the worst government digital services), UKRI's transformation ambitions, and HM Treasury's scrutiny of GBP 8 billion annual research funding allocation. The strongest alignment exists around replacing Je-S — virtually every stakeholder agrees the current system is unacceptable. The most significant conflict is between the desire for a comprehensive, all-singing platform (UKRI councils) and the practical reality that replacing Je-S while maintaining service continuity is technically and operationally challenging. Research Council cultural differences (each of the seven councils has different processes and terminology) add significant complexity.

### Critical Success Factors

- Maintain uninterrupted grant application and management capability throughout migration from Je-S — any funding round disruption damages UK research competitiveness
- Achieve researcher satisfaction scores significantly above Je-S baseline (currently rated 2.1/5.0)
- Support the diverse requirements of seven Research Councils and Innovate UK without creating seven separate systems
- Integrate with university research management systems (Pure, Symplectic, Worktribe) to reduce duplicate data entry
- Deliver portfolio analytics that enable UKRI to demonstrate research impact and value for money to Treasury

### Stakeholder Alignment Score

**Overall Alignment**: HIGH

Unusually strong alignment on the need for change — Je-S replacement is universally demanded. Tensions exist around scope (councils want everything, delivery team wants incremental approach), timeline (researchers want it yesterday, cautious migration is safer), and governance (councils want autonomy, UKRI centre wants standardisation).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| UKRI Chief Executive | Sponsor | HIGH | HIGH | Manage Closely — Programme board |
| UKRI Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| EPSRC Chief Executive | Engineering & Physical Sciences | HIGH | HIGH | Manage Closely — Largest council by volume |
| MRC Chief Executive | Medical Research Council | HIGH | HIGH | Manage Closely — Complex review processes |
| BBSRC, NERC, STFC, ESRC, AHRC CEOs | Research Council leaders | MEDIUM | HIGH | Keep Informed — Council-specific requirements |
| Innovate UK Director | Innovation funding | HIGH | HIGH | Manage Closely — Different funding model |
| UKRI Finance Director | Budget and grants finance | HIGH | MEDIUM | Keep Satisfied — Financial controls |
| UKRI SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, data protection |
| SRO, Innovation Funding Platform | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| DSIT | Department | Policy oversight, UKRI sponsor | HIGH | HIGH |
| HM Treasury | HM Treasury | Funding and spending review | HIGH | MEDIUM |
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| Universities (130+) | Higher Education | Applicants, research organisations | LOW | HIGH |
| University Research Offices | Higher Education | Grant administration, costing | MEDIUM | HIGH |
| Principal Investigators (researchers) | Academia | End users — grant applicants | LOW | HIGH |
| Peer Reviewers | Academia / Industry | Review and assessment | LOW | HIGH |
| Russell Group | University body | Research-intensive universities | MEDIUM | HIGH |
| UCAS / HESA | Education data | Student and institutional data | LOW | MEDIUM |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Jisc | Sector body | Digital infrastructure for research | MEDIUM | MEDIUM |
| Research Management Systems vendors | Commercial | Pure, Symplectic, Worktribe | LOW | HIGH |
| GDS Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| ORCID | International | Researcher identifier | LOW | HIGH |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • UKRI CEO         │
        │  • NAO              │  • UKRI CDO         │
        │  • CDDO             │  • EPSRC CEO        │
        │  • UKRI SIRO        │  • MRC CEO          │
        │  • UKRI Finance Dir │  • Innovate UK Dir  │
 P      │                     │  • SRO              │
 O      │                     │  • DSIT             │
 W      ├─────────────────────┼─────────────────────┤
 E      │                     │                     │
 R      │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • UCAS / HESA      │  • Researchers (PIs)│
        │                     │  • University ROs   │
        │                     │  • Peer Reviewers   │
        │                     │  • Russell Group    │
        │                     │  • Other Council    │
        │                     │    CEOs             │
        │                     │  • Jisc             │
        │                     │  • RMS vendors      │
        │                     │  • GDS Assessment   │
        │                     │  • ORCID            │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: UKRI Chief Executive — Demonstrate Research Impact and Value for Money

**Stakeholder**: UKRI Chief Executive

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Replace the legacy Je-S system with a modern platform that enables UKRI to demonstrate the impact and value for money of GBP 8 billion annual research funding, providing portfolio analytics for DSIT and Treasury while dramatically improving the researcher experience.

**Context & Background**:
UKRI was created in 2018 by merging seven Research Councils and Innovate UK. The legacy Je-S system predates UKRI and cannot provide cross-council portfolio views. Treasury spending reviews increasingly demand evidence of research impact and efficiency. The current system's poor user experience damages UK research competitiveness — researchers report spending 30-40 hours per application on a system rated 2.1/5.0.

**Driver Intensity**: CRITICAL

**Enablers**:

- Strong political support for Je-S replacement (universal dissatisfaction)
- UKRI Digital transformation programme funded
- GDS digital service standard providing proven delivery methodology

**Blockers**:

- Seven Research Councils with different processes, terminology, and cultures
- Migration risk from a system processing GBP 8 billion in active grants
- Academic calendar constraints on migration windows

**Related Stakeholders**: DSIT, HM Treasury, Researchers

---

### SD-2: Researchers — Stop Wasting Research Time on Administrative Systems

**Stakeholder**: Principal Investigators (approximately 60,000 active applicants)

**Driver Category**: PERSONAL / OPERATIONAL

**Driver Statement**: Spend less time fighting the grant application system and more time on research, with an application process that is intuitive, saves progress reliably, reuses institutional and personal data across applications, and provides transparent feedback on application status.

**Context & Background**:
Je-S is universally loathed by the research community. Common complaints include: no auto-save (lost work), incompatibility with modern browsers, inability to reuse data from previous applications, opaque status tracking, and a forms-based interface designed for administrators rather than researchers. Researchers estimate spending 30-40 hours per standard application, of which 15-20 hours are "fighting the system" rather than substantive intellectual work. This represents a hidden tax on UK research productivity.

**Driver Intensity**: CRITICAL

**Enablers**:

- ORCID adoption widespread — enables auto-population of researcher profiles
- University research management systems (Pure, Symplectic) hold institutional data that can be pre-populated
- GOV.UK Forms and design patterns provide proven UX approaches

**Blockers**:

- Researcher conservatism — fear that a new system will be worse than Je-S during transition
- Diverse research domains have genuinely different application structures (EPSRC vs AHRC)
- Many researchers are infrequent users — interface must be intuitive without training

**Related Stakeholders**: University Research Offices, ORCID, Russell Group

---

### SD-3: Research Council CEOs — Preserve Council-Specific Processes

**Stakeholder**: EPSRC, MRC, BBSRC, NERC, STFC, ESRC, AHRC Chief Executives

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Ensure the new platform supports council-specific funding schemes, review processes, assessment criteria, and terminology without forcing homogenisation that would compromise the quality of funding decisions in each discipline.

**Context & Background**:
Each Research Council has evolved specific processes suited to their domain: MRC has complex clinical trial costing; EPSRC handles large consortium applications; AHRC manages creative practice outputs; NERC has specific environmental data requirements. Previous UKRI standardisation attempts have met resistance because one-size-fits-all processes reduce assessment quality.

**Driver Intensity**: HIGH

**Enablers**:

- Platform can be configurable rather than rigid — different schemes as configurations, not code changes
- Cross-council themes (interdisciplinary research) provide incentive for some standardisation
- New UKRI funding framework provides opportunity to rationalise where genuinely beneficial

**Blockers**:

- Cultural resistance to change in long-established councils
- Risk that standardisation reduces assessment quality in specialist domains
- Council identity and autonomy are politically sensitive within UKRI

**Related Stakeholders**: UKRI CEO, Peer Reviewers, Researchers

---

### SD-4: University Research Offices — Reduce Administrative Burden

**Stakeholder**: University Research Offices (130+ institutions)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Reduce the time spent on UKRI grant administration — application preparation, costing, submission, post-award management — by integrating the funding platform with institutional research management systems and eliminating duplicate data entry.

**Context & Background**:
Research offices spend significant staff time re-keying data between institutional systems and Je-S. Full Economic Costing (fEC) calculations are performed in institutional systems then manually transferred. Post-award financial reporting requires manual reconciliation. Integration via APIs would save an estimated 2-3 FTE per large research-intensive university.

**Driver Intensity**: HIGH

**Enablers**:

- Major RMS platforms (Pure, Symplectic, Worktribe) willing to build API integrations
- UKRI costing model is standardised (fEC), enabling structured data exchange
- Jisc providing coordination across the sector

**Blockers**:

- 130+ universities with diverse systems and capabilities
- Smaller universities lack IT capacity to implement integrations
- Data quality varies significantly across institutions

**Related Stakeholders**: UKRI Finance, RMS vendors, Jisc, Russell Group

---

## Driver-to-Goal Mapping

### Goal G-1: Modern Grant Application Experience

**Derived From Drivers**: SD-1, SD-2

**Goal Owner**: UKRI CDO

**Goal Statement**: Deliver a grant application service achieving researcher satisfaction score > 4.0/5.0 (vs Je-S baseline 2.1/5.0) within 12 months of launch, with application preparation time reduced by 40%.

**Why This Matters**: UK research competitiveness depends on researchers spending time on research, not administration. Every hour saved on applications is an hour available for science.

**Success Metrics**:

- **Primary Metric**: Researcher satisfaction score (currently 2.1/5.0)
- **Secondary Metrics**:
  - Average application preparation time (40% reduction target)
  - Application completion rate (reduce abandonment)
  - Accessibility compliance: WCAG 2.2 Level AA

**Baseline**: Je-S satisfaction 2.1/5.0, 30-40 hours per application

**Target**: 4.0/5.0 satisfaction, 18-24 hours per application

---

### Goal G-2: Cross-Council Portfolio Analytics

**Derived From Drivers**: SD-1

**Goal Owner**: UKRI CEO

**Goal Statement**: Deliver portfolio analytics that provide cross-council views of research funding by theme, institution, researcher, geographic region, and impact area — enabling UKRI to respond to Treasury spending review questions within 24 hours rather than the current 2-4 weeks.

**Why This Matters**: Treasury's confidence in UKRI funding allocation depends on UKRI's ability to demonstrate impact and value. Current inability to answer cross-council questions quickly undermines UKRI's case for funding protection.

**Success Metrics**:

- **Primary Metric**: Time to respond to Treasury portfolio questions (2-4 weeks to 24 hours)
- **Secondary Metrics**:
  - Number of cross-council analytics dashboards available
  - Research output tracking (publications, citations, impact case studies linked to grants)

---

### Goal G-3: Institutional Integration

**Derived From Drivers**: SD-2, SD-4

**Goal Owner**: Product Manager

**Goal Statement**: Deliver API-based integration with the three major research management systems (Pure, Symplectic, Worktribe) by Q2 2028, enabling auto-population of institutional data and eliminating duplicate costing entry.

**Why This Matters**: Duplicate data entry wastes university research office time and introduces errors in costing and reporting.

**Success Metrics**:

- **Primary Metric**: Number of universities with active API integration
- **Secondary Metrics**:
  - Reduction in research office FTE on UKRI administration (target: 2 FTE per large university)
  - Data entry error rate reduction

---

## Goal-to-Outcome Mapping

### Outcome O-1: UK Research Productivity and Competitiveness

**Supported Goals**: G-1, G-3

**Outcome Statement**: Recover an estimated 500,000 researcher-hours per year currently wasted on administrative system friction, equivalent to GBP 25 million in researcher time at average academic salary.

**Measurement Details**:

- **KPI**: Researcher hours spent on application administration
- **Current Value**: Estimated 1.2 million hours/year across 60,000 applicants
- **Target Value**: 720,000 hours/year (40% reduction)
- **Measurement Frequency**: Annual
- **Data Source**: Application completion time analytics, researcher survey

**Business Value**:

- **Financial Impact**: GBP 25M equivalent in recovered researcher productivity
- **Strategic Impact**: UK more attractive for international research talent
- **Operational Impact**: Faster funding cycle from application to award
- **Customer Impact**: Researcher satisfaction, reduced burnout

---

### Outcome O-2: Evidence-Based Research Funding Allocation

**Supported Goals**: G-2

**Outcome Statement**: UKRI can demonstrate research portfolio composition, impact, and value for money to Treasury and Parliament within 24 hours of request, strengthening the case for protecting research funding in spending reviews.

**Measurement Details**:

- **KPI**: Time to produce cross-council portfolio analysis
- **Current Value**: 2-4 weeks
- **Target Value**: 24 hours
- **Measurement Frequency**: Per request
- **Data Source**: Portfolio analytics platform usage logs

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| UKRI CEO | SD-1 | Demonstrate impact and value | G-1 | Modern application experience | O-1 | Research productivity |
| UKRI CEO | SD-1 | Demonstrate impact and value | G-2 | Portfolio analytics | O-2 | Evidence-based allocation |
| Researchers | SD-2 | Stop wasting research time | G-1 | Modern application experience | O-1 | Research productivity |
| Researchers | SD-2 | Stop wasting research time | G-3 | Institutional integration | O-1 | Research productivity |
| Council CEOs | SD-3 | Preserve council processes | G-1 | Modern application experience | O-1 | Research productivity |
| University ROs | SD-4 | Reduce admin burden | G-3 | Institutional integration | O-1 | Research productivity |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: UKRI CEO (SD-1) wants cross-council standardisation for portfolio analytics, but Council CEOs (SD-3) want to preserve council-specific processes and terminology.
  - **Resolution Strategy**: Configurable platform — standard data model with council-specific overlays. Councils configure their schemes within the platform rather than having separate systems. Shared taxonomy for portfolio reporting with council-specific labels for user-facing elements.

- **Conflict 2**: Researchers (SD-2) want immediate migration from Je-S, but migration risk management requires a phased approach that temporarily increases complexity (running both systems in parallel).
  - **Resolution Strategy**: Council-by-council migration with clear timeline. Smallest councils first (AHRC, ESRC) to prove the platform, largest last (EPSRC). No council runs dual systems for more than 6 months.

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Migration Disruption During Funding Round

**Related Stakeholders**: Researchers, Council CEOs, UKRI CEO

**Risk Description**: Platform migration disrupts an active funding round, causing application loss, deadline extension, and reputational damage to UKRI.

**Probability**: MEDIUM | **Impact**: CRITICAL

**Mitigation Strategy**: Migrate between funding rounds; maintain Je-S read-only access for 12 months post-migration; extensive pre-migration testing with real application data

---

### Risk R-2: Council Resistance to Standardisation

**Related Stakeholders**: Council CEOs

**Risk Description**: Research Councils resist process standardisation, demanding extensive customisation that inflates delivery cost and timeline beyond budget.

**Probability**: HIGH | **Impact**: MEDIUM

**Mitigation Strategy**: Define mandatory data standard for portfolio reporting (non-negotiable), but allow council-specific configuration for application forms and review workflows. CEO-level governance for scope disputes.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UKRI Strategy 2022-2027 | Strategy | UKRI | Digital transformation priorities | N/A — external reference |
| Je-S Replacement Business Case | Business Case | UKRI | Investment justification | N/A — external reference |
| FAIR Data Principles | Guidance | GO FAIR | Research data management standards | N/A — external reference |
| Full Economic Costing (fEC) | Policy | UKRI | Grant costing methodology | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Innovation Funding Platform (Project 003)
**Model**: Claude Opus 4.6
