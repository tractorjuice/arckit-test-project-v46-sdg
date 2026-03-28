# Project Requirements: National Digital Learning Platform

> **Template Origin**: Official | **ArcKit Version**: 4.6.1 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Requirements Specification |
| **Project** | National Digital Learning Platform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-28 |
| **Last Modified** | 2026-03-28 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-28 |
| **Owner** | Product Manager, NDLP Programme |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | NDLP Programme Board, DfE Digital, Development Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-28 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive business, functional, non-functional, integration, and data requirements for the National Digital Learning Platform (NDLP). It provides the authoritative specification against which the platform will be designed, built, and acceptance tested. Requirements are traceable to stakeholder drivers documented in ARC-001-STKE-v1.0.

---

## Executive Summary

### Business Context

The Department for Education is commissioning a National Digital Learning Platform to provide unified, free access to high-quality digital learning resources for all state-funded schools and colleges in England. The platform addresses the widening digital divide exposed by COVID-19, where disadvantaged pupils lost an estimated additional 0.5 months of learning progress due to inadequate access to digital resources and devices.

Currently, the English education system relies on a fragmented landscape of commercial EdTech platforms, with schools independently procuring and managing multiple solutions. This creates inconsistency in resource quality, duplicated procurement effort, and significant barriers for disadvantaged schools with limited budgets. The NDLP will provide a single, quality-assured platform that integrates with existing school Management Information Systems, supports diverse pedagogical approaches, and is accessible to all learners regardless of their socioeconomic background.

### Objectives

- Provide free, universal access to quality-assured digital learning resources aligned to the national curriculum (KS1-KS4)
- Integrate with major school MIS providers to eliminate duplicate data entry and enable seamless classroom use
- Reduce teacher time spent on resource preparation by 50% (from 4 hours to 2 hours per week)
- Ensure full compliance with the ICO Age Appropriate Design Code and WCAG 2.2 Level AA
- Support voluntary adoption by 40% of state-funded schools within 18 months

### Expected Outcomes

- Narrowing of the disadvantaged attainment gap by 0.3 months at KS2 within 2 years
- Reduction in teacher resource preparation time by 2 hours per week
- GBP 50M saving from reduced need for separate catch-up programmes
- Improved parental engagement with learning, particularly in disadvantaged communities

### Project Scope

**In Scope**:

- Web-based learning platform accessible via browser on any device
- Curriculum resource library (KS1-KS4 core subjects: English, Maths, Science)
- Teacher resource management and lesson planning tools
- Pupil-facing learning interface with age-appropriate design
- Parent/carer engagement portal with progress visibility
- Integration with DfE Sign-in, GIAS, and top 3 MIS providers
- Content quality assurance framework and review workflow
- Analytics dashboard (aggregated, non-individual teacher level)

**Out of Scope**:

- Post-16 / FE college curriculum content (Phase 2)
- Adaptive learning / AI-powered personalisation (Phase 2)
- Hardware provision (covered by separate Get Help with Technology programme)
- Assessment/examination functionality (Ofqual jurisdiction)
- SEND-specific specialist content creation (Phase 2 — partnership with nasen)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| SRO | Programme Sponsor | DfE | Decision maker |
| CDO | Technical Authority | DfE Digital | Architecture oversight |
| Service Owner | Product Strategy | DfE | Requirements prioritisation |
| Product Manager | Feature Delivery | DfE | Day-to-day requirements management |
| Curriculum Lead | Content Quality | DfE Curriculum & Standards | Content requirements |
| DfE SIRO | Information Risk | DfE | Data protection sign-off |
| Headteacher Representative | User Advocate | Schools | User acceptance |
| Teacher Representative | User Advocate | Schools | User research and testing |
| Parent Representative | User Advocate | Parents | Accessibility and engagement review |

---

## Business Requirements

### BR-1: Universal Free Access to Quality Learning Resources

**Description**: The platform MUST provide free access to a comprehensive library of quality-assured digital learning resources covering the national curriculum for Key Stages 1-4, available to all state-funded schools in England without charge.

**Rationale**: The digital divide in education is primarily driven by cost barriers. Free, universal access ensures that a school's budget does not determine its pupils' access to quality digital resources.

**Success Criteria**:

- 100% of KS1-KS4 core subject areas covered with at least 50 resources each
- All resources reviewed and quality-assured before publication
- Zero-cost access for any state-funded school

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Parents (SD-4)

---

### BR-2: Reduce Teacher Resource Preparation Time

**Description**: The platform MUST demonstrably reduce the time teachers spend finding, evaluating, and adapting digital learning resources by at least 50%.

