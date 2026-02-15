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


## 📈 Insights Gerados pelo Modelo (Business Intelligence)

Com base na importância das variáveis (*Feature Importance*) calculada pelo algoritmo de machine learning, identificamos os pilares críticos para a retenção:

> **Nota de Usabilidade:** As métricas abaixo refletem a análise da base total de clientes (referência macro). Como o dashboard é **totalmente dinâmico**, estes valores são recalculados instantaneamente ao aplicar os filtros de segmento no Power BI para realizar análises granulares.

1.  **O Fator Idade (Peso: 23,12%):** A idade é o maior preditor do modelo. O risco de evasão escala drasticamente conforme o envelhecimento: enquanto jovens (18-24 anos) têm apenas **6,79%** de probabilidade média de churn, esse valor sobe para **46,97%** na faixa Sênior (55-64 anos).
2.  **Fidelidade por Volume de Produtos (Peso: 22,27%):** A quantidade de produtos (`NumOfProducts`) é o segundo maior driver de decisão. Identificamos uma anomalia crítica: clientes com **3 ou 4 produtos** possuem probabilidades de churn alarmantes de **81,44%** e **92,13%**, respectivamente.
3.  **Engajamento e Atividade (Peso: 20,06%):** O status de "Membro Inativo" foi identificado como o principal **sinal precursor** de evasão. No dashboard, validamos que clientes inativos possuem uma probabilidade de churn de **26,49%**,
4.  **Vulnerabilidade Geográfica (Alemanha):** A localização na **Alemanha** contribui com **13,45%** para a decisão do modelo. Clientes alemães apresentam a maior probabilidade média de churn entre todos os países, atingindo **32,97%**.

## 📊 Dashboard Estratégico (Power BI)
O dashboard foi estruturado em **4 visões dinâmicas**, permitindo que diferentes áreas do banco tomem decisões:

### 🏠 Página Inicial (Menu de Navegação)
Interface de entrada com sistema de botões interativos para acesso rápido a todas as áreas do projeto.
![Página Inicial](screenshots/imagem1.png)

### 1. Visão Geral
Monitoramento macro da saúde da base e principais KPIs de churn do banco.
![Visão Geral](screenshots/imagem2.png)

### 2. Plano de Retenção
Identificação nominal de clientes de alto valor e cálculo de **Capital em Risco**.
![Plano de Retenção](screenshots/imagem3.png)

### 3. Perfil do Cliente
Segmentação demográfica e comportamental para entender profundamente os motivos da saída.
![Perfil do Cliente](screenshots/imagem4.png)

### 4. Performance do Modelo de Machine Learning
Transparência total sobre a importância das variáveis e métricas de validação do modelo XGBoost.
![Performance do Modelo de Machine Learning](screenshots/imagem5.png)


## 📚 Fonte dos Dados

Os dados utilizados foram obtidos no Kaggle:
[Churn Modelling — por Shruti_Iyyer](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling/data)

## ▶️ Como abrir

1. Abra `dashboard-powerbi/churn_powerbi_dashboard.pbix` no **Power BI Desktop**.


## 📁 Estrutura do Projeto
```
churn-prediction-xgboost-powerbi/
├── data/
│   ├── raw/                    # Dados originais
│   │   └── Churn_Modelling.csv
│   └── processed/              # Dados processados pelo modelo
│       ├── churn_predictions.csv
│       ├── model_metrics.csv
│       └── feature_importance.csv
├── notebooks/
│   └── bank_churn_risk_prediction.ipynb   # Pipeline completo de ML
├── dashboard-powerbi/
│   └── churn_powerbi_dashboard.pbix       # Dashboard interativo
├── requirements.txt
├── LICENSE
└── README.md
```

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python (Pandas, Scikit-Learn, XGBoost, Joblib).
* **Visualização:** Matplotlib, Seaborn e Power BI (DAX avançado).
* **UX/UI:** Design Dark Mode focado em navegabilidade por botões e Tooltips instrucionais.

## 📄 Licença

Este projeto está sob a licença **MIT** - veja o arquivo [LICENSE](LICENSE) para detalhes.



## 👨‍💻 Desenvolvedor

**Leonardo Serpa** 

---
