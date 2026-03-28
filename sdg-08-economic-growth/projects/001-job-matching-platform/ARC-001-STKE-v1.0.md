# Stakeholder Drivers & Goals Analysis: Job Matching Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Job Matching Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | SRO, Job Matching Platform Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Job Matching Programme Board, DWP Digital, CDDO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose

This document identifies key stakeholders for the AI-powered Job Matching Platform, their underlying drivers, how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. The platform will replace the current Find a Job service with an intelligent matching engine that connects jobseekers to opportunities based on skills, experience, location, and career aspirations.

### Key Findings

The Job Matching Platform sits at the intersection of two powerful and sometimes conflicting forces: the political imperative to reduce unemployment claimant counts through AI-driven efficiency, and the professional commitment of Jobcentre Plus work coaches to exercise human judgement in supporting vulnerable jobseekers. The strongest alignment exists around improving match quality — Ministers, work coaches, employers, and jobseekers all benefit from better matches. The most significant conflict is between Treasury pressure for rapid AI automation to reduce work coach headcount and the operational evidence that AI augmentation of work coaches (not replacement) produces better employment outcomes, particularly for those furthest from the labour market.

### Critical Success Factors

- Maintain uninterrupted integration with Universal Credit throughout development — any disruption to claimant commitment recording is programme-ending
- Demonstrate measurably better job matching outcomes than Find a Job within 6 months of public beta to retain political sponsorship
- Pass GDS service assessment at Beta with particular scrutiny on AI transparency and bias testing
- Achieve employer adoption — the platform is only valuable if employers post vacancies
- Ensure work coach confidence in AI recommendations — if coaches bypass the system, investment is wasted

### Stakeholder Alignment Score

**Overall Alignment**: MEDIUM

Strong consensus on the need for improved job matching, but significant tensions around the role of AI versus human judgement, the pace of work coach role change, employer onboarding burden, and data sharing between DWP, HMRC, and DfE. The devolved administrations' different employability programmes (e.g., Fair Start Scotland) add integration complexity.

---

## Stakeholder Identification

### Internal Stakeholders

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Secretary of State for Work and Pensions | Minister | HIGH | HIGH | Manage Closely — Ministerial briefings, PQ preparedness |
| DWP Permanent Secretary | Accounting Officer | HIGH | HIGH | Manage Closely — Programme board, spend controls |
| SRO, Job Matching Platform | Programme Sponsor | HIGH | HIGH | Manage Closely — Weekly programme board |
| DWP Chief Digital Information Officer (CDIO) | Digital Leadership | HIGH | HIGH | Manage Closely — Architecture governance |
| Director of Labour Market Policy | Policy ownership | HIGH | HIGH | Manage Closely — Policy requirements, conditionality rules |
| UC Operations Director | Operational delivery | HIGH | HIGH | Manage Closely — Work coach impact, operational readiness |
| DWP SIRO | Information risk | HIGH | MEDIUM | Keep Satisfied — DPIA sign-off, AI risk acceptance |
| DWP Finance Director | Budget holder | HIGH | MEDIUM | Keep Satisfied — Spend approvals, business case |
| Jobcentre Plus District Managers | Regional operations | MEDIUM | HIGH | Keep Informed — Rollout planning, local impact |
| Jobcentre Plus Work Coaches | Frontline users | LOW | HIGH | Keep Informed — User research, training, change management |
| DWP Data Science Team | AI/ML development | MEDIUM | HIGH | Keep Informed — Model development, bias testing |
| DWP Contact Centre Management | Telephony channel | MEDIUM | MEDIUM | Keep Informed — Channel shift impact |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| CDDO | Cabinet Office | Assurance & spend control | HIGH | MEDIUM |
| HM Treasury | HM Treasury | Funding approval | HIGH | MEDIUM |
| GDS Service Assessment Team | Cabinet Office | Service standard assurance | MEDIUM | HIGH |
| National Audit Office (NAO) | Parliament | Value for money audit | HIGH | MEDIUM |
| Information Commissioner's Office (ICO) | Regulator | Data protection / AI oversight | HIGH | HIGH |
| HMRC | Partner department | RTI earnings data | HIGH | HIGH |
| DfE / IfATE | Education department | Skills and qualifications data | MEDIUM | HIGH |
| Employers (large) | Private sector | Vacancy posting, outcomes | MEDIUM | HIGH |
| Employers (SMEs) | Private sector | Vacancy posting | LOW | MEDIUM |
| Jobseekers (UC claimants) | Citizens | Primary service users | LOW | HIGH |
| Jobseekers (non-UC) | Citizens | Voluntary service users | LOW | MEDIUM |
| Devolved Administrations | Scotland, Wales, NI | Devolved employability | MEDIUM | HIGH |
| Recruitment agencies | Private sector | Intermediaries | LOW | HIGH |
| Citizens Advice | Charity | Claimant advocacy | LOW | HIGH |
| Equality and Human Rights Commission (EHRC) | Regulator | AI fairness scrutiny | HIGH | MEDIUM |
| Centre for Data Ethics and Innovation (CDEI) | Advisory body | AI governance guidance | MEDIUM | MEDIUM |

