# Podcast Sentiment Analysis

## Overview
This project focuses on performing sentiment analysis on podcast transcripts using multiple machine learning models, including traditional models, RoBERTa, and ALBERT. The datasets used in this study include the MELD dataset and a collection of Shakespearean texts. The project follows a comprehensive approach, from data collection and preprocessing to model training, evaluation, and analysis of results.

## Datasets
We used two primary datasets:

- **MELD (Multimodal EmotionLines Dataset)**: A widely-used dataset for emotion recognition and sentiment analysis. It includes over 13,000 instances with sentiment and emotion labels derived from multi-turn dialogue conversations.
  
- **Shakespeare Dataset**: A corpus of text from Shakespearean works, which was used to analyze sentiment in a classical literary context.

## Data Preprocessing
Preprocessing is a crucial step before feeding data into the models. The following steps were performed:

1. **Text Cleaning**: Removing special characters, stopwords, and punctuation.
2. **Tokenization**: Breaking down the text into individual tokens suitable for model input.
3. **Lowercasing**: Converting all text to lowercase to ensure consistency.
4. **Labeling Sentiment**: Sentiment scores were assigned based on the data labels provided in the MELD dataset and generated from the Shakespeare texts.

## Models
We implemented three models to perform sentiment analysis:

1. **Traditional Model**: A basic machine learning approach using models like Logistic Regression or Naive Bayes as baselines. These models provide a simple yet effective method to compare against more advanced methods.

2. **RoBERTa (Robustly Optimized BERT Pretraining Approach)**: This transformer-based model was fine-tuned on our datasets to perform sentiment analysis. It is known for its ability to handle large amounts of text data and perform well in NLP tasks.

3. **ALBERT (A Lite BERT)**: ALBERT is a lighter and more efficient variant of BERT, optimized for faster training and lower memory usage while still maintaining accuracy. It was also fine-tuned on the same datasets for sentiment analysis.

## Results and Discussion

### Shakespeare Podcast Dataset Results

| Model                | Accuracy | Precision | Recall | F1-score |
|----------------------|----------|-----------|--------|----------|
| Naive Bayes          | 75.32%   | 0.6851    | 0.7532 | 0.6581   |
| Linear SVC           | 79.22%   | 0.6921    | 0.7922 | 0.7289   |
| Logistic Regression   | 77.92%   | 0.7001    | 0.7792 | 0.7041   |
| SGD Classifier       | 76.62%   | 0.7400    | 0.7662 | 0.7483   |
| **ALBERT**           | **80.51%** | **0.8283** | **0.8051** | **0.7798** |
| **RoBERTa**         | **90.90%** | **0.9091** | **0.9104** | **0.9166** |

### MELD Dataset Results

| Model                | Accuracy | Precision | Recall | F1-score |
|----------------------|----------|-----------|--------|----------|
| Naive Bayes          | 55.17%   | 0.6606    | 0.5517 | 0.4771   |
| Linear SVC           | 50.96%   | 0.5027    | 0.5096 | 0.5019   |
| Logistic Regression   | 52.87%   | 0.5248    | 0.5287 | 0.5101   |
| SGD Classifier       | 49.43%   | 0.4912    | 0.4943 | 0.4915   |
| **ALBERT**           | **66.28%** | **0.6595** | **0.6628** | **0.6553** |
| **RoBERTa**         | **69.34%** | **0.6934** | **0.6952** | **0.7017** |

## Conclusion
The project successfully demonstrated the effectiveness of transformer-based models, particularly RoBERTa and ALBERT, for sentiment analysis tasks on both conversational and classical text datasets. While traditional models provided a useful baseline, the transformer models showed superior results in handling complex text and improving sentiment classification accuracy.

## Future Work
Future work could involve exploring multi-modal sentiment analysis, where audio and visual data are incorporated, or testing other advanced models for NLP tasks.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


