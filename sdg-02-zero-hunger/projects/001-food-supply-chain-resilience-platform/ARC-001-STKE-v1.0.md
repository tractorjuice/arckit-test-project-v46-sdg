# Stakeholder Drivers & Goals Analysis: Food Supply Chain Resilience Platform

> **Template Origin**: Official | **ArcKit Version**: 4.1.1 | **Command**: `/arckit:stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Food Supply Chain Resilience Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-09 |
| **Last Modified** | 2026-03-09 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-09 |
| **Owner** | Senior Responsible Owner, DEFRA Food Resilience Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | DEFRA Digital, Food Standards Agency, Cabinet Office Food Strategy Unit |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-09 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the Food Supply Chain Resilience Platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The platform monitors UK food supply chain risks across import corridors, domestic production, and distribution networks, providing early warning of disruptions.

### Key Findings

The strongest driver alignment exists between the DEFRA Secretary of State's need for crisis-readiness and the Food Standards Agency's mandate to protect consumers -- both converge on real-time supply chain visibility. The primary tension is between Treasury's demand for cost containment and the operational need for comprehensive data acquisition from commercial supply chain actors who may resist mandatory reporting. Cross-departmental data sharing with projects 003, 004, and 005 creates both synergies and governance complexity.

### Critical Success Factors

- Securing voluntary or regulatory data-sharing agreements with major retailers and importers
- Achieving real-time integration with border control and port logistics systems
- Demonstrating value during a real supply disruption within the first 12 months
- Passing GDS service assessment at Beta stage

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Government stakeholders share a strong common vision for food resilience, but alignment with commercial supply chain actors is conditional on perceived mutual benefit and data confidentiality assurances. Treasury cost constraints create friction with the operational scope needed for comprehensive monitoring.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| S-1: DEFRA Secretary of State | Minister | HIGH | HIGH | Ministerial briefings, crisis readiness demos |
| S-2: DEFRA Permanent Secretary | Accounting Officer | HIGH | HIGH | Programme board, spend control oversight |
| S-3: SRO, Food Resilience Programme | Senior Responsible Owner | HIGH | HIGH | Weekly programme board, decision authority |
| S-4: DEFRA Chief Digital Officer | Digital Strategy Lead | HIGH | HIGH | Architecture reviews, technology decisions |
| S-5: Food Supply Chain Analysis Team | Policy Analysts | MEDIUM | HIGH | Sprint reviews, requirements input |
| S-6: DEFRA Finance Director | Budget Holder | HIGH | MEDIUM | Quarterly business case reviews |
| S-7: DEFRA SIRO | Information Risk Owner | HIGH | MEDIUM | Data governance, risk sign-off |
| S-8: DEFRA Cyber Security Lead | GovAssure Liaison | MEDIUM | HIGH | Security architecture reviews |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| S-9: Food Standards Agency (FSA) | Regulator | Data partner and co-user | HIGH | HIGH |
| S-10: Major Retailers (top 10) | Tesco, Sainsbury's, Asda, etc. | Data providers | HIGH | MEDIUM |
| S-11: HMRC Border Force | Border control | Data provider (import volumes) | MEDIUM | LOW |
| S-12: Port Operators | Felixstowe, Dover, etc. | Data provider (logistics) | MEDIUM | MEDIUM |
| S-13: NFU (National Farmers' Union) | Industry body | Consulted on domestic production | LOW | HIGH |
| S-14: Cabinet Office (Project 005) | Cross-govt dashboard | Data consumer | MEDIUM | HIGH |
| S-15: CDDO | Spend control / assurance | HIGH | MEDIUM |
| S-16: Treasury (HMT) | Budget approver | HIGH | LOW |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for programme outcomes and spend | HIGH / HIGH | Manage Closely -- steering board, decision escalation |
| Service Owner | Owns end-to-end service and user outcomes | HIGH / HIGH | Manage Closely -- regular service reviews |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed -- sprint reviews, roadmap input |
| Delivery Manager | Manages delivery cadence, risks, dependencies | MEDIUM / HIGH | Keep Informed -- stand-ups, risk log |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied -- spend control submissions |
| DEFRA CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied -- quarterly strategy alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Owns protective security risk at board level | HIGH / MEDIUM | Keep Satisfied -- security risk escalation |
| Departmental Security Officer (DSO) | Security coordination and policy implementation | HIGH / MEDIUM | Keep Satisfied -- security compliance gates |
| Senior Information Risk Owner (SIRO) | Information and cyber security risk, DPIA sign-off | HIGH / MEDIUM | Keep Satisfied -- information risk decisions |
| Cyber Security Lead | Operational cyber security, GovAssure liaison | MEDIUM / HIGH | Keep Informed -- security architecture reviews |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • S-6 Finance Dir  │  • S-1 Secretary    │
        │  • S-7 SIRO         │    of State         │
        │  • S-15 CDDO        │  • S-2 Perm Sec     │
        │  • S-16 Treasury    │  • S-3 SRO          │
 P      │                     │  • S-4 CDO          │
 O      │                     │  • S-9 FSA          │
 W      ├─────────────────────┼─────────────────────┤
 E      │                     │                     │
 R      │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • S-11 Border      │  • S-5 Policy Team  │
        │    Force            │  • S-8 Cyber Lead   │
        │                     │  • S-12 Port Ops    │
        │                     │  • S-13 NFU         │
        │                     │  • S-14 Cabinet Off │
        │                     │  • S-10 Retailers   │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| S-1 Secretary of State | HIGH | HIGH | Manage Closely | Monthly ministerial briefing, crisis alerts |
| S-2 Permanent Secretary | HIGH | HIGH | Manage Closely | Programme board, accounting officer assurance |
| S-3 SRO | HIGH | HIGH | Manage Closely | Weekly programme board |
| S-4 CDO | HIGH | HIGH | Manage Closely | Architecture review board |
| S-5 Policy Team | LOW | HIGH | Keep Informed | Sprint reviews, user research |
| S-6 Finance Director | HIGH | LOW | Keep Satisfied | Quarterly budget reviews |
| S-7 SIRO | HIGH | MEDIUM | Keep Satisfied | DPIA sign-off, data governance board |
| S-8 Cyber Security Lead | MEDIUM | HIGH | Keep Informed | Security architecture reviews |
| S-9 FSA | HIGH | HIGH | Manage Closely | Joint steering group, data partnership board |
| S-10 Retailers | HIGH | MEDIUM | Keep Satisfied | Industry advisory panel |
| S-11 Border Force | MEDIUM | LOW | Monitor | Data feed SLA reviews |
| S-12 Port Operators | MEDIUM | MEDIUM | Keep Informed | Quarterly integration reviews |
| S-13 NFU | LOW | HIGH | Keep Informed | Stakeholder newsletter, consultation |
| S-14 Cabinet Office | MEDIUM | HIGH | Keep Informed | Cross-programme data board |
| S-15 CDDO | HIGH | MEDIUM | Keep Satisfied | Spend control, assessment gates |
| S-16 Treasury | HIGH | LOW | Keep Satisfied | Annual spending review submissions |

---

## Stakeholder Drivers Analysis

### SD-1: DEFRA Secretary of State -- Crisis Preparedness

**Stakeholder**: S-1 DEFRA Secretary of State

**Driver Category**: STRATEGIC / RISK

**Driver Statement**: Ensure the UK Government can detect and respond to food supply disruptions before they reach consumer-visible levels, avoiding political fallout from empty supermarket shelves.

**Context & Background**: COVID-19 and post-Brexit border friction exposed gaps in government visibility of food supply chains. The 2021 HGV driver shortage and 2022 egg supply crisis generated sustained negative media coverage. Ministers need early warning to coordinate cross-government response before parliamentary questions arise.

**Driver Intensity**: CRITICAL

**Enablers**:
- Real-time data feeds from supply chain actors
- Cross-government information sharing protocols
- Pre-agreed crisis response playbooks

**Blockers**:
- Commercial reluctance to share proprietary supply data
- Fragmented data standards across the food industry
- Competing ministerial priorities for DEFRA digital spend

**Related Stakeholders**: S-2 (Permanent Secretary), S-9 (FSA), S-14 (Cabinet Office)

---

### SD-2: Permanent Secretary -- Governance and Accountability

**Stakeholder**: S-2 DEFRA Permanent Secretary

**Driver Category**: RISK / COMPLIANCE

**Driver Statement**: Ensure the programme delivers value for money, avoids NAO criticism, and complies with government spending controls. Protect the department from reputational damage if the platform fails to perform during a real crisis.

**Context & Background**: As Accounting Officer, the Permanent Secretary is personally accountable to Parliament for the proper use of public funds. Previous DEFRA IT programmes (e.g., Rural Payments Agency CAP delivery) attracted significant NAO criticism. There is institutional memory of delivery failure risk.

**Driver Intensity**: HIGH

**Enablers**:
- Strong programme governance with clear escalation
- Phased delivery demonstrating early value
- Robust business case with measurable benefits

**Blockers**:
- Overly ambitious scope without phased delivery
- Insufficient user research leading to low adoption
- Dependency on third-party data providers outside government control

**Related Stakeholders**: S-6 (Finance Director), S-16 (Treasury), S-15 (CDDO)

---

### SD-3: SRO -- Programme Delivery Success

**Stakeholder**: S-3 SRO

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Deliver a working platform that passes GDS service assessment, meets user needs, and is adopted by DEFRA policy teams as their primary tool for supply chain monitoring. Personal reputation tied to programme success.

**Context & Background**: The SRO is accountable for programme outcomes across all delivery phases. Success here is career-defining -- demonstrating the ability to deliver complex cross-departmental digital programmes. Failure risks reassignment and departmental credibility.

**Driver Intensity**: HIGH

**Enablers**:
- Experienced delivery team with agile capability
- Clear user needs validated through research
- Supportive ministerial backing

**Blockers**:
- Resource competition with other DEFRA digital programmes
- Scope creep from multiple stakeholder demands
- Technical complexity of real-time data integration

**Related Stakeholders**: S-4 (CDO), S-5 (Policy Team)

---

### SD-4: DEFRA CDO -- Architecture Excellence

**Stakeholder**: S-4 DEFRA Chief Digital Officer

**Driver Category**: STRATEGIC

**Driver Statement**: Establish the platform as a reference architecture for DEFRA's digital transformation, demonstrating cloud-native, event-driven design patterns that can be reused across DEFRA projects (003, 004).

**Context & Background**: DEFRA manages multiple data-intensive platforms across environment, agriculture, and food domains. The CDO needs to show that modern architecture patterns can be applied to government challenges, attracting and retaining digital talent while reducing long-term technical debt.

**Driver Intensity**: HIGH

**Enablers**:
- Alignment with Architecture Principles (ARC-000-PRIN-v1.0)
- Reusable components shared with projects 003 and 004
- Technology Code of Practice compliance

**Blockers**:
- Legacy system integration constraints
- Skills gaps in the existing DEFRA digital team
- Pressure to reuse existing (outdated) platforms

**Related Stakeholders**: S-8 (Cyber Security Lead), S-15 (CDDO)

---

### SD-5: Food Supply Chain Analysis Team -- Operational Insight

**Stakeholder**: S-5 Policy Analysts

**Driver Category**: OPERATIONAL

**Driver Statement**: Replace fragmented manual processes (spreadsheets, email chains, phone calls to industry contacts) with a single platform providing real-time visibility of supply chain status, enabling faster and more evidence-based policy advice to Ministers.

**Context & Background**: Currently, supply chain monitoring relies on informal industry relationships, weekly reports from trade associations, and ad-hoc data requests. During the 2022 egg shortage, the team spent days manually gathering data that should have been available in hours. Analysts need self-service analytics without relying on IT for every query.

**Driver Intensity**: HIGH

**Enablers**:
- User-friendly dashboards requiring minimal training
- Automated data ingestion from key supply chain nodes
- Self-service reporting and alert configuration

**Blockers**:
- Resistance to changing established working practices
- Data quality issues from heterogeneous sources
- Analysts lacking confidence in automated data vs. personal contacts

**Related Stakeholders**: S-1 (Secretary of State), S-9 (FSA)

---

### SD-6: Finance Director -- Cost Control

**Stakeholder**: S-6 Finance Director

**Driver Category**: FINANCIAL

**Driver Statement**: Contain programme costs within the approved spending envelope (£12M over 3 years) and demonstrate measurable return on investment through avoided crisis costs and operational efficiencies.

**Context & Background**: DEFRA digital spend is under Treasury scrutiny following the 2025 Spending Review. Every programme must demonstrate value for money. The Finance Director needs quarterly cost forecasts and benefit realisation tracking to satisfy HMT reporting requirements.

**Driver Intensity**: MEDIUM

**Enablers**:
- Phased delivery with clear cost-per-phase breakdowns
- Benefit realisation framework from day one
- Cloud consumption model allowing cost scaling with usage

**Blockers**:
- Unpredictable data acquisition costs from commercial providers
- Scope expansion without corresponding budget increase
- Hidden costs in cross-departmental data sharing agreements

**Related Stakeholders**: S-16 (Treasury), S-2 (Permanent Secretary)

---

### SD-7: SIRO -- Information Risk Management

**Stakeholder**: S-7 DEFRA SIRO

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the platform handles commercially sensitive supply chain data and any personal data in compliance with UK GDPR, the Official Secrets Act (where applicable), and DEFRA's information risk appetite. Avoid data breaches that could damage industry trust and government credibility.

**Context & Background**: The platform will aggregate commercially sensitive data from retailers and importers. A data breach could expose competitive intelligence, destroy industry willingness to share data, and trigger ICO enforcement action. The SIRO must sign off the risk acceptance for the platform's data handling.

**Driver Intensity**: HIGH

**Enablers**:
- Robust data classification and access controls
- DPIA completed before industry data onboarding
- Clear data sharing agreements with legal protections

**Blockers**:
- Ambiguity about classification of aggregated supply chain data
- Industry distrust of government data handling
- Complex data residency requirements

**Related Stakeholders**: S-8 (Cyber Security Lead), S-10 (Retailers)

---

### SD-8: FSA -- Consumer Protection Intelligence

**Stakeholder**: S-9 Food Standards Agency

**Driver Category**: COMPLIANCE / CUSTOMER

**Driver Statement**: Gain early visibility of supply chain disruptions that could affect food safety (e.g., cold chain failures, supplier substitution, contamination risks) to enable proactive consumer protection interventions.

**Context & Background**: The FSA's primary mandate is protecting consumers. Supply disruptions often create food safety risks as suppliers substitute ingredients, extend shelf life, or compromise cold chain integrity to maintain supply. The FSA needs the platform to provide an early warning layer complementing their existing food safety surveillance.

**Driver Intensity**: CRITICAL

**Enablers**:
- Real-time data feeds with food safety indicators
- Integration with FSA's existing surveillance systems
- Joint analyst access to the platform

**Blockers**:
- Data access governance between DEFRA and FSA
- Different data classification requirements
- Technical integration complexity between DEFRA and FSA systems

**Related Stakeholders**: S-1 (Secretary of State), S-5 (Policy Team)

---

### SD-9: Major Retailers -- Competitive Confidentiality

**Stakeholder**: S-10 Major Retailers

**Driver Category**: RISK / STRATEGIC

**Driver Statement**: Participate in government supply chain monitoring only if commercially sensitive data (pricing, supplier relationships, stock levels) is protected from competitors and Freedom of Information (FOI) requests. Seek mutual benefit through aggregated industry intelligence.

**Context & Background**: Retailers hold the most granular supply chain data but face existential competitive risk from disclosure. Previous voluntary sharing initiatives (e.g., during COVID-19) worked because of crisis conditions and temporary assurances. Sustained participation requires legally binding data protection and clear mutual benefit (e.g., access to aggregated industry benchmarks).

**Driver Intensity**: HIGH

**Enablers**:
- FOI exemptions for commercially sensitive data (s.43 FOIA 2000)
- Aggregation and anonymisation before government access
- Industry advisory panel with retailer representation
- Reciprocal access to aggregated supply chain intelligence

**Blockers**:
- Distrust of government data handling after past FOI disclosures
- Competitive sensitivity of supply chain data
- Legal uncertainty about FOI exemption durability
- Cost of implementing data feeds

**Related Stakeholders**: S-7 (SIRO), S-9 (FSA), S-13 (NFU)

---

### SD-10: Cabinet Office -- Cross-Government Dashboard

**Stakeholder**: S-14 Cabinet Office (Project 005)

**Driver Category**: OPERATIONAL

**Driver Statement**: Receive reliable, timely, standardised food supply chain metrics from the platform to populate the National Food Strategy Dashboard, enabling cross-departmental policy coordination and ministerial reporting.

**Context & Background**: The National Food Strategy Dashboard (Project 005) depends on data from all four SDG 2 projects. Supply chain resilience metrics are a critical input. The Cabinet Office needs data delivered through standard APIs with defined quality SLAs, not ad-hoc reports.

**Driver Intensity**: MEDIUM

**Enablers**:
- Published API with versioned data contracts
- Agreed data quality SLAs and freshness targets
- Alignment with cross-programme data standards

**Blockers**:
- Platform delays pushing back dashboard data availability
- Data quality issues in early phases
- Misaligned release schedules between projects

**Related Stakeholders**: S-3 (SRO), S-4 (CDO)

---

### SD-11: Treasury -- Value for Money

**Stakeholder**: S-16 Treasury (HMT)

**Driver Category**: FINANCIAL

**Driver Statement**: Ensure the programme delivers demonstrable value for money against the approved business case, with clear benefit realisation metrics and exit strategy if benefits are not achieved.

**Context & Background**: HMT approved the programme within the 2025 Spending Review. They require quarterly benefit tracking and reserve the right to pause funding at stage gates if the programme is not delivering against its business case metrics.

**Driver Intensity**: MEDIUM

**Enablers**:
- Robust benefits realisation framework
- Independent assurance reviews (IPA gateway reviews)
- Phased funding model aligned with delivery milestones

**Blockers**:
- Benefits that are difficult to quantify (crisis avoidance is counterfactual)
- Cross-departmental benefits attribution complexity
- Spending review reprioritisation risk

**Related Stakeholders**: S-6 (Finance Director), S-2 (Permanent Secretary)

---

### SD-12: CDDO -- Standards Compliance

**Stakeholder**: S-15 CDDO

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure the programme meets the GDS Service Standard, Technology Code of Practice, and cross-government spend control requirements. The platform should be a positive example of government digital delivery.

**Context & Background**: CDDO provides assurance for government digital programmes above £1M. They assess against the 14-point Service Standard and 12-point Technology Code of Practice. Failure to pass assessment gates can delay or halt programmes.

**Driver Intensity**: MEDIUM

**Enablers**:
- User research embedded from Discovery
- Open standards and open source preferred
- Accessibility built in from the start

**Blockers**:
- Insufficient user research evidence
- Proprietary technology choices without justification
- Poor documentation of design decisions

**Related Stakeholders**: S-4 (CDO), S-3 (SRO)

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve Real-Time Supply Chain Visibility

**Derived From Drivers**: SD-1, SD-5, SD-8

**Goal Owner**: S-3 SRO

**Goal Statement**: Deliver a platform providing near-real-time ( < 4 hours latency) visibility of UK food supply chain status across the top 20 food categories by volume, covering > 60% of UK food supply by Q4 2027.

**Why This Matters**: Addresses the Minister's need for crisis preparedness (SD-1), the policy team's need for operational insight (SD-5), and the FSA's consumer protection intelligence requirement (SD-8).

**Success Metrics**:
- **Primary Metric**: Percentage of UK food supply (by volume) with real-time monitoring coverage
- **Secondary Metrics**:
  - Data latency (time from source event to platform visibility)
  - Number of food categories monitored
  - Number of active data providers connected

**Baseline**: No systematic real-time monitoring; manual processes with 3-7 day latency

**Target**: > 60% coverage, < 4 hours latency, 20 food categories, 50+ data providers

**Measurement Method**: Platform telemetry dashboards tracking data feed health, coverage calculations from ONS food consumption data

**Dependencies**:
- Data sharing agreements signed with major retailers (SD-9)
- Border Force and port data feeds operational (S-11, S-12)
- Technical integration with FSA systems complete (SD-8)

**Risks to Achievement**:
- Retailers refuse to share data without regulatory compulsion
- Data quality from heterogeneous sources is insufficient for meaningful analysis
- Technical complexity of real-time ingestion exceeds team capability

---

### Goal G-2: Detect Supply Disruptions Before Consumer Impact

**Derived From Drivers**: SD-1, SD-8

**Goal Owner**: S-5 Policy Team Lead

**Goal Statement**: Develop predictive alerting capability that identifies potential supply disruptions at least 72 hours before consumer-facing shortages, with a false positive rate < 20%, operational by Q2 2027.

**Why This Matters**: The core value proposition -- giving government lead time to respond before crises become political events.

**Success Metrics**:
- **Primary Metric**: Average lead time between alert and consumer-visible disruption
- **Secondary Metrics**:
  - Alert accuracy (true positive rate)
  - Response time from alert to policy team acknowledgement
  - Number of disruptions detected vs. missed

**Baseline**: Zero systematic early warning; disruptions identified via media or industry calls

**Target**: 72 hours average lead time, > 80% true positive rate

**Measurement Method**: Post-incident analysis comparing alert timestamps to reported consumer impact

**Dependencies**:
- G-1 must deliver sufficient data coverage for pattern detection
- Historical disruption data for model training
- Policy team trained on alert response procedures

**Risks to Achievement**:
- Insufficient historical data to train reliable prediction models
- Supply chain dynamics too complex for current analytical approaches
- Alert fatigue from false positives reduces analyst trust

---

### Goal G-3: Pass GDS Service Assessment at Beta

**Derived From Drivers**: SD-3, SD-12

**Goal Owner**: S-3 SRO

**Goal Statement**: Pass the GDS Beta service assessment with no critical findings and fewer than 3 advisory findings by Q3 2027.

**Why This Matters**: Mandatory gate for government digital services. Failure delays launch and signals poor delivery capability.

**Success Metrics**:
- **Primary Metric**: Assessment outcome (Pass/Not Pass)
- **Secondary Metrics**:
  - Number of critical findings
  - Number of advisory findings
  - User satisfaction scores from Beta users

**Baseline**: Not yet assessed

**Target**: Pass with 0 critical, < 3 advisory findings

**Measurement Method**: GDS service assessment panel report

**Dependencies**:
- Continuous user research throughout Alpha and Beta
- Accessibility testing completed
- Performance testing against defined SLOs

**Risks to Achievement**:
- Insufficient user research evidence
- Accessibility gaps in specialist data visualisation components
- Lack of documented design decisions (ADRs)

---

### Goal G-4: Contain Programme Costs Within Budget

**Derived From Drivers**: SD-2, SD-6, SD-11

**Goal Owner**: S-6 Finance Director

**Goal Statement**: Deliver the platform within the approved £12M 3-year budget, with cost variance < 10% per phase, demonstrating a positive cost-benefit ratio by Year 3.

**Why This Matters**: Satisfies Treasury spending controls, protects the Permanent Secretary from NAO criticism, and demonstrates DEFRA's digital delivery maturity.

**Success Metrics**:
- **Primary Metric**: Total programme spend vs. approved budget
- **Secondary Metrics**:
  - Cost variance per delivery phase
  - Benefit-to-cost ratio
  - Cost per data source integrated

**Baseline**: £12M approved over 3 years (FY 2026/27: £4M, FY 2027/28: £5M, FY 2028/29: £3M)

**Target**: < 10% variance, BCR > 1.5 by Year 3

**Measurement Method**: Quarterly financial reporting to programme board, IPA gateway review at major milestones

**Dependencies**:
- Data acquisition costs predictable and within estimates
- Cloud infrastructure costs scale as modelled
- No major scope changes without corresponding budget adjustment

**Risks to Achievement**:
- Data acquisition costs from commercial providers exceed estimates
- Scope creep from ministerial requests without budget uplift
- Foreign exchange risk on international data feeds

---

### Goal G-5: Secure Industry Data Participation

**Derived From Drivers**: SD-9, SD-7

**Goal Owner**: S-3 SRO

**Goal Statement**: Onboard at least 8 of the top 10 UK food retailers and 5 major importers onto the platform with signed data sharing agreements by Q1 2028.

**Why This Matters**: Without industry data, the platform has no unique value over existing open-source indicators.

**Success Metrics**:
- **Primary Metric**: Number of signed data sharing agreements with top-10 retailers
- **Secondary Metrics**:
  - Volume of data received per provider
  - Data quality score per provider
  - Provider satisfaction with data handling

**Baseline**: Zero formal data sharing agreements for supply chain monitoring

**Target**: 8/10 top retailers, 5 major importers, active data feeds from all

**Measurement Method**: Data partnership board tracking, quarterly provider satisfaction survey

**Dependencies**:
- Legal framework for FOI exemptions confirmed
- Data aggregation and anonymisation architecture operational
- Industry advisory panel established and meeting regularly

**Risks to Achievement**:
- Retailers refuse participation without regulatory mandate
- FOI exemption challenge succeeds, destroying industry trust
- Cost of data feed implementation prohibitive for smaller importers

---

### Goal G-6: Deliver FSA Integration

**Derived From Drivers**: SD-8

**Goal Owner**: S-9 FSA Representative

**Goal Statement**: Deliver operational data integration between the platform and FSA surveillance systems, enabling FSA analysts to access supply chain data with < 1 hour latency, by Q2 2027.

**Why This Matters**: The FSA is the strongest external advocate and co-funder. Their integration validates the platform's cross-government value.

**Success Metrics**:
- **Primary Metric**: FSA analyst adoption rate (active users / licensed users)
- **Secondary Metrics**:
  - Data feed latency DEFRA-to-FSA
  - Number of food safety incidents where platform data contributed to early detection

**Baseline**: No automated data sharing; ad-hoc email and phone requests

**Target**: > 80% FSA analyst adoption, < 1 hour latency, measurable contribution to 5+ safety interventions per year

**Measurement Method**: Platform usage analytics, FSA incident reports cross-referenced with platform alerts

**Dependencies**:
- Data governance agreement between DEFRA and FSA
- Technical integration architecture agreed
- FSA security accreditation of DEFRA platform data feeds

**Risks to Achievement**:
- Governance disagreement on data access scope
- Technical incompatibility between DEFRA and FSA security environments
- FSA analysts prefer existing tools and resist adoption

---

### Goal G-7: Supply Data to National Food Strategy Dashboard

**Derived From Drivers**: SD-10

**Goal Owner**: S-4 CDO

**Goal Statement**: Deliver published, versioned APIs providing food supply chain resilience metrics to the National Food Strategy Dashboard (Project 005), with 99.5% availability and daily refresh, by Q3 2027.

**Why This Matters**: The Cabinet Office dashboard depends on this platform as its primary supply chain data source. Failure blocks cross-government food strategy monitoring.

**Success Metrics**:
- **Primary Metric**: API availability (uptime percentage)
- **Secondary Metrics**:
  - Data freshness (hours since last update)
  - API response time (p95 latency)
  - Number of metrics exposed

**Baseline**: No standardised data feed to Cabinet Office

**Target**: 99.5% availability, daily data refresh, < 2 second p95 response, 15+ metrics

**Measurement Method**: API monitoring dashboards, cross-programme data quality reviews

**Dependencies**:
- G-1 real-time data coverage must be operational
- Data contract agreed with Project 005 team
- API versioning and deprecation policy in place

**Risks to Achievement**:
- Platform delays cascade to dashboard timeline
- Data quality insufficient for dashboard-grade metrics
- Misaligned metric definitions between DEFRA and Cabinet Office

---

### Goal G-8: Achieve Security Accreditation

**Derived From Drivers**: SD-7, SD-4

**Goal Owner**: S-7 SIRO

**Goal Statement**: Achieve OFFICIAL security accreditation with Cyber Essentials Plus certification and successful IT Health Check before the platform handles commercial supply chain data, by Q4 2026.

**Why This Matters**: Security accreditation is a prerequisite for onboarding industry data. Without it, retailers will not share data and the platform cannot achieve its core purpose.

**Success Metrics**:
- **Primary Metric**: Security accreditation granted (Yes/No)
- **Secondary Metrics**:
  - Number of critical vulnerabilities at IT Health Check
  - Time to remediate identified vulnerabilities
  - Cyber Essentials Plus certification status

**Baseline**: Not yet assessed

**Target**: Accreditation granted, 0 critical vulnerabilities, CE+ certified

**Measurement Method**: IT Health Check report, CE+ certificate, SIRO risk acceptance sign-off

**Dependencies**:
- Security architecture reviewed and approved
- Penetration testing completed
- Incident response procedures documented

**Risks to Achievement**:
- Critical vulnerabilities discovered during health check
- Security remediation delays programme timeline
- SIRO risk appetite lower than expected

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Government Response Time to Food Supply Disruptions

**Supported Goals**: G-1, G-2

**Outcome Statement**: Government response time to food supply disruptions reduced from an average of 7 days (manual detection and response) to < 48 hours (automated detection and coordinated response).

**Measurement Details**:
- **KPI**: Average time from supply disruption onset to government coordinated response
- **Current Value**: ~7 days (based on 2022-2025 incident analysis)
- **Target Value**: < 48 hours
- **Measurement Frequency**: Per-incident, reported quarterly
- **Data Source**: DEFRA incident management records, platform alert logs
- **Report Owner**: S-5 Policy Team Lead

**Business Value**:
- **Financial Impact**: Estimated £50-200M avoided economic loss per major disruption through earlier intervention
- **Strategic Impact**: UK positioned as global leader in food supply chain resilience
- **Operational Impact**: Policy team capacity freed from manual data gathering
- **Customer Impact**: Reduced consumer exposure to shortages and price spikes

**Timeline**:
- **Phase 1 (Months 1-6)**: Platform MVP with manual alert triage -- target < 5 day response
- **Phase 2 (Months 7-12)**: Automated alerting for top 10 food categories -- target < 72 hour response
- **Phase 3 (Months 13-24)**: Predictive capability across 20 categories -- target < 48 hour response
- **Sustainment (Year 3+)**: Continuous improvement, target < 24 hours

**Stakeholder Benefits**:
- **S-1 Secretary of State**: Confident crisis response, fewer parliamentary surprises
- **S-5 Policy Team**: Evidence-based briefings produced in hours not days
- **S-9 FSA**: Early food safety intervention capability

**Leading Indicators**:
- Number of data providers connected
- Alert detection accuracy improving over time
- Policy team using platform daily (usage metrics)

**Lagging Indicators**:
- Post-incident analysis shows platform-detected disruptions before media
- Ministerial feedback on crisis briefing quality
- Reduced parliamentary questions on food supply surprises

---

### Outcome O-2: Industry Data Sharing Ecosystem Established

**Supported Goals**: G-5, G-8

**Outcome Statement**: A sustainable data sharing ecosystem where > 60% of UK food supply by volume is monitored through voluntary industry participation, underpinned by trust and mutual benefit.

**Measurement Details**:
- **KPI**: Percentage of UK food supply (by volume) covered by data sharing agreements
- **Current Value**: 0%
- **Target Value**: > 60%
- **Measurement Frequency**: Quarterly
- **Data Source**: Platform coverage dashboard, ONS food supply data
- **Report Owner**: S-3 SRO

**Business Value**:
- **Financial Impact**: Avoided cost of mandatory reporting regulation (estimated £30-50M industry compliance cost)
- **Strategic Impact**: Public-private partnership model replicable across other resilience domains
- **Operational Impact**: Comprehensive supply chain picture without regulatory burden

**Timeline**:
- **Phase 1 (Months 1-6)**: 3 pilot retailers onboarded (15% coverage)
- **Phase 2 (Months 7-12)**: 6 retailers + 2 importers (40% coverage)
- **Phase 3 (Months 13-24)**: 8 retailers + 5 importers (60% coverage)
- **Sustainment (Year 3+)**: Expand to second-tier retailers and producers ( > 75%)

**Stakeholder Benefits**:
- **S-10 Retailers**: Access to aggregated industry intelligence, reduced regulatory risk
- **S-9 FSA**: Broader food safety surveillance data
- **S-13 NFU**: Domestic production data integration

**Leading Indicators**:
- Number of data sharing agreements in negotiation
- Retailer attendance at industry advisory panel
- Pilot data quality scores

**Lagging Indicators**:
- Coverage percentage milestone achievement
- Provider renewal rates (annual re-commitment)
- Industry satisfaction survey scores

---

### Outcome O-3: Cross-Government Food Intelligence Capability

**Supported Goals**: G-6, G-7

**Outcome Statement**: A single platform providing food supply chain intelligence consumed by DEFRA, FSA, and Cabinet Office, eliminating data silos and enabling joined-up food policy across government.

**Measurement Details**:
- **KPI**: Number of government departments/agencies actively consuming platform data
- **Current Value**: 0
- **Target Value**: 3+ (DEFRA, FSA, Cabinet Office)
- **Measurement Frequency**: Monthly
- **Data Source**: Platform API usage analytics, user activity logs
- **Report Owner**: S-4 CDO

**Business Value**:
- **Financial Impact**: Reduced duplication of data collection across departments (est. £2M/year saved)
- **Strategic Impact**: Model for cross-departmental data platforms per government data strategy
- **Operational Impact**: Single source of truth for food supply chain data (Principle 10)

**Timeline**:
- **Phase 1 (Months 1-6)**: DEFRA internal users operational
- **Phase 2 (Months 7-12)**: FSA integration live
- **Phase 3 (Months 13-24)**: Cabinet Office Project 005 API operational
- **Sustainment (Year 3+)**: Expand to DHSC, DLUHC for food poverty indicators

**Stakeholder Benefits**:
- **S-14 Cabinet Office**: Reliable data feed for National Food Strategy Dashboard
- **S-9 FSA**: Integrated food safety surveillance layer
- **S-4 CDO**: Reusable architecture pattern for DEFRA

**Leading Indicators**:
- Cross-departmental data governance agreements signed
- API integration development progress
- User research with FSA and Cabinet Office analysts

**Lagging Indicators**:
- Active users across all consuming departments
- Data-informed policy decisions cited in ministerial submissions
- Reduction in ad-hoc data requests between departments

---

### Outcome O-4: Positive Cost-Benefit Ratio Demonstrated

**Supported Goals**: G-4

**Outcome Statement**: The programme demonstrates a benefit-to-cost ratio > 1.5 by Year 3, validated through independent assurance, satisfying Treasury and NAO scrutiny.

**Measurement Details**:
- **KPI**: Benefit-to-cost ratio (BCR)
- **Current Value**: N/A (pre-delivery)
- **Target Value**: > 1.5
- **Measurement Frequency**: Annually
- **Data Source**: Benefits realisation tracker, quarterly financial reports, IPA gateway reviews
- **Report Owner**: S-6 Finance Director

**Business Value**:
- **Financial Impact**: Programme justified against public spending criteria
- **Strategic Impact**: Supports future DEFRA digital investment cases

**Timeline**:
- **Phase 1 (Months 1-12)**: Costs tracked, early benefit indicators identified
- **Phase 2 (Months 13-24)**: First measurable benefits (operational efficiency, crisis response)
- **Phase 3 (Months 25-36)**: Full BCR calculation with independent validation
- **Sustainment (Year 3+)**: Annual benefits realisation review

**Stakeholder Benefits**:
- **S-16 Treasury**: Value for money demonstrated
- **S-2 Permanent Secretary**: Accounting Officer assurance met
- **S-6 Finance Director**: Clean financial governance record

**Leading Indicators**:
- Phase cost variance within 10% tolerance
- Benefit realisation metrics being tracked
- IPA gateway reviews progressing positively

**Lagging Indicators**:
- Final BCR calculation > 1.5
- NAO report (if commissioned) positive or neutral
- Treasury approves continued funding

---

### Outcome O-5: GDS Service Standard Compliance

**Supported Goals**: G-3

**Outcome Statement**: The platform passes GDS Beta service assessment and achieves Live service status, demonstrating DEFRA's digital delivery maturity and user-centred design capability.

**Measurement Details**:
- **KPI**: GDS assessment outcome
- **Current Value**: Not yet assessed
- **Target Value**: Pass at Beta, Pass at Live
- **Measurement Frequency**: At assessment milestones
- **Data Source**: GDS assessment panel reports
- **Report Owner**: S-3 SRO

**Business Value**:
- **Strategic Impact**: DEFRA credibility as a digital-capable department
- **Operational Impact**: Service meets user needs, accessible and performant

**Timeline**:
- **Phase 1 (Months 1-6)**: Discovery and Alpha complete
- **Phase 2 (Months 7-12)**: Beta assessment
- **Phase 3 (Months 13-24)**: Live assessment
- **Sustainment (Year 3+)**: Continuous improvement, annual reassessment

**Stakeholder Benefits**:
- **S-15 CDDO**: Programme meets cross-government standards
- **S-3 SRO**: Programme delivery credibility
- **S-5 Policy Team**: Service that genuinely meets their needs

**Leading Indicators**:
- User research sessions completed per sprint
- Accessibility audit pass rate
- Design decision documentation (ADRs) up to date

**Lagging Indicators**:
- GDS assessment outcome
- User satisfaction scores
- Task completion rates in usability testing

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| S-1 Secretary of State | SD-1 | Crisis preparedness | G-1 | Real-time visibility | O-1 | Reduced response time |
| S-1 Secretary of State | SD-1 | Crisis preparedness | G-2 | Predictive alerting | O-1 | Reduced response time |
| S-2 Permanent Secretary | SD-2 | Governance accountability | G-4 | Cost containment | O-4 | Positive BCR |
| S-3 SRO | SD-3 | Programme delivery | G-3 | GDS assessment pass | O-5 | GDS compliance |
| S-3 SRO | SD-3 | Programme delivery | G-5 | Industry participation | O-2 | Data sharing ecosystem |
| S-4 CDO | SD-4 | Architecture excellence | G-7 | Dashboard API | O-3 | Cross-govt intelligence |
| S-5 Policy Team | SD-5 | Operational insight | G-1 | Real-time visibility | O-1 | Reduced response time |
| S-6 Finance Director | SD-6 | Cost control | G-4 | Cost containment | O-4 | Positive BCR |
| S-7 SIRO | SD-7 | Information risk | G-8 | Security accreditation | O-2 | Data sharing ecosystem |
| S-9 FSA | SD-8 | Consumer protection | G-6 | FSA integration | O-3 | Cross-govt intelligence |
| S-9 FSA | SD-8 | Consumer protection | G-2 | Predictive alerting | O-1 | Reduced response time |
| S-10 Retailers | SD-9 | Competitive confidentiality | G-5 | Industry participation | O-2 | Data sharing ecosystem |
| S-14 Cabinet Office | SD-10 | Cross-govt dashboard | G-7 | Dashboard API | O-3 | Cross-govt intelligence |
| S-16 Treasury | SD-11 | Value for money | G-4 | Cost containment | O-4 | Positive BCR |
| S-15 CDDO | SD-12 | Standards compliance | G-3 | GDS assessment pass | O-5 | GDS compliance |

### Conflict Analysis

**Conflict 1**: SD-1 (Speed of deployment) vs SD-9 (Industry data confidentiality)
- The Minister wants rapid deployment, but industry data onboarding requires time-consuming legal negotiations and trust-building
- **Resolution Strategy**: Phased approach -- launch with open-source data and government data feeds first (Phase 1), then progressively add industry data as agreements are signed. Demonstrate value with available data to maintain ministerial confidence while building industry relationships.

**Conflict 2**: SD-6 (Cost control) vs SD-5 (Comprehensive operational insight)
- The Finance Director wants to contain costs, but comprehensive supply chain coverage requires expensive commercial data acquisition and extensive integration work
- **Resolution Strategy**: Prioritise data sources by impact-per-pound. Start with the highest-value, lowest-cost data feeds (government border data, open agricultural statistics). Only pursue expensive commercial data where the business case for that specific feed is positive.

**Conflict 3**: SD-7 (Information risk caution) vs SD-1 (Rapid crisis response)
- The SIRO requires thorough risk assessment before handling commercial data, but the Minister needs the platform operational quickly
- **Resolution Strategy**: Separate the security accreditation pathway for government-only data (fast track) from commercially sensitive data (full accreditation). Launch initial capability with government data while completing industry data accreditation in parallel.

### Synergies

- **Synergy 1**: SD-1 (Ministerial crisis readiness) and SD-8 (FSA consumer protection) -- both drive G-1 and G-2. FSA co-funding strengthens the business case and provides additional data access through their regulatory powers.
- **Synergy 2**: SD-4 (Architecture excellence) and SD-10 (Cross-govt dashboard) -- both drive reusable, well-architected APIs. Building for Project 005 forces good API design that benefits all consumers.
- **Synergy 3**: SD-9 (Retailer confidentiality) and SD-7 (Information risk) -- both require robust data protection. Investment in security controls satisfies both industry trust and government risk management.

---

## Communication & Engagement Plan

### S-1: DEFRA Secretary of State

**Primary Message**: The platform will ensure you are never surprised by a food supply crisis again. Real-time monitoring and predictive alerts give you a 72-hour head start.

**Key Talking Points**:
- Early warning means proactive ministerial statements, not reactive damage control
- Dashboard providing at-a-glance supply chain status for briefings
- Industry voluntarily sharing data, demonstrating public-private partnership

**Communication Frequency**: Monthly ministerial briefing; ad-hoc crisis alerts

**Preferred Channel**: Ministerial submission with dashboard screenshots; private office briefing

**Success Story**: "Minister informed of potential egg supply disruption 4 days before media reports, enabling coordinated response with retailers"

### S-9: Food Standards Agency

**Primary Message**: The platform provides an early warning layer for food safety risks driven by supply chain disruption, complementing FSA's existing surveillance.

**Key Talking Points**:
- Shared data access enabling proactive consumer protection
- Joint analyst community building cross-government capability
- Integration with existing FSA systems, not replacement

**Communication Frequency**: Bi-weekly joint steering group; monthly data quality review

**Preferred Channel**: Joint steering committee; shared collaboration space

**Success Story**: "FSA identified cold chain risk in imported poultry 48 hours before potential contamination incident, enabling targeted inspections"

### S-10: Major Retailers

**Primary Message**: Your data is legally protected and aggregated before government access. In return, you receive industry intelligence you cannot get elsewhere.

**Key Talking Points**:
- FOI exemption under s.43 for commercially sensitive data
- Aggregation means no individual retailer data exposed
- Industry advisory panel gives you direct influence over platform direction
- Access to benchmarked supply chain resilience metrics

**Communication Frequency**: Quarterly industry advisory panel; annual data partnership review

**Preferred Channel**: Industry advisory panel meetings; dedicated account manager per retailer

**Success Story**: "Participating retailers received 5-day advance warning of shipping disruption at Felixstowe, enabling proactive stock redistribution"

### S-16: Treasury

**Primary Message**: The programme is on track and on budget, delivering measurable benefits in crisis response and operational efficiency.

**Key Talking Points**:
- Quarterly financial reports showing < 10% cost variance
- Benefit realisation tracking against approved business case
- Phased delivery reduces risk of sunk costs

**Communication Frequency**: Quarterly financial report; annual spending review submission

**Preferred Channel**: Formal written reports; HMT spending review meetings

**Success Story**: "Platform-enabled early intervention during Dover port disruption avoided estimated £150M in economic losses"

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| S-5 Policy Team | Manual data gathering via spreadsheets, emails, phone calls | Platform-based monitoring with automated alerts | HIGH | MEDIUM | Embed in existing workflows; training programme; demonstrate time savings |
| S-9 FSA Analysts | Separate surveillance systems; ad-hoc DEFRA data requests | Integrated data access through shared platform | MEDIUM | LOW | Joint design sessions; phased integration; maintain existing systems during transition |
| S-10 Retailers | No systematic data sharing with government | Regular automated data feeds to DEFRA platform | HIGH | HIGH | Industry advisory panel; demonstrate mutual benefit; FOI protections; pilot with willing participants |
| S-12 Port Operators | Ad-hoc information sharing during disruptions | Automated data feeds from logistics systems | MEDIUM | MEDIUM | Technical support for integration; demonstrate operational benefit |

### Change Readiness

**Champions** (Enthusiastic supporters):
- S-5 Policy Team Lead -- frustrated with manual processes, keen for modern tools
- S-9 FSA -- strong co-funding commitment, sees clear value for consumer protection
- S-4 CDO -- sees the platform as a DEFRA digital transformation exemplar

**Fence-sitters** (Neutral, need convincing):
- S-10 Retailers -- willing in principle but need legal certainty on data protection
- S-12 Port Operators -- open to integration but concerned about implementation cost
- S-6 Finance Director -- supportive if costs stay within budget

**Resisters** (Opposed or skeptical):
- S-11 Border Force -- sceptical about adding data feeds to already strained systems; strategy: demonstrate minimal integration burden, offer DEFRA technical support
- Some S-5 analysts -- attached to existing informal industry contacts and sceptical of automated data; strategy: involve in user research, demonstrate platform complements rather than replaces personal networks

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Industry Data Refusal

**Related Stakeholders**: S-10 Retailers, S-13 NFU

**Risk Description**: Major retailers refuse to participate in voluntary data sharing, leaving the platform with insufficient data coverage to fulfil its purpose.

**Impact on Goals**: G-1, G-2, G-5 critically affected; O-1, O-2 unachievable

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Build compelling value proposition with pilot participants; ministerial engagement with retailer CEOs; reserve option for mandatory reporting regulation as backstop

**Contingency Plan**: Pivot to open-source and government data sources; explore alternative data acquisition (satellite imagery, shipping data, social media signals)

---

### Risk R-2: FOI Challenge Destroys Trust

**Related Stakeholders**: S-10 Retailers, S-7 SIRO

**Risk Description**: A Freedom of Information request successfully challenges the s.43 exemption for commercially sensitive supply chain data, exposing retailer data and destroying willingness to participate.

**Impact on Goals**: G-5 critically affected; O-2 undermined

**Probability**: LOW

**Impact**: CRITICAL

**Mitigation Strategy**: Legal review of FOI exemption before any data onboarding; data aggregation architecture ensuring individual retailer data is never stored in identifiable form; contractual commitments to retailers

**Contingency Plan**: Restructure data handling to ensure only aggregated, non-identifiable data held; amend data sharing agreements to reflect new legal position

---

### Risk R-3: NAO Scrutiny of Programme Delivery

**Related Stakeholders**: S-2 Permanent Secretary, S-16 Treasury

**Risk Description**: Programme cost overruns or benefit shortfalls attract NAO investigation, damaging DEFRA credibility and threatening programme continuation.

**Impact on Goals**: G-4 directly; all goals indirectly through funding risk

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Robust benefits realisation framework from day one; quarterly reporting to programme board; IPA gateway reviews at key milestones; phased delivery with early benefit demonstration

**Contingency Plan**: Descope to minimum viable platform; accelerate high-value-per-cost data sources; present honest assessment to NAO with remediation plan

---

### Risk R-4: FSA Integration Governance Dispute

**Related Stakeholders**: S-9 FSA, S-7 SIRO

**Risk Description**: DEFRA and FSA cannot agree on data access scope, classification, or governance, delaying or blocking integration.

**Impact on Goals**: G-6 directly; G-2, O-3 indirectly

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Joint steering group established early; data governance framework agreed in principle before technical integration; escalation to Permanent Secretaries if needed

**Contingency Plan**: Implement DEFRA-only capability first; resume FSA integration when governance resolved; offer FSA read-only access through controlled interface

---

### Risk R-5: Ministerial Priority Shift

**Related Stakeholders**: S-1 Secretary of State

**Risk Description**: A change in DEFRA Secretary of State or government priorities redirects attention away from food resilience, reducing political support and budget protection.

**Impact on Goals**: All goals at risk from reduced political sponsorship

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Build cross-party support through select committee engagement; demonstrate value to senior officials (Permanent Secretary) who outlast ministers; embed platform in DEFRA business-as-usual operations quickly

**Contingency Plan**: Reduce to operational monitoring tool without ministerial dashboard; focus on FSA and policy team value; seek alternative funding through operational budgets

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval (phase gates) | S-6 Finance Director | S-2 Permanent Secretary | S-16 Treasury | All stakeholders |
| Requirements prioritisation | Product Manager | S-3 SRO | S-5 Policy Team, S-9 FSA | S-4 CDO |
| Architecture decisions | Technical Architect | S-4 CDO | S-8 Cyber Lead, S-15 CDDO | S-3 SRO |
| Data sharing agreements | Data Partnership Lead | S-3 SRO | S-7 SIRO, Legal | S-10 Retailers |
| Security accreditation | S-8 Cyber Lead | S-7 SIRO | S-4 CDO | S-3 SRO |
| Go/No-go for Beta launch | S-3 SRO | S-2 Permanent Secretary | All stakeholders | S-1 Minister |
| Crisis alert escalation | S-5 Policy Team Lead | S-3 SRO | S-9 FSA | S-1 Minister |
| Cross-project data standards | S-4 CDO | S-3 SRO | S-14 Cabinet Office | Projects 003, 004 |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager -- day-to-day delivery decisions, sprint-level trade-offs
2. **Level 2**: SRO Programme Board -- scope changes, resource allocation, cross-stakeholder conflicts
3. **Level 3**: Permanent Secretary -- budget overruns > 10%, significant delivery risks, cross-departmental governance disputes
4. **Level 4**: Secretary of State -- strategic direction changes, industry relationship escalation, policy decisions affecting platform scope

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| S-3 SRO | Scheduled 2026-03-23 | Initial review of stakeholder identification | PENDING |
| S-5 Policy Team Lead | Scheduled 2026-03-23 | Validate driver and goal accuracy | PENDING |
| S-9 FSA Representative | Scheduled 2026-03-30 | Confirm FSA drivers and integration goals | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| SRO | Pending appointment | | |
| DEFRA CDO | Pending confirmation | | |
| FSA Representative | Pending nomination | | |

---

## Appendices

### Appendix A: Related Documents

- ARC-000-PRIN-v1.0 -- SDG 2 Enterprise Architecture Principles
- Project 003 (Food Waste Reduction Analytics) -- shared DEFRA domain
- Project 004 (Agricultural Subsidy Management) -- shared DEFRA domain
- Project 005 (National Food Strategy Dashboard) -- primary data consumer

### Appendix B: Glossary

| Term | Definition |
|------|-----------|
| BCR | Benefit-to-cost ratio |
| CAP | Common Agricultural Policy (EU) |
| CE+ | Cyber Essentials Plus |
| CDDO | Central Digital and Data Office |
| DPIA | Data Protection Impact Assessment |
| ELM | Environmental Land Management |
| FOI | Freedom of Information |
| FSA | Food Standards Agency |
| IPA | Infrastructure and Projects Authority |
| NAO | National Audit Office |
| SRO | Senior Responsible Owner |
| SIRO | Senior Information Risk Owner |

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 2 Programme | Governance context, cross-project principles | projects/000-global/ |
| GDS Service Standard | Standard | GOV.UK | 14-point assessment framework | gov.uk/service-manual |
| UK Food Security Report | Policy | DEFRA | Annual food supply chain risk assessment | gov.uk/defra |
| National Food Strategy | Policy | Cabinet Office | Henry Dimbleby recommendations | nationalfoodstrategy.org |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-03-09
**ArcKit Version**: 4.1.1
**Project**: Food Supply Chain Resilience Platform (Project 001)
**AI Model**: Claude Opus 4.6 (1M context)
