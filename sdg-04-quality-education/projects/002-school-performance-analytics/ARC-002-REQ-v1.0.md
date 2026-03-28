# Project Requirements: School Performance Analytics

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-002-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | School Performance Analytics (Project 002) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, SPA Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SPA Programme Board, Ofsted Digital, DfE Analysis Directorate |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the requirements for the School Performance Analytics (SPA) platform. The platform will consolidate multiple education data sources into a unified analytical tool for Ofsted inspectors, DfE analysts, and school leaders, replacing the current fragmented landscape of IDSR, ASP, and manual data collation processes.

---

## Executive Summary

### Business Context

Ofsted inspectors currently spend an estimated 40% of their pre-inspection preparation time manually collating data from six or more separate systems. The School Performance Analytics platform will consolidate these data sources into a single dashboard, providing inspectors with a comprehensive, accurate, and timely view of school performance. Crucially, the same data view will be available to schools, ensuring transparency and supporting self-evaluation.

### Objectives

- Consolidate 6 data sources into a single analytical platform
- Reduce inspector pre-inspection data preparation time by 60%
- Provide schools with transparent access to the same data Ofsted uses
- Maintain 99.5% data accuracy against source systems
- Replace legacy IDSR and ASP systems within 24 months

### Expected Outcomes

- 4 hours saved per inspection preparation x 6,500 inspections/year = 26,000 hours saved annually
- Improved inspection consistency through standardised data presentation
- Reduced FOI requests as schools can access their own data directly
- GBP 2.1M annual saving from decommissioning 3 legacy analytical systems

### Project Scope

**In Scope**:

- Unified data dashboard for Ofsted inspectors (pre-inspection data pack)
- School-facing self-evaluation dashboard (same data, school's own view)
- Data pipelines from NPD, school census, attendance, exclusions, exam results, financial benchmarking
- Risk indicators for inspection targeting (transparent methodology)
- DfE Sign-in for school access; Ofsted internal SSO for inspectors
- Regional Director performance overview dashboards

**Out of Scope**:

- Inspection report writing tools (separate Ofsted system)
- Parent-facing school comparison tools (covered by separate Find and Compare Schools)
- Real-time safeguarding data (separate referral systems)
- Post-16 / FE provider analytics (Phase 2)

---

## Business Requirements

### BR-1: Unified Pre-Inspection Data Dashboard

**Description**: Provide Ofsted inspectors with a single dashboard consolidating all school performance data required for pre-inspection preparation.

**Rationale**: Inspectors currently access 6+ systems manually. Consolidation saves time and reduces errors.

**Success Criteria**:

- All data needed for Section 5 and Section 8 inspection preparation available in one dashboard
- Inspector preparation time reduced from 7 hours to 3 hours
- 90% of inspectors rate the dashboard as "better" or "much better" than current tools

**Priority**: MUST_HAVE
**Stakeholder**: HM Chief Inspector (SD-1), Lead Inspectors (SD-2)

---

### BR-2: School Self-Evaluation Dashboard

**Description**: Provide headteachers and school leaders with access to the same data dashboard that inspectors use, enabling transparent, data-informed self-evaluation.

**Rationale**: Transparency addresses sector concerns about "secret data" and supports school improvement.

**Success Criteria**:

- 80% of schools access their dashboard at least once per term
- Dashboard accessible within 24 hours of source data update
- FOI requests for inspection data reduced by 50%

**Priority**: MUST_HAVE
**Stakeholder**: Headteachers (SD-4), Teaching Unions (SD-5)

---

### BR-3: Data Quality Assurance

**Description**: Maintain 99.5% data accuracy against source systems through automated reconciliation and quality monitoring.

**Rationale**: Incorrect data in inspection preparation can lead to unfair judgements and erode trust.

**Success Criteria**:

- Automated daily reconciliation against all source systems
- Data discrepancies flagged and resolved within 24 hours
- Zero instances of inspection judgements based on incorrect data

**Priority**: MUST_HAVE
**Stakeholder**: HM Chief Inspector (SD-1), DfE Analysis Directorate (SD-3)

---

### BR-4: Consolidate Legacy Analytics Systems

**Description**: Replace IDSR, ASP, and bespoke analytical tools with the unified SPA platform within 24 months.

**Rationale**: Multiple overlapping systems create maintenance overhead, data inconsistency, and user confusion.

**Success Criteria**:

- IDSR decommissioned within 18 months
- ASP decommissioned or integrated within 24 months
- GBP 2.1M annual saving from legacy decommissioning

**Priority**: SHOULD_HAVE
**Stakeholder**: DfE Analysis Directorate (SD-3), Ofsted COO

---

### BR-5: Risk-Based Inspection Targeting Support

**Description**: Provide risk indicators that support — but do not determine — inspection targeting decisions, with transparent methodology.

**Rationale**: Risk-based targeting enables Ofsted to prioritise inspections where they are most needed. However, the methodology must be transparent and the final decision must involve professional judgement.

**Success Criteria**:

- Risk indicators based on objective data (attainment trends, attendance, exclusions, complaints)
- Methodology published and accessible to schools
- Final targeting decisions documented with rationale (not automated)
- No individual teacher data used in risk indicators

**Priority**: SHOULD_HAVE
**Stakeholder**: HM Chief Inspector (SD-1), Headteachers (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: Claire — Ofsted Lead Inspector (HMI)

- **Role**: His Majesty's Inspector, leads Section 5 inspections
- **Goals**: Quickly access comprehensive school data; identify key lines of enquiry; prepare focused inspection
- **Pain Points**: Currently spends 7 hours collating data from 6 systems; data sometimes inconsistent between sources; no single view of trends
- **Technical Proficiency**: Medium (comfortable with spreadsheets, not coding)

#### Persona 2: James — Secondary School Headteacher

- **Goals**: Understand what data Ofsted will see; use same data for self-evaluation; prepare staff for inspection
- **Pain Points**: Cannot access IDSR in same format as inspectors; ASP data often months out of date; governors ask for data he cannot easily produce
- **Technical Proficiency**: Medium

#### Persona 3: Dr. Okonkwo — DfE Senior Analyst

- **Goals**: Conduct national-level analysis of school performance trends; produce statistical publications; provide data to ministers
- **Pain Points**: Multiple data stores with inconsistent schemas; significant time spent on data wrangling; limited self-service analytical capability
- **Technical Proficiency**: High (R, Python, SQL)

---

### Functional Requirements Detail

#### FR-1: Consolidated School Profile Dashboard

**Description**: Display a comprehensive school profile combining data from all integrated sources in a single dashboard view.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given an inspector accesses a school profile, when the dashboard loads, then it displays attainment, progress, attendance, exclusions, finance, and workforce data in a single view
- [ ] Given data is available from the source system, when the dashboard is accessed, then data is no more than 24 hours old
- [ ] Given a school's data changes in a source system, when reconciliation runs, then the dashboard reflects the updated data within 24 hours
- [ ] Edge case: When a source system is unavailable, the dashboard displays last-known data with a "stale data" indicator

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-2: Trend Analysis and Comparators

**Description**: Display multi-year trend data for key performance indicators with national, regional, and similar-school comparator groups.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given an inspector views a school's attainment data, when they select trend view, then 5 years of historical data is displayed
- [ ] Given a school is viewed, when comparators are shown, then national average, regional average, and statistical neighbour benchmarks are displayed
- [ ] Given a metric shows significant deviation from comparators, when viewed, then it is visually highlighted with contextual explanation

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-3: Pre-Inspection Data Pack Generation

**Description**: Generate a downloadable pre-inspection data pack containing all key performance data for a specific school, formatted for inspector use.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an inspector initiates a data pack, when it generates, then a PDF/Excel document is produced within 30 seconds
- [ ] Given a data pack is generated, when reviewed, then it contains standardised sections aligned to the Education Inspection Framework
- [ ] Given a school has missing data elements, when the pack generates, then missing elements are clearly flagged rather than silently omitted

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-4: School-Facing Self-Evaluation View

**Description**: Provide schools with access to their own data through the same dashboard interface that inspectors use, with appropriate access controls.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a headteacher authenticates via DfE Sign-in, when they access the platform, then they see only their own school's data
- [ ] Given a MAT CEO authenticates, when they access the platform, then they can view all schools in their trust
- [ ] Given a school views their dashboard, when comparing to the inspector view, then the data is identical (no hidden inspection-only metrics)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-5: Risk Indicator Framework

**Description**: Calculate and display risk indicators based on objective data to support inspection targeting decisions.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given risk indicators are calculated, when viewed by a Regional Director, then each indicator shows the methodology and source data
- [ ] Given a school's risk indicators change, when reviewed, then the system logs the change with timestamp and data values
- [ ] Given risk indicators are displayed, when a targeting decision is made, then the decision and rationale must be manually recorded (no automated triggering)

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

#### FR-6: Data Pipeline Monitoring

**Description**: Provide operational monitoring of all data pipelines, including data freshness, quality metrics, and reconciliation status.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a data pipeline runs, when it completes, then a quality report is generated showing accuracy, completeness, and timeliness metrics
- [ ] Given data accuracy falls below 99.5%, when detected, then an alert is raised to the data operations team
- [ ] Given a source system feed fails, when the pipeline detects the failure, then it retries with exponential backoff and alerts after 3 failures

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-7: Statistical Neighbour Calculation

**Description**: Calculate statistical neighbour groups for each school based on demographic and contextual characteristics, enabling fair comparison.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a school is viewed, when statistical neighbours are calculated, then the algorithm uses FSM rate, EAL proportion, prior attainment, and deprivation index
- [ ] Given the methodology is queried, when a user accesses the documentation, then the full statistical methodology is published and accessible

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-8: Cohort-Level Pupil Group Analysis

**Description**: Enable drill-down into performance data by pupil groups (FSM, SEND, EAL, gender, ethnicity) at cohort level, without individual pupil identification.

**Relates To**: BR-1

**Acceptance Criteria**:

- [ ] Given an inspector views attainment data, when they filter by FSM eligibility, then cohort-level metrics (averages, distributions) are displayed
- [ ] Given a pupil group has fewer than 10 pupils, when data is displayed, then it is suppressed to prevent individual identification
- [ ] Given data is displayed by ethnicity, when the group size is small, then groups are aggregated to maintain statistical confidentiality

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-9: Analytical Workspace (DfE Analysts)

**Description**: Provide DfE analysts with a self-service analytical workspace enabling SQL queries, R/Python notebooks, and data visualisation against the unified data store.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a DfE analyst accesses the workspace, when they write a SQL query, then it executes against the unified data store and returns results within 30 seconds
- [ ] Given an analyst creates a visualisation, when they save it, then it is stored in their workspace and shareable with colleagues
- [ ] Given pupil-level data is queried, when results are exported, then statistical disclosure control is automatically applied

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

#### FR-10: Audit Trail

**Description**: Maintain comprehensive audit logs of all data access, dashboard views, data pack downloads, and risk indicator reviews.

**Relates To**: BR-3 (data governance)

**Acceptance Criteria**:

- [ ] Given any user accesses a school's data, when the access occurs, then an audit record is created (who, what, when, from where)
- [ ] Given audit logs are reviewed, when queried, then they are searchable by user, school, date range, and action type
- [ ] Given audit logs exist, when retention policy applies, then logs are retained for 7 years (aligned with Ofsted record retention)

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

## Non-Functional Requirements

### NFR-P-1: Dashboard Load Time

**Requirement**: School profile dashboards must load within 3 seconds at the 95th percentile, including data from all integrated sources.

**Load Conditions**: Peak: 2,000 concurrent users (inspection season); Normal: 500 concurrent users
**Priority**: HIGH

---

### NFR-A-1: Availability

**Requirement**: 99.9% availability during term time. Enhanced availability (99.99%) during Ofsted inspection windows (September-July). Maintenance windows permitted during August.

**Priority**: HIGH

---

### NFR-SEC-1: Data Classification and Access Control

**Requirement**: Role-based access control with data classification enforcement. Inspectors see all schools in their region; headteachers see only their school; MAT CEOs see their trust schools; DfE analysts see aggregated/anonymised data unless specific DPIA authorisation for pupil-level access.

**Priority**: CRITICAL

---

### NFR-SEC-2: Statistical Disclosure Control

**Requirement**: Automatic suppression of data where pupil group sizes are below statistical disclosure thresholds (typically n<10 for pupil-level aggregations, n<3 for sensitive characteristics).

**Priority**: CRITICAL

---

### NFR-C-1: Ofsted-DfE Data Sharing Agreement Compliance

**Requirement**: All data sharing between Ofsted and DfE must comply with the existing data sharing agreement, with data processed only for purposes specified in the agreement.

**Priority**: CRITICAL

---

### NFR-U-1: WCAG 2.2 Level AA

**Requirement**: All user-facing dashboards must meet WCAG 2.2 Level AA, including data visualisations (charts, graphs must have accessible alternatives).

**Priority**: HIGH

---

## Integration Requirements

### INT-1: National Pupil Database (NPD)

**Purpose**: Pupil-level attainment and characteristics data — the primary source for school performance analysis.

**Integration Type**: Batch data pipeline (updated termly with provisional/final results cycles)
**Data Exchanged**: Pupil-level attainment (KS1, KS2, KS4, KS5), pupil characteristics (FSM, SEND, EAL, ethnicity, gender, prior attainment)
**Authentication**: DfE internal network, service account authentication
**SLA**: Data available within 48 hours of NPD publication
**Priority**: CRITICAL

---

### INT-2: School Census

**Purpose**: School-level and pupil-level data on school composition, workforce, and characteristics.

**Integration Type**: Batch data pipeline (3 census collections per year: autumn, spring, summer)
**Data Exchanged**: School workforce data, class sizes, pupil numbers by year group, FSM eligibility, SEND provision, absence data
**Priority**: CRITICAL

---

### INT-3: Get Information About Schools (GIAS)

**Purpose**: Authoritative school establishment data.

**Integration Type**: Daily batch synchronisation
**Data Exchanged**: School name, URN, UKPRN, address, phase, type, MAT membership, governance, Ofsted rating
**Priority**: MUST_HAVE

---

### INT-4: DfE Sign-in

**Purpose**: Authentication for school users (headteachers, MAT CEOs, school governors).

**Integration Type**: Real-time (SAML 2.0 / OpenID Connect)
**Priority**: MUST_HAVE

---

### INT-5: School Financial Benchmarking Data

**Purpose**: Per-pupil expenditure and financial health indicators for contextual analysis.

**Integration Type**: Annual batch data pipeline
**Data Exchanged**: Income, expenditure by category, per-pupil cost, financial health indicators
**Priority**: SHOULD_HAVE

---

## Data Requirements

### DR-1: School Performance Record

**Description**: Consolidated school-level performance data combining all source feeds.

**Key Attributes**: URN, school name, phase, type, MAT, region, KS2 attainment (RWM combined), KS4 attainment (Attainment 8, Progress 8), attendance rate, persistent absence rate, exclusion rate (fixed-term, permanent), Ofsted rating, inspection date, FSM rate, SEND rate, EAL rate, pupil numbers

**Data Classification**: OFFICIAL
**Data Retention**: 10 years for trend analysis
**Data Volume**: 22,000 school records updated termly

---

### DR-2: Pupil-Level Analytical Dataset

**Description**: Pseudonymised pupil-level data for cohort analysis and statistical neighbour calculation.

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: 7 years aligned with NPD retention
**Data Volume**: 8 million pupil records per cohort
**Access**: DfE analysts only, under specific DPIA authorisation

---

### DR-3: Risk Indicator Dataset

**Description**: Calculated risk indicators per school for inspection targeting support.

**Data Classification**: OFFICIAL-SENSITIVE (inspection sensitive)
**Data Retention**: 5 years for trend analysis
**Access**: Ofsted Regional Directors and targeting team only; schools can see their own indicators

---

## Success Criteria and KPIs

| Metric | Baseline | Target | Timeline | Measurement |
|--------|----------|--------|----------|-------------|
| Inspector prep time | 7 hours | 3 hours | 12 months post-launch | Inspector time tracking |
| Data accuracy | 97% (estimated) | 99.5% | At launch | Automated reconciliation |
| School dashboard adoption | 0% | 80% termly access | 18 months | Platform analytics |
| Legacy systems decommissioned | 0 | 3 | 24 months | IT asset register |
| Inspector satisfaction | N/A | 85% positive | 12 months | Inspector survey |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| ASP | Analyse School Performance (DfE tool, legacy) |
| EIF | Education Inspection Framework |
| IDSR | Inspection Data Summary Report |
| NPD | National Pupil Database |
| Progress 8 | Secondary school value-added measure |
| Statistical Neighbour | Schools with similar demographic characteristics |
| URN | Unique Reference Number (school identifier) |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: School Performance Analytics
**Model**: Claude Opus 4.6