### UK Government Digital Roles (GovS 005)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Responsible Owner (SRO) | Accountable for platform outcomes and spend | HIGH / HIGH | Manage Closely — Steering board, decision escalation |
| Service Owner | Owns end-to-end job matching service and user outcomes | HIGH / HIGH | Manage Closely — Service reviews, user outcomes |
| Product Manager | Prioritises features against user needs and policy | MEDIUM / HIGH | Keep Informed — Sprint reviews, roadmap |
| Delivery Manager | Manages delivery cadence, risks, dependencies | MEDIUM / HIGH | Keep Informed — Stand-ups, risk escalation |
| CDDO | Assurance, spend control, cross-government standards | HIGH / MEDIUM | Keep Satisfied — Spend submissions, assessment gates |
| CDIO | Departmental digital strategy and technology oversight | HIGH / MEDIUM | Keep Satisfied — Architecture alignment |

### UK Government Security Roles (GovS 007)

| Role | Responsibility | Power/Interest | Engagement Strategy |
|------|---------------|----------------|---------------------|
| Senior Security Risk Owner (SSRO) | Protective security risk at board level | HIGH / MEDIUM | Keep Satisfied — Security risk escalation |
| Departmental Security Officer (DSO) | Security coordination and policy | HIGH / MEDIUM | Keep Satisfied — Security compliance gates |
| Senior Information Risk Owner (SIRO) | Information and cyber security risk, DPIA sign-off | HIGH / MEDIUM | Keep Satisfied — AI DPIA, risk acceptance |
| Cyber Security Lead | Operational cyber security, GovAssure | MEDIUM / HIGH | Keep Informed — Security reviews, pen testing |

### Stakeholder Power-Interest Grid

```text
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • HM Treasury      │  • Secretary of     │
        │  • NAO              │    State (Minister)  │
        │  • DWP SIRO         │  • Permanent Sec.   │
        │  • DWP Finance Dir  │  • SRO              │
        │  • CDDO             │  • CDIO             │
        │  • EHRC             │  • Service Owner    │
        │  • SSRO / DSO       │  • Director Labour  │
 P      │                     │    Market Policy     │
 O      │                     │  • UC Ops Director  │
 W      │                     │  • HMRC (RTI)       │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Employers (SME)  │  • Jobseekers       │
        │  • Recruitment      │  • Work Coaches     │
        │    agencies          │  • Citizens Advice  │
        │  • CDEI             │  • DfE / IfATE      │
        │                     │  • District Managers│
        │                     │  • Data Science Team│
        │                     │  • Devolved Admins  │
        │                     │  • Employers (large)│
        │                     │  • ICO              │
        │                     │  • GDS Assessment   │
        │                     │  • Cyber Sec Lead   │
        └─────────────────────┴─────────────────────┘
```

---

## Stakeholder Drivers Analysis

### SD-1: Secretary of State — Reduce Unemployment Claimant Count

**Stakeholder**: Secretary of State for Work and Pensions

**Driver Category**: STRATEGIC

**Driver Statement**: Deliver a visible, measurable reduction in the unemployment claimant count by deploying AI to match jobseekers to suitable vacancies faster and more accurately than the current Find a Job service.

