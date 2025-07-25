# 🛍️ Product Review Sentiment Analyzer

This project leverages **Natural Language Processing (NLP)** techniques to extract actionable insights from unstructured customer reviews. The insights generated can support **SDG 8: Decent Work and Economic Growth** by helping businesses improve product quality, address customer needs, and stay competitive.

---

## 🧑‍💻 Group Members

| Name                     | Student ID   |
|--------------------------|--------------|
| Teo Kai Ning             | 22091346     |
| Chua Sze Yan             | 23094470     |
| Tan Jian Lin             | 17207012     |
| Chong Zhan Hang          | 24077643     |
| James Tang Tzeun Zhu     | 24063011     |
| Areej Abdurahman Mohammad| 23119264     |

---

## 📌 Project Summary

We developed a **sentiment classification system** that categorizes customer reviews into **positive**, **neutral**, or **negative** sentiments. The system also extracts **key themes** using topic modeling to better understand customer concerns and feedback.

---

## 🗃️ Dataset

We used **Amazon product reviews**, which include detailed customer feedback. These reviews are processed to support classification and topic detection tasks.

---

## 🔧 Preprocessing Steps

- **Text Normalization**: Lowercasing, HTML removal, punctuation and whitespace removal
- **Tokenization**
- **Stopword Handling**: Retained for DistilBERT due to contextual embeddings
- **Lemmatization**: Preserves grammar and meaning
- **Label Encoding**: Transforms sentiments into classes: `positive`, `neutral`, `negative`

---

## 🧠 Techniques Used

### Sentiment Classification

- **Model**: [DistilBERT](https://huggingface.co/distilbert-base-uncased)
- **Loss Function**: `Focal Loss` (best performing)
- **Key Metrics**:
  - **F1 Score**: 0.72
  - **Validation Loss**: 0.0235
  - **Precision & Recall**: Highest among all models
  - **Advantage**: Handles class imbalance by focusing on hard-to-classify samples

### Topic Modeling

- **Model**: [BERTopic](https://maartengr.github.io/BERTopic/)
- **Fine-tuned Results**:
  - **Coherence Score**: ↑ from 0.42 → 0.48
  - **Diversity**: ↑ from 0.51 → 0.70
  - **True Topics**: ↓ from 55 → 52 (better interpretability)

---

## 🖥️ Architecture Overview

- **Frontend**: Gradio-based UI for user feedback
- **Backend**: Python logic for sentiment classification and topic modeling
- **Storage**: Results saved as `.csv` for trend analysis
- **Email Notification**: Optionally send results to users

---

## 🚀 Features

- Text input + star rating + category checkboxes
- Instant sentiment detection + email response (optional)
- Downloads CSV summary of user feedback
- Topic and sentiment trends stored for analytics

---

## 📈 Results

| Model           | F1 Score | Validation Loss |
|----------------|----------|-----------------|
| DistilBERT + Focal Loss | **0.72**   | **0.0235**         |
| Trainer Loss   | -        | 0.48            |
| Weighted Loss  | -        | 0.57            |

Topic modeling results improved after fine-tuning, making the topics more coherent and diverse.

---
