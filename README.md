# Quant_Genius_AI
# QuantGenius AI  
Explainable Market Intelligence Framework  
MSc Artificial Intelligence – Dissertation Project (BSBI / UCA)

------------------------------------------------------------
1. PROJECT OVERVIEW
------------------------------------------------------------

QuantGenius AI is an explainable market intelligence framework designed to support financial analysis and decision-making in non-stationary market environments. The system integrates quantitative forecasting models, explainable artificial intelligence (XAI), and retrieval-augmented contextual evidence from regulatory filings and financial news.

Unlike traditional trading systems, QuantGenius is explicitly designed as a decision-support tool, prioritising transparency, interpretability, robustness, and governance over raw predictive performance. The framework avoids claims of deterministic market prediction and instead focuses on structuring uncertainty and contextualising numerical forecasts.

This project was developed as part of an MSc dissertation and adheres to academic, ethical, and regulatory considerations relevant to financial AI systems.

------------------------------------------------------------
2. RESEARCH OBJECTIVES
------------------------------------------------------------

The primary objectives of QuantGenius AI are:

1. To evaluate the effectiveness of modern machine learning and deep learning models for short- and medium-horizon financial forecasting.
2. To enhance interpretability through explainable AI techniques and retrieval-augmented contextual evidence.
3. To assess robustness and reliability under non-stationary market conditions using explicit data drift monitoring.
4. To design a transparent, reproducible, and governance-aware financial decision-support framework.

------------------------------------------------------------
3. SYSTEM ARCHITECTURE (HIGH-LEVEL)
------------------------------------------------------------

The QuantGenius framework consists of four core layers:

3.1 Quantitative Forecasting Layer
- Models:
  - Gradient Boosted Decision Trees (XGBoost)
  - Long Short-Term Memory (LSTM) networks
  - Transformer-based sequence models
- Forecasting horizons:
  - Short-term: 1, 3, 5 trading days
  - Intermediate-term: 10, 15, 20 trading days
- Evaluation:
  - Rolling-window validation
  - Out-of-sample testing
  - No look-ahead bias

3.2 Feature Engineering Layer
- Price-based features (returns, volatility)
- Technical indicators (RSI, MACD, moving averages, Bollinger Bands)
- Volatility-normalised targets
- Multi-scale temporal representations

3.3 Explainability & Contextual Fusion Layer
- Retrieval-Augmented Generation (RAG)-style evidence retrieval
- Sources:
  - Regulatory filings (SEC-style disclosures)
  - Financial news articles
- Evidence retrieval constrained by “as-of” dates
- Controlled post-prediction forecast adjustments

3.4 Robustness & Governance Layer
- Data drift monitoring using Population Stability Index (PSI)
- Horizon-specific drift diagnostics
- Human-in-the-loop oversight
- Transparent reporting of system stability

------------------------------------------------------------
4. PROJECT STRUCTURE
------------------------------------------------------------

QuantGenius/
│
├── notebooks/
│   ├── QuantGenius_Main.ipynb
│   ├── Results_and_Figures.ipynb
│
├── data/
│   ├── market_data/
│   ├── text_data/
│
├── models/
│   ├── trained_models/
│
├── tables/
│   ├── cell12_best_overall_*.csv
│   ├── cell15_fusion_results_*.csv
│   ├── drift_summary_*.csv
│
├── reports/
│   ├── figures/
│   ├── evidence/
│
├── ui/
│   ├── quantgenius_ui.py
│
├── README.md
└── requirements.txt

------------------------------------------------------------
5. HOW TO REPRODUCE THE PROJECT (RECOMMENDED PATH)
------------------------------------------------------------

5.1 Environment Requirements
- Python 3.9–3.10 (recommended)
- Google Colab (preferred)
- GPU optional (used only during training)

IMPORTANT:
The interactive UI uses Gradio and may face dependency conflicts.
All core results, figures, and tables can be reproduced without the UI.

5.2 Step-by-Step Reproduction (Core Results)

1. Open QuantGenius_Main.ipynb in Google Colab
2. Run cells sequentially from Cell 1 to Cell 13
   - Data loading
   - Feature engineering
   - Model training
   - Baseline evaluation
3. Run Cell 14
   - Retrieval index creation (text embeddings)
4. Run Cell 15
   - Fusion results
   - Drift analysis
5. Verify outputs:
   - CSV files in /tables
   - Figures in /reports/figures

These outputs correspond directly to Chapter 4 (Findings, Analysis, Discussion).

------------------------------------------------------------
6. INTERACTIVE UI (OPTIONAL DEMONSTRATION)
------------------------------------------------------------

An optional interactive dashboard is included, allowing users to:
- Select ticker and forecasting horizon
- View baseline vs. fused forecasts
- Inspect retrieved regulatory and news evidence
- Monitor drift diagnostics

Notes:
- The UI is a demonstration layer, not required for replication
- Dependency conflicts may occur depending on environment
- A screen recording of the UI in operation is provided as evidence

If the UI cannot be launched, all analytical outputs remain fully reproducible.

------------------------------------------------------------
7. DATA SOURCES
------------------------------------------------------------

- Historical market data via public financial APIs
- Regulatory disclosures from publicly available filings
- Financial news from reputable financial media APIs

All data usage complies with academic research standards.
No proprietary or confidential datasets are used.

------------------------------------------------------------
8. ETHICAL CONSIDERATIONS
------------------------------------------------------------

- The system does not provide investment advice
- No claims of guaranteed profitability
- Outputs are descriptive and explanatory
- Human oversight is explicitly required
- Model limitations and uncertainty are transparently communicated

------------------------------------------------------------
9. KEY FINDINGS SUMMARY
------------------------------------------------------------

- Predictive accuracy remains modest across all horizons
- Retrieval-augmented fusion improves interpretability
- Regulatory filings provide stable contextual grounding
- News sentiment provides short-term narrative context
- Drift monitoring enhances governance and trustworthiness

------------------------------------------------------------
10. KNOWN LIMITATIONS
------------------------------------------------------------

- Daily-frequency data only
- No causal inference claims
- Concept drift not fully addressed
- UI dependency conflicts on some systems

All limitations are explicitly discussed in the dissertation.

------------------------------------------------------------
11. ACADEMIC POSITIONING
------------------------------------------------------------

This project meets MSc dissertation standards by:
- Avoiding exaggerated claims
- Prioritising methodological integrity
- Ensuring reproducibility
- Aligning with responsible AI principles in finance

------------------------------------------------------------
12. AUTHOR
------------------------------------------------------------

Ashtosh Rajesh Tiwari 
MSc Artificial Intelligence  
Berlin School of Business and Innovation (BSBI)  
Validated by University for the Creative Arts (UCA)


The project is fully assessable even without live execution.
