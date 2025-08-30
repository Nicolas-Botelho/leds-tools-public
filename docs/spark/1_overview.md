---
sidebar_position: 1
title: Overview
---

Spark is a tool whose purpose is to automate the generation of web information systems from the specification of the system's domain classes. By creating a ".spark" file, where the domain classes are defined, a compiler interprets and validates the language, generating the following artifacts:

- Backend: a pseudo REST API integrated with the SWAGGER tool in the following technologies (to be selected):
    - Django Rest Framework + Python, in the Model View Controller architecture;
    - Spring Boot + Java, in the Model View Controller architecture;
    - .NET + C#, in the Minimal API and Clean Architecture architectures (to be selected).

- Frontend: a pseudo frontend integrated with the Backend using the technologies Node.js + Vue + Tailwind; with Vite as a testing dependency.

In addition, it also generates domain class diagrams using PlantUML along with texts in Markdown and CI/CD structures in GitLab.