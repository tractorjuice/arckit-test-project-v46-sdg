# Strategic Outline Business Case (SOBC): National Food Strategy Dashboard

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-005-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case |
| **Project** | National Food Strategy Dashboard (Project 005) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Senior Responsible Owner, Cabinet Office Food Strategy Unit |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Cabinet Office Finance, HM Treasury, DEFRA, DfE, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This SOBC sets out the strategic justification for the National Food Strategy Dashboard, following HM Treasury Green Book methodology and the Five Case Model.

---

## Executive Summary

**Purpose**: The National Food Strategy Dashboard will provide ministers, policy teams, and the public with a single authoritative view of UK food system performance, aggregating data from all four SDG 2 operational projects and wider published sources to track progress against the Government Food Strategy 2022.

**Problem Statement**: The Government Food Strategy 2022 committed to actions across multiple departments, but there is no unified way to track progress. Answering ministerial questions about food strategy delivery takes 3+ days of manual cross-departmental data gathering. The public has no accessible way to hold government to account on food policy commitments. This transparency gap undermines government accountability and wastes policy team time.

**Proposed Solution**: Build a cross-government data aggregation platform consuming APIs from Projects 001-004 and external sources, with an internal government dashboard for rapid ministerial briefing and a public GOV.UK dashboard for citizen transparency.

**Strategic Fit**: Directly delivers the Government Food Strategy 2022 commitment to transparency and accountability. Supports the Dimbleby Review recommendation for a Food System Data Programme. Aligns with the Open Government Partnership commitments.

**Investment Required**: £4.5M over 3 years

- Capital: £3.3M
- Operational (3 years): £1.2M

**Expected Benefits**: £12.5M over 5 years

- Policy team productivity: £5.0M (elimination of manual cross-departmental data gathering)
- FOI cost reduction: £1.5M (fewer requests when data is publicly available)
- Better policy targeting: £4.0M (evidence-based intervention enabled by real-time data)
- Cross-government coordination savings: £2.0M (shared data reduces duplicated analysis)

**Return on Investment**:

- NPV: £6.2M (discounted at 3.5%)
- Payback Period: 18 months
- ROI: 178%

**Recommended Option**: Option 2: Cross-Government Dashboard Platform

**Key Risks**:

1. Source project data feeds unavailable on schedule (dependency on Projects 001-004)
2. Ministerial pressure for premature public dashboard release before data quality is assured
3. ONS methodology review delays public dashboard launch

**Go/No-Go Recommendation**: **PROCEED**

**Rationale**: Low-cost, high-value investment that multiplies the impact of the four operational projects by providing cross-government visibility. The dashboard is the connective tissue of the SDG 2 programme. Without it, £71.5M invested in Projects 001-004 produces siloed departmental benefits without cross-government policy insight.

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**: Food strategy performance data is scattered across DEFRA, DfE, FSA, and WRAP publications with different frequencies, formats, and methodologies. Preparing a cross-departmental food strategy briefing requires 3+ days of analyst time contacting multiple departments. Parliamentary questions about food strategy progress are answered with incomplete, inconsistent data.

**Consequences of Inaction**:

- Ministerial embarrassment from slow or inaccurate food strategy responses
- £71.5M invested in Projects 001-004 produces siloed benefits without cross-government coordination value
- Public accountability gap as Government Food Strategy progress is unmeasured
- Parliamentary committees unable to effectively scrutinise food strategy delivery
- FOI burden continues to grow as public and media seek data through formal requests

### A1.2 Why Now?

- Government Food Strategy 2022 committed to transparency and accountability mechanisms
- Projects 001-004 beginning to produce operational data that needs aggregation
- Dimbleby Review follow-up scrutiny expected in Parliament during 2027-2028
- GOV.UK platform and API standards now mature enough for interactive dashboards
- Cross-government data sharing frameworks established through SDG 2 programme governance

---

# PART B: ECONOMIC CASE

## B2. Options Analysis

### Option 0: Do Nothing

**Costs** (3-year): £1.5M (continued manual cross-departmental data gathering)

**Benefits**: £0

**Consequence**: No cross-government food strategy visibility. £71.5M in source project investment produces siloed departmental outputs.

**Recommendation**: **Reject**

---

### Option 1: Manual Reporting and Static Publication

**Description**: Produce a quarterly PDF report on food strategy progress, compiled manually by the Food Strategy Unit from departmental submissions. Publish on GOV.UK as a static document.

**Costs** (3-year): £2.0M (analyst time, design, publication)

**Benefits** (5-year): £4.0M (some productivity gain, partial FOI reduction)

**Net Benefit**: £2.0M

**Pros**: Low investment, quick to start.

**Cons**: Still labour-intensive; static publication not interactive; 3-month reporting lag; no alerting capability; does not consume source project APIs.

**Stakeholder Goals Met**: 30%

**Recommendation**: **Reject** -- Does not solve the fundamental problem of slow, manual data gathering.

---

### Option 2: Cross-Government Dashboard Platform (RECOMMENDED)

**Description**: Build a data platform consuming APIs from Projects 001-004 and external sources, with internal interactive dashboard and public GOV.UK dashboard. Phased: internal dashboard first, public dashboard after ONS methodology review.

**Costs** (3-year): £4.5M

**Benefits** (5-year): £12.5M

**Net Benefit**: £8.0M

**NPV**: £6.2M

**Pros**:

