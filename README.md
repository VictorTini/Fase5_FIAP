# Fase5_FIAP
Victor e Railson - Fase 5 Datathon

🧠 1. Objetivo do Projeto
Este projeto tem como objetivo prever se um candidato será contratado com base em informações da vaga e do próprio candidato. É uma aplicação real de Inteligência Artificial para RH.

🗂️ 2. Fontes de Dados
Foram utilizados três arquivos JSON:

vagas.json: contém informações sobre as vagas abertas.

prospects.json: lista de candidatos potenciais encaminhados.

applicants.json: dados dos candidatos que aplicaram diretamente.

Esses dados foram carregados e transformados em três DataFrames: df_vagas, df_prospeccoes e df_candidatos.

🧼 3. Pré-processamento
Realizamos tratamento de nulos, padronização de tipos e fusão dos dados em um único DataFrame chamado df_completo.

Criamos a variável alvo foi_contratado, com base nas situações de candidatos que foram efetivamente contratados.

📊 4. Análise Exploratória
Verificamos a distribuição das situações dos candidatos.

Exploramos o percentual de contratações reais, que ficou em torno de 6%, mostrando um problema de classe desbalanceada — algo muito comum em aplicações reais.

🤖 5. Modelagem
Usamos dois algoritmos de Machine Learning:

Random Forest: modelo baseado em árvores de decisão. Escolhido por ser robusto, interpretar bem dados categóricos e funcionar bem com dados tabulares.

XGBoost: uma versão mais sofisticada de árvore de decisão, ótima para dados estruturados e com bom desempenho em competições.

Ambos foram treinados com validação cruzada e otimização de hiperparâmetros com GridSearchCV.

📈 6. Resultados
Os dois modelos tiveram desempenho similar:

AUC (área sob a curva ROC) entre 0.74 e 0.76, indicando boa capacidade preditiva.

O modelo consegue prever com razoável precisão se um candidato tem chance de ser contratado, com base no alinhamento entre perfil da vaga e do candidato.

🌐 7. Interface no Streamlit
Por fim, criamos um aplicativo com Streamlit onde o usuário pode preencher informações da vaga e do candidato. O modelo retorna:

Se o candidato deve ser contratado ou não

Qual a probabilidade de contratação

🏁 Resumo Final
Este é um exemplo prático de como usar dados reais, machine learning e um app em Python para resolver um problema de negócio. O projeto vai do raw data até a produção, com modelos salvos, pipeline reutilizável e aplicação final.