**Context & Background**: The political landscape demands demonstrable progress on employment. The current Find a Job service has low employer engagement and crude keyword matching. Ministers face regular PQs on employment outcomes. The AI opportunity is politically attractive — it demonstrates innovation and efficiency simultaneously.

**Driver Intensity**: CRITICAL

**Enablers**:
- Strong AI/ML capability within DWP Data Science team
- Large datasets (UC claimant data, HMRC RTI, vacancy data) available for training
- Cross-party support for improving employment services

**Blockers**:
- Negative media coverage of AI bias in employment could kill political support
- Work coach union resistance to AI-driven role change
- Poor employer adoption would undermine outcomes

**Related Stakeholders**: HM Treasury (fiscal impact), UC Operations Director (delivery), NAO (scrutiny)

---

### SD-2: Jobcentre Plus Work Coaches — Maintain Professional Judgement

**Stakeholder**: Jobcentre Plus Work Coaches (approximately 13,500 FTE)

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Work coaches want tools that enhance their ability to support jobseekers, not algorithms that override their professional judgement about individual circumstances. They fear being reduced to administrators who enforce AI recommendations rather than skilled professionals who understand local labour markets and individual barriers.

**Context & Background**: Work coaches have deep knowledge of local employers, individual claimant circumstances (health conditions, caring responsibilities, housing instability), and the nuances of what makes a "suitable" job. The current system already creates tension when mandatory job search requirements conflict with coach assessments. An AI system that generates inappropriate recommendations (e.g., suggesting physically demanding work for someone with undisclosed health conditions) would increase workload, not reduce it.

**Driver Intensity**: HIGH

**Enablers**:
- AI designed as recommendation engine that coaches can accept, modify, or override
- Coach input used to improve model accuracy over time (feedback loop)
- Training and professional development around AI-augmented practice

**Blockers**:
- AI presented as replacement for coach judgement
- Performance metrics that measure coach compliance with AI recommendations
- Insufficient training time during rollout

**Related Stakeholders**: UC Operations Director (staff management), PCS Union (industrial relations), Jobseekers (outcome quality)

---

### SD-3: Employers — Reduce Time-to-Hire with Quality Candidates

**Stakeholder**: Employers (large and SME)

**Driver Category**: OPERATIONAL / FINANCIAL

**Driver Statement**: Employers want to fill vacancies quickly with candidates who have the right skills and are likely to stay. The current Find a Job service delivers high volumes of poorly-matched applications, wasting hiring managers' time and increasing cost-per-hire.

**Context & Background**: The UK has approximately 900,000 vacancies at any time. Employers report that government job platforms deliver lower-quality candidates than commercial platforms (Indeed, LinkedIn, Reed). Many employers have stopped posting on Find a Job. For the new platform to succeed, it must compete with commercial alternatives on match quality while offering the additional value of access to the UC claimant pool and work coach-mediated referrals.

**Driver Intensity**: HIGH

**Enablers**:
- AI matching that pre-screens for skills and experience
- Integration with employer ATS (Applicant Tracking Systems) via standard APIs
- Work coach-curated referrals for roles requiring support

**Blockers**:
- Complex onboarding process that deters SME employers
- Poor candidate quality damaging employer trust
- Data sharing concerns (employer vacancy data used for labour market analysis)

**Related Stakeholders**: Recruitment agencies (competitive tension), DBT (business engagement), Jobseekers (match quality)

---

### SD-4: Jobseekers — Find Suitable Work That Matches Aspirations

**Stakeholder**: Jobseekers (UC claimants and voluntary users)

**Driver Category**: PERSONAL / FINANCIAL

**Driver Statement**: Jobseekers want to find work that matches their skills, experience, location, and career aspirations — not just any job to satisfy conditionality requirements. They want the system to understand their circumstances and present genuinely relevant opportunities.

**Context & Background**: The current Find a Job service uses basic keyword matching that produces irrelevant results. A nurse searching for "care" receives results for car valets. Location filtering is crude — it does not account for public transport accessibility. Jobseekers on UC face mandatory job search activity targets, creating an incentive to apply for unsuitable roles. A better matching engine would reduce wasted applications and improve employment sustainability (fewer people cycling back onto UC within 6 months).

