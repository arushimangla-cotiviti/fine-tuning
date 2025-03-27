# Fine Tuning
This repository fine-tunes a pre-trained LLaMA 3.2 model (3B/1B Instruct) to classify text data. The dataset consists of multiple columns, with raw_field and raw_desc as input features, and gdf_field as the target label. The goal is to train a model to predict the gdf_field based on the combination of raw_field and raw_desc.

# Requirements
## Before running the code, you need to install the required libraries:

!pip install transformers datasets torch scikit-learn pandas

# Steps to Run

1. Prepare your dataset: Place your dataset in a CSV format and update the code to read the dataset (you can adjust the data loading part if necessary).

## Preprocessing:

The script handles missing values in raw_desc by filling them with empty strings.
It combines raw_field and raw_desc to form the final input text.

## Model Training:

The script uses LLaMA 3.2 3B/1B Instruct as the pre-trained model and fine-tunes it for your classification task.

The model is trained for several epochs based on the dataset size and hyperparameters you specify.
The fine-tuned model is saved to the ./results directory after training.

## Evaluation:

After training, the model is evaluated on the test set, and the classification results are printed.
