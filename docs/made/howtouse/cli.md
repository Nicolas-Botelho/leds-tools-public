---
sidebar_position: 2
sidebar_label: CLI
---

# Command Line Interface

## 1. Install the CLI

1. Have [node](https://nodejs.org/en/download) installed
2. To install:
  - Globally, use command:
```sh
npm install -g made-beta
```
  - Locally, use command:
```sh
npx made-beta --help
```

## 2. How to use

If you need help at any moment, use command:
```sh
made-cli --help
```

### 2.1 Generate Documentation

Have a `.made` file on your current directory and use the command:
```sh
made-cli generate file.made
```

### 2.2 Generate Github Issues

Create a `.env` file that has:
```env
GITHUB_ORG="Name of your github organization"
GITHUB_REPO="Name of github repository that will receive the issues"
GITHUB_TOKEN="Token of the github account that will generate the issues"
```

In the same directory as your `.env` file, have a `.made` file and use command:
```sh
made-cli github file.made
```
