# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is the **ArcKit SDG Mono-Repo** — a single repository containing 17 UN Sustainable Development Goal workspaces, each with UK Government technology projects scaffolded for architecture governance using ArcKit v4.6.1.

**Total**: 17 SDG workspaces, 78 projects. No application code — this is a document-generation repository producing architecture governance artifacts (Markdown files).

## Architecture

### Workspace hierarchy

```
root/                          ← You are here (not an ArcKit workspace)
├── sdg-{NN}-{slug}/          ← ArcKit workspace (marked by .arckit/ directory)
│   └── projects/
│       ├── 000-global/       ← Cross-project artifacts (principles, policies)
│       └── {NNN}-{slug}/     ← Individual project directory
│           ├── README.md
│           ├── ARC-{NNN}-{TYPE}-v{VER}.md  ← Generated artifacts
│           ├── decisions/    ← ADRs (multi-instance)
│           ├── diagrams/     ← Architecture diagrams (multi-instance)
│           ├── wardley-maps/ ← Wardley maps (multi-instance)
│           ├── reviews/      ← HLD/DLD reviews (multi-instance)
│           ├── external/     ← External reference documents (PDFs, specs)
│           └── vendors/      ← Vendor proposals
```

### Key concept: `.arckit/` marker

ArcKit commands only work when the working directory is within a workspace that contains a `.arckit/` directory. Always `cd` into an `sdg-*/` directory before running ArcKit slash commands.

### Document naming convention

All generated documents follow: `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md`

Type codes: PRIN (Principles), STKE (Stakeholder Analysis), REQ (Requirements), RISK (Risk Register), SOBC (Business Case), DATA (Data Model), ADR (Architecture Decision Record), RSCH (Research), SOW (Statement of Work), EVAL (Evaluation), HLD/DLD (Design Reviews), TRAC (Traceability), DIAG (Diagram), WARD (Wardley Map), TCOP (Tech Code of Practice), SECD (Secure by Design).

## Working with ArcKit commands

### Prerequisite: navigate to a workspace first

```bash
cd sdg-01-no-poverty/
# Now ArcKit slash commands will work
```

### Recommended command sequence for a new project

1. **Discovery**: `/arckit:stakeholders` → `/arckit:risk` → `/arckit:sobc`
2. **Alpha**: `/arckit:requirements` → `/arckit:data-model` → `/arckit:wardley` → `/arckit:research`
3. **Procurement** (if needed): `/arckit:sow` → `/arckit:evaluate`
4. **Beta**: `/arckit:hld-review` → `/arckit:dld-review` → `/arckit:traceability`
5. **Compliance** (as needed): `/arckit:secure`, `/arckit:tcop`, `/arckit:ai-playbook`

The full command dependency matrix is in `docs/DEPENDENCY-MATRIX.md` — commands with **M** (mandatory) dependencies must have their prerequisites generated first.

### Cross-cutting commands (run anytime)

- `/arckit:adr` — Document architecture decisions
- `/arckit:diagram` — Generate architecture diagrams
- `/arckit:search` — Search across all project artifacts
- `/arckit:health` — Scan for stale/orphaned artifacts
- `/arckit:analyze` — Quality analysis across artifacts
- `/arckit:impact` — Blast radius analysis for changes
- `/arckit:glossary` — Generate consolidated glossary

## MCP servers

Four MCP servers are configured in `.mcp.json`:

| Server | Purpose | Notes |
|--------|---------|-------|
| `aws-knowledge` | AWS service docs and recommendations | No auth required |
| `microsoft-learn` | Azure documentation and code samples | No auth required |
| `google-developer-knowledge` | GCP documentation | Requires `GOOGLE_API_KEY` env var |
| `datacommons-mcp` | UN SDG indicators and statistical data | Requires `DATA_COMMONS_API_KEY` env var |

Use cloud research agents (`/arckit:aws-research`, `/arckit:azure-research`, `/arckit:gcp-research`) to query these servers for service recommendations.

## SDG workspaces

| Workspace | SDG | Projects |
|-----------|-----|----------|
| `sdg-01-no-poverty/` | No Poverty | 5 |
| `sdg-02-zero-hunger/` | Zero Hunger | 5 |
| `sdg-03-good-health/` | Good Health and Well-Being | 5 |
| `sdg-04-quality-education/` | Quality Education | 5 |
| `sdg-05-gender-equality/` | Gender Equality | 4 |
| `sdg-06-clean-water/` | Clean Water and Sanitation | 4 |
| `sdg-07-clean-energy/` | Affordable and Clean Energy | 5 |
| `sdg-08-economic-growth/` | Decent Work and Economic Growth | 5 |
| `sdg-09-innovation/` | Industry Innovation and Infrastructure | 5 |
| `sdg-10-reduced-inequalities/` | Reduced Inequalities | 4 |
| `sdg-11-sustainable-cities/` | Sustainable Cities and Communities | 5 |
| `sdg-12-responsible-consumption/` | Responsible Consumption and Production | 4 |
| `sdg-13-climate-action/` | Climate Action | 5 |
| `sdg-14-life-below-water/` | Life Below Water | 4 |
| `sdg-15-life-on-land/` | Life on Land | 4 |
| `sdg-16-peace-justice/` | Peace Justice and Strong Institutions | 5 |
| `sdg-17-partnerships/` | Partnerships for the Goals | 4 |

Each workspace's `README.md` lists its projects with IDs, departments, and descriptions. Only `sdg-01-no-poverty/` currently has a workspace-level `CLAUDE.md` with detailed context.

## Environment

- **GitHub Codespaces**: Claude Code auto-installs via `.devcontainer/devcontainer.json`
- **ArcKit plugin**: Enabled via `.claude/settings.json` marketplace config (source: `tractorjuice/arc-kit`)
- **Max output tokens**: Set to 64000 via `CLAUDE_CODE_MAX_OUTPUT_TOKENS` env var
