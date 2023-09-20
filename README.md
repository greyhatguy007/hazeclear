# AI-ML based Intelligent de-hazing algorithm

## Introduction

This project aims to develop a deep learning model to dehaze images. Image dehazing is pivotal for enhancing visual clarity in various applications in computer vision tasks. The model is constructed using an encoder-decoder architecture in PyTorch.

## Dataset

We are utilizing the [Dense-Haze dataset](https://www.kaggle.com/datasets/rajat95gupta/hazing-images-dataset-cvpr-2019) available on Kaggle. This dataset contains 55 pairs of hazy and non-hazy images, making it a suitable benchmark for image dehazing tasks.

## Project Steps

1. **Data Preprocessing**:
    - Resize images and normalize pixel values.

2. **Model Development**:
    - Design an encoder-decoder neural network architecture.
    - Initialize model layers, including convolutional layers, pooling layers, and upsampling layers.
    - Define the forward propagation mechanism.

3. **Training the Model**:
    - Define loss function (Mean Squared Error) and optimizer (Adam).
    - Train the model using the training dataset.

4. **Model Evaluation**:
    - Compute evaluation metrics, including Peak Signal to Noise Ratio (PSNR) and Structural Similarity Index (SSIM).

5. **Results Visualization**:
    - Showcase original, hazy, and dehazed images side by side.
    - Plot training loss and validation loss across epochs.

6. **Optimization (if necessary)**:
    - Tune hyperparameters, such as learning rate, batch size, and number of epochs.
    - Modify the model architecture by adding more layers or changing layer configurations.
    - Implement data augmentation to artificially increase the training dataset size and robustness.

7. **Deployment**:
    - Convert the trained model into a format suitable for deployment.
    - Integrate the model into a web or mobile application for real-time image dehazing.

## Technical Details

- **Framework**: PyTorch
- **Model Architecture**: [Encoder-Decoder CNN](./docs/encoder-decoder-architecture/)
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam
- **Evaluation Metrics**: [PSNR, SSIM](./docs/evaluation-metric/readme.md)

## Future Work

1. Experiment with advanced architectures like U-Net or ResNet.
2. Implement a custom loss function for improved performance.
3. Enhance the deployment solution to process video streams for real-time dehazing.

## Contributions

Contributions to this project are welcome. Please ensure that you adhere to the project's coding and documentation standards.

## Acknowledgments

Special thanks to the creators of the Dense-Haze dataset for making it publicly available on Kaggle.
