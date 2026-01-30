# Zomato-Project

# Business Context
Online food delivery platforms like Zomato generate massive volumes of restaurant data and customer reviews every day.
While this data is rich in insights, raw ratings and reviews alone do not explain customer behavior, restaurant performance, or competitive positioning.
The challenge was to transform this fragmented data into actionable intelligence that could help:
Restaurants improve pricing and engagement
Platforms optimize recommendations
Stakeholders understand customer sentiment at scale

# ❓ Problem Statement
The project aimed to answer the following key business questions:
How are restaurants distributed based on cost, cuisine, ratings, and engagement?
Can restaurants be grouped into meaningful segments based on similar characteristics?
What is the overall customer sentiment toward restaurants?
Which machine learning model performs best for sentiment classification?
How can these insights drive better decision-making for food platforms and restaurants?

# 📊 Data Overview
Two datasets were used:
1️⃣ Restaurant Metadata Dataset
Restaurant name & location
Cuisines
Cost for two
Ratings
Number of reviews & followers
2️⃣ Customer Reviews Dataset
Review text
Customer ratings
This allowed the analysis to combine structured numerical data with unstructured textual data.

# 🔧 Methodology & Approach
1. Data Preparation
Handled missing and inconsistent values
Converted cost fields into numeric format
Cleaned review text (lowercasing, punctuation removal)
Applied lemmatization for NLP preprocessing
Scaled numerical features where required
✔️ Result: A clean, modeling-ready dataset

# 2. Exploratory Data Analysis (EDA)
EDA was used to uncover patterns and validate assumptions.
Key Insights:
Most restaurants fall into the mid-price range
North Indian and Chinese cuisines dominate the platform
Customer engagement is highly skewed
A small percentage of restaurants receive the majority of reviews
Higher price does not necessarily mean higher ratings
Multiple visualizations (distributions, bar plots, heatmaps, pair plots) supported these findings.

# 3. Restaurant Clustering (Unsupervised Learning)
To segment restaurants into meaningful groups:
Applied Principal Component Analysis (PCA) for dimensionality reduction
Used Hierarchical Clustering (Ward linkage)
Evaluated cluster quality using Silhouette Score

# 📌 Outcome:
6 optimal restaurant clusters were identified, representing distinct segments based on:
Pricing
Customer engagement
Rating behavior
These clusters help explain competitive positioning across restaurants.

# 4. Sentiment Analysis (Supervised Learning)
Customer reviews were classified into Positive and Negative sentiment.
Models Tested:
Logistic Regression
Decision Tree
Random Forest
XGBoost
K-Nearest Neighbors
Evaluation Metrics:
Accuracy
Precision
Recall
F1-Score
ROC–AUC

# 🏆 Best Model: 
Logistic Regression
Highest ROC–AUC score
Balanced precision and recall
Strong generalization
Simple and interpretable for business use
ROC curve analysis further validated model performance.

# 📈 Key Results
Successfully segmented restaurants into 6 meaningful clusters
Identified strong imbalance in customer engagement
Logistic Regression outperformed complex models for sentiment prediction
Customer sentiment aligned strongly with engagement and ratings

# 💡 Business Impact & Recommendations
For Restaurants
Adjust pricing and menu strategy based on cluster behavior
Improve visibility through customer engagement and reviews
Leverage sentiment feedback to enhance service quality
For Food Platforms
Use clustering to improve restaurant recommendations
Incorporate sentiment signals into ranking algorithms
Target promotions using popular cuisines and peak engagement patterns

# 🧠 Key Learnings
Unsupervised learning is powerful for market segmentation
Simpler models can outperform complex ones when data is well-prepared
Combining EDA + clustering + NLP delivers deeper business insights
Interpretability matters when deploying ML in real-world platforms

# 🛠️ Tech Stack
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
NLP (TF-IDF, text preprocessing)
PCA & Hierarchical Clustering