**Rationale**: Teacher workload is unsustainable and resource preparation is a major contributor. Reducing this workload improves teacher wellbeing, retention, and time available for direct pupil interaction.

**Success Criteria**:

- Teacher-reported preparation time reduces from 4 hours to 2 hours per week
- 80% of teachers report the platform saves them time
- Resource search to download in under 3 clicks / 30 seconds

**Priority**: MUST_HAVE

**Stakeholder**: Headteachers (SD-3), Teaching Unions (SD-6)

---

### BR-3: Narrow the Disadvantaged Attainment Gap

**Description**: The platform MUST support targeted interventions and equitable access patterns that contribute to narrowing the attainment gap between disadvantaged and non-disadvantaged pupils.

**Rationale**: SDG 4 specifically targets inclusive and equitable quality education. The platform must not merely provide access but actively support equity outcomes.

**Success Criteria**:

- Platform usage rates for FSM-eligible pupils within 10% of non-FSM peers
- Targeted resources for catch-up and intervention available for all key stages
- Usage analytics disaggregated by disadvantage indicators

**Priority**: MUST_HAVE

**Stakeholder**: Secretary of State (SD-1), Pupil Premium Policy Team

---

### BR-4: Integrate Seamlessly with School Systems

**Description**: The platform MUST integrate with school Management Information Systems so that teachers can access the platform without re-entering data and class lists synchronise automatically.

**Rationale**: Without MIS integration, the platform creates additional workload rather than reducing it. Integration is the single biggest determinant of teacher adoption.

**Success Criteria**:

- Working integration with SIMS, Bromcom, and Arbor (covering 85% of schools)
- Class list synchronisation accurate to 99.9%
- School onboarding completed in under 30 minutes

**Priority**: MUST_HAVE

**Stakeholder**: MAT CEOs (SD-2), Headteachers (SD-3)

---

### BR-5: Comply with Children's Data Protection Standards

**Description**: The platform MUST fully comply with the ICO Age Appropriate Design Code (all 15 standards), UK GDPR, and the Data Protection Act 2018.

**Rationale**: The platform will process personal data of millions of children. Non-compliance would trigger ICO enforcement, damage public trust, and potentially cause harm to children.

**Success Criteria**:

- Independent AADC compliance audit passed (15/15 standards)
- DPIA completed and approved by DfE SIRO
- Privacy settings default to highest protection level
- No profiling or non-educational use of children's data

**Priority**: MUST_HAVE

**Stakeholder**: ICO (SD-8), DfE SIRO

---

### BR-6: Support Curriculum Neutrality and Pedagogical Freedom

**Description**: The platform MUST support diverse pedagogical approaches without imposing a single teaching methodology, ensuring schools retain full autonomy over curriculum delivery.

**Rationale**: School autonomy over curriculum delivery is a fundamental principle of the English education system. Headteachers and unions will reject any platform perceived as dictating how to teach.

**Success Criteria**:

- Resources tagged by topic/concept, not by pedagogical approach
- Teachers can adapt, combine, and annotate resources
- No "recommended sequence" that implies a mandatory curriculum pathway
- Platform does not prescribe lesson structure or teaching methods

**Priority**: MUST_HAVE

**Stakeholder**: Headteachers (SD-3), Teaching Unions (SD-6), Ofsted (SD-5)

---

### BR-7: Enable Parental Engagement with Learning

**Description**: The platform MUST provide parents and carers with appropriate visibility of their child's learning activities and progress, in a format accessible to parents with low digital literacy.

**Rationale**: Parental engagement is the strongest predictor of educational achievement. The platform must enable, not exclude, parental involvement.

**Success Criteria**:

- Parent portal accessible at WCAG 2.2 AA standard
- Content readable at age 9-11 reading level
- Available in top 10 community languages
- 70% of active parents report feeling more engaged with their child's learning

**Priority**: SHOULD_HAVE

**Stakeholder**: Parents/Carers (SD-4)

---

### BR-8: Provide Trust-Level Analytics for MATs

**Description**: The platform SHOULD provide Multi-Academy Trusts with aggregated analytics dashboards showing resource usage and engagement patterns across all schools in their trust.

**Rationale**: MAT CEOs need trust-wide visibility to ensure consistent quality and identify schools that may need additional support. However, analytics must be aggregated (never individual teacher level) to address union concerns.

**Success Criteria**:

- Trust-level dashboard showing school-by-school engagement (aggregated)
- Cohort-level progress indicators (never individual teacher)
- Data export capability for trust reporting
- Contractual prohibition on using data for teacher performance management

