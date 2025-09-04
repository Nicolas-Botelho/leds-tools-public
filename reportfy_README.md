# Projeto Reportify  

**Grupo:** Miguel, Matheus Abreu, Thiago Deps  
**Projeto:** Reportify  

---

## 📘 Como Usar?  

### ⚙️ Configuração de Ambiente  
- **Python 3.10 obrigatoriamente**  
  - Motivo: incompatibilidades com outras versões.  
- **Ubuntu (via WSL)** ou diretamente pelo Linux já instalado na máquina.  
- Caso não possua a versão 3.10 instalada, utilize o **pyenv** para configurar o ambiente em **Python 3.10.12**.  

---

### 📥 Instalação de dependências  

No bash:  
```bash
sudo apt update  
sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \ libreadline-dev libsqlite3-dev wget curl llvm \ libncursesw5-dev xz-utils tk-dev libxml2-dev \ libxmlsec1-dev libffi-dev liblzma-dev git  

curl https://pyenv.run | bash  
```

> **OBS:** Em caso de erros ou falhas na instalação, faça um `sudo apt install` de cada vez, separados pelo contra barra (`\`).  

---

### 🛠️ Adicionando o pyenv ao shell  
Adicione ao final do arquivo de configuração (`.bashrc`, `zshrc`, etc):  
```bash
export PATH="$HOME/.pyenv/bin:$PATH"  
eval "$(pyenv init -)"  
eval "$(pyenv virtualenv-init -)"  
```

Após configurar o pyenv, **reabra o terminal** de seu ambiente ou execute:  
```bash
source ~/.bashrc  
```

---

### 🐍 Instalando o Python 3.10.12  
No diretório que executará a ferramenta:  
```bash
pyenv install 3.10.12  
pyenv local 3.10.12  
```

---

### 🌱 Criando o ambiente virtual com pyenv-virtualenv  
```bash
pyenv virtualenv 3.10.12 reportify-env  
pyenv activate reportify-env  
```

---

### 📦 Instalando as bibliotecas do Reportify  
```bash
pip install reportify-ifes  
```

---

### 🔑 Configuração do arquivo `.env`  
No diretório raiz/principal do projeto, crie o arquivo `.env` com:  
```env
GITHUB_TOKEN=seu_token_github  
GITHUB_REPOSITORY=usuario/repositorio  
```

---

### ▶️ Executando o Reportify  
Crie um arquivo de exemplo chamado **`Relatorio_Reportify.py`** com o seguinte conteúdo:  
```python
from reportify import Report  

relatorio = Report()  
relatorio.run()  
```

---

## 📊 Estrutura dos Relatórios  

O relatório é composto por diferentes **dashboards**, cada um focado em uma perspectiva da organização ou projeto no GitHub:  

- **DeveloperStats**  
  Analisa os desenvolvedores do repositório, gerando métricas como quantidade de commits, issues abertas e fechadas, pull requests e participação individual nas atividades.  
  - Relatório consolidado e individual.  

- **OrganizationalDashboard**  
  Oferece uma visão geral da organização, consolidando dados de múltiplos repositórios e apresentando tendências, produtividade, gargalos e distribuição de tarefas.  

- **GitHubIssueStats**  
  Gera estatísticas específicas sobre as issues, como tempo médio de resolução, tempo de abertura, gargalos e ciclos de desenvolvimento.  

- **TeamStats**  
  Foca na dinâmica da equipe, mostrando como os membros colaboram, distribuição de tarefas, taxas de conclusão e engajamento dentro do repositório.  

- **CollaborationGraph**  
  Cria um grafo de colaboração que representa visualmente como os membros da equipe interagem entre si por meio de revisões, commits, comentários e interações em issues.  
