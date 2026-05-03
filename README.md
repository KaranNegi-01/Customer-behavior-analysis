# Customer-behavior-analysis
End-to-end customer shopping behavior analysis using Python, MySQL &amp; Power BI — uncovering spending patterns, customer segments, and product preferences from 3,900 transactions.

# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analysis project uncovering spending patterns, customer 
segments, and product preferences from **3,900 real transactions** — using 
Python for data preparation, MySQL for structured analysis, and Power BI 
for interactive dashboards.

## 📁 Dataset Overview

| Property | Details |
|----------|---------|
| Total Rows | 3,900 transactions |
| Total Columns | 18 |
| Missing Values | 37 (all in Review Rating) |

**Column Categories:**
- **Customer Demographics** — Age, Gender, Location, Subscription Status
- **Purchase Details** — Item, Category, Amount, Season, Size, Color
- **Shopping Behavior** — Discount Applied, Frequency, Review Rating, Shipping Type

---

## 🐍 Python — Data Preparation & Cleaning

- Imported dataset using `pandas`; explored structure with `df.info()` and `.describe()`
- Imputed 37 missing **Review Rating** values using **median per product category**
- Renamed all columns to `snake_case` for consistency
- **Feature Engineering:**
  - Created `age_group` by binning customer ages
  - Created `purchase_frequency_days` from purchase data
  - Dropped `promo_code_used` (redundant with `discount_applied`)
- Connected Python to **MySQL** and loaded the cleaned DataFrame for SQL analysis

---

## 🗄️ SQL Analysis — Key Queries & Findings

### 💰 Revenue & Spending
- Male customers generated **$157,890** vs **$75,191** for females — more than 2x
- **839 customers** used discounts yet spent above the average purchase amount
- Express shipping averaged **$60.48** vs **$58.46** for Standard

### 🛒 Products & Ratings
- **Top 5 by Avg Rating:** Gloves, Sandals, Boots, Hat, Skirt
- **Top sellers by category:**
  - Accessories → Jewelry (171 orders)
  - Clothing → Blouse & Pants (171 orders each)
  - Footwear → Sandals (160 orders)
  - Outerwear → Jacket (163 orders)

### 👥 Customer Segmentation
| Segment | Count |
|---------|-------|
| Loyal | 3,116 |
| Returning | 701 |
| New | 83 |

### 🔔 Subscriptions
- Non-subscribers (2,847) → **$170,436** revenue
- Subscribers (1,053) → **$62,645** revenue
- Average spend nearly identical: **$59.87** vs **$59.49**
- **2,518 repeat buyers** (>5 purchases) are not yet subscribed — conversion opportunity

### 🏷️ Discount Dependency
| Product | Discount Rate |
|---------|--------------|
| Hat | ~50% |
| Sneakers | ~49% |
| Coat | ~48% |
| Sweater | ~48% |
| Pants | ~47% |

### 📊 Revenue by Age Group
- Young Adults led at **$62,143**, with a gradual decline across older groups

---

## 📊 Power BI Dashboard

An interactive dashboard built with filters for **Subscription Status, Gender, 
Category, and Shipping Type.**

**Key KPIs displayed:**
- 👥 Total Customers: **3.9K**
- 💵 Avg Purchase Amount: **$59.76**
- ⭐ Avg Review Rating: **3.75**

**Visualizations include:**
- % of Customers by Subscription Status (27% Yes / 73% No)
- Revenue & Sales by Category
- Revenue & Sales by Age Group

---

## 💡 Key Findings

| Finding | Insight |
|---------|---------|
| Male Revenue Dominance | Males generated 2x female revenue — priority segment |
| Loyal Customer Base | 80% are loyal; only 83 new customers — acquisition gap |
| Discount Dependency | Top 5 products at 47–50% discount rate — margin risk |
| Subscription Gap | Only 27% subscribe despite strong repeat buying behavior |

---

## ✅ Business Recommendations

1. **Boost Subscriptions** — Target 2,518 non-subscribing repeat buyers with exclusive perks
2. **Loyalty Programs** — Convert 701 Returning customers into the Loyal segment
3. **Review Discount Policy** — Reassess Hat, Sneakers & Coat discount strategies
4. **Product Positioning** — Promote top-rated (Gloves, Sandals) & best-selling (Blouse, Jewelry) items
5. **Targeted Marketing** — Focus on Young Adults & express-shipping users for higher ROI

---

## 📂 Project Structure

\```
📦 customer-shopping-behavior-analysis
 ┣ 📂 data
 ┃ ┗ 📄 shopping_behavior.csv
 ┣ 📂 python
 ┃ ┗ 📄 data_cleaning.ipynb
 ┣ 📂 sql
 ┃ ┗ 📄 analysis_queries.sql
 ┣ 📂 dashboard
 ┃ ┗ 📄 customer_behavior.pbix
 ┗ 📄 README.md
\```

---

## 🙋‍♂️ Author

**Karan Negi**  
[LinkedIn](https://www.linkedin.com/in/karan-negi-1833a6363) • [GitHub](https://github.com/)