**Priority**: SHOULD_HAVE

**Stakeholder**: MAT CEOs (SD-2)

---

## Functional Requirements

### User Personas

#### Persona 1: Ms. Patel — Year 4 Primary Teacher

- **Role**: Class teacher, English and Maths lead
- **Goals**: Find quality resources quickly, reduce evening/weekend planning, track pupil engagement with homework
- **Pain Points**: Spends 5 hours/week searching for resources across 4 different platforms; unreliable school broadband; shared staff laptop
- **Technical Proficiency**: Medium
- **Context**: Teaches in a two-form entry primary school in Birmingham with 45% FSM eligibility

#### Persona 2: Mr. Davies — Year 10 Science Teacher

- **Goals**: Access practical-aligned resources for combined science GCSE, set and track homework, share resources with department
- **Pain Points**: Department uses 3 different platforms with separate logins; cannot find resources specific to AQA specification; pupils lose work when platform subscriptions lapse
- **Technical Proficiency**: High
- **Context**: Teaches in a secondary academy in South Wales border area; part of a MAT with 12 schools

#### Persona 3: Sarah — Parent of Year 6 Pupil (FSM eligible)

- **Goals**: Help daughter with SATs preparation at home, understand what she is learning, communicate with teacher about progress
- **Pain Points**: Shares a smartphone with two other children; no broadband at home (uses mobile data); left school at 16 with no GCSEs; English is second language (Urdu first)
- **Technical Proficiency**: Low
- **Context**: Single parent, three children, eligible for free school meals, lives in social housing in Bradford

---

### Use Cases

#### UC-1: Teacher Discovers and Uses a Curriculum Resource

**Actor**: Ms. Patel (Year 4 Teacher)

**Preconditions**:

- Teacher authenticated via DfE Sign-in
- School registered on the platform with MIS integration active
- Class lists synchronised from MIS

**Main Flow**:

1. Teacher navigates to resource library
2. Teacher filters by Key Stage (KS2), Subject (Maths), Topic (Fractions)
3. System displays quality-assured resources sorted by relevance
4. Teacher previews a resource and reviews learning objectives
5. Teacher selects resource and assigns it to her Year 4 class
6. System records assignment and notifies pupils (if homework)
7. Teacher can view completion status on class dashboard

**Postconditions**:

- Resource assigned to specified class
- Pupils can access the resource via their own accounts
- Usage logged for aggregated analytics (not individual teacher tracking)

**Alternative Flows**:

- **Alt 3a**: No resources match filters — system suggests broader search terms or related topics
- **Alt 5a**: Teacher customises the resource before assigning (adds annotations, removes sections)

**Priority**: CRITICAL

---

#### UC-2: Parent Views Child's Learning Progress

**Actor**: Sarah (Parent, FSM eligible)

**Preconditions**:

