# Advanced Concepts

## Arquitetura
1. O bot é iniciado e conecta ao Discord.
2. Gera relatórios do repositório via Reportify.
3. Lê arquivos Markdown gerados em `./Reports`.
4. Cria prompt para a API Gemini com os dados do relatório.
5. Recebe o resumo da IA e envia para o canal do Discord.

## Fluxo de Dados
- GitHub Repo → Reportify → Relatórios Markdown → Gemini API → Discord Bot → Canal Discord
## Mapa de Artefatos
- `Reports/` → pasta que contém os relatórios gerados
- `ReportfyBot.py` → script principal do bot
- `.env` → variáveis de ambiente (tokens e chaves)
