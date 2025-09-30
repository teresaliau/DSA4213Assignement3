# DSA4213 Assignment 3 - Emotion Classification

## Overview

This project involves training and evaluating an emotion classification model using HuggingFace Transformers. It uses a fine-tuned model and a LoRA (Low-Rank Adaptation) model for comparison.

## Project Structure

### **File Descriptions**

- **.gitignore**: Specifies which files and directories Git should ignore.

- **Experiments+interactive.ipynb**: Explores different texts and compares **Full Fine-Tuning (FT)** vs **LoRA** models with an interactive demo.

- **Finetuning+creating_models.ipynb**: Contains scripts for **fine-tuning** the models and **creating LoRA adapters**, along with evaluation results.

- **README.md**: This file. Provides an overview of the project and instructions for setup and running the code.

- **confusion_matrices.png**: Visualizes the confusion matrices for the **Full Fine-Tuning (FT)** and **LoRA** models.

- **data_distribution.png**: Displays the **data distribution** used in the experiments.

- **error_analysis.json**: Contains error analysis results for **Full FT** and **LoRA** models.

- **main.ipynb**: The **entry point** for running the model, including loading pre-trained models, performing fine-tuning, and testing with custom inputs.

- **ood_evaluation.json**: Stores evaluation results on **out-of-domain (OOD)** data.

- **requirements.txt**: Lists required Python libraries to run the project.

- **results_summary.json**: Provides a summary of the evaluation results for both models.


## Instructions

### Step 1: Download the models

You will need to download the models for both the **Full Fine-Tuned Model** and the **LoRA Adapter** from the link below:

* **Link to folder With models**: [Link](https://drive.google.com/drive/folders/1816wQI74aatPBEL_OIk4FQhVvZtPRG39?usp=sharing)

**Link to Individual models**
* **Full Fine-Tuned Model**: [Link](https://drive.google.com/drive/folders/1exOmAGt4iIYT3tBniyPrJHAzLbUnJLKy?usp=sharing)
* **LoRA Adapter**: [Link](https://drive.google.com/drive/folders/1G0PzrUMzjJ4ZNlyt_h_4X5t6X8fY0BK-?usp=sharing)

### Step 2: Upload to Google Drive

Once you have downloaded the models, upload the model folders (`model_full_finetuned` and `model_lora_adapter`) to your Google Drive. For simplicity, we recommend uploading them to the `MyDrive` directory of your Google Drive.

### Step 3: Mount Google Drive in Colab

Open the notebook in Google Colab and mount your Google Drive to access the model files. The following code is already included in main.ipynb script

```python
from google.colab import drive
drive.mount('/content/drive')
```

### Step 4: Set the correct model paths

After mounting your Google Drive, the notebook will automatically load the models from your Drive. If you've uploaded the models to `MyDrive`, the paths will look like this:

```python
# Define model paths in your Google Drive
model_full_path = '/content/drive/MyDrive/model_full_finetuned'
model_lora_path = '/content/drive/MyDrive/model_lora_adapter'
```
If your models are saved elsewhere, change the paths accordingly
Ensure that these paths reflect where you uploaded the model folders.

### Step 5: Run the Notebook

Once the models are mounted correctly, you can run the notebook. The notebook will load the models from your Google Drive and start running the emotion classification tasks.

### Step 6: INteract with the models
You can input your own sentences in the last section of the notebook. Press Enter within the bar for it to stop running.