- Automates cross-departmental data aggregation
- Interactive dashboards with drill-down
- Public accountability through GOV.UK publication
- Alerting for deteriorating indicators
- Multiplies value of £71.5M source project investment
- Reusable for other cross-government performance monitoring

**Cons**:

- Dependent on source project API delivery
- ONS methodology review required for public metrics
- Smaller standalone investment value without source projects

**Stakeholder Goals Met**: 95%

**Recommendation**: **PROCEED**

---

### Option 3: Commercial BI Platform

**Description**: Procure a commercial business intelligence platform (Power BI, Tableau Server) for government use, with custom data connectors to source projects.

**Costs** (3-year): £5.5M (licences + development)

**Benefits** (5-year): £10.0M

**Net Benefit**: £4.5M

**Cons**: Vendor lock-in; licence costs escalate; limited GOV.UK integration for public dashboard; accessibility concerns with commercial BI tools; does not meet GDS Service Standard for public-facing service.

**Recommendation**: **Reject** -- Higher cost, vendor lock-in, poor fit for citizen-facing GOV.UK publication.

---

## B3. Options Comparison

| Criterion | Option 0 | Option 1 | Option 2 (Recommended) | Option 3 |
|-----------|----------|----------|------------------------|----------|
| 3-Year TCO | £1.5M | £2.0M | £4.5M | £5.5M |
| 5-Year Benefits | £0 | £4.0M | £12.5M | £10.0M |
| NPV | -£1.5M | £1.5M | £6.2M | £3.2M |
| Goals Met | 0% | 30% | 95% | 65% |
| Briefing Speed | 3+ days | 1 day | < 5 minutes | < 15 minutes |
| Public Dashboard | No | Static PDF | Interactive GOV.UK | Limited |

---

# PART D: FINANCIAL CASE

## D1. Investment Profile

| Year | Capital | Operational | Total |
|------|---------|-------------|-------|
| Year 1 | £1.8M | £0.2M | £2.0M |
| Year 2 | £1.2M | £0.4M | £1.6M |
| Year 3 | £0.3M | £0.6M | £0.9M |
| **Total** | **£3.3M** | **£1.2M** | **£4.5M** |

## D2. Benefits Realisation

| Benefit | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|---------|--------|--------|--------|--------|--------|-------|
| Policy team productivity | £0 | £0.5M | £1.0M | £1.5M | £2.0M | £5.0M |
| FOI cost reduction | £0 | £0.1M | £0.3M | £0.5M | £0.6M | £1.5M |
| Better policy targeting | £0 | £0.3M | £0.7M | £1.2M | £1.8M | £4.0M |
| Coordination savings | £0 | £0.2M | £0.4M | £0.6M | £0.8M | £2.0M |
| **Total** | **£0** | **£1.1M** | **£2.4M** | **£3.8M** | **£5.2M** | **£12.5M** |

---

# PART E: MANAGEMENT CASE

## E1. Programme Governance

| Body | Chair | Frequency | Purpose |
|------|-------|-----------|---------|
| Dashboard Programme Board | SRO | Monthly | Strategy, risk, milestones |
| Cross-Programme Data Board | SRO + Source Project SROs | Quarterly | API specifications, data quality SLAs |
| ONS Methodology Board | Food Strategy Director + ONS | Quarterly | Statistical quality assurance |
| Public Dashboard Approval Board | Minister + Comms | Pre-publication | Publication sign-off |

## E2. Delivery Approach

| Phase | Duration | Deliverables | Investment |
|-------|----------|-------------|------------|
| Discovery | 3 months | KPI framework, API specifications, ONS engagement | £0.4M |
| Alpha | 3 months | Internal dashboard prototype, 2 source APIs connected | £0.8M |
| Private Beta (Internal) | 6 months | Full internal dashboard, all source APIs, alerting | £1.5M |
| Public Beta | 6 months | GOV.UK public dashboard, ONS-reviewed methodology | £1.0M |
| Live | Ongoing | Continuous improvement, new KPIs, Diet/Health expansion | £0.8M |

## E3. Key Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Source project API delays | HIGH | MEDIUM | Phased dashboard; use published statistics as interim |
| Premature public release pressure | MEDIUM | HIGH | Internal dashboard first; clear publication criteria; ministerial briefing on data readiness |
| ONS methodology delay | MEDIUM | MEDIUM | Early ONS engagement; parallel statistical and technical workstreams |
| GOV.UK platform limitations | LOW | MEDIUM | Early GDS engagement; progressive enhancement approach |
| Cross-departmental governance | MEDIUM | MEDIUM | SDG 2 Programme Board oversight; pre-agreed data sharing protocols |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Government Food Strategy 2022 | Policy | DEFRA/Cabinet Office | Transparency and accountability commitments | gov.uk |
| National Food Strategy 2021 | Review | Henry Dimbleby | Food System Data Programme recommendation | nationalfoodstrategy.org |
| UK Code of Practice for Statistics | Standard | UK Statistics Authority | Quality standards for public metrics | code.statisticsauthority.gov.uk |
| HM Treasury Green Book | Guidance | HMT | Five Case Model, NPV methodology | gov.uk |
| ARC-000-PRIN-v1.0 | Principles | SDG 2 | Governing architecture principles | ARC-000-PRIN-v1.0.md |
| ARC-005-STKE-v1.0 | Stakeholders | SDG 2 | Stakeholder drivers and goals | ARC-005-STKE-v1.0.md |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Food Strategy Dashboard
**Model**: Claude Opus 4.6
