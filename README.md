# Banking Data Pipeline: ETL & Data Cleaning

This repository contains the Python ('.ipynb') code for the ETL (Extract, Transform, Load) and Data Cleaning phase of the **End-to-End Banking Card Analytics & Fraud Detection** project.

## 🛠️ Tech Stack Used
* **Python:** 'Pandas'
* **Target Data Warehouse:** 'Google BigQuery'

## 🧹 Key Transformations
* Data Extraction & Consolidation: Extracted and cleaned 5 raw datasets (Transactions, Cards, Users, MCC Codes, and Fraud Labels) containing over **13.3 million transactions**.
* Data Type & Date-time Standardization: Parsed date strings (date, expires, acct_open_date) into proper datetime objects and resolved mixed data types by explicitly casting columns like zip, merchant_state, and errors to strings.
* Currency Formatting: Stripped string symbols ($ and ,) from financial columns across multiple tables (e.g., amount, credit_limit, yearly_income, total_debt) and properly cast them to float values.
* Binary Encoding: Mapped categorical boolean flags (e.g., 'Yes'/'No' for has_chip, card_on_dark_web, and fraud_label) into machine-readable binary integers (1/0).
* Logical Missing Value Imputation: Handled nulls based on business context, such as filling missing errors with "No Error", and missing merchant_state or zip with "Unknown".
* Outlier Preservation: Deliberately retained business-critical outliers (e.g., massive transaction amounts, negative chargebacks) to train the Fraud Detection model effectively on real-world anomalies.

👉 **View Full Project Portfolio:** https://jazzy-glade-f06.notion.site/3a56ce984c60804d9429fdbfeb3353e7](https://jazzy-glade-f06.notion.site/H-Th-ng-Ph-n-T-ch-D-ng-Ti-n-C-nh-B-o-R-i-Ro-Th-Ng-n-H-ng-3a56ce984c60804d9429fdbfeb3353e7
