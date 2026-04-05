# Classification_NLP_TensorFlw
Project Overview
This repository features an end-to-end Natural Language Processing (NLP) pipeline designed to identify and filter spam emails. By leveraging a Long Short-Term Memory (LSTM) neural network, the model understands the sequential context of text to distinguish between legitimate communication ("Ham") and unsolicited messages ("Spam") with high precision.

Key Highlights:
Data Hygiene: Implemented specialized text cleaning including punctuation removal and stop-word filtering using NLTK.

Class Balancing: Addressed dataset bias by downsampling majority classes to ensure model fairness and prevent overfitting to "Ham" messages.

Advanced Training: Utilized dynamic learning rate reduction and early stopping to optimize convergence.

Technical Stack
Language: Python 3.x

Deep Learning: TensorFlow / Keras

Data Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn, WordCloud

NLP Tools: NLTK (Natural Language Toolkit)

Machine Learning Pipeline
1. Data Preprocessing & EDA
Imbalance Handling: Balanced the dataset to a 1:1 ratio to ensure the model learns features of both classes equally.

Cleaning: Stripped email-specific headers (e.g., "Subject:"), removed stop words, and eliminated noise via punctuation filtering.

Visualization: Generated WordClouds to identify high-frequency keywords in Spam vs. Ham categories.

2. Neural Network Architecture
The model utilizes a sequential architecture optimized for text data:

Embedding Layer: Maps words into a 32-dimensional dense vector space.

LSTM Layer: A 16-unit Long Short-Term Memory layer to capture temporal dependencies and context in sentences.

Dense Layers: A 32-unit ReLU hidden layer followed by a Sigmoid output layer for binary classification.

3. Model Optimization
To ensure production-grade performance, the training process included:

EarlyStopping: Monitored val_accuracy to halt training once improvements plateaued, saving the best weights.

ReduceLROnPlateau: Automatically halved the learning rate when val_loss stalled, allowing for finer weight adjustments.

Results
The model achieved impressive results within 8 epochs:

Validation Accuracy: 97.0%

Validation Loss: 0.13

Convergence: The model demonstrated high stability, with the learning rate successfully adapting to minimize loss.



Future Enhancements
[ ] Implement BERT or RoBERTa transformers for state-of-the-art context understanding.

[ ] Deploy the model as a REST API using FastAPI or Flask.

[ ] Integrate a frontend dashboard for real-time email scanning.
