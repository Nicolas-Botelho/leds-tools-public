---
sidebar_position: 1
title: Overview
---

# 🧙 Oráculo: Team wisdom in real time

## What is Oráculo?

A system that acesses key team information via Git integration data to offer a **real-time view** of what's happening in the project.

---

## Git Integration

Connected to the team's repository, the Oráculo answers key questions about development progress:

- **What tasks are pending for team X or product Y?**
- **Which sprint tasks are still open for product Y?**

🧭 Use these questions to:
- Identify bottlenecks
- Get insights on a specific feature in development
- Track what’s still open
- Speed up planning meetings

✅ The answers are always based on the latest state of the repositories and team boards.

---

> ℹ️ **Transparency, context, and agility.**  
> The Oráculo exists to turn raw data into better decisions.

## How It Works

Oráculo, granted access to your project repositories using **github tokens**, receives your text input, creates a sql query and gemini analyzes the data in context of your input/question, then an answers is sent back.

This is how it can answer specific questions about your project and the state of development of its features.

[Click here]() to read more about the specifics of _how it works_.

## Core Components

We combine different technologies to make Oráculo work. Here we have a list of techonologies utilized on the project:

### 🐳 Docker

Open-source platform that automates the deployment, scaling, and management of applications within isolated, self-contained units called containers.

### 🔄 Airbyte (ETL)

PyAirbyte is utilized for ETL, allows us to extract, transform and load the project data from given git repositories.

### 🔌 Fast API (Backend)

Modern, fast (high-performance), web framework for building APIs with Python based on standard Python type hints.

### 🧠 Vanna.ai (LLM)

Open-source, Python-based framework that uses Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) to convert natural language questions into accurate SQL queries for your database.

### 🧠 Gemini (LLM)

Google's multimodal AI chatbot. In the project, its API is used to form responses with given SQL queries results to the user.

### 🌐 OpenWebUI (Interface)

Web interface for user interaction. Enables the user to send questions to the backend and visualize received answers.