<div align="center">

# Funnel Drop Analysis

**Python | Pandas | Matplotlib | Seaborn | SciPy**

Finding where users drop off in an online store — and what it is actually costing the business.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4C72B0)
![SciPy](https://img.shields.io/badge/SciPy-1.x-8CAAE6?logo=scipy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/analytics-ak/funnel-drop-analysis/blob/main/funnel_drop_analysis.ipynb)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/analytics-ak/funnel-drop-analysis/main?labpath=funnel_drop_analysis.ipynb)

</div>

---

## The Short Version

5,000 users visited this store. Only 1,010 bought something. That is a 20.2% overall conversion rate.

The other 3,990 users left without buying — and nearly 60% of the total loss happens at one single step: the **Product Page to Cart transition**.

This analysis finds exactly where the funnel breaks, tests four possible explanations using statistical methods, rules out three of them, and points to the one fix that will have the highest business impact.

---

## The Core Problem

**2,388 users reached the Product Page and did not add anything to cart.**

That is the biggest drop in the entire funnel. Users are landing on product pages, spending time there, and still leaving without taking action.

Using an industry-standard average order value of $50 and the current 20.2% conversion rate as a baseline — recovering just **10% of those lost Product Page sessions** would add approximately **$11,900 in revenue per 5,000 sessions**. At scale, across real traffic volumes, this number grows significantly.

The problem is not checkout. It is not mobile. It is not where traffic comes from. It is the Product Page itself failing to convince users to act.

![Funnel Analysis](images/01_funnel_analysis.png)

---

## What the Numbers Show

| Funnel Step | Sessions | Drop to Next Step | What It Means |
|---|---|---|---|
| Home | 5,000 | 20.26% | Normal drop — most sites see this |
| Product Page | 3,987 | **59.89%** | **The main problem — nearly 60% leave here** |
| Cart | 1,599 | 29.77% | Moderate drop — worth watching |
| Checkout | 1,123 | 10.06% | Low drop — checkout is working fine |
| Confirmation | 1,010 | — | Final purchases |

Once users add something to the cart, most of them actually finish buying. The battle is not at checkout. It is getting that first item into the cart.

---

## Four Things Tested — Three Ruled Out

Before pointing at the Product Page, four possible explanations were tested properly using statistical methods — not just eyeballing charts.

| Factor | How It Was Tested | Result |
|---|---|---|
| Device type | Chi-square test | **No difference** — p = 0.98. Desktop, mobile, tablet all behave identically |
| Referral source | Chi-square test | **No difference** — p = 0.47. Google, social, email, direct all convert similarly |
| Time of visit | Hour and day analysis | **No pattern** — conversion is flat across all hours (20–23%) and all days (18–22%) |
| Product page engagement | Avg time comparison | **Same for everyone** — buyers and non-buyers both spend ~96–97 seconds on the product page |

All four tested. Three ruled out with statistical confidence. The problem is not traffic quality, not device, not timing. It is the product page itself.

---

## What the Data Actually Shows

### The product page is getting attention — just not converting it

Buyers and non-buyers spend the same amount of time on the product page (~96 seconds). Users are not bouncing immediately. They are reading, looking, and still not clicking Add to Cart. That points to a persuasion problem — not a traffic problem.

![Funnel Drop-Off](images/05_funnel_analysis_premium.png)

---

### The first item is everything

Sessions with 0 items in cart have 0% conversion. The moment a user adds just 1 item, conversion jumps to 35–38%. Adding more items after that changes almost nothing.

The entire conversion battle is about getting that first item added. Everything else is secondary.

![Cart Intensity](images/06_conversion_rate_analysis.png)

---

### Buyers spend 4x longer on the site — but not on the product page

Non-buyers spend about 90 seconds total on the site. Buyers spend around 388 seconds. The difference is not because buyers read product pages more carefully — both groups spend the same time there. Buyers simply visit more pages because they go through more funnel steps.

![Session Duration](images/04_session_analysis_highres.png)

---

### All devices behave the same

Desktop, mobile, and tablet users drop at exactly the same rate at every funnel step. There is no mobile problem here.

![Device Funnel](images/02_device_funnel.png)
![Device Heatmap](images/03_device_conversions_heatmap.png)

**Chi-square test: p = 0.98** — statistically no difference between devices.

---

### Referral source barely matters

Google converts at ~42%, Social Media at ~38%. The gap is small and not statistically significant. All sources show the same funnel pattern.

![Referral Source](images/07_referral_conversion_premium.png)

**Chi-square test: p = 0.47** — no significant difference between referral sources.

---

### Time of visit changes nothing

Conversion is flat across every hour of the day and every day of the week. There is no peak time worth targeting.

![Time Based](images/08_time_based_conversion.png)

---

## What Was Expected vs What Actually Happened

| Assumption | Expected | Reality |
|---|---|---|
| Biggest drop at Product Page → Cart | ✅ True | 60% drop — confirmed as the main problem |
| Mobile users convert less | ❌ False | All devices perform identically (p = 0.98) |
| More time on product page = more likely to buy | ❌ False | Buyers and non-buyers spend the same time there |
| Social media traffic converts worse | ❌ False | All sources are similar (p = 0.47) |
| More items in cart = higher conversion | ⚠️ Partially true | First item matters most — after that it flattens |

Three out of five assumptions were wrong. This is why testing with data matters.

---

## What Should Be Done

The highest impact will come from focusing on the Product Page → Cart transition. Everything else has been tested and ruled out.

| Problem | Action | Expected Impact |
|---|---|---|
| Users read product pages but do not add to cart | Make the Add to Cart button more prominent and easier to find | Direct impact on the 59.89% drop rate — even a 5% recovery adds ~$6,000 per 5,000 sessions |
| Users are not convinced to act | Improve product images, descriptions, and pricing clarity | Reduces decision friction at the exact point where users are already engaged |
| Users do not trust the site enough to buy | Add trust signals — reviews, ratings, return policy, guarantees | Addresses hesitation for users who spend time on the page but still leave |
| Cart abandonment exists (~589 sessions) | Add cart reminder or urgency signals | Secondary priority — checkout is already working well |

**Fixing the Product Page is the only lever that matters here.** Device, traffic source, and time of visit have all been ruled out. The data is specific about where the problem is.

---

## A Note on the Dataset

After working through this data, one thing became clear — the numbers across devices, referral sources, and countries are almost identical. In real e-commerce, that never happens. Mobile and desktop always behave differently. Paid and organic traffic always show different patterns.

This dataset is most likely synthetically generated. That is called out in the notebook because recognising data limitations is just as important as the analysis itself.

The analysis approach, funnel logic, statistical tests, and the way findings are connected — all of that works the same whether the data is real or synthetic. But the specific numbers should not be taken as benchmarks for real business decisions.

---

## Data Quality Checks

Before any analysis, the data was validated:

- No missing values across all 10 columns
- Funnel path validation — all 5,000 sessions follow the correct step order. Every session is clean.
- Timestamps converted to datetime and sorted by session and time

---

## Dataset

| Detail | Info |
|---|---|
| **Source** | [Kaggle — E-Commerce Funnel Data](https://www.kaggle.com/datasets/sufya6/e-commerce-customer-journey-click-to-conversion) |
| **Total Rows** | 12,719 |
| **Total Sessions** | 5,000 |
| **Columns** | 10 |
| **Time Period** | January 2025 – August 2025 |
| **Type** | Synthetic |

---

## Tools Used

| Tool | Used For |
|---|---|
| Python | Data cleaning, analysis, funnel calculations |
| Pandas | Session-level and page-level data operations |
| NumPy | Numerical computations |
| Matplotlib | Funnel charts, bar charts, comparison plots |
| Seaborn | Heatmaps, violin plots, styled visuals |
| SciPy | Chi-square statistical tests |
| Jupyter Notebook | Full analysis in one place, start to finish |

---

## Project Structure

```
funnel-drop-analysis/
│
├── funnel_drop_analysis.ipynb    ← Full analysis notebook
├── README.md                     ← You are reading this
│
└── images/
    ├── 01_funnel_analysis.png
    ├── 02_device_funnel.png
    ├── 03_device_conversions_heatmap.png
    ├── 04_session_analysis_highres.png
    ├── 05_funnel_analysis_premium.png
    ├── 06_conversion_rate_analysis.png
    ├── 07_referral_conversion_premium.png
    └── 08_time_based_conversion.png
```

---

## How to Run This

1. Clone this repo
   ```bash
   git clone https://github.com/analytics-ak/funnel-drop-analysis.git
   ```
2. Install required libraries
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```
3. Open the notebook
   ```bash
   Jupyter Notebook funnel_drop_analysis.ipynb
   ```
4. Run all cells — charts generate automatically

This analysis shows that conversion is not limited by traffic or checkout — it is driven by the ability to convert product interest into action at a single critical step.

---

## Author

**Ashish Kumar Dongre**

🔗 [LinkedIn](https://www.linkedin.com/in/ashish-kumar-dongre-742a6217b/) &nbsp;|&nbsp; 💻 [GitHub](https://github.com/analytics-ak/funnel-drop-analysis/) &nbsp;|&nbsp; 📂 [Dataset on Kaggle](https://www.kaggle.com/datasets/sufya6/e-commerce-customer-journey-click-to-conversion)
