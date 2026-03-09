\# Task 3: Fake News Detection



\## 📄 Project Description

This project detects whether a news article is \*\*real\*\* or \*\*fake\*\* based on its text content.  

We use \*\*text preprocessing\*\*, \*\*TF-IDF vectorization\*\*, and a \*\*binary classifier\*\* (Logistic Regression or SVM) to perform the detection.



---



\## 🗂 Dataset

\- \*\*Fake.csv\*\* – 23,502 fake news articles

\- \*\*True.csv\*\* – 21,417 real news articles

\- Each dataset contains columns like:

&nbsp; - `title` – article headline

&nbsp; - `text` – article content

\- We combine the two datasets into a single DataFrame with a \*\*label column\*\*:

&nbsp; - `0` = Real

&nbsp; - `1` = Fake



> Note: The datasets themselves are \*\*not uploaded\*\* to GitHub. They are ignored in `.gitignore`.



---



\## ⚙️ Preprocessing

\- Lowercasing

\- Removing stopwords

\- Tokenization

\- Lemmatization

\- Combining `title` and `text` into a single column

\- TF-IDF vectorization (max\_features=10,000)



---



\## 🧠 Model

\- \*\*Binary classification\*\* using Logistic Regression:

&nbsp; - Solver: default (`lbfgs`)

&nbsp; - Max iterations: 1000

\- Input: TF-IDF features

\- Output: 0 (Real) / 1 (Fake)

\- Metrics: Accuracy, F1-score



---



\## 📈 Results

\- Example performance on test set:

```text

Accuracy: 0.95

&nbsp;             precision    recall  f1-score   support



&nbsp;          0       0.95      0.95      0.95      4283

&nbsp;          1       0.95      0.95      0.95      4705



&nbsp;   accuracy                           0.95      8988

&nbsp;  macro avg       0.95      0.95      0.95      8988

weighted avg       0.95      0.95      0.95      8988

