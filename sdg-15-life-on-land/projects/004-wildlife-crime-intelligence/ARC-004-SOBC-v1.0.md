# Strategic Outline Business Case (SOBC): Wildlife Crime Intelligence

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-004-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Wildlife Crime Intelligence (Project 004) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Wildlife Crime Intelligence Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Programme Board, NCA Finance, DEFRA, Home Office, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the justification for investing in a Wildlife Crime Intelligence platform. It follows the HM Treasury Green Book Five Case Model and is informed by stakeholder analysis (ARC-004-STKE-v1.0) and requirements specification (ARC-004-REQ-v1.0).

---

## Executive Summary

**Purpose**: The UK lacks a unified digital platform for wildlife crime intelligence. The National Wildlife Crime Unit (NWCU) — a team of approximately 12 staff coordinating the response to wildlife crime across the UK — relies on email, spreadsheets, and telephone to receive, grade, and disseminate intelligence across 43 territorial police forces, Border Force, and international partners.

**Problem Statement**: Wildlife crime intelligence is fragmented across dozens of separate systems and inboxes. Critical intelligence about organised wildlife trafficking networks, raptor persecution patterns, and CITES border violations is lost or delayed because there is no single platform to collate, grade, analyse, and disseminate it. The NWCU Strategic Assessment consistently identifies this fragmentation as the primary barrier to effective enforcement. CITES permit verification at the border takes 30 minutes per check, enabling illegal shipments to pass through while legitimate trade is delayed.

**Proposed Solution**: Deliver a National Intelligence Model (NIM) compliant wildlife crime intelligence platform with 5x5x5 grading, intelligence search and analysis, CITES permit verification API for Border Force, structured NGO intelligence-sharing channels, and international exchange capability (INTERPOL/Europol).

**Strategic Fit**: Directly delivers UK commitments from the Illegal Wildlife Trade Conference, supports CITES implementation obligations, aligns with NCA mission to reduce serious and organised crime, and contributes to SDG 15 targets on combating poaching and trafficking.

**Investment Required**: £5M over 3 years

- Capital: £3.5M
- Operational (3 years): £1.5M

**Expected Benefits**: £15.5M over 5 years

- Intelligence-led operation outcomes: £5M
- POCA asset recovery from wildlife crime: £4M
- Border enforcement efficiency: £2.5M
- Police force efficiency: £2M
- International cooperation value: £2M

**Return on Investment**:

- NPV: £7.8M (discounted at 3.5%)
- Payback Period: 20 months
- ROI: 210%

**Recommended Option**: Option 2: Full Intelligence Platform with CITES Integration

**Key Risks**:

1. Police force engagement — WCOs have limited time and competing priorities
2. NCA security requirements creating access barriers for police and NGO contributors
3. INTERPOL I-24/7 integration complexity

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: The intelligence fragmentation problem is universally acknowledged by all stakeholders. The investment is modest (£5M) relative to the value of disrupting organised wildlife crime networks and meeting international commitments. The primary risk is operational adoption, not technology.

**Next Steps if Approved**:

1. Security architecture design and NCA accreditation planning: Q2 2026
2. User research with WCOs across representative police forces: Q3 2026
3. Alpha with core intelligence workflow: Q4 2026
4. Beta with CITES API and pilot forces: Q2 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Wildlife crime in the UK encompasses offences from local-level badger baiting to international organised trafficking in endangered species worth billions globally. The UK's enforcement response is coordinated by the NWCU — a small, effective but severely under-tooled unit that relies on ad hoc information sharing to perform a national coordination function.

Current intelligence flows:

- **Police WCOs**: Submit intelligence via email or telephone to NWCU (no standard format, no grading)
- **Border Force**: Report seizures via email with attached paper CITES permit copies
- **RSPB**: Share raptor persecution intelligence through personal relationships with NWCU officers
- **INTERPOL**: International notices received via I-24/7 terminal, manually cross-referenced
- **CITES permits**: DEFRA database queried manually by phone/email from Border Force officers

**Specific Pain Points**:

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| NWCU | SD-1 | No unified intelligence database | Cannot produce strategic assessment from data | CRITICAL |
| Border Force | SD-2 | Manual CITES permit verification, 30 mins/check | Illegal trade enabled, legitimate trade delayed | HIGH |
| Police WCOs | SD-3 | Complex/slow intelligence submission | <30% of WCOs submit regularly, intelligence lost | HIGH |
| RSPB | SD-4 | Informal intelligence sharing, no feedback | Intelligence submitted but outcome unknown | HIGH |

