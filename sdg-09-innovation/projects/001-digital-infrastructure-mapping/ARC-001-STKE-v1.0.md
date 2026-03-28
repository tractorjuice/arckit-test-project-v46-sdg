# Stakeholder Drivers & Goals Analysis: Digital Infrastructure Mapping

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Digital Infrastructure Mapping (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Digital Infrastructure Mapping Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Digital Infrastructure Programme Board, DSIT Digital, Ofcom, BDUK |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Digital Infrastructure Mapping platform, their underlying drivers (motivations, concerns, pressures), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to programme success metrics.

### Key Findings

The Digital Infrastructure Mapping platform sits at the centre of a tension between commercial operators who regard network coverage data as competitively sensitive and government's obligation to provide accurate, transparent coverage information to citizens and to direct public investment effectively. The strongest alignment exists between DSIT, BDUK, and local authorities — all want accurate coverage data to avoid wasteful duplication of publicly funded broadband rollout. The most significant conflict is between telecoms operators (who resist granular disclosure of coverage gaps) and Ofcom/DSIT (who need granular data to hold operators accountable for coverage obligations and to target Project Gigabit funding).

### Critical Success Factors

- Achieve operator buy-in for data submission by demonstrating commercial benefit (reduced duplicative builds, streamlined planning consent) alongside regulatory obligation
- Deliver coverage data accuracy sufficient to direct Project Gigabit investment without funding premises that already have or are due to receive commercial coverage
- Integrate Ofcom Connected Nations data, operator submissions, and crowdsourced coverage reports into a single coherent national picture
- Meet INSPIRE Regulations for spatial data publication while protecting legitimately commercially sensitive network topology details
- Provide coverage information to citizens in an accessible format that enables informed decisions about broadband and mobile services

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for better coverage data and the economic case for avoiding duplicative infrastructure investment. Significant tensions between commercial confidentiality (operators), regulatory transparency (Ofcom), investment targeting accuracy (BDUK), and citizen right-to-know (consumer groups). The devolved administrations add complexity through separate broadband programmes (R100 in Scotland, Superfast Cymru successor in Wales).

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Science, Innovation and Technology | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DSIT Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Digital Infrastructure Mapping | Programme Sponsor (DSIT) | HIGH | HIGH | Manage Closely — Weekly programme board |
| DSIT Chief Digital Officer | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance, digital strategy |
| BDUK (Building Digital UK) Director | Broadband investment delivery | HIGH | HIGH | Manage Closely — Investment targeting, subsidy control |
| DSIT Telecoms Policy Team | Policy development | MEDIUM | HIGH | Keep Informed — Policy alignment, legislative requirements |
| DSIT SIRO | Information risk ownership | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| DSIT Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| Product Manager | Feature prioritisation | MEDIUM | HIGH | Keep Informed — Sprint reviews, roadmap input |
| GDS Assessment Team | Service standard assurance | MEDIUM | HIGH | Keep Informed — Pre-assessment workshops |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Ofcom | Regulator | Data provider and regulatory authority | HIGH | HIGH |
| BT / Openreach | Telecoms operator | Major data provider (largest UK network) | HIGH | HIGH |
| Virgin Media O2 (VMO2) | Telecoms operator | Data provider (cable and mobile) | HIGH | HIGH |
| Three UK | Mobile operator | Data provider (mobile coverage) | MEDIUM | HIGH |
| Vodafone UK | Mobile operator | Data provider (mobile and fixed) | MEDIUM | HIGH |
| CityFibre | Alt-net operator | Data provider (full fibre) | MEDIUM | HIGH |
| Local Authorities (380+) | Local government | Coverage data consumers, planning authorities | MEDIUM | HIGH |
| CDDO | Cabinet Office | Assurance and spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval (Project Gigabit) | HIGH | MEDIUM |
| Devolved Administrations | Scottish Government, Welsh Government | Separate broadband programmes | MEDIUM | HIGH |
| Ordnance Survey | Geospatial data provider | Authoritative geometry and addressing | MEDIUM | HIGH |
| Citizens / Consumers | Public | End users of coverage information | LOW | HIGH |
| Internet Service Providers Association (ISPA) | Industry body | Industry coordination | LOW | MEDIUM |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Geospatial Commission | Cabinet Office | Geospatial strategy and standards | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for Digital Infrastructure Mapping outcomes | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns end-to-end coverage mapping service | HIGH / HIGH | Manage Closely — Regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk log |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |
| CDIO | DSIT digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation |
| Departmental Security Officer (DSO) | Day-to-day security coordination | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Owns information and cyber security risk | HIGH / MEDIUM | Keep Satisfied — DPIA sign-off, risk acceptance |
| Cyber Security Lead | Operational cyber security, CAF assessment | MEDIUM / HIGH | Keep Informed — Security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • Secretary of     │
        │  • NAO              │    State (DSIT)     │
        │  • DSIT SIRO        │  • Permanent Sec.   │
        │  • DSIT Finance Dir │  • SRO              │
        │  • CDDO             │  • DSIT CDO         │
 P      │  • SSRO / DSO       │  • BDUK Director    │
 O      │                     │  • Ofcom            │
 W      │                     │  • BT/Openreach     │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • ISPA             │  • Citizens         │
        │                     │  • Local Authorities│
        │                     │  • VMO2, Three,     │
        │                     │    Vodafone, CityF. │
        │                     │  • Devolved Admins  │
        │                     │  • Ordnance Survey  │
        │                     │  • Product Manager  │
        │                     │  • GDS Assessment   │
        │                     │  • Geospatial Comm. │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Secretary of State (DSIT) | HIGH | HIGH | Manage Closely | Ministerial briefings, PQ lines |
| DSIT Permanent Secretary | HIGH | HIGH | Manage Closely | Programme board, accounting officer assurance |
| SRO | HIGH | HIGH | Manage Closely | Weekly programme board |
| DSIT CDO | HIGH | HIGH | Manage Closely | Architecture governance |
| BDUK Director | HIGH | HIGH | Manage Closely | Investment targeting integration |
| Ofcom | HIGH | HIGH | Manage Closely | Data sharing governance, Connected Nations integration |
| BT/Openreach | HIGH | HIGH | Manage Closely | Operator data submission, commercial sensitivity |
| HM Treasury | HIGH | MEDIUM | Keep Satisfied | Business case updates, Project Gigabit alignment |
| NAO | HIGH | MEDIUM | Keep Satisfied | Audit readiness, value for money |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control submissions |
| Citizens | LOW | HIGH | Keep Informed | GOV.UK coverage checker, accessibility |
| Local Authorities | MEDIUM | HIGH | Keep Informed | Coverage data API access, planning integration |
| Other Operators (VMO2, Three, Vodafone, CityFibre) | MEDIUM | HIGH | Keep Informed | Data submission requirements, API specification |
| Devolved Administrations | MEDIUM | HIGH | Keep Informed | Broadband programme coordination |
| Ordnance Survey | MEDIUM | HIGH | Keep Informed | Geospatial data integration |
| ISPA | LOW | MEDIUM | Monitor | Industry engagement |

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Deliver Universal Gigabit Connectivity

**Stakeholder**: Secretary of State for Science, Innovation and Technology

**Driver Category**: POLITICAL / STRATEGIC

**Driver Statement**: Demonstrate measurable progress toward the government's commitment to nationwide gigabit-capable broadband by 2030, using accurate coverage data to direct public investment where it is most needed and to hold operators accountable for build commitments.

**Context & Background**:
The government's Project Gigabit programme has allocated GBP 5 billion to extend gigabit-capable broadband to hard-to-reach areas. Accurate coverage data is essential to avoid publicly subsidising areas where commercial build is planned or complete. Parliamentary scrutiny is intense — Select Committee hearings regularly challenge the accuracy of claimed coverage figures. Inaccurate data risks both over-spending (subsidising commercial areas) and under-spending (missing genuinely unserved premises).

**Driver Intensity**: CRITICAL

**Enablers**:

- Accurate, premises-level coverage data from all operators
- Integration with BDUK voucher and contract management systems
- Real-time updates as operators complete new builds

**Blockers**:

- Operator reluctance to share granular, premises-level data
- Discrepancy between operator-claimed coverage and actual user experience
- Lack of standardised data submission format across operators

**Related Stakeholders**: BDUK Director, Ofcom, HM Treasury, Local Authorities

---

### SD-2: Ofcom — Regulatory Transparency and Accountability

**Stakeholder**: Ofcom

**Driver Category**: COMPLIANCE / STRATEGIC

**Driver Statement**: Obtain accurate, granular, and timely coverage data from all operators to fulfil statutory duties under the Communications Act 2003, including publishing the annual Connected Nations report, monitoring Universal Service Obligation compliance, and enforcing coverage obligations attached to spectrum licences.

**Context & Background**:
Ofcom currently publishes Connected Nations annually, based on operator-submitted data with limited independent verification. There is a recognised gap between operators' theoretical coverage predictions and actual consumer experience. Ofcom needs a platform that enables continuous data collection, independent validation (e.g., via crowdsourced measurements), and more granular analysis than current annual reporting allows. The 2024 spectrum auction coverage obligations for 5G require ongoing monitoring.

**Driver Intensity**: CRITICAL

**Enablers**:

- Regulatory power to compel data submission under the Communications Act
- Established data collection processes (Connected Nations methodology)
- Growing availability of crowdsourced coverage measurement data

**Blockers**:

- Operator data quality varies significantly across providers
- Resource constraints for independent coverage verification
- Complexity of indoor vs outdoor coverage measurement methodologies

**Related Stakeholders**: Secretary of State, BT/Openreach, mobile operators

---

### SD-3: BT/Openreach — Protect Commercial Interests While Meeting Regulatory Obligations

**Stakeholder**: BT Group / Openreach

**Driver Category**: COMMERCIAL / COMPLIANCE

**Driver Statement**: Comply with regulatory data submission requirements while protecting commercially sensitive information about network topology, planned build areas, and competitive strategy from disclosure to rival operators or premature public release.

**Context & Background**:
Openreach is the UK's largest fixed broadband network operator, serving approximately 80% of premises. Openreach's forward build plans are commercially sensitive — premature disclosure could enable rivals to cherry-pick profitable areas. However, Openreach also benefits from accurate coverage data that prevents BDUK from subsidising areas where Openreach is already planning commercial build. This creates a nuanced position: Openreach wants enough transparency to protect its commercial territory but not so much that rivals can use the data competitively.

**Driver Intensity**: HIGH

**Enablers**:

- Clear data handling rules that separate regulatory use from public disclosure
- Tiered access model with different granularity for different users
- Commitment from DSIT that subsidised builds will not duplicate commercial plans

**Blockers**:

- Risk of FOIA requests exposing commercially sensitive build plans
- Concern that granular data enables competitor analysis
- Administrative burden of frequent data submissions

**Related Stakeholders**: Ofcom, BDUK, VMO2, CityFibre

---

### SD-4: BDUK — Accurate Investment Targeting

**Stakeholder**: BDUK (Building Digital UK)

**Driver Category**: FINANCIAL / OPERATIONAL

**Driver Statement**: Obtain premises-level coverage data with sufficient accuracy and timeliness to ensure Project Gigabit funding reaches only genuinely unserved and underserved premises, avoiding both over-build (wasting public money) and under-build (leaving premises behind).

**Context & Background**:
BDUK manages the GBP 5 billion Project Gigabit programme. Each procurement area is defined based on coverage data — premises are classified as "in scope" (eligible for subsidy) or "out of scope" (commercially served). Inaccurate data at this stage leads to costly errors: including commercially served premises wastes subsidy, excluding unserved premises contradicts the programme's purpose. BDUK needs data that is accurate, current, and at premises level (not postcode or exchange level).

**Driver Intensity**: CRITICAL

**Enablers**:

- Premises-level (UPRN-based) coverage data from all operators
- Regular updates reflecting commercial build progress
- Integration with BDUK's procurement and contract management systems

**Blockers**:

- Operator build plans change frequently, making point-in-time data quickly outdated
- Definition of "coverage" varies (e.g., gigabit-capable connection available vs. service actually activated)
- Multiple overlapping operator plans create reconciliation challenges

**Related Stakeholders**: Secretary of State, HM Treasury, Ofcom, Local Authorities

---

### SD-5: Local Authorities — Inform Local Digital Inclusion Strategies

**Stakeholder**: Local Authorities (380+ councils across England)

**Driver Category**: OPERATIONAL / STRATEGIC

**Driver Statement**: Access accurate, ward-level and premises-level broadband and mobile coverage data to inform local digital inclusion strategies, support planning applications for telecoms infrastructure, and engage with constituents about connectivity improvements in their areas.

**Context & Background**:
Local authorities play a key role in both demand-side (digital inclusion, skills) and supply-side (planning consent for masts and cabinets, wayleave agreements) broadband delivery. Currently, local authorities rely on fragmented, often outdated coverage data from multiple sources. They need a single, authoritative, regularly updated view of coverage in their area — broken down by technology (FTTC, FTTP, 4G, 5G), speed tier, and premises type (residential, business, public buildings).

**Driver Intensity**: HIGH

**Enablers**:

- Self-service API access to coverage data for their geographic area
- GIS-compatible data formats for integration with local planning systems
- Clear, jargon-free presentation for use in public communications

**Blockers**:

- Lack of GIS expertise in many smaller authorities
- Limited bandwidth to process and interpret complex coverage datasets
- Concern about accuracy of data provided to constituents

**Related Stakeholders**: BDUK, Ofcom, Citizens, Devolved Administrations

---

### SD-6: Citizens — Know What Broadband and Mobile Coverage Is Available

**Stakeholder**: Citizens / Consumers

**Driver Category**: CUSTOMER / PERSONAL

**Driver Statement**: Understand what broadband and mobile coverage is actually available at a specific address or location, based on verified data rather than operator marketing claims, to make informed purchasing decisions and to hold operators and government accountable for coverage commitments.

**Context & Background**:
Citizens frequently experience a gap between operator-advertised coverage and actual service. "Up to" speed claims are misleading. The ASA has repeatedly ruled against overclaiming by broadband providers. Citizens need an authoritative, government-backed source of truth for coverage at their address that reflects actual availability, not theoretical maximum speeds.

**Driver Intensity**: HIGH

**Enablers**:

- Simple, address-based coverage lookup on GOV.UK
- Clear language distinguishing "available" from "may be available" from "planned"
- Ability to report coverage discrepancies (crowdsourced verification)

**Blockers**:

- Technical complexity of presenting nuanced coverage data simply
- Liability concerns if government-published data proves inaccurate
- Operator resistance to government publishing alternative coverage figures

**Related Stakeholders**: Ofcom, Local Authorities, ISPA

---

## Driver-to-Goal Mapping

### Goal G-1: National Premises-Level Coverage Database

**Derived From Drivers**: SD-1, SD-2, SD-4

**Goal Owner**: SRO, Digital Infrastructure Mapping

**Goal Statement**: Establish a single, authoritative, UPRN-level database of broadband and mobile coverage across all UK premises by Q4 2027, with data updated at least monthly from all major operators.

**Why This Matters**: Without premises-level data, investment targeting relies on postcode-level approximations that include and exclude wrong premises, wasting public money and leaving genuinely unserved premises behind.

**Success Metrics**:

- **Primary Metric**: Percentage of UK premises with coverage data from all relevant operators
- **Secondary Metrics**:
  - Data freshness: average age of coverage records < 30 days
  - Operator participation: all operators with >1% market share submitting data

**Baseline**: Ofcom Connected Nations data — annual, exchange-area level, operator-submitted

**Target**: Monthly, UPRN-level, multi-operator, with independent verification layer

**Measurement Method**: Coverage database statistics dashboard, operator submission monitoring

**Dependencies**:

- Operator agreement on data submission format and frequency
- Ofcom regulatory support for compelling submission
- Ordnance Survey AddressBase Premium licence for UPRN matching

**Risks to Achievement**:

- Operator non-compliance or data quality issues delay population
- UPRN matching accuracy insufficient for rural premises with non-standard addressing

---

### Goal G-2: Project Gigabit Integration

**Derived From Drivers**: SD-1, SD-4

**Goal Owner**: BDUK Director

**Goal Statement**: Integrate the coverage database with BDUK procurement systems to automate the identification of eligible (unserved/underserved) premises for each Project Gigabit procurement area, reducing manual data reconciliation from 12 weeks to 2 weeks per procurement.

**Why This Matters**: Faster, more accurate procurement area definition accelerates GBP 5 billion of broadband investment and reduces the risk of subsidy errors.

**Success Metrics**:

- **Primary Metric**: Time to define procurement area premises list (from 12 weeks to 2 weeks)
- **Secondary Metrics**:
  - Subsidy error rate (premises wrongly included/excluded) < 2%
  - Number of procurement challenges due to data accuracy reduced by 80%

**Baseline**: 12 weeks manual process, estimated 5-8% error rate

**Target**: 2 weeks automated process, < 2% error rate

**Measurement Method**: BDUK procurement timeline tracking, post-contract audit

---

### Goal G-3: Citizen Coverage Checker

**Derived From Drivers**: SD-5, SD-6

**Goal Owner**: Service Owner, Digital Infrastructure Mapping

**Goal Statement**: Deliver a public-facing, GOV.UK-hosted coverage checker that enables any citizen to look up broadband and mobile coverage at their address, achieving 1 million lookups per month within 6 months of launch.

**Why This Matters**: Citizens cannot make informed decisions about broadband services or hold operators accountable without accessible, trustworthy coverage information.

**Success Metrics**:

- **Primary Metric**: Monthly unique coverage lookups
- **Secondary Metrics**:
  - User satisfaction score > 4.0/5.0
  - Accessibility compliance: WCAG 2.2 Level AA
  - Coverage discrepancy reports submitted per month (crowdsourced verification)

**Baseline**: No single authoritative citizen-facing coverage tool exists

**Target**: 1 million lookups/month within 6 months, 4.0/5.0 satisfaction

**Measurement Method**: GOV.UK analytics, user satisfaction survey, feedback submissions

---

### Goal G-4: Regulatory Reporting Automation

**Derived From Drivers**: SD-2

**Goal Owner**: Ofcom Director of Digital Infrastructure

**Goal Statement**: Enable Ofcom to produce Connected Nations reporting from the platform's data, reducing the annual data collection and analysis cycle from 6 months to 2 months and enabling quarterly interim reports.

**Why This Matters**: More frequent, faster reporting enables Ofcom to identify and address coverage gaps sooner and to monitor spectrum licence obligations in near-real-time.

**Success Metrics**:

- **Primary Metric**: Connected Nations report production time (6 months to 2 months)
- **Secondary Metrics**:
  - Quarterly interim reports published (0 to 4 per year)
  - Data validation automation rate (manual checks reduced by 70%)

**Baseline**: Annual 6-month production cycle

**Target**: 2-month production, quarterly interim reports

**Measurement Method**: Ofcom reporting timeline, publication dates

---

## Goal-to-Outcome Mapping

### Outcome O-1: Efficient Public Investment in Digital Infrastructure

**Supported Goals**: G-1, G-2

**Outcome Statement**: Reduce wasted Project Gigabit subsidy by eliminating over-build of commercially served premises, saving an estimated GBP 200-400 million over the programme lifetime.

**Measurement Details**:

- **KPI**: Subsidy accuracy rate (percentage of funded premises genuinely unserved)
- **Current Value**: Estimated 92-95% accuracy
- **Target Value**: >98% accuracy
- **Measurement Frequency**: Quarterly
- **Data Source**: Post-contract audit, coverage database reconciliation
- **Report Owner**: BDUK Programme Director

**Business Value**:

- **Financial Impact**: GBP 200-400M subsidy savings over programme lifetime
- **Strategic Impact**: Accelerated nationwide gigabit coverage
- **Operational Impact**: Faster procurement cycles, fewer challenges
- **Customer Impact**: More premises receive funded coverage

**Timeline**:

- **Phase 1 (Months 1-6)**: Database populated with major operator data, initial BDUK integration
- **Phase 2 (Months 7-12)**: Full operator coverage, automated procurement area definition
- **Phase 3 (Months 13-18)**: Continuous monitoring, post-build verification
- **Sustainment (Year 2+)**: Ongoing operation, data quality improvement

---

### Outcome O-2: Informed Citizens and Transparent Coverage

**Supported Goals**: G-3, G-4

**Outcome Statement**: Enable every UK citizen to check broadband and mobile coverage at their address through an authoritative government service, reducing reliance on operator marketing claims and supporting informed consumer choice.

**Measurement Details**:

- **KPI**: Monthly active users of coverage checker
- **Current Value**: No single authoritative service exists
- **Target Value**: 1 million lookups/month within 6 months of launch
- **Measurement Frequency**: Monthly
- **Data Source**: GOV.UK analytics
- **Report Owner**: Service Owner

**Business Value**:

- **Financial Impact**: Reduced ASA complaints about misleading coverage claims
- **Strategic Impact**: Government trusted as impartial source of coverage information
- **Operational Impact**: Reduced MP casework on connectivity issues
- **Customer Impact**: Better-informed purchasing decisions

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Universal gigabit connectivity | G-1 | National coverage database | O-1 | Efficient public investment |
| Secretary of State | SD-1 | Universal gigabit connectivity | G-2 | Project Gigabit integration | O-1 | Efficient public investment |
| Ofcom | SD-2 | Regulatory transparency | G-1 | National coverage database | O-2 | Informed citizens |
| Ofcom | SD-2 | Regulatory transparency | G-4 | Regulatory reporting automation | O-2 | Informed citizens |
| BT/Openreach | SD-3 | Protect commercial interests | G-1 | National coverage database | O-1 | Efficient public investment |
| BDUK | SD-4 | Accurate investment targeting | G-2 | Project Gigabit integration | O-1 | Efficient public investment |
| Local Authorities | SD-5 | Local digital inclusion | G-3 | Citizen coverage checker | O-2 | Informed citizens |
| Citizens | SD-6 | Know what coverage exists | G-3 | Citizen coverage checker | O-2 | Informed citizens |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: BT/Openreach (SD-3) wants to protect commercially sensitive build plans, but BDUK (SD-4) and Ofcom (SD-2) need granular, premises-level data including forward build plans to avoid subsidy errors and enforce obligations.
  - **Resolution Strategy**: Tiered access model — regulatory/investment tier (full granularity, restricted access for BDUK and Ofcom under NDA), public tier (aggregated to postcode/ward level, no operator-attributable forward plans). FOIA exemptions under section 43 (commercial interests) applied to granular data.

- **Conflict 2**: Citizens (SD-6) want simple, definitive "yes/no" coverage answers, but the reality is nuanced (technology, speed, indoor/outdoor, shared vs dedicated). Over-simplification risks inaccuracy; full detail risks confusion.
  - **Resolution Strategy**: Progressive disclosure — simple summary view ("Good broadband available" / "Limited broadband") with ability to drill into detailed technology and speed data for informed users.

**Synergies**:

- **Synergy 1**: DSIT's drive for accurate investment targeting (SD-1) and BDUK's need for premises-level data (SD-4) are perfectly aligned — the same database serves both
- **Synergy 2**: Ofcom's regulatory reporting (SD-2) and citizen transparency (SD-6) both benefit from the same underlying data quality improvements

---

## Communication & Engagement Plan

### Telecoms Operators (BT/Openreach, VMO2, Three, Vodafone, CityFibre)

**Primary Message**: The platform protects commercially sensitive data through tiered access while reducing your regulatory reporting burden and preventing publicly funded over-build in your commercial areas.

**Key Talking Points**:

- Tiered access model protects forward build plans from public disclosure and competitor access
- Standardised data submission format reduces the multiple different requests you receive from DSIT, Ofcom, BDUK, and local authorities
- Accurate coverage data prevents Project Gigabit funding in areas where you are already planning commercial build

**Communication Frequency**: Monthly operator forum

**Preferred Channel**: Bilateral meetings + industry working group

**Success Story**: "BDUK withdrew 3 procurement areas from competitive tender because our data showed your commercial build plans would cover those premises within 18 months — saving you from subsidised competition."

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Telecoms Operators | Submit data annually to Ofcom in bespoke formats | Submit monthly in standardised format to single platform | HIGH | HIGH | Demonstrate commercial benefit, regulatory backstop |
| BDUK | Manual data reconciliation across multiple sources | Automated premises-level coverage analysis | HIGH | LOW | Close involvement in requirements, early integration testing |
| Ofcom | Annual manual data collection and analysis | Continuous data feed, automated analysis | MEDIUM | LOW | Position as enhancement to Connected Nations, not replacement |
| Local Authorities | Fragmented coverage information from multiple sources | Self-service API and portal access | MEDIUM | LOW | Training, documentation, API sandbox |
| Citizens | No single authoritative coverage checker | GOV.UK coverage lookup | LOW | LOW | User research, accessibility testing |

### Change Readiness

**Champions** (Enthusiastic supporters):

- BDUK — direct operational benefit, reduces manual effort and improves accuracy
- Local Authorities — long-demanded single source of coverage data

**Fence-sitters** (Neutral, need convincing):

- Ofcom — supportive in principle but concerned about resource implications for data validation
- CityFibre — smaller operator worried about disproportionate compliance burden

**Resisters** (Opposed or skeptical):

- BT/Openreach — concerned about granular data exposure to competitors and FOIA
- VMO2 — sceptical about government's ability to protect commercial data

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Operator Non-Compliance with Data Submission

**Related Stakeholders**: BT/Openreach, VMO2, Three, Vodafone, CityFibre

**Risk Description**: One or more major operators refuse or delay data submission, citing commercial sensitivity, administrative burden, or legal concerns, rendering the national picture incomplete.

**Impact on Goals**: G-1 (national database), G-2 (Project Gigabit integration), G-3 (citizen checker)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Ofcom regulatory direction under Communications Act 2003; demonstrate commercial benefit of preventing subsidised over-build; standardise submission format to reduce burden

**Contingency Plan**: Use Ofcom Connected Nations data as fallback for non-compliant operators; name and shame in Parliamentary reports

---

### Risk R-2: Data Accuracy Insufficient for Investment Decisions

**Related Stakeholders**: BDUK, HM Treasury, NAO

**Risk Description**: Coverage data accuracy is insufficient to correctly classify premises as served/unserved, leading to subsidy errors that trigger NAO criticism and Treasury scrutiny.

**Impact on Goals**: G-1, G-2

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Independent verification layer using crowdsourced data, Ofcom drive testing, and post-build audit; clear accuracy tolerance thresholds communicated to BDUK

**Contingency Plan**: Manual verification for high-value procurement areas; phased rollout starting with areas where data confidence is highest

---

### Risk R-3: FOIA Disclosure of Commercially Sensitive Data

**Related Stakeholders**: BT/Openreach, VMO2, CityFibre

**Risk Description**: A Freedom of Information request successfully obtains granular operator-specific coverage data, destroying operator trust and future willingness to submit data.

**Impact on Goals**: G-1 (operator participation)

**Probability**: LOW

**Impact**: HIGH

**Mitigation Strategy**: Legal review confirming section 43 (commercial interests) exemption applies; data aggregation policies that prevent operator-attributable analysis at granular level; clear data handling agreement with operators

**Contingency Plan**: Renegotiate data sharing terms; consider legislative protection if FOIA exemption proves inadequate

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Data submission format and frequency | Product Manager | SRO | Ofcom, Operators, BDUK | Local Authorities |
| Tiered access model (what data is public vs restricted) | DSIT Policy Team | Secretary of State | Ofcom, Operators, ICO | Citizens, Local Authorities |
| Coverage accuracy thresholds | Product Manager | SRO | Ofcom, BDUK, OS | HM Treasury, NAO |
| Architecture decisions | Technical Lead | DSIT CDO | Geospatial Commission, GDS | CDDO |
| Go/No-go for public launch | SRO | Permanent Secretary | All stakeholders | All |
| Budget approval | DSIT Finance | Permanent Secretary | HM Treasury | CDDO, NAO |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, operator disputes)
3. **Level 3**: SRO / Permanent Secretary (strategic direction, Ministerial escalation)
4. **Level 4**: Secretary of State (cross-government disputes, regulatory intervention)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| BDUK Director | PENDING | | PENDING |
| Ofcom | PENDING | | PENDING |
| Operator Representatives | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| DSIT CDO | | | |
| BDUK Director | | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

