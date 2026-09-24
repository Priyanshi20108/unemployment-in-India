# Unemployment in India — Exploratory Data Analysis

An exploratory data analysis of unemployment, employment, and labour participation trends across Indian states between May 2019 and June 2020 — a window that captures the sharp economic impact of the COVID-19 lockdown.

## 📊 Dataset

- **Source:** [Unemployment in India](https://www.kaggle.com/datasets/gokulrajkmv/unemployment-in-india) (Kaggle)
- **Period:** May 2019 – June 2020
- **Granularity:** Monthly, by state and by area (Rural/Urban)
- **Columns used:**
  | Column | Description |
  |---|---|
  | `State` | Indian state / union territory |
  | `Date` | Month of observation |
  | `Frequency` | Reporting frequency (Monthly) |
  | `Unemployment Rate` | Estimated unemployment rate (%) |
  | `Employed` | Estimated number of people employed |
  | `Labour Participation Rate` | Estimated labour participation rate (%) |
  | `Region` | Rural or Urban |

> Note: in the raw CSV these last two are labeled `Region` (state) and `Area` (Rural/Urban) — renamed here to `State` and `Region` respectively to avoid confusion.

## 🛠️ Tools & Libraries

- Python 3
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

## 🔍 Analysis Steps

1. Data cleaning — handled missing values, fixed column names and dtypes (`Date` → datetime, `Frequency` → category)
2. Correlation analysis between unemployment, employment, and labour participation
3. Visual comparison of unemployment by rural vs. urban region
4. State-level unemployment trends over time
5. Distribution analysis via histograms

## 📈 Key Findings

- **Weak linear relationships overall** — unemployment, employment, and labour participation rate don't move together in any strong linear way (all correlations under 0.25 in magnitude).
- **Urban unemployment runs higher than rural** (~13% vs. ~10% on average), even though rural areas account for the majority (69%) of total employment.
- **The COVID-19 lockdown (Apr–Jun 2020) is the dominant event in the dataset** — unemployment spikes sharply across every state examined, with Bihar (~59%) and Delhi (~46%) hit hardest, while labour participation drops in both rural and urban areas over the same window before partially recovering.
- **Unemployment is unevenly distributed across states** — Tripura, Haryana, Jharkhand, Bihar, and Himachal Pradesh show the highest sustained average unemployment rates.
- **Most observations sit in a "normal" range** (low unemployment, moderate employment), with a long right tail driven almost entirely by the lockdown months.