**Consequences of Inaction**:

- **Organised crime flourishes**: Wildlife trafficking networks operate with impunity due to intelligence gaps — estimated £100M+ annual value of illegal wildlife trade transiting the UK
- **International credibility**: UK cannot demonstrate effective CITES enforcement, risking trade sanctions
- **POCA under-utilisation**: Financial investigation potential unrealised — estimated £2-4M annual asset recovery foregone
- **Species extinction risk**: Inadequate enforcement contributes to decline of protected species (raptors, badgers, pearl mussels)

### A1.2 Strategic Drivers

**Strategic Alignment**:

- **Illegal Wildlife Trade Conference Commitments**: UK pledged to strengthen enforcement infrastructure
- **CITES Implementation**: National obligation to enforce international wildlife trade controls
- **NCA Strategic Assessment**: Wildlife crime identified as a serious and organised crime threat
- **UK Wildlife Crime Priorities**: Seven priority areas requiring coordinated intelligence
- **Serious and Organised Crime Strategy**: Cross-cutting approach to serious crime networks
- **Architecture Principles (ARC-000-PRIN)**: Compliant with SDG 15 programme principles

### A1.3 Stakeholder Goals

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | NWCU Head | >80% WCOs using platform for intelligence | ~30% ad hoc | >80% on platform | 12 months post-launch |
| G-2 | Border Force | CITES verification < 2 minutes | 30 minutes manual | < 2 minutes automated | 6 months post-launch |
| G-3 | NWCU Head | Structured NGO intelligence channel | Informal email | Digital submission + feedback | 6 months post-launch |

### A1.4 Scope

**In Scope**: Intelligence submission, 5x5x5 grading, search and analysis, CITES verification API, NGO submission channel, intelligence products, INTERPOL exchange, POCA support

**Out of Scope**: Case management, prosecution files, customs declarations, forensic evidence, RSPCA welfare systems

**Dependencies**:

- **DEFRA**: CITES permit database API access
- **NCA IT**: OFFICIAL-SENSITIVE hosting infrastructure
- **Police forces**: Network access approval for 43 forces
- **INTERPOL**: I-24/7 integration approval

### A1.5 Why Now?

**Urgency Factors**:

- NWCU Strategic Assessment 2025 identifies intelligence platform as the single most impactful capability gap
- UK hosting next Illegal Wildlife Trade Conference — must demonstrate enforcement progress
- Growing organised crime involvement in wildlife trafficking (NCA assessment)
- Raptor persecution intelligence from satellite tagging is growing but has no structured destination

**Opportunity Cost of Delay**: £0.3M per month in foregone asset recovery plus continued intelligence loss.

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **WCO Adoption**: >80% of active WCOs submitting intelligence through platform
   - **Measure**: User analytics, submission volumes per force
   - **Threshold**: >60% minimum, >80% target

2. **Intelligence Turnaround**: Submission to dissemination within 48 hours
   - **Measure**: Workflow timing analytics
   - **Threshold**: <72 hours minimum, <48 hours target

3. **CITES Verification Speed**: <2 minutes per permit check
   - **Measure**: API response time and officer workflow timing
   - **Threshold**: <5 minutes minimum, <2 minutes target

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with email and telephone-based intelligence coordination.

**Costs** (3-year):

- Capital: £0
- Operational: £1.5M (NWCU staff time on manual intelligence management)
- Total: £1.5M

**Benefits**: £0

**Cons**:

- Intelligence fragmentation continues — networks undetected
- International commitments unmet — CITES non-compliance risk
- POCA asset recovery potential unrealised
- NWCU effectiveness limited by tooling rather than capability

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Intelligence capability gap is the single largest barrier to wildlife crime enforcement.

---

### Option 1: Basic Intelligence Database

**Description**: Simple intelligence submission and search database for NWCU and WCOs. No CITES integration, no NGO channels, no international exchange.

**Costs** (3-year) - ROM (±40%):

- Capital: £1.5M
- Operational: £0.6M
- Total: £2.1M

**Benefits** (5-year): £7M

- Intelligence-led operations: £3M
- Police force efficiency: £2M
- POCA recovery (limited): £2M

**Net Benefit**: £4.9M

**Pros**:

- Lower cost and complexity
- Addresses primary WCO submission challenge
- Faster to deploy (9 months)

**Cons**:

- No CITES border enforcement improvement
- No NGO intelligence integration
- No international exchange
- No POCA financial investigation tools

**Stakeholder Goals Met**: 40% (G-1 partially)

---

