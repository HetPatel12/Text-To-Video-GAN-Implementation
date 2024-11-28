# Text-to-Video GAN Implementation

This project implements a **Generative Adversarial Network (GAN)** to dynamically generate videos from natural language text prompts. It demonstrates the use of deep learning techniques to synthesize video frames based on descriptive inputs, offering a step towards automated video generation.

## Overview

- **Problem Statement**: Manual video creation is time-consuming and demands significant effort. This project addresses this gap by automating the process using GANs.
- **Goal**: To develop a GAN model capable of generating realistic videos from text prompts.
- **Applications**: Media creation, gaming, animation, and content generation.

## Features

- Generate videos based on text descriptions (e.g., "circle moving diagonally up-right").
- Frame-by-frame continuity ensures smooth motion synthesis.
- Lightweight GAN architecture optimized for computational efficiency.

## Dataset

- **Generation**: 
  - 30,000 videos generated programmatically.
  - Each video comprises 10 frames.
  - Resolutions: 64x64 pixels per frame.
  - Examples: "circle bouncing vertically," "circle moving left."
- **Preprocessing**:
  - Normalize image frames for GAN input.
  - Encode text prompts using a vocabulary-based embedding.

## Architecture

### Generator
- Combines text embeddings with random noise.
- Upscales features to synthesize 64x64 RGB video frames.

### Discriminator
- Classifies frames as real or generated.
- Uses convolutional layers for feature extraction.

### Text Embedding
- Encodes text prompts into numerical vectors using embedding layers.

## Training

- **Adversarial Setup**:
  - The generator attempts to create convincing frames.
  - The discriminator learns to differentiate between real and generated frames.
- **Parameters**:
  - Batch size: 16
  - Loss: Binary Cross-Entropy
  - Optimizer: Adam (learning rate: 0.0002)
  - Epochs: 13
- **Platform**: Designed for efficiency on T4 GPUs. Training on CPUs is slower but possible.

## Results

- Example Prompt: "Circle moving up-right."
- Output: Videos generated frame-by-frame, showcasing realistic motions.

## Future Work

- **Enhanced Dataset**: Include varied motions, shapes, and interactions for improved generalization.
- **Higher Resolutions**: Generate videos at resolutions of 128x128 or higher.
- **Advanced Text Embeddings**: Integrate models like BERT or GPT for richer text understanding.
- **Complex Scenes**: Expand capabilities for multi-object and interactive video generation.

## Getting Started

1. **Prerequisites**:
   - Python
   - PyTorch
   - OpenCV
2. **Dataset Generation**:
   - Run the provided script to generate synthetic training data.
3. **Training**:
   - Train the GAN model using the scripts in this repository.
4. **Video Generation**:
   - Use the trained model to generate videos based on new text prompts.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Text-to-Video-GAN.git
2. cd Text-to-Video-GAN
