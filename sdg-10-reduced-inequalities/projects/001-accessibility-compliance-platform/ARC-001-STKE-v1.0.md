# Stakeholder Drivers & Goals Analysis: Accessibility Compliance Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Accessibility Compliance Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Service Owner, Accessibility Compliance Platform, GDS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Leadership, CDDO, Equality Hub, EHRC Liaison |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Accessibility Compliance Platform, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The Accessibility Compliance Platform faces a central tension between automated accessibility testing at scale and the lived-experience testing advocated by disability charities and user groups. GDS leadership wants comprehensive monitoring coverage across approximately 12,000 public sector websites, while organisations like RNIB and Scope argue that automated tools catch only 30-40% of real accessibility barriers and must be supplemented by manual audit and user testing with disabled people. A secondary tension exists between EHRC's enforcement appetite and departments' capacity to remediate identified issues within compliance timescales.

### Critical Success Factors

- Achieve automated scanning coverage of 95% of in-scope public sector websites within 12 months of launch
- Integrate axe-core and WAVE engine results into a single compliance dashboard with actionable remediation guidance
- Establish a lived-experience testing panel of at least 200 disabled users to complement automated scanning
- Demonstrate measurable improvement in public sector WCAG 2.2 compliance rates within 18 months
- Maintain platform accessibility at WCAG 2.2 Level AAA — the compliance platform must itself be exemplary

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for better accessibility monitoring, but significant disagreement on the role and weight of automated vs manual/lived-experience testing. EHRC wants enforcement-grade evidence; disability charities want user-centred assessment; departments want achievable compliance targets; Treasury wants cost efficiency. The platform must reconcile these through a blended assessment methodology.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| GDS Director General | GDS Senior Leadership | HIGH | HIGH | Manage Closely — Strategic direction, ministerial briefings |
| GDS Head of Accessibility | Accessibility standards lead | HIGH | HIGH | Manage Closely — Technical standards, methodology |
| CDDO Director | Cross-government digital assurance | HIGH | HIGH | Manage Closely — Spend control, standards alignment |
| Service Owner | End-to-end service accountability | HIGH | HIGH | Manage Closely — Service reviews, user outcomes |
| GDS Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap input |
| GDS Delivery Manager | Delivery cadence, risks | MEDIUM | HIGH | Keep Informed — Stand-ups, risk escalation |
| GDS Design Lead | Inclusive design standards | MEDIUM | HIGH | Keep Informed — Design system alignment |
| GDS Chief Technology Officer | Technical architecture | HIGH | MEDIUM | Keep Satisfied — Architecture governance |
| Cabinet Office Finance | Budget approval | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| EHRC (Equality & Human Rights Commission) | Regulator | PSBAR enforcement body | HIGH | HIGH |
| RNIB (Royal National Institute of Blind People) | Charity | Visual accessibility advocacy | MEDIUM | HIGH |
| Scope | Charity | Disability equality charity | MEDIUM | HIGH |
| Mencap | Charity | Learning disability advocacy | MEDIUM | HIGH |
| AbilityNet | Charity/Consultancy | Digital accessibility testing | MEDIUM | HIGH |
| Government departmental web teams | All departments | Compliance subjects | MEDIUM | HIGH |
| Local authority digital teams | ~340 local authorities | Compliance subjects | LOW | HIGH |
| NHS Digital | Partner | NHS website accessibility | MEDIUM | HIGH |
| Ofcom | Regulator | Communications accessibility | MEDIUM | MEDIUM |
| W3C WAI | Standards body | WCAG standards development | LOW | MEDIUM |
| Deque Systems | Vendor | axe-core accessibility engine | LOW | HIGH |
| WebAIM | Organisation | WAVE accessibility tool | LOW | HIGH |
| Disabled citizens | Citizens | Ultimate beneficiaries | LOW | HIGH |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes and spend | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns end-to-end accessibility compliance service | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |
| CDIO (GDS) | Digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation |
| Departmental Security Officer (DSO) | Security coordination and policy | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Information risk, DPIA sign-off | HIGH / MEDIUM | Keep Satisfied — Information risk decisions |
| Cyber Security Lead | Operational cyber security | MEDIUM / HIGH | Keep Informed — Security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * Cabinet Office   |  * GDS Director     |
        |    Finance          |    General          |
        |  * GDS CTO          |  * CDDO Director    |
        |  * SIRO             |  * GDS Head of      |
        |  * SSRO / DSO       |    Accessibility    |
 P      |                     |  * Service Owner    |
 O      |                     |  * EHRC             |
 W      |                     |                     |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * W3C WAI          |  * RNIB             |
        |  * Deque Systems    |  * Scope            |
        |  * WebAIM           |  * Mencap           |
        |                     |  * AbilityNet       |
        |                     |  * Dept web teams   |
        |                     |  * Local authorities|
        |                     |  * NHS Digital      |
        |                     |  * Disabled citizens|
        |                     |  * Ofcom            |
        |                     |  * Product Manager  |
        |                     |  * Delivery Manager |
        |                     |  * Cyber Sec Lead   |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: GDS Director General — Demonstrable Improvement in Public Sector Accessibility

