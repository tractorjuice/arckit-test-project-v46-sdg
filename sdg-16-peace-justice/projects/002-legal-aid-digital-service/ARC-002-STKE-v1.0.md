# Stakeholder Drivers & Goals Analysis: Legal Aid Digital Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Legal Aid Digital Service (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Legal Aid Transformation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | LAA Executive Board, MoJ Digital, CDDO, Law Society |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Legal Aid Digital Service, analyses their underlying drivers, maps these to goals and measurable outcomes, and identifies conflicts and synergies that must be managed for successful delivery.

### Key Findings

The Legal Aid Digital Service faces a fundamental tension between improving efficiency (Treasury/LAA) and expanding access (legal profession/citizens). The LASPO Act 2012 dramatically reduced legal aid scope, and the Means Test Review 2023 has created significant policy changes that the current systems cannot implement efficiently. The strongest alignment exists around digitising the means test — all stakeholders agree that the current paper-based process is slow, error-prone, and frustrating. The most significant conflict is between the drive for automated eligibility determination (LAA/MoJ) and the legal profession's concern that automated systems may incorrectly deny legal aid to vulnerable individuals.

### Critical Success Factors

- Accurately implement the revised means test rules from the Means Test Review 2023 without errors that deny eligible citizens access to justice
- Reduce application-to-determination time from 20+ working days to under 5 working days
- Maintain solicitor engagement — if firms stop doing legal aid work because the system is too burdensome, access to justice collapses
- Integrate with HMCTS case management to provide real-time legal aid status at court hearings
- Pass GDS service assessment to maintain CDDO confidence

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need to digitise and accelerate the means test process, but tensions between automated determination (LAA efficiency) versus human review of complex cases (legal profession quality), and between cost containment (Treasury) versus expanding legal aid scope (access to justice advocates).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Lord Chancellor | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, legal aid policy |
| LAA Chief Executive | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| LAA Director of Digital | Digital transformation lead | HIGH | HIGH | Manage Closely — Architecture, delivery |
| LAA Casework Director | Operational delivery | HIGH | HIGH | Manage Closely — Process redesign, staff training |
| LAA Finance Director | Budget management | HIGH | MEDIUM | Keep Satisfied — Cost control, business case |
| LAA SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, data protection |
| LAA caseworkers | Frontline assessment staff | LOW | HIGH | Keep Informed — Workflow design, training |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| MoJ Policy Team | MoJ | Legal aid policy ownership | HIGH | HIGH |
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding | HIGH | MEDIUM |
| Law Society | Professional body | Solicitor representation | MEDIUM | HIGH |
| Bar Council | Professional body | Barrister representation | MEDIUM | HIGH |
| Legal Aid Practitioners Group (LAPG) | Professional network | Legal aid provider advocacy | LOW | HIGH |
| HMCTS | Partner agency | Court integration | MEDIUM | HIGH |
| Citizens Advice | Charity | Applicant support | LOW | HIGH |
| Legal aid applicants | Citizens | Service users | LOW | HIGH |
| HMRC | Partner department | Income verification data | MEDIUM | MEDIUM |
| DWP | Partner department | Benefits status verification | MEDIUM | MEDIUM |
| NAO | Parliament | Value for money | HIGH | MEDIUM |
| Justice Select Committee | Parliament | Oversight | HIGH | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * Lord Chancellor  |
        |  * NAO              |  * LAA CEO          |
        |  * Justice Select   |  * LAA Digital Dir  |
        |    Committee        |  * LAA Casework Dir |
        |  * LAA Finance      |  * MoJ Policy Team  |
 P      |  * LAA SIRO         |                     |
 O      |  * CDDO             |                     |
 W      +---------------------+---------------------+
 E      |                     |                     |
 R      |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * HMRC             |  * Law Society      |
        |  * DWP              |  * Bar Council      |
        |                     |  * LAPG             |
        |                     |  * Citizens Advice  |
        |                     |  * Applicants       |
        |                     |  * LAA caseworkers  |
        |                     |  * HMCTS            |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Lord Chancellor — Implementing the Means Test Review and Restoring Access to Justice

**Stakeholder**: Lord Chancellor and Secretary of State for Justice

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Successfully implement the means test changes from the Legal Aid Means Test Review 2023, demonstrating that the government is expanding access to legal aid and reducing barriers for vulnerable citizens, while maintaining fiscal responsibility.

**Context & Background**:
The LASPO Act 2012 removed legal aid for many areas of civil law, generating sustained criticism that access to justice has been undermined. The Means Test Review 2023 raised income and capital thresholds, bringing an estimated 2 million additional people into eligibility. However, these changes require system changes that the current LAA infrastructure cannot deliver efficiently. The Lord Chancellor faces parliamentary questions on legal aid deserts, the withdrawal of solicitors from legal aid work, and the impact on access to justice for vulnerable communities.

