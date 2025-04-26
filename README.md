# 📘 Course Info

**Course**: PCMLAI (Section-D)  
**End Date**: March 2025  

---

**👤 Student**: *Gopikrishna Putti*

---

**🔗 Project Notebook**:  
[Capstone Project - GitHub](https://github.com/gputti/PCMLAI_capstone/blob/main/capstone_project.ipynb)


# PCMLAI_capstone
PCMLAI capstone customer conversation sentiment analysis

# Sentiment Classification of Healthcare Customer Support Conversations

---

## 📝 Notes to Reviewer

- **Data Confidentiality**:  
  The dataset used in this project contains proprietary, real-world data from my workplace. To maintain confidentiality, the dataset and all related print statements have been intentionally excluded.

- **Hardware Constraints**:  
  While the full dataset comprises ~290,000 records, model training was conducted on a 100,000-record subset due to local hardware limitations.

---

## 📌 Project Overview

**Objective**:  
Develop a sentiment classification model for healthcare customer support interactions, focusing on detecting *negative* sentiments which are critical for quality monitoring and compliance.

---

## 💼 Business Problem

In the U.S., healthcare companies are required to audit their customer support calls. However, manual auditing is resource-intensive and only allows a fraction of calls to be reviewed.

Using machine learning, especially large language models (LLMs), enables 100% of interactions to be analyzed in real time, improving both compliance and service quality. This project aims to build a scalable sentiment analysis solution as a foundation for such automation.

---

## 🧹 Data Collection, Cleaning & EDA

- **Source**:  
  Data was collected from two Snowflake databases using Apache Spark and SQL, then exported to CSV format. (Data preparation scripts are omitted for relevance.)

- **Dataset Size**:  
  ~290,000 conversations were collected, but only 100,000 rows were used for modeling.

- **Preprocessing Steps**:
  - Text cleaning performed with the `clean-text` package
  - Removal of:
    - Punctuation and special characters
    - Numbers and currency symbols
    - Phone numbers and identifiable numeric strings

- **Key Features**:
  - `conversation` – Customer support dialogue text
  - `sentiment` – Labeled as `positive`, `neutral`, or `negative`

> **Note**: The key business focus is on accurately identifying **negative** sentiments.

---

## 📊 Visualizations

The following charts were generated as part of the project (included in the code):

- Sentiment distribution chart
- Model training curves (accuracy & loss)
- Recall comparison across models
- Confusion matrices

---

## 🤖 Modeling Approach

### Models Used:

- **Primary Model**:  
  - Keras Sequential Neural Network

- **Benchmark Models**:  
  - Logistic Regression  
  - Random Forest Classifier  
  - Gradient Boosting Classifier

### Evaluation Metrics:

Although **accuracy** was calculated, **recall** was prioritized due to the business need to minimize **false negatives** (i.e., failing to detect a negative sentiment).

Metrics evaluated for each model:

- Accuracy
- Recall
- Precision
- F1-score
- Confusion Matrix

> For this use case, **high recall** is essential to avoid overlooking dissatisfied or at-risk customers.

---

## ✅ Summary of Findings

- All models delivered similar performance.
- The **neural network** model achieved slightly better recall than the others.
- Deep learning showed promise for scaling up and deployment in real-world production environments.

---
## Also model file is available at: https://github.com/gputti/PCMLAI_capstone/blob/main/classifier_model.keras
