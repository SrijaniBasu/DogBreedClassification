# Dog Breed Classification (CNN on Kaggle Dog Breed Dataset)

This project trains a Convolutional Neural Network (CNN) to classify dog images into three breeds using the **Kaggle Dog Breed Identification**-style dataset.

The workflow is implemented in a single Jupyter/Colab notebook and covers:
- Downloading the dataset from Kaggle
- Preprocessing and loading images
- Building and training a CNN model with Keras
- Evaluating test accuracy
- Saving the trained model (`dog_breed.h5`)

---

## 1. Project Overview

**Goal:**  
Given an input image of a dog, the model predicts which one of the following breeds it belongs to:

- `scottish_deerhound`
- `maltese_dog`
- `bernese_mountain_dog`

**Key Steps:**
1. Use Kaggle API to download the dataset.
2. Load labels from `labels.csv` and filter only the three selected breeds.
3. Load and resize images to `224 x 224`.
4. One-hot encode breed labels.
5. Train a CNN with multiple convolution + max-pooling layers.
6. Evaluate the model on a held-out test set.
7. Visualize training vs validation accuracy.
8. Save the trained model for later use.

---

## 2. Dataset

The notebook downloads the dataset from Kaggle:

```bash
kaggle datasets download catherinehorng/dogbreedidfromcomp
