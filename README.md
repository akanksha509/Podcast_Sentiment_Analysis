# Podcast Sentiment Analysis

## Overview
This project focuses on performing sentiment analysis on podcast transcripts using multiple machine learning models, including traditional models, RoBERTa, and ALBERT. The datasets used in this study include the MELD dataset and a collection of Shakespearean texts. The project follows a comprehensive approach, from data collection and preprocessing to model training, evaluation, and analysis of results.

## Datasets
We used two primary datasets:

- **MELD (Multimodal EmotionLines Dataset)**: A widely-used dataset for emotion recognition and sentiment analysis. It includes over 13,000 instances with sentiment and emotion labels derived from multi-turn dialogue conversations.
- **Shakespeare Dataset**: A corpus of text from Shakespearean works, which was used to analyze sentiment in a classical literary context.

## Data Preprocessing
Preprocessing is a crucial step before feeding data into the models. The following steps were performed:

- **Text Cleaning**: Removing special characters, stopwords, and punctuation.
- **Tokenization**: Breaking down the text into individual tokens that are suitable for model input.
- **Lowercasing**: Converting all text to lowercase to ensure consistency.
- **Labeling Sentiment**: Sentiment scores were assigned based on the data labels provided in the MELD dataset and generated from the Shakespeare texts.

## Results
The performance of both traditional machine learning models and advanced deep learning models was evaluated across the two datasets: Shakespeare podcast transcripts (informational content) and MELD (conversational content). Each model was analyzed for accuracy, precision, recall, F1-score, and ROC-AUC to assess its effectiveness in sentiment classification.

### Shakespeare Podcast Dataset Results
#### Traditional Machine Learning Models
The performance metrics of the traditional machine learning models used in the Shakespeare dataset analysis are summarized in Table below. These models include Naive Bayes, Linear SVC, Logistic Regression, and SGD Classifier, evaluated based on accuracy, precision, recall, and F1-score.

| Models             | Accuracy | Precision | Recall | F1-score |
|--------------------|----------|-----------|--------|----------|
| Naive Bayes        | 0.7532   | 0.6851    | 0.7532 | 0.6581   |
| Linear SVC         | 0.7922   | 0.6921    | 0.7922 | 0.7289   |
| Logistic Regression | 0.7792   | 0.7001    | 0.7792 | 0.7041   |
| SGD Classifier     | 0.7662   | 0.7400    | 0.7662 | 0.7483   |

#### Deep Learning Models
The performance of the deep learning models ALBERT and RoBERTa on the Shakespeare podcast dataset is summarized below.

| Models   | Accuracy | Precision | Recall | F1-score |
|----------|----------|-----------|--------|----------|
| ALBERT   | 0.8051   | 0.8283    | 0.8051 | 0.7798   |
| RoBERTa  | 0.9090   | 0.9091    | 0.9104 | 0.9166   |

### MELD Dataset Results
#### Traditional Machine Learning Models
The results for traditional machine learning models on the MELD dataset are presented in the table below.

| Models             | Accuracy | Precision | Recall | F1-score |
|--------------------|----------|-----------|--------|----------|
| Naive Bayes        | 0.5517   | 0.6606    | 0.5517 | 0.4771   |
| Linear SVC         | 0.5096   | 0.5027    | 0.5096 | 0.5019   |
| Logistic Regression | 0.5287   | 0.5248    | 0.5287 | 0.5101   |
| SGD Classifier     | 0.4943   | 0.4912    | 0.4943 | 0.4915   |

#### Deep Learning Models
The performance of the deep learning models on the MELD dataset is presented below.

| Models   | Accuracy | Precision | Recall | F1-score |
|----------|----------|-----------|--------|----------|
| ALBERT   | 0.6628   | 0.6595    | 0.6628 | 0.6553   |
| RoBERTa  | 0.6934   | 0.6934    | 0.6952 | 0.7017   |

## ROC Curves
### For the Shakespeare Dataset:
- **ALBERT**: High discriminative power with AUC values of 0.95 (positive), 0.85 (neutral), and 0.77 (negative).
  ![Screenshot 2024-12-10 183744](https://github.com/user-attachments/assets/35113184-e4a8-4890-a8ae-3366e00890f6)

- **RoBERTa**: Outperforms ALBERT with AUC values of 0.99 (positive), 0.93 (neutral), and 0.96 (negative).
  ![Screenshot 2024-12-10 183823](https://github.com/user-attachments/assets/d6485d19-b6a0-4eb3-9350-e1e4db8d1178)

### For the MELD Dataset:
- **ALBERT**: Moderate performance with AUC values of 0.83 (positive), 0.86 (neutral), and 0.84 (negative).
  ![Screenshot 2024-12-10 183754](https://github.com/user-attachments/assets/014ee36a-605d-4b5e-bccb-13383dc2471b)
  
- **RoBERTa**: Slightly better with AUC values of 0.84 (positive), 0.82 (neutral), and 0.80 (negative).
  ![Screenshot 2024-12-10 183834](https://github.com/user-attachments/assets/f7c280e2-1a22-49eb-9b9a-6cc34a3da64c)
  
## Conclusion
The project successfully demonstrated the effectiveness of transformer-based models, particularly RoBERTa and ALBERT, for sentiment analysis tasks on both conversational and classical text datasets. While traditional models provided a useful baseline, the transformer models showed superior results in handling complex text and improving sentiment classification accuracy.

Future work could involve exploring multi-modal sentiment analysis, where audio and visual data are incorporated, or testing other advanced models for NLP tasks.



