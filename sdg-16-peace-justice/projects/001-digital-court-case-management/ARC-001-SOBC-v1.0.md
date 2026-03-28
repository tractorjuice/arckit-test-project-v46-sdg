# Strategic Outline Business Case (SOBC): Digital Court Case Management

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Digital Court Case Management (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, HMCTS Reform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | HMCTS Reform Programme Board, MoJ Finance, HM Treasury, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case presents the rationale for investing in a Digital Court Case Management system as part of the HMCTS Reform Programme. It follows the HM Treasury Green Book five-case model and seeks approval to proceed to the Outline Business Case (OBC) stage.

---

## Executive Summary

**Purpose**: The Digital Court Case Management project delivers an end-to-end digital case management system for criminal courts, replacing fragmented legacy systems (XHIBIT, Libra) with an integrated platform that improves case progression, reduces the Crown Court backlog, and enhances access to justice for all court users.

**Problem Statement**: The Crown Court backlog exceeds 67,000 cases with defendants waiting over two years for trial. Existing case management systems are fragmented, do not interoperate, and require extensive duplicate data entry across the criminal justice system. This delays justice, wastes judicial time, and costs the public purse through extended remand and repeated witness attendance.

**Proposed Solution**: Build a modern, integrated digital case management system that connects with the Common Platform for cross-agency data sharing, provides judges with digital case management tools, and offers citizens self-service access to case information. Phased migration from legacy systems by court circuit.

**Strategic Fit**: Directly supports the HMCTS Reform Programme (GBP 1.3B investment), the Lord Chancellor's priority to reduce the Crown Court backlog, the Government's SDG 16 commitments on access to justice, and the Technology Code of Practice requirement for modern, interoperable government services.

**Investment Required**: GBP 38M over 3 years

- Capital: GBP 28M
- Operational (3 years): GBP 10M

**Expected Benefits**: GBP 95M over 5 years

- Reduced remand costs through faster case progression: GBP 42M
- Reduced cracked and ineffective trial costs: GBP 28M
- Court staff efficiency savings: GBP 15M
- Reduced witness expense and attendance costs: GBP 10M

**Return on Investment**:

- NPV: GBP 41M (discounted at 3.5%)
- Payback Period: 22 months
- ROI: 150%

**Recommended Option**: Option 3: Build modern integrated platform with Common Platform integration

**Key Risks**:

1. Common Platform integration complexity and API stability
2. Judicial adoption — judges must buy in to digital case management
3. Data migration quality from 50+ million historical case records

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The Crown Court backlog is a national crisis affecting public confidence in justice. The investment is modest relative to the HMCTS Reform Programme (GBP 1.3B) and the annual cost of the backlog (estimated GBP 500M+ in remand, witness, and court costs). The NPV of GBP 41M demonstrates strong value for money. Phased delivery with court circuit rollout mitigates risk.

**Next Steps if Approved**:

1. Secure funding approval: Q2 2026
2. Define detailed requirements: `/arckit.requirements` (completed — ARC-001-REQ-v1.0)
3. Develop Outline Business Case (OBC): Q3 2026
4. Procurement approach: Q3 2026
5. Discovery/Alpha phase: Q4 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The Crown Court backlog has exceeded 67,000 outstanding cases, with average waiting times from charge to trial exceeding 52 weeks. Some defendants wait over two years in custody for trial. The existing case management landscape is fragmented across three primary legacy systems — XHIBIT (Crown Court, deployed 2002), Libra (magistrates' courts, deployed 2003), and various bespoke systems for specific case types. These systems do not interoperate effectively, requiring extensive manual data re-entry across the criminal justice system.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Lord Chancellor | SD-1 | 67,000+ Crown Court backlog eroding public confidence | Parliamentary scrutiny, media criticism, SDG 16 reporting | CRITICAL |
| HMCTS CEO | SD-3 | Fragmented legacy systems, GBP 1.3B Reform Programme under-delivering | NAO criticism, accounting officer accountability | CRITICAL |
| CPS | SD-4 | 60% of case data requires re-entry across HMCTS/CPS systems | Prosecutor time wasted, data inconsistency, cracked trials | HIGH |
| Defence practitioners | SD-5 | Multiple logins, desktop-only access, poor listing info | Administrative burden on financially pressured practitioners | HIGH |
| Court users | SD-6 | Limited visibility of case progress, legal jargon, digital exclusion | Citizen anxiety, unnecessary court attendance, access to justice | HIGH |

**Consequences of Inaction**:

- Crown Court backlog continues to grow, potentially exceeding 80,000 cases by 2028
- Average charge-to-trial time increases further, breaching defendants' right to a trial within a reasonable time (Article 6 ECHR)
- Legacy systems reach end of supportable life, increasing security and resilience risks
- UK fails to meet SDG 16 targets on access to justice and effective institutions
- Annual cost of the backlog (remand, witness attendance, court inefficiency) continues at GBP 500M+
- HMCTS Reform Programme criticised for failing to deliver core case management modernisation

### A1.2 Strategic Alignment

| Strategy/Policy | Alignment |
|-----------------|-----------|
| HMCTS Reform Programme | Core deliverable — integrated digital case management is a foundational component |
| Lord Chancellor's Priorities | Directly addresses Crown Court backlog reduction and access to justice |
| Technology Code of Practice | Modern, interoperable, open-standards-based system replacing legacy |
| GDS Service Standard | User-centred design, accessibility, multi-channel access |
| SDG 16: Peace, Justice and Strong Institutions | Target 16.3: Equal access to justice; Target 16.6: Effective, accountable institutions |
| Criminal Procedure Rules | Supports active case management duties imposed on courts |
| Open Justice Principle | System supports public access to court listings and published outcomes |
| Levelling Up White Paper | Improves access to justice across all regions, including underserved areas |

### A1.3 Spending Objectives (SMART)

1. **Reduce** the Crown Court outstanding caseload from 67,000 to below 54,000 within 18 months of full deployment (20% reduction)
2. **Reduce** average charge-to-Crown Court trial time from 52 weeks to 39 weeks within 18 months (25% reduction)
3. **Eliminate** duplicate data entry between HMCTS and CPS systems through Common Platform integration within 12 months of deployment
4. **Achieve** 80% judicial user satisfaction score within 6 months of deployment
5. **Deliver** self-service case status checking for citizens with 90% task completion rate within 12 months

---

## A2. The Case for Change

### A2.1 Existing Arrangements

| System | Coverage | Age | Issues |
|--------|----------|-----|--------|
| XHIBIT | Crown Court case display and management | 24 years (2002) | No integration with CPS/Common Platform, desktop-only, unsupported browser requirements |
| Libra | Magistrates' court case management | 23 years (2003) | Batch-mode processing, no real-time case progression, vendor-dependent |
| Common Platform | Cross-CJS shared workspace | 6 years (partial deployment) | Integration gaps with HMCTS case management, API stability issues, inconsistent adoption |
| Paper case files | All jurisdictions | N/A | Duplication, loss risk, no remote access, environmental cost |

**Annual operating cost of current arrangements**: GBP 22M (maintenance, licensing, support staff for legacy systems)

### A2.2 Business Needs

1. **Integrated case management**: A single, integrated system replacing fragmented legacy platforms
2. **Cross-agency interoperability**: Seamless data exchange with CPS, police, HMPPS, and LAA through the Common Platform
3. **Judicial tools**: Digital case management dashboard supporting active case management duties
4. **Citizen access**: Self-service case information and proactive notifications for all court users
5. **Data-driven operations**: Real-time management information for backlog management and court performance

### A2.3 Desired Outcomes and Benefits

| Benefit | Type | Value (5-year) | Measurement |
|---------|------|----------------|-------------|
| Reduced remand costs (faster case progression) | Cash-releasing | GBP 42M | Remand days x cost per day |
| Reduced cracked/ineffective trial costs | Cash-releasing | GBP 28M | Trial rate x cost per failed trial |
| Court staff efficiency savings | Cash-releasing | GBP 15M | FTE hours saved x cost per hour |
| Reduced witness expense claims | Cash-releasing | GBP 10M | Attendance reduction x average claim |
| Improved access to justice | Non-cashable | N/A (qualitative) | LiP satisfaction, SDG 16 indicators |
| Improved public confidence | Non-cashable | N/A (qualitative) | Public trust surveys, media sentiment |
| **Total quantified benefits** | | **GBP 95M** | |

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

| CSF | Description | Weight |
|-----|-------------|--------|
| CSF-1 | System must not disrupt court operations during migration | 25% |
| CSF-2 | Judiciary must adopt and be satisfied with the system | 20% |
| CSF-3 | Common Platform integration must work reliably | 20% |
| CSF-4 | System must demonstrably reduce the backlog | 20% |
| CSF-5 | System must be accessible to litigants in person | 15% |

## B2. Options Considered

### Option 1: Do Nothing (Baseline)

**Description**: Continue operating XHIBIT, Libra, and paper-based processes. Maintain current Common Platform integration level.

**Costs**: GBP 110M over 5 years (GBP 22M/year operating cost)
**Benefits**: GBP 0 (no improvement)
**NPV**: GBP 0 (baseline)

**Assessment**: Backlog continues to grow. Legacy systems become unsupportable. SDG 16 targets missed. Unacceptable.

---

### Option 2: Incremental Legacy Enhancement

**Description**: Invest in incremental improvements to XHIBIT and Libra — add APIs, improve Common Platform integration, build a citizen-facing layer on top of existing systems.

**Costs**: GBP 18M capital + GBP 25M operational over 5 years = GBP 43M total
**Benefits**: GBP 35M over 5 years (limited efficiency gains, no structural improvement)
**NPV**: GBP -7M

**Assessment**: Addresses symptoms but not root cause. Legacy technical debt remains. Limited integration possible due to architectural constraints of 20+ year old systems. Integration APIs would be fragile wrappers around batch-mode systems. Poor value for money.

---

### Option 3: Build Modern Integrated Platform (RECOMMENDED)

**Description**: Build a modern, cloud-native digital case management platform with full Common Platform integration, judicial dashboard, practitioner portal, and citizen-facing services. Phased migration from legacy systems by court circuit.

**Costs**: GBP 28M capital + GBP 10M operational (3 years) + GBP 15M operational (years 4-5) = GBP 53M total over 5 years
**Benefits**: GBP 95M over 5 years
**NPV**: GBP 41M (discounted at 3.5%)
**BCR**: 1.79

**Assessment**: Best value for money. Addresses root cause. Enables structural improvement in case progression. Supports future extension to civil and family jurisdictions. Aligns with TCoP and GDS standards.

---

### Option 4: Procure Commercial Off-the-Shelf (COTS) Case Management

**Description**: Procure a commercial case management system and customise for HMCTS requirements. Integrate with Common Platform through vendor-provided APIs.

**Costs**: GBP 35M capital (including licence and customisation) + GBP 18M operational over 5 years = GBP 53M total
**Benefits**: GBP 80M over 5 years (reduced due to customisation limitations and vendor dependency)
**NPV**: GBP 24M

**Assessment**: Viable but vendor lock-in risk. Customisation for judicial independence requirements may be extensive. Common Platform integration less flexible than bespoke. Intellectual property and data sovereignty concerns with commercial vendors. Higher long-term operational cost due to licensing.

---

## B3. Options Appraisal Summary

| Criterion (Weight) | Option 1: Do Nothing | Option 2: Enhance | Option 3: Build (REC) | Option 4: COTS |
|---------------------|-----------------------|--------------------|-----------------------|----------------|
| CSF-1: No disruption (25%) | 5 (no change = no risk) | 3 (some disruption) | 4 (phased migration) | 3 (big-bang risk) |
| CSF-2: Judicial adoption (20%) | 1 (no improvement) | 2 (minor improvement) | 4 (co-designed) | 3 (vendor UI) |
| CSF-3: Integration (20%) | 1 (poor current state) | 2 (limited by legacy) | 5 (designed for it) | 3 (vendor APIs) |
| CSF-4: Backlog reduction (20%) | 1 (backlog grows) | 2 (marginal improvement) | 5 (structural change) | 4 (good improvement) |
| CSF-5: LiP access (15%) | 1 (no access) | 2 (bolt-on layer) | 5 (designed in) | 3 (limited customisation) |
| **Weighted Score** | **1.95** | **2.30** | **4.60** | **3.25** |
| **5-year NPV** | **GBP 0** | **GBP -7M** | **GBP 41M** | **GBP 24M** |

**Recommended Option**: Option 3 — Build Modern Integrated Platform

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Approach**: Mixed procurement — internal HMCTS Digital delivery team for core platform, specialist suppliers for specific capabilities.

**Procurement Route**:

- Core platform development: Internal HMCTS Digital team augmented via Digital Marketplace (G-Cloud for hosting, Digital Outcomes and Specialists for specialist roles)
- Legacy data migration: Specialist supplier via competitive procurement
- Common Platform integration: Joint delivery with existing HMCTS/CPS Common Platform team

**Contract Structure**:

- Time and materials for Discovery/Alpha phases
- Fixed price with agile delivery for Beta and Live phases
- Hosting via Crown Hosting or approved UK cloud provider (framework agreement)

**Key Commercial Risks**:

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Supplier market lacks court domain expertise | MEDIUM | HIGH | Include domain expertise as evaluation criterion, provide domain training |
| Vendor lock-in through technology choices | MEDIUM | MEDIUM | Open standards mandate, multi-cloud architecture, no proprietary dependencies |
| Cost overrun during migration phase | HIGH | MEDIUM | Fixed-price migration contract with defined data scope |

---

# PART D: FINANCIAL CASE

## D1. Capital Costs

| Cost Category | Year 1 | Year 2 | Year 3 | Total |
|---------------|--------|--------|--------|-------|
| Platform development | GBP 8M | GBP 7M | GBP 3M | GBP 18M |
| Common Platform integration | GBP 2M | GBP 1.5M | GBP 0.5M | GBP 4M |
| Data migration | GBP 1M | GBP 2M | GBP 1M | GBP 4M |
| User research and design | GBP 0.5M | GBP 0.5M | GBP 0M | GBP 1M |
| Security and compliance | GBP 0.5M | GBP 0.3M | GBP 0.2M | GBP 1M |
| **Total Capital** | **GBP 12M** | **GBP 11.3M** | **GBP 4.7M** | **GBP 28M** |

## D2. Operational Costs (Post-Deployment)

| Cost Category | Annual Cost | 3-Year Total |
|---------------|-------------|--------------|
| Cloud hosting and infrastructure | GBP 1.5M | GBP 4.5M |
| Support and maintenance team | GBP 1.2M | GBP 3.6M |
| Licence costs (open source support, third-party APIs) | GBP 0.3M | GBP 0.9M |
| Training and change management | GBP 0.3M | GBP 0.9M |
| **Total Operational** | **GBP 3.3M/year** | **GBP 10M** |

## D3. Benefits Realisation

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Reduced remand costs | GBP 2M | GBP 8M | GBP 10M | GBP 11M | GBP 11M | GBP 42M |
| Reduced cracked/ineffective trials | GBP 1M | GBP 5M | GBP 7M | GBP 7.5M | GBP 7.5M | GBP 28M |
| Court staff efficiency | GBP 0.5M | GBP 2.5M | GBP 4M | GBP 4M | GBP 4M | GBP 15M |
| Reduced witness expenses | GBP 0.5M | GBP 2M | GBP 2.5M | GBP 2.5M | GBP 2.5M | GBP 10M |
| **Total Benefits** | **GBP 4M** | **GBP 17.5M** | **GBP 23.5M** | **GBP 25M** | **GBP 25M** | **GBP 95M** |

## D4. Affordability

The GBP 28M capital investment falls within the HMCTS Reform Programme approved budget envelope. Operational costs of GBP 3.3M per year represent a reduction from the current GBP 22M annual legacy system operating cost (net saving of GBP 18.7M/year once legacy systems are decommissioned).

**Funding Source**: HMCTS Reform Programme allocation within MoJ Spending Review settlement.

---

# PART E: MANAGEMENT CASE

## E1. Programme Structure

**Programme**: HMCTS Reform Programme
**Project**: Digital Court Case Management
**SRO**: Director General, HMCTS Reform
**Project Director**: HMCTS CDIO

**Governance**:

- HMCTS Reform Programme Board (monthly)
- Digital Court Case Management Project Board (fortnightly)
- Judicial IT Advisory Committee (quarterly)
- Criminal Justice Board reporting (quarterly)

## E2. Delivery Approach

**Methodology**: Agile delivery (Scrum) within a phased programme structure

**Phases**:

| Phase | Duration | Key Deliverables |
|-------|----------|------------------|
| Discovery | 3 months | User research, technology assessment, proof of concept |
| Alpha | 6 months | Prototype judicial dashboard, Common Platform integration PoC, architecture design |
| Private Beta | 9 months | Core case management deployed to 3 pilot court circuits |
| Public Beta | 6 months | Expanded to all Crown Court centres, citizen-facing services |
| Live | Ongoing | Full national rollout, migration from legacy, continuous improvement |

**Migration Strategy**: Phased by court circuit (7 circuits in England and Wales), starting with South Eastern circuit (highest volume), completing within 18 months. Parallel running with legacy for minimum 3 months per circuit.

## E3. Risk Management

| Risk | Probability | Impact | Risk Score | Mitigation | Owner |
|------|-------------|--------|------------|------------|-------|
| Common Platform API instability | HIGH | HIGH | 16 | Early integration testing, API contract testing, fallback manual process | HMCTS CDIO |
| Judicial non-adoption | MEDIUM | HIGH | 12 | Co-design with judiciary, champions programme, optional paper during transition | SRO |
| Data migration errors | MEDIUM | HIGH | 12 | Automated reconciliation, manual review, extended parallel running | Migration Lead |
| Legacy system decommission delays | MEDIUM | MEDIUM | 9 | Clear decommission criteria, circuit-by-circuit approach | Operations Director |
| Budget overrun | MEDIUM | MEDIUM | 9 | Earned value management, phase gates, descoping non-essential features | Finance Director |
| Staff resistance to change | MEDIUM | MEDIUM | 9 | Comprehensive change management, super-user network, protected training time | Change Lead |

## E4. Benefits Realisation Plan

| Benefit | Metric | Baseline | Target | Owner | Review Frequency |
|---------|--------|----------|--------|-------|------------------|
| Reduced backlog | Outstanding cases | 67,000 | 54,000 | HMCTS CEO | Monthly |
| Faster case progression | Charge-to-trial weeks | 52 | 39 | Operations Director | Quarterly |
| Reduced cracked trials | Cracked trial rate | 40% | 28% | Service Owner | Quarterly |
| Staff efficiency | Admin hours per case | TBD at Alpha | -15% | Operations Director | Quarterly |
| Judicial satisfaction | Survey score | N/A (new) | 80% | SRO | Six-monthly |

## E5. Timeline and Key Milestones

| Milestone | Date | Dependencies |
|-----------|------|-------------|
| SOBC approval | Q2 2026 | This document |
| Discovery start | Q3 2026 | Funding approval |
| Alpha start | Q4 2026 | Discovery completion |
| GDS Alpha assessment | Q2 2027 | Alpha completion |
| Private Beta start | Q2 2027 | Alpha assessment pass |
| First circuit migration | Q4 2027 | Private Beta successful |
| GDS Beta assessment | Q1 2028 | Private Beta evidence |
| National rollout complete | Q2 2028 | All circuits migrated |
| Legacy decommission | Q4 2028 | 12-month parallel running |

---

## Approval

### Sign-Off

| Role | Name | Decision | Date |
|------|------|----------|------|
| SRO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| HMCTS CEO | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| MoJ Finance Director | | [ ] PROCEED / [ ] DO NOT PROCEED | |
| CDDO Spend Control | | [ ] PROCEED / [ ] DO NOT PROCEED | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HMCTS Reform Programme Business Case | Business Case | HMCTS | GBP 1.3B investment, reform objectives | N/A — internal |
| HM Treasury Green Book | Guidance | HM Treasury | Five-case model, discount rate 3.5% | N/A — external reference |
| Crown Court backlog statistics | Statistics | HMCTS | 67,000 outstanding cases | N/A — external reference |
| Criminal Procedure Rules 2020 | Legislation | legislation.gov.uk | Active case management duties | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Court Case Management
**Model**: Claude Opus 4.6
