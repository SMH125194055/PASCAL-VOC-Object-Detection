# PASCAL VOC 2007 Object Detection and Classification

## Project Overview
This project implements a **multi-label classification** and **object detection** system using the **PASCAL VOC 2007** dataset. The model is built using **transfer learning** with **MobileNetV2** as a feature extractor and follows a **multi-task learning** paradigm to predict both bounding boxes and class labels simultaneously.

---

## 🔑 Key Features
- **Multi-task Learning**: Joint object localization (bounding box regression) and classification.
- **Data Augmentation**: Extensive image augmentations to improve model generalization.
- **Transfer Learning**: MobileNetV2 pre-trained on ImageNet used as a fixed feature extractor.
- **Focal Loss**: Addresses class imbalance effectively.
- **Image Processing**: Smart padding and resizing while maintaining aspect ratio.

---

## 🧠 Technical Details

- **Dataset**: [PASCAL VOC 2007](http://host.robots.ox.ac.uk/pascal/VOC/voc2007/) (20 object classes)

### Model Architecture
- **Base**: MobileNetV2 (with frozen weights)
- **Heads**:
  - **Classification Head**: For multi-label class prediction
  - **Regression Head**: For bounding box prediction

### Training
- **Optimizer**: Adam
- **Loss Functions**:
  - **Classification**: Focal Loss
  - **Bounding Box**: Mean Squared Error (MSE)

### Evaluation Metrics
- **Classification Accuracy**: Multi-label accuracy
- **Bounding Box**: Mean Intersection over Union (mIoU)

---

## 📈 Results
- **Classification Accuracy**: ~85%
- **Bounding Box Prediction**: ~0.75 mIoU

---
