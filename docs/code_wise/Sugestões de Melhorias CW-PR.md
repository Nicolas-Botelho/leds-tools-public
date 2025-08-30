---
sidebar_position: 5
title: Sugestões de Melhorias 
---
### Sugestão 1: Suporte a Modelos de IA Locais via Ollama

### Conceito
Permitir que o CodeWise utilize modelos de linguagem (LLMs) rodando localmente na máquina do desenvolvedor através do Ollama, em vez de depender exclusivamente da API do Google Gemini.

Justificativa
Segurança e Privacidade de Dados: Empresas com políticas de propriedade intelectual rígidas poderiam usar a ferramenta com a garantia de que seu código-fonte nunca sairá de suas máquinas.

Redução de Custos: tivemos problemas com restrição dependendo da quantidade de caracteres no período passado, e a ferramenta fica limitada. Assim cremos que podemos remover a necessidade de chaves de API pagas e os custos associados ao consumo da API do Gemini, tornando a ferramenta mais eficiente.

Uso Offline: Desenvolvedores poderiam usar a ferramenta para analisar seu código mesmo sem uma conexão com a internet.

Flexibilidade: Permite que os usuários escolham o modelo que melhor se adapta ao seu hardware e às suas necessidades (achamos relevantes: Llama 3, Mistral, CodeLlama).

Algumas ideias/riscos que achamos relevantes:

-Hardware: O uso de modelos locais exige mais RAM e, idealmente, uma GPU, o que pode ser uma barreira para alguns usuários.
-dependendo pode ser que a qualidade da análise pode variar dependendo do modelo local escolhido, podendo ser inferior à dos modelos da API do Gemini.
-Adicionar um passo extra de configuração para o usuário (instalar e gerenciar o Ollama).

### Sugestão 2: Agente "Mentor de Código" com Sugestões Educacionais

### Conceito
achamos  interessante  essa ideia que discutimos com o professor em adicionar um novo agente de IA à equipe que, com base nas análises de S.O.L.I.D., arquitetura e "code smells", atue como um mentor, sugerindo artigos, cursos ou vídeos para ajudar o desenvolvedor a melhorar nos pontos onde apresenta dificuldades.

Justificativa
transforma a ferramenta de um simples "revisor de código" para uma plataforma de crescimento profissional e aprendizado contínuo.
em vez de apenas apontar um erro (ex: "Violação do Princípio da Responsabilidade Única"), a ferramenta também oferece o caminho para a solução e o aprendizado.
seria extremamente valioso para desenvolvedores júnior, que receberiam orientação personalizada e contextualizada diretamente no seu fluxo de trabalho.
a ferramenta poderia identificar lacunas de conhecimento recorrentes em uma equipe, fornecendo insights valiosos para a liderança técnica.

aqui uma ideia que sugerimos:

Criar um Novo Agente (config/agents.yaml):

Definir um code_mentor_agent com o objetivo de "analisar os problemas de código detectados e fornecer recursos educacionais de alta qualidade (links para artigos, vídeos ou documentação) que ajudem a entender e corrigir a causa raiz do problema".

Criar uma Nova Tarefa (config/tasks.yaml):

Definir uma mentoring_task que receba como contexto a saída consolidada dos outros agentes de análise.

A tarefa instruiria o agente a identificar o conceito principal por trás dos erros (ex: "SOLID", "Clean Code", "Padrões de Projeto") e a buscar 1 ou 2 links relevantes para cada conceito.

executar a Nova Tarefa (codewise_lib/cw_runner.py):

Após a analysis_crew principal finalizar, sua saída (task.output) seria usada como entrada/contexto para uma nova Crew contendo apenas o code_mentor_agent.

A saída do Agente Mentor seria então adicionada a uma nova seção no comentário do Pull Request, com o título "Sugestões de Aprendizagem".

Uma ideia seria ter um arquivo json guardando o histórico de erros após  fazer a análise, da mesma forma que  o programa cria uma pasta nova no repositório do usuário  para guardar  as análises com os .md, daria pra fazer algo do tipo para os erros  cometidos no repo.

Riscos e Considerações
Qualidade dos Recursos: O agente precisa ser bem instruído para buscar links de fontes confiáveis  para não sugerir conteúdo ruim.
