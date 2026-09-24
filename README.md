# Handwritten Gurumukhi Character Recognition Using Random Forest

## Project Overview

This project develops a machine learning system for recognizing handwritten Gurumukhi characters using a Random Forest classifier. The system processes character images, extracts suitable feature representations, trains and evaluates the model, and predicts unseen handwritten characters.

## Dataset

The project uses a publicly available labeled dataset containing **12,128 handwritten character images across 41 classes**. The images are converted to grayscale, resized to **32 × 32 pixels**, and normalized before being used for classification.

The dataset is divided into **9,702 training images and 2,426 testing images** using a stratified 80:20 split.

## Methodology

The images are preprocessed and represented using two feature approaches:

- Raw pixel features
- Histogram of Oriented Gradients (HOG)

Random Forest classifiers are trained using both representations. Hyperparameter tuning is then performed using RandomizedSearchCV to improve the final model.

## Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Raw Pixels + Random Forest | 95.75% | 95.80% | 95.76% | 95.74% |
| HOG + Random Forest | 78.52% | 79.03% | 78.52% | 78.46% |
| Tuned Random Forest | **96.54%** | **96.65%** | **96.54%** | **96.53%** |

The tuned Random Forest model achieved the highest performance with an accuracy of **96.54%** on the test dataset.

## Evaluation

The model is evaluated using accuracy, precision, recall, F1-score, and a confusion matrix. Additional visualizations are used to analyze class distribution, predictions, misclassified images, and prediction confidence.

The trained model is also tested on an unseen handwritten character image.

## Technologies Used

Python, Google Colab, NumPy, Pandas, Pillow, Scikit-learn, Scikit-image, Matplotlib, and Seaborn.

## Repository Contents

The repository contains the complete Google Colab notebook used for dataset exploration, preprocessing, feature extraction, model training, hyperparameter tuning, evaluation, and prediction.

## Conclusion

The project demonstrates the use of Random Forest for handwritten Gurumukhi character recognition. The experiments show that raw pixel features performed better than HOG features for the selected Random Forest configuration, while hyperparameter tuning further improved the model's performance.
