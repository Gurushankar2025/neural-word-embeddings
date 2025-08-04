# Resume Screening – Hire or Reject

### Overview
This project predicts whether a resume should be **Hired** or **Rejected** based on combined resume fields  
(excluding ID and Name). Neural word embeddings are used for vectorization and KNN for classification.

---

### Embeddings Used
- **spaCy (en_core_web_lg)** – n = 3
- **Gensim Word2Vec** – n = 5

---

### Classifier
- **K-Nearest Neighbors (KNN)** – best performing model
- Other models tested (Logistic Regression, SVM, Multinomial NB) scored around 50–60%

---

### Best Results
- **Gensim Word2Vec (n=5): ~74% accuracy**
- **spaCy (n=3): ~72% accuracy**

Detailed metrics and confusion matrices are available in  
[`results/comparison.md`](results/comparison.md)

---

### Steps
1. Preprocess resumes (combine all fields except ID/Name)
2. Vectorize using spaCy and Gensim embeddings
3. Handle imbalance with SMOTE
4. Train KNN classifier
5. Evaluate with confusion matrix and metrics

---

### Dataset
- **File:** `AI_Resume_Screening.csv` (stored in `data/`)
- Preprocessing excludes:
  - Resume ID
  - Name

---


