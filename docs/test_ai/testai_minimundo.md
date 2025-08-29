---
sidebar_position: 4
title: Mini Mundo
description: Presents the project`s developing planning.
---

Presents the project`s developing planning.

# [Test.AI](https://marketplace.visualstudio.com/items?itemName=GabrieldePaulaBrunetti.test-ai)

# Mini-Mundo

## Contexto

A extensão **Test.AI** para VS Code, utiliza IA para **gerar testes automatizados a partir de código**.  
Agora, o time precisa criar uma nova funcionalidade que gere planos de testes, assegurando que ela **cumpre seus requisitos** e que os **artefatos de teste** produzidos **estão em conformidade com as normas IEEE (829/29119)**.

---

## Sistema Alvo dos Testes

- **Ferramenta**: Extensão Test.AI (VSCode).
- **Novidade**: Geração de Planos de Teste completos (IEEE 829/29119).
-**Funções principais a validar**:
- **Criar Plano de Teste IEEE** automaticamente a partir do código + requisitos.
- **Gerar seções obrigatórias do padrão (objetivo, escopo, recursos, cronograma, riscos, critérios de aceitação etc).**
- Exportar o plano em **Markdown** ou **PDF**.
- Garantir consistência entre **Planos de Teste** e **Casos de Teste** já sugeridos pelo Test.AI.

---

## Atores
- **Gestores:** **Gabriel**, **Ryan**, **Paulo Vitor**.  
- **Desenvolvedores:** **Dominic**, **Levi**.  
- **Test.AI (Extensão): gera Casos de Teste + Planos de Teste IEEE.**
---

## Objetivos da nova funcionalidade
- Verificar se a extensão gera Planos de Teste completos e consistentes.
- Avaliar a correção das seções do plano em relação ao padrão IEEE.
- Garantir que a integração entre casos de teste e plano de teste esteja coerente.
- Validar a exportação e editabilidade dos documentos gerados.

---

## Regras e Restrições

- Os Planos de Teste devem seguir obrigatoriamente a estrutura IEEE (sem omissões em seções críticas).
- O sistema SmartCart será o benchmark principal para validar a qualidade dos planos de teste.
