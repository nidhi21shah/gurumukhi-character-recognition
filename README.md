# Handwritten Gurumukhi Character Recognition Using Random Forest

## Project Overview

This project develops a machine learning system for recognizing handwritten Gurumukhi characters using a Random Forest classifier. The system preprocesses character images, generates feature representations, trains and evaluates the classifier, and predicts unseen handwritten character images.

## Dataset

The project uses a publicly available labeled dataset containing 12,128 handwritten character images across 41 classes. The original images are 256 × 256 pixels and are converted to grayscale, resized to 32 × 32 pixels, and normalized during preprocessing.

A stratified 80:20 train-test split is used, resulting in 9,702 training images and 2,426 testing images.

## Methodology

The project follows these main steps:

- Dataset exploration and visualization
- Image preprocessing
- Raw pixel feature extraction
- HOG feature extraction
- Random Forest model training
- Hyperparameter tuning using RandomizedSearchCV
- Model evaluation
- Prediction of unseen handwritten characters

Two feature representations were compared: normalized raw pixel values and Histogram of Oriented Gradients (HOG).

## Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Raw Pixels + Random Forest | 95.75% | 95.80% | 95.76% | 95.74% |
| HOG + Random Forest | 78.52% | 79.03% | 78.52% | 78.46% |
| Tuned Random Forest | **96.54%** | **96.65%** | **96.54%** | **96.53%** |

The tuned Random Forest model achieved an accuracy of 96.54% on the test dataset.

## Final Model

The final model uses normalized raw pixel features with a tuned Random Forest classifier.

The selected parameters are:

- Number of estimators: 400
- Maximum depth: 30
- Minimum samples split: 2
- Minimum samples leaf: 2
- Maximum features: log2

## Evaluation

The model was evaluated using accuracy, precision, recall, F1-score, and a confusion matrix. Additional visualizations were used to examine class distribution, sample images, model performance, misclassified images, and prediction confidence.

The final model was also tested on an unseen handwritten character image.

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Pillow
- Scikit-learn
- Scikit-image
- Matplotlib
- Seaborn

## Repository Structure

```text
gurumukhi-character-recognition/
│
├── documentation/
│   └── Project_Documentation.pdf
│
├── results/
│   └── Project result visualizations
│
├── Gurmukhi_Handwritten_Character_Recognition_using_Random_Forest.ipynb
├── gurumukhi_class_labels.json
├── requirements.txt
└── README.md