**Stakeholder**: GDS Director General

**Driver Category**: STRATEGIC

**Driver Statement**: Demonstrate measurable improvement in public sector website accessibility to fulfil the government's commitment to inclusive digital services, following critical NAO and PAC reports on accessibility compliance gaps.

**Context & Background**:
The NAO's 2024 report on digital accessibility found that fewer than 40% of public sector websites met WCAG 2.1 AA standards despite PSBAR 2018 being in force for over six years. The PAC subsequently called for GDS to provide central monitoring capability. The GDS Director General needs a credible platform to demonstrate progress.

**Driver Intensity**: CRITICAL

**Enablers**:

- Automated scanning at scale to quantify the compliance landscape
- Clear, actionable remediation guidance for non-compliant organisations
- Political support from the Minister for the Cabinet Office

**Blockers**:

- Limited enforcement powers (EHRC is the enforcement body, not GDS)
- Departmental resistance to centralised monitoring
- Budget constraints within Cabinet Office

**Related Stakeholders**: CDDO Director, EHRC, Minister for Cabinet Office

---

### SD-2: EHRC — Enforcement-Grade Evidence for PSBAR Compliance

**Stakeholder**: Equality & Human Rights Commission (EHRC)

**Driver Category**: COMPLIANCE

**Driver Statement**: Obtain reliable, court-admissible evidence of PSBAR non-compliance to support enforcement action against persistently non-compliant public sector bodies, without the EHRC needing to commission expensive manual audits for every case.

**Context & Background**:
The EHRC is responsible for enforcing the Public Sector Bodies Accessibility Regulations 2018 but has limited resources for manual auditing. To date, enforcement has been complaint-driven rather than proactive. A monitoring platform that provides robust automated evidence would enable targeted enforcement at scale.

**Driver Intensity**: HIGH

**Enablers**:

- Automated scanning results that can be used as preliminary evidence
- Standardised reporting format aligned with PSBAR requirements
- Historical compliance trend data showing persistent non-compliance

**Blockers**:

- Automated tools alone may not satisfy evidentiary standards for enforcement
- Privacy concerns around publishing individual organisation scores
- Resource constraints limiting EHRC's ability to act on findings

**Related Stakeholders**: GDS Head of Accessibility, departmental web teams

---

### SD-3: RNIB — Lived Experience Must Inform Compliance Assessment

**Stakeholder**: Royal National Institute of Blind People (RNIB)

**Driver Category**: CUSTOMER

**Driver Statement**: Ensure that accessibility compliance is assessed through the lived experience of disabled people, not just automated rule-checking, because many critical accessibility barriers (poor heading structure, confusing navigation, misleading link text) are invisible to automated tools.

**Context & Background**:
RNIB has extensive evidence that automated accessibility tools detect only 30-40% of WCAG failures and miss entirely the usability barriers that prevent blind and partially sighted people from completing tasks. RNIB advocates for a "blended" assessment approach combining automated scanning with manual expert review and testing by disabled users.

**Driver Intensity**: HIGH

**Enablers**:

- Budget for lived-experience testing panels
- Platform architecture that accommodates manual assessment data alongside automated results
- GDS willingness to weight manual findings in overall compliance scores

**Blockers**:

- Cost and scalability of manual testing across 12,000+ websites
- Difficulty standardising subjective user experience assessments
- Tension with automated-first approach preferred by Treasury for cost efficiency

**Related Stakeholders**: Scope, Mencap, AbilityNet, disabled citizens

---

### SD-4: Departmental Web Teams — Achievable Standards with Clear Guidance

**Stakeholder**: Government departmental web teams (~40 departments)

**Driver Category**: OPERATIONAL

