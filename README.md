# Named Entity Recognition with BERT and T5
This repository contains code and evaluation scripts for a project comparing two pre-trained
language models—**BERT** (token classifier) and **T5** (text-to-text generator)—on a span-labelled
Named Entity Recognition (NER) task.

## Datasets
* **English-EWT** (in-domain)
* **English-PUD** (out-of-domain)

## Project Overview
The goal of this project is to evaluate the performance of BERT (token classifier) and T5 (text-to-text generator) on a span-labeling NER task using:
(1) In-domain dataset: English-EWT;
(2) Out-of-domain dataset: English-PUD

Two tagset formats are evaluated:
(1) Full BIO tags (e.g., B-PER, I-LOC)
(2) Simplified B/I/O tags (e.g., B, I, O)

Performance is assessed using:
(1) Token-level F1 (macro-average)
(2) Span-level labelled and unlabelled matching scores

## How to Reproduce Results

1. Install Dependencies
Install all required packages using pip:

2. Run the Notebook
Launch the notebook in Google Colab (recommended) or locally in Jupyter Notebook. Run all cells in sequence to:
(1) Preprocess datasets (auto-downloads)
(2) Train BERT and T5
(3) Evaluate models under both tagset formats
(4) Produce results tables, span metrics, and qualitative examples

3. Random Seeds and Reproducibility
Random seeds are fixed for:
(1) Python random
(2) NumPy
(3) PyTorch
This ensures consistent results across runs.

## Evaluation Metrics
The notebook reports:
(1) Macro F1 scores (token-level) for both full and simplified tags
(2) Labelled/unlabelled span match scores
(3) Qualitative examples showing prediction vs. gold tags
(4) Table and bar plot comparison of model performance

## References
Devlin, J. et al. (2019). BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding.
Raffel, C. et al. (2020). Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer.
Hugging Face Transformers Documentation
UniversalNER Dataset

