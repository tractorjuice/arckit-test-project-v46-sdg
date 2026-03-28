# Project Requirements: UK Emissions Trading Registry

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-003-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | UK Emissions Trading Registry (Project 003) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, UK ETS Registry |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | UK ETS Programme Board, DESNZ Digital, UK ETS Authority, FCA, ICE Futures Europe, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines requirements for the UK Emissions Trading Scheme Registry — the regulated digital system managing carbon allowance accounts, transaction processing, compliance tracking, and auction settlement for the UK's carbon trading scheme.

---

## Executive Summary

### Business Context

The UK Emissions Trading Scheme (UK ETS) replaced UK participation in the EU ETS following Brexit. Approximately 1,000 installations and aviation operators are obligated to monitor, report, and surrender carbon allowances equal to their verified emissions. The scheme operates a cap-and-trade mechanism with allowances auctioned by government (generating approximately GBP 5 billion annually) and traded on secondary markets through ICE Futures Europe. The registry is the authoritative record of allowance ownership and must meet both environmental compliance and financial regulatory standards.

### Objectives

- Operate a 99.95% available registry with zero downtime during the annual compliance surrender window
- Implement FCA-grade KYC/AML controls with tiered requirements proportionate to account type
- Process allowance transactions within the 26-hour settlement window mandated by legislation
- Integrate with ICE Futures Europe for auction settlement and clearing house operations
- Reduce operator compliance burden by 30% compared to EU ETS registry experience through improved UX

### Expected Outcomes

- 100% registry availability during 30 April surrender deadline (zero penalties attributable to registry downtime)
- FCA supervisory assessment passed without major findings
- 90% of compliance surrenders completed without helpdesk intervention
- Auction settlement processed automatically within contractual timescales (same-day T+0)
- Zero fraud incidents involving registry account compromise

### Project Scope

**In Scope**:

- Account management (opening, maintenance, closure for operators, traders, government accounts)
- Allowance lifecycle management (creation, allocation, auction, transfer, surrender, cancellation)
- Transaction processing with immutable audit trail
- Compliance tracking and automated penalty calculation
- KYC/AML verification and ongoing monitoring
- Auction settlement integration with ICE Futures Europe
- Verified emissions reporting integration
- Regulatory reporting for UK ETS Authority and FCA

**Out of Scope**:

- Emissions monitoring and verification (separate MRV system)
- Secondary market trading platform (ICE Futures Europe)
- Carbon offset/credit management (separate voluntary carbon market)
- EU ETS linkage technical implementation (policy decision pending)

---

## Business Requirements

### BR-001: Regulatory Compliant Registry Operations

**Description**: Operate a registry that meets all requirements of the Greenhouse Gas Emissions Trading Scheme Order 2020 and subsequent amendments.

**Rationale**: Legal obligation — non-compliance exposes DESNZ to judicial review and regulatory censure.

**Success Criteria**:

- All legislative registry requirements implemented and verified
- UK ETS Authority confirms regulatory compliance
- Annual compliance cycle (surrender, reconciliation, penalty) completed without regulatory incident

**Priority**: MUST_HAVE

---

### BR-002: Financial Crime Prevention

**Description**: Implement KYC, AML, sanctions screening, and market abuse detection controls that satisfy FCA supervisory expectations for a financial market infrastructure.

**Rationale**: UK ETS allowances are financial instruments under UK MiFID. EU ETS experienced EUR 5 billion VAT carousel fraud and multiple phishing attacks.

**Success Criteria**:

- FCA supervisory assessment passed without major findings
- All accounts KYC-verified before activation
- Real-time transaction monitoring operational with suspicious activity reporting
- Zero fraud incidents involving registry account compromise

**Priority**: MUST_HAVE

---

### BR-003: Operator Compliance Efficiency

**Description**: Enable obligated operators to complete annual compliance obligations (emissions reporting, allowance surrender) with minimum administrative burden.

**Rationale**: Operators are industrial companies whose primary business is not financial trading. Compliance should be simple and efficient.

**Success Criteria**:

- 90% of surrenders completed self-service without helpdesk intervention
- Operator satisfaction score 4/5+ for surrender process
- Compliance process completable within 1 working day for straightforward cases

**Priority**: MUST_HAVE

---

