# VisionEcho: Image-to-Speech Converter for Visually Impaired Individuals 🖼️🔊

## 🧠 Overview

**VisionEcho** project is a smart system that helps blind and visually impaired people understand what is shown in an image. It does this in two main steps: first, it looks at a picture and creates a sentence describing what’s happening (like “a man is riding a bike on the street”). Then, it reads that sentence out loud using a voice tool. This means someone who can’t see the image can still know what’s in it just by listening.

We use a special deep learning model to do this. It includes a CNN (InceptionV3) to see and understand the image, and an RNN (GRU) to write a caption about the image. We also use an attention mechanism so the model knows which part of the image to focus on when writing each word. Finally, we use a Text-to-Speech (TTS) tool to speak the caption.

This project was built using Python with TensorFlow and other helpful libraries like NumPy, Pandas, and gTTS. The data used for training came from the Flickr8k dataset, which includes thousands of images and their descriptions. The final goal of this project is to make visual information more accessible for people who cannot see.


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
