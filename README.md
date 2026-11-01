🛍️ Customer Shopping Behavior Analysis

End-to-end analysis of 3,900 retail purchases using Python, PostgreSQL and Power BI, to understand what drives spending, loyalty and subscriptions and to turn that into marketing and product recommendations.

🎯 Business Problem

A retail company has seen shifting purchase patterns across demographics and product categories. The goal: how can customer shopping data be used to identify trends, improve engagement, and optimize marketing and product strategy? See 📄 Business Problem Document.

🧰 Tech Stack
Stage	Tool
🧹 Data cleaning & feature engineering	Python (pandas)
🗄️ Storage & analysis	PostgreSQL, SQL
📊 Visualization	Power BI
📝 Reporting	PDF report
📁 Project Files
File	Description
🐍 Customer_Shopping_Behaviour.ipynb	Python data cleaning & loading to PostgreSQL
🗃️ customer_behaviour_queries.sql	10 business-question SQL queries
📊 customer_behavior_dashboard.pbix	Power BI dashboard
📄 Business_Problem_Document.pdf	Business problem statement
📝 Customer_Shopping_Behavior_Analysis.pdf	Full analysis report & recommendations
📦 Dataset

3,900 purchases, 18 columns: demographics (age, gender, location, subscription status), purchase details (item, category, amount, season, size, color) and behaviour (discount, previous purchases, frequency, review rating, shipping type). 37 missing values in Review Rating.

🔄 Workflow
🐍 Python (notebook) – load data, impute missing review ratings with the per-category median, convert column names to snake_case, create age_group and purchase_frequency_days, drop promo_code_used (identical to discount_applied), load into PostgreSQL.
🗃️ SQL (queries) – 10 queries covering revenue by gender and age group, discount behaviour, top-rated and top-selling products, shipping comparison, subscriber value, and New / Returning / Loyal segmentation.
📈 Power BI (dashboard) – interactive dashboard of the key trends.
💡 Key Recommendations
🔔 Boost subscriptions with exclusive subscriber benefits
🏆 Reward repeat buyers to move them into the “Loyal” segment
💸 Review discount policy to balance sales lift against margin
⭐ Highlight top-rated and best-selling products in campaigns
🎯 Target high-revenue age groups and express-shipping users

Full findings: 📝 Analysis Report

🚀 How to Run
Install the libraries: pip install pandas sqlalchemy psycopg2-binary jupyter
Download the dataset and keep it next to the notebook as customer_shopping_behavior.csv
Create a PostgreSQL database named customer_behaviour
Set your login as environment variables (never hard-code a password):
export DB_USER=postgres and export DB_PASSWORD=your_password
Run the notebook, then the SQL queries
Open the Power BI dashboard in Power BI Desktop