### BR-004: Reliable Auction Revenue

**Description**: Process auction settlement reliably, ensuring government auction revenue (approximately GBP 5 billion annually) is collected on schedule.

**Rationale**: Auction revenue is included in HM Treasury fiscal forecasts. Settlement failures have immediate fiscal consequences.

**Success Criteria**:

- 100% of auction settlements processed within contractual timescales
- Automated reconciliation with ICE clearing house
- Real-time revenue reporting to HM Treasury

**Priority**: MUST_HAVE

---

### BR-005: Four-Nation Regulatory Access

**Description**: Provide the four UK regulators (EA, SEPA, NRW, DAERA) with appropriate access to registry data for their respective jurisdictions, supporting compliance monitoring and enforcement.

**Rationale**: UK ETS is a UK-wide scheme with four regulators responsible for different geographic jurisdictions.

**Success Criteria**:

- Each regulator has access to data for operators within their jurisdiction
- Cross-jurisdiction data sharing governed by documented agreements
- Regulatory dashboards showing compliance status for their jurisdictions

**Priority**: MUST_HAVE

---

## Functional Requirements

### User Personas

#### Persona 1: Compliance Manager (Operator)

- **Role**: Environmental compliance manager at power station/refinery/manufacturing plant
- **Goals**: Submit verified emissions, surrender allowances, maintain account, meet 30 April deadline
- **Pain Points**: Complex EU ETS interface, unclear error messages, excessive KYC for simple compliance
- **Technical Proficiency**: Medium

#### Persona 2: Carbon Trader

- **Role**: Carbon market trader at bank/commodity house
- **Goals**: Transfer allowances, manage multiple accounts, execute trades rapidly
- **Pain Points**: Slow transaction processing, limited API access, no real-time balance visibility
- **Technical Proficiency**: High

#### Persona 3: UK ETS Authority Regulator

- **Role**: Compliance officer at Environment Agency/SEPA/NRW/DAERA
- **Goals**: Monitor compliance, identify non-surrender, initiate enforcement, produce regulatory reports
- **Pain Points**: Manual data extraction, limited cross-jurisdiction visibility
- **Technical Proficiency**: Medium

#### Persona 4: Auction Administrator (Government)

- **Role**: DESNZ auction programme manager
- **Goals**: Manage auction schedule, process settlement, report revenue to HM Treasury
- **Pain Points**: Manual settlement reconciliation, limited real-time visibility
- **Technical Proficiency**: Medium-High

---

### Functional Requirements Detail

#### FR-001: Account Management

**Description**: Manage registry accounts for operators, traders, government, and regulators with appropriate access controls and KYC verification.

**Relates To**: BR-001, BR-002

**Acceptance Criteria**:

- [ ] Given a new account application, when submitted with required KYC documentation, then the account is created within 5 working days
- [ ] Given account types (operator holding, trading, government holding, regulator), when created, then appropriate permissions and limits are applied
- [ ] Given a compliance-only operator account, when KYC is assessed, then simplified verification is applied (Companies House check, director identity)
- [ ] Given a trading account, when KYC is assessed, then full financial-grade verification is applied (PEP/sanctions, beneficial ownership, source of funds)

**Priority**: MUST_HAVE

---

#### FR-002: Allowance Transaction Processing

**Description**: Process allowance transfers between accounts with real-time balance validation, immutable audit trail, and 26-hour settlement window compliance.

**Relates To**: BR-001

**Acceptance Criteria**:

- [ ] Given a transfer request with valid sender balance, when initiated by an authorised user, then the transfer is executed within 26 hours
- [ ] Given a transfer request, when processed, then an immutable audit trail record is created
- [ ] Given insufficient balance, when a transfer is requested, then it is rejected with a clear error message
- [ ] Given a transfer, when processed, then real-time balance updates are reflected for both parties
- [ ] Given the transaction log, when queried, then all transactions are retrievable by account, date, type, and counterparty

**Priority**: MUST_HAVE

---

#### FR-003: Annual Compliance Surrender

**Description**: Enable operators to surrender allowances equal to their verified emissions by the 30 April deadline.

**Relates To**: BR-001, BR-003

**Acceptance Criteria**:

