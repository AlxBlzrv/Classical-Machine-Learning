# Association Rules and Apriori Algorithm

## Introduction

Association rules are a popular data mining technique used to discover interesting relationships between variables in large datasets. These relationships are often represented in the form of "if-then" statements, where the presence of one set of items in a transaction implies the presence of another set of items. The most well-known algorithm for mining association rules is the Apriori algorithm.

### Apriori Algorithm

The Apriori algorithm works by identifying frequent itemsets in a dataset and then extending them to larger itemsets as long as those itemsets appear sufficiently often in the dataset. The algorithm uses a bottom-up approach, where frequent subsets are extended one item at a time, and groups of candidates are tested against the data.

Key metrics used in association rules include:
- **Support:** The proportion of transactions in the dataset that contain a particular itemset.
- **Confidence:** The likelihood that a transaction containing the antecedent also contains the consequent.
- **Lift:** The ratio of the observed support to that expected if the antecedent and consequent were independent.

## Project Overview

This project demonstrates the application of the Apriori algorithm to discover association rules in a retail dataset. The dataset used is the "Online Retail Dataset" from Kaggle, which contains transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.

### Data Loading and Preprocessing

The dataset is loaded, and basic preprocessing steps are performed, including:
- Removing leading and trailing spaces from item descriptions.
- Dropping rows with missing `InvoiceNo`.
- Converting `InvoiceNo` to string type.
- Removing credit transactions (where `InvoiceNo` contains 'C').

### Creating a Basket of Purchases

A basket of purchases is created for the United Kingdom, where quantities are converted to binary values (1 if the item was purchased, 0 otherwise).

### Applying Apriori Algorithm

The Apriori algorithm is applied to find frequent itemsets with a minimum support of 1%. Association rules are then generated from these frequent itemsets with a lift threshold of 1.

### Sorting and Analyzing Rules

The generated rules are sorted by confidence and support in descending order to identify the strongest rules.

### Visualization

Several visualizations are created to better understand the data and the generated rules:
- **Scatter Plot:** Visualizes the support and confidence of the rules, with the size of points representing the lift.
- **Histograms:** Show the distribution of support, confidence, and lift.
- **Heatmap:** Visualizes the correlations between the top 20 most frequent items.

### Output

The top 10 association rules with the highest confidence and support are printed.

## Conclusion

This project demonstrates the use of the Apriori algorithm for discovering association rules in a retail dataset. By understanding the relationships between items, businesses can make informed decisions on product placements, cross-selling, and promotions, ultimately improving sales and customer satisfaction.
