# multilingual-health-qa-africa

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/multilingual-health-qa-africa/blob/main/notebooks/03_finetuning.ipynb)

## Overview
This project fine-tunes multilingual LLMs to answer maternal and reproductive health questions in Akan, Amharic, Luganda, Swahili, and English for the Zindi competition.

## Project Structure
- `notebooks/01_EDA.ipynb` — Exploratory Data Analysis
- `notebooks/02_preprocessing.ipynb` — Data preprocessing pipeline
- `notebooks/03_finetuning.ipynb` — Model fine-tuning with PEFT/LoRA
- `notebooks/04_inference.ipynb` — Inference and answer generation
- `notebooks/05_submission.ipynb` — Submission file generation

## Setup Instructions

### On Google Colab
1. Open the Colab badge link above
2. Upload your Zindi data files (`Train.csv`, `Val.csv`, `Test.csv`) to the Colab session
3. Run all cells in order

### Local Setup
```bash
git clone https://github.com/YOUR_USERNAME/multilingual-health-qa-africa.git
cd multilingual-health-qa-africa
pip install -r requirements.txt
```

## Models Experimented
- google/mt5-small → mt5-base → mt5-large
- facebook/mbart-large-50
- google/flan-t5-base → flan-t5-large
- microsoft/mdeberta-v3-base (encoder experiments)

## Evaluation Metrics
- ROUGE-1 F1
- ROUGE-L F1
- LLM-as-a-Judge

## Results Summary
| Experiment | Model | ROUGE-1 | ROUGE-L | Notes |
|---|---|---|---|---|
| Baseline | mt5-small | TBD | TBD | No fine-tuning |
| Exp 2 | mt5-base | TBD | TBD | Fine-tuned 3 epochs |
| ... | ... | ... | ... | ... |

## Leaderboard Progression
Screenshots in `/submissions/` folder.

## Ethical Considerations
See report section 8 for full discussion of bias, misinformation risks, and responsible deployment.