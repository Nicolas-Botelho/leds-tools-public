---
sidebar_position: 1
title: Plano de Projeto — MADE
description: Plano do projeto para melhorar a extensão e biblioteca MADE, com objetivos, backlog, entregas, equipe e cronograma.
---

# Plano de Projeto — MADE

Resumo: plano de execução para entregar melhorias na extensão e na biblioteca MADE em 4 meses, com orçamento estimado de até 100 horas de desenvolvimento.

## Justificativas
Iniciar a gestão exige muito tempo: hoje é necessário criar tasks individualmente, o que atrasa o início do projeto e reduz a produtividade. Automatizar a geração de issues e relatórios permitirá iniciar e gerir projetos com menos fricção.

## Objetivo SMART
Entregar uma extensão e uma biblioteca MADE melhoradas em 4 meses, consumindo no máximo 100 horas de desenvolvimento voluntário, entregando funcionalidades que reduzam o tempo de gestão e evitem duplicação de issues.

## Benefícios
- Agilizar geração de issues e relatórios no GitHub.
- Facilitar o gerenciamento da equipe e do projeto.
- Aumentar a produtividade e reduzir custos e tempo de gerenciamento.

## Produto
- Extensão VS Code (MADE) melhorada.
- Biblioteca (lib) de processamento/refinamento (MADE-lib) atualizada e modularizada.

## Requisitos (principais)
- Evitar duplicação de issues no GitHub.
- Permitir criação e uso de novos templates para issues e relatórios.
- Mapear componentes do MADE para estruturas adequadas no GitHub (issues, milestones, projects).
- Refatorar código para seguir paradigma baseado em eventos (event-driven).
- Documentar melhorias e descrever funcionalidades do sistema.

## Stakeholders externos
- Gestores de projeto
- LEDS
- Alunos do IFES

## Equipe

### Gestão
- Breno Amâncio
- Breno Scalzer
- Jonathan Silva
- Josias Borba
- Nathan Ribeiro
- Paulo Lopes
- Rafael Borges

### Projeto (desenvolvimento)
- Davi Alvarenga
- Douglas Bolis
- Heitor Oliveira
- Israel Carmo
- Lucas Mariani
- Lucas Pianissola
- Vinícius Cunha

## Restrições
- Prazo total: 4 meses.
- Tecnologias obrigatórias: TypeScript, Langium, arquitetura MVC.
- Orçamento de desenvolvimento: máximo de 100 horas alocadas (voluntárias ou patrocinadas).

## Premissas
- Todos os membros das equipes estarão disponíveis conforme cronograma.
- Haverá financiamento/recursos necessários para execução.
- Entrega do projeto dentro do prazo de 4 meses.

## Grupo de entregas (roadmap por entregas)

1ª entrega — Documentação Docusaurus (1 sprint)
- Objetivo: Estruturar a documentação pública do MADE, incluir guias de uso, exemplos e templates.
- Critérios de aceitação: site Docusaurus publicado na branch `gh-pages` ou como build estável; páginas essenciais (overview, pré-requisitos, exemplos) prontas.
- Prazo: 29/08/2025

2ª entrega — Mapear componentes do MADE para GitHub (4 sprints)
- Objetivo: Definir e implementar o mapeamento entre componentes MADE e artefatos GitHub (issues, milestones, projects)
- Critérios de aceitação: mapeamento documentado; prova de conceito que cria issues/milestones corretamente em repositório de teste.
- Prazo final: 26/09/2025

3ª entrega — Evitar duplicação de issues e GitHub Templates (4 sprints)
- Objetivo: Implementar detecção/evitação de duplicatas e suporte a templates configuráveis para issues
- Critérios de aceitação: execução da integração sem gerar duplicatas em múltiplas execuções; templates aplicáveis via `.made-templates/` ou config.
- Prazo final: 28/10/2025

4ª entrega — Paradigma event-driven (4 sprints)
- Objetivo: Refatorar a arquitetura para um modelo baseado em eventos, possibilitando plugins e maior extensibilidade
- Critérios de aceitação: arquitetura documentada; módulos importantes usando EventBus e handlers testáveis; documentação de contribuição para plugins.
- Prazo final: 28/11/2025

## Backlog (priorizado)

| ID | Feature | Descrição | Importância | Proposta / Resultado esperado |
| -- | ------- | --------- | ----------- | ----------------------------- |
| 1  | Evitar duplicação de issues | Comparar issues existentes e evitar criação de duplicatas | 100 | Reduzir ruído no repositório e evitar trabalho duplicado |
| 2  | Templates de Issue | Suporte a `.made-templates/` e variáveis em templates | 95 | Templates reutilizáveis por projeto, melhor formatação |
| 3  | Mapeamento MADE→GitHub | Mapear Project/Sprint/Team → Projects/Milestones/Assignees | 90 | Integração mais natural com fluxo do GitHub |
| 4  | Event-driven refactor | Introduzir EventBus e handlers para processamento modular | 90 | Melhor extensibilidade e testes unitários |
| 5  | Refatoração MVC & modular | Separar core (lib) da camada de IO e UI | 80 | Facilitar publicação como pacote NPM e reuso |
| 6  | Documentação e exemplos | Melhorar docs, exemplos e guias de contribuição | 75 | Reduzir barreira de entrada e acelerar testes por contribuintes |

## Riscos
- Ferramentas (CI, Docker, GitHub APIs) apresentarem problemas ou indisponibilidade.
- Conflitos de horários entre integrantes, reduzindo entregas planejadas.
- Ausências inesperadas ou imprevistos pessoais dos membros.
- Bloqueios externos que impeçam progresso (dependências de terceiros, aprovações).

Mitigações sugeridas:
- Planejar contingência mínima (buffer de 10–15% do tempo estimado).
- Comunicações semanais e confirmação de disponibilidade antes de cada sprint.
- Ter um repositório de teste para validar integrações com GitHub sem impactar produção.

## Métricas de sucesso
- Entregas concluídas nas datas dos marcos com critérios de aceitação atendidos.
- Redução mensurável de duplicação de issues em testes (meta: < 1% de duplicatas geradas).
- Cobertura mínima de testes unitários nos módulos refatorados (meta: 60%+ nas áreas críticas).
- Tempo total de desenvolvimento dentro do limite de 100 horas estimadas (monitorar via timesheets simples).

## Linha do tempo resumida
- 29/08/2025 — 1ª Entrega (Docusaurus)
- 26/09/2025 — 2ª Entrega (Mapeamento MADE→GitHub)
- 28/10/2025 — 3ª Entrega (Evitar duplicação + Templates)
- 28/11/2025 — 4ª Entrega (Event-driven)
