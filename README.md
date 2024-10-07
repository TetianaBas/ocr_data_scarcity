# Handwriting Recognition Under Data Scarcity: Ukrainian Use Case

## Overview

The initial aim of this project was to develop a system for recognizing Ukrainian characters. While a dataset containing 28,000 samples of Cyrillic handwritten characters (CoMNIST) was available, it was created in Russia and featured Soviet Union-related imagery. As a Ukrainian I have ethical considerations that made me to choose not to use this dataset. Instead I generated a small datset myself (yes, manually). I integrated my small dataset with external dataset 'Rukopys' of the same size, resulting in 20-30 samples/category dataset with 34 categories. I explored varaious CNN architectured for OCR however all faied due to data scarcity. This data scarcity condition prompted a shift in focus to explore data augmentation techniques, applying machine learning frameworks under conditions of data scarcity. The goal became analogous to developing OCR for a rare language with minimal written samples, necessitating innovative approaches to overcome the limitations. 

## Objectives

- Develop a model for Ukrainian handwriting recognition with minimal data.
- Explore and implement data augmentation techniques to increase the dataset’s effectiveness.
- Train and evaluate machine learning models under constrained data conditions.

## Features

- **Dataset Generation**: A manually created dataset was merged with the external 'Rukopys' dataset to expand the variety of samples.
- **Data Augmentation**: Techniques such as Gaussian noise reduction, grayscale conversion, thresholding, and normalization were applied to standardize the images.
- **Dimensionality Reduction**: PCA and t-SNE were used for feature extraction and visualization.
- **Variational Autoencoders (VAEs)**: Implemented for generating synthetic data and improving the model's ability to generalize.

## Installation

Ensure that you have the following libraries installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-image scikit-learn tensorflow keras opencv-python
```

## Usage

1. **Data Preprocessing**: Preprocess images using the provided scripts to convert them to grayscale, apply Gaussian blur, and resize.
2. **Dataset Augmentation**: Utilize `ImageDataGenerator` for augmenting the dataset.
3. **Model Training**: Train models using VAE or CNN architectures. 
4. **Evaluation**: Evaluate the models using the test set and visualize the results using t-SNE and PCA.

## Results

- The final dataset included original and augmented samples, improving model robustness.
- PCA and t-SNE visualizations highlighted the feature distribution, guiding further tuning of the models.
- The VAE-based synthetic data generation proved effective in balancing the dataset and enhancing model performance.

## Ethical Considerations

The decision to create a new dataset stems from the ethical implications of using datasets associated with unwanted imagery. This approach ensures that the project aligns with ethical research practices while promoting inclusive and responsible AI development.

## References

- [Rukopys Dataset](https://github.com/lynnporu/rukopys-dataset)
