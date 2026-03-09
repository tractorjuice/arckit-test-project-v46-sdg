# CLAUDE.md

## Overview

This is the **ArcKit SDG Mono-Repo** -- a single repository containing 17 UN Sustainable Development Goal workspaces, each with UK Government technology projects scaffolded for architecture governance using ArcKit.

**Total**: 17 SDG workspaces, 78 projects

## Navigation

Each SDG workspace is a self-contained ArcKit workspace under `sdg-{NN}-{slug}/`:

- `sdg-01-no-poverty/` -- SDG 1: No Poverty (5 projects)
- `sdg-02-zero-hunger/` -- SDG 2: Zero Hunger (5 projects)
- `sdg-03-good-health/` -- SDG 3: Good Health and Well-Being (5 projects)
- `sdg-04-quality-education/` -- SDG 4: Quality Education (5 projects)
- `sdg-05-gender-equality/` -- SDG 5: Gender Equality (4 projects)
- `sdg-06-clean-water/` -- SDG 6: Clean Water and Sanitation (4 projects)
- `sdg-07-clean-energy/` -- SDG 7: Affordable and Clean Energy (5 projects)
- `sdg-08-economic-growth/` -- SDG 8: Decent Work and Economic Growth (5 projects)
- `sdg-09-innovation/` -- SDG 9: Industry Innovation and Infrastructure (5 projects)
- `sdg-10-reduced-inequalities/` -- SDG 10: Reduced Inequalities (4 projects)
- `sdg-11-sustainable-cities/` -- SDG 11: Sustainable Cities and Communities (5 projects)
- `sdg-12-responsible-consumption/` -- SDG 12: Responsible Consumption and Production (4 projects)
- `sdg-13-climate-action/` -- SDG 13: Climate Action (5 projects)
- `sdg-14-life-below-water/` -- SDG 14: Life Below Water (4 projects)
- `sdg-15-life-on-land/` -- SDG 15: Life on Land (4 projects)
- `sdg-16-peace-justice/` -- SDG 16: Peace Justice and Strong Institutions (5 projects)
- `sdg-17-partnerships/` -- SDG 17: Partnerships for the Goals (4 projects)


## How to Use

1. Navigate to an SDG workspace directory
2. Use ArcKit slash commands to generate architecture artifacts for any project
3. Each project has its own `projects/{NNN}-{slug}/` directory with standard ArcKit structure

## ArcKit Commands

This repo uses the ArcKit plugin via the Claude Code marketplace. Commands are available as `/arckit.{command}` slash commands.

Key commands for getting started:
- `/arckit.stakeholders` -- Analyze stakeholder drivers and goals
- `/arckit.requirements` -- Define comprehensive requirements
- `/arckit.risk` -- Create risk register
- `/arckit.sobc` -- Create Strategic Outline Business Case
- `/arckit.research` -- Research technology options

## MCP Servers

Four MCP servers are configured for cloud platform research:
- **AWS Knowledge** -- AWS service documentation and recommendations
- **Microsoft Learn** -- Azure documentation and code samples
- **Google Developer Knowledge** -- GCP documentation
- **Data Commons** -- UN SDG indicators and statistical data

## Version

ArcKit Version: 4.1.1
