# 📰 Fake News Detection with NLP  
### *Built with TF-IDF, XGBoost, and Fine-Tuned BERT*

> Classifying political statements as **Fake** or **Real** using the LIAR dataset and state-of-the-art NLP techniques.

---

## 🚀 Live Demo

🔗 **Try the App** → [Fake News Detector on Hugging Face Spaces](https://huggingface.co/spaces/ShahOfData/shah_fake-news-detector)  
💻 **View Portfolio** → [shahnekouei.com/projects](https://shahnekouei.com/projects)

---

## 🧠 Project Highlights

- ✅ Binary classification: Fake vs. Real  
- ✅ Preprocessing: lowercasing, stopword removal, punctuation cleanup  
- ✅ Models compared:
  - TF-IDF + Logistic Regression
  - TF-IDF + XGBoost
  - **BERT (fine-tuned and deployed)**
- ✅ Evaluation: accuracy, precision, recall, F1-score, confusion matrix  
- ✅ Deployment using Gradio + Hugging Face Spaces

---

## 📊 Dataset Summary

| Item              | Description |
|-------------------|-------------|
| 📚 **Dataset**    | [LIAR Dataset (Wang, 2017)](https://www.cs.ucsb.edu/~william/data/liar_dataset.zip) |
| 🧾 **Size**       | ~12,800 labeled political statements |
| 🗂️ **Labels**     | `true`, `mostly-true`, `half-true`, `barely-true`, `false`, `pants-fire` |
| 🔁 **Remapping**  | Real (1): `true`, `mostly-true`, `half-true`<br>Fake (0): `false`, `barely-true`, `pants-fire` |

---

## 📈 Model Results

### ✅ Logistic Regression (TF-IDF)

**Test Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.59      | 0.39   | 0.47     |
| Real  | 0.62      | 0.79   | 0.70     |
> **Accuracy:** `0.61`

---

### ✅ XGBoost (TF-IDF)

**Test Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.53      | 0.61   | 0.57     |
| Real  | 0.66      | 0.57   | 0.61     |
> **Accuracy:** `0.5919`  
> **Confusion Matrix:** `[[340, 213], [304, 410]]`

---

### ✅ BERT (Fine-Tuned & Deployed)

**Test Set**
| Class | Precision | Recall | F1 Score |
|-------|-----------|--------|----------|
| Fake  | 0.58      | 0.58   | 0.58     |
| Real  | 0.67      | 0.67   | 0.67     |
> **Accuracy:** `0.63`  
> **Confusion Matrix:** `[[319, 234], [233, 481]]`

🖼️ *Confusion matrix visual available in the repo and demo.*

---

## 🧩 Project Structure

```bash
├── fakeNewsCode.ipynb             # Training and evaluation notebook
├── tfidf_vectorizer.pkl           # Saved TF-IDF vectorizer
├── xgboost_model.pkl              # Trained XGBoost model
├── hugging_face_fake_news/
│   └── model/                     # Fine-tuned BERT model files
├── app.py                         # Gradio app script
├── requirements.txt               # Dependencies for deployment
├── README.md                      # Project documentation
