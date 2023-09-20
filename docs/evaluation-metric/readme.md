# Image Quality Metrics: PSNR and SSIM

## Table of Contents

- [Introduction](#introduction)
- [PSNR (Peak Signal-to-Noise Ratio)](#psnr-peak-signal-to-noise-ratio)
  - [Definition](#definition)
  - [Calculation](#calculation)
  - [Interpretation](#interpretation)
- [SSIM (Structural Similarity Index)](#ssim-structural-similarity-index)
  - [Definition](#definition-1)
  - [Calculation](#calculation-1)
  - [Interpretation](#interpretation-1)

## Introduction

When working on image processing tasks, especially tasks like denoising, super-resolution, and restoration, it's crucial to have quantitative metrics to evaluate the quality of the processed images compared to their original counterparts. PSNR and SSIM are two widely used metrics for this purpose.

## PSNR (Peak Signal-to-Noise Ratio)

### Definition

PSNR is a popular metric used to measure the quality of reconstructed images. It describes the ratio between the maximum possible power of an image (signal) and the power of corrupting noise that affects its fidelity.

### Calculation

\[ \text{PSNR} = 10 \times \log_{10}\left(\frac{\text{MAX}_I^2}{\text{MSE}}\right) \]

Where:
- \( \text{MAX}_I \) is the maximum possible pixel value of the image. For an 8-bit grayscale image, it is 255.
- \( \text{MSE} \) is the Mean Squared Error between the original and the reconstructed image.

### Interpretation

- PSNR values are usually expressed in terms of the logarithmic decibel scale. 
- A higher PSNR indicates that the reconstruction is of high quality. However, in some cases, images with high PSNR may appear to be of lower quality to human observers.

## SSIM (Structural Similarity Index)

### Definition

SSIM is an index that measures the similarity between two images. It provides a more intuitive quality metric than mathematical error metrics like MSE or PSNR, as it considers changes in structural information, texture information, and luminance.

### Calculation

The SSIM index is calculated on various windows of an image. The measure between two windows \( x \) and \( y \) of common size \( K \times K \) is:

\[ \text{SSIM}(x,y) = \frac{(2\mu_x\mu_y + c_1)(2\sigma_{xy} + c_2)}{(\mu_x^2 + \mu_y^2 + c_1)(\sigma_x^2 + \sigma_y^2 + c_2)} \]

Where:
- \( \mu_x \) is the average of \( x \)
- \( \mu_y \) is the average of \( y \)
- \( \sigma_x^2 \) is the variance of \( x \)
- \( \sigma_y^2 \) is the variance of \( y \)
- \( \sigma_{xy} \) is the covariance of \( x \) and \( y \)
- \( c_1 \) and \( c_2 \) are two variables to stabilize the division with weak denominator.

### Interpretation

- SSIM values range from -1 to 1, where 1 indicates the two images being compared are identical.
- A value of 0 indicates no structural similarity, and a value of -1 indicates that the structural information of the images is completely different.
- It's a popular metric because it tends to align well with the human visual system's perception of quality.

---

**Note**: This documentation aims to provide an overview of PSNR and SSIM. To delve deeper into these topics, refer to foundational papers and specialized texts.
