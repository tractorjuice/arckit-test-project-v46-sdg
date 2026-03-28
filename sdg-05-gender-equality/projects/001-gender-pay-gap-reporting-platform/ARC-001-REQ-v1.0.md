# Project Requirements: Gender Pay Gap Reporting Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | Gender Pay Gap Reporting Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Gender Pay Gap Reporting Programme, GEO |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GEO Programme Board, CDDO, EHRC Enforcement Team, HMRC RTI |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the business, functional, non-functional, integration, and data requirements for the Gender Pay Gap Reporting Platform. It provides the basis for solution design, vendor procurement, and acceptance testing. Requirements are traceable to stakeholder drivers documented in ARC-001-STKE-v1.0 and governed by principles in ARC-000-PRIN-v1.0.

---

## Executive Summary

### Business Context

The Equality Act 2010 (Section 78), as enacted through the Equality Act 2010 (Specific Duties and Public Authorities) Regulations 2017, requires all employers with 250 or more employees to publish gender pay gap data annually by 4 April. The current GOV.UK service provides a basic submission and publication mechanism but lacks automated validation, HMRC data integration, and analytical capability. Approximately 10% of eligible employers fail to report by the deadline, submitted data contains frequent calculation errors, and GEO statisticians spend considerable effort on post-submission data cleaning.

The Gender Pay Gap Reporting Platform will replace the existing service with an automated collection and analytics platform that improves data quality through HMRC RTI pre-population and automated validation, reduces employer reporting burden by 60%, and enables rich analytics for policy development.

### Objectives

- Achieve 100% employer compliance with statutory reporting obligations by 4 April annually
- Reduce average employer reporting effort from 40 staff-hours to 16 staff-hours (60% reduction)
- Improve data quality to National Statistics standard with 95% first-submission validation pass rate
- Deliver self-service analytics for GEO, EHRC, and the public with open data APIs
- Provide EHRC with automated compliance monitoring dashboards

### Expected Outcomes

- 100% eligible employer compliance rate (up from ~90%)
- 60% reduction in employer reporting time (40 hours to 16 hours)
- 95% of submissions pass automated validation on first or second attempt (up from ~30%)
- Code of Practice for Statistics designation for annual pay gap publication within 24 months
- 50+ open data API consumers within 12 months of launch

### Project Scope

**In Scope**:

- Employer submission portal with pre-populated HMRC RTI data
- Automated gender pay gap calculation engine
- Data validation and quality assurance at point of submission
- EHRC compliance monitoring dashboard
- Public-facing analytics dashboard and open data APIs
- Employer accounts with submission history and year-on-year comparison
- Contextual guidance integrated into the reporting journey
- API for programmatic submission from employer payroll systems

**Out of Scope**:

- Ethnicity pay gap reporting (future phase, dependent on legislative change)
- Mandatory employer action plans (future phase, requires legislation)
- Employer pay gap reduction advisory services
- Changes to the Equality Act 2010 calculation methodology

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| Minister for Women and Equalities | Ministerial sponsor | GEO | Strategic direction |
| SRO, Pay Gap Reporting | Programme accountability | GEO | Decision maker |
| GEO Head of Pay Gap Policy | Policy ownership | GEO | Requirements definition |
| GEO Digital Lead | Technical delivery | GEO | Technical oversight |
| GEO Head of Statistics | Analytical requirements | GEO | Data quality assurance |
| EHRC Enforcement Team | Enforcement data needs | EHRC | Compliance requirements |
| HMRC RTI Team | Data source integration | HMRC | Integration partner |
| SIRO | Information risk | GEO | Security review |
| Employer representatives | Reporting obligations | CBI, FSB | User acceptance |

---

## Business Requirements

### BR-1: Statutory Compliance Enablement

**Description**: The platform must enable all eligible employers (250+ employees) to fulfil their statutory obligation under the Equality Act 2010 to report gender pay gap data by the annual deadline of 4 April.

**Rationale**: Statutory obligation under the Equality Act 2010 (Section 78). Non-compliance exposes employers to EHRC enforcement action and the government to criticism about the integrity of the reporting regime.

