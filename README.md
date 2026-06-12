# Semantic Search Engine for Large-Scale Information Retrieval
Semantic Search Engine using Word2Vec, SBERT, and Hybrid Retrieval techniques on the MS MARCO dataset with Gradio-based interactive search

## Overview

This project implements and compares multiple semantic document retrieval approaches using the **MS MARCO dataset**. The goal is to improve search quality beyond traditional keyword matching by leveraging word embeddings and transformer-based sentence embeddings.

Three retrieval architectures were designed, implemented, evaluated, and compared:

- **Design 1:** Word2Vec + Query Expansion
- **Design 2:** SBERT (Bi-Encoder) + FAISS
- **Design 3:** Hybrid Retrieval with Re-ranking

An interactive **Gradio-based web interface** was also developed to demonstrate and compare retrieval performance.

---

## Dataset

**MS MARCO (Microsoft Machine Reading Comprehension Dataset)**

- 200,000 training queries
- Approximately 2 million passages
- Evaluation performed on sampled benchmark queries with available relevance judgments

Dataset Sources:

- MS MARCO: https://microsoft.github.io/msmarco/
- Hugging Face: https://huggingface.co/datasets/microsoft/ms_marco

---

## Project Objectives

- Build a semantic search system capable of retrieving relevant documents.
- Compare classical embedding methods with transformer-based retrieval.
- Study the impact of query expansion techniques.
- Evaluate retrieval effectiveness using standard Information Retrieval metrics.
- Develop an interactive demonstration interface for users.

---

## Retrieval Designs

### Design 1: Word2Vec + Query Expansion

- Trained Word2Vec embeddings on the passage corpus.
- Expanded user queries using semantically similar terms.
- Retrieved relevant passages using embedding similarity.

### Design 2: SBERT (Bi-Encoder) + FAISS

- Generated dense sentence embeddings using Sentence-BERT.
- Indexed passage embeddings using FAISS.
- Retrieved top-k passages using approximate nearest neighbour search.

### Design 3: Hybrid Retrieval with Re-ranking

- Combined retrieval strengths from previous designs.
- Retrieved candidate passages efficiently.
- Applied re-ranking to improve final retrieval quality.

---

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Gensim
- Sentence Transformers
- FAISS
- Hugging Face Datasets
- Scikit-learn
- Gradio
- NLTK
- Matplotlib

---

## Evaluation Metrics

The retrieval systems were evaluated using standard Information Retrieval metrics:

- Precision@K
- Recall@K
- F1 Score
- Mean Reciprocal Rank (MRR)
- Normalized Discounted Cumulative Gain (NDCG)

Latency analysis was also conducted to compare retrieval efficiency across designs.

---

## Gradio Demonstration

A Gradio-based web application was developed to provide an interactive interface where users can:

- Enter custom search queries.
- Select retrieval methods.
- Compare retrieval results.
- View ranking scores.
- Observe retrieval latency.

## Demo

---

## Repository Structure

```text
Semantic_Search_Engine/
│
├── Search_Engine.ipynb    # Complete implementation notebook
├── requirments.txt                 # Required Python packages
├── README.md                       # Project documentation
├── project_proposal.pdf            # Initial project proposal
├── final_presentation.pdf          # Project presentation slides
├── project_report.pdf              # Final project report
└── grdio_demo.png                  # Gradio interface screenshot
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/sidda19/Semantic_Search_Engine.git
cd Semantic_Search_Engine
pip install -r requirments.txt
```

---

## Running the Project

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Install the required packages.
3. Execute the notebook cells sequentially.
4. Launch the Gradio demonstration included in the final section of the notebook.

---

## Future Improvements

Potential future enhancements include:

- Incorporating BM25 as a classical retrieval baseline.
- Fine-tuning transformer models on retrieval tasks.
- Deploying the Gradio application using Hugging Face Spaces.
- Exploring advanced FAISS indexing techniques.
- Scaling to larger datasets and production environments.

---

## Authors

This project was developed as a group academic project on semantic document retrieval and large-scale information retrieval systems.

### Team Members

- Sidda Divya (GitHub: `sidda19`)
- Manemoni Sumanjali
- Ganesh
- Divyam Sahu