**Driver Intensity**: CRITICAL

**Enablers**:

- Rapid implementation of revised means test rules in the digital system
- Visible improvement in application-to-determination times
- Data demonstrating expanded eligibility and increased legal aid take-up

**Blockers**:

- Legacy systems unable to implement complex new means test rules quickly
- Solicitor firms continuing to leave legal aid work due to low fees and administrative burden
- Negative media coverage of eligibility errors (false denials)

**Related Stakeholders**: MoJ Policy (rule design), LAA CEO (delivery), Law Society (practitioner viability), Applicants (beneficiaries)

---

### SD-2: LAA Chief Executive — Operational Efficiency and Accurate Determinations

**Stakeholder**: LAA Chief Executive

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Transform the legal aid application and determination process from a paper-heavy, slow, error-prone operation into an efficient digital service that delivers accurate eligibility determinations within 5 working days, reducing unit cost per determination while maintaining accuracy.

**Context & Background**:
The LAA processes approximately 300,000 legal aid applications per year across criminal and civil categories. The current process relies heavily on paper forms, manual data entry by caseworkers, and manual verification of financial information. Average determination time exceeds 20 working days for civil cases. Error rates in means test calculations are unacceptably high, leading to both false grants (costing the legal aid fund) and false denials (denying citizens access to justice). The LAA CEO is accountable for the GBP 1.7 billion annual legal aid fund.

**Driver Intensity**: CRITICAL

**Enablers**:

- Automated income verification through HMRC and DWP data sharing
- Digital application form with guided entry and real-time validation
- Rules engine implementing the full means test with automated determination for straightforward cases
- Human review reserved for complex cases

**Blockers**:

- HMRC and DWP unwilling or unable to provide real-time income verification APIs
- Means test rules too complex for reliable automation
- Caseworker resistance to workflow changes
- Legacy system data migration risks

**Related Stakeholders**: LAA Casework Director (operations), HMRC/DWP (data sharing), Law Society (application quality), Treasury (cost control)

---

### SD-3: Law Society — Reducing Administrative Burden on Legal Aid Practitioners

**Stakeholder**: Law Society

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Reduce the administrative burden of legal aid applications on solicitor firms, which is a significant factor in firms' decisions to withdraw from legal aid work, threatening the sustainability of the legal aid provider base.

**Context & Background**:
Legal aid fee rates have been substantially cut and have not kept pace with inflation. The administrative burden of legal aid applications — completing complex forms, gathering evidence of means, chasing LAA for determination decisions — makes legal aid work financially unviable for many firms. Legal aid deserts (areas with no legal aid providers) are growing. The Law Society has warned that the legal aid provider base is approaching a tipping point where access to justice cannot be maintained.

**Driver Intensity**: HIGH

**Enablers**:

- Simple, fast digital application process (under 30 minutes per application)
- Real-time eligibility pre-check before full application
- Transparent determination tracking with clear decision reasoning
- API access for integration with practice management software

**Blockers**:

- System that is more complex than paper forms
- Additional registration or accreditation requirements
- Slow response times or frequent downtime
- Lack of mobile-responsive design for solicitors working in court or police stations

**Related Stakeholders**: LAPG (practitioner network), Bar Council (barrister legal aid), LAA CEO (provider sustainability), Lord Chancellor (access to justice)

---

### SD-4: Legal Aid Applicants — Fast, Fair, Dignified Access to Legal Representation

**Stakeholder**: Legal aid applicants (approximately 300,000 per year)

**Driver Category**: CUSTOMER / USER

**Driver Statement**: Apply for legal aid through a simple, fast process that treats them with dignity, provides clear information about eligibility, and delivers a determination quickly enough to be useful — ideally before their court hearing or legal problem escalates.

**Context & Background**:
Legal aid applicants are often in crisis — facing criminal charges, domestic abuse, housing eviction, family breakdown, or immigration detention. The current application process requires detailed financial disclosure through complex paper forms, with determination times that often exceed the timescale of the legal problem. Applicants may be unaware they are eligible, or may be deterred from applying by the complexity of the process.

**Driver Intensity**: HIGH

**Enablers**:

- Plain-language online application with guidance at every step
- Real-time eligibility indication (before full application)
- Rapid determination (under 5 working days)
- Clear, understandable decision letters with explanation of reasoning
- Assisted digital support for applicants who cannot self-serve

**Blockers**:

- Complex financial disclosure requirements
- Digital-only service excluding vulnerable applicants
- Opaque decision-making with unclear rejection reasons
- Long waiting times during which the legal problem escalates

