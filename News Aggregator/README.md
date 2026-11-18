# Elevo NLP Internship Project – News Category Classification

## 📄 Project Description

This project classifies news articles into categories such as **World, Sports, Business, and Sci/Tech** using Natural Language Processing (NLP) techniques.  

The model uses **TF-IDF** vectorization and a **Neural Network** (Keras/TensorFlow) for multiclass classification.

---

## 🗂 Dataset

- **AG News dataset (Kaggle)**: 120,000 training samples, 7,600 test samples.
- Each sample has:
  - `Title` – article headline
  - `Description` – article text
  - `Class Index` – category (0=World, 1=Sports, 2=Business, 3=Sci/Tech)

> Note: Original dataset files are **not uploaded** to GitHub. They are listed in `.gitignore`.

---

## ⚙️ Preprocessing

- Lowercasing
- Removing stopwords
- Tokenization
- Lemmatization
- TF-IDF vectorization (max_features=10,000)

---

## 🧠 Model

- Neural Network with Keras:
  - Input layer: 10,000 features
  - Hidden layers: Dense(512, relu), Dense(256, relu)
  - Output layer: Dense(4, softmax)
- Loss: categorical_crossentropy
- Optimizer: Adam
- Epochs: 5
- Batch size: 128

---

## 📈 Results

- Training Accuracy: ~99%
- Validation Accuracy: ~90%
- Classification report on training data (validation accuracy ~90%; the model overfits):

```text
precision    recall    f1-score
0 (World)    0.99      0.98      0.99
1 (Sports)   1.00      1.00      1.00
2 (Business) 0.98      0.98      0.98
3 (Sci/Tech) 0.98      0.98      0.98
```
