# PolloSoft – Knowledge Management System

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ethereallekin/pollosoft-knowledge-management/blob/main/PolloSoft_KM_Prototype.ipynb)

Team project for the **Knowledge Management** course at **TECMILENIO**.

We designed a knowledge management system for **PolloSoft**, a fictional iOS app studio from Monterrey that builds native apps with Swift and SwiftUI, runs automated QA tests, sells subscriptions with StoreKit 2 and grows its apps with social media marketing.

## What is in this repository

| File | Description |
|---|---|
| `PolloSoft_KM_Prototype.ipynb` | Google Colab notebook with the prototype (dataset, classifier, semantic search and ontology) |
| `docs/PolloSoft_KM_Project_Progress.pdf` | Project progress report |
| `requirements.txt` | Libraries needed to run the notebook outside Colab |

## The prototype

1. **Dataset** – 48 short mock documents from PolloSoft, 8 for each category: Technical Guide, Deployment SOP, Bug Report, Analytics Report, Marketing Plan and Policy.
2. **Automatic classification** – the documents are converted to vectors with TF-IDF and classified with Naive Bayes and Logistic Regression.
3. **Semantic search** – a question in natural language is compared with every document using cosine similarity, and the most similar documents are shown first.
4. **Ontology** – a concept map of PolloSoft's document types and concepts, drawn with networkx.

### Results

| Model | Test accuracy | Cross-validation accuracy |
|---|---|---|
| Naive Bayes | 0.833 | 0.707 |
| **Logistic Regression** | **0.917** | **0.787** |

Logistic Regression classified correctly 11 of 12 test documents and 6 of 6 new documents. The semantic search returned the correct document in first place for all four example questions.

## How to run it

**Google Colab:** click the *Open in Colab* button above and select `Runtime → Run all`.

**Locally:**

```bash
pip install -r requirements.txt
jupyter notebook PolloSoft_KM_Prototype.ipynb
```

## Team

- Daniela Alejandra Escamilla Alanis
- Leonardo Alonso González del Ángel
- Dana Elena Zertuche Castro

Teacher: Alfredo Paul Aguirre Torres
