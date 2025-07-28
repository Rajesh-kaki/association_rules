# Association Rule Mining on Online Retail Data
This project applies association rule mining techniques to an online retail dataset to uncover meaningful itemset combinations and generate market basket insights using the Apriori algorithm.

🧠 What is Association Rule Mining?
Association rule mining is a key technique in unsupervised learning used to discover interesting relationships (associations) between variables in large datasets.

🔸 Common Use Case: Market Basket Analysis
"If a customer buys bread and butter, they are likely to buy jam."

🔸 Key Terms:
Support: How frequently an itemset appears in the dataset.

Confidence: The likelihood of seeing item B in transactions containing item A.

Lift: Ratio of observed support to that expected if A and B were independent.

📁 Dataset Overview
File Used: Online retail.xlsx

Content: Customer purchase history from an online retailer.

Feature Used: Only one column items (after renaming), listing purchased products.

⚙️ Implementation Steps
1. Data Loading
Loaded transaction data using pandas from an Excel file.

Displayed and renamed relevant columns for consistency.

2. Preprocessing
Each transaction was transformed into a format suitable for applying the Apriori algorithm (typically a list of itemsets per row).

3. Transaction Encoding
Used one-hot encoding to convert product names into binary format — each row becomes a transaction vector indicating presence/absence of items.

4. Applying Apriori Algorithm
Applied the apriori function from mlxtend.frequent_patterns to identify frequent itemsets.

Used minimum support threshold to filter results.

5. Generating Association Rules
Generated rules from the frequent itemsets using:

Confidence Threshold

Lift > 1 to ensure meaningful relationships

Sorted rules based on support or confidence for interpretation.

📊 Insights
Identified combinations of items frequently purchased together.

High-lift rules indicated strong product affinities useful for cross-selling.

Rule filtering enabled business-friendly interpretation.

🛠️ Libraries Used
pandas – for data manipulation

mlxtend.frequent_patterns – for apriori and association_rules functions

📂 Files
association_rules.ipynb — Main notebook for rule mining

Online retail.xlsx — Dataset used for market basket analysis

📌 Key Takeaways
Association rule mining is powerful for understanding customer buying behavior.

Apriori algorithm efficiently filters frequent itemsets based on support thresholds.

Insights derived can inform product bundling and personalized marketing strategies.
