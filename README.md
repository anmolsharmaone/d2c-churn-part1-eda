##Customer Churn Intelligence & Retention for D2C brands.

Business Understanding, Exploratory Data Analysis, and Data Audit will be covered in Part 1.Part 1 covers Business Understanding, Exploratory Data Analysis, and Data Audit.

Project Overview

The objective of this project is to gain understanding into the behavior of customers who have churned from a Direct-to-Consumer (D2C) personal care brand. The goal of Part 1 is to review the existing data sets, evaluate data quality, analyze the data, and formulate business hypotheses that could help explain why customers are churning.

The results of this analysis will be used for future customer segmentation, churn prediction modelling and designing retention strategies.

Repository Contents

- eda_audit.ipynb
  Make a notebook for exploratory data analysis.Prepare an exploratory data analysis notebook.

- data_quality_report.md
  The summary provides the results of data quality analysis, risks and recommendations.

- business_memo.md
  Business-level overview of important churn learnings and priorities for retention

- requirements.txt
  - Required Python libraries

Datasets Used

The analysis will be based on the following datasets which are part of the capstone project:

- customers.csv
- orders.csv
- support_tickets.csv
- web_events_snapshot.csv
- intervention_history.csv
- churn_labels.csv
- rfm_modeling_snapshot.csv

This dataset is not part of this repository.

You are expected to download the data set from the registered capstone Google Drive link and store this locally in the data folder before running the notebook.

Analysis Performed

Data Audit

Inventories the datasets and inspects the schemas.Inventories datasets and inspects schemas.
- Missing value assessment
- Duplicate record checks
- Customer coverage validation
- Join integrity verification
- Leakage risk identification

Exploratory Data Analysis

- Customer profile analysis
- Order behavior analysis
- Monetary value analysis
- Customer engagement analysis
- Loyalty tier distribution
- Churn distribution analysis

Churn Risk Hypotheses

The analysis found that there were multiple factors correlated with churn risk:

Customers have not been active for a long time (recency)
- Low purchase frequency
- Lower customer spending
- Reduced website/app engagement
What might happen if a child is not supported or returns to the setting?What could be the consequences of a child not being supported or returning to the setting?

Key Findings

Customers that churned were also much more likely to be inactive.
Customers who made fewer purchases had higher churn rates.
The churn rate for lower-spending customers was higher.
Increased churn risk was linked to a reduced digital engagement.
There is a need to further explore the service behaviour and the return behaviour of the customer.

Tools and Libraries

The project was developed using:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

How to Run

1. Clone the repository

git clone <repository-url>

2. Install dependencies

pip install -r requirements.txt

4. Read the capstone data.
5. Read in the capstone data.

6. Generate the CSV files for all the schools in that local data folder

5. Open and run:

eda_audit.ipynb

Output Files

- Exploratory analysis notebook
- Data quality assessment
Business memo summarizing findings -
The hypotheses concerning the churn risk were validated.The hypotheses related to churn-risk were backed by data.

Author
Anmol Sharma
Capstone Project Submission – Part 1
Data Audit, EDA & Business Understanding