**Driver Intensity**: HIGH

**Enablers**:
- AI that understands skills taxonomies and transferable skills
- Location matching that accounts for commute time via public transport
- Career pathway suggestions showing progression opportunities

**Blockers**:
- Algorithmic bias directing certain groups to lower-paid work
- Poor explainability — jobseekers not understanding why roles are recommended
- Benefit conditionality pressure to accept any match, not the best match

**Related Stakeholders**: Work Coaches (mediation), EHRC (fairness), Citizens Advice (advocacy)

---

### SD-5: HMRC — Secure and Accurate Data Sharing

**Stakeholder**: HMRC

**Driver Category**: COMPLIANCE / OPERATIONAL

**Driver Statement**: HMRC must ensure that Real Time Information (RTI) earnings data shared with DWP for job matching and outcome tracking is used strictly within the agreed data sharing agreement, with robust security controls and audit trail.

**Context & Background**: HMRC shares RTI data with DWP under a statutory data sharing gateway (Welfare Reform Act 2012). Expanding use to an AI-powered job matching engine requires a new or amended DPIA and potentially a new legal gateway. HMRC is cautious about scope creep — RTI data intended for UC payment calculation being repurposed for AI model training raises data protection concerns that ICO would scrutinise.

**Driver Intensity**: HIGH

**Enablers**:
- Clear legal gateway for data sharing
- Purpose limitation controls preventing RTI data from being used for AI training without consent
- Robust audit trail and access controls

**Blockers**:
- Ambiguity about whether AI model training constitutes a new purpose under UK GDPR
- ICO enforcement action risk
- Technical complexity of real-time secure data feeds

**Related Stakeholders**: ICO (regulatory oversight), DWP SIRO (risk ownership), DWP Data Science (data needs)

---

### SD-6: DWP Finance Director — Demonstrate Value for Money

**Stakeholder**: DWP Finance Director

**Driver Category**: FINANCIAL

**Driver Statement**: The platform must demonstrate clear return on investment through reduced UC claimant duration, decreased work coach case load per FTE, and lower cost-per-employment-outcome compared to the current service.

**Context & Background**: DWP's digital transformation budget is under intense Treasury scrutiny following previous large-scale IT programme overruns (Universal Credit IT, which cost over GBP 1 billion more than originally planned). Any new AI investment must demonstrate credible, measurable savings. The Green Book methodology requires robust benefits quantification discounted at 3.5%.

**Driver Intensity**: HIGH

**Enablers**:
- Clear baseline metrics from existing Find a Job service
- Phased delivery with measurable benefits at each stage
- Alignment with HM Treasury Green Book appraisal methodology

**Blockers**:
- Benefits realisation dependent on employer adoption (outside DWP control)
- Work coach efficiency gains may not translate to headcount reduction (union agreements)
- Attribution challenge — improved employment outcomes may be due to economic conditions, not the platform

**Related Stakeholders**: HM Treasury (funding), NAO (VfM audit), UC Operations Director (operational savings)

---

## Driver-to-Goal Mapping

### Goal G-1: Improve Job Match Quality

**Derived From Drivers**: SD-1, SD-3, SD-4

**Goal Owner**: Service Owner, Job Matching Platform

**Goal Statement**: Increase the proportion of job applications resulting in interviews from 8% (Find a Job baseline) to 20% within 12 months of public beta launch.

**Why This Matters**: Better match quality simultaneously satisfies Ministerial targets (faster moves off UC), employer needs (less time screening unsuitable candidates), and jobseeker experience (less wasted effort on unsuitable applications). It is the single metric that aligns the most stakeholders.

**Success Metrics**:
- **Primary Metric**: Application-to-interview conversion rate
- **Secondary Metrics**:
  - Time from claim start to first suitable job referral (target: reduce from 14 days to 3 days)
  - Employer satisfaction with candidate quality (target: 70% satisfied vs 35% baseline)
  - Jobseeker satisfaction with relevance of recommendations (target: 65% satisfied)

