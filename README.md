# Classification_NLP_TensorFlw
##Project Overview
This repository features an end-to-end Natural Language Processing (NLP) pipeline designed to identify and filter spam emails. By leveraging a Long Short-Term Memory (LSTM) neural network, the model understands the sequential context of text to distinguish between legitimate communication ("Ham") and unsolicited messages ("Spam") with high precision.

##Key Highlights:
Data Hygiene: Implemented specialized text cleaning including punctuation removal and stop-word filtering using NLTK.

Class Balancing: Addressed dataset bias by downsampling majority classes to ensure model fairness and prevent overfitting to "Ham" messages.

Advanced Training: Utilized dynamic learning rate reduction and early stopping to optimize convergence.

##Technical Stack
Language: Python 3.x

Deep Learning: TensorFlow / Keras

Data Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn, WordCloud

NLP Tools: NLTK (Natural Language Toolkit)