**Driver Statement**: Receive clear, actionable guidance on how to fix accessibility issues identified by the platform, with realistic timescales and prioritised remediation paths, rather than being overwhelmed by automated scan reports listing hundreds of technical violations.

**Context & Background**:
Many departmental web teams are small (2-5 people) and lack specialist accessibility expertise. Previous accessibility audits produced lengthy PDF reports that were difficult to action. Teams want integration with their development workflows (e.g., CI/CD pipeline hooks, Jira integration) and plain-English guidance, not just WCAG success criterion references.

**Driver Intensity**: MEDIUM

**Enablers**:

- Developer-friendly API for integrating scanning into CI/CD pipelines
- Remediation guidance written for non-specialist audiences
- Prioritisation framework (critical barriers vs minor issues)

**Blockers**:

- Lack of dedicated accessibility budget within departments
- Skills gap in accessibility remediation techniques
- Legacy CMS platforms that are difficult to modify

**Related Stakeholders**: GDS Head of Accessibility, GDS Design Lead

---

### SD-5: Scope — Cognitive Accessibility Must Not Be Overlooked

**Stakeholder**: Scope

**Driver Category**: CUSTOMER

**Driver Statement**: Ensure that the platform measures cognitive accessibility barriers (complex language, confusing navigation, lack of consistent patterns) that disproportionately affect people with learning disabilities, autism, and acquired brain injuries — areas where automated tools have the weakest coverage.

**Context & Background**:
WCAG 2.2 includes new success criteria around cognitive accessibility (3.3.7 Redundant Entry, 3.3.8 Accessible Authentication, 3.2.6 Consistent Help), but these are difficult to test automatically. Scope estimates that 1 in 4 disabled people have a cognitive or learning disability, yet accessibility compliance traditionally focuses on visual and motor impairments.

**Driver Intensity**: HIGH

**Enablers**:

- Inclusion of cognitive accessibility criteria in assessment methodology
- Plain English requirement for all platform outputs
- User testing with people with learning disabilities and cognitive impairments

**Blockers**:

- Limited automated testing capability for cognitive accessibility
- Less public awareness of cognitive accessibility vs visual/motor accessibility
- Additional cost of specialist user testing

**Related Stakeholders**: Mencap, RNIB, disabled citizens

---

### SD-6: Cabinet Office Finance — Cost-Efficient Monitoring at Scale

**Stakeholder**: Cabinet Office Finance

**Driver Category**: FINANCIAL

**Driver Statement**: Deliver comprehensive accessibility monitoring across 12,000+ public sector websites at a cost significantly below the alternative of commissioning individual manual audits, which would cost approximately GBP 5,000-15,000 per website.

**Context & Background**:
Manual accessibility audits for 12,000 websites would cost GBP 60-180M. Automated scanning at scale offers orders-of-magnitude cost reduction while providing continuous monitoring rather than point-in-time snapshots. Treasury expects a credible cost-benefit analysis showing the platform is better value than the status quo.

**Driver Intensity**: HIGH

**Enablers**:

- Open source scanning tools (axe-core) to minimise licensing costs
- Cloud-native architecture with pay-per-use pricing
- Economies of scale from centralised platform vs per-department tools

**Blockers**:

- Pressure from disability charities for expensive manual testing alongside automation
- Risk of scope creep into comprehensive audit service
- Ongoing operational costs may exceed initial estimates

**Related Stakeholders**: GDS Director General, CDDO Director, HM Treasury

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 95% Automated Scanning Coverage

**Derived From Drivers**: SD-1, SD-2, SD-6

**Goal Owner**: GDS Director General

**Goal Statement**: Achieve automated WCAG 2.2 scanning coverage of 95% of in-scope public sector websites (approximately 11,400 of 12,000) within 12 months of platform launch.

**Why This Matters**: Comprehensive coverage is the prerequisite for demonstrating improvement (SD-1), enabling targeted enforcement (SD-2), and proving cost-efficiency vs manual audits (SD-6).

**Success Metrics**:

- **Primary Metric**: Percentage of in-scope websites scanned at least monthly
- **Secondary Metrics**:
  - Number of unique WCAG violations detected per scan cycle
  - Scan completion rate (successful scans / attempted scans)
  - Time to first scan for newly registered websites

**Baseline**: Currently fewer than 500 websites scanned regularly by GDS accessibility team

**Target**: 11,400 websites scanned monthly (95% coverage)