- Parent authenticated via parent account (linked to child's school record)
- Child has active assignments on the platform

**Main Flow**:

1. Parent opens platform on smartphone browser
2. System displays child's dashboard in parent's preferred language (Urdu)
3. Parent views current learning topics and recent assignments
4. Parent sees completion status for homework tasks
5. Parent taps a topic to see suggested activities to support learning at home
6. System provides age-appropriate, jargon-free guidance

**Postconditions**:

- Parent has viewed child's learning summary
- No data about parent's access shared with school or teacher

**Alternative Flows**:

- **Alt 2a**: Parent has multiple children — system shows selector for each child
- **Alt 5a**: Parent is offline — system shows cached version of last-viewed data

**Priority**: HIGH

---

#### UC-3: MAT Administrator Reviews Trust-Wide Analytics

**Actor**: MAT Data Manager

**Preconditions**:

- Administrator authenticated via DfE Sign-in with MAT-level permissions
- At least one term of usage data available

**Main Flow**:

1. Administrator navigates to trust analytics dashboard
2. System displays aggregated resource usage across all trust schools
3. Administrator filters by subject, key stage, or school
4. System shows engagement metrics (resources accessed, homework completion rates) at school level
5. Administrator exports report for trust board meeting
6. System generates PDF/CSV with trust branding

**Postconditions**:

- Report generated with aggregated, non-individual data
- No teacher-level or individual pupil data exposed

**Priority**: MEDIUM

---

### Functional Requirements Detail

#### FR-1: Curriculum Resource Library

**Description**: The system must provide a searchable library of quality-assured digital learning resources organised by key stage, subject, topic, and resource type.

**Relates To**: BR-1, BR-6, UC-1

**Acceptance Criteria**:

- [ ] Given a teacher is authenticated, when they navigate to the resource library, then they see resources organised by KS1/KS2/KS3/KS4 and subject
- [ ] Given a teacher selects filters (key stage, subject, topic), when they search, then results are returned within 2 seconds
- [ ] Given a resource exists, when a teacher views it, then they see learning objectives, curriculum alignment, and estimated duration
- [ ] Edge case: When no resources match the search, the system suggests related topics

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: Content quality assurance workflow (FR-3)

---

#### FR-2: Resource Assignment and Homework Setting

**Description**: The system must allow teachers to assign resources to classes or groups of pupils, with optional deadlines for homework.

**Relates To**: BR-2, UC-1

**Acceptance Criteria**:

- [ ] Given a teacher has selected a resource, when they choose "Assign to class", then they can select from their synchronised class lists
- [ ] Given a teacher assigns homework, when they set a deadline, then pupils see the deadline on their dashboard
- [ ] Given a pupil completes an assignment, when the teacher views the class dashboard, then completion status is updated in real time
- [ ] Edge case: When a pupil is absent from the class list (e.g., recently joined), the teacher can manually add them

**Priority**: MUST_HAVE
**Complexity**: MEDIUM
**Dependencies**: MIS integration (FR-6)

---

#### FR-3: Content Quality Assurance Workflow

**Description**: The system must support a content review and approval workflow ensuring all published resources meet DfE quality standards.

**Relates To**: BR-1, BR-6

**Acceptance Criteria**:

- [ ] Given a resource is submitted, when it enters review, then it is assigned to a subject-specialist reviewer
- [ ] Given a reviewer approves a resource, when it is published, then it carries a "DfE Quality Assured" badge
- [ ] Given a resource receives negative user feedback (>20% negative ratings), when reviewed, then it is flagged for quality re-review
- [ ] Edge case: Resources from external EdTech partners go through the same quality assurance process

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-4: Pupil Learning Interface

**Description**: The system must provide an age-appropriate interface for pupils to access assigned resources, complete activities, and track their own learning.

**Relates To**: BR-1, BR-5, UC-2

**Acceptance Criteria**:

- [ ] Given a KS1 pupil (age 5-7) is logged in, when they see their dashboard, then the interface uses large icons, simple language, and minimal text
- [ ] Given a KS4 pupil (age 14-16) is logged in, when they see their dashboard, then the interface provides detailed subject organisation and self-directed learning options
- [ ] Given a pupil with SEND is logged in, when they access resources, then text-to-speech, adjustable font size, and high contrast mode are available
- [ ] Edge case: When a pupil accesses the platform from a shared family device, their session is isolated from siblings' sessions

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

#### FR-5: Parent/Carer Portal

**Description**: The system must provide parents and carers with visibility of their child's learning activities, homework status, and suggested home learning activities.

**Relates To**: BR-7, UC-2

**Acceptance Criteria**:

- [ ] Given a parent is authenticated, when they view their child's dashboard, then they see current topics, homework status, and recent activity
- [ ] Given a parent selects a different language, when the page reloads, then all content is displayed in the selected language
- [ ] Given a parent has multiple children at the same school, when they log in, then they can switch between children's dashboards
- [ ] Edge case: Parent access MUST NOT reveal which teacher set which homework (union requirement)

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM
**Dependencies**: MIS integration (FR-6), multilingual support (FR-10)

---

#### FR-6: MIS Integration (SIMS, Bromcom, Arbor)

**Description**: The system must integrate with the three largest school MIS providers to synchronise school structure, class lists, and pupil data.

**Relates To**: BR-4, UC-1

**Acceptance Criteria**:

- [ ] Given a school uses SIMS, when the IT administrator initiates integration, then class lists, pupil names, and year groups are synchronised within 10 minutes
- [ ] Given a pupil joins or leaves a school, when the MIS is updated, then the platform reflects the change within 24 hours
- [ ] Given a teacher creates a class group in the MIS, when synchronisation runs, then the group appears on the platform
- [ ] Edge case: When MIS is temporarily unavailable, the platform continues to function with last-known class lists

**Priority**: MUST_HAVE
**Complexity**: HIGH
**Dependencies**: MIS vendor API access agreements

---

#### FR-7: DfE Sign-in Integration

**Description**: The system must use DfE Sign-in as the sole authentication mechanism for teachers and school administrators.

**Relates To**: BR-4

**Acceptance Criteria**:

- [ ] Given a teacher has a DfE Sign-in account, when they access the platform, then they are redirected to DfE Sign-in and returned authenticated
- [ ] Given a teacher is authenticated, when they access the platform from a different device, then their session and preferences are consistent
- [ ] Given DfE Sign-in is temporarily unavailable, when a teacher attempts to log in, then the system displays a meaningful error message with expected resolution time

**Priority**: MUST_HAVE
**Complexity**: MEDIUM

---

#### FR-8: Offline Content Access

**Description**: The system should support downloading resources for offline use, enabling teachers and pupils in areas with poor connectivity to access learning materials.

**Relates To**: BR-3 (digital divide)

**Acceptance Criteria**:

- [ ] Given a teacher selects "Download for offline", when they choose resources, then a cached copy is stored on the device
- [ ] Given a pupil is offline, when they access previously downloaded resources, then they can view and interact with the content
- [ ] Given a pupil completes offline work, when connectivity is restored, then progress is synchronised to the platform

**Priority**: SHOULD_HAVE
**Complexity**: HIGH

---

#### FR-9: Analytics Dashboard (Aggregated)

**Description**: The system must provide analytics dashboards showing resource usage, engagement patterns, and adoption metrics at school and trust level.

**Relates To**: BR-8, UC-3

**Acceptance Criteria**:

- [ ] Given a school administrator views analytics, when they access the dashboard, then they see school-level aggregated data only
- [ ] Given a MAT administrator views analytics, when they access the trust dashboard, then they see school-by-school comparison (aggregated)
- [ ] Given any user views analytics, when they attempt to view individual teacher data, then the system denies access
- [ ] Edge case: Analytics dashboards comply with AADC — no individual pupil profiling visible

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

#### FR-10: Multilingual Support

**Description**: The system must support the parent portal in the 10 most common community languages in England.

**Relates To**: BR-7

**Acceptance Criteria**:

- [ ] Given a parent selects Urdu as their language, when the portal loads, then all navigation, labels, and guidance text display in Urdu
- [ ] Given educational content is in English, when a parent views their child's assignments, then the surrounding interface is in the selected language but resource content remains in English
- [ ] Languages supported: English, Urdu, Polish, Punjabi, Bengali, Gujarati, Arabic, Somali, Tamil, Mandarin

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

#### FR-11: Resource Adaptation and Annotation

**Description**: The system must allow teachers to adapt, annotate, and save customised versions of resources for their own use.

**Relates To**: BR-6

**Acceptance Criteria**:

- [ ] Given a teacher views a resource, when they select "Adapt", then they can add annotations, remove sections, or reorder content
- [ ] Given a teacher saves an adapted resource, when they view their library, then the customised version is saved alongside the original
- [ ] Given a teacher shares an adapted resource with their department, when colleagues view it, then the adaptations are visible with attribution

**Priority**: SHOULD_HAVE
**Complexity**: MEDIUM

---

#### FR-12: Content Search with Curriculum Alignment

**Description**: The system must provide intelligent search that understands curriculum structure, enabling teachers to find resources by national curriculum reference, exam board specification, or learning objective.

**Relates To**: BR-1, BR-6

**Acceptance Criteria**:

- [ ] Given a teacher searches for "Year 6 fractions", when results appear, then resources are tagged with specific national curriculum references (e.g., 6F1, 6F2)
- [ ] Given a secondary teacher searches by exam board (e.g., "AQA Combined Science B4"), when results appear, then resources are aligned to that specific specification
- [ ] Given a search returns results, when the teacher hovers over a resource, then a preview shows curriculum alignment, difficulty level, and estimated duration

**Priority**: MUST_HAVE
**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-1: Page Load Time

**Requirement**: All pages must load within 2 seconds at the 95th percentile under normal load conditions, and within 4 seconds under peak load (results day/census day).

**Load Conditions**:

- Normal load: 100,000 concurrent users
- Peak load: 500,000 concurrent users (results day scenario)
- Data volume: 10 million pupil records, 500,000 teacher accounts

**Priority**: CRITICAL

---

#### NFR-P-2: Search Response Time

**Requirement**: Resource search queries must return results within 500ms at the 95th percentile, including filtering by key stage, subject, topic, and exam board.

**Priority**: HIGH

---

### Availability and Resilience Requirements

#### NFR-A-1: Availability Target

**Requirement**: The platform must achieve 99.9% uptime during term time (September-July), with enhanced 99.99% availability during examination and results periods.

- Maximum planned downtime: 4 hours/month during school holidays only
- Maximum unplanned downtime: 8.7 hours/year

**Priority**: CRITICAL

---

#### NFR-A-2: Disaster Recovery

**RPO**: Maximum 15 minutes data loss for transactional data
**RTO**: Maximum 1 hour to restore service

**Backup Requirements**:

- Continuous backup for transactional data
- Daily full backup retained for 90 days
- Geographic backup in a separate UK region

**Priority**: CRITICAL

---

### Security Requirements

#### NFR-SEC-1: Authentication via DfE Sign-in

**Requirement**: All teacher and administrator access must authenticate via DfE Sign-in using SAML 2.0 / OpenID Connect. Pupil access via school-managed accounts. Parent access via self-registration linked to school verification.

**MFA**: Required for administrators and trust-level analytics access.

**Session Management**:

- Session timeout: 60 minutes of inactivity for teachers; 30 minutes for admin
- Absolute session timeout: 8 hours (aligned with school day)

**Priority**: CRITICAL

---

#### NFR-SEC-2: Children's Data Encryption

**Requirement**: All children's personal data must be encrypted at rest (AES-256) and in transit (TLS 1.3+). Application-level field encryption required for SEND status, FSM eligibility, and safeguarding flags.

**Priority**: CRITICAL

---

#### NFR-SEC-3: Age Appropriate Design Code Compliance

**Requirement**: The platform must comply with all 15 standards of the ICO Age Appropriate Design Code, including:

- [ ] Best interests of the child as a primary consideration
- [ ] Data protection impact assessments
- [ ] Age-appropriate application (different interfaces for different age groups)
- [ ] Transparency (child-friendly privacy information)
- [ ] Detrimental use (no use of data in ways detrimental to children's wellbeing)
- [ ] Default settings (high privacy by default)
- [ ] Data minimisation
- [ ] Data sharing restrictions
- [ ] Geolocation (off by default)
- [ ] Parental controls
- [ ] Profiling (off by default for under-18s)
- [ ] Nudge techniques (prohibited for children)
- [ ] Connected toys and devices (N/A for this platform)
- [ ] Online tools (transparency about data use)
- [ ] Data protection by design

**Priority**: CRITICAL

---

### Compliance and Regulatory Requirements

#### NFR-C-1: UK GDPR Compliance

**Requirement**: Full compliance with UK GDPR including data subject rights for children, parents, and educators.

**Key Requirements**:

- [ ] Data subject access requests fulfilled within 30 days
- [ ] Right to erasure supported (with education record retention exceptions)
- [ ] Privacy by design and by default
- [ ] Data breach notification to ICO within 72 hours
- [ ] DPIA completed and approved

**Priority**: CRITICAL

---

#### NFR-C-2: DfE Data Standards Compliance

**Requirement**: All data collection, storage, and sharing must comply with DfE data standards including the Common Basic Data Set (CBDS), Unique Pupil Number (UPN) usage, and School Census data definitions.

**Priority**: HIGH

---

### Usability Requirements

#### NFR-U-1: WCAG 2.2 Level AA Accessibility

**Requirement**: All user-facing components must meet WCAG 2.2 Level AA. Features include:

- [ ] Keyboard navigation for all functions
- [ ] Screen reader compatibility (tested with JAWS, NVDA, VoiceOver)
- [ ] High contrast mode
- [ ] Adjustable font sizes (up to 200% without horizontal scrolling)
- [ ] Alt text for all images
- [ ] Captions for all video/audio content
- [ ] No content relies solely on colour to convey meaning

**Priority**: CRITICAL

---

#### NFR-U-2: Mobile Responsive Design

**Requirement**: The platform must be fully functional on mobile devices (minimum 320px viewport width), optimised for the parent portal which will primarily be accessed via smartphones.

**Priority**: HIGH

---

## Integration Requirements

### INT-1: Integration with DfE Sign-in

**Purpose**: Federated authentication for teachers, school administrators, and trust administrators.

**Integration Type**: Real-time API (SAML 2.0 / OpenID Connect)

**Data Exchanged**:

- **From DfE Sign-in to NDLP**: User identity, organisation (school/MAT), roles and permissions
- **From NDLP to DfE Sign-in**: Service registration, access request approvals

**Authentication**: SAML 2.0 assertion with signed tokens
**SLA**: 99.95% availability, < 500ms authentication response time
**Priority**: CRITICAL

---

### INT-2: Integration with Get Information About Schools (GIAS)

**Purpose**: Authoritative source for school/establishment data (name, address, type, phase, URN, UKPRN, MAT membership).

**Integration Type**: Batch API (daily synchronisation) + real-time lookup

**Data Exchanged**:

- **From GIAS to NDLP**: School name, address, URN, UKPRN, phase, type, MAT membership, open/closed status
- **From NDLP to GIAS**: None (read-only consumer)

**Authentication**: API key
**SLA**: Data refreshed within 24 hours of GIAS update
**Priority**: MUST_HAVE

---

### INT-3: Integration with School MIS (SIMS, Bromcom, Arbor)

**Purpose**: Synchronise class lists, pupil data, and school structure to eliminate manual data entry.

**Integration Type**: Real-time API + scheduled batch synchronisation

**Data Exchanged**:

- **From MIS to NDLP**: Class lists, pupil names, UPN, year group, registration group, SEND status (flag only), FSM eligibility (flag only)
- **From NDLP to MIS**: Resource assignment data, completion status (where MIS supports inbound data)

**Authentication**: OAuth 2.0 (per MIS vendor specification)
**Error Handling**: Retry with exponential backoff; continue with cached data if MIS unavailable
**SLA**: Synchronisation within 24 hours of MIS change; API response < 2 seconds
**Priority**: CRITICAL

---

### INT-4: Integration with GOV.UK Notify

**Purpose**: Send notifications to parents/carers about homework assignments, progress updates, and platform communications.

**Integration Type**: Real-time API

**Data Exchanged**:

- **From NDLP to GOV.UK Notify**: Notification content, recipient contact details, template ID
- **From GOV.UK Notify to NDLP**: Delivery status callbacks

**Authentication**: API key
**SLA**: Notification delivered within 5 minutes of trigger
**Priority**: SHOULD_HAVE

---

### INT-5: Integration with ESFA Funding Data

**Purpose**: Identify schools eligible for enhanced support based on funding data, pupil premium allocation, and disadvantage indicators.

**Integration Type**: Batch file transfer (monthly)

**Data Exchanged**:

- **From ESFA to NDLP**: School-level pupil premium allocation, FSM eligibility rates, funding band
- **From NDLP to ESFA**: None (read-only consumer)

**Priority**: SHOULD_HAVE

---

## Data Requirements

### DR-1: Pupil Record

**Description**: Core pupil data synchronised from MIS for platform operation.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| pupil_id | UUID | Yes | Platform-internal identifier | Primary key, never exposed externally |
| upn | String(13) | Yes | Unique Pupil Number | Validated against DfE UPN format |
| first_name | String(100) | Yes | Pupil first name | Not null |
| last_name | String(100) | Yes | Pupil last name | Not null |
| date_of_birth | Date | Yes | For age-appropriate interface selection | Not null |
| year_group | Integer | Yes | Current year group (R, 1-13) | Range: 0-13 |
| school_urn | String(6) | Yes | School URN from GIAS | Foreign key to school record |
| fsm_eligible | Boolean | Yes | Free school meal eligibility flag | Default: false |
| send_flag | Boolean | Yes | SEND status flag (not detail) | Default: false |
| eal_flag | Boolean | No | English as Additional Language | Default: false |

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Deleted within 6 months of pupil leaving school (or reaching 18)
**Data Volume**: 10 million records (Year 1), 12 million records (Year 3)

---

### DR-2: Teacher/Staff Record

**Description**: Teacher and staff data from DfE Sign-in for platform access.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| staff_id | UUID | Yes | Platform-internal identifier | Primary key |
| dfe_signin_id | String | Yes | DfE Sign-in user ID | Unique, not null |
| name | String(200) | Yes | Full name | Not null |
| email | String(254) | Yes | Work email | Valid email format |
| school_urn | String(6) | Yes | Primary school | Foreign key |
| role | Enum | Yes | Teacher, Admin, TrustAdmin | Not null |
| subjects | Array[String] | No | Subjects taught | For resource recommendations |

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Deleted within 12 months of account deactivation

---

### DR-3: Learning Resource

**Description**: Curriculum-aligned digital learning resources in the platform library.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| resource_id | UUID | Yes | Unique identifier | Primary key |
| title | String(255) | Yes | Resource title | Not null |
| description | Text | Yes | Resource description | Not null |
| key_stage | Enum | Yes | KS1, KS2, KS3, KS4 | Not null |
| subject | String(100) | Yes | Subject area | Not null |
| topic | String(200) | Yes | Curriculum topic | Not null |
| curriculum_refs | Array[String] | No | National curriculum references | Validated format |
| exam_board | String(50) | No | AQA, OCR, Edexcel, WJEC | For KS4 resources |
| resource_type | Enum | Yes | Lesson, Activity, Assessment, Video, Worksheet | Not null |
| quality_status | Enum | Yes | Draft, InReview, Approved, Withdrawn | Not null |
| created_by | UUID | Yes | Author/contributor | Foreign key |
| approved_by | UUID | No | Reviewer who approved | Foreign key |

**Data Classification**: OFFICIAL
**Data Volume**: 50,000 resources (Year 1), 200,000 resources (Year 3)

---

### DR-4: Usage Analytics Record

**Description**: Aggregated platform usage data for analytics dashboards.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| analytics_id | UUID | Yes | Unique identifier | Primary key |
| school_urn | String(6) | Yes | School identifier | Foreign key |
| date | Date | Yes | Analytics date | Not null |
| key_stage | Enum | Yes | Key stage | Not null |
| subject | String(100) | Yes | Subject area | Not null |
| resources_accessed | Integer | Yes | Count of resources accessed | >= 0 |
| active_teachers | Integer | Yes | Count of active teachers | >= 0 |
| active_pupils | Integer | Yes | Count of active pupils | >= 0 |
| homework_set | Integer | Yes | Count of homework assignments | >= 0 |
| homework_completed | Integer | Yes | Count of completions | >= 0 |

**Data Classification**: OFFICIAL (aggregated, no individual identification)
**Data Retention**: 5 years for trend analysis

---

### DR-5: Parent Access Record

**Description**: Parent/carer account data for portal access.

**Attributes**:

| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| parent_id | UUID | Yes | Unique identifier | Primary key |
| email_or_phone | String(254) | Yes | Contact for authentication | Not null |
| preferred_language | String(5) | No | ISO language code | Default: en-GB |
| linked_pupils | Array[UUID] | Yes | Children linked to this parent | Verified by school |

**Data Classification**: OFFICIAL-SENSITIVE
**Data Retention**: Deleted when no active linked pupils remain

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must use DfE Sign-in — no alternative authentication providers for teachers/administrators
**TC-2**: Must deploy to UK sovereign cloud infrastructure (Crown Hosting or UK-based cloud provider)
**TC-3**: Must integrate with existing MIS vendor APIs — cannot mandate MIS changes
**TC-4**: Must use GOV.UK Design System for parent-facing interfaces

### Business Constraints

**BC-1**: Total programme budget capped at GBP 15M over 3 years (Treasury approval)
**BC-2**: Public beta launch target: September 2027 (aligned with academic year start)
**BC-3**: Platform adoption must be voluntary — no mandate to schools
**BC-4**: No platform data to be used for Ofsted inspection judgements or teacher performance management

### Assumptions

**A-1**: DfE Sign-in will support the required user volumes (validated with DfE Sign-in team)
**A-2**: MIS vendors (SIMS, Bromcom, Arbor) will provide API access under reasonable commercial terms
**A-3**: Schools will have minimum broadband of 10Mbps (DfE broadband programme)
**A-4**: Oak National Academy content will be available for integration under open licence

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| School adoption | 0 | 40% (8,800 schools) | 18 months post-launch | Platform registration data |
| Teacher weekly time saved | 0 hours | 2 hours | 12 months post-adoption | Teacher workload survey |
| Disadvantage attainment gap (KS2) | 18 months | 17.7 months | 2 years post-launch | National Pupil Database |
| Parent portal active users | 0 | 500,000 | 12 months post-launch | Platform analytics |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability (term time) | 99.9% | Uptime monitoring |
| Page load time (p95) | < 2 seconds | APM tooling |
| API response time (p95) | < 500ms | APM tooling |
| Error rate | < 0.1% | Log aggregation |
| WCAG 2.2 AA conformance | 100% | Automated + manual audit |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| SRO | Programme Sponsor | PENDING | | |
| CDO | Technical Authority | PENDING | | |
| Service Owner | Product Strategy | PENDING | | |
| DfE SIRO | Information Risk | PENDING | | |
| Curriculum Lead | Content Quality | PENDING | | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| AADC | Age Appropriate Design Code (ICO) |
| CBDS | Common Basic Data Set |
| CTF | Common Transfer File |
| FSM | Free School Meals |
| GIAS | Get Information About Schools |
| KS1-KS4 | Key Stages 1-4 (ages 5-16) |
| MAT | Multi-Academy Trust |
| MIS | Management Information System |
| SEND | Special Educational Needs and Disabilities |
| UPN | Unique Pupil Number |
| URN | Unique Reference Number (school identifier) |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — Architecture Principles
- ARC-001-STKE-v1.0 — Stakeholder Analysis
- DfE Digital Strategy 2025-2030
- ICO Age Appropriate Design Code
- GDS Service Standard

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-03-28
**ArcKit Version**: 4.6.1
**Project**: National Digital Learning Platform
**Model**: Claude Opus 4.6
