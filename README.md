# E-Commerce Customer Analytics & ETL Pipeline
📊 **Domain:** Business Intelligence, Data Engineering, Retail & E-Commerce

---

## 💼 Business Case & Objective
In the retail sector, understanding consumer behavior, promotion efficiency, and lifetime loyalty is critical for maximizing profit margins. 

This project establishes a robust **end-to-end data processing infrastructure** that automates the extraction, transformation, and loading (ETL) of raw transaction logs into a relational database system. The database is then utilized to deliver deep market-basket insights, customer lifetime segmentation, and cohort performance dashboards for executive decision-making.

---

## 🛠️ Technical Skillset Demonstrated
* **Data Engineering (ETL):** Automated Python pipeline mapping programmatic object-relational logic (SQLAlchemy, Psycopg2) to structured storage engines.
* **Data Quality & Manipulation:** Advanced multi-level feature grouping, data distribution evaluation, null-value structural imputation, and anomaly filtering via Pandas.
* **Advanced Database Analytics:** Complex SQL implementations leveraging Window Functions (`ROW_NUMBER()`), Conditional Aggregations (`CASE WHEN`), Common Table Expressions (CTEs), and relational subqueries.

---

## ⚡ Data Pipeline & Engineering Architecture
The data pipeline processes **3,900 customer profiles** through an enterprise cleaning architecture before analytical reporting:

1. **Strategic Imputation Layer:** Handled non-random missing data records in review rankings by computing and mapping historical category medians to preserve data distribution profiles.
2. **Database Integrity Formatting:** Enforced algorithmic naming syntax conversion across features (lowercase transformation and system snake-case replacements) to secure native cross-platform SQL query support.
3. **Dimensional Deduplication:** Applied absolute validation matrix checking to verify a 1:1 perfect multicollinearity map between promotional categories, safely pruning redundant data fields.
4. **Quantile Behavioral Binning:** Binned continuous multi-generation demographic variables into equal-frequency user cohorts (`young_Adult`, `Adult`, `Middle-aged`, `Senior`) via mathematical quantile partitions.

---

## 🎯 Strategic Business Insights Generated
The SQL analytics engine evaluates key business performance indicators across several major vectors:

* **Customer Segmentation:** Programmed an RFM-aligned categorical scoring logic allocating active user accounts into dedicated target pools (`New`, `Returning`, `Loyal`) to empower personalized marketing campaigns.
* **Subscription Revenue Modeling:** Evaluated core performance margins between direct contract members and standard shoppers, highlighting volume velocity, transactional values, and aggregate lifetime values.
* **Promotional Conversion Efficiency:** Quantified exactly which product lines rely most heavily on discount mechanics to trigger successful conversion metrics.
* **Inventory Rank Mapping:** Implemented isolated categorization ranks to safely filter out top-performing product variants across dynamic merchandise silos without distorting historical trend variances.

---

## 📂 Repository Contents & Structure
The repository is organized following industry-standard clean architecture guidelines:
* 📂 **`dataset/`**: Container folder protecting the raw data source asset.
  * 📄 `customer_shopping_behavior.csv`: The primary e-commerce transactional dataset (3,900 records).
* 📄 **`customer_shopping_behavior.ipynb`**: Complete Jupyter documentation executing the data validation, cohort transformations, and pipeline loading.
* 📄 **`analytical_queries.sql`**: Production-ready, commented PostgreSQL code addressing executive analytics briefs.

---

## 🚀 How to Replicate Locally

### 1. Prerequisites
Ensure you have Python 3.x and PostgreSQL installed locally.

### 2. Environment Setup
```bash
pip install pandas psycopg2-binary sqlalchemy
```

### 3. Run the ETL Pipeline
1. Open the Jupyter Notebook `customer_shopping_behavior.ipynb`.
2. Ensure your local PostgreSQL server is active.
3. Update the database connection credentials inside cell 28:
   ```python
   username = "your_postgres_user"
   password = "your_password"
   database = "customer_behavior"
   ```
4. Run all notebook cells to automatically pull from the relative `dataset/` directory, process the metrics, and stream the schema directly into your active PostgreSQL database instance.

### 4. Executive Reporting
Open your preferred SQL client (e.g., pgAdmin or terminal CLI), connect to the newly created database table, and run `analytical_queries.sql` to generate active business intelligence reports.
---------
