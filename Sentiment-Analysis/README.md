# Sentiment Analysis Projects

This part of my portfolio showcases sentiment analysis projects built on real product reviews and movie reviews, progressing from data cleaning and classical labeling to LSTM-based deep learning models.[file:5][file:6]

## 1. Product Review Sentiment Analysis (Kaggle E‑Commerce Data)

**Goal:** Predict customer sentiment (Positive, Neutral, Negative) from real-world product reviews in a women’s clothing e‑commerce dataset.[file:5]

**What I did:**
- Loaded and explored the Kaggle “Women’s Clothing E-Commerce Reviews” dataset and removed irrelevant or noisy columns (IDs, titles, recommendation flags). [file:5]
- Cleaned the text by handling missing reviews, converting to lowercase, and removing special characters to standardize the input. [file:5]
- Created sentiment labels from numeric ratings via a custom function: low ratings as Negative, mid ratings as Neutral, and high ratings as Positive. [file:5]

**Modeling approach:**
- Tokenized review text with Keras `Tokenizer` (top 5,000 words) and padded sequences to a fixed length. [file:5]
- One-hot encoded the three sentiment classes using `get_dummies` for multi-class classification. [file:5]
- Built an LSTM-based model: Embedding layer (vocab size 5,000, embedding dim 256) → LSTM (256 units with dropout and recurrent dropout) → Dense (3 units, softmax). [file:5]
- Trained with categorical cross-entropy loss and Adam optimizer for 5 epochs, achieving about 81% accuracy on the test set. [file:5]

**Results & usage:**
- Evaluated the model on a held-out test set to quantify generalization performance. [file:5]
- Implemented a `predict_sentiment` helper that tokenizes and pads new review text, runs inference, and returns “Positive”, “Neutral”, or “Negative”. [file:5]

---

## 2. Movie Review Sentiment Analysis with LSTM (IMDB)

**Goal:** Build and debug an LSTM model for binary sentiment classification on the IMDB movie reviews dataset using Keras. [file:6]

**What I did:**
- Loaded IMDB reviews via `tf.keras.datasets.imdb` with a vocabulary limit of the top 10,000 words. [file:6]
- Explored the encoded reviews and word index, and experimented with decoding integer sequences back to text to better understand the data. [file:6]
- Preprocessed text using a Keras `Tokenizer` with an out-of-vocabulary token and padded/truncated sequences to a fixed length (100 tokens). [file:6]

**Modeling approach:**
- Defined a Sequential model: Embedding (10,000 vocab size, 16-dim) → stacked LSTM layers → Dense (24 units, ReLU) → Dropout → Dense (1 unit, sigmoid) for binary sentiment output. [file:6]
- Compiled the model with binary cross-entropy loss, Adam optimizer, and accuracy metric. [file:6]
- Encountered and resolved issues such as data cardinality mismatches between features and labels, ensuring that padded sequences and label arrays aligned in size before training. [file:6]

**Key learnings:**
- Understood the full LSTM sentiment pipeline: integer-encoded sequences → padding → embedding → recurrent layers → dense output. [file:6]
- Gained experience troubleshooting common deep learning pitfalls (import changes, shape mismatches, and dataset handling) when working with Keras and TensorFlow. [file:5][file:6]

---

## Skills Demonstrated

- **Data preprocessing:** Handling null values, text normalization, regex-based cleaning, and label engineering from numeric ratings. [file:5]
- **NLP & vectorization:** Tokenization, vocabulary limiting, sequence padding and truncation, and one-hot encoding of labels. [file:5][file:6]
- **Deep learning for NLP:** Designing, training, and debugging LSTM models with Embedding layers for both multi-class and binary sentiment classification. [file:5][file:6]
- **Model evaluation & inference:** Using held-out test sets, accuracy metrics, and helper functions for deployment-style sentiment prediction on new text. [file:5][file:6]

