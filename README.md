"# Kiswahili-ASR-WebApp-with-Whisper" 
--- 
## Currently experiencing Issues pushing the related files to github due to a cloud syncing issue. Refer to the linked gamma presentation for details on the project in the mean time

https://gamma.app/docs/Fine-Tuning-Whisper-for-Kiswahili-Speech-Recognition-npuzgrxrnj75roh?mode=doc
---

This repository contains the code, model configurations, and training pipeline for fine-tuning OpenAI's Whisper model for **Kiswahili Automatic Speech Recognition (ASR)**. The goal is to improve transcription accuracy for Kiswahili, a widely spoken but underrepresented language in modern ASR systems.

## 📌 Project Overview

Kiswahili, spoken by over 100 million people across East Africa, suffers from low representation in popular ASR models. To address this, we fine-tuned the [Whisper model](https://openai.com/research/whisper), a state-of-the-art speech-to-text model, using a curated Kiswahili speech corpus. This fine-tuned model is optimized for better performance on regional accents, vocabulary, and phonetics.

### ✅ Key Features

* Fine-tuning using [OpenAI Whisper](https://github.com/openai/whisper)
* Support for Swahili speech data (custom dataset)
* Evaluation metrics for WER (Word Error Rate)
* Scripts for training, inference, and data preprocessing
* Notebook integration for ease of experimentation

## 🛠️ Project Structure

```
├── data/                    # Dataset storage and preprocessing scripts
├── models/                  # Checkpoints and fine-tuned model storage
├── notebooks/               # Jupyter/Colab notebooks for exploration
├── training/                # Training and evaluation scripts
├── utils/                   # Helper functions and utilities
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

## 📁 Dataset

We used a curated Kiswahili speech dataset consisting of transcribed audio recordings from publicly available sources. Audio files were preprocessed (converted to `.wav`, downsampled) and split into train, validation, and test sets.

You can use your own Kiswahili dataset following this structure:

```
dataset/
├── train/
│   ├── audio1.wav
│   └── transcript1.txt
├── val/
└── test/
```

## 🧪 Training Pipeline

1. **Preprocessing**:

   * Normalize audio
   * Tokenize transcripts
2. **Fine-tuning**:

   * Based on OpenAI’s Whisper model
   * Optimized with HuggingFace `transformers` and `datasets`
3. **Evaluation**:

   * Calculates Word Error Rate (WER)
   * Visualizes predictions and confidence