- [ ] Given verified emissions data, when loaded into the registry, then the required surrender quantity is displayed for each operator
- [ ] Given an operator with sufficient allowances, when surrender is initiated, then the process completes within 10 minutes
- [ ] Given surrender completion, when confirmed, then a compliance certificate is generated
- [ ] Given non-surrender by 30 April, when the deadline passes, then automatic penalty calculation is triggered
- [ ] Given the surrender window (1 March - 30 April), when in effect, then registry availability is 100%

**Priority**: MUST_HAVE

---

#### FR-004: KYC/AML Verification

**Description**: Implement tiered Know Your Customer and Anti-Money Laundering verification for all account holders.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given a new account application, when submitted, then automated Companies House and PEP/sanctions checks are performed
- [ ] Given a trading account, when onboarding, then beneficial ownership verification to 25% threshold is required
- [ ] Given all accounts, when active, then ongoing monitoring against sanctions lists is performed daily
- [ ] Given a sanctions match, when detected, then the account is immediately frozen and alert raised to compliance team
- [ ] Given suspicious transaction patterns, when detected by monitoring rules, then a SAR is prepared for NCA submission

**Priority**: MUST_HAVE

---

#### FR-005: Auction Settlement

**Description**: Process auction settlement with ICE Futures Europe, ensuring allowance delivery against payment within contractual timescales.

**Relates To**: BR-004

**Acceptance Criteria**:

- [ ] Given an auction result from ICE, when received, then allowances are allocated to winning bidders' registry accounts within T+0
- [ ] Given auction settlement, when processed, then revenue is confirmed and reported to HM Treasury
- [ ] Given a settlement failure, when detected, then automated retry is initiated with escalation after 3 attempts
- [ ] Given all auction settlements, when processed, then reconciliation with ICE clearing records is automated

**Priority**: MUST_HAVE

---

#### FR-006: Regulatory Dashboard

**Description**: Provide regulators with dashboards showing compliance status, transaction activity, and enforcement triggers for their jurisdiction.

**Relates To**: BR-005

**Acceptance Criteria**:

- [ ] Given a regulator login (EA/SEPA/NRW/DAERA), when authenticated, then only data for their jurisdiction is accessible
- [ ] Given the compliance dashboard, when accessed, then operators' surrender status against verified emissions is shown
- [ ] Given non-compliance, when detected after deadline, then enforcement recommendations with penalty calculations are generated
- [ ] Given the dashboard, when queried, then aggregated transaction statistics and anomaly flags are shown

**Priority**: MUST_HAVE

---

#### FR-007: Transaction Monitoring

**Description**: Real-time monitoring of all transactions for market abuse, fraud, and money laundering indicators.

**Relates To**: BR-002

**Acceptance Criteria**:

- [ ] Given all transactions, when processed, then they are screened against configurable risk rules
- [ ] Given unusual transaction patterns (velocity, value, counterparty), when detected, then alerts are raised
- [ ] Given a high-risk alert, when raised, then a compliance analyst review queue is populated
- [ ] Given a confirmed suspicious activity, when escalated, then SAR filing workflow is initiated

**Priority**: MUST_HAVE

---

## Non-Functional Requirements

### Performance Requirements

#### NFR-P-001: Transaction Processing Time

**Requirement**: Individual allowance transfers processed within 30 seconds. Batch surrenders (up to 1,000 operators) processed within 4 hours.

**Priority**: MUST_HAVE

#### NFR-P-002: Auction Settlement Throughput

**Requirement**: Process auction settlement for up to 50 winning bidders within 30 minutes of auction close.

**Priority**: MUST_HAVE

### Availability Requirements

#### NFR-A-001: General Availability

**Requirement**: 99.95% uptime (4.4 hours maximum downtime per year). Zero downtime during surrender window (1 March - 30 April).

**Priority**: MUST_HAVE

#### NFR-A-002: Disaster Recovery

**RPO**: 0 (zero data loss for transactions) | **RTO**: 15 minutes

**Priority**: MUST_HAVE

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: All users must authenticate via MFA. Operators and traders require hardware token or authenticator app. Regulatory staff require PIV/smart card or equivalent.

**Priority**: MUST_HAVE

#### NFR-SEC-002: Transaction Authorisation

**Requirement**: Transfers above configurable threshold (default GBP 100,000 equivalent) require dual authorisation (maker-checker pattern).

