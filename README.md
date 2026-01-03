# Deep Learning–Based Medical Diagnoser using LSTM

## Project Overview
This project presents a **Deep Learning–based medical diagnosis system** that predicts a **disease category** and suggests a **medication** based on patient-reported symptoms written in natural language. The model uses **Natural Language Processing (NLP)** techniques along with a **Long Short-Term Memory (LSTM)** neural network to understand symptom patterns and generate predictions.

The project demonstrates how AI and deep learning can assist in healthcare by providing faster, data-driven insights from textual medical data.

---

## Problem Statement
Patients usually describe their symptoms in text form, such as:
> *"I feel tired all the time and have low energy."*

Traditional systems struggle to understand the **context and sequence** of such descriptions. This project aims to solve that problem using an LSTM-based model that can:
- Analyze symptom sequences
- Learn contextual patterns
- Predict the disease category
- Recommend suitable medication

---

## Why LSTM?
Medical symptom descriptions are **sequential text data**, where word order matters.

**LSTM (Long Short-Term Memory)** networks are ideal because they:
- Capture long-term dependencies in text
- Retain important contextual information
- Perform well for NLP-based classification tasks

---

## 🧠 Key Design Decision
The original dataset contained **178 unique diseases**, many with very few samples. This caused severe **class imbalance**, leading to incorrect predictions.

### Solution Implemented
- Diseases were grouped into **broader disease categories**
- Reduced output complexity
- Enabled the LSTM model to learn meaningful patterns
- Improved prediction stability and accuracy

This approach reflects **real-world healthcare AI systems**.

---

## Dataset Description
The dataset consists of:
- **Patient_Problem** – Textual description of symptoms
- **Disease Category** – High-level medical category
- **Prescription** – Recommended medication or treatment

---

## Technology Stack
- **Language**: Python  
- **Deep Learning Framework**: TensorFlow / Keras  
- **Model**: LSTM (Recurrent Neural Network)  
- **NLP Techniques**: Tokenization, Padding  
- **Libraries**:
  - NumPy
  - Pandas
  - Scikit-learn
  - TensorFlow / Keras

---

## Model Architecture
1. Input Layer – Padded tokenized text  
2. Embedding Layer – Converts words to dense vectors  
3. LSTM Layer – Learns symptom sequences  
4. Dense Layers:
   - Disease Category Prediction (Softmax)
   - Prescription Prediction (Softmax)

---

## Workflow
1. Text preprocessing and tokenization  
2. Padding sequences to uniform length  
3. Encoding disease categories and prescriptions  
4. Training the LSTM model  
5. Predicting outputs for new symptom inputs  
