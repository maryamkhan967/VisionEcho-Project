# VisionEcho: Image-to-Speech Converter for Visually Impaired Individuals 🖼️🔊

## 🧠 Overview

**VisionEcho** is an assistive AI system designed to empower visually impaired individuals by converting visual content into spoken descriptions. This project integrates deep learning, computer vision, and natural language processing to generate accurate captions for images and convert them into audio output. It enhances digital accessibility and fosters greater independence for the visually impaired.


## ✨ Key Features

- **Image-to-Caption Generation**  
  Automatically generates descriptive captions for input images using a CNN-RNN model inspired by the *Show, Attend, and Tell* architecture.

- **Caption-to-Speech Synthesis**  
  Transforms generated captions into natural audio using Google Text-to-Speech (gTTS), making visual content accessible through sound.

- **Attention Mechanism**  
  Employs attention layers to dynamically focus on the most relevant parts of an image during caption generation for improved accuracy.

- **BLEU Score Evaluation**  
  Assesses the quality of the generated captions against ground truth annotations.

- **Visualization Tools**  
  Displays attention maps to show which parts of the image the model focuses on while generating each word in the caption.


## 🏗️ Model Architecture

- **Encoder**: InceptionV3 (pre-trained CNN) extracts image features.
- **Decoder**: GRU-based RNN generates captions word-by-word.
- **Attention**: Helps the decoder focus on relevant image regions.
- **TTS**: Google Text-to-Speech API converts captions to speech.


## 🛠️ Model Training

1. **Dataset**  
   Download and extract the Flickr8k dataset from:  
   [https://www.kaggle.com/adityajn105/flickr8k](https://www.kaggle.com/adityajn105/flickr8k)

2. **Training Script**  
   Use the `VisionEcho.ipynb` notebook to train the model. It will:
   - Load and preprocess the dataset.
   - Tokenize captions.
   - Extract image features using InceptionV3.
   - Train the CNN-RNN model with attention.
   - Save checkpoints during training.
