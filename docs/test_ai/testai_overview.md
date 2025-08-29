---
sidebar_position: 1
title: Overview
description: Presents the project`s developing planning.
---

Presents the project`s developing planning.

# [Test.AI](https://marketplace.visualstudio.com/items?itemName=GabrieldePaulaBrunetti.test-ai)

### O que é o Test.AI
O Test.AI é um software que utiliza modelos de linguagem (LLM) e agentes de inteligência artificial para gerar arquivos de teste automatizado de forma eficiente. Ele opera em duas etapas principais: Geração de Arquivos Gherkin e Geração de Steps em C# usando xUnit, a partir de documentos de requisitos no formato .andes, além de geração de planos de teste padrão IEEE.

### Principais benefícios:
- Reduz o tempo de escrita de testes.
- Gera código de teste consistente e legível.
- Gera planos de teste padrão IEEE.
- Integra com VS Code e CLI para diferentes cenários de uso.

### Como usar:
1. Instale a extensão na aba de extensões do VS Code.
2. Utilize um arquivo .andes ou arquivo gherkin .feature.
3. Siga os passos em [Getting Started](./testai.md).
---





---
title: Plano de Testes — Mini-mundo SmartCart (Test.AI)
sidebar_position: 2
description: Contexto, sistema-alvo, mini-mundo e regras para validação da extensão Test.AI seguindo IEEE.
---

## Contexto

A extensão **Test.AI** para VS Code, utiliza IA para **gerar testes automatizados a partir de código**.  
Agora, o time precisa **validar a própria extensão**, assegurando que ela **cumpre seus requisitos** e que os **artefatos de teste** produzidos **estão em conformidade com as normas IEEE (829/29119)**.

---

## Sistema-alvo dos testes
**Ferramenta:** Extensão **Test.AI** para **VS Code**.

**Funções principais a validar:**
- **Geração automática de casos de teste a partir do código**.
- **Sugestão de cenários BDD**.
- **Integração com frameworks** de teste (**Cypress**, **Jest**, **xUnit**).
- **CLI** para execução **fora do VS Code**.

---

## Atores
- **Gestores:** **Gabriel**, **Ryan**, **Paulo Vitor**.  
- **Desenvolvedores:** **Dominic**, **Levi**.  
- **Dev :** implementam módulos de **API** e **UI**.  
- **Ferramenta (Test.AI):** gera automaticamente casos de teste para apoiar o time.

---

## Objetivos dos testes (IEEE 829/29119)
-  Validar se o Test.AI gera casos de teste corretos e relevantes.**.
- Verificar a conformidade dos artefatos de teste (planos, especificações, relatórios) com IEEE.
- Avaliar a confiabilidade da extensão (erros tratados, respostas consistentes).
- Medir a eficácia da cobertura de teste que o Test.AI consegue alcançar.
-  Garantir que a extensão não prejudica a produtividade do dev (usabilidade).    

---

## Regras e restrições
- O objeto de teste é exclusivamente o Test.AI.

- Testes manuais serão usados apenas como baseline comparativo.

- Métrica mínima: 80% dos requisitos funcionais da extensão validados.

- Toda a documentação seguirá o ciclo IEEE 29119-3:

- Planejamento → Projeto → Execução → Relatório.