**Baseline**: 8% application-to-interview rate (Find a Job, 2025-26 data)
**Target**: 20% application-to-interview rate
**Measurement Method**: Tracked via platform analytics and employer outcome reporting (integrated with employer ATS where possible)

**Dependencies**:
- Sufficient employer vacancy volume on the platform (minimum 500,000 active vacancies)
- HMRC RTI integration for employment outcome verification
- Skills taxonomy mapping (ESCO/SOC alignment)

**Risks to Achievement**:
- Insufficient training data quality leads to poor initial model performance
- Employer resistance to sharing outcome data (interview/hire confirmation)

---

### Goal G-2: Reduce Average UC Claimant Duration

**Derived From Drivers**: SD-1, SD-6

**Goal Owner**: Director of Labour Market Policy

**Goal Statement**: Reduce the average duration on UC for job-seeking claimants from 9.2 months to 7.5 months within 18 months of national rollout.

**Why This Matters**: Each month reduction in average claim duration saves approximately GBP 580 per claimant in UC payments. With 1.5 million job-seeking claimants, a 1.7-month average reduction represents potential savings of GBP 1.5 billion annually — though attribution will be contested.

**Success Metrics**:
- **Primary Metric**: Average UC claim duration for job-seeking conditionality groups
- **Secondary Metrics**:
  - Employment sustainability rate at 6 months (target: 75% vs 62% baseline)
  - Proportion of claimants finding work within 3 months (target: 45% vs 30% baseline)

**Baseline**: 9.2 months average claim duration (DWP Stat-Xplore, 2025-26)
**Target**: 7.5 months average claim duration
**Measurement Method**: DWP administrative data, Stat-Xplore

---

### Goal G-3: Preserve and Enhance Work Coach Role

**Derived From Drivers**: SD-2

**Goal Owner**: UC Operations Director

**Goal Statement**: Deploy AI as an augmentation tool that increases work coach capacity from an average caseload of 120 claimants to 160 claimants per FTE, while maintaining or improving employment outcome rates and coach job satisfaction scores.

**Why This Matters**: Work coaches are the human interface of DWP. Their professional judgement about individual barriers, local labour markets, and employer relationships cannot be replicated by AI. But their caseloads are unsustainable. AI should handle routine matching so coaches can focus time on complex cases — people with health conditions, caring responsibilities, or skills gaps that require bespoke support.

**Success Metrics**:
- **Primary Metric**: Average coach caseload (target: 160 from 120 baseline)
- **Secondary Metrics**:
  - Employment outcome rate maintained or improved (baseline: 42% into work within 12 months)
  - Work coach satisfaction survey score (target: maintain above 3.5/5)
  - AI recommendation override rate (monitor — high override indicates poor model fit)

**Baseline**: 120 claimants per work coach, 42% employment outcome rate
**Target**: 160 claimants per work coach, 42%+ employment outcome rate
**Measurement Method**: DWP workforce management data, staff survey, platform analytics

---

### Goal G-4: Achieve Employer Platform Adoption

**Derived From Drivers**: SD-3

**Goal Owner**: SRO, Job Matching Platform

**Goal Statement**: Onboard 50,000 employers posting at least one vacancy within 12 months of public beta, with 80% of those employers posting repeat vacancies.

**Why This Matters**: The platform is only valuable if employers use it. Find a Job had declining employer engagement because match quality was poor and the posting process was cumbersome. Without sufficient vacancy volume, AI matching quality is constrained by a small pool of opportunities.

**Success Metrics**:
- **Primary Metric**: Number of employers with active vacancies
- **Secondary Metrics**:
  - Vacancy volume (target: 500,000 active vacancies)
  - Employer retention rate at 12 months (target: 80%)
  - Average time to post a vacancy (target: < 5 minutes)

**Baseline**: 25,000 active employers on Find a Job (2025-26)
**Target**: 50,000 active employers within 12 months of beta
**Measurement Method**: Platform analytics, employer CRM

---

### Goal G-5: Ensure Algorithmic Fairness Across Protected Characteristics

**Derived From Drivers**: SD-4 (fairness), SD-1 (political risk)

**Goal Owner**: DWP Chief Data Officer

