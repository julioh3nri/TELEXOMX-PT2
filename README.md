# 📉 Previsão de Evasão de Clientes no Setor de Telecom

Este projeto tem como objetivo prever a **evasão (churn)** de clientes de uma empresa de telecomunicações, utilizando algoritmos de **Machine Learning** supervisionado. A análise considera variáveis contratuais, comportamentais e demográficas para identificar os fatores mais relevantes que influenciam na saída dos clientes.

---

## 📊 Objetivos

- Identificar padrões de evasão de clientes com base em dados históricos.
- Construir e comparar modelos de machine learning para prever churn.
- Avaliar o desempenho dos modelos com métricas adequadas.
- Interpretar os fatores que mais influenciam a saída dos clientes.
- Propor melhorias para estratégias de retenção com base na análise.

---

## 🗂️ Estrutura do Projeto

- data/ # Arquivos de dados (tratados ou brutos)
- notebooks/ # Jupyter Notebooks de análise e modelagem
- models/ # Modelos treinados (salvos com joblib/pickle)
- imgs/ # Gráficos e visualizações (matriz de confusão, etc.)
- README.md # Documentação do projeto
- requirements.txt # Bibliotecas necessárias
- ## 🧠 Modelos Utilizados

--- 

### ✅ Regressão Logística (com normalização)
- Modelo linear e interpretável.
- Requer normalização dos dados devido à sensibilidade à escala.
- Coeficientes ajudam a entender o impacto positivo/negativo de cada variável.

### 🌲 Random Forest (sem normalização)
- Modelo de árvore robusto a outliers e variáveis em diferentes escalas.
- Não requer normalização.
- Mede a importância das variáveis com base na redução da impureza.

---

## ⚙️ Técnicas e Ferramentas

- **Linguagem:** Python
- **Bibliotecas:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Modelagem:** Regressão Logística, Random Forest
- **Pré-processamento:** One-Hot Encoding, Normalização (StandardScaler)
- **Avaliação:** Acurácia, Precisão, Recall, F1-score, Matriz de Confusão
- **Análise de variáveis:** Coeficientes (Logística) e Importância (Random Forest)

---

## 📈 Avaliação dos Modelos

### Regressão Logística
- **Acurácia:** ~80%
- **Recall (Classe 1):** ~53%
- **Ponto forte:** Boa interpretabilidade e equilíbrio entre precisão e recall.
- **Ponto fraco:** Perde parte dos clientes que realmente evadem (falsos negativos).

### Random Forest
- **Acurácia:** ~79%
- **Recall (Classe 1):** ~46%
- **Ponto forte:** Capta relações não lineares entre variáveis.
- **Ponto fraco:** Menor sensibilidade à classe de evasão.

---

## 🧪 Principais Variáveis Relevantes

- `tipo_contrato_Two year`: contratos longos reduzem a evasão.
- `metodo_pagamento_Electronic check`: associado a maior evasão.
- `meses_contrato`: contratos mais curtos indicam risco.
- `valor_total`: clientes com maior gasto têm maior chance de sair.
- `tipo_internet_Fiber optic`: maior evasão comparado a outros tipos.
- `tem_parceiro` e `tem_dependentes`: clientes com vínculos sociais tendem a permanecer mais.
