# AI-Assisted Customer Insights Pipeline

## Overview
This project builds an AI-assisted analytics pipeline to extract structured business insights from unstructured customer review data. Using Amazon reviews, the analysis identifies key drivers of customer satisfaction, recurring complaint patterns, and actionable product and operational recommendations.

## Business Problem
Companies receive large volumes of customer feedback, but reviews are typically unstructured and difficult to analyze at scale. This project demonstrates how text analytics and clustering can transform raw review data into clear insights that decisions can be made on.

## Dataset
- Source: Amazon Reviews dataset (500,000+ reviews)
- Modeling sample: 20,000 reviews (balanced positive and negative)
- Data includes review text, ratings, and product metadata

> Note: Full dataset not included due to size. Public dataset available on Kaggle.

## Methodology

### 1. Data Preparation
- Cleaned review text (removed HTML, links, special characters)
- Filtered valid reviews and created sentiment groups

### 2. Feature Engineering
- Applied TF-IDF vectorization to convert text into numerical features
- Used unigrams and bigrams to capture context

### 3. Clustering (Core ML Step)
- Applied KMeans clustering to identify recurring review themes
- Tuned number of clusters to balance interpretability and coverage

### 4. AI-Assisted Theme Labeling
- Extracted top terms and sample reviews per cluster
- Used AI (LLM-assisted analysis) to assign business-friendly theme names

### 5. Analysis
- Compared theme frequency across all reviews
- Analyzed positive vs. negative sentiment by theme
- Identified themes with highest negative sentiment (business risk areas)

## Key Insights

- **Product experience drives satisfaction**  
  Taste, texture, and consistency are the strongest drivers of positive reviews.

- **Logistics create disproportionate risk**  
  Shipping delays, damage, and incorrect orders generate negative sentiment even when products are acceptable.

- **Category-specific drivers matter**  
  Pet products depend on animal acceptance; dietary products depend on ingredient trust.

- **Expectation mismatch drives complaints**  
  Negative reviews often result from differences between product listings and actual experience.

## Visualizations

### Theme Distribution
![Theme Distribution](main/figures/top_review_themes.png)

### Sentiment by Theme
![Sentiment by Theme](main/figures/pos_neg_reviews_by_theme.png)

### Highest Negative Sentiment Themes
![Negative Sentiment](main/figures/most_negative.png)

## Business Recommendations

- Optimize product flavor and consistency through testing
- Improve packaging durability and shipping reliability
- Align product descriptions with actual customer experience
- Increase transparency in ingredients and product claims
- Focus on high-risk themes with high negative sentiment

## Technical Stack
- Python
- pandas
- scikit-learn (TF-IDF, KMeans)
- matplotlib
- NLP preprocessing
- AI-assisted analysis (LLM-based theme labeling)

## Project Structure
