
# 🚗 Self-Driving Car Segmentation with UNet & FCN8s

This project implements semantic segmentation for self-driving car scenarios using two popular deep learning architectures: **UNet** and **FCN8s**. The goal is to segment drivable areas from road scene images using pixel-level classification.

---

## 📌 Project Overview

- **Models Used**: UNet and FCN8s (Fully Convolutional Network)
- **Framework**: PyTorch
- **Tasks**:
  - Load and preprocess datasets
  - Build and train models
  - Evaluate using Dice coefficient, IoU, and loss
  - Perform inference on custom images

---

## 📁 Dataset Structure

The dataset consists of images and their corresponding segmentation masks. The expected directory structure is:

```
dataset/
├── train/
│   ├── images/
│   └── masks/
├── val/
│   ├── images/
│   └── masks/
└── test/
    ├── images/
    └── masks/
```

Update paths in the notebook as needed.

---

## 🧠 Model Architectures

- **UNet**:
  - U-shaped encoder-decoder
  - Skip connections for spatial context
- **FCN8s**:
  - Encoder with transposed convolutions
  - Skip connections at multiple resolutions

---

## ⚙️ How to Run

1. **Install Dependencies**:
   ```bash
   pip install torch torchvision albumentations matplotlib opencv-python tqdm
   ```

2. **Launch the Notebook**:
   Open and run `Self_Driving_Cars_with_UNet_and_FCN8s.ipynb`.

3. **Update Dataset Paths**:
   Modify image and mask paths in the notebook to point to your dataset.

4. **Train Models**:
   Run the training cells to train UNet and FCN8s. Loss and Dice graphs will be plotted automatically.

5. **Evaluate and Test**:
   Evaluate both models on the validation and test datasets. Compare performance using Dice and IoU.

6. **Run Inference**:
   Upload your own image in Colab:
   ```python
   from google.colab import files
   uploaded = files.upload()
   ```
   Then use `run_inference()` to visualize predictions.

---

## 📊 Metrics & Results

The models are evaluated using:

- **Dice Coefficient**
- **Intersection over Union (IoU)**
- **Mean IoU (mIoU)**
- **Loss Curves**

Graphs and scores are printed during training and testing.

---

## 📦 File Summary

| File | Description |
|------|-------------|
| `Self_Driving_Cars_with_UNet_and_FCN8s.ipynb` | Main notebook with full training and evaluation pipeline |

---

## 📝 License

This project is licensed under the **MIT License**. Feel free to use and modify for your own research or learning.

---

## ✍️ Author

Made for educational and research purposes in semantic segmentation and computer vision for self-driving applications.
