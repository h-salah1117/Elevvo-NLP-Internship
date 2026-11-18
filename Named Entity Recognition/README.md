# Elevvo NLP Internship - Task 4: Named Entity Recognition (NER)

## 📌 Project Overview
This project focuses on **Named Entity Recognition (NER)** using news articles. The goal is to automatically identify and categorize key entities such as **People (PER)**, **Locations (LOC)**, and **Organizations (ORG)** from unstructured text.

## 📊 Dataset
* **Source:** CoNLL-2003 Dataset (Kaggle).
* **Format:** Tokenized text with BIO (Beginning, Inside, Outside) tagging.
* **Tags:** Includes PER, LOC, ORG, and MISC entities.

## 🛠️ Implementation Details
* **Library:** [SpaCy](https://spacy.io/) was used for its robust pre-trained models and efficiency.
* **Approach:**
    * **Model-based NER:** Leveraged spaCy's pre-trained pipelines to detect entities.
    * **Rule-based Matching:** Implemented custom patterns to refine entity detection.

## ✨ Bonus Features
* **Visualization:** Used `displacy` to create an interactive visual map of entities within the text.
* **Model Comparison:** Evaluated and compared results between two different spaCy models:
    1. `en_core_web_sm` (Small/Fast).
    2. `en_core_web_md` (Medium/Accurate).

## 🚀 How to Run
1. Install requirements: `pip install spacy pandas`
2. Download models: `python -m spacy download en_core_web_sm`
3. Open `NER.ipynb` and run the cells.

---
**Course:** Natural Language Processing Track | **Provider:** [Elevvo.tech](https://elevvo.tech)  
**Deadline:** March 10, 2026
