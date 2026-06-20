# Multilingual Health Question Answering in Low-Resource African Languages

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Muen1/multilingual-health-qa-africa/blob/main/notebooks/03_finetuning.ipynb)

## Overview
Fine-tuning multilingual large language models to answer maternal and reproductive
health questions in low-resource African languages (Akan, Amharic, Luganda, Swahili,
and English) for the Zindi competition.

## Repository Structure
```text
multilingual-health-qa-africa/

├── notebooks/

│   ├── 01_EDA.ipynb              # Exploratory data analysis

│   ├── 02_preprocessing.ipynb   # Data cleaning and prompt construction

│   ├── 03_finetuning.ipynb      # Model fine-tuning with LoRA/PEFT

│   ├── 04_inference.ipynb       # Generate predictions on test set

│   ├── 05_submission.ipynb      # Build and validate submission CSV

│   └── 06_evaluation.ipynb      # Experiment comparison and visualization

├── data/                         # Data files (stored in Google Drive)

├── submissions/                  # Submission screenshots

├── plots/                        # Charts and learning curves

├── requirements.txt

└── README.md
```

## Setup Instructions

### Google Colab (recommended)
1. Click the badge above to open the fine-tuning notebook
2. When prompted, mount your Google Drive
3. Ensure your data files are in `My Drive/multilingual_health_qa/data/`
4. Run all cells top to bottom

### Local Setup
```bash
git clone https://github.com/YOUR_USERNAME/multilingual-health-qa-africa.git
cd multilingual-health-qa-africa
pip install -r requirements.txt
```

## Experiments Summary

| # | Model | Key Change | ROUGE-1 | ROUGE-L | Zindi Score |
|---|-------|-----------|---------|---------|-------------|
| 1 | mt5-small | Zero-shot baseline | — | — | — |
| 2 | mt5-small | Fine-tuned, LR=3e-4 | — | — | — |
| 3 | flan-t5-base | LoRA r=16 | — | — | — |
| 4 | flan-t5-base | LoRA r=32 | — | — | — |
| 5 | flan-t5-base | Improved prompt | — | — | — |
| 6 | flan-t5-large | LoRA r=16 | — | — | — |

(Fill in scores as experiments are completed)

## Evaluation Metrics
- ROUGE-1 F1
- ROUGE-L F1  
- LLM-as-a-Judge (Zindi leaderboard)


