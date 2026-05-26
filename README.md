# 🧠 Yelp Review Sentiment Analysis & Convenience Store Rating Prediction

## Predicting Convenience Store Popularity in Sacramento County Using NLP & Machine Learning

---

# 📌 Project Overview

This project analyzes Yelp customer review data to predict convenience store popularity and customer satisfaction across Sacramento County, California.

Using a combination of:

- Natural Language Processing (NLP)
- Sentiment Analysis
- TF-IDF Feature Engineering
- Machine Learning Regression Models
- Yelp Review Scraping

this project transforms raw customer reviews into predictive business insights.

The primary objective was to identify which convenience stores are most favored by customers based on Yelp review text and rating behavior.

---

# 🎯 Business Problem

Yelp relies heavily on customer reviews to recommend businesses to users.

However, convenience stores often receive mixed reputations due to:

- poor management
- cleanliness concerns
- pricing complaints
- inconsistent customer experiences

This project helps solve the following business problem:

> How do convenience store popularity ratings in Sacramento County rank based on Yelp customer review data?

The goal was to improve recommendation quality by using customer-generated review text to identify:

- highly rated stores
- poorly rated stores
- customer sentiment patterns
- predictive rating behavior

---

# 🛠️ Technologies Used

## Programming & Analytics

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib

## NLP & Text Mining

- NLTK
- TF-IDF
- TextBlob
- Tokenization
- Stemming
- Stopword Removal

## Machine Learning

- Scikit-Learn
- Lasso Regression
- Ridge Regression
- Elastic Net Regression
- Cross Validation

## Data Collection

- Yelp GraphQL Endpoint
- JSON Parsing
- Web Scraping Automation

---

# 📂 Dataset Information

## Data Source

Yelp Convenience Store Reviews

## Geographic Coverage

The project collected review data from seven Sacramento County regions:

- Elk Grove
- Arden
- Natomas
- Carmichael
- Del Paso Heights
- Rancho Cordova
- Folsom

---

# 📊 Dataset Summary

| Metric | Value |
|---|---|
| Total Reviews | 2,661 |
| Total Stores | 42 |
| Regions Covered | 7 |
| Review Source | Yelp |
| Dataset Type | Text + Ratings |

---

# 📖 Data Dictionary

| Column | Description |
|---|---|
| biz_id | Business ID |
| biz_name | Business name |
| author_name | Review author |
| author_location | Reviewer location |
| rating | Yelp rating (1–5) |
| date | Review date |
| text | Customer review |
| useful | Useful votes |
| funny | Funny votes |
| cool | Cool votes |
| helpful | Helpful reactions |

---

# 🧹 Data Cleaning & Validation

The dataset underwent preprocessing and validation before modeling.

## Cleaning Steps

- Checked for missing values
- Removed duplicate observations
- Validated text formatting
- Verified review consistency
- Combined regional datasets
- Standardized text processing

## Results

✅ No missing values  
✅ No duplicate rows  
✅ Clean review dataset ready for NLP modeling

---

# 🔍 Exploratory Data Analysis

## Sentiment Classification

Customer reviews were classified into:

- Positive
- Negative
- Neutral

using TextBlob sentiment polarity.

---

# 😊 Overall Sentiment Results

| Sentiment | Count |
|---|---|
| Positive | 1,857 |
| Negative | 744 |
| Neutral | 60 |

---

# 📈 Most Positively Reviewed Stores

The stores with the highest number of positive reviews included:

- Nugget Markets
- Walgreens
- CVS Pharmacy
- Walmart Supercenter
- 7-Eleven

---

# 📉 Most Negatively Reviewed Stores

The stores with the highest number of negative reviews included:

- Walgreens
- CVS Pharmacy
- Walmart Supercenter
- 7-Eleven
- Safeway

---

# 🧠 NLP Pipeline

Customer review text was transformed into machine-learning-ready numerical features using:

## TF-IDF (Term Frequency–Inverse Document Frequency)

The NLP pipeline included:

- Tokenization
- Stopword removal
- English stemming
- TF-IDF vectorization

This converted raw review text into a numerical sparse matrix for predictive modeling.

---

# 🤖 Machine Learning Models

Three regression models were implemented and compared:

| Model | Purpose |
|---|---|
| Lasso Regression | Feature selection + prediction |
| Ridge Regression | Regularization + prediction |
| Elastic Net | Combined L1/L2 regularization |

---

# 📊 Model Evaluation Metrics

Models were evaluated using:

- RMSE
- R²
- Cross-validation
- Gains Charts
- Lift Charts

---

# 🥇 Best Performing Model — Lasso Regression

