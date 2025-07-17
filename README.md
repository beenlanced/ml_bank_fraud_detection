Predict fair taxi price

Problem:

This project looks at detecting bank fraud by detecting outliers or anomalies from unlabled bank transactions.

Anti-Money Laundering (AML) and fraud analytics require one to consider several factors when building production based systems.

We have to consider the **limitations of the financial institution**. For example, how up to date are the systems of the institution as it is important to understand will new technology be needed to handle all of the possible feature information that machine learning (ML) models can capture and can the current systems handle real-time decision making.

**Balancing customer experiences with bank losses**. Like medical doctors, we should do no harm. Alerts generated from ML models should not impact legit customers too much. At best, inconveniences should inspire a sense of confidence that the institution is looking out for the well-being of its customers. It is standard that banks and financial institutions will have to take on some losses, but tools should help identify the line between customer annoyance and mitigating business losses.

Lastly, **understand the operation teams capacity**. While, the ML system can send anomalous transactions to agents for follow-up for further investigation and support. A priortization scheme may need to be implemented first to optimize mitigating large accounts and larger losses first. An unfortunate consequence, is that small, infrequent irregular cases may not get investigated because they do not meet largeness thresholds.

### The problem

This project focuses on creating a Machine Learning model to identify the anomolous events, which would then be sent to operation and support teams for futher investigation. It presents a method for anomaly detection using the technique fo Isolation Forests.

### Why Isolation Forest?

According to [Wikipedia](https://en.wikipedia.org/wiki/Isolation_forest):

The Isolation Forest (iForest) algorithm took advantage of the attributes of anomalies being “few and different”, they are easier to “isolate” compared to normal points. So instead of trying to build a model of normal instances, it explicitly isolates anomalous points in the dataset.

The main advantage of this approach is the possibility of exploiting sampling techniques to an extent that is not allowed to the profile-based methods, creating a very fast algorithm with a low memory demand.

Isolation Forest is an efficient and simple algorithm used for anomaly detection which makes it a popular choice in industries like cybersecurity, finance and healthcare. It identifies outliers in large datasets by isolating them through binary partitioning which requires minimal computational overhead. This ability to quickly finding anomalies is important in applications where detecting unusual patterns is key to safeguarding against risks or identifying hidden insights.

Key Concepts in Isolation Forest
Let's see some key concepts that define Isolation Forest:

- `Isolation:` The algorithm isolates anomalies by focusing on their differences from normal data points rather than their similarities. Anomalies are typically rare and distinct from the majority helps in making them easier to isolate.

- `Partitioning:` Data is split by randomly selecting features and using random values to partition the data. This helps in efficiently isolating anomalies from normal data.

- `Anomaly Score:` It measures how easily a data point can be isolated. Points that require fewer splits to isolate are considered anomalies and assigned higher scores.

### What this Project does speciffically Specifically

- Loads and inspects the bank data
- Preprocesses/cleans the data
- Cluster the data using unsupervised learning algorithm: [Isolation Forest](https://en.wikipedia.org/wiki/Isolation_forest)
- Identify anomalies and outliers
- Visualizes results using Seaborn

## acknowledge:

- [How to apply Unsupervised Anomaly Detection on bank transactions](https://www.justintodata.com/unsupervised-anomaly-detection-on-bank-transactions-outliers/) from authors of https://www.justintodata.com as the inspiration for this project.

A pretty handy tutorial on [Isolation Forest for Outlier Detection with Python](https://www.youtube.com/watch?v=O9VvmWj-JAk)

dataset
[1999 Czech Financial Dataset - Real Anonymized Transactions](https://data.world/lpetrocelli/czech-financial-dataset-real-anonymized-transactions)

using the transaction csv file

In this notebook, I will detect outliers using the unsupervised learning algorithm: [Isolation Forest](https://en.wikipedia.org/wiki/Isolation_forest).

### Why Isolation Forest?

According to [Wikipedia](https://en.wikipedia.org/wiki/Isolation_forest):

The Isolation Forest (iForest) algorithm took advantage of the attributes of anomalies being “few and different”, they are easier to “isolate” compared to normal points. So instead of trying to build a model of normal instances, it explicitly isolates anomalous points in the dataset.

The main advantage of this approach is the possibility of exploiting sampling techniques to an extent that is not allowed to the profile-based methods, creating a very fast algorithm with a low memory demand.

Isolation Forest is an efficient and simple algorithm used for anomaly detection which makes it a popular choice in industries like cybersecurity, finance and healthcare. It identifies outliers in large datasets by isolating them through binary partitioning which requires minimal computational overhead. This ability to quickly finding anomalies is important in applications where detecting unusual patterns is key to safeguarding against risks or identifying hidden insights.

Key Concepts in Isolation Forest
Let's see some key concepts that define Isolation Forest:

- `Isolation:` The algorithm isolates anomalies by focusing on their differences from normal data points rather than their similarities. Anomalies are typically rare and distinct from the majority helps in making them easier to isolate.

- `Partitioning:` Data is split by randomly selecting features and using random values to partition the data. This helps in efficiently isolating anomalies from normal data.

- `Anomaly Score:` It measures how easily a data point can be isolated. Points that require fewer splits to isolate are considered anomalies and assigned higher scores.

A pretty handy tutorial on [Isolation Forest for Outlier Detection with Python](https://www.youtube.com/watch?v=O9VvmWj-JAk)

Uses:
`IForest` Isolation Forest (iForest) algorithm for anomaly detection
`FacetGrid` seaborn figure type for visualization.
`PyOD` a comprehensive but easy-to-use Python library for detecting anomalies in multivariate data and for plotting resutls

### Using a PyOD Visualization tool

taken from [src](https://github.com/yzhao062/pyod/blob/master/examples/compare_all_models.py)
