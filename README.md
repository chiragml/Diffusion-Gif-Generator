# Diffusion GiF Generator

> **Input Image**
<p align="center">  
  <img src="chester.jpg" width="30%" />
</p>
<p>
  <strong>Prompt:</strong>
  ["A man singing with a crowd in the background",
              "The man turns to the crowd",
              "A stage shows up and reveals a concert happening."]
</p>


> **Output Comparison**

<p align="center">
  <strong>Initial Model (40 min)</strong>  
  <img src="out%20(2).gif" alt="Initial Model Output - 40 min" width="30%" />
  <strong>Optimized Model (9 min)</strong>
  <img src="out3.gif" alt="Optimized Model Output - 9 min" width="30%" />
</p>

## Overview

This project transforms an image and text prompt into a video GIF using a Stable Diffusion model optimized for performance and efficiency. Through extensive optimizations, the model's processing time has been reduced from 40 minutes to 9 minutes per GIF generation. The training was dome on T4 GPU on Google Colab. 

## Features

- **Input**: An image and a text prompt.
- **Output**: A high-quality, animated GIF.

## Optimizations Implemented

The following optimizations significantly reduced the model's runtime while maintaining output quality:

- **Model CPU Offload**: Offloads model layers to the CPU to balance memory usage between CPU and GPU.
- **Memory Optimization**: Enhances memory management for smoother processing.
- **Attention Optimization**: Streamlines attention layers to improve computational efficiency.
- **Model Pruning** (Pruned 30%): Reduces model size without sacrificing performance.
  - **Analyze Sensitivity**: Identifies the sensitivity of different layers to pruning for targeted optimization.
  - **Adaptive Pruning**: Dynamically adjusts pruning intensity based on model sensitivity analysis.

- **Hyperparameter Tuning**: Fine-tunes model parameters to balance quality and speed.

## Usage

1. **Input Preparation**: Provide an initial image and a descriptive prompt.
2. **Run the Model**: Execute the script to generate the animated GIF.
3. **View Output**: Compare processing times and performance in the generated GIF.

## Setup

To run this project, ensure you have the required dependencies installed. You may also want to clone the repository and configure your environment for optimal model performance.
Make sure you have GPU in the system that you're using. 

## Future Scope of work

The project will be experimenting with different pruning techniques like iterative_pruning, magnitude_pruning etc and also more optimizations using cuda programming. 
Target for this project is to get the generation time under one minute and increase the generation quality to reduce the looping speed. 