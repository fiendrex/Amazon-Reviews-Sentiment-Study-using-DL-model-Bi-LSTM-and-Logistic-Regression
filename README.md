# Amazon-Reviews-Sentiment-Study-using-DL-model-Bi-LSTM-and-Logistic-Regression
# Amazon Customer Review Analysis
## Project Overview

This repository contains a dataset of over 21,000 customer reviews for Amazon. The data is suitable for natural language processing (NLP) tasks, such as sentiment analysis, topic modeling, and understanding key drivers of customer satisfaction and dissatisfaction across different geographical regions.

---

## Dataset Description

The analysis is based on the `Amazon_Reviews.csv` file, which contains review metadata and the full text of customer feedback.

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `Reviewer Name` | Object | The name or pseudonym of the reviewer. |
| `Profile Link` | Object | A unique link identifier for the reviewer's profile. |
| `Country` | Object | The reviewer's country of origin. |
| `Review Count` | Object | The total number of reviews written by the user. |
| `Review Date` | Object | The date and time the review was submitted. |
| `Rating` | Object | The rating given by the user (e.g., 'Rated 1 out of 5 stars'). |
| `Review Title` | Object | The headline or title of the customer review. |
| **`Review Text`** | Object | The full body text of the customer review – **primary text for NLP analysis.** |
| `Date of Experience` | Object | The specific date associated with the experience being reviewed. |

---

## Sentiment Analysis Model Summary

The following models were developed and evaluated for the task of **Sentiment Classification** (e.g., predicting the rating or binary positive/negative sentiment based on the `Review Text`).

| Model | Task | Key Preprocessing Steps | Precision (Max) | Recall (Max) | Accuracy | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Model 1** | Classification | Text Vectorization (e.g., TF-IDF or Word2Vec), Scaling. | 0.92 | **0.97** | **90.52%** | Achieved the highest Recall and overall Accuracy. |
| **Model 2** | Classification | Text Vectorization, Hyperparameter Tuning. | **0.93** | 0.94 | 88.25% | Achieved the highest Precision, focusing on true positive predictions. |

---

## Conclusion

The analysis demonstrates that **Model 1** is the superior choice for this classification task, achieving a maximum accuracy of **$90.52\%$**. Its high Recall of **$0.97$** suggests it is highly effective at identifying the target class (e.g., positive or negative sentiment) and minimizing false negatives.

**Key Model Insights:**
* Model 1 has a balanced performance, making it robust for general sentiment classification.
* Model 2, with slightly higher Precision, might be preferred in scenarios where minimizing false positives is critical (e.g., only identifying high-confidence positive reviews).
