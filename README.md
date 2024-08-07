# Gesture UI - Project 2 (2024)

## Overview

This project involves building and comparing multiple convolutional neural network (CNN) models to identify hand gestures from a dataset of images. The dataset was sourced from the HaGRID project on Kaggle. The focus is on developing an effective gesture recognition model and evaluating its performance.

## Objective

- Preprocess the image dataset.
- Train and compare multiple CNN models, including models from scratch and using transfer learning.
- Evaluate model performance based on accuracy, validation loss, and computational efficiency.

## Dataset Description

- **Source**: [HaGRID Dataset](https://www.kaggle.com/datasets/kapitanov/hagrid)
- **Features**: 125,912 images resized to 512x512 pixels, divided into 18 gesture classes.
- **Data Splits**:
  - Training Set: 70%
  - Validation Set: 10%
  - Test Set: 20%

## Methodology

### Data Preprocessing

- **Image Resizing**: Reduced image size to 128x128 pixels to accommodate hardware limitations.
- **RGB vs. Grayscale**: Compared the performance of models trained on RGB and grayscale images.
- **Data Augmentation**: Applied random rotations, flips, and shifts to enhance training variability.

### Model Training

1. **Basic CNN**: Constructed from scratch with three convolutional layers.
2. **VGG-16 Transfer Learning**: Used VGG-16 architecture pre-trained on ImageNet.
3. **Deep CNN**: Utilized a deeper CNN architecture with five convolutional blocks.
4. **Deep CNN (Grayscale)**: Trained on grayscale images with a simplified architecture.

### Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **Training and Inference Time**

## Results

### Model Performance

- **Basic CNN**: Training accuracy of 6.13%, validation accuracy of 6.76%.
- **VGG-16 Model**: Training accuracy of 60.43%, validation accuracy of 57.99%.
- **Deep CNN**: Training accuracy of 98.57%, validation accuracy of 90.07%.
- **Deep CNN (Grayscale)**: Training accuracy of 91.27%, validation accuracy of 80.00%.

### Inference Times

- **Basic CNN**: 72.2 seconds per epoch.
- **VGG-16 Model**: 252-258 seconds per epoch.
- **Deep CNN**: 202 seconds per epoch.
- **Deep CNN (Grayscale)**: 203 seconds per epoch.

### Real-World Testing

Tested models on a separate set of real-world gesture images:
- **Deep CNN**: Failed to correctly classify any gestures.
- **Deep CNN (Grayscale)**: Correctly predicted one gesture, indicating better real-world applicability.

## Conclusion

This project explored the efficacy of various CNN architectures for hand gesture recognition. The Deep CNN model achieved the highest validation accuracy but struggled with real-world data, likely due to overfitting. The simpler Deep CNN (Grayscale) model, despite lower training metrics, demonstrated better generalization to new data. Future work should focus on optimizing models for real-world application and exploring additional techniques to improve robustness and accuracy.

## Deliverables

- **Report**: Detailed methodology, results, and conclusions.
- **Code**: Python notebooks/.py files for data preprocessing, model training, and evaluation.
