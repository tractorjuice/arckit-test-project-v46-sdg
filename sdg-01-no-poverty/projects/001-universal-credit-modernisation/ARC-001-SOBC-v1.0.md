# Strategic Outline Business Case (SOBC): Universal Credit Modernisation

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | Universal Credit Modernisation (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Universal Credit Modernisation Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DWP Programme Board, HM Treasury Spending Team, CDDO, NAO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case sets out the case for investment in the modernisation of the Universal Credit digital platform. It follows the HM Treasury Green Book Five Case Model and is informed by the stakeholder analysis (ARC-001-STKE-v1.0) and requirements specification (ARC-001-REQ-v1.0). UC processes GBP 36B+ annually for approximately 6 million households. This SOBC seeks approval to proceed to the Outline Business Case (OBC) stage.

---

## Executive Summary

**Purpose**: Universal Credit is the UK's largest welfare programme, disbursing over GBP 36 billion annually to approximately 6 million households. The current digital platform has accumulated significant technical debt, resulting in slow claim processing, limited policy agility, and an inability to scale for surge demand. This business case seeks GBP 470M over 5 years to modernise the platform.

**Problem Statement**: Average new claim processing takes 23 working days, claimant satisfaction is 68% (below GDS benchmarks), and the system cannot accommodate policy changes faster than several months. The COVID-19 pandemic exposed critical scalability weaknesses when claims surged 7x. Continued operation on the current platform costs GBP 85M/year and rising.

**Proposed Solution**: A phased modernisation programme replacing the claims processing engine with a configurable rules-based platform, delivering a mobile-first claimant experience, and establishing modern integrations with HMRC, local authorities, and devolved administrations.

**Strategic Fit**: Directly supports the government's commitment to SDG 1: No Poverty by ensuring the primary UK safety net is accessible, efficient, and responsive. Aligns with the DWP Digital Strategy, GDS Service Standard, Technology Code of Practice, and Spending Review commitments.

**Investment Required**: GBP 470M over 5 years

- Capital: GBP 340M
- Operational (5 years transitional): GBP 130M

**Expected Benefits**: GBP 1.08B over 10 years

- Operational cost savings: GBP 180M/year by Year 3 (GBP 25M direct, GBP 155M processing efficiency)
- Error reduction savings: GBP 45M/year (reduced overpayments and mandatory reconsiderations)
- Channel shift savings: GBP 28M/year (reduced telephony volume)

**Return on Investment**:

- NPV: GBP 312M (discounted at 3.5% over 10 years)
- Payback Period: 38 months
- ROI: 130% over 10 years

**Recommended Option**: Option 2: Phased Platform Modernisation

**Key Risks**:

1. Payment disruption during migration — mitigated by phased approach with parallel running
2. HMRC RTI data freshness improvement dependency — mitigated by interim enhanced batch processing
3. Digital talent recruitment in competitive market — mitigated by competitive pay frameworks and apprenticeships

**Go/No-Go Recommendation**: **PROCEED** to Outline Business Case

**Rationale**: The current platform is unsustainable. Operational costs are rising, policy agility is inadequate for government needs, and the platform cannot withstand another demand surge. The recommended option delivers strong positive NPV with acceptable risk through phased delivery.

**Next Steps if Approved**:

1. Develop Outline Business Case (OBC): July 2026
2. Commence Alpha phase: September 2026
3. GDS Alpha assessment: December 2026
4. Procurement for specialist integration services: Q1 2027

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Universal Credit was designed and built from 2012 onward, with the current digital platform evolving through multiple iterations. While the system successfully processes payments for 6 million households monthly, it has accumulated substantial technical debt. The monolithic architecture limits the pace of change, makes policy implementation slow, and creates operational risk during demand surges.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Secretary of State | SD-1 | Cannot demonstrate rapid improvement to claimant experience | Parliamentary scrutiny, media criticism | CRITICAL |
| UC Operations Director | SD-3 | System struggles under surge demand; 23-day average processing time | Claimant hardship, staff pressure | CRITICAL |
| DWP CDIO | SD-4 | Technical debt prevents modern architecture; difficulty recruiting digital talent | 30% developer attrition, slow feature velocity | HIGH |
| HM Treasury | SD-5 | Rising operational costs (GBP 85M/year) with diminishing returns | Spending Review pressure | HIGH |
| UC Claimants | SD-6 | Complex, slow process with unclear status; 68% satisfaction | 6 million households affected | CRITICAL |
| HMRC | SD-7 | Fragile data exchange with limited error handling | Incorrect assessments from stale RTI data | HIGH |

**Consequences of Inaction**:

- Operational costs rise to GBP 100M/year within 3 years as legacy support costs escalate
- Next demand surge (economic downturn, policy change) risks system failure affecting millions
- Unable to implement policy changes at pace required by government (e.g., annual uprating taking 4+ months)
- Increasing NAO scrutiny of value for money as platform ages
- Digital talent attrition accelerates as platform becomes less attractive to engineers

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: This business case is informed by stakeholder analysis documented in ARC-001-STKE-v1.0.

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative |
|-----------|-------------|-------------|-------------------|---------------------|
| SD-1 | Secretary of State | POLITICAL | Demonstrable improvement to claimant experience | SDG 1 delivery, Ministerial accountability |
| SD-3 | UC Operations | OPERATIONAL | Payment continuity and operational efficiency | Service reliability for 6M households |
| SD-4 | DWP CDIO | STRATEGIC | Modern architecture enabling policy agility | Digital transformation, talent retention |
| SD-5 | HM Treasury | FINANCIAL | Cost containment and value for money | Public spending efficiency |
| SD-6 | Claimants | CUSTOMER | Simple, fast, dignified access to entitlements | Citizen outcomes, poverty reduction |

**Strategic Alignment**:

- **SDG 1: No Poverty**: Modernised UC directly improves access to the UK's primary safety net, reducing barriers that prevent vulnerable people from accessing support
- **DWP Digital Strategy 2025-2030**: Platform modernisation is the flagship initiative
- **GDS Service Standard**: New service must pass Alpha, Beta, and Live assessments
- **Technology Code of Practice**: Open standards, reusable components, no vendor lock-in
- **Architecture Principles (ARC-000-PRIN-v1.0)**: Principles 1 (User-Centred), 3 (Resilience), 4 (Interoperability), 5 (Security by Design), 15 (Maintainability)

### A1.3 Stakeholder Goals

**Goals Addressed** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | UC Service Owner | Reduce claim processing from 23 to 10 working days | 23 days | 10 days | March 2028 |
| G-2 | Service Owner | Achieve 85% claimant satisfaction | 68% | 85% | March 2028 |
| G-3 | CDIO | Deploy policy changes within 2 weeks | 3-6 months | 2 weeks | March 2028 |
| G-4 | Treasury | Reduce operational cost by GBP 25M/year | GBP 85M/year | GBP 60M/year | Year 3 |
| G-5 | Operations | Support 200K concurrent users without degradation | 80K (degraded) | 200K (stable) | March 2027 |

### A1.4 Scope

**In Scope**:

- Claims processing engine replacement with configurable rules engine
- Claimant-facing digital service (GOV.UK integrated, mobile-first)
- Staff tooling (Work Coach case management, Service Centre interface)
- Integration modernisation (HMRC RTI, local authority housing, devolved platforms)
- Data migration from legacy platform (6 million active claims)
- Staff training programme (25,000+ staff)
- GOV.UK platform integrations (One Login, Notify, Pay)

**Out of Scope** (for this phase):

- Legacy benefit migration to UC (JSA, ESA managed migration — separate programme)
- Sanctions and compliance policy redesign
- Jobcentre Plus physical estate
- Pension Credit and State Pension systems

**Interfaces**:

- **HMRC**: RTI earnings data (inbound), claimant verification requests (outbound)
- **Local Authorities**: Housing cost verification (bidirectional), direct payment instructions (outbound)
- **Devolved Administrations**: Scottish choices configuration, Scottish Child Payment data
- **GOV.UK**: One Login (identity), Notify (communications), Pay (advances)
- **DWP Payment System**: BACS payment file generation

**Assumptions**:

1. GOV.UK One Login supports benefits-level identity proofing by Q4 2026 — risk if wrong: alternative identity pathway needed
2. HMRC commits to 24-hour RTI data freshness — risk if wrong: interim enhanced batch (4x daily)
3. 60% of local authorities adopt API within 24 months — risk if wrong: batch adapter maintained
4. GBP 470M budget envelope maintained through Spending Review period — risk if wrong: scope reduction required

**Dependencies**:

- **Internal**: DWP cloud platform operational by Q3 2026
- **External**: GOV.UK One Login readiness, HMRC RTI improvement commitment
- **Technical**: UK sovereign cloud availability with required security accreditation

### A1.5 Why Now?

**Urgency Factors**:

- Current platform support costs increasing 8% year-on-year as technical debt compounds
- Next economic downturn will trigger UC claim surge that the current platform may not withstand
- GDS has signalled that the current service would not pass a live reassessment
- Key vendor contracts expire in 2027, creating a natural modernisation window
- Spending Review settlement includes modernisation funding that will be reallocated if not utilised

**Opportunity Cost of Delay**:

- GBP 15M per year in escalating legacy support costs
- GBP 45M per year in avoidable overpayments and errors (current error rate)
- Reputational risk from system failure during demand surge — unquantifiable but catastrophic
- Loss of GBP 470M Spending Review allocation if not committed by FY 2027-28

**Window of Opportunity**:

- Spending Review funding available and ring-fenced for modernisation
- Vendor contract renewal creates natural migration point
- GOV.UK platform maturity (One Login, Notify, Pay) enables modern service design
- DWP Digital has built internal capability through smaller projects, ready for flagship programme

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

1. **Payment Continuity**: Zero unplanned payment disruptions affecting claimants during modernisation
   - **Measure**: Number of unplanned payment failures affecting >0.01% of claimants
   - **Threshold**: Zero

2. **Processing Time Improvement**: Demonstrable reduction in claim processing time
   - **Measure**: Average new claim processing time (working days)
   - **Threshold**: 10 working days by March 2028

3. **Claimant Satisfaction**: Measurable improvement in citizen experience
   - **Measure**: GDS transaction satisfaction survey score
   - **Threshold**: 85% by March 2028

4. **Cost Efficiency**: Operational cost reduction demonstrated
   - **Measure**: Annual operational cost
   - **Threshold**: GBP 60M/year by Year 3 (down from GBP 85M)

5. **Policy Agility**: Faster deployment of policy changes
   - **Measure**: Time from policy confirmation to production deployment
   - **Threshold**: 2 weeks for standard policy changes

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue operating the current UC platform with incremental patches and fixes.

**Costs** (5-year):

- Capital: GBP 0
- Operational: GBP 500M (GBP 85M/year rising to GBP 115M by Year 5)
- Total: GBP 500M

**Benefits**: GBP 0 (no improvement; deterioration expected)

**Pros**:

- No upfront investment
- No migration risk

**Cons**:

- Operational costs escalate 8% annually as legacy support becomes more expensive
- System may fail under next demand surge, causing payment disruption for millions
- Cannot implement policy changes at required pace
- GDS live reassessment failure increasingly likely
- Digital talent attrition accelerates (30%+ annual turnover)

**Risks**:

- System failure during demand surge: Unquantifiable human and reputational impact
- Vendor contract renewal without modernisation: GBP 40M premium for legacy support
- NAO value for money challenge on rising operational costs

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unsustainable. Costs escalate, capability degrades, and risk of catastrophic failure increases annually.

---

### Option 1: Tactical Remediation

**Description**: Address the most critical issues through targeted improvements to the existing platform — performance optimisation, limited UI refresh, improved monitoring — without replacing the underlying architecture.

**Scope**:

- Performance tuning and caching layer for existing application
- GOV.UK Design System skin over existing claimant portal
- Enhanced monitoring and alerting
- Manual process automation for top 10 highest-volume tasks

**Costs** (5-year) — ROM (+/-40%):

- Capital: GBP 65M
  - Performance remediation: GBP 20M
  - UI refresh: GBP 15M
  - Automation: GBP 20M
  - Monitoring: GBP 10M
- Operational: GBP 425M over 5 years (GBP 85M/year, no reduction)
- Total 5-year TCO: GBP 490M

**Benefits** (5-year):

- Modest processing time improvement (23 days to 18 days)
- Marginal satisfaction improvement (68% to 72%)
- No operational cost saving (architecture unchanged)
- Total quantified benefit: GBP 35M (reduced errors from automation)

**Net Benefit**: Negative GBP 30M (costs exceed benefits)

**Pros**:

- Lower upfront investment (GBP 65M vs GBP 340M)
- Lower migration risk (no data migration)
- Faster initial delivery (6 months for first improvements)

**Cons**:

- Does not address fundamental architectural issues
- No operational cost reduction (same platform, same support costs)
- Insufficient improvement to pass GDS reassessment
- Defers modernisation costs — total 10-year cost higher than Option 2
- Technical debt continues to compound

**Stakeholder Impact**:

- G-1 (Processing time): Partially met — 18 days vs 10-day target
- G-2 (Satisfaction): Partially met — 72% vs 85% target
- G-3 (Policy agility): Not met — architecture unchanged
- G-4 (Cost reduction): Not met — no savings
- G-5 (Scalability): Partially met — improved but not fundamentally solved

**Stakeholder Goals Met**: 20%

**Risks**:

- Investment wasted when full modernisation becomes unavoidable within 3-5 years
- Creates false confidence that "something is being done" while fundamental issues remain
- Vendor leverages legacy dependency for higher support costs at contract renewal

---

### Option 2: Phased Platform Modernisation (RECOMMENDED)

**Description**: Replace the UC digital platform through a phased modernisation programme, delivering a configurable rules engine, mobile-first claimant experience, modern staff tooling, and standards-based integrations — while maintaining uninterrupted payment operations through parallel running.

**Scope**:

- Phase 1 (Months 1-12): New claimant portal, GOV.UK integration, enhanced communications
- Phase 2 (Months 9-24): New processing engine with configurable rules, staff tooling
- Phase 3 (Months 18-36): Phased data migration by region, parallel running, cutover
- Phase 4 (Months 30-48): Integration modernisation (HMRC near-real-time, LA APIs)
- Phase 5 (Months 36-60): Legacy decommission, optimisation, continuous improvement

**Costs** (5-year) — ROM (+/-30%):

- Capital: GBP 340M
  - Platform development (internal team): GBP 120M
  - Cloud infrastructure: GBP 45M
  - System integration services: GBP 85M
  - Migration and parallel running: GBP 55M
  - Training and change management: GBP 35M
- Operational: GBP 130M transitional (Years 1-2 at GBP 85M legacy + new, declining from Year 3)
- Total 5-year TCO: GBP 470M

**Benefits** (10-year, from Year 3):

| Benefit ID | Benefit Description | Stakeholder Goal | Type | Year 3 | Year 4 | Year 5 | 10-Year Total |
|------------|---------------------|------------------|------|--------|--------|--------|---------------|
| B-001 | Operational cost reduction | G-4 | FINANCIAL | GBP 25M | GBP 25M | GBP 25M | GBP 200M |
| B-002 | Processing efficiency (FTE redeployment) | G-1 | OPERATIONAL | GBP 80M | GBP 100M | GBP 155M | GBP 650M |
| B-003 | Error and overpayment reduction | G-1 | FINANCIAL | GBP 30M | GBP 40M | GBP 45M | GBP 180M |
| B-004 | Channel shift (reduced telephony) | G-2 | OPERATIONAL | GBP 10M | GBP 20M | GBP 28M | GBP 100M |
| **Total Benefits** | | | | **GBP 145M** | **GBP 185M** | **GBP 253M** | **GBP 1,130M** |

**Net Present Value** (3.5% discount rate, 10-year horizon):

- Total Benefits PV: GBP 782M
- Total Costs PV: GBP 470M
- **NPV: GBP 312M** (strongly positive)

**Return on Investment**:

- **ROI: 130%** over 10 years
- **Payback Period: 38 months** from programme start

**Pros**:

- Strongly positive NPV (GBP 312M)
- Acceptable payback period (38 months)
- Phased delivery reduces risk — each phase delivers independent value
- Modern platform attracts and retains digital talent
- Configurable rules engine transforms policy delivery capability
- Scalable architecture withstands demand surges
- Passes GDS service assessments

**Cons**:

- Significant upfront investment (GBP 340M capital)
- 5-year programme duration — requires sustained political and organisational commitment
- Migration risk during parallel running (mitigated by phased approach)
- Dependent on HMRC and LA integration cooperation

**Stakeholder Impact**:

- G-1 (Processing time): Met — 10 working days by March 2028
- G-2 (Satisfaction): Met — 85% by March 2028
- G-3 (Policy agility): Met — 2-week policy deployment
- G-4 (Cost reduction): Met — GBP 60M/year operational cost (GBP 25M saving)
- G-5 (Scalability): Met — 200K concurrent users supported

**Stakeholder Goals Met**: 100%

**Risks**:

- Payment disruption during migration: Mitigated by phased regional migration with parallel running and rollback capability
- Timeline overrun: Mitigated by phased delivery (each phase independently valuable) and agile methodology
- Integration partner readiness: Mitigated by fallback batch adapters and early engagement governance

---

### Option 3: Full Replacement (Big Bang)

**Description**: Complete replacement of the UC platform through a single integrated programme with simultaneous migration of all 6 million claims, including comprehensive integration modernisation and AI-enhanced assessment.

**Scope**:

- All Option 2 scope delivered as single integrated release
- AI-enhanced fraud detection and eligibility assessment
- Real-time event-driven integration with all partners (no batch)
- Multi-region active-active deployment for 99.99% availability

**Costs** (5-year) — ROM (+/-40%):

- Capital: GBP 650M (significantly higher due to integration complexity and AI development)
- Operational: GBP 150M (higher transitional costs due to big-bang migration)
- Total 5-year TCO: GBP 800M

**Benefits** (10-year): GBP 1,250M (marginally higher than Option 2 due to AI-enhanced accuracy)

**Net Benefit**: GBP 450M (lower than Option 2 risk-adjusted due to higher costs and execution risk)

**Pros**:

- Comprehensive solution addressing all requirements simultaneously
- AI-enhanced accuracy potentially delivering higher error reduction
- 99.99% availability exceeds minimum requirement

**Cons**:

- GBP 330M more expensive than Option 2 with marginal incremental benefit
- Big-bang migration of 6 million claims creates unacceptable payment disruption risk
- 3-year delivery before any benefit realisation (no phased value)
- Historical evidence shows government big-bang IT programmes fail at this scale (NHS NPfIT)
- Exceeds Spending Review envelope by GBP 305M — requires additional Treasury approval

**Stakeholder Goals Met**: 100% (if delivered successfully — execution risk is HIGH)

**Recommendation**: **Reject** — Unacceptable execution risk and cost. Big-bang migration of 6 million claims is inconsistent with BR-001 (zero payment disruption). Historical precedent for government IT programmes at this scale is overwhelmingly negative.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Phased Platform Modernisation**

**Rationale**:

1. **Best Value**: Highest risk-adjusted NPV at GBP 312M over 10 years
2. **Stakeholder Satisfaction**: Meets 100% of identified stakeholder goals
3. **Acceptable Risk**: Phased delivery with parallel running mitigates the catastrophic risk of payment disruption
4. **Affordability**: Within GBP 495M Spending Review envelope
5. **Deliverability**: Phased approach delivers incremental value from Month 12, reducing political and organisational risk

**Sensitivity Analysis**:

- If costs increase 20%: NPV still positive (GBP 218M)
- If benefits reduce 20%: NPV still positive (GBP 156M)
- If timeline extends 12 months: Payback extends to 50 months — still within acceptable range
- Combined pessimistic scenario (costs +20%, benefits -20%, timeline +12 months): NPV GBP 62M — still positive

**Optimism Bias Adjustment** (HM Treasury Green Book):

- Standard uplift for IT-enabled business change: +200% on capital (Green Book supplementary guidance)
- Moderated by programme maturity factors (existing platform, proven technology, phased approach): Applied at +40%
- Adjusted Total Cost: GBP 470M + GBP 136M = GBP 606M (with optimism bias)
- NPV with optimism bias: GBP 176M — still strongly positive

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: The market for large-scale government benefits platform modernisation is mature, with multiple suppliers capable of delivering components. No single supplier covers the entire scope — a multi-supplier model is appropriate.

**Supplier Landscape**:

- **Tier 1** (Large integrators): Experienced in government-scale platform delivery, system integration, and migration
- **Tier 2** (Specialist vendors): Cloud platform specialists, rules engine providers, identity and access management
- **Tier 3** (SMEs): Agile delivery, user research, accessibility testing, component development

**UK Government Digital Marketplace Assessment**:

- **G-Cloud 14**: 200+ suppliers offering cloud hosting and managed services
- **DOS6**: 150+ suppliers for digital outcomes and specialist resources
- **SME participation**: Target 33% of contract value to SMEs (per government policy)

### C1.2 Sourcing Route

**Recommended Route**: Multi-lot procurement through Digital Marketplace (G-Cloud for cloud services, DOS for delivery) with competitive further competition within frameworks.

**Rationale**:

- Compliant with Public Contracts Regulations 2015
- Competitive market exists — no sole source justification
- Framework access ensures speed while maintaining value for money
- SME access built into framework structures

### C1.3 Contract Approach

**Proposed Contract Type**:

- **Build**: Time and materials for agile delivery teams (DOS Outcomes) with milestone payments
- **Run**: Managed service agreement for cloud operations (G-Cloud) with SLA-based pricing

**Contract Duration**:

- Initial term: 3 years (delivery and migration)
- Extension options: 1 + 1 years (optimisation and stabilisation)
- Total potential: 5 years

**Key Contract Terms**:

- SLAs: 99.95% availability, < 2 second page load, < 15 minute MTTR
- Service credits: Per-minute basis for downtime beyond SLA
- IP: Crown owns all bespoke IP
- Exit management: Mandatory exit plan and knowledge transfer included
- Open source: All bespoke code published as open source unless security exemption applies

### C1.4 Social Value

**UK Government Requirement**: Minimum 10% weighting on social value (Social Value Act 2012 and PPN 06/20).

**Social Value Themes**:

1. **Economic**: Apprenticeships in digital skills, jobs in regions of economic deprivation
2. **Social**: Diversity and inclusion in delivery teams, accessibility expertise
3. **Environmental**: Carbon-neutral cloud infrastructure, sustainable operations

**Evaluation Approach**:

- Technical: 60%
- Cost: 30%
- Social Value: 10%

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: GBP 470M over 5 years

### D1.1 Capital Expenditure (CapEx)

| Item | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------|--------|--------|--------|--------|--------|-------|
| Platform development (internal) | GBP 30M | GBP 40M | GBP 30M | GBP 15M | GBP 5M | GBP 120M |
| Cloud infrastructure (setup + migration) | GBP 15M | GBP 15M | GBP 10M | GBP 5M | GBP 0 | GBP 45M |
| System integration services | GBP 20M | GBP 30M | GBP 25M | GBP 10M | GBP 0 | GBP 85M |
| Migration and parallel running | GBP 5M | GBP 20M | GBP 20M | GBP 10M | GBP 0 | GBP 55M |
| Training and change management | GBP 5M | GBP 10M | GBP 10M | GBP 5M | GBP 5M | GBP 35M |
| **Total CapEx** | **GBP 75M** | **GBP 115M** | **GBP 95M** | **GBP 45M** | **GBP 10M** | **GBP 340M** |

### D1.2 Operational Expenditure (OpEx)

| Item | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------|--------|--------|--------|--------|--------|-------|
| Legacy platform operations | GBP 85M | GBP 70M | GBP 30M | GBP 5M | GBP 0 | GBP 190M |
| New platform operations | GBP 5M | GBP 15M | GBP 30M | GBP 55M | GBP 60M | GBP 165M |
| Dual-running overlap | GBP 0 | GBP 10M | GBP 15M | GBP 0 | GBP 0 | GBP 25M |
| **Total OpEx** | **GBP 90M** | **GBP 95M** | **GBP 75M** | **GBP 60M** | **GBP 60M** | **GBP 380M** |

*Note: Year 4-5 operational costs (GBP 60M/year) represent the new steady-state, a GBP 25M/year saving from the current GBP 85M/year baseline.*

### D1.3 Total Cost of Ownership (TCO)

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---|--------|--------|--------|--------|--------|-------|
| CapEx | GBP 75M | GBP 115M | GBP 95M | GBP 45M | GBP 10M | GBP 340M |
| OpEx | GBP 90M | GBP 95M | GBP 75M | GBP 60M | GBP 60M | GBP 380M |
| **Total TCO** | **GBP 165M** | **GBP 210M** | **GBP 170M** | **GBP 105M** | **GBP 70M** | **GBP 720M** |

*Baseline comparison: Do Nothing costs GBP 500M over 5 years in operational costs alone (rising trajectory). Option 2 total TCO of GBP 720M includes capital investment that generates GBP 1,130M benefits over 10 years.*

## D2. Funding Source

**Budget Allocation**:

- **Source**: DWP Spending Review settlement 2025-2030, ring-fenced for UC Modernisation
- **Amount Available**: GBP 495M over 5 years (GBP 25M contingency headroom)
- **Timing**: Available from FY 2026-27 onward

**Budget Approval Path**:

1. DWP Investment Committee: Up to GBP 50M
2. DWP Programme Board + CDDO spend control: GBP 50M to GBP 100M
3. HM Treasury: Above GBP 100M (programme-level approval at SOBC, OBC, FBC gates)

**Funding Gaps**: None identified — programme is within Spending Review settlement.

## D3. Affordability

**Organisational Budget Context**:

- Total DWP digital budget: GBP 600M/year
- This programme: 12.5% of annual digital budget at peak year (Year 2)
- Assessment: **Affordable** — within settlement, risk managed through phased delivery

**Cash Flow Impact**:

- Largest annual spend: GBP 210M in Year 2
- **Cashflow Risk**: LOW — funding pre-allocated in Spending Review
- **Mitigation**: Phased delivery allows spend re-profiling if needed

---

# PART E: MANAGEMENT CASE

## E1. Programme Structure

**Governance**:

- **Programme Board**: Monthly, chaired by SRO, attended by CDIO, Operations Director, Finance Director, HMRC representative
- **Steering Committee**: Quarterly, chaired by Permanent Secretary, attended by Treasury, CDDO, NAO observer
- **Delivery teams**: Agile squads with fortnightly sprint reviews

**Key Roles**:

| Role | Responsibility | Named Individual |
|------|---------------|-----------------|
| SRO | Overall programme accountability | DWP Director General |
| Programme Director | Day-to-day programme management | TBC (recruitment underway) |
| Service Owner | End-to-end service and user outcomes | Existing UC Service Owner |
| Chief Architect | Technical architecture and design authority | DWP Chief Architect |
| Integration Lead | HMRC, LA, and GOV.UK platform integration | TBC |
| Change Lead | Training, communications, stakeholder management | TBC |

## E2. Assurance

**Internal Assurance**:

- DWP Portfolio Office: Monthly RAG reporting
- DWP Investment Committee: Quarterly review

**External Assurance**:

- IPA Gateway Reviews: At SOBC, OBC, and pre-procurement gates
- GDS Service Assessments: Alpha, Beta, Live
- CDDO Spend Controls: At each major spend commitment
- NAO: Value for money review at mid-programme point

## E3. Benefits Realisation

**Benefits Realisation Plan**:

| Benefit | Baseline | Measure | Owner | First Realisation | Reporting |
|---------|----------|---------|-------|-------------------|-----------|
| Operational cost reduction | GBP 85M/year | Annual operational budget | DWP Finance Director | Year 3 (Month 36) | Quarterly |
| Processing time improvement | 23 working days | Case management system data | UC Service Owner | Year 2 (Month 18) | Monthly |
| Claimant satisfaction | 68% | GDS transaction survey | UC Service Owner | Year 2 (Month 18) | Monthly |
| Error reduction | GBP 45M/year overpayments | Quality assurance sampling | UC Operations Director | Year 3 (Month 30) | Quarterly |
| Channel shift | 40% calls per claim | Telephony and digital analytics | Service Owner | Year 2 (Month 15) | Monthly |

## E4. Risk Management

**Top Programme Risks**:

| Risk | Probability | Impact | Mitigation | Owner |
|------|------------|--------|------------|-------|
| Payment disruption during migration | LOW | CRITICAL | Phased migration, parallel running, rollback rehearsals | Operations Director |
| HMRC RTI data freshness dependency | MEDIUM | HIGH | Interim enhanced batch processing, design for variable freshness | Integration Lead |
| Digital talent recruitment | HIGH | MEDIUM | Competitive pay frameworks, apprenticeships, managed service partners | HR Director |
| Policy changes during delivery | HIGH | MEDIUM | Configurable rules engine, protected policy sprint capacity | SRO |
| Local authority API adoption rate | HIGH | MEDIUM | Batch adapter fallback maintained, central funding for LA integration | DLUHC liaison |
| GOV.UK One Login readiness | MEDIUM | HIGH | Alternative identity verification pathway | GDS liaison |
| Scope creep from stakeholder requests | MEDIUM | HIGH | Rigorous change control, phased backlog prioritisation | Programme Director |

## E5. Timeline

| Phase | Activities | Start | End |
|-------|-----------|-------|-----|
| SOBC Approval | This document | Q1 2026 | Q2 2026 |
| OBC Development | Detailed requirements, procurement strategy | Q2 2026 | Q4 2026 |
| Alpha | User research, prototype, GDS Alpha assessment | Q3 2026 | Q1 2027 |
| Beta (Private) | Build, test, limited deployment | Q1 2027 | Q3 2027 |
| Beta (Public) | Wider rollout, GDS Beta assessment | Q3 2027 | Q1 2028 |
| Phase 1 Go-Live | Claimant portal and communications | Q3 2027 | |
| Phase 2 Go-Live | Processing engine (phased by region) | Q1 2028 | |
| Live Assessment | GDS Live assessment | Q2 2028 | |
| Migration Complete | All regions migrated, legacy decommissioned | Q4 2028 | |
| Optimisation | Continuous improvement, integration completion | Q1 2029 | Q1 2031 |

---

## Approval

### Business Case Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| DWP Permanent Secretary | Accounting Officer | [ ] Approved | PENDING | |
| SRO | Programme Sponsor | [ ] Approved | PENDING | |
| DWP Finance Director | Budget Holder | [ ] Approved | PENDING | |
| HM Treasury Spending Team | Funding Approval | [ ] Approved | PENDING | |
| CDDO | Digital Assurance | [ ] Approved | PENDING | |

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| DWP Permanent Secretary (Accounting Officer) | _________ | PENDING |
| SRO, UC Modernisation | _________ | PENDING |
| DWP Finance Director | _________ | PENDING |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| UC | Universal Credit |
| RTI | Real Time Information — HMRC employer earnings reporting |
| BACS | Bankers' Automated Clearing Services |
| NPV | Net Present Value |
| TCO | Total Cost of Ownership |
| ROM | Rough Order of Magnitude |
| IPA | Infrastructure and Projects Authority |
| DOS | Digital Outcomes and Specialists (procurement framework) |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — Enterprise Architecture Principles (SDG 1: No Poverty)
- ARC-001-STKE-v1.0 — Stakeholder Drivers & Goals Analysis
- ARC-001-REQ-v1.0 — Requirements Specification
- HM Treasury Green Book — Appraisal and evaluation guidance
- GDS Service Standard — https://www.gov.uk/service-manual/service-standard

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Universal Credit Modernisation
**Model**: Claude Opus 4.6
