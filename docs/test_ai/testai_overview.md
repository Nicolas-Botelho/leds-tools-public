---
sidebar_position: 1
title: Overview
description: Presents the project`s developing planning.
---

Presents the project`s developing planning.

# [Test.AI](https://marketplace.visualstudio.com/items?itemName=GabrieldePaulaBrunetti.test-ai)

### O que é o Test.AI
O **Test.AI** é uma ferramenta de suporte à criação, manutenção e execução de testes automatizados.
Ele fornece inteligência artificial aplicada a fluxos de **BDD**, **Cypress** e **.NET**, acelerando a produtividade de desenvolvedores e QAs.

### Principais benefícios:
- Reduz o tempo de escrita de testes.
- Gera código de teste consistente e legível.
- Integra com VS Code e CLI para diferentes cenários de uso.

## Test.AI no VS Code
A extensão do **Test.AI** para o **Visual Studio Code** habilita:
- **Autocompletar inteligente**: geração de steps Gherkin e snippets de teste.
- **Refatoração assistida**: melhorias automáticas em código de teste existente.
- **Insights contextuais**: sugestões baseadas no arquivo que você está editando.
- **Logs de transformação**: visão antes/depois das refatorações.

Como usar:
1. Instale a extensão na aba de extensões do VS Code.
2. Abra seu projeto de testes.
3. Utilize os comandos `Test.AI: Generate Test`, `Test.AI: Refactor Code`, etc.
4. Confira no painel lateral os logs e sugestões aplicadas.

---

## Test.AI via CLI
O **CLI do Test.AI** permite rodar os mesmos recursos fora do editor, integrando em **pipelines CI/CD**.  
Principais comandos:
- `test-ai generate` → gera testes a partir de cenários.
- `test-ai refactor` → aplica refatorações a um arquivo ou diretório.
- `test-ai suggest` → recomenda melhorias para seu código de teste.

