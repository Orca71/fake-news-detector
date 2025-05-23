# 📰 Fake News Detection (LIAR Dataset)

This project builds a natural language processing pipeline to classify political statements as **Fake** or **Real**, using the LIAR dataset. The goal is to distinguish between truthful and misleading claims using machine learning techniques, with a focus on explainability and performance.

---

## 🧠 Features

- Preprocessing: lowercasing, punctuation removal, stopword filtering
- Feature extraction: TF-IDF vectorization
- Models implemented:
  - ✅ Logistic Regression
  - ✅ XGBoost Classifier
  - ⏳ BERT (fine-tuning in progress)
- Evaluation: confusion matrix, precision, recall, F1-score

---

## 🔍 Dataset Overview

- **Source**: [LIAR Dataset (Wang, 2017)](https://www.cs.ucsb.edu/~william/data/liar_dataset.zip)
- **6 original labels**: `true`, `mostly-true`, `half-true`, `barely-true`, `false`, `pants-fire`
- **Binary remapping**:
  - Real (1): `true`, `mostly-true`, `half-true`
  - Fake (0): `false`, `barely-true`, `pants-fire`
- Contains 12,000+ short political statements from PolitiFact (2007–2016)

---

## 📊 Model Performance

### Logistic Regression (TF-IDF Features)

**Validation Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.65      | 0.44   | 0.52     |
| Real  | 0.60      | 0.78   | 0.68     |
> Accuracy: **0.62**

**Test Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.59      | 0.39   | 0.47     |
| Real  | 0.62      | 0.79   | 0.70     |
> Accuracy: **0.61**

---

### XGBoost (TF-IDF Features)

**Validation Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.57      | 0.65   | 0.60     |
| Real  | 0.62      | 0.54   | 0.58     |
> Accuracy: **0.5927**  
> Confusion Matrix: `[[398, 218], [305, 363]]`

**Test Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.53      | 0.61   | 0.57     |
| Real  | 0.66      | 0.57   | 0.61     |
> Accuracy: **0.5919**  
> Confusion Matrix: `[[340, 213], [304, 410]]`

---

## 🚧 BERT Status

The BERT model is being fine-tuned on the binary-labeled LIAR dataset. Initial results are pending — full metrics will be shared after full training on the complete dataset.

---

## 📁 Project Structure

```bash
├── fakeNewsCode.ipynb         # Training and inference notebook
├── cleaned_test.csv           # Preprocessed data
├── tfidf_vectorizer.pkl       # Saved TF-IDF vectorizer
├── xgboost_model.pkl          # Saved XGBoost model
├── README.md                  # Project documentation