**Success Criteria**:

- 100% of eligible employers can submit data through the platform
- Platform available and performant during the entire reporting window (January-April)
- Submission confirmation provides legal evidence of compliance

**Priority**: MUST_HAVE

**Stakeholder**: Minister, EHRC, employers

---

### BR-2: Employer Reporting Burden Reduction

**Description**: The platform must significantly reduce the time and effort employers spend on gender pay gap reporting through automation, pre-population, and integrated guidance.

**Rationale**: Employer burden is the primary barrier to compliance and data quality. Reducing burden improves compliance rates, reduces errors, and builds goodwill for any future expansion of reporting requirements.

**Success Criteria**:

- Average reporting time reduced from 40 hours to 16 hours (60% reduction)
- 80% of data fields pre-populated from HMRC RTI for employers who opt in
- Built-in calculation engine eliminates manual spreadsheet calculations

**Priority**: MUST_HAVE

**Stakeholder**: Employers (CBI, FSB), HMRC

---

### BR-3: Data Quality Assurance

**Description**: The platform must ensure that published gender pay gap data is accurate, complete, and of sufficient quality for National Statistics designation, through automated validation at point of submission.

**Rationale**: Data quality underpins the policy value of the entire reporting regime. Currently, ~70% of submissions require some form of correction, undermining statistical credibility.

**Success Criteria**:

- 95% of submissions pass automated validation on first or second attempt
- Zero calculation errors in published data
- Code of Practice for Statistics assessment passed within 24 months

**Priority**: MUST_HAVE

**Stakeholder**: GEO Statisticians, Minister, ONS

---

### BR-4: EHRC Compliance Monitoring

**Description**: The platform must provide EHRC with automated compliance monitoring capability, enabling identification of non-compliant employers and supporting enforcement proceedings.

**Rationale**: EHRC's enforcement role requires timely, accurate data on employer compliance. Current manual processes are resource-intensive and delay enforcement action.

**Success Criteria**:

- Real-time compliance dashboard showing submitted/not-submitted status for all eligible employers
- Automated alerts when the reporting deadline passes for non-compliant employers
- Data export capability for EHRC enforcement case management

**Priority**: MUST_HAVE

**Stakeholder**: EHRC Enforcement Team

---

### BR-5: Public Transparency and Accountability

**Description**: The platform must publish employer gender pay gap data in accessible, comparable, and analysable formats, enabling employees, unions, and the public to scrutinise employer performance.

**Rationale**: Public transparency is the primary accountability mechanism of the reporting regime. The TUC and Fawcett Society have consistently advocated for richer, more accessible data publication.

**Success Criteria**:

- All employer data published within 48 hours of the reporting deadline
- Searchable, filterable public dashboard by sector, region, and employer size
- Open data API available for independent analysis

**Priority**: MUST_HAVE

**Stakeholder**: TUC, Fawcett Society, employees/citizens

---

### BR-6: Policy Analytics Capability

**Description**: The platform must provide GEO with analytical tools to identify sectoral and regional pay gap trends, track progress over time, and generate evidence for policy development.

**Rationale**: Without analytical capability, pay gap data is a compliance exercise rather than a policy tool. The Minister needs trend data to demonstrate progress and inform policy interventions.

**Success Criteria**:

- Year-on-year trend analysis at sector, region, and employer-size levels
- Intersectional analysis capability (gender x sector x region)
- Automated generation of annual statistical publication data

**Priority**: SHOULD_HAVE

**Stakeholder**: GEO Statisticians, Minister, GEO Head of Policy

---

### BR-7: Future Extensibility

**Description**: The platform architecture must accommodate future expansion of reporting requirements (ethnicity pay gap, disability pay gap, mandatory action plans) without fundamental re-architecture.

**Rationale**: The government has consulted on ethnicity pay gap reporting and mandatory action plans. The platform must be designed to accommodate these future requirements to avoid costly re-builds.

**Success Criteria**:

