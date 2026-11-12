<div align="center">

# 💬 Tweet Sentiment Classification

**Can classical machine learning tell a positive tweet from a negative one?**
NLP preprocessing → TF-IDF features → four models compared.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-154F5B)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)

`10,000 labelled tweets` · `4 models` · `best accuracy 76%`

</div>

> This repository is a **project showcase**. Source code and the full report are private.
> Contact: albinajeti20@gmail.com

## Overview

```mermaid
flowchart LR
    A[NLTK twitter_samples<br/>5k positive · 5k negative] --> B[Cleaning<br/>emojis · punctuation · stopwords]
    B --> C[Porter stemming]
    C --> D[TF-IDF features]
    D --> E[Naive Bayes · Logistic Regression<br/>SVM · Random Forest]
```

| Stage | What I did |
|---|---|
| **1. Data** | Used NLTK's `twitter_samples` corpus: 10,000 tweets labelled positive or negative. |
| **2. Cleaning** | Removed emojis, punctuation and stopwords, lowercased the text and stemmed it. I tried Porter and Lancaster stemming and WordNet lemmatization; Porter worked best. |
| **3. Features** | Converted the text to TF-IDF vectors, with an 80/20 train/test split. |
| **4. Models** | Tuned and compared four classifiers using accuracy, precision, recall, F1 and confusion matrices. |

## Results

<p align="center"><img src="assets/model_accuracy.svg" width="700" alt="Accuracy per model"></p>

- **Logistic Regression** performed best with **76% accuracy**.
- All four models are within one percentage point of each other. With TF-IDF features, the choice of model matters less than the text representation.
- Naive Bayes classified negative tweets slightly better than positive ones (788 vs 715 correct).

## Next steps
- Try word embeddings or transformer models (e.g. BERT) that understand context and sarcasm
- Handle negation ("not good") explicitly during preprocessing

<sub>© 2025 Albin Ajeti. All rights reserved. See [LICENSE](LICENSE).</sub>
