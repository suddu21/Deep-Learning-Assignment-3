# Deep Learning Assignment 3 - Transliteration Model - Sudhanva Satish DA24M023


This repository contains the implementation of a sequence-to-sequence (Seq2Seq) model for transliteration between Latin script and Indian scripts (Hindi) using the Google Dakshina dataset.
It has been done as part of DA6401 Assignment 3

## Project Overview

The project implements an Encoder-Decoder architecture for transliteration tasks, specifically focusing on:
- Hindi (Latin to Devanagari)

The model uses various RNN architectures (SimpleRNN, LSTM, GRU) with attention mechanisms to improve translation accuracy.

## Dataset

The project uses the Dakshina dataset, which contains parallel corpora for Indian language transliteration. The dataset is organized as follows:
- Training data: `hi.translit.sampled.train.tsv` (Hindi)
- Validation data: `hi.translit.sampled.dev.tsv` (Hindi)

## Project Structure

```
.
├── DA24M023_DL_A3.ipynb          # Main notebook containing the implementation
├── models/                        # Directory containing saved model weights
├── predictions_attention/         # Predictions from attention-based models
├── predictions_vanilla/          # Predictions from vanilla models
├── dakshina_dataset_v1.0/        # Dataset directory
└── wandb/                        # Weights & Biases logging directory
```

## Features

- Character-level tokenization for handling Indian scripts
- Multiple RNN architectures (SimpleRNN, LSTM)
- Attention mechanism implementation
- Model training with Weights & Biases integration
- Comprehensive evaluation metrics
- Support for both Hindi and Kannada transliteration

## Usage

1. Clone the repository
2. Install the required dependencies
3. Download the Dakshina dataset
4. Open and run the Jupyter notebook `DA24M023_DL_A3.ipynb`
5. Each question specific code snippet is marked inside the notebook

## Model Architecture

The model uses a sequence-to-sequence architecture with:
- Encoder: Multiple RNN layers (configurable)
- Decoder: Multiple RNN layers with attention mechanism
- Embedding layer for character representation
- Dense output layer with softmax activation

## Results

The model's performance can be tracked using Weights & Biases, which provides:
- Training and validation loss curves
- Accuracy metrics
- Model checkpoints
- Prediction samples