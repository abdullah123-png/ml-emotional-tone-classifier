# ml-emotional-tone-classifier
This repository contains an AI model that classifies short text (3–25 words) into seven tones: joy, sadness, anger, love, fear, surprise, and neutral. The neural network uses an input layer the size of the input text's word count, three hidden layers having 16 neurons each and a 7-neuron output layer.

## Overview
This project explores how self-attention can be used to detect emotional tone in text.  
The model extracts Query, Key, and Value matrices from DistilBERT and applies a simplified attention mechanism I implemented in Python.

---

## Model Design
- **Architecture:** Custom self-attention neural network
- **Base Model:** DistilBERT (For the Query, Key and Value matrices of the self-attention mechanism)
- **Language:** Python
- **Frameworks:** PyTorch, Transformers, NumPy, Pandas, JSON, pickle, PySimpleGUIQt
- **Input Length:** 3–25 words

---

## How It Works - A very brief overview
1. Text is processed into a list where every word and piece of punctuation is seperated
2. Each word and piece of punctuation's vector embedding is searched for in a .npy file
3. Self attention is applied to the embeddings  
4. The updated embeddings are put through the neural network where an emotionak tone is outputted

---

## Dataset
I trained and validated on an emotion-labelled text dataset ().  
Each sample is labelled with tones like **joy, sadness, anger, fear, love, suprise or neutral**.

---

## Training
Training was done through manual backpropagation code and cross-entropy loss.  
Hyperparameters and evaluation metrics are tracked to measure accuracy and loss across epochs.

---

## Results
- Training Accuracy: 40%
- Example prediction:  
  > “It was a stormy and gloomy night and I was very sad.” → sadness (96.073% confidence)

---

## Purpose
Developed as a passion project of mine.  
Goal: To understand how machine learning can capture emotional tone in natural language and to implement my own attention-based model from scratch.

---

## 🛠️ Installation
```bash
git clone https://github.com/YourUsername/ml-tone-classifier.git
cd ml-tone-classifier
pip install -r requirements.txt
python main.py
