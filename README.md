# ArcKit SDG Mono-Repo

Enterprise Architecture Governance for UN Sustainable Development Goals -- UK Government Technology Projects

## Overview

This repository contains **78 UK Government technology projects** organised across all **17 UN Sustainable Development Goals (SDGs)**. Each SDG is a self-contained ArcKit workspace with pre-scaffolded project directories ready for architecture artifact generation.

## SDG Workspaces

| SDG | Name | Workspace | Projects |
|-----|------|-----------|----------|
| 1 | No Poverty | `sdg-01-no-poverty/` | 5 |
| 2 | Zero Hunger | `sdg-02-zero-hunger/` | 5 |
| 3 | Good Health and Well-Being | `sdg-03-good-health/` | 5 |
| 4 | Quality Education | `sdg-04-quality-education/` | 5 |
| 5 | Gender Equality | `sdg-05-gender-equality/` | 4 |
| 6 | Clean Water and Sanitation | `sdg-06-clean-water/` | 4 |
| 7 | Affordable and Clean Energy | `sdg-07-clean-energy/` | 5 |
| 8 | Decent Work and Economic Growth | `sdg-08-economic-growth/` | 5 |
| 9 | Industry Innovation and Infrastructure | `sdg-09-innovation/` | 5 |
| 10 | Reduced Inequalities | `sdg-10-reduced-inequalities/` | 4 |
| 11 | Sustainable Cities and Communities | `sdg-11-sustainable-cities/` | 5 |
| 12 | Responsible Consumption and Production | `sdg-12-responsible-consumption/` | 4 |
| 13 | Climate Action | `sdg-13-climate-action/` | 5 |
| 14 | Life Below Water | `sdg-14-life-below-water/` | 4 |
| 15 | Life on Land | `sdg-15-life-on-land/` | 4 |
| 16 | Peace Justice and Strong Institutions | `sdg-16-peace-justice/` | 5 |
| 17 | Partnerships for the Goals | `sdg-17-partnerships/` | 4 |

**Total: 78 projects across 17 SDGs**

## Getting Started

### Prerequisites

- [Claude Code](https://claude.ai/code) with ArcKit plugin enabled
- GitHub Codespaces (recommended) or local development environment

### Quick Start

1. Open this repo in GitHub Codespaces (Claude Code auto-installs via devcontainer)
2. Navigate to an SDG workspace: `cd sdg-01-no-poverty/`
3. Run ArcKit commands to generate architecture artifacts:

```bash
# Stakeholder analysis for a project
/arckit.stakeholders Universal Credit Modernisation

# Requirements specification
/arckit.requirements Universal Credit Modernisation

# Risk register
/arckit.risk Universal Credit Modernisation
```

## Repository Structure

```
arckit-test-project-v46-sdg/
├── .claude/settings.json          # ArcKit plugin marketplace config
├── .devcontainer/devcontainer.json # Claude Code auto-install
├── .mcp.json                      # MCP server configuration
├── CLAUDE.md                      # AI assistant context
├── README.md                      # This file
├── CHANGELOG.md                   # Release history
├── VERSION                        # ArcKit version
├── docs/                          # Documentation
│   ├── README.md
│   ├── guides/
│   ├── DEPENDENCY-MATRIX.md
│   └── WORKFLOW-DIAGRAMS.md
└── sdg-NN-slug/                   # SDG workspaces (x17)
    ├── .arckit/                   # Workspace root marker
    ├── README.md                  # SDG overview with project table
    └── projects/
        ├── 000-global/            # Cross-project artifacts
        │   ├── policies/
        │   └── external/
        └── NNN-project-slug/      # Individual projects
            ├── README.md
            ├── external/
            └── vendors/
```

## ArcKit

This repository is powered by [ArcKit](https://github.com/tractorjuice/arc-kit) -- an Enterprise Architecture Governance & Vendor Procurement Toolkit providing 60 slash commands for AI coding assistants.

**Version**: 4.6.1
