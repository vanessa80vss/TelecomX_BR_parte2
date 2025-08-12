# TelecomX_BR_parte2
Projeto de análise de dados e Machine Learning One Oracle-Alura-ClearSale

TelecomX_BR_parte2 — Previsão de Evasão de Clientes
📌 Descrição do Projeto
Este projeto faz parte do Challenge Telecom X – Parte 2 e tem como objetivo desenvolver modelos preditivos capazes de prever quais clientes têm maior chance de cancelar seus serviços.
A análise permite que a empresa antecipe ações para reduzir a evasão (churn), otimizando estratégias de retenção.

🎯 Objetivos
Preparação dos dados para modelagem:
Eliminação de colunas irrelevantes (ex.: IDs).
Codificação de variáveis categóricas (One-Hot Encoding).
Análise de balanceamento das classes.
Aplicação opcional de técnicas de balanceamento (SMOTE, oversampling, undersampling).
Normalização/Padrão de dados quando necessário.
Análise exploratória e seleção de variáveis:
Matriz de correlação para variáveis numéricas.
Identificação de variáveis mais correlacionadas com a evasão.
Visualizações: Boxplots, Scatter Plots.
Treinamento e avaliação de modelos:
Separação dos dados em treino e teste.
Teste de pelo menos dois modelos:
Um sensível à escala (ex.: Regressão Logística, KNN).
Um não sensível à escala (ex.: Árvore de Decisão, Random Forest, XGBoost).
Avaliação com métricas:
Acurácia
Precisão
Recall
F1-score
Matriz de confusão
Comparação de desempenho e análise de overfitting/underfitting.

Conclusão estratégica:
Principais fatores que influenciam a evasão.
Modelo mais adequado para o cenário.

📂 Estrutura do Projeto
TelecomX_BR_parte2/
│-- data/
│   ├── df_limpo.csv              # Base de dados tratada na Parte 1
│-- notebooks/
│   ├── TelecomX_BR_parte2.ipynb  # Notebook principal com todo o pipeline
│-- results/
│   ├── matriz_confusao.png
│   ├── comparativo_f1.png
│-- README.md

Pipeline de Modelagem
Importação dos dados tratados da Parte 1.
Pré-processamento:
Remoção de colunas irrelevantes.
Encoding de variáveis categóricas.
Balanceamento das classes (SMOTE opcional).
Normalização quando necessário.
Análise exploratória e seleção de variáveis.
Treinamento de modelos:
Modelos baseados em distância (com normalização).
Modelos baseados em árvore (sem necessidade de normalização).
Avaliação com métricas e escolha do melhor modelo via F1-score.

Conclusões estratégicas.
📈 Resultados Obtidos
Modelo escolhido:
🔹 XGBoost (tuned) — F1-score: 0.6268
Matriz de Confusão — Interpretação:
Boa taxa de acerto para a classe "Não" (clientes que não cancelaram).
Necessidade de melhorar o Recall da classe "Sim" (clientes que cancelaram), pois ainda existem falsos negativos relevantes.
Comparação com outros modelos:
Random Forest apresentou desempenho próximo, mas o XGBoost obteve melhor equilíbrio entre Precisão e Recall.

🧠 Conclusões Estratégicas
Principais fatores de evasão incluem tempo de contrato, total gasto e tipo de serviço contratado.
XGBoost apresentou:
Melhor equilíbrio entre precisão e recall.
Maior F1-score no conjunto de teste.
Potencial para otimizações adicionais (ajuste de hiperparâmetros, feature engineering avançado).

Próximos passos:
Ajustar o Recall da classe positiva.
Criar alertas proativos para clientes com alto risco de churn.

📌 Tecnologias Utilizadas
Python (Pandas, NumPy, Scikit-learn, XGBoost, Imbalanced-learn)
Visualização (Matplotlib, Seaborn)
Google Colab para desenvolvimento
GitHub para versionamento e publicação

📬 Autor
Desenvolvido por Vanessa Santos como parte do desafio Telecom X.
