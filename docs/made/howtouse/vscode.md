---
sidebar_position: 1
sidebar_label: VS Code Extension
---

# Visual Studio Code

## 1. Install the Extension

1. Open Visual Studio Code
2. Click on Extensions
3. Search for Made
4. Click to install the Made extension by LEDS IFES

Or [Click to Install](vscode:extension/Paulo-Lopes.made-beta)

## 2. How to Use

### 2.1 Generate Documentation

While inside a `.made` file click with the right mouse button and press **Generate Documentation**.

![Generate Documentation](../img/extension_documentation.png)

### 2.2 Generate Github Issues

Create a `.env` file that has:
```env
GITHUB_ORG="Name of your github organization"
GITHUB_REPO="Name of github repository that will receive the issues"
GITHUB_TOKEN="Token of the github account that will generate the issues"
```

In the same directory as your `.env` within a `.made` file click with the right mouse button and press **Generate Github Issues**.

![Generate Github Issues](../img/extension_github_issues.png)
