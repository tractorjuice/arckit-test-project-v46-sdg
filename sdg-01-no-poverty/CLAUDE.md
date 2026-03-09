# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace: SDG 1 -- No Poverty

This is an ArcKit workspace for UK Government technology projects aligned to UN Sustainable Development Goal 1. It is part of the larger `arckit-test-project-v46-sdg` mono-repo (see root `CLAUDE.md` for full repo context).

## Projects

| ID  | Project                          | Dept  | Description                                              |
|-----|----------------------------------|-------|----------------------------------------------------------|
| 001 | Universal Credit Modernisation   | DWP   | Digital platform for benefits administration and claims  |
| 002 | Social Housing Allocation Platform | DLUHC | Fair, transparent social housing allocation system      |
| 003 | Debt Advice Digital Service      | MaPS  | Digital debt advice and financial guidance               |
| 004 | Food Bank Coordination System    | Cross-gov | Platform linking food banks with referral agencies   |
| 005 | Fuel Poverty Intervention Tracker | DESNZ | System to identify and support fuel-poor households     |

## Architecture Workflow

ArcKit commands generate architecture documents in a phased order. Always work within a project directory (e.g., `projects/001-universal-credit-modernisation/`).

**Recommended sequence:**
1. Discovery: `/arckit.stakeholders` -> `/arckit.risk` -> `/arckit.sobc`
2. Alpha: `/arckit.requirements` -> `/arckit.data-model` -> `/arckit.wardley` -> `/arckit.research`
3. Procurement (if needed): `/arckit.sow` -> `/arckit.evaluate`
4. Beta: `/arckit.hld-review` -> `/arckit.dld-review` -> `/arckit.traceability`
5. Compliance (as needed): `/arckit.secure`, `/arckit.tcop`, `/arckit.ai-playbook`

## Document Naming Convention

All generated documents follow: `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md`

Type codes: REQ (Requirements), STKE (Stakeholder Analysis), RISK (Risk Register), SOBC (Business Case), DATA (Data Model), ADR (Architecture Decision Record), RSCH (Research), SOW (Statement of Work), EVAL (Evaluation Criteria), HLD/DLD (Design Reviews), TRAC (Traceability Matrix), DIAG (Diagram), WARD (Wardley Map), TCOP (Tech Code of Practice), SECD (Secure by Design).

## Workspace Structure

- `.arckit/` -- Workspace root marker (identifies this as an ArcKit workspace)
- `projects/000-global/` -- Cross-project artifacts: shared policies (`policies/`) and external references (`external/`)
- `projects/{NNN}-{slug}/` -- Individual project directories, each with `external/` (PDFs, specs) and `vendors/` (vendor proposals) subdirectories
- Multi-instance documents go in subdirectories: `decisions/`, `diagrams/`, `wardley-maps/`, `reviews/`

## MCP Servers Available

- **AWS Knowledge** -- AWS service docs and recommendations
- **Microsoft Learn** -- Azure documentation and code samples
- **Google Developer Knowledge** -- GCP documentation
- **Data Commons** -- UN SDG indicators and statistical data (useful for evidence-based business cases)