**Related Stakeholders**: Citizens Advice (support), Law Society (application assistance), HMCTS (court deadline pressure)

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Application-to-Determination Time to Under 5 Working Days

**Derived From Drivers**: SD-1, SD-2, SD-3, SD-4
**Goal Owner**: LAA Chief Executive
**Goal Statement**: Reduce the average time from legal aid application submission to eligibility determination from 20+ working days to under 5 working days for all application types within 12 months of deployment.

**Success Metrics**:

- **Primary Metric**: Average working days from application to determination
- **Baseline**: 20+ working days (civil), 5 working days (criminal — already faster)
- **Target**: Under 5 working days for all categories
- **Measurement Method**: LAA case management data

---

### Goal G-2: Implement Means Test Review 2023 Rules Accurately

**Derived From Drivers**: SD-1, SD-2
**Goal Owner**: MoJ Policy Team (rules), LAA Digital Director (implementation)
**Goal Statement**: Implement the revised means test thresholds and rules from the 2023 review with zero critical calculation errors, bringing an estimated 2 million additional citizens into eligibility.

**Success Metrics**:

- **Primary Metric**: Means test calculation accuracy rate (target: 99.9%)
- **Secondary Metric**: Number of additional citizens assessed as eligible under new thresholds

---

### Goal G-3: Reduce Solicitor Application Time to Under 30 Minutes

**Derived From Drivers**: SD-3, SD-2
**Goal Owner**: LAA Director of Digital
**Goal Statement**: Reduce the time solicitors spend completing a legal aid application from approximately 2 hours (paper) to under 30 minutes (digital) within 6 months of deployment.

**Success Metrics**:

- **Primary Metric**: Average solicitor time per application (minutes)
- **Baseline**: Approximately 120 minutes per application
- **Target**: Under 30 minutes
- **Measurement Method**: Solicitor time-tracking survey and system analytics

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Lord Chancellor | SD-1 | Implement means test review | G-1 | Sub-5-day determination | O-1 | Faster access to representation |
| Lord Chancellor | SD-1 | Implement means test review | G-2 | Accurate new rules | O-2 | Expanded eligibility |
| LAA CEO | SD-2 | Operational efficiency | G-1 | Sub-5-day determination | O-1 | Faster access |
| LAA CEO | SD-2 | Operational efficiency | G-2 | Accurate new rules | O-2 | Expanded eligibility |
| Law Society | SD-3 | Reduce admin burden | G-3 | Sub-30-min application | O-3 | Sustainable provider base |
| Applicants | SD-4 | Fast, fair access | G-1 | Sub-5-day determination | O-1 | Faster access |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: LAA CEO (SD-2) wants automated determination for efficiency, while Law Society (SD-3) wants human review for complex cases to protect vulnerable applicants from incorrect automated denials.
  - **Resolution Strategy**: Tiered approach — automated determination for straightforward cases (clear eligibility or ineligibility), mandatory human review for cases near thresholds, complex income, or vulnerability indicators. Transparent algorithm with audit trail.

- **Conflict 2**: HM Treasury wants cost containment of the GBP 1.7B legal aid fund, while Lord Chancellor (SD-1) needs to expand eligibility under the Means Test Review, increasing the fund.
  - **Resolution Strategy**: Demonstrate that digital efficiency savings offset the cost of expanded eligibility. Faster, more accurate means testing reduces overpayments and fraudulent claims.

**Synergies**:

- **Synergy 1**: All stakeholders agree that faster determination times benefit everyone — applicants get representation sooner, solicitors get paid sooner, LAA reduces caseworker burden, and the Lord Chancellor can demonstrate improvement
- **Synergy 2**: Automated income verification from HMRC/DWP satisfies LAA's efficiency goals (SD-2) and reduces applicants' disclosure burden (SD-4) simultaneously

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | LAA Finance | LAA CEO | HM Treasury, CDDO | All |
| Means test rules | MoJ Policy | Lord Chancellor | LAA, Law Society | All |
| System architecture | LAA Digital Dir | LAA CEO | HMCTS, CDDO | All |
| Go/No-go deployment | LAA CEO | Lord Chancellor | All key stakeholders | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Legal Aid Means Test Review 2023 | Policy | MoJ | Revised thresholds, eligibility expansion | N/A — external reference |
| LASPO Act 2012 | Legislation | legislation.gov.uk | Legal aid scope and eligibility | N/A — external reference |
| Legal Aid Statistics | Data | MoJ/LAA | 300,000 applications/year, GBP 1.7B fund | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Legal Aid Digital Service
**Model**: Claude Opus 4.6
