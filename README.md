# DSA4213 Assignment 3 - Emotion Classification

## Overview

This project involves training and evaluating an emotion classification model using HuggingFace Transformers. It uses a fine-tuned model and a LoRA (Low-Rank Adaptation) model for comparison.

## Project Structure

### **Files Description**

- **.gitignore**: Specifies which files and directories should be ignored by Git. This file helps avoid tracking temporary or unnecessary files such as logs and `__pycache__`.

- **Experiments+interactive.ipynb**: Contains the experiments comparing **Full Fine-Tuning (FT)** and **LoRA (Low-Rank Adaptation)** models. Also includes an interactive demo for testing the models with custom input sentences to classify emotions.

- **Finetuning+creating_models.ipynb**: Demonstrates the **fine-tuning process** for a pre-trained model and the creation of **LoRA adapters**. This notebook covers model setup, fine-tuning, and training on an emotion classification task.

- **README.md**: This file. Provides a detailed overview of the project, including how to set up and run the models, along with necessary instructions for downloading and uploading the models to Google Drive, and running the code on Colab.

- **confusion_matrices.png**: Visualizes the **confusion matrices** for the comparison between **Full Fine-Tuning (FT)** and **LoRA** models. It helps illustrate how well each model predicts the emotion categories.

- **data_distribution.png**: Provides a summary of the **data distribution** used in the experiments. It visualizes how the dataset is split and the distribution of emotion labels across the dataset.

- **error_analysis.json**: Contains detailed results of the **error analysis** for both **Full Fine-Tuning (FT)** and **LoRA** models. Includes insights on where each model performed poorly and the types of errors made during classification.

- **main.ipynb**: This is the **entry point** for the project when running it on **Google Colab**. It loads pre-trained models, performs fine-tuning, evaluates models, and provides an interactive section where you can test the models with your own input sentences.

- **ood_evaluation.json**: Stores the evaluation results for the models when tested on **out-of-domain (OOD)** data. This file includes performance metrics for both the **Full Fine-Tuning** and **LoRA** models on data that was not part of the training set.

- **requirements.txt**: Lists the Python dependencies required to run the project, including libraries like `transformers`, `datasets`, `torch`, etc. This ensures all necessary libraries are installed in your environment for smooth execution.

- **results_summary.json**: Provides a **summary of the results** from the fine-tuning experiments, including key performance metrics such as accuracy and F1 score, and compares the performance of the **Full Fine-Tuning** model with the **LoRA** model.


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
