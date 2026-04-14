# E-Commerce ML Project

End-to-end machine learning project on the [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii) dataset. Covers customer segmentation, revenue forecasting, churn prediction, web analytics, and an AI-powered data agent.

---

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 1 | `1_customer_segmentation.ipynb` | RFM feature engineering + K-Means clustering to segment customers into Champions, Loyal, At Risk, and Lost |
| 2 | `2_eda.ipynb` | Exploratory analysis — monthly revenue trends, MoM growth, and top countries by revenue |
| 3 | `3_revenue_forecast.ipynb` | Linear regression model to forecast monthly revenue using time and seasonality features |
| 4 | `4_churn_prediction.ipynb` | Logistic Regression and Random Forest classifiers to predict customer churn |
| 5 | `5_online_shoppers_analysis.ipynb` | Web session EDA (traffic sources, bounce rates, funnel) + logistic regression purchase predictor |
| 6 | `6_ai_agent.ipynb` | LangChain Pandas agent that answers natural language questions about the dataset |

---

## Datasets

### Online Retail II
Used in notebooks 1–4.

1. Download from [Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) or [UCI](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
2. Place the file at `data/online_retail_II.xlsx`

### Online Shoppers Purchasing Intention
Used in notebook 5.

1. Download from [Kaggle](https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset)
2. Place the file at `data/online_shoppers_intention.csv`

> Data files are excluded from this repo via `.gitignore` due to size.

---

## Setup

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/ecommerce-ml-project.git
cd ecommerce-ml-project

# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl langchain langchain-groq langchain-anthropic langchain-experimental python-dotenv
```

For notebook 6 (AI Agent), create a `.env` file in the project root:

```
GROQ_API_KEY=your_groq_key_here
ANTHROPIC_API_KEY=your_anthropic_key_here
```

Get a free Groq API key at [console.groq.com](https://console.groq.com).

---

## Project Structure

```
├── 1_customer_segmentation.ipynb
├── 2_eda.ipynb
├── 3_revenue_forecast.ipynb
├── 4_churn_prediction.ipynb
├── 5_online_shoppers_analysis.ipynb
├── 6_ai_agent.ipynb
├── data/                  # Add dataset files here (gitignored)
├── .env                   # API keys (gitignored, never commit)
└── README.md
```

---

## Key Results

- **Customer Segmentation:** Identified 4 segments — Champions, Loyal Regulars, At Risk, and Lost — enabling targeted retention campaigns
- **Revenue Forecast:** Linear regression baseline for monthly revenue prediction
- **Churn Prediction:** Random Forest outperforms Logistic Regression on imbalanced churn labels
- **Purchase Prediction:** `PageValues` is the strongest predictor of online purchase conversion