The Lasso Regression model performed best on validation data.

## Validation Performance

| Metric | Value |
|---|---|
| RMSE | 1.3703 |
| Validation R² | 0.40 |
| Non-Zero Features Selected | 397 |

The model demonstrated the best balance between:

- predictive accuracy
- generalization performance
- feature reduction

---

# 📈 Ridge Regression Results

| Metric | Value |
|---|---|
| RMSE | 1.5292 |
| Validation R² | 0.25 |

While Ridge performed strongly on training data, it generalized less effectively on validation data.

---

# 📉 Elastic Net Results

| Metric | Value |
|---|---|
| RMSE | 1.4667 |
| Validation R² | 0.31 |

Elastic Net performed better than Ridge but slightly weaker than Lasso.

---

# 🏪 Predicted Store Rankings

Using Lasso predictions, median predicted ratings were calculated for each convenience store.

---

# ⭐ Top 5 Predicted Stores

| Store | Predicted Rating |
|---|---|
| Royal C Store | 3.72 |
| Super Quick Food Store | 3.69 |
| Capital Grocery | 3.63 |
| P & A Food & Liquor | 3.58 |
| G & G Food & Liquor | 3.56 |

---

# ⚠️ Bottom 5 Predicted Stores

| Store | Predicted Rating |
|---|---|
| Quik Stop | 0.97 |
| Superstar Market & Liquor | 1.45 |
| Coloma Grocery | 1.76 |
| K Mini-Mart | 1.92 |
| Wilton Store | 1.99 |

---

# 📌 Key Findings

## 📍 Sentiment Alone Was Not Enough

Sentiment analysis produced skewed results because large chain stores appeared more frequently due to multiple locations.

This motivated the use of predictive modeling for more balanced rankings.

---

## 📍 Lasso Regression Performed Best

Lasso generalized better on unseen validation data compared to Ridge and Elastic Net.

---

## 📍 Customer Review Text Contains Strong Predictive Signals

Review text successfully predicted store favorability and popularity ratings.

---

## 📍 Smaller Stores Can Outperform Large Chains

Several smaller local convenience stores ranked higher than nationally recognized chains.

---

# 💼 Business Recommendations

## 1️⃣ Improve Low-Rated Stores

Yelp should partner with poorly rated businesses to address:

- cleanliness
- staffing
- pricing
- customer service

---

## 2️⃣ Focus on High-Impact Customer Drivers

Customer satisfaction is heavily influenced by:

- service quality
- speed
- store condition

---

## 3️⃣ Real-Time Sentiment Monitoring

Yelp should continuously monitor reviews to identify emerging issues before reputational damage grows.

---

## 4️⃣ Predictive Recommendation Targeting

Use predictive analytics to improve recommendation ranking quality.

---

## 5️⃣ Replicate Best Practices

Analyze operational patterns from highly rated stores and apply them to underperforming businesses.

---

# ⚠️ Limitations

Several limitations were identified:

- Geographic focus limited to Sacramento County
- Review bias from customer experiences
- Uneven store review counts
- Potential bot-generated reviews
- Sentiment skew from large chain stores

---

# 🚀 Future Enhancements

Potential future improvements include:

- Deep learning NLP models
- BERT-based sentiment analysis
- Real-time review pipelines
- Geographic expansion
- Topic modeling
- Recommendation systems

---

# 📷 Example Analysis Outputs

## Sentiment Analysis
- Positive Sentiment Charts
- Negative Sentiment Charts
- Neutral Sentiment Charts

## Machine Learning Evaluation
- Gains Charts
- Lift Charts
- Model Comparison Metrics

---

# 📁 Repository Structure

```text
yelp-review-sentiment-analysis/
│
├── README.md
├── Yelp_Sentiment_Analysis.ipynb
├── Combined_Region_File.csv
├── requirements.txt
├── images/
└── charts/
```

---

# 🎓 Academic Context

California State University, Sacramento  
MSBA 212 — Advanced Business Analytics

Prepared By:
### Kumari Nicky

---

# 📌 Conclusion

This project demonstrates how customer-generated Yelp review data can be transformed into meaningful business intelligence using NLP and machine learning.

By combining:

- sentiment analysis
- TF-IDF feature engineering
- regression modeling
- predictive analytics

the project successfully identified convenience store popularity patterns across Sacramento County.

The findings show that review text contains strong predictive signals that can help improve business recommendations and customer targeting strategies.

---

# ⭐ Final Takeaway

Customer reviews are more than opinions.

When analyzed correctly using NLP and machine learning, they become powerful predictive signals that help businesses improve customer experience, reputation, and strategic decision-making.

```