- Data model supports additional pay gap dimensions (ethnicity, disability) without schema redesign
- Workflow engine supports configurable reporting requirements
- API design supports versioning for future data fields

**Priority**: SHOULD_HAVE

**Stakeholder**: Minister, GEO Head of Policy

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — HR Director at a Large Employer

- **Role**: HR Director at a FTSE 250 company, 5,000 employees
- **Goals**: Complete pay gap reporting accurately and efficiently to meet legal obligation; understand the company's pay gap to inform diversity strategy
- **Pain Points**: Current manual calculation process is error-prone and time-consuming; difficulty identifying which employees to include/exclude; no year-on-year comparison
- **Technical Proficiency**: Medium

#### Persona 2: James — Payroll Manager at an SME

- **Role**: Payroll manager at a mid-sized company, 300 employees, recently crossed the 250 threshold
- **Goals**: Understand what is required; complete submission with minimal effort; avoid errors that could trigger EHRC attention
- **Pain Points**: First-time reporter with no institutional knowledge; limited understanding of the complex calculation methodology; no dedicated HR analytics capability
- **Technical Proficiency**: Low-Medium

#### Persona 3: Dr. Amara — GEO Statistician

- **Role**: Senior statistician at GEO responsible for the annual pay gap statistical release
- **Goals**: Access clean, validated data for analysis; produce National Statistics-quality publications; identify data quality issues early
- **Pain Points**: Spends 40% of time cleaning submitted data; no integrated analytical tools; data exports lose context
- **Technical Proficiency**: High

#### Persona 4: Rebecca — EHRC Enforcement Officer

- **Role**: Enforcement officer responsible for identifying and pursuing non-compliant employers
- **Goals**: Quickly identify employers who have not submitted; access submission data for enforcement proceedings; track enforcement case outcomes
- **Pain Points**: Manual cross-referencing of submissions against eligible employers; no real-time compliance visibility; limited data for enforcement cases
- **Technical Proficiency**: Medium

---

### Use Cases

#### UC-1: Employer Submits Gender Pay Gap Data (Pre-Populated)

**Actor**: Sarah (HR Director)

**Preconditions**:

- Employer has an active account on the platform
- HMRC RTI data sharing consent is in place
- Employer's snapshot date has passed (5 April)

**Main Flow**:

1. Sarah logs into the platform using her employer account
2. System displays pre-populated pay data from HMRC RTI for the snapshot date
3. Sarah reviews the pre-populated data and makes corrections where needed
4. System calculates gender pay gap metrics using the Equality Act methodology
5. Sarah reviews the calculated metrics with explanatory guidance
6. Sarah adds optional narrative commentary
7. Sarah confirms and submits the report
8. System validates the submission and provides confirmation with reference number
9. System queues the submission for publication

**Postconditions**:

- Submission recorded with timestamp for compliance evidence
- Data queued for publication on the public dashboard
- EHRC compliance dashboard updated to show employer as compliant

**Alternative Flows**:

- **Alt 3a**: If Sarah disagrees with pre-populated data, she can override with manual data entry and provide a reason
- **Alt 8a**: If validation fails, system displays specific errors with guidance on correction

---

#### UC-2: First-Time Employer Registration and Submission

**Actor**: James (Payroll Manager)

**Preconditions**:

- Employer has crossed the 250-employee threshold
- Employer does not have an existing account

**Main Flow**:

1. James navigates to the platform and selects "Register as a new employer"
2. System validates employer against Companies House register
3. James verifies employer identity and creates an account
4. System presents a step-by-step guided journey for first-time reporters
5. James enters or confirms employee data (with optional HMRC pre-population)
6. System calculates metrics with detailed explanations at each step
7. James reviews, confirms, and submits
8. System validates and confirms submission

**Priority**: CRITICAL

---

### Functional Requirements Detail

#### FR-1: HMRC RTI Data Pre-Population

**Description**: The system must pre-populate employer pay data from HMRC Real Time Information for the relevant snapshot date, mapping RTI payroll data to the gender pay gap calculation fields.

