<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:0f3460,100:00c896&height=200&section=header&text=Pakistan%20Freelancing%20Economy&fontSize=36&fontColor=ffffff&fontAlignY=38&desc=2015%20–%202025%20%7C%206%2C000%20Profiles%20%7C%2010-Year%20Longitudinal%20Analysis&descAlignY=58&descSize=15" width="100%"/>

[![Kaggle](https://img.shields.io/badge/View%20on-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/azharalisoomro/pakistan-freelancing-economy-2015-2025)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C8CBF?style=for-the-badge)](https://seaborn.pydata.org)
[![SHAP](https://img.shields.io/badge/SHAP-Explainability-FF6B6B?style=for-the-badge)](https://shap.readthedocs.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-00c896?style=for-the-badge)](LICENSE)

<br/>

> **A 10-year data-driven deep dive into Pakistan's gig economy.**  
> 6,000 freelancer profiles · 3 platforms · 39 cities · 36 features · PKR/USD historical FX rates

<br/>

[📊 Key Findings](#-key-findings) • [🗂 Notebook Sections](#-notebook-sections) • [🛠 Tech Stack](#️-tech-stack) • [🚀 Run It](#-getting-started) • [👤 Author](#-about-the-author)

</div>

---

## 🌐 What This Notebook Does

Pakistan consistently ranks among the world's top freelancing nations — but the raw numbers hide a far more nuanced story. This notebook goes well beyond counting earnings. It diagnoses *why* some freelancers earn 4× more than others, whether the PKR currency crisis helped or hurt real purchasing power, which skills are genuinely worth learning right now, and how unequal opportunity is across the country.

Every section is structured around a testable hypothesis, visualized with 20+ charts, and closed with a boxed insight summary — designed to be useful to freelancers, policymakers, and data science reviewers alike.

---

## 📊 Key Findings

<table>
<tr>
<td width="50%">

### 💰 The Currency Paradox
PKR nominal earnings surged after the 2022–23 crisis — but once adjusted for Pakistan's CPI inflation, real purchasing power tells a very different story. Freelancers earning in USD are partially insulated; those spending domestically are not.

</td>
<td width="50%">

### 🌟 AI/ML: The Rising Star
The Skill ROI Matrix reveals AI/ML sits in the top-right quadrant — both the highest current earnings AND fastest post-2021 acceleration. The ChatGPT release (late 2022) is visible in the actual earnings data.

</td>
</tr>
<tr>
<td width="50%">

### 🏙 Geography Barely Matters
The metro vs non-metro earnings gap nearly vanishes when you control for skill category. Freelancing is a genuine geographic equalizer — what you know matters far more than where you live.

</td>
<td width="50%">

### 🏆 Reputation Compounds
Top-badge freelancers earn a **multiple** of entry-level badge holders. JSS score, repeat client rate, and account age compound over time — the longer you're on a platform, the wider the moat.

</td>
</tr>
</table>

---

## 🗂 Notebook Sections

```
📓 Pakistan Freelancing Economy 2015–2025
│
├── 1️⃣  Setup, Theme & Data Loading
│       ├── Custom dark-theme color system (12 named colors)
│       ├── Dataset overview: 6,000 rows × 36 columns
│       └── Executive summary banner: key dataset stats at a glance
│
├── 2️⃣  Data Quality Audit
│       ├── Missing value heatmap with severity thresholds
│       ├── Imputation rate by flag column
│       ├── IQR outlier detection on all numeric fields
│       ├── Log-transformed earnings sanity check
│       └── Quality verdict card
│
├── 3️⃣  Demographic EDA
│       ├── Top 15 cities by freelancer count
│       ├── Gender distribution + earnings gap by gender
│       ├── Age distribution with IQR bands
│       ├── Education level vs earnings
│       ├── Age vs earnings scatter (colored by experience)
│       └── Primary income vs side income vs student earnings
│
├── 4️⃣  Platform & Skills Analysis
│       ├── Platform market share (Upwork · Fiverr · Freelancer.com)
│       ├── Median vs mean earnings per platform
│       ├── Skill category earnings ranking
│       ├── Top 15 sub-skills by median earnings
│       ├── Platform × Skill heatmap
│       ├── Skill ROI Matrix — 4-quadrant bubble chart
│       │     (Rising Stars / Cash Cows / Emerging / Declining)
│       └── Platform badge distribution breakdown
│
├── 5️⃣  Earnings Deep Dive
│       ├── Lorenz curve + Gini coefficient
│       ├── Earnings by client region (median vs mean)
│       └── Income inequality statistics (top 10% share)
│
├── 6️⃣  Time-Series & PKR Currency Impact
│       ├── 10-year USD earnings trend with event annotations
│       │     (COVID-19 · PKR crisis · AI/ML surge)
│       ├── PKR nominal vs real (CPI-adjusted, 2015=100)
│       ├── Historical PKR/USD exchange rate (annotated YoY deltas)
│       ├── Top 5 skill earning trajectories over time
│       ├── Pre vs post-2022 statistical comparison
│       │     (USD · PKR nominal · real purchasing power)
│       ├── Quarterly earnings seasonality heatmap
│       └── Dual-axis: USD earnings + PKR/USD rate overlay
│
├── 7️⃣  English Proficiency & Income
│       ├── Earnings ladder: Basic → Conversational → Fluent → Native
│       ├── Step-up $ and % annotation at each level
│       ├── Hourly rate by proficiency level
│       ├── Violin plots — full earnings spread per level
│       ├── Platform × English proficiency heatmap
│       ├── Client region × English proficiency heatmap
│       └── English premium within same skill category
│
├── 8️⃣  Missing Flag Analysis
│       ├── Earnings: data present vs imputed (flag=0 vs flag=1)
│       ├── Flag co-occurrence correlation heatmap
│       ├── Imputation rate by platform and experience tier
│       ├── Total missing flags per freelancer distribution
│       ├── Earnings vs total flag count (MAR confirmation)
│       └── MCAR vs MAR diagnosis table for every flag column
│
├── 9️⃣  Profile Level & Reputation Analysis
│       ├── Badge earnings ladder with multiplier annotations
│       ├── Earnings spread by badge level (IQR visualization)
│       ├── Reputation gap over time (top badge vs entry badge)
│       ├── Upwork JSS tier earnings breakdown
│       ├── JSS score distribution + threshold analysis
│       ├── JSS vs earnings scatter (colored by hourly rate)
│       ├── Repeat client rate tiers vs earnings
│       ├── Review score distribution
│       └── Account age compounding effect
│
└── 🔟  City Tier & Payment Method Analysis
        ├── Metro vs Non-Metro earnings distributions
        ├── Top 20 cities by median earnings (min 30 freelancers)
        ├── City-level Gini coefficient ranking
        ├── Payment method share + earnings by method
        ├── Payment method × city tier breakdown
        ├── Skill concentration: metro vs non-metro
        ├── Geographic Opportunity Index (median × (1 − Gini))
        └── Metro vs Non-Metro controlling for skill category

    🔢  Skill Growth Trajectories 2015–2025 (Section 11)
        ├── All skill trajectories (top 3 highlighted)
        ├── Total growth ranking (2015 → 2025)
        ├── CAGR ranking per skill
        ├── Momentum index (avg YoY growth 2022–2025)
        ├── Early (2015–2019) vs Late (2020–2025) growth comparison
        ├── Growth scatter: early vs late (4-quadrant)
        ├── Best entry year per skill (peak YoY jump)
        └── Quarterly seasonality normalized heatmap by skill
```

---

## 🛠️ Tech Stack

```python
# Data manipulation
import pandas as pd
import numpy as np

# Visualization
import matplotlib.pyplot as plt
import matplotlib.ticker as mticker
import matplotlib.patches as mpatches
import seaborn as sns

# Analysis
from scipy.stats import gini         # Inequality measurement
```

**Dataset:** `pk_freelancing_economy_2015_2025.csv`  
**Scope:** 6,000 freelancer profiles · Upwork, Fiverr, Freelancer.com · 39 cities · 2015–2025  
**Key fields:** `monthly_earnings_usd`, `monthly_earnings_pkr`, `pkr_usd_rate`, `skill_category`, `primary_skill`, `platform`, `profile_level`, `job_success_score_pct`, `english_proficiency`, `repeat_client_rate_pct`, `account_age_years`, `*_missing_flag` columns

---

## 🔑 Analytical Techniques

| Technique | Section | What It Reveals |
|---|---|---|
| **IQR Outlier Detection** | §2 | Data integrity before any analysis |
| **MCAR vs MAR Diagnosis** | §8 | Whether missingness is random or signal |
| **Lorenz Curve + Gini** | §5 | Income inequality among Pakistani freelancers |
| **CPI Deflation** | §6 | Real vs nominal earnings — the currency paradox |
| **Dual-Axis Time Series** | §6 | USD earnings vs PKR/USD rate divergence |
| **Skill ROI Matrix** | §4 | 4-quadrant bubble chart: earnings × growth × count |
| **Momentum Index** | §11 | Avg YoY growth 2022–2025 — is a skill still accelerating? |
| **Geographic Opp Index** | §10 | City score = median earnings × (1 − Gini) |
| **Reputation Multiplier** | §9 | Exact earnings premium per badge / JSS tier |
| **English Premium Control** | §7 | Premium within same skill category — isolated effect |

---

## 🚀 Getting Started

### Option 1 — Run on Kaggle (zero setup)

[![Open in Kaggle](https://img.shields.io/badge/Open%20in-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/azharalisoomro/pakistan-freelancing-economy-2015-2025)

Free GPU/CPU, dataset pre-mounted, all libraries available.

### Option 2 — Run Locally

```bash
# 1. Clone
git clone https://github.com/azharalisoomro/pakistan-freelancing-economy.git
cd pakistan-freelancing-economy

# 2. Virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install
pip install -r requirements.txt

# 4. Launch
jupyter notebook pakistan-freelancing-economy-2015-2025.ipynb
```

**requirements.txt**
```
pandas>=2.0.0
numpy>=1.26.0
matplotlib>=3.8.0
seaborn>=0.13.0
scipy>=1.11.0
jupyter>=1.0.0
```

> Update the `PATH` variable in Section 1 to point to your local CSV file.

---

## 📁 Repository Structure

```
📦 pakistan-freelancing-economy/
├── 📓 pakistan-freelancing-economy-2015-2025.ipynb
├── 📂 data/
│   └── pk_freelancing_economy_2015_2025.csv
├── 📄 requirements.txt
└── 📄 README.md
```

---

## 💡 Who This Is For

```
📌 Freelancers        → Which skill to invest in, which platform to prioritize,
                        how much the English premium is actually worth

📌 Policymakers       → Where the geographic and gender gaps are, and how large

📌 Data Analysts      → A real-world notebook demonstrating EDA, inequality
                        measurement, time-series, and flag analysis end-to-end

📌 Recruiters         → Evidence of analytical depth on a domain-specific problem
                        with economic and social relevance
```

---

## 🤝 Contributing

Suggestions, data corrections, or new analytical angles are welcome.

1. Fork the repo
2. `git checkout -b feature/your-idea`
3. `git commit -m 'Add: description'`
4. `git push origin feature/your-idea`
5. Open a Pull Request

Or open an [Issue](https://github.com/azharalisoomro/pakistan-freelancing-economy/issues) to start a conversation.

---

## 👤 About the Author

<div align="center">

**Azhar Ali Soomro**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/azharalisoomro)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/azharalisoomro)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/azharalisoomro)

</div>

Third-year BS Computer Science (AI specialization) student at **Sukkur IBA University** and member of **Comeback Pakistan Cohort 1** — a highly selective AI career accelerator (top 5%, full scholarship). This analysis directly informs **Freelancer's Co-Pilot**, an AI tool being built to help Pakistani freelancers price smarter, write better proposals, and navigate the global market with data behind them.

---

## ⭐ Support

If this notebook helped you — an upvote on Kaggle or a star on GitHub keeps the work going.

[![Upvote on Kaggle](https://img.shields.io/badge/Upvote%20on-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/code/azharalisoomro/pakistan-freelancing-economy-2015-2025)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c896,50:0f3460,100:0f172a&height=100&section=footer" width="100%"/>

*Built to understand Pakistan's freelancers better — and eventually build better tools for them.*

</div>