**Goal Statement**: Achieve less than 5% variance in match quality metrics across all nine protected characteristics under the Equality Act 2010, validated quarterly by independent audit.

**Why This Matters**: AI bias in job matching could systematically disadvantage women, ethnic minorities, disabled people, or older workers. This would violate the Equality Act, create political crisis, and undermine public trust in AI in government. The EHRC and ICO have both signalled willingness to take enforcement action against biased AI in public services.

**Success Metrics**:
- **Primary Metric**: Variance in application-to-interview rate across protected groups
- **Secondary Metrics**:
  - Demographic parity in recommendation distribution
  - Equal opportunity in positive outcome rates
  - Disparate impact ratio above 0.8 (four-fifths rule)

**Baseline**: No current baseline (new capability)
**Target**: < 5% variance across protected characteristics
**Measurement Method**: Quarterly bias audit by independent assessor, ongoing automated monitoring

---

## Goal-to-Outcome Mapping

### Outcome O-1: Faster, Sustainable Employment

**Supported Goals**: G-1, G-2

**Outcome Statement**: Reduce average time to employment for UC jobseeking claimants by 20% while improving 6-month employment sustainability from 62% to 75%.

**Measurement Details**:
- **KPI**: Average days from UC claim start to employment start
- **Current Value**: 276 days (9.2 months)
- **Target Value**: 225 days (7.5 months)
- **Measurement Frequency**: Monthly
- **Data Source**: DWP administrative data, HMRC RTI employment start dates
- **Report Owner**: DWP Labour Market Analysis team

**Business Value**:
- **Financial Impact**: Estimated GBP 1.5B annual UC payment savings (fully attributable savings will be lower)
- **Strategic Impact**: Demonstrates AI delivering citizen outcomes, building case for wider adoption
- **Operational Impact**: Reduced work coach caseload pressure
- **Customer Impact**: Jobseekers find suitable work faster, reducing financial hardship

**Timeline**:
- **Phase 1 (Months 1-6)**: Private beta — 10% improvement in pilot areas
- **Phase 2 (Months 7-12)**: Public beta — 15% improvement nationally
- **Phase 3 (Months 13-18)**: Live — 20% improvement sustained
- **Sustainment (Year 2+)**: Continuous model improvement, target 25% improvement

---

### Outcome O-2: Work Coach Effectiveness Amplified

**Supported Goals**: G-3

**Outcome Statement**: Increase work coach capacity by 33% (120 to 160 caseload) while maintaining employment outcome rates, enabling redeployment of freed capacity to intensive support for complex cases.

**Measurement Details**:
- **KPI**: Coach caseload with maintained outcome rates
- **Current Value**: 120 claimants per coach
- **Target Value**: 160 claimants per coach
- **Measurement Frequency**: Monthly
- **Data Source**: DWP workforce management system
- **Report Owner**: UC Operations Director

**Business Value**:
- **Financial Impact**: Enables handling 33% more claimants without proportional headcount increase (estimated GBP 180M annual efficiency)
- **Operational Impact**: Coaches focus on complex cases, improving outcomes for hardest-to-help
- **Customer Impact**: Better support for vulnerable claimants; faster routine matching for job-ready claimants

---

### Outcome O-3: Trusted AI in Public Services

**Supported Goals**: G-5

**Outcome Statement**: Establish the Job Matching Platform as a model for trustworthy AI deployment in UK Government, with published bias metrics, algorithmic transparency records, and positive EHRC assessment.

