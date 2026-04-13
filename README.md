# NLP Sentiment Analysis — Movie Reviews

> **Python · NLTK · VADER · AFINN · WordNet · Word2Vec · LSTM · TensorFlow**

A complete **Natural Language Processing (NLP)** pipeline for sentiment analysis on movie reviews. Compares lexicon-based approaches (AFINN, VADER, WordNet) with deep learning models (Word2Vec + Neural Network, LSTM).

---

## What it does

Takes raw movie reviews and classifies them as **positive** or **negative** using multiple approaches:

```
Raw review text
      │
      ▼
┌─────────────────────┐
│  Text Preprocessing │  HTML removal, stopwords, contractions, accents
└──────────┬──────────┘
           │
     ┌─────┴──────┐
     ▼            ▼
Lexicon-based   Deep Learning
─────────────   ─────────────
AFINN           Word2Vec CBOW
VADER           Word2Vec Skip-gram
WordNet         LSTM
```

---

## Pipeline

### 1. Text Preprocessing
- Remove HTML tags (`BeautifulSoup`)
- Remove accented characters (`unicodedata`)
- Expand contractions (`we'll` → `we will`)
- Remove stopwords (`NLTK`)
- Tokenization (`ToktokTokenizer`)

### 2. Lexicon-based Models
| Model | Description |
|---|---|
| **AFINN** | Word-level sentiment scores (-5 to +5) |
| **WordNet** | Synset-based positive/negative scoring |
| **VADER** | Compound score sensitive to intensity |

### 3. Deep Learning Models
| Model | Description |
|---|---|
| **Word2Vec CBOW** | Context → target word (size=500) |
| **Word2Vec Skip-gram** | Target → context words (size=500) |
| **LSTM** | Sequential model with embedding layer |

---

## Dataset

- **Movie reviews** dataset with `review` and `sentiment` columns
- 2,500 positive + 2,500 negative reviews (balanced)
- Split: 4,000 train / 1,000 test

---

## Results

| Model | Approach |
|---|---|
| AFINN | Lexicon — word polarity scores |
| VADER | Lexicon — compound sentiment score |
| WordNet | Lexicon — synset aggregation |
| Word2Vec + NN | Embedding + Dense layers |
| LSTM | Embedding + Sequential learning |

---

## Stack

- **Language:** Python 3.x
- **NLP:** NLTK, spaCy, contractions, BeautifulSoup
- **Lexicons:** AFINN, VADER, SentiWordNet
- **Embeddings:** Gensim Word2Vec (CBOW + Skip-gram)
- **Deep Learning:** TensorFlow / Keras (LSTM)
- **Evaluation:** scikit-learn (F1, accuracy, precision, recall)

---

## Requirements

```bash
pip install nltk spacy afinn contractions beautifulsoup4
pip install gensim tensorflow scikit-learn pandas numpy
python -m spacy download en_core_web_sm
```

---

## Quick start

```bash
# 1. Clone
git clone https://github.com/PiriTnz/nlp-sentiment-analysis.git
cd nlp-sentiment-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add dataset
# → place movie_reviews.csv in the project folder

# 4. Run
jupyter notebook sentiment_analysis.ipynb
```

---

## Project structure

```
nlp-sentiment-analysis/
├── sentiment_analysis.ipynb   # main notebook
├── movie_reviews.csv          # dataset (not included in repo)
├── requirements.txt
└── README.md
```

---

## Skills demonstrated

`NLP` · `Text Preprocessing` · `Sentiment Analysis` · `VADER` · `AFINN` · `WordNet` · `Word2Vec` · `LSTM` · `TensorFlow` · `Gensim` · `NLTK` · `scikit-learn`

---

## Author

**Tanaz Piriaei** — Ingénieure IA Logicielle  
M2 Informatique — Données, Intelligence & Systèmes Intelligents  
Université Claude Bernard Lyon 1  
[LinkedIn](https://linkedin.com/in/tanaz-piriaei-b34b512a6) · [GitHub](https://github.com/PiriTnz)