**Relates To**: BR-2, UC-1

**Acceptance Criteria**:

- [ ] Given an employer with HMRC RTI consent, when they begin a submission, then pay data is pre-populated from RTI for the snapshot date
- [ ] Given pre-populated data, when the employer reviews it, then they can override any field with manual entry and a reason
- [ ] Given RTI data that cannot be mapped to a required field, then the field is flagged for manual completion with guidance

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: HMRC data sharing agreement; RTI API specification

---

#### FR-2: Gender Pay Gap Calculation Engine

**Description**: The system must implement the full gender pay gap calculation methodology as defined in the Equality Act 2010 (Specific Duties and Public Authorities) Regulations 2017, including mean and median hourly pay gap, mean and median bonus pay gap, proportion receiving bonuses, and quartile pay band distribution.

**Relates To**: BR-1, BR-3

**Acceptance Criteria**:

- [ ] Given employee pay data, when calculated, then mean hourly pay gap matches the Equality Act methodology
- [ ] Given employee pay data, when calculated, then median hourly pay gap is correct
- [ ] Given bonus data, when calculated, then mean and median bonus gaps are correct
- [ ] Given employee data, when calculated, then quartile pay bands are correctly distributed
- [ ] Edge case: Part-time workers' hourly rates calculated correctly per ACAS guidance
- [ ] Edge case: Employees on leave during the snapshot period handled per GEO guidance

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-3: Automated Data Validation

**Description**: The system must validate submitted data against defined quality rules, flagging errors and warnings before submission is accepted.

**Relates To**: BR-3

**Acceptance Criteria**:

- [ ] Given a submission with calculation errors, then system identifies specific errors with correction guidance
- [ ] Given a pay gap exceeding statistical norms for the sector, then system flags a warning (not a block)
- [ ] Given missing required fields, then system prevents submission until completed
- [ ] Given a submission that passes validation, then it is accepted and queued for publication

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-4: Employer Account Management

**Description**: The system must provide employer accounts with role-based access, submission history, and year-on-year comparison.

**Relates To**: BR-1, BR-2

**Acceptance Criteria**:

- [ ] Given a registered employer, then they can view all previous submissions
- [ ] Given multiple submissions across years, then year-on-year comparison is displayed
- [ ] Given an employer account, then multiple users can be authorised with different roles (submitter, approver, viewer)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-5: EHRC Compliance Dashboard

**Description**: The system must provide EHRC with a real-time dashboard showing compliance status for all eligible employers, with filtering, search, and enforcement case export.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given the reporting deadline, then EHRC can see which employers have/have not submitted
- [ ] Given a non-compliant employer, then EHRC can export relevant data for enforcement proceedings
- [ ] Given compliance data, then dashboard shows trends (year-on-year compliance improvement)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-6: Public Analytics Dashboard

**Description**: The system must provide a public-facing dashboard enabling citizens, employers, unions, and media to search, filter, and compare employer pay gap data.

**Relates To**: BR-5

**Acceptance Criteria**:

- [ ] Given published data, then users can search by employer name, sector, region, and size
- [ ] Given search results, then users can sort and filter by pay gap magnitude
- [ ] Given an employer, then users can view year-on-year trend for that employer
- [ ] Given aggregate data, then users can view sectoral and regional averages

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-7: Open Data API

**Description**: The system must provide a versioned RESTful API enabling programmatic access to published pay gap data for independent analysis, research, and journalism.

**Relates To**: BR-5, BR-6

**Acceptance Criteria**:

- [ ] Given a registered API consumer, then they can query published data by employer, sector, region, year
- [ ] Given the API, then it supports pagination, filtering, and bulk download
- [ ] Given API versioning, then existing consumers are not broken by new data fields

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-8: Submission API for Payroll Systems

**Description**: The system must provide an API enabling employers to submit pay gap data programmatically from their payroll systems, reducing manual data entry for large employers with automated payroll.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given a registered API client, then employers can submit data via authenticated API call
- [ ] Given an API submission, then the same validation rules apply as the web portal
- [ ] Given an API submission, then confirmation and reference number are returned

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-9: Contextual Guidance Engine

