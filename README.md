# Arabic Letters Classification

This project is part of the Intelligent Systems course assignment. The goal is to classify Arabic letters using machine learning and deep learning techniques. The dataset consists of 65 different Arabic alphabets, 10 Arabic words, and 3 paragraphs, collected from 82 users.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Results](#results)
- 
## Overview
The project involves training a Convolutional Neural Network (CNN) to classify Arabic letters. The dataset contains variations of each letter (beginning, middle, end, and regular forms), as well as words and paragraphs.

## Dataset
The dataset consists of:
- **53,199 alphabet images** (65 classes).
- **8,144 word images**.
- **241 paragraph images**.

The dataset is organized into `train` and `test` directories. The `train` directory contains 65 subdirectories, each representing a class (0-64).

## Model Architecture
The model is a CNN with the following layers:
- **Input Layer**: 160x160 grayscale images.
- **Convolutional Layers**: 5 layers with ReLU activation and max pooling.
- **Dense Layers**: 1 hidden layer with 1024 units and ReLU activation.
- **Output Layer**: 65 units with softmax activation (for 65 classes).

## Training
The model was trained for 50 epochs using the Adam optimizer with a learning rate of 0.001. Data augmentation techniques like random rotation and zoom were applied to improve generalization.

### Training Results
- **Training Accuracy**: 95.39%
- **Validation Accuracy**: 90.02%

## Results
The model achieved a validation accuracy of **90.02%**. Predictions for the test dataset are saved in `predictions.csv`.
