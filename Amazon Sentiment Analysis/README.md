# Elevvo NLP Internship - Task 1: Sentiment Analysis on Product Reviews

## 📌 Project Overview

This project is part of the **Elevvo NLP Internship Program**. The objective is to build a binary classifier that analyzes product reviews from Amazon (Cell Phones and Accessories) to determine if the sentiment is **Positive** or **Negative**.

## 🛠️ Tech Stack & Tools

* **Language:** Python
* **Libraries:** Pandas, NLTK, Scikit-learn, Matplotlib, Seaborn
* **Environment:** VS Code / Jupyter Notebook
* **Data:** https://www.kaggle.com/datasets/abdallahwagih/amazon-reviews/data

## 🚀 Workflow & Implementation

### 1. Data Processing

* **Format Conversion:** Handled the initial dataset in JSON format and converted it to CSV for efficient manipulation.
* **Data Cleaning:** Removed null values from essential columns like `reviewText` and `overall`.

### 2. Text Preprocessing

* **Normalization:** Converted all text to lowercase.
* **Noise Removal:** Removed special characters and numbers using Regular Expressions (Regex).
* **Stopwords Removal:** Used the NLTK library to filter out common English words that don't carry sentiment.

### 3. Feature Engineering & Modeling

* **Vectorization:** Applied `TfidfVectorizer` to convert cleaned text into numerical features.
* **Classification:** Trained multiple models to compare performance:
    * **Logistic Regression** (Achieved ~92% accuracy).
    * **Balanced Logistic Regression**.
    * **Naive Bayes**.

### 4. Visualization (Bonus Task)

* Visualized the **Top 20 Positive and Negative Words** based on the model's coefficients to understand which features drive the sentiment prediction.

## 📊 Results Summary

The Logistic Regression model outperformed others in accuracy, effectively distinguishing between positive terms like "great" and "love" versus negative terms like "poor" and "worst".

---

**Contact:** [Hazem Mohammad Salah]  

**Internship Provider:** [Elevvo.tech]