**Measurement Method**: Platform analytics dashboard — websites registered vs successfully scanned per cycle

---

### Goal G-2: Establish Blended Assessment Methodology

**Derived From Drivers**: SD-2, SD-3, SD-5

**Goal Owner**: GDS Head of Accessibility

**Goal Statement**: Develop and operationalise a blended accessibility assessment methodology combining automated scanning, expert manual review, and lived-experience testing by disabled users, with clear weighting criteria, within 18 months.

**Why This Matters**: Automated scanning alone satisfies neither EHRC's enforcement evidence needs (SD-2) nor the disability sector's demand for lived-experience inclusion (SD-3, SD-5).

**Success Metrics**:

- **Primary Metric**: Assessment methodology published and peer-reviewed
- **Secondary Metrics**:
  - Number of websites receiving blended assessment per quarter
  - Size of lived-experience testing panel
  - Correlation rate between automated findings and manual/user findings

**Baseline**: No standardised blended methodology exists across government

**Target**: Methodology published, 200+ person testing panel operational, 500+ blended assessments per year

**Measurement Method**: Methodology governance records, panel management system, assessment completion logs

---

### Goal G-3: Measurable Improvement in WCAG Compliance Rates

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: GDS Director General

**Goal Statement**: Increase the proportion of scanned public sector websites meeting WCAG 2.2 Level AA from the current estimated 40% to 70% within 24 months of platform launch through proactive monitoring and remediation guidance.

**Why This Matters**: The platform's purpose is not just measurement but improvement. GDS must demonstrate that monitoring drives compliance, satisfying both political sponsors (SD-1) and departmental teams seeking actionable guidance (SD-4).

**Success Metrics**:

- **Primary Metric**: Percentage of scanned websites passing WCAG 2.2 Level AA
- **Secondary Metrics**:
  - Average remediation time (violation detected to fixed)
  - Proportion of critical violations remediated within 90 days
  - Departmental satisfaction with remediation guidance (survey)

**Baseline**: Estimated 40% compliance across public sector (NAO 2024 report)

**Target**: 70% compliance within 24 months

**Measurement Method**: Automated scan results aggregated quarterly, validated by sample manual audits

---

### Goal G-4: Developer-Friendly Integration Capability

**Derived From Drivers**: SD-4

**Goal Owner**: Service Owner

**Goal Statement**: Provide a documented, stable API and CI/CD pipeline integration that enables departmental web teams to scan their own sites during development, receiving remediation guidance before deployment, within 12 months.

**Why This Matters**: Reactive compliance scanning after deployment is less effective than shift-left accessibility testing during development. Departments want to prevent accessibility failures rather than remediate them post-publication.

**Success Metrics**:

- **Primary Metric**: Number of departments integrating scanning API into CI/CD pipelines
- **Secondary Metrics**:
  - API call volume per month
  - Developer satisfaction with API documentation (survey)
  - Reduction in post-deployment WCAG violations for API-integrated teams

**Baseline**: No centralised accessibility scanning API available

**Target**: 20+ departments integrating within 12 months, 50+ within 24 months

**Measurement Method**: API usage analytics, department onboarding tracker, developer survey

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Accessibility Barriers for Disabled Citizens

**Supported Goals**: G-1, G-2, G-3

**Outcome Statement**: Reduce the number of critical accessibility barriers encountered by disabled citizens on public sector websites by 50% within 24 months, measured by automated violation counts and user-reported barriers.

**Measurement Details**:

- **KPI**: Critical WCAG violations per 100 pages scanned
- **Current Value**: Estimated 12.3 critical violations per 100 pages (GDS sample audit 2025)
- **Target Value**: 6.2 critical violations per 100 pages
- **Measurement Frequency**: Monthly
- **Data Source**: Platform automated scanning results
- **Report Owner**: GDS Head of Accessibility

**Business Value**:

- **Strategic Impact**: UK becomes a global leader in public sector digital accessibility
- **Operational Impact**: Fewer accessibility complaints reduce departmental complaint-handling burden
- **Customer Impact**: Disabled citizens can access government services more independently

**Timeline**:

- **Phase 1 (Months 1-6)**: Baseline established, scanning at scale operational
- **Phase 2 (Months 7-12)**: First compliance improvement visible, remediation guidance driving change
- **Phase 3 (Months 13-24)**: 50% reduction target achieved
- **Sustainment (Year 2+)**: Continuous monitoring maintains gains, targets raised

