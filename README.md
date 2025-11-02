# PCA From Scratch --- Image Compression & Eigenfaces

This project implements **Principal Component Analysis (PCA)**
completely **from scratch** (without using `numpy.linalg` or
scikit-learn's PCA).\
It demonstrates how PCA can be used for **dimensionality reduction**,
**image compression**, and **face recognition (Eigenfaces)**.

------------------------------------------------------------------------

## 🚀 Features

-   Manual implementation of PCA (no `np.cov`, `np.linalg.eig`, or
    `sklearn.decomposition.PCA`)
-   Uses **Power Iteration** to compute eigenvalues and eigenvectors
-   Works on:
    -   A color image (`china.jpg`) from scikit-learn
    -   A grayscale image (`camera`)
    -   The **Olivetti Faces** dataset (face compression and eigenface
        visualization)
-   Visualizes:
    -   Original vs reconstructed images
    -   Top eigenfaces (principal components)

------------------------------------------------------------------------

## 🧩 How It Works

1.  **Mean Centering**\
    Each feature (pixel intensity) is centered by subtracting its mean.

2.  **Covariance Matrix Calculation**\
    Covariance between all feature pairs is computed manually with
    nested loops.

3.  **Power Iteration Method**\
    The largest eigenvalues and corresponding eigenvectors of the
    covariance matrix are found using iterative approximation.

4.  **Projection & Reconstruction**

    -   Compression: Data is projected onto the top *n* eigenvectors.\
    -   Decompression: Data is reconstructed from this reduced
        representation.

------------------------------------------------------------------------

## 📊 Results

### 🏙️ 1. RGB and grayscale Image Compression

Reduces a 3-channel RGB image to just 2 principal components and
reconstructs it.

Compresses the classic "camera" image using 50 PCA components.


------------------------------------------------------------------------

### 👤 2. Olivetti Faces --- Eigenfaces

Uses PCA to extract the **top 10 eigenfaces** and reconstruct faces from
compressed representations.

  Top Eigenfaces                    Original vs Reconstructed Faces
  --------------------------------- ----------------------------------
  Principal patterns in face data   Shows quality of PCA compression


------------------------------------------------------------------------

## 📘 Educational Value

This project is perfect for learning: - How PCA mathematically reduces
dimensionality - How covariance and eigenvectors work - How to compute
eigenvalues via iterative methods - How PCA can reconstruct approximate
images from fewer components

