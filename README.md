# Detecting Fake Job Postings Using Natural Language Processing and Machine Learning

This project develops an NLP-based Machine Learning solution to automatically detect fraudulent job advertisements, addressing the rise of online recruitment scams as part of **SDG 8: Decent Work and Economic Growth**.

## Table of Content
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [System Architecture](#system-architecture)
4. [Dataset Description](#dataset-description)
5. [Implementation Workflow](#implementation-workflow)
    * [Data Preprocessing](#data-preprocessing)
    * [Feature Extraction](#feature-extraction)
    * [Machine Learning Modeling](#machine-learning-modeling)
6. [Performance Evaluation](#performance-evaluation)
7. [Prototype Development](#prototype-development)
8. [Disclaimer](#disclaimer)

---

## Project Overview
Online job platforms are crucial for the modern labor market, but the rapid increase in fake postings has led to identity theft, fraud, and a loss of trust. This study proposes an automated detection system to protect job seekers and recruitment platforms.

---

## Objectives
* **Identify Linguistic Patterns:** Analyze common structural and linguistic features in fraudulent ads.
* **Prototype Development:** Design and develop a functional NLP application prototype.
* **Performance Testing:** Evaluate the system with end-users for real-world efficacy.

---

## System Architecture
The solution follows a modular NLP pipeline designed for scalability and high recall in fraud detection.


---

## Dataset Description
* **Dataset Source:** [Kaggle - Real or Fake: Fake Job Posting Prediction](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction?select=fake_job_postings.csv)
* **File Name:** `fake_job_postings.csv`
* **Size:** ~17,880 records with 17 attributes.

---

## Implementation Workflow

### Data Preprocessing
To handle noisy text, the following cleaning steps were applied:
* **Cleaning:** Removal of URLs, HTML tags, and special characters.
* **Normalization:** Lowercasing, punctuation removal, and digit stripping.
* **Tokenization & Stopword Removal:** Breaking text into individual units and removing non-informative words.

### Feature Extraction
Transformed raw text into numerical formats using:
* **TF-IDF Vectorization:** Capturing word importance across the corpus.
* **Word Embeddings:** (Optional) for deeper semantic understanding.

### Machine Learning Modeling
Several algorithms were benchmarked for accuracy and recall:
* **Linear Models:** Logistic Regression, SVM.
* **Ensemble Methods:** Random Forest.
* **Deep Learning:** RNN, LSTM.
* **Class Imbalance:** Applied **SMOTE** to ensure the model effectively identifies the minority (fraudulent) class.

---

## Performance Evaluation
The models were evaluated using metrics critical for fraud detection, where **SVM (After SMOTE)** provided the best balance:

| Model | Accuracy | Recall (Class 1) | Precision (Class 1) |
| :--- | :--- | :--- | :--- |
| **SVM (After SMOTE)** | **98.4%** | **78%** | **88%** |
| Logistic Regression | 97.6% | 83% | 73% |
| Naive Bayes | 93.7% | 88% | 44% |

---

## Prototype Development
The final system is deployed as an interactive detector using **Gradio** and **Streamlit**.
* **Features:** Users can paste any job description into the interface to receive a real-time "Real" or "Fake" prediction.

---

## Disclaimer
This project was developed for **educational purposes**. The authors are **not liable** for any decisions made based on the model's predictions.

---
 *Feel free to explore my other repositories for AWS and GCP implementations!*

