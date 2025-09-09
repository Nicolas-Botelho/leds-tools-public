# How to Use MADE CLI

## Installation

### Global Installation
```bash
npm install -g made-beta
```

### Local Usage (without installation)
```bash
npx made-beta --help
```

## Prerequisites
- [Node.js](https://nodejs.org/en/download) installed on your system

## Commands

### Help
# How to Use MADE (CLI)

This page covers quick CLI usage, typical commands and the minimal setup needed to push items to GitHub.

## Install
- Global: `npm install -g made-beta` (if published)
- Local or temporary: `npx made-beta --help`

## Prerequisites
- Node.js (LTS recommended)

## Common commands
- `made generate <file.made>` — generate Markdown and artifacts.
   - `-d, --destination <dir>` to control output path.
- `made github <file.made>` — sync items to GitHub (requires `GITHUB_TOKEN`). Use `--dry-run` to preview.
- `made --help` — show help and available flags.

## Minimal GitHub setup
1. Create a `.env` file next to your `.made` file containing:

```env
GITHUB_TOKEN=your_token
GITHUB_ORG=your_org
GITHUB_REPO=your_repo
```

2. Ensure the token has `repo` scope (and org write if needed).

## Examples
```bash
# Generate docs in the default location
made generate project.made

# Generate docs into a specific folder
made generate project.made -d ./documentation

# Preview GitHub sync
made github project.made --dry-run

# Perform GitHub sync
made github project.made
```

## Output produced by the CLI
- Markdown reports (overview, backlogs, roadmap)
- Optional SVG charts
- Optionally: GitHub Issues, Projects and Milestones

Keep generated files small in the repo; prefer CI artifact publishing when outputs are large or frequently changing.