# DSA4213 Assignment 3 - Emotion Classification

## Overview

This project involves training and evaluating an emotion classification model using HuggingFace Transformers. It uses a fine-tuned model and a LoRA (Low-Rank Adaptation) model for comparison.

## Instructions

### Step 1: Download the models

You will need to download the models for both the **Full Fine-Tuned Model** and the **LoRA Adapter** from the links below:

* **Full Fine-Tuned Model**: [Download Link](https://drive.google.com/drive/folders/1exOmAGt4iIYT3tBniyPrJHAzLbUnJLKy?usp=sharing)
* **LoRA Adapter**: [Download Link](https://drive.google.com/drive/folders/1G0PzrUMzjJ4ZNlyt_h_4X5t6X8fY0BK-?usp=sharing)

### Step 2: Upload to Google Drive

Once you have downloaded the models, upload the model folders (`model_full_finetuned` and `model_lora_adapter`) to your Google Drive. For simplicity, we recommend uploading them to the `MyDrive` directory of your Google Drive.

### Step 3: Mount Google Drive in Colab

Open the notebook in Google Colab and mount your Google Drive to access the model files. To do this, add the following code at the beginning of the notebook:

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

Ensure that these paths reflect where you uploaded the model folders.

### Step 5: Run the Notebook

Once the models are mounted correctly, you can run the notebook. The notebook will load the models from your Google Drive and start running the emotion classification tasks.



Let me know if you'd like to refine this further!
