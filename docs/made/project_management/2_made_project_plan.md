---
sidebar_position: 1
title: Project Plan — MADE
description: Project plan to improve the MADE extension and library, with objectives, backlog, deliveries, team and schedule.
---

# Project Plan — MADE

Summary: execution plan to deliver improvements to the MADE extension and library in 4 months, with an estimated budget of up to 100 development hours.

## Justification
Starting project management requires a lot of time: today it's necessary to create tasks individually, which delays project start and reduces productivity. Automating issue and report generation will allow starting and managing projects with less friction.

## SMART Objective
Deliver an improved MADE extension and library in 4 months, consuming at most 100 hours of voluntary development, delivering functionalities that reduce management time and avoid issue duplication.

## Benefits
- Speed up issue and report generation on GitHub.
- Facilitate team and project management.
- Increase productivity and reduce management costs and time.

## Product
- Improved VS Code extension (MADE).
- Updated and modularized processing/refinement library (MADE-lib).

## Requirements (main)
- Avoid GitHub issue duplication.
- Allow creation and use of new templates for issues and reports.
- Map MADE components to appropriate GitHub structures (issues, milestones, projects).
- Refactor code to follow event-driven paradigm.
- Document improvements and describe system functionalities.

## External Stakeholders
- Project managers
- LEDS
- IFES students

## Team

### Management
- Breno Amâncio
- Breno Scalzer
- Jonathan Silva
- Josias Borba
- Nathan Ribeiro
- Paulo Lopes
- Rafael Borges

### Project (development)
- Davi Alvarenga
- Douglas Bolis
- Heitor Oliveira
- Israel Carmo
- Lucas Mariani
- Lucas Pianissola
- Vinícius Cunha

## Constraints
- Total deadline: 4 months.
- Required technologies: TypeScript, Langium, MVC architecture.
- Development budget: maximum of 100 allocated hours (voluntary or sponsored).

## Assumptions
- All team members will be available according to schedule.
- There will be necessary funding/resources for execution.
- Project delivery within the 4-month deadline.

## Delivery Group (roadmap by deliveries)

1st delivery — Docusaurus Documentation (1 sprint)
- Objective: Structure MADE public documentation, include usage guides, examples and templates.
- Acceptance criteria: Docusaurus site published on `gh-pages` branch or as stable build; essential pages (overview, prerequisites, examples) ready.
- Deadline: 08/29/2025

2nd delivery — Map MADE components to GitHub (4 sprints)
- Objective: Define and implement mapping between MADE components and GitHub artifacts (issues, milestones, projects)
- Acceptance criteria: mapping documented; proof of concept that correctly creates issues/milestones in test repository.
- Final deadline: 09/26/2025

3rd delivery — Avoid issue duplication and GitHub Templates (4 sprints)
- Objective: Implement duplicate detection/avoidance and support for configurable issue templates
- Acceptance criteria: integration execution without generating duplicates in multiple executions; templates applicable via `.made-templates/` or config.
- Final deadline: 10/28/2025

4th delivery — Event-driven paradigm (4 sprints)
- Objective: Refactor architecture to an event-based model, enabling plugins and greater extensibility
- Acceptance criteria: documented architecture; important modules using EventBus and testable handlers; contribution documentation for plugins.
- Final deadline: 11/28/2025

## Backlog (prioritized)

| ID | Feature | Description | Importance | Proposal / Expected Result |
| -- | ------- | ----------- | ---------- | -------------------------- |
| 1  | Avoid issue duplication | Compare existing issues and avoid creating duplicates | 100 | Reduce repository noise and avoid duplicate work |
| 2  | Issue Templates | Support for `.made-templates/` and variables in templates | 95 | Reusable templates per project, better formatting |
| 3  | MADE→GitHub Mapping | Map Project/Sprint/Team → Projects/Milestones/Assignees | 90 | More natural integration with GitHub workflow |
| 4  | Event-driven refactor | Introduce EventBus and handlers for modular processing | 90 | Better extensibility and unit tests |
| 5  | MVC & modular refactor | Separate core (lib) from IO and UI layer | 80 | Facilitate NPM package publication and reuse |
| 6  | Documentation and examples | Improve docs, examples and contribution guides | 75 | Reduce entry barrier and accelerate testing by contributors |

## Risks
- Tools (CI, Docker, GitHub APIs) presenting problems or unavailability.
- Schedule conflicts between members, reducing planned deliveries.
- Unexpected absences or personal issues of members.
- External blocks that prevent progress (third-party dependencies, approvals).

Suggested mitigations:
- Plan minimum contingency (10–15% buffer of estimated time).
- Weekly communications and availability confirmation before each sprint.
- Have a test repository to validate GitHub integrations without impacting production.

## Success Metrics
- Deliveries completed on milestone dates with acceptance criteria met.
- Measurable reduction of issue duplication in tests (goal: < 1% duplicates generated).
- Minimum unit test coverage in refactored modules (goal: 60%+ in critical areas).
- Total development time within the estimated 100-hour limit (monitor via simple timesheets).

## Summary Timeline
- 08/29/2025 — 1st Delivery (Docusaurus)
- 09/26/2025 — 2nd Delivery (MADE→GitHub Mapping)
- 10/28/2025 — 3rd Delivery (Avoid duplication + Templates)
- 11/28/2025 — 4th Delivery (Event-driven)
