# neural Word Embeddings – Projects

This repository contains **projects demonstrating neural word embeddings** for practical NLP tasks.  
Current work includes **resume screening (hire/reject)** and upcoming **embedding operations** with Word2Vec and GloVe.

---

## Projects

### 1. Resume Screening (Hire or Reject)
- Predicts whether a resume should be **Hired** or **Rejected**
- Combines all resume fields (excluding ID and Name) into unified text
- Vectorized using:
  - **spaCy large model (en_core_web_lg)** – n = 3
  - **Gensim Word2Vec** – n = 5
- Classifier: **K-Nearest Neighbors (KNN)** (best performer)
- **Best result:** Gensim ~74% accuracy (spaCy ~72%)

Detailed metrics and confusion matrices are in  
[`projects/resume-screening/results/comparison.md`](projects/resume-screening/results/comparison.md)

---

### 2. Neural Embedding Operations (Upcoming)
- Word similarity checks
- Most similar words retrieval
- Odd-one-out (doesn’t match) operations
- Using Word2Vec and GloVe embeddings

---

## Dataset
- **File:** `AI_Resume_Screening.csv`
- Located at: `data/`
- Preprocessing excludes:
  - Resume ID
  - Name

---

## Tech Stack
- **spaCy** – pre-trained word vectors (`en_core_web_lg`)
- **Gensim** – Word2Vec embeddings
- **python-Levenshtein** – optimized similarity for Gensim
- **scikit-learn** – KNN, metrics
- **imblearn** – class imbalance handling (SMOTE)
- **pandas, numpy, matplotlib, seaborn** – data handling & visualization

---

## Setup

Clone repo and install dependencies:
```bash
git clone <repo-link>
cd neural-word-embeddings
pip install -r requirements.txt
python -m spacy download en_core_web_lg
