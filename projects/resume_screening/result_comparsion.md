# Resume Screening – Model Comparison

This document compares the performance of **spaCy** and **Gensim Word2Vec** embeddings  
for the resume screening (Hire vs Reject) classification task.

---

## Models Compared
- **spaCy (en_core_web_lg)** – n=3
- **Gensim Word2Vec** – n=5

Classifier used: **K-Nearest Neighbors (KNN)**

---

## Metrics

| Embedding       | Accuracy | Precision | Recall |
|-----------------|----------|-----------|--------|
| spaCy (n=3)     | 71.9%    | 70.1%     | 74.2%  |
| Gensim (n=5)    | 73.8%    | 75.5%     | 70.3%  |

---

## Observations
- **spaCy** achieved slightly higher recall, meaning it captured more actual hires.
- **Gensim Word2Vec** achieved higher precision and overall accuracy, making fewer false positives.
- Both models performed similarly (~72–74%), with Gensim having a slight edge overall.

---

## Next Steps
- Add GloVe embeddings for further comparison.
- Experiment with FastText or transformer-based embeddings (BERT, Sentence Transformers).

