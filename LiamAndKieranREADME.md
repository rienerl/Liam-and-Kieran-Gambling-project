
# In the Black: An Exploration into Gambling Revenue, Taxes, and Economic Impact
# Liam Riener and Kieran Santos
# Dickinson College Data Analytics

## 📑 Table of Contents

- [Introduction](#-introduction)
- [Data Collection](#-data-collection)
- [Data Analysis](#-data-analysis)
  - [Key Observations](#key-observations)
  - [Correlation Findings](#correlation-findings)
- [Modeling the Future](#-modeling-the-future)
  - [Model Architecture](#model-architecture)
- [Insights & Policy Recommendations](#-insights--policy-recommendations)
- [Societal Implications](#-societal-implications)
- [Future Work](#-future-work)
- [Works Cited](#-works-cited)

---

## 📘 Introduction

Large-scale American commercial gambling began in Las Vegas, Nevada in 1931. Gambling has long been linked to data science as operators try to make money while providing the illusion of equal chance, while gamblers try to beat the house and win big.

In 2018, the Supreme Court struck down a set of gambling laws, allowing states to legalize sports gambling. Of the 36 states with legal commercial gaming operations, 12 began after 2018. Nationwide revenue from the industry has grown exponentially since 2018. Commercial operations have since scrambled to maximize profit while governments use taxation to fund public goods and services.

This project explores correlations between gambling legalization, tax rates, revenue, and total GDP. It aims to inform policymakers about how different approaches to regulation and taxation affect economic outcomes and business viability. We also model potential futures of American commercial gambling through 2030.

---

## 📊 Data Collection

- **GDP Data**: U.S. Bureau of Economic Analysis (2016–2025), data from 2014-23
- **Gambling Data**: American Gaming Association “State of the States” reports (2015–2024), data from 2014-23

We merged datasets by state and year to create a unified, 10-year view of gambling revenue, tax rates, and GDP across states where commercial gambling is legal.

---

## 🔎 Data Analysis

### Key Observations

- Gambling generates an average of **0.66% of GDP** in legal states, **7% in Nevada**, and nearly **2% in Mississippi**.
- **Nevada** is a significant outlier (earliest legalization by 45 years, gambling-centric economy) and was excluded from some analyses due to its weight in calculating correlation and modelling.

### Correlation Findings

- Very weak correla

| Variables                            | Correlation |
|-------------------------------------|-------------|
| GGR and GDP (YoY increase)          | **0.84**    |
| Tax Rate and GDP                    | 0.13        |
| Tax Rate and GGR                    | -0.10       |
| Tax Rate and Legalization Year      | 0.10        |
| Tax Rate and Year of Data           | -0.10       |
| GDP and Legalization Year           | 0.12        |
| GDP and GGR as % of GDP             | -0.19       |

---

## 🔮 Modeling the Future

### Model Architecture

Due to weak correlations between most variables, we projected gambling revenue with based on a **5% yearly GDP increase**, using:

1. **Linear Model**  
   `GGR = 5.17B + 0.0036 × GDP`

2. **Log-Linear Model**  
   `log(GGR) = 23.71 + 7.20 × 10⁻¹⁴ × GDP`

3. **Quadratic Model**  
   `GGR = 79B − 0.00929 × GDP + 5.32 × 10⁻¹⁶ × GDP²`

> 🔮 The quadratic model projects **tripled national gambling revenue by 2030**, compared to 2014. Continued lack of regulation, CA & TX legalize?
> The linear model projects modest growth, assumes 2018-23 legalization spree will fade and regulation will impede online gambling boom.
> The log-linear model projects a mix between the two models, projecting a continuation of accelerated growth and some caution.
> No model projects downturn in gambling. Public and government reaction to gambling revenue growth is unknown, may result in downturn.

---

## 💡 Insights & Policy Recommendations

- **Tax Rates** do **not** significantly affect revenue → States can impose reasonable taxes without discouraging gambling businesses.
- **Smaller economies** tend to have a **higher GGR-to-GDP ratio**, suggesting greater dependency on gambling.
- GGR growth is closely tied to broader **economic trends** (e.g. 2020 pandemic dip).
- **Cross-state learning** can improve regulation—Nevada’s long history offers valuable lessons.

---

## ⚖️ Societal Implications

- Public services funded by gambling raise **ethical concerns** about revenue sources.
- Greater legalization and online access risk **normalizing gambling**, especially among youth.
- Lack of revenue sensitivity to tax rates implies gambling is **highly lucrative and potentially addictive**.
- **Stronger regulation** is needed to prevent exploitation and support responsible gambling.

---

## 🔭 Future Work

- Develop **state- and region-specific** forecasting models.
- Incorporate **additional variables** despite weak current correlations.
- Conduct **international comparisons** of gambling policy and economic impact.
- Analyze **user-level behavior** on online platforms, especially post-2018 legalization.
- Find revenue, acceleration of revenue thresholds at while governments will reasonably slow growth through regulation

---

## 📚 Works Cited

- “Gross Domestic Product by State and Personal Income by State, 4th Quarter 2014–2023 and Preliminary 2015–24.” *U.S. Bureau of Economic Analysis*, 2016–2025.
- “State of the States 2015–2024: The AGA Analysis of the Commercial Casino Industry.” *American Gaming Association*, 2015–2024.
- Chat-GPT 4o was used to help with coding, formatting of text in readME file. Words and research all by Liam Riener and Kieran Santos