**Description**: The system must provide contextual guidance at each step of the reporting journey, explaining the calculation methodology, common pitfalls, and regulatory requirements in plain language.

**Relates To**: BR-2

**Acceptance Criteria**:

- [ ] Given each step of the submission flow, then relevant guidance is displayed inline
- [ ] Given a complex calculation step (e.g., part-time hourly rate), then worked examples are provided
- [ ] Given guidance content, then it is maintained as structured content separate from application code

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

#### FR-10: Statistical Reporting Engine

**Description**: The system must generate automated statistical reports for GEO publication, including aggregate pay gap statistics by sector, region, employer size, and year.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given validated submission data, then aggregate statistics are computed automatically
- [ ] Given aggregate statistics, then statistical disclosure control rules are applied (minimum cell size of 5)
- [ ] Given computed statistics, then output is formatted for National Statistics publication

**Priority**: SHOULD_HAVE

**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Response Time

**Requirement**: Web page load time < 2 seconds (p95); API response time < 500ms (p95); calculation engine response < 5 seconds for employers with up to 50,000 employees.

**Load Conditions**:

- Peak load: 2,000 concurrent employer sessions during final week of reporting window
- Average load: 200 concurrent sessions
- API: 100 requests per second during peak

**Priority**: MUST_HAVE

---

#### NFR-P-2: Peak Period Scalability

**Requirement**: The system must handle a 10x increase in traffic during the final two weeks before the 4 April deadline without degradation. Historically, 40% of submissions arrive in the final week.

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-1: Authentication and Access Control

**Requirement**: Employer users must authenticate via GOV.UK One Login or equivalent government identity service. EHRC and GEO staff access via departmental SSO. All access role-based with least privilege.

**MFA Required**: Yes, for all users

**Priority**: MUST_HAVE

---

#### NFR-SEC-2: Data Encryption

**Requirement**: All data encrypted in transit (TLS 1.3+) and at rest (AES-256). Pre-publication employer data classified as OFFICIAL-SENSITIVE requires enhanced encryption controls.

**Priority**: MUST_HAVE

---

#### NFR-SEC-3: Audit Logging

**Requirement**: All data access, modifications, and submissions must be logged with immutable audit trail. EHRC access to employer data must be specifically logged for transparency.

**Log Retention**: 7 years

**Priority**: MUST_HAVE

---

### Availability Requirements

#### NFR-A-1: Availability Target

**Requirement**: 99.9% uptime overall; 99.95% during reporting window (January-April). Maximum planned downtime: 4 hours per month, scheduled outside reporting window.

**Priority**: MUST_HAVE

---

#### NFR-A-2: Disaster Recovery

**RPO**: 1 hour (maximum acceptable data loss)

**RTO**: 4 hours (maximum acceptable downtime)

**Priority**: MUST_HAVE

---

### Compliance Requirements

#### NFR-C-1: Equality Act Compliance

**Requirement**: All calculations must precisely implement the Equality Act 2010 (Specific Duties and Public Authorities) Regulations 2017 methodology, validated against GEO published test cases.

**Priority**: MUST_HAVE

---

#### NFR-C-2: WCAG 2.2 Level AA Accessibility

**Requirement**: All user-facing components must meet WCAG 2.2 Level AA. The GOV.UK Design System must be used for all citizen-facing interfaces.

**Priority**: MUST_HAVE

---

#### NFR-C-3: UK GDPR Compliance

**Requirement**: Full UK GDPR compliance including data subject rights, DPIA, lawful basis documentation, and automated retention/deletion.

**Priority**: MUST_HAVE

---

#### NFR-C-4: Welsh Language Compliance

**Requirement**: Public-facing elements must comply with Welsh Language Standards where applicable to the GEO.

**Priority**: SHOULD_HAVE

---

### Usability Requirements

#### NFR-U-1: GOV.UK Design System

**Requirement**: All citizen and employer-facing interfaces must use the GOV.UK Design System, ensuring consistency with other government services.

