# Sentiment Analysis from Tweets

This project applies machine learning models to classify tweets as **positive** or **negative**.  
It uses the `twitter_samples` dataset from the NLTK library and compares different ML models.

## Tools & Libraries
- Python, Pandas, Scikit-learn, NLTK, Matplotlib
- Models: Naive Bayes, Logistic Regression, SVM, Random Forest

## Methodology
1. Data cleaning: removed emojis, punctuation, stopwords, applied stemming.  
2. Feature extraction: TF-IDF Vectorizer.  
3. Model training and evaluation with accuracy, confusion matrix, and classification reports.  

## Results
- **Logistic Regression** performed best with **76% accuracy**.  
- Naive Bayes, SVM, and Random Forest were close (~75%).  

## Key Takeaway
Even with modest accuracy, the project shows how preprocessing and model selection impact NLP tasks.  
It was my first sentiment analysis project and sparked my interest in NLP and machine learning.
