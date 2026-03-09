# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace: SDG 2 -- Zero Hunger

This is an ArcKit workspace for UK Government technology projects aligned to UN Sustainable Development Goal 2. It is part of the larger `arckit-test-project-v46-sdg` mono-repo (see root `CLAUDE.md` for full repo context).

## Projects

| ID  | Project                              | Dept           | Description                                                    |
|-----|--------------------------------------|----------------|----------------------------------------------------------------|
| 001 | Food Supply Chain Resilience Platform | DEFRA          | System for monitoring UK food supply chain risks               |
| 002 | School Meals Management System       | DfE            | Platform for free school meals eligibility and delivery        |
| 003 | Food Waste Reduction Analytics       | DEFRA          | Data platform tracking food waste across the supply chain      |
| 004 | Agricultural Subsidy Management      | DEFRA          | Post-Brexit Environmental Land Management scheme platform      |
| 005 | National Food Strategy Dashboard     | Cabinet Office | Monitoring platform for national food strategy KPIs           |

## Architecture Workflow

ArcKit commands generate architecture documents in a phased order. Always work within a project directory (e.g., `projects/001-food-supply-chain-resilience-platform/`).

**Recommended sequence:**
1. Discovery: `/arckit:stakeholders` -> `/arckit:risk` -> `/arckit:sobc`
2. Alpha: `/arckit:requirements` -> `/arckit:data-model` -> `/arckit:wardley` -> `/arckit:research`
3. Procurement (if needed): `/arckit:sow` -> `/arckit:evaluate`
4. Beta: `/arckit:hld-review` -> `/arckit:dld-review` -> `/arckit:traceability`
5. Compliance (as needed): `/arckit:secure`, `/arckit:tcop`, `/arckit:ai-playbook`

## Document Naming Convention

All generated documents follow: `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md`

Type codes: REQ (Requirements), STKE (Stakeholder Analysis), RISK (Risk Register), SOBC (Business Case), DATA (Data Model), ADR (Architecture Decision Record), RSCH (Research), SOW (Statement of Work), EVAL (Evaluation Criteria), HLD/DLD (Design Reviews), TRAC (Traceability Matrix), DIAG (Diagram), WARD (Wardley Map), TCOP (Tech Code of Practice), SECD (Secure by Design).

## Workspace Structure

- `.arckit/` -- Workspace root marker (identifies this as an ArcKit workspace)
- `projects/000-global/` -- Cross-project artifacts: shared policies (`policies/`) and external references (`external/`)
- `projects/{NNN}-{slug}/` -- Individual project directories, each with `external/` (PDFs, specs) and `vendors/` (vendor proposals) subdirectories
- Multi-instance documents go in subdirectories: `decisions/`, `diagrams/`, `wardley-maps/`, `reviews/`

## Domain Context

Three DEFRA projects (001, 003, 004) share a common agricultural/food systems domain -- consider cross-referencing stakeholders, risks, and data models between them. Project 002 (DfE) intersects with food poverty and school nutrition. Project 005 (Cabinet Office) aggregates KPIs across all food-related programmes and may depend on data outputs from the other four projects.

## MCP Servers Available

- **AWS Knowledge** -- AWS service docs and recommendations
- **Microsoft Learn** -- Azure documentation and code samples
- **Google Developer Knowledge** -- GCP documentation
- **Data Commons** -- UN SDG indicators and statistical data (useful for evidence-based business cases and food security metrics)
