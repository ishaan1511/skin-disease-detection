# Skin Disease Detection Model

## Abstract

Skin disease detection using deep learning has shown promising results; however, many existing approaches rely on general-purpose convolutional neural networks that are not explicitly optimized for dermatological variability. In this work, we present a skin disease detection model designed to outperform widely adopted CNN benchmarks by improving class-level discrimination and robustness. Through systematic evaluation against ResNet, EfficientNet, and MobileNetV2, we demonstrate consistent gains in per-class accuracy, highlighting the model’s suitability for clinically meaningful deployment.

## 1. Introduction

Early and accurate detection of skin diseases is critical for effective treatment and improved patient outcomes. Recent advances in convolutional neural networks (CNNs) have enabled automated image-based diagnosis to approach the performance of dermatologists in controlled settings. Despite this progress, real-world deployment remains challenging due to factors such as visual similarity between diseases, class imbalance, and high intra-class variation.

Most existing skin disease classification systems rely on architectures originally designed for generic object recognition. While these models perform well in aggregate, they often exhibit unstable performance across disease classes—an issue that is particularly problematic in medical applications where reliability is paramount. This work introduces a **dedicated skin disease detection model** that explicitly targets these limitations and aims to surpass strong CNN baselines in both accuracy and class-wise consistency.




## 2. Benchmark Architectures

To evaluate the robustness and generalization performance of our skin disease detection system, we benchmarked three widely used convolutional neural network architectures:

- **ResNet** – a deep residual network known for stable optimization in medical imaging tasks  
- **EfficientNet** – a parameter-efficient architecture that scales depth, width, and resolution  
- **MobileNetV2** – a lightweight model optimized for deployment on resource-constrained devices  

Each model was trained and evaluated on the same skin disease dataset under identical preprocessing and evaluation protocols.

### Per-Class Accuracy Results

The following plots show **class-wise accuracy across all skin disease categories** for each benchmark model.  
These visualizations help identify which conditions are consistently well-classified and which remain challenging across architectures.

### ResNet – Per-Class Accuracy
![ResNet Per-Class Accuracy](resnet_per_class_accuracy.png)

### EfficientNet – Per-Class Accuracy
![EfficientNet Per-Class Accuracy](efficientnet_per_class_accuracy.png)

### MobileNetV2 – Per-Class Accuracy
![MobileNetV2 Per-Class Accuracy](mobilenetv2_per_class_accuracy.png)

## 4. Benchmark Analysis

Our analysis reveals that while benchmark models achieve strong average performance, they share several limitations:

- Performance varies significantly across disease classes, particularly for visually similar conditions  
- Rare or underrepresented classes consistently exhibit lower accuracy  
- Increasing model capacity alone does not resolve fine-grained classification errors  

These findings indicate that general-purpose CNN architectures are insufficient for capturing the nuanced visual patterns required for reliable skin disease detection.

## 5. Our Model

