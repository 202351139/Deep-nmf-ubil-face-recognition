# Deep Non-Negative Matrix Factorization for Face Recognition

This project implements a practical reproduction of the paper:

**Deep Non-Negative Matrix Factorization Architecture Based on Underlying Basis Images Learning**

Authors: Yang Zhao, Huiyang Wang, Jihong Pei

Published in IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI), 2021.

## Project Overview

The project implements and compares three approaches:

1. Non-Negative Matrix Factorization (NMF)
2. Deep Non-Negative Basis Matrix Factorization (DNBMF)
3. Regularized Deep Non-Negative Basis Matrix Factorization (RDNBMF)

The models are evaluated for face recognition using the Olivetti Faces dataset.

## Methodology

For standard NMF:

X = WH

For deep NMF:

X = W2 H2 H1

The learned representations are used for face recognition with a 1-Nearest Neighbor classifier.

## Dataset

Olivetti Faces dataset from scikit-learn.

- 400 face images
- 40 subjects
- 10 images per subject
- Image size: 64 × 64

The dataset is divided into training and testing sets using a stratified 75/25 split.

## Parameters

- NMF rank: 40
- Deep NMF ranks: 40 and 20
- Maximum iterations: 300
- Regularization parameter: 0.05
- Classifier: 1-Nearest Neighbor

## Implemented Features

- Dataset loading and preprocessing
- NMF implementation
- DNBMF implementation
- RDNBMF implementation
- Feature extraction using Moore-Penrose pseudo-inverse
- Face recognition using 1-NN
- Accuracy comparison
- Convergence plots
- Basis image visualization
- Image reconstruction
- Confusion matrices
- Classification reports

## Results

The notebook generates the following results:

- Recognition accuracy comparison
- Convergence comparison
- Learned basis images
- Original vs reconstructed images
- Confusion matrices
- Classification reports

The implementation results are generated when the notebook is executed.

## How to Run

### Google Colab

Upload `Deeplearning_project.ipynb` to Google Colab and run the cells sequentially.

### Local Environment

Install the required packages:

```bash
pip install -r requirements.txt
