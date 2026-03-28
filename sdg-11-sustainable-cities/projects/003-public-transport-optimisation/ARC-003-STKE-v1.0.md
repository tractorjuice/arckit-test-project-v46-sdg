# Stakeholder Drivers & Goals Analysis: Public Transport Optimisation

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Public Transport Optimisation (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Public Transport Optimisation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Public Transport Optimisation Programme Board, DfT, Combined Authorities, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Public Transport Optimisation platform, their drivers, goals, and measurable outcomes. The platform will enable multi-modal transport planning, real-time scheduling optimisation, and open data publication to improve bus, rail, and active travel services across England.

### Key Findings

The Public Transport Optimisation platform sits at the intersection of a deregulated bus market, franchised rail system, and devolved combined authority responsibilities. The strongest alignment exists around improving real-time passenger information — every stakeholder benefits from passengers having accurate, timely journey data. The most significant tension is between bus operators (who view route and patronage data as commercially confidential) and combined authorities (who need that data to plan networks and enforce Bus Service Improvement Plans). The mandatory Bus Open Data Service (BODS) requirements provide a regulatory lever, but compliance remains patchy.

### Critical Success Factors

- Achieve 95%+ BODS compliance across all operators in participating areas
- Reduce passenger wait time variability by 20% through real-time schedule optimisation
- Integrate bus, rail, tram, and active travel data into a unified multi-modal data platform
- Support Bus Service Improvement Plan (BSIP) delivery for at least 10 combined/local transport authorities
- Comply with DfT Accessible Information Regulations for real-time passenger information

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Consensus on the need for better transport data and passenger information, but structural tensions between commercial bus operators, combined authorities with franchising ambitions, and DfT's national policy objectives. The rail sector operates under different regulatory and data frameworks, adding integration complexity.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Transport | DfT Minister | HIGH | HIGH | Manage Closely — Ministerial briefings |
| DfT Director of Buses and Taxis | Policy ownership | HIGH | HIGH | Manage Closely — BSIP alignment |
| SRO, Public Transport Optimisation | Programme Sponsor (DfT) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DfT BODS Team | Bus Open Data Service management | HIGH | HIGH | Manage Closely — Data standards co-design |
| DfT Data Science Unit | Analytical capability | MEDIUM | HIGH | Keep Informed — Model development |
| DfT Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Combined Authority Transport Directors | MCAs (GMCA, WMCA, WYCA, etc.) | Key delivery partners | HIGH | HIGH |
| Transport for London | TfL | Model of best practice, data partner | HIGH | HIGH |
| Bus Operators (Big 5) | First, Stagecoach, Arriva, Go-Ahead, National Express | Regulated data providers | HIGH | HIGH |
| SME Bus Operators | Community and independent operators | Data compliance challenge | LOW | HIGH |
| Network Rail | Infrastructure manager | Rail data integration | HIGH | MEDIUM |
| Train Operating Companies | Franchised operators | Rail timetable and real-time data | MEDIUM | HIGH |
| Traveline | National travel information service | Journey planning consumer | MEDIUM | HIGH |
| Transport Focus | Passenger watchdog | Passenger interests | MEDIUM | HIGH |
| Bus Users UK | Charity | Passenger advocacy | LOW | HIGH |
| CDDO | Cabinet Office | Spend control and assurance | HIGH | MEDIUM |
| HM Treasury | Funding approval | Funding | HIGH | MEDIUM |
| Passengers | Citizens | Service users | LOW | HIGH |
| Traffic Commissioners | DfT regulatory | Bus registration and compliance | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | End-to-end transport data service | HIGH / HIGH | Manage Closely — Service reviews |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control gates |

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State for Transport — Delivering Bus Service Improvement

**Stakeholder**: Secretary of State for Transport

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Deliver visible improvements to bus services outside London, demonstrating that the Bus Services Act 2017 and Bus Service Improvement Plans are producing tangible results for passengers — more reliable services, better information, and integrated ticketing.

**Context & Background**:
Bus patronage outside London has declined 30% since 2010, with the Covid-19 pandemic accelerating decline. £2 billion in Bus Service Improvement Plan funding has been allocated, but delivery is patchy. The Minister needs evidence that investment is working — real-time data on service performance, patronage trends, and passenger satisfaction. The "Get Around for £2" fare cap has boosted patronage but strained operator economics, increasing the need for operational efficiency.

**Driver Intensity**: CRITICAL

**Enablers**:
- Real-time service performance dashboards showing BSIP impact
- Data-driven evidence for funding allocation decisions

**Blockers**:
- Operators withholding commercially sensitive data
- Combined authorities lacking analytical capability to use the data

---

### SD-2: Combined Authority Transport Directors — Network Planning with Data

**Stakeholder**: Combined Authority Transport Directors (GMCA, WMCA, WYCA, etc.)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Access comprehensive, real-time transport data to plan bus networks effectively under new franchising powers, identify gaps in provision, optimise timetables, and monitor operator performance against Bus Service Improvement Plans — capabilities that currently require expensive consultancy or don't exist at all.

**Context & Background**:
The Bus Services Act 2017 gave combined authorities franchising powers (following the Manchester model). Franchising requires detailed understanding of route economics, patronage patterns, and service reliability — data that operators currently control. Combined authorities are investing in Enhanced Partnership arrangements as a stepping stone to franchising but lack the data infrastructure to monitor operator compliance. Several authorities have tried building their own analytics platforms at costs of £1-5M each.

**Driver Intensity**: CRITICAL

**Enablers**:
- Centralised access to BODS data with analytical tools
- Multi-modal data integration (bus + rail + tram + active travel)

**Blockers**:
- Operator resistance to sharing commercially sensitive data beyond BODS minimums
- Varying data maturity across combined authorities

---

### SD-3: Bus Operators — Protecting Commercial Interests While Complying

**Stakeholder**: Bus Operators (First, Stagecoach, Arriva, Go-Ahead, National Express and SME operators)

**Driver Category**: COMMERCIAL / COMPLIANCE

**Driver Statement**: Comply with mandatory BODS requirements at minimum cost while protecting commercially sensitive route and patronage data from competitors and from combined authorities who might use it to support franchising cases that threaten the commercial model.

**Context & Background**:
Bus operators are required to publish timetable, fares, and real-time data through BODS. However, compliance varies — timetable data is reasonably complete but fares data and real-time vehicle location data remain incomplete. Operators view granular patronage and revenue data as commercially confidential. The tension with combined authorities is existential for some operators — franchising transfers route planning authority from operators to local government, and operators fear their own data being used to justify franchising assessments.

**Driver Intensity**: HIGH

**Enablers**:
- Clear boundaries on what data is mandatory (BODS) vs. voluntary
- Platform features that help operators optimise their own networks

**Blockers**:
- Combined authorities using the platform to build franchising evidence
- Additional data publication requirements beyond BODS mandatory minimums

---

### SD-4: Transport Focus — Passenger Experience and Accessibility

**Stakeholder**: Transport Focus (statutory passenger watchdog)

**Driver Category**: CUSTOMER / COMPLIANCE

**Driver Statement**: Ensure the platform delivers tangible improvements to passenger experience — accurate real-time information, accessible journey planning, and consistent service quality data that enables Transport Focus to hold operators and authorities to account on behalf of passengers.

**Context & Background**:
Transport Focus's National Bus Passenger Survey consistently shows that real-time information accuracy is a top passenger concern. Passengers report buses marked "2 minutes" on displays that never arrive, apps showing services that were cancelled hours earlier, and no information at all at many bus stops. The Accessible Information Regulations require operators to provide audible and visible next-stop announcements, but compliance monitoring is difficult without accurate real-time data.

**Driver Intensity**: HIGH

**Enablers**:
- High-quality real-time feeds validated against actual vehicle positions
- Accessibility compliance monitoring data

**Blockers**:
- Operators publishing inaccurate real-time data that misleads passengers
- Platform focused on authority/operator needs at expense of passenger-facing improvements

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 95% BODS Compliance in Participating Areas

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: DfT BODS Team

**Goal Statement**: Achieve 95% or higher BODS compliance scores (timetable, fares, and real-time data) for all operators in at least 10 combined/local transport authority areas within 12 months.

**Why This Matters**: Provides the data foundation for all analytics (SD-1) and ensures operators meet regulatory obligations (SD-3).

**Success Metrics**:
- **Primary Metric**: BODS compliance score by operator and authority area
- **Secondary Metrics**: Number of operators publishing fares data in NeTEx format; real-time feed uptime percentage

**Baseline**: Overall BODS compliance approximately 72% (DfT 2025 assessment)
**Target**: 95% across timetable, fares, and real-time for participating areas
**Measurement Method**: BODS quality dashboard

---

### Goal G-2: Reduce Passenger Wait Time Variability by 20%

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: SRO, Public Transport Optimisation

**Goal Statement**: Reduce the coefficient of variation in passenger wait times by 20% in participating areas through real-time schedule optimisation and better headway management within 18 months.

**Why This Matters**: Directly improves passenger experience (SD-4), demonstrates BSIP value (SD-1), and provides combined authorities with evidence of platform impact (SD-2).

**Success Metrics**:
- **Primary Metric**: Coefficient of variation in wait times at key stops
- **Secondary Metrics**: Excess Wait Time (EWT) metric; passenger satisfaction scores

**Baseline**: Average EWT of 2.8 minutes (Transport Focus survey 2025)
**Target**: EWT reduced to 2.2 minutes or less
**Measurement Method**: AVL data analysis, Transport Focus passenger surveys

---

### Goal G-3: Integrated Multi-Modal Data Platform Serving 10+ Transport Authorities

**Derived From Drivers**: SD-2

**Goal Owner**: SRO, Public Transport Optimisation

**Goal Statement**: Deploy an integrated multi-modal transport data platform (bus, rail, tram, active travel) serving at least 10 combined or local transport authorities within 18 months.

**Why This Matters**: Enables network-wide planning that reflects how passengers actually travel (multi-modal), not just single-mode analysis.

**Success Metrics**:
- **Primary Metric**: Number of transport authorities actively using the platform
- **Secondary Metrics**: Number of transport modes integrated per authority; analytics queries per month

**Baseline**: 0 (new platform)
**Target**: 10+ authorities, 3+ modes per authority
**Measurement Method**: Platform analytics, authority adoption tracker

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Bus service improvement | G-1 | 95% BODS compliance | O-1 | Better bus services |
| Secretary of State | SD-1 | Bus service improvement | G-2 | Reduce wait variability | O-1 | Better bus services |
| Combined Authorities | SD-2 | Network planning with data | G-3 | Multi-modal platform | O-2 | Data-driven planning |
| Bus Operators | SD-3 | Compliance at minimum cost | G-1 | BODS compliance | O-1 | Better bus services |
| Transport Focus | SD-4 | Passenger experience | G-2 | Reduce wait variability | O-1 | Better bus services |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Combined Authorities (SD-2) want comprehensive operator data for franchising assessments, but Bus Operators (SD-3) want to limit data sharing to BODS mandatory minimums to protect commercial interests and the deregulated model.
  - **Resolution Strategy**: Platform provides BODS-compliant data only. Additional data sharing governed by Enhanced Partnership or franchising legal frameworks, not platform architecture. Platform does not extract or publish data beyond operators' BODS obligations.

- **Conflict 2**: DfT (SD-1) wants rapid deployment to show BSIP results, but SME operators lack technical capability to publish compliant BODS data on the required timescale.
  - **Resolution Strategy**: Funded BODS compliance support programme for SME operators. Simplified data publication tools within the platform. Phased compliance targets (large operators first, SMEs with 12-month grace period).

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Bus Services Act 2017 | Legislation | legislation.gov.uk | BODS mandate, franchising powers | N/A — external reference |
| BODS Technical Specification | Standard | DfT | TransXChange, SIRI-VM, NeTEx requirements | N/A — external reference |
| Bus Service Improvement Plans | Policy | DfT/LTAs | Local bus strategy and funding | N/A — external reference |
| Accessible Information Regulations | Legislation | DfT | Real-time accessible passenger info | N/A — external reference |
| NaPTAN | Standard | DfT | National stop/station reference | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Public Transport Optimisation (Project 003)
**Model**: Claude Opus 4.6
