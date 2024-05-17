# multimodal-depression-detection
## Integrating Linguistic and Acoustic Features for Depression Detection: A Comparative Analysis of ML Models

### Overview

This project presents a comparative analysis of machine learning (ML) models for depression detection by integrating linguistic and acoustic features. The study utilized the DAIC-WOZ interviews, extracting linguistic features such as absolutist words and emotions, and acoustic features like prosodic and vocal tract characteristics. The performance of three distinct ML models was evaluated to determine the effectiveness of combining these features in detecting depression.

### Introduction
Depression is a significant mental health disorder affecting millions worldwide. Traditional diagnostic methods are often subjective and resource-intensive. This study explores the potential of machine learning to automate depression detection using both linguistic and acoustic features from interview data. The goal is to enhance the accuracy and reliability of diagnostic tools, providing timely and effective interventions.

### Data
The dataset used in this study consists of 189 recordings from the DAIC-WOZ corpus, which includes both audio recordings and text transcriptions of interactions between individuals and a virtual agent. Participants were screened for depression using the PHQ-8 questionnaire, and their responses were labeled as either depressed or not depressed.

### Methodology
#### Unimodal Approach
The unimodal approach focuses on text features extracted from interview transcripts. Preprocessing steps include tokenization, stop word removal, and lemmatization. Features analyzed:

- **Positive and Negative Emotion Scores**: Derived using LIWC-22 software.
- **Frequency of Absolutist Words**: Using an expanded dictionary of absolutist terms.

Three ML models were used for classification:
- Random Forest
- Gaussian Naive Bayes
- Gradient Boosting

#### Multimodal Approach
The multimodal approach integrates both text and acoustic features. Acoustic features were extracted using the COVAREP toolbox, focusing on:

- **Prosodic Features**: Fundamental frequency (F0) and Voiced/Unvoiced (VUV) segments.
- **Vocal Tract Features**: First two formants (F1, F2).

The combined features were used to train the same ML models for depression classification.

### Results

#### Performance of Unimodal Approach with Text Features

| Model                | F1 Score | Precision | Recall | Accuracy |
|----------------------|----------|-----------|--------|----------|
| Random Forest        | 0.25     | 0.29      | 0.22   | 0.58     |
| Gaussian Naive Bayes | 0.33     | 0.42      | 0.28   | 0.65     |
| Gradient Boosting    | 0.41     | 0.44      | 0.39   | 0.65     |

#### Performance of Multimodal Approach with Text and Speech Features

| Model                | F1 Score | Precision | Recall | Accuracy |
|----------------------|----------|-----------|--------|----------|
| Random Forest        | 0.50     | 0.57      | 0.44   | 0.72     |
| Gaussian Naive Bayes | 0.42     | 0.47      | 0.39   | 0.66     |
| Gradient Boosting    | 0.56     | 0.64      | 0.50   | 0.75     |

### Comparison of Unimodal and Multimodal Approaches

Comparing the unimodal and multimodal approaches, the results indicated that the multimodal approach achieved better performance in depression detection. The F1 scores improved from 0.41 in the unimodal text approach to 0.56 in the multimodal approach, indicating a significant enhancement in the model’s ability to correctly identify depressed individuals. The inclusion of speech features provided additional contextual information, resulting in improved precision, recall, and accuracy scores in the multimodal models.


### Conclusion
This study highlights the potential of integrating linguistic and acoustic features for automated depression detection using ML models. The multimodal approach significantly improves detection accuracy, providing a foundation for developing scalable and accessible diagnostic tools. Future work includes incorporating LSTM or neural networks and integrating video features for a more comprehensive analysis.
