# 🏦 Previsão de Churn Bancário com Machine Learning e Power BI



## 🎯 Visão do Projeto
Este projeto integra **Machine Learning (XGBoost)** e **Business Intelligence** para transformar dados brutos em uma estratégia de retenção de clientes. O foco é identificar preventivamente clientes com alta probabilidade de churn, permitindo que o banco aja de forma proativa para proteger seu capital.



## 🧠 Inteligência de Dados (Python)
A base do projeto foi construída no Jupyter Notebook, onde realizei o ciclo completo de ML:
* **Feature Engineering:** Transformação de variáveis categóricas e tratamento de dados.
* **Model Selection:** Comparação entre Regressão Logística, Random Forest, Gradient Boosting e XGBoost.
* **Otimização:** Uso de `GridSearchCV` para tunagem de hiperparâmetros do **XGBoost**.
* **Performance Final:**
  
    * **Acurácia:** 86,80%
    * **AUC (Área sob a curva ROC):** 87,21%


## 📊 Dashboard Estratégico (Power BI)
O dashboard foi estruturado em **4 visões dinâmicas**, permitindo que diferentes áreas do banco tomem decisões:

1.  **Visão Geral:** Monitoramento macro da saúde da base e taxa de churn.
2.  **Plano de Retenção:** Identificação nominal de clientes e **Capital em Risco** (integrando o saldo bancário com a probabilidade de churn).
3.  **Perfil do Cliente:** Análise comportamental focada nas variáveis críticas (Idade, Tempo de Relacionamento, Gênero e Localização).
4.  **Performance do Modelo de Machine Learning:** Transparência total sobre a importância das variáveis (Feature Importance) e métricas de confiança do modelo.

## 🛠️ Tecnologias e Metodologias
* **Linguagem:** Python (Pandas, Scikit-Learn, XGBoost, Joblib, Seaborn, matplotlib).
* **Visualização:** Power BI (DAX avançado para cálculo de medidas de risco).
* **UX/UI:** Design Dark Mode focado em leitura dinâmica e navegabilidade por botões.

---
