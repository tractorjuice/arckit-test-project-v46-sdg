# Stakeholder Drivers & Goals Analysis: UK Emissions Trading Registry

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | UK Emissions Trading Registry (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, UK ETS Registry Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | UK ETS Programme Board, DESNZ Digital, UK ETS Authority, Environment Agency, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the UK Emissions Trading Scheme (UK ETS) Registry, the digital system that manages carbon allowance accounts, tracks transactions, and ensures compliance for obligated entities. The UK ETS replaced the UK's participation in the EU ETS following Brexit and is a cornerstone of UK carbon pricing policy.

### Key Findings

The UK ETS Registry operates at the intersection of environmental regulation and financial markets, creating a uniquely complex stakeholder landscape. The strongest alignment exists between DESNZ (scheme design), the Environment Agency (compliance enforcement), and the devolved regulators (Scottish Environment Protection Agency, Natural Resources Wales, DAERA Northern Ireland) on the need for a robust, fraud-resistant registry. The most significant tension is between industry demands for a simple, low-cost compliance process and the regulatory requirement for rigorous Know Your Customer (KYC) and anti-money-laundering controls on what is effectively a financial trading system.

### Critical Success Factors

- Achieve 100% availability during the annual compliance surrender window (30 April deadline) — obligated entities face penalties for non-surrender
- Implement KYC/AML controls that satisfy FCA-equivalent standards without creating excessive barriers for legitimate industrial participants
- Maintain transaction processing within 26-hour settlement window mandated by the UK ETS legislation
- Achieve interoperability with potential EU ETS linkage (pending political negotiations)
- Prevent fraud, double-counting, and market manipulation in a market worth approximately GBP 5 billion annually

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong alignment on the need for a robust, functional registry, but significant tensions between regulatory rigour (Environment Agency, FCA), user simplicity (industrial operators), market efficiency (ICE Futures Europe, traders), and political sensitivity (DESNZ, devolved administrations). The four-nation governance structure adds complexity.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DESNZ Minister for Energy Security | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, market events |
| DESNZ Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board |
| SRO, UK ETS Registry | Programme Sponsor (DESNZ) | HIGH | HIGH | Manage Closely — Weekly programme board |
| UK ETS Authority | Joint authority (DESNZ, EA, SEPA, NRW, DAERA) | HIGH | HIGH | Manage Closely — Authority board |
| DESNZ Carbon Markets Team | Policy design, cap setting | HIGH | HIGH | Manage Closely — Requirements, compliance rules |
| DESNZ CDIO | Digital strategy | HIGH | MEDIUM | Keep Satisfied — Architecture governance |
| DESNZ SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA, risk acceptance |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Environment Agency | Regulator (England) | Compliance enforcement | HIGH | HIGH |
| SEPA | Regulator (Scotland) | Compliance enforcement | HIGH | HIGH |
| Natural Resources Wales | Regulator (Wales) | Compliance enforcement | HIGH | HIGH |
| DAERA | Regulator (Northern Ireland) | Compliance enforcement | HIGH | HIGH |
| FCA | Financial regulator | Market oversight, MiFID compliance | HIGH | HIGH |
| ICE Futures Europe | Exchange | UK ETS allowance auction and trading | HIGH | HIGH |
| Obligated operators (c.1,000) | Industry | Registry account holders, compliance | LOW | HIGH |
| Aviation operators | Airlines, business aviation | Aviation ETS compliance | LOW | HIGH |
| Traders and intermediaries | Financial sector | Carbon market participants | LOW | HIGH |
| Verifiers (UKAS accredited) | Assurance providers | Emissions verification | LOW | HIGH |
| HM Treasury | HM Treasury | Auction revenue (c. GBP 5bn/year) | HIGH | MEDIUM |
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| European Commission (DG CLIMA) | EU | Potential ETS linkage partner | MEDIUM | MEDIUM |
| UNFCCC Secretariat | International | International carbon market standards | LOW | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for registry outcomes | HIGH / HIGH | Manage Closely — Steering board |
| Service Owner | Owns end-to-end registry service | HIGH / HIGH | Manage Closely — Service reviews |
| Product Manager | Prioritises features | MEDIUM / HIGH | Keep Informed — Sprint reviews |
| CDDO | Assurance, spend control | HIGH / MEDIUM | Keep Satisfied — Spend control submissions |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        +---------------------+---------------------+
        |                     |                     |
        |   KEEP SATISFIED    |   MANAGE CLOSELY    |
   High |                     |                     |
        |  * HM Treasury      |  * DESNZ Minister   |
        |  * CDDO             |  * Permanent Sec.   |
        |  * DESNZ CDIO       |  * SRO              |
        |  * DESNZ SIRO       |  * UK ETS Authority |
 P      |                     |  * Carbon Markets   |
 O      |                     |  * Environment      |
 W      |                     |    Agency           |
 E      |                     |  * SEPA / NRW / DAERA|
 R      |                     |  * FCA              |
        |                     |  * ICE Futures      |
        +---------------------+---------------------+
        |                     |                     |
        |      MONITOR        |    KEEP INFORMED    |
        |                     |                     |
   Low  |  * UNFCCC           |  * Obligated ops    |
        |  * EU Commission    |  * Aviation ops     |
        |                     |  * Traders          |
        |                     |  * Verifiers        |
        +---------------------+---------------------+
```

---

## Stakeholder Drivers Analysis

### SD-1: UK ETS Authority — Robust, Compliant Registry Operations

**Stakeholder**: UK ETS Authority (joint DESNZ, EA, SEPA, NRW, DAERA)

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: Operate a registry that meets all UK ETS legislative requirements, processes transactions within mandated timescales, prevents fraud and double-counting, and supports the four-nation regulatory enforcement process reliably.

**Context & Background**:
The UK ETS Authority is the joint body responsible for the scheme across the four UK nations. The Greenhouse Gas Emissions Trading Scheme Order 2020 mandates registry requirements including account management, transaction processing, compliance tracking, and reporting. The registry must process allowance surrenders by 30 April annually — failure means operators face automatic penalties. The Authority needs a registry that works flawlessly during these critical compliance windows.

**Driver Intensity**: CRITICAL

**Enablers**:

- 99.95% availability during compliance windows
- Automated compliance tracking and penalty calculation
- Four-nation regulatory access with appropriate data segregation
- Full audit trail for all transactions (immutable ledger)
- Automated sanctions screening for all account holders

**Blockers**:

- Single points of failure in transaction processing
- Inadequate KYC/AML controls exposing the scheme to fraud
- Registry unavailability during surrender deadline
- Inconsistent data access across the four regulators

**Related Stakeholders**: FCA (market integrity), Obligated operators (compliance), HM Treasury (auction revenue)

---

### SD-2: FCA — Market Integrity and Financial Crime Prevention

**Stakeholder**: Financial Conduct Authority

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure the UK ETS Registry implements financial-grade controls for market abuse prevention, insider dealing detection, anti-money laundering, and Know Your Customer verification — the carbon market is classified as a financial market and must be regulated to the same standard.

**Context & Background**:
UK ETS allowances are classified as financial instruments under UK MiFID. The FCA is responsible for market oversight, including preventing market manipulation, insider dealing, and money laundering through carbon markets. The EU ETS experienced significant VAT carousel fraud (estimated EUR 5 billion) and phishing attacks on registry accounts. The FCA expects the UK ETS Registry to implement controls equivalent to a regulated financial exchange, including real-time transaction monitoring, suspicious activity reporting, and robust identity verification.

**Driver Intensity**: CRITICAL

**Enablers**:

- Real-time transaction monitoring with anomaly detection
- Automated suspicious activity reports (SARs) to NCA
- KYC verification integrated with Companies House and PEP/sanctions databases
- Transaction velocity limits and circuit breakers for abnormal trading patterns
- Segregation of market-sensitive information (pre-auction data)

**Blockers**:

- Registry designed as environmental compliance tool without financial-grade controls
- Insufficient identity verification allowing anonymous or pseudonymous accounts
- No real-time monitoring capability
- Weak access controls enabling insider access to market-sensitive data

**Related Stakeholders**: UK ETS Authority (registry operator), ICE Futures Europe (exchange), Traders (market participants), HM Treasury (regulatory framework)

---

### SD-3: Obligated Industrial Operators — Simple, Efficient Compliance

**Stakeholder**: Obligated operators (c.1,000 installations — power stations, refineries, steel works, cement plants, ceramics)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Complete UK ETS compliance obligations (account management, emissions reporting, allowance surrender) with minimum administrative burden, clear guidance, and reasonable KYC requirements that recognise these are industrial companies, not financial traders.

**Context & Background**:
Obligated operators are primarily industrial companies whose core business is manufacturing, power generation, or refining — not financial trading. Many have small compliance teams (often 1-2 people managing ETS alongside other environmental regulations). Under the EU ETS, operators complained about complex registry interfaces, excessive KYC requirements for simple compliance accounts, and unclear error messages during surrender. The UK ETS is an opportunity to improve on the EU ETS user experience while maintaining regulatory rigour.

**Driver Intensity**: HIGH

**Enablers**:

- Intuitive registry interface designed for non-specialist compliance staff
- Clear, step-by-step guidance for annual surrender process
- Proportionate KYC — simplified requirements for compliance-only accounts vs full requirements for trading accounts
- Automated reminders for key compliance deadlines
- API integration enabling operators to submit data from their environmental management systems

**Blockers**:

- Financial-grade KYC requirements applied uniformly to all account types
- Complex interface designed for financial traders, not industrial compliance staff
- Unclear error messages and poor guidance during surrender process
- Registry downtime during the pre-surrender preparation period

**Related Stakeholders**: UK ETS Authority (regulator), Verifiers (emissions verification), Environment Agency (enforcement)

---

### SD-4: HM Treasury — Reliable Auction Revenue

**Stakeholder**: HM Treasury

**Driver Category**: FINANCIAL

**Driver Statement**: Ensure the UK ETS Registry and auction platform reliably generate approximately GBP 5 billion per year in auction revenue, with transparent price discovery, competitive auction participation, and no market disruption that would impact revenue forecasts.

**Context & Background**:
UK ETS auction revenue is a significant income stream for HM Treasury, included in fiscal forecasts. Allowances are auctioned through ICE Futures Europe on behalf of the UK Government. The registry must reliably process auction settlement, maintain accurate account balances, and support the auction platform's clearing requirements. Any registry failure that disrupts auctions would have immediate fiscal consequences and market confidence impacts.

**Driver Intensity**: HIGH

**Enablers**:

- Reliable API integration with ICE Futures Europe auction platform
- Automated auction settlement processing within contractual timescales
- Real-time account balance verification for auction participation eligibility
- Transparent reporting of auction results and revenue to HM Treasury

**Blockers**:

- Registry failures disrupting auction settlement
- Account balance discrepancies affecting auction eligibility
- Security breaches undermining market confidence
- System performance issues during high-volume auction days

**Related Stakeholders**: ICE Futures Europe (auction platform), UK ETS Authority (scheme governance), FCA (market oversight)

---

### SD-5: ICE Futures Europe — Reliable Trading Infrastructure Integration

**Stakeholder**: ICE Futures Europe (Intercontinental Exchange)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Maintain reliable, high-performance integration between the UK ETS Registry and ICE Futures Europe trading and clearing systems, with defined SLAs, clear error handling, and predictable settlement processes.

**Context & Background**:
ICE Futures Europe operates the UK ETS allowance auction platform and the secondary market for UK ETS futures and options. The registry must integrate with ICE's clearing house for allowance delivery against futures contracts and auction settlement. ICE requires registry API availability, predictable latency, and automated settlement — any registry issues that delay settlement create financial risk for ICE clearing members.

**Driver Intensity**: HIGH

**Enablers**:

- Documented, versioned API for registry-exchange integration
- Defined SLAs for transaction processing and settlement confirmation
- Automated reconciliation between registry and exchange records
- Disaster recovery that maintains integration availability

**Blockers**:

- Unplanned registry maintenance during trading hours
- API changes without adequate notice
- Settlement failures requiring manual intervention
- Inconsistent transaction processing times

**Related Stakeholders**: UK ETS Authority (registry governance), FCA (market oversight), HM Treasury (auction revenue)

---

## Driver-to-Goal Mapping

### Goal G-1: Achieve 100% Compliance Window Availability

**Derived From Drivers**: SD-1, SD-3

**Goal Owner**: SRO

**Goal Statement**: Achieve 100% registry availability during the annual surrender window (1 March — 30 April) and 99.95% availability year-round, with automated failover and no single points of failure.

**Success Metrics**:

- **Primary Metric**: Zero downtime during surrender window
- **Secondary Metrics**:
  - Annual availability exceeds 99.95%
  - Mean Time to Recovery (MTTR) under 15 minutes

---

### Goal G-2: Implement FCA-Grade Financial Crime Controls

**Derived From Drivers**: SD-2, SD-1

**Goal Owner**: DESNZ SIRO

**Goal Statement**: Implement KYC, AML, and market abuse detection controls that satisfy FCA supervisory expectations within 12 months of platform launch, with tiered requirements proportionate to account type.

**Success Metrics**:

- **Primary Metric**: FCA supervisory assessment passed without major findings
- **Secondary Metrics**:
  - All accounts KYC-verified before activation
  - Real-time transaction monitoring operational
  - SAR filing capability live

---

### Goal G-3: Reduce Operator Compliance Burden

**Derived From Drivers**: SD-3, SD-1

**Goal Owner**: Service Owner

**Goal Statement**: Achieve operator satisfaction score of 4/5 or above for the surrender process, with 90% of surrenders completed without helpdesk intervention, within the first compliance cycle.

**Success Metrics**:

- **Primary Metric**: 90% self-service surrender completion rate
- **Secondary Metrics**:
  - Operator satisfaction survey average 4/5+
  - Helpdesk call volume during surrender window reduced 50% vs EU ETS baseline

---

## Complete Traceability Matrix

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| UK ETS Authority | SD-1 | Robust compliance | G-1 | 100% surrender availability | O-1 | Reliable carbon market |
| UK ETS Authority | SD-1 | Robust compliance | G-2 | Financial crime controls | O-1 | Reliable carbon market |
| FCA | SD-2 | Market integrity | G-2 | Financial crime controls | O-1 | Reliable carbon market |
| Operators | SD-3 | Simple compliance | G-1 | 100% surrender availability | O-1 | Reliable carbon market |
| Operators | SD-3 | Simple compliance | G-3 | Reduce compliance burden | O-1 | Reliable carbon market |
| HM Treasury | SD-4 | Auction revenue | G-1 | 100% surrender availability | O-1 | Reliable carbon market |
| ICE Futures | SD-5 | Trading integration | G-1 | 100% surrender availability | O-1 | Reliable carbon market |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: FCA demands financial-grade KYC/AML for all accounts (SD-2) vs operators want simple, proportionate compliance process (SD-3)
  - **Resolution Strategy**: Tiered accounts — compliance-only accounts with simplified KYC; trading accounts with full financial-grade verification. Activity thresholds trigger KYC escalation.

- **Conflict 2**: ICE Futures needs predictable registry performance SLAs (SD-5) vs registry team needs maintenance windows for updates (implicit)
  - **Resolution Strategy**: Defined maintenance windows outside trading hours; zero-downtime deployment practices; DR capability enabling maintenance on secondary while primary serves traffic.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Scheme rules and cap levels | Carbon Markets Team | DESNZ Minister | UK ETS Authority, devolved admins | Industry |
| Registry technical architecture | Technical Lead | SRO | FCA, ICE, EA | Operators |
| KYC/AML policy | Compliance Lead | DESNZ SIRO | FCA, NCA | UK ETS Authority |
| Budget approval | Finance Director | Permanent Secretary | HM Treasury | CDDO |
| Auction integration | Technical Lead | SRO | ICE, HM Treasury | FCA |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Greenhouse Gas Emissions Trading Scheme Order 2020 | Legislation | legislation.gov.uk | UK ETS legal framework, registry requirements | N/A — external reference |
| UK ETS Authority guidance | Regulatory guidance | GOV.UK | Scheme rules, compliance obligations | N/A — external reference |
| FCA carbon markets supervision | Regulatory approach | FCA | Market integrity, MiFID classification | N/A — external reference |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: UK Emissions Trading Registry (Project 003)
**Model**: Claude Opus 4.6
