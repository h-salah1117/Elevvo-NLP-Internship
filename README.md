# Elevvo NLP Internship

Four NLP tasks I completed during the **[Elevvo](https://elevvo.tech) NLP internship** (2026), covering text classification, sequence labeling and model comparison with classical ML, neural networks and spaCy.

## Results at a glance

| Task | Dataset | Approach | Result (test set unless noted) |
|:--|:--|:--|:--|
| [Sentiment analysis](Amazon%20Sentiment%20Analysis/) | Amazon reviews (cell phones & accessories) | TF-IDF + Logistic Regression, vs balanced LR and Naive Bayes | ~92% accuracy (Logistic Regression, best) |
| [Fake news detection](Fake%20News%20Detection/) | Fake/True news, ~45K articles | Lemmatization + TF-IDF (10K features) + Logistic Regression | 0.95 accuracy, 0.95 F1 on 8,988 test articles |
| [News topic classification](News%20Aggregator/) | AG News, 120K train / 7.6K test | TF-IDF + Keras MLP (512 → 256 → 4) | ~90% validation accuracy (~99% train: overfits, see notes) |
| [Named entity recognition](Named%20Entity%20Recognition/) | CoNLL-2003 | spaCy pretrained pipelines + rule-based matching; `sm` vs `md` comparison | Qualitative comparison, displaCy visualization |

## What I'd do differently

- **News classification overfits** (99% train vs 90% validation after 5 epochs). Next steps: dropout, early stopping, and a fine-tuned transformer baseline (e.g. DistilBERT).
- **NER** has no span-level scores yet. Next step: evaluate both spaCy models with entity-level precision, recall and F1 on the CoNLL-2003 test split.

## Tech stack

Python · pandas · NLTK · scikit-learn · TensorFlow/Keras · spaCy · Matplotlib/Seaborn

## Run any task

```bash
git clone https://github.com/h-salah1117/Elevvo-NLP-Internship.git
cd Elevvo-NLP-Internship
pip install pandas nltk scikit-learn tensorflow spacy matplotlib seaborn
python -m spacy download en_core_web_sm   # NER task only
jupyter notebook
```

The datasets aren't committed (they're too large). Each task's README links to its Kaggle source.