---

### Outcome O-2: Cost-Efficient Compliance Monitoring

**Supported Goals**: G-1, G-4

**Outcome Statement**: Deliver public sector accessibility monitoring at less than 5% of the cost of equivalent manual auditing, achieving GBP 3-9M annual cost avoidance.

**Measurement Details**:

- **KPI**: Cost per website assessed annually
- **Current Value**: GBP 5,000-15,000 per manual audit
- **Target Value**: GBP 50-200 per website for automated + sampled blended assessment
- **Measurement Frequency**: Annually
- **Data Source**: Platform operating costs / number of websites monitored

---

## Complete Traceability Matrix

### Stakeholder - Driver - Goal - Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| GDS Director General | SD-1 | Demonstrable accessibility improvement | G-1 | 95% scanning coverage | O-1 | Reduced barriers for disabled citizens |
| GDS Director General | SD-1 | Demonstrable accessibility improvement | G-3 | 70% compliance rate | O-1 | Reduced barriers for disabled citizens |
| EHRC | SD-2 | Enforcement-grade evidence | G-1 | 95% scanning coverage | O-2 | Cost-efficient monitoring |
| EHRC | SD-2 | Enforcement-grade evidence | G-2 | Blended assessment methodology | O-1 | Reduced barriers for disabled citizens |
| RNIB | SD-3 | Lived experience in assessment | G-2 | Blended assessment methodology | O-1 | Reduced barriers for disabled citizens |
| Dept web teams | SD-4 | Achievable standards, clear guidance | G-3 | 70% compliance rate | O-1 | Reduced barriers for disabled citizens |
| Dept web teams | SD-4 | Achievable standards, clear guidance | G-4 | Developer-friendly API | O-2 | Cost-efficient monitoring |
| Scope | SD-5 | Cognitive accessibility | G-2 | Blended assessment methodology | O-1 | Reduced barriers for disabled citizens |
| Cabinet Office Finance | SD-6 | Cost-efficient monitoring | G-1 | 95% scanning coverage | O-2 | Cost-efficient monitoring |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: RNIB/Scope (SD-3, SD-5) want extensive lived-experience testing, but Cabinet Office Finance (SD-6) needs cost efficiency. Manual testing 12,000+ sites is not affordable.
  - **Resolution Strategy**: Tiered approach — automated scanning for all sites, blended assessment (automated + manual + user testing) for the 500 highest-traffic/highest-risk sites. Lived-experience panel funded centrally but deployed strategically.

- **Conflict 2**: EHRC (SD-2) wants enforcement-grade evidence from automated tools, but disability charities argue automated results alone are insufficient for fair enforcement since they miss 60% of barriers.
  - **Resolution Strategy**: Automated scan results used for risk-based prioritisation and monitoring trends, not as sole enforcement evidence. Blended assessment required before any enforcement action. EHRC and GDS to jointly develop evidence standards.

**Synergies**:

- **Synergy 1**: GDS Director General's need for measurable improvement (SD-1) aligns perfectly with departmental web teams' desire for actionable guidance (SD-4) — both benefit from the same remediation support capability
- **Synergy 2**: EHRC's enforcement needs (SD-2) and Cabinet Office Finance's cost-efficiency goal (SD-6) both benefit from automated scanning at scale — the same infrastructure serves both monitoring and enforcement evidence collection

---

## Communication & Engagement Plan

### GDS Director General

**Primary Message**: The platform will provide unprecedented visibility into public sector accessibility compliance, enabling evidence-based improvement and demonstrating UK leadership in digital inclusion.

**Communication Frequency**: Monthly

**Preferred Channel**: Programme board papers, dashboard demonstrations

### RNIB / Scope / Mencap

**Primary Message**: The platform combines automated scanning with meaningful lived-experience testing, ensuring that the voices and experiences of disabled people shape compliance assessment.

**Communication Frequency**: Quarterly

**Preferred Channel**: Disability Sector Advisory Group meetings, published methodology consultation

### Departmental Web Teams

**Primary Message**: The platform provides practical, developer-friendly tools and guidance to help you meet accessibility standards — it is a support tool, not just an inspection regime.

**Communication Frequency**: Monthly

