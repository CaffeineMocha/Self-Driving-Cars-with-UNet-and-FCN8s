
# Self-Driving Car Segmentation with UNet & FCN8s

This project implements semantic segmentation for self-driving car scenarios using two deep learning architectures: UNet and FCN8s. The objective is to identify drivable areas from road scene images using pixel-level classification.

---

## Project Overview

- Models Used: UNet and FCN8s (Fully Convolutional Network)
- Framework: PyTorch
- Tasks:
  - Load and preprocess datasets
  - Build and train models
  - Evaluate using Dice coefficient, IoU, and loss
  - Perform inference on custom images

---

## Dataset Structure

The dataset should be organized as follows:

```
dataset/
├── train/
│   ├── images/
│   └── masks/
└── test/
    ├── images/
    └── masks/
```

Please update the dataset paths in the notebook accordingly.

---

## Model Architectures

- UNet:
  - U-shaped encoder-decoder
  - Skip connections for spatial context

- FCN8s:
  - Encoder with transposed convolutions
  - Skip connections at multiple resolutions

---

## How to Run

1. Install dependencies:
   ```bash
   pip install torch torchvision albumentations matplotlib opencv-python tqdm
   ```

2. Launch the notebook:
   Open and run `Self_Driving_Cars_with_UNet_and_FCN8s.ipynb`.

3. Update dataset paths:
   Make sure the image and mask folder paths are correctly set in the notebook.

4. Train models:
   Run the training cells to train UNet and FCN8s. Training and validation performance will be plotted.

5. Evaluate and test:
   Evaluate both models using test data. Metrics include Dice and IoU.

6. Run inference:
   Upload an image in Google Colab:
   ```python
   from google.colab import files
   uploaded = files.upload()
   ```
   Use `run_inference()` to visualize predictions.

---

## Metrics and Results

The models are evaluated using:

- Dice Coefficient
- Intersection over Union (IoU)
- Mean IoU (mIoU)
- Loss Curves

Evaluation scores and plots are included in the notebook.

---

## File Summary

| File | Description |
|------|-------------|
| `Self_Driving_Cars_with_UNet_and_FCN8s.ipynb` | Main notebook with training, evaluation, and inference pipeline |

---

## License

This project is licensed under the MIT License.

---

## Author

Developed for educational and research purposes in semantic segmentation and autonomous driving.
