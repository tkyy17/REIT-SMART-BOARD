# 🏢 REIT Smart Analytics Board

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-Gradio-orange)](https://gradio.app/)
[![ML](https://img.shields.io/badge/Model-XGBoost-red)](https://xgboost.readthedocs.io/)
[![License](https://img.shields.io/badge/License-Academic-green)]()

**A Hybrid Machine Learning Dashboard for Malaysian REIT Performance Prediction**

[cite_start]This repository contains the source code and documentation for the **REIT Smart Analytics Board**, a Final Year Project (FYP) developed to predict Net Property Income (NPI) for major Malaysian Real Estate Investment Trusts (Pavilion, Sunway, and IGB)[cite: 58, 60].

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
- [Methodology](#-methodology)
- [Performance](#-performance)
- [Project Structure](#-project-structure)
- [Disclaimer](#-disclaimer)
- [Credits](#-credits)

---

## 🔭 Overview

Traditional REIT analysis often relies on static historical data. [cite_start]This project introduces a **Smart Analytics Board** that utilizes a hybrid machine learning approach to forecast financial performance[cite: 58].

[cite_start]By combining **XGBoost Regression** with **Time-Series Trend Analysis**, the system overcomes the limitations of small datasets (2020–2024) to provide accurate 1–3 year NPI forecasts with quantified risk assessments[cite: 59, 132].

## 🚀 Key Features

* [cite_start]**🔮 Hybrid Prediction Engine:** Fuses Machine Learning (55% weight) with Trend Analysis (45% weight) for stable, realistic forecasts[cite: 541, 691].
* [cite_start]**📊 Interactive Dashboard:** A web-based interface built with Gradio to visualize trends and forecasts dynamically[cite: 62].
* [cite_start]**📉 Risk Quantification:** Visualizes **95% Confidence Intervals** to show the upper and lower bounds of predictions[cite: 63].
* [cite_start]**🎛️ Scenario Simulation:** "What-if" analysis tools to simulate the impact of **Interest Rate** and **Occupancy Rate** changes[cite: 62].
* [cite_start]**🚦 Automated Recommendations:** Generates actionable `BUY`, `HOLD`, or `SELL` signals based on growth thresholds[cite: 553].
* [cite_start]**🏆 Multi-REIT Comparison:** Side-by-side performance analysis of Pavilion, Sunway, and IGB REITs[cite: 63].

## 🛠 Tech Stack

* [cite_start]**Language:** Python 3.8+ [cite: 271]
* **Interface:** Gradio (Web UI)
* **Machine Learning:** XGBoost, Scikit-learn
* **Data Processing:** Pandas, NumPy
* **Visualization:** Plotly (Interactive Charts)

## 💻 Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/reit-smart-board.git](https://github.com/yourusername/reit-smart-board.git)
    cd reit-smart-board
    ```

2.  **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: If `requirements.txt` is missing, install the core libraries manually)*:
    ```bash
    pip install gradio pandas numpy plotly xgboost scikit-learn
    ```

## ▶️ Usage

1.  **Run the application:**
    ```bash
    python pavilion_xgb_app.py
    ```

2.  **Access the Dashboard:**
    The terminal will output a local URL (usually `http://localhost:7860` or similar). Open this link in your web browser.

3.  **Explore:**
    * **Tab 1 (Single REIT):** Select a REIT, adjust the sliders for interest/occupancy, and click "Generate Forecast".
    * **Tab 2 (Comparison):** Select multiple REITs to see overlaid performance charts.

## 🧠 Methodology

[cite_start]To address the challenge of limited historical data (annual reports from 2020–2024), this system uses a **Hybrid Algorithm**[cite: 541]:

1.  [cite_start]**Feature Engineering:** Creates lag variables, rolling averages, and efficiency ratios (NPI Margin)[cite: 240, 526].
2.  [cite_start]**XGBoost Model:** A regularized regression model captures non-linear relationships between revenue, occupancy, and NPI[cite: 59].
3.  [cite_start]**Trend Component:** A time-series decay factor ensures predictions remain grounded in realistic business growth patterns[cite: 541].
4.  [cite_start]**Weighted Ensemble:** The final prediction is a weighted average: `(0.55 * ML_Prediction) + (0.45 * Trend_Prediction)`[cite: 541].

## 📈 Performance

[cite_start]The model was evaluated against historical data with the following results[cite: 64, 718]:

| Metric | Result | Benchmark | Status |
| :--- | :--- | :--- | :--- |
| **R² Score** | **0.917** | > 0.80 | ✅ Exceeded |
| **MAPE** | **3.4%** | < 5.0% | ✅ Passed |
| **Confidence Coverage** | **97.2%** | 95.0% | ✅ Validated |

## 📂 Project Structure

```text
reit-smart-board/
├── pavilion_xgb_app.py   # Main application code
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
└── data/                 # (Optional) Folder for raw datasets if externalized

⚠️ Disclaimer
This system is developed for academic and research purposes only as part of a Final Year Project. The "BUY/HOLD/SELL" recommendations are generated by an algorithm and do not constitute professional financial advice. Always consult a licensed financial advisor before making investment decisions.

👥 Credits
Author: Tan Kang Yuan (B230042A) 
Supervisor: Chan Ler-Kuan 
Institution: Southern University College, Faculty of Engineering and Information Technology
