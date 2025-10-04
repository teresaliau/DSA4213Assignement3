# DSA4213 Assignment 3 - Emotion Classification

## Overview

This project involves training and evaluating an emotion classification model using HuggingFace Transformers. It uses a fine-tuned model and a LoRA (Low-Rank Adaptation) model for comparison.

## Project Structure



```
DSA4213Assignement3/
├── main.py                   # Main entry point - run this script
├── .gitignore                # Specifies which files and directories Git should ignore.
├── Experiments+interactive.ipynb  # Explores different texts and compares Full Fine-Tuning (FT) vs LoRA models with an interactive demo.
├── Finetuning+creating_models.ipynb  # Contains scripts for fine-tuning the models and creating LoRA adapters, along with creating the other files in this repo (evaluation results).
├── README.md                 # This file. Provides an overview of the project and instructions for setup and running the code.
├── confusion_matrices.png    # Visualizes the confusion matrices for the Full Fine-Tuning (FT) and LoRA models.
├── data_distribution.png     # Displays the data distribution of the dataset.
├── error_analysis.json       # Contains error analysis results for Full FT and LoRA models.
├── main.ipynb                # The entry point for running the model, including loading pre-trained models, performing fine-tuning, and testing with custom inputs.
├── ood_evaluation.json       # Stores evaluation results on Go-emotion (Reddit) data.
├── requirements.txt          # Lists the Python libraries and versions that were used to run the results.
└── results_summary.json      # Provides a summary of the evaluation results for both models.
```


## Quick Start

### 1. Install Dependencies
```bash
git clone https://github.com/teresaliau/DSA4213Assignement3.git
cd DSA4213Assignement3
python -m venv venv
#or python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 2. Download Models
Download the pre-trained models from [Google Drive](https://drive.google.com/drive/folders/1816wQI74aatPBEL_OIk4FQhVvZtPRG39?usp=sharing) and unzip them, then place them in your project directory.

**Individual model links:**
- [Full Fine-Tuned Model](https://drive.google.com/drive/folders/17vyWvUEaaRNV-VS1ExNclcYASXwNhGXp?usp=sharing)
- [LoRA Adapter](https://drive.google.com/drive/folders/1Fef-FreqWlStGqCVvK-3M6jCVC08eUA0?usp=sharing)
```bash
!ls
```
This should print

confusion_matrices.png		

model_full_finetuned

data_distribution.png		

model_lora_adapter

error_analysis.json			

ood_evaluation.json

Experiments+interactve.ipynb		

README.md

Finetuning+creating_models.ipynb	

requirements.txt

main.ipynb				

results_summary.json

main.py			

venv

### 3. Upload Run the Code

**Option 1: Python Script (Recommended)**
Upload the models into the local repo. Running:
```bash
!ls
```
You should see **Full Fine-Tuned Model** and **LoRA Adapter**

```bash
python main.py
# or python3 main.py for Apple
```

**Option 2: Jupyter Notebook (If main.py doesn't work)**

*For Google Colab:*
1. Upload `main.ipynb` to Colab
2. Mount Google Drive and upload models there (in 'MyDrive'
3. Update model paths:
   ```python
   model_full_path = '/content/drive/MyDrive/model_full_finetuned'
   model_lora_path = '/content/drive/MyDrive/model_lora_adapter'
   ```
Point to tight path accordingly
4. Run all cells

*For local Jupyter:*
```bash
jupyter notebook main.ipynb
```

### 4. Interactive Demos

Enter your own input sentences. If you want the py to stop running, press Enter without entering any characters.

## Potential Issues

**CUDA errors on Mac:**
- Code automatically uses MPS (Apple Silicon) or CPU
- For GPU access, use Google Colab with GPU runtime


**If main.py still doesn't work:**
Use `main.ipynb` in Google Colab instead!

