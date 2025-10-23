# Model Experiments: Classification Benchmarks

This repository is for testing and comparing lightweight image classification models optimized for mobile and edge deployment. The goal is to explore performance, quantization effects, and export options for real-world applications.

## Models Tested

### 1. MobileNet V3
- Docs: [Hugging Face TIMM](https://huggingface.co/docs/timm/en/models/mobilenet-v3)
- Tutorial: [YouTube Video](https://www.youtube.com/watch?v=5JAZiue-fzY)
- Size: ~17 MB
- Notes:
  - Downloaded via Keras API, then exported as a standalone `.h5` or `.tflite` file.
  - Designed for efficiency and serves as a strong baseline for mobile image classification.

### 2. Quantized ResNet
- Explanation: [ResNet Deep Dive](https://www.youtube.com/watch?v=Ky3R0gxFUbo)
- Quantization Tutorial: [Quantizing ResNet](https://www.youtube.com/watch?v=jNZ1rkIfwsM)
- Size: 90.8 MB before quantization, 22.8 MB after
- Notes:
  - Standard ResNet architecture fine-tuned and quantized to int8 for mobile deployment.
  - Used to test accuracy vs. performance trade-offs compared to MobileNet V3.

### 3. TensorFlow Lite (TFLite)
- Framework used for model conversion, quantization, and on-device inference.
- Enables running both MobileNet V3 and Quantized ResNet efficiently on Android and iOS.

### Dataset
[Breast Ultrasound Images Dataset](https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset/data)

## Goals
- Compare accuracy, model size, and inference latency.
- Evaluate quantization impact on model performance.
- Prepare models for deployment in mobile and offline environments.
