📰 Fake News Detection using Deep Learning (LSTM)
📌 Project Overview
This project is an end-to-end Natural Language Processing (NLP) pipeline designed to classify news articles as either REAL or FAKE based strictly on their text content. It leverages custom word embeddings and a Recurrent Neural Network (RNN) architecture to analyze the sequential context of words in news reporting.
🚀 Tech Stack & Tools
Language: Python
Deep Learning Framework: TensorFlow / Keras
NLP & Text Processing: NLTK, Gensim (Word2Vec)
Data Manipulation: Pandas, NumPy
Evaluation & Splitting: Scikit-learn
🧠 Model Architecture & Pipeline
The project follows a rigorous data science workflow:
Data Preprocessing: Raw article text is cleaned by removing punctuation, special characters, and English stopwords using NLTK.
Word Embeddings (Word2Vec): Instead of sparse matrices (like TF-IDF), a custom Word2Vec model is trained locally to generate dense, 100-dimensional semantic vectors for the vocabulary.
Tokenization & Padding: Text sequences are uniformly padded to 500 tokens to feed into the neural network.
Deep Learning Model:
Input/Embedding Layer: Ingests the pre-trained Word2Vec matrix.
LSTM Layer (64 units): Captures the long-term dependencies and context of the words in the article.
Dropout Layer (0.2): Implemented for regularization to prevent overfitting.
Dense Layers: A hidden layer with ReLU activation, followed by a final output node using a Sigmoid activation function for binary classification (0 = Fake, 1 = Real).
📊 Evaluation Metrics
The model's performance is validated on a 20% holdout test set using:
Binary Crossentropy Loss
Accuracy
Precision, Recall, and F1-Score
Confusion Matrix analysis

<img width="817" height="532" alt="Screenshot 2026-06-21 181758" src="https://github.com/user-attachments/assets/1df03393-8452-4969-8afc-e1bc5af45df7" />
