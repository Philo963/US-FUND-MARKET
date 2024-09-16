1. Select Data File > 200 MB 
• File: Download the large dataset, containing both U.S. Mutual Funds and ETFs, 
from Yahoo Finance. Since the file contains 23,783 Mutual Funds and 2,310 
ETFs, it is expected to be quite large (especially with historical data and financial 
ratios). 
• Source: You can scrape the latest data from Yahoo Finance or use available 
versions from platforms like Kaggle or other financial repositories. 
2. EDA (Exploratory Data Analysis), Visualization, and Description 
• Objective: Understand the dataset’s structure and key trends. 
o Steps: 
▪ Load the data and inspect its columns (fund family, inception date, 
net assets, portfolio composition, etc.). 
▪ Generate summary statistics (e.g., mean, median, min, max for 
financial indicators like total_net_assets, price/earning, 
Sharpe ratio). 
▪ Visualize important aspects such as: 
▪ The distribution of Mutual Funds vs ETFs. 
▪ Historical performance (returns over different periods). 
▪ Portfolio allocation (cash, stocks, bonds, sectors). 
▪ ESG scores distribution. 
▪ Identify correlations between variables, e.g., total assets vs. Sharpe 
ratio, or returns vs. risk ratios. 
Visualization Suggestions: 
• Histograms for fund family sizes, net assets. 
• Time series line charts for fund returns over time. 
• Boxplots for comparing financial ratios (alpha, beta) between ETFs and Mutual 
Funds. 
3. Transformation (Cleaning) 
• Objective: Prepare the dataset for analysis by handling inconsistencies. 
o Steps: 
▪ Remove or fill missing values in key financial metrics. 
▪ Standardize date formats (e.g., inception dates). 
▪ Convert financial indicators into correct data types (e.g., numerical 
for price/earning, categorical for fund family). 
▪ Normalize financial ratios (Sharpe, alpha, beta) to ensure they are 
on a similar scale for model training. 
▪ Handle duplicates or irrelevant columns. 
4. Apply Different Machine Learning Models 
• Objective: Perform predictive modeling on the dataset. 
Machine Learning Models: 
• Traditional ML: 
o Linear/Logistic Regression: Predict future fund returns based on 
financial indicators. 
o Random Forest/Gradient Boosting: Use for classification of top
performing funds based on net assets, ratios, ESG scores, etc. 
o K-Means Clustering: Cluster funds based on portfolio composition 
(stocks, bonds, cash, sectors). 
• Deep Learning: 
o LSTM/RNN for predicting future fund prices using historical time series 
data. 
o ANN (Artificial Neural Network) for predicting fund performance based 
on historical returns and financial ratios. 
Steps: 
• Split the data into training, validation, and test sets. 
• Train and compare models using metrics such as accuracy, R², MSE, or Sharpe 
ratio for regression models. 
• Hyperparameter tuning and model optimization. 
5. Pipeline (SSIS, Talend, Cloud, Informatica, Databricks) 
• Objective: Build a pipeline to automate data ingestion, transformation, modeling, 
and storage. 
o Tool: Use Azure Databricks (or any other cloud-based service) to 
implement the pipeline. 
o Steps: 
▪ Ingest data from the CSV file using Databricks or Talend. 
▪ Apply the transformation logic and clean the data. 
▪ Use MLflow within Databricks to automate model training and 
validation. 
▪ Trigger periodic updates to the model as new data is ingested. 
▪ Store the cleaned data and model outputs in a data warehouse. 
6. Store in Data Warehouse 
• Objective: Store processed data in a scalable warehouse. 
o Tool: Use Google BigQuery, AWS Redshift, or Azure Synapse. 
o Steps: 
▪ Upload the cleaned dataset into the warehouse. 
▪ Ensure partitioning and indexing for optimal query performance. 
▪ Set up scheduled data loads for continuous updates (e.g., every 
semester). 
7. Applied SQL Queries (15 Queries) 
• Objective: Perform SQL queries on the stored data to derive insights. 
Sample Queries: 
1. Retrieve the top 10 funds with the highest net assets. 
2. Find the average yearly return for ETFs over the past 5 years. 
3. List the top 5 funds with the best Sharpe ratios. 
4. Calculate the total number of Mutual Funds in each fund family. 
5. Retrieve the top 10 funds with the highest ESG scores. 
6. Find the correlation between alpha and beta for all funds. 
7. List all ETFs with a negative Treynor ratio in the last quarter. 
8. Compare the 1-year and 3-year return performance for a particular fund. 
9. Rank funds by their historical price-to-earnings ratio. 
10. Find funds that have outperformed the market by a given percentage. 
11. Calculate the percentage of total assets in different portfolio allocations (stocks, 
bonds). 
12. Retrieve the inception date and net assets of the oldest funds. 
13. Find funds with the highest growth in total net assets over the last 5 years. 
14. Query to find funds whose cash allocation exceeds 50%. 
15. Compare ETFs and Mutual Funds by their risk ratios (Sharpe, beta, alpha).
