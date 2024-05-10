# Market Basket Analysis

## Author
Anuradha Sahithi Padavala

## Introduction
Market basket analysis is a technique used to discover co-occurrence relationships among activities performed by subjects. This analysis helps in understanding the buying behavior of customers, which can be leveraged to promote products effectively. For example, promoting conditioner alongside shampoo could potentially increase shampoo revenue due to their co-occurrence in shopping baskets.

## Metrics
### Support
Support is an indication of how frequently the itemset appears in the dataset.
- **Support(X)**: `frequency(X)/N`
- **Support(A=>B)**: `frequency(A,B)/N`

### Confidence
Confidence is an indication of how often the rule has been found to be true.
- **Confidence(A=>B)**: `P(A∩B)/P(A) = frequency(A,B)/frequency(A)`

### Lift
Lift indicates the correlation between A and B in the rule A=>B. It shows how one item-set A affects the item-set B.
- **Lift(A=>B)**: `Support(A,B)/(Supp(A)Supp(B))`

### Density
Density measures how sparse the transaction-item matrix is. A high density indicates that it is common for more items to appear together in a basket, whereas a low density suggests that few items are purchased together.

## Implementation in R
Utilized Levenshire Similarity and Fuzzy Wizzy logic to draw the correlation between the products and reorders.
The most common package for market basket analysis in R is `arules`. The `arules::apriori()` function is the workhorse of this package.

### Example Code
```R
library(arules)

# Loading data
data(Groceries, package = "arules")

# Executing Apriori Algorithm
apriori_Groceries <- apriori(data = Groceries, parameter = list(support = 0.05, confidence = 0.1, minlen = 2))

# Viewing results
inspect(sort(apriori_Groceries, by = "confidence"))

# Plotting
itemFrequencyPlot(Groceries, topN = 10)
