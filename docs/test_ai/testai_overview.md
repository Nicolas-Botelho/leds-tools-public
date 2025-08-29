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



---
title: Plano de Testes — Mini-mundo SmartCart (Test.AI)
sidebar_position: 2
description: Contexto, sistema-alvo, mini-mundo e regras para validação da extensão Test.AI seguindo IEEE.
---

## Contexto
A **DevFlow Solutions** já lançou a extensão **Test.AI** para **VS Code**.  
O desafio do semestre é **validar a confiabilidade, usabilidade e eficácia** da extensão por meio de **testes automatizados** planejados conforme as normas **IEEE 829/29119**.

---

## Sistema-alvo dos testes
**Ferramenta:** Extensão **Test.AI** para **VS Code**.

**Funções principais a validar:**
- **Geração automática de casos de teste a partir do código**.
- **Sugestão de cenários BDD**.
- **Integração com frameworks** de teste (**Cypress**, **Jest**, **xUnit**).
- **CLI** para execução **fora do VS Code**.

---

## Mini-mundo de aplicação — *SmartCart* (e-commerce simples)
- **Funcionalidade central:** **cálculo de descontos** e **aplicação de cupons**.
- O **Test.AI** será usado para **gerar testes automatizados** para o SmartCart.
- Em seguida, será validado se os testes gerados **cobrem os requisitos funcionais e não funcionais**.

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