#### Interview with BDUK Director — 2026-03-15

**Key Points**:

- Current 12-week manual process for defining procurement areas is the single biggest bottleneck
- Data quality issues have caused 3 procurement challenges in FY25/26, each costing 4-6 months delay
- Needs UPRN-level data, not postcode-level — postcode boundaries do not align with network boundaries

**Quotes**:

- "Every premises we wrongly include in a procurement area is public money we've wasted. Every premises we wrongly exclude is a citizen we've left behind."

**Follow-up Actions**:

- Detailed requirements session for BDUK integration API
- Access to BDUK procurement area definition methodology

---

### Appendix B: References

- UK Digital Strategy 2022
- Project Gigabit Programme Business Case
- Ofcom Connected Nations Report 2025
- UK Geospatial Strategy 2030
- INSPIRE Regulations (UK implementation)
- Communications Act 2003 (data gathering powers)

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| UK Digital Strategy 2022 | Strategy | DSIT | Gigabit connectivity targets | N/A — external reference |
| Project Gigabit | Programme | BDUK | GBP 5B broadband investment programme | N/A — external reference |
| Connected Nations 2025 | Report | Ofcom | UK coverage statistics and methodology | N/A — external reference |
| INSPIRE Regulations | Regulation | legislation.gov.uk | Spatial data sharing obligations | N/A — external reference |
| Communications Act 2003 | Legislation | legislation.gov.uk | Ofcom data gathering powers | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Digital Infrastructure Mapping (Project 001)
**Model**: Claude Opus 4.6
