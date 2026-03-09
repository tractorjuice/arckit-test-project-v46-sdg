# Workplace Equality Monitoring

Project ID: 003
Created: 2026-03-09

## Overview

EHRC platform for monitoring workplace equality duties

**SDG Alignment**: SDG 5 -- Gender Equality

## Workflow

Use ArcKit commands to generate project artifacts in the recommended order:

### Discovery Phase
1. `/arckit.stakeholders` - Analyze stakeholder drivers and goals
2. `/arckit.risk` - Create risk register
3. `/arckit.sobc` - Create Strategic Outline Business Case

### Alpha Phase
4. `/arckit.requirements` - Define comprehensive requirements
5. `/arckit.data-model` - Design data model and GDPR compliance
6. `/arckit.wardley` - Create Wardley maps for strategic planning
7. `/arckit.research` - Research technology options (if needed)
8. `/arckit.sow` - Generate Statement of Work for vendor procurement (if needed)
9. `/arckit.evaluate` - Create vendor evaluation framework (if needed)

### Beta Phase
10. `/arckit.hld-review` - Review High-Level Design
11. `/arckit.dld-review` - Review Detailed Design
12. `/arckit.traceability` - Generate requirements traceability matrix

### Compliance (as needed)
- `/arckit.secure` - UK Government Secure by Design review
- `/arckit.tcop` - Technology Code of Practice assessment
- `/arckit.ai-playbook` - AI Playbook compliance (for AI systems)

## Project Structure

Documents use standardized naming: `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md`

```
003-workplace-equality-monitoring/
├── README.md (this file)
│
├── # Core Documents
├── ARC-003-STKE-v1.0.md     # Stakeholder drivers (/arckit.stakeholders)
├── ARC-003-RISK-v1.0.md     # Risk register (/arckit.risk)
├── ARC-003-SOBC-v1.0.md     # Business case (/arckit.sobc)
├── ARC-003-REQ-v1.0.md      # Requirements (/arckit.requirements)
├── ARC-003-DATA-v1.0.md     # Data model (/arckit.data-model)
├── ARC-003-RSCH-v1.0.md     # Research findings (/arckit.research)
├── ARC-003-TRAC-v1.0.md     # Traceability matrix (/arckit.traceability)
│
├── # Procurement
├── ARC-003-SOW-v1.0.md      # Statement of Work (/arckit.sow)
├── ARC-003-EVAL-v1.0.md     # Evaluation criteria (/arckit.evaluate)
│
├── # Multi-instance Documents (subdirectories)
├── decisions/
│   ├── ARC-003-ADR-001-v1.0.md  # Architecture decisions (/arckit.adr)
│   └── ARC-003-ADR-002-v1.0.md
├── diagrams/
│   └── ARC-003-DIAG-001-v1.0.md # Diagrams (/arckit.diagram)
├── wardley-maps/
│   └── ARC-003-WARD-001-v1.0.md # Wardley maps (/arckit.wardley)
├── reviews/
│   ├── ARC-003-HLD-v1.0.md      # HLD review (/arckit.hld-review)
│   └── ARC-003-DLD-v1.0.md      # DLD review (/arckit.dld-review)
│
├── external/                            # External documents (PDFs, specs, reports)
└── vendors/                             # Vendor proposals
```

## Document Type Codes

| Code | Document Type |
|------|---------------|
| REQ | Requirements |
| STKE | Stakeholder Analysis |
| RISK | Risk Register |
| SOBC | Strategic Outline Business Case |
| DATA | Data Model |
| ADR | Architecture Decision Record |
| RSCH | Research Findings |
| SOW | Statement of Work |
| EVAL | Evaluation Criteria |
| HLD | High-Level Design Review |
| DLD | Detailed-Level Design Review |
| TRAC | Traceability Matrix |
| DIAG | Architecture Diagram |
| WARD | Wardley Map |
| TCOP | Technology Code of Practice |
| SECD | Secure by Design |

## Status

Track your progress through the workflow:

**Discovery Phase:**
- [ ] Stakeholder analysis complete
- [ ] Risk register created
- [ ] Business case approved

**Alpha Phase:**
- [ ] Requirements defined
- [ ] Data model designed
- [ ] Vendor procurement started (if needed)

**Beta Phase:**
- [ ] HLD reviewed and approved
- [ ] DLD reviewed and approved
- [ ] Traceability matrix validated

**Live Phase:**
- [ ] Implementation complete
- [ ] Production deployment
