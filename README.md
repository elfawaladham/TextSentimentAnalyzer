# 🧐 Text Sentiment Classification

This project implements a text sentiment classification model using TensorFlow and Keras to predict whether a given review is positive or negative. The project explores different model architectures such as MLP, CNN, and LSTM for classifying the sentiment of text reviews.

## 📚 Problem Statement

The goal of this project is to build a classifier that analyzes the sentiment of reviews. The dataset consists of text files categorized into two folders: one containing positive reviews and the other containing negative reviews. The classifier is trained to predict whether a new review is positive or negative.

## 🔧 Installation

To run this project, you need to install the following dependencies:

```bash
pip install -r requirements.txt
```

## 📦 Dataset

The dataset consists of two folders:

- pos/: Contains positive reviews.
- neg/: Contains negative reviews.

Each folder has multiple text files representing individual reviews. The dataset is preprocessed and split into training and testing sets.

## 🧮 Data Preprocessing

- Tokenization: The text is tokenized using Keras’ Tokenizer, and the top 5,000 words are retained. Words not in the top 5,000 are replaced with an ‘UNK’ token.
- Padding: Reviews are padded or truncated to a fixed length based on the 70th percentile of review lengths.
- Word Embeddings: Keras’ Embedding layer is used to convert tokenized words into dense vectors for model training.

## 💬 Model Architectures

Three different models were built and evaluated for sentiment classification:
1. Multilayer Perceptron (MLP):
- embedding layer followed by several fully connected dense layers.
- Achieved 82.4% training accuracy and 63.8% test accuracy.
2. Convolutional Neural Network (CNN):
- Embedding layer followed by a Conv1D layer and MaxPooling1D for feature extraction.
- Achieved 64.2% training accuracy and 55.3% test accuracy.
3. Long Short-Term Memory (LSTM):
- Embedding layer followed by an LSTM layer for capturing sequential dependencies.
- Achieved the best performance with 98.0% training accuracy and 80.0% test accuracy.# TextSentimentAnalyzer
