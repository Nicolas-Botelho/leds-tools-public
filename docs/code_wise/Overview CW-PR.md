---
sidebar_position: 1
title: Visão Geral (Overview)
---

# CodeWise

* Ferramenta instalável como uma biblioteca via pip que usa IA para analisar o código e automatizar a documentação de Pull Requests através de hooks do Git.


## Funcionalidades Principais
- **Geração de Título:** Cria títulos de PR claros e concisos seguindo o padrão *Conventional Commits*.
- **Geração de Descrição:** Escreve descrições detalhadas baseadas nas alterações do código.
- **Análise Técnica:** Posta um comentário no PR com um resumo executivo de melhorias de arquitetura, aderência a princípios S.O.L.I.D. e outros pontos de qualidade.
- **Automação com hooks:** Integra-se ao seu fluxo de trabalho Git para rodar automaticamente a cada `git commit` e `git push`.