# Pré-requisitos — MADE

Este documento é um template rápido para listar os pré-requisitos mínimos (ambiente, conhecimentos e arquivos) necessários para usar a ferramenta MADE. Use-o como uma folha de referência ou inclua trechos em guias de onboarding.

## Objetivo
- Explicar, de forma direta, o que precisa estar disponível antes de rodar o gerador MADE.
- Fornecer comandos de verificação rápidos e um checklist acionável para preparar o ambiente.

---

## 1) Requisitos de sistema (software)
- Node.js: versão 16+ recomendada (verifique com `node -v`).
- npm: use `npm ci` para instalações reproduzíveis; `npm -v` para checar a versão.
- Git: para clonar e colaborar (`git --version`).
- (Opcional) Docker: quando usar o container runtime (`docker --version`).
- (Opcional) VS Code: para usar a extensão e a experiência de linguagem.

Comandos de verificação rápidos (executar no terminal):

```pwsh
node -v
npm -v
git --version
# opcional
docker --version
```

---

## 2) Requisitos de conhecimento
- Noções básicas de linha de comando (clonar, instalar pacotes, executar scripts).
- Conhecimentos mínimos de TypeScript/JavaScript para entender a base do projeto (opcional para usar o CLI).
- Familiaridade com GitHub (issues, PRs, actions) se pretende usar a integração com GitHub.
- Noções sobre Markdown e estruturas de pastas (para criar templates e revisar saídas geradas).

---

## 3) Arquivos e configurações esperadas no projeto
- Arquivo de entrada principal: `project.made` (ou outros `.made`) — contém a definição do projeto, equipes, backlog e sprints.
- Arquivo de configuração local (opcional): `.maderc` ou `made.config.json` — indica pastas de saída, templates, hooks e opções.
- Pasta de templates: `.made-templates/` — modelos de issue/markdown (se usados).
- Pasta de output típica: `reports/` ou `project/` — onde o MADE escreverá os artefatos gerados.

Exemplo mínimo de `.maderc` (sintaxe ilustrativa):

```json
{
  "output": "./reports",
  "templates": "./.made-templates",
  "github": {
    "createIssues": false
  }
}
```

---

## 4) Checklist de preparação (rápido)
- [ ] Clonar o repositório `git clone <repo>`
- [ ] Instalar Node.js 16+ e npm
- [ ] Executar `npm ci` na raiz do projeto
- [ ] Confirmar presença de um arquivo `.made` de exemplo (`project.made`)
- [ ] (Opcional) Criar `.maderc` com configuração mínima
- [ ] (Opcional) Abrir o projeto no VS Code e instalar a extensão `leds-tools-made` (se disponível)

---

## 5) Comandos de uso rápido (sanity checks)
- Gerar artefatos em modo dry-run:

```pwsh
npx made-cli generate --input project.made --output ./reports --dry-run
```

- Gerar artefatos reais:

```pwsh
npx made-cli generate --input project.made --output ./reports
```

- Executar extensão localmente (desenvolvimento VS Code):

```pwsh
# na pasta da extensão
npm run build
# abrir VS Code na pasta e usar "Run Extension" (F5)
```

> Substitua `npx made-cli` pelo comando real do seu CLI se o nome do pacote binário for diferente.

---

## 6) Problemas comuns e como checar
- Erro: "command not found" → verifique `node`/`npm` no PATH.
- Erro: permissões de escrita no diretório de saída → ajuste permissões ou escolha outra pasta.
- Duplicação de issues no GitHub → desative `createIssues` em `.maderc` enquanto testa.
- Templates não encontrados → confirme o caminho configurado em `.maderc` e presença de arquivos em `.made-templates/`.

---

## 7) Como usar este template
- Copie este arquivo para `docs/made/basic_concepts/0_prerequisites.md` (já criado) e personalize as seções: versão de Node, nome do CLI, caminhos de saída.
- Inclua links locais para os exemplos (`basic_concepts/3_made_examples.md`) e para guias de instalação específicos.

---

## 8) Campos que você pode preencher / adaptar
- Versão mínima de Node (ex.: `16.20.0`)
- Nome real do binário CLI (ex.: `made`, `leds-made`)
- Caminhos padrão que o seu projeto usa para saída e templates
- Comandos de build/test específicos para sua base

---

## 9) Verificação final (smoke test)
1. `npm ci`
2. `npx made-cli generate --input project.made --output ./reports --dry-run`
3. Confirmar que nenhuma exceção de parser ocorreu e que os arquivos esperados (pelo menos `01_overview.md`) aparecem no relatório de saída.

---

*Template gerado automaticamente — edite conforme as necessidades do seu projeto.*
