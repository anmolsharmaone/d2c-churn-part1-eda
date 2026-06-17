Data Quality Report

Dataset Overview

The data consists of 7 files: customer details, orders, customer support tickets, web activity, campaign history, churn labels, and a modelling snapshot (prepared for the dataset).

Dataset sizes:

- customers: 2400 rows
- orders: 10009 rows
- support_tickets: 1921 rows
- web_events_snapshot: 2400 rows
- intervention_history: 2400 rows
- churn_labels: 2400 rows
- rfm_modeling_snapshot: 2400 rows

Missing Values

The most important missing data were in the customer profile data.

- loyalty_tier: 1386 missing values
- skin_type: 401 missing values
I'm getting this error when I view the orders table.I'm seeing this error when I look at the orders table.

Observations:

More than half of the customers don't have the loyalty_tier field. This is probably a result of customers not joining the loyalty program, or of the information not being recorded.

The skin_type is a smaller proportion of missing data and seems to be a profile variable that is optional.

The number of missing ratings are less than 1% of all orders, and this is not likely to significantly affect analysis.

Recommended Handling:

Fill in missing loyalty tier data with "Unknown"
Fill in missing skin_type values with "Unknown".
Look for gaps in ratings, and add mean rating if needed when modeling.

Duplicate Records

All datasets were subject to "duplicate" checks.

There were no significant duplicate records found.

As the name implies, the customer-level datasets have one row per customer, and the orders and tickets have multiple rows per customer as we'd expect.

Join Integrity

All datasets were searched for customer IDs.

Findings:

All records of orders refer to valid customers.
All support tickets are correlated with valid customers
- All Web activity logs are tied to valid customers.
All campaign records are matched to legitimate customers.
All churn records are correlated with valid customers.

There are no orphan records.

Customer Coverage

Each customer is in the list of:

- customers
- web_events_snapshot
- intervention_history
- churn_labels
- rfm_modeling_snapshot

Additional observations:

- 2400 customers have an order history available.
Of the 1247 customers, 1247 have support tickets.

This implies that there could be behavioral indicators in the form of support interactions which are of critical importance for churn analysis.

Date Fields

The data set has several Date columns:

- signup_date
- order_date
- ticket_date
- snapshot_date

No significant problems were noted in loading the date format.

Prior to analysis, all date fields were converted to datetime.

Potential Outliers

There may be outliers in:

- gross_amount
- delivery_days
- resolution_hours
- recency_days
- monetary_180d

The following values have been preserved as they may be representative of customer behavior and not data errors.

Leakage Considerations

There is a special concern for constructing predictive models.

These are fields that are not suitable for use as input features:

- churn_next_60d
- split

The target variable is the future customer behavior and it shouldn't be used as part of the model training.

If creating features from raw datasets, then only information available on or before the snapshot date should be used.

Final Assessment

The overall data quality is good and the dataset can be used for customer analytics and churn modelling.

The key areas that need to be addressed are:

- High missingness in loyalty_tier
Moderate missingness in skin_type = 48.79%.Moderate missingness in skin_type = 48.79%.
- Careful controlling of target leakage during modelling

No significant problems with duplicates, joins, or missing data sets were detected.