**Measurement Details**:
- **KPI**: Bias variance across protected characteristics
- **Current Value**: N/A (new system)
- **Target Value**: < 5% variance
- **Measurement Frequency**: Quarterly
- **Data Source**: Independent bias audit reports
- **Report Owner**: DWP Chief Data Officer

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Secretary of State | SD-1 | Reduce claimant count | G-1 | Improve match quality | O-1 | Faster employment |
| Secretary of State | SD-1 | Reduce claimant count | G-2 | Reduce UC duration | O-1 | Faster employment |
| Work Coaches | SD-2 | Maintain professional judgement | G-3 | Enhance coach role | O-2 | Coach effectiveness |
| Employers | SD-3 | Quality candidates fast | G-1 | Improve match quality | O-1 | Faster employment |
| Employers | SD-3 | Quality candidates fast | G-4 | Employer adoption | O-1 | Faster employment |
| Jobseekers | SD-4 | Suitable work matching aspirations | G-1 | Improve match quality | O-1 | Faster employment |
| Jobseekers | SD-4 | Suitable work matching aspirations | G-5 | Algorithmic fairness | O-3 | Trusted AI |
| HMRC | SD-5 | Secure data sharing | G-1 | Improve match quality | O-1 | Faster employment |
| Finance Director | SD-6 | Demonstrate VfM | G-2 | Reduce UC duration | O-1 | Faster employment |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: Secretary of State (SD-1) wants rapid AI automation to reduce claimant count, but Work Coaches (SD-2) need AI positioned as augmentation, not replacement. Aggressive automation targets would undermine coach morale and trigger industrial action.
  - **Resolution Strategy**: PHASE — Position AI as augmentation in Phase 1 (coach-assisted matching). Track outcomes. If AI-only matching proves effective for job-ready claimants, consider direct matching in Phase 2 with coach oversight. Never remove coach ability to override.

- **Conflict 2**: Finance Director (SD-6) wants headcount efficiency from AI, but UC Operations Director needs to maintain coach numbers to handle complex cases. The efficiency gain may not translate to budget reduction.
  - **Resolution Strategy**: INNOVATE — Reframe savings as capacity reallocation, not headcount reduction. Freed coach capacity redirected to intensive support for ESA/health-related claimants (currently underserved).

- **Conflict 3**: HMRC (SD-5) wants strict purpose limitation on RTI data, but DWP Data Science needs RTI data to train matching models. Training on real earnings data is materially different from using it for payment calculation.
  - **Resolution Strategy**: COMPROMISE — Use anonymised, aggregated RTI data for model training (acceptable under DPIA). Use individual RTI data only for real-time outcome verification under existing legal gateway.

**Synergies**:

- **Synergy 1**: Ministerial driver (SD-1) and Employer driver (SD-3) perfectly align — better match quality serves both political and commercial goals
- **Synergy 2**: Work Coach augmentation (SD-2) and Jobseeker experience (SD-4) align — coaches using AI recommendations can provide more personalised support

---

## Communication & Engagement Plan

### Secretary of State

**Primary Message**: The Job Matching Platform uses AI to deliver better employment outcomes faster, demonstrating the UK as a global leader in ethical AI in public services.

**Key Talking Points**:
- AI improves match quality from 8% to 20% interview rate — real people finding real jobs
- Algorithmic transparency published proactively — ahead of any regulatory requirement
- Work coaches empowered, not replaced — the human touch remains central

**Communication Frequency**: Monthly Ministerial briefing
**Preferred Channel**: Written brief with data dashboard

### Jobcentre Plus Work Coaches

**Primary Message**: This is a tool built for you, not instead of you. It handles the routine matching so you can spend more time on the claimants who need you most.

**Key Talking Points**:
- You always have the ability to override any AI recommendation
- Your feedback improves the model — the system learns from your expertise
- Training and support throughout rollout — no one expected to figure it out alone

**Communication Frequency**: Weekly during rollout, monthly thereafter
**Preferred Channel**: Team meetings, JCP intranet, hands-on workshops

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Work Coaches | Manual job search, keyword matching, local knowledge | AI-recommended matches with coach review and override | HIGH | HIGH | Augmentation framing, training programme, feedback loop |
| Jobseekers | Browse Find a Job, keyword search, bulk apply | Personalised recommendations, skills-based matching | MEDIUM | LOW | Improved experience, clear explainability of recommendations |
| Employers | Post on Find a Job, receive bulk applications | Post once, receive pre-screened shortlists | MEDIUM | MEDIUM | Simplified posting, ATS integration, free trial period |
| DWP Data Science | Ad hoc analysis projects | Operational AI team with production ML systems | HIGH | LOW | Career development, new roles, MLOps capability building |

### Change Readiness

**Champions**:
- DWP Data Science Team — enthusiastic about operational AI, new career opportunities
- Large employers — frustrated with current system, eager for better candidates

