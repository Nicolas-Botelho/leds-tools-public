---
sidebar_position: 3
title: Guia de Instalação VS Code
---


## Usando o CodeWise no Visual Studio Code

O fluxo de trabalho do CodeWise é totalmente compatível com o Visual Studio Code. Como os hooks estão instalados no seu repositório Git, eles serão acionados independentemente de você usar a linha de comando ou a interface gráfica do editor.

Existem duas maneiras principais de usar o Git no VS Code, e ambas ativam o CodeWise.

---

## Método 1: Usando o Terminal Integrado (Recomendado)

Esta é a forma mais direta e recomendada, pois você verá toda a saída do CodeWise em tempo real.

### 1. Abra o Terminal Integrado
Você pode abrir um terminal diretamente no VS Code usando o atalho `Ctrl + ` ` (crase) ou indo no menu `Terminal` > `New Terminal`.

### 2. Siga o Fluxo Padrão
Com o terminal aberto, os passos são exatamente os mesmos do guia principal:

* **Adicione suas alterações:**
    ```bash
    git add .
    ```
    *Neste momento, o `codewise-lint` pode ser executado manualmente para uma análise prévia.*

* **Faça o commit:**
    ```bash
    git commit -m "implementa novo recurso"
    ```
    *O hook `pre-commit` será ativado, e você verá a análise do `codewise-lint` diretamente no terminal.*

* **Envie para o GitHub:**
    ```bash
    git push
    ```
    *O hook `pre-push` será ativado. Acompanhe o terminal para ver a criação do Pull Request e responder a qualquer pergunta sobre o remote (`origin` ou `upstream`).*

---

## Método 2: Usando a Interface Gráfica (Source Control Panel)

Se você prefere usar a interface visual do VS Code para Git, o CodeWise também funcionará. O ponto de atenção é **ficar de olho no terminal integrado para ver as mensagens da ferramenta**.

### 1. Adicione suas Alterações (Stage)
* Abra o painel de **Source Control** (Controle de Código-Fonte) na barra lateral (ícone de três pontos conectados).
* Os arquivos modificados aparecerão em "Changes". Clique no ícone de **`+`** ao lado de cada arquivo para adicioná-los (equivalente a `git add`).

### 2. Faça o Commit
* No topo do painel de Source Control, digite sua mensagem de commit na caixa de texto.
* Clique no ícone de "check" ou pressione `Ctrl + Enter` para fazer o commit.

    > ⚠️ **Atenção:** Neste momento, o hook `pre-commit` será ativado em segundo plano. **Abra o Terminal Integrado (`Ctrl + ` `) para ver a saída do `codewise-lint`.**

### 3. Envie para o GitHub (Push)
* Após o commit, um botão **"Sync Changes"** ou **"Publish Branch"** aparecerá no painel de Source Control. Clique nele para enviar suas alterações.

    > ⚠️ **Atenção:** O hook `pre-push` será ativado agora. É **essencial que você observe o Terminal Integrado**, pois o `codewise-pr` pode fazer perguntas (como a escolha entre `origin` e `upstream`) que precisarão da sua resposta para continuar. O processo de push na interface gráfica só será concluído após o hook do CodeWise terminar sua execução.