**Priority**: MUST_HAVE

---

## Integration Requirements

### INT-1: Integration with HMRC Real Time Information (RTI)

**Purpose**: Pre-populate employer pay data from HMRC payroll records to reduce manual data entry and improve data accuracy.

**Integration Type**: Batch data feed (nightly during reporting window) or near-real-time API

**Data Exchanged**:

- **From HMRC to Platform**: Employee pay records (gross pay, hours worked, bonus payments) for snapshot date, anonymised to employer level
- **From Platform to HMRC**: Nothing (read-only consumption)

**Authentication**: Mutual TLS with API key

**Legal Basis**: Digital Economy Act 2017 data sharing agreement

**SLA**: Data available within 24 hours of RTI processing

**Priority**: MUST_HAVE

---

### INT-2: Integration with Companies House

**Purpose**: Validate employer identity and determine reporting eligibility based on employee count and active status.

**Integration Type**: Real-time API (Companies House REST API)

**Data Exchanged**:

- **From Companies House to Platform**: Company registration details, active status, SIC codes

**Priority**: MUST_HAVE

---

### INT-3: Integration with GOV.UK One Login

**Purpose**: Provide employer authentication using the government's identity assurance service.

**Integration Type**: OIDC/OAuth 2.0

**Priority**: MUST_HAVE

---

### INT-4: Integration with GOV.UK Notify

**Purpose**: Send submission confirmations, deadline reminders, and compliance notifications to employers.

**Integration Type**: REST API (GOV.UK Notify API)

**Priority**: MUST_HAVE

---

## Data Requirements

### Data Entities

#### Entity 1: Employer

**Description**: An organisation with 250+ employees subject to gender pay gap reporting obligations.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| employer_id | UUID | Yes | Unique identifier | Primary key |
| companies_house_number | String(8) | Yes | Companies House registration | Validated against CH API |
| employer_name | String(255) | Yes | Legal name | From Companies House |
| sic_code | String(5) | Yes | Standard Industrial Classification | From Companies House |
| employee_count | Integer | Yes | Total employees at snapshot date | >= 250 for eligibility |
| sector | Enum | Yes | Public/private/voluntary | Required for reporting |
| region | String(50) | Yes | Primary operating region | ONS region codes |

**Data Classification**: OFFICIAL

---

#### Entity 2: Submission

**Description**: An annual gender pay gap submission from an eligible employer.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| submission_id | UUID | Yes | Unique identifier | Primary key |
| employer_id | UUID | Yes | FK to Employer | Foreign key |
| reporting_year | Integer | Yes | Reporting year | e.g., 2026 |
| snapshot_date | Date | Yes | Relevant pay period snapshot | 5 April for private/voluntary; 31 March for public |
| mean_hourly_pay_gap | Decimal(5,2) | Yes | Mean hourly pay gap percentage | Calculated |
| median_hourly_pay_gap | Decimal(5,2) | Yes | Median hourly pay gap percentage | Calculated |
| mean_bonus_gap | Decimal(5,2) | Yes | Mean bonus pay gap percentage | Calculated |
| median_bonus_gap | Decimal(5,2) | Yes | Median bonus pay gap percentage | Calculated |
| male_bonus_proportion | Decimal(5,2) | Yes | % of males receiving bonus | Calculated |
| female_bonus_proportion | Decimal(5,2) | Yes | % of females receiving bonus | Calculated |
| lower_quartile_female | Decimal(5,2) | Yes | % female in lower quartile | Calculated |
| lower_middle_quartile_female | Decimal(5,2) | Yes | % female in lower middle quartile | Calculated |
| upper_middle_quartile_female | Decimal(5,2) | Yes | % female in upper middle quartile | Calculated |
| upper_quartile_female | Decimal(5,2) | Yes | % female in upper quartile | Calculated |
| submitted_at | Timestamp | Yes | Submission timestamp | Immutable |
| status | Enum | Yes | Submission status | draft/submitted/published |
| data_source | Enum | Yes | How data was provided | manual/hmrc_prepopulated/api |

