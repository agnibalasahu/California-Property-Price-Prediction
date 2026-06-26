<div align="center">

# 🏡 California House Price Predictor
### *Can data tell us what a home is worth?*

<br/>

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Status](https://img.shields.io/badge/Status-Complete-28A745?style=for-the-badge)](.)

<br/>

> *"In God we trust. All others must bring data."* — W. Edwards Deming

<br/>

**20,640 districts. 10 features. 1 goal — predict California home prices.**

---

</div>

## 🗺️ The Story

Imagine you're a real estate analyst in California. Every day, buyers and sellers ask you the same question — *"What is this house really worth?"*

This project answers that question using **machine learning and regression analysis** on real California housing data. We explore what drives property prices — from ocean proximity to household income — and build models that predict median house values across California's districts.

---

## ✨ What's Inside

```
📦 California-Property-Price-Prediction
 ┣ 📓 California_Property_Price_Prediction.ipynb   ← Main notebook (start here!)
 ┣ 📊 Price_Prediction.csv                         ← Dataset (20,640 records)
 ┗ 📄 README.md                                    ← You are here
```

---

## 🔍 Project Workflow

```
📥 Load Data
     ↓
🔎 Explore & Visualize (EDA)
     ↓
🧹 Clean & Preprocess
     ↓
⚙️  Engineer Features
     ↓
🤖 Train Models
   ┣━ Simple Linear Regression
   ┗━ Multiple Linear Regression
     ↓
📊 Evaluate & Compare
     ↓
🏆 Select Best Model
```

---

## 📊 Dataset Snapshot

| Feature | Description | Type |
|---|---|---|
| `longitude` / `latitude` | Geographic coordinates | Float |
| `housing_median_age` | Median age of houses in district | Int |
| `total_rooms` | Total rooms in district | Int |
| `total_bedrooms` | Total bedrooms in district | Int |
| `population` | District population | Int |
| `households` | Number of households | Int |
| `median_income` | Median household income | Float |
| `ocean_proximity` | Distance category to ocean | String |
| 🎯 `median_house_value` | **Target — what we predict** | Float |

> 📍 Source: California Census Data — 20,640 districts across the state

---

## 🧠 Key Insights from EDA

- 💰 **Income rules** — `median_income` has the strongest correlation with house value (r = 0.69)
- 🌊 **Location matters** — ISLAND and NEAR BAY properties are significantly more expensive
- 🗺️ **Coastal clusters** — Bay Area and LA show the highest property values on the map
- ⚠️ **Data cap** — House values are capped at $500,001 (ceiling effect in raw data)

---

## 🤖 Models Built

### 1️⃣ Simple Linear Regression
> One feature. One line. A baseline to beat.

Uses only `median_income` — the single strongest predictor.

```
median_house_value = slope × median_income + intercept
```

### 2️⃣ Multiple Linear Regression
> All features. Full power. Real-world complexity.

Uses all 15 features including 3 engineered ones:

| Engineered Feature | Formula |
|---|---|
| `rooms_per_household` | total_rooms ÷ households |
| `bedrooms_per_room` | total_bedrooms ÷ total_rooms |
| `population_per_household` | population ÷ households |

---

## 📈 Results

<div align="center">

| Metric | Simple LR | Multiple LR | Winner |
|:---:|:---:|:---:|:---:|
| **R² Score** | 0.4589 | 0.5970 | 🏆 Multiple LR |
| **RMSE** | $84,209 | $72,669 | 🏆 Multiple LR |
| **MAE** | $62,991 | $50,889 | 🏆 Multiple LR |
| **Features Used** | 1 | 15 | — |

</div>

### 🏆 Final Model: **Multiple Linear Regression**
- ✅ Explains **59.7%** of variance in house prices
- ✅ Average prediction error of **~$50,889**
- ✅ **15% lower RMSE** than Simple Linear Regression
- ✅ Captures geographic, demographic, and proximity signals

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `Python 3.10+` | Core language |
| `Pandas` | Data manipulation |
| `NumPy` | Numerical computation |
| `Matplotlib + Seaborn` | Visualizations |
| `Scikit-learn` | ML models, scaling, metrics |
| `Jupyter Notebook` | Interactive development |

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/agnibalasahu/California-Property-Price-Prediction.git
cd California-Property-Price-Prediction

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Launch the notebook
jupyter notebook California_Property_Price_Prediction.ipynb
```

---

## 🔮 Future Improvements

- [ ] Ridge & Lasso Regression to handle multicollinearity
- [ ] Random Forest for non-linear patterns
- [ ] Remove capped values ($500,001) to reduce bias
- [ ] Cross-validation for more robust evaluation
- [ ] Deploy as a web app using Flask or Streamlit

---

## 👨‍💻 Author

<div align="center">

**Agnibala Sahu**
🎓 Student | Artificial Inteligence and Machine Learning

[![GitHub](https://img.shields.io/badge/GitHub-agnibalasahu-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/agnibalasahu)

<br/>

*Part A — Property Price Prediction | Machine Learning | Regression Analysis*

</div>
