Set-Content -Path README.md -Value @'
<div align="center">

# 📦 Smart Retail AI: 3D Demand & Inventory Forecasting
### *End-to-End Time Series ML Pipeline • Live Weather API • 3D Spatial Analytics • Smart Audio Alerts*

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://retail-demand-forecasting-ml-gsoypcyccegh9bzgu4vh7x.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Streamlit-1.32%2B-FF4B4B.svg?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Model](https://img.shields.io/badge/Model-XGBoost%20%7C%20Tree--Ensemble-brightgreen.svg)](https://xgboost.readthedocs.io/)

[🌐 View Live Web App](https://retail-demand-forecasting-ml-gsoypcyccegh9bzgu4vh7x.streamlit.app/) • [📂 GitHub Repository](https://github.com/Anuska111/retail-demand-forecasting-ml)

</div>

---

### 🔄 System Architecture & Data Pipeline

```mermaid
flowchart TD
    subgraph Data_Sources ["1. Input & Real-Time Sync"]
        A[("Historical Sales CSV")]
        B["Live Open-Meteo REST API"]
        C["User Inputs (Price, Discount)"]
    end

    subgraph Preprocessing ["2. Feature Pipeline"]
        D["Time-Series Feature Extraction"]
        E["One-Hot Categorical Encoding"]
    end

    subgraph ML_Engine ["3. ML Inference Engine"]
        F["Trained XGBoost Regressor"]
        G["Predicted Demand (Units)"]
    end

    subgraph UI_Modules ["4. Streamlit Dashboard"]
        H["🚀 Real-Time Demand Metrics"]
        I["🌐 Interactive 3D Spatial Matrix"]
        J["📈 Price Elasticity Simulation"]
    end

    subgraph Alert_System ["5. Stockout Decision & Alerts"]
        K{"Demand > Shelf Inventory?"}
        L["🚨 Deficit Alert & Sound"]
        M["✅ Optimal Stock Level"]
    end

    A --> D
    B --> D
    C --> D
    D --> E
    E --> F
    F --> G
    G --> H
    G --> I
    G --> J
    G --> K
    K -- "Yes" --> L
    K -- "No" --> M
------------------------
🖥️ Dashboard Architecture & Tab Modules
Module Tab,Core Functionality,Primary Tech / Output
🚀 AI Demand Forecasting,Real-time demand inference with interactive capacity gauge & live stockout warnings,"XGBoost / Scikit-Learn, Audio API, Gauge"
🌐 3D Inventory Matrix,"3D multidimensional cluster plots across categories, price elasticities, and store limits",Plotly Express 3D Scatter Engine
📊 Analytics & Simulation,"Price sensitivity simulations, competitor pricing index, and historical trends",Dynamic Elasticity Curve Models

🛠️ Technology Stack
├── Languages      : Python 3.10+
├── ML / Analytics : XGBoost, Scikit-Learn, Statsmodels, Pandas, NumPy, Joblib
├── APIs & Web     : Open-Meteo REST API, Requests
├── Frontend / UI  : Streamlit, Plotly (3D & Indicators), HTML5/CSS3, Web Audio API
└── Environment    : PyCharm, Git, GitHub, Streamlit Cloud

📂 Repository File Tree
retail-demand-forecasting-ml/
│
├── app.py                     # Main full-stack Streamlit web application
├── retail_store_inventory.csv # Historical dataset (73,100 rows × 15 features)
├── retail_demand_model.pkl    # Serialized trained Tree-Ensemble model
├── model_features.pkl         # Encoded feature column list
├── category_mappings.pkl      # Categorical dropdown metadata
├── requirements.txt           # Environment dependencies
└── README.md                  # Project documentation
