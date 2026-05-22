# MLPs and ConvNets for CIFAR-10 Image Classification

## Overview

This project explores the design, training, and evaluation of Multi-Layer Perceptrons (MLPs) and Convolutional Neural Networks (ConvNets) for image classification on the CIFAR-10 dataset.

The goal is to investigate the strengths and limitations of different neural network architectures, evaluate techniques for improving generalization, and study the impact of data corruption and label noise on model performance.

## Dataset

The project uses the CIFAR-10 dataset, which contains:

- 60,000 color images
- Image size: 32 × 32 pixels
- 10 object categories:
  - Airplane
  - Automobile
  - Bird
  - Cat
  - Deer
  - Dog
  - Frog
  - Horse
  - Ship
  - Truck

## Project Components

### 1. Custom Optimizer Implementation

A custom optimizer framework was implemented to better understand the parameter update process used in neural network training.

### 2. Multi-Layer Perceptrons (MLPs)

A baseline MLP architecture was developed and trained on CIFAR-10.

Experiments included:

- Network depth and width exploration
- Regularization techniques
- Dropout
- Weight decay
- Normalization methods
- Performance comparison across multiple random seeds

### 3. Convolutional Neural Networks (ConvNets)

A LeNet-inspired convolutional neural network was implemented and optimized for image classification.

Experiments focused on:

- Convolutional feature extraction
- Pooling operations
- Architectural improvements
- Regularization strategies
- Performance comparison against MLPs

### 4. Investigating MLP Limitations

To analyze whether MLPs exploit the spatial structure of images, two pixel-shuffling experiments were conducted:

- Fixed pixel permutation throughout training
- Random pixel permutation at every iteration

These experiments demonstrate the importance of spatial locality in image recognition tasks.

### 5. Robustness to Label Noise

The project further investigates model behavior under corrupted datasets by:

- Randomly shuffling ground-truth labels
- Training MLPs on noisy datasets
- Training ConvNets on noisy datasets
- Comparing learning dynamics and overfitting behavior

## Key Findings

- ConvNets significantly outperform MLPs on image classification tasks due to their ability to exploit local spatial patterns.
- Regularization and data augmentation improve model generalization.
- MLP performance degrades substantially when image structure is disrupted.
- Both MLPs and ConvNets can eventually fit noisy labels, highlighting the risk of memorization in deep learning models.
- Convolutional architectures are substantially more robust and data-efficient than fully connected networks for visual recognition tasks.