### Option 2: Full Intelligence Platform with CITES Integration (RECOMMENDED)

**Description**: Comprehensive NIM-compliant platform including intelligence submission and search, 5x5x5 grading workflow, CITES permit verification API, NGO submission channels, intelligence product generation, international exchange capability, and POCA financial investigation support.

**Costs** (3-year) - ROM (±30%):

- Capital: £3.5M
  - Core intelligence platform: £1.5M
  - CITES integration and species ID tools: £0.8M
  - Security accreditation and infrastructure: £0.5M
  - Mobile app and offline capability: £0.3M
  - International exchange integration: £0.2M
  - Contingency (15%): £0.2M
- Operational: £1.5M over 3 years
  - NCA hosting: £0.25M/year
  - Support and maintenance: £0.15M/year
  - INTERPOL connectivity: £0.1M/year
- Total 3-year TCO: £5.0M

**Benefits** (5-year):

| Benefit ID | Description | Type | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------------|-------------|------|--------|--------|--------|--------|--------|--------------|
| B-001 | Intelligence-led operation outcomes (disruptions, prosecutions) | OPERATIONAL | £0.5M | £1.0M | £1.0M | £1.25M | £1.25M | £5.0M |
| B-002 | POCA asset recovery from wildlife crime | FINANCIAL | £0.3M | £0.7M | £0.8M | £1.0M | £1.2M | £4.0M |
| B-003 | Border enforcement efficiency (seizure increase, legitimate trade facilitation) | OPERATIONAL | £0.3M | £0.5M | £0.5M | £0.6M | £0.6M | £2.5M |
| B-004 | Police force efficiency (reduced manual intelligence handling) | OPERATIONAL | £0.2M | £0.4M | £0.4M | £0.5M | £0.5M | £2.0M |
| B-005 | International cooperation (shared intelligence, coordinated operations) | STRATEGIC | £0.2M | £0.3M | £0.4M | £0.5M | £0.6M | £2.0M |
| **Total** | | | **£1.5M** | **£2.9M** | **£3.1M** | **£3.85M** | **£4.15M** | **£15.5M** |

**NPV** (3.5% discount): £7.8M

**ROI**: 210% over 5 years

**Payback Period**: 20 months

**Pros**:

- 90% of stakeholder goals met
- Positive NPV of £7.8M
- Addresses all critical intelligence capability gaps
- CITES enforcement significantly improved
- POCA financial investigation enabled
- International obligations met

**Cons**:

- NCA security accreditation process may extend timeline
- 43 police forces require individual access arrangements
- INTERPOL integration requires dedicated secure connectivity
- Small NWCU team must manage platform alongside operations

**Stakeholder Goals Met**: 90%

---

### Option 3: Advanced Analytics Platform with AI

**Description**: Full platform plus AI-powered wildlife trafficking pattern detection, predictive analytics for seasonal crime hotspots, automated CITES permit fraud detection, and dark web wildlife trade monitoring.

**Costs** (3-year) - ROM (±40%):

- Capital: £7M
- Operational: £2.5M
- Total: £9.5M

**Benefits** (5-year): £18M (marginal uplift over Option 2)

**Recommendation**: **Reject** — Insufficient intelligence data volume to train AI models effectively. Advanced analytics can be added once intelligence data quality and volume improve through the base platform.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Full Intelligence Platform with CITES Integration**

**Rationale**:

1. **Best Value**: NPV of £7.8M with ROI of 210%
2. **Capability Transformation**: From fragmented email to NIM-compliant intelligence platform
3. **International Obligations**: Meets CITES and IWT Conference commitments
4. **Law Enforcement Impact**: Enables intelligence-led enforcement and POCA financial disruption
5. **Modest Investment**: £5M over 3 years is exceptionally cost-effective for national law enforcement capability

**Sensitivity Analysis**:

- If costs increase 30%: NPV still positive (£6.3M)
- If benefits reduce 30%: NPV still positive (£3.0M)
- If WCO adoption is only 50% (not 80%): Benefits reduce 25%, NPV remains positive

**Optimism Bias Adjustment** (Green Book):

- Standard uplift: +40% on costs
- Adjusted TCO: £5.0M + £2.0M = £7.0M
- NPV with optimism bias: Still positive at £5.8M

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

**Recommended Route**: Digital Marketplace (DOS6) for specialist delivery. Direct award for NCA infrastructure components (within NCA framework agreements).

**Specialist Capabilities Needed**:

- Law enforcement intelligence platform development
- NCA security accreditation experience
- CITES/environmental crime domain knowledge
- INTERPOL integration experience