**Priority**: MUST_HAVE

#### NFR-SEC-003: Audit Trail

**Requirement**: Immutable, cryptographically signed audit trail for all transactions. Retained for minimum 7 years. Tamper-evident with independent verification capability.

**Priority**: MUST_HAVE

#### NFR-SEC-004: Penetration Testing

**Requirement**: Annual penetration testing by CHECK/CREST-certified provider. Critical and high findings remediated before go-live. Quarterly vulnerability scanning.

**Priority**: MUST_HAVE

### Compliance Requirements

#### NFR-C-001: Financial Regulation

**Requirement**: Comply with UK MiFID requirements for financial market infrastructure. FCA-supervisable with regulatory reporting capability.

**Priority**: MUST_HAVE

#### NFR-C-002: Data Protection

**Requirement**: UK GDPR compliant. DPIA completed. Personal data (account holder identity, beneficial owners) encrypted at rest. Data retention aligned with AML regulations (5 years post-account closure).

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-001: ICE Futures Europe

**Purpose**: Auction settlement, clearing house integration, and secondary market delivery.

**Integration Type**: Real-time API (FIX protocol and REST API)

**Data Exchanged**: Auction results, settlement instructions, delivery notifications, reconciliation

**SLA**: 99.99% API availability during trading hours; settlement within T+0

**Priority**: MUST_HAVE

### INT-002: Companies House

**Purpose**: KYC verification of corporate account holders.

**Integration Type**: REST API (real-time lookup)

**Data Exchanged**: Company registration, directors, significant persons of control

**Priority**: MUST_HAVE

### INT-003: PEP/Sanctions Databases

**Purpose**: Politically Exposed Persons and sanctions screening for all account holders.

**Integration Type**: REST API (real-time and batch screening)

**Data Exchanged**: Name matching against HMT sanctions list, global PEP databases

**Priority**: MUST_HAVE

### INT-004: National Crime Agency

**Purpose**: Suspicious Activity Report submission.

**Integration Type**: Secure file transfer (SAR Online)

**Data Exchanged**: Suspicious activity reports with supporting evidence

**Priority**: MUST_HAVE

### INT-005: HMRC

**Purpose**: VAT and tax reporting for auction revenue and trading activity.

**Integration Type**: Batch reporting (monthly)

**Data Exchanged**: Auction revenue, account holder tax identifiers

**Priority**: SHOULD_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Registry Account

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique account identifier |
| account_type | Enum | Yes | Operator_holding, trading, government, regulator |
| holder_name | String | Yes | Legal entity name |
| companies_house_number | String | No | UK company registration |
| jurisdiction | Enum | Yes | England, Scotland, Wales, NI |
| kyc_status | Enum | Yes | Pending, verified, enhanced, suspended |
| balance_allowances | Integer | Yes | Current allowance balance |
| created_date | DateTime | Yes | Account creation date |
| status | Enum | Yes | Active, suspended, closed |

#### Entity 2: Transaction

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| id | UUID | Yes | Unique transaction identifier |
| transaction_type | Enum | Yes | Transfer, surrender, auction_allocation, cancellation |
| from_account | UUID | Yes | Source account |
| to_account | UUID | Yes | Destination account |
| quantity | Integer | Yes | Number of allowances |
| timestamp | DateTime | Yes | Transaction timestamp (UTC) |
| status | Enum | Yes | Pending, completed, failed, reversed |
| authorised_by | UUID | Yes | User who authorised |
| audit_hash | String | Yes | Cryptographic hash for tamper detection |

**Data Volume**: Approximately 500,000 transactions per year; 5,000 accounts

---

## Approval

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| SRO, DESNZ | _________ | PENDING |
| UK ETS Authority Chair | _________ | PENDING |
| FCA Supervisor | _________ | PENDING |
| ICE Futures Europe Representative | _________ | PENDING |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GHG Emissions Trading Scheme Order 2020 | Legislation | legislation.gov.uk | Registry requirements | N/A |
| UK MiFID | Legislation | legislation.gov.uk | Financial instrument classification | N/A |
| FCA Market Abuse Regulation | Regulation | FCA | Market integrity requirements | N/A |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: UK Emissions Trading Registry (Project 003)
**Model**: Claude Opus 4.6
