# Hindi News Classifier using BERT

A Natural Language Processing project that fine-tunes the `bert-base-multilingual-cased` model for a sequence classification task: categorizing Hindi news headlines into six predefined labels.

## 📌 Project Overview

This project fine-tunes a pre-trained multilingual BERT model to classify short Hindi news titles into six categories:

- Crime
- Sports
- Health
- Entertainment
- Education & Career
- India & World

## 🧠 Model Details

- **Model Type:** Sequence Classification
- **Base Model:** [`bert-base-multilingual-cased`](https://huggingface.co/bert-base-multilingual-cased)
- **Fine-tuning:** The model was fine-tuned for 3 epochs using Hugging Face's `Trainer` API with:
  - Learning Rate: 2e-5
  - Batch Size: 16 (train), 32 (eval)
  - Optimizer: AdamW
  - Metric: Accuracy
- **Dataset Size:** 8,731 Hindi news titles
- **Validation Accuracy:** **84.8%**
- **Weighted F1 Score:** **0.8489**

## 🗂 Dataset

Custom dataset created using Python web scraping (`requests`, `BeautifulSoup`). Contains Hindi news headlines labeled in English.

## 📁 Files

- `WebScraping.ipynb` – Scrapes Hindi news headlines from BBC Hindi and News18; generates the dataset
- `HindiNewsClassifier.ipynb`: Fine-tunes a multilingual BERT model on the scraped dataset for classification
- `hindi_news_dataset.csv`: Preprocessed dataset
- `test_news_titles.csv` – Sample unseen Hindi headlines used for inference/testing
- `confusion_matrix.png`: Model evaluation visualization

## 📊 Results

- Accuracy: **84.8%**
- Weighted F1 Score: **0.8489**
- Evaluated using scikit-learn metrics and a confusion matrix.

## 📚 Tech Stack

- Python
- Hugging Face Transformers
- PyTorch
- scikit-learn
- matplotlib
- BeautifulSoup (for scraping)
