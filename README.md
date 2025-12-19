# Resume-Based Job Recommendation System

## Overview
This project focuses on building and evaluating a data-driven job recommendation system that matches candidate resumes to relevant job postings using multiple similarity-based machine learning approaches.

The goal is to compare lexical, semantic, and embedding-based techniques for resume–job matching and design an ensemble ranking strategy that improves top-N recommendation quality.

---

## Problem Statement
Job seekers often struggle to identify relevant roles from large volumes of job postings, while traditional keyword-based matching fails to capture semantic relevance.  
This project addresses the problem by evaluating multiple NLP-based similarity methods and combining their strengths into a robust recommendation pipeline.

---

## Dataset
- **Resumes:** 2,200+ anonymized resumes  
- **Job Postings:** 15,000+ job descriptions  
- **Text Fields:** Resume content, job titles, job descriptions  
- **Scale:** ~17K total documents  

---

## Approach

### 1. Data Preprocessing
- Text cleaning and normalization
- Tokenization and lemmatization using spaCy
- Stopword removal and batching for large-scale processing

### 2. Feature Representation
- TF-IDF vectorization
- BM25 scoring
- Word2Vec and Doc2Vec embeddings
- Sentence-BERT embeddings for semantic similarity

### 3. Similarity & Ranking
- Cosine similarity for vector-based methods
- Ranking comparison across models
- Ensemble ranking combining BM25, SBERT, and fuzzy similarity

---

## Models & Methods
- TF-IDF + Cosine Similarity
- BM25
- Word2Vec
- Doc2Vec
- Sentence-BERT
- Ensemble ranking approach

---

## Evaluation
- Compared ranking quality across models
- Analyzed semantic relevance of top-N recommendations
- Evaluated consistency and stability of rankings across resume samples

---

## Results & Insights
- Lexical models (TF-IDF, BM25) performed well for keyword-heavy resumes
- Embedding-based models (SBERT) captured semantic relevance better for sparse resumes
- Ensemble ranking improved recommendation consistency and relevance compared to individual models
- Model performance varied based on resume length and content density

---

## Limitations & Future Work

- Evaluation was primarily qualitative due to the absence of labeled ground truth for resume–job relevance; future work could incorporate human-labeled relevance judgments or implicit feedback.
- The system currently operates on static datasets; integrating external job APIs could enable real-time job ingestion and recommendations.
- Future enhancements may include personalization, learning-to-rank models, and interactive feedback loops to continuously improve recommendation quality.

---

## Tools & Technologies
Python, pandas, NumPy, scikit-learn, spaCy, Sentence-Transformers
