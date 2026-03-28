# Stakeholder Drivers & Goals Analysis: Apprenticeship Matching Service

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Apprenticeship Matching Service (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Apprenticeship Matching Service Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | AMS Programme Board, DfE Apprenticeships Directorate, ESFA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Apprenticeship Matching Service (AMS), their underlying drivers, and how these translate into goals and measurable outcomes. The AMS will connect prospective apprentices with employers offering apprenticeship vacancies, replacing the ageing Find an Apprenticeship service with a modern, skills-matched platform.

### Key Findings

The apprenticeship ecosystem faces a paradox: employers report difficulty filling apprenticeship vacancies (35% unfilled in 2025) while young people report difficulty finding relevant opportunities. The current Find an Apprenticeship service is a basic vacancy listing with no skills matching, limited employer support, and poor mobile experience. The strongest stakeholder alignment exists around improving match quality — employers want candidates with relevant aptitude, while apprentices want roles that match their career interests and are accessible from their location. The key conflict is between large Levy-paying employers (who want premium features) and SMEs (who need simplicity and are critical for apprenticeship volume).

### Critical Success Factors

- Increase apprenticeship vacancy fill rate from 65% to 80% within 18 months
- Achieve 50,000 successful matches in Year 1 (20% improvement on current)
- Reduce time from application to start from average 12 weeks to 6 weeks
- Ensure 30% of matches involve disadvantaged young people (care leavers, SEND, FSM-eligible)
- Integrate with Apprenticeship Service employer accounts and ESFA funding systems

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM-HIGH

Strong alignment on the need for a better matching service. Tensions exist between large employers (want sophisticated features) and SMEs (want simplicity), and between training providers (who want to maintain intermediary role) and DfE (who want direct employer-apprentice connection).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Minister for Skills | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DfE Apprenticeships Director | Policy lead | HIGH | HIGH | Manage Closely — Policy alignment |
| SRO, AMS Programme | Programme Sponsor | HIGH | HIGH | Manage Closely — Programme board |
| ESFA Chief Executive | Funding and regulation | HIGH | HIGH | Manage Closely — Funding integration |
| DfE CDO | Digital leadership | HIGH | MEDIUM | Keep Satisfied — Architecture governance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Large Levy-Paying Employers | Private sector | Apprenticeship creators | HIGH | HIGH |
| SME Employers | Private sector | Volume apprenticeship providers | MEDIUM | HIGH |
| Young People (16-24) | Citizens | Apprenticeship seekers | LOW | HIGH |
| Career Changers (25+) | Citizens | Adult apprenticeship seekers | LOW | HIGH |
| Training Providers (FE Colleges, ITPs) | Education/private | Delivery partners | HIGH | HIGH |
| IfATE / Skills England | Standards body | Apprenticeship standards | HIGH | MEDIUM |
| National Apprenticeship Service (NAS) | DfE | Current service operator | HIGH | HIGH |
| Careers & Enterprise Company | Charity | Careers guidance | MEDIUM | HIGH |
| Schools and Sixth Forms | Education | Source of apprenticeship applicants | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance | HIGH | MEDIUM |
| Jobcentre Plus (DWP) | Partner department | Unemployment support | MEDIUM | MEDIUM |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * CDDO             |  * Minister Skills  |
        |  * DfE CDO          |  * Apprenticeships  |
        |  * IfATE/Skills Eng |    Director          |
        |                     |  * SRO              |
        |                     |  * ESFA CEO         |
 P      |                     |  * Levy Employers   |
 O      |                     |  * Training Provs.  |
 W      |                     |  * NAS              |
 E      +---------------------+---------------------+
 R      |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * Jobcentre Plus   |  * Young People     |
        |                     |  * Career Changers  |
        |                     |  * SME Employers    |
        |                     |  * Schools/6th Form |
        |                     |  * Careers & Ent. Co|
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: Minister for Skills — Increase Apprenticeship Starts and Reduce Youth Unemployment

**Stakeholder**: Minister for Skills

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Increase apprenticeship starts to meet the government's target of 500,000 new starts per year, with a particular focus on young people aged 16-24 in disadvantaged communities, demonstrating that apprenticeships are a prestigious, high-quality route into skilled employment.

**Context & Background**: Apprenticeship starts have declined from 509,000 (2015/16) to approximately 337,000 (2024/25), partly due to Levy reforms encouraging employers to invest in higher-level (and more expensive) apprenticeships for existing staff rather than entry-level opportunities for young people. The Minister needs a matching service that specifically drives new entry-level starts.

**Driver Intensity**: CRITICAL

---

### SD-2: Large Levy-Paying Employers — Talent Pipeline and Levy Utilisation

**Stakeholder**: Large Levy-Paying Employers (organisations with payroll > GBP 3M)

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Maximise return on Apprenticeship Levy investment by accessing a diverse, high-quality pipeline of apprenticeship candidates matched to their specific skill requirements, reducing vacancy fill times and improving retention rates.

**Context & Background**: Levy-paying employers contribute 0.5% of payroll to the Apprenticeship Levy. Unspent Levy expires after 24 months. Large employers want a platform that actively matches candidates to their vacancies based on skills, aptitude, and location — not just a passive listing. They also want integration with their HR systems for seamless onboarding.

**Driver Intensity**: HIGH

---

### SD-3: SME Employers — Simplicity and Support

**Stakeholder**: SME Employers (< 250 employees)

**Driver Category**: OPERATIONAL / RISK

**Driver Statement**: Find suitable apprenticeship candidates quickly and easily, with guidance on the apprenticeship process, without the administrative complexity that currently deters small businesses from offering apprenticeships.

**Context & Background**: SMEs account for 60% of apprenticeship starts but find the current system complex. Many struggle with the Apprenticeship Service account, training provider selection, and vacancy creation. They need a simple, guided experience that handles complexity behind the scenes.

**Driver Intensity**: HIGH

---

### SD-4: Young People (16-24) — Finding the Right Opportunity

**Stakeholder**: Young People seeking apprenticeships

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Find apprenticeship opportunities that match their interests, skills, and location, with clear information about what the role involves, what qualifications they will gain, and what career progression looks like — accessible on a mobile phone.

**Context & Background**: Young people report that the current Find an Apprenticeship service is difficult to navigate, does not help them understand which roles suit their interests, and provides inadequate information about career outcomes. They compare the experience unfavourably to commercial job platforms (Indeed, LinkedIn) and expect a modern, mobile-first experience.

**Driver Intensity**: HIGH

---

### SD-5: Training Providers — Maintaining Market Position

**Stakeholder**: Training Providers (FE Colleges and Independent Training Providers)

**Driver Category**: FINANCIAL / STRATEGIC

**Driver Statement**: Ensure that the matching service supports rather than disintermediates training providers, maintaining their role in connecting employers with apprentices and delivering high-quality training.

**Context & Background**: Training providers currently play a critical intermediary role — they recruit apprentices, match them with employers, and deliver the training. A matching service that enables direct employer-apprentice connection could undermine their business model. However, providers also see an opportunity for a better platform to increase overall apprenticeship volumes, benefiting everyone.

**Driver Intensity**: HIGH

---

### SD-6: ESFA — Funding Integration and Compliance

**Stakeholder**: Education and Skills Funding Agency

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Ensure that the matching service integrates with ESFA funding systems so that matched apprenticeships automatically trigger the correct funding pathway (Levy, co-investment, or SME incentive), with compliance checks built into the matching workflow.

**Driver Intensity**: HIGH

---

## Driver-to-Goal Mapping

### Goal G-1: Increase Vacancy Fill Rate from 65% to 80%

**Derived From Drivers**: SD-1, SD-2, SD-3
**Goal Owner**: SRO
**Success Metrics**: Percentage of listed apprenticeship vacancies that result in a confirmed start

---

### Goal G-2: 50,000 Successful Matches in Year 1

**Derived From Drivers**: SD-1, SD-4
**Goal Owner**: Service Owner
**Success Metrics**: Number of confirmed apprenticeship starts originating from AMS matches

---

### Goal G-3: 30% of Matches Involve Disadvantaged Young People

**Derived From Drivers**: SD-1
**Goal Owner**: DfE Apprenticeships Director
**Success Metrics**: Percentage of successful matches where the apprentice is care-experienced, SEND, or from an area of high deprivation (IMD decile 1-3)

---

### Goal G-4: Reduce Time from Application to Start from 12 Weeks to 6 Weeks

**Derived From Drivers**: SD-2, SD-3, SD-4
**Goal Owner**: SRO
**Success Metrics**: Median elapsed time from first application to apprenticeship start date

---

### Goal G-5: Integrate with Apprenticeship Service and ESFA Funding

**Derived From Drivers**: SD-6
**Goal Owner**: DfE CDO
**Success Metrics**: Percentage of matches where funding pathway is automatically determined; zero manual funding interventions required

---

## Conflict Analysis

- **Conflict 1**: Large employers (SD-2) want sophisticated matching algorithms and premium features, but SMEs (SD-3) need simplicity — feature complexity could overwhelm small businesses
  - **Resolution Strategy**: Tiered experience — simple guided flow for SMEs; advanced features (bulk vacancy management, HR integration, analytics) for large employers. Same platform, different entry points.

- **Conflict 2**: Training providers (SD-5) want to maintain intermediary role, but DfE (SD-1) wants direct employer-apprentice connection to improve transparency
  - **Resolution Strategy**: Compromise — providers remain visible as delivery partners, can recommend candidates, and are matched alongside vacancies. Platform enhances rather than replaces provider role. Provider quality ratings visible to employers and apprentices.

- **Conflict 3**: Minister (SD-1) wants increased Level 2-3 starts for young people, but Levy employers (SD-2) prefer Level 4-7 apprenticeships for existing staff
  - **Resolution Strategy**: Platform design — prominent placement of entry-level opportunities; "first apprenticeship" filter for young people; analytics showing employer's entry-level vs upskilling split.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Matching algorithm design | Technical Lead | CDO | Employers, Providers, Young People | ESFA |
| Funding integration | ESFA | SRO | DfE Finance, Training Providers | Employers |
| Disadvantage targeting | Apprenticeships Dir. | Minister | Careers & Enterprise Co, DWP | Schools |
| Provider quality ratings | SRO | ESFA CEO | IfATE, Providers | Employers, Apprentices |
| Go/No-go for live | SRO | Apprenticeships Dir. | All | All |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Apprenticeships Accountability Statement | Policy | DfE | Government apprenticeship targets | N/A — external reference |
| Skills for Jobs White Paper | Policy | DfE | Skills system reform | N/A — external reference |
| Apprenticeship Funding Rules | Guidance | ESFA | Funding pathways and eligibility | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Apprenticeship Matching Service
**Model**: Claude Opus 4.6