**Fence-sitters**:
- JCP District Managers — supportive in principle but concerned about rollout disruption
- Devolved Administrations — interested but wary of UK-wide system affecting devolved employability

**Resisters**:
- PCS Union — concerned about work coach headcount implications
- Some work coaches — fear of deskilling, distrust of AI
- Recruitment agencies — perceive platform as competitive threat

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Work Coach Resistance Undermines Adoption

**Related Stakeholders**: Work Coaches, PCS Union, UC Operations Director
**Risk Description**: Work coaches may refuse to use or actively bypass AI recommendations if they perceive the system as threatening their professional role or generating poor-quality suggestions.
**Impact on Goals**: G-3 (coach effectiveness), G-1 (match quality dependent on coach engagement)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Augmentation framing from day one; coach feedback loop integrated into model improvement; visible override capability; no performance metrics tied to AI compliance rate
**Contingency Plan**: If adoption below 50% after 3 months, pause rollout and conduct intensive engagement with coach representatives

### Risk R-2: AI Bias Causes Political and Legal Crisis

**Related Stakeholders**: EHRC, ICO, Secretary of State, Jobseekers
**Risk Description**: AI matching model systematically disadvantages a protected group (e.g., recommending lower-paid roles to women or ethnic minorities), discovered by media or regulator.
**Impact on Goals**: G-5 (fairness), G-1 (platform credibility)
**Probability**: MEDIUM
**Impact**: CRITICAL
**Mitigation Strategy**: Quarterly independent bias audit; automated bias monitoring in production; Algorithmic Transparency Record published proactively; AI Ethics Board with external members
**Contingency Plan**: Immediate model rollback to rule-based matching; public statement and remediation plan within 48 hours

### Risk R-3: Employer Adoption Falls Short

**Related Stakeholders**: Employers, Service Owner
**Risk Description**: Employers do not adopt the platform in sufficient numbers, limiting vacancy volume and therefore AI match quality.
**Impact on Goals**: G-4 (employer adoption), G-1 (match quality)
**Probability**: MEDIUM
**Impact**: HIGH
**Mitigation Strategy**: Employer advisory panel from Alpha; ATS integration (Indeed, LinkedIn job feed); vacancy scraping as fallback; free premium features for early adopters
**Contingency Plan**: If below 30,000 employers at 6 months, aggregate vacancies from commercial job boards via API partnerships

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Budget approval | DWP Finance Director | SRO | HM Treasury, CDDO | All stakeholders |
| AI model deployment | DWP Data Science Lead | Chief Data Officer | AI Ethics Board, SIRO | Service Owner, Work Coaches |
| Feature prioritisation | Product Manager | Service Owner | Work Coaches, Employers | Delivery Manager |
| Architecture decisions | Lead Architect | CDIO | CDDO, Security Lead | Development teams |
| Go/No-go for beta | SRO | Permanent Secretary | GDS, CDDO, AI Ethics Board | Minister, All |
| Bias remediation action | Chief Data Officer | SIRO | EHRC, ICO | Minister, SRO |

### Escalation Path

1. **Level 1**: Product Manager / Delivery Manager (day-to-day decisions)
2. **Level 2**: Programme Board (scope, timeline, budget variances, stakeholder conflicts)
3. **Level 3**: SRO / Permanent Secretary (strategic direction, Ministerial risks, AI ethics)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| SRO | PENDING | | PENDING |
| Service Owner | PENDING | | PENDING |
| UC Operations Director | PENDING | | PENDING |
| DWP CDIO | PENDING | | PENDING |
| Work Coach Representatives | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (SRO) | | | |
| Service Owner | | | |
| Enterprise Architect | | | |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | SDG 8 Programme | Principles 1, 2, 7, 8, 9, 14 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| GDS Service Standard | Standard | GOV.UK | Service assessment criteria | https://www.gov.uk/service-manual/service-standard |
| CDDO Algorithmic Transparency Standard | Standard | GOV.UK | AI transparency recording | https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub |
| Equality Act 2010 | Legislation | UK Parliament | Protected characteristics | https://www.legislation.gov.uk/ukpga/2010/15 |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: Job Matching Platform
**Model**: Claude Opus 4.6
