# Twitter-Named-Entity-Recognition-System

## Overview

Built an NER system to automatically detect fine-grained entities in tweets, without relying on hashtags. Helps analyze trends and topics from social media text.

## Objective

- Identify 10 entity types: person, location, company, facility, product, music artist, movie, sports team, TV show, other

- Train models that generalize well to unseen tweets

- Evaluate performance using Precision, Recall, F1-score

## Dataset

- Source: Annotated English tweets

- Format: CoNLL (BIO tagging)

- Structure: One word per line; last column = label; sentences separated by empty line

  `Harry    B-PER`
  `Potter   I-PER`
  `in       O`
  `London   B-geo-loc`

## Approach
- **BiLSTM + CRF**

  - Word2Vec embeddings
  
  - Bidirectional LSTM for context
  
  - CRF layer for sequence labeling

- **Transformer-Based (BERT)**

  - Model: bert-base-uncased

  - Tokenization and subword label alignment
  
  - Early stopping & hyperparameter tuning
  
  - Predictions recombined from subtokens
 
## Pipeline

- Data loading & preprocessing

- Tokenization & label alignment

- Model training & evaluation

- Prediction on custom sentences
  
## Key Insights

- Transformers outperform RNNs on contextual understanding

- Attention-based models capture long-range dependencies better

- Tokenization and label alignment are critical

- Early stopping prevents overfitting
  
## Tools & Technologies

Python, TensorFlow 2.15, Hugging Face Transformers, Word2Vec, Pandas, NumPy, Scikit-learn

## Use Cases

- Trend detection & social media analytics

- Brand, product, and event monitoring

- Automated information extraction from tweets
