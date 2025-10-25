[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/analytics-ak/funnel-drop-analysis/blob/main/funnel-drop.ipynb)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/analytics-ak/funnel-drop-analysis/main)
[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/kernels/welcome?src=https://github.com/analytics-ak/funnel-drop-analysis/blob/main/funnel-drop.ipynb)

# Funnel Drop Analysis — E-Commerce Conversion Study

## Project Overview
This project explores how online shoppers move through an e-commerce sales funnel — from visiting the homepage to completing a purchase. The main goal is to identify **where users drop off**, **why conversions decline**, and **what can be improved** to boost overall revenue.

In any online store, not every visitor becomes a buyer. Some leave after browsing products, others abandon their cart before checkout. By studying these behaviour patterns, we can uncover hidden issues in the user journey — such as confusing layouts, slow load times, or weak call-to-actions — and turn those insights into **practical, data-backed improvements**.

This analysis not only highlights the biggest problem areas in the funnel but also provides **clear recommendations** for product, marketing, and UX teams to improve conversion rates and customer experience.

## Objective
The main objective of this project is to understand how customers move through the e-commerce funnel and identify the points where they lose interest or drop off. Specifically, the analysis focuses on:

* **Finding the weakest funnel stage** — where most users exit before completing a purchase.
* **Comparing performance across devices and traffic sources** — to see how desktop, mobile, and tablet users behave differently.
* **Recommending actionable improvements** — simple design or experience changes that can help more visitors become paying customers.

In short, the goal is to turn raw user data into **clear insights** that can directly guide product and marketing decisions to improve conversions and revenue.

## Key Funnel Steps
The e-commerce journey is divided into five main stages that represent how a customer moves from browsing to buying:

**Home Page → 2. Product Page → 3. Cart → 4. Checkout → 5. Order Confirmation**

Each of these steps plays a key role in the buying process. The analysis tracks how many users **move forward** at each stage and how many **drop off** before completing their purchase. By measuring the percentage of users continuing from one step to the next, we can clearly see where potential customers lose interest — helping teams focus on the exact stages that need UX (User Experience) or marketing improvements.

## Main Metrics Used
To understand user behaviour and funnel performance, the following key metrics were analysed:

* **To Next Step Conversion %** — shows how many users move from one funnel stage to the next (e.g., from Product Page to Cart).
* **Overall Conversion %** — measures the total percentage of visitors who complete a purchase out of all who entered the funnel.
* **Bounce Rate** — indicates how many users leave after viewing just one page without taking any action.
* **Average Session Time** — tells how long users stay on the site, helping us understand engagement levels.
* **Cart Abandonment Rate** — shows how many users add items to the cart but don’t finish checkout, a key signal of lost revenue opportunities.

Together, these metrics paint a clear picture of where users are getting stuck and how efficiently the funnel turns visitors into customers.

---

## Data Analysis & Visuals
This section highlights the key analyses performed to understand how users behave at each stage of the e-commerce funnel. Each chart and table focuses on a specific part of the customer journey — showing where users drop off, how long they stay engaged, and what factors influence their likelihood to purchase. The visuals make it easier to spot patterns, compare performance across devices or countries, and identify areas that need the most attention.

### Conversion Rate by Month
The conversion rate isn’t constant throughout the year — it changes with time and seasonal trends. In this analysis, **March** recorded the **highest conversion rate (around 41%)**, while **February** showed the **lowest (about 37%)**. This pattern suggests that user intent and purchase behaviour may be influenced by **seasonal promotions, marketing campaigns, or product launches**.

<img src="Conversion Rate by Month.png" alt="Monthly Conversion Rate (Seasonality)" width="800">

*Insight: Conversions show strong seasonality, peaking in March at over 41.5% and hitting a low in February at 37.1%.*

### Funnel Drop-Off Analysis
The funnel analysis clearly shows that **most users exit on the Product Page**, before adding anything to their cart. This makes it the **biggest problem area** in the entire journey. Many visitors reach the Product Page but don’t take the next step — this could be due to unclear product details, lack of trust, limited images, or high prices. By improving the **Product Page experience** — such as better visuals, simpler CTAs (Call to Actions), or trust badges — we can help more users continue to the cart and complete their purchase.

| PageType     | UserCount | To_Next_Step_Conversion_% | Overall_Conversion_% |
|:-------------|:----------|:--------------------------|:---------------------|
| Home         | 5,000     | 79.74%                    | 100.00%              |
| Product Page | 3,987     | 40.11%                    | 79.74%               |
| Cart         | 1,599     | 70.23%                    | 31.98%               |
| Checkout     | 1,123     | 89.94%                    | 22.46%               |
| Confirmation | 1,010     | 0.00%                     | 20.20%               |

*Insight: The primary funnel leak is at the `product_page`, which sees a **59.9% drop-off** (from 79.7% to 31.9% overall conversion) before users add items to their cart.*

### Average Time to Conversion
Users who complete a purchase spend **much more time on the site** — around **388 seconds** on average — compared to **114 seconds** for non-buyers. This shows that **higher engagement often leads to higher conversion**. Encouraging users to explore more pages or interact longer can improve their chances of making a purchase.

**Average Session Duration Comparison**

| Purchased       | Session Duration (seconds) |
|:----------------|:---------------------------|
| 0 (Not Purchased) | 114.00                     |
| 1 (Purchased)   | 388.24                     |

*Insight: Users who purchase spend an average of **388 seconds**, 3.4 times longer than non-purchasers (114 seconds), indicating higher engagement is crucial for conversion.*

### Conversion Rate by Country
**France** has the highest conversion rate, meaning people there are more likely to buy after visiting the site. Countries like the **USA**, **India**, and the **UK** are not far behind — all show similar buying patterns.

<img src="Conversion Rate by Country.png" alt="Top 10 Countries by Conversion Rate" width="800">

*Insight: France leads with the highest conversion rate (over 40%), while other top countries show a tight, competitive performance around 38-40%.*

### Conversion by Items in Cart
Users who add **more items to their cart** are **more likely to complete a purchase** than those with just one or two items. This shows that higher interest or stronger buying intent often leads to a successful checkout.

<img src="Conversion by Items in Cart.png" alt="Conversion Rate vs. Number of Items in Cart" width="800">

*Insight: After an initial drop for 1-2 items, the conversion rate steadily **increases for carts with 3, 4, or 5 items**, suggesting users making larger purchases are more committed.*

### Conversion by Referral Source
Visitors coming from **Google** and **Email campaigns** convert slightly better than those from other traffic sources. This means users who find the site through search or email are usually more interested and ready to buy. It highlights the value of strong SEO and well-targeted email marketing.

<img src="Conversion by Referral Source.png" alt="Conversion Rate by Referral Source" width="800">

*Insight: All referral sources perform at a similar, healthy rate, with **Google (~42%)** and **Email (~39%)** traffic converting slightly better than other channels.*

### Time on Page by Buyers vs Non-Buyers
Both **buyers and non-buyers spend nearly the same amount of time** on each page. This means that just keeping users longer on the site doesn’t guarantee a sale — what really matters is **the quality and clarity of the content**.

<img src="Average Time on Page.png" alt="Average Time on Page: Buyers vs. Non-Buyers" width="800">

*Insight: Time on page is nearly identical for buyers and non-buyers, suggesting **page content or UX design**, not engagement time, is the main driver for conversion.*

### Conversion by Device Type
**Desktop and tablet users** tend to buy more often than **mobile users**. This shows that the mobile shopping experience may have some issues — like slower loading or smaller buttons — that affect conversions.

<img src="Conversion by Device Type.png" alt="Conversion by Device Type and Referral Source" width="800">

*Insight: **Desktop and Tablet** devices consistently outperform **Mobile** in conversion rates, highlighting a potential friction point in the mobile user experience.*

### Cart Abandonment Study
Cart abandonment rates are **nearly the same** across all devices and traffic sources. This means the issue isn’t limited to one group — it’s a **general problem** in the checkout process. Number of sessions that abandoned the cart: **589**

**Referral Source Distribution for Cart Abandonment**
| Referral Source | Percentage |
|:----------------|:-----------|
| Email           | 26.66%     |
| Google          | 25.47%     |
| Direct          | 24.28%     |
| Social Media    | 23.60%     |

**Device Distribution for Cart Abandonment**
| Device Type | Percentage |
|:------------|:-----------|
| Mobile      | 33.96%     |
| Tablet      | 33.79%     |
| Desktop     | 32.26%     |

*Insight: Cart abandonment is **evenly distributed** across all devices (32-34%) and referral sources (23-27%), suggesting a universal issue (e.g., shipping costs, complex checkout) rather than a segment-specific one.*

### User Path Tracking (Next Step Flow)
Most users follow a common path — **Home → Product Page → Cart**. However, many of them **drop off between the Product Page and the Cart**, showing that this step needs the most attention.

**Most Common Next Page from ‘Home’:**
| Next Page Type | Non-Buyer Count | Buyer Count |
|:---------------|:----------------|:------------|
| Product Page   | 2,977           | 1,010       |

**Most Common Next Page from ‘Product Page’:**
| Next Page Type | Non-Buyer Count | Buyer Count |
|:---------------|:----------------|:------------|
| Cart           | 589             | 1,010       |

*Insight: This data confirms the primary user flow (`home` → `product_page` → `cart`) and quantifies the significant user drop-off between the product page and the cart.*

---

## Quick Insights
* The biggest drop happens between the **Product Page and Cart**, with nearly **60% of users leaving** at this step.
* **Mobile users** show a **slightly lower conversion rate** compared to desktop and tablet.
* **Email traffic** brings in the **most engaged users**, converting better than social or direct visitors.
* **Cart abandonment** is slightly higher for **mobile and social media users**, showing they are less ready to buy or face friction during checkout.
* The **average session time** looks good overall, but improving load speed and simplifying navigation could make the buying process even smoother.

## Business Use Case
This analysis helps **product and marketing teams** understand which parts of the funnel need the most attention. It shows where users drop off, which traffic sources bring real buyers, and what design or experience changes can make the journey smoother. By using these insights, teams can make focused improvements that directly increase **conversions and revenue**.

## Real-World Applications
The insights from this project can be used in many practical ways, such as:
* **Marketing Optimisation:** Identify which channels bring the most valuable traffic and focus efforts there.
* **UX Improvement:** Spot pain points in the user journey and make design changes that keep users moving forward.
* **Product Strategy:** Use behaviour data to plan better product placements, offers, or features.
* **Revenue Forecasting:** Estimate how small conversion improvements can lead to big sales growth over time.

## Revenue Impact Estimation (Assumed Example)
This dataset doesn’t include actual revenue, so the numbers below are based on assumptions. If we consider **100,000 monthly sessions**, a **2.5% conversion rate**, and an **average order value (AOV)** of **$75**, then improving the **Product → Cart** step by just **10%** could add around **$18K–$20K in extra sales per month** — nearly **$200K+ per year**. This shows how even small improvements in a single funnel stage can create **big revenue gains** when applied across all users.

## Future Improvements
To make this analysis stronger and more actionable, the next steps could include:
* Adding real session and revenue data to connect user behaviour with actual financial results.
* Including demographic segmentation to see how age, location, or interests affect conversion.
* Use predictive models to identify users likely to drop off before they do.
* Building a live dashboard for tracking key funnel metrics in real time.

## What I Learned
* Learned how to **track and visualise user journeys** across the full e-commerce funnel.
* Understood how to **spot weak points** using conversion data and metrics.
* Gained experience in **explaining insights in simple business terms** that anyone can understand.
* Realized that even a **small percentage increase** in conversion can create a big impact on revenue.
* Learned how to **turn data into clear actions** that help improve sales and user experience.

## Project Summary and Conclusion
This project gave a complete view of how users move through the e-commerce funnel. By analysing each stage, it clearly showed **where users drop off**, **which channels drive quality traffic**, and **what changes can boost conversions**.

The biggest opportunity lies in improving the **Product → Cart** step and fixing **mobile UX issues**, as both directly affect the number of completed purchases. In short, this analysis proves that **data-driven decisions** can turn small optimisations into significant growth — improving user experience, conversions, and overall sales performance.

---

## How to Run the Project

To run this analysis on your local machine, please follow these steps:

```bash
# 1. Clone the repository
git clone https://github.com/analytics-ak/funnel-drop-analysis.git
cd funnel-drop-analysis

# 2. Install dependencies
# (It's recommended to use a virtual environment)
pip install pandas numpy matplotlib seaborn jupyter

# 3. Run the notebook
jupyter notebook "funnel-drop.ipynb"
```
---
## Profile & Dataset

* 🔗 **LinkedIn:** [View My Profile](https://www.linkedin.com/in/analytics-ashish/)
* 📂 **Dataset:** [Funnel Simulation Dataset on Kaggle](https://www.kaggle.com/datasets/sufya6/e-commerce-customer-journey-click-to-conversion)
* 💻 **GitHub Repository:** [Funnel Drop Analysis](https://github.com/analytics-ak/funnel-drop-analysis/)
* 📘 **Notebook:** [funnel-drop.ipynb](https://github.com/analytics-ak/funnel-drop-analysis/blob/main/funnel-drop.ipynb)

<br>

## Author: Ashish Kumar Dongre — Senior Data Analyst
I love working with data and finding simple insights that help businesses grow. Skilled in **Python (Jupyter, pandas, seaborn, matplotlib)**, and experienced in turning raw data into clear, useful reports.
