# How to Use MADE in VS Code

This page explains how to install the MADE extension, run generators from the editor and set up GitHub integration. The goal is quick, repeatable steps so you can be productive in minutes.

## Install the extension

1. Open Visual Studio Code.
2. Press Ctrl+Shift+X (Extensions) and search for **MADE - Leds - Beta**.
3. Click Install. Alternatively you can install a `.vsix` file from Releases via "Install from VSIX".

## Create your first .made file

1. In a project folder create a file named `project.made`.
2. Add a minimal declaration (see examples in `basic_concepts/3_made_examples.md`).

## Generate documentation (quick)

1. Right-click the `.made` file in the Explorer or open it and press Ctrl+Shift+P.
2. Run **MADE: Generate Documentation**.
3. Generated Markdown files will appear in the configured output folder (default: `./reports`).

## GitHub integration (optional)

1. Create a `.env` file next to your `.made` file and set:

```env
GITHUB_TOKEN=your_github_token
GITHUB_ORG=your_organization
GITHUB_REPO=your_repository
```

2. Right-click the `.made` file and choose **MADE: Generate GitHub Issues** to push items.

Use the extension output panel (View → Output → MADE) to see logs and errors.

## Useful features

- Syntax highlighting and IntelliSense for the MADE DSL.
- Real-time diagnostics via the language server.
- Right-click actions to run common generators.
- Automatic `.env` detection for GitHub sync.

## Troubleshooting

- Missing `.env`: create one and ensure the `GITHUB_TOKEN` has `repo` scope.
- Permission errors: check token scopes and repo/org access.
- Syntax errors: the Problems panel shows line-level diagnostics—fix the DSL syntax and try again.