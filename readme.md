# Image Anomaly Detection with Convolutional Autoencoder

Machine learning project to explore and learn about **unsupervised anomaly detection** for images and how to apply **Convolutional Autoencoder** on the **MVTec AD** dataset. My system learns to reconstruct "normal" samples and measures reconstruction errors to detect anomalies.

## Project Summary
- **Model**: 
    - Convolutional Autoencoder
    - Architecture: Encoder -> Bottleneck -> Decoder
    - Training: on normal samples only

- **Anomaly Scoring**:
    - Pixel-wise MSE
    - Structural SSIM, 1-SSIM
    - Patch-level error 95th percentile for local anomalies

- **Thresholds**:
    - Compared strategies: k_sigma, median+MAD, Youden J, Recall target
    - Handling class imbalance

## Metrics
- **ROC-AUC**: 0.80
- **F1-Score**: 0.87
- **Precision**: 91%
- **Recall**: 83%
- Visualization with **Confusion matrix, ROC/PR curve, error heatmap**

## Best practices applied
- Reproducible pipeline with fixed seed and preprocessing
- Youden J and Recall constraints to tune Threshold
- Extensive visualization with heatmap plots and original vs. reconstructed plots
- Ensemble scoring strategy to best evaluate the model

## About me
- Author: Andrés C. Meneguzzo
- Email: andres.meneguzzo@gmail.com
- Phone: +39 344-289-6968
- Linkedin: https://www.linkedin.com/in/andr%C3%A9s-christian-meneguzzo-12b00631b/