# 🛍️ Customer Shopping Behavior Analysis

End-to-end analysis of 3,900 retail purchases using **Python, PostgreSQL and Power BI**, to understand what drives spending, loyalty and subscriptions and to turn that into marketing and product recommendations.

## 🎯 Business Problem
A retail company has seen shifting purchase patterns across demographics and product categories. The goal: *how can customer shopping data be used to identify trends, improve engagement, and optimize marketing and product strategy?* See [`reports/Business_Problem_Document.pdf`](reports/Business_Problem_Document.pdf).

## 🧰 Tech Stack
| Stage | Tool |
|---|---|
| 🧹 Data cleaning & feature engineering | Python (pandas) |
| 🗄️ Storage & analysis | PostgreSQL, SQL |
| 📊 Visualization | Power BI |
| 📝 Reporting | PDF report |

## 📁 Repository Structure
```
├── notebooks/   Python data cleaning & loading to PostgreSQL
├── sql/         10 business-question queries
├── dashboard/   Power BI dashboard (.pbix)
├── reports/     Business problem document & full analysis report
├── data/        Place the raw CSV here (git-ignored)
├── requirements.txt
└── README.md
```

## 📦 Dataset
3,900 purchases, 18 columns: demographics (age, gender, location, subscription status), purchase details (item, category, amount, season, size, color) and behaviour (discount, previous purchases, frequency, review rating, shipping type). 37 missing values in `Review Rating`.

## 🔄 Workflow
1. 🐍 **Python** – load data, impute missing review ratings with the per-category median, convert column names to snake_case, create `age_group` (quartile bins) and `purchase_frequency_days`, drop `promo_code_used` (identical to `discount_applied`), load into PostgreSQL.
2. 🗃️ **SQL** – 10 queries covering revenue by gender and age group, discount behaviour, top-rated and top-selling products, shipping comparison, subscriber value, and New / Returning / Loyal segmentation.
3. 📈 **Power BI** – interactive dashboard of the key trends.

## 💡 Key Recommendations
- 🔔 Boost subscriptions with exclusive subscriber benefits
- 🏆 Reward repeat buyers to move them into the "Loyal" segment
- 💸 Review discount policy to balance sales lift against margin
- ⭐ Highlight top-rated and best-selling products in campaigns
- 🎯 Target high-revenue age groups and express-shipping users

## 🚀 How to Run
```bash
pip install -r requirements.txt
export DB_USER=postgres
export DB_PASSWORD=your_password 
```
1. Put `customer_shopping_behavior.csv` in `data/`
2. Create a PostgreSQL database named `customer_behaviour`
3. Run `notebooks/Customer_Shopping_Behaviour.ipynb`
4. Run the queries in `sql/customer_behaviour_queries.sql`
5. Open `dashboard/customer_behavior_dashboard.pbix` in Power BI Desktop