**Preferred Channel**: GDS blog posts, developer documentation, API release notes, community of practice meetings

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Departmental web teams | Ad hoc accessibility testing, manual audits | Continuous automated monitoring, API integration | HIGH | MEDIUM | Training programme, phased rollout, support community |
| EHRC | Complaint-driven enforcement, expensive audits | Proactive monitoring data, risk-based enforcement | MEDIUM | LOW | Joint evidence standards development |
| Disability charities | Excluded from compliance assessment | Formal lived-experience testing panel role | MEDIUM | LOW | Co-design of methodology, panel recruitment support |
| GDS accessibility team | Manual sample-based auditing | Platform operators and methodology stewards | HIGH | LOW | Role evolution, upskilling on platform management |

### Change Readiness

**Champions** (Enthusiastic supporters):

- GDS Head of Accessibility — strong advocate for centralised monitoring
- RNIB — welcomes formal role in compliance assessment
- AbilityNet — sees commercial and mission opportunity in blended assessment

**Fence-sitters** (Neutral, need convincing):

- Departmental web teams — supportive in principle but concerned about unfunded mandate to fix issues
- EHRC — interested but cautious about automated evidence quality

**Resisters** (Opposed or skeptical):

- Some departments with poor accessibility records — fear of exposure and reputational damage
  - Strategy: Emphasise improvement support over naming-and-shaming; offer remediation assistance before publishing scores

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Disability Sector Rejects Automated-Only Assessment

**Related Stakeholders**: RNIB, Scope, Mencap, disabled citizens

**Risk Description**: Disability charities publicly criticise the platform as "accessibility theatre" if it relies primarily on automated scanning without meaningful lived-experience testing, undermining the platform's credibility.

**Impact on Goals**: G-2 (Blended assessment methodology), G-3 (Compliance improvement)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Co-design the blended assessment methodology with disability charities from Discovery. Secure ring-fenced budget for lived-experience testing panel. Publish methodology for public consultation.

---

### Risk R-2: Departments Lack Resources to Remediate

**Related Stakeholders**: Departmental web teams, GDS Director General

**Risk Description**: The platform identifies widespread accessibility failures but departments lack budget, skills, or mandate to fix them, resulting in no improvement despite monitoring — undermining the platform's purpose.

**Impact on Goals**: G-3 (Compliance improvement)

**Probability**: HIGH

**Impact**: HIGH

**Mitigation Strategy**: Provide prioritised remediation guidance (critical barriers first). Advocate for central remediation fund. Offer GDS accessibility consulting support for highest-priority services.

---

### Risk R-3: EHRC Enforcement Diverges from Platform Methodology

**Related Stakeholders**: EHRC, departmental web teams

**Risk Description**: EHRC develops enforcement methodology that does not align with platform assessment methodology, creating confusion about what "compliance" means and undermining departmental trust in the platform.

**Impact on Goals**: G-1 (Scanning coverage), G-2 (Blended methodology)

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Joint GDS-EHRC working group to develop aligned methodology and evidence standards. Formal MoU on data sharing and enforcement process.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Assessment methodology | GDS Head of Accessibility | SRO | EHRC, disability charities, AbilityNet | Departments |
| Budget approval | Cabinet Office Finance | SRO | CDDO, GDS CTO | All stakeholders |
| Scanning scope (which sites) | Service Owner | GDS Director General | CDDO, EHRC | Departments |
| Remediation guidance content | GDS Design Lead | GDS Head of Accessibility | Dept web teams, RNIB | All |
| Architecture decisions | GDS CTO | SRO | Security, CDDO | Development team |
| Enforcement evidence use | EHRC | EHRC Board | GDS, legal advisors | Departments |

### Escalation Path

1. **Level 1**: Product Manager / Service Owner (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, methodology disputes)
3. **Level 3**: GDS Director General (strategic direction, major stakeholder conflicts, ministerial escalation)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| GDS Director General | PENDING | | PENDING |
| GDS Head of Accessibility | PENDING | | PENDING |
| CDDO Director | PENDING | | PENDING |
| EHRC | PENDING | | PENDING |
| RNIB | PENDING | | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| PSBAR 2018 | Legislation | legislation.gov.uk | Accessibility monitoring requirements | N/A — external reference |
| WCAG 2.2 | Standard | W3C | Accessibility success criteria | N/A — external reference |
| NAO Digital Accessibility Report 2024 | Audit report | NAO | Public sector compliance baseline | N/A — external reference |
| GDS Service Standard | Standard | GOV.UK | 14 service standard points | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Accessibility Compliance Platform
**Model**: Claude Opus 4.6