**Data Classification**: OFFICIAL-SENSITIVE (pre-publication)

**Data Retention**: 10 years (aggregated/anonymised after 3 years for trend analysis)

---

### Data Quality Requirements

**Data Accuracy**: Pay gap calculations must match GEO test cases with zero tolerance for mathematical errors. Statistical outliers flagged but not rejected automatically.

**Data Completeness**: All 6 mandatory metrics required for a valid submission. Optional narrative commentary encouraged but not required.

**Data Timeliness**: Published within 48 hours of reporting deadline. EHRC compliance data available in real-time.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use GOV.UK Design System for all public-facing interfaces
**TC-2**: Must integrate with GOV.UK One Login for employer authentication
**TC-3**: Must deploy to UK sovereign cloud infrastructure (Crown Hosting or approved UK cloud)

### Business Constraints

**BC-1**: Must be operational for the April 2027 reporting deadline (first full reporting cycle)
**BC-2**: HMRC data sharing agreement must be in place before pre-population feature can go live
**BC-3**: Budget cap of GBP 8M total programme cost over 3 years

### Assumptions

**A-1**: HMRC will agree to a data sharing arrangement under the Digital Economy Act 2017 within 6 months of project start
**A-2**: The Equality Act calculation methodology will not change significantly during the development period
**A-3**: GOV.UK One Login will be available and stable for employer authentication
**A-4**: Approximately 11,000 employers will be eligible to report in the first cycle

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Employer compliance rate | 90% | 100% | April 2027 | Submissions vs eligible employers |
| Average reporting time | 40 hours | 16 hours | April 2027 | Post-submission survey |
| First-submission validation pass rate | 30% | 95% | April 2027 | Platform validation logs |
| Open data API consumers | 0 | 50+ | 12 months post-launch | API registration count |
| EHRC enforcement cases from manual detection | 100% manual | 100% automated | April 2027 | EHRC case data |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability | 99.9% (99.95% in reporting window) | Uptime monitoring |
| Page load time (p95) | < 2 seconds | APM tooling |
| Calculation engine response (p95) | < 5 seconds | APM tooling |
| API response time (p95) | < 500ms | API monitoring |
| Error rate | < 0.1% | Log aggregation |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| HMRC DSA | Data sharing agreement for RTI pre-population | GEO/HMRC | Month 6 | Not Started | HIGH — pre-population delayed |
| GOV.UK One Login | Identity service for employer authentication | GDS | Ongoing | Available | HIGH — alternative auth needed |
| Companies House API | Employer validation and eligibility | Companies House | Available | Available | LOW — API already available |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | HMRC DSA delayed beyond 6 months | MEDIUM | HIGH | Early engagement, Ministerial escalation, manual fallback | SRO |
| R-2 | Peak load exceeds capacity near deadline | MEDIUM | HIGH | Load testing at 3x peak, auto-scaling, CDN | GEO Digital |
| R-3 | Calculation engine errors in edge cases | LOW | HIGH | Extensive test suite against GEO test cases, employer override | GEO Digital |
| R-4 | Employer resistance to changed process | MEDIUM | MEDIUM | Pilot programme, employer engagement, clear guidance | GEO Policy |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | [ ] Approved | | |
| GEO Head of Policy | Policy Owner | [ ] Approved | | |
| GEO Digital Lead | Technical Lead | [ ] Approved | | |
| EHRC Enforcement | Enforcement Partner | [ ] Approved | | |
| SIRO | Information Risk | [ ] Approved | | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|------------|
| GPG | Gender Pay Gap — the difference between the average earnings of men and women |
| RTI | Real Time Information — HMRC system for employer payroll reporting |
| EHRC | Equality and Human Rights Commission |
| GEO | Government Equalities Office |
| SIC | Standard Industrial Classification — industry classification codes |
| Snapshot date | The date on which employer pay data is measured (5 April for private/voluntary; 31 March for public sector) |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Gender Pay Gap Reporting Platform (Project 001)
**Model**: Claude Opus 4.6
