# Market Basket Analysis

## Author
Anuradha Sahithi Padavala

## Project Overview
This project focuses on conducting a market basket analysis using an online retail dataset from the UCI Machine Learning Repository. The primary goal is to uncover relationships between different products purchased together, enhancing the recommendation systems.

## Dataset
The analysis utilizes the "Online Retail.xlsx" dataset, which includes detailed transaction data from an online retailer.
Dataset size ~600000

## Features of the Project

### Exploratory Data Analysis
- **Data Cleaning**: Null values are removed to prepare the dataset for analysis.
- **Data Distribution Analysis**: The distribution of transactions is analyzed by country and top-selling items.
- **Word Cloud Generation**: A word cloud is generated for product descriptions to visualize the most frequent terms.

### Data Pre-Processing
- **NLP Utilization**: Natural Language Processing (NLP) is used to extract nouns and proper nouns from item descriptions using spaCy, categorizing items based on common words.
- **Levenshtein Distance**: This method is applied to calculate similarities between item descriptions to group similar items together.

### Recommendation System
- **Category Mapping**: Items are assigned to categories based on their description similarities.
- **Recommendation Methods**:
  - `get_recommendation()`: Takes an invoice number and returns a recommended item.
  - `get_basket_rec()`: Accepts a basket of items and recommends a new item based on the basket's contents.

## Key Functions
- **Extract Nouns**: Extracts nouns from text for categorization.
- **Create Category Name**: Generates category names based on common words in descriptions.
- **Item and Category Mapping**: Maps each item to its respective category for easier retrieval and recommendation.

## Results
- **Recommendation Examples**: The system successfully recommends items like "GUMBALL MONOCHROME COAT RACK" based on previous purchases, demonstrating effective use of market basket analysis techniques.

## Conclusion
This project illustrates the effective application of NLP and similarity metrics in building a recommendation system based on market basket analysis. The approach enhances the shopping experience by providing tailored recommendations.

## Contact
For further inquiries or collaboration, please contact Anuradha Sahithi Padavala.