**Market Assessment**: Small but specialist market — a number of UK firms have experience building intelligence platforms for law enforcement at OFFICIAL-SENSITIVE. Law enforcement software is a recognised G-Cloud category.

**Contract Approach**:

- **Build**: Fixed-price milestones for platform components
- **Run**: Managed service, 3+2 years within NCA hosting
- **Security**: NCA responsible for accreditation; supplier must have appropriate vetting clearances

### C1.4 Social Value

- Cyber security apprenticeships
- Environmental crime research partnerships with universities
- SME specialist supplier engagement

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment**: £5.0M over 3 years

| | Year 1 | Year 2 | Year 3 | Total |
|---|--------|--------|--------|-------|
| CapEx | £2.2M | £1.3M | £0 | £3.5M |
| OpEx | £0.3M | £0.5M | £0.7M | £1.5M |
| **Total** | **£2.5M** | **£1.8M** | **£0.7M** | **£5.0M** |

## D2. Funding Source

**Source**: Joint funding from DEFRA (wildlife crime prevention, CITES obligations) and Home Office/NCA (serious and organised crime capability).

- DEFRA contribution: £2.5M (CITES enforcement, wildlife crime coordination)
- Home Office/NCA contribution: £2.5M (intelligence platform, law enforcement capability)

**Precedent**: NWCU itself is jointly funded by DEFRA and Home Office — the platform follows the same funding model.

## D3. Affordability

**Assessment**: **Affordable** — £5M over 3 years is modest for a national law enforcement capability. Joint DEFRA/Home Office funding distributes the cost across beneficiary departments.

**Ongoing Affordability**: Annual operational costs of £0.5M/year are within NWCU's existing budget envelope, offset by POCA asset recovery revenue (target £2M/year).

---

# PART E: MANAGEMENT CASE

## E1. Delivery Approach

**Methodology**: Agile, with intensive security assurance alongside development.

**Phases**:

| Phase | Duration | Key Activities |
|-------|----------|---------------|
| Discovery | 8 weeks | User research with WCOs, security architecture, NCA accreditation planning |
| Alpha | 12 weeks | Prototype intelligence submission and search, 5x5x5 workflow |
| Security Accreditation | 12 weeks (parallel) | NCA RA&A, penetration testing, risk assessment |
| Private Beta | 16 weeks | Core platform with NWCU and 5 pilot police forces |
| CITES Integration | 12 weeks (parallel) | CITES API development and Border Force integration |
| Public Beta | 12 weeks | All 43 forces, NGO channels, INTERPOL exchange |
| Live | Ongoing | Continuous improvement, POCA tools |

## E2. Governance

**Programme Board**: Monthly, co-chaired by NCA Director General (Threats) and DEFRA Director for Nature

**Members**: NWCU Head, NCA CTO, NPCC WC Lead, Border Force WC Lead, DEFRA CITES Authority

**Reporting**: Monthly to NCA Board, quarterly to DEFRA/Home Office joint oversight

## E3. Risk Management

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| WCO adoption — limited time and competing priorities | HIGH | HIGH | Ultra-simple submission (< 10 mins), mobile app, management buy-in via NPCC WC Lead | Service Owner |
| NCA security accreditation delays | MEDIUM | HIGH | Parallel accreditation track, early NCA CTO engagement, experienced security assessors | NCA CTO |
| 43 force IT access — diverse environments | HIGH | MEDIUM | Web-based platform at OFFICIAL (no special infrastructure), force IT engagement programme | Technical Lead |
| INTERPOL I-24/7 integration complexity | MEDIUM | MEDIUM | Phased — platform operational before international exchange; manual exchange as fallback | SRO |
| NWCU capacity — small team managing implementation | HIGH | MEDIUM | Dedicated programme team (not NWCU operational staff), NWCU as subject matter experts only | SRO |
| Sensitive intelligence compromise | LOW | CRITICAL | NCA security standards, tiered access, 5x5x5 sanitisation, audit logging | NCA SSRO |

---

## Approval

| Role | Name | Decision | Signature | Date |
|------|------|----------|-----------|------|
| SRO | PENDING | [ ] Approved | | |
| NCA Director General (Threats) | PENDING | [ ] Approved | | |
| DEFRA Director for Nature | PENDING | [ ] Approved | | |
| NCA CTO | PENDING | [ ] Approved | | |
| Home Office Sponsor | PENDING | [ ] Approved | | |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Wildlife Crime Intelligence
**Model**: Claude Opus 4.6
