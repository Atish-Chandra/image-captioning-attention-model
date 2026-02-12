# image-captioning-attention-model
Encoder–decoder image captioning model with attention mechanism (InceptionV3 + LSTM/GRU) for assistive audio generation.


# Descriptive Audio Model of Images for Blind

## Overview

This project develops an end-to-end deep learning system that converts images into descriptive natural language captions, which can then be transformed into speech for accessibility applications.

The goal is to assist visually impaired individuals by generating contextually relevant textual descriptions of visual content using an encoder–decoder neural architecture enhanced with an attention mechanism.

---

## Problem Statement

Visual content dominates modern digital interaction, yet remains inaccessible to visually impaired individuals without assistive systems.

The objective of this project is to design and implement a deep learning framework capable of:

1. Extracting high-level semantic features from images
2. Generating coherent natural language descriptions
3. Supporting conversion of generated text into speech
4. Operating within a scalable encoder–decoder architecture

The system must:

- Handle large-scale image–caption datasets
- Learn alignment between visual features and language tokens
- Generate sequential text predictions
- Optimize contextual accuracy during decoding
- Provide computational efficiency during inference

---

## Technical Requirements

The modeling pipeline includes:

### 1. Data Preprocessing
- Caption tokenization using Keras Tokenizer
- Vocabulary indexing (word-to-index and index-to-word mappings)
- Sequence padding
- Image resizing and normalization for InceptionV3
- Dataset splitting into training and validation sets

### 2. Feature Extraction (Encoder)
- Pretrained InceptionV3 (ImageNet weights)
- Extraction of convolutional feature maps
- Dense projection into embedding space
- Dropout for regularization

### 3. Attention Mechanism
- Soft attention layer
- Context vector computation
- Alignment scoring between image features and decoder hidden states

### 4. Decoder Architecture
- Embedding layer
- GRU/LSTM recurrent unit
- Dense transformation layers
- Softmax output layer over vocabulary

### 5. Caption Generation Strategies
- Greedy Search decoding
- Beam Search decoding
- Sequence termination via end-token prediction

### 6. Evaluation
- Train/test split validation
- Caption quality comparison
- Baseline comparison with prior image-captioning architectures

---

## Model Architecture

The system follows a CNN–RNN encoder–decoder framework:

Image → InceptionV3 Encoder → Attention Mechanism → RNN Decoder → Caption Tokens → Text-to-Speech

The attention mechanism allows the decoder to focus dynamically on relevant spatial regions of the image during each timestep of caption generation.

---

## Deliverables

- `ML_Project_Final_Final.ipynb`  
  Full implementation including preprocessing, model architecture, training, and caption generation.

- `Descriptive_Audio_Model_of_Images_for_Blind.pdf` :contentReference[oaicite:2]{index=2}  
  Structured academic-style report detailing methodology, related work, architecture, and future improvements.

---

## Key Contributions

- Implementation of attention-based image captioning
- Integration of pretrained CNN feature extraction
- Sequential language modeling using recurrent networks
- Caption-to-audio transformation capability
- Accessibility-driven AI application

---

## Assumptions

- Captions are sufficiently descriptive for supervised learning.
- Image features extracted via pretrained CNN generalize well to dataset.
- Tokenization and vocabulary restriction balance expressiveness and computational efficiency.

---

## Author

Atish Chandra  
M.S. Computer Science  
Machine Learning | Computer Vision | NLP
