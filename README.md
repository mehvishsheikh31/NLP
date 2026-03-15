# NLP
Complete NLP roadmap for beginners — 5 Google Colab notebooks covering Text Preprocessing, BoW, TF-IDF, Word2Vec, LSTM, and BERT. Every line of code explained. CampusX playlist companion.
# 🧠 NLP Basics — CampusX Playlist Notebooks

> **Complete NLP roadmap from scratch to BERT — every line of code explained.**
> Built for absolute beginners following the [CampusX NLP Playlist](https://www.youtube.com/@campusx-official).

---

## 📌 What is this repo?

This repository contains **5 beginner-friendly Google Colab notebooks** covering the complete basics of Natural Language Processing (NLP).

Every notebook is written so that:
- ✅ **Every single line of code has a comment explaining it**
- ✅ **No advanced concepts — only what you need to understand NLP**
- ✅ **Each topic builds on the previous one**
- ✅ **Practice cells at the end of every notebook**
- ✅ **Works 100% in Google Colab — no local setup needed**

---

## 📂 Notebooks in this repo

| File | Phase | Topics Covered |
|------|-------|----------------|
| `NLP_Phase1.ipynb` | Phase 1 | Text Cleaning, Tokenization, Stopwords, Stemming, Lemmatization |
| `NLP_Phase2.ipynb` | Phase 2 | Bag of Words, TF-IDF, N-grams, Spam Detector |
| `NLP_Phase3.ipynb` | Phase 3 | Word2Vec, Cosine Similarity, Word Analogy, GloVe, FastText |
| `NLP_Phase4.ipynb` | Phase 4 | RNN idea, LSTM, Sentiment Analysis with Deep Learning |
| `NLP_Phase5.ipynb` | Phase 5 | Transformers, BERT, Hugging Face, Fine-tuning |

---

## 🗺️ The NLP Roadmap

```
Phase 1 → Clean Text
          tokenize · remove stopwords · stem · lemmatize
             ↓
Phase 2 → Text as Numbers
          Bag of Words · TF-IDF · N-grams · Spam Classifier
             ↓
Phase 3 → Word Meaning
          Word2Vec · Cosine Similarity · GloVe · FastText
             ↓
Phase 4 → Deep Learning
          RNN · LSTM · Sentiment Analysis
             ↓
Phase 5 → State of the Art
          Transformers · BERT · Hugging Face · Fine-tuning
```

---

## 🚀 How to Use

### Option 1 — Open directly in Google Colab (recommended)

1. Click any notebook file in this repo
2. Click the **"Open in Colab"** button at the top of the file
3. Press **Shift + Enter** to run each cell from top to bottom

### Option 2 — Download and upload manually

1. Download the `.ipynb` file you want
2. Go to [colab.research.google.com](https://colab.research.google.com)
3. Click **File → Upload Notebook**
4. Select the downloaded file
5. Run cells with **Shift + Enter**

---

## 📖 Phase-by-Phase Summary

### Phase 1 — Text Preprocessing
**What you learn:** How to clean raw messy text before feeding it to any model.

```python
# Example: clean a messy tweet
text = "<p>OMG!!! India WON!! #Cricket @BCCI https://scores.com 🏏</p>"

# After Phase 1 pipeline:
output = ['india', 'win', 'cricket']   # clean, meaningful tokens only
```

Topics: text cleaning with regex, word tokenization, sentence tokenization,
stopword removal, stemming vs lemmatization.

---

### Phase 2 — Bag of Words and TF-IDF
**What you learn:** How to convert text into numbers that ML models understand.

```python
# Bag of Words
vectorizer = CountVectorizer()
X = vectorizer.fit_transform(reviews)   # text → number matrix

# TF-IDF (smarter — scores word importance)
tfidf = TfidfVectorizer()
X = tfidf.fit_transform(reviews)
```

Topics: CountVectorizer, TfidfVectorizer, N-grams, Naive Bayes classifier,
train/test split, accuracy score. Final project: spam detector.

---

### Phase 3 — Word Embeddings
**What you learn:** How to give words meaningful number representations so
similar words are close together.

```python
# Train Word2Vec
model = Word2Vec(sentences=tokenized, vector_size=50, window=3)

# Find similar words
model.wv.most_similar('cricket', topn=5)

# Word analogy: king - man + woman = ?
model.wv.most_similar(positive=['king','woman'], negative=['man'])
```

Topics: Word2Vec, cosine similarity, word analogy, GloVe pre-trained vectors,
FastText (handles typos and unknown words).

---

### Phase 4 — Deep Learning for NLP
**What you learn:** How LSTM reads text word by word with memory,
unlike traditional ML models.

```python
# Build LSTM model
model = Sequential([
    Embedding(vocab_size, 16, input_length=20),
    LSTM(32),
    Dropout(0.5),
    Dense(1, activation='sigmoid')
])

model.fit(X_train, y_train, epochs=30)
```

Topics: RNN concept, LSTM (Long Short-Term Memory), Embedding layer,
Dropout, training and plotting accuracy/loss curves, sentiment analysis.

---

### Phase 5 — Transformers and BERT
**What you learn:** How BERT reads ALL words at once (not one by one)
and how to use it with just a few lines of code.

```python
# Use BERT in 3 lines
from transformers import pipeline
model = pipeline('sentiment-analysis')
result = model("This movie was amazing!")
# → {'label': 'POSITIVE', 'score': 0.9998}
```

Topics: Transformer attention concept, Hugging Face pipeline,
sentiment analysis, Named Entity Recognition (NER), Question Answering,
Fill-Mask, DistilBERT fine-tuning on custom data.

---

## 🛠️ Libraries Used

| Library | Used for | Install |
|---------|----------|---------|
| `nltk` | Tokenization, stopwords, stemming, lemmatization | `pip install nltk` |
| `scikit-learn` | BoW, TF-IDF, Naive Bayes, train/test split | `pip install scikit-learn` |
| `gensim` | Word2Vec, FastText | `pip install gensim` |
| `tensorflow` | LSTM, Embedding, deep learning | Pre-installed in Colab |
| `transformers` | BERT, Hugging Face models | `pip install transformers` |
| `pandas` | Data tables | `pip install pandas` |
| `matplotlib` | Charts and graphs | `pip install matplotlib` |

> All installations are handled inside each notebook. Just run the first cell!

---


# New (fixed)
eval_strategy='epoch'
```

---

## 📋 Prerequisites

You do NOT need to install anything on your computer.
Everything runs in **Google Colab** (free, browser-based).

You should know basic Python:
- Variables and data types
- Lists and dictionaries  
- For loops and functions
- If/else statements

That is all. No math, no ML background needed to start!

---

## 🎯 Who is this for?

- Students following the **CampusX NLP playlist**
- Beginners who want to learn NLP from scratch
- Anyone who wants working Colab notebooks with clear explanations
- People who got confused by other NLP tutorials and want simpler code

---

## 📊 What you will be able to build after all 5 phases

- ✅ Spam SMS detector
- ✅ Movie sentiment classifier
- ✅ Word similarity finder (like a thesaurus)
- ✅ Question answering system
- ✅ Named entity extractor (find names, places from text)
- ✅ Fine-tuned BERT for your own classification task

---

## 🙏 Credits

- Notebooks built as a companion to the **CampusX NLP Playlist**
- Pre-trained models from [Hugging Face](https://huggingface.co)
- GloVe vectors from [Stanford NLP](https://nlp.stanford.edu/projects/glove/)

---

## 📄 License

This project is open source and free to use for learning purposes.

---

*Happy Learning! If this helped you, give the repo a ⭐*
