# 📰 Fake News Detection (LIAR Dataset)

This project builds a classification pipeline to detect fake news using the **LIAR dataset**, which contains over 12,000 labeled short political statements. The goal is to classify a given statement as **True**, **False**, or something in between using NLP and machine learning.

---

## 🧠 Features

- Text preprocessing (lowercasing, punctuation removal, stopword filtering)
- TF-IDF vectorization
- Logistic Regression, Random Forest, and Feedforward Neural Network classifiers
- Evaluation with confusion matrix, precision, recall, and F1-score

---

## 🔍 Dataset Overview

- Source: [LIAR Dataset (Wang, 2017)](https://www.cs.ucsb.edu/~william/data/liar_dataset.zip)
- 6-way label classification:
  - `true`, `mostly-true`, `half-true`, `barely-true`, `false`, `pants-fire`
- Statements from PolitiFact covering 2007–2016

---

## 📊 Model Performance (2-class Example)

| Class     | Precision | Recall | F1 Score |
|-----------|-----------|--------|----------|
| Fake      | 0.60      | 0.64   | 0.62     |
| Real      | 0.58      | 0.55   | 0.56     |

> Full 6-class classification and advanced NLP improvements are in progress.

---

## 🚧 Project Status

✅ Core binary classifier working  
🔄 Working on improving multiclass performance and adding Word2Vec/transformers

---

## 📁 File Structure

```bash
├── nlppractice.ipynb          # Jupyter notebook for classification pipeline
├── liar_dataset/              # Dataset folder (excluded here)
├── README.md                  # This file
