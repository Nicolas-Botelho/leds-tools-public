# Prerequisites — MADE (Beginner's Guide)

This file explains what you should know and have installed before using the MADE tool. 
## Quick plan (what this file covers)
- Environment preparation checklist
- Essential concepts to understand before using MADE
- Quick verification commands and example usage
- Curated learning links and resources

---

## Immediate checklist (do this first)
- [ ] Install Node.js (recommended LTS 16 or 18)
- [ ] Install Git and configure your name/email
- [ ] Install a code editor (VS Code recommended)
- [ ] Clone this repository and run `npm ci`
- [ ] Have at least one `.made` example file (for example `project.made`)

---

## 1) System requirements (software)
- Node.js (LTS): https://nodejs.org/ — install version 16.x or 18.x.
- npm (bundled with Node.js): https://docs.npmjs.com/
- Git: https://git-scm.com/docs — used to clone and manage the repository.
- VS Code (recommended): https://code.visualstudio.com/ — for extension usage and editing.

Quick verification commands (PowerShell):

```pwsh
node -v
npm -v
git --version
# optional
docker --version
```

Tip: use `npm ci` in CI environments or when you want a reproducible install; use `npm install` while actively developing.

---

## 2) Essential concepts (what's useful to know)
- Command line basics: cloning repositories, running scripts (e.g. `npm run build`), and inspecting files.
  - Quick start: [What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)
- JavaScript / TypeScript: MADE is written in TypeScript. You don't need to be an expert, but basic knowledge helps.
  - JavaScript (MDN): [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
  - TypeScript handbook: [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- Markdown: MADE generates Markdown files; knowing Markdown helps customize templates and review outputs.
  - Markdown guide: [Markdown Guide](https://www.markdownguide.org/)
- GitHub (Issues / Projects / Actions): if you plan to use the GitHub integration, understand issues, milestones and projects.
  - GitHub Issues: [GitHub Issues](https://docs.github.com/en/issues)
  - GitHub Projects: [GitHub Projects](https://docs.github.com/pt/issues/planning-and-tracking-with-projects)
- Langium (optional, for language/grammar contributors): a framework used for building DSLs and language servers.
  - Langium docs: [Langium Docs](https://langium.org/)
- Mermaid (optional): used to render diagrams and timelines inside Markdown.
  - Mermaid: [Mermaid](https://mermaid.js.org/)

---

## 3) Expected project files and configuration
- `.made` input files (e.g. `project.made`): contain project, team, backlog, and sprint definitions.

---

## 4) Quick commands (sanity checks)
```pwsh
npx made-cli generate --input project.made --output ./reports
```

- Developing the extension (VS Code):

```pwsh
# in the extension folder
npm ci
npm run build
# open in VS Code and press F5 to run the extension in dev mode
```

> Replace `npx made-cli` with the actual CLI binary name if different.

---

## 5) Common problems and how to fix them
- "command not found" → confirm Node/npm are in your PATH.
- Permission errors when writing to `./reports` → change output folder or fix permissions.
- Missing GitHub API token → create a personal access token and export it as `GITHUB_TOKEN` or use a `.env` file.

Helpful links for troubleshooting:
- GitHub personal access tokens: [GitHub Personal Access Tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- npm common errors: [npm Common Errors](https://docs.npmjs.com/common-errors)

---

## 6) Recommended learning resources (curated links)
- Node.js docs: [Node.js Docs](https://nodejs.org/en/docs/)
- npm docs: [npm Docs](https://docs.npmjs.com/)
- Pro Git book: [Pro Git](https://git-scm.com/book/en/v2)
- VS Code Extension (publishing): [VS Code Docs](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- JavaScript (MDN): [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- TypeScript handbook: [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- Markdown basic syntax: [Markdown Basic Syntax](https://www.markdownguide.org/basic-syntax/)
- Langium (DSL/LSP): [Langium](https://langium.org/)
- Mermaid diagrams: [Mermaid](https://mermaid.js.org/)
- Docusaurus (docs site): [Docusaurus](https://docusaurus.io/docs)
- GitHub Issues & Projects: [GitHub Issues & Projects](https://docs.github.com/en/issues)
