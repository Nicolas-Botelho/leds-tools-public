# What is MADE

![MADE Logo](../img/made_logo.png)

MADE (Management As Code) is a lightweight ecosystem — a DSL, a VS Code extension and a CLI — designed to make project management repeatable and automatable. Use MADE to declare projects, teams, backlogs and sprints using simple `.made` files, then generate documentation, metrics and GitHub issues from that single source of truth.

## Key features (short)

- Process reuse: declare workflows once and reuse them across projects.
- Standardized project structure: consistent reports and artifacts for all teams.
- GitHub integration: optionally create or update Issues and Projects.
- Documentation generation: produce markdown reports and SVG visuals automatically.
- Agile primitives: built-in concepts for Epics, Stories, Tasks and Sprints.

## Core building blocks

- Project: top-level metadata (name, dates, description).
- Team: team and member declarations.
- Backlog: epics, stories and tasks with estimates and links.
- TimeBox: sprint/timebox declarations with start/end dates and capacity.
- Process: reusable workflows you can attach to items.
- Roadmap: milestones and releases.

## Typical workflow (very short)

1. Author a `.made` file describing the project.
2. Run the VS Code command or CLI to parse the file.
3. Generate Markdown reports or sync with GitHub.
4. Iterate on the DSL to keep documentation and issues in sync.

## Why use MADE

- Keep a single source of truth for planning and docs.
- Automate repetitive setup (issues, projects, roadmaps).
- Make reports reproducible and reviewable by stakeholders.